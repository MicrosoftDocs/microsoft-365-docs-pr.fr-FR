---
title: Suivre l’analyse de pertinence dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
titleSuffix: Office 365
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 3ab1e2c3-28cf-4bf5-b0a8-c0222f32bdf5
ROBOTS: NOINDEX, NOFOLLOW
description: Découvrez comment afficher et interpréter l’état et les résultats de l’entraînement Pertinence pour les problèmes de Advanced eDiscovery.
ms.openlocfilehash: 224337969b5e662d45c5b804fa5a0ee045f4fb84
ms.sourcegitcommit: 5ba0015c1554048f817fdfdc85359eee1368da64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "49769179"
---
# <a name="track-relevance-analysis-in-advanced-ediscovery"></a><span data-ttu-id="7255a-103">Suivre l’analyse de pertinence dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7255a-103">Track Relevance analysis in Advanced eDiscovery</span></span>
  
<span data-ttu-id="7255a-104">Dans Advanced eDiscovery, l’onglet Suivi de pertinence affiche la validité calculée de la formation Pertinence effectuée dans l’onglet Balise et indique l’étape suivante à effectuer dans le processus de formation itérative en Pertinence.</span><span class="sxs-lookup"><span data-stu-id="7255a-104">In Advanced eDiscovery, the Relevance Track tab displays the calculated validity of the Relevance training performed in the Tag tab and indicates the next step to take in the iterative training process in Relevance.</span></span> 
  
## <a name="tracking-relevance-training-status"></a><span data-ttu-id="7255a-105">Suivi de l’état d’entraînement Pertinence</span><span class="sxs-lookup"><span data-stu-id="7255a-105">Tracking Relevance training status</span></span>

