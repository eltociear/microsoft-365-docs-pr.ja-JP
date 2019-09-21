---
title: チュートリアルのスプーフィングインテリジェンスの洞察
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 7/30/2018
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 59a3ecaf-15ed-483b-b824-d98961d88bdd
ms.collection:
- M365-security-compliance
description: 新しいスプーフィングインテリジェンスの理解のしくみを参照してください。
ms.openlocfilehash: 652dde07d615a4eef98074fb8d2b5c676f65d633
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2019
ms.locfileid: "37086553"
---
# <a name="walkthrough-spoof-intelligence-insight"></a>チュートリアル: スプーフィングインテリジェンスの洞察

スプーフィングインテリジェンスによる洞察を使用して、認証されていない電子メールを正当に送信している送信者をすばやく判断できます。 スプーフィングされたメッセージの送信を許可することにより、ユーザーが誤検知を行うリスクを軽減することができます。
  
さらに、スプーフィングインテリジェンスモニターを使用して、許可されたドメインペアを管理することによって、セキュリティの追加の層を提供したり、安全でないメッセージが組織に到着しないようにしたりすることもできます。
  
職場または学校のアカウントに Office 365 の&amp;グローバル管理者、セキュリティ管理者、またはセキュリティ閲覧者のアクセス許可が付与されている場合は、セキュリティコンプライアンスセンターでスプーフィングインテリジェンスに関する洞察を得ることができます。 詳細については、「 [Office 365 セキュリティ&amp;コンプライアンスセンターのアクセス許可](permissions-in-the-security-and-compliance-center.md)」を参照してください。
  
[Office 365 セキュリティ&amp;コンプライアンスセンターのレポートと洞察](reports-and-insights-in-security-and-compliance.md)を初めて使用する場合は、ダッシュボードから洞察や推奨されるアクションに簡単にアクセスする方法を確認することができます。
  
セキュリティ&amp; /コンプライアンスセンターでは、複数のダッシュボードからスプーフィングインテリジェンスの洞察を確認できます。 どのダッシュボードを使用しているかに関係なく、洞察は同じ情報を提供し、同じタスクをすばやく実行することができます。
  
これは、セキュリティ&amp;コンプライアンスセンターのいくつかのチュートリアルの1つです。 レポートと分析情報の移動については、「関連項目」セクションのチュートリアルを参照してください。
  
## <a name="getting-to-the-spoof-intelligence-insight-in-the-security-amp-compliance-center"></a>セキュリティ&amp; /コンプライアンスセンターのスプーフィングインテリジェンスについての理解を得る

1. 開始するに[は、セキュリティ&amp;コンプライアンスセンターに移動](../../compliance/go-to-the-securitycompliance-center.md)する必要があります。
    
2. セキュリティ&amp; /コンプライアンスセンターで、[**脅威管理** \> ] ダッシュボードに移動し**ます。**
    
3. [ **Insights** ] 行で、スプーフィングインテリジェンスに関する洞察を探します。 スプーフィングインテリジェンスを有効にしている場合、この洞察には**過去30日間の認証に失敗したスプーフィングドメインの**資格が与えられます。 スプーフィングによる保護を有効にしていない場合は、[**スプーフィング保護を有効**にする] のタイトルを使用して、これを実行するように求めるメッセージが表示されます。 
    
## <a name="about-the-insight-on-the-dashboard"></a>ダッシュボードの詳細について

ダッシュボードの洞察には、このような情報が表示されます。
  
![スプーフィングインテリジェンスの洞察のスクリーンショット](../media/28aeabac-c1a1-4d16-9fbe-14996f742a9a.png)
  
この洞察には、次の2つのモードがあります。
  
 **洞察モード**。 いずれかのスプーフィングポリシーを有効にしている場合は、過去30日間のスプーフィングインテリジェンス機能によって影響を受けたメールの数が洞察によって示されます。 
  
 **If モードについ**て スプーフィングポリシーが有効になっていない場合は、過去30日間のスプーフィングインテリジェンス機能によって影響を*受けるメールの数が洞察*に示されています。 
  
どちらの方法でも、洞察に表示される偽装ドメインは2つのカテゴリに分かれています。疑わしいドメインの組と、不審でないドメインのペア。 これらのカテゴリは、確認のために3つの異なるバケットにさらに細分化されています。 
  
*ドメインペア*は、"From:" アドレスと送信元インフラストラクチャの組み合わせです。 
  
- "差出人" アドレスは、メールアプリケーションによって差出人アドレスとして表示されるアドレスです。 このアドレスは電子メールの作成者を識別します。 つまり、メッセージを書いた個人またはシステムのメールボックスになります。 これは、 5322.From アドレスとも呼ばれます。
    
