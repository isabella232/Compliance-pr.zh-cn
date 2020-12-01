---
title: 体系结构概述
description: 了解 Microsoft 365 中的体系结构
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
ms.openlocfilehash: 7ceceb59d0afcbc72fac9758f3de500082b8b365
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506424"
---
# <a name="architecture-overview"></a>体系结构概述

## <a name="what-is-microsoft-365"></a>什么是 Microsoft 365？

Microsoft 365 是基于云的、基于订阅的 Office、Windows 10、企业移动性 + 安全性和合规性的版本。 Microsoft 365 客户获取客户端（如 Outlook 和 Windows），它们也受益于 Microsoft 代表自己的服务，例如 Exchange Online、Microsoft 团队和 SharePoint Online。 服务的所有组件都会定期更新为订阅模型的一部分，以便我们的客户拥有 "长达" 的产品。 Microsoft 代表客户管理服务基础结构，这意味着 Microsoft 将负责保护存储客户数据的基础结构。

在规模方面，我们目前使用近达一百万台计算机来为 Microsoft 365 服务供电。 为这些服务供电的基础结构在特定于服务的硬件和虚拟化环境中因 Azure、Windows 和 Linux 以及多租户和专用平台而异。 Microsoft 365 是一个全球性的业务，基础结构分布在世界各地的数据中心中，使我们的客户能够满足数据派驻和主权要求。

简言之，该服务非常复杂，以惊人的规模运行，并且需要数千个 Microsoft 工程师才能生成和维护。 我们将此基础结构的所有保护保持安全，这是我们的头等大事。

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Microsoft 365 如何确保客户租户之间的隔离？

Microsoft 的云服务在假定所有租户都可能会与所有其他租户建立恶意。 为了正确地将租户相互隔离，Microsoft 实现了各种隔离技术和控制。 这些控制措施旨在防止信息泄露或未经授权访问跨租户的客户数据，并防止一个租户的操作对另一个租户的服务产生不利影响。

在 Microsoft 365 租户中，使用 Azure Active Directory (Azure AD) 以逻辑方式隔离客户内容。 Microsoft 365 中的用户身份验证不仅验证用户身份，而且还验证用户帐户所属的租户标识，从而阻止用户访问其租户环境外部的数据。 若要对 Azure AD 的逻辑隔离进行补充，客户内容将始终在 rest 和途进行加密。 单个服务还可以提供其他层的租户隔离，例如在单独的加密数据库中对租户数据隔离的 SharePoint Online。

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>如何避免单一故障点的 Microsoft 365 工程师弹性服务？

Microsoft 设计和构建云服务，以最大限度地提高可靠性并最大限度地减少对正常操作的故障和挑战的客户面临的负面影响。 此策略首先是连接地理分散的数据中心的网络的设计。 Microsoft 的网络体系结构包括直接互连和多个网络路径。 Microsoft 365 服务利用此冗余来自动路由失败的流量，以提高服务质量。

在服务级别，Microsoft 365 的恢复策略优先于软件弹性。 只要有可能，我们的服务将通过自动服务运行状况监视部署到主动/主动配置中，从而使服务能够在无人干预的情况下检测和恢复许多常见故障和故障。 除了主动/主动配置之外，Microsoft 365 服务可确保服务在单独的故障区域中部署，从而防止一个区域中的故障影响其他区域的可用性，从而提高了容错能力。

数据恢复通过保护 Microsoft 365 服务中的数据的完整性和可用性来补充服务弹性。 我们的服务使用本地存储冗余和地域冗余将客户数据的副本复制到不同的故障区域中。 如果一个故障区域中的数据已损坏或丢失，则可以在另一个容错区域中访问它，而不会丢失可用性。 自动完整性检查会自动恢复受多种物理或逻辑损坏影响的数据。 Microsoft 365 还为客户提供了用于在 Exchange Online 和 SharePoint Online 中恢复客户意外删除或修改的数据的工具。

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Microsoft 365 如何跟踪依赖项并防止未经授权的外部系统连接？

Microsoft 365 服务团队将关键系统组件及其依赖项标识为业务连续性管理的一部分。 此外，Microsoft 365 文档和跟踪所有外部系统连接，以确保仅允许在网络防火墙配置中获得授权连接。 Microsoft 365 的信息安全体系结构中记录了 microsoft 365 系统、依赖项和外部连接。 信息安全体系结构和相应的数据流图表都会至少每年进行一次评审和更新，以及对系统进行重大更改的情况。

Microsoft 365 体系结构将定期进行验证，并使用基于云的工具自动进行验证，以验证与安全原则的协调并持续测试隔离和恢复功能。 体系结构验证可用于自动识别服务的当前状态从所需状态偏差的实例，并标记所有用于检查和缓解的偏差。 体系结构验证的目标是确保服务基础结构的安全功能继续按预期运行。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 请参阅下表，以验证与 Microsoft 365 体系结构相关的控制措施。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | AC-4：信息流实施 <br> CP-9：信息系统备份 <br> PL-8：信息安全体系结构 <br> SC-7：边界保护 <br> SC-22：体系结构和预配 | 2020年9月24日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 6：信息安全组织 <br> . 13.1：网络安全管理 <br> 17.2：冗余 | 2020 年 2 月 22 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 6：信息安全组织 <br> . 13.1：网络安全管理 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-37：租户隔离 <br> CA-49：备份策略 <br> CA-51：数据复制 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-05：数据流图表 <br> CA-37：租户隔离 <br> CA-49：备份策略 <br> CA-51：数据复制 | 2019 年 9 月 30 日 |