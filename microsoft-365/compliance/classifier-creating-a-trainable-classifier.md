---
title: Créer un classifieur de formation (aperçu)
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Utilisez des classifieurs adaptés lorsque l’un des classifieurs de zone prêt à l’emploi ne répond pas à vos besoins. Un classificateur Microsoft 365 est un outil que vous pouvez former afin de reconnaître différents types de contenu en leur donnant des exemples à consulter. Cette rubrique vous montre comment créer un classifieur personnalisé.
ms.openlocfilehash: cb3cda9777d692a56263e92cd908eb09bfa99895
ms.sourcegitcommit: 8fda7852b2a5baa92b8a365865b014ea6d100bbc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/03/2019
ms.locfileid: "39813372"
---
# <a name="creating-a-trainable-classifier-preview"></a><span data-ttu-id="17f11-105">Création d’un classifieur de formation (aperçu)</span><span class="sxs-lookup"><span data-stu-id="17f11-105">Creating a trainable classifier (preview)</span></span>

<span data-ttu-id="17f11-106">Utilisez des classifieurs adaptés lorsque l’un des classifieurs de la zone ne répond pas à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="17f11-106">Use trainable classifiers when one of the out of the box classifiers won't meet your needs.</span></span> <span data-ttu-id="17f11-107">Un classificateur Microsoft 365 est un outil que vous pouvez former afin de reconnaître différents types de contenu en leur donnant des exemples à consulter.</span><span class="sxs-lookup"><span data-stu-id="17f11-107">A Microsoft 365 classifier is a tool you can train to recognize various types of content by giving it samples to look at.</span></span> <span data-ttu-id="17f11-108">Formation le classificateur implique d’abord de donner aux échantillons prélevés par des personnes et correspondant à la catégorie positive.</span><span class="sxs-lookup"><span data-stu-id="17f11-108">Training the classifier involves first giving it samples that are human picked and positively match the category.</span></span> <span data-ttu-id="17f11-109">Ensuite, une fois qu’il les a traités, vous testez les prévisions en lui donnant un mélange d’échantillons positifs et négatifs.</span><span class="sxs-lookup"><span data-stu-id="17f11-109">Then, after it has processed those, you test the predictions by giving it a mix of positive and negative samples.</span></span>

<span data-ttu-id="17f11-110">Pour en savoir plus sur les différents types de classifieurs, voir [Getting Started with trainable Classifiers (Preview)](classifier-getting-started-with.md)</span><span class="sxs-lookup"><span data-stu-id="17f11-110">To learn more about the different types of classifiers, see [Getting started with trainable classifiers (preview)](classifier-getting-started-with.md)</span></span>

<span data-ttu-id="17f11-111">Cette chronologie reflète un exemple de déploiement.</span><span class="sxs-lookup"><span data-stu-id="17f11-111">This timeline reflects a sample deployment.</span></span>

![formation de classifieur-chronologie](media/trainable-classifier-deployment-timeline_border.png)

> [!TIP]
> <span data-ttu-id="17f11-113">L’option opt-in est requise pour la première fois pour les classifieurs de formation.</span><span class="sxs-lookup"><span data-stu-id="17f11-113">Opt-in is required the first time for trainable classifiers.</span></span> <span data-ttu-id="17f11-114">Il faut douze jours pour que Microsoft 365 effectue une évaluation de base du contenu de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="17f11-114">It takes twelve days for Microsoft 365 to complete a baseline evaluation of your organizations content.</span></span>

## <a name="seed-content"></a><span data-ttu-id="17f11-115">Contenu de départ</span><span class="sxs-lookup"><span data-stu-id="17f11-115">Seed content</span></span>

<span data-ttu-id="17f11-116">Si vous souhaitez qu’un classifieur puisse identifier de manière indépendante et précise un élément comme étant dans une catégorie particulière de contenu, vous devez d’abord le présenter avec de nombreux exemples du type de contenu qui se trouve dans la catégorie.</span><span class="sxs-lookup"><span data-stu-id="17f11-116">When you want a trainable classifier to independently and accurately identify an item as being in particular category of content, you first have to present it with many samples of the type of content that are in the category.</span></span> <span data-ttu-id="17f11-117">Cette alimentation d’échantillons vers le classificateur peut être qualifiée d' *amorçage*.</span><span class="sxs-lookup"><span data-stu-id="17f11-117">This feeding of samples to the trainable classifier is known as *seeding*.</span></span> <span data-ttu-id="17f11-118">Le contenu de départ est sélectionné par un humain et est jugé pour représenter la catégorie de contenu.</span><span class="sxs-lookup"><span data-stu-id="17f11-118">Seed content is selected by a human and is judged to represent the category of content.</span></span>