1. <span data-ttu-id="7255a-106">Consultez les détails suivants dans suivi de pertinence pour les problèmes de cas, comme illustré dans l’exemple suivant d’une boîte de dialogue Nom **du** problème ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7255a-106">View the following details in Relevance Track for the case issues, as shown in the following example of an **Issue name** dialog below.</span></span>

   - <span data-ttu-id="7255a-107">**Évaluation**: cet indicateur de progression indique dans quelle mesure l’entraînement Pertinence effectué à ce stade a atteint l’objectif d’évaluation en termes de marge d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7255a-107">**Assessment**: This progress indicator shows to what degree the Relevance training performed to this point has achieved the assessment target in terms of margin of error.</span></span> <span data-ttu-id="7255a-108">La richesse des résultats de l’entraînement Pertinence s’affiche également.</span><span class="sxs-lookup"><span data-stu-id="7255a-108">The richness of the Relevance training results is also displayed.</span></span>

   - <span data-ttu-id="7255a-109">**Formation**: cet indicateur de progression et cette info-conseil codés en couleur indiquent la stabilité des résultats de l’entraînement Pertinence et une échelle numérique indiquant le nombre d’exemples d’entraînement Pertinence marqués pour chaque problème.</span><span class="sxs-lookup"><span data-stu-id="7255a-109">**Training**: This color-coded progress indicator and tool-tip indicates the Relevance training results stability and a numeric scale showing the number of Relevance training samples tagged for each issue.</span></span> <span data-ttu-id="7255a-110">L’expert surveille la progression du processus itératif de formation Pertinence.</span><span class="sxs-lookup"><span data-stu-id="7255a-110">The expert monitors the progress of the iterative Relevance training process.</span></span> 
  
   - <span data-ttu-id="7255a-111">**Calcul par lot**: cet indicateur de progression fournit des informations sur la fin du calcul par lots.</span><span class="sxs-lookup"><span data-stu-id="7255a-111">**Batch calculation**: This progress indicator provides information about the completion of Batch calculation.</span></span>
  
   - <span data-ttu-id="7255a-112">**Étape suivante**: affiche la recommandation pour l’étape suivante à effectuer.</span><span class="sxs-lookup"><span data-stu-id="7255a-112">**Next step**: Displays the recommendation for the next step to be performed.</span></span> 
  
    <span data-ttu-id="7255a-113">Dans l’exemple, une évaluation réussie d’un problème est affichée, indiquée par l’indicateur de progression de couleur terminé et la coche.</span><span class="sxs-lookup"><span data-stu-id="7255a-113">In the example, a successfully completed Assessment for an issue is shown, indicated by the completed color progress indicator and the checkmark.</span></span> <span data-ttu-id="7255a-114">Le marquage est en cours, mais le cas est toujours considéré comme instable (état de stabilité également indiqué dans une info-conseil).</span><span class="sxs-lookup"><span data-stu-id="7255a-114">Tagging is underway, but the case is still considered unstable (stability status also shown in a tool-tip).</span></span> <span data-ttu-id="7255a-115">La recommandation de l’étape suivante est « Formation ».</span><span class="sxs-lookup"><span data-stu-id="7255a-115">The next step recommendation is "Training".</span></span> 
  
    ![Formation de suivi de pertinence étape 1](../media/a00fe607-680a-48eb-9d61-4565319f7ab6.png)
  
    <span data-ttu-id="7255a-117">La vue étendue affiche des informations et des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7255a-117">The expanded view displays additional information and options.</span></span> <span data-ttu-id="7255a-118">La marge d’erreur actuelle affichée est la marge d’erreur du rappel dans l’état actuel de l’évaluation, compte tenu des fichiers d’évaluation existants (déjà balisé).</span><span class="sxs-lookup"><span data-stu-id="7255a-118">The displayed current error margin is the error margin of the recall in the current state of assessment, given the existing (already tagged) assessment files.</span></span>
  
    > [!NOTE]
    >  <span data-ttu-id="7255a-119">L’étape d’évaluation peut  être contourné en effanant la case à cocher Évaluation par problème, puis pour « tous les problèmes ».</span><span class="sxs-lookup"><span data-stu-id="7255a-119">The Assessment stage can be bypassed by clearing the **Assessment** check box per issue and then for "all issues".</span></span> <span data-ttu-id="7255a-120">Toutefois, il n’y aura donc pas de statistiques pour ce problème.</span><span class="sxs-lookup"><span data-stu-id="7255a-120">However, as a result, there will be no statistics for this issue.</span></span> <span data-ttu-id="7255a-121">> la case à cocher **d’évaluation** ne peut être effectuée qu’avant l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="7255a-121">> Clearing the **Assessment** check box can only be done before assessment is performed.</span></span> <span data-ttu-id="7255a-122">Lorsque plusieurs problèmes existent dans un cas, l’évaluation est contourné uniquement si la case à cocher est effacée pour chaque problème</span><span class="sxs-lookup"><span data-stu-id="7255a-122">Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
    <span data-ttu-id="7255a-123">Lorsque l’évaluation n’est pas terminée avec le premier exemple de fichiers, l’évaluation peut être l’étape suivante pour baliser d’autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="7255a-123">When assessment is not completed with the first sample set of files, assessment might be the next step for tagging more files.</span></span>
  
    <span data-ttu-id="7255a-124">Dans **la piste de pertinence,** l’indicateur de progression de la formation et l’info-conseil indiquent le nombre estimé d’échantillons supplémentaires nécessaires pour atteindre la \> stabilité.</span><span class="sxs-lookup"><span data-stu-id="7255a-124">In **Relevance** \> **Track**, the training progress indicator and tool-tip indicate the estimated number of additional samples needed to reach stability.</span></span> <span data-ttu-id="7255a-125">Cette estimation fournit des instructions pour la formation supplémentaire nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7255a-125">This estimate provides a guideline for the additional training needed.</span></span>
  
    ![Formation de suivi de pertinence](../media/98dbc3f5-5238-4d73-9f88-1aa4d77ea729.png)
  
2. <span data-ttu-id="7255a-127">Lorsque vous avez terminé le marquage et si vous avez besoin de continuer la formation, cliquez sur **Formation.**</span><span class="sxs-lookup"><span data-stu-id="7255a-127">When you're done tagging and if you need to continue training, click **Training**.</span></span> <span data-ttu-id="7255a-128">Un autre exemple de jeu de fichiers est généré à partir du jeu de fichiers chargé pour une formation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="7255a-128">Another sample set of files is generated from the loaded file set for additional training.</span></span> <span data-ttu-id="7255a-129">Vous êtes ensuite renvoyé à l’onglet Balise pour baliser et former d’autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="7255a-129">You are then returned to the Tag tab to tag and train more files.</span></span>

