---
title: Microsoft 365 が Sender Policy Framework (SPF) を使用してスプーフィングを防止する方法
f1.keywords:
- CSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 12/15/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 3aff33c5-1416-4867-a23b-e0c0c5b4d2be
ms.collection:
- M365-security-compliance
description: '概要: この記事では、Microsoft 365 が DNS で Sender Policy Framework (SPF) TXT レコードを使用して、カスタムドメインから送信されたメッセージを宛先の電子メールシステムが信頼するようにする方法について説明します。 これは、Microsoft 365 から送信される送信メールに適用されます。 Microsoft 365 から Microsoft 365 内部の受信者に送信されるメッセージは、常に SPF に合格します。'
ms.openlocfilehash: d73fb881b8395c6c1383cca70e506694795f1364
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43633992"
---
# <a name="how-microsoft-365-uses-sender-policy-framework-spf-to-prevent-spoofing"></a>Microsoft 365 が Sender Policy Framework (SPF) を使用してスプーフィングを防止する方法

 **概要:** この記事では、Microsoft 365 が DNS で Sender Policy Framework (SPF) TXT レコードを使用して、カスタムドメインから送信されたメッセージを宛先の電子メールシステムが信頼するようにする方法について説明します。 これは、Microsoft 365 から送信される送信メールに適用されます。 Microsoft 365 から Microsoft 365 内部の受信者に送信されるメッセージは、常に SPF に合格します。

SPF TXT レコードは、DNS 形式のレコードです。SPF TXT レコードで、メール メッセージの送信元のドメイン名を確認すると、スプーフィングやフィッシングの防止に役立ちます。SPF は、送信者の IP アドレスを、送信側ドメインの所有者とされる名前と照合して、メール メッセージの発信元を確認します。

> [!NOTE]
> SPF レコードの種類は、2014 年にインターネット技術標準化委員会 (IETF) によって廃止されました。代わりに、SPF 情報を公開するには、DNS で TXT レコードを必ず使用してください。この記事の以降の部分では、わかりやすいように SPF TXT レコードという用語を使用します。

ドメイン管理者は DNS の TXT レコードで SPF 情報を公開します。 この SPF 情報は、承認された送信メール サーバーを識別します。 送信先メール システムにより、承認された送信メール サーバーからメッセージが発信されたことが確認されます。 既に SPF に精通している場合、または簡単に展開でき、Microsoft 365 の DNS で SPF TXT レコードに含める内容を知る必要がある場合は、「 [microsoft 365 で spf を設定](set-up-spf-in-office-365-to-help-prevent-spoofing.md)する」を参照して、スプーフィングを防止できます。 Microsoft 365 で完全にホストされている展開がない場合、または SPF の動作方法や、Microsoft 365 の SPF のトラブルシューティング方法の詳細については、「」を参照してください。

> [!NOTE]
> 以前は、SharePoint Online も使用している場合、カスタム ドメインに別の SPF TXT レコードを追加する必要がありました。 この作業を行う必要はなくなりました。 この変更により、SharePoint Online の通知メッセージが [迷惑メール] フォルダーに振り分けられるリスクが軽減されます。 すぐに変更する必要はありませんが、"参照が多すぎます" エラーが表示された場合は、「 [Microsoft 365 での spf の設定](set-up-spf-in-office-365-to-help-prevent-spoofing.md)」の説明に従って spf TXT レコードを変更して、スプーフィングを防止します。

## <a name="how-spf-works-to-prevent-spoofing-and-phishing-in-microsoft-365"></a>Microsoft 365 でのスプーフィングとフィッシングを防ぐための SPF のしくみ
<a name="HowSPFWorks"> </a>

SPF は、送信者がドメインの代理として送信することを許可されているかどうかを判断します。送信者がこの操作を許可されていない場合、つまり、受信側のサーバーで電子メールの SPF チェックが失敗した場合は、そのサーバー上で構成されたスパム ポリシーが、メッセージについて行う処理を決定します。

各 SPF TXT レコードには、SPF TXT レコードであるという宣言、ドメインからのメールの送信を許可されている IP アドレス、ドメインの代わりに送信できる外部ドメイン、および適用ルールの3つの部分が含まれています。 3つすべての有効な SPF TXT レコードを指定する必要があります。 この記事では、SPF TXT レコードを作成する方法と、Microsoft 365 のサービスを操作するためのベストプラクティスについて説明します。 ドメインレジストラーを使用してレコードを DNS に公開する手順へのリンクも提供されています。

