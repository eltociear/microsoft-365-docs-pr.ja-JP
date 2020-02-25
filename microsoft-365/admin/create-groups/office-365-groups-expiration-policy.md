---
title: Office 365 グループの有効期限ポリシー
ms.reviewer: arvaradh
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
description: Office 365 グループの有効期限ポリシーについて説明します。
ms.openlocfilehash: 5a7a9f9a67e8436a8d4120551e306a68a015bcb9
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/24/2020
ms.locfileid: "42241326"
---
# <a name="office-365-group-expiration-policy"></a><span data-ttu-id="3544c-103">Office 365 グループの有効期限ポリシー</span><span class="sxs-lookup"><span data-stu-id="3544c-103">Office 365 Group Expiration Policy</span></span>

<span data-ttu-id="3544c-104">Office 365 グループの使用率が向上したことで、管理者とユーザーは、未使用のグループをクリーンアップする方法が必要になります。</span><span class="sxs-lookup"><span data-stu-id="3544c-104">With the increase in usage of Office 365 Groups, administrators and users need a way to clean up unused groups.</span></span> <span data-ttu-id="3544c-105">有効期限ポリシーは、非アクティブなグループをシステムから削除して、クリーナーを作成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3544c-105">Expiration policies can help remove inactive groups from the system and make things cleaner.</span></span>

<span data-ttu-id="3544c-106">グループの有効期限が切れると、関連付けられているすべてのサービス (メールボックス、プランナー、SharePoint サイトなど) も削除されます。</span><span class="sxs-lookup"><span data-stu-id="3544c-106">When a group expires, all of its associated services (the mailbox, Planner, SharePoint site, etc.) are also deleted.</span></span>

<span data-ttu-id="3544c-107">グループの有効期限が切れた場合、"削除済み" となることを意味します。これは、最大30日間復旧できます。</span><span class="sxs-lookup"><span data-stu-id="3544c-107">When a group expires it is "soft-deleted" which means it can still be recovered for up to 30 days.</span></span>

<span data-ttu-id="3544c-108">管理者は、有効期限を指定して、その期間の最後に到達し、更新されていないアクティブなグループを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3544c-108">Administrators can specify an expiration period and any inactive group that reaches the end of that period, and is not renewed, will be deleted.</span></span> <span data-ttu-id="3544c-109">有効期限は、グループが作成された時点、または最後に更新された日付から始まります。</span><span class="sxs-lookup"><span data-stu-id="3544c-109">The expiration period begins when the group is created, or on the date it was last renewed.</span></span> <span data-ttu-id="3544c-110">グループの所有者は、有効期限が切れる前に、別の有効期限が切れるまでグループを更新できるように、メールを自動的に送信します。</span><span class="sxs-lookup"><span data-stu-id="3544c-110">Group owners will automatically be sent an email before the expiration that allows them to renew the group for another expiration interval.</span></span> <span data-ttu-id="3544c-111">Teams ユーザーには、Teams で永続的な通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3544c-111">Teams users will see persistent notifications in Teams.</span></span>

<span data-ttu-id="3544c-112">アクティブに使用されているグループは自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3544c-112">Groups that are actively in use are renewed automatically.</span></span> <span data-ttu-id="3544c-113">次のいずれかのアクションを実行すると、グループが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3544c-113">Any of the following actions will auto-renew a group:</span></span>
- <span data-ttu-id="3544c-114">SharePoint-ファイルの表示、編集、ダウンロード、移動、共有、またはアップロードを行います。</span><span class="sxs-lookup"><span data-stu-id="3544c-114">SharePoint - view, edit, download, move, share, or upload files.</span></span>
- <span data-ttu-id="3544c-115">Outlook-グループのメッセージと同じように、グループからのメッセージの読み取りまたは書き込み。メッセージ (web 上の Outlook)。</span><span class="sxs-lookup"><span data-stu-id="3544c-115">Outlook - join group, read or write group message from the group, and like a message (Outlook on the web).</span></span>
- <span data-ttu-id="3544c-116">Teams チャネルを訪れます。</span><span class="sxs-lookup"><span data-stu-id="3544c-116">Teams - visiting a teams channel.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3544c-p104">有効期限ポリシーを変更すると、サービスによって各グループの有効期限が再計算されます。常にグループの作成日からカウントされます。その後で新しい有効期限ポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="3544c-p104">When you change the expiration policy, the service recalculates the expiration date for each group. It always starts counting from the date when the group was created, and then applies the new expiration policy.</span></span>

<span data-ttu-id="3544c-119">既定では、有効期限はオフになっていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3544c-119">It's important to know that expiration is turned off by default.</span></span> <span data-ttu-id="3544c-120">この機能を使用する場合は、管理者がテナントに対して有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3544c-120">Administrators will have to enable it for their tenant if they want to use it.</span></span>

