---
title: Créer un modèle de traitement de formulaire
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: Priority
description: Créer un modèle de traitement de formulaire dans Microsoft SharePoint Syntex.
ms.openlocfilehash: df8a8bc5828c0235ecb18387fe753d77f0856eec
ms.sourcegitcommit: f7ca339bdcad38796c550064fb152ea09687d0f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/30/2020
ms.locfileid: "48321820"
---
# <a name="create-a-form-processing-model-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="5ef9f-103">Créer un modèle de traitement de formulaire dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="5ef9f-103">Create a form processing model in Microsoft SharePoint Syntex</span></span>


<span data-ttu-id="5ef9f-104">Grâce à [AI Builder](https://docs.microsoft.com/ai-builder/overview), une fonctionnalité de Microsoft PowerApps, les utilisateurs de SharePoint Syntex peuvent créer un [modèle de traitement de formulaire](form-processing-overview.md) directement à partir d’une bibliothèque de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-104">Using [AI Builder](https://docs.microsoft.com/ai-builder/overview) - a feature in Microsoft PowerApps - SharePoint Syntex users can create a [form processing model](form-processing-overview.md) directly from a SharePoint document library.</span></span> 

<span data-ttu-id="5ef9f-105">Pour créer un modèle de traitement de formulaire, vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5ef9f-105">Creating a form processing model involves the following:</span></span>
 - <span data-ttu-id="5ef9f-106">Étape 1 : créer le modèle de traitement de formulaire pour créer le type de contenu</span><span class="sxs-lookup"><span data-stu-id="5ef9f-106">Step 1: Create the from processing model to create the content type</span></span>
 - <span data-ttu-id="5ef9f-107">Étape 2 : ajouter et analyser des fichiers d’exemple</span><span class="sxs-lookup"><span data-stu-id="5ef9f-107">Step 2: Add and analyze example files</span></span>
 - <span data-ttu-id="5ef9f-108">Étape 3 : sélectionner vos champs de formulaire</span><span class="sxs-lookup"><span data-stu-id="5ef9f-108">Step 3: Select your form fields</span></span>
 - <span data-ttu-id="5ef9f-109">Étape 4 : entraîner et tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="5ef9f-109">Step 4: Train and test your model</span></span>
 - <span data-ttu-id="5ef9f-110">Étape 5 : publier votre modèle</span><span class="sxs-lookup"><span data-stu-id="5ef9f-110">Step 5: Publish your model</span></span>
 - <span data-ttu-id="5ef9f-111">Étape 6 : utiliser votre modèle</span><span class="sxs-lookup"><span data-stu-id="5ef9f-111">Step 6: Use your model</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef9f-112">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="5ef9f-112">Requirements</span></span>

<span data-ttu-id="5ef9f-113">Vous pouvez créer un modèle de traitement de formulaire uniquement dans les bibliothèques de documents SharePoint pour lesquelles il est activé.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-113">You can only create a form processing model in SharePoint document libraries for which it is enabled.</span></span> <span data-ttu-id="5ef9f-114">Si le traitement de formulaire est activé, vous pouvez voir le **AI Builder** **« Créer un modèle de traitement de formulaire »** dans le menu **Automatiser** de votre bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-114">If form processing is enabled, you are able to see the **AI Builder** **"Create a form processing model'** under the **Automate** menu in your document library.</span></span>  <span data-ttu-id="5ef9f-115">Si vous souhaitez que le traitement soit activé sur votre bibliothèque de documents, vous devez contacter votre administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-115">If you need processing enabled on your document library, you must contact your SharePoint administrator.</span></span>

 ![Créer un modèle AI Builder](../media/content-understanding/create-ai-builder-model.png)</br>

## <a name="step-1-create-a-form-processing-model"></a><span data-ttu-id="5ef9f-117">Étape 1 : créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="5ef9f-117">Step 1: Create a form Processing model</span></span>

<span data-ttu-id="5ef9f-118">La première étape de la création d’un modèle de traitement de formulaire consiste à le nommer, à créer le nouveau type de contenu et à créer une nouvelle vue de bibliothèque de documents pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-118">The first step in creating a form processing model is to name it and create the define the new content type and create a new document library view for it.</span></span>

1. <span data-ttu-id="5ef9f-119">Dans la bibliothèque de documents, sélectionnez le menu **Automatiser**, puis **AI Builder**, et enfin **Créer un modèle de traitement de formulaire**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-119">From the document library, select the **Automate** menu, select **AI Builder**, and then select **Create a Form Processing model**.</span></span>

    ![Créer un modèle](../media/content-understanding/create-ai-builder-model.png)</br>

2. <span data-ttu-id="5ef9f-121">Dans le volet **Nouveau modèle de traitement de formulaire**, dans le champ **Nom**, saisissez un nom pour votre modèle (par exemple, *Bons de commande*).</span><span class="sxs-lookup"><span data-stu-id="5ef9f-121">In the **New form processing model** pane, in the  **Name** field, type a name for your model (for example, *Purchase Orders*).</span></span>

    ![Nouveau modèle de traitement de formulaire](../media/content-understanding/new-form-model.png)</br> 

3. <span data-ttu-id="5ef9f-123">Lorsque vous créez un modèle de traitement de formulaire, vous créez un nouveau type de contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-123">When you create a form processing model, you create a new SharePoint content type.</span></span> <span data-ttu-id="5ef9f-124">Un type de contenu SharePoint représente une catégorie de documents qui ont des caractéristiques communes et qui partagent une collection de colonnes ou de propriétés de métadonnées pour ce contenu spécifique.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-124">A SharePoint content type represents a category of documents that have common characteristics and share a collection of columns or metadata properties for that particular content.</span></span> <span data-ttu-id="5ef9f-125">Les types de contenu SharePoint sont gérés via la [galerie des types de contenu]().</span><span class="sxs-lookup"><span data-stu-id="5ef9f-125">SharePoint Content Types are managed through the [Content types gallery]().</span></span>

    <span data-ttu-id="5ef9f-126">Sélectionnez **Paramètres avancés** si vous souhaitez mapper ce modèle à un type de contenu existant dans la galerie des types de contenu SharePoint, pour utiliser son schéma.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-126">Select **Advanced settings** if you want to map this model to an existing content type in the SharePoint Content types gallery to use its schema.</span></span> 

4. <span data-ttu-id="5ef9f-127">Votre modèle crée une nouvelle vue dans votre bibliothèque de documents pour vos données extraites.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-127">Your model creates a new view in your document library for your extracted data.</span></span> <span data-ttu-id="5ef9f-128">Si vous ne souhaitez pas que la vue par défaut soit définie, désélectionnez **Définir la vue par défaut**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-128">If you do not want it to the default view, deselect **Set the view as default**.</span></span>

5. <span data-ttu-id="5ef9f-129">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-129">Select **Create**.</span></span>

## <a name="step-2-add-and-analyze-documents"></a><span data-ttu-id="5ef9f-130">Étape 2 : ajouter et analyser des documents</span><span class="sxs-lookup"><span data-stu-id="5ef9f-130">Step 2: Add and analyze documents</span></span>

<span data-ttu-id="5ef9f-131">Après avoir créé votre nouveau modèle de traitement de formulaire, votre navigateur ouvre une nouvelle page de modèle de traitement de formulaires AI Builder dans PowerApps.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-131">After you create your new form processing model, your browser opens a new PowerApps AI Builder forms processing model page.</span></span> <span data-ttu-id="5ef9f-132">Sur cette page, vous pouvez ajouter et analyser vos exemples de documents.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-132">On this page you can add and analyze your example documents.</span></span> </br>

> [!NOTE]
> <span data-ttu-id="5ef9f-133">Lorsque vous recherchez des exemples de fichiers à utiliser, consultez l’article [Configuration requise et limitations du modèle de traitement de formulaire](https://docs.microsoft.com/ai-builder/form-processing-model-requirements).</span><span class="sxs-lookup"><span data-stu-id="5ef9f-133">When looking for example files to use, see the [form processing model input document requirements and optimization tips](https://docs.microsoft.com/ai-builder/form-processing-model-requirements).</span></span> 

   ![AI Builder de Power Apps](../media/content-understanding/powerapps.png)</br> 
 
1. <span data-ttu-id="5ef9f-135">Sélectionnez **Ajouter des documents** pour commencer à ajouter des exemples de documents analysés afin de déterminer les paires de valeurs nommées pouvant être extraites.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-135">Select **Add documents** to begin adding example documents analyzed to determine the named value pairs that can be extracted.</span></span> <span data-ttu-id="5ef9f-136">Vous pouvez ensuite choisir de **Télécharger à partir du stockage local**, de **SharePoint** ou du **Stockage Blob Azure**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-136">You can then choose either **Upload from local storage**, **SharePoint**, or **Azure Blob storage**.</span></span> <span data-ttu-id="5ef9f-137">Vous devez utiliser au moins cinq fichiers pour la formation.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-137">You need to use at least five files for training.</span></span>

2. <span data-ttu-id="5ef9f-138">Après avoir ajouté des fichiers, sélectionnez **Analyser** pour vérifier les informations communes à tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-138">After adding files, select **Analyze** to check for any information common is all files.</span></span> <span data-ttu-id="5ef9f-139">Cette opération peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-139">This may take several minutes to complete.</span></span></br> 
 
    ![Analyser les fichiers](../media/content-understanding/analyze.png)</br> 

3. <span data-ttu-id="5ef9f-141">Une fois les fichiers analysés, dans la page **Sélectionnez les champs de formulaire à enregistrer**, sélectionnez le fichier pour afficher les champs détectés.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-141">After the files have been analyzed, in the **Select the form fields you want to save** page select the file to view the detected fields.</span></span></br>

    ![Sélectionner les champs de formulaire](../media/content-understanding/select-form-fields.png)</br> 

## <a name="step-3-select-your-form-fields"></a><span data-ttu-id="5ef9f-143">Étape 3 : sélectionner vos champs de formulaire</span><span class="sxs-lookup"><span data-stu-id="5ef9f-143">Step 3: Select your form fields</span></span>

<span data-ttu-id="5ef9f-144">Après avoir analysé les documents pour les champs, vous pouvez maintenant voir les champs trouvés et identifier ceux que vous souhaitez enregistrer.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-144">After analyzing the documents for fields, you can now see the fields that were found, and identify the ones that you want to save.</span></span> <span data-ttu-id="5ef9f-145">Les champs enregistrés s’affichent sous forme de colonnes dans la vue de la bibliothèque de documents de votre modèle et montrent les valeurs extraites de chaque document.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-145">Saved fields display as columns in your model's document library view and show the values extracted from each document.</span></span>

1. <span data-ttu-id="5ef9f-146">La page suivante affiche l’un de vos exemples de fichiers et mettra en évidence tous les champs communs qui ont été automatiquement détectés par le système.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-146">The next page displays one of your sample files and will highlight all common fields that were automatically detected by the system.</span></span> </br>

    ![Sélectionner la page des champs](../media/content-understanding/select-fields-page.png)</br> 

2. <span data-ttu-id="5ef9f-148">Sélectionnez les champs que vous souhaitez enregistrer et cochez la case pour confirmer votre sélection.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-148">Select the fields that you want to save and select the checkbox to confirm your selection.</span></span> <span data-ttu-id="5ef9f-149">Par exemple, dans le modèle Bon de commande, choisissez de sélectionner les champs *Date*, *B.C.* et *Total*.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-149">For example, in the Purchase Order model, choose to select the *Date*, *PO*, and *Total* fields.</span></span>  <span data-ttu-id="5ef9f-150">Notez que vous pouvez également choisir de renommer un champ si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-150">Note that you can also choose to rename a field if you choose.</span></span> </br>

    ![Sélectionnez B.C.#](../media/content-understanding/po.png)</br> 

3. <span data-ttu-id="5ef9f-152">Si un champ n’a pas été détecté par l’analyse, vous pouvez toujours choisir de l’ajouter.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-152">If a field was not detected by analysis, you can still choose to add it.</span></span> <span data-ttu-id="5ef9f-153">Sélectionnez les informations que vous souhaitez extraire et, dans la zone de nom, saisissez le nom souhaité.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-153">Highlight the information you want to extract, and in the name box type in the name you want.</span></span> <span data-ttu-id="5ef9f-154">Cochez ensuite la case.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-154">Then select the check box.</span></span> <span data-ttu-id="5ef9f-155">Notez que vous devez confirmer les champs non détectés dans vos fichiers d’exemple restants.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-155">Note that you need to confirm undetected fields in your remaining sample files.</span></span>

4. <span data-ttu-id="5ef9f-156">Cliquez sur **Confirmer les champs** après avoir sélectionné les champs que vous souhaitez enregistrer.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-156">Click **Confirm fields** after you have selected the fields that you want to save.</span></span> </br>
 
    ![Confirmer les champs après avoir sélectionné les champs](../media/content-understanding/confirm-fields.png)</br> 
 
5. <span data-ttu-id="5ef9f-158">Sur la page **Sélectionnez les champs de formulaire que vous souhaitez enregistrer**, le nombre de champs que vous avez sélectionnés s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-158">On the **Select the form fields you want to save** page, it shows the number of fields you have selected.</span></span> <span data-ttu-id="5ef9f-159">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-159">Select **Done**.</span></span>

## <a name="step-4-train-and-test-your-model"></a><span data-ttu-id="5ef9f-160">Étape 4 : entraîner et tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="5ef9f-160">Step 4: Train and test your model</span></span>

<span data-ttu-id="5ef9f-161">Après avoir sélectionné les champs que vous souhaitez enregistrer, la page **Résumé du modèle** vous permet d’entraîner et de tester votre modèle.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-161">After selecting the fields you want to save, the **Model Summary** page lets you train and test your model.</span></span>

1. <span data-ttu-id="5ef9f-162">Sur la page **Résumé du modèle**, les champs enregistrés s’afficheront dans la section **Champs sélectionnés**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-162">On the **Model Summary** page, the saved fields will show in the **Selected fields** section.</span></span> <span data-ttu-id="5ef9f-163">Sélectionnez **Entraîner** pour commencer la formation sur vos fichiers d’exemple.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-163">Select **Train** to begin training on your example files.</span></span> <span data-ttu-id="5ef9f-164">Notez que cette opération peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-164">Note that this may take a few minutes to complete.</span></span></br>

     ![Sélectionner Entraîner les champs](../media/content-understanding/select-fields-train.png)</br> 

2. <span data-ttu-id="5ef9f-166">Lorsque vous voyez la notification indiquant que la formation est terminée, sélectionnez **Accéder à la page Informations**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-166">When you see the notification that training has completed, select **Go to details page**.</span></span> 

3. <span data-ttu-id="5ef9f-167">Sur la page **Informations sur le modèle**, vous pouvez choisir de tester le fonctionnement de votre modèle en sélectionnant **Test rapide**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-167">On the **Model details** page, you can choose to test how your model works by selecting **Quick test**.</span></span> <span data-ttu-id="5ef9f-168">Cela vous permet de glisser et déposer des fichiers sur la page et de voir si les champs sont détectés.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-168">This lets you drag and drop files to the page and see if the fields are detected.</span></span>

    ![Confirmer les champs](../media/content-understanding/select-fields-train.png)</br> 

2. <span data-ttu-id="5ef9f-170">Lorsque vous voyez la notification indiquant que la formation est terminée, sélectionnez **Accéder à la page Informations**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-170">When you see the notification that training has completed, select **Go to details page**.</span></span> 

3. <span data-ttu-id="5ef9f-171">Sur la page **Informations sur le modèle**, choisissez de tester le fonctionnement de votre modèle en sélectionnant **Test rapide**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-171">On the **Model details** page, choose to test how your model works by selecting **Quick test**.</span></span> <span data-ttu-id="5ef9f-172">Cela vous permet de glisser et déposer des fichiers sur la page et de voir si les champs sont détectés.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-172">This lets you drag and drop files to the page and see if the fields are detected.</span></span>

## <a name="step-5-publish-your-model"></a><span data-ttu-id="5ef9f-173">Étape 5 : publier votre modèle</span><span class="sxs-lookup"><span data-stu-id="5ef9f-173">Step 5: Publish your model</span></span>

1. <span data-ttu-id="5ef9f-174">Si vous êtes satisfait des résultats de votre modèle, sélectionnez **Publier** afin de pouvoir l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-174">If you are satisfied with the results of your model, select **Publish** to make it available for use.</span></span>

2. <span data-ttu-id="5ef9f-175">Une fois le modèle publié, sélectionnez **Utiliser le modèle**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-175">After the model is published, select **Use model**.</span></span> <span data-ttu-id="5ef9f-176">Cela crée un flux PowerAutomate qui peut s’exécuter dans votre bibliothèque de documents SharePoint et qui extrait les champs qui ont été identifiés dans le modèle. Ensuite, sélectionnez **Créer un flux**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-176">This creates a PowerAutomate flow that can run in your SharePoint document library and extracts the fields that have been identified in the model, then select **Create Flow**.</span></span>
  
3. <span data-ttu-id="5ef9f-177">Une fois terminé, vous verrez le message **Votre flux a été créé avec succès**.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-177">When completed, you will see the message **Your flow has been successfully created**.</span></span>
 
## <a name="step-6-use-your-model"></a><span data-ttu-id="5ef9f-178">Étape 6 : utiliser votre modèle</span><span class="sxs-lookup"><span data-stu-id="5ef9f-178">Step 6: Use your model</span></span>

<span data-ttu-id="5ef9f-179">Après avoir publié votre modèle et créé son flux PowerAutomate, vous pouvez l’utiliser dans votre bibliothèque de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-179">After publishing your model and creating it's PowerAutomate flow, you can use your model in your SharePoint document library.</span></span>

1. <span data-ttu-id="5ef9f-180">Après avoir publié votre modèle, sélectionnez **Accéder à SharePoint** pour accéder à votre bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-180">After publishing your model, select **Go to SharePoint** to go to your document library.</span></span>

2. <span data-ttu-id="5ef9f-181">Dans la vue du modèle de la bibliothèque de documents, notez que les champs que vous avez sélectionnés s’affichent désormais sous forme de colonnes.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-181">In the document library model view, notice that the fields you selected now display as columns.</span></span></br>

    ![Modèle de bibliothèque de documents appliqué](../media/content-understanding/doc-lib-view.png)</br> 

3. <span data-ttu-id="5ef9f-183">Notez que le lien Informations en regard de **Documents** indique qu’un modèle de traitement de formulaire est appliqué à cette bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-183">Notice that the information link next to **Documents** notes that a forms processing model is applied to this document library.</span></span>

    ![Bouton Informations](../media/content-understanding/info-button.png)</br>  

4. <span data-ttu-id="5ef9f-185">Téléchargez des fichiers dans votre bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-185">Upload files to your document library.</span></span> <span data-ttu-id="5ef9f-186">Tous les fichiers que le modèle identifie comme son type de contenu répertorient les fichiers dans votre vue et affichent les données extraites dans les colonnes.</span><span class="sxs-lookup"><span data-stu-id="5ef9f-186">Any files that the model identifies as it's content type lists the files in your view and displays the extracted data in the columns.</span></span></br>

    ![Terminé](../media/content-understanding/doc-lib-done.png)</br>  

## <a name="see-also"></a><span data-ttu-id="5ef9f-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ef9f-188">See Also</span></span>
  
[<span data-ttu-id="5ef9f-189">Documentation Power Automate</span><span class="sxs-lookup"><span data-stu-id="5ef9f-189">Power Automate documentation</span></span>](https://docs.microsoft.com/power-automate/)

[<span data-ttu-id="5ef9f-190">Formation : Améliorer les performances de votre entreprise avec AI Builder</span><span class="sxs-lookup"><span data-stu-id="5ef9f-190">Training: Improve business performance with AI Builder</span></span>](https://docs.microsoft.com/learn/paths/improve-business-performance-ai-builder/?source=learn)
