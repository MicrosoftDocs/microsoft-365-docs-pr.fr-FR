---
title: Suivi de l’analyse de pertinence dans Office 365 Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
titleSuffix: Office 365
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 3ab1e2c3-28cf-4bf5-b0a8-c0222f32bdf5
description: 'Découvrez comment afficher et interpréter la pertinence état de formation et résultats pour les problèmes de cas dans Office 365 Advanced eDiscovery.  '
ms.openlocfilehash: 5fa9fe49f1a644f2a64321c1ec106b11c487c885
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41601401"
---
# <a name="track-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="119c2-103">Suivi de l’analyse de pertinence dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="119c2-103">Track Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="119c2-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="119c2-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="119c2-106">Dans Advanced eDiscovery, l’onglet suivi de pertinence affiche la validité calculée de la formation à la pertinence effectuée dans l’onglet balise et indique l’étape suivante à effectuer dans le processus de formation itérative en matière de pertinence.</span><span class="sxs-lookup"><span data-stu-id="119c2-106">In Advanced eDiscovery, the Relevance Track tab displays the calculated validity of the Relevance training performed in the Tag tab and indicates the next step to take in the iterative training process in Relevance.</span></span> 
  
## <a name="tracking-relevance-training-status"></a><span data-ttu-id="119c2-107">Suivi de l’état de formation à la pertinence</span><span class="sxs-lookup"><span data-stu-id="119c2-107">Tracking Relevance training status</span></span>

