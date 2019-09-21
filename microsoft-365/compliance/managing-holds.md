---
title: 詳細な電子情報開示で保留リストを管理する
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 1e457ffa05670e6a8b48692bbb382ebd8f2b404e
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2019
ms.locfileid: "37085976"
---
# <a name="manage-holds-in-advanced-ediscovery"></a>詳細な電子情報開示で保留リストを管理する

高度な電子情報開示ケースを使用して、ケースに関連する可能性があるコンテンツを保持するためのホールドを作成できます。 高度な電子情報開示の保持機能を使用すると、保管担当者とそのデータソースに保持を配置できます。 さらに、メールボックスおよび OneDrive for Business サイトに、非 wi-fi ダイヤルを保持することができます。 また、Office 365 グループのグループメールボックス、SharePoint サイト、OneDrive for Business サイトにホールドを配置することもできます。 同様に、Microsoft Teams に関連付けられているメールボックスおよびサイトにホールドを配置することができます。 コンテンツの場所を保持する場合、コンテンツは保管担当者を解放するか、特定のデータの場所を削除するか、保留ポリシー全体を削除するまで保持されます。

## <a name="manage-custodian-based-holds"></a>保管担当者ベースの保持を管理する

場合によっては、特定して保持するように設定した一連のデータ保管担当者が存在することがあります。 上級電子情報開示では、これらの保管担当者が保留になっていると、ユーザーと選択されたデータソースが保管担当者保留ポリシーに自動的に追加されます。 

保管担当者ホールドポリシーを表示するには、次のようにします。

1. [**セキュリティ & コンプライアンスセンター**] で、[**電子情報開示 > Advanced ediscovery** ] をクリックして、組織内のケースの一覧を表示します。
   
2. ケース内に保管担当者を追加するには、[**保管担当者**] タブに移動します。 高度な電子情報開示ケース内に保管担当者を追加して保存する方法については、「 [Add 保管担当者 to a Advanced Ediscovery case」を](add-custodians-to-case.md)参照してください。 保管担当者を既に追加していて、保留リストに配置している場合は、手順3に進みます。
   
3. [**保留**] タブに移動し、[保管担当者 Policy] を選択します。
   
4. フライアウトページには、ポリシーの [ホールド] の統計が表示されます。 また、保管担当者ベースのホールドにクエリを適用するなどの操作を実行することもできます。 保留クエリの作成と条件の使用の詳細については、「[コンテンツ検索のキーワードクエリと検索条件](keyword-queries-and-search-conditions.md)」を参照してください。
 
## <a name="manage-non-custodial-holds"></a>非 wi-fi ダイヤルの保持を管理する

保留リストを作成するときに、指定されたコンテンツの場所に保持されているコンテンツの範囲を指定する場合は、次のオプションがあります。

  - すべてのコンテンツが保留にされている場合、無限の保留リストを作成します。また、検索クエリに一致したコンテンツのみが保留にされている場合、クエリ ベースの保留リストも作成できます。
  - 日付の範囲を指定して、その日付の範囲内に送信、受信、または作成したコンテンツのみを保留にすることができます。また、コンテンツがいつ送信、受信、作成されたかにかかわらず、すべてのコンテンツを保留にすることもできます。

高度な電子情報開示ケースの保留リストを作成するには、次のようにします。

1. [**セキュリティ & コンプライアンスセンター**] で、[**電子情報開示 > Advanced ediscovery** ] をクリックして、組織内のケースの一覧を表示します。
  
2. 保留リストを作成するケースの横の [**開く**] をクリックします。
  
3. 大文字と小文字のホームページから、[**保留**] タブをクリックします。
  
4. [**保留**] タブで、[**作成**] をクリックします。
  
5. [**保留リストに名前**を付ける] ページで、ホールドに名前を付けます。 ホールドの名前は組織内で一意である必要があります。
 
6. (省略可能) [**説明 **] ボックスで、保留リストの説明を追加します。
  
7. [**次へ**] をクリックします。
  
