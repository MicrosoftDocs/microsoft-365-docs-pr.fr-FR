---
title: Examiner les incidents dans Microsoft Defender pour le point de terminaison
description: Voir les alertes associées, gérer l'incident et consulter les métadonnées d'alerte pour vous aider à examiner un incident
keywords: examiner, incident, alertes, métadonnées, risque, source de détection, appareils affectés, modèles, corrélation
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
- m365initiative-defender-endpoint
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 1d8f4452273047684a30db3b18d1281f40f46378
ms.sourcegitcommit: 13ce4b31303a1a21ca53700a54bcf8d91ad2f8c1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51903297"
---
# <a name="investigate-incidents-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="93fa4-104">Examiner les incidents dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="93fa4-104">Investigate incidents in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="93fa4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="93fa4-105">**Applies to:**</span></span>
- [<span data-ttu-id="93fa4-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="93fa4-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="93fa4-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="93fa4-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


<span data-ttu-id="93fa4-108">Examinez les incidents qui affectent votre réseau, comprenez ce qu'ils signifient et rassemblez des preuves pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="93fa4-108">Investigate incidents that affect your network, understand what they mean, and collate evidence to resolve them.</span></span> 

<span data-ttu-id="93fa4-109">Lorsque vous examinez un incident, vous voyez :</span><span class="sxs-lookup"><span data-stu-id="93fa4-109">When you investigate an incident, you'll see:</span></span>
- <span data-ttu-id="93fa4-110">Détails de l’incident</span><span class="sxs-lookup"><span data-stu-id="93fa4-110">Incident details</span></span>
- <span data-ttu-id="93fa4-111">Commentaires et actions sur les incidents</span><span class="sxs-lookup"><span data-stu-id="93fa4-111">Incident comments and actions</span></span>
- <span data-ttu-id="93fa4-112">Onglets (alertes, appareils, enquêtes, preuves, graphique)</span><span class="sxs-lookup"><span data-stu-id="93fa4-112">Tabs (alerts, devices, investigations, evidence, graph)</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4qLUV]


## <a name="analyze-incident-details"></a><span data-ttu-id="93fa4-113">Analyser les détails de l'incident</span><span class="sxs-lookup"><span data-stu-id="93fa4-113">Analyze incident details</span></span> 
<span data-ttu-id="93fa4-114">Cliquez sur un incident pour voir le **volet Incident.**</span><span class="sxs-lookup"><span data-stu-id="93fa4-114">Click an incident to see the **Incident pane**.</span></span> <span data-ttu-id="93fa4-115">Sélectionnez **Ouvrir la page Incident** pour voir les détails de l'incident et les informations connexes (alertes, périphériques, enquêtes, preuves, graphique).</span><span class="sxs-lookup"><span data-stu-id="93fa4-115">Select **Open incident page** to see the incident details and related information (alerts, devices, investigations, evidence, graph).</span></span> 

