---
title: Examiner Microsoft Defender pour les domaines de point de terminaison
description: Utilisez les options d’examen pour déterminer si les appareils et les serveurs communiquent avec des domaines malveillants.
keywords: examiner le domaine, le domaine, le domaine malveillant, Microsoft Defender pour le point de terminaison, alerte, URL
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
ms.topic: article
ms.date: 04/24/2018
ms.technology: mde
ms.openlocfilehash: 7826229ba67384137c033745a5b85e557fc9c4a7
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933468"
---
# <a name="investigate-a-domain-associated-with-a-microsoft-defender-for-endpoint-alert"></a><span data-ttu-id="ea480-104">Examiner un domaine associé à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ea480-104">Investigate a domain associated with a Microsoft Defender for Endpoint alert</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="ea480-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ea480-105">**Applies to:**</span></span>
- [<span data-ttu-id="ea480-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ea480-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="ea480-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ea480-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="ea480-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="ea480-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="ea480-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ea480-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigatedomain-abovefoldlink) 

<span data-ttu-id="ea480-110">Examinez un domaine pour voir si les appareils et les serveurs de votre réseau d’entreprise communiquent avec un domaine malveillant connu.</span><span class="sxs-lookup"><span data-stu-id="ea480-110">Investigate a domain to see if devices and servers in your enterprise network have been communicating with a known malicious domain.</span></span>

<span data-ttu-id="ea480-111">Vous pouvez examiner un domaine à l’aide de la fonctionnalité de recherche ou en cliquant sur un lien de domaine à partir de la chronologie **de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="ea480-111">You can investigate a domain by using the search feature or by clicking on a domain link from the **Device timeline**.</span></span>

<span data-ttu-id="ea480-112">Vous pouvez voir les informations des sections suivantes dans l’affichage URL :</span><span class="sxs-lookup"><span data-stu-id="ea480-112">You can see information from the following sections in the URL view:</span></span>

- <span data-ttu-id="ea480-113">Détails de l’URL, Contacts, Serveurs de noms</span><span class="sxs-lookup"><span data-stu-id="ea480-113">URL details, Contacts, Nameservers</span></span>
- <span data-ttu-id="ea480-114">Alertes associées à cette URL</span><span class="sxs-lookup"><span data-stu-id="ea480-114">Alerts related to this URL</span></span> 
- <span data-ttu-id="ea480-115">URL dans l’organisation</span><span class="sxs-lookup"><span data-stu-id="ea480-115">URL in organization</span></span>
- <span data-ttu-id="ea480-116">Appareils les plus récemment observés avec UNE URL</span><span class="sxs-lookup"><span data-stu-id="ea480-116">Most recent observed devices with URL</span></span>

## <a name="url-worldwide"></a><span data-ttu-id="ea480-117">URL dans le monde entier</span><span class="sxs-lookup"><span data-stu-id="ea480-117">URL worldwide</span></span>

<span data-ttu-id="ea480-118">La section **URL dans le** monde entier répertorie l’URL, un lien vers d’autres détails sur Whois, le nombre d’incidents ouverts connexes et le nombre d’alertes actives.</span><span class="sxs-lookup"><span data-stu-id="ea480-118">The **URL Worldwide** section lists the URL, a link to further details at Whois, the number of related open incidents, and the number of active alerts.</span></span>

## <a name="incident"></a><span data-ttu-id="ea480-119">Incident</span><span class="sxs-lookup"><span data-stu-id="ea480-119">Incident</span></span>

<span data-ttu-id="ea480-120">La **carte Incident** affiche un graphique à barres de toutes les alertes actives dans les incidents au cours des 180 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="ea480-120">The **Incident** card displays a bar chart of all active alerts in incidents over the past 180 days.</span></span>

## <a name="prevalence"></a><span data-ttu-id="ea480-121">Prévalence</span><span class="sxs-lookup"><span data-stu-id="ea480-121">Prevalence</span></span>

<span data-ttu-id="ea480-122">La **carte de** prévalence fournit des détails sur la prévalence de l’URL au sein de l’organisation, sur une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ea480-122">The **Prevalence** card provides details on the prevalence of the URL within the organization, over a specified period of time.</span></span>

<span data-ttu-id="ea480-123">Bien que la période par défaut soit les 30 derniers jours, vous pouvez personnaliser la plage en sélectionnant la flèche pointant vers le bas dans le coin de la carte.</span><span class="sxs-lookup"><span data-stu-id="ea480-123">Although the default time period is the past 30 days, you can customize the range by selecting the downward-pointing arrow in the corner of the card.</span></span> <span data-ttu-id="ea480-124">La plage la plus courte disponible est pour la prévalence au cours du dernier jour, tandis que la plage la plus longue se trouve sur les 6 derniers mois.</span><span class="sxs-lookup"><span data-stu-id="ea480-124">The shortest range available is for prevalence over the past day, while the longest range is over the past 6 months.</span></span>

## <a name="alerts"></a><span data-ttu-id="ea480-125">Alertes</span><span class="sxs-lookup"><span data-stu-id="ea480-125">Alerts</span></span>

<span data-ttu-id="ea480-126">**L’onglet Alertes** fournit une liste des alertes associées à l’URL.</span><span class="sxs-lookup"><span data-stu-id="ea480-126">The **Alerts** tab provides a list of alerts that are associated with the URL.</span></span> <span data-ttu-id="ea480-127">Le tableau présenté ici est une version filtrée des alertes visible sur l’écran de file d’attente des alertes, affichant uniquement les alertes associées au domaine, leur gravité, leur état, l’incident associé, la classification, l’état de l’enquête, etc.</span><span class="sxs-lookup"><span data-stu-id="ea480-127">The table shown here is a filtered version of the alerts visible on the Alert queue screen, showing only alerts associated with the domain, their severity, status, the associated incident, classification, investigation state, and more.</span></span>

<span data-ttu-id="ea480-128">L’onglet Alertes peut être ajusté pour afficher plus  ou moins d’informations, en sélectionnant Personnaliser les colonnes dans le menu Actions au-dessus des en-têtes de colonne.</span><span class="sxs-lookup"><span data-stu-id="ea480-128">The Alerts tab can be adjusted to show more or less information, by selecting **Customize columns** from the action menu above the column headers.</span></span> <span data-ttu-id="ea480-129">Le nombre d’éléments affichés peut également être ajusté en sélectionnant des **éléments par page** dans le même menu.</span><span class="sxs-lookup"><span data-stu-id="ea480-129">The number of items displayed can also be adjusted, by selecting **items per page** on the same menu.</span></span>

## <a name="observed-in-organization"></a><span data-ttu-id="ea480-130">Observé dans l’organisation</span><span class="sxs-lookup"><span data-stu-id="ea480-130">Observed in organization</span></span>

<span data-ttu-id="ea480-131">**L’onglet Observé dans l’organisation** fournit une vue chronologique des événements et des alertes associées qui ont été observés sur l’URL.</span><span class="sxs-lookup"><span data-stu-id="ea480-131">The **Observed in organization** tab provides a chronological view on the events and associated alerts that were observed on the URL.</span></span> <span data-ttu-id="ea480-132">Cet onglet inclut une chronologie et un tableau personnalisable répertoriant les détails des événements, tels que l’heure, l’appareil et une brève description de ce qui s’est passé.</span><span class="sxs-lookup"><span data-stu-id="ea480-132">This tab includes a timeline and a customizable table listing event details, such as the time, device, and a brief description of what happened.</span></span> 

<span data-ttu-id="ea480-133">Vous pouvez afficher les événements de différentes périodes en entrant les dates dans les champs de texte au-dessus des en-têtes de tableau.</span><span class="sxs-lookup"><span data-stu-id="ea480-133">You can view events from different periods of time by entering the dates into the text fields above the table headers.</span></span> <span data-ttu-id="ea480-134">Vous pouvez également personnaliser l’plage de temps en sélectionnant différentes zones de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="ea480-134">You can also customize the time range by selecting different areas of the timeline.</span></span>

<span data-ttu-id="ea480-135">**Examinez un domaine :**</span><span class="sxs-lookup"><span data-stu-id="ea480-135">**Investigate a domain:**</span></span>

1. <span data-ttu-id="ea480-136">Sélectionnez **l’URL** dans le menu déroulant **de** la barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="ea480-136">Select **URL** from the **Search bar** drop-down menu.</span></span>
2. <span data-ttu-id="ea480-137">Entrez l’URL dans le **champ** Recherche.</span><span class="sxs-lookup"><span data-stu-id="ea480-137">Enter the URL in the **Search** field.</span></span>
3. <span data-ttu-id="ea480-138">Cliquez sur l’icône de recherche ou appuyez sur **Entrée.**</span><span class="sxs-lookup"><span data-stu-id="ea480-138">Click the search icon   or press **Enter**.</span></span> <span data-ttu-id="ea480-139">Des détails sur l’URL sont affichés.</span><span class="sxs-lookup"><span data-stu-id="ea480-139">Details about the URL are displayed.</span></span> <span data-ttu-id="ea480-140">Remarque : les résultats de la recherche seront renvoyés uniquement pour les URL observées dans les communications à partir d’appareils de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ea480-140">Note: search results will only be returned for URLs observed in communications from devices in the organization.</span></span>
4. <span data-ttu-id="ea480-141">Utilisez les filtres de recherche pour définir les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="ea480-141">Use the search filters to define the search criteria.</span></span> <span data-ttu-id="ea480-142">Vous pouvez également utiliser la zone de recherche de chronologie pour filtrer les résultats affichés de tous les appareils de l’organisation observés en communication avec l’URL, le fichier associé à la communication et la dernière date observée.</span><span class="sxs-lookup"><span data-stu-id="ea480-142">You can also use the timeline search box to filter the displayed results of all devices in the organization observed communicating with the URL, the file associated with the communication and the last date observed.</span></span>
5. <span data-ttu-id="ea480-143">En cliquant sur l’un des noms d’appareils, vous pouvez continuer à examiner les alertes, comportements et événements signalés.</span><span class="sxs-lookup"><span data-stu-id="ea480-143">Clicking any of the device names will take you to that device's view, where you can continue investigate reported alerts, behaviors, and events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea480-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea480-144">Related topics</span></span>
- [<span data-ttu-id="ea480-145">Afficher et organiser la file d’attente des alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ea480-145">View and organize the Microsoft Defender for Endpoint Alerts queue</span></span>](alerts-queue.md)
- [<span data-ttu-id="ea480-146">Gérer les alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ea480-146">Manage Microsoft Defender for Endpoint alerts</span></span>](manage-alerts.md)
- [<span data-ttu-id="ea480-147">Examiner microsoft Defender pour les alertes de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ea480-147">Investigate Microsoft Defender for Endpoint alerts</span></span>](investigate-alerts.md)
- [<span data-ttu-id="ea480-148">Examiner un fichier associé à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ea480-148">Investigate a file associated with a Microsoft Defender for Endpoint alert</span></span>](investigate-files.md)
- [<span data-ttu-id="ea480-149">Examiner les appareils de la liste Microsoft Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ea480-149">Investigate devices in the Microsoft Defender for Endpoint Devices list</span></span>](investigate-machines.md)
- [<span data-ttu-id="ea480-150">Examiner une adresse IP associée à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ea480-150">Investigate an IP address associated with a Microsoft Defender for Endpoint alert</span></span>](investigate-ip.md)
- [<span data-ttu-id="ea480-151">Examiner un compte d’utilisateur dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ea480-151">Investigate a user account in Microsoft Defender for Endpoint</span></span>](investigate-user.md)
