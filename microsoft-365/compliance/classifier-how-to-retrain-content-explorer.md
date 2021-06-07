---
title: Comment reformer un classificateur en explorateur de contenu
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez comment fournir des commentaires à un classifieur entraidable dans l’Explorateur de contenu.
ms.openlocfilehash: ef0539a3d474ffecaeac8633b4a58aa068a5c182
ms.sourcegitcommit: f3d1009840513703c38bab99a6e13a3656eae5ee
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/07/2021
ms.locfileid: "52793063"
---
# <a name="how-to-retrain-a-classifier-in-content-explorer"></a><span data-ttu-id="eac94-103">Comment reformer un classificateur en explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="eac94-103">How to retrain a classifier in content explorer</span></span>

<span data-ttu-id="eac94-104">Un Microsoft 365 classifieur entraisable est un outil que vous pouvez former pour reconnaître différents types de contenu en lui donnant des exemples à examiner.</span><span class="sxs-lookup"><span data-stu-id="eac94-104">A Microsoft 365 trainable classifier is a tool you can train to recognize various types of content by giving it samples to look at.</span></span> <span data-ttu-id="eac94-105">Une fois formé, vous pouvez l’utiliser pour identifier l’élément à appliquer Office étiquettes de confidentialité, stratégies de conformité des communications et stratégies d’étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="eac94-105">Once trained, you can use it to identify item for application of Office sensitivity labels, communications compliance policies, and retention label policies.</span></span>

<span data-ttu-id="eac94-106">Cet article vous montre comment améliorer les performances des classifieurs entraisables personnalisés et de certains classifieurs pré-formés en leur fournissant des commentaires supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="eac94-106">This article shows you how to improve the performance of custom trainable classifiers and some pre-trained classifiers by providing them additional feedback.</span></span>

<span data-ttu-id="eac94-107">Pour en savoir plus sur les différents types de classifieurs, voir En savoir plus sur les [classifieurs entraisables.](classifier-learn-about.md)</span><span class="sxs-lookup"><span data-stu-id="eac94-107">To learn more about the different types of classifiers, see [Learn about trainable classifiers](classifier-learn-about.md).</span></span>

<span data-ttu-id="eac94-108">Regardez cette vidéo pour obtenir un résumé rapide du processus d’ajustement et de formation.</span><span class="sxs-lookup"><span data-stu-id="eac94-108">Watch this video for a quick summary of the tuning and retraining process.</span></span> <span data-ttu-id="eac94-109">Vous devrez tout de même lire cet article complet pour obtenir les détails.</span><span class="sxs-lookup"><span data-stu-id="eac94-109">You'll still need to read this full article to get the details.</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWyGMs]


## <a name="permissions"></a><span data-ttu-id="eac94-110">Autorisations</span><span class="sxs-lookup"><span data-stu-id="eac94-110">Permissions</span></span>

<span data-ttu-id="eac94-111">Pour accéder aux classifieurs dans le centre Microsoft 365 conformité :</span><span class="sxs-lookup"><span data-stu-id="eac94-111">To access classifiers in the Microsoft 365 Compliance center:</span></span>

- <span data-ttu-id="eac94-112">le rôle d’administrateur de conformité ou l’administrateur des données de conformité est requis pour former un classificateur</span><span class="sxs-lookup"><span data-stu-id="eac94-112">the Compliance admin role or Compliance Data Administrator is required to train a classifier</span></span>

<span data-ttu-id="eac94-113">Vous aurez besoin de comptes avec ces autorisations pour utiliser des classifieurs dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="eac94-113">You'll need accounts with these permissions to use classifiers in these scenarios:</span></span>

- <span data-ttu-id="eac94-114">Scénario de stratégie d’étiquette de rétention : rôles gestion des enregistrement et gestion de la rétention</span><span class="sxs-lookup"><span data-stu-id="eac94-114">Retention label policy scenario: Record Management and Retention Management roles</span></span> 

## <a name="overall-workflow"></a><span data-ttu-id="eac94-115">Flux de travail global</span><span class="sxs-lookup"><span data-stu-id="eac94-115">Overall workflow</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eac94-116">Vous fournissez des commentaires dans l’Explorateur de contenu pour appliquer automatiquement des stratégies d’étiquette de rétention Exchange les éléments et utilise le classifieur comme condition.</span><span class="sxs-lookup"><span data-stu-id="eac94-116">You provide feedback in content explorer for auto-apply retention label policies to Exchange items and uses the classifier as a condition.</span></span> <span data-ttu-id="eac94-117">**Si vous n’avez pas de stratégie de rétention qui applique automatiquement une étiquette de rétention à Exchange éléments et utilise un classificateur comme condition, arrêtez-vous ici.**</span><span class="sxs-lookup"><span data-stu-id="eac94-117">**If you don't have a retention policy that auto-applies a retention label to Exchange items and      uses a classifier as a condition, stop here.**</span></span>

