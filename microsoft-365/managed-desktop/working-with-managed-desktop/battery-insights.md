---
title: Informations sur la batterie
description: ''
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: b14ef9970aa709ad5e23fdae467992497a1331e8
ms.sourcegitcommit: 3dca80f268006658a0b721aa4f6df1224c7964dc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "41260141"
---
# <a name="battery-insights"></a><span data-ttu-id="cb712-103">Informations sur la batterie</span><span class="sxs-lookup"><span data-stu-id="cb712-103">Battery insights</span></span>
<span data-ttu-id="cb712-104">Cette vue fournit des mesures d’utilisation de l’alimentation, de la batterie et de l’application pour vos appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cb712-104">This view provides power, battery, and app usage metrics for your Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="cb712-105">À cette fin, une application est considérée « en cours d’utilisation » si elle est en cours d’exécution et en focus.</span><span class="sxs-lookup"><span data-stu-id="cb712-105">For these purposes, an app is considered "in use" if it is running and in focus.</span></span>

<span data-ttu-id="cb712-106">Pour afficher les données d’utilisation, sélectionnez l’onglet **batterie** .</span><span class="sxs-lookup"><span data-stu-id="cb712-106">To view usage data, select the **Battery** tab.</span></span>

![Volet de la batterie : durée de vie de la batterie prévisible par modèle d’appareil dans le coin supérieur gauche, consommateurs de l’énergie de haut niveau (par application) dans le coin supérieur droit, tableau Insights en bas.](images/insights_battery.png)

## <a name="predicted-battery-life"></a><span data-ttu-id="cb712-109">Durée de vie de la batterie prévisible</span><span class="sxs-lookup"><span data-stu-id="cb712-109">Predicted battery life</span></span>

<span data-ttu-id="cb712-110">Dans la zone de **durée de vie** de la batterie prévue, nous fournissons des prévisions pour la durée de vie de la batterie attendue pour vos appareils, organisés par modèle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb712-110">In the **Predicted battery life** area, we provide predictions for the expected battery life for your devices, organized by device model.</span></span>

> [!NOTE]
> <span data-ttu-id="cb712-111">Ces données proviennent de l’échantillonnage de l’utilisation de l’énergie, du temps d’utilisation et de la capacité de la batterie à partir d’une <em>sélection</em> aléatoire des appareils dans votre déploiement de bureau géré Microsoft qui sont également des données de rapport.</span><span class="sxs-lookup"><span data-stu-id="cb712-111">This data is derived from sampling energy usage, usage time, and battery capacity from a random <em>selection</em> of the devices in your Microsoft Managed Desktop deployment that are also reporting data.</span></span>

<span data-ttu-id="cb712-112">Le tableau indique la durée de vie de la batterie prévue (en heures), la durée de vie moyenne de la batterie pour les mêmes modèles dans d’autres déploiements de bureau géré Microsoft et le nombre d’appareils qui signalent ces données dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="cb712-112">The table provides the predicted battery life (in hours), average battery life for the same models in other Microsoft Managed Desktop deployments, and the number of devices reporting this data in your environment.</span></span> <span data-ttu-id="cb712-113">Triez les données en sélectionnant les en-têtes de colonne.</span><span class="sxs-lookup"><span data-stu-id="cb712-113">Sort the data by selecting the column headings.</span></span>



## <a name="top-energy-consumers"></a><span data-ttu-id="cb712-114">Principaux consommateurs énergétiques</span><span class="sxs-lookup"><span data-stu-id="cb712-114">Top energy consumers</span></span>

<span data-ttu-id="cb712-115">Dans la zone **Consumer Energy Top** , vous trouverez les applications de votre environnement qui consomment le plus d’énergie en milliwatt-Hours (MWh).</span><span class="sxs-lookup"><span data-stu-id="cb712-115">In the **Top energy consumers** area you’ll find the apps in your environment that consume the most energy in milliWatt-hours (mWh).</span></span> <span data-ttu-id="cb712-116">Les applications affichées sont déterminées par un appareil spécifique, que vous sélectionnez dans la section **durée de vie** de la batterie à gauche.</span><span class="sxs-lookup"><span data-stu-id="cb712-116">The apps shown are per specific device, which you select in the **Predicted battery life** section to the left.</span></span> <span data-ttu-id="cb712-117">Par exemple, pour voir la consommation par application de vos appareils de la surface de votre site, sélectionnez cette ligne dans la zone autonomie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="cb712-117">For example, to see the per-app consumption for your Microsft Surface Book 2 devices, select that row in the battery life area.</span></span> <span data-ttu-id="cb712-118">Si vous ne sélectionnez aucun modèle, les données de consommation de l’application affichées s’affichent pour toutes les applications pour lesquelles nous disposons de données collectives.</span><span class="sxs-lookup"><span data-stu-id="cb712-118">If you don't select any model, the app consumption data shown is for all apps that we have data for collectively.</span></span>

 <span data-ttu-id="cb712-119">Pour chaque application, les segments colorés vous montrent la distribution de l’utilisation de l’énergie de l’application dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb712-119">For each app, colored segments show you the distribution of the app's energy use among these categories:</span></span>

