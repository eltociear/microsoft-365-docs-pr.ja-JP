---
title: Microsoft 365 分類子 (プレビュー) の概要
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft 365 trainable クラシファイアは、コンテンツのさまざまな種類を認識するために学習することができます。 分類子がトレーニングされ、結果が正確であることを確認したら、それを使用して組織のコンテンツを検索し、それを分類して保持または機密ラベルを適用するか、データ損失防止 (DLP) またはアイテム保持ポリシーに含めることができます。
ms.openlocfilehash: 6b8574b7c87f0b038c46894940cb8d15b152ab5c
ms.sourcegitcommit: 6dfa646b9de30336dedfd0cac7320c57ad74ae11
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "38690656"
---
# <a name="getting-started-with-trainable-classifiers-preview"></a><span data-ttu-id="c00cc-104">トレーニング可能な分類子の使用を開始する (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="c00cc-104">Getting started with trainable classifiers (preview)</span></span>

<span data-ttu-id="c00cc-105">コンテンツを保護し、適切に処理するために、コンテンツの分類とラベル付けを行うことは、情報保護の統制の出発点となります。</span><span class="sxs-lookup"><span data-stu-id="c00cc-105">Classifying and labeling content so it can be protected and handled properly is the starting place for the information protection discipline.</span></span> <span data-ttu-id="c00cc-106">Microsoft 365 には、コンテンツを分類するための3つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="c00cc-106">Microsoft 365 has three ways to classify content.</span></span>

## <a name="manually"></a><span data-ttu-id="c00cc-107">手動</span><span class="sxs-lookup"><span data-stu-id="c00cc-107">Manually</span></span>

<span data-ttu-id="c00cc-108">これには、人間の judgement とアクションが必要です。</span><span class="sxs-lookup"><span data-stu-id="c00cc-108">This requires human judgement and action.</span></span> <span data-ttu-id="c00cc-109">管理者は、既存のラベルと機密情報の種類を使用するか、独自に作成して発行することができます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-109">An admin may either use the pre-existing labels and sensitive information types or create their own and then publish them.</span></span> <span data-ttu-id="c00cc-110">ユーザーおよび管理者は、発生時にコンテンツに適用されます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-110">Users and admins apply them to content as they encounter it.</span></span> <span data-ttu-id="c00cc-111">その後、コンテンツを保護し、廃棄を管理できます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-111">You can then protect the content and manage its disposition.</span></span>

## <a name="automated-pattern-matching"></a><span data-ttu-id="c00cc-112">自動パターンマッチング</span><span class="sxs-lookup"><span data-stu-id="c00cc-112">Automated pattern matching</span></span>

<span data-ttu-id="c00cc-113">この分類機構のカテゴリには、コンテンツの検索が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-113">This category of classification mechanisms includes finding content by:</span></span>

