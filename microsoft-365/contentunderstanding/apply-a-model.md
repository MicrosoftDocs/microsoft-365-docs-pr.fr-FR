---
title: Appliquer un modèle de présentation de document à une bibliothèque de documents (aperçu)
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.service: o365-administration
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Découvrez comment appliquer un modèle publié à une bibliothèque de documents SharePoint.
ms.openlocfilehash: 8a4931f4b7a936caeb99d7f8c07deefdac62919b
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47950247"
---
# <a name="apply-a-document-understanding-model-preview"></a><span data-ttu-id="cd683-103">Appliquer un modèle de présentation de document (aperçu)</span><span class="sxs-lookup"><span data-stu-id="cd683-103">Apply a document understanding model (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="cd683-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="cd683-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="cd683-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="cd683-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSoL]

</br>

<span data-ttu-id="cd683-106">Après avoir publié votre modèle de présentation de document, vous pouvez l’appliquer à une bibliothèque de documents SharePoint dans votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cd683-106">After publishing your document understanding model, you can apply it to a SharePoint document library in your Microsoft 365 tenant.</span></span>

> [!Note]
> <span data-ttu-id="cd683-107">Vous ne pourrez appliquer le modèle qu’aux bibliothèques de documents auxquelles vous avez accès.</span><span class="sxs-lookup"><span data-stu-id="cd683-107">You will only be able to apply the model to document libraries that you have access to.</span></span>


## <a name="apply-your-model-to-a-document-library"></a><span data-ttu-id="cd683-108">Appliquer votre modèle à une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="cd683-108">Apply your model to a document library.</span></span>

<span data-ttu-id="cd683-109">Pour appliquer votre modèle à une bibliothèque de documents SharePoint :</span><span class="sxs-lookup"><span data-stu-id="cd683-109">To apply your model to to a SharePoint document library:</span></span>

1. <span data-ttu-id="cd683-110">Sur la page d’accueil du modèle, dans la vignette **appliquer le modèle aux bibliothèques** , sélectionnez **publier le modèle**.</span><span class="sxs-lookup"><span data-stu-id="cd683-110">On the model home page, on the **Apply model to libraries** tile, select **Publish model**.</span></span> <span data-ttu-id="cd683-111">Ou vous pouvez sélectionner l’option  **+ Ajouter une bibliothèque** dans la section **bibliothèques avec ce modèle** .</span><span class="sxs-lookup"><span data-stu-id="cd683-111">Or you can  select  **+Add Library** in the **Libraries with this model** section.</span></span> </br>

    ![Ajouter un modèle à la bibliothèque](../media/content-understanding/apply-to-library.png)</br>

2. <span data-ttu-id="cd683-113">Vous pouvez ensuite sélectionner le site SharePoint qui contient la bibliothèque de documents à laquelle vous souhaitez appliquer le modèle.</span><span class="sxs-lookup"><span data-stu-id="cd683-113">You can then select the SharePoint site that contains the document library that you want to apply the model to.</span></span> <span data-ttu-id="cd683-114">Si le site ne s’affiche pas dans la liste, utilisez la zone de recherche pour le trouver.</span><span class="sxs-lookup"><span data-stu-id="cd683-114">If the site does not show in the list, use the search box to find it.</span></span></br>

    ![Sélectionner un site](../media/content-understanding/site-search.png)</br>

    > [!Note]
    > <span data-ttu-id="cd683-116">Vous devez disposer des autorisations *gérer les listes* ou *modifier* les droits sur la bibliothèque de documents à laquelle vous appliquez le modèle.</span><span class="sxs-lookup"><span data-stu-id="cd683-116">You must have *Manage List* permissions or *Edit* rights to the document library you are applying the model to.</span></span></br>

3. <span data-ttu-id="cd683-117">Après avoir sélectionné le site, vous devez sélectionner la bibliothèque de documents à laquelle vous souhaitez appliquer le modèle.</span><span class="sxs-lookup"><span data-stu-id="cd683-117">After selecting the site, you then need to select the document library to which you want to apply the model.</span></span> <span data-ttu-id="cd683-118">Dans l’exemple, nous sélectionnons la bibliothèque de documents *documents* à partir du site de *suivi de cas contoso* .</span><span class="sxs-lookup"><span data-stu-id="cd683-118">In the example, we are selecting the *Documents* document library from the *Contoso Case Tracking* site.</span></span></br>

    ![Sélectionner une bibliothèque de documents](../media/content-understanding/select-doc-library.png)</br>

4. <span data-ttu-id="cd683-120">Étant donné que le modèle est associé à un type de contenu, lorsque vous l’appliquez à la bibliothèque, il crée un affichage pour le type de contenu avec les étiquettes extraites sous forme de colonnes.</span><span class="sxs-lookup"><span data-stu-id="cd683-120">Since the model is associated to a content type, when you apply it to the library it will create a view for the content type with the labels you extracted showing as columns.</span></span> <span data-ttu-id="cd683-121">Cet affichage est l’affichage par défaut de la bibliothèque, mais vous pouvez choisir de ne pas l’afficher par défaut en sélectionnant **Paramètres avancés** et en désélectionnant **définir cette nouvelle vue comme valeur par défaut**.</span><span class="sxs-lookup"><span data-stu-id="cd683-121">This view will be the library's default view by default, but you can optionally choose to not have it be the default view by selecting **Advanced settings** and deselecting **Set this new view as default**.</span></span></br>

    ![Affichage de la bibliothèque](../media/content-understanding/library-view.png)</br>

