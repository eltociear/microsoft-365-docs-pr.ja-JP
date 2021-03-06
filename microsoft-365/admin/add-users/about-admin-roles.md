---
title: Microsoft 365 管理センターの管理者ロールについて
f1.keywords:
- CSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: da585eea-f576-4f55-a1e0-87090b6aaa9d
description: 管理者ロールはビジネス機能にマップされ、管理センターで特定のタスクを実行するための権限を付与します。 たとえば、サービス管理者が Microsoft のサポート チケットを開きます。
ms.custom: okr_smb
ms.openlocfilehash: 4e3cec5b2ff86b35d02f8963a584efdb272f2c5e
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43618922"
---
# <a name="about-admin-roles"></a>管理者ロールについて

サブスクリプションには、組織内のユーザーに割り当てることができる管理者ロール セットがあります。 各管理者ロールは、一般的なビジネス機能にマップされ、組織内のユーザーに管理センターで特定のタスクを実行する許可を与えます。 詳細については、「[管理者の役割を割り当てる](assign-admin-roles.md)」を参照してください。

> [!TIP] 
> 役割の詳細な説明をお探しですか ? 「[Azure Active Directory での管理者ロールのアクセス許可](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles)」を確認してください。

## <a name="things-to-consider"></a>考慮事項

管理者は機密データやファイルにアクセスできるため、組織のデータをより安全に保つためにこれらのガイドラインに従うことをお勧めします。

| 推奨事項                  | 重要な理由                 |
| :------------------- | :------------------- |
| 2 〜 4 人のグローバル管理者を配置する  | グローバル管理者のパスワードをリセットできるのは別のグローバル管理者のみであるため、アカウントがロックアウトされた場合に備えて、組織内に少なくとも 2 人のグローバル管理者を配置することをお勧めします。 ただし、グローバル管理者は組織の設定とほとんどのデータにほぼ無制限にアクセスできます。これはセキュリティ上の脅威であるため、グローバル管理者は 4 人を超えて配置しないことをお勧めします。 |
| *制限が最も多い* 役割を割り当てる    | *制限が最も多い* 役割の割り当ては、仕事を完了するために必要なアクセス権のみを管理者に付与することを意味します。 たとえば、従業員のパスワードを誰かにリセットさせたい場合、無制限のグローバル管理者ロールを割り当てるべきではなく、パスワード管理者やヘルプデスク管理者などの制限付き管理者ロールを割り当ててください。これにより、データを安全に保つことができます。                 |
| 管理者に多要素認証 (MFA) を要求する                  |    実際にはすべてのユーザーに対して MFA を要求することをお勧めしますが、管理者は間違いなく MFA を使用してサインインする必要があります。 MFA は、ユーザーが自分が宣言したとおりの人物であることを確認するために、ユーザーに 2 番目の識別方法を入力させます。 管理者は多くの顧客および従業員のデータにアクセスできます。MFA が必要な場合、管理者のパスワードが侵害されたとしても、2 番目の形式の ID がなければパスワードは役に立ちません。  <br><br>MFA を有効にすると、ユーザーが次回サインインするときに、アカウントを回復するための代替のメール アドレスおよび電話番号を提供する必要があります。  <br> [多要素認証をセットアップする](../security-and-compliance/set-up-multi-factor-authentication.md)          |

  
## <a name="some-roles-are-missing-from-active-users--manage-admin-roles-where-did-they-go"></a>[アクティブなユーザー] > [管理者ロールを管理する] に一部の役割がありません。 どこに行ってしまったのでしょうか ?
既定では、最初にほとんどの組織が使用する役割が表示されます。 役割が見つからない場合は、一覧の一番下に移動し、[**See more roles (役割をさらに表示する)**] を選択します。

## <a name="how-can-i-tell-which-permissions-are-assigned-to-me"></a>自分に割り当てられているアクセス許可を確認する方法
管理センターで、設定またはページを編集する許可がないことを通知するメッセージが表示される場合、その許可を持たない役割が割り当てられていることが原因です。

## <a name="what-about-the-azure-active-directory-roles"></a>Azure Active Directory ロールとは 

Azure ポータルには、Microsoft 365 管理センターで使用可能な役割よりも多くの役割があります。 大企業の場合、Azure ポータルに組織のニーズを満たす役割があるかもしれません。

すべての Azure Active Directory ロールの一覧と説明については、「[Azure Active Directory での管理者ロールのアクセス許可](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles)」を参照してください。

Microsoft 365 管理センターまたは Azure ポータルで役割を割り当てても、Windows PowerShell の Azure AD モジュールを使用してロールを割り当てても関係なく、管理者ロールを割り当てられたユーザーが、組織が登録されているクラウド サービスへの同じアクセス レベルを所有します。
  
