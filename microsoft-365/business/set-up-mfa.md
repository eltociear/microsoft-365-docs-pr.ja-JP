---
title: 多要素認証をセットアップする
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- MiniMaven
- MSB365
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
description: Microsoft 365 Business で多要素認証をセットアップします。
ms.openlocfilehash: 3aa08670551da3754784237e14a35e94c6f64250
ms.sourcegitcommit: bd52f7b662887f552f90c46f69d6a2a42fb66914
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2019
ms.locfileid: "37575625"
---
# <a name="multi-factor-authentication"></a><span data-ttu-id="967f7-103">多要素認証</span><span class="sxs-lookup"><span data-stu-id="967f7-103">Multi-factor authentication</span></span>

<span data-ttu-id="967f7-104">多要素認証 (MFA) では、ユーザーは2番目の方法でサインインして、電話またはオーセンティケータアプリで自分の身元を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="967f7-104">Multi-factor authentication (MFA) requires users to sign in with a second method to verify their identity with a phone call or with an authenticator app.</span></span>

## <a name="set-up-mfa-in-the-microsoft-365-admin-center"></a><span data-ttu-id="967f7-105">Microsoft 365 管理センターで MFA をセットアップする</span><span class="sxs-lookup"><span data-stu-id="967f7-105">Set up MFA in the Microsoft 365 admin center</span></span>

<span data-ttu-id="967f7-106">[![[ラベル] 管理センターが変更されたことを知らせるために、aka.ms/aboutM365preview で詳細を確認できます。](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span><span class="sxs-lookup"><span data-stu-id="967f7-106">[![Label to let you know the admin center is changing and you can find more details at aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span></span>

1. <span data-ttu-id="967f7-107">グローバル管理者の資格情報を使用して、 [Microsoft 365 管理センター](https://admin.microsoft.com)にサインインします。</span><span class="sxs-lookup"><span data-stu-id="967f7-107">Sign in to [Microsoft 365 admin center](https://admin.microsoft.com) by using your global admin credentials.</span></span> 
2. <span data-ttu-id="967f7-108">左側のナビゲーションで、[**セットアップ**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="967f7-108">On the left nav, choose **Setup**.</span></span>
3. <span data-ttu-id="967f7-109">[セットアップ] ページで、[**多要素認証 (MFA) カードを有効にする** **] を選択し**ます。</span><span class="sxs-lookup"><span data-stu-id="967f7-109">On the Setup page, choose **View** on the **Turn on multi-factor authentication (MFA)** card.</span></span>
4. <span data-ttu-id="967f7-110">[ **Mfa を有効**にする] ページで、[**開始**] を選択するか、既に MFA を設定して変更を行う場合は [**管理**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="967f7-110">On the **Turn on MFA** page, choose **Get started**, or **Manage** if you have already set up MFA and want to make changes.</span></span> 

  <span data-ttu-id="967f7-111">:::image type="content" source="media/turnonmfa.png" alt-text="[MFA] ページを有効にするスクリーンショット。":::</span><span class="sxs-lookup"><span data-stu-id="967f7-111">:::image type="content" source="media/turnonmfa.png" alt-text="Screenshot of turn on MFA page.":::</span></span>

5. <span data-ttu-id="967f7-112">[ **Strenghen サインインセキュリティ**] パネルで、[**管理者に対して多要素認証を必要とする**] または [**ポリシーの作成**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="967f7-112">On the **Strenghen sign-in security** panel, check both or one of **Require multi-factor authentication for admins**, and then choose **Create policy**.</span></span>