---
title: Hiérarchiser les incidents dans Microsoft 365 Defender
description: Découvrez comment filtrer les incidents à partir de la file d’attente des incidents dans Microsoft 365 Defender
keywords: incident, file d’attente, vue d’ensemble, appareils, identités, utilisateurs, boîte aux lettres, courrier électronique, incidents, analyse, réponse
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
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
ms.openlocfilehash: a3b6edda36d2872177d9a88f3259220dcf2e76f3
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52291314"
---
# <a name="prioritize-incidents-in-microsoft-365-defender"></a><span data-ttu-id="50f19-104">Hiérarchiser les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="50f19-104">Prioritize incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="50f19-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="50f19-105">**Applies to:**</span></span>
- <span data-ttu-id="50f19-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="50f19-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="50f19-107">Microsoft 365 Defender applique l’analyse de corrélation et regroupe les alertes associées et les enquêtes automatisées de différents produits dans un incident.</span><span class="sxs-lookup"><span data-stu-id="50f19-107">Microsoft 365 Defender applies correlation analytics and aggregates related alerts and automated investigations from different products into an incident.</span></span> <span data-ttu-id="50f19-108">Microsoft 365 Defender déclenche également des alertes uniques sur les activités qui peuvent uniquement être identifiées comme malveillantes en raison de la visibilité de bout en bout dont Microsoft 365 Defender dispose dans toute la suite de produits.</span><span class="sxs-lookup"><span data-stu-id="50f19-108">Microsoft 365 Defender also triggers unique alerts on activities that can only be identified as malicious given the end-to-end visibility that Microsoft 365 Defender has across the entire suite of products.</span></span> <span data-ttu-id="50f19-109">Cette vue donne à vos analystes de sécurité un niveau d’attaque plus large, qui les aide à mieux comprendre et traiter les menaces complexes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="50f19-109">This view gives your security analysts the broader attack story, which help them better understand and deal with complex threats across your organization.</span></span>

<span data-ttu-id="50f19-110">La **file d’attente Incident** affiche un ensemble d’incidents qui ont été créés sur plusieurs appareils, utilisateurs et boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="50f19-110">The **Incident queue** shows a collection of incidents that were created across devices, users, and mailboxes.</span></span> <span data-ttu-id="50f19-111">Elle vous aide à trier les incidents afin de hiérarchiser et de créer une décision de réponse cyber-sécurité.</span><span class="sxs-lookup"><span data-stu-id="50f19-111">It helps you sort through incidents to prioritize and create an informed cybersecurity response decision.</span></span> 

<span data-ttu-id="50f19-112">Vous pouvez vous rendre dans la file d’attente des incidents à partir **d’incidents & alertes** > Incidents lors du lancement rapide du centre de sécurité Microsoft 365 ([security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="50f19-112">You get to the incident queue from **Incidents & alerts > Incidents** on the quick launch of the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)).</span></span> <span data-ttu-id="50f19-113">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="50f19-113">Here's an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents.png" alt-text="Exemple de file d’attente d’incident":::

<span data-ttu-id="50f19-115">La section **Incidents et alertes** les plus récents présente un graphique du nombre d’alertes reçues et d’incidents créés au cours des dernières 24 heures.</span><span class="sxs-lookup"><span data-stu-id="50f19-115">The **Most recent incidents and alerts** section shows a graph of the number of alerts received and incidents created in the last 24 hours.</span></span>

<span data-ttu-id="50f19-116">Par défaut, la file d’attente des incidents dans Microsoft 365 centre de sécurité affiche les incidents observés au cours des six derniers mois.</span><span class="sxs-lookup"><span data-stu-id="50f19-116">By default, the incident queue in the Microsoft 365 security center displays incidents seen in the last six months.</span></span> <span data-ttu-id="50f19-117">L’incident le plus récent se trouve en haut de la liste pour que vous le voyez en premier.</span><span class="sxs-lookup"><span data-stu-id="50f19-117">The most recent incident is at the top of the list so you can see it first.</span></span>

<span data-ttu-id="50f19-118">La file d’attente des incidents possède des colonnes personnalisables (sélectionnez Sélectionner des colonnes) qui vous donnent une visibilité sur les différentes caractéristiques de l’incident ou les entités impactées.</span><span class="sxs-lookup"><span data-stu-id="50f19-118">The incident queue has customizable columns (select **Choose columns**) that give you visibility into different characteristics of the incident or the impacted entities.</span></span> <span data-ttu-id="50f19-119">Cela vous permet de prendre une décision éclairée concernant la hiérquage des incidents à analyser.</span><span class="sxs-lookup"><span data-stu-id="50f19-119">This helps you make an informed decision regarding the prioritization of incidents for analysis.</span></span>

<span data-ttu-id="50f19-120">Pour une visibilité supplémentaire en un coup d’œil, l’appellation automatique des incidents génère des noms d’incident basés sur des attributs d’alerte tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="50f19-120">For additional visibility at a glance, automatic incident naming generates incident names based on alert attributes such as the number of endpoints affected, users affected, detection sources, or categories.</span></span> <span data-ttu-id="50f19-121">Cela vous permet de comprendre rapidement l’étendue de l’incident.</span><span class="sxs-lookup"><span data-stu-id="50f19-121">This allows you to quickly understand the scope of the incident.</span></span>

