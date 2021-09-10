---
title: 数据保留、删除和销毁Microsoft 365
description: 有关数据保留、Microsoft 365和销毁的 Microsoft 策略概述。
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: c851b235a70104720457d08c51529ee7b25c65e4
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946908"
---
# <a name="data-retention-deletion-and-destruction-in-microsoft-365"></a>数据保留、删除和销毁Microsoft 365

Microsoft 有一个适用于 Microsoft 365 标准策略，该策略指定删除后客户数据的保留时间。 通常有两种删除客户数据的情况：

- **主动** 删除：租户具有活动订阅，用户或管理员删除数据，或者管理员删除用户。
- **被动删除**：租户订阅结束。

## <a name="data-retention"></a>数据保留

对于其中每个删除方案，下表按数据类别和分类显示数据保留期的最大值：

| 数据类别 | 数据分类 | 说明 | 示例 | 保留期 |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| 客户数据 | 客户内容| 管理员和用户直接提供/创建的内容 <br><br> 包括使用 Microsoft 数据中心内的服务时在 Microsoft 数据中心创建和存储的所有文本、声音、视频、图像Microsoft 365 | 允许用户创作数据的最常用 Microsoft 365 应用程序的示例包括 Word、Excel、PowerPoint、Outlook 和 OneNote <br><br> 客户内容还包括客户拥有/提供的密码 (、证书、加密密钥、存储密钥)  | **主动删除方案：** 最多 30 天 <br><br> **被动删除方案：** 最多 180 天 |
| 客户数据 | EUII (最终用户可识别)  | 标识或可用于标识 Microsoft 服务用户的数据。 EUII 不包含客户内容 | 用户名或显示名称 (DOMAIN\UserName)  <br><br> 用户主体名称 (name@domain)  <br><br>  特定于用户的 IP 地址 | **主动删除方案：** 最多 180 (租户管理员操作)  <br><br> **被动删除方案：** 最多 180 天 |
| 个人数据 <br>  (数据不包含在客户数据)  | EUPI 用户的最终用户假名 ()  | Microsoft 创建的与 Microsoft 服务用户绑定的标识符。 与其他信息（如映射表）结合使用时，EUPI 将标识最终用户 <br><br> EUPI 不包含客户上载或创建的信息 | 用户 GUID、PUID 或 SID <br><br> 会话 ID | **主动删除方案：** 最多 30 天 <br><br> **被动删除方案：** 最多 180 天 |

## <a name="subscription-retention"></a>订阅保留

在活动订阅的术语中，订阅者可以访问、提取或删除存储在 Microsoft 365。 如果付费订阅结束或终止，Microsoft 将存储在 Microsoft 365 中的客户数据存储在有限功能帐户中 90 天，以便订阅者能够提取数据。 90 天保留期结束后，Microsoft 将禁用帐户并删除客户数据。 在订阅到期或终止 Microsoft 365 后 180 天内，Microsoft 将禁用该帐户，并从帐户中删除所有客户数据。 任何数据超过最大保留期后，将在商业上不可恢复。

对于免费试用版，在大多数国家和地区，你的帐户将进入宽限期状态 30 天。 在此宽限期内，你可以购买 Microsoft 365。 如果决定不购买 Microsoft 365，可取消试用或等待宽限期到期，届时系统将会删除你的试用帐户信息和数据。

## <a name="expedited-deletion"></a>快速删除

对于任何订阅，订阅者可以联系 Microsoft 支持并请求加速订阅预配取消。 在此过程中，当管理员输入 Microsoft 提供的锁定代码三天后，将删除所有用户数据。 这包括 SharePoint Online 和 Exchange Online 中处于保留状态或存储在非活动邮箱中的数据。

有关加速取消预配的信息，请参阅 [取消订阅](/microsoft-365/commerce/subscriptions/cancel-your-subscription)。

## <a name="related-links"></a>相关链接

- [数据承载设备破坏](assurance-data-bearing-device-destruction.md)
- [Office 365 中的永久性](assurance-data-immutability.md)
- [Exchange Online 数据删除](assurance-exchange-online-data-deletion.md)
- [SharePoint Online 数据删除](assurance-sharepoint-online-data-deletion.md)
