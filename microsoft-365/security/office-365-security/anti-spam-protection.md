---
title: スパム対策保護
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
ms.collection:
- M365-security-compliance
description: Exchange Online および Microsoft 365 でスパムを防止するのに役立つスパム対策設定とフィルターについて説明します。 Microsoft 365 でスパムを過剰に取得していますか? スパムフィルターとスパム対策の設定はカスタマイズできます。
ms.openlocfilehash: 3bb1c81af0061cc20b4c7bb2a963c0d06b7914e3
ms.sourcegitcommit: d4d082292dc711a579fe925ad989ea54ec2e27f4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2020
ms.locfileid: "43708573"
---
# <a name="anti-spam-protection-in-microsoft-365"></a>Microsoft 365 でのスパム対策保護

> [!NOTE]
> このトピックは、Microsoft 365 管理者を対象としています。 エンドユーザーのトピックについては、「[迷惑メールフィルターの概要](https://support.Microsoft.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)」と「[迷惑メールおよびフィッシングについ](https://support.Microsoft.com/article/86c1d76f-4d5a-4967-9647-35665dc17c31)て」を参照してください。

Exchange Online または exchange online メールボックスを使用しないスタンドアロンの Exchange Online Protection (EOP) のお客様のために、メールボックスが含まれる Microsoft 365 顧客は、電子メールメッセージが EOP によってスパム (迷惑メール) から自動的に保護されます。

Microsoft のメールの安全性ロードマップには、他に例を見ない製品間のアプローチが含まれます。 EOP のスパム対策およびフィッシング対策テクノロジは、電子メールプラットフォーム全体に適用され、ユーザーに最新のスパム対策およびフィッシング対策ツールと、ネットワーク全体での技術革新を提供します。 EOP の目標は、包括的で使用可能なメール サービスを提供し、迷惑メール、詐欺目的のメールの脅威 (フィッシング)、マルウェアを検出し、それらからユーザーを保護することです。

メールの使用が増えるにつれ、メールの不正使用も増えました。 監視されていない迷惑メールによって、受信トレイとネットワークに余分な負荷が掛かり、ユーザー満足度に影響を及ぼし、正当なメール通信の効果が阻害されます。 これが Microsoft がスパム対策テクノロジへの投資を継続する理由です。 簡単に言えば、迷惑メールを格納して、フィルター処理することから始めます。

## <a name="anti-spam-technologies-in-eop"></a>EOP のスパム対策テクノロジ

迷惑メールを減らすために、EOP には、独自のスパムフィルタリングテクノロジを使用して正当な電子メールから迷惑メールを識別し、分離する迷惑メール保護が含まれています。 EOP スパムフィルターは、既知のスパムおよびフィッシングの脅威から、およびコンシューマープラットフォームの Outlook.com からのユーザーフィードバックを学習します。 迷惑メール分類プログラムの EOP ユーザーからの継続的なフィードバックにより、EOP テクノロジが絶えずトレーニングおよび改善されるようにしています。

EOP のスパム対策設定は、次のテクノロジで構成されています。

- **接続フィルター**: 受信電子メールの送信元サーバーを、Ip 許可一覧、Ip 禁止一覧、および*セーフリスト*(Microsoft が管理する信頼できる差出人の動的で、編集不能な一覧) を介して早い段階で特定します。 これらの設定は、接続フィルターポリシーで構成します。 詳細について[は、「Configure connection filtering In Microsoft 365」を](configure-the-connection-filter-policy.md)参照してください。

  > [!NOTE]
  > スプーフィングインテリジェンスは、接続フィルターを使用して、電子メールドメインをスプーフィングしている送信者の許可とブロックの一覧を作成します。 詳細については、「 [Microsoft 365 のスプーフィングインテリジェンスの詳細](learn-about-spoof-intelligence.md)」を参照してください。

- **スパムフィルター処理 (コンテンツフィルター)**: EOP は、スパムフィルター verdicts**スパム**、**信頼度の高いスパム**、**バルクメール**、**フィッシング電子**メール、および**信頼度の高いフィッシング電子メール**を使用してメッセージを分類します。 これらの verdicts に基づいて実行するアクションを構成することができ、配信される代わりに検疫されたメッセージのエンドユーザー通知オプションを構成できます。 詳細については、「 [Microsoft 365 でスパム対策ポリシーを構成する](configure-your-spam-filter-policies.md)」を参照してください。

  > [!NOTE]
  > 既定では、スパムフィルターは、受信者の迷惑メールフォルダーにスパムとしてマークされたメッセージを送信するように構成されています。 ただし、EOP がオンプレミスの Exchange メールボックスを保護するハイブリッド環境では、メッセージに追加される EOP スパムヘッダーを認識するように、社内 Exchange 組織内の2つのメールフロールール (トランスポートルールとも呼ばれます) を構成する必要があります。 詳細については、「[迷惑メール フォルダーにスパムを配信するようにスタンドアロン EOP を構成する](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)」を参照してください。

- **送信スパムフィルター**: EOP は、送信メッセージのコンテンツまたは送信メッセージの制限を超えて、ユーザーがスパムを送信しないようにすることも確認します。 詳細については、「 [Microsoft 365 で送信スパムフィルターを構成する](configure-the-outbound-spam-policy.md)」を参照してください。

- **スプーフィングインテリジェンス**: 詳細については、「 [Microsoft 365 のスプーフィングインテリジェンスの詳細](learn-about-spoof-intelligence.md)」を参照してください。

## <a name="manage-errors-in-spam-filtering"></a>スパムフィルター処理でエラーを管理する

適切なメッセージをスパム (誤検知とも呼ばれます) として識別したり、スパムを受信トレイに配信することができます。 次のセクションの推奨事項を使用して、発生したことを確認し、今後の事態を防ぐことができます。

次に、どちらのシナリオにも当てはまるベストプラクティスをいくつか示します。

- 誤分類メッセージを常に Microsoft に送信します。 詳細については、「[メッセージとファイルを Microsoft に報告する](report-junk-email-messages-to-microsoft.md)」を参照してください。

- **スパム対策メッセージヘッダーを調べる**: これらの値は、メッセージがスパムとしてマークされた理由、またはスパムフィルター処理をスキップした理由を示します。 詳細については、「[スパム対策メッセージ ヘッダー](anti-spam-message-headers.md)」を参照してください。

- **MX レコードのポイントを microsoft 365 に**設定します。 EOP が最適な保護を提供するためには、まず microsoft 365 に電子メールを配信することをお勧めします。 手順については、「 [Microsoft 365 の任意の dns ホスティングプロバイダーで dns レコードを作成する](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider)」を参照してください。

  MX レコードが他の場所 (たとえば、サードパーティのスパム対策ソリューションまたはアプライアンス) を指している場合、EOP が正確なスパムフィルタリングを提供するのは困難です。 このシナリオでは、コネクタ (_スキップリスト_とも呼ばれます) の拡張フィルター処理を構成する必要があります。 手順については、「 [Exchange Online のコネクタの拡張フィルター処理](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors)」を参照してください。

- **電子メール認証の使用**: 電子メールドメインを所有している場合は、そのドメイン内の送信者からのメッセージが正当であることを確認するために DNS を使用できます。 EOP でスパムや不要なスプーフィングを防止するために、次のすべての電子メール認証方法を使用します。

  - **SPF**: Sender Policy Framework は、送信側ドメインの所有者に対してメッセージの送信元 IP アドレスを確認します。 SPF の簡単な説明と、すぐに構成する方法については、「[スプーフィングを防止するために spf をセットアップする](set-up-spf-in-office-365-to-help-prevent-spoofing.md)」を参照してください。 Microsoft 365 が SPF をどのように使用しているか、またはハイブリッド展開のようなトラブルシューティングや標準的でない展開についての詳細については、 [microsoft 365 が送信者ポリシーフレームワーク (SPF) を使用してスプーフィングを防止する方法](how-office-365-uses-spf-to-prevent-spoofing.md)から始めます。

  - **Dkim**: domainkeys が識別されたメールは、自分のドメインから送信されたメッセージのメッセージヘッダーにデジタル署名を追加します。 詳細については、「 [Microsoft 365 でカスタムドメインから送信される送信電子メールを検証するために DKIM を使用する](use-dkim-to-validate-outbound-email.md)」を参照してください。

  - **DMARC**: ドメインベースのメッセージの認証、レポート、および準拠宛先メールシステムは、SPF または dkim チェックに失敗したメッセージに対する処理を決定し、電子メールパートナーに対して別のレベルの信頼を提供します。 詳細については、「 [Microsoft 365 で電子メールを検証するために DMARC を使用する](use-dmarc-to-validate-email.md)」を参照してください。

- **バルクメール設定の確認**: スパム対策ポリシーで構成する一括準拠レベル (BCL) しきい値は、バルクメール (_灰色のメール_とも呼ばれる) がスパムとしてマークされているかどうかを決定します。 既定でオンになっている_MarkAsSpamBulkMail_の PowerShell のみの設定は、結果にも影響します。 詳細については、「 [Microsoft 365 でスパム対策ポリシーを構成する](configure-your-spam-filter-policies.md)」を参照してください。

### <a name="prevent-the-delivery-of-spam-to-the-inbox"></a>受信トレイへのスパムの配信を禁止する

- **組織の設定を確認**します。メッセージがスパムフィルターをスキップできるようにする設定 (たとえば、スパム対策ポリシーの [許可されたドメイン] の一覧に独自のドメインを追加する場合など) に注目してください。 推奨される設定については、「 [EOP And Microsoft 365 ATP security](recommended-settings-for-eop-and-office365-atp.md) 」および「 [safe Sender リストを作成](create-safe-sender-lists-in-office-365.md)する」の推奨設定を参照してください。

- **ユーザーのメールボックスで迷惑メールルールが有効になっていることを確認**します。既定で有効になっていますが、無効にすると、迷惑メールとしてマークされたメッセージを [迷惑メール] フォルダーに移動することはできません。 詳細については、「 [Microsoft 365 の「Exchange Online メールボックスの迷惑メール設定を構成する](configure-junk-email-settings-on-exo-mailboxes.md)」を参照してください。

- **利用可能な受信拒否リストを使用する**: 詳細については、「[ブロックする送信者リストを作成](create-block-sender-lists-in-office-365.md)する」を参照してください。

- **バルクメールからの登録解除**ユーザーがサインアップしたもの (ニュースレター、製品アナウンスなど) についてのメッセージで、よく知られたソースからの登録解除リンクが含まれている場合は、購読を中止するように依頼することを検討してください。

- **スタンドアロン EOP: EOP スパムフィルタリング verdicts のオンプレミスの exchange でのメールフロールールの作成**: EOP がオンプレミスの exchange メールボックスを保護するために、オンプレミス exchange のメールフロールール (トランスポートルールとも呼ばれる) を構成して、迷惑メールルールがメッセージを迷惑メールフォルダーに移動できるようにする必要があります。 詳細については、「[迷惑メール フォルダーにスパムを配信するようにスタンドアロン EOP を構成する](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)」を参照してください。

### <a name="prevent-good-email-from-being-identified-as-spam"></a>適切な電子メールがスパムと識別されないようにする

誤検知を防止するために、次の手順を実行することができます。

- **ユーザーの Outlook 迷惑メールフィルターの設定を確認**します。

  - **Outlook 迷惑メールフィルターが無効になっていることを確認**する: Outlook の迷惑メールフィルターが既定値の [**自動フィルター処理なし**] に設定されている場合、outlook は massages をスパムとして分類しようとしません。  Outlook の迷惑メールフィルターでは、**低**または**高**に設定されている場合、迷惑メールフォルダーにスパムを識別して移動するための独自の SmartScreen フィルターテクノロジを使用しているため、誤検知を受けることができます。 Microsoft は、Exchange および Outlook 11 月2016日に、SmartScreen フィルターのスパム定義の更新プログラムの生成を停止しました。 既存の SmartScreen スパム定義は残されていましたが、その有効性は時間とともに低下する可能性があります。

  - [ **Outlook のセーフリストのみ] 設定が無効になっていることを確認し**ます。この設定を有効にすると、ユーザーの差出人セーフリストまたは宛先セーフリストに含まれる送信者からのメッセージのみが受信トレイに配信されます。他のすべてのユーザーからのメールは、自動的に [迷惑メール] フォルダーに移動されます。

  これらの設定の詳細については、「 [Microsoft 365 の「Exchange Online メールボックスの迷惑メール設定を構成する](configure-junk-email-settings-on-exo-mailboxes.md)」を参照してください。

- **利用可能な差出人セーフリストを使用**します。詳細については、「365.md」を参照してください。詳細については、「作成-安全な送信者リスト」 (を参照してください。

- 「Exchange Online サービスの説明」の「[受信および送信の制限](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#receiving-and-sending-limits)」で説明されているように **、ユーザーが送信と受信の制限内にあることを確認**します。

- **スタンドアロン EOP: ディレクトリ同期を使用**する: スタンドアロン EOP を使用してオンプレミスの Exchange 組織を保護する場合は、ディレクトリ同期を使用してユーザー設定をサービスと同期させる必要があります。 こうすることで、ユーザーの信頼できる差出人のリストが EOP に適用されます。 詳しくは、「[ディレクトリ同期を使用してメール ユーザーを管理する](manage-mail-users-in-eop.md#use-directory-synchronization-to-manage-mail-users)」 を参照してください。

## <a name="anti-spam-legislation"></a>スパム対策法

Microsoft では、新しいテクノロジと自主規制の開発には効果的な政府の政策と法的枠組みによるサポートが必要であると考えています。 迷惑メールが世界中にまん延するにつれ、商用メールを規制する動きが多くの立法機関で活発化してきました。 現在、多くの国でスパム対策法が適用されています。 米国では、迷惑メールに対応した連邦法と州法が制定されており、この補完的なアプローチによって迷惑メールを減少させ、正規の電子商取引を促進しています。 CAN-SPAM 法では、詐欺メールや偽装メールを阻止するためのさまざまなツールが提供されています。