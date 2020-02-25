---
title: Office 365 の修復アクション自動調査と応答
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
ms.openlocfilehash: 433813ed1a801117a88da696392030db5091b54b
ms.sourcegitcommit: 133bf7936e5ef1a4d06998429d0d01096bda929f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/24/2020
ms.locfileid: "42261054"
---
# <a name="remediation-actions-following-an-automated-investigation-in-office-365"></a><span data-ttu-id="52407-104">Office 365 での自動調査の後の修復アクション</span><span class="sxs-lookup"><span data-stu-id="52407-104">Remediation actions following an automated investigation in Office 365</span></span>

## <a name="remediation-actions"></a><span data-ttu-id="52407-105">修復アクション</span><span class="sxs-lookup"><span data-stu-id="52407-105">Remediation actions</span></span>

<span data-ttu-id="52407-106">Office 365 の[自動調査および応答機能](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air)高度な脅威保護には、特定の修復アクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="52407-106">[Automated investigation and response capabilities](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air) in Office 365 Advanced Threat Protection include certain remediation actions.</span></span> <span data-ttu-id="52407-107">自動化された調査を実行している場合や、完了した場合は、通常、セキュリティ運用チームによる承認を必要とする1つ以上の修復アクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="52407-107">Whenever an automated investigation is running or has completed, you'll typically see one or more remediation actions that require approval by your security operations team to proceed.</span></span> <span data-ttu-id="52407-108">次の表に、Office 365 Advanced Threat Protection で現在利用可能な修復処置の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="52407-108">The following table summarizes remediation actions currently available in Office 365 Advanced Threat Protection.</span></span> 

|<span data-ttu-id="52407-109">アクション</span><span class="sxs-lookup"><span data-stu-id="52407-109">Action</span></span> | <span data-ttu-id="52407-110">説明</span><span class="sxs-lookup"><span data-stu-id="52407-110">Description</span></span> |
|-----|-----|
|<span data-ttu-id="52407-111">URL のブロック (クリック時)</span><span class="sxs-lookup"><span data-stu-id="52407-111">Block URL (time-of-click)</span></span> |<span data-ttu-id="52407-112">悪意のある Url を含む電子メールやドキュメントを保護します。</span><span class="sxs-lookup"><span data-stu-id="52407-112">Protect against emails and documents that contain malicious URLs.</span></span> <span data-ttu-id="52407-113">これにより、ユーザーが既存の Office ファイルまたは古い電子メールメッセージ内のリンクをクリックしたときに、悪意のあるリンクや関連する web ページが[安全なリンク](https://docs.microsoft.com/microsoft-365/security/office-365-security/atp-safe-links)でブロックされるようになります。</span><span class="sxs-lookup"><span data-stu-id="52407-113">This enables the blocking of malicious links and any related webpages via [Safe Links](https://docs.microsoft.com/microsoft-365/security/office-365-security/atp-safe-links) when the user clicks a link in an existing Office file or in an older email message.</span></span> |
|<span data-ttu-id="52407-114">電子メールの削除 (ソフト)</span><span class="sxs-lookup"><span data-stu-id="52407-114">Soft delete email</span></span>  |<span data-ttu-id="52407-115">ユーザーのメールボックスから特定の電子メールメッセージを削除する</span><span class="sxs-lookup"><span data-stu-id="52407-115">Soft delete specific email messages from a user's mailbox</span></span>|
|<span data-ttu-id="52407-116">削除済みメールクラスターの回復</span><span class="sxs-lookup"><span data-stu-id="52407-116">Soft delete email clusters</span></span>  |<span data-ttu-id="52407-117">すべてのユーザーのメールボックスからのクエリに一致する悪意のある電子メールメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="52407-117">Soft delete malicious email messages matching a query from all users' mailboxes</span></span>|
|<span data-ttu-id="52407-118">外部メール転送の無効化</span><span class="sxs-lookup"><span data-stu-id="52407-118">Turn off external mail forwarding</span></span> |<span data-ttu-id="52407-119">特定のエンドユーザーのメールボックスから転送ルールを削除します。</span><span class="sxs-lookup"><span data-stu-id="52407-119">Removes forwarding rule from a specific end user's mailbox</span></span>|

## <a name="approve-or-reject-pending-actions"></a><span data-ttu-id="52407-120">保留中のアクションを承認 (または拒否) します。</span><span class="sxs-lookup"><span data-stu-id="52407-120">Approve (or reject) pending actions</span></span>

![AIR の調査処理 ページ](../../media/air-investigationactionspage.png)

<span data-ttu-id="52407-122">[調査の詳細](air-view-investigation-results.md)を表示している間に、保留中の修復処理を承認または拒否することができます。</span><span class="sxs-lookup"><span data-stu-id="52407-122">While viewing the [details of an investigation](air-view-investigation-results.md), you can approve or reject any pending remediation actions.</span></span> <span data-ttu-id="52407-123">自動化された調査が完了するように、この手順をできるだけ早く実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="52407-123">We recommend doing this as soon as possible so that your automated investigations complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52407-124">修復アクションを承認または拒否するには、適切なアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="52407-124">Appropriate permissions are required to approve or reject remediation actions.</span></span> <span data-ttu-id="52407-125">[AIR 機能を使用するには、必要なアクセス許可を](office-365-air.md#required-permissions-to-use-air-capabilities)参照してください。</span><span class="sxs-lookup"><span data-stu-id="52407-125">See [Required permissions to use AIR capabilities](office-365-air.md#required-permissions-to-use-air-capabilities).</span></span>

1. <span data-ttu-id="52407-126">[**操作**] タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="52407-126">Select the **Actions** tab.</span></span>

2. <span data-ttu-id="52407-127">リストからアイテムを選択します。</span><span class="sxs-lookup"><span data-stu-id="52407-127">Select an item in the list.</span></span> <span data-ttu-id="52407-128">(これにより、[承認] ボタンと [拒否] ボタンが有効になります)。</span><span class="sxs-lookup"><span data-stu-id="52407-128">(This activates the Approve and Reject buttons.)</span></span>

3. <span data-ttu-id="52407-129">選択したアイテムの利用可能な情報を確認し、その操作を承認または拒否します。</span><span class="sxs-lookup"><span data-stu-id="52407-129">Review available information for the item(s) you selected, and then either approve or reject the action(s).</span></span> 
 - <span data-ttu-id="52407-130">**承認**は修復を開始することを許可します。</span><span class="sxs-lookup"><span data-stu-id="52407-130">**Approve** allows remediation to begin.</span></span>
 - <span data-ttu-id="52407-131">**却下**にはその他のアクションはありません</span><span class="sxs-lookup"><span data-stu-id="52407-131">**Reject** takes no further action</span></span>

## <a name="next-steps"></a><span data-ttu-id="52407-132">次のステップ</span><span class="sxs-lookup"><span data-stu-id="52407-132">Next steps</span></span>

- [<span data-ttu-id="52407-133">侵害されたユーザーセキュリティのプレイブックについて</span><span class="sxs-lookup"><span data-stu-id="52407-133">Learn about the compromised user security playbook</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/address-compromised-users-quickly)

- [<span data-ttu-id="52407-134">ATP レポートを表示する</span><span class="sxs-lookup"><span data-stu-id="52407-134">View your ATP reports</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/view-reports-for-atp)