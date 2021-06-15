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
ms.openlocfilehash: 07a49fcdcfa7ea401b16b293b4831244253d2b28
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52925886"
---
# <a name="prioritize-incidents-in-microsoft-365-defender"></a><span data-ttu-id="8f01f-104">Hiérarchiser les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8f01f-104">Prioritize incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="8f01f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8f01f-105">**Applies to:**</span></span>
- <span data-ttu-id="8f01f-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8f01f-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="8f01f-107">Microsoft 365 Defender applique l’analyse de corrélation et regroupe les alertes associées et les enquêtes automatisées de différents produits dans un incident.</span><span class="sxs-lookup"><span data-stu-id="8f01f-107">Microsoft 365 Defender applies correlation analytics and aggregates related alerts and automated investigations from different products into an incident.</span></span> <span data-ttu-id="8f01f-108">Microsoft 365 Defender déclenche également des alertes uniques sur les activités qui peuvent uniquement être identifiées comme malveillantes en raison de la visibilité de bout en bout dont dispose Microsoft 365 Defender sur l’ensemble de la suite de produits.</span><span class="sxs-lookup"><span data-stu-id="8f01f-108">Microsoft 365 Defender also triggers unique alerts on activities that can only be identified as malicious given the end-to-end visibility that Microsoft 365 Defender has across the entire suite of products.</span></span> <span data-ttu-id="8f01f-109">Cette vue donne à vos analystes de sécurité un niveau d’attaque plus large, qui les aide à mieux comprendre et traiter les menaces complexes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8f01f-109">This view gives your security analysts the broader attack story, which help them better understand and deal with complex threats across your organization.</span></span>

<span data-ttu-id="8f01f-110">La **file d’attente Incident** affiche un ensemble d’incidents qui ont été créés sur plusieurs appareils, utilisateurs et boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="8f01f-110">The **Incident queue** shows a collection of incidents that were created across devices, users, and mailboxes.</span></span> <span data-ttu-id="8f01f-111">Elle vous aide à trier les incidents afin de hiérarchiser et de créer une décision de réponse cyber-sécurité.</span><span class="sxs-lookup"><span data-stu-id="8f01f-111">It helps you sort through incidents to prioritize and create an informed cybersecurity response decision.</span></span> 

<span data-ttu-id="8f01f-112">Vous pouvez vous rendre dans la file d’attente des incidents à partir **d’incidents & alertes** > Incidents lors du lancement rapide du centre de sécurité Microsoft 365 ([security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="8f01f-112">You get to the incident queue from **Incidents & alerts > Incidents** on the quick launch of the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)).</span></span> <span data-ttu-id="8f01f-113">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="8f01f-113">Here's an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents.png" alt-text="Exemple de file d’attente d’incident":::

<span data-ttu-id="8f01f-115">La section **Incidents et alertes** les plus récents présente un graphique du nombre d’alertes reçues et d’incidents créés au cours des dernières 24 heures.</span><span class="sxs-lookup"><span data-stu-id="8f01f-115">The **Most recent incidents and alerts** section shows a graph of the number of alerts received and incidents created in the last 24 hours.</span></span>

<span data-ttu-id="8f01f-116">Par défaut, la file d’attente des incidents dans Microsoft 365 centre de sécurité affiche les incidents observés au cours des six derniers mois.</span><span class="sxs-lookup"><span data-stu-id="8f01f-116">By default, the incident queue in the Microsoft 365 security center displays incidents seen in the last six months.</span></span> <span data-ttu-id="8f01f-117">L’incident le plus récent se trouve en haut de la liste pour que vous le voyez en premier.</span><span class="sxs-lookup"><span data-stu-id="8f01f-117">The most recent incident is at the top of the list so you can see it first.</span></span>

<span data-ttu-id="8f01f-118">La file d’attente des incidents possède des colonnes personnalisables (sélectionnez Sélectionner des colonnes) qui vous donnent une visibilité sur les différentes caractéristiques de l’incident ou les entités impactées.</span><span class="sxs-lookup"><span data-stu-id="8f01f-118">The incident queue has customizable columns (select **Choose columns**) that give you visibility into different characteristics of the incident or the impacted entities.</span></span> <span data-ttu-id="8f01f-119">Cela vous permet de prendre une décision éclairée concernant la hiérquage des incidents à analyser.</span><span class="sxs-lookup"><span data-stu-id="8f01f-119">This helps you make an informed decision regarding the prioritization of incidents for analysis.</span></span>

