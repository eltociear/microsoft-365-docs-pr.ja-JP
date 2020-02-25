---
title: Outlook で配布リストを Office 365 グループにアップグレードする
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: sirkkuw
manager: scotv
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 787d7a75-e201-46f3-a242-f698162ff09f
description: Outlook で1つまたは複数の配布リストを Office 365 グループにアップグレードする方法と、PowerShell を使用して複数の配布リストを同時にアップグレードする方法について説明します。
ms.openlocfilehash: 9e6867a5ccdb97586e3d58784a49312e078ae659
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/24/2020
ms.locfileid: "42254812"
---
# <a name="upgrade-distribution-lists-to-office-365-groups-in-outlook"></a><span data-ttu-id="1dbda-103">Outlook で配布リストを Office 365 グループにアップグレードする</span><span class="sxs-lookup"><span data-stu-id="1dbda-103">Upgrade distribution lists to Office 365 Groups in Outlook</span></span>

<span data-ttu-id="1dbda-104">Outlook を使用して配布リストを Office 365 グループにアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-104">You can upgrade distribution lists to Office 365 Groups with Outlook.</span></span> <span data-ttu-id="1dbda-105">これは、組織の配布リストに Office 365 グループのすべての機能を提供するのに便利な方法です。</span><span class="sxs-lookup"><span data-stu-id="1dbda-105">This is a great way to give your organization's distribution lists all the features and functionality of Office 365 groups.</span></span> [<span data-ttu-id="1dbda-106">Outlook で配布リストをグループにアップグレードする理由</span><span class="sxs-lookup"><span data-stu-id="1dbda-106">Why you should upgrade your distribution lists to groups in Outlook</span></span>](https://support.office.com/article/7fb3d880-593b-4909-aafa-950dd50ce188.aspx)

<span data-ttu-id="1dbda-107">配布リストは 1 つずつ、または複数を同時にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-107">You can upgrade DLs one at a time, or several at the same time.</span></span>

## <a name="upgrade-one-or-many-distribution-lists-to-office-365-groups-in-outlook"></a><span data-ttu-id="1dbda-108">Outlook で 1 つまたは複数の配布リストを Office 365 グループにアップグレードする</span><span class="sxs-lookup"><span data-stu-id="1dbda-108">Upgrade one or many distribution lists to Office 365 Groups in Outlook</span></span>

<span data-ttu-id="1dbda-109">配布リストをアップグレードするには、Office 365 全体管理者または Exchange 管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-109">You must be an Office 365 global admin or Exchange admin to upgrade a distribution list.</span></span> <span data-ttu-id="1dbda-110">Office 365 グループにアップグレードするには、配布グループがメールボックスの所有者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-110">To upgrade to Office 365 groups, a distribution group must have an owner with a mailbox.</span></span> 

1. <span data-ttu-id="1dbda-111"><a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange 管理センター</a>に移動します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-111">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>

2. <span data-ttu-id="1dbda-112">Exchange 管理センターで、[**受信者** \> **グループ**] に移動します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-112">In the Exchange admin center, go to **Recipients** \> **Groups**.</span></span><br/><span data-ttu-id="1dbda-113">Office 365 グループにアップグレードする対象である配布リスト ( **配布グループ** とも呼ばれる) があることを示す通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-113">You'll see a notice indicating you have distribution lists (also called **distribution groups** ) that are eligible to be upgraded to Office 365 groups.</span></span><br/> <span data-ttu-id="1dbda-114">![[開始] ボタンを選択する](../media/8cf838b4-2644-401f-a366-08c1eea183eb.png)</span><span class="sxs-lookup"><span data-stu-id="1dbda-114">![Select the Get started button](../media/8cf838b4-2644-401f-a366-08c1eea183eb.png)</span></span>

3. <span data-ttu-id="1dbda-115">**グループ** ページから 1 つ以上の配布リスト ( **配布グループ** とも呼ばれる) を選びます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-115">Select one or more distribution lists (also called a **distribution group** ) from the **groups** page.</span></span><br/><span data-ttu-id="1dbda-116">![配布グループを選択する](../media/2c303433-d60b-4100-a6ae-5809b03a8cdb.png)</span><span class="sxs-lookup"><span data-stu-id="1dbda-116">![Select a distribution group](../media/2c303433-d60b-4100-a6ae-5809b03a8cdb.png)</span></span>

