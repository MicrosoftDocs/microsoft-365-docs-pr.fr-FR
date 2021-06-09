---
title: Marquage et évaluation dans Advanced eDiscovery
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
description: Examinez les étapes à suivre pour effectuer une formation sur l’évaluation, y compris le marquage des fichiers et l’examen des résultats de l’Advanced eDiscovery.
ms.openlocfilehash: 15bc8254ea1589d9afa17a74eaf3bfbcdfd4bba0
ms.sourcegitcommit: 5ba0015c1554048f817fdfdc85359eee1368da64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "49769189"
---
# <a name="tagging-and-assessment-in-the-relevance-module-in-advanced-ediscovery"></a><span data-ttu-id="d443c-103">Marquage et évaluation dans le module de pertinence dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d443c-103">Tagging and Assessment in the Relevance module in Advanced eDiscovery</span></span>
  
<span data-ttu-id="d443c-104">Cette section décrit la procédure d’évaluation dans le module Pertinence dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d443c-104">This section describes the procedure for Assessment in the Relevance module in Advanced eDiscovery.</span></span>
  
## <a name="performing-assessment-training-and-analysis"></a><span data-ttu-id="d443c-105">Formation et analyse de l’évaluation</span><span class="sxs-lookup"><span data-stu-id="d443c-105">Performing Assessment training and analysis</span></span>

