---
title: Créer un centre de contenu dans Microsoft SharePoint Syntex
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
description: Découvrez comment créer un centre de contenu.
ms.openlocfilehash: 4377cbfbda8572fe9e08a079a05146961105298b
ms.sourcegitcommit: 162c01dfaa2fdb3225ce4c24964c1065ce22ed5d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2021
ms.locfileid: "49976530"
---
# <a name="create-a-content-center-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="780b9-103">Créer un centre de contenu dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="780b9-103">Create a content center in Microsoft SharePoint Syntex</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CPSF]

</br>

<span data-ttu-id="780b9-104">Pour créer et gérer des modèles de présentation de documents, vous devez d’abord utiliser un centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="780b9-104">To create and manage document understanding models, you first need a content center.</span></span> <span data-ttu-id="780b9-105">Le centre de contenu est l’interface de création de modèles et contient également des informations sur les bibliothèques de documents auxquelles les modèles publiés ont été appliqués.</span><span class="sxs-lookup"><span data-stu-id="780b9-105">The content center is the model creation interface and also contains information about which document libraries published models have been applied to.</span></span></br>

   ![Sélectionner une bibliothèque de documents](../media/content-understanding/content-center-page.png)</br>

<span data-ttu-id="780b9-107">Vous créez un centre de contenu par défaut lors de [l’installation](set-up-content-understanding.md).</span><span class="sxs-lookup"><span data-stu-id="780b9-107">You create a default content center during [setup](set-up-content-understanding.md).</span></span> <span data-ttu-id="780b9-108">Mais un administrateur SharePoint peut également choisir de créer d’autres centres au besoin.</span><span class="sxs-lookup"><span data-stu-id="780b9-108">But a SharePoint admin can also choose to create additional centers as needed.</span></span> <span data-ttu-id="780b9-109">Bien qu’il soit possible qu’un seul centre de contenu soit adapté aux environnements pour lesquels vous voulez regrouper toutes les activités du modèle, vous souhaiterez peut-être disposer de centres supplémentaires pour plusieurs services au sein de votre organisation, lesquels peuvent avoir des besoins et des autorisations différents pour leurs modèles.</span><span class="sxs-lookup"><span data-stu-id="780b9-109">While a single content center may be fine for environments for which you want a roll-up of all model activity, you may want to have additional centers for multiple departments within your organization, which may have different needs and permission requirements for their models.</span></span>

> [!NOTE]
> <span data-ttu-id="780b9-110">Un administrateur SharePoint peut créer un site de centre de contenu comme ils peuvent [créer n’importe quel autre site SharePoint](https://docs.microsoft.com/sharepoint/create-site-collection) via le panneau de configuration du site Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="780b9-110">A SharePoint admin can create a content center site like they would [create any other SharePoint site](https://docs.microsoft.com/sharepoint/create-site-collection) through the admin center site provisioning panel.</span></span>

<span data-ttu-id="780b9-111">Pour créer un nouveau centre de contenu, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="780b9-111">To create a new content center:</span></span>

1. <span data-ttu-id="780b9-112">Dans le centre d’administration Microsoft 365, accédez au centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="780b9-112">On the Microsoft 365 admin center, go to the SharePoint admin center.</span></span>
2. <span data-ttu-id="780b9-113">Dans le Centre d’administration SharePoint, sous **Sites** sélectionnez **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="780b9-113">On the SharePoint admin center, under **Sites**, select **Active Sites**.</span></span>
3. <span data-ttu-id="780b9-114">Dans la page **Sites actifs**, cliquez sur **Créer**, puis sélectionnez **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="780b9-114">On the **Active Sites** page, click **Create**, and then select **Other options**.</span></span>
4. <span data-ttu-id="780b9-115">Dans le menu **Choisir un modèle** , sélectionnez **Centre de contenu**.</span><span class="sxs-lookup"><span data-stu-id="780b9-115">On the **Choose a template** menu, select **Content Center**.</span></span>
5. <span data-ttu-id="780b9-116">Pour le nouveau site, fournissez un **Nom de site**, **Administrateur principal** et une **Langue**.</span><span class="sxs-lookup"><span data-stu-id="780b9-116">For the new site, provide a **Site Name**, **Primary administrator**, and a **Language**.</span></span></br>

> [!NOTE] 
> <span data-ttu-id="780b9-117">Vous pouvez sélectionner un site de centre de contenu à afficher dans l’une des langues disponibles, mais notez que les modèles actuellement peuvent uniquement être créés pour les fichiers en anglais.</span><span class="sxs-lookup"><span data-stu-id="780b9-117">You can select a content center site to render in any of the available languages, but note that currently models can only be created for English files.</span></span> <span data-ttu-id="780b9-118">Notez également que comme les autres modèles de site, la langue du site par défaut ne peut pas être modifiée une fois le site créé.</span><span class="sxs-lookup"><span data-stu-id="780b9-118">Also note that like other site templates, the default site language isn't editable after the site is created.</span></span></br>

6. <span data-ttu-id="780b9-119">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="780b9-119">Select **Finished**.</span></span>
 
<span data-ttu-id="780b9-120">Une fois que vous avez créé un site de centre de contenu, celui-ci est répertorié sur la page **Sites actifs** dans le centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="780b9-120">After you create a content center site, you will see it listed on the **Active sites** page in the SharePoint admin center.</span></span> 

### <a name="give-access-to-additional-users"></a><span data-ttu-id="780b9-121">Accorder l’accès à d’autres utilisateurs</span><span class="sxs-lookup"><span data-stu-id="780b9-121">Give access to additional users</span></span>
 
<span data-ttu-id="780b9-122">Une fois le site créé, vous pouvez autoriser d’autres utilisateurs à accéder au site via le [modèle d’autorisations de site SharePoint](https://docs.microsoft.com/sharepoint/modern-experience-sharing-permissions) standard.</span><span class="sxs-lookup"><span data-stu-id="780b9-122">After you create the site, you can give additional users access to the site through the standard [SharePoint site permissions model](https://docs.microsoft.com/sharepoint/modern-experience-sharing-permissions).</span></span>

## <a name="see-also"></a><span data-ttu-id="780b9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="780b9-123">See Also</span></span>
[<span data-ttu-id="780b9-124">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="780b9-124">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="780b9-125">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="780b9-125">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="780b9-126">Créer un centre de contenu</span><span class="sxs-lookup"><span data-stu-id="780b9-126">Create a content center</span></span>](create-a-content-center.md)

[<span data-ttu-id="780b9-127">Présentation de la présentation des documents</span><span class="sxs-lookup"><span data-stu-id="780b9-127">Document understanding overview</span></span>](document-understanding-overview.md)

[<span data-ttu-id="780b9-128">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="780b9-128">Create a form processing model</span></span>](create-a-form-processing-model.md)

[<span data-ttu-id="780b9-129">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="780b9-129">Apply a model</span></span>](apply-a-model.md)    
