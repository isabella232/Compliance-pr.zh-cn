---
title: Microsoft 365 工程团队的 Microsoft 365 内部日志记录
description: 本文介绍 Microsoft 365 工程团队的内部日志记录的工作原理。
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
ms.openlocfilehash: 110a61c27a00380eede4d4f2303acfb025a27a1f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497076"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Microsoft 365 工程部的内部日志记录

除了可供客户使用的事件和日志数据之外，Microsoft 365 工程师还可使用内部日志数据收集系统。 许多不同类型的日志数据都从 Microsoft 365 服务器上载到名为"部署"的内部大数据计算服务。 每个服务团队将审核日志从各自的服务器上载到"子场"数据库中进行聚合和分析。 此数据传输通过经过 FIPS 140-2 验证的 TLS 连接在专门批准的端口和协议上发生，该连接使用名为 Office 数据加载程序 (ODL) 的专有自动化工具。 Microsoft 365 中用于收集和处理审核记录的工具不允许对原始审核记录内容或时间顺序进行永久或不可恢复的更改。

服务团队使用一个集中式存储库来分析应用程序使用情况，测量系统和运行性能，并查找可能指示问题或安全问题的异常和模式。 每个服务团队将日志基线上载到"科科斯"中，具体取决于他们要分析的内容，这通常包括：

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

在将数据上载到Insings之前，ODL 应用程序使用推移服务模糊化包含客户数据（如租户信息和最终用户可识别信息）的任何字段，并使用哈希值替换这些字段。 将重写匿名日志和哈希日志，然后将这些日志上载到"均能"中。 服务团队针对其 In Teams 中的数据运行范围查询，以用于关联、警报和报告。 在审核日志中保留数据的时间段由服务团队确定;大多数审核日志数据将保留 90 天或更长时间，以支持安全事件调查并满足法规的保留要求。

仅授权人员对存储在"波斯"中的 Microsoft 365 数据的访问权限。 Microsoft 将审核功能管理限制为负责审核功能的有限服务团队成员子集。 这些团队成员无法修改或删除"科科斯"的数据，并且记录并审核对"科科斯"的日志记录机制的所有更改。

每个服务团队通过授权某些应用程序执行特定分析来访问其日志数据进行分析。 例如，Microsoft 365 安全团队通过专有事件日志分析程序使用来自 Microsoft 365 的数据关联、警报和生成有关 Microsoft 365 生产环境中可能可疑活动的可操作报告。 此数据中的报告用于更正漏洞并提高服务的整体性能。 如果特定警报或报告需要进一步调查，服务人员可以请求将数据导入回 Microsoft 365 服务。 由于从管理中心导入的特定日志已加密，并且服务人员无法访问解密密钥，因此目标日志以编程方式通过解密服务传递，此服务将范围结果返回给授权服务人员。 本练习发现的任何漏洞都使用 Microsoft 的标准安全事件管理通道进行报告并上报。
