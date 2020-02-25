---
title: Office 365 にドメインを追加する
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365_Setup
- Adm_O365
- Adm_TOC
ms.custom:
- TopSMBIssues
- SaRA
- MSStore_Link
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 6383f56d-3d09-4dcb-9b41-b5f5a5efd611
description: Microsoft 365 管理センターで Office 365 にドメインを追加するには、 DNS ホストで DNS レコードを追加します。 これらの手順を案内するウィザードがあります。
ms.openlocfilehash: 4170fd74ae734a6fda9e535c17086997b1db6f6b
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/24/2020
ms.locfileid: "42247922"
---
# <a name="add-a-domain-to-office-365"></a><span data-ttu-id="d3108-104">Office 365 にドメインを追加する</span><span class="sxs-lookup"><span data-stu-id="d3108-104">Add a domain to Office 365</span></span>

 <span data-ttu-id="d3108-105">探している内容が見つからない場合は、**[ドメインに関する FAQ を確認Q](domains-faq.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3108-105">**[Check the Domains FAQ](domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
 <span data-ttu-id="d3108-106">*追加、変更またはドメインを削除するには、[ビジネスまたはエンタープライズ プラン](https://products.office.com/business/office)の**グローバル管理者**である**必要**があります。これらの変更は、テナント全体、*カスタマイズ管理者*または*正規ユーザー*に影響を与え、変更を加えることはできません。*</span><span class="sxs-lookup"><span data-stu-id="d3108-106">*To Add, modify or remove domains you **must** be a **Global Administrator** of a [business or enterprise plan](https://products.office.com/business/office). These changes affect the whole tenant, *Customized administrators* or *regular users* won't be able to make these changes.*</span></span>  

 <span data-ttu-id="d3108-107">以下の手順に従って、ドメインの追加、セットアップ、またはセットアップの続行を行います。</span><span class="sxs-lookup"><span data-stu-id="d3108-107">Follow these steps to add, set up, or continue setting up a domain.</span></span> 

::: moniker range="o365-worldwide"
  
::: moniker-end

::: moniker range="o365-germany"

> [!VIDEO https://www.microsoft.com/videoplayer/embed/dda6df6d-37b0-41ff-905b-089448355a31?autoplay=false]
  
::: moniker-end

::: moniker range="o365-worldwide"

1. <span data-ttu-id="d3108-108"><a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> の管理センターにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d3108-108">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>

::: moniker-end
::: moniker range="o365-germany"

1. <span data-ttu-id="d3108-109"><a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a> から管理センターにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d3108-109">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">https://portal.office.de/adminportal</a>.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="d3108-110"><a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a> から管理センターにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d3108-110">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">https://portal.partner.microsoftonline.cn</a>.</span></span>

::: moniker-end
    
2. <span data-ttu-id="d3108-111">[**設定**]  >  [**ドメイン**] ページの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3108-111">Go to the **Settings** > **Domains** page.</span></span> 

3. <span data-ttu-id="d3108-112">[**ドメインの追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3108-112">Select **Add domain**.</span></span>
    
4. <span data-ttu-id="d3108-113">追加するドメインの名前を入力し、**[次へ]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3108-113">Enter the name of the domain you want to add, then select **Next**.</span></span>
    
5. <span data-ttu-id="d3108-114">ドメインの所有を確認する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3108-114">Choose how you want to verify that you own the domain.</span></span>
    
    1. <span data-ttu-id="d3108-115">ドメインが GoDaddy または 1&amp;1 に登録されている場合、**[サインイン]** > **[次へ]** を選択します。Office 365 が[レコードを自動的に設定](../get-help-with-domains/domain-connect.md)します。</span><span class="sxs-lookup"><span data-stu-id="d3108-115">If your domain is registered at GoDaddy or 1&amp;1, select **Sign in** > **Next** and Office 365 [will set up your records automatically](../get-help-with-domains/domain-connect.md).</span></span>
    
    2. <span data-ttu-id="d3108-116">ドメインに登録している連絡先に、検証コードを含むメールを送信できます。</span><span class="sxs-lookup"><span data-stu-id="d3108-116">You can have an email sent to the registered contact for the domain with a verification code.</span></span> <span data-ttu-id="d3108-117">レコードのメールに見覚えがない、またはメールにアクセスできない場合、3 番目のオプションを利用できます。</span><span class="sxs-lookup"><span data-stu-id="d3108-117">If you don't recognize or have access to the email on record, you can use the third option.</span></span>
    
    3. <span data-ttu-id="d3108-118">TXT レコードを使用し、ドメインを検証できます。</span><span class="sxs-lookup"><span data-stu-id="d3108-118">You can use a TXT record to verify your domain.</span></span> <span data-ttu-id="d3108-119">これを選択し、**[次へ]** を選択すると、この DNS レコードをレジストラーの Web サイトに追加する方法が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3108-119">Select this and select **Next** to see instructions for how to add this DNS record to your registrar's website.</span></span> <span data-ttu-id="d3108-120">レコードを追加すると、検証に最大 30 分かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="d3108-120">This can take up to 30 minutes to verify after you've added the record.</span></span> 
    
6. <span data-ttu-id="d3108-121">Office でドメインを使用するために必要な DNS 変更の方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3108-121">Choose how you want to make the DNS changes required for Office to use your domain.</span></span>
    
    1. <span data-ttu-id="d3108-122">DNS を Office に自動構成させる場合、**[DNS レコードを追加してもらう]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3108-122">Choose **Add the DNS records for me** if you want Office to configure your DNS automatically.</span></span> 
    
  
    2. <span data-ttu-id="d3108-123">特定の Office 365 サービスのみをドメインに追加する場合、またはここではこの手順をスキップして後で行う場合、**[DNS レコードを自分で追加する]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3108-123">Choose **I'll add the DNS records myself** if you want to attach only specific Office 365 services to your domain or if you want to skip this for now and do this later.</span></span> <span data-ttu-id="d3108-124">**次のように、操作内容を正確に把握している場合に、このオプションを選択します。**</span><span class="sxs-lookup"><span data-stu-id="d3108-124">**Choose this option if you know exactly what you're doing.**</span></span>
    
7. <span data-ttu-id="d3108-125">*DNS レコードを自分で追加する*を選択した場合、**[次へ]** を選択します。そして、ドメインを設定するために、レジストラー Web サイトに追加する必要があるすべてのレコードが含まれるページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3108-125">If you chose to  *add DNS records yourself*  , select **Next** and you'll see a page with all the records that you need to add to your registrars website to set up your domain.</span></span> 
    
  
  
    <span data-ttu-id="d3108-126">ポータルでレジストラーが認識されない場合、[一般的な方法に従うことができます](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d3108-126">If the portal doesn't recognize your registrar, you can [follow these general instructions.](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)</span></span>
    
    <span data-ttu-id="d3108-127">[ホスト固有の命令](https://support.office.com/article/ae950c9e-e8d9-4108-b0cb-449156998580)の一覧からお使いのホストを見つけ、手順に従って必要なすべてのレコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d3108-127">Check our list of [host-specific instructions](https://support.office.com/article/ae950c9e-e8d9-4108-b0cb-449156998580) to find your host and follow the steps to add all the records you need.</span></span> 
    
    <span data-ttu-id="d3108-128">ドメインの DNS ホスティング プロバイダーまたはドメイン レジストラーがわからない場合は、「[ドメイン レジストラーまたは DNS ホスティング プロバイダーを探す](../get-help-with-domains/find-your-domain-registrar.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3108-128">If you don't know the DNS hosting provider or domain registrar for your domain, see [Find your domain registrar or DNS hosting provider](../get-help-with-domains/find-your-domain-registrar.md).</span></span>
    
    <span data-ttu-id="d3108-129">後で行う場合、下にスクロールして **[この手順をスキップ]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3108-129">If you want to wait for later, scroll to the bottom and select **Skip this step**.</span></span>
    
8. <span data-ttu-id="d3108-130">**[完了]** を選択します。これで完了です!</span><span class="sxs-lookup"><span data-stu-id="d3108-130">Select **Finish** - you're done!</span></span> 

## <a name="related-articles"></a><span data-ttu-id="d3108-131">関連記事</span><span class="sxs-lookup"><span data-stu-id="d3108-131">Related articles</span></span>

[<span data-ttu-id="d3108-132">ドメイン FAQ</span><span class="sxs-lookup"><span data-stu-id="d3108-132">Domains FAQ</span></span>](domains-faq.md)

[<span data-ttu-id="d3108-133">ドメインとは</span><span class="sxs-lookup"><span data-stu-id="d3108-133">What is a domain?</span></span>](../get-help-with-domains/what-is-a-domain.md)

[<span data-ttu-id="d3108-134">Office 365 でドメイン名を購入する</span><span class="sxs-lookup"><span data-stu-id="d3108-134">Buy a domain name in Office 365</span></span>](../get-help-with-domains/buy-a-domain-name.md)

[<span data-ttu-id="d3108-135">ドメインを設定する (ホスト固有の手順)</span><span class="sxs-lookup"><span data-stu-id="d3108-135">Set up your domain (host-specific instructions)</span></span>](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md)

[<span data-ttu-id="d3108-136">Office 365 のドメインに関するヘルプ</span><span class="sxs-lookup"><span data-stu-id="d3108-136">Get help with Office 365 domains</span></span>](../get-help-with-domains/get-help-with-domains.md)