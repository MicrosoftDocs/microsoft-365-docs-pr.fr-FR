---
title: Appliquer un modèle de présentation de document à une bibliothèque de documents
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-syntex
localization_priority: Normal
description: Découvrir comment appliquer un modèle publié à une bibliothèque de documents SharePoint
ms.openlocfilehash: cda9de43d0139c52f950527eb75d050602005fd2
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843293"
---
# <a name="apply-a-document-understanding-model-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="bc836-103">Appliquer un modèle de présentation de document dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="bc836-103">Apply a document understanding model in Microsoft SharePoint Syntex</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSoL]

</br>

<span data-ttu-id="bc836-104">Une fois que vous avez publié votre modèle de présentation de document, vous pouvez l’appliquer à une ou plusieurs bibliothèques de documents SharePoint dans votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bc836-104">After publishing your document understanding model, you can apply it to one or more SharePoint document library in your Microsoft 365 tenant.</span></span>

> [!NOTE]
> <span data-ttu-id="bc836-105">Vous pouvez uniquement appliquer le modèle aux bibliothèques de documents auxquelles vous avez accès.</span><span class="sxs-lookup"><span data-stu-id="bc836-105">You are only able to apply the model to document libraries that you have access to.</span></span>


## <a name="apply-your-model-to-a-document-library"></a><span data-ttu-id="bc836-106">Appliquez votre modèle à une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="bc836-106">Apply your model to a document library.</span></span>

<span data-ttu-id="bc836-107">Pour appliquer votre modèle à une bibliothèque de documents SharePoint :</span><span class="sxs-lookup"><span data-stu-id="bc836-107">To apply your model to to a SharePoint document library:</span></span>

1. <span data-ttu-id="bc836-108">Sur la page d’accueil du modèle, dans la vignette **Appliquer le modèle aux bibliothèques** , sélectionnez **Publier le modèle**.</span><span class="sxs-lookup"><span data-stu-id="bc836-108">On model home page, on the **Apply model to libraries** tile, select **Publish model**.</span></span> <span data-ttu-id="bc836-109">Vous pouvez également sélectionner **+ Ajouter une bibliothèque** dans la section **Bibliothèques avec ce modèle**.</span><span class="sxs-lookup"><span data-stu-id="bc836-109">Or you can select  **+Add Library** in the **Libraries with this model** section.</span></span> </br>

    ![Ajouter un modèle à la bibliothèque](../media/content-understanding/apply-to-library.png)</br>

2. <span data-ttu-id="bc836-111">Vous pouvez ensuite sélectionner le site SharePoint contenant la bibliothèque de documents à laquelle vous voulez appliquer le modèle.</span><span class="sxs-lookup"><span data-stu-id="bc836-111">You can then select the SharePoint site that contains the document library that you want to apply the model to.</span></span> <span data-ttu-id="bc836-112">Si le site n’apparaît pas dans la liste, utilisez la zone de recherche pour le trouver.</span><span class="sxs-lookup"><span data-stu-id="bc836-112">If the site does not show in the list, use the search box to find it.</span></span></br>

    ![Sélection d’un site](../media/content-understanding/site-search.png)</br>

    > [!NOTE]
    > <span data-ttu-id="bc836-114">Vous devez disposer d’autorisations *Gérer la liste* ou de droits *Modifier* sur la bibliothèque de documents à laquelle vous appliquez le modèle.</span><span class="sxs-lookup"><span data-stu-id="bc836-114">You must have *Manage List* permissions or *Edit* rights to the document library you are applying the model to.</span></span></br>

3. <span data-ttu-id="bc836-115">Une fois le site sélectionné, sélectionnez la bibliothèque de documents à laquelle vous voulez appliquer le modèle.</span><span class="sxs-lookup"><span data-stu-id="bc836-115">After selecting the site, select the document library to which you want to apply the model.</span></span> <span data-ttu-id="bc836-116">Dans l’exemple, sélectionnez la bibliothèque de documents *Documents* à partir du site de *Suivi de cas contoso*.</span><span class="sxs-lookup"><span data-stu-id="bc836-116">In the sample, select the *Documents* document library from the *Contoso Case Tracking* site.</span></span></br>

    ![Sélectionner une bibliothèque de documents](../media/content-understanding/select-doc-library.png)</br>

