---
title: Insider リスク管理ケース
description: Microsoft 365 の insider リスク管理ケースについて説明します。
keywords: Microsoft 365、insider リスク管理、リスク管理、コンプライアンス
localization_priority: Normal
ms.prod: Microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection: m365-security-compliance
ms.openlocfilehash: 7af3e54a13ceabf4acfaa2259ea0089854660721
ms.sourcegitcommit: 1e9ce51efa583c33625299d17e37f58048a4169c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2020
ms.locfileid: "43804836"
---
# <a name="insider-risk-management-cases"></a>Insider リスク管理ケース

ケースは insider リスク管理の中心であり、ポリシーで定義されているリスク指標によって発生した問題について、深く調査してアクションを実行することができます。 ケースは、従業員のコンプライアンス関連の問題に対処するためにさらにアクションが必要になる状況で、警告から手動で作成されます。 各ケースは1人の従業員を対象としており、従業員に対して複数の通知を既存のケースまたは新しいケースに追加できます。 ケースの詳細を調査した後は、従業員に通知を送信するか、問題を解決できないと解決したり、データまたは従業員の調査にエスカレーションしたりすることで、行動を取ることができます。

## <a name="case-dashboard"></a>ケースダッシュボード

Insider リスク管理**ケースダッシュボード**を使用すると、ケースを表示してアクションを実行できます。 ダッシュボードの各レポートウィジェットには、過去30日間の情報が表示されます。

- **アクティブなケース**: 調査中のアクティブなケースの合計数。
- **過去30日間のケース**: 作成されたケースの合計数は、*アクティブな*状態と*クローズ*状態で並べ替えられています。
- **Statistics**: 時間、日、または月単位で表示されているアクティブなケースの平均時間。

ケースキューは、次の case 属性の現在の状態に加えて、組織のすべてのアクティブなケースとクローズされたケースを一覧表示します。

- **ケース名**: 警告が確認され、ケースが作成されるときに定義される、ケースの名前。  
- **状態**: サポート案件の状態 (*アクティブ*か*クローズ*)。
- **User**: ケースの従業員。
- **開い**ている時間のケース: ケースが開かれてから経過した時間。
- **Total policy alerts**: ケースに含まれるポリシー一致の数。 この数は、新しい通知がケースに追加された場合に増加する可能性があります。
- **最終更新**日: ケースの状態に追加のケースメモまたは変更があったために経過した時間。
- **最終更新者**: ケースを最後に更新した insider リスク管理アナリストまたは調査担当者の名前。

![Insider リスク管理ケースダッシュボード](../media/insider-risk-cases-dashboard.png)

**検索**コントロールを使用して、ケース名を特定のテキストで検索し、ケースフィルターを使用して、次の属性でケースを並べ替えます。

- 状態
- 開始日、開始日、終了日
- 最終更新日時、開始日、終了日

## <a name="investigate-a-case"></a>ケースを調査する

適切な是正措置を講じるには、insider リスク管理通知の詳細な調査が重要です。 Insider リスク管理ケースは、従業員のリスクアクティビティの履歴やアラートの詳細を深く掘り下げ、リスクにさらされる内容とメッセージを調査するための中央管理ツールです。 リスクアナリストや調査担当者も、レビューのフィードバックとメモを集中管理し、ケース解決を処理するケースを使用します。 

ケースを選択すると、ケース管理ツールが開き、アナリストと調査担当は、ケースの詳細について掘り下げることができます。

### <a name="case-overview"></a>ケースの概要

[**ケースの概要**] タブでは、ケースのアラートアクティビティおよびリスクレベル履歴の概要を示します。 [**通知**] ウィジェットには、そのケースに一致するポリシーが表示されます。これには、アラートの状態、アラートのリスク重大度、およびアラートが検出された日時が含まれます。 **リスクレベルの履歴**グラフには、過去30日間のユーザーのリスクレベルが表示されます。 折れ線グラフを使用すると、アナリストと調査担当が時間の経過とともに、全体的なユーザーのリスクの傾向をすばやく確認できます。 **リスクアクティビティコンテンツ**ウィジェットは、ケースに追加された通知に含まれるデータの種類と内容を要約します。 このウィジェットを使用すると、データとコンテンツセット全体が、そのケースの危険にさらされます。

ケースの**詳細**ウィンドウは、すべてのケースの管理タブで利用でき、リスクアナリストと調査担当のケースの詳細が要約されています。 次の領域が含まれています。

