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
ms.openlocfilehash: 4957c92cb95464213cce4a81ded07de166468c73
ms.sourcegitcommit: 82a4d74020cd93ba444006317cfecc178c6d41dc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52689012"
---
# <a name="investigate-alerts-in-microsoft-365-defender"></a><span data-ttu-id="8a12b-104">Examiner les alertes dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8a12b-104">Investigate alerts in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="8a12b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8a12b-105">**Applies to:**</span></span>
- <span data-ttu-id="8a12b-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8a12b-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="8a12b-107">Les alertes sont la base de tous les incidents et indiquent l’occurrence d’événements malveillants ou suspects dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8a12b-107">Alerts are the basis of all incidents and indicate the occurrence of malicious or suspicious events in your environment.</span></span> <span data-ttu-id="8a12b-108">Les alertes font généralement partie d’une attaque plus large et fournissent des indices sur un incident.</span><span class="sxs-lookup"><span data-stu-id="8a12b-108">Alerts are typically part of a broader attack and provide clues about an incident.</span></span>

<span data-ttu-id="8a12b-109">Dans Microsoft 365 Defender, les alertes associées sont regroupées pour former des [incidents.](incidents-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8a12b-109">In Microsoft 365 Defender, related alerts are aggregated together to form [incidents](incidents-overview.md).</span></span> <span data-ttu-id="8a12b-110">Les incidents fournissent toujours le contexte plus large d’une attaque, mais l’analyse des alertes peut être utile lorsque des analyses plus approfondies sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="8a12b-110">Incidents will always provide the broader context of an attack, however, analyzing alerts can be valuable when deeper analysis is required.</span></span> 

<span data-ttu-id="8a12b-111">La **file d’attente Alertes** affiche l’ensemble actuel des alertes.</span><span class="sxs-lookup"><span data-stu-id="8a12b-111">The **Alerts queue** shows the current set of alerts.</span></span> <span data-ttu-id="8a12b-112">Vous arrivez à la file d’attente des alertes à partir **d’incidents & alertes** > alertes sur le lancement rapide du centre de sécurité Microsoft 365 ([security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="8a12b-112">You get to the alerts queue from **Incidents & alerts > Alerts** on the quick launch of the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)).</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-queue.png" alt-text="Exemple de file d’attente des alertes":::

<span data-ttu-id="8a12b-114">Des alertes provenant de différentes solutions de sécurité Microsoft telles que Microsoft Defender pour endpoint, Microsoft Defender pour Office 365 et Microsoft 365 Defender apparaissent ici.</span><span class="sxs-lookup"><span data-stu-id="8a12b-114">Alerts from different Microsoft security solutions like Microsoft Defender for Endpoint, Microsoft Defender for Office 365, and Microsoft 365 Defender appear here.</span></span>

<span data-ttu-id="8a12b-115">Par défaut, la file d’attente des alertes dans Microsoft 365 centre de sécurité affiche les alertes nouvelles et en cours depuis les 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="8a12b-115">By default, the alerts queue in the Microsoft 365 security center displays the new and in progress alerts from the last 30 days.</span></span> <span data-ttu-id="8a12b-116">L’alerte la plus récente se trouve en haut de la liste pour que vous la voyez en premier.</span><span class="sxs-lookup"><span data-stu-id="8a12b-116">The most recent alert is at the top of the list so you can see it first.</span></span> 

<span data-ttu-id="8a12b-117">Dans la file d’attente des alertes par défaut, vous pouvez sélectionner **Filtres** pour voir un volet **Filtres,** à partir duquel vous pouvez spécifier un sous-ensemble des alertes.</span><span class="sxs-lookup"><span data-stu-id="8a12b-117">From the default alerts queue, you can select **Filters** to see a **Filters** pane, from which you can specify a subset of the alerts.</span></span> <span data-ttu-id="8a12b-118">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="8a12b-118">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-filter.png" alt-text="Exemple de volet de filtres pour la file d’attente d’alertes":::

<span data-ttu-id="8a12b-120">Vous pouvez filtrer les alertes en fonction de ces critères :</span><span class="sxs-lookup"><span data-stu-id="8a12b-120">You can filter alerts according to these criteria:</span></span>

- <span data-ttu-id="8a12b-121">Severity</span><span class="sxs-lookup"><span data-stu-id="8a12b-121">Severity</span></span>
- <span data-ttu-id="8a12b-122">Statut</span><span class="sxs-lookup"><span data-stu-id="8a12b-122">Status</span></span>
- <span data-ttu-id="8a12b-123">Catégorie</span><span class="sxs-lookup"><span data-stu-id="8a12b-123">Category</span></span>
- <span data-ttu-id="8a12b-124">Source de détection</span><span class="sxs-lookup"><span data-stu-id="8a12b-124">Detection source</span></span>
- <span data-ttu-id="8a12b-125">Balises</span><span class="sxs-lookup"><span data-stu-id="8a12b-125">Tags</span></span>
- <span data-ttu-id="8a12b-126">Stratégie</span><span class="sxs-lookup"><span data-stu-id="8a12b-126">Policy</span></span>
- <span data-ttu-id="8a12b-127">Ressources impactées</span><span class="sxs-lookup"><span data-stu-id="8a12b-127">Impacted assets</span></span>

## <a name="analyze-an-alert"></a><span data-ttu-id="8a12b-128">Analyser une alerte</span><span class="sxs-lookup"><span data-stu-id="8a12b-128">Analyze an alert</span></span>

<span data-ttu-id="8a12b-129">Pour voir la page principale de l’alerte, sélectionnez le nom de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="8a12b-129">To see the main alert page, select the name of the alert.</span></span> <span data-ttu-id="8a12b-130">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="8a12b-130">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-main.png" alt-text="Exemple de page de détails d’une alerte dans le centre de Microsoft 365 de sécurité":::

<span data-ttu-id="8a12b-132">Vous pouvez également sélectionner l’action Ouvrir la **page d’alerte** principale dans le volet Gérer **les** alertes.</span><span class="sxs-lookup"><span data-stu-id="8a12b-132">You can also select the **Open the main alert page** action from the **Manage alert** pane.</span></span>

<span data-ttu-id="8a12b-133">Une page d’alerte se compose des sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a12b-133">An alert page is composed of these sections:</span></span> 

- <span data-ttu-id="8a12b-134">Article d’alerte, qui est la chaîne d’événements et d’alertes liés à cette alerte dans l’ordre chronologique</span><span class="sxs-lookup"><span data-stu-id="8a12b-134">Alert story, which is the chain of events and alerts related to this alert in chronological order</span></span>
- <span data-ttu-id="8a12b-135">Détails récapitulatifs</span><span class="sxs-lookup"><span data-stu-id="8a12b-135">Summary details</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-main.png" alt-text="Exemple de page de détails d’une alerte dans le centre de Microsoft 365 de sécurité":::

<span data-ttu-id="8a12b-137">Dans une page d’alerte, vous pouvez sélectionner les ellipses (**...**) à côté de n’importe quelle entité pour voir les actions disponibles, telles que l’ouverture de la page d’alerte ou la liaison de l’alerte à un autre incident.</span><span class="sxs-lookup"><span data-stu-id="8a12b-137">Throughout an alert page, you can select the ellipses (**...**) beside any entity to see available actions, such as opening the alert page or linking the alert to another incident.</span></span>

### <a name="alert-sources"></a><span data-ttu-id="8a12b-138">Sources d’alerte</span><span class="sxs-lookup"><span data-stu-id="8a12b-138">Alert sources</span></span>
<span data-ttu-id="8a12b-139">Microsoft 365 Les alertes Defender peuvent être issues de solutions telles que Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365 et Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="8a12b-139">Microsoft 365 Defender alerts may come from solutions like Microsoft Defender for Endpoint, Microsoft Defender for Office 365, and Microsoft Cloud App Security.</span></span> <span data-ttu-id="8a12b-140">Vous remarquerez peut-être des alertes avec des caractères prédépendants dans l’alerte.</span><span class="sxs-lookup"><span data-stu-id="8a12b-140">You may notice alerts with prepended characters in the alert.</span></span> <span data-ttu-id="8a12b-141">Le tableau suivant fournit des conseils pour vous aider à comprendre le mappage des sources d’alerte en fonction du caractère prédépendant de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="8a12b-141">The following table provides guidance to help you understand the mapping of alert sources based on the prepended character on the alert.</span></span>

> [!NOTE]
> - <span data-ttu-id="8a12b-142">Les GUID prédépendants sont spécifiques uniquement aux expériences unifiées telles que la file d’attente des alertes unifiées, la page des alertes unifiées, l’examen unifié et l’incident unifié.</span><span class="sxs-lookup"><span data-stu-id="8a12b-142">The prepended GUIDs are specific only to unified experiences such as unified alerts queue, unified alerts page, unified investigation, and unified incident.</span></span><br>
> - <span data-ttu-id="8a12b-143">Le caractère précédé ne modifie pas le GUID de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="8a12b-143">The prepended character does not change the GUID of the alert.</span></span> <span data-ttu-id="8a12b-144">La seule modification du GUID est le composant prédépendant.</span><span class="sxs-lookup"><span data-stu-id="8a12b-144">The only change to the GUID is the prepended component.</span></span><br>


<span data-ttu-id="8a12b-145">Source de l’alerte</span><span class="sxs-lookup"><span data-stu-id="8a12b-145">Alert source</span></span> | <span data-ttu-id="8a12b-146">Caractère prédépendé</span><span class="sxs-lookup"><span data-stu-id="8a12b-146">Prepended character</span></span> 
:---|:---
<span data-ttu-id="8a12b-147">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8a12b-147">Microsoft Defender for Office 365</span></span> | `fa{GUID}` <br> <span data-ttu-id="8a12b-148">Exemple : `fa123a456b-c789-1d2e-12f1g33h445h6i`</span><span class="sxs-lookup"><span data-stu-id="8a12b-148">Example: `fa123a456b-c789-1d2e-12f1g33h445h6i`</span></span> 
<span data-ttu-id="8a12b-149">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8a12b-149">Microsoft Defender for Endpoint</span></span> | <span data-ttu-id="8a12b-150">`da` ou `ed` pour les alertes de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="8a12b-150">`da` or `ed` for custom detection alerts</span></span> <br> 
<span data-ttu-id="8a12b-151">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="8a12b-151">Microsoft Defender for Identity</span></span> | `aa{GUID}` <br> <span data-ttu-id="8a12b-152">Exemple : `aa123a456b-c789-1d2e-12f1g33h445h6i`</span><span class="sxs-lookup"><span data-stu-id="8a12b-152">Example: `aa123a456b-c789-1d2e-12f1g33h445h6i`</span></span> 
<span data-ttu-id="8a12b-153">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="8a12b-153">Microsoft Cloud App Security</span></span> |`ca{GUID}` <br> <span data-ttu-id="8a12b-154">Exemple : `aa123a456b-c789-1d2e-12f1g33h445h6i`</span><span class="sxs-lookup"><span data-stu-id="8a12b-154">Example: `aa123a456b-c789-1d2e-12f1g33h445h6i`</span></span> 



### <a name="analyze-affected-assets"></a><span data-ttu-id="8a12b-155">Analyser les ressources affectées</span><span class="sxs-lookup"><span data-stu-id="8a12b-155">Analyze affected assets</span></span>

<span data-ttu-id="8a12b-156">La section **Actions entreprises** contient une liste des biens concernés, tels que les boîtes aux lettres, les appareils et les utilisateurs affectés par cette alerte.</span><span class="sxs-lookup"><span data-stu-id="8a12b-156">The **Actions taken** section has a list of impacted assets, such as mailboxes, devices, and users affected by this alert.</span></span> 

<span data-ttu-id="8a12b-157">Vous pouvez également sélectionner Afficher dans  le centre  **de sécurité** pour afficher l’onglet Historique du centre de Microsoft 365 de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8a12b-157">You can also select **View in action center** to view the **History** tab of the **Action center** in the Microsoft 365 security center.</span></span> 

### <a name="trace-an-alerts-role-in-the-alert-story"></a><span data-ttu-id="8a12b-158">Suivre le rôle d’une alerte dans l’article d’alerte</span><span class="sxs-lookup"><span data-stu-id="8a12b-158">Trace an alert's role in the alert story</span></span>

<span data-ttu-id="8a12b-159">L’article d’alerte affiche toutes les ressources ou entités associées à l’alerte dans une arborescence de processus.</span><span class="sxs-lookup"><span data-stu-id="8a12b-159">The alert story displays all assets or entities related to the alert in a process tree view.</span></span> <span data-ttu-id="8a12b-160">L’alerte dans le titre est celle qui est sélectionnée lorsque vous vous pointez pour la première fois sur la page de votre alerte sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8a12b-160">The alert in the title is the one in focus when you first land on your selected alert's page.</span></span> <span data-ttu-id="8a12b-161">Les ressources de l’article d’alerte sont ex expandables et peuvent être cliquées.</span><span class="sxs-lookup"><span data-stu-id="8a12b-161">Assets in the alert story are expandable and clickable.</span></span> <span data-ttu-id="8a12b-162">Ils fournissent des informations supplémentaires et accélèrent votre réponse en vous permettant d’agir directement dans le contexte de la page d’alerte.</span><span class="sxs-lookup"><span data-stu-id="8a12b-162">They provide additional information and expedite your response by allowing you to take action right in the context of the alert page.</span></span> 

> [!NOTE]
> <span data-ttu-id="8a12b-163">La section de l’article sur l’alerte peut contenir plusieurs alertes, avec des alertes supplémentaires liées à la même arborescence d’exécution apparaissant avant ou après l’alerte que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8a12b-163">The alert story section may contain more than one alert, with additional alerts related to the same execution tree appearing before or after the alert you've selected.</span></span>

### <a name="view-more-alert-information-on-the-details-page"></a><span data-ttu-id="8a12b-164">Afficher plus d’informations sur les alertes sur la page de détails</span><span class="sxs-lookup"><span data-stu-id="8a12b-164">View more alert information on the details page</span></span>

<span data-ttu-id="8a12b-165">La page de détails affiche les détails de l’alerte sélectionnée, ainsi que les détails et les actions qui y sont associés.</span><span class="sxs-lookup"><span data-stu-id="8a12b-165">The details page shows the details of the selected alert, with details and actions related to it.</span></span> <span data-ttu-id="8a12b-166">Si vous sélectionnez l’une des ressources ou entités affectées dans l’article d’alerte, la page de détails change pour fournir des informations contextuelles et des actions pour l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8a12b-166">If you select any of the affected assets or entities in the alert story, the details page changes to provide contextual information and actions for the selected object.</span></span>

<span data-ttu-id="8a12b-167">Une fois que vous avez sélectionné une entité d’intérêt, la page de détails change pour afficher les informations sur le type d’entité sélectionné, les informations historiques lorsqu’elle est disponible et les options d’action sur cette entité directement à partir de la page d’alerte.</span><span class="sxs-lookup"><span data-stu-id="8a12b-167">Once you've selected an entity of interest, the details page changes to display information about the selected entity type, historic information when it's available, and options to take action on this entity directly from the alert page.</span></span>

## <a name="manage-alerts"></a><span data-ttu-id="8a12b-168">Gérer des alertes</span><span class="sxs-lookup"><span data-stu-id="8a12b-168">Manage alerts</span></span>

<span data-ttu-id="8a12b-169">Pour gérer une alerte, sélectionnez l’alerte dans la file d’attente des alertes sur sa ligne pour voir un volet Gérer **les** alertes.</span><span class="sxs-lookup"><span data-stu-id="8a12b-169">To manage an alert, select the alert in the alerts queue on its row to see a **Manage alert** pane.</span></span> <span data-ttu-id="8a12b-170">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="8a12b-170">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-manage.png" alt-text="Exemple du volet récapitulatif d’une alerte":::

<span data-ttu-id="8a12b-172">Le **volet Gérer les** alertes vous permet de spécifier :</span><span class="sxs-lookup"><span data-stu-id="8a12b-172">The **Manage alert** pane allows you to specify:</span></span>

- <span data-ttu-id="8a12b-173">État de l’alerte (Nouveau, Résolu, En cours).</span><span class="sxs-lookup"><span data-stu-id="8a12b-173">The alert status (New, Resolved, In progress).</span></span>
- <span data-ttu-id="8a12b-174">Classification de l’alerte (non définie, alerte True, Fausse alerte).</span><span class="sxs-lookup"><span data-stu-id="8a12b-174">The alert's classification  (Not set, True alert, False Alert).</span></span>
- <span data-ttu-id="8a12b-175">Pour la classification en tant qu’alerte réelle, le type de menace pour l’alerte dans le **champ Détermination.**</span><span class="sxs-lookup"><span data-stu-id="8a12b-175">For the classification as a true alert, the type of threat for the alert in **Determination** field.</span></span>
- <span data-ttu-id="8a12b-176">Commentaire de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="8a12b-176">A comment on the alert.</span></span>

> [!NOTE]
> <span data-ttu-id="8a12b-177">Une façon de gérer les alertes par le biais de l’utilisation de balises.</span><span class="sxs-lookup"><span data-stu-id="8a12b-177">One way of managing alerts it through the use of tags.</span></span> <span data-ttu-id="8a12b-178">La fonctionnalité de marquage de Microsoft Defender pour Office 365 est déployée de manière incrémentielle et est actuellement en prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="8a12b-178">The tagging capability for Microsoft Defender for Office 365 is incrementally being rolled out and is currently in preview.</span></span> <br>
> <span data-ttu-id="8a12b-179">Actuellement, les noms de balise modifiés sont appliqués uniquement aux alertes créées *après la* mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8a12b-179">Currently, modified tag names are only applied to alerts created *after* the update.</span></span> <span data-ttu-id="8a12b-180">Les alertes qui ont été générées avant la modification ne reflètent pas le nom de balise mis à jour.</span><span class="sxs-lookup"><span data-stu-id="8a12b-180">Alerts that were generated before the modification will not reflect the updated tag name.</span></span> 

<span data-ttu-id="8a12b-181">À partir de ce volet, vous pouvez également effectuer les actions supplémentaires ci-après :</span><span class="sxs-lookup"><span data-stu-id="8a12b-181">From this pane, you can also perform these additional actions:</span></span> 

- <span data-ttu-id="8a12b-182">Ouvrir la page principale d’alerte</span><span class="sxs-lookup"><span data-stu-id="8a12b-182">Open the main alert page</span></span>
- <span data-ttu-id="8a12b-183">Consulter un expert en menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="8a12b-183">Consult a Microsoft threat expert</span></span>
- <span data-ttu-id="8a12b-184">Afficher l’envoi</span><span class="sxs-lookup"><span data-stu-id="8a12b-184">View submission</span></span>
- <span data-ttu-id="8a12b-185">Lien vers un autre incident</span><span class="sxs-lookup"><span data-stu-id="8a12b-185">Link to another incident</span></span>
- <span data-ttu-id="8a12b-186">Voir l’alerte dans une chronologie</span><span class="sxs-lookup"><span data-stu-id="8a12b-186">See the alert in a timeline</span></span>
- <span data-ttu-id="8a12b-187">Créer une règle de suppression</span><span class="sxs-lookup"><span data-stu-id="8a12b-187">Create a suppression rule</span></span>

<span data-ttu-id="8a12b-188">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="8a12b-188">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-alerts/alerts-ss-alerts-actions.png" alt-text="Exemple d’actions sur une alerte dans le centre de Microsoft 365 de sécurité":::

<span data-ttu-id="8a12b-190">La liste des actions supplémentaires dépend du type d’alerte.</span><span class="sxs-lookup"><span data-stu-id="8a12b-190">The list of additional actions depends on the type of alert.</span></span>

## <a name="resolve-an-alert"></a><span data-ttu-id="8a12b-191">Résoudre une alerte</span><span class="sxs-lookup"><span data-stu-id="8a12b-191">Resolve an alert</span></span>

<span data-ttu-id="8a12b-192">Une fois que vous avez terminé l’analyse d’une  alerte et qu’elle peut être  résolue, allez dans le volet Gérer l’alerte et marquez l’état de l’alerte comme Résolu et classez-la en tant qu’alerte **False** ou Alerte **True.**</span><span class="sxs-lookup"><span data-stu-id="8a12b-192">Once you're done analyzing an alert and it can be resolved, go to the **Manage alert** pane for the alert and mark the it status as **Resolved** and classify it as either a **False alert** or **True alert**.</span></span> <span data-ttu-id="8a12b-193">Pour les alertes vraies, spécifiez le type de menace de l’alerte dans le **champ Détermination.**</span><span class="sxs-lookup"><span data-stu-id="8a12b-193">For true alerts, specify the alert's threat type in the **Determination** field.</span></span>

<span data-ttu-id="8a12b-194">La classification des alertes et la spécification de leur détermination permettent d’Microsoft 365 Defender pour fournir plus d’alertes vraies et moins de fausses alertes.</span><span class="sxs-lookup"><span data-stu-id="8a12b-194">Classifying alerts and specifying their determination helps tune Microsoft 365 Defender to provide more true alerts and less false alerts.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8a12b-195">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8a12b-195">Next steps</span></span>

<span data-ttu-id="8a12b-196">Si nécessaire pour les incidents in-process, poursuivez votre [enquête.](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="8a12b-196">As needed for in-process incidents, continue your [investigation](investigate-incidents.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8a12b-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a12b-197">See also</span></span>

- [<span data-ttu-id="8a12b-198">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="8a12b-198">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="8a12b-199">Gérer des incidents</span><span class="sxs-lookup"><span data-stu-id="8a12b-199">Manage incidents</span></span>](manage-incidents.md)
- [<span data-ttu-id="8a12b-200">Examiner des incidents</span><span class="sxs-lookup"><span data-stu-id="8a12b-200">Investigate incidents</span></span>](investigate-incidents.md)
