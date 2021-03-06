---
title: ネットワークソリューションを使用して Microsoft をセットアップするためにネームサーバーを変更する
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: d4ba60f3-4e1c-4180-99bd-250b8955be2a
description: 'DNS レコードを管理する場合は、microsoft カスタムドメインとネットワークソリューションをセットアップする方法について説明します。 '
ms.openlocfilehash: 2b3b575943ebd95ffcbd34dd4578133fa7dd4f79
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629757"
---
# <a name="change-nameservers-to-set-up-microsoft-with-network-solutions"></a>ネットワークソリューションを使用して Microsoft をセットアップするためにネームサーバーを変更する

 探している内容が見つからない場合は、**[ドメインに関する FAQ を確認Q](../setup/domains-faq.md)** を参照してください。
  
Microsoft が DNS レコードを管理する場合は、次の手順に従ってください。 (必要に応じ[て、すべての MICROSOFT DNS レコードをネットワークソリューションで管理](create-dns-records-at-network-solutions.md)できます。)
  
    
## <a name="add-a-txt-record-at-network-solutions-to-verify-that-you-own-the-domain"></a>Network Solutions で TXT レコードを追加して、ドメインを所有していることを確認する

ドメインを Microsoft で使用する前に、必ずそのドメインを所有していることを確認する必要があります。 ドメインレジストラーで自分のアカウントにログインし、DNS レコードを作成することにより、そのドメインを所有していることが Microsoft に証明されます。
  
> [!NOTE]
> このレコードは、ドメインを所有していることを確認するためだけに使用されます。その他には影響しません。 必要に応じて、後で削除することができます。 
  
次の手順を実行するか、[ビデオ (47 秒から開始) を参照](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-Network-Solutions-69b092e3-c026-4d19-a7d0-16cdb2d8b261?ui=en-US&amp;rs=en-US&amp;ad=US)してください。
  
