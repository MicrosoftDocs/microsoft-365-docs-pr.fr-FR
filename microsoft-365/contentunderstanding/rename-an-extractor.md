---
title: Renommer un extracteur dans Microsoft SharePoint Syntex
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
description: Apprenez comment et pourquoi renommer un extracteur dans Microsoft SharePoint Syntex.
ms.openlocfilehash: 4c0db1d0523e30706a2e6ec31286e5e91adb61a6
ms.sourcegitcommit: 39609c4d8c432c8e7d7a31cb35c8020e5207385b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "51445956"
---
# <a name="rename-an-extractor-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="f2554-103">Renommer un extracteur dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="f2554-103">Rename an extractor in Microsoft SharePoint Syntex</span></span>

<span data-ttu-id="f2554-104">À un moment donné, vous devrez peut-être renommer un extracteur si vous souhaitez faire référence à un champ de données extrait par un nom différent.</span><span class="sxs-lookup"><span data-stu-id="f2554-104">At some point, you might need to rename an extractor if you want to refer to an extracted data field by a different name.</span></span> <span data-ttu-id="f2554-105">Par exemple, votre organisation décide d'apporter des modifications à ses documents contractuels et désigne les «clients» par le terme «clients» dans ses documents.</span><span class="sxs-lookup"><span data-stu-id="f2554-105">For example, your organization decides to make changes to their contract documents, and refers to “customers” as “clients” in their documents.</span></span> <span data-ttu-id="f2554-106">Si vous extrayez un champ «Client» dans votre modèle, vous pouvez choisir de le renommer en «Client».</span><span class="sxs-lookup"><span data-stu-id="f2554-106">If you were extracting a “Customer” field in your model, you can choose to rename it to “Client.”</span></span>

<span data-ttu-id="f2554-107">Lorsque vous synchronisez votre modèle mis à jour avec votre bibliothèque de documents SharePoint, vous verrez une nouvelle colonne «Client» dans la vue de votre bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="f2554-107">When you sync your updated model to your SharePoint document library, you will see a new “Client” column in your document library view.</span></span> <span data-ttu-id="f2554-108">Votre vue conservera la colonne «Client» pour les activités passées, mais mettra à jour la nouvelle colonne «Client» pour tous les nouveaux documents traités par votre modèle.</span><span class="sxs-lookup"><span data-stu-id="f2554-108">Your view will retain the “Customer” column for past activity, but will update the new “Client” column for all new documents that are processed by your model.</span></span> 

> [!IMPORTANT]
>  <span data-ttu-id="f2554-109">Assurez-vous de synchroniser votre modèle mis à jour avec les bibliothèques de documents où vous l'aviez précédemment appliqué pour que le nouveau nom de colonne s'affiche.</span><span class="sxs-lookup"><span data-stu-id="f2554-109">Make sure to sync your updated model to the document libraries where you had previously applied it for the new column name to display.</span></span> 

## <a name="rename-an-extractor"></a><span data-ttu-id="f2554-110">Renommer un extracteur</span><span class="sxs-lookup"><span data-stu-id="f2554-110">Rename an extractor</span></span>

<span data-ttu-id="f2554-111">Suivez ces étapes pour renommer un extracteur d'entité.</span><span class="sxs-lookup"><span data-stu-id="f2554-111">Follow these steps to rename an entity extractor.</span></span>

1. <span data-ttu-id="f2554-112">Dans le centre de contenu, sélectionnez **Modèles** pour afficher votre liste de modèles.</span><span class="sxs-lookup"><span data-stu-id="f2554-112">From the content center, select **Models** to see your models list.</span></span>

2. <span data-ttu-id="f2554-113">Sur la page **Modèles**, dans la colonne **Nom**, sélectionnez le modèle pour lequel vous souhaitez renommer un extracteur.</span><span class="sxs-lookup"><span data-stu-id="f2554-113">On the **Models** page, in the **Name** column, select the model for which you want to rename an extractor.</span></span>

3. <span data-ttu-id="f2554-114">Sous **'entité**, sélectionnez le nom de l’extracteur que vous voulez renommer, puis sélectionnez **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="f2554-114">Under **Entity extractors**, select the name of the extractor you want to rename, and then select **Rename**.</span></span></br>

    ![Capture d'écran de la section Extracteurs d'entités montrant un extracteur sélectionné avec l'option Renommer en surbrillance.](../media/content-understanding/entity-extractor-rename.png) </br>

4. <span data-ttu-id="f2554-116">Sur **le panneau de l'extracteur** d'entité Renommer :</span><span class="sxs-lookup"><span data-stu-id="f2554-116">On the **Rename entity extractor** panel:</span></span>

   <span data-ttu-id="f2554-117">a.</span><span class="sxs-lookup"><span data-stu-id="f2554-117">a.</span></span> <span data-ttu-id="f2554-118">Sous **Nouveau nom**, saisissez le nouveau nom de l'extracteur.</span><span class="sxs-lookup"><span data-stu-id="f2554-118">Under **New name**, enter the new name of the extractor.</span></span></br>

    ![Capture d'écran montrant le panneau de l'extracteur d'entités.](../media/content-understanding/rename-entity-extractor-panel.png) </br>

   <span data-ttu-id="f2554-120">b.</span><span class="sxs-lookup"><span data-stu-id="f2554-120">b.</span></span> <span data-ttu-id="f2554-121">(Facultatif) Sous **Paramètres avancés**, sélectionnez si vous voulez associer une colonne de site existante.</span><span class="sxs-lookup"><span data-stu-id="f2554-121">(Optional) Under **Advanced settings**, select whether you want to associate an existing site column.</span></span>

5. <span data-ttu-id="f2554-122">Sélectionnez **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="f2554-122">Select **Rename**.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2554-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2554-123">See Also</span></span>
[<span data-ttu-id="f2554-124">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="f2554-124">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="f2554-125">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="f2554-125">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="f2554-126">Renommer un modèle</span><span class="sxs-lookup"><span data-stu-id="f2554-126">Rename a model</span></span>](rename-a-model.md)

[<span data-ttu-id="f2554-127">Types d’explications</span><span class="sxs-lookup"><span data-stu-id="f2554-127">Explanation types</span></span>](explanation-types-overview.md)

[<span data-ttu-id="f2554-128">Utiliser la taxonomie du magasin de termes lors de la création d’un extracteur</span><span class="sxs-lookup"><span data-stu-id="f2554-128">Leverage term store taxonomy when creating an extractor</span></span>](leverage-term-store-taxonomy.md)

[<span data-ttu-id="f2554-129">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="f2554-129">Document Understanding overview</span></span>](document-understanding-overview.md)

[<span data-ttu-id="f2554-130">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="f2554-130">Apply a model</span></span>](apply-a-model.md) 
