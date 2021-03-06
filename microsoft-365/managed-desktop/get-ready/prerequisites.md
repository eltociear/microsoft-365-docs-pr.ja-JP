---
title: Microsoft マネージド デスクトップの前提条件
description: ''
keywords: Microsoft マネージドデスクトップ、Microsoft 365、サービス、ドキュメント
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: b6ee70ca577d58661cabee9e2a597b061c4cc190
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43632829"
---
# <a name="prerequisites-for-microsoft-managed-desktop"></a>Microsoft マネージド デスクトップの前提条件

<!--This topic is the target for a "Learn more" link in the Admin Portal (aka.ms/prereq-azure); do not delete.-->
<!--from Prerequisites -->

このトピックでは、Microsoft マネージドデスクトップで成功を保証するために満たす必要のあるインフラストラクチャ要件の概要について説明します。 

Microsoft FastTrack を使用すると、これらの要件を満たし、Microsoft マネージドデスクトップへの参加準備に役立てることができます。 詳細については、「 [Microsoft FastTrack](https://fasttrack.microsoft.com/about)」を参照してください。 

分野 | 前提条件の詳細
--- | ---
ライセンス |Microsoft マネージドデスクトップでは、次のいずれかの Microsoft 365 ライセンス (または同等のライセンス) が必要です。<br>-Microsoft 365 E5<br>-Microsoft 365 E5 セキュリティアドオンを使用した microsoft 365 E3<br><br>Microsoft マネージドデスクトップでの特定のサービスプランおよびその役割の詳細については、このトピックの「[ライセンスの詳細](#more-about-licenses)」を参照してください。<br>利用可能なライセンスの詳細については、「 [Microsoft 365 ライセンス](https://www.microsoft.com/microsoft-365/compare-all-microsoft-365-plans)」を参照してください。
接続 |  すべての Microsoft 管理対象デスクトップデバイスでは、企業ネットワークから多数の Microsoft サービスエンドポイントへの接続が必要です。<br><br>必要な Ip および Url の完全な一覧については、「[ネットワーク構成](../get-ready/network.md)」を参照してください。 
Azure Active Directory |    Azure Active Directory (Azure AD) は、すべてのユーザーアカウントの権限を持つ必要があります。または、サポートされている最新バージョンの Azure AD Connect を使用して、オンプレミスの Active Directory からユーザーアカウントを同期する必要があります。<br><br>[エンタープライズ状態ローミング](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview)は、Microsoft Managed Desktop ユーザーが有効になっている必要があります。<br><br>詳細については、「 [AZURE AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/whatis-azure-ad-connect)」を参照してください。<br><br>サポートされている Azure AD Connect のバージョンの詳細については、「 [AZURE Ad connect: バージョンリリース履歴](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-version-history)」を参照してください。
認証 |    Azure AD がユーザーアカウントの権限元ではない場合は、次のいずれかを Azure AD Connect で構成する必要があります。<br>-パスワードハッシュの同期<br>-パススルー認証<br>-ADFS とのフェデレーション<br><br>Azure AD Connect を使用して認証オプションを設定する場合は、パスワードの書き戻しもお勧めします。 詳細については、「[パスワードの書き戻し](https://docs.microsoft.com/azure/active-directory/authentication/howto-sspr-writeback)」を参照してください。 <br><br>Azure AD での認証オプションの詳細については、「 [AZURE Ad Connect ユーザーのサインインオプション](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-user-signin)」を参照してください。
Microsoft 365 | OneDrive for Business は、Microsoft Managed Desktop ユーザーが有効になっている必要があります。<br><br>Microsoft マネージドデスクトップに登録する必要はありませんが、次のサービスをクラウドに移行することを強くお勧めします。<br>-Email: Exchange 2013 またはそれ以降のオンプレミスで、クラウドベースのメールボックス、Exchange online、または exchange Online ハイブリッドでの構成に移行します。<br>-[ファイルとフォルダー]: OneDrive for Business または SharePoint Online に移行します。<br>-オンラインコラボレーションツール: Teams への移行。
デバイスの管理 | Microsoft マネージドデスクトップデバイスでは、Microsoft Intune を使用した管理が必要です。 Intune は、モバイルデバイス管理機関として設定する必要があります。<br><br>詳細については、「 [Microsoft Intune](https://www.microsoft.com/cloud-platform/microsoft-intune)」を参照してください。 
データのバックアップと復旧 | Microsoft マネージドデスクトップでは、ファイルを OneDrive for business に同期して保護する必要があります。 OneDrive for Business に同期されていないファイルは、Microsoft マネージドデスクトップによって保証されず、デバイスの交換中またはデバイスのリセットが必要な呼び出し中に失われる可能性があります。<br><br>必須ではありませんが、Microsoft Managed Desktop は、マップされたネットワークドライブから適切なクラウドソリューションに移行することを強くお勧めします。 詳細については、「 [Microsoft マネージデスクトップのマップされたドライブの準備](mapped-drives.md)」を参照してください。

Microsoft マネージドデスクトップの使用を開始する準備ができたら、Microsoft アカウントマネージャーにお問い合わせください。 

## <a name="more-about-licenses"></a>ライセンスの詳細

Microsoft マネージドデスクトップでは、機能するために特定のライセンスオプションが必要になります。 これらのオプションは、いくつかのさまざまなライセンスバンドルで利用できます。一部は既に所有している場合があります。 次の表に、Microsoft マネージドデスクトップでのライセンスと、その役割を要約するために必要なオプションを示します。

> [!TIP]
> これらのライセンスオプションを特定のユーザーに割り当てるには、Azure Active Directory の[グループベースのライセンス機能](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal)を活用することをお勧めします。



|ライセンスオプション |これらの*ライセンス製品で利用*可能 |Microsoft マネージドデスクトップでの使用方法|
|-------------|-------------|-------------|
|Azure Active Directory Premium P1     |-Microsoft 365 E5<br>-Microsoft 365 E3 + Microsoft 365 *E5*セキュリティアドオン<br>-Enterprise Mobility + Security E5<br>-Enterprise Mobility + Security E3<br>-Azure Active Directory Premium P1|  Microsoft クラウドサービスへのアクセスを提供します。自動操縦でデバイスを登録できるようにする      |
|Microsoft Intune | -Microsoft 365 E5<br>-Microsoft 365 E3 + Microsoft 365 *E5*セキュリティアドオン<br>-Enterprise Mobility + Security E5<br>-Enterprise Mobility + Security E3<br>-Microsoft Intune  |  デバイスの登録、更新の展開、デバイスの管理に必要       |
|Windows 10 Enterprise  |-Microsoft 365 E5<br>-Microsoft 365 E3 + Microsoft 365 *E5*セキュリティアドオン<br>-Windows 10 Enterprise E3<br>-Windows 10 Enterprise E5 | Windows 10 のエンタープライズ機能を提供します。       |
|Microsoft Defender Advanced Threat Protection | -Microsoft 365 E5<br>-Microsoft 365 E3 + Microsoft 365 *E5*セキュリティアドオン<br>-Windows 10 Enterprise E5<br>-Microsoft Defender Advanced Threat Protection   |  脅威への対応としての検出、監視、アラート、応答を提供します。  |
|エンタープライズ向け Microsoft 365 アプリ  |-Microsoft 365 E5<br>-Microsoft 365 E3<br>-Office 365 E5<br>-Office 365 E3| Office および生産性とコラボレーションツールをアクティブにする    |

> [!TIP]
> Microsoft アカウントマネージャーは、現在のライセンスとサービスプランを確認し、必要な追加ライセンスまたはサービスプランを取得して、重複を回避するために、最も効率的なパスを見つけるのに役立ちます。
