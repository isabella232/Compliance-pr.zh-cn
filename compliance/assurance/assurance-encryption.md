---
title: 加密和密钥管理概述
description: 了解加密和密钥管理中的Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: dc53f42c6aa7ce16e1291538bfad6d63c5a1689d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946967"
---
# <a name="encryption-and-key-management-overview"></a>加密和密钥管理概述

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>加密在保护客户内容方面扮演什么角色？

大多数 Microsoft 商业云服务都是多租户的，这意味着客户内容可能存储在与其他客户相同的物理硬件上。 为了保护客户内容的机密性，Microsoft 在线服务使用一些最强大和最安全的加密协议对静态和传输中的所有数据进行加密。

加密不能替代强访问控制。 Microsoft 的访问控制策略 Zero Standing Access (ZSA) 保护客户内容免受 Microsoft 员工未经授权的访问。 加密通过保护存储位置的客户内容机密性和防止在 Microsoft 联机服务系统之间或 Microsoft 联机服务与客户之间传输时读取内容来补充访问控制。

## <a name="how-do-microsoft-online-services-encrypt-data-at-rest"></a>Microsoft 联机服务如何加密其余数据？

Microsoft 联机服务中所有客户内容都受一种或多种加密形式的保护。 Microsoft 服务器使用 BitLocker 在卷级别加密包含客户内容的磁盘驱动器。 如果其他过程或控制 (（例如，访问控制或硬件) 的回收）存在故障，可能会导致对包含客户内容的磁盘进行未经授权的物理访问，BitLocker 提供的加密将保护客户内容。

除了卷级加密之外，Microsoft 在线服务还使用应用程序层的服务加密来加密客户内容。 服务加密提供权限保护以及强加密保护的管理功能。 它还允许在操作系统Windows这些操作系统存储或处理的客户数据之间分离。

## <a name="how-do-microsoft-online-services-encrypt-data-in-transit"></a>Microsoft 联机服务如何加密传输数据？

Microsoft 在线服务使用强传输协议（如 TLS）来防止未经授权的方在客户数据通过网络移动时窃听客户数据。 传输数据的示例包括正在传递的邮件、联机会议中的对话或在数据中心之间复制的文件。

对于 Microsoft 联机服务，每当用户设备与 Microsoft 服务器通信或 Microsoft 服务器与另一台服务器通信时，数据都被视为"正在传输"。

## <a name="how-do-microsoft-online-services-manage-the-keys-used-for-encryption"></a>Microsoft 联机服务如何管理用于加密的密钥？

强加密只与用于加密数据的密钥一样安全。 Microsoft 使用自己的安全证书加密传输数据的 TLS 连接。 对于静态数据，受 BitLocker 保护的卷使用全卷加密密钥进行加密，该密钥使用卷主密钥进行加密，而卷主密钥又绑定到服务器中的受信任的平台模块 (TPM) 。 BitLocker 使用符合 FIPS 的算法来确保从不会以清晰方式通过线路存储或发送加密密钥。

服务加密为客户静态数据提供了另一层加密，为客户提供了两种加密密钥管理选项：Microsoft 管理的密钥或客户密钥。 使用 Microsoft 管理的密钥时，Microsoft 联机服务自动生成并安全存储用于服务加密的根密钥。

如果客户要求控制自己的根加密密钥，可以将服务加密与客户密钥一同使用。 使用客户密钥，客户可以使用本地硬件服务模块 (HSM) 或 AKV (生成自己的加密密钥) 。 客户根密钥存储在 AKV 中，可在 AKV 中用作加密客户邮箱数据或文件的密钥链之一的根。 客户根密钥只能由 Microsoft 联机服务代码间接访问，用于数据加密，并且不能由 Microsoft 员工直接访问。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与加密和密钥管理相关的控件的验证，请参阅下表。

### <a name="azure-and-dynamics-365"></a>Azure 和 Dynamics 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1：加密控件 <br> A.18.1.5：加密控件 | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1：加密控件 <br> A.18.1.5：加密控件 | 2020 年 12 月 2 日 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6：通过公共数据传输网络传输的 PII 加密 | 2020 年 12 月 2 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | DS-1：安全存储加密证书和密钥 <br> DS-2：客户数据在传输过程中加密 <br> DS-3：在传输中加密的 Azure 组件的内部通信 <br> DS-4：加密控件和过程 | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-8：传输机密性和完整性 <br> SC-13：加密的使用 <br> SC-28：保护其余信息 <br>  | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1：加密控件 <br> A.18.1.5：加密控件 | 2021 年 4 月 20 日 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6：通过公共数据传输网络传输的 PII 加密 | 2021 年 4 月 20 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44：传输数据加密 <br> CA-54：静态数据加密 <br> CA-62：客户密钥邮箱加密 <br> CA-63：客户密钥数据删除 <br> CA-64：客户密钥 | 2020 年 12 月 24 日 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16：客户加密密钥 <br> CUEC-17：客户密钥保管库 <br>  CUEC-18：客户密钥轮换| 2020 年 12 月 24 日 |
