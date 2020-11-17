---
title: Créer un classifieur
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: enabler-strategic
localization_priority: Priority
description: Découvrez comment créer un classifieur
ms.openlocfilehash: 478b4253f7bb888323c2a873f3ab295cc841e193
ms.sourcegitcommit: e7bf23df4852b78912229d1d38ec475223597f34
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "49087678"
---
# <a name="create-a-classifier-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="ac1ea-103">Créer un classifieur dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="ac1ea-103">Create a classifier in Microsoft SharePoint Syntex</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CL0R]  

</br>

<span data-ttu-id="ac1ea-104">Un classifieur est un type de modèle permettant d’automatiser l’identification et la classification d’un type de document.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-104">A classifier is a type of model that you can use to automate identification and classification of a document type.</span></span> <span data-ttu-id="ac1ea-105">Par exemple, vous devez parfois identifier tous les documents *Renouvellement de contrat* ajoutés à votre bibliothèque de documents, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-105">For example, you may want to identify all *Contract Renewal* documents that are added to your document library, such as is shown in the following illustration.</span></span>

![Document Renouvellement de contrat](../media/content-understanding/contract-renewal.png)

<span data-ttu-id="ac1ea-107">La création d’un classifieur vous permet de créer un [type de contenu SharePoint](https://docs.microsoft.com/sharepoint/governance/content-type-and-workflow-planning#content-type-overview) qui sera associé au modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-107">Creating a classifier enables you to create a new [SharePoint content type](https://docs.microsoft.com/sharepoint/governance/content-type-and-workflow-planning#content-type-overview) that will be associated to the model.</span></span>

<span data-ttu-id="ac1ea-108">Lors de la création du classifieur, vous devez créer des *explications* pour définir le modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-108">When creating the classifier, you need to create *explanations* to define the model.</span></span> <span data-ttu-id="ac1ea-109">Cela vous permet de noter les données courantes nécessaires pour trouver systématiquement ce type de document.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-109">This enables you to note common data that you would expect to consistently find this document type.</span></span> 

<span data-ttu-id="ac1ea-110">Utilisez des exemples de type de document (« exemples de fichiers ») pour « entraîner » votre modèle à identifier les fichiers qui ont le même type de contenu.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-110">Use examples of the document type ("example files") to "train" your model to identify files that have the same content type.</span></span>

<span data-ttu-id="ac1ea-111">Pour créer un classifieur, vous devez :</span><span class="sxs-lookup"><span data-stu-id="ac1ea-111">To create a classifier, you need to:</span></span>
1. <span data-ttu-id="ac1ea-112">Nommer votre modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-112">Name your model.</span></span>
2. <span data-ttu-id="ac1ea-113">Ajouter vos exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-113">Add your example files.</span></span>
3. <span data-ttu-id="ac1ea-114">Étiqueter vos exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-114">Label your example files.</span></span>
4. <span data-ttu-id="ac1ea-115">Créer une explication.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-115">Create an explanation.</span></span>
5. <span data-ttu-id="ac1ea-116">Tester votre modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-116">Test your model.</span></span>

> [!NOTE]
> <span data-ttu-id="ac1ea-117">Bien que votre modèle utilise un classifieur pour identifier et classifier des types de documents, vous pouvez également choisir d’extraire des informations spécifiques de chaque fichier identifié par le modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-117">While your model uses a classifier to identify and classify document types, you can also choose to pull specific pieces of information from each file identified by the model.</span></span> <span data-ttu-id="ac1ea-118">Pour ce faire, créez un **extracteur** à ajouter à votre modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-118">Do this by creating an **extractor** to add to your model.</span></span> <span data-ttu-id="ac1ea-119">Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Créer un extracteur](create-an-extractor.md).</span><span class="sxs-lookup"><span data-stu-id="ac1ea-119">See [Create an extractor](create-an-extractor.md).</span></span>

## <a name="name-your-model"></a><span data-ttu-id="ac1ea-120">Nommer votre modèle</span><span class="sxs-lookup"><span data-stu-id="ac1ea-120">Name your model</span></span>

<span data-ttu-id="ac1ea-121">La première étape de création de votre modèle consiste à lui attribuer un nom :</span><span class="sxs-lookup"><span data-stu-id="ac1ea-121">The first step to create your model is to give it a name:</span></span>

