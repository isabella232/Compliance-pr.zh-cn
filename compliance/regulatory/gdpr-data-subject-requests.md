---
title: 针对 GDPR 和 CCPA 的数据主体请求
keywords: Microsoft 365, Microsoft 365 教育版, Microsoft 365 文档, GDPR, CCPA
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
description: 了解如何使用 Microsoft 产品和服务，在一般数据保护条例 (GPDR) 和加州消费者隐私法案 (CCPA) 下完成 DSR。
ms.custom: seo-marvel-mar2020
hideEdit: true
ms.openlocfilehash: b5ef9464a686a5f2c8823f196408fd71026fa52d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158882"
---
# <a name="data-subject-requests-and-the-gdpr-and-ccpa"></a>针对 GDPR 和 CCPA 的数据主体请求

一般数据保护条例 (GDPR) 引入了新规定，适用于向欧盟 (EU) 民众提供商品和服务的组织，或收集并分析欧盟居民相关数据的组织。无论你或你的企业位于何处，都要遵守这些新规定。 有关其他详细信息，请参阅 [GDPR 摘要主题](gdpr.md)。

同样，加州消费者隐私法案 (CCPA) 规定了加州消费者的隐私权和义务，包括与 GDPR 的数据主体权利类似的权利，例如删除、访问和接收（可移植性）其个人信息的权利。  CCPA 还就某些披露规定了在选择行使权限时防止歧视的保障措施，并就分类为“销售”的特定数据传输提出了“选择退出/选择加入”要求。 本文档介绍了如何根据 GDPR 和 CCPA 使用 Microsoft 产品和服务来完成数据主体请求 (DSR)。

- [Office 365](gdpr-dsr-Office365.md)
- [Azure](gdpr-dsr-Azure.md)
- [Intune](gdpr-dsr-Intune.md)
- [Dynamics 365](gdpr-dsr-Dynamics365.md)
- [Visual Studio 系列产品](gdpr-dsr-visual-studio-family.md)
- [Azure DevOps Services](gdpr-dsr-vsts.md)
- [Microsoft 支持和专业服务](gdpr-dsr-prof-services.md)

## <a name="terminology"></a>术语

本文档中使用的 GDPR 术语的有用定义：

- *数据控制者（控制者）*：单独或与他人共同确定个人数据处理目的和方法的法人、公共机关、机构或其他团体。  
- *个人数据* 和 *数据主体*：与已识别或可识别的自然人（数据主体）相关的任何信息；可识别的自然人是可以直接或间接识别的自然人。  
- *处理者*：代表控制者处理个人数据的自然人或法人、公共机关、机构或其他团队。  
- *客户数据*：在企业日常运营中生成和存储的数据。

## <a name="what-is-a-dsr"></a>什么是 DSR？

根据一般数据保护条例 (GDPR)，用户（在条例中称为“数据主体”）有权管理由雇主或其他类型机构或组织（称为“数据控制者”或简称为“控制者”）收集的个人数据。根据 GDPR，数据主体有权对自己的个人数据执行以下操作：获取个人数据副本、请求更改个人数据、限制个人数据处理、删除个人数据或接收电子格式的个人数据，以便于转移给其他控制者。

加州消费者隐私法案 (CCPA) 规定了加州消费者的隐私权和义务，包括与 GDPR 的数据主体权利类似的权利，例如删除、访问和接收（可移植性）其个人信息的权利。  

作为控制者，你有义务迅速考虑每个 DSR，并通过执行所请求的操作或解释控制者为什么无法接受 DSR 来提供实质性响应。 控制者应咨询自己的法律顾问或合规顾问，以决定如何妥善处置任何给定 DSR。

根据组织的 GDPR 合规性规定，完成 DSR 可能涉及多个过程。
  
- **发现**。 确定完成 DSR 所需的数据的过程。
- **访问**。 检索数据，并可能将已发现的信息传输给数据主体。
- **校正**。 实现更改或其他请求的个人数据更改。
- **限制**。 通过限制访问或从 Microsoft 云中删除数据，更改对个人数据的访问或处理。
- **导出**。 根据 GDPR 的“数据可移植性权利”，向数据主体提供“结构化的计算机可读常用格式”个人数据。
- **删除**。 从 Microsoft 云中永久删除个人数据。

## <a name="specific-dsr-considerations"></a>具体 DSR 注意事项

### <a name="insights-generated-by-microsoft-products-or-services"></a>Microsoft 产品或服务生成的见解

MyAnalytics 等服务可能会生成[见解](/microsoft-365/compliance/gdpr-dsr-office365#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365)。Office 365 包括，向使用它们的用户和组织提供见解的联机服务。 这些服务生成的数据可能会产生与 DSR 相关的个人数据。 请单击下面列表中的链接，详细了解服务专属 DSR 过程。  

### <a name="dsrs-for-system-generated-logs"></a>针对系统生成日志发出的 DSR

Microsoft 生成的日志和相关数据可能包含，根据 GDPR 的“个人数据”定义被视为个人数据的数据。 不支持限制或校正系统生成日志中的数据。 系统生成日志中的数据由 Microsoft 云内执行的实际操作和诊断数据构成；修改会泄漏操作历史记录，并增加欺诈和安全风险。 Microsoft 支持访问、导出和删除完成 DSR 所必需的系统生成日志。 此类数据的示例可能包括：  

- 产品和服务使用情况数据，例如用户活动日志
- 用户搜索请求和查询数据
- 由系统功能以及用户或其他系统的交互产生的产品和服务生成数据。  

### <a name="yammer-and-kaizala"></a>Yammer 和 Kaizala

删除用户帐户将删除 Yammer 和 Kaizala 的系统生成日志。若要从这些应用程序中删除数据，请参阅以下资源之一：

- [管理 Yammer Enterprise 中的 GDPR 数据主体请求](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)
- [导出或删除用户在 Kaizala 中的组织数据](/office365/kaizala/export-or-delete-a-user-s-data)

### <a name="national-clouds"></a>国家云

在一些国家云中，全局 IT 管理员需要删除系统生成日志。

### <a name="microsoft-services"></a>Microsoft 服务

如果组织或用户与 Microsoft 交互以获取与 Microsoft 产品和服务相关的支持，部分此类数据可能包含个人数据。 有关详细信息，请参阅[符合 GDPR 的 Microsoft 支持和专业服务数据主体请求](gdpr-dsr-prof-services.md)。

### <a name="microsoft-controller-products"></a>Microsoft 控制者产品

在某些情况下，组织用户可能会访问 Microsoft 作为数据控制者的 Microsoft 产品或服务。 在这种情况下，用户需要直接向 Microsoft 发出自己的 DSR，并且 Microsoft 会直接向用户完成请求。

### <a name="third-party-products"></a>第三方产品

对于通过 Microsoft 帐户身份验证访问的第三方产品和服务，应将任何数据主体请求定向到相应的第三方。

## <a name="data-subject-request-admin-tools"></a>数据主体请求管理工具

- **安全与合规中心**：使用 [安全与合规性中心](https://aka.ms/stpsecurityandcompliance)或应用程序内部功能导出用户生成的数据。
- **Azure AD 管理中心**：使用 [Azure AD 管理中心](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/Allusers/menuId/)从 Azure Active Directory 和相关服务中删除数据主体。
- **Microsoft 数据日志导出**：租户管理员可使用 [Microsoft 数据记录导出](https://aka.ms/MicrosoftGDPR)功能导出系统生成的日志。

## <a name="learn-more"></a>了解更多

- [Microsoft 信任中心](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