1. <span data-ttu-id="119c2-108">Consultez les détails suivants dans le suivi de pertinence pour les problèmes de cas, comme indiqué dans l’exemple suivant d’une boîte de dialogue **nom du problème** ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="119c2-108">View the following details in Relevance Track for the case issues, as shown in the following example of an **Issue name** dialog below.</span></span> 
    
  - <span data-ttu-id="119c2-109">**Évaluation**: cet indicateur de progression indique dans quelle mesure la formation pertinente effectuée à ce stade a atteint la cible de l’évaluation en termes de marge d’erreur.</span><span class="sxs-lookup"><span data-stu-id="119c2-109">**Assessment**: This progress indicator shows to what degree the Relevance training performed to this point has achieved the assessment target in terms of margin of error.</span></span> <span data-ttu-id="119c2-110">La richesse des résultats d’apprentissage de pertinence est également affichée.</span><span class="sxs-lookup"><span data-stu-id="119c2-110">The richness of the Relevance training results is also displayed.</span></span> 
    
  - <span data-ttu-id="119c2-111">**Formation**: cet indicateur de progression codé en couleur et l’affichage de l’info-bulle indiquent la pertinence des résultats de formation pertinents et une balance numérique illustrant le nombre d’exemples d’apprentissage de pertinence marqués pour chaque problème.</span><span class="sxs-lookup"><span data-stu-id="119c2-111">**Training**: This color-coded progress indicator and tool-tip display indicates the Relevance training results stability and a numeric scale showing the number of Relevance training samples tagged for each issue.</span></span> <span data-ttu-id="119c2-112">L’expert surveille la progression du processus de formation à la pertinence itératif.</span><span class="sxs-lookup"><span data-stu-id="119c2-112">The expert monitors the progress of the iterative Relevance training process.</span></span> 
    
  - <span data-ttu-id="119c2-113">**Calcul par lot**: cet indicateur de progression fournit des informations sur la fin du calcul du lot.</span><span class="sxs-lookup"><span data-stu-id="119c2-113">**Batch calculation**: This progress indicator provides information about the completion of Batch calculation.</span></span>
    
  - <span data-ttu-id="119c2-114">**Étape suivante**: affiche la recommandation pour l’étape suivante à effectuer.</span><span class="sxs-lookup"><span data-stu-id="119c2-114">**Next step**: Displays the recommendation for the next step to be performed.</span></span> 
    
    <span data-ttu-id="119c2-115">Dans l’exemple, une évaluation réussie pour un problème est illustrée par l’indicateur de progression des couleurs terminées et la coche.</span><span class="sxs-lookup"><span data-stu-id="119c2-115">In the example, a successfully completed Assessment for an issue is shown, indicated by the completed color progress indicator and the checkmark.</span></span> <span data-ttu-id="119c2-116">Le marquage est en cours, mais le cas est toujours considéré comme instable (l’état de stabilité apparaît également dans une info-bulle).</span><span class="sxs-lookup"><span data-stu-id="119c2-116">Tagging is underway, but the case is still considered unstable (stability status also shown in a tool-tip).</span></span> <span data-ttu-id="119c2-117">La recommandation suivante est la « formation ».</span><span class="sxs-lookup"><span data-stu-id="119c2-117">The next step recommendation is "Training".</span></span> 
    
    ![Formation de suivi de pertinence étape 1](media/a00fe607-680a-48eb-9d61-4565319f7ab6.png)
  
    <span data-ttu-id="119c2-119">L’affichage développé affiche des informations et des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="119c2-119">The expanded view displays additional information and options.</span></span> <span data-ttu-id="119c2-120">La marge d’erreur actuelle affichée est la marge d’erreur du rappel dans l’état actuel de l’évaluation, étant donné les fichiers d’évaluation existants (déjà balisés).</span><span class="sxs-lookup"><span data-stu-id="119c2-120">The displayed current error margin is the error margin of the recall in the current state of assessment, given the existing (already tagged) assessment files.</span></span>
    
    > [!NOTE]
    >  <span data-ttu-id="119c2-121">La phase d’évaluation peut être ignorée en désactivant la case à cocher **évaluation** par problème, puis pour « tous les problèmes ».</span><span class="sxs-lookup"><span data-stu-id="119c2-121">The Assessment stage can be bypassed by clearing the **Assessment** check box per issue and then for "all issues".</span></span> <span data-ttu-id="119c2-122">Toutefois, il n’y aura pas de statistiques pour ce problème.</span><span class="sxs-lookup"><span data-stu-id="119c2-122">However, as a result, there will be no statistics for this issue.</span></span> <span data-ttu-id="119c2-123">> la désactivation de la case à cocher **évaluation** ne peut être effectuée qu’avant l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="119c2-123">> Clearing the **Assessment** check box can only be done before assessment is performed.</span></span> <span data-ttu-id="119c2-124">Dans le cas où plusieurs problèmes existent, l’évaluation est ignorée uniquement si la case à cocher est désactivée pour chaque problème.</span><span class="sxs-lookup"><span data-stu-id="119c2-124">Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
    <span data-ttu-id="119c2-125">Lorsque l’évaluation n’est pas effectuée avec le premier ensemble de fichiers, l’évaluation peut être la prochaine étape de marquage de fichiers supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="119c2-125">When assessment is not completed with the first sample set of files, assessment might be the next step for tagging more files.</span></span> 
    
    <span data-ttu-id="119c2-126">Dans le **suivi**de **pertinence** \> , l’indicateur de progression de formation et le Conseil d’outils indiquent le nombre estimé d’échantillons supplémentaires nécessaires pour atteindre la stabilité.</span><span class="sxs-lookup"><span data-stu-id="119c2-126">In **Relevance** \> **Track**, the training progress indicator and tool-tip indicate the estimated number of additional samples needed to reach stability.</span></span> <span data-ttu-id="119c2-127">Cette estimation fournit une indication pour la formation supplémentaire requise.</span><span class="sxs-lookup"><span data-stu-id="119c2-127">This estimate provides a guideline for the additional training needed.</span></span>
    
    ![Formation de suivi de pertinence](media/98dbc3f5-5238-4d73-9f88-1aa4d77ea729.png)
  
2. <span data-ttu-id="119c2-129">Lorsque vous avez fini d’étiqueter et si vous devez poursuivre la formation, cliquez sur **formation**.</span><span class="sxs-lookup"><span data-stu-id="119c2-129">When you're done tagging and if you need to continue training, click **Training**.</span></span> <span data-ttu-id="119c2-130">Un autre exemple de jeu de fichiers est généré à partir du jeu de fichiers chargé pour une formation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="119c2-130">Another sample set of files is generated from the loaded file set for additional training.</span></span> <span data-ttu-id="119c2-131">Vous revenez ensuite à l’onglet balise pour marquer et former davantage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="119c2-131">You are then returned to the Tag tab to tag and train more files.</span></span>
    
