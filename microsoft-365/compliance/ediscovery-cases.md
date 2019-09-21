---
title: セキュリティ & コンプライアンスセンターの電子情報開示ケース
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 8dd335ab-29d0-41c3-8dd8-9f7c7481e60c
description: セキュリティ & コンプライアンスセンターを使用して、組織内の電子情報開示ケースを作成および管理します。 ケースにメンバーを割り当てたり、コンテンツの場所を保持に配置したり、ケースに関連付けられたコンテンツ検索を実行したり、検索結果をエクスポートしたりすることができます。 また、高度な電子情報開示に関する詳細な分析のためにケースデータを準備することもできます。
ms.openlocfilehash: f0487a7657b1d6cc4374bfc7308092285aebc979
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2019
ms.locfileid: "37085755"
---
# <a name="ediscovery-cases-in-the-security--compliance-center"></a>セキュリティ & コンプライアンスセンターの電子情報開示ケース

Office 365 および Microsoft 365 のコンプライアンスセンターで電子情報開示ケースを使用して、組織内で電子情報開示ケースを作成、アクセス、および管理できるユーザーを制御することができます。 組織に Office 365 E5 サブスクリプションがある場合は、Office 365 Advanced eDiscovery を使用して、電子情報開示ケースを使用して検索結果を分析することもできます。
  
電子情報開示ケースを使用すると、ケースへのメンバーの追加、特定のケース メンバーが実行可能なアクションの種類の制御、訴訟事件に関連のあるコンテンツの場所の保留、複数のコンテンツ検索と 1 つのケースの関連付けを実行できます。また、ケースに関連付けられたコンテンツ検索の結果をエクスポートしたり、Advanced eDiscovery で分析できるように検索結果を準備したりできます。電子情報開示ケースは、組織内の特定の訴訟事件に関するコンテンツ検索と検索結果にアクセスできるユーザーを制限するのに適切な方法です。
  
次のワークフローを使用して、セキュリティ & コンプライアンスセンターと高度な電子情報開示の電子情報開示ケースを設定および使用します。

