---
title: Balisage et évaluation dans Advanced eDiscovery
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
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
ROBOTS: NOINDEX, NOFOLLOW
description: Examinez les étapes pour effectuer une formation à l’évaluation, notamment des fichiers de marquage, et en examinant les résultats de l’évaluation dans Advanced eDiscovery.
ms.openlocfilehash: 15bc8254ea1589d9afa17a74eaf3bfbcdfd4bba0
ms.sourcegitcommit: 5ba0015c1554048f817fdfdc85359eee1368da64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "49769189"
---
# <a name="tagging-and-assessment-in-the-relevance-module-in-advanced-ediscovery"></a><span data-ttu-id="7f388-103">Balisage et évaluation dans le module de pertinence dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7f388-103">Tagging and Assessment in the Relevance module in Advanced eDiscovery</span></span>
  
<span data-ttu-id="7f388-104">Cette section décrit la procédure d’évaluation dans le module pertinence dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7f388-104">This section describes the procedure for Assessment in the Relevance module in Advanced eDiscovery.</span></span>
  
## <a name="performing-assessment-training-and-analysis"></a><span data-ttu-id="7f388-105">Exécution de la formation et de l’analyse de l’évaluation</span><span class="sxs-lookup"><span data-stu-id="7f388-105">Performing Assessment training and analysis</span></span>

