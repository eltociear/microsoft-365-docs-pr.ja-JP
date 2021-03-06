---
title: EOP とは
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
ms.reviewer: andypunt
manager: dansimp
ms.date: 02/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 393b0050-7c7e-49e6-a03d-b1e09fe4de9e
description: この入門ドキュメントは、Exchange Online Protection (EOP) といくつかの重要な用語を理解するのに役立ちます。 これは、exchange Online のクラウドホスト型メールボックスを保護している、または Exchange Server 2016 などのオンプレミスのメールボックスを保護している EOP スタンドアロンのお客様に適用されます。
ms.openlocfilehash: dc08507a80db8e15d2e08ff5b954dec1905cfada
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43630919"
---
# <a name="what-is-exchange-online-protection-eop"></a>Exchange Online Protection (EOP) とは

Exchange Online Protection (EOP) は、クラウドベースの電子メールフィルター処理サービスであり、スパムやマルウェアから組織を保護します。 メールボックスが Microsoft 365 にある場合は、サービスの一部であるため、EOP によって自動的に保護されます。 これには、Microsoft 365 とオンプレミスの両方にメールボックスがあり、ハイブリッドシナリオとしてよく知られている組織が含まれます。 EOP スタンドアロンは、クラウドにメールボックスを持っていないが、社内メールボックスを保護する必要があるお客様も利用できます。

EOP は迷惑メールのフィルターを試行し、ユーザーが表示したくないコンテンツを受信トレイがクリアしないようにします。 通常、迷惑メールは [迷惑メール] フォルダーに配信されます。 迷惑メールフォルダーが自分で必要なことを確認するための簡単な方法であることを確認するために、フィルター処理で必要なことを確認することができます。  

> [!TIP]
> 迷惑メールやその他の不正な電子メールが迷惑メールフォルダーに自動的に送られる場合に適しています。 サービスは、既定またはカスタムの管理者設定の状態に基づいて必要な処理を実行します。 言い換えると、ユーザーは迷惑メールフォルダーに多数のスパムメールを表示することを心配する必要はありません。 管理者がすべての迷惑メールを視界から除外することを希望している場合は、検疫を構成する必要があります。 詳細については、「[検疫メールメッセージ](quarantine-email-messages.md)」の記事を参照してください。

## <a name="important-terms"></a>重要な用語

**Inbound**: Microsoft 365 に入ってくるメッセージ。

**送信**: Microsoft 365 から出てきたメッセージ。

**Internal**: 組織内のユーザーから組織内のユーザーに送信されるメッセージ。 これには、ハイブリッドシナリオを使用していて、1つのメールボックスがオンプレミスになっていて、他のメールボックスがクラウド内に存在する可能性があるユーザーが含まれます。

**誤負 (FN)**: スパムやその他の迷惑メールが、受信トレイに正しく送信されません。

**誤検知 (FP)**: 誤ってスパムとしてマークされ、迷惑メールフォルダーまたは検疫に入れられる正当なメッセージ。

**スパム (迷惑メールとも呼ば**れます): これには、商業広告、チェーンレター、政治的メールなどの形式があります。これは、ユーザーが電子メールを送信しようとしたり、不正なコミットを試行したりしているスパムからのサインアップを行わないメールです。

**フィッシング**: フィッシングとは、id の盗難または詐欺を防止する目的で個人情報を提供することを目的とする特別な種類のスパムです。 通常、この種類のメッセージには、悪意のあるリンクや添付ファイルが含まれますが、常には含まれません。

**スプーフィング: スプーフィング**は、スパム送信者が from ヘッダーを偽造して、メッセージが実際の送信元以外の場所から発信されたように見えるようにします。 これはスパムでもかまいませんが、フィッシングユーザーに最もよく使用されます。

**偽装**: この種のスパムは、送信者アドレスを偽造する方法でもありますが、実際のソースのようになるように、名前またはドメインの一部を変更することによって行われます。 たとえば、請求書の "l" が実際には11で、Microsoft の "o" が0という数字に置き換えられていると、Bi11@micr0s0ft.com のようになります。

**Bulk**: バルクメールは通常、ユーザーによって要請されますが、企業が他の企業に情報を販売するときに間接的に発生する場合があります。 通常、ユーザーは大量のメール (newletters) に意図的にサインアップしていますが、後で忘れることはなく、スパムであると考えられます。 バルクメールが送信されると、ユーザーがサインアップするよりも多くの場合、大量メールがスパムになる。
