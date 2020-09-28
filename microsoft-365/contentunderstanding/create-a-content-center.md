---
title: Créer un centre de contenu dans Microsoft SharePoint Syntex
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Découvrez comment créer un centre de contenu.
ms.openlocfilehash: 62977bc5a34b041e9e958ff46e0dbc010d6bd822
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48295431"
---
# <a name="create-a-content-center-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="dd245-103">Créer un centre de contenu dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="dd245-103">Create a content center in Microsoft SharePoint Syntex</span></span>

<span data-ttu-id="dd245-104">Le contenu de cet article est destiné à la préversion privée du projet cortex.</span><span class="sxs-lookup"><span data-stu-id="dd245-104">The content in this article is for the Project Cortex Private Preview.</span></span> <span data-ttu-id="dd245-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="dd245-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span></br>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CPSF]

</br>

<span data-ttu-id="dd245-106">Pour créer et gérer les modèles de présentation des documents, vous avez d’abord besoin d’un centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="dd245-106">To create and manage document understanding models, you first need a content center.</span></span> <span data-ttu-id="dd245-107">Le centre de contenu est l’interface de création de modèles et contient également des informations sur les bibliothèques de documents auxquelles des modèles publiés ont été appliqués.</span><span class="sxs-lookup"><span data-stu-id="dd245-107">The content center is the model creation interface and also contains information about which document libraries published models have been applied to.</span></span></br>

   ![Sélectionner une bibliothèque de documents](../media/content-understanding/content-center-page.png)</br>

<span data-ttu-id="dd245-109">Vous créez un centre de contenu initial lors de l' [installation](set-up-content-understanding.md).</span><span class="sxs-lookup"><span data-stu-id="dd245-109">You create an initial content center during [setup](set-up-content-understanding.md).</span></span> <span data-ttu-id="dd245-110">Toutefois, un administrateur SharePoint peut également choisir de créer des centres supplémentaires en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="dd245-110">But a SharePoint admin can also choose to create additional centers as needed.</span></span> <span data-ttu-id="dd245-111">Bien qu’un seul centre de contenu puisse être parfait pour les environnements pour lesquels vous souhaitez un cumul de toutes les activités des modèles, vous pouvez souhaiter avoir des centres supplémentaires pour plusieurs services au sein de votre organisation, qui peuvent avoir des besoins et des exigences différents pour leurs modèles.</span><span class="sxs-lookup"><span data-stu-id="dd245-111">While a single content center may be fine for environments for which you want a roll-up of all model activity, you may want to have additional centers for multiple departments within your organization, which may have different needs and requirements for their models.</span></span>

> [!NOTE]
> <span data-ttu-id="dd245-112">Un administrateur SharePoint peut créer un site Centre de contenu, comme il [créerait n’importe quel autre site SharePoint](https://docs.microsoft.com/sharepoint/create-site-collection) à l’aide d’un modèle de site.</span><span class="sxs-lookup"><span data-stu-id="dd245-112">A SharePoint admin can create a content center site like they would [create any other SharePoint site](https://docs.microsoft.com/sharepoint/create-site-collection) by using a site template.</span></span>

<span data-ttu-id="dd245-113">Pour créer un nouveau centre de contenu :</span><span class="sxs-lookup"><span data-stu-id="dd245-113">To create a new content center:</span></span>

1. <span data-ttu-id="dd245-114">Dans le centre d’administration Microsoft 365, accédez au centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="dd245-114">From the Microsoft 365 admin center, go to the SharePoint admin center.</span></span>
2. <span data-ttu-id="dd245-115">Dans le centre d’administration SharePoint, sous **sites**, sélectionnez **sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="dd245-115">In the SharePoint admin center, under **Sites**, select **Active Sites**.</span></span>
3. <span data-ttu-id="dd245-116">Sur la page **sites actifs** , cliquez sur **créer**, puis sélectionnez **autres options**.</span><span class="sxs-lookup"><span data-stu-id="dd245-116">On the **Active Sites** page, click **Create**, and then select **Other options**.</span></span>
4. <span data-ttu-id="dd245-117">Dans le menu **choisir un modèle** , sélectionnez **Centre de contenu**.</span><span class="sxs-lookup"><span data-stu-id="dd245-117">On the **Choose a template** menu, select **Content Center**.</span></span>
5. <span data-ttu-id="dd245-118">Pour le nouveau site, fournissez un **nom de site**, un **administrateur principal**et une **langue**.</span><span class="sxs-lookup"><span data-stu-id="dd245-118">For the new site, provide a **Site Name**, **Primary administrator**, and a **Language**.</span></span></br>

> [!NOTE] 
> <span data-ttu-id="dd245-119">Vous pouvez éventuellement sélectionner un site Centre de contenu à afficher dans l’une des langues disponibles.</span><span class="sxs-lookup"><span data-stu-id="dd245-119">You can optionally select a content center site to render in any of the available languages.</span></span> <span data-ttu-id="dd245-120">Seuls les modèles actuels peuvent être créés pour les fichiers en anglais.</span><span class="sxs-lookup"><span data-stu-id="dd245-120">Only current models can be created for English files.</span></span></br>

6. <span data-ttu-id="dd245-121">Sélectionnez **terminé**.</span><span class="sxs-lookup"><span data-stu-id="dd245-121">Select **Finished**.</span></span>

### <a name="give-access-to-additional-users"></a><span data-ttu-id="dd245-122">Accorder l’accès à d’autres utilisateurs</span><span class="sxs-lookup"><span data-stu-id="dd245-122">Give access to additional users</span></span>
 
<span data-ttu-id="dd245-123">Après avoir créé le site, vous pouvez accorder à d’autres utilisateurs l’accès au site via le [modèle d’autorisations de site SharePoint](https://docs.microsoft.com/sharepoint/modern-experience-sharing-permissions)standard.</span><span class="sxs-lookup"><span data-stu-id="dd245-123">After you create the site, you can give additional users access to the site through the standard [SharePoint site permissions model](https://docs.microsoft.com/sharepoint/modern-experience-sharing-permissions).</span></span>

## <a name="see-also"></a><span data-ttu-id="dd245-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd245-124">See Also</span></span>
[<span data-ttu-id="dd245-125">Créer un classifieur</span><span class="sxs-lookup"><span data-stu-id="dd245-125">Create a classifier</span></span>](create-a-classifier.md)</br>
[<span data-ttu-id="dd245-126">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="dd245-126">Create an extractor</span></span>](create-an-extractor.md)</br>
<span data-ttu-id="dd245-127">[Créer un centre](create-a-content-center.md) 
 de contenu [Présentation](document-understanding-overview.md) de l’explication des documents</span><span class="sxs-lookup"><span data-stu-id="dd245-127">[Create a content center](create-a-content-center.md)
[Document understanding overview](document-understanding-overview.md)</span></span></br>
[<span data-ttu-id="dd245-128">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="dd245-128">Create a form processing model</span></span>](create-a-form-processing-model.md)</br>
[<span data-ttu-id="dd245-129">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="dd245-129">Apply a model</span></span>](apply-a-model.md)    
