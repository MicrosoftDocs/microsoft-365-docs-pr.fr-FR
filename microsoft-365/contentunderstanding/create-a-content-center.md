---
title: Créer un centre de contenu (aperçu)
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.service: ''
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Découvrez comment créer un centre de contenu.
ms.openlocfilehash: 5332ffa195519aebd5ae8dd2c26d7d62fd9b3267
ms.sourcegitcommit: a3a5dc541b0c971608cc86ef480509c25a13ca60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "46612749"
---
# <a name="create-a-content-center-preview"></a><span data-ttu-id="6a751-103">Créer un centre de contenu (aperçu)</span><span class="sxs-lookup"><span data-stu-id="6a751-103">Create a content center (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="6a751-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="6a751-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="6a751-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="6a751-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span></br>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CPSF]

</br>

<span data-ttu-id="6a751-106">Pour créer et gérer les modèles de présentation des documents, vous avez d’abord besoin d’un centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="6a751-106">To create and manage document understanding models, you first need a content center.</span></span> <span data-ttu-id="6a751-107">Le centre de contenu est l’interface de création de modèles et contient également des informations sur les bibliothèques de documents qui ont été appliquées à des modèles publiés.</span><span class="sxs-lookup"><span data-stu-id="6a751-107">The content center is the model creation interface and also contains information about which document libraries published models have been applied.</span></span></br>

   ![Sélectionner une bibliothèque de documents](../media/content-understanding/content-center-page.png)</br>

<span data-ttu-id="6a751-109">Un centre de contenu initial est créé lors de l' [installation](set-up-content-understanding.md), mais un administrateur SharePoint peut choisir d’en créer d’autres en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="6a751-109">An initial content center is created during [setup](set-up-content-understanding.md), but a SharePoint admin can choose to create additional ones as needed.</span></span> <span data-ttu-id="6a751-110">Alors qu’un seul centre de contenu peut être parfait pour les environnements dans lesquels vous souhaitez voir un cumul de toutes les activités de modèle, vous souhaiterez peut-être ajouter des éléments supplémentaires si votre organisation dispose de plusieurs services qui peuvent avoir différents besoins et exigences pour leurs modèles.</span><span class="sxs-lookup"><span data-stu-id="6a751-110">While a single content center may be fine for environments in which you want to see a roll-up of all model activity, you may want to have additional ones if your have multiple departments within your organization that may have different needs and requirements for their models.</span></span>

<span data-ttu-id="6a751-111">Un administrateur SharePoint peut créer un site Centre de contenu, comme il [créerait n’importe quel autre site SharePoint](https://docs.microsoft.com/sharepoint/create-site-collection) , via un modèle de site.</span><span class="sxs-lookup"><span data-stu-id="6a751-111">A SharePoint admin can create a content center site like they would [create any other SharePoint site](https://docs.microsoft.com/sharepoint/create-site-collection) - through a site template.</span></span>

<span data-ttu-id="6a751-112">Pour créer un nouveau centre de contenu :</span><span class="sxs-lookup"><span data-stu-id="6a751-112">To create a new content center:</span></span>

1. <span data-ttu-id="6a751-113">Dans le centre d’administration Microsoft 365, accédez au centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6a751-113">On the Microsoft 365 admin center, go to the SharePoint admin center.</span></span>
2. <span data-ttu-id="6a751-114">Dans le centre d’administration SharePoint, sous **sites**, sélectionnez **sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="6a751-114">On the SharePoint admin center, under **Sites**, select **Active Sites**.</span></span>
3. <span data-ttu-id="6a751-115">Sur la page **sites actifs** , cliquez sur **créer**, puis sélectionnez **autres options**.</span><span class="sxs-lookup"><span data-stu-id="6a751-115">On the **Active Sites** page, click **Create**, and then select **Other options**.</span></span>
4. <span data-ttu-id="6a751-116">Dans le menu **choisir un modèle** , sélectionnez **Centre de contenu**.</span><span class="sxs-lookup"><span data-stu-id="6a751-116">On the **Choose a template** menu, select **Content Center**.</span></span>
5. <span data-ttu-id="6a751-117">Pour le nouveau site, fournissez un **nom de site**, un **administrateur principal**et une **langue**.</span><span class="sxs-lookup"><span data-stu-id="6a751-117">For the new site, provide a **Site Name**, **Primary administrator**, and a **Language**.</span></span></br>

> [!Note] 
> <span data-ttu-id="6a751-118">Vous pouvez sélectionner un site Centre de contenu à afficher dans n’importe quelle langue disponible, mais notez que les modèles ne peuvent être créés que pour des fichiers en anglais.</span><span class="sxs-lookup"><span data-stu-id="6a751-118">You can select a content center site to render in any of the available languages, but note that currently models can only be created for English files.</span></span></br>

6. <span data-ttu-id="6a751-119">Cliquez sur **terminé**.</span><span class="sxs-lookup"><span data-stu-id="6a751-119">Click **Finished**.</span></span>

### <a name="give-access-to-additional-users"></a><span data-ttu-id="6a751-120">Accorder l’accès à d’autres utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6a751-120">Give access to additional users</span></span>
 
<span data-ttu-id="6a751-121">Une fois le site créé, vous pouvez accorder à d’autres utilisateurs l’accès au site via le [modèle d’autorisations de site SharePoint](https://docs.microsoft.com/sharepoint/modern-experience-sharing-permissions)standard.</span><span class="sxs-lookup"><span data-stu-id="6a751-121">After the site is created, you can give additional users access to the site through the standard [SharePoint site permissions model](https://docs.microsoft.com/sharepoint/modern-experience-sharing-permissions).</span></span>





## <a name="see-also"></a><span data-ttu-id="6a751-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a751-122">See Also</span></span>
[<span data-ttu-id="6a751-123">Créer un classifieur</span><span class="sxs-lookup"><span data-stu-id="6a751-123">Create a classifier</span></span>](create-a-classifier.md)</br>
[<span data-ttu-id="6a751-124">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="6a751-124">Create an extractor</span></span>](create-an-extractor.md)</br>
<span data-ttu-id="6a751-125">[Créer un centre](create-a-content-center.md) 
 de contenu [Présentation](document-understanding-overview.md) de l’explication des documents</span><span class="sxs-lookup"><span data-stu-id="6a751-125">[Create a content center](create-a-content-center.md)
[Document understanding overview](document-understanding-overview.md)</span></span></br>
[<span data-ttu-id="6a751-126">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="6a751-126">Create a form processing model</span></span>](create-a-form-processing-model.md)</br>
[<span data-ttu-id="6a751-127">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="6a751-127">Apply a model</span></span>](apply-a-model.md)    




