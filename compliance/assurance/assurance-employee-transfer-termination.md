---
title: Microsoft 员工转移和离职
description: 了解 Microsoft 员工离职和离职Microsoft 365
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
hideEdit: true
ms.openlocfilehash: 4a71ab3ddf6688df5480a8f260e004778aa6212b
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573357"
---
# <a name="microsoft-employee-transfer-and-termination"></a>Microsoft 员工转移和离职

与其他每个组织一样，Microsoft 会处理员工离职和离职问题，这是其正常业务运营的一部分。 当员工更改职位或离开公司时，必须及时撤销不适当的访问权限。 为了推动高效的访问更改和访问吊销，Microsoft 使用标准化过程和自动化流程来协调人力资源信息系统 (HRIS) 与标识管理 (IDM) 系统。 这两个系统之间的自动协调对于维护运营一致性、保护 Microsoft 的联机服务和数据、防止特权妨碍以及降低与内部威胁相关的风险至关重要。

Microsoft 在线服务旨在运行，无需为工程师提供对生产环境的管理访问权限。 Microsoft 使用实时 (JIT) Just-Enough-Access (JEA) 模型为工程师提供所需的临时访问权限，以便根据需要支持他们的服务。 若要请求并使用服务团队帐户进行 JIT 访问，工程师必须通过 IDM 工具请求和维护资格。 当员工被转移或离职时，将自动修改其服务团队帐户和相关资格，以防止不当访问。

## <a name="transfer-and-reassignment"></a>转移和重新分配

员工转移是通过员工经理的转移交易请求启动的。 经理创建了一个工厂，并参与全球人才招聘流程。 员工接受新角色的优惠后，HR 服务将完成 HR 核心工具中的转移，从而触发 IDM 设置所有员工资格的到期日期。 员工必须提交请求并收到新经理的批准，以保留其资格。 提交请求或接收经理批准失败会导致被转移的员工资格吊销。 对于包含特定安全隐患的传输，将立即重新评估系统访问和安全组成员身份以反映其新角色。

## <a name="termination"></a>终止

当员工离职时，Microsoft 使用明确定义的策略和过程来立即撤消对 Microsoft 系统和资源的物理和逻辑访问。 当员工发出通知时，员工的经理会向 HRIS 输入终止日期。 在员工最后一个工作日之后，HRIS 将员工标记为已终止，并共享信息给 IDM，这将自动删除所有服务团队帐户和资格。

对于雇佣终止，HR 与员工的经理合作，以按照相应步骤终止和离职员工。 与自愿终止类似，终止信息连同任何必要步骤（如有效日期协调、删除访问）一起输入到 HRIS 中。 和与转换角色相关的任何其他步骤。