### <a name="reaching-stable-training-levels"></a><span data-ttu-id="7255a-130">Atteindre des niveaux de formation stables</span><span class="sxs-lookup"><span data-stu-id="7255a-130">Reaching stable training levels</span></span>

<span data-ttu-id="7255a-131">Une fois que les fichiers d’évaluation ont atteint un niveau stable de formation, Advanced eDiscovery est prêt pour le calcul par lots.</span><span class="sxs-lookup"><span data-stu-id="7255a-131">After the assessment files have attained a stable level of training, Advanced eDiscovery is ready for Batch calculation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7255a-132">En règle générale, après trois exemples de formation stables, l’étape suivante est « Calcul par lot ».</span><span class="sxs-lookup"><span data-stu-id="7255a-132">Usually, after three stable training samples, the next step is "Batch calculation".</span></span> <span data-ttu-id="7255a-133">Il peut y avoir des exceptions, par exemple, lorsque des modifications ont été apportées au marquage des fichiers à partir d’exemples précédents ou lorsque des fichiers d’amorçage ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="7255a-133">There may be exceptions, for example, when there were changes to the tagging of files from earlier samples or when seed files were added.</span></span> 
  
### <a name="performing-batch-calculation"></a><span data-ttu-id="7255a-134">Effectuer le calcul par lots</span><span class="sxs-lookup"><span data-stu-id="7255a-134">Performing Batch calculation</span></span>

<span data-ttu-id="7255a-135">Le calcul par lot est exécuté en tant qu’étape suivante une fois la formation terminée (lorsqu’un état stable de formation est affiché par la barre de progression, une coche et un état stable dans l’info-conseil).) Le calcul par lots applique les connaissances acquises lors de l’entraînement Pertinence à l’ensemble de la population de fichiers, afin d’évaluer la pertinence des fichiers et d’affecter des scores de pertinence.</span><span class="sxs-lookup"><span data-stu-id="7255a-135">Batch calculation is executed as the next step after training is successfully completed (when a stable training status is shown by the progress bar, a checkmark and stable status in the tool-tip.) Batch calculation applies the knowledge acquired during the Relevance training to the entire file population, to assess the files' relevance and to assign Relevance scores.</span></span>
  
<span data-ttu-id="7255a-136">Lorsqu’il y a plusieurs problèmes, le calcul par lot est effectué par problème.</span><span class="sxs-lookup"><span data-stu-id="7255a-136">When there is more than one issue, Batch calculation is done per issue.</span></span> <span data-ttu-id="7255a-137">Pendant le calcul par lots, la progression est surveillée lors du traitement de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="7255a-137">During Batch calculation, progress is monitored while processing all of the files.</span></span> 
  
<span data-ttu-id="7255a-138">Ici, l’étape suivante recommandée est « Aucun », ce qui indique qu’aucune formation itérative supplémentaire sur la pertinence n’est requise à ce stade.</span><span class="sxs-lookup"><span data-stu-id="7255a-138">Here, the recommended next step is "None", which indicates that no additional iterative Relevance training is required at this point.</span></span> <span data-ttu-id="7255a-139">La phase suivante est **l’onglet Déterminer \> la** pertinence.</span><span class="sxs-lookup"><span data-stu-id="7255a-139">The next phase is the **Relevance \> Decide** tab.</span></span> 
  
<span data-ttu-id="7255a-140">Si vous souhaitez importer de nouveaux fichiers après le calcul par lots, l’administrateur peut ajouter les fichiers importés à un nouveau chargement.</span><span class="sxs-lookup"><span data-stu-id="7255a-140">If you want to import new files after Batch calculation, the administrator can add the imported files to a new load.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7255a-141">Si vous cliquez sur **Annuler** pendant le calcul par lots, le processus enregistre ce qui a déjà été exécuté.</span><span class="sxs-lookup"><span data-stu-id="7255a-141">If you click **Cancel** during Batch calculation, the process saves what was already executed.</span></span> <span data-ttu-id="7255a-142">Si vous exécutez à nouveau le calcul par lots, le processus se poursuit à partir du dernier point exécuté.</span><span class="sxs-lookup"><span data-stu-id="7255a-142">If you run Batch calculation again, the process will continue from the last executed point.</span></span> 
  
