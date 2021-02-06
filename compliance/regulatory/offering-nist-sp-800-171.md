---
title: NIST SP 800-171
description: Microsoft 云服务遵守 NIST SP 800-171 指南，以保护非 (信息系统中) CUI 中受控的未分类信息。
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
ms.openlocfilehash: da5e2621969ff9cd4ce2778fa7f075522454aef7
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121111"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>关于 NIST SP 800-171

美国国家标准与技术协会 (NIST) 并维护度量标准和指南，以帮助保护联邦机构的信息和信息系统。 为响应有关管理受控未分类信息 (CUI) 的管理命令 13556，发布了 [NIST SP 800-171，](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final)保护非安全信息系统和组织中的受控未分类 *信息*。 CUI 定义为数字和物理信息，由政府 (或代表其实体创建) 虽然未分类，但仍敏感且需要保护。

NIST SP 800-171 最初于 2015 年 6 月发布，此后已多次进行更新，以响应不断变化的网络威胁。 它提供有关如何安全访问、传输 CUI 以及将 CUI 存储在非信息系统和组织的准则;其要求分为四个主要类别：

- 用于管理和保护的控件和过程
- 监视和管理 IT 系统
- 针对最终用户的清晰做法和过程
- 技术和物理安全措施的实施

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft 和 NIST SP 800-171

经认可的第三方评估组织，即，与 Microsoft 合作，证明其范围内云服务符合 NIST SP 800-171 中的条件，即处理 CUI 时，保护非 *Federing Information Systems* and Organizations 中的受控未分类信息 (CUI) 。 [Microsoft 实现 FedRAMP](offering-fedramp.md)要求有助于确保 Microsoft 范围内云服务符合或超过 NIST SP 800-171 的要求，同时使用已实施的系统和做法。

NIST SP 800-171 要求是 NIST SP 800-53（FedRAMP 使用的标准）的子集。 NIST SP 800-171 附录 D 提供了其 CUI 安全要求与 NIST SP 800-53 中相关安全控件的直接映射，其中范围内云服务已在 FedRAMP 计划下进行评估和授权。

处理或存储美国政府 CUI 的任何实体（教育机构、咨询公司、制造承包商）都必须符合 NIST SP 800-171 的严格要求。 此证明意味着 Microsoft 范围内云服务可以容纳希望部署 CUI 工作负载的客户，同时保证 Microsoft 完全合规。 例如，所有使用信息系统内 Microsoft 云服务处理、存储或传输"覆盖的防御信息"的 DoD 承包商都符合美国国防部的 DFARS 条款，这些条款要求遵守 NIST SP 800-171 的安全要求。

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft 范围内云服务

- [Azure 政府](https://aka.ms/AzureCompliance)
- [Azure 商业](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)
- [Dynamics 365 美国政府版](https://aka.ms/d365-compliance-list)
- Intune
- [Office 365 美国政府社区云 (GCC) 、Office 365 GCC High 和 DoD](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>审核、报告和证书

- [符合 NIST SP 800-171 的 Azure 政府证明](https://aka.ms/Azure-NIST-800-171)

## <a name="how-to-implement"></a>如何实现

- [Azure 蓝图示例](/azure/governance/blueprints/samples/)：获取对实现符合基于 NIST 的控件的工作负荷的支持。

## <a name="frequently-asked-questions"></a>常见问题

**能否将 Microsoft 合规性与 NIST SP 800-171 一起用于我的组织？**

是的。 Microsoft 客户可以使用来自独立第三方评估组织 (3PAO) 的报告中所述的经审核的控制措施，作为自己的 FedRAMP 和 NIST 风险分析和资格鉴定工作的一部分。 这些报告证明 Microsoft 在其范围内云服务中实施的控制措施的有效性。 客户有责任确保其 CUI 工作负载符合 NIST SP 800-171 准则。

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>使用 Microsoft 合规性管理器评估风险

[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。 合规性管理器提供了一个高级模板，用于对此法规建立评估。 在合规性管理器的“**评估模板**”页面中找到模板。 了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。

## <a name="resources"></a>资源

- [Microsoft DoD 认证符合 NIST 800-171 要求](offering-DoD-DISA-L2-L4-L5.md)
- [NIST 800-171 合规性从网络安全文档开始](https://www.nist800171.com/)
- [Microsoft 云服务 FedRAMP 授权](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [使用 Office 365 GCC High 的 NIST 800-171 3.3 审核和责任](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft 和 NIST 网络安全框架](offering-nist-csf.md)
- [Microsoft 政府云](https://www.microsoft.com/enterprise/government)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
