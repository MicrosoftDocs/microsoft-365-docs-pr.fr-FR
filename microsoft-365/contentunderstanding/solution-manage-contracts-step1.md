---
title: Étape 1. Utiliser SharePoint Syntex pour identifier les fichiers de contrat et extraire des données
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: ssquires
audience: admin
ms.topic: article
ms.date: 05/17/2021
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Découvrez comment utiliser SharePoint Syntex pour identifier les fichiers de contrat et extraire des données à l’aide d’Microsoft 365 solution.
ms.openlocfilehash: f246dd4ed619dd9885d2c45c69d607cfa9c2483f
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538554"
---
# <a name="step-1-use-sharepoint-syntex-to-identify-contract-files-and-extract-data"></a><span data-ttu-id="c9a32-104">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="c9a32-104">Step 1.</span></span> <span data-ttu-id="c9a32-105">Utiliser SharePoint Syntex pour identifier les fichiers de contrat et extraire des données</span><span class="sxs-lookup"><span data-stu-id="c9a32-105">Use SharePoint Syntex to identify contract files and extract data</span></span>

<span data-ttu-id="c9a32-106">Votre organisation a besoin d’un moyen d’identifier et de classer tous les documents de contrat parmi les nombreux fichiers que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="c9a32-106">Your organization needs a way to identify and classify all contract documents from the many files you receive.</span></span> <span data-ttu-id="c9a32-107">Vous souhaitez également être en mesure d’afficher rapidement plusieurs éléments clés dans chacun des fichiers de contrat identifiés (par exemple, *client,* *fournisseur* et montant *des frais).*</span><span class="sxs-lookup"><span data-stu-id="c9a32-107">You also want to be able to quickly view several key elements in each of the contract files identified (for example, *Client*, *Contractor*, and *Fee amount*).</span></span> <span data-ttu-id="c9a32-108">Pour ce faire, vous pouvez utiliser [SharePoint Syntex](index.md) pour créer un modèle de compréhension de document et l’appliquer à une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="c9a32-108">You can do this by using [SharePoint Syntex](index.md) to create a document understanding model and applying it to a document library.</span></span>

## <a name="overview-of-the-process"></a><span data-ttu-id="c9a32-109">Vue d’ensemble du processus</span><span class="sxs-lookup"><span data-stu-id="c9a32-109">Overview of the process</span></span>

<span data-ttu-id="c9a32-110">[La compréhension des documents](document-understanding-overview.md) utilise des modèles d’intelligence artificielle (IA) pour automatiser la classification des fichiers et l’extraction des informations.</span><span class="sxs-lookup"><span data-stu-id="c9a32-110">[Document understanding](document-understanding-overview.md) uses artificial intelligence (AI) models to automate classification of files and extraction of information.</span></span> <span data-ttu-id="c9a32-111">Les modèles de compréhension des documents sont également optimaux pour l’extraction d’informations à partir de documents non structurés et semi-structurés où les informations dont vous avez besoin ne sont pas contenues dans des tableaux ou des formulaires, tels que des contrats.</span><span class="sxs-lookup"><span data-stu-id="c9a32-111">Document understanding models are also optimal in extracting information from unstructured and semi-structured documents where the information you need isn't contained in tables or forms, such as contracts.</span></span>

1. <span data-ttu-id="c9a32-112">Tout d’abord, vous devez trouver au moins cinq exemples de fichiers que vous pouvez utiliser pour « former » le modèle afin de rechercher des caractéristiques spécifiques au type de contenu que vous essayez d’identifier (contrat).</span><span class="sxs-lookup"><span data-stu-id="c9a32-112">First, you need to find at least five example files that you can use to "train" the model to search for characteristics that are specific to the content type you're trying to identify (a contract).</span></span> 

