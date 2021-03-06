---
title: サービス暗号化
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.date: 10/3/2019
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '概要: Microsoft Office 365 のデータ復元性について理解します。'
ms.openlocfilehash: 1c31c0d5524370fd417460fbacf3695df4fa0102
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43632242"
---
# <a name="service-encryption"></a>サービス暗号化

ボリュームレベルの暗号化に加えて、Exchange Online、Skype for Business、SharePoint Online、および OneDrive for business では、顧客データを暗号化するためにサービス暗号化も使用されます。 サービス暗号化では、2つの主要な管理オプションを使用できます。

- Microsoft は、すべての暗号化キーを管理します。 (現在、このオプションは SharePoint Online、OneDrive for Business、Skype for business で利用できます)。

- 組織がルートキーを提供します。 これらのキーは、Azure Key Vault を使用して管理します。 このオプションは、顧客キーと呼ばれます。 顧客キーは現在、Exchange Online、SharePoint Online、OneDrive for business、Skype for Business、および Teams ファイルで使用できます。 顧客キーを使用する場合、これらのキーは Microsoft が管理するキーを置き換えてデータを暗号化します。

サービス暗号化には複数の利点があります。 たとえば、顧客キーは次のようになります。

- 強力な暗号化保護の上に、権限の保護と管理の機能を提供します。

- マルチテナントのキー管理をマルチテナントサービスが提供できるようにする顧客キーオプションが含まれています。

- Windows オペレーティングシステム管理者と、オペレーティングシステムによって保存または処理される顧客データへのアクセスを分離します。

- は、暗号化に関するコンプライアンス要件を持つお客様の要求を満たす Microsoft 365 の能力を向上させます。

## <a name="customer-key"></a>カスタマー キー

Customer キーを使用すると、社内ハードウェアサービスモジュール (HSM) または Azure Key Vault (AKV) のどちらかを使用して、独自の暗号化キーを生成できます。 キーの生成方法に関係なく、Office 365 で使用される暗号化キーを制御および管理するのには、AKV を使用します。 AKV にキーを格納すると、メールボックスのデータまたはファイルを暗号化する keychains のルートとして使用できるようになります。

顧客キーのもう1つの利点は、Microsoft がデータを処理できるようにするためのコントロールです。 Microsoft を使用してサービスを終了したり、クラウドに格納されているデータの一部を削除したりするなど、Office 365 からのデータを削除する場合は、テクニカルコントロールとして顧客キーを使用することができます。 これにより、Microsoft を含むすべての人がデータにアクセスしたり、データを処理したりすることがなくなります。 顧客キーが追加されており、Microsoft の担当者によるデータへのアクセスを制御するために使用する、お客様のロックボックスを補完しています。

Exchange Online、Skype for Business、SharePoint Online、チームサイト、OneDrive for business などの Microsoft 365 用のカスタマーキーを設定する方法については、次の記事を参照してください。

- [顧客キーによるサービスの暗号化](customer-key-overview.md)

- [顧客キーを設定する](customer-key-set-up.md)

- [顧客キーを管理する](customer-key-manage.md)

- [顧客キーまたは可用性キーをロールまたは回転する](customer-key-availability-key-roll.md)

- [可用性キーについて理解する](customer-key-availability-key-understand.md)
 
