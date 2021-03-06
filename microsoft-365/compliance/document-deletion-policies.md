---
title: ドキュメント削除ポリシーの概要
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 55e8d858-f278-482b-a198-2e62d6a2e6e5
description: 組織では、コンプライアンス、法律、またはその他のビジネス要件のために長期間ドキュメントを保持する必要がある場合があります。 ただし、組織でドキュメントを必要以上に長期に保持している場合は、不要な法的リスクを作成します。 ドキュメント削除ポリシーを使用すると、特定の期間が経過した後にサイト内のドキュメントを削除することによって、積極的にリスクを軽減できます。たとえば、ドキュメントが作成された後に、ユーザーの OneDrive for Business サイトのドキュメントを5年後に削除することができます。
ms.openlocfilehash: fba7af2c58b373e51aed93ce9a353a45528bb9f9
ms.sourcegitcommit: 60c1932dcca249355ef7134df0ceb0e57757dc81
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2020
ms.locfileid: "43943000"
---
# <a name="overview-of-document-deletion-policies"></a>ドキュメント削除ポリシーの概要

> [!IMPORTANT]
> 今後は、ドキュメント削除ポリシーの代わりに、Microsoft 365 コンプライアンスセンター、Microsoft 365 セキュリティセンター、またはセキュリティ&amp; /コンプライアンスセンターで作成されたアイテム保持ポリシーまたはラベルを使用することをお勧めします。 ドキュメント削除ポリシーは、保持ポリシーを使用して引き続き並行して機能しますが、Office 365 でコンテンツを保持または削除する必要がある場合は、アイテム保持ポリシーを使用することをお勧めします。 詳細については、「[これらの機能の代わりにアイテム保持ポリシーを使用](retention-policies.md#use-a-retention-policy-instead-of-these-features)する」を参照してください。
  
組織では、コンプライアンス、法律、またはその他のビジネス要件のために長期間ドキュメントを保持する必要がある場合があります。 ただし、組織でドキュメントを必要以上に長期に保持している場合は、不要な法的リスクを作成します。 ドキュメント削除ポリシーを使用すると、特定の期間が経過した後にサイト内のドキュメントを削除することによって、積極的にリスクを軽減できます。たとえば、ドキュメントが作成された後に、ユーザーの OneDrive for Business サイトのドキュメントを5年後に削除することができます。
  
ドキュメント削除ポリシーは、次のような強力な柔軟性を備えています。
  
- サイトの所有者が、一元的に作成および管理するポリシーから選択できるようにします。 また、ポリシーがコンテンツに適用されないことを決定した場合に、サイトの所有者に対して完全な脱退を許可することもできます。
    
- サイトコレクション内のすべてのサイト (すべての OneDrive for Business サイトなど) に対して1つの必須ポリシーを適用するか、またはチームサイトテンプレートなど、特定のサイトコレクションテンプレートから作成されたすべてのサイトコレクションに対してポリシーを強制することもできます。
    
- サイトの所有者に必要な操作を行わずに、自動的に適用される既定のルールを既定のポリシーとして指定します。
    
- サイト所有者が選択できるいくつかの削除ルールを含むポリシーを作成します。
    
ドキュメント削除ポリシーセンターを使用して、ドキュメント削除ポリシーを作成および管理します。 または、[サイトコレクションを作成](https://go.microsoft.com/fwlink/p/?LinkID=404342)し、[**エンタープライズ**] タブの [**コンプライアンスポリシーセンター** ] を選択して、ポリシーセンターを手動で作成することもできます。各テナントには、ドキュメント削除ポリシーセンターを1つだけ含めることができます。 
  
![ドキュメント削除ポリシー センターのホーム ページ](../media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="when-to-use-document-deletion-policies"></a>ドキュメント削除ポリシーを使用する場合

Microsoft では、ドキュメント削除ポリシーに加えて、サイトコンテンツに対して次のアイテム保持ポリシーを提供しています。
  
- [レコード管理](https://go.microsoft.com/fwlink/p/?LinkID=404250)
    
- [コンテンツタイプ、リスト、およびライブラリの情報管理ポリシー](https://go.microsoft.com/fwlink/p/?LinkID=404239)
    
- [サイト ポリシー](https://go.microsoft.com/fwlink/p/?LinkID=404242)
    
各種類のポリシーは、特定の種類のサイトまたはデータに最適に機能します。 たとえば、組織には、契約のための財務サイトや記事のサポート技術情報など、コンテンツタイプを使用する高度な構造化サイトがあります。 この場合は、コンテンツタイプのポリシーを使用できます。 または、組織で法的ドキュメントを保持する必要がある場合があります。その場合は、コンテンツタイプとレコードセンターを使用してファイルプランを実装することができます。
  
ドキュメント削除ポリシーは、構造化データとコンテンツタイプに最適に機能するレコード管理ポリシーまたは情報管理ポリシーを置き換えません。 OneDrive for Business サイトやチームサイトなどの非構造化データの自動削除を幅広く管理する必要がある場合は、ドキュメント削除ポリシーを使用する必要があります。
  
![サイト コンテンツの保持オプションを示す図](../media/IP-Retention-policies-for-site-content.png)
  
リストまたはライブラリ用に既にコンテンツ タイプ ポリシーまたは情報管理ポリシーを使用しているサイトにドキュメント削除ポリシーを適用した場合、前者のポリシーは無視され、ドキュメント削除ポリシーが有効になります。 つまり、構造化または非構造化コンテンツ (両方ではない) に対して指定されたポリシーのみを使用するようにサイトを計画する必要があります。 ドキュメント削除ポリシーが他のポリシーを上書きする方法の詳細については、「[サイトのドキュメント削除ポリシーを適用または削除する](apply-or-remove-a-document-deletion-policy-for-a-site.md)」を参照してください。
  
他のポリシーとは異なり、ドキュメント削除ポリシーは、リストではなく、ドキュメントライブラリでのみ機能します。
  
## <a name="deletion-policies-and-rules"></a>削除ポリシーとルール

ドキュメント削除ポリシーには、以下を指定する1つまたは複数の削除ルールが含まれています。
  
- 削除されるまでの期間です。
    
- ドキュメントの作成日または最終更新日時から削除日を計算するかどうかを指定します。
    
- ドキュメントを完全に削除するか、ゴミ箱に削除するかを指定します。
    
ポリシーに複数のルールが含まれている場合、サイト所有者は、そのコンテンツに最も適したルールを選択できます。
  
![新しい削除ルール ページ](../media/IP-New-deletion-rule.png)
  
## <a name="policies-and-assignments"></a>ポリシーと割り当て

ドキュメント削除ポリシーを作成したら、それをサイトコレクションテンプレートに割り当てることができます。たとえば、ポリシーを OneDrive for Business テンプレートに割り当てることによって、すべてのユーザーの OneDrive サイトが含まれるようにすることができます。 ポリシーをサイトコレクションテンプレートに割り当てると、そのテンプレートから作成されたすべてのサイトコレクションに加えて、そのテンプレートから作成されたすべてのサイトコレクションにも適用されます。
  
![OneDrive オプションを表示するテンプレート ページの選択](../media/IP-Choose-a-template.png)
  
ポリシーを特定のサイトコレクションに割り当てることもできます。これにより、そのサイトコレクションテンプレートに割り当てられているすべてのポリシーが上書きされます。 たとえば、ポリシーをチームサイトテンプレートに割り当てることができますが、そのテンプレートから作成された特定のサイトコレクションに対して、異なる一連のポリシーを適用することによって上書きします。
  
### <a name="one-mandatory-policy-or-several-policies-to-choose-from"></a>1つの必須ポリシーまたは複数のポリシーから選択する

ポリシーを割り当てるときに、ポリシーを必須にするように選択して、このポリシーを割り当てることができ、サイトコレクション内のすべてのサイトに適用されるようにすることができます。 サイト所有者は必須ポリシーから除外することはできません。つまり、サイト内のドキュメントは、何に関係なく削除ポリシーの対象になります。
  
1つのポリシーを必須にする代わりに、複数のポリシーをサイトコレクションに割り当てることもできます。これにより、各サイト所有者が自分のサイトに適用するポリシーを選択できるようになります。または、完全にオプトアウトすることもできます。 たとえば、一般的なビジネスドキュメント用に1つのポリシーを作成し、別の保持スケジュールが設定されている財務ドキュメントに対して別のポリシーを作成できます。 サイトの所有者は、サイトに含まれるコンテンツと、適用するドキュメント削除ポリシーをよく知っている場合があります。 各サイトに適用できるポリシーは1つだけです。
  
### <a name="one-rule-or-several-rules-to-choose-from"></a>1つまたは複数のルールを選択する

さらに、各ポリシーには多くのルールを含めることができます。たとえば、一般的なビジネスドキュメントの削除ポリシーには、次の2つのルールがあります。
  
- 法的義務や継続的なビジネスニーズに基づいて保持を必要としないドキュメントは、作成から1年を超えて保持してはなりません。
    
- 複数年の間に必要なアクティブなビジネスの使用に必要なドキュメントは、作成から3年以上保持しないようにする必要があります。
    
サイトの所有者は、サイトに一般的なビジネスドキュメントが含まれていることを確認し、この削除ポリシーを選択してから、ポリシーから適切なルールを選択します。 ルールは、現在サイトに適用されているポリシー (どのポリシーからではない) からのみ選択でき、ルールはサイト内のすべてのドキュメントライブラリに適用されます。
  
## <a name="the-relationship-of-site-collections-policies-and-rules"></a>サイトコレクション、ポリシー、およびルールの関係

基本的な関係は次のとおりです。
  
サイトコレクションまたはサイトコレクションテンプレートには、1つまたは複数のポリシーを割り当てることができます。また、各ポリシーには1つ以上のルールを含めることができます。 ただし、サイトごとにアクティブなポリシーは1つだけであり、サイト内のライブラリに対していつでもアクティブな削除ルールは1つだけです。
  
![ポリシー間の関係を示す図](../media/IP-Two-policies-four-rules.png)
  
## <a name="document-deletion-policies-are-inherited"></a>ドキュメント削除ポリシーが継承される

アクセス許可、ナビゲーションなど、他の多くのサイト機能と同様に、ドキュメント削除ポリシーが継承されます。 サイト所有者は、サイトのドキュメント削除ポリシーを選択でき、すべてのサブサイトは親からポリシーを継承します。 サブサイトの所有者は、別のポリシーとルールの組み合わせを選択することによって継承を解除でき、継承が再度切断されるまで、そのポリシーはすべてのサブサイトに適用されます。
  
## <a name="assigning-document-deletion-policies-for-the-first-time"></a>初めてドキュメント削除ポリシーを割り当てる

ドキュメント削除ポリシーに指定された期間は、ポリシーが割り当てられた後の時間ではなく、ドキュメントが作成または変更されてからの経過時間を意味することを理解しておくことが重要です。 たとえば、作成された2年後にドキュメントを完全に削除するドキュメント削除ポリシーを作成し、そのポリシーを、複数のサイトコレクションを作成したサイトコレクションテンプレート (4 または5年前) に割り当てることができます。 この場合、既存のサイトコレクションには、削除ポリシーで指定された2年より前のバージョンよりも多くのドキュメントが含まれている可能性があります。これは、初めてドキュメント削除ポリシーを割り当てた後に、多くのコンテンツが削除されることを意味します。
  
ポリシーを初めて割り当てると、サイト内のすべてのドキュメントが評価され、条件を満たしている場合、ドキュメントは削除されます。 これは、ポリシーの割り当て以降に新しく作成されたドキュメントだけでなく、すべての既存のドキュメントに適用されます。 また、期間は、ポリシーが最初に割り当てられた時間ではなく、各ドキュメントの保存期間を対象としていることに注意してください。
  
そのため、最初にポリシーをサイトに割り当てる前に、既存のコンテンツの保存期間と、ポリシーが既存のコンテンツに与える影響について考慮する必要があります。 また、新しいポリシーを割り当てる前にサイト所有者に連絡して、考えられる影響を評価するための時間を提供することもできます。
  
## <a name="time-lag-for-propagating-policies"></a>ポリシーの伝達のタイムラグ

ポリシーをサイトコレクションに割り当てると、サイト所有者は [**サイトの設定**] ページの [**ドキュメント削除ポリシー** ] リンクを使用して、サイトで利用可能なポリシーを表示および適用します。 
  
サイトコレクションにポリシーが割り当てられていない場合、[**ドキュメント削除ポリシー**のリンクは表示されません。 また、リンクは、ポリシーがサイトに割り当てられた直後には表示されず、[**ドキュメント削除ポリシー** ] リンクが表示されるときにポリシーが割り当てられると、最大24時間かかることがあります。 
  
## <a name="permissions"></a>Permissions

ドキュメント削除ポリシーセンターを使用するコンプライアンスチームのメンバーは、ポリシーセンターとポリシーを適用するサイトコレクションの両方に対するアクセス許可を必要とします。 以下のことをお勧めします。
  
1. ドキュメント削除ポリシーセンターのすべてのユーザーを含むセキュリティグループを作成します。これは、コンプライアンスポリシー管理チームである可能性が高いと考えられます。 詳細については[、「メールが有効なセキュリティグループの管理](https://go.microsoft.com/fwlink/p/?LinkID=404345)」を参照してください。 
    
2. [ドキュメント削除ポリシーセンター] で、[サイトコレクションの所有者] のアクセス許可をセキュリティグループに割り当てます。 詳細については、「[サイトコレクション管理者のアクセス許可](https://go.microsoft.com/fwlink/p/?LinkID=404346)」を参照してください。 
    
3. ドキュメント削除ポリシーを割り当てる必要がある各サイトコレクションで、サイトコレクション所有者のアクセス許可をセキュリティグループに割り当てます。
    
## <a name="how-document-deletion-policies-work-with-hold-policies"></a>ドキュメント削除ポリシーで保持ポリシーを使用する方法

保持ポリシーでは、すべてのコンテンツが一定の期間保持されるようにします。また、ドキュメント削除ポリシーを使用すると、特定の期間が経過した後にすべてのコンテンツが削除されるようになります。
  
一定期間ドキュメントを保持する必要がある場合は、削除ポリシーと組み合わせて保持ポリシーを使用できます。 たとえば、変更後3年間、ドキュメントを保持した後、削除ポリシーを設定して、最終変更後3年間そのドキュメントを削除することができます。
  
削除ポリシーは、ホールドを上書きできないことに注意してください。 サイトが保留中で、ドキュメント削除ポリシーによってドキュメントが削除されると、ドキュメントが手動で削除された場合と同じように、ドキュメントが保持保持ライブラリに保持されます。
  
## <a name="see-also"></a>関連項目

[サイトのドキュメント削除ポリシーを適用または削除する](apply-or-remove-a-document-deletion-policy-for-a-site.md)

[ドキュメント削除ポリシーを作成する](create-a-document-deletion-policy.md)


