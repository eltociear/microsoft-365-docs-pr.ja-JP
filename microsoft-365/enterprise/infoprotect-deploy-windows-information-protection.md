---
title: '手順 4: Windows Information Protection の構成する'
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/19/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Microsoft 365 の Windows Information Protection について理解し、展開します。
ms.openlocfilehash: 66c9e10772edb0782096ba120858e895684255b2
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43631647"
---
# <a name="step-4-configure-windows-information-protection"></a>手順 4: Windows Information Protection の構成する

*この手順は省略可能で、Microsoft 365 Enterprise のバージョン E3 および E5 の両方に適用されます*

![フェーズ 6: 情報保護](../media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

個人用デバイスが業務に使用されるようになったことで、アプリやデバイスによって非公開の組織データが漏えいされるリスクが高まっています。 例えば、従業員はソーシャル メディア サイトに将来の製品のマーケティング計画の写真を誤って送信したり、機密性の高い情報を含むファイルをパブリック クラウド ストレージに保存したりします。 

Windows Information Protection (WIP) は、Windows 10 デバイス上のこのようなデータの漏えいを防ぎます。 詳細については、「[WIP を使用してエンタープライズ データを保護する](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)」を参照してください。

Microsoft 365 Enterprise では、WIP は Windows 10 Enterprise と Microsoft Intune を組み合わせたもので、そしてそれは、サブスクリプションに含まれています。 

Microsoft 365 Enterprise を使用して組織に WIP を展開するには、次の手順に従ってください。

1. Windows デバイスを Intune に登録します。 これは、[フェーズ 5: モバイル デバイス管理](mobility-infrastructure.md)で実行する必要があります。
2. [WIP 用の Intune ポリシー](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/create-wip-policy-using-intune-azure)を作成します。
  - 保護アプリのリストに記入してください。
  - WIP の保護レベルを選択します。

[Microsoft Endpoint Configuration Manager](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/overview-create-wip-policy-sccm) で WIPを使用することもできます。 

詳細については、「[WIP のベスト プラクティス]( https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/guidance-and-best-practices-wip)」を参照してください。

中間チェックポイントとして、この手順に対応する[終了条件](infoprotect-exit-criteria.md#crit-infoprotect-step4)を確認してください。

## <a name="next-step"></a>次の手順

|||
|:-------|:-----|
|![手順 5](../media/stepnumbers/Step5.png)|[データ損失防止 (DLP) を構成する](infoprotect-data-loss-prevention.md)|