1. まず、[このリンク](https://www.networksolutions.com/manage-it)を使って Network Solutions でドメイン ページにアクセスします。ログインするように求められます。
    
    > [!IMPORTANT]
    > [**ログイン**] ボタンを選択する前に、[ **Log in to** ] ドロップダウンリストで [ **Manage My Domain Names** ] を選びます。
  
    ![[Manage My Domain Names] を選択して、Network Solutions にログインします](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. 変更するドメインの名前の横にあるチェック ボックスをオンにします。
    
    ![自分のドメインのチェック ボックスを選択します](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. [ **EDIT DNS**] を選びます。
    
    ![[DNS の編集] を選択します。](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. [ **Manage ADVANCED DNS Records**] を選びます。
    
    (You may have to scroll down.)
    
    ![[Manage Advanced DNS Records] を選択します。](../../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. [**テキスト (Txt レコード)** ] セクションまでスクロールしてから、[ **Txt レコードの編集**] を選択します。
    
    ![[TXT レコードの編集] を選択する](../../media/240a01d6-750a-4da6-8554-641b571e4b71.png)
  
6. 新規レコードのボックスに、次の表の値を入力するか、コピーして貼り付けます。
    
|**Host**|**TTL**|**Text**|
|:-----|:-----|:-----|
|@  <br/> (The system will change this value to **@ (None)** when you save the record.)  <br/> |3600  <br/> |MS=ms *XXXXXXXX*  <br/> **注**: これは例です。 Microsoft 365 の表に記載されている、特定の**宛先またはポイントを**使用して、ここでのアドレスを指定します。           [確認する方法](../get-help-with-domains/information-for-dns-records.md)
   
    
   ![新しいレコードのボックスに値を入力するか貼り付けます。](../../media/8a76daab-b6ff-4c82-ba68-192b24fbb934.png)
  
7. [**続行**] を選択します。
    
    ![[続行] を選択する](../../media/89e7fb38-b4d9-4949-a1bb-d0dd10b361e0.png)
  
8. [ **Save Changes**] を選びます。
    
    ![[変更の保存] を選択する](../../media/bd4d7cd0-c8a3-497a-b080-cfd5a5c60dc5.png)
  
9. 数分待つと、続行できます。この間、作成したレコードがインターネット全体で更新されます。
    
これで、ドメインレジストラーのサイトでレコードが追加されたので、Microsoft 365 に戻り、Microsoft 365 にレコードを検索するよう要求します。
  
Microsoft が正しい TXT レコードを見つけると、ドメインが確認されます。
  
1. Microsoft 管理センターで、[<a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">ドメイン</a>の**設定** \> ] ページに移動します。

    
2. **[ドメイン]** ページで、確認するドメインを選択します。 
    
    
  
3. **[セットアップ]** ページで、**[セットアップの開始]** を選択します。
    
    
  
4. **[ドメインの確認]** ページで、**[確認]** を選択します。
    
    
  
> [!NOTE]
>  通常、DNS の変更が有効になるのに 15 分ほどかかります。ただし、インターネットの DNS システム全体を更新する変更の場合、さらに長くかかることもあります。DNS レコードの追加でメール フローなどに問題が発生した場合は、「[ドメイン名または DNS レコードの変更後の問題に関するトラブルシューティング](../get-help-with-domains/find-and-fix-issues.md)」を参照してください。 
  
## <a name="change-your-domains-nameserver-ns-records"></a>ドメインのネーム サーバー (NS) レコードを変更する

Microsoft によるドメインの設定を完了するには、ドメインレジストラーでドメインの NS レコードを変更して、Microsoft プライマリネームサーバーとセカンダリネームサーバーをポイントするようにします。 これにより、ドメインの DNS レコードが更新されるように Microsoft が設定されます。 メール、Skype for Business Online、一般向け Web サイトをドメインで利用できるようにすべてのレコードを追加し、すべての設定を完了します。
  
> [!CAUTION]
> ドメインの NS レコードを変更して Microsoft ネームサーバーをポイントすると、現在ドメインに関連付けられているすべてのサービスが影響を受けます。 たとえば、ドメインに送信されるすべての電子メール (rob@ *your_domain*など) は、この変更を行った後に Microsoft に送られ始めます。
  
Microsoft がドメインをセットアップできるように、NS レコードを変更する準備はできましたか? 次の手順を実行するか、[ビデオ (2 分 23 秒から開始) を参照](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-Network-Solutions-69b092e3-c026-4d19-a7d0-16cdb2d8b261?ui=en-US&amp;rs=en-US&amp;ad=US)してください。
  
> [!IMPORTANT]
>  このセクションの手順を完了すると、次の4つのネームサーバー*のみ*が一覧表示されます。 **ns1.bdm.microsoftonline.com**、 **ns2.bdm.microsoftonline.com**、 **ns3.bdm.microsoftonline.com**、および**ns4.bdm.microsoftonline.com**。 次の手順では、他の不要なネームサーバーを一覧から削除する方法、および上記のネームサーバーが一覧に表示されていない場合に、 *正しい*  ネームサーバーを追加する方法を説明します。 
  
1. まず、[このリンク](https://www.networksolutions.com/manage-it)を使って Network Solutions でドメイン ページにアクセスします。 ログインするように求められます。
    
    > [!IMPORTANT]
    > [**ログイン**] ボタンを選択する前に、[ **Log in to** ] ドロップダウンリストで [ **Manage My Domain Names** ] を選びます。 
  
    ![[Manage My Domain Names] を選択して、Network Solutions にログインします](../../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. 変更するドメインの名前の横にあるチェック ボックスをオンにします。
    
    ![自分のドメインのチェック ボックスを選択します](../../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. [ **EDIT DNS**] を選びます。
    
    ![[DNS の編集] を選択します。](../../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. [ **MOVE DNS**] を選びます。
    
    ![NetworkSolutionsBP-1-1](../../media/e57a30f3-63d5-4bcb-84c6-c8be21c261a2.png)
  
5. 現在表示されているページに既に一覧表示されているネームサーバーがあるかどうかに応じて、以下の 2 つの手順のいずれかに進みます。
    
  - 既に一覧表示されているネーム サーバーが **ない** 場合は、 [既に一覧表示されているネームサーバーがない場合](#if-there-are-no-nameservers-already-listed)。
    
  - 既に一覧表示されているネーム サーバーが **ある** 場合は、 [既に一覧表示されているネームサーバーがある場合](#if-there-are-nameservers-already-listed)。
    
### <a name="if-there-are-no-nameservers-already-listed"></a>既に一覧表示されているネームサーバーがない場合

1. [**ドメイン**] ページの [ **Domain Name servers の指定**] セクションで、[さらに**ネームサーバーを追加**] を選択します。
    
    ![NetworkSolutionsBP-1-2-1](../../media/57e22ef1-ac88-4d4a-bc8e-058023255dfd.png)
  
2. [ **Domain Names**] ページに、次の表のネームサーバーの値を入力するか、コピーして貼り付けます。 
    
|||
|:-----|:-----|
|**Name Server 1** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**Name Server 2** <br/> |ns2.bdm.microsoftonline.com  <br/> |
|**Name Server 2** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**Name Server 2** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
    
![NetworkSolutionsBP-1-2-2](../../media/795e8c6b-4828-4de2-b624-82f067bb2eb1.png)
  
3. [ **MOVE DNS**] を選びます。
    
    ![NetworkSolutionsBP-1-2-3](../../media/d4a0a7c2-6868-471f-bbf4-16ce2e2348de.png)
  
4. [ **Save Changes**] を選びます。
    
    ![NetworkSolutionsBP-1-2-4](../../media/897bc864-b340-4385-abeb-f94bc7f73e5e.png)
  
> [!NOTE]
> ネーム サーバー レコードの更新がインターネットの DNS システム全体に反映されるまでに、最大で数時間かかる場合があります。 その後、自分のドメインで使用できるように、Microsoft メールとその他のサービスがすべて設定されます。 
  
### <a name="if-there-are-nameservers-already-listed"></a>既に一覧表示されているネームサーバーがある場合

> [!CAUTION]
> これらの手順は、前途した 4 件の *正しい*  ネームサーバー以外にも既存のネームサーバーがある場合に  *のみ*  行ってください (つまり、現在のネームサーバーのうち *ns1.bdm.microsoftonline.com* 、 *ns2.bdm.microsoftonline.com* 、 **ns3.bdm.microsoftonline.com** 、 **ns4.bdm.microsoftonline.com** のいずれでも  **ない**  もの  **だけ**  を削除します)。
  
1. 他のネームサーバーが表示されている場合は、各ネームサーバーを選び、キーボードの **Delete** キーを押して、ネームサーバーを削除します。
    
    ![NetworkSolutions-BP-Redelegate-1-5](../../media/eeb8ad22-bf4a-43a8-b97a-f09c3654d89b.png)
  
2. [**その他のネームサーバーを追加**] を選択します。
    
    ![NetworkSolutionsBP-1-2-1](../../media/57e22ef1-ac88-4d4a-bc8e-058023255dfd.png)
  
3. [ **Domain Names**] ページに、次の表のネームサーバーの値を入力するか、コピーして貼り付けます。
 
    
|||
|:-----|:-----|
|**Name Server 1** <br/> |ns1.bdm.microsoftonline.com  <br/> |
|**Name Server 2** <br/> |ns2.bdm.microsoftonline.com  <br/> |
|**Name Server 3** <br/> |ns3.bdm.microsoftonline.com  <br/> |
|**Name Server 4** <br/> |ns4.bdm.microsoftonline.com  <br/> |
   
    
![NetworkSolutionsBP-1-2-2](../../media/795e8c6b-4828-4de2-b624-82f067bb2eb1.png)
  
4. [ **MOVE DNS**] を選びます。
    
    ![NetworkSolutionsBP-1-2-3](../../media/d4a0a7c2-6868-471f-bbf4-16ce2e2348de.png)
  
5. [ **Save Changes** ] を選びます。
    
    ![NetworkSolutionsBP-1-2-4](../../media/897bc864-b340-4385-abeb-f94bc7f73e5e.png)
  
> [!NOTE]
> ネーム サーバー レコードの更新がインターネットの DNS システム全体に反映されるまでに、最大で数時間かかる場合があります。 その後、自分のドメインで使用できるように、Microsoft メールとその他のサービスがすべて設定されます。
