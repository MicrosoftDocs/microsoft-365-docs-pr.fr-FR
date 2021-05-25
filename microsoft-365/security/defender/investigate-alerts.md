---
title: Examiner les alertes dans Microsoft 365 Defender
description: Examinez les alertes visibles sur les appareils, les utilisateurs et les boîtes aux lettres.
keywords: incidents, alertes, examiner, analyser, réponse, corrélation, attaque, ordinateurs, appareils, utilisateurs, identités, identité, boîte aux lettres, courrier électronique, 365, microsoft, m365
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
ms.openlocfilehash: 6a34269c414f59d40c9160d5728159ed9cddf976
ms.sourcegitcommit: 07e536f1a6e335f114da55048844e4a866fe731b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "52651347"
---
# <a name="investigate-alerts-in-microsoft-365-defender"></a><span data-ttu-id="3a7fa-104">Examiner les alertes dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3a7fa-104">Investigate alerts in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="3a7fa-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3a7fa-105">**Applies to:**</span></span>
- <span data-ttu-id="3a7fa-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3a7fa-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="3a7fa-107">Les alertes sont la base de tous les incidents et indiquent l’occurrence d’événements malveillants ou suspects dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-107">Alerts are the basis of all incidents and indicate the occurrence of malicious or suspicious events in your environment.</span></span> <span data-ttu-id="3a7fa-108">Les alertes font généralement partie d’une attaque plus large et fournissent des indices sur un incident.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-108">Alerts are typically part of a broader attack and provide clues about an incident.</span></span>

<span data-ttu-id="3a7fa-109">Dans Microsoft 365 Defender, les alertes associées sont regroupées pour former des [incidents.](incidents-overview.md)</span><span class="sxs-lookup"><span data-stu-id="3a7fa-109">In Microsoft 365 Defender, related alerts are aggregated together to form [incidents](incidents-overview.md).</span></span> <span data-ttu-id="3a7fa-110">Les incidents fournissent toujours le contexte plus large d’une attaque, mais l’analyse des alertes peut être utile lorsque des analyses plus approfondies sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-110">Incidents will always provide the broader context of an attack, however, analyzing alerts can be valuable when deeper analysis is required.</span></span> 

<span data-ttu-id="3a7fa-111">La **file d’attente Alertes** affiche l’ensemble actuel des alertes.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-111">The **Alerts queue** shows the current set of alerts.</span></span> <span data-ttu-id="3a7fa-112">Vous arrivez à la file d’attente des alertes à partir **d’incidents & alertes** > alertes sur le lancement rapide du centre de sécurité Microsoft 365 ([security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="3a7fa-112">You get to the alerts queue from **Incidents & alerts > Alerts** on the quick launch of the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)).</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-queue.png" alt-text="Exemple de file d’attente des alertes":::

<span data-ttu-id="3a7fa-114">Des alertes provenant de différentes solutions de sécurité Microsoft telles que Microsoft Defender pour endpoint, Microsoft Defender pour Office 365 et Microsoft 365 Defender apparaissent ici.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-114">Alerts from different Microsoft security solutions like Microsoft Defender for Endpoint, Microsoft Defender for Office 365, and Microsoft 365 Defender appear here.</span></span>

<span data-ttu-id="3a7fa-115">Par défaut, la file d’attente des alertes dans Microsoft 365 centre de sécurité affiche les alertes nouvelles et en cours depuis les 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-115">By default, the alerts queue in the Microsoft 365 security center displays the new and in progress alerts from the last 30 days.</span></span> <span data-ttu-id="3a7fa-116">L’alerte la plus récente se trouve en haut de la liste, ce qui vous permet de la voir en premier.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-116">The most recent alert is at the top of the list so you can see it first.</span></span> 

<span data-ttu-id="3a7fa-117">Dans la file d’attente des alertes par défaut, vous pouvez sélectionner **Filtres** pour voir un volet **Filtres,** à partir duquel vous pouvez spécifier un sous-ensemble des alertes.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-117">From the default alerts queue, you can select **Filters** to see a **Filters** pane, from which you can specify a subset of the alerts.</span></span> <span data-ttu-id="3a7fa-118">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-118">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-filter.png" alt-text="Exemple de volet de filtres pour la file d’attente d’alertes":::

<span data-ttu-id="3a7fa-120">Vous pouvez filtrer les alertes en fonction de ces critères :</span><span class="sxs-lookup"><span data-stu-id="3a7fa-120">You can filter alerts according to these criteria:</span></span>

