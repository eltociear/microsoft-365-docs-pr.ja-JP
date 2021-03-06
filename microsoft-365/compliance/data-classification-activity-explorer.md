---
title: アクティビティ エクスプローラーの使用を開始する (プレビュー)
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: アクティビティ エクスプローラーでは、ラベル付きコンテンツを取り扱うユーザーの操作の確認およびフィルター処理を行い、データ分類機能の機能性を完全なものにします。
ms.openlocfilehash: 68304bc75d33c993db52895828ec49e3b5203a4c
ms.sourcegitcommit: 3b2fdf159d7dd962493a3838e3cf0cf429ee2bf2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "42929461"
---
# <a name="get-started-with-activity-explorer-preview"></a>アクティビティ エクスプローラーの使用を開始する (プレビュー)

データ分類の概要およびコンテンツ エクスプローラーのタブにより、どのコンテンツが検出されてラベルが付けられているか、およびそのコンテンツのある場所に対する可視性が与えられます。 アクティビティ エクスプローラーでは、ラベル付きコンテンツに対して実行される内容を監視できるようにすることで、こうした一連の機能性を完全なものにします。 アクティビティ エクスプローラーでは、履歴ビューを提供します。

![アクティビティ エクスプローラーのプレースホルダー スクリーンショットの全体像](../media/data-classification-activity-explorer-1.png)

次を使用し、データをフィルター処理します。

- 日付の範囲
- アクティビティの種類
- 場所
- ユーザー
- 機密ラベル
- 保持ラベル


リストまたは棒グラフとしてデータを表示することができます。

## <a name="prerequisites"></a>前提条件

アクティビティ エクスプローラーにアクセスして使用するすべてのアカウントには、これらのいずれかのサブスクリプションのライセンスが割り当てられている必要があります。

- Microsoft 365 (E5)
- Office 365 (E5)
- 高度なコンプライアンス (E5) アドオン
- 高度な脅威インテリジェンス (E5) アドオン

## <a name="activity-type"></a>アクティビティの種類

Microsoft 365 では、SharePoint Online、OneDrive およびエンドポイントを横断して 12 種類のアクティビティを監視したり、レポートしたりします。 エンドポイントとは、Windows 10 を実行しているユーザー デバイスです。

- ファイルが作成されました
- ファイルが変更されました
- ファイルの名前が変更されました
- ファイルがクラウドにコピーされました
- ファイルが許可されていないアプリによってアクセスされました
- ファイルが印刷されました
- ファイルがリムーバブル メディアにコピーされました
- ファイルがネットワーク共有にコピーされました
- ファイルの読み取り
- ファイルがクリップボードにコピーされました
- ラベルが適用されました
- ラベルが変更されました (アップグレード、ダウングレード、または削除されました)

機密ラベル付きのコンテンツに対してどんな操作が行われたかを理解する価値は、[データ損失防止ポリシー](data-loss-prevention-policies.md) が有効かどうかなど、既定の環境の制限を確認できることです。 そうでない場合、つまり、多数の `highly confidential` でラベル付けされたアイテムおよび `general` にダウングレードされたアイテムなどの予想しない何かが検出された場合は、各種ポリシーを管理して、望ましくない動作を制限するための新しい操作を行うことができます。

フィルターを設定すると、次のことが実行できます。

- 横棒グラフのセグメントにマウス ポインターを置き、そのカテゴリに分類されたアイテムの数を確認できます ![アクティビティ エクスプローラーのマウスでのポイント](../media/data-classification-activity-explorer-hover-over-2.png)
- データをエクスポートする
- リストから任意のアイテムを選択して、フライ アウトに操作の詳細を表示します。

![アクティビティ エクスプローラーの詳細のフライ アウト](../media/data-classification-activity-explorer-fly-out-3.png)

## <a name="see-also"></a>関連項目
- [機密ラベル](sensitivity-labels.md)
- [保持ラベル](labels.md)
- [機密情報の種類の検索基準](what-the-sensitive-information-types-look-for.md)
- [アイテム保持ポリシーの概要](retention-policies.md)
