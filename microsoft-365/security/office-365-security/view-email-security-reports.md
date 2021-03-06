---
title: 電子メールセキュリティレポートの表示セキュリティ & コンプライアンスセンター、侵害されたユーザー、暗号化、脅威保護の状態、マルウェア検出、上位マルウェア、スパム検出、送受信された電子メール、ユーザーが報告したメッセージ、閲覧レポート、検出、セキュリティデータ、セキュリティ情報
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: 01/16/2020
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
ms.collection:
- M365-security-compliance
description: 組織の電子メールセキュリティレポートを検索して使用する方法について説明します。 電子メールセキュリティレポートは、セキュリティ & コンプライアンスセンターで利用できます。
ms.openlocfilehash: b65dd6479262b97f08e34420d9a88ee2a327a73b
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "43631087"
---
# <a name="view-email-security-reports-in-the-security--compliance-center"></a>セキュリティ/コンプライアンス センターで電子メールのセキュリティ レポートを表示する

[セキュリティ & コンプライアンスセンター](https://protection.office.com)では、Microsoft 365 のスパム対策、マルウェア対策、暗号化機能などの電子メールセキュリティ機能が組織を保護していることを確認するのに役立つさまざまなレポートが提供されています。 [必要なアクセス許可](#what-permissions-are-needed-to-view-these-reports)がある場合は、**レポート** \> **ダッシュボード**にアクセスすることによって、セキュリティ & コンプライアンスセンターでこれらのレポートを表示できます。

![セキュリティ & コンプライアンスセンターのレポートダッシュボード](../../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)

電子メールのセキュリティレポートには、次のようなものがあります。

- [URL の脅威保護レポート](#url-threat-protection-report-new)(**新**機能)
- [侵害されたユーザーレポート](#compromised-users-report)
- [暗号化レポート](#encryption-report)
- [脅威保護の状態レポート](#threat-protection-status-report)
- [マルウェア検出レポート](#malware-detections-report)
- [上位マルウェアレポート](#top-malware-report)
- [[上位送信者および受信者] レポート](#top-senders-and-recipients-report)
- [スプーフィング検出レポート](#spoof-detections-report)
- [スパム検出レポート](#spam-detections-report)
- [送信および受信した電子メールレポート](#sent-and-received-email-report)
- [ユーザーによって報告されたメッセージレポート](#user-reported-messages-report)

## <a name="url-threat-protection-report-new"></a>URL の脅威保護レポート (**新**機能)

次のものを持つすべてのユーザーが URL の脅威保護レポートを利用できます。

- Exchange Online Protection*と*Advanced Threat protection アドオン (プラン 1*または*プラン 2)
- Microsoft 365 E5 サブスクリプション

これは、2つの集計ビューを持つ ' クリック中心 ' レポートです。

1. 最初のビューは、 *url クリック保護アクション*によって指定されます。これは、テナント内のユーザーによる url クリック数の表示、およびクリックの結果を表示することに重点を置いています。 ここをクリックすると、ユーザーが悪意のある web サイトに対する禁止ページをクリックしたことが示されます (これは、安全なリンクポリシー内で管理者によって無効にされる場合があります)。

2. 2番目のビューは *[url] をクリックし*ます。これは、電子メールクライアントや Microsoft Word など、現在安全なリンクをサポートしているさまざまなアプリケーションでクリックされた url の数を示します。 両方の集計ビューのデータは、4時間ごとに更新されます。

URL の脅威保護レポートの詳細表には、テナント内で発生するすべてのクリックがほぼリアルタイムで表示されます。また、*ユーザー名*、 *url*、*ネットワークメッセージ ID* (URL が電子メールからクリックされた場合) などの調査情報や、調査や分析に役立つその他の情報が含まれます。

既定では、このレポートには、安全なリンクによってブロックされた Url からのクリックに関するデータのみが表示されますが、フィルターで [*許可さ*れた url] チェックボックスをオンにすると、すべての url クリックに関する情報を表示することもできます。

このレポートには、[安全なリンク] ポリシーを適用したユーザーからのクリックのデータは含まれません。 [*ユーザーのクリックを追跡*しない] オプションが選択されています。

![アクションの URL の脅威保護レポートの図。](../../media/tp-URLThreatProRpt1.PNG)

## <a name="compromised-users-report"></a>侵害されたユーザーレポート

このレポートは、Exchange Online Protection を使用しているすべてのユーザーが、疑わしいユーザーまたは制限されたユーザーとしてマークされたユーザーアカウント数を示しています。データは、ユーザーアカウントが問題を示しているか、侵害されている可能性がある状態のいずれかを入力します。 侵害されたユーザーレポートによって、不審または制限付きの状態でマークされたアカウントでスパイクや傾向を特定でき、セキュリティとテナントの wellness に関する問題が発生する可能性があります。

![侵害されたユーザーのレポートは、Microsoft 365 に表示されます。](../../media/tp-threatProtectStatRpt-CompromisedUserRpt.png)

## <a name="encryption-report"></a>暗号化レポート

**暗号化レポート**には、組織のポリシーによって、またはエンドユーザーの制御によって暗号化された電子メールメッセージに関する情報が表示されます。 組織のセキュリティチームは、このレポートの情報を使用して、パターンを識別し、機密性の高い電子メールメッセージのポリシーを事前に適用または調整することができます。

このレポートを表示するには、セキュリティ & コンプライアンスセンターで、[**レポート** \> **ダッシュボード** \>の**暗号化レポート**] に移動します。

![暗号化レポート](../../media/encryptionreport-defaultview.png)

最初にレポートを開くと、過去7日間の電子メールメッセージで使用されていた暗号化方法に関するデータが表示されます。 レポートに表示される日付の範囲と詳細を変更するには、画面の右上隅にある [**フィルター** ] をクリックします。

![暗号化レポートのフィルター](../../media/encryptionreport-filters.png)

[**分解**] メニューを使用して、データを暗号化テンプレート (またはメソッド) 別に表示することもできます。

![暗号化方法またはテンプレート](../../media/encryptionreport-breakdownby.png)

また、[**データの表示**] メニューを使用して、上位5人の受信者ドメインに対する暗号化されたメッセージの数を表示するようにビューを変更できます。

![暗号化レポートのデータをメニュー別に表示する](../../media/encryptionreport-viewdataby.png)

新しい暗号化レポートを柔軟に使用することで、傾向を表示し、適切な操作を実行できます。 たとえば、ユーザーによって大量の電子メールメッセージが暗号化されている場合、暗号化ポリシーを追加して、特定のユースケースの暗号化を自動化することができます。 (詳細については、「 [Microsoft 365 で電子メールメッセージを暗号化するためのメールフロールールを定義する](../../compliance/define-mail-flow-rules-to-encrypt-email.md)」を参照してください)。もう1つの例として、使用可能な暗号化テンプレートが多数あり、それを使用しているユーザーがいない場合は、その機能についてユーザーにトレーニングが必要かどうかを調べることができます。

このレポートを使用すると、組織のセキュリティとコンプライアンスチームは、メッセージの暗号化の使用方法と、さらにアクションが必要かどうかを監視できます。 暗号化の詳細については、「 [Microsoft 365 の電子メールの暗号化](../../compliance/email-encryption.md)」を参照してください。

## <a name="threat-protection-status-report"></a>脅威保護の状態レポート

**脅威保護の状態**レポートは、Exchange Online Protection によって検出およびブロックされた悪意のある電子メールを示すスマートレポートです。 このレポートは、マルウェアまたはフィッシング詐欺として特定された電子メールを時間の経過とともに (最大90日間) 表示し、セキュリティ管理者が傾向を特定したり、ポリシーが調整を必要とするかどうかを判断したりするのに役立ちます。

> [!NOTE]
> 脅威保護の状態レポートは、 [Office 365 ATP](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp)または[Exchange Online Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/what-is-eop) (EOP) のいずれかを使用しているお客様が利用できます。ただし、ATP のお客様の脅威保護状態レポートに表示される情報には、EOP のお客様に表示されるものとは異なるデータが含まれている可能性があります。 たとえば、EOP のお客様は、電子メールで検出されたマルウェアに関する情報を表示できますが、 [SharePoint Online、OneDrive、Microsoft Teams で検出された悪意のあるファイル](https://docs.microsoft.com/microsoft-365/security/office-365-security/atp-for-spo-odb-and-teams)に関する情報は、ATP 固有の機能です。 ([ATP レポートの詳細について](https://docs.microsoft.com/microsoft-365/security/office-365-security/view-reports-for-atp)は、を参照してください)。

このレポートを表示するには、[セキュリティ & コンプライアンスセンター](https://protection.office.com)で、[**レポート** \> **ダッシュボード** \>の**脅威保護の状態**] に移動します。

![脅威保護の状態レポート](../../media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)

脅威保護の状態レポートを初めて開いたとき、既定では過去7日間のデータがレポートに表示されます。ただし、[**フィルター** ] をクリックして、最大90日間の日付範囲を変更することができます。 (試用版サブスクリプションを使用している場合は、30日間のデータに制限されることがあります)。

このレポートは、組織の[Exchange Online Protection 機能](https://docs.microsoft.com/microsoft-365/security/office-365-security/eop-features)の有効性と影響、および長期的な傾向を確認するのに役立ちます。

![脅威保護の状態レポートのフィルター](../../media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)

悪意があると識別された電子メール、フィッシングとして識別された電子メール、マルウェアを含んでいると識別された電子メールのデータを表示するかどうかを選択することもできます。

![脅威保護の状態レポートの表示オプション](../../media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)

## <a name="malware-detections-report"></a>マルウェア検出レポート

**マルウェア検出**レポートは、組織のマルウェアが含まれているとして検出された受信メッセージと送信メッセージの数を示します。

このレポートを表示するには、[セキュリティ & コンプライアンスセンター](https://protection.office.com)で、[**レポート** \> **ダッシュボード** \> **マルウェア検出**] に移動します。

![マルウェア検出レポートの例](../../media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)

[脅威保護の状態レポート](#threat-protection-status-report)などの他のレポートと同様に、レポートには既定で過去7日間のデータが表示されます。 ただし、[**フィルター** ] を選択して、日付の範囲を変更できます。

## <a name="top-malware-report"></a>上位マルウェアレポート

**上位マルウェア**レポートには、 [Exchange Online](https://docs.microsoft.com/microsoft-365/security/office-365-security/eop-features)によって検出されたさまざまな種類のマルウェアが表示されます。

このレポートを表示するには、[セキュリティ & コンプライアンスセンター](https://protection.office.com)で、[ **Reports** \> **Dashboard** \> **Top マルウェア**] に移動します。

![SCC-EOP Top マルウェア](../../media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)

円グラフのくさび形の上にポインターを移動すると、マルウェアの種類の名前と、マルウェアを持っていることが検出されたメッセージの数を確認できます。

レポートをクリック (またはタップ) して、新しいブラウザーウィンドウでレポートを開きます。これにより、レポートの詳細が表示されます。

![このレポートには、組織で検出された上位のマルウェアが表示されます。](../../media/3fded224-fb31-4713-86f2-8afce5ce2991.png)

グラフの下に、検出されたマルウェアの一覧と、マルウェアを持っていることが検出されたメッセージの数が表示されます。

## <a name="top-senders-and-recipients-report"></a>[上位送信者および受信者] レポート

[**上位の送信者と受信者**] レポートは、上位の電子メール送信者を示す円グラフです。

このレポートを表示するには、[セキュリティ & コンプライアンスセンター](https://protection.office.com)で、[**レポート** \> **ダッシュボード** \>の**上位送信者および受信者**] に移動します。

![このレポートを表示するには、セキュリティ & コンプライアンスセンターで、[ \>レポート\>ダッシュボードのトップ送信者と受信者] に移動します。](../../media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)

円グラフのくさび形の上にポインターを移動すると、送信または受信したメッセージの数が表示されます。

レポートをクリック (またはタップ) して、新しいブラウザーウィンドウでレポートを開きます。これにより、レポートの詳細が表示されます。

[**データの表示**] リストを使用して、上位の送信者、受信者、スパム受信者、およびマルウェア受信者のデータを表示するかどうかを選択します。 また、 [Exchange Online Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/what-is-eop)によって検出されたマルウェアの受信者を確認することもできます。

![特定の情報を表示するには、[データの表示] リストを使用します。](../../media/bd91449f-7d42-4749-8666-7b44044049b8.png)

グラフの下に、上位の電子メール送信者または受信者の数と、指定された期間に送受信されたメッセージ数が表示されます。

## <a name="spoof-detections-report"></a>スプーフィング検出レポート

**スプーフィング検出**レポートには、検出されたスプーフィングメールメッセージの数と、それらのメッセージのうちどれが "good" (正当なビジネス上の理由で、メールのスプーフィングが行われたもの) であることが示されています。

このレポートを表示するには、[セキュリティ & コンプライアンスセンター](https://protection.office.com)で、[**レポート** \> **ダッシュボード** \> **スプーフィングメール**] に移動します。

![セキュリティ & コンプライアンスセンターで、[レポート\>ダッシュボード\>のスプーフィングメール] に移動します。](../../media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)

グラフの1日をポイントすると、受信したスプーフィングメールメッセージの数を確認できます。

レポートをクリック (またはタップ) して、新しいブラウザーウィンドウでレポートを開きます。これにより、レポートの詳細が表示されます。 スプーフィング対策保護の詳細については、「 [Microsoft 365 のスプーフィング対策保護](anti-spoofing-protection.md)」を参照してください。

## <a name="spam-detections-report"></a>スパム検出レポート

**スパム検出**レポートには、Exchange Online によってブロックされているすべてのスパムコンテンツが表示されます。 メッセージは、受信者ごとではなく、メッセージごとにカウントされます。 たとえば、電子メールメッセージが組織内の100の受信者に送信された場合は、1つのメッセージとして数えられます。

このレポートを表示するには、[セキュリティ & コンプライアンスセンター](https://protection.office.com)で、[**レポート** \> ]**ダッシュボード** \>の [**スパム検出**] に移動します。

![このレポートを表示するには、セキュリティ & コンプライアンスセンターで、[ \>レポート\>ダッシュボード EOP スパム検出] に移動します。](../../media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)

グラフの1日の上にカーソルを置くと、その日にブロックされたアイテムの数と、それらのアイテムがどのように分類されているかを確認できます。 たとえば、フィルター処理されたスパムメッセージの数と、ブロックされたインターネットプロトコル (IP) アドレスからのアイテムの数を確認できます。

レポートをクリック (またはタップ) して、新しいブラウザーウィンドウでレポートを開きます。これにより、レポートの詳細が表示されます。

![スパム検出レポートでは、ブロックまたはフィルターで除外されたスパムメッセージの数がわかります。](../../media/370ec67d-eb30-4863-bfcf-68a41be02295.png)

グラフの下に、検出されたスパムアイテムの一覧が表示されます。 その他の情報を表示するアイテムを選択します。これには、受信または送信、メッセージ ID、受信者などの追加情報が表示されます。 スパム対策保護の詳細については、「 [Office 365 電子メールのスパム対策保護](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spam-and-anti-malware-protection)」を参照してください。

## <a name="sent-and-received-email-report"></a>送信および受信した電子メールレポート

**送信および受信**した電子メールレポートは、スパム検出、マルウェア、および "good" と識別された電子メールを含む、受信および送信電子メールに関する情報を示すスマートレポートです。

このレポートを表示するには、[セキュリティ & コンプライアンスセンター](https://protection.office.com)で、[**レポート** \> **ダッシュボード** \> **送受信された電子メール**] に移動します。

![このレポートを表示するには、セキュリティ & コンプライアンスセンターで、[ \>レポート\>ダッシュボード送受信メール] に移動します。](../../media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)

グラフの1日の上にカーソルを置くと、受信したメッセージの数と、それらのメッセージがどのように分類されるかを確認できます。 たとえば、マルウェアが含まれているとして検出されたメッセージの数と、スパムとして識別されたメッセージの数を確認できます。

レポートをクリック (またはタップ) して、新しいブラウザーウィンドウでレポートを開きます。これにより、レポートの詳細が表示されます。

[**分類**] ボックスの一覧を使用すると、情報を種類別または方向 (受信および送信) 別に表示できます。

![[分類] ボックスの一覧を使用して、種類または方向で情報を表示する](../../media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)

グラフの下に、 **GoodMail**、 **SpamContentFiltered**などの電子メールカテゴリの一覧が表示されます。 カテゴリを選択して、マルウェアに対して行われたアクションや電子メールが受信または送信されたかどうかなどの追加情報を表示します。

![このレポートは、マルウェア対策、スパム対策、およびその他のメッセージの検出に関する情報を示します。](../../media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)

電子メールインテリジェンスの詳細については、「 [Microsoft 365 のメールフローインテリジェンス](https://docs.microsoft.com/microsoft-365/security/office-365-security/mail-flow-intelligence-in-office-365)」を参照してください。

## <a name="user-reported-messages-report"></a>ユーザーによって報告されたメッセージレポート

ユーザーによって報告された**メッセージ**レポートには、ユーザーが[レポートメッセージアドイン](https://docs.microsoft.com/microsoft-365/security/office-365-security/enable-the-report-message-add-in)を使用して、迷惑メール、フィッシングの試行、または正常なメールとして報告した電子メールメッセージに関する情報が表示されます。

組織に対して構成されたスパムポリシーの例外やメールフロールールなどの配信理由を含む、各メッセージの詳細を表示できます。 詳細を表示するには、[ユーザーレポート] リスト内のアイテムを選択し、[**概要**] タブと [**詳細**] タブで情報を表示します。

![ユーザーによって報告されたメッセージのレポートには、ユーザーが迷惑メールではないというラベルが付けられます。](../../media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)

このレポートを表示するには、[セキュリティ & コンプライアンスセンター](https://protection.office.com)で、次のいずれかの手順を実行します。

- [**脅威管理** \> ]**ダッシュボード** \>の**ユーザーによって報告**されたメッセージに移動します。

- [**脅威の管理** \> ] に移動して **、ユーザーから報告**されたメッセージを**確認** \>します。

![セキュリティ & コンプライアンスセンターで、[脅威管理\> ] [ \>ユーザーが報告するメッセージを確認する] を選択します。](../../media/e372c57c-1414-4616-957b-bc933b8c8711.png)

> [!IMPORTANT]
> ユーザーによって報告されたメッセージレポートが正常に機能するためには、Office 365 環境の**監査ログを有効にする必要があり**ます。 これは、通常、Exchange Online で監査ログの役割が割り当てられているユーザーによって行われます。 詳細については、「 [Microsoft 365 監査ログ検索を有効または無効にする](https://docs.microsoft.com/microsoft-365/compliance/turn-audit-log-search-on-or-off)」を参照してください。

## <a name="what-permissions-are-needed-to-view-these-reports"></a>これらのレポートを表示するには、どのようなアクセス許可が必要ですか。

この記事に記載されているレポートを表示して使用するには、**セキュリティ & コンプライアンスセンターと Exchange 管理センターの両方に対して適切な役割が割り当てられている必要があり**ます。

- セキュリティ & コンプライアンスセンターでは、次の役割のいずれかが割り当てられている必要があります。

  -組織の管理-セキュリティ管理者 (これは Azure Active Directory 管理センター ([https://aad.portal.azure.com](https://aad.portal.azure.com)) で割り当てることができます-セキュリティリーダ

- Exchange Online の場合は、Exchange 管理センター ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) または PowerShell コマンドレット (「 [Exchange online Powershell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)」を参照) のいずれかで、次のいずれかの役割が割り当てられている必要があります。

  -組織の管理-表示のみの組織の管理-表示のみの受信者ロールコンプライアンス管理

詳細については、次のリソースを参照してください。

- [セキュリティ/コンプライアンス センターのアクセス許可](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center)
 
- [Exchange Online の機能アクセス許可](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)

## <a name="what-if-the-reports-arent-showing-data"></a>レポートでデータが表示されない場合はどうなりますか。

レポートにデータが表示されない場合は、ポリシーが正しく設定されているかどうかを再確認してください。 詳細については、「 [Microsoft 365 の脅威から保護](https://docs.microsoft.com/microsoft-365/security/office-365-security/protect-against-threats)する」を参照してください。

## <a name="related-topics"></a>関連項目

[Microsoft 365 メールのスパム対策保護](https://docs.microsoft.com/microsoft-365/security/office-365-security/anti-spam-and-anti-malware-protection)

[セキュリティ & コンプライアンスセンターのレポートと分析情報](https://docs.microsoft.com/microsoft-365/security/office-365-security/reports-and-insights-in-security-and-compliance)

[セキュリティ & コンプライアンスセンターでレポートのスケジュールを作成する](https://docs.microsoft.com/microsoft-365/security/office-365-security/create-a-schedule-for-a-report)

[セキュリティ & コンプライアンスセンターでカスタムレポートを設定およびダウンロードする](https://docs.microsoft.com/microsoft-365/security/office-365-security/set-up-and-download-a-custom-report)