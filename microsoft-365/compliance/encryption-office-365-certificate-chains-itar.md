---
title: Office 365 の暗号化チェーン-DOD および GCC High
f1.keywords:
- NOCSH
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 3/24/2020
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
- Strat_O365_IP
description: Office 365 の DOD および GCC 高ルート証明書と証明機関 (CAs) の完全な一覧を表示します。
ms.openlocfilehash: 615a62b2ae2a954580ebf82f4c1b70748c991a71
ms.sourcegitcommit: 6adfcf042e64b21f09f2b8e072e8eba6d3479e31
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/25/2020
ms.locfileid: "42951905"
---
# <a name="office-365-encryption-chains---dod-and-gcc-high"></a>Office 365 の暗号化チェーン-DOD および GCC High

Office 365 は、いくつかの異なる証明書プロバイダーを活用しています。 以下は、 **DOD および GCC が多くのお客様**が Office 365 へのアクセス時に遭遇する既知の Office 365 ルート証明書の完全なリストを示しています。 独自のインフラストラクチャにインストールする必要がある証明書の詳細については、「 [Plan for サードパーティ SSL certificates For Office 365](https://docs.microsoft.com/office365/enterprise/plan-for-third-party-ssl-certificates)」を参照してください。

次の証明書情報は、**すべての DOD および GCC 高のお客様**に適用されます。

>[!NOTE]
>**世界中のお客様**に適用される証明書情報については、「 [Office 365 暗号化チェーン](encryption-office-365-certificate-chains.md)」を参照してください。

| **証明書の種類** | **P7b ダウンロード** | **CRL エンドポイント** | **OCSP エンドポイント** |
| --- | --- | --- | --- | --- |
| 公的に信頼されたルートおよび中間証明書 | [Office 365 ITAR 証明書バンドル (P7B)](https://download.microsoft.com/download/b/3/a/b3ae08a2-516c-46a9-8723-6256e4fd6383/O365_Chain_Certs_ITAR20200304.p7b) | crl.entrust.net<br>crl3.digicert.com<br>crl4.digicert.com | ocsp.digicert.com<br>ocsp.entrust.net |

証明書プロバイダーの詳細については、以下のセクションを展開して、その他の詳細を確認してください。

## <a name="office-365-certificate-details"></a>**Office 365 証明書の詳細**

### <a name="baltimore-cybertrust-root"></a>**Baltimore CyberTrust Root**

| **Subject** | CN = ボルチモア CyberTrust Root<br>OU = CyberTrust<br>O = ボルチモア<br>C = IE |
| --- | --- |
| **シリアル番号** | 02:00:00: B9 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha1RSA |
| **有効期限以前** | 12 18:46:00 2000 年5月 |
| **有効期限が過ぎていない** | 12 23:59:00 2025 年5月 |
| **サブジェクトキー識別子** | e5: 9d:59:30:82:47:58: cc: ac: fa:08:54:36:86: 7b:: b5:04: 4d: f0 |
| **拇印 (SHA-1)** | D4DE20D05E66FC53FE1A50882C78DB2852CAE474 |
| **拇印 (SHA-256)** | 16AF57A9F676B0AB126095AA5EBADEF22AB31119D644AC95CD4B93DBF3F26AEB |
| **Pin (SHA-256)** | Y9mvm0exBk1JoQ57f9Vm28jKo5lFm/woKcVxrYxu80o = |

### <a name="digicert-cloud-services-ca-1"></a>**DigiCert Cloud Services CA-1**

| **Subject** | CN = DigiCert Cloud Services CA-1<br>O = DigiCert Inc<br>C = US |
| --- | --- |
| **発行者** | CN = DigiCert グローバルルート CA<br>OU = digicert<br>O = DigiCert Inc<br>C = US |
| **シリアル番号** | 01: 9E: C1: C6: BD: 3F:59: 7B: B2: 0C:33:38: E5:51: D8:77 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha256RSA |
| **有効期限以前** | 04 12:00:00 2015 年8月 UTC |
| **有効期限が過ぎていない** | 04 12:00:00 2030 年8月 UTC |
| **サブジェクトキー識別子** | dd:51: d0: a2:31:73: a9:73: ae: 8f: b4:01: 7e: 5d: 8c:57: cb: 9f: f0: f7 |
| **権限キー識別子** | キー id:03: de:50:35:56: d1: 4c: bb:66: f0: a3: e2: 1b: 1b: c3:97: b2: 3d: d1:55 |
| **拇印 (SHA-1)** | 81B68D6CD2F221F8F534E677523BB236BBA1DC56 |
| **拇印 (SHA-256)** | 2F6889961A7CA7067E8BA103C2CF9B9A924F8CA293F11178E23A1978D2F133D3 |
| **Pin (SHA-256)** | UgpUVparimk8QCjtWQaUQ7EGrtrykc/L8N66EhFY3VE = |
| **CRL Url** | http://crl4.digicert.com/DigiCertGlobalRootCA.crl<br>http://crl3.digicert.com/DigiCertGlobalRootCA.crl |
| **OCSP の Url** | http://ocsp.digicert.com |

### <a name="digicert-global-root-ca"></a>**DigiCert グローバルルート CA**

| **Subject** | CN = DigiCert グローバルルート CA<br>OU = digicert<br>O = DigiCert Inc<br>C = US |
| --- | --- |
| **シリアル番号** | 08: 3B: E0:56:90:42:46: B1: A1:75: 6A: C9:59:91: C7: 4A |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha1RSA |
| **有効期限以前** | 10 00:00:00 2006 年11月 UTC |
| **有効期限が過ぎていない** | 10 00:00:00 2031 年11月 UTC |
| **サブジェクトキー識別子** | 03: de:50:35:56: d1: 4c: bb:66: f0: a3: e2: 1b: 1b: c3:97: b2: 3d: d1:55 |
| **権限キー識別子** | キー id:03: de:50:35:56: d1: 4c: bb:66: f0: a3: e2: 1b: 1b: c3:97: b2: 3d: d1:55 |
| **拇印 (SHA-1)** | A8985D3A65E5E5C4B2D7D66D40C6DD2FB19C5436 |
| **拇印 (SHA-256)** | 4348A0E9444C78CB265E058D5E8944B4D84F9662BD26DB257F8934A443C70161 |
| **Pin (SHA-256)** | r/mIkG3eEpVdm + u/ko-kr/cwxzOMo1bk4TyHIlByibiA5E = |

### <a name="digicert-high-assurance-ev-root-ca"></a>**DigiCert の高保証 EV ルート CA**

| **Subject** | CN = DigiCert 高保証 EV ルート CA<br>OU = digicert<br>O = DigiCert Inc<br>C = US |
| --- | --- |
| **シリアル番号** | 02: AC: 5C:26: 6A: 0B:40: 9B: 8F: 0B:79: F2: AE:46:25:77 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha1RSA |
| **有効期限以前** | 10 00:00:00 2006 年11月 UTC |
| **有効期限が過ぎていない** | 10 00:00:00 2031 年11月 UTC |
| **サブジェクトキー識別子** | b1: 3e: c3:69:03: f8: bf:47:01: d4:98:26: 1a:08:02: ef:63:64: 2b: c3 |
| **権限キー識別子** | キー id: b1:、3e: c3:69:03: f8: bf:47:01: d4:98:26: 1a:08:02: ef:63:64: 2b: c3 |
| **拇印 (SHA-1)** | 5FB7EE0633E259DBAD0C4C9AE6D38F1A61C7DC25 |
| **拇印 (SHA-256)** | 7431E5F4C3C1CE4690774F0B61E05440883BA9A01ED00BA6ABD7806ED3B118CF |
| **Pin (SHA-256)** | WoiWRyIOVNa9ihaBciRSC7XHjliYS9VwUGOIud4PB18 = |

### <a name="digicert-sha2-extended-validation-server-ca"></a>**DigiCert SHA2 Extended Validation Server CA**

| **Subject** | CN = DigiCert SHA2 Extended Validation Server CA<br>OU = digicert<br>O = DigiCert Inc<br>C = US |
| --- | --- |
| **シリアル番号** | 0C:79: A9:44: B0: 8C:11:95:20:92:61: 5F: E2: 6B: 1D:83 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha256RSA |
| **有効期限以前** | 10月 22 00:00:00 2013 UTC |
| **有効期限が過ぎていない** | 10月 22 00:00:00 2028 UTC |
| **サブジェクトキー識別子** | 3D: D3:50: A5: D6: A0: AD: EE: F3: 4A:60: 0A:65: D3:21: D4: F8: F8: D6: 0F |
| **権限キー識別子** | キー Id: b1:、3e: c3:69:03: f8: bf:47:01: d4:98:26: 1a:08:02: ef:63:64: 2b: c3 |
| **拇印 (SHA-1)** | 7E2F3A4F8FE8FA8A5730AECA029696637E986F3F |
| **拇印 (SHA-256)** | 403E062A2653059113285BAF80A0D4AE422C848C9F78FAD01FC94BC5B87FEF1A |

### <a name="entrust-root-certification-authority"></a>**Entrust ルート証明機関**

| **Subject** | CN = Entrust ルート証明機関<br>OU = "(c) 2006 Entrust, Inc"<br>OU = entrust/CPS はリファレンスに組み込まれています。<br>OU = 「www.entrust.net/legal-terms」を参照<br>O =&quot;Entrust, Inc&quot;<br>C = US |
| --- | --- |
| **シリアル番号** | 45: 6B:50:54 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha1RSA |
| **有効期限以前** | 27 12:23:42 2006 年11月 UTC |
| **有効期限が過ぎていない** | 27 12:53:42 2026 年11月 UTC |
| **サブジェクトキー識別子** | 68:90: E4:67: A4: A6:53:80: C7:86:66: A4: F1: F7: 4B:43: FB:84: BD: 6D |
| **権限キー識別子** | キー Id:68:90: e4:67: a4: a6:53:80: c7:86:66: a4: f1: f7: 4b:43: fb:84: bd: 6d |
| **拇印 (SHA-1)** | B31EB1B740E36C8402DADC37D44DF5D4674952F9 |
| **拇印 (SHA-256)** | 73C176434F1BC6D5ADF45B0E76E727287C8DE57616C1E6E6141A2B2CBC7D8E4C |

### <a name="entrust-root-certification-authority---g2"></a>**Entrust ルート証明機関-G2**

| **Subject** | CN = Entrust ルート証明機関-G2<br>OU =&quot;(c) 2009 Entrust, inc.-承認済みの使用のみ&quot;<br>OU = 「www.entrust.net/legal-terms」を参照<br>O =&quot;Entrust, Inc&quot;<br>C = US |
| --- | --- |
| **シリアル番号** | 4A:53: 8C:28 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha256RSA |
| **有効期限以前** | 7月 07 17:25:54 2009 UTC |
| **有効期限が過ぎていない** | 10月 07 17:55:54 2030 UTC |
| **サブジェクトキー識別子** | 6a:72:26: 7a: d0: 1e: ef: 7d: e7: 3b:69:51: d4: 6c: 8d: 9f:90:12:66: ab |
| **拇印 (SHA-1)** | 8CF427FD190C3AD1660CFM DE81E57EFBB932272D4 |
| **拇印 (SHA-256)** | 43DF5774B03E7FEF5FE40D931A7BEDF1BB2E6B42738C4E6D3841103D3AA7F339 |
| **Pin (SHA-256)** | du6FkDdMcVQ3u8prumAo6t3i3G27uMP2EOhR8R0at/U = |

### <a name="entrustnet-certification-authority-2048"></a>**Entrust.net Certification Authority (2048)**

| **Subject** | CN = Entrust 証明機関 (2048)<br>OU = (c) 1999 Entrust.net 制限付き<br>OU = entrust/CPS\_2048 incorp。 ref で。 (制限 s liab.)<br>O = Entrust |
| --- | --- |
| **シリアル番号** | 38:63: DE: F8 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha1RSA |
| **有効期限以前** | 10月 24 17:50:51 1999 UTC |
| **有効期限が過ぎていない** | 7月 24 14:15:12 2029 UTC |
| **サブジェクトキー識別子** | 55: e4:81: d1:11:80:: d8:89: b9:08: a3:31: f9: a1:24:09:16: b9:70 |
| **拇印 (SHA-1)** | 503006091D97D4F5AE39F7CBE7927D7D652D3431 |
| **拇印 (SHA-256)** | 6DC47172E01CBCB0BF62580D895FE2B8AC9AD4F87 3801E0C10B9C837D21EB177 |
| **Pin (SHA-256)** | HqPF5D7WbC2imDpCpKebHpBnhs6fG1hiFBmgBGOofTg = |

### <a name="entrust-certification-authority---l1c"></a>**Entrust 証明機関-L1C**

| **Subject** | CN = Entrust 証明機関-L1C<br>OU =&quot;(c) 2009 Entrust, Inc&quot;<br>OU = entrust/rpa はリファレンスに組み込まれています。<br>O =&quot;Entrust, Inc&quot;<br>C = US |
| --- | --- |
| **発行者** | CN = Entrust 証明機関 (2048)<br>OU = (c) 1999 Entrust.net 制限付き<br>OU = entrust/CPS\_2048 incorp。 ref で。 (制限 liab.)<br>O = Entrust |
| **シリアル番号** | 4C: 0E: 8C:39 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha1RSA |
| **有効期限以前** | 11 15:40:40 2011 年11月 UTC |
| **有効期限が過ぎていない** | 11 02:51:17 2021 年11月 UTC |
| **サブジェクトキー識別子** | 1e: f1: ab:89:06: f8:49: 0f:01:33:77: ee:17: 7a: ee:19: 7c:93:28: 4d |
| **権限キー識別子** | キー id:55: e4:81: d1:11:80: be: d8:89: b9:08:08:31:-f9: a1:24:09:16: b9:70 |
| **拇印 (SHA-1)** | C53E73073F93CE7895DE7484126BC303DAB9E657 |
| **拇印 (SHA-256)** | 0EE4DAF71A85D842D23F4910FD4C909B7271861931F1D5FEAC868225F52700E2 |
| **Pin (SHA-256)** | VFv5NemtodoRftw8KsvFb8AoCWwOJL6bOJS + Ui0bQ94 = |
| **CRL Url** | http://crl.entrust.net/2048ca.crl |
| **OCSP の Url** | http://ocsp.entrust.net |

### <a name="entrust-certification-authority---l1e"></a>**Entrust 証明機関-L1E**

| **Subject** | CN = Entrust 証明機関-L1E<br>OU =&quot;(c) 2009 Entrust, Inc&quot;<br>OU = entrust/rpa はリファレンスに組み込まれています。<br>O =&quot;Entrust, Inc&quot;<br>C = US |
| --- | --- |
| **発行者** | CN = Entrust 証明機関 (2048)<br>OU = (c) 1999 Entrust.net 制限付き<br>OU = entrust/CPS\_2048 incorp。 ref で。 (制限 liab.)<br>O = Entrust |
| **シリアル番号** | 4C: 0E: C9:18 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha1RSA |
| **有効期限以前** | 11 15:40:40 2011 年11月 UTC |
| **有効期限が過ぎていない** | 11 02:51:17 2021 年11月 UTC |
| **サブジェクトキー識別子** | 5B:41: 8A: B2: C4:43: C1: BD: BF: C8:54:41:55: 9D: E0:96: AD: FF: B9: A1 |
| **権限キー識別子** | キー id:68:90: e4:67: a4: a6:53:80: c7:86:66: a4: f1: f7: 4b:43: fb:84: bd: 6d |
| **拇印 (SHA-1)** | 8A000CC056F7D17349F045BEB0319A3B91C9F979 |
| **拇印 (SHA-256)** | 3C7A634E5778A0F731972B702DAE24B2CF2060219F607E69878B164C61A06C41 |
| **CRL Url** | http://crl.entrust.net/rootca1.crl |
| **OCSP の Url** | http://ocsp.entrust.net |

### <a name="entrust-certification-authority---l1k"></a>**Entrust 証明機関-L1K**

| **Subject** | CN = Entrust 証明機関-L1K<br>OU =&quot;(c) 2012 Entrust, inc.-承認済みの使用のみ&quot;<br>OU = 「www.entrust.net/legal-terms」を参照<br>O =&quot;Entrust, Inc&quot;<br>C = US |
| --- | --- |
| **発行者** | CN = Entrust ルート証明機関-G2<br>OU =&quot;(c) 2009 Entrust, inc.-承認済みの使用のみ&quot;<br>OU = 「www.entrust.net/legal-terms」を参照<br>O =&quot;Entrust, Inc&quot;<br>C = US |
| **シリアル番号** | 0E: E9: 4C: C3:00:00:00:00:51: D3:77:85 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha256RSA |
| **有効期限以前** | 10月 05 19:13:56 2015 UTC |
| **有効期限が過ぎていない** | 10月 05 19:43:56 2030 UTC |
| **サブジェクトキー識別子** | 82: a2:70:74: dd: bc:53: 3f: cf: 7b: d4: f7: cd: 7f: a7:60: c6: 0a: 4c: bf |
| **権限キー識別子** | キー id: 6a:27:26: 7a: d0: 1e: ef: 7d: e7: 3b:69:51: d4: 6c: 8d: 9f:90:12:66: ab |
| **拇印 (SHA-1)** | F21C12F46CDB6B2E16F09F9419CDFF328437B2D7 |
| **拇印 (SHA-256)** | 13EFB39A2F6654E8C67BD04F4C6D4C90CD6CAB5091BCEDC73787F6B77D3D3FE7 |
| **Pin (SHA-256)** | 980Ionqp3wkYtN9SZVgMzuWQzJta1nfxNPwTem1X0uc = |
| **CRL Url** | http://crl.entrust.net/g2ca.crl |
| **OCSP の Url** | http://ocsp.entrust.net |

### <a name="entrust-certification-authority---l1m"></a>**Entrust 証明機関-L1M**

| **Subject** | CN = Entrust サーティフィケーション Authority-L1M, OU =&quot;(c) 2014 Entrust, Inc.-承認済みの使用のみ&quot;<br>OU = 「www.entrust.net/legal-terms」を参照<br>O =&quot;Entrust, Inc&quot;<br>C = US |
| --- | --- |
| **発行者** | CN = Entrust ルート証明機関-G2<br>OU =&quot;(c) 2009 Entrust, inc.-承認済みの使用のみ&quot;<br>OU = 「www.entrust.net/legal-terms」を参照<br>O =&quot;Entrust, Inc&quot;<br>C = US |
| **シリアル番号** | 61: A1: E7: D2:00:00:00:00:51: D3:66: A6 |
| **公開キーの長さ** | RSA 2048 ビット (e 65537) |
| **署名アルゴリズム** | sha256RSA |
| **有効期限以前** | 10月 15 07:25:03 2014 UTC |
| **有効期限が過ぎていない** | 10月 15 08:55:03 2030 UTC |
| **サブジェクトキー識別子** | C3: F7: D0: D0: D0:: B5:91:21:70:91:54: 365:70:39: DD: BC:89:70: C7: 3A |
| **権限キー識別子** | キー id: 6a:27:26: 7a: d0: 1e: ef: 7d: e7: 3b:69:51: d4: 6c: 8d: 9f:90:12:66: ab |
| **拇印 (SHA-1)** | CC136695639065FAB47074D28C55314C66077E90 |
| **拇印 (SHA-256)** | 75C5B3F01FD1F51A2C447AB7C785D72E69FA9C472C08571E7EADF3B8EABAE70C |
| **CRL Url** | http://crl.entrust.net/g2ca.crl |
| **OCSP の Url** | http://ocsp.entrust.net |

### <a name="microsoft-it-tls-ca-1"></a>**Microsoft IT TLS CA 1**

| **Subject** | CN = Microsoft IT TLS CA 1<br>OU = Microsoft IT<br>O = Microsoft Corporation<br>L = Redmond<br>S = ワシントン<br>C = US |
| --- | --- |
| **発行者** | CN = ボルチモア CyberTrust Root<br>OU = CyberTrust<br>O = ボルチモア<br>C = IE |
| **シリアル番号** | 08: B8: 7A:50: 1B: BE: 9C: DA: 2D:16: 4D: 3E:39:43: BF:55 |
| **公開キーの長さ** | RSA 4096 ビット (e 65537) |
| **署名アルゴリズム** | sha256RSA |
| **有効期限以前** | 20 12:51:28 2016 年5月 |
| **有効期限が過ぎていない** | 20 12:51:28 2024 年5月 |
| **サブジェクトキー識別子** | 58:88: 9f: d6: dc: 9c:48:22: b7:15: 3e: ff:84:88: e8: e6:85: ff: fa: 7d |
| **権限キー識別子** | キー id: e5: 9d:59:30:82:47:58: cc: ac: fa:08:54:36:86:82: 3a: b5:04: 4d: f0 |
| **拇印 (SHA-1)** | 417E225037FBFAA4F95761D5AE729E1AEA7E3A42 |
| **拇印 (SHA-256)** | 4FF404F02E2CD00188F15D1C00F4B6D1E38B5A395CF85314EAEBA855B6A64B75 |
| **Pin (SHA-256)** | xjXxgkOYlag7jCtR5DreZm9b61iaIhd + J3 + b2LiybIw = |
| **CRL Url** | http://crl3.digicert.com/Omniroot2025.crl |
| **OCSP の Url** | http://ocsp.digicert.com |

### <a name="microsoft-it-tls-ca-2"></a>**Microsoft IT TLS CA 2**

| **Subject** | CN = Microsoft IT TLS CA 2<br>OU = Microsoft IT<br>O = Microsoft Corporation<br>L = Redmond<br>S = ワシントン<br>C = US |
| --- | --- |
| **発行者** | CN = ボルチモア CyberTrust Root<br>OU = CyberTrust<br>O = ボルチモア<br>C = IE |
| **シリアル番号** | 0F: 2C:10: C9: 5B:06: C0:93: 7F: B8: D4:49: F8: 3E:85:69 |
| **公開キーの長さ** | RSA 4096 ビット (e 65537) |
| **署名アルゴリズム** | sha256RSA |
| **有効期限以前** | 20 12:51:57 2016 年5月 |
| **有効期限が過ぎていない** | 20 12:51:57 2024 年5月 |
| **サブジェクトキー識別子** | 91: 9e: 3b:44: 6c: 3d:57: 9c:42:77: 2a:34: d7: 4f: d1: cc: 4a:97: 2c: da |
| **権限キー識別子** | キー id: e5: 9d:59:30:82:47:58: cc: ac: fa:08:54:36:86:82: 3a: b5:04: 4d: f0 |
| **拇印 (SHA-1)** | 54D9D20239080C32316ED9FF980A48988F4ADF2D |
| **拇印 (SHA-256)** | 4E107C981B42ACBE41C01067E16D44DB64814D4193E572317EA04B87C79C475F |
| **Pin (SHA-256)** | wBdPad95AU7OgLRs0FU/E6ILO1MSCM84kJ9y0H + TT7s = |
| **CRL Url** | http://crl3.digicert.com/Omniroot2025.crl |
| **OCSP の Url** | http://ocsp.digicert.com |

### <a name="microsoft-it-tls-ca-4"></a>**Microsoft IT TLS CA 4**

| **Subject** | CN = Microsoft IT TLS CA 4<br>OU = Microsoft IT<br>O = Microsoft Corporation<br>L = Redmond<br>S = ワシントン<br>C = US |
| --- | --- |
| **発行者** | CN = ボルチモア CyberTrust Root<br>OU = CyberTrust<br>O = ボルチモア<br>C = IE |
| **シリアル番号** | 0B: 6A: B3: B0: 3E:、B1: A9: F6: C4:60:92: 6A: A8: CD: FE: B3 |
| **公開キーの長さ** | RSA 4096 ビット (e 65537) |
| **署名アルゴリズム** | sha256RSA |
| **有効期限以前** | 20 12:52:38 2016 年5月 |
| **有効期限が過ぎていない** | 20 12:52:38 2024 年5月 |
| **サブジェクトキー識別子** | 7a: 7b: 8c: c1: cf: e7: a0: ca: 1c: d4: 6b: fa: fb: e1:33: 0f: 0f: 1a: 9d 9d |
| **権限キー識別子** | キー id: e5: 9d:59:30:82:47:58: cc: ac: fa:08:54:36:86:82: 3a: b5:04: 4d: f0 |
| **拇印 (SHA-1)** | 8A38755D0996823FE8FA3116A277CE446EAC4E99 |
| **拇印 (SHA-256)** | 5FFAC43E0DDC5B4AF2B696F6BC4DB7E91DF314BB8FE0D0713A0B1A7AD2A68FAC |
| **Pin (SHA-256)** | wUY9EOTJmS7Aj4fDVCu/KeE + + mV7FgIcbn4WhMz1I2k = |
| **CRL Url** | http://crl3.digicert.com/Omniroot2025.crl |
| **OCSP の Url** | http://ocsp.digicert.com |

### <a name="microsoft-it-tls-ca-5"></a>**Microsoft IT TLS CA 5**

| **Subject** | CN = Microsoft IT TLS CA 5<br>OU = Microsoft IT<br>O = Microsoft Corporation<br>L = Redmond<br>S = ワシントン<br>C = US |
| --- | --- |
| **発行者** | CN = ボルチモア CyberTrust Root<br>OU = CyberTrust<br>O = ボルチモア<br>C = IE |
| **シリアル番号** | 08:88: CD:52: 5F:19:24:44: 4D:14: A5:82:91: DE: B9:52 |
| **公開キーの長さ** | RSA 4096 ビット (e 65537) |
| **署名アルゴリズム** | sha256RSA |
| **有効期限以前** | 20 12:53:03 2016 年5月 |
| **有効期限が過ぎていない** | 20 12:53:03 2024 年5月 |
| **サブジェクトキー識別子** | 08: fe:25: 9f:74: ea:87:04: c2: bc: bb: 8e: a8:38: 5f:33: c6: d1: 6c:65 |
| **権限キー識別子** | キー id: e5: 9d:59:30:82:47:58: cc: ac: fa:08:54:36:86:82: 3a: b5:04: 4d: f0 |
| **拇印 (SHA-1)** | AD898AC73DF333EB60AC1F5FC6C4B2219DDB79B7 |
| **拇印 (SHA-256)** | F0EE5914ED94C7252D058B4E39808AEE6FA8F62CF0974FB7D6D2A9DF16E3A87F |
| **Pin (SHA-256)** | RCbqB + W8nwjznTeP4O6VjqcwdxIgI79eBpnBKRr32gc = |
| **CRL Url** | http://crl3.digicert.com/Omniroot2025.crl |
| **OCSP の Url** | http://ocsp.digicert.com |