- <span data-ttu-id="3a7fa-121">Severity</span><span class="sxs-lookup"><span data-stu-id="3a7fa-121">Severity</span></span>
- <span data-ttu-id="3a7fa-122">Statut</span><span class="sxs-lookup"><span data-stu-id="3a7fa-122">Status</span></span>
- <span data-ttu-id="3a7fa-123">Catégorie</span><span class="sxs-lookup"><span data-stu-id="3a7fa-123">Category</span></span>
- <span data-ttu-id="3a7fa-124">Source de détection</span><span class="sxs-lookup"><span data-stu-id="3a7fa-124">Detection source</span></span>
- <span data-ttu-id="3a7fa-125">Balises</span><span class="sxs-lookup"><span data-stu-id="3a7fa-125">Tags</span></span>
- <span data-ttu-id="3a7fa-126">Stratégie</span><span class="sxs-lookup"><span data-stu-id="3a7fa-126">Policy</span></span>
- <span data-ttu-id="3a7fa-127">Ressources impactées</span><span class="sxs-lookup"><span data-stu-id="3a7fa-127">Impacted assets</span></span>

## <a name="analyze-an-alert"></a><span data-ttu-id="3a7fa-128">Analyser une alerte</span><span class="sxs-lookup"><span data-stu-id="3a7fa-128">Analyze an alert</span></span>

<span data-ttu-id="3a7fa-129">Pour voir la page principale de l’alerte, sélectionnez le nom de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-129">To see the main alert page, select the name of the alert.</span></span> <span data-ttu-id="3a7fa-130">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-130">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-main.png" alt-text="Exemple de page de détails d’une alerte dans le centre de Microsoft 365 de sécurité":::

<span data-ttu-id="3a7fa-132">Vous pouvez également sélectionner l’action Ouvrir la **page d’alerte** principale dans le volet Gérer **les** alertes.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-132">You can also select the **Open the main alert page** action from the **Manage alert** pane.</span></span>

<span data-ttu-id="3a7fa-133">Une page d’alerte se compose des sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a7fa-133">An alert page is composed of these sections:</span></span> 

- <span data-ttu-id="3a7fa-134">Article d’alerte, qui est la chaîne d’événements et d’alertes liés à cette alerte dans l’ordre chronologique</span><span class="sxs-lookup"><span data-stu-id="3a7fa-134">Alert story, which is the chain of events and alerts related to this alert in chronological order</span></span>
- <span data-ttu-id="3a7fa-135">Détails récapitulatifs</span><span class="sxs-lookup"><span data-stu-id="3a7fa-135">Summary details</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-main.png" alt-text="Exemple de page de détails d’une alerte dans le centre de Microsoft 365 de sécurité":::

<span data-ttu-id="3a7fa-137">Dans une page d’alerte, vous pouvez sélectionner les ellipses (**...**) à côté de n’importe quelle entité pour voir les actions disponibles, telles que l’ouverture de la page d’alerte ou la liaison de l’alerte à un autre incident.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-137">Throughout an alert page, you can select the ellipses (**...**) beside any entity to see available actions, such as opening the alert page or linking the alert to another incident.</span></span>

### <a name="analyze-affected-assets"></a><span data-ttu-id="3a7fa-138">Analyser les ressources affectées</span><span class="sxs-lookup"><span data-stu-id="3a7fa-138">Analyze affected assets</span></span>

<span data-ttu-id="3a7fa-139">La section **Actions entreprises** contient une liste des biens concernés, tels que les boîtes aux lettres, les appareils et les utilisateurs affectés par cette alerte.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-139">The **Actions taken** section has a list of impacted assets, such as mailboxes, devices, and users affected by this alert.</span></span> 

<span data-ttu-id="3a7fa-140">Vous pouvez également sélectionner Afficher dans  le centre  **de sécurité** pour afficher l’onglet Historique du centre de Microsoft 365 de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-140">You can also select **View in action center** to view the **History** tab of the **Action center** in the Microsoft 365 security center.</span></span> 

### <a name="trace-an-alerts-role-in-the-alert-story"></a><span data-ttu-id="3a7fa-141">Suivre le rôle d’une alerte dans l’article d’alerte</span><span class="sxs-lookup"><span data-stu-id="3a7fa-141">Trace an alert's role in the alert story</span></span>

