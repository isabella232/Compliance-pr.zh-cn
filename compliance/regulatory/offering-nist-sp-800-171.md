---
title: NIST SP 800-171
description: Microsoft 云服务遵守 NIST SP 800-171 准则，保护非 (信息系统中) 的未分类信息。
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
ms.openlocfilehash: bce6847fe4c0cd1541348b70aadacc9c13238c31
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158325"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>关于 NIST SP 800-171

美国国家标准和技术协会 NIST () 并维护度量标准和指南，以帮助保护联邦机构的信息和信息系统。 为响应关于管理受控未分类信息 (CUI) 的 13556 号行政命令，发布了 [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final)，保护非法信息系统和组织中的受控未分类 *信息*。 CUI 定义为数字和物理信息，由政府 (或代表实体创建的信息) 虽然未分类，但仍非常敏感，需要保护。

NIST SP 800-171 最初于 2015 年 6 月发布，此后已多次更新，以响应不断变化的网络威胁。 它提供有关如何安全访问、传输 CUI 以及将 CUI 存储在非系统信息系统和组织的准则;其要求分为四个主要类别：

- 管理和保护的控件和过程
- 监视和管理 IT 系统
- 为最终用户明确做法和过程
- 技术和物理安全措施的实施

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft 和 NIST SP 800-171

经认可的第三方评估组织，即，由用户 Secureinfo 和 Coalfire 与 Microsoft 合作，证明其范围内云服务在处理 CUI 时符合 NIST SP 800-171 中的保护受控未分类信息 *(CUI)* 中的条件。 [Microsoft 实施 FedRAMP](offering-fedramp.md)要求有助于确保 Microsoft 范围内云服务符合或超过 NIST SP 800-171 的要求，同时使用已实施的系统和做法。

NIST SP 800-171 要求是 NIST SP 800-53（FedRAMP 使用的标准）的子集。 NIST SP 800-171 的附录 D 提供了其 CUI 安全要求与 NIST SP 800-53 中相关安全控件的直接映射，已在 FedRAMP 计划下评估和授权其范围内云服务。

处理或存储美国政府 CUI 的任何实体（ 教育机构、咨询公司、制造承包商）都必须符合 NIST SP 800-171 的严格要求。 此证明意味着 Microsoft 范围内云服务可以容纳希望部署 CUI 工作负载的客户，同时保证 Microsoft 完全合规。 例如，在信息系统内使用范围内 Microsoft 云服务处理、存储或传输"覆盖的防御信息"的所有 DoD 承包商都符合美国国防部 DFARS 条款，这些条款要求遵守 NIST SP 800-171 的安全要求。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- Azure Commercial， Azure Government
- Dynamics 365 美国政府版
- Intune
- Office 365美国政府社区云 (GCC) 、Office 365 GCC高和 DoD

## <a name="azure-dynamics-365-and-nist-sp-800-171"></a>Azure、Dynamics 365 和 NIST SP 800-171

有关 Azure、Dynamics 365 和其他在线服务合规性的信息，请参阅 Azure [NIST SP 800-171 产品/服务](/azure/compliance/offerings/offering-nist-800-171)。

## <a name="office-365-and-nist-sp-800-171"></a>Office 365 和 NIST SP 800-171

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **GCC** | 活动源服务、必应 服务、Delve、Exchange Online、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink |
| **GCC 高级** | 活动源服务、必应 服务、Exchange Online、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、 
SharePoint联机、Skype for Business、Windows Ink |
| **DoD** | 活动源服务、必应 服务、Exchange Online、智能服务、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、Microsoft Teams、SharePoint Online、Skype for Business、Windows Ink |

### <a name="frequently-asked-questions"></a>常见问题解答

**能否将 Microsoft 与 NIST SP 800-171 一同用于我的组织？**

能。 Microsoft 客户可以使用独立第三方评估组织 (3PAO) 报告中描述的有关 FedRAMP 标准的审核控制措施，作为其自己的 FedRAMP 和 NIST 风险分析和资格限定工作的一部分。 这些报告证实 Microsoft 在其范围内云服务中实施的控制措施的有效性。 客户有责任确保其 CUI 工作负载符合 NIST SP 800-171 准则。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>使用 Microsoft 合规性管理器评估风险

[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。 合规性管理器提供了一个高级模板，用于对此法规建立评估。 在合规性管理器的“**评估模板**”页面中找到模板。 了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。

### <a name="resources"></a>资源

- [Microsoft DoD 认证符合 NIST 800-171 要求](offering-DoD-DISA-L2-L4-L5.md)
- [NIST 800-171 合规性从网络安全文档开始](https://www.nist800171.com/)
- [Microsoft 云服务 FedRAMP 授权](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [NIST 800-171 3.3 审核和责任与Office 365 GCC高](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft 和 NIST 网络安全框架](offering-nist-csf.md)
- [Microsoft 政府云](https://www.microsoft.com/enterprise/government)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