- <span data-ttu-id="c00cc-114">キーワードまたはメタデータ値 (キーワードクエリ言語)</span><span class="sxs-lookup"><span data-stu-id="c00cc-114">keywords or metadata values (keyword query language)</span></span>
- <span data-ttu-id="c00cc-115">ソーシャルセキュリティ、クレジットカード、または銀行口座番号[(機密情報の種類)](what-the-sensitive-information-types-look-for.md)など、以前に識別された機密情報のパターンを使用する</span><span class="sxs-lookup"><span data-stu-id="c00cc-115">using previously identified patterns of sensitive information like social security, credit card or bank account numbers [(sensitive information types)](what-the-sensitive-information-types-look-for.md)</span></span>
- <span data-ttu-id="c00cc-116">テンプレートのバリエーションであるためにアイテムを認識する[(ドキュメントのフィンガープリント)](document-fingerprinting.md)</span><span class="sxs-lookup"><span data-stu-id="c00cc-116">Recognizing an item because it is a variation on a template [(document finger printing)](document-fingerprinting.md)</span></span>
- <span data-ttu-id="c00cc-117">正確な文字列の存在[(正確なデータ一致)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="c00cc-117">using the presence of exact strings [(exact data match)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span></span>

<span data-ttu-id="c00cc-118">機密情報と保持ラベルを自動的に適用して、[データ損失防止 (DLP)](data-loss-prevention-policies.md)と[アイテム保持ポリシー](retention-policies.md)でコンテンツを使用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-118">Sensitivity and retention labels can then be automatically applied that make the content available for use in [data loss prevention (DLP)](data-loss-prevention-policies.md) and [retention policies](retention-policies.md).</span></span>

## <a name="trainable-classifiers"></a><span data-ttu-id="c00cc-119">Trainable 分類子</span><span class="sxs-lookup"><span data-stu-id="c00cc-119">Trainable classifiers</span></span>

<span data-ttu-id="c00cc-120">この分類方法は、その性質によって、手動または自動のパターン一致メソッドによって簡単に識別されないコンテンツに特に適しています。</span><span class="sxs-lookup"><span data-stu-id="c00cc-120">This classification method is particularly well suited to content that, by its nature, isn't predisposed to being easily identified by either the manual or automated pattern matching methods.</span></span> <span data-ttu-id="c00cc-121">この分類の方法は、アイテムに基づいてアイテムを識別する分類子をトレーニングすることになります (アイテムに含まれる要素ではありません) (パターンマッチング)。</span><span class="sxs-lookup"><span data-stu-id="c00cc-121">This method of classification is more about training a classifier to identify an item based on what the item is, not by elements that are in the item (pattern matching).</span></span> <span data-ttu-id="c00cc-122">分類子は、分類するコンテンツの数百の例を参照して、コンテンツの種類を識別する方法を学習します。</span><span class="sxs-lookup"><span data-stu-id="c00cc-122">A classifier learns how to identify a type of content by looking a hundreds of examples of the content you are interested in classifying.</span></span> <span data-ttu-id="c00cc-123">最初に、カテゴリに含まれていることを示す例を示します。その後、それらを処理するときに、一致する例と一致しない例の両方を組み合わせてテストします。</span><span class="sxs-lookup"><span data-stu-id="c00cc-123">You start by feeding it examples that are definitely in the category, then once it processes those, you test it by giving it a mix of both matching and non-matching examples.</span></span> <span data-ttu-id="c00cc-124">その後、分類子は、特定のアイテムが作成しているカテゴリに含まれているかどうかについて予測を行います。</span><span class="sxs-lookup"><span data-stu-id="c00cc-124">The classifier then makes predictions as to whether or not any given item falls into the category you are building.</span></span> <span data-ttu-id="c00cc-125">その後、結果を確認し、陽性、ネガ、偽陽性、誤検知を並べ替えて、予測の精度を高めることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="c00cc-125">You then confirm its results, sorting out the positives, negatives, false positives and false negatives to help increase the accuracy of its predictions.</span></span> <span data-ttu-id="c00cc-126">トレーニング対象の分類子を発行すると、SharePoint Online、Exchange、OneDrive などの場所にあるアイテムを基準に並べ替えられ、コンテンツが分類されます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-126">When you publish the trained classifier, it sorts through items in locations, like SharePoint Online, Exchange, and OneDrive and classifies the content.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c00cc-127">両方の種類の分類子は、条件と[通信のコンプライアンス](communication-compliance.md)[に基づいて、自動適用の保持ラベルポリシー](labels.md#applying-a-retention-label-automatically-based-on-conditions)の条件として使用できます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-127">Both types of classifiers are available as a condition for [auto-apply retention label policy based on a condition](labels.md#applying-a-retention-label-automatically-based-on-conditions) and [Communication compliance](communication-compliance.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c00cc-128">Trainable 分類子は、暗号化されておらず英語になっているアイテムに対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="c00cc-128">Trainable classifiers only work with items that are not encrypted and are in english.</span></span>

## <a name="types-of-classifiers"></a><span data-ttu-id="c00cc-129">分類子の種類</span><span class="sxs-lookup"><span data-stu-id="c00cc-129">Types of classifiers</span></span>

<span data-ttu-id="c00cc-130">分類子と trainable 分類子を使用する準備ができています。</span><span class="sxs-lookup"><span data-stu-id="c00cc-130">There are ready to use classifiers and trainable classifiers.</span></span> <span data-ttu-id="c00cc-131">Trainable クラシファイアを公開された状態にするには、トレーニングに必要な時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="c00cc-131">Getting a trainable classifier to a publishable state requires a time investment to train it.</span></span> <span data-ttu-id="c00cc-132">分類子の使用を開始するために、Microsoft 365 には分類子を使用する準備が整っています。</span><span class="sxs-lookup"><span data-stu-id="c00cc-132">To help you get started using classifiers, Microsoft 365 comes with a few ready to use classifiers.</span></span>

> [!NOTE]
> <span data-ttu-id="c00cc-133">分類とラベル付けワークフローで分類子を使用できるようにするには、その前に、分類の予測が期待どおりになっていることを確認するために、分類に適合していると思われる組織のコンテンツのサンプルに照らしてテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c00cc-133">Before using any ready to use classifier in your classification and labeling workflow, you should test it against a sample of your organizations content that you feel fits the category to verify that its classification predictions meet your expectations.</span></span>

### <a name="understanding-ready-to-use-classifiers"></a><span data-ttu-id="c00cc-134">分類子を使用する準備ができていることを理解する</span><span class="sxs-lookup"><span data-stu-id="c00cc-134">Understanding ready to use classifiers</span></span>

<span data-ttu-id="c00cc-135">Microsoft 365 には、分類子を使用する準備ができました。</span><span class="sxs-lookup"><span data-stu-id="c00cc-135">Microsoft 365 comes with six ready to use classifiers:</span></span>

- <span data-ttu-id="c00cc-136">**不快な言葉**: profanities、slurs、taunts、および偽装式を含むテキストアイテムを検出します。これは、より有害な用語と同じ意味を持つ式です。</span><span class="sxs-lookup"><span data-stu-id="c00cc-136">**Offensive Language**: detects text items which contain profanities, slurs, taunts, and disguised expressions (which are expressions that have the same meaning as a more offensive term).</span></span>
- <span data-ttu-id="c00cc-137">**履歴書**: 申請者の個人、教育、専門資格、作業経験、その他の個人を特定できる情報のテキストアカウントであるアイテムを検出します。</span><span class="sxs-lookup"><span data-stu-id="c00cc-137">**Resumes**: detects items which are textual accounts of an applicant's personal, educational, professional qualifications, work experience and other personally identifying information</span></span>
- <span data-ttu-id="c00cc-138">**SourceCode**: 広く使用されているコンピュータプログラミング言語で記述された命令およびステートメントのセットを含むアイテムを検出します。</span><span class="sxs-lookup"><span data-stu-id="c00cc-138">**SourceCode**: detects items which contain a set of instructions and statements written in widely used computer programming languages.</span></span>
- <span data-ttu-id="c00cc-139">**嫌がらせ**: 次の特徴に基づいて、1人または複数の個人を対象とした不快感のある言語のテキストアイテムの特定のカテゴリを検出します。競合、ethnicity、宗教、国内原産者、性別、性的なオリエンテーション、年齢、障碍。</span><span class="sxs-lookup"><span data-stu-id="c00cc-139">**Harassment**: detects a specific category of offensive language text items related to offensive conduct targeting one or multiple individuals based on the following traits: race, ethnicity, religion, national origin, gender, sexual orientation, age, disability.</span></span>
- <span data-ttu-id="c00cc-140">**不適切な用語**: 多くのユーザーを embarrass する式を含む、不快感を与える言語のテキストアイテムの特定のカテゴリを検出します。</span><span class="sxs-lookup"><span data-stu-id="c00cc-140">**Profanity**: detects a specific category of offensive language text items which contain expressions that embarrass most people</span></span>
- <span data-ttu-id="c00cc-141">**脅威**: 暴力を確定する脅威、または人またはプロパティに物理的な悪影響や損害を与えることに関連する脅威に関連する、不快な言語のテキストアイテムの特定のカテゴリを検出します。</span><span class="sxs-lookup"><span data-stu-id="c00cc-141">**Threat**: detects a specific category of offensive language text items related to threats to commit violence or do physical harm or damage to a person or property</span></span>

<span data-ttu-id="c00cc-142">これらは、 **Microsoft 365 コンプライアンスセンター** > **データ分類 (プレビュー)** > **Trainable 分類子**ビューに、の`Ready to use`状態と共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-142">These appear in the **Microsoft 365 compliance center** > **Data classification (preview)** > **Trainable classifiers** view with the status of `Ready to use`.</span></span>

![分類子-すぐに使用できる分類子](media/classifiers-ready-to-use-classifiers.png)

> [!IMPORTANT]
> <span data-ttu-id="c00cc-144">不快な言葉、嫌がらせ、冒涜、および脅威の分類子は、検索可能なテキストのみで機能することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c00cc-144">Please note that the offensive language, harassment, profanity, and threat classifiers only work with searchable text are not exhaustive or complete.</span></span>  <span data-ttu-id="c00cc-145">さらに、言語と文化的な標準が絶えず変化し、これらの現実からは、これらの分類子を裁量で更新する権利を Microsoft が留保します。</span><span class="sxs-lookup"><span data-stu-id="c00cc-145">Further, language and cultural standards continually change, and in light of these realities, Microsoft reserves the right to update these classifiers in its discretion.</span></span> <span data-ttu-id="c00cc-146">分類子は、お客様の組織が不快な言葉や使用されている他の言語を監視するのに役立ちますが、分類子は、そのような言語の結果に対応していません。そのような言語。</span><span class="sxs-lookup"><span data-stu-id="c00cc-146">While the classifiers may assist your organization in monitoring offensive and other language used, the classifiers do not address consequences of such language and are not intended to provide your organization’s sole means of monitoring or responding to the use of such language.</span></span> <span data-ttu-id="c00cc-147">お客様の組織は、Microsoft またはその子会社ではなく、事前に訓練された分類子によって識別されるコンテンツの監視、実施、ブロック、削除、保持に関連するすべての意思決定に対して責任を負うことになります。</span><span class="sxs-lookup"><span data-stu-id="c00cc-147">Your organization, and not Microsoft or its subsidiaries, remains responsible for all decisions related to monitoring, enforcement, blocking, removal and retention of any content identified by a pre-trained classifier.</span></span>

#### <a name="process-flow-for-using-ready-to-use-classifiers"></a><span data-ttu-id="c00cc-148">分類子を使用する準備完了のプロセスフロー</span><span class="sxs-lookup"><span data-stu-id="c00cc-148">Process flow for using ready to use classifiers</span></span>

<span data-ttu-id="c00cc-149">分類子を使用する準備が整っている必要はありませんが、コンプライアンスソリューションで使用する前に、必要なコンテンツの種類を特定することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c00cc-149">Ready to use classifiers don't need to be trained, but you do need to confirm that they will identify the types of content that you need them to before you use them in compliance solutions.</span></span> <span data-ttu-id="c00cc-150">事前に学習した分類子のテストは、このフローに従います。</span><span class="sxs-lookup"><span data-stu-id="c00cc-150">Testing a pre-trained classifier follows this flow.</span></span>

![事前に学習した分類子をテストするプロセスフロー](media/classifier-pre-trained-classifier-flow.png)

### <a name="understanding-trainable-classifiers"></a><span data-ttu-id="c00cc-152">Trainable 分類子について</span><span class="sxs-lookup"><span data-stu-id="c00cc-152">Understanding trainable classifiers</span></span>

<span data-ttu-id="c00cc-153">使用準備ができている分類子がニーズに合わない場合は、独自の分類子を作成してトレーニングできます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-153">When the ready to use classifiers don't meet your needs, you can create and train your own classifiers.</span></span> <span data-ttu-id="c00cc-154">独自の作成に関しては、非常に多くの作業が行われますが、組織のニーズに合わせてさらに優れた機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-154">There is significantly more work involved with creating your own, but they'll be much better tailored to your organizations needs.</span></span> <span data-ttu-id="c00cc-155">事前に学習された分類子の使用方法の詳細については、「 [use a ready in Use Using クラシファイア](classifier-using-a-ready-to-use-classifier.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c00cc-155">For more detail on how to use a pre-trained classifier, see [Using a ready to use classifier](classifier-using-a-ready-to-use-classifier.md)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c00cc-156">Trainable 分類子を作成したユーザーのみが、その分類子によって行われた予測をトレーニングし、確認することができます。</span><span class="sxs-lookup"><span data-stu-id="c00cc-156">Only the user who creates a trainable classifier can train and review predictions made by that classifier.</span></span>

#### <a name="process-flow-for-creating-trainable-classifiers"></a><span data-ttu-id="c00cc-157">Trainable 分類子を作成するためのプロセスフロー</span><span class="sxs-lookup"><span data-stu-id="c00cc-157">Process flow for creating trainable classifiers</span></span>

<span data-ttu-id="c00cc-158">保持ポリシー、コミュニケーション監督などのコンプライアンスソリューションで使用するための trainable 分類子の作成と発行は、このフローに従います。</span><span class="sxs-lookup"><span data-stu-id="c00cc-158">Creating and publishing a trainable classifier for use in compliance solutions such as retention policies and communication supervision follows this flow.</span></span> <span data-ttu-id="c00cc-159">Trainable 分類子を作成する方法の詳細については、「 [trainable クラシファイアを作成](classifier-creating-a-trainable-classifier.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c00cc-159">For more detail on creating a trainable classifier see, [Creating a trainable classifier](classifier-creating-a-trainable-classifier.md).</span></span>

![プロセスフロー trainable クラシファイア](media/classifier-trainable-classifier-flow.png)

## <a name="see-also"></a><span data-ttu-id="c00cc-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="c00cc-161">See also</span></span>

- [<span data-ttu-id="c00cc-162">保持ラベル</span><span class="sxs-lookup"><span data-stu-id="c00cc-162">retention labels</span></span>](labels.md)
- [<span data-ttu-id="c00cc-163">アイテム保持ポリシー</span><span class="sxs-lookup"><span data-stu-id="c00cc-163">retention policies</span></span>](retention-policies.md)
- [<span data-ttu-id="c00cc-164">データ損失防止 (DLP)</span><span class="sxs-lookup"><span data-stu-id="c00cc-164">data loss prevention (DLP)</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="c00cc-165">機密ラベル</span><span class="sxs-lookup"><span data-stu-id="c00cc-165">sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="c00cc-166">機密情報の種類</span><span class="sxs-lookup"><span data-stu-id="c00cc-166">sensitive information types</span></span>](what-the-sensitive-information-types-look-for.md)
- [<span data-ttu-id="c00cc-167">ドキュメントのフィンガープリント</span><span class="sxs-lookup"><span data-stu-id="c00cc-167">document finger printing</span></span>](document-fingerprinting.md)
- [<span data-ttu-id="c00cc-168">正確なデータ一致</span><span class="sxs-lookup"><span data-stu-id="c00cc-168">exact data match</span></span>](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)