### <a name="assessing-tagging-consistency"></a><span data-ttu-id="7255a-143">Évaluation de la cohérence du marquage</span><span class="sxs-lookup"><span data-stu-id="7255a-143">Assessing tagging consistency</span></span>

<span data-ttu-id="7255a-144">S’il existe des incohérences dans le marquage de fichiers, cela peut affecter l’analyse.</span><span class="sxs-lookup"><span data-stu-id="7255a-144">If there are inconsistencies in file tagging, it can affect the analysis.</span></span> <span data-ttu-id="7255a-145">Le Advanced eDiscovery de cohérence de marquage peut être utilisé lorsque les résultats ne sont pas optimaux ou que la cohérence est en doute.</span><span class="sxs-lookup"><span data-stu-id="7255a-145">The Advanced eDiscovery tagging consistency process can be used when results are not optimal or consistency is in doubt.</span></span> <span data-ttu-id="7255a-146">Une liste des fichiers marqués incohérents possibles est renvoyée, et ils peuvent être révisés et retardés, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7255a-146">A list of possible inconsistently tagged files is returned, and they can be reviewed and retagged, as necessary.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7255a-147">Après sept séries d’entraînements ou plus après  l’évaluation, la cohérence du marquage peut être vue dans la progression de formation détaillée des résultats du suivi de \>  \>  \>  \> **pertinence.**</span><span class="sxs-lookup"><span data-stu-id="7255a-147">After seven or more training rounds following assessment, tagging consistency can be viewed in **Relevance** \> **Track** \> **Issue** \> **Detailed results** \> **Training progress**.</span></span> <span data-ttu-id="7255a-148">Cette révision est effectuée pour un problème à la fois.</span><span class="sxs-lookup"><span data-stu-id="7255a-148">This review is done for one issue at a time.</span></span>
  
1. <span data-ttu-id="7255a-149">Dans **la piste de \> pertinence,** développez la ligne d’un problème.</span><span class="sxs-lookup"><span data-stu-id="7255a-149">In **Relevance \> Track**, expand an issue's row.</span></span>
  
2. <span data-ttu-id="7255a-150">À droite de **l’étape suivante,** cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="7255a-150">To the right of **Next step**, click **Modify**.</span></span>
  
3. <span data-ttu-id="7255a-151">Sélectionnez **incohérences de balise comme** option de **l’étape** suivante, après sept exemples de formation et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7255a-151">Select **Tag inconsistencies** as the **Next step** option, after seven training samples and click **OK**.</span></span>
  
4. <span data-ttu-id="7255a-152">Sélectionner **les incohérences de balise**.</span><span class="sxs-lookup"><span data-stu-id="7255a-152">Select **Tag inconsistencies**.</span></span> <span data-ttu-id="7255a-153">**L’onglet** Balise s’ouvre et affiche une liste des incohérences à retager si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7255a-153">The **Tag** tab opens displaying a list of the inconsistencies to retag as necessary.</span></span>
  
5. <span data-ttu-id="7255a-154">Cliquez **sur Calculer** pour envoyer les modifications.</span><span class="sxs-lookup"><span data-stu-id="7255a-154">Click **Calculate** to submit the changes.</span></span> <span data-ttu-id="7255a-155">L’étape suivante après le marquage des incohérences est « Formation ».</span><span class="sxs-lookup"><span data-stu-id="7255a-155">The next step after tagging inconsistencies is "Training".</span></span> 
  
## <a name="viewing-and-using-relevance-results"></a><span data-ttu-id="7255a-156">Affichage et utilisation des résultats de pertinence</span><span class="sxs-lookup"><span data-stu-id="7255a-156">Viewing and using Relevance results</span></span>

