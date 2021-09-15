---
title: 支付卡行业 (PCI) 数据安全标准 (DSS)
description: Azure、SharePoint Online 和 OneDrive for Business 符合支付卡行业数据安全标准 Level 1 3.2 版。
keywords: Microsoft 365, 合规性, 产品/服务
ms.localizationpriority: high
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 63303389fc8fae69b9a6803a513efeb1281f781e
ms.sourcegitcommit: 4afc3ca7f8c18ae7136b4c82c572531947e82daa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/15/2021
ms.locfileid: "59349956"
---
# <a name="payment-card-industry-pci-data-security-standard-dss"></a>支付卡行业 (PCI) 数据安全标准 (DSS)

## <a name="pci-dss-overview"></a>PCI DSS 概述

支付卡行业 (PCI) 数据安全标准 (DSS) 是一种全球信息安全标准，旨在通过增强对信用卡数据的控制来预防欺诈。 如果各种规模的组织接受五大信用卡品牌（Visa、MasterCard、American Express、Discover 和 Japan Credit Bureau (JCB)）的支付卡，则他们必须遵循 PCI DSS 标准。 任何存储、处理和传输付款持卡人数据的组织都必须符合 PCI DSS。

## <a name="microsoft-and-pci-dss"></a>Microsoft 和 PCI DSS

Microsoft 由经认可的合格安全性评估师 (QSA) 完成 PCI DSS 年度评估。 审核员审查了 Microsoft Azure、Microsoft OneDrive for Business 和 Microsoft SharePoint Online 环境，其中包括验证基础结构、开发、操作、管理、支持和范围内服务。 PCI DSS 根据交易量指定了四个级别的合规性。 Azure、OneDrive for Business 和 SharePoint Online 被认证为符合 PCI DSS 3.2 版的 Service Provider Level 1（成交量最高，每年超过 600 万）。

通过该评估，我们获得了可向客户提供的合规性证明 (AoC) 和 QSA 颁发的合规性报告 (RoC)。 合规性的有效期开始于通过审核并收到评审员的 AoC，并于签署该 AoC 之日起一年后失效。 

希望开发持卡人环境或卡处理服务的客户可以在许多底层部分中使用这些验证，从而减少获取自己的 PCI DSS 认证的相关工作和成本。

重要的是要明白，Azure、OneDrive for Business 和 SharePoint Online 的 PCI DSS 合规性状态不会自动转化为客户在这些平台上构建或托管的服务的 PCI DSS 认证。客户有责任确保他们达到 PCI DSS 要求的合规性。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- Azure 与 Azure 政府
- Intune
- Microsoft 云应用安全
- [Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- Microsoft Graph
- Office 365
- OneDrive for Business 和 SharePoint Online（仅限美国）
- PowerApps 云服务，作为独立服务提供，或者随 Office 365 或 Dynamics 365 品牌计划或套件一并提供
- Power Automate（作为独立服务提供，或者随 Office 365 或 Dynamics 365 品牌计划或套件一并提供）
- Power BI 云服务，作为独立服务提供，或者随 Office 365 品牌计划或套件一并提供

## <a name="azure-dynamics-365-and-pci-dss"></a>Azure、Dynamics 365 和 PCI DSS

有关 Azure、Dynamics 365 和其他联机服务合规性的详细信息，请参阅 [Azure PCI DSS 产品/服务](/azure/compliance/offerings/offering-pci-dss)。

## <a name="office-365-and-pci-dss"></a>Office 365 和 PCI DSS

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **商业** | OneDrive for Business（美国）、SharePoint Online（美国） |

### <a name="office-365-audit-reports-and-certificates"></a>Office 365 审核、报告和证书

- [OneDrive for Business 和 SharePoint Online PCI DSS 合规性证明 (AoC)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=f1962237-32ea-4123-939e-1c8f04d13c16&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_PCI_DSS)

### <a name="frequently-asked-questions"></a>常见问题解答

**为什么合规性证明 (AoC) 封面上写着“2018 年 6 月”？**

封面上的 2018 年 6 月是 AoC 模板发布的日期。 有关评估的日期，请参阅第 2 部分。 

**PA DSS 与 PCI DSS 之间有何关系？**

支付应用程序数据安全标准 (PA DSS) 是一套符合 PCI DSS 的要求，它取代了 Visa 的支付应用程序最佳做法，并整合了其他主要发卡机构的合规性要求。 PA DSS 帮助软件供应商开发第三方应用程序，以在卡授权或结算过程中存储、处理或传输持卡人支付数据。 零售商必须使用经 PA DSS 认证的应用程序，以有效取得 PCI DSS 合规性。 PA DSS 不适用于 Azure。

**什么是收单机构，Azure 是否使用收单机构？**

收单机构是指处理支付卡事务的银行或其他实体。 Azure 不提供支付卡处理服务，因此不使用收单机构。

**PCI DSS 适用于哪些组织和商家？**

PCI DSS 适用于任何接受、传输或存储持卡人数据的公司，不论规模或交易量如何。 也就是说，如果任何客户使用信用卡或借记卡向公司进行了支付，则会应用 PCI DSS 要求。 根据过去 12 个月内总交易量，被确认为四个级别之一的公司。 Level 1 针对一年处理的交易量超过 600 万的公司；Level 2 针对 100 万到 600 万交易量；Level 3 针对 2 万到 100 万交易量；Level 4 针对低于 2 万交易量。

**OneDrive for Business 和 SharePoint Online 是否有在美国境外实现 PCI DSS 合规性的计划？**

目前，OneDrive for Business 和 SharePoint Online 仅在美国符合 PCI-DSS 要求。 Microsoft 将评估美国以外地区的要求和时间表，并在将或如果有其他地区添加到路线图时提供更新。

**OneDrive for Business 和 SharePoint Online 的范围内是什么？**

目前，只有上载到 OneDrive for Business 和 SharePoint Online 的文件和文档符合 PCI DSS 标准。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>使用 Microsoft 合规性管理器评估风险

[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。 合规性管理器提供了一个高级模板，用于对此法规建立评估。 在合规性管理器的“**评估模板**”页面中找到模板。 了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。

### <a name="resources"></a>资源

- [支付卡行业数据安全标准委员会](https://www.pcisecuritystandards.org/)
- [PCI 数据安全标准](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-1.pdf)
- [PCI DSS 快速参考指南](https://www.pcisecuritystandards.org/documents/PCISSC%20QRG%20August%202014%20-print.pdf)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