<span data-ttu-id="50f19-122">Par exemple : incident en plusieurs étapes sur plusieurs points de *terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="50f19-122">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>

> [!NOTE]
> <span data-ttu-id="50f19-123">Les incidents qui existaient avant le déploiement de la dénomination automatique des incidents ne seront pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="50f19-123">Incidents that existed prior the rollout of automatic incident naming will not have their name changed.</span></span>

<span data-ttu-id="50f19-124">La file d’attente des incidents expose également plusieurs options de filtrage qui, lorsqu’elles sont appliquées, vous permettent d’effectuer un large éventail de tous les incidents existants dans votre environnement ou de décider de vous concentrer sur un scénario ou une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="50f19-124">The incident queue also exposes multiple filtering options, that when applied, enable you to perform a broad sweep of all existing incidents in your environment, or decide to focus on a specific scenario or threat.</span></span> <span data-ttu-id="50f19-125">L’application de filtres dans la file d’attente des incidents permet de déterminer le type d’incident nécessitant une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="50f19-125">Applying filters on the incident queue can help determine which incident requires immediate attention.</span></span> 

## <a name="available-filters"></a><span data-ttu-id="50f19-126">Filtres disponibles</span><span class="sxs-lookup"><span data-stu-id="50f19-126">Available filters</span></span>

<span data-ttu-id="50f19-127">Dans la file d’attente des incidents par défaut, vous pouvez sélectionner **Filtres** pour afficher un volet Filtres, à partir duquel vous pouvez afficher un ensemble filtré d’incidents.</span><span class="sxs-lookup"><span data-stu-id="50f19-127">From the default incident queue, you can select **Filters** to see a Filters pane, from which you can view a filtered set of incidents.</span></span> <span data-ttu-id="50f19-128">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="50f19-128">Here is an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents-filters.png" alt-text="Exemple du volet Filtres de la file d’attente des incidents":::

<span data-ttu-id="50f19-130">Ce tableau répertorie les noms de filtres disponibles.</span><span class="sxs-lookup"><span data-stu-id="50f19-130">This table lists the filter names that are available.</span></span>

