---
title: Microsoft 365 中的数据不可变性
description: 了解 Microsoft 365 如何以可发现的形式保留数据，以解决法规合规性、内部管理要求和诉讼风险。
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
ms.openlocfilehash: 2e86cdfe082ec35fd7fd111a13a4def6f1b01806
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497632"
---
# <a name="data-immutability-in-microsoft-365"></a><span data-ttu-id="e1798-103">Microsoft 365 中的数据不可变性</span><span class="sxs-lookup"><span data-stu-id="e1798-103">Data immutability in Microsoft 365</span></span>

<span data-ttu-id="e1798-104">法规遵从性、内部管理要求或诉讼风险要求组织以可发现的形式保留电子邮件和关联数据。</span><span class="sxs-lookup"><span data-stu-id="e1798-104">Regulatory compliance, internal governance requirements, or litigation risks require organizations to preserve email and associated data in a discoverable form.</span></span> <span data-ttu-id="e1798-105">系统内的所有数据都必须可发现，并且不能销毁或更改任何数据。</span><span class="sxs-lookup"><span data-stu-id="e1798-105">All data in the system must be discoverable and none of it can be destroyed or altered.</span></span> <span data-ttu-id="e1798-106">针对此的行业标准术语是"不可变"。</span><span class="sxs-lookup"><span data-stu-id="e1798-106">The industry-standard term for this is "immutability."</span></span>

<span data-ttu-id="e1798-107">用于不可变的传统方法通常通过将电子邮件移动到单独的只读存储位置来有效。</span><span class="sxs-lookup"><span data-stu-id="e1798-107">Traditional methods for immutability typically worked by moving email messages to a separate, read-only storage location.</span></span> <span data-ttu-id="e1798-108">虽然此类系统用于保留邮箱项目以便进行发现，但是它们通常会通过从日常工作流中删除保留的项目来影响用户体验。</span><span class="sxs-lookup"><span data-stu-id="e1798-108">While such systems serve the purpose of preserving mailbox items for discovery, they often affect the user experience by removing preserved items from the customary daily workflow.</span></span> <span data-ttu-id="e1798-109">对于 IT 专业人员，这种不可变方法要求部署和持续维护单独的服务器和存储基础结构。</span><span class="sxs-lookup"><span data-stu-id="e1798-109">For IT professionals, this immutability approach requires the deployment and ongoing maintenance of a separate server and storage infrastructure.</span></span> <span data-ttu-id="e1798-110">使用邮件系统外部的工具执行发现，其中包括关联的部署和维护成本。</span><span class="sxs-lookup"><span data-stu-id="e1798-110">Discovery is performed with tools external to the mail system and includes associated deployment and maintenance costs.</span></span>

<span data-ttu-id="e1798-111">通过 Microsoft 365 及其服务中存档的就地保留和保留策略功能，可以保留传入、内部和传出数据的许多类。</span><span class="sxs-lookup"><span data-stu-id="e1798-111">Through in-place retention and preservation policy features of archiving in Microsoft 365 and its services, you can preserve and retain many classes of incoming, internal, and outgoing data.</span></span> <span data-ttu-id="e1798-112">这包括：</span><span class="sxs-lookup"><span data-stu-id="e1798-112">This includes:</span></span>

- <span data-ttu-id="e1798-113">入站和出站电子邮件通信</span><span class="sxs-lookup"><span data-stu-id="e1798-113">Inbound and outbound email communications</span></span>
- <span data-ttu-id="e1798-114">电子邮件窗体或共享联机文档中包含的书籍和记录</span><span class="sxs-lookup"><span data-stu-id="e1798-114">Books and records contained in email form or in shared online documents</span></span>
- <span data-ttu-id="e1798-115">会议请求</span><span class="sxs-lookup"><span data-stu-id="e1798-115">Meeting requests</span></span>
- <span data-ttu-id="e1798-116">传真</span><span class="sxs-lookup"><span data-stu-id="e1798-116">Faxes</span></span>
- <span data-ttu-id="e1798-117">即时消息</span><span class="sxs-lookup"><span data-stu-id="e1798-117">Instant messages</span></span>
- <span data-ttu-id="e1798-118">联机会议期间共享的文档</span><span class="sxs-lookup"><span data-stu-id="e1798-118">Documents shared during online meetings</span></span>
- <span data-ttu-id="e1798-119">语音邮件</span><span class="sxs-lookup"><span data-stu-id="e1798-119">Voicemails</span></span>

