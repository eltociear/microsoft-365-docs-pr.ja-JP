---
title: ATP のアタックシミュレータ
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
description: グローバル管理者は、攻撃シミュレータを使用して、組織内で現実的な攻撃シナリオを実行できます。 これは、実際の攻撃によってビジネスに遭遇する前に、脆弱性のあるユーザーを特定して見つけるのに役立ちます。
ms.openlocfilehash: cac09ed48a46531ea2246f9c3ef798649dc73196
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43638574"
---
# <a name="attack-simulator-in-atp"></a>ATP のアタックシミュレータ

**概要**グローバル管理者またはセキュリティ管理者で、組織に Office 365 Advanced Threat Protection プラン2があり、脅威の[調査および応答機能](office-365-ti.md)が含まれている場合は、攻撃シミュレータを使用して、組織で現実的な攻撃シナリオを実行できます。 これにより、実際の攻撃が収益に影響を与える前に、脆弱なユーザーを特定して検出することができます。 詳細については、この記事をお読みください。

## <a name="what-do-you-need-to-know-before-you-begin"></a>始める前に把握しておくべき情報

- セキュリティ & コンプライアンスセンターを開くには、に<https://protection.office.com/>移動します。 アタックシミュレータは、**脅威管理** \>の**アタックシミュレータ**で利用できます。

  ![脅威管理-アタックシミュレータ](../../media/ThreatMgmt-AttackSimulator.png)

- 異なる Microsoft 365 サブスクリプション間でのアタックシミュレータの可用性の詳細については、「 [Office 365 Advanced Threat Protection サービスの説明](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)」を参照してください。

- **組織の管理**または**セキュリティ管理者**の役割グループのメンバーである必要があります。 セキュリティ & コンプライアンスセンターの役割グループの詳細については、「[セキュリティ & コンプライアンスセンターのアクセス許可](permissions-in-the-security-and-compliance-center.md)」を参照してください。

- アタックシミュレータでキャンペーンを作成および管理するには、アカウントが多要素認証 (MFA) 用に構成されている必要があります。 手順については、「[多要素認証をセットアップ](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication)する」を参照してください。

攻撃が正常に開始されるようにするには、シミュレートされた攻撃の実行に使用しているアカウントが多要素認証を使用していることを確認してください。 さらに、全体管理者またはセキュリティ管理者である必要があります。 役割とアクセス許可の詳細については、「[セキュリティ & コンプライアンスセンターのアクセス許可](permissions-in-the-security-and-compliance-center.md)」を参照してください。

- フィッシングキャンペーンは、30日間、イベントを収集して処理します。 キャンペーンを開始した後、過去90日間は過去のキャンペーンデータを利用できるようになります。

- アタックシミュレータに対応する PowerShell コマンドレットはありません。

## <a name="spear-phishing-campaigns"></a>スピアーフィッシングキャンペーン

*フィッシング*とは、正規または信頼された送信者からのメッセージで機密情報を盗もうとする電子メール攻撃の一般的な用語です。 *スピアーフィッシング*は、対象となる受信者に特化した、非常に集中的でカスタマイズされたコンテンツ (通常は、攻撃者による受信者の偵察後) を使用する、対象となるフィッシング攻撃です。

- グローバル管理者またはセキュリティ管理者

アタックシミュレータでは、2つの異なる種類のスピアーフィッシングキャンペーンを利用できます。

- 少なくとも、グローバル管理者アカウントと、アタックシミュレータを使用するセキュリティ管理者に対して、[多要素認証/条件付きアクセス](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication)が有効になっています。 (理想的には、組織内のすべてのユーザーに対して多要素認証/条件付きアクセスが有効になっています)。

  - これについて説明する既定のページはテストのみで、フィッシングメッセージを認識するためのヒントを示します。

    ![ユーザーがフィッシングリンクをクリックして資格情報を入力した場合に表示されること](../../media/attack-simulator-phishing-result.png)

  - 指定するカスタムページ (URL)。

- **スピアーフィッシング (添付ファイル)**: 攻撃により、受信者がメッセージ内の .docx または .pdf 添付ファイルを開くように誘導しようとします。 添付ファイルには、既定のフィッシングリンクと同じコンテンツが含まれていますが\<、最初\>の文の先頭には "表示名があります。このメッセージは、最近使用した電子メールメッセージとして表示されています..."。