1. <span data-ttu-id="ac1ea-122">Dans le centre de contenu, sélectionnez **Nouveau**, puis **Créer un modèle**.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-122">From the content center, select **New**, and then **Create a model**.</span></span>
2. <span data-ttu-id="ac1ea-123">Dans le volet **Nouveau modèle de compréhension de document**, renseignez le champ **Nom** avec le nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-123">In the **New document understanding model** pane, in the **Name** field type the name of the model.</span></span> <span data-ttu-id="ac1ea-124">Par exemple, si vous souhaitez identifier les documents de renouvellement de contrat, vous pouvez nommer le modèle *Renouvellement de contrat*.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-124">For example, if you want to identify contract renewal documents, you could name the model *Contract Renewal*.</span></span>
3. <span data-ttu-id="ac1ea-125">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-125">Choose **Create**.</span></span> <span data-ttu-id="ac1ea-126">Cette opération permet de créer une page d’accueil pour le modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-126">This creates a home page for the model.</span></span></br>

    ![Page d’accueil du modèle de classifieur](../media/content-understanding/model-home.png)

<span data-ttu-id="ac1ea-128">La création d’un modèle entraîne également celle d’un type de contenu de site.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-128">When you create a model, you are also creating a new site content type.</span></span> <span data-ttu-id="ac1ea-129">Un type de contenu représente une catégorie de documents qui ont des caractéristiques communes et qui partagent une collection de colonnes ou de propriétés de métadonnées pour ce contenu spécifique.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-129">A content type represents a category of documents that have common characteristics and share a collection of columns or metadata properties for that particular content.</span></span> <span data-ttu-id="ac1ea-130">Les types de contenu SharePoint sont gérés via la [galerie des types de contenu](https://support.microsoft.com/office/create-or-customize-a-site-content-type-27eb6551-9867-4201-a819-620c5658a60f).</span><span class="sxs-lookup"><span data-stu-id="ac1ea-130">SharePoint content types are managed through the [Content types gallery](https://support.microsoft.com/office/create-or-customize-a-site-content-type-27eb6551-9867-4201-a819-620c5658a60f).</span></span> <span data-ttu-id="ac1ea-131">Pour cet exemple, la création du modèle entraîne celle d’un type de contenu *Renouvellement de contrat*.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-131">For this example, when you create the model, you are creating a new *Contract Renewal* content type.</span></span>

<span data-ttu-id="ac1ea-132">Sélectionnez **Paramètres avancés** si vous souhaitez mapper ce modèle à un type de contenu d’entreprise existant dans la galerie des types de contenu SharePoint, pour utiliser son schéma.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-132">Select **Advanced settings** if you want to map this model to an existing enterprise content type in the SharePoint Content types gallery to use its schema.</span></span> <span data-ttu-id="ac1ea-133">Les types de contenu d’entreprise sont stockés dans le hub Type de contenu au sein du Centre d’administration SharePoint. Ils sont syndiqués sur tous les sites du client.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-133">Enterprise content types are stored in the Content Type Hub in the SharePoint admin center and are syndicated to all sites in the tenant.</span></span> <span data-ttu-id="ac1ea-134">Note : vous pouvez certes utiliser un type de contenu existant pour tirer parti de son schéma et faciliter l’identification et la classification. Néanmoins, vous devez entraîner votre modèle à extraire des informations des fichiers qu’il identifie.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-134">Note that while you can use an existing content type to leverage its schema to help with identification and classification, you still need to train your model to extract information from files it identifies.</span></span></br>

![Paramètres avancés](../media/content-understanding/advanced-settings.png)

## <a name="add-your-example-files"></a><span data-ttu-id="ac1ea-136">Ajouter vos exemples de fichiers</span><span class="sxs-lookup"><span data-stu-id="ac1ea-136">Add your example files</span></span>

<span data-ttu-id="ac1ea-137">Sur la page d’accueil du modèle, ajoutez vos exemples de fichiers dont vous aurez besoin pour entraîner le modèle à identifier votre type de document.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-137">On the model home page, add your examples files you will need to help train the model to identify your document type.</span></span> </br>
</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4D0iX] 

</br>

> [!NOTE]
> <span data-ttu-id="ac1ea-138">Vous devez utiliser les mêmes fichiers pour le classifieur et l’[entraînement de l’extracteur](create-an-extractor.md).</span><span class="sxs-lookup"><span data-stu-id="ac1ea-138">You should use the same files for both classifier and [extractor training](create-an-extractor.md).</span></span> <span data-ttu-id="ac1ea-139">Vous pouvez toujours ajouter d’autres fichiers ultérieurement, mais l’ensemble déjà ajouté d’exemples de fichiers est en général complet.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-139">You always have the option to add more later, but typically you add a full set of example files.</span></span> <span data-ttu-id="ac1ea-140">Étiquetez certains d’entre eux pour entraîner votre modèle, puis testez les autres non étiquetés pour évaluer l’adéquation du modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-140">Label some to train your model, and test the remaining unlabeled ones to evaluate model fitness.</span></span> 

