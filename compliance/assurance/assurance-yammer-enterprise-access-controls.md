---
title: Microsoft 365 Yammer企业访问控制
description: 本文包含有关生产环境中Yammer Enterprise访问控制的简短摘要。
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ac02d8ba8719d9ef78a24bee37732007af7cba8b
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573570"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer企业访问控制 

对生产环境的物理和Yammer访问仅限于一小部分人员 (基础结构和操作) 。 与其他专业Microsoft 365一样，Yammer工程师对客户数据具有零长期访问权限。 必须使用基于审批的实时访问控制系统（类似于具有有限数量的审批者锁箱）请求访问。 审批者验证请求 (例如，他们根据需求、业务案例、时间等验证请求是否合法) 然后批准或拒绝请求。 如果请求得到批准，则针对定义的有限时间授予 JIT 访问权限。 超过访问时间后，访问将自动过期。

与其他 Microsoft 365 服务一样，对 Yammer 环境的所有访问都使用多重身份验证。 所有访问和命令历史记录都归用户所有，由安全团队Yammer查看。

有关管理和管理Yammer，请参阅管理Yammer[帮助](/yammer/yammer-landing-page)。