---
title: 機密度ラベルで SharePoint Online ファイルを保護する
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/27/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- SPO_Content
ms.custom:
- Ent_Solutions
ms.assetid: 5b9c8e41-25d2-436d-89bb-9aecb9ec2b80
description: '概要: Azure Information Protection を適用して、機密性の高い SharePoint Online チーム サイト内のファイルを保護します。'
ms.openlocfilehash: b5251d393249e9023f6f437cb3df6c074ebdf436
ms.sourcegitcommit: bf30a2314376f0b7d577741b97df017969737d11
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/27/2019
ms.locfileid: "39638060"
---
# <a name="protect-sharepoint-online-files-with-a-sensitivity-label"></a><span data-ttu-id="24a7a-103">機密度ラベルで SharePoint Online ファイルを保護する</span><span class="sxs-lookup"><span data-stu-id="24a7a-103">Protect SharePoint Online files with a sensitivity label</span></span>

<span data-ttu-id="24a7a-104">この記事の手順を使用して、Office 365 の秘密度ラベルを構成し、ファイルの暗号化とアクセス許可を提供します。</span><span class="sxs-lookup"><span data-stu-id="24a7a-104">Use the steps in this article to configure an Office 365 sensitivity label to provide encryption and permissions for files.</span></span> <span data-ttu-id="24a7a-105">これらのファイルは、非常に機密性の高い社外秘の保護のため構成されている SharePoint ライブラリに追加できます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-105">These files can be added to a SharePoint library configured for highly confidential protection.</span></span> <span data-ttu-id="24a7a-106">または、サイトから直接ファイルを開き、ラベルを適用できます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-106">Or, you can open a file directly from the site and apply the label.</span></span> <span data-ttu-id="24a7a-107">暗号化およびアクセス許可の保護は、ファイルをサイトからダウンロードした場合にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-107">The encryption and permissions protection travels with a file even when it is downloaded from the site.</span></span> 

