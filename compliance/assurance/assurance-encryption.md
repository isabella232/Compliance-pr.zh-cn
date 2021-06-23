---
title: 加密和密钥管理概述
description: 了解加密和密钥管理Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 5e46fdb5ddc3b1b80df0bcadf9054b9353a0dc8e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088641"
---
# <a name="encryption-and-key-management-overview"></a>加密和密钥管理概述

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>加密在保护客户内容方面扮演什么角色？

大多数 Microsoft 商业云服务都是多租户的，这意味着客户内容可能存储在与其他客户相同的物理硬件上。 为了保护客户内容的机密性，Microsoft 365使用一些最强且最安全的加密协议对静态和传输中的所有数据进行加密。

加密不能替代强访问控制。 Microsoft 365的访问控制策略 Zero Standing Access (ZSA) 保护客户内容免受 Microsoft 员工未经授权的访问。 加密通过保护存储任何位置的客户内容机密性以及防止在 Microsoft 365 系统之间传输时或在 Microsoft 365 与客户之间传输内容来补充访问控制。

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>如何Microsoft 365对其余数据进行加密？

所有客户内容Microsoft 365一种或多种加密形式进行保护。 Microsoft 服务器使用 BitLocker 在卷级别加密包含客户内容的磁盘驱动器。 BitLocker 提供的加密可保护客户内容，以防其他过程或控件 (例如，访问控制或硬件) 的回收可能会导致对包含客户内容的磁盘进行未经授权的物理访问。

Exchange Online、Microsoft Teams、SharePoint Online 和 OneDrive for Business 还使用应用程序层的服务加密来加密客户内容。 服务加密提供权限保护以及强加密保护的管理功能。 它还允许在操作系统Windows由这些操作系统存储或处理的客户数据之间分离。

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>如何Microsoft 365传输数据加密？

Microsoft 365服务使用强传输协议（如 TLS）来防止未经授权的方在客户数据通过网络移动时窃听客户数据。 传输数据的示例包括正在传递的邮件、联机会议中的对话或在数据中心之间复制的文件。

在Microsoft 365中，每当用户设备与 Microsoft 服务器或 Microsoft 服务器与另一台服务器通信时，数据都被视为"正在传输"。 Exchange Online、SharePoint Online、Microsoft Teams 和 Office Online 均使用 TLS 来确保数据在传输过程中保持机密性。

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>如何Microsoft 365用于加密的密钥？

强加密仅与用于加密数据的密钥一样安全。 Microsoft 使用自己的安全证书加密传输数据的 TLS 连接。 对于静态数据，受 BitLocker 保护的卷使用全卷加密密钥进行加密，该密钥使用卷主密钥进行加密，而卷主密钥又绑定到服务器中的受信任的平台模块 (TPM) 。 BitLocker 使用符合 FIPS 的算法来确保从不会以清晰方式通过线路存储或发送加密密钥。

服务加密为 Exchange Online、Microsoft Teams、SharePoint Online 和 OneDrive for Business 中的静态客户数据提供了另一层OneDrive for Business。 服务加密为客户提供了两种加密密钥管理选项：Microsoft 管理的密钥或客户密钥。 使用 Microsoft 管理的密钥时，Microsoft 365自动生成并安全存储用于服务加密的根密钥。

具有控制自己的根加密密钥的要求的客户可以使用服务加密和客户密钥。 使用客户密钥，客户可以使用本地硬件服务模块 (HSM) 或 AKV (生成自己的) 。 客户根密钥存储在 AKV 中，可在 AKV 中用作加密客户邮箱数据或文件的密钥链之一的根。 客户根密钥仅可通过数据Microsoft 365代码间接访问，并且不能由 Microsoft 员工直接访问。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与加密和密钥管理相关的控件的验证，请参阅下表。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | SC-8：传输机密性和完整性 <br> SC-13：加密的使用 <br> SC-28：保护其余信息 <br>  | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1：加密控件 <br> A.18.1.5：加密控件 | 2021 年 4 月 20 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1：加密控件 <br> A.18.1.5：加密控件 | 2021 年 4 月 20 日 |
| [ISO 27018 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6：通过公共数据传输网络传输的 PII 加密 | 2021 年 4 月 20 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44：传输数据加密 <br> CA-54：静态数据加密 <br> CA-62：客户密钥邮箱加密 <br> CA-63：客户密钥数据删除 <br> CA-64：客户密钥 | 2020 年 12 月 24 日 |
| [SOC 3 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16：客户加密密钥 <br> CUEC-17：客户密钥保管库 <br>  CUEC-18：客户密钥轮换| 2020 年 12 月 24 日 |
