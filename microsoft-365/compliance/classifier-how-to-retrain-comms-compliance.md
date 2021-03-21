---
title: Comment reformer un classifieur en conformité de communications
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
description: Découvrez comment fournir des commentaires à un classifieur entraidable dans la conformité des communications.
ms.openlocfilehash: 75fff8220b052618c70a6490b8c3569c11ecc861
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50918145"
---
# <a name="how-to-retrain-a-classifier-in-communications-compliance"></a><span data-ttu-id="c69c3-103">Comment reformer un classifieur en conformité de communications</span><span class="sxs-lookup"><span data-stu-id="c69c3-103">How to retrain a classifier in communications compliance</span></span>

<span data-ttu-id="c69c3-104">Un classifieur Entraéable Microsoft 365 est un outil que vous pouvez former pour reconnaître différents types de contenu en lui donnant des exemples à examiner.</span><span class="sxs-lookup"><span data-stu-id="c69c3-104">A Microsoft 365 trainable classifier is a tool you can train to recognize various types of content by giving it samples to look at.</span></span> <span data-ttu-id="c69c3-105">Une fois formé, vous pouvez l’utiliser pour identifier l’élément pour l’application des étiquettes de confidentialité Office, des stratégies de conformité des communications et des stratégies d’étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="c69c3-105">Once trained, you can use it to identify item for application of Office sensitivity labels, communications compliance policies, and retention label policies.</span></span>

<span data-ttu-id="c69c3-106">Cet article vous montre comment améliorer les performances des classifieurs entraisables personnalisés et de certains classifieurs pré-formés en leur fournissant des commentaires supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c69c3-106">This article shows you how to improve the performance of custom trainable classifiers and some pre-trained classifiers by providing them additional feedback.</span></span>

