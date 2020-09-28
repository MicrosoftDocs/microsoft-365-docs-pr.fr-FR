---
title: Créer un classifieur
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: En savoir plus sur la création d’un classifieur
ms.openlocfilehash: 29b2a4775bec12649c66b4cb4a07fe5f0fc93ae2
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48294901"
---
# <a name="create-a-classifier-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="5f6e0-103">Créer un classifieur dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="5f6e0-103">Create a classifier in Microsoft SharePoint Syntex</span></span>

<span data-ttu-id="5f6e0-104">Le contenu de cet article est destiné à la préversion privée du projet cortex.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-104">The content in this article is for the Project Cortex Private Preview.</span></span> <span data-ttu-id="5f6e0-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="5f6e0-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CL0R]  

</br>

<span data-ttu-id="5f6e0-106">Un classifieur est un type de modèle que vous pouvez utiliser pour automatiser l’identification et la classification d’un type de document.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-106">A classifier is a type of model that you can use to automate identification and classification of a document type.</span></span> <span data-ttu-id="5f6e0-107">Par exemple, vous pouvez identifier tous les documents de *renouvellement de contrat* ajoutés à votre bibliothèque de documents, comme illustré dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-107">For example, you may want to identify all *Contract Renewal* documents that are added to your document library, such as is shown in the following illustration.</span></span>

![Document de renouvellement de contrat](../media/content-understanding/contract-renewal.png)

