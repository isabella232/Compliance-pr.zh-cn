---
title: 审核日志记录概述
description: 了解 Microsoft 365 中的审核日志记录
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: dc56d0413811d59309c974931e1fa50ee184e94a
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497683"
---
# <a name="audit-logging-overview"></a>审核日志记录概述

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Microsoft 365 如何使用审核日志记录？

Microsoft 365 使用审核日志记录来检测其产品和服务中的未经授权的活动，并为 Microsoft 人员提供责任。 审核日志捕获有关系统配置更改和访问事件的详细信息，以及用于标识活动负责人、活动发生时间及发生位置以及活动结果的详细信息。 自动日志分析支持近实时检测可疑行为。 潜在事件会上报给 Microsoft 365 安全响应团队，以进一步进行调查。

Microsoft 365 内部审核日志记录从各种源捕获日志数据，例如：

- 事件日志
- AppLocker 日志
- 性能数据
- System Center 数据
- 呼叫详细信息记录
- 用户体验质量数据
- IIS Web 服务器日志
- SQL Server日志
- Syslog 数据
- 安全审核日志

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Microsoft 365 如何集中并报告审核日志？

许多不同类型的日志数据都从 Microsoft 365 服务器上载到名为"部署"的内部大数据计算服务。 每个服务团队将审核日志从各自的服务器上载到"子场"数据库中进行聚合和分析。 此数据传输通过经过 FIPS 140-2 验证的 TLS 连接在批准的端口和协议上发生，该连接使用名为 Office 数据加载程序 (ODL) 的专有自动化工具。

服务团队针对其 In Teams 中的数据运行范围查询，以执行日志关联、警报和报告。 例如，Microsoft 365 安全团队使用具有专有事件日志分析程序的 Microsoft 365 技术数据关联日志数据、发送警报，并生成有关 Microsoft 365 生产环境中可能可疑活动的可操作报告。 此数据中的报告用于更正漏洞并提高服务的整体性能。

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Microsoft 365 如何保护审核日志？

Microsoft 365 中用于收集和处理审核记录的工具不允许对原始审核记录内容或时间顺序进行永久或不可恢复的更改。 仅授权人员对存储在"波斯"中的 Microsoft 365 数据的访问权限。 Microsoft 365 将审核功能管理限制为负责审核功能的有限服务团队成员子集。 这些团队成员无法修改或删除"科科斯"的数据，并且记录并审核对"科科斯"的日志记录机制的所有更改。 审核日志的保留时间足够长，以支持事件调查和满足法规要求。 在审核日志中保留数据的确切时段由服务团队确定;大多数审核日志数据将保留 90 天或更长时间。

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Microsoft 365 如何保护可能在审核日志中捕获的最终用户可识别信息？

在将数据上载到Insings之前，ODL 应用程序使用推移服务模糊化包含客户数据（如租户信息和最终用户可识别信息）的任何字段，并使用哈希值替换这些字段。 将重写匿名日志和哈希日志，然后将这些日志上载到"均能"中。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与审核日志记录相关的控制措施的验证，请参阅下表。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | AU-2：审核事件 <br> AU-3：审核记录的内容 <br> AU-4：审核存储容量 <br> AU-5：审核处理失败响应 <br> AU-6：审核审阅、分析和报告 <br> AU-7：减少审核并生成报告 <br> AU-8：时间戳 <br> AU-9：保护审核信息  <br> AU-10：不拒绝 <br> AU-11：审核记录保留 <br> AU-12：审核生成  | 2020 年 9 月 24 日 | 
| [OFFICE 365 (ISO 27001/27002) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4：日志记录和监视 | 2020 年 2 月 22 日 |
| [OFFICE 365 (ISO 27017) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4：日志记录和监视 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48：数据中心日志记录 <br> CA-60：审核日志记录 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48：数据中心日志记录 <br> CA-60：审核日志记录 | 2020 年 12 月 24 日|