<span data-ttu-id="c69c3-107">Pour en savoir plus sur les différents types de classifieurs, voir En savoir plus sur les [classifieurs entraisables.](classifier-learn-about.md)</span><span class="sxs-lookup"><span data-stu-id="c69c3-107">To learn more about the different types of classifiers, see [Learn about trainable classifiers](classifier-learn-about.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="c69c3-108">Autorisations</span><span class="sxs-lookup"><span data-stu-id="c69c3-108">Permissions</span></span>

<span data-ttu-id="c69c3-109">Pour accéder aux classifieurs dans le Centre de conformité Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="c69c3-109">To access classifiers in the Microsoft 365 Compliance center:</span></span>

- <span data-ttu-id="c69c3-110">le rôle d’administrateur de conformité ou l’administrateur des données de conformité est requis pour former un classificateur</span><span class="sxs-lookup"><span data-stu-id="c69c3-110">the Compliance admin role or Compliance Data Administrator is required to train a classifier</span></span>

<span data-ttu-id="c69c3-111">Vous aurez besoin de comptes avec ces autorisations pour utiliser des classifieurs dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="c69c3-111">You'll need accounts with these permissions to use classifiers in these scenarios:</span></span>

- <span data-ttu-id="c69c3-112">Scénario de stratégie de conformité des communications : administrateur de la gestion des risques internes, administrateur de vérification de surveillance</span><span class="sxs-lookup"><span data-stu-id="c69c3-112">Communication compliance policy scenario: Insider Risk Management Admin, Supervisory Review Administrator</span></span> 

## <a name="overall-workflow"></a><span data-ttu-id="c69c3-113">Flux de travail global</span><span class="sxs-lookup"><span data-stu-id="c69c3-113">Overall workflow</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c69c3-114">Vous fournissez des commentaires dans la solution de conformité qui utilise le classificateur comme condition.</span><span class="sxs-lookup"><span data-stu-id="c69c3-114">You provide feedback in the compliance solution that is using the classifier as a condition.</span></span> <span data-ttu-id="c69c3-115">**Si vous n’avez pas de stratégie de conformité des communications qui utilise un classificateur comme condition, arrêtez-vous ici.**</span><span class="sxs-lookup"><span data-stu-id="c69c3-115">**If you don't have a communications compliance policy that uses a classifier as a condition, stop here.**</span></span>

<span data-ttu-id="c69c3-116">Lorsque vous utilisez vos classifieurs, vous souhaitez peut-être augmenter la précision des classifications qu’ils sont en train d’effectuer.</span><span class="sxs-lookup"><span data-stu-id="c69c3-116">As you use your classifiers, you may want to increase the precision of the classifications that they're making.</span></span> <span data-ttu-id="c69c3-117">Pour ce faire, vous évaluez la qualité des classifications des éléments qu’il a identifiés comme étant une correspondance ou non.</span><span class="sxs-lookup"><span data-stu-id="c69c3-117">You do this by evaluating the quality of the classifications made  for items it has identified as being a match or not a match.</span></span> <span data-ttu-id="c69c3-118">Une fois que vous avez fait 30 évaluations pour un classificateur, il prend ce retour d’expérience et se réévalue automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c69c3-118">After you make 30 evaluations for a classifier it takes that feedback and automatically retrains itself.</span></span>

<span data-ttu-id="c69c3-119">Pour en savoir plus sur le flux de travail global de la nouvelle formation d’un classifieur, voir Flux de processus pour former à nouveau [un classificateur.](classifier-learn-about.md#retraining-classifiers)</span><span class="sxs-lookup"><span data-stu-id="c69c3-119">To understand more about the overall workflow of retraining a classifier, see [Process flow for retraining a classifier](classifier-learn-about.md#retraining-classifiers).</span></span>

> [!NOTE]
> <span data-ttu-id="c69c3-120">Un classifieur doit déjà être publié et en cours d’utilisation avant de pouvoir être à nouveau formé.</span><span class="sxs-lookup"><span data-stu-id="c69c3-120">A classifier must already be published and in use before it can be retrained.</span></span>

## <a name="how-to-retrain-a-classifier-in-communication-compliance-policies"></a><span data-ttu-id="c69c3-121">Comment former à nouveau un classificateur dans les stratégies de conformité des communications</span><span class="sxs-lookup"><span data-stu-id="c69c3-121">How to retrain a classifier in communication compliance policies</span></span>

1. <span data-ttu-id="c69c3-122">Ouvrez la stratégie de conformité des communications qui utilise un classificateur comme condition et choisissez l’un des éléments identifiés dans la **liste En** attente.</span><span class="sxs-lookup"><span data-stu-id="c69c3-122">Open the Communication compliance policy that uses a classifier as a condition and choose one of the identified items from the **Pending** list.</span></span>
2. <span data-ttu-id="c69c3-123">Choisissez les points de non-accès et **améliorez la classification.**</span><span class="sxs-lookup"><span data-stu-id="c69c3-123">Choose the ellipsis and **Improve classification**.</span></span>
3. <span data-ttu-id="c69c3-124">Dans le **volet commentaires détaillés,** si l’élément est un vrai positif, choisissez, **Match**.</span><span class="sxs-lookup"><span data-stu-id="c69c3-124">In the **Detailed feedback** pane, if the item is a true positive, choose, **Match**.</span></span>  <span data-ttu-id="c69c3-125">Si l’élément est un faux positif, c’est-à-dire qu’il a été inclus de manière incorrecte dans la catégorie, **sélectionnez Ne pas correspondre.**</span><span class="sxs-lookup"><span data-stu-id="c69c3-125">If the item is a false positive, that is it was incorrectly included in the category, choose **Not a match**.</span></span>
4. <span data-ttu-id="c69c3-126">S’il existe un autre classificateur qui serait plus approprié pour l’élément, vous pouvez le choisir dans la liste Suggérer d’autres **classifieurs entra nessifiables.**</span><span class="sxs-lookup"><span data-stu-id="c69c3-126">If there is another classifier that would be more appropriate for the item, you can choose it from the **Suggest other trainable classifiers** list.</span></span> <span data-ttu-id="c69c3-127">Cela déclenchera l’évaluation de l’élément par l’autre classificateur.</span><span class="sxs-lookup"><span data-stu-id="c69c3-127">This will trigger the other classifier to evaluate the item.</span></span>

> [!TIP]
> <span data-ttu-id="c69c3-128">Vous pouvez fournir des commentaires sur plusieurs éléments simultanément en les sélectionnant tous, puis en sélectionnant Fournir des commentaires détaillés **dans** la barre de commandes.</span><span class="sxs-lookup"><span data-stu-id="c69c3-128">You can provide feedback on multiple items simultaneously by choosing them all and then choosing **Provide detailed feedback** in the command bar.</span></span>

5. <span data-ttu-id="c69c3-129">Choose **Send feedback** to send your evaluation of the , `match` `not a match` classifications and suggest other trainable classifiers.</span><span class="sxs-lookup"><span data-stu-id="c69c3-129">Choose **Send feedback** to send your evaluation of the `match`, `not a match` classifications and suggest other trainable classifiers.</span></span> <span data-ttu-id="c69c3-130">Lorsque vous avez fourni 30 instances de commentaires à un classifieur, il se formera automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c69c3-130">When you've provided 30 instances of feedback to a classifier, it will automatically  retrain.</span></span> <span data-ttu-id="c69c3-131">La formation peut prendre entre 1 et 4 heures.</span><span class="sxs-lookup"><span data-stu-id="c69c3-131">Retraining can take from 1-4 hours.</span></span> <span data-ttu-id="c69c3-132">Les classifieurs ne peuvent être formés que deux fois par jour.</span><span class="sxs-lookup"><span data-stu-id="c69c3-132">Classifiers can only be retrained twice per day.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c69c3-133">Ces informations sont ensuite données au classifieur de votre client, elles ne sont **pas revenir à Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="c69c3-133">This information goes to the classifier in your tenant, **it does not go back to Microsoft**.</span></span>

6.  <span data-ttu-id="c69c3-134">Ouvrez la page **Classification des** données dans le Centre de conformité Microsoft **365.**</span><span class="sxs-lookup"><span data-stu-id="c69c3-134">Open the **Data classification** page in the **Microsoft 365 compliance center**.</span></span>
7. <span data-ttu-id="c69c3-135">Ouvrez **les classifieurs Avec formation.**</span><span class="sxs-lookup"><span data-stu-id="c69c3-135">Open **Trainable classifiers**.</span></span>
8. <span data-ttu-id="c69c3-136">Le classificateur qui a été utilisé dans votre stratégie de conformité des communications s’affiche sous **l’en-tête Nouvelle** formation.</span><span class="sxs-lookup"><span data-stu-id="c69c3-136">The classifier that was used in your Communications compliance policy will appear under the **Re-training** heading.</span></span>

![classifieur dans l’état de la formation](../media/classifier-retraining.png)

9. <span data-ttu-id="c69c3-138">Une fois la nouvelle formation terminée, choisissez le classificateur pour ouvrir la vue d’ensemble de la nouvelle formation.</span><span class="sxs-lookup"><span data-stu-id="c69c3-138">Once retraining completes, choose the classifier to open the retraining overview.</span></span>

![Vue d’ensemble des résultats de la formation du classificateur](../media/classifier-retraining-overview.png)

10. <span data-ttu-id="c69c3-140">Examinez l’action recommandée et les comparaisons de prédictions des versions réétrainées et actuellement publiées du classificateur.</span><span class="sxs-lookup"><span data-stu-id="c69c3-140">Review the recommended action, and the prediction comparisons of the retrained and currently published versions of the classifier.</span></span>
11. <span data-ttu-id="c69c3-141">If you satisfied with the results of the retraining, choose **Re-publish**.</span><span class="sxs-lookup"><span data-stu-id="c69c3-141">If you satisfied with the results of the retraining, choose **Re-publish**.</span></span>
12. <span data-ttu-id="c69c3-142">Si vous n’êtes pas satisfait des résultats de la nouvelle formation, vous pouvez choisir de fournir des commentaires supplémentaires au classifieur dans l’interface de conformité des communications et de démarrer un autre cycle de formation ou de ne rien faire, auquel cas la version actuellement publiée du classificateur continuera d’être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c69c3-142">If you are not satisfied with the results of the retraining, you can choose to provide additional feedback to the classifier in the Communications compliance interface and start another retraining cycle or do nothing in which case the currently published version of the classifier will continue to be used.</span></span> 

## <a name="details-on-republishing-recommendations"></a><span data-ttu-id="c69c3-143">Détails sur la republier des recommandations</span><span class="sxs-lookup"><span data-stu-id="c69c3-143">Details on republishing recommendations</span></span>

<span data-ttu-id="c69c3-144">Voici quelques informations sur la façon dont nous vous suggérons de publier à nouveau un classifieur retrained ou de suggérer une nouvelle formation.</span><span class="sxs-lookup"><span data-stu-id="c69c3-144">Here is a little information on how we formulate the recommendation to re-publish a retrained classifier or suggest further retraining.</span></span> <span data-ttu-id="c69c3-145">Cela nécessite une compréhension plus approfondie du fonctionnement des classifieurs entraisables.</span><span class="sxs-lookup"><span data-stu-id="c69c3-145">This requires a little deeper understanding of how trainable classifiers work.</span></span>

<span data-ttu-id="c69c3-146">Après une nouvelle formation, nous évaluons les performances du classificateur à la fois sur les éléments avec des commentaires, ainsi que sur tous les éléments utilisés à l’origine pour former le classificateur.</span><span class="sxs-lookup"><span data-stu-id="c69c3-146">After a retrain, we evaluate the classifier's performance on both the items with feedback as well as any items originally used to train the classifier.</span></span> 

- <span data-ttu-id="c69c3-147">Pour les modèles intégrés, les éléments utilisés pour former le classifieur sont les éléments utilisés par Microsoft pour créer le modèle.</span><span class="sxs-lookup"><span data-stu-id="c69c3-147">For built-in models, items used to train the classifier are the items used by Microsoft to build the model.</span></span>
- <span data-ttu-id="c69c3-148">Pour les modèles personnalisés, les éléments utilisés dans la formation d’origine du classifieur sont issus des sites que vous avez ajoutés pour le test et la révision.</span><span class="sxs-lookup"><span data-stu-id="c69c3-148">For custom models, items used in the original training the classifier are from the sites you had added for test and review.</span></span>

<span data-ttu-id="c69c3-149">Nous comparons les nombres de performances sur les deux ensembles d’éléments pour le classifieur réécrit et publié afin de fournir une recommandation quant à l’amélioration de la republier.</span><span class="sxs-lookup"><span data-stu-id="c69c3-149">We compare the performance numbers on both sets of items for the retrained and published classifier to provide a recommendation on whether there was improvement to republish.</span></span> 

## <a name="see-also"></a><span data-ttu-id="c69c3-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c69c3-150">See also</span></span>

- [<span data-ttu-id="c69c3-151">En savoir plus sur les classifieurs avec capacité d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="c69c3-151">Learn about trainable classifiers</span></span>](classifier-learn-about.md)
- [<span data-ttu-id="c69c3-152">Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="c69c3-152">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)