<span data-ttu-id="3a7fa-142">L’article d’alerte affiche toutes les ressources ou entités associées à l’alerte dans une arborescence de processus.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-142">The alert story displays all assets or entities related to the alert in a process tree view.</span></span> <span data-ttu-id="3a7fa-143">L’alerte dans le titre est celle qui est sélectionnée lorsque vous vous pointez pour la première fois sur la page de votre alerte sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-143">The alert in the title is the one in focus when you first land on your selected alert's page.</span></span> <span data-ttu-id="3a7fa-144">Les ressources de l’article d’alerte sont ex expandables et peuvent être cliquées.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-144">Assets in the alert story are expandable and clickable.</span></span> <span data-ttu-id="3a7fa-145">Ils fournissent des informations supplémentaires et accélèrent votre réponse en vous permettant d’agir directement dans le contexte de la page d’alerte.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-145">They provide additional information and expedite your response by allowing you to take action right in the context of the alert page.</span></span> 

> [!NOTE]
> <span data-ttu-id="3a7fa-146">La section de l’article sur l’alerte peut contenir plusieurs alertes, avec des alertes supplémentaires liées à la même arborescence d’exécution apparaissant avant ou après l’alerte que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-146">The alert story section may contain more than one alert, with additional alerts related to the same execution tree appearing before or after the alert you've selected.</span></span>

### <a name="view-more-alert-information-on-the-details-page"></a><span data-ttu-id="3a7fa-147">Afficher plus d’informations sur les alertes sur la page de détails</span><span class="sxs-lookup"><span data-stu-id="3a7fa-147">View more alert information on the details page</span></span>

<span data-ttu-id="3a7fa-148">La page de détails affiche les détails de l’alerte sélectionnée, ainsi que les détails et les actions qui y sont associés.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-148">The details page shows the details of the selected alert, with details and actions related to it.</span></span> <span data-ttu-id="3a7fa-149">Si vous sélectionnez l’une des ressources ou entités affectées dans l’article d’alerte, la page de détails change pour fournir des informations contextuelles et des actions pour l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-149">If you select any of the affected assets or entities in the alert story, the details page changes to provide contextual information and actions for the selected object.</span></span>

<span data-ttu-id="3a7fa-150">Une fois que vous avez sélectionné une entité d’intérêt, la page de détails change pour afficher les informations sur le type d’entité sélectionné, les informations historiques lorsqu’elle est disponible et les options d’action sur cette entité directement à partir de la page d’alerte.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-150">Once you've selected an entity of interest, the details page changes to display information about the selected entity type, historic information when it's available, and options to take action on this entity directly from the alert page.</span></span>

## <a name="manage-alerts"></a><span data-ttu-id="3a7fa-151">Gérer des alertes</span><span class="sxs-lookup"><span data-stu-id="3a7fa-151">Manage alerts</span></span>

<span data-ttu-id="3a7fa-152">Pour gérer une alerte, sélectionnez l’alerte dans la file d’attente des alertes sur sa ligne pour voir un volet Gérer **les** alertes.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-152">To manage an alert, select the alert in the alerts queue on its row to see a **Manage alert** pane.</span></span> <span data-ttu-id="3a7fa-153">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-153">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-manage.png" alt-text="Exemple du volet récapitulatif d’une alerte":::

<span data-ttu-id="3a7fa-155">Le **volet Gérer les** alertes vous permet de spécifier :</span><span class="sxs-lookup"><span data-stu-id="3a7fa-155">The **Manage alert** pane allows you to specify:</span></span>

- <span data-ttu-id="3a7fa-156">État de l’alerte (Nouveau, Résolu, En cours).</span><span class="sxs-lookup"><span data-stu-id="3a7fa-156">The alert status (New, Resolved, In progress).</span></span>
- <span data-ttu-id="3a7fa-157">Classification de l’alerte (non définie, alerte True, Fausse alerte).</span><span class="sxs-lookup"><span data-stu-id="3a7fa-157">The alert's classification  (Not set, True alert, False Alert).</span></span>
- <span data-ttu-id="3a7fa-158">Pour la classification en tant qu’alerte réelle, le type de menace pour l’alerte dans le **champ Détermination.**</span><span class="sxs-lookup"><span data-stu-id="3a7fa-158">For the classification as a true alert, the type of threat for the alert in **Determination** field.</span></span>
- <span data-ttu-id="3a7fa-159">Commentaire de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-159">A comment on the alert.</span></span>

