---
title: 別のユーザーにメールボックス アクセス許可を付与する - 管理者ヘルプ
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 1dbcf12f-a9de-4d1d-b0b3-a227f8a736d8
description: 'ユーザーに別のユーザーのメールボックスにアクセスする権利を与える方法について説明します。 これにより、ユーザーは他のユーザーのメールボックスからメールを読み取り、メールを送信する権利を与えられます。 '
ms.openlocfilehash: 5a0677844e8503253561c57f926c9c4fadadd76d
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43617172"
---
# <a name="give-mailbox-permissions-to-another-user---admin-help"></a>別のユーザーにメールボックス アクセス許可を付与する - 管理者ヘルプ

::: moniker range="o365-worldwide"

> [!NOTE]
> 新しい Microsoft 365 管理センターを利用していない場合、[ホーム] ページの上部にある [**新しい管理センターをお試しください**] の切り替えを選択して有効にすることができます。

::: moniker-end

管理者として、一部のユーザーに別のユーザーのメールボックスへのアクセスを許可する会社要件を設定することができます。 たとえば、アシスタントが上司のメールボックスの内容を読み取ったり、そこからメールを送信したりできるようにすること、または特定のユーザーが別のユーザーの代理でメールを送信できるようにすることが必要な場合があります。 このトピックでは、これを実現する方法を説明します。
  
共有メールボックスの作成および管理の方法については、「[共有メールボックスを作成する](../email/create-a-shared-mailbox.md)」を参照してください。
    
## <a name="looking-to-set-up-mailbox-permissions"></a>メールボックスのアクセス許可をどのように設定しますか?

メールボックスのアクセス許可を使用すると、他のユーザーにメールボックスへの読み取り/書き込みのアクセス許可を付与できます。以下の記事では、この機能の設定および使用に必要なヘルプを提供します。
  
 **アクセス許可の設定**
  
アクセス許可を設定する最初のステップは、他のユーザーが特定のメールボックスで実行できるアクションを決定することです。ユーザーはそのメールボックスからメールを読み取ること、他のユーザーの代理としてメールを送信すること、そのメールボックスが送信元のように偽装してメールを送信することができます。それぞれのアクセス許可を設定する方法については、以下の記事を参照してください。
  
