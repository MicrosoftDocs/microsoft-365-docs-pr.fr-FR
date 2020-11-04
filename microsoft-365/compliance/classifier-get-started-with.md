---
title: Prise en main des classificateurs de formation (préversion)
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
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MOE150
- MET150
description: Un classificateur Microsoft 365 est un outil que vous pouvez former afin de reconnaître différents types de contenu en leur donnant des exemples à consulter. Cet article vous explique comment créer et former un classifieur personnalisé et comment le former pour améliorer la précision.
ms.openlocfilehash: f0d3659c1ee03fe69a5513f24d15b295400a24dc
ms.sourcegitcommit: 7355cc8871cde5fac6d7d6dcecc3e41e35601623
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48906345"
---
# <a name="get-started-with-trainable-classifiers-preview"></a><span data-ttu-id="9a20a-104">Prise en main des classificateurs de formation (préversion)</span><span class="sxs-lookup"><span data-stu-id="9a20a-104">Get started with trainable classifiers (preview)</span></span>

<span data-ttu-id="9a20a-105">Un classificateur Microsoft 365 pouvant être formé est un outil que vous pouvez former afin de reconnaître différents types de contenu en leur donnant des exemples à consulter.</span><span class="sxs-lookup"><span data-stu-id="9a20a-105">A Microsoft 365 trainable classifier is a tool you can train to recognize various types of content by giving it samples to look at.</span></span> <span data-ttu-id="9a20a-106">Une fois l’apprentissage effectué, vous pouvez l’utiliser pour identifier un élément pour l’application des étiquettes de sensibilité d’Office, des stratégies de conformité des communications et des stratégies d’étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="9a20a-106">Once trained, you can use it to identify item for application of Office sensitivity labels, Communications compliance policies, and retention label policies.</span></span>

<span data-ttu-id="9a20a-107">La création d’un classificateur de formation personnalisée implique d’abord de donner aux échantillons prélevés par des personnes et correspondant à la catégorie.</span><span class="sxs-lookup"><span data-stu-id="9a20a-107">Creating a custom trainable classifier first involves giving it samples that are human picked and positively match the category.</span></span> <span data-ttu-id="9a20a-108">Ensuite, une fois qu’il les a traités, vous testez la capacité des classifieurs à les prédire en leur donnant un mélange d’échantillons positifs et négatifs.</span><span class="sxs-lookup"><span data-stu-id="9a20a-108">Then, after it has processed those, you test the classifiers ability to predict by giving it a mix of positive and negative samples.</span></span> <span data-ttu-id="9a20a-109">Cet article vous explique comment créer et former un classificateur personnalisé et comment améliorer les performances des classifieurs de formation personnalisée et des classifieurs préformés pendant leur durée de formation.</span><span class="sxs-lookup"><span data-stu-id="9a20a-109">This article shows you how to create and train a custom classifier and how to improve the performance of custom trainable classifiers and pre-trained classifiers over their lifetime through retraining.</span></span>