<span data-ttu-id="24a7a-p102">これらの手順は、SharePoint サイトとそれらのサイト内のファイルの高度な機密保護を構成するための大きなソリューションの一部です。詳細については、「[SharePoint Online サイトとファイルをセキュリティで保護する](https://docs.microsoft.com/microsoft-365/compliance/deploy-sharepoint-online-sites-for-three-tiers-of-protection)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24a7a-p102">These steps are part of a larger solution for configuring highly confidential protection for SharePoint sites and the files within these sites. For more information, see [Secure SharePoint Online sites and files](https://docs.microsoft.com/microsoft-365/compliance/deploy-sharepoint-online-sites-for-three-tiers-of-protection).</span></span> 

<span data-ttu-id="24a7a-110">SharePoint Online 内のファイルに機密度ラベルを使用することは、すべてのお客様に推奨されるものではなく、ファイルの一部に対してこの保護レベルを必要としているお客様向けのオプションです。</span><span class="sxs-lookup"><span data-stu-id="24a7a-110">Using Azure Information Protection for files in SharePoint Online is not recommended for all customers, but is an option for customers who need this level of protection for a subset of files.</span></span>

<span data-ttu-id="24a7a-111">このソリューションに関する重要な注意点がいくつかあります:</span><span class="sxs-lookup"><span data-stu-id="24a7a-111">Some important notes about this solution:</span></span>
- <span data-ttu-id="24a7a-112">暗号化が Office 365 に保存されているファイルに適用されている場合、このサービスはこれらのファイルのコンテンツを処理することはできません。</span><span class="sxs-lookup"><span data-stu-id="24a7a-112">When Azure Information Protection encryption is applied to files stored in Office 365, the service cannot process the contents of these files.</span></span> <span data-ttu-id="24a7a-113">共同編集、電子情報開示、検索、Delve、その他の共同作業機能は機能しません。</span><span class="sxs-lookup"><span data-stu-id="24a7a-113">Co-authoring, eDiscovery, search, Delve, and other collaborative features do not work.</span></span> <span data-ttu-id="24a7a-114">データ損失防止 (DLP) ポリシーはメタデータ (Office 365 ラベルを含む) でのみ機能し、これらのファイルのコンテンツ (ファイル内のクレジットカード番号など) には機能しません。</span><span class="sxs-lookup"><span data-stu-id="24a7a-114">Data Loss Prevention (DLP) policies can only work with the metadata (including Office 365 labels) but not the contents of these files (such as credit card numbers within files).</span></span>

- <span data-ttu-id="24a7a-115">このソリューションでは、ユーザーは保護を適用するラベルを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24a7a-115">This solution requires a user to select a label that applies the protection.</span></span> <span data-ttu-id="24a7a-116">自動暗号化と SharePoint がファイルにインデックスを付け検査する機能を要求するには、SharePoint Online で Information Rights Management (IRM) を使用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="24a7a-116">If you require automatic encryption and the ability for SharePoint to index and inspect the files, consider using Information Rights Management (IRM) in SharePoint Online.</span></span> <span data-ttu-id="24a7a-117">IRM の SharePoint ライブラリを構成する場合、ファイルが編集のためにダウンロードされるときに、自動的に暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-117">When you configure a SharePoint library for IRM, files are automatically encrypted when they are downloaded for editing.</span></span>  <span data-ttu-id="24a7a-118">SharePoint IRM には、決定に影響を与える可能性のある制限が含まれます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-118">SharePoint IRM includes limitations that might influence your decision.</span></span> <span data-ttu-id="24a7a-119">詳細については、「[SharePoint 管理センターにおける Information Rights Management (IRM) の設定](https://support.office.com/article/Set-up-Information-Rights-Management-IRM-in-SharePoint-admin-center-239CE6EB-4E81-42DB-BF86-A01362FED65C)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24a7a-119">[Set up Information Rights Management (IRM) in SharePoint admin center](https://support.office.com/article/Set-up-Information-Rights-Management-IRM-in-SharePoint-admin-center-239CE6EB-4E81-42DB-BF86-A01362FED65C).</span></span>

## <a name="admin-setup"></a><span data-ttu-id="24a7a-120">管理者セットアップ</span><span class="sxs-lookup"><span data-stu-id="24a7a-120">Admin setup</span></span>

<span data-ttu-id="24a7a-121">特定の SharePoint Online チーム サイトで、ファイルに対してこの追加レベルのセキュリティ保護を行うには、サイト独自のラベル、または厳しく規制されたデータの一般的なラベルのサブラベルのいずれかである、カスタマイズされた機密ラベルを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24a7a-121">To accomplish this additional level of security for files stored in the underlying SharePoint site of a team, you must configure a customized sensitivity label that is either its own label or a sublabel of the general label for highly regulated data.</span></span> <span data-ttu-id="24a7a-122">SharePoint Online チーム サイトの Office 365 グループのメンバーにだけ、カスタマイズされたラベルまたはサブラベルがラベルのリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-122">Only members of the Office 365 group for the SharePoint Online team site will see the customized label or sublabel in their list of labels.</span></span>

- <span data-ttu-id="24a7a-123">全体での使用と個別のプライベート チームの両方に対して少ない数のラベルが必要な場合は、秘密度ラベルを使用します。</span><span class="sxs-lookup"><span data-stu-id="24a7a-123">Use a sensitivity label when you need a small number of labels for both global use and individual private teams.</span></span>

- <span data-ttu-id="24a7a-124">ラベルを多数使用している場合、または機密性の高いチーム用のラベルを厳しく規制されたラベルの下でまとめる場合は、機密サブラベルを使用します。</span><span class="sxs-lookup"><span data-stu-id="24a7a-124">Use a sensitivity sublabel when you have a large number of labels or want to organize labels for highly confidential teams under the highly regulated label.</span></span>

<span data-ttu-id="24a7a-125">[こちらの手順](encryption-sensitivity-labels.md)を使用して、別のラベルまたはサブラベルを次の設定で構成します。</span><span class="sxs-lookup"><span data-stu-id="24a7a-125">Use [these instructions](encryption-sensitivity-labels.md) to configure a separate label or a sublabel with the following settings:</span></span>

- <span data-ttu-id="24a7a-126">ラベルまたはサブラベルの名前には、チーム サイトの名前が含まれている</span><span class="sxs-lookup"><span data-stu-id="24a7a-126">The name of the label or sublabel contains the name of the team</span></span>
- <span data-ttu-id="24a7a-127">暗号化が有効になっている</span><span class="sxs-lookup"><span data-stu-id="24a7a-127">Encryption is enabled</span></span>
- <span data-ttu-id="24a7a-128">チーム サイトの Office 365 グループに、共同作成者のアクセス許可が与えられている</span><span class="sxs-lookup"><span data-stu-id="24a7a-128">The Office 365 group for the team has Co-Author permissions</span></span>

<span data-ttu-id="24a7a-129">作成した後、ユーザーのために新しいラベルまたはサブラベルを発行します。ユーザーは、それらをローカルでチームにアップロードする前、またはチームに保存された後にファイルに適用できます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-129">After creating, publish the new label or sublabel for your users, who can then apply them to files either locally before uploading them to the team or later once the file is stored in the team.</span></span>
 
<span data-ttu-id="24a7a-130">Microsoft Word、Excel、PowerPoint の [**ホーム**] リボンの [**機密度**] のオプションから機密度ラベルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-130">Once your uses can select the sensitivity label from the **Sensitivity** option from the **Home** ribbon in Microsoft Word, Excel, and PowerPoint.</span></span>
  
> [!NOTE]
> <span data-ttu-id="24a7a-131">機密性の高い SharePoint Online チーム サイトが複数ある場合は、複数の機密度ラベルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24a7a-131">If you have multiple highly sensitive SharePoint Online team sites, you should create multiple sensitivity labels.</span></span> 
  
## <a name="adding-permissions-for-external-users"></a><span data-ttu-id="24a7a-132">外部ユーザーに対するアクセス許可の追加</span><span class="sxs-lookup"><span data-stu-id="24a7a-132">Adding permissions for external users</span></span>
<span data-ttu-id="24a7a-133">機密ラベルで保護されているファイルへのアクセス権を外部ユーザーに付与するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="24a7a-133">There are two ways you can grant external users access to files protected with a sensitivity label.</span></span> <span data-ttu-id="24a7a-134">どちらの場合も、外部ユーザーには Azure AD アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="24a7a-134">In both these cases, external users must have an Azure AD account.</span></span> <span data-ttu-id="24a7a-135">外部ユーザーが Azure AD を使用する組織のメンバーではない場合、サインアップ ページ ([https://aka.ms/aip-signup](https://aka.ms/aip-signup)) を使用して個人で Azure AD アカウントを取得できます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-135">If external users aren't members of an organization that uses Azure AD, they can obtain an Azure AD account as an individual by using this sign-up page: [https://aka.ms/aip-signup](https://aka.ms/aip-signup).</span></span>

 - <span data-ttu-id="24a7a-136">チーム サイトの Office 365 グループに外部ユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="24a7a-136">Add external users to the Office 365 group for the team site.</span></span> <span data-ttu-id="24a7a-137">最初に、自分のディレクトリに B2B ユーザーとしてのアカウントを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24a7a-137">You'll need to first add the account as a B2B user in your directory.</span></span> <span data-ttu-id="24a7a-138">[Azure Rights Management によるグループ メンバーシップのキャッシュ](https://docs.microsoft.com/azure/information-protection/plan-design/prepare#group-membership-caching-by-azure-information-protection)には、数時間かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="24a7a-138">It can take a couple of hours for [group membership caching by Azure Rights Management](https://docs.microsoft.com/azure/information-protection/plan-design/prepare#group-membership-caching-by-azure-information-protection).</span></span>  
 - <span data-ttu-id="24a7a-139">ラベル構成に直接外部ユーザーのアカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="24a7a-139">Add external user accounts directly to the label configuration.</span></span> <span data-ttu-id="24a7a-140">組織 (例: Fabrikam.com) のすべてのユーザー、Office 365 グループ (組織内の財務グループなど)、またはユーザーを追加できます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-140">You can add all users from an organization (e.g. Fabrikam.com), an Azure AD group (such as a finance group within an organization), or an individual user.</span></span> <span data-ttu-id="24a7a-141">たとえば、規制機関の外部チームを機密度ラベルのアクセス許可に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="24a7a-141">For example, you can add an external team of regulators to the protection for a label.</span></span>

## <a name="see-also"></a><span data-ttu-id="24a7a-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="24a7a-142">See Also</span></span>

[<span data-ttu-id="24a7a-143">SharePoint Online サイトとファイルをセキュリティで保護する</span><span class="sxs-lookup"><span data-stu-id="24a7a-143">Secure SharePoint Online sites and files</span></span>](https://docs.microsoft.com/microsoft-365/compliance/deploy-sharepoint-online-sites-for-three-tiers-of-protection)
  
[<span data-ttu-id="24a7a-144">選挙運動、非営利組織、およびその他のアジャイル組織のための Microsoft Security ガイダンス</span><span class="sxs-lookup"><span data-stu-id="24a7a-144">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](/security/office-365-security/microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="24a7a-145">クラウド導入およびハイブリッド ソリューション</span><span class="sxs-lookup"><span data-stu-id="24a7a-145">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)