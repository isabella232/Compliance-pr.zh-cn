---
title: Microsoft 365 Yammer 企业访问控制
description: 本文包含有关生产环境中的 Yammer 企业访问控制的简短摘要。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497355"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer 企业访问控制 

对 Yammer 生产环境的物理和逻辑访问仅限于一小组人员 (基础结构和操作) 。 与其他 Microsoft 365 工程师一样，Yammer 工程师对客户数据具有零长期访问权限。 必须使用基于审批的实时访问控制系统（类似于具有有限数量的审批者锁箱）请求访问。 审批者验证请求 (例如，他们根据需求、业务案例、时间等验证请求是否合法) 然后批准或拒绝请求。 如果请求得到批准，则针对定义的有限时间授予 JIT 访问权限。 超过访问时间后，访问将自动过期。

与其他 Microsoft 365 服务一样，对 Yammer 生产环境的所有访问都使用多重身份验证。 所有访问和命令历史记录都归用户所有，由 Yammer 安全团队定期记录并查看。

有关 Yammer 管理和管理详细信息，请参阅 [Yammer 管理员帮助](/yammer/yammer-landing-page)。