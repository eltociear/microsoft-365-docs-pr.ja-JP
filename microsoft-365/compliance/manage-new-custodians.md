---
title: 高度な電子情報開示ケースで保管担当者を管理する
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
ms.openlocfilehash: 17c77f14267f988a071e201733ae54ad9c438547
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2019
ms.locfileid: "37085991"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-case"></a>高度な電子情報開示ケースで保管担当者を管理する

Advanced eDiscovery の [保管担当者] タブには、ケースに追加されているすべての保管担当者の一覧が含まれています。 保管担当者をケースに追加すると、各保管担当者の詳細が Azure Active Directory から自動的に収集され、高度な電子情報開示で表示できるようになります。

![保管担当者の管理](media/CustodianDetails.PNG)

## <a name="view-custodian-details"></a>保管担当者の詳細を表示する

保管担当者の詳細を表示するには、[**保管担当者**] タブのリストで保管担当者をクリックします。ポップアップページが表示され、保管担当者に関する次の情報が含まれています。

- 連絡先情報

  - [**表示名**保管担当者のアドレス帳に表示される名前。 通常は、保管担当者の名、ミドルネーム、姓の組み合わせになります。
  
   - **Mail/SMTP** -保管担当者のプライマリ SMTP アドレス (例: brianj@contoso.onmicrosoft.com)。 保管担当者のユーザープリンシパル名 (UPN) もリストされていることに注意してください。

  - **Title** -保管担当者の役職。

  - **Department** -保管担当者が機能する部署の名前。

  - **上司**-保管担当者の上司。 指定した上司は、この保管担当者のエスカレーション情報を受け取ります。
  
- 場所情報

  - **City** -保管担当者が配置されている市区町村。

  - **State** -保管担当者の住所の都道府県を示します。

  - **国/地域**-保管担当者が配置されている国/地域。

  - **Office** -保管担当者の事業所のオフィスの場所。

- ケース情報

  - **ホールド状態**-保管担当者が保留中であるかどうかを示します。 

  - **通信の状態**: 保管担当者に保留通知が発行されているかどうかを示します。 保管担当者に通知が発行されている場合は、このプロパティの値が**公開**されます。 保管担当者に通知が発行されていない場合、状態**は未発行になります。** 

  - **状態**-ケース内の保管担当者の状態。 状態が "**アクティブ**" は、保管担当者がケースの一部であることを示します。 保管担当者がケースからリリースされている場合は、ステータスが [**リリース**済み] に変更されます。 

- データソースとインデックス作成に関する情報

    - **データソース**-保管担当者に関連付けられていて、ケースの一部であるデータソース (メールボックス、サイト、およびチーム) の数と種類が表示されます。

    - **インデックスの更新時刻**-高度なインデックス作成ジョブが最後にトリガーされた日時を示します。 このプロパティは、高度なインデックス処理が現在進行中であることも示します。


## <a name="edit-a-custodian"></a>保管担当者を編集する

ケースの進行状況に応じて、特定の保管担当者に関連する追加のデータソースが存在する可能性があることがわかっている場合があり &。 その他のシナリオでは、確認され、関連性がないと見なされた特定のデータソースを削除することが必要な場合があります。

保管担当者に関連付けられているデータソースを更新するには、次のようにします。

1. **電子情報開示 > Advanced ediscovery**に移動し、ケースを開きます。
  
2. [**保管担当者**] タブをクリックします。
  
3. リストから保管担当者を選択し、フライアウトページの [**編集**] をクリックします。

    ![データソースの編集](media/EditCustodianDataSource.PNG)
  
4. [**データソースの選択**] タブをクリックして、保管担当者の Exchange メールボックスと OneDrive アカウントの設定を変更し、[**データソースの選択**] をクリックします。
  
5. 保管担当者に関連付けられている Teams、SharePoint、または Exchange メールボックスを追加または削除するには、[**その他のデータソースの選択**] タブをクリックします。 

    保管担当者に関連付けられているデータソースの詳細については、「 [Add 保管担当者 to case](add-custodians-to-case.md#step-3-associate-additional-data-sources-to-a-custodian)」の「手順 3: 追加のデータソースを保管担当者に関連付ける」を参照してください。 
  
6. 保管担当者のホールドを有効または無効にするには、[ **custodial ホールドを配置**する] をクリックします。

## <a name="resolve-custodian-processing-errors"></a>保管担当者処理エラーを解決する

法的調査のためのほとんどの電子情報開示ワークフローでは、保管担当者が訴訟に追加された後、保管担当者のデータのサブセットが検索されます。 非常に大きなファイルサイズまたはデータの破損が原因で、保管担当者に関連付けられているデータソース内の一部のアイテムが部分的にインデックス処理されることがあります。 高度な電子情報開示の[高度なインデックス](indexing-custodian-data.md)機能を使用すると、ほとんどのインデックス付きアイテムは、必要に応じてこれらのアイテムのインデックスを再作成することで、自動的に修復できます。

保管担当者がケースに追加されると、保管担当者に関連付けられているデータソース内のデータは自動的に再インデックス化されます (高度なインデックス作成プロセスによって)。 つまり、データをダウンロードして修復してからオフラインで検索する代わりに、データをインプレースのままにしておくことができます。 ただし、訴訟のライフサイクルの間に、新しいデータソースが保管担当者に関連付けられる場合があります。 この場合は、高度なインデックス処理を再実行して、保管担当者のデータを再インデックス化して、部分的にインデックス付けされたアイテムを修復し、保管担当者のデータのインデックスを更新します。

部分的なインデックスが作成されたアイテムを処理するために、再インデックス処理をトリガーするには

1. **電子情報開示 > Advanced ediscovery**に移動し、ケースを開きます。

2. [**保管担当者] タブ**をクリックし、データが再インデックス化にする必要がある保管担当者を選択します。 

3. [フライアウト] ページで、[**インデックスの更新**] をクリックします。

   インデックスジョブが作成されたことを示すダイアログが表示されます。

保管担当者データの再インデックス作成は、長時間実行されるプロセスです。作成された対応するジョブには、**保管担当者データの再インデックス**という名前が付けられます。 [**ジョブ**] タブまたは [**保管担当者**] タブで進行状況を追跡するには、[**インデックス作成ジョブの状態**] 列の状態を監視します。

詳細については、次のトピックを参照してください。

- [処理中のエラーの操作](processing-data-for-case.md)

- [ジョブを管理する](managing-jobs-ediscovery20.md)

## <a name="release-a-custodian-from-a-case"></a>ケースからの保管担当者のリリース

保管担当者がリリースされるのは、ケースがクローズされた場合、保管担当者がケースのコンテンツを保持する義務がなくなった場合、または保管担当者がケースに関連していないと判断された場合です。 

保留通知が公開された後に保管担当者をリリースした場合は、リリース通知が保管担当者に送信されます。 さらに、保管担当者に関連付けられたデータソースに配置されたすべての保留リストが削除されます。 保管担当者が、法的情報保留通知を発行していない*サイレントホールド*に配置されていた場合、リリース通知は送信されませんが、その保管担当者に関連付けられていたデータソースに配置された保留リストは削除されます。

保管担当者をリリースするには、次のようにします。 

1. **電子情報開示 > Advanced ediscovery**に移動し、ケースを開きます。

2.  [**保管担当者**] タブに移動します。

3.  [**保管担当者] タブ**をクリックし、ケースからリリースされる保管担当者を選択します。

4. [フライアウト] ページで、[ **Release 保管担当者**] をクリックします。

   保管担当者に関連付けられたデータソースにホールドが設定されている場合、保留が解除され、別の高度な電子情報開示ケースに関連付けられている他のすべての保留が引き続き適用されることを説明する警告ページが表示されます。 Office 365 (Office 365 アイテム保持ポリシーなど) の他の種類の保持および保持機能が含まれています。

5. [**はい**] をクリックして、保管担当者を解放することを確認します。 

    [**保管担当者**] タブでこのユーザーの状態が [**リリース**済み] に設定されていて、フライアウトページの**ホールド状態**が**False**に変更されることに注意してください。 

> [!NOTE]
> 保管担当者は、いくつかの法的なケースに同時に関与する場合があります。 保管担当者がケースからリリースされた場合、他の事柄の保留と通知は影響を受けません。

## <a name="bulk-edit-custodians"></a>一括編集保管担当者

一括エディターを使用して、同時に複数の保管担当者を編集できます。 これを行うには、[**保管担当者**] タブで2つ以上の保管担当者を選択して一括エディターを表示し、タスクの1つをクリックします。

![複数の保管担当者の設定を編集するためのフライアウトページ](media/AeDBulkEditCustodians.png)