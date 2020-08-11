---
title: Créer un modèle de traitement de formulaire (aperçu)
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.service: ''
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Créez un modèle de traitement de formulaire dans le projet cortex.
ms.openlocfilehash: 733baf24d8a484571ba9882fdda2633dc2ce0504
ms.sourcegitcommit: a3a5dc541b0c971608cc86ef480509c25a13ca60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "46612773"
---
# <a name="create-a-form-processing-model-preview"></a><span data-ttu-id="e2f19-103">Créer un modèle de traitement de formulaire (aperçu)</span><span class="sxs-lookup"><span data-stu-id="e2f19-103">Create a form processing model (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="e2f19-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="e2f19-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="e2f19-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="e2f19-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

<span data-ttu-id="e2f19-106">Utilisation de l’outil [ai Builder](https://docs.microsoft.com/ai-builder/overview) -une fonctionnalité de Microsoft PowerApp-Project cortex les utilisateurs peuvent créer un [modèle de traitement de formulaire](form-processing-overview.md) directement à partir d’une bibliothèque de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e2f19-106">Using [AI Builder](https://docs.microsoft.com/ai-builder/overview) - a feature in Microsoft PowerApps - Project Cortex users can create a [form processing model](form-processing-overview.md) directly from a SharePoint document library.</span></span> 

<span data-ttu-id="e2f19-107">La création d’un modèle de traitement de formulaire implique les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2f19-107">Creating a form processing model involves the following:</span></span>
 - <span data-ttu-id="e2f19-108">Étape 1 : créer le modèle de traitement pour créer le type de contenu</span><span class="sxs-lookup"><span data-stu-id="e2f19-108">Step 1: Create the from processing model to create the content type</span></span>
 - <span data-ttu-id="e2f19-109">Étape 2 : ajouter et analyser des exemples de fichiers</span><span class="sxs-lookup"><span data-stu-id="e2f19-109">Step 2: Add and analyze example files</span></span>
 - <span data-ttu-id="e2f19-110">Étape 3 : sélection de vos champs de formulaire</span><span class="sxs-lookup"><span data-stu-id="e2f19-110">Step 3: Select your form fields</span></span>
 - <span data-ttu-id="e2f19-111">Étape 4 : formation et test de votre modèle</span><span class="sxs-lookup"><span data-stu-id="e2f19-111">Step 4: Train and test your model</span></span>
 - <span data-ttu-id="e2f19-112">Étape 5 : publier votre modèle</span><span class="sxs-lookup"><span data-stu-id="e2f19-112">Step 5: Publish your model</span></span>
 - <span data-ttu-id="e2f19-113">Étape 6 : utiliser votre modèle</span><span class="sxs-lookup"><span data-stu-id="e2f19-113">Step 6: Use your model</span></span>


## <a name="requirements"></a><span data-ttu-id="e2f19-114">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="e2f19-114">Requirements</span></span>

<span data-ttu-id="e2f19-115">Vous pouvez uniquement créer un modèle de traitement de formulaire dans les bibliothèques de documents SharePoint dans lesquelles il est activé.</span><span class="sxs-lookup"><span data-stu-id="e2f19-115">You can only create a form processing model in SharePoint document libraries in which it is enabled.</span></span> <span data-ttu-id="e2f19-116">Si le traitement des formulaires est activé, vous pouvez voir le **Générateur d’ai** **« créer un modèle de traitement de formulaire »** dans le menu **automatiser** de votre bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="e2f19-116">If form processing is enabled, you will be able to see the **AI Builder** **"Create a form processing model'** under the **Automate** menu in your document library.</span></span>  <span data-ttu-id="e2f19-117">Si vous avez besoin d’un traitement activé dans votre bibliothèque de documents, contactez votre administrateur.</span><span class="sxs-lookup"><span data-stu-id="e2f19-117">If you need from processing enabled on your document library, contact your admin.</span></span>

 ![Créer un modèle de générateur AI](../media/content-understanding/create-ai-builder-model.png)</br>


## <a name="step-1-create-a-form-processing-model"></a><span data-ttu-id="e2f19-119">Étape 1 : créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="e2f19-119">Step 1: Create a Form Processing model</span></span>

<span data-ttu-id="e2f19-120">La première étape de la création d’un modèle de traitement de formulaire consiste à le nommer de façon à créer le nouveau type de contenu et à créer une nouvelle vue de bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="e2f19-120">The first step in creating a form processing model is to name it to create the define the new content type and create a new document library view for it.</span></span>

1. <span data-ttu-id="e2f19-121">Dans votre bibliothèque de documents, sélectionnez le menu **automatiser** , sélectionnez **générateur ai**, puis sélectionnez **créer un modèle de traitement de formulaire**.</span><span class="sxs-lookup"><span data-stu-id="e2f19-121">In your document library, select the **Automate** menu, select **AI Builder**, and then select **Create a Form Processing model**.</span></span>

    ![Créer un modèle de générateur AI](../media/content-understanding/create-ai-builder-model.png)</br>
2. <span data-ttu-id="e2f19-123">Dans le volet **nouveau modèle de traitement de formulaire** , dans le champ **nom** , tapez un nom pour votre modèle (par exemple, *bons de commande*).</span><span class="sxs-lookup"><span data-stu-id="e2f19-123">In the **New form processing model** pane, in the  **Name** field, type a name for your model (for example, *Purchase Orders*).</span></span>

    ![Nouveau modèle de traitement de formulaire](../media/content-understanding/new-form-model.png)</br> 

3. <span data-ttu-id="e2f19-125">Lorsque vous créez un modèle de traitement de formulaire, vous créez un nouveau type de contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e2f19-125">When you create a form processing model, you are creating a new SharePoint content type.</span></span> <span data-ttu-id="e2f19-126">Un type de contenu SharePoint représente une catégorie de documents qui ont des caractéristiques communes et qui partagent une collection de colonnes ou de propriétés de métadonnées pour ce contenu particulier.</span><span class="sxs-lookup"><span data-stu-id="e2f19-126">A SharePoint content type represents a category of documents that have common characteristics and share a collection of columns or metadata properties for that particular content.</span></span> <span data-ttu-id="e2f19-127">Les types de contenu SharePoint sont gérés via la [Galerie de types de contenu]().</span><span class="sxs-lookup"><span data-stu-id="e2f19-127">SharePoint Content Types are managed through the [Content types gallery]().</span></span>

    <span data-ttu-id="e2f19-128">Sélectionnez **Paramètres avancés** si vous souhaitez mapper ce modèle à un type de contenu existant dans la Galerie de types de contenu SharePoint pour utiliser son schéma.</span><span class="sxs-lookup"><span data-stu-id="e2f19-128">Select **Advanced settings** if you want to map this model to an existing content type in the SharePoint Content types gallery to use its schema.</span></span> 

4. <span data-ttu-id="e2f19-129">Votre modèle crée un nouvel affichage dans votre bibliothèque de documents pour vos données extraites.</span><span class="sxs-lookup"><span data-stu-id="e2f19-129">Your model will create a new view in your document library for your extracted data.</span></span> <span data-ttu-id="e2f19-130">Si vous ne souhaitez pas que l’affichage par défaut s’affiche, désélectionnez **définir l’affichage comme mode par défaut**.</span><span class="sxs-lookup"><span data-stu-id="e2f19-130">If you do not want it to the default view, deselect **Set the view as default**.</span></span>
5. <span data-ttu-id="e2f19-131">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="e2f19-131">Select **Create**.</span></span>


## <a name="step-2-add-and-analyze-documents"></a><span data-ttu-id="e2f19-132">Étape 2 : ajouter et analyser des documents</span><span class="sxs-lookup"><span data-stu-id="e2f19-132">Step 2: Add and analyze documents</span></span>

<span data-ttu-id="e2f19-133">Une fois que vous avez créé votre nouveau modèle de traitement de formulaire, votre navigateur ouvre une nouvelle page de modèle de traitement des formulaires du générateur AI PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e2f19-133">After you create your new form processing model, your browser will open a new PowerApps AI Builder forms processing model page.</span></span> <span data-ttu-id="e2f19-134">Sur cette page, vous pouvez ajouter et analyser vos exemples de documents.</span><span class="sxs-lookup"><span data-stu-id="e2f19-134">On this page you can add and analyze your example documents.</span></span> </br>

> [!Note]
> <span data-ttu-id="e2f19-135">Lorsque vous recherchez des exemples de fichiers à utiliser, voir le [modèle de traitement de formulaire exigences en matière de document d’entrée et conseils d’optimisation](https://docs.microsoft.com/ai-builder/form-processing-model-requirements).</span><span class="sxs-lookup"><span data-stu-id="e2f19-135">When looking for example files to use, see the [form processing model input document requirements and optimization tips](https://docs.microsoft.com/ai-builder/form-processing-model-requirements).</span></span> 

   ![Générateur d’applications d’alimentation](../media/content-understanding/powerapps.png)</br> 
 

1. <span data-ttu-id="e2f19-137">Cliquez sur **Ajouter des documents** pour commencer à ajouter des exemples de documents analysés afin de déterminer les paires de valeurs nommées pouvant être extraites.</span><span class="sxs-lookup"><span data-stu-id="e2f19-137">Click **Add documents** to begin adding example documents that are analyzed to determine what named value pairs can be extracted.</span></span> <span data-ttu-id="e2f19-138">Vous pouvez choisir **Télécharger à partir du stockage local**, **SharePoint**ou le **stockage BLOB Azure**.</span><span class="sxs-lookup"><span data-stu-id="e2f19-138">You can choose either **Upload from local storage**, **SharePoint**, or **Azure Blob storage**.</span></span> <span data-ttu-id="e2f19-139">Vous devrez utiliser au moins cinq fichiers pour la formation.</span><span class="sxs-lookup"><span data-stu-id="e2f19-139">You will need to use at least five files for training.</span></span>
2. <span data-ttu-id="e2f19-140">Après avoir ajouté vos fichiers, sélectionnez **analyser** pour vérifier les informations courantes : tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="e2f19-140">After adding your files, select **Analyze** to check for any information that is common is all files.</span></span> <span data-ttu-id="e2f19-141">Notez que cette opération peut prendre plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="e2f19-141">Note that this may take several minutes to complete.</span></span></br> 
 
    ![Analyser les fichiers](../media/content-understanding/analyze.png)</br> 

3. <span data-ttu-id="e2f19-143">Une fois qu’ils ont été analysés, dans la page **sélectionnez les champs de formulaire que vous souhaitez enregistrer** , cliquez sur le fichier pour afficher les champs qui ont été détectés.</span><span class="sxs-lookup"><span data-stu-id="e2f19-143">After they have been analyzed, in the **Select the form fields you want to save** page, click the file to see the fields that were detected.</span></span></br>

    ![Sélectionner les champs de formulaire](../media/content-understanding/select-form-fields.png)</br> 

## <a name="step-3-select-your-form-fields"></a><span data-ttu-id="e2f19-145">Étape 3 : sélection de vos champs de formulaire</span><span class="sxs-lookup"><span data-stu-id="e2f19-145">Step 3: Select your form fields</span></span>

<span data-ttu-id="e2f19-146">Après avoir analysé vos documents pour les champs, vous pouvez voir les champs trouvés et ceux que vous souhaitez enregistrer.</span><span class="sxs-lookup"><span data-stu-id="e2f19-146">After analyzing your documents for fields, you can now see which fields were found, and which ones you want to save.</span></span> <span data-ttu-id="e2f19-147">Les champs enregistrés s’affichent sous forme de colonnes dans la vue bibliothèque de documents de votre modèle et affichent les valeurs extraites de chaque document.</span><span class="sxs-lookup"><span data-stu-id="e2f19-147">Saved fields will display as columns in your model's document library view and will show the values extracted from each document.</span></span>

1. <span data-ttu-id="e2f19-148">La page suivante affiche l’un de vos fichiers d’exemple et met en surbrillance tous les champs communs détectés automatiquement par le système.</span><span class="sxs-lookup"><span data-stu-id="e2f19-148">The next page will display one of your sample files and will highlight all common fields that were automatically detected by the system.</span></span> </br>

    ![Sélectionner les champs de formulaire](../media/content-understanding/select-fields-page.png)</br> 

2. <span data-ttu-id="e2f19-150">Sélectionnez les champs que vous souhaitez enregistrer, puis activez la case à cocher pour confirmer votre sélection.</span><span class="sxs-lookup"><span data-stu-id="e2f19-150">Select the fields you want to save, and select the checkbox to confirm your selection.</span></span> <span data-ttu-id="e2f19-151">Par exemple, dans le modèle bon de commande, vous pouvez choisir de sélectionner les champs *Date*, *op*et *total* .</span><span class="sxs-lookup"><span data-stu-id="e2f19-151">For example, in the Purchase Order model, you can choose to select the *Date*, *PO*, and *Total* fields.</span></span>  <span data-ttu-id="e2f19-152">Notez que vous pouvez également choisir de renommer un champ si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="e2f19-152">Note that you can also choose to rename a field if you choose.</span></span> </br>

    ![Sélectionnez cf #](../media/content-understanding/po.png)</br> 

3. <span data-ttu-id="e2f19-154">Si un champ n’a pas été détecté par l’analyse, vous pouvez toujours choisir de l’ajouter.</span><span class="sxs-lookup"><span data-stu-id="e2f19-154">If a field was not detected by analysis, you can still choose to add it.</span></span> <span data-ttu-id="e2f19-155">Mettez en surbrillance les informations que vous souhaitez extraire, et dans la zone Nom, tapez le nom que vous voulez lui attribuer.</span><span class="sxs-lookup"><span data-stu-id="e2f19-155">Highlight the information you want to extract, and in the name box type in the name you want to give it.</span></span> <span data-ttu-id="e2f19-156">Ensuite, sélectionnez la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="e2f19-156">Then select the check.</span></span> <span data-ttu-id="e2f19-157">Notez que vous devrez confirmer les champs non détectés dans vos fichiers restants.</span><span class="sxs-lookup"><span data-stu-id="e2f19-157">Note that you will need to confirm undetected fields in your remaining example files.</span></span>
4. <span data-ttu-id="e2f19-158">Cliquez sur **confirmer les champs** après avoir sélectionné les champs que vous souhaitez enregistrer.</span><span class="sxs-lookup"><span data-stu-id="e2f19-158">Click **Confirm fields** after you have selected the fields you want to save.</span></span> </br>
 
    ![Confirmer les champs](../media/content-understanding/confirm-fields.png)</br> 
 
5. <span data-ttu-id="e2f19-160">Dans la page **sélectionnez les champs de formulaire que vous souhaitez enregistrer** , le nombre de champs que vous avez sélectionnés est affiché.</span><span class="sxs-lookup"><span data-stu-id="e2f19-160">On the **Select the form fields you want to save** page, it will show the number of fields you have selected.</span></span> <span data-ttu-id="e2f19-161">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="e2f19-161">Select **Done**.</span></span>

## <a name="step-4-train-and-test-your-model"></a><span data-ttu-id="e2f19-162">Étape 4 : formation et test de votre modèle</span><span class="sxs-lookup"><span data-stu-id="e2f19-162">Step 4: Train and test your model</span></span>

<span data-ttu-id="e2f19-163">Après avoir sélectionné les champs que vous souhaitez enregistrer, la page de **Résumé du modèle** vous permettra de former et de tester votre modèle.</span><span class="sxs-lookup"><span data-stu-id="e2f19-163">After selecting the fields you want to save, the **Model Summary** page will let you train and test your model.</span></span>

1. <span data-ttu-id="e2f19-164">Sur la page **Résumé du modèle** , les champs enregistrés s’affichent dans la section **champs sélectionnés** .</span><span class="sxs-lookup"><span data-stu-id="e2f19-164">On the **Model Summary** page, the saved fields will show in the **Selected fields** section.</span></span> <span data-ttu-id="e2f19-165">Sélectionnez **train** pour commencer la formation sur vos exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e2f19-165">Select **Train** to begin training on your example files.</span></span> <span data-ttu-id="e2f19-166">Notez que cette opération peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="e2f19-166">Note that this may take a few minutes to complete.</span></span></br>
    <span data-ttu-id="e2f19-167">![Confirmer les champs](../media/content-understanding/select-fields-train.png)</span><span class="sxs-lookup"><span data-stu-id="e2f19-167">![Confirm fields](../media/content-understanding/select-fields-train.png)</span></span></br> 
2. <span data-ttu-id="e2f19-168">Lorsque vous voyez la notification indiquant que la formation est terminée, sélectionnez **accéder à la page Détails**.</span><span class="sxs-lookup"><span data-stu-id="e2f19-168">When you see the notification that training has completed, select **Go to details page**.</span></span> 
3. <span data-ttu-id="e2f19-169">Sur la page **Détails du modèle** , vous pouvez choisir de tester le fonctionnement de votre modèle en sélectionnant **test rapide**.</span><span class="sxs-lookup"><span data-stu-id="e2f19-169">On the **Model details** page, you can choose to test how your model works by selecting **Quick test**.</span></span> <span data-ttu-id="e2f19-170">Cela vous permet de glisser-déplacer des fichiers vers la page et de voir si les champs sont détectés.</span><span class="sxs-lookup"><span data-stu-id="e2f19-170">This lets you drag and drop files to the page and see if the fields are detected.</span></span>

## <a name="step-5-publish-your-model"></a><span data-ttu-id="e2f19-171">Étape 5 : publier votre modèle</span><span class="sxs-lookup"><span data-stu-id="e2f19-171">Step 5: Publish your model</span></span>



1. <span data-ttu-id="e2f19-172">Si vous êtes satisfait des résultats de votre modèle, sélectionnez **publier** pour le mettre à disposition.</span><span class="sxs-lookup"><span data-stu-id="e2f19-172">If you are satisfied with the results of your model, select **Publish** to make it available for use.</span></span>
2. <span data-ttu-id="e2f19-173">Une fois le modèle publié, sélectionnez **utiliser le modèle**.</span><span class="sxs-lookup"><span data-stu-id="e2f19-173">After the model published, select **Use model**.</span></span> <span data-ttu-id="e2f19-174">Cela crée un flux PowerAutomate qui s’exécutera dans votre bibliothèque de documents SharePoint et extraira les champs identifiés dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="e2f19-174">This creates a PowerAutomate flow that will run in your SharePoint document library and will extract the fields that have been identified in the model.</span></span> <span data-ttu-id="e2f19-175">Sélectionnez **créer un flux**.</span><span class="sxs-lookup"><span data-stu-id="e2f19-175">Select **Create Flow**.</span></span>  
3. <span data-ttu-id="e2f19-176">Une fois l’opération terminée, vous verrez le message que **votre flux a été créé avec succès**.</span><span class="sxs-lookup"><span data-stu-id="e2f19-176">When completed, you will see the message **Your flow has been successfully created**.</span></span>
 
 
## <a name="step-6-use-your-model"></a><span data-ttu-id="e2f19-177">Étape 6 : utiliser votre modèle</span><span class="sxs-lookup"><span data-stu-id="e2f19-177">Step 6: Use your model</span></span>

<span data-ttu-id="e2f19-178">Après avoir publié votre modèle et créé son flux PowerAutomate, vous pouvez utiliser votre modèle dans votre bibliothèque de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e2f19-178">After publishing your model and creating it's PowerAutomate flow, you can use your model in your SharePoint document library.</span></span>

1. <span data-ttu-id="e2f19-179">Après avoir publié votre modèle, sélectionnez **accéder à SharePoint** pour accéder à votre bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="e2f19-179">After publishing your model , select **Go to SharePoint** to go to your document library.</span></span>
2. <span data-ttu-id="e2f19-180">Dans votre vue de modèle de bibliothèque de documents, Notez que les champs que vous avez sélectionnés s’affichent désormais sous forme de colonnes.</span><span class="sxs-lookup"><span data-stu-id="e2f19-180">On your document library model view, notice that the fields you selected now display as columns.</span></span></br>

    ![Bibliothèque de documents avec modèle appliqué](../media/content-understanding/doc-lib-view.png)</br> 

    <span data-ttu-id="e2f19-182">Notez également que le lien d’informations en regard de **documents** indique qu’un modèle de traitement des formulaires est appliqué à cette bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="e2f19-182">Also notice that the information link next to **Documents** will note that a forms processing model is applied to this document library.</span></span>

    ![Compressé](../media/content-understanding/info-button.png)</br>  

3. <span data-ttu-id="e2f19-184">Charger des fichiers dans votre bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="e2f19-184">Upload files to your document library.</span></span> <span data-ttu-id="e2f19-185">Tous les fichiers que le modèle identifie comme étant le type de contenu répertorient les fichiers dans votre affichage et affichent les données extraites dans les colonnes.</span><span class="sxs-lookup"><span data-stu-id="e2f19-185">Any files that the model identifies as it's content type will list the files in your view, and will display the extracted data in the columns.</span></span></br>

    ![Compressé](../media/content-understanding/doc-lib-done.png)</br>  



## <a name="see-also"></a><span data-ttu-id="e2f19-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2f19-187">See Also</span></span>
  
[<span data-ttu-id="e2f19-188">Mise à l’arrêt de la documentation</span><span class="sxs-lookup"><span data-stu-id="e2f19-188">Power Automate documentation</span></span>](https://docs.microsoft.com/power-automate/)</br>
[<span data-ttu-id="e2f19-189">Formation : améliorer les performances d’entreprise avec le générateur AI</span><span class="sxs-lookup"><span data-stu-id="e2f19-189">Training: Improve business performance with AI Builder</span></span>](https://docs.microsoft.com/learn/paths/improve-business-performance-ai-builder/?source=learn)</br>




