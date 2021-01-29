---
title: Microsoft 365 安全事件管理：抑制、隔离和恢复
description: 本文概述了 Microsoft 365 中的安全事件管理控制、隔离和恢复过程。
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 702735ed2ba35a4f3b0a02123f0c58b5fb4d397e
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037578"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a>Microsoft 365 安全事件管理：抑制、隔离和恢复

根据 Microsoft 365 安全响应团队、服务团队和其他人员执行的分析，制定适当的抑制和恢复计划，以最大限度地减少安全事件的影响。 然后，相应的服务团队在 Microsoft 365 安全响应团队的支持下，在生产中应用该计划。

## <a name="containment"></a>包含

在检测到安全事件后，在攻击者可以访问更多资源或造成更多损害之前，必须包含入侵。 我们的安全事件响应过程的主要目标是限制客户或他们的数据，或 Microsoft 系统、服务和应用程序的影响。

## <a name="eradication"></a>一个

解决是一个以高度可信度消除安全事件的根本原因的过程。 目标是双重的：

- 从环境中完全退出攻击者
- 缓解漏洞 (如果已知) 启用或可能允许攻击者重新访问环境。

根据事件的性质、安全事件的范围、渗透的深度和可能的威胁，Microsoft 365 安全响应团队将建议服务团队采用管理技术。 考虑到这些不一致步骤可能导致的潜在业务影响，如有必要，这些决策由服务团队和 Microsoft 365 安全响应团队在执行事件管理器 (进行详细分析和批准后) 。

## <a name="recovery"></a>恢复

当响应团队获得合理的可信度，即攻击者已从环境中退出并且所有已知的易受攻击的路径都已被消除时，各个服务团队将启动还原步骤，以将服务引入已知且良好的配置。 这些还原步骤将咨询 Microsoft 365 安全响应团队。 此活动包括标识服务的上次已知良好状态、从备份还原到此状态、检查还原状态中的易受攻击路径等。Microsoft 365 安全响应团队与服务团队一起协作，将确定最适合环境的恢复计划。

恢复的一个关键方面是增强的规划和控制，以验证恢复计划已成功执行，并且环境中不存在泄露的迹象。

## <a name="customer-notification-of-security-incident"></a>客户安全事件通知

如果 Microsoft 确定发生了安全事件，我们将在我们同意的合同和合规性要求内，以过度延迟方式通知您。 确定所有受影响的租户后，Microsoft 365 客户体验 (CxP) 通信团队将努力确定可能适用于受影响租户的任何相关法规。 Microsoft 365 CxP 通信团队使用适用法规中定义的相应通信通道通知相应的租户联系人。

通知将包括有关事件的详细信息，例如事件描述、对客户数据的影响（如果有）以及 Microsoft 采取的操作和/或建议客户为解决问题和防止重复采取的操作。 通知将传递给 Microsoft 365 租户 (管理员) 管理员。 若要确保收到通知，应确保管理员在租户配置文件中提供和维护准确的联系信息。 此外，根据事件的性质，还可通过 Microsoft 365 服务运行状况仪表板通知客户[。](http://status.yammer.com/)

## <a name="related-articles"></a>相关文章

- [Microsoft 365 安全事件管理](assurance-security-incident-management.md)
- [Microsoft 365 安全事件管理准备](assurance-sim-preparation.md)
- [Microsoft 365 安全事件管理检测和分析](assurance-sim-detection-analysis.md)
- [Microsoft 365 安全事件管理后期活动](assurance-sim-post-incident-activity.md)
