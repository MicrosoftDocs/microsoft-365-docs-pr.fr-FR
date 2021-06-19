---
title: Incidents dans Microsoft 365 Defender
description: Examinez les incidents rencontrés sur les appareils, les utilisateurs et les boîtes aux lettres dans Microsoft 365 Defender portail.
keywords: incidents, alertes, examiner, analyser, réponse, corrélation, attaque, ordinateurs, appareils, utilisateurs, identités, identité, boîte aux lettres, courrier électronique, 365, microsoft, m365, réponse aux incidents, cyber-attaque
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
ms.openlocfilehash: 3dac22afb074a58ea2afdf842a9a62c6cee77dcc
ms.sourcegitcommit: bc64d9f619259bd0a94e43a9010aae5cffb4d6c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53022780"
---
# <a name="incidents-in-microsoft-365-defender"></a><span data-ttu-id="6998d-104">Incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6998d-104">Incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="6998d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6998d-105">**Applies to:**</span></span>
- <span data-ttu-id="6998d-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6998d-106">Microsoft 365 Defender</span></span>

> <span data-ttu-id="6998d-107">Vous voulez essayer Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="6998d-107">Want to experience Microsoft 365 Defender?</span></span> <span data-ttu-id="6998d-108">Vous pouvez [l’évaluer dans un environnement de laboratoire](m365d-evaluation.md?ocid=cx-docs-MTPtriallab) ou [exécuter votre projet pilote en production](m365d-pilot.md?ocid=cx-evalpilot).</span><span class="sxs-lookup"><span data-stu-id="6998d-108">You can [evaluate it in a lab environment](m365d-evaluation.md?ocid=cx-docs-MTPtriallab) or [run your pilot project in production](m365d-pilot.md?ocid=cx-evalpilot).</span></span>
>

<span data-ttu-id="6998d-109">Un incident dans Microsoft 365 Defender est une collection d’alertes corrélées et de données associées qui constitue l’histoire d’une attaque.</span><span class="sxs-lookup"><span data-stu-id="6998d-109">An incident in Microsoft 365 Defender is a collection of correlated alerts and associated data that make up the story of an attack.</span></span> 

<span data-ttu-id="6998d-110">Microsoft 365 et applications créent des alertes lorsqu’ils détectent un événement ou une activité suspect ou malveillant.</span><span class="sxs-lookup"><span data-stu-id="6998d-110">Microsoft 365 services and apps create alerts when they detect a suspicious or malicious event or activity.</span></span> <span data-ttu-id="6998d-111">Les alertes individuelles fournissent des indices précieux sur une attaque terminée ou en cours.</span><span class="sxs-lookup"><span data-stu-id="6998d-111">Individual alerts provide valuable clues about a completed or ongoing attack.</span></span> <span data-ttu-id="6998d-112">Toutefois, les attaques utilisent généralement différentes techniques pour différents types d’entités, telles que les appareils, les utilisateurs et les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6998d-112">However, attacks typically employ various techniques against different types of entities, such as devices, users, and mailboxes.</span></span> <span data-ttu-id="6998d-113">Le résultat est plusieurs alertes pour plusieurs entités dans votre client.</span><span class="sxs-lookup"><span data-stu-id="6998d-113">The result is multiple alerts for multiple entities in your tenant.</span></span> 

<span data-ttu-id="6998d-114">Étant donné que l’agrégation des alertes individuelles pour obtenir des informations sur une attaque peut être complexe et chronophage, Microsoft 365 Defender regroupe automatiquement les alertes et leurs informations associées dans un incident.</span><span class="sxs-lookup"><span data-stu-id="6998d-114">Because piecing the individual alerts together to gain insight into an attack can be challenging and time-consuming, Microsoft 365 Defender automatically aggregates the alerts and their associated information into an incident.</span></span>

:::image type="content" source="../../media/incidents-overview/incidents.png" alt-text="Comment Microsoft 365 Defender des événements d’entités dans un incident":::

<span data-ttu-id="6998d-116">Regardez cette courte vue d’ensemble des incidents Microsoft 365 Defender (4 minutes).</span><span class="sxs-lookup"><span data-stu-id="6998d-116">Watch this short overview of incidents in Microsoft 365 Defender (4 minutes).</span></span>

