---
title: Aperçu de la batterie
description: Un rapport qui affiche des données sur l’autonomie prévue de la batterie et les principaux consommateurs d’énergie
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
audience: Admin
ms.openlocfilehash: 32ab3a984d5ab46aac26989518cd3e570082d688
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51579709"
---
# <a name="battery-insights"></a><span data-ttu-id="ac3be-104">Aperçu de la batterie</span><span class="sxs-lookup"><span data-stu-id="ac3be-104">Battery insights</span></span>
<span data-ttu-id="ac3be-105">Cette vue fournit des mesures d’utilisation de l’alimentation, de la batterie et de l’application pour vos appareils de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac3be-105">This view provides power, battery, and app usage metrics for your Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="ac3be-106">À ces fins, une application est considérée comme « en cours d’utilisation » si elle est en cours d’exécution et en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ac3be-106">For these purposes, an app is considered "in use" if it is running and in focus.</span></span>

<span data-ttu-id="ac3be-107">Pour afficher les données d’utilisation, sélectionnez **l’onglet** Batterie.</span><span class="sxs-lookup"><span data-stu-id="ac3be-107">To view usage data, select the **Battery** tab.</span></span>

![Volet de batterie : durée de vie prévue de la batterie par modèle d’appareil en haut à gauche, consommateurs d’énergie supérieurs (par application) en haut à droite, tableau d’informations en bas.](../../media/insights_battery.png)

## <a name="predicted-battery-life"></a><span data-ttu-id="ac3be-110">Durée de vie prévue de la batterie</span><span class="sxs-lookup"><span data-stu-id="ac3be-110">Predicted battery life</span></span>

<span data-ttu-id="ac3be-111">Dans la **zone d’autonomie prévue de** la batterie, nous fournissons des prévisions pour l’autonomie prévue de la batterie pour vos appareils, organisée par modèle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="ac3be-111">In the **Predicted battery life** area, we provide predictions for the expected battery life for your devices, organized by device model.</span></span>

> [!NOTE]
> <span data-ttu-id="ac3be-112">Ces données sont dérivées de l’échantillonnage de l’utilisation de l’énergie, du temps d’utilisation et de la capacité de la batterie à partir d’une sélection aléatoire des appareils de votre déploiement Bureau géré Microsoft qui sont également des données de rapport. <em></em></span><span class="sxs-lookup"><span data-stu-id="ac3be-112">This data is derived from sampling energy usage, usage time, and battery capacity from a random <em>selection</em> of the devices in your Microsoft Managed Desktop deployment that are also reporting data.</span></span>

<span data-ttu-id="ac3be-113">Le tableau indique l’autonomie prévue de la batterie (en heures), l’autonomie moyenne de la batterie pour les mêmes modèles dans d’autres déploiements de Bureau géré Microsoft et le nombre d’appareils signalant ces données dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="ac3be-113">The table provides the predicted battery life (in hours), average battery life for the same models in other Microsoft Managed Desktop deployments, and the number of devices reporting this data in your environment.</span></span> <span data-ttu-id="ac3be-114">Trie les données en sélectionnant les en-tête de colonne.</span><span class="sxs-lookup"><span data-stu-id="ac3be-114">Sort the data by selecting the column headings.</span></span>



## <a name="top-energy-consumers"></a><span data-ttu-id="ac3be-115">Principaux consommateurs d’énergie</span><span class="sxs-lookup"><span data-stu-id="ac3be-115">Top energy consumers</span></span>

<span data-ttu-id="ac3be-116">Dans la **zone Consommateurs** d’énergie les plus consommateurs d’énergie, vous trouverez les applications de votre environnement qui consomment le plus d’énergie en milliWatt-hours (mWh).</span><span class="sxs-lookup"><span data-stu-id="ac3be-116">In the **Top energy consumers** area you’ll find the apps in your environment that consume the most energy in milliWatt-hours (mWh).</span></span> <span data-ttu-id="ac3be-117">Les applications affichées sont par appareil spécifique, que vous sélectionnez dans la section Durée de vie **prévue de la** batterie à gauche.</span><span class="sxs-lookup"><span data-stu-id="ac3be-117">The apps shown are per specific device, which you select in the **Predicted battery life** section to the left.</span></span> <span data-ttu-id="ac3be-118">Par exemple, pour voir la consommation par application pour vos appareils Microsoft Surface Book 2, sélectionnez cette ligne dans la zone d’autonomie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="ac3be-118">For example, to see the per-app consumption for your Microsoft Surface Book 2 devices, select that row in the battery life area.</span></span> <span data-ttu-id="ac3be-119">Si vous ne sélectionnez aucun modèle, les données de consommation d’application affichées sont pour toutes les applications pour qui nous avons des données collectivement.</span><span class="sxs-lookup"><span data-stu-id="ac3be-119">If you don't select any model, the app consumption data shown is for all apps that we have data for collectively.</span></span>

 <span data-ttu-id="ac3be-120">Pour chaque application, les segments de couleur vous montrent la répartition de l’utilisation énergétique de l’application parmi ces catégories :</span><span class="sxs-lookup"><span data-stu-id="ac3be-120">For each app, colored segments show you the distribution of the app's energy use among these categories:</span></span>

