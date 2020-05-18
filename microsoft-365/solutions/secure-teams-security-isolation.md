---
title: セキュリティの分離を使用してチームを構成する
f1.keywords: NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- M365solutions
ms.custom:
- Ent_Solutions
description: セキュリティ固有の秘密度ラベルを使用してチームを作成する方法について説明します。
ms.openlocfilehash: 3af0826e925f2592aaae930200c0f7b8b9865be1
ms.sourcegitcommit: 9c828bc27cd73a1bb85e9fe38d818190025ebb3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2020
ms.locfileid: "44160065"
---
# <a name="configure-a-team-with-security-isolation"></a>セキュリティの分離を使用してチームを構成する

この記事では、Microsoft Teams でプライベート チームを構成し、固有の秘密度ラベルを使用してファイルを暗号化して、チーム メンバーのみがファイルを復号化できるようにするための推奨事項と手順を説明します。

この記事では、プライベート アクセスの他にも、チーム チャネルの [**ファイル**] セクションからアクセスできる関連付けられた SharePoint サイトを構成して厳しく規制されたデータの保存で必要な追加のセキュリティを提供する方法について説明します。

規制の厳しいデータ用にチームを構成する場合の要素は次のとおりです。

- プライベート チーム
- チームに関連付けられた SharePoint サイトでの以下の追加のセキュリティ:
  - サイトのメンバーがサイトを他のユーザーと共有することの防止。
  - サイトのメンバーではないユーザーがサイトへのアクセス権を要求することの防止。
- このチーム専用の秘密度ラベル:
    - 非管理対象デバイスから SharePoint コンテンツにアクセスできないようにする
    - 要求に応じて、チームのゲストアクセスを許可または拒否する
    - ラベルを適用するドキュメントを暗号化する

> [!IMPORTANT]
> この記事の手順に進む前に、「[Microsoft Teams、Office 365 グループ、SharePoint サイトのコンテンツを保護するために秘密度ラベル](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites)を有効にしていることを確認します。

## <a name="initial-protections"></a>初期保護

