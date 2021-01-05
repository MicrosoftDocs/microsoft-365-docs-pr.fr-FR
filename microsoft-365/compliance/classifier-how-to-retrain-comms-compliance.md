---
title: Procédure de recyclage d’un classifieur dans la conformité des communications
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
description: Découvrez comment fournir des commentaires à un classificateur de formation dans le respect des communications.
ms.openlocfilehash: cdb8787715c3e022dfa0aa17cd83cc405aeef955
ms.sourcegitcommit: 54d1a2f363b2d5b63aae258c3cec0573a08f2866
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "49752648"
---
# <a name="how-to-retrain-a-classifier-in-communications-compliance"></a><span data-ttu-id="de570-103">Procédure de recyclage d’un classifieur dans la conformité des communications</span><span class="sxs-lookup"><span data-stu-id="de570-103">How to retrain a classifier in communications compliance</span></span>

<span data-ttu-id="de570-104">Un classificateur Microsoft 365 pouvant être formé est un outil que vous pouvez former afin de reconnaître différents types de contenu en leur donnant des exemples à consulter.</span><span class="sxs-lookup"><span data-stu-id="de570-104">A Microsoft 365 trainable classifier is a tool you can train to recognize various types of content by giving it samples to look at.</span></span> <span data-ttu-id="de570-105">Une fois l’apprentissage effectué, vous pouvez l’utiliser pour identifier un élément pour l’application des étiquettes de sensibilité d’Office, des stratégies de conformité des communications et des stratégies d’étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="de570-105">Once trained, you can use it to identify item for application of Office sensitivity labels, communications compliance policies, and retention label policies.</span></span>

<span data-ttu-id="de570-106">Cet article vous explique comment améliorer les performances des classifieurs de formation personnalisée et de certains classifieurs pré-formés en leur fournissant des commentaires supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="de570-106">This article shows you how to improve the performance of custom trainable classifiers and some pre-trained classifiers by providing them additional feedback.</span></span>

