---
title: 送信者ドメインの洞察を修正する
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: 管理者は、セキュリティ & コンプライアンスセンターのメールフローダッシュボードでの送信者ドメインの洞察を修正する方法について説明します。
ms.openlocfilehash: a416b4d15ff52a611f00a88de8440c749ff08ad3
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43635174"
---
# <a name="fix-sender-domain-insight"></a>送信者ドメインの洞察を修正する

Microsoft 365 では、内部のオンプレミスの電子メール環境から Microsoft 365 に送信されるメッセージで、特定のセキュリティ条件を満たす必要があります。

- 送信元の IP アドレスまたは証明書を使用して、オンプレミスの電子メールサーバーからの SMTP 接続を認証するために、Microsoft 365 で受信コネクタを作成しました。

- オンプレミスの電子メールサーバーを、Microsoft 365 経由で外部世界に中継するように構成しました。

- 構成では、次のいずれかのステートメントが true になります。

  - 送信者の電子メールドメインが組織に登録されている。 詳細については、「Office のドメインを追加する365」を参照してください。

  - オンプレミスの電子メールサーバーが、証明書を使用して Microsoft 365 に電子メールを送信するように構成されています。証明書は、microsoft 365 に登録したドメイン名と完全に一致しており、そのドメインを使用して Microsoft 365 に証明書ベースのコネクタが作成されています。 

条件を満たしていないメッセージは、組織には含まれず、拒否される可能性があります。

「**送信者ドメインを修正**する」には、オンプレミスの環境からの、条件に一致しないメールが表示されます。これにより、オンプレミスの電子メール環境にある潜在的に侵害されたコンピューターやユーザーアカウントを特定し、修復のアクションを実行するのに役立てることができます。

![セキュリティ & コンプライアンスセンターのメールフローダッシュボードでの送信者ドメインの洞察を修正する](../../media/sender-domain-insight-selected.png)

[詳細の**表示**] をクリックすると、次の図に示すように、詳細を含む別のウィジェットに移動します。

![「送信者ドメインを修正する」の詳細ウィジェット](../../media/sender-domain-view-details.png)

Office 365 にメッセージを配信するために使用された受信コネクタが表示されます。 [**サンプルメッセージ id の表示**] をクリックして、オンプレミスの電子メール環境から送信されたメッセージの詳細を確認することもできます。 これらのメッセージは Office 365 によって拒否されたため、メッセージ追跡を使用することはできませんが、サンプルのメッセージ id を使用してオンプレミスの電子メール環境内のメッセージを追跡できます。

![「Fix sender domain insights」のサンプルメッセージ id を表示する](../../media/sender-domain-view-sample-message-ids.png)

## <a name="see-also"></a>関連項目

メールフローダッシュボードのその他のメールフローインサイトの詳細については、「[セキュリティ & コンプライアンスセンター」の「mail flow insights](mail-flow-insights-v2.md)」を参照してください。