> [!NOTE]
> 現時点では、アタックシミュレータのスピアーフィッシングキャンペーンは期限切れになりません。

### <a name="create-a-spear-phishing-campaign"></a>スピアーフィッシングキャンペーンを作成する

スピアーフィッシングキャンペーンの重要な部分は、対象の受信者に送信される電子メールメッセージのルックアンドフィールです。 電子メールメッセージを作成して構成するには、次のオプションがあります。

- **組み込みの電子メールテンプレートを使用**する: 2 つの組み込みテンプレートを利用できます: [**賞品 Giveaway** ] および [**給与の更新**]。 キャンペーンを作成および開始するときに、テンプレートから、電子メールのプロパティをいくつか、すべて、またはまったくカスタマイズすることができます。

- **再利用可能な電子メールテンプレートを作成**する: 電子メールテンプレートを作成して保存すると、今後のスピアーフィッシングキャンペーンで使用できるようになります。 キャンペーンを作成および開始するときに、テンプレートから、電子メールのプロパティをいくつか、すべて、またはまったくカスタマイズすることができます。

- **ウィザードで電子メールメッセージを作成**する: スピアーフィッシングキャンペーンを作成して起動すると、ウィザードで直接電子メールメッセージを作成できます。

#### <a name="step-1-optional-create-a-custom-email-template"></a>手順 1 (省略可能): カスタム電子メールテンプレートを作成する

組み込みのテンプレートのいずれかを使用する場合、またはウィザードで直接電子メールメッセージを作成する場合は、この手順を省略できます。

1. セキュリティ & コンプライアンスセンターで、[**脅威管理** \> ] [**アタックシミュレータ**] に移動します。

2. [**アタックのシミュレート**] ページの [**スピアーフィッシング (資格情報のハーベスト)** ] セクションまたは [**スピアーフィッシング (添付ファイル)** ] セクションで、[アタックの**詳細**] をクリックします。

   テンプレートを作成する場所は重要ではありません。 テンプレートで使用可能なオプションは、どちらの種類のフィッシング攻撃でも同じです。

3. 開かれた [**アタックの詳細**] ページの [**フィッシングテンプレート**] セクションで、[**テンプレートの作成**] 領域の [**新しいテンプレート**] をクリックします。

4. 新しいポップアップで [**フィッシングテンプレートの構成**] ウィザードが起動します。 [**開始**] ステップに、テンプレートの一意の表示名を入力し、[**次へ**] をクリックします。

5. [**電子メールの詳細の構成**] ステップで、次の設定を構成します。

   - **From (名前)**: メッセージの送信者に使用する表示名を指定します。

   - **From (電子メール)**: 送信者の電子メールアドレス。

   - [**フィッシングログインサーバーの URL**]: ドロップダウンをクリックし、一覧から使用可能な url のいずれかを選択します。 これは、ユーザーがクリックしたくなる URL です。 3 つの選択肢は次のものです。

     - <http://portal.docdeliveryapp.com>
     - <http://portal.docdeliveryapp.net>
     - <http://portal.docstoreinternal.com>
     - <http://portal.docstoreinternal.net>
     - <http://portal.hardwarecheck.net>
     - <http://portal.hrsupportint.com>
     - <http://portal.payrolltooling.com>
     - <http://portal.payrolltooling.net>
     - <http://portal.prizegiveaway.net>
     - <http://portal.prizesforall.com>
     - <http://portal.salarytoolint.com>
     - <http://portal.salarytoolint.net>

     > [!NOTE]
     > <ul><li>すべての Url は、https ではなく、意図的に http になっています。</li><li>URL 評価サービスでは、これらの Url の1つ以上が安全でないと識別されることがあります。 フィッシングキャンペーンで URL を使用する前に、サポートされている web ブラウザーで URL の可用性を確認してください。</li></ul>

   - **ユーザー設定のランディングページの URL**: ユーザーがフィッシングリンクをクリックして資格情報を入力した場合に実行される、オプションのランディングページを入力します。 このリンクにより、既定のランディングページが置き換えられます。 たとえば、社内の認識トレーニングがある場合は、その URL をここで指定できます。

   - **Category**: 現在、この設定は使用されていません (入力した内容はすべて無視されます)。

   - **Subject**: 電子メールメッセージの**件名**フィールド。

   完了したら、**[次へ]** をクリックします。

