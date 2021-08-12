---
title: Microsoft 365监控和审核访问控制
description: 摘要：内部可用的各种监视和审核访问控制Microsoft 365。
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
ms.openlocfilehash: e374b22212bce461329e14764a3b35eaa76d5f27fd340e64b9b64fb26ecf35f6
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290576"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>监视和审核Microsoft 365

Microsoft 对应用程序内发生的所有委派、权限和操作执行广泛的Microsoft 365。 Microsoft 365访问控制是一个基于最小特权原则并合并数据访问控件和审核的自动化过程：

- 所有允许的访问都可跟踪到唯一用户。 管理员负责处理客户内容。
- 将捕获访问控制请求、审批和管理操作日志，以分析安全和恶意事件。
- 访问级别几乎基于安全组成员身份进行实时审查，以确保只有具有授权业务理由并满足资格要求的用户才能访问系统。
- Microsoft 365、其访问控制和支持服务（包括 Azure Active Directory 和物理数据中心）会定期由独立的第三[](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)方审核是否符合[ISO/IEC 27001、ISO/IEC](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [27018、SOC、FedRAMP](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [ (Office 365) ](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)和其他[](https://www.microsoft.com/TrustCenter/Compliance/SOC)标准。
- Microsoft 365工程师每年参加一次安全培训，查看提升的访问最佳过程，并确认 Microsoft 的安全和隐私策略，以维护对服务的权利。

自动警报在检测到可疑活动时触发，例如在短时间内多次登录失败。 安全Microsoft 365团队使用机器学习和大数据分析来查看和分析活动，查找异常访问模式，并主动响应异常和非法活动。 Microsoft 还采用专门的渗透测试人员团队，并定期参加红队和蓝队练习，以查找服务中的安全和访问控制问题。 客户可以使用审核报告和由客户提供的管理活动 API 来验证访问控制系统Microsoft 365。

有关详细信息，请参阅Office 365[活动 API 参考](/office/office-365-management-api/office-365-management-activity-api-reference)和审核与Microsoft 365。 [](assurance-auditing-and-reporting-overview.md)
