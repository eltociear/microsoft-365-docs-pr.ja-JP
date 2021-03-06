---
title: Microsoft の脅威保護で自動調査を行った後の修復アクション
description: Microsoft の脅威保護で自動化された調査に従う修復アクションの概要を理解する
keywords: 自動化、調査、警告、トリガー、アクション、修復
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: conceptual
ms.custom: autoir
ms.openlocfilehash: ca0c557de24320692d903a1136fc434d635f0507
ms.sourcegitcommit: 58c1b4208a5e231463091573e40696d08fc39b8e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/25/2020
ms.locfileid: "42955593"
---
# <a name="remediation-actions-following-automated-investigations-in-microsoft-threat-protection"></a>Microsoft の脅威保護で自動調査を行った後の修復アクション

**適用対象:**
- Microsoft Threat Protection


## <a name="remediation-actions"></a>修復アクション

Microsoft の脅威保護の自動化された調査の最中および実行後に、修復アクションは悪意のあるアイテムまたは疑わしいアイテムに対して識別されます。 一部の種類の修復アクションは、エンドポイントとも呼ばれるデバイスで実行されます。 その他の修復アクションは、電子メールコンテンツに対して実行されます。 修復アクションが実行、承認、または拒否された後、自動調査が完了します。

次の表に、Microsoft の脅威保護で現在サポートされている修復アクションの概要を示します。 

|デバイス (エンドポイント) の修復アクション  |メールの修復アクション  |
|---------|---------|
|ファイルの検疫<br/>レジストリ キーの削除<br/>プロセスの強制終了 <br/>サービスの停止 <br/>ドライバーの無効化 <br/>スケジュールされたタスクの実行      |メール メッセージまたはクラスターの論理的な削除<br/>URL のブロック (クリック時)<br/>外部メール転送の無効化          |

修復が保留になっているか、既に完了しているかにかかわらず、[アクションセンター](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center)で確認できます。

## <a name="remediation-actions-follow-automated-investigations"></a>修復操作は自動調査に従います。

自動調査が完了すると、関係するすべての証拠について判定が行われ、修復アクションが特定されます。 修復アクションが自動的に実行される場合もあれば、修復アクションが承認を待機する場合もあります。 考えられる判定と結果を次の表に示します。

|判定    |分野    |結果|
|------|------|------|
|Malicious (悪意のある)    |デバイス (エンドポイント)    |修復アクションが自動的に実行されます|
|Malicious (悪意のある)    |メールのコンテンツ (URL または添付ファイル) | 推奨される修復アクションが承認待ちになります|
|Suspicious (不審)    |デバイスまたはメールのコンテンツ |推奨される修復アクションが承認待ちになります|
|脅威なし    |デバイスまたはメールのコンテンツ    |必要な修復アクションはありません|

[保留中のアクションをアクション センターで確認する](mtp-autoir-actions.md#review-a-pending-action-in-the-action-center)

> [!TIP]
> Microsoft の脅威保護の自動化された調査と応答機能によって何かが失敗したか、誤って検出されたと思われる場合は、お知らせください。 [誤検知/ネガを報告](mtp-autoir-report-false-positives-negatives.md)します。

## <a name="next-steps"></a>次の手順

- [アクションを承認または拒否する](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-autoir-actions)

- [アクション センターの詳細](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center)
