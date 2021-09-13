---
title: 数据承载设备破坏
description: 本文将概述 Microsoft 数据中心的数据影响设备销毁过程。
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
ms.openlocfilehash: 6a26334b805be069298302d3ad1e8e5b9e728150
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158277"
---
# <a name="data-bearing-device-destruction"></a>数据承载设备破坏

## <a name="data-destruction-overview"></a>数据销毁概述

Microsoft 具有与数据 (DBD) 处理和管理 Microsoft 数据中心中的 DBD 的指南、策略、安全要求和过程。

DBD 是能够存储客户或专有 Microsoft 数据的任何存储设备：

- 硬盘驱动器 (HDD) 
- 固态硬盘 (SSD) 
- USB 驱动器
- IO 加速器卡
- SD/Compact Flash 卡
- HSM 卡
- PCIe SSD 卡
- NVDIMM (非易失性双行内存模块) 

在 Microsoft 数据中心内使用的故障 DBD 在数据中心园区内进行审核和销毁。 根据任何适用的规则、法律和法规，评估从服务中停用的任何资产，以与其安全/隐私要求和资产分类相一样的方式处置。

Microsoft 对包含数据的 DBD 和资产使用三类数据删除：

- **Clear**：与逻辑技术相关，可帮助清理所有用户可地址存储位置的数据，以防范简单的非安全数据恢复技术。 这些技术通常通过标准读取和写入命令应用到存储设备，例如使用新值重写，或者使用菜单选项将设备重置为出厂状态 (其中不支持重写) 。
- **Purge：** 与物理或逻辑技术相关，这些技术使用一些技术使目标数据恢复无法实现。
- **销毁**：使用一些现代技术使目标数据恢复无法实现，并随后导致无法使用该媒体存储数据。

清除和销毁清理是使用安全组批准的工具和流程执行的。 记录将保留对资产的清除和销毁。 对于仅对磁介质 (，未完成清除操作的设备成功取消对)  (的解压，为基于切分的板（如 SSD) ）使用多引脚连接 (，或销毁。

## <a name="clear"></a>Clear

如果已停用的资产经过评估并被视为不可访问，则已批准的数据清除解决方案会清除该资产。 Microsoft 数据中心使用 NIST SP-800-88 明确准则。

## <a name="purge"></a>清除

根据现场配置和设备可用性，在销毁之前会清除某些设备。 清除设备包括经 NSA 批准的用于磁媒体的反gaussers和用于固态硬盘的多引脚功能设备。 Microsoft 数据中心使用 NIST SP-800-88 清除准则。

## <a name="destroy"></a>销毁

如果评估并认为已停用的资产可访问，则使用符合 NIST SP-800-88 准则的已批准标准操作程序现场销毁该资产。 这些 DBD 在物理和逻辑上受到跟踪，以通过最终处置保持锁链。

每个 Microsoft 数据中心都使用一个现场进程来对故障和停用的 DBD 进行删除和处置。 在此过程中，Microsoft 人员确保在整个处置过程中保持安全链。

## <a name="resources"></a>资源

- [NIST 特殊出版物 800-88](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)