- 送信元のインフラストラクチャ (送信者) は、送信元の IP アドレスの PTR レコードの組織ドメインです。 送信元の IP アドレスに PTR レコードがない場合、送信元の IP アドレスは、CIDR 表記法 (/24) で255.255.255.0 サブネットマスクを使用して識別されます。 たとえば、IP アドレスが192.168.100.100 の場合、送信者の完全な IP アドレスは 192.168.100.100/24 です。
    
 **疑わしいドメインペア**は次のとおりです。 
  
- **信頼度の高いスプーフィング**。 Office 365 は、履歴送信パターンおよびドメインの評価スコアに基づいて、これらのドメインが疑わしいという強力な信号を受信しました。 Office 365 は、ドメインがスプーフィングされており、これらのドメインから送信されたメッセージが正当ではない可能性が高いことを確信しています。 
    
- **適度に信頼度**の高いスプーフィング。 Office 365 は、履歴送信パターンおよびドメインの評価スコアに基づいて、これらのドメインが疑わしいという、中程度の信号を受信しました。 Office 365 は、ドメインがスプーフィングされており、これらのドメインから送信されたメッセージが正当であることを適度に確信しています。 このバケットは、信頼度の高いスプーフィングバケットよりも誤検知 (FPs) を含む可能性が高くなります。 
    
 **不審ではないドメインのペアに**は、 **rescued スプーフィング**が含まれます。 Rescued スプーフィングは、明示的な認証チェック ( [SPF](https://docs.microsoft.com/office365/SecurityCompliance/how-office-365-uses-spf-to-prevent-spoofing)、 [dkim](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)、 [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)) に失敗したものの、拡張された認証チェックに合格したドメインです。 そのため、Office 365 では、ユーザーの代わりにメールが rescued され、メールに対するスプーフィング対策アクションは行われませんでした。 
  
## <a name="view-detailed-information-about-suspicious-domain-pairs-from-the-spoof-intelligence-insight"></a>スプーフィングインテリジェンスの洞察から、疑わしいドメインペアに関する詳細情報を表示する

1. スプーフィングインテリジェンスの洞察で、いずれかのドメインペア (high、中、または rescued) をクリックします。
  
[**スプーフィングインテリジェンスの洞察**] ページに、認証されていないメールを組織に送信している送信者の一覧が表示されます。 このページの情報は、スプーフィングされたメッセージが承認されているかどうかを判断したり、さらにアクションを実行する必要があるかどうかを判断するのに役立つ。 メッセージ数、スプーフィングが最後に検出された日付などによって、情報を並べ替えることができます。 (たとえば、[**メッセージ件数**] や [**最後に表示**] など) をクリックします。 
    
2. このテーブル内の項目を選択すると、そのドメインのペアに関する豊富な情報が含まれる詳細ウィンドウが表示されます。これには、これをキャッチした理由、ドメインの概要、送信者に関する WhoIs データ、および同じ送信者からのテナントに表示された類似の電子メールなどがあります。 ここから、ドメインペアを**Allowedtospoof** safe sender リストから追加または削除することもできます。 
  
![スプーフィングインテリジェンスの詳細情報ウィンドウにあるドメインのスクリーンショット](../media/03ad3e6e-2010-4e8e-b92e-accc8bbebb79.png)
  
## <a name="add-or-remove-a-domain-from-the-allowedtospoof-safe-sender-list"></a>AllowedToSpoof safe 送信者リストにドメインを追加または削除する

ドメインを AllowedToSpoof safe sender リストから追加または削除すると、スプーフィングインテリジェンスの洞察の詳細ウィンドウでドメインペアを確認することができます。 それに応じてトグルを設定するだけです。
  
これにより、偽装されたドメインと送信元インフラストラクチャの一意のドメインペアの組み合わせが変更されます。また、分離されたドメインまたは送信元のインフラストラクチャ全体についても対応しません。 たとえば、次のドメインの組を ' AllowedToSpoof ' 送信者の許可一覧に追加すると、*偽装ドメイン*"gmail.com" と、インフラストラクチャ " *Mx.com"* を*送信*します。そのドメインペアからのメールのみがスプーフィングに許可されます。 "Gmail.com" のスプーフィングを試みる他の送信者、および "tms.mx.com" がスプーフィングしようとしている他のドメインは、スプーフィングインテリジェンスによって引き続き保護されます。 
  
## <a name="related-topics"></a>関連項目

[スプーフィング インテリジェンスの詳細情報](learn-about-spoof-intelligence.md)
  
[Office 365 でのスプーフィング対策保護](anti-spoofing-protection.md)
  
[チュートリアル - ダッシュボードからインサイトへの移動](from-a-dashboard-to-an-insight.md)
  
[チュートリアル - 詳細レポートからインサイトへの移動](from-a-detailed-report-to-an-insight.md)
  
[チュートリアル - インサイトから詳細レポートへの移動](from-an-insight-to-a-detailed-report.md)
  
