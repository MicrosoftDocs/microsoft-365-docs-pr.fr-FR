---
title: Application d’une étiquette de rétention à un modèle de présentation des documents
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 10/1/2020
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Cet article explique comment appliquer une étiquette de rétention à un modèle de présentation des documents
ms.openlocfilehash: 26ad64906c0e2a311d8b244e8e1596a8b975cc15
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48294917"
---
# <a name="apply-a-retention-label-to-a-document-understanding-model"></a><span data-ttu-id="19d24-103">Application d’une étiquette de rétention à un modèle de présentation des documents</span><span class="sxs-lookup"><span data-stu-id="19d24-103">Apply a retention label to a document understanding model</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSoL]

</br>

<span data-ttu-id="19d24-104">Vous pouvez facilement appliquer une [étiquette de rétention](https://docs.microsoft.com/microsoft-365/compliance/retention) à un modèle de présentation des documents dans Microsoft SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="19d24-104">You can easily apply a [retention label](https://docs.microsoft.com/microsoft-365/compliance/retention) to a document understanding model in Microsoft SharePoint Syntex.</span></span>

<span data-ttu-id="19d24-105">Les étiquettes de rétention permettent d’appliquer des paramètres de rétention aux documents identifiés par vos modèles de document.</span><span class="sxs-lookup"><span data-stu-id="19d24-105">Retention labels let you apply retention settings to the documents that your document understanding models identify.</span></span>  <span data-ttu-id="19d24-106">Par exemple, vous souhaitez que votre modèle identifie non seulement les documents d' *avis d’assurance* téléchargés vers votre bibliothèque de documents, mais aussi lui appliquer une balise de rétention de l' *entreprise* afin que ces documents ne puissent pas être supprimés de la bibliothèque de documents pendant la période spécifiée (les cinq prochains mois, par exemple).</span><span class="sxs-lookup"><span data-stu-id="19d24-106">For example, you want your model to not only identify any *Insurance notice* documents that are uploaded to your document library, but to also apply a *Business* retention tag to them so that these documents cannot be deleted from the document library for the specified time period (the next five months, for example).</span></span>

<span data-ttu-id="19d24-107">Vous pouvez appliquer une étiquette de rétention préexistante à votre modèle de compréhension de document par le biais de vos paramètres de modèle sur la page d’accueil de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="19d24-107">You can apply a pre-existing retention label to your document understanding model through your model settings on your model's home page.</span></span> 

> [!Important]
> <span data-ttu-id="19d24-108">Pour que les étiquettes de rétention puissent être appliquées à votre modèle de compréhension de contenu, elles doivent être [créées et publiées dans le centre de conformité Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/create-apply-retention-labels#how-to-create-and-publish-retention-labels).</span><span class="sxs-lookup"><span data-stu-id="19d24-108">For retention labels to be available to apply to your content understanding model, they need to be [created and published in the Microsoft 365 Compliance Center](https://docs.microsoft.com/microsoft-365/compliance/create-apply-retention-labels#how-to-create-and-publish-retention-labels).</span></span>

## <a name="to-add-a-retention-label-to-a-document-understanding-model"></a><span data-ttu-id="19d24-109">Pour ajouter une étiquette de rétention à un modèle de présentation de document</span><span class="sxs-lookup"><span data-stu-id="19d24-109">To add a retention label to a document understanding model</span></span>

1. <span data-ttu-id="19d24-110">À partir de la page d’accueil du modèle, sélectionnez **paramètres du modèle**.</span><span class="sxs-lookup"><span data-stu-id="19d24-110">From the model home page, select **Model settings**.</span></span></br>
2. <span data-ttu-id="19d24-111">Dans **paramètres du modèle**, dans la section **sécurité et conformité** , sélectionnez le menu **étiquette** de rétention pour afficher la liste des étiquettes de rétention disponibles pour que votre s’applique au modèle.</span><span class="sxs-lookup"><span data-stu-id="19d24-111">In **Model settings**, in the **Security and compliance** section, select the **Retention label** menu to see a list of retention labels that are available for your to apply to the model.</span></span></br>
 <span data-ttu-id="19d24-112">![Menu étiquette de rétention](../media/content-understanding/retention-labels-menu.png)</span><span class="sxs-lookup"><span data-stu-id="19d24-112">![Retention label menu](../media/content-understanding/retention-labels-menu.png)</span></span></br> 
3. <span data-ttu-id="19d24-113">Sélectionnez l’étiquette de rétention que vous souhaitez appliquer au modèle, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="19d24-113">Select the retention label you want to apply to the model, and then select **Save**.</span></span></br>

<span data-ttu-id="19d24-114">Après avoir appliqué l’étiquette de rétention à votre modèle, vous pouvez l’appliquer à un :</span><span class="sxs-lookup"><span data-stu-id="19d24-114">After applying the retention label to your model, you are able to apply it to a:</span></span>
- <span data-ttu-id="19d24-115">Nouvelle bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="19d24-115">New document library</span></span>
- <span data-ttu-id="19d24-116">Bibliothèque de documents à laquelle le modèle est déjà appliqué</span><span class="sxs-lookup"><span data-stu-id="19d24-116">Document library to which the model is already applied</span></span>
 
## <a name="apply-the-retention-label-to-a-document-library-to-which-the-model-is-already-applied"></a><span data-ttu-id="19d24-117">Appliquer l’étiquette de rétention à une bibliothèque de documents à laquelle le modèle est déjà appliqué</span><span class="sxs-lookup"><span data-stu-id="19d24-117">Apply the retention label to a document library to which the model is already applied</span></span>

<span data-ttu-id="19d24-118">Si votre modèle de présentation de document a déjà été appliqué à une bibliothèque de documents, vous pouvez effectuer les opérations suivantes pour synchroniser la mise à jour de l’étiquette de rétention afin de l’appliquer à la bibliothèque de documents :</span><span class="sxs-lookup"><span data-stu-id="19d24-118">If your document understanding model has already been applied to a document library, you can do the following to sync your retention label update to apply it to the document library:</span></span></br>

1. <span data-ttu-id="19d24-119">Sur la page d’accueil de votre modèle, dans la section **bibliothèques avec ce modèle** , sélectionnez la bibliothèque de documents à laquelle vous souhaitez appliquer la mise à jour des étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="19d24-119">On your model home page, in the **Libraries with this model** section, select the document library to which you want to apply the retention label update.</span></span> </br> 
2. <span data-ttu-id="19d24-120">Sélectionnez **synchroniser**.</span><span class="sxs-lookup"><span data-stu-id="19d24-120">Select **Sync**.</span></span> </br>
 <span data-ttu-id="19d24-121">![Modèle de synchronisation](../media/content-understanding/sync-model.png)</span><span class="sxs-lookup"><span data-stu-id="19d24-121">![Sync model](../media/content-understanding/sync-model.png)</span></span></br> 


<span data-ttu-id="19d24-122">Après avoir appliqué la mise à jour et la synchronisation avec votre modèle, vous pouvez vérifier qu’elle a été appliquée en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="19d24-122">After applying the update and syncing it to your model, you can confirm that it has been applied by doing the following:</span></span>

1. <span data-ttu-id="19d24-123">Dans le centre de contenu, dans la section **bibliothèques avec ce modèle** , cliquez sur la bibliothèque à laquelle le modèle mis à jour a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="19d24-123">In the content center, in the **Libraries with this model** section, click on the library to which your updated model was applied.</span></span> </br>
2. <span data-ttu-id="19d24-124">Dans la vue de votre bibliothèque de documents, sélectionnez l’icône des informations pour vérifier les propriétés du modèle.</span><span class="sxs-lookup"><span data-stu-id="19d24-124">In your document library view, select the information icon to check the model properties.</span></span></br>  
3. <span data-ttu-id="19d24-125">Dans la liste **modèles actifs** , sélectionnez votre modèle mis à jour.</span><span class="sxs-lookup"><span data-stu-id="19d24-125">In the **Active models** list, select your updated model.</span></span></br>
4. <span data-ttu-id="19d24-126">Dans la section **étiquette de rétention** , vous verrez le nom de l’étiquette de rétention appliquée.</span><span class="sxs-lookup"><span data-stu-id="19d24-126">In the **Retention label** section you will see the name of the applied retention label.</span></span></br>


<span data-ttu-id="19d24-127">Sur la page d’affichage de votre modèle dans votre bibliothèque de documents, une nouvelle colonne **étiquette de rétention** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="19d24-127">On your model's view page in your document library, a new **Retention label** column will display.</span></span>  <span data-ttu-id="19d24-128">Comme votre modèle classifie les fichiers qu’il identifie comme appartenant à son type de contenu et les répertorie dans la vue de la bibliothèque, la colonne de l’étiquette de rétention affichera également le nom de l’étiquette de rétention qui lui a été appliquée par le biais du modèle.</span><span class="sxs-lookup"><span data-stu-id="19d24-128">As your model classifies files it identifies as belonging to it's content type and lists them in the library view, the Retention label column will also display the name of the retention label that has been applied to it through the model.</span></span>


<span data-ttu-id="19d24-129">Par exemple, tous les documents d' *avis d’assurance* que votre modèle identifie ont également l’étiquette de rétention de l' *entreprise* appliquée, ce qui les empêche de se supprimer de la bibliothèque de documents pendant cinq mois.</span><span class="sxs-lookup"><span data-stu-id="19d24-129">For example, all *Insurance notice* documents that your model identifies will also have the *Business* retention label applied to them, preventing them from being deleted from the document library for five months.</span></span> <span data-ttu-id="19d24-130">Si vous tentez de supprimer le fichier de la bibliothèque de documents, une erreur s’affiche indiquant qu’il n’est pas autorisé en raison de l’étiquette de rétention appliquée.</span><span class="sxs-lookup"><span data-stu-id="19d24-130">If an attempt is made to delete the file from the document library, an error will display saying it is not allowed because of the applied retention label.</span></span>

## <a name="see-also"></a><span data-ttu-id="19d24-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19d24-131">See Also</span></span>
[<span data-ttu-id="19d24-132">Créer un classifieur</span><span class="sxs-lookup"><span data-stu-id="19d24-132">Create a classifier</span></span>](create-a-classifier.md)</br>
[<span data-ttu-id="19d24-133">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="19d24-133">Create an extractor</span></span>](create-an-extractor.md)</br>
[<span data-ttu-id="19d24-134">Présentation de l’explication des documents</span><span class="sxs-lookup"><span data-stu-id="19d24-134">Document Understanding overview</span></span>](document-understanding-overview.md)</br>
[<span data-ttu-id="19d24-135">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="19d24-135">Create a form processing model</span></span>](create-a-form-processing-model.md)  
