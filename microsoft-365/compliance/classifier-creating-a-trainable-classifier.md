---
title: Créer un classifieur de formation (aperçu)
f1.keywords:
- NOCSH
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
description: Utilisez des classifieurs pilotables lorsque l’un des classifieurs intégrés ne répond pas à vos besoins. Un classificateur Microsoft 365 est un outil que vous pouvez former afin de reconnaître différents types de contenu en leur donnant des exemples à consulter. Cette rubrique vous montre comment créer un classifieur personnalisé.
ms.openlocfilehash: 05ec9992fb4ec072403e193df3d7dbbbb8b1a96b
ms.sourcegitcommit: e8b9a4f18330bc09f665aa941f1286436057eb28
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/14/2020
ms.locfileid: "45126355"
---
# <a name="creating-a-trainable-classifier-preview"></a><span data-ttu-id="7d4ad-105">Création d’un classifieur de formation (aperçu)</span><span class="sxs-lookup"><span data-stu-id="7d4ad-105">Creating a trainable classifier (preview)</span></span>

<span data-ttu-id="7d4ad-106">Utilisez des classifieurs adaptés lorsque l’un des classifieurs de la zone ne répond pas à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-106">Use trainable classifiers when one of the out of the box classifiers won't meet your needs.</span></span> <span data-ttu-id="7d4ad-107">Un classificateur Microsoft 365 est un outil que vous pouvez former afin de reconnaître différents types de contenu en leur donnant des exemples à consulter.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-107">A Microsoft 365 classifier is a tool you can train to recognize various types of content by giving it samples to look at.</span></span> <span data-ttu-id="7d4ad-108">Formation le classificateur implique d’abord de donner aux échantillons prélevés par des personnes et correspondant à la catégorie positive.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-108">Training the classifier involves first giving it samples that are human picked and positively match the category.</span></span> <span data-ttu-id="7d4ad-109">Ensuite, une fois qu’il les a traités, vous testez les prévisions en lui donnant un mélange d’échantillons positifs et négatifs.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-109">Then, after it has processed those, you test the predictions by giving it a mix of positive and negative samples.</span></span>

<span data-ttu-id="7d4ad-110">Pour en savoir plus sur les différents types de classifieurs, voir [Getting Started with trainable Classifiers (Preview)](classifier-getting-started-with.md)</span><span class="sxs-lookup"><span data-stu-id="7d4ad-110">To learn more about the different types of classifiers, see [Getting started with trainable classifiers (preview)](classifier-getting-started-with.md)</span></span>

<span data-ttu-id="7d4ad-111">Cette chronologie reflète un exemple de déploiement.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-111">This timeline reflects a sample deployment.</span></span>

![formation de classifieur-chronologie](../media/trainable-classifier-deployment-timeline_border.png)

> [!TIP]
> <span data-ttu-id="7d4ad-113">L’option opt-in est requise pour la première fois pour les classifieurs de formation.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-113">Opt-in is required the first time for trainable classifiers.</span></span> <span data-ttu-id="7d4ad-114">Il faut douze jours pour que Microsoft 365 effectue une évaluation de base du contenu de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-114">It takes twelve days for Microsoft 365 to complete a baseline evaluation of your organizations content.</span></span> <span data-ttu-id="7d4ad-115">Contactez votre administrateur général pour lancer le processus d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-115">Contact your global administrator to kick off the opt-in process.</span></span>

## <a name="seed-content"></a><span data-ttu-id="7d4ad-116">Contenu de départ</span><span class="sxs-lookup"><span data-stu-id="7d4ad-116">Seed content</span></span>