2. <span data-ttu-id="c9a32-113">À l SharePoint Syntex, créez un modèle de compréhension de document.</span><span class="sxs-lookup"><span data-stu-id="c9a32-113">Using SharePoint Syntex, create a new document understanding model.</span></span> <span data-ttu-id="c9a32-114">À l’aide de vos exemples de fichiers, vous devez [créer un classificateur](create-a-classifier.md).</span><span class="sxs-lookup"><span data-stu-id="c9a32-114">Using your example files, you need to [create a classifier](create-a-classifier.md).</span></span> <span data-ttu-id="c9a32-115">En formeant le classifieur avec vos exemples de fichiers, vous lui apprenez à rechercher des caractéristiques spécifiques à ce que vous verrez dans les contrats de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="c9a32-115">By training the classifier with your example files, you teach it to search for characteristics that are specific to what you would see in your company's contracts.</span></span> <span data-ttu-id="c9a32-116">Par exemple, [créez une «](create-a-classifier.md#create-an-explanation) explication » qui recherche des chaînes spécifiques dans vos contrats, telles que contrat de *service,* Conditions d’contrat *et* *Rémunération.*</span><span class="sxs-lookup"><span data-stu-id="c9a32-116">For example, [create an "explanation"](create-a-classifier.md#create-an-explanation) that searches for specific strings that are in your contracts, such as *Service Agreement*, *Terms of Agreement*, and *Compensation*.</span></span> <span data-ttu-id="c9a32-117">Vous pouvez même former votre explication pour rechercher ces chaînes dans des sections spécifiques du document ou en regard d’autres chaînes.</span><span class="sxs-lookup"><span data-stu-id="c9a32-117">You can even train your explanation to look for these strings in specific sections of the document, or located next to other strings.</span></span> <span data-ttu-id="c9a32-118">Lorsque vous pensez avoir formé votre classificateur avec les informations dont il a besoin, vous pouvez tester votre modèle sur un exemple d’exemple de fichiers pour voir son efficacité.</span><span class="sxs-lookup"><span data-stu-id="c9a32-118">When you think you have trained your classifier with the information it needs, you can test your model on a sample set of example files to see how efficient it is.</span></span> <span data-ttu-id="c9a32-119">Après le test, si nécessaire, vous pouvez choisir d’apporter des modifications à vos explications pour les rendre plus efficaces.</span><span class="sxs-lookup"><span data-stu-id="c9a32-119">After testing, if needed you can choose to make changes to your explanations to make them more efficient.</span></span> 

3. <span data-ttu-id="c9a32-120">Dans votre modèle, vous pouvez créer [un extracteur](create-an-extractor.md) pour extraire des éléments de données spécifiques de chaque contrat.</span><span class="sxs-lookup"><span data-stu-id="c9a32-120">In your model, you can [create an extractor](create-an-extractor.md) to pull out specific pieces of data from each contract.</span></span> <span data-ttu-id="c9a32-121">Par exemple, pour chaque contrat, les informations qui vous intéressent le plus sont qui est le client, le nom de l’prestataire et le coût total.</span><span class="sxs-lookup"><span data-stu-id="c9a32-121">For example, for each contract, the information you're most concerned about is who the client is, the name of the contractor, and the total cost.</span></span>

4. <span data-ttu-id="c9a32-122">Une fois que vous avez créé votre modèle, appliquez-le à [une SharePoint de documents.](apply-a-model.md)</span><span class="sxs-lookup"><span data-stu-id="c9a32-122">After you successfully create your model, [apply it to a SharePoint document library](apply-a-model.md).</span></span> <span data-ttu-id="c9a32-123">Lorsque vous téléchargez des documents dans la bibliothèque de documents, votre modèle de compréhension des documents s’exécute et identifie et classifie tous les fichiers qui correspondent au type de contenu de contrats que vous avez défini dans votre modèle.</span><span class="sxs-lookup"><span data-stu-id="c9a32-123">As you upload documents to the document library, your document understanding model will run and will identify and classify all files that match the contracts content type you defined in your model.</span></span> <span data-ttu-id="c9a32-124">Tous les fichiers classés en tant que contrats s’affichent dans un affichage bibliothèque personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c9a32-124">All files that are classified as contracts will display in a custom library view.</span></span> <span data-ttu-id="c9a32-125">Les fichiers affichent également les valeurs de chaque contrat que vous avez défini dans votre extracteur.</span><span class="sxs-lookup"><span data-stu-id="c9a32-125">The files will also display the values from each contract that you defined in your extractor.</span></span>

   ![Contrats dans la bibliothèque de documents](../media/content-understanding/doc-lib-solution.png)

5. <span data-ttu-id="c9a32-127">Si vous avez des exigences de rétention pour [](apply-a-retention-label-to-a-model.md) vos contrats, vous pouvez également utiliser votre modèle pour appliquer une étiquette de rétention qui empêchera la suppression de vos contrats pendant une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c9a32-127">If you have retention requirements for your contracts, you can also use your model to [apply a retention label](apply-a-retention-label-to-a-model.md) that will prevent your contracts from being deleted for a specified period of time.</span></span>

## <a name="steps-to-create-and-train-your-model"></a><span data-ttu-id="c9a32-128">Étapes de création et de formation de votre modèle</span><span class="sxs-lookup"><span data-stu-id="c9a32-128">Steps to create and train your model</span></span>