6. [**電子メールの作成**] ステップで、電子メールメッセージの本文を作成します。 [**電子メール**] タブ (リッチ html エディター) または [**ソース**] タブ (生の html コード) を使用できます。

   必要に応じて、HTML 形式を単純にすることも複雑にすることもできます。 受信者の電子メールクライアントでのメッセージの believability を向上させるために、画像とテキストを挿入することができます。

   - `${username}`受信者の名前を挿入します。

   - `${loginserverurl}`前の手順で検出された**フィッシングログインサーバーの URL**値を挿入します。

   完了したら、**[次へ]** をクリックします。

7. [**確認**] ステップで、[**完了**] をクリックします。

#### <a name="step-2-create-and-launch-the-spear-phishing-campaign"></a>手順 2: スピアーフィッシングキャンペーンを作成して起動する

1. セキュリティ & コンプライアンスセンターで、[**脅威管理** \> ] [**アタックシミュレータ**] に移動します。

2. [**アタックのシミュレート**] ページで、作成するキャンペーンの種類に応じて、次のいずれかの選択を行います。

   - [**スピアーフィッシング (資格情報のハーベスト)** ] セクションで、[**アタックの起動**] をクリックするか、[**アタックの詳細** \>の**起動攻撃**] をクリックします。

   - [**スピアーフィッシング (添付ファイル)** ] セクションで、[**アタックの起動**] をクリックするか、[**アタックの詳細** \>を**起動**する] をクリックします。

3. 新しいポップアップで [**フィッシング攻撃の構成**] ウィザードが開始されます。 **開始**ステップで、次のいずれかの手順を実行します。

   - [**名前**] ボックスに、キャンペーンの一意の表示名を入力します。 後でウィザードで電子メールメッセージを作成するので、[**テンプレートの使用**] をクリックしないでください。

   - [**テンプレートを使用する**] をクリックし、組み込みまたはカスタムの電子メールテンプレートを選択します。 テンプレートを選択すると、テンプレートに基づいて [**名前**] ボックスに自動的に入力されますが、名前を変更することもできます。

   ![フィッシング開始ページ](../../media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)

   完了したら、**[次へ]** をクリックします。

4. [**ターゲット受信者**] ステップで、次のいずれかの手順を実行します。

   - [**アドレス帳**] をクリックして、キャンペーンの受信者 (ユーザーまたはグループ) を選択します。 対象となる受信者ごとに、Exchange Online メールボックスが必要です。 検索条件を入力せずに [**フィルター**と**適用**] をクリックすると、すべての受信者が返されてキャンペーンに追加されます。

   - [**インポート**]、[**ファイルのインポート**] の順にクリックして、電子メールアドレスのコンマ区切り値 (CSV) または行区切りのファイルをインポートします。 各行には、受信者の電子メールアドレスが含まれている必要があります。

   完了したら、**[次へ]** をクリックします。

5. [**電子メールの詳細の構成**] ステップで、次の設定を構成します。

   **開始**ステップでテンプレートを選択した場合、これらの値のほとんどは既に構成されていますが、変更できます。

   - **From (名前)**: メッセージの送信者に使用する表示名を指定します。

   - **From (電子メール)**: 送信者の電子メールアドレス。 組織の電子メールドメインから本物または偽の電子メールアドレスを入力することも、本物または偽の外部電子メールアドレスを入力することもできます。 組織からの有効な送信者の電子メールアドレスは、受信者の電子メールクライアントで実際に解決されます。

   - [**フィッシングログインサーバーの URL**]: ドロップダウンをクリックし、一覧から使用可能な url のいずれかを選択します。 これは、ユーザーがクリックしたくなる URL です。 3 つの選択肢は次のものです。

     - <http://portal.docdeliveryapp.com>
     - <http://portal.docdeliveryapp.net>
     - <http://portal.docstoreinternal.com>
     - <http://portal.docstoreinternal.net>
     - <http://portal.hardwarecheck.net>
     - <http://portal.hrsupportint.com>
     - <http://portal.payrolltooling.com>
     - <http://portal.payrolltooling.net>
     - <http://portal.prizegiveaway.net>
     - <http://portal.prizesforall.com>
     - <http://portal.salarytoolint.com>
     - <http://portal.salarytoolint.net>

     > [!NOTE]
     > <ul><li>すべての Url は、https ではなく、意図的に http になっています。</li><li>URL 評価サービスでは、これらの Url の1つ以上が安全でないと識別されることがあります。 フィッシングキャンペーンで URL を使用する前に、サポートされている web ブラウザーで URL の可用性を確認してください。</li><li>URL を選択する必要があります。 <b>スピアーフィッシング (添付)</b>キャンペーンの場合は、次の手順でメッセージの本文からリンクを削除できます (それ以外の場合、メッセージにはリンク<b>と</b>添付ファイルの両方が含まれます)。</li></ul>

   - **添付ファイルの種類**: この設定は、**スピアーフィッシング (添付ファイル)** キャンペーンでのみ使用できます。 ドロップダウンをクリックし、[] を選択し**ます。.DOCX**また**は**リストから PDF を表示します。

   - [**添付ファイル名**]: この設定は、**スピアーフィッシング (添付ファイル)** キャンペーンでのみ使用できます。 .Docx または .pdf 添付ファイルのファイル名を入力します。

   - **ユーザー設定のランディングページの URL**: ユーザーがフィッシングリンクをクリックして資格情報を入力した場合に実行される、オプションのランディングページを入力します。 このリンクにより、既定のランディングページが置き換えられます。 たとえば、社内の認識トレーニングがある場合は、その URL をここで指定できます。

   - **Subject**: 電子メールメッセージの**件名**フィールド。

   完了したら、**[次へ]** をクリックします。

