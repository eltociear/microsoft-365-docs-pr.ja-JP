---
title: Microsoft マネージドデスクトップアプリの要件
description: ''
keywords: Microsoft マネージドデスクトップ、Microsoft 365、サービス、ドキュメント
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 5889a4e80f44349b4f149ee4f2a631f12b32251e
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43637854"
---
# <a name="microsoft-managed-desktop-app-requirements"></a>Microsoft マネージドデスクトップアプリの要件

<!--This topic is the target for aka.ms/app-req. This is aka link is used from EA agreement for MMD. do not delete.-->

<!--Application addendum -->
 
Microsoft マネージドデスクトップデバイスのパフォーマンス、信頼性、および保守性を保証するために、お客様の基幹業務アプリはエンドユーザーの環境に重大な影響を与えたり、セキュリティの態勢を変更したりする必要がありません。 そのため、Microsoft マネージドデスクトップデバイスに展開する基幹業務アプリケーションは、このトピックの要件を満たしている必要があります。

## <a name="application-condition"></a>アプリケーションの条件

アプリケーションが Microsoft マネージドデスクトップ環境に悪影響を与えることは重要ではありません。 アプリケーションを展開するためにアプリケーションが満たす必要がある要件を次に示します。 特定のアプリケーションまたはドライバーについては、ここに記載されているすべての要件を Microsoft が免除することがあります。 Microsoft は、Microsoft マネージドデスクトップデバイスのパフォーマンスと信頼性に悪影響を及ぼすアプリケーションまたはドライバーを削除することを決定する場合があります。

## <a name="centrally-managed-apps"></a>一元管理されたアプリ

Microsoft 管理デバイスにインストールされているすべてのアプリケーションとドライバーは、Microsoft Intune、Microsoft Store、または Microsoft Store for Business を使用して展開する必要があります。可能であれば、Windows Update サービスを使用してドライバーを展開することもできます。 

## <a name="prohibited-app-classes"></a>禁止されたアプリクラス

Microsoft マネージドデスクトップデバイスでは、特定の種類のアプリケーションが許可されていません。
- サードパーティ製のウイルス対策、セキュリティ、または監査ソフトウェア
- Microsoft Office for enterprise の365以前のバージョンの Microsoft Office
- 他のサードパーティ製ソフトウェアをインストールまたはバンドルするアプリケーション

## <a name="restricted-app-behaviors"></a>制限されたアプリの動作

アプリの動作によっては、ユーザーの環境に悪影響を及ぼす場合や、Microsoft マネージドデスクトップデバイスにセキュリティリスクをもたらす場合があります。 次の動作を持つアプリは、Microsoft に固有のものではなく、Microsoft マネージドデスクトップ環境での実行が許可されていません。

ユーザーの作業状況:
- バックグラウンドサービスをインストールする
- Windows スタートアップパスに自分自身を追加する
- ドライバーに依存するアプリケーション
- サードパーティの web ブラウザー

セキュリティ:
- エンドユーザーの権限を昇格させる
- アプリストアとして機能するか、組み込みの拡張マネージャーを備えている
- 既知のセキュリティの脆弱性
- エンドユーザーデータへのアクセスを暗号化または制限する
- 署名されていないか、信頼できるルートにロールアップしない証明書を使用して署名されている


## <a name="driver-deployment"></a>ドライバーの展開

Microsoft マネージドデスクトップは、Microsoft の管理されたデバイスを使用して Windows Update または受信トレイで利用可能なデバイスドライバーのみをサポートしています。 

アプリケーションで特定のドライバーを実行する必要がある場合は、制限付きアプリケーションと見なされ、Microsoft マネージドデスクトップに展開する前に例外が必要になります。 

