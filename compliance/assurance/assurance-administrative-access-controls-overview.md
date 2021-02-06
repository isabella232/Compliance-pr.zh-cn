---
title: Microsoft 365 中的管理访问控制
description: 本文概述了 Microsoft 365 中的管理访问控制和数据分类。
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: d3d6cd30fbe682de979d5c04943c57cedc86552f
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120711"
---
# <a name="administrative-access-controls-in-microsoft-365"></a><span data-ttu-id="fecb7-103">Microsoft 365 中的管理访问控制</span><span class="sxs-lookup"><span data-stu-id="fecb7-103">Administrative access controls in Microsoft 365</span></span> 

<span data-ttu-id="fecb7-104">Microsoft 在自动执行大多数 Microsoft 365 操作的同时有意限制 Microsoft 访问客户内容的系统和控件方面投入大量资金。</span><span class="sxs-lookup"><span data-stu-id="fecb7-104">Microsoft has invested heavily in systems and controls that automate most Microsoft 365 operations while intentionally limiting access to customer content by Microsoft.</span></span> <span data-ttu-id="fecb7-105">人员管理服务，软件运行服务。</span><span class="sxs-lookup"><span data-stu-id="fecb7-105">Humans govern the service, and software operates the service.</span></span> <span data-ttu-id="fecb7-106">此结构使 Microsoft 能够大规模管理 Microsoft 365，并管理客户内容受到内部威胁的风险。</span><span class="sxs-lookup"><span data-stu-id="fecb7-106">This structure enables Microsoft to manage Microsoft 365 at scale and manage the risks of internal threats to customer content.</span></span>

<span data-ttu-id="fecb7-107">默认情况下，Microsoft 工程师在 Microsoft 365 中具有零长期管理权限和零长期客户内容访问权限。</span><span class="sxs-lookup"><span data-stu-id="fecb7-107">By default, Microsoft engineers have zero standing administrative privileges and zero standing access to customer content in Microsoft 365.</span></span> <span data-ttu-id="fecb7-108">Microsoft 工程师可以在有限时间内限制、审核和安全访问客户的内容。</span><span class="sxs-lookup"><span data-stu-id="fecb7-108">A Microsoft engineer can have limited, audited, and secured access to a customer's content for a limited amount of time.</span></span> <span data-ttu-id="fecb7-109">只有在服务操作需要访问时，并且仅在 Microsoft 高层管理人员批准时访问。</span><span class="sxs-lookup"><span data-stu-id="fecb7-109">Access is only when necessary for service operations and only when approved by a member of Microsoft senior management.</span></span> <span data-ttu-id="fecb7-110">对于客户密码箱许可客户，客户提供对 Microsoft 365 上托管的内容的访问审批。</span><span class="sxs-lookup"><span data-stu-id="fecb7-110">For Customer Lockbox licensed customers, the customer provides access approval to their content hosted on Microsoft 365.</span></span>

<span data-ttu-id="fecb7-111">Microsoft 使用多种云交付形式提供联机服务：</span><span class="sxs-lookup"><span data-stu-id="fecb7-111">Microsoft provides online services using multiple forms of cloud delivery:</span></span>

