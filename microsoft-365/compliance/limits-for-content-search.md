---
title: セキュリティ & コンプライアンスセンターでのコンテンツ検索の制限
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 78fe3147-1979-4c41-83bb-aeccf244368d
description: '同時検索の最大数など、Office 365 のセキュリティ & コンプライアンスセンターのコンテンツ検索機能に適用される制限について説明します。 '
ms.openlocfilehash: 6933fcb2a7b54c3617b2c01d54fa50fa4955ead2
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2019
ms.locfileid: "37085020"
---
# <a name="limits-for-content-search-in-the-security--compliance-center"></a>セキュリティ & コンプライアンスセンターでのコンテンツ検索の制限

> [!NOTE]
> このトピックの制限は、Exchange Online のインプレース電子情報開示および SharePoint Online の電子情報開示センターの現在の制限とは異なります。 
  
セキュリティ & コンプライアンスセンターのコンテンツ検索機能には、さまざまな制限が適用されます。 これには、**コンテンツ検索**ページで実行される検索と、電子情報開示ケースに関連付けられている検索が含まれます。 これらの制限は、Office 365 組織に提供されるサービスの正常性と品質を維持するために役立ちます。 Exchange Online での検索用の電子メールメッセージのインデックス作成に関連する制限もあります。 コンテンツ検索またはメールのインデックス作成の制限を変更することはできませんが、コンテンツの検索を計画、実行、およびトラブルシューティングする際にこれらの制限を考慮することができるように注意する必要があります。 
  
## <a name="content-search-limits"></a>コンテンツ検索の制限

次の表に、セキュリティ & コンプライアンスセンターでの検索の制限を示します。
  
|**制限の説明**|**制限**|
|:-----|:-----|
|単一のコンテンツ検索で検索できるメールボックスまたはサイトの最大数  <br/> |無制限  <br/> |
|組織内で同時に実行できるコンテンツ検索の最大数。  <br/> |無制限  <br/> |
|一度に1人のユーザーが開始できるコンテンツ検索の最大数。 この制限は、ユーザーがセキュリティ & コンプライアンスセンター PowerShell で**new-compliancesearch \| **コマンドを使用して、複数の検索を開始しようとした場合に発生する可能性があることに注意してください。  <br/> |10   <br/> |
|コンテンツ検索の結果をプレビューしているときにプレビューページに表示される、ユーザーごとのメールボックスあたりのアイテムの最大数。  <br/> |100  <br/> |
|コンテンツ検索の結果をプレビューしているときにプレビューページに表示される、すべてのユーザーメールボックスに含まれるアイテムの最大数。 最新のアイテムが表示されます。  <br/> |1,000  <br/> |
|検索結果をプレビューできるユーザーのメールボックスの最大数。 検索クエリに一致するコンテンツを含むメールボックスが 1000 を超える場合は、最も多い検索結果を持つ上位 1000 メールボックスのみをプレビューできます。  <br/> |1,000  <br/> |
|コンテンツ検索の結果をプレビューしているときにプレビューページに表示される SharePoint および OneDrive for Business サイトで検出されたアイテムの最大数。 最新のアイテムが表示されます。  <br/> |200  <br/> |
|検索結果としてプレビューできるサイトの最大数 (SharePoint および OneDrive for business)。 検索クエリに一致するコンテンツを含むサイトの総数が200を超える場合は、最も検索結果が多い上位200サイトのみがプレビューで利用可能になります。  <br/> |200  <br/> |
|コンテンツ検索の結果をプレビューするときにプレビューページに表示される、パブリックフォルダーメールボックスあたりのアイテムの最大数。  <br/> |100  <br/> |
|コンテンツ検索の結果をプレビューするときにプレビューページに表示されるすべてのパブリックフォルダーメールボックスで検出されるアイテムの最大数。  <br/> |200  <br/> |
|検索結果としてプレビューできるパブリックメールボックスの最大数。 検索クエリに一致するコンテンツが含まれるパブリックフォルダーメールボックスが500より多い場合は、最も検索結果の上位500パブリックフォルダーメールボックスのみがプレビューで利用可能になります。  <br/> |500  <br/> |
|コンテンツ検索の検索クエリの最大文字数 (演算子と条件を含む)。  <br/><br/> **注:** この制限は、クエリが展開された後に有効になります。つまり、各キーワードに対してクエリが拡張されます。 たとえば、検索クエリに15個のキーワードと追加のパラメーターと条件がある場合、クエリは15回展開され、それぞれにクエリ内の他のパラメーターと条件が含まれます。 そのため、検索クエリの文字数が上限を下回っている場合でも、この制限を超える可能性がある拡張クエリです。  <br/> |**メールボックス:** 1万  <br/> **サイト:** すべてのサイトを検索する場合は4000、サイト<sup>1</sup>を検索する場合は2000 <br/> |
|プレフィックスワイルドカードを使用して検索クエリで完全に一致する語句を検索するとき、またはプレフィックスワイルドカードと**NEAR**または**onear**ブール演算子を使用するときに返されるバリエーションの最大数。  <br/> |1万<sup>2</sup> <br/> |
|プレフィックスワイルドカードの最小文字数。たとえば`time*` `one*`、、、、など`set*`です。  <br/> |1/3  <br/> |
|コンテンツ検索に含まれるメールボックスの最大数。このアクションを実行するには、「 **new-compliancesearchaction-purge** 」コマンドを使用して、"検索と削除" アクションを実行します。 削除アクションを実行しているコンテンツ検索に、この制限を超えるソースメールボックスがある場合、削除アクションは失敗します。 検索と削除の詳細については、「 [Office 365 組織の電子メールメッセージの検索と削除](search-for-and-delete-messages-in-your-organization.md)」を参照してください。  <br/> |50,000  <br/> |
   
