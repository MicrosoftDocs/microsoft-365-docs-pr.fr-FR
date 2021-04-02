---
title: Dupliquer un modèle dans Microsoft SharePoint Syntex
ms.author: chucked
author: chuckedmonson
manager: pamgreen
audience: admin
ms.reviewer: ssquires
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-syntex
localization_priority: Priority
description: Apprenez comment et pourquoi dupliquer un modèle dans Microsoft SharePoint Syntex.
ms.openlocfilehash: 501c33b5309ca4af264a361c80fb0409c08c92e3
ms.sourcegitcommit: 39609c4d8c432c8e7d7a31cb35c8020e5207385b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "51446036"
---
# <a name="duplicate-a-model-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="705d0-103">Dupliquer un modèle dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="705d0-103">Duplicate a model in Microsoft SharePoint Syntex</span></span>

<span data-ttu-id="705d0-104">La duplication d'un modèle de compréhension de document peut vous faire gagner du temps et vous épargner des efforts si vous devez créer un nouveau modèle et si vous savez qu'un modèle existant est très similaire à ce dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="705d0-104">Duplicating a document understanding model can save you time and effort if you need to create a new model, and know that an existing model is very similar to what you need.</span></span>

<span data-ttu-id="705d0-105">Par exemple, un modèle existant nommé « Contrats » classe les mêmes fichiers que ceux avec lesquels vous devez travailler.</span><span class="sxs-lookup"><span data-stu-id="705d0-105">For example, an existing model named “Contracts” classifies the same files you need to work with.</span></span> <span data-ttu-id="705d0-106">Votre nouveau modèle extraira certaines des données existantes, mais devra être mis à jour pour extraire des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="705d0-106">Your new model will extract some of the existing data, but will need to be updated to extract some additional data.</span></span> <span data-ttu-id="705d0-107">Au lieu de créer et de former un nouveau modèle à partir de zéro, vous pouvez utiliser la fonction de duplication de modèle pour faire une copie du modèle de contrats, qui copiera également tous les éléments de formation associés, tels que les fichiers d'exemple et les extracteurs d'entités.</span><span class="sxs-lookup"><span data-stu-id="705d0-107">Instead of creating and training a new model from scratch, you can use the duplicate model feature to make a copy of the Contracts model, which will also copy all associated training items, such as example files and entity extractors.</span></span>

<span data-ttu-id="705d0-108">Lorsque vous dupliquez le modèle, après l'avoir renommé (par exemple, en «Renouvellements de contrats»), vous pouvez ensuite le mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="705d0-108">When you duplicate the model, after you rename it (for example, to “Contract Renewals”), you can then make updates to it.</span></span> <span data-ttu-id="705d0-109">Par exemple, vous pouvez choisir de supprimer certains des champs extraits existants dont vous n'avez pas besoin, puis entraîner le modèle à en extraire un nouveau (par exemple, «Date de renouvellement»).</span><span class="sxs-lookup"><span data-stu-id="705d0-109">For example, you can choose to remove some of the existing extracted fields that you don’t need, and then train the model to extract a new one (for example, “Renewal date”).</span></span>

## <a name="duplicate-a-model"></a><span data-ttu-id="705d0-110">Dupliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="705d0-110">Duplicate a model</span></span>

<span data-ttu-id="705d0-111">Suivez ces étapes pour dupliquer un modèle de compréhension de document.</span><span class="sxs-lookup"><span data-stu-id="705d0-111">Follow these steps to duplicate a document understanding model.</span></span>

1. <span data-ttu-id="705d0-112">Dans le centre de contenu, sélectionnez **Modèles** pour afficher la liste de vos modèles.</span><span class="sxs-lookup"><span data-stu-id="705d0-112">From the content center, select **Models** to see your models list.</span></span>

2. <span data-ttu-id="705d0-113">Sur la page **Modèles**, sélectionnez le modèle que vous souhaitez dupliquer.</span><span class="sxs-lookup"><span data-stu-id="705d0-113">On the **Models** page, select the model you want to duplicate.</span></span>

3. <span data-ttu-id="705d0-114">En utilisant le ruban ou le bouton **Afficher les actions** (à côté du nom du modèle), sélectionnez **Dupliquer**.</span><span class="sxs-lookup"><span data-stu-id="705d0-114">By using either the ribbon or the **Show actions** button (next to the model name), select **Duplicate**.</span></span></br>

    ![Capture d'écran de la page Modèles montrant un modèle sélectionné avec les options de duplication en surbrillance.](../media/content-understanding/select-model-duplicate-both.png) </br>

4. <span data-ttu-id="705d0-116">Dans le panneau **Dupliquer le modèle** :</span><span class="sxs-lookup"><span data-stu-id="705d0-116">On the **Duplicate model** panel:</span></span>

   <span data-ttu-id="705d0-117">a.</span><span class="sxs-lookup"><span data-stu-id="705d0-117">a.</span></span> <span data-ttu-id="705d0-118">Sous **Nom** , saisissez le nouveau nom du modèle que vous souhaitez dupliquer.</span><span class="sxs-lookup"><span data-stu-id="705d0-118">Under **Name**, enter the new name of the model that you want to duplicate.</span></span></br>

    ![Capture d'écran montrant le panneau du modèle dupliqué.](../media/content-understanding/duplicate-model-panel.png) </br>

   <span data-ttu-id="705d0-120">b.</span><span class="sxs-lookup"><span data-stu-id="705d0-120">b.</span></span> <span data-ttu-id="705d0-121">Sous **Description**, ajoutez une description de votre nouveau modèle.</span><span class="sxs-lookup"><span data-stu-id="705d0-121">Under **Description**, add a description of your new model.</span></span>

   <span data-ttu-id="705d0-122">c.</span><span class="sxs-lookup"><span data-stu-id="705d0-122">c.</span></span> <span data-ttu-id="705d0-123">(Facultatif) Sous **Paramètres avancés** , sélectionnez si vous voulez associer un [type de contenu](/sharepoint/governance/content-type-and-workflow-planning#content-type-overview) existant .</span><span class="sxs-lookup"><span data-stu-id="705d0-123">(Optional) Under **Advanced settings**, select whether you want to associate an existing [content type](/sharepoint/governance/content-type-and-workflow-planning#content-type-overview).</span></span>

5. <span data-ttu-id="705d0-124">Sélectionnez **Dupliquer**.</span><span class="sxs-lookup"><span data-stu-id="705d0-124">Select **Duplicate**.</span></span>

## <a name="see-also"></a><span data-ttu-id="705d0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="705d0-125">See Also</span></span>
[<span data-ttu-id="705d0-126">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="705d0-126">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="705d0-127">Renommer un modèle</span><span class="sxs-lookup"><span data-stu-id="705d0-127">Rename a model</span></span>](rename-a-model.md)

[<span data-ttu-id="705d0-128">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="705d0-128">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="705d0-129">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="705d0-129">Document Understanding overview</span></span>](document-understanding-overview.md)

[<span data-ttu-id="705d0-130">Types d’explications</span><span class="sxs-lookup"><span data-stu-id="705d0-130">Explanation types</span></span>](explanation-types-overview.md)

[<span data-ttu-id="705d0-131">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="705d0-131">Apply a model</span></span>](apply-a-model.md) 

[<span data-ttu-id="705d0-132">Mode d’accessibilité Syntex de SharePoint</span><span class="sxs-lookup"><span data-stu-id="705d0-132">SharePoint Syntex Accessibility Mode</span></span>](accessibility-mode.md)