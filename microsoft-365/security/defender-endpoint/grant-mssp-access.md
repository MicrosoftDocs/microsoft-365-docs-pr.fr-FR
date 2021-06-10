---
title: Accorder l’accès au fournisseur de services de sécurité géré (MSSP)
description: Prendre les mesures nécessaires pour configurer l’intégration MSSP avec Microsoft Defender for Endpoint
keywords: fournisseur de services de sécurité géré, mssp, configurer, intégration
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 311903cdd1409f4ab997641cc842ff199ce2500d
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843105"
---
# <a name="grant-managed-security-service-provider-mssp-access-preview"></a><span data-ttu-id="edb1b-104">Accorder un accès au fournisseur de services de sécurité gérés (MSSP) (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="edb1b-104">Grant managed security service provider (MSSP) access (preview)</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="edb1b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="edb1b-105">**Applies to:**</span></span>
- [<span data-ttu-id="edb1b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="edb1b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="edb1b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="edb1b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="edb1b-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="edb1b-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="edb1b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="edb1b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-mssp-support-abovefoldlink)

>[!IMPORTANT] 
><span data-ttu-id="edb1b-110">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="edb1b-110">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="edb1b-111">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="edb1b-111">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="edb1b-112">Pour implémenter une solution d’accès délégué multi-locataire, prenez les mesures suivantes :</span><span class="sxs-lookup"><span data-stu-id="edb1b-112">To implement a multi-tenant delegated access solution, take the following steps:</span></span>

1. <span data-ttu-id="edb1b-113">Activez [le contrôle d’accès basé sur](rbac.md) les rôles dans Defender pour le point de terminaison et connectez-vous à des groupes Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="edb1b-113">Enable [role-based access control](rbac.md) in Defender for Endpoint and connect with Active Directory (AD) groups.</span></span>

2. <span data-ttu-id="edb1b-114">Configurer des [packages d’accès de gouvernance pour](/azure/active-directory/governance/identity-governance-overview) la demande d’accès et la mise en service.</span><span class="sxs-lookup"><span data-stu-id="edb1b-114">Configure [Governance Access Packages](/azure/active-directory/governance/identity-governance-overview) for access request and provisioning.</span></span>

3. <span data-ttu-id="edb1b-115">Gérer les demandes d’accès et les audits [dans Microsoft Myaccess](/azure/active-directory/governance/entitlement-management-request-approve).</span><span class="sxs-lookup"><span data-stu-id="edb1b-115">Manage access requests and audits in [Microsoft Myaccess](/azure/active-directory/governance/entitlement-management-request-approve).</span></span>

## <a name="enable-role-based-access-controls-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="edb1b-116">Activer les contrôles d’accès basés sur les rôles dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="edb1b-116">Enable role-based access controls in Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="edb1b-117">**Créer des groupes d’accès pour les ressources MSSP dans Customer AAD : Groupes**</span><span class="sxs-lookup"><span data-stu-id="edb1b-117">**Create access groups for MSSP resources in Customer AAD: Groups**</span></span>

    <span data-ttu-id="edb1b-118">Ces groupes seront liés aux rôles que vous créez dans Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="edb1b-118">These groups will be linked to the Roles you create in Defender for Endpoint.</span></span> <span data-ttu-id="edb1b-119">Pour ce faire, dans le client AD client, créez trois groupes.</span><span class="sxs-lookup"><span data-stu-id="edb1b-119">To do so, in the customer AD tenant, create three groups.</span></span> <span data-ttu-id="edb1b-120">Dans notre exemple d’approche, nous créons les groupes suivants :</span><span class="sxs-lookup"><span data-stu-id="edb1b-120">In our example approach, we create the following groups:</span></span>

    - <span data-ttu-id="edb1b-121">Analyste de niveau 1</span><span class="sxs-lookup"><span data-stu-id="edb1b-121">Tier 1 Analyst</span></span> 
    - <span data-ttu-id="edb1b-122">Analyste de niveau 2</span><span class="sxs-lookup"><span data-stu-id="edb1b-122">Tier 2 Analyst</span></span> 
    - <span data-ttu-id="edb1b-123">Approuveurs d’analyste MSSP</span><span class="sxs-lookup"><span data-stu-id="edb1b-123">MSSP Analyst Approvers</span></span>  


