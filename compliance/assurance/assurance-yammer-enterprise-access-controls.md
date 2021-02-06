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
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120361"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer 企业访问控制 

对 Yammer 生产环境的物理和逻辑访问仅限于一小组人员 (基础结构和操作) 。 与其他 Microsoft 365 工程师一样，Yammer 工程师对客户数据具有零长期访问权限。 必须使用基于审批的实时访问控制系统（类似于具有有限数量的审批者锁箱）请求访问。 审批者验证请求 (例如，他们根据需求、业务案例、时间等验证请求是否合法) 然后批准或拒绝请求。 如果请求得到批准，将授予针对已定义和有限时间进行 JIT 访问的权限。 超过访问时间后，访问将自动过期。

与其他 Microsoft 365 服务一样，对 Yammer 生产环境的所有访问都使用多重身份验证。 所有访问和命令历史记录都归用户所有，Yammer 安全团队会定期记录并查看这些历史记录。

有关 Yammer 管理和管理的信息，请参阅 [Yammer 管理员帮助](/yammer/yammer-landing-page)。