---
title: 自動調査後に保留中のアクションを承認または拒否する
description: アクション センターを使用して、自動調査と応答に関連するアクションを管理する
keywords: アクション、センター、autoair、自動、調査、応答、修復
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: deniseb
author: denisebmsft
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: conceptual
ms.custom: autoir
ms.openlocfilehash: 5c690d07af285b5232d383bb89071c3b64343772
ms.sourcegitcommit: 0c9c28a87201c7470716216d99175356fb3d1a47
ms.translationtype: MT + HT Review
ms.contentlocale: ja-JP
ms.lasthandoff: 12/09/2019
ms.locfileid: "39911379"
---
# <a name="approve-or-reject-pending-actions-from-automated-investigations"></a>自動調査による保留中のアクションを承認または拒否する

**適用対象:**
- Microsoft Threat Protection

[!include[Prerelease information](prerelease.md)]

自動調査が実行されたときに、調査を続行するには承認を必要とする 1 つまたは複数の[修復](mtp-action-center.md#remediation-actions)アクションが発生する場合があります。 たとえば、一連のメール メッセージを削除する必要がある場合や、検疫されたファイルを削除する必要がある場合があります。 自動調査を続行し適時完了できるよう、保留中のアクションはできるだけ早く承認 (または拒否) することが重要です。 

保留中のアクションを確認して承認する方法には、いくつかあります。
- [アクション センターを使用する](#review-a-pending-action-in-the-action-center)
- [[Investigation details (調査の詳細)] ビューを使用する](#review-a-pending-action-in-the-investigation-details-view)

> [!NOTE]
> 修復アクションを承認または拒否するには、[適切なアクセス許可](mtp-action-center.md#required-permissions-for-action-center-tasks)が必要です。

## <a name="review-a-pending-action-in-the-action-center"></a>保留中のアクションをアクション センターで確認する

1. [https://security.microsoft.com](https://security.microsoft.com) にアクセスし、サインインします。 

2. ナビゲーション ウィンドウで、[**アクション センター**] を選択します。 

3. アクション センターの [**Pending (保留中)**] タブで、リスト内のアイテムを選択します。 

    - [**Investigation number (調査番号)**] 列でアイテムを選択すると、[Investigation details (調査の詳細)] ページが開きます。 このページでは、調査の結果を表示し、推奨されるアクションを承認または拒否できます。
 
    - リスト内の行を選択すると、ポップアップが開き、そのアイテムに関する情報が表示されます。 <br/>![アクションを承認または拒否する](../images/air-actioncenter-itemselected.png)<br/>リンクを使用して関連付けられている警告または調査を表示し、アクションを承認または拒否します。

## <a name="review-a-pending-action-in-the-investigation-details-view"></a>保留中のアクションを調査の詳細ビューで確認する

![調査の詳細](../images/mtp-air-investdetails.png)

1. [[Investigation details (調査の詳細)](mtp-autoir-results.md)] ページで、[**Pending actions (保留中のアクション)**] (または [**Actions (アクション)**]) タブを選択します。承認待ちのアイテムがそこに表示されます。

2. リスト内のアイテムを選択し、[**Approve (承認)**] または [**Reject (拒否)**] を選択します。

## <a name="next-steps"></a>次のステップ

- [アクション センターの詳細](mtp-action-center.md)
- [インシデントの詳細](incidents-overview.md)
- [捜索の詳細](advanced-hunting-overview.md)