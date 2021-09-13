---
title: 美国证券交易Exchange美国 (美国) 规则 17a-4 (4) SEC
description: 一家独立的评估公司验证了 Azure 和 Office 365 可以帮助金融公司满足 SEC 规则 17a-4 (f) 记录保留和不可变存储要求。
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
ms.openlocfilehash: 50c44b6801e15af02bf4bfa4f4d46758b7a6c7a8
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158890"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>美国证券交易Exchange美国 (美国) 规则 17a-4 (4) SEC

## <a name="about-sec-rule-17a-4f"></a>关于 SEC 规则 17a-4 (f) 

美国[证券交易Exchange委员会 (SEC) ](https://www.sec.gov/)是美国政府的独立机构，是美国证券交易的主要监管机构和监管机构。 它行使对联邦证券法的强制执行权限，提出新的证券规则，并监督证券行业的市场监管。

SEC 对选择在电子存储媒体上保留书籍和记录的受管制实体定义了严格和明确的要求。 它建立了 [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) 和 [17 CFR 240.17a-4，](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) 以监管证券经纪人的记录保管（包括保留期）。 随后 [，SEC](https://www.sec.gov/rules/interp/34-47806.htm) 修正了 17 CFR 240.17a-4 第 (f) 段，明确发布两个解释性版本，以允许书籍和记录在电子存储媒体上保留，只要满足某些条件。

如果电子存储系统在所需的保留期内阻止更改或清除记录，它将满足这些条件。 根据记录类型，保留期从 3 到 6 年，前两年要求立即访问。 此外，其中一个解释性版本要求存储系统能够保留超过 SEC 建立的保留期的记录，以遵守副发、法定保留或其他此类要求。

## <a name="microsoft-and-sec-rule-17a-4f"></a>Microsoft 和 SEC 规则 17a-4 (f) 

金融服务客户（代表全球监管最严格的行业之一）受复杂的规定约束，如在不可擦除和不可修改的状态保留财务交易和相关通信。 最规范的就是美国证券交易委员会 (SEC) 条例 17a-4 (f) ) Exchange，该规则对选择在电子存储媒体上保留书籍和记录的受管制实体规定了严格的要求。 存储的记录必须防篡改，在指定保留期之后才能更改或删除它们。

Microsoft Azure使用策略存储的不可变 Blob Microsoft Office 365 和具有保留锁定的 Blob 存储可帮助金融机构满足 SEC 规则 17a-4 (f) 的不可变存储要求。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="independent-assessments"></a>独立评估

为了评估 Azure 和 Office 365是否符合 SEC 规则 17a-4 (f) ，Microsoft 保留了一家专门负责记录管理和信息管理的独立评估公司 Cohasset Associates。

### <a name="azure"></a>Azure

[Azure Blob](/azure/storage/blobs/storage-blob-immutable-storage) 存储的不可变存储使用户能够在一次写入中存储业务关键 (WORM) 状态。 此状态使数据在用户指定的间隔内不可擦除和不可修改。 在保留间隔内，可创建和读取 blob，但不能修改或删除 blob。 Azure 不可变存储的这些功能可帮助客户满足其记录保留要求。

Microsoft 保留了一家专门负责记录管理和信息管理的独立第三方评估公司，以评估 Azure Blob 存储不可变存储是否符合 SEC 规则 17a-4 (要求) 要求。 生成的报告 *[Cohasset Assessment： Microsoft Azure WORM 存储](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)* 客户可用。

评估员认为，具有 *Azure Blob* 的不可变存储功能且基于时间锁定的策略选项的 Azure 存储以不可擦除和不可重写的格式保留基于时间的 Blob (记录) ，并满足 SEC 规则 17a-4 (f) 的相关存储要求。 [FINRA 规则 4511 (c)](offering-FINRA-4511.md)，以及 CFTC 规则 [1.31 (c) - (d](offering-cftc-1-31-us.md)) 。

根据请求，Microsoft 还将提供一份 90 天信函，要求客户在使用电子存储媒体前至少 *90* 天通知其指定的检查机构，以满足 SEC 17a-4 (f)  (2) 要求。 如该法规所规定，"成员、代理或客户必须提供其自己的表示形式，或者由存储中型供应商或其他具有适当专业知识的第三方提供，所选存储媒体满足本段 (f)  (2) 中规定的条件。" 若要获取 *Microsoft* 电子 存储 媒体服务 for SEC 规则 17a-4 的证明，具有 Azure [](https://azure.microsoft.com/support/create-ticket/)支持计划的客户可以在 [Azure](https://azure.microsoft.com/support/plans/)门户创建支持票证，并请求 SEC 规则 17a-4 的证明书。 在此文档中，Microsoft 提供与 SEC 17a-4 (f)  (2) 相关的保证。

### <a name="office-365"></a>Office 365

对于[SEC 17a-4 (f) ](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d)要求，Cohasset 验证了 Microsoft 365 包括存档功能，这些功能允许受管制客户（包括代理经销商）以一种有助于他们遵守 SEC 记录保留要求的方式存储数据。 电子邮件中的Microsoft 365功能有助于保留各种数据，包括电子邮件、语音邮件、共享文档、即时消息和第三方数据。 特别是，Microsoft 365中的存档功能使客户能够设置全局或细化邮件保留策略，以存储已定义时间段及以后不可重写、不可擦除格式的数据。

## <a name="audits-reports-and-certificates"></a>审核、报告和证书

### <a name="azure--sec-rule-17"></a>Azure & SEC 规则 17

- [SEC 17a-4 (f) & CFTC 1.31 (c-d) 合规性Azure 存储](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)

可以通过 *创建支持* 票证存储 媒体服务 Azure 支持来请求 Microsoft 针对 SEC 规则 17a-4 [的电子数据](https://azure.microsoft.com/support/create-ticket/)[证明](https://azure.microsoft.com/support/plans/)。 在此证明信中，Microsoft 提供保证，帮助客户遵守 SEC 17a-4 (f)  (2) 要求。

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC 规则 17

- [SEC 17a-4 (合规性) ：& 具有 SharePoint、OneDrive、Teams、Exchange 和 Skype for Business 的 Microsoft 安全与合规Skype for Business](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=2dc92867-5f83-49d8-ad04-9e7295c9e40e&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

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

- [ Azure 合规性文档](/azure/compliance/)
- [ Azure 实现合规性世界](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [美国证券交易Exchange委员会](https://www.sec.gov/) (美国) [规则 17a-4](https://www.sec.gov/rules/final/34-38245.txt)
- [Microsoft 云金融服务资源](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Microsoft 云金融服务合规性计划](https://aka.ms/FSCP-Print)
- [云计算法规原则和 Microsoft 在线服务的合规性地图](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [Microsoft 云中金融机构的风险评估和合规性指南](https://azure.microsoft.com/resources/risk-assessment-and-compliance-guide-for-financial-institutions-in-the-microsoft-cloud-/)
- [金融服务行业用例](/azure/industry/financial/)
- [存档Microsoft Office 365、数据保留和规则 17a-4 中的存档](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
