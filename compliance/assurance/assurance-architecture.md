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
ms.openlocfilehash: e1b4e9701e76c1e758f683750c8ebfeda2bc1f1f
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787482"
---
# <a name="architecture-overview"></a>体系结构概述

## <a name="what-is-microsoft-365"></a>什么是 Microsoft 365？

Microsoft 365 是基于云的 Office、Windows 10、企业移动性 + 安全性和合规性的基于订阅的版本。 Microsoft 365 客户可以获取 Outlook 和 Windows 等客户端，他们还可以从 Microsoft 代表他们托管的服务（如 Exchange Online、Microsoft Teams 和 SharePoint Online）中获益。 服务的所有组件会定期作为订阅模型的一部分进行更新，以便我们的客户拥有"常青"产品。 Microsoft 代表客户管理服务基础结构，这意味着 Microsoft 负责保护存储客户数据的基础结构。

就规模而言，我们目前使用近一百万台计算机来为 Microsoft 365 服务提供电源。 支持这些服务的基础结构因 Azure、Windows 和 Linux 以及多租户和专用平台中的特定于服务的硬件和虚拟化环境而有很大差异。 Microsoft 365 是一家全球企业，我们的基础结构分布于世界各地的数据中心，使我们的客户可以满足数据驻留和权利要求。

简而言之，该服务非常复杂，运行规模之大，并且需要数千名 Microsoft 工程师进行构建和维护。 保护所有这些基础结构的安全是我们的首要任务。

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Microsoft 365 如何确保客户租户之间的隔离？

Microsoft 的云服务基于以下假设构建：所有租户都有可能危害所有其他租户。 为了正确地将租户彼此隔离，Microsoft 实施了各种隔离技术和控件。 这些控件旨在防止信息泄露或跨租户未经授权访问客户数据，并防止一个租户的操作对另一个租户的服务造成负面影响。

客户内容在逻辑上隔离在 Microsoft 365 租户内，使用 Azure Active Directory (Azure AD) 。 Microsoft 365 中的用户身份验证不仅验证用户标识，还验证用户帐户属于的租户标识，从而阻止用户访问租户环境外部的数据。 为了补充 Azure AD 的逻辑隔离，客户内容始终在其余和传输过程中加密。 个别服务还可以提供额外的租户隔离层，例如 SharePoint Online 隔离单独加密数据库中的租户数据。

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Microsoft 365 如何设计避免单点故障的复原服务？

Microsoft 设计和构建云服务以最大化可靠性，并最大限度地减少在正常操作中出现故障和难题时对客户的负面影响。 此策略从连接地理位置分散的数据中心的网络设计开始。 Microsoft 的网络体系结构包括直接互连和多个网络路径。 Microsoft 365 服务利用此冗余自动路由故障流量以提高服务质量。

在服务级别，Microsoft 365 的恢复策略优先处理软件恢复。 只要有可能，我们的服务就部署在主动/主动配置中，并自动进行服务运行状况监视，使服务可以检测和从许多常见故障中恢复，而无需人工干预。 除了主动/主动配置之外，Microsoft 365 服务还通过确保服务部署在单独的容错区域中来增加容错能力，防止一个区域中的故障影响其他区域的可用性。

数据复原通过保护 Microsoft 365 服务中数据的完整性和可用性来补充服务恢复能力。 我们的服务使用本地存储冗余和地理位置冗余将客户数据的副本复制到不同的容错区域。 如果一个故障区域中的数据已损坏或丢失，则它可以在另一个故障区域中访问，而不会丢失可用性。 自动完整性检查自动还原受多种物理或逻辑损坏影响的数据。 Microsoft 365 还为客户提供了用于还原客户在 Exchange Online 和 SharePoint Online 中意外删除或修改的数据的工具。

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Microsoft 365 如何跟踪依赖项并防止未经授权的外部系统连接？

Microsoft 365 服务团队将关键系统组件及其依赖项标识为业务连续性管理的一部分。 此外，Microsoft 365 还记录并跟踪所有外部系统连接，以确保网络防火墙配置中只允许授权连接。 Microsoft 365 的信息安全体系结构中记录了 Microsoft 365 系统、依赖项和外部连接。 信息安全体系结构和相应的数据流图将至少每年查看和更新一次，并且只要对系统进行了重大更改。

定期自动使用基于云的工具验证 Microsoft 365 体系结构，以验证是否符合我们的安全原则，并持续测试隔离和恢复能力功能。 体系结构验证可自动识别服务当前状态偏离所需状态的实例，并标记任何偏差以便进行审阅和缓解。 体系结构验证的目标是确保服务基础结构的管理功能继续正常工作。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 请参阅下表，以验证与 Microsoft 365 体系结构相关的控件。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [Office 365 (FedRAMP) ](https://compliance.microsoft.com/compliancemanager) | AC-4：信息流强制 <br> CP-9：信息系统备份 <br> PL-8：信息安全体系结构 <br> SC-7：边界保护 <br> SC-22：体系结构和设置 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6：信息安全组织 <br> A.13.1：网络安全管理 <br> A.17.2：冗余 | 2020 年 2 月 22 日 |
| [Office 365 (ISO 27017) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6：信息安全组织 <br> A.13.1：网络安全管理 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37：租户隔离 <br> CA-49：备份策略 <br> CA-51：数据复制 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05：数据流图 <br> CA-37：租户隔离 <br> CA-49：备份策略 <br> CA-51：数据复制 | 2020 年 12 月 24 日 |