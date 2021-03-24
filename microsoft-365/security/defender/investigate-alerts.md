---
title: Examiner les alertes dans Microsoft 365 Defender
description: Examiner les alertes visibles sur les appareils, les utilisateurs et les boîtes aux lettres.
keywords: incidents, alertes, enquêter, corrélation, attaque, machines, appareils, utilisateurs, identités, identité, boîte de réception, e-mail, 365, microsoft, m365
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
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
ms.openlocfilehash: bc325f88ec41861c2adc4d5147e94d2d2d5b1ebe
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51056638"
---
# <a name="investigate-alerts-in-microsoft-365-defender"></a><span data-ttu-id="0f0c9-104">Examiner les alertes dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0f0c9-104">Investigate alerts in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="0f0c9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0f0c9-105">**Applies to:**</span></span>
- <span data-ttu-id="0f0c9-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0f0c9-106">Microsoft 365 Defender</span></span>

[!INCLUDE [Prerelease](../includes/prerelease.md)]

<span data-ttu-id="0f0c9-107">Les alertes sont la base de tous les incidents et indiquent l’occurrence d’événements malveillants ou suspects dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-107">Alerts are the basis of all incidents and indicate the occurrence of malicious or suspicious events in your environment.</span></span> <span data-ttu-id="0f0c9-108">Les alertes font généralement partie d’une attaque plus large et fournissent des indices sur un incident.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-108">Alerts are typically part of a broader attack and provide pieces of clues about an incident.</span></span>

<span data-ttu-id="0f0c9-109">Dans Microsoft 365 Defender, les alertes associées sont regroupées pour former des incidents.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-109">In Microsoft 365 Defender, related alerts are aggregated together to form incidents.</span></span> <span data-ttu-id="0f0c9-110">Les incidents fournissent toujours le contexte plus large d’une attaque, mais l’analyse des alertes peut être utile lorsque des analyses plus approfondies sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-110">Incidents will always provide the broader context of an attack, however, investigating alerts can be valuable when deeper analysis is required.</span></span> 



## <a name="using-alert-pages-in-investigations"></a><span data-ttu-id="0f0c9-111">Utilisation de pages d’alerte dans les enquêtes</span><span class="sxs-lookup"><span data-stu-id="0f0c9-111">Using alert pages in investigations</span></span>

<span data-ttu-id="0f0c9-112">À partir de l’onglet Alertes d’une page d’incident, la sélection d’une alerte vous amène aux pages d’alerte individuelles.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-112">From the Alerts tab of any incident page, selecting an alert brings you to the individual alert pages.</span></span> <span data-ttu-id="0f0c9-113">Une page d’alerte se compose de trois sections : ressources affectées, article d’alerte et volet d’informations.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-113">An alert page is composed of three sections: affected assets, alert story, and the details pane.</span></span>

![Image d’exemple de page d’alerte](../../media/new-alert-page2.png)

<span data-ttu-id="0f0c9-115">Tout au long d’une page d’alerte, vous pouvez sélectionner l’icône à trois points (**...**) à côté de n’importe quelle entité afin de voir les actions disponibles, telles que l’ouverture de la page de biens spécifique ou l’action de correction spécifique.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-115">Throughout an alert page, you can select the three-dot icon (**...**) beside any entity so you can see available actions like opening the specific asset page or doing specific remediation steps.</span></span>

### <a name="analyze-affected-assets"></a><span data-ttu-id="0f0c9-116">Analyser les ressources affectées</span><span class="sxs-lookup"><span data-stu-id="0f0c9-116">Analyze affected assets</span></span>
<span data-ttu-id="0f0c9-117">La section Ressources affectées répertorie les boîtes aux lettres, les appareils et les utilisateurs affectés par cette alerte.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-117">The affected assets section lists mailboxes, devices, and users affected by this alert.</span></span> <span data-ttu-id="0f0c9-118">La sélection de l’une des cartes de biens remplit le volet latéral détails avec des informations, y compris d’autres alertes impliquant les biens, le cas besoin.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-118">Selecting any of the asset cards populates the details side pane with information, including other alerts that occurred involving the assets, if any.</span></span>


### <a name="trace-an-alerts-role-in-the-alert-story"></a><span data-ttu-id="0f0c9-119">Suivre le rôle d’une alerte dans l’article d’alerte</span><span class="sxs-lookup"><span data-stu-id="0f0c9-119">Trace an alert's role in the alert story</span></span>
<span data-ttu-id="0f0c9-120">L’article d’alerte affiche toutes les ressources ou entités associées à l’alerte dans une arborescence de processus.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-120">The alert story displays all assets or entities related to the alert in a process tree view.</span></span> <span data-ttu-id="0f0c9-121">L’alerte dans le titre est celle qui est sélectionnée lorsque vous vous pointez pour la première fois sur la page de votre alerte sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-121">The alert in the title is the one in focus when you first land on your selected alert's page.</span></span> <span data-ttu-id="0f0c9-122">Les ressources de l’article d’alerte sont ex expandables et peuvent être cliquées.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-122">Assets in the alert story are expandable and clickable.</span></span> <span data-ttu-id="0f0c9-123">Ils fournissent des informations supplémentaires et accélèrent la réponse en vous permettant d’agir directement dans le contexte de la page d’alerte.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-123">They provide additional information and expedite response by allowing you to take actions right in the context of the alert page.</span></span> 