> [!TIP]
> <span data-ttu-id="17f11-119">Vous devez avoir au moins 50 échantillons positifs et un maximum de 500.</span><span class="sxs-lookup"><span data-stu-id="17f11-119">You need to have at least 50 positive samples and as many as 500.</span></span> <span data-ttu-id="17f11-120">Le classificateur pouvant être mis en place traitera jusqu’à 500 exemples de création les plus récents (par date et heure de création du fichier).</span><span class="sxs-lookup"><span data-stu-id="17f11-120">The trainable classifier will process up to the 500 most recent created samples (by file created date/time stamp).</span></span> <span data-ttu-id="17f11-121">Plus le nombre d’exemples que vous fournissez est précis, plus les prévisions seront précises.</span><span class="sxs-lookup"><span data-stu-id="17f11-121">The more samples you provide, the more accurate the predictions the classifier will make.</span></span>

## <a name="testing-content"></a><span data-ttu-id="17f11-122">Test du contenu</span><span class="sxs-lookup"><span data-stu-id="17f11-122">Testing content</span></span>

<span data-ttu-id="17f11-123">Une fois que le classifieur peut traiter suffisamment d’échantillons positifs pour créer un modèle de prévision, vous devez tester les prévisions qu’il permet de déterminer si le classifieur peut faire la distinction entre les éléments qui correspondent à la catégorie et ceux qui ne l’ont pas.</span><span class="sxs-lookup"><span data-stu-id="17f11-123">Once the trainable classifier has processed enough positive samples to build a prediction model, you need to test the predictions it makes to see if the classifier can correctly distinguish between items that match the category and items that don't.</span></span> <span data-ttu-id="17f11-124">Pour ce faire, vous devez l’alimenter un autre ensemble de contenu choisi par l’homme qui se compose d’exemples qui doivent être inclus dans la catégorie et les échantillons qui ne le seront pas.</span><span class="sxs-lookup"><span data-stu-id="17f11-124">You do this by feeding it another, hopefully larger, set of human picked content that consists of samples that should fall into the category and samples that won't.</span></span> <span data-ttu-id="17f11-125">Une fois qu’il les traite, vous parcourez manuellement les résultats et vérifiez si chaque prévision est correcte, incorrecte ou si vous n’êtes pas sûr.</span><span class="sxs-lookup"><span data-stu-id="17f11-125">Once it processes those, you manually go through the results and verify whether each prediction is correct, incorrect, or you aren't sure.</span></span> <span data-ttu-id="17f11-126">Le classificateur de formation utilise ces commentaires pour améliorer son modèle de prévision.</span><span class="sxs-lookup"><span data-stu-id="17f11-126">The trainable classifier uses this feedback to improve its prediction model.</span></span>

> [!TIP]
> <span data-ttu-id="17f11-127">Pour obtenir de meilleurs résultats, comportez 10 000 éléments dans votre jeu d’échantillons de test avec une répartition égale des correspondances positives et négatives.</span><span class="sxs-lookup"><span data-stu-id="17f11-127">For best results, have 10,000 items in your test sample set with an even distribution of positive and negative matches.</span></span>

## <a name="how-to-create-a-trainable-classifier"></a><span data-ttu-id="17f11-128">Procédure de création d’un classifieur de formation</span><span class="sxs-lookup"><span data-stu-id="17f11-128">How to create a trainable classifier</span></span>

