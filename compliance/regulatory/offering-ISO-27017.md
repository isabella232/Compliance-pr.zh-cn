---
title: ISO/IEC 27017:2015 信息安全控制措施行为守则
description: Microsoft 云服务已实施此信息安全控制措施行为守则。
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
ms.openlocfilehash: b17c7629918bdf4386ad24d28c6cb6687728603c
ms.sourcegitcommit: deff41bc5085d0da42c33dd6d1672be0724a067c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/26/2021
ms.locfileid: "58561350"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a>ISO/IEC 27017:2015 信息安全控制措施行为守则

## <a name="iso-iec-27017-overview"></a>ISO-IEC 27017 概述

ISO/IEC 27017:2015 行为守则专为组织设计，用作在根据 ISO/IEC 27002:2013 实施云计算信息安全管理系统时选择云服务信息安全控制措施的参考。 此外，云服务提供商还可将其用作实施公认的保护控制措施的指南文档。

此国际标准基于 ISO/IEC 27002 提供了特定于云的附加实施指南，并针对 ISO/IEC 27002:2013 第 5-18 条中特定于云的信息安全威胁和风险提供了附加控制措施、实施指南和其他信息。 具体来说，此标准提供了 ISO/IEC 27002 中有关 37 个控制措施的指南，以及在 ISO/IEC 27002 中未重复的 7 个新控制措施。 这些新控制措施可解决以下重要方面：

- 云计算环境中的共享角色和职责
- 合同终止时删除和退回云服务客户资产
- 保护客户的虚拟环境并将其与其他客户的虚拟环境分离
- 强化要求以满足业务需求的虚拟机
- 云计算环境的管理操作程序
- 使客户能够监视云计算环境中的相关活动
- 协调虚拟和物理网络的安全管理

## <a name="microsoft-and-isoiec-27017"></a>Microsoft 和 ISO/IEC 27017

ISO/IEC 27017 在为云服务提供商和云服务客户提供指南方面是独一无二的。 此外，它还为云服务客户提供有关预期从云服务提供商获得内容的实用信息。 通过确保客户了解云中的共同职责，他们可以直接从 ISO/IEC 27017 中受益。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- [Azure、Azure 政府和 Azure 德国](https://aka.ms/AzureCompliance)
- Microsoft Cloud App Security
- [Dynamics 365、Dynamics 365 和 Dynamics 365 德国](https://aka.ms/d365-compliance-list)
- Intune
- Microsoft Defender for Endpoint
- Microsoft Graph
- Microsoft 医疗保健机器人
- [Microsoft 托管桌面](/microsoft-365/managed-desktop/intro/compliance)
- Office 365、Office 365 美国政府版、Office 365 美国政府国防部版和 Office 365 德国版
- Power Automate (以前称为 Microsoft Flow) 云服务，作为独立服务提供，或者随 Office 365 或 Dynamics 365 品牌计划或套件一并提供
- PowerApps 云服务，作为独立服务提供，后者随 Office 365 或 Dynamics 365 品牌计划或套件一并提供
- Power BI 云服务，作为独立服务提供，或者随 Office 365 品牌计划或套件一并提供
- Power BI Embedded
- Windows 365

## <a name="azure-dynamics-365-and-iso-270172015"></a>Azure、Dynamics 365 和 ISO 27017:2015

有关 Azure、Dynamics 365 和其他联机服务合规性的详细信息，请参阅 [Azure ISO 27017 产品/服务](/azure/compliance/offerings/offering-iso-27017)。

## <a name="office-365-and-iso-270172015"></a>Office 365 和 ISO 27017:2015

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **商业** | Access Online、Azure Active Directory、Azure 通信服务、合规性管理器、客户密码箱、Delve、Exchange Online、Exchange Online Protection、Forms、Griffin、身份管理器、密码箱 (Torus)、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 高级合规版附加产品、Office 365 客户门户、Office 365 微服务（包括但不限于 Kaizala、ObjectStore、Sway、PowerPoint Online 文档服务、查询批注服务、学校数据同步、Siphon、语音、StaffHub、可扩展应用程序计划）、Office 365 安全与合规中心、Office Online、Office Pro Plus、Office 服务基础结构、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、使用客户密钥进行服务加密、SharePoint Online、Skype for Business、Stream |
| **GCC** | Azure Active Directory、Azure 通信服务、合规性管理器、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |
| **GCC 高级** | Azure Active Directory、Azure 通信服务、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business |
| **DoD** | Azure Active Directory、Azure 通信服务、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365 审核、报告和证书

作为 ISO/IEC 27001:2013 认证过程的一部分，每年都会对 Microsoft 云服务进行 ISO/IEC 27017:2015 行为守则审核。

- [Office 365: ISO 27001、27018 和 27017 审核评估报告](https://aka.ms/o365isoreport)

### <a name="frequently-asked-questions"></a>常见问题解答

**此标准适用于哪些人员？**

此行为守则为云服务提供商和云服务客户提供控制措施和实施指南。 其格式结构类似于 ISO/IEC 27002:2013。

**在哪里可以查看 Microsoft 的 ISO/IEC 27017:2015 合规性信息？**

你可以下载适用于 Azure、Intune 和 Power BI 的 [ISO/IEC 27017:2015 证书](https://aka.ms/azureiso27017)。

**能否在我所在组织的认证过程中使用 Microsoft 服务的 ISO/IEC 27017 合规性认证？**

正确。 如果你的企业正在寻求对任何 Microsoft 范围内企业云服务中部署的实施流程进行认证，则可以在你的合规性评估中利用 Microsoft 的相关认证。 但是，你需要负责聘请评估方来评估合规性政策的实施情况，以及所在组织中的控制措施和流程。

**如何获得适用审核报告的副本？**

[服务信任门户](https://aka.ms/stphelp)提供独立第三方审核报告和其他相关文档。 你可以使用门户下载和查看本文档以就自己的法规要求获得帮助。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>使用 Microsoft 合规性管理器评估风险

[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。 合规性管理器提供了一个高级模板，用于对此法规建立评估。 在合规性管理器的“**评估模板**”页面中找到模板。 了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。

### <a name="resources"></a>资源

- [ISO/IEC 27017:2015 行为守则](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [Microsoft 在线服务条款](https://aka.ms/Online-Services-Terms)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
