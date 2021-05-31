---
title: Appliquer une étiquette de confidentialité à un modèle dans Microsoft SharePoint Syntex
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: ssquires
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-syntex
localization_priority: Priority
description: Découvrez comment appliquer une étiquette de confidentialité à un modèle dans SharePoint Syntex.
ms.openlocfilehash: 799ab3fa0fcdc9af9d227428056d2cd7abeaf539
ms.sourcegitcommit: a05f61a291eb4595fa9313757a3815b7f217681d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2021
ms.locfileid: "52706700"
---
# <a name="apply-a-sensitivity-label-to-a-model-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="8d243-103">Appliquer une étiquette de confidentialité à un modèle dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="8d243-103">Apply a sensitivity label to a model in Microsoft SharePoint Syntex</span></span>

<span data-ttu-id="8d243-104">Vous pouvez facilement appliquer une [étiquette de confidentialité](../compliance/sensitivity-labels.md) à un modèle de compréhension de document dans Microsoft SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="8d243-104">You can easily apply a [sensitivity label](../compliance/sensitivity-labels.md) to document understanding models in Microsoft SharePoint Syntex.</span></span> <span data-ttu-id="8d243-105">Cette fonctionnalité n’est pas encore disponible pour les modèles de traitement de formulaire.</span><span class="sxs-lookup"><span data-stu-id="8d243-105">This feature isn't available yet for form processing models.</span></span>

<span data-ttu-id="8d243-106">Les étiquettes de confidentialité vous permettent d’appliquer des stratégies de chiffrement, de partage et d’accès conditionnel aux documents que vos modèles identifient.</span><span class="sxs-lookup"><span data-stu-id="8d243-106">Sensitivity labels let you apply encryption, sharing, and conditional access policies to the documents that your models identify.</span></span> <span data-ttu-id="8d243-107">Par exemple, vous souhaitez que votre modèle identifie non seulement les documents financiers qui contiennent des numéros de compte bancaire ou des numéros de carte de crédit chargés dans votre bibliothèque de documents, mais également qu’il leur applique une étiquette de confidentialité *Chiffrement* afin de restreindre l’accès à ce contenu et la façon dont il peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="8d243-107">For example, you want your model to not only identify any financial documents that contain bank account numbers or credit card numbers that are uploaded to your document library, but also to apply an *Encryption* sensitivity label to them to restrict who can access that content and how it can be used.</span></span>

<span data-ttu-id="8d243-108">Vous pouvez appliquer une étiquette de confidentialité préexistante à votre modèle via les paramètres du modèle sur la page d’accueil de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="8d243-108">You can apply a pre-existing sensitivity label to your model through your model settings on your model's home page.</span></span> <span data-ttu-id="8d243-109">L’étiquette doit déjà être publiée pour pouvoir être sélectionnée dans les paramètres du modèle.</span><span class="sxs-lookup"><span data-stu-id="8d243-109">The label must already be published to be available for selection from model settings.</span></span>

> [!Important]
> <span data-ttu-id="8d243-110">Pour que les étiquettes de niveau de confidentialité soient disponibles et s’appliquent à votre modèle de compréhension de document, elles doivent être [créées et publiées dans le Centre de conformité Microsoft 365](../business-video/create-sensitivity-labels.md).</span><span class="sxs-lookup"><span data-stu-id="8d243-110">For sensitivity labels to be available to apply to your document understanding models, they need to be [created and published in the Microsoft 365 Compliance Center](../business-video/create-sensitivity-labels.md).</span></span>

## <a name="add-a-sensitivity-label-to-a-document-understanding-model"></a><span data-ttu-id="8d243-111">Appliquer une étiquette de confidentialité à un modèle de compréhension de document</span><span class="sxs-lookup"><span data-stu-id="8d243-111">Add a sensitivity label to a document understanding model</span></span>

1. <span data-ttu-id="8d243-112">Sur la page d’accueil du modèle, sélectionnez **Paramètres du modèle**.</span><span class="sxs-lookup"><span data-stu-id="8d243-112">From the model home page, select **Model settings**.</span></span>

   ![Capture d’écran de la page Modèles avec l’option Paramètres du modèle mise en évidence.](../media/content-understanding/sensitivity-model-settings.png)