<span data-ttu-id="7255a-157">Dans **l’onglet Suivi \>** de pertinence, développez la ligne d’un problème, puis en regard des résultats détaillés, cliquez sur **Afficher.**</span><span class="sxs-lookup"><span data-stu-id="7255a-157">In the **Relevance \> Track** tab, expand an issue's row, and next to **Detailed results**, click **View**.</span></span> <span data-ttu-id="7255a-158">Les volets de résultats détaillés sont affichés, comme indiqué et décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7255a-158">The Detailed results panes are displayed, as shown and described below.</span></span>
  
![Résultats détaillés de la formation de pertinence](../media/495c04a9-ed1e-4355-8cab-c14270ca2bbb.png)
  
### <a name="tagging-summary"></a><span data-ttu-id="7255a-160">Résumé du marquage</span><span class="sxs-lookup"><span data-stu-id="7255a-160">Tagging summary</span></span>

 <span data-ttu-id="7255a-161">Dans l’exemple ci-dessous, **le** résumé de marquage affiche les totaux de chacun des processus de marquage des fichiers d’évaluation, de formation et de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="7255a-161">In the example shown below, the **Tagging summary** displays totals for each of Assessment, Training, and Catch-up file tagging processes.</span></span>
  
![Résumé du marquage du suivi de pertinence](../media/0ec906fc-bc84-4245-a964-fb3ca37891db.png)
  
### <a name="keywords"></a><span data-ttu-id="7255a-163">Mots clés</span><span class="sxs-lookup"><span data-stu-id="7255a-163">Keywords</span></span>

<span data-ttu-id="7255a-164">Un mot clé est une chaîne, un mot, une expression ou une séquence de mots uniques dans un fichier identifié par Advanced eDiscovery comme un indicateur significatif de la pertinence d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="7255a-164">A keyword is a unique string, word, phrase, or sequence of words in a file identified by Advanced eDiscovery as a significant indicator of whether a file is relevant.</span></span> <span data-ttu-id="7255a-165">Les colonnes « Inclure » répertorient les mots clés et les poids dans les fichiers marqués comme pertinents, et les colonnes « Exclure » répertorient les mots clés et les pondérations dans les fichiers marqués comme non pertinents.</span><span class="sxs-lookup"><span data-stu-id="7255a-165">The "Include" columns list keyword and weights in files tagged as Relevant, and the "Exclude" columns lists keywords and weights in files tagged as Not relevant.</span></span>
  
<span data-ttu-id="7255a-166">Advanced eDiscovery attribue des valeurs négatives ou positives de poids de mot clé.</span><span class="sxs-lookup"><span data-stu-id="7255a-166">Advanced eDiscovery assigns negative or positive keyword weight values.</span></span> <span data-ttu-id="7255a-167">Plus le poids est élevé, plus la probabilité qu’un fichier dans lequel le mot clé apparaît soit attribuée à un score de pertinence plus élevé lors du calcul par lot est élevée.</span><span class="sxs-lookup"><span data-stu-id="7255a-167">The higher the weight, the higher the likelihood that a file in which the keyword appears is assigned a higher Relevance score during Batch calculation.</span></span>
  
<span data-ttu-id="7255a-168">La Advanced eDiscovery de mots clés peut être utilisée pour compléter une liste conçue par un expert ou comme une vérification de l’insérezation indirecte à tout moment dans le processus de révision de fichier.</span><span class="sxs-lookup"><span data-stu-id="7255a-168">The Advanced eDiscovery list of keywords can be used to supplement a list built by an expert or as an indirect sanity check at any point in the file review process.</span></span>
  
### <a name="training-progress"></a><span data-ttu-id="7255a-169">Progression de la formation</span><span class="sxs-lookup"><span data-stu-id="7255a-169">Training progress</span></span>

<span data-ttu-id="7255a-170">Le **volet Progression** de l’entraînement inclut un graphique de progression de la formation et un indicateur de qualité, comme illustré dans l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7255a-170">The **Training Progress** pane includes a training progress graph and quality indicator display, as shown in the example below.</span></span>
  
