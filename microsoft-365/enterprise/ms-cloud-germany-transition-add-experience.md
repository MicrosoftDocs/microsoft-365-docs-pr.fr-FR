---
title: Activités post-migration pour la migration à partir de Microsoft Cloud Deutschland
ms.author: andyber
author: andybergen
manager: laurawi
ms.date: 12/11/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Ent_TLGs
description: 'Résumé : Activités post-migration après le passage de Microsoft Cloud Germany (Microsoft Cloud Deutschland) vers Office 365 services dans la nouvelle région de centres de données allemands.'
ms.openlocfilehash: 3659ce8ffa3424c3521c8f8954be88c7d53d0a51
ms.sourcegitcommit: 3d30ec03628870a22c54b6ec5d865cbe94f34245
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52930414"
---
# <a name="post-migration-activities-for-the-migration-from-microsoft-cloud-deutschland"></a><span data-ttu-id="b6f66-103">Activités post-migration pour la migration à partir de Microsoft Cloud Deutschland</span><span class="sxs-lookup"><span data-stu-id="b6f66-103">Post-migration activities for the migration from Microsoft Cloud Deutschland</span></span>

<span data-ttu-id="b6f66-104">Les sections suivantes fournissent des activités post-migration pour plusieurs services après le passage de Microsoft Cloud Germany (Microsoft Cloud Deutschland) vers Office 365 services dans la nouvelle région de centres de données allemands.</span><span class="sxs-lookup"><span data-stu-id="b6f66-104">The following sections provide post-migration activities for multiple services after moving from Microsoft Cloud Germany (Microsoft Cloud Deutschland) to Office 365 services in the new German datacenter region.</span></span>

## <a name="azure-ad"></a><span data-ttu-id="b6f66-105">Azure AD</span><span class="sxs-lookup"><span data-stu-id="b6f66-105">Azure AD</span></span>
<!-- This AAD Endpoints comparison table could be added to the documentation, not finally decided.
### Azure AD Endpoints
**Applies to:** All customers

After the cut over to Azure AD is complete, the organization is fully using Office 365 services and is no longer connected to Microsoft Cloud Deutschland and the endpoints cannot be used anymore. At this point, the customer needs to ensure that all applications are using the endpoints for the new German datacenter region.
The following table provides an overview about which endpoints will replace the previously used endpoints in Microsoft Cloud Germany (Microsoft Cloud Deutschland). 

|Endpoint in Microsoft Cloud Germany  |Endpoint in the new German datacenter region  |
|:---------|:---------|
|becws.microsoftonline.de<br>provisioningapi.microsoftonline.de |becws.microsoftonline.com<br>provisioningapi.microsoftonline.com |
|adminwebservice.microsoftonline.de |adminwebservice.microsoftonline.com |
|login.microsoftonline.de<br>logincert.microsoftonline.de<br>sts.microsoftonline.de |login.microsoftonline.com<br>login.windows.net<br>logincert.microsoftonline.com<br>accounts.accesscontrol.windows.net |
|enterpriseregistration.microsoftonline.de |enterpriseregistration.windows.net |
|graph.cloudapi.de |graph.windows.net |
|graph.microsoft.de |graph.microsoft.com |
|||
-->

### <a name="azure-ad-federated-authentication-with-ad-fs"></a><span data-ttu-id="b6f66-106">Authentification fédérée Azure AD avec AD FS</span><span class="sxs-lookup"><span data-stu-id="b6f66-106">Azure AD federated authentication with AD FS</span></span>
<span data-ttu-id="b6f66-107">**S’applique à :** Tous les clients utilisant l’authentification fédérée avec AD FS</span><span class="sxs-lookup"><span data-stu-id="b6f66-107">**Applies to:** All customers using federated authentication with AD FS</span></span>

| <span data-ttu-id="b6f66-108">Étapes</span><span class="sxs-lookup"><span data-stu-id="b6f66-108">Step(s)</span></span> | <span data-ttu-id="b6f66-109">Description</span><span class="sxs-lookup"><span data-stu-id="b6f66-109">Description</span></span> | <span data-ttu-id="b6f66-110">Impact</span><span class="sxs-lookup"><span data-stu-id="b6f66-110">Impact</span></span> |
|:-------|:-------|:-------|
| <span data-ttu-id="b6f66-111">Supprimez les confiances de partie de confiance de Microsoft Cloud Deutschland AD FS.</span><span class="sxs-lookup"><span data-stu-id="b6f66-111">Remove relying party trusts from Microsoft Cloud Deutschland AD FS.</span></span> | <span data-ttu-id="b6f66-112">Une fois le cut-over vers Azure AD terminé, l’organisation utilise entièrement les services Office 365 et n’est plus connectée à Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="b6f66-112">After the cut-over to Azure AD is complete, the organization is fully using Office 365 services and is no longer connected to Microsoft Cloud Deutschland.</span></span> <span data-ttu-id="b6f66-113">À ce stade, le client doit supprimer l’confiance de la partie de confiance vers les points de terminaison Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="b6f66-113">At this point, the customer needs to remove the relying party trust to the Microsoft Cloud Deutschland endpoints.</span></span> <span data-ttu-id="b6f66-114">Cette action ne peut être effectuée que lorsqu’aucune des applications du client ne pointe vers les points de terminaison Microsoft Cloud Deutschland lorsque Azure AD est mis à profit en tant que fournisseur d’identité (IdP).</span><span class="sxs-lookup"><span data-stu-id="b6f66-114">This can only be done when none of the customer's applications points to Microsoft Cloud Deutschland endpoints when Azure AD is leveraged as an Identity Provider (IdP).</span></span> | <span data-ttu-id="b6f66-115">Organisations d’authentification fédérée</span><span class="sxs-lookup"><span data-stu-id="b6f66-115">Federated Authentication organizations</span></span> | 
||||