2. <span data-ttu-id="edb1b-124">Créez des rôles Defender pour les points de terminaison pour les niveaux d’accès appropriés dans Customer Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="edb1b-124">Create Defender for Endpoint roles for appropriate access levels in Customer Defender for Endpoint.</span></span>

    <span data-ttu-id="edb1b-125">Pour activer RBAC dans l’Centre de sécurité Microsoft Defender client, accédez aux **autorisations Paramètres > > Rôles** et « Activer les rôles », à partir d’un compte d’utilisateur ayant des droits d’administrateur général ou d’administrateur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="edb1b-125">To enable RBAC in the customer Microsoft Defender Security Center, access **Settings > Permissions > Roles** and "Turn on roles", from a user account with Global Administrator or Security Administrator rights.</span></span>

    ![Image de l’accès MSSP](images/mssp-access.png)

    <span data-ttu-id="edb1b-127">Ensuite, créez des rôles RBAC pour répondre aux besoins du niveau SOC MSSP.</span><span class="sxs-lookup"><span data-stu-id="edb1b-127">Then, create RBAC roles to meet MSSP SOC Tier needs.</span></span> <span data-ttu-id="edb1b-128">Lier ces rôles aux groupes d’utilisateurs créés via « Groupes d’utilisateurs affectés ».</span><span class="sxs-lookup"><span data-stu-id="edb1b-128">Link these roles to the created user groups via "Assigned user groups".</span></span>

    <span data-ttu-id="edb1b-129">Deux rôles possibles :</span><span class="sxs-lookup"><span data-stu-id="edb1b-129">Two possible roles:</span></span>

    - <span data-ttu-id="edb1b-130">**Analystes de niveau 1**</span><span class="sxs-lookup"><span data-stu-id="edb1b-130">**Tier 1 Analysts**</span></span> <br>
      <span data-ttu-id="edb1b-131">Effectuez toutes les actions à l’exception de la réponse en direct et gérez les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="edb1b-131">Perform all actions except for live response and manage security settings.</span></span>

    - <span data-ttu-id="edb1b-132">**Analystes de niveau 2**</span><span class="sxs-lookup"><span data-stu-id="edb1b-132">**Tier 2 Analysts**</span></span> <br>
      <span data-ttu-id="edb1b-133">Fonctionnalités de niveau 1 avec ajout à la [réponse en direct](live-response.md)</span><span class="sxs-lookup"><span data-stu-id="edb1b-133">Tier 1 capabilities with the addition to [live response](live-response.md)</span></span>

    <span data-ttu-id="edb1b-134">Pour plus d’informations, voir [Utiliser le contrôle d’accès basé sur un rôle.](rbac.md)</span><span class="sxs-lookup"><span data-stu-id="edb1b-134">For more information, see [Use role-based access control](rbac.md).</span></span>



## <a name="configure-governance-access-packages"></a><span data-ttu-id="edb1b-135">Configurer les packages d’accès de gouvernance</span><span class="sxs-lookup"><span data-stu-id="edb1b-135">Configure Governance Access Packages</span></span>

1.  <span data-ttu-id="edb1b-136">**Ajouter MSSP en tant qu’organisation connectée dans Customer AAD : Gouvernance des identités**</span><span class="sxs-lookup"><span data-stu-id="edb1b-136">**Add MSSP as Connected Organization in Customer AAD: Identity Governance**</span></span>
    
    <span data-ttu-id="edb1b-137">L’ajout du MSSP en tant qu’organisation connectée permettra au MSSP de demander et de mettre en service des accès.</span><span class="sxs-lookup"><span data-stu-id="edb1b-137">Adding the MSSP as a connected organization will allow the MSSP to request and have accesses provisioned.</span></span> 

    <span data-ttu-id="edb1b-138">Pour ce faire, dans le client AD client, accédez à Gouvernance des identités : Organisation connectée.</span><span class="sxs-lookup"><span data-stu-id="edb1b-138">To do so, in the customer AD tenant, access Identity Governance: Connected organization.</span></span> <span data-ttu-id="edb1b-139">Ajoutez une nouvelle organisation et recherchez votre client d’analyste MSSP via un ID de client ou un domaine.</span><span class="sxs-lookup"><span data-stu-id="edb1b-139">Add a new organization and search for your MSSP Analyst tenant via Tenant ID or Domain.</span></span> <span data-ttu-id="edb1b-140">Nous vous suggérons de créer un client AD distinct pour vos analystes MSSP.</span><span class="sxs-lookup"><span data-stu-id="edb1b-140">We suggest creating a separate AD tenant for your MSSP Analysts.</span></span>

