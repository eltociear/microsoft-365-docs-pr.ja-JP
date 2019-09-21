---
title: Office 365 の高度な電子情報開示でインポートされたファイルを追加するためのロードを設定する
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Office 365 Advanced eDiscovery で関連性トレーニングを実行する前に、インポートされたファイルを最後に定義したロードまたはバッチファイルに追加する手順を確認します。  '
ms.openlocfilehash: 65e022680cc0bd39bbca3e05a4e3b6d24da1b2ad
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2019
ms.locfileid: "37086400"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a>Office 365 の高度な電子情報開示でインポートされたファイルを追加するためのロードを設定する

> [!NOTE]
> Advanced eDiscovery を使用するには、Advanced Compliance アドオンがインストールされた Office 365 E3 サブスクリプション、または E5 サブスクリプションがお客様の組織で必要になります。このプランを利用しておらず、Advanced eDiscovery をお試しになりたい場合は、[Office 365 Enterprise E5 の試用版にサインアップ](https://go.microsoft.com/fwlink/p/?LinkID=698279)してください。 
  
高度な電子情報開示では、ケースに追加されたファイルの新しいバッチがロードされます。 既定では、1つの負荷が定義され、インポートされたすべてのファイルが追加されます。 関連性トレーニングを実行する前に、インポートしたファイルをロードに追加する必要があります。 
  
次のようなシナリオを考えてみましょう。
  
- 新しいファイルは、ケースデータベースに読み込まれた以前のファイルに似ていることがわかっているか、ファイルの以前の負荷がファイルコレクションからランダムに設定されていました。 このインスタンスでは、インポートしたファイルを現在のファイルの読み込みに追加します。
    
- 新しいファイルが以前のファイルと異なる (たとえば、別のソースからの) 場合、または以前の負荷と類似しているか、異なる新しいファイルがあります。 このシナリオでは、インポートしたファイルを新しいファイルの読み込みに追加します。 上級電子情報開示は、これをローリングロードシナリオとして認識し、キャッチアッププロセスを起動し、キャッチアップが完了するまで関連トレーニングとバッチ計算をロックし、新しい負荷を統合し、トレーニングを行います。 
    
## <a name="adding-imported-files-to-the-current-load"></a>インポートされたファイルを現在の負荷に追加する

インポートされたすべてのファイルは、高度な電子情報開示で処理するには、負荷に追加する必要があります。 インポートしたファイルは、最後に定義されたロードに追加されます。 後で追加のファイルをインポートする場合は、それらもロードに追加する必要があります。
  
1. [**関連性\>の関連性の設定**] タブで、[**ロード**] を選択します。
    
    ![[関連性の設定をロード] タブ](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. **インクルードファイル**: 含めるファイルのオプションを選択します。 既定では、現在の負荷にファイルを追加すると、"すべてのファイル" の作成に基づきます。
    
    > [!TIP]
    > 利用可能なすべてのカリングファイルを関連に読み込みます。 利用可能なファイルのサブセットのみを読み込む予定の場合は、「サポート」を参照してください。サブセットを読み込むと、関連性トレーニングに悪影響を及ぼす可能性があります。 
  
3. [**ロード管理**] で、ロードを選択します。
    
4. [**ファイルの追加**] をクリックします。 ファイルがロードに追加され、確認メッセージが表示されます。 
    
5. **[OK]** をクリックします。
    
ファイルをトレーニングするために、上級電子情報開示の関連性でファイルを処理できるようになりました。
  
## <a name="editing-a-load-name-within-a-case"></a>ケース内での読み込み名の編集

読み込み名を変更する場合は、ケースにとって重要な名前を使用することをお勧めします。
  
1. [**関連性\>の関連性の設定**] タブで、[**ロード**] を選択します。
    
2. [Load **management** ] の一覧から、ロードを選択し、[**編集**] アイコンをクリックします。 [読み込みの編集] ウィンドウが表示されます。 
    
3. 変更を入力し、[ **OK]** をクリックします。
    
## <a name="adding-imported-files-to-a-new-load"></a>インポートされたファイルを新しいロードに追加する

関連性のトレーニングを開始するか、バッチ計算を実行すると、追加のファイルセットをインポートして処理することができます。 
  
キャッチアップの間に、キャッチアップセットを作成、タグ付け、および分析することができます。 上級電子情報開示は、新しい負荷における関連ファイルと関連しないファイルの評価を以前の負荷と比較します。 結果に基づいて、キャッチアップに関する決定事項を必要に応じて確認するよう求められます。また、上級電子情報開示では、見越計上の関連性情報に基づいた推奨事項を提供します。 
  
ロールロードおよびキャッチアップ機能は、次のように異なります。 
  
- バッチ計算後に新しいファイル読み込みをインポートする場合、Advanced eDiscovery は次のいずれかのカテゴリにどの程度ファイルが含まれるかを決定します。
    
  - 類似 (同種): 新しい、カスタムの関連性のトレーニングは必須ではなく、以前の負荷からのナレッジの見越計上を新しい負荷に適用することができます。 
    
  - Distinct (異種): 新しいカスタムラウンドの関連性トレーニングが必要であり、前のロードからのナレッジを適用できません。 
    
    これらの用語は、ロード間ではなく、ファイルの類似性のレベルを表します。 
    
- 関連性トレーニングの際に (バッチ計算の前に)、新しいファイル読み込みをインポートする場合、キャッチアップを使用すると、英語のファイルセットに対して関連性のトレーニングを続行できます。 上級電子情報開示では、新しい負荷が以前の負荷と類似しているか、または異なるかは予測されません。 これは単に、新しい負荷に関する情報を収集し、関連のトレーニングが新しいファイルおよび以前のファイルセットに対して継続するようにします。 
    
- 関連性のトレーニングに問題があり、バッチの計算後に問題が発生した場合、キャッチアッププロセスはすべての問題に対して1回実行され、結果は各問題について計算され、表示されます。
    
> [!NOTE]
> キャッチアップサンプルのサイズは異なる場合があります。 これは、以前の負荷に対する新しい負荷のサイズと、新しい負荷を追加する前に完了したサンプルの数によって異なります。 キャッチアップサンプルは、通常、新しいロードから 200 ~ 2000 ファイルのセットです。 
  
> [!TIP]
> キャッチアップは他のタスクを停止し、個々のファイルのタグ付けとレビューを必要とします。 そのため、大きなバッチで新しいファイルを追加するときのオーバーヘッドを減らすことができます。 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a>キャッチアップおよびローリングロードを使用して新しいファイル読み込みを追加する

1. [**関連性\>の関連性の設定**] タブで、[**ロード**] を選択します。
    
2. [ロード**管理**] で、 **+** アイコンをクリックしてロードを追加します。 確認メッセージが表示されます。 
    
3. **[はい]** をクリックして続行します。 [**新しい読み込みの追加**] ダイアログが表示されます。 
    
    > [!NOTE]
    > 以前のロードに対してアクションが実行された場合にのみ、新しいロードを追加できます。 
  
4. [**新しい負荷の追加**] ダイアログで、[**読み込み名**] と [**説明**] に情報を入力し、[ **OK**] をクリックします。 高度な電子情報開示新しい負荷を追加します。
    
5. 新しいロードファイルをインポートするには、[**ファイルの追加**] をクリックします。 すべての新しいファイルがこの負荷に追加されます。 詳細な電子情報開示は、ファイルをインポートした後、ローリングロードシナリオを認識し、次の手順としてキャッチアップを示します。
    
6. ダイアログボックスの下部にある [**キャッチアップ**] をクリックして、シナリオを実行します。 
    
    ファイルへの同時タグ付けを可能にするすべての問題について、通常、新しいロードから 200 ~ 2000 ファイルを含む単一のキャッチアップセットが作成されます。
    
    負荷が類似または特徴的かどうか、高度な電子情報開示を統合するか分割するか、または次の手順での処理に関する情報についての詳細が表示されます。
    
    その後、ファイルにタグを付けて、計算操作を実行できます。 タグ付けを使用すると、負荷が類似または特徴的かどうかを判断し、新しいファイルセットで作業を続行することができます。
    
7. キャッチアップセットがレビューされた後、キャッチアップ結果の**関連性\>トラック**を表示します。 
    
1. 関連性のあるトレーニング中に新しいファイルの読み込みが追加された場合 (つまり、その問題がまだバッチ計算を通過していない場合)、キャッチアップ結果に関係なく、次の手順で**トレーニングを続行**します。 
    
    新しいおよび以前の負荷は、1つの負荷として処理され、関連のトレーニングは米国で続行されます。 これで、この手順が完了し、関連のトレーニングを続行できます。 
    
2. バッチ計算後に新しいロードが追加された場合は、次の手順に進みます。
    
8. バッチ計算後に新しい負荷が追加された場合、Advanced eDiscovery は、次のように、新しい負荷が以前の負荷と類似しているか、または異なるかを判断します。
    
1. 同じような負荷が発生した場合は、追加の関連性トレーニングは不要です。 ダッシュボードでは、「* * Batch calculation * *」を再度実行して、新しい負荷の関連性スコアを計算することをお勧めします。 類似していることが判明したので、前の分類子分析を新しいファイルに対して実行することができます。 
    
2. 明確な負荷が見つかった場合は、より関連性のトレーニングが必要であり、次の手順ではキャッチアップが決定されます。 次のようにして、キャッチアップの決定を選択します。
    
    [負荷の**マージ**] を選択した場合、上級電子情報開示では、トレーニングセットの以前の負荷と新しい負荷をマージします。 最初の読み込みはバッチ計算を通じて行われましたが、多くのトレーニングが必要です。 新規および以前の負荷を一緒にトレーニングを続行します。 バッチ計算は再実行され、以前のバッチ計算スコアを無視する必要があります。 既存の負荷の関連性スコアを再計算する場合、たとえば、既存のファイルの読み込みが開始されていない場合は、このオプションを選択します。
    
    **分割荷重**を選択する場合は、新しい負荷でのみ関連のトレーニングを続行します。 この例では、以前のバッチ計算のスコアはそのまま残ります。 既存の負荷の既存の関連性スコアを再計算できない場合、たとえば既存の負荷の確認が既に開始されている場合は、このオプションを選択します。 関連性スコアはこの点以降の個別に管理され、結合することはできません。
    
3. [**トレーニングの続行**] をクリックします。
    
## <a name="see-also"></a>関連項目

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[問題の定義とユーザーの割り当て](define-issues-and-assign-users.md)
  
[強調表示されたキーワードと詳細オプションの定義](define-highlighted-keywords-and-advanced-options.md)
