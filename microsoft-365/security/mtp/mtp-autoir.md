---
title: Microsoft Threat Protection での自動調査および対応
description: Microsoft Threat Protection での自動調査および対応機能の概要を説明します
keywords: 自動化、調査、警告、トリガー、アクション、修復
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: deniseb
author: denisebmsft
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: conceptual
ms.custom: autoir
ms.openlocfilehash: 8c82c00bb785086da424072581252e6085937921
ms.sourcegitcommit: 8c244b38c43dd00c4ef0102f8bed02ab36639a6b
ms.translationtype: MT + HT Review
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2019
ms.locfileid: "39967910"
---
# <a name="automated-investigation-and-response-air-in-microsoft-threat-protection"></a>Microsoft Threat Protection での自動調査および対応 (AIR)

**適用対象:**
- Microsoft Threat Protection

[!include[Prerelease information](prerelease.md)]

## <a name="your-virtual-analyst"></a>仮想アナリスト

セキュリティ警告がトリガーされた場合、組織のセキュリティ運用チームはこれらの警告を調査し、組織を保護するための手順を実行する必要があります。 警告の優先順位付けと調査には、多くの時間がかかる場合があります。調査実行中に新しい警告が出されるような状況では、この傾向が特に強くなります。 セキュリティ運用チームは、監視および保護を必要とする脅威の膨大さに圧倒されてしまう可能性があります。 

組織のレベル 1 またはレベル 2 のセキュリティ運用チームは、仮想アナリストを使用することができます。 仮想アナリストは、セキュリティ運用チームであれば実行するであろう脅威の調査と修復の最適な手順を模倣して実行します。 仮想アシスタントは、処理能力の制限なしに24時間年中無休で作業することが可能で、調査と脅威の修復を大量に処理することができます。 このような仮想アシスタントを使用すると、対応するまでの時間を大幅に短縮できます。その結果、セキュリティ運用チームでは、その他の重要な戦略的プロジェクトに取り組むための時間的余裕が生まれます。 これは、決して仮定のシナリオではありません。 このような仮想アナリストは、Microsoft Threat Protection スイートの一部として提供されており、*自動調査と対応* (AIR) と呼ばれています。

セキュリティ運用チームは AIR を使用することで、セキュリティの警告やインシデントへの組織の対応能力を大幅に向上させることが可能です。 AIR を使用すると、調査と修復アクションでのコストを削減でき、脅威対策スイートを最大限に活用できます。 セキュリティ運用チームを支援する以下の操作が AIR により実行されます。

1.  脅威に対してアクションを実行する必要があるかどうかの判断。
2.  必要な修復アクションの実行 (または推奨)。
3.  実行する必要がある追加の調査の特定。
4.  必要に応じた、他の警告に対するプロセスの反復。

## <a name="the-automated-investigation-process"></a>自動調査のプロセス

[**Alert (警告)**] > [**incident (インシデント)**] > [**automated investigation (自動調査)**] > [**verdict (判定)**] > [**remediation action (修復アクション)**]

大まかな流れとしては、トリガーされた警告によりインシデントが作成され、これにより自動調査の開始が可能になります。 この調査の結果、1 つまたは複数の修復アクションが実行される可能性があります。 Microsoft Threat Protection では、次の表にまとめたとおり、各自動調査により Azure Advanced Threat Protection (Azure ATP)、Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP)、Office 365 Advanced Threat Protection (Office 365 ATP) の間でシグナルの関連付けが行われます。 

|エンティティ |脅威対策サービス  |
|---------|---------|
|デバイス (エンドポイントとも呼ばれます)     |[Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)<br/>[Azure ATP](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp) |      
|メールの内容 (メールボックス内のファイルとメッセージ)     |[Office 365 ATP](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp)         |


各調査では、調査対象の証拠それぞれについて判定 (*Malicious (悪意のある)*、 *Suspicious (疑わしい)*、または *Clean (クリーン)*) が作成されます。 脅威の種類および出された判定に応じて、修復アクションが自動的に、または組織のセキュリティ運用チームの承認を受けて実行されます。 保留中および完了済みのアクションは、[アクション センター](mtp-action-center.md)に一覧表示されます。

調査の実行中にその他の関連する警告が発生した場合は、それらの警告は調査が完了するまで調査に追加され続けます。 有害なエンティティが別の場所に見つかった場合、そのエンティティを対象に含めるために自動調査の対象範囲が拡大され、全般的なセキュリティのプレイブックが実行されます。 

> [!NOTE]
> すべての警告が自動調査をトリガーするとは限らず、すべての調査が自動化された修復アクションにつながるわけでもありません。これは、組織で AIR がどのように構成されているかにより決まります。 

## <a name="requirements-for-air-in-microsoft-threat-protection"></a>Microsoft Threat Protection の AIR の要件

| | |
|--|--|
|サブスクリプションの要件 |- Microsoft 365 E5 または Microsoft 365 E3 と Identity & Threat Protection<br/>- [Microsoft 365 のプラン](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-overview#plans) を参照してください|
|ネットワーク要件 |- [Azure ATP](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp) がオン<br/>- [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) (MCAS) が構成済み<br/>- [MCAS が Azure ATP と統合済み](https://docs.microsoft.com/cloud-app-security/aatp-integration) |
|Windows コンピューターの要件 |- Windows 10、バージョン 1709 以降がインストール済み (「[Windows 10 リリース情報](https://docs.microsoft.com/windows/release-information/)」を参照してください)<br/>- [Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints) が構成済み <br/>- [Windows Defender ウイルス対策](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-windows-defender-antivirus-features)が構成済み |
|アクセス許可 |- AIR を*構成*するユーザーには、Azure Active Directory ([https://portal.azure.com](https://portal.azure.com)) または Microsoft 365 管理センター ([https://admin.microsoft.com](https://admin.microsoft.com)) のいずれかで、**グローバル管理者**または**セキュリティ管理者**の役割が割り当てられている必要があります。<br/><br/>- AIR の機能を*使用*する方法については、「[アクション センターのタスクに必要なアクセス許可](mtp-action-center.md#required-permissions-for-action-center-tasks)」を参照してください。 |

## <a name="next-steps"></a>次のステップ

- [自動調査と対応に関連するアクションを承認または拒否する](mtp-autoir-actions.md)
- [アクション センターの詳細](mtp-action-center.md)