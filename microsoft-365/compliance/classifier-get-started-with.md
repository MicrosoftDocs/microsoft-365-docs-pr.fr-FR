---
title: Prise en main des classifieurs avec capacité d’apprentissage
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
description: Un classifieur Microsoft 365 est un outil que vous pouvez former pour reconnaître différents types de contenu en lui donnant des exemples à examiner. Cet article vous montre comment créer et former un classifieur personnalisé et comment les former à nouveau pour améliorer la précision.
ms.openlocfilehash: bca1de5edc3efd38f943b02091c3f47d832e6a19
ms.sourcegitcommit: 54d1a2f363b2d5b63aae258c3cec0573a08f2866
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "49752658"
---
# <a name="get-started-with-trainable-classifiers"></a><span data-ttu-id="c7a2a-104">Prise en main des classifieurs avec capacité d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="c7a2a-104">Get started with trainable classifiers</span></span>

<span data-ttu-id="c7a2a-105">Un classifieur entraidable Microsoft 365 est un outil que vous pouvez former pour reconnaître différents types de contenu en lui donnant des exemples à examiner.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-105">A Microsoft 365 trainable classifier is a tool you can train to recognize various types of content by giving it samples to look at.</span></span> <span data-ttu-id="c7a2a-106">Une fois formé, vous pouvez l’utiliser pour identifier l’élément pour l’application des étiquettes de confidentialité Office, des stratégies de conformité des communications et des stratégies d’étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-106">Once trained, you can use it to identify item for application of Office sensitivity labels, Communications compliance policies, and retention label policies.</span></span>

<span data-ttu-id="c7a2a-107">La création d’un classifieur entraisable personnalisé implique d’abord de lui donner des exemples qui sont choisis par l’homme et qui correspondent à la catégorie.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-107">Creating a custom trainable classifier first involves giving it samples that are human picked and positively match the category.</span></span> <span data-ttu-id="c7a2a-108">Ensuite, après les avoir traitées, vous testez la capacité des classifieurs à prévoir en lui donnant un mélange d’échantillons positifs et négatifs.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-108">Then, after it has processed those, you test the classifiers ability to predict by giving it a mix of positive and negative samples.</span></span> <span data-ttu-id="c7a2a-109">Cet article vous montre comment créer et former un classifieur personnalisé et comment améliorer les performances des classifieurs entraînables personnalisés et des classifieurs pré-formés tout au long de leur durée de vie via une nouvelle formation.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-109">This article shows you how to create and train a custom classifier and how to improve the performance of custom trainable classifiers and pre-trained classifiers over their lifetime through retraining.</span></span>

