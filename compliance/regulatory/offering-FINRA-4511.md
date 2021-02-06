---
title: 金融行业监管机构 (FINRA) 条例 4511 (c) 美国
description: 独立评估公司验证了 Azure 和 Office 365 可以帮助金融公司满足 FINRA 规则 4511 记录保留和不可变存储要求。
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
ms.openlocfilehash: f4a26a88ca742178d894b5e46d0372d91babba66
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120841"
---
# <a name="financial-industry-regulatory-authority-finra-rule-4511c-united-states"></a>金融行业监管机构 (FINRA) 条例 4511 (c) 美国

## <a name="about-finra-rule-4511"></a>关于 FINRA 规则 4511

[金融行业监管局 (FINRA) ](https://www.finra.org/#/)是监管美国超过 4，500 家经纪人公司的金融机构的最大独立机构。 它获得美国消费者协会授权，"通过确保代理制造行业能够公平且有希望地运营来保护美国的经纪人。"

2011 年，美国证券交易委员会 (SEC) 批准 FINRA 采用用于管理电子存储媒体上的书籍和记录的保留的 SEC 规则。 [FINRA 规则 4511 (c) ](https://www.finra.org/sites/default/files/NoticeDocument/p123548.pdf) 指定"符合 FINRA 规则的所有书籍和记录应采用符合 SEA (证券交易法案) 条例 17a-4 的格式和媒体进行保留。"

此外，FINRA 条例 4511 (c) 要求公司将那些根据适用的 FINRA 或 SEA 规则没有指定保留期的书籍和记录至少保留六年。 实际上，如果书籍和记录与帐户相关，则要求在帐户关闭后保留 6 年。 否则，保留期为创建此类书籍和记录后的 6 年。

## <a name="microsoft-and-finra-rule-4511c"></a>Microsoft 和 FINRA 规则 4511 (c) 

金融服务客户代表了世界上监管最严格的行业之一，需遵守复杂的规定，如在不可擦除和不可修改的状态保留财务交易和相关通信。 其中包括金融行业监管局 (FINRA) 的规则 4511，该法规对选择在电子存储介质上保留书籍和记录的受监管实体规定了严格的要求。 存储的记录必须防篡改，在指定保留期之后才能更改或删除它们。

具有策略锁定的 Microsoft Azure 不可变 Blob 存储Microsoft Office具有保留锁定的 Microsoft Office 365 可帮助金融机构满足 FINRA 规则 4511 (c) 。

## <a name="microsoft-azure"></a>Microsoft Azure

为了评估 Azure 是否符合 FINRA 规则 4511 (c) ，Microsoft 保留了一家专门负责记录管理和信息管理的独立评估公司 Cohasset Associates。 生成的报告 [SEC 17a-4 (f) & CFTC 1.31 (c-d) 合规性评估：Microsoft Azure 存储](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)包含 Azure 对 FINRA 规则 4511 (c) 的合规性，该规则遵守 SEC 规则 17a-4 (f) 的格式和媒体要求。

Cohasset 验证了使用策略锁定选项的 Azure 不可变 [Blob](/azure/storage/blobs/storage-blob-immutable-storage) 存储（用于以不可擦除和不可重写的 (WORM) 格式保留基于时间的 Blob）满足相关的 FINRA 存储要求。 每个 Blob (记录) 在要求的保留期到期且任何关联的合法保留已解除之前，都受到保护，防止其被修改、覆盖或删除。

具有敏感工作负载的软件提供商和合作伙伴现在可以依赖 Azure 不可变 Blob 存储作为记录保留和不可变存储的一条一步商店云解决方案。 金融机构现在可以构建自己的应用程序，以利用这些功能，同时保持合规性。

## <a name="microsoft-365"></a>Microsoft 365

对于 FINRA 规则 [4511 (c) ](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) 要求，Cohasset 验证了 Microsoft 365 包括存档功能，这些功能使受监管客户（包括经纪人）能够以有助于他们遵守 SEC 记录保留要求的方式存储数据。 Microsoft 365 中的保留功能有助于保留各种数据，包括电子邮件、语音邮件、共享文档、即时消息和第三方数据。 特别是，Microsoft 365 中的存档使客户能够设置全局或精细的邮件保留策略，以不可重写、不可擦除的格式存储已定义时段及之后的数据。

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft 范围内云服务

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>审核、报告和证书

### <a name="azure--finra-rule-4511c"></a>Azure & FINRA 规则 4511 (c) 

[SEC 17a-4 (f) & CFTC 1.31 (c-d) Azure 存储合规性评估](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--finra-rule-4511c"></a>Office 365 & FINRA 规则 4511 (c) 

[Office 365 中的存档、数据保留和 SEC 规则 17a-4 合规性](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)

## <a name="how-to-implement"></a>如何实现

- **金融服务法规**：针对云计算和 Microsoft 在线服务的关键美国法规原则的合规性地图。 [了解更多](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- **风险评估和合规性指南**：针对 Microsoft 云服务风险评估和监管机构通知创建一个管理模型。 [了解更多](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- **金融用例**：在案例概述、教程和其他资源的帮助下构建适合金融服务的 Azure 解决方案。 [了解更多](/azure/industry/financial/)

## <a name="resources"></a>资源

- [Microsoft 金融服务合规性计划](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Microsoft 商业云服务和金融服务](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Azure 中的金融服务合规性](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Azure 金融服务云风险评估工具](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365 保留策略](/office365/securitycompliance/retention-policies)
- [Microsoft 金融服务博客](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
