---
title: ユーザーにセキュリティ/コンプライアンス センターへのアクセス権を付与する
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: ユーザーがセキュリティまたはコンプライアンス機能を管理する前に、セキュリティ & コンプライアンスセンターでアクセス許可を割り当てる必要があります。
ms.openlocfilehash: 5110bcecb6731cbf51023c6df19bed30bcba72c1
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43638060"
---
# <a name="give-users-access-to-the-security--compliance-center"></a>ユーザーにセキュリティ/コンプライアンス センターへのアクセス権を付与する

ユーザーがセキュリティまたはコンプライアンス機能を管理する前に、セキュリティ & コンプライアンスセンターでアクセス許可を割り当てる必要があります。 セキュリティ & コンプライアンスセンターでは、組織の全体管理者または組織のメンバーとして、これらのアクセス許可をユーザーに与えることができます。 ユーザーが管理できるのは、アクセス権が付与されたセキュリティまたはコンプライアンスの機能のみです。

セキュリティ & コンプライアンスセンターでユーザーに付与できるさまざまなアクセス許可の詳細については、「[セキュリティ & コンプライアンスセンターでアクセス許可](permissions-in-the-security-and-compliance-center.md)を確認する」を参照してください。

## <a name="what-do-you-need-to-know-before-you-begin"></a>始める前に把握しておくべき情報

- この記事に記載されている手順を完了するには、グローバル管理者であるか、またはセキュリティ & コンプライアンスセンターの組織の組織の管理役割グループのメンバーである必要があります。

- セキュリティ & コンプライアンスセンターの役割グループには、Exchange Online の役割グループと同じような名前が付いている場合がありますが、これらは同じではありません。

- 役割グループのメンバーシップは、Exchange Online とセキュリティ & コンプライアンスセンターとの間で共有されません。

- (AOBO) 権限を持つ代理アクセス許可 (DAP) パートナーは、セキュリティ & コンプライアンスセンターにアクセスできません。

## <a name="use-the-admin-center-to-give-another-user-access-to-the-security--compliance-center"></a>管理センターを使用して、別のユーザーにセキュリティ & コンプライアンスセンターへのアクセス権を付与する

1. [サインインして、管理センターに移動](https://docs.microsoft.com/microsoft-365/compliance/go-to-the-securitycompliance-center)します。

2. Microsoft 365 管理センターで、**管理センター**を開き、[**セキュリティ & コンプライアンス**] をクリックします。

3. [セキュリティ & コンプライアンスセンター] で、[**アクセス許可**] に移動します。

4. リストからユーザーを追加する役割グループを選択し、 **[編集] [** ![編集] アイコン](../../media/O365-MDM-CreatePolicy-EditIcon.gif)をクリックします。

5. 役割グループのプロパティページの [**メンバー**] で、 **[追加]**![アイコン](../../media/ITPro-EAC-AddIcon.gif)をクリックし、追加するユーザーの名前を選択します。

6. 役割グループに追加するすべてのユーザーを選択したら、[ **\>追加**] をクリックし、[ **OK]** をクリックします。

7. **[保存]** をクリックして、役割グループに加えた変更を保存します。

### <a name="how-do-you-know-this-worked"></a>正常な動作を確認する方法

1. [セキュリティ & コンプライアンスセンター] で、[**アクセス許可**] に移動します。

2. リストから、メンバーを表示する役割グループを選択します。

3. 右側の役割グループの詳細では、役割グループのメンバーを表示できます。

## <a name="use-powershell-to-give-another-user-access-to-the-security--compliance-center"></a>PowerShell を使用して、別のユーザーにセキュリティ & コンプライアンスセンターへのアクセス権を付与する

1. [セキュリティ/コンプライアンス センターの PowerShell に接続する](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)。

2. 次の例で示すように、**Add-RoleGroupMember** コマンドを使用して、ユーザーを Organization Management の役割に追加できます。

   ```PowerShell
   Add-RoleGroupMember -Identity "Organization Management" -Member MatildaS
   ```

   **パラメーター**:

   - _Identity_は、メンバーを追加する役割グループです。

   - _Member_は、役割グループに追加するメールボックス、ユニバーサルセキュリティグループ (USG)、またはコンピューターです。 一度に 1 メンバーしか指定できません。

構文とパラメーターの詳細については、「 [add-rolegroupmember](https://docs.microsoft.com/powershell/module/exchange/role-based-access-control/Add-RoleGroupMember)」を参照してください。

### <a name="how-do-you-know-this-worked"></a>正常な動作を確認する方法

ユーザーにセキュリティ & コンプライアンスセンターへのアクセス権が与えられたことを確認するには、次の例に示すように、 **add-rolegroupmember**コマンドレットを使用して組織の管理役割グループのメンバーを表示します。

```PowerShell
Get-RoleGroupMember -Identity "Organization Management"
```

構文とパラメーターの詳細については、「 [add-rolegroupmember](https://docs.microsoft.com/powershell/module/exchange/role-based-access-control/Get-RoleGroupMember)」を参照してください。
