---
title: Utiliser le module de pertinence dans Office 365 Advanced eDiscovery
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
ms.assetid: 5d671821-d188-42da-a9ce-9cfe92beedfd
description: 'Découvrez le module de pertinence dans Office 365 Advanced eDiscovery, notamment un flux de travail et des instructions, ainsi que les étapes de formation et de révision de fichiers.  '
ms.openlocfilehash: 5151c94d2b0bd1824abb499f6cb27bbfbc7618b7
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41601301"
---
# <a name="use-the-relevance-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="d702b-103">Utiliser le module de pertinence dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d702b-103">Use the Relevance module in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="d702b-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="d702b-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="d702b-106">Dans Advanced eDiscovery, le module de pertinence inclut la formation pertinente et la révision des fichiers associés à un cas.</span><span class="sxs-lookup"><span data-stu-id="d702b-106">In Advanced eDiscovery, the Relevance module includes the Relevance training and review of files related to a case.</span></span> <span data-ttu-id="d702b-107">Le flux de travail de pertinence est illustré et décrit comme suit :</span><span class="sxs-lookup"><span data-stu-id="d702b-107">The Relevance workflow is shown and described as follows:</span></span>
  
![Flux de travail de pertinence](media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="d702b-109">**Cycles d’évaluation et de suivi**:</span><span class="sxs-lookup"><span data-stu-id="d702b-109">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="d702b-110">**Évaluation**: Advanced eDiscovery permet une évaluation précoce basée sur un échantillon aléatoire de fichiers et utilise cette évaluation pour déterminer les performances du processus de codage prédictif.</span><span class="sxs-lookup"><span data-stu-id="d702b-110">**Assessment**: Advanced eDiscovery enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="d702b-111">**Track**: Advanced eDiscovery calcule et affiche les résultats intermédiaires de l’évaluation tout en surveillant la validité statistique du processus.</span><span class="sxs-lookup"><span data-stu-id="d702b-111">**Track**: Advanced eDiscovery calculates and displays interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="d702b-112">**Cycles de formation et de suivi**:</span><span class="sxs-lookup"><span data-stu-id="d702b-112">**Cycles of training and tracking**:</span></span>
    
  - <span data-ttu-id="d702b-113">**Tag**: Advanced eDiscovery apprend des critères de pertinence spécifiques à chaque problème en fonction de la révision itérative et du marquage des fichiers individuels de l’expert.</span><span class="sxs-lookup"><span data-stu-id="d702b-113">**Tag**: Advanced eDiscovery learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="d702b-114">**Track**: Advanced eDiscovery calcule et affiche les résultats intermédiaires de la formation à la pertinence tout en surveillant la validité statistique du processus.</span><span class="sxs-lookup"><span data-stu-id="d702b-114">**Track**: Advanced eDiscovery calculates and displays interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="d702b-115">**Calcul par lot**: Advanced eDiscovery prend les critères de pertinence accumulés et appris, l’applique à l’ensemble de la collection de fichiers et génère des scores de pertinence pour chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="d702b-115">**Batch calculation**: Advanced eDiscovery takes the accumulated and learned Relevance criteria, applies it to the entire file collection, and generates Relevance scores for each file.</span></span>
    
- <span data-ttu-id="d702b-116">**Décider**: Advanced eDiscovery affiche les résultats de l’analyse appliquée à l’ensemble de l’incident après le calcul par lot et affiche les données pour les décisions de révision de document.</span><span class="sxs-lookup"><span data-stu-id="d702b-116">**Decide**: Advanced eDiscovery displays the results of the analysis applied to the entire case after Batch calculation and displays data for making document review decisions.</span></span>
    
- <span data-ttu-id="d702b-117">**Test**: les résultats avancés de découverte électronique peuvent être testés pour vérifier la validité et l’efficacité du traitement eDiscovery avancé.</span><span class="sxs-lookup"><span data-stu-id="d702b-117">**Test**: Advanced eDiscovery results can be tested to verify the validity and effectiveness of the Advanced eDiscovery processing.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="d702b-118">Instructions pour la formation et la révision de pertinence</span><span class="sxs-lookup"><span data-stu-id="d702b-118">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="d702b-119">Vous trouverez ci-dessous une vue d’ensemble des directives de formation et de révision :</span><span class="sxs-lookup"><span data-stu-id="d702b-119">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="d702b-120">**Erreurs et incohérences**: si des erreurs de marquage sont effectuées pendant l’apprentissage, revenez aux exemples de fichiers précédents pour les corriger.</span><span class="sxs-lookup"><span data-stu-id="d702b-120">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them.</span></span> <span data-ttu-id="d702b-121">S’il y a trop d’erreurs à corriger ou qu’il existe une nouvelle perspective ou un problème, les critères de pertinence doivent être redéfinis par l’administrateur et l’apprentissage de pertinence doit être redémarré.</span><span class="sxs-lookup"><span data-stu-id="d702b-121">If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="d702b-122">**Balisage et formation**:</span><span class="sxs-lookup"><span data-stu-id="d702b-122">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="d702b-123">Les fichiers doivent être balisés en fonction du contenu uniquement.</span><span class="sxs-lookup"><span data-stu-id="d702b-123">Files should be tagged based on content only.</span></span> <span data-ttu-id="d702b-124">Ne considérez pas les métadonnées, telles que le dépositaire, la date ou le chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="d702b-124">Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="d702b-125">Ne pas tenir compte des indications de plage de dates dans le texte lors du marquage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d702b-125">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="d702b-126">Ne considérez pas les images graphiques incorporées lors du balisage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d702b-126">Do not consider embedded graphical images when tagging files.</span></span>
    
  - <span data-ttu-id="d702b-127">Si vous affichez un fichier à l’aide de l’icône d' **affichage de texte mis en forme** pendant le marquage, ne tenez pas compte de la mise en forme du texte.</span><span class="sxs-lookup"><span data-stu-id="d702b-127">If viewing a file using the **formatted text view** icon while tagging, do not consider the formatting of text.</span></span> <span data-ttu-id="d702b-128">Par exemple, un mot affiché avec un barré (une ligne horizontale à travers son centre indiquant la suppression) est toujours considéré par pertinence dans le cadre du texte analysé.</span><span class="sxs-lookup"><span data-stu-id="d702b-128">For example, a word displayed with a strikethrough (a horizontal line through its center indicating deletion) is still considered by Relevance as part of the analyzed text.</span></span> 
    
  - <span data-ttu-id="d702b-129">Ignorer le texte appliqué à la pertinence (tel que défini par le gestionnaire de cas ou l’administrateur) sera supprimé du contenu du fichier affiché dans l’affichage de texte en pertinence.</span><span class="sxs-lookup"><span data-stu-id="d702b-129">Ignore text applied to Relevance (as set by the Case Manager or Administrator) will be removed in the displayed file content in the text view in Relevance.</span></span> <span data-ttu-id="d702b-130">Si les valeurs pour ignorer le texte ont été définies après l’apprentissage de pertinence déjà démarré, le nouveau texte ignoré est appliqué aux fichiers d’exemple créés à partir du point dans lequel ils ont été définis.</span><span class="sxs-lookup"><span data-stu-id="d702b-130">If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined.</span></span> <span data-ttu-id="d702b-131">La fonctionnalité ignorer le texte doit être utilisée avec précaution, car son utilisation peut réduire les performances de l’analyse des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d702b-131">The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="d702b-132">Utilisez l’option **ignorer le balisage** uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d702b-132">Use the **Skip tagging** option only when necessary.</span></span> <span data-ttu-id="d702b-133">Advanced eDiscovery n’effectue pas de formation basée sur des fichiers ignorés.</span><span class="sxs-lookup"><span data-stu-id="d702b-133">Advanced eDiscovery does not train based on skipped files.</span></span> <span data-ttu-id="d702b-134">Dans l’évaluation, s’il est difficile de déterminer si un fichier est pertinent, il est préférable de baliser comme pertinentes (R) ou non pertinente (NR) autant que possible, au lieu de sélectionner **Ignorer**.</span><span class="sxs-lookup"><span data-stu-id="d702b-134">In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**.</span></span> <span data-ttu-id="d702b-135">Lorsque Advanced eDiscovery évalue la formation, il peut se voir sur la manière dont ces types de fichiers ont été traités.</span><span class="sxs-lookup"><span data-stu-id="d702b-135">When Advanced eDiscovery evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="d702b-136">Même les fichiers avec une très petite quantité de texte extrait doivent être balisés en formation sous la forme R/NR, plutôt qu’en tant que « Skip », lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="d702b-136">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="d702b-137">Le marquage peut avoir un impact sur le classifieur tant que le fichier est lisible et peut être marqué comme R/NR.</span><span class="sxs-lookup"><span data-stu-id="d702b-137">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="d702b-138">Le numéro de séquence de fichier de la liste des fichiers d’exemple affichés sous l’onglet **balise** permet à l’utilisateur de revenir à l’ordre d’affichage d’origine des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d702b-138">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="d702b-139">Vous pouvez revenir à n’importe quel exemple et modifier le balisage des fichiers d’évaluation et de jeu de formation.</span><span class="sxs-lookup"><span data-stu-id="d702b-139">You can go back to any sample and change the tagging of the assessment and training set files.</span></span> <span data-ttu-id="d702b-140">Les modifications seront appliquées lors de la création de l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="d702b-140">The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="d702b-141">Les fichiers Excel numérisés au format PDF doivent être traités de la même manière que les fichiers Excel natifs lors du balisage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d702b-141">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="d702b-142">En cas de doute sur le balisage de pertinence d’un fichier, consultez un expert.</span><span class="sxs-lookup"><span data-stu-id="d702b-142">When in doubt regarding the Relevance tagging of a file, consult an expert.</span></span> <span data-ttu-id="d702b-143">Un balisage incorrect lors de la formation sur la pertinence peut entraîner un manque de temps dans le processus et peut également avoir un impact négatif sur la qualité des résultats globaux.</span><span class="sxs-lookup"><span data-stu-id="d702b-143">Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="d702b-144">Les mots clés définis dans les listes de mots clés s’affichent dans des couleurs pour aider l’utilisateur à identifier les fichiers appropriés lors du marquage.</span><span class="sxs-lookup"><span data-stu-id="d702b-144">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="d702b-145">**Calcul par lots**: les fichiers marqués comme R/NR par l’expert recevront un score de 0 ou de 100.</span><span class="sxs-lookup"><span data-stu-id="d702b-145">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100.</span></span> <span data-ttu-id="d702b-146">Cela s’applique au marquage effectué avant le calcul du lot.</span><span class="sxs-lookup"><span data-stu-id="d702b-146">This applies to tagging made before Batch calculation.</span></span> <span data-ttu-id="d702b-147">Si l’expert a activé le problème sur inactif après le calcul par lot et a continué à marquer ce problème, les scores nouvellement marqués ne seront pas 100/0 mais plutôt le score d’origine.</span><span class="sxs-lookup"><span data-stu-id="d702b-147">If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="d702b-148">**Problèmes et mode d’échantillonnage**: les problèmes sont généralement désactivés lorsqu’ils sont terminés (la formation à la pertinence est stabilisée et le calcul par lot a été effectué), lors de l’annulation des problèmes ou lorsqu’un autre utilisateur travaille sur les problèmes.</span><span class="sxs-lookup"><span data-stu-id="d702b-148">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="d702b-149">Étapes de la formation pertinente</span><span class="sxs-lookup"><span data-stu-id="d702b-149">Steps in Relevance training</span></span>

<span data-ttu-id="d702b-150">Dans l' **onglet \> suivi de pertinence** , Advanced eDiscovery fournit des recommandations sur la façon de procéder au traitement, avec les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d702b-150">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps.</span></span> <span data-ttu-id="d702b-151">Les implications sont décrites ci-dessous quand chacune des étapes suivantes est recommandée dans le processus de formation à la pertinence.</span><span class="sxs-lookup"><span data-stu-id="d702b-151">The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="d702b-152">Balisage/continuer le balisage : révision de fichier et balisage de pertinence effectuée par un expert pour chaque fichier et problème au sein d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="d702b-152">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="d702b-153">Implication : un échantillon existant doit être balisé.</span><span class="sxs-lookup"><span data-stu-id="d702b-153">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="d702b-154">Évaluation/continue Assessment : permet une validation précoce de la pertinence du problème et une vue préliminaire de la pertinence du remplissage du fichier importés pour le cas en cours.</span><span class="sxs-lookup"><span data-stu-id="d702b-154">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="d702b-155">Implication : une évaluation plus grande est requise ou recommandée.</span><span class="sxs-lookup"><span data-stu-id="d702b-155">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="d702b-156">Formation/poursuivez la formation : processus au cours duquel eDiscovery avancé apprend à l’expert qui balise les échantillons de fichiers et vous permet d’identifier les critères de pertinence pertinents pour chaque problème dans le contexte de chaque cas.</span><span class="sxs-lookup"><span data-stu-id="d702b-156">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="d702b-157">Implication : le problème nécessite une formation supplémentaire ; l’exemple suivant doit être créé et balisé.</span><span class="sxs-lookup"><span data-stu-id="d702b-157">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="d702b-158">Calcul par lot : processus de pertinence dans lequel Advanced eDiscovery prend les connaissances acquises au cours de l’étape de formation et l’applique à l’ensemble du remplissage du fichier.</span><span class="sxs-lookup"><span data-stu-id="d702b-158">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population.</span></span> <span data-ttu-id="d702b-159">Tous les fichiers du groupe de fichiers pertinent sont évalués à des fins de pertinence et reçoivent un score de pertinence.</span><span class="sxs-lookup"><span data-stu-id="d702b-159">All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="d702b-160">Implication : le problème est stabilisé et le calcul par lot peut être effectué.</span><span class="sxs-lookup"><span data-stu-id="d702b-160">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="d702b-161">Rattrapage : pertinence indique quand un expert examine et marque un échantillon de fichiers sélectionnés à partir d’une charge de fichier supplémentaire lors d’un scénario de charge en continu.</span><span class="sxs-lookup"><span data-stu-id="d702b-161">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="d702b-162">Implication : une nouvelle charge a été ajoutée et l’interception est nécessaire pour continuer à travailler.</span><span class="sxs-lookup"><span data-stu-id="d702b-162">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="d702b-163">Incohérences de balise : le processus identifie, via un algorithme eDiscovery avancé, des incohérences dans le processus de marquage de fichier susceptibles d’avoir un impact négatif sur l’analyse.</span><span class="sxs-lookup"><span data-stu-id="d702b-163">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="d702b-164">Implication : l’exemple suivant inclut des fichiers qui ont été balisés dans les exemples précédents, et leur balisage doit être rétablie.</span><span class="sxs-lookup"><span data-stu-id="d702b-164">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="d702b-165">Mettre à jour le classifieur : permet à l’utilisateur d’appliquer des balises ou des modifications.</span><span class="sxs-lookup"><span data-stu-id="d702b-165">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="d702b-166">Implication : les modifications de marquage et d’amorçage peuvent être appliquées sans avoir à exécuter manuellement un autre exemple de pertinence.</span><span class="sxs-lookup"><span data-stu-id="d702b-166">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="d702b-167">En attente : le processus d’apprentissage de pertinence est terminé.</span><span class="sxs-lookup"><span data-stu-id="d702b-167">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="d702b-168">Implication : aucune formation pertinente n’est requise à ce stade.</span><span class="sxs-lookup"><span data-stu-id="d702b-168">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="d702b-169">Bien qu’Advanced eDiscovery vous guide tout au long du processus, avec les étapes suivantes recommandées à différentes étapes, il vous permet également de naviguer entre les onglets et les pages, et de faire des choix pour répondre aux situations susceptibles de concerner votre cas, problème ou processus de révision de documents.</span><span class="sxs-lookup"><span data-stu-id="d702b-169">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="d702b-170">Il est possible d’accepter ou de remplacer les choix avancés de traitement de l’étape suivante de eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d702b-170">It is possible to accept or override Advanced eDiscovery Next step processing choices.</span></span> <span data-ttu-id="d702b-171">Si vous souhaitez effectuer une étape différente de l’étape suivante recommandée, cliquez sur l' **étape suivante** figurant dans la boîte de dialogue Affichage du problème développé dans la boîte de dialogue, cliquez sur le bouton **modifier** en regard de l’étape suivante, puis sélectionnez une autre étape suivante.</span><span class="sxs-lookup"><span data-stu-id="d702b-171">If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d702b-172">Certaines options peuvent rester désactivées après un déverrouillage, car elles ne sont pas prises en charge à ce stade du processus.</span><span class="sxs-lookup"><span data-stu-id="d702b-172">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d702b-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d702b-173">See also</span></span>

[<span data-ttu-id="d702b-174">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d702b-174">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="d702b-175">Présentation de l’évaluation en matière de pertinence</span><span class="sxs-lookup"><span data-stu-id="d702b-175">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d702b-176">Balisage et évaluation</span><span class="sxs-lookup"><span data-stu-id="d702b-176">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d702b-177">Étiquetage et formation à la pertinence</span><span class="sxs-lookup"><span data-stu-id="d702b-177">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d702b-178">Analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="d702b-178">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d702b-179">Choix en fonction des résultats</span><span class="sxs-lookup"><span data-stu-id="d702b-179">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d702b-180">Évaluation de l’analyse de pertinence</span><span class="sxs-lookup"><span data-stu-id="d702b-180">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

