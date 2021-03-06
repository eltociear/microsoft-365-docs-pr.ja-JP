---
title: ケーススタディ-Contoso 社は、Microsoft Teams、Exchange、Yammer の通信に対して、不快な言語ポリシーを迅速に構成します。
description: Contoso 社のケーススタディと、Microsoft Teams、Exchange Online、Yammer の通信で不快な言葉を監視するために、コミュニケーションコンプライアンスポリシーを迅速に構成する方法について説明します。
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- remotework
search.appverid:
- MET150
- MOE150
ms.openlocfilehash: 39815140d223d95275e03b0e85b931699bd69f7e
ms.sourcegitcommit: 2399ee6f9bc955cf8f2a76c01fc84c19eb37ff42
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2020
ms.locfileid: "43919714"
---
# <a name="case-study---contoso-quickly-configures-an-offensive-language-policy-for-microsoft-teams-exchange-and-yammer-communications"></a>ケーススタディ-Contoso 社は、Microsoft Teams、Exchange、Yammer の通信に対して、不快な言語ポリシーを迅速に構成します。

Microsoft 365 の通信コンプライアンスは、組織内の不適切なメッセージに対する修復措置を検出、取得、および解決するのに役立つため、コミュニケーションリスクを最小限に抑えることができます。 定義済みおよびカスタムのポリシーを使用すると、ポリシーの一致に関する内部通信と外部通信をスキャンして、指定したレビュー担当者がそれらを調査できるようにすることができます。 レビューアーは、スキャンされた電子メール、Microsoft Teams、Yammer、または組織内のサードパーティの通信を調査し、適切な修復処置を行って、組織のメッセージ標準に準拠していることを確認できます。

Contoso Corporation は、不快感を与える言葉を監視するポリシーをすばやく構成する必要がある架空の組織です。 従業員は主に、メール、Microsoft Teams、Yammer のサポートに Microsoft 365 を使用していましたが、workplace 嫌がらせに関して会社のポリシーを適用するための新しい要件があります。 Contoso 社の IT 管理者およびコンプライアンスの専門家は、Microsoft 365 の使用に関する基本事項について基本的な理解を深めており、コミュニケーションのコンプライアンスをすばやく始める方法についてのエンドツーエンドのガイダンスを求めています。

このケーススタディでは、有害な言語の通信を監視するための通信コンプライアンスポリシーをすばやく構成するための基本事項について説明します。 このガイダンスには次のものが含まれます。

- 手順 1-通信のコンプライアンスを計画する
- 手順 2-Microsoft 365 での通信コンプライアンスへのアクセス
- 手順 3-前提条件を構成し、通信コンプライアンスポリシーを作成する
- ステップ 4-通知の調査と修復

## <a name="step-1---planning-for-communication-compliance"></a>手順 1-通信のコンプライアンスを計画する

Contoso 社の IT 管理者およびコンプライアンスの専門家は、Microsoft 365 のコンプライアンスソリューションに関するオンラインウェビナーに参加しており、コミュニケーションコンプライアンスポリシーが、workplace 嫌がらせを削減するために更新された企業ポリシー要件を満たすのを支援することを決定しました。 共同作業では、Microsoft Teams で送信されるチャット、Yammer のプライベートメッセージ、コミュニティの会話、Exchange Online で送信された電子メールメッセージなどを監視するための、通信コンプライアンスポリシーを作成し、有効にするための計画が策定されました。 プランには、次の内容が含まれます。

- 通信コンプライアンス機能にアクセスする必要がある IT 管理者。
- コミュニケーションポリシーを作成および管理する必要があるコンプライアンススペシャリスト。
- コミュニケーションのコンプライアンス警告を調査および修復する必要がある、他の部門 (人事、法律など) のコンプライアンススペシャリストおよびその他の仕事仲間。
- 通信コンプライアンス不快な言語ポリシーの範囲内となるユーザー。

### <a name="licensing"></a>ライセンス