<span data-ttu-id="8f01f-120">Pour une visibilité supplémentaire en un coup d’œil, l’appellation automatique des incidents génère des noms d’incident basés sur des attributs d’alerte tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="8f01f-120">For additional visibility at a glance, automatic incident naming generates incident names based on alert attributes such as the number of endpoints affected, users affected, detection sources, or categories.</span></span> <span data-ttu-id="8f01f-121">Cela vous permet de comprendre rapidement l’étendue de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8f01f-121">This allows you to quickly understand the scope of the incident.</span></span>

<span data-ttu-id="8f01f-122">Par exemple : incident en plusieurs étapes sur plusieurs points de *terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="8f01f-122">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>

> [!NOTE]
> <span data-ttu-id="8f01f-123">Les incidents qui existaient avant le déploiement de la dénomination automatique des incidents ne seront pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="8f01f-123">Incidents that existed prior the rollout of automatic incident naming will not have their name changed.</span></span>

<span data-ttu-id="8f01f-124">La file d’attente des incidents expose également plusieurs options de filtrage qui, lorsqu’elles sont appliquées, vous permettent d’effectuer un large éventail de tous les incidents existants dans votre environnement ou de décider de vous concentrer sur un scénario ou une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="8f01f-124">The incident queue also exposes multiple filtering options, that when applied, enable you to perform a broad sweep of all existing incidents in your environment, or decide to focus on a specific scenario or threat.</span></span> <span data-ttu-id="8f01f-125">L’application de filtres dans la file d’attente des incidents permet de déterminer le type d’incident nécessitant une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="8f01f-125">Applying filters on the incident queue can help determine which incident requires immediate attention.</span></span> 

## <a name="available-filters"></a><span data-ttu-id="8f01f-126">Filtres disponibles</span><span class="sxs-lookup"><span data-stu-id="8f01f-126">Available filters</span></span>

<span data-ttu-id="8f01f-127">Dans la file d’attente des incidents par défaut, vous pouvez sélectionner **Filtres** pour afficher un volet Filtres, à partir duquel vous pouvez afficher un ensemble filtré d’incidents.</span><span class="sxs-lookup"><span data-stu-id="8f01f-127">From the default incident queue, you can select **Filters** to see a Filters pane, from which you can view a filtered set of incidents.</span></span> <span data-ttu-id="8f01f-128">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="8f01f-128">Here is an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents-filters.png" alt-text="Exemple du volet filtres de la file d’attente des incidents":::

<span data-ttu-id="8f01f-130">Ce tableau répertorie les noms de filtres disponibles.</span><span class="sxs-lookup"><span data-stu-id="8f01f-130">This table lists the filter names that are available.</span></span>