4. <span data-ttu-id="1dbda-117">[アップグレード] アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-117">Select the upgrade icon.</span></span><br/>![Office 365 グループへのアップグレードアイコン](../media/1e28cb3d-bff3-4be3-8329-1902d2d54720.png)

5. <span data-ttu-id="1dbda-119">[情報] ダイアログで、[**はい**] を選択してアップグレードを確認します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-119">On the information dialog, select **Yes** to confirm the upgrade.</span></span> <span data-ttu-id="1dbda-120">プロセスがすぐに開始されます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-120">The process begins immediately.</span></span> <span data-ttu-id="1dbda-121">アップグレードする配布リストのサイズや数に応じて、処理には数分または数時間かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-121">Depending on the size and number of DLs you're upgrading, the process can take minutes or hours.</span></span><br/><span data-ttu-id="1dbda-122">配布リストをアップグレードできない場合は、それを示すダイアログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-122">If the distribution list can't be upgraded, a dialog appears saying so.</span></span> <span data-ttu-id="1dbda-123">[アップグレードできない配布リストがあるかどうかを](#which-distribution-lists-cannot-be-upgraded)確認します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-123">See [Which distribution lists cannot be upgraded?](#which-distribution-lists-cannot-be-upgraded).</span></span>

6. <span data-ttu-id="1dbda-124">複数の配布リストをアップグレードする場合は、ドロップダウンリストを使用して、アップグレードされた配布リストをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-124">If you're upgrading multiple distribution lists, use the drop-down list to filter which distribution lists have been upgraded.</span></span> <span data-ttu-id="1dbda-125">リストが完成していない場合は、しばらく待ってから [**更新**] を選択して、正常にアップグレードされた内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-125">If the list isn't complete, wait a while longer and then select **Refresh** to see what's been successfully upgraded.</span></span><br/><span data-ttu-id="1dbda-p106">選択した配布リストのすべてのアップグレード プロセスが完了しても、通知は表示されません。[ **アップグレード可能** ] または [ **アップグレードされた配布リスト** ] に一覧された内容を確認して、これを把握することができます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-p106">There's no notice that tells you when the upgrade process has completed for all DLs you selected. You can figure this out by looking to see what's listed under **Available for upgrade** or **Upgraded DLs**.</span></span>

