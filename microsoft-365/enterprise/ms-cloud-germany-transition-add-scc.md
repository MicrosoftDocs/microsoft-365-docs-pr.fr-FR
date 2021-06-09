---
title: Informations sur l’expérience eDiscovery lors de la migration à partir de Microsoft Cloud Deutschland
ms.author: andyber
author: andybergen
manager: laurawi
ms.date: 12/01/2020
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
description: 'Résumé : Étapes de migration eDiscovery pour la migration à partir de Microsoft Cloud Deutschland.'
ms.openlocfilehash: 0128c8563b2043e4ec41d2c5ab1b208bd3977511
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844249"
---
# <a name="information-about-the-ediscovery-experience-during-the-migration-from-microsoft-cloud-deutschland"></a><span data-ttu-id="0a62b-103">Informations sur l’expérience eDiscovery lors de la migration à partir de Microsoft Cloud Deutschland</span><span class="sxs-lookup"><span data-stu-id="0a62b-103">Information about the eDiscovery experience during the migration from Microsoft Cloud Deutschland</span></span>
<span data-ttu-id="0a62b-104">Les sections suivantes fournissent des informations supplémentaires sur l’expérience eDiscovery lors du passage de Microsoft Cloud Germany (Microsoft Cloud Deutschland) à des services Office 365 dans la nouvelle région de centres de données allemands.</span><span class="sxs-lookup"><span data-stu-id="0a62b-104">The following sections provide additional information about the eDiscovery experience when moving from Microsoft Cloud Germany (Microsoft Cloud Deutschland) to Office 365 services in the new German datacenter region.</span></span>