2. <span data-ttu-id="edb1b-141">**Créer un catalogue de ressources dans Customer AAD: Identity Governance**</span><span class="sxs-lookup"><span data-stu-id="edb1b-141">**Create a resource catalog in Customer AAD: Identity Governance**</span></span>

    <span data-ttu-id="edb1b-142">Les catalogues de ressources sont une collection logique de packages d’accès, créés dans le client Client AD.</span><span class="sxs-lookup"><span data-stu-id="edb1b-142">Resource catalogs are a logical collection of access packages, created in the customer AD tenant.</span></span>

    <span data-ttu-id="edb1b-143">Pour ce faire, dans le client AD client, accédez à Gouvernance des identités : catalogues et ajoutez **nouveau catalogue**.</span><span class="sxs-lookup"><span data-stu-id="edb1b-143">To do so, in the customer AD tenant,  access Identity Governance: Catalogs, and add **New Catalog**.</span></span> <span data-ttu-id="edb1b-144">Dans notre exemple, nous l’appeller **MSSP Accesses**.</span><span class="sxs-lookup"><span data-stu-id="edb1b-144">In our example, we will call it **MSSP Accesses**.</span></span> 

    ![Image du nouveau catalogue](images/goverance-catalog.png)

    <span data-ttu-id="edb1b-146">Pour plus d’informations, voir [Créer un catalogue de ressources.](/azure/active-directory/governance/entitlement-management-catalog-create)</span><span class="sxs-lookup"><span data-stu-id="edb1b-146">Further more information, see [Create a catalog of resources](/azure/active-directory/governance/entitlement-management-catalog-create).</span></span>


3. <span data-ttu-id="edb1b-147">**Créer des packages d’accès pour les ressources MSSP Client AAD : Gouvernance des identités**</span><span class="sxs-lookup"><span data-stu-id="edb1b-147">**Create access packages for MSSP resources Customer AAD: Identity Governance**</span></span>

    <span data-ttu-id="edb1b-148">Les packages d’accès sont la collection de droits et d’accès accordés à un demandeur lors de l’approbation.</span><span class="sxs-lookup"><span data-stu-id="edb1b-148">Access packages are the collection of rights and accesses that a requestor will be granted upon approval.</span></span> 

    <span data-ttu-id="edb1b-149">Pour ce faire, dans le client AD client, accédez à Gouvernance des identités : packages d’accès et ajoutez **un nouveau package d’accès.**</span><span class="sxs-lookup"><span data-stu-id="edb1b-149">To do so, in the customer AD tenant, access Identity Governance: Access Packages, and add **New Access Package**.</span></span> <span data-ttu-id="edb1b-150">Créez un package d’accès pour les approuveurs MSSP et chaque niveau d’analyste.</span><span class="sxs-lookup"><span data-stu-id="edb1b-150">Create an access package for the MSSP approvers and each analyst tier.</span></span> <span data-ttu-id="edb1b-151">Par exemple, la configuration suivante de l’analyste de niveau 1 crée un package d’accès qui :</span><span class="sxs-lookup"><span data-stu-id="edb1b-151">For example, the following Tier 1 Analyst configuration creates an access package that:</span></span>

    - <span data-ttu-id="edb1b-152">Nécessite un membre du groupe AD **MSSP Analyst Approvers** pour autoriser les nouvelles demandes</span><span class="sxs-lookup"><span data-stu-id="edb1b-152">Requires a member of the AD group **MSSP Analyst Approvers** to authorize new requests</span></span>
    - <span data-ttu-id="edb1b-153">Possède des révisions d’accès annuel, où les analystes SOC peuvent demander une extension d’accès</span><span class="sxs-lookup"><span data-stu-id="edb1b-153">Has annual access reviews, where the SOC analysts can request an access extension</span></span>
    - <span data-ttu-id="edb1b-154">Peut uniquement être demandé par les utilisateurs dans le client SOC MSSP</span><span class="sxs-lookup"><span data-stu-id="edb1b-154">Can only be requested by users in the MSSP SOC Tenant</span></span>
    - <span data-ttu-id="edb1b-155">L’accès automatique expire après 365 jours</span><span class="sxs-lookup"><span data-stu-id="edb1b-155">Access auto expires after 365 days</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="edb1b-156">![Image du nouveau package d’accès](images/new-access-package.png)</span><span class="sxs-lookup"><span data-stu-id="edb1b-156">![Image of new access package](images/new-access-package.png)</span></span>

    <span data-ttu-id="edb1b-157">Pour plus d’informations, [voir Créer un package d’accès.](/azure/active-directory/governance/entitlement-management-access-package-create)</span><span class="sxs-lookup"><span data-stu-id="edb1b-157">For more information, see [Create a new access package](/azure/active-directory/governance/entitlement-management-access-package-create).</span></span>


