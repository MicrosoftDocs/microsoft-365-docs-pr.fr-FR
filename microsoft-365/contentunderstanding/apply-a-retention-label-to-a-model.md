---
title: Appliquer une étiquette de rétention à un modèle
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
description: Cet article décrit l’application d’une étiquette de rétention à un modèle dans SharePoint Syntex
ms.openlocfilehash: 796130bfa967663b5696f49279154cfe9b16f703
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50925367"
---
# <a name="apply-a-retention-label-to-a-model-in-sharepoint-syntex"></a><span data-ttu-id="98381-103">Application d’une étiquette de rétention à un modèle dans SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="98381-103">Apply a retention label to a model in SharePoint Syntex</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4GydO]  

</br>


<span data-ttu-id="98381-104">Vous pouvez facilement appliquer une [étiquette de rétention](../compliance/retention.md) à un modèle dans Microsoft SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="98381-104">You can easily apply a [retention label](../compliance/retention.md) to a model in Microsoft SharePoint Syntex.</span></span> <span data-ttu-id="98381-105">Vous pouvez le faire pour la compréhension des documents et les modèles de traitement des formulaires.</span><span class="sxs-lookup"><span data-stu-id="98381-105">You can do this for both document understanding and form processing models.</span></span>

<span data-ttu-id="98381-106">Les étiquettes de rétention vous permettent d’appliquer des paramètres de rétention aux documents identifiés par vos modèles.</span><span class="sxs-lookup"><span data-stu-id="98381-106">Retention labels let you apply retention settings to the documents that your models identify.</span></span>  <span data-ttu-id="98381-107">Par exemple, vous souhaitez que votre modèle identifie tous les documents d’*avis d’assurance* qui sont téléchargés dans votre bibliothèque de documents, mais également qu’il leur applique une étiquette de rétention *Entreprise*, afin que ces documents ne puissent pas être supprimés de la bibliothèque de documents pendant la période spécifiée ( les cinq prochains mois, par exemple).</span><span class="sxs-lookup"><span data-stu-id="98381-107">For example, you want your model to not only identify any *Insurance notice* documents that are uploaded to your document library, but to also apply a *Business* retention tag to them so that these documents cannot be deleted from the document library for the specified time period (the next five months, for example).</span></span>

<span data-ttu-id="98381-108">Vous pouvez appliquer une étiquette de rétention préexistante à votre modèle via les paramètres du modèle sur la page d’accueil de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="98381-108">You can apply a pre-existing retention label to your model through your model settings on your model's home page.</span></span> 

