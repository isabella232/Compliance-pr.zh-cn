---
title: '证券交易委员会 - 法规系统合规性和完整性 (SCI) '
description: SCI 规则适用于 SCI 实体，包括诸如股票和选项交换 (SROs) 、注册的结算机构以及 ATSs (替代交易系统等 SCI) 。
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
ms.openlocfilehash: 049f0516598209411b0c5ca47eea39140762fd3d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50119871"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>证券交易委员会：法规系统合规性和完整性 (SCI) 

## <a name="about-regulation-sci"></a>关于法规 SCI

美国证券交易委员会 (SEC) 是美国联邦政府机构的独立机构，也是美国证券交易的主要监管机构和监管机构。 它行使对联邦证券法的强制执行权限，提出新的证券规则，并监督证券行业的市场监管。

2014 年 11 月，美国证券交易委员会采用法规系统合规性和完整性 [ (SCI) ](https://www.sec.gov/rules/final/2014/34-73639.pdf) (和表单 SCI 来报告 SCI 事件) 以强化美国证券交易中的技术基础结构。 该法规旨在降低系统中断的频率、提高发生此类事件的复原能力，以及增强 SEC 对证券交易技术的监管以及法规的执行。

SCI 规则适用于 SCI 实体，包括诸如股票和选项交换 (SROs) 、注册的结算机构以及 ATSs (替代交易系统等 SCI) 。 这些规则主要监管直接支持关键证券交易功能的系统：交易、结算和结算、订单传送、市场数据、市场监管和市场监视。

## <a name="microsoft-and-sec-regulation-sci"></a>Microsoft 和 SEC 法规 SCI

美国证券交易委员会 (美国) SCI，加强运营和支持美国证券交易市场的财务组织的技术基础结构。 在 SEC 监管下，其要求旨在确保这些系统具有高可用性、强复原和低延迟 (大量邮件，且延迟) 。

为了帮助指导必须遵守此法规的金融服务客户，Microsoft 发布了 [Microsoft Azure SEC 法规系统合规性和完整性云实施指南](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)。 本文档中的指南：

- 概述了支持强复原、高可用性和低延迟的整体 Azure 功能。
- 明确 Azure 处理哪些控制区域和管理方面。 Azure 功能和服务到 SCI 要求的这种点分映射可衡量 Azure 是否符合法规框架。 它还帮助客户了解在哪里可以将安全责任转移到他们在本地运营时完全拥有的 Azure。 这些功能受 Microsoft 在 Azure SLA 中做出的承诺支持。
- 指定客户负责处理的每个法规 SCI 要求，并提供 Azure 文档和服务以帮助他们履行这些责任。

本文档提供了关键法规 SCI 重点关注的详尽清单。 此清单可帮助金融组织了解如何采用 Azure，以帮助确保监管机构、客户和领导层能够遵守适用的法规要求。

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft 范围内云服务

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>如何实现

- [法规 SCI 实施指南](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)：根据法规映射 Azure 功能，并详细介绍合规性的共同责任。
- [设计可靠的 Azure 应用程序](/azure/architecture/resiliency/)：简要概述如何将可靠性构建到 Azure 应用程序设计的每个步骤中。
- [设计高度可用的应用程序](/azure/storage/common/storage-designing-ha-apps-with-ragrs)：开发人员如何有助于确保其 Azure 存储应用程序高度可用。
- [风险评估和合规性指南](https://aka.ms/RiskGovernanceGuide)：针对 Microsoft 云服务风险评估和监管机构通知创建一个管理模型。

## <a name="frequently-asked-questions"></a>常见问题

**使用云技术时，共同责任意味着什么？**

随着计算环境从本地数据中心转移到云中的数据中心，安全性的责任也会转移，云服务提供商 (CSP) 客户现在共同承担该责任。 对于每个应用程序和解决方案，该责任中有多少由客户承担，以及云解决方案提供商的多少取决于客户部署的 Azure 模型：IaaS、SaaS 或 PaaS。 客户有责任了解他们实施所需安全控制的责任程度。 但是，Microsoft 提供了帮助客户导航此复杂动态的指南。 有关详细信息，请阅读 [云计算的共享责任](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91)。

**哪些金融机构可以利用 Azure 帮助满足法规 SCI 要求？**

受此法规保护的财务组织或 SCI 实体可以部署 Azure。 SEC 表示其法规适用于"自监管组织 (SROs) ，包括股票和选项交换、注册的结算机构、FINRA 和 MSRB、替代交易系统 (ATSs) 、交易超过指定批量阈值的 NMS 和非 NMS 股票、合并市场数据传播者 (计划处理者) 和某些豁免结算机构。"

## <a name="resources"></a>资源

- [SEC 对有关法规 SCI 的常见问题的响应](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [BCDR (业务连续性和灾难恢复) ：Azure 配对区域](/azure/best-practices-availability-paired-regions)
- [云计算法规原则和准则的合规性Microsoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Microsoft 云金融服务合规性计划](https://aka.ms/FSCP-Print)
- [Azure 中的金融服务合规性](https://aka.ms/FinServ-Compliance-Azure)
- [Microsoft 金融服务](https://aka.ms/FinServ-Compliance)
- [Microsoft 和 SEC 规则 17a-4](offering-SEC-17a-4.md)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