- <span data-ttu-id="cb712-120">UC</span><span class="sxs-lookup"><span data-stu-id="cb712-120">CPU</span></span>
- <span data-ttu-id="cb712-121">Display</span><span class="sxs-lookup"><span data-stu-id="cb712-121">Display</span></span>
- <span data-ttu-id="cb712-122">Réseau</span><span class="sxs-lookup"><span data-stu-id="cb712-122">Network</span></span>
- <span data-ttu-id="cb712-123">Autres</span><span class="sxs-lookup"><span data-stu-id="cb712-123">Other</span></span>

<span data-ttu-id="cb712-124">« Other » peut inclure la consommation d’énergie par diverses sources, telles que l’activité du disque, l’utilisation du haut débit mobile et l’énergie perdue à la résistance interne.</span><span class="sxs-lookup"><span data-stu-id="cb712-124">"Other" could include energy consumption by a variety of sources, such as disk activity, mobile broadband usage, and energy lost to internal resistance.</span></span> 

<span data-ttu-id="cb712-125">Applications affichées dans \* \* Consumers Energy Top</span><span class="sxs-lookup"><span data-stu-id="cb712-125">The apps displayed in \*\*Top energy consumers"</span></span>

<span data-ttu-id="cb712-126">Vous pouvez filtrer cet affichage pour n’afficher que les applications de premier plan, les applications d’arrière-plan ou les deux à l’aide du menu en haut à droite.</span><span class="sxs-lookup"><span data-stu-id="cb712-126">You can filter this view to show only foreground apps, background apps, or both by using the menu in the upper right.</span></span> <span data-ttu-id="cb712-127">Les applications de premier plan sont celles qui ont eu une interaction avec l’utilisateur au cours des 28 derniers jours, comme la sélection d’un article à l’aide d’une souris.</span><span class="sxs-lookup"><span data-stu-id="cb712-127">Foreground apps are those that have had user interaction in the last 28 days, such as selecting something with a mouse.</span></span>

## <a name="insights"></a><span data-ttu-id="cb712-128">Informations</span><span class="sxs-lookup"><span data-stu-id="cb712-128">Insights</span></span>

<span data-ttu-id="cb712-129">La zone **Insights** présente les trois principaux consommateurs énergétiques dans les catégories d’UC et de réseau.</span><span class="sxs-lookup"><span data-stu-id="cb712-129">The **Insights** area shows the top three energy consumers in the CPU and network categories.</span></span> <span data-ttu-id="cb712-130">Ces éléments consomment une consommation supérieure à la moyenne par rapport à tous les déploiements de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cb712-130">These items are consuming higher than average energy compared to all Microsoft Managed Desktop deployments.</span></span> <span data-ttu-id="cb712-131">Nous n’affichons pas la ressource d’affichage, car elle dépend étroitement de la durée d’utilisation de l’appareil et des paramètres de luminosité de l’écran.</span><span class="sxs-lookup"><span data-stu-id="cb712-131">We don't show the display resource because it depends heavily on device usage time and screen brightness settings.</span></span> 

<span data-ttu-id="cb712-132">Pour plus d’informations, sélectionnez les listes dans la colonne **Détails** .</span><span class="sxs-lookup"><span data-stu-id="cb712-132">Select the listings in the **Details** column for more information.</span></span>

## <a name="battery-optimization"></a><span data-ttu-id="cb712-133">Optimisation de la batterie</span><span class="sxs-lookup"><span data-stu-id="cb712-133">Battery optimization</span></span>

<span data-ttu-id="cb712-134">Windows 10 offre de nombreux [paramètres d’appareil](https://support.microsoft.com/help/20443/windows-10-battery-saving-tips) pour améliorer la consommation d’énergie et augmenter la durée de vie de la batterie de vos appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cb712-134">Windows 10 offers numerous [device settings](https://support.microsoft.com/help/20443/windows-10-battery-saving-tips) to improve power usage and increase the battery life of your Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="cb712-135">Certains de ces paramètres peuvent réduire d’autres fonctionnalités de Windows, de sorte que vous devrez également prendre en compte d’autres facteurs, tels que le rôle de l’appareil dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb712-135">Some of these settings can decrease other Windows functionality, so you'll also have to consider other factors such as the role of the device in your organization.</span></span> <span data-ttu-id="cb712-136">Le support Windows conserve une liste de ces [conseils d’économie de batterie](https://support.microsoft.com/help/20443/windows-10-battery-saving-tips).</span><span class="sxs-lookup"><span data-stu-id="cb712-136">Windows support maintains a list of these [battery saving tips](https://support.microsoft.com/help/20443/windows-10-battery-saving-tips).</span></span>

<span data-ttu-id="cb712-137">Les utilisateurs peuvent ajuster certains paramètres sans avoir besoin d’une élévation ou d’une prise en charge de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="cb712-137">Users can adjust some settings on their own without the need for admin elevation or support.</span></span> <span data-ttu-id="cb712-138">D’autres paramètres doivent être pris en charge par l’administrateur informatique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb712-138">Other settings require support from your organization's IT administrator.</span></span>
