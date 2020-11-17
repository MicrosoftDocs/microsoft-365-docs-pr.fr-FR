---
title: Appliquer une étiquette de rétention à un modèle de compréhension de document
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: enabler-strategic
localization_priority: Priority
description: Cet article vous explique comment appliquer une étiquette de rétention à un modèle de compréhension de document
ms.openlocfilehash: 2e6d300b63a173d01488406485cffa44fab4278e
ms.sourcegitcommit: e7bf23df4852b78912229d1d38ec475223597f34
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "49087474"
---
# <a name="apply-a-retention-label-to-a-document-understanding-model"></a><span data-ttu-id="b5144-103">Appliquer une étiquette de rétention à un modèle de compréhension de document</span><span class="sxs-lookup"><span data-stu-id="b5144-103">Apply a retention label to a document understanding model</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4GydO]  

</br>


<span data-ttu-id="b5144-104">Vous pouvez facilement appliquer une [étiquette de rétention](https://docs.microsoft.com/microsoft-365/compliance/retention) à un modèle de compréhension de document dans Microsoft SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="b5144-104">You can easily apply a [retention label](https://docs.microsoft.com/microsoft-365/compliance/retention) to a document understanding model in Microsoft SharePoint Syntex.</span></span>

<span data-ttu-id="b5144-105">Les étiquettes de rétention vous permettent d’appliquer des paramètres de rétention aux documents identifiés par vos modèles de compréhension de document.</span><span class="sxs-lookup"><span data-stu-id="b5144-105">Retention labels let you apply retention settings to the documents that your document understanding models identify.</span></span>  <span data-ttu-id="b5144-106">Par exemple, vous souhaitez que votre modèle identifie tous les documents d’*avis d’assurance* qui sont téléchargés dans votre bibliothèque de documents, mais également qu’il leur applique une étiquette de rétention *Entreprise*, afin que ces documents ne puissent pas être supprimés de la bibliothèque de documents pendant la période spécifiée ( les cinq prochains mois, par exemple).</span><span class="sxs-lookup"><span data-stu-id="b5144-106">For example, you want your model to not only identify any *Insurance notice* documents that are uploaded to your document library, but to also apply a *Business* retention tag to them so that these documents cannot be deleted from the document library for the specified time period (the next five months, for example).</span></span>

<span data-ttu-id="b5144-107">Vous pouvez appliquer une étiquette de rétention préexistante à votre modèle de compréhension de document via les paramètres du modèle sur la page d’accueil de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="b5144-107">You can apply a pre-existing retention label to your document understanding model through your model settings on your model's home page.</span></span> 

> [!Important]
> <span data-ttu-id="b5144-108">Pour que les étiquettes de rétention soient disponibles et s’appliquent à votre modèle de compréhension de contenu, elles doivent être [créées et publiées dans le Centre de conformité Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/create-apply-retention-labels#how-to-create-and-publish-retention-labels).</span><span class="sxs-lookup"><span data-stu-id="b5144-108">For retention labels to be available to apply to your content understanding model, they need to be [created and published in the Microsoft 365 Compliance Center](https://docs.microsoft.com/microsoft-365/compliance/create-apply-retention-labels#how-to-create-and-publish-retention-labels).</span></span>

## <a name="to-add-a-retention-label-to-a-document-understanding-model"></a><span data-ttu-id="b5144-109">Pour ajouter une étiquette de rétention à un modèle de compréhension de document</span><span class="sxs-lookup"><span data-stu-id="b5144-109">To add a retention label to a document understanding model</span></span>

1. <span data-ttu-id="b5144-110">Sur la page d’accueil du modèle, sélectionnez **Paramètres du modèle**.</span><span class="sxs-lookup"><span data-stu-id="b5144-110">From the model home page, select **Model settings**.</span></span></br>
2. <span data-ttu-id="b5144-111">Dans **Paramètres du modèle**, dans la section **Sécurité et conformité**, sélectionnez le menu **Étiquette de rétention** pour afficher une liste des étiquettes de rétention que vous pouvez appliquer au modèle.</span><span class="sxs-lookup"><span data-stu-id="b5144-111">In **Model settings**, in the **Security and compliance** section, select the **Retention label** menu to see a list of retention labels that are available for your to apply to the model.</span></span></br>
 <span data-ttu-id="b5144-112">![Menu Étiquette de rétention](../media/content-understanding/retention-labels-menu.png)</span><span class="sxs-lookup"><span data-stu-id="b5144-112">![Retention label menu](../media/content-understanding/retention-labels-menu.png)</span></span></br> 
3. <span data-ttu-id="b5144-113">Sélectionnez l’étiquette de rétention que vous souhaitez appliquer au modèle, puis **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b5144-113">Select the retention label you want to apply to the model, and then select **Save**.</span></span></br>

<span data-ttu-id="b5144-114">Après avoir appliqué l’étiquette de rétention à votre modèle, vous pouvez l’appliquer à une :</span><span class="sxs-lookup"><span data-stu-id="b5144-114">After applying the retention label to your model, you are able to apply it to a:</span></span>
- <span data-ttu-id="b5144-115">nouvelle bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="b5144-115">New document library</span></span>
- <span data-ttu-id="b5144-116">bibliothèque de documents à laquelle le modèle est déjà appliqué</span><span class="sxs-lookup"><span data-stu-id="b5144-116">Document library to which the model is already applied</span></span>
 
## <a name="apply-the-retention-label-to-a-document-library-to-which-the-model-is-already-applied"></a><span data-ttu-id="b5144-117">Appliquer l’étiquette de rétention à une bibliothèque de documents à laquelle le modèle est déjà appliqué</span><span class="sxs-lookup"><span data-stu-id="b5144-117">Apply the retention label to a document library to which the model is already applied</span></span>

<span data-ttu-id="b5144-118">Si votre modèle de compréhension de document a déjà été appliqué à une bibliothèque de documents, vous pouvez effectuer les opérations suivantes pour synchroniser la mise à jour de votre étiquette de rétention afin de l’appliquer à la bibliothèque de documents :</span><span class="sxs-lookup"><span data-stu-id="b5144-118">If your document understanding model has already been applied to a document library, you can do the following to sync your retention label update to apply it to the document library:</span></span></br>

1. <span data-ttu-id="b5144-119">Sur la page d’accueil de votre modèle, dans la section **Bibliothèques avec ce modèle**, sélectionnez la bibliothèque de documents à laquelle vous souhaitez appliquer la mise à jour de l’étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="b5144-119">On your model home page, in the **Libraries with this model** section, select the document library to which you want to apply the retention label update.</span></span> </br> 
2. <span data-ttu-id="b5144-120">Sélectionnez **Synchroniser**.</span><span class="sxs-lookup"><span data-stu-id="b5144-120">Select **Sync**.</span></span> </br>
 <span data-ttu-id="b5144-121">![Modèle de synchronisation](../media/content-understanding/sync-model.png)</span><span class="sxs-lookup"><span data-stu-id="b5144-121">![Sync model](../media/content-understanding/sync-model.png)</span></span></br> 


<span data-ttu-id="b5144-122">Après avoir appliqué la mise à jour et l’avoir synchronisée avec votre modèle, vous pouvez vérifier si elle a été appliquée en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="b5144-122">After applying the update and syncing it to your model, you can confirm that it has been applied by doing the following:</span></span>

1. <span data-ttu-id="b5144-123">Dans le centre de contenu, dans la section **Bibliothèques avec ce modèle**, cliquez sur la bibliothèque à laquelle votre modèle mis à jour a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="b5144-123">In the content center, in the **Libraries with this model** section, click on the library to which your updated model was applied.</span></span> </br>
2. <span data-ttu-id="b5144-124">Dans l’affichage de votre bibliothèque de documents, sélectionnez l’icône Information pour vérifier les propriétés du modèle.</span><span class="sxs-lookup"><span data-stu-id="b5144-124">In your document library view, select the information icon to check the model properties.</span></span></br>  
3. <span data-ttu-id="b5144-125">Dans la liste **Modèles actifs**, sélectionnez votre modèle mis à jour.</span><span class="sxs-lookup"><span data-stu-id="b5144-125">In the **Active models** list, select your updated model.</span></span></br>
4. <span data-ttu-id="b5144-126">Dans la section **Étiquette de rétention**, vous verrez le nom de l’étiquette de rétention appliquée.</span><span class="sxs-lookup"><span data-stu-id="b5144-126">In the **Retention label** section you will see the name of the applied retention label.</span></span></br>


<span data-ttu-id="b5144-127">Sur la page d’affichage de votre modèle, dans votre bibliothèque de documents, une nouvelle colonne **Étiquette de rétention** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b5144-127">On your model's view page in your document library, a new **Retention label** column will display.</span></span>  <span data-ttu-id="b5144-128">Lorsque votre modèle classe les fichiers qu’il identifie comme appartenant à son type de contenu et les répertorie dans l’affichage de la bibliothèque, la colonne Étiquette de rétention affiche également le nom de l’étiquette de rétention qui lui a été appliquée via le modèle.</span><span class="sxs-lookup"><span data-stu-id="b5144-128">As your model classifies files it identifies as belonging to it's content type and lists them in the library view, the Retention label column will also display the name of the retention label that has been applied to it through the model.</span></span>


<span data-ttu-id="b5144-129">Par exemple, tous les documents d’*avis d’assurance* que votre modèle identifie auront également l’étiquette de rétention *Entreprise* qui leur sera appliquée, ce qui fait qu’ils ne pourront pas être supprimés de la bibliothèque de documents pendant cinq mois.</span><span class="sxs-lookup"><span data-stu-id="b5144-129">For example, all *Insurance notice* documents that your model identifies will also have the *Business* retention label applied to them, preventing them from being deleted from the document library for five months.</span></span> <span data-ttu-id="b5144-130">Si vous tentez de supprimer le fichier de la bibliothèque de documents, une erreur s’affiche indiquant que l’opération n’est pas autorisée en raison de l’étiquette de rétention appliquée.</span><span class="sxs-lookup"><span data-stu-id="b5144-130">If an attempt is made to delete the file from the document library, an error will display saying it is not allowed because of the applied retention label.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5144-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5144-131">See Also</span></span>
[<span data-ttu-id="b5144-132">Créer un classifieur</span><span class="sxs-lookup"><span data-stu-id="b5144-132">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="b5144-133">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="b5144-133">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="b5144-134">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="b5144-134">Document Understanding overview</span></span>](document-understanding-overview.md)


