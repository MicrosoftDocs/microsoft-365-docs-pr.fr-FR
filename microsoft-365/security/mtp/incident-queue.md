---
title: Hiérarchiser les incidents dans la Protection Microsoft contre les menaces
description: Découvrir comment hiérarchiser les incidents à partir de la file d’attente des incidents dans la Protection Microsoft contre les menaces
keywords: incident, file d’attente, vue d’ensemble, appareils, identités, utilisateurs, boîte aux lettres, e-mail, incidents
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
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
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: ef10eede38128bbf9b23537d860113b71f603089
ms.sourcegitcommit: 74bf600424d0cb7b9d16b4f391aeda7875058be1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42235123"
---
# <a name="prioritize-incidents-in-microsoft-threat-protection"></a><span data-ttu-id="91f2d-104">Hiérarchiser les incidents dans la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="91f2d-104">Prioritize incidents in Microsoft Threat Protection</span></span>

<span data-ttu-id="91f2d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="91f2d-105">**Applies to:**</span></span>
- <span data-ttu-id="91f2d-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="91f2d-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="91f2d-107">La Protection Microsoft contre les menaces applique l’analyse de la corrélation et regroupe toutes les alertes et analyses associées à différents produits en un seul incident.</span><span class="sxs-lookup"><span data-stu-id="91f2d-107">Microsoft Threat Protection applies correlation analytics and aggregates all related alerts and investigations from different products into one incident.</span></span> <span data-ttu-id="91f2d-108">La Protection Microsoft contre les menaces déclenche également des alertes uniques pour les activités qui peuvent uniquement être détectées comme malveillantes, en raison de la visibilité de bout en bout que la Protection Microsoft de la protection de menace a sur l’ensemble du patrimoine et de la suite de produits.</span><span class="sxs-lookup"><span data-stu-id="91f2d-108">Microsoft Threat Protection also triggers unique alerts on activities that can only be identified as malicious given the end-to-end visibility that Microsoft Threat Protection has across the entire estate and suite of products.</span></span> <span data-ttu-id="91f2d-109">En procédant ainsi, la Protection Microsoft contre les menaces donne une vue d’ensemble des attaques, ce qui permet à un analyste en charge des opérations de sécurité de comprendre et de gérer les menaces complexes au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="91f2d-109">By doing so, Microsoft Threat Protection narrates the broader attack story, allowing a security operations analyst to understand and deal with complex threats across the organization.</span></span>


<span data-ttu-id="91f2d-110">La **file d’attente des incidents** affiche un ensemble d’incidents qui ont été signalés par plusieurs appareils, utilisateurs et boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="91f2d-110">The **Incidents queue** shows a collection of incidents that were flagged from across devices, users, and mailboxes.</span></span> <span data-ttu-id="91f2d-111">Elle vous aide à trier les incidents afin de hiérarchiser et de créer une décision de réponse cyber-sécurité.</span><span class="sxs-lookup"><span data-stu-id="91f2d-111">It helps you sort through incidents to prioritize and create an informed cybersecurity response decision.</span></span>


![Image de la file d’attente des incidents](../../media/incidents-queue.png) 

<span data-ttu-id="91f2d-113">Par défaut, la file d’attente dans le Centre de sécurité Microsoft 365 affiche les incidents détectés au cours des 30 derniers jours, l’incident le plus récent apparaissant en tête de liste, qui vous permet d’accéder en avant-première aux incidents les plus récents.</span><span class="sxs-lookup"><span data-stu-id="91f2d-113">By default, the queue in the Microsoft 365 security center displays incidents seen in the last 30 days, with the most recent incident showing at the top of the list, helping you see the most recent incidents first.</span></span>

<span data-ttu-id="91f2d-114">La file d’attente des incidents présente les colonnes personnalisables qui vous permettent de tirer parti des différentes caractéristiques de l’incident ou des entités qu’il contient, ce qui vous permet de prendre une décision éclairée sur la hiérarchisation des incidents à traiter.</span><span class="sxs-lookup"><span data-stu-id="91f2d-114">The incident queue exposes customizable columns that give you visibility into different characteristics of the incident or the contained entities, helping you make an informed decision regarding prioritization of incidents to handle.</span></span> 

