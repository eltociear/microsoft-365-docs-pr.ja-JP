---
title: Advanced eDiscovery での AzCopy のトラブルシューティング
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: o365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f8b72112feea4af0a33ef3a0cc12005c8deea195
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43637517"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery"></a>Advanced eDiscovery での AzCopy のトラブルシューティング

Advanced eDiscovery でエラーを修復するために Microsoft 以外の365データまたはドキュメントを読み込む場合、ユーザーインターフェイスは、アップロードするファイルが保存されている場所と、ファイルがアップロードされる Azure ストレージの場所を含む、Azure AzCopy コマンドを提供します。 ドキュメントをアップロードするには、このコマンドをコピーして、ローカルコンピューターのコマンドプロンプトで実行します。  次のスクリーンショットは、AzCopy コマンドの例を示しています。

![Microsoft 以外の365ファイルのアップロード](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

通常、提供されるコマンドは、実行時に機能します。 ただし、表示されるコマンドが正常に実行されない場合もあります。 考えられるいくつかの理由を次に示します。

## <a name="the-supported-version-of-azcopy-isnt-installed-on-the-local-computer"></a>サポートされているバージョンの AzCopy がローカルコンピューターにインストールされていません

現時点では、Microsoft 以外の365データを Advanced eDiscovery で読み込むには、AzCopy v1.1 を使用する必要があります。 AzCopy v2.0 を使用していない場合、前のスクリーンショットに表示されている [**ファイルのアップロード**] ページに表示される azcopy コマンドはエラーを返します。 このバージョンをインストールするには、「 [Windows で AzCopy](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy)v2.0 でデータを転送する」を参照してください。

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a>AzCopy がローカルコンピューターにインストールされていないか、既定の場所にインストールされていません

AzCopy がインストールされていない場合や、既定のインストール先 (つまり`%ProgramFiles(x86)%`) 以外の場所にインストールされている場合、azcopy コマンドを実行すると、次のエラーが表示されることがあります。

    The system cannot find the path specified.

AzCopy がローカルコンピューターにインストールされていない場合は、[ここ](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy)からインストールできます。 必ず既定の場所にインストールしてください。

AzCopy がインストールされていても、既定の場所とは異なる場所にインストールされている場合は、コマンドをコピーしてテキストファイルに貼り付け、次に、AzCopy がインストールされている場所へのパスを変更することができます。 たとえば、Azcopy がに`%ProgramFiles%`ある場合は、コマンドの最初の部分をから`%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe`に`%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`変更できます。 この変更を行った後、テキストファイルからコピーし、コマンドプロンプトで実行します。

> [!TIP]
> AzCopy が既定のインストール先以外の場所にインストールされている場合は、それをアンインストールしてから、既定の場所に再インストールすることを検討してください。 これにより、今後この問題を回避することができます。