> [!NOTE]
> <span data-ttu-id="3a7fa-160">Une façon de gérer les alertes par le biais de l’utilisation de balises.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-160">One way of managing alerts it through the use of tags.</span></span> <span data-ttu-id="3a7fa-161">La fonctionnalité de marquage de Microsoft Defender pour Office 365 est déployée de manière incrémentielle et est actuellement en prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-161">The tagging capability for Microsoft Defender for Office 365 is incrementally being rolled out and is currently in preview.</span></span> <br>
> <span data-ttu-id="3a7fa-162">Actuellement, les noms de balise modifiés sont appliqués uniquement aux alertes créées *après la* mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-162">Currently, modified tag names are only applied to alerts created *after* the update.</span></span> <span data-ttu-id="3a7fa-163">Les alertes qui ont été générées avant la modification ne reflètent pas le nom de balise mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-163">Alerts that were generated before the modification will not reflect the updated tag name.</span></span> 

<span data-ttu-id="3a7fa-164">À partir de ce volet, vous pouvez également effectuer les actions supplémentaires ci-après :</span><span class="sxs-lookup"><span data-stu-id="3a7fa-164">From this pane, you can also perform these additional actions:</span></span> 

- <span data-ttu-id="3a7fa-165">Ouvrir la page principale d’alerte</span><span class="sxs-lookup"><span data-stu-id="3a7fa-165">Open the main alert page</span></span>
- <span data-ttu-id="3a7fa-166">Consulter un expert en menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="3a7fa-166">Consult a Microsoft threat expert</span></span>
- <span data-ttu-id="3a7fa-167">Afficher l’envoi</span><span class="sxs-lookup"><span data-stu-id="3a7fa-167">View submission</span></span>
- <span data-ttu-id="3a7fa-168">Lien vers un autre incident</span><span class="sxs-lookup"><span data-stu-id="3a7fa-168">Link to another incident</span></span>
- <span data-ttu-id="3a7fa-169">Voir l’alerte dans une chronologie</span><span class="sxs-lookup"><span data-stu-id="3a7fa-169">See the alert in a timeline</span></span>
- <span data-ttu-id="3a7fa-170">Créer une règle de suppression</span><span class="sxs-lookup"><span data-stu-id="3a7fa-170">Create a suppression rule</span></span>

<span data-ttu-id="3a7fa-171">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-171">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-actions.png" alt-text="Exemple d’actions sur une alerte dans le centre de Microsoft 365 de sécurité":::

<span data-ttu-id="3a7fa-173">La liste des actions supplémentaires dépend du type d’alerte.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-173">The list of additional actions depends on the type of alert.</span></span>

## <a name="resolve-an-alert"></a><span data-ttu-id="3a7fa-174">Résoudre une alerte</span><span class="sxs-lookup"><span data-stu-id="3a7fa-174">Resolve an alert</span></span>

<span data-ttu-id="3a7fa-175">Une fois que vous avez terminé l’analyse d’une  alerte et qu’elle peut être  résolue, allez dans le volet Gérer l’alerte et marquez l’état de l’alerte comme Résolu et classez-la en tant qu’alerte **False** ou Alerte **True.**</span><span class="sxs-lookup"><span data-stu-id="3a7fa-175">Once you're done analyzing an alert and it can be resolved, go to the **Manage alert** pane for the alert and mark the it status as **Resolved** and classify it as either a **False alert** or **True alert**.</span></span> <span data-ttu-id="3a7fa-176">Pour les alertes vraies, spécifiez le type de menace de l’alerte dans le **champ Détermination.**</span><span class="sxs-lookup"><span data-stu-id="3a7fa-176">For true alerts, specify the alert's threat type in the **Determination** field.</span></span>

<span data-ttu-id="3a7fa-177">La classification des alertes et la spécification de leur détermination permettent d’Microsoft 365 Defender pour fournir plus d’alertes vraies et moins de fausses alertes.</span><span class="sxs-lookup"><span data-stu-id="3a7fa-177">Classifying alerts and specifying their determination helps tune Microsoft 365 Defender to provide more true alerts and less false alerts.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3a7fa-178">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="3a7fa-178">Next steps</span></span>

<span data-ttu-id="3a7fa-179">Si nécessaire pour les incidents in-process, poursuivez votre [enquête.](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="3a7fa-179">As needed for in-process incidents, continue your [investigation](investigate-incidents.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3a7fa-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a7fa-180">See also</span></span>

- [<span data-ttu-id="3a7fa-181">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="3a7fa-181">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="3a7fa-182">Gérer des incidents</span><span class="sxs-lookup"><span data-stu-id="3a7fa-182">Manage incidents</span></span>](manage-incidents.md)
- [<span data-ttu-id="3a7fa-183">Examiner des incidents</span><span class="sxs-lookup"><span data-stu-id="3a7fa-183">Investigate incidents</span></span>](investigate-incidents.md)
