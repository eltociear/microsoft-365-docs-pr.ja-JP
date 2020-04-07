---
title: セルフサービスのサインアップサブスクリプションを管理する
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- commerce
- Adm_NonTOC
search.appverid:
- MET150
description: 組織の無料セルフサービスサインアップサブスクリプションを管理する方法について説明します。
ms.openlocfilehash: 056ae95f9f5067ea3fa86164b620c72c84e3aad4
ms.sourcegitcommit: e525bcf073a61e1350484719a0c3ceb6ff0d8db1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2020
ms.locfileid: "43154138"
---
# <a name="manage-self-service-sign-up-subscriptions"></a><span data-ttu-id="b9cde-103">セルフサービスのサインアップサブスクリプションを管理する</span><span class="sxs-lookup"><span data-stu-id="b9cde-103">Manage self-service sign-up subscriptions</span></span>

## <a name="what-are-self-service-sign-up-subscriptions"></a><span data-ttu-id="b9cde-104">セルフサービスのサインアップサブスクリプションとは</span><span class="sxs-lookup"><span data-stu-id="b9cde-104">What are self-service sign-up subscriptions?</span></span>

<span data-ttu-id="b9cde-105">組織内のユーザーがサインアップできる無料のセルフサービスサインアップサブスクリプションの数には制限があります。</span><span class="sxs-lookup"><span data-stu-id="b9cde-105">There are a limited number of free self-service sign-up subscriptions that users in your organization can sign up for.</span></span> <span data-ttu-id="b9cde-106">ユーザーは自分でサインアップし、セルフサービスのサインアップサブスクリプションを自分自身に対してのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b9cde-106">A user can only sign up for and use a self-service sign-up subscription for themselves.</span></span> <span data-ttu-id="b9cde-107">これらのサブスクリプションは、[ **Products & services** ] ページに表示され、**空き**のマークが付けられ、"会社のユーザーによってライセンス認証が完了しました" というメモがあります。</span><span class="sxs-lookup"><span data-stu-id="b9cde-107">These subscriptions appear on the **Products & services** page, are marked as **Free**, and have a note that says, "This is a free subscription activated by users in your company."</span></span> <span data-ttu-id="b9cde-108">セルフサービスのサインアップサブスクリプションを管理するには、ユーザーのサインアップをブロックし、ユーザーがサインアップした無料のサブスクリプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9cde-108">You can manage self-service sign-up subscriptions by blocking users from signing up, and by deleting free subscriptions that users have signed up for.</span></span> <span data-ttu-id="b9cde-109">セルフサービスのサインアップと利用可能なサブスクリプションの詳細については、「[組織でのセルフサービスサインアップの使用](../../admin/misc/self-service-sign-up.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9cde-109">For more information about self-service sign up and the available subscriptions, see [Using self-service sign up in your organization](../../admin/misc/self-service-sign-up.md).</span></span>

## <a name="how-are-these-subscriptions-different-from-self-service-purchase-subscriptions"></a><span data-ttu-id="b9cde-110">これらのサブスクリプションはセルフサービス購入サブスクリプションとどのような違いがありますか?</span><span class="sxs-lookup"><span data-stu-id="b9cde-110">How are these subscriptions different from self-service purchase subscriptions?</span></span>

<span data-ttu-id="b9cde-111">セルフサービスサインアップサブスクリプションは無料であり、セルフサービス購入サブスクリプションよりも多くの製品リストで利用できます。</span><span class="sxs-lookup"><span data-stu-id="b9cde-111">Self-service sign-up subscriptions are free, and are available for a larger list of products than self-service purchase subscriptions.</span></span> <span data-ttu-id="b9cde-112">ユーザーがセルフサービス購入サブスクリプションにサインアップすると、ユーザーはそれに対して支払いを担当します。</span><span class="sxs-lookup"><span data-stu-id="b9cde-112">When a user signs up for a self-service purchase subscription, they are responsible for paying for it.</span></span> <span data-ttu-id="b9cde-113">また、セルフサービス購入サブスクリプションは、電源プラットフォーム製品 (Power BI、電源アプリ、および電源の自動化) に対してのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b9cde-113">Also, self-service purchase subscriptions are only available for Power Platform products (Power BI, Power Apps, and Power Automate).</span></span> <span data-ttu-id="b9cde-114">詳細については、「[セルフサービス購入](self-service-purchase-faq.md)に関する FAQ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9cde-114">For more information, see [Self-service purchase FAQ](self-service-purchase-faq.md).</span></span>

## <a name="block-users-from-signing-up"></a><span data-ttu-id="b9cde-115">ユーザーのサインアップをブロックする</span><span class="sxs-lookup"><span data-stu-id="b9cde-115">Block users from signing up</span></span>

<span data-ttu-id="b9cde-116">[**Set-msolcompanysettings**](https://docs.microsoft.com/powershell/module/msonline/set-msolcompanysettings?view=azureadps-1.0)コマンドレットを**AllowAdHocSubscriptions**パラメーターと共に使用して、ユーザーがセルフサービスサインアップサブスクリプションにサインアップできるかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="b9cde-116">You use the [**Set-MsolCompanySettings**](https://docs.microsoft.com/powershell/module/msonline/set-msolcompanysettings?view=azureadps-1.0) cmdlet with the **AllowAdHocSubscriptions** parameter to control whether users can sign up for self-service sign-up subscriptions.</span></span> <span data-ttu-id="b9cde-117">詳細については、「[セルフサービス設定を制御する方法](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-self-service-signup#how-do-i-control-self-service-settings)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9cde-117">For more information, see [How do I control self-service settings?](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-self-service-signup#how-do-i-control-self-service-settings)</span></span>

## <a name="delete-a-self-service-sign-up-subscription"></a><span data-ttu-id="b9cde-118">セルフサービスのサインアップサブスクリプションを削除する</span><span class="sxs-lookup"><span data-stu-id="b9cde-118">Delete a self-service sign-up subscription</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9cde-119">セルフサービスのサインアップサブスクリプションを削除すると、すべてのユーザーが自分のデータや電子メールにアクセスしたり、すべてのデータとメールを削除したりするのをブロックします。</span><span class="sxs-lookup"><span data-stu-id="b9cde-119">When you delete a self-service sign-up subscription, you block all users from accessing their data and email and delete all data and email.</span></span>

1. <span data-ttu-id="b9cde-120">管理センターで、**[課金]** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">[製品とサービス]</a> ページの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9cde-120">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Products & services</a> page.</span></span>
2. <span data-ttu-id="b9cde-121">削除するセルフサービスのサインアップサブスクリプションを検索します。</span><span class="sxs-lookup"><span data-stu-id="b9cde-121">Find the self-service sign-up subscription that you want to delete.</span></span> <span data-ttu-id="b9cde-122">[**設定 &** の [アクション] セクションで、[**サブスクリプションの削除**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9cde-122">In the **Settings & Actions** section, select **Delete subscription**.</span></span>
3. <span data-ttu-id="b9cde-123">[**サブスクリプションの削除**] ウィンドウで、チェックボックスをオンにして、[**サブスクリプションの削除**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9cde-123">In the **Delete subscription** pane, select the check box, then select **Delete subscription**.</span></span>

## <a name="i-have-a-self-service-sign-up-subscription-that-blocks-directory-deletion"></a><span data-ttu-id="b9cde-124">ディレクトリの削除をブロックするセルフサービスのサインアップサブスクリプションがあります</span><span class="sxs-lookup"><span data-stu-id="b9cde-124">I have a self-service sign-up subscription that blocks directory deletion</span></span>

<span data-ttu-id="b9cde-125">個々のユーザーがサインアップできるセルフサービスサインアップ製品は、Azure AD ディレクトリで認証のためのゲストユーザーを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="b9cde-125">The self-service sign-up products that individual users can sign up for also create a guest user for authentication in your Azure AD directory.</span></span> <span data-ttu-id="b9cde-126">データ損失を回避するため、これらのセルフサービス製品はディレクトリから完全に削除されるまでディレクトリの削除をブロックします。</span><span class="sxs-lookup"><span data-stu-id="b9cde-126">To avoid data loss, these self-service products block directory deletions until they're fully deleted from the directory.</span></span> <span data-ttu-id="b9cde-127">Azure AD 管理者のみが削除できます。詳細については、「 [Azure Active directory でディレクトリを削除する](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-delete-howto)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9cde-127">They can be deleted only by the Azure AD admin. For more information, see [Delete a directory in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-delete-howto).</span></span>