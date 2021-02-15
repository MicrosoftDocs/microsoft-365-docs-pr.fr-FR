---
title: Hiérarchiser les incidents dans Microsoft 365 Defender
description: Découvrez comment filtrer les incidents à partir de la file d’attente des incidents dans Microsoft 365 Defender
keywords: incident, file d’attente, vue d’ensemble, appareils, identités, utilisateurs, boîte aux lettres, e-mail, incidents
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: e01fce970b806bc425db2cd4886e82f79434656f
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49929293"
---
# <a name="prioritize-incidents-in-microsoft-365-defender"></a><span data-ttu-id="6b4f3-104">Hiérarchiser les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6b4f3-104">Prioritize incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="6b4f3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-105">**Applies to:**</span></span>
- <span data-ttu-id="6b4f3-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6b4f3-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="6b4f3-107">Microsoft 365 Defender applique l’analyse de corrélation et regroupe toutes les alertes et enquêtes associées de différents produits en un seul incident.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-107">Microsoft 365 Defender applies correlation analytics and aggregates all related alerts and investigations from different products into one incident.</span></span> <span data-ttu-id="6b4f3-108">Microsoft 365 Defender déclenche également des alertes uniques sur les activités qui peuvent uniquement être identifiées comme malveillantes en raison de la visibilité de bout en bout de Microsoft 365 Defender sur l’ensemble du patrimoine et de la suite de produits.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-108">Microsoft 365 Defender also triggers unique alerts on activities that can only be identified as malicious given the end-to-end visibility that Microsoft 365 Defender has across the entire estate and suite of products.</span></span> <span data-ttu-id="6b4f3-109">Cette vue donne à votre analyste des opérations de sécurité un niveau d’attaque plus large, ce qui lui permet de mieux comprendre et de gérer les menaces complexes au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-109">This view gives your security operations analyst the broader attack story, which helps them better understand and deal with complex threats across the organization.</span></span>


<span data-ttu-id="6b4f3-110">La **file d’attente des incidents** affiche un ensemble d’incidents qui ont été signalés par plusieurs appareils, utilisateurs et boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-110">The **Incidents queue** shows a collection of incidents that were flagged from across devices, users, and mailboxes.</span></span> <span data-ttu-id="6b4f3-111">Elle vous aide à trier les incidents afin de hiérarchiser et de créer une décision de réponse cyber-sécurité.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-111">It helps you sort through incidents to prioritize and create an informed cybersecurity response decision.</span></span>


![Image de la file d’attente des incidents](../../media/incidents-queue.png) 

<span data-ttu-id="6b4f3-113">Par défaut, la file d’attente du Centre de sécurité Microsoft 365 affiche les incidents observés au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-113">By default, the queue in the Microsoft 365 security center displays incidents seen in the last 30 days.</span></span> <span data-ttu-id="6b4f3-114">L’incident le plus récent se trouve en haut de la liste pour que vous le voyez en premier.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-114">The most recent incident is at the top of the list so you can see it first.</span></span>

<span data-ttu-id="6b4f3-115">La file d’attente des incidents expose des colonnes personnalisables qui vous donnent une visibilité sur les différentes caractéristiques de l’incident ou des entités contenues.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-115">The incident queue exposes customizable columns that give you visibility into different characteristics of the incident or the contained entities.</span></span> <span data-ttu-id="6b4f3-116">Cela vous permet de prendre une décision éclairée concernant la hiér donc des incidents à gérer.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-116">This helps you make an informed decision regarding prioritization of incidents to handle.</span></span>

<span data-ttu-id="6b4f3-117">Pour une visibilité supplémentaire en un coup d’œil, l’appellation automatique des incidents génère des noms d’incident basés sur des attributs d’alerte tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-117">For additional visibility at a glance, automatic incident naming generates incident names based on alert attributes such as the number of endpoints affected, users affected, detection sources, or categories.</span></span> <span data-ttu-id="6b4f3-118">Cela vous permet de comprendre rapidement l’étendue de l’incident.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-118">This allows you to quickly understand the scope of the incident.</span></span>

<span data-ttu-id="6b4f3-119">Par exemple : *incident en plusieurs étapes sur plusieurs points de terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="6b4f3-119">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>

