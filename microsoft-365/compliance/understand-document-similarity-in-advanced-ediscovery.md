---
title: 高度な電子情報開示でのドキュメントの類似性を理解する
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
titleSuffix: Office 365
ms.date: 09/14/2017
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: '「ドキュメントの類似性」の値を確認します。2つのファイルの resemblance の最小レベルは、詳細な電子情報開示で機能します。 '
ms.openlocfilehash: bfce2e3018c690fc0a25bcda8e2c03690a334dc4
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43633412"
---
# <a name="understand-document-similarity-in-advanced-ediscovery-classic"></a>Advanced eDiscovery でのドキュメントの類似性 (クラシック) について

> [!NOTE]
> Advanced eDiscovery を使用するには、Advanced Compliance アドオンがインストールされた Office 365 E3 サブスクリプション、または E5 サブスクリプションがお客様の組織で必要になります。このプランを利用しておらず、Advanced eDiscovery をお試しになりたい場合は、[Office 365 Enterprise E5 の試用版にサインアップ](https://go.microsoft.com/fwlink/p/?LinkID=698279)してください。 
  
詳細な電子情報開示では、ドキュメントの類似性は、2つのドキュメントがほぼ重複していると見なされるために必要な resemblance の最小レベルです。
  
> [!TIP]
> ほとんどのビジネスアプリケーションでは、類似性値 60%-75% を使用することをお勧めします。 非常に低品質な光学式文字認識 (OCR) 資料の場合は、類似性の値を低くして適用できます。 
  
> [!NOTE]
> 特定のケースに対して設定して実行した後、類似性の値を変更することはできません。 
  
同一の複製 (ND) セット内では、類似性のしきい値の下に resemblance レベルのドキュメントが存在することがあります。 文書を ND セットに参加させるには、その類似性を超えるレベルの resemblance で、ND セットに少なくとも1つのドキュメントが存在する必要があります。 
  
たとえば、類似性が80% に設定されている場合、document F1 はレベル85% のドキュメント F2 に似ていますが、ドキュメント F2 はドキュメント F3 のレベルが90% であると仮定します。 
  
ただし、document F1 は、しきい値を下回る70% のレベルで、document F3 のようになります。 しかし、この例では、ドキュメント F1、F2、および F3 はすべて、一方の ND セットに表示されます。 同様に、類似性値80% を使用すると、2つのセットが作成されている可能性があります。 設定-1 には、E1 および E2 というドキュメントが含まれています。 [設定] は、ドキュメント F1、F2、および F3 を含みます。 
  
Resemblance のレベルは次のように示されています。
  
![ドキュメントの類似性](../media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
別のドキュメント X1 が挿入されたと仮定します。 X1 と E3 の間の resemblance は87% です。 同様に、X1 と F1 の間の resemblance は92% です。 その結果として、すべての設定が1つの ND セットに結合されるようにします。
  
![ドキュメントの類似性](../media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> 1つの ND セットに2つのドキュメントが割り当てられている場合は、そのセットに追加のドキュメントが追加された場合でも、セットが結合された場合でも、同じ ND セットに残ります。 
  
設定が結合されると、新しい文書がセットに追加されたときにピボットドキュメントが変更されることがあります。 
  
## <a name="see-also"></a>関連項目

[Advanced eDiscovery (クラシック)](office-365-advanced-ediscovery.md)
  
[分析オプションの設定](set-analyze-options-in-advanced-ediscovery.md)
  
[無視するテキストの設定](set-ignore-text-in-advanced-ediscovery.md)
  
[[詳細設定の分析] の設定](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[分析結果の表示](view-analyze-results-in-advanced-ediscovery.md)

