---
title: Afficher et organiser la liste des appareils Microsoft Defender pour les points de terminaison
description: Découvrez les fonctionnalités disponibles que vous pouvez utiliser dans la liste Appareils, telles que le tri, le filtrage et l'exportation de la liste pour améliorer les investigations.
keywords: sort, filter, export, csv, device name, domain, last seen, internal IP, health state, active alerts, active malware detections, threat category, review alerts, network, connection, malware, type, password stealer, ransomware, exploit, threat, general malware, unwanted software
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
ms.topic: article
ms.technology: mde
ms.openlocfilehash: a031a35929f319e87a9ad1a9ca48d6bf95a3ef72
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51861574"
---
# <a name="view-and-organize-the-microsoft-defender-for-endpoint-devices-list"></a><span data-ttu-id="1e69e-104">Afficher et organiser la liste Microsoft Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1e69e-104">View and organize the Microsoft Defender for Endpoint Devices list</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="1e69e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1e69e-105">**Applies to:**</span></span>
- [<span data-ttu-id="1e69e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1e69e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1e69e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1e69e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="1e69e-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1e69e-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="1e69e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1e69e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-machinesview-abovefoldlink)


<span data-ttu-id="1e69e-110">La **liste Appareils affiche** la liste des appareils de votre réseau sur lequel des alertes ont été générées.</span><span class="sxs-lookup"><span data-stu-id="1e69e-110">The **Devices list** shows a list of the devices in your network where alerts were generated.</span></span> <span data-ttu-id="1e69e-111">Par défaut, la file d'attente affiche les appareils visibles au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1e69e-111">By default, the queue displays devices seen in the last 30 days.</span></span>  

<span data-ttu-id="1e69e-112">En un coup d'œil, vous verrez des informations telles que le domaine, le niveau de risque, la plateforme du système d'exploitation et d'autres détails pour faciliter l'identification des appareils les plus exposés.</span><span class="sxs-lookup"><span data-stu-id="1e69e-112">At a glance you'll see information such as domain, risk level, OS platform, and other details for easy identification of devices most at risk.</span></span>

<span data-ttu-id="1e69e-113">Vous pouvez choisir parmi plusieurs options pour personnaliser l'affichage liste des appareils.</span><span class="sxs-lookup"><span data-stu-id="1e69e-113">There are several options you can choose from to customize the devices list view.</span></span> <span data-ttu-id="1e69e-114">Dans la barre de navigation supérieure, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="1e69e-114">On the top navigation you can:</span></span>

- <span data-ttu-id="1e69e-115">Ajouter ou supprimer des colonnes</span><span class="sxs-lookup"><span data-stu-id="1e69e-115">Add or remove columns</span></span>
- <span data-ttu-id="1e69e-116">Exporter la liste entière au format CSV</span><span class="sxs-lookup"><span data-stu-id="1e69e-116">Export the entire list in CSV format</span></span>
- <span data-ttu-id="1e69e-117">Sélectionner le nombre d'éléments à afficher par page</span><span class="sxs-lookup"><span data-stu-id="1e69e-117">Select the number of items to show per page</span></span>
- <span data-ttu-id="1e69e-118">Appliquer des filtres</span><span class="sxs-lookup"><span data-stu-id="1e69e-118">Apply filters</span></span>

<span data-ttu-id="1e69e-119">Pendant le processus d'intégration, la liste **Appareils** est progressivement remplie avec les appareils qui commencent à signaler les données de capteur.</span><span class="sxs-lookup"><span data-stu-id="1e69e-119">During the onboarding process, the **Devices list** is gradually populated with devices as they begin to report sensor data.</span></span> <span data-ttu-id="1e69e-120">Utilisez cette vue pour suivre vos points de terminaison intégrés lors de leur mise en ligne ou téléchargez la liste complète des points de terminaison en tant que fichier CSV pour l'analyse hors connexion.</span><span class="sxs-lookup"><span data-stu-id="1e69e-120">Use this view to track your onboarded endpoints as they come online, or download the complete endpoint list as a CSV file for offline analysis.</span></span>

>[!NOTE]
> <span data-ttu-id="1e69e-121">Si vous exportez la liste des appareils, elle contiendra tous les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1e69e-121">If you export the device list, it will contain every device in your organization.</span></span> <span data-ttu-id="1e69e-122">Le téléchargement peut prendre beaucoup de temps, en fonction de la taille de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1e69e-122">It might take a significant amount of time to download, depending on how large your organization is.</span></span> <span data-ttu-id="1e69e-123">L'exportation de la liste au format CSV affiche les données de manière non filtrée.</span><span class="sxs-lookup"><span data-stu-id="1e69e-123">Exporting the list in CSV format displays the data in an unfiltered manner.</span></span> <span data-ttu-id="1e69e-124">Le fichier CSV inclut tous les appareils de l'organisation, quel que soit le filtrage appliqué dans l'affichage lui-même.</span><span class="sxs-lookup"><span data-stu-id="1e69e-124">The CSV file will include all devices in the organization, regardless of any filtering applied in the view itself.</span></span>

![Image de la liste des appareils avec liste d'appareils](images/device-list.png)

## <a name="sort-and-filter-the-device-list"></a><span data-ttu-id="1e69e-126">Trier et filtrer la liste des appareils</span><span class="sxs-lookup"><span data-stu-id="1e69e-126">Sort and filter the device list</span></span>

<span data-ttu-id="1e69e-127">Vous pouvez appliquer les filtres suivants pour limiter la liste des alertes et obtenir une vue plus centrée.</span><span class="sxs-lookup"><span data-stu-id="1e69e-127">You can apply the following filters to limit the list of alerts and get a more focused view.</span></span>

### <a name="risk-level"></a><span data-ttu-id="1e69e-128">Niveau de risque</span><span class="sxs-lookup"><span data-stu-id="1e69e-128">Risk level</span></span>

<span data-ttu-id="1e69e-129">Le niveau de risque reflète l'évaluation globale des risques de l'appareil en fonction d'une combinaison de facteurs, notamment les types et la gravité des alertes actives sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="1e69e-129">The risk level reflects the overall risk assessment of the device based on a combination of factors, including the types and severity of active alerts on the device.</span></span> <span data-ttu-id="1e69e-130">La résolution des alertes actives, l'approbation des activités de correction et la suppression des alertes suivantes peuvent réduire le niveau de risque.</span><span class="sxs-lookup"><span data-stu-id="1e69e-130">Resolving active alerts, approving remediation activities, and suppressing subsequent alerts can lower the risk level.</span></span>

### <a name="exposure-level"></a><span data-ttu-id="1e69e-131">Niveau d'exposition</span><span class="sxs-lookup"><span data-stu-id="1e69e-131">Exposure level</span></span>

<span data-ttu-id="1e69e-132">Le niveau d'exposition reflète l'exposition actuelle de l'appareil en fonction de l'impact cumulé de ses recommandations de sécurité en attente.</span><span class="sxs-lookup"><span data-stu-id="1e69e-132">The exposure level reflects the current exposure of the device based on the cumulative impact of its pending security recommendations.</span></span> <span data-ttu-id="1e69e-133">Les niveaux possibles sont faibles, moyens et élevés.</span><span class="sxs-lookup"><span data-stu-id="1e69e-133">The possible levels are low, medium, and high.</span></span> <span data-ttu-id="1e69e-134">Une faible exposition signifie que vos appareils sont moins vulnérables à l'exploitation.</span><span class="sxs-lookup"><span data-stu-id="1e69e-134">Low exposure means your devices are less vulnerable from exploitation.</span></span>

<span data-ttu-id="1e69e-135">Si le niveau d'exposition indique « Aucune donnée disponible », il existe plusieurs raisons pour lesquelles cela peut être le cas :</span><span class="sxs-lookup"><span data-stu-id="1e69e-135">If the exposure level says "No data available," there are a few reasons why this may be the case:</span></span>

- <span data-ttu-id="1e69e-136">L'appareil a cessé de signaler pendant plus de 30 jours. Dans ce cas, il est considéré comme inactif et l'exposition n'est pas calculée</span><span class="sxs-lookup"><span data-stu-id="1e69e-136">Device stopped reporting for more than 30 days – in that case it is considered inactive, and the exposure isn't computed</span></span>
- <span data-ttu-id="1e69e-137">Le système d'exploitation de l'appareil n'est [pas pris en charge : voir les conditions minimales requises pour Microsoft Defender pour endpoint](minimum-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="1e69e-137">Device OS not supported - see [minimum requirements for Microsoft Defender for Endpoint](minimum-requirements.md)</span></span>
- <span data-ttu-id="1e69e-138">Appareil avec agent obsolète (très peu probable)</span><span class="sxs-lookup"><span data-stu-id="1e69e-138">Device with stale agent (very unlikely)</span></span>

### <a name="os-platform"></a><span data-ttu-id="1e69e-139">Plateforme du système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="1e69e-139">OS Platform</span></span>

<span data-ttu-id="1e69e-140">Sélectionnez uniquement les plateformes de système d'exploitation qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="1e69e-140">Select only the OS platforms you're interested in investigating.</span></span>

### <a name="health-state"></a><span data-ttu-id="1e69e-141">État d’intégrité</span><span class="sxs-lookup"><span data-stu-id="1e69e-141">Health state</span></span>

<span data-ttu-id="1e69e-142">Filtrez selon les états d'état d'état d'appareil suivants :</span><span class="sxs-lookup"><span data-stu-id="1e69e-142">Filter by the following device health states:</span></span>

- <span data-ttu-id="1e69e-143">**Actif** : appareils qui rapportent activement des données de capteur au service.</span><span class="sxs-lookup"><span data-stu-id="1e69e-143">**Active** – Devices that are actively reporting sensor data to the service.</span></span>
- <span data-ttu-id="1e69e-144">**Inactif** : appareils qui ont complètement cessé d'envoyer des signaux pendant plus de 7 jours.</span><span class="sxs-lookup"><span data-stu-id="1e69e-144">**Inactive** – Devices that have completely stopped sending signals for more than 7 days.</span></span>
- <span data-ttu-id="1e69e-145">**Mal configuré : appareils** dont les communications avec le service sont réduites ou qui ne sont pas en mesure d'envoyer des données de capteur.</span><span class="sxs-lookup"><span data-stu-id="1e69e-145">**Misconfigured** – Devices that have impaired communications with service or are unable to send sensor data.</span></span> <span data-ttu-id="1e69e-146">Les appareils mal configurés peuvent également être classés sur :</span><span class="sxs-lookup"><span data-stu-id="1e69e-146">Misconfigured devices can further be classified to:</span></span>
  - <span data-ttu-id="1e69e-147">Aucune donnée de capteur</span><span class="sxs-lookup"><span data-stu-id="1e69e-147">No sensor data</span></span>
  - <span data-ttu-id="1e69e-148">Communications compromises</span><span class="sxs-lookup"><span data-stu-id="1e69e-148">Impaired communications</span></span>

  <span data-ttu-id="1e69e-149">Pour plus d'informations sur la façon de résoudre les problèmes sur les appareils mal configurés, voir corriger les [capteurs défectueux.](fix-unhealthy-sensors.md)</span><span class="sxs-lookup"><span data-stu-id="1e69e-149">For more information on how to address issues on misconfigured devices see, [Fix unhealthy sensors](fix-unhealthy-sensors.md).</span></span>

### <a name="antivirus-status"></a><span data-ttu-id="1e69e-150">État de l'antivirus</span><span class="sxs-lookup"><span data-stu-id="1e69e-150">Antivirus status</span></span>

<span data-ttu-id="1e69e-151">Filtrer les appareils par état antivirus.</span><span class="sxs-lookup"><span data-stu-id="1e69e-151">Filter devices by antivirus status.</span></span> <span data-ttu-id="1e69e-152">S'applique uniquement aux appareils Windows 10 actifs.</span><span class="sxs-lookup"><span data-stu-id="1e69e-152">Applies to active Windows 10 devices only.</span></span>

- <span data-ttu-id="1e69e-153">**Désactivé :** la protection contre & virus est désactivée.</span><span class="sxs-lookup"><span data-stu-id="1e69e-153">**Disabled** - Virus & threat protection is turned off.</span></span>
- <span data-ttu-id="1e69e-154">**Not reporting** : la protection contre & contre les virus n'est pas un rapport.</span><span class="sxs-lookup"><span data-stu-id="1e69e-154">**Not reporting** - Virus & threat protection is not reporting.</span></span>
- <span data-ttu-id="1e69e-155">**Non mis à jour** : la protection & contre les virus n'est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1e69e-155">**Not updated** - Virus & threat protection is not up to date.</span></span>

<span data-ttu-id="1e69e-156">Pour plus d'informations, consultez le tableau de [bord gestion & des menaces et des vulnérabilités.](tvm-dashboard-insights.md)</span><span class="sxs-lookup"><span data-stu-id="1e69e-156">For more information, see [View the Threat & Vulnerability Management dashboard](tvm-dashboard-insights.md).</span></span>

### <a name="threat-mitigation-status"></a><span data-ttu-id="1e69e-157">État de l'atténuation des menaces</span><span class="sxs-lookup"><span data-stu-id="1e69e-157">Threat mitigation status</span></span>

<span data-ttu-id="1e69e-158">Pour afficher les appareils qui peuvent être affectés par une certaine menace, sélectionnez-la dans le menu déroulant, puis sélectionnez les aspects de vulnérabilité à atténuer.</span><span class="sxs-lookup"><span data-stu-id="1e69e-158">To view devices that may be affected by a certain threat, select the threat from the dropdown menu, and then select what vulnerability aspect needs to be mitigated.</span></span>

<span data-ttu-id="1e69e-159">Pour en savoir plus sur certaines menaces, consultez [l'analyse des menaces.](threat-analytics.md)</span><span class="sxs-lookup"><span data-stu-id="1e69e-159">To learn more about certain threats, see [Threat analytics](threat-analytics.md).</span></span> <span data-ttu-id="1e69e-160">Pour plus d'informations sur l'atténuation, [voir Threat & Vulnerability Management](next-gen-threat-and-vuln-mgt.md).</span><span class="sxs-lookup"><span data-stu-id="1e69e-160">For mitigation information, see [Threat & Vulnerability Management](next-gen-threat-and-vuln-mgt.md).</span></span>

### <a name="windows-10-version"></a><span data-ttu-id="1e69e-161">Version de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1e69e-161">Windows 10 version</span></span>

<span data-ttu-id="1e69e-162">Sélectionnez uniquement les versions de Windows 10 qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="1e69e-162">Select only the Windows 10 versions you're interested in investigating.</span></span>

### <a name="tags--groups"></a><span data-ttu-id="1e69e-163">Balises & groupes</span><span class="sxs-lookup"><span data-stu-id="1e69e-163">Tags & Groups</span></span>

<span data-ttu-id="1e69e-164">Filtrez la liste en fonction du regroupement et du marquage que vous avez ajoutés à des appareils individuels.</span><span class="sxs-lookup"><span data-stu-id="1e69e-164">Filter the list based on the grouping and tagging that you've added to individual devices.</span></span> <span data-ttu-id="1e69e-165">Voir [Créer et gérer des balises d'appareil](machine-tags.md) et créer et gérer des groupes [d'appareils.](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="1e69e-165">See [Create and manage device tags](machine-tags.md) and [Create and manage device groups](machine-groups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e69e-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e69e-166">Related topics</span></span>

- [<span data-ttu-id="1e69e-167">Examiner les appareils de la liste Microsoft Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1e69e-167">Investigate devices in the Microsoft Defender for Endpoint Devices list</span></span>](investigate-machines.md)
