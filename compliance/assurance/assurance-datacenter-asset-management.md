---
title: 数据中心资产管理
description: Microsoft 数据中心资产管理概述。
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: fafba29a25c5b01fa37d091fb210185a98365192
ms.sourcegitcommit: b228be59e13ae2e05ba85f65c1d4648fef5e9260
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/14/2021
ms.locfileid: "60356379"
---
# <a name="datacenter-asset-management"></a>数据中心资产管理

Microsoft 数据中心由各种物理和虚拟组件组成，其中每个组件都称为资产。 Microsoft 云运营与 (CO+I) 团队遵循安全标准化流程，以部署、跟踪和停用物理和虚拟资产。

## <a name="supply-chain-integrity"></a>供应链完整性

保护资产首先保护供应链。 Microsoft 致力于实现供应链完整性和端到端供应链安全性。 供应商在传输云组件时遵循严格的过程链，以减少更改和篡改的风险。 所有入站和出站库存都会经过仔细检查和监视，以确保固件和组件的完整性。

通常计划将信息系统组件交付到 Microsoft 数据中心。 对于计划外交付，Microsoft 会进行全面检查，并确保在物理输入前批准它们进入 Microsoft 计算机聊天室。 当信息系统组件进入建筑物时，资产管理团队会将收到的项目与引用的票证进行比较，并将设备扫描到资产管理工具中。 接收或交付的所有信息系统组件都由工作流票证工具跟踪，并记录在资产管理工具的发货日志中。 禁止访问者使用个人笔记本电脑和移动电话 (紧急呼叫和做笔记) 除外，尽管允许在生产环境中 (托管) 。 根据数据中心策略，禁止将手机插入设备或拍摄照片。 如果进入数据中心的设备用于维护目的，则设备需要在数据中心访问工具系统中进行数据中心管理审批。

## <a name="asset-inventory"></a>资产库存

Microsoft 要求所有数据中心资产都要有人负责并具有指定的所有者。 所有者负责维护其物理和虚拟资产的最新资产信息。 将新的物理资产添加到数据中心时，将对其进行签名、扫描、添加唯一标记并签入到库存控制系统。 自动化监视工具可帮助跟踪物理资产和虚拟资产。

## <a name="asset-maintenance"></a>资产维护

Microsoft 有两个提供不同类型的资产维护的团队：Critical Environment (CE) 和 Site Services 团队。 CE 团队为包含设施运营基础结构的电力、机械和物理系统提供设施管理。 他们还计划、执行、记录并查看在 CE 组件上执行的所有维护活动。 Microsoft 数据中心依赖计算机化的维护管理系统来管理维护计划和工作订单。 Site Services 团队为位于 Microsoft 数据中心的所有 Microsoft 联机服务资产提供服务。 此外，网站服务团队还为属于数据中心的属性设置服务的资产提供现场技术支持和中断修复服务。

## <a name="asset-classification"></a>资产分类

Microsoft 资产（包括数据）根据数据分类Enterprise分类准则进行分类。 这些准则可促进企业的标准化，并每年进行一次审阅和更新。 资产分类和资产保护标准概述了员工与每个资产交互时必须遵循的安全过程。 请注意，客户被视为其存储在 Microsoft 云环境中的数据的所有者。 分类为客户内容或客户数据的数据资产受适用的安全程序保护。

Microsoft 将所有文档视为系统资产。 网站服务团队负责根据资产分类和资产保护标准以及服务团队定义的任何附加要求，对其资产进行分类，并采用相关安全措施。

资产所有者需要为其资产分配资产分类（无例外）。 在 Microsoft 数据中心环境中，资产是指服务器和网络设备。 其他数字媒体（如 U 盘、外部硬盘驱动器或 CD/DVD）不用于服务操作。 数据中心中不使用非数字媒体。

## <a name="media-storage"></a>媒体存储

Microsoft 数字媒体资产以物理方式安全地存储在 Microsoft 数据中心并置会议室中。 多层物理访问控制和视频监控已到位，以保护和监视这些资产。 数字媒体资产在生命周期结束时，会使用与 NIST SP 800-88 一致的方法在处置之前清除、清除或销毁它们。 数据 [影响设备销毁一](assurance-data-bearing-device-destruction.md) 文介绍了安全处置资产的过程。

## <a name="media-transport"></a>媒体传输

Microsoft 通过保护链将资产传输活动限制为授权人员。 使用锁定、防篡改和要求验证资产库存可确保资产传输中仅涉及授权人员。

从 Microsoft 数据中心传输的所有媒体都需要精确跟踪。 Microsoft 已与多个批准的供应商签订合同，以提供安全寄送服务。 安全传输从准确的清单和锁链开始。 在传递位置，传输公司的已批准人员必须见证容器防篡改图章的删除和解锁。 接收人员对装运进行盘点，并发送一条消息，确认是否收到资产。 Microsoft 还与供应商签订合同，提供设备销毁。 根据资产分类，需要现场销毁某些设备。

在安全控制的空间之外传输 Microsoft 数字媒体需要监督两个数据中心运营团队成员。 资产由授权人员持续伴随并监督，直至销毁。

数据中心管理团队通过票证工具中跟踪的票证控制信息系统组件的交付和删除。 信息系统组件的交付和删除由系统所有者授权。

## <a name="asset-retention"></a>资产保留

根据公司记录管理设置的保留要求、资产分类或合同要求，适当保留 Microsoft 拥有的资产。 有关数据保留详细信息，请参阅数据保留[、删除和销毁Microsoft 365。](assurance-data-retention-deletion-and-destruction-overview.md)