<span data-ttu-id="ac1ea-141">Pour votre ensemble d’apprentissage, vous devez utiliser des exemples positifs et négatifs :</span><span class="sxs-lookup"><span data-stu-id="ac1ea-141">For your training set, you want to use both positive and negative examples:</span></span>
- <span data-ttu-id="ac1ea-142">Exemple positif : documents représentant le type de document.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-142">Positive example: Documents that represent the document type.</span></span> <span data-ttu-id="ac1ea-143">Ces documents contiennent des chaînes et des informations qui doivent toujours figurer dans ce type de document.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-143">These contain strings and information that would always be in this type of document.</span></span>
- <span data-ttu-id="ac1ea-144">Exemple négatif : tout autre document ne représentant pas le document à classer.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-144">Negative example: Any other document that does not represent the document you want to classify.</span></span> 

<span data-ttu-id="ac1ea-145">Veillez à utiliser au moins cinq exemples positifs et au moins un exemple négatif pour entraîner votre modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-145">Be sure to use at least five positive examples and at least one negative example to train your model.</span></span>  <span data-ttu-id="ac1ea-146">Vous devez créer d’autres exemples pour tester votre modèle après le processus d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-146">You want to create additional ones to test your model after the training process.</span></span>

<span data-ttu-id="ac1ea-147">Pour ajouter des exemples de fichiers :</span><span class="sxs-lookup"><span data-stu-id="ac1ea-147">To add example files:</span></span>

1. <span data-ttu-id="ac1ea-148">Sur la page d’accueil du modèle, dans la mosaïque **Ajouter des exemples de fichiers**, cliquez sur **Ajouter des fichiers**.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-148">On the model home page, in the **Add example files** tile, click **Add files**.</span></span>
2. <span data-ttu-id="ac1ea-149">À la page **Sélectionner des exemples de fichiers pour votre modèle**, sélectionnez vos exemples de fichiers dans la bibliothèque Fichiers d’entraînement du centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-149">On the **Select example files for your model** page, select your example files from the Training files library in the content center.</span></span> <span data-ttu-id="ac1ea-150">Si vous ne l’avez pas déjà fait, choisissez de les charger maintenant en cliquant sur **Charger** pour les copier dans la bibliothèque Fichiers d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-150">If you had not already uploaded them there, choose to upload them now by clicking **Upload** to copy them to the Training files library.</span></span>
3. <span data-ttu-id="ac1ea-151">Après avoir sélectionné vos exemples de fichiers à utiliser pour entraîner le modèle, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-151">After selecting your example files to use to train the model, click **Add**.</span></span>

    ![Sélectionner des exemples de fichiers](../media/content-understanding/select-sample.png) 

## <a name="label-your-example-files"></a><span data-ttu-id="ac1ea-153">Étiqueter vos exemples de fichiers</span><span class="sxs-lookup"><span data-stu-id="ac1ea-153">Label your example files</span></span>

<span data-ttu-id="ac1ea-154">Une fois que vous avez ajouté vos exemples de fichiers, vous devez les étiqueter comme positifs ou négatifs.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-154">After adding your example files, you need to label them as either positive or negative examples.</span></span>

1. <span data-ttu-id="ac1ea-155">Depuis la page d’accueil du modèle, dans la mosaïque **Classer des fichiers et exécuter l’entraînement**, cliquez sur **Entraîner le classifieur**.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-155">From the model home page, on the **Classify files and run training** tile, click **Train classifier**.</span></span>
   <span data-ttu-id="ac1ea-156">La page d’étiquettes affiche alors une liste de vos exemples de fichiers, le premier fichier étant visible dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-156">This displays the label page that shows a listing of your example files, with the first file visible in the viewer.</span></span>
2. <span data-ttu-id="ac1ea-157">Dans la visionneuse située en haut du premier exemple de fichier, un texte doit vous demander si le fichier est un exemple du modèle que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-157">In the viewer on the top of the first example file, you should see text asking if the file is an example of the model you just created.</span></span> <span data-ttu-id="ac1ea-158">Si cet exemple est positif, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-158">If it is a positive example, select **Yes**.</span></span> <span data-ttu-id="ac1ea-159">Si cet exemple est négatif, sélectionnez **Non**.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-159">If it is a negative example, select **No**.</span></span>
3. <span data-ttu-id="ac1ea-160">Dans la liste **Exemples étiquetés** à gauche, sélectionnez, puis étiquetez les fichiers supplémentaires à utiliser comme exemples.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-160">From the **Labeled examples** list on the left, select additional files that you want to use as examples, and label them.</span></span> 

    ![Page d’accueil du classifieur](../media/content-understanding/classifier-home-page.png) 


