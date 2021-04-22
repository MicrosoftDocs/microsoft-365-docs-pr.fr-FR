---
title: Hiérarchiser les incidents dans Microsoft 365 Defender
description: Découvrez comment filtrer les incidents à partir de la file d'attente des incidents dans Microsoft 365 Defender
keywords: incident, file d'attente, vue d'ensemble, appareils, identités, utilisateurs, boîte aux lettres, courrier électronique, incidents, analyse, réponse
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
ms.openlocfilehash: c3efff1e7ebb3a5e868ede018512d12cf38e38fc
ms.sourcegitcommit: 4076b43a4b661de029f6307ddc1a989ab3108edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "51939705"
---
# <a name="prioritize-incidents-in-microsoft-365-defender"></a><span data-ttu-id="2bf7b-104">Hiérarchiser les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2bf7b-104">Prioritize incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="2bf7b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2bf7b-105">**Applies to:**</span></span>
- <span data-ttu-id="2bf7b-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2bf7b-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="2bf7b-107">Microsoft 365 Defender applique l'analyse de corrélation et regroupe les alertes associées et les enquêtes automatisées de différents produits dans un incident.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-107">Microsoft 365 Defender applies correlation analytics and aggregates related alerts and automated investigations from different products into an incident.</span></span> <span data-ttu-id="2bf7b-108">Microsoft 365 Defender déclenche également des alertes uniques sur les activités qui peuvent uniquement être identifiées comme malveillantes en raison de la visibilité de bout en bout de Microsoft 365 Defender sur l'ensemble de la suite de produits.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-108">Microsoft 365 Defender also triggers unique alerts on activities that can only be identified as malicious given the end-to-end visibility that Microsoft 365 Defender has across the entire suite of products.</span></span> <span data-ttu-id="2bf7b-109">Cette vue donne à vos analystes de sécurité un niveau d'attaque plus large, qui les aide à mieux comprendre et traiter les menaces complexes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-109">This view gives your security analysts the broader attack story, which help them better understand and deal with complex threats across your organization.</span></span>

<span data-ttu-id="2bf7b-110">La **file d'attente Incident** affiche un ensemble d'incidents qui ont été créés sur plusieurs appareils, utilisateurs et boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-110">The **Incident queue** shows a collection of incidents that were created across devices, users, and mailboxes.</span></span> <span data-ttu-id="2bf7b-111">Elle vous aide à trier les incidents afin de hiérarchiser et de créer une décision de réponse cyber-sécurité.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-111">It helps you sort through incidents to prioritize and create an informed cybersecurity response decision.</span></span> 

<span data-ttu-id="2bf7b-112">Vous pouvez vous rendre dans la file d'attente des incidents à partir d'incidents **& alertes** > Incidents dans le lancement rapide du Centre de sécurité Microsoft 365 ([security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="2bf7b-112">You get to the incident queue from **Incidents & alerts > Incidents** on the quick launch of the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)).</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents.png" alt-text="Exemple de file d'attente d'incident":::

<span data-ttu-id="2bf7b-114">Par défaut, la file d'attente des incidents dans le Centre de sécurité Microsoft 365 affiche les incidents observés au cours des six derniers mois.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-114">By default, the incident queue in the Microsoft 365 security center displays incidents seen in the last six months.</span></span> <span data-ttu-id="2bf7b-115">L'incident le plus récent se trouve en haut de la liste pour que vous le voyez en premier.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-115">The most recent incident is at the top of the list so you can see it first.</span></span>

<span data-ttu-id="2bf7b-116">La file d'attente des incidents possède des colonnes personnalisables (sélectionnez Sélectionner des colonnes) qui vous donnent une visibilité sur les différentes caractéristiques de l'incident ou les entités impactées.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-116">The incident queue has customizable columns (select **Choose columns**) that give you visibility into different characteristics of the incident or the impacted entities.</span></span> <span data-ttu-id="2bf7b-117">Cela vous permet de prendre une décision éclairée concernant la hiérquage des incidents à analyser.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-117">This helps you make an informed decision regarding the prioritization of incidents for analysis.</span></span>

<span data-ttu-id="2bf7b-118">Pour une visibilité supplémentaire en un coup d'œil, l'appellation automatique des incidents génère des noms d'incident basés sur des attributs d'alerte tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-118">For additional visibility at a glance, automatic incident naming generates incident names based on alert attributes such as the number of endpoints affected, users affected, detection sources, or categories.</span></span> <span data-ttu-id="2bf7b-119">Cela vous permet de comprendre rapidement l'étendue de l'incident.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-119">This allows you to quickly understand the scope of the incident.</span></span>