- <span data-ttu-id="ac3be-121">UC</span><span class="sxs-lookup"><span data-stu-id="ac3be-121">CPU</span></span>
- <span data-ttu-id="ac3be-122">Afficher</span><span class="sxs-lookup"><span data-stu-id="ac3be-122">Display</span></span>
- <span data-ttu-id="ac3be-123">Réseau</span><span class="sxs-lookup"><span data-stu-id="ac3be-123">Network</span></span>
- <span data-ttu-id="ac3be-124">Autres</span><span class="sxs-lookup"><span data-stu-id="ac3be-124">Other</span></span>

<span data-ttu-id="ac3be-125">Les « autres » peuvent inclure la consommation d’énergie par diverses sources, telles que l’activité du disque, l’utilisation du haut débit mobile et la perte d’énergie par la résistance interne.</span><span class="sxs-lookup"><span data-stu-id="ac3be-125">"Other" could include energy consumption by a variety of sources, such as disk activity, mobile broadband usage, and energy lost to internal resistance.</span></span> 

<span data-ttu-id="ac3be-126">Vous pouvez filtrer cette vue pour afficher uniquement les applications de premier plan, les applications d’arrière-plan ou les deux à l’aide du menu en haut à droite.</span><span class="sxs-lookup"><span data-stu-id="ac3be-126">You can filter this view to show only foreground apps, background apps, or both by using the menu in the upper right.</span></span> <span data-ttu-id="ac3be-127">Les applications de premier plan sont celles qui ont eu une interaction utilisateur au cours des 28 derniers jours, telles que la sélection d’un contenu à l’aide d’une souris.</span><span class="sxs-lookup"><span data-stu-id="ac3be-127">Foreground apps are those that have had user interaction in the last 28 days, such as selecting something with a mouse.</span></span>

## <a name="insights"></a><span data-ttu-id="ac3be-128">Informations</span><span class="sxs-lookup"><span data-stu-id="ac3be-128">Insights</span></span>

<span data-ttu-id="ac3be-129">La **zone Insights** présente les trois premiers consommateurs d’énergie dans les catégories processeur et réseau.</span><span class="sxs-lookup"><span data-stu-id="ac3be-129">The **Insights** area shows the top three energy consumers in the CPU and network categories.</span></span> <span data-ttu-id="ac3be-130">Ces éléments consomment plus d’énergie que la moyenne par rapport à tous les déploiements de Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac3be-130">These items are consuming higher than average energy compared to all Microsoft Managed Desktop deployments.</span></span> <span data-ttu-id="ac3be-131">Nous n’affichons pas la ressource d’affichage, car elle dépend fortement du temps d’utilisation de l’appareil et des paramètres de luminosité de l’écran.</span><span class="sxs-lookup"><span data-stu-id="ac3be-131">We don't show the display resource because it depends heavily on device usage time and screen brightness settings.</span></span> 

<span data-ttu-id="ac3be-132">Sélectionnez les descriptions dans la **colonne Détails** pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ac3be-132">Select the listings in the **Details** column for more information.</span></span>

## <a name="battery-optimization"></a><span data-ttu-id="ac3be-133">Optimisation de la batterie</span><span class="sxs-lookup"><span data-stu-id="ac3be-133">Battery optimization</span></span>

<span data-ttu-id="ac3be-134">Windows 10 offre de nombreux [paramètres d’appareil](https://support.microsoft.com/help/20443/windows-10-battery-saving-tips) pour améliorer l’utilisation de l’alimentation et augmenter l’autonomie de la batterie de vos appareils de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac3be-134">Windows 10 offers numerous [device settings](https://support.microsoft.com/help/20443/windows-10-battery-saving-tips) to improve power usage and increase the battery life of your Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="ac3be-135">Certains de ces paramètres peuvent diminuer les autres fonctionnalités de Windows. Vous devez donc également prendre en compte d’autres facteurs tels que le rôle de l’appareil dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ac3be-135">Some of these settings can decrease other Windows functionality, so you'll also have to consider other factors such as the role of the device in your organization.</span></span> <span data-ttu-id="ac3be-136">La prise en charge de Windows conserve une liste de ces conseils [d’économie de batterie.](https://support.microsoft.com/help/20443/windows-10-battery-saving-tips)</span><span class="sxs-lookup"><span data-stu-id="ac3be-136">Windows support maintains a list of these [battery saving tips](https://support.microsoft.com/help/20443/windows-10-battery-saving-tips).</span></span>

<span data-ttu-id="ac3be-137">Les utilisateurs peuvent ajuster certains paramètres eux-mêmes sans avoir besoin d’une élévation ou d’une prise en charge par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="ac3be-137">Users can adjust some settings on their own without the need for admin elevation or support.</span></span> <span data-ttu-id="ac3be-138">D’autres paramètres nécessitent la prise en charge de l’administrateur informatique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ac3be-138">Other settings require support from your organization's IT administrator.</span></span>