> [!NOTE]
> <span data-ttu-id="c9a32-129">Pour ces étapes, vous pouvez utiliser les exemples de fichiers dans le référentiel [Microsoft SharePoint Syntex Samples](https://github.com/pnp/syntex-samples).</span><span class="sxs-lookup"><span data-stu-id="c9a32-129">For these steps, you can use the example files in the [Microsoft SharePoint Syntex Samples repository](https://github.com/pnp/syntex-samples).</span></span> <span data-ttu-id="c9a32-130">Les exemples de ce référentiel contiennent à la fois les fichiers de modèle de compréhension de document et les fichiers utilisés pour former le modèle.</span><span class="sxs-lookup"><span data-stu-id="c9a32-130">The samples in this repository contain both the document understanding model files and the files used to train the model.</span></span>

### <a name="create-a-contract-model"></a><span data-ttu-id="c9a32-131">Créer un modèle de contrat</span><span class="sxs-lookup"><span data-stu-id="c9a32-131">Create a Contract model</span></span>

<span data-ttu-id="c9a32-132">La première étape consiste à créer votre modèle de contrat.</span><span class="sxs-lookup"><span data-stu-id="c9a32-132">The first step is to create your Contract model.</span></span>

1. <span data-ttu-id="c9a32-133">Dans le centre de contenu, sélectionnez **Nouveau**, puis **Créer un modèle**.</span><span class="sxs-lookup"><span data-stu-id="c9a32-133">From the content center, select **New**, and then **Create a model**.</span></span>

2. <span data-ttu-id="c9a32-134">Dans le **volet Nouveau document comprendre le modèle,** dans **le** champ Nom, tapez le nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="c9a32-134">On the **New document understanding model** pane, in the **Name** field, type the name of the model.</span></span> <span data-ttu-id="c9a32-135">Pour cette solution de gestion de contrat, vous pouvez nommer le contrat *de modèle.*</span><span class="sxs-lookup"><span data-stu-id="c9a32-135">For this contract management solution, you can name the model *Contract*.</span></span>

4. <span data-ttu-id="c9a32-136">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="c9a32-136">Choose **Create**.</span></span> <span data-ttu-id="c9a32-137">Cette opération permet de créer une page d’accueil pour le modèle.</span><span class="sxs-lookup"><span data-stu-id="c9a32-137">This creates a home page for the model.</span></span></br>

    ![Capture d’écran de la page d’accueil contrat.](../media/content-understanding/models-contract-home-page.png)


### <a name="train-your-model-to-classify-a-type-of-file"></a><span data-ttu-id="c9a32-139">Former votre modèle pour classifier un type de fichier</span><span class="sxs-lookup"><span data-stu-id="c9a32-139">Train your model to classify a type of file</span></span>

#### <a name="add-example-files-for-your-model"></a><span data-ttu-id="c9a32-140">Ajouter des exemples de fichiers pour votre modèle</span><span class="sxs-lookup"><span data-stu-id="c9a32-140">Add example files for your model</span></span>

<span data-ttu-id="c9a32-141">Vous devez ajouter au moins cinq exemples de fichiers qui sont des documents de contrat et un exemple de fichier qui n’est pas un document de contrat (par exemple, une instruction de travail).</span><span class="sxs-lookup"><span data-stu-id="c9a32-141">You need to add at least five example files that are contract documents, and one example file that's not a contract document (for example, a statement of work).</span></span> 

1. <span data-ttu-id="c9a32-142">Dans la page **Modèles > contrat,** sous **Actions** clés Ajouter des  >  **exemples** de fichiers, **sélectionnez Ajouter des fichiers.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-142">On the **Models > Contract** page, under **Key actions** > **Add example files**, select **Add files**.</span></span>

   ![Capture d’écran montrant la page Contrats avec l’option Ajouter des exemples de fichiers mise en évidence.](../media/content-understanding/key-actions-add-example-files.png)

2. <span data-ttu-id="c9a32-144">Dans la page **Sélectionner des exemples** de fichiers pour votre modèle, ouvrez le dossier Contrat, sélectionnez les fichiers à utiliser, puis sélectionnez **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-144">On the **Select example files for your model** page, open the Contract folder, select files you want to use, and then select **Add**.</span></span> <span data-ttu-id="c9a32-145">Si vous n’avez pas d’exemples de fichiers, **sélectionnez Télécharger** pour les ajouter.</span><span class="sxs-lookup"><span data-stu-id="c9a32-145">If you don't have example files there, select **Upload** to add them.</span></span>

#### <a name="label-the-files-as-positive-or-negative-examples"></a><span data-ttu-id="c9a32-146">Étiqueter les fichiers en tant qu’exemples positifs ou négatifs</span><span class="sxs-lookup"><span data-stu-id="c9a32-146">Label the files as positive or negative examples</span></span>

1. <span data-ttu-id="c9a32-147">Dans la page **Modèles > contrat,** sous Actions clés Classifier les fichiers et exécuter une formation, sélectionnez Former le  >   **classifieur**.</span><span class="sxs-lookup"><span data-stu-id="c9a32-147">On the **Models > Contract** page, under **Key actions** > **Classify files and run training**, select **Train classifier**.</span></span>

   ![Screenshot showing the Contracts page with Classify files and run training option highlighted.](../media/content-understanding/key-actions-classify-files.png)

2. <span data-ttu-id="c9a32-149">Dans la page Model **> Contract > Contract classifier,** dans la visionneuse en haut du premier exemple de fichier, vous verrez un texte demandant si le fichier est un exemple du modèle de contrat que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="c9a32-149">On the **Models > Contract > Contract classifier** page, in the viewer on the top of the first example file, you'll see text asking if the file is an example of the Contract model you created.</span></span> <span data-ttu-id="c9a32-150">Si cet exemple est positif, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="c9a32-150">If it is a positive example, select **Yes**.</span></span> <span data-ttu-id="c9a32-151">Si cet exemple est négatif, sélectionnez **Non**.</span><span class="sxs-lookup"><span data-stu-id="c9a32-151">If it is a negative example, select **No**.</span></span>

3. <span data-ttu-id="c9a32-152">Dans la **liste d’exemples** étiquetés à gauche, sélectionnez les autres fichiers que vous souhaitez utiliser comme exemples et étiquetez-les.</span><span class="sxs-lookup"><span data-stu-id="c9a32-152">From the **Labeled examples** list on the left, select other files that you want to use as examples, and label them.</span></span> 

    ![Page d’accueil du classifieur](../media/content-understanding/models-contract-classifier.png) 

#### <a name="add-at-least-one-explanation-to-train-the-classifier"></a><span data-ttu-id="c9a32-154">Ajouter au moins une explication pour former le classifieur</span><span class="sxs-lookup"><span data-stu-id="c9a32-154">Add at least one explanation to train the classifier</span></span> 

1. <span data-ttu-id="c9a32-155">Dans la page **> contrat > contrat,** sélectionnez **l’onglet** Train.</span><span class="sxs-lookup"><span data-stu-id="c9a32-155">On the **Models > Contract > Contract classifier** page, select the **Train** tab.</span></span>

2. <span data-ttu-id="c9a32-156">Dans la section **Fichiers entraînés,** vous verrez une liste des exemples de fichiers que vous avez précédemment étiquetés.</span><span class="sxs-lookup"><span data-stu-id="c9a32-156">In the **Trained files** section, you'll see a list of the example files that you previously labeled.</span></span> <span data-ttu-id="c9a32-157">Sélectionnez l’un des fichiers positifs dans la liste pour l’afficher dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="c9a32-157">Select one of the positive files from the list to display it in the viewer.</span></span>

3. <span data-ttu-id="c9a32-158">Dans la section **Explications,** sélectionnez **Nouveau,** puis **Vide.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-158">In the **Explanations** section, select **New** and then **Blank**.</span></span>

4. <span data-ttu-id="c9a32-159">À la page **Créer une explication** :</span><span class="sxs-lookup"><span data-stu-id="c9a32-159">On the **Create an explanation** page:</span></span>

    <span data-ttu-id="c9a32-160">a.</span><span class="sxs-lookup"><span data-stu-id="c9a32-160">a.</span></span> <span data-ttu-id="c9a32-161">Dans le **champ** Nom, tapez le nom de l’explication (par exemple, « Contrat »).</span><span class="sxs-lookup"><span data-stu-id="c9a32-161">In the **Name** field, type the name of the explanation (such as "Agreement").</span></span>

    <span data-ttu-id="c9a32-162">b.</span><span class="sxs-lookup"><span data-stu-id="c9a32-162">b.</span></span> <span data-ttu-id="c9a32-163">Dans le **champ Type d’explication,** **sélectionnez Liste d’expressions,** car vous ajoutez une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="c9a32-163">In the **Explanation type** field, select **Phrase list**, because you add a text string.</span></span>

    <span data-ttu-id="c9a32-164">c.</span><span class="sxs-lookup"><span data-stu-id="c9a32-164">c.</span></span> <span data-ttu-id="c9a32-165">Dans la **zone de liste Phrase,** tapez la chaîne (par exemple, « AGREEMENT »).</span><span class="sxs-lookup"><span data-stu-id="c9a32-165">In the **Phrase list** box, type the string (such as "AGREEMENT").</span></span> <span data-ttu-id="c9a32-166">Vous pouvez sélectionner **la case sensible** si la chaîne doit être sensible à la cas.</span><span class="sxs-lookup"><span data-stu-id="c9a32-166">You can select **Case sensitive** if the string needs to be case-sensitive.</span></span>

    <span data-ttu-id="c9a32-167">d.</span><span class="sxs-lookup"><span data-stu-id="c9a32-167">d.</span></span> <span data-ttu-id="c9a32-168">Sélectionnez **Enregistrer et entraîner.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-168">Select **Save and train**.</span></span>

    ![Capture d’écran du panneau Créer une explication.](../media/content-understanding/contract-classifier-create-explanation.png) 

#### <a name="test-your-model"></a><span data-ttu-id="c9a32-170">Tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="c9a32-170">Test your model</span></span>

<span data-ttu-id="c9a32-171">Vous pouvez tester votre modèle de contrat sur des exemples de fichiers qu’il n’a pas vus auparavant.</span><span class="sxs-lookup"><span data-stu-id="c9a32-171">You can test your Contract model on example files it hasn’t seen before.</span></span> <span data-ttu-id="c9a32-172">Cela est facultatif, mais il peut s’avérer utile.</span><span class="sxs-lookup"><span data-stu-id="c9a32-172">This is optional, but it can be a useful best practice.</span></span>

1. <span data-ttu-id="c9a32-173">Dans la page **Modèles > contrat > classifieur** de contrat, sélectionnez **l’onglet Test.** Cette fonction exécute le modèle sur vos exemples de fichiers non lamentés.</span><span class="sxs-lookup"><span data-stu-id="c9a32-173">On the **Models > Contract > Contract classifier** page, select the **Test** tab. This runs the model on your unlabeled example files.</span></span>

2. <span data-ttu-id="c9a32-174">Dans la **liste Fichiers de test,** vos exemples de fichiers s’affichent et indiquent si le modèle les a prédits comme positifs ou négatifs.</span><span class="sxs-lookup"><span data-stu-id="c9a32-174">In the **Test Files** list, your example files display and shows if the model predicted them to be positive or negative.</span></span> <span data-ttu-id="c9a32-175">Utilisez ces informations pour déterminer plus facilement l’efficacité de votre classifieur lors de l’identification de vos documents.</span><span class="sxs-lookup"><span data-stu-id="c9a32-175">Use this information to help determine the effectiveness of your classifier in identifying your documents.</span></span>

    ![Capture d’écran des fichiers non lamentés dans la liste Fichiers texte](../media/content-understanding/test-on-files.png) 

3. <span data-ttu-id="c9a32-177">Lorsque vous avez terminé, **sélectionnez Quitter la formation.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-177">When done, select **Exit Training**.</span></span>

### <a name="create-and-train-an-extractor"></a><span data-ttu-id="c9a32-178">Créer et former un extracteur</span><span class="sxs-lookup"><span data-stu-id="c9a32-178">Create and train an extractor</span></span>

1. <span data-ttu-id="c9a32-179">Dans la page **Modèles > contrat,** sous **Actions** clés Créer et former des  >  **extracteurs,** **sélectionnez Créer un extracteur**.</span><span class="sxs-lookup"><span data-stu-id="c9a32-179">On the **Models > Contract** page, under **Key actions** > **Create and train extractors**, select **Create extractor**.</span></span>

   ![Screenshot showing the Contracts page with Create and train extractors option highlighted.](../media/content-understanding/key-actions-create-extractors.png)

2. <span data-ttu-id="c9a32-181">Dans le **panneau Nouvel extracteur d’entités,** dans le champ Nouveau nom, tapez le nom de votre extracteur. </span><span class="sxs-lookup"><span data-stu-id="c9a32-181">On the **New entity extractor** panel, in the **New name** field, type the name of your extractor.</span></span> <span data-ttu-id="c9a32-182">Par exemple, nommez-le *Client* si vous souhaitez extraire le nom du client de chaque contrat.</span><span class="sxs-lookup"><span data-stu-id="c9a32-182">For example, name it *Client* if you want to extract the name of the client from each contract.</span></span>

3. <span data-ttu-id="c9a32-183">Lorsque vous avez terminé, sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-183">When you're done, select **Create**.</span></span>

#### <a name="label-the-entity-you-want-to-extract"></a><span data-ttu-id="c9a32-184">Étiqueter l’entité que vous souhaitez extraire</span><span class="sxs-lookup"><span data-stu-id="c9a32-184">Label the entity you want to extract</span></span>

<span data-ttu-id="c9a32-185">Lorsque vous créez l’extracteur, la page de l’extracteur s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="c9a32-185">When you create the extractor, the extractor page opens.</span></span> <span data-ttu-id="c9a32-186">Cette page affiche la liste des fichiers échantillons, le premier fichier de la liste étant affiché dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="c9a32-186">Here you see a list of your sample files, with the first file on the list displayed in the viewer.</span></span>

![Capture d’écran de la page Exemples étiquetés de l’extracteur client.](../media/content-understanding/client-extractor-labeled-examples.png) 

<span data-ttu-id="c9a32-188">Pour étiqueter l’entité :</span><span class="sxs-lookup"><span data-stu-id="c9a32-188">To label the entity:</span></span>

1. <span data-ttu-id="c9a32-189">Dans la visionneuse, sélectionnez les données à extraire des fichiers.</span><span class="sxs-lookup"><span data-stu-id="c9a32-189">From the viewer, select the data that you want to extract from the files.</span></span> <span data-ttu-id="c9a32-190">Par exemple, si vous souhaitez extraire le *client,* vous mettez en surbrillez la valeur du client dans le premier fichier (dans cet exemple, Best *For You Organics*), puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c9a32-190">For example, if you want to extract the *Client*, you highlight the client value in the first file (in this example, *Best For You Organics*), and then select **Save**.</span></span> <span data-ttu-id="c9a32-191">La valeur du fichier s’affiche dans la liste **Exemples** étiquetés, sous la **colonne Étiquette.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-191">You'll see the value display from the file in the **Labeled examples** list, under the **Label** column.</span></span>

2. <span data-ttu-id="c9a32-192">Sélectionnez **Fichier suivant** à l’auto-ave et ouvrez le fichier suivant dans la liste dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="c9a32-192">Select **Next file** to autosave and open the next file in the list in the viewer.</span></span> <span data-ttu-id="c9a32-193">Ou **sélectionnez Enregistrer,** puis sélectionnez un autre fichier dans la liste **d’exemples étiquetés.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-193">Or select **Save**, and then select another file from the **Labeled examples** list.</span></span>

3. <span data-ttu-id="c9a32-194">Dans la visionneuse, répétez les étapes 1 et 2, puis répétez jusqu’à ce que vous avez enregistré l’étiquette dans tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="c9a32-194">In the viewer, repeat steps 1 and 2, then repeat until you saved the label in all the files.</span></span>

<span data-ttu-id="c9a32-195">Une fois que vous avez étiqueté les fichiers, une bannière de notification s’affiche pour vous informer de la mise en formation.</span><span class="sxs-lookup"><span data-stu-id="c9a32-195">After you've labeled the files, a notification banner displays informing you to move to training.</span></span> <span data-ttu-id="c9a32-196">Vous pouvez choisir d’étiqueter d’autres documents ou de passer à la formation.</span><span class="sxs-lookup"><span data-stu-id="c9a32-196">You can choose to label more documents or advance to training.</span></span>

#### <a name="add-an-explanation"></a><span data-ttu-id="c9a32-197">Ajouter une explication</span><span class="sxs-lookup"><span data-stu-id="c9a32-197">Add an explanation</span></span>

<span data-ttu-id="c9a32-198">Vous pouvez créer une explication qui fournit un conseil sur le format d’entité lui-même et les variantes qu’il peut avoir dans les exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c9a32-198">You can create an explanation that provides a hint about the entity format itself and variations it might have in the example files.</span></span> <span data-ttu-id="c9a32-199">Par exemple, une valeur de date peut être dans de nombreux formats différents, tels que :</span><span class="sxs-lookup"><span data-stu-id="c9a32-199">For example, a date value can be in many different formats, such as:</span></span>

- <span data-ttu-id="c9a32-200">14/10/2019</span><span class="sxs-lookup"><span data-stu-id="c9a32-200">10/14/2019</span></span>
- <span data-ttu-id="c9a32-201">14 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="c9a32-201">October 14, 2019</span></span>
- <span data-ttu-id="c9a32-202">Lundi 14 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="c9a32-202">Monday, October 14, 2019</span></span>

<span data-ttu-id="c9a32-203">Pour vous aider à identifier la *date de début du* contrat, vous pouvez créer une explication de modèle.</span><span class="sxs-lookup"><span data-stu-id="c9a32-203">To help identify the *Contract Start Date*, you can create a pattern explanation.</span></span>

1. <span data-ttu-id="c9a32-204">Dans la section **Explications,** sélectionnez **Nouveau,** puis **Vide.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-204">In the **Explanations** section, select **New** and then **Blank**.</span></span>

2. <span data-ttu-id="c9a32-205">À la page **Créer une explication** :</span><span class="sxs-lookup"><span data-stu-id="c9a32-205">On the **Create an explanation** page:</span></span>

    <span data-ttu-id="c9a32-206">a.</span><span class="sxs-lookup"><span data-stu-id="c9a32-206">a.</span></span> <span data-ttu-id="c9a32-207">Dans le **champ Nom,** tapez le nom de l’explication (par exemple, *Date*).</span><span class="sxs-lookup"><span data-stu-id="c9a32-207">In the **Name** field, type the name of the explanation (such as *Date*).</span></span>

    <span data-ttu-id="c9a32-208">b.</span><span class="sxs-lookup"><span data-stu-id="c9a32-208">b.</span></span> <span data-ttu-id="c9a32-209">Dans le **champ Type d’explication,** sélectionnez **Liste de modèles.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-209">In the **Explanation type** field, select **Pattern list**.</span></span>

    <span data-ttu-id="c9a32-210">c.</span><span class="sxs-lookup"><span data-stu-id="c9a32-210">c.</span></span> <span data-ttu-id="c9a32-211">Dans le **champ Valeur,** fournissez la variante de date telle qu’elle apparaît dans les exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c9a32-211">In the **Value** field, provide the date variation as they appear in the sample files.</span></span> <span data-ttu-id="c9a32-212">Par exemple, si certaines dates apparaissent au format 0/00/0000, vous devez entrer les variations qui apparaissent dans vos documents, par exemple :</span><span class="sxs-lookup"><span data-stu-id="c9a32-212">For example, if you have date formats that appear as 0/00/0000, you enter any variations that appear in your documents, such as:</span></span>

    - <span data-ttu-id="c9a32-213">0/0/0000</span><span class="sxs-lookup"><span data-stu-id="c9a32-213">0/0/0000</span></span>
    - <span data-ttu-id="c9a32-214">0/00/0000</span><span class="sxs-lookup"><span data-stu-id="c9a32-214">0/00/0000</span></span>
    - <span data-ttu-id="c9a32-215">00/0/0000</span><span class="sxs-lookup"><span data-stu-id="c9a32-215">00/0/0000</span></span>
    - <span data-ttu-id="c9a32-216">00/00/0000</span><span class="sxs-lookup"><span data-stu-id="c9a32-216">00/00/0000</span></span>

4. <span data-ttu-id="c9a32-217">Sélectionnez **Enregistrer et entraîner.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-217">Select **Save and train**.</span></span>

#### <a name="test-your-model-again"></a><span data-ttu-id="c9a32-218">Tester à nouveau votre modèle</span><span class="sxs-lookup"><span data-stu-id="c9a32-218">Test your model again</span></span>

<span data-ttu-id="c9a32-219">Vous pouvez tester votre modèle de contrat sur des exemples de fichiers qu’il n’a pas vus auparavant.</span><span class="sxs-lookup"><span data-stu-id="c9a32-219">You can test your Contract model on example files it hasn’t seen before.</span></span> <span data-ttu-id="c9a32-220">Cela est facultatif, mais il peut s’avérer utile.</span><span class="sxs-lookup"><span data-stu-id="c9a32-220">This is optional, but it can be a useful best practice.</span></span>

1. <span data-ttu-id="c9a32-221">Dans la page **Modèles > contrat > classifieur** de contrat, sélectionnez **l’onglet Test.** Cette fonction exécute le modèle sur vos exemples de fichiers non lamentés.</span><span class="sxs-lookup"><span data-stu-id="c9a32-221">On the **Models > Contract > Contract classifier** page, select the **Test** tab. This runs the model on your unlabeled example files.</span></span>

2. <span data-ttu-id="c9a32-222">Dans la liste **Des fichiers de** test, vos exemples de fichiers s’affichent et indiquent si le modèle est en mesure d’extraire les informations dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="c9a32-222">In the **Test files** list, your example files display and shows if the model is able to extract the information you need.</span></span> <span data-ttu-id="c9a32-223">Utilisez ces informations pour déterminer plus facilement l’efficacité de votre classifieur lors de l’identification de vos documents.</span><span class="sxs-lookup"><span data-stu-id="c9a32-223">Use this information to help determine the effectiveness of your classifier in identifying your documents.</span></span>

3. <span data-ttu-id="c9a32-224">Lorsque vous avez terminé, **sélectionnez Quitter la formation.**</span><span class="sxs-lookup"><span data-stu-id="c9a32-224">When done, select **Exit Training**.</span></span>

### <a name="apply-your-model-to-a-document-library"></a><span data-ttu-id="c9a32-225">Appliquer votre modèle à une bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="c9a32-225">Apply your model to a document library</span></span>

<span data-ttu-id="c9a32-226">Pour appliquer votre modèle à une bibliothèque SharePoint de documents :</span><span class="sxs-lookup"><span data-stu-id="c9a32-226">To apply your model to a SharePoint document library:</span></span>

1. <span data-ttu-id="c9a32-227">Dans la page **Modèles > contrat,** sous **Actions** clés Appliquer le modèle aux  >  bibliothèques, sélectionnez **Appliquer le modèle**.</span><span class="sxs-lookup"><span data-stu-id="c9a32-227">On the **Models > Contract** page, under **Key actions** > **Apply model to libraries**, select **Apply model**.</span></span>

   ![Screenshot showing the Contracts page with Apply model to libraries option highlighted.](../media/content-understanding/key-actions-apply-model.png)

2. <span data-ttu-id="c9a32-229">Dans le **panneau Ajouter un** contrat, sélectionnez le site SharePoint qui contient la bibliothèque de documents à appliquer au modèle.</span><span class="sxs-lookup"><span data-stu-id="c9a32-229">On the **Add Contract** panel, select the SharePoint site that contains the document library that you want to apply the model to.</span></span> <span data-ttu-id="c9a32-230">Si le site n’apparaît pas dans la liste, utilisez la zone de recherche pour le trouver.</span><span class="sxs-lookup"><span data-stu-id="c9a32-230">If the site does not show in the list, use the search box to find it.</span></span> <span data-ttu-id="c9a32-231">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c9a32-231">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9a32-232">Vous devez disposer d’autorisations *Gérer la liste* ou de droits *Modifier* sur la bibliothèque de documents à laquelle vous appliquez le modèle.</span><span class="sxs-lookup"><span data-stu-id="c9a32-232">You must have *Manage List* permissions or *Edit* rights to the document library you are applying the model to.</span></span>

3. <span data-ttu-id="c9a32-233">Après avoir sélectionné le site, sélectionnez la bibliothèque de documents à laquelle vous souhaitez appliquer le modèle.</span><span class="sxs-lookup"><span data-stu-id="c9a32-233">After you select the site, select the document library to which you want to apply the model.</span></span>

4. <span data-ttu-id="c9a32-234">Étant donné que le modèle est associé à un type de contenu, lorsque vous l’appliquez à la bibliothèque, il ajoute le type de contenu et son affichage avec les étiquettes que vous avez extraites en tant que colonnes.</span><span class="sxs-lookup"><span data-stu-id="c9a32-234">Because the model is associated to a content type, when you apply it to the library it will add the content type and its view with the labels you extracted showing as columns.</span></span> <span data-ttu-id="c9a32-235">Cet affichage est l’affichage par défaut de la bibliothèque par défaut, mais vous pouvez éventuellement choisir  de ne pas en faire l’affichage par défaut en sélectionnant **Paramètres** avancés et en effanant la case à cocher Définir ce nouvel affichage comme affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="c9a32-235">This view is the library's default view by default, but you can optionally choose to have it not be the default view by selecting **Advanced settings** and clearing the **Set this new view as default** check box.</span></span>

5. <span data-ttu-id="c9a32-236">Sélectionnez **Ajouter** pour appliquer le modèle à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c9a32-236">Select **Add** to apply the model to the library.</span></span>

6. <span data-ttu-id="c9a32-237">Dans la page **Modèles > contrat,** dans la **section** Bibliothèques avec ce modèle, vous verrez l’URL du site SharePoint répertorié.</span><span class="sxs-lookup"><span data-stu-id="c9a32-237">On the **Models > Contract** page, in the **Libraries with this model** section, you'll see the URL to the SharePoint site listed.</span></span>

    ![Capture d’écran de la page d’accueil Contrat affichant les bibliothèques avec cette section de modèle.](../media/content-understanding/contract-libraries-with-this-model.png)

<span data-ttu-id="c9a32-239">Après avoir appliqué le modèle à la bibliothèque de documents, vous pouvez commencer à télécharger des documents sur le site et voir les résultats.</span><span class="sxs-lookup"><span data-stu-id="c9a32-239">After you apply the model to the document library, you can begin uploading documents to the site and see the results.</span></span>

## <a name="next-step"></a><span data-ttu-id="c9a32-240">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="c9a32-240">Next step</span></span>

[<span data-ttu-id="c9a32-241">Étape 2. Utiliser Microsoft Teams pour créer votre canal de gestion de contrat</span><span class="sxs-lookup"><span data-stu-id="c9a32-241">Step 2. Use Microsoft Teams to create your contract management channel</span></span>](solution-manage-contracts-step2.md)