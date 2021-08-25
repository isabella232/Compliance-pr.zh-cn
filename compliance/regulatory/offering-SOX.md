---
title: 2002 年萨班尼斯-奥克斯莱法案 (Sarbanes-Oxley Act of 2002, SOX)
description: 金融服务公司可以使用 Microsoft 合规性报告来解决其遵守《Sarbanes-Oxley法的问题。
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
ms.openlocfilehash: 375f7a58db675f3f14bd98ff580919ef40f603f1
ms.sourcegitcommit: 16cec8f7ca799a415bfbae937b177a628a0f2987
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/24/2021
ms.locfileid: "58505885"
---
# <a name="sarbanes-oxley-act-of-2002-sox"></a>2002 年萨班尼斯-奥克斯莱法案 (Sarbanes-Oxley Act of 2002, SOX)

## <a name="sox-overview"></a>SOX 概述

SOX [2002 年萨班斯-奥克斯利法案 (](https://www.congress.gov/bill/107th-congress/house-bill/3763) SOX) 是美国联邦法律，由美国证券交易委员会Exchange美国 (监管[](https://www.sec.gov/)) 。 此外，SOX 还要求公开交易公司具有适当的内部控制结构，以验证其财务报表是否准确反映其财务结果。 SOX 受到客户内部流程的严重影响，尤其是在控制财务报告方面。 例如，SOX 要求涉及内部客户控制措施，用于准备和审阅财务报表，尤其是影响与财务信息相关的重大更改的准确性、完整性、有效性和公开披露的控制措施。

SEC 不定义或实施 SOX 认证过程。 相反，它为上市公司提供了广泛的准则，以确定如何遵守 SOX 报告要求。

## <a name="microsoft-and-sox"></a>Microsoft 和 SOX

遵守 Sarbanes-Oxley 法案 (SOX) 的 Microsoft 云服务客户可以使用 MICROSOFT 在履行自己的 SOX 合规义务时从独立审计公司收到的 SOC 1 类型 2 证明。 此证明适用于报告对财务信息进行的内部控制。

即使没有针对云服务提供商的 SOX 认证或验证，Microsoft 也可以帮助客户履行 SOX 义务。 例如，SOX 要求对准备和审阅财务报表进行内部控制，尤其是影响与财务信息相关的重大更改的准确性、完整性、有效性和公开披露的控制措施。 为帮助公司，Microsoft 维护了适用于跨各种服务组合报告此类控件的 SOC 1 类型 2 证明，这些服务组合可用于构建各种应用程序。 它基于美国注册公共会计协会 (AICPA) 18 (SSAE 18) 标准声明和国际标准保障服务活动 No。 3402（ISAE 3402）。  (此证明取代了 SAS 70.) 

第三方审核公司生成的审核报告证实 Microsoft 控制措施设计正确，在指定的日期运行，且在指定的时段内有效运行。 客户可以审阅报告，了解 Microsoft 控制措施目标及其控制措施的有效性，并访问补充控制措施。

在 Microsoft，我们与客户共同承担合规性责任。 我们提供有关合规性计划的详细信息，您可以通过向认证第三方请求详细的审核结果来验证这些细节。 但是，最终由你决定我们的服务是否符合适用于你的业务的特定法律和法规。 例如，有一些与 SOX 相关的安全控件（如用户访问云资源）属于你的责任：你的组织必须开发这些控件的适当审核，作为 SOX 合规性的一部分。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- Azure
- [Dynamics 365](https://aka.ms/d365-compliance-list)
- Intune
- Office 365
- Power BI 云服务（作为独立服务提供，或者随 Office 365 品牌计划或套件一并提供）

## <a name="azure-dynamics-365-and-sox"></a>Azure、Dynamics 365 和 SOX

随着云采用的发展，越来越多的客户正在探索如何将受 SOX 合规性义务限制的应用程序和工作负载迁移到云。 即使没有针对云服务提供商的 SOX 认证或验证，Azure 也可以帮助你履行 SOX 义务。

如果需遵守 SOX 合规义务，应查看 Azure [SOC 1 类型 2](./offering-soc-1.md)证明，根据以下要求执行：

- SSAE 编号。 18，证明标准：阐明和重新编纂，包括 AT-C 第 320 部分， *对与用户实体财务报告的内部控制相关的服务组织中的控制检查进行报告* （AICPA、专业标准）。
- SOC 1 对与用户实体财务报告的内部控制相关的服务组织中的控制检查进行报告（AICPA 指南）。

AICPA SSAE 18 标准取代了 SAS 70，适用于报告服务组织中与用户实体对金融服务的内部控制相关的控制措施。 这是在向在 Azure 上部署的资产履行自己的行业特定合规性义务时，你可以依赖的第三方技术服务提供商审查的正式审核。 它包括审核员有关控制有效性的意见，以在指定的监视期间实现相关控制目标。

此外，Azure 还生成 [了](https://azure.microsoft.com/resources/microsoft-azure-guidance-for-sarbanes-oxley-sox/) 指南文档，可帮助你在履行自己的 SOX 合规义务时使用 Azure 的现有合规性报告。 它利用将 SOX 相关应用程序迁移到 Azure 的内部 Microsoft 体验。 此外，本指南还提供迁移最佳做法，包括 SOX 合规性含义、对两个公开提供的案例研究的回顾以及从 Microsoft 内部迁移项目中获得的经验。

## <a name="office-365-and-sox"></a>Office 365 和 SOX

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **商业** | 扩充循环、自动替换文字、 Azure 信息保护、二进制转换服务、Bookings、Delve、文档项、编辑器、Exchange Online、表单、插入联机媒体、Insights、Kaizala、Microsoft Analytics、Microsoft Booking、Microsoft Graph、Microsoft Teams、MyAnalytics、Office 365 云应用安全、Office 365 组、Office 365 视频、OneDrive for Business、Planner、Power Apps、PowerApps、Power Automate、Power BI、PowerPointDesigner、PowerPoint Online Document Service、SharePoint Online、Skype for Business、StaffHub、Stream、Sway、微软待办、Web 呈现服务Yammer Enterprise  |

### <a name="audits-reports-and-certificates"></a>审核、报告和证书

[SOC 1 针对：](offering-SOC.md)

- Azure 和 Power BI
- Dynamics 365
- Office 365

### <a name="frequently-asked-questions"></a>常见问题解答

**如何使用 Microsoft SOX 合规性促进我的组织的合规性流程？**

当你将应用程序和数据迁移到涵盖的 Microsoft 云服务时，你可以基于 Microsoft 保留的证明和认证来构建。 独立审核员报告证明 Microsoft 为帮助维护数据的安全性和隐私而实施的控制措施的有效性。 但是，你完全负责确保组织遵守所有适用的法律和法规。

### <a name="resources"></a>资源

- [Azure 合规性文档](/azure/compliance/)
- [Azure 实现合规性世界](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [Microsoft 365合规性产品/服务](/compliance/regulatory/offering-home)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
- [2002 年萨班斯-奥克斯利法案 (](https://www.congress.gov/bill/107th-congress/house-bill/3763) SOX) 
- [美国证券交易Exchange委员会](https://www.sec.gov/) (SEC) 
- [Microsoft 云金融服务资源](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Microsoft 云金融服务合规性计划](https://aka.ms/FSCP-Print)
- [云计算法规原则和 Microsoft 在线服务的合规性地图](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [Microsoft 云中金融机构的风险评估和合规性指南](https://azure.microsoft.com/resources/risk-assessment-and-compliance-guide-for-financial-institutions-in-the-microsoft-cloud-/)
- [金融服务行业用例](/azure/industry/financial/)
