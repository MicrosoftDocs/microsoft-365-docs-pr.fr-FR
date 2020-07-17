---
title: Décision basée sur les résultats dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
titleSuffix: Office 365
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Découvrez comment l’onglet décider de Microsoft 365 Advanced eDiscovery fournit des données qui peuvent vous aider à déterminer la taille correcte de l’ensemble de révision des fichiers de cas. '
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 0139bc0505150a4d27aaca97b9b253f2043d649f
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44817903"
---
# <a name="decision-based-on-the-results-in-advanced-ediscovery-classic"></a><span data-ttu-id="472ed-103">Décision basée sur les résultats dans Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="472ed-103">Decision based on the results in Advanced eDiscovery (classic)</span></span>

> [!NOTE]
> <span data-ttu-id="472ed-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="472ed-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
 <span data-ttu-id="472ed-106">Dans Advanced eDiscovery, l’onglet décider fournit des informations supplémentaires sur l’affichage et l’utilisation des statistiques d’aide à la décision pour déterminer la taille de l’ensemble de révision des fichiers de cas.</span><span class="sxs-lookup"><span data-stu-id="472ed-106">In Advanced eDiscovery, the Decide tab provides additional information for viewing and using decision-support statistics for determining the size of the review set of case files.</span></span> 
  
## <a name="using-the-decide-tab"></a><span data-ttu-id="472ed-107">Utilisation de l’onglet décider</span><span class="sxs-lookup"><span data-stu-id="472ed-107">Using the Decide tab</span></span>

