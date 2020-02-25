---
title: ユーザーに別のメール エイリアスを追加する
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 0b0bd900-68b1-4bf5-808b-5d240a7739f4
description: 'Office 365 for business アカウントに関連付けられている電子メールエイリアスと呼ばれる複数の電子メールアドレスを設定する方法について説明します。 '
ms.openlocfilehash: 10f219f380d30a5ee8e9822e7a35ee533d165c33
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/24/2020
ms.locfileid: "42255325"
---
# <a name="add-another-email-alias-for-a-user"></a><span data-ttu-id="6512b-103">ユーザーに別のメール エイリアスを追加する</span><span class="sxs-lookup"><span data-stu-id="6512b-103">Add another email alias for a user</span></span>
  
<span data-ttu-id="6512b-104">この記事は、ビジネスサブスクリプションを持つ Office 365 管理者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="6512b-104">This article is for Office 365 administrators who have business subscriptions.</span></span> <span data-ttu-id="6512b-105">ホーム ユーザー向けではありません。</span><span class="sxs-lookup"><span data-stu-id="6512b-105">It's not for home users.</span></span>
  
<span data-ttu-id="6512b-106">Office 365 のプライマリ電子メールアドレスは、通常、アカウントの作成時にユーザーが割り当てられた電子メールアドレスです。</span><span class="sxs-lookup"><span data-stu-id="6512b-106">A primary email address in Office 365 is usually the email address a user was assigned when their account was created.</span></span> <span data-ttu-id="6512b-107">ユーザーが別のユーザーにメールを送信するときに、通常、メール アプリの [ *差出人*  ] フィールドに表示されているものが、プライマリ メール アドレスとなります。</span><span class="sxs-lookup"><span data-stu-id="6512b-107">When the user sends email to someone else, their primary email address is what typically appears in the  *From*  field in email apps.</span></span> <span data-ttu-id="6512b-108">また、一般法人向け Office 365 アカウントに関連付けられた複数のメール アドレスを持つこともできます。</span><span class="sxs-lookup"><span data-stu-id="6512b-108">They can also have more than one email address associated with their Office 365 for business account.</span></span> <span data-ttu-id="6512b-109">これらの追加アドレスをエイリアスと呼びます。</span><span class="sxs-lookup"><span data-stu-id="6512b-109">These additional addresses are called aliases.</span></span> 
  
<span data-ttu-id="6512b-110">たとえば、Jenna が電子メールアドレス jenna@contosoco.com を持っているとしますが、ユーザーがその名前で自分を参照している場合は、jen@contosoco.com で電子メールを受信したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="6512b-110">For example, let's say Jenna has the email address jenna@contosoco.com, but she also wants to receive email at jen@contosoco.com because some people refer to her by that name.</span></span> <span data-ttu-id="6512b-111">両方の電子メールアドレスが Jenna の受信トレイに送られるように、のエイリアスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="6512b-111">You can create aliases for her so that both email addresses go to Jenna's inbox.</span></span>
<br><br>  
  
<span data-ttu-id="6512b-112">ユーザーあたり最大 400 個のエイリアスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6512b-112">You can create up to 400 aliases for a user.</span></span> <span data-ttu-id="6512b-113">追加の料金やライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6512b-113">No additional fees or licenses are required.</span></span>
  
> [!Tip]
> <span data-ttu-id="6512b-114">Info@NodPublishers.com や sales@NodPublishers.com などの1つの電子メールアドレスに送信された電子メールを複数のユーザーが管理できるようにする場合は、共有メールボックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6512b-114">If you want multiple people to manage email sent to a single email address like info@NodPublishers.com or sales@NodPublishers.com, create a shared mailbox.</span></span> <span data-ttu-id="6512b-115">詳細については、「[共有メールボックスを作成](create-a-shared-mailbox.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6512b-115">To learn more, see [Create a shared mailbox](create-a-shared-mailbox.md).</span></span>
  
