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
ms.openlocfilehash: 3714a5df73253d0814e1d4067248116cb6e10a40
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506423"
---
# <a name="audit-logging-overview"></a>审核日志记录概述

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Microsoft 365 如何使用审核日志记录？

Microsoft 365 采用审核日志记录来检测其产品和服务中的未经授权的活动，并为 Microsoft 人员提供责任。 审核日志捕获有关系统配置更改和访问事件的详细信息，并提供了详细信息，以确定谁负责活动、活动发生的时间和时间以及活动的结果是什么。 自动化日志分析支持接近实时检测可疑行为。 可能的事件已上报给 Microsoft 365 安全响应团队，以进一步进行调查。

Microsoft 365 内部审核日志记录捕获来自各种源的日志数据，例如：

- 事件日志
- AppLocker 日志
- 性能数据
- System Center data
- 呼叫详细信息记录
- 经验数据的质量
- IIS Web 服务器日志
- SQL Server 日志
- Syslog 数据
- 安全审核日志

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Microsoft 365 如何对审核日志进行集中和报告？

将许多不同类型的日志数据从 Microsoft 365 服务器上传到内部的大型数据计算服务（称为 Cosmos）。 每个服务团队将审核日志从各自的服务器上载到 Cosmos 数据库中，以进行聚合和分析。 此数据传输140-2 通过经过认可的端口和协议（使用称为 Office 数据加载工具的专用自动化工具 (ODL) ）进行验证的 TLS 连接进行。

服务团队针对 Cosmos 中的数据在日志关联、警报和报告中运行对其数据的范围内查询。 例如，Microsoft 365 安全团队使用来自 Cosmos 的数据和专有的事件日志分析器来关联日志数据，发送警报，并生成可操作报告，以了解 Microsoft 365 生产环境中可能存在的可疑活动。 这些数据中的报告用于更正漏洞并提高服务的整体性能。

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Microsoft 365 如何保护审核日志？

Microsoft 365 中用于收集和处理审核记录的工具不允许对原始审核记录的内容或时间排序进行永久或不可恢复的更改。 对存储在 Cosmos 中的 Microsoft 365 数据的访问仅限于已授权的人员。 Microsoft 365 将审核功能的管理限制为负责审核功能的服务团队成员的有限子集。 这些团队成员不能修改或删除 Cosmos 中的数据，并且会记录和审核对 Cosmos 的日志记录机制所做的所有更改。 审核日志的保留时间足够长，以支持事件调查并满足法规要求。 Cosmos 中的审核日志数据保留的确切期限由服务团队决定;大多数审核日志数据会保留90天或更长时间。

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Microsoft 365 如何保护可在审核日志中捕获的最终用户可识别信息？

在将数据上载到 Cosmos 中之前，ODL 应用程序使用清理服务来模糊处理包含客户数据（如租户信息和最终用户身份信息）的任何字段，并将这些字段替换为哈希值。 重写匿名和哈希日志，然后将其上载到 Cosmos。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 请参阅下表以验证与审核日志记录相关的控件。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | AU-2：审核事件 <br> AU-3：审核记录的内容 <br> AU-4：审核存储容量 <br> AU-5：对审核处理失败的响应 <br> AU-6：审核评审、分析和报告 <br> AU-7：审核缩减和报告生成 <br> AU-8：时间戳 <br> AU-9：审核信息保护  <br> AU-10：不可否认性 <br> AU-11：审核记录保留 <br> AU-12：审核生成  | 2020年9月24日 | 
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.4：日志记录和监视 | 2020 年 2 月 22 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.4：日志记录和监视 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48：数据中心日志记录 <br> CA-60：审核日志记录 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48：数据中心日志记录 <br> CA-60：审核日志记录 | 2019 年 9 月 30 日 |