<span data-ttu-id="e1798-120">此外，Microsoft 还开发了附加功能，允许通过与第[](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc)三方数据捕获和管理解决方案集成来存档来自其他源的数据。</span><span class="sxs-lookup"><span data-stu-id="e1798-120">In addition, Microsoft has developed add-on features to allow [archiving of data](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) from other sources through integration with third-party data capturing and management solutions.</span></span> <span data-ttu-id="e1798-121">导入第三方数据后，可以将 Microsoft 365 合规性功能应用于数据，包括：</span><span class="sxs-lookup"><span data-stu-id="e1798-121">After third-party data is imported, you can apply Microsoft 365 compliance features to the data, including:</span></span>

- [<span data-ttu-id="e1798-122">诉讼保留</span><span class="sxs-lookup"><span data-stu-id="e1798-122">Litigation Hold</span></span>](/microsoft-365/compliance/create-a-litigation-hold)
- [<span data-ttu-id="e1798-123">就地电子数据展示和保留</span><span class="sxs-lookup"><span data-stu-id="e1798-123">In-Place eDiscovery and Hold</span></span>](/microsoft-365/compliance/manage-legal-investigations)
- [<span data-ttu-id="e1798-124">合规性搜索</span><span class="sxs-lookup"><span data-stu-id="e1798-124">Compliance Search</span></span>](/microsoft-365/compliance/search-for-content)
- [<span data-ttu-id="e1798-125">就地存档</span><span class="sxs-lookup"><span data-stu-id="e1798-125">In-Place Archiving</span></span>](/microsoft-365/compliance/enable-archive-mailboxes)
- [<span data-ttu-id="e1798-126">邮箱审核</span><span class="sxs-lookup"><span data-stu-id="e1798-126">Mailbox auditing</span></span>](/microsoft-365/compliance/enable-mailbox-auditing)
- [<span data-ttu-id="e1798-127">保留策略</span><span class="sxs-lookup"><span data-stu-id="e1798-127">Retention Policies</span></span>](/microsoft-365/compliance/retention-policies)

<span data-ttu-id="e1798-128">例如，当邮箱置于诉讼保留时，将保留第三方数据。</span><span class="sxs-lookup"><span data-stu-id="e1798-128">For example, when a mailbox is placed on Litigation Hold, third-party data is preserved.</span></span> <span data-ttu-id="e1798-129">可以使用电子数据展示或合规性搜索In-Place第三方数据。</span><span class="sxs-lookup"><span data-stu-id="e1798-129">You can search third-party data using In-Place eDiscovery or Compliance Search.</span></span> <span data-ttu-id="e1798-130">也可以像对 Microsoft 数据一样将存档和保留策略应用于第三方数据。</span><span class="sxs-lookup"><span data-stu-id="e1798-130">Or you can apply archiving and retention policies to third-party data just like you can for Microsoft data.</span></span> <span data-ttu-id="e1798-131">在 Microsoft 365 中存档第三方数据可帮助你的组织遵守政府及法规策略。</span><span class="sxs-lookup"><span data-stu-id="e1798-131">Archiving third-party data in Microsoft 365 helps your organization stay compliant with government and regulatory policies.</span></span>

<span data-ttu-id="e1798-132">Microsoft 365 中的存档向美国证券交易委员会 (SEC) 规则 17a-4 兼容存储。</span><span class="sxs-lookup"><span data-stu-id="e1798-132">Archiving in Microsoft 365 provides Securities and Exchange Commission (SEC) Rule 17a-4-compliant storage.</span></span> <span data-ttu-id="e1798-133">Microsoft 365 使用就地保留策略和保留策略（包括保留锁定）保留以不可重写、不可擦除格式收集的所有数据的永久文件。</span><span class="sxs-lookup"><span data-stu-id="e1798-133">Microsoft 365 preserves permanent files of all data collected in a non-rewriteable, non-erasable format using in-place retention policies and preservation policies, including preservation lock.</span></span>

<span data-ttu-id="e1798-134">具体来说：</span><span class="sxs-lookup"><span data-stu-id="e1798-134">Specifically:</span></span>