## <a name="add-email-aliases-to-a-user"></a><span data-ttu-id="6512b-116">ユーザーにメール エイリアスを追加する</span><span class="sxs-lookup"><span data-stu-id="6512b-116">Add email aliases to a user</span></span>
<span data-ttu-id="6512b-117"><a name="AddEmailPreview"> </a></span><span class="sxs-lookup"><span data-stu-id="6512b-117"><a name="AddEmailPreview"> </a></span></span>

<span data-ttu-id="6512b-118">これを行うには、[管理者のアクセス許可](../add-users/about-admin-roles.md)が必要です。</span><span class="sxs-lookup"><span data-stu-id="6512b-118">You must have [admin permissions](../add-users/about-admin-roles.md) to do this.</span></span> 

  
::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="6512b-119">新しい Microsoft 365 管理センターを利用していない場合、[ホーム] ページの上部にある [**新しい管理センターをお試しください**] の切り替えを選択して有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6512b-119">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="6512b-120">管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">アクティブなユーザー</a>] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-120">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="6512b-121">[**アクティブなユーザー** ] ページで、[ユーザー >**メールエイリアスの管理**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-121">On the **Active Users** page, select the user > **Manage email aliases**.</span></span> <span data-ttu-id="6512b-122">ユーザーにライセンスが割り当てられていない場合、このオプションは表示されません。</span><span class="sxs-lookup"><span data-stu-id="6512b-122">You won't see this option if the person doesn't have a license assigned to them.</span></span> 
    
