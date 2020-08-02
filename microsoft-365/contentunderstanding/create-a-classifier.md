---
title: Créer un classifieur (aperçu)
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.service: ''
search.appverid: ''
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
description: En savoir plus sur la création d’un classifieur
ms.openlocfilehash: 029ac16310f8e95a69a713896b1109a778eb3b8d
ms.sourcegitcommit: ea5e2f85bd6b609658545b120c7e08789b9686fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/01/2020
ms.locfileid: "46537221"
---
# <a name="create-a-classifier-preview"></a><span data-ttu-id="e21ec-103">Créer un classifieur (aperçu)</span><span class="sxs-lookup"><span data-stu-id="e21ec-103">Create a classifier (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="e21ec-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="e21ec-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="e21ec-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="e21ec-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CL0R]  

</br>

<span data-ttu-id="e21ec-106">Un classifieur est un type de modèle qui automatise l’identification et la classification d’un type de document.</span><span class="sxs-lookup"><span data-stu-id="e21ec-106">A classifier is a type of model that automates identification and classification of a document type.</span></span> <span data-ttu-id="e21ec-107">Par exemple, vous pouvez identifier tous les documents de *renouvellement de contrat* ajoutés à votre bibliothèque de documents, tels que les suivants.</span><span class="sxs-lookup"><span data-stu-id="e21ec-107">For example, you may want to identify all *Contract Renewal* documents that are added to your document library, such as the following.</span></span>

![Document de renouvellement de contrat](../media/content-understanding/contract-renewal.png)

