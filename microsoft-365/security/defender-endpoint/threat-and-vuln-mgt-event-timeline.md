---
title: Chronologie des événements dans la gestion des menaces et des vulnérabilités
description: La chronologie des événements est un flux d'actualités sur les risques qui vous permet d'interpréter la façon dont le risque est introduit dans l'organisation et les atténuations qui ont eu pour effet de le réduire.
keywords: chronologie des événements, chronologie des événements microsoft Defender pour point de terminaison, chronologie des événements tvm de Microsoft Defender pour point de terminaison, gestion des menaces et des vulnérabilités, Microsoft Defender pour point de terminaison
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 64362598ff4b0512eb110917071e6d32abb8ede9
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933480"
---
# <a name="event-timeline---threat-and-vulnerability-management"></a><span data-ttu-id="78a18-104">Chronologie des événements : gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="78a18-104">Event timeline - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="78a18-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="78a18-105">**Applies to:**</span></span>
- [<span data-ttu-id="78a18-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="78a18-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="78a18-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="78a18-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="78a18-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="78a18-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="78a18-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="78a18-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

<span data-ttu-id="78a18-110">La chronologie des événements est un flux d'actualités sur les risques qui vous permet d'interpréter la façon dont le risque est introduit dans l'organisation par le biais de nouvelles vulnérabilités ou de nouvelles exploitations.</span><span class="sxs-lookup"><span data-stu-id="78a18-110">Event timeline is a risk news feed that helps you interpret how risk is introduced into the organization through new vulnerabilities or exploits.</span></span> <span data-ttu-id="78a18-111">Vous pouvez afficher les événements qui peuvent avoir un impact sur les risques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="78a18-111">You can view events that may impact your organization's risk.</span></span> <span data-ttu-id="78a18-112">Par exemple, vous pouvez trouver de nouvelles vulnérabilités qui ont été introduites, des vulnérabilités qui sont devenues exploitables, des exploits ajoutés à un kit d'exploitation, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="78a18-112">For example, you can find new vulnerabilities that were introduced, vulnerabilities that became exploitable, exploit that was added to an exploit kit, and more.</span></span>

<span data-ttu-id="78a18-113">La chronologie des événements indique également l'histoire de votre [score](tvm-exposure-score.md) d'exposition et du score de sécurité [Microsoft](tvm-microsoft-secure-score-devices.md) pour les appareils afin que vous pouvez déterminer la cause des modifications importantes.</span><span class="sxs-lookup"><span data-stu-id="78a18-113">Event timeline also tells the story of your [exposure score](tvm-exposure-score.md) and [Microsoft Secure Score for Devices](tvm-microsoft-secure-score-devices.md) so you can determine the cause of large changes.</span></span> <span data-ttu-id="78a18-114">Les événements peuvent avoir un impact sur vos appareils ou votre score pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="78a18-114">Events can impact your devices or your score for devices.</span></span> <span data-ttu-id="78a18-115">Réduisez votre exposition en résribuant ce qui doit être corrigé en fonction des recommandations de sécurité [prioritaires.](tvm-security-recommendation.md)</span><span class="sxs-lookup"><span data-stu-id="78a18-115">Reduce you exposure by addressing what needs to be remediated based on the prioritized [security recommendations](tvm-security-recommendation.md).</span></span>

>[!TIP]
><span data-ttu-id="78a18-116">Pour obtenir des e-mails sur les nouveaux événements de vulnérabilité, voir Configurer les notifications par courrier électronique de vulnérabilité [dans Microsoft Defender pour le point de terminaison](configure-vulnerability-email-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="78a18-116">To get emails about new vulnerability events, see [Configure vulnerability email notifications in Microsoft Defender for Endpoint](configure-vulnerability-email-notifications.md)</span></span>

## <a name="navigate-to-the-event-timeline-page"></a><span data-ttu-id="78a18-117">Accéder à la page Chronologie des événements</span><span class="sxs-lookup"><span data-stu-id="78a18-117">Navigate to the Event timeline page</span></span>

<span data-ttu-id="78a18-118">Il existe également trois points d'entrée du tableau de bord de gestion des menaces [et des vulnérabilités](tvm-dashboard-insights.md):</span><span class="sxs-lookup"><span data-stu-id="78a18-118">There are also three entry points from the [threat and vulnerability management dashboard](tvm-dashboard-insights.md):</span></span>

- <span data-ttu-id="78a18-119">**Carte de score d'exposition de** l'organisation : pointez sur les points d'événement dans le graphique « Score d'exposition au fil du temps », puis sélectionnez « Voir tous les événements de ce jour ».</span><span class="sxs-lookup"><span data-stu-id="78a18-119">**Organization exposure score card**: Hover over the event dots in the "Exposure Score over time" graph and select "See all events from this day."</span></span> <span data-ttu-id="78a18-120">Les événements représentent des vulnérabilités logicielles.</span><span class="sxs-lookup"><span data-stu-id="78a18-120">The events represent software vulnerabilities.</span></span>
- <span data-ttu-id="78a18-121">**Score de sécurité Microsoft pour les** appareils : pointez sur les points d'événement dans le graphique « Votre score pour les appareils au fil du temps », puis sélectionnez « Voir tous les événements de ce jour ».</span><span class="sxs-lookup"><span data-stu-id="78a18-121">**Microsoft Secure Score for Devices**: Hover over the event dots in the "Your score for devices over time" graph and select "See all events from this day."</span></span> <span data-ttu-id="78a18-122">Les événements représentent de nouvelles évaluations de configuration.</span><span class="sxs-lookup"><span data-stu-id="78a18-122">The events represent new configuration assessments.</span></span>
- <span data-ttu-id="78a18-123">**Carte événements principales**: sélectionnez « Afficher plus » en bas du tableau des événements supérieurs.</span><span class="sxs-lookup"><span data-stu-id="78a18-123">**Top events card**: Select "Show more" at the bottom of the top events table.</span></span> <span data-ttu-id="78a18-124">La carte affiche les trois événements les plus importants au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="78a18-124">The card displays the three most impactful events in the last 7 days.</span></span> <span data-ttu-id="78a18-125">Les événements avec impact peuvent inclure si l'événement affecte un grand nombre d'appareils ou s'il s'agit d'une vulnérabilité critique.</span><span class="sxs-lookup"><span data-stu-id="78a18-125">Impactful events can include if the event affects a large number of devices, or if it is a critical vulnerability.</span></span>

### <a name="exposure-score-and-microsoft-secure-score-for-devices-graphs"></a><span data-ttu-id="78a18-126">Graphiques du score d'exposition et du niveau de sécurité Microsoft pour les appareils</span><span class="sxs-lookup"><span data-stu-id="78a18-126">Exposure score and Microsoft Secure Score for Devices graphs</span></span>

<span data-ttu-id="78a18-127">Dans le tableau de bord de gestion des menaces et des vulnérabilités, pointez sur le graphique du score d'exposition pour afficher les principaux événements de vulnérabilité logicielle qui ont eu un impact sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="78a18-127">In the threat and vulnerability management dashboard, hover over the Exposure score graph to view top software vulnerability events from that day that impacted your devices.</span></span> <span data-ttu-id="78a18-128">Pointez sur le graphique Score de sécurité Microsoft pour les appareils pour afficher les nouvelles évaluations de configuration de la sécurité qui affectent votre score.</span><span class="sxs-lookup"><span data-stu-id="78a18-128">Hover over the Microsoft Secure Score for Devices graph to view new security configuration assessments that affect your score.</span></span>

<span data-ttu-id="78a18-129">Si aucun événement n'affecte vos appareils ou votre score pour les appareils, aucun ne s'affiche.</span><span class="sxs-lookup"><span data-stu-id="78a18-129">If there are no events that affect your devices or your score for devices, then none will be shown.</span></span>

<span data-ttu-id="78a18-130">![Score d'exposition ](images/tvm-event-timeline-exposure-score350.png) 
 ![ pointage Niveau de sécurisation Microsoft pour les appareils pointage](images/tvm-event-timeline-device-hover360.png)</span><span class="sxs-lookup"><span data-stu-id="78a18-130">![Exposure score hover](images/tvm-event-timeline-exposure-score350.png) 
![Microsoft Secure Score for Devices hover](images/tvm-event-timeline-device-hover360.png)</span></span>

### <a name="drill-down-to-events-from-that-day"></a><span data-ttu-id="78a18-131">Descendre dans les événements de ce jour</span><span class="sxs-lookup"><span data-stu-id="78a18-131">Drill down to events from that day</span></span>

<span data-ttu-id="78a18-132">La sélection **d'Afficher tous** les événements de ce jour vous place sur la page chronologie des événements avec une plage de dates personnalisée pour ce jour.</span><span class="sxs-lookup"><span data-stu-id="78a18-132">Selecting **Show all events from this day** takes you to the Event timeline page with a custom date range for that day.</span></span>

![Chronologie des événements : plage de dates personnalisée sélectionnée](images/tvm-event-timeline-drilldown.png)

<span data-ttu-id="78a18-134">Sélectionnez **Plage personnalisée** pour modifier la plage de dates en une autre personnalisée ou une plage de temps pré-définie.</span><span class="sxs-lookup"><span data-stu-id="78a18-134">Select **Custom range** to change the date range to another custom one, or a pre-set time range.</span></span>

![Options de plage de dates de chronologie des événements](images/tvm-event-timeline-dates.png)

## <a name="event-timeline-overview"></a><span data-ttu-id="78a18-136">Vue d'ensemble de la chronologie des événements</span><span class="sxs-lookup"><span data-stu-id="78a18-136">Event timeline overview</span></span>

<span data-ttu-id="78a18-137">Dans la page Chronologie des événements, vous pouvez afficher toutes les informations nécessaires relatives à un événement.</span><span class="sxs-lookup"><span data-stu-id="78a18-137">On the Event timeline page, you can view the all the necessary info related to an event.</span></span> 

<span data-ttu-id="78a18-138">Fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="78a18-138">Features:</span></span>

- <span data-ttu-id="78a18-139">Personnaliser les colonnes</span><span class="sxs-lookup"><span data-stu-id="78a18-139">Customize columns</span></span>
- <span data-ttu-id="78a18-140">Filtrer par type d'événement ou pourcentage d'appareils touchés</span><span class="sxs-lookup"><span data-stu-id="78a18-140">Filter by event type or percent of impacted devices</span></span>
- <span data-ttu-id="78a18-141">Afficher 30, 50 ou 100 éléments par page</span><span class="sxs-lookup"><span data-stu-id="78a18-141">View 30, 50, or 100 items per page</span></span>

<span data-ttu-id="78a18-142">Les deux grands nombres en haut de la page indiquent le nombre de nouvelles vulnérabilités et de vulnérabilités exploitables, et non d'événements.</span><span class="sxs-lookup"><span data-stu-id="78a18-142">The two large numbers at the top of the page show the number of new vulnerabilities and exploitable vulnerabilities, not events.</span></span> <span data-ttu-id="78a18-143">Certains événements peuvent avoir plusieurs vulnérabilités et d'autres peuvent avoir plusieurs événements.</span><span class="sxs-lookup"><span data-stu-id="78a18-143">Some events can have multiple vulnerabilities, and some vulnerabilities can have multiple events.</span></span>

![Page Chronologie des événements](images/tvm-event-timeline-overview-mixed-type.png)

### <a name="columns"></a><span data-ttu-id="78a18-145">Colonnes</span><span class="sxs-lookup"><span data-stu-id="78a18-145">Columns</span></span>

- <span data-ttu-id="78a18-146">**Date**: mois, jour, année</span><span class="sxs-lookup"><span data-stu-id="78a18-146">**Date**: month, day, year</span></span>
- <span data-ttu-id="78a18-147">**Événement**: événement impactant, y compris le composant, le type et le nombre d'appareils touchés</span><span class="sxs-lookup"><span data-stu-id="78a18-147">**Event**: impactful event, including component, type, and number of impacted devices</span></span>
- <span data-ttu-id="78a18-148">**Composant associé :** logiciel</span><span class="sxs-lookup"><span data-stu-id="78a18-148">**Related component**: software</span></span>
- <span data-ttu-id="78a18-149">**Appareils touchés à l'origine**: nombre et pourcentage d'appareils touchés lorsque cet événement s'est produit à l'origine.</span><span class="sxs-lookup"><span data-stu-id="78a18-149">**Originally impacted devices**: the number, and percentage, of impacted devices when this event originally occurred.</span></span> <span data-ttu-id="78a18-150">Vous pouvez également filtrer d'après le pourcentage d'appareils touchés à l'origine, par rapport au nombre total d'appareils.</span><span class="sxs-lookup"><span data-stu-id="78a18-150">You can also filter by the percent of originally impacted devices, out of your total number of devices.</span></span>
- <span data-ttu-id="78a18-151">**Appareils actuellement touchés**: nombre actuel et pourcentage d'appareils impactés par cet événement.</span><span class="sxs-lookup"><span data-stu-id="78a18-151">**Currently impacted devices**: the current number, and percentage, of devices that this event currently impacts.</span></span> <span data-ttu-id="78a18-152">Vous pouvez trouver ce champ en sélectionnant **Personnaliser les colonnes.**</span><span class="sxs-lookup"><span data-stu-id="78a18-152">You can find this field by selecting **Customize columns**.</span></span>
- <span data-ttu-id="78a18-153">**Types**: reflètent les événements horodatés qui ont un impact sur le score.</span><span class="sxs-lookup"><span data-stu-id="78a18-153">**Types**: reflect time-stamped events that impact the score.</span></span> <span data-ttu-id="78a18-154">Elles peuvent être filtrées.</span><span class="sxs-lookup"><span data-stu-id="78a18-154">They can be filtered.</span></span>
    - <span data-ttu-id="78a18-155">Exploit ajouté à un kit d'exploitation</span><span class="sxs-lookup"><span data-stu-id="78a18-155">Exploit added to an exploit kit</span></span>
    - <span data-ttu-id="78a18-156">Exploit a été vérifié</span><span class="sxs-lookup"><span data-stu-id="78a18-156">Exploit was verified</span></span>
    - <span data-ttu-id="78a18-157">Nouvelle exploitation publique</span><span class="sxs-lookup"><span data-stu-id="78a18-157">New public exploit</span></span>
    - <span data-ttu-id="78a18-158">Nouvelle vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="78a18-158">New vulnerability</span></span>
    - <span data-ttu-id="78a18-159">Nouvelle évaluation de la configuration</span><span class="sxs-lookup"><span data-stu-id="78a18-159">New configuration assessment</span></span>
- <span data-ttu-id="78a18-160">**Tendance des scores :** tendance du score d'exposition</span><span class="sxs-lookup"><span data-stu-id="78a18-160">**Score trend**: exposure score trend</span></span>

### <a name="icons"></a><span data-ttu-id="78a18-161">Icônes</span><span class="sxs-lookup"><span data-stu-id="78a18-161">Icons</span></span>

<span data-ttu-id="78a18-162">Les icônes suivantes s'affiche en plus des événements :</span><span class="sxs-lookup"><span data-stu-id="78a18-162">The following icons show up next to events:</span></span>

- ![icône de bogue](images/tvm-black-bug-icon.png) <span data-ttu-id="78a18-164">Nouvelle exploitation publique</span><span class="sxs-lookup"><span data-stu-id="78a18-164">New public exploit</span></span>
- ![icône d'avertissement de rapport](images/report-warning-icon.png) <span data-ttu-id="78a18-166">Nouvelle vulnérabilité publiée</span><span class="sxs-lookup"><span data-stu-id="78a18-166">New vulnerability was published</span></span>
- ![kit exploit](images/bug-lightning-icon2.png) <span data-ttu-id="78a18-168">Exploit trouvé dans exploit kit</span><span class="sxs-lookup"><span data-stu-id="78a18-168">Exploit found in exploit kit</span></span>
- ![icône de bogue avec icône d'avertissement](images/bug-caution-icon2.png) <span data-ttu-id="78a18-170">Exploit vérifié</span><span class="sxs-lookup"><span data-stu-id="78a18-170">Exploit verified</span></span>

### <a name="drill-down-to-a-specific-event"></a><span data-ttu-id="78a18-171">Accès à un événement spécifique</span><span class="sxs-lookup"><span data-stu-id="78a18-171">Drill down to a specific event</span></span>

<span data-ttu-id="78a18-172">Une fois que vous avez sélectionné un événement, un flyout s'affiche avec une liste des détails et des CV actuels qui affectent vos appareils.</span><span class="sxs-lookup"><span data-stu-id="78a18-172">Once you select an event, a flyout will appear with a list of the details and current CVEs that affect your devices.</span></span> <span data-ttu-id="78a18-173">Vous pouvez afficher d'autres CV ou consulter la recommandation associée.</span><span class="sxs-lookup"><span data-stu-id="78a18-173">You can show more CVEs or view the related recommendation.</span></span>

<span data-ttu-id="78a18-174">La flèche sous « tendance de score » vous permet de déterminer si cet événement a potentiellement augmenté ou réduit le score d'exposition de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="78a18-174">The arrow below "score trend" helps you determine whether this event potentially raised or lowered your organizational exposure score.</span></span> <span data-ttu-id="78a18-175">Un score d'exposition plus élevé signifie que les appareils sont plus vulnérables à l'exploitation.</span><span class="sxs-lookup"><span data-stu-id="78a18-175">Higher exposure score means devices are more vulnerable to exploitation.</span></span>

![Volant de chronologie des événements](images/tvm-event-timeline-flyout500.png)

<span data-ttu-id="78a18-177">À partir de là, sélectionnez Go **to related security recommendation** view the recommendation that addresses the new software vulnerability in the security [recommendations page](tvm-security-recommendation.md).</span><span class="sxs-lookup"><span data-stu-id="78a18-177">From there, select **Go to related security recommendation** view the recommendation that addresses the new software vulnerability in the [security recommendations page](tvm-security-recommendation.md).</span></span> <span data-ttu-id="78a18-178">Après avoir lu la description et les détails de la vulnérabilité dans la recommandation de sécurité, vous pouvez envoyer une demande de correction et suivre la demande dans la [page de correction.](tvm-remediation.md)</span><span class="sxs-lookup"><span data-stu-id="78a18-178">After reading the description and vulnerability details in the security recommendation, you can submit a remediation request, and track the request in the [remediation page](tvm-remediation.md).</span></span>  

## <a name="view-event-timelines-in-software-pages"></a><span data-ttu-id="78a18-179">Afficher les chronologies des événements dans les pages logicielles</span><span class="sxs-lookup"><span data-stu-id="78a18-179">View Event timelines in software pages</span></span>

<span data-ttu-id="78a18-180">Pour ouvrir une page de logiciels, sélectionnez un > sélectionnez le nom du logiciel avec lien hypertexte (comme Visual Studio 2017) dans la section intitulée « Composant associé » dans le volant.</span><span class="sxs-lookup"><span data-stu-id="78a18-180">To open a software page, select an event > select the hyperlinked software name (like Visual Studio 2017) in the section called "Related component" in the flyout.</span></span> [<span data-ttu-id="78a18-181">En savoir plus sur les pages logicielles</span><span class="sxs-lookup"><span data-stu-id="78a18-181">Learn more about software pages</span></span>](tvm-software-inventory.md#software-pages)

<span data-ttu-id="78a18-182">Une page complète s'affiche avec tous les détails d'un logiciel spécifique.</span><span class="sxs-lookup"><span data-stu-id="78a18-182">A full page will appear with all the details of a specific software.</span></span> <span data-ttu-id="78a18-183">Pointez sur le graphique pour voir la chronologie des événements pour ce logiciel spécifique.</span><span class="sxs-lookup"><span data-stu-id="78a18-183">Mouse over the graph to see the timeline of events for that specific software.</span></span>

![Page de logiciels avec un graphique de chronologie des événements](images/tvm-event-timeline-software2.png)

<span data-ttu-id="78a18-185">Accédez à l'onglet Chronologie des événements pour afficher tous les événements liés à ce logiciel.</span><span class="sxs-lookup"><span data-stu-id="78a18-185">Navigate to the event timeline tab to view all the events related to that software.</span></span> <span data-ttu-id="78a18-186">Vous pouvez également voir les recommandations de sécurité, les vulnérabilités découvertes, les appareils installés et la distribution des versions.</span><span class="sxs-lookup"><span data-stu-id="78a18-186">You can also see security recommendations, discovered vulnerabilities, installed devices, and version distribution.</span></span>

![Page logicielle avec un onglet Chronologie des événements](images/tvm-event-timeline-software-pages.png)

## <a name="related-topics"></a><span data-ttu-id="78a18-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78a18-188">Related topics</span></span>

- [<span data-ttu-id="78a18-189">Vue d'ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="78a18-189">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="78a18-190">Tableau de bord</span><span class="sxs-lookup"><span data-stu-id="78a18-190">Dashboard</span></span>](tvm-dashboard-insights.md)
- [<span data-ttu-id="78a18-191">Score d'exposition</span><span class="sxs-lookup"><span data-stu-id="78a18-191">Exposure score</span></span>](tvm-exposure-score.md)
- [<span data-ttu-id="78a18-192">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="78a18-192">Security recommendations</span></span>](tvm-security-recommendation.md)
- [<span data-ttu-id="78a18-193">Corriger des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="78a18-193">Remediate vulnerabilities</span></span>](tvm-remediation.md)
- [<span data-ttu-id="78a18-194">Inventaire des logiciels</span><span class="sxs-lookup"><span data-stu-id="78a18-194">Software inventory</span></span>](tvm-software-inventory.md)

