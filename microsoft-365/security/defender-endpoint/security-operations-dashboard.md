---
title: Centre de sécurité Microsoft Defender Tableau de bord opérations de sécurité
description: Utilisez le tableau de bord pour identifier les appareils à risque, suivre l’état du service et consulter les statistiques et les informations sur les appareils et les alertes.
keywords: tableau de bord, alertes, nouveau, en cours, résolu, risque, appareils à risque, infections, rapports, statistiques, graphiques, graphiques, santé, détections de programmes malveillants actifs, catégorie de menace, catégories, programme de vol de mot de passe, ransomware, exploit, menace, faible gravité, programmes malveillants actifs
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
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: bfa23138b1bab4abcdfa0b4b9d689a4a4cfc7fc1
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064913"
---
# <a name="microsoft-defender-security-center-security-operations-dashboard"></a><span data-ttu-id="ca190-104">Centre de sécurité Microsoft Defender Tableau de bord opérations de sécurité</span><span class="sxs-lookup"><span data-stu-id="ca190-104">Microsoft Defender Security Center Security operations dashboard</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="ca190-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ca190-105">**Applies to:**</span></span>
- [<span data-ttu-id="ca190-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ca190-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

><span data-ttu-id="ca190-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ca190-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="ca190-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ca190-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-secopsdashboard-abovefoldlink) 

<span data-ttu-id="ca190-109">Le **tableau de bord Opérations** de sécurité est l’endroit protection évolutive des points de terminaison fonctionnalités de sécurité sont à l’écran.</span><span class="sxs-lookup"><span data-stu-id="ca190-109">The **Security operations dashboard** is where the endpoint detection and response capabilities are surfaced.</span></span> <span data-ttu-id="ca190-110">Il fournit une vue d’ensemble de l’endroit où les détections ont été détectées et met en évidence les cas où des actions de réponse sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ca190-110">It provides a high level overview of where detections were seen and highlights where response actions are needed.</span></span> 

<span data-ttu-id="ca190-111">Le tableau de bord affiche une capture instantanée des éléments ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ca190-111">The dashboard displays a snapshot of:</span></span>

- <span data-ttu-id="ca190-112">Alertes actives</span><span class="sxs-lookup"><span data-stu-id="ca190-112">Active alerts</span></span>
- <span data-ttu-id="ca190-113">Appareils à risque</span><span class="sxs-lookup"><span data-stu-id="ca190-113">Devices at risk</span></span>
- <span data-ttu-id="ca190-114">État du capteur</span><span class="sxs-lookup"><span data-stu-id="ca190-114">Sensor health</span></span>
- <span data-ttu-id="ca190-115">L’intégrité du service</span><span class="sxs-lookup"><span data-stu-id="ca190-115">Service health</span></span>
- <span data-ttu-id="ca190-116">Rapports quotidiens sur les appareils</span><span class="sxs-lookup"><span data-stu-id="ca190-116">Daily devices reporting</span></span>
- <span data-ttu-id="ca190-117">Examens automatisés actifs</span><span class="sxs-lookup"><span data-stu-id="ca190-117">Active automated investigations</span></span>
- <span data-ttu-id="ca190-118">Statistiques d’enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="ca190-118">Automated investigations statistics</span></span>
- <span data-ttu-id="ca190-119">Utilisateurs à risque</span><span class="sxs-lookup"><span data-stu-id="ca190-119">Users at risk</span></span>
- <span data-ttu-id="ca190-120">Activités suspectes</span><span class="sxs-lookup"><span data-stu-id="ca190-120">Suspicious activities</span></span>


![Image du tableau de bord Opérations de sécurité](images/atp-sec-ops-dashboard.png)

<span data-ttu-id="ca190-122">Vous pouvez explorer et examiner les alertes et les appareils pour déterminer rapidement si, où et quand des activités suspectes se sont produites dans votre réseau pour vous aider à comprendre le contexte dans lequel elles sont apparues.</span><span class="sxs-lookup"><span data-stu-id="ca190-122">You can explore and investigate alerts and devices to quickly determine if, where, and when suspicious activities occurred in your network to help you understand the context they appeared in.</span></span>