> [!NOTE]
> <span data-ttu-id="6b4f3-120">Les incidents qui existaient avant le déploiement de la dénomination automatique des incidents ne seront pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-120">Incidents that existed prior the rollout of automatic incident naming will not have their name changed.</span></span>

<span data-ttu-id="6b4f3-121">La file d’attente des incidents expose également plusieurs options de filtrage qui, lorsqu’elles sont appliquées, vous permettent d’effectuer un large éventail de tous les incidents existants dans votre environnement ou de décider de vous concentrer sur un scénario ou une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-121">The incident queue also exposes multiple filtering options, that when applied, enable you to perform a broad sweep of all existing incidents in your environment, or decide to focus on a specific scenario or threat.</span></span> <span data-ttu-id="6b4f3-122">L’application de filtres dans la file d’attente des incidents permet de déterminer le type d’incident nécessitant une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-122">Applying filters on the incident queue can help determine which incident requires immediate attention.</span></span> 

## <a name="available-filters"></a><span data-ttu-id="6b4f3-123">Filtres disponibles</span><span class="sxs-lookup"><span data-stu-id="6b4f3-123">Available filters</span></span>

### <a name="assigned-to"></a><span data-ttu-id="6b4f3-124">Affectée à</span><span class="sxs-lookup"><span data-stu-id="6b4f3-124">Assigned to</span></span>
<span data-ttu-id="6b4f3-125">Vous pouvez choisir d’afficher les alertes qui vous sont affectées ou celles gérées par l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-125">You can choose to show alerts that are assigned to you or those handled by automation.</span></span>

### <a name="categories"></a><span data-ttu-id="6b4f3-126">Catégories</span><span class="sxs-lookup"><span data-stu-id="6b4f3-126">Categories</span></span>
<span data-ttu-id="6b4f3-127">Choisissez des catégories pour vous concentrer sur des tactiques, des techniques ou des composants d’attaque spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-127">Choose categories to focus on specific tactics, techniques, or attack components seen.</span></span> 

### <a name="classification"></a><span data-ttu-id="6b4f3-128">Classification</span><span class="sxs-lookup"><span data-stu-id="6b4f3-128">Classification</span></span>
<span data-ttu-id="6b4f3-129">Filtrez les incidents en fonction des classifications définies des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-129">Filter incidents based on the set classifications of the related alerts.</span></span> <span data-ttu-id="6b4f3-130">Les valeurs incluent des alertes vraies, des alertes fausses ou non définies.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-130">The values include true alerts, false alerts, or not set.</span></span>

### <a name="data-sensitivity"></a><span data-ttu-id="6b4f3-131">Confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="6b4f3-131">Data sensitivity</span></span>
<span data-ttu-id="6b4f3-132">Certaines attaques se concentrent sur le ciblage de données sensibles ou précieuses.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-132">Some attacks focus on targeting to exfiltrate sensitive or valuable data.</span></span> <span data-ttu-id="6b4f3-133">En appliquant un filtre pour déterminer si des données confidentielles sont impliquées dans l’incident, vous pouvez rapidement déterminer si des informations sensibles ont été compromises et hiérarchiser les problèmes.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-133">By applying a filter to see if sensitive data is involved in the incident, you can quickly determine if sensitive information has potentially been compromised and prioritize addressing those incidents.</span></span>

>[!NOTE]
><span data-ttu-id="6b4f3-134">Applicable uniquement si la protection des informations Microsoft est activée.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-134">Only applicable if Microsoft Information Protection is turned on.</span></span>

### <a name="device-group"></a><span data-ttu-id="6b4f3-135">Groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="6b4f3-135">Device group</span></span>
<span data-ttu-id="6b4f3-136">Filtrer par groupes d’appareils définis.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-136">Filter by defined device groups.</span></span>

### <a name="investigation-state"></a><span data-ttu-id="6b4f3-137">État de l’examen</span><span class="sxs-lookup"><span data-stu-id="6b4f3-137">Investigation state</span></span>
<span data-ttu-id="6b4f3-138">Filtrer les incidents selon l’état de l’examen automatisé.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-138">Filter incidents by the status of automated investigation.</span></span> 

