---
title: ドキュメントのラベル アクティビティを表示する
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: 5/9/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
- SPO_Content
localization_priority: Priority
search.appverid:
- MOE150
- MET150
description: セキュリティ &amp; コンプライアンス センターのラベル アクティビティ エクスプローラーを使用すると、過去 30 日間の SharePoint および OneDrive for Business のすべてコンテンツのラベル アクティビティをすばやく検索して表示することができます。リアルタイム データが表示され、テナント内での状況を明確に把握できます。
ms.openlocfilehash: b0a799e192f6b6c3cb8087b38322094ca7423fea
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43626333"
---
# <a name="view-label-activity-for-documents"></a>ドキュメントのラベル アクティビティを表示する

ラベルを作成した後、意図したとおりにラベルがコンテンツに適用されているかどうかを確認することをお勧めします。セキュリティ &amp; コンプライアンス センターのラベル アクティビティ エクスプローラーを使用すると、過去 30 日間の SharePoint および OneDrive for Business のすべてコンテンツのラベル アクティビティをすばやく検索して表示することができます。リアルタイム データが表示され、テナント内での状況を明確に把握できます。
  
たとえば、ラベル アクティビティ エクスプローラーで以下のことができます:
  
- それぞれのラベルが適用された回数を日ごとに表示 (最大 30 日間)。
    
- 誰がいつ、どのファイルにラベルを付けたかを正確に表示。ファイルが存在するサイトへのリンクも表示。
    
- ラベルが変更されたり削除されたりしたファイル、古いラベルおよび新しいラベル、変更を行ったユーザーの表示。
    
- データをフィルター処理して、特定のレベル、ファイル、ユーザーのラベル アクティビティすべてを表示。場所 (SharePoint または OneDrive for Business) や、ラベルが適用された方法 (手動か自動) でラベル アクティビティをフィルター処理することも可能。
    
- 各ドキュメントだけでなくフォルダーのラベル アクティビティも表示。今後は、ラベルが付けられたフォルダーの中のファイル数が表示される予定。
    
ラベル アクティビティ エクスプローラーにアクセスするには、セキュリティ &amp; コンプライアンス センターで **[情報ガバナンス]** > **[ラベル アクティビティ エクスプローラー]** の順に移動します。
  
なお、ラベル アクティビティ エクスプローラーには、Office 365 Enterprise E5 サブスクリプションが必要となります。
  
![ラベル アクティビティ エクスプローラー](../media/671ca0cd-1457-40b4-9917-b663360afd95.png)
  
## <a name="view-label-activities-for-files-or-folders"></a>ファイルまたはフォルダーのラベル アクティビティの表示

ラベル アクティビティ エクスプローラーの上部で、ファイルまたはフォルダーのアクティビティを表示するかどうかを選択できます。フォルダーのアクティビティではフォルダーのみが表示されます。フォルダー内のファイルは表示されません。
  
フォルダーにラベルを付けると、そのフォルダー内のすべてのファイルもそのラベルを取得するため (明示的に適用されているラベルがあるファイルを除く)、フォルダーのラベル アクティビティを表示したい場合があります。したがって、フォルダーにラベルを付けると、多数のファイルに影響を及ぼす可能性があります。詳細については、「[SharePoint ライブラリ、フォルダー、またはドキュメント セット内のすべてのコンテンツへの既定の保持ラベルの適用](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set)」を参照してください。
  
![ファイルとフォルダーのラベル アクティビティを表示するドロップダウン メニュー](../media/11030584-f52d-49eb-86f3-7ead16a3b704.png)
  
### <a name="label-activities"></a>ラベル アクティビティ

 ラベルの**追加**、**削除**、**変更**の、ラベルに関するすべての操作が**ラベル アクティビティ**に該当します。このビューを使用して、それぞれのラベルがどのぐらいの数のファイルに適用されたかの包括的な確認を日別で行うことができます。 
  
### <a name="label-changes"></a>ラベルの変更

 **ラベルの変更**には、ラベルの**削除**または**変更**によって危険が生じる可能性のある操作の情報が含まれています。このビューを使用すれば、そのような危険な操作と実行したユーザーをすぐに確認できます。グラフの下にあるアクティビティ リストでファイルを選択し、右側の詳細ウィンドウにあるそのファイルのリンクをクリックすると、詳細情報を確認できます。 
  
![ラベル アクティビティの詳細ウィンドウ](../media/eb580fd4-b5be-4fda-9ba5-c1256777310d.png)
  
## <a name="filter-label-activity"></a>ラベル アクティビティのフィルター処理

データをすばやくフィルター処理して、特定のレベル、ファイル、ユーザーのラベル アクティビティすべてを表示できます。場所 (SharePoint または OneDrive for Business) や、ラベルが適用された方法 (手動か自動) でラベル アクティビティをフィルター処理することもできます。
  
![ラベル アクティビティのフィルター](../media/9de92985-120f-48b4-96a7-ef7ec8a71ff0.png)
  