### <a name="spf-basics-ip-addresses-allowed-to-send-from-your-custom-domain"></a>SPF の基本: カスタム ドメインからの送信が許可された IP アドレス
<a name="SPFBasicsIPaddresses"> </a>

SPF ルールの基本的な構文を見てみましょう。

v=spf1 \<IP\> \<enforcement rule\>

たとえば、contoso.com に対して次の SPF ルールが存在するとします。

v=spf1 \<IP address #1\> \<IP address #2\> \<IP address #3\> \<enforcement rule\>

この例では、SPF ルールは、ドメイン contoso.com について、これらの IP アドレスからのメールのみを受け入れるように受信電子メール サーバーに指示します。

- IP アドレス #1

- IP アドレス #2

- IP アドレス #3

この SPF ルールは受信メール サーバーに、メッセージが contoso.com からのものであるものの、これら 3 つの IP アドレスのいずれからのものでもない場合、受信側サーバーはメッセージに対して強制ルールを適用する必要があることを指示します。通常、強制ルールは次のオプションのいずれかです。

- **Hard fail。** メッセージ エンベロープ内に 'hard fail' を含むメッセージをマークし、受信側サーバーでこの種類のメッセージに対して構成されたスパム ポリシーに従います。

- **Soft fail。** メッセージ エンベロープ内に 'soft fail' を含むメッセージをマークします。通常、電子メール サーバーはこれらのメッセージを配信するように構成されます。ほとんどのエンド ユーザーには、このマークは表示されません。

- **Neutral。** 何もしません。つまり、メッセージ エンベロープをマークしません。通常、これはテスト用に予約されているものであり、ほとんど使用されません。

次の例は、さまざまな状況での SPF のしくみを示しています。これらの例では、contoso.com は送信者、woodgrovebank.com は受信者です。

### <a name="example-1-email-authentication-of-a-message-sent-directly-from-sender-to-receiver"></a>例 1:送信者から受信者に直接送信されるメッセージの電子メール認証
<a name="spfExample1"> </a>

SPF は、送信者から受信者へのパスが直接パスである場合に最適に機能します。次に例を示します。

![サーバーからサーバーへ直接送信されるときに SPF がメールを認証する方法を示す図。](../../media/835c20a7-ed4c-49c4-91fe-b8ebb3e452a1.jpg)

Woodgrovebank.com がメッセージを受け取る際に、IP アドレス # 1 が contoso.com の SPF TXT レコードにある場合は、メッセージは SPF チェックに合格し認証されます。

### <a name="example-2-spoofed-sender-address-fails-the-spf-check"></a>例 2:偽装された送信者のアドレスが SPF チェックに失敗する
<a name="spfExample2"> </a>

フィッシャーが contoso.com を偽装する方法を見つけたとします。

![偽装しているサーバーから送信されるときに SPF がメールを認証する方法を示す図。](../../media/235dac3d-cdc5-466e-86e0-37b5979de198.jpg)

IP アドレス #12 は contoso の SPF TXT レコードにないため、メッセージは SPF チェックに失敗し、受信者はそのメッセージをスパムとしてマークすることを選択できます。

### <a name="example-3-spf-and-forwarded-messages"></a>例 3:SPF と転送されたメッセージ
<a name="spfExample3"> </a>

SPF の欠点の1つは、メールが転送されたときに機能しないことです。 たとえば、woodgrovebank.com のユーザーが、outlook.com アカウントにすべての電子メールを送信する転送ルールを設定しているとします。

![電子メール メッセージが転送される際に SPF がメールを認証できないことを示す図。](../../media/6e92acd6-463e-4a1b-8327-fb1cf861f356.jpg)

このメッセージは最初、woodgrovebank.com で SPF チェックに合格していますが、outlook.com の SPF チェックに失敗します。 IP #25 は、contoso 社の SPF TXT レコードには含まれていません。 このため、Outlook.com はメッセージをスパムとしてマークする可能性があります。 この問題を回避するには、SPF を DKIM や DMARC などの他の電子メールの認証方法と組み合わせて使用します。