3. <span data-ttu-id="6512b-123">[ **+ エイリアスの追加**] を選択し、ユーザーの新しい別名を入力します。</span><span class="sxs-lookup"><span data-stu-id="6512b-123">Select **+ Add an alias** and enter a new alias for the user.</span></span>   
    
    > [!Important] 
    > <span data-ttu-id="6512b-124">"**パラメーター名 ' EmailAddresses" と一致するパラメーターが見つからない**というエラーメッセージが表示された場合は、テナントの設定が完了するまでに少し時間がかかることを意味します。または、ユーザーが最近追加した場合はカスタムドメインになります。</span><span class="sxs-lookup"><span data-stu-id="6512b-124">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="6512b-125">セットアップ プロセスが完了するには、最大 4 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="6512b-125">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="6512b-126">しばらく待ってからセットアップ処理を完了してから、もう一度実行してください。</span><span class="sxs-lookup"><span data-stu-id="6512b-126">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="6512b-127">問題が解決しない場合は、サポートにご連絡ください。サポートでは完全な同期を行います。</span><span class="sxs-lookup"><span data-stu-id="6512b-127">If the problem persists, call Support and they will do a full sync for you.</span></span>
    
  
    > [!IMPORTANT]
    > <span data-ttu-id="6512b-128">GoDaddy または別のパートナーからサブスクリプションを購入した場合、新しいエイリアスをプライマリとして設定するには、GoDaddy またはパートナーの管理コンソールに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6512b-128">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="6512b-129">メール エイリアスは、ドロップダウン リストにあるドメインで終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6512b-129">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="6512b-130">一覧に別のドメイン名を追加するには、「 [Office 365 にドメインを追加](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6512b-130">To add another domain name to the list, see [Add a domain to Office 365](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx).</span></span> 
  
     
5. <span data-ttu-id="6512b-131">完了したら、[**変更の保存**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-131">When you're done, choose **Save changes**.</span></span>
    
6. <span data-ttu-id="6512b-132">Office 365 全体に新しいエイリアスが設定されるまで 24 時間待ちます。</span><span class="sxs-lookup"><span data-stu-id="6512b-132">Wait 24 hours for the new aliases to populate throughout Office 365.</span></span>
    
    <span data-ttu-id="6512b-133">これで、ユーザーにはプライマリアドレスとエイリアスが設定されます。</span><span class="sxs-lookup"><span data-stu-id="6512b-133">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="6512b-134">たとえば、Eliza Hoffman のプライマリアドレス、Eliza@NodPublishers.com、およびエイリアス Sales@NodPublishers.com に送信されるすべてのメールは、Eliza の受信トレイに移動します。</span><span class="sxs-lookup"><span data-stu-id="6512b-134">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="6512b-135">**ユーザーが返信すると、*差出人*アドレスはプライマリ電子メールエイリアスになります。**</span><span class="sxs-lookup"><span data-stu-id="6512b-135">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="6512b-136">たとえば、メッセージが Sales@NodPublishers.com に送信され、Eliza の受信トレイに到着したとします。</span><span class="sxs-lookup"><span data-stu-id="6512b-136">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="6512b-137">Eliza がメッセージに返信する場合、Sales@NodPublishers.com ではなく、Eliza のプライマリ メール アドレスが送信者として表示されます。</span><span class="sxs-lookup"><span data-stu-id="6512b-137">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 
    
::: moniker-end

::: moniker range="o365-germany"
    
1. <span data-ttu-id="6512b-138">管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">アクティブなユーザー</a>] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-138">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span> 
    
    
2. <span data-ttu-id="6512b-139">[ **アクティブなユーザー**] ページで、編集するユーザー名を選びます。</span><span class="sxs-lookup"><span data-stu-id="6512b-139">On the **Active Users** page, select the name of the person you want to edit.</span></span>

3. <span data-ttu-id="6512b-140">[**ユーザー名/メールエイリアス**] の横にある [**編集**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-140">Next to **Username / Email Aliases**, select **Edit**.</span></span>

    > [!Important] 
    > <span data-ttu-id="6512b-141">"**パラメーター名 ' EmailAddresses" と一致するパラメーターが見つからない**というエラーメッセージが表示された場合は、テナントの設定が完了するまでに少し時間がかかることを意味します。または、ユーザーが最近追加した場合はカスタムドメインになります。</span><span class="sxs-lookup"><span data-stu-id="6512b-141">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="6512b-142">セットアップ プロセスが完了するには、最大 4 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="6512b-142">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="6512b-143">しばらく待ってからセットアップ処理を完了してから、もう一度実行してください。</span><span class="sxs-lookup"><span data-stu-id="6512b-143">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="6512b-144">問題が解決しない場合は、サポートにご連絡ください。サポートでは完全な同期を行います。</span><span class="sxs-lookup"><span data-stu-id="6512b-144">If the problem persists, call Support and they will do a full sync for you.</span></span>

4. <span data-ttu-id="6512b-145">[**エイリアス**] の下のテキストボックスに、新しい電子メールエイリアスの最初の部分を入力します。</span><span class="sxs-lookup"><span data-stu-id="6512b-145">In the text box under **Alias**, type the first part of the new email alias.</span></span> <span data-ttu-id="6512b-146">独自のドメインを Office 365 に追加した場合は、ドロップダウン リストを使って新しいメール エイリアスにそのドメインを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="6512b-146">If you added your own domain to Office 365, you can choose the domain for the new email alias by using the drop-down list.</span></span> <span data-ttu-id="6512b-147">[**追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-147">Then select **Add**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6512b-148">GoDaddy または別のパートナーからサブスクリプションを購入した場合、新しいエイリアスをプライマリとして設定するには、GoDaddy またはパートナーの管理コンソールに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6512b-148">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="6512b-149">メール エイリアスは、ドロップダウン リストにあるドメインで終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6512b-149">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="6512b-150">一覧に別のドメイン名を追加するには、「 [Office 365 にドメインを追加](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6512b-150">To add another domain name to the list, see [Add a domain to Office 365](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx).</span></span> 

5. <span data-ttu-id="6512b-151">完了したら、[**保存**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-151">When you're done, select **Save**.</span></span>

6. <span data-ttu-id="6512b-152">Office 365 全体に新しいエイリアスが設定されるまで 24 時間待ちます。</span><span class="sxs-lookup"><span data-stu-id="6512b-152">Wait 24 hours for the new aliases to populate throughout Office 365.</span></span> 
    
    <span data-ttu-id="6512b-153">これで、ユーザーにはプライマリアドレスとエイリアスが設定されます。</span><span class="sxs-lookup"><span data-stu-id="6512b-153">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="6512b-154">たとえば、Eliza Hoffman のプライマリアドレス、Eliza@NodPublishers.com、およびエイリアス Sales@NodPublishers.com に送信されるすべてのメールは、Eliza の受信トレイに移動します。</span><span class="sxs-lookup"><span data-stu-id="6512b-154">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="6512b-155">**ユーザーが返信すると、*差出人*アドレスはプライマリ電子メールエイリアスになります。**</span><span class="sxs-lookup"><span data-stu-id="6512b-155">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="6512b-156">たとえば、メッセージが Sales@NodPublishers.com に送信され、Eliza の受信トレイに到着したとします。</span><span class="sxs-lookup"><span data-stu-id="6512b-156">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="6512b-157">Eliza がメッセージに返信する場合、Sales@NodPublishers.com ではなく、Eliza のプライマリ メール アドレスが送信者として表示されます。</span><span class="sxs-lookup"><span data-stu-id="6512b-157">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="6512b-158">管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">アクティブなユーザー</a>] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-158">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

    
2. <span data-ttu-id="6512b-159">[ **アクティブなユーザー**] ページで、編集するユーザー名を選びます。</span><span class="sxs-lookup"><span data-stu-id="6512b-159">On the **Active Users** page, select the name of the person you want to edit.</span></span>

3. <span data-ttu-id="6512b-160">[**ユーザー名/メールエイリアス**] の横にある [**編集**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-160">Next to **Username / Email Aliases**, select **Edit**.</span></span>

    > [!Important] 
    > <span data-ttu-id="6512b-161">"**パラメーター名 ' EmailAddresses" と一致するパラメーターが見つからない**というエラーメッセージが表示された場合は、テナントの設定が完了するまでに少し時間がかかることを意味します。または、ユーザーが最近追加した場合はカスタムドメインになります。</span><span class="sxs-lookup"><span data-stu-id="6512b-161">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="6512b-162">セットアップ プロセスが完了するには、最大 4 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="6512b-162">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="6512b-163">しばらく待ってからセットアップ処理を完了してから、もう一度実行してください。</span><span class="sxs-lookup"><span data-stu-id="6512b-163">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="6512b-164">問題が解決しない場合は、サポートにご連絡ください。サポートでは完全な同期を行います。</span><span class="sxs-lookup"><span data-stu-id="6512b-164">If the problem persists, call Support and they will do a full sync for you.</span></span>

4. <span data-ttu-id="6512b-165">[**エイリアス**] の下のテキストボックスに、新しい電子メールエイリアスの最初の部分を入力します。</span><span class="sxs-lookup"><span data-stu-id="6512b-165">In the text box under **Alias**, type the first part of the new email alias.</span></span> <span data-ttu-id="6512b-166">独自のドメインを Office 365 に追加した場合は、ドロップダウン リストを使って新しいメール エイリアスにそのドメインを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="6512b-166">If you added your own domain to Office 365, you can choose the domain for the new email alias by using the drop-down list.</span></span> <span data-ttu-id="6512b-167">[**追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-167">Then select **Add**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6512b-168">GoDaddy または別のパートナーからサブスクリプションを購入した場合、新しいエイリアスをプライマリとして設定するには、GoDaddy またはパートナーの管理コンソールに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6512b-168">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="6512b-169">メール エイリアスは、ドロップダウン リストにあるドメインで終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6512b-169">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="6512b-170">一覧に別のドメイン名を追加するには、「 [Office 365 にドメインを追加](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6512b-170">To add another domain name to the list, see [Add a domain to Office 365](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx).</span></span> 

5. <span data-ttu-id="6512b-171">完了したら、[**保存**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6512b-171">When you're done, select **Save**.</span></span>

6. <span data-ttu-id="6512b-172">Office 365 全体に新しいエイリアスが設定されるまで 24 時間待ちます。</span><span class="sxs-lookup"><span data-stu-id="6512b-172">Wait 24 hours for the new aliases to populate throughout Office 365.</span></span> 
    
    <span data-ttu-id="6512b-173">これで、ユーザーにはプライマリアドレスとエイリアスが設定されます。</span><span class="sxs-lookup"><span data-stu-id="6512b-173">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="6512b-174">たとえば、Eliza Hoffman のプライマリアドレス、Eliza@NodPublishers.com、およびエイリアス Sales@NodPublishers.com に送信されるすべてのメールは、Eliza の受信トレイに移動します。</span><span class="sxs-lookup"><span data-stu-id="6512b-174">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="6512b-175">**ユーザーが返信すると、*差出人*アドレスはプライマリ電子メールエイリアスになります。**</span><span class="sxs-lookup"><span data-stu-id="6512b-175">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="6512b-176">たとえば、メッセージが Sales@NodPublishers.com に送信され、Eliza の受信トレイに到着したとします。</span><span class="sxs-lookup"><span data-stu-id="6512b-176">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="6512b-177">Eliza がメッセージに返信する場合、Sales@NodPublishers.com ではなく、Eliza のプライマリ メール アドレスが送信者として表示されます。</span><span class="sxs-lookup"><span data-stu-id="6512b-177">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 

::: moniker-end


## <a name="did-you-get-a-parameter-cannot-be-found-that-matches-parameter-name-emailaddresses"></a><span data-ttu-id="6512b-178">"パラメーター名 EmailAddresses に一致するパラメーターが見つかりません" が表示されましたか?</span><span class="sxs-lookup"><span data-stu-id="6512b-178">Did you get "A parameter cannot be found that matches parameter name EmailAddresses"?</span></span>


<span data-ttu-id="6512b-179">"**パラメーター名が電子メールアドレスに一致するパラメーターが見つかりません**" というエラーメッセージが表示された場合は、テナントの設定が完了するまでに少し時間がかかっていること、または、ユーザーが最近追加された場合はカスタムドメインを使用していることを意味します。</span><span class="sxs-lookup"><span data-stu-id="6512b-179">If you get the error message "**A parameter cannot be found that matches parameter name EmailAddresses**" it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="6512b-180">セットアップ プロセスが完了するには、最大 4 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="6512b-180">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="6512b-181">しばらく待ってからセットアップ処理を完了してから、もう一度実行してください。</span><span class="sxs-lookup"><span data-stu-id="6512b-181">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="6512b-182">問題が解決しない場合は、サポートにご連絡ください。サポートでは完全な同期を行います。</span><span class="sxs-lookup"><span data-stu-id="6512b-182">If the problem persists, call Support and they will do a full sync for you.</span></span>
  
## <a name="did-you-purchase-your-subscription-from-godaddy-or-another-partner"></a><span data-ttu-id="6512b-183">GoDaddy または別のパートナーからサブスクリプションを購入した場合</span><span class="sxs-lookup"><span data-stu-id="6512b-183">Did you purchase your subscription from GoDaddy or another Partner?</span></span>


<span data-ttu-id="6512b-184">GoDaddy または別のパートナーからサブスクリプションを購入した場合、新しいエイリアスをプライマリとして設定するには、GoDaddy またはパートナーの管理コンソールに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6512b-184">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span>
  
## <a name="related-articles"></a><span data-ttu-id="6512b-185">関連記事</span><span class="sxs-lookup"><span data-stu-id="6512b-185">Related articles</span></span>

[<span data-ttu-id="6512b-186">別のアドレスからメールを送信する</span><span class="sxs-lookup"><span data-stu-id="6512b-186">Send email from a different address</span></span>](https://support.office.com/article/ccba89cb-141c-4a36-8c56-6d16a8556d2e.aspx)

[<span data-ttu-id="6512b-187">ユーザー名とメール アドレスを変更する</span><span class="sxs-lookup"><span data-stu-id="6512b-187">Change a user name and email address</span></span>](../add-users/change-a-user-name-and-email-address.md)
  