[手順 1: 潜在的なケースのメンバーに電子情報開示のアクセス許可を割り当てる](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[手順 2: 新しいケースを作成する](#step-2-create-a-new-case)

[手順 3: ケースにメンバーを追加する](#step-3-add-members-to-a-case)

[手順 4: コンテンツの場所を保留にする](#step-4-place-content-locations-on-hold)

[手順 5: ケースに関連付けられているコンテンツ検索を作成して実行する](#step-5-create-and-run-a-content-search-associated-with-a-case)

[手順 6: ケースに関連付けられているコンテンツ検索の結果をエクスポートする](#step-6-export-the-results-of-a-content-search-associated-with-a-case)

[手順 7: Advanced eDiscovery 用に検索結果を準備する](#step-7-prepare-search-results-for-advanced-ediscovery)

[手順 8: Advanced eDiscovery のケースに移動する](#step-8-go-to-the-case-in-advanced-ediscovery)

[(省略可能) 手順 9: ケースを閉じる](#optional-step-9-close-a-case)

[(省略可能) 手順 10: 閉じたケースを再度開く](#optional-step-10-re-open-a-closed-case)

[詳細情報](#more-information)
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>手順 1: 潜在的なケースのメンバーに電子情報開示のアクセス許可を割り当てる

最初の手順として、適切な電子情報開示関連のアクセス許可をユーザーに割り当てて、手順2で電子情報開示ケースに追加できるようにします。 電子情報開示のアクセス許可を割り当てるには、セキュリティ & コンプライアンスセンターで、組織の管理役割グループのメンバーであるか (または、役割管理役割が割り当てられている必要があります)。 次の一覧は、セキュリティ & コンプライアンスセンターの電子情報開示関連の役割グループを示しています。 
  
- **レビュー担当者**-この役割グループには、電子情報開示関連のアクセス許可が最も制限されています。 この役割グループの主な目的は、メンバーが Office 365 Advanced eDiscovery でケースデータの表示とアクセスを行えるようにすることです。 このグループのメンバーは、自分が所属しているセキュリティ & コンプライアンスセンターの**電子情報開示**ページでのみ、ケースのリストを表示して開くことができます。 セキュリティ/コンプライアンスセンターでユーザーがケースにアクセスした後、[ **Advanced ediscovery に切り替え**] をクリックすると、高度な電子情報開示でケースデータにアクセスして分析することができます。 ケースを作成したり、ケースにメンバーを追加したり、ホールドを作成したり、検索を作成したり、検索結果をプレビューしたり、検索結果をエクスポートしたり、高度な電子情報開示の結果を準備したりすることはできません。 
    
- **電子情報開示マネージャー** - この役割グループのメンバーは、電子情報開示ケースを作成して管理できます。このメンバーは、ケースへのメンバーの追加と削除、コンテンツの場所の保留、ケースに関連付けられたコンテンツ検索の作成と編集、コンテンツ検索の結果のエクスポート、Advanced eDiscovery で分析するための検索結果の準備ができます。この役割グループには 2 つのサブグループがあります。これらのサブグループの違いは、範囲に基づきます。
    
  - **電子情報開示マネージャー** -自分が作成またはメンバーとなっている電子情報開示ケースを表示および管理できます。 別の電子情報開示管理者が作成したケースのメンバーとして2番目の電子情報開示マネージャーを追加しなかった場合、2番目の電子情報開示マネージャーは、セキュリティ & コンプライアンスセンターの [**電子情報開示**] ページでケースを表示または開くことができません。 電子情報開示マネージャーは、高度な電子情報開示のケースにアクセスして分析タスクを実行することもできます。 
    
  - **電子情報開示管理者** - 電子情報開示マネージャーが実行できるすべてのケースの管理タスクを実行できます。さらに、電子情報開示管理者は、次のことができます。
    
    - [**電子情報開示**] ページにリストされたすべてのケースを表示する。 
    
    - 自分自身をケースのメンバーとして追加した後、組織のすべてのケースを管理する。
    
    - Advanced eDiscovery で組織内のすべてのケースに関するケース データにアクセスする。
    
    組織に電子情報開示管理者が必要な理由については、「[詳細情報](#more-information)」セクションをご覧ください。 
    
> [!IMPORTANT]
> あるユーザーが、これらの電子情報開示関連のどの役割グループのメンバーでもなく、レビュー担当者の役割が割り当てられた役割グループのメンバーでもない場合は、そのユーザーを電子情報開示ケースのメンバーとして追加することはできません。 

EDiscovery アクセス許可の詳細については、「[電子情報開示のアクセス許可を割り当てる](assign-ediscovery-permissions.md)」を参照してください。
  
 **電子情報開示のアクセス許可を割り当てるには:**
  
1. [https://protection.office.com](https://protection.office.com) に移動します。
    
2. 職場または学校のアカウントを使用して、Office 365 にサインインします。
    
3. [セキュリティ & コンプライアンスセンター] で、[**アクセス許可**] をクリックし、割り当てる電子情報開示のアクセス許可に基づいて次のいずれかを実行します。
    
    - レビュー担当者のアクセス許可を割り当てるには、[**レビュー担当者**] 役割グループを選択し、[**メンバー**] の横にある [**編集**] をクリックします。[**メンバーの選択**]、[**編集**]、[![追加アイコン](media/ITPro-EAC-AddIcon.gif) **追加**] の順にクリックし、レビュー担当者の役割グループに追加するユーザーを選択してから、[**追加**] をクリックします。
    
    - 電子情報開示マネージャーのアクセス許可を割り当てるには、[**電子情報開示管理者**] 役割グループを選択し、[**電子情報開示マネージャー**] の横にある [**編集**] をクリックします。[**電子情報開示マネージャーの選択**]、[**編集**]、[![追加アイコン](media/ITPro-EAC-AddIcon.gif) 追加] の順にクリックし、電子情報開示マネージャーとして追加するユーザーを選択してから [**追加**] をクリックします。
    
    - 電子情報開示管理者のアクセス許可を割り当てるには、[**電子情報開示マネージャー**] 役割グループを選択し、[**電子情報開示管理者**] の横にある [**編集**] をクリックします。[**電子情報開示管理者の選択**]、[**編集**]、[![追加アイコン](media/ITPro-EAC-AddIcon.gif) **追加**] の順にクリックし、電子情報開示管理者として追加するユーザーを選択してから [**追加**] をクリックします。
    
4. すべてのユーザーを追加した後、[**完了**]、[**保存**] の順にクリックして変更を役割グループに保存してから、[**閉じる**] をクリックします。

## <a name="step-2-create-a-new-case"></a>手順 2: 新しいケースを作成する

次の手順では、新しい電子情報開示ケースを作成します。 電子情報開示のケースを作成するには、電子情報開示マネージャー役割グループのメンバーである必要があります。 前述のとおり、セキュリティ & コンプライアンスセンターで新しいケースを作成すると、組織に Office 365 E5 サブスクリプションがある場合に、上級電子情報開示でその同じケースにアクセスできるようになります。
  
1. [https://protection.office.com](https://protection.office.com) に移動します。
    
2. 職場または学校のアカウントを使用して、Office 365 にサインインします。
    
3. セキュリティ & コンプライアンスセンターで、[**電子情報** \> **開示電子情報開示**] ![をクリック](media/ITPro-EAC-AddIcon.gif)し、[追加] アイコンをクリックして**ケースを作成**します。
    
4. [**新しいケース**] ページで、ケースに名前を付け、オプションで説明を入力し、[**保存**] をクリックします。ケース名は組織内で一意である必要があることに注意してください。
    
    ![新しいケースを作成する](media/7f78f83b-1525-4c77-9888-4b6bda1e148d.png)
  
    新しいケースは、[**電子情報開示**] ページのケースのリストに表示されます。なお、ケース名の上にカーソルを置くと、ケースの状態 ([**アクティブ**] または [**閉じる**])、(前述の手順で作成した) ケースの説明、ケースの最終更新日および更新者を含む、ケースの情報を表示できます。
    
    > [!TIP]
    > 新しいケースを作成した後に、いつでも名前を変更することができます。[**電子情報開示**] ページのケース名をクリックするだけです。[**このケースの管理**] ポップアップ ページで、[**名前**] のボックスに表示される名前を変更してから、変更を保存します。 
  
## <a name="step-3-add-members-to-a-case"></a>手順 3: ケースにメンバーを追加する

新しいケースを作成したら、次の手順はケースにメンバーを追加することです。前述のように、ケースのメンバーとして追加できるのは、レビュー担当者または電子情報開示マネージャー役割グループのメンバーであるユーザーだけです。なお、ケースを作成した電子情報開示マネージャーは自動的にメンバーとして追加されます。
  
1. [セキュリティ & コンプライアンスセンター] で、[**電子情報** \> **開示電子情報開示**] をクリックして、組織内のケースの一覧を表示します。 
    
2. メンバーを追加するケースの名前をクリックします。
    
    [**このケースを管理**] ポップアップ ページが表示されます。 
    
    ![ケースの管理ポップアップ ページ](media/11f35ceb-6c98-4580-a3bc-ad688e9c7af9.png)
  
3. [**メンバーの管理**] で、[![追加アイコン](media/ITPro-EAC-AddIcon.gif) **追加**] をクリックして、ケースにメンバーを追加します。 
    
    ケースに役割グループを追加することもできます。[**役割グループの管理**] で、[![追加アイコン](media/ITPro-EAC-AddIcon.gif) **追加**] をクリックします。
    
    > [!NOTE]
    > 役割グループで、電子情報開示ケースにメンバーを割り当てることができるユーザーが制御されます。つまり、ケースにはメンバーである役割グループのみを割り当てることができます。
    
4. ケースのメンバーとして追加できるユーザーまたは役割グループのリストで、追加するユーザーまたは役割グループの名前の横にあるチェック ボックスをオンにします。
    
    > [!TIP]
    > メンバーとして追加できるユーザーが多数いる場合は、[**検索**] ボックスを使用してリストで特定のユーザーを検索します。 
  
5. グループのメンバーとして追加するユーザーまたは役割グループを選択したら、[**追加**] をクリックします。
    
    [**このケースを管理**] で、[**保存**] をクリックして、ケース メンバーの新しいリストを保存します。 
    
6. [**保存**] をクリックして、ケース メンバーの新しいリストを保存します。 
  
## <a name="step-4-place-content-locations-on-hold"></a>手順 4: コンテンツの場所を保留にする

電子情報開示ケースを使用して、ケースに関連する可能性があるコンテンツを保持するための保留を作成できます。ケースのカストディアンであるユーザーのメールボックスと OneDrive for Business サイトを保留にできます。Office 365 グループのグループ メールボックス、SharePoint サイト、および OneDrive for Business サイトも保留にすることができます。同様に、Microsoft Teams と関連付けられているメッセージボックスとサイトを保留にすることができます。コンテンツの場所を保留にすると、コンテンツの場所の保留を解除するか、または保留を削除するまでコンテンツは保持されます。

> [!NOTE]
> コンテンツの場所を保留にした後、保留が有効になるまで最大で 24 時間かかります。 
>   
保留リストを作成するときに、指定されたコンテンツの場所に保持されているコンテンツの範囲を指定する場合は、次のオプションがあります。
  
- すべてのコンテンツが保留にされている場合、無限の保留リストを作成します。また、検索クエリに一致したコンテンツのみが保留にされている場合、クエリ ベースの保留リストも作成できます。
    
- 日付の範囲を指定して、その日付の範囲内に送信、受信、または作成したコンテンツのみを保留にすることができます。また、コンテンツがいつ送信、受信、作成されたかにかかわらず、すべてのコンテンツを保留にすることもできます。
    
> [!NOTE]
> 組織内のすべての電子情報開示ケース全体で、最大 10,000 個のポリシーを保留にすることができます。 
  
電子情報開示ケースの保留リストを作成するには、次のようにします。
  
1. [セキュリティ & コンプライアンスセンター] で、[**電子情報** \> **開示電子情報開示**] をクリックして、組織内のケースの一覧を表示します。 
    
2. 保留リストを作成するケースの横の [**開く**] をクリックします。 
    
3. ケースの [**ホーム**] ページで、[**保留**] タブをクリックします。 
    
    ![[保留] タブをクリックする](media/3fef2db4-36de-4517-a34d-82f47b82d9bf.png)
  
4. [**保留**] ページで、[![追加アイコン](media/ITPro-EAC-AddIcon.gif) **作成**] をクリックします。
    
5. [**保留リストの名前を設定**] ページで、保留リストに名前を付けます。保留リストの名前は組織内で一意である必要があります。 
    
    ![保留リストに一意の名前を付ける](media/7e15ea63-abd1-4f14-a29c-7ecfb9571d2c.png)
  
6. (省略可能) [**説明 **] ボックスで、保留リストの説明を追加します。 
    
7. [**次へ**] をクリックします。
    
8. 保留にするコンテンツの場所を選択します。メールボックス、サイト、パブリック フォルダーを保留にできます。
    
    ![保留にするコンテンツの場所を選択する](media/a59e4265-9151-4dbf-913f-6a4ab8db06b4.png)
  
   a. **Exchange メール** - [**ユーザー、グループ、またはチームの選択**] をクリックし、もう一度 [**ユーザー、グループ、またはチームの選択**] をクリックして保留にするメールボックスを指定します。検索ボックスを使用して、保留にする (グループメンバーのメールボックスを保留にする) ユーザーのメールボックスと配布グループを検索します。Office 365 グループまたは Microsoft チームの関連付けられているメールボックスを保留にすることもできます。ユーザー、グループ、チームのチェック ボックスをオンにし、[**選択**]、[**完了**] の順にクリックします。
    
    > [!NOTE]
    > [**ユーザー、グループ、またはチームの選択**] をクリックして保留にするメールボックスを指定するときに、表示されるメールボックス ピッカーは空の状態です。これは、パフォーマンスを向上させるための仕様です。このリストにユーザーを追加するには、検索ボックスに名前 (3 文字以上) を入力します。 
  
   b. **SharePoint サイト** - [**サイトの選択**] をクリックし、もう一度 [**サイトの選択**] をクリックして保留にする SharePoint および OneDrive for Business サイトを指定します。保留にする各サイトの URL を入力します。Office 365 グループまたは Microsoft チーム用の SharePoint サイトの URL を追加することもできます。[**選択**]、[**完了**] の順にクリックします。
    
    Office 365 グループと Microsoft Teams を保留にする場合のヒントについては、「[詳細情報](#more-information)」を参照してください。 
    
    > [!NOTE]
    > ユーザーのユーザー プリンパル名 (UPN) が変更されるまれなケースでは、その OneDrive アカウントの URL も新しい UPN を組み込むために変更されます。このような場合は、ユーザーの新しい OneDrive URL を追加し、古いものを削除して、保留リストを変更する必要があります。 
  
   **Exchange パブリック フォルダー** - トグル スイッチ ![トグル コントロール](media/963dfcd0-1765-4306-bcce-c3008c4406b9.png)を [**すべて**] の位置に移動し、Exchange Online 組織内のパブリック フォルダーをすべて保留にします。保留にする特定のパブリック フォルダーは選択できないことに注意してください。パブリック フォルダーを保留にしない場合は、トグル スイッチを [**なし**] に設定したままにしておいてください。
    
9. 保留リストにコンテンツの場所を追加し終わったら、[**次へ**] をクリックします。
    
10. 条件付きのクエリ ベースの保留リストを作成するには、次の手順を行います。それ以外の場合は、[**次へ**] をクリックするだけです。
    
    ![条件付きのクエリ ベースの保留リストを作成する](media/d587b58e-d05c-4ac0-b0fe-09019e4f1063.png)
  
    
       a. [**キーワード**] の下にあるボックスに、検索条件を満たすコンテンツのみが保留にされるように、検索クエリを入力します。キーワード、メッセージ プロパティ、またはファイル名などのドキュメント プロパティを指定することができます。**AND**、**OR**、または **NOT** などのブール演算子を使用する、より複雑なクエリを使用することもできます。キーワード ボックスを空のままにすると、指定されたコンテンツの場所にあるすべてのコンテンツが保留にされます。
    
    b. [![追加アイコン](media/ITPro-EAC-AddIcon.gif) **条件の追加**] をクリックして、1 つまたは複数の条件を追加し、保留リストの検索クエリの条件を絞り込みます。保留リストの作成時に、作成され実行される KQL 検索クエリに、条件ごとの句が追加されます。たとえば、指定した日付の範囲内に作成されたメールまたはサイトのドキュメントが保留にされるように、日付の範囲を指定できます。条件は **AND** 演算子によってキーワード クエリ (キーワード ボックスで指定) に論理的に接続されます。つまり、アイテムは、キーワード クエリと保留にする条件の両方を満たす必要があります。

    検索クエリの作成と条件の使用の詳細については、「[コンテンツ検索のキーワード クエリと検索条件](keyword-queries-and-search-conditions.md)」を参照してください。
    
11. クエリ ベースの保留リストを構成した後、[**次へ**] をクリックします。
    
12. 設定を確認し、[**この保留リストを作成**] をクリックします。
    
### <a name="hold-statistics"></a>保留アイテムの統計情報

しばらくすると、選択した保留アイテムの詳細ウィンドウの [**保留リスト**] ページに、新しい保留アイテムに関する情報が表示されます。この情報には、保留中のメッセージボックスとサイトの数、保留にされたコンテンツに関する統計情報 (保留にされたアイテムの合計数とサイズ、保留アイテムの統計情報の最終計算時など) が含まれます。この保留アイテムの統計情報から、電子情報開示ケースに関連するコンテンツがどのくらい保留にされているかを確認できます。 
  
![保留アイテムの統計情報](media/575cfe0a-9210-4ae4-8df8-65665d66712e.png)
  
保留アイテムの統計情報については、次の点に注意してください。
  
- 保留にされているアイテムの合計数は、すべてのコンテンツ ソースのうち、保留にされているアイテム数を示します。クエリベースの保留リストを作成した場合、この統計情報は、クエリに一致するアイテム数を示します。
    
- 保留にされているアイテム数には、コンテンツの場所で見つかった、インデックスのないアイテムも含まれます。クエリベースの保留リストを作成した場合、コンテンツの場所にあるインデックスのないすべてのアイテムは保留にされます。これには、クエリベースの保留リストの検索条件と一致しないインデックスのないアイテムと、日付範囲の条件から外れる可能性のあるインデックスのないアイテムが含まれます。これは、コンテンツ検索を実行したときの結果とは異なります。コンテンツ検索の場合、検索クエリと一致しないインデックスのないアイテム、または日付範囲の条件によって除外されるアイテムは、検索結果に含まれません。インデックスのないアイテムの詳細については、「[Office 365 のコンテンツ検索で部分的にインデックスが作成されたアイテム](partially-indexed-items-in-content-search.md)」を参照してください。
    
- 最新の保留アイテムの統計情報を取得するには、[**統計を更新**] をクリックし、現在保留にされているアイテム数を計算する検索見積もりを再実行します。必要に応じて、ツール バーの [**更新**] ![更新アイコン](media/O365-MDM-Policy-RefreshIcon.gif) をクリックして、詳細ウィンドウの保留アイテムの統計情報を更新します。 
    
- 通常、保留にされているアイテム数は時間と共に増えます。これは、メッセージ ボックスまたはサイトが保留にされているユーザーは、一般的に新しいメール メッセージを送受信し、新しい SharePoint および OneDrive for Business ドキュメントを作成するためです。
    
> [!NOTE]
> SharePoint サイトまたは OneDrive アカウントが複数地域環境内の別の領域に移動された場合、そのサイトの統計情報は保留アイテムの統計情報には含まれません。ただし、サイト内のコンテンツは引き続き保留にされます。また、サイトが別の領域に移動された場合、保留リストに表示される URL は更新されません。保留リストを編集し、URL を更新する必要があります。 
  
## <a name="step-5-create-and-run-a-content-search-associated-with-a-case"></a>手順 5: ケースに関連付けられているコンテンツ検索を作成して実行する

電子情報開示のケースを作成し、ケースに関連する管理者にホールドを適用したら、ケースに関連付けられた 1 つ以上のコンテンツ検索を作成して、実行できます。 ケースに関連付けられたコンテンツ検索は、セキュリティ & コンプライアンスセンターの [**検索**] ページに表示されません。 つまり、ケースに関連付けられたコンテンツ検索は、電子情報開示マネージャー役割グループのメンバーを兼ねているケースのメンバーのみがアクセスできます。 
  
1. [セキュリティ & コンプライアンスセンター] で、[**電子情報** \> **開示電子情報開示**] をクリックして、組織内のケースの一覧を表示します。 
    
2. コンテンツ検索を作成するケースの横の [**開く**] をクリックします。 
    
3. ケースの [**ホーム**] ページで、[**検索**] タブをクリックします。 
    
    ![[検索] タブ](media/2e15fe32-1a2e-4588-ad0b-5d96f77cece9.png)
  
4. [**検索**] ページで、[![追加アイコン](media/ITPro-EAC-AddIcon.gif) **新しい検索**] をクリックします。 
    
5. [**新しい検索**] ページで、キーワードと条件を追加して検索クエリを作成できます。 
    
    ![新しい検索](media/0e9954e7-c0ea-4e05-820b-e4b81dc5f81d.png)
  
6. キーワード、メッセージのプロパティ (送信日、受信日など)、またはドキュメントのプロパティ (ファイル名、ドキュメントの最終変更日など) を指定できます。**AND**、**OR**、**NOT**、**NEAR**、**ONEAR** などのブール演算子を使用する、より複雑なクエリを使用できます。また、ドキュメント内の機密情報 (社会保障番号など) や、外部で共有されているドキュメントを検索することもできます。キーワード ボックスを空のままにすると、指定したコンテンツの場所にあるすべてのコンテンツが検索結果に含まれます。 
    
7. [**キーワード リストの表示**] チェック ボックスをオンにして、各行にキーワードを入力することができます。この操作を行うと、各行のキーワードが、作成された検索クエリの **OR** 演算子で接続されます。 
    
    ![キーワード リスト](media/29cceb5d-2817-4fc4-b91a-ced1c5824a17.png)
  
    キーワード リストを使用するのはなぜですか。各キーワードと一致するアイテム数を示す統計情報を取得することができます。これは、最も有効な (および最も有効でない) キーワードをすばやく識別するのに役立ちます。行で (かっこで囲まれた) キーワード フレーズを使用することもできます。検索統計の詳細については、「[コンテンツ検索結果のキーワード統計の表示](view-keyword-statistics-for-content-search.md)」を参照してください。
    
    キーワード リストの使用の詳細については、「[検索クエリを作成する](content-search.md#building-a-search-query)」を参照してください。
    
8. [**条件**] で、検索クエリに条件を追加し、検索を絞り込み、より絞り込まれた結果セットが返されるようにします。各条件によって、句が KQL 検索クエリに追加されます。KQL 検索クエリは、検索の開始時に作成され、実行されます。条件は **AND** 演算子によってキーワード クエリ (キーワード ボックスで指定) に論理的に接続されます。つまり、アイテムは、キーワード クエリと、結果に含める条件の両方を満たす必要があります。このように、条件は結果を絞り込むのに役立ちます。 
    
    検索クエリの作成と条件の使用の詳細については、[コンテンツ検索のキーワード クエリ](keyword-queries-and-search-conditions.md)に関するページを参照してください。
    
9. [**場所: 保留になっている場所**] で、検索するコンテンツの場所を選択します。同じ検索で、メールボックス、サイト、パブリック フォルダーを検索できます。
    
    ![場所、保留になっている場所](media/d56398aa-0b20-4500-8e26-494eab92a99f.png)
  
    - **すべての場所** - 組織内のすべてのコンテンツの場所を検索するには、このオプションを選択します。このオプションを選択すると、すべての Exchange メールボックス (すべての Office 365 グループおよび Microsoft Teams のメールボックスを含む)、すべての SharePoint および OneDrive for Business サイト (すべての Office 365 グループおよび Microsoft Teams のサイトを含む)、およびすべてのパブリック フォルダーを検索することを選択できます。
    
    - **保留になっているすべての場所** - このケースで保留になっているすべてのコンテンツの場所を検索するには、このオプションを選択します。ケースに保留が複数ある場合にこのオプションを選択すると、すべての保留のコンテンツの場所が検索されます。また、コンテンツの場所がクエリによって保留となっている場合、この手順で作成するコンテンツ検索の実行では、保留中のアイテムのみが検索されます。たとえば、特定の日付前に送信または作成されたアイテムを保持するクエリを使用したケースの保留がある場合、コンテンツ検索のその検索基準を使用すると、このようなアイテムのみが検索されます。これは、ケースの保留クエリと、コンテンツ検索クエリを **AND** 演算子で接続して行われます。ケース コンテンツの検索の詳細については、この記事の最後の「[詳細情報](#more-information)」セクションを参照してください。 
    
    - **特定の場所** - 検索するメールボックスとサイトを選択するには、このオプションを選択します。このオプションを選択し、[**変更**] をクリックすると、場所のリストが表示されます。ユーザー、グループ、チーム、サイトの場所のいずれかまたはすべてを検索するように選択できます。
    
      ![特定の場所を選択する](media/97469b15-7be1-4aee-be27-f8343636152c.png)
  
      組織内のすべてのパブリック フォルダーを検索するように選択することもできますが、このオプションを選択して、保留中の任意のコンテンツの場所を検索すると、検索クエリにはクエリを使用したケースが保留となっているケースは適用されません。つまり、クエリを使用したケースの保留によって保持されているコンテンツだけでなく、場所のすべてのコンテンツが検索されます。
    
      事前に入力したケースのコンテンツの場所を削除するか、新しい場所を追加できます。このオプションを選択すると、特定のサービスのすべてのコンテンツの場所を検索 (すべての Exchange メールボックスを検索するなど) したり、サービスの特定のコンテンツの場所を検索したりすることができ、柔軟性が高まります。また、組織内のパブリック フォルダーを検索するかどうかを選択することもできます。
    
      検索するコンテンツの場所を追加する場合は、次のことに注意してください。
    
      - [**ユーザー、グループ、またはチームの選択**] をクリックして検索するメールボックスを指定するときに、表示されるメールボックス ピッカーは空の状態です。これは、パフォーマンスを向上させるための仕様です。このリストに受信者を追加するには、[**ユーザー、グループ、またはチームの選択**] をクリックし、検索ボックスに名前 (3 文字以上) を入力して、名前の横にあるチェック ボックスをオンにしてから [**選択**] をクリックします。 
    
      - 非アクティブのメールボックス、Office 365 グループ、Microsoft Teams、および配布グループを検索するメールボックスのリストに追加できます。動的配布グループはサポートされません。Office 365 グループまたは Microsoft Teams を追加すると、グループまたはチームのメールボックスが検索されます。グループ メンバーのメールボックスは検索されません。
    
      - サイトを追加するには、[**サイトの選択**] をクリックし、もう一度 [**サイトの選択**] をクリックしてから、検索する各サイトの URL を入力します。Office 365 グループと Microsoft Teams の SharePoint サイトの URL も追加できます。 
    
10. 検索するコンテンツの場所を選択したら、[**完了**]、[**次へ**] の順にクリックします。
    
11. [**新しい検索**] ページで、[**保存**] をクリックしてから、検索の名前を入力します。ケースに関連付けられたコンテンツ検索の名前は、Office 365 組織内で一意である必要があります。 
    
12. [**保存して実行**] をクリックして、検索設定を保存します。 
    
13. 検索の一意の名前を入力し、[**保存**] をクリックして検索を開始します。 
    
    検索が始まります。しばらくすると、検索結果の見積もりが詳細ウィンドウに表示されます。見積もりには、検索条件と一致したアイテムの合計サイズと数が含まれます。また、検索見積もりには、検索されたコンテンツの場所にあるインデックスのないアイテム数も含まれます。検索条件を満たさないインデックスなしアイテムの数は、詳細ウィンドウに表示される検索の統計情報に含まれます。(他のメッセージまたはドキュメントのプロパティが検索条件と一致するため) インデックスなしアイテムが検索クエリと一致する場合、インデックスなしアイテムの見積もり数には含まれません。検索条件によってインデックスのないアイテムが除外される場合、インデックスのないアイテムの見積もりにも含まれません。
    
  検索が完了した後、検索結果をプレビューすることができます。必要に応じて、[**更新**] ![更新アイコン](media/O365-MDM-Policy-RefreshIcon.gif) をクリックして詳細ウィンドウの情報を更新します。 
    
## <a name="step-6-export-the-results-of-a-content-search-associated-with-a-case"></a>手順 6: ケースに関連付けられているコンテンツ検索の結果をエクスポートする

検索の実行が成功したら、検索結果をエクスポートできます。検索結果をエクスポートすると、メールボックス アイテムが PST ファイルまたは個々のメッセージとしてでダウンロードされます。SharePoint サイトと OneDrive for Business サイトからコンテンツをエクスポートすると、ネイティブ Office ドキュメントとその他のドキュメントのコピーがエクスポートされます。各検索結果に関する情報を含むマニフェスト ファイル (XML 形式) もエクスポートされます。
  
[ケースに関連付けられている 1 つの検索](#export-the-results-of-a-single-search-associated-with-a-case)の結果をエクスポートすることも、[ケースに関連付けられている複数の検索](#export-the-results-of-multiple-searches-associated-with-a-case)の結果をエクスポートすることもできます。
  
### <a name="export-the-results-of-a-single-search-associated-with-a-case"></a>ケースに関連付けられている 1 つの検索の結果をエクスポートする

1. [セキュリティ & コンプライアンスセンター] で、[**電子情報** \> **開示電子情報開示**] をクリックして、組織内のケースの一覧を表示します。 
    
2. 検索をエクスポートするケースの横の [**開く**] をクリックします。 
    
3. ケースの [**ホーム**] ページで [**検索**] をクリックします。
    
4. ケースの検索の一覧で、検索結果をエクスポートする検索をクリックし、![検索結果のエクスポート アイコン](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) [**詳細**] をクリックしてから、ドロップダウン リストから [**結果のエクスポート**] を選択します。 
    
    [**結果のエクスポート**] ページが表示されます。 
    
    ![[結果のエクスポート] ページ](media/ab0bb46d-310b-4374-8644-717146df6676.png)
  
    ケースに関連付けられているコンテンツの検索の結果をエクスポートするワークフローは、**[コンテンツの検索]** ページで検索の検索結果をエクスポートする場合と同じです。 詳細な手順については、「[コンテンツ検索の結果をエクスポート](export-search-results.md)する」を参照してください。
    
    > [!NOTE]
    > 検索されたメールボックスで同じメール メッセージの複数のインスタンスが検出された可能性がある場合でも、検索結果をエクスポートするときに、メール メッセージの 1 つのコピーのみがエクスポートされるようにする重複除去オプションを有効にできます。重複除去および重複したアイテムの特定方法の詳細については、「[電子情報開示検索結果での重複除去](de-duplication-in-ediscovery-search-results.md)」を参照してください。 
  
5. [**エクスポート**] タブをクリックすると、そのケースに対して存在するエクスポート ジョブのリストが表示されます。 
    
    ![[エクスポート] タブ](media/1b84c45e-4ec9-4ecd-9e07-eaf8fc4cc307.png)
  
    先ほど作成したエクスポート ジョブが表示されるようにするには、[**更新**] ![更新アイコン](media/O365-MDM-Policy-RefreshIcon.gif) をクリックして、エクスポート ジョブのリストを更新することが必要な場合があります。なお、エクスポート ジョブの名前は、対応するコンテンツ検索の名前の末尾に **_Export** が付加されたものとなります。 
    
6. 先ほど作成したエクスポート ジョブをクリックすると、詳細ウィンドウに状態の情報が表示されます。この情報には、Microsoft クラウド内の Azure ストレージ領域に転送されたアイテムの割合が含まれます。
    
    すべてのアイテムが転送されたら、[**結果のダウンロード**] をクリックして、検索結果をローカルコンピューターにダウンロードします。 詳細については、「[コンテンツ検索の結果をエクスポート](export-search-results.md)する」のステップ2を参照してください。
    
### <a name="export-the-results-of-multiple-searches-associated-with-a-case"></a>ケースに関連付けられている複数の検索の結果をエクスポートする

ケースに関連付けられている 1 つのコンテンツ検索の結果をエクスポートする代わりに、同じケースの複数の検索の結果を一度にエクスポートすることもできます。1 つずつ検索の結果をエクスポートするより、複数の検索の結果をまとめてエクスポートする方が時間がかからず簡単です。
  
> [!NOTE]
> すべての検索結果を検索するように構成されている場合は、複数の検索の結果をエクスポートすることはできません。 電子情報開示ケースに関連付けられている検索の複数の検索結果のみをエクスポートします。 セキュリティ & コンプライアンスセンターの [**コンテンツ検索**] ページにリストされている複数の検索の結果をエクスポートすることはできません。 
  
1. [セキュリティ & コンプライアンスセンター] で、[**電子情報** \> **開示電子情報開示**] をクリックして、組織内のケースの一覧を表示します。 
    
2. 検索結果をエクスポートするケースの横の [**開く**] をクリックします。 
    
3. ケースの [**ホーム**] ページで [**検索**] をクリックします。
    
4. ケースの検索のリストで、検索結果をエクスポートする複数の検索を選択します。
    
    > [!NOTE]
    > 複数の検索を選択するには、Ctrl キーを押しながら各検索をクリックします。または、最初の検索をクリックし、Shift キーを押したまま最後の検索をクリックすることで、連続する複数の検索をまとめて選択することもできます。 
  
5. 検索を選択した後、[**一括操作**] ページが表示されます。 
    
    ![[一括操作] ページで、[結果のエクスポート] をクリックする](media/f34e3707-a9c1-494f-91a4-da1165aa730a.png)
  
    
6. ![検索結果のエクスポート アイコン](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) [**結果のエクスポート**] をクリックします。

7. [**結果のエクスポート**] ページで、エクスポートに一意の名前を付け、出力オプションを選択し、コンテンツのエクスポート方法を選択します。[**エクスポート**] をクリックします。
    
    ケースに関連付けられている複数のコンテンツ検索から結果をエクスポートするワークフローは、単一の検索の検索結果をエクスポートする場合と同じです。 詳細な手順については、「[コンテンツ検索の結果をエクスポート](export-search-results.md)する」を参照してください。
    
    > [!NOTE]
    > 1 つ以上の検索で検索されたメールボックスで同じメッセージの複数のインスタンスが検出された可能性がある場合でも、ケースに関連付けられている複数の検索から検索結果をエクスポートするときに、メール メッセージの 1 つのコピーのみがエクスポートされるようにする重複除去オプションを有効にすることもできます。重複除去および重複したアイテムの特定方法の詳細については、「[電子情報開示検索結果での重複除去](de-duplication-in-ediscovery-search-results.md)」を参照してください。 
  
8. エクスポートの開始後、[**エクスポート**] タブをクリックすると、そのケースのエクスポート ジョブのリストが表示されます。 
    
    ![[エクスポート] タブ、複数の検索](media/b9505e1b-559f-4a8c-96b3-a3f734753926.png)
  
    先ほど作成したエクスポート ジョブを表示するには、[**更新**] ![更新アイコン](media/O365-MDM-Policy-RefreshIcon.gif) をクリックして、エクスポート ジョブを更新することが必要な場合があります。エクスポート ジョブに含まれる検索が [**検索**] 列にリストされることに注意してください。 
    
8. 先ほど作成したエクスポート ジョブをクリックすると、詳細ウィンドウに状態の情報が表示されます。この情報には、Microsoft クラウド内の Azure ストレージ領域に転送されたアイテムの割合が含まれます。
    
9. すべてのアイテムが転送されたら、[**結果のダウンロード**] をクリックして、検索結果をローカルコンピューターにダウンロードします。 詳細については、「[コンテンツ検索結果をエクスポート](export-search-results.md)する」のステップ2を参照してください。
    
#### <a name="more-information-about-exporting-the-results-of-multiple-searches"></a>複数の検索の結果のエクスポートに関するその他の情報

- 複数の検索の結果をエクスポートするときは、すべての検索の検索クエリを **OR** 演算子を使用して組み合わせた後、組み合わされた検索が開始されます。組み合わされた検索の予想される結果が、選択したエクスポート ジョブの詳細ウィンドウに表示されます。検索結果は、Microsoft クラウドの Azure ストレージ領域に転送されます。転送のステータスも、詳細ウィンドウに表示されます。前述のとおり、すべての検索結果が転送された後、それらをローカル コンピューターにダウンロードできます。 
    
- エクスポートするすべての検索の検索クエリのキーワードの最大数は 500 です (これは、1 つのコンテンツ検索の上限と同じです)。これは、エクスポート ジョブで **OR** 演算子を使用して、すべての検索クエリが組み合わされるためです。この上限を超えた場合は、エラーが返されます。その場合は、結果をエクスポートする検索の数を減らすか、またはエクスポートする検索の検索クエリを簡略化する必要があります。 
    
- エクスポートされる検索結果は、アイテムが見つかったコンテンツ ソースごとにまとめられています。つまり、エクスポート結果のコンテンツ ソースのアイテムが異なる検索で返される可能性があります。たとえば、メールボックスごとに 1 つの PST ファイルにメール メッセージをエクスポートする場合、PST ファイルに複数の検索の結果が含まれることがあります。
    
- 同じコンテンツの場所の同じメール アイテムまたはドキュメントが、エクスポートする複数の検索によって返される場合、アイテムの 1 つのコピーだけがエクスポートされます。 
    
- 作成した後で複数の検索のエクスポートを編集することはできません。たとえば、エクスポートの検索を追加または削除することはできません。エクスポートされる検索結果を変更するには、新しいエクスポート ジョブを作成する必要があります。エクスポート ジョブを作成した後で行うことができるのは、コンピューターへの結果のダウンロード、エクスポートの再実行、またはエクスポート ジョブの削除だけです。
    
- エクスポートを再実行した場合、エクスポート ジョブを構成する検索のクエリに対する変更は、取得される検索結果に影響しません。エクスポートを再実行すると、エクスポート ジョブを作成したときと同じ組み合わせの検索クエリ ジョブが再び実行されます。
    
- 電子情報開示ケースの [**エクスポート**] ページからエクスポートを再実行した場合、Azure ストレージ領域に転送される検索結果で以前の結果が上書きされます。転送された以前の結果はダウンロードできなくなります。 
    
- Advanced eDiscovery での分析に対して複数の検索結果を準備することはできません。Advanced eDiscovery での分析に対して結果を準備できる検索は 1 つだけです。

## <a name="step-7-prepare-search-results-for-advanced-ediscovery"></a>手順 7: Advanced eDiscovery 用に検索結果を準備する

組織に Office 365 E5 サブスクリプションがある場合、ケースに関連するコンテンツ検索の結果を Advanced eDiscovery で分析する準備ができます。検索結果を準備したら、Advanced eDiscovery に移動し (「[手順 8: Advanced eDiscovery のケースに移動する](#step-8-go-to-the-case-in-advanced-ediscovery)」を参照)、検索結果のデータを Advanced eDiscovery でさらに分析することができます。
  
Advanced eDiscovery の検索結果を準備すると、光学式文字認識 (OCR) 機能によって、画像からテキストが自動的に抽出されます。OCR は、圧縮されていないファイル、メールの添付ファイル、および埋め込み画像の場合にサポートされています。画像ファイルの任意のテキストに Advanced eDiscovery のテキスト分析機能 (類似データ、メールのスレッド化、テーマ、プレディクティブ コーディング) を適用できます。
  
> [!NOTE]
> Advanced eDiscovery を使用してユーザーのデータを分析するには、ユーザー (データの保管担当者) に Office365 E5 ライセンスが割り当てられている必要があります。または、Office365 E1 または E3 ライセンスを持つユーザーに Advanced eDiscovery 単体のライセンスを割り当てることもできます。ケースに割り当てられ、Advanced eDiscovery を使用してデータを分析する管理者および法令遵守責任者には E5 ライセンスは不要です。 
  
1. [セキュリティ & コンプライアンスセンター] で、[**電子情報** \> **開示電子情報開示**] をクリックして、組織内のケースの一覧を表示します。 
    
2. Advanced eDiscovery で分析するために、検索結果を準備するケースの横の [**開く**] をクリックします。 
    
3. ケースの [**ホーム**] ページで [**検索**] をクリックして、検索を選択します。
    
4. 詳細ウィンドウで、![検索結果のエクスポート アイコン](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) [**詳細**] をクリックしてから、[**Advanced eDiscovery に対する準備**] をクリックします。
    
    ![Advanced eDiscovery 用に結果を準備する](media/b6548ff0-a6e9-42b1-9ae4-5c15146f5690.png)
  
5. [**Advanced eDiscovery に対する準備**] ページで、以下のいずれかを準備するように選択します。 
    
    - 形式が認識されていないものを除く、暗号化されている、または他の理由でインデックスが作成されなかったすべてのアイテム。
    
    - 形式が認識されていないものを含む、暗号化されている、または他の理由でインデックスが作成されなかったすべてのアイテム。
    
    - 形式が認識できない、暗号化されている、または他の理由でインデックスが作成されなかったアイテムのみ。
    
6. (省略可能) [**SharePoint ファイルのバージョンを含めます**] チェック ボックスをオンにします。 
    
7. [**準備**] をクリックします。
    
    検索結果が、Advanced eDiscovery を使用して分析するために準備されます。
    
8. [**閉じる**] をクリックして、詳細ウィンドウを閉じます。 
    
## <a name="step-8-go-to-the-case-in-advanced-ediscovery"></a>手順 8: Advanced eDiscovery のケースに移動する

セキュリティ & コンプライアンスセンターでケースを作成した後、上級電子情報開示と同じケースに進むことができます。
  
Advanced eDiscovery のケースに移動するには、次のようにします。
  
1. [セキュリティ & コンプライアンスセンター] で、[**電子情報** \> **開示電子情報開示**] をクリックして、組織内のケースの一覧を表示します。 
    
2. Advanced eDiscovery の移動するケースの横の [**開く**] をクリックします。 
    
3. ケースの [**ホーム**] ページで、[**Advanced eDiscovery に切り替え**] をクリックします。
    
    ![[Advanced eDiscovery に切り替え] を選択する](media/d7e31558-e79c-4782-b841-2b735568a576.png)
  
    [**Advanced eDiscovery に接続しています**] の進行状況バーが表示されます。Advanced eDiscovery に接続されると、ページにコンテナーのリストが表示されます。 
    
    ![Advanced eDiscorvery の進行状況バー](media/4a84273d-765b-44b8-9006-c20e810ea393.png)
  
    これらのコンテナーは、手順7で高度な電子情報開示で分析するために準備した検索結果を表します。 セキュリティ & コンプライアンスセンターでは、コンテナーの名前がコンテンツ検索と同じ名前になっていることに注意してください。 リスト内のコンテナーは、準備したものです。 上級電子情報開示のために別のユーザーが検索結果を準備している場合、対応するコンテナーはリストに含まれません。
    
4. コンテナーから Advanced eDiscovery のケースに検索結果データを読み込むには、コンテナーを選択し、[**プロセス**] をクリックします。
    
    コンテナーの処理方法については、「[Office 365 Advanced eDiscovery でプロセス モジュールを実行し、データを読み込む](run-the-process-module-and-load-data-in-advanced-ediscovery.md)」を参照してください。
    
> [!TIP]
> [**電子情報開示**への切り替え] をクリックして、セキュリティ & コンプライアンスセンターの同じケースに戻ります。 
  
## <a name="optional-step-9-close-a-case"></a>(省略可能) 手順 9: ケースを閉じる

電子情報開示ケースでサポートされる訴訟や捜査が完了したら、ケースを閉じることができます。ケースを閉じたときの動作を示します。
  
- ケースに保留中の任意のコンテンツの場所が含まれている場合、これらの保留が無効になります。この結果、ユーザーまたは自動プロセス (削除ポリシーなど) によってコンテンツが完全に削除または消去される場合があります。  
    
- ケースを閉じると、そのケースに関連付けられている保留だけが無効になります。コンテンツの場所に他の保留 (訴訟ホールド、保持ポリシー、別の電子情報開示ケースからの保留など) がある場合、これらの保留はそのまま保持されます。
    
- ケースは、セキュリティ & コンプライアンスセンターの [電子情報開示] ページに表示されたままになっています。 クローズしたケースの詳細、保持、検索、メンバーは保持されます。
    
- ケースは閉じた後でも編集できます。たとえば、メンバーの追加または削除、検索の作成、検索結果のエクスポート、Advanced eDiscovery で分析するための検索結果の準備が行えます。アクティブ ケースと閉じたケースの主な違いは、ケースを閉じると保留が無効になることです。
    
ケースを閉じるには、次のようにします。
  
1. [セキュリティ & コンプライアンスセンター] で、[**電子情報** \> **開示電子情報開示**] をクリックして、組織内のケースの一覧を表示します。 
    
2. 閉じるケースの名前をクリックします。
    
    [**このケースを管理**] ポップアップ ページが表示されます。 
    
3. [**ケースの状態の管理**] で、![[プレビューの固定を解除] ボタン](media/b6512677-5e7b-42b0-a8a3-3be1d7fa23ee.gif) [**ケースの終了**] をクリックします。
    
    ケースに関連付けられた保留が無効になることを示す警告が表示されます。
    
4. [**はい**] をクリックしてケースを閉じます。 
    
    [**このケースを管理**] ポップアップ ページの状態が [**アクティブ**] から [**閉じています**] に変わります。
    
5. [**このケースを管理**] ページを閉じます。 
    
6. [**電子情報開示**] ページで、![[更新] アイコン](media/O365-MDM-Policy-RefreshIcon.gif) [**更新**] をクリックして、閉じたケースの状態を更新します。閉じるプロセスが完了するまで最大で 60 分かかる場合があります。 
    
    プロセスが完了すると、[**電子情報開示**] ページのケースの状態は [**閉じる**] に変わります。もう一度ケース名をクリックして、[**このケースを管理**] ポップアップ ページを表示します。ここには、ケースが閉じられた時刻とケースを閉じたユーザーの情報が含まれます。 
     
## <a name="optional-step-10-re-open-a-closed-case"></a>(省略可能) 手順 10: 閉じたケースを再度開く

ケースをもう一度開くと、ケースを閉じたときに有効だった保留を自動的に回復することはできません。ケースをもう一度開いた後に、[**保留**] ページに移動して、以前の保留を有効にする必要があります。保留を有効にするには、詳細ウィンドウで保留を選択し、[**オンにする**] をクリックします。 
  
1. [セキュリティ & コンプライアンスセンター] で、[**電子情報** \> **開示電子情報開示**] をクリックして、組織内のケースの一覧を表示します。 
    
2. 再度開くケースの名前をクリックします。
    
    [**このケースを管理**] ポップアップ ページが表示されます。 
    
3. [**ケースの状態を管理する**] で、[**ケースを再度開く**] をクリックします。
    
    ケースを閉じたときに関連付けられていた保留は自動的に有効にならないことを示す警告が表示されます。
    
4. [**はい**] をクリックしてケースを再度開きます。 
    
    [**このケースを管理**] ポップアップ ページの状態が [**閉じる**] から [**アクティブ**] に変わります。
    
5. [**このケースを管理**] ページを閉じます。 
    
6. [**電子情報開示**] ページで、![[更新] アイコン](media/O365-MDM-Policy-RefreshIcon.gif) [**更新**] をクリックして、再度開いたケースの状態を更新します。再度開くプロセスが完了するまで最大で 60 分かかる場合があります。 
    
    プロセスが完了すると、[**電子情報開示**] ページのケースの状態は [**アクティブ**] に変わります。 
  
## <a name="more-information"></a>詳細情報

- **電子情報開示ケースまたは電子情報開示ケースに関連付けられた保留アイテムに制限はありますか。** 次の表には、電子情報開示ケースとケースの保留に関する制限をまとめています。
    
  |**制限の説明**|**制限**|
  |:-----|:-----|
  |組織のケースの最大数  <br/> |制限なし  <br/> |
  |組織のケース保留の最大数  <br/> |10,000  <br/> |
  |1 つのケース保留のメールボックスの最大数  <br/> |1,000  <br/> |
  |1 つのケース保留の SharePoint および OneDrive for Business サイトの最大数  <br/> |100  <br/> |
   
- **Advanced eDiscovery のケース管理ページで作成されたケースについて** 以前の高度な電子情報開示ケースの一覧にアクセスするには、セキュリティ & コンプライアンスセンターの [**電子情報開示**] ページの下部にあるリンクをクリックします。 ただし、以前のケースで作業を行うには、Office 365 サポートに連絡して、セキュリティ & コンプライアンスセンターで、ケースを新しい電子情報開示ケースに移行するよう要求する必要があります。 
    
- **電子情報開示管理者を作成する理由。** 前述のとおり、電子情報開示管理者は、組織内のすべての電子情報開示ケースを表示したり、これらのケースにアクセスしたりできる、電子情報開示マネージャー役割グループのメンバーです。すべての電子情報開示ケースにアクセスする能力には、2 つの重要な目的があります。
    
  - 電子情報開示のケースの唯一のメンバーが組織を退職すると、どのユーザー (組織管理役割グループのメンバー、または電子情報開示マネージャー役割グループの他のメンバーなど) も、ケースのメンバーではないため、その電子情報開示のケースにアクセスできなくなります。 この状況では、ケースのデータにアクセスする方法はありません。 しかし、電子情報開示管理者は組織内のすべての電子情報開示ケースにアクセスできるため、セキュリティ & コンプライアンスセンターでケースを表示し、そのケースのメンバーとして自分または別の電子情報開示マネージャーを追加することができます。
    
  - 電子情報開示管理者は、すべての電子情報開示ケースを表示し、これらのケースにアクセスできるため、すべてのケースと関連するコンテンツ検索の監査と監視を行うことができます。これは、コンテンツ検索または電子情報開示ケースの誤った使い方の防止に役立ちます。さらに、電子情報開示管理者はコンテンツ検索の結果に含まれる潜在的な機密情報にアクセスできるため、電子情報開示管理者となるユーザーの数を制限する必要があります。
    
    最後に説明したように、セキュリティ & コンプライアンスセンターの電子情報開示管理者は、アドバンスト eDiscovery の管理者として自動的に追加されます。 つまり、電子情報開示管理者であるユーザーは、ユーザーの設定、ケースの作成、ケースへのデータの追加など、高度な電子情報開示で管理タスクを実行できます。
    
- **コンテンツの場所を保留にするには、どのようなライセンスが必要ですか。** 一般に、コンテンツの場所を保留にするには、組織に Office 365 E3 サブスクリプション以上が必要です。メールボックスを保留にするには、保留にするメールボックスの Exchange Online プラン 2 のライセンスが必要です。
    
- **ケースのすべてのコンテンツを検索するのに、手順 5 でその他知っておく必要があることはありますか。** 前述のとおり、ケースで保留となっているコンテンツの場所を検索することができます。これを行うときに、保留の基準と一致するコンテンツのみが検索されます。保留の基準がない場合、すべてのコンテンツが検索されます。コンテンツがクエリで保留になっている場合、(手順 4 で保留となった) 保留の基準と (手順 5 の検索からの) 保留基準が検索結果で返されます。
    
    すべてのケースのコンテンツを検索する場合は、次の点に注意してください。
    
  - 同じケース内でコンテンツの場所が複数保留となっている場合、すべてのケースのコンテンツのオプションを使用してコンテンツの場所を検索するときに、保留のクエリは **OR** 演算子によって結合されます。同様に、コンテンツの場所が (1 つはクエリが使用され、もう 1 つはすべてのコンテンツが保留となっている無限の保留である) 2 つの異なる保留の一部である場合、無限の保留のため、すべてのコンテンツが検索されます。 
    
  - コンテンツ検索があるケース用であり、すべてのケースのコンテンツを検索するように構成し、(コンテンツの場所を追加または削除したり、保留のクエリを変更して) 保留を変更したりした場合、検索構成はそれらの変更で更新されます。ただし、検索結果を更新するには、保留が変更されてから検索を再実行する必要があります。
    
  - 電子情報開示ケースのコンテンツの場所で複数のケースが保留となっており、すべてのケースのコンテンツを検索するように選択した場合、その検索クエリのキーワードの最大数は 500 となります。これは、コンテンツ検索で **OR** 演算子を使用して、クエリによるすべての保留が結合されるためです。結合された保留のクエリとコンテンツ検索クエリのキーワードが 500 を超える場合、クエリを使用したケースの保留と一致するもののみでなく、メールボックスのコンテンツがすべて検索されます。 
    
  - 保留のケースの状態が [**有効にしています**] の場合、保留が有効になっている間もケースのコンテンツの場所を検索できます。
    
  - 前述のとおり、検索がすべてのケースのコンテンツを検索するように構成されている場合、複数の検索の結果をエクスポートする場合に、その検索を含めることはできません。検索がケースのすべてのコンテンツを検索するように構成されている場合は、その 1 つの検索の結果をエクスポートする必要があります。
    
- **保留中のメールボックス、SharePoint サイト、または OneDrive アカウントを複数地域の別の領域に移動する場合でも、保留は適用されますか。** いずれの場合も、メールボックス、サイト、または OneDrive アカウントのコンテンツは引き続き保持されます。ただし、保留アイテムの統計情報には、別の領域に移動されたコンテンツの場所のアイテムが含まれなくなります。移動されたコンテンツの場所に関する保留アイテムの統計情報を含めるには、保留リストを編集し、URL (またはメールボックスの SMTP アドレス) を更新して、コンテンツの場所が保留アイテムの統計情報にもう一度含まれるようにする必要があります。 
    
- **Office 365 グループと Microsoft Teams を保留にする場合はどうですか。** Microsoft Teams は Office 365 グループに組み込まれています。そのため、電子情報開示ケースで保留にする場合とよく似ています。Office 365 グループと Microsoft Teams を保留にするときは、次のことに注意してください。 
    
  - Office 365 グループと Microsoft Teams にあるコンテンツを保留にするには、グループまたはチームに関連付けられているメールボックスと SharePoint サイトを指定する必要があります。
    
  - Exchange Online で **Get-UnifiedGroup** コマンドレットを実行し、Office 365 グループまたは Microsoft チームのプロパティを表示します。これは、Office 365 グループまたは Microsoft チームに関連付けられているサイトの URL を取得するのに適した方法です。たとえば、次のコマンドを実行すると、Senior Leadership Team という Office 365 グループの選択したプロパティが表示されます。 
    
     ```
    Get-UnifiedGroup "Senior Leadership Team" | FL DisplayName,Alias,PrimarySmtpAddress,SharePointSiteUrl

     DisplayName            : Senior Leadership Team
     Alias                  : seniorleadershipteam
     PrimarySmtpAddress     : seniorleadershipteam@contoso.onmicrosoft.com
     SharePointSiteUrl      : https://contoso.sharepoint.com/sites/seniorleadershipteam
    ```

    > [!NOTE]
    > **Get-UnifiedGroup** コマンドレットを実行するには、Exchange Online で View-Only Recipients という役割が割り当てられているか、View-Only Recipients という役割が割り当てられている役割グループに属している必要があります。 
  
  - ユーザーのメールボックスを検索すると、ユーザーが属している Office 365 グループまたは Microsoft チームは検索されません。同様に、Office 365 グループまたは Microsoft チームを保留にすると、そのグループ メールボックスとグループ サイトのみが保留にされます。保留リストに明示的に追加しない限り、グループ メンバーのメールボックスと OneDrive for Business サイトは保留にされません。そのため、法的な理由から Office 365 グループまたは Microsoft チームを保留にする必要がある場合は、同じ保留リストにグループとチーム メンバーのメールボックスと OneDrive for Business サイトを追加することを検討してください。
    
  - Office 365 グループまたは Microsoft チームのメンバーの一覧を取得するには、Microsoft 365 管理センターの [**ホーム\>グループ**] ページでプロパティを表示します。 または、Exchange Online PowerShell で次のコマンドを実行することもできます。 
    
      ```
      Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress 
      ```

    > [!NOTE]
    > **Get-UnifiedGroupLinks** コマンドレットを実行するには、Exchange Online で View-Only Recipients という役割が割り当てられているか、View-Only Recipients という役割が割り当てられている役割グループに属している必要があります。 
  
  - Microsoft Teams チャネルが含まれる会話は、Microsoft チームに関連付けられているメールボックスに保存されます。同様に、チャネルでチーム メンバーが共有するファイルはチームの SharePoint サイトに保存されます。そのため、チャネル内の会話とファイルを保持するには、Microsoft チーム メールボックスと SharePoint サイトを保留にする必要があります。
    
    または、Microsoft Teams のチャット リストに含まれる会話は、チャットに参加したユーザーのメールボックスに保存されます。チャットの会話でユーザーが共有するファイルは、ファイルを共有するユーザーの OneDrive for Business サイトに保存されます。そのため、チャット リストの会話やファイルを保持するには、個々のユーザーのメールボックスと OneDrive for Business サイトを保留にする必要があります。これが、チームのメールボックス (とサイト) を保留にするだけでなく、Microsoft チームのメンバーのメールボックスを保留にすることをお勧めする理由です。
    
    > [!IMPORTANT]
    > Microsoft Teams のチャット リストに含まれている会話に参加するユーザーは、メールボックスを電子情報開示の保留対象にするときにチャット会話を保持するために、Exchange Online の (クラウド ベースの) メールボックスを持つ必要があります。この理由は、チャット リストに含まれている会話がチャット参加者のクラウドベースのメールボックスに保存されるためです。チャット参加者が Exchange Online のメールボックスを持っていない場合、チャットの会話を保持できなくなります。たとえば、Exchange のハイブリッド展開では、オンプレミスのメールボックスを持つユーザーは Microsoft Teams のチャット リストに含まれている会話に参加できる可能性があります。ただし、この場合はユーザーにクラウドベースのメールボックスがないため、それらの会話の内容を保持できません。 
  
  - 各 Microsoft チームまたはチーム チャネルには、メモと共同作業用の Wiki が含まれています。Wiki コンテンツは、.mht 形式のファイルに自動的に保存されます。このファイルは、チームの SharePoint サイトの Teams Wiki データ ドキュメント ライブラリに保存されます。Wiki のコンテンツを保留にするには、チームの SharePoint サイトを保留にします。
    
    > [!NOTE]
    > (チームの SharePoint サイトを保留にするときに) Microsoft チームまたはチーム チャネルの Wiki コンテンツを保持する機能は、2017 年 6 月 22 日にリリースされました。チーム サイトが保留にされると、この日から Wiki コンテンツが保持されます。ただし、チーム サイトが保留にされ、Wiki コンテンツが 2017 年 6 月 22 日よりも前に削除された場合、その Wiki コンテンツは保持されていません。 
  
- **OneDrive for Business サイトの URL を見つけるにはどうすればよいですか。** 組織内の OneDrive for Business サイトの URL リストを収集して、電子情報開示ケースに関連する保留または検索リストに追加できるようにするには、[組織内のすべての OneDrive の場所のリストの作成](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a)に関する記事を参照してください。この記事のこのスクリプトでは、すべての OneDrive サイトのリストを含むテキスト ファイルが作成されます。このスクリプトを実行するには、SharePoint Online Management Shell をインストールして使用する必要があります。必ず、検索する各 OneDrive サイトに、組織の MySite ドメインの URL を追加してください。これは、すべての OneDrive を含むドメインです。たとえば、`https://contoso-my.sharepoint.com` です。以下に、ユーザーの OneDrive サイトの URL 例を示します。`https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft.com`。