<br>

>[!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Bzwz?]

<span data-ttu-id="6998d-117">Le regroupement d’alertes associées dans un incident vous offre une vue complète d’une attaque.</span><span class="sxs-lookup"><span data-stu-id="6998d-117">Grouping related alerts into an incident gives you a comprehensive view of an attack.</span></span> <span data-ttu-id="6998d-118">Par exemple, vous pouvez voir :</span><span class="sxs-lookup"><span data-stu-id="6998d-118">For example, you can see:</span></span>

- <span data-ttu-id="6998d-119">Point de départ de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="6998d-119">Where the attack started.</span></span>
- <span data-ttu-id="6998d-120">Quelles tactiques ont été utilisées .</span><span class="sxs-lookup"><span data-stu-id="6998d-120">What tactics were used.</span></span>
- <span data-ttu-id="6998d-121">Jusqu’où l’attaque est passée dans votre client.</span><span class="sxs-lookup"><span data-stu-id="6998d-121">How far the attack has gone into your tenant.</span></span>
- <span data-ttu-id="6998d-122">Étendue de l’attaque, telle que le nombre d’appareils, d’utilisateurs et de boîtes aux lettres qui ont été touchés.</span><span class="sxs-lookup"><span data-stu-id="6998d-122">The scope of the attack, such as how many devices, users, and mailboxes were impacted.</span></span> 
- <span data-ttu-id="6998d-123">Toutes les données associées à l’attaque.</span><span class="sxs-lookup"><span data-stu-id="6998d-123">All of the data associated with the attack.</span></span>

<span data-ttu-id="6998d-124">Si [elle est activée,](m365d-enable.md)Microsoft 365 Defender [peuvent automatiquement](m365d-autoir.md) examiner et résoudre les alertes par le biais de l’automatisation et de l’intelligence artificielle.</span><span class="sxs-lookup"><span data-stu-id="6998d-124">If [enabled](m365d-enable.md), Microsoft 365 Defender can [automatically investigate and resolve](m365d-autoir.md) alerts through automation and artificial intelligence.</span></span> <span data-ttu-id="6998d-125">Vous pouvez également effectuer des étapes de correction supplémentaires pour résoudre l’attaque.</span><span class="sxs-lookup"><span data-stu-id="6998d-125">You can also perform additional remediation steps to resolve the attack.</span></span> 

## <a name="incidents-and-alerts-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="6998d-126">Incidents et alertes dans le portail Microsoft 365 Defender web</span><span class="sxs-lookup"><span data-stu-id="6998d-126">Incidents and alerts in the Microsoft 365 Defender portal</span></span>