![Avancement de la formation de suivi de pertinence](../media/8a5089f5-a162-4246-ae09-bc1921859860.png)
  
<span data-ttu-id="7255a-172">**Indicateur de qualité de formation**: affiche l’évaluation de la cohérence du marquage comme suit :</span><span class="sxs-lookup"><span data-stu-id="7255a-172">**Training quality indicator**: Displays the rating of the tagging consistency as follows:</span></span>
  
- <span data-ttu-id="7255a-173">**Bon**: les fichiers sont balisé de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="7255a-173">**Good**: Files are tagged consistently.</span></span> <span data-ttu-id="7255a-174">(Lumière verte affichée)</span><span class="sxs-lookup"><span data-stu-id="7255a-174">(Green light displayed)</span></span>
  
- <span data-ttu-id="7255a-175">**Moyen**: certains fichiers peuvent être marqués de manière incohérente.</span><span class="sxs-lookup"><span data-stu-id="7255a-175">**Medium**: Some files may be tagged inconsistently.</span></span> <span data-ttu-id="7255a-176">(Lumière jaune affichée)</span><span class="sxs-lookup"><span data-stu-id="7255a-176">(Yellow light displayed)</span></span>

- <span data-ttu-id="7255a-177">**Avertissement**: de nombreux fichiers peuvent être marqués de manière incohérente.</span><span class="sxs-lookup"><span data-stu-id="7255a-177">**Warning**: Many files may be tagged inconsistently.</span></span> <span data-ttu-id="7255a-178">(Lumière rouge affichée)</span><span class="sxs-lookup"><span data-stu-id="7255a-178">(Red light displayed)</span></span>

<span data-ttu-id="7255a-179">**Graphique de progression de l’entraînement**: indique le degré de stabilité de l’entraînement Pertinence après de nombreux cycles d’entraînement Pertinence par rapport à la valeur de mesure F.</span><span class="sxs-lookup"><span data-stu-id="7255a-179">**Training progress graph**: Shows the degree of Relevance training stability after many Relevance training cycles in comparison to the F-measure value.</span></span> <span data-ttu-id="7255a-180">À mesure que nous allons de gauche à droite sur le graphique, l’intervalle de confiance est réduit et utilisé, avec la mesure F, par Advanced eDiscovery Pertinence pour déterminer la stabilité lorsque les résultats de l’entraînement Pertinence sont optimisés.</span><span class="sxs-lookup"><span data-stu-id="7255a-180">As we move from the left to the right across the graph, the confidence interval narrows and is used, along with the F-measure, by Advanced eDiscovery Relevance to determine stability when the Relevance training results are optimized.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7255a-181">La pertinence utilise F2, une mesure F dans laquelle le rappel reçoit deux fois plus de poids que la précision.</span><span class="sxs-lookup"><span data-stu-id="7255a-181">Relevance uses F2, an F-measure metric where Recall receives twice as much weight as Precision.</span></span> <span data-ttu-id="7255a-182">Pour les cas avec une richesse élevée (plus de 25 %) la pertinence utilise F1 (rapport 1:1).</span><span class="sxs-lookup"><span data-stu-id="7255a-182">For cases with high richness (over 25%), Relevance uses F1 (1:1 ratio).</span></span> <span data-ttu-id="7255a-183">Le rapport de mesure F peut être configuré dans les **paramètres** avancés d’installation \> **de pertinence.**</span><span class="sxs-lookup"><span data-stu-id="7255a-183">The F-measure ratio can be configured in **Relevance setup** \> **Advanced settings**.</span></span>
  
### <a name="batch-calculation-results"></a><span data-ttu-id="7255a-184">Résultats de calcul par lot</span><span class="sxs-lookup"><span data-stu-id="7255a-184">Batch calculation results</span></span>

<span data-ttu-id="7255a-185">Le **volet Résultats du calcul batch** inclut le nombre de fichiers qui ont été marqués pour Pertinence, comme suit :</span><span class="sxs-lookup"><span data-stu-id="7255a-185">The **Batch calculation results** pane includes the number of files that were scored for Relevance, as follows:</span></span> 
  
