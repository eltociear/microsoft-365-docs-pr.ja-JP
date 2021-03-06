---
title: 高度なメッセージ暗号化
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 10/16/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: 高度なメッセージ暗号化では、管理者が保護されたメッセージをより多く実行できるようにすることで、組織がコンプライアンスの義務を満たすことができます。
ms.openlocfilehash: 0e28bd283b6a7d1666d5db9b71040d2f377adffe
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43626895"
---
# <a name="advanced-message-encryption"></a>高度なメッセージ暗号化

Office 365 の高度なメッセージの暗号化は、 [microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home)、Office 365 E5、Microsoft 365 E5 (非営利団体の価格)、Office 365 Enterprise E5 (非営利スタッフの価格)、office の365教育用 A5 に含まれています。 Office 365 Advanced Message Encryption を含まないサブスクリプションが組織にある場合は、microsoft 365 E3 の Microsoft 365 E5 コンプライアンス SKU アドオンを使用して購入できます。 microsoft 365 E3 (非営利団体の価格)、または Office 365 Advanced コンプライアンス SKU アドオン for Microsoft 365 E3、Microsoft 365 E3 (非営利スタッフの価格)、Office の 365 Sku、または microsoft の microsoft 365 E5/A5 Information Protection and ガバナンス SKU アドオン Microsoft 365 A3/E3。

高度なメッセージ暗号化は、外部の受信者に対してより柔軟な制御と暗号化された電子メールへのアクセスを必要とするコンプライアンス義務を満たすためにお客様を支援します Office 365 の高度なメッセージ暗号化を使用すると、自動ポリシーにより、組織の外部で共有される機密メールを制御することができます。 これらのポリシーは、PII、財務、健康 Id などの機密情報の種類を識別するために構成したり、保護を強化するためにキーワードを使用したりすることができます。 ポリシーを構成したら、ポリシーをカスタムのブランド化された電子メールテンプレートとペアにして、ポリシーに適合する電子メールの追加の制御の有効期限を追加します。 また、管理者は、メールへのアクセスをいつでも取り消すことにより、セキュリティで保護された web ポータルを介して外部からアクセスされる暗号化メールを制御することもできます。

外部の受信者に送信される電子メールの有効期限は、失効日と設定のみを行うことができます。

## <a name="get-started-with-office-365-advanced-message-encryption"></a>Office 365 Advanced Message Encryption の使用を開始する

次の記事では、高度なメッセージ暗号化の設定方法と使用方法について説明します。

組織には、Office 365 Advanced Message Encryption を含むサブスクリプションが必要です。 サポートされているサブスクリプションの詳細については、「[メッセージポリシーとコンプライアンスサービスの説明](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)」を参照してください。

Office 365 メッセージの暗号化が既にセットアップされていない場合は、「 [365 office の新しいメッセージの暗号化機能をセットアップ](set-up-new-message-encryption-capabilities.md)する」を参照してください。

高度なメッセージ暗号化では、単一のブランド化テンプレートに制限されません。 代わりに、複数のブランド化テンプレートを作成して使用することができます。 詳細については、「[組織のブランドを暗号化されたメッセージに追加する](add-your-organization-brand-to-encrypted-messages.md)」を参照してください。

[Office 365 Advanced Message Encryption で暗号化された電子メールの有効期限日を設定](ome-advanced-expiration.md)します。 セキュリティで保護された web ポータルから暗号化された電子メールへのアクセスを期限切れにすることによって保護を強化する自動ポリシーを使用して、組織外で共有する機密メールを制御

[Office 365 の高度なメッセージ暗号化によって暗号化された電子メールを取り消し](revoke-ome-encrypted-mail.md)ます。 セキュリティで保護された web ポータルから暗号化された電子メールへのアクセスを取り消すことにより、組織の外部で共有される機密メールを制御し、保護を強化します。  

Office 365 の高度なメッセージ暗号化では、カスタムブランド設定テンプレートを適用するたびに、Microsoft はテンプレートを適用するメールフロールールに適合するラッパーを電子メールに適用します。 メッセージを失効させることができます。また、ユーザーがポータル経由で受信するメッセージに有効期限日を適用することもできます。 つまり、カスタムブランド化テンプレートが適用されている電子メール。 詳細と例については、「すべての[外部の受信者が OME ポータルを使用して暗号化されたメールを読み取るようにする](manage-office-365-message-encryption.md#ensure-all-external-recipients-use-the-ome-portal-to-read-encrypted-mail)」のガイダンスを参照してください。