<span data-ttu-id="ca190-123">À partir du **tableau de bord Opérations** de sécurité, vous verrez des événements agrégés pour faciliter l’identification d’événements ou de comportements significatifs sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="ca190-123">From the **Security operations dashboard** you will see aggregated events to facilitate the identification of significant events or behaviors on a device.</span></span> <span data-ttu-id="ca190-124">Vous pouvez également descendre dans les événements granulaires et les indicateurs de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="ca190-124">You can also drill down into granular events and low-level indicators.</span></span>

<span data-ttu-id="ca190-125">Il dispose également de vignettes cliquables qui donnent des indications visuelles sur l’état d’état général de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ca190-125">It also has clickable tiles that give visual cues on the overall health state of your organization.</span></span> <span data-ttu-id="ca190-126">Chaque vignette ouvre une vue détaillée de la vue d’ensemble correspondante.</span><span class="sxs-lookup"><span data-stu-id="ca190-126">Each tile opens a detailed view of the corresponding overview.</span></span>

## <a name="active-alerts"></a><span data-ttu-id="ca190-127">Alertes actives</span><span class="sxs-lookup"><span data-stu-id="ca190-127">Active alerts</span></span>
<span data-ttu-id="ca190-128">Vous pouvez afficher le nombre global d’alertes actives des 30 derniers jours de votre réseau à partir de la vignette.</span><span class="sxs-lookup"><span data-stu-id="ca190-128">You can view the overall number of active alerts from the last 30 days in your network from the tile.</span></span> <span data-ttu-id="ca190-129">Les alertes sont regroupées en **nouveautés** **et en cours.**</span><span class="sxs-lookup"><span data-stu-id="ca190-129">Alerts are grouped into **New** and **In progress**.</span></span>

![Cliquez sur chaque tranche ou gravité pour voir la liste des alertes des 30 derniers jours](images/active-alerts-tile.png)

<span data-ttu-id="ca190-131">Chaque groupe est sous-classé selon les niveaux de gravité d’alerte correspondants.</span><span class="sxs-lookup"><span data-stu-id="ca190-131">Each group is further sub-categorized into their corresponding alert severity levels.</span></span> <span data-ttu-id="ca190-132">Cliquez sur le nombre d’alertes à l’intérieur de chaque anneau d’alerte pour afficher un affichage trié de la file d’attente de cette catégorie **(nouveau** ou **en cours).**</span><span class="sxs-lookup"><span data-stu-id="ca190-132">Click the number of alerts inside each alert ring to see a sorted view of that category's queue (**New** or **In progress**).</span></span>

<span data-ttu-id="ca190-133">Pour plus d’informations, voir [la vue d’ensemble des alertes.](alerts-queue.md)</span><span class="sxs-lookup"><span data-stu-id="ca190-133">For more information see, [Alerts overview](alerts-queue.md).</span></span>

<span data-ttu-id="ca190-134">Chaque ligne inclut une catégorie de gravité d’alerte et une brève description de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="ca190-134">Each row includes an alert severity category and a short description of the alert.</span></span> <span data-ttu-id="ca190-135">Vous pouvez cliquer sur une alerte pour afficher sa vue détaillée.</span><span class="sxs-lookup"><span data-stu-id="ca190-135">You can click an alert to see its detailed view.</span></span> <span data-ttu-id="ca190-136">Pour plus d’informations, [consultez La vue d’ensemble](investigate-alerts.md) de Microsoft Defender pour les alertes de point de [terminaison et les alertes.](alerts-queue.md)</span><span class="sxs-lookup"><span data-stu-id="ca190-136">For more information see,  [Investigate Microsoft Defender for Endpoint alerts](investigate-alerts.md) and [Alerts overview](alerts-queue.md).</span></span>


