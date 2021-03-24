---
title: Rapport sur l’état et la conformité de l’appareil dans Microsoft Defender ATP
description: Suivre les détections d’état de l’appareil, l’état antivirus, la plateforme de système d’exploitation et les versions de Windows 10 à l’aide du rapport d’état et de conformité de l’appareil
keywords: état d’état d’état, antivirus, plateforme de système d’exploitation, version de Windows 10, version, santé, conformité, état
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
ms.openlocfilehash: 9d41071fc5849f3a11061437af2bb88b117ec4a8
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064057"
---
# <a name="device-health-and-compliance-report-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="0b33c-104">Rapport sur l’état et la conformité de l’appareil dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0b33c-104">Device health and compliance report in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="0b33c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0b33c-105">**Applies to:**</span></span>
- [<span data-ttu-id="0b33c-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0b33c-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="0b33c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0b33c-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="0b33c-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="0b33c-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="0b33c-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="0b33c-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="0b33c-110">Le rapport d’état des appareils fournit des informations de haut niveau sur les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0b33c-110">The devices status report provides high-level information about the devices in your organization.</span></span> <span data-ttu-id="0b33c-111">Le rapport inclut des informations de tendance montrant l’état d’état du capteur, l’état antivirus, les plateformes de système d’exploitation et les versions de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0b33c-111">The report includes trending information showing the sensor health state, antivirus status, OS platforms, and Windows 10 versions.</span></span>

<span data-ttu-id="0b33c-112">Le tableau de bord est structuré en deux sections : ![ image du rapport de périphérique](images/device-reports.png)</span><span class="sxs-lookup"><span data-stu-id="0b33c-112">The dashboard is structured into two sections: ![Image of the device report](images/device-reports.png)</span></span>
 
<span data-ttu-id="0b33c-113">Section</span><span class="sxs-lookup"><span data-stu-id="0b33c-113">Section</span></span> | <span data-ttu-id="0b33c-114">Description</span><span class="sxs-lookup"><span data-stu-id="0b33c-114">Description</span></span>
:---|:---
<span data-ttu-id="0b33c-115">1</span><span class="sxs-lookup"><span data-stu-id="0b33c-115">1</span></span> | <span data-ttu-id="0b33c-116">Tendances des appareils</span><span class="sxs-lookup"><span data-stu-id="0b33c-116">Device trends</span></span>
<span data-ttu-id="0b33c-117">2</span><span class="sxs-lookup"><span data-stu-id="0b33c-117">2</span></span> | <span data-ttu-id="0b33c-118">Résumé de l’appareil (jour actuel)</span><span class="sxs-lookup"><span data-stu-id="0b33c-118">Device summary (current day)</span></span>
 
 
## <a name="device-trends"></a><span data-ttu-id="0b33c-119">Tendances des appareils</span><span class="sxs-lookup"><span data-stu-id="0b33c-119">Device trends</span></span> 
<span data-ttu-id="0b33c-120">Par défaut, les tendances des appareils affichent les informations de l’appareil de la période de 30 jours se terminant par la dernière journée entière.</span><span class="sxs-lookup"><span data-stu-id="0b33c-120">By default, the device trends displays device information from the 30-day period ending in the latest full day.</span></span> <span data-ttu-id="0b33c-121">Pour mieux prendre en compte les tendances qui se produisent dans votre organisation, vous pouvez affiner la période de rapport en ajustant la période indiquée.</span><span class="sxs-lookup"><span data-stu-id="0b33c-121">To gain better perspective on trends occurring in your organization, you can fine-tune the reporting period by adjusting the time period shown.</span></span> <span data-ttu-id="0b33c-122">Pour ajuster la période, sélectionnez une plage de temps dans les options de la baisse :</span><span class="sxs-lookup"><span data-stu-id="0b33c-122">To adjust the time period, select a time range from the drop-down options:</span></span>
 
- <span data-ttu-id="0b33c-123">30 jours</span><span class="sxs-lookup"><span data-stu-id="0b33c-123">30 days</span></span>
- <span data-ttu-id="0b33c-124">3 mois</span><span class="sxs-lookup"><span data-stu-id="0b33c-124">3 months</span></span>
- <span data-ttu-id="0b33c-125">6 mois</span><span class="sxs-lookup"><span data-stu-id="0b33c-125">6 months</span></span>
- <span data-ttu-id="0b33c-126">Personnalisé</span><span class="sxs-lookup"><span data-stu-id="0b33c-126">Custom</span></span>

>[!NOTE]
><span data-ttu-id="0b33c-127">Ces filtres sont appliqués uniquement à la section Tendances des appareils.</span><span class="sxs-lookup"><span data-stu-id="0b33c-127">These filters are only applied on the device trends section.</span></span> <span data-ttu-id="0b33c-128">Elle n’affecte pas la section récapitulatif de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0b33c-128">It doesn't affect the device summary section.</span></span>

## <a name="device-summary"></a><span data-ttu-id="0b33c-129">Résumé de l’appareil</span><span class="sxs-lookup"><span data-stu-id="0b33c-129">Device summary</span></span> 
<span data-ttu-id="0b33c-130">Alors que les tendances des appareils indiquent les tendances des appareils, le résumé de l’appareil affiche les informations d’appareil limitées au jour actuel.</span><span class="sxs-lookup"><span data-stu-id="0b33c-130">While the devices trends shows trending device information, the device summary shows device information scoped to the current day.</span></span> 

>[!NOTE]
><span data-ttu-id="0b33c-131">Les données reflétées dans la section récapitulatif sont limitées à 180 jours avant la date actuelle.</span><span class="sxs-lookup"><span data-stu-id="0b33c-131">The data reflected in the summary section is scoped to 180 days prior to the current date.</span></span> <span data-ttu-id="0b33c-132">Par exemple, si la date du jour est le 27 mars 2019, les données de la section récapitulatif reflétera les chiffres du 28 septembre 2018 au 27 mars 2019.</span><span class="sxs-lookup"><span data-stu-id="0b33c-132">For example if today's date is March 27, 2019, the data on the summary section will reflect numbers starting from September 28, 2018 to March 27, 2019.</span></span><br>
> <span data-ttu-id="0b33c-133">Le filtre appliqué à la section tendances n’est pas appliqué à la section récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="0b33c-133">The filter applied on the trends section is not applied on the summary section.</span></span> 
 
<span data-ttu-id="0b33c-134">La section Tendances des appareils vous permet d’aller jusqu’à la liste des appareils avec le filtre correspondant qui lui est appliqué.</span><span class="sxs-lookup"><span data-stu-id="0b33c-134">The device trends section allows you to drill down to the devices list with the corresponding filter applied to it.</span></span> <span data-ttu-id="0b33c-135">Par exemple, si vous cliquez sur la barre inactive de la carte d’état d’état du capteur, la liste des appareils affiche uniquement les appareils dont l’état du capteur est inactif.</span><span class="sxs-lookup"><span data-stu-id="0b33c-135">For example, clicking on the Inactive bar in the Sensor health state card will bring you the devices list with results showing only devices whose sensor status is inactive.</span></span> 
 
 
 
## <a name="device-attributes"></a><span data-ttu-id="0b33c-136">Attributs d’appareil</span><span class="sxs-lookup"><span data-stu-id="0b33c-136">Device attributes</span></span>
<span data-ttu-id="0b33c-137">Le rapport est composé de cartes qui affichent les attributs d’appareil suivants :</span><span class="sxs-lookup"><span data-stu-id="0b33c-137">The report is made up of cards that display the following device attributes:</span></span>
 
- <span data-ttu-id="0b33c-138">**État d’état**: affiche des informations sur l’état du capteur sur les appareils, en fournissant une vue agrégée des appareils actifs, qui rencontrent des problèmes de communication, qui sont inactifs ou où aucune donnée de capteur n’est visible.</span><span class="sxs-lookup"><span data-stu-id="0b33c-138">**Health state**: shows information about the sensor state on devices, providing an aggregated view of devices that are active, experiencing impaired communications, inactive, or where no sensor data is seen.</span></span>
  
- <span data-ttu-id="0b33c-139">**État antivirus des appareils Windows 10** actifs : indique le nombre d’appareils et l’état de l’Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0b33c-139">**Antivirus status for active Windows 10 devices**: shows the number of devices and status of Microsoft Defender Antivirus.</span></span>
    
- <span data-ttu-id="0b33c-140">**Plateformes de système d’exploitation**: affiche la distribution des plateformes de système d’exploitation qui existent au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0b33c-140">**OS platforms**: shows the distribution of OS platforms that exists within your organization.</span></span> 
 
- <span data-ttu-id="0b33c-141">**Versions de Windows 10**: affiche la distribution des appareils Windows 10 et de leurs versions dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0b33c-141">**Windows 10 versions**: shows the distribution of Windows 10 devices and their versions in your organization.</span></span>
 
 
 
## <a name="filter-data"></a><span data-ttu-id="0b33c-142">Filtrer les données</span><span class="sxs-lookup"><span data-stu-id="0b33c-142">Filter data</span></span>
 
<span data-ttu-id="0b33c-143">Utilisez les filtres fournis pour inclure ou exclure des appareils avec certains attributs.</span><span class="sxs-lookup"><span data-stu-id="0b33c-143">Use the provided filters to include or exclude devices with certain attributes.</span></span>

<span data-ttu-id="0b33c-144">Vous pouvez sélectionner plusieurs filtres à appliquer à partir des attributs d’appareil.</span><span class="sxs-lookup"><span data-stu-id="0b33c-144">You can select multiple filters to apply from the device attributes.</span></span> 
 
>[!NOTE]
><span data-ttu-id="0b33c-145">Ces filtres **s’appliquent à toutes** les cartes du rapport.</span><span class="sxs-lookup"><span data-stu-id="0b33c-145">These filters apply to **all** the cards in the report.</span></span>
 
<span data-ttu-id="0b33c-146">Par exemple, pour afficher des données sur les appareils Windows 10 avec l’état d’état d’état du capteur actif :</span><span class="sxs-lookup"><span data-stu-id="0b33c-146">For example, to show data about Windows 10 devices with Active sensor health state:</span></span>
 
1. <span data-ttu-id="0b33c-147">Sous **Filtres > l’état d'> du capteur actif.**</span><span class="sxs-lookup"><span data-stu-id="0b33c-147">Under **Filters > Sensor health state > Active**.</span></span>
2. <span data-ttu-id="0b33c-148">Sélectionnez **ensuite les plateformes de système > windows 10.**</span><span class="sxs-lookup"><span data-stu-id="0b33c-148">Then select **OS platforms > Windows 10**.</span></span>
3. <span data-ttu-id="0b33c-149">Sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="0b33c-149">Select **Apply**.</span></span>


## <a name="related-topic"></a><span data-ttu-id="0b33c-150">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="0b33c-150">Related topic</span></span>
- [<span data-ttu-id="0b33c-151">Rapport sur la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0b33c-151">Threat protection report</span></span>](threat-protection-reports.md)
