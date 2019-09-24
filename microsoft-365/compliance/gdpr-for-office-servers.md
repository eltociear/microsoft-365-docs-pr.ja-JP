---
title: Office Server の GDPR
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: オンプレミス サーバー上の Office で GDPR の要件に対応する方法について説明します。
ms.openlocfilehash: 3c6c7aa30d4d55262cef1edabc528d6644b340c1
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2019
ms.locfileid: "37085796"
---
# <a name="gdpr-for-office-on-premises-servers"></a><span data-ttu-id="3cdf4-103">オンプレミス サーバー上の Office の GDPR</span><span class="sxs-lookup"><span data-stu-id="3cdf4-103">GDPR for Office on-premises Servers</span></span>

<span data-ttu-id="3cdf4-p101">一般データ保護規則 (GDPR) により、組織が個人データを保護し、データ主体要求に適切に応答するための要件が導入されます。このシリーズの記事では、オンプレミスのワークロードのために推奨されるアプローチを示します。</span><span class="sxs-lookup"><span data-stu-id="3cdf4-p101">The General Data Protection Regulation (GDPR) introduces requirements for organizations to protect personal data and respond appropriately to data subject requests. This series of articles provides recommended approaches for on-premises workloads:</span></span>

-   [<span data-ttu-id="3cdf4-106">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="3cdf4-106">SharePoint Server</span></span>](gdpr-for-sharepoint-server.md)

-   [<span data-ttu-id="3cdf4-107">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="3cdf4-107">Exchange Server</span></span>](gdpr-for-exchange-server.md)

-   [<span data-ttu-id="3cdf4-108">Skype for Business Server</span><span class="sxs-lookup"><span data-stu-id="3cdf4-108">Skype for Business Server</span></span>](gdpr-for-skype-for-business-server.md)

-   [<span data-ttu-id="3cdf4-109">Project Server</span><span class="sxs-lookup"><span data-stu-id="3cdf4-109">Project Server</span></span>](gdpr-for-project-server.md)

-   [<span data-ttu-id="3cdf4-110">Office Web Apps Server および Office Online Server</span><span class="sxs-lookup"><span data-stu-id="3cdf4-110">Office Web Apps Server and Office Online Server</span></span>](gdpr-for-office-online-server.md)

-   [<span data-ttu-id="3cdf4-111">オンプレミス ファイル共有</span><span class="sxs-lookup"><span data-stu-id="3cdf4-111">On-premises file shares</span></span>](gdpr-for-on-premises-file-shares.md)