## <a name="devices-at-risk"></a><span data-ttu-id="ca190-137">Appareils à risque</span><span class="sxs-lookup"><span data-stu-id="ca190-137">Devices at risk</span></span>
<span data-ttu-id="ca190-138">Cette vignette affiche la liste des appareils avec le plus grand nombre d’alertes actives.</span><span class="sxs-lookup"><span data-stu-id="ca190-138">This tile shows you a list of devices with the highest number of active alerts.</span></span> <span data-ttu-id="ca190-139">Le nombre total d’alertes pour chaque appareil est affiché dans un cercle en regard du nom de l’appareil, puis classé par niveaux de gravité à l’extrémité de la vignette (placez le pointage sur chaque barre de gravité pour voir son étiquette).</span><span class="sxs-lookup"><span data-stu-id="ca190-139">The total number of alerts for each device is shown in a circle next to the device name, and then further categorized by severity levels at the far end of the tile (hover over each severity bar to see its label).</span></span>

![La vignette Appareils à risque affiche la liste des appareils avec le plus grand nombre d’alertes et une répartition de la gravité des alertes.](images/devices-at-risk-tile.png)

<span data-ttu-id="ca190-141">Cliquez sur le nom de l’appareil pour voir les détails sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="ca190-141">Click the name of the device to see details about that device.</span></span> <span data-ttu-id="ca190-142">Pour plus d’informations, consultez la liste Examiner les appareils de la liste [Microsoft Defender pour les appareils de point de terminaison.](investigate-machines.md)</span><span class="sxs-lookup"><span data-stu-id="ca190-142">For more information see, [Investigate devices in the Microsoft Defender for Endpoint Devices list](investigate-machines.md).</span></span>

<span data-ttu-id="ca190-143">Vous pouvez également cliquer sur **La** liste Appareils en haut de la vignette pour aller directement à la liste **Appareils,** triée par le nombre d’alertes actives.</span><span class="sxs-lookup"><span data-stu-id="ca190-143">You can also click **Devices list** at the top of the tile to go directly to the **Devices list**, sorted by the number of active alerts.</span></span> <span data-ttu-id="ca190-144">Pour plus d’informations, consultez la liste Examiner les appareils de la liste [Microsoft Defender pour les appareils de point de terminaison.](investigate-machines.md)</span><span class="sxs-lookup"><span data-stu-id="ca190-144">For more information see, [Investigate devices in the Microsoft Defender for Endpoint Devices list](investigate-machines.md).</span></span>

## <a name="devices-with-sensor-issues"></a><span data-ttu-id="ca190-145">Appareils avec des problèmes de capteur</span><span class="sxs-lookup"><span data-stu-id="ca190-145">Devices with sensor issues</span></span>
<span data-ttu-id="ca190-146">La **vignette Appareils avec problèmes** de capteur fournit des informations sur la capacité de chaque appareil à fournir des données de capteur au service Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="ca190-146">The **Devices with sensor issues** tile provides information on the individual device’s ability to provide sensor data to the Microsoft Defender for Endpoint service.</span></span> <span data-ttu-id="ca190-147">Il indique le nombre d’appareils qui nécessitent une attention particulière et vous aide à identifier les appareils problématiques.</span><span class="sxs-lookup"><span data-stu-id="ca190-147">It reports how many devices require attention and helps you identify problematic devices.</span></span>

![Vignette des appareils avec problèmes de capteur](images/atp-tile-sensor-health.png)

<span data-ttu-id="ca190-149">Deux indicateurs d’état fournissent des informations sur le nombre d’appareils qui ne sont pas correctement signalés au service :</span><span class="sxs-lookup"><span data-stu-id="ca190-149">There are two status indicators that provide information on the number of devices that are not reporting properly to the service:</span></span>
- <span data-ttu-id="ca190-150">**Mal configurés** : ces appareils peuvent signaler partiellement des données de capteur au service Microsoft Defender for Endpoint et peuvent avoir des erreurs de configuration qui doivent être corrigées.</span><span class="sxs-lookup"><span data-stu-id="ca190-150">**Misconfigured** – These devices might partially be reporting sensor data to the Microsoft Defender for Endpoint service and might have configuration errors that need to be corrected.</span></span>
- <span data-ttu-id="ca190-151">**Inactif** : appareils qui ont cessé de signaler au service Microsoft Defender for Endpoint pendant plus de sept jours au cours du mois précédent.</span><span class="sxs-lookup"><span data-stu-id="ca190-151">**Inactive** - Devices that have stopped reporting to the Microsoft Defender for Endpoint service for more than seven days in the past month.</span></span>