| <span data-ttu-id="8f01f-131">Nom du filtre</span><span class="sxs-lookup"><span data-stu-id="8f01f-131">Filter name</span></span> | <span data-ttu-id="8f01f-132">Description</span><span class="sxs-lookup"><span data-stu-id="8f01f-132">Description</span></span> |
|:-------|:-----|
| <span data-ttu-id="8f01f-133">Affectée à</span><span class="sxs-lookup"><span data-stu-id="8f01f-133">Assigned to</span></span> | <span data-ttu-id="8f01f-134">Vous pouvez choisir d’afficher les alertes qui vous sont affectées ou celles gérées par l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="8f01f-134">You can choose to show alerts that are assigned to you or those handled by automation.</span></span> |
| <span data-ttu-id="8f01f-135">Catégories</span><span class="sxs-lookup"><span data-stu-id="8f01f-135">Categories</span></span> | <span data-ttu-id="8f01f-136">Choisissez des catégories pour vous concentrer sur des tactiques, des techniques ou des composants d’attaque spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8f01f-136">Choose categories to focus on specific tactics, techniques, or attack components seen.</span></span> |
| <span data-ttu-id="8f01f-137">Classification</span><span class="sxs-lookup"><span data-stu-id="8f01f-137">Classification</span></span> | <span data-ttu-id="8f01f-138">Filtrez les incidents en fonction des classifications définies des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="8f01f-138">Filter incidents based on the set classifications of the related alerts.</span></span> <span data-ttu-id="8f01f-139">Les valeurs incluent des alertes vraies, des alertes fausses ou non définies.</span><span class="sxs-lookup"><span data-stu-id="8f01f-139">The values include true alerts, false alerts, or not set.</span></span> |
| <span data-ttu-id="8f01f-140">Confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="8f01f-140">Data sensitivity</span></span> | <span data-ttu-id="8f01f-141">Certaines attaques se concentrent sur le ciblage de données sensibles ou précieuses.</span><span class="sxs-lookup"><span data-stu-id="8f01f-141">Some attacks focus on targeting to exfiltrate sensitive or valuable data.</span></span> <span data-ttu-id="8f01f-142">En appliquant un filtre pour déterminer si des données confidentielles sont impliquées dans l’incident, vous pouvez rapidement déterminer si des informations sensibles ont été compromises et hiérarchiser les problèmes.</span><span class="sxs-lookup"><span data-stu-id="8f01f-142">By applying a filter to see if sensitive data is involved in the incident, you can quickly determine if sensitive information has potentially been compromised and prioritize addressing those incidents.</span></span> <br><br> <span data-ttu-id="8f01f-143">Applicable uniquement si la protection des informations Microsoft est activée.</span><span class="sxs-lookup"><span data-stu-id="8f01f-143">Only applicable if Microsoft Information Protection is turned on.</span></span>|
| <span data-ttu-id="8f01f-144">Groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="8f01f-144">Device group</span></span> | <span data-ttu-id="8f01f-145">Filtrer par groupes d’appareils définis.</span><span class="sxs-lookup"><span data-stu-id="8f01f-145">Filter by defined device groups.</span></span> |
| <span data-ttu-id="8f01f-146">État de l’examen</span><span class="sxs-lookup"><span data-stu-id="8f01f-146">Investigation state</span></span> | <span data-ttu-id="8f01f-147">Filtrer les incidents selon l’état de l’examen automatisé.</span><span class="sxs-lookup"><span data-stu-id="8f01f-147">Filter incidents by the status of automated investigation.</span></span>  |
| <span data-ttu-id="8f01f-148">Plusieurs catégories</span><span class="sxs-lookup"><span data-stu-id="8f01f-148">Multiple categories</span></span> | <span data-ttu-id="8f01f-149">Vous pouvez choisir de ne voir que les incidents qui ont été mappés à plusieurs catégories et qui peuvent donc potentiellement causer davantage de dommages.</span><span class="sxs-lookup"><span data-stu-id="8f01f-149">You can choose to see only incidents that have mapped to multiple categories  and can thus potentially cause more damage.</span></span> |
| <span data-ttu-id="8f01f-150">Plusieurs sources de service</span><span class="sxs-lookup"><span data-stu-id="8f01f-150">Multiple service sources</span></span>  | <span data-ttu-id="8f01f-151">Filtrez pour voir uniquement les incidents qui contiennent des alertes provenant de différentes sources (Microsoft Defender pour le point de terminaison, Microsoft Cloud App Security, Microsoft Defender pour l’identité, Microsoft Defender pour Office 365).</span><span class="sxs-lookup"><span data-stu-id="8f01f-151">Filter to only see incidents that contain alerts from different sources (Microsoft Defender for Endpoint, Microsoft Cloud App Security, Microsoft Defender for Identity, Microsoft Defender for Office 365).</span></span> |
| <span data-ttu-id="8f01f-152">Plateforme du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="8f01f-152">OS platform</span></span> | <span data-ttu-id="8f01f-153">Limitez l’affichage de la file d’attente des incidents par système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8f01f-153">Limit the incident queue view by operating system.</span></span> |
| <span data-ttu-id="8f01f-154">Sources de service</span><span class="sxs-lookup"><span data-stu-id="8f01f-154">Service sources</span></span> | <span data-ttu-id="8f01f-155">En sélectionnant une source spécifique, vous pouvez vous concentrer sur les incidents qui contiennent au moins une alerte de la source choisie.</span><span class="sxs-lookup"><span data-stu-id="8f01f-155">By choosing a specific source, you can focus on incidents that contain at least one alert from that chosen source.</span></span> |
| <span data-ttu-id="8f01f-156">Severity</span><span class="sxs-lookup"><span data-stu-id="8f01f-156">Severity</span></span> | <span data-ttu-id="8f01f-157">La gravité d’un incident indique l’impact qu’il peut avoir sur vos ressources.</span><span class="sxs-lookup"><span data-stu-id="8f01f-157">The severity of an incident is indicative of the impact it can have on your assets.</span></span> <span data-ttu-id="8f01f-158">Plus la gravité est élevée, plus l’impact est important et nécessite généralement l’attention la plus immédiate.</span><span class="sxs-lookup"><span data-stu-id="8f01f-158">The higher the severity, the bigger the impact and typically requires the most immediate attention.</span></span> |
| <span data-ttu-id="8f01f-159">Statut</span><span class="sxs-lookup"><span data-stu-id="8f01f-159">Status</span></span> | <span data-ttu-id="8f01f-160">Vous pouvez choisir de limiter la liste des incidents affichés en fonction de leur état pour identifier ceux qui sont actifs ou résolus.</span><span class="sxs-lookup"><span data-stu-id="8f01f-160">You can choose to limit the list of incidents shown based on their status to see which ones are active or resolved.</span></span> |
|||

## <a name="save-defined-filters-as-urls"></a><span data-ttu-id="8f01f-161">Enregistrer les filtres définis en tant qu’URL</span><span class="sxs-lookup"><span data-stu-id="8f01f-161">Save defined filters as URLs</span></span>