> [!NOTE]
> <sup>1</sup> SharePoint および OneDrive for business の場所を検索すると、検索対象のサイトの url 内の文字がこの制限に対してカウントされます。 <br/> <sup>2</sup>語句以外のクエリ (二重引用符を使用しないキーワード値) の場合は、特別なプレフィックスインデックスを使用します。 これにより、文書内で単語が発生しても、文書内のどこにも存在しないことがわかります。 語句のクエリ (二重引用符で囲まれたキーワード値) を処理するには、ドキュメント内の位置を語句内の単語と比較する必要があります。 これは、語句のクエリにプレフィックスインデックスを使用できないことを意味します。 この場合は、プレフィックスが展開される可能性のあるすべての単語を含むクエリを内部で展開します。たとえば、 `"time*"`はに`"time OR timer OR times OR timex OR timeboxed OR …"`展開できます。 10,000 は、単語が拡張可能なバリエーションの最大数であり、クエリに一致するドキュメントの数ではありません。 語句以外の用語には、上限がありません。 
  
## <a name="indexing-limits-for-email-messages"></a>電子メールメッセージのインデックス作成の制限

次の表では、インデックスが設定されていないアイテム、またはコンテンツ検索の結果で、部分的にインデックスが付けられたアイテムとして電子メールメッセージが返される可能性があるインデックスの制限について説明します。
  
