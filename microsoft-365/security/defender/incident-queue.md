---
title: Hiérarchiser les incidents dans Microsoft 365 Defender
description: Découvrez comment filtrer les incidents à partir de la file d'attente des incidents dans Microsoft 365 Defender
keywords: incident, file d’attente, vue d’ensemble, appareils, identités, utilisateurs, boîte aux lettres, e-mail, incidents
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
ms.openlocfilehash: 3b381749108d4a75024d9a546c0d3f1631c948ed
ms.sourcegitcommit: 76f3c75413cc960289489d0ca29efadb8a9a5b31
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/19/2021
ms.locfileid: "51887256"
---
# <a name="prioritize-incidents-in-microsoft-365-defender"></a><span data-ttu-id="bd1db-104">Hiérarchiser les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bd1db-104">Prioritize incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="bd1db-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bd1db-105">**Applies to:**</span></span>
- <span data-ttu-id="bd1db-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bd1db-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="bd1db-107">Microsoft 365 Defender applique l'analyse de corrélation et regroupe les alertes associées et les enquêtes automatisées de différents produits dans un incident.</span><span class="sxs-lookup"><span data-stu-id="bd1db-107">Microsoft 365 Defender applies correlation analytics and aggregates related alerts and automated investigations from different products into an incident.</span></span> <span data-ttu-id="bd1db-108">Microsoft 365 Defender déclenche également des alertes uniques sur les activités qui peuvent uniquement être identifiées comme malveillantes en raison de la visibilité de bout en bout de Microsoft 365 Defender sur l'ensemble de la suite de produits.</span><span class="sxs-lookup"><span data-stu-id="bd1db-108">Microsoft 365 Defender also triggers unique alerts on activities that can only be identified as malicious given the end-to-end visibility that Microsoft 365 Defender has across the entire suite of products.</span></span> <span data-ttu-id="bd1db-109">Cette vue offre à vos analystes de sécurité un niveau d'attaque plus large, qui les aide à mieux comprendre et traiter les menaces complexes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bd1db-109">This view gives your security analysts the broader attack story, which help them better understand and deal with complex threats across your organization.</span></span>

<span data-ttu-id="bd1db-110">La **file d'attente Incident** affiche un ensemble d'incidents qui ont été créés sur des appareils, des utilisateurs et des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="bd1db-110">The **Incident queue** shows a collection of incidents that were created across devices, users, and mailboxes.</span></span> <span data-ttu-id="bd1db-111">Elle vous aide à trier les incidents afin de hiérarchiser et de créer une décision de réponse cyber-sécurité.</span><span class="sxs-lookup"><span data-stu-id="bd1db-111">It helps you sort through incidents to prioritize and create an informed cybersecurity response decision.</span></span> 

<span data-ttu-id="bd1db-112">Vous pouvez vous rendre dans la file d'attente des incidents à partir d'incidents **& alertes** > Incidents dans le lancement rapide du Centre de sécurité Microsoft 365 ([security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="bd1db-112">You get to the incident queue from **Incidents & alerts > Incidents** on the quick launch of the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)).</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents.png" alt-text="Exemple de file d'attente d'incident":::

<span data-ttu-id="bd1db-114">Par défaut, la file d'attente des incidents dans le Centre de sécurité Microsoft 365 affiche les incidents observés au cours des six derniers mois.</span><span class="sxs-lookup"><span data-stu-id="bd1db-114">By default, the incident queue in the Microsoft 365 security center displays incidents seen in the last six months.</span></span> <span data-ttu-id="bd1db-115">L'incident le plus récent se trouve en haut de la liste pour que vous le voyez en premier.</span><span class="sxs-lookup"><span data-stu-id="bd1db-115">The most recent incident is at the top of the list so you can see it first.</span></span>

<span data-ttu-id="bd1db-116">La file d'attente des incidents possède des colonnes personnalisables (sélectionnez Sélectionner des colonnes) qui vous donnent une visibilité sur les différentes caractéristiques de l'incident ou les entités impactées.</span><span class="sxs-lookup"><span data-stu-id="bd1db-116">The incident queue has customizable columns (select **Choose columns**) that give you visibility into different characteristics of the incident or the impacted entities.</span></span> <span data-ttu-id="bd1db-117">Cela vous permet de prendre une décision éclairée concernant la hiérquage des incidents à analyser.</span><span class="sxs-lookup"><span data-stu-id="bd1db-117">This helps you make an informed decision regarding the prioritization of incidents for analysis.</span></span>