1. <span data-ttu-id="7f388-106">Sous l' **onglet \> suivi de pertinence** , cliquez sur **évaluation** pour démarrer l’évaluation de cas.</span><span class="sxs-lookup"><span data-stu-id="7f388-106">In the **Relevance \> Track** tab, click **Assessment** to start case assessment.</span></span>

    <span data-ttu-id="7f388-107">Dans le cadre de cette procédure, un exemple d’ensemble d’évaluation de 500 fichiers est créé et l’onglet **balise** s’affiche, qui contient le panneau balisage, le contenu du fichier et d’autres options de marquage.</span><span class="sxs-lookup"><span data-stu-id="7f388-107">For example purposes in this procedure, a sample assessment set of 500 files is created and the **Tag** tab is displayed, which contains the Tagging panel, displayed file content and other tagging options.</span></span> 

    ![Onglet Balise de pertinence pour l’évaluation](../media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. <span data-ttu-id="7f388-109">Examinez chaque fichier dans l’exemple, déterminez la pertinence du fichier pour chaque problème de cas, et marquez le fichier à l’aide des boutons pertinence (R), non pertinent (NR) et ignorer dans le volet de **marquage** .</span><span class="sxs-lookup"><span data-stu-id="7f388-109">Review each file in the sample, determine the file's relevance for each case issue, and tag the file using the Relevance (R), Not relevant (NR) and Skip buttons in the **Tagging panel** pane.</span></span> 

    > [!NOTE]
    >  <span data-ttu-id="7f388-110">L’évaluation requiert 500 fichiers balisés.</span><span class="sxs-lookup"><span data-stu-id="7f388-110">Assessment requires 500 tagged files.</span></span> <span data-ttu-id="7f388-111">Si les fichiers sont « ignorés », vous recevrez plus de fichiers à balise.</span><span class="sxs-lookup"><span data-stu-id="7f388-111">If files are "skipped", you will receive more files to tag.</span></span> 
  
3. <span data-ttu-id="7f388-112">Après avoir balisé tous les fichiers de l’exemple, cliquez sur **calculer**.</span><span class="sxs-lookup"><span data-stu-id="7f388-112">After tagging all files in the sample, click **Calculate**.</span></span>

    <span data-ttu-id="7f388-113">La marge d’erreur et la richesse de l’évaluation actuelle sont calculées et affichées sous l’onglet de **suivi de pertinence** , avec des détails détaillés par problème, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7f388-113">The Assessment current error margin and richness are calculated and displayed in the **Relevance Track** tab, with expanded details per issue, as shown below.</span></span> <span data-ttu-id="7f388-114">Pour plus d’informations sur cette boîte de dialogue, voir la section [examen des résultats](#reviewing-assessment-results) de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="7f388-114">More details about this dialog are described in the [Reviewing assessment results](#reviewing-assessment-results) section.</span></span>

    ![Suivi de pertinence - Évaluation](../media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > <span data-ttu-id="7f388-116">Par défaut, nous vous recommandons de passer à l’étape suivante par défaut lorsque l’indicateur de progression de l’évaluation du problème est terminé, indiquant que l’exemple d’évaluation a été révisé et que des fichiers appropriés ont été marqués.</span><span class="sxs-lookup"><span data-stu-id="7f388-116">By default, we recommend that you proceed to the default Next step when the Assessment progress indicator for the issue has completed, indicating that the assessment sample was reviewed and sufficient relevant files were tagged.</span></span> <span data-ttu-id="7f388-117">> sinon, si vous souhaitez afficher les résultats de l’onglet de **suivi** et contrôler la marge d’erreur et l’étape suivante, cliquez sur **modifier** en regard de l' **étape suivante**, sélectionnez **continuer l’évaluation**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f388-117">> Otherwise, if you want to view the **Track** tab results and control the margin of error and the next step, click **Modify** adjacent to **Next Step**, select **Continue assessment**, and then click **OK**.</span></span>
  
4. <span data-ttu-id="7f388-118">Cliquez sur **modifier** à droite de la case à cocher **évaluation** pour afficher et spécifier les paramètres d’évaluation par problème.</span><span class="sxs-lookup"><span data-stu-id="7f388-118">Click **Modify** to the right of the **Assessment** check box to view and specify assessment parameters per issue.</span></span> <span data-ttu-id="7f388-119">Une boîte de dialogue de **niveau d’évaluation** s’affiche pour chaque problème, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7f388-119">An **Assessment level** dialog for each issue is displayed, as shown in the following example:</span></span> 

    ![Problème de cas de niveau d’évaluation](../media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    <span data-ttu-id="7f388-121">Les paramètres suivants du problème sont calculés et affichés dans la boîte de dialogue **niveau d’évaluation** :</span><span class="sxs-lookup"><span data-stu-id="7f388-121">The following parameters for the issue are calculated and displayed in the **Assessment level** dialog:</span></span> 

    <span data-ttu-id="7f388-122">**Marge d’erreur cible pour les estimations de rappel**: en fonction de cette valeur, le nombre estimé de fichiers supplémentaires nécessaires à la révision est calculé.</span><span class="sxs-lookup"><span data-stu-id="7f388-122">**Target error margin for recall estimates**: Based on this value, the estimated number of additional files necessary to review is calculated.</span></span> <span data-ttu-id="7f388-123">La marge utilisée pour le rappel est supérieure à 75% et avec un niveau de confiance de 95%.</span><span class="sxs-lookup"><span data-stu-id="7f388-123">The margin used for recall is greater than 75% and with a 95% confidence level.</span></span>

    <span data-ttu-id="7f388-124">**Fichiers d’évaluation supplémentaires requis**: indique le nombre de fichiers nécessaires si les exigences actuelles de marge d’erreur n’ont pas été respectées.</span><span class="sxs-lookup"><span data-stu-id="7f388-124">**Additional assessment files required**: Indicates how many more files are necessary if the current error margin's requirements have not been met.</span></span> 

5. <span data-ttu-id="7f388-125">Pour ajuster la marge d’erreur actuelle et observer l’effet de différentes marges d’erreur (par problème) :</span><span class="sxs-lookup"><span data-stu-id="7f388-125">To adjust the current error margin and see the effect of different error margins (per issue):</span></span>

6. <span data-ttu-id="7f388-126">Dans la liste **Sélectionner un problème** , sélectionnez un problème.</span><span class="sxs-lookup"><span data-stu-id="7f388-126">In the **Select issue** list, select an issue.</span></span> 

7. <span data-ttu-id="7f388-127">Dans **marge d’erreur cible pour les estimations de rappel**, entrez une nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="7f388-127">In **Target error margin for recall estimates**, enter a new value.</span></span>

8. <span data-ttu-id="7f388-128">Cliquez sur **mettre à jour les valeurs** pour voir l’impact des ajustements.</span><span class="sxs-lookup"><span data-stu-id="7f388-128">Click **Update values** to see the impact of the adjustments.</span></span> 

9. <span data-ttu-id="7f388-129">Cliquez sur **avancé** dans la boîte de dialogue **niveau d’évaluation** pour voir les paramètres et détails supplémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="7f388-129">Click **Advanced** in the **Assessment level** dialog to see the following additional parameters and details:</span></span> 

    ![Vue avancée de problème de cas de niveau d’évaluation](../media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    - <span data-ttu-id="7f388-131">**Richesse estimée**: richesse estimée en fonction des résultats de l’évaluation actuelle</span><span class="sxs-lookup"><span data-stu-id="7f388-131">**Estimated richness**: Estimated richness according to the current assessment results</span></span>

    - <span data-ttu-id="7f388-132">**Pour le rappel présumé**: par défaut, la marge d’erreur cible s’applique au rappel supérieur à 75%.</span><span class="sxs-lookup"><span data-stu-id="7f388-132">**For assumed recall**: By default, the target error margin applies to recall above 75%.</span></span> <span data-ttu-id="7f388-133">Cliquez sur **modifier** si vous souhaitez modifier ce paramètre et contrôler la marge d’erreur sur une plage de valeurs de rappel différente.</span><span class="sxs-lookup"><span data-stu-id="7f388-133">Click **Edit** if you want to change this parameter and control the margin of error on a different range of recall values.</span></span> 

    - <span data-ttu-id="7f388-134">**Niveau de confiance**: par défaut, la marge d’erreur recommandée pour la confiance est de 95%.</span><span class="sxs-lookup"><span data-stu-id="7f388-134">**Confidence level**: By default, the recommended error margin for confidence is 95%.</span></span> <span data-ttu-id="7f388-135">Cliquez sur **modifier** si vous souhaitez modifier ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="7f388-135">Click **Edit** if you want to change this parameter.</span></span>

    - <span data-ttu-id="7f388-136">**Marge d’erreur de richesse attendue**: en fonction des valeurs mises à jour, il s’agit de la marge d’erreur attendue de la richesse, après examen de tous les fichiers d’évaluation supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7f388-136">**Expected richness error margin**: Given the updated values, this is the expected margin of error of the richness, after all additional assessment files are reviewed.</span></span>

    - <span data-ttu-id="7f388-137">**Fichiers d’évaluation supplémentaires requis**: étant donné les valeurs mises à jour, le nombre de fichiers d’évaluation supplémentaires qui doivent être vérifiés pour atteindre la cible.</span><span class="sxs-lookup"><span data-stu-id="7f388-137">**Additional assessment files required**: Given the updated values, the number of additional assessment files that need to be reviewed to reach the target.</span></span>

    - <span data-ttu-id="7f388-138">**Nombre total de fichiers d’évaluation requis**: étant donné les valeurs mises à jour, le nombre total de fichiers d’évaluation requis pour la révision.</span><span class="sxs-lookup"><span data-stu-id="7f388-138">**Total assessment files required**: Given the updated values, total assessment files required for review.</span></span>

    - <span data-ttu-id="7f388-139">**Nombre prévu de fichiers pertinents lors de l’évaluation**: étant donné les valeurs mises à jour, le nombre prévu de fichiers pertinents dans l’intégralité de l’évaluation une fois que tous les fichiers d’évaluation supplémentaires sont examinés.</span><span class="sxs-lookup"><span data-stu-id="7f388-139">**Expected number of relevant files in assessment**: Given the updated values, the expected number of relevant files in the entire assessment after all additional assessment files are reviewed.</span></span>

10. <span data-ttu-id="7f388-140">Cliquez sur **recalculer les valeurs** si les paramètres sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="7f388-140">Click **Recalculate values**, if parameters are changed.</span></span> <span data-ttu-id="7f388-141">Lorsque vous avez terminé, cliquez sur **OK** pour enregistrer les modifications (ou **suivant** lorsqu’il y a plusieurs problèmes à consulter ou modifier, puis **Terminer**).</span><span class="sxs-lookup"><span data-stu-id="7f388-141">When you're done, if there is one issue, click **OK** to save the changes (or **Next** when there are multiple issues to review or modify and then **Finish**).</span></span> 

    <span data-ttu-id="7f388-142">Lorsqu’il existe plusieurs problèmes, une fois que tous les problèmes ont été vérifiés ou ajustés, un **niveau d’évaluation : Résumé** s’affiche, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="7f388-142">When there are multiple issues, after all issues have been reviewed or adjusted, an **Assessment level: summary** dialog is displayed, as shown in the following example.</span></span> 

    ![Résumé de niveau d’évaluation](../media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    <span data-ttu-id="7f388-144">Une fois l’évaluation terminée, passez à l’étape suivante de la formation pertinente.</span><span class="sxs-lookup"><span data-stu-id="7f388-144">On successful completion of assessment, proceed to the next stage in Relevance training.</span></span>

## <a name="reviewing-assessment-results"></a><span data-ttu-id="7f388-145">Examen des résultats de l’évaluation</span><span class="sxs-lookup"><span data-stu-id="7f388-145">Reviewing assessment results</span></span>

<span data-ttu-id="7f388-146">Une fois qu’un exemple d’évaluation est balisé, les résultats de l’évaluation sont calculés et affichés sous l’onglet suivi de pertinence.</span><span class="sxs-lookup"><span data-stu-id="7f388-146">After an Assessment sample is tagged, the assessment results are calculated and displayed in the Relevance Track tab.</span></span>
  
<span data-ttu-id="7f388-147">Les résultats suivants s’affichent dans l’affichage de suivi étendu :</span><span class="sxs-lookup"><span data-stu-id="7f388-147">The following results are displayed in the expanded Track display:</span></span>
  
- <span data-ttu-id="7f388-148">Évaluation de la marge d’erreur actuelle pour les estimations de rappel</span><span class="sxs-lookup"><span data-stu-id="7f388-148">Assessment current error margin for recall estimates</span></span>

- <span data-ttu-id="7f388-149">Richesse estimée</span><span class="sxs-lookup"><span data-stu-id="7f388-149">Estimated richness</span></span>

- <span data-ttu-id="7f388-150">Fichiers d’évaluation supplémentaires requis (pour révision)</span><span class="sxs-lookup"><span data-stu-id="7f388-150">Additional assessment files required (for review)</span></span>

<span data-ttu-id="7f388-151">L’évaluation de la marge d’erreur actuelle est la marge d’erreur recommandée par Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7f388-151">The Assessment current error margin is the error margin recommended by Advanced eDiscovery.</span></span> <span data-ttu-id="7f388-152">Le numéro affiché pour le « fichiers d’évaluation supplémentaires requis » correspond à cette recommandation.</span><span class="sxs-lookup"><span data-stu-id="7f388-152">The number displayed for the "Additional assessment files required" corresponds to that recommendation.</span></span>
  
<span data-ttu-id="7f388-153">L’indicateur de progression de l’évaluation indique le niveau d’exécution de l’évaluation, en fonction de la marge d’erreur actuelle.</span><span class="sxs-lookup"><span data-stu-id="7f388-153">The Assessment progress indicator shows the level of completion of the assessment, given the current error margin.</span></span> <span data-ttu-id="7f388-154">Lorsque l’évaluation est en cours, l’utilisateur balise un autre exemple d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="7f388-154">When assessment is underway, the user will tag another assessment sample.</span></span>
  
<span data-ttu-id="7f388-155">Lorsque l’indicateur de progression de l’évaluation indique l’évaluation terminée, cela signifie que la révision de l’exemple d’évaluation a été effectuée et que des fichiers appropriés ont été marqués.</span><span class="sxs-lookup"><span data-stu-id="7f388-155">When the assessment progress indicator shows assessment as complete, that means the assessment sample review was completed and sufficient relevant files were tagged.</span></span> 
  
<span data-ttu-id="7f388-156">L’affichage de suivi étendu présente l’étape suivante recommandée, les statistiques d’évaluation et l’accès aux résultats détaillés.</span><span class="sxs-lookup"><span data-stu-id="7f388-156">The expanded Track display shows the recommended next step, the assessment statistics, and access to detailed results.</span></span>
  
<span data-ttu-id="7f388-157">Lorsque la richesse est très faible, le nombre de fichiers d’évaluation supplémentaires nécessaires pour atteindre un nombre minimal de fichiers pertinents pour produire des statistiques utiles est très élevé.</span><span class="sxs-lookup"><span data-stu-id="7f388-157">When richness is very low, the number of additional assessment files needed to reach a minimal number of relevant files to produce useful statistics is very high.</span></span> <span data-ttu-id="7f388-158">Advanced eDiscovery vous recommande de passer à la formation.</span><span class="sxs-lookup"><span data-stu-id="7f388-158">Advanced eDiscovery will then recommend moving on to training.</span></span> <span data-ttu-id="7f388-159">L’indicateur de progression de l’évaluation est ombré et aucune statistique n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="7f388-159">The assessment progress indicator will be shaded, and no statistics will be available.</span></span>
  
<span data-ttu-id="7f388-160">En l’absence de stabilisation statistiquement basée statistiquement, les résultats seront moins élevés.</span><span class="sxs-lookup"><span data-stu-id="7f388-160">In the absence of statistically based stabilization, there will be results with a lower level of accuracy and confidence level.</span></span> <span data-ttu-id="7f388-161">Toutefois, ces résultats peuvent être utilisés pour rechercher des fichiers pertinents lorsque vous n’avez pas besoin de connaître le pourcentage de fichiers pertinents trouvés.</span><span class="sxs-lookup"><span data-stu-id="7f388-161">However, these results can be used to find relevant files when you do not need to know the percentage of relevant files found.</span></span> <span data-ttu-id="7f388-162">De même, cet État peut être utilisé pour former des problèmes avec une faible richesse, où les scores de pertinence peuvent accélérer l’accès aux fichiers pertinents à un problème spécifique.</span><span class="sxs-lookup"><span data-stu-id="7f388-162">Similarly, this status can be used to train issues with low richness, where Relevance scores can accelerate access to files relevant to a specific issue.</span></span>
  
> [!TIP]
> <span data-ttu-id="7f388-163">Dans l' **onglet \> suivi de pertinence** , affichage des problèmes étendus, les options d’affichage suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="7f388-163">In the **Relevance \> Track** tab, expanded issue display, the following viewing options are available:</span></span> 
> 
> <span data-ttu-id="7f388-164">L’étape suivante recommandée, telle que l' **étape suivante** , peut être contournée (par problème) en cliquant sur le bouton **modifier** à sa droite, puis en sélectionnant une autre étape dans l' **étape suivante**.</span><span class="sxs-lookup"><span data-stu-id="7f388-164">The recommended next step, such as **Next step: Tagging** can be bypassed (per issue) by clicking the **Modify** button to its right, and then selecting an different step in the **Next step**.</span></span> <span data-ttu-id="7f388-165">Lorsque l’indicateur de progression de l’évaluation n’est pas terminé, l’option évaluation est recommandée suivant, pour baliser les fichiers d’évaluation et augmenter la précision des statistiques.</span><span class="sxs-lookup"><span data-stu-id="7f388-165">When the assessment progress indicator has not completed, assessment will be the next recommended option, to tag more assessment files and increase statistics accuracy.</span></span> 
> 
> <span data-ttu-id="7f388-166">Vous pouvez modifier la marge d’erreur et évaluer son impact en cliquant sur **modifier**, puis dans la **boîte de dialogue niveau d’évaluation**, en modifiant la **marge d’erreur cible pour les estimations de rappel**, puis en cliquant sur **mettre à jour les valeurs**.</span><span class="sxs-lookup"><span data-stu-id="7f388-166">You can change the error margin and assess its impact, by clicking **Modify**, and in the **Assessment level dialog**, changing the **Target error margin for recall estimates**, and clicking **Update values**.</span></span> <span data-ttu-id="7f388-167">De plus, dans cette boîte de dialogue, vous pouvez afficher les options avancées en cliquant sur **avancé**.</span><span class="sxs-lookup"><span data-stu-id="7f388-167">Also, in this dialog, you can view advanced options, by clicking **Advanced**.</span></span> 
> 
> <span data-ttu-id="7f388-168">Vous pouvez afficher des statistiques de niveau d’évaluation supplémentaires et leur impact en cliquant sur **affichage**.</span><span class="sxs-lookup"><span data-stu-id="7f388-168">You can view additional assessment level statistics and their impact by clicking **View**.</span></span> <span data-ttu-id="7f388-169">Dans la boîte de dialogue résultats détaillés affichés, les statistiques sont disponibles par problème, lorsqu’il y a au moins 500 fichiers d’évaluation marqués et que 18 fichiers sont balisés comme pertinents pour le problème.</span><span class="sxs-lookup"><span data-stu-id="7f388-169">In the displayed Detail results dialog, statistics are available per issue, when there are at least 500 tagged assessment files and at least 18 files are tagged as Relevant for the issue.</span></span> 