4. <span data-ttu-id="bc836-118">Étant donné que le modèle est associé à un type de contenu, lorsque vous l’appliquez à la bibliothèque, le type de contenu et son affichage sont ajoutés aux étiquettes que vous avez extraites sous forme de colonnes.</span><span class="sxs-lookup"><span data-stu-id="bc836-118">Since the model is associated to a content type, when you apply it to the library it will add the content type and its view with the labels you extracted showing as columns.</span></span> <span data-ttu-id="bc836-119">Cet affichage est l’affichage par défaut de la bibliothèque par défaut, mais vous pouvez choisir de ne pas l’utiliser par défaut en sélectionnant **Paramètres avancés** et en désactivant la case à cocher **Définir cette nouvelle vue comme par défaut**.</span><span class="sxs-lookup"><span data-stu-id="bc836-119">This view is the library's default view by default, but you can optionally choose to not have it be the default view by selecting **Advanced settings** and deselecting **Set this new view as default**.</span></span></br>

    ![Vue de la bibliothèque](../media/content-understanding/library-view.png)</br>

5. <span data-ttu-id="bc836-121">Sélectionnez **Ajouter** pour appliquer le modèle à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="bc836-121">Select **Add** to apply the model to the library.</span></span> 
6. <span data-ttu-id="bc836-122">Dans la page d’accueil du modèle, dans la section **Bibliothèques avec ce modèle**, l’URL du site SharePoint doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="bc836-122">On the model home page, in the **Libraries with this model** section, you should see the URL to the SharePoint site listed.</span></span></br>

    ![Bibliothèque sélectionnée](../media/content-understanding/selected-library.png)</br>

7. <span data-ttu-id="bc836-124">Accédez à votre bibliothèque de documents et vérifiez que vous êtes dans la vue bibliothèque de documents du modèle.</span><span class="sxs-lookup"><span data-stu-id="bc836-124">Go to your document library and make sure you are in the model's document library view.</span></span> <span data-ttu-id="bc836-125">Notez que si vous sélectionnez le bouton informations en regard du nom de la bibliothèque de documents, un message indique qu’un modèle est appliqué à la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="bc836-125">Notice that if you select the information button next to the document library name, a message notes that the document library has a model applied to it.</span></span>

    ![Vue informations](../media/content-understanding/info-du.png)</br> 

    <span data-ttu-id="bc836-127">Vous pouvez sélectionner **Afficher les modèles actifs** pour afficher des détails sur les modèles appliqués à la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="bc836-127">You can the select **View active models** to see details about any models that are applied to the document library.</span></span>

8. <span data-ttu-id="bc836-128">Dans le volet **Modèles actifs**, vous pouvez afficher les modèles appliqués à la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="bc836-128">In the **Active models** pane, you can see the models that are applied to the document library.</span></span> <span data-ttu-id="bc836-129">Sélectionnez un modèle pour afficher plus d’informations le concernant, par exemple une description du modèle, qui a publié le modèle et si le modèle applique une étiquette de rétention aux fichiers qu’il classifie.</span><span class="sxs-lookup"><span data-stu-id="bc836-129">Select a model to see more details about it, such as a description of the model, who published the model, and if the model applies a retention label to the files it classifies.</span></span>

    ![Volet Modèles actifs](../media/content-understanding/active-models.png)</br> 

<span data-ttu-id="bc836-131">Une fois le modèle appliqué à la bibliothèque de documents, vous pouvez commencer à télécharger des documents sur le site et afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="bc836-131">After applying the model to the document library, you can begin uploading documents to the site and see the results.</span></span>

<span data-ttu-id="bc836-132">Le modèle identifie les fichiers avec le type de contenu associé au modèle et les répertorie dans votre affichage.</span><span class="sxs-lookup"><span data-stu-id="bc836-132">The model identifies any files with model’s associated content type and lists them in your view.</span></span> <span data-ttu-id="bc836-133">Si votre modèle inclut des extracteurs, l’affichage affiche les colonnes des données que vous extrayez à partir de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="bc836-133">If your model has any extractors, the view displays columns for the data you are extracting from each file.</span></span>

### <a name="apply-the-model-to-files-already-in-the-document-library"></a><span data-ttu-id="bc836-134">Appliquer le modèle aux fichiers figurant déjà dans la bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="bc836-134">Apply the model to files already in the document library</span></span>

