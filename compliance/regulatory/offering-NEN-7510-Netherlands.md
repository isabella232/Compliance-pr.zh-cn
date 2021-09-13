---
title: NEN 7510
description: 荷兰组织必须证明对患者健康状况数据的控制符合 NEN 7510 标准。
keywords: Microsoft 365, 合规性, 产品/服务
ms.localizationpriority: high
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
ms.openlocfilehash: 438780ab33c99bae410218bdb54265093105c16b
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158286"
---
# <a name="nen-7510"></a>NEN 7510

## <a name="nen-7510-overview"></a>NEN 7510 概述

荷兰处理患者健康状况信息的组织必须证明对此类数据的控制及组织自身都符合 NEN 7510 标准规定的要求。 Microsoft 本身不受 NEN 7510 约束，但医疗保健部门的云客户需要确定其有关基于 Microsoft 云构建的解决方案符合 NEN 7510。 Microsoft 云服务会进行各种定期认证和审核，其中一些包括与 NEN 7510 中所规定要求密切相关的元素。

## <a name="microsoft-and-nen-75102011"></a>Microsoft 和 NEN 7510:2011

Microsoft 已分析我们当前的认证和保证声明，并且已创建 [NEN 7510 覆盖报告](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=15d5a5fa-fbb6-4ea6-8126-2a2c684ae789&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_GRC_Assessment_Reports)（可在服务信任平台上获得），该报告将这些认证和保证声明与 NEN 7510 控制措施（微软作为云服务提供商对此负责）进行了对应。 本文档可帮助客户确定他们必须实施哪些其他控制措施，以确保用于存储或处理患者健康状况信息的 Microsoft 云服务符合 NEN 7510 标准。

了解如何借助 Azure 安全性和合规性蓝图加快 NEN 7510 部署：[下载 Microsoft 云：Azure 和 Office 365 NEN7510-2011 标准覆盖用户指南](https://aka.ms/Azure-NEN7510-2011)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- Azure 与 Azure 政府
- Intune
- Office 365

## <a name="office-365-and-iso-27001"></a>Office 365 和 ISO 27001

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **商业** | Azure 信息保护， Bookings， Delve， Exchange Online， Exchange Online Protection， Kaizala， Microsoft Analytics， Microsoft Booking， Microsoft Graph， Microsoft Teams， Microsoft 待办事项网页版， MyAnalytics， Office 365 云应用安全， Office 365 组， Office 365 视频， OneDrive for Business， Planner， Power Apps， Power Automate， Power BI for Office 365， PowerApps， SharePoint Online， Skype for Business， StaffHub，Stream，Sway，Yammer Enterprise |

## <a name="audits-reports-and-certificates"></a>审核、报告和证书

- [Azure 和 Office 365 NEN 7510:2011 标准覆盖](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=15d5a5fa-fbb6-4ea6-8126-2a2c684ae789&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_GRC_Assessment_Reports)

## <a name="frequently-asked-questions"></a>常见问题

**使用 Microsoft 云服务的客户符合 NEN 7510 吗？**

证明 NEN 合规性是医疗保健组织（即“客户”）的责任。 使用云服务供应商时，客户通常要求供应商提供保证，并添加他们自己的（其他）技术和组织决策、选择和流程。 这将使得客户对 NEN 7510 合规性进行全面评估，并可将其提交到第三方审核员进行审核或获得认证。 NEN 7510 覆盖报告提供了关于 Microsoft 云服务覆盖哪些 NEN 7510 控制措施的深入分析，但这不包括端到端合规性。

**Microsoft 是否符合 NEN 7510？**

NEN 7510 合规性的责任适用于荷兰医疗保健组织。 它要求组织实施信息安全管理系统，并借助适当的技术和组织措施来应对风险。 对于作为云服务提供商角色的 Microsoft，NEN 7510 合规性不是目标，在技术上也不可行。 客户实施或使用 Microsoft 云服务时，这些服务可能在 NEN 7510 评估范围内。 但是，组织必须添加自己的（其他）控制措施、选择和流程，它们是 NEN 7510 总体评估的一部分。 该报告的目的是证明医疗保健实体可以采用符合 NEN 7510 的 Microsoft 云服务。

**此报告不显示 100% 的覆盖。NEN 7510 合规性不可行？**

Microsoft 云服务提供了很多控制措施，可帮助荷兰医疗保健组织满足其 NEN 7510 合规性需求。 但是，组织需要通过其自己的实施选择、其他技术控件和管理流程来补充这些供应商的保证。 该报告显示了适用控制措施的完整列表中超过 94% 的直接覆盖。 对于其他控制措施，Microsoft 在报告中提供了有关这些控制措施如何证明合规性的指南。

> [!NOTE]
> 实施控制措施的完整列表不是 NEN 7510 的主要目的（虽然 Microsoft Online Services 广泛覆盖确实有所帮助）。 NEN 7510 强制实施基于风险的信息安全系统，供组织用于确定适用于他们的控制措施。

**NEN 7510 覆盖报告是否是具有法律约束力的文档？**

否。 它是客户内部 NEN 7510 保证流程的支持工具，有助于建立 NEN 7510 合规性是可行的信心和信任。 该报告（由 KPMG 的独立审核员创建）属于说明性文档，并且包含法律免责声明。

**Microsoft 是否已为报告付费？**

Microsoft 已在其全球保证与 NEN 7510 标准中的控制措施之间创建了对应关系。 然后，Microsoft 聘用 KPMG 的一位独立审核员对与 NEN 7510 对应的控制措施进行独立审核，最终生成这份报告。

**我们是否可以共享此报告？**

该报告是根据保密协议 (NDA) 提供给你的，基于该协议，该报告仅供客户参考，并且不会通过 Microsoft 服务信任门户以外的其他渠道进行复制或披露。

客户可以在其合规性或保证流程中与自己的内部或外部审核员共享该报告。

## <a name="resources"></a>资源

- [关于 NEN](https://www.nen.nl/About-NEN.htm)
- [NEN 7510:2011 标准](https://www.nen.nl/NEN-Shop-2/Standard/NEN-75102011-nl.htm)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
