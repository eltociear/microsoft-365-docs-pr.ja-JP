---
title: Office 365 の電子メールの暗号化
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/28/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: c0d87cbe-6d65-4c03-88ad-5216ea5564e8
ms.collection:
- M365-security-compliance
description: Office Message Encryption (OME)、S/MIME、Information Rights Management (IRM) など、Office 365 での暗号化のオプションを比較し、トランスポート層セキュリティ (TLS) について紹介します。
ms.openlocfilehash: 79a7ddd13e437255fa671e949236c879b235c2ba
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2019
ms.locfileid: "37085916"
---
# <a name="email-encryption-in-office-365"></a><span data-ttu-id="d4c3a-103">Office 365 の電子メールの暗号化</span><span class="sxs-lookup"><span data-stu-id="d4c3a-103">Email encryption in Office 365</span></span>

<span data-ttu-id="d4c3a-104">この記事では、Office Message Encryption (OME)、S/MIME、Information Rights Management (IRM) など、Office 365 での暗号化のオプションを比較し、トランスポート層セキュリティ (TLS) について紹介します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-104">Compares encryption options in Office 365 including Office Message Encryption (OME), S/MIME, Information Rights Management (IRM), and introduces Transport Layer Security (TLS).</span></span>
  
<span data-ttu-id="d4c3a-105">Office 365 では、電子メールのセキュリティのビジネス ニーズを満たすために複数の暗号化オプションが提供されています。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-105">Office 365 delivers multiple encryption options to help you meet your business needs for email security.</span></span> <span data-ttu-id="d4c3a-106">この記事では、Office 365 でメールを暗号化する 3 つの方法を紹介します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-106">This article presents three ways to encrypt email in Office 365.</span></span> <span data-ttu-id="d4c3a-107">Office 365 のすべてのセキュリティ機能については、[Office 365 トラスト センター](http://go.microsoft.com/fwlink/p/?LinkID=282470)にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-107">If you want to learn more about all security features in Office 365, visit the [Office 365 Trust Center](http://go.microsoft.com/fwlink/p/?LinkID=282470).</span></span> <span data-ttu-id="d4c3a-108">この記事では、Office 365 管理者が Office 365 で電子メールを保護する上で役立つ次の 3 つの種類の暗号化を紹介します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-108">This article presents the three types of encryption available for Office 365 administrators to help secure email in Office 365:</span></span>
  
- <span data-ttu-id="d4c3a-109">Office Message Encryption (OME)。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-109">Office Message Encryption (OME).</span></span>

- <span data-ttu-id="d4c3a-110">Secure/Multipurpose Internet Mail Extensions (S/MIME)。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-110">Secure/Multipurpose Internet Mail Extensions (S/MIME).</span></span>

- <span data-ttu-id="d4c3a-111">Information Rights Management (IRM)。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-111">Information Rights Management (IRM).</span></span>

## <a name="what-is-email-encryption-and-how-does-office-365-use-it"></a><span data-ttu-id="d4c3a-112">電子メールの暗号化とはどのようなもので、Office 365 ではどのように使用しますか?</span><span class="sxs-lookup"><span data-stu-id="d4c3a-112">What is email encryption and how does Office 365 use it?</span></span>

<span data-ttu-id="d4c3a-113">暗号化とは、認証された受信者だけが特定の情報をデコードおよび利用できるようにその情報をエンコードするプロセスのことです。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-113">Encryption is the process by which information is encoded so that only an authorized recipient can decode and consume the information.</span></span> <span data-ttu-id="d4c3a-114">Office 365 では、サービスでの使用とカスタマー コントロールとしての使用の 2 つの方法で暗号化を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-114">Office 365 uses encryption in two ways: in the service, and as a customer control.</span></span> <span data-ttu-id="d4c3a-115">サービスでは、暗号化は Office 365 で既定で使用されるため、ユーザーによる設定は特に必要ありません。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-115">In the service, encryption is used in Office 365 by default; you don't have to configure anything.</span></span> <span data-ttu-id="d4c3a-116">たとえば、Office 365 はトランスポート層セキュリティ (TLS) を使用して、2 つのサーバー間の接続またはセッションを暗号化します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-116">For example, Office 365 uses Transport Layer Security (TLS) to encrypt the connection, or session, between two servers.</span></span> 
  
<span data-ttu-id="d4c3a-117">一般的な電子メールの暗号化のしくみは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-117">Here’s how email encryption typically works:</span></span>
  
- <span data-ttu-id="d4c3a-118">メッセージの送信中に送信者のコンピューターまたは中央サーバーによって、メッセージがプレーンテキストから読み取り不可能な暗号テキストに暗号化または変換されます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-118">A message is encrypted, or transformed from plain text into unreadable ciphertext, either on the sender’s machine, or by a central server while the message is in transit.</span></span>

- <span data-ttu-id="d4c3a-119">メッセージが途中で読み取られることを防ぐため、送信中のメッセージは暗号テキストのままです。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-119">The message remains in ciphertext while it's in  transit in order to protect it from being read in case the message is intercepted.</span></span>

- <span data-ttu-id="d4c3a-120">受信者がメッセージを受信すると、メッセージは次の 2 つの方法で読み取り可能なプレーンテキストに変換し直されます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-120">Once the message is received by the recipient, the message is transformed back into readable plain text in one of two ways:</span></span>

  - <span data-ttu-id="d4c3a-121">受信者のコンピューターでキーを使用してメッセージを解読するか、</span><span class="sxs-lookup"><span data-stu-id="d4c3a-121">The recipient’s machine uses a key to decrypt the message, or</span></span>

  - <span data-ttu-id="d4c3a-122">受信者の身元を確認した後に、受信者の代わりに中央サーバーでメッセージを解読します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-122">A central server decrypts the message on behalf of the recipient, after validating the recipient’s identity.</span></span>

<span data-ttu-id="d4c3a-123">Office 365 内の組織間、または Office 365 と Office 365 外部の信頼できるビジネス パートナー間など、Office 365 でサーバー間の通信をセキュリティで保護する方法については、「[Exchange Online が TLS を使って Office 365 のメール接続をセキュリティで保護する方法](exchange-online-uses-tls-to-secure-email-connections.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-123">For more information on how Office 365 secures communication between servers, for example between organizations within Office 365 or between Office 365 and a trusted business partner outside of Office 365, see [How office 365 uses TLS to secure connections between servers](exchange-online-uses-tls-to-secure-email-connections.md).</span></span>
  
<span data-ttu-id="d4c3a-124">[Office 365 の暗号化](https://www.youtube.com/watch?v=KmfxCd5ublI)の概要はこの動画でご覧いただけます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-124">Watch this video for an introduction to [Encryption in Office 365https://www.youtube.com/watch?v=KmfxCd5ublI](https://www.youtube.com/watch?v=KmfxCd5ublI).</span></span>
  
## <a name="comparing-email-encryption-options-available-in-office-365"></a><span data-ttu-id="d4c3a-125">Office 365 で使用可能な電子メール暗号化オプションの比較</span><span class="sxs-lookup"><span data-stu-id="d4c3a-125">Comparing email encryption options available in Office 365</span></span>

||![OME を説明する概念アートワーク](media/2bf27b5e-bbb3-46d1-95bf-884dc27a746c.png)|![IRM を説明する概念アートワーク](media/9c0cc444-9448-40c6-b244-8fcc593a64e0.png)|![SMIME を説明する概念アートワーク](media/ae4613a8-c17e-47e1-8e13-12e891e43744.png)|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d4c3a-129">暗号化オプションの説明</span><span class="sxs-lookup"><span data-stu-id="d4c3a-129">What is it?</span></span>|<span data-ttu-id="d4c3a-p103">Office 365 Message Encryption (OME) は、Azure Rights Management (Azure RMS) で構築され、宛先のメール アドレス (Gmail、Yahoo! Mail、Outlook.com など) に関係なく、暗号化された電子メールを組織内外の宛先に送信できるようにするサービスです。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-p103">Office 365 Message Encryption (OME) is a service built on Azure Rights Management (Azure RMS) that lets you send encrypted email to people inside or outside your organization, regardless of the destination email address (Gmail, Yahoo! Mail, Outlook.com, etc.).</span></span> <br/> <span data-ttu-id="d4c3a-p104">管理者は、暗号化の条件を定義するトランスポート ルールを設定できます。ユーザーがルールに一致するメッセージを送信する場合、自動的に暗号化が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-p104">As an admin, you can set up transport rules that define the conditions for encryption. When a user sends a message that matches a rule, encryption is applied automatically.</span></span> <br/> <span data-ttu-id="d4c3a-134">暗号化メッセージを表示するために、受信者は 1 回限りのパスコードを取得するか、Microsoft アカウントでサインインするか、Office 365 に関連付けられている職場または学校のアカウントでサインインできます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-134">To view encrypted messages, recipients can either get a one-time passcode, sign in with a Microsoft account, or sign in with a work or school account associated with Office 365.</span></span> <span data-ttu-id="d4c3a-135">受信者は暗号化された返事を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-135">Recipients can also send encrypted replies.</span></span> <span data-ttu-id="d4c3a-136">暗号化されたメッセージを表示したり、暗号化された返信を送信するのに、受信者は Office 365 サブスクリプションを必要としません。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-136">They don’t need an Office 365 subscription to view encrypted messages or send encrypted replies.</span></span>|<span data-ttu-id="d4c3a-p106">IRM は、電子メール メッセージに使用制限の適用も行える暗号化ソリューションです。機密情報が権限のないユーザーによって印刷、転送、またはコピーされるのを防止します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-p106">IRM is an encryption solution that also applies usage restrictions to email messages. It helps prevent sensitive information from being printed, forwarded, or copied by unauthorized people.</span></span> <br/> <span data-ttu-id="d4c3a-139">Office 365 の IRM 機能には Azure Rights Management (Azure RMS) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-139">IRM capabilities in Office 365 use Azure Rights Management (Azure RMS).</span></span>|<span data-ttu-id="d4c3a-140">S/MIME は証明書基盤の暗号化ソリューションであり、メッセージを暗号化し、デジタル署名できます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-140">S/MIME is a certificate-based encryption solution that allows you to both encrypt and digitally sign a message.</span></span> <span data-ttu-id="d4c3a-141">メッセージを暗号化することで、本来の受信者だけがメッセージを開き、閲覧できます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-141">The message encryption helps ensure that only the intended recipient can open and read the message.</span></span> <span data-ttu-id="d4c3a-142">デジタル署名は、受信者が送信者の身元を確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-142">A digital signature helps the recipient validate the identity of the sender.</span></span> <br/> <span data-ttu-id="d4c3a-143">デジタル署名と暗号化メッセージのいずれも、独自のデジタル証明書の利用により可能となります。この証明書には、デジタル署名を検証し、メッセージを暗号化し、復号化するための鍵が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-143">Both digital signatures and message encryption are made possible through the use of unique digital certificates that contain the keys for verifying digital signatures and encrypting or decrypting messages.</span></span> <br/> <span data-ttu-id="d4c3a-144">S/MIME を使用するには、受信者ごとにファイルに公開鍵を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-144">To use S/MIME, you must have public keys on file for each recipient.</span></span> <span data-ttu-id="d4c3a-145">受信者は独自の秘密キーを維持し、保護する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-145">Recipients have to maintain their own private keys, which must remain secure.</span></span> <span data-ttu-id="d4c3a-146">受信者の秘密キーが危険にさらされた場合、受信者は新しい秘密キーを取得し、すべての潜在的な送信者に公開キーを再配布する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-146">If a recipient’s private keys are compromised, the recipient needs to get a new private key and redistribute public keys to all potential senders.</span></span>|
|<span data-ttu-id="d4c3a-147">この機能について</span><span class="sxs-lookup"><span data-stu-id="d4c3a-147">What does it do?</span></span>|<span data-ttu-id="d4c3a-148">OME:</span><span class="sxs-lookup"><span data-stu-id="d4c3a-148">Legacy OME</span></span> <br/> <span data-ttu-id="d4c3a-149">内部または外部の受信者に送信されたメッセージを暗号化します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-149">Encrypts messages sent to internal or external recipients.</span></span> <br/>  <span data-ttu-id="d4c3a-p109">ユーザーは Outlook.com、Yahoo! Mail、および Gmail を含むすべての電子メール アドレスに暗号化されたメッセージを送信できます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-p109">Allows users to send encrypted messages to any email address, including Outlook.com, Yahoo! Mail, and Gmail.</span></span> <br/>  <span data-ttu-id="d4c3a-152">管理者であれば、組織のブランドを反映するように電子メール表示ポータルをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-152">Allows you, as an admin, to customize the email viewing portal to reflect your organization’s brand.</span></span> <br/> <span data-ttu-id="d4c3a-153">Microsoft がキーを安全に管理および格納するため、ユーザーがそうする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-153">Microsoft securely manages and stores the keys, so you don’t have to.</span></span> <br/> <span data-ttu-id="d4c3a-154">暗号化されたメッセージ (HTML 添付ファイルとして送信済み) をブラウザーで開くことができる場合は、クライアント側の特別なソフトウェアは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-154">No special client side software is needed as long as the encrypted message (sent as an HTML attachment) can be opened in a browser.</span></span>|<span data-ttu-id="d4c3a-155">IRM:</span><span class="sxs-lookup"><span data-stu-id="d4c3a-155">IRM</span></span> <br/> <span data-ttu-id="d4c3a-156">暗号化と使用制限を利用し、電子メールのメッセージと添付ファイルをオンラインとオフラインで保護します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-156">Uses encryption and usage restrictions to provide online and offline protection for email messages and attachments.</span></span> <br/> <span data-ttu-id="d4c3a-157">管理者には、自動的に IRM を適用してメッセージを選択するためのトランスポート ルールまたは Outlook 保護ルールを設定する権限が付与されます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-157">Gives you, as an admin, the ability to set up transport rules or Outlook protection rules to automatically apply IRM to select messages.</span></span> <br/> <span data-ttu-id="d4c3a-158">ユーザーは Outlook または Outlook on the web (旧称: Outlook Web App) で手動でテンプレートを適用できます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-158">Lets users manually apply templates in Outlook or Outlook on the web (formerly known as Outlook Web App).</span></span>|<span data-ttu-id="d4c3a-159">S/MIME は、デジタル署名による送信者の認証および暗号化によるメッセージの機密性を処理します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-159">S/MIME addresses sender authentication with digital signatures, and message confidentiality with encryption.</span></span>|
|<span data-ttu-id="d4c3a-160">暗号化オプションの限界</span><span class="sxs-lookup"><span data-stu-id="d4c3a-160">What does it not do?</span></span>|<span data-ttu-id="d4c3a-161">OME では、メッセージに利用制限を適用できません。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-161">OME doesn’t let you apply usage restrictions to messages.</span></span> <span data-ttu-id="d4c3a-162">たとえば、受信者が暗号化メッセージを転送したり印刷したりするのを制限することはできません。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-162">For example, you can’t use it to stop a recipient from forwarding or printing an encrypted message.</span></span>|<span data-ttu-id="d4c3a-163">一部のアプリケーションでは、すべてのデバイスで IRM 電子メールをサポートするわけではないかもしれません。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-163">Some applications may not support IRM emails on all devices.</span></span> <span data-ttu-id="d4c3a-164">以上の製品と IRM メールに対応しているその他の製品に関する詳細については、「[クライアント デバイスの機能](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-164">For more information about these and other products that support IRM email, see [Client device capabilitieshttps://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities).</span></span>|<span data-ttu-id="d4c3a-165">S/MIME では、マルウェア、スパム、およびポリシーについて、暗号化されたメッセージをスキャンできません。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-165">S/MIME doesn’t allow encrypted messages to be scanned for malware, spam, or policies.</span></span>|
|<span data-ttu-id="d4c3a-166">推奨事項とシナリオ例</span><span class="sxs-lookup"><span data-stu-id="d4c3a-166">Recommendations and example scenarios</span></span>|<span data-ttu-id="d4c3a-167">顧客であろうと他の会社であろうと、組織外のユーザーに機密のビジネス情報を送信する場合は、OME を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-167">We recommend using OME  when you want to send sensitive business information to people outside your organization, whether they’re consumers or other businesses.</span></span> <span data-ttu-id="d4c3a-168">例:</span><span class="sxs-lookup"><span data-stu-id="d4c3a-168">For example:</span></span>  <br/>  <span data-ttu-id="d4c3a-169">顧客にクレジット カード請求書を送信する銀行員</span><span class="sxs-lookup"><span data-stu-id="d4c3a-169">A bank employee sending credit card statements to customers</span></span>  <br/>  <span data-ttu-id="d4c3a-170">患者に医療記録を送信する診療所</span><span class="sxs-lookup"><span data-stu-id="d4c3a-170">A doctor’s office sending medical records to a patient</span></span>  <br/>  <span data-ttu-id="d4c3a-171">他の弁護士に法的な機密情報を送信する弁護士</span><span class="sxs-lookup"><span data-stu-id="d4c3a-171">An attorney sending confidential legal information to another attorney</span></span>|<span data-ttu-id="d4c3a-p113">使用制限と暗号化の両方を適用する場合は、IRM を使用することをお勧めします。例:</span><span class="sxs-lookup"><span data-stu-id="d4c3a-p113">We recommend using IRM when you want to apply usage restrictions as well as encryption. For example:</span></span>  <br/>  <span data-ttu-id="d4c3a-174">新しい製品に関する機密情報の詳細をチームに送信するマネージャーが [転送不可] オプションを適用する場合。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-174">A manager sending confidential details to her team about a new product applies the “Do Not Forward” option.</span></span>  <br/>  <span data-ttu-id="d4c3a-175">エグゼクティブが、Office 365 を使用しているパートナーからの添付ファイルを含む重要な提案書を別の会社と共有しなければならず、電子メールと添付ファイルの両方を保護する必要がある場合。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-175">An executive needs to share a bid proposal with another company, which includes an attachment from a partner who is using Office 365, and require both the email and the attachment to be protected.</span></span>|<span data-ttu-id="d4c3a-176">ユーザーの組織または受信者の組織のいずれかが、適切なピアツーピア暗号化を必要とする場合は、S/MIME を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-176">We recommend using S/MIME when either your organization or the recipient’s organization requires true peer-to-peer encryption.</span></span>  <br/>  <span data-ttu-id="d4c3a-177">S/MIME は、次のシナリオで最もよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-177">S/MIME is most commonly used in the following scenarios:</span></span>  <br/>  <span data-ttu-id="d4c3a-178">他の政府機関と通信する政府機関</span><span class="sxs-lookup"><span data-stu-id="d4c3a-178">Government agencies communicating with other government agencies</span></span>  <br/>  <span data-ttu-id="d4c3a-179">政府機関と通信する会社</span><span class="sxs-lookup"><span data-stu-id="d4c3a-179">A business communicating with a government agency</span></span>|
||

## <a name="what-encryption-options-are-available-for-my-office-365-subscription"></a><span data-ttu-id="d4c3a-180">使用中の Office 365 サブスクリプションでは、どの暗号化オプションを利用できますか?</span><span class="sxs-lookup"><span data-stu-id="d4c3a-180">What encryption options are available for my Office 365 subscription?</span></span>

<span data-ttu-id="d4c3a-181">Office 365 サブスクリプションの電子メール暗号化オプションについては、「[Exchange Online サービスの説明](https://technet.microsoft.com/ja-JP/library/exchange-online-service-description.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-181">For information about email encryption options for your Office 365 subscription see the [Exchange Online service descriptionhttps://technet.microsoft.com/ja-JP/library/exchange-online-service-description.aspx](https://technet.microsoft.com/ja-JP/library/exchange-online-service-description.aspx).</span></span> <span data-ttu-id="d4c3a-182">ここでは、次の暗号化の機能に関する情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-182">Here, you can find information about the following encryption features:</span></span>
  
- <span data-ttu-id="d4c3a-183">Azure RMS、IRM 機能と OME の両方を含む</span><span class="sxs-lookup"><span data-stu-id="d4c3a-183">Azure RMS, including both IRM capabilities and OME</span></span>

- <span data-ttu-id="d4c3a-184">S/MIME</span><span class="sxs-lookup"><span data-stu-id="d4c3a-184">S/MIME</span></span>

- <span data-ttu-id="d4c3a-185">TLS</span><span class="sxs-lookup"><span data-stu-id="d4c3a-185">TLS</span></span>

- <span data-ttu-id="d4c3a-186">保存中のデータの暗号化 (BitLocker を使用)</span><span class="sxs-lookup"><span data-stu-id="d4c3a-186">Encryption of data at rest (through BitLocker)</span></span>

<span data-ttu-id="d4c3a-187">Office 365 で、PGP (Pretty Good Privacy) などのサードパーティ製の暗号化ツールを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-187">You can also use third-party encryption tools with Office 365, for example, PGP (Pretty Good Privacy).</span></span> <span data-ttu-id="d4c3a-188">Office 365 は PGP/MIME をサポートしていません。 PGP で暗号化されたメールを送受信する場合にのみ PGP/Inline を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-188">Office 365 does not support PGP/MIME and you can only use PGP/Inline to send and receive PGP-encrypted emails.</span></span>

## <a name="what-about-encryption-for-data-at-rest"></a><span data-ttu-id="d4c3a-189">保存中のデータの暗号化について</span><span class="sxs-lookup"><span data-stu-id="d4c3a-189">What about encryption for data at rest?</span></span>

<span data-ttu-id="d4c3a-190">"保存データ" とは、アクティブに送信されている過程にはないデータです。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-190">“Data at rest” refers to data that isn’t actively in transit.</span></span> <span data-ttu-id="d4c3a-191">Office 365 では、保存中の電子メール データは BitLocker ドライブ暗号化を使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-191">In Office 365, email data at rest is encrypted using BitLocker Drive Encryption.</span></span> <span data-ttu-id="d4c3a-192">BitLocker は、Office 365 データセンター内のハード ドライブを暗号化し、権限のないアクセスに対する保護を強化します。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-192">BitLocker encrypts the hard drives in Office 365 datacenters to provide enhanced protection against unauthorized access.</span></span> <span data-ttu-id="d4c3a-193">詳細については、「[BitLocker の概要](https://go.microsoft.com/fwlink/p/?LinkId=394737)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-193">To learn more, see [Overview of SharePoint Framework Extensions](https://go.microsoft.com/fwlink/p/?LinkId=394737).</span></span>
  
## <a name="more-information-about-email-encryption-options-in-office-365"></a><span data-ttu-id="d4c3a-194">Office 365 の電子メール暗号化オプションの詳細</span><span class="sxs-lookup"><span data-stu-id="d4c3a-194">More information about email encryption options in Office 365</span></span>

<span data-ttu-id="d4c3a-195">この記事の電子メール暗号化オプションと TLS の詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4c3a-195">For more information about the email encryption options in this article as well as TLS, see these articles:</span></span>
  
<span data-ttu-id="d4c3a-196">**OME**</span><span class="sxs-lookup"><span data-stu-id="d4c3a-196">**OME**</span></span>
  
[<span data-ttu-id="d4c3a-197">Office 365 Message Encryption (OME)</span><span class="sxs-lookup"><span data-stu-id="d4c3a-197">Office 365 Message Encryption (OME)</span></span>](ome.md)
  
<span data-ttu-id="d4c3a-198">**IRM**</span><span class="sxs-lookup"><span data-stu-id="d4c3a-198">**IRM**</span></span>
  
[<span data-ttu-id="d4c3a-199">Exchange Online での Information Rights Management</span><span class="sxs-lookup"><span data-stu-id="d4c3a-199">Information Rights Management in Exchange Online</span></span>](https://technet.microsoft.com/ja-JP/library/jj983436%28v=exchg.150%29.aspx)
  
[<span data-ttu-id="d4c3a-200">Azure Active Directory Rights Management の概要</span><span class="sxs-lookup"><span data-stu-id="d4c3a-200">What is Azure Rights Management?</span></span>](https://technet.microsoft.com/library/jj585026)
  
<span data-ttu-id="d4c3a-201">**S/MIME**</span><span class="sxs-lookup"><span data-stu-id="d4c3a-201">**S/MIME**</span></span>
  
[<span data-ttu-id="d4c3a-202">S/MIME によるメッセージの署名と暗号化</span><span class="sxs-lookup"><span data-stu-id="d4c3a-202">S/MIME for message signing and encryption</span></span>](https://technet.microsoft.com/library/dn626158)
  
[<span data-ttu-id="d4c3a-203">S/MIME について</span><span class="sxs-lookup"><span data-stu-id="d4c3a-203">Understanding S/MIME</span></span>](https://technet.microsoft.com/library/aa995740%28v=exchg.65%29.aspx)
  
[<span data-ttu-id="d4c3a-204">公開キー暗号について</span><span class="sxs-lookup"><span data-stu-id="d4c3a-204">Understanding Public Key Cryptography</span></span>](https://technet.microsoft.com/library/aa998077%28v=exchg.65%29.aspx)
  
<span data-ttu-id="d4c3a-205">**TLS**</span><span class="sxs-lookup"><span data-stu-id="d4c3a-205">**tls**</span></span>
  
[<span data-ttu-id="d4c3a-206">Office 365 でコネクタを使用してメール フローを構成する</span><span class="sxs-lookup"><span data-stu-id="d4c3a-206">Configure mail flow using connectors in Office 365</span></span>](https://technet.microsoft.com/ja-JP/library/jj723138%28v=exchg.150%29.aspx)