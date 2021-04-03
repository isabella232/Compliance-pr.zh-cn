---
title: Microsoft 365 监视和审核访问控制
description: 摘要：Microsoft 365 中可用的各种监视和审核访问控制的摘要。
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e9a9ea713afbf7568c1ae67d31a57dd9dce51fc3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497544"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>在 Microsoft 365 中监视和审核访问控制

Microsoft 对 Microsoft 365 中发生的所有委派、权限和操作执行广泛的监视和审核。 Microsoft 365 访问控制是一个基于最小特权原则构建的自动化过程，它合并了数据访问控件和审核：

- 所有允许的访问都可跟踪到唯一用户。 管理员负责处理客户内容。
- 将捕获访问控制请求、审批和管理操作日志，以分析安全和恶意事件。
- 访问级别几乎基于安全组成员身份进行实时审查，以确保只有具有授权业务理由并满足资格要求的用户才能访问系统。
- Microsoft 365、其访问控制和支持服务（包括 Azure Active Directory 和物理数据中心）定期由独立的第三[](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)方审核是否符合[ISO/IEC 27001、ISO/IEC](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [27018、SOC、FedRAMP](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) (Office [365) ](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)和其他标准。 [](https://www.microsoft.com/TrustCenter/Compliance/SOC)
- Microsoft 365 工程师必须每年参加一次安全培训，查看提升的访问最佳过程，并确认 Microsoft 的安全和隐私策略，以维护对服务的权利。

自动警报在检测到可疑活动时触发，例如在短时间内多次登录失败。 Microsoft 365 安全响应团队使用机器学习和大数据分析来查看和分析活动，查找异常访问模式，并主动响应异常和非法活动。 Microsoft 还采用专门的渗透测试人员团队，并定期参加红队和蓝队练习，以查找服务中的安全和访问控制问题。 客户可以使用审核报告和 Microsoft 365 提供的管理活动 API 验证访问控制系统的有效性。

有关详细信息，请参阅 [Office 365 管理活动 API 参考](/office/office-365-management-api/office-365-management-activity-api-reference) 和 Microsoft [365 中的审核和报告](assurance-auditing-and-reporting-overview.md)。