## <a name="roles-available-in-the-microsoft-365-admin-center"></a>Microsoft 365 管理センターで利用可能な役割

Microsoft 365 管理センターでは、30 を超える Azure AD の役割を管理できます。 ただし、これらの役割は、Azure ポータルで使用可能な役割のサブセットです。

::: moniker range="o365-worldwide"

管理センターで、[**役割**] に移動し、任意の役割を選択して詳細ウィンドウを開きます。 [**アクセス許可**] タブを選択して、実行する許可を持った役割を割り当てられた管理者についての詳細な一覧を表示します。

::: moniker-end

おそらく、組織内で次の役割を割り当てる必要があるだけです。 (役割に関連付けられたコマンドレットなどの詳細については、「[Azure Active Directory での管理者ロールのアクセス許可](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles)」を参照してください。)

|管理者ロール     |誰にこの役割を割り当てるか  |
|---------|---------|
|Exchange 管理者     |   ユーザーのメールボックス、Microsoft 365 グループ、および Exchange Online を表示および管理する必要があるユーザーに Exchange 管理者ロールを割り当てます。 <br><br> Exchange 管理者は、以下のことも実行できます。<br> - ユーザーのメールボックスの削除されたアイテムを復元する <br> - "メールボックス所有者として送信する" 権限および "代理人として送信する" 権限を代理人に付与する <br>  |
|グローバル管理者     |   Microsoft オンライン サービス全体のほとんどの管理機能およびデータへのグローバルなアクセスが必要なユーザーに、グローバル管理者ロールを割り当てます。 <br><br> グローバルなアクセスを多くのユーザーに許可することはセキュリティ上のリスクであるため、2 〜 4 人のグローバル管理者を配置することをお勧めします。 <br><br> グローバル管理者のみが、以下の操作を実行できます。<br> - すべてのユーザーのパスワードをリセットする <br> - ドメインを追加および管理する <br> <br> **注:** Microsoft オンライン サービスにサインアップしたユーザーが、自動的にグローバル管理者になります。 |
|グローバル閲覧者    |   グローバル管理者が表示できる管理センターの管理機能および設定を表示する必要があるユーザーに、グローバル閲覧者ロールを割り当てます。 グローバル閲覧者管理者は、設定を編集できません。   |
|グループ管理者     |   Microsoft 365 管理センターや Azure Active Directory ポータルなど、管理センター全体に渡ってすべてのグループ設定を管理する必要があるユーザーに、グループ管理者ロールを割り当てます。 <br><br> グループ管理者は、以下の操作を実行できます。<br> - Microsoft 365 グループの作成、編集、削除、復元 <br> - グループの作成、有効期限、および名前付けポリシーの作成および更新 <br> - Azure Active Directory セキュリティ グループの作成、編集、削除、復元| 
|ヘルプデスク管理者     |   ヘルプデスク管理者ロールは、以下の操作を行う必要があるユーザーに割り当てます。<br> - パスワードをリセットする <br> - ユーザーを強制的にサインアウトさせる <br> - サービス リクエストを管理する <br> - サービス正常性を監視する <br> <br> **注**: ヘルプデスク管理者は、管理者以外のユーザー、およびディレクトリ閲覧者、ゲスト招待者、ヘルプデスク管理者、メッセージ センター閲覧者、レポート閲覧者の役割に割り当てられたユーザーのみを支援できます。      |
|Office アプリ管理者    |   Office アプリ管理者ロールは、以下の操作を行う必要があるユーザーに割り当てます。 <br> - Office クラウド ポリシー サービスを使用して、Office のクラウドベースのポリシーを作成および管理する <br> - サービス リクエストを作成および管理する <br> - ユーザーの Office アプリに表示される新しいコンテンツを管理する   <br> - サービス正常性を監視する  |
|サービス管理者    |   サービス管理者ロールは追加の役割として、役割に以下の操作が含まれていないものの、以下の操作を行う必要がある管理者またはユーザーに割り当てます。 <br> - サービス リクエストを開いて管理する <br> - メッセージ センターの投稿を表示して共有する   |
|SharePoint 管理者    |   SharePoint 管理者ロールは、SharePoint Online 管理センターにアクセスして管理する必要があるユーザーに割り当てます。 <br><br>SharePoint 管理者は、以下のことも実行できます。 <br> - サイトを作成および削除する <br> - サイト コレクションとグローバル SharePoint 設定を管理する   |
|Teams のサービス管理者    |   Teams のサービス管理者ロールは、Teams 管理センターにアクセスして管理する必要があるユーザーに割り当てます。 <br><br>Teams のサービス管理者は、以下のことも実行できます。 <br> - 会議を管理する <br> - 会議ブリッジを管理する <br> - フェデレーション、Teams のアップグレード、Teams クライアントの設定を含む組織全体にわたる設定を管理する   |
|ユーザー管理者     |    ユーザー管理者ロールは、すべてのユーザーに対して以下の操作を行う必要があるユーザーに割り当てます。 <br> - ユーザーおよびグループを追加する <br> - ライセンスを割り当てる <br> - ほとんどのユーザー プロパティを管理する <br> ユーザー ビューを作成および管理する <br> パスワードの有効期限ポリシーを更新する <br> - サービス リクエストを管理する <br> - サービス正常性を監視する <br><br>  ユーザー管理者は、管理者ではないユーザー、およびディレクトリ閲覧者、ゲスト招待者、ヘルプデスク管理者、メッセージ センター閲覧者、レポート閲覧者の役割が割り当てられているユーザーに対して、以下の操作を行うこともできます。 <br> - ユーザー名を管理する<br> - ユーザーを削除および復元する<br> - パスワードをリセットする <br> - ユーザーを強制的にサインアウトさせる <br> - (FIDO) デバイス キーを更新する   |

