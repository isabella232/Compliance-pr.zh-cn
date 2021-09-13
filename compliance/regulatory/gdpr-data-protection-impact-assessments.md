---
title: 数据保护影响评估
description: 这些文档为数据控制者相关信息，帮助他们确定是否需要 DPIA 以及要包含的详细信息。
keywords: 数据保护影响评估, DPIA, Dynamics 365, Microsoft 专业服务, Microsoft 365, Microsoft 365 文档, GDPR
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
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: c634e1c63a123232f600cbe085964cf9d2e366a9
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158778"
---
# <a name="data-protection-impact-assessment-for-the-gdpr"></a>GDPR 规定的数据保护影响评估

一般数据保护条例 (GDPR) 引入了新规定，适用于向欧盟 (EU) 民众提供商品和服务的组织，或收集并分析欧盟居民相关数据的组织。无论你或你的企业位于何处，都要遵守这些新规定。 如需了解更多详情，可以参阅 [GDPR 摘要主题](gdpr.md)。 本文档介绍了 GDPR 规定在使用 Microsoft 产品和服务时执行的数据保护影响评估 (DPIA)。

## <a name="terminology"></a>术语

本文档中使用的 GDPR 术语的有用定义：

- *数据控制者（控制者）*：单独或与他人共同确定个人数据处理目的和方法的法人、公共机关、机构或其他团体。  
- *个人数据* 和 *数据主体*：与已识别或可识别的自然人（数据主体）相关的任何信息；可识别的自然人是可以直接或间接识别的自然人。  
- *处理者*：代表控制者处理个人数据的自然人或法人、公共机关、机构或其他团队。  
- *客户数据*：在企业日常运营中生成和存储的数据。

## <a name="what-is-a-dpia"></a>什么是 DPIA？

GDPR 要求，数据控制者必须准备对“可能会对自然人的权利和自由造成高风险”的操作执行数据保护影响评估 (DPIA)。 Microsoft 产品和服务不需要创建 DPIA。 不过，由于 Microsoft 产品和服务可高度自定义，因此是否需要创建 DPIA 具体视 Microsoft 配置详细信息而定。 Microsoft 无法控制此类信息，几乎或根本不了解此类信息。 作为数据控制者，你必须确定此类数据的正确使用。

## <a name="dpia-in-action"></a>DPIA 演示

DPIA 指南适用于 Office 365、Azure、Dynamics 365 以及 Microsoft 支持部门和专业服务。该指南包括以下几方面的考虑：

**何时需要 DPIA？**

在考虑是否完成 DPIA 时，应考虑下列风险因素。 每个指南的第 1 部分中介绍了其他潜在因素和更多详细信息。  

- 基于自动化处理的系统而广泛的数据评估。  
- 大规模地处理特殊类别的数据（揭示唯一识别自然人的信息的数据），或与刑事犯罪和违法行为相关的个人数据。
- 大规模地系统监视公开区域。

GDPR 声明如下：“如果涉及由个体医生、其他医疗保健专业人员或律师来处理患者或客户的个人数据，则个人数据的处理不应视为处理大量数据。在这种情况下，数据保护影响评估不应是强制性的。”

**完成 DPIA 需要什么？**

DPIA 应提供预期处理的具体信息，详见指南的第 2 部分。该信息包括：

- 评估与 DPIA 目的相关的数据处理必要性和合理性。  
- 评估对自然人的权利和自由造成的风险。
- 旨在消除风险的预期措施（包括安全措施和机制），以确保保护个人数据并证明 GDPR 合规性。
- 处理目的  
- 处理的个人数据类别  
- 数据保留  
- 个人数据的位置和传输  
- 与第三方下级处理者分享的数据  
- 与独立第三方分享的数据  
- 数据主体权利

## <a name="additional-considerations"></a>其他注意事项

下面介绍了可能与 Microsoft 实现相关的具体详情。

- [Office 365](gdpr-dpia-office365.md)：本文档适用于 Office 365 应用程序和服务，包括但不限于 Exchange Online、SharePoint Online、Yammer、Skype for Business 和 Power BI。 有关详细信息，请参阅表 [1](/microsoft-365/compliance/gdpr-dpia-office365#part-1--determining-whether-a-dpia-is-needed) 和表 [2](/microsoft-365/compliance/gdpr-dpia-office365#part-2--contents-of-a-dpia)。  
- [Azure](gdpr-dpia-azure.md)：我们鼓励客户与其隐私官和法律顾问合作，共同确定与使用 Microsoft Azure 相关的任何 DPIA 的必要性和内容。  
- [Dynamics 365](gdpr-dpia-dynamics.md)：DPIA 的内容可能因你使用的 Dynamics 365 工具而异。 有关具体详细信息，请参阅[第 2 部分 - DPIA 内容](/microsoft-365/compliance/gdpr-dpia-dynamics#part-2--contents-of-a-dpia)。
- [Windows](/compliance/regulatory/gdpr-dpia-windows)：本文档适用于[Windows 诊断数据处理器配置](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)。 我们鼓励客户与其隐私官和法律顾问合作，共同确定与使用 Windows 诊断数据处理器配置相关的任何 DPIA 的必要性和内容。
- [Microsoft 支持和专业服务](gdpr-dpia-prof-services.md)：专业服务不会执行特定例程或自动数据处理，也不会处理特殊类别或执行便于或需要监视可公开访问数据的任务。 有关详细信息，请参阅[第 1 部分 - 确定是否需要 DPIA](/microsoft-365/compliance/gdpr-dpia-prof-services#part-1--determining-whether-a-dpia-is-needed)。 控制者必须在专业服务的特定实现和使用上下文中，考虑上面概述的 DPIA 元素以及其他任何相关因素。 有关专业服务信息，请参阅[第 2 部分 - DPIA 内容](/microsoft-365/compliance/gdpr-dpia-prof-services#part-2--contents-of-a-dpia)。

## <a name="learn-more"></a>了解详细信息

- [Microsoft 信任中心](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
