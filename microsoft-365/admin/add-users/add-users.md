---
title: Office 365 にユーザーを個別にまたは一括して追加する
f1.keywords:
- NOCSH
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
- Adm_O365_Setup
- Adm_O365_TOC
ms.custom:
- MSStore_Link
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 1970f7d6-03b5-442f-b385-5880b9c256ec
description: Office 365 にユーザーを 1 人ずつまたは同時に複数のユーザーを CSV ファイルから追加する方法について説明します。
ms.openlocfilehash: 708bce2cb5a2c1b6a621bffc3ce56a2744bb518d
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/24/2020
ms.locfileid: "42241686"
---
# <a name="add-users-individually-or-in-bulk-to-office-365"></a><span data-ttu-id="aae0b-103">Office 365 にユーザーを個別にまたは一括して追加する</span><span class="sxs-lookup"><span data-stu-id="aae0b-103">Add users individually or in bulk to Office 365</span></span>

<span data-ttu-id="aae0b-104">[一般法人向け Office 365](https://go.microsoft.com/fwlink/?LinkID=519395) にサインインしてアクセスする前に、チームの各ユーザーにはユーザー アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="aae0b-104">The people on your team each need a user account before they can sign in and access [Office 365 for business](https://go.microsoft.com/fwlink/?LinkID=519395).</span></span> <span data-ttu-id="aae0b-105">ユーザー アカウントを追加する最も簡単な方法は、Microsoft 365 管理センターで 1 人ずつ追加する方法です。</span><span class="sxs-lookup"><span data-stu-id="aae0b-105">The easiest way to add user accounts is to add them one at a time in the Microsoft 365 admin center.</span></span> <span data-ttu-id="aae0b-106">この手順を実行すると、Office 365 ライセンス、サインイン用の資格情報、および Office 365 メールボックスがユーザーに付与されます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-106">After you do this step, your users will have Office 365 licenses, sign in credentials, and Office 365 mailboxes.</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="aae0b-107">新しい Microsoft 365 管理センターを利用していない場合、[ホーム] ページの上部にある [**新しい管理センターをお試しください**] の切り替えを選択して有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-107">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="aae0b-108"><a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> の管理センターにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="aae0b-108">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="aae0b-109">[**ユーザー**] > [**アクティブなユーザー**] の順に移動し、[**ユーザーの追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-109">Go to **Users** > **Active users**, and select **Add a user**.</span></span>
   
3. <span data-ttu-id="aae0b-110">[**基本設定**] ウィンドウに次の情報を入力し、[**次へ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-110">In the **Set up the basics** pane, fill in the following information, and then select **Next**.</span></span> 
  
- <span data-ttu-id="aae0b-111">[**名前**] 姓、名、表示名、ユーザー名を入力します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-111">**Name** Fill in first, last, display name, and username.</span></span> 
    
- <span data-ttu-id="aae0b-112">[ **ドメイン**] たとえば、ユーザー名が Jakob、そのドメインが contoso.com の場合、Office 365 にサインインするには、「jakob@contoso.com」と入力します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-112">**Domain** For example, if the user's username is Jakob, and his domain is contoso.com, he'll sign in to Office 365 by typing jakob@contoso.com.</span></span> 
    
- <span data-ttu-id="aae0b-113">[**パスワードの設定**] ユーザー用のパスワードとして、自動生成されたパスワードを使用するのか独自の強力なパスワードを作成するのかを選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-113">**Password settings** Choose to the use auto-generated password or create your own strong password for the user.</span></span> 
    
    - <span data-ttu-id="aae0b-114">ユーザーは 90 日後にパスワードを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aae0b-114">They'll need to change their password after 90 days.</span></span> <span data-ttu-id="aae0b-115">または、[**初回サインイン時にこのユーザーにパスワードの変更を要求する**] を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-115">Or you can choose to **Require this user to change their password when they first sign in**.</span></span>
    
    - <span data-ttu-id="aae0b-116">ユーザーが追加されたときに、パスワードをメールで送信するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-116">Choose whether you want to  send the password in email when the user has been added.</span></span> 
    
4. <span data-ttu-id="aae0b-117">[**製品ライセンスの割り当て**] ウィンドウで、ユーザーの場所と適切なライセンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-117">In the **Assign product licenses** pane, select the location and the appropriate license for the user.</span></span> <span data-ttu-id="aae0b-118">利用可能なライセンスがない場合でも、ユーザーを追加し、追加のライセンスを購入できます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-118">If you don't have any licenses available, you can still add a user and buy additional licenses.</span></span> <span data-ttu-id="aae0b-119">[**次へ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-119">Select **Next**.</span></span>

5. <span data-ttu-id="aae0b-120">[**オプションの設定**] ページで、このユーザーを管理者にする場合は [**役割**] を展開します。ユーザーに関する追加情報を入力する場合は、[**プロファイル情報**] を展開します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-120">In the **Optional settings** page, expand **Roles** if you want to make this user an admin, and expand **Profile info** if you want to add additional information about the user.</span></span> 

6. <span data-ttu-id="aae0b-121">[**次へ**] を選択し、新しいユーザーの設定を確認し、必要に応じて変更を行い、[**追加の完了**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-121">Select **Next**, review your new user's settings, make any changes you like, and then select **Finish adding**.</span></span> 

::: moniker-end


::: moniker range="o365-germany"

1. <span data-ttu-id="aae0b-122"><a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a> で管理センターにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="aae0b-122">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a>.</span></span>

2. <span data-ttu-id="aae0b-123">[**ユーザー**] > [**アクティブなユーザー**] の順に移動し、[**ユーザーの追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-123">Go to **Users** > **Active users**, and select **Add a user**.</span></span>
   
  
   <span data-ttu-id="aae0b-124">[**新しいユーザー**] ウィンドウで、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-124">In the **New user** pane, fill in the following information.</span></span> <span data-ttu-id="aae0b-125">完了したら、[**追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-125">Select **Add** when you are done.</span></span> 
  
- <span data-ttu-id="aae0b-126">[**名前**] 名、姓、表示名、ユーザー名を入力します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-126">**Name** Fill in first, last, display name, and user name.</span></span> 
    
- <span data-ttu-id="aae0b-127">[ **ドメイン**] たとえば、ユーザー名が Jakob、そのドメインが contoso.com の場合、Office 365 にサインインするには、「jakob@contoso.com」と入力します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-127">**Domain** For example, if the user's username is Jakob, and his domain is contoso.com, he'll sign in to Office 365 by typing jakob@contoso.com.</span></span> 
    
- <span data-ttu-id="aae0b-128">[**連絡先情報**] 展開して、携帯電話番号、住所などを入力します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-128">**Contact information** Expand to fill in a mobile phone number, address, and so on.</span></span> 
    
- <span data-ttu-id="aae0b-129">[**パスワード**] 自動生成されたパスワードを使用するか、展開してユーザーに強力なパスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-129">**Password** Use the auto-generated password or expand to specify a strong password for the user.</span></span> 
    
    <span data-ttu-id="aae0b-p105">ユーザーは、90 日後にパスワードを変更する必要があります。または、[**ユーザーが初回サインイン時にパスワードを変更する**] を選ぶこともできます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-p105">They'll need to change their password after 90 days. Or you can choose to **Make this user change their password when they first sign in**.</span></span>
    
- <span data-ttu-id="aae0b-132">[**役割**] このユーザーに管理者権限を割り当てる場合に展開します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-132">**Roles** Expand if you need to make this user an admin.</span></span> 
    
- <span data-ttu-id="aae0b-p106">[**製品ライセンス**] このセクションを展開し、適切なライセンスを選択します。利用可能なライセンスを持っていない場合でも、ユーザーを追加したり、追加のライセンスを購入したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-p106">**Product licenses** Expand this section and select the appropriate license. If you don't have any licenses available, you can still add a user and buy additional licenses.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="aae0b-135"><a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a> で管理センターにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="aae0b-135">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span></span>

2. <span data-ttu-id="aae0b-136">[**ユーザー**] > [**アクティブなユーザー**] の順に移動し、[**ユーザーの追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-136">Go to **Users** > **Active users**, and select **Add a user**.</span></span>
   
  
   <span data-ttu-id="aae0b-137">[**新しいユーザー**] ウィンドウで、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-137">In the **New user** pane, fill in the following information.</span></span> <span data-ttu-id="aae0b-138">完了したら、[**追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-138">Select **Add** when you are done.</span></span> 
  
- <span data-ttu-id="aae0b-139">[**名前**] 名、姓、表示名、ユーザー名を入力します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-139">**Name** Fill in first, last, display name, and user name.</span></span> 
    
- <span data-ttu-id="aae0b-140">[ **ドメイン**] たとえば、ユーザー名が Jakob、そのドメインが contoso.com の場合、Office 365 にサインインするには、「jakob@contoso.com」と入力します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-140">**Domain** For example, if the user's username is Jakob, and his domain is contoso.com, he'll sign in to Office 365 by typing jakob@contoso.com.</span></span> 
    
- <span data-ttu-id="aae0b-141">[**連絡先情報**] 展開して、携帯電話番号、住所などを入力します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-141">**Contact information** Expand to fill in a mobile phone number, address, and so on.</span></span> 
    
- <span data-ttu-id="aae0b-142">[**パスワード**] 自動生成されたパスワードを使用するか、展開してユーザーに強力なパスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-142">**Password** Use the auto-generated password or expand to specify a strong password for the user.</span></span> 
    
    <span data-ttu-id="aae0b-p108">ユーザーは、90 日後にパスワードを変更する必要があります。または、[**ユーザーが初回サインイン時にパスワードを変更する**] を選ぶこともできます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-p108">They'll need to change their password after 90 days. Or you can choose to **Make this user change their password when they first sign in**.</span></span>
    
- <span data-ttu-id="aae0b-145">[**役割**] このユーザーに管理者権限を割り当てる場合に展開します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-145">**Roles** Expand if you need to make this user an admin.</span></span> 
    
- <span data-ttu-id="aae0b-p109">[**製品ライセンス**] このセクションを展開し、適切なライセンスを選択します。利用可能なライセンスを持っていない場合でも、ユーザーを追加したり、追加のライセンスを購入したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-p109">**Product licenses** Expand this section and select the appropriate license. If you don't have any licenses available, you can still add a user and buy additional licenses.</span></span> 

::: moniker-end 
  
<span data-ttu-id="aae0b-148">ユーザーの追加後に、ユーザーが Microsoft Online Services チームからのメール通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-148">After you add a user, you'll get an email notification from the Microsoft Online Services Team.</span></span> <span data-ttu-id="aae0b-149">メールには、ユーザーが Office 365 にサインインするための、Office 365 のユーザー ID とパスワードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="aae0b-149">The email will contain the person's Office 365 user ID and password so they can sign in to Office 365.</span></span> <span data-ttu-id="aae0b-150">新しいユーザーに Office 365 のサインイン情報を知らせる必要があります。</span><span class="sxs-lookup"><span data-stu-id="aae0b-150">You need to tell your new user about their Office 365 sign in information.</span></span> <span data-ttu-id="aae0b-151">新しいパスワードは、通常のプロセスを使用して通知してください。</span><span class="sxs-lookup"><span data-stu-id="aae0b-151">Use your normal process for communicating new passwords.</span></span>

> [!NOTE]
><span data-ttu-id="aae0b-152">メールボックスを移行してユーザーを作成する場合、ユーザーにライセンスを割り当てることによって Office 365 のユーザー アカウントのライセンス認証を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="aae0b-152">If you create users by migrating mail boxes, you will need to activate Office 365 user accounts by assigning licenses.</span></span> <span data-ttu-id="aae0b-153">ユーザーにライセンスを割り当てない場合、30 日間の猶予期間が過ぎるとユーザーのメールボックスが無効になります。</span><span class="sxs-lookup"><span data-stu-id="aae0b-153">If you don't assign a license to a user, their mailbox will be disabled after a grace period of 30 days.</span></span> <span data-ttu-id="aae0b-154">Microsoft 365 管理センターを使用して[ライセンスをユーザーに割り当てる](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc)方法をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="aae0b-154">See how to [assign licenses to users](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc) using the Microsoft 365 admin center.</span></span>

### <a name="video-add-and-manage-users-in-the-admin-center"></a><span data-ttu-id="aae0b-155">ビデオ: 管理センターでユーザーを追加して管理する</span><span class="sxs-lookup"><span data-stu-id="aae0b-155">Video: Add and manage users in the admin center</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1FOfN?autoplay=false]
  
## <a name="next-steps"></a><span data-ttu-id="aae0b-156">次の手順</span><span class="sxs-lookup"><span data-stu-id="aae0b-156">Next steps</span></span>

<span data-ttu-id="aae0b-157">
            [PC や Mac への Office のインストール](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658.aspx)および[モバイルへの Office アプリのインストール](https://support.office.com/article/7dabb6cb-0046-40b6-81fe-767e0b1f014f.aspx)を行う新しいユーザーと[Office 365 向け従業員のクイック スタート](https://support.office.com/article/b9700090-ce64-4046-ab92-ce8488a7bc0f.aspx)を共有してください。</span><span class="sxs-lookup"><span data-stu-id="aae0b-157">Share the [Employee quick start guide](https://support.office.com/article/b9700090-ce64-4046-ab92-ce8488a7bc0f.aspx) with your new users to set things up, like [Office on a PC or Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658.aspx) and [Office mobile apps](https://support.office.com/article/7dabb6cb-0046-40b6-81fe-767e0b1f014f.aspx).</span></span>
  
## <a name="need-help"></a><span data-ttu-id="aae0b-158">ヘルプが必要な場合</span><span class="sxs-lookup"><span data-stu-id="aae0b-158">Need help?</span></span>

<span data-ttu-id="aae0b-159">[一般法人向け Office 365 のサポートにお問い合わせください](../contact-support-for-business-products.md)。</span><span class="sxs-lookup"><span data-stu-id="aae0b-159">[Contact Office 365 for business support](../contact-support-for-business-products.md).</span></span>  

## <a name="have-hundreds-or-thousands-of-users-to-add"></a><span data-ttu-id="aae0b-160">多数のユーザーを追加する場合</span><span class="sxs-lookup"><span data-stu-id="aae0b-160">Have hundreds or thousands of users to add?</span></span>


<span data-ttu-id="aae0b-161">複数のユーザーを同時に追加するには、次の手順に従います。 </span><span class="sxs-lookup"><span data-stu-id="aae0b-161">To add multiple users at the same time, follow these steps:</span></span>
  
- <span data-ttu-id="aae0b-162">**ユーザーをまとめて追加するには、スプレッドシートを使用します。**</span><span class="sxs-lookup"><span data-stu-id="aae0b-162">**Use a spreadsheet to add people in bulk.**</span></span> <span data-ttu-id="aae0b-163">「[同時に複数のユーザーを追加する](https://docs.microsoft.com/office365/enterprise/add-several-users-at-the-same-time)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aae0b-163">See [Add several users at the same time](https://docs.microsoft.com/office365/enterprise/add-several-users-at-the-same-time).</span></span>
    
- <span data-ttu-id="aae0b-164">**アカウントの追加とライセンスの割り当てを自動化します。**</span><span class="sxs-lookup"><span data-stu-id="aae0b-164">**Automate adding accounts and assigning licenses.**</span></span> <span data-ttu-id="aae0b-165">「[Office 365 PowerShell を使用してユーザー アカウントを作成する](https://docs.microsoft.com/office365/enterprise/powershell/create-user-accounts-with-office-365-powershell)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aae0b-165">See [Create user accounts with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/create-user-accounts-with-office-365-powershell).</span></span> <span data-ttu-id="aae0b-166">この方法は、Windows PowerShell コマンドレットについて詳しい知識のある場合に選んでください。</span><span class="sxs-lookup"><span data-stu-id="aae0b-166">Choose this method if you're already familiar with using Windows PowerShell cmdlets.</span></span>
    
- <span data-ttu-id="aae0b-167">**ActiveDirectory を使用する場合**</span><span class="sxs-lookup"><span data-stu-id="aae0b-167">**Using ActiveDirectory?**</span></span> <span data-ttu-id="aae0b-168">[Office 365 のディレクトリ同期をセットアップ](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization)します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-168">[Set up directory synchronization for Office 365](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization).</span></span> <span data-ttu-id="aae0b-169">Azure AD Connect ツールを使用し、Office 365 で Active Directory ユーザー アカウント (およびその他の Active Directory オブジェクト) を複製します。</span><span class="sxs-lookup"><span data-stu-id="aae0b-169">Use the Azure AD Connect tool to replicate Active Directory user accounts (and other Active Directory objects) in Office 365.</span></span> <span data-ttu-id="aae0b-170">同期では、ユーザー アカウントのみが追加されます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-170">The sync only adds the user accounts.</span></span> <span data-ttu-id="aae0b-171">同期されているユーザーがメールとその他の Office アプリを使用するには、そのユーザーにライセンスを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="aae0b-171">You will need to assign licenses to the synced users before they can use email and other Office apps.</span></span>
    
- <span data-ttu-id="aae0b-172">**Exchange Server から移行する場合**</span><span class="sxs-lookup"><span data-stu-id="aae0b-172">**Migrating from Exchange?**</span></span> <span data-ttu-id="aae0b-173">[複数のメール アカウントを Office 365 に移行する方法](https://docs.microsoft.com/Exchange/mailbox-migration/mailbox-migration)。</span><span class="sxs-lookup"><span data-stu-id="aae0b-173">[Ways to migrate multiple email accounts to Office 365](https://docs.microsoft.com/Exchange/mailbox-migration/mailbox-migration).</span></span> <span data-ttu-id="aae0b-174">カットオーバー、段階的方法、またはハイブリッド Exchange による方法のいずれかを使って、複数のメールボックスを Office 365 に移行するときは、移行の一部としてユーザーが自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-174">When you migrate multiple mailboxes to Office 365 by using either cutover, staged, or a hybrid Exchange method, you will add users automatically as part of the migration.</span></span> <span data-ttu-id="aae0b-175">移行では、ユーザー アカウントのみが追加されます。</span><span class="sxs-lookup"><span data-stu-id="aae0b-175">The migration only adds the user accounts.</span></span> <span data-ttu-id="aae0b-176">ユーザーがメールとその他の Office アプリを使用するには、そのユーザーにライセンスを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="aae0b-176">You will need assign licenses to the users before they can use email and other Office apps.</span></span>

## <a name="related-articles"></a><span data-ttu-id="aae0b-177">関連記事</span><span class="sxs-lookup"><span data-stu-id="aae0b-177">Related articles</span></span>

[<span data-ttu-id="aae0b-178">Office 365 に新しい従業員を追加する</span><span class="sxs-lookup"><span data-stu-id="aae0b-178">Add a new employee to Office 365</span></span>](add-new-employee.md)

[<span data-ttu-id="aae0b-179">組織からユーザーを削除する</span><span class="sxs-lookup"><span data-stu-id="aae0b-179">Delete a user from your organization</span></span>](delete-a-user.md)

[<span data-ttu-id="aae0b-180">Office 365 でユーザーを復元する</span><span class="sxs-lookup"><span data-stu-id="aae0b-180">Restore a user in Office 365</span></span>](restore-user.md)

[<span data-ttu-id="aae0b-181">同時に複数のユーザーを Office 365 に追加する</span><span class="sxs-lookup"><span data-stu-id="aae0b-181">Add several users at the same time to Office 365</span></span>](https://docs.microsoft.com/office365/enterprise/add-several-users-at-the-same-time)