<span data-ttu-id="e21ec-109">La création d’un classifieur crée un nouveau [type de contenu SharePoint](https://docs.microsoft.com/sharepoint/governance/content-type-and-workflow-planning#content-type-overview) qui sera associé au modèle.</span><span class="sxs-lookup"><span data-stu-id="e21ec-109">Creating a classifier will create a new [SharePoint Content Type](https://docs.microsoft.com/sharepoint/governance/content-type-and-workflow-planning#content-type-overview) that will be associated to the model.</span></span>

<span data-ttu-id="e21ec-110">Lors de la création du classifieur, vous devez créer des *explications* qui permettent de définir le modèle en notant les données courantes que vous prévoyez de trouver de manière cohérente pour ce type de document.</span><span class="sxs-lookup"><span data-stu-id="e21ec-110">When creating the classifier, you need to create *explanations* that help to define the model by noting common data that you would expect to find consistently for this document type.</span></span> 

<span data-ttu-id="e21ec-111">Vous utilisez des exemples de type de document (« exemples de fichiers ») pour aider à « former » votre modèle afin d’identifier les fichiers qui ont le même type de contenu.</span><span class="sxs-lookup"><span data-stu-id="e21ec-111">You use examples of the document type ("example files") to help "train" your model to identify files that have the same content type.</span></span>

<span data-ttu-id="e21ec-112">Pour créer un classifieur, vous devez :</span><span class="sxs-lookup"><span data-stu-id="e21ec-112">To create a classifier, you need to:</span></span>
1. <span data-ttu-id="e21ec-113">Nommer votre modèle</span><span class="sxs-lookup"><span data-stu-id="e21ec-113">Name your model</span></span>
2. <span data-ttu-id="e21ec-114">Ajouter vos exemples de fichiers</span><span class="sxs-lookup"><span data-stu-id="e21ec-114">Add your example files</span></span>
3. <span data-ttu-id="e21ec-115">Étiqueter vos exemples de fichiers</span><span class="sxs-lookup"><span data-stu-id="e21ec-115">Label your example files</span></span>
4. <span data-ttu-id="e21ec-116">Créer une explication</span><span class="sxs-lookup"><span data-stu-id="e21ec-116">Create an explanation</span></span>
5. <span data-ttu-id="e21ec-117">Tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="e21ec-117">Test your model</span></span> 

> [!Note]
> <span data-ttu-id="e21ec-118">Alors qu’un classifieur est utilisé par votre modèle pour identifier et classer les types de documents, vous pouvez également choisir d’extraire des informations spécifiques de chaque fichier identifié par le modèle.</span><span class="sxs-lookup"><span data-stu-id="e21ec-118">While a classifier is used by your model to identify and classify document types, you can also choose to pull specific pieces of information from each file identified by the model.</span></span> <span data-ttu-id="e21ec-119">Pour ce faire, vous devez créer un **extracteur** à ajouter à votre modèle, ce qui est décrit dans [Create an Extractor](create-an-extractor.md).</span><span class="sxs-lookup"><span data-stu-id="e21ec-119">You do this by creating an **extractor** to add to your model, and this is described in [Create an extractor](create-an-extractor.md).</span></span>

## <a name="name-your-model"></a><span data-ttu-id="e21ec-120">Nommer votre modèle</span><span class="sxs-lookup"><span data-stu-id="e21ec-120">Name your model</span></span>

<span data-ttu-id="e21ec-121">La première étape consiste à créer votre modèle dans votre centre de contenu en lui attribuant un nom :</span><span class="sxs-lookup"><span data-stu-id="e21ec-121">The first step is to create your model in your Content Center by giving it a name:</span></span>

1. <span data-ttu-id="e21ec-122">Dans votre centre de contenu, cliquez sur **nouveau**, puis sur **créer un modèle**.</span><span class="sxs-lookup"><span data-stu-id="e21ec-122">In your Content Center, click **New**, and then click **Create a model**.</span></span>
2. <span data-ttu-id="e21ec-123">Dans le volet **nouveau modèle de présentation des documents** , dans le champ **nom** , tapez le nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="e21ec-123">In the **New document understanding model** pane, in the **Name** field, type the name of the model.</span></span> <span data-ttu-id="e21ec-124">Pour notre exemple, si nous voulons identifier les documents de renouvellement de contrat, nous pouvons nommer ce modèle *renouvellement de contrat*.</span><span class="sxs-lookup"><span data-stu-id="e21ec-124">For our example, if we want to identify contract renewal documents, we might name this model *Contract Renewal*.</span></span>
3. <span data-ttu-id="e21ec-125">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="e21ec-125">Click **Create**.</span></span> <span data-ttu-id="e21ec-126">Cette opération crée une page d’accueil pour le modèle.</span><span class="sxs-lookup"><span data-stu-id="e21ec-126">This will create a home page for the model.</span></span></br>

    ![Page d’accueil du modèle de classifieur](../media/content-understanding/model-home.png)

<span data-ttu-id="e21ec-128">Lorsque vous créez un modèle, vous créez un nouveau type de contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e21ec-128">When you create a model, you are creating a new SharePoint content type.</span></span> <span data-ttu-id="e21ec-129">Un type de contenu SharePoint représente une catégorie de documents qui ont des caractéristiques communes et qui partagent une collection de colonnes ou de propriétés de métadonnées pour ce contenu particulier.</span><span class="sxs-lookup"><span data-stu-id="e21ec-129">A SharePoint content type represents a category of documents that have common characteristics and share a collection of columns or metadata properties for that particular content.</span></span> <span data-ttu-id="e21ec-130">Les types de contenu SharePoint sont gérés via la [Galerie de types de contenu]().</span><span class="sxs-lookup"><span data-stu-id="e21ec-130">SharePoint Content Types are managed through the [Content types gallery]().</span></span> <span data-ttu-id="e21ec-131">Pour notre exemple, lorsque nous créons le modèle, nous allons créer un nouveau type de contenu de *renouvellement de contrat* .</span><span class="sxs-lookup"><span data-stu-id="e21ec-131">For our example, when we create the model, we will be creating a new *Contract Renewal* content type.</span></span>

<span data-ttu-id="e21ec-132">Sélectionnez **Paramètres avancés** si vous souhaitez mapper ce modèle à un type de contenu existant dans la Galerie de types de contenu SharePoint pour utiliser son schéma.</span><span class="sxs-lookup"><span data-stu-id="e21ec-132">Select **Advanced settings** if you want to map this model to an existing content type in the SharePoint Content types gallery to use its schema.</span></span> <span data-ttu-id="e21ec-133">Notez que même si vous pouvez utiliser un type de contenu existant pour tirer parti de son schéma afin de faciliter l’identification et la classification, vous devrez tout de même former votre modèle pour extraire des informations des fichiers qu’il identifie.</span><span class="sxs-lookup"><span data-stu-id="e21ec-133">Note that while you can use an existing content type to leverage its schema to help with identification and classification, you will still need to train your model to extract information from files it identifies.</span></span></br>

![Paramètres avancés](../media/content-understanding/advanced-settings.png)

## <a name="add-your-example-files"></a><span data-ttu-id="e21ec-135">Ajouter vos exemples de fichiers</span><span class="sxs-lookup"><span data-stu-id="e21ec-135">Add your example files</span></span>

<span data-ttu-id="e21ec-136">Sur la page d’accueil du modèle, vous pouvez ajouter vos exemples de fichiers dont vous aurez besoin pour former le modèle afin d’identifier votre type de document.</span><span class="sxs-lookup"><span data-stu-id="e21ec-136">On the model home page, you can add your examples files you will need to help train the model to identify your document type.</span></span> </br>
</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4D0iX] 

