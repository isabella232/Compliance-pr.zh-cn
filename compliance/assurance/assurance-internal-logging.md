---
title: Microsoft 365工程团队的内部Microsoft 365日志记录
description: 本文介绍工程团队的内部日志记录Microsoft 365工作原理。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: 20a21fe0d67f8986ec6e89b8ecbfd2915f9b8245
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481934"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Microsoft 365 工程部的内部日志记录

除了可供客户使用的事件和日志数据之外，Microsoft 还维护一个内部日志数据收集系统，可供Microsoft 365使用。 许多不同类型的日志数据从 Microsoft 365 服务器上载到专有安全监视解决方案，用于近实时 (NRT) 分析和内部、大数据计算服务 (Cosmos) ，用于长期存储。 此数据传输通过经过 FIPS 140-2 验证的 TLS 连接在批准的端口和协议上发生，该连接使用称为 Office 数据加载程序 (ODL) 的专有自动化工具。 用于收集和Microsoft 365审核记录的工具不允许对原始审核记录内容或时间顺序进行永久或不可恢复的更改。

服务团队Cosmos存储库，以分析应用程序使用情况、测量系统和运行性能，以及查找可能指示问题或安全问题的异常和模式。 每个服务团队上载一个基线，其中包括：

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

在上载之前，ODL 应用程序使用推移服务删除包含客户数据（如租户信息和最终用户可识别信息）的任何字段，并使用哈希值替换这些字段。 将清理的日志上载到 Cosmos 并上载到 NRT 安全监视解决方案，该解决方案将分析日志中的潜在安全事件和性能指示器。 服务审核日志数据保留Cosmos由服务团队确定;大多数审核日志数据将保留 90 天或更长时间，以支持安全事件调查并满足法规的保留要求。

对Microsoft 365中存储Cosmos数据的访问权限仅限于授权人员。 Microsoft 将审核日志的管理限制为负责审核功能的有限安全团队成员子集。 安全团队没有长期管理权限来访问Cosmos，并且会记录和审核所有更改。

在 NRT 分析后，每个服务团队都可以使用分析工具和仪表板进行数据关联、交互式查询和数据分析。 这些报告用于监视和改进服务的整体性能。