> [!NOTE]
> <span data-ttu-id="ac1ea-162">Étiquetez au moins cinq exemples positifs.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-162">Label at least five positive examples.</span></span> <span data-ttu-id="ac1ea-163">Vous devez également étiqueter au moins un exemple négatif.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-163">You must also label at least one negative example.</span></span> 

## <a name="create-an-explanation"></a><span data-ttu-id="ac1ea-164">Créer une explication</span><span class="sxs-lookup"><span data-stu-id="ac1ea-164">Create an explanation</span></span>

<span data-ttu-id="ac1ea-165">L’étape suivante consiste à créer une explication à la page Entraîner.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-165">The next step is for you to create an explanation on the Train page.</span></span> <span data-ttu-id="ac1ea-166">Une explication permet au modèle de comprendre comment reconnaître le document.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-166">An explanation helps the model understand how to recognize the document.</span></span> <span data-ttu-id="ac1ea-167">Par exemple, les documents Renouvellement de contrat contiennent toujours une chaîne de caractères *Demande de divulgation supplémentaire*.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-167">For example, the Contract Renewal documents always contain a *Request for additional disclosure* text string.</span></span>

> [!Note]
> <span data-ttu-id="ac1ea-168">Utilisées avec des extracteurs, les explications identifient la chaîne à extraire du document.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-168">When used with extractors, an explanation identifies the string that you want to extract from the document.</span></span> 

<span data-ttu-id="ac1ea-169">Pour créer une explication :</span><span class="sxs-lookup"><span data-stu-id="ac1ea-169">To create an explanation:</span></span>

1. <span data-ttu-id="ac1ea-170">Depuis la page d’accueil du modèle, sélectionnez l’onglet **Entraîner** pour accéder à la page correspondante.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-170">From the model home page, select the **Train** tab to go to the Train page.</span></span>
2. <span data-ttu-id="ac1ea-171">À la page Entraîner, la section **Fichiers entraînés** contient normalement une liste des exemples de fichiers précédemment étiquetés.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-171">On the Train page, in the **Trained files** section you should see a list of the sample files that you previously labeled.</span></span> <span data-ttu-id="ac1ea-172">Sélectionnez un des fichiers positifs de la liste pour l’afficher dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-172">Select one of the positive files from the list, and it displays in the viewer.</span></span>
3. <span data-ttu-id="ac1ea-173">Dans la section Explication, sélectionnez **Nouveau**, puis **Espace**.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-173">In the Explanation section, select **New** and then **Blank**.</span></span>
4. <span data-ttu-id="ac1ea-174">À la page **Créer une explication** :</span><span class="sxs-lookup"><span data-stu-id="ac1ea-174">On the **Create an explanation** page:</span></span></br>
    <span data-ttu-id="ac1ea-175">a.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-175">a.</span></span> <span data-ttu-id="ac1ea-176">Tapez le **nom** (par exemple, « bloc de divulgation »).</span><span class="sxs-lookup"><span data-stu-id="ac1ea-176">Type the **Name** (for example, "Disclosure Block").</span></span></br>
    <span data-ttu-id="ac1ea-177">b.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-177">b.</span></span> <span data-ttu-id="ac1ea-178">Sélectionnez le **type**.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-178">Select the **Type**.</span></span> <span data-ttu-id="ac1ea-179">Pour l’échantillon, sélectionnez **Liste d’expressions**, puisque vous ajoutez une chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-179">For the sample, select **Phrase list**, since you add a text string.</span></span></br>
    <span data-ttu-id="ac1ea-180">c.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-180">c.</span></span> <span data-ttu-id="ac1ea-181">Dans la zone **Tapez ici**, tapez la chaîne.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-181">In the **Type here** box, type the string.</span></span> <span data-ttu-id="ac1ea-182">Pour l’échantillon, ajoutez « Demande de divulgation supplémentaire ».</span><span class="sxs-lookup"><span data-stu-id="ac1ea-182">For the sample, add "Request for additional disclosure".</span></span> <span data-ttu-id="ac1ea-183">Vous pouvez sélectionner **Respecter la casse** si la chaîne doit respecter la casse.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-183">You can select **Case sensitive** if the string needs to be case sensitive.</span></span></br>
    <span data-ttu-id="ac1ea-184">d.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-184">d.</span></span> <span data-ttu-id="ac1ea-185">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-185">Click **Save**.</span></span>

    ![Créer une explication](../media/content-understanding/explanation.png) 
    