- [別のユーザーのメールボックスからメールを読み取る](give-mailbox-permissions-to-another-user.md#read-email-in-another-users-mailbox)
    
- [別のユーザーのメールボックスからメールを送信する](give-mailbox-permissions-to-another-user.md#send-email-from-another-users-mailbox)

- [別のユーザーの代理でメールを送信する](give-mailbox-permissions-to-another-user.md#send-email-on-behalf-of-another-user)
    
 **変更の伝達:**
  
アクセス許可を設定すると、変更がシステム全体に伝達されるまでに最大で 60 分かかる可能性があります。
  
 **アクセス許可の設定後に使用する方法:**
  
アクセス許可が付与された後に、メールボックスにアクセスするには、いくつかの異なる方法があります。このヘルプについては、次の記事を参照してください。[別のユーザーのメールボックスにアクセスする](https://support.office.com/article/Access-another-person-s-mailbox-A909AD30-E413-40B5-A487-0EA70B763081.aspx)
  
## <a name="send-email-from-another-users-mailbox"></a>別のユーザーのメールボックスからメールを送信する

::: moniker range="o365-worldwide"

1. 管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">アクティブなユーザー</a>] の順に選択します。  
    
2. (送信許可を与える予定の) ユーザーの名前を選択して、[プロパティ] ウィンドウを開きます。
    
3. [**メール**] タブで、[**メールボックスへのアクセス許可の管理**] を選択します。

4. [**差出人を指定して送信する**] の横にある [**編集**] を選択します。 

5. [**アクセス許可を追加する**] を選択してから、このユーザーが送信できるようにするユーザーの名前を選択します。 
    
6. [**保存**] を選択します。
 
::: moniker-end

::: moniker range="o365-germany"

1. 管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">アクティブなユーザー</a>] の順に選択します。  

2. 目的のユーザーを選択し、[**メール設定**] を展開して、[**メールボックスのアクセス許可**] の横にある [**編集**] を選択します。

3. [**差出人を指定して送信する**] の横にある [**編集**] を選択します。 

4. [**アクセス許可を追加する**] を選択してから、このユーザーが送信できるようにするユーザーの名前を選択します。 
    
5. [**保存**] を選択します。

::: moniker-end

::: moniker range="o365-21vianet"

1. 管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">アクティブなユーザー</a>] の順に選択します。 

2. 目的のユーザーを選択し、[**メール設定**] を展開して、[**メールボックスのアクセス許可**] の横にある [**編集**] を選択します。

3. [**差出人を指定して送信する**] の横にある [**編集**] を選択します。 

4. [**アクセス許可を追加する**] を選択してから、このユーザーが送信できるようにするユーザーの名前を選択します。 
    
5. [**保存**] を選択します。

::: moniker-end
  
## <a name="read-email-in-another-users-mailbox"></a>別のユーザーのメールボックスのメールを読み取る

::: moniker range="o365-worldwide"

1. 管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">アクティブなユーザー</a>] の順に選択します。  
    
2. (読み取りを許可するメールボックスを持つ) ユーザーの名前を選択して、[プロパティ] ウィンドウを開きます。
    
3. [**メール**] タブで、[**メールボックスへのアクセス許可の管理**] を選択します。
    
4. [**読み取りと管理**] の横にある [**編集**] を選択します。 
    
5. [**アクセス許可を追加する**] を選択し、このメールボックスからのメールの読み取りを許可するユーザーの名前を選択します。

6. [**保存**] を選択します。

::: moniker-end

::: moniker range="o365-germany"

1. 管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">アクティブなユーザー</a>] の順に選択します。  
  
2. 目的のユーザーを選択し、[**メール設定**] を展開して、[**メールボックスのアクセス許可**] の横にある [**編集**] を選択します。
    
3. [**読み取りと管理**] の横にある [**編集**] を選択します。 
    
4. [**アクセス許可を追加する**] を選択し、このメールボックスからのメールの読み取りを許可するユーザーの名前を選択します。

5. [**保存**] を選択します。

::: moniker-end

::: moniker range="o365-21vianet"

1. 管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">アクティブなユーザー</a>] の順に選択します。 
  
2. 目的のユーザーを選択し、[**メール設定**] を展開して、[**メールボックスのアクセス許可**] の横にある [**編集**] を選択します。
    
3. [**読み取りと管理**] の横にある [**編集**] を選択します。 
    
4. [**アクセス許可を追加する**] を選択し、このメールボックスからのメールの読み取りを許可するユーザーの名前を選択します。

5. [**保存**] を選択します。

::: moniker-end


## <a name="send-email-on-behalf-of-another-user"></a>別のユーザーの代理でメールを送信する

::: moniker range="o365-worldwide"

1. 管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">アクティブなユーザー</a>] の順に選択します。  

2. (**代理送信**許可を与える予定の) ユーザーの名前を選択して、[プロパティ] ウィンドウを開きます。
    
3. [**メール**] タブで、[**メールボックスへのアクセス許可の管理**] を選択します。
    
4. [**代理送信**] の横にある [**編集**] を選択します。

5. [**アクセス許可を追加する**] を選択し、このメールボックスからのメールの代理送信を許可するユーザーの名前を選択します。

6. [**保存**] を選択します。

::: moniker-end

::: moniker range="o365-germany"

1. 管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">アクティブなユーザー</a>] の順に選択します。  

2. 目的のユーザーを選択し、[**メール設定**] を展開して、[**メールボックスのアクセス許可**] の横にある [**編集**] を選択します。

3. [**代理送信**] の横にある [**編集**] を選択します。
    
4. [**アクセス許可を追加する**] を選択し、このメールボックスからのメールの代理送信を許可するユーザーの名前を選択します。

5. [**保存**] を選択します。

::: moniker-end

::: moniker range="o365-21vianet"

1. 管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">アクティブなユーザー</a>] の順に選択します。 

2. 目的のユーザーを選択し、[**メール設定**] を展開して、[**メールボックスのアクセス許可**] の横にある [**編集**] を選択します。

3. [**代理送信**] の横にある [**編集**] を選択します。
    
4. [**アクセス許可を追加する**] を選択し、このメールボックスからのメールの代理送信を許可するユーザーの名前を選択します。

5. [**保存**] を選択します。

::: moniker-end


## <a name="send-and-read-from-outlook-and-outlook-on-the-web-for-business"></a>Outlook および一般法人向け Outlook on the web での送信および読み取り


別のユーザーのメールボックスからメールを送信する方法については、次のトピックを参照してください。
  
- [他のユーザーのメールおよび予定表のアイテムを管理する](https://support.office.com/article/afb79d6b-2967-43b9-a944-a6b953190af5.aspx)
    
- [別のユーザーまたはグループからメールを送信する](https://support.office.com/article/0f4964af-aec6-484b-a65c-0434df8cdb6b.aspx)
