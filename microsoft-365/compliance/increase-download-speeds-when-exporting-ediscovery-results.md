---
title: 電子情報開示検索結果をエクスポートするときにダウンロード速度を上げる
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: セキュリティ & コンプライアンスセンターと高度な電子情報開示の検索結果をダウンロードするときに、データのスループットを向上させるように Windows レジストリを構成する方法について説明します。
ms.openlocfilehash: a5e08f2fe7d8840cfe8f176080c90b8b40d16af6
ms.sourcegitcommit: 60c1932dcca249355ef7134df0ceb0e57757dc81
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2020
ms.locfileid: "43943356"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results"></a>電子情報開示検索結果をエクスポートするときにダウンロード速度を上げる

電子情報開示エクスポートツールを使用して、セキュリティ & コンプライアンスセンターのコンテンツ検索の結果をダウンロードするか、Advanced eDiscovery からデータをダウンロードすると、ツールによって、データをローカルコンピューターにダウンロードするための一定数の同時エクスポート操作が開始されます。 既定では、同時操作の数は、データのダウンロードに使用しているコンピューターのコア数の8倍に設定されます。 たとえば、デュアルコアコンピューター (1 つのチップ上に2台の中央処理装置があることを意味します) では、既定の同時エクスポート操作数は16です。 データ転送のスループットとダウンロード処理の速度を向上させるために、検索結果のダウンロードに使用するコンピューターで Windows レジストリ設定を構成することによって、同時操作の数を増やすことができます。 ダウンロードプロセスを高速化するには、24回の同時操作の設定から始めることをお勧めします。
  
低帯域幅ネットワーク経由で検索結果をダウンロードする場合は、この設定値を大きくすると、悪影響を及ぼす可能性があります。 または、高帯域幅ネットワーク (同時操作の最大数は 48) で、24を超える同時操作の設定値を増やすことができる場合もあります。 このレジストリ設定を構成した後で、環境に最適な同時操作数を見つけるために、この設定を変更する必要がある場合があります。
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a>レジストリ設定を作成してデータをエクスポートするときの同時操作数を変更する

セキュリティ & コンプライアンスセンターまたは Advanced eDiscovery からのデータから検索結果をダウンロードするために使用するコンピューターで、次の手順を実行します。
  
1. 電子情報開示エクスポートツールが開いている場合は、それを閉じます。 
    
2. ファイル名サフィックス .reg を使用して、次のテキストをウィンドウのレジストリファイルに保存します。たとえば、ConcurrentOperations のようにします。 
    
    ```text
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    前述のとおり、24回の同時操作から始めて、必要に応じてこの設定を変更することをお勧めします。
    
3. エクスプローラーで、前の手順で作成した .reg ファイルをクリックまたはダブルクリックします。
    
4. [ユーザーアクセス制御] ウィンドウで、[**はい**] をクリックしてレジストリエディターに変更を許可します。 
    
5. 続行するように求めるメッセージが表示されたら、[**はい**] をクリックします。
    
    レジストリエディターに、設定が正常にレジストリに追加されたことを示すメッセージが表示されます。
    
6. 手順 2-5 を繰り返して、 `DownloadConcurrency`レジストリの設定の値を変更できます。 
    
    > [!IMPORTANT]
    > `DownloadConcurrency`レジストリ設定を作成または変更した後は、必ず新しいエクスポートジョブを作成するか、またはダウンロードする検索結果またはデータに対して既存のエクスポートジョブを再起動します。 詳細については、「[詳細情報](#more-information)」を参照してください。 
  
## <a name="more-information"></a>詳細情報

- この手順で作成した .reg ファイルを初めて実行するときに、新しいレジストリキーが作成されます。 その後`DownloadConcurrency` 、.reg の編集ファイルを変更して再実行するたびに、レジストリ設定が編集されます。 
    
- 電子情報開示エクスポートツールは、 [Azure AzCopy ユーティリティ](https://go.microsoft.com/fwlink/?linkid=849949)を使用して、セキュリティ & コンプライアンスセンターまたは Advanced eDiscovery から検索データをダウンロードします。 レジストリ設定`DownloadConcurrency`の構成は、azcopy ユーティリティを実行するときに、 **/NC**パラメーターを使用するのと似ています。 そのため、の`"DownloadConcurrency=24"`レジストリ設定は、azcopy ユーティリティ`/NC:24`でパラメーター値を使用するのと同じ効果があります。 
    
- 現在進行中のエクスポートのダウンロードを停止してから再起動した場合 (検索結果を再度ダウンロードしようとした場合)、電子情報開示エクスポートツールは同じダウンロードを再開しようとします。 そのため、ダウンロードを開始し、停止した後、 `DownloadConcurrency`レジストリ設定を変更すると、再起動するとダウンロードが失敗することがあります ([エクスポートされた結果の**ダウンロード**] をクリックします)。 これは、エクスポートツールがレジストリ設定を変更したために有効でない設定を使用して、以前のダウンロードを再開しようとしたためです。
    
    そのため、 `DownloadConcurrency`レジストリの設定を変更した後は、セキュリティ & コンプライアンスセンターで、エクスポートジョブを ([**再起動**] をクリックして) 必ず開始してください。 その後、エクスポートされた結果をダウンロードできます。 検索結果とデータのエクスポートの詳細については、以下を参照してください。
    
  - [コンテンツ検索の結果をエクスポートする](export-search-results.md)
    
  - [高度な電子情報開示で結果をエクスポートする](export-results-in-advanced-ediscovery.md)
    
