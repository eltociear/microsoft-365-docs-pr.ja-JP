---
title: 共同作業のためのチームの作成
ms.author: stevhord
author: samanro
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-identity-device-management
- M365-Campaigns
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
description: Microsoft Teams を使用してチームのコラボレーションスペースを作成します。
ms.openlocfilehash: 0b0d0d968bcf1cec44fefabcde84fba6ddab3c63
ms.sourcegitcommit: c452413dff5d5388c9725f38871246237c313e65
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2019
ms.locfileid: "35183365"
---
# <a name="create-teams-for-collaboration-in-microsoft-teams"></a><span data-ttu-id="a7aeb-103">Microsoft Teams での共同作業のためのチームの作成</span><span class="sxs-lookup"><span data-stu-id="a7aeb-103">Create teams for collaboration in Microsoft Teams</span></span>

<span data-ttu-id="a7aeb-104">Microsoft Teams は、任意のデバイスから、スタッフが開催し、会話を行えるようにするコラボレーションアプリです。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-104">Microsoft Teams is a collaboration app that helps your staff stay organized and have conversations, from any device.</span></span> <span data-ttu-id="a7aeb-105">Microsoft Teams を使用して、組織外のスタッフまたはゲストのメンバーとのインスタント会話を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-105">You can use Microsoft Teams to have instant conversations with members of your staff or guests outside your organization.</span></span> <span data-ttu-id="a7aeb-106">また、電話をかけたり、会議をホストしたり、ファイルを共有したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-106">You can also make phone calls, host meetings, and share files.</span></span>

## <a name="best-practices"></a><span data-ttu-id="a7aeb-107">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="a7aeb-107">Best practices</span></span>

<span data-ttu-id="a7aeb-108">たとえば、次のようなチームを作成して、安全にコミュニケーションを行い共同作業を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-108">As an example, campaigns can create the following teams to communicate and collaborate securely:</span></span>

1. <span data-ttu-id="a7aeb-109">**キャンペーンは、** 主なキャンペーンメンバーだけがアクセスし、潜在的な機密の懸念事項について話し合うように、プライベートチームとしてチームを設定します。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-109">**A Campaign Leads team** - set this up as a private team so that only your key campaign members can access it and discuss potentially sensitive concerns.</span></span>
2. <span data-ttu-id="a7aeb-110">**一般的なキャンペーンチーム**。これは、すべてのユーザーが日常的なコミュニケーションや作業に使用できるようにするためのものです。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-110">**A general Campaign team** - this is for everyone to use for day to day communications and work.</span></span> <span data-ttu-id="a7aeb-111">個人、グループ、または委員会は、作業を行うためにこのチームのチャネルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-111">Individuals, groups, or committees can set up channels in this team to do their work.</span></span> <span data-ttu-id="a7aeb-112">たとえば、イベント計画のユーザーは、チャットのためのチャネルをセットアップし、キャンペーンイベントについて物流を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-112">For example, the event planning people can set up a channel to chat and coordinate logistics for campaign events.</span></span>
3. <span data-ttu-id="a7aeb-113">**パートナーチーム**-ベンダー、パートナー、またはボランティアとの間で、機密事項を許可せずに調整することができます。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-113">**A partners team** - one where you can coordinate with your vendors, partners, or volunteers without allowing them into anything sensitive.</span></span>

<span data-ttu-id="a7aeb-114">また、特定のプロジェクトのチームを作成し、含める必要のあるユーザーに基づいて適切な保護を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-114">You can also create teams for specific projects and apply the right amount of protection based on who needs to be included.</span></span> 

![セキュリティで保護されたコミュニケーションとコラボレーションを可能にする3つの独立したチームを含む Microsoft Teams ウィンドウの図](media/m365-democracy-teams-collab.png)

<span data-ttu-id="a7aeb-116">チームを作成する場合は、次のように作成します。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-116">When you create a team, here's what else gets created:</span></span>

