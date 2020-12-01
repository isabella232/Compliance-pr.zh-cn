---
title: 加密和密钥管理概述
description: 了解 Microsoft 365 中的加密和密钥管理
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
ms.openlocfilehash: 96a3871657dc1e6021949ca9fc2376df382fe15b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506285"
---
# <a name="encryption-and-key-management-overview"></a>加密和密钥管理概述

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>加密在保护客户内容中扮演什么角色？

大多数 Microsoft 商业云服务都是多租户的，这意味着客户内容可以存储在与其他客户相同的物理硬件上。 为了保护客户内容的机密性，Microsoft 365 使用一些最强和最安全的加密协议来加密静态和传输中的所有数据。

加密不是强大的访问控制的替代方案。 Microsoft 365 的访问控制策略 of Zero ZSA Access (的) 保护客户内容免受 Microsoft 员工的未经授权的访问。 加密通过在 Microsoft 365 系统之间或 Microsoft 365 与客户之间进行传输时防止内容被阅读，来保护客户内容的机密性，从而补充了访问控制。

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Microsoft 365 如何对数据进行静态加密？

Microsoft 365 中的所有客户内容都受一个或多个加密形式的保护。 Microsoft 服务器使用 BitLocker 在卷级加密包含客户内容的磁盘驱动器。 BitLocker 提供的加密可在其他进程或控件发生失误时保护客户内容 (例如，对硬件) 的访问控制或回收，从而导致对包含客户内容的磁盘的未经授权的物理访问。

Exchange Online、Microsoft 团队、SharePoint Online 和 OneDrive for Business 也会在应用程序层使用服务加密来加密客户内容。 服务加密在强加密保护的顶层提供了权限保护和管理功能。 它还允许在 Windows 操作系统和由这些操作系统存储或处理的客户数据之间进行分离。

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Microsoft 365 如何加密数据传输？

Microsoft 365 产品和服务使用强大的传输协议（如 TLS）防止未经授权的参与方在客户数据通过网络移动时窃听。 传输中的数据示例包括正在传递的邮件、联机会议中发生的对话或在数据中心之间复制的文件。

在 Microsoft 365 中，只要用户的设备与 Microsoft 服务器通信或 Microsoft 服务器与另一台服务器通信，数据就会被视为 "在传输中"。 Exchange Online、SharePoint Online、Microsoft 团队和 Office Online 都使用 TLS，以确保数据在传输过程中保持机密。

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Microsoft 365 如何管理用于加密的密钥？

强加密只与用于加密数据的密钥一样安全。 Microsoft 使用其自己的安全证书对 TLS 连接进行数据传输。 对于静态数据，受 BitLocker 保护的卷使用完整的卷加密密钥进行加密，该密钥使用批量主密钥进行加密，而批量主密钥又绑定到服务器中 (TPM) 的受信任的平台模块。 BitLocker 使用符合 FIPS 标准的算法，以确保不会以明文形式在线路中存储或发送加密密钥。

服务加密为 Exchange Online、Microsoft 团队、SharePoint Online 和 OneDrive for Business 中的客户静态数据提供了额外的加密层。 服务加密为客户提供了两个加密密钥管理选项： Microsoft-托管密钥或客户密钥。 使用 Microsoft 管理的密钥时，Microsoft 365 服务会自动生成并安全地存储用于服务加密的根密钥。

如果客户具有控制其自己的根加密密钥的要求，则可以利用客户密钥进行服务加密。 使用客户密钥，客户可以使用本地硬件服务模块 (HSM) 或 Azure Key Vault (AKV) 生成自己的加密密钥。 客户根密钥存储在 AKV 中，在这些密钥中，它们可用作加密客户邮箱数据或文件的 keychains 之一的根。 客户根键只能由 Microsoft 365 服务代码间接访问以进行数据加密，Microsoft 员工无法直接访问它们。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 请参阅下表以验证与加密和密钥管理相关的控件。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | SC-8：传输机密性和完整性 <br> SC-13：使用加密 <br> SC-28：静态信息保护 <br>  | 2020年9月24日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | . 10.1：加密控件 <br> 18.1.5：加密控件 | 2020 年 2 月 22 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | . 10.1：加密控件 <br> 18.1.5：加密控件 | 2020 年 2 月 22 日 |
| [ISO 27018 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 11.6：通过公共数据传输网络传输的 PII 加密 | 2020 年 2 月 22 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-44：数据传输加密 <br> CA-54：静态数据加密 <br> CA-62：客户密钥邮箱加密 <br> CA-63：客户密钥数据删除 <br> CA-64：客户密钥 | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-16：客户加密密钥 <br> CUEC-17：客户密钥存储库 <br>  CUEC-18：客户密钥轮换| 2019 年 9 月 30 日 |