5. <span data-ttu-id="cd683-123">Sélectionnez **Ajouter** pour appliquer le modèle à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="cd683-123">Select **Add** to apply the model to the library.</span></span> 
6. <span data-ttu-id="cd683-124">Sur la page d’accueil du modèle, dans la section **bibliothèques avec ce modèle** , vous verrez l’URL du site SharePoint dans la zone.</span><span class="sxs-lookup"><span data-stu-id="cd683-124">On the model home page, in the **Libraries with this model** section, you will see the URL to the SharePoint site listed.</span></span></br>

    ![Affichage de la bibliothèque](../media/content-understanding/selected-library.png)</br>

7. <span data-ttu-id="cd683-126">Accédez à votre bibliothèque de documents et assurez-vous que vous êtes dans la vue bibliothèque de documents du modèle.</span><span class="sxs-lookup"><span data-stu-id="cd683-126">Go to your document library and make sure you are in the model's document library view.</span></span> <span data-ttu-id="cd683-127">Vous remarquerez que si vous sélectionnez le bouton informations en regard du nom de la bibliothèque de documents, un message indique que votre modèle a été appliqué à la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="cd683-127">You'll notice that if you select the information button next to the document library name, a message will note that your model has been applied to the document library.</span></span>

    ![Affichage de la bibliothèque](../media/content-understanding/info-du.png)</br> 


<span data-ttu-id="cd683-129">Après avoir appliqué le modèle à la bibliothèque de documents, vous pouvez commencer à télécharger des documents sur le site et voir les résultats.</span><span class="sxs-lookup"><span data-stu-id="cd683-129">After applying the model to the document library, you can begin uploading documents to the site and see the results.</span></span>

<span data-ttu-id="cd683-130">Le modèle identifie les fichiers dont le type de contenu est associé au modèle et les répertorie dans votre vue.</span><span class="sxs-lookup"><span data-stu-id="cd683-130">The model will identify any files with model’s associated content type and will list them in your view.</span></span> <span data-ttu-id="cd683-131">Si votre modèle comporte des extracteurs, l’affichage affiche les colonnes des données que vous extrayez de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="cd683-131">If your model has any extractors, the view will display columns for the data you are extracting from each file.</span></span>

### <a name="apply-the-model-to-files-already-in-the-document-library"></a><span data-ttu-id="cd683-132">Appliquer le modèle aux fichiers figurant déjà dans la bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="cd683-132">Apply the model to files already in the document library</span></span>

<span data-ttu-id="cd683-133">Lorsqu’un modèle appliqué traite tous les fichiers téléchargés vers la bibliothèque de documents après son application, vous pouvez également effectuer les opérations suivantes pour exécuter le modèle sur des fichiers qui existaient déjà dans la bibliothèque de documents avant l’application du modèle :</span><span class="sxs-lookup"><span data-stu-id="cd683-133">While an applied model will process all files uploaded to the document library after it is applied, you can also do the following to run the model on files that already existed in the document library prior to the model being applied:</span></span>

1. <span data-ttu-id="cd683-134">Dans votre bibliothèque de documents, sélectionnez les fichiers que vous souhaitez traiter par votre modèle.</span><span class="sxs-lookup"><span data-stu-id="cd683-134">In your document library, select the files that you want to be processed by your model.</span></span>
2. <span data-ttu-id="cd683-135">Une fois que vous avez sélectionné vos fichiers, **classifier et extraire** apparaît dans le ruban de la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="cd683-135">After selecting your files, **Classify and extract** will appear in the document library ribbon.</span></span> <span data-ttu-id="cd683-136">Sélectionnez **classifier et extraire**.</span><span class="sxs-lookup"><span data-stu-id="cd683-136">Select **Classify and extract**.</span></span>
3. <span data-ttu-id="cd683-137">Les fichiers que vous avez sélectionnés seront ajoutés à la file d’attente pour être traités.</span><span class="sxs-lookup"><span data-stu-id="cd683-137">The files you selected will be added to the queue to be processed.</span></span>

      ![Classer et extraire](../media/content-understanding/extract-classify.png)</br> 





## <a name="see-also"></a><span data-ttu-id="cd683-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd683-139">See Also</span></span>
[<span data-ttu-id="cd683-140">Créer un classifieur</span><span class="sxs-lookup"><span data-stu-id="cd683-140">Create a classifier</span></span>](create-a-classifier.md)</br>
[<span data-ttu-id="cd683-141">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="cd683-141">Create an extractor</span></span>](create-an-extractor.md)</br>
[<span data-ttu-id="cd683-142">Présentation de l’explication des documents</span><span class="sxs-lookup"><span data-stu-id="cd683-142">Document Understanding overview</span></span>](document-understanding-overview.md)</br>
[<span data-ttu-id="cd683-143">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="cd683-143">Create a form processing model</span></span>](create-a-form-processing-model.md)  