<span data-ttu-id="9a20a-110">Pour en savoir plus sur les différents types de classifieurs, voir [en savoir plus sur les classifieurs de formation (aperçu)](classifier-learn-about.md).</span><span class="sxs-lookup"><span data-stu-id="9a20a-110">To learn more about the different types of classifiers, see [Learn about trainable classifiers (preview)](classifier-learn-about.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9a20a-111">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="9a20a-111">Prerequisites</span></span>

### <a name="licensing-requirements"></a><span data-ttu-id="9a20a-112">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="9a20a-112">Licensing requirements</span></span>

<span data-ttu-id="9a20a-113">Les classifieurs sont une fonctionnalité de conformité de Microsoft 365 E5 ou E5.</span><span class="sxs-lookup"><span data-stu-id="9a20a-113">Classifiers are a Microsoft 365 E5, or E5 Compliance feature.</span></span> <span data-ttu-id="9a20a-114">Vous devez disposer de l’un de ces abonnements pour pouvoir les utiliser.</span><span class="sxs-lookup"><span data-stu-id="9a20a-114">You must have one of these subscriptions to make use of them.</span></span>

### <a name="permissions"></a><span data-ttu-id="9a20a-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="9a20a-115">Permissions</span></span>

<span data-ttu-id="9a20a-116">Pour accéder aux classifieurs dans l’interface utilisateur :</span><span class="sxs-lookup"><span data-stu-id="9a20a-116">To access classifiers in the UI:</span></span> 

- <span data-ttu-id="9a20a-117">l’administrateur global doit s’abonner au client pour créer des classifieurs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9a20a-117">the Global admin needs to opt in for the tenant to create custom classifiers.</span></span>
- <span data-ttu-id="9a20a-118">L’administrateur de conformité ou le rôle d’enquête de données est nécessaire pour former un classifieur.</span><span class="sxs-lookup"><span data-stu-id="9a20a-118">Compliance Administrator or Data Investigation role is required to train a classifier.</span></span>

<span data-ttu-id="9a20a-119">Vous aurez besoin de comptes dotés des autorisations suivantes pour utiliser les classifieurs dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="9a20a-119">You'll need accounts with these permissions to use classifiers in these scenarios:</span></span>

- <span data-ttu-id="9a20a-120">Scénario de stratégie d’étiquette de rétention : rôles de gestion des enregistrements et de rétention</span><span class="sxs-lookup"><span data-stu-id="9a20a-120">Retention label policy scenario: Record Management and Retention Management roles</span></span> 
- <span data-ttu-id="9a20a-121">Scénario de stratégie d’étiquette de confidentialité : administrateur de sécurité, administrateur de conformité, administrateur de données de conformité</span><span class="sxs-lookup"><span data-stu-id="9a20a-121">Sensitivity label policy scenario: Security Administrator, Compliance Administrator, Compliance Data Administrator</span></span>
- <span data-ttu-id="9a20a-122">Scénario de stratégie de conformité des communications : administrateur de gestion des risques Insiders, administrateur de vérification de la surveillance</span><span class="sxs-lookup"><span data-stu-id="9a20a-122">Communication compliance policy scenario: Insider Risk Management Admin, Supervisory Review Administrator</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="9a20a-123">Par défaut, seul l’utilisateur qui crée un classifieur personnalisé peut former et examiner les prévisions effectuées par ce classifieur.</span><span class="sxs-lookup"><span data-stu-id="9a20a-123">By default, only the user who creates a custom classifier can train and review predictions made by that classifier.</span></span> <span data-ttu-id="9a20a-124">Si vous souhaitez que d’autres personnes puissent former et passer en revue les prévisions de classifieur, consultez la rubrique [accorder à d’autres personnes les droits de formation et de révision](#give-others-train-and-review-rights).</span><span class="sxs-lookup"><span data-stu-id="9a20a-124">If you want others to be able to train and review classifier predictions, see [Give others train and review rights](#give-others-train-and-review-rights).</span></span>

## <a name="prepare-for-a-custom-trainable-classifier"></a><span data-ttu-id="9a20a-125">Préparer un classificateur de formation personnalisée</span><span class="sxs-lookup"><span data-stu-id="9a20a-125">Prepare for a custom trainable classifier</span></span> 

<span data-ttu-id="9a20a-126">Il est utile de comprendre ce qui est impliqué dans la création d’un classificateur de formation personnalisée avant de vous plonger dans.</span><span class="sxs-lookup"><span data-stu-id="9a20a-126">It's helpful to understand what's involved in creating a custom trainable classifier before you dive in.</span></span> 

### <a name="timeline"></a><span data-ttu-id="9a20a-127">Chronologie</span><span class="sxs-lookup"><span data-stu-id="9a20a-127">Timeline</span></span>

<span data-ttu-id="9a20a-128">Cette chronologie reflète un exemple de déploiement de classifieur de formation.</span><span class="sxs-lookup"><span data-stu-id="9a20a-128">This timeline reflects a sample deployment of trainable classifiers.</span></span>

![formation de classifieur-chronologie](../media/trainable-classifier-deployment-timeline_border.png)

> [!TIP]
> <span data-ttu-id="9a20a-130">L’option opt-in est requise pour la première fois pour les classifieurs de formation.</span><span class="sxs-lookup"><span data-stu-id="9a20a-130">Opt-in is required the first time for trainable classifiers.</span></span> <span data-ttu-id="9a20a-131">Il faut douze jours pour que Microsoft 365 effectue une évaluation de base du contenu de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9a20a-131">It takes twelve days for Microsoft 365 to complete a baseline evaluation of your organizations content.</span></span> <span data-ttu-id="9a20a-132">Contactez votre administrateur général pour lancer le processus d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a20a-132">Contact your global administrator to kick off the opt-in process.</span></span>

### <a name="overall-workflow"></a><span data-ttu-id="9a20a-133">Flux de travail global</span><span class="sxs-lookup"><span data-stu-id="9a20a-133">Overall workflow</span></span>

<span data-ttu-id="9a20a-134">Pour en savoir plus sur le flux de travail général de création de classifieurs de formation personnalisée, consultez la rubrique [processus Flow for Creating Customer trainable Classifiers](classifier-learn-about.md#process-flow-for-creating-custom-classifiers).</span><span class="sxs-lookup"><span data-stu-id="9a20a-134">To understand more about the overall workflow of creating custom trainable classifiers, see [Process flow for creating customer trainable classifiers](classifier-learn-about.md#process-flow-for-creating-custom-classifiers).</span></span>

### <a name="seed-content"></a><span data-ttu-id="9a20a-135">Contenu de départ</span><span class="sxs-lookup"><span data-stu-id="9a20a-135">Seed content</span></span>

<span data-ttu-id="9a20a-136">Si vous souhaitez qu’un classifieur puisse identifier de manière indépendante et précise un élément comme étant dans une catégorie particulière de contenu, vous devez d’abord le présenter avec de nombreux exemples du type de contenu qui se trouve dans la catégorie.</span><span class="sxs-lookup"><span data-stu-id="9a20a-136">When you want a trainable classifier to independently and accurately identify an item as being in particular category of content, you first have to present it with many samples of the type of content that are in the category.</span></span> <span data-ttu-id="9a20a-137">Cette alimentation d’échantillons vers le classificateur peut être qualifiée d' *amorçage*.</span><span class="sxs-lookup"><span data-stu-id="9a20a-137">This feeding of samples to the trainable classifier is known as *seeding*.</span></span> <span data-ttu-id="9a20a-138">Le contenu de départ est sélectionné par un humain et est jugé pour représenter la catégorie de contenu.</span><span class="sxs-lookup"><span data-stu-id="9a20a-138">Seed content is selected by a human and is judged to represent the category of content.</span></span>

> [!TIP]
> <span data-ttu-id="9a20a-139">Vous devez avoir au moins 50 échantillons positifs et un maximum de 500.</span><span class="sxs-lookup"><span data-stu-id="9a20a-139">You need to have at least 50 positive samples and as many as 500.</span></span> <span data-ttu-id="9a20a-140">Le classificateur pouvant être mis en place traitera jusqu’à 500 exemples de création les plus récents (par date et heure de création du fichier).</span><span class="sxs-lookup"><span data-stu-id="9a20a-140">The trainable classifier will process up to the 500 most recent created samples (by file created date/time stamp).</span></span> <span data-ttu-id="9a20a-141">Plus le nombre d’exemples que vous fournissez est précis, plus les prévisions seront précises.</span><span class="sxs-lookup"><span data-stu-id="9a20a-141">The more samples you provide, the more accurate the predictions the classifier will make.</span></span>

### <a name="testing-content"></a><span data-ttu-id="9a20a-142">Test du contenu</span><span class="sxs-lookup"><span data-stu-id="9a20a-142">Testing content</span></span>

<span data-ttu-id="9a20a-143">Une fois que le classifieur peut traiter suffisamment d’échantillons positifs pour créer un modèle de prévision, vous devez tester les prévisions qu’il permet de déterminer si le classifieur peut faire la distinction entre les éléments qui correspondent à la catégorie et ceux qui ne l’ont pas.</span><span class="sxs-lookup"><span data-stu-id="9a20a-143">Once the trainable classifier has processed enough positive samples to build a prediction model, you need to test the predictions it makes to see if the classifier can correctly distinguish between items that match the category and items that don't.</span></span> <span data-ttu-id="9a20a-144">Pour ce faire, sélectionnez un autre jeu de contenu humain prélevé qui se compose d’exemples qui doivent être inclus dans la catégorie et les échantillons qui ne le seront pas.</span><span class="sxs-lookup"><span data-stu-id="9a20a-144">You do this by selecting another, hopefully larger, set of human picked content that consists of samples that should fall into the category and samples that won't.</span></span> <span data-ttu-id="9a20a-145">Vous devez tester avec des données différentes des données initiales initialement fournies.</span><span class="sxs-lookup"><span data-stu-id="9a20a-145">You should test with different data than the initial seed data you first provided.</span></span> <span data-ttu-id="9a20a-146">Une fois qu’il les traite, vous parcourez manuellement les résultats et vérifiez si chaque prévision est correcte, incorrecte ou si vous n’êtes pas sûr.</span><span class="sxs-lookup"><span data-stu-id="9a20a-146">Once it processes those, you manually go through the results and verify whether each prediction is correct, incorrect, or you aren't sure.</span></span> <span data-ttu-id="9a20a-147">Le classificateur de formation utilise ces commentaires pour améliorer son modèle de prévision.</span><span class="sxs-lookup"><span data-stu-id="9a20a-147">The trainable classifier uses this feedback to improve its prediction model.</span></span>

> [!TIP]
> <span data-ttu-id="9a20a-148">Pour obtenir de meilleurs résultats, vous devez avoir au moins 200 éléments dans votre jeu d’échantillons de test avec une répartition égale des correspondances positives et négatives.</span><span class="sxs-lookup"><span data-stu-id="9a20a-148">For best results, have at least 200 items in your test sample set with an even distribution of positive and negative matches.</span></span>

## <a name="how-to-create-a-trainable-classifier"></a><span data-ttu-id="9a20a-149">Procédure de création d’un classifieur de formation</span><span class="sxs-lookup"><span data-stu-id="9a20a-149">How to create a trainable classifier</span></span>

1. <span data-ttu-id="9a20a-150">Collect entre les éléments de contenu Seed 50-500.</span><span class="sxs-lookup"><span data-stu-id="9a20a-150">Collect between 50-500 seed content items.</span></span> <span data-ttu-id="9a20a-151">Il doit s’agir uniquement d’exemples qui représentent fortement le type de contenu que vous souhaitez que le classifieur peut identifier de manière positive comme appartenant à la catégorie de classification.</span><span class="sxs-lookup"><span data-stu-id="9a20a-151">These must be only samples that strongly represent the type of content you want the trainable classifier to positively identify as being in the classification category.</span></span> <span data-ttu-id="9a20a-152">Pour connaître les types de fichiers pris en charge, reportez-vous aux [extensions de nom de fichier et aux types de fichiers analysés par défaut dans SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) .</span><span class="sxs-lookup"><span data-stu-id="9a20a-152">See, [Default crawled file name extensions and parsed file types in SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) for the supported file types.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="9a20a-153">Les éléments de l’exemple Seed et test ne doivent pas être chiffrés et doivent être en anglais.</span><span class="sxs-lookup"><span data-stu-id="9a20a-153">The seed and test sample items must not be encrypted and they must be in English.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="9a20a-154">Assurez-vous que les éléments de votre ensemble Seed sont des exemples **forts** de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="9a20a-154">Make sure the items in your seed set are **strong** examples of the category.</span></span> <span data-ttu-id="9a20a-155">Le classificateur de formation génère initialement son modèle en fonction de ce que vous amorcez avec.</span><span class="sxs-lookup"><span data-stu-id="9a20a-155">The trainable classifier initially builds its model based on what you seed it with.</span></span> <span data-ttu-id="9a20a-156">Le classifieur part du principe que tous les échantillons de départ sont des positifs forts et n’ont aucun moyen de savoir si un échantillon est une correspondance faible ou négative avec la catégorie.</span><span class="sxs-lookup"><span data-stu-id="9a20a-156">The classifier assumes all seed samples are strong positives and has no way of knowing if a sample is a weak or negative match to the category.</span></span>

2. <span data-ttu-id="9a20a-157">Placez le contenu Seed dans un dossier SharePoint Online dédié au maintien *du contenu de l’amorçage uniquement*.</span><span class="sxs-lookup"><span data-stu-id="9a20a-157">Place the seed content in a SharePoint Online folder that is dedicated to holding *the seed content only*.</span></span> <span data-ttu-id="9a20a-158">Notez l’URL du site, de la bibliothèque et du dossier.</span><span class="sxs-lookup"><span data-stu-id="9a20a-158">Make note of the site, library, and folder URL.</span></span>

   > [!TIP]
   > <span data-ttu-id="9a20a-159">Si vous créez un nouveau site et dossier pour vos données de départ, autorisez au moins une heure pour cet emplacement à indexer avant de créer le classifieur qui utilisera ces données de départ.</span><span class="sxs-lookup"><span data-stu-id="9a20a-159">If you create a new site and folder for your seed data, allow at least an hour for that location to be indexed before creating the trainable classifier that will use that seed data.</span></span>

3. <span data-ttu-id="9a20a-160">Connectez-vous au centre de conformité Microsoft 365 avec l’accès administrateur de conformité ou au rôle d’administrateur de sécurité, puis ouvrez le **Centre de conformité Microsoft 365 ou la** classification des données du centre de **sécurité Microsoft 365**  >  **Data classification**.</span><span class="sxs-lookup"><span data-stu-id="9a20a-160">Sign in to Microsoft 365 compliance center with compliance admin or security admin role access and open **Microsoft 365 compliance center** or **Microsoft 365 security center** > **Data classification**.</span></span>

4. <span data-ttu-id="9a20a-161">Sélectionnez l’onglet **classeurs de formation** .</span><span class="sxs-lookup"><span data-stu-id="9a20a-161">Choose the **Trainable classifiers** tab.</span></span>

5. <span data-ttu-id="9a20a-162">Sélectionnez **Create Training classificateur**.</span><span class="sxs-lookup"><span data-stu-id="9a20a-162">Choose **Create trainable classifier**.</span></span>

6. <span data-ttu-id="9a20a-163">Remplissez les valeurs appropriées pour les `Name` `Description` champs et de la catégorie d’éléments que vous souhaitez que le classifieur pouvant identifier.</span><span class="sxs-lookup"><span data-stu-id="9a20a-163">Fill in appropriate values for the `Name` and `Description` fields of the category of items you want this trainable classifier to identify.</span></span>

7. <span data-ttu-id="9a20a-164">Sélectionnez l’URL du site, de la bibliothèque et du dossier SharePoint Online pour le site de contenu Seed à partir de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="9a20a-164">Pick the SharePoint Online site, library, and folder URL for the seed content site from step 2.</span></span> <span data-ttu-id="9a20a-165">Choisissez `Add` .</span><span class="sxs-lookup"><span data-stu-id="9a20a-165">Choose `Add`.</span></span>

8. <span data-ttu-id="9a20a-166">Passez en revue les paramètres, puis choisissez `Create trainable classifier` .</span><span class="sxs-lookup"><span data-stu-id="9a20a-166">Review the settings and choose `Create trainable classifier`.</span></span>

9. <span data-ttu-id="9a20a-167">Dans les 24 heures, le classificateur peut traiter les données de départ et créer un modèle de prévision.</span><span class="sxs-lookup"><span data-stu-id="9a20a-167">Within 24 hours the trainable classifier will process the seed data and build a prediction model.</span></span> <span data-ttu-id="9a20a-168">L’état du classifieur est `In progress` en cours de traitement des données de l’amorçage.</span><span class="sxs-lookup"><span data-stu-id="9a20a-168">The classifier status is `In progress` while it processes the seed data.</span></span> <span data-ttu-id="9a20a-169">Lorsque le classificateur a terminé le traitement des données de départ, l’État devient `Need test items` .</span><span class="sxs-lookup"><span data-stu-id="9a20a-169">When the classifier is finished processing the seed data, the status changes to `Need test items`.</span></span>

10. <span data-ttu-id="9a20a-170">Vous pouvez désormais afficher la page de détails en choisissant le classifieur.</span><span class="sxs-lookup"><span data-stu-id="9a20a-170">You can now view the details page by choosing the classifier.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="9a20a-171">![classificateur prêt à être testé](../media/classifier-trainable-ready-to-test-detail.png)</span><span class="sxs-lookup"><span data-stu-id="9a20a-171">![trainable classifier ready for testing](../media/classifier-trainable-ready-to-test-detail.png)</span></span>

11. <span data-ttu-id="9a20a-172">Collectez au moins 200 éléments de contenu de test (10 000 max) pour obtenir de meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="9a20a-172">Collect at least 200 test content items (10,000 max) for best results.</span></span> <span data-ttu-id="9a20a-173">Il doit s’agir d’un mélange d’éléments qui sont des positifs forts, de fortes négatifs et d’autres moins évidents dans leur nature.</span><span class="sxs-lookup"><span data-stu-id="9a20a-173">These should be a mix of items that are strong positives, strong negatives and some that are a little less obvious in their nature.</span></span> <span data-ttu-id="9a20a-174">Pour connaître les types de fichiers pris en charge, reportez-vous aux [extensions de nom de fichier et aux types de fichiers analysés par défaut dans SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) .</span><span class="sxs-lookup"><span data-stu-id="9a20a-174">See, [Default crawled file name extensions and parsed file types in SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) for the supported file types.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="9a20a-175">Les éléments de l’exemple ne doivent pas être chiffrés et doivent être en anglais.</span><span class="sxs-lookup"><span data-stu-id="9a20a-175">The sample items must not be encrypted and they must be in English.</span></span>

12. <span data-ttu-id="9a20a-176">Placez le contenu de test dans un dossier SharePoint Online dédié à la conservation *du contenu de test uniquement*.</span><span class="sxs-lookup"><span data-stu-id="9a20a-176">Place the test content in a SharePoint Online folder that is dedicated to holding *the test content only*.</span></span> <span data-ttu-id="9a20a-177">Notez le site SharePoint Online, la bibliothèque et l’URL du dossier.</span><span class="sxs-lookup"><span data-stu-id="9a20a-177">Make note of the SharePoint Online site, library, and folder URL.</span></span>

    > [!TIP]
    > <span data-ttu-id="9a20a-178">Si vous créez un nouveau site et dossier pour vos données de test, autorisez au moins une heure pour cet emplacement à indexer avant de créer le classifieur qui utilisera ces données de départ.</span><span class="sxs-lookup"><span data-stu-id="9a20a-178">If you create a new site and folder for your test data, allow at least an hour for that location to be indexed before creating the trainable classifier that will use that seed data.</span></span>

13. <span data-ttu-id="9a20a-179">Choisissez `Add items to test` .</span><span class="sxs-lookup"><span data-stu-id="9a20a-179">Choose `Add items to test`.</span></span>

14. <span data-ttu-id="9a20a-180">Sélectionnez l’URL du site, de la bibliothèque et du dossier SharePoint Online pour le site de contenu de test à partir de l’étape 12.</span><span class="sxs-lookup"><span data-stu-id="9a20a-180">Pick the SharePoint Online site, library, and folder URL for the test content site from step 12.</span></span> <span data-ttu-id="9a20a-181">Choisissez `Add` .</span><span class="sxs-lookup"><span data-stu-id="9a20a-181">Choose `Add`.</span></span>

15. <span data-ttu-id="9a20a-182">Terminez l’Assistant en sélectionnant `Done` .</span><span class="sxs-lookup"><span data-stu-id="9a20a-182">Finish the wizard by choosing `Done`.</span></span> <span data-ttu-id="9a20a-183">Votre classificateur peut prendre jusqu’à une heure pour traiter les fichiers de test.</span><span class="sxs-lookup"><span data-stu-id="9a20a-183">Your trainable classifier will take up to an hour to process the test files.</span></span>

16. <span data-ttu-id="9a20a-184">Lorsque le classificateur de formation est fini de traiter vos fichiers de test, l’État sur la page des détails prend la forme `Ready to review` .</span><span class="sxs-lookup"><span data-stu-id="9a20a-184">When the trainable classifier is done processing your test files, the status on the details page will change to `Ready to review`.</span></span> <span data-ttu-id="9a20a-185">Si vous devez augmenter la taille de l’échantillon de test, choisissez `Add items to test` et autorisez le classificateur en train de traiter les éléments supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9a20a-185">If you need to increase the test sample size, choose `Add items to test` and allow the trainable classifier to process the additional items.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="9a20a-186">![capture d’écran prêt à examiner](../media/classifier-trainable-ready-to-review-detail.png)</span><span class="sxs-lookup"><span data-stu-id="9a20a-186">![ready to review screenshot](../media/classifier-trainable-ready-to-review-detail.png)</span></span>

17. <span data-ttu-id="9a20a-187">Choisissez `Tested items to review` Tab pour passer en revue les éléments.</span><span class="sxs-lookup"><span data-stu-id="9a20a-187">Choose `Tested items to review` tab to review items.</span></span>

18. <span data-ttu-id="9a20a-188">Microsoft 365 présente 30 éléments à la fois.</span><span class="sxs-lookup"><span data-stu-id="9a20a-188">Microsoft 365 will present 30 items at a time.</span></span> <span data-ttu-id="9a20a-189">Vérifiez-les et, dans la `We predict this item is "Relevant". Do you agree?` zone, choisissez `Yes` ou `No` ou `Not sure, skip to next item` .</span><span class="sxs-lookup"><span data-stu-id="9a20a-189">Review them and in the `We predict this item is "Relevant". Do you agree?` box choose either `Yes` or `No` or `Not sure, skip to next item`.</span></span> <span data-ttu-id="9a20a-190">La précision du modèle est automatiquement mise à jour après 30 éléments.</span><span class="sxs-lookup"><span data-stu-id="9a20a-190">Model accuracy is automatically updated after every 30 items.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="9a20a-191">![zone passer en revue les éléments](../media/classifier-trainable-review-detail.png)</span><span class="sxs-lookup"><span data-stu-id="9a20a-191">![review items box](../media/classifier-trainable-review-detail.png)</span></span>

19. <span data-ttu-id="9a20a-192">Passez *en revue au moins* 200 éléments.</span><span class="sxs-lookup"><span data-stu-id="9a20a-192">Review *at least* 200 items.</span></span> <span data-ttu-id="9a20a-193">Une fois le score de précision stabilisé, l’option **publier** devient disponible et l’état du classifieur indique `Ready to use` .</span><span class="sxs-lookup"><span data-stu-id="9a20a-193">Once the accuracy score has stabilized, the **publish** option will become available and the classifier status will say `Ready to use`.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="9a20a-194">![score de précision et prêt à publier](../media/classifier-trainable-review-ready-to-publish.png)</span><span class="sxs-lookup"><span data-stu-id="9a20a-194">![accuracy score and ready to publish](../media/classifier-trainable-review-ready-to-publish.png)</span></span>

20. <span data-ttu-id="9a20a-195">Publiez le classifieur.</span><span class="sxs-lookup"><span data-stu-id="9a20a-195">Publish the classifier.</span></span>

21. <span data-ttu-id="9a20a-196">Une fois publié, votre classifieur sera disponible sous forme de condition dans [Office auto-étiquetage avec les étiquettes de confidentialité](apply-sensitivity-label-automatically.md), [appliquant automatiquement la stratégie d’étiquette de rétention en fonction d’une condition](apply-retention-labels-automatically.md#configuring-conditions-for-auto-apply-retention-labels) et de [la conformité de la communication](communication-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="9a20a-196">Once published your classifier will be available as a condition in [Office auto-labeling with sensitivity labels](apply-sensitivity-label-automatically.md), [auto-apply retention label policy based on a condition](apply-retention-labels-automatically.md#configuring-conditions-for-auto-apply-retention-labels) and in [Communication compliance](communication-compliance.md).</span></span>

## <a name="give-others-train-and-review-rights"></a><span data-ttu-id="9a20a-197">Donner aux autres les droits de formation et de révision</span><span class="sxs-lookup"><span data-stu-id="9a20a-197">Give others train and review rights</span></span>

<span data-ttu-id="9a20a-198">Utilisez cette procédure pour donner aux autres autorisations pour former, examiner et ajuster votre classificateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9a20a-198">Use this procedure to give others permissions to train, review and tune your custom trainable classifier.</span></span>  
 
1. <span data-ttu-id="9a20a-199">En tant que créateur du classifieur, un administrateur général ou un administrateur eDiscovery se connecte au centre de conformité à l’aide de PowerShell à l’aide des procédures décrites dans [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell?view=exchange-ps&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="9a20a-199">As the creator of the classifier, a global admin or eDiscovery admin connect to the Compliance center using PowerShell using the procedures in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell?view=exchange-ps&preserve-view=true).</span></span>

2. <span data-ttu-id="9a20a-200">Ensuite, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="9a20a-200">Run this command:</span></span>

   ```powershell
   Add-ComplianceCaseMember -Case "<classifier name>" -Member "<user or role group>"
   ```
   
   <span data-ttu-id="9a20a-201">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9a20a-201">For example:</span></span>
   
   `Add-ComplianceCaseMember -Case "Financial Contract Classifier" -Member johnevans@contoso.com`

   <span data-ttu-id="9a20a-202">Vous pouvez exécuter cette commande plusieurs fois pour ajouter plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9a20a-202">You can run this command multiple times to add multiple users.</span></span> <span data-ttu-id="9a20a-203">Notez que vous pouvez uniquement ajouter des groupes de rôles Exchange Online Protection (EOP) et non des groupes de rôles Azure.</span><span class="sxs-lookup"><span data-stu-id="9a20a-203">Note that you can only add Exchange Online Protection (EOP) Role Groups and not Azure Role Groups.</span></span>