- **ケース名**: 自動生成されたケースシーケンス番号、および最初の確認通知が一致するポリシーテンプレートに関連付けられているリスクの名前が付いたケースの名前。 
- **ケースの状態**: サポートされているケースの現在の状態 (*アクティブ*か*終了*)。
- **ユーザーのリスクスコア**: ケースに対するユーザーの現在の計算リスクレベル。 このスコアは24時間ごとに計算され、ユーザーに関連付けられたすべてのアクティブなアラートからアラートのリスクスコアを使用します。
- **通知確認**: ケースに対して確認されたユーザーの警告のリスト。
- **リスクがあるコンテンツ**: コンテンツソースと種類で並べ替えられたコンテンツのリスト。 たとえば、SharePoint Online のケース警告コンテンツの場合は、警告のリスクアクティビティに関連付けられているフォルダーまたはファイル名が、ケースに表示されることがあります。

![Insider リスク管理ケースの詳細](../media/insider-risk-case-details.png)

### <a name="alerts"></a>アラート

[**通知**] タブには、ケースに含まれている現在の通知が要約されます。 新しい警告は既存のケースに追加され、割り当てられたときに**警告**キューに追加される場合があります。 次の警告属性がキューに一覧表示されます。

- 状態
- 重要度
- 検出された時間

[**警告の詳細**] ページを表示するには、キューから通知を選択します。

検索コントロールを使用して、特定のテキストのアラート名を検索し、アラートフィルターを使用して、次の属性によってケースを並べ替えます。

- 状態
- 重要度
- 検出された時間、開始日、終了日

### <a name="user-activity"></a>ユーザー アクティビティ

[**ユーザーアクティビティ**] タブは、内部リスク分析および insider リスク管理ソリューションのケースを調査するための最も強力なツールの1つです。 このタブは、すべての通知の過去のタイムライン、すべての警告の詳細、ユーザーの現在のリスクスコア、ケースにおけるリスクを含めるための効果的なアクションを実行する制御など、ケースのクイックレビューを有効にするように構成されています。

![Insider リスク管理のユーザーアクティビティ](../media/insider-risk-user-activities.png)

1. **日付と時刻のフィルター**: 既定では、ケースで確認された通知の過去6か月間は、[ユーザーアクティビティ] グラフに表示されます。 グラフビューのフィルターは、グラフウィンドウの両端にあるスライダーコントロール、またはグラフフィルターコントロールで特定の開始日と終了日を定義することで簡単に実行できます。
2. **リスクアラートのアクティビティと詳細**: リスクアクティビティは、[ユーザーアクティビティ] グラフに色付きのバブルとして視覚的に表示されます。 バブルはさまざまなカテゴリのリスクに対して作成され、バブルサイズはカテゴリのリスクアクティビティの数に比例します。 バブルを選択して、各リスクアクティビティの詳細を表示します。 詳細は次のとおりです。
    - リスクアクティビティの**日付**。
    - **リスクアクティビティカテゴリ**。 たとえば、組織または*SharePoint Online からダウンロード*された*添付ファイルを含む電子メール (s) が*含まれます。
    - アラートの**リスクスコア**。 このスコアは、アラートのリスク重大度レベルの数値スコアです。
    - 通知に関連付けられているイベントの数。 リスクアクティビティに関連付けられている各ファイルまたは電子メールへのリンクも利用できます。
3. **リスクアクティビティの凡例**: ユーザーアクティビティグラフの下部に、色分けされた凡例が表示され、各アラートのリスクカテゴリをすばやく判断できます。
4. **リスクアクティビティ chronology**: 対応する通知のバブルで利用可能なすべての詳細を含む、ケースに関連付けられているすべてのリスクアラートの完全な chronology が一覧表示されます。
5. ケース**アクション**: ケースを解決するためのオプションは、ケースアクションツールバーにあります。 ケースを解決したり、従業員に電子メール通知を送信したり、データまたは従業員の調査のためにケースをエスカレートしたりすることができます。

### <a name="content-explorer"></a>コンテンツ エクスプローラー

[**コンテンツエクスプローラー** ] タブでは、リスクの通知に関連付けられている個々のファイルおよび電子メールメッセージのすべてのコピーをリスク分析者と調査担当者が確認できます。 たとえば、従業員が数百のファイルを SharePoint Online から USB デバイスにダウンロードする際に通知が作成され、そのアクティビティがポリシー警告をトリガーすると、その通知に関するすべてのダウンロードファイルが取得され、元のストレージソースから insider リスク管理ケースにコピーされます。

コンテンツエクスプローラーは、基本的で高度な検索とフィルター処理機能を備えた強力なツールです。 コンテンツエクスプローラーの使用の詳細については、「 [Insider リスク管理コンテンツエクスプローラー](insider-risk-management-content-explorer.md)」を参照してください。

![Insider リスク管理ケースコンテンツエクスプローラー](../media/insider-risk-content-explorer.png)

### <a name="case-notes"></a>ケースメモ