5. <span data-ttu-id="ac1ea-187">Le centre de contenu vérifie à présent si l’explication que vous avez créée suffisamment complète pour identifier correctement comme positifs et négatifs les autres exemples de fichiers étiquetés.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-187">The Content Center now checks to see if the explanation you created is complete enough to identify the remaining labeled example files correctly, as positive and negative examples.</span></span> <span data-ttu-id="ac1ea-188">Dans la section Fichiers entraînés, consultez la colonne **Évaluation** après la fin de l’apprentissage pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-188">In the Trained Files section, check the **Evaluation** column after the training has completed to see the results.</span></span> <span data-ttu-id="ac1ea-189">Les fichiers affichent la valeur **Correspondance** si les explications que vous avez créées sont suffisantes pour correspondre aux éléments étiquetés comme positifs ou négatifs.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-189">The files show a value of **Match**, if the explanations you created was enough to match what you labeled as positive or negative.</span></span>

    ![Valeur de correspondance](../media/content-understanding/match.png) 

<span data-ttu-id="ac1ea-191">Si une **incompatibilité** apparaît sur les fichiers étiquetés, vous devrez sans doute créer une explication supplémentaire pour fournir au modèle des informations supplémentaires permettant d’identifier le type de document.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-191">If you receive a **Mismatch** on the labeled files, you may need to create an additional explanation to provide the model more information to identify the document type.</span></span> <span data-ttu-id="ac1ea-192">Dans ce cas, cliquez sur le fichier pour obtenir plus d’informations sur la raison de l’incompatibilité.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-192">If this happens, click on the file to get more information about why the mismatch occurred.</span></span>

## <a name="test-your-model"></a><span data-ttu-id="ac1ea-193">Tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="ac1ea-193">Test your model</span></span>

<span data-ttu-id="ac1ea-194">Si vous avez reçu une correspondance sur vos fichiers échantillons étiquetés, vous pouvez à présent tester votre modèle sur les autres exemples de fichiers non étiquetés pour vérifier que ce modèle est inconnu.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-194">If you received a match on your labeled sample files, you can now  test your model on your remaining unlabeled example files that the model has not seen before.</span></span>  <span data-ttu-id="ac1ea-195">Cette étape est facultative mais utile, car elle permet d’évaluer la « pertinence » ou le degré de préparation du modèle avant utilisation, en le testant sur des fichiers pour l’instant inconnus de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-195">This is optional, but a useful step to evaluate the “fitness” or readiness of the model before using it, by testing it on files the model hasn’t seen before.</span></span>

1. <span data-ttu-id="ac1ea-196">Dans la page d’accueil du modèle, sélectionnez l’onglet **Test**. Le modèle est alors exécuté sur vos fichiers échantillons non étiquetés.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-196">From the model home page, select the **Test** tab.  This runs the model on your unlabeled sample files.</span></span>
2. <span data-ttu-id="ac1ea-197">Dans la liste **Fichiers de test**, vos exemples de fichiers indiquent s’ils sont positifs ou négatifs d’après les prévisions du modèle.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-197">In the **Test files** list, your example files display and shows if the model predicted them to be positive or negative.</span></span> <span data-ttu-id="ac1ea-198">Utilisez ces informations pour déterminer plus facilement l’efficacité de votre classifieur lors de l’identification de vos documents.</span><span class="sxs-lookup"><span data-stu-id="ac1ea-198">Use this information to help determine the effectiveness of your classifier in identifying your documents.</span></span>

    ![Test des fichiers non étiquetés](../media/content-understanding/test-on-files.png) 

## <a name="see-also"></a><span data-ttu-id="ac1ea-200">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac1ea-200">See Also</span></span>
[<span data-ttu-id="ac1ea-201">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="ac1ea-201">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="ac1ea-202">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="ac1ea-202">Document Understanding overview</span></span>](document-understanding-overview.md)

[<span data-ttu-id="ac1ea-203">Types d’explications</span><span class="sxs-lookup"><span data-stu-id="ac1ea-203">Explanation types</span></span>](explanation-types-overview.md)

[<span data-ttu-id="ac1ea-204">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="ac1ea-204">Apply a model</span></span>](apply-a-model.md) 