<span data-ttu-id="bd1db-118">Pour une visibilité supplémentaire en un coup d'œil, l'appellation automatique des incidents génère des noms d'incident basés sur des attributs d'alerte tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="bd1db-118">For additional visibility at a glance, automatic incident naming generates incident names based on alert attributes such as the number of endpoints affected, users affected, detection sources, or categories.</span></span> <span data-ttu-id="bd1db-119">Cela vous permet de comprendre rapidement l'étendue de l'incident.</span><span class="sxs-lookup"><span data-stu-id="bd1db-119">This allows you to quickly understand the scope of the incident.</span></span>

<span data-ttu-id="bd1db-120">Par exemple : *incident en plusieurs étapes sur plusieurs points de terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="bd1db-120">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>

> [!NOTE]
> <span data-ttu-id="bd1db-121">Les incidents qui existaient avant le déploiement de la dénomination automatique des incidents ne seront pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="bd1db-121">Incidents that existed prior the rollout of automatic incident naming will not have their name changed.</span></span>

<span data-ttu-id="bd1db-122">La file d'attente des incidents expose également plusieurs options de filtrage qui, lorsqu'elles sont appliquées, vous permettent d'effectuer un large éventail de tous les incidents existants dans votre environnement ou de décider de vous concentrer sur un scénario ou une menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="bd1db-122">The incident queue also exposes multiple filtering options, that when applied, enable you to perform a broad sweep of all existing incidents in your environment, or decide to focus on a specific scenario or threat.</span></span> <span data-ttu-id="bd1db-123">L’application de filtres dans la file d’attente des incidents permet de déterminer le type d’incident nécessitant une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="bd1db-123">Applying filters on the incident queue can help determine which incident requires immediate attention.</span></span> 

## <a name="available-filters"></a><span data-ttu-id="bd1db-124">Filtres disponibles</span><span class="sxs-lookup"><span data-stu-id="bd1db-124">Available filters</span></span>

<span data-ttu-id="bd1db-125">Dans la file d'attente des incidents par défaut, vous pouvez sélectionner **Filtres** pour afficher un volet Filtres, à partir duquel vous pouvez afficher un ensemble filtré d'incidents.</span><span class="sxs-lookup"><span data-stu-id="bd1db-125">From the default incident queue, you can select **Filters** to see a Filters pane, from which you can view a filtered set of incidents.</span></span> <span data-ttu-id="bd1db-126">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="bd1db-126">Here is an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents-filters.png" alt-text="Exemple du volet filtres de la file d'attente des incidents":::

<span data-ttu-id="bd1db-128">Ce tableau répertorie les noms de filtres disponibles.</span><span class="sxs-lookup"><span data-stu-id="bd1db-128">This table lists the filter names that are available.</span></span>