<span data-ttu-id="ca190-152">Lorsque vous cliquez sur l’un des groupes, vous êtes dirigé vers la liste des appareils, filtré en fonction de votre choix.</span><span class="sxs-lookup"><span data-stu-id="ca190-152">When you click any of the groups, you’ll be directed to devices list, filtered according to your choice.</span></span> <span data-ttu-id="ca190-153">Pour plus d’informations, voir [Vérifier l’état du capteur](check-sensor-status.md) et Examiner les [appareils.](investigate-machines.md)</span><span class="sxs-lookup"><span data-stu-id="ca190-153">For more information, see [Check sensor state](check-sensor-status.md) and [Investigate devices](investigate-machines.md).</span></span>

## <a name="service-health"></a><span data-ttu-id="ca190-154">L’intégrité du service</span><span class="sxs-lookup"><span data-stu-id="ca190-154">Service health</span></span>
<span data-ttu-id="ca190-155">La **vignette d’état** du service vous informe si le service est actif ou s’il existe des problèmes.</span><span class="sxs-lookup"><span data-stu-id="ca190-155">The **Service health** tile informs you if the service is active or if there are issues.</span></span>

![La vignette d’état du service affiche un indicateur global du service](images/status-tile.png)

<span data-ttu-id="ca190-157">Pour plus d’informations sur l’état du service, voir [Vérifier l’état du service Microsoft Defender pour Endpoint.](service-status.md)</span><span class="sxs-lookup"><span data-stu-id="ca190-157">For more information on the service health, see [Check the Microsoft Defender for Endpoint service health](service-status.md).</span></span>


## <a name="daily-devices-reporting"></a><span data-ttu-id="ca190-158">Rapports quotidiens sur les appareils</span><span class="sxs-lookup"><span data-stu-id="ca190-158">Daily devices reporting</span></span>
<span data-ttu-id="ca190-159">La **vignette Rapports quotidiens sur** les appareils affiche un graphique à barres qui représente le nombre d’appareils signalant quotidiennement au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="ca190-159">The **Daily devices reporting** tile shows a bar graph that represents the number of devices reporting daily in the last 30 days.</span></span> <span data-ttu-id="ca190-160">Pointez sur des barres individuelles sur le graphique pour voir le nombre exact d’appareils signalant des rapports chaque jour.</span><span class="sxs-lookup"><span data-stu-id="ca190-160">Hover over individual bars on the graph to see the exact number of devices reporting in each day.</span></span>

![Image de la vignette rapports quotidiennes des appareils](images/atp-daily-devices-reporting.png)


## <a name="active-automated-investigations"></a><span data-ttu-id="ca190-162">Examens automatisés actifs</span><span class="sxs-lookup"><span data-stu-id="ca190-162">Active automated investigations</span></span>
<span data-ttu-id="ca190-163">Vous pouvez afficher le nombre global d’enquêtes automatisées des 30 derniers jours de votre réseau à partir de la **vignette Enquêtes automatisées actives.**</span><span class="sxs-lookup"><span data-stu-id="ca190-163">You can view the overall number of automated investigations from the last 30 days in your network from the **Active automated investigations** tile.</span></span> <span data-ttu-id="ca190-164">Les examens sont regroupés en **action en attente,** **en attente de l’appareil** et en **cours d’exécution.**</span><span class="sxs-lookup"><span data-stu-id="ca190-164">Investigations are grouped into **Pending action**, **Waiting for device**, and **Running**.</span></span>

![Inmage d’enquêtes automatisées actives](images/atp-active-investigations-tile.png)