- <span data-ttu-id="fecb7-112">**公共云：** 包括 Microsoft 365、Azure 以及北美、北美、欧洲、亚洲、澳大利亚等托管的其他服务的多租户版本。</span><span class="sxs-lookup"><span data-stu-id="fecb7-112">**Public clouds:** Includes multi-tenant versions of Microsoft 365, Azure, and other services hosted in North America, South America, Europe, Asia, Australia, etc.</span></span>
- <span data-ttu-id="fecb7-113">**国家云：** 包括美国 () 之外的所有自主和第三方运营的云，但之前提到的云除外，例如由世纪银行运营的中国 Microsoft 365)  (和由 Microsoft 运营的德国 microsoft 365 (，但采用一种模型，德国数据受托人德国电信控制并监视 Microsoft 对包含客户数据) 的客户数据和系统的访问权限。</span><span class="sxs-lookup"><span data-stu-id="fecb7-113">**National clouds:** Includes all sovereign and third party-operated clouds outside of the United States (except ones noted previously), such as Microsoft 365 in China (operated by 21Vianet), and Microsoft 365 in Germany (operated by Microsoft, but under a model in which a German data trustee, Deutsche Telekom, controls and monitors Microsoft's access to customer data and systems that contain customer data).</span></span>
- <span data-ttu-id="fecb7-114">**政府云：** 包括可供美国政府客户使用 Microsoft 365 和 Azure 服务。</span><span class="sxs-lookup"><span data-stu-id="fecb7-114">**Government clouds:** Includes Microsoft 365 and Azure services that are available to United States government customers.</span></span>

<span data-ttu-id="fecb7-115">对于本文，Microsoft 365 服务包括：</span><span class="sxs-lookup"><span data-stu-id="fecb7-115">For purposes of this article, Microsoft 365 services include:</span></span>

- [<span data-ttu-id="fecb7-116">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="fecb7-116">Exchange Online</span></span>](/Exchange/exchange-online)
- [<span data-ttu-id="fecb7-117">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="fecb7-117">Exchange Online Protection</span></span>](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [<span data-ttu-id="fecb7-118">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="fecb7-118">SharePoint Online</span></span>](/sharepoint/sharepoint-online)
- [<span data-ttu-id="fecb7-119">OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="fecb7-119">OneDrive for Business</span></span>](/OneDrive/onedrive)
- [<span data-ttu-id="fecb7-120">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="fecb7-120">Skype for Business</span></span>](/SkypeForBusiness/skype-for-business-online)
- [<span data-ttu-id="fecb7-121">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="fecb7-121">Microsoft Teams</span></span>](/MicrosoftTeams/Teams-overview)
- [<span data-ttu-id="fecb7-122">Yammer</span><span class="sxs-lookup"><span data-stu-id="fecb7-122">Yammer</span></span>](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a><span data-ttu-id="fecb7-123">Microsoft 365 访问控制</span><span class="sxs-lookup"><span data-stu-id="fecb7-123">Microsoft 365 access controls</span></span>

<span data-ttu-id="fecb7-124">出于访问控制目的，Microsoft 将 Microsoft 365 数据分类为客户数据或其他类型的数据。</span><span class="sxs-lookup"><span data-stu-id="fecb7-124">For access control purposes, Microsoft categorizes Microsoft 365 data as customer data or other types of data.</span></span>

### <a name="customer-data"></a><span data-ttu-id="fecb7-125">客户数据</span><span class="sxs-lookup"><span data-stu-id="fecb7-125">Customer data</span></span>

<span data-ttu-id="fecb7-126">客户数据是客户在使用 Microsoft 365 服务时或代表客户提供的所有数据。</span><span class="sxs-lookup"><span data-stu-id="fecb7-126">Customer data is all data provided by or on behalf of a customer when using Microsoft 365 services.</span></span> <span data-ttu-id="fecb7-127">此数据是由 Microsoft 365 用户直接创建或上载的客户内容，包括：</span><span class="sxs-lookup"><span data-stu-id="fecb7-127">This data is customer content directly created or uploaded by Microsoft 365 users, including:</span></span>

- <span data-ttu-id="fecb7-128">电子邮件</span><span class="sxs-lookup"><span data-stu-id="fecb7-128">Emails</span></span>
- <span data-ttu-id="fecb7-129">SharePoint Online 内容</span><span class="sxs-lookup"><span data-stu-id="fecb7-129">SharePoint Online content</span></span>
- <span data-ttu-id="fecb7-130">即时消息</span><span class="sxs-lookup"><span data-stu-id="fecb7-130">Instant messages</span></span>
- <span data-ttu-id="fecb7-131">日历项目</span><span class="sxs-lookup"><span data-stu-id="fecb7-131">Calendar items</span></span>
- <span data-ttu-id="fecb7-132">文档</span><span class="sxs-lookup"><span data-stu-id="fecb7-132">Documents</span></span>
- <span data-ttu-id="fecb7-133">联系人</span><span class="sxs-lookup"><span data-stu-id="fecb7-133">Contacts</span></span>
- <span data-ttu-id="fecb7-134">EUII 的最终用户 (信息)  (用户唯一的数据，或可链接到单个用户但不包括客户内容) </span><span class="sxs-lookup"><span data-stu-id="fecb7-134">End-user identifiable information (EUII) (data that is unique to a user or that is linkable to an individual user but does not include customer content)</span></span>

### <a name="other-types-of-data"></a><span data-ttu-id="fecb7-135">其他类型的数据</span><span class="sxs-lookup"><span data-stu-id="fecb7-135">Other types of data</span></span>

<span data-ttu-id="fecb7-136">其他类型的数据包括：</span><span class="sxs-lookup"><span data-stu-id="fecb7-136">Other types of data include:</span></span>

- <span data-ttu-id="fecb7-137">**帐户数据：** 包括管理员 (或购买服务时提供的管理数据) 信息，以及付款 (支付工具信息，如信用卡详细信息) 。</span><span class="sxs-lookup"><span data-stu-id="fecb7-137">**Account data:** Includes administrative data (information provided by administrators when they sign-up or purchase services), and payment data (information about payment instruments, such as credit card details).</span></span>
- <span data-ttu-id="fecb7-138">**组织可识别信息：** 包括用于标识租户的数据、使用情况数据，且无法链接到单个用户或包含在客户内容中。</span><span class="sxs-lookup"><span data-stu-id="fecb7-138">**Organizationally identifiable information:** Includes data used to identify a tenant, usage data, and not linkable to an individual user or included in customer content.</span></span>
- <span data-ttu-id="fecb7-139">**系统元数据：** 包括包含配置设置、系统状态、Microsoft IP 地址和有关订阅和租户的技术信息的服务日志。</span><span class="sxs-lookup"><span data-stu-id="fecb7-139">**System metadata:** Includes service logs that contain configuration settings, system status, Microsoft IP addresses, and technical information about subscriptions and tenants.</span></span>

<span data-ttu-id="fecb7-140">Microsoft 已建立访问控制机制，以确保没有人能够未经批准地访问客户数据或访问控制数据。</span><span class="sxs-lookup"><span data-stu-id="fecb7-140">Microsoft has established access control mechanisms to ensure that no one has unapproved access to Customer Data or access control data.</span></span> <span data-ttu-id="fecb7-141">访问控制数据管理对环境中其他类型的数据或功能的访问，包括访问客户内容或 EUII、Microsoft 密码、安全证书和其他与身份验证相关的数据。</span><span class="sxs-lookup"><span data-stu-id="fecb7-141">Access control data manages access to other types of data or functions within the environment, including access to customer content or EUII, Microsoft passwords, security certificates, and other authentication-related data.</span></span> <span data-ttu-id="fecb7-142">访问控制机制还防止对 Microsoft 365 生产环境进行未经批准的物理、逻辑或远程访问。</span><span class="sxs-lookup"><span data-stu-id="fecb7-142">Access control mechanisms also guard against unapproved physical, logical, or remote access to the Microsoft 365 production environment.</span></span>

<span data-ttu-id="fecb7-143">Microsoft 使用三类访问控制来运行 Microsoft 365：</span><span class="sxs-lookup"><span data-stu-id="fecb7-143">There are three categories of access controls used by Microsoft for operating Microsoft 365:</span></span>

- <span data-ttu-id="fecb7-144">隔离控件</span><span class="sxs-lookup"><span data-stu-id="fecb7-144">Isolation controls</span></span>
- <span data-ttu-id="fecb7-145">人员控制</span><span class="sxs-lookup"><span data-stu-id="fecb7-145">Personnel controls</span></span>
- <span data-ttu-id="fecb7-146">技术控制</span><span class="sxs-lookup"><span data-stu-id="fecb7-146">Technology controls</span></span>

<span data-ttu-id="fecb7-147">组合后，这些控件有助于阻止和检测 Microsoft 365 中的恶意操作。</span><span class="sxs-lookup"><span data-stu-id="fecb7-147">When combined, these controls help prevent and detect malicious actions in Microsoft 365.</span></span> <span data-ttu-id="fecb7-148">除了 Microsoft 使用的隔离、人员和技术控制外，还有第四类控件：客户实施的这些控件。</span><span class="sxs-lookup"><span data-stu-id="fecb7-148">In addition to the isolation, personnel, and technology controls used by Microsoft, there is a fourth category of controls: those controls implemented by customers.</span></span>

<span data-ttu-id="fecb7-149">Microsoft 365 允许您以在本地环境中管理数据的相同方式管理数据。</span><span class="sxs-lookup"><span data-stu-id="fecb7-149">Microsoft 365 allows you to manage data the same way data is managed in on-premises environments.</span></span> <span data-ttu-id="fecb7-150">注册 Microsoft 365 组织的人将自动成为全局管理员。</span><span class="sxs-lookup"><span data-stu-id="fecb7-150">The person who signs up an organization for Microsoft 365 automatically becomes a global administrator.</span></span> <span data-ttu-id="fecb7-151">全局管理员有权访问管理门户中所有功能，并且可以：</span><span class="sxs-lookup"><span data-stu-id="fecb7-151">The global admin has access to all features in Management Portals and can:</span></span>

- <span data-ttu-id="fecb7-152">创建或编辑用户</span><span class="sxs-lookup"><span data-stu-id="fecb7-152">Create or edit users</span></span>
- <span data-ttu-id="fecb7-153">将管理员角色分配给其他人</span><span class="sxs-lookup"><span data-stu-id="fecb7-153">Assign admin roles to others</span></span>
- <span data-ttu-id="fecb7-154">重置用户密码</span><span class="sxs-lookup"><span data-stu-id="fecb7-154">Reset user passwords</span></span>
- <span data-ttu-id="fecb7-155">管理用户许可证</span><span class="sxs-lookup"><span data-stu-id="fecb7-155">Manage user licenses</span></span>
- <span data-ttu-id="fecb7-156">管理域</span><span class="sxs-lookup"><span data-stu-id="fecb7-156">Manage domains</span></span>
- <span data-ttu-id="fecb7-157">批准客户密码箱请求</span><span class="sxs-lookup"><span data-stu-id="fecb7-157">Approve Customer Lockbox requests</span></span>

<span data-ttu-id="fecb7-158">我们建议每个组织至少配置两个管理员帐户。</span><span class="sxs-lookup"><span data-stu-id="fecb7-158">We recommend that each organization configure at least two admin accounts.</span></span> <span data-ttu-id="fecb7-159">对于大型企业组织，我们建议使用为不同功能服务的专用管理员帐户。</span><span class="sxs-lookup"><span data-stu-id="fecb7-159">For large enterprise organizations, we recommend specialized admin accounts that serve different functions.</span></span>

<span data-ttu-id="fecb7-160">有关分配管理员角色和权限的信息，请参阅分配 [管理员角色](/microsoft-365/admin/add-users/assign-admin-roles) 和 [关于管理员角色](/microsoft-365/admin/add-users/about-admin-roles)。</span><span class="sxs-lookup"><span data-stu-id="fecb7-160">For information about assigning admin roles and permissions, see [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles) and [About admin roles](/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-links"></a><span data-ttu-id="fecb7-161">相关链接</span><span class="sxs-lookup"><span data-stu-id="fecb7-161">Related Links</span></span>

- [<span data-ttu-id="fecb7-162">Microsoft 365 中的隔离</span><span class="sxs-lookup"><span data-stu-id="fecb7-162">Isolation in Microsoft 365</span></span>](assurance-isolation-in-microsoft-365.md)
- [<span data-ttu-id="fecb7-163">Microsoft 聘用前筛选</span><span class="sxs-lookup"><span data-stu-id="fecb7-163">Microsoft pre-employment screening</span></span>](assurance-pre-employment-screening.md)
- [<span data-ttu-id="fecb7-164">Microsoft 云背景核查</span><span class="sxs-lookup"><span data-stu-id="fecb7-164">Microsoft cloud background check</span></span>](assurance-cloud-background-check.md)
- [<span data-ttu-id="fecb7-165">监视和审核访问控制</span><span class="sxs-lookup"><span data-stu-id="fecb7-165">Monitoring and Auditing Access Controls</span></span>](assurance-monitoring-and-auditing-access-controls.md)
- [<span data-ttu-id="fecb7-166">Yammer Enterprise 访问控制</span><span class="sxs-lookup"><span data-stu-id="fecb7-166">Yammer Enterprise Access Controls</span></span>](assurance-yammer-enterprise-access-controls.md)