6. [**電子メールの作成**] ステップで、電子メールメッセージの本文を作成します。 **開始**手順でテンプレートを選択した場合、メッセージ本文は既に構成されていますが、カスタマイズできます。 [**電子メール**] タブ (リッチ html エディター) または [**ソース**] タブ (生の html コード) を使用できます。

   必要に応じて、HTML 形式を単純にすることも複雑にすることもできます。 受信者の電子メールクライアントでのメッセージの believability を向上させるために、画像とテキストを挿入することができます。

   - `${username}`受信者の名前を挿入します。

   - `${loginserverurl}`[**フィッシングログインサーバーの URL**の値を挿入します。

   **スピアーフィッシング (添付)** キャンペーンの場合は、メッセージの本文からリンクを削除する必要があります (それ以外の場合、メッセージにはリンク**と**添付ファイルの両方が含まれ、リンククリックは添付ファイルキャンペーンで追跡されません)。

   ![電子メール本文の作成](../../media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)

   完了したら、**[次へ]** をクリックします。

7. [**確認**] ステップで、[**完了**] をクリックしてキャンペーンを開始します。 フィッシングメッセージは、対象の受信者に配信されます。

## <a name="password-attack-campaigns"></a>パスワード攻撃キャンペーン

*パスワード攻撃*は、組織内のユーザーアカウントのパスワードを推測しようと試みます。通常、攻撃者が1つ以上の有効なユーザーアカウントを識別した後。

アタックシミュレータでは、2つの異なる種類のパスワード攻撃キャンペーンを使用して、ユーザーのパスワードの複雑さをテストできます。

- **ブルートフォースパスワード (辞書攻撃)**:*ブルートフォース*または*辞書*攻撃では、ユーザーアカウントのパスワードの大規模な辞書ファイルが使用されます。これは、1つのアカウントに対して多数のパスワードを使用することを望んでいます。 パスワードのロックアウトが正しくないと、ブルートフォースパスワード攻撃を防ぐことができます。

  辞書攻撃の場合、1つまたは複数のパスワードを指定して (手動で入力またはアップロードされたファイルで)、1人または複数のユーザーを指定できます。

- **パスワードのスプレー攻撃**:*パスワードのスプレー*攻撃では、ユーザーアカウントの一覧と同じように慎重にパスワードを使用します (1 つのパスワードを複数のアカウントに対して使用します)。 パスワードのスプレー攻撃は、ブルートフォースパスワード攻撃よりも検知するのは困難です (攻撃者が、ユーザーの誤ったパスワードロックアウトを防ぐリスクなしに、1つまたは数百のアカウントに対して1つのパスワードを試行したときに成功する可能性が高くなります)。

  パスワードのスプレー攻撃では、1つのパスワードのみを指定して、1人または複数のユーザーを指定できます。

> [!NOTE]
> アタックシミュレータのパスワード攻撃は、エンドポイントにユーザー名とパスワードの基本的な認証要求を渡すので、他の認証方法 (AD FS、パスワードハッシュ同期、パススルー、Ping フェデレーションなど) でも動作します。 MFA が有効になっているユーザーは、パスワード攻撃が実際のパスワードを試行しても、常にエラーとして登録されます (つまり、MFA ユーザーがキャンペーンの**成功試行**回数に表示されることはありません)。 これは予想される結果です。 MFA は、パスワード攻撃から保護するための主要な方法です。

### <a name="create-and-launch-a-password-attack-campaign"></a>パスワード攻撃キャンペーンを作成および開始する

1. セキュリティ & コンプライアンスセンターで、[**脅威管理** \> ] [**アタックシミュレータ**] に移動します。

2. [**アタックのシミュレート**] ページで、作成するキャンペーンの種類に応じて、次のいずれかの選択を行います。

   - [**ブルートフォースパスワード (辞書攻撃)** ] セクションで、 **[アタックの起動**] をクリックするか、[アタックの**詳細** \>を**起動**する] をクリックします。

   - [**パスワードのスプレーアタック**] セクションで、[**アタックの起動**] をクリックするか、[**アタックの詳細** \>の**起動攻撃**] をクリックします。

3. **パスワード攻撃の構成**ウィザードが新しいポップアップで開始されます。 [**開始**] ステップで、キャンペーンの一意の表示名を入力し、[**次へ**] をクリックします。

4. [**ターゲットユーザー** ] ステップで、次のいずれかの手順を実行します。

   - [**アドレス帳**] をクリックして、キャンペーンの受信者 (ユーザーまたはグループ) を選択します。 対象となる受信者ごとに、Exchange Online メールボックスが必要です。 検索条件を入力せずに [**フィルター**と**適用**] をクリックすると、すべての受信者が返されてキャンペーンに追加されます。

   - [**インポート**]、[**ファイルのインポート**] の順にクリックして、電子メールアドレスのコンマ区切り値 (CSV) または行区切りのファイルをインポートします。 各行には、受信者の電子メールアドレスが含まれている必要があります。

   完了したら、**[次へ]** をクリックします。

5. [**アタック設定の選択**] ステップで、キャンペーンの種類に基づいて、次のいずれかを選択します。

   - **ブルートフォースパスワード (辞書攻撃)**: 次のいずれかの手順を実行します。

     - **パスワードを手動で入力**します。 [enter**キーを押してパスワードを追加**します] ボックスにパスワードを入力し、enter キーを押します。 必要な回数だけこの手順を繰り返します。

     - **辞書ファイルからのパスワードのアップロード**: [**アップロード**] をクリックして、各行に1つのパスワードを含む既存のテキストファイルをインポートします。最後の行は空白にします。 テキストファイルのサイズは 10 MB 以下でなければなりません。また、3万を超えるパスワードを含めることはできません。

   - **パスワードのスプレーアタック**: [アタック] ボックスで**使用するパスワードには**、1つのパスワードを入力します。

   完了したら、**[次へ]** をクリックします。

6. [**確認**] ステップで、[**完了**] をクリックしてキャンペーンを開始します。 指定したパスワードは、指定したユーザーに対して試行されます。

## <a name="view-campaign-results"></a>キャンペーン結果の表示

キャンペーンを開始した後、メインの [**攻撃のシミュレート**] ページで進行状況と結果を確認できます。

アクティブなキャンペーンには、ステータスバー、完成したパーセンテージの値、および (ユーザーの合計数) のカウントが表示されます。 [**更新**] ボタンをクリックすると、アクティブなキャンペーンの進行状況が更新されます。 [**終了**] をクリックして、アクティブなキャンペーンを停止することもできます。

キャンペーンが完了すると、[**アタックが完了**] に変わります。 次のいずれかの操作を実行して、キャンペーンの結果を表示できます。

- [シミュレートされた**アタック**のメイン] ページで、キャンペーンの名前の下にある [**レポートの表示**] をクリックします。

- [アタックの**シミュレーション**] ページで、攻撃の種類についてセクションの [**アタックの詳細**] をクリックします。 開かれた [**アタックの詳細**] ページで、[**アタックの履歴**] セクションでキャンペーンを選択します。

上記のいずれかの操作を行うと、[**アタックの詳細**] というページが表示されます。 各種類のキャンペーンでこのページで使用できる情報については、以下のセクションで説明します。

### <a name="spear-phishing-credentials-harvest-campaign-results"></a>スピアーフィッシング (資格情報のハーベスト) キャンペーンの結果

次の情報は、各キャンペーンの [**アタックの詳細**] ページで利用できます。

- キャンペーンの期間 (開始日時と終了日/時刻) を指定します。

- **対象ユーザーの合計数**

- **成功**した試行: リンクをクリック**して**資格情報 (*任意*のユーザー名とパスワード値) を入力したユーザーの数。

- **全体的な成功率**:**対象となるユーザーの合計****試行回数** / で計算されたパーセンテージ。

- **[最速] クリック**: キャンペーンの開始後、最初のユーザーがリンクをクリックするのにかかった時間。

- **平均クリック**数: すべてのユーザーがリンクをクリックすると、リンクをクリックしたユーザーの数で割った時間の合計。

- **[成功率]**: 計算されたパーセンテージ (リンクをクリックしたユーザーの数)/**対象ユーザーの合計**数。

- **最高の資格情報**: キャンペーンを開始した後、最初のユーザーが資格情報を入力するのにかかった時間。

- **平均資格情報**: ユーザーの資格情報を入力したユーザーの数で割った資格情報の入力にかかった時間の合計。

- **資格情報の成功率**: 計算の対象となるパーセンテージ (資格情報を入力したユーザー数)/**対象ユーザーの合計**数。

- **リンクがクリック**された、1日あたりの**資格情報が入力**された番号を示す棒グラフ。

- クリックされた**リンク**、指定された**資格情報**、およびキャンペーンの**None**パーセンテージを示す円グラフ。

- [**侵害**されたユーザー] セクションに、リンクをクリックしたユーザーの詳細が一覧表示されます。

  - ユーザーの電子メール アドレス

  - リンクをクリックした日付/時刻。

  - クライアント IP アドレス。

  - ユーザーの Windows および web ブラウザーのバージョンに関する詳細。

  [**エクスポート**] をクリックすると、結果を CSV ファイルにエクスポートできます。

### <a name="spear-phishing-attachment-campaign-results"></a>スピアーフィッシング (添付ファイル) のキャンペーン結果

次の情報は、各キャンペーンの [**アタックの詳細**] ページで利用できます。

- キャンペーンの期間 (開始日時と終了日/時刻) を指定します。

- **対象ユーザーの合計数**

- **成功**した試行回数: 添付ファイルを開いた、またはダウンロードしてから開いたユーザーの数 (プレビューではカウントされません)。

- **全体的な成功率**:**対象となるユーザーの合計****試行回数** / で計算されたパーセンテージ。

- **添付ファイルの最速開き時間**: キャンペーンの開始後、最初のユーザーが添付ファイルを開いたのにかかった時間。

- **添付ファイルの平均開かれる時間**: 添付ファイルを開いたユーザーの数によって除算された、すべてのユーザーが添付ファイルを開くのにかかった時間の合計。

- **添付ファイルオープン成功率**: 計算されるパーセンテージ (添付ファイルを開いたユーザーの数)/**対象ユーザー総数**。

### <a name="brute-force-password-dictionary-attack-campaign-results"></a>ブルートフォースパスワード (辞書攻撃) キャンペーンの結果

次の情報は、各キャンペーンの [**アタックの詳細**] ページで利用できます。

- キャンペーンの期間 (開始日時と終了日/時刻) を指定します。

- **対象ユーザーの合計数**

- **成功**した試行: 指定されたパスワードの1つを使用していることが検出されたユーザーの数。

- **全体的な成功率**:**対象となるユーザーの合計****試行回数** / で計算されたパーセンテージ。

- [**侵害**されたユーザー] セクションに、影響を受けるユーザーの電子メールアドレスが一覧表示されます。 [**エクスポート**] をクリックすると、結果を CSV ファイルにエクスポートできます。

### <a name="password-spray-attack-campaign-results"></a>パスワードスプレーアタックキャンペーンの結果

次の情報は、各キャンペーンの [**アタックの詳細**] ページで利用できます。

- キャンペーンの期間 (開始日時と終了日/時刻) を指定します。

- **対象ユーザーの合計数**

- **成功**した試行: 指定されたパスワードを使用していることが検出されたユーザーの数。

- **全体的な成功率**:**対象となるユーザーの合計****試行回数** / で計算されたパーセンテージ。
