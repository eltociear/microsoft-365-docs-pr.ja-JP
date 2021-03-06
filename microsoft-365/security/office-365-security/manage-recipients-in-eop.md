---
title: EOP で受信者を管理する
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 2921f544-8257-4bae-8e3a-ce9250e9f162
description: Microsoft Exchange Online Protection (EOP) には、メールの受信者を管理するためのいくつかの方法が備わっています。 管理者は、Exchange 管理センター (EAC) またはリモート Windows PowerShell を使用して特定の管理タスクを実行し、Microsoft 365 管理センターで実行されたその他の管理タスクを確認できます。
ms.openlocfilehash: b5d1efa0fb54b97f226f25375fb747e5373a36cd
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43635342"
---
# <a name="manage-recipients-in-eop"></a>EOP で受信者を管理する

Microsoft Exchange Online Protection (EOP) には、メールの受信者を管理するためのいくつかの方法が備わっています。 管理者は、Exchange 管理センター (EAC) またはリモート Windows PowerShell を使用して特定の管理タスクを実行し、Microsoft 365 管理センターで実行されたその他の管理タスクを確認できます。

EOP は次の受信者の種類をサポートします。

- **メールユーザー**: メールユーザーは、EOP 管理対象ドメインの受信者です。 これらの受信者は、組織内にログオン資格情報を持っていますが、外部の電子メールアドレスを持っています。つまり、受信者のメールボックスはクラウド組織外にあります。

  メールを受信できるようにメールユーザーを追加したり、特定のユーザーのメールフロールール (トランスポートルールとも呼ばれます) を作成したりすることもできます。 組織内のメールユーザーに役割を割り当てることもできます。管理役割グループの権限を持つユーザーは、Exchange 管理センター (EAC) にアクセスして、特定の管理タスクを実行できます。 ユーザーの役割と、EOP でユーザーの役割を割り当てる方法の詳細については、「 [Manage admin role group permissions IN EOP](manage-admin-role-group-permissions-in-eop.md)」を参照してください。

  EOP でのメール ユーザーの管理方法については、「[EOP でメール ユーザーを管理する](manage-mail-users-in-eop.md)」を参照してください。

- **グループ**: メールユーザーを配布グループまたはセキュリティグループにまとめてグループ化できます。

EOP でのグループの管理方法については、「[EOP でグループを管理する](manage-groups-in-eop.md)」を参照してください。
