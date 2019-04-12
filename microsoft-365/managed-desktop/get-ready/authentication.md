---
title: Microsoft マネージドデスクトップへのオンプレミスリソースアクセスの準備
description: Azure ad が認証を提供するためにオンプレミスの ad と通信できることを確認するための重要な手順
keywords: microsoft マネージドデスクトップ、microsoft 365、サービス、ドキュメント
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 0f9cbe6712b8d16f435cfdf5fd84875656fa9c2e
ms.sourcegitcommit: ef589025820ddf6edb5f454826b1c12c9bcb8e49
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/11/2019
ms.locfileid: "31824467"
---
#  <a name="prepare-on-premises-resources-access-for-microsoft-managed-desktop"></a>Microsoft マネージドデスクトップへのオンプレミスリソースアクセスの準備

Microsoft マネージドデスクトップでは、デバイスは自動的に Azure Active Directory に参加します。 これは、オンプレミスの active directory を使用している場合に、Azure AD に参加しているデバイスがオンプレミスの active directory と通信できることを確認するために、いくつかのことを確認する必要があることを意味します。 

> [!NOTE]  
> *ハイブリッド*Azure AD join は、Microsoft マネージドデスクトップではサポートされていません。

Azure Active Directory を使用すると、ユーザーはシングルサインオン (SSO) を利用できます。これは、通常、ユーザーが何かを実行するたびに資格情報を提供する必要がないことを意味します。 azure active directory の初めての方は、「 [How to: Plan for azure ad join implementation](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan)」を参照してください。ただし、azure active directory のドキュメントを参照しているため、*ハイブリッド*azure ad join は Microsoft によってサポートされていないことに注意してください。管理されたデスクトップ。


このトピックでは、ローカルの Active Directory 接続に依存するアプリとその他のリソースが、Microsoft マネージドデスクトップで円滑に動作するようにするために確認する必要がある事柄について説明します。


> [!IMPORTANT]  
> ユーザーが Azure Active Directory にデバイスを登録し、Intune に登録できるようにするには、このトピックの残りの部分に進む前に、「[デバイスの設定を構成](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan#configure-your-device-settings)する」の手順に従ってください。


## <a name="single-sign-on-for-on-premises-resources"></a>オンプレミスのリソースのシングルサインオン

UPN またはパスワード (既定の方法) を使用してデバイスのシングルサインオン (SSO) を既定で有効にする必要があります。 ただし、Windows Hello for business を使用することもできます。これには、いくつかのセットアップ手順が必要になります。 sso に関する背景情報については、「Azure AD に参加している[デバイスで sso とオンプレミスのリソースがどのように機能するか](https://docs.microsoft.com/azure/active-directory/devices/azuread-join-sso#how-it-works)」を参照してください。


### <a name="single-sign-on-by-using-upn-and-passwords"></a>UPN とパスワードを使用したシングルサインオン

ユーザーが UPN とパスワードによる認証を行うために特別なセットアップは必要ありません。これは、既定で Azure から取得されます。 ただし、これが正常に動作することを確認するには、次の点を再度確認する必要があります。

- Azure active directory (AAD) Connect が、Windows server 2008 R2 以降を実行しているオンプレミスの Active directory サーバーでセットアップされていることを確認します。
- AAD Connect は、サポートされているバージョンを実行しており、次の3つのキー属性を Azure AD と同期するように設定されています。 
    - ユーザーが社内の Active Directory に存在する DNS ドメイン名
    - ユーザーがオンプレミスの Active Directory に存在する NetBIOS ドメイン名
    - ユーザーの SAM アカウント名


### <a name="sso-by-using-windows-hello-for-business"></a>Windows Hello for business を使用した SSO

または、Windows Hello for business を使用することで、ユーザーにすばやくパスワードを提供することができます。 これを設定するには、「 [Windows Hello for business を使用してオンプレミスのシングルサインオンで Azure AD に参加](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base)しているデバイスを構成する」を参照し、要件を確認してから、そこに示されている手順に従います。


## <a name="apps-and-resources-that-use-authentication"></a>認証を使用するアプリとリソース

azure Active Directory と連携するようにアプリをセットアップするための詳細なガイダンスについては、「azure コンテンツセットの[アプリケーションとリソースに関する考慮事項](https://docs.microsoft.com/azure/active-directory/devices/azureadjoin-plan#understand-considerations-for-applications-and-resources)」を参照してください。 概要:


- Azure AD app gallery に追加されたものなど、**クラウドベースのアプリ**を使用している場合、多くの場合、Microsoft マネージドデスクトップを操作するための準備は必要ありません。 ただし、Web アカウントマネージャー (WAM) を使用していない Win32 アプリでは、認証のためにユーザーに確認を求めることができます。

- **オンプレミスでホスト**されているアプリの場合は、それらのアプリをブラウザーの信頼済みサイトの一覧に追加してください。 これにより、ユーザーが資格情報の入力を求められることなく、Windows 認証がシームレスに動作するようになります。

- Active Directory フェデレーションサービスを使用している場合は、「 [AD FS を使用してシングルサインオンを確認および管理](https://docs.microsoft.com/previous-versions/azure/azure-services/jj151809(v=azure.100))する」の手順に従います。 

- **オンプレミス**のアプリで古いプロトコルを使用する場合、デバイスがオンプレミスのドメインコントローラーにアクセスできる限り、特別なセットアップは必要ありません。 ただし、これらのアプリケーションにセキュリティで保護されたアクセスを提供するには、Azure AD アプリケーションプロキシを展開する必要があります。 詳細については、「 [Azure Active Directory のアプリケーションプロキシを使用したオンプレミスアプリケーションへのリモートアクセス](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy)」を参照してください。

- オンプレミスで実行され、**コンピューター認証に依存**するアプリはサポートされていないため、これらを新しいバージョンに置き換えることを検討する必要があります。

## <a name="network-shares-that-use-authentication"></a>認証を使用するネットワーク共有

デバイスが UNC パスを使用してオンプレミスのドメインコントローラーにアクセスできる限り、ユーザーがネットワーク共有にアクセスするための特別なセットアップは必要ありません。

## <a name="printers"></a>プリンター

プリンターをクラウドのみの環境で自動的に検出することはできませんが、ユーザーはプリンターの UNC パスを使用して直接追加することもできます。

<!--add fuller material on printers when available-->