2. <span data-ttu-id="8d243-114">Dans le volet **Paramètres du modèle**, dans la section **Conformité**, sélectionnez le menu **Étiquette de confidentialité** pour afficher la liste des étiquettes de confidentialité que vous pouvez appliquer au modèle.</span><span class="sxs-lookup"><span data-stu-id="8d243-114">On **Model settings** pane, in the **Compliance** section, select the **Sensitivity label** menu to see a list of sensitivity labels that are available for you to apply to the model.</span></span>

   ![Capture d’écran du volet Paramètres du modèle montrant le menu d’étiquette de confidentialité.](../media/content-understanding/sensitivity-model-settings-pane.png) 

3. <span data-ttu-id="8d243-116">Sélectionnez l’étiquette de confidentialité que vous souhaitez appliquer au modèle, puis **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8d243-116">Select the sensitivity label you want to apply to the model, and then select **Save**.</span></span>

<span data-ttu-id="8d243-117">Après avoir appliqué l’étiquette de confidentialité à votre modèle, vous pouvez l’appliquer à une :</span><span class="sxs-lookup"><span data-stu-id="8d243-117">After you apply the sensitivity label to your model, you can apply it to a:</span></span>

- <span data-ttu-id="8d243-118">nouvelle bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="8d243-118">New document library</span></span>
- <span data-ttu-id="8d243-119">bibliothèque de documents à laquelle le modèle est déjà appliqué</span><span class="sxs-lookup"><span data-stu-id="8d243-119">Document library to which the model is already applied</span></span>
 
### <a name="apply-the-sensitivity-label-to-a-document-library-to-which-the-model-is-already-applied"></a><span data-ttu-id="8d243-120">Appliquer l’étiquette de confidentialité à une bibliothèque de documents à laquelle le modèle est déjà appliqué</span><span class="sxs-lookup"><span data-stu-id="8d243-120">Apply the sensitivity label to a document library to which the model is already applied</span></span>

<span data-ttu-id="8d243-121">Si votre modèle de compréhension de document a déjà été appliqué à une bibliothèque de documents, vous pouvez effectuer les opérations suivantes pour synchroniser la mise à jour de votre étiquette de confidentialité afin de l’appliquer à la bibliothèque de documents :</span><span class="sxs-lookup"><span data-stu-id="8d243-121">If your document understanding model has already been applied to a document library, you can do the following to sync your sensitivity label update to apply it to the document library:</span></span>

1. <span data-ttu-id="8d243-122">Sur la page d’accueil du modèle, dans la section **Bibliothèques avec ce modèle**, sélectionnez la bibliothèque de documents à laquelle vous souhaitez appliquer la mise à jour de l’étiquette de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="8d243-122">On the model home page, in the **Libraries with this model** section, select the document library to which you want to apply the sensitivity label update.</span></span>

2. <span data-ttu-id="8d243-123">Sélectionnez **Synchroniser**.</span><span class="sxs-lookup"><span data-stu-id="8d243-123">Select **Sync**.</span></span>

   ![Capture d’écran montrant les bibliothèques avec cette section de modèle avec La synchronisation mise en surbrillance.](../media/content-understanding/sensitivity-libraries-sync.png)

<span data-ttu-id="8d243-125">Après avoir appliqué la mise à jour et l'avoir synchronisée avec votre modèle, vous pouvez confirmer qu'elle a été appliquée en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="8d243-125">After you apply the update and sync it to your model, you can confirm that it has been applied by doing the following steps:</span></span>

1. <span data-ttu-id="8d243-126">Dans le centre de contenu, dans la section **Bibliothèques avec ce modèle**, sélectionnez la bibliothèque à laquelle votre modèle mis à jour a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="8d243-126">In the content center, in the **Libraries with this model** section, select the library to which your updated model was applied.</span></span> 

2. <span data-ttu-id="8d243-127">Dans l’affichage de votre bibliothèque de documents, sélectionnez l’icône Information pour vérifier les propriétés du modèle.</span><span class="sxs-lookup"><span data-stu-id="8d243-127">In your document library view, select the information icon to check the model properties.</span></span>

3. <span data-ttu-id="8d243-128">Dans la liste **Modèles actifs**, sélectionnez votre modèle mis à jour.</span><span class="sxs-lookup"><span data-stu-id="8d243-128">In the **Active models** list, select your updated model.</span></span>