### <a name="reaching-stable-training-levels"></a><span data-ttu-id="119c2-132">Atteindre des niveaux de formation stables</span><span class="sxs-lookup"><span data-stu-id="119c2-132">Reaching stable training levels</span></span>

<span data-ttu-id="119c2-133">Une fois que les fichiers d’évaluation ont atteint un niveau de formation stable, Advanced eDiscovery est prêt pour le calcul par lot.</span><span class="sxs-lookup"><span data-stu-id="119c2-133">After the assessment files have attained a stable level of training, Advanced eDiscovery is ready for Batch calculation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="119c2-134">En règle générale, après trois exemples de formation stables, l’étape suivante est « calcul par lot ».</span><span class="sxs-lookup"><span data-stu-id="119c2-134">Usually, after three stable training samples, the next step is "Batch calculation".</span></span> <span data-ttu-id="119c2-135">Il peut y avoir des exceptions, par exemple, lorsque des modifications ont été apportées au balisage des fichiers provenant d’exemples précédents ou lors de l’ajout de fichiers Seed.</span><span class="sxs-lookup"><span data-stu-id="119c2-135">There may be exceptions, for example, when there were changes to the tagging of files from earlier samples or when seed files were added.</span></span> 
  
### <a name="performing-batch-calculation"></a><span data-ttu-id="119c2-136">Exécution du calcul par lot</span><span class="sxs-lookup"><span data-stu-id="119c2-136">Performing Batch calculation</span></span>

<span data-ttu-id="119c2-137">Le calcul du lot est exécuté en tant que prochaine étape une fois la formation terminée (lorsqu’un état de formation stable est affiché dans la barre de progression, un état de coche et de stabilité dans le Conseil d’outils). Le calcul par lot applique les connaissances acquises lors de la formation à la pertinence à l’ensemble du remplissage du fichier, afin d’évaluer la pertinence des fichiers et d’affecter des scores de pertinence.</span><span class="sxs-lookup"><span data-stu-id="119c2-137">Batch calculation is executed as the next step after training is successfully completed (when a stable training status is shown by the progress bar, a checkmark and stable status in the tool-tip.) Batch calculation applies the knowledge acquired during the Relevance training to the entire file population, to assess the files' relevance and to assign Relevance scores.</span></span>
  
<span data-ttu-id="119c2-138">Lorsqu’il y a plusieurs problèmes, le calcul du lot est effectué par problème.</span><span class="sxs-lookup"><span data-stu-id="119c2-138">When there is more than one issue, Batch calculation is done per issue.</span></span> <span data-ttu-id="119c2-139">Pendant le calcul du lot, la progression est surveillée lors du traitement de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="119c2-139">During Batch calculation, progress is monitored while processing all of the files.</span></span> 
  
<span data-ttu-id="119c2-140">Ici, l’étape suivante recommandée est « None », ce qui indique qu’aucune formation de pertinence itérative supplémentaire n’est requise à ce stade.</span><span class="sxs-lookup"><span data-stu-id="119c2-140">Here, the recommended next step is "None", which indicates that no additional iterative Relevance training is required at this point.</span></span> <span data-ttu-id="119c2-141">La phase suivante est l' **onglet \> décider** de la pertinence.</span><span class="sxs-lookup"><span data-stu-id="119c2-141">The next phase is the **Relevance \> Decide** tab.</span></span> 
  
<span data-ttu-id="119c2-142">Si vous souhaitez importer de nouveaux fichiers après le calcul par lot, l’administrateur peut ajouter les fichiers importés à une nouvelle charge.</span><span class="sxs-lookup"><span data-stu-id="119c2-142">If you want to import new files after Batch calculation, the administrator can add the imported files to a new load.</span></span>
  
> [!NOTE]
> <span data-ttu-id="119c2-143">Si vous cliquez sur **Annuler** pendant le calcul du lot, le processus enregistre ce qui a déjà été exécuté.</span><span class="sxs-lookup"><span data-stu-id="119c2-143">If you click **Cancel** during Batch calculation, the process saves what was already executed.</span></span> <span data-ttu-id="119c2-144">Si vous réexécutez le calcul du lot, le processus se poursuit depuis le dernier point exécuté.</span><span class="sxs-lookup"><span data-stu-id="119c2-144">If you run Batch calculation again, the process will continue from the last executed point.</span></span> 
  