</br>

> [!Note]
> <span data-ttu-id="e21ec-137">Les mêmes fichiers doivent être utilisés pour la formation des classifieurs et de l' [extracteur](create-an-extractor.md).</span><span class="sxs-lookup"><span data-stu-id="e21ec-137">The same files should be used for both classifier and [extractor training](create-an-extractor.md).</span></span> <span data-ttu-id="e21ec-138">Vous avez toujours la possibilité d’ajouter plus tard, mais vous devez généralement ajouter un ensemble complet de fichiers d’exemple.</span><span class="sxs-lookup"><span data-stu-id="e21ec-138">You always have the option to add more later, but typically you should add a full set of example files.</span></span> <span data-ttu-id="e21ec-139">Vous allez étiqueter certaines pour former votre modèle et tester les autres non libellés afin d’évaluer la pertinence du modèle.</span><span class="sxs-lookup"><span data-stu-id="e21ec-139">You will label some to train your model, and test the remaining unlabeled ones to evaluate model fitness.</span></span> 

<span data-ttu-id="e21ec-140">Pour votre jeu de formation, vous pouvez utiliser des exemples positifs et des exemples négatifs :</span><span class="sxs-lookup"><span data-stu-id="e21ec-140">For your training set, you will want to use both positive examples, and negative examples:</span></span>
- <span data-ttu-id="e21ec-141">Exemple positif : documents qui représentent le type de document.</span><span class="sxs-lookup"><span data-stu-id="e21ec-141">Positive example: Documents that represent the document type.</span></span> <span data-ttu-id="e21ec-142">Elles contiennent des chaînes et des informations qui seraient toujours dans ce type de document.</span><span class="sxs-lookup"><span data-stu-id="e21ec-142">They contain strings and information that would always be in this type of document.</span></span>
- <span data-ttu-id="e21ec-143">Exemple négatif : documents qui ne représentent pas le type de document.</span><span class="sxs-lookup"><span data-stu-id="e21ec-143">Negative example: Documents that do not represent the document type.</span></span>  <span data-ttu-id="e21ec-144">Il manque des chaînes et des informations qui doivent être présentes dans ce type de document.</span><span class="sxs-lookup"><span data-stu-id="e21ec-144">They are missing strings and information that needs to be present in this type of document.</span></span>

<span data-ttu-id="e21ec-145">Vous pouvez utiliser au moins cinq exemples positifs et un exemple négatif pour former votre modèle.</span><span class="sxs-lookup"><span data-stu-id="e21ec-145">You will want to use at least five positive examples and one negative examples to train your model.</span></span>  <span data-ttu-id="e21ec-146">Vous aurez besoin d’autres pour tester votre modèle après la formation.</span><span class="sxs-lookup"><span data-stu-id="e21ec-146">You will want to have additional ones to test your model after training.</span></span>

<span data-ttu-id="e21ec-147">Pour ajouter des fichiers d’exemple :</span><span class="sxs-lookup"><span data-stu-id="e21ec-147">To add sample files:</span></span>