| <span data-ttu-id="50f19-131">Nom du filtre</span><span class="sxs-lookup"><span data-stu-id="50f19-131">Filter name</span></span> | <span data-ttu-id="50f19-132">Description</span><span class="sxs-lookup"><span data-stu-id="50f19-132">Description</span></span> |
|:-------|:-----|
| <span data-ttu-id="50f19-133">Affectée à</span><span class="sxs-lookup"><span data-stu-id="50f19-133">Assigned to</span></span> | <span data-ttu-id="50f19-134">Vous pouvez choisir d’afficher les alertes qui vous sont affectées ou celles gérées par l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="50f19-134">You can choose to show alerts that are assigned to you or those handled by automation.</span></span> |
| <span data-ttu-id="50f19-135">Catégories</span><span class="sxs-lookup"><span data-stu-id="50f19-135">Categories</span></span> | <span data-ttu-id="50f19-136">Choisissez des catégories pour vous concentrer sur des tactiques, des techniques ou des composants d’attaque spécifiques.</span><span class="sxs-lookup"><span data-stu-id="50f19-136">Choose categories to focus on specific tactics, techniques, or attack components seen.</span></span> |
| <span data-ttu-id="50f19-137">Classification</span><span class="sxs-lookup"><span data-stu-id="50f19-137">Classification</span></span> | <span data-ttu-id="50f19-138">Filtrez les incidents en fonction des classifications définies des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="50f19-138">Filter incidents based on the set classifications of the related alerts.</span></span> <span data-ttu-id="50f19-139">Les valeurs incluent des alertes vraies, des alertes fausses ou non définies.</span><span class="sxs-lookup"><span data-stu-id="50f19-139">The values include true alerts, false alerts, or not set.</span></span> |
| <span data-ttu-id="50f19-140">Confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="50f19-140">Data sensitivity</span></span> | <span data-ttu-id="50f19-141">Certaines attaques se concentrent sur le ciblage de données sensibles ou précieuses.</span><span class="sxs-lookup"><span data-stu-id="50f19-141">Some attacks focus on targeting to exfiltrate sensitive or valuable data.</span></span> <span data-ttu-id="50f19-142">En appliquant un filtre pour déterminer si des données confidentielles sont impliquées dans l’incident, vous pouvez rapidement déterminer si des informations sensibles ont été compromises et hiérarchiser les problèmes.</span><span class="sxs-lookup"><span data-stu-id="50f19-142">By applying a filter to see if sensitive data is involved in the incident, you can quickly determine if sensitive information has potentially been compromised and prioritize addressing those incidents.</span></span> <br><br> <span data-ttu-id="50f19-143">Applicable uniquement si la protection des informations Microsoft est activée.</span><span class="sxs-lookup"><span data-stu-id="50f19-143">Only applicable if Microsoft Information Protection is turned on.</span></span>|
| <span data-ttu-id="50f19-144">Groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="50f19-144">Device group</span></span> | <span data-ttu-id="50f19-145">Filtrer par groupes d’appareils définis.</span><span class="sxs-lookup"><span data-stu-id="50f19-145">Filter by defined device groups.</span></span> |
| <span data-ttu-id="50f19-146">État de l’examen</span><span class="sxs-lookup"><span data-stu-id="50f19-146">Investigation state</span></span> | <span data-ttu-id="50f19-147">Filtrer les incidents selon l’état de l’examen automatisé.</span><span class="sxs-lookup"><span data-stu-id="50f19-147">Filter incidents by the status of automated investigation.</span></span>  |
| <span data-ttu-id="50f19-148">Plusieurs catégories</span><span class="sxs-lookup"><span data-stu-id="50f19-148">Multiple categories</span></span> | <span data-ttu-id="50f19-149">Vous pouvez choisir de ne voir que les incidents qui ont été mappés à plusieurs catégories et qui peuvent donc potentiellement causer davantage de dommages.</span><span class="sxs-lookup"><span data-stu-id="50f19-149">You can choose to see only incidents that have mapped to multiple categories  and can thus potentially cause more damage.</span></span> |
| <span data-ttu-id="50f19-150">Plusieurs sources de service</span><span class="sxs-lookup"><span data-stu-id="50f19-150">Multiple service sources</span></span>  | <span data-ttu-id="50f19-151">Filtrez pour voir uniquement les incidents qui contiennent des alertes provenant de différentes sources (Microsoft Defender pour le point de terminaison, Microsoft Cloud App Security, Microsoft Defender pour l’identité, Microsoft Defender pour Office 365).</span><span class="sxs-lookup"><span data-stu-id="50f19-151">Filter to only see incidents that contain alerts from different sources (Microsoft Defender for Endpoint, Microsoft Cloud App Security, Microsoft Defender for Identity, Microsoft Defender for Office 365).</span></span> |
| <span data-ttu-id="50f19-152">Plateforme du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="50f19-152">OS platform</span></span> | <span data-ttu-id="50f19-153">Limitez l’affichage de la file d’attente des incidents par système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="50f19-153">Limit the incident queue view by operating system.</span></span> |
| <span data-ttu-id="50f19-154">Sources de service</span><span class="sxs-lookup"><span data-stu-id="50f19-154">Service sources</span></span> | <span data-ttu-id="50f19-155">En sélectionnant une source spécifique, vous pouvez vous concentrer sur les incidents qui contiennent au moins une alerte de la source choisie.</span><span class="sxs-lookup"><span data-stu-id="50f19-155">By choosing a specific source, you can focus on incidents that contain at least one alert from that chosen source.</span></span> |
| <span data-ttu-id="50f19-156">Severity</span><span class="sxs-lookup"><span data-stu-id="50f19-156">Severity</span></span> | <span data-ttu-id="50f19-157">La gravité d’un incident indique l’impact qu’il peut avoir sur vos ressources.</span><span class="sxs-lookup"><span data-stu-id="50f19-157">The severity of an incident is indicative of the impact it can have on your assets.</span></span> <span data-ttu-id="50f19-158">Plus la gravité est élevée, plus l’impact est important et nécessite généralement l’attention la plus immédiate.</span><span class="sxs-lookup"><span data-stu-id="50f19-158">The higher the severity, the bigger the impact and typically requires the most immediate attention.</span></span> |
| <span data-ttu-id="50f19-159">Statut</span><span class="sxs-lookup"><span data-stu-id="50f19-159">Status</span></span> | <span data-ttu-id="50f19-160">Vous pouvez choisir de limiter la liste des incidents affichés en fonction de leur état pour identifier ceux qui sont actifs ou résolus.</span><span class="sxs-lookup"><span data-stu-id="50f19-160">You can choose to limit the list of incidents shown based on their status to see which ones are active or resolved.</span></span> |
|||

## <a name="next-steps"></a><span data-ttu-id="50f19-161">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="50f19-161">Next steps</span></span>

<span data-ttu-id="50f19-162">Une fois que vous avez déterminé quel incident nécessite la priorité la plus élevée, sélectionnez-le et :</span><span class="sxs-lookup"><span data-stu-id="50f19-162">After you've determined which incident requires the highest priority, select it and:</span></span>

- <span data-ttu-id="50f19-163">[Gérer](manage-incidents.md) les propriétés de l’incident pour les balises, l’affectation à un analyste de sécurité et les commentaires.</span><span class="sxs-lookup"><span data-stu-id="50f19-163">[Manage](manage-incidents.md) the properties of the incident for tags, assignment to a security analyst, and comments.</span></span>
- <span data-ttu-id="50f19-164">Commencez votre [enquête.](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="50f19-164">Begin your [investigation](investigate-incidents.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="50f19-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50f19-165">See also</span></span>
- [<span data-ttu-id="50f19-166">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="50f19-166">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="50f19-167">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="50f19-167">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="50f19-168">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="50f19-168">Manage incidents</span></span>](manage-incidents.md)