1. <span data-ttu-id="d443c-106">Dans **l’onglet Suivi de \> pertinence,** cliquez **sur Évaluation** pour démarrer l’évaluation des cas.</span><span class="sxs-lookup"><span data-stu-id="d443c-106">In the **Relevance \> Track** tab, click **Assessment** to start case assessment.</span></span>

    <span data-ttu-id="d443c-107">Par exemple, dans le cadre de cette procédure, un exemple  d’ensemble d’évaluation de 500 fichiers est créé et l’onglet Balise s’affiche, qui contient le panneau marquage, le contenu du fichier affiché et d’autres options de marquage.</span><span class="sxs-lookup"><span data-stu-id="d443c-107">For example purposes in this procedure, a sample assessment set of 500 files is created and the **Tag** tab is displayed, which contains the Tagging panel, displayed file content and other tagging options.</span></span> 

    ![Onglet Balise de pertinence pour l’évaluation](../media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. <span data-ttu-id="d443c-109">Passez en revue chaque fichier de l’exemple, déterminez la pertinence du fichier pour chaque problème de cas et  marquez le fichier à l’aide des boutons Pertinence (R), Non pertinent (NR) et Ignorer dans le volet Marquage.</span><span class="sxs-lookup"><span data-stu-id="d443c-109">Review each file in the sample, determine the file's relevance for each case issue, and tag the file using the Relevance (R), Not relevant (NR) and Skip buttons in the **Tagging panel** pane.</span></span> 

    > [!NOTE]
    >  <span data-ttu-id="d443c-110">L’évaluation nécessite 500 fichiers balisé.</span><span class="sxs-lookup"><span data-stu-id="d443c-110">Assessment requires 500 tagged files.</span></span> <span data-ttu-id="d443c-111">Si les fichiers sont « ignorés », vous recevrez d’autres fichiers à baliser.</span><span class="sxs-lookup"><span data-stu-id="d443c-111">If files are "skipped", you will receive more files to tag.</span></span> 
  
3. <span data-ttu-id="d443c-112">Après avoir balisé tous les fichiers de l’exemple, cliquez sur **Calculer.**</span><span class="sxs-lookup"><span data-stu-id="d443c-112">After tagging all files in the sample, click **Calculate**.</span></span>

    <span data-ttu-id="d443c-113">La marge d’erreur et la richesse  actuelles de l’évaluation sont calculées et affichées dans l’onglet Suivi de pertinence, avec des détails développés par problème, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d443c-113">The Assessment current error margin and richness are calculated and displayed in the **Relevance Track** tab, with expanded details per issue, as shown below.</span></span> <span data-ttu-id="d443c-114">Plus d’informations sur cette boîte de dialogue sont décrites dans la section Révision des résultats [de l’évaluation.](#reviewing-assessment-results)</span><span class="sxs-lookup"><span data-stu-id="d443c-114">More details about this dialog are described in the [Reviewing assessment results](#reviewing-assessment-results) section.</span></span>

    ![Suivi de pertinence - Évaluation](../media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > <span data-ttu-id="d443c-116">Par défaut, nous vous recommandons de passer à l’étape suivante par défaut une fois l’indicateur de progression de l’évaluation du problème terminé, indiquant que l’exemple d’évaluation a été examiné et que des fichiers pertinents suffisants ont été balisé.</span><span class="sxs-lookup"><span data-stu-id="d443c-116">By default, we recommend that you proceed to the default Next step when the Assessment progress indicator for the issue has completed, indicating that the assessment sample was reviewed and sufficient relevant files were tagged.</span></span> <span data-ttu-id="d443c-117">> Dans le cas contraire, si  vous souhaitez afficher les résultats de l’onglet Suivi et contrôler la marge d’erreur et l’étape suivante, cliquez sur Modifier en regard de l’étape **suivante,** sélectionnez Continuer l’évaluation, puis cliquez sur **OK.**  </span><span class="sxs-lookup"><span data-stu-id="d443c-117">> Otherwise, if you want to view the **Track** tab results and control the margin of error and the next step, click **Modify** adjacent to **Next Step**, select **Continue assessment**, and then click **OK**.</span></span>
  
4. <span data-ttu-id="d443c-118">Cliquez **sur Modifier** à  droite de la case à cocher Évaluation pour afficher et spécifier les paramètres d’évaluation par problème.</span><span class="sxs-lookup"><span data-stu-id="d443c-118">Click **Modify** to the right of the **Assessment** check box to view and specify assessment parameters per issue.</span></span> <span data-ttu-id="d443c-119">Une **boîte de dialogue de** niveau d’évaluation pour chaque problème s’affiche, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="d443c-119">An **Assessment level** dialog for each issue is displayed, as shown in the following example:</span></span> 

    ![Problème de cas de niveau d’évaluation](../media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    <span data-ttu-id="d443c-121">Les paramètres suivants du problème sont calculés et affichés dans la boîte de dialogue **Niveau d’évaluation** :</span><span class="sxs-lookup"><span data-stu-id="d443c-121">The following parameters for the issue are calculated and displayed in the **Assessment level** dialog:</span></span> 

    <span data-ttu-id="d443c-122">**Marge d’erreur cible pour** les estimations de rappel : en fonction de cette valeur, le nombre estimé de fichiers supplémentaires à réviser est calculé.</span><span class="sxs-lookup"><span data-stu-id="d443c-122">**Target error margin for recall estimates**: Based on this value, the estimated number of additional files necessary to review is calculated.</span></span> <span data-ttu-id="d443c-123">La marge utilisée pour le rappel est supérieure à 75 % et avec un niveau de confiance de 95 %.</span><span class="sxs-lookup"><span data-stu-id="d443c-123">The margin used for recall is greater than 75% and with a 95% confidence level.</span></span>

    <span data-ttu-id="d443c-124">**Fichiers d’évaluation supplémentaires** requis : indique combien de fichiers supplémentaires sont nécessaires si les exigences de la marge d’erreur actuelle n’ont pas été satisfaites.</span><span class="sxs-lookup"><span data-stu-id="d443c-124">**Additional assessment files required**: Indicates how many more files are necessary if the current error margin's requirements have not been met.</span></span> 

5. <span data-ttu-id="d443c-125">Pour ajuster la marge d’erreur actuelle et voir l’effet de différentes marges d’erreur (par problème) :</span><span class="sxs-lookup"><span data-stu-id="d443c-125">To adjust the current error margin and see the effect of different error margins (per issue):</span></span>

6. <span data-ttu-id="d443c-126">Dans la **liste Sélectionner un problème,** sélectionnez un problème.</span><span class="sxs-lookup"><span data-stu-id="d443c-126">In the **Select issue** list, select an issue.</span></span> 

7. <span data-ttu-id="d443c-127">Dans **marge d’erreur cible pour les estimations de rappel,** entrez une nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="d443c-127">In **Target error margin for recall estimates**, enter a new value.</span></span>

8. <span data-ttu-id="d443c-128">Cliquez **sur Mettre à jour** les valeurs pour voir l’impact des ajustements.</span><span class="sxs-lookup"><span data-stu-id="d443c-128">Click **Update values** to see the impact of the adjustments.</span></span> 

9. <span data-ttu-id="d443c-129">Cliquez **sur Avancé** dans la boîte de dialogue **Niveau** d’évaluation pour voir les paramètres et détails supplémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="d443c-129">Click **Advanced** in the **Assessment level** dialog to see the following additional parameters and details:</span></span> 

    ![Vue avancée de problème de cas de niveau d’évaluation](../media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    - <span data-ttu-id="d443c-131">**Richesse estimée :** richesse estimée en fonction des résultats d’évaluation actuels</span><span class="sxs-lookup"><span data-stu-id="d443c-131">**Estimated richness**: Estimated richness according to the current assessment results</span></span>

    - <span data-ttu-id="d443c-132">**Pour le rappel supposé :** par défaut, la marge d’erreur cible s’applique au rappel supérieur à 75 %.</span><span class="sxs-lookup"><span data-stu-id="d443c-132">**For assumed recall**: By default, the target error margin applies to recall above 75%.</span></span> <span data-ttu-id="d443c-133">Cliquez **sur Modifier** si vous souhaitez modifier ce paramètre et contrôler la marge d’erreur sur une plage différente de valeurs de rappel.</span><span class="sxs-lookup"><span data-stu-id="d443c-133">Click **Edit** if you want to change this parameter and control the margin of error on a different range of recall values.</span></span> 

    - <span data-ttu-id="d443c-134">**Niveau de confiance**: par défaut, la marge d’erreur recommandée pour la confiance est de 95 %.</span><span class="sxs-lookup"><span data-stu-id="d443c-134">**Confidence level**: By default, the recommended error margin for confidence is 95%.</span></span> <span data-ttu-id="d443c-135">Cliquez **sur Modifier** si vous souhaitez modifier ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="d443c-135">Click **Edit** if you want to change this parameter.</span></span>

    - <span data-ttu-id="d443c-136">**Marge d’erreur** de richesse attendue : étant donné les valeurs mises à jour, il s’agit de la marge d’erreur attendue de la richesse, une fois tous les fichiers d’évaluation supplémentaires examinés.</span><span class="sxs-lookup"><span data-stu-id="d443c-136">**Expected richness error margin**: Given the updated values, this is the expected margin of error of the richness, after all additional assessment files are reviewed.</span></span>

    - <span data-ttu-id="d443c-137">**Fichiers d’évaluation supplémentaires** requis : étant donné les valeurs mises à jour, le nombre de fichiers d’évaluation supplémentaires qui doivent être examinés pour atteindre la cible.</span><span class="sxs-lookup"><span data-stu-id="d443c-137">**Additional assessment files required**: Given the updated values, the number of additional assessment files that need to be reviewed to reach the target.</span></span>

    - <span data-ttu-id="d443c-138">**Nombre total de fichiers d’évaluation requis**: étant donné les valeurs mises à jour, le nombre total de fichiers d’évaluation requis pour la révision.</span><span class="sxs-lookup"><span data-stu-id="d443c-138">**Total assessment files required**: Given the updated values, total assessment files required for review.</span></span>

    - <span data-ttu-id="d443c-139">**Nombre attendu de fichiers pertinents** dans l’évaluation : étant donné les valeurs mises à jour, le nombre attendu de fichiers pertinents dans l’ensemble de l’évaluation une fois tous les fichiers d’évaluation supplémentaires examinés.</span><span class="sxs-lookup"><span data-stu-id="d443c-139">**Expected number of relevant files in assessment**: Given the updated values, the expected number of relevant files in the entire assessment after all additional assessment files are reviewed.</span></span>

10. <span data-ttu-id="d443c-140">Cliquez **sur Recalculer les valeurs,** si les paramètres sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="d443c-140">Click **Recalculate values**, if parameters are changed.</span></span> <span data-ttu-id="d443c-141">Lorsque vous avez terminé, s’il existe un problème,  cliquez sur **OK** pour enregistrer les modifications (ou suivant lorsqu’il existe plusieurs problèmes à réviser ou modifier, puis **à terminer).**</span><span class="sxs-lookup"><span data-stu-id="d443c-141">When you're done, if there is one issue, click **OK** to save the changes (or **Next** when there are multiple issues to review or modify and then **Finish**).</span></span> 

    <span data-ttu-id="d443c-142">Lorsqu’il existe plusieurs problèmes, une fois tous les  problèmes examinés ou ajustés, un niveau d’évaluation : boîte de dialogue récapitulatif s’affiche, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="d443c-142">When there are multiple issues, after all issues have been reviewed or adjusted, an **Assessment level: summary** dialog is displayed, as shown in the following example.</span></span> 

    ![Résumé de niveau d’évaluation](../media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    <span data-ttu-id="d443c-144">Une fois l’évaluation terminée, passer à l’étape suivante de l’entraînement Pertinence.</span><span class="sxs-lookup"><span data-stu-id="d443c-144">On successful completion of assessment, proceed to the next stage in Relevance training.</span></span>

## <a name="reviewing-assessment-results"></a><span data-ttu-id="d443c-145">Examen des résultats de l’évaluation</span><span class="sxs-lookup"><span data-stu-id="d443c-145">Reviewing assessment results</span></span>

<span data-ttu-id="d443c-146">Une fois qu’un exemple d’évaluation est balisé, les résultats de l’évaluation sont calculés et affichés dans l’onglet Suivi de pertinence.</span><span class="sxs-lookup"><span data-stu-id="d443c-146">After an Assessment sample is tagged, the assessment results are calculated and displayed in the Relevance Track tab.</span></span>
  
<span data-ttu-id="d443c-147">Les résultats suivants sont affichés dans l’affichage Piste étendue :</span><span class="sxs-lookup"><span data-stu-id="d443c-147">The following results are displayed in the expanded Track display:</span></span>
  
- <span data-ttu-id="d443c-148">Marge d’erreur actuelle d’évaluation pour les estimations de rappel</span><span class="sxs-lookup"><span data-stu-id="d443c-148">Assessment current error margin for recall estimates</span></span>

- <span data-ttu-id="d443c-149">Richesse estimée</span><span class="sxs-lookup"><span data-stu-id="d443c-149">Estimated richness</span></span>

- <span data-ttu-id="d443c-150">Fichiers d’évaluation supplémentaires requis (pour révision)</span><span class="sxs-lookup"><span data-stu-id="d443c-150">Additional assessment files required (for review)</span></span>

<span data-ttu-id="d443c-151">La marge d’erreur actuelle de l’évaluation est la marge d’erreur recommandée par Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d443c-151">The Assessment current error margin is the error margin recommended by Advanced eDiscovery.</span></span> <span data-ttu-id="d443c-152">Le nombre affiché pour les « fichiers d’évaluation supplémentaires requis » correspond à cette recommandation.</span><span class="sxs-lookup"><span data-stu-id="d443c-152">The number displayed for the "Additional assessment files required" corresponds to that recommendation.</span></span>
  
<span data-ttu-id="d443c-153">L’indicateur de progression de l’évaluation indique le niveau d’achèvement de l’évaluation, compte tenu de la marge d’erreur actuelle.</span><span class="sxs-lookup"><span data-stu-id="d443c-153">The Assessment progress indicator shows the level of completion of the assessment, given the current error margin.</span></span> <span data-ttu-id="d443c-154">Lorsque l’évaluation est en cours, l’utilisateur marque un autre exemple d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="d443c-154">When assessment is underway, the user will tag another assessment sample.</span></span>
  
<span data-ttu-id="d443c-155">Lorsque l’indicateur de progression de l’évaluation indique que l’évaluation est terminée, cela signifie que l’examen de l’exemple d’évaluation a été terminé et que des fichiers pertinents suffisants ont été marqués.</span><span class="sxs-lookup"><span data-stu-id="d443c-155">When the assessment progress indicator shows assessment as complete, that means the assessment sample review was completed and sufficient relevant files were tagged.</span></span> 
  
<span data-ttu-id="d443c-156">L’affichage suivi développé montre l’étape suivante recommandée, les statistiques d’évaluation et l’accès aux résultats détaillés.</span><span class="sxs-lookup"><span data-stu-id="d443c-156">The expanded Track display shows the recommended next step, the assessment statistics, and access to detailed results.</span></span>
  
<span data-ttu-id="d443c-157">Lorsque la richesse est très faible, le nombre de fichiers d’évaluation supplémentaires nécessaires pour atteindre un nombre minimal de fichiers pertinents afin de produire des statistiques utiles est très élevé.</span><span class="sxs-lookup"><span data-stu-id="d443c-157">When richness is very low, the number of additional assessment files needed to reach a minimal number of relevant files to produce useful statistics is very high.</span></span> <span data-ttu-id="d443c-158">Advanced eDiscovery vous recommanderez ensuite de passer à la formation.</span><span class="sxs-lookup"><span data-stu-id="d443c-158">Advanced eDiscovery will then recommend moving on to training.</span></span> <span data-ttu-id="d443c-159">L’indicateur de progression de l’évaluation sera ombbré et aucune statistiques ne sera disponible.</span><span class="sxs-lookup"><span data-stu-id="d443c-159">The assessment progress indicator will be shaded, and no statistics will be available.</span></span>
  
<span data-ttu-id="d443c-160">En l’absence de stabilisation basée sur les statistiques, des résultats seront obtenus avec un niveau de précision et de confiance inférieurs.</span><span class="sxs-lookup"><span data-stu-id="d443c-160">In the absence of statistically based stabilization, there will be results with a lower level of accuracy and confidence level.</span></span> <span data-ttu-id="d443c-161">Toutefois, ces résultats peuvent être utilisés pour rechercher des fichiers pertinents lorsque vous n’avez pas besoin de connaître le pourcentage de fichiers pertinents trouvés.</span><span class="sxs-lookup"><span data-stu-id="d443c-161">However, these results can be used to find relevant files when you do not need to know the percentage of relevant files found.</span></span> <span data-ttu-id="d443c-162">De même, cet état peut être utilisé pour entraîner des problèmes de faible richesse, où les scores de pertinence peuvent accélérer l’accès aux fichiers pertinents pour un problème spécifique.</span><span class="sxs-lookup"><span data-stu-id="d443c-162">Similarly, this status can be used to train issues with low richness, where Relevance scores can accelerate access to files relevant to a specific issue.</span></span>
  
> [!TIP]
> <span data-ttu-id="d443c-163">Dans **l’onglet Suivi de \> pertinence,** affichage des problèmes développé, les options d’affichage suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="d443c-163">In the **Relevance \> Track** tab, expanded issue display, the following viewing options are available:</span></span> 
> 
> <span data-ttu-id="d443c-164">L’étape suivante recommandée,  telle que l’étape suivante : le balisage peut être contourné (par problème) en cliquant sur le bouton Modifier à droite, puis en sélectionnant une autre étape à l’étape **suivante.** </span><span class="sxs-lookup"><span data-stu-id="d443c-164">The recommended next step, such as **Next step: Tagging** can be bypassed (per issue) by clicking the **Modify** button to its right, and then selecting an different step in the **Next step**.</span></span> <span data-ttu-id="d443c-165">Lorsque l’indicateur de progression de l’évaluation n’est pas terminé, l’évaluation est la prochaine option recommandée, pour baliser d’autres fichiers d’évaluation et améliorer la précision des statistiques.</span><span class="sxs-lookup"><span data-stu-id="d443c-165">When the assessment progress indicator has not completed, assessment will be the next recommended option, to tag more assessment files and increase statistics accuracy.</span></span> 
> 
> <span data-ttu-id="d443c-166">Vous pouvez modifier la marge d’erreur et évaluer son impact en cliquant sur Modifier **et** dans la boîte de dialogue Niveau d’évaluation, en modifiant la marge d’erreur cible pour les estimations de rappel et en cliquant sur Mettre à jour les **valeurs.**</span><span class="sxs-lookup"><span data-stu-id="d443c-166">You can change the error margin and assess its impact, by clicking **Modify**, and in the **Assessment level dialog**, changing the **Target error margin for recall estimates**, and clicking **Update values**.</span></span> <span data-ttu-id="d443c-167">En outre, dans cette boîte de dialogue, vous pouvez afficher les options avancées en cliquant sur **Avancé.**</span><span class="sxs-lookup"><span data-stu-id="d443c-167">Also, in this dialog, you can view advanced options, by clicking **Advanced**.</span></span> 
> 
> <span data-ttu-id="d443c-168">Vous pouvez afficher des statistiques supplémentaires sur le niveau d’évaluation et leur impact en cliquant sur **Afficher.**</span><span class="sxs-lookup"><span data-stu-id="d443c-168">You can view additional assessment level statistics and their impact by clicking **View**.</span></span> <span data-ttu-id="d443c-169">Dans la boîte de dialogue De résultats détaillés affichée, des statistiques sont disponibles par problème, lorsqu’il y a au moins 500 fichiers d’évaluation balisé et qu’au moins 18 fichiers sont marqués comme pertinents pour le problème.</span><span class="sxs-lookup"><span data-stu-id="d443c-169">In the displayed Detail results dialog, statistics are available per issue, when there are at least 500 tagged assessment files and at least 18 files are tagged as Relevant for the issue.</span></span> 
