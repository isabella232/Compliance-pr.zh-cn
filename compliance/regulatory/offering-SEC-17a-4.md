---
title: 美国证券交易Exchange委员会 (美国) 规则 17a-4 (4) 美国
description: 独立评估公司验证了 Azure 和 Office 365可以帮助金融公司满足 SEC 规则 17a-4 (f) 记录保留和不可变存储要求。
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
ms.openlocfilehash: d92fc7b56d2c240588b90afad6a82264fde911c5
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384322"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>美国证券交易Exchange委员会 (美国) 规则 17a-4 (4) 美国

## <a name="about-sec-rule-17a-4f"></a>关于 SEC 规则 17a-4 (f) 

美国[证券交易Exchange委员会 (SEC) ](https://www.sec.gov/)是美国政府的独立机构，是美国证券交易委员会的主要监管机构和监管机构。 它行使对联邦证券法的强制执行权限，提出新的证券规则，并监督证券行业的市场监管。

SEC 对选择在电子存储媒体上保留书籍和记录的受管制实体定义了严格和明确的要求。 它建立了 [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) 和 [17 CFR 240.17a-4，](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) 以监管证券经纪人的记录保管（包括保留期）。 随后 [，SEC](https://www.sec.gov/rules/interp/34-47806.htm) 修正了 17 CFR 240.17a-4 段落 (f) ，明确发布两个解释性版本，以允许书籍和记录在电子存储媒体上保留，只要满足某些条件。

如果电子存储系统在所需的保留期内阻止更改或清除记录，它将满足这些条件。 根据记录类型，保留期从 3 到 6 年，前两年要求立即访问。 此外，其中一个解释性版本要求存储系统能够保留超过 SEC 建立的保留期的记录，以遵守副发、法定保留或其他此类要求。

## <a name="microsoft-and-sec-rule-17a-4f"></a>Microsoft 和 SEC 规则 17a-4 (f) 

金融服务客户（代表全球监管最严格的行业之一）受复杂的规定约束，如在不可擦除和不可修改的状态保留财务交易和相关通信。 最规范的就是美国证券交易委员会 (Exchange SEC) 的条例 17a-4 (f) ，该规则对选择在电子存储媒体上保留书籍和记录的受管制实体规定了严格的要求。 存储的记录必须防篡改，在指定保留期之后才能更改或删除它们。

Microsoft Azure使用策略锁定存储保留锁定的不可变 Blob Microsoft Office 365 可帮助金融机构满足 SEC 规则 17a-4 (f) 的不可变存储要求。

为了评估 Azure 和 Office 365是否符合 SEC 规则 17a-4 (f) ，Microsoft 保留了一家专门负责记录管理和信息管理的独立评估公司 Cohasset Associates。 在生成的报告中：

- **Azure：SEC** [17a-4 (f) 合规性评估：Microsoft Azure 存储](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)，Cohasset 验证了使用策略锁定选项的 Azure 不可变 [Blob 存储（](/azure/storage/blobs/storage-blob-immutable-storage)用于以不可擦除和不可重写的 (WORM) 格式保留基于时间的 Blob）符合 SEC 规则的不可变存储要求。 每个 Blob (记录) 在要求的保留期到期且任何关联的合法保留解除之前，防止其被修改、覆盖或删除。 具有敏感工作负载的软件提供商和合作伙伴现在可依赖 Azure 不可变 blob 存储作为一种主要云解决方案，用于记录保留和不可变存储。 金融机构现在可以构建自己的应用程序，以利用这些功能，同时保持合规性。
- **Microsoft 365：** 对于 SEC [17a-4 (f)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d)要求，Cohasset 验证了 Microsoft 365 包括存档功能，这些功能允许受管制客户（包括代理经销商）以可帮助其遵守 SEC 记录保留要求的方式存储数据。 电子邮件中的Microsoft 365功能有助于保留各种数据，包括电子邮件、语音邮件、共享文档、即时消息和第三方数据。 特别是，Microsoft 365中的存档功能使客户能够设置全局或细化邮件保留策略，以存储已定义时间段及以后不可重写、不可擦除格式的数据。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内云平台&服务

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>审核、报告和证书

### <a name="azure--sec-rule-17"></a>Azure & SEC 规则 17

[SEC 17a-4 (f) & CFTC 1.31 (c-d) 合规性Azure 存储](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC 规则 17

[SEC 17a-4 (f) 合规性评估：& 具有 SharePoint、OneDrive、Teams、Exchange 和 Skype for Business 的 Microsoft 安全与合规Skype for Business](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=2dc92867-5f83-49d8-ad04-9e7295c9e40e&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>如何实现

### <a name="financial-services-regulation"></a>金融服务法规

云计算和 Microsoft 在线服务的关键美国法规原则的合规性地图。 [了解更多](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>风险评估&合规性指南

创建 Microsoft 云服务风险评估和监管机构通知的治理模型。 [了解更多](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>财务用例

使用案例概述、教程和其他资源来构建适用于金融服务的 Azure 解决方案。 [了解更多](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>使用 Microsoft 合规性管理器评估风险

[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。 合规性管理器提供了一个高级模板，用于对此法规建立评估。 在合规性管理器的“**评估模板**”页面中找到模板。 了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。

## <a name="resources"></a>资源

- [存档Microsoft Office 365、数据保留和规则 17a-4 中的存档](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
- [合规性 Microsoft 金融服务](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [合规性计划 Microsoft 商业云服务和金融服务](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Azure 中的金融服务合规性](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Azure 金融服务云风险评估工具](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365保留策略](/office365/securitycompliance/retention-policies)
- [Microsoft 金融服务Community](https://techcommunity.microsoft.com/t5/financial-services/ct-p/FinancialServices)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