1. <span data-ttu-id="e21ec-148">Sur la page d’accueil du modèle, dans la vignette **créer un exemple de bibliothèque** , cliquez sur Ajouter des **fichiers**.</span><span class="sxs-lookup"><span data-stu-id="e21ec-148">On the model home page, in the **Build sample library** tile, click **Add files**.</span></span>
2. <span data-ttu-id="e21ec-149">Sur la page **Sélectionner des fichiers d’exemple pour votre modèle** , sélectionnez vos exemples de fichiers dans la bibliothèque fichiers d’exemple dans le centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="e21ec-149">On the **Select sample files for your model** page, select your example files from the Sample files library in the Content Center.</span></span> <span data-ttu-id="e21ec-150">Si vous ne les avez pas déjà téléchargées à cet emplacement, vous pouvez choisir de les télécharger maintenant en cliquant sur **charger** pour les déplacer dans l’exemple de bibliothèque de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e21ec-150">If you had not already uploaded them there, you can choose to upload them now by clicking **Upload** to move them the Sample file library.</span></span>
3. <span data-ttu-id="e21ec-151">Après avoir sélectionné vos exemples de fichiers à utiliser pour former le modèle, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e21ec-151">After selecting your example files to use to train the model, click **Add**.</span></span>

    ![Sélectionner des exemples de fichiers](../media/content-understanding/select-sample.png) 

## <a name="label-your-example-files"></a><span data-ttu-id="e21ec-153">Étiqueter vos exemples de fichiers</span><span class="sxs-lookup"><span data-stu-id="e21ec-153">Label your example files</span></span>

<span data-ttu-id="e21ec-154">Après avoir ajouté vos exemples de fichiers, vous devez les étiqueter en tant qu’exemples positifs ou en tant qu’exemples négatifs.</span><span class="sxs-lookup"><span data-stu-id="e21ec-154">After adding your example files, you then need to label them as either positive examples or negative examples.</span></span>

1. <span data-ttu-id="e21ec-155">Sur la page d’accueil du modèle, dans la vignette **classer les fichiers et exécuter la formation** , cliquez sur organiser le **classificateur**.</span><span class="sxs-lookup"><span data-stu-id="e21ec-155">On the model home page, on the **Classify files and run training** tile, click **Train Classifier**.</span></span>
   <span data-ttu-id="e21ec-156">Cette opération affiche la page étiquette qui affiche la liste de vos exemples de fichiers, avec le premier fichier visible dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="e21ec-156">This will display the label page that shows a listing of your example files, with the first file visible in the viewer.</span></span>
2. <span data-ttu-id="e21ec-157">Dans la visionneuse, dans la partie supérieure du premier fichier, vous verrez si le fichier est un exemple de modèle que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="e21ec-157">In the viewer, on the top of the first example file, you will see text asking you if the file is an example of the model you just created.</span></span> <span data-ttu-id="e21ec-158">S’il s’agit d’un exemple positif, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="e21ec-158">If it is a positive example, select **Yes**.</span></span> <span data-ttu-id="e21ec-159">S’il s’agit d’un exemple négatif, sélectionnez **non**.</span><span class="sxs-lookup"><span data-stu-id="e21ec-159">If it is a negative example, select **No**.</span></span>
3. <span data-ttu-id="e21ec-160">Dans la liste des **exemples étiquetés** à gauche, sélectionnez les fichiers supplémentaires que vous souhaitez utiliser comme exemples, et étiquetez-les également.</span><span class="sxs-lookup"><span data-stu-id="e21ec-160">From the **Labeled examples** list on the left, select additional files that you want to use as examples, and label them as well.</span></span> 

    ![Page d’accueil du modèle de classifieur](../media/content-understanding/classifier-home-page.png) 


> [!Note]
> <span data-ttu-id="e21ec-162">Étiquetez au moins cinq exemples positifs et un exemple négatif.</span><span class="sxs-lookup"><span data-stu-id="e21ec-162">Label at least five positive examples, and one negative example.</span></span> 

## <a name="create-an-explanation"></a><span data-ttu-id="e21ec-163">Créer une explication</span><span class="sxs-lookup"><span data-stu-id="e21ec-163">Create an explanation</span></span>

<span data-ttu-id="e21ec-164">L’étape suivante consiste à créer une explication sur la page de formation.</span><span class="sxs-lookup"><span data-stu-id="e21ec-164">The next step is to create an explanation on the Train page.</span></span>  <span data-ttu-id="e21ec-165">Une explication est une indication ou un indice destiné à aider le modèle à comprendre comment reconnaître ce document.</span><span class="sxs-lookup"><span data-stu-id="e21ec-165">An explanation is a hint or clue to help the model understand how to recognize this document.</span></span> <span data-ttu-id="e21ec-166">Par exemple, nos documents de renouvellement de contrat contiennent toujours une *demande pour une chaîne de texte de divulgation supplémentaire* .</span><span class="sxs-lookup"><span data-stu-id="e21ec-166">For example, our Contract Renewal documents always contain a *Request for additional disclosure* text string.</span></span>