<span data-ttu-id="de570-107">Pour en savoir plus sur les différents types de classifieurs, reportez-vous à la rubrique [en savoir plus sur les classifieurs de formation](classifier-learn-about.md).</span><span class="sxs-lookup"><span data-stu-id="de570-107">To learn more about the different types of classifiers, see [Learn about trainable classifiers](classifier-learn-about.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="de570-108">Autorisations</span><span class="sxs-lookup"><span data-stu-id="de570-108">Permissions</span></span>

<span data-ttu-id="de570-109">Pour accéder aux classifieurs dans le centre de conformité Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="de570-109">To access classifiers in the Microsoft 365 Compliance center:</span></span>

- <span data-ttu-id="de570-110">le rôle d’administrateur de conformité ou l’administrateur des données de conformité est requis pour former un classifieur</span><span class="sxs-lookup"><span data-stu-id="de570-110">the Compliance admin role or Compliance Data Administrator is required to train a classifier</span></span>

<span data-ttu-id="de570-111">Vous aurez besoin de comptes dotés des autorisations suivantes pour utiliser les classifieurs dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="de570-111">You'll need accounts with these permissions to use classifiers in these scenarios:</span></span>

- <span data-ttu-id="de570-112">Scénario de stratégie de conformité des communications : administrateur de gestion des risques Insiders, administrateur de vérification de la surveillance</span><span class="sxs-lookup"><span data-stu-id="de570-112">Communication compliance policy scenario: Insider Risk Management Admin, Supervisory Review Administrator</span></span> 

## <a name="overall-workflow"></a><span data-ttu-id="de570-113">Flux de travail global</span><span class="sxs-lookup"><span data-stu-id="de570-113">Overall workflow</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de570-114">Vous fournissez des commentaires dans la solution de conformité qui utilise le classifieur comme condition.</span><span class="sxs-lookup"><span data-stu-id="de570-114">You provide feedback in the compliance solution that is using the classifier as a condition.</span></span> <span data-ttu-id="de570-115">**Si vous n’avez pas de stratégie de conformité des communications qui utilise un classifieur comme condition, arrêtez-vous ici.**</span><span class="sxs-lookup"><span data-stu-id="de570-115">**If you don't have a communications compliance policy that uses a classifier as a condition, stop here.**</span></span>

<span data-ttu-id="de570-116">Lorsque vous utilisez vos classifieurs, vous souhaiterez peut-être augmenter la précision des classifications qu’ils effectuent.</span><span class="sxs-lookup"><span data-stu-id="de570-116">As you use your classifiers, you may want to increase the precision of the classifications that they're making.</span></span> <span data-ttu-id="de570-117">Pour ce faire, vous évaluez la qualité des classifications effectuées pour les éléments qu’il a identifiés comme étant une correspondance ou non.</span><span class="sxs-lookup"><span data-stu-id="de570-117">You do this by evaluating the quality of the classifications made  for items it has identified as being a match or not a match.</span></span> <span data-ttu-id="de570-118">Une fois que vous avez effectué 30 évaluations pour un classifieur, il effectue ces commentaires et proveille lui-même automatiquement.</span><span class="sxs-lookup"><span data-stu-id="de570-118">After you make 30 evaluations for a classifier it takes that feedback and automatically retrains itself.</span></span>

<span data-ttu-id="de570-119">Pour en savoir plus sur le flux de travail global de recyclage d’un classifieur, consultez la rubrique [processus Flow for Retraining a classificateur](classifier-learn-about.md#retraining-classifiers).</span><span class="sxs-lookup"><span data-stu-id="de570-119">To understand more about the overall workflow of retraining a classifier, see [Process flow for retraining a classifier](classifier-learn-about.md#retraining-classifiers).</span></span>

> [!NOTE]
> <span data-ttu-id="de570-120">Un classifieur doit déjà être publié et en cours d’utilisation avant de pouvoir être reformé.</span><span class="sxs-lookup"><span data-stu-id="de570-120">A classifier must already be published and in use before it can be retrained.</span></span>

## <a name="how-to-retrain-a-classifier-in-communication-compliance-policies"></a><span data-ttu-id="de570-121">Procédure de recyclage d’un classifieur dans les stratégies de conformité de communication</span><span class="sxs-lookup"><span data-stu-id="de570-121">How to retrain a classifier in communication compliance policies</span></span>

1. <span data-ttu-id="de570-122">Ouvrez la stratégie de conformité de communication qui utilise un classifieur comme condition et choisissez l’un des éléments identifiés dans la liste **en attente** .</span><span class="sxs-lookup"><span data-stu-id="de570-122">Open the Communication compliance policy that uses a classifier as a condition and choose one of the identified items from the **Pending** list.</span></span>
2. <span data-ttu-id="de570-123">Choisissez les points de suspension et **améliorer la classification**.</span><span class="sxs-lookup"><span data-stu-id="de570-123">Choose the ellipsis and **Improve classification**.</span></span>
3. <span data-ttu-id="de570-124">Dans le volet **commentaires détaillés** , si l’élément est un vrai positif, choisissez, **faire correspondre**.</span><span class="sxs-lookup"><span data-stu-id="de570-124">In the **Detailed feedback** pane, if the item is a true positive, choose, **Match**.</span></span>  <span data-ttu-id="de570-125">S’il s’agit d’un faux positif, c’est qu’il était incorrectement inclus dans la catégorie, **ne choisira pas de correspondance**.</span><span class="sxs-lookup"><span data-stu-id="de570-125">If the item is a false positive, that is it was incorrectly included in the category, choose **Not a match**.</span></span>
4. <span data-ttu-id="de570-126">S’il existe un autre classifieur plus approprié pour l’élément, vous pouvez le sélectionner dans la liste **suggérer d’autres classifieurs de formation** .</span><span class="sxs-lookup"><span data-stu-id="de570-126">If there is another classifier that would be more appropriate for the item, you can choose it from the **Suggest other trainable classifiers** list.</span></span> <span data-ttu-id="de570-127">Cette opération déclenche l’évaluation de l’élément par l’autre classifieur.</span><span class="sxs-lookup"><span data-stu-id="de570-127">This will trigger the other classifier to evaluate the item.</span></span>

> [!TIP]
> <span data-ttu-id="de570-128">Vous pouvez envoyer vos commentaires sur plusieurs éléments simultanément en les sélectionnant, puis en choisissant **fournir des commentaires détaillés** dans la barre de commandes.</span><span class="sxs-lookup"><span data-stu-id="de570-128">You can provide feedback on multiple items simultaneously by choosing them all and then choosing **Provide detailed feedback** in the command bar.</span></span>

5. <span data-ttu-id="de570-129">Sélectionnez **Envoyer des commentaires** pour envoyer votre évaluation de `match` , `not a match` classifications et suggérer d’autres classifieurs de formation.</span><span class="sxs-lookup"><span data-stu-id="de570-129">Choose **Send feedback** to send your evaluation of the `match`, `not a match` classifications and suggest other trainable classifiers.</span></span> <span data-ttu-id="de570-130">Une fois que vous avez fourni 30 instances de commentaires à un classifieur, il est automatiquement retrainé.</span><span class="sxs-lookup"><span data-stu-id="de570-130">When you've provided 30 instances of feedback to a classifier, it will automatically  retrain.</span></span> <span data-ttu-id="de570-131">La reformation peut durer de 1-4 heures.</span><span class="sxs-lookup"><span data-stu-id="de570-131">Retraining can take from 1-4 hours.</span></span> <span data-ttu-id="de570-132">Les classifieurs ne peuvent être reformés qu’une fois par jour.</span><span class="sxs-lookup"><span data-stu-id="de570-132">Classifiers can only be retrained twice per day.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de570-133">Ces informations sont dirigées vers le classificateur de votre client, **qui ne revient pas à Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="de570-133">This information goes to the classifier in your tenant, **it does not go back to Microsoft**.</span></span>

6.  <span data-ttu-id="de570-134">Ouvrez la page **classification des données** dans le centre de **conformité Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="de570-134">Open the **Data classification** page in the **Microsoft 365 compliance center**.</span></span>
7. <span data-ttu-id="de570-135">Ouvrez les **classifieurs avec apprentissage**.</span><span class="sxs-lookup"><span data-stu-id="de570-135">Open **Trainable classifiers**.</span></span>
8. <span data-ttu-id="de570-136">Le classifieur qui a été utilisé dans votre stratégie de conformité des communications apparaît sous le titre **nouvelle formation** .</span><span class="sxs-lookup"><span data-stu-id="de570-136">The classifier that was used in your Communications compliance policy will appear under the **Re-training** heading.</span></span>

![classifieur dans l’état de la reformation](../media/classifier-retraining.png)

9. <span data-ttu-id="de570-138">Une fois la reformation terminée, sélectionnez le classifieur pour ouvrir la vue d’ensemble de la formation.</span><span class="sxs-lookup"><span data-stu-id="de570-138">Once retraining completes, choose the classifier to open the retraining overview.</span></span>

![vue d’ensemble des résultats de la formation du classifieur](../media/classifier-retraining-overview.png)

10. <span data-ttu-id="de570-140">Examinez l’action recommandée, ainsi que les comparaisons de prédiction des versions reformation et actuellement publiées du classifieur.</span><span class="sxs-lookup"><span data-stu-id="de570-140">Review the recommended action, and the prediction comparisons of the retrained and currently published versions of the classifier.</span></span>
11. <span data-ttu-id="de570-141">Si vous êtes satisfait du résultat de la nouvelle formation, choisissez **republier**.</span><span class="sxs-lookup"><span data-stu-id="de570-141">If you satisfied with the results of the retraining, choose **Re-publish**.</span></span>
12. <span data-ttu-id="de570-142">Si vous n’êtes pas satisfait du résultat de la nouvelle formation, vous pouvez choisir de fournir des commentaires supplémentaires au classifieur dans l’interface de conformité des communications et d’entamer un autre cycle de recyclage ou de ne rien faire, auquel cas la version actuellement publiée du classifieur continuera à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="de570-142">If you are not satisfied with the results of the retraining, you can choose to provide additional feedback to the classifier in the Communications compliance interface and start another retraining cycle or do nothing in which case the currently published version of the classifier will continue to be used.</span></span> 

## <a name="details-on-republishing-recommendations"></a><span data-ttu-id="de570-143">Détails sur les recommandations de republication</span><span class="sxs-lookup"><span data-stu-id="de570-143">Details on republishing recommendations</span></span>

<span data-ttu-id="de570-144">Voici quelques informations sur la formulation de la recommandation pour republier un classifieur de nouvelle formation ou suggérer une nouvelle formation.</span><span class="sxs-lookup"><span data-stu-id="de570-144">Here is a little information on how we formulate the recommendation to re-publish a retrained classifier or suggest further retraining.</span></span> <span data-ttu-id="de570-145">Cela nécessite un peu plus de compréhension de la façon dont fonctionnent les classifieurs.</span><span class="sxs-lookup"><span data-stu-id="de570-145">This requires a little deeper understanding of how trainable classifiers work.</span></span>

<span data-ttu-id="de570-146">Après un recyclage, nous évaluons les performances du classifieur sur les éléments à l’aide de commentaires, ainsi que sur les éléments initialement utilisés pour former le classifieur.</span><span class="sxs-lookup"><span data-stu-id="de570-146">After a retrain, we evaluate the classifier's performance on both the items with feedback as well as any items originally used to train the classifier.</span></span> 

- <span data-ttu-id="de570-147">Pour les modèles intégrés, les éléments utilisés pour former le classifieur sont les éléments utilisés par Microsoft pour créer le modèle.</span><span class="sxs-lookup"><span data-stu-id="de570-147">For built-in models, items used to train the classifier are the items used by Microsoft to build the model.</span></span>
- <span data-ttu-id="de570-148">Pour les modèles personnalisés, les éléments utilisés lors de la formation d’origine le classifieur proviennent des sites que vous avez ajoutés à des fins de test et de révision.</span><span class="sxs-lookup"><span data-stu-id="de570-148">For custom models, items used in the original training the classifier are from the sites you had added for test and review.</span></span>

<span data-ttu-id="de570-149">Nous comparons les numéros de performances des deux ensembles d’éléments pour le classificateur reformé et publié afin de fournir une recommandation quant à la nécessité de republier.</span><span class="sxs-lookup"><span data-stu-id="de570-149">We compare the performance numbers on both sets of items for the retrained and published classifier to provide a recommendation on whether there was improvement to republish.</span></span> 

## <a name="see-also"></a><span data-ttu-id="de570-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de570-150">See also</span></span>

- [<span data-ttu-id="de570-151">En savoir plus sur les classifieurs de formation</span><span class="sxs-lookup"><span data-stu-id="de570-151">Learn about trainable classifiers</span></span>](classifier-learn-about.md)
- [<span data-ttu-id="de570-152">Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="de570-152">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)