<span data-ttu-id="91f2d-115">La file d’attente des incidents présente également plusieurs options de filtrage, qui, lorsqu’elles sont appliquées, vous permettent de choisir d’effectuer un large éventail de tous les incidents existants dans votre environnement, ou de vous concentrer sur un scénario ou une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="91f2d-115">The incident queue also exposes multiple filtering options, that when applied, enable you to choose to perform a broad sweep of all existing incidents in your environment, or decide to focus on a specific scenario or threat.</span></span> <span data-ttu-id="91f2d-116">L’application de filtres dans la file d’attente des incidents permet de déterminer le type d’incident nécessitant une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="91f2d-116">Applying filters on the incident queue can help determine which incident requires immediate attention.</span></span> 

## <a name="available-filters"></a><span data-ttu-id="91f2d-117">Filtres disponibles</span><span class="sxs-lookup"><span data-stu-id="91f2d-117">Available filters</span></span>

### <a name="status"></a><span data-ttu-id="91f2d-118">Statut</span><span class="sxs-lookup"><span data-stu-id="91f2d-118">Status</span></span>
<span data-ttu-id="91f2d-119">Vous pouvez choisir de limiter la liste des incidents affichés en fonction de leur état pour identifier ceux qui sont actifs ou résolus.</span><span class="sxs-lookup"><span data-stu-id="91f2d-119">You can choose to limit the list of incidents shown based on their status to see which ones are active or resolved.</span></span>

### <a name="severity"></a><span data-ttu-id="91f2d-120">Gravité</span><span class="sxs-lookup"><span data-stu-id="91f2d-120">Severity</span></span>
<span data-ttu-id="91f2d-121">La gravité d'un incident est indicative de l'impact qu'il peut avoir sur vos actifs.</span><span class="sxs-lookup"><span data-stu-id="91f2d-121">The severity of an incident is indicative of the impact it can have in your assets.</span></span> <span data-ttu-id="91f2d-122">Plus la gravité est élevée, plus l’impact est important et nécessite une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="91f2d-122">The higher the severity the bigger the impact and typically requires the most immediate attention.</span></span> 

### <a name="assigned-to-owner"></a><span data-ttu-id="91f2d-123">Assignée à (propriétaire)</span><span class="sxs-lookup"><span data-stu-id="91f2d-123">Assigned to (owner)</span></span>
<span data-ttu-id="91f2d-124">Vous pouvez choisir de filtrer la liste en sélectionnant ceux qui vous sont affectés ou ceux qui vous sont affectés.</span><span class="sxs-lookup"><span data-stu-id="91f2d-124">You can choose to filter the list by selecting assigned to anyone or ones that are assigned to you.</span></span>

### <a name="multiple-alerts"></a><span data-ttu-id="91f2d-125">Plusieurs alertes</span><span class="sxs-lookup"><span data-stu-id="91f2d-125">Multiple alerts</span></span> 
<span data-ttu-id="91f2d-126">Filtre pour afficher uniquement les incidents contenant plusieurs alertes.</span><span class="sxs-lookup"><span data-stu-id="91f2d-126">Filter to see only incidents containing more than one alert.</span></span> <span data-ttu-id="91f2d-127">Il peut s’agir d’une indication d’une attaque plus complexe ou plus avancée dans la chaîne de terminaison.</span><span class="sxs-lookup"><span data-stu-id="91f2d-127">This could be an indication for an attack that is more complex or progressed in the kill chain.</span></span> 