> [!NOTE]
> <span data-ttu-id="3544c-121">Office 365 グループの有効期限ポリシーを構成して使用するには、その有効期限ポリシーが適用されているすべてのグループのメンバーに対して、必ずしも Azure AD Premium ライセンスを割り当てる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3544c-121">Configuring and using the expiration policy for Office 365 groups requires you to possess but not necessarily assign Azure AD Premium licenses for the members of all groups to which the expiration policy is applied.</span></span> <span data-ttu-id="3544c-122">詳細については、「 [Azure Active Directory Premium の](https://docs.microsoft.com/azure/active-directory/active-directory-get-started-premium)概要」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3544c-122">For more information see [Getting started with Azure Active Directory Premium](https://docs.microsoft.com/azure/active-directory/active-directory-get-started-premium).</span></span>

## <a name="who-can-configure-and-use-the-office-365-groups-expiration-policy"></a><span data-ttu-id="3544c-123">Office 365 グループの有効期限ポリシーを構成して使用できるユーザー</span><span class="sxs-lookup"><span data-stu-id="3544c-123">Who can configure and use the Office 365 Groups expiration policy?</span></span>

|<span data-ttu-id="3544c-124">Role</span><span class="sxs-lookup"><span data-stu-id="3544c-124">Role</span></span>|<span data-ttu-id="3544c-125">できること</span><span class="sxs-lookup"><span data-stu-id="3544c-125">What they can do</span></span>|
|---------|---------|
|<span data-ttu-id="3544c-126">Office 365 のグローバル管理者 (Azure、会社の管理者の場合)、ユーザー管理者</span><span class="sxs-lookup"><span data-stu-id="3544c-126">Office 365 global admin (in Azure, the Company administrator), User administrator</span></span>|<span data-ttu-id="3544c-127">Office 365 グループの有効期限ポリシー設定を作成、読み取り、更新、または削除します。</span><span class="sxs-lookup"><span data-stu-id="3544c-127">Create, read, update, or delete the Office 365 groups expiration policy settings.</span></span>|
|<span data-ttu-id="3544c-128">ユーザー</span><span class="sxs-lookup"><span data-stu-id="3544c-128">User</span></span>|<span data-ttu-id="3544c-129">自分が所有する Office 365 グループを更新または[復元](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-restore-deleted)する</span><span class="sxs-lookup"><span data-stu-id="3544c-129">Renew or [restore](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-restore-deleted) an Office 365 Group that they own</span></span>|

## <a name="how-to-set-the-expiration-policy"></a><span data-ttu-id="3544c-130">有効期限ポリシーを設定する方法</span><span class="sxs-lookup"><span data-stu-id="3544c-130">How to set the expiration policy</span></span>

<span data-ttu-id="3544c-131">前述したように、有効期限は既定でオフになっています。</span><span class="sxs-lookup"><span data-stu-id="3544c-131">As noted above, expiry is turned off by default.</span></span> <span data-ttu-id="3544c-132">管理者は有効期限ポリシーを有効にして、そのプロパティを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3544c-132">An administrator will have to enable the expiration policy and set the properties for it to take effect.</span></span> <span data-ttu-id="3544c-133">これを有効にするには、 **Azure Active Directory (AAD)** > **グループ** > の**有効期限が切れる**ようにします。</span><span class="sxs-lookup"><span data-stu-id="3544c-133">To enable it go to **Azure Active Directory (AAD)** > **Groups** > **Expiration**.</span></span> <span data-ttu-id="3544c-134">ここでは、既定のグループの有効期間を設定して、最初と2番目の有効期限の通知がグループの所有者に移動するまでの時間を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3544c-134">Here you can set the default group lifetime and specify how far in advance you want the first and second expiration notifications to go to the group owner.</span></span>

<span data-ttu-id="3544c-135">グループの有効期間は日単位で指定し、180、365、または指定したカスタム値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3544c-135">The group lifetime is specified in days and can be set to 180, 365 or to a custom value that you specify.</span></span> <span data-ttu-id="3544c-136">カスタム値は、少なくとも30日である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3544c-136">The custom value has to be at least 30 days.</span></span>

<span data-ttu-id="3544c-137">グループに所有者がいない場合は、指定された管理者に有効期限のメールが送られます。</span><span class="sxs-lookup"><span data-stu-id="3544c-137">If the group does not have an owner the expiration emails will go to a specified administrator.</span></span>

<span data-ttu-id="3544c-138">すべてのグループに対してポリシーを設定するか、選択したグループのみを設定するか、または **[なし**] を選択して完全にオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="3544c-138">You can set the policy for all of your groups, only selected groups, or turn it off completely by selecting **None**.</span></span> <span data-ttu-id="3544c-139">現在、グループごとに異なるポリシーを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="3544c-139">Note that currently you can't have different policies for different groups.</span></span>

![Azure Active Directory でのグループの有効期限設定のスクリーンショット](../media/azure-groups-expiration-settings.png)

## <a name="how-expiry-works-with-the-retention-policy"></a><span data-ttu-id="3544c-141">保持ポリシーを使用した有効期限のしくみ</span><span class="sxs-lookup"><span data-stu-id="3544c-141">How expiry works with the retention policy</span></span>

<span data-ttu-id="3544c-142">グループの [セキュリティとコンプライアンスセンター] でアイテム保持ポリシーをセットアップした場合、有効期限ポリシーは保持ポリシーとシームレスに連動します。</span><span class="sxs-lookup"><span data-stu-id="3544c-142">If you have setup retention policy in Security and Compliance center for groups, expiration policy works seamlessly with retention policy.</span></span> <span data-ttu-id="3544c-143">グループの有効期限が切れると、グループサイト内のグループの会話は、アイテム保持ポリシーで定義されている特定の日数だけ、保持コンテナーに保持されます。</span><span class="sxs-lookup"><span data-stu-id="3544c-143">When a group expires, the group's conversations in mail box and files in the group site are retained in the retention container for the specific number of days defined in the retention policy.</span></span> <span data-ttu-id="3544c-144">ただし、有効期限が切れた後は、グループまたはそのコンテンツは表示されません。</span><span class="sxs-lookup"><span data-stu-id="3544c-144">Users will not see the group, or its content, after expiration however.</span></span>

## <a name="how-and-when-a-group-owner-learns-if-their-groups-are-going-to-expire"></a><span data-ttu-id="3544c-145">グループの有効期限が切れるかどうかをグループの所有者が学習する方法とタイミング</span><span class="sxs-lookup"><span data-stu-id="3544c-145">How and when a Group owner learns if their Groups are going to expire</span></span>

<span data-ttu-id="3544c-146">グループの所有者には、電子メールを介してのみ通知されます。</span><span class="sxs-lookup"><span data-stu-id="3544c-146">Group owners will only be notified via email.</span></span> <span data-ttu-id="3544c-147">このグループが Planner、SharePoint、またはその他のアプリによって作成された場合、有効期限通知は常に電子メール経由で送信されます。</span><span class="sxs-lookup"><span data-stu-id="3544c-147">If the group was created via Planner, SharePoint, or any other app, the expiration notifications will always come via email.</span></span> <span data-ttu-id="3544c-148">グループが Teams によって作成された場合、グループの所有者は [activity] セクションを通じて更新する通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="3544c-148">If the group was created via Teams, the group owner will receive a notification to renew through the activity section.</span></span> <span data-ttu-id="3544c-149">グループの所有者が有効な電子メールアドレスを持っていない場合は、グループの有効期限を有効にすることはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="3544c-149">It's not recommended that you enable expiration on a group if your group owner doesn't have a valid email address.</span></span>

<span data-ttu-id="3544c-150">グループの有効期限が切れるまで30日間、グループの所有者 (または所有者がいないグループに対して指定したメールアドレス) は、グループを簡単に更新できる電子メールを受信します。</span><span class="sxs-lookup"><span data-stu-id="3544c-150">30 days before the group expires, the group owners (or the email addresses that you specified for groups that don't have an owner) will receive an email allowing them to easily renew the group.</span></span> <span data-ttu-id="3544c-151">更新されていない場合は、有効期限が切れるまで15日後にもう一度更新メールを受信します。</span><span class="sxs-lookup"><span data-stu-id="3544c-151">If they don't renew it, they'll receive another renewal email 15 days before expiration.</span></span> <span data-ttu-id="3544c-152">まだ更新していない場合は、有効期限が切れる前に1日に1回のメール通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="3544c-152">If they still haven't renewed it, they will receive one more email notification the day before expiration.</span></span>

<span data-ttu-id="3544c-153">何らかの理由で、所有者または管理者が期限切れになる前にグループを更新しない場合でも、管理者は有効期限が切れてから30日以内にグループを復元することができます。</span><span class="sxs-lookup"><span data-stu-id="3544c-153">If for some reason none of the owners or admins renew the group before it expires, the admin can still restore the group for up to 30 days after expiration.</span></span> <span data-ttu-id="3544c-154">詳細については[、「削除された Office 365 グループを復元する](https://support.office.com/article/restore-a-deleted-office-365-group-b7c66b59-657a-4e1a-8aa0-8163b1f4eb54)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3544c-154">For details see: [Restore a deleted Office 365 Group](https://support.office.com/article/restore-a-deleted-office-365-group-b7c66b59-657a-4e1a-8aa0-8163b1f4eb54).</span></span>

## <a name="related-articles"></a><span data-ttu-id="3544c-155">関連記事</span><span class="sxs-lookup"><span data-stu-id="3544c-155">Related articles</span></span>

[<span data-ttu-id="3544c-156">アイテム保持ポリシーの概要</span><span class="sxs-lookup"><span data-stu-id="3544c-156">Overview of retention policies</span></span>](https://support.office.com/article/5e377752-700d-4870-9b6d-12bfc12d2423)

[<span data-ttu-id="3544c-157">孤立グループに新しい所有者を割り当てる</span><span class="sxs-lookup"><span data-stu-id="3544c-157">Assign a new owner to an orphaned group</span></span>](https://support.office.com/article/86bb3db6-8857-45d1-95c8-f6d540e45732)

[<span data-ttu-id="3544c-158">Office 365 グループの有効期限を構成する</span><span class="sxs-lookup"><span data-stu-id="3544c-158">Configure Office 365 groups expiration</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-groups-lifecycle-azure-portal)