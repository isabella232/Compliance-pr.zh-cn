---
title: 数据不可变Microsoft 365
description: 了解如何Microsoft 365可发现的形式保留数据，以解决法规合规性、内部管理要求和诉讼风险。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e17685c7d927ab8188abe1ef4dae4d2cdf0f3764
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946904"
---
# <a name="data-immutability-in-microsoft-365"></a>数据不可变Microsoft 365

法规遵从性、内部管理要求或诉讼风险要求组织以可发现的形式保留电子邮件和关联数据。 系统内的所有数据都必须可发现，并且不能销毁或更改任何数据。 针对此的行业标准术语是"不可变"。

用于不可变的传统方法通常通过将电子邮件移动到单独的只读存储位置来有效。 虽然此类系统用于保留邮箱项目以便进行发现，但是它们通常会通过从日常工作流中删除保留的项目来影响用户体验。 对于 IT 专业人员，这种不可变方法要求部署和持续维护单独的服务器和存储基础结构。 使用邮件系统外部的工具执行发现，其中包括关联的部署和维护成本。

通过存档服务及其服务中的就地保留和保留策略Microsoft 365，您可以保留传入、内部和传出数据的许多类。 这包括：

- 入站和出站电子邮件通信
- 电子邮件表单或共享联机文档中包含的书籍和记录
- 会议请求
- 传真
- 即时消息
- 联机会议期间共享的文档
- 语音留言

此外，Microsoft 还开发了附加功能，允许通过与第[](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc)三方数据捕获和管理解决方案集成来存档来自其他源的数据。 导入第三方数据后，可以将Microsoft 365合规性功能应用于数据，包括：

- [诉讼保留](/microsoft-365/compliance/create-a-litigation-hold)
- [就地电子数据展示和保留](/microsoft-365/compliance/manage-legal-investigations)
- [合规性搜索](/microsoft-365/compliance/search-for-content)
- [就地存档](/microsoft-365/compliance/enable-archive-mailboxes)
- [邮箱审核](/microsoft-365/compliance/enable-mailbox-auditing)
- [保留策略](/microsoft-365/compliance/retention-policies)

例如，当邮箱置于诉讼保留时，将保留第三方数据。 可以使用电子数据展示或合规性搜索In-Place第三方数据。 也可以像对 Microsoft 数据一样将存档和保留策略应用于第三方数据。 将第三方数据存档Microsoft 365有助于组织遵守政府法规策略。

Microsoft 365存档为美国证券交易Exchange C17a (4) 法规 17a-4 兼容存储提供。 Microsoft 365保留策略和保留策略（包括保留锁定）以不可重写、不可擦除格式收集的所有数据的永久文件。

具体来说：

- 使用上述保留策略存储的所有记录都保存在普通用户的专用存储区域中。 只有授权用户可以访问和搜索这些记录，但不能更改或清除它们。
- 每个项目的元数据包括用于计算保留期的时间戳。 当收到或创建一个新项，并且无法修改或删除元数据时，将应用时间戳。
- 利用Microsoft 365存档，用户可以组合不同的保留策略和保留操作以创建精细的保留策略。 这些策略定义保留项的类型或位置以及保留持续时间。
- 保留锁定功能允许用户选择是否使策略成为限制性策略。 限制性策略禁止任何人删除、禁用或更改保留策略。 这意味着，一旦启用保留锁定，就无法禁用它，并且不存在这样一种机制，在保留期间，保留策略收集的现有保管人的任何数据都将被覆盖、修改、擦除或删除。 此外，保留锁定设置的保留期可能不会缩短或减少。 但是，如果法律要求继续保留存储的数据，可能会延长，如上所述。 保留锁定可确保任何人（甚至是管理员或具有特定控制访问权限的管理员）都不得更改设置或覆盖或擦除已存储的数据，使 Microsoft 365 中的存档符合 2003 年发布的 SEC 规则 17a-4 中规定的指导。

若要了解 Microsoft 365 如何帮助您履行法规义务，尤其是与规则 17a-4 要求相关的法规义务，请参阅涵盖[](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf)Exchange Online Archiving、SharePoint Online、OneDrive for Business 和 Skype for Business 的白皮书。 该白皮书还根据 SEC 规则 17a-4 中的每个要求深入分析 Microsoft 365 存档特性和功能，并演示受监管客户 Microsoft 365 存档如何帮助他们满足这些要求。
