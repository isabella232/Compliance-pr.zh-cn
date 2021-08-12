---
title: 审核日志记录概述
description: 了解审核日志记录Microsoft 365
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
ms.openlocfilehash: 5a851373660fbc64de8fbfbb191e7b631493bae6534f687e73917f10fa605ac7
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "54289291"
---
# <a name="audit-logging-overview"></a>审核日志记录概述

## <a name="how-does-microsoft-365-employ-audit-logging"></a>如何Microsoft 365审核日志记录？

Microsoft 365审核日志记录，以检测其产品和服务中的未经授权的活动，并为 Microsoft 人员提供责任。 审核日志捕获有关系统配置更改和访问事件的详细信息，以及用于标识活动负责人、活动发生时间及发生位置以及活动结果的详细信息。 自动日志分析支持近实时检测可疑行为。 潜在事件将上报给安全Microsoft 365团队进行进一步调查。

Microsoft 365审核日志记录从各种源捕获日志数据，例如：

- 事件日志
- AppLocker 日志
- 性能数据
- System Center数据
- 呼叫详细信息记录
- 用户体验质量数据
- IIS Web 服务器日志
- SQL Server日志
- Syslog 数据
- 安全审核日志

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>如何Microsoft 365审核日志进行集中并报告？

许多不同类型的日志数据从 Microsoft 365 服务器上载到专有安全监视解决方案，用于近实时 (NRT) 分析和内部大数据计算服务 (Cosmos) 用于长期存储。 此数据传输通过经过 FIPS 140-2 验证的 TLS 连接在批准的端口和协议上发生，该连接使用名为 Office 数据加载程序 (ODL) 的专有自动化工具。

日志使用基于规则、统计和机器学习方法在 NRT 中处理，以检测系统性能指标和潜在的安全事件。 机器学习模型使用传入日志数据和存储在 Cosmos历史记录数据来持续改进检测功能。 与安全相关的检测会生成警报，向呼叫工程师通知潜在事件，并触发自动修正操作（如果适用）。 除了自动安全监视之外，服务团队还使用分析工具和仪表板进行数据关联、交互式查询和数据分析。 这些报告用于监视和改进服务的整体性能。

有关安全监视和警报详细信息，请参阅 [安全监视概述](assurance-security-monitoring.md)。

![审核数据流](../media/assurance-audit-data-flow.png)

## <a name="how-does-microsoft-365-protect-audit-logs"></a>如何Microsoft 365审核日志？

用于收集和Microsoft 365审核记录的工具不允许对原始审核记录内容或时间顺序进行永久或不可恢复的更改。 对Microsoft 365中存储Cosmos数据的访问权限仅限于授权人员。 此外，Microsoft 365将审核日志管理限制为负责审核功能的有限安全团队成员子集。 安全团队没有对安全团队长期管理Cosmos。 管理访问需要实时访问 (JIT) 访问审批，并且记录并审核Cosmos日志记录机制的所有更改。 审核日志的保留时间足够长，以支持事件调查和满足法规要求。 数据保留时间审核日志由服务Cosmos确定;大多数审核日志数据将保留 90 天或更长时间。

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>如何Microsoft 365审核日志中捕获的最终用户可识别信息？

在上载日志数据之前，ODL 应用程序使用推移服务删除包含客户数据（如租户信息和最终用户可识别信息）的任何字段，并使用哈希值替换这些字段。 匿名日志和哈希日志将被重写，然后上传到Cosmos。 所有日志传输都通过 FIPS 140-2 (TLS 加密连接) 。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与审核日志记录相关的控制措施的验证，请参阅下表。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | AU-2：审核事件 <br> AU-3：审核记录的内容 <br> AU-4：审核存储容量 <br> AU-5：审核处理失败响应 <br> AU-6：审核审阅、分析和报告 <br> AU-7：减少审核并生成报告 <br> AU-8：时间戳 <br> AU-9：保护审核信息  <br> AU-10：不拒绝 <br> AU-11：审核记录保留 <br> AU-12：审核生成  | 2020 年 9 月 24 日 | 
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4：日志记录和监视 | 2021 年 4 月 20 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4：日志记录和监视 | 2021 年 4 月 20 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48：数据中心日志记录 <br> CA-60：审核日志记录 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48：数据中心日志记录 <br> CA-60：审核日志记录 | 2020 年 12 月 24 日|