<span data-ttu-id="2bf7b-120">Par exemple : incident en plusieurs étapes sur plusieurs points de *terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="2bf7b-120">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>

> [!NOTE]
> <span data-ttu-id="2bf7b-121">Les incidents qui existaient avant le déploiement de la dénomination automatique des incidents ne seront pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-121">Incidents that existed prior the rollout of automatic incident naming will not have their name changed.</span></span>

<span data-ttu-id="2bf7b-122">La file d'attente des incidents expose également plusieurs options de filtrage qui, lorsqu'elles sont appliquées, vous permettent d'effectuer un large éventail de tous les incidents existants dans votre environnement ou de décider de vous concentrer sur un scénario ou une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-122">The incident queue also exposes multiple filtering options, that when applied, enable you to perform a broad sweep of all existing incidents in your environment, or decide to focus on a specific scenario or threat.</span></span> <span data-ttu-id="2bf7b-123">L’application de filtres dans la file d’attente des incidents permet de déterminer le type d’incident nécessitant une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-123">Applying filters on the incident queue can help determine which incident requires immediate attention.</span></span> 

## <a name="available-filters"></a><span data-ttu-id="2bf7b-124">Filtres disponibles</span><span class="sxs-lookup"><span data-stu-id="2bf7b-124">Available filters</span></span>

<span data-ttu-id="2bf7b-125">Dans la file d'attente des incidents par défaut, vous pouvez sélectionner **Filtres** pour afficher un volet Filtres, à partir duquel vous pouvez afficher un ensemble filtré d'incidents.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-125">From the default incident queue, you can select **Filters** to see a Filters pane, from which you can view a filtered set of incidents.</span></span> <span data-ttu-id="2bf7b-126">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-126">Here is an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents-filters.png" alt-text="Exemple du volet Filtres de la file d'attente des incidents":::

<span data-ttu-id="2bf7b-128">Ce tableau répertorie les noms de filtres disponibles.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-128">This table lists the filter names that are available.</span></span>