- <span data-ttu-id="a7aeb-117">新しい[Office 365 グループ](https://docs.microsoft.com/en-us/MicrosoftTeams/office-365-groups)</span><span class="sxs-lookup"><span data-stu-id="a7aeb-117">A new [Office 365 group](https://docs.microsoft.com/en-us/MicrosoftTeams/office-365-groups)</span></span>
- <span data-ttu-id="a7aeb-118">チームファイルを保存するための[SharePoint Online](https://docs.microsoft.com/en-us/MicrosoftTeams/sharepoint-onedrive-interact)サイトとドキュメントライブラリ</span><span class="sxs-lookup"><span data-stu-id="a7aeb-118">A [SharePoint Online](https://docs.microsoft.com/en-us/MicrosoftTeams/sharepoint-onedrive-interact) site and document library to store team files</span></span>
- <span data-ttu-id="a7aeb-119">[Exchange Online](https://docs.microsoft.com/en-us/MicrosoftTeams/exchange-teams-interact)の共有メールボックスと予定表</span><span class="sxs-lookup"><span data-stu-id="a7aeb-119">An [Exchange Online](https://docs.microsoft.com/en-us/MicrosoftTeams/exchange-teams-interact) shared mailbox and calendar</span></span>
- <span data-ttu-id="a7aeb-120">OneNote ノートブック</span><span class="sxs-lookup"><span data-stu-id="a7aeb-120">A OneNote notebook</span></span>
- <span data-ttu-id="a7aeb-121">Planner や Power BI などの他の Office 365 アプリに結びつける</span><span class="sxs-lookup"><span data-stu-id="a7aeb-121">Ties into other Office 365 apps such as Planner and Power BI</span></span>

<span data-ttu-id="a7aeb-122">Microsoft Teams の内部では、次のことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-122">Inside Microsoft Teams, you can find:</span></span>
1. <span data-ttu-id="a7aeb-123">**Teams** -自分が属している、または自分で作成したチャネルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-123">**Teams** - Find channels to belong to or create your own.</span></span> <span data-ttu-id="a7aeb-124">内部チャネルでは、オンプレでの会議を保持し、会話を行い、ファイルを共有することができます。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-124">Inside channels you can hold on-the-spot meetings, have conversations, and share files.</span></span>

2. <span data-ttu-id="a7aeb-125">**会議**-日または週に対して設定したすべてのものを表示します。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-125">**Meetings** - See everything you've got lined up for the day or week.</span></span> <span data-ttu-id="a7aeb-126">または、会議をスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-126">Or, schedule a meeting.</span></span> <span data-ttu-id="a7aeb-127">この予定表は、Outlook の予定表と同期します。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-127">This calendar syncs with your Outlook calendar.</span></span>
 
3. <span data-ttu-id="a7aeb-128">**呼び出し**-組織で設定されている場合は、microsoft teams を使用していない場合でも、microsoft teams からすべてのユーザーを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-128">**Calls** - In some cases, if your organization has it set up, you can call anyone from Microsoft Teams, even if they're not using Microsoft Teams.</span></span>

4. <span data-ttu-id="a7aeb-129">**作業**中のすべての未読メッセージ、@mentions、返信などをキャッチアップします。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-129">**Activity** - Catch up on all your unread messages, @mentions, replies, and more.</span></span> 

<span data-ttu-id="a7aeb-130">上部にあるコマンドボックスを使用して、特定のアイテムまたはユーザーを検索したり、クイックアクションを実行したり、アプリを起動したりします。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-130">Use the command box at the top to search for specific items or people, take quick actions, and launch apps.</span></span>


## <a name="set-it-up"></a><span data-ttu-id="a7aeb-131">設定する</span><span class="sxs-lookup"><span data-stu-id="a7aeb-131">Set it up</span></span>


<span data-ttu-id="a7aeb-132">キャンペーンマネージャーだけでなく、次のような候補として、プライベートチームを作成します。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-132">Create a private team for just the campaign manager and candidate like this.</span></span> 

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWeqWA]

<span data-ttu-id="a7aeb-133">キャンペーン内のすべてのユーザーがファイルの通信と共有に使用できる、組織全体のチームを作成します。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-133">Create an organization-wide team that everyone in the campaign can use to communicate and share files'</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2GCG9]

<span data-ttu-id="a7aeb-134">ファイナンスの広告など、キャンペーン外のゲストと共有するチームを作成します。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-134">Create a team that you share with guests outside the campaign, such as advertising of financing.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1FQMp]

<span data-ttu-id="a7aeb-135">Microsoft teams の[技術ドキュメント](https://docs.microsoft.com/en-us/microsoftteams/microsoft-teams)に関する microsoft teams の詳細情報</span><span class="sxs-lookup"><span data-stu-id="a7aeb-135">Learn more about Microsoft Teams at [Microsoft Teams technical documentation](https://docs.microsoft.com/en-us/microsoftteams/microsoft-teams)</span></span>

## <a name="admin-settings"></a><span data-ttu-id="a7aeb-136">管理設定</span><span class="sxs-lookup"><span data-stu-id="a7aeb-136">Admin settings</span></span>

<span data-ttu-id="a7aeb-137">組織全体のチームを作成するには、管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-137">You must be an admin to create an organization-wide team.</span></span> <span data-ttu-id="a7aeb-138">詳細については、「 [Office 365 の管理者とは](https://support.office.com/en-us/article/what-is-an-admin-e123627e-4892-4461-b9aa-1b6d57a5cfa4?ui=en-US&rs=en-US&ad=US)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7aeb-138">For more information, see [What is an Admin in Office 365?](https://support.office.com/en-us/article/what-is-an-admin-e123627e-4892-4461-b9aa-1b6d57a5cfa4?ui=en-US&rs=en-US&ad=US).</span></span>
  