<span data-ttu-id="c7a2a-110">Pour en savoir plus sur les différents types de classifieurs, voir En savoir plus sur les [classifieurs entraisables.](classifier-learn-about.md)</span><span class="sxs-lookup"><span data-stu-id="c7a2a-110">To learn more about the different types of classifiers, see [Learn about trainable classifiers](classifier-learn-about.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c7a2a-111">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="c7a2a-111">Prerequisites</span></span>

### <a name="licensing-requirements"></a><span data-ttu-id="c7a2a-112">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="c7a2a-112">Licensing requirements</span></span>

<span data-ttu-id="c7a2a-113">Les classifieurs sont une fonctionnalité de conformité Microsoft 365 E5 ou E5.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-113">Classifiers are a Microsoft 365 E5, or E5 Compliance feature.</span></span> <span data-ttu-id="c7a2a-114">Vous devez avoir l’un de ces abonnements pour pouvoir les utiliser.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-114">You must have one of these subscriptions to make use of them.</span></span>

### <a name="permissions"></a><span data-ttu-id="c7a2a-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="c7a2a-115">Permissions</span></span>

<span data-ttu-id="c7a2a-116">Pour accéder aux classifieurs dans l’interface utilisateur :</span><span class="sxs-lookup"><span data-stu-id="c7a2a-116">To access classifiers in the UI:</span></span> 

- <span data-ttu-id="c7a2a-117">L’administrateur global doit choisir le client pour créer des classifieurs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-117">the Global admin needs to opt in for the tenant to create custom classifiers.</span></span>
- <span data-ttu-id="c7a2a-118">Le rôle Administrateur de conformité est requis pour former un classifieur.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-118">Compliance Administrator role is required to train a classifier.</span></span>

<span data-ttu-id="c7a2a-119">Vous aurez besoin de comptes avec ces autorisations pour utiliser des classifieurs dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="c7a2a-119">You'll need accounts with these permissions to use classifiers in these scenarios:</span></span>

- <span data-ttu-id="c7a2a-120">Scénario de stratégie d’étiquette de rétention : rôles gestion des enregistrement et gestion de la rétention</span><span class="sxs-lookup"><span data-stu-id="c7a2a-120">Retention label policy scenario: Record Management and Retention Management roles</span></span> 
- <span data-ttu-id="c7a2a-121">Scénario de stratégie d’étiquette de confidentialité : administrateur de sécurité, administrateur de conformité, administrateur de données de conformité</span><span class="sxs-lookup"><span data-stu-id="c7a2a-121">Sensitivity label policy scenario: Security Administrator, Compliance Administrator, Compliance Data Administrator</span></span>
- <span data-ttu-id="c7a2a-122">Scénario de stratégie de conformité des communications : administrateur de la gestion des risques internes, administrateur de vérification de surveillance</span><span class="sxs-lookup"><span data-stu-id="c7a2a-122">Communication compliance policy scenario: Insider Risk Management Admin, Supervisory Review Administrator</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="c7a2a-123">Par défaut, seul l’utilisateur qui crée un classifieur personnalisé peut entraîner et passer en revue les prédictions faites par ce classificateur.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-123">By default, only the user who creates a custom classifier can train and review predictions made by that classifier.</span></span>

## <a name="prepare-for-a-custom-trainable-classifier"></a><span data-ttu-id="c7a2a-124">Préparer un classifieur entraisable personnalisé</span><span class="sxs-lookup"><span data-stu-id="c7a2a-124">Prepare for a custom trainable classifier</span></span> 

<span data-ttu-id="c7a2a-125">Il est utile de comprendre ce qui est impliqué dans la création d’un classifieur entraisable personnalisé avant de vous plonger.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-125">It's helpful to understand what's involved in creating a custom trainable classifier before you dive in.</span></span> 

### <a name="timeline"></a><span data-ttu-id="c7a2a-126">Chronologie</span><span class="sxs-lookup"><span data-stu-id="c7a2a-126">Timeline</span></span>

<span data-ttu-id="c7a2a-127">Cette chronologie reflète un exemple de déploiement de classifieurs entraisables.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-127">This timeline reflects a sample deployment of trainable classifiers.</span></span>

![trainable-classifier-timeline](../media/trainable-classifier-deployment-timeline_border.png)

> [!TIP]
> <span data-ttu-id="c7a2a-129">L’option d’opt-in est requise la première fois pour les classifieurs entraisables.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-129">Opt-in is required the first time for trainable classifiers.</span></span> <span data-ttu-id="c7a2a-130">Il faut douze jours pour que Microsoft 365 termine une évaluation de référence du contenu de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-130">It takes twelve days for Microsoft 365 to complete a baseline evaluation of your organizations content.</span></span> <span data-ttu-id="c7a2a-131">Contactez votre administrateur général pour lancer le processus d’opt-in.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-131">Contact your global administrator to kick off the opt-in process.</span></span>

### <a name="overall-workflow"></a><span data-ttu-id="c7a2a-132">Flux de travail global</span><span class="sxs-lookup"><span data-stu-id="c7a2a-132">Overall workflow</span></span>

<span data-ttu-id="c7a2a-133">Pour en savoir plus sur le flux de travail global de création de classifieurs entra nessables personnalisés, voir Flux de processus pour la création de [classifieurs entra mentables par le client.](classifier-learn-about.md#process-flow-for-creating-custom-classifiers)</span><span class="sxs-lookup"><span data-stu-id="c7a2a-133">To understand more about the overall workflow of creating custom trainable classifiers, see [Process flow for creating customer trainable classifiers](classifier-learn-about.md#process-flow-for-creating-custom-classifiers).</span></span>

### <a name="seed-content"></a><span data-ttu-id="c7a2a-134">Contenu d’amorçage</span><span class="sxs-lookup"><span data-stu-id="c7a2a-134">Seed content</span></span>

<span data-ttu-id="c7a2a-135">Lorsque vous souhaitez qu’un classifieur entraisable identifie de manière indépendante et précise un élément comme étant dans une catégorie particulière de contenu, vous devez d’abord le présenter avec de nombreux exemples du type de contenu de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-135">When you want a trainable classifier to independently and accurately identify an item as being in particular category of content, you first have to present it with many samples of the type of content that are in the category.</span></span> <span data-ttu-id="c7a2a-136">Cet amorçage d’échantillons au classifieur entraçable est appelé *amorçage.*</span><span class="sxs-lookup"><span data-stu-id="c7a2a-136">This feeding of samples to the trainable classifier is known as *seeding*.</span></span> <span data-ttu-id="c7a2a-137">Le contenu de amorçage est sélectionné par un humain et est jugé pour représenter la catégorie de contenu.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-137">Seed content is selected by a human and is judged to represent the category of content.</span></span>

> [!TIP]
> <span data-ttu-id="c7a2a-138">Vous devez avoir au moins 50 échantillons positifs et jusqu’à 500.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-138">You need to have at least 50 positive samples and as many as 500.</span></span> <span data-ttu-id="c7a2a-139">Le classificateur entraçable traitera jusqu’aux 500 exemples créés les plus récents (par date/horodateur de création de fichier).</span><span class="sxs-lookup"><span data-stu-id="c7a2a-139">The trainable classifier will process up to the 500 most recent created samples (by file created date/time stamp).</span></span> <span data-ttu-id="c7a2a-140">Plus vous fournissez d’exemples, plus les prédictions du classifieur seront précises.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-140">The more samples you provide, the more accurate the predictions the classifier will make.</span></span>

### <a name="testing-content"></a><span data-ttu-id="c7a2a-141">Test du contenu</span><span class="sxs-lookup"><span data-stu-id="c7a2a-141">Testing content</span></span>

<span data-ttu-id="c7a2a-142">Une fois que le classificateur entraçable a traitée suffisamment d’échantillons positifs pour créer un modèle de prédiction, vous devez tester les prédictions qu’il effectue pour voir si le classificateur peut correctement faire la distinction entre les éléments qui correspondent à la catégorie et les éléments qui ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-142">Once the trainable classifier has processed enough positive samples to build a prediction model, you need to test the predictions it makes to see if the classifier can correctly distinguish between items that match the category and items that don't.</span></span> <span data-ttu-id="c7a2a-143">Pour ce faire, vous sélectionnez un autre ensemble de contenu sélectionné par l’être humain, avec un plus grand nombre d’échantillons qui doivent être placés dans la catégorie, et des exemples qui ne le seront pas.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-143">You do this by selecting another, hopefully larger, set of human picked content that consists of samples that should fall into the category and samples that won't.</span></span> <span data-ttu-id="c7a2a-144">Vous devez tester avec des données différentes des données initiales initiales que vous avez fournies.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-144">You should test with different data than the initial seed data you first provided.</span></span> <span data-ttu-id="c7a2a-145">Une fois qu’il les traite, vous allez manuellement à travers les résultats et vérifiez si chaque prédiction est correcte, incorrecte ou vous n’êtes pas sûr.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-145">Once it processes those, you manually go through the results and verify whether each prediction is correct, incorrect, or you aren't sure.</span></span> <span data-ttu-id="c7a2a-146">Le classifieur entraisable utilise ce retour d’expérience pour améliorer son modèle de prédiction.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-146">The trainable classifier uses this feedback to improve its prediction model.</span></span>

> [!TIP]
> <span data-ttu-id="c7a2a-147">Pour obtenir de meilleurs résultats, vous devez avoir au moins 200 éléments dans votre exemple de test avec une distribution équitable de correspondances positives et négatives.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-147">For best results, have at least 200 items in your test sample set with an even distribution of positive and negative matches.</span></span>

## <a name="how-to-create-a-trainable-classifier"></a><span data-ttu-id="c7a2a-148">Comment créer un classifieur entra nementable</span><span class="sxs-lookup"><span data-stu-id="c7a2a-148">How to create a trainable classifier</span></span>

1. <span data-ttu-id="c7a2a-149">Collectez entre 50 et 500 éléments de contenu d’amorçage.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-149">Collect between 50-500 seed content items.</span></span> <span data-ttu-id="c7a2a-150">Il doit s’agit uniquement d’exemples qui représentent fortement le type de contenu que le classifieur entraçable doit identifier comme étant dans la catégorie de classification.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-150">These must be only samples that strongly represent the type of content you want the trainable classifier to positively identify as being in the classification category.</span></span> <span data-ttu-id="c7a2a-151">Voir, [Extensions de nom](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) de fichier et types de fichiers analyse par défaut dans SharePoint Server pour les types de fichiers pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-151">See, [Default crawled file name extensions and parsed file types in SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) for the supported file types.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="c7a2a-152">Les exemples d’amorçage et de test ne doivent pas être chiffrés et doivent être en anglais.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-152">The seed and test sample items must not be encrypted and they must be in English.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="c7a2a-153">Assurez-vous que les éléments de votre ensemble de valeurs de amorçage **sont de forts** exemples de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-153">Make sure the items in your seed set are **strong** examples of the category.</span></span> <span data-ttu-id="c7a2a-154">Le classifieur entraçable crée initialement son modèle en fonction de ce avec quoi vous l’amorçez.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-154">The trainable classifier initially builds its model based on what you seed it with.</span></span> <span data-ttu-id="c7a2a-155">Le classificateur suppose que tous les échantillons de amorçage sont des positifs forts et n’a aucun moyen de savoir si un échantillon est une correspondance faible ou négative avec la catégorie.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-155">The classifier assumes all seed samples are strong positives and has no way of knowing if a sample is a weak or negative match to the category.</span></span>

2. <span data-ttu-id="c7a2a-156">Placez le contenu d’amorçage dans un dossier SharePoint Online dédié à la mise en place du *contenu d’amorçage uniquement.*</span><span class="sxs-lookup"><span data-stu-id="c7a2a-156">Place the seed content in a SharePoint Online folder that is dedicated to holding *the seed content only*.</span></span> <span data-ttu-id="c7a2a-157">Notez l’URL du site, de la bibliothèque et du dossier.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-157">Make note of the site, library, and folder URL.</span></span>

   > [!TIP]
   > <span data-ttu-id="c7a2a-158">Si vous créez un site et un dossier pour vos données d’amorçage, autorisez l’indexation d’au moins une heure de cet emplacement avant de créer le classifieur entraisable qui utilisera ces données d’amorçage.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-158">If you create a new site and folder for your seed data, allow at least an hour for that location to be indexed before creating the trainable classifier that will use that seed data.</span></span>

3. <span data-ttu-id="c7a2a-159">Connectez-vous au Centre de conformité Microsoft 365 avec l’accès au rôle d’administrateur de conformité ou d’administrateur de sécurité et ouvrez le Centre de conformité **Microsoft 365** ou la classification des données du Centre de sécurité **Microsoft 365.**  >  </span><span class="sxs-lookup"><span data-stu-id="c7a2a-159">Sign in to Microsoft 365 compliance center with compliance admin or security admin role access and open **Microsoft 365 compliance center** or **Microsoft 365 security center** > **Data classification**.</span></span>

4. <span data-ttu-id="c7a2a-160">Sélectionnez **l’onglet Classifieurs avec formation.**</span><span class="sxs-lookup"><span data-stu-id="c7a2a-160">Choose the **Trainable classifiers** tab.</span></span>

5. <span data-ttu-id="c7a2a-161">Choose **Create trainable classifier**.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-161">Choose **Create trainable classifier**.</span></span>

6. <span data-ttu-id="c7a2a-162">Remplissez les valeurs appropriées pour les champs de la catégorie d’éléments que ce `Name` `Description` classifieur entraçable doit identifier.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-162">Fill in appropriate values for the `Name` and `Description` fields of the category of items you want this trainable classifier to identify.</span></span>

7. <span data-ttu-id="c7a2a-163">Choisissez l’URL du site, de la bibliothèque et du dossier SharePoint Online pour le site de contenu d’amorçage à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-163">Pick the SharePoint Online site, library, and folder URL for the seed content site from step 2.</span></span> <span data-ttu-id="c7a2a-164">Choose `Add` .</span><span class="sxs-lookup"><span data-stu-id="c7a2a-164">Choose `Add`.</span></span>

8. <span data-ttu-id="c7a2a-165">Examinez les paramètres et choisissez `Create trainable classifier` .</span><span class="sxs-lookup"><span data-stu-id="c7a2a-165">Review the settings and choose `Create trainable classifier`.</span></span>

9. <span data-ttu-id="c7a2a-166">Dans un délai de 24 heures, le classifieur entraçable traitera les données d’amorçage et créera un modèle de prédiction.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-166">Within 24 hours the trainable classifier will process the seed data and build a prediction model.</span></span> <span data-ttu-id="c7a2a-167">L’état du classificateur est `In progress` pendant qu’il traite les données d’amorçage.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-167">The classifier status is `In progress` while it processes the seed data.</span></span> <span data-ttu-id="c7a2a-168">Lorsque le classificateur a terminé le traitement des données de amorçage, l’état change en `Need test items` .</span><span class="sxs-lookup"><span data-stu-id="c7a2a-168">When the classifier is finished processing the seed data, the status changes to `Need test items`.</span></span>

10. <span data-ttu-id="c7a2a-169">Vous pouvez désormais afficher la page de détails en choisissant le classificateur.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-169">You can now view the details page by choosing the classifier.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="c7a2a-170">![Classifieur entraisable prêt pour le test](../media/classifier-trainable-ready-to-test-detail.png)</span><span class="sxs-lookup"><span data-stu-id="c7a2a-170">![trainable classifier ready for testing](../media/classifier-trainable-ready-to-test-detail.png)</span></span>

11. <span data-ttu-id="c7a2a-171">Collectez au moins 200 éléments de contenu de test (10 000 max) pour obtenir de meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-171">Collect at least 200 test content items (10,000 max) for best results.</span></span> <span data-ttu-id="c7a2a-172">Il doit s’agit d’un mélange d’éléments qui sont de forts positifs, de négatifs forts et d’autres qui sont un peu moins évidents dans leur nature.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-172">These should be a mix of items that are strong positives, strong negatives and some that are a little less obvious in their nature.</span></span> <span data-ttu-id="c7a2a-173">Voir, [Extensions de nom](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) de fichier et types de fichiers analyse par défaut dans SharePoint Server pour les types de fichiers pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-173">See, [Default crawled file name extensions and parsed file types in SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) for the supported file types.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c7a2a-174">Les exemples d’éléments ne doivent pas être chiffrés et doivent être en anglais.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-174">The sample items must not be encrypted and they must be in English.</span></span>

12. <span data-ttu-id="c7a2a-175">Placez le contenu de test dans un dossier SharePoint Online dédié à la mise en place du *contenu de test uniquement.*</span><span class="sxs-lookup"><span data-stu-id="c7a2a-175">Place the test content in a SharePoint Online folder that is dedicated to holding *the test content only*.</span></span> <span data-ttu-id="c7a2a-176">Notez l’URL du site, de la bibliothèque et du dossier SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-176">Make note of the SharePoint Online site, library, and folder URL.</span></span>

    > [!TIP]
    > <span data-ttu-id="c7a2a-177">Si vous créez un site et un dossier pour vos données de test, autorisez l’indexation d’au moins une heure de cet emplacement avant de créer le classifieur entraisable qui utilisera ces données d’amorçage.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-177">If you create a new site and folder for your test data, allow at least an hour for that location to be indexed before creating the trainable classifier that will use that seed data.</span></span>

13. <span data-ttu-id="c7a2a-178">Choose `Add items to test` .</span><span class="sxs-lookup"><span data-stu-id="c7a2a-178">Choose `Add items to test`.</span></span>

14. <span data-ttu-id="c7a2a-179">Choisissez l’URL du site, de la bibliothèque et du dossier SharePoint Online pour le site de contenu de test à l’étape 12.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-179">Pick the SharePoint Online site, library, and folder URL for the test content site from step 12.</span></span> <span data-ttu-id="c7a2a-180">Choose `Add` .</span><span class="sxs-lookup"><span data-stu-id="c7a2a-180">Choose `Add`.</span></span>

15. <span data-ttu-id="c7a2a-181">Terminez l’Assistant en choisissant `Done` .</span><span class="sxs-lookup"><span data-stu-id="c7a2a-181">Finish the wizard by choosing `Done`.</span></span> <span data-ttu-id="c7a2a-182">Le traitement des fichiers de test peut prendre jusqu’à une heure.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-182">Your trainable classifier will take up to an hour to process the test files.</span></span>

16. <span data-ttu-id="c7a2a-183">Lorsque le classifieur entra vous permet de traiter vos fichiers de test, l’état sur la page de détails passe à `Ready to review` .</span><span class="sxs-lookup"><span data-stu-id="c7a2a-183">When the trainable classifier is done processing your test files, the status on the details page will change to `Ready to review`.</span></span> <span data-ttu-id="c7a2a-184">Si vous devez augmenter la taille de l’échantillon de test, choisissez et autorisez le `Add items to test` classifieur entraçable à traiter les éléments supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-184">If you need to increase the test sample size, choose `Add items to test` and allow the trainable classifier to process the additional items.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="c7a2a-185">![Capture d’écran prête à être revue](../media/classifier-trainable-ready-to-review-detail.png)</span><span class="sxs-lookup"><span data-stu-id="c7a2a-185">![ready to review screenshot](../media/classifier-trainable-ready-to-review-detail.png)</span></span>

17. <span data-ttu-id="c7a2a-186">Choisissez `Tested items to review` l’onglet pour passer en revue les éléments.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-186">Choose `Tested items to review` tab to review items.</span></span>

18. <span data-ttu-id="c7a2a-187">Microsoft 365 présente 30 éléments à la fois.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-187">Microsoft 365 will present 30 items at a time.</span></span> <span data-ttu-id="c7a2a-188">Examinez-les et dans la `We predict this item is "Relevant". Do you agree?` zone choisissez soit ou `Yes` `No` `Not sure, skip to next item` .</span><span class="sxs-lookup"><span data-stu-id="c7a2a-188">Review them and in the `We predict this item is "Relevant". Do you agree?` box choose either `Yes` or `No` or `Not sure, skip to next item`.</span></span> <span data-ttu-id="c7a2a-189">La précision du modèle est automatiquement mise à jour après 30 éléments.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-189">Model accuracy is automatically updated after every 30 items.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="c7a2a-190">![zone d’avis sur les éléments](../media/classifier-trainable-review-detail.png)</span><span class="sxs-lookup"><span data-stu-id="c7a2a-190">![review items box](../media/classifier-trainable-review-detail.png)</span></span>

19. <span data-ttu-id="c7a2a-191">Passer *en revue au moins* 200 éléments.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-191">Review *at least* 200 items.</span></span> <span data-ttu-id="c7a2a-192">Une fois que le score  de précision s’est stabilisé, l’option de publication devient disponible et l’état du classificateur le dit `Ready to use` .</span><span class="sxs-lookup"><span data-stu-id="c7a2a-192">Once the accuracy score has stabilized, the **publish** option will become available and the classifier status will say `Ready to use`.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="c7a2a-193">![score de précision et prêt à être publié](../media/classifier-trainable-review-ready-to-publish.png)</span><span class="sxs-lookup"><span data-stu-id="c7a2a-193">![accuracy score and ready to publish](../media/classifier-trainable-review-ready-to-publish.png)</span></span>

20. <span data-ttu-id="c7a2a-194">Publiez le classifieur.</span><span class="sxs-lookup"><span data-stu-id="c7a2a-194">Publish the classifier.</span></span>

21. <span data-ttu-id="c7a2a-195">Une fois publié, votre classificateur sera disponible en tant que condition dans l’étiquetage automatique [d’Office](apply-sensitivity-label-automatically.md)avec des étiquettes de confidentialité , appliquer automatiquement la stratégie d’étiquette de rétention basée sur une [condition](apply-retention-labels-automatically.md#configuring-conditions-for-auto-apply-retention-labels) et dans la conformité des [communications](communication-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="c7a2a-195">Once published your classifier will be available as a condition in [Office auto-labeling with sensitivity labels](apply-sensitivity-label-automatically.md), [auto-apply retention label policy based on a condition](apply-retention-labels-automatically.md#configuring-conditions-for-auto-apply-retention-labels) and in [Communication compliance](communication-compliance.md).</span></span>