> [!NOTE]
> <span data-ttu-id="0f0c9-124">La section de l’article sur l’alerte peut contenir plusieurs alertes, avec des alertes supplémentaires liées à la même arborescence d’exécution apparaissant avant ou après l’alerte que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-124">The alert story section may contain more than one alert, with additional alerts related to the same execution tree appearing before or after the alert you've selected.</span></span>

### <a name="view-more-alert-information-in-the-details-pane"></a><span data-ttu-id="0f0c9-125">Afficher plus d’informations sur les alertes dans le volet d’informations</span><span class="sxs-lookup"><span data-stu-id="0f0c9-125">View more alert information in the details pane</span></span>

<span data-ttu-id="0f0c9-126">Le volet d’informations affiche tout d’abord les détails de l’alerte sélectionnée, ainsi que les détails et les actions qui y sont associés.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-126">The details pane shows the details of the selected alert at first, with details and actions related to it.</span></span> <span data-ttu-id="0f0c9-127">Si vous sélectionnez l’une des ressources ou entités affectées dans l’article d’alerte, le volet d’informations change pour fournir des informations contextuelles et des actions pour l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-127">If you select any of the affected assets or entities in the alert story, the details pane changes to provide contextual information and actions for the selected object.</span></span>

<span data-ttu-id="0f0c9-128">Une fois que vous avez sélectionné une entité d’intérêt, le volet d’informations change pour afficher les informations sur le type d’entité sélectionné, les informations historiques lorsqu’elle est disponible et les options d’action sur cette entité directement à partir de la page d’alerte.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-128">Once you've selected an entity of interest, the details pane changes to display information about the selected entity type, historic information when it's available, and options to take action on this entity directly from the alert page.</span></span>

### <a name="manage-alerts"></a><span data-ttu-id="0f0c9-129">Gérer les alertes</span><span class="sxs-lookup"><span data-stu-id="0f0c9-129">Manage alerts</span></span>

<span data-ttu-id="0f0c9-130">Une fois que vous avez terminé d’examiner les alertes, vous pouvez revenir à l’alerte que vous avez démarrée, marquer l’état de l’alerte comme résolu et le classer comme alerte False ou Alerte True.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-130">Once you're done investigating the alerts, you can go back to the alert you started with, mark the alert's status as Resolved and classify it as either a False alert or True alert.</span></span> <span data-ttu-id="0f0c9-131">La classification des alertes permet d’affiner votre produit pour fournir plus d’alertes vraies et moins de fausses alertes.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-131">Classifying alerts helps tune your product to provide more true alerts and less false alerts.</span></span>

> [!NOTE]
> <span data-ttu-id="0f0c9-132">Une façon de gérer les alertes par le biais de l’utilisation de balises.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-132">One way of managing alerts it through the use of tags.</span></span> <span data-ttu-id="0f0c9-133">La fonctionnalité de marquage de Microsoft Defender pour Office 365 est déployée de manière incrémentielle et est actuellement en prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-133">The tagging capability for Microsoft Defender for Office 365 in incrementally being rolled out and is currently in preview.</span></span> <br>
> <span data-ttu-id="0f0c9-134">Actuellement, les noms de balise modifiés sont appliqués uniquement aux alertes créées *après la* mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-134">Currently, modified tag names are only applied to alerts created *after* the update.</span></span> <span data-ttu-id="0f0c9-135">Les alertes qui ont été générées avant la modification ne reflètent pas le nom de balise mis à jour.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-135">Alerts that were generated prior to the modification will not reflect the updated tag name.</span></span> 


## <a name="manage-the-unified-alert-queue"></a><span data-ttu-id="0f0c9-136">Gérer la file d’attente d’alerte unifiée</span><span class="sxs-lookup"><span data-stu-id="0f0c9-136">Manage the unified alert queue</span></span>

<span data-ttu-id="0f0c9-137">La sélection des alertes sous Incidents & alertes dans le volet de navigation du Centre de sécurité Microsoft 365 vous amène à la file d’attente d’alertes unifiée.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-137">Selecting Alerts under Incidents & Alerts in the Microsoft 365 security center navigation pane brings you to the unified alert queue.</span></span> <span data-ttu-id="0f0c9-138">Les alertes de différentes solutions de sécurité Microsoft telles que Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365 et Microsoft 365 Defender apparaissent dans cette section.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-138">Alerts from different Microsoft security solutions like Microsoft Defender for Endpoint, Microsoft Defender for Office 365, and Microsoft 365 Defender appear in this section.</span></span> 

