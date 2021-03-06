---
title: SharePoint、OneDrive、Microsoft Teams で検出された悪意のあるファイルに関する情報を表示する
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
ms.collection:
- M365-security-compliance
description: SharePoint、OneDrive、Teams で検出された悪意のあるファイルに関する情報を表示する方法と、それらのファイルに対してアクションを実行する方法について説明します。
ms.openlocfilehash: 95f497c5be16d1ba1d4fa9fc57f0dd9650450414
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43635402"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>SharePoint、OneDrive、Microsoft Teams で検出された悪意のあるファイルに関する情報を表示する

[Office 365 ATP For SharePoint、OneDrive、Microsoft Teams](atp-for-spo-odb-and-teams.md)では、組織がドキュメントライブラリおよびチームサイト内の悪意のあるファイルから保護されます。 悪意のあるファイルが検出されると、そのファイルはブロックされるようになり、組織のセキュリティチームによって追加の操作が行われるまで、そのファイルを開いたり、コピー、移動、または共有することができなくなります。 この記事では、検出されたファイルと実行するアクションに関する情報を表示する方法について説明します。 

この記事で説明されているタスクを実行するには、[セキュリティ&amp;コンプライアンスセンターに必要なアクセス許可](permissions-in-the-security-and-compliance-center.md)を持っている必要があります。 
  
## <a name="view-reports-with-information-about-detected-files"></a>検出されたファイルに関する情報をレポートを表示する

Office 365 ATP によって検出されたファイルの状態と詳細情報を表示するには、脅威保護の状態レポートを使用できます。
  
1. [[セキュリティ&amp; /コンプライアンスセンター](https://protection.office.com)] で、[**レポート** \> **ダッシュボード** \>の**脅威保護の状態**] を選択します。
    
2. レポートの右上隅で、[**詳細テーブルの表示**] を選択します。
    
3. レポートで検出されたファイルの一覧を表示します。
    
4. リスト内の項目を選択して、実行されたアクション、ファイル名、ファイルパスなどを含む詳細情報を表示します。
    
5. [**詳細分析**] タブを選択して、観測された動作や分析の詳細などの情報を表示します。 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a>検疫内のファイルを表示し、処理を実行する

1. セキュリティ&amp; /コンプライアンスセンターで、[**脅威管理** \> **レビュー** \>の**検疫**] を選択します。 (に[https://protection.office.com/quarantine](https://protection.office.com/quarantine)直接移動することもできます。)
    
2. 左上隅で、ドロップダウンメニューの [**電子メール**] を [**ファイル**] に変更します。 結果のリストに含まれるアイテムが多すぎる場合は、**フィルター**機能を使用して選択範囲を絞り込みます。
    
3. リストで項目を選択すると、ファイルの URL などの詳細情報が表示されます。
    
4. 使用可能なアクションを選択します。
    
    - ファイルのブロックを解除するには、[**ファイルの解放**] を選択します。 

      Microsoft への誤検知としてファイルを報告するには、[ **microsoft にレポートを送信**する] を選択します。 

    - [**ファイルのダウンロード**] を選択して、ファイルをさらに調査します。 

    - 検疫されたアイテムのリストからファイルを削除するには、[**検疫から削除**] を選択します。 このオプションを選択する場合は、SharePoint Online、OneDrive for Business、または Microsoft Teams の対応するライブラリからもファイルを削除する必要があります。 このオプションでは、ファイルが開かれたり共有されたりすることはブロックされません。 
    
5. [**閉じる**] を選択して、選択したアイテムの詳細を閉じます。 
  
  

