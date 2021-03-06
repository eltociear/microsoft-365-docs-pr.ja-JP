---
title: 管理センターの Microsoft 365 レポート-Yammer デバイスの使用状況レポート
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: b793ffdd-effa-43d0-849a-b1ca2e899f38
description: 'Yammer デバイスの使用状況レポートを取得して、ユーザーが Yammer を使用しているデバイスについて把握します。 '
ms.openlocfilehash: 1dfd72c8974aa10b3774d2cdb17ac1bf82b9501b
ms.sourcegitcommit: 2b626a7924b4be08f6eb21181453b778e6fde418
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/30/2020
ms.locfileid: "43047013"
---
# <a name="microsoft-365-reports-in-the-admin-center---yammer-device-usage-report"></a>管理センターの Microsoft 365 レポート-Yammer デバイスの使用状況レポート

Microsoft 365 **Reports** dashboard には、組織内の製品全体にわたるアクティビティの概要が表示されます。 これにより、個別の製品レベルのレポートを詳細に確認して、各製品内のアクティビティについてより詳しく知ることができます。 [レポートの概要に関するトピック](activity-reports.md)を参照してください。
  
Yammer デバイスの使用状況レポートでは、ユーザーが Yammer を使用しているデバイスについての情報を示します。デバイスの種類別に毎日使用するユーザー数を表示したり、デバイスの種類別にユーザー数を表示したりします。どちらも選択した期間で表示できます。また、ユーザーごとの詳細を表示することもできます。
  
> [!NOTE]
> レポートを表示するには、Microsoft 365 または Exchange、SharePoint、Teams サービス、Teams 通信、または Skype for Business 管理者のグローバル管理者、グローバル閲覧者またはレポート閲覧者である必要があります。 
  
## <a name="how-do-i-get-to-the-yammer-device-usage-report"></a>Yammer デバイスの使用状況レポートの作成方法

1. 管理センターで、[**レポート**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">使用状況</a>] ページの順に移動します。

    
2. **[レポートの選択**] ドロップダウンから、[ **Yammer** \> **デバイスの使用状況**] を選択します。
  
## <a name="interpret-the-yammer-activity-report"></a>Yammer のアクティビティ レポートの内容を理解する

ユーザーの Yammer デバイスの使用状況を詳しく見るには、[ **ユーザー**] グラフと [ **分布**] グラフを確認します。 
  
デバイスの使用状況レポートには、次の情報が含まれます。
  
- [日] タブを使用して、過去7日間、30日間、90日間、または180日の**Yammer デバイスの使用**状況レポートの傾向を表示します。 ただし、レポートで特定の日を選択すると、テーブルには、現在の日付 (レポートが生成された日付ではありません) から最大28日間のデータが表示されます。 
    
- 各レポートには、このレポートが生成された日付が表示されます。通常、レポートはアクティビティの時刻から 24 から 48 時間の遅延を反映します。
    
- [ **ユーザー**] グラフでは、デバイスの種類別に毎日使用するユーザー数が表示されます。<br/>![Yammer デバイスの使用状況のグラフのユーザービュー](../../media/ecfba1ec-fbea-4491-88da-1fb19b4d5629.png)<br/>![ユーザービューを示す Yammer デバイスの使用状況レポート](../../media/f396865a-ad6e-4f8b-a145-cc3865b352f4.png)
  
- [ **分布**] グラフでは、デバイスの種類別にユーザー数が表示されます。<br/>![Yammer デバイスの使用状況レポートの配布ビュー](../../media/7a0b152e-2d2b-4d23-8dc2-046be53b724f.png)<br/>![Yammer のデバイス使用状況レポート](../../media/780c351d-7a1d-451d-8c16-4c454ef58aa8.png)
  
- グラフの下の [ **詳細**] 表には、Yammer デバイスの使用状況の内訳がユーザー レベルごとに表示されます。 
    
    列を追加および削除することもできます。使用可能な列は次のとおりです。
    
  - [ **ユーザー名**] はユーザーのメール アドレスです。 実際のメール アドレスを表示することも、このフィールドを匿名にすることもできます。 
    
    このグリッドには、Microsoft 365 アカウントを使用して Yammer にログインしたユーザー、またはシングルサインオンを使用してネットワークにログインしたユーザーが表示されます。
    
  - [ **表示名**] はユーザーの氏名です。実際のメール アドレスを表示することも、このフィールドを匿名にすることもできます。 
    
  - [ **ユーザー状態**] は、アクティブ、削除済み、または中断の 3 つの値で示されます。 
    
    このレポートには、アクティブ、中断、および削除済みのユーザーのデータが表示されます。保留中のユーザーは反映されません。このようなユーザーはメッセージの投稿、閲覧、または「いいね!」ができないためです。
    
  - [ **Web**] では、ユーザーが Web で Yammer を使用したかどうかが示されます。 
    
  - [ **Windows Phone**] では、ユーザーが Windows Phone で Yammer を使用したかどうかが示されます。 
    
  - [ **Android スマートフォン**] では、ユーザーが Android スマートフォンで Yammer を使用したかどうかが示されます。 
    
  - [ **iPhone**] では、ユーザーが iPhone で Yammer を使用したかどうかが示されます。 
    
  - [ **iPad**] では、ユーザーが iPad で Yammer を使用したかどうかが示されます。 
    
  - [ **その他**] では、ユーザーがそれ以外のデバイスで Yammer を使用したかどうかが示されます。 
    
    組織のポリシーにより、ユーザー情報を特定できるレポートを表示できない場合は、これらすべてのレポートのプライバシー設定を変更できます。 「**Microsoft 365 管理センターのアクティビティ レポート**」の「[ユーザー レベルの詳細を非表示にする方法](activity-reports.md)」セクションを参照してください。
    
- **エクスポート**リンクを選択して、レポートデータを Excel の .csv ファイルにエクスポートすることもできます。 これにより、すべてのユーザーのデータがエクスポートされ、単純な並べ替えとフィルター処理を行ってさらに分析することができます。 ユーザー数が 2000 未満である場合は、レポート自体のテーブル内で並べ替えとフィルター処理を行うことができます。 ユーザー数が 2000 を超える場合は、フィルター処理と並べ替えを行うために、データをエクスポートする必要があります。 
    