### <a name="assessing-tagging-consistency"></a><span data-ttu-id="119c2-145">Évaluation de la cohérence des marquages</span><span class="sxs-lookup"><span data-stu-id="119c2-145">Assessing tagging consistency</span></span>

<span data-ttu-id="119c2-146">S’il existe des incohérences dans le balisage de fichier, cela peut avoir une incidence sur l’analyse.</span><span class="sxs-lookup"><span data-stu-id="119c2-146">If there are inconsistencies in file tagging, it can affect the analysis.</span></span> <span data-ttu-id="119c2-147">Le processus avancé de cohérence des balises eDiscovery peut être utilisé lorsque les résultats ne sont pas optimaux ou si la cohérence est incertaine.</span><span class="sxs-lookup"><span data-stu-id="119c2-147">The Advanced eDiscovery tagging consistency process can be used when results are not optimal or consistency is in doubt.</span></span> <span data-ttu-id="119c2-148">Une liste de fichiers susceptibles d’être balisés de manière incohérente est renvoyée et peuvent être révisées et ré-balisage, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="119c2-148">A list of possible inconsistently tagged files is returned, and they can be reviewed and re-tagged, as necessary.</span></span>
  
> [!NOTE]
> <span data-ttu-id="119c2-149">Après **l’évaluation** \> de sept ou plusieurs arrondis de formation, la cohérence du marquage peut être affichée \*\*\*\* \> dans la **formation**sur **le suivi** \> des \> **résultats détaillés** .</span><span class="sxs-lookup"><span data-stu-id="119c2-149">After seven or more training rounds following assessment, tagging consistency can be viewed in **Relevance** \> **Track** \> **Issue** \> **Detailed results** \> **Training progress**.</span></span> <span data-ttu-id="119c2-150">Cette révision est réalisée pour un problème à la fois.</span><span class="sxs-lookup"><span data-stu-id="119c2-150">This review is done for one issue at a time.</span></span> 
  
1. <span data-ttu-id="119c2-151">Dans **le \> suivi de pertinence**, développez la ligne d’un problème.</span><span class="sxs-lookup"><span data-stu-id="119c2-151">In **Relevance \> Track**, expand an issue's row.</span></span>
    
2. <span data-ttu-id="119c2-152">À droite de l' **étape suivante**, cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="119c2-152">To the right of **Next step**, click **Modify**.</span></span>
    
3. <span data-ttu-id="119c2-153">Sélectionnez **incohérences de balise** comme **étape suivante** , après sept exemples de formation, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="119c2-153">Select **Tag inconsistencies** as the **Next step** option, after seven training samples and click **OK**.</span></span>
    
4. <span data-ttu-id="119c2-154">Sélectionnez **incohérences de balise**.</span><span class="sxs-lookup"><span data-stu-id="119c2-154">Select **Tag inconsistencies**.</span></span> <span data-ttu-id="119c2-155">L’onglet **balise** s’ouvre et affiche la liste des incohérences à réactiver.</span><span class="sxs-lookup"><span data-stu-id="119c2-155">The **Tag** tab opens displaying a list of the inconsistencies to re-tag as necessary.</span></span> 
    
5. <span data-ttu-id="119c2-156">Cliquez sur **calculer** pour envoyer les modifications.</span><span class="sxs-lookup"><span data-stu-id="119c2-156">Click **Calculate** to submit the changes.</span></span> <span data-ttu-id="119c2-157">L’étape suivante, après le marquage des incohérences, est « formation ».</span><span class="sxs-lookup"><span data-stu-id="119c2-157">The next step after tagging inconsistencies is "Training".</span></span> 
    
## <a name="viewing-and-using-relevance-results"></a><span data-ttu-id="119c2-158">Affichage et utilisation des résultats de pertinence</span><span class="sxs-lookup"><span data-stu-id="119c2-158">Viewing and using Relevance results</span></span>

<span data-ttu-id="119c2-159">Dans l' **onglet \> suivi de pertinence** , développez la ligne d’un problème, puis en regard de **résultats détaillés**, cliquez sur **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="119c2-159">In the **Relevance \> Track** tab, expand an issue's row, and next to **Detailed results**, click **View**.</span></span> <span data-ttu-id="119c2-160">Les volets de résultats détaillés sont affichés, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="119c2-160">The Detailed results panes are displayed, as shown and described below.</span></span>
  
