---
title: Microsoft 安全事件管理：包含、隔离和恢复
description: 本文概述了 Microsoft 联机服务中的安全事件管理包含、隔离和恢复过程。
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 0c99c28ee6a291acbcfe913a87aa107d3be5c75a
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946990"
---
# <a name="microsoft-security-incident-management-containment-eradication-and-recovery"></a>Microsoft 安全事件管理：包含、隔离和恢复

根据安全响应团队、服务团队和其他人员执行的分析，制定了适当的抑制和恢复计划，以最大限度地减少安全事件的影响。 然后，适当的服务团队在生产中应用该计划，并获得安全响应团队的支持。

## <a name="containment"></a>遏制

在检测到安全事件后，必须包含入侵，然后攻击者才能访问更多资源或造成更多损害。 我们的安全事件响应过程的主要目标是限制客户或他们的数据，或 Microsoft 系统、服务和应用程序的影响。

## <a name="eradication"></a>消除

消除是根除安全事件的过程，具有较高的置信度。 目标是双重的：

- 从环境中完全收回攻击者
- 缓解漏洞攻击 (如果已知) 启用或可能允许攻击者重新访问环境。

根据事件的性质、安全事件的范围、渗透的深度和可能的威胁，安全响应团队将建议服务团队采用保护技术。 考虑到这些不明智的步骤可能导致的潜在业务影响，如有必要，这些决策由服务团队和安全响应团队在经过执行事件管理器 (的详细分析和批准后) 。

## <a name="recovery"></a>恢复

由于响应团队获得合理的置信度，即攻击者已从环境中退出，并且所有已知易受攻击的路径都已被消除，因此各个服务团队将启动还原步骤，以将服务引入已知且良好的配置。 这些还原步骤将与安全响应团队一起协商。 此活动包括确定服务上次已知的良好状态、从备份还原到此状态、检查还原状态中的易受攻击路径等。安全响应团队与服务团队联系后，将确定最适合环境的恢复计划。

恢复的一个关键方面是增强的改进功能和控制，以验证恢复计划已成功执行，并且环境中不存在泄露的迹象。

## <a name="customer-notification-of-security-incident"></a>客户安全事件通知

如果 Microsoft 确定发生了安全事件，我们将在我们同意的合同和合规性要求内，以过度延迟方式通知你。 确定所有受影响的租户后，相应的通信团队将努力确定可能适用于受影响租户的任何相关法规。 通信团队使用适用法规中定义的相应通信通道通知相应的租户联系人。

![事件响应流程。](../media/assurance-incident-response-process.png)

通知将包括有关事件的详细信息，例如事件描述、客户数据的影响（如果有）以及 Microsoft 采取的操作，以及/或建议客户为解决问题并防止重复采取的操作。 通知将传递给 Microsoft (租户) 管理员。 若要确保收到通知，应确保管理员在租户配置文件中提供和维护准确的联系信息。 此外，根据事件的性质，Microsoft 365也可通过服务运行状况仪表板[Microsoft 365通知客户](http://status.yammer.com/)。

## <a name="related-articles"></a>相关文章

- [Microsoft 安全事件管理](assurance-security-incident-management.md)
- [Microsoft 安全事件管理：准备](assurance-sim-preparation.md)
- [Microsoft 安全事件管理：检测和分析](assurance-sim-detection-analysis.md)
- [Microsoft 安全事件管理：事后活动](assurance-sim-post-incident-activity.md)
- [如何记录安全事件支持票证](/azure/security/fundamentals/event-support-ticket)
- [GDPR 规定的 Azure 和 Dynamics 365 泄露通知](/compliance/regulatory/gdpr-breach-azure-dynamics)