7. <span data-ttu-id="1dbda-p107">アップグレードする配布リストを選択しても、ページ上に [アップグレード可能] と表示され続ける場合は、アップグレードに失敗しています。「[アップグレードが機能しない場合の対処方法](#what-to-do-if-the-upgrade-doesnt-work)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1dbda-p107">If you selected a DL for upgrade, but it's still appears on the page as Available to upgrade, then it failed to upgrade. See [What to do if the upgrade doesn't work](#what-to-do-if-the-upgrade-doesnt-work).</span></span>

> [!NOTE]
> <span data-ttu-id="1dbda-p108">グループのダイジェスト メールを受け取っている場合は、下部に通知が表示され、所有者になっている対象の配布リストをアップグレードできるように示されることがあります。ダイジェスト メールの詳細については、「[Have a group conversation in Outlook](https://support.office.com/article/a0482e24-a769-4e39-a5ba-a7c56e828b22.aspx)」 (Outlook でグループ会話を使用する) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1dbda-p108">If you're getting the groups digest emails you may notice at the bottom that it will sometimes offer to let you upgrade any eligible distribution lists that you're the owner of. See [Have a group conversation in Outlook](https://support.office.com/article/a0482e24-a769-4e39-a5ba-a7c56e828b22.aspx) for more information about digest emails.</span></span>


## <a name="what-to-do-if-the-upgrade-doesnt-work"></a><span data-ttu-id="1dbda-132">アップグレードが機能しない場合の対処方法</span><span class="sxs-lookup"><span data-stu-id="1dbda-132">What to do if the upgrade doesn't work</span></span>

<span data-ttu-id="1dbda-133">アップグレードに失敗した配布リストは、変更されないまま保持されます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-133">Distribution lists that fail to upgrade remain unchanged.</span></span>

<span data-ttu-id="1dbda-p109">1 つ以上の **対象** の配布リストがアップグレードに失敗した場合は、 [サポート チケット](../contact-support-for-business-products.md)を開きます。問題を解決するために、この問題をグループ エンジニアリング チームにエスカレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-p109">If one or more **eligible** distribution lists fail to be upgraded, open a [Support ticket](../contact-support-for-business-products.md). The issue will need to be escalated to the Groups Engineering team for them to figure out the problem.</span></span>

<span data-ttu-id="1dbda-p110">サービスが停止しているため、配布リストがアップグレードされなかった可能性もありますが、この可能性は低いです。必要な場合は、しばらく待ってから、もう一度配布リストをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="1dbda-p110">It's possible that the distribution list didn't get upgraded because of a service outage, but pretty unlikely. If you want, wait a while and then try to upgrade the DL again.</span></span>

## <a name="how-to-use-powershell-to-upgrade-several-distribution-lists-at-the-same-time"></a><span data-ttu-id="1dbda-138">PowerShell を使用して複数の配布リストを同時にアップグレードする方法</span><span class="sxs-lookup"><span data-stu-id="1dbda-138">How to use PowerShell to upgrade several distribution lists at the same time</span></span>

<span data-ttu-id="1dbda-p111">PowerShell の使用経験がある場合は、UI ではなく、この手順を使用することをお勧めします。配布リストのアップグレードに役立つ一連のコマンドレットが用意されています。以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1dbda-p111">If you're experienced at using PowerShell, you might want to go this route instead of using the UI. We have a set of cmdlets that will help you upgrade distribution lists. See below.</span></span>

### <a name="upgrade-a-single-dl"></a><span data-ttu-id="1dbda-142">1 つの DL をアップグレードする</span><span class="sxs-lookup"><span data-stu-id="1dbda-142">Upgrade a single DL</span></span>

<span data-ttu-id="1dbda-143">1 つの DL をアップグレードするには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-143">To upgrade a single DL run the following command:</span></span>

`Upgrade-DistributionGroup -DlIdentities \<Dl SMTP address\>`

<span data-ttu-id="1dbda-144">たとえば、SMTP アドレスが dl1@contoso.com の DL をアップグレードする場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-144">For example, if you want to upgrade a DLs with SMTP address dl1@contoso.com, run the following command:</span></span>

`Upgrade-DistributionGroup -DlIdentities dl1@contoso.com`

> [!NOTE]
> <span data-ttu-id="1dbda-145">[New-UnifiedGroup](https://go.microsoft.com/fwlink/?LinkID=786379) PowerShell コマンドレットを使用して、1 つの配布リストを Office 365 グループにアップグレードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-145">You can also upgrade a single distribution list to an Office 365 group using the [New-UnifiedGroup](https://go.microsoft.com/fwlink/?LinkID=786379) PowerShell cmdlet</span></span>

### <a name="upgrade-multiple-dls-in-a-batch"></a><span data-ttu-id="1dbda-146">複数の DL を一括してアップグレードする</span><span class="sxs-lookup"><span data-stu-id="1dbda-146">Upgrade multiple DLs in a batch</span></span>

<span data-ttu-id="1dbda-147">複数の DL をバッチとして渡し、まとめてアップグレードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-147">You can also pass multiple DLs as a batch and upgrade them together:</span></span>

```
Upgrade-DistributionGroup -DlIdentities \<DL SMTP address1\>, \< DL SMTP address2\>,

\< DL SMTP address3\>, \< DL SMTP address 4\>
```

<span data-ttu-id="1dbda-148">たとえば、SMTP `dl1@contoso.com`アドレス`dl2@contoso.com` `dl3@contoso.com` `dl4@contoso.com` `dl5@contoso.com`と、、を使用して5つの dl をアップグレードする場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-148">For example, if you want to upgrade five DLs with SMTP address `dl1@contoso.com` and `dl2@contoso.com`, `dl3@contoso.com`, `dl4@contoso.com` and `dl5@contoso.com`, run the following command:</span></span>

`Upgrade-DistributionGroup -DlIdentities dl1@contoso.com, dl2@contoso.com, dl3@contoso.com, dl4@contoso.com, dl5@contoso.com`

### <a name="upgrade-all-eligible-dls"></a><span data-ttu-id="1dbda-149">対象となるすべての DL をアップグレードする</span><span class="sxs-lookup"><span data-stu-id="1dbda-149">Upgrade all eligible DLs</span></span>

<span data-ttu-id="1dbda-150">対象となるすべての DL をアップグレードするには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-150">There are two ways in which you can upgrade all the eligible DLs.</span></span>

> [!NOTE]
> <span data-ttu-id="1dbda-151">このため、このコマンドレットはパイプラインからのデータを受信しません。このため、"foreach-オブジェクト{}" 演算子を使用して正常に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-151">The Upgrade-DistributionGroup cmdlet doesn't receive data from the pipeline, for this reason it's required to use "foreach-object{}" operator to run successfully.</span></span>

1. <span data-ttu-id="1dbda-152">テナント内の対象となる Dl を取得し、次のアップグレードコマンドを使用してアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="1dbda-152">Get the eligible DLs in the tenant and upgrade them using the upgrade command:</span></span>

```
Get-EligibleDistributionGroupForMigration | Foreach-Object{
    Upgrade-DistributionGroup -DlIdentities $_.PrimarySMTPAddress
}
```

2. <span data-ttu-id="1dbda-153">2.すべての DL の一覧を取得し、対象となる DL のみをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="1dbda-153">Get the list of all DLs and upgrade only the eligible DLs:</span></span>

```
Get-DistributionGroup| Foreach-Object{
    Upgrade-DistributionGroup -DlIdentities $_.PrimarySMTPAddress
}
```

## <a name="faq-about-upgrading-distribution-lists-to-office-365-groups-in-outlook"></a><span data-ttu-id="1dbda-154">Outlook での配布リストの Office 365 グループへのアップグレードに関する FAQ</span><span class="sxs-lookup"><span data-stu-id="1dbda-154">FAQ about upgrading distribution lists to Office 365 Groups in Outlook</span></span>

### <a name="which-distribution-lists-cannot-be-upgraded"></a><span data-ttu-id="1dbda-155">アップグレードできない配布リスト</span><span class="sxs-lookup"><span data-stu-id="1dbda-155">Which distribution lists cannot be upgraded?</span></span>

<span data-ttu-id="1dbda-156">クラウド管理されている、単純で入れ子になっていない配布リストのみをアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-156">You can only upgrade cloud-managed, simple, non-nested distribution lists.</span></span> <span data-ttu-id="1dbda-157">次の表は、アップグレード**できない**配布リストを示しています。</span><span class="sxs-lookup"><span data-stu-id="1dbda-157">The table below lists distribution lists that **CANNOT** be upgraded.</span></span>

|<span data-ttu-id="1dbda-158">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="1dbda-158">**Property**</span></span>|<span data-ttu-id="1dbda-159">**対象**</span><span class="sxs-lookup"><span data-stu-id="1dbda-159">**Eligible?**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1dbda-160">オンプレミスで管理される配布リスト</span><span class="sxs-lookup"><span data-stu-id="1dbda-160">On-premises managed distribution list.</span></span>  <br/> |<span data-ttu-id="1dbda-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-161">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-p113">入れ子になった配布リスト子グループがあるか、または別のグループのメンバーである配布リスト</span><span class="sxs-lookup"><span data-stu-id="1dbda-p113">Nested distribution lists. Distribution list either has child groups or is a member of another group.</span></span>  <br/> |<span data-ttu-id="1dbda-164">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-164">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-165">メンバー受信者を含む配布リスト**Usermailbox**、 **sharedmailbox**、 **teammailbox**、 **mailuser**以外の種類の**詳細**</span><span class="sxs-lookup"><span data-stu-id="1dbda-165">Distribution lists with member **RecipientTypeDetails** other than **UserMailbox**, **SharedMailbox**, **TeamMailbox**, **MailUser**</span></span>  <br/> |<span data-ttu-id="1dbda-166">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-166">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-167">100 人を超える所有者を含む配布リスト</span><span class="sxs-lookup"><span data-stu-id="1dbda-167">Distribution list which has more than 100 owners</span></span>  <br/> |<span data-ttu-id="1dbda-168">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-168">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-169">メンバーのみで、所有者を含まない配布リスト</span><span class="sxs-lookup"><span data-stu-id="1dbda-169">Distribution list which only has members but no owner</span></span>  <br/> |<span data-ttu-id="1dbda-170">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-170">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-171">特殊文字を含むエイリアスがある配布リスト</span><span class="sxs-lookup"><span data-stu-id="1dbda-171">Distribution list which has alias containing special characters</span></span>  <br/> |<span data-ttu-id="1dbda-172">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-172">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-173">配布リストが共有メールボックスの転送アドレスになるように構成されている場合</span><span class="sxs-lookup"><span data-stu-id="1dbda-173">If the distribution list is configured to be a forwarding address for Shared Mailbox</span></span>  <br/> |<span data-ttu-id="1dbda-174">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-174">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-175">DL が別の DL の**Sender 制限**の一部である場合。</span><span class="sxs-lookup"><span data-stu-id="1dbda-175">If the DL is part of **Sender Restriction** in another DL.</span></span>  <br/> |<span data-ttu-id="1dbda-176">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-176">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-177">セキュリティ グループ</span><span class="sxs-lookup"><span data-stu-id="1dbda-177">Security groups</span></span>  <br/> |<span data-ttu-id="1dbda-178">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-178">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-179">動的配布リスト</span><span class="sxs-lookup"><span data-stu-id="1dbda-179">Dynamic Distribution lists</span></span>  <br/> |<span data-ttu-id="1dbda-180">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-180">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-181">**RoomLists**に変換された配布リスト</span><span class="sxs-lookup"><span data-stu-id="1dbda-181">Distribution lists which were converted to **RoomLists**</span></span>  <br/> |<span data-ttu-id="1dbda-182">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-182">No</span></span>  <br/> |
|<span data-ttu-id="1dbda-183">**Memberjoinrestriction**または**MemberDepartRestriction**を**閉じる**配布リスト</span><span class="sxs-lookup"><span data-stu-id="1dbda-183">Distribution lists where **MemberJoinRestriction** and/or **MemberDepartRestriction** is **Closed**</span></span>  <br/> |<span data-ttu-id="1dbda-184">いいえ</span><span class="sxs-lookup"><span data-stu-id="1dbda-184">No</span></span>  <br/> |

### <a name="how-do-i-check-which-dls-are-eligible-for-upgrade"></a><span data-ttu-id="1dbda-185">アップグレードの対象となる DL を確認するにはどうすればよいですか?</span><span class="sxs-lookup"><span data-stu-id="1dbda-185">How do I check which DLs are eligible for upgrade?</span></span>

<span data-ttu-id="1dbda-186">ある DL がアップグレード対象かどうかを確認するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-186">If you want to check whether a DL is eligible or not, you can run the below command:</span></span>

`Get-DistributionGroup \<DL SMTP address\> | Get-EligibleDistributionGroupForMigration`

<span data-ttu-id="1dbda-187">アップグレード対象の DL を確認する場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-187">If you want to check which DLs are eligible for upgrade just run the following command:</span></span>

`Get-EligibleDistributionGroupForMigration`

### <a name="who-can-run-the-upgrade-scripts"></a><span data-ttu-id="1dbda-188">どのユーザーがアップグレード スクリプトを実行できますか?</span><span class="sxs-lookup"><span data-stu-id="1dbda-188">Who can run the upgrade scripts?</span></span>

<span data-ttu-id="1dbda-189">Office 365 全体管理者または Exchange 管理者の権限を持つユーザーです。</span><span class="sxs-lookup"><span data-stu-id="1dbda-189">People with Office 365 global admin or Exchange admin rights.</span></span>

### <a name="why-is-the-contact-card-still-showing-a-distribution-list-what-should-i-do-to-prevent-a-upgraded-distribution-list-from-showing-up-in-my-auto-suggest-list"></a><span data-ttu-id="1dbda-190">連絡先カードに依然として配布リストが表示されるのはなぜでしょうか。</span><span class="sxs-lookup"><span data-stu-id="1dbda-190">Why is the contact card still showing a distribution list?</span></span> <span data-ttu-id="1dbda-191">アップグレードした配布リストが自動提案リストに表示されないようにするにはどうすればよいでしょうか。</span><span class="sxs-lookup"><span data-stu-id="1dbda-191">What should I do to prevent a upgraded distribution list from showing up in my auto suggest list?</span></span>

- <span data-ttu-id="1dbda-192">Outlook の場合: 移行後に Office 365 グループ名を入力して Outlook でメールを送信しようとすると、受信者はグループではなく配布リストとして解決されます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-192">For Outlook: When someone tries to send an email in Outlook by typing the Office 365 group name after migration, the recipient will be resolved as the distribution list instead of the group.</span></span> <span data-ttu-id="1dbda-193">受信者の連絡先カードは配布リストの連絡先カードとなります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-193">The contact card of the recipient will be the distribution lists contact card.</span></span> <span data-ttu-id="1dbda-194">これは Outlook の受信者キャッシュまたはニックネーム キャッシュに起因します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-194">This is because of the recipient cache or nick name cache in Outlook.</span></span> <span data-ttu-id="1dbda-195">電子メールはグループに正常に送信されますが、送信者に混乱を招く可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-195">The email will be sent successfully to the group, but might cause confusion to the sender.</span></span><br/><span data-ttu-id="1dbda-196">「[Outlook のオートコンプリートの一覧についての情報](https://go.microsoft.com/fwlink/?LinkID=798736)」というトピックにある手順を実行してキャッシュをリセットすると、この問題は解消されます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-196">You can perform the steps in this topic, [Information about the Outlook AutoComplete list](https://go.microsoft.com/fwlink/?LinkID=798736) to reset the cache, which will fix this issue.</span></span>

- <span data-ttu-id="1dbda-197">Web 上の Outlook の場合: web 上の Outlook の場合、配布リストの受信者はキャッシュに残ります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-197">For Outlook on the web: In case of Outlook on the web, the distribution list recipient will still remain in the cache.</span></span> <span data-ttu-id="1dbda-198">[オートコンプリートリストから [候補の名前または電子メールアドレスを削除](https://support.office.com/article/9E1419D9-E88F-445B-B07F-F558B8A37C58.aspx)する] の手順に従って、キャッシュを更新し、グループの連絡先カードを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-198">You can follow the steps in [Remove suggested name or email address from the Auto-Complete List](https://support.office.com/article/9E1419D9-E88F-445B-B07F-F558B8A37C58.aspx) to refresh the cache to see the group contact card.</span></span>

### <a name="do-new-group-members-get-a-welcome-email-in-their-inbox"></a><span data-ttu-id="1dbda-199">新しいグループのメンバーは、受信トレイでウェルカム メッセージを受け取りますか?</span><span class="sxs-lookup"><span data-stu-id="1dbda-199">Do new group members get a welcome email in their inbox?</span></span>

<span data-ttu-id="1dbda-p117">いいえ。ウェルカム メッセージを有効にする設定は、既定で false に設定されています。この設定は、既存のグループ メンバーにも、移行が完了した後に参加する可能性がある新しいグループ メンバーにも影響します。グループの所有者が後でゲスト ユーザーを許可した場合、ゲスト ユーザーは受信トレイでウェルカム メールを受け取ることはありません。ゲスト メンバーはグループで継続して作業を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1dbda-p117">No. The setting to enable welcome messages is set to false by default. This setting affects both existing and new group members who may join after the migration is complete. If the group owner later allows guest users, guest users won't receive a welcome email in their inbox. Guest members can continue working with the group.</span></span>

### <a name="what-if-one-or-some-of-the-dls-are-not-upgraded"></a><span data-ttu-id="1dbda-205">1つまたは一部の Dl がアップグレードされていない場合はどうなりますか?</span><span class="sxs-lookup"><span data-stu-id="1dbda-205">What if one or some of the DLs are not upgraded?</span></span>

<span data-ttu-id="1dbda-206">DL が対象になるが、アップグレードできない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-206">There are some cases in which though DL is eligible but could not be upgraded.</span></span> <span data-ttu-id="1dbda-207">DL はアップグレードされず、DL として残ります。</span><span class="sxs-lookup"><span data-stu-id="1dbda-207">The DL does not get upgraded and remains as a DL.</span></span>

- <span data-ttu-id="1dbda-208">管理者が組織内のグループに対して**グループ電子メールアドレスポリシー**を適用していて、条件を満たしていない DLs をアップグレードしようとした場合、dl はアップグレードされません。</span><span class="sxs-lookup"><span data-stu-id="1dbda-208">Where admin has applied **Group Email Address Policy** for the groups in an organization and they try to upgrade DLs which doesn't fulfill the criteria, the DL does not get upgraded</span></span>

- <span data-ttu-id="1dbda-209">**Memberjoinrestriction**または**MemberDepartRestriction**を**Closed**に設定した dl をアップグレードできませんでした</span><span class="sxs-lookup"><span data-stu-id="1dbda-209">DLs with **MemberJoinRestriction** or **MemberDepartRestriction** set to **Closed**, could not be upgraded</span></span>

### <a name="what-happens-to-the-dl-if-the-upgrade-from-eac-fails"></a><span data-ttu-id="1dbda-210">EAC からのアップグレードに失敗した場合、配布リストはどうなりますか?</span><span class="sxs-lookup"><span data-stu-id="1dbda-210">What happens to the DL if the upgrade from EAC fails?</span></span>

<span data-ttu-id="1dbda-p119">呼び出しがサーバーに送信された場合にのみ、アップグレードが発生します。アップグレードが失敗した場合、配布リストはそのまま保持されます。配布リストは、以前のように動作します。</span><span class="sxs-lookup"><span data-stu-id="1dbda-p119">The upgrade will happen only when the call is submitted to the server. If the upgrade fails, your DLs will be intact. They will work like they used to.</span></span>

