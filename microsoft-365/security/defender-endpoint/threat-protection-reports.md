---
title: Rapport sur la protection contre les menaces dans Microsoft Defender ATP
description: Suivre les détections, catégories et gravité des alertes à l’aide du rapport de protection contre les menaces
keywords: détection d’alerte, source, alerte par catégorie, gravité de l’alerte, classification des alertes, détermination
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
ms.openlocfilehash: 4ecd2df31e1e03da5134d3d4180dcba75d3cee26
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51183836"
---
# <a name="threat-protection-report-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="6bbad-104">Rapport sur la protection contre les menaces dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6bbad-104">Threat protection report in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="6bbad-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6bbad-105">**Applies to:**</span></span>
- [<span data-ttu-id="6bbad-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6bbad-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6bbad-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6bbad-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="6bbad-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="6bbad-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="6bbad-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6bbad-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 

<span data-ttu-id="6bbad-110">Le rapport sur la protection contre les menaces fournit des informations de haut niveau sur les alertes générées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6bbad-110">The threat protection report provides high-level information about alerts generated in your organization.</span></span> <span data-ttu-id="6bbad-111">Le rapport inclut des informations de tendance montrant les sources de détection, les catégories, les gravités, les états, les classifications et les déterminations des alertes dans le temps.</span><span class="sxs-lookup"><span data-stu-id="6bbad-111">The report includes trending information showing the detection sources, categories, severities, statuses, classifications, and determinations of alerts across time.</span></span>

<span data-ttu-id="6bbad-112">Le tableau de bord est structuré en deux sections :</span><span class="sxs-lookup"><span data-stu-id="6bbad-112">The dashboard is structured into two sections:</span></span>

![Image du rapport sur la protection contre les menaces](images/threat-protection-reports.png)

<span data-ttu-id="6bbad-114">Section</span><span class="sxs-lookup"><span data-stu-id="6bbad-114">Section</span></span> | <span data-ttu-id="6bbad-115">Description</span><span class="sxs-lookup"><span data-stu-id="6bbad-115">Description</span></span> 
:---|:---
<span data-ttu-id="6bbad-116">1</span><span class="sxs-lookup"><span data-stu-id="6bbad-116">1</span></span> | <span data-ttu-id="6bbad-117">Tendances des alertes</span><span class="sxs-lookup"><span data-stu-id="6bbad-117">Alerts trends</span></span>
<span data-ttu-id="6bbad-118">2</span><span class="sxs-lookup"><span data-stu-id="6bbad-118">2</span></span> | <span data-ttu-id="6bbad-119">Résumé des alertes</span><span class="sxs-lookup"><span data-stu-id="6bbad-119">Alert summary</span></span>

## <a name="alert-trends"></a><span data-ttu-id="6bbad-120">Tendances des alertes</span><span class="sxs-lookup"><span data-stu-id="6bbad-120">Alert trends</span></span>
<span data-ttu-id="6bbad-121">Par défaut, les tendances des alertes affichent les informations d’alerte de la période de 30 jours se terminant par la dernière journée entière.</span><span class="sxs-lookup"><span data-stu-id="6bbad-121">By default, the alert trends display alert information from the 30-day period ending in the latest full day.</span></span> <span data-ttu-id="6bbad-122">Pour mieux prendre en compte les tendances qui se produisent dans votre organisation, vous pouvez affiner la période de rapport en ajustant la période indiquée.</span><span class="sxs-lookup"><span data-stu-id="6bbad-122">To gain better perspective on trends occurring in your organization, you can fine-tune the reporting period by adjusting the time period shown.</span></span> <span data-ttu-id="6bbad-123">Pour ajuster la période, sélectionnez une plage de temps dans les options de la baisse :</span><span class="sxs-lookup"><span data-stu-id="6bbad-123">To adjust the time period, select a time range from the drop-down options:</span></span>

- <span data-ttu-id="6bbad-124">30 jours</span><span class="sxs-lookup"><span data-stu-id="6bbad-124">30 days</span></span>
- <span data-ttu-id="6bbad-125">3 mois</span><span class="sxs-lookup"><span data-stu-id="6bbad-125">3 months</span></span>
- <span data-ttu-id="6bbad-126">6 mois</span><span class="sxs-lookup"><span data-stu-id="6bbad-126">6 months</span></span>
- <span data-ttu-id="6bbad-127">Personnalisé</span><span class="sxs-lookup"><span data-stu-id="6bbad-127">Custom</span></span>

>[!NOTE]
><span data-ttu-id="6bbad-128">Ces filtres sont appliqués uniquement à la section tendances des alertes.</span><span class="sxs-lookup"><span data-stu-id="6bbad-128">These filters are only applied on the alert trends section.</span></span> <span data-ttu-id="6bbad-129">Elle n’affecte pas la section récapitulatif des alertes.</span><span class="sxs-lookup"><span data-stu-id="6bbad-129">It doesn't affect the alert summary section.</span></span>


## <a name="alert-summary"></a><span data-ttu-id="6bbad-130">Résumé des alertes</span><span class="sxs-lookup"><span data-stu-id="6bbad-130">Alert summary</span></span>
<span data-ttu-id="6bbad-131">Alors que les tendances des alertes indiquent des informations d’alerte de tendance, le résumé de l’alerte affiche les informations d’alerte limitées au jour actuel.</span><span class="sxs-lookup"><span data-stu-id="6bbad-131">While the alert trends shows trending alert information, the alert summary shows alert information scoped to the current day.</span></span>

 <span data-ttu-id="6bbad-132">Le résumé des alertes vous permet d’aller jusqu’à une file d’attente d’alertes particulière avec le filtre correspondant qui lui est appliqué.</span><span class="sxs-lookup"><span data-stu-id="6bbad-132">The alert summary allows you to drill down to a particular alert queue with the corresponding filter applied to it.</span></span> <span data-ttu-id="6bbad-133">Par exemple, si vous cliquez sur la barre EDR dans la carte sources de détection, la file d’attente des alertes affiche uniquement les alertes générées à partir des détections EDR.</span><span class="sxs-lookup"><span data-stu-id="6bbad-133">For example, clicking on the EDR bar in the Detection sources card will bring you the alerts queue with results showing only alerts generated from EDR detections.</span></span> 

>[!NOTE]
><span data-ttu-id="6bbad-134">Les données reflétées dans la section récapitulatif sont limitées à 180 jours avant la date actuelle.</span><span class="sxs-lookup"><span data-stu-id="6bbad-134">The data reflected in the summary section is scoped to 180 days prior to the current date.</span></span> <span data-ttu-id="6bbad-135">Par exemple, si la date du jour est le 5 novembre 2019, les données de la section récapitulatif reflétera les numéros du 5 mai 2019 au 5 novembre 2019.</span><span class="sxs-lookup"><span data-stu-id="6bbad-135">For example if today's date is November 5, 2019, the data on the summary section will reflect numbers starting from May 5, 2019 to November 5, 2019.</span></span><br>
> <span data-ttu-id="6bbad-136">Le filtre appliqué à la section tendances n’est pas appliqué à la section récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="6bbad-136">The filter applied on the trends section is not applied on the summary section.</span></span> 

## <a name="alert-attributes"></a><span data-ttu-id="6bbad-137">Attributs d’alerte</span><span class="sxs-lookup"><span data-stu-id="6bbad-137">Alert attributes</span></span>
<span data-ttu-id="6bbad-138">Le rapport est composé de cartes qui affichent les attributs d’alerte suivants :</span><span class="sxs-lookup"><span data-stu-id="6bbad-138">The report is made up of cards that display the following alert attributes:</span></span>

- <span data-ttu-id="6bbad-139">**Sources de détection**: affiche des informations sur les capteurs et les technologies de détection qui fournissent les données utilisées par Microsoft Defender pour le point de terminaison pour déclencher des alertes.</span><span class="sxs-lookup"><span data-stu-id="6bbad-139">**Detection sources**: shows information about the sensors and detection technologies that provide the data used by Microsoft Defender for Endpoint to trigger alerts.</span></span>

- <span data-ttu-id="6bbad-140">**Catégories de menaces**: indique les types d’activité de menace ou d’attaque qui ont déclenché des alertes, indiquant les zones de focus possibles pour vos opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6bbad-140">**Threat categories**: shows the types of threat or attack activity that triggered alerts, indicating possible focus areas for your security operations.</span></span>

- <span data-ttu-id="6bbad-141">**Gravité :** indique le niveau de gravité des alertes, indiquant l’impact potentiel des menaces collectives sur votre organisation et le niveau de réponse nécessaire pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="6bbad-141">**Severity**: shows the severity level of alerts, indicating the collective potential impact of threats to your organization and the level of response needed to address them.</span></span>

- <span data-ttu-id="6bbad-142">**État**: affiche l’état de résolution des alertes, indiquant l’efficacité de vos réponses d’alerte manuelles et de la correction automatisée (si activée).</span><span class="sxs-lookup"><span data-stu-id="6bbad-142">**Status**: shows the resolution status of alerts, indicating the efficiency of your manual alert responses and of automated remediation (if enabled).</span></span> 

- <span data-ttu-id="6bbad-143">**Classification &** détermination : indique comment vous avez classé les alertes lors de leur résolution, si vous les avez classées comme menaces réelles (alertes vraies) ou comme détections incorrectes (fausses alertes).</span><span class="sxs-lookup"><span data-stu-id="6bbad-143">**Classification & determination**: shows how you have classified alerts upon resolution, whether you have classified them as actual threats (true alerts) or as incorrect detections (false alerts).</span></span> <span data-ttu-id="6bbad-144">Ces cartes indiquent également la détermination des alertes résolues, fournissant des informations supplémentaires telles que les types de menaces réelles détectées ou les activités légitimes détectées de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6bbad-144">These cards also show the determination of resolved alerts, providing additional insight like the types of actual threats found or the legitimate activities that were incorrectly detected.</span></span>


 

## <a name="filter-data"></a><span data-ttu-id="6bbad-145">Filtrer les données</span><span class="sxs-lookup"><span data-stu-id="6bbad-145">Filter data</span></span>

<span data-ttu-id="6bbad-146">Utilisez les filtres fournis pour inclure ou exclure des alertes avec certains attributs.</span><span class="sxs-lookup"><span data-stu-id="6bbad-146">Use the provided filters to include or exclude alerts with certain attributes.</span></span>

>[!NOTE]
><span data-ttu-id="6bbad-147">Ces filtres **s’appliquent à toutes** les cartes du rapport.</span><span class="sxs-lookup"><span data-stu-id="6bbad-147">These filters apply to **all** the cards in the report.</span></span>

<span data-ttu-id="6bbad-148">Par exemple, pour afficher les données relatives aux alertes de gravité élevée uniquement :</span><span class="sxs-lookup"><span data-stu-id="6bbad-148">For example, to show data about high-severity alerts only:</span></span>

1. <span data-ttu-id="6bbad-149">Sous **Filtres > gravité**, sélectionnez **Élevé**</span><span class="sxs-lookup"><span data-stu-id="6bbad-149">Under **Filters > Severity**, select **High**</span></span>
2. <span data-ttu-id="6bbad-150">Assurez-vous que toutes les autres options sous **Gravité** sont désélectionnés.</span><span class="sxs-lookup"><span data-stu-id="6bbad-150">Ensure that all other options under **Severity** are deselected.</span></span>
3. <span data-ttu-id="6bbad-151">Sélectionnez **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="6bbad-151">Select **Apply**.</span></span> 

## <a name="related-topic"></a><span data-ttu-id="6bbad-152">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="6bbad-152">Related topic</span></span>
- [<span data-ttu-id="6bbad-153">Rapport sur l’état et la conformité de l’appareil</span><span class="sxs-lookup"><span data-stu-id="6bbad-153">Device health and compliance report</span></span>](machine-reports.md)