<span data-ttu-id="bc836-135">Lorsqu’un modèle appliqué traite tous les fichiers téléchargés vers la bibliothèque de documents une fois qu’il est appliqué, vous pouvez également effectuer les opérations suivantes pour exécuter le modèle sur des fichiers qui existent déjà dans la bibliothèque de documents avant l’application du modèle :</span><span class="sxs-lookup"><span data-stu-id="bc836-135">While an applied model processes all files uploaded to the document library after it is applied, you can also do the following to run the model on files that already exists in the document library prior to the model being applied:</span></span>

1. <span data-ttu-id="bc836-136">Dans votre bibliothèque de documents, sélectionnez les fichiers que vous voulez traiter par votre modèle.</span><span class="sxs-lookup"><span data-stu-id="bc836-136">In your document library, select the files that you want to be processed by your model.</span></span>
2. <span data-ttu-id="bc836-137">Une fois que vous avez sélectionné vos fichiers, **Classer et extraire** s’affiche dans le ruban de la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="bc836-137">After selecting your files, **Classify and extract** will appear in the document library ribbon.</span></span> <span data-ttu-id="bc836-138">Sélectionnez **Classer et extraire**.</span><span class="sxs-lookup"><span data-stu-id="bc836-138">Select **Classify and extract**.</span></span>
3. <span data-ttu-id="bc836-139">Les fichiers que vous avez sélectionnés sont ajoutés à la file d’attente à traiter.</span><span class="sxs-lookup"><span data-stu-id="bc836-139">The files you selected will be added to the queue to be processed.</span></span>

      ![Classer et extraire](../media/content-understanding/extract-classify.png)</br> 

> [!NOTE]
> <span data-ttu-id="bc836-141">Vous pouvez copier des fichiers individuels dans une bibliothèque et les appliquer à un modèle, mais pas des dossiers.</span><span class="sxs-lookup"><span data-stu-id="bc836-141">You can copy individual files to a library and apply them to a model, but not folders.</span></span>

### <a name="the-classification-date-field"></a><span data-ttu-id="bc836-142">Champ Date de classification</span><span class="sxs-lookup"><span data-stu-id="bc836-142">The Classification Date field</span></span>

<span data-ttu-id="bc836-143">Lorsqu’un document SharePoint Syntex comprenant ou un modèle de traitement de formulaire est appliqué à une bibliothèque de documents, un champ <b>Date de classification</b> est inclus dans le schéma de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="bc836-143">When a SharePoint Syntex document understanding or form processing model is applied to a document library, a <b> Classification date </b> field is included in the library schema.</span></span> <span data-ttu-id="bc836-144">Par défaut, ce champ est vide, mais lorsque des documents sont traitées et classifiées par modèle, ce champ est mis à jour avec l’horodatage d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="bc836-144">By default this field is empty, but when documents are processed and classified by a model, this field is updated with a date-time stamp of completion.</span></span> 

   ![Colonne de date de classification](../media/content-understanding/class-date-column.png)</br> 

<span data-ttu-id="bc836-146">Le champ Date de classification est utilisé par le déclencheur [<b>Lorsqu’un fichier est classifié par un modèle de contenu</b>'](/connectors/sharepointonline/#when-a-file-is-classified-by-a-content-understanding-model) pour exécuter un flux Power Automate après qu’un modèle de compréhension de contenu Syntex a terminé de traiter un fichier et mis à jour le champ « Date de classification ».</span><span class="sxs-lookup"><span data-stu-id="bc836-146">The Classification date field is used by the [<b>When a file is classified by a content understanding model</b> trigger](/connectors/sharepointonline/#when-a-file-is-classified-by-a-content-understanding-model) to run a Power Automate flow after a Syntex content understanding model has finished processing a file and updated the "Classification date" field.</span></span>

   ![Déclencheur de flux](../media/content-understanding/trigger.png)</br>

<span data-ttu-id="bc836-148">Le déclencheur <b>Lorsqu'un fichier est classifié selon un modèle de compréhension du contenu</b> peut ensuite être utilisé pour démarrer un autre flux de travail à l’aide d’informations extraites du fichier.</span><span class="sxs-lookup"><span data-stu-id="bc836-148">The <b>When a file is classified by a content understanding model</b> trigger can then be used to start another workflow using any  extracted information from the file.</span></span>



## <a name="see-also"></a><span data-ttu-id="bc836-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc836-149">See Also</span></span>
[<span data-ttu-id="bc836-150">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="bc836-150">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="bc836-151">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="bc836-151">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="bc836-152">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="bc836-152">Document Understanding overview</span></span>](document-understanding-overview.md)
