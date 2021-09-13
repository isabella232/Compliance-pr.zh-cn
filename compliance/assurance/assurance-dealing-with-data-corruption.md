---
title: Microsoft 365处理数据损坏
description: 本文介绍了数据损坏Microsoft 365以及 Microsoft 为阻止和恢复数据而做出的工作。
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
ms.openlocfilehash: 860a150760e080df4a577d73478a75ac94b8700b
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158262"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a>处理数据损坏Microsoft 365

在具有大量数据和独立系统时，运行大规模云服务的一个难题是如何处理数据损坏。 数据损坏可能是由：

- 应用程序或基础结构错误，损坏部分或所有应用程序状态
- 导致数据丢失或无法读取数据的硬件问题
- 人为操作错误
- 恶意黑客和解除攻击的员工
- 导致数据部分丢失的外部服务中的事件

由于数据完整性的复原能力更大意味着数据损坏事件更少，因此 Microsoft 内置了 Microsoft 365 保护机制，以防止损坏发生，以及使我们能够在出现损坏时恢复数据的系统和进程。 检查和过程存在于工程发布过程的各个阶段，以提高防止数据损坏的复原能力，包括：

- 系统设计
- 代码组织和结构
- 代码审阅
- 单元测试、集成测试和系统测试
- 旅行线测试/入口

在Microsoft 365环境中，数据中心之间的对等复制可确保始终存在任何数据的多个实时副本。 标准映像和脚本用于恢复丢失的服务器，复制的数据用于还原客户数据。 由于内置了数据复原检查和过程，Microsoft 仅维护 Microsoft 365 信息系统文档 (包括与安全相关的文档) 的备份，使用 SharePoint Online 中的内置复制和内部代码存储库工具 Source Repositor。 系统文档存储在 SharePoint Online 中，Source 则包含系统和应用程序映像。 SharePoint Online 和 Source 则使用版本控制，并且几乎可以实时复制。