1. <span data-ttu-id="17f11-129">Collect entre les éléments de contenu Seed 50-500.</span><span class="sxs-lookup"><span data-stu-id="17f11-129">Collect between 50-500 seed content items.</span></span> <span data-ttu-id="17f11-130">Il doit s’agir uniquement d’exemples qui représentent fortement le type de contenu que vous souhaitez que le classifieur peut identifier de manière positive comme appartenant à la catégorie de classification.</span><span class="sxs-lookup"><span data-stu-id="17f11-130">These must be only samples that strongly represent the type of content you want the trainable classifier to positively identify as being in the classification category.</span></span> <span data-ttu-id="17f11-131">Pour connaître les types de fichiers pris en charge, reportez-vous aux [extensions de nom de fichier et aux types de fichiers analysés par défaut dans SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) .</span><span class="sxs-lookup"><span data-stu-id="17f11-131">See, [Default crawled file name extensions and parsed file types in SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) for the supported file types.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17f11-132">Les éléments de l’exemple Seed et test ne doivent pas être chiffrés et doivent être en anglais.</span><span class="sxs-lookup"><span data-stu-id="17f11-132">The seed and test sample items must not be encrypted and they must be in English.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17f11-133">Assurez-vous que les éléments de votre ensemble Seed sont des exemples **forts** de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="17f11-133">Make sure the items in your seed set are **strong** examples of the category.</span></span> <span data-ttu-id="17f11-134">Le classificateur de formation génère initialement son modèle en fonction de ce que vous amorcez avec.</span><span class="sxs-lookup"><span data-stu-id="17f11-134">The trainable classifier initially builds its model based on what you seed it with.</span></span> <span data-ttu-id="17f11-135">Le classifieur part du principe que tous les échantillons de départ sont des positifs forts et n’ont aucun moyen de savoir si un échantillon est une correspondance faible ou négative avec la catégorie.</span><span class="sxs-lookup"><span data-stu-id="17f11-135">The classifier assumes all seed samples are strong positives and has no way of knowing if a sample is a weak or negative match to the category.</span></span>

2. <span data-ttu-id="17f11-136">Placez le contenu Seed dans un dossier SharePoint Online dédié au maintien *du contenu de l’amorçage uniquement*.</span><span class="sxs-lookup"><span data-stu-id="17f11-136">Place the seed content in a SharePoint Online folder that is dedicated to holding *the seed content only*.</span></span> <span data-ttu-id="17f11-137">Notez l’URL du site, de la bibliothèque et du dossier.</span><span class="sxs-lookup"><span data-stu-id="17f11-137">Make note of the site, library, and folder URL.</span></span>

> [!TIP]
> <span data-ttu-id="17f11-138">Si vous créez un nouveau site et dossier pour vos données de départ, autorisez au moins une heure pour cet emplacement à indexer avant de créer le classifieur qui utilisera ces données de départ.</span><span class="sxs-lookup"><span data-stu-id="17f11-138">If you create a new site and folder for your seed data, allow at least an hour for that location to be indexed before creating the trainable classifier that will use that seed data.</span></span>

3. <span data-ttu-id="17f11-139">Connectez-vous au centre de conformité Microsoft 365 avec l’administrateur de conformité ou l’accès au rôle d’administrateur de sécurité et ouvrez le **Centre de conformité Microsoft 365 ou la** classification des**données** du centre > de **sécurité Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="17f11-139">Sign in to Microsoft 365 compliance center with compliance admin or security admin role access and open **Microsoft 365 compliance center** or **Microsoft 365 security center** > **Data classification**</span></span>

4. <span data-ttu-id="17f11-140">Sélectionnez l’onglet **classeurs de formation** .</span><span class="sxs-lookup"><span data-stu-id="17f11-140">Choose the **Trainable classifiers** tab.</span></span>

5. <span data-ttu-id="17f11-141">Sélectionnez **Create Training classificateur**.</span><span class="sxs-lookup"><span data-stu-id="17f11-141">Choose **Create trainable classifier**.</span></span>

6. <span data-ttu-id="17f11-142">Renseignez les valeurs appropriées pour `Name`les `Description` champs de la catégorie d’éléments que vous souhaitez que le classifieur pouvant identifier.</span><span class="sxs-lookup"><span data-stu-id="17f11-142">Fill in appropriate values for the `Name`, and `Description` fields of the category of items you want this trainable classifier to identify.</span></span>

7. <span data-ttu-id="17f11-143">Entrez l’URL du site, de la bibliothèque et du dossier SharePoint Online exactes pour le site de contenu Seed à partir de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="17f11-143">Enter the exact SharePoint Online site, library, and folder URL for the seed content site from step 2.</span></span> <span data-ttu-id="17f11-144">Choisissez `Add`.</span><span class="sxs-lookup"><span data-stu-id="17f11-144">Choose `Add`.</span></span>

8. <span data-ttu-id="17f11-145">Passez en revue les paramètres `Create trainable classifier`, puis choisissez.</span><span class="sxs-lookup"><span data-stu-id="17f11-145">Review the settings and choose `Create trainable classifier`.</span></span>

