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
localization_priority: Priority
description: Découvrir comment appliquer un modèle publié à une bibliothèque de documents SharePoint
ms.openlocfilehash: 742c6b7088619579f6157e20de63fe311039d6e2
ms.sourcegitcommit: 162c01dfaa2fdb3225ce4c24964c1065ce22ed5d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2021
ms.locfileid: "49975930"
---
# <a name="apply-a-document-understanding-model-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="4c585-103">Appliquer un modèle de présentation de document dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="4c585-103">Apply a document understanding model in Microsoft SharePoint Syntex</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSoL]

</br>

<span data-ttu-id="4c585-104">Une fois que vous avez publié votre modèle de présentation de document, vous pouvez l’appliquer à une ou plusieurs bibliothèques de documents SharePoint dans votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c585-104">After publishing your document understanding model, you can apply it to one or more SharePoint document library in your Microsoft 365 tenant.</span></span>

> [!NOTE]
> <span data-ttu-id="4c585-105">Vous pouvez uniquement appliquer le modèle aux bibliothèques de documents auxquelles vous avez accès.</span><span class="sxs-lookup"><span data-stu-id="4c585-105">You are only able to apply the model to document libraries that you have access to.</span></span>


## <a name="apply-your-model-to-a-document-library"></a><span data-ttu-id="4c585-106">Appliquez votre modèle à une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="4c585-106">Apply your model to a document library.</span></span>

<span data-ttu-id="4c585-107">Pour appliquer votre modèle à une bibliothèque de documents SharePoint :</span><span class="sxs-lookup"><span data-stu-id="4c585-107">To apply your model to to a SharePoint document library:</span></span>

1. <span data-ttu-id="4c585-108">Sur la page d’accueil du modèle, dans la vignette **Appliquer le modèle aux bibliothèques** , sélectionnez **Publier le modèle**.</span><span class="sxs-lookup"><span data-stu-id="4c585-108">On model home page, on the **Apply model to libraries** tile, select **Publish model**.</span></span> <span data-ttu-id="4c585-109">Vous pouvez également sélectionner **+ Ajouter une bibliothèque** dans la section **Bibliothèques avec ce modèle**.</span><span class="sxs-lookup"><span data-stu-id="4c585-109">Or you can select  **+Add Library** in the **Libraries with this model** section.</span></span> </br>

    ![Ajouter un modèle à la bibliothèque](../media/content-understanding/apply-to-library.png)</br>

2. <span data-ttu-id="4c585-111">Vous pouvez ensuite sélectionner le site SharePoint contenant la bibliothèque de documents à laquelle vous voulez appliquer le modèle.</span><span class="sxs-lookup"><span data-stu-id="4c585-111">You can then select the SharePoint site that contains the document library that you want to apply the model to.</span></span> <span data-ttu-id="4c585-112">Si le site n’apparaît pas dans la liste, utilisez la zone de recherche pour le trouver.</span><span class="sxs-lookup"><span data-stu-id="4c585-112">If the site does not show in the list, use the search box to find it.</span></span></br>

    ![Sélection d’un site](../media/content-understanding/site-search.png)</br>

    > [!NOTE]
    > <span data-ttu-id="4c585-114">Vous devez disposer d’autorisations *Gérer la liste* ou de droits *Modifier* sur la bibliothèque de documents à laquelle vous appliquez le modèle.</span><span class="sxs-lookup"><span data-stu-id="4c585-114">You must have *Manage List* permissions or *Edit* rights to the document library you are applying the model to.</span></span></br>

3. <span data-ttu-id="4c585-115">Une fois le site sélectionné, sélectionnez la bibliothèque de documents à laquelle vous voulez appliquer le modèle.</span><span class="sxs-lookup"><span data-stu-id="4c585-115">After selecting the site, select the document library to which you want to apply the model.</span></span> <span data-ttu-id="4c585-116">Dans l’exemple, sélectionnez la bibliothèque de documents *Documents* à partir du site de *Suivi de cas contoso*.</span><span class="sxs-lookup"><span data-stu-id="4c585-116">In the sample, select the *Documents* document library from the *Contoso Case Tracking* site.</span></span></br>

    ![Sélectionner une bibliothèque de documents](../media/content-understanding/select-doc-library.png)</br>

4. <span data-ttu-id="4c585-118">Étant donné que le modèle est associé à un type de contenu, lorsque vous l’appliquez à la bibliothèque, le type de contenu et son affichage sont ajoutés aux étiquettes que vous avez extraites sous forme de colonnes.</span><span class="sxs-lookup"><span data-stu-id="4c585-118">Since the model is associated to a content type, when you apply it to the library it will add the content type and its view with the labels you extracted showing as columns.</span></span> <span data-ttu-id="4c585-119">Cet affichage est l’affichage par défaut de la bibliothèque par défaut, mais vous pouvez choisir de ne pas l’utiliser par défaut en sélectionnant **Paramètres avancés** et en désactivant la case à cocher **Définir cette nouvelle vue comme par défaut**.</span><span class="sxs-lookup"><span data-stu-id="4c585-119">This view is the library's default view by default, but you can optionally choose to not have it be the default view by selecting **Advanced settings** and deselecting **Set this new view as default**.</span></span></br>

    ![Vue de la bibliothèque](../media/content-understanding/library-view.png)</br>

