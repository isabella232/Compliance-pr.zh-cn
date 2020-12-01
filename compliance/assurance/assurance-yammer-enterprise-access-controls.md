---
title: Microsoft 365 Yammer 企业访问控制
description: 本文包含有关生产环境中 Yammer 企业访问控制的简短摘要。
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
ms.openlocfilehash: d44bead3627ed9b99c93bcffc9f29f87731f7407
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506368"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer 企业访问控制 

对 Yammer 生产环境的物理和逻辑访问仅限于一小组用户 (基础结构和运营) 。 与其他 Microsoft 365 工程师一样，Yammer 工程师可以获得对客户数据的零访问权限。 必须使用基于审批的实时访问控制系统请求访问，这类似于具有有限数量的审批者的密码箱。 审批者验证请求 (例如，他们根据需求、业务案例、时间等 ) 验证请求是否合法，然后批准或拒绝该请求。 如果请求得到批准，则会为已定义和有限的时间授予 JIT 访问权限。 超出访问时间后，访问将自动过期。

与其他 Microsoft 365 服务一样，对 Yammer 生产环境的所有访问都将使用多重身份验证。 所有访问和命令历史记录都属于用户，并定期由 Yammer 安全团队记录和查看。

有关 Yammer 管理和管理的详细信息，请参阅 [Yammer 管理员帮助](https://docs.microsoft.com/yammer/yammer-landing-page)。