### <a name="multiple-service-sources"></a><span data-ttu-id="91f2d-128">Plusieurs sources de service</span><span class="sxs-lookup"><span data-stu-id="91f2d-128">Multiple service sources</span></span> 
<span data-ttu-id="91f2d-129">Filtre pour afficher uniquement les incidents qui contiennent des alertes provenant de différentes sources (Microsoft Defender - Protection avancée contre les menaces, Microsoft Cloud App Security, Azure - Protection avancée contre les menaces, Office 365 - Protection avancée contre les menaces)</span><span class="sxs-lookup"><span data-stu-id="91f2d-129">Filter to only see incidents that contain alerts from different sources (Microsoft Defender ATP, Microsoft Cloud App Security, Azure ATP, Office 365 ATP)</span></span>
### <a name="service-sources"></a><span data-ttu-id="91f2d-130">Sources de service</span><span class="sxs-lookup"><span data-stu-id="91f2d-130">Service sources</span></span>
<span data-ttu-id="91f2d-131">En sélectionnant une source spécifique, vous pouvez vous concentrer sur les incidents qui contiennent au moins une alerte de la source choisie.</span><span class="sxs-lookup"><span data-stu-id="91f2d-131">By choosing a specific source, you can focus on incidents that contain at least one alert from that chosen source.</span></span> 

### <a name="multiple-categories"></a><span data-ttu-id="91f2d-132">Plusieurs catégories</span><span class="sxs-lookup"><span data-stu-id="91f2d-132">Multiple categories</span></span> 
<span data-ttu-id="91f2d-133">Vous pouvez choisir d’afficher uniquement les incidents qui ont été mappés à plusieurs catégories de la chaîne de terminaison et qui peuvent causer des dommages plus importants.</span><span class="sxs-lookup"><span data-stu-id="91f2d-133">You can choose to see only incidents that have mapped to multiple categories of the kill chain and can potentially cause more damage.</span></span> 

### <a name="categories"></a><span data-ttu-id="91f2d-134">Catégories</span><span class="sxs-lookup"><span data-stu-id="91f2d-134">Categories</span></span>
<span data-ttu-id="91f2d-135">Choisir des catégories spécifiques pour vous concentrer sur une étape spécifique de la chaîne de terminaison</span><span class="sxs-lookup"><span data-stu-id="91f2d-135">Choose specific categories to focus on a specific step in the kill chain</span></span>

### <a name="data-sensitivity"></a><span data-ttu-id="91f2d-136">Confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="91f2d-136">Data sensitivity</span></span>
<span data-ttu-id="91f2d-137">Certaines attaques se concentrent sur le ciblage de données sensibles ou précieuses.</span><span class="sxs-lookup"><span data-stu-id="91f2d-137">Some attacks focus on targeting to exfiltrate sensitive or valuable data.</span></span> <span data-ttu-id="91f2d-138">En appliquant un filtre pour déterminer si des données confidentielles sont impliquées dans l’incident, vous pouvez rapidement déterminer si des informations sensibles ont été compromises et hiérarchiser les problèmes.</span><span class="sxs-lookup"><span data-stu-id="91f2d-138">By applying a filter to see if sensitive data is involved in the incident, you can quickly determine if sensitive information has potentially been compromised and prioritize addressing those incidents.</span></span>

>[!NOTE]
><span data-ttu-id="91f2d-139">Applicable uniquement si la protection des informations Microsoft est activée.</span><span class="sxs-lookup"><span data-stu-id="91f2d-139">Only applicable if Microsoft Information Protection is turned on.</span></span>


## <a name="next-steps"></a><span data-ttu-id="91f2d-140">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="91f2d-140">Next steps</span></span>
<span data-ttu-id="91f2d-141">Après avoir déterminé quel incident a besoin de la priorité la plus élevée, vous pouvez effectuer d’autres tâches d’examen sur un incident.</span><span class="sxs-lookup"><span data-stu-id="91f2d-141">After you've determined which incident requires the highest priority, you can proceed to do further investigative work on an incident.</span></span>
- [<span data-ttu-id="91f2d-142">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="91f2d-142">Investigate incidents</span></span>](investigate-incidents.md)


## <a name="related-topics"></a><span data-ttu-id="91f2d-143">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="91f2d-143">Related topics</span></span>
- [<span data-ttu-id="91f2d-144">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="91f2d-144">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="91f2d-145">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="91f2d-145">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="91f2d-146">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="91f2d-146">Manage incidents</span></span>](manage-incidents.md)