## <a name="automated-investigations-statistics"></a><span data-ttu-id="ca190-166">Statistiques d’enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="ca190-166">Automated investigations statistics</span></span>
<span data-ttu-id="ca190-167">Cette vignette affiche les statistiques relatives aux enquêtes automatisées au cours des sept derniers jours.</span><span class="sxs-lookup"><span data-stu-id="ca190-167">This tile shows statistics related to automated investigations in the last seven days.</span></span> <span data-ttu-id="ca190-168">Il indique le nombre d’enquêtes terminées, le nombre d’enquêtes correctement corrigés, le temps en attente moyen d’un examen à lancer, le temps moyen de correction d’une alerte, le nombre d’alertes examinées et le nombre d’heures d’automatisation enregistrées à partir d’un examen manuel classique.</span><span class="sxs-lookup"><span data-stu-id="ca190-168">It shows the number of investigations completed, the number of successfully remediated investigations, the average pending time it takes for an investigation to be initiated, the average time it takes to remediate an alert, the number of alerts investigated, and the number of hours of automation saved from a typical manual investigation.</span></span> 

![Image des statistiques d’enquêtes automatisées](images/atp-automated-investigations-statistics.png)

<span data-ttu-id="ca190-170">Vous pouvez cliquer sur **Examens** automatisés, **Examens** corrigés et **Alertes examinées** pour accéder à la page **Enquêtes,** filtrée par catégorie appropriée.</span><span class="sxs-lookup"><span data-stu-id="ca190-170">You can click on **Automated investigations**, **Remediated investigations**, and **Alerts investigated** to navigate to the **Investigations** page, filtered by the appropriate category.</span></span> <span data-ttu-id="ca190-171">Cela vous permet d’obtenir une répartition détaillée des enquêtes en contexte.</span><span class="sxs-lookup"><span data-stu-id="ca190-171">This lets you see a detailed breakdown of investigations in context.</span></span>

## <a name="users-at-risk"></a><span data-ttu-id="ca190-172">Utilisateurs à risque</span><span class="sxs-lookup"><span data-stu-id="ca190-172">Users at risk</span></span>
<span data-ttu-id="ca190-173">La vignette affiche la liste des comptes d’utilisateurs avec les alertes les plus actives et le nombre d’alertes visibles sur les alertes élevées, moyennes ou faibles.</span><span class="sxs-lookup"><span data-stu-id="ca190-173">The tile shows you a list of user accounts with the most active alerts and the number of alerts seen on high, medium, or low alerts.</span></span> 

![La vignette Comptes d’utilisateurs à risque affiche la liste des comptes d’utilisateurs avec le plus grand nombre d’alertes et une répartition de la gravité des alertes](images/atp-users-at-risk.png)

<span data-ttu-id="ca190-175">Cliquez sur le compte d’utilisateur pour voir les détails sur le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ca190-175">Click the user account to see details about the user account.</span></span> <span data-ttu-id="ca190-176">Pour plus d’informations, [voir Examiner un compte d’utilisateur.](investigate-user.md)</span><span class="sxs-lookup"><span data-stu-id="ca190-176">For more information see [Investigate a user account](investigate-user.md).</span></span>

><span data-ttu-id="ca190-177">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ca190-177">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="ca190-178">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ca190-178">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-secopsdashboard-belowfoldlink)

## <a name="related-topics"></a><span data-ttu-id="ca190-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca190-179">Related topics</span></span>
- [<span data-ttu-id="ca190-180">Comprendre le portail Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ca190-180">Understand the Microsoft Defender for Endpoint portal</span></span>](use.md)
- [<span data-ttu-id="ca190-181">Vue d’ensemble du portail</span><span class="sxs-lookup"><span data-stu-id="ca190-181">Portal overview</span></span>](portal-overview.md)
- [<span data-ttu-id="ca190-182">Afficher le tableau de bord gestion & des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="ca190-182">View the Threat & Vulnerability Management dashboard</span></span>](tvm-dashboard-insights.md)
- [<span data-ttu-id="ca190-183">Afficher le tableau de bord Analyse des menaces et prendre les mesures de prévention recommandées</span><span class="sxs-lookup"><span data-stu-id="ca190-183">View the Threat analytics dashboard and take recommended mitigation actions</span></span>](threat-analytics.md)