![Décision de pertinence](../media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
<span data-ttu-id="472ed-109">Cet onglet comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="472ed-109">This tab includes the following:</span></span>
  
- <span data-ttu-id="472ed-110">**Problème**: à partir de là, vous pouvez sélectionner le problème d’intérêt dans la liste.</span><span class="sxs-lookup"><span data-stu-id="472ed-110">**Issue**: From here, you can select the issue of interest from the list.</span></span> 
    
- <span data-ttu-id="472ed-111">**Review-ratio de rappel**: Comparaison de la révision eDiscovery avancée en fonction des scores de pertinence.</span><span class="sxs-lookup"><span data-stu-id="472ed-111">**Review-recall ratio**: Comparison of Advanced eDiscovery review according to Relevance scores.</span></span> <span data-ttu-id="472ed-112">Le point de coupure dans le graphique représente le pourcentage de fichiers à examiner, mappé à un score de pertinence.</span><span class="sxs-lookup"><span data-stu-id="472ed-112">The Cutoff point in the chart represents the percentage of files to review, mapped to a Relevance score.</span></span> <span data-ttu-id="472ed-113">Il est utilisé dans la phase test de pertinence et en tant que seuil d’exportation pour l’élimination.</span><span class="sxs-lookup"><span data-stu-id="472ed-113">This is used in the Relevance Test phase and as an Export threshold for culling.</span></span> <span data-ttu-id="472ed-114">Le point de démarcation par défaut, pour le nombre de fichiers à réviser, se trouve à l’endroit où l’équilibre entre rappel et précision est optimal.</span><span class="sxs-lookup"><span data-stu-id="472ed-114">The default cutoff point, for the number of files to review is at the point in which the balance between Recall and Precision is optimal.</span></span> <span data-ttu-id="472ed-115">Le point de démarcation réel doit être déterminé par l’utilisateur en fonction des objectifs et du coût compromis (pourcentage de révision) et du risque (pourcentage de rappel). À l’aide du curseur, vous pouvez ajuster le point de coupure et observer l’effet sur le graphique et les paramètres, lors de l’ajustement du pourcentage de fichiers pertinents à extraire, et avant la validation d’une décision.</span><span class="sxs-lookup"><span data-stu-id="472ed-115">The actual cutoff point should be determined by the user depending on objectives and the cost tradeoff (%review) and risk (%recall).Using the slider, you can adjust the cutoff point and see the effect on the graph and parameters, when adjusting the percent of relevant files to be retrieved, and before validating a decision.</span></span>
    
- <span data-ttu-id="472ed-116">**Paramètres**: Review, Recall, les paramètres de coût total et pertinents suivants sont des statistiques calculées cumulatives relatives au jeu de révision en relation avec la collection pour l’ensemble du cas.</span><span class="sxs-lookup"><span data-stu-id="472ed-116">**Parameters**: Review, Recall, Next relevant and Total cost parameters are cumulative calculated statistics pertaining to the review set in relation to the collection for the entire case.</span></span> <span data-ttu-id="472ed-117">Les définitions de ces paramètres sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="472ed-117">Definitions for these parameters are as follows:</span></span>
    
    <span data-ttu-id="472ed-118">**Révision**: pourcentage de fichiers à vérifier en fonction de ce seuil de troncature.</span><span class="sxs-lookup"><span data-stu-id="472ed-118">**Review**: Percentage of files to review based on this cutoff.</span></span> 
    
    <span data-ttu-id="472ed-119">**Rappel**: pourcentage de fichiers pertinents dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="472ed-119">**Recall**: Percentage of relevant files in the review set.</span></span> 
    
    <span data-ttu-id="472ed-120">**Suivant**: coût de révision et d’identification d’un fichier supplémentaire pertinent qui n’est pas actuellement dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="472ed-120">**Next relevant**: Cost to review and identify an additional relevant file that is not currently in the review set.</span></span> 
    
    <span data-ttu-id="472ed-121">**Coût total**: coût de révision de ce pourcentage des fichiers de cas.</span><span class="sxs-lookup"><span data-stu-id="472ed-121">**Total cost**: Cost for reviewing this percentage of the case files.</span></span> <span data-ttu-id="472ed-122">Les paramètres de coût des paramètres peuvent être définis par le gestionnaire de cas.</span><span class="sxs-lookup"><span data-stu-id="472ed-122">Cost parameter settings can be set by the Case manager.</span></span>
    
- <span data-ttu-id="472ed-123">**Répartition par score de pertinence**: les fichiers dans l’affichage gris foncé vers la gauche sont en dessous du score de coupure.</span><span class="sxs-lookup"><span data-stu-id="472ed-123">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score.</span></span> <span data-ttu-id="472ed-124">Une info-bulle affiche le score de pertinence et le pourcentage de fichiers correspondant dans le jeu de fichiers de révision en relation avec le nombre total de fichiers.</span><span class="sxs-lookup"><span data-stu-id="472ed-124">A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
<span data-ttu-id="472ed-125">Le volet de détails étendu affiche des détails supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="472ed-125">The expanded Details pane displays additional details.</span></span> <span data-ttu-id="472ed-126">Les fichiers dans les figures de collection n’incluent pas les fichiers vides ou nebulous.</span><span class="sxs-lookup"><span data-stu-id="472ed-126">Files in collection figures do not include empty or nebulous files.</span></span> <span data-ttu-id="472ed-127">Les figures des fichiers de famille représentent des fichiers qui ne sont pas chargés en pertinence, mais qui sont toujours comptés dans le cadre de la famille.</span><span class="sxs-lookup"><span data-stu-id="472ed-127">Family files figures represent files that are not loaded in Relevance, yet still counted as part of the family.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="472ed-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="472ed-128">Related topics</span></span>

[<span data-ttu-id="472ed-129">Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="472ed-129">Advanced eDiscovery (classic)</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="472ed-130">Présentation de l’évaluation en matière de pertinence</span><span class="sxs-lookup"><span data-stu-id="472ed-130">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="472ed-131">Balisage et évaluation</span><span class="sxs-lookup"><span data-stu-id="472ed-131">Tagging and Assessment</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="472ed-132">Formation à la pertinence</span><span class="sxs-lookup"><span data-stu-id="472ed-132">Performing Relevance training</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="472ed-133">Analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="472ed-133">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="472ed-134">Évaluation de l’analyse de pertinence</span><span class="sxs-lookup"><span data-stu-id="472ed-134">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