5. <span data-ttu-id="4c585-121">Sélectionnez **Ajouter** pour appliquer le modèle à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4c585-121">Select **Add** to apply the model to the library.</span></span> 
6. <span data-ttu-id="4c585-122">Dans la page d’accueil du modèle, dans la section **Bibliothèques avec ce modèle**, l’URL du site SharePoint doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="4c585-122">On the model home page, in the **Libraries with this model** section, you should see the URL to the SharePoint site listed.</span></span></br>

    ![Bibliothèque sélectionnée](../media/content-understanding/selected-library.png)</br>

7. <span data-ttu-id="4c585-124">Accédez à votre bibliothèque de documents et vérifiez que vous êtes dans la vue bibliothèque de documents du modèle.</span><span class="sxs-lookup"><span data-stu-id="4c585-124">Go to your document library and make sure you are in the model's document library view.</span></span> <span data-ttu-id="4c585-125">Notez que si vous sélectionnez le bouton informations en regard du nom de la bibliothèque de documents, un message indique que votre modèle a été appliqué à la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="4c585-125">Notice that if you select the information button next to the document library name, a message notes that your model has been applied to the document library.</span></span>

    ![Vue informations](../media/content-understanding/info-du.png)</br> 


<span data-ttu-id="4c585-127">Une fois le modèle appliqué à la bibliothèque de documents, vous pouvez commencer à télécharger des documents sur le site et afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="4c585-127">After applying the model to the document library, you can begin uploading documents to the site and see the results.</span></span>

<span data-ttu-id="4c585-128">Le modèle identifie les fichiers avec le type de contenu associé au modèle et les répertorie dans votre affichage.</span><span class="sxs-lookup"><span data-stu-id="4c585-128">The model identifies any files with model’s associated content type and lists them in your view.</span></span> <span data-ttu-id="4c585-129">Si votre modèle inclut des extracteurs, l’affichage affiche les colonnes des données que vous extrayez à partir de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="4c585-129">If your model has any extractors, the view displays columns for the data you are extracting from each file.</span></span>

### <a name="apply-the-model-to-files-already-in-the-document-library"></a><span data-ttu-id="4c585-130">Appliquer le modèle aux fichiers figurant déjà dans la bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="4c585-130">Apply the model to files already in the document library</span></span>

<span data-ttu-id="4c585-131">Lorsqu’un modèle appliqué traite tous les fichiers téléchargés vers la bibliothèque de documents une fois qu’il est appliqué, vous pouvez également effectuer les opérations suivantes pour exécuter le modèle sur des fichiers qui existent déjà dans la bibliothèque de documents avant l’application du modèle :</span><span class="sxs-lookup"><span data-stu-id="4c585-131">While an applied model processes all files uploaded to the document library after it is applied, you can also do the following to run the model on files that already exists in the document library prior to the model being applied:</span></span>

1. <span data-ttu-id="4c585-132">Dans votre bibliothèque de documents, sélectionnez les fichiers que vous voulez traiter par votre modèle.</span><span class="sxs-lookup"><span data-stu-id="4c585-132">In your document library, select the files that you want to be processed by your model.</span></span>
2. <span data-ttu-id="4c585-133">Une fois que vous avez sélectionné vos fichiers, **Classer et extraire** s’affiche dans le ruban de la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="4c585-133">After selecting your files, **Classify and extract** will appear in the document library ribbon.</span></span> <span data-ttu-id="4c585-134">Sélectionnez **Classer et extraire**.</span><span class="sxs-lookup"><span data-stu-id="4c585-134">Select **Classify and extract**.</span></span>
3. <span data-ttu-id="4c585-135">Les fichiers que vous avez sélectionnés sont ajoutés à la file d’attente à traiter.</span><span class="sxs-lookup"><span data-stu-id="4c585-135">The files you selected will be added to the queue to be processed.</span></span>

      ![Classer et extraire](../media/content-understanding/extract-classify.png)</br> 

> [!NOTE]
> <span data-ttu-id="4c585-137">Vous pouvez copier des fichiers individuels dans une bibliothèque et les appliquer à un modèle, mais pas des dossiers.</span><span class="sxs-lookup"><span data-stu-id="4c585-137">You can copy individual files to a library and apply them to a model, but not folders.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c585-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c585-138">See Also</span></span>
[<span data-ttu-id="4c585-139">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="4c585-139">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="4c585-140">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="4c585-140">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="4c585-141">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="4c585-141">Document Understanding overview</span></span>](document-understanding-overview.md)