![Résultats détaillés de la formation de pertinence](media/495c04a9-ed1e-4355-8cab-c14270ca2bbb.png)
  
### <a name="tagging-summary"></a><span data-ttu-id="119c2-162">Synthèse des marquages</span><span class="sxs-lookup"><span data-stu-id="119c2-162">Tagging summary</span></span>

 <span data-ttu-id="119c2-163">Dans l’exemple ci-dessous, le **Résumé de marquage** affiche les totaux pour chaque processus d’évaluation, de formation et de marquage de fichier de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="119c2-163">In the example shown below, the **Tagging summary** displays totals for each of Assessment, Training, and Catch-up file tagging processes.</span></span> 
  
![Résumé du marquage du suivi de pertinence](media/0ec906fc-bc84-4245-a964-fb3ca37891db.png)
  
### <a name="keywords"></a><span data-ttu-id="119c2-165">Mots clés</span><span class="sxs-lookup"><span data-stu-id="119c2-165">Keywords</span></span>

<span data-ttu-id="119c2-166">Un mot clé est une chaîne, un mot, une phrase ou une séquence de mots unique identifiée par Advanced eDiscovery comme un indicateur significatif de la pertinence d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="119c2-166">A keyword is a unique string, word, phrase, or sequence of words in a file identified by Advanced eDiscovery as a significant indicator of whether a file is relevant.</span></span> <span data-ttu-id="119c2-167">Le mot clé de liste de colonnes « include » et les pondérations dans les fichiers marqués comme pertinents et les colonnes « Exclude » répertorient les mots clés et les pondérations dans les fichiers marqués comme non pertinents.</span><span class="sxs-lookup"><span data-stu-id="119c2-167">The "Include" columns list keyword and weights in files tagged as Relevant, and the "Exclude" columns lists keywords and weights in files tagged as Not relevant.</span></span>
  
<span data-ttu-id="119c2-168">Advanced eDiscovery affecte des valeurs de pondération de mots clés négatives ou positives.</span><span class="sxs-lookup"><span data-stu-id="119c2-168">Advanced eDiscovery assigns negative or positive keyword weight values.</span></span> <span data-ttu-id="119c2-169">Plus le poids est élevé, plus le score de pertinence d’un fichier dans lequel apparaît le mot clé est élevé pendant le calcul du lot.</span><span class="sxs-lookup"><span data-stu-id="119c2-169">The higher the weight, the higher the likelihood that a file in which the keyword appears is assigned a higher Relevance score during Batch calculation.</span></span> 
  
<span data-ttu-id="119c2-170">La liste de mots-clés eDiscovery avancée peut être utilisée pour compléter une liste créée par un expert ou comme un contrôle de validité indirect à tout moment du processus de révision de fichier.</span><span class="sxs-lookup"><span data-stu-id="119c2-170">The Advanced eDiscovery list of keywords can be used to supplement a list built by an expert or as an indirect sanity check at any point in the file review process.</span></span>
  
### <a name="training-progress"></a><span data-ttu-id="119c2-171">Progression de la formation</span><span class="sxs-lookup"><span data-stu-id="119c2-171">Training progress</span></span>

<span data-ttu-id="119c2-172">Le volet progression de la **formation** inclut un graphique de progression de formation et un affichage d’indicateur de qualité, comme illustré dans l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="119c2-172">The **Training Progress** pane includes a training progress graph and quality indicator display, as shown in the example below.</span></span> 
  
![Avancement de la formation de suivi de pertinence](media/8a5089f5-a162-4246-ae09-bc1921859860.png)
  
 <span data-ttu-id="119c2-174">**Indicateur de qualité de formation**: affiche l’évaluation de la cohérence des balises comme suit :</span><span class="sxs-lookup"><span data-stu-id="119c2-174">**Training quality indicator**: Displays the rating of the tagging consistency as follows:</span></span>
  
- <span data-ttu-id="119c2-175">**Approprié**: les fichiers sont balisés de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="119c2-175">**Good**: Files are tagged consistently.</span></span> <span data-ttu-id="119c2-176">(Voyant vert affiché)</span><span class="sxs-lookup"><span data-stu-id="119c2-176">(Green light displayed)</span></span>
    