9. <span data-ttu-id="17f11-146">Dans les 24 heures, le classificateur peut traiter les données de départ et créer un modèle de prévision.</span><span class="sxs-lookup"><span data-stu-id="17f11-146">Within 24 hours the trainable classifier will process the seed data and build a prediction model.</span></span> <span data-ttu-id="17f11-147">L’état du classifieur est `In progress` en cours de traitement des données de l’amorçage.</span><span class="sxs-lookup"><span data-stu-id="17f11-147">The classifier status is `In progress` while it processes the seed data.</span></span> <span data-ttu-id="17f11-148">Lorsque le classificateur a terminé le traitement des données de départ, l’état `Need test items`devient.</span><span class="sxs-lookup"><span data-stu-id="17f11-148">When the classifier is finished processing the seed data, the status changes to `Need test items`.</span></span>

10. <span data-ttu-id="17f11-149">Vous pouvez désormais afficher la page de détails en choisissant le classifieur.</span><span class="sxs-lookup"><span data-stu-id="17f11-149">You can now view the details page by choosing the classifier.</span></span>


![classificateur prêt à être testé](media/classifier-trainable-ready-to-test-detail.png)

11. <span data-ttu-id="17f11-151">Collectez au moins 200 éléments de contenu de test.</span><span class="sxs-lookup"><span data-stu-id="17f11-151">Collect at least 200 test content items.</span></span> <span data-ttu-id="17f11-152">Microsoft recommande 10 000 pour obtenir de meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="17f11-152">Microsoft recommends 10,000 for best results.</span></span> <span data-ttu-id="17f11-153">Il doit s’agir d’un mélange d’éléments qui sont des positifs forts, de fortes négatifs et d’autres moins évidents dans leur nature.</span><span class="sxs-lookup"><span data-stu-id="17f11-153">These should be a mix of items that are strong positives, strong negatives and some that are a little less obvious in their nature.</span></span> <span data-ttu-id="17f11-154">Pour connaître les types de fichiers pris en charge, reportez-vous aux [extensions de nom de fichier et aux types de fichiers analysés par défaut dans SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) .</span><span class="sxs-lookup"><span data-stu-id="17f11-154">See, [Default crawled file name extensions and parsed file types in SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) for the supported file types.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17f11-155">Les éléments de l’exemple ne doivent pas être chiffrés et doivent être en anglais.</span><span class="sxs-lookup"><span data-stu-id="17f11-155">The sample items must not be encrypted and they must be in English.</span></span>

12. <span data-ttu-id="17f11-156">Placez le contenu de test dans un dossier SharePoint Online dédié à la conservation *du contenu de test uniquement*.</span><span class="sxs-lookup"><span data-stu-id="17f11-156">Place the test content in a SharePoint Online folder that is dedicated to holding *the test content only*.</span></span> <span data-ttu-id="17f11-157">Notez le site SharePoint Online, la bibliothèque et l’URL du dossier.</span><span class="sxs-lookup"><span data-stu-id="17f11-157">Make note of the SharePoint Online site, library, and folder URL.</span></span>

> [!TIP]
> <span data-ttu-id="17f11-158">Si vous créez un nouveau site et dossier pour vos données de test, autorisez au moins une heure pour cet emplacement à indexer avant de créer le classifieur qui utilisera ces données de départ.</span><span class="sxs-lookup"><span data-stu-id="17f11-158">If you create a new site and folder for your test data, allow at least an hour for that location to be indexed before creating the trainable classifier that will use that seed data.</span></span>

13. <span data-ttu-id="17f11-159">Choisissez `Add items to test`.</span><span class="sxs-lookup"><span data-stu-id="17f11-159">Choose `Add items to test`.</span></span>

14. <span data-ttu-id="17f11-160">Entrez l’URL du site, de la bibliothèque et du dossier SharePoint Online exactes pour le site de contenu de test à partir de l’étape 12.</span><span class="sxs-lookup"><span data-stu-id="17f11-160">Enter the exact SharePoint Online site, library, and folder URL for the test content site from step 12.</span></span> <span data-ttu-id="17f11-161">Choisissez `Add`.</span><span class="sxs-lookup"><span data-stu-id="17f11-161">Choose `Add`.</span></span>

15. <span data-ttu-id="17f11-162">Terminez l’Assistant en `Done`sélectionnant.</span><span class="sxs-lookup"><span data-stu-id="17f11-162">Finish the wizard by choosing `Done`.</span></span> <span data-ttu-id="17f11-163">Votre classificateur peut prendre jusqu’à une heure pour traiter les fichiers de test.</span><span class="sxs-lookup"><span data-stu-id="17f11-163">Your trainable classifier will take up to an hour to process the test files.</span></span>

