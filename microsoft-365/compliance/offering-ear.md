---
title: US 輸出管理の規制 (EAR)
description: Microsoft クラウドサービスは、お客様が米輸出管理規則 (EAR) に準拠したコンプライアンス要件を満たし、輸出規制リスクを管理する手助けをしています。
keywords: Microsoft 365、コンプライアンス、オファーリング
localization_priority: None
ms.prod: Microsoft-365-enterprise
ms.topic: article
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection: M365-security-compliance
hideEdit: true
ms.openlocfilehash: 283b6a45807547f9a8d0521cf2c6793a2a15c4d6
ms.sourcegitcommit: 4612c270867c148818eaa4008f45ca793f5d2a2f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/08/2019
ms.locfileid: "38690722"
---
# <a name="compliance-offering-us-export-administration-regulations-ear"></a><span data-ttu-id="78015-104">コンプライアンスオファリング: US Export Administration の規制 (EAR)</span><span class="sxs-lookup"><span data-stu-id="78015-104">Compliance offering: US Export Administration Regulations (EAR)</span></span>

## <a name="about-the-ear"></a><span data-ttu-id="78015-105">イヤーについて</span><span class="sxs-lookup"><span data-stu-id="78015-105">About the EAR</span></span>

<span data-ttu-id="78015-106">米国商務省は、[業界およびセキュリティ (BIS) のビューロー](https://www.bis.doc.gov/)で輸出管理の規則 (イヤー) を適用します。</span><span class="sxs-lookup"><span data-stu-id="78015-106">The US Department of Commerce enforces the Export Administration Regulations (EAR) through the [Bureau of Industry and Security (BIS)](https://www.bis.doc.gov/).</span></span> <span data-ttu-id="78015-107">この耳は、商業および軍事の目的と特定の防衛物の両方で使用できる "デュアルユース" のアイテムを含む、ほとんどの商用商品、ソフトウェア、およびテクノロジの輸出および再輸出に関する制御を幅広く制御し、課しています。</span><span class="sxs-lookup"><span data-stu-id="78015-107">The EAR broadly governs and imposes controls on the export and re-export of most commercial goods, software, and technology, including “dual-use” items that can be used both for commercial and military purposes and certain defense items.</span></span>

<span data-ttu-id="78015-108">BIS ガイダンスでは、データまたはソフトウェアがクラウドにアップロードされるとき、またはユーザーノード間で転送されるときに、クラウドプロバイダーではなく、顧客が "エクスポーター" となり、そのデータまたはソフトウェアの転送、保存、およびアクセスを確実に行うことができるようになります。イヤーに準拠します。</span><span class="sxs-lookup"><span data-stu-id="78015-108">BIS guidance holds that, when data or software is uploaded to the cloud or transferred between user nodes, the customer, not the cloud provider, is the “exporter” who has the responsibility to ensure that transfers of, storage of, and access to that data or software complies with the EAR.</span></span>

<span data-ttu-id="78015-109">[BIS によれ](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)ば、*輸出*とは、保護された技術または技術データを米国内の国外の人物に転送すること (または*エクスポート*とも呼ばれます) を指します。</span><span class="sxs-lookup"><span data-stu-id="78015-109">[According to the BIS](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file), *export* refers to the transfer of protected technology or technical data to a foreign destination or its release to a foreign person in the United States (also referred to as a *deemed export*).</span></span> <span data-ttu-id="78015-110">耳になることは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="78015-110">The EAR broadly governs:</span></span>

- <span data-ttu-id="78015-111">米国からエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="78015-111">Exports from the United States.</span></span>
- <span data-ttu-id="78015-112">元のアイテムと特定の外部元アイテムを再輸出または再転送します。これには、 *minimis*の一部のコンテンツが含まれています。</span><span class="sxs-lookup"><span data-stu-id="78015-112">Re-exports or retransfers of US-origin items and certain foreign-origin items with more than a *de minimis* portion of US-origin content.</span></span>
- <span data-ttu-id="78015-113">他の国から個人に連絡または開示を行います。</span><span class="sxs-lookup"><span data-stu-id="78015-113">Transfers or disclosures to persons from other countries.</span></span>

<span data-ttu-id="78015-114">EAR の対象となるアイテムは、各アイテムに固有の[エクスポート制御分類番号 (ECCN)](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn)が割り当てられている Commerce コントロールリスト (ccl) にあります。</span><span class="sxs-lookup"><span data-stu-id="78015-114">Items subject to the EAR can be found on the Commerce Control List (CCL) where each item is assigned a unique [Export Control Classification Number (ECCN)](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn).</span></span> <span data-ttu-id="78015-115">CCL に記載されていないアイテムは EAR99 として指定されており、ほとんどの EAR99 市販製品ではライセンスをエクスポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="78015-115">Items not listed on the CCL are designated as EAR99 and most EAR99 commercial products will not require a license to be exported.</span></span> <span data-ttu-id="78015-116">ただし、宛先、エンドユーザー、またはアイテムの使用終了によっては、EAR99 アイテムでも、BIS エクスポートライセンスが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="78015-116">However, depending on the destination, end user, or end use of the item, even an EAR99 item may require a BIS export license.</span></span>

<span data-ttu-id="78015-117">2016年6月に公開された[最終的なルール](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)では、サードツーエンドで FIPS 140-2 の検証済み暗号化モジュールを使用して、サードツーエンドで暗号化されていて、故意に軍事によって禁止されていない国またはロシアのフェデレーションに保存されていなかった場合にも、そのことを明確にします</span><span class="sxs-lookup"><span data-stu-id="78015-117">The [final rule](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations), published in June 2016, clarified that EAR licensing requirements also would not apply to the transmission and storage of unclassified technical data and software if they were encrypted end-to-end using FIPS 140-2 validated cryptographic modules and were not intentionally stored in a military-embargoed country or in the Russian Federation.</span></span>

## <a name="microsoft-and-the-ear"></a><span data-ttu-id="78015-118">Microsoft とイヤー</span><span class="sxs-lookup"><span data-stu-id="78015-118">Microsoft and the EAR</span></span>

<span data-ttu-id="78015-119">Microsoft のテクノロジ、製品、およびサービスは、輸出管理の規制 (EAR) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="78015-119">Microsoft technologies, products, and services are subject to the US Export Administration Regulations (EAR).</span></span> <span data-ttu-id="78015-120">EAR のコンプライアンス認定はありませんが、Microsoft Azure、Microsoft Azure Government、および Microsoft Office 365 Government (GCCHigh および DoD 環境) には、お客様にとって、EAR 管理のエクスポートの対象となる重要な機能とツールがあります。リスクを制御し、コンプライアンス要件を満たします。</span><span class="sxs-lookup"><span data-stu-id="78015-120">While there is no compliance certification for the EAR, Microsoft Azure, Microsoft Azure Government, and Microsoft Office 365 Government (GCCHigh and DoD environments) offer important features and tools to help eligible customers subject to the EAR manage export control risks and meet their compliance requirements.</span></span>

<span data-ttu-id="78015-121">この米コマース部門は、Microsoft などのクラウドサービスプロバイダーではなく、顧客データのエクスポーターと見なされるというお客様の地位を獲得しています。</span><span class="sxs-lookup"><span data-stu-id="78015-121">The US Commerce Department, which enforces the EAR, has taken the position that customers, not cloud service providers such as Microsoft, are considered to be exporters of their own customer data.</span></span> <span data-ttu-id="78015-122">ほとんどのお客様のデータは、耳になる輸出規制の対象となる "テクノロジ" または "技術データ" とは見なされませんが、Microsoft の範囲内のクラウドサービスは、お客様が管理し、発生する可能性のある輸出規制リスクを大幅に軽減できるように構造化されています。</span><span class="sxs-lookup"><span data-stu-id="78015-122">While most customer data is not considered “technology” or “technical data” subject to EAR export controls, Microsoft in-scope cloud services are structured to help customers manage and significantly mitigate the potential export control risks they face.</span></span> <span data-ttu-id="78015-123">Microsoft は一般に、対象ユーザーに対して政府機関のクラウドサービスの使用を推奨していますが、排他的ではありません。</span><span class="sxs-lookup"><span data-stu-id="78015-123">Microsoft generally, but not exclusively, recommends the use of its government cloud services for eligible customers.</span></span> <span data-ttu-id="78015-124">適切な計画があれば、お客様は次のツールと独自の内部手順を使用して、輸出規制に関する完全なコンプライアンスを実現できます。</span><span class="sxs-lookup"><span data-stu-id="78015-124">With appropriate planning, customers can use the following tools and their own internal procedures to help ensure full compliance with US export controls.</span></span>

- <span data-ttu-id="78015-125">**データの場所を制御**します。</span><span class="sxs-lookup"><span data-stu-id="78015-125">**Controls on data location**.</span></span> <span data-ttu-id="78015-126">お客様は、データが保存されている場所を確認でき、ストレージを制限する堅牢なツールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="78015-126">Customers have visibility into where their data is stored and access to robust tools to restrict its storage.</span></span> <span data-ttu-id="78015-127">そのため、データを米国内に格納し、管理対象テクノロジまたは技術データを米国外で転送することを最小限に抑えることができます。</span><span class="sxs-lookup"><span data-stu-id="78015-127">They may therefore ensure that their data is stored in the United States and minimize transfer of controlled technology or technical data outside the United States.</span></span> <span data-ttu-id="78015-128">さらに、顧客データは、データが「故意に格納される」というイヤー prohibitions と一致していません。 Azure データセンターは、25か d のいずれかの国またはロシアのフェデレーションにありません。</span><span class="sxs-lookup"><span data-stu-id="78015-128">Furthermore, customer data is not stored in a non-conforming location, consistent with EAR prohibitions on where data is “intentionally stored”: no Azure datacenter is located in any of the 25 Group D:5 countries or the Russian Federation.</span></span>
- <span data-ttu-id="78015-129">**エンドツーエンドの暗号化**。</span><span class="sxs-lookup"><span data-stu-id="78015-129">**End-to-end encryption**.</span></span> <span data-ttu-id="78015-130">耳で指定された物理的な格納場所に対してエンドツーエンドの暗号化セーフハーバーを利用することにより、Microsoft のスコープ内のクラウドサービスは、輸出管理のリスクに対する保護に役立つ暗号化機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="78015-130">By taking advantage of the end-to-end encryption safe harbor for physical storage locations specified in the EAR, Microsoft in-scope cloud services deliver encryption features that can help protect against export control risks.</span></span> <span data-ttu-id="78015-131">また、転送中および保存中の[データを暗号化するためのさまざまなオプション](https://aka.ms/Azure-Encryption-Overview)をお客様に提供します。また、暗号化オプションの中から柔軟に選択できます。</span><span class="sxs-lookup"><span data-stu-id="78015-131">They also offer customers a [wide range of options for encrypting data](https://aka.ms/Azure-Encryption-Overview) in transit and at rest, and the flexibility to choose among encryption options.</span></span>
- <span data-ttu-id="78015-132">**許可されていないエクスポートを防止するためのツールとプロトコル**。</span><span class="sxs-lookup"><span data-stu-id="78015-132">**Tools and protocols to prevent unauthorized deemed export**.</span></span> <span data-ttu-id="78015-133">また、暗号化を使用すると、非 US のユーザーが暗号化されたデータにアクセスしている場合でも、暗号化されたデータを読み取ることができない場合や、データを認識していない場合でも、データの読み取りまたは認識ができない場合には何も表示されません。したがって、制御されたデータの "リリース" はありません。</span><span class="sxs-lookup"><span data-stu-id="78015-133">The use of encryption also helps protect against a potential deemed export (or deemed re-export) under the EAR, because even if a non-US person has access to encrypted data, nothing is revealed if they cannot read or understand the data while it is encrypted; thus there is no “release” of controlled data.</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="78015-134">Microsoft スコープ内クラウドサービス</span><span class="sxs-lookup"><span data-stu-id="78015-134">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="78015-135">Azure および Azure Government</span><span class="sxs-lookup"><span data-stu-id="78015-135">Azure and Azure Government</span></span>](https://aka.ms/AzureCompliance)
- [<span data-ttu-id="78015-136">Office 365 Government (GCC-高および DoD)</span><span class="sxs-lookup"><span data-stu-id="78015-136">Office 365 Government (GCC-High and DoD)</span></span>](https://aka.ms/Office-365-Export-Controls)
- <span data-ttu-id="78015-137">Intune</span><span class="sxs-lookup"><span data-stu-id="78015-137">Intune</span></span>

## <a name="how-to-implement"></a><span data-ttu-id="78015-138">実装方法</span><span class="sxs-lookup"><span data-stu-id="78015-138">How to implement</span></span>

<span data-ttu-id="78015-139">お客様が耳の下での義務を評価するための輸出規制とガイダンスの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="78015-139">Overview of US export controls and guidance for customers assessing their obligations under the EAR.</span></span>

- [<span data-ttu-id="78015-140">Azure</span><span class="sxs-lookup"><span data-stu-id="78015-140">Azure</span></span>](https://aka.ms/Azure-Export-Controls)
- [<span data-ttu-id="78015-141">Office 365</span><span class="sxs-lookup"><span data-stu-id="78015-141">Office 365</span></span>](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a><span data-ttu-id="78015-142">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="78015-142">Frequently asked questions</span></span>

<span data-ttu-id="78015-143">**Microsoft クラウドサービスを使用する際に、輸出規制に準拠するにはどうすればよいですか。**</span><span class="sxs-lookup"><span data-stu-id="78015-143">**What should I do to comply with export controls when using Microsoft cloud services?**</span></span>

<span data-ttu-id="78015-144">この耳では、データが Microsoft クラウドなどのクラウドサーバーにアップロードされるときに、クラウドサービスプロバイダーではなく、データを所有する顧客がエクスポーターと見なされます。</span><span class="sxs-lookup"><span data-stu-id="78015-144">Under the EAR, when data is uploaded to a cloud server such as the Microsoft cloud, the customer who owns the data — not the cloud services provider — is considered to be the exporter.</span></span> <span data-ttu-id="78015-145">そのため、データの所有者 (Microsoft のお客様) は、Microsoft cloud の使用方法を慎重に評価する必要があります。輸出規制を implicate し、使用しているデータやストアに格納されているデータがイヤーにあるかどうかを判断します。、適用される場合は、どのようなコントロールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="78015-145">For that reason, the owner of the data — that is, the Microsoft customer — must carefully assess how their use of the Microsoft cloud may implicate US export controls and determine whether any of the data they want to use or store there may be subject to EAR controls, and if so, what controls apply.</span></span> <span data-ttu-id="78015-146">[Azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)と[Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI)のクラウドサービスを使用して、お客様が輸出規制を完全に遵守できるようにする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="78015-146">Learn more about how [Azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) and [Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) cloud services can help customers ensure their full compliance with US export controls.</span></span>

<span data-ttu-id="78015-147">**マイクロソフトのテクノロジ、製品、サービスは、耳の対象となりますか?**</span><span class="sxs-lookup"><span data-stu-id="78015-147">**Are Microsoft technologies, products, and services subject to the EAR?**</span></span>

<span data-ttu-id="78015-148">ほとんどの Microsoft テクノロジ、製品、およびサービスは、次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="78015-148">Most Microsoft technologies, products, and services either:</span></span>

- <span data-ttu-id="78015-149">は、EAR の対象ではないため、Commerce コントロールリストには含まれず、ECCN もありません。</span><span class="sxs-lookup"><span data-stu-id="78015-149">Are not subject to the EAR and thus are not on the Commerce Control List and have no ECCN;</span></span>
- <span data-ttu-id="78015-150">または、Microsoft による自己分類の対象となる EAR99 または5D992 の大規模な市場を対象としており、ライセンスを必要とせずにライセンスを持たない国にエクスポートすることはできません (NLR)。</span><span class="sxs-lookup"><span data-stu-id="78015-150">Or they are EAR99 or 5D992 Mass Market-eligible for self-classification by Microsoft and may be exported to non-embargoed countries without a license as No License Required (NLR).</span></span>

<span data-ttu-id="78015-151">ということですが、一部の Microsoft 製品には、ライセンスを必要とする場合としない場合がある ECCN が割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="78015-151">That said, a few Microsoft products have been assigned an ECCN that may or may not require a license.</span></span> <span data-ttu-id="78015-152">イヤーまたは法律顧問を参照して、適切なライセンスの種類および輸出目的の国を決定します。</span><span class="sxs-lookup"><span data-stu-id="78015-152">Consult the EAR or legal counsel to determine the appropriate license type and eligible countries for export purposes.</span></span>

<span data-ttu-id="78015-153">**召集 (ITAR) における EAR と国際トラフィックの違いは何ですか?**</span><span class="sxs-lookup"><span data-stu-id="78015-153">**What’s the difference between the EAR and International Traffic in Arms Regulations (ITAR)?**</span></span>

<span data-ttu-id="78015-154">最も広範なアプリケーションを使用した基本的な輸出規制は、同社の米国防省によって管理されるイヤーです。</span><span class="sxs-lookup"><span data-stu-id="78015-154">The primary US export controls with the broadest application are the EAR, administered by the US Department of Commerce.</span></span> <span data-ttu-id="78015-155">この耳は、商業および軍用アプリケーションを含むデュアル使用のアイテムと、純粋に商用アプリケーションのアイテムに適用されます。</span><span class="sxs-lookup"><span data-stu-id="78015-155">The EAR is applicable to dual-use items that have both commercial and military applications, and to items with purely commercial applications.</span></span>

<span data-ttu-id="78015-156">また、米国には、ITAR などの特殊な輸出規制規則もあります。これにより、最も機密性の高いアイテムやテクノロジを制御できます。</span><span class="sxs-lookup"><span data-stu-id="78015-156">The United States also has separate and more specialized export control regulations, such as the ITAR, that governs the most sensitive items and technology.</span></span> <span data-ttu-id="78015-157">米国の州署によって管理され、関連する技術データを含む、多くの軍事、防衛、および諜報部のアイテム (「防衛記事」とも呼ばれる) のエクスポート、一時インポート、再エクスポート、転送に関する制御を行います。</span><span class="sxs-lookup"><span data-stu-id="78015-157">Administered by the US Department of State, they impose controls on the export, temporary import, re-export, and transfer of many military, defense, and intelligence items (also known as “defense articles”), including related technical data.</span></span>

## <a name="resources"></a><span data-ttu-id="78015-158">リソース</span><span class="sxs-lookup"><span data-stu-id="78015-158">Resources</span></span>

- [<span data-ttu-id="78015-159">Microsoft 製品をエクスポートする: 概要</span><span class="sxs-lookup"><span data-stu-id="78015-159">Exporting Microsoft Products: Overview</span></span>](https://www.microsoft.com/exporting/overview.aspx)
- [<span data-ttu-id="78015-160">Microsoft 製品をエクスポートする: よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="78015-160">Exporting Microsoft Products: FAQ</span></span>](https://www.microsoft.com/exporting/faq.aspx)
- [<span data-ttu-id="78015-161">Microsoft 製品のエクスポート: 製品検索</span><span class="sxs-lookup"><span data-stu-id="78015-161">Exporting Microsoft Products: Product Lookup</span></span>](https://www.microsoft.com/exporting/exporting-information.aspx)
- [<span data-ttu-id="78015-162">暗号化に対するエクスポートの制限</span><span class="sxs-lookup"><span data-stu-id="78015-162">Export restrictions on cryptography</span></span>](https://docs.microsoft.com/windows/uwp/security/export-restrictions-on-cryptography)
- [<span data-ttu-id="78015-163">Microsoft および FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="78015-163">Microsoft and FIPS 140-2</span></span>](offering-fips-140-2.md)
- [<span data-ttu-id="78015-164">Microsoft および ITAR</span><span class="sxs-lookup"><span data-stu-id="78015-164">Microsoft and ITAR</span></span>](offering-itar.md)
- [<span data-ttu-id="78015-165">Microsoft セキュリティセンターのコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="78015-165">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)