- <span data-ttu-id="7255a-186">**Success**</span><span class="sxs-lookup"><span data-stu-id="7255a-186">**Success**</span></span>
  
- <span data-ttu-id="7255a-187">**Vide**: ne contient pas de texte, par exemple, uniquement les espaces/onglets</span><span class="sxs-lookup"><span data-stu-id="7255a-187">**Empty**: Contains no text, for example, only spaces/tabs</span></span>
  
- <span data-ttu-id="7255a-188">**Échec :** en raison d’une taille excessive ou de l’échec de lecture</span><span class="sxs-lookup"><span data-stu-id="7255a-188">**Failed**: Due to excessive size or could not be read</span></span>
  
- <span data-ttu-id="7255a-189">**Ignoré :** en raison d’une taille excessive</span><span class="sxs-lookup"><span data-stu-id="7255a-189">**Ignored**: Due to excessive size</span></span>
  
- <span data-ttu-id="7255a-190">**Nebulous**: contient du texte sans signification ou aucune fonctionnalité pertinente au problème</span><span class="sxs-lookup"><span data-stu-id="7255a-190">**Nebulous**: Contains meaningless text or no features relevant to the issue</span></span>
  
> [!NOTE]
> <span data-ttu-id="7255a-191">Empty, Failed, Ignored ou Nebulous reçoit un score de pertinence de -1.</span><span class="sxs-lookup"><span data-stu-id="7255a-191">Empty, Failed, Ignored, or Nebulous will receive a Relevance score of -1.</span></span>
  
### <a name="training-statistics"></a><span data-ttu-id="7255a-192">Statistiques de formation</span><span class="sxs-lookup"><span data-stu-id="7255a-192">Training statistics</span></span>

<span data-ttu-id="7255a-193">Le **volet Statistiques** de formation affiche des statistiques et des graphiques basés sur les résultats de Advanced eDiscovery formation Pertinence.</span><span class="sxs-lookup"><span data-stu-id="7255a-193">The **Training statistics** pane displays statistics and graphs based on results from Advanced eDiscovery Relevance training.</span></span> 
  
![Statistiques de la formation de suivi de pertinence](../media/9a07740e-20d3-49fb-b9b9-84265e0a1836.png)
  
<span data-ttu-id="7255a-195">Cet affichage présente les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="7255a-195">This view shows the following:</span></span>
  
- <span data-ttu-id="7255a-196">**Taux de révision/rappel :** comparaison des résultats en fonction des scores de pertinence dans une révision hypothétiquement linéaire.</span><span class="sxs-lookup"><span data-stu-id="7255a-196">**Review-recall ratio**: Comparison of results according to Relevance scores in a hypothetically linear review.</span></span> <span data-ttu-id="7255a-197">Le rappel est estimé en raison de la taille du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="7255a-197">Recall is estimated given the review set size set.</span></span>
  
- <span data-ttu-id="7255a-198">**Paramètres :** statistiques calculées cumulatives relatives au jeu à réviser par rapport à la population de fichiers pour l’ensemble du cas.</span><span class="sxs-lookup"><span data-stu-id="7255a-198">**Parameters**: Cumulative calculated statistics pertaining to the review set in relation to the file population for the entire case.</span></span>
  
- <span data-ttu-id="7255a-199">**Révision**: pourcentage de fichiers à réviser en fonction de ce cutoff.</span><span class="sxs-lookup"><span data-stu-id="7255a-199">**Review**: Percentage of files to review based on this cutoff.</span></span>
  
- <span data-ttu-id="7255a-200">**Rappel**: pourcentage de fichiers pertinents dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="7255a-200">**Recall**: Percentage of Relevant files in the review set.</span></span> 
  
- <span data-ttu-id="7255a-201">**Répartition par score de pertinence**: les fichiers dans l’affichage gris foncé à gauche sont inférieurs au score de seuil.</span><span class="sxs-lookup"><span data-stu-id="7255a-201">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score.</span></span> <span data-ttu-id="7255a-202">Une info-conseil affiche le score de pertinence et le pourcentage connexe de fichiers dans le jeu de fichiers de révision par rapport au nombre total de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7255a-202">A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