![Image des détails de l'incident1](images/atp-incident-details.png)

### <a name="alerts"></a><span data-ttu-id="93fa4-117">Alertes</span><span class="sxs-lookup"><span data-stu-id="93fa4-117">Alerts</span></span>
<span data-ttu-id="93fa4-118">Vous pouvez examiner les alertes et voir comment elles ont été liées dans un incident.</span><span class="sxs-lookup"><span data-stu-id="93fa4-118">You can investigate the alerts and see how they were linked together in an incident.</span></span> <span data-ttu-id="93fa4-119">Les alertes sont regroupées en incidents pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="93fa4-119">Alerts are grouped into incidents based on the following reasons:</span></span>
- <span data-ttu-id="93fa4-120">Examen automatisé : l'examen automatisé a déclenché l'alerte liée lors de l'examen de l'alerte d'origine</span><span class="sxs-lookup"><span data-stu-id="93fa4-120">Automated investigation - The automated investigation triggered the linked alert while investigating the original alert</span></span> 
- <span data-ttu-id="93fa4-121">Caractéristiques de fichier : les fichiers associés à l'alerte ont des caractéristiques similaires</span><span class="sxs-lookup"><span data-stu-id="93fa4-121">File characteristics - The files associated with the alert have similar characteristics</span></span>
- <span data-ttu-id="93fa4-122">Association manuelle : un utilisateur a lié manuellement les alertes</span><span class="sxs-lookup"><span data-stu-id="93fa4-122">Manual association - A user manually linked the alerts</span></span>
- <span data-ttu-id="93fa4-123">Durée immédiate : les alertes ont été déclenchées sur le même appareil au cours d'une certaine période</span><span class="sxs-lookup"><span data-stu-id="93fa4-123">Proximate time - The alerts were triggered on the same device within a certain timeframe</span></span>
- <span data-ttu-id="93fa4-124">Même fichier : les fichiers associés à l'alerte sont exactement les mêmes</span><span class="sxs-lookup"><span data-stu-id="93fa4-124">Same file - The files associated with the alert are exactly the same</span></span>
- <span data-ttu-id="93fa4-125">MÊME URL : l'URL qui a déclenché l'alerte est exactement la même</span><span class="sxs-lookup"><span data-stu-id="93fa4-125">Same URL - The URL that triggered the alert is exactly the same</span></span>

![Image de l'onglet Alertes avec page détails de l'incident indiquant les raisons pour lesquelles les alertes ont été liées dans cet incident](images/atp-incidents-alerts-reason.png)

<span data-ttu-id="93fa4-127">Vous pouvez également gérer une alerte et voir les métadonnées d'alerte ainsi que d'autres informations.</span><span class="sxs-lookup"><span data-stu-id="93fa4-127">You can also manage an alert and see alert metadata along with other information.</span></span> <span data-ttu-id="93fa4-128">Pour plus d'informations, voir [Examiner les alertes.](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="93fa4-128">For more information, see [Investigate alerts](investigate-alerts.md).</span></span> 

### <a name="devices"></a><span data-ttu-id="93fa4-129">Appareils</span><span class="sxs-lookup"><span data-stu-id="93fa4-129">Devices</span></span>
<span data-ttu-id="93fa4-130">Vous pouvez également examiner les appareils qui font partie d'un incident donné ou y sont liés.</span><span class="sxs-lookup"><span data-stu-id="93fa4-130">You can also investigate the devices that are part of, or related to, a given incident.</span></span> <span data-ttu-id="93fa4-131">Pour plus d'informations, voir [Examiner les appareils.](investigate-machines.md)</span><span class="sxs-lookup"><span data-stu-id="93fa4-131">For more information, see [Investigate devices](investigate-machines.md).</span></span>

![Image de l'onglet Appareils dans la page détails de l'incident](images/atp-incident-device-tab.png)

### <a name="investigations"></a><span data-ttu-id="93fa4-133">Examens</span><span class="sxs-lookup"><span data-stu-id="93fa4-133">Investigations</span></span>
<span data-ttu-id="93fa4-134">Sélectionnez **Examens** pour voir toutes les enquêtes automatiques lancées par le système en réponse aux alertes d'incident.</span><span class="sxs-lookup"><span data-stu-id="93fa4-134">Select **Investigations** to see all the automatic investigations launched by the system in response to the incident alerts.</span></span>

![Image de l'onglet Enquêtes dans la page détails de l'incident](images/atp-incident-investigations-tab.png)

## <a name="going-through-the-evidence"></a><span data-ttu-id="93fa4-136">Passer en travers de la preuve</span><span class="sxs-lookup"><span data-stu-id="93fa4-136">Going through the evidence</span></span>
<span data-ttu-id="93fa4-137">Microsoft Defender pour le point de terminaison examine automatiquement tous les événements pris en charge par les incidents et les entités suspectes dans les alertes, en vous fournissant des réponse automatiques et des informations sur les fichiers, processus, services et bien plus encore importants.</span><span class="sxs-lookup"><span data-stu-id="93fa4-137">Microsoft Defender for Endpoint automatically investigates all the incidents' supported events and suspicious entities in the alerts, providing you with autoresponse and information about the important files, processes, services, and more.</span></span> 

<span data-ttu-id="93fa4-138">Chacune des entités analysées sera marquée comme infectée, corrigé ou suspect.</span><span class="sxs-lookup"><span data-stu-id="93fa4-138">Each of the analyzed entities will be marked as infected, remediated, or suspicious.</span></span> 

![Image de l'onglet Preuve dans la page détails de l'incident](images/atp-incident-evidence-tab.png)

## <a name="visualizing-associated-cybersecurity-threats"></a><span data-ttu-id="93fa4-140">Visualisation des menaces de cybersécurité associées</span><span class="sxs-lookup"><span data-stu-id="93fa4-140">Visualizing associated cybersecurity threats</span></span> 
<span data-ttu-id="93fa4-141">Microsoft Defender pour le point de terminaison regroupe les informations sur les menaces dans un incident afin que vous pouvez voir les modèles et corrélations provenant de différents points de données.</span><span class="sxs-lookup"><span data-stu-id="93fa4-141">Microsoft Defender for Endpoint aggregates the threat information into an incident so you can see the patterns and correlations coming in from various data points.</span></span> <span data-ttu-id="93fa4-142">Vous pouvez afficher cette corrélation via le graphique d'incident.</span><span class="sxs-lookup"><span data-stu-id="93fa4-142">You can view such correlation through the incident graph.</span></span>

### <a name="incident-graph"></a><span data-ttu-id="93fa4-143">Graphique d'incident</span><span class="sxs-lookup"><span data-stu-id="93fa4-143">Incident graph</span></span>
<span data-ttu-id="93fa4-144">Graph **présente** l'histoire des attaques de cybersécurité.</span><span class="sxs-lookup"><span data-stu-id="93fa4-144">The **Graph** tells the story of the cybersecurity attack.</span></span> <span data-ttu-id="93fa4-145">Par exemple, il vous montre quel était le point d'entrée, quel indicateur de compromission ou d'activité a été observé sur quel appareil.</span><span class="sxs-lookup"><span data-stu-id="93fa4-145">For example, it shows you what was the entry point, which indicator of compromise or activity was observed on which device.</span></span> <span data-ttu-id="93fa4-146">etc.</span><span class="sxs-lookup"><span data-stu-id="93fa4-146">etc.</span></span>

![Image du graphique d'incident](images/atp-incident-graph-tab.png)

<span data-ttu-id="93fa4-148">Vous pouvez cliquer sur les cercles sur le graphique d'incident pour afficher les détails des fichiers malveillants, les détections de fichiers associées, le nombre d'instances dans le monde entier, si elle a été observée dans votre organisation, si c'est le cas, le nombre d'instances.</span><span class="sxs-lookup"><span data-stu-id="93fa4-148">You can click the circles on the incident graph to view the details of the malicious files, associated file detections, how many instances have there been worldwide, whether it’s been observed in your organization, if so, how many instances.</span></span>

![Image des détails de l'incident](images/atp-incident-graph-details.png)

## <a name="related-topics"></a><span data-ttu-id="93fa4-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93fa4-150">Related topics</span></span>
- [<span data-ttu-id="93fa4-151">File d’attente des incidents</span><span class="sxs-lookup"><span data-stu-id="93fa4-151">Incidents queue</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/view-incidents-queue)
- [<span data-ttu-id="93fa4-152">Examiner les incidents dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="93fa4-152">Investigate incidents in Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/investigate-incidents)
- [<span data-ttu-id="93fa4-153">Gérer Microsoft Defender pour les incidents de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="93fa4-153">Manage Microsoft Defender for Endpoint incidents</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/manage-incidents)
