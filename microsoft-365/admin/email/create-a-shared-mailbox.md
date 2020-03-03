---
title: 共有メールボックスを作成する
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 871a246d-3acd-4bba-948e-5de8be0544c9
description: 共有メールボックスを作成すると、社内の複数のユーザーが 1 つのメール アドレスに送付されたメールを閲覧したり、回答したりできます。
ms.openlocfilehash: 2ceec37928eafab0c4f02382dd24aa3fa91aa9cd
ms.sourcegitcommit: 812aab5f58eed4bf359faf0e99f7f876af5b1023
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/02/2020
ms.locfileid: "42362302"
---
# <a name="create-a-shared-mailbox"></a><span data-ttu-id="56932-103">共有メールボックスを作成する</span><span class="sxs-lookup"><span data-stu-id="56932-103">Create a shared mailbox</span></span> 

> [!NOTE]
> <span data-ttu-id="56932-104">組織でハイブリッド Exchange 環境を使用する場合は、オンプレミスの Exchange 管理センター (EAC) を使用して、共有メールボックスを作成および管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="56932-104">If your organization uses a hybrid Exchange environment, you should use the on-premises Exchange admin center (EAC) to create and manage shared mailboxes.</span></span> <span data-ttu-id="56932-105">「[Exchange 管理センターで共有メールボックスを作成する](https://docs.microsoft.com/Exchange/collaboration/shared-mailboxes/create-shared-mailboxes?view=exchserver-2019.)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56932-105">See [Create shared mailboxes in the Exchange admin center](https://docs.microsoft.com/Exchange/collaboration/shared-mailboxes/create-shared-mailboxes?view=exchserver-2019.)</span></span><br><br>
> <span data-ttu-id="56932-106">共有メールボックスと Outlook 用 Office 365 グループのどちらを作成すればよいかわからない場合は、「[グループを比較する](../create-groups/compare-groups.md)」のガイダンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="56932-106">If you're not sure if you should create a shared mailbox or an Office 365 Group for Outlook, see [Compare groups](../create-groups/compare-groups.md) for some guidance.</span></span> <span data-ttu-id="56932-107">現在、共有メールボックスを Office 365 グループに移行することはできません。</span><span class="sxs-lookup"><span data-stu-id="56932-107">Note that currently, it's not possible to migrate a shared mailbox to an Office 365 Group.</span></span> <span data-ttu-id="56932-108">この機能をご希望の場合は、[こちらから投票](https://go.microsoft.com/fwlink/?linkid=871518)してお知らせください。</span><span class="sxs-lookup"><span data-stu-id="56932-108">If this is something you want, let us know by [voting here](https://go.microsoft.com/fwlink/?linkid=871518).</span></span>

<span data-ttu-id="56932-p103">共有メールボックスの作成は簡単なので、ユーザーのグループが共通のメール アドレス (info@contoso.com など) を監視して、そこからメールを送信することができます。共有メールボックスに送信されたメッセージにグループのユーザーが返信すると、そのメールは、個別のユーザーからではなく共有メールボックスから送信されたように表示されます。</span><span class="sxs-lookup"><span data-stu-id="56932-p103">It's easy to create shared mailboxes so a group of people can monitor and send email from a common email addresses, like info@contoso.com. When a person in the group replies to a message sent to the shared mailbox, the email appears to be from the shared mailbox, not from the individual user.</span></span>

<span data-ttu-id="56932-111">共有メールボックスには共有の予定表も含まれています。</span><span class="sxs-lookup"><span data-stu-id="56932-111">Shared mailboxes include a shared calendar.</span></span> <span data-ttu-id="56932-112">全員が予定を入力できる場所として共有の予定表を利用したい小規模な企業は多数あります。</span><span class="sxs-lookup"><span data-stu-id="56932-112">A lot of small businesses like to use the shared calendar as a place for everyone to enter their appointments.</span></span> <span data-ttu-id="56932-113">たとえば、客先に訪問する社員が 3 人いる場合、全員で共有の予定表を使用して予定を入力できます。</span><span class="sxs-lookup"><span data-stu-id="56932-113">For example, if you have 3 people who do customer visits, all can use the shared calendar to enter the appointments.</span></span> <span data-ttu-id="56932-114">これで、誰がどこにいるのかが常にわかるようになります。</span><span class="sxs-lookup"><span data-stu-id="56932-114">This is an easy way to keep everyone informed where people are.</span></span>

<span data-ttu-id="56932-115">共有メールボックスを作成する前に、「[共有メールボックスについて](about-shared-mailboxes.md)」を読んで詳細をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="56932-115">Before creating a shared mailbox, be sure to read [About shared mailboxes](about-shared-mailboxes.md) for more information.</span></span>

## <a name="create-a-shared-mailbox-and-add-members"></a><span data-ttu-id="56932-116">共有メールボックスを作成し、メンバーを追加する</span><span class="sxs-lookup"><span data-stu-id="56932-116">Create a shared mailbox and add members</span></span>
  
1. <span data-ttu-id="56932-117">Office 365 のグローバル管理者アカウント、または Exchange の管理者アカウントでサインインします。</span><span class="sxs-lookup"><span data-stu-id="56932-117">Sign in with an Office 365 global admin account or Exchange admin account.</span></span> <span data-ttu-id="56932-118">"**このページへのアクセス許可がないため、この操作を実行できません**" というメッセージが表示される場合、そのユーザーは管理者ではありません。</span><span class="sxs-lookup"><span data-stu-id="56932-118">If you get the message "**You don't have permission to access this page or perform this action**," then you aren't an admin.</span></span> 

::: moniker range="o365-worldwide"

2. <span data-ttu-id="56932-119">管理センターで、**[グループ]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">[共有メールボックス]</a> ページの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="56932-119">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

2. <span data-ttu-id="56932-120">[[管理センター]](https://go.microsoft.com/fwlink/p/?linkid=848041) で、**[グループ]** \> **[共有メールボックス]** ページの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="56932-120">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=848041), go to the **Groups** \> **Shared mailboxes** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

2. <span data-ttu-id="56932-121">[[管理センター]](https://go.microsoft.com/fwlink/p/?linkid=850627) で、**[グループ]** \> **[共有メールボックス]** ページの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="56932-121">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=850627), go to the **Groups** \> **Shared mailboxes** page.</span></span>

::: moniker-end
    
3. <span data-ttu-id="56932-122">**[共有メールボックス]** ページで、**[+ メールボックスの追加]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-122">On the **Shared mailboxes** page, select **+ Add a mailbox**.</span></span> <span data-ttu-id="56932-123">共有メールボックスの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="56932-123">Enter a name for the shared mailbox.</span></span> <span data-ttu-id="56932-124">その後、ウィザードでメール アドレスが選ばれますが、自分で編集することができます。</span><span class="sxs-lookup"><span data-stu-id="56932-124">Then the wizard chooses the email address, but you can edit it.</span></span>
    
    ![共有メールボックスに名前を付けます。](../../media/e3035132-8986-4ec7-b7c0-f2752080d2c0.png)
  
4. <span data-ttu-id="56932-126">**[追加]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-126">Select **Add**.</span></span> <span data-ttu-id="56932-127">メンバーを追加できるようになるまで、数分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="56932-127">It may take a few minutes before you can add members.</span></span>

5. <span data-ttu-id="56932-128">**[次のステップ]** で、**[このメールボックスにメンバーを追加する]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-128">Under **Next steps**, select **Add members to this mailbox**.</span></span> <span data-ttu-id="56932-129">メンバーは、この共有メールボックスへの受信メールと送信した返信を表示できるようになります。</span><span class="sxs-lookup"><span data-stu-id="56932-129">Members are the people who will be able to view the incoming mail to this shared mailbox, and the outgoing replies.</span></span>

   ![[メンバーの追加] を選択する](../../media/a2a72e3d-6170-40fe-a94f-0af8fbef8ab2.png)

6. <span data-ttu-id="56932-131">**[+ メンバーの追加]** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-131">Select the **+Add members** button.</span></span> <span data-ttu-id="56932-132">この共有メールボックスの使用を許可するユーザーをクリックしてチェック マークを付け、**[保存]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-132">Put a check mark next to the people who you want to use this shared mailbox, and select **Save**.</span></span>

   ![共有メールボックスにメンバーを割り当てる](../../media/e6c58953-f6d7-4f0b-97ba-308516bf2a94.png)

7. <span data-ttu-id="56932-134">**[閉じる]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-134">Select **Close**.</span></span>

<span data-ttu-id="56932-135">これで共有メールボックスを作成できました。共有の予定表も含まれています。</span><span class="sxs-lookup"><span data-stu-id="56932-135">You have a shared mailbox and it includes a shared calendar.</span></span> <span data-ttu-id="56932-136">次の手順として、「共有メールボックス アカウントのサインインをブロックする」に進みます。</span><span class="sxs-lookup"><span data-stu-id="56932-136">Now go on to the next step: block sign-in for the shared mailbox account.</span></span>

## <a name="block-sign-in-for-the-shared-mailbox-account"></a><span data-ttu-id="56932-137">共有メールボックス アカウントのサインインをブロックする</span><span class="sxs-lookup"><span data-stu-id="56932-137">Block sign-in for the shared mailbox account</span></span>

<span data-ttu-id="56932-138">どの共有メールボックスにも、対応するユーザー アカウントがあります。</span><span class="sxs-lookup"><span data-stu-id="56932-138">Every shared mailbox has a corresponding user account.</span></span> <span data-ttu-id="56932-139">共有メールボックスを作成する際に、パスワードの入力を求められなかったことにご注意ください。</span><span class="sxs-lookup"><span data-stu-id="56932-139">Notice how you weren't asked to provide a password when you created the shared mailbox?</span></span> <span data-ttu-id="56932-140">このアカウントにはパスワードが設定されていますが、そのパスワードはシステムで生成され、ユーザーにはわかりません。</span><span class="sxs-lookup"><span data-stu-id="56932-140">The account has a password, but it's system-generated (unknown).</span></span> <span data-ttu-id="56932-141">ユーザーは、そのアカウントを使用して共有メールボックスにログインする訳ではありません。</span><span class="sxs-lookup"><span data-stu-id="56932-141">You aren't supposed to use the account to log in to the shared mailbox.</span></span>

<span data-ttu-id="56932-142">では、管理者が共有メールボックスのユーザー アカウントのパスワードをリセットした場合はどうなりますか。</span><span class="sxs-lookup"><span data-stu-id="56932-142">But what if an admin simply resets the password of the shared mailbox user account?</span></span> <span data-ttu-id="56932-143">また、攻撃者がその共有メールボックス アカウントの資格情報にアクセスできるようになった場合はどうなるでしょうか。</span><span class="sxs-lookup"><span data-stu-id="56932-143">Or what if an attacker gains access to the shared mailbox account credentials?</span></span> <span data-ttu-id="56932-144">そうなれば、そのユーザー アカウントで共有メールボックスにログインして、メールを送信することが可能になってしまいます。</span><span class="sxs-lookup"><span data-stu-id="56932-144">This would allow the user account to log in to the shared mailbox and send email.</span></span> <span data-ttu-id="56932-145">これを防ぐために、この共有メールボックスに関連付けられているアカウントのサインインをブロックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="56932-145">To prevent this, you need to block sign-in for the account that's associated with the shared mailbox.</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="56932-146">新しい Microsoft 365 管理センターを利用していない場合、[ホーム] ページの上部にある [**新しい管理センターをお試しください**] の切り替えを選択して有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="56932-146">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="56932-147">管理センターで、[**ユーザー**] \> [<a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">アクティブなユーザー</a>] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-147">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="56932-148">ユーザー アカウントの一覧から、共有メールボックスのアカウントを探します (例: フィルターを **[ライセンス未付与のユーザー]** に変更する)。</span><span class="sxs-lookup"><span data-stu-id="56932-148">In the list of user accounts, find the account for the shared mailbox (for example, change the filter to **Unlicensed users**).</span></span>

3. <span data-ttu-id="56932-149">そのユーザーを選択してプロパティ ウィンドウを開き、**[このユーザーをブロックする]** アイコンを選択します ![[このユーザーをブロックする] アイコンのスクリーンショット](../../media/block-user-icon.png)。</span><span class="sxs-lookup"><span data-stu-id="56932-149">Select the user to open their properties pane, and then select the **Block this user** icon ![Screen shot of the Block this user icon](../../media/block-user-icon.png).</span></span>

   <span data-ttu-id="56932-150">**注**: アカウントが既にブロックされている場合、上部に **[サインインはブロック済み]** と表示され、アイコンは **[このユーザーのブロックを解除する]** になります。</span><span class="sxs-lookup"><span data-stu-id="56932-150">**Note**: If the account is already blocked, **Sign in blocked** will appear at the top and the icon will read **Unblock this user**.</span></span>

4. <span data-ttu-id="56932-151">**[このユーザーをブロックしますか?]** ウィンドウで、**[このユーザーのサインインをブロックする]** を選択し、**[変更の保存]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-151">In the **Block this user?** pane, select **Block the user from signing in**, and then select **Save changes**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="56932-152">管理センターで、**[ユーザー]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">[アクティブなユーザー]</a> ページの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="56932-152">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="56932-153">ユーザー アカウントの一覧から、共有メールボックスのアカウントを探し (例: 表示を **[ライセンス未付与のユーザー]** に変更する)、そのアカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-153">In the list of user accounts, find the account for the shared mailbox (for example, change the view to **Unlicensed users**) and then select the account.</span></span>

3. <span data-ttu-id="56932-154">[プロパティ] ポップアップで、**[サインインをブロックする]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-154">In the properties flyout, select **Block sign-in**.</span></span>

    <span data-ttu-id="56932-155">**注:** アカウントが既にブロックされている場合、ボタンは **[サインインのブロックを解除する]** になります。</span><span class="sxs-lookup"><span data-stu-id="56932-155">**Note:** If the account was already blocked, the button would say **Unblock sign-in**.</span></span>

4. <span data-ttu-id="56932-156">**[サインイン状態を編集する]** ポップアップで、[このユーザーのサインインをブロックする] が選択されていることを確認し、**[保存]**、**[閉じる]** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-156">In the **Edit sign-in status** flyout, verify that Block the user from signing in is selected, select **Save** and then **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="56932-157">管理センターで、**[ユーザー]** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">[アクティブなユーザー]</a> ページの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="56932-157">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="56932-158">ユーザー アカウントの一覧から、共有メールボックスのアカウントを探し (例: 表示を **[ライセンス未付与のユーザー]** に変更する)、そのアカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-158">In the list of user accounts, find the account for the shared mailbox (for example, change the view to **Unlicensed users**) and then select the account.</span></span>

3. <span data-ttu-id="56932-159">[プロパティ] ポップアップで、**[サインインをブロックする]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-159">In the properties flyout, select **Block sign-in**.</span></span>

    <span data-ttu-id="56932-160">**注:** アカウントが既にブロックされている場合、ボタンは **[サインインのブロックを解除する]** になります。</span><span class="sxs-lookup"><span data-stu-id="56932-160">**Note:** If the account was already blocked, the button would say **Unblock sign-in**.</span></span>

4. <span data-ttu-id="56932-161">**[サインイン状態を編集する]** ポップアップで、[このユーザーのサインインをブロックする] が選択されていることを確認し、**[保存]**、**[閉じる]** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-161">In the **Edit sign-in status** flyout, verify that Block the user from signing in is selected, select **Save** and then **Close**.</span></span>
::: moniker-end

<span data-ttu-id="56932-162">Azure AD PowerShell を使用してアカウントのサインインをブロックする方法 (同時に多数のアカウントをブロックする方法など) の詳細については、「[Office 365 PowerShell でユーザー アカウントをブロックする](https://docs.microsoft.com/office365/enterprise/powershell/block-user-accounts-with-office-365-powershell)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56932-162">For instructions on how to block sign-in for accounts using Azure AD PowerShell (including many accounts at the same time), see [Block user accounts with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/block-user-accounts-with-office-365-powershell).</span></span>

## <a name="add-the-shared-mailbox-to-outlook"></a><span data-ttu-id="56932-163">共有メールボックスを Outlook に追加する</span><span class="sxs-lookup"><span data-stu-id="56932-163">Add the shared mailbox to Outlook</span></span>

<span data-ttu-id="56932-164">お客様の職場で自動マッピングを有効にしている場合 (既定では、ほとんどのユーザーが有効にします)、共有メールボックスは、ユーザーが Outlook を閉じて再起動した後にユーザーの Outlook アプリに自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="56932-164">If you have automapping enabled in your business (by default, most people do), the shared mailbox will appear in your user's Outlook app automatically after they close and restart Outlook.</span></span> 

<span data-ttu-id="56932-165">自動マッピングはユーザーのメールボックスに設定されますが、共有メールボックスには設定されません。  </span><span class="sxs-lookup"><span data-stu-id="56932-165">Automapping is set on the user's mailbox, not the shared mailbox.</span></span> <span data-ttu-id="56932-166">つまり、セキュリティ グループを使用して、共有メールボックスへのアクセス権を持つユーザーを管理する場合、自動マッピングは機能しません。</span><span class="sxs-lookup"><span data-stu-id="56932-166">This means if you try to use a security group to manage who has access to the shared mailbox, automapping won't work.</span></span> <span data-ttu-id="56932-167">そのため、自動マッピングが必要な場合は、明示的にアクセス許可を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="56932-167">So, if you want automapping, you have to assign permissions explicitly.</span></span> <span data-ttu-id="56932-168">自動マッピングは既定でオンになっています。</span><span class="sxs-lookup"><span data-stu-id="56932-168">Automapping is on by default.</span></span> <span data-ttu-id="56932-169">この機能をオフにする方法については、「[Outlook for Office 365 で共有メールボックスの自動マッピングを削除する方法](https://docs.microsoft.com/office365/troubleshoot/administration/remove-automapping-for-shared-mailbox)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56932-169">To learn how to turn it off, see [Remove automapping for a shared mailbox](https://docs.microsoft.com/office365/troubleshoot/administration/remove-automapping-for-shared-mailbox).</span></span>

<span data-ttu-id="56932-170">Outlook の共有メールボックスの詳細については、次を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56932-170">To learn more about shared mailboxes in Outlook, see:</span></span>

- <span data-ttu-id="56932-171"><a href="https://support.office.com/article/d94a8e9e-21f1-4240-808b-de9c9c088afd.aspx" target="_blank">Outlook で共有メールボックスを開いて使用する</a></span><span class="sxs-lookup"><span data-stu-id="56932-171"><a href="https://support.office.com/article/d94a8e9e-21f1-4240-808b-de9c9c088afd.aspx" target="_blank">Open and use a shared mailbox in Outlook</a></span></span>

- <span data-ttu-id="56932-172"><a href="https://support.office.com/article/98b5a90d-4e38-415d-a030-f09a4cd28207.aspx" target="_blank">共有メールボックスを Outlook on the web に追加する</a></span><span class="sxs-lookup"><span data-stu-id="56932-172"><a href="https://support.office.com/article/98b5a90d-4e38-415d-a030-f09a4cd28207.aspx" target="_blank">Add a shared mailbox to Outlook on the web</a></span></span>

- <span data-ttu-id="56932-173"><a href="https://support.office.com/article/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Outlook Mobile に共有メールボックスを追加する</a></span><span class="sxs-lookup"><span data-stu-id="56932-173"><a href="https://support.office.com/article/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Add a shared mailbox to Outlook mobile</a></span></span>

- <span data-ttu-id="56932-174"><a href="https://support.office.com/article/6ecc39c5-5577-4a1d-b18c-bbdc92972cb2.aspx" target="_blank">Outlook for Mac で共有フォルダーまたはメールボックスを開く</a></span><span class="sxs-lookup"><span data-stu-id="56932-174"><a href="https://support.office.com/article/6ecc39c5-5577-4a1d-b18c-bbdc92972cb2.aspx" target="_blank">Open a shared folder or mailbox in Outlook for Mac</a></span></span>

- <span data-ttu-id="56932-175"><a href="https://support.office.com/article/b0963400-2a51-4c64-afc7-b816d737d164.aspx" target="_blank">共有メールボックスにルールを追加する</a></span><span class="sxs-lookup"><span data-stu-id="56932-175"><a href="https://support.office.com/article/b0963400-2a51-4c64-afc7-b816d737d164.aspx" target="_blank">Add rules to a shared mailbox</a></span></span>


## <a name="use-a-shared-mailbox-on-a-mobile-device-phone-or-tablet"></a><span data-ttu-id="56932-176">モバイル デバイス (スマートフォンまたはタブレット) で共有メールボックスを使用する</span><span class="sxs-lookup"><span data-stu-id="56932-176">Use a shared mailbox on a mobile device (phone or tablet)</span></span>

<span data-ttu-id="56932-177">モバイル デバイスでは、次の 2 つの方法で共有メールボックスにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="56932-177">You can access a shared mailbox on a mobile device in two ways:</span></span>
- <span data-ttu-id="56932-178">共有メールボックスを <a href="https://apps.apple.com/us/app/microsoft-outlook/id951937596" target="_blank">Outlook for iOS アプリ</a>、または <a href="https://play.google.com/store/apps/details?id=com.microsoft.office.outlook&hl=en_US" target="_blank">Outlook for Android モバイル アプリ</a>に追加する。</span><span class="sxs-lookup"><span data-stu-id="56932-178">Add the shared mailbox in the <a href="https://apps.apple.com/us/app/microsoft-outlook/id951937596" target="_blank">Outlook for iOS app</a> or the <a href="https://play.google.com/store/apps/details?id=com.microsoft.office.outlook&hl=en_US" target="_blank">Outlook for Android mobile app</a>.</span></span> 
    
    <span data-ttu-id="56932-179">手順については、「<a href="https://support.office.com/article/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Outlook Mobile に共有メールボックスを追加する</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56932-179">For instructions, see <a href="https://support.office.com/article/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Add a shared mailbox to Outlook mobile</a>.</span></span>

- <span data-ttu-id="56932-180">ブラウザーを開いて Office 365 にサインインし、Outlook on the web に移動する。</span><span class="sxs-lookup"><span data-stu-id="56932-180">Open your browser, sign in to Office 365, and then go to Outlook on the web.</span></span> <span data-ttu-id="56932-181">Outlook on the web から、共有メールボックスにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="56932-181">From Outlook on the web you'll be able to access the shared mailbox.</span></span>

    <span data-ttu-id="56932-182">手順については、「<a href="https://support.office.com/article/98b5a90d-4e38-415d-a030-f09a4cd28207.aspx" target="_blank">共有メールボックスを Outlook on the web に追加する</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56932-182">For instructions, see <a href="https://support.office.com/article/98b5a90d-4e38-415d-a030-f09a4cd28207.aspx" target="_blank">Add a shared mailbox to Outlook on the web</a>.</span></span>

## <a name="use-the-shared-calendar"></a><span data-ttu-id="56932-183">共有の予定表を使う</span><span class="sxs-lookup"><span data-stu-id="56932-183">Use the shared calendar</span></span>

<span data-ttu-id="56932-184">共有メールボックスを作成すると、共有の予定表が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="56932-184">When you created the shared mailbox, you automatically created a shared calendar.</span></span> <span data-ttu-id="56932-185">共有メールボックスの予定表は SharePoint の予定表に比べて、予定や他の人の場所を把握するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="56932-185">We like the shared mailbox calendar rather than a SharePoint calendar for keeping track of appointments and where people are.</span></span> <span data-ttu-id="56932-186">共有の予定表は Outlook と統合されており、SharePoint の予定表よりずっと簡単に使用できます。</span><span class="sxs-lookup"><span data-stu-id="56932-186">A shared calendar is integrated with Outlook and it's much easier to use than a SharePoint calendar.</span></span>

1. <span data-ttu-id="56932-187">Outlook アプリで予定表ビューに移動し、共有メールボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="56932-187">In the Outlook app, go to calendar view, and select the shared mailbox.</span></span>

2. <span data-ttu-id="56932-188">予定を入力すると、共有メールボックスのメンバー全員がその予定を表示できます。</span><span class="sxs-lookup"><span data-stu-id="56932-188">When you enter appointments, everyone who is a member of the shared mailbox will be able to see them.</span></span>

3. <span data-ttu-id="56932-189">共有メールボックスのすべてのメンバーは、予定表での予定の作成、表示、および管理を、個人的な予定の場合と同様に行えます。</span><span class="sxs-lookup"><span data-stu-id="56932-189">Any member of the shared mailbox can create, view, and manage appointments on the calendar, just like they would their personal appointments.</span></span> <span data-ttu-id="56932-190">共有メールボックスのメンバーになっているすべてのユーザーは、共有の予定表に加えられた変更を確認できます。</span><span class="sxs-lookup"><span data-stu-id="56932-190">Everyone who is a member of shared mailbox can see their changes to the shared calendar.</span></span>

## <a name="related-articles"></a><span data-ttu-id="56932-191">関連記事</span><span class="sxs-lookup"><span data-stu-id="56932-191">Related articles</span></span>

[<span data-ttu-id="56932-192">共有メールボックスについて</span><span class="sxs-lookup"><span data-stu-id="56932-192">About shared mailboxes</span></span>](about-shared-mailboxes.md)

[<span data-ttu-id="56932-193">共有メールボックスを構成する</span><span class="sxs-lookup"><span data-stu-id="56932-193">Configure a shared mailbox</span></span>](configure-a-shared-mailbox.md)

[<span data-ttu-id="56932-194">ユーザー メールボックスを共有メールボックスに変換する</span><span class="sxs-lookup"><span data-stu-id="56932-194">Convert a user mailbox to a shared mailbox</span></span>](convert-user-mailbox-to-shared-mailbox.md)

[<span data-ttu-id="56932-195">共有メールボックスからライセンスを削除する</span><span class="sxs-lookup"><span data-stu-id="56932-195">Remove a license from a shared mailbox</span></span>](remove-license-from-shared-mailbox.md)

[<span data-ttu-id="56932-196">共有メールボックスの問題を解決する</span><span class="sxs-lookup"><span data-stu-id="56932-196">Resolve issues with shared mailboxes</span></span>](resolve-issues-with-shared-mailboxes.md)