| <span data-ttu-id="bd1db-129">Nom du filtre</span><span class="sxs-lookup"><span data-stu-id="bd1db-129">Filter name</span></span> | <span data-ttu-id="bd1db-130">Description</span><span class="sxs-lookup"><span data-stu-id="bd1db-130">Description</span></span> |
|:-------|:-----|
| <span data-ttu-id="bd1db-131">Affectée à</span><span class="sxs-lookup"><span data-stu-id="bd1db-131">Assigned to</span></span> | <span data-ttu-id="bd1db-132">Vous pouvez choisir d'afficher les alertes qui vous sont affectées ou celles gérées par l'automatisation.</span><span class="sxs-lookup"><span data-stu-id="bd1db-132">You can choose to show alerts that are assigned to you or those handled by automation.</span></span> |
| <span data-ttu-id="bd1db-133">Catégories</span><span class="sxs-lookup"><span data-stu-id="bd1db-133">Categories</span></span> | <span data-ttu-id="bd1db-134">Choisissez des catégories pour vous concentrer sur des tactiques, des techniques ou des composants d'attaque spécifiques.</span><span class="sxs-lookup"><span data-stu-id="bd1db-134">Choose categories to focus on specific tactics, techniques, or attack components seen.</span></span> |
| <span data-ttu-id="bd1db-135">Classification</span><span class="sxs-lookup"><span data-stu-id="bd1db-135">Classification</span></span> | <span data-ttu-id="bd1db-136">Filtrer les incidents en fonction des classifications définies des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="bd1db-136">Filter incidents based on the set classifications of the related alerts.</span></span> <span data-ttu-id="bd1db-137">Les valeurs incluent des alertes vraies, des alertes fausses ou non définies.</span><span class="sxs-lookup"><span data-stu-id="bd1db-137">The values include true alerts, false alerts, or not set.</span></span> |
| <span data-ttu-id="bd1db-138">Confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="bd1db-138">Data sensitivity</span></span> | <span data-ttu-id="bd1db-139">Certaines attaques se concentrent sur le ciblage de données sensibles ou précieuses.</span><span class="sxs-lookup"><span data-stu-id="bd1db-139">Some attacks focus on targeting to exfiltrate sensitive or valuable data.</span></span> <span data-ttu-id="bd1db-140">En appliquant un filtre pour déterminer si des données confidentielles sont impliquées dans l’incident, vous pouvez rapidement déterminer si des informations sensibles ont été compromises et hiérarchiser les problèmes.</span><span class="sxs-lookup"><span data-stu-id="bd1db-140">By applying a filter to see if sensitive data is involved in the incident, you can quickly determine if sensitive information has potentially been compromised and prioritize addressing those incidents.</span></span> <br><br> <span data-ttu-id="bd1db-141">Applicable uniquement si la protection des informations Microsoft est activée.</span><span class="sxs-lookup"><span data-stu-id="bd1db-141">Only applicable if Microsoft Information Protection is turned on.</span></span>|
| <span data-ttu-id="bd1db-142">Groupe d'appareils</span><span class="sxs-lookup"><span data-stu-id="bd1db-142">Device group</span></span> | <span data-ttu-id="bd1db-143">Filtrer par groupes d'appareils définis.</span><span class="sxs-lookup"><span data-stu-id="bd1db-143">Filter by defined device groups.</span></span> |
| <span data-ttu-id="bd1db-144">État de l'examen</span><span class="sxs-lookup"><span data-stu-id="bd1db-144">Investigation state</span></span> | <span data-ttu-id="bd1db-145">Filtrer les incidents selon l'état de l'examen automatisé.</span><span class="sxs-lookup"><span data-stu-id="bd1db-145">Filter incidents by the status of automated investigation.</span></span>  |
| <span data-ttu-id="bd1db-146">Plusieurs catégories</span><span class="sxs-lookup"><span data-stu-id="bd1db-146">Multiple categories</span></span> | <span data-ttu-id="bd1db-147">Vous pouvez choisir de ne voir que les incidents qui ont été mappés à plusieurs catégories et qui peuvent donc potentiellement causer davantage de dommages.</span><span class="sxs-lookup"><span data-stu-id="bd1db-147">You can choose to see only incidents that have mapped to multiple categories  and can thus potentially cause more damage.</span></span> |
| <span data-ttu-id="bd1db-148">Plusieurs sources de service</span><span class="sxs-lookup"><span data-stu-id="bd1db-148">Multiple service sources</span></span>  | <span data-ttu-id="bd1db-149">Filtrez pour voir uniquement les incidents qui contiennent des alertes provenant de différentes sources (Microsoft Defender pour endpoint, Microsoft Cloud App Security, Microsoft Defender pour l'identité, Microsoft Defender pour Office 365).</span><span class="sxs-lookup"><span data-stu-id="bd1db-149">Filter to only see incidents that contain alerts from different sources (Microsoft Defender for Endpoint, Microsoft Cloud App Security, Microsoft Defender for Identity, Microsoft Defender for Office 365).</span></span> |
| <span data-ttu-id="bd1db-150">Plateforme du système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="bd1db-150">OS platform</span></span> | <span data-ttu-id="bd1db-151">Limitez l'affichage de la file d'attente des incidents par système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="bd1db-151">Limit the incident queue view by operating system.</span></span> |
| <span data-ttu-id="bd1db-152">Sources de service</span><span class="sxs-lookup"><span data-stu-id="bd1db-152">Service sources</span></span> | <span data-ttu-id="bd1db-153">En sélectionnant une source spécifique, vous pouvez vous concentrer sur les incidents qui contiennent au moins une alerte de la source choisie.</span><span class="sxs-lookup"><span data-stu-id="bd1db-153">By choosing a specific source, you can focus on incidents that contain at least one alert from that chosen source.</span></span> |
| <span data-ttu-id="bd1db-154">Severity</span><span class="sxs-lookup"><span data-stu-id="bd1db-154">Severity</span></span> | <span data-ttu-id="bd1db-155">La gravité d'un incident indique l'impact qu'il peut avoir sur vos ressources.</span><span class="sxs-lookup"><span data-stu-id="bd1db-155">The severity of an incident is indicative of the impact it can have on your assets.</span></span> <span data-ttu-id="bd1db-156">Plus la gravité est élevée, plus l'impact est important et nécessite généralement l'attention la plus immédiate.</span><span class="sxs-lookup"><span data-stu-id="bd1db-156">The higher the severity, the bigger the impact and typically requires the most immediate attention.</span></span> |
| <span data-ttu-id="bd1db-157">Statut</span><span class="sxs-lookup"><span data-stu-id="bd1db-157">Status</span></span> | <span data-ttu-id="bd1db-158">Vous pouvez choisir de limiter la liste des incidents affichés en fonction de leur état pour identifier ceux qui sont actifs ou résolus.</span><span class="sxs-lookup"><span data-stu-id="bd1db-158">You can choose to limit the list of incidents shown based on their status to see which ones are active or resolved.</span></span> |
|||

## <a name="incident-response-workflow"></a><span data-ttu-id="bd1db-159">Flux de travail de réponse aux incidents</span><span class="sxs-lookup"><span data-stu-id="bd1db-159">Incident response workflow</span></span>

<span data-ttu-id="bd1db-160">Voici le flux de travail classique pour répondre aux incidents :</span><span class="sxs-lookup"><span data-stu-id="bd1db-160">Here's the typical workflow for responding to incidents:</span></span>

1. <span data-ttu-id="bd1db-161">Identifier et trier les incidents les plus prioritaires pour l'examen et la résolution.</span><span class="sxs-lookup"><span data-stu-id="bd1db-161">Identify and triage the highest priority incidents for investigation and resolution.</span></span>
2. <span data-ttu-id="bd1db-162">Pour chaque incident prioritaire, lancez une [enquête](investigate-incidents.md):</span><span class="sxs-lookup"><span data-stu-id="bd1db-162">For each high-priority incident, begin an [investigation](investigate-incidents.md):</span></span>

   <span data-ttu-id="bd1db-163">a.</span><span class="sxs-lookup"><span data-stu-id="bd1db-163">a.</span></span> <span data-ttu-id="bd1db-164">Affichez le résumé de l'incident pour comprendre sa portée et sa gravité, ainsi que les entités concernées (onglet **Résumé).**</span><span class="sxs-lookup"><span data-stu-id="bd1db-164">View the summary of the incident to understand it's scope and severity and what entities are affected (the **Summary** tab).</span></span>

   <span data-ttu-id="bd1db-165">b.</span><span class="sxs-lookup"><span data-stu-id="bd1db-165">b.</span></span> <span data-ttu-id="bd1db-166">Commencez à regarder les alertes pour comprendre leur origine, leur étendue et leur gravité (onglet **Alertes).**</span><span class="sxs-lookup"><span data-stu-id="bd1db-166">Begin looking at the alerts to understand their origin, scope, and severity (the **Alerts** tab).</span></span>

   <span data-ttu-id="bd1db-167">c.</span><span class="sxs-lookup"><span data-stu-id="bd1db-167">c.</span></span> <span data-ttu-id="bd1db-168">Si nécessaire, rassemblez des informations sur les appareils, les utilisateurs et les boîtes aux lettres touchés (onglets **Appareils,** Utilisateurs et Boîtes **aux lettres).**</span><span class="sxs-lookup"><span data-stu-id="bd1db-168">As needed, gather information on impacted devices, users, and mailboxes (the **Devices**, **Users**, and **Mailboxes** tabs).</span></span>

   <span data-ttu-id="bd1db-169">d.</span><span class="sxs-lookup"><span data-stu-id="bd1db-169">d.</span></span> <span data-ttu-id="bd1db-170">Découvrez comment Microsoft 365 Defender a résolu automatiquement certaines alertes (onglet **Enquêtes).**</span><span class="sxs-lookup"><span data-stu-id="bd1db-170">See how Microsoft 365 Defender has automatically resolved some alerts (the **Investigations** tab).</span></span>
   
   <span data-ttu-id="bd1db-171">e.</span><span class="sxs-lookup"><span data-stu-id="bd1db-171">e.</span></span> <span data-ttu-id="bd1db-172">Si nécessaire, utilisez les informations du jeu de données pour l'incident pour plus d'informations (onglet Preuve **et** réponse).</span><span class="sxs-lookup"><span data-stu-id="bd1db-172">As needed, use information in the data set for the incident for more information (the **Evidence and Response** tab).</span></span>

   <span data-ttu-id="bd1db-173">À mesure que vous examinez, vous devez être concerné par :</span><span class="sxs-lookup"><span data-stu-id="bd1db-173">As you investigate, you should be concerned with:</span></span>

   - <span data-ttu-id="bd1db-174">Containment : réduction de tout impact supplémentaire sur votre client.</span><span class="sxs-lookup"><span data-stu-id="bd1db-174">Containment: Reducing any additional impact on your tenant.</span></span>
   - <span data-ttu-id="bd1db-175">Éradication : suppression de la menace de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bd1db-175">Eradication: Removing the security threat.</span></span>
   - <span data-ttu-id="bd1db-176">Récupération : restauration des ressources de votre client à l'état dans celui où elles se sont trouver avant l'incident.</span><span class="sxs-lookup"><span data-stu-id="bd1db-176">Recovery: Restoring your tenant resources to the state they were in before the incident.</span></span>

3. <span data-ttu-id="bd1db-177">Après avoir résolu l'incident, prenez le temps de :</span><span class="sxs-lookup"><span data-stu-id="bd1db-177">After you resolve the incident, take the time to:</span></span>

   - <span data-ttu-id="bd1db-178">Comprendre le type de l'attaque et son impact.</span><span class="sxs-lookup"><span data-stu-id="bd1db-178">Understand the type of the attack and its impact.</span></span>
   - <span data-ttu-id="bd1db-179">Recherchez une tendance d'attaques de sécurité dans la communauté de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="bd1db-179">Research the attack in the security community for a security attack trend.</span></span>
   - <span data-ttu-id="bd1db-180">Rappelez-vous du flux de travail que vous avez utilisé pour résoudre l'incident et mettre à jour vos flux de travail et playbooks standard selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="bd1db-180">Recall the workflow you used to resolve the incident and update your standard workflows and playbooks as needed.</span></span>
   - <span data-ttu-id="bd1db-181">Déterminez si des modifications de votre posture de sécurité sont nécessaires et prenez les mesures nécessaires pour les implémenter.</span><span class="sxs-lookup"><span data-stu-id="bd1db-181">Determine whether changes in your security posture are needed and take the steps to implement them.</span></span>

<span data-ttu-id="bd1db-182">Voici un résumé du processus de base.</span><span class="sxs-lookup"><span data-stu-id="bd1db-182">Here's a summary of the basic process.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents-process.png" alt-text="Processus de base pour l'examen des incidents":::

## <a name="next-step"></a><span data-ttu-id="bd1db-184">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="bd1db-184">Next step</span></span>

<span data-ttu-id="bd1db-185">Une fois que vous avez déterminé quel incident nécessite la priorité la plus élevée, sélectionnez-le et commencez votre [enquête.](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="bd1db-185">After you've determined which incident requires the highest priority, select it and begin your [investigation](investigate-incidents.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bd1db-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd1db-186">See also</span></span>
- [<span data-ttu-id="bd1db-187">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="bd1db-187">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="bd1db-188">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="bd1db-188">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="bd1db-189">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="bd1db-189">Manage incidents</span></span>](manage-incidents.md)