<span data-ttu-id="6998d-127">Vous gérez les incidents à partir **d’incidents & alertes** > incidents sur le lancement rapide du portail Microsoft 365 Defender ([security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="6998d-127">You manage incidents from **Incidents & alerts > Incidents** on the quick launch of the Microsoft 365 Defender portal ([security.microsoft.com](https://security.microsoft.com)).</span></span> <span data-ttu-id="6998d-128">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="6998d-128">Here's an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents.png" alt-text="Page Incidents dans le portail Microsoft 365 Defender web":::

<span data-ttu-id="6998d-130">La sélection d’un nom d’incident affiche un résumé de l’incident et donne accès aux onglets avec des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6998d-130">Selecting an incident name displays a summary of the incident and provides access to tabs with additional information.</span></span>

:::image type="content" source="../../media/incidents-overview/incidents-ss-incident-summary.png" alt-text="Exemple de page Résumé d’un incident dans le portail Microsoft 365 Defender web":::

<span data-ttu-id="6998d-132">Les onglets supplémentaires pour un incident sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6998d-132">The additional tabs for an incident are:</span></span>

- <span data-ttu-id="6998d-133">Alertes</span><span class="sxs-lookup"><span data-stu-id="6998d-133">Alerts</span></span> 

  <span data-ttu-id="6998d-134">Toutes les alertes liées à l’incident et leurs informations.</span><span class="sxs-lookup"><span data-stu-id="6998d-134">All the alerts related to the incident and their information.</span></span>

- <span data-ttu-id="6998d-135">Appareils</span><span class="sxs-lookup"><span data-stu-id="6998d-135">Devices</span></span>

  <span data-ttu-id="6998d-136">Tous les appareils identifiés comme faisant partie ou liés à l’incident.</span><span class="sxs-lookup"><span data-stu-id="6998d-136">All the devices that have been identified to be part of or related to the incident.</span></span>

- <span data-ttu-id="6998d-137">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6998d-137">Users</span></span>

  <span data-ttu-id="6998d-138">Tous les utilisateurs identifiés comme faisant partie ou associés à l’incident.</span><span class="sxs-lookup"><span data-stu-id="6998d-138">All the users that have been identified to be part of or related to the incident.</span></span>

- <span data-ttu-id="6998d-139">Boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="6998d-139">Mailboxes</span></span>

  <span data-ttu-id="6998d-140">Toutes les boîtes aux lettres identifiées comme faisant partie ou liées à l’incident.</span><span class="sxs-lookup"><span data-stu-id="6998d-140">All the mailboxes that have been identified to be part of or related to the incident.</span></span>

- <span data-ttu-id="6998d-141">Examens</span><span class="sxs-lookup"><span data-stu-id="6998d-141">Investigations</span></span>

  <span data-ttu-id="6998d-142">Toutes les [enquêtes automatisées](m365d-autoir.md) déclenchées par des alertes dans l’incident.</span><span class="sxs-lookup"><span data-stu-id="6998d-142">All the [automated investigations](m365d-autoir.md) triggered by alerts in the incident.</span></span>

- <span data-ttu-id="6998d-143">Preuve et réponse</span><span class="sxs-lookup"><span data-stu-id="6998d-143">Evidence and Response</span></span>

  <span data-ttu-id="6998d-144">Tous les événements pris en charge et entités suspectes dans les alertes dans l’incident.</span><span class="sxs-lookup"><span data-stu-id="6998d-144">All the supported events and suspicious entities in the alerts in the incident.</span></span>

- <span data-ttu-id="6998d-145">Graph (en prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="6998d-145">Graph (in preview)</span></span>

  <span data-ttu-id="6998d-146">Figure montrant la connexion des alertes aux biens touchés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6998d-146">A figure showing the connection of alerts to the impacted assets in your organization.</span></span>

<span data-ttu-id="6998d-147">Voici la relation entre un incident et ses données et les onglets d’un incident dans le Microsoft 365 Defender web.</span><span class="sxs-lookup"><span data-stu-id="6998d-147">Here's the relationship between an incident and its data and the tabs of an incident in the Microsoft 365 Defender portal.</span></span>

:::image type="content" source="../../media/incidents-overview/incidents-security-center.png" alt-text="Relation d’un incident et de ses données avec les onglets d’un incident dans le portail Microsoft 365 Defender web":::

## <a name="example-incident-response-workflow-for-microsoft-365-defender"></a><span data-ttu-id="6998d-149">Exemple de flux de travail de réponse aux incidents pour Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6998d-149">Example incident response workflow for Microsoft 365 Defender</span></span>

<span data-ttu-id="6998d-150">Voici un exemple de flux de travail pour répondre aux incidents dans Microsoft 365 avec le portail Microsoft 365 Defender web.</span><span class="sxs-lookup"><span data-stu-id="6998d-150">Here's an example workflow for responding to incidents in Microsoft 365 with the Microsoft 365 Defender portal.</span></span>

:::image type="content" source="../../media/incidents-overview/incidents-example-workflow.png" alt-text="Exemple de flux de travail de réponse aux incidents pour Microsoft 365":::

<span data-ttu-id="6998d-152">Identifiez régulièrement les incidents les plus prioritaires pour l’analyse et la résolution dans la file d’attente des incidents et préparez-les à répondre.</span><span class="sxs-lookup"><span data-stu-id="6998d-152">On an ongoing basis, identify the highest priority incidents for analysis and resolution in the incident queue and get them ready for response.</span></span> <span data-ttu-id="6998d-153">Il s’agit d’une combinaison de :</span><span class="sxs-lookup"><span data-stu-id="6998d-153">This is a combination of:</span></span>

- <span data-ttu-id="6998d-154">[Tri pour](incident-queue.md) déterminer les incidents les plus prioritaires via le filtrage et le tri de la file d’attente d’incidents.</span><span class="sxs-lookup"><span data-stu-id="6998d-154">[Triaging](incident-queue.md) to determining the highest priority incidents through filtering and sorting of the incident queue.</span></span>
- <span data-ttu-id="6998d-155">[Gestion](manage-incidents.md) des incidents en modifiant leur titre, en les attribuant à un analyste et en ajoutant des balises et des commentaires.</span><span class="sxs-lookup"><span data-stu-id="6998d-155">[Managing](manage-incidents.md) incidents by modifying their title, assigning them to an analyst, and adding tags and comments.</span></span>

1. <span data-ttu-id="6998d-156">Pour chaque incident, lancez une analyse et une analyse d’attaque et [d’alerte](investigate-incidents.md):</span><span class="sxs-lookup"><span data-stu-id="6998d-156">For each incident, begin an [attack and alert investigation and analysis](investigate-incidents.md):</span></span>
 
   1. <span data-ttu-id="6998d-157">Affichez le résumé de l’incident pour comprendre sa portée et sa gravité, ainsi que les entités concernées (onglet **Résumé).**</span><span class="sxs-lookup"><span data-stu-id="6998d-157">View the summary of the incident to understand it's scope and severity and what entities are affected (the **Summary** tab).</span></span>

   1. <span data-ttu-id="6998d-158">Commencez à analyser les alertes pour comprendre leur origine, leur étendue et leur gravité (onglet **Alertes).**</span><span class="sxs-lookup"><span data-stu-id="6998d-158">Begin analyzing the alerts to understand their origin, scope, and severity (the **Alerts** tab).</span></span>

   1. <span data-ttu-id="6998d-159">Si nécessaire, rassemblez des informations sur les appareils, les utilisateurs et les boîtes aux lettres touchés (onglets **Appareils,** Utilisateurs et Boîtes **aux lettres).**</span><span class="sxs-lookup"><span data-stu-id="6998d-159">As needed, gather information on impacted devices, users, and mailboxes (the **Devices**, **Users**, and **Mailboxes** tabs).</span></span>

   1. <span data-ttu-id="6998d-160">Découvrez comment Microsoft 365 Defender [a automatiquement résolu certaines alertes](m365d-autoir.md) (onglet **Enquêtes).**</span><span class="sxs-lookup"><span data-stu-id="6998d-160">See how Microsoft 365 Defender has [automatically resolved some alerts](m365d-autoir.md) (the **Investigations** tab).</span></span>
   
   1. <span data-ttu-id="6998d-161">Si nécessaire, utilisez les informations du jeu de données pour l’incident pour plus d’informations (onglet Preuve **et** réponse).</span><span class="sxs-lookup"><span data-stu-id="6998d-161">As needed, use information in the data set for the incident for more information (the **Evidence and Response** tab).</span></span>

2. <span data-ttu-id="6998d-162">Après ou pendant votre analyse, effectuez un contenu pour réduire tout impact supplémentaire de l’attaque et de l’éradication de la menace de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6998d-162">After or during your analysis, perform containment to reduce any additional impact of the attack and eradication of the security threat.</span></span>

3. <span data-ttu-id="6998d-163">Dans la mesure du possible, récupérez à partir de l’attaque en restaurant les ressources de votre client à l’état où elles se sont trouver avant l’incident.</span><span class="sxs-lookup"><span data-stu-id="6998d-163">As much as possible, recover from the attack by restoring your tenant resources to the state they were in before the incident.</span></span>

4. <span data-ttu-id="6998d-164">[Résolvez](manage-incidents.md#resolve-an-incident) l’incident et prenez le temps d’apprendre après l’incident pour :</span><span class="sxs-lookup"><span data-stu-id="6998d-164">[Resolve](manage-incidents.md#resolve-an-incident) the incident and take time for post-incident learning to:</span></span>

   - <span data-ttu-id="6998d-165">Comprendre le type de l’attaque et son impact.</span><span class="sxs-lookup"><span data-stu-id="6998d-165">Understand the type of the attack and its impact.</span></span>
   - <span data-ttu-id="6998d-166">Recherchez une tendance des attaques de sécurité dans [l’analyse](threat-analytics.md) des menaces et la communauté de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6998d-166">Research the attack in [Threat Analytics](threat-analytics.md) and the security community for a security attack trend.</span></span>
   - <span data-ttu-id="6998d-167">Rappelez-vous du flux de travail que vous avez utilisé pour résoudre l’incident et mettre à jour vos flux de travail, processus, stratégies et playbooks standard si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6998d-167">Recall the workflow you used to resolve the incident and update your standard workflows, processes, policies, and playbooks as needed.</span></span>
   - <span data-ttu-id="6998d-168">Déterminez si des modifications sont nécessaires dans votre configuration de sécurité et implémentez-les.</span><span class="sxs-lookup"><span data-stu-id="6998d-168">Determine whether changes in your security configuration are needed and implement them.</span></span>

<span data-ttu-id="6998d-169">Si vous débutez dans l’analyse de la sécurité, consultez [l’introduction](incidents-overview.md) à la réponse à votre premier incident pour plus d’informations et pour passer au travers d’un exemple d’incident.</span><span class="sxs-lookup"><span data-stu-id="6998d-169">If you are new to security analysis, see the [introduction to responding to your first incident](incidents-overview.md) for additional information and to step through an example incident.</span></span>

## <a name="example-security-operations-for-microsoft-365-defender"></a><span data-ttu-id="6998d-170">Exemples d’opérations de sécurité pour Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6998d-170">Example security operations for Microsoft 365 Defender</span></span>

<span data-ttu-id="6998d-171">Voici un exemple d’opérations de sécurité pour Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="6998d-171">Here's an example of security operations for Microsoft 365 Defender.</span></span>

:::image type="content" source="../../media/incidents-overview/incidents-example-operations.png" alt-text="Exemple d’opérations de sécurité pour Microsoft 365 Defender":::

<span data-ttu-id="6998d-173">Les tâches quotidiennes peuvent inclure les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="6998d-173">Daily tasks can include:</span></span>

- <span data-ttu-id="6998d-174">[Gestion des](manage-incidents.md) incidents</span><span class="sxs-lookup"><span data-stu-id="6998d-174">[Managing](manage-incidents.md) incidents</span></span>
- <span data-ttu-id="6998d-175">Examen des actions [d’investigation et de réponse automatisées (AIR)](m365d-action-center.md) dans le centre de gestion des actions</span><span class="sxs-lookup"><span data-stu-id="6998d-175">Reviewing [automated investigation and response (AIR)](m365d-action-center.md) actions in the Action center</span></span>
- <span data-ttu-id="6998d-176">Examen de la dernière [analyse des menaces](threat-analytics.md)</span><span class="sxs-lookup"><span data-stu-id="6998d-176">Reviewing the latest [Threat Analytics](threat-analytics.md)</span></span>
- <span data-ttu-id="6998d-177">[Réponse aux](investigate-incidents.md) incidents</span><span class="sxs-lookup"><span data-stu-id="6998d-177">[Responding](investigate-incidents.md) to incidents</span></span>

<span data-ttu-id="6998d-178">Les tâches mensuelles peuvent inclure les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="6998d-178">Monthly tasks can include:</span></span>

- <span data-ttu-id="6998d-179">Examen des [paramètres AIR](m365d-configure-auto-investigation-response.md)</span><span class="sxs-lookup"><span data-stu-id="6998d-179">Reviewing [AIR settings](m365d-configure-auto-investigation-response.md)</span></span>
- <span data-ttu-id="6998d-180">Examen de [la gestion des niveaux de sécurité](microsoft-secure-score-improvement-actions.md) et & des [vulnérabilités](../defender-endpoint/next-gen-threat-and-vuln-mgt.md)</span><span class="sxs-lookup"><span data-stu-id="6998d-180">Reviewing [Secure Score](microsoft-secure-score-improvement-actions.md) and [Threat & Vulnerability Management](../defender-endpoint/next-gen-threat-and-vuln-mgt.md)</span></span>
- <span data-ttu-id="6998d-181">Rapports à votre chaîne de gestion de la sécurité informatique</span><span class="sxs-lookup"><span data-stu-id="6998d-181">Reporting to your IT security management chain</span></span>

<span data-ttu-id="6998d-182">Les tâches trimestrielles peuvent inclure un rapport et un briefing des résultats de sécurité au directeur de la sécurité des informations (CISO).</span><span class="sxs-lookup"><span data-stu-id="6998d-182">Quarterly tasks can include a report and briefing of security results to the Chief Information Security Officer (CISO).</span></span>

<span data-ttu-id="6998d-183">Les tâches annuelles peuvent inclure la conduite d’un incident majeur ou d’un exercice de violation pour tester votre personnel, vos systèmes et vos processus.</span><span class="sxs-lookup"><span data-stu-id="6998d-183">Annual tasks can include conducting a major incident or breach exercise to test your staff, systems, and processes.</span></span> 

<span data-ttu-id="6998d-184">Les tâches quotidiennes, mensuelles, trimestrielles et annuelles peuvent être utilisées pour mettre à jour ou affiner des processus, des stratégies et des configurations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6998d-184">Daily, monthly, quarterly, and annual tasks can be used to update or refine processes, policies, and security configurations.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6998d-185">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="6998d-185">Next steps</span></span>

<span data-ttu-id="6998d-186">**Si vous êtes nouveau dans l’analyse** de la sécurité et la réponse aux incidents :</span><span class="sxs-lookup"><span data-stu-id="6998d-186">**If you are new** to security analysis and incident response:</span></span>

- <span data-ttu-id="6998d-187">Consultez la procédure pas à pas Répondre à votre premier [incident](first-incident-overview.md) pour obtenir une visite guidée d’un processus classique d’analyse, de correction et de révision post-incident dans le portail Microsoft 365 Defender avec un exemple d’attaque.</span><span class="sxs-lookup"><span data-stu-id="6998d-187">See the [Respond to your first incident walkthrough](first-incident-overview.md) to get a guided tour of a typical process of analysis, remediation, and post-incident review in the Microsoft 365 Defender portal with an example of an attack.</span></span>

<span data-ttu-id="6998d-188">**Si vous avez de l’expérience en** matière d’analyse de sécurité et de réponse aux incidents :</span><span class="sxs-lookup"><span data-stu-id="6998d-188">**If you have experience** with security analysis and incident response:</span></span>

- <span data-ttu-id="6998d-189">Commencer avec la file d’attente des incidents à partir de la page **Incidents** du portail Microsoft 365 Defender web.</span><span class="sxs-lookup"><span data-stu-id="6998d-189">Get started with the incident queue from the **Incidents** page of the Microsoft 365 Defender portal.</span></span> <span data-ttu-id="6998d-190">Ici, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="6998d-190">From here, you can:</span></span>

  - <span data-ttu-id="6998d-191">Voir quels incidents doivent [être](incident-queue.md) hiérarchisés en fonction de la gravité et d’autres facteurs.</span><span class="sxs-lookup"><span data-stu-id="6998d-191">See which incidents should be [prioritized](incident-queue.md) based on severity and other factors.</span></span> 

  - <span data-ttu-id="6998d-192">[Gérer les incidents,](manage-incidents.md)ce qui inclut le changement de nom, l’affectation, la classification et l’ajout de balises et de commentaires en fonction de votre flux de travail de gestion des incidents.</span><span class="sxs-lookup"><span data-stu-id="6998d-192">[Manage incidents](manage-incidents.md), which includes renaming, assignment, classifying, and adding tags and comments based on your incident management workflow.</span></span>

  - <span data-ttu-id="6998d-193">Effectuer [des examens](investigate-incidents.md) des incidents.</span><span class="sxs-lookup"><span data-stu-id="6998d-193">Perform [investigations](investigate-incidents.md) of incidents.</span></span>

- <span data-ttu-id="6998d-194">Consultez ces manuels de réponse aux incidents pour obtenir des [instructions détaillées](/security/compass/incident-response-playbooks) sur le hameçonnage, la pulvérisation de mots de passe et les attaques d’octroi de consentement d’application.</span><span class="sxs-lookup"><span data-stu-id="6998d-194">See these [incident response playbooks](/security/compass/incident-response-playbooks) for detailed guidance for phishing, password spray, and app consent grant attacks.</span></span>