<span data-ttu-id="7d4ad-117">Si vous souhaitez qu’un classifieur puisse identifier de manière indépendante et précise un élément comme étant dans une catégorie particulière de contenu, vous devez d’abord le présenter avec de nombreux exemples du type de contenu qui se trouve dans la catégorie.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-117">When you want a trainable classifier to independently and accurately identify an item as being in particular category of content, you first have to present it with many samples of the type of content that are in the category.</span></span> <span data-ttu-id="7d4ad-118">Cette alimentation d’échantillons vers le classificateur peut être qualifiée d' *amorçage*.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-118">This feeding of samples to the trainable classifier is known as *seeding*.</span></span> <span data-ttu-id="7d4ad-119">Le contenu de départ est sélectionné par un humain et est jugé pour représenter la catégorie de contenu.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-119">Seed content is selected by a human and is judged to represent the category of content.</span></span>

> [!TIP]
> <span data-ttu-id="7d4ad-120">Vous devez avoir au moins 50 échantillons positifs et un maximum de 500.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-120">You need to have at least 50 positive samples and as many as 500.</span></span> <span data-ttu-id="7d4ad-121">Le classificateur pouvant être mis en place traitera jusqu’à 500 exemples de création les plus récents (par date et heure de création du fichier).</span><span class="sxs-lookup"><span data-stu-id="7d4ad-121">The trainable classifier will process up to the 500 most recent created samples (by file created date/time stamp).</span></span> <span data-ttu-id="7d4ad-122">Plus le nombre d’exemples que vous fournissez est précis, plus les prévisions seront précises.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-122">The more samples you provide, the more accurate the predictions the classifier will make.</span></span>

## <a name="testing-content"></a><span data-ttu-id="7d4ad-123">Test du contenu</span><span class="sxs-lookup"><span data-stu-id="7d4ad-123">Testing content</span></span>

<span data-ttu-id="7d4ad-124">Une fois que le classifieur peut traiter suffisamment d’échantillons positifs pour créer un modèle de prévision, vous devez tester les prévisions qu’il permet de déterminer si le classifieur peut faire la distinction entre les éléments qui correspondent à la catégorie et ceux qui ne l’ont pas.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-124">Once the trainable classifier has processed enough positive samples to build a prediction model, you need to test the predictions it makes to see if the classifier can correctly distinguish between items that match the category and items that don't.</span></span> <span data-ttu-id="7d4ad-125">Pour ce faire, vous devez l’alimenter un autre ensemble de contenu choisi par l’homme qui se compose d’exemples qui doivent être inclus dans la catégorie et les échantillons qui ne le seront pas.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-125">You do this by feeding it another, hopefully larger, set of human picked content that consists of samples that should fall into the category and samples that won't.</span></span> <span data-ttu-id="7d4ad-126">Une fois qu’il les traite, vous parcourez manuellement les résultats et vérifiez si chaque prévision est correcte, incorrecte ou si vous n’êtes pas sûr.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-126">Once it processes those, you manually go through the results and verify whether each prediction is correct, incorrect, or you aren't sure.</span></span> <span data-ttu-id="7d4ad-127">Le classificateur de formation utilise ces commentaires pour améliorer son modèle de prévision.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-127">The trainable classifier uses this feedback to improve its prediction model.</span></span>

> [!TIP]
> <span data-ttu-id="7d4ad-128">Pour obtenir de meilleurs résultats, comportez 10 000 éléments dans votre jeu d’échantillons de test avec une répartition égale des correspondances positives et négatives.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-128">For best results, have 10,000 items in your test sample set with an even distribution of positive and negative matches.</span></span>

## <a name="how-to-create-a-trainable-classifier"></a><span data-ttu-id="7d4ad-129">Procédure de création d’un classifieur de formation</span><span class="sxs-lookup"><span data-stu-id="7d4ad-129">How to create a trainable classifier</span></span>