### <a name="all-roles"></a>すべての役割

 以下は、Microsoft 365 管理センターで利用可能なすべての管理者ロールの一覧です。

|管理者ロール     |説明  |
|---------|---------|
|アプリケーション管理者     |    エンタープライズ アプリケーション、アプリケーションの登録、およびアプリケーション プロキシ設定へのフル アクセス。     |
|アプリケーション開発者     |    アプリケーションの登録を作成し、自分の代わりにアプリへのアクセスに同意します。     |
|認証管理者     |    ユーザーに対し、MFA などの非パスワード資格情報の認証の再登録を要求できます。     |
|Azure Information Protection 管理者     |   Azure Information Protection ポリシーのラベルを管理し、保護テンプレートを管理し、保護をアクティブ化します。       |
|請求管理者     |    購入、サブスクリプション管理、サービス リクエスト管理、サービス正常性の監視を行います。     |
|クラウド アプリケーション管理者     | エンタープライズ アプリケーション、アプリケーションの登録へのフル アクセス。 アプリケーションプロキシは対象外です。     |
|クラウド デバイス管理者     |    デバイスの有効化、無効化、および削除をし、Windows 10 BitLocker キーを読み取ることができます。     |
|コンプライアンス管理者     |    規制要件および eDiscovery ケースを管理し、場所、ID、アプリのデータ ガバナンスを維持します。     |
|コンプライアンス データ管理者     |    データを追跡し、データが保護されていることを確認し、問題に対する分析情報を取得し、リスクを軽減します。     |
|条件付きアクセス管理者     |   Azure Active Directory の条件付きアクセス設定を管理しますが、Exchange ActiveSync の条件付きアクセス ポリシーは管理しません。      |
|カスタマー ロックボックス アクセス承認者     |      カスタマーロックボックス要求を管理します。カスタマーロックボックスのオンとオフを切り替えることができます。   |
|Desktop Analytics 管理者     |   デスクトップ管理ツールおよびサービスにアクセスし、管理できます。      |
|Dynamics 365 管理者     |  Microsoft Dynamics 365 Online へのフル アクセス。サービス リクエストの管理、サービス正常性の監視を行います。       |
|Exchange 管理者     |  Exchange Online へのフル アクセス。グループの作成および管理、サービス リクエストの管理、およびサービス正常性の監視を行います。    |
|外部 ID プロバイダー管理者    |     直接フェデレーションで使用する ID プロバイダーを構成します。    |
|グローバル管理者     |    すべての管理センターのすべての管理機能およびほとんどのデータに無制限にアクセスできます。     |
|グローバル閲覧者     |    すべての管理センターのすべての管理機能およびほとんどのデータへの読み取り専用アクセス権があります。 この役割のアクセス権および制限の詳細については、「[Azure Active Directory での管理者ロールのアクセス許可](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#global-reader)」を参照してください。    |
|グループ管理者   |グループを作成し、管理センター全体のすべてのグループ設定を管理します。|
|ゲスト招待者     |    Azure Active Directory B2B ゲスト ユーザーの招待を管理します。     |
|ヘルプデスク管理者     | すべての非管理者および一部の管理者ロールのパスワードをリセットして再認証し、サービス リクエストを管理し、サービス正常性の監視を行います。      |
|Intune 管理者     | Intune へのフル アクセス。ユーザーとデバイスの管理によるポリシーの関連付け、グループの作成および管理を行います。      |
|Kaizala 管理者     |    すべての Kaizala 管理機能およびデータへのフル アクセス。サービス リクエストの管理を行います。     |
|ライセンス管理者     |     ユーザーへのライセンスの割り当ておよび削除を行い、ユーザーの使用場所を編集します。    |
|メッセージ センターのプライバシー閲覧者     |    メッセージ センターのデータ プライバシー メッセージへのアクセス。メール通知の取得を行います。     |
|メッセージ センター閲覧者     | メッセージ センターで通常のメッセージの読み取りおよび共有を行い、毎週のメール ダイジェストを取得し、ユーザー、グループ、ドメイン、およびサブスクリプションへの読み取り専用アクセス権を持ちます。     |
|Office アプリ管理者    |   Office のクラウドベース ポリシー、およびユーザーの Office アプリに表示される新しいコンテンツの管理を行います。   |
|Power BI 管理者    |   Power Bl 管理タスクへのフル アクセス。サービス リクエストを管理し、およびサービス正常性の監視を行います。   |
|Power プラットフォーム管理者     |    Microsoft Dynamics 365、PowerApps、データ損失防止ポリシー、および Microsoft Flow へのフル アクセス。     |
|特権ロール管理者     |    役割の割り当て、および Privileged Identity Management のすべてのアクセス制御機能を管理します。     |
|特権認証管理者     |    パスワードのリセットや、パスワード以外の資格情報の更新、強制的サインアウト、サービスの正常性の監視、およびサービス要求の管理を行います。     |
|レポート閲覧者     |   レポート ダッシュボード、PowerBI 導入コンテンツ パック、サインイン レポート、および Microsoft Graph による API のレポートから使用状況レポート データを読み取ります。      |
|検索管理者     |    Microsoft Search へのフル アクセス。検索管理者および検索編集者ロールの割り当て、編集コンテンツの管理、サービス正常性の監視、およびサービス リクエストの作成を行います。     |
|検索編集者     |    ブックマーク、Q＆A、場所など、Microsoft Search のコンテンツの作成、編集、および削除のみができます。     |
|セキュリティ管理者     |    組織のセキュリティの制御、セキュリティ ポリシーの管理、セキュリティ分析およびレポートの確認、脅威の状況の監視を行います。     |
|セキュリティ オペレーター     |    セキュリティの警告の調査および対応、Identity Protection センターの機能の管理、サービス正常性の監視を行います。     |
|セキュリティ閲覧者     |    セキュリティ機能、サインイン レポート、監査ログへの読み取り専用アクセス。     |
|サービス サポート管理者     |    Azure、Microsoft 365、および Office 365 サービスのサービス リクエストの作成、およびサービス正常性の監視を行います。     |
|SharePoint 管理者     |    SharePoint Online へのフル アクセス。Microsoft 365 グループの管理、サービス リクエストの管理、およびサービス正常性の監視を行います。     |
|Skype for Business 管理者     | すべての Teams および Skype 機能、Skype ユーザー属性へのフル アクセス。サービス リクエストの管理、およびサービス正常性の監視を行います。      |
|Teams 管理者     |    Teams および Skype 管理センターへのフル アクセス。Microsoft 365 グループおよびサービス リクエストの管理、およびサービス正常性の監視を行います。     |
|Teams 通信マネージャー     |    電話番号の割り当て、音声および会議ポリシーの作成および管理、通話分析の読み取りを行います。     |
|Teams 通信サポート エンジニア     |    すべての通話参加者の通話レコードの詳細情報を読み取り、通信の問題をトラブルシューティングします。     |
|Teams 通信サポート スペシャリスト     |    特定のユーザーのみのユーザーの通話詳細を読み取り、通信の問題をトラブルシューティングします。|
|ユーザー管理者     |   ユーザー パスワードのリセット、フィルターを含むユーザーとグループの作成と管理、サービス リクエストの管理、およびサービス正常性の監視を行います。|

## <a name="delegated-administration-for-microsoft-partners"></a>Microsoft パートナーの代理管理

Microsoft パートナーと連携している場合、パートナーに管理者ロールを割り当てることができます。 次に、彼らはあなたの会社のユーザーまたはその会社の管理者ロールを割り当てることができます。 たとえば、彼らがあなたのためにオンライン組織をセットアップし管理している場合、彼らにして欲しいのはこれかもしれません。
  
パートナーは、次の役割を割り当てることができます。
  
- パートナー センターを介した多要素認証の管理を除いた、グローバル管理者と同等の特権を持つ完全な管理。
    
- ヘルプデスク管理者と同等の特権を持つ制限付き管理。

パートナーがこれらの役割をユーザーに割り当てる前に、パートナーを代理管理者としてアカウントに追加する必要があります。 このプロセスは認定パートナーによって開始されます。 パートナーは管理者に電子メールを送信し、代理管理者となる権限を割り当てるかどうか質問します。手順については、「[パートナー リレーションシップの承認または削除](https://docs.microsoft.com/microsoft-365/admin/misc/add-partner)」を参照してください。
  
## <a name="related-articles"></a>関連記事

[管理者の役割を割り当てる](assign-admin-roles.md)
  
[Microsoft 365 管理センターのアクティビティ レポート](../activity-reports/activity-reports.md)