チームおよび基になる SharePoint サイトへのアクセスを保護するためには、次のベスト プラクティスを確認します。
- [ID とデバイスのアクセス ポリシー](https://docs.microsoft.com/microsoft-365/enterprise/identity-access-policies)
- [SharePoint Online アクセス ポリシー](https://docs.microsoft.com/microsoft-365/enterprise/sharepoint-file-access-policies)。
- [ベースライン保護を使用してチームを展開する](configure-teams-baseline-protection.md)

## <a name="guest-sharing"></a>ゲスト共有

会社の性質に応じて、このチームのゲスト共有を有効または無効にする必要がある場合があります。 チーム内の組織外のユーザーと共同作業する場合は、ゲスト共有を有効にします。 

ゲストと安全に共有する方法の詳細については、次のリソースをご覧ください。

- [組織外のユーザーと共有する場合、ファイルが偶発的に公開されることを制限する](https://docs.microsoft.com/microsoft-365/solutions/share-limit-accidental-exposure)
- [セキュリティで保護されたゲスト共有環境を作成する](https://docs.microsoft.com/microsoft-365/solutions/create-secure-guest-sharing-environment)

ゲスト共有を許可または禁止するには、関連付けられている SharePoint サイトのチーム レベルとサイト レベルの共有コントロールに対して、秘密度ラベルを組み合わせて使用します。

## <a name="create-a-private-team"></a>プライベート チームを作成する

このチーム専用の秘密度ラベルを作成しています。次の手順では、チームを作成します。 既存のチームがある場合は、それを使用できます。

機密情報のチームを作成するには
1. Teams で、アプリの左側にある **[Teams]** をクリックして、チーム リストの下部にある **[チームに参加またはチームの作成]** をクリックします。
2. **[チームの作成]** (最初のカード、左上隅) をクリックします。
3. **[初めからチームを作成する]** を選びます。
4. **[秘密度]**] リストで、既定のままにします。
5. **[プライバシー]** で、**[プライベート]** をクリックします。
6. 機密プロジェクトに関連するチームの名前を入力します。 たとえば、**Project Saturn**。
7. **[作成]** をクリックします。
8. チームにユーザーを追加し、**[閉じる]** をクリックします。

## <a name="private-channel-settings"></a>プライベート チャネルの設定

プライベート チャネルの作成権限をチームの所有者に制限することをお勧めします。

プライベート チャネルの作成を制限するには
1. チームで、**[その他のオプション]** をクリックしてから、**[チームの管理]** をクリックします。
2. **[設定]** タブで、**[メンバーのアクセス許可]** を展開します。
3. **[プライベート チャネルを作成する]** チェック ボックスをオフにします。

[チーム ポリシー](https://docs.microsoft.com/MicrosoftTeams/teams-policies)を使用して、プライベート チャネルを作成できるユーザーを制御することもできます。

## <a name="create-a-sensitivity-label"></a>秘密度ラベルを作成する

チームをセキュリティ分離用に構成するには、このチーム専用に作成された秘密度ラベルを使用します。 このラベルは、ゲスト共有を制御し、非管理対象デバイスからのアクセスを禁止するために、チーム レベルで使用されます。 チームの所有者とメンバーだけが開くことができるように、チーム内の個々のファイルを分類および暗号化するために使用することもできます。

暗号化されたドキュメントを表示できますが、編集することはできない内部のパートナーや関係者のグループがある場合は、閲覧専用のアクセス許可を使用して、ラベルに追加できます。 閲覧者のアクセス許可を持つチームの SharePoint サイトにこれらのユーザーを追加することができます。また、これらのユーザーには、チーム自体ではなく、ドキュメントが保持されるサイトに対する読み取り専用のアクセス権が与えられます。

秘密度ラベルを作成する
1. [Microsoft 365 コンプライアンス センター](https://compliance.microsoft.com)を開きます。
2. **[ソリューション]** で、**[情報保護]** をクリックします。
3. **[ラベルの作成]** をクリックします。
4. チーム名に似たラベルの名前を入力します。 たとえば、**Highly sensitive - Project Saturn** です。
5. ツール ヒントを追加し、**[次へ]** をクリックします。
6. **[暗号化]** ページの **[暗号化]** ドロップダウンで、**[適用]** を選びます。
7. チームのアクセス許可を追加するには:<br>
  a. **[アクセス許可の割り当て]** をクリックします。<br>
  b. **[ユーザーまたはグループの追加]** をクリックして、作成したチームを選択し、**[追加]** をクリックします。<br>
  c.  **[アクセス許可の選択]** をクリックします。<br>
  d.  ドロップダウン リストから **[共同編集者]** を選択し、**[保存]** をクリックします。<br>
8. ラベルを使用してファイルに読み取り専用アクセス権を持つユーザーまたはグループを含める場合は、次の操作を行います。<br>
  a. **[アクセス許可の割り当て]** をクリックします。<br>
  b. **[ユーザーまたはグループの追加]** をクリックして、追加するユーザーまたはグループを選択し、**[追加]** をクリックします。<br>
  c.  **[アクセス許可の選択]** をクリックします。<br>
  d.  ドロップダウン リストから **[閲覧者]** を選択し、**[保存]** をクリックします。<br>
  e.  **[保存]** をクリックします。
9. **[次へ]** をクリックします。
10. このラベルで分類されているファイルにヘッダー、フッター、またはウォーターマークを自動的に追加するには、**[コンテンツのマーキング]** ページで、[コンテンツのマーキング] を有効にします。
11. **[サイトとグループの設定]** ページで、**[サイトとグループの設定]** を **[オン]** に設定します。
12. **[Office 365 グループに接続されているチーム サイトのプライバシー]** ドロップダウンで、**[非公開 - メンバーのみがサイトにアクセス可能]** を選びます。
13. ゲスト アクセスを許可する場合は、**[Ofﬁce 365 グループ所有者が組織外のユーザーをグループに追加できるようにする**] チェック ボックスを選択します。 
14. **[非管理対象デバイス]** で、**[アクセスをブロックする]** を選びます。
15. **[次へ]** をクリックします。
16. **[Office アプリの自動ラベル付け]** ページで、**[次へ]** をクリックします。
17. **[送信]** をクリックしてから、**[完了]** をクリックします。

ラベルを作成したら、それを使用するユーザーに発行する必要があります。 この場合、ラベルをチーム内のユーザーのみが使用できるようにします。

秘密度ラベルを発行する
1. Microsoft 365 コンプライアンス センターまたは **[情報保護]** ページで、**[ラベル ポリシー]** タブを選びます。
2. **[ラベルの発行]** をクリックします。
3. **[発行する秘密度ラベルの選択]** ページで、**[発行する秘密度ラベルの選択]** をクリックします。
4. 作成したラベルを選択し、**[追加]** をクリックします。
5. **[次へ]** をクリックします。
6. [ユーザーとグループに発行] ページで、**[ユーザーとグループの選択]** をクリックします。
7. **[追加]** をクリックし、作成したチームを選びます。
8. **[追加]** をクリックし、**[完了]** をクリックします。
9. **[次へ]** をクリックします。
10. [ポリシーの設定] ページで、**[ユーザーはラベルを削除するか、分類ラベルを下げるために正当な理由を提供する必要がある]** チェック ボックスをオンにし、**[次へ]** をクリックします。
11. ポリシーの名前を入力し、**[次へ]** をクリックします。
12. **[送信]** をクリックしてから、**[完了]** をクリックします。

## <a name="apply-the-label-to-the-team"></a>チームにラベルを適用する

ラベルを発行したら、ゲスト共有および管理対象デバイスの設定を有効にするために、ラベルをチームに適用する必要があります。 この操作は SharePoint 管理センターで行います。 発行後にラベルが使用可能になるまでに、しばらく時間がかかる場合があることに注意してください。

秘密度ラベルを適用する
1. [SharePoint 管理センター](https://admin.microsoft.com/sharepoint)を開きます。
2. **[サイト]** で、**[アクティブなサイト]** をクリックします。
3. チームに関連付けられているサイトをクリックします。
4. **[ポリシー]** タブで、**[秘密度]** の下側にある **[編集]** をクリックします。
5. 作成したラベルを選択し、**[保存]** をクリックします。

## <a name="sharepoint-settings"></a>SharePoint の設定

SharePoint では、次の 3 つの手順を実行します。

- ラベルを作成したときに選択したものと一致するように、SharePoint 管理センターでサイトのゲスト共有設定を更新し、*既存のアクセス権を持つユーザー*に対して、既定の共有リンクを更新します。
- サイト自体の共有設定を更新し、メンバーがファイル、フォルダー、サイトを共有できないようにし、アクセス要求を無効にします。
- 閲覧者アクセス許可を持つラベルにユーザーまたはグループを追加した場合は、それらを読み取りアクセス許可を持つ SharePoint サイトに追加できます。

### <a name="sharepoint-guest-settings"></a>SharePoint ゲストの設定

ラベルを作成したときに選択したゲスト共有設定 (チーム メンバーシップのみに影響します) は、以下のように関連付けられている SharePoint サイトのゲスト共有設定と一致します。

|ラベルの設定|SharePoint サイトの設定|
|:------------|:----------------------|
|**Ofﬁce 365 グループ所有者が組織外のユーザーをグループに追加できるようにする**が選択されている|**新規および既存のゲスト** (新規チームの既定値)|
|**Ofﬁce 365 グループ所有者が組織外のユーザーをグループに追加できるようにする**が選択されていない|**組織内のユーザーのみ**|

また、既定の共有リンクの種類を更新して、意図したよりも広い対象ユーザーにファイルやフォルダーが不用意に共有されるリスクを軽減します。

サイトの設定を更新する
1. [SharePoint 管理センター](https://admin.microsoft.com/sharepoint)を開きます。
2. **[サイト]** で、**[アクティブなサイト]** をクリックします。
3. チームに関連付けられているサイトをクリックします。
4. **[ポリシー]** タブで、**[外部共有]** の下側にある **[編集]** をクリックします。
5. 秘密度ラベルを作成したときにゲスト共有が許可されていた場合は、**[新規および既存のゲスト]** が選択されていることを確認します。 秘密度ラベルを作成したときにゲスト共有が許可されていなかった場合は、**[組織内のユーザーのみ]** を選びます。
6. [既定の共有リンクの種類] で、**[組織レベルの設定と同じ]** チェック ボックスをオフにして、**[既存のアクセス権を持つユーザー]** を選びます。
7. **[保存]** をクリックします。

#### <a name="private-channels"></a>プライベート チャネル

チームにプライベート チャネルを追加する場合、各プライベート チャネルは、既定の共有設定を使用して新しい SharePoint サイトを作成します。 これらのサイトは SharePoint 管理センターでは表示されないので、次のパラメーターと共に [Set-SPOSite](https://docs.microsoft.com/powershell/module/sharepoint-online/set-sposite) PowerShell コマンドレットを使用して、ゲスト共有設定を更新する必要があります。

- `-SharingCapability Disabled` ゲスト共有を無効にするには (既定では有効です)
- `-DefaultSharingLinkType Internal` 既定の共有リンクを*特定のユーザー*に変更するには

チームでプライベート チャネルを使用する予定がない場合は、[[チーム設定]](https://support.microsoft.com/office/ce053b04-1b8e-4796-baa8-90dc427b3acc) の **[メンバーのアクセス許可]** で、チーム メンバーがチームを作成する権限を無効にすることを検討してください。

### <a name="site-sharing-settings"></a>サイト共有設定

SharePoint サイトがチーム メンバーではないユーザーと共有されないようにするには、SharePoint サイトの共有を所有者に制限します。 また、ファイルとフォルダーの共有をチームの所有者に制限します。 これにより、ファイルがチーム外のユーザーと共有されるたびに所有者が認識できます。

所有者のみのサイト共有を構成する
1. Teams で、更新するチームの **[全般]** タブに移動します。
2. チームのツール バーで、**[ファイル]** をクリックします。
3. 省略記号をクリックし、**[SharePoint で開く]** をクリックします。
4. 基となる SharePoint サイトのツール バーで、設定アイコンをクリックしてから、**[サイトの権限]** をクリックします。
5. [サイトの権限] ウィンドウで、**[共有設定]** の **[共有設定の変更]** をクリックします。
6. **[共有アクセス許可]** で、**[サイト所有者のみが、ファイル、フォルダー、およびサイトを共有できます]** を選択して、**[保存]** をクリックします。

### <a name="custom-site-permissions"></a>カスタム サイトのアクセス許可

閲覧者のアクセス許可を持つユーザーを秘密度ラベルに追加した場合は、それらを読み取りアクセス権を持つ SharePoint サイトに追加し、ファイルに簡単にアクセスできます。

サイトにユーザーを追加する
1. サイトの設定アイコンをクリックし、**[サイトの権限]** をクリックします。
2. **[ユーザーの招待]** をクリックして、**[サイトのみ共有]** をクリックします。
3. 招待するユーザーとグループの名前を入力します。
4. 追加するユーザーまたはグループごとに、そのアクセス許可を **[編集]** から **[読み取り]** に変更します。
5. サイトへのリンクを含むメールを送信するかどうかを選びます。
6. **[追加]** をクリックします。

## <a name="additional-protections"></a>追加の保護

Microsoft 365 は、コンテンツを保護するための追加の方法を提供しています。 次のオプションを使用して、組織のセキュリティを強化することを検討してください。

- ゲスト ユーザーを[使用条件](https://docs.microsoft.com/azure/active-directory/conditional-access/terms-of-use)に同意させる。
- ゲストに[セッション タイムアウト ポリシー](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)を設定する。
- [機密情報の種類](https://docs.microsoft.com/microsoft-365/compliance/custom-sensitive-info-types)を作成し、[データ損失防止](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies)を使用して、機密情報にアクセスするポリシーを設定する。
- [Azure Active Directory アクセス](https://docs.microsoft.com/azure/active-directory/governance/access-reviews-overview) レビューを使用して、チームのアクセス権とメンバーシップを定期的に確認する。

## <a name="drive-user-adoption-for-team-members"></a>チーム メンバーのユーザーによる導入を促す

チームを設置したら、このチームの導入とチーム メンバーへの追加のセキュリティを促します。

## <a name="train-your-users"></a>ユーザーをトレーニングする

チームのメンバーは、チームおよびそのすべてのリソース (チャット、会議、およびその他のアプリなど) にアクセスできます。 チャネルの [**ファイル**] セクションにあるファイルで作業をする場合、チームのメンバーは、作成したファイルに秘密度ラベルを割り当てる必要があります。

ラベルがファイルに適用されると、ファイルは暗号化されます。 チームのメンバーは、ファイルを開いてリアルタイムで共同作業を行えます。 ファイルがサイトを離れて悪意のあるユーザーに転送された場合、そのようなユーザーがファイルを開いて内容を表示するには、チーム メンバーのユーザー アカウントの資格情報を入力する必要があります。 

チーム メンバーをトレーニングする:

- SharePoint サイトのチャット、会議、ファイル、その他のリソースに新しいチームを使用することの重要性と、厳しく規制されたデータのリークによって生じる事態 (法的影響、規制上の罰金、ランサムウェア、競争力の低下など)。
- チームにアクセスする方法
- サイトに新しいファイルを作成し、ローカルに保存された新しいファイルをアップロードする方法。
- チームの正しい秘密度ラベルでファイルにラベルを付ける方法。
- ファイルがサイトからリークされてもラベルによって保護されるしくみ。

このトレーニングには、チーム メンバーが上記の機能とその結果を体感できるように、実践的な演習を組み込む必要があります。

### <a name="conduct-periodic-reviews-of-usage-and-address-team-member-feedback"></a>使用状況を定期的にレビューし、チーム メンバーのフィードバックに対処する

トレーニング後の数週間、次のことを行います。

- チーム メンバーのフィードバックに迅速に対応し、ポリシーと構成を微調整します。
- チームの使用状況を分析し、それが期待された使用法と一致しているかを比較する。
- 厳しく規制されたファイルが秘密度ラベルを使用して正しくラベル付けされていることを確認する。 (ラベルが割り当てられているファイルがわかるようにするには、SharePoint のフォルダーを表示し、[**列の追加**] で [**列の表示/非表示**] オプションを使用して [**秘密度**] 列を追加します。)

必要に応じて、ユーザーの再トレーニングを行います。

## <a name="see-also"></a>関連項目

[Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-configure)