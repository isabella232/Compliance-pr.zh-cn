---
title: '健康信息信任联盟 (HITRUST) CSF (Common Security Framework) '
description: Azure 和 Office 365 已通过健康信息信任联盟认证 (HITRUST) Common Security Framework (CSF) 。
keywords: Microsoft 365, 合规性, 产品/服务
ms.localizationpriority: medium
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
ms.openlocfilehash: 97875374c58bf174090a9dd34f26d3e22b2b50b3
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482967"
---
# <a name="health-information-trust-alliance-hitrust-common-security-framework-csf"></a>健康信息信任联盟 (HITRUST) CSF (Common Security Framework) 

## <a name="hitrust-csf-overview"></a>HITRUST CSF 概述

健康信息信任联盟 (HITRUST) 是一家由医疗保健行业代表管理的组织。 HITRUST 创建和维护通用安全框架 (CSF) ，这是一个可认证框架，可帮助医疗保健组织及其提供商以一致且简化的方式证明其安全性和合规性。

CSF 基于 HIPAA 和 HITECH 法案，这两项美国医疗保健法对使用、披露和保护个人身份健康信息制定了相关要求，并强制执行了不相容性。 HITRUST 提供了一个基准，即标准化的合规性框架、评估和认证流程，云服务提供商和涵盖的运行状况实体可基于该基准衡量合规性。 CSF 还合并了支付卡行业数据安全标准 ([PCI-DSS](https://www.microsoft.com/trustcenter/compliance/pci) [) 、ISO/IEC 27001](https://www.microsoft.com/trustcenter/compliance/iso-iec-27001) 信息安全管理标准以及 Exchanges ([MARS-E](https://www.microsoft.com/trustcenter/compliance/mars-e)) 最低可接受风险标准等现有框架中的特定于医疗保健的安全、隐私和其他法规要求。

CSF 分为 19 个不同的域，包括终结点保护、移动设备安全性和访问控制。 HITRUST 针对这些控件证明 IT 产品/服务。 HITRUST 还根据组织、系统和法规因素调整针对组织风险的认证要求。

健康信息信任联盟 (HITRUST) CSF (Common Security Framework) 

HITRUST 提供三种保证或评估级别：自我评估、CSF 验证和 CSF 认证。 每个级别在它下面的级别上都增加了严格性。 经过 CSF 认证的最高级别的组织符合 CSF 的所有认证要求。 Microsoft Azure和Office 365是首个获得 HITRUST CSF 认证的超大规模云服务。 一家 HITRUST 评估公司（一家 HITRUST 评估公司）根据 Azure 和 Office 365实施保护敏感信息的安全、隐私和法规要求执行评估。 Microsoft 支持 HITRUST 共享责任计划。

了解如何使用 Azure 安全与合规蓝图加快 HITRUST 部署。

[下载 MICROSOFT AZURE HITRUST 客户责任矩阵 (CRM) 蓝图 v9.0d](https://servicetrust.microsoft.com/ViewPage/Blueprint?command=Download&downloadType=Document&downloadId=3ccde498-4761-4be0-be8b-cd8d379a3a4f&docTab=fc060920-cdb8-11e7-bacf-0bf52b09d912_Healthcare_Blueprint)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- Azure 与 Azure 政府
- Intune
- [Microsoft 托管桌面](/microsoft-365/managed-desktop/intro/compliance)
- Office 365

## <a name="azure-dynamics-365-and-hitrust"></a>Azure、Dynamics 365 和 HITRUST

有关 Azure、Dynamics 365 和其他联机服务合规性的信息，请参阅 [Azure HITRUST 产品](/azure/compliance/offerings/offering-hitrust)/

## <a name="office-365-and-hitrust"></a>Office 365 和 HITRUST

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **商业** | 活动源服务、必应 服务、Delve、Exchange Online Protection、Exchange Online、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 审核、报告及证书

该证书的 HITRUST CSF Office 365有效期为两年。

- [Office 365HITRUST 认证书](https://aka.ms/O365HITRUSTcertification)

### <a name="frequently-asked-questions"></a>常见问题解答

**为什么某些Office 365服务不在认证范围内？**

与其他云服务提供商相比，Microsoft 提供了最全面的产品/服务。 为了与跨地区和行业的广泛合规性产品/服务保持一致性，我们根据市场需求、客户反馈和产品生命周期，在保证工作范围内包括服务。 如果某个服务未包括在特定合规性产品的当前范围内，则组织有责任根据合规性义务评估风险并确定您处理该服务中数据的方式。 我们会持续收集客户的反馈，并与监管机构和审核员合作，扩大合规性范围以满足您的安全性和合规性需求。

**Microsoft 认证是否意味着我的组织使用 Office 365，是否符合 HITRUST CSF？**

当你将数据存储在 SaaS（如 Office 365）中时，实现合规性是 Microsoft 和组织之间的共同责任。 Microsoft 管理大多数基础结构控件，包括物理安全性、网络控件、应用程序级别控件等，并且你的组织有责任管理访问控制和保护敏感数据。 HITRUST Office 365证明 Microsoft 控制框架的合规性。 基于这一点，组织需要实现和维护自己的数据保护控件，以满足 HITRUST CSF 要求。

**Microsoft 是否为我的组织提供在使用产品时实施相应Office 365？**

是的，可以在合规性分数（跨 Microsoft 云解决方案）中查找推荐的客户操作，这些解决方案可帮助组织在使用云服务时履行复杂的合规性义务。 具体来说，对于 HITRUST CSF，建议使用合规性分数中的 NIST 800-53 和 NIST CSF 评估执行风险评估。 在评估中，我们提供了分步指南以及可用于实施数据保护控制措施的 Microsoft 解决方案。 可以在 Microsoft 合规性管理器 中了解有关 [合规性分数的更多信息](/microsoft-365/compliance/compliance-manager)。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>使用 Microsoft 合规性管理器评估风险

[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。 合规性管理器提供了一个高级模板，用于对此法规建立评估。 在合规性管理器的“**评估模板**”页面中找到模板。 了解如何在 [合规性管理器 中生成和管理评估](/microsoft-365/compliance/compliance-manager-assessments)。

### <a name="resources"></a>资源

- [HITRUST 联盟](https://hitrustalliance.net/)
- [HITRUST CSF 9.3](https://hitrustalliance.net/csf-license-agreement/)
- [了解并利用 CSF](https://hitrustalliance.net/understanding-leveraging-csf/)
- [详细了解 HITRUST 共享责任计划](https://go.microsoft.com/fwlink/p/?linkid=2100268)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
