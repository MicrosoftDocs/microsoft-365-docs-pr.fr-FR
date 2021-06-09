---
title: Décision basée sur les résultats dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
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
description: Découvrez comment l’onglet Décider dans Advanced eDiscovery fournit des données qui peuvent vous aider à déterminer la taille correcte du jeu de révision des fichiers de cas.
ROBOTS: NOINDEX, NOFOLLOW
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 7a4c2fe891a48451d9b8d852f603b225ab7b080d
ms.sourcegitcommit: 5ba0015c1554048f817fdfdc85359eee1368da64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "49769149"
---
# <a name="decisions-based-on-relevance-results-in-advanced-ediscovery"></a><span data-ttu-id="e6016-103">Décisions basées sur la pertinence des résultats dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="e6016-103">Decisions based on Relevance results in Advanced eDiscovery</span></span>
  
<span data-ttu-id="e6016-104">Dans le module Pertinence d’Advanced eDiscovery, l’onglet Décider fournit des informations supplémentaires pour l’affichage et l’utilisation des statistiques de prise de décision pour déterminer la taille du jeu de fichiers de cas à réviser.</span><span class="sxs-lookup"><span data-stu-id="e6016-104">In the Relevance module in Advanced eDiscovery, the Decide tab provides additional information for viewing and using decision-support statistics for determining the size of the review set of case files.</span></span>
  
## <a name="using-the-decide-tab"></a><span data-ttu-id="e6016-105">Utilisation de l’onglet Décider</span><span class="sxs-lookup"><span data-stu-id="e6016-105">Using the Decide tab</span></span>

![Décision de pertinence](../media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
<span data-ttu-id="e6016-107">Cet onglet comprend les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="e6016-107">This tab includes the following components:</span></span>
  
- <span data-ttu-id="e6016-108">**Problème**: à partir de là, vous pouvez sélectionner le problème d’intérêt dans la liste.</span><span class="sxs-lookup"><span data-stu-id="e6016-108">**Issue**: From here, you can select the issue of interest from the list.</span></span>

- <span data-ttu-id="e6016-109">**Taux de révision/rappel :** comparaisons de la révision Advanced eDiscovery en fonction des scores de pertinence.</span><span class="sxs-lookup"><span data-stu-id="e6016-109">**Review-recall ratio**: Comparisons of Advanced eDiscovery review according to Relevance scores.</span></span> <span data-ttu-id="e6016-110">Le point de coupure dans le graphique représente le pourcentage de fichiers à réviser, mappé à un score de pertinence.</span><span class="sxs-lookup"><span data-stu-id="e6016-110">The Cutoff point in the chart represents the percentage of files to review, mapped to a Relevance score.</span></span> <span data-ttu-id="e6016-111">Il est utilisé dans la phase test de pertinence et comme seuil d’exportation pour l’élimination.</span><span class="sxs-lookup"><span data-stu-id="e6016-111">This is used in the Relevance Test phase and as an Export threshold for culling.</span></span> <span data-ttu-id="e6016-112">Le point de coupure par défaut, pour le nombre de fichiers à réviser, est au point où l’équilibre entre Rappel et Précision est optimal.</span><span class="sxs-lookup"><span data-stu-id="e6016-112">The default cutoff point, for the number of files to review is at the point in which the balance between Recall and Precision is optimal.</span></span> <span data-ttu-id="e6016-113">Le point de coupure réel doit être déterminé par l’utilisateur en fonction des objectifs et du compromis de coût (%review) et du risque (%recall).</span><span class="sxs-lookup"><span data-stu-id="e6016-113">The actual cutoff point should be determined by the user depending on objectives and the cost tradeoff (%review) and risk (%recall).</span></span> <span data-ttu-id="e6016-114">À l’aide du curseur, vous pouvez ajuster le point de coupure et voir l’effet sur le graphique et les paramètres, lors de l’ajustement du pourcentage de fichiers pertinents à récupérer et avant de valider une décision.</span><span class="sxs-lookup"><span data-stu-id="e6016-114">Using the slider, you can adjust the cutoff point and see the effect on the graph and parameters, when adjusting the percent of relevant files to be retrieved, and before validating a decision.</span></span>

- <span data-ttu-id="e6016-115">**Parameters**: Review, Recall, Next relevant and Total cost parameters are cumulative calculated statistics pertaining to the review set in relation to the collection for the entire case.</span><span class="sxs-lookup"><span data-stu-id="e6016-115">**Parameters**: Review, Recall, Next relevant and Total cost parameters are cumulative calculated statistics pertaining to the review set in relation to the collection for the entire case.</span></span> <span data-ttu-id="e6016-116">Les définitions de ces paramètres sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6016-116">Definitions for these parameters are as follows:</span></span>

  - <span data-ttu-id="e6016-117">**Révision**: Pourcentage de fichiers à réviser en fonction de ce cutoff.</span><span class="sxs-lookup"><span data-stu-id="e6016-117">**Review**: Percentage of files to review based on this cutoff.</span></span>

  - <span data-ttu-id="e6016-118">**Rappel**: pourcentage de fichiers pertinents dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="e6016-118">**Recall**: Percentage of relevant files in the review set.</span></span>

  - <span data-ttu-id="e6016-119">**Pertinence suivante**: coût de révision et d’identification d’un autre fichier pertinent qui n’est pas actuellement dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="e6016-119">**Next relevant**: Cost to review and identify another relevant file that is not currently in the review set.</span></span>

  - <span data-ttu-id="e6016-120">**Coût total**: coût pour la révision de ce pourcentage des fichiers de cas.</span><span class="sxs-lookup"><span data-stu-id="e6016-120">**Total cost**: Cost for reviewing this percentage of the case files.</span></span> <span data-ttu-id="e6016-121">Les paramètres de coût peuvent être définies par le gestionnaire de cas.</span><span class="sxs-lookup"><span data-stu-id="e6016-121">Cost parameter settings can be set by the Case manager.</span></span>

  - <span data-ttu-id="e6016-122">**Répartition par score de pertinence**: les fichiers dans l’affichage gris foncé à gauche sont inférieurs au score de seuil.</span><span class="sxs-lookup"><span data-stu-id="e6016-122">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score.</span></span> <span data-ttu-id="e6016-123">Une info-conseil affiche le score de pertinence et le pourcentage connexe de fichiers dans le jeu de fichiers de révision par rapport au nombre total de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e6016-123">A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>

<span data-ttu-id="e6016-124">Le volet **Détails développé** affiche plus de détails.</span><span class="sxs-lookup"><span data-stu-id="e6016-124">The expanded **Details** pane displays more details.</span></span> <span data-ttu-id="e6016-125">Les fichiers des figures de collection n’incluent pas les fichiers vides ou les fichiers nebules.</span><span class="sxs-lookup"><span data-stu-id="e6016-125">Files in collection figures do not include empty or nebulous files.</span></span> <span data-ttu-id="e6016-126">Les figures de fichiers de famille représentent des fichiers qui ne sont pas chargés en Pertinence, mais qui sont toujours comptés dans le cadre de la famille.</span><span class="sxs-lookup"><span data-stu-id="e6016-126">Family files figures represent files that are not loaded in Relevance, yet still counted as part of the family.</span></span>