<span data-ttu-id="3cdf4-112">GDPR について、また Microsoft による支援方法の詳細については、[Microsoft セキュリティ センター](https://www.microsoft.com/ja-JP/TrustCenter/Privacy/gdpr/default.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cdf4-112">For more information about the GDPR and how Microsoft can help you, see the [Microsoft Trust Center](https://www.microsoft.com/ja-JP/TrustCenter/Privacy/gdpr/default.aspx).</span></span>

<span data-ttu-id="3cdf4-p102">オンプレミス データで何らかの作業を実行する前に、法律およびコンプライアンスのチームに問い合わせて、ガイダンス情報を入手し、個人データを処理する際の既存の分類スキーマやアプローチについて確認してください。Microsoft では、[http://aka.ms/gdprpartners](<http://aka.ms/gdprpartners>) の Microsoft GDPR Data Discovery Toolkit で、分類スキーマの開発と拡張の推奨事項を提供しています。このツールキットでは、オンプレミス データをクラウドに移行するためのアプローチも記述されています。クラウドでは、必要に応じて、より洗練されたデータ ガバナンス機能を使用できます。このセクションの記事では、意図的にオンプレミスのままにするデータに関する推奨事項が示されています。</span><span class="sxs-lookup"><span data-stu-id="3cdf4-p102">Before doing any work with on-premises data, consult with your legal and compliance teams to seek guidance and to learn about existing classification schemas and approaches to working with personal data. Microsoft provides recommendations for developing and extending classifications schemas in the Microsoft GDPR Data Discovery Toolkit at [http://aka.ms/gdprpartners](<http://aka.ms/gdprpartners>). This toolkit also describes approaches for moving on-premises data to the cloud where you can use more sophisticated data governance capabilities, if this is desired. The articles in this section provide recommendations for data that is intended to remain on premises.</span></span>

<span data-ttu-id="3cdf4-p103">次の図に、これらのワークロードそれぞれで、個人データを検出、分類、保護、監視するために使用する推奨機能のリストを示します。詳細については、このセクションの記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cdf4-p103">The following illustration lists recommended capabilities to use across each of these workloads to discover, classify, protect, and monitor personal data. See the articles in this section for more information.</span></span>

![](media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a><span data-ttu-id="3cdf4-119">図の説明</span><span class="sxs-lookup"><span data-stu-id="3cdf4-119">Illustration description</span></span>

<span data-ttu-id="3cdf4-120">見やすいように、次の表では図の例と同じ例を記載しています。</span><span class="sxs-lookup"><span data-stu-id="3cdf4-120">For accessibility, the following table provides the same examples in the illustration.</span></span>

|             |<span data-ttu-id="3cdf4-121">Windows Server ファイル共有</span><span class="sxs-lookup"><span data-stu-id="3cdf4-121">Windows Server file shares</span></span>|<span data-ttu-id="3cdf4-122">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="3cdf4-122">SharePoint Server</span></span>|<span data-ttu-id="3cdf4-123">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="3cdf4-123">Exchange Server</span></span>|<span data-ttu-id="3cdf4-124">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="3cdf4-124">Skype for Business</span></span>|<span data-ttu-id="3cdf4-125">Project Server</span><span class="sxs-lookup"><span data-stu-id="3cdf4-125">Project Server</span></span>|
|:------------|:-------------------------|:----------------|:--------------|:-----------------|:-------------|
|<span data-ttu-id="3cdf4-126">検出</span><span class="sxs-lookup"><span data-stu-id="3cdf4-126">Discover</span></span>|<span data-ttu-id="3cdf4-127">Azure Information Protection スキャナー\*</span><span class="sxs-lookup"><span data-stu-id="3cdf4-127">Azure Information Protection scanner\*</span></span>|<span data-ttu-id="3cdf4-128">検索センターまたは電子情報開示 (データ分類後); Azure Information Protection スキャナー\*</span><span class="sxs-lookup"><span data-stu-id="3cdf4-128">Search Center or eDiscovery (after data is classified); Azure Information Protection scanner\*</span></span>|<span data-ttu-id="3cdf4-129">Exchange 電子情報開示ポータル</span><span class="sxs-lookup"><span data-stu-id="3cdf4-129">Exchange eDiscovery Portal</span></span>|<span data-ttu-id="3cdf4-130">Exchange 電子情報開示ポータル</span><span class="sxs-lookup"><span data-stu-id="3cdf4-130">Exchange eDiscovery portal</span></span>|<span data-ttu-id="3cdf4-131">検出およびエクスポートのための SQL スクリプト</span><span class="sxs-lookup"><span data-stu-id="3cdf4-131">SQL scripts for discovery and exporting</span></span>|
|<span data-ttu-id="3cdf4-132">分類</span><span class="sxs-lookup"><span data-stu-id="3cdf4-132">Classify</span></span>|<span data-ttu-id="3cdf4-133">Azure Information Protection スキャナー\*; Office 365 機密情報タイプ</span><span class="sxs-lookup"><span data-stu-id="3cdf4-133">Azure Information Protection scanner\*; Office 365 sensitive information types</span></span>|<span data-ttu-id="3cdf4-134">Azure Information Protection スキャナー\*; Office 365 機密情報タイプ</span><span class="sxs-lookup"><span data-stu-id="3cdf4-134">Azure Information Protection scanner\*; Office 365 sensitive information types</span></span>|<span data-ttu-id="3cdf4-135">Exchange 保持タグおよびアイテム保持ポリシー</span><span class="sxs-lookup"><span data-stu-id="3cdf4-135">Exchange retention tags and retention policies</span></span>|<span data-ttu-id="3cdf4-136">Exchange 保持タグおよびアイテム保持ポリシー</span><span class="sxs-lookup"><span data-stu-id="3cdf4-136">Exchange retention tags and retention policies</span></span>||
|<span data-ttu-id="3cdf4-137">保護</span><span class="sxs-lookup"><span data-stu-id="3cdf4-137">Protect</span></span>||<span data-ttu-id="3cdf4-138">Exchange Server データ損失防止規則; アクセス許可、ライブラリの IRM 保護</span><span class="sxs-lookup"><span data-stu-id="3cdf4-138">Exchange Server data loss prevention rules; Permissions, IRM-protection for libraries</span></span>|<span data-ttu-id="3cdf4-139">Exchange Server データ損失防止規則; IRM と Exchange Server の統合</span><span class="sxs-lookup"><span data-stu-id="3cdf4-139">Exchange Server data loss prevention rules; IRM integration with Exchange Server</span></span>|||
|<span data-ttu-id="3cdf4-140">監視</span><span class="sxs-lookup"><span data-stu-id="3cdf4-140">Monitor</span></span>|<span data-ttu-id="3cdf4-141">SIEM ツールとのログ統合</span><span class="sxs-lookup"><span data-stu-id="3cdf4-141">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="3cdf4-142">SIEM ツールとのログ統合</span><span class="sxs-lookup"><span data-stu-id="3cdf4-142">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="3cdf4-143">SIEM ツールとのログ統合</span><span class="sxs-lookup"><span data-stu-id="3cdf4-143">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="3cdf4-144">SIEM ツールとのログ統合</span><span class="sxs-lookup"><span data-stu-id="3cdf4-144">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="3cdf4-145">SIEM ツールとのログ統合</span><span class="sxs-lookup"><span data-stu-id="3cdf4-145">Integrate logs with SIEM tools</span></span>|

<span data-ttu-id="3cdf4-p104">\* 保護機能によってファイルが暗号化されることに注意してください。結果として、SharePoint Server では、保護されたファイルの機密情報の種類を検索できなくなります。</span><span class="sxs-lookup"><span data-stu-id="3cdf4-p104">\*Note that protection encrypts the file. Consequently, SharePoint Server can’t find the sensitive information types in protected files.</span></span>