4. <span data-ttu-id="8d243-129">Dans la section **Étiquette de confidentialité**, vous verrez le nom de l’étiquette de confidentialité appliquée.</span><span class="sxs-lookup"><span data-stu-id="8d243-129">In the **Sensitivity label** section, you'll see the name of the applied sensitivity label.</span></span>

<span data-ttu-id="8d243-130">Sur la page d’affichage de votre modèle, dans votre bibliothèque de documents, une nouvelle colonne **Étiquette de confidentialité** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8d243-130">On your model's view page in your document library, a new **Sensitivity label** column will display.</span></span> <span data-ttu-id="8d243-131">Lorsque votre modèle classe les fichiers qu’il identifie comme appartenant à son type de contenu et les répertorie dans l’affichage de la bibliothèque, la colonne **Éiquette de confidentialité** affiche également le nom de l’étiquette de confidentialité qui lui a été appliquée via le modèle.</span><span class="sxs-lookup"><span data-stu-id="8d243-131">As your model classifies files it identifies as belonging to its content type and lists them in the library view, the **Sensitivity label** column will also display the name of the sensitivity label that has been applied to it through the model.</span></span>

<span data-ttu-id="8d243-132">Par exemple, tous les documents financiers identifiés par votre modèle auront également l’étiquette de confidentialité *Chiffrement* appliquée, ce qui les empêchera d’être accessibles par des personnes non autorisées.</span><span class="sxs-lookup"><span data-stu-id="8d243-132">For example, all financial documents that your model identifies also will have the *Encryption* sensitivity label applied to them, preventing them from being accessed by unauthorized people.</span></span> <span data-ttu-id="8d243-133">Si une personne non autorisée tente d’accéder au fichier à partir de la bibliothèque de documents, une erreur s’affiche indiquant qu’il n’est pas autorisé en raison de l’étiquette de confidentialité appliquée.</span><span class="sxs-lookup"><span data-stu-id="8d243-133">If an attempt is made to access the file from the document library by an unauthorized person, an error will display saying it isn't allowed because of the applied sensitivity label.</span></span>

<!---
## Add a sensitivity label to a form processing model

> [!Important]
> For sensitivity labels to be available to apply to your form processing model, they need to be [created and published in the Microsoft 365 Compliance Center](../business-video/create-sensitivity-labels.md).

You can either apply a sensitivity label to a form processing model when you are creating a model, or apply it to an existing model.

### Add a sensitivity label when you create a form processing model

1. When you [create a new form processing model](create-a-form-processing-model.md), select **Advanced settings**.

2. In **Advanced settings**, in the **Sensitivity label** section, select the menu and then select the sensitivity label you want to apply to the model.

3.  After you've completed your remaining model settings, select **Create** to build your model.

### Add a sensitivity label to an existing form processing model

You can add a sensitivity label to an existing form processing model in different ways:

- Through the **Automate** menu in the document library
- Through the **Active model** settings in the document library 

#### Add a sensitivity label to an existing form processing model through the Automate menu

You can add a sensitivity label to an existing form processing model that you own through the **Automate** menu in the document library in which the model is applied.

1. In your document library to which the form processing model is applied, select the **Automate** menu, select **AI Builder**, and then select **View form processing model details**.

2. On the **Model details** pane, in the **Sensitivity label** section, select the sensitivity label you want to apply. Then select **Save**.

#### Add a sensitivity label to an existing form processing model in the active model settings

You can add a sensitivity label to an existing form processing model that you own through the **Active model** settings in the document library in which the model is applied.

1. In the SharePoint document library in which the model is applied, select the **View active models** icon, and then select **View active models**.

2. In **Active models**, select the form processing model to which you want to apply the sensitivity label.

3. On the **Model details** pane, in the **Sensitivity label** section, select the sensitivity label you want to apply. Then select **Save**.

   > [!NOTE]
   > You must be the model owner for the **Model settings** pane to be editable. 
--->

## <a name="see-also"></a><span data-ttu-id="8d243-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d243-134">See also</span></span>

[<span data-ttu-id="8d243-135">Appliquer une autre étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="8d243-135">Apply a retention label</span></span>](apply-a-retention-label-to-a-model.md)

[<span data-ttu-id="8d243-136">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="8d243-136">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="8d243-137">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="8d243-137">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="8d243-138">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="8d243-138">Document Understanding overview</span></span>](document-understanding-overview.md)