- <span data-ttu-id="119c2-177">**Moyen**: certains fichiers peuvent être balisés de manière incohérente.</span><span class="sxs-lookup"><span data-stu-id="119c2-177">**Medium**: Some files may be tagged inconsistently.</span></span> <span data-ttu-id="119c2-178">(Jaune clair affiché)</span><span class="sxs-lookup"><span data-stu-id="119c2-178">(Yellow light displayed)</span></span>
    
- <span data-ttu-id="119c2-179">**Avertissement**: de nombreux fichiers peuvent être balisés de manière incohérente.</span><span class="sxs-lookup"><span data-stu-id="119c2-179">**Warning**: Many files may be tagged inconsistently.</span></span> <span data-ttu-id="119c2-180">(Lumière rouge affichée)</span><span class="sxs-lookup"><span data-stu-id="119c2-180">(Red light displayed)</span></span>
    
 <span data-ttu-id="119c2-181">**Graphique de progression de formation**: indique le degré de stabilité de la formation à la pertinence après un certain nombre de cycles de formation pertinents par rapport à la valeur de la mesure F.</span><span class="sxs-lookup"><span data-stu-id="119c2-181">**Training progress graph**: Shows the degree of Relevance training stability after a number of Relevance training cycles in comparison to the F-measure value.</span></span> <span data-ttu-id="119c2-182">À mesure que nous passons de la gauche vers la droite sur le graphique, l’intervalle de confiance réduit et est utilisé, ainsi que la mesure F, par rapport à l’intérêt eDiscovery avancé afin de déterminer la stabilité lorsque les résultats d’apprentissage pertinents sont optimisés.</span><span class="sxs-lookup"><span data-stu-id="119c2-182">As we move from the left to the right across the graph, the confidence interval narrows and is used, along with the F-measure, by Advanced eDiscovery Relevance to determine stability when the Relevance training results are optimized.</span></span>
  
> [!NOTE]
> <span data-ttu-id="119c2-183">La pertinence utilise F2, une mesure F-Measure où le rappel reçoit deux fois plus de poids que la précision.</span><span class="sxs-lookup"><span data-stu-id="119c2-183">Relevance uses F2, an F-measure metric where Recall receives twice as much weight as Precision.</span></span> <span data-ttu-id="119c2-184">Pour les cas de grande richesse (plus de 25%), la pertinence utilise F1 (ratio 1:1).</span><span class="sxs-lookup"><span data-stu-id="119c2-184">For cases with high richness (over 25%), Relevance uses F1 (1:1 ratio).</span></span> <span data-ttu-id="119c2-185">Le rapport de mesure F peut être configuré dans \*\*\*\* \> **Paramètres avancés**de configuration de pertinence.</span><span class="sxs-lookup"><span data-stu-id="119c2-185">The F-measure ratio can be configured in **Relevance setup** \> **Advanced settings**.</span></span> 
  
### <a name="batch-calculation-results"></a><span data-ttu-id="119c2-186">Résultats du calcul par lots</span><span class="sxs-lookup"><span data-stu-id="119c2-186">Batch calculation results</span></span>

<span data-ttu-id="119c2-187">Le volet **résultats du calcul par lots** inclut le nombre de fichiers dont la pertinence a été évaluée, comme suit :</span><span class="sxs-lookup"><span data-stu-id="119c2-187">The **Batch calculation results** pane includes the number of files that were scored for Relevance, as follows:</span></span> 
  
- <span data-ttu-id="119c2-188">**Success**</span><span class="sxs-lookup"><span data-stu-id="119c2-188">**Success**</span></span>
    
- <span data-ttu-id="119c2-189">**Empty**: ne contient pas de texte, par exemple, uniquement des espaces/tabulations</span><span class="sxs-lookup"><span data-stu-id="119c2-189">**Empty**: Contains no text, for example, only spaces/tabs</span></span>
    
- <span data-ttu-id="119c2-190">**Échec**: en raison d’une taille excessive ou n’a pas pu être lu</span><span class="sxs-lookup"><span data-stu-id="119c2-190">**Failed**: Due to excessive size or could not be read</span></span>
    
