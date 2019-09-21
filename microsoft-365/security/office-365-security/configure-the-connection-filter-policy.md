---
title: 接続フィルターポリシー、許可一覧、禁止一覧を構成する
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 8/27/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
ms.collection:
- M365-security-compliance
description: 信頼できるユーザーからの電子メールがブロックされないようにするには、接続フィルターポリシーを使用して、信頼する IP アドレスの許可リスト (安全な差出人のリストとも呼ばれます) を作成します。 受信拒否リストを作成することもできます。
ms.openlocfilehash: 09da8b2b7ee6c584d479ffc1206e7b3cf72d1eb8
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2019
ms.locfileid: "37086048"
---
# <a name="configure-the-connection-filter-policy"></a>接続フィルター ポリシーを設定する

ほとんどの人は友人やビジネス パートナーを信頼しています。信頼する人からの電子メールが迷惑メール フォルダーに入っていたり、スパム フィルターによって完全にブロックされたりすると、もどかしさを感じます。そのようなメールがブロックされないようにするには、接続フィルター ポリシーを利用して許可リスト (「差出人セーフ リスト」ともいう) を作成し、信頼する IP アドレスを登録することができます。また、受信拒否リストを作成して既知のスパム メール送信者の IP アドレスを登録し、そのような送信者からの電子メール メッセージを受信しないようにすることもできます。
  
- *[許可リスト](create-safe-sender-lists-in-office-365.md)* について検討する場合、接続フィルターポリシーは、フィルターによって許可されている*信頼さ*れたアカウントに特に注意してください。 これは、必要な情報を保持しながら、信頼できるまたは信頼されていないメールをより正確にフィルター処理することが重要になります。 接続フィルターポリシーの許可リストは、アカウントおよび Ip の大規模なプールから少数の信頼された Ip にフィルターを適用し、信頼できるメールボックスへのアクセスを容易にすることを目的としています。