| <span data-ttu-id="2bf7b-129">Nom du filtre</span><span class="sxs-lookup"><span data-stu-id="2bf7b-129">Filter name</span></span> | <span data-ttu-id="2bf7b-130">Description</span><span class="sxs-lookup"><span data-stu-id="2bf7b-130">Description</span></span> |
|:-------|:-----|
| <span data-ttu-id="2bf7b-131">Affectée à</span><span class="sxs-lookup"><span data-stu-id="2bf7b-131">Assigned to</span></span> | <span data-ttu-id="2bf7b-132">Vous pouvez choisir d'afficher les alertes qui vous sont affectées ou celles gérées par l'automatisation.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-132">You can choose to show alerts that are assigned to you or those handled by automation.</span></span> |
| <span data-ttu-id="2bf7b-133">Catégories</span><span class="sxs-lookup"><span data-stu-id="2bf7b-133">Categories</span></span> | <span data-ttu-id="2bf7b-134">Choisissez des catégories pour vous concentrer sur des tactiques, des techniques ou des composants d'attaque spécifiques.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-134">Choose categories to focus on specific tactics, techniques, or attack components seen.</span></span> |
| <span data-ttu-id="2bf7b-135">Classification</span><span class="sxs-lookup"><span data-stu-id="2bf7b-135">Classification</span></span> | <span data-ttu-id="2bf7b-136">Filtrez les incidents en fonction des classifications définies des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-136">Filter incidents based on the set classifications of the related alerts.</span></span> <span data-ttu-id="2bf7b-137">Les valeurs incluent des alertes vraies, des alertes fausses ou non définies.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-137">The values include true alerts, false alerts, or not set.</span></span> |
| <span data-ttu-id="2bf7b-138">Confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="2bf7b-138">Data sensitivity</span></span> | <span data-ttu-id="2bf7b-139">Certaines attaques se concentrent sur le ciblage de données sensibles ou précieuses.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-139">Some attacks focus on targeting to exfiltrate sensitive or valuable data.</span></span> <span data-ttu-id="2bf7b-140">En appliquant un filtre pour déterminer si des données confidentielles sont impliquées dans l’incident, vous pouvez rapidement déterminer si des informations sensibles ont été compromises et hiérarchiser les problèmes.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-140">By applying a filter to see if sensitive data is involved in the incident, you can quickly determine if sensitive information has potentially been compromised and prioritize addressing those incidents.</span></span> <br><br> <span data-ttu-id="2bf7b-141">Applicable uniquement si la protection des informations Microsoft est activée.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-141">Only applicable if Microsoft Information Protection is turned on.</span></span>|
| <span data-ttu-id="2bf7b-142">Groupe d'appareils</span><span class="sxs-lookup"><span data-stu-id="2bf7b-142">Device group</span></span> | <span data-ttu-id="2bf7b-143">Filtrer par groupes d'appareils définis.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-143">Filter by defined device groups.</span></span> |
| <span data-ttu-id="2bf7b-144">État de l'examen</span><span class="sxs-lookup"><span data-stu-id="2bf7b-144">Investigation state</span></span> | <span data-ttu-id="2bf7b-145">Filtrer les incidents selon l'état de l'examen automatisé.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-145">Filter incidents by the status of automated investigation.</span></span>  |
| <span data-ttu-id="2bf7b-146">Plusieurs catégories</span><span class="sxs-lookup"><span data-stu-id="2bf7b-146">Multiple categories</span></span> | <span data-ttu-id="2bf7b-147">Vous pouvez choisir de ne voir que les incidents qui ont été mappés à plusieurs catégories et qui peuvent donc potentiellement causer davantage de dommages.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-147">You can choose to see only incidents that have mapped to multiple categories  and can thus potentially cause more damage.</span></span> |
| <span data-ttu-id="2bf7b-148">Plusieurs sources de service</span><span class="sxs-lookup"><span data-stu-id="2bf7b-148">Multiple service sources</span></span>  | <span data-ttu-id="2bf7b-149">Filtrez pour voir uniquement les incidents qui contiennent des alertes provenant de différentes sources (Microsoft Defender pour endpoint, Microsoft Cloud App Security, Microsoft Defender pour l'identité, Microsoft Defender pour Office 365).</span><span class="sxs-lookup"><span data-stu-id="2bf7b-149">Filter to only see incidents that contain alerts from different sources (Microsoft Defender for Endpoint, Microsoft Cloud App Security, Microsoft Defender for Identity, Microsoft Defender for Office 365).</span></span> |
| <span data-ttu-id="2bf7b-150">Plateforme du système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="2bf7b-150">OS platform</span></span> | <span data-ttu-id="2bf7b-151">Limitez l'affichage de la file d'attente des incidents par système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-151">Limit the incident queue view by operating system.</span></span> |
| <span data-ttu-id="2bf7b-152">Sources de service</span><span class="sxs-lookup"><span data-stu-id="2bf7b-152">Service sources</span></span> | <span data-ttu-id="2bf7b-153">En sélectionnant une source spécifique, vous pouvez vous concentrer sur les incidents qui contiennent au moins une alerte de la source choisie.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-153">By choosing a specific source, you can focus on incidents that contain at least one alert from that chosen source.</span></span> |
| <span data-ttu-id="2bf7b-154">Severity</span><span class="sxs-lookup"><span data-stu-id="2bf7b-154">Severity</span></span> | <span data-ttu-id="2bf7b-155">La gravité d'un incident indique l'impact qu'il peut avoir sur vos ressources.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-155">The severity of an incident is indicative of the impact it can have on your assets.</span></span> <span data-ttu-id="2bf7b-156">Plus la gravité est élevée, plus l'impact est important et nécessite généralement l'attention la plus immédiate.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-156">The higher the severity, the bigger the impact and typically requires the most immediate attention.</span></span> |
| <span data-ttu-id="2bf7b-157">Statut</span><span class="sxs-lookup"><span data-stu-id="2bf7b-157">Status</span></span> | <span data-ttu-id="2bf7b-158">Vous pouvez choisir de limiter la liste des incidents affichés en fonction de leur état pour identifier ceux qui sont actifs ou résolus.</span><span class="sxs-lookup"><span data-stu-id="2bf7b-158">You can choose to limit the list of incidents shown based on their status to see which ones are active or resolved.</span></span> |
|||

## <a name="next-step"></a><span data-ttu-id="2bf7b-159">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2bf7b-159">Next step</span></span>

<span data-ttu-id="2bf7b-160">Une fois que vous avez déterminé quel incident nécessite la priorité la plus élevée, sélectionnez-le et commencez votre [analyse.](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="2bf7b-160">After you've determined which incident requires the highest priority, select it and begin your [analysis](investigate-incidents.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2bf7b-161">Articles associés</span><span class="sxs-lookup"><span data-stu-id="2bf7b-161">See also</span></span>
- [<span data-ttu-id="2bf7b-162">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="2bf7b-162">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="2bf7b-163">Analyser les incidents</span><span class="sxs-lookup"><span data-stu-id="2bf7b-163">Analyze incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="2bf7b-164">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="2bf7b-164">Manage incidents</span></span>](manage-incidents.md)