> [!Important]
> <span data-ttu-id="98381-109">Pour que les étiquettes de rétention soient disponibles et s’appliquent à votre modèle de compréhension de document, elles doivent être [créées et publiées dans le Centre de conformité Microsoft 365](../compliance/create-apply-retention-labels.md#how-to-create-and-publish-retention-labels).</span><span class="sxs-lookup"><span data-stu-id="98381-109">For retention labels to be available to apply to your document understanding models, they need to be [created and published in the Microsoft 365 Compliance Center](../compliance/create-apply-retention-labels.md#how-to-create-and-publish-retention-labels).</span></span>

## <a name="to-add-a-retention-label-to-a-document-understanding-model"></a><span data-ttu-id="98381-110">Pour ajouter une étiquette de rétention à un modèle de compréhension de document</span><span class="sxs-lookup"><span data-stu-id="98381-110">To add a retention label to a document understanding model</span></span>

1. <span data-ttu-id="98381-111">Sur la page d’accueil du modèle, sélectionnez **Paramètres du modèle**.</span><span class="sxs-lookup"><span data-stu-id="98381-111">From the model home page, select **Model settings**.</span></span></br>
2. <span data-ttu-id="98381-112">Dans **Paramètres du modèle**, dans la section **Sécurité et conformité**, sélectionnez le menu **Étiquette de rétention** pour afficher une liste des étiquettes de rétention que vous pouvez appliquer au modèle.</span><span class="sxs-lookup"><span data-stu-id="98381-112">In **Model settings**, in the **Security and compliance** section, select the **Retention label** menu to see a list of retention labels that are available for your to apply to the model.</span></span></br>
 <span data-ttu-id="98381-113">![Menu Étiquette de rétention](../media/content-understanding/retention-labels-menu.png)</span><span class="sxs-lookup"><span data-stu-id="98381-113">![Retention label menu](../media/content-understanding/retention-labels-menu.png)</span></span></br> 
3. <span data-ttu-id="98381-114">Sélectionnez l’étiquette de rétention que vous souhaitez appliquer au modèle, puis **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="98381-114">Select the retention label you want to apply to the model, and then select **Save**.</span></span></br>

<span data-ttu-id="98381-115">Après avoir appliqué l’étiquette de rétention à votre modèle, vous pouvez l’appliquer à une :</span><span class="sxs-lookup"><span data-stu-id="98381-115">After applying the retention label to your model, you are able to apply it to a:</span></span>
- <span data-ttu-id="98381-116">nouvelle bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="98381-116">New document library</span></span>
- <span data-ttu-id="98381-117">bibliothèque de documents à laquelle le modèle est déjà appliqué</span><span class="sxs-lookup"><span data-stu-id="98381-117">Document library to which the model is already applied</span></span>
 
## <a name="apply-the-retention-label-to-a-document-library-to-which-the-model-is-already-applied"></a><span data-ttu-id="98381-118">Appliquer l’étiquette de rétention à une bibliothèque de documents à laquelle le modèle est déjà appliqué</span><span class="sxs-lookup"><span data-stu-id="98381-118">Apply the retention label to a document library to which the model is already applied</span></span>

<span data-ttu-id="98381-119">Si votre modèle de compréhension de document a déjà été appliqué à une bibliothèque de documents, vous pouvez effectuer les opérations suivantes pour synchroniser la mise à jour de votre étiquette de rétention afin de l’appliquer à la bibliothèque de documents :</span><span class="sxs-lookup"><span data-stu-id="98381-119">If your document understanding model has already been applied to a document library, you can do the following to sync your retention label update to apply it to the document library:</span></span></br>

1. <span data-ttu-id="98381-120">Sur la page d’accueil de votre modèle, dans la section **Bibliothèques avec ce modèle**, sélectionnez la bibliothèque de documents à laquelle vous souhaitez appliquer la mise à jour de l’étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="98381-120">On your model home page, in the **Libraries with this model** section, select the document library to which you want to apply the retention label update.</span></span> </br> 
2. <span data-ttu-id="98381-121">Sélectionnez **Synchroniser**.</span><span class="sxs-lookup"><span data-stu-id="98381-121">Select **Sync**.</span></span> </br>
 <span data-ttu-id="98381-122">![Modèle de synchronisation](../media/content-understanding/sync-model.png)</span><span class="sxs-lookup"><span data-stu-id="98381-122">![Sync model](../media/content-understanding/sync-model.png)</span></span></br> 


<span data-ttu-id="98381-123">Après avoir appliqué la mise à jour et l’avoir synchronisée avec votre modèle, vous pouvez vérifier si elle a été appliquée en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="98381-123">After applying the update and syncing it to your model, you can confirm that it has been applied by doing the following:</span></span>

1. <span data-ttu-id="98381-124">Dans le centre de contenu, dans la section **Bibliothèques avec ce modèle**, cliquez sur la bibliothèque à laquelle votre modèle mis à jour a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="98381-124">In the content center, in the **Libraries with this model** section, click on the library to which your updated model was applied.</span></span> </br>
2. <span data-ttu-id="98381-125">Dans l’affichage de votre bibliothèque de documents, sélectionnez l’icône Information pour vérifier les propriétés du modèle.</span><span class="sxs-lookup"><span data-stu-id="98381-125">In your document library view, select the information icon to check the model properties.</span></span></br>  
3. <span data-ttu-id="98381-126">Dans la liste **Modèles actifs**, sélectionnez votre modèle mis à jour.</span><span class="sxs-lookup"><span data-stu-id="98381-126">In the **Active models** list, select your updated model.</span></span></br>
4. <span data-ttu-id="98381-127">Dans la section **Étiquette de rétention**, vous verrez le nom de l’étiquette de rétention appliquée.</span><span class="sxs-lookup"><span data-stu-id="98381-127">In the **Retention label** section you will see the name of the applied retention label.</span></span></br>


<span data-ttu-id="98381-128">Sur la page d’affichage de votre modèle, dans votre bibliothèque de documents, une nouvelle colonne **Étiquette de rétention** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="98381-128">On your model's view page in your document library, a new **Retention label** column will display.</span></span>  <span data-ttu-id="98381-129">Lorsque votre modèle classe les fichiers qu’il identifie comme appartenant à son type de contenu et les répertorie dans l’affichage de la bibliothèque, la colonne Étiquette de rétention affiche également le nom de l’étiquette de rétention qui lui a été appliquée via le modèle.</span><span class="sxs-lookup"><span data-stu-id="98381-129">As your model classifies files it identifies as belonging to it's content type and lists them in the library view, the Retention label column will also display the name of the retention label that has been applied to it through the model.</span></span>


<span data-ttu-id="98381-130">Par exemple, tous les documents d’*avis d’assurance* que votre modèle identifie auront également l’étiquette de rétention *Entreprise* qui leur sera appliquée, ce qui fait qu’ils ne pourront pas être supprimés de la bibliothèque de documents pendant cinq mois.</span><span class="sxs-lookup"><span data-stu-id="98381-130">For example, all *Insurance notice* documents that your model identifies will also have the *Business* retention label applied to them, preventing them from being deleted from the document library for five months.</span></span> <span data-ttu-id="98381-131">Si vous tentez de supprimer le fichier de la bibliothèque de documents, une erreur s’affiche indiquant que l’opération n’est pas autorisée en raison de l’étiquette de rétention appliquée.</span><span class="sxs-lookup"><span data-stu-id="98381-131">If an attempt is made to delete the file from the document library, an error will display saying it is not allowed because of the applied retention label.</span></span>

## <a name="to-add-a-retention-label-to-a-form-processing-model"></a><span data-ttu-id="98381-132">Pour ajouter une étiquette de rétention à un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="98381-132">To add a retention label to a form processing model</span></span>

> [!Important]
> <span data-ttu-id="98381-133">Pour que les étiquettes de rétention soient disponibles et s’appliquent à votre modèle de traitement des formulaires, elles doivent être [créées et publiées dans le Centre de conformité Microsoft 365](../compliance/create-apply-retention-labels.md#how-to-create-and-publish-retention-labels).</span><span class="sxs-lookup"><span data-stu-id="98381-133">For retention labels to be available to apply to your form processing model, they need to be [created and published in the Microsoft 365 Compliance Center](../compliance/create-apply-retention-labels.md#how-to-create-and-publish-retention-labels).</span></span>

<span data-ttu-id="98381-134">Vous pouvez appliquer une étiquette de rétention à un modèle de traitement de formulaires lorsque vous créez un modèle ou l’appliquer à un modèle existant.</span><span class="sxs-lookup"><span data-stu-id="98381-134">You can either apply a retention label to a form processing model when you are creating a model, or apply it to an existing model.</span></span>

### <a name="to-add-a-retention-label-when-you-create-a-form-processing-model"></a><span data-ttu-id="98381-135">Pour ajouter une étiquette de rétention lorsque vous créez un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="98381-135">To add a retention label when you create a form processing model</span></span>

1. <span data-ttu-id="98381-136">Lorsque vous [créez un modèle de traitement de formulaires,](./create-a-form-processing-model.md)sélectionnez <b>Paramètres avancés.</b></span><span class="sxs-lookup"><span data-stu-id="98381-136">When you are [creating a new form processing model](./create-a-form-processing-model.md), select <b>Advanced settings.</b></span></span>
2. <span data-ttu-id="98381-137">Dans <b>Paramètres avancés</b>, dans la section <b>Étiquette de rétention</b>, sélectionnez le menu, puis l’étiquette de rétention que vous voulez appliquer au modèle.</b></span><span class="sxs-lookup"><span data-stu-id="98381-137">In <b>Advanced settings</b>, in the <b>Retention label</b> section, select the menu and then select the retention label you want to apply to the model.</b></span></span>

 
     ![Ajouter à un nouveau modèle de traitement de formulaire](../media/content-understanding/retention-label-forms.png)</br>

3.  <span data-ttu-id="98381-139">Une fois que vous avez terminé vos paramètres de modèle restants, sélectionnez <b>Créer</b> pour créer votre modèle.</span><span class="sxs-lookup"><span data-stu-id="98381-139">After you've completed your remaining model settings, select <b>Create</b> to build your model.</span></span>

### <a name="to-add-a-retention-label-to-an-existing-form-processing-model"></a><span data-ttu-id="98381-140">Pour ajouter une étiquette de rétention à un modèle de traitement de formulaire existant</span><span class="sxs-lookup"><span data-stu-id="98381-140">To add a retention label to an existing form processing model</span></span>

<span data-ttu-id="98381-141">Vous pouvez ajouter une étiquette de rétention à un modèle de traitement de formulaire existant de différentes manières :</span><span class="sxs-lookup"><span data-stu-id="98381-141">You can add a retention label to an existing form processing model in different ways:</span></span>
- <span data-ttu-id="98381-142">Via le menu Automatiser de la bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="98381-142">Through the Automate menu in the document library</span></span>
- <span data-ttu-id="98381-143">Via les paramètres de modèle actif dans la bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="98381-143">Through the Active model settings in the document library</span></span> 


#### <a name="to-add-a-retention-label-to-an-existing-form-processing-model-through-the-automate-menu"></a><span data-ttu-id="98381-144">Pour ajouter une étiquette de rétention à un modèle de traitement de formulaire existant via le menu Automatiser</span><span class="sxs-lookup"><span data-stu-id="98381-144">To add a retention label to an existing form processing model through the Automate menu</span></span>

<span data-ttu-id="98381-145">Vous pouvez ajouter une étiquette de rétention à un modèle de traitement de formulaires que vous possédez via le menu Automatiser de la bibliothèque de documents dans laquelle le modèle est appliqué.</span><span class="sxs-lookup"><span data-stu-id="98381-145">You can add a retention label to an existing form processing model that you own through the Automate menu in the document library in which the model is applied.</span></span>


1. <span data-ttu-id="98381-146">Dans la bibliothèque de documents à laquelle le modèle de traitement de formulaire est appliqué, sélectionnez le menu <b>Automatiser</b>, sélectionnez <b>Générateur IA</b>, puis sélectionnez <b>Afficher les détails du modèle de traitement de formulaire</b>.</span><span class="sxs-lookup"><span data-stu-id="98381-146">In your document library to which the form processing model is applied, select the <b>Automate</b> menu, select <b>AI Builder</b>, then select <b>View form processing model details</b>.</span></span>

   ![Menu Automatiser](../media/content-understanding/automate-menu.png)</br>

2. <span data-ttu-id="98381-148">Dans les détails du modèle, dans la section <b>Étiquette de rétention</b> , sélectionnez l’étiquette de rétention que vous voulez appliquer.</span><span class="sxs-lookup"><span data-stu-id="98381-148">In the model details, in the <b>Retention Label</b> section, select the retention label you want to apply.</span></span>  <span data-ttu-id="98381-149">Sélectionnez <b>Enregistrer</b>.</span><span class="sxs-lookup"><span data-stu-id="98381-149">Then select <b>Save</b>.</span></span>

     ![Ajouter à un modèle de traitement de formulaire existant](../media/content-understanding/retention-label-model-details.png)</br> 

#### <a name="to-add-a-retention-label-to-an-existing-form-processing-model-in-the-active-model-settings"></a><span data-ttu-id="98381-151">Pour ajouter une étiquette de rétention à un modèle de traitement de formulaire existant dans les paramètres du modèle actif</span><span class="sxs-lookup"><span data-stu-id="98381-151">To add a retention label to an existing form processing model in the active model settings</span></span>

<span data-ttu-id="98381-152">Vous pouvez ajouter une étiquette de rétention à un modèle de traitement de formulaires que vous possédez via les paramètres du modèle actif de la bibliothèque de documents dans laquelle le modèle est appliqué.</span><span class="sxs-lookup"><span data-stu-id="98381-152">You can add a retention label to an existing form processing model that you own through the Active model settings in the document library in which the model is applied.</span></span>

1. <span data-ttu-id="98381-153">Dans la bibliothèque de documents SharePoint dans laquelle le modèle est appliqué, sélectionnez l’icône <b>Afficher les modèles actifs</b>, puis sélectionnez <b>Afficher les modèles actifs</b>.</b></span><span class="sxs-lookup"><span data-stu-id="98381-153">In the SharePoint document library in which the model is applied, select the <b>View active models</b> icon, and then select <b>View active models</b>.</b></span></span>

   ![Afficher les modèles actifs](../media/content-understanding/info-du.png)</br> 

2. <span data-ttu-id="98381-155">Dans <b>Modèles actifs</b>, sélectionnez le modèle de traitement de formulaire auquel vous voulez appliquer l’étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="98381-155">In <b>Active models</b>, select the form processing model to which you want to apply the retention label.</span></span>

     ![Détails du modèle](../media/content-understanding/retention-label-model-details.png)</br> 


3. <span data-ttu-id="98381-157">Dans les détails du modèle, dans la section <b>Étiquette de rétention</b> , sélectionnez l’étiquette de rétention que vous voulez appliquer.</span><span class="sxs-lookup"><span data-stu-id="98381-157">In the model details, in the <b>Retention Label</b> section, select the retention label you want to apply.</span></span>  <span data-ttu-id="98381-158">Sélectionnez <b>Enregistrer</b>.</span><span class="sxs-lookup"><span data-stu-id="98381-158">Then select <b>Save</b>.</span></span>

> [!NOTE]
> <span data-ttu-id="98381-159">Vous devez être le propriétaire du modèle pour que le volet des paramètres du modèle soit modifiable.</span><span class="sxs-lookup"><span data-stu-id="98381-159">You must be the model owner for the model settings pane to be editable.</span></span> 


## <a name="see-also"></a><span data-ttu-id="98381-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98381-160">See Also</span></span>
[<span data-ttu-id="98381-161">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="98381-161">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="98381-162">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="98381-162">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="98381-163">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="98381-163">Document Understanding overview</span></span>](document-understanding-overview.md)