### <a name="spf-basics-including-third-party-domains-that-can-send-mail-on-behalf-of-your-domain"></a>SPF の基本:自分のドメインに代わってメールを送信できるサード パーティのドメインを含める
<a name="SPFBasicsIncludes"> </a>

IP アドレスに加えて、送信者としてドメインを含めるように SPF TXT レコードを構成することもできます。 これらは、"include" ステートメントとして SPF TXT レコードに追加されます。 たとえば、contoso.com には、所有する contoso.net と contoso.org からメール サーバーのすべての IP アドレスを含めることもできます。 これを行うには、contoso.com は次のような SPF TXT レコードを発行します。

```text
v=spf1 include:contoso.net include:contoso.org -all
```

受信側のサーバーは、このレコードを DNS に表示するときに、contoso.net の SPF TXT レコードに対する DNS 参照も行い、contoso.org に対しても実行します。Contoso.net または contoso.org のレコード内に追加の include ステートメントが見つかった場合は、それに従っていることになります。 サービス拒否攻撃を防止するための、1 つの電子メール メッセージに対する DNS 参照の最大数は 10 です。 各 include ステートメントは追加の DNS 参照を表します。 メッセージが上限 10 を超えると、メッセージは SPF チェックに失敗します。 メッセージがこの制限に達すると、受信側サーバーの構成方法によっては、"参照が多すぎます" または "メッセージの最大ホップ数を超えています" というメッセージが表示されることがあります (参照がループし、DNS のタイムアウトを超えた場合に発生する可能性があります)。 この問題を回避する方法に関するヒントについては、「 [Microsoft 365 の SPF のベストプラクティス](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot)」を参照してください。

## <a name="requirements-for-your-spf-txt-record-and-microsoft-365"></a>SPF TXT レコードと Microsoft 365 の要件
<a name="SPFReqsinO365"> </a>

Microsoft 365 をセットアップするときにメールを設定すると、ドメインの正当なメールソースとして Microsoft メッセージングサーバーを識別する SPF TXT レコードが既に作成されています。 このレコードは、おそらく次のようになります。

```text
v=spf1 include:spf.protection.outlook.com -all
```

完全にホストされている顧客、つまり、送信メールを送信するオンプレミスのメールサーバーが存在しない場合、これは Office 365 に対して発行する必要がある SPF TXT レコードのみです。