<!--
    Question from ckinder
    The following paragraph is not clear
-->
### <a name="group-approvals"></a><span data-ttu-id="b6f66-116">Approbations de groupe</span><span class="sxs-lookup"><span data-stu-id="b6f66-116">Group approvals</span></span>
<span data-ttu-id="b6f66-117">**S’applique à :** Utilisateurs finaux dont les demandes d’approbation de groupe Azure AD n’ont pas été approuvées au cours des 30 derniers jours avant la migration</span><span class="sxs-lookup"><span data-stu-id="b6f66-117">**Applies to:** End-users whose Azure AD group approval requests weren't approved in the last 30 days before migration</span></span> 

| <span data-ttu-id="b6f66-118">Étapes</span><span class="sxs-lookup"><span data-stu-id="b6f66-118">Step(s)</span></span> | <span data-ttu-id="b6f66-119">Description</span><span class="sxs-lookup"><span data-stu-id="b6f66-119">Description</span></span> | <span data-ttu-id="b6f66-120">Impact</span><span class="sxs-lookup"><span data-stu-id="b6f66-120">Impact</span></span> |
|:-------|:-------|:-------|
| <span data-ttu-id="b6f66-121">Les demandes de joindre un groupe Azure AD au cours des 30 derniers jours avant la migration doivent être demandées à nouveau si la demande d’origine n’a pas été approuvée.</span><span class="sxs-lookup"><span data-stu-id="b6f66-121">Requests to join an Azure AD group in the last 30 days before migration will need to be requested again if the original request wasn't approved.</span></span> | <span data-ttu-id="b6f66-122">Les clients d’utilisateur final devront utiliser le panneau d’accès pour soumettre une demande de rejoindre à nouveau un groupe Azure AD si ces demandes n’ont pas été approuvées au cours des 30 derniers jours avant la migration.</span><span class="sxs-lookup"><span data-stu-id="b6f66-122">End-user customers will need to use the Access panel to submit a request to join an Azure AD group again if those requests weren't approved in the last 30 days before the migration.</span></span> |  <span data-ttu-id="b6f66-123">En tant qu’utilisateur final :</span><span class="sxs-lookup"><span data-stu-id="b6f66-123">As an end-user:</span></span> <ol><li><span data-ttu-id="b6f66-124">Accédez au [panneau d’accès.](https://account.activedirectory.windowsazure.com/r#/joinGroups)</span><span class="sxs-lookup"><span data-stu-id="b6f66-124">Navigate to [Access panel](https://account.activedirectory.windowsazure.com/r#/joinGroups).</span></span></li><li><span data-ttu-id="b6f66-125">Recherchez un groupe Azure AD pour lequel l’approbation de l’appartenance était en attente pendant les 30 jours avant la migration.</span><span class="sxs-lookup"><span data-stu-id="b6f66-125">Find an Azure AD group for which membership approval was pending during the 30 days before migration.</span></span></li><li><span data-ttu-id="b6f66-126">Demandez à rejoindre à nouveau le groupe Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b6f66-126">Request to join the Azure AD group again.</span></span></li></ol> <span data-ttu-id="b6f66-127">Les demandes de participation à un groupe actif moins de 30 jours avant la migration ne peuvent pas être approuvées, sauf si elles sont demandées à nouveau après la migration.</span><span class="sxs-lookup"><span data-stu-id="b6f66-127">Requests to join a group that are active less than 30 days before migration cannot be approved, unless they're requested again after migration.</span></span> |
||||

## <a name="custom-dns-updates"></a><span data-ttu-id="b6f66-128">Mises à jour DNS personnalisées</span><span class="sxs-lookup"><span data-stu-id="b6f66-128">Custom DNS updates</span></span>
<span data-ttu-id="b6f66-129">**S’applique à :**  Tous les clients gérant leurs propres zones DNS</span><span class="sxs-lookup"><span data-stu-id="b6f66-129">**Applies to:**  All customer managing their own DNS zones</span></span>

| <span data-ttu-id="b6f66-130">Étapes</span><span class="sxs-lookup"><span data-stu-id="b6f66-130">Step(s)</span></span> | <span data-ttu-id="b6f66-131">Description</span><span class="sxs-lookup"><span data-stu-id="b6f66-131">Description</span></span> | <span data-ttu-id="b6f66-132">Impact</span><span class="sxs-lookup"><span data-stu-id="b6f66-132">Impact</span></span> |
|:------|:-------|:-------|
| <span data-ttu-id="b6f66-133">Mettez à jour les services DNS locaux pour les points Office 365 services locaux.</span><span class="sxs-lookup"><span data-stu-id="b6f66-133">Update on-premises DNS services for Office 365 services endpoints.</span></span> | <span data-ttu-id="b6f66-134">Les entrées DNS gérées par le client qui pointent vers Microsoft Cloud Deutschland doivent être mises à jour pour pointer vers les points de terminaison Office 365 services globaux.</span><span class="sxs-lookup"><span data-stu-id="b6f66-134">Customer-managed DNS entries that point to Microsoft Cloud Deutschland need to be updated to point to the Office 365 Global services endpoints.</span></span> <span data-ttu-id="b6f66-135">Reportez-vous aux domaines dans [le centre d Microsoft 365'administration](https://admin.microsoft.com/Adminportal/Home#/Domains) et appliquez les modifications dans votre configuration DNS.</span><span class="sxs-lookup"><span data-stu-id="b6f66-135">Please refer to [Domains in the Microsoft 365 admin center](https://admin.microsoft.com/Adminportal/Home#/Domains) and apply the changes in your DNS configuration.</span></span> | <span data-ttu-id="b6f66-136">Si vous ne le faites pas, le service ou les clients logiciels risquent d’échouer.</span><span class="sxs-lookup"><span data-stu-id="b6f66-136">Failure to do so may result in failure of the service or of software clients.</span></span> |
||||

## <a name="third-party-services"></a><span data-ttu-id="b6f66-137">Services tiers</span><span class="sxs-lookup"><span data-stu-id="b6f66-137">Third-party services</span></span>
<span data-ttu-id="b6f66-138">**S’applique à :** Clients utilisant des services tiers pour les points de terminaison Office 365 services</span><span class="sxs-lookup"><span data-stu-id="b6f66-138">**Applies to:** Customers using third-party services for Office 365 services endpoints</span></span>

| <span data-ttu-id="b6f66-139">Étapes</span><span class="sxs-lookup"><span data-stu-id="b6f66-139">Step(s)</span></span> | <span data-ttu-id="b6f66-140">Description</span><span class="sxs-lookup"><span data-stu-id="b6f66-140">Description</span></span> | <span data-ttu-id="b6f66-141">Impact</span><span class="sxs-lookup"><span data-stu-id="b6f66-141">Impact</span></span> |
|:-------|:-------|:-------|
| <span data-ttu-id="b6f66-142">Mettez à jour les partenaires et les services tiers pour les points Office 365 services.</span><span class="sxs-lookup"><span data-stu-id="b6f66-142">Update partners and third-party services for Office 365 services endpoints.</span></span> | <ul><li><span data-ttu-id="b6f66-143">Les services tiers et les partenaires qui pointent vers Office 365 Germany doivent être mis à jour pour pointer vers les points de terminaison Office 365 services.</span><span class="sxs-lookup"><span data-stu-id="b6f66-143">Third-party services and partners that point to Office 365 Germany need to be updated to point to the Office 365 services endpoints.</span></span> <span data-ttu-id="b6f66-144">Exemple : ré-inscrire, en alignement avec vos fournisseurs et partenaires, la version d’application de la galerie d’applications, si disponible.</span><span class="sxs-lookup"><span data-stu-id="b6f66-144">Example: Re-register, in alignment with your vendors and partners, the gallery app version of applications, if available.</span></span> </li><li><span data-ttu-id="b6f66-145">Pointez toutes les applications personnalisées qui utilisent Graph API à `graph.microsoft.de` partir de `graph.microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="b6f66-145">Point all custom applications that leverage Graph API from `graph.microsoft.de` to `graph.microsoft.com`.</span></span> <span data-ttu-id="b6f66-146">Les autres API avec des points de terminaison modifiés doivent également être mises à jour, si elles sont mises à profit.</span><span class="sxs-lookup"><span data-stu-id="b6f66-146">Other APIs with changed endpoints also need to be updated, if leveraged.</span></span> </li><li><span data-ttu-id="b6f66-147">Modifiez toutes les applications d’entreprise tierces pour les rediriger vers les points de terminaison internationaux.</span><span class="sxs-lookup"><span data-stu-id="b6f66-147">Change all non-first-party enterprise applications to redirect to the worldwide endpoints.</span></span> </li></ul>| <span data-ttu-id="b6f66-148">Action requise.</span><span class="sxs-lookup"><span data-stu-id="b6f66-148">Required action.</span></span> <span data-ttu-id="b6f66-149">Si vous ne le faites pas, le service ou les clients logiciels risquent d’échouer.</span><span class="sxs-lookup"><span data-stu-id="b6f66-149">Failure to do so may result in failure of the service or of software clients.</span></span> |
||||