### <a name="multiple-categories"></a><span data-ttu-id="6b4f3-139">Plusieurs catégories</span><span class="sxs-lookup"><span data-stu-id="6b4f3-139">Multiple categories</span></span> 
<span data-ttu-id="6b4f3-140">Vous pouvez choisir de ne voir que les incidents qui ont été mappés à plusieurs catégories et qui peuvent donc potentiellement causer davantage de dommages.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-140">You can choose to see only incidents that have mapped to multiple categories  and can thus potentially cause more damage.</span></span> 

### <a name="multiple-service-sources"></a><span data-ttu-id="6b4f3-141">Plusieurs sources de service</span><span class="sxs-lookup"><span data-stu-id="6b4f3-141">Multiple service sources</span></span> 
<span data-ttu-id="6b4f3-142">Filtrez pour voir uniquement les incidents qui contiennent des alertes provenant de différentes sources (Microsoft Defender pour endpoint, Microsoft Cloud App Security, Microsoft Defender pour l’identité, Microsoft Defender pour Office 365).</span><span class="sxs-lookup"><span data-stu-id="6b4f3-142">Filter to only see incidents that contain alerts from different sources (Microsoft Defender for Endpoint, Microsoft Cloud App Security, Microsoft Defender for Identity, Microsoft Defender for Office 365).</span></span>

### <a name="os-platform"></a><span data-ttu-id="6b4f3-143">Plateforme du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6b4f3-143">OS platform</span></span>
<span data-ttu-id="6b4f3-144">Limitez l’affichage de la file d’attente des incidents par système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-144">Limit the incident queue view by operating system.</span></span>

### <a name="service-sources"></a><span data-ttu-id="6b4f3-145">Sources de service</span><span class="sxs-lookup"><span data-stu-id="6b4f3-145">Service sources</span></span>
<span data-ttu-id="6b4f3-146">En sélectionnant une source spécifique, vous pouvez vous concentrer sur les incidents qui contiennent au moins une alerte de la source choisie.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-146">By choosing a specific source, you can focus on incidents that contain at least one alert from that chosen source.</span></span> 

### <a name="severity"></a><span data-ttu-id="6b4f3-147">Severity</span><span class="sxs-lookup"><span data-stu-id="6b4f3-147">Severity</span></span>
<span data-ttu-id="6b4f3-148">La gravité d’un incident indique l’impact qu’il peut avoir sur vos ressources.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-148">The severity of an incident is indicative of the impact it can have on your assets.</span></span> <span data-ttu-id="6b4f3-149">Plus la gravité est élevée, plus l’impact est important et nécessite généralement l’attention la plus immédiate.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-149">The higher the severity, the bigger the impact and typically requires the most immediate attention.</span></span> 

### <a name="status"></a><span data-ttu-id="6b4f3-150">Statut</span><span class="sxs-lookup"><span data-stu-id="6b4f3-150">Status</span></span>
<span data-ttu-id="6b4f3-151">Vous pouvez choisir de limiter la liste des incidents affichés en fonction de leur état pour identifier ceux qui sont actifs ou résolus.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-151">You can choose to limit the list of incidents shown based on their status to see which ones are active or resolved.</span></span>




## <a name="next-steps"></a><span data-ttu-id="6b4f3-152">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="6b4f3-152">Next steps</span></span>
<span data-ttu-id="6b4f3-153">Après avoir déterminé quel incident a besoin de la priorité la plus élevée, vous pouvez effectuer d’autres tâches d’examen sur un incident.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-153">After you've determined which incident requires the highest priority, you can proceed to do further investigative work on an incident.</span></span>
- [<span data-ttu-id="6b4f3-154">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="6b4f3-154">Investigate incidents</span></span>](investigate-incidents.md)


## <a name="see-also"></a><span data-ttu-id="6b4f3-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b4f3-155">See also</span></span>
- [<span data-ttu-id="6b4f3-156">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="6b4f3-156">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="6b4f3-157">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="6b4f3-157">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="6b4f3-158">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="6b4f3-158">Manage incidents</span></span>](manage-incidents.md)