ケースのケース**メモ**タブでは、リスクアナリストと調査担当者が、そのケースの作業に関するコメント、フィードバック、および洞察を共有しています。 メモは、ケースに永続的に追加され、メモの保存後に編集または削除することはできません。 警告からケースを作成すると、[**警告の確認と内部のリスクケースの作成**] ダイアログに入力されたコメントが、ケースメモとして自動的に追加されます。

ケースノートダッシュボードには、メモを作成したユーザーによってメモが表示され、ノートが保存されてから経過した時間が表示されます。 特定のキーワードのケースメモテキストフィールドを検索するには、ケースダッシュボードの [**検索**] ボタンを使用して、特定のキーワードを入力します。

ケースにメモを追加するには、次のようにします。

1. [Microsoft 365 コンプライアンスセンター](https://compliance.microsoft.com)で、[ **Insider リスク管理**] に移動し、[**ケース**] タブを選択します。
2. ケースを選択し、[**ケースメモ**] タブを選択します。
3. [**ケースメモの追加**] を選択します。
4. [**ケースメモの追加**] ダイアログで、ケースのメモを入力します。 メモをケースに追加するには [**保存**] を選択するか、メモを保存せずに **[閉じる] を選択します**。

### <a name="contributors"></a>多様

ケースの [**寄稿**者] タブでは、リスクアナリストや調査担当者が、ケースに他のレビュー担当者を追加することができます。 既定では、 **Insider リスク管理アナリスト**と**insider リスク管理**の各調査担当者の役割が割り当てられているすべてのユーザーが、アクティブなケースとクローズしたケースの共同作成者として一覧表示されます。

調査の機密性と整合性を維持するには、すべての insider リスク管理ケースを適切なアクセス制御で管理する必要があります。 サポート案件へのアクセス制御を維持するために、ユーザーには次の2種類のいずれかのアクセス許可が割り当てられます。

- **永続的なアクセス**: 通知からケースを作成するときに、 **Insider リスク管理アナリスト**と**insider リスク管理**の各調査担当者の役割を持つユーザーに永続的アクセスが自動的に付与されます。 永続的なアクセスでは、ケースの有効期間中、ケースのフルコントロールが許可され、他のケースの投稿者を追加する機能が付与されます。
- **一時アクセス**: ユーザーには、そのケースに永続的なアクセス権を持つ投稿者のみがアクセス権を付与します。 通常、このアクセスレベルは、ケースにメモを追加する必要があるユーザーに付与されます。 一時的なアクセス権を持つ投稿者は、次のものを除き、すべてのケース管理制御を行います。
    - 通知を確認または消去するためのアクセス許可
    - ケースの投稿者を編集するためのアクセス許可
    - コンテンツエクスプローラーでファイルとメッセージを表示するためのアクセス許可

ケースに共同作成者を追加するには、次のようにします。

1. [Microsoft 365 コンプライアンスセンター](https://compliance.microsoft.com)で、[ **Insider リスク管理**] に移動し、[**ケース**] タブを選択します。
2. ケースを選択し、[**投稿**者] タブを選択します。
3. [**投稿者の追加**] を選択します。
4. [**共同作成者の追加**] ダイアログで、追加するユーザーの名前の入力を開始し、[推奨されるユーザー] ボックスの一覧からユーザーを選択します。 このリストは、テナントのサブスクリプションの Azure Active Directory から生成されます。
5. [**投稿者の追加**] ダイアログで、投稿者のアクセスレベルを選択します。 [**永続的**] または [**一時的**] を選択できます。
6. [**追加**] を選択して、ユーザーを共同作成者として追加するか、[**キャンセル**] を選択してユーザーを共同作成者として追加せずにダイアログを閉じます。

## <a name="case-actions"></a>Case アクション

リスクアナリストと捜査官は、ケースの重要度、従業員のリスク履歴、組織のリスクガイドラインに応じて、いくつかの方法のいずれかで、ケースに対してアクションを実行できます。 状況によっては、従業員またはデータ調査にケースをエスカレートして、組織の他の領域と共同作業を行ったり、より詳細なリスクアクティビティを把握したりする必要があります。 エンドツーエンドの解決管理に役立つように、Insider リスク管理は Microsoft 365 コンプライアンスの他の機能と緊密に統合されています。

### <a name="send-a-notice"></a>通知を送信する

ほとんどの場合、ポリシー一致アラートを作成する従業員アクションは、不注意または過失になります。 電子メールを使用して従業員に事前通知の通知を送信することは、ケースのレビューとアクションを文書化するための効果的な方法、および企業ポリシーの従業員に通知するための方法、またはそれらをリフレッシャートレーニングにするための方法です。 通知は、insider リスク管理インフラストラクチャ用に[作成した通知テンプレート](insider-risk-management-notices.md)から生成されます。

従業員に通知を送信しても、そのケースは*クローズ*として解決***されない***ことを覚えておくことが重要です。 場合によっては、新しいケースを開かずに、追加のリスクアクティビティを検索するために従業員に通知を送信した後で、ケースを開いたままにしておくこともできます。 通知を送信した後でケースを解決する場合は、通知を送信した後のフォローアップの手順として、**解決ケース**を選択する必要があります。

ケースに割り当てられた従業員に通知を送信するには、次のようにします。

1. [Microsoft 365 コンプライアンスセンター](https://compliance.microsoft.com)で、[ **Insider リスク管理**] に移動し、[**ケース**] タブを選択します。
2. ケースを選択してから、ケースアクションツールバーの [**電子メール通知の送信**] ボタンを選択します。
3. [**電子メール通知の送信**] ダイアログで、[通知**テンプレートの選択**] ドロップダウンコントロールを選択して、通知の通知テンプレートを選択します。 この選択範囲は、通知の他のフィールドに事前に入力されています。
4. [通知] フィールドを確認し、必要に応じて更新します。 ここで入力した値は、テンプレートの値より優先されます。
5. [**送信**] を選択して従業員に通知を送信するか、[**キャンセル**] を選択して、通知を従業員に送信せずにダイアログを閉じます。 送信されたすべての通知は、ケース**メモ**ダッシュボードのケースメモキューに追加されます。

### <a name="escalate-for-investigation"></a>調査のためのエスカレーション

従業員のリスクアクティビティに対して追加の法的レビューが必要になる状況で、従業員調査のケースをエスカレートします。 このエスカレーションは、Microsoft 365 組織で新しい電子情報開示ケースを開きます。 Advanced eDiscovery は、組織の内部および外部の法的調査に対応するコンテンツを保持、収集、確認、分析、およびエクスポートするためのエンドツーエンドのワークフローを提供します。 また、訴訟チームが、訴訟に関与する保管担当者と通信するための法的情報保留通知ワークフロー全体を管理することもできます。 Insider リスク管理ケースから作成された高度な電子情報開示ケースの保管担当者としてレビュー担当者を割り当てることで、法務チームは適切なアクションを実行し、コンテンツの保持を管理することができます。 高度な電子情報開示ケースの詳細については、「 [Microsoft 365 の高度な電子情報開示の概要](overview-ediscovery-20.md)」を参照してください。

ケースを従業員調査にエスカレートするには、次のようにします。

1. [Microsoft 365 コンプライアンスセンター](https://compliance.microsoft.com)で、[ **Insider リスク管理**] に移動し、[**ケース**] タブを選択します。
2. ケースを選択し、[ケースアクション] ツールバーの [**調査対象のエスカレート**] ボタンを選択します。
3. [**調査のためのエスカレーション**] ダイアログで、新入社員の調査の名前を入力します。 必要に応じて、ケースに関するメモを入力し、[**エスカレート**] を選択します。
5. [**確認**] を選択して従業員の調査ケースを作成するか、[**キャンセル**] を選択して、新しい従業員調査ケースを作成せずにダイアログを閉じます。

Insider リスク管理ケースが新しい従業員の調査ケースにエスカレートされた後、Microsoft 365 コンプライアンスセンターの**電子情報開示** > の**高度な**領域で新しいケースを確認できます。

### <a name="resolve-the-case"></a>ケースを解決する

アナリストと調査担当者がレビューと調査を完了した後、ケースを解決して、現在のケースに含まれているすべての警告を処理できるようにすることができます。 ケースを解決すると、解決方法の分類が追加され、ケースの状態が*Closed*に変更されます。また、解決策の処理の理由が、ケース**メモ**ダッシュボードのケースメモキューに自動的に追加されます。 ケースは次のいずれかとして解決されます。

- **無害**: ポリシーに一致するアラートが低リスク、非深刻、または誤検知として評価される場合の分類。
- [**確認ポリシー違反**]: ポリシーがアラートに一致する場合の分類は、危険、重大、または悪意のある目的として評価されます。

ケースを解決するには、次のようにします。

1. [Microsoft 365 コンプライアンスセンター](https://compliance.microsoft.com)で、[ **Insider リスク管理**] に移動し、[**ケース**] タブを選択します。
2. ケースを選択してから、ケースアクションのツールバーの [**ケースの解決**] ボタンを選択します。
3. [**ケースの解決**] ダイアログで、[**解決**方法] ドロップダウンコントロールを選択して、ケースの解決分類を選択します。 オプションには、**無害**または確認された**ポリシー違反**があります。
4. [**ケースの解決**] ダイアログで、[実行された**アクション**] テキストフィールドに解決の分類の理由を入力します。
5. [**解決**] を選択してケースを終了するか、[**キャンセル**] を選択してケースを解決せずにダイアログを閉じます。