最初の手順は、Contoso 社の Microsoft 365 ライセンスに、コミュニケーションコンプライアンスソリューションのサポートが含まれていることを確認することです。 通信コンプライアンスにアクセスして使用するために、Contoso 社の IT 管理者は Contoso に次のいずれかの情報が含まれていることを確認する必要があります。

- Microsoft 365 E5 サブスクリプション (有料または試用版)
- Microsoft 365 E3 サブスクリプション + Microsoft 365 E5 コンプライアンスアドオン
- Microsoft 365 E3 サブスクリプション + Microsoft 365 E5 Insider リスク管理アドオン
- Microsoft 365 A5 サブスクリプション (有料または試用版)
- Microsoft 365 A3 サブスクリプション + Microsoft 365 A5 コンプライアンスアドオン
- Microsoft 365 A3 サブスクリプション + Microsoft 365 A5 Insider リスク管理アドオン
- Microsoft 365 G5 サブスクリプション (有料または試用版)
- Microsoft 365 G5 サブスクリプション + Microsoft 365 G5 コンプライアンスアドオン
- Microsoft 365 G5 サブスクリプション + Microsoft 365 G5 Insider リスク管理アドオン
- Office 365 Enterprise E5 サブスクリプション (有料または試用版)
- Office 365 Enterprise E3 サブスクリプション + Office 365 Advanced コンプライアンスアドオン (新しいサブスクリプションでは使用できなくなりました)。メモを参照してください。

また、通信コンプライアンスポリシーに含まれているユーザーに上記のいずれかのライセンスを割り当てる必要があることも確認する必要があります。

>[!IMPORTANT]
>Office 365 Advanced コンプライアンスは、スタンドアロンサブスクリプションとして販売されなくなりました。 現在のサブスクリプションの有効期限が切れた場合、お客様は上記のサブスクリプションのいずれかに移行する必要があります。これには、同じまたは追加のコンプライアンス機能が含まれます。

Contoso 社の IT 管理者は、次の手順を実行して Contoso のライセンスサポートを確認します。

