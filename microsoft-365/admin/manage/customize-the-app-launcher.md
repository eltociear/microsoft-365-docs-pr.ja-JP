---
title: カスタム タイルをアプリ起動ツールに追加する
f1.keywords:
- CSH
ms.author: twerner
author: twernermsft
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 1136115a-75af-4497-b693-640c4ce70bc6
description: 'カスタムタイルをアプリ起動ツールに追加することによって、電子メール、ドキュメント、アプリ、SharePoint サイト、外部サイト、その他のリソースへのクイックリンクを作成します。 '
ms.openlocfilehash: 705d45a2c26d3bd5e2d45d6d8f5a7c998c449f8d
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43628198"
---
# <a name="add-custom-tiles-to-the-app-launcher"></a>カスタム タイルをアプリ起動ツールに追加する

Microsoft 365 では、アプリ起動ツールを使用して、電子メール、予定表、ドキュメント、アプリをすばやく簡単に入手できます ([詳細につい](https://support.office.com/article/79f12104-6fed-442f-96a0-eb089a3f476a.aspx)ては、こちらを参照してください)。 これらは、Microsoft 365 で入手できるアプリ、および[SharePoint ストア](https://support.office.com/article/dd98e50e-d3db-4ecb-9bb7-82b189822d43.aspx)または[Azure AD](https://msdn.microsoft.com/office/office365/howto/connect-your-app-to-o365-app-launcher)から追加するカスタムアプリです。
  
SharePoint サイト、外部サイト、レガシー アプリなどをポイントするカスタム タイルをアプリ起動ツールに追加できます。カスタム タイルは、アプリ起動ツールの [ **すべて**] のアプリの下に表示されますが、[ **ホーム**] アプリにピン留めしたり、同じ操作を行うようにユーザーに指示したりできます。この操作により、関連サイト、アプリ、仕事に必要なリソースへのアクセスが容易になります。以下の例では、"Contoso Portal" と呼ばれるカスタム タイルを使って、組織の SharePoint イントラネット サイトにアクセスします。 
  
![アプリ起動ツール](../../media/7acc06cc-ac7a-4c6e-8ea7-81570a5bdbab.png)
  
## <a name="add-a-custom-tile-to-the-app-launcher"></a>カスタム タイルをアプリ起動ツールに追加する

1. 管理センターで、[**設定** > ] の**設定**に移動し、[**組織プロファイル**] タブを選択します。
    
2. [**組織プロファイル**] タブで、[**カスタムアプリ起動ツールタイル**] を選択します。
  
3. [**カスタムタイルの追加**] を選択します。 
  
4. 新しいタイルの **タイル名**を入力します。 名前がタイルに表示されます。 
    
5. タイルの**web サイトの URL**を入力します。 これは、アプリ起動ツールでタイルを選択したときにユーザーが移動する場所です。 URL に HTTPS を使用します。<br/>ヒント: SharePoint サイトのタイルを作成している場合は、そのサイトに移動し、URL をコピーして、ここに貼り付けます。 既定のチームサイトの URL は次のようになります。`https://<company_name>.sharepoint.com` 
  
6. タイルの**イメージの URL**を入力します。 この画像は [個人用アプリ] ページとアプリ起動ツールに表示されます。<br/>ヒント: 画像は60x60 ピクセルで、組織内のすべてのユーザーが認証を必要とせずに使用できるようにする必要があります。

7. タイルの **説明**を入力します。 [個人用アプリ] ページでタイルを選択し、[**アプリの詳細**] を選択すると、これが表示されます。 
  
8. [ **Save changes** ] を選択してカスタムタイルを作成します。 
    
これでカスタム タイルは、管理者とユーザー用にアプリ起動ツールの [ **すべて**] のタブに表示されるようになります。 
  
## <a name="promote-the-tile-to-app-launcher"></a>タイルをアプリ起動ツールに昇格させる

1. アプリ起動ツールのアイコンを選択し、[**すべてのアプリ**] を選択します。 
    
2. アプリの新しいタイルを見つけ、省略記号を選択して、[**スタート] に [ピン留め] を**選択します。
  
    > [!NOTE]
    > 前の手順で作成したカスタム タイルが表示されない場合は、Exchange Online メールボックスが自分に割り当てられていること、およびメールボックスに最低一度はサインインしていることを確認します。 これらの手順は、Microsoft 365 のカスタムタイルに必要です。 
  
> [!IMPORTANT]
> 自身とユーザーの両方がこれらの手順に従って、[個人用アプリ] ページからアプリ起動ツールへとタイルを昇格する必要があります。 
  
## <a name="edit-or-delete-a-custom-tile"></a>Edit or delete a custom tile

1. 管理センターで、[**設定** > の**設定** > ] [<a href="https://go.microsoft.com/fwlink/p/?linkid=2067339" target="_blank">組織プロファイル</a>] タブに移動します。
    
2. [**組織プロファイル**] ページで、[**組織のカスタムタイルの追加**] の横にある [**編集**] を選択します。

3. カスタム タイルの **タイル名**、 **URL**、 **説明**、 **画像 URL** を更新します。( [カスタム タイルをアプリ起動ツールに追加する](#add-a-custom-tile-to-the-app-launcher)参照)。
    
4. [**更新プログラム** \>の**クローズ**] を選択します。 
    
カスタムタイルを削除するには、**カスタム**タイルウィンドウでタイルを選択し、[**タイル** > の**削除**を削除] を選択します。 
  
## <a name="whats-next"></a>次の作業

アプリ起動ツールにタイルを追加するだけでなく、アプリ起動ツールタイルをナビゲーションバーに追加することもできます ([詳細につい](https://support.office.com/article/d536512c-b0f7-49fd-b8db-a8a967e23f23.aspx)ては、こちらを参照してください)。 組織のブランドに合わせて Microsoft 365 のルックアンドフィールをカスタマイズするには、「 [microsoft 365 テーマをカスタマイズ](../setup/customize-your-organization-theme.md)する」を参照してください。
  