<span data-ttu-id="eac94-118">Lorsque vous utilisez vos classifieurs, vous souhaitez peut-être augmenter la précision des classifications qu’ils sont en train d’effectuer.</span><span class="sxs-lookup"><span data-stu-id="eac94-118">As you use your classifiers, you may want to increase the precision of the classifications that they're making.</span></span> <span data-ttu-id="eac94-119">Pour ce faire, vous devez évaluer la qualité des classifications des éléments qu’il a identifiés comme étant une correspondance ou non.</span><span class="sxs-lookup"><span data-stu-id="eac94-119">You do this by evaluating the quality of the classifications made  for items it has identified as being a match or not a match.</span></span> <span data-ttu-id="eac94-120">Une fois que vous avez fait 30 évaluations pour un classificateur, il prend ce retour d’expérience et se réévalue automatiquement.</span><span class="sxs-lookup"><span data-stu-id="eac94-120">After you make 30 evaluations for a classifier it takes that feedback and automatically retrains itself.</span></span>

<span data-ttu-id="eac94-121">Pour en savoir plus sur le flux de travail global de la nouvelle formation d’un classifieur, voir Flux de processus pour former à nouveau [un classificateur.](classifier-learn-about.md#retraining-classifiers)</span><span class="sxs-lookup"><span data-stu-id="eac94-121">To understand more about the overall workflow of retraining a classifier, see [Process flow for retraining a classifier](classifier-learn-about.md#retraining-classifiers).</span></span>

> [!NOTE]
> <span data-ttu-id="eac94-122">Un classificateur doit déjà être publié et en cours d’utilisation avant de pouvoir être à nouveau formé.</span><span class="sxs-lookup"><span data-stu-id="eac94-122">A classifier must already be published and in use before it can be retrained.</span></span>

## <a name="how-to-retrain-a-classifier-in-content-explorer"></a><span data-ttu-id="eac94-123">Comment reformer un classificateur en explorateur de contenu</span><span class="sxs-lookup"><span data-stu-id="eac94-123">How to retrain a classifier in content explorer</span></span>

1. <span data-ttu-id="eac94-124">Connectez-vous au centre Microsoft 365 conformité avec l’accès au rôle d’administrateur de conformité ou d’administrateur de sécurité et ouvrez **Microsoft 365'explorateur** de contenu de classification des données du centre  >    >  **de conformité.**</span><span class="sxs-lookup"><span data-stu-id="eac94-124">Sign in to Microsoft 365 compliance center with compliance admin or security admin role access and open **Microsoft 365 compliance center** > **Data classification** > **Content explorer**.</span></span> 
2. <span data-ttu-id="eac94-125">Sous le filtre **sur les étiquettes, les types d’informations** ou la liste des catégories, développez **classifieurs Avec formation.**</span><span class="sxs-lookup"><span data-stu-id="eac94-125">Under the **Filter on labels, info types, or categories** list, expand **Trainable classifiers**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eac94-126">L’apparition des éléments agrégés sous l’en-tête classifieurs entraçables peut prendre jusqu’à huit jours.</span><span class="sxs-lookup"><span data-stu-id="eac94-126">It can take up to eight days for aggregated items to appear under the trainable classifiers heading.</span></span>

3. <span data-ttu-id="eac94-127">Choisissez le classifieur entraisable que vous avez utilisé dans votre stratégie d’étiquette de rétention à appliquer automatiquement.</span><span class="sxs-lookup"><span data-stu-id="eac94-127">Choose the trainable classifier you used in you auto-apply retention label policy.</span></span> <span data-ttu-id="eac94-128">Il s’agit du classifieur entraçable sur qui vous allez nous faire part de vos commentaires.</span><span class="sxs-lookup"><span data-stu-id="eac94-128">This is the trainable classifier you will give feedback on.</span></span>

> [!NOTE]
> <span data-ttu-id="eac94-129">Si un élément possède une entrée dans la **colonne** Étiquette de rétention, cela signifie que l’élément a été classé en tant que `match` .</span><span class="sxs-lookup"><span data-stu-id="eac94-129">If an item has an entry in the **Retention label** column, it means that the item was classified as a `match`.</span></span>  <span data-ttu-id="eac94-130">Si un élément n’a pas  d’entrée dans la colonne Étiquette de rétention, cela signifie qu’il a été classé en tant que `close match` .</span><span class="sxs-lookup"><span data-stu-id="eac94-130">If an item doesn't have an entry in the **Retention label** column, it means it was classified as a `close match`.</span></span> <span data-ttu-id="eac94-131">Vous pouvez améliorer le plus la précision du classificateur en fournissant des commentaires sur `close match` les éléments.</span><span class="sxs-lookup"><span data-stu-id="eac94-131">You can improve the classifier precision the most by providing feedback on `close match` items.</span></span> 

4. <span data-ttu-id="eac94-132">Choisissez un élément et ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="eac94-132">Choose an item and open it.</span></span>
 
 > [!TIP]
> <span data-ttu-id="eac94-133">Vous pouvez fournir des commentaires sur plusieurs éléments simultanément en les sélectionnant tous, puis en choisissant **Améliorer la classification** dans la barre de commandes.</span><span class="sxs-lookup"><span data-stu-id="eac94-133">You can provide feedback on multiple items simultaneously by choosing them all and then choosing **Improve classification** in the command bar.</span></span>

5. <span data-ttu-id="eac94-134">Choose **Provide feedback**.</span><span class="sxs-lookup"><span data-stu-id="eac94-134">Choose **Provide feedback**.</span></span>
6. <span data-ttu-id="eac94-135">Dans le **volet commentaires détaillés,** si l’élément est un vrai positif, choisissez, **Match**.</span><span class="sxs-lookup"><span data-stu-id="eac94-135">In the **Detailed feedback** pane, if the item is a true positive, choose, **Match**.</span></span>  <span data-ttu-id="eac94-136">Si l’élément est un faux positif, c’est-à-dire qu’il a été inclus de manière incorrecte dans la catégorie, **sélectionnez Ne pas correspondre.**</span><span class="sxs-lookup"><span data-stu-id="eac94-136">If the item is a false positive, that is it was incorrectly included in the category, choose **Not a match**.</span></span>
7. <span data-ttu-id="eac94-137">S’il existe un autre classificateur qui serait plus approprié pour l’élément, vous pouvez le choisir dans la liste Suggérer d’autres **classifieurs entra nessifiables.**</span><span class="sxs-lookup"><span data-stu-id="eac94-137">If there is another classifier that would be more appropriate for the item, you can choose it from the **Suggest other trainable classifiers** list.</span></span> <span data-ttu-id="eac94-138">Cela déclenchera l’évaluation de l’élément par l’autre classificateur.</span><span class="sxs-lookup"><span data-stu-id="eac94-138">This will trigger the other classifier to evaluate the item.</span></span>
8. <span data-ttu-id="eac94-139">Choose **Send feedback** to send your evaluation of the , `match` `not a match` classifications and suggest other trainable classifiers.</span><span class="sxs-lookup"><span data-stu-id="eac94-139">Choose **Send feedback** to send your evaluation of the `match`, `not a match` classifications and suggest other trainable classifiers.</span></span> <span data-ttu-id="eac94-140">Une fois que vous avez fourni 30 instances de commentaires à un classifieur, il se formera automatiquement.</span><span class="sxs-lookup"><span data-stu-id="eac94-140">When you've provided 30 instances of feedback to a classifier, it will automatically  retrain.</span></span> <span data-ttu-id="eac94-141">La formation peut prendre entre une et quatre heures.</span><span class="sxs-lookup"><span data-stu-id="eac94-141">Retraining can take from one to four hours.</span></span> <span data-ttu-id="eac94-142">Les classifieurs ne peuvent être formés que deux fois par jour.</span><span class="sxs-lookup"><span data-stu-id="eac94-142">Classifiers can only be retrained twice per day.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eac94-143">Ces informations sont ensuite données au classifieur de votre client, elles ne sont **pas revenir à Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="eac94-143">This information goes to the classifier in your tenant, **it does not go back to Microsoft**.</span></span>

9. <span data-ttu-id="eac94-144">Ouvrez **les classifieurs Avec formation.**</span><span class="sxs-lookup"><span data-stu-id="eac94-144">Open **Trainable classifiers**.</span></span>
10. <span data-ttu-id="eac94-145">Le classificateur qui a été utilisé dans votre stratégie de conformité des communications s’affiche sous **l’en-tête Nouvelle** formation.</span><span class="sxs-lookup"><span data-stu-id="eac94-145">The classifier that was used in your Communications compliance policy will appear under the **Re-training** heading.</span></span>

![classifieur dans l’état de la formation](../media/classifier-retraining.png)

11. <span data-ttu-id="eac94-147">Une fois la nouvelle formation terminée, choisissez le classificateur pour ouvrir la vue d’ensemble de la nouvelle formation.</span><span class="sxs-lookup"><span data-stu-id="eac94-147">Once retraining completes, choose the classifier to open the retraining overview.</span></span>

![Vue d’ensemble des résultats de la formation du classificateur](../media/classifier-retraining-overview.png)

12. <span data-ttu-id="eac94-149">Examinez l’action recommandée, ainsi que les comparaisons de prédictions des versions du classifieur actuellement publiées et retentées.</span><span class="sxs-lookup"><span data-stu-id="eac94-149">Review the recommended action, and the prediction comparisons of the retrained and currently published versions of the classifier.</span></span>
13. <span data-ttu-id="eac94-150">If you satisfied with the results of the retraining, choose **Re-publish**.</span><span class="sxs-lookup"><span data-stu-id="eac94-150">If you satisfied with the results of the retraining, choose **Re-publish**.</span></span>
14. <span data-ttu-id="eac94-151">Si vous n’êtes pas satisfait des résultats de la nouvelle formation, vous pouvez choisir de fournir des commentaires supplémentaires au classificateur dans l’interface de l’Explorateur de contenu et de démarrer un autre cycle de formation ou de ne rien faire, auquel cas la version actuellement publiée du classificateur continuera d’être utilisée.</span><span class="sxs-lookup"><span data-stu-id="eac94-151">If you are not satisfied with the results of the retraining, you can choose to provide additional feedback to the classifier in the Content Explorer interface and start another retraining cycle or do nothing in which case the currently published version of the classifier will continue to be used.</span></span> 

## <a name="details-on-republishing-recommendations"></a><span data-ttu-id="eac94-152">Détails sur la republier des recommandations</span><span class="sxs-lookup"><span data-stu-id="eac94-152">Details on republishing recommendations</span></span>

<span data-ttu-id="eac94-153">Voici quelques informations sur la façon dont nous formulerons la recommandation pour publier à nouveau un classifieur retrained ou suggérer une nouvelle formation.</span><span class="sxs-lookup"><span data-stu-id="eac94-153">Here is a little information on how we formulate the recommendation to re-publish a retrained classifier or suggest further retraining.</span></span> <span data-ttu-id="eac94-154">Cela nécessite une compréhension plus approfondie du fonctionnement des classifieurs entraisables.</span><span class="sxs-lookup"><span data-stu-id="eac94-154">This requires a little deeper understanding of how trainable classifiers work.</span></span>

<span data-ttu-id="eac94-155">Après une nouvelle formation, nous évaluons les performances du classificateur à la fois sur les éléments avec des commentaires, ainsi que sur tous les éléments utilisés à l’origine pour former le classificateur.</span><span class="sxs-lookup"><span data-stu-id="eac94-155">After a retrain, we evaluate the classifier's performance on both the items with feedback as well as any items originally used to train the classifier.</span></span> 

- <span data-ttu-id="eac94-156">Pour les modèles intégrés, les éléments utilisés pour former le classifieur sont les éléments utilisés par Microsoft pour créer le modèle.</span><span class="sxs-lookup"><span data-stu-id="eac94-156">For built-in models, items used to train the classifier are the items used by Microsoft to build the model.</span></span>
- <span data-ttu-id="eac94-157">Pour les modèles personnalisés, les éléments utilisés dans la formation d’origine du classifieur sont issus des sites que vous avez ajoutés pour le test et la révision.</span><span class="sxs-lookup"><span data-stu-id="eac94-157">For custom models, items used in the original training the classifier are from the sites you had added for test and review.</span></span>

<span data-ttu-id="eac94-158">Nous comparons les nombres de performances sur les deux ensembles d’éléments pour le classifieur réécrit et publié afin de fournir une recommandation sur l’amélioration de la publication.</span><span class="sxs-lookup"><span data-stu-id="eac94-158">We compare the performance numbers on both sets of items for the retrained and published classifier to provide a recommendation on whether there was improvement to republish.</span></span> 

## <a name="see-also"></a><span data-ttu-id="eac94-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eac94-159">See also</span></span>

- [<span data-ttu-id="eac94-160">En savoir plus sur les classifieurs avec capacité d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="eac94-160">Learn about trainable classifiers</span></span>](classifier-learn-about.md)
- [<span data-ttu-id="eac94-161">Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="eac94-161">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)