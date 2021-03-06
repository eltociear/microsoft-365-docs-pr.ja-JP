---
title: ニュージーランド政府機関向けクラウドコンピューティングのセキュリティとプライバシーに関する考慮事項
description: Microsoft NZ は、ニュージーランドクラウドコンピューティングフレームワークで公開されている質問に対応しています。
keywords: Microsoft 365、コンプライアンス、サービス
localization_priority: None
ms.prod: Microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection: M365-security-compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 3142ce35cdc55e32cf5f40042967ba60de789dcc
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2020
ms.locfileid: "41601884"
---
# <a name="new-zealand-government-cloud-computing-security-and-privacy-considerations"></a>ニュージーランド政府機関向けクラウドコンピューティングのセキュリティとプライバシーに関する考慮事項

## <a name="new-zealand-government-cloud-computing-security-and-privacy-overview"></a>ニュージーランド政府機関向けクラウドコンピューティングのセキュリティとプライバシーの概要

2015年10月に、公的機関による情報技術を使用して、「クラウドファースト」ポリシーを再確定する、改訂された全行政の ICT 戦略を裏書しました。 改定された戦略では、"クラウドコンピューティングのリスクと保証" フレームワーク "を保持しています。これは、NZ 政府機関のチーフ情報責任者 (GCIO) の権限で開発および実装されています。

政府は、クラウドサービスを評価して採用するときに、すべてのニュージーランド状態サービスエージェンシーがこのフレームワーク内で機能することを想定しています。 「クラウドコンピューティングの要件」では、クラウドサービスを採用する際に実行する必要がある機関と、政府機関のクラウドポリシーの概要について概説します。

「クラウドコンピューティング: 情報のセキュリティとプライバシーに関する考慮事項」 (「クラウドコンピューティング ISPC」) というように、GCIO が、潜在的なクラウドソリューションに関して、一貫した堅牢なデューデリジェンスを実現できるようにするために、GCIO が公開しています。 このドキュメントには、データ主権、プライバシー、セキュリティ、ガバナンス、機密性、データの整合性、可用性、およびインシデントの対応と管理に焦点を絞った100の質問が含まれています。 「クラウドコンピューティング IPSC」では、クラウドサービスプロバイダーが公式のコンプライアンスを実証する必要がある、NZ という標準が定義されていないことに注意してください。 ドキュメントで設定されているいくつかの質問については、クラウドサービスプロバイダーがさまざまな関連標準に準拠する方法を理解することが重要であることを示しています。

Microsoft およびニュージーランド政府機関向けのクラウドコンピューティングのセキュリティとプライバシーに関する考慮事項

エージェンシーが Microsoft enterprise cloud services の分析と評価を行うのに役立つように、Microsoft ニュージーランドでは、エンタープライズクラウドサービスが「クラウドコンピューティング ISPC」で設定した質問をどのように解決するかを示す一連のドキュメントが作成されています。Microsoft cloud services が認定されている基準にそれらをリンクします。 これらの認定資格は、Microsoft がクラウドサービスを設計、構築、運用することによって、プライバシーおよびセキュリティリスクを効果的に軽減し、データ主権の懸念事項を解決できるようにすることを中心としています。

Microsoft Cloud での NZ CC フレームワークの利点について説明します。 [NZ cc framework backgrounder をダウンロードし](https://aka.ms/nzcc-framework-backgrounder)てください。

Azure セキュリティおよびコンプライアンスブループリントを使用して、NZ による [CC] フレームワークの展開を促進する方法について説明します。 [azure からの応答を nz にダウンロード](https://gallery.technet.microsoft.com/Response-to-GCIO-Cloud-e117bbb9)します。

## <a name="microsoft-in-scope-cloud-services"></a>対象となる Microsoft のクラウド サービス

- [Azure および Azure Government](https://aka.ms/AzureCompliance)
- [Dynamics 365](https://aka.ms/d365-compliance-list)
- Intune
- Power BI クラウド サービス (スタンドアロン サービス、または Office 365 ブランド プランあるいはスイートに搭載されているサービス)
- [Office 365](https://go.microsoft.com/fwlink/p/?LinkID=2077751)
- Exchange Online、SharePoint Online、Skype for Business Online。 Microsoft NZ は、ホワイトペーパー「 [Office outlook 365: Seemail 統合およびリファレンスアーキテクチャ](https://download.microsoft.com/download/8/5/9/859CDCEE-D293-47D8-9B6A-670B108B48E1/Microsoft_Office_365_white_paper_EN_US.pdf)」で説明されている Exchange Online と seemail を統合するためのリファレンスアーキテクチャを開発するための gcio チームと協力しています。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**フレームワークが適用されるユーザー**

「CIO の義務」の下にある組織: パブリックおよび非パブリックのサービス部門、20個の学区の健康ボード、7つのクラウンエンティティは、クラウドサービスの使用を決定する際に、フレームワークに準拠している必要があります。

**このフレームワークに対する Microsoft の対応を ICT システムの認定プロセスに使用することはできますか?**

事務局が[新ニュージーランド情報セキュリティマニュアル](https://go.microsoft.com/fwlink/p/?linkid=2099496)の下にある ICT システムの認定および認定を行う必要がある場合は、これらの応答を分析の一部として使用できます。

## <a name="resources"></a>リソース

- [海外でホストされている Office プロダクティビティサービスのセキュリティ要件: Office 365 の準拠ガイド](https://aka.ms/o365-gcio-conformance-guidance)
- [ニュージーランドのセキュリティおよびプライバシーに関する要件のコンテキストにおける Microsoft Azure コンプライアンス](https://aka.ms/azurecompliancenewzealand)
- [NZ 政府 ICT 戦略2015](https://www.ict.govt.nz/strategy-and-action-plan/strategy/)
- [クラウドコンピューティングのための NZ 政府の要件](https://aka.ms/NZ-Cloud-Requirements)
- [クラウドコンピューティング: 情報のセキュリティとプライバシーに関する考慮事項 (ISPC)](https://www.digital.govt.nz/standards-and-guidance/technology-and-architecture/cloud-services/)
- [Microsoft オンライン サービス条件](https://aka.ms/Online-Services-Terms)
- [Office 365: SEEMail 統合と参照アーキテクチャ](https://download.microsoft.com/download/8/5/9/859CDCEE-D293-47D8-9B6A-670B108B48E1/Microsoft_Office_365_white_paper_EN_US.pdf)(クラウドサービス導入に関する Microsoft NZ の追加ガイダンス)
- [Microsoft セキュリティ センターのコンプライアンス](https://www.microsoft.com/trust-center/compliance/compliance-overview)

## <a name="microsoft-responses-to-cloud-computing-ipsc"></a>「クラウドコンピューティング IPSC」への Microsoft の応答

- [Azure](https://aka.ms/Azure-NZ-response)
- [Dynamics 365](https://aka.ms/d365-nz-response)
- [Intune](https://aka.ms/Intune-NZ-response)
- [Office 365](https://aka.ms/O365-NZ-Response)
- [Power BI](https://download.microsoft.com/download/5/1/7/51726B9B-2E76-49C4-9D4F-A36BF025CB93/Response-to-GCIO-105-questions-Power-BI.pdf)

## <a name="download-the-offering-backgrounder"></a>サービスの背景解説をダウンロードする

このサービスに関する背景解説をご覧になりたい場合は、 [PDF](https://download.microsoft.com/download/6/6/4/664E4B6F-15C6-421E-8F74-3FA468587A47/NZ_CC_Compliance_Backgrounder.pdf) ファイルをダウンロードできます。