|**インデックス作成の制限**|**メモ**|**説明**|
|:-----|:-----|:-----|
|添付ファイルの最大サイズ (Excel ファイルを除く)  <br/> |150 MB  <br/> |インデックス作成のために解析する電子メール添付ファイルの最大サイズ。 この制限を超える添付ファイルは、インデックス作成のために解析されません。添付ファイル付きのメッセージは、部分的にインデックス付けされたものとしてマークされます。  <br/> <br/>**注:** 解析は、indexing service が添付ファイルからテキストを抽出し、句読点やスペースなどの不要な文字を削除して、テキストを (トークン化されたプロセスの) 単語に分割してインデックスに格納するプロセスです。           |
|Excel ファイルの最大サイズ  <br/> |4 MB  <br/> |インデックス作成のために解析される電子メールメッセージに添付された、またはサイトにある Excel ファイルの最大サイズ。 この制限を超える Excel ファイルは解析されず、ファイルまたは電子メールの添付ファイルを含むメッセージは、インデックスが設定されていないとマークされます。  <br/> |
|添付ファイルの最大数  <br/> |250  <br/> |インデックス作成のために解析される電子メールメッセージに添付されたファイルの最大数。 メッセージに250個を超える添付ファイルがある場合、最初の250添付ファイルは解析され、インデックスが作成され、メッセージは、解析されなかった追加の添付ファイルがあったため、部分的なインデックスとしてマークされます。  <br/> |
|添付ファイルの最大の深さ  <br/> |31  <br/> |解析される入れ子になった添付ファイルの最大数。 たとえば、電子メールメッセージに別のメッセージが添付されていて、添付されたメッセージに Word 文書が添付されている場合、Word 文書と添付されたメッセージにはインデックスが作成されます。 この動作は、最大30個の入れ子になった添付ファイルに対して続行されます。  <br/> |
|添付画像の最大数  <br/> |.0  <br/> |電子メールメッセージに添付された画像は、パーサーによってスキップされ、インデックス付けされません。  <br/> |
|アイテムの解析にかかる最大時間  <br/> |30 秒  <br/> |インデックス作成のためにアイテムを解析するのには、最大30秒かかります。 解析時間が30秒を超えると、アイテムは部分的にインデックス付けされたマークが付けられます。  <br/> |
|最大パーサー出力  <br/> |200 万文字  <br/> |パーサーからの、インデックスが作成されたテキストの最大出力量。 たとえば、パーサーが文書から800万文字を抽出した場合、最初の200万文字のみがインデックス作成されます。  <br/> |
|注釈トークンの最大数  <br/> |200万  <br/> |電子メールメッセージにインデックスが設定されている場合、各単語には、その単語のインデックスを作成する方法を指定する異なる処理命令で注釈が付けられます。 処理命令の各セットは、注釈トークンと呼ばれます。 Office 365 でサービスの品質を維持するために、電子メールメッセージに対して使用できる注釈トークンは200万個に制限されています。  <br/> |
|インデックスの最大本文サイズ  <br/> |6700万文字  <br/> |電子メールメッセージの本文とそのすべての添付ファイルの文字数の合計。 電子メールメッセージのインデックスが作成されると、メッセージ本文とすべての添付ファイル内のすべてのテキストが1つの文字列に連結されます。 この文字列のインデックスが作成される最大サイズは、6700万文字です。  <br/> |
|本文の一意のトークンの最大数  <br/> |100 万  <br/> |前述したように、トークンは、コンテンツからテキストを抽出し、句読点とスペースを削除して、インデックスに格納されている単語 (トークンと呼ばれます) に分割した結果です。 たとえば、語句`"cat, mouse, bird, dog, dog"`には5つのトークンが含まれています。 ただし、これらのうちの4つだけは一意のトークンです。 電子メールメッセージごとに100万一意のトークンの制限があります。これにより、ランダムなトークンを使用してもインデックスが大きくなりすぎないようにすることができます。  <br/> |
  
## <a name="more-information"></a>詳細情報

検索結果のエクスポートやコンテンツのインデックス作成など、コンテンツ検索のさまざまな側面に関連する追加の制限があります。 これらの制限については、以下のトピックを参照してください。
  
- [コンテンツ検索の結果をエクスポートする](export-search-results.md#export-limits)
    
- [Office 365 のコンテンツ検索で部分的にインデックスが作成されたアイテム](partially-indexed-items-in-content-search.md)
    
- [Office 365 の電子情報開示で部分的にインデックスが作成されたアイテムを調査する](investigating-partially-indexed-items-in-ediscovery.md)
    
- [SharePoint Online の検索制限](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f)
    
コンテンツ検索の詳細については、以下を参照してください。
  
- [Office 365 のコンテンツ検索](content-search.md)
    
- [コンテンツ検索のキーワード クエリと検索条件](keyword-queries-and-search-conditions.md)