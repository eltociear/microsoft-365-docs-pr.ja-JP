---
title: Office 365 では、Teams、safelinks、安全なリンク、悪意のあるリンク、office 365 ATP、Teams の安全なリンク、ユーザーが無効なリンクをクリックするのを停止する悪意のあるリンク
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
audience: Admin
ms.date: 02/28/2020
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: クリックしたときに Teams が安全なリンクにアクセスできるようになります。 1対1のチャット、グループ間、またはチャネル内のチャットを使用しているかどうか、および Office 365 ATP へのサブスクリプションがある場合は、このセーフティ機能を有効にして使用することができます。
ms.openlocfilehash: ba7ef2ae63b788ec94fbbb15c3c00312177a59d5
ms.sourcegitcommit: cf07dfccec476ac2526a6171ec6b6365686f759f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/29/2020
ms.locfileid: "42341610"
---
<!--06/21/2019-->

# <a name="office-365-safe-links-in-teams"></a><span data-ttu-id="b2e57-104">Teams での Office 365 の安全なリンク</span><span class="sxs-lookup"><span data-stu-id="b2e57-104">Office 365 Safe Links in Teams</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2e57-105">この機能は、2020年2月28日の Microsoft Teams テクノロジ導入プログラム (タップ) にあるお客様向けの**パブリックプレビュー**です。</span><span class="sxs-lookup"><span data-stu-id="b2e57-105">This feature is in **Public Preview** for customers in the Microsoft Teams Technology Adoption Program (TAP) as of Feb 28, 2020.</span></span> <span data-ttu-id="b2e57-106">このメモは、Teams の安全なリンクがより幅広く利用できる場合に記事から削除されます。</span><span class="sxs-lookup"><span data-stu-id="b2e57-106">This note will be removed from the article when Safe Links for Teams is more widely available.</span></span>

<span data-ttu-id="b2e57-107">作業を管理するための Office 365 クラウドベースのアプリケーションである Microsoft Teams は、既に安全な添付ファイル (Office 365) を使用していますが、これでクリック時に安全なリンクにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="b2e57-107">Microsoft Teams, an Office 365 Cloud-based application for managing your work, already uses safe attachments (for Office 365), but it will now have access to safe links at the time of your click.</span></span> <span data-ttu-id="b2e57-108">1対1のチャット、グループ間、またはチャネル内のチャットを使用しているかどうか、および Office 365 ATP へのサブスクリプションがある場合は、この安全策を有効にして使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b2e57-108">Whether you’re using chats 1-on-1 Chats, between Groups, or in Channels, and Tabs, if you have a subscription to Office 365 ATP, you will have the ability to enable and use this safety measure.</span></span>

<span data-ttu-id="b2e57-109">そのしくみは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b2e57-109">Here’s how it works:</span></span> 

1. <span data-ttu-id="b2e57-110">Teams アプリケーションを起動すると、Office 365 は、ユーザーが Office 365 ATP を使用している組織に所属しており、ユーザーが Microsoft Teams の保護が有効になっているアクティブな安全リンクポリシーの一部であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2e57-110">When you start the Teams application, Office 365 will check to make sure the user belongs to an organization that has Office 365 ATP, and that the user is part of an active safe links policy with its protection enabled for Microsoft Teams.</span></span>

2. <span data-ttu-id="b2e57-111">上記の条件に該当する場合、Url は、チャット、グループチャット、チャネル、およびそのユーザーのタブでクリックしたときに検証されます。</span><span class="sxs-lookup"><span data-stu-id="b2e57-111">If the above are true, then URLs will be validated at the time of click in Chats, Group Chats, Channels, and in Tabs for that user.</span></span>
 
## <a name="what-will-users-experience"></a><span data-ttu-id="b2e57-112">ユーザーにはどのような状況がありますか?</span><span class="sxs-lookup"><span data-stu-id="b2e57-112">What will users experience?</span></span> 

<span data-ttu-id="b2e57-113">保護されたすべてのユーザーには、次のような危険な Url があります。</span><span class="sxs-lookup"><span data-stu-id="b2e57-113">All protected users will have this experience with hazardous URLs:</span></span> 

- <span data-ttu-id="b2e57-114">リンクが Teams 会話、グループチャット、またはチャネルからクリックされた場合は、既定のブラウザーでページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2e57-114">If the link was clicked from a Teams conversation, group chat, or from channels, a page will render in the default browser.</span></span> <span data-ttu-id="b2e57-115">固定されたタブからリンクがクリックされた場合は、そのページがそのタブ内の Teams GUI に表示され、セキュリティ上の理由から、ブラウザーで開くオプションは無効になります。</span><span class="sxs-lookup"><span data-stu-id="b2e57-115">If the link was clicked from a pinned tab, the page will appear in the Teams GUI within that tab, and the option to open in browser will be disabled for security purposes.</span></span>

- <span data-ttu-id="b2e57-116">このユーザーは、URL のサイトへの進行をブロックされます。</span><span class="sxs-lookup"><span data-stu-id="b2e57-116">This user will be blocked from proceeding to the URL’s site.</span></span>

<span data-ttu-id="b2e57-117">リンクを送信したユーザーが Office 365 ATP によって保護されていない場合は、自分のコンピューターで URL をクリックして、問題のサイトを解決することができます。</span><span class="sxs-lookup"><span data-stu-id="b2e57-117">If the user who sent the link isn’t protected by Office 365 ATP, he or she is free to click the URL on his or her machine and resolve the problem site.</span></span> <span data-ttu-id="b2e57-118">これにより、Office 365 管理者は、保護されたユーザーがどのようなものであるかを認識できるようになります。</span><span class="sxs-lookup"><span data-stu-id="b2e57-118">This makes it doubly important for Office 365 Administrators to be aware of who their protected users are and should be.</span></span>

![Teams ページの安全なリンクは、悪意のあるリンクを報告し、ページへの送信をブロックします。](/microsoft-365/media/TP_SafelinksForTeams_Malicious.png)

<span data-ttu-id="b2e57-120">Teams で、このページの [*戻る*] ボタンをクリックすると、そのページが閉じます (または、ユーザーが空白のページが閉じられる可能性があります)。</span><span class="sxs-lookup"><span data-stu-id="b2e57-120">Clicking the *Go Back* button on this page in Teams will close it out (or may result in a blank page users  can close out).</span></span> <span data-ttu-id="b2e57-121">ただし、リンクをもう一度クリックすると、このページが表示されるように、サイトの評価が reassessment されます。</span><span class="sxs-lookup"><span data-stu-id="b2e57-121">However, clicking on the link again will result in reassessment of the reputation of the site so that this page reappears.</span></span>

> [!NOTE]
><span data-ttu-id="b2e57-122">一部の Office 365 管理者は、[ブロック] ページで**続行**するかどうかのメッセージを有効にします。</span><span class="sxs-lookup"><span data-stu-id="b2e57-122">Some Office 365 Admins will enable the **Continue Anyway** message on the blocking page.</span></span> <span data-ttu-id="b2e57-123">ただし、安全なリンクによってサイトの評価が測定され、不足している場合は、これ以上のクリックスルーを行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b2e57-123">However, if safe links measures the reputation of a site and finds it lacking, no further click-through should be undertaken.</span></span> <span data-ttu-id="b2e57-124">ユーザーが安全対策を省略することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="b2e57-124">It is not recommended that users bypass safety measures.</span></span> <span data-ttu-id="b2e57-125">続行する前に、この点を考慮に入れてください。</span><span class="sxs-lookup"><span data-stu-id="b2e57-125">Please weigh this into your considerations before enabling Continue Anyway.</span></span> 
