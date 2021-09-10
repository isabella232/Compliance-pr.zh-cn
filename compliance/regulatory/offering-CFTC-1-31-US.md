---
title: '美国商品 (委员会) CFTC 规则 1.31 (c-d) '
description: 独立评估公司验证了 Azure 和 Office 365可以帮助金融公司满足 CFTC 规则 1.31 记录保留和不可变存储要求。
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
ms.openlocfilehash: 8bb9f380d57e932576c969f10512f508de7c6ada
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947550"
---
# <a name="commodity-futures-trading-commission-cftc-rule-131c-d-united-states"></a>美国商品 (委员会) CFTC 规则 1.31 (c-d) 

## <a name="about-cftc-rule-13c-d"></a>关于 CFTC 规则 1.3 (c-d) 

美国 [商品](https://www.cftc.gov/) 贸易委员会 (CFTC) 一家独立的美国联邦机构，负责监管商品交易和选项市场，最近还监管交换市场。  
  
长期 CFTC 规则 1.31 定义了 SEC 规则 17a-4 和 f (建立的) 。 此外，还指定电子记录必须保留 5 年，并且原始记录在前两年内保持"易于访问"，并在整个保留期内由委员会或美国国防部进行检查。  
  
2017 年 [，CFTC](https://www.cftc.gov/sites/default/files/idc/groups/public/@lrfederalregister/documents/file/2017-11014a.pdf)修订了规则，修订并现代化记录保存法规，以采用描述性较低、基于原则的标准，以便更灵活地维护记录。 此修订使规则更具技术中性，使受管制实体能够选择最适合其业务的技术，同时维护"确保记录保存过程的可靠性"的安全措施。 修订后的规则删除了组织将原始记录保留两年的要求，但保留了五年维护期，这符合受 CFTC 和 SEC 监管的公司的做法。

## <a name="microsoft-and-cftc-rule-131c-d"></a>Microsoft 和 CFTC 规则 1.31 (c-d) 

金融服务客户（代表全球监管最严格的行业之一）受复杂的规定约束，如在不可擦除和不可修改的状态保留财务交易和相关通信。 最规范的一个规则是美国商品贸易委员会 (CFTC) 第 1.31 条规则，该规则对选择在电子存储媒体上保留书籍和记录的受管制实体规定了严格的要求。 存储的记录必须防篡改，在指定保留期之后才能更改或删除它们。 Microsoft Azure使用策略锁定存储使用保留锁定的不可变 Blob Microsoft Office 365 可以帮助金融机构满足 CFTC 规则 1.31 (c-d) 的存储要求。

### <a name="microsoft-azure"></a>Microsoft Azure

为了评估 Azure 是否符合 CFTC 规则 1.31 (c-d) ，Microsoft 保留了一家专门负责记录管理和信息管理的独立评估公司 Cohasset Associates。 在结果报告中[，CFTC 1.31 (c)  (d) ](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)合规性评估：Microsoft Azure 存储 ，Cohasset 验证了使用策略锁定选项的 Azure 不可变 Blob[存储（](/azure/storage/blobs/storage-blob-immutable-storage)用于以不可擦除和不可重写的 (WORM) 格式保留基于时间的 Blob）是否符合 CFTC 规则基于原则的要求。 每个 Blob (记录) 在要求的保留期到期且任何关联的合法保留解除之前，防止其被修改、覆盖或删除。 具有敏感工作负载的软件提供商和合作伙伴现在可以依赖 Azure 不可变 blob 存储作为一个一站式云解决方案来保留记录。 金融机构现在可以构建自己的应用程序，以利用这些功能，同时保持合规性。

### <a name="microsoft-365"></a>Microsoft 365

对于[CFTC 1.31 (c) - (d) ](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d)要求，Cohasset 验证了 Microsoft 365 包括存档功能，使受管制客户（包括代理经销商）能够按照有助于他们遵守 SEC 记录保留要求的方式存储数据。 Microsoft 365中的保留功能可帮助保留各种数据，包括电子邮件、语音邮件、共享文档、即时消息和第三方数据。 特别是，Microsoft 365中的存档功能使客户能够设置全局或细化邮件保留策略，以存储已定义时间段及以后不可重写、不可擦除格式的数据。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- [Azure](https://aka.ms/AzureCompliance)
- [Office 365](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>审核、报告和证书

- [Azure & CFTC 规则 1.31：SEC 17a-4 (f) & CFTC 1.31 (c-d) 合规性Azure 存储](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)
- Office 365 & CFTC 规则 1.31：Office 365中的存档、数据保留和 SEC 规则 17a-4 合规性

## <a name="how-to-implement"></a>如何实现

- [金融服务法规](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)：云计算和 Microsoft 在线服务的关键美国法规原则的合规性地图。
- [风险评估和合规性指南](https://aka.ms/RiskGovernanceGuide)：针对 Microsoft 云服务风险评估和监管机构通知创建一个管理模型。
- [金融用例](/azure/industry/financial/)：在案例概述、教程和其他资源的帮助下构建适合金融服务的 Azure 解决方案。

## <a name="resources"></a>资源

- [Microsoft 金融服务合规性计划](https://aka.ms/FSCP-Print)
- [Microsoft 商业云服务和金融服务](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
- [Azure 中的金融服务合规性](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft Office 365保留策略](/office365/securitycompliance/retention-policies)
- [Microsoft 金融服务博客](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
