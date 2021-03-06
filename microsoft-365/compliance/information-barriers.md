---
title: 情報バリアについて
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 07/08/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: 情報バリアを使用して、組織内の Microsoft Teams を使用して通信のコンプライアンスを確保します。
ms.openlocfilehash: 344c2b6999a8fd890358a25b39ef3a37abc9ef58
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43636105"
---
# <a name="information-barriers"></a>情報バリア

## <a name="overview"></a>概要

<!--

# Information barriers (click-through test)

## Overview



 [![Click-Through for Information Barriers](./media/information-barriers/clickthrough-information-barriers-thumbnail.png)](./media/information-barriers/clickthrough-information-barriers.pdf)


Click through an overview of Information Barriers: [PDF](./media/information-barriers/clickthrough-information-barriers.pdf) | [PowerPoint](https://github.com/MicrosoftDocs/microsoft-365-docs-pr/raw/Click-Through-Test/microsoft-365/compliance/media/information-barriers/Clickthrough-Information-Barriers.pptx)

OLD: Move comment field here

 [![Click-Through for Information Barriers](./media/information-barriers/Clickthrough_InformationBarriers_Thumbnail.png)](./media/information-barriers/Clickthrough_InformationBarriers.pdf)

For the PowerPoint slide of this Click-Through, click [here](https://github.com/MicrosoftDocs/microsoft-365-docs-pr/raw/Click-Through-Test/microsoft-365/compliance/media/information-barriers/InfoBarriersExample.pptx).

>[!Tip]
>Try this new [Click-Through on information barriers](media/information-barriers/Clickthrough_InformationBarriers.pdf) for a quick overview of the essential facts.
>

--> 


Microsoft クラウドサービスには、強力なコミュニケーションとコラボレーションの機能が含まれています。 しかし、2つのグループ間の通信を制限して、組織内での利息の競合を回避する必要があるとします。 または、内部情報を保護するために、組織内の特定のユーザー間の通信を制限する必要がある場合があります。 Microsoft 365 は、グループと組織間での通信とコラボレーションを可能にするため、必要に応じて特定のユーザーグループ間の通信を制限する方法がありますか。 情報バリアを使用して、できることはありません。 

情報バリアは、Microsoft Teams から展開されるようになっています。 [サブスクリプション](#required-licenses-and-permissions)に情報の障壁が含まれている場合、コンプライアンス管理者または情報バリア管理者は、Microsoft Teams のユーザーグループ間の通信を許可または禁止するポリシーを定義できます。 情報バリアポリシーは、次のような状況で使用できます。

- 営業担当営業グループのユーザーがマーケティングチームと通信することはできません。
- 機密企業情報を扱う財務担当者は、組織内の特定のグループと通信することはできません。
- 組織内の特定のグループに属するユーザーとの通信を、取引先機密資料を含む内部チームに対して行うことはできません。
- 研究チームは、製品開発チームとの通話またはオンラインチャットのみを行います。

> [!IMPORTANT]
> 情報の障壁は、2つの方法の制限***のみをサポート***します。 マーケティングなどの1つの方法の制限は、マーケティングとは通信できませんが、営業***はサポート***されていません。

これらのすべてのシナリオ例 (およびその他) については、Microsoft Teams での通信を禁止または許可するように情報バリアポリシーを定義できます。 このようなポリシーを使用すると、ユーザーが不要な通話やチャットを行うことができなくなり、Microsoft Teams 内の特定のグループとのみ通信できるようになります。 情報バリアポリシーが有効になっていると、そのポリシーの対象となっているユーザーが Microsoft Teams 内の他のユーザーと通信しようとするたびに、チェックが行われて、通信 (情報バリアポリシーによって定義されている) を回避 (または許可) します。 情報の障壁に関するユーザーの作業の詳細については、「 [Microsoft Teams の情報障壁](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)」を参照してください。

> [!IMPORTANT]
> 現時点では、情報バリアは、SharePoint Online または OneDrive を使用した電子メール通信やファイル共有には適用されません。 さらに、情報バリアは、[コンプライアンスの境界](set-up-compliance-boundaries.md)から独立しています。<p>情報バリアポリシーを定義して適用する前に、組織の[Exchange アドレス帳ポリシー](https://docs.microsoft.com/exchange/address-books/address-book-policies/address-book-policies)が有効になっていないことを確認してください。 (情報障壁はアドレス帳ポリシーに基づいています。) 

## <a name="what-happens-with-information-barriers"></a>情報バリアで行われる処理

情報バリアポリシーが設定されている場合、他の特定のユーザーとの通信を行わないユーザーは、それらのユーザーを検索、選択、チャット、または呼び出すことができません。 情報の障壁を使用して、承認されていない通信を防止するためのチェックが行われます。

最初は、情報の障壁は Microsoft Teams のチャットおよびチャネルにのみ適用されます。 Microsoft Teams では、情報バリアポリシーによって、次の種類の承認されていない通信が決定および防止されます。
- ユーザーを検索する
- チームへのメンバーの追加
- 他のユーザーとのチャットセッションの開始
- グループチャットの開始
- 会議への参加を招待する
- 画面の共有
- 電話をかける 

関係する人物が、アクティビティを回避するための情報バリアポリシーに含まれている場合、それらのユーザーは処理を続行できません。 また、情報バリアポリシーに含まれるすべてのユーザーが Microsoft Teams 内の他のユーザーと通信することをブロックする可能性があります。 情報バリアポリシーの影響を受けるユーザーが同じチームまたはグループのチャットに含まれている場合、それらのユーザーはチャットセッションから削除され、グループとの通信が許可されない可能性があります。

情報の障壁に関するユーザーの作業の詳細については、「 [Microsoft Teams の情報障壁](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)」を参照してください。

## <a name="required-licenses-and-permissions"></a>必要なライセンスとアクセス許可

情報バリアは現在ロールアウトされており、次のようなサブスクリプションに含まれています。

- Microsoft 365 E5
- Office 365 E5
- Office 365 Advanced Compliance
- Microsoft 365 E5 情報の保護とコンプライアンス

詳細については、「[コンプライアンスソリューション](https://products.office.com/business/security-and-compliance/compliance-solutions)」を参照してください。

[情報バリアポリシーを定義または編集](information-barriers-policies.md)するには、次のいずれかの役割が割り当てられている必要があります。

- Microsoft 365 グローバル管理者
- Office 365 グローバル管理者
- コンプライアンス管理者
- IB コンプライアンス管理 (新しい役割)

役割とアクセス許可の詳細については、「 [Office 365 セキュリティ & コンプライアンスセンターのアクセス許可](../security/office-365-security/protect-against-threats.md)」を参照してください。

情報バリアポリシーを定義、検証、または編集するには、PowerShell コマンドレットを熟知している必要があります。 [「How to](information-barriers-policies.md)」の記事では PowerShell コマンドレットの例をいくつか示していますが、パラメーターなどの追加の詳細については、組織のために知っておく必要があります。

## <a name="next-steps"></a>次の手順

- [Microsoft Teams の情報障壁の詳細を知る](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

- [情報バリアポリシーに使用できる属性を参照してください。](information-barriers-attributes.md)

- [情報バリアのポリシーを定義する](information-barriers-policies.md)

- [情報バリアポリシーの編集 (または削除)](information-barriers-edit-segments-policies.md) 