8. 保留にするコンテンツの場所を選択します。メールボックス、サイト、パブリック フォルダーを保留にできます。

   a. **Exchange 電子メール**-[**ユーザー、グループ、またはチームの選択**] をクリックし、[**ユーザー、グループ、または teams**を再度選択する] をもう一度クリックして、保持するメールボックスを指定します。 検索ボックスを使用して、ユーザーのメールボックスと配布グループを検索します (グループメンバーのメールボックスを保留にする場合)。 また、Office 365 グループまたは Microsoft チームに対して、関連付けられたメールボックスにホールドを配置することもできます。 [ユーザー、グループ、チーム] チェックボックスをオンにし、[**選択**] をクリックし、[**完了**] をクリックします。
 
    > [!NOTE]
    > [**ユーザー、グループ、またはチームの選択**] をクリックして保留にするメールボックスを指定するときに、表示されるメールボックス ピッカーは空の状態です。これは、パフォーマンスを向上させるための仕様です。このリストにユーザーを追加するには、検索ボックスに名前 (3 文字以上) を入力します。

    b. **SharePoint サイト** - [**サイトの選択**] をクリックし、もう一度 [**サイトの選択**] をクリックして保留にする SharePoint および OneDrive for Business サイトを指定します。保留にする各サイトの URL を入力します。Office 365 グループまたは Microsoft チーム用の SharePoint サイトの URL を追加することもできます。[**選択**]、[**完了**] の順にクリックします。
    
     Office 365 グループと Microsoft Teams を保持する方法に関するヒントについては、 **FAQ**セクションを参照してください。

    > [!NOTE]
    > ユーザープリンシパル名 (UPN) が変更された場合、そのユーザーの OneDrive アカウントの URL も新しい UPN を組み込むように変更されます。 このような場合は、ユーザーの新しい OneDrive URL を追加して古いバージョンを削除することによって、保留リストを変更する必要があります。

     c. **Exchange パブリックフォルダー** -切り替えスイッチをすべての位置に移動して、Exchange Online 組織内のすべてのパブリックフォルダーを保持します。 特定のパブリックフォルダーを保持の対象にすることはできないことに注意してください。 パブリックフォルダーを保持しない場合は、トグルスイッチを **[なし**] のままにします。

9. 保留リストにコンテンツの場所を追加し終わったら、[**次へ**] をクリックします。
  
