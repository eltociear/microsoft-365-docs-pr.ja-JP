---
title: Microsoft 365 に送信されるメールのトラブルシューティング
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f4caa4e1-e414-4b21-8822-31c08064c059
ms.collection:
- M365-security-compliance
description: この記事では、Microsoft 365 の受信トレイに電子メールを送信しようとしたときに問題が発生している送信者のトラブルシューティングに関する情報を提供し、顧客への一括メール送信のベストプラクティスを提供します。
ms.openlocfilehash: 89fd6d11cca0d7689203948922b27e46ae2c602a
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43631147"
---
# <a name="troubleshooting-mail-sent-to-office-365"></a>Office 365 に送信されるメールのトラブルシューティング

この記事では、Microsoft 365 の受信トレイに電子メールを送信しようとしたときに問題が発生している送信者のトラブルシューティングに関する情報を提供し、顧客への一括メール送信のベストプラクティスを提供します。

## <a name="troubleshooting-common-problems-with-mail-delivery-to-office-365"></a>Office 365 へのメール配信に関する一般的な問題のトラブルシューティング

一般的に見られる次の問題のいずれかを選択します。

- [IP およびドメインの評価の管理者ですか](#are-you-managing-your-ip-and-domains-sending-reputation)

- [新しい IP アドレスから電子メールを送信していますか](#are-you-sending-email-from-new-ip-addresses)

- [DNS が正しく設定されていることを確認する](#confirm-that-your-dns-is-set-up-correctly)

- [ルーティング不能な IP で自分をアドバタイズしていないことを確認する](#ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip)

- [Office 365 でユーザーに電子メールを送信すると、配信不能レポート (NDR) を受信する](#you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365)

- [送信した電子メールが、受信側の EOP の迷惑メール フォルダーに分類される](#my-email-landed-in-the-recipients-junk-folder-in-eop)

- [自分の IP アドレスからのトラフィックが EOP によって調整される](#traffic-from-my-ip-address-is-throttled-by-eop)

### <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a>IP およびドメインの評価の管理者ですか

EOP filtering technologies は、Microsoft 365 に加えて、Exchange Server、Microsoft Office Outlook、および Windows Live メールなどのその他の Microsoft 製品にスパム対策の保護を提供するように設計されています。 また、SPF、DKIM、DMARC も利用しています。電子メールを送信しているドメインが許可されていることを確認することによって、スプーフィングやフィッシングの問題に対処するための電子メール認証テクノロジ。 EOP のフィルター処理は、送信 IP、ドメイン、認証、リストの正確さ、苦情率、コンテンツなどに関連するいくつかの要因によって影響を受けます。 これらのうちの1つとして、送信者の評判と電子メールを配信する機能についての重要な要因の1つとして、迷惑メールの苦情率があります。

### <a name="are-you-sending-email-from-new-ip-addresses"></a>新しい IP アドレスから電子メールを送信していますか

通常、電子メールを送信するために初めて使用する IP アドレスには、当社のシステムで構築された評価はありません。その結果、新しい IP アドレスからの電子メールでは、配信の問題が発生する可能性が高くなります。迷惑メールを送信しないための評価が IP で構築されると、通常 EOP の電子メール配信エクスペリエンスは向上します。

既存の SPF レコードで認証されているドメインに追加される新しい IP アドレスの場合、通常、そのドメインの送信評価の一部を継承できるという利点があります。ご使用のドメインの送信評価が優れていると、新しい IP の評価もすぐに向上します。新しい IP は、ボリューム、配布リストの正確さ、迷惑メールの苦情の割合に応じて、数週間またはすぐにでも、評価が向上することを期待できます。

### <a name="confirm-that-your-dns-is-set-up-correctly"></a>DNS が正しく設定されていることを確認する

メールのルーティングに必要な MX レコードなど、DNS レコードの作成と保守の手順については、DNS ホスティング プロバイダーに確認する必要があります。

### <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a>ルーティング不能な IP で自分をアドバタイズしていないことを確認する

DNS 逆引き参照を行えない送信者からの電子メールは受け付けないことがあります。場合によっては、正当な送信者が、EOP に対して接続しようとするときに、インターネット ルーティング不能な IP で自身をアドバタイズすることがあります。プライベート (ルーティング不能な) ネットワーク用に予約されている IP アドレスは次のとおりです。

- 192.168.0.0/16 (または 192.168.0.0 ～ 192.168.255.255)

- 10.0.0.0/8 (または 10.0.0.0 ～ 10.255.255.255)

- 172.16.0.0/11 (または 172.16.0.0 ～ 172.31.255.255)

### <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a>Office 365 でユーザーに電子メールを送信すると、配信不能レポート (NDR) を受信する

一部の配信の問題の原因は、Microsoft によって送信者の IP アドレスがブロックされていることや、ユーザーのアカウントが以前の迷惑メール処理によって禁止された送信者として識別されていることにあります。エラーがあって NDR を受信したと分かっている場合には、まず、NDR メッセージに記載されている指示に従って問題を解決してください。

受信したエラーの詳細については、「 [Exchange Online のメール配信不能レポート](https://docs.microsoft.com/exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/non-delivery-reports-in-exchange-online)」にあるエラーコードの一覧を参照してください。

 たとえば、次の NDR を受信した場合、送信 IP アドレスが Microsoft によってブロックされたことを示しています。

 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`

この一覧から削除を要求するには、[リストから除外ポータルを使用して、受信拒否リストから自分自身を削除](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)します。

### <a name="my-email-landed-in-the-recipients-junk-folder-in-eop"></a>送信した電子メールが、受信側の EOP の迷惑メール フォルダーに分類される

メッセージが誤ってスパムとして特定された場合、受信側と連絡を取り、その偽陽性メッセージを Microsoft スパム分析チームに送信することができます。Microsoft スパム分析チームでは、メッセージを評価して分析します。分析結果によっては、このメッセージが許可されるようにサービス全体のスパム コンテンツ フィルター ルールが調整されることがあります。スパムとして分類されるべきでないメッセージを Microsoft にメールで送信します。その場合は、次の手順に従ってください。

### <a name="to-use-email-to-submit-false-positive-messages-to-the-microsoft-spam-analysis-team"></a>偽陽性メッセージを Microsoft スパム分析チームに電子メールで送信するには

1. スパムではないとして送信するメッセージを保存します。

2. 空の新規メッセージを作成して、スパムではないメッセージを添付ファイルとして追加します。

    必要に応じて複数のスパムではないメッセージを添付ファイルとして追加できます。

3. 元のメッセージの件名行をコピーし、新しいメッセージの件名行に貼り付けます。

    > [!IMPORTANT]
    > 新しいメッセージの本文は空のままにします。

4. 新しいメッセージを [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com) に送信します。

### <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a>自分の IP アドレスからのトラフィックが EOP によって調整される

IP アドレスが EOP によって調整されたことを示す NDR を EOP から受信することがあります。例:

 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`

不審な動作が対象の IP アドレスで検出され、さらに詳しく評価される間、一時的に制限されているために NDR を受信しました。評価によって疑いが晴れると、この制限はすぐ解除されます。

### <a name="i-cant-receive-email-from-senders-in-office-365"></a>Office 365 で送信者からの電子メールを受信できない

 Microsoft ユーザーからのメッセージを受信するには、ご使用のネットワークが Microsoft データセンター内で EOP が使用している IP アドレスからの接続を許可していることを確認してください。 詳細については、「 [Exchange Online Protection の IP アドレス](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges)」を参照してください。

## <a name="best-practices-for-bulk-emailing-to-microsoft-365-users"></a>Microsoft 365 ユーザーに一括メール送信するためのベストプラクティス

多くの場合、電子メールキャンペーンを Microsoft 365 ユーザーに対して実行し、電子メールが安全かつタイムリーに到着するようにするには、このセクションのヒントに従います。

### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a>メッセージを送信している [送信元] の名前が反映されていることを確認する

[件名] はメッセージの内容に関する要約で、メッセージ本文には、オファリング、サービス、製品について明瞭かつ簡潔に記されている必要があります。 例：

正しい:

> From: marketing@shoppershandbag.com <br/> 件名: クリスマスシーズンのカタログを更新しました。

正しくない:

> From: someone@outlook.com <br/> 件名: カタログ

送信元について、また実行内容について分かりやすくすれば、ほとんどのスパム フィルターに引っかかることなく配信しやすくなります。

### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a>キャンペーン電子メールには必ず登録解除オプションを含める

マーケティング電子メール、特にニュースレターなどでは、その後の電子メールを登録解除する方法を必ず含める必要があります。例：

 `This email was sent to example@contoso.com by sender@fabrikam.com.`

 `Update Profile/Email Address | Instant removal with SafeUnsubscribe&trade; | Privacy Policy`

一部の送信者は、「登録解除」という件名で特定のエイリアスに電子メールを送信することを受信者に求めています。これよりも、上記の例の 1 回のクリックで完了する操作を推奨します。受信者に電子メールを送信することを要求する場合、ユーザーがリンクをクリックする際に、すべての必須フィールドにあらかじめデータが入っているようにしてください。

### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a>マーケティング電子メールまたはニュースレターの登録にダブル オプトイン オプションを使用する

業界におけるこのベスト プラクティスは、会社の製品またはサービスを利用するためにユーザーによる連絡先情報の登録が必須である、または推奨される場合に適しています。一部の会社では、登録プロセスの際にマーケティング電子メールまたはニュースレターにユーザーを自動的にサインアップするようになっていますが、これは電子メールのフィルタリングにおいては問題のあるマーケティング手法であると見なされています。

登録プロセスで、「はい、ニュースレターを送信してください」、「はい、特別なオファーを送信してください」などのチェックボックスが既定で選択されていると、不注意なユーザーが、受信の必要のないマーケティング電子メールやニュースレターに意図せずにサインアップする可能性があります。

 代わりに、ダブル オプトイン オプションの使用をお勧めします。このオプションでは、マーケティング電子メールまたはニュースレターのチェックボックスは既定で選択されていない状態になっています。さらに、登録フォームが送信されると、確認の電子メールがユーザーに送信されます。そのメールには、マーケティング電子メールを受信する意思を確認するための URL が記載されています。

 これにより、マーケティング電子メールを本当に受信する意志があるユーザーだけが電子メールにサインアップするようになり、以降は、問題のあるマーケティング電子メール手法を送信元の会社から排除できます。

### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a>電子メール メッセージの内容が透過的かつトレース可能であることを確認する

電子メールの送信方法と同様、その内容も重要になります。電子メール コンテンツを作成するときは、次のベスト プラクティスを使用して、電子メールがフィルタリング サービスによってフラグ設定されないようにする必要があります。

- 送信者をアドレス帳に追加するよう、電子メール・メッセージが受信者に要求する場合、そうした操作がメールの配信を保証するものではないことを明記する必要があります。

- メッセージ本文に含まれるリダイレクトは、類似性と一貫性があるべきで、多種多様であってはなりません。このコンテキストのリダイレクトとは、リンクやドキュメントなど、メッセージから離れた任意の対象のことです。広告や登録解除リンク、またはプロファイルの更新リンクがたくさんある場合には、すべてが同じドメインを指していなければなりません。例：

  正しい:

  `unsubscribe.bulkmailer.com`

  `profile.bulkmailer.com`

  `options.bulkmailer.com`

  正しくない:

  `unsubscribe.bulkmailer.com`

  `profile.excite.com`

  `options.yahoo.com`

- サイズの大きな画像や添付ファイル、画像だけのメッセージは避けてください。

- パブリック プライバシーまたは P3P 設定では、トラッキング ピクセルが存在することを明記する必要があります (Web バグまたはビーコン)。

### <a name="remove-incorrect-email-aliases-from-your-databases"></a>データベースから不正な電子メール エイリアスを削除する

バウンス バックを作成するデータベース内のすべての電子メール エイリアスは不要であり、電子メールのフィルタリング サービスによってさらにセキュリティを確保するうえで送信メールを危険にさらすものです。電子メール データベースを最新の情報に保ってください。