- <span data-ttu-id="e1798-135">使用上述保留策略存储的所有记录都保存在普通用户的专用存储区域中。</span><span class="sxs-lookup"><span data-stu-id="e1798-135">All records stored using the retention policies noted above are retained in a dedicated storage area out of the purview of the ordinary user.</span></span> <span data-ttu-id="e1798-136">只有授权用户可以访问和搜索这些记录，但不能更改或清除它们。</span><span class="sxs-lookup"><span data-stu-id="e1798-136">Only authorized users can access and search these records, but cannot alter or erase them.</span></span>
- <span data-ttu-id="e1798-137">每个项目的元数据包括用于计算保留期的时间戳。</span><span class="sxs-lookup"><span data-stu-id="e1798-137">Metadata for each item includes a timestamp used in the calculation of retention duration.</span></span> <span data-ttu-id="e1798-138">当收到或创建一个新项，并且无法修改或删除元数据时，将应用时间戳。</span><span class="sxs-lookup"><span data-stu-id="e1798-138">Timestamps are applied when a new item is received or created and cannot be modified or removed from the metadata.</span></span>
- <span data-ttu-id="e1798-139">Microsoft 365 中的存档允许用户组合不同的保留策略和保留操作以创建精细的保留策略。</span><span class="sxs-lookup"><span data-stu-id="e1798-139">Archiving in Microsoft 365 allows users to combine different retention policies and hold actions to create granular retention policies.</span></span> <span data-ttu-id="e1798-140">这些策略定义保留项的类型或位置以及保留持续时间。</span><span class="sxs-lookup"><span data-stu-id="e1798-140">These policies define the type or location of the items preserved and the duration of preservation.</span></span>
- <span data-ttu-id="e1798-141">保留锁定功能允许用户选择是否使策略成为限制性策略。</span><span class="sxs-lookup"><span data-stu-id="e1798-141">The Preservation Lock feature allows users to choose whether to make the policy a restrictive policy.</span></span> <span data-ttu-id="e1798-142">限制性策略禁止任何人删除、禁用或更改保留策略。</span><span class="sxs-lookup"><span data-stu-id="e1798-142">A restrictive policy prohibits anyone from having the ability to remove, disable, or make any changes to the retention policy.</span></span> <span data-ttu-id="e1798-143">这意味着，一旦启用保留锁定，就无法禁用它，并且不存在这样一种机制，在保留期间，保留策略收集的现有保管人的任何数据都将被覆盖、修改、擦除或删除。</span><span class="sxs-lookup"><span data-stu-id="e1798-143">This means that once Preservation Lock is enabled, it cannot be disabled, and no mechanism will exist under which any data from existing custodians that has been collected by the retention policies in place may be overwritten, modified, erased, or deleted during the preservation period.</span></span> <span data-ttu-id="e1798-144">此外，保留锁定设置的保留期可能不会缩短或减少。</span><span class="sxs-lookup"><span data-stu-id="e1798-144">Further, the hold period set by Preservation Lock may not be shortened or decreased.</span></span> <span data-ttu-id="e1798-145">但是，如果法律要求继续保留存储的数据，可能会延长，如上所述。</span><span class="sxs-lookup"><span data-stu-id="e1798-145">It may, however, be lengthened, in the case of a legal requirement to continue retention of the stored data, as noted above.</span></span> <span data-ttu-id="e1798-146">保留锁定可确保任何人（甚至是管理员或具有特定控制访问权限的管理员）都不得更改设置或覆盖或擦除已存储的数据，使 Microsoft 365 中的存档符合 2003 年发布的 SEC 规则 17a-4 中规定的指导。</span><span class="sxs-lookup"><span data-stu-id="e1798-146">Preservation Lock ensures that no one, not even administrators or those with certain control access, may change the settings or overwrite or erase data that has been stored, bringing archiving in Microsoft 365 in line with the guidance set forth in the 2003 Release of SEC Rule 17a-4.</span></span>

<span data-ttu-id="e1798-147">若要了解 Microsoft 365 如何帮助您履行法规义务，尤其是与规则 17a-4 要求相关的义务，[](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf)请参阅涵盖 Exchange Online Archiving、SharePoint Online、OneDrive for Business 和 Skype for Business 的白皮书。</span><span class="sxs-lookup"><span data-stu-id="e1798-147">To understand how Microsoft 365 helps you meet regulatory obligations, specifically in relation to Rule 17a-4 requirements, see the [whitepaper](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf) that covers Exchange Online Archiving, SharePoint Online, OneDrive for Business, and Skype for Business.</span></span> <span data-ttu-id="e1798-148">该白皮书还根据 SEC 规则 17a-4 中的每个要求深入分析了 Microsoft 365 存档特性和功能，并演示了受监管客户 Microsoft 365 存档如何帮助他们满足这些要求。</span><span class="sxs-lookup"><span data-stu-id="e1798-148">The whitepaper also provides an in-depth analysis of Microsoft 365 archiving features and functionalities against each of the requirements under SEC Rule 17a-4 and demonstrates to regulated customers how Microsoft 365 archiving can enable them to meet these requirements.</span></span>