- <span data-ttu-id="119c2-191">**Ignoré**: en raison d’une taille excessive</span><span class="sxs-lookup"><span data-stu-id="119c2-191">**Ignored**: Due to excessive size</span></span>
    
- <span data-ttu-id="119c2-192">**Nebulous**: contient un texte inutile ou aucune fonctionnalité pertinente pour le problème</span><span class="sxs-lookup"><span data-stu-id="119c2-192">**Nebulous**: Contains meaningless text or no features relevant to the issue</span></span>
    
> [!NOTE]
> <span data-ttu-id="119c2-193">Empty, failed, ignored ou nebulous recevront un score de pertinence de-1.</span><span class="sxs-lookup"><span data-stu-id="119c2-193">Empty, Failed, Ignored, or Nebulous will receive a Relevance score of -1.</span></span> 
  
### <a name="training-statistics"></a><span data-ttu-id="119c2-194">Statistiques de formation</span><span class="sxs-lookup"><span data-stu-id="119c2-194">Training statistics</span></span>

<span data-ttu-id="119c2-195">Le volet **statistiques de formation** affiche les statistiques et les graphiques basés sur les résultats de la formation avancée eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="119c2-195">The **Training statistics** pane displays statistics and graphs based on results from Advanced eDiscovery Relevance training.</span></span> 
  
![Statistiques de la formation de suivi de pertinence](media/9a07740e-20d3-49fb-b9b9-84265e0a1836.png)
  
<span data-ttu-id="119c2-197">Cet affichage montre les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="119c2-197">This view shows the following:</span></span>
  
- <span data-ttu-id="119c2-198">**Review-ratio de rappel**: comparaison des résultats selon les scores de pertinence dans une révision hypothétique.</span><span class="sxs-lookup"><span data-stu-id="119c2-198">**Review-recall ratio**: Comparison of results according to Relevance scores in a hypothetically linear review.</span></span> <span data-ttu-id="119c2-199">Le rappel est estimé en fonction de la définition de la taille de l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="119c2-199">Recall is estimated given the review set size set.</span></span>
    
- <span data-ttu-id="119c2-200">**Paramètres**: statistiques calculées cumulatives relatives au jeu de révision en relation avec le remplissage du fichier pour l’ensemble du cas.</span><span class="sxs-lookup"><span data-stu-id="119c2-200">**Parameters**: Cumulative calculated statistics pertaining to the review set in relation to the file population for the entire case.</span></span>
    
- <span data-ttu-id="119c2-201">**Révision**: pourcentage de fichiers à vérifier en fonction de ce seuil de troncature.</span><span class="sxs-lookup"><span data-stu-id="119c2-201">**Review**: Percentage of files to review based on this cutoff.</span></span>
    
- <span data-ttu-id="119c2-202">**Rappel**: pourcentage de fichiers pertinents dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="119c2-202">**Recall**: Percentage of Relevant files in the review set.</span></span> 
    
- <span data-ttu-id="119c2-203">**Répartition par score de pertinence**: les fichiers dans l’affichage gris foncé vers la gauche sont en dessous du score de coupure.</span><span class="sxs-lookup"><span data-stu-id="119c2-203">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score.</span></span> <span data-ttu-id="119c2-204">Une info-bulle affiche le score de pertinence et le pourcentage de fichiers correspondant dans le jeu de fichiers de révision en relation avec le nombre total de fichiers.</span><span class="sxs-lookup"><span data-stu-id="119c2-204">A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="119c2-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="119c2-205">See also</span></span>

[<span data-ttu-id="119c2-206">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="119c2-206">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="119c2-207">Présentation de l’évaluation en matière de pertinence</span><span class="sxs-lookup"><span data-stu-id="119c2-207">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="119c2-208">Exécution et examen de l’évaluation</span><span class="sxs-lookup"><span data-stu-id="119c2-208">Performing and reviewing Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="119c2-209">Formation à la pertinence</span><span class="sxs-lookup"><span data-stu-id="119c2-209">Performing Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="119c2-210">Prise de décisions en fonction des résultats</span><span class="sxs-lookup"><span data-stu-id="119c2-210">Making decisions based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="119c2-211">Évaluation de l’analyse de pertinence</span><span class="sxs-lookup"><span data-stu-id="119c2-211">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

