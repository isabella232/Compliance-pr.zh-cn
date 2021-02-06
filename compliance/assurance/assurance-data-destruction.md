---
title: Microsoft 365 中数据销毁
description: 有关回收、处置或销毁 Microsoft 365 数据中心磁盘驱动器和服务器的 Microsoft 策略概述。
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
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: d97c5f1be6bf09a772244aac14086171643af89e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120671"
---
# <a name="data-destruction-in-microsoft-365"></a>Microsoft 365 中数据销毁

## <a name="physical-data-destruction"></a>物理数据销毁

Microsoft 具有可处理磁盘驱动器和出现故障或停用服务器的回收和处置的数据处理标准策略。 在重新使用任何 Microsoft 365 磁盘驱动器之前，Microsoft 会执行与国家标准和技术协会特别出版物 800-88 ([NIST SP 800-88](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf) 媒体安全指南一致的物理) 。 由于 Microsoft 365 中所有磁盘驱动器都使用 BitLocker 卷级加密进行加密，因此从技术上说，不需要 NIST SP 800-88 兼容擦除。 尽管如此，Microsoft 仍执行此过程。

Microsoft 365 数据中心内使用的故障磁盘通过 ISO 过程以物理方式销毁和审核。 资产类型确定适当的处置方式。 对于无法擦除的硬盘驱动器，Microsoft 使用销毁过程销毁媒体，使信息恢复变得不可能。 例如，磁盘会以物理方式销毁、放大或放大。 Microsoft 保留销毁的所有记录，并在 Microsoft 365 中重复使用的服务器上执行类似的恢复过程。 这些指南包括电子和物理安全。

每个数据中心都使用现场物理销毁过程处理其磁盘。 指定用于磁盘处置的存储媒体的安全箱位于数据中心的每个区域中。 每个安全站都有视频监控监控。 处置站达到大约 50% 的容量后，网站服务团队会联系物理安全团队以协调删除操作。 网站服务人员和安全办公室删除安全处置箱，将其放在指定的安全存储区域中。 在处置过程中管理数据承载设备的处理的策略和过程会定期进行测试，包括确保批准销毁的销毁条件的程序。

在数据销毁过程中，磁盘的擦除方式与 NIST 800-88 (（如果可能）) ，然后放入工业服务器，并实际进行擦除。 Microsoft 对使用 NIST SP 800-88 一致的清理/清除、资产销毁、加密、准确的清单、跟踪和保护传输期间锁链的资产负责。 此过程通过封闭电路电视进行监视，并且完成时将颁发销毁证书。

Microsoft 使用来自极端协议解决方案的数据擦除单元 [ (](https://www.enterprisedataerasure.com/) EPS) 。 EPS 软件支持 NIST SP 800-88 清理和清除/安全擦除要求。 清理或销毁之前，清单由 Microsoft 资产管理者创建。 如果供应商用于销毁，则供应商会为销毁的每个资产提供销毁证书，该证书由资产管理者验证。

## <a name="virtual-data-destruction"></a>虚拟数据销毁

Microsoft 具有可解决数据的有效虚拟销毁的数据处理策略和过程，防止数据在服务租户之间不当共享或在服务中硬删除后可访问。 从一个租户中的服务中删除的数据不能供另一个服务租户访问，即使重新分配了任何基础物理存储。 这是多种虚拟化和碎片技术（用于扩展虚拟环境）的复合效果、每个服务租户 (中应用程序的活动删除行为（如页面清零 [) ）](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing) 以及所需的媒体和应用程序内容加密过程的结果。