> [!Note]
> <span data-ttu-id="e21ec-167">Lorsqu’il est utilisé avec des extracteurs, une explication est utilisée pour identifier la chaîne que vous souhaitez extraire du document.</span><span class="sxs-lookup"><span data-stu-id="e21ec-167">When used with extractors, an explanation is use to identify the string that you want to extract from the document.</span></span> 

<span data-ttu-id="e21ec-168">Pour créer une explication :</span><span class="sxs-lookup"><span data-stu-id="e21ec-168">To create an explanation:</span></span>

1. <span data-ttu-id="e21ec-169">Sur la page d’accueil du modèle, cliquez sur l’onglet **train** pour accéder à la page de formation.</span><span class="sxs-lookup"><span data-stu-id="e21ec-169">On the model home page, click the **Train** tab to go to the Train page.</span></span>
2. <span data-ttu-id="e21ec-170">Sur la page train, dans la section **fichiers formés** , vous verrez une liste des exemples de fichiers que vous avez étiquetés précédemment.</span><span class="sxs-lookup"><span data-stu-id="e21ec-170">On the Train page, in the **Trained files** section, you will see a list of the example files that you had labeled previously.</span></span> <span data-ttu-id="e21ec-171">Sélectionnez un de vos fichiers positifs dans la liste, qui s’affichera dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="e21ec-171">Select one of your positive files from the list, and it will display in the viewer.</span></span>
3. <span data-ttu-id="e21ec-172">Dans la section explication, cliquez sur **nouveau**, puis sur **vide**.</span><span class="sxs-lookup"><span data-stu-id="e21ec-172">In the Explanation section, click **New**, then click **Blank**.</span></span>
4. <span data-ttu-id="e21ec-173">Sur la page **créer une explication** :</span><span class="sxs-lookup"><span data-stu-id="e21ec-173">On the **Create an explanation** page:</span></span></br>
    <span data-ttu-id="e21ec-174">a.</span><span class="sxs-lookup"><span data-stu-id="e21ec-174">a.</span></span> <span data-ttu-id="e21ec-175">Tapez le **nom** (par exemple, « bloc de divulgation »).</span><span class="sxs-lookup"><span data-stu-id="e21ec-175">Type the **Name** (for example, "Disclosure Block").</span></span></br>
    <span data-ttu-id="e21ec-176">b.</span><span class="sxs-lookup"><span data-stu-id="e21ec-176">b.</span></span> <span data-ttu-id="e21ec-177">Sélectionnez le **type**.</span><span class="sxs-lookup"><span data-stu-id="e21ec-177">Select the **Type**.</span></span> <span data-ttu-id="e21ec-178">Pour notre exemple, nous allons sélectionner **expression List**, étant donné que nous ajoutons une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="e21ec-178">For our example, we'll select **Phrase list**, since we are adding a text string.</span></span></br>
    <span data-ttu-id="e21ec-179">c.</span><span class="sxs-lookup"><span data-stu-id="e21ec-179">c.</span></span> <span data-ttu-id="e21ec-180">Dans la zone **Tapez ici** , tapez la chaîne.</span><span class="sxs-lookup"><span data-stu-id="e21ec-180">In the **Type here** box, type the string.</span></span>  <span data-ttu-id="e21ec-181">Pour notre exemple, nous allons ajouter « demande d’informations supplémentaires ».</span><span class="sxs-lookup"><span data-stu-id="e21ec-181">For our example, we'll add "Request for additional disclosure".</span></span> <span data-ttu-id="e21ec-182">Vous **pouvez sélectionner respecter la casse si** la chaîne doit respecter la casse.</span><span class="sxs-lookup"><span data-stu-id="e21ec-182">You can select **Case sensitive** if the string needs to be case sensitive.</span></span></br>
    <span data-ttu-id="e21ec-183">d.</span><span class="sxs-lookup"><span data-stu-id="e21ec-183">d.</span></span> <span data-ttu-id="e21ec-184">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e21ec-184">Click **Save**.</span></span>

    ![Créer une explication](../media/content-understanding/explanation.png) 
    
 