<span data-ttu-id="5f6e0-109">La création d’un classifieur vous permet de créer un nouveau [type de contenu SharePoint](https://docs.microsoft.com/sharepoint/governance/content-type-and-workflow-planning#content-type-overview) qui sera associé au modèle.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-109">Creating a classifier enables you to create a new [SharePoint Content Type](https://docs.microsoft.com/sharepoint/governance/content-type-and-workflow-planning#content-type-overview) that will be associated to the model.</span></span>

<span data-ttu-id="5f6e0-110">Lors de la création du classifieur, vous devez créer des *explications* pour définir le modèle.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-110">When creating the classifier, you need to create *explanations* to define the model.</span></span> <span data-ttu-id="5f6e0-111">Cela vous permet de noter les données communes que vous devriez voir toujours trouver ce type de document.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-111">This enables you to note common data that you would expect to consistently find this document type.</span></span> 

<span data-ttu-id="5f6e0-112">Utilisez des exemples de type de document (« exemples de fichiers ») pour « former » votre modèle afin d’identifier les fichiers qui ont le même type de contenu.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-112">Use examples of the document type ("example files") to "train" your model to identify files that have the same content type.</span></span>

<span data-ttu-id="5f6e0-113">Pour créer un classifieur, vous devez :</span><span class="sxs-lookup"><span data-stu-id="5f6e0-113">To create a classifier, you need to:</span></span>
1. <span data-ttu-id="5f6e0-114">Nommez votre modèle.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-114">Name your model.</span></span>
2. <span data-ttu-id="5f6e0-115">Ajoutez vos exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-115">Add your example files.</span></span>
3. <span data-ttu-id="5f6e0-116">Étiquetez vos exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-116">Label your example files.</span></span>
4. <span data-ttu-id="5f6e0-117">Créer une explication.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-117">Create an explanation.</span></span>
5. <span data-ttu-id="5f6e0-118">Testez votre modèle.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-118">Test your model.</span></span>

> [!NOTE]
> <span data-ttu-id="5f6e0-119">Bien que votre modèle utilise un classifieur pour identifier et classer les types de documents, vous pouvez également choisir d’extraire des informations spécifiques de chaque fichier identifié par le modèle.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-119">While your model uses a classifier to identify and classify document types, you can also choose to pull specific pieces of information from each file identified by the model.</span></span> <span data-ttu-id="5f6e0-120">Pour ce faire, créez un **extracteur** à ajouter à votre modèle.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-120">Do this by creating an **extractor** to add to your model.</span></span> <span data-ttu-id="5f6e0-121">Consultez la rubrique [créer un extracteur](create-an-extractor.md).</span><span class="sxs-lookup"><span data-stu-id="5f6e0-121">See [Create an extractor](create-an-extractor.md).</span></span>

## <a name="name-your-model"></a><span data-ttu-id="5f6e0-122">Nommer votre modèle</span><span class="sxs-lookup"><span data-stu-id="5f6e0-122">Name your model</span></span>

<span data-ttu-id="5f6e0-123">La première étape pour créer votre modèle consiste à lui attribuer un nom :</span><span class="sxs-lookup"><span data-stu-id="5f6e0-123">The first step to create your model is to give it a name:</span></span>

1. <span data-ttu-id="5f6e0-124">Dans le centre de contenu, sélectionnez **nouveau**, puis **créez un modèle**.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-124">From the Content Center, select **New**, and then **Create a model**.</span></span>
2. <span data-ttu-id="5f6e0-125">Dans le volet **nouveau modèle de présentation des documents** , dans le champ **nom** , tapez le nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-125">In the **New document understanding model** pane, in the **Name** field type the name of the model.</span></span> <span data-ttu-id="5f6e0-126">Par exemple, si vous souhaitez identifier les documents de renouvellement de contrat, vous pouvez nommer le modèle *renouvellement de contrat*.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-126">For example, if you want to identify contract renewal documents, you could name the model *Contract Renewal*.</span></span>
3. <span data-ttu-id="5f6e0-127">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-127">Choose **Create**.</span></span> <span data-ttu-id="5f6e0-128">Cela crée une page d’accueil pour le modèle.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-128">This creates a home page for the model.</span></span></br>

    ![Page d’accueil du modèle de classifieur](../media/content-understanding/model-home.png)

<span data-ttu-id="5f6e0-130">Lorsque vous créez un modèle, vous créez également un nouveau type de contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-130">When you create a model, you are also creating a new SharePoint content type.</span></span> <span data-ttu-id="5f6e0-131">Un type de contenu SharePoint représente une catégorie de documents qui ont des caractéristiques communes et qui partagent une collection de colonnes ou de propriétés de métadonnées pour ce contenu particulier.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-131">A SharePoint content type represents a category of documents that have common characteristics and share a collection of columns or metadata properties for that particular content.</span></span> <span data-ttu-id="5f6e0-132">Les types de contenu SharePoint sont gérés via la [Galerie de types de contenu](https://support.microsoft.com/office/create-or-customize-a-site-content-type-27eb6551-9867-4201-a819-620c5658a60f).</span><span class="sxs-lookup"><span data-stu-id="5f6e0-132">SharePoint Content Types are managed through the [Content types gallery](https://support.microsoft.com/office/create-or-customize-a-site-content-type-27eb6551-9867-4201-a819-620c5658a60f).</span></span> <span data-ttu-id="5f6e0-133">Pour cet exemple, lorsque vous créez le modèle, vous créez un nouveau type de contenu de *renouvellement de contrat* .</span><span class="sxs-lookup"><span data-stu-id="5f6e0-133">For this example, when you create the model, you are creating a new *Contract Renewal* content type.</span></span>

<span data-ttu-id="5f6e0-134">Sélectionnez **Paramètres avancés** si vous souhaitez mapper ce modèle à un type de contenu existant dans la Galerie de types de contenu SharePoint pour utiliser son schéma.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-134">Select **Advanced settings** if you want to map this model to an existing content type in the SharePoint Content types gallery to use its schema.</span></span> <span data-ttu-id="5f6e0-135">Notez que si vous pouvez utiliser un type de contenu existant pour tirer parti de son schéma afin de faciliter l’identification et la classification, vous devez tout de même former votre modèle pour extraire des informations des fichiers qu’il identifie.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-135">Note that while you can use an existing content type to leverage its schema to help with identification and classification, you still need to train your model to extract information from files it identifies.</span></span></br>

![Paramètres avancés](../media/content-understanding/advanced-settings.png)

## <a name="add-your-example-files"></a><span data-ttu-id="5f6e0-137">Ajouter vos exemples de fichiers</span><span class="sxs-lookup"><span data-stu-id="5f6e0-137">Add your example files</span></span>

<span data-ttu-id="5f6e0-138">Sur la page d’accueil du modèle, ajoutez vos exemples de fichiers dont vous aurez besoin pour former le modèle afin d’identifier votre type de document.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-138">On the model home page, add your examples files you will need to help train the model to identify your document type.</span></span> </br>
</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4D0iX] 

</br>

> [!NOTE]
> <span data-ttu-id="5f6e0-139">Vous devez utiliser les mêmes fichiers pour la formation des classifieurs et de l' [extracteur](create-an-extractor.md).</span><span class="sxs-lookup"><span data-stu-id="5f6e0-139">You should use the same files for both classifier and [extractor training](create-an-extractor.md).</span></span> <span data-ttu-id="5f6e0-140">Vous avez toujours la possibilité de l’ajouter plus tard, mais vous ajoutez généralement un ensemble complet de fichiers d’exemple.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-140">You always have the option to add more later, but typically you add a full set of sample files.</span></span> <span data-ttu-id="5f6e0-141">Étiquetez une partie pour former votre modèle et testez les autres pour évaluer la pertinence du modèle.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-141">Label some to train your model, and test the remaining unlabeled ones to evaluate model fitness.</span></span> 

<span data-ttu-id="5f6e0-142">Pour votre jeu de formation, vous voulez utiliser des exemples positifs et négatifs :</span><span class="sxs-lookup"><span data-stu-id="5f6e0-142">For your training set, you want to use both positive and negative examples:</span></span>
- <span data-ttu-id="5f6e0-143">Exemple positif : documents qui représentent le type de document.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-143">Positive example: Documents that represent the document type.</span></span> <span data-ttu-id="5f6e0-144">Elles contiennent des chaînes et des informations qui seraient toujours dans ce type de document.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-144">These contain strings and information that would always be in this type of document.</span></span>
- <span data-ttu-id="5f6e0-145">Exemple négatif : documents qui ne représentent pas le type de document.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-145">Negative example: Documents that do not represent the document type.</span></span> <span data-ttu-id="5f6e0-146">Il manque des chaînes et des informations qui doivent être présentes dans ce type de document.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-146">These are missing strings and information that needs to be present in this type of document.</span></span>

<span data-ttu-id="5f6e0-147">Veillez à utiliser au moins cinq exemples positifs et au moins un exemple négatif pour former votre modèle.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-147">Be sure to use at least five positive examples and at least one negative example to train your model.</span></span>  <span data-ttu-id="5f6e0-148">Vous souhaitez en créer d’autres pour tester votre modèle après le processus de formation.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-148">You want to create additional ones to test your model after the training process.</span></span>

<span data-ttu-id="5f6e0-149">Pour ajouter des fichiers d’exemple :</span><span class="sxs-lookup"><span data-stu-id="5f6e0-149">To add sample files:</span></span>

1. <span data-ttu-id="5f6e0-150">À partir de la page d’accueil du modèle, dans la vignette **créer un exemple de bibliothèque** , cliquez sur Ajouter des **fichiers**.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-150">From the model home page, in the **Build sample library** tile, click **Add files**.</span></span>
2. <span data-ttu-id="5f6e0-151">Sur la page **Sélectionner des fichiers d’exemple pour votre modèle** , sélectionnez vos exemples de fichiers dans la bibliothèque fichiers d’exemple dans le centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-151">On the **Select sample files for your model** page, select your example files from the Sample files library in the Content Center.</span></span> <span data-ttu-id="5f6e0-152">Si vous ne les avez pas déjà téléchargées, choisissez de les télécharger maintenant en cliquant sur **charger** pour les déplacer dans l’exemple de bibliothèque de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-152">If you had not already uploaded them there, choose to upload them now by clicking **Upload** to move them the Sample file library.</span></span>
3. <span data-ttu-id="5f6e0-153">Après avoir sélectionné vos exemples de fichiers à utiliser pour former le modèle, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-153">After selecting your example files to use to train the model, click **Add**.</span></span>

    ![Sélectionner des exemples de fichiers](../media/content-understanding/select-sample.png) 

## <a name="label-your-example-files"></a><span data-ttu-id="5f6e0-155">Étiqueter vos exemples de fichiers</span><span class="sxs-lookup"><span data-stu-id="5f6e0-155">Label your example files</span></span>

<span data-ttu-id="5f6e0-156">Après avoir ajouté vos fichiers d’exemple, vous devez les étiqueter en tant qu’exemples positifs ou négatifs.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-156">After adding your example files, you need to label them as either positive or negative examples.</span></span>

1. <span data-ttu-id="5f6e0-157">À partir de la page d’accueil du modèle, dans la vignette **classer les fichiers et exécuter la formation** , cliquez sur organiser le **classificateur**.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-157">From the model home page, on the **Classify files and run training** tile, click **Train Classifier**.</span></span>
   <span data-ttu-id="5f6e0-158">Ceci affiche la page étiquette qui affiche la liste de vos exemples de fichiers, avec le premier fichier visible dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-158">This displays the label page that shows a listing of your example files, with the first file visible in the viewer.</span></span>
2. <span data-ttu-id="5f6e0-159">Dans la visionneuse en haut du premier fichier d’exemple, vous devriez voir un texte vous demandant si le fichier est un exemple de modèle que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-159">In the viewer on the top of the first example file, you should see text asking if the file is an example of the model you just created.</span></span> <span data-ttu-id="5f6e0-160">S’il s’agit d’un exemple positif, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-160">If it is a positive example, select **Yes**.</span></span> <span data-ttu-id="5f6e0-161">S’il s’agit d’un exemple négatif, sélectionnez **non**.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-161">If it is a negative example, select **No**.</span></span>
3. <span data-ttu-id="5f6e0-162">Dans la liste des **exemples étiquetés** à gauche, sélectionnez les fichiers supplémentaires que vous souhaitez utiliser comme exemples, puis étiquetez-les.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-162">From the **Labeled examples** list on the left, select additional files that you want to use as examples, and label them.</span></span> 

    ![Page d’accueil du classifieur](../media/content-understanding/classifier-home-page.png) 


> [!NOTE]
> <span data-ttu-id="5f6e0-164">Étiquetez au moins cinq exemples positifs et un exemple négatif.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-164">Label at least five positive examples, and one negative example.</span></span> 

## <a name="create-an-explanation"></a><span data-ttu-id="5f6e0-165">Créer une explication</span><span class="sxs-lookup"><span data-stu-id="5f6e0-165">Create an explanation</span></span>

<span data-ttu-id="5f6e0-166">L’étape suivante consiste à créer une explication sur la page de formation.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-166">The next step is for you to create an explanation on the Train page.</span></span> <span data-ttu-id="5f6e0-167">Une explication aide le modèle à comprendre comment reconnaître le document.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-167">An explanation helps the model understand how to recognize the document.</span></span> <span data-ttu-id="5f6e0-168">Par exemple, les documents de renouvellement de contrat contiennent toujours une *demande de chaîne de texte de divulgation supplémentaire* .</span><span class="sxs-lookup"><span data-stu-id="5f6e0-168">For example, the Contract Renewal documents always contain a *Request for additional disclosure* text string.</span></span>

> [!Note]
> <span data-ttu-id="5f6e0-169">Lorsqu’il est utilisé avec des extracteurs, une explication identifie la chaîne que vous souhaitez extraire du document.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-169">When used with extractors, an explanation identifies the string that you want to extract from the document.</span></span> 

<span data-ttu-id="5f6e0-170">Pour créer une explication :</span><span class="sxs-lookup"><span data-stu-id="5f6e0-170">To create an explanation:</span></span>

1. <span data-ttu-id="5f6e0-171">À partir de la page d’accueil du modèle, sélectionnez l’onglet **train (apprentissage** ) pour accéder à la page de formation.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-171">From the model home page, select the **Train** tab to go to the Train page.</span></span>
2. <span data-ttu-id="5f6e0-172">Sur la page de formation, dans la section **fichiers formés** , vous devriez voir une liste des fichiers d’exemple que vous avez précédemment étiquetés.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-172">On the Train page, in the **Trained files** section you should see a list of the sample files that you previously labeled.</span></span> <span data-ttu-id="5f6e0-173">Sélectionnez un des fichiers positifs dans la liste et affichez-le dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-173">Select one of the positive files from the list, and it displays in the viewer.</span></span>
3. <span data-ttu-id="5f6e0-174">Dans la section explication, sélectionnez **nouveau** , puis **vide**.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-174">In the Explanation section, select **New** and then **Blank**.</span></span>
4. <span data-ttu-id="5f6e0-175">Sur la page **créer une explication** :</span><span class="sxs-lookup"><span data-stu-id="5f6e0-175">On the **Create an explanation** page:</span></span></br>
    <span data-ttu-id="5f6e0-176">a.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-176">a.</span></span> <span data-ttu-id="5f6e0-177">Tapez le **nom** (par exemple, « bloc de divulgation »).</span><span class="sxs-lookup"><span data-stu-id="5f6e0-177">Type the **Name** (for example, "Disclosure Block").</span></span></br>
    <span data-ttu-id="5f6e0-178">b.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-178">b.</span></span> <span data-ttu-id="5f6e0-179">Sélectionnez le **type**.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-179">Select the **Type**.</span></span> <span data-ttu-id="5f6e0-180">Pour l’exemple, sélectionnez **liste des expressions**, étant donné que vous ajoutez une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-180">For the sample, select **Phrase list**, since you add a text string.</span></span></br>
    <span data-ttu-id="5f6e0-181">c.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-181">c.</span></span> <span data-ttu-id="5f6e0-182">Dans la zone **Tapez ici** , tapez la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-182">In the **Type here** box, type the string.</span></span> <span data-ttu-id="5f6e0-183">Pour l’exemple, ajoutez « demande d’informations supplémentaires ».</span><span class="sxs-lookup"><span data-stu-id="5f6e0-183">For the sample, add "Request for additional disclosure".</span></span> <span data-ttu-id="5f6e0-184">Vous **pouvez sélectionner respecter la casse si** la chaîne doit respecter la casse.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-184">You can select **Case sensitive** if the string needs to be case sensitive.</span></span></br>
    <span data-ttu-id="5f6e0-185">d.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-185">d.</span></span> <span data-ttu-id="5f6e0-186">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-186">Click **Save**.</span></span>

    ![Créer une explication](../media/content-understanding/explanation.png) 
    
 
5. <span data-ttu-id="5f6e0-188">Le modèle vérifie désormais si l’explication que vous avez créée était suffisante pour identifier correctement les fichiers d’exemple étiquetés restants, comme des exemples positifs et négatifs.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-188">The model now checks to see if the explanation you created was good enough to identify the remaining labeled example files correctly, as positive and negative examples.</span></span> <span data-ttu-id="5f6e0-189">Dans la section fichiers formés, vérifiez la colonne **évaluation** une fois la formation terminée pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-189">In the Trained Files section, check the **Evaluation** column after the training has completed to see the results.</span></span> <span data-ttu-id="5f6e0-190">Les fichiers affichent une valeur de **correspondance**, si les explications que vous avez créées étaient suffisantes pour correspondre à ce que vous avez étiqueté positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-190">The files show a value of **Match**, if the explanations you created was enough to match what you labeled as positive or negative.</span></span>

    ![Valeur de la correspondance](../media/content-understanding/match.png) 

<span data-ttu-id="5f6e0-192">Si vous recevez une **incompatibilité** sur les fichiers étiquetés, vous devrez peut-être créer une explication supplémentaire pour fournir au modèle plus d’informations afin d’identifier le type de document.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-192">If you receive a **Mismatch** on the labeled files, you may need to create an additional explanation to provide the model more information to identify the document type.</span></span> <span data-ttu-id="5f6e0-193">Dans ce cas, cliquez sur le fichier pour obtenir plus d’informations sur la raison de l’incompatibilité.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-193">If this happens, click on the file to get more information about why the mismatch occurred.</span></span>

## <a name="test-your-model"></a><span data-ttu-id="5f6e0-194">Tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="5f6e0-194">Test your model</span></span>

<span data-ttu-id="5f6e0-195">Si vous avez reçu une correspondance sur vos fichiers d’exemple étiquetés, vous pouvez maintenant tester votre modèle sur vos fichiers d’exemple sans étiquette restants.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-195">If you received a match on your labeled sample files, you can now test your model on your remaining unlabeled example files.</span></span>

1. <span data-ttu-id="5f6e0-196">À partir de la page d’accueil du modèle, sélectionnez l’onglet **test** .  Cela exécute le modèle sur vos fichiers d’exemple non labellisés.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-196">From the model home page, select the **Test** tab.  This runs the model on your unlabeled sample files.</span></span>
2. <span data-ttu-id="5f6e0-197">Dans la liste des **fichiers test** , vos exemples de fichiers affichent et indiquent si le modèle a déterminé qu’il soit positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-197">In the **Test files** list, your example files display and shows if the model predicted them to be positive or negative.</span></span> <span data-ttu-id="5f6e0-198">Utilisez ces informations pour vous aider à déterminer l’efficacité de votre classifieur lors de l’identification de vos documents.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-198">Use this information to help determine the effectiveness of your classifier in identifying your documents.</span></span>

    ![Test des fichiers non labellisés](../media/content-understanding/test-on-files.png) 

## <a name="see-also"></a><span data-ttu-id="5f6e0-200">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f6e0-200">See Also</span></span>
[<span data-ttu-id="5f6e0-201">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="5f6e0-201">Create an extractor</span></span>](create-an-extractor.md)</br>
[<span data-ttu-id="5f6e0-202">Présentation de l’explication des documents</span><span class="sxs-lookup"><span data-stu-id="5f6e0-202">Document Understanding overview</span></span>](document-understanding-overview.md)</br>
[<span data-ttu-id="5f6e0-203">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="5f6e0-203">Create a form processing model</span></span>](create-a-form-processing-model.md)</br>
[<span data-ttu-id="5f6e0-204">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="5f6e0-204">Apply a model</span></span>](apply-a-model.md) 