<span data-ttu-id="8f01f-162">Une fois que vous avez configuré un filtre utile dans la file d’attente des incidents, vous pouvez mettre en signet l’URL de l’onglet du navigateur ou l’enregistrer en tant que lien sur une page Web, un document Word ou un lieu de votre choix.</span><span class="sxs-lookup"><span data-stu-id="8f01f-162">Once you have configured a useful filter in the incidents queue, you can bookmark the URL of the browser tab or otherwise save it as a link on a Web page, a Word document, or a place of your choice.</span></span> <span data-ttu-id="8f01f-163">Cela vous permettra d’accéder en un seul clic aux vues clés de la file d’attente des incidents, telles que :</span><span class="sxs-lookup"><span data-stu-id="8f01f-163">This will give you single-click access to key views of the incident queue, such as:</span></span>

- <span data-ttu-id="8f01f-164">Nouveaux incidents</span><span class="sxs-lookup"><span data-stu-id="8f01f-164">New incidents</span></span>
- <span data-ttu-id="8f01f-165">Incidents de gravité élevée</span><span class="sxs-lookup"><span data-stu-id="8f01f-165">High-severity incidents</span></span>
- <span data-ttu-id="8f01f-166">Incidents non signés</span><span class="sxs-lookup"><span data-stu-id="8f01f-166">Unassigned incidents</span></span>
- <span data-ttu-id="8f01f-167">Incidents non signés de gravité élevée</span><span class="sxs-lookup"><span data-stu-id="8f01f-167">High-severity, unassigned incidents</span></span>
- <span data-ttu-id="8f01f-168">Incidents qui m’ont été attribués</span><span class="sxs-lookup"><span data-stu-id="8f01f-168">Incidents assigned to me</span></span>
- <span data-ttu-id="8f01f-169">Incidents qui m’ont été attribués et pour Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8f01f-169">Incidents assigned to me and for Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="8f01f-170">Incidents avec une ou plusieurs balises spécifiques</span><span class="sxs-lookup"><span data-stu-id="8f01f-170">Incidents with a specific tag or tags</span></span>
- <span data-ttu-id="8f01f-171">Incidents avec une catégorie de menace spécifique</span><span class="sxs-lookup"><span data-stu-id="8f01f-171">Incidents with a specific threat category</span></span>
- <span data-ttu-id="8f01f-172">Incidents avec une menace associée spécifique</span><span class="sxs-lookup"><span data-stu-id="8f01f-172">Incidents with a specific associated threat</span></span>
- <span data-ttu-id="8f01f-173">Incidents avec un acteur spécifique</span><span class="sxs-lookup"><span data-stu-id="8f01f-173">Incidents with a specific actor</span></span>

<span data-ttu-id="8f01f-174">Une fois que vous avez compilé et stocké votre liste d’affichages de filtre utiles en tant [](manage-incidents.md) qu’URL, vous pouvez l’utiliser rapidement pour traiter et hiérarchiser les incidents dans votre file d’attente et les gérer pour analyse ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8f01f-174">Once you have compiled and stored your list of useful filter views as URLs, you can use it quickly process and prioritize the incidents in your queue and [manage](manage-incidents.md) them for subsequent analysis.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8f01f-175">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8f01f-175">Next steps</span></span>

<span data-ttu-id="8f01f-176">Une fois que vous avez déterminé quel incident nécessite la priorité la plus élevée, sélectionnez-le et :</span><span class="sxs-lookup"><span data-stu-id="8f01f-176">After you've determined which incident requires the highest priority, select it and:</span></span>

- <span data-ttu-id="8f01f-177">[Gérer les](manage-incidents.md) propriétés de l’incident pour les balises, l’affectation, la résolution immédiate des incidents faux positifs et les commentaires.</span><span class="sxs-lookup"><span data-stu-id="8f01f-177">[Manage](manage-incidents.md) the properties of the incident for tags, assignment, immediate resolution for false positive incidents, and comments.</span></span>
- <span data-ttu-id="8f01f-178">Commencez vos [enquêtes.](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="8f01f-178">Begin your [investigations](investigate-incidents.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8f01f-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f01f-179">See also</span></span>
- [<span data-ttu-id="8f01f-180">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="8f01f-180">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="8f01f-181">Gérer des incidents</span><span class="sxs-lookup"><span data-stu-id="8f01f-181">Manage incidents</span></span>](manage-incidents.md)
- [<span data-ttu-id="8f01f-182">Examiner des incidents</span><span class="sxs-lookup"><span data-stu-id="8f01f-182">Investigate incidents</span></span>](investigate-incidents.md)