- 接続フィルターポリシーブロックリストを作成する場合は、代わりに、フィルターでの信頼できないアカウントをキャッチすることを考えることができます。

 組織全体に適用されるスパム設定の詳細については、「 [EOP と Office 365 でメールが迷惑メールとして検出されないようにする](https://go.microsoft.com/fwlink/p/?LinkId=534224)」または「[Office 365 のスパム フィルターでスパムや迷惑メールをブロックして、検出漏れ問題を防止する](https://go.microsoft.com/fwlink/p/?LinkId=534225)」を参照してください。これらは、管理者レベルの制御権限を持っている場合にスパムの誤検知や検出漏れを防ぐ上で役立ちます。

> [!TIP]
> [許可 (または安全な送信者) のリスト](create-safe-sender-lists-in-office-365.md)と[ブロックリスト](create-block-sender-lists-in-office-365.md)を作成する方法については、一時停止および読み取りを行う必要があります。
  
次のビデオでは、接続フィルター ポリシーの構成手順を示します。
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>事前に必要な知識

- 予想所要時間: 15 分

- この手順を実行する際には、あらかじめアクセス許可を割り当てる必要があります。 必要なアクセス許可を確認するには、「 [Exchange Online の機能のアクセス許可](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx)」トピックの「スパム対策」のエントリを参照してください。

- 許可またはブロックする送信者の IP アドレスを取得するには、メッセージのインターネット ヘッダーを確認するという方法があります。 「[スパム対策メッセージ ヘッダー](anti-spam-message-headers.md)」で説明されているように、CIP ヘッダーを調べます。 さまざまな電子メールクライアントでメッセージヘッダーを表示する方法については、「[メッセージヘッダーアナライザー](https://go.microsoft.com/fwlink/p/?LinkId=306583)」を参照してください。

- IP ブロック一覧の IP アドレスから送信された電子メール メッセージは拒否され、スパムとしてマークされず、追加のフィルター処理は行われません。

- 以下の接続フィルター手順はリモート PowerShell 経由でも実行することができます。Get-HostedConnectionFilterPolicy コマンドレットを使用して設定を確認し、 Set-HostedConnectionFilterPolicy を使用して接続フィルター ポリシー設定を編集します。 [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) コマンドレットを使用して設定を確認し、[Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) を使用して接続フィルター ポリシー設定を編集します。 Windows PowerShell を使って Exchange Online Protection に接続する方法については、「[Exchange Online Protection の PowerShell への接続](https://go.microsoft.com/fwlink/p/?linkid=627290)」を参照してください。 Windows PowerShell を使って Exchange Online に接続する方法については、「[Exchange Online PowerShell への接続](https://go.microsoft.com/fwlink/p/?linkid=396554)」を参照してください。

## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>EAC を使用して既定の接続フィルター ポリシーを編集する

IP 許可リストまたは IP 禁止リストを作成するには、Exchange 管理センター (EAC) で接続フィルター ポリシーを編集します。接続フィルター ポリシーの設定は、受信メッセージのみに適用されます。
  
1. Exchange 管理センター (EAC) で、 **[保護]** \> **[接続フィルター]** に移動し、既定のポリシーをダブルクリックします。

2. **[接続フィルター]** メニュー項目をクリックし、IP 許可一覧、IP 禁止一覧、あるいはその両方のうち、必要な一覧を作成します。

   この一覧を作成するには、![[追加] アイコン](../media/ITPro-EAC-AddIcon.gif) をクリックします。後続のダイアログ ボックスでは、IP アドレスまたはアドレス範囲を指定して **[OK]** をクリックします。さらにアドレスを追加するには、このプロセスを繰り返します。(IP アドレスは、追加後に編集または削除できます。)

   形式を nnn. nnn にする場合は、IPV4 IP アドレスを指定します。 nnn には0から255の数値を指定します。 クラスレス ドメイン間ルーティング (CIDR) の範囲を nnn.nnn.nnn.nnn/rr (rr は 24 から 32 までの数値) の形式で指定することもできます。 24 ~ 32 の範囲外の範囲を指定するには、次のセクション「 [IP 許可一覧を構成するときの考慮事項](#additional-considerations-when-configuring-ip-allow-lists)」を参照してください。

   > [!NOTE]
   > 両方のリストに IP アドレスを追加すると、その IP アドレスから送信された電子メールが許可されます。 <br/><br/> 最大 1273 のエントリを指定できます。各エントリは、単一の IP アドレス、または IP アドレスの CIDR 範囲 (/24 から /32 まで) にすることができます。<br/><br/> TLS で暗号化されたメッセージを送信している場合、IPv6 アドレスとアドレスの範囲はサポートされていません。
  
3. 必要に応じて、[**セーフリストを有効**にする] チェックボックスをオンにして、特定の既知の送信者からの電子メールが失われないようにします。 どう。 Microsoft は、信頼できる送信者のサードパーティソースにサブスクライブします。 このセーフリストを使用することは、これらの信頼できる差出人が誤ってスパムとしてマークされていることを意味します。 受信する誤検知 (良好なメールに分類されているメール) の数を減らす必要があるため、このオプションを選択することをお勧めします。 

4. **[保存]** をクリックします。既定のポリシー設定の概要が右側のウィンドウに表示されます。

## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>IP 許可一覧を構成する場合のその他の留意点

IP 許可一覧を構成する場合に考慮するまたは認識すべきその他の留意点を以下に示します。
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>推奨範囲外の CIDR 範囲の指定

/1 から/23 の CIDR IP アドレス範囲を指定するには、スパムの信頼レベル (SCL) を設定するメールフロールールを作成する必要があります。これは、スパムの**フィルター処理をバイパス**する (つまり、この ip アドレス範囲内で受信するすべてのメッセージが[迷惑メールではない] に設定し、サービスによって追加のフィルター処理は実行されません)。 ただし、これらの IP アドレスのいずれかが Microsoft の独自のブロックリストまたはサードパーティのブロックリストのいずれかに表示される場合でも、これらのメッセージはブロックされます。 そのため、/24 ~ 32 IP アドレス範囲を使用することを強くお勧めします。
  
このメールフロールールを作成するには、次の手順を実行します。
  
1. EAC で、 **[メール フロー]** \> **[ルール]** に移動します。

2. ![[追加] アイコン](../media/ITPro-EAC-AddIcon.gif) をクリックしてから、 **[新しいルールを作成する]** を選択します。

3. ルールに名前を付けてから、 **[その他のオプション]** をクリックします。

4. **[このルールを適用する条件]** で、 **[差出人]** を選択してから、 **[IP アドレスがこれらの範囲内か完全に一致している]** を選択します。

5. [ **Ip アドレスの指定**] で、ip アドレスの範囲を指定し **、** ![[追加] アイコン](../media/ITPro-EAC-AddIcon.gif)をクリックして、[ **ok]** をクリックします。

6. **[実行する処理]** ボックスで、 **[メッセージのプロパティを変更する]** の次に **[SCL (Spam Confidence Level) の設定]** を選択することによって、処理を設定します。 **[SCL の指定]** ボックスで、 **[スパム対策フィルターをバイパスする]** を選択してから、 **[ok]** をクリックします。

7. これ以外にも、ルールを監査する、ルールをテストする、一定期間だけルールをアクティブにするといった選択肢もあります。 ルールを施行する前に一定期間ルールをテストすることをお勧めします。 [Exchange Server のメールフロールールの手順には](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures)、これらの選択についての詳細が含まれています。

8. [**保存**] をクリックしてルールを保存します。 ルールがルールの一覧に表示されます。

ルールを作成して適用すると、サービスは指定した IP アドレス範囲のスパムフィルター処理をバイパスします。

### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>特定のドメインに関する IP 許可一覧例外の範囲指定

一般に、安全だと思われるドメインの IP アドレス (または IP アドレス範囲) をすべて IP 許可一覧に追加することをお勧めします。 ただし、IP 許可一覧のエントリをすべてのドメインに適用しない場合は、特定のドメインを除外するメールフロールール (トランスポートルールとも呼ばれます) を作成できます。
  
たとえば、ContosoA.com、ContosoB.com、および ContosoC.com という 3 つのドメインがあり、IP アドレス (簡単にするために、1.2.3.4 を使用する) を追加して、ContosoB.com ドメインのフィルター処理だけを省略することにしましょう。 すべてのドメインの Spam Confidence Level (SCL) を -1 に設定する (非スパムに分類されることを意味する) 1.2.3.4 用の IP 許可一覧を作成します。 その後、ContosoB.com 以外のすべてのドメインの SCL を0に設定するメールフロールールを作成できます。 これにより、ルールの適用外のドメインに指定されている ContosoB.com を除く IP アドレスに対応するすべてのドメインについてメッセージが再スキャンされます。 ContosoB.com の SCL はフィルター処理をスキップする -1 のままであるのに対して、ContosoA.com と ContosoC.com の SCL はコンテンツ フィルターによって再スキャンされる 0 です。
  
これを実現するには、以下の手順を実行します。
  
1. EAC で、 **[メール フロー]** \> **[ルール]** に移動します。

2. ![[追加] アイコン](../media/ITPro-EAC-AddIcon.gif) をクリックしてから、 **[新しいルールを作成する]** を選択します。

3. ルールに名前を付けてから、 **[その他のオプション]** をクリックします。

4. **[このルールを適用する条件]** で、 **[差出人]** を選択してから、 **[IP アドレスがこれらの範囲内か完全に一致している]** を選択します。

5. [Ip**アドレスの指定**] ボックスで、ip 許可一覧![に入力した ip アドレスまたは ip アドレスの範囲を指定し](../media/ITPro-EAC-AddIcon.gif)、 **[追加]** アイコンをクリックし、[ **OK]** をクリックします。

6. [**実行する**処理] で、[**メッセージのプロパティを変更する**] を選択して、**スパムの信頼レベル (SCL) を設定**することにより、アクションを設定します。 [ **SCL の指定**] ボックスで、[ **0**] を選択し、[ **OK**] をクリックします。

7. [**例外の追加**] をクリックし、[除く] の**場合**は [**送信者**] を選択し、[ **domain is**] を選択します。

8. [**ドメインの指定**] ボックスに、スパムフィルタリングをバイパスするドメイン ( **contosob.com**など) を入力します。 ![[追加] アイコン](../media/ITPro-EAC-AddIcon.gif)をクリックして、それを語句の一覧に**移動します**。 その他のドメインを例外として追加する場合はこの手順を繰り返し、完了したら、 **[ok]** をクリックします。 

9. これ以外にも、ルールを監査する、ルールをテストする、一定期間だけルールをアクティブにするといった選択肢もあります。 ルールを施行する前に一定期間ルールをテストすることをお勧めします。 [Exchange Server のメールフロールールの手順には](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures)、これらの選択についての詳細が含まれています。

10. [**保存**] をクリックしてルールを保存します。 ルールがルールの一覧に表示されます。

ルールを作成して適用すると、指定した IP アドレスまたは IP アドレス範囲に対するスパム フィルター処理が入力したドメイン例外の場合にのみ省略されます。

### <a name="scenarios-where-allowed-ip-addresses-are-still-filtered"></a>許可された IP アドレスがまだフィルター処理されているシナリオ

接続フィルターポリシーで構成した許可された IP アドレスからのメッセージは、次のシナリオでは依然としてスパムフィルター処理の対象となります。

- 接続フィルターポリシーの送信元 IP アドレスも、*任意*のテナント内のオンプレミスの ip ベースの受信コネクタで構成されています (このテナント a を呼び出すことになります) **。また、テナント A**および Exchange Online Protection サーバーは、最初に検出したOffice 365 のメッセージは、どちらも Microsoft データセンター内の同じ Active Directory フォレストに存在します。 このシナリオでは、 **Ipv: CAL**がメッセージの[スパム対策メッセージヘッダー](anti-spam-message-headers.md)に追加されます (メッセージがスパムフィルタリングをバイパスしていることを示します)。ただし、メッセージはスパムフィルター処理の対象となります。

- テナント (接続フィルターポリシーを構成した場所) と、Office 365 で最初にメッセージを検出した Exchange Online Protection サーバーは、どちらも Microsoft データセンター内の異なる Active Directory フォレストに存在することになります。 このシナリオでは、 **Ipv: CAL**はメッセージヘッダーに追加されないため、メッセージはスパムフィルター処理の対象となります。

これらのシナリオのいずれかが発生した場合は、次の設定を使用して EAC でメールフロールールを作成し、その IP アドレスまたはアドレスからのメッセージがスパムフィルタリングをバイパスするようにすることができます。

- ルールの条件:**送信者** \> **の IP アドレスがこれらの範囲内にある場合、または完全に一致する** \>場合\>は (IP アドレスまたはアドレス)、**このルールを適用**します。

- ルールの処理: \> **メッセージのプロパティを変更する** \> **スパム信頼レベル (SCL) を設定**する**スパムフィルターをバイパス**する。

これは基本的に、[[特定のドメインに対する IP 許可一覧の例外](#scoping-an-ip-allow-list-exception-for-a-specific-domain)] セクションのルール作成手順と同じです。

## <a name="new-to-office-365"></a>Office 365 を初めて使用する場合

||
|:-----|
|![LinkedIn Learning](../media/eac8a413-9498-4220-8544-1e37d1aaea13.png)の短いアイコン**を Office 365 に追加しますか?** LinkedIn Learning が提供する **Office 365 管理者および IT プロフェッショナル**向けの無料のビデオ コースをご覧ください。|

## <a name="for-more-information"></a>関連情報

[Exchange Online の差出人セーフ リストと受信拒否リスト](safe-sender-and-blocked-sender-lists-faq.md)
  
[スパム フィルター ポリシーの構成](configure-your-spam-filter-policies.md)
  
[送信スパム ポリシーを構成する](configure-the-outbound-spam-policy.md)
  
[メッセージがスパムとしてマークされないようにする方法](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[検出漏れの問題を防止するために Office 365 スパム フィルターを使用して迷惑メールをブロックする](https://go.microsoft.com/fwlink/p/?LinkId=534225)