![Image de l’exemple de page d’alerte](../../media/unified-alert-queue.png)

<span data-ttu-id="0f0c9-140">La file d’attente Alertes affiche la liste des alertes qui ont été signalées dans votre réseau.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-140">The Alerts queue shows a list of alerts that were flagged in your network.</span></span> <span data-ttu-id="0f0c9-141">Par défaut, la file d’attente affiche les alertes visibles au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-141">By default, the queue displays alerts seen in the last 30 days.</span></span> <span data-ttu-id="0f0c9-142">Les alertes les plus récentes sont affichées en haut de la liste pour vous aider à voir les alertes les plus récentes en premier.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-142">The most recent alerts are shown at the top of the list helping you see the most recent alerts first.</span></span>

> [!NOTE]
> <span data-ttu-id="0f0c9-143">Au moment du lancement, la file d’attente des alertes unifiées ne dispose que de 7 jours d’alertes Microsoft Defender pour Office 365 disponibles.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-143">At the time of launch, the unified alerts queue will only have 7 days’ worth of Microsoft Defender for Office 365 alerts available.</span></span> <span data-ttu-id="0f0c9-144">La file d’attente continuera à se développer au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="0f0c9-144">The queue will continue to build over time.</span></span> <span data-ttu-id="0f0c9-145">Si vous devez trier les alertes avant le lancement de la file d’attente des alertes unifiées, utilisez la file d’attente des alertes dans le Centre de sécurité [et conformité.](https://protection.office.com/viewalerts)</span><span class="sxs-lookup"><span data-stu-id="0f0c9-145">If you need to triage alerts prior to the launch of the unified alerts queue, use the alerts queue in the [Security and Compliance Center](https://protection.office.com/viewalerts).</span></span>


<span data-ttu-id="0f0c9-146">Dans la barre de navigation supérieure, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="0f0c9-146">On the top navigation, you can:</span></span>

- <span data-ttu-id="0f0c9-147">Appliquer des filtres</span><span class="sxs-lookup"><span data-stu-id="0f0c9-147">Apply filters</span></span>
- <span data-ttu-id="0f0c9-148">Personnaliser des colonnes pour ajouter ou supprimer des colonnes</span><span class="sxs-lookup"><span data-stu-id="0f0c9-148">Customize columns to add or remove columns</span></span>
- <span data-ttu-id="0f0c9-149">Exporter des données</span><span class="sxs-lookup"><span data-stu-id="0f0c9-149">Export data</span></span>

<span data-ttu-id="0f0c9-150">Vous pouvez également filtrer les alertes en fonction de différents critères :</span><span class="sxs-lookup"><span data-stu-id="0f0c9-150">You can also filter alerts according to different criteria:</span></span>

- <span data-ttu-id="0f0c9-151">Severity</span><span class="sxs-lookup"><span data-stu-id="0f0c9-151">Severity</span></span>
- <span data-ttu-id="0f0c9-152">Statut</span><span class="sxs-lookup"><span data-stu-id="0f0c9-152">Status</span></span>
- <span data-ttu-id="0f0c9-153">Catégorie</span><span class="sxs-lookup"><span data-stu-id="0f0c9-153">Category</span></span>
- <span data-ttu-id="0f0c9-154">Source de détection</span><span class="sxs-lookup"><span data-stu-id="0f0c9-154">Detection source</span></span>
- <span data-ttu-id="0f0c9-155">Stratégie</span><span class="sxs-lookup"><span data-stu-id="0f0c9-155">Policy</span></span>
- <span data-ttu-id="0f0c9-156">Ressources impactées</span><span class="sxs-lookup"><span data-stu-id="0f0c9-156">Impacted assets</span></span>
- <span data-ttu-id="0f0c9-157">Première activité</span><span class="sxs-lookup"><span data-stu-id="0f0c9-157">First activity</span></span>
- <span data-ttu-id="0f0c9-158">Dernière activité</span><span class="sxs-lookup"><span data-stu-id="0f0c9-158">Last activity</span></span>


<span data-ttu-id="0f0c9-159">Pour démarrer une enquête sur un incident, [lisez Examiner les incidents dans Microsoft 365 Defender](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="0f0c9-159">To start an investigation on an incident, read [Investigate incidents in Microsoft 365 Defender](investigate-incidents.md)</span></span>
## <a name="see-also"></a><span data-ttu-id="0f0c9-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f0c9-160">See also</span></span>

- [<span data-ttu-id="0f0c9-161">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="0f0c9-161">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="0f0c9-162">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="0f0c9-162">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="0f0c9-163">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="0f0c9-163">Manage incidents</span></span>](manage-incidents.md)
