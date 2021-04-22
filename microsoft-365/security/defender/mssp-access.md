---
title: Fournir un accès au fournisseur de services de sécurité gérés (MSSP)
description: En savoir plus sur les modifications apportées au Centre de sécurité Microsoft Defender vers le Centre de sécurité Microsoft 365
keywords: Mise en place du Centre de sécurité Microsoft 365, Microsoft Defender pour Office 365, Microsoft Defender pour le point de terminaison, MDO, MDE, volet unique, portail convergé, portail de sécurité, portail de sécurité Defender
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
localization_priority: Normal
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
manager: dansimp
audience: ITPro
ms.topic: article
search.appverid:
- MOE150
- MET150
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.openlocfilehash: 4b34d3ea20716fb2424d9317b8a51c088a5714a6
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935352"
---
# <a name="provide-managed-security-service-provider-mssp-access"></a><span data-ttu-id="3eeed-104">Fournir un accès au fournisseur de services de sécurité gérés (MSSP)</span><span class="sxs-lookup"><span data-stu-id="3eeed-104">Provide managed security service provider (MSSP) access</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

[!INCLUDE [Prerelease](../includes/prerelease.md)]

<span data-ttu-id="3eeed-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3eeed-105">**Applies to:**</span></span>

- [<span data-ttu-id="3eeed-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3eeed-106">Microsoft 365 Defender</span></span>](microsoft-365-defender.md)
- [<span data-ttu-id="3eeed-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3eeed-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

<span data-ttu-id="3eeed-108">Pour implémenter une solution d'accès délégué multi-locataire, prenez les mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eeed-108">To implement a multi-tenant delegated access solution, take the following steps:</span></span>

1. <span data-ttu-id="3eeed-109">Activez le contrôle d'accès basé sur les rôles dans Defender pour le point de terminaison dans le Centre de sécurité Microsoft 365 et [connectez-vous](/windows/security/threat-protection/microsoft-defender-atp/rbac) aux groupes Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="3eeed-109">Enable [role-based access control](/windows/security/threat-protection/microsoft-defender-atp/rbac) in Defender for Endpoint in Microsoft 365 security center and connect with Azure Active Directory (Azure AD) groups.</span></span>

2. <span data-ttu-id="3eeed-110">Configurer des [packages d'accès de gouvernance pour](/azure/active-directory/governance/identity-governance-overview) la demande d'accès et la mise en service.</span><span class="sxs-lookup"><span data-stu-id="3eeed-110">Configure [Governance Access Packages](/azure/active-directory/governance/identity-governance-overview) for access request and provisioning.</span></span>

3. <span data-ttu-id="3eeed-111">Gérer les demandes d'accès et les audits [dans Microsoft Myaccess](/azure/active-directory/governance/entitlement-management-request-approve).</span><span class="sxs-lookup"><span data-stu-id="3eeed-111">Manage access requests and audits in [Microsoft Myaccess](/azure/active-directory/governance/entitlement-management-request-approve).</span></span>

## <a name="enable-role-based-access-controls-in-microsoft-defender-for-endpoint-in-microsoft-365-security-center"></a><span data-ttu-id="3eeed-112">Activer les contrôles d'accès basés sur les rôles dans Microsoft Defender pour le point de terminaison dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3eeed-112">Enable role-based access controls in Microsoft Defender for Endpoint in Microsoft 365 security center</span></span>

1. <span data-ttu-id="3eeed-113">**Créer des groupes d'accès pour les ressources MSSP dans Customer AAD : Groupes**</span><span class="sxs-lookup"><span data-stu-id="3eeed-113">**Create access groups for MSSP resources in Customer AAD: Groups**</span></span>

    <span data-ttu-id="3eeed-114">Ces groupes seront liés aux rôles que vous créez dans Defender for Endpoint dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3eeed-114">These groups will be linked to the Roles you create in Defender for Endpoint in Microsoft 365 security center.</span></span> <span data-ttu-id="3eeed-115">Pour ce faire, dans le client AD client, créez trois groupes.</span><span class="sxs-lookup"><span data-stu-id="3eeed-115">To do so, in the customer AD tenant, create three groups.</span></span> <span data-ttu-id="3eeed-116">Dans notre exemple d'approche, nous créons les groupes suivants :</span><span class="sxs-lookup"><span data-stu-id="3eeed-116">In our example approach, we create the following groups:</span></span>

    - <span data-ttu-id="3eeed-117">Analyste de niveau 1</span><span class="sxs-lookup"><span data-stu-id="3eeed-117">Tier 1 Analyst</span></span> 
    - <span data-ttu-id="3eeed-118">Analyste de niveau 2</span><span class="sxs-lookup"><span data-stu-id="3eeed-118">Tier 2 Analyst</span></span> 
    - <span data-ttu-id="3eeed-119">Approbations d'analyste MSSP</span><span class="sxs-lookup"><span data-stu-id="3eeed-119">MSSP Analyst Approvers</span></span>  


2. <span data-ttu-id="3eeed-120">Créez des rôles Defender pour les points de terminaison pour les niveaux d'accès appropriés dans Customer Defender for Endpoint dans les rôles et groupes du Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3eeed-120">Create Defender for Endpoint roles for appropriate access levels in Customer Defender for Endpoint in Microsoft 365 security center roles and groups.</span></span>

    <span data-ttu-id="3eeed-121">Pour activer RBAC dans le Centre de sécurité Microsoft 365 client, accédez aux **autorisations > Rôles** de points de terminaison & groupes > Rôles avec un compte d'utilisateur ayant des droits d'administrateur général ou d'administrateur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3eeed-121">To enable RBAC in the customer Microsoft 365 security center, access **Permissions >  Endpoints roles & groups > Roles** with a user account with Global Administrator or Security Administrator rights.</span></span>

    ![Image de l'accès MSSP](../../media/mssp-access.png)

    <span data-ttu-id="3eeed-123">Ensuite, créez des rôles RBAC pour répondre aux besoins du niveau SOC MSSP.</span><span class="sxs-lookup"><span data-stu-id="3eeed-123">Then, create RBAC roles to meet MSSP SOC Tier needs.</span></span> <span data-ttu-id="3eeed-124">Lier ces rôles aux groupes d'utilisateurs créés via « Groupes d'utilisateurs affectés ».</span><span class="sxs-lookup"><span data-stu-id="3eeed-124">Link these roles to the created user groups via "Assigned user groups".</span></span>

    <span data-ttu-id="3eeed-125">Deux rôles possibles :</span><span class="sxs-lookup"><span data-stu-id="3eeed-125">Two possible roles:</span></span>

    - <span data-ttu-id="3eeed-126">**Analystes de niveau 1**</span><span class="sxs-lookup"><span data-stu-id="3eeed-126">**Tier 1 Analysts**</span></span> <br>
      <span data-ttu-id="3eeed-127">Effectuez toutes les actions à l'exception de la réponse en direct et gérez les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3eeed-127">Perform all actions except for live response and manage security settings.</span></span>

    - <span data-ttu-id="3eeed-128">**Analystes de niveau 2**</span><span class="sxs-lookup"><span data-stu-id="3eeed-128">**Tier 2 Analysts**</span></span> <br>
      <span data-ttu-id="3eeed-129">Fonctionnalités de niveau 1 avec l'ajout de la [réponse en direct](/windows/security/threat-protection/microsoft-defender-atp/live-response)</span><span class="sxs-lookup"><span data-stu-id="3eeed-129">Tier 1 capabilities with the addition to [live response](/windows/security/threat-protection/microsoft-defender-atp/live-response)</span></span>

    <span data-ttu-id="3eeed-130">Pour plus d'informations, voir [Utiliser le contrôle d'accès basé sur un rôle.](/windows/security/threat-protection/microsoft-defender-atp/rbac)</span><span class="sxs-lookup"><span data-stu-id="3eeed-130">For more information, see [Use role-based access control](/windows/security/threat-protection/microsoft-defender-atp/rbac).</span></span>



## <a name="configure-governance-access-packages"></a><span data-ttu-id="3eeed-131">Configurer les packages d'accès de gouvernance</span><span class="sxs-lookup"><span data-stu-id="3eeed-131">Configure Governance Access Packages</span></span>

1.  <span data-ttu-id="3eeed-132">**Ajouter MSSP en tant qu'organisation connectée dans Customer AAD : Gouvernance des identités**</span><span class="sxs-lookup"><span data-stu-id="3eeed-132">**Add MSSP as Connected Organization in Customer AAD: Identity Governance**</span></span>
    
    <span data-ttu-id="3eeed-133">L'ajout du MSSP en tant qu'organisation connectée permettra au MSSP de demander et de mettre en service des accès.</span><span class="sxs-lookup"><span data-stu-id="3eeed-133">Adding the MSSP as a connected organization will allow the MSSP to request and have accesses provisioned.</span></span> 

    <span data-ttu-id="3eeed-134">Pour ce faire, dans le client AD client, accédez à Gouvernance des identités : Organisation connectée.</span><span class="sxs-lookup"><span data-stu-id="3eeed-134">To do so, in the customer AD tenant, access Identity Governance: Connected organization.</span></span> <span data-ttu-id="3eeed-135">Ajoutez une nouvelle organisation et recherchez votre client d'analyste MSSP via un ID de client ou un domaine.</span><span class="sxs-lookup"><span data-stu-id="3eeed-135">Add a new organization and search for your MSSP Analyst tenant via Tenant ID or Domain.</span></span> <span data-ttu-id="3eeed-136">Nous vous suggérons de créer un client AD distinct pour vos analystes MSSP.</span><span class="sxs-lookup"><span data-stu-id="3eeed-136">We suggest creating a separate AD tenant for your MSSP Analysts.</span></span>

2. <span data-ttu-id="3eeed-137">**Créer un catalogue de ressources dans Customer AAD: Identity Governance**</span><span class="sxs-lookup"><span data-stu-id="3eeed-137">**Create a resource catalog in Customer AAD: Identity Governance**</span></span>

    <span data-ttu-id="3eeed-138">Les catalogues de ressources sont une collection logique de packages d'accès, créés dans le client Client AD.</span><span class="sxs-lookup"><span data-stu-id="3eeed-138">Resource catalogs are a logical collection of access packages, created in the customer AD tenant.</span></span>

    <span data-ttu-id="3eeed-139">Pour ce faire, dans le client AD client, accédez à La gouvernance des identités : catalogues et ajoutez **nouveau catalogue**.</span><span class="sxs-lookup"><span data-stu-id="3eeed-139">To do so, in the customer AD tenant,  access Identity Governance: Catalogs, and add **New Catalog**.</span></span> <span data-ttu-id="3eeed-140">Dans notre exemple, nous l'appeller **MSSP Accesses**.</span><span class="sxs-lookup"><span data-stu-id="3eeed-140">In our example, we will call it **MSSP Accesses**.</span></span> 

    ![Image du nouveau catalogue](../../media/goverance-catalog.png)

    <span data-ttu-id="3eeed-142">Pour plus d'informations, voir [Créer un catalogue de ressources.](/azure/active-directory/governance/entitlement-management-catalog-create)</span><span class="sxs-lookup"><span data-stu-id="3eeed-142">Further more information, see [Create a catalog of resources](/azure/active-directory/governance/entitlement-management-catalog-create).</span></span>


3. <span data-ttu-id="3eeed-143">**Créer des packages d'accès pour les ressources MSSP Client AAD : Gouvernance des identités**</span><span class="sxs-lookup"><span data-stu-id="3eeed-143">**Create access packages for MSSP resources Customer AAD: Identity Governance**</span></span>

    <span data-ttu-id="3eeed-144">Les packages d'accès sont la collection de droits et d'accès accordés à un demandeur lors de l'approbation.</span><span class="sxs-lookup"><span data-stu-id="3eeed-144">Access packages are the collection of rights and accesses that a requestor will be granted upon approval.</span></span> 

    <span data-ttu-id="3eeed-145">Pour ce faire, dans le client AD client, accédez à Gouvernance des identités : packages d'accès et ajoutez **un nouveau package d'accès.**</span><span class="sxs-lookup"><span data-stu-id="3eeed-145">To do so, in the customer AD tenant, access Identity Governance: Access Packages, and add **New Access Package**.</span></span> <span data-ttu-id="3eeed-146">Créez un package d'accès pour les approuveurs MSSP et chaque niveau d'analyste.</span><span class="sxs-lookup"><span data-stu-id="3eeed-146">Create an access package for the MSSP approvers and each analyst tier.</span></span> <span data-ttu-id="3eeed-147">Par exemple, la configuration suivante de l'analyste de niveau 1 crée un package d'accès qui :</span><span class="sxs-lookup"><span data-stu-id="3eeed-147">For example, the following Tier 1 Analyst configuration creates an access package that:</span></span>

    - <span data-ttu-id="3eeed-148">Nécessite un membre du groupe AD **MSSP Analyst Approvers** pour autoriser les nouvelles demandes</span><span class="sxs-lookup"><span data-stu-id="3eeed-148">Requires a member of the AD group **MSSP Analyst Approvers** to authorize new requests</span></span>
    - <span data-ttu-id="3eeed-149">Possède des révisions d'accès annuel, où les analystes SOC peuvent demander une extension d'accès</span><span class="sxs-lookup"><span data-stu-id="3eeed-149">Has annual access reviews, where the SOC analysts can request an access extension</span></span>
    - <span data-ttu-id="3eeed-150">Peut uniquement être demandé par les utilisateurs du client SOC MSSP</span><span class="sxs-lookup"><span data-stu-id="3eeed-150">Can only be requested by users in the MSSP SOC Tenant</span></span>
    - <span data-ttu-id="3eeed-151">L'accès automatique expire après 365 jours</span><span class="sxs-lookup"><span data-stu-id="3eeed-151">Access auto expires after 365 days</span></span>

    ![Image du nouveau package d'accès](../../media/new-access-package.png)

    <span data-ttu-id="3eeed-153">Pour plus d'informations, [voir Créer un package d'accès.](/azure/active-directory/governance/entitlement-management-access-package-create)</span><span class="sxs-lookup"><span data-stu-id="3eeed-153">For more information, see [Create a new access package](/azure/active-directory/governance/entitlement-management-access-package-create).</span></span>


4. <span data-ttu-id="3eeed-154">**Fournir un lien de demande d'accès aux ressources MSSP à partir de Customer AAD: Identity Governance**</span><span class="sxs-lookup"><span data-stu-id="3eeed-154">**Provide access request link to MSSP resources from Customer AAD: Identity Governance**</span></span>

    <span data-ttu-id="3eeed-155">Le lien du portail Mon accès est utilisé par les analystes SOC MSSP pour demander l'accès via les packages d'accès créés.</span><span class="sxs-lookup"><span data-stu-id="3eeed-155">The My Access portal link is used by MSSP SOC analysts to request access via the access packages created.</span></span> <span data-ttu-id="3eeed-156">Le lien est durable, ce qui signifie qu'il peut être utilisé au fil du temps pour de nouveaux analystes.</span><span class="sxs-lookup"><span data-stu-id="3eeed-156">The link is durable, meaning the same link may be used over time for new analysts.</span></span> <span data-ttu-id="3eeed-157">La demande d'analyste est entrée dans une file d'attente pour approbation par les approuveurs d'analyste **MSSP.**</span><span class="sxs-lookup"><span data-stu-id="3eeed-157">The analyst request goes into a queue for approval by the **MSSP Analyst Approvers**.</span></span>


    ![Image des propriétés d'accès](../../media/access-properties.png)

    <span data-ttu-id="3eeed-159">Le lien se trouve sur la page de vue d'ensemble de chaque package d'accès.</span><span class="sxs-lookup"><span data-stu-id="3eeed-159">The link is located on the overview page of each access package.</span></span>

## <a name="manage-access"></a><span data-ttu-id="3eeed-160">Gérer l’accès</span><span class="sxs-lookup"><span data-stu-id="3eeed-160">Manage access</span></span> 

1. <span data-ttu-id="3eeed-161">Examiner et autoriser les demandes d'accès dans Customer et/ou MSSP myaccess.</span><span class="sxs-lookup"><span data-stu-id="3eeed-161">Review and authorize access requests in Customer and/or MSSP myaccess.</span></span>

    <span data-ttu-id="3eeed-162">Les demandes d'accès sont gérées dans le client Mon accès, par les membres du groupe d'approbations d'analyste MSSP.</span><span class="sxs-lookup"><span data-stu-id="3eeed-162">Access requests are managed in the customer My Access, by members of the MSSP Analyst Approvers group.</span></span>

    <span data-ttu-id="3eeed-163">Pour ce faire, accédez à la myaccess du client à l'aide de :  `https://myaccess.microsoft.com/@<Customer Domain >` .</span><span class="sxs-lookup"><span data-stu-id="3eeed-163">To do so, access the customer's myaccess using:  `https://myaccess.microsoft.com/@<Customer Domain >`.</span></span> 

    <span data-ttu-id="3eeed-164">Exemple :  `https://myaccess.microsoft.com/@M365x440XXX.onmicrosoft.com#/`</span><span class="sxs-lookup"><span data-stu-id="3eeed-164">Example:  `https://myaccess.microsoft.com/@M365x440XXX.onmicrosoft.com#/`</span></span>   
2. <span data-ttu-id="3eeed-165">Approuver ou refuser des demandes dans la section **Approbations** de l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3eeed-165">Approve or deny requests in the **Approvals** section of the UI.</span></span>

     <span data-ttu-id="3eeed-166">À ce stade, l'accès analyste a été mis en service et chaque analyste doit pouvoir accéder au Centre de sécurité Microsoft 365 du client :</span><span class="sxs-lookup"><span data-stu-id="3eeed-166">At this point, analyst access has been provisioned, and each analyst should be able to access the customer's Microsoft 365 Security Center:</span></span> 

    <span data-ttu-id="3eeed-167">`https://security.microsoft.com/?tid=<CustomerTenantId>` avec les autorisations et les rôles qui leur ont été attribués.</span><span class="sxs-lookup"><span data-stu-id="3eeed-167">`https://security.microsoft.com/?tid=<CustomerTenantId>` with the permissions and roles they were assigned.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3eeed-168">L'accès délégué à Microsoft Defender pour point de terminaison dans le Centre de sécurité Microsoft 365 permet actuellement d'accéder à un seul client par fenêtre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="3eeed-168">Delegated access to Microsoft Defender for Endpoint in the Microsoft 365 security center currently allows access to a single tenant per browser window.</span></span>