1. <span data-ttu-id="7d4ad-130">Collect entre les éléments de contenu Seed 50-500.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-130">Collect between 50-500 seed content items.</span></span> <span data-ttu-id="7d4ad-131">Il doit s’agir uniquement d’exemples qui représentent fortement le type de contenu que vous souhaitez que le classifieur peut identifier de manière positive comme appartenant à la catégorie de classification.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-131">These must be only samples that strongly represent the type of content you want the trainable classifier to positively identify as being in the classification category.</span></span> <span data-ttu-id="7d4ad-132">Pour connaître les types de fichiers pris en charge, reportez-vous aux [extensions de nom de fichier et aux types de fichiers analysés par défaut dans SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-132">See, [Default crawled file name extensions and parsed file types in SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) for the supported file types.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d4ad-133">Les éléments de l’exemple Seed et test ne doivent pas être chiffrés et doivent être en anglais.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-133">The seed and test sample items must not be encrypted and they must be in English.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d4ad-134">Assurez-vous que les éléments de votre ensemble Seed sont des exemples **forts** de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-134">Make sure the items in your seed set are **strong** examples of the category.</span></span> <span data-ttu-id="7d4ad-135">Le classificateur de formation génère initialement son modèle en fonction de ce que vous amorcez avec.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-135">The trainable classifier initially builds its model based on what you seed it with.</span></span> <span data-ttu-id="7d4ad-136">Le classifieur part du principe que tous les échantillons de départ sont des positifs forts et n’ont aucun moyen de savoir si un échantillon est une correspondance faible ou négative avec la catégorie.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-136">The classifier assumes all seed samples are strong positives and has no way of knowing if a sample is a weak or negative match to the category.</span></span>

2. <span data-ttu-id="7d4ad-137">Placez le contenu Seed dans un dossier SharePoint Online dédié au maintien *du contenu de l’amorçage uniquement*.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-137">Place the seed content in a SharePoint Online folder that is dedicated to holding *the seed content only*.</span></span> <span data-ttu-id="7d4ad-138">Notez l’URL du site, de la bibliothèque et du dossier.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-138">Make note of the site, library, and folder URL.</span></span>

> [!TIP]
> <span data-ttu-id="7d4ad-139">Si vous créez un nouveau site et dossier pour vos données de départ, autorisez au moins une heure pour cet emplacement à indexer avant de créer le classifieur qui utilisera ces données de départ.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-139">If you create a new site and folder for your seed data, allow at least an hour for that location to be indexed before creating the trainable classifier that will use that seed data.</span></span>

3. <span data-ttu-id="7d4ad-140">Connectez-vous au centre de conformité Microsoft 365 avec l’administrateur de conformité ou l’accès au rôle d’administrateur de sécurité et ouvrez le **Centre de conformité Microsoft 365 ou la** classification des données du centre de **sécurité Microsoft 365**  >  **Data classification**</span><span class="sxs-lookup"><span data-stu-id="7d4ad-140">Sign in to Microsoft 365 compliance center with compliance admin or security admin role access and open **Microsoft 365 compliance center** or **Microsoft 365 security center** > **Data classification**</span></span>

4. <span data-ttu-id="7d4ad-141">Sélectionnez l’onglet **classeurs de formation** .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-141">Choose the **Trainable classifiers** tab.</span></span>

5. <span data-ttu-id="7d4ad-142">Sélectionnez **Create Training classificateur**.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-142">Choose **Create trainable classifier**.</span></span>

6. <span data-ttu-id="7d4ad-143">Renseignez les valeurs appropriées pour les `Name` `Description` champs de la catégorie d’éléments que vous souhaitez que le classifieur pouvant identifier.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-143">Fill in appropriate values for the `Name`, and `Description` fields of the category of items you want this trainable classifier to identify.</span></span>

7. <span data-ttu-id="7d4ad-144">Entrez l’URL du site, de la bibliothèque et du dossier SharePoint Online exactes pour le site de contenu Seed à partir de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-144">Enter the exact SharePoint Online site, library, and folder URL for the seed content site from step 2.</span></span> <span data-ttu-id="7d4ad-145">Choisissez `Add` .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-145">Choose `Add`.</span></span>

8. <span data-ttu-id="7d4ad-146">Passez en revue les paramètres, puis choisissez `Create trainable classifier` .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-146">Review the settings and choose `Create trainable classifier`.</span></span>

9. <span data-ttu-id="7d4ad-147">Dans les 24 heures, le classificateur peut traiter les données de départ et créer un modèle de prévision.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-147">Within 24 hours the trainable classifier will process the seed data and build a prediction model.</span></span> <span data-ttu-id="7d4ad-148">L’état du classifieur est `In progress` en cours de traitement des données de l’amorçage.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-148">The classifier status is `In progress` while it processes the seed data.</span></span> <span data-ttu-id="7d4ad-149">Lorsque le classificateur a terminé le traitement des données de départ, l’État devient `Need test items` .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-149">When the classifier is finished processing the seed data, the status changes to `Need test items`.</span></span>

10. <span data-ttu-id="7d4ad-150">Vous pouvez désormais afficher la page de détails en choisissant le classifieur.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-150">You can now view the details page by choosing the classifier.</span></span>


![classificateur prêt à être testé](../media/classifier-trainable-ready-to-test-detail.png)

11. <span data-ttu-id="7d4ad-152">Collectez au moins 200 éléments de contenu de test.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-152">Collect at least 200 test content items.</span></span> <span data-ttu-id="7d4ad-153">Microsoft recommande 10 000 pour obtenir de meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-153">Microsoft recommends 10,000 for best results.</span></span> <span data-ttu-id="7d4ad-154">Il doit s’agir d’un mélange d’éléments qui sont des positifs forts, de fortes négatifs et d’autres moins évidents dans leur nature.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-154">These should be a mix of items that are strong positives, strong negatives and some that are a little less obvious in their nature.</span></span> <span data-ttu-id="7d4ad-155">Pour connaître les types de fichiers pris en charge, reportez-vous aux [extensions de nom de fichier et aux types de fichiers analysés par défaut dans SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-155">See, [Default crawled file name extensions and parsed file types in SharePoint Server](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types) for the supported file types.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d4ad-156">Les éléments de l’exemple ne doivent pas être chiffrés et doivent être en anglais.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-156">The sample items must not be encrypted and they must be in English.</span></span>

12. <span data-ttu-id="7d4ad-157">Placez le contenu de test dans un dossier SharePoint Online dédié à la conservation *du contenu de test uniquement*.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-157">Place the test content in a SharePoint Online folder that is dedicated to holding *the test content only*.</span></span> <span data-ttu-id="7d4ad-158">Notez le site SharePoint Online, la bibliothèque et l’URL du dossier.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-158">Make note of the SharePoint Online site, library, and folder URL.</span></span>

> [!TIP]
> <span data-ttu-id="7d4ad-159">Si vous créez un nouveau site et dossier pour vos données de test, autorisez au moins une heure pour cet emplacement à indexer avant de créer le classifieur qui utilisera ces données de départ.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-159">If you create a new site and folder for your test data, allow at least an hour for that location to be indexed before creating the trainable classifier that will use that seed data.</span></span>

13. <span data-ttu-id="7d4ad-160">Choisissez `Add items to test` .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-160">Choose `Add items to test`.</span></span>

14. <span data-ttu-id="7d4ad-161">Entrez l’URL du site, de la bibliothèque et du dossier SharePoint Online exactes pour le site de contenu de test à partir de l’étape 12.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-161">Enter the exact SharePoint Online site, library, and folder URL for the test content site from step 12.</span></span> <span data-ttu-id="7d4ad-162">Choisissez `Add` .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-162">Choose `Add`.</span></span>

15. <span data-ttu-id="7d4ad-163">Terminez l’Assistant en sélectionnant `Done` .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-163">Finish the wizard by choosing `Done`.</span></span> <span data-ttu-id="7d4ad-164">Votre classificateur peut prendre jusqu’à une heure pour traiter les fichiers de test.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-164">Your trainable classifier will take up to an hour to process the test files.</span></span>

16. <span data-ttu-id="7d4ad-165">Lorsque le classificateur de formation est fini de traiter vos fichiers de test, l’État sur la page des détails prend la forme `Ready to review` .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-165">When the trainable classifier is done processing your test files, the status on the details page will change to `Ready to review`.</span></span> <span data-ttu-id="7d4ad-166">Si vous devez augmenter la taille de l’échantillon de test, choisissez `Add items to test` et autorisez le classificateur en train de traiter les éléments supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-166">If you need to increase the test sample size, choose `Add items to test` and allow the trainable classifier to process the additional items.</span></span>

![capture d’écran prêt à examiner](../media/classifier-trainable-ready-to-review-detail.png)

17. <span data-ttu-id="7d4ad-168">Choisissez `Tested items to review` Tab pour passer en revue les éléments.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-168">Choose `Tested items to review` tab to review items.</span></span>

18. <span data-ttu-id="7d4ad-169">Microsoft 365 présente 30 éléments à la fois.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-169">Microsoft 365 will present 30 items at a time.</span></span> <span data-ttu-id="7d4ad-170">Vérifiez-les et, dans la `We predict this item is "Relevant". Do you agree?` zone, choisissez `Yes` ou `No` ou `Not sure, skip to next item` .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-170">Review them and in the `We predict this item is "Relevant". Do you agree?` box choose either `Yes` or `No` or `Not sure, skip to next item`.</span></span> <span data-ttu-id="7d4ad-171">La précision du modèle est automatiquement mise à jour après 30 éléments.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-171">Model accuracy is automatically updated after every 30 items.</span></span>

![zone passer en revue les éléments](../media/classifier-trainable-review-detail.png)

19. <span data-ttu-id="7d4ad-173">Passez *en revue au moins* 200 éléments.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-173">Review *at least* 200 items.</span></span>

<!-- insert Analyze steps here-->

20. <span data-ttu-id="7d4ad-174">Continuez à passer en revue jusqu’à ce que la précision atteigne au moins 70% et que l' `Publish the classifier` État est `Ready to use` .</span><span class="sxs-lookup"><span data-stu-id="7d4ad-174">Continue to review until the accuracy reaches at least 70% and the `Publish the classifier` status is `Ready to use`.</span></span>

![précision et prêt à publier](../media/classifier-trainable-review-ready-to-publish.png)

21. <span data-ttu-id="7d4ad-176">Publiez le classifieur.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-176">Publish the classifier.</span></span>

22. <span data-ttu-id="7d4ad-177">Une fois publié, votre classifieur sera disponible sous forme de condition dans [Office autolabeling avec des étiquettes de confidentialité](apply-sensitivity-label-automatically.md), [appliquant automatiquement une stratégie d’étiquette de rétention basée sur une condition](apply-retention-labels-automatically.md#configuring-conditions-for-auto-apply-retention-labels) et [la conformité de la communication](communication-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="7d4ad-177">Once published your classifier will be available as a condition in [Office autolabeling with sensitivity labels](apply-sensitivity-label-automatically.md), [auto-apply retention label policy based on a condition](apply-retention-labels-automatically.md#configuring-conditions-for-auto-apply-retention-labels) and in [Communication compliance](communication-compliance.md).</span></span>

> [!CAUTION]
> <span data-ttu-id="7d4ad-178">Une fois qu’un classifieur est publié, il ne peut pas passer par une formation supplémentaire, nous vous recommandons donc de tester et de réviser autant d’éléments que possible afin de vous assurer que la précision est la plus élevée possible.</span><span class="sxs-lookup"><span data-stu-id="7d4ad-178">Once a classifier is published, it can't go through any additional training, so be very sure that you have tested and reviewed as many items as possible to ensure that the accuracy is as high as possible.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d4ad-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d4ad-179">See also</span></span>

- [<span data-ttu-id="7d4ad-180">Prise en main des classificateurs pouvant être formés (préversion)</span><span class="sxs-lookup"><span data-stu-id="7d4ad-180">Getting started with trainable classifiers (preview)</span></span>](classifier-getting-started-with.md)
- [<span data-ttu-id="7d4ad-181">Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="7d4ad-181">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/sharepoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)