ハイブリッド展開がある場合 (つまり、社内のメールボックスと Microsoft 365 でホストされているメールボックスがあります。または、Exchange Online Protection (EOP) スタンドアロンのお客様 (つまり組織が EOP を使用してオンプレミスのメールボックスを保護している場合) は、各社内エッジメールサーバーの送信 IP アドレスを DNS の SPF TXT レコードに追加します。

## <a name="form-your-spf-txt-record-for-microsoft-365"></a>Microsoft 365 用の SPF TXT レコードの形成
<a name="FormYourSPF"> </a>

この記事に記載されている構文の情報を使って、カスタム ドメイン用の SPF TXT レコードを形成します。ここに記載されていない他の構文オプションもありますが、これらが最もよく使うオプションです。レコードを形成した後は、ドメイン レジストラーでレコードを更新する必要があります。

Microsoft 365 に含める必要のあるドメインの詳細については、「 [SPF に必要な外部 DNS レコード](https://docs.microsoft.com/office365/enterprise/external-domain-name-system-records)」を参照してください。 ドメインレジストラーの SPF (TXT) レコードを更新するための手順を順[を追って説明](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider#add-a-txt-record-for-spf-to-help-prevent-email-spam)します。

### <a name="spf-txt-record-syntax-for-microsoft-365"></a>Microsoft 365 の SPF TXT レコードの構文
<a name="SPFSyntaxO365"> </a>

Microsoft 365 の通常の SPF TXT レコードの構文は次のとおりです。

```text
v=spf1 [<ip4>|<ip6>:<IP address>] [include:<domain name>] <enforcement rule>
```

たとえば、

```text
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 include:spf.protection.outlook.com -all
```

各部分の意味は次のとおりです。

- **v=spf1** は必須です。これは、SPF TXT レコードとして TXT レコードを定義します。

- **ip4** は、IP バージョン 4 のアドレスを使用していることを示します。**ip6** は、IP バージョン 6 のアドレスを使用していることを示します。IPv6 の IP アドレスを使用している場合は、この記事の例の **ip4** を **ip6** に置き換えます。CIDR 表記を使用して IP アドレス範囲を指定することもできます (たとえば、**ip4:192.168.0.1/26**)。

- _IP address_ は、SPF TXT レコードに追加する IP アドレスです。 通常、これは組織の送信メール サーバーの IP アドレスです。 複数の送信メール サーバーを一覧表示できます。 詳細については、「[例: 複数のオンプレミスメールサーバーと Microsoft 365 のための SPF TXT レコード](how-office-365-uses-spf-to-prevent-spoofing.md#ExampleSPFMultipleMailServerO365)」を参照してください。

- _domain name_ は、正当な送信者として追加するドメインです。 Microsoft 365 に含める必要のあるドメイン名の一覧については、「 [SPF に必要な外部 DNS レコード](https://docs.microsoft.com/office365/enterprise/external-domain-name-system-records)」を参照してください。

- 通常、強制ルールは次のいずれかです。

  - -all

    hard fail を示します。ドメインに対するすべての承認済みの IP アドレスが既知の場合は、SPF TXT レコードにそれらを一覧表示して、-all (hard fail) 修飾子を使用します。また、SPF のみを使用している場合、つまり、DMARC または DKIM のいずれも使用していない場合は、-all 修飾子を使用する必要もあります。常にこの修飾子を使用することをお勧めします。

  - ~ all

    soft fail を示します。 IP アドレスの完全な一覧があるかどうかがわからない場合は、~ all (soft fail) 修飾子を使用する必要があります。 また、p=quarantine または p=reject と共に DMARC を使用している場合も、~all を使用できます。 それ以外の場合は、-all を使用します。

  - ? all

    neutral を示します。SPF のテスト時に使用されます。実際の展開でこの修飾子を使用することはお勧めしません。

### <a name="example-spf-txt-record-to-use-when-all-of-your-mail-is-sent-by-microsoft-365"></a>例: Microsoft 365 によってすべてのメールが送信されるときに使用する SPF TXT レコード
<a name="ExampleSPFNoSP"> </a>

すべてのメールが Microsoft 365 によって送信される場合は、SPF TXT レコードで次のように使用します。

```text
v=spf1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-a-hybrid-scenario-with-one-on-premises-exchange-server-and-microsoft-365"></a>例: 1 つの社内 Exchange サーバーと Microsoft 365 を使用したハイブリッドシナリオの SPF TXT レコード
<a name="ExampleSPFHybridOneExchangeServer"> </a>

ハイブリッド環境で、オンプレミスの Exchange Server の IP アドレスが 192.168.0.1 である場合、SPF の強制ルールを hard fail に設定するために、SPF TXT レコードを次のように形成します。

```text
v=spf1 ip4:192.168.0.1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-multiple-outbound-on-premises-mail-servers-and-microsoft-365"></a>例: 複数のオンプレミスメールサーバーと Microsoft 365 のための SPF TXT レコード
<a name="ExampleSPFMultipleMailServerO365"> </a>

送信メールサーバーが複数ある場合は、SPF TXT レコードに各メールサーバーの IP アドレスを含め、各 IP アドレスをスペースで区切った後に "ip4:" ステートメントを続けます。 以下に例を示します。

```text
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 ip4:192.168.0.3 include:spf.protection.outlook.com -all
```

## <a name="next-steps-set-up-spf-for-microsoft-365"></a>次の手順: Microsoft 365 用の SPF のセットアップ
<a name="SPFNextSteps"> </a>

SPF TXT レコードを作成したら、「 [Microsoft 365 での spf のセットアップ](set-up-spf-in-office-365-to-help-prevent-spoofing.md)」の手順に従って、スプーフィングがドメインに追加されるのを防ぐことができます。

SPF は、スプーフィングを防止するために設計されていますが、SPF で防御できないスプーフィングの手法があります。 これらを保護するために、SPF をセットアップした後は、Microsoft 365 の DKIM と DMARC も構成する必要があります。 開始するには、「 [DKIM を使用して、Microsoft 365 でカスタムドメインから送信される送信電子メールを検証する](use-dkim-to-validate-outbound-email.md)」を参照してください。 次に、「 [USE DMARC to validate email In Microsoft 365」](use-dmarc-to-validate-email.md)を参照してください。

## <a name="troubleshooting-best-practices-for-spf-in-microsoft-365"></a>トラブルシューティング: Microsoft 365 での SPF のベストプラクティス
<a name="SPFTroubleshoot"> </a>

カスタム ドメインに作成できる SPF TXT レコードは 1 つのみです。複数のレコードを作成すると、ラウンド ロビン状況の原因となり、SPF が失敗します。これを避けるために、各サブドメインに対して個別にレコードを作成できます。たとえば、contoso.com に 1 つのレコードを作成し、bulkmail.contoso.com に別のレコードを作成します。

メールメッセージが配信される前に10を超える DNS 参照を発生させると、受信側のメールサーバーは、 _permerror_とも呼ばれる永続的なエラーで応答し、メッセージが SPF チェックに失敗します。 また、受信側のサーバーは、次のようなエラーを含む配信不能レポート (NDR) で応答することもあります。

- メッセージのホップ数を超えました。

- メッセージに必要な参照数が多すぎます。

## <a name="avoiding-the-too-many-lookups-error-when-you-use-third-party-domains-with-microsoft-365"></a>Microsoft 365 でサードパーティのドメインを使用する場合の "参照が多すぎます" エラーを回避する
<a name="SPFTroubleshoot"> </a>

サード パーティのドメインの SPF TXT レコードには、受信側のサーバーに多数の DNS 参照を実行するよう指示するものがあります。たとえば、この記事の執筆時には、Salesforce.com のレコードに 5 つの include ステートメントが含まれています。

```text
v=spf1 include:_spf.google.com
include:_spfblock.salesforce.com
include:_qa.salesforce.com
include:_spfblock1.salesforce.com
include:spf.mandrillapp.com mx ~all
```

エラーを回避するために、(たとえばバルク メールを送信する) あらゆるユーザーがサブドメインを使用する必要があるというポリシーを、特にこの目的のために実装できます。次にバルク メールを含むサブドメイン用の別の SPF TXT レコードを定義します。

 salesforce.com の例などのように、SPF TXT レコードでドメインを使用する必要がある場合がありますが、サードパーティがこの目的のためにユーザーの使用するサブドメインを既に作成している場合もあります。 たとえば、exacttarget.com は、SPF TXT レコードに対して使用する必要があるサブドメインを作成しました。

```text
cust-spf.exacttarget.com
```

SPF TXT レコードにサード パーティのドメインを含む場合は、参照の上限値 10 に達することを回避するために、どのドメインまたはサブドメインを使用するかを、サードパーティに確認する必要があります。

## <a name="how-to-view-your-current-spf-txt-record-and-determine-the-number-of-lookups-that-it-requires"></a>現在の SPF TXT レコードを表示し、それに必要な参照数を決定する方法
<a name="SPFTroubleshoot"> </a>

nslookup を使用して、SPF TXT レコードなどの DNS レコードを表示できます。 また、ご希望に応じて、無料のオンライン ツールを多数入手し、SPF TXT レコードの内容を表示することもできます。 SPF TXT を参照し、一連の include ステートメントとリダイレクトに従って、レコードが必要とする DNS 参照数を判断できます。 オンライン ツールには、これらの参照数をカウントして表示するものもあります。 この数を継続的に追跡することで、組織から送信されたメッセージが、受信側のサーバーからの permerror と呼ばれる永続的なエラーの要因にならないようにできます。

## <a name="for-more-information"></a>関連情報
<a name="SPFTroubleshoot"> </a>

SPF TXT レコードを追加するにはヘルプが必要ですか? 「Microsoft [365 の任意の dns ホスティングプロバイダーで dns レコードを作成](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider#add-a-txt-record-for-spf-to-help-prevent-email-spam)する」に記載されている、「microsoft 365 でのカスタムドメインを使用した Sender Policy Framework の使用に関する詳細情報」を参照してください。 [スパム対策メッセージヘッダー](anti-spam-message-headers.md)には、Microsoft 365 が SPF チェックに使用する構文とヘッダーフィールドが含まれています。