10. 条件を使用してクエリベースの保持を作成するには、次の手順を実行します。 それ以外の場合は、[**次へ**] をクリックします。
    
    - 検索条件に一致するコンテンツのみが保持されるようにするには、[**キーワード**] の下のボックスに検索クエリを入力します。 ファイル名などの、キーワード、メッセージプロパティ、またはドキュメントプロパティを指定できます。 ブール演算子 (AND、OR、NOT など) を使用するより複雑なクエリを使用することもできます。 [キーワード] ボックスを空白のままにすると、指定したコンテンツの場所にあるすべてのコンテンツが保持されます。

    - [条件の**追加**] をクリックして、1つまたは複数の条件を追加して、保留リストの検索クエリを絞り込みます。 各条件は、保留を作成するときに作成および実行される KQL 検索クエリに句を追加します。 たとえば、日付範囲を指定して、指定した期間内に作成された電子メールまたはサイトのドキュメントが保留リストに配置されるようにすることができます。 条件は、AND 演算子によって (キーワード ボックスで指定された) キーワード クエリに論理的に結合されます。 これは、アイテムがキーワードクエリと条件の両方に一致する必要があることを意味します。

     検索クエリの作成と条件の使用の詳細については、「[コンテンツ検索のキーワード クエリと検索条件](https://docs.microsoft.com/en-us/office365/SecurityCompliance/keyword-queries-and-search-conditions)」を参照してください。

12. クエリ ベースの保留リストを構成した後、[**次へ**] をクリックします。
 
13. 設定を確認し、[**この保留リストを作成**] をクリックします。


## <a name="view-hold-statistics"></a>保留の統計を表示する

しばらくすると、選択した保留リストの [**保留**] タブの [詳細] ウィンドウに、新しい保留リストに関する情報が表示されます。 この情報には、保留になっているアイテムの合計数とサイズ、保持統計情報が最後に計算されたときなど、保留中のコンテンツに関するメールボックスとサイトの数および統計情報が含まれます。 これらの保持統計情報は、電子情報開示ケースに関連するコンテンツの量を特定するのに役立ちます。

保留アイテムの統計情報については、次の点に注意してください。

- 保留にされているアイテムの合計数は、すべてのコンテンツ ソースのうち、保留にされているアイテム数を示します。クエリベースの保留リストを作成した場合、この統計情報は、クエリに一致するアイテム数を示します。
  
- 保留にされているアイテム数には、コンテンツの場所で見つかった、インデックスのないアイテムも含まれます。クエリベースの保留リストを作成した場合、コンテンツの場所にあるインデックスのないすべてのアイテムは保留にされます。これには、クエリベースの保留リストの検索条件と一致しないインデックスのないアイテムと、日付範囲の条件から外れる可能性のあるインデックスのないアイテムが含まれます。これは、コンテンツ検索を実行したときの結果とは異なります。コンテンツ検索の場合、検索クエリと一致しないインデックスのないアイテム、または日付範囲の条件によって除外されるアイテムは、検索結果に含まれません。インデックスのないアイテムの詳細については、「[Office 365 のコンテンツ検索で部分的にインデックスが作成されたアイテム](partially-indexed-items-in-content-search.md)」を参照してください。 

- 最新の保持統計情報を取得するには、[統計情報の更新] をクリックして、保留中の現在のアイテム数を計算する検索推定を再度実行します。

- 必要に応じて、ツールバーの [更新] をクリックして、[詳細] ウィンドウで保持の統計情報を更新します。

- 通常、保留にされているアイテム数は時間と共に増えます。これは、メッセージ ボックスまたはサイトが保留にされているユーザーは、一般的に新しいメール メッセージを送受信し、新しい SharePoint および OneDrive for Business ドキュメントを作成するためです。

- SharePoint サイトまたは OneDrive アカウントが複数地域環境内の別の領域に移動された場合、そのサイトの統計情報は保留アイテムの統計情報には含まれません。ただし、サイト内のコンテンツは引き続き保留にされます。また、サイトが別の領域に移動された場合、保留リストに表示される URL は更新されません。保留リストを編集し、URL を更新する必要があります。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

- **追加の Office 365 グループまたは Microsoft Teams サイトを保管担当者にマップするにはどうすればよいですか。Office 365 グループおよび Microsoft Teams には、非 wi-fi ダイヤルを含めることができます。** Microsoft Teams は、Office 365 グループ上に構築されています。 そのため、電子情報開示ケースでそれらを保持することは非常によく似ています。 Office 365 グループと Microsoft Teams を保持する場合は、次の点に注意してください。
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
    > Get-UnifiedGroup コマンドレットを実行するには、Exchange Online で View-Only Recipients という役割が割り当てられているか、View-Only Recipients という役割が割り当てられている役割グループに属している必要があります。

 - ユーザーのメールボックスを検索すると、そのユーザーがメンバーになっているすべての Office 365 グループまたは Microsoft チームは検索されません。 同様に、Office 365 グループまたは Microsoft teams ホールドを配置すると、グループメールボックスとグループサイトのみが保持されます。グループメンバーのメールボックスと OneDrive for Business サイトは、保管担当者として明示的に追加したり、データソースを保持したりしない限り、保留リストには置かれません。 そのため、特定の保管担当者に対して Office 365 グループまたは Microsoft teams を保持する必要がある場合は、グループメールボックスとグループメールボックスを保管担当者にマッピングすることを検討してください (「Advanced eDiscovery での保管担当者の管理」を参照してください)。 Office 365 グループまたは Microsoft teams が1つの保管担当者に属さない場合は、そのソースを非 custodial ホールドに追加することを検討してください。 
 
 - Office 365 グループまたは Microsoft teams のメンバーの一覧を取得するには、Microsoft 365 管理センターの [ホーム > グループ] ページでプロパティを表示します。 または、Exchange Online PowerShell で次のコマンドを実行することもできます。

   ``` 
   Get-UnifiedGroupLinks <group or team name> -LinkType Members | FL DisplayName,PrimarySmtpAddress
   ```

    > [!NOTE]
    > **Get-UnifiedGroupLinks** コマンドレットを実行するには、Exchange Online で View-Only Recipients という役割が割り当てられているか、View-Only Recipients という役割が割り当てられている役割グループに属している必要があります。

- Microsoft Teams チャネルの一部であるチャネル会話は、チームに関連付けられているメールボックスに格納されます。 同様に、チームメンバーがチャネルで共有するファイルは、チームの SharePoint サイトに格納されます。 そのため、チャネル内の会話やファイルを保持するには、Microsoft teams メールボックスと SharePoint サイトを保留にする必要があります。
  
- または、Microsoft Teams のチャットリストに含まれる会話が、チャットに参加しているユーザーのメールボックスに保存されます。  ユーザーがチャット会話で共有しているファイルは、そのファイルを共有しているユーザーの OneDrive for Business サイトに保存されます。 そのため、会話やファイルをチャットリストに保持するには、個々のユーザーメールボックスと OneDrive for Business サイトを保持する必要があります。 
  
- 各 Microsoft チームまたはチーム チャネルには、メモと共同作業用の Wiki が含まれています。Wiki コンテンツは、.mht 形式のファイルに自動的に保存されます。このファイルは、チームの SharePoint サイトの Teams Wiki データ ドキュメント ライブラリに保存されます。Wiki のコンテンツを保留にするには、チームの SharePoint サイトを保留にします。

  > [!NOTE]
  > (チームの SharePoint サイトを保留にするときに) Microsoft チームまたはチーム チャネルの Wiki コンテンツを保持する機能は、2017 年 6 月 22 日にリリースされました。チーム サイトが保留にされると、この日から Wiki コンテンツが保持されます。ただし、チーム サイトが保留にされ、Wiki コンテンツが 2017 年 6 月 22 日よりも前に削除された場合、その Wiki コンテンツは保持されていません。