---
title: Office 365 の自動調査と応答に関する保留中の修復アクションを確認および承認する
keywords: AIR、自動赤外線、ATP、自動化、調査、応答、修復、脅威、高度、脅威、保護
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Office 365 Advanced Threat Protection プラン2の自動調査および応答機能の修復アクションについて説明します。
ms.openlocfilehash: d2b617e29fc36d1f39ab6c9ef6f708d5f608b206
ms.sourcegitcommit: 2859c82b30ae9cbd3a3e4bcdebd65f18444f1a9e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "42826464"
---
# <a name="view-pending-or-completed-remediation-actions-following-an-automated-investigation-in-office-365"></a><span data-ttu-id="bcc81-104">Office 365 の自動調査の後に、保留中または完了した修復アクションを表示する</span><span class="sxs-lookup"><span data-stu-id="bcc81-104">View pending or completed remediation actions following an automated investigation in Office 365</span></span>

## <a name="approve-or-reject-pending-actions"></a><span data-ttu-id="bcc81-105">保留中のアクションを承認 (または拒否) します。</span><span class="sxs-lookup"><span data-stu-id="bcc81-105">Approve (or reject) pending actions</span></span>

![AIR の調査処理 ページ](../../media/air-investigationactionspage.png)

<span data-ttu-id="bcc81-107">[調査の詳細](air-view-investigation-results.md)を表示している間に、保留中の修復処理を承認または拒否することができます。</span><span class="sxs-lookup"><span data-stu-id="bcc81-107">While viewing the [details of an investigation](air-view-investigation-results.md), you can approve or reject any pending remediation actions.</span></span> <span data-ttu-id="bcc81-108">自動化された調査が完了するように、この手順をできるだけ早く実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bcc81-108">We recommend doing this as soon as possible so that your automated investigations complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bcc81-109">修復アクションを承認または拒否するには、適切なアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="bcc81-109">Appropriate permissions are required to approve or reject remediation actions.</span></span> <span data-ttu-id="bcc81-110">[AIR 機能を使用するには、必要なアクセス許可を](office-365-air.md#required-permissions-to-use-air-capabilities)参照してください。</span><span class="sxs-lookup"><span data-stu-id="bcc81-110">See [Required permissions to use AIR capabilities](office-365-air.md#required-permissions-to-use-air-capabilities).</span></span>

1. <span data-ttu-id="bcc81-111">[https://protection.office.com](https://protection.office.com) に移動し、サインインします。</span><span class="sxs-lookup"><span data-stu-id="bcc81-111">Go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="bcc81-112">これにより、セキュリティ & コンプライアンスセンターに移動できます。</span><span class="sxs-lookup"><span data-stu-id="bcc81-112">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="bcc81-113">[**脅威管理** > の**調査**] に移動します。</span><span class="sxs-lookup"><span data-stu-id="bcc81-113">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="bcc81-114">調査の一覧で、[ **ID** ] 列のアイテムを選択します。</span><span class="sxs-lookup"><span data-stu-id="bcc81-114">In the list of investigations, select an item in the **ID** column.</span></span> 

4. <span data-ttu-id="bcc81-115">[**操作**] タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="bcc81-115">Select the **Actions** tab.</span></span>

5. <span data-ttu-id="bcc81-116">リストからアイテムを選択します。</span><span class="sxs-lookup"><span data-stu-id="bcc81-116">Select an item in the list.</span></span> <span data-ttu-id="bcc81-117">(これにより、[承認] ボタンと [拒否] ボタンが有効になります)。</span><span class="sxs-lookup"><span data-stu-id="bcc81-117">(This activates the Approve and Reject buttons.)</span></span>

6. <span data-ttu-id="bcc81-118">選択したアイテムの利用可能な情報を確認し、その操作を承認または拒否します。</span><span class="sxs-lookup"><span data-stu-id="bcc81-118">Review available information for the item(s) you selected, and then either approve or reject the action(s).</span></span> 
 - <span data-ttu-id="bcc81-119">**承認**は修復を開始することを許可します。</span><span class="sxs-lookup"><span data-stu-id="bcc81-119">**Approve** allows remediation to begin.</span></span>
 - <span data-ttu-id="bcc81-120">**却下**にはその他のアクションはありません</span><span class="sxs-lookup"><span data-stu-id="bcc81-120">**Reject** takes no further action</span></span>

## <a name="next-steps"></a><span data-ttu-id="bcc81-121">次の手順</span><span class="sxs-lookup"><span data-stu-id="bcc81-121">Next steps</span></span>

- [<span data-ttu-id="bcc81-122">Office 365 の自動調査の詳細と結果</span><span class="sxs-lookup"><span data-stu-id="bcc81-122">Details and results of an automated investigation in Office 365</span></span>](air-view-investigation-results.md)

- [<span data-ttu-id="bcc81-123">脅威エクスプローラーを使用する</span><span class="sxs-lookup"><span data-stu-id="bcc81-123">Use Threat Explorer</span></span>](threat-explorer.md)