4. <span data-ttu-id="edb1b-158">**Fournir un lien de demande d’accès aux ressources MSSP à partir de Customer AAD: Identity Governance**</span><span class="sxs-lookup"><span data-stu-id="edb1b-158">**Provide access request link to MSSP resources from Customer AAD: Identity Governance**</span></span>

    <span data-ttu-id="edb1b-159">Le lien du portail Mon accès est utilisé par les analystes SOC MSSP pour demander l’accès via les packages d’accès créés.</span><span class="sxs-lookup"><span data-stu-id="edb1b-159">The My Access portal link is used by MSSP SOC analysts to request access via the access packages created.</span></span> <span data-ttu-id="edb1b-160">Le lien est durable, ce qui signifie qu’il peut être utilisé au fil du temps pour de nouveaux analystes.</span><span class="sxs-lookup"><span data-stu-id="edb1b-160">The link is durable, meaning the same link may be used over time for new analysts.</span></span> <span data-ttu-id="edb1b-161">La demande d’analyste est entrée dans une file d’attente pour approbation par les approuveurs d’analyste **MSSP.**</span><span class="sxs-lookup"><span data-stu-id="edb1b-161">The analyst request goes into a queue for approval by the **MSSP Analyst Approvers**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="edb1b-162">![Image des propriétés d’accès](images/access-properties.png)</span><span class="sxs-lookup"><span data-stu-id="edb1b-162">![Image of access properties](images/access-properties.png)</span></span>

    <span data-ttu-id="edb1b-163">Le lien se trouve sur la page de vue d’ensemble de chaque package d’accès.</span><span class="sxs-lookup"><span data-stu-id="edb1b-163">The link is located on the overview page of each access package.</span></span>

## <a name="manage-access"></a><span data-ttu-id="edb1b-164">Gérer l’accès</span><span class="sxs-lookup"><span data-stu-id="edb1b-164">Manage access</span></span> 

1. <span data-ttu-id="edb1b-165">Examiner et autoriser les demandes d’accès dans Customer et/ou MSSP myaccess.</span><span class="sxs-lookup"><span data-stu-id="edb1b-165">Review and authorize access requests in Customer and/or MSSP myaccess.</span></span>

    <span data-ttu-id="edb1b-166">Les demandes d’accès sont gérées dans le client Mon accès, par les membres du groupe d’approbations d’analyste MSSP.</span><span class="sxs-lookup"><span data-stu-id="edb1b-166">Access requests are managed in the customer My Access, by members of the MSSP Analyst Approvers group.</span></span>

    <span data-ttu-id="edb1b-167">Pour ce faire, accédez à la myaccess du client à l’aide de :  `https://myaccess.microsoft.com/@<Customer Domain >` .</span><span class="sxs-lookup"><span data-stu-id="edb1b-167">To do so, access the customer's myaccess using:  `https://myaccess.microsoft.com/@<Customer Domain >`.</span></span> 

    <span data-ttu-id="edb1b-168">Exemple :  `https://myaccess.microsoft.com/@M365x440XXX.onmicrosoft.com#/`</span><span class="sxs-lookup"><span data-stu-id="edb1b-168">Example:  `https://myaccess.microsoft.com/@M365x440XXX.onmicrosoft.com#/`</span></span>   
2. <span data-ttu-id="edb1b-169">Approuver ou refuser des demandes dans la section **Approbations** de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="edb1b-169">Approve or deny requests in the **Approvals** section of the UI.</span></span>

    <span data-ttu-id="edb1b-170">À ce stade, l’accès analyste a été mis en service et chaque analyste doit pouvoir accéder aux informations du client Centre de sécurité Microsoft Defender :`https://securitycenter.Microsoft.com/?tid=<CustomerTenantId>`</span><span class="sxs-lookup"><span data-stu-id="edb1b-170">At this point, analyst access has been provisioned, and each analyst should be able to access the customer's Microsoft Defender Security Center: `https://securitycenter.Microsoft.com/?tid=<CustomerTenantId>`</span></span>

## <a name="related-topics"></a><span data-ttu-id="edb1b-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edb1b-171">Related topics</span></span>
- [<span data-ttu-id="edb1b-172">Accéder au portail client MSSP</span><span class="sxs-lookup"><span data-stu-id="edb1b-172">Access the MSSP customer portal</span></span>](access-mssp-portal.md)
- [<span data-ttu-id="edb1b-173">Configurer des notifications d’alerte</span><span class="sxs-lookup"><span data-stu-id="edb1b-173">Configure alert notifications</span></span>](configure-mssp-notifications.md)
- [<span data-ttu-id="edb1b-174">Récupérer les alertes d’un client</span><span class="sxs-lookup"><span data-stu-id="edb1b-174">Fetch alerts from customer tenant</span></span>](fetch-alerts-mssp.md)



 