16. <span data-ttu-id="17f11-164">Lorsque le classificateur de formation est fini de `Ready to review`traiter vos fichiers de test, l’État sur la page des détails prend la forme.</span><span class="sxs-lookup"><span data-stu-id="17f11-164">When the trainable classifier is done processing your test files, the status on the details page will change to `Ready to review`.</span></span> <span data-ttu-id="17f11-165">Si vous devez augmenter la taille de l’échantillon de test `Add items to test` , choisissez et autorisez le classificateur en train de traiter les éléments supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="17f11-165">If you need to increase the test sample size, choose `Add items to test` and allow the trainable classifier to process the additional items.</span></span>

![capture d’écran prêt à examiner](media/classifier-trainable-ready-to-review-detail.png)

17. <span data-ttu-id="17f11-167">Choisissez `Tested items to review` Tab pour passer en revue les éléments.</span><span class="sxs-lookup"><span data-stu-id="17f11-167">Choose `Tested items to review` tab to review items.</span></span>

18. <span data-ttu-id="17f11-168">Microsoft 365 présente 30 éléments à la fois.</span><span class="sxs-lookup"><span data-stu-id="17f11-168">Microsoft 365 will present 30 items at a time.</span></span> <span data-ttu-id="17f11-169">Vérifiez-les et, `We predict this item is "Relevant". Do you agree?` dans la zone `Yes` , `No` choisissez `Not sure, skip to next item`ou ou.</span><span class="sxs-lookup"><span data-stu-id="17f11-169">Review them and in the `We predict this item is "Relevant". Do you agree?` box choose either `Yes` or `No` or `Not sure, skip to next item`.</span></span> <span data-ttu-id="17f11-170">La précision du modèle est automatiquement mise à jour après 30 éléments.</span><span class="sxs-lookup"><span data-stu-id="17f11-170">Model accuracy is automatically updated after every 30 items.</span></span>

![zone passer en revue les éléments](media/classifier-trainable-review-detail.png)

19. <span data-ttu-id="17f11-172">Passez *en revue au moins* 200 éléments.</span><span class="sxs-lookup"><span data-stu-id="17f11-172">Review *at least* 200 items.</span></span>

<!-- insert Analyze steps here-->

20. <span data-ttu-id="17f11-173">Continuez à passer en revue jusqu’à ce que la précision atteigne `Publish the classifier` au moins `Ready to use`70% et que l’État est.</span><span class="sxs-lookup"><span data-stu-id="17f11-173">Continue to review until the accuracy reaches at least 70% and the `Publish the classifier` status is `Ready to use`.</span></span>

![précision et prêt à publier](media/classifier-trainable-review-ready-to-publish.png)

21. <span data-ttu-id="17f11-175">Publiez le classifieur.</span><span class="sxs-lookup"><span data-stu-id="17f11-175">Publish the classifier.</span></span>

22. <span data-ttu-id="17f11-176">Une fois publié, votre classifieur est disponible sous forme de condition dans la [stratégie d’attribution automatique d’étiquette de rétention basée sur une condition](labels.md#applying-a-retention-label-automatically-based-on-conditions) et [la conformité de communication](communication-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="17f11-176">Once published your classifier will be available as a condition in the [auto-apply retention label policy based on a condition](labels.md#applying-a-retention-label-automatically-based-on-conditions) and in [Communication compliance](communication-compliance.md).</span></span>

> [!CAUTION]
> <span data-ttu-id="17f11-177">Une fois qu’un classifieur est publié, il ne peut pas passer par une formation supplémentaire, nous vous recommandons donc de tester et de réviser autant d’éléments que possible afin de vous assurer que la précision est la plus élevée possible.</span><span class="sxs-lookup"><span data-stu-id="17f11-177">Once a classifier is published, it can't go through any additional training, so be very sure that you have tested and reviewed as many items as possible to ensure that the accuracy is as high as possible.</span></span>

## <a name="see-also"></a><span data-ttu-id="17f11-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17f11-178">See also</span></span>

- [<span data-ttu-id="17f11-179">Prise en main des classificateurs de formation (préversion)</span><span class="sxs-lookup"><span data-stu-id="17f11-179">Getting started with trainable classifiers (preview)</span></span>](classifier-getting-started-with.md)
- [<span data-ttu-id="17f11-180">Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="17f11-180">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)
