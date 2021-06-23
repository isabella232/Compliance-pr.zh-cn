---
title: Microsoft 365项目的内部Microsoft 365日志记录
description: 本文介绍工程团队的内部日志记录Microsoft 365工作原理。
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
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088591"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a><span data-ttu-id="00f1b-103">Microsoft 365 工程部的内部日志记录</span><span class="sxs-lookup"><span data-stu-id="00f1b-103">Internal logging for Microsoft 365 engineering</span></span>

<span data-ttu-id="00f1b-104">除了可供客户使用的事件和日志数据之外，Microsoft 还维护了一个内部日志数据收集系统，可供Microsoft 365使用。</span><span class="sxs-lookup"><span data-stu-id="00f1b-104">In addition to the events and log data available for customers, Microsoft maintains an internal log data collection system that is available to Microsoft 365 engineers.</span></span> <span data-ttu-id="00f1b-105">许多不同类型的日志数据从 Microsoft 365 服务器上载到专有安全监视解决方案，用于近实时 (NRT) 分析和内部、大数据计算服务 (Cosmos) ，用于长期存储。</span><span class="sxs-lookup"><span data-stu-id="00f1b-105">Many different types of log data are uploaded from Microsoft 365 servers to a proprietary security monitoring solution for near real-time (NRT) analysis and an internal, big data computing service (Cosmos) for long-term storage.</span></span> <span data-ttu-id="00f1b-106">此数据传输通过经过 FIPS 140-2 验证的 TLS 连接在批准的端口和协议上发生，该连接使用名为 Office 数据加载程序 (ODL) 的专有自动化工具。</span><span class="sxs-lookup"><span data-stu-id="00f1b-106">This data transfer occurs over a FIPS 140-2-validated TLS connection on approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL).</span></span> <span data-ttu-id="00f1b-107">用于收集和Microsoft 365审核记录的工具不允许对原始审核记录内容或时间顺序进行永久或不可恢复的更改。</span><span class="sxs-lookup"><span data-stu-id="00f1b-107">The tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.</span></span>

<span data-ttu-id="00f1b-108">服务团队Cosmos一个集中式存储库，以对应用程序使用情况进行分析，测量系统和操作性能，并查找可能指示问题或安全问题的异常和模式。</span><span class="sxs-lookup"><span data-stu-id="00f1b-108">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues.</span></span> <span data-ttu-id="00f1b-109">每个服务团队上载一个基线，其中包括：</span><span class="sxs-lookup"><span data-stu-id="00f1b-109">Each service team uploads a baseline that includes:</span></span>

- <span data-ttu-id="00f1b-110">事件日志</span><span class="sxs-lookup"><span data-stu-id="00f1b-110">Event logs</span></span>
- <span data-ttu-id="00f1b-111">AppLocker 日志</span><span class="sxs-lookup"><span data-stu-id="00f1b-111">AppLocker logs</span></span>
- <span data-ttu-id="00f1b-112">性能数据</span><span class="sxs-lookup"><span data-stu-id="00f1b-112">Performance data</span></span>
- <span data-ttu-id="00f1b-113">System Center数据</span><span class="sxs-lookup"><span data-stu-id="00f1b-113">System Center data</span></span>
- <span data-ttu-id="00f1b-114">呼叫详细信息记录</span><span class="sxs-lookup"><span data-stu-id="00f1b-114">Call detail records</span></span>
- <span data-ttu-id="00f1b-115">用户体验质量数据</span><span class="sxs-lookup"><span data-stu-id="00f1b-115">Quality of experience data</span></span>
- <span data-ttu-id="00f1b-116">IIS Web 服务器日志</span><span class="sxs-lookup"><span data-stu-id="00f1b-116">IIS Web Server logs</span></span>
- <span data-ttu-id="00f1b-117">SQL Server日志</span><span class="sxs-lookup"><span data-stu-id="00f1b-117">SQL Server logs</span></span>
- <span data-ttu-id="00f1b-118">Syslog 数据</span><span class="sxs-lookup"><span data-stu-id="00f1b-118">Syslog data</span></span>
- <span data-ttu-id="00f1b-119">安全审核日志</span><span class="sxs-lookup"><span data-stu-id="00f1b-119">Security audit logs</span></span>

<span data-ttu-id="00f1b-120">在上载之前，ODL 应用程序使用推移服务删除包含客户数据（如租户信息和最终用户可识别信息）的任何字段，并使用哈希值替换这些字段。</span><span class="sxs-lookup"><span data-stu-id="00f1b-120">Prior to uploading, the ODL application uses a scrubbing service to remove any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value.</span></span> <span data-ttu-id="00f1b-121">已清理的日志将上载到 Cosmos 并上载到 NRT 安全监视解决方案，该解决方案将分析日志中的潜在安全事件和性能指示器。</span><span class="sxs-lookup"><span data-stu-id="00f1b-121">The scrubbed logs are uploaded to Cosmos and to the NRT security monitoring solution that analyzes the logs for potential security events and performance indicators.</span></span> <span data-ttu-id="00f1b-122">服务审核日志数据保留Cosmos由服务团队决定;大多数审核日志数据将保留 90 天或更长时间，以支持安全事件调查并满足法规的保留要求。</span><span class="sxs-lookup"><span data-stu-id="00f1b-122">The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="00f1b-123">对Microsoft 365中存储Cosmos数据的访问权限仅限于授权人员。</span><span class="sxs-lookup"><span data-stu-id="00f1b-123">Access to Microsoft 365 data stored in Cosmos is restricted to authorized personnel.</span></span> <span data-ttu-id="00f1b-124">Microsoft 将审核日志的管理限制为负责审核功能的有限安全团队成员子集。</span><span class="sxs-lookup"><span data-stu-id="00f1b-124">Microsoft restricts the management of audit logs to a limited subset of Security Team members responsible for audit functionality.</span></span> <span data-ttu-id="00f1b-125">安全团队没有长期管理权限来访问Cosmos，并且会记录和审核所有更改。</span><span class="sxs-lookup"><span data-stu-id="00f1b-125">The Security Team does not have standing administrative access to Cosmos, and all changes are recorded and audited.</span></span>

<span data-ttu-id="00f1b-126">在 NRT 分析后，每个服务团队都可以使用分析工具和仪表板进行数据关联、交互式查询和数据分析。</span><span class="sxs-lookup"><span data-stu-id="00f1b-126">After NRT analysis, each service team can use analysis tools and dashboards for data correlation, interactive queries, and data analytics.</span></span> <span data-ttu-id="00f1b-127">这些报告用于监视和改进服务的整体性能。</span><span class="sxs-lookup"><span data-stu-id="00f1b-127">These reports are used to monitor and improve the overall performance of the service.</span></span>