## <a name="ediscovery-administration-until-phase-4"></a><span data-ttu-id="0a62b-105">Administration eDiscovery jusqu’à la phase 4</span><span class="sxs-lookup"><span data-stu-id="0a62b-105">eDiscovery administration until phase 4</span></span>
<span data-ttu-id="0a62b-106">Jusqu’à la phase 4, le Centre de sécurité et conformité sera entièrement disponible.</span><span class="sxs-lookup"><span data-stu-id="0a62b-106">Until phase 4, the Security and Compliance Center will be fully available.</span></span> <span data-ttu-id="0a62b-107">Tout le contenu reste dans Microsoft Cloud Germany et est gérable par le Centre de sécurité et conformité Microsoft Cloud Germany ( https://protection.office.de/) .</span><span class="sxs-lookup"><span data-stu-id="0a62b-107">All content still remains in the Microsoft Cloud Germany and is manageable by the Microsoft Cloud Germany Security and Compliance Center (https://protection.office.de/).</span></span>

## <a name="ediscovery-experience-between-phase-4-until-the-the-end-of-phase-9"></a><span data-ttu-id="0a62b-108">Expérience eDiscovery entre la phase 4 et la fin de la phase 9</span><span class="sxs-lookup"><span data-stu-id="0a62b-108">eDiscovery experience between phase 4 until the the end of phase 9</span></span>
<span data-ttu-id="0a62b-109">Depuis le début de la phase 4 jusqu’à la fin de la phase 9, les recherches de découverte électronique échouent ou retournent 0 résultat pour les emplacements SharePoint Online, OneDrive Entreprise et Exchange Online qui ont été migrés.</span><span class="sxs-lookup"><span data-stu-id="0a62b-109">From the beginning of phase 4 until phase 9 is completed, eDiscovery searches will fail or return 0 results for SharePoint Online, OneDrive for Business, and Exchange Online locations that have been migrated.</span></span>

> [!NOTE]
> <span data-ttu-id="0a62b-110">Pendant la migration, les clients peuvent continuer à créer des cas, des obligations, des recherches et des exportations dans le Centre de sécurité [&](/microsoft-365/compliance/manage-legal-investigations)conformité, y compris la recherche [de contenu.](/microsoft-365/compliance/search-for-content)</span><span class="sxs-lookup"><span data-stu-id="0a62b-110">During migration, customers can continue to create cases, holds, searches, and exports in the [Security & Compliance Center](/microsoft-365/compliance/manage-legal-investigations), including [Content Search](/microsoft-365/compliance/search-for-content).</span></span> <span data-ttu-id="0a62b-111">Toutefois, les recherches sur les emplacements SharePoint Online, OneDrive Entreprise et Exchange Online qui ont été migrés retournent 0 résultat ou produisent une erreur.</span><span class="sxs-lookup"><span data-stu-id="0a62b-111">However, searches against SharePoint Online, OneDrive for Business, and Exchange Online locations that have been migrated will either return 0 results or produce an error.</span></span>

<span data-ttu-id="0a62b-112">Dans le cas où une recherche renvoie zéro résultat ou une erreur lors de la migration, veuillez effectuer l’action suivante pour SharePoint Online :</span><span class="sxs-lookup"><span data-stu-id="0a62b-112">In the event that a search returns zero results or an error during migration, please take the following action for SharePoint Online:</span></span>

- <span data-ttu-id="0a62b-113">Téléchargez les sites directement à partir du site SharePoint Online ou OneDrive Entreprise en suivant les instructions dans Télécharger des fichiers et des [dossiers](https://support.office.com/article/download-files-and-folders-from-onedrive-or-sharepoint-5c7397b7-19c7-4893-84fe-d02e8fa5df05)à partir de OneDrive ou SharePoint .</span><span class="sxs-lookup"><span data-stu-id="0a62b-113">Download sites directly from the SharePoint Online or OneDrive for Business site by following the instructions in [Download files and folders from OneDrive or SharePoint](https://support.office.com/article/download-files-and-folders-from-onedrive-or-sharepoint-5c7397b7-19c7-4893-84fe-d02e8fa5df05).</span></span> <span data-ttu-id="0a62b-114">Cette méthode nécessite des autorisations SharePoint’administrateur en ligne ou des autorisations en lecture seule sur le site.</span><span class="sxs-lookup"><span data-stu-id="0a62b-114">This method will require SharePoint Online administrator permissions or read-only permissions on the site.</span></span>
- <span data-ttu-id="0a62b-115">Si les limites sont dépassées, comme expliqué dans télécharger des fichiers et des dossiers à partir de OneDrive ou [de SharePoint,](https://support.office.com/article/download-files-and-folders-from-onedrive-or-sharepoint-5c7397b7-19c7-4893-84fe-d02e8fa5df05)les clients peuvent utiliser le client de synchronisation OneDrive Entreprise en suivant les instructions des SharePoint de synchronisation et des fichiers [Teams](https://support.office.com/article/sync-sharepoint-files-with-the-new-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88)avec votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0a62b-115">If limits are exceeded, as explained in [Download files and folders from OneDrive or SharePoint](https://support.office.com/article/download-files-and-folders-from-onedrive-or-sharepoint-5c7397b7-19c7-4893-84fe-d02e8fa5df05), customers can use the OneDrive for Business sync client by following the guidance in [Sync SharePoint and Teams files with your computer](https://support.office.com/article/sync-sharepoint-files-with-the-new-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88).</span></span>

- <span data-ttu-id="0a62b-116">Pour plus d’informations, [voir eDiscovery inaltérable dans Exchange Server](/Exchange/policy-and-compliance/ediscovery/ediscovery).</span><span class="sxs-lookup"><span data-stu-id="0a62b-116">For more information, see  [In-Place eDiscovery in Exchange Server](/Exchange/policy-and-compliance/ediscovery/ediscovery).</span></span>


## <a name="ediscovery-administration-after-phase-9"></a><span data-ttu-id="0a62b-117">Administration eDiscovery après la phase 9</span><span class="sxs-lookup"><span data-stu-id="0a62b-117">eDiscovery administration after phase 9</span></span>

<span data-ttu-id="0a62b-118">**S’applique à :** Tous les clients utilisant eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0a62b-118">**Applies to:** All customers using eDiscovery</span></span>

<span data-ttu-id="0a62b-119">À la phase 9, les dernières étapes de déplacement vers la nouvelle région de centres de données allemande seront effectuées.</span><span class="sxs-lookup"><span data-stu-id="0a62b-119">In phase 9, the final steps for moving to the new German datacenter region will be completed.</span></span> <span data-ttu-id="0a62b-120">Dans cette phase, tous les composants de service restants seront migrés.</span><span class="sxs-lookup"><span data-stu-id="0a62b-120">In this phase, all remaining service components will be migrated.</span></span>
<span data-ttu-id="0a62b-121">Après la phase 9, l’utilisation du Centre de sécurité et conformité dans Microsoft Cloud Germany (protection.office.de) n’est plus prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0a62b-121">After phase 9, using the Security and Compliance Center in Microsoft Cloud Germany (protection.office.de) is no longer supported.</span></span> <span data-ttu-id="0a62b-122">Utilisez plutôt le nouveau [Centre de sécurité](https://security.microsoft.com/) ou [centre](https://compliance.microsoft.com/) de conformité.</span><span class="sxs-lookup"><span data-stu-id="0a62b-122">Please use the new [Security Center](https://security.microsoft.com/) or [Compliance Center](https://compliance.microsoft.com/) instead.</span></span> <span data-ttu-id="0a62b-123">Toutes les données ont été migrées vers les nouveaux portails d’administration.</span><span class="sxs-lookup"><span data-stu-id="0a62b-123">All data have been migrated to the new admin portals.</span></span>

| <span data-ttu-id="0a62b-124">Étapes</span><span class="sxs-lookup"><span data-stu-id="0a62b-124">Step(s)</span></span> | <span data-ttu-id="0a62b-125">Description</span><span class="sxs-lookup"><span data-stu-id="0a62b-125">Description</span></span> | <span data-ttu-id="0a62b-126">Impact</span><span class="sxs-lookup"><span data-stu-id="0a62b-126">Impact</span></span> |
|:-------|:-------|:-------|
|  <span data-ttu-id="0a62b-127">Tous SharePoint en ligne, OneDrive Entreprise et Exchange Online ont été migrés avec le Centre de sécurité et conformité (SCC).</span><span class="sxs-lookup"><span data-stu-id="0a62b-127">All SharePoint Online, OneDrive for Business, and Exchange Online locations have been migrated along with the Security and Compliance Center (SCC).</span></span> | <span data-ttu-id="0a62b-128">Toute l’activité eDiscovery doit être exécuté à partir du client international.</span><span class="sxs-lookup"><span data-stu-id="0a62b-128">All eDiscovery activity should be run from the worldwide tenant.</span></span> <span data-ttu-id="0a62b-129">Les recherches seront désormais réussies à 100 %.</span><span class="sxs-lookup"><span data-stu-id="0a62b-129">Searches will now be 100% successful.</span></span> <span data-ttu-id="0a62b-130">Les défaillances ou erreurs doivent suivre les canaux de support normaux.</span><span class="sxs-lookup"><span data-stu-id="0a62b-130">Any failures or errors should follow normal support channels.</span></span> | <span data-ttu-id="0a62b-131">Aucun</span><span class="sxs-lookup"><span data-stu-id="0a62b-131">None</span></span> |
||||

### <a name="ediscovery-retention-policy"></a><span data-ttu-id="0a62b-132">Stratégie de rétention eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0a62b-132">eDiscovery Retention Policy</span></span>
<span data-ttu-id="0a62b-133">**S’applique à :**  Tous les clients qui ont appliqué une stratégie de rétention dans le cadre des étapes préalables à la migration</span><span class="sxs-lookup"><span data-stu-id="0a62b-133">**Applies to:**  All customers who applied a retention policy as part of the pre-migration steps</span></span>

| <span data-ttu-id="0a62b-134">Étapes</span><span class="sxs-lookup"><span data-stu-id="0a62b-134">Step(s)</span></span> | <span data-ttu-id="0a62b-135">Description</span><span class="sxs-lookup"><span data-stu-id="0a62b-135">Description</span></span> | <span data-ttu-id="0a62b-136">Impact</span><span class="sxs-lookup"><span data-stu-id="0a62b-136">Impact</span></span> |
|:-------|:-------|:-------|
| <span data-ttu-id="0a62b-137">Supprimer les stratégies de rétention à l’échelle de l’organisation qui ont été créées pendant les étapes préalables à la migration</span><span class="sxs-lookup"><span data-stu-id="0a62b-137">Remove organization-wide retention policies that were created during pre-migration steps</span></span> | <span data-ttu-id="0a62b-138">Les clients peuvent supprimer les stratégies de rétention à l’échelle de l’organisation qui ont été créées pendant le travail préalable à la migration des clients.</span><span class="sxs-lookup"><span data-stu-id="0a62b-138">Customers can remove the organization-wide retention policies that were created during the customers' pre-migration work.</span></span> | <span data-ttu-id="0a62b-139">Aucun</span><span class="sxs-lookup"><span data-stu-id="0a62b-139">None</span></span> |
||||