1. IT 管理者は、 **microsoft 365 管理センター** [https://admin.microsoft.com)にサインインして](https://admin.microsoft.com)、 **microsoft 365 管理センター** > **請求** > **ライセンス**に移動します。

2. ここでは、通信コンプライアンスのサポートを含む[ライセンスオプション](https://docs.microsoft.com/microsoft-365/compliance/communication-compliance-configure?view=o365-worldwide#before-you-begin)の1つを持っていることを確認します。

![コミュニケーションコンプライアンスライセンス](../media/communication-compliance-case-licenses.png)

### <a name="permissions-for-communication-compliance"></a>通信コンプライアンスのアクセス許可

既定では、全体管理者は通信コンプライアンス機能にアクセスできません。 Contoso IT 管理者とコンプライアンス担当者がコミュニケーションコンプライアンスにアクセスできるように、[アクセス許可を構成する必要があり](https://docs.microsoft.com/microsoft-365/compliance/communication-compliance-configure?view=o365-worldwide#step-1-required-enable-permissions-for-communication-compliance)ます。

1. Contoso IT 管理者は、 **Office 365 セキュリティとコンプライアンスセンター**のアクセス許可ページにサインインします[(https://protection.office.com/permissions) ](https://protection.office.com/permissions)グローバル管理者アカウントの資格情報を使用して、Microsoft 365 の役割を表示および管理するためのリンクを選択します)。
2. [**作成**] を選択すると、新しい役割グループに [*通信コンプライアンス*] のフレンドリ名が与えられ、[**次へ**] を選択します。
3. [**役割の選択**] を選択し、[**追加**] を選択します。 必要な役割を追加するには、*監督レビュー管理者*、*ケース管理*、*コンプライアンス管理者*、*およびレビュー*のチェックボックスをオンにし、[**追加**]、[**完了]、** [**次へ**] の順に選択します。

![コミュニケーションコンプライアンスの役割](../media/communication-compliance-case-roles.png)

4. 次に、IT 管理者は [**メンバーの選択**] を選択し、[**追加**] を選択します。 ポリシーを作成するすべてのユーザーとグループのチェックボックスをオンにして、ポリシーの一致でメッセージを管理します。 最初の計画で特定された人事および法務部門に IT 管理者、コンプライアンスの専門家、その他の仕事仲間を追加し、[**追加**]、[**完了**]、[**次へ**] を選択します。
5. アクセス許可を確定するには、IT 管理者が [**役割グループの作成**] を選択して終了します。 Contoso 社の Microsoft 365 サービスでは、役割が有効になるまでに約30分かかります。

![コミュニケーションコンプライアンスレビュー](../media/communication-compliance-case-review.png)

## <a name="step-2---accessing-communication-compliance-in-microsoft-365"></a>手順 2-Microsoft 365 での通信コンプライアンスへのアクセス

通信コンプライアンスのアクセス許可を構成した後、新しい役割グループで定義されている Contoso IT 管理者とコンプライアンススペシャリストは、Microsoft 365 の通信コンプライアンスソリューションにアクセスできます。 Contoso 社の IT 管理者およびコンプライアンスの専門家は、コミュニケーションへのコンプライアンスにアクセスし、新しいポリシーの作成を開始するためのいくつかの方法を備えています。

- コミュニケーションコンプライアンスソリューションから直接開始する
- Microsoft 365 コンプライアンスセンターからの開始
- Microsoft 365 ソリューションカタログからの開始
- Microsoft 365 管理センターから開始する

### <a name="starting-directly-from-the-communication-compliance-solution"></a>コミュニケーションコンプライアンスソリューションから直接開始する

ソリューションにアクセスする最も簡単な方法は、**コミュニケーションコンプライアンス**(<https://compliance.microsoft.com/supervisoryreview>) ソリューションに直接サインインすることです。 このリンクを使用すると、Contoso IT 管理者とコンプライアンスの専門家は、通知の状態をすばやく確認し、定義済みのテンプレートから新しいポリシーを作成できる、コミュニケーションコンプライアンスの概要ダッシュボードに送られます。

![コミュニケーションコンプライアンスの概要](../media/communication-compliance-case-overview.png)

### <a name="starting-from-the-microsoft-365-compliance-center"></a>Microsoft 365 コンプライアンスセンターからの開始

Contoso IT 管理者とコンプライアンス担当者がコミュニケーションコンプライアンスソリューションにアクセスするもう1つの簡単な方法は、 **Microsoft 365 コンプライアンスセンター** [(https://compliance.microsoft.com)](https://compliance.microsoft.com)) に直接サインインすることです。 サインインした後、ユーザーは、すべてのコンプライアンスソリューションを表示するために [**すべて表示**] を選択するだけで、開始する**通信コンプライアンス**ソリューションを選択するだけで済みます。

![コンプライアンスセンター](../media/communication-compliance-case-center.png)

### <a name="starting-from-the-microsoft-365-solution-catalog"></a>Microsoft 365 ソリューションカタログからの開始

Contoso 社の IT 管理者およびコンプライアンス担当者は、Microsoft 365 ソリューションカタログを選択して、コミュニケーションコンプライアンスソリューションにアクセスすることもできます。 **Microsoft 365 コンプライアンスセンター**で、左側のナビゲーションの [**ソリューション**の**カタログ**] セクションを選択すると、すべての microsoft 365 コンプライアンスソリューションを一覧表示したソリューションカタログを開くことができます。 「 **Insider リスク管理**」セクションまでスクロールすると、Contoso IT 管理者は通信のコンプライアンスを選択して開始することができます。 Contoso 社の IT 管理者は、[ナビゲーションに表示] コントロールを使用して、コミュニケーションコンプライアンスソリューションを左側のナビゲーションウィンドウにピン留めし、今後のサインイン時にすばやくアクセスできるようにすることも決定します。

![ソリューションカタログ](../media/communication-compliance-case-solution.png)

### <a name="starting-from-the-microsoft-365-admin-center"></a>Microsoft 365 管理センターから開始する

Microsoft 365 管理センターから開始して通信コンプライアンスにアクセスするには、Contoso IT 管理者とコンプライアンス担当者が microsoft 365[管理https://admin.microsoft.com)センターに](https://admin.microsoft.com)サインインし、 **microsoft 365 管理センター** > **コンプライアンス**に移動します。

![通信コンプライアンスリンク](../media/communication-compliance-case-compliance-link.png)

これにより、 **Office 365 セキュリティ/コンプライアンスセンター**が開き、ページ上部のバナーで提供される**Microsoft 365 コンプライアンスセンター**へのリンクを選択する必要があります。

![Office 365 セキュリティ/コンプライアンスセンター](../media/communication-compliance-case-scc.png)

**Microsoft 365 コンプライアンスセンター**では、Contoso IT 管理者は [**すべて表示**] を選択して、コンプライアンスソリューションの完全な一覧を表示します。

![通信コンプライアンスメニュー](../media/communication-compliance-case-show-all.png)

[**すべて表示**] を選択すると、Contoso IT 管理者はコミュニケーションコンプライアンスソリューションにアクセスできるようになります。

![コミュニケーションコンプライアンスの概要](../media/communication-compliance-case-overview.png)

## <a name="step-3---configuring-prerequisites-and-creating-a-communication-compliance-policy"></a>手順 3-前提条件を構成し、通信コンプライアンスポリシーを作成する

通信コンプライアンスポリシーの使用を開始するには、攻撃的な言葉を監視するように新しいポリシーを設定する前に Contoso IT 管理者が構成する必要があるいくつかの前提条件があります。 これらの前提条件が満たされたら、Contoso IT 管理者とコンプライアンス担当者が新しいポリシーを構成し、コンプライアンススペシャリストが調査を開始し、生成されたすべての警告を修復することができます。

### <a name="enabling-auditing-in-microsoft-365"></a>Microsoft 365 で監査を有効にする

通信のコンプライアンスでは、監査ログを使用して通知を表示し、レビュー担当者が行った修復アクションを追跡する必要があります。 監査ログは、定義された組織のポリシーに関連付けられているすべてのアクティビティの要約です。または、通信コンプライアンスポリシーに変更がある場合はいつでも、その概要です。

Contoso 社の IT 管理者は、監査を有効[にするため](https://docs.microsoft.com/microsoft-365/compliance/turn-audit-log-search-on-or-off)の手順を確認して完了します。 監査を有効にすると、監査ログが準備されていて、準備が完了してから数時間で検索を実行できることを示すメッセージが表示されます。 Contoso 社の IT 管理者は、このアクションを1回だけ実行する必要があります。

### <a name="configuring-yammer-tenant-for-native-mode"></a>ネイティブモードで Yammer テナントを構成する

通信のコンプライアンスを行うには、組織の Yammer テナントがネイティブモードになっていることが必要です。これは、プライベートメッセージやパブリックコミュニティの会話で不快な言葉を監視するためです。

Contoso 社の IT 管理者は、 [microsoft 365 トピックの Yammer ネイティブモードの概要](https://docs.microsoft.com/yammer/configure-your-yammer-network/overview-native-mode)にある情報を確認し、「 [Microsoft 365 のネイティブモードの Yammer ネットワークを構成](https://docs.microsoft.com/yammer/configure-your-yammer-network/native-mode)する」の手順に従って移行ツールを実行することを確認してください。

### <a name="setting-up-a-group-for-in-scope-users"></a>スコープ内ユーザーのグループの設定

Contoso 社のコンプライアンス担当者が、不快な言葉を監視するコミュニケーションポリシーに従業員を追加することを希望しています。 各従業員のユーザーアカウントをポリシーに個別に追加することを決定することもできますが、これはより簡単になり、このポリシーのユーザーに対して**すべての従業員**配布グループを使用するための時間が大幅に節約されることが決定されました。

Contoso 社の従業員全員を含む新しいグループを作成する必要があるので、次の手順を実行します。

1. Contoso it 管理者は、 **microsoft 365 管理センター** [https://admin.microsoft.com)にサインインして](https://admin.microsoft.com)、 **microsoft 365 管理センター** > **グループ** > **グループ**に移動します。
2. [**グループの追加**] を選択し、ウィザードを完了して、新しい*Microsoft 365 グループ*または*配布グループ*を作成します。

![グループ](../media/communication-compliance-case-all-employees.png)

3. 新しいグループを作成した後、すべての Contoso ユーザーを新しいグループに追加する必要があります。 **Exchange 管理センター** [https://outlook.office365.com/ecp) ](https://outlook.office365.com/ecp)を開き、 **exchange 管理センター** > の [**受信者** > **グループ**] に移動します。 Contoso IT 管理者は、メンバーシップ領域および作成した新しい*すべての従業員*グループを選択し、[**編集**] コントロールを選択して、すべての contoso 従業員をウィザードの新しいグループに追加します。

![Exchange 管理センター](../media/communication-compliance-case-eac.png)

### <a name="creating-the-policy-to-monitor-for-offensive-language"></a>不快な言葉を監視するポリシーを作成する

すべての前提条件が満たされたら、Contoso の IT 管理者とコンプライアンスの専門家が、不快な言葉を監視するための通信コンプライアンスポリシーを構成する準備ができました。 新しい不快な言語のポリシーテンプレートを使用すると、このポリシーの構成は簡単で短時間になります。

1. Contoso IT 管理者およびコンプライアンスの専門家は、 **Microsoft 365 コンプライアンスセンター**にサインインし、左側のナビゲーションウィンドウから [**通信コンプライアンス**] を選択します。 この操作により、コミュニケーションコンプライアンスポリシーテンプレートのクイックリンクがある**概要**ダッシュボードが開きます。 [テンプレートの**開始**] を選択して、**不快感を得る言語テンプレートのモニター**を選択します。

![コミュニケーションコンプライアンス不快な言語テンプレート](../media/communication-compliance-case-template.png)

2. ポリシーテンプレートウィザードでは、Contoso IT 管理者とコンプライアンスの専門家が連携して、**ポリシー名**、**監督対象のユーザーまたはグループ**、および**レビュー担当者**という3つの必須フィールドを完了します。
3. ポリシーウィザードによって既にポリシーの名前が提案されているため、IT 管理者およびコンプライアンスの専門家は、提案された名前を保持し、残りのフィールドに焦点を当てることに決定します。 **ユーザーまたはグループ**の [監督] フィールドに [ *All employees* ] グループを選択し、[**レビュー担当者**] フィールドのポリシー通知を調査および修復する必要があるコンプライアンススペシャリストを選択します。 ポリシーを構成して通知情報の収集を開始するための最後の手順として、[**ポリシーの作成**] を選択します。

![通信コンプライアンス不快な言語ウィザード](../media/communication-compliance-case-wizard.png)

## <a name="step-4--investigate-and-remediate-alerts"></a>手順 4: 通知を調べて修復する

これで、不快感を与える言語を監視するための通信コンプライアンスポリシーが構成されました。次の手順では、Contoso コンプライアンスの専門家がポリシーによって生成された警告を調査して修復します。 ポリシーがすべての通信ソースチャネル内の通信を完全に処理し、通知が**通知ダッシュボード**に表示されるまでに最大24時間かかります。

通知が生成された後、Contoso 社のコンプライアンス担当者は[ワークフローの指示](https://docs.microsoft.com/microsoft-365/compliance/communication-compliance-investigate-remediate)に従って、不快な言葉の問題を調査および修復します。