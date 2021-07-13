---
title: 联邦风险和授权管理项目 (FedRAMP)
description: Microsoft 被授予美国联邦风险和授权管理计划 P-ATOS 和 ATOS。
keywords: Microsoft 365, 合规性, 产品/服务
localization_priority: None
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
ms.openlocfilehash: d9b7988b2ab236a26aad0981879f9b49c9ed028a
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384942"
---
# <a name="federal-risk-and-authorization-management-program-fedramp"></a>联邦风险和授权管理项目 (FedRAMP)

## <a name="fedramp-overview"></a>FedRAMP 概述

建立美国联邦风险和授权管理计划 (FedRAMP) 以提供一种标准化方法，用于根据联邦信息安全管理法案 (FISMA) 评估、监视和授权云计算产品和服务，并加速联邦机构采用安全的云解决方案。

管理和Office现在要求所有联邦行政机构使用 FedRAMP 验证云服务的安全性。  (由于其他机构也采用了该标准，因此它还在公共部门的其他领域很有用。) 美国国家标准和技术协会 (NIST) SP 800-53 设置了强制性标准，建立了信息系统的安全类别（机密性、完整性和可用性）来评估在信息和信息系统受到威胁时对组织的潜在影响。 FedRAMP 是一个计划，它证明云服务提供商 (CSP) 符合这些标准。

准备向联邦机构销售服务的 CSP 可以通过三种途径来演示 FedRAMP 合规性：

- 从联合授权委员会 (联合授权) 获得临时授权以 (P-ATO) 。 JAB 是 FedRAMP 的主要管理和决策正文。 来自国防部、国防安全部和一般服务管理部门的代表负责。 该板向已证明 FedRAMP 合规性的 CSP 授予 P-ATO。
- 从联邦机构接收 (ATO) 运营授权。
- 或者，独立开发满足计划要求的云解决方案提供商提供包。

上述每个途径都需要 FedRAMP 计划管理 Office (PMO) 由经该计划认证的独立第三方组织进行评估。

FedRAMP 授权基于 NIST 准则在三个影响级别授予：低、中和高。 这些级别对丢失机密性、完整性或可用性对组织的影响进行排名：低 (有限影响) 、中等 (严重负面影响) 以及高 (严重或灾难性) 。

## <a name="microsoft-and-fedramp"></a>Microsoft 与 FedRAMP

Microsoft 政府云服务（包括 Azure 政府、Dynamics 365 政府版和 Office 365 美国政府版）符合美国联邦风险和授权管理计划 (FedRAMP) 的严格要求，使美国联邦机构能够受益于 Microsoft 云的成本节省和严格安全。

Microsoft 政府云服务为公共部门客户提供一系列与 FedRAMP 兼容的丰富服务，以及强大的指南和实施工具，包括 [FedRAMP 高](https://aka.ms/fedrampblueprint)蓝图，它帮助客户为必须实施 FedRAMP 高控制措施的任何 Azure 部署体系结构部署一组核心策略。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内云平台&服务

- Azure 与 Azure 政府
- [Dynamics 365 美国政府版](https://aka.ms/d365-compliance-list)
- Intune
- Office 365美国政府，Office 365美国政府 - 高级Office 365美国政府防御
- Power BI 云服务，作为独立服务提供，后者随 Office 365 品牌计划或套件一并提供

## <a name="azure-dynamics-365-and-fedramp"></a>Azure、Dynamics 365 和 FedRAMP

有关 Azure、Dynamics 365 和其他在线服务合规性的信息，请参阅 Azure [FedRAMP 产品](/azure/compliance/offerings/offering-fedramp)/

## <a name="office-365-and-fedramp"></a>Office 365 和 FedRAMP

- Office 365美国政府Office 365美国健康与公共服务部拥有一个 ATO， (DH DH DH) 。
- Office 365美国政府国防队具有来自美国国防信息系统局的 P-ATO， (DISA) 。 任何希望Office 365美国政府国防队的客户都可使用 DISA P-ATO 生成代理 ATO 来记录其接受。
- Office 365 (美国政府和美国政府) Office 365计划的 FEDRAMP 机构 ATO 具有来自检查员常规的 DHSP Office中等影响级别的 FedRAMP 机构 ATO。 Office 365美国政府是首个获得此授权的基于云的电子邮件和协作服务。

### <a name="office-365-cloud-environments"></a>Office 365云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365适用性和范围内服务

使用下表确定您的 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **GCC** | 活动源服务、必应 服务、Delve、Exchange Online、Exchange Online Protection、基础结构、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink |
| **GCC 高** | 活动源服务、必应 服务、Exchange Online、Exchange Online Protection、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink |
| **DoD** | 活动源服务、必应 服务、Exchange Online Protection、Exchange Online、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365审核、报告和证书

Microsoft 每年都必须重新证明其云服务，以维持其 P-ATO 和 ATO 认证。 为此，Microsoft 必须持续监视和评估其安全控制，并证明其服务的安全性保持合规性。

- [Microsoft FedRAMP 审计报告](https://aka.ms/MicrosoftFedRAMPAuditDocuments)  

### <a name="frequently-asked-questions"></a>常见问题解答

**Microsoft 云服务是否遵守 FISMA (联邦信息安全) ？**

FISMA 是联邦法律，要求美国联邦机构及其合作伙伴仅从遵守 FISMA 要求的组织采购信息系统和服务。 指示他们符合 FISMA 的多数机构及其供应商都是指它们如何满足特别出版物 800-53 修订版 4 中 NIST 标识的控制措施。 FISMA 流程 (，但基础标准本身) 于 2011 年由 FedRAMP 取代。

**FedRAMP 适用于谁？**

'FedRAMP is mandatored for federal agency cloud deployments and service models at the low and moderate risk impact levels." 任何想要参与 CSP 的联邦机构都可能需要满足 FedRAMP 规范。 此外，在美国政府使用的产品或服务中采用云技术的公司可能需要获得 ATO。

**我的代理在哪里开始自己的合规性工作？**

有关联邦机构为成功导航 FedRAMP 并满足其要求而必须执行的步骤的概述，请转到获取 [授权：代理授权](https://www.fedramp.gov/agency-authorization/)。

**能否在我的代理的授权过程中使用 Microsoft 合规性？**

是。 你可以将 Microsoft 云服务认证用作任何需要来自联邦政府机构 ATO 的计划或计划的基础。 但是，你需要为这些服务之外的组件获得自己的授权。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>使用 Microsoft 合规性管理器评估风险

[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。 合规性管理器提供了一个高级模板，用于对此法规建立评估。 在合规性管理器的“**评估模板**”页面中找到模板。 了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。

### <a name="resources"></a>资源

- [联邦风险和授权管理计划](https://www.fedramp.gov/)
- [FedRAMP 安全评估框架](https://www.fedramp.gov/assets/resources/documents/FedRAMP_Security_Assessment_Framework.pdf)
- [在 Microsoft 管理云中的合规性](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft 政府云](https://go.microsoft.com/fwlink/p/?linkid=2087246)