5.  <span data-ttu-id="e21ec-186">Le modèle vérifie que l’explication que vous avez créée est suffisante pour identifier correctement les fichiers d’exemple étiquetés restants en tant qu’exemples positifs et négatifs.</span><span class="sxs-lookup"><span data-stu-id="e21ec-186">The model will now check to see if the explanation you created was good enough to identify your remaining labeled example files correctly as positive and negative examples.</span></span> <span data-ttu-id="e21ec-187">Dans la section fichiers formés, vérifiez la colonne **évaluation** une fois la formation terminée pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="e21ec-187">In Trained Files section, check the **Evaluation** column after the training has completed to see the results.</span></span>  <span data-ttu-id="e21ec-188">Les fichiers affichent une valeur de **correspondance** si l’explication que vous avez créée est suffisante pour faire correspondre ce que vous avez étiqueté (positif ou négatif).</span><span class="sxs-lookup"><span data-stu-id="e21ec-188">The files will show a value of **Match** if the explanation you created was enough to match what you had labeled them as (positive or negative).</span></span>

    ![Créer une explication](../media/content-understanding/match.png) 

<span data-ttu-id="e21ec-190">Si vous recevez une **incompatibilité** avec vos fichiers étiquetés, vous devrez peut-être créer une explication supplémentaire pour fournir au modèle plus d’informations afin d’identifier le type de document.</span><span class="sxs-lookup"><span data-stu-id="e21ec-190">If you receive a **Mismatch** on your labeled files, you may need to create an additional explanation to provide the model more information to identify the document type.</span></span> <span data-ttu-id="e21ec-191">Vous pouvez cliquer sur le fichier pour obtenir plus d’informations sur la raison de l’incompatibilité.</span><span class="sxs-lookup"><span data-stu-id="e21ec-191">You can click on the file to get more information about why the mismatch occurred.</span></span>

## <a name="test-your-model"></a><span data-ttu-id="e21ec-192">Tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="e21ec-192">Test your model</span></span>

<span data-ttu-id="e21ec-193">Si vous avez reçu une correspondance sur vos exemples de fichiers étiquetés, vous pouvez maintenant tester votre modèle sur vos fichiers d’exemple sans étiquette restants.</span><span class="sxs-lookup"><span data-stu-id="e21ec-193">If you received a match on your labeled example files, you can now test your model on your remaining unlabeled example files.</span></span>

1. <span data-ttu-id="e21ec-194">Sur la page d’accueil du modèle, cliquez sur l’onglet **test** .  Cette opération exécutera le modèle sur vos fichiers d’exemple sans étiquette.</span><span class="sxs-lookup"><span data-stu-id="e21ec-194">On the model home page, click the **Test** tab.  This will run the model on your unlabeled example files.</span></span>
2. <span data-ttu-id="e21ec-195">Dans la liste des **fichiers de test** , vos exemples de fichiers s’afficheront et s’afficheront si le modèle prévoit des exemples positifs ou négatifs.</span><span class="sxs-lookup"><span data-stu-id="e21ec-195">In the **Test files** list, your example files will display and will show if the model predicted them to be positive or negative examples.</span></span> <span data-ttu-id="e21ec-196">Vous pouvez utiliser ces informations pour déterminer l’efficacité de votre classifieur lors de l’identification de vos documents.</span><span class="sxs-lookup"><span data-stu-id="e21ec-196">You can use this information to help determine the effectiveness of your classifier in identifying your documents.</span></span>

    ![Test des fichiers non labellisés](../media/content-understanding/test-on-files.png) 



## <a name="see-also"></a><span data-ttu-id="e21ec-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e21ec-198">See Also</span></span>
[<span data-ttu-id="e21ec-199">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="e21ec-199">Create an extractor</span></span>](create-an-extractor.md)</br>
[<span data-ttu-id="e21ec-200">Présentation de l’explication des documents</span><span class="sxs-lookup"><span data-stu-id="e21ec-200">Document Understanding overview</span></span>](document-understanding-overview.md)</br>
[<span data-ttu-id="e21ec-201">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="e21ec-201">Create a form processing model</span></span>](create-a-form-processing-model.md)</br>
[<span data-ttu-id="e21ec-202">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="e21ec-202">Apply a model</span></span>](apply-a-model.md) 




