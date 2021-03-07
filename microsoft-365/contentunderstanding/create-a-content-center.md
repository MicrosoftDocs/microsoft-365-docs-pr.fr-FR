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
ms.openlocfilehash: 3544bbef7cf2f898733c7aaad620487098a2dd24
ms.sourcegitcommit: babbba2b5bf69fd3facde2905ec024b753dcd1b3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "50515135"
---
# <a name="create-a-content-center-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="e678b-103">Créer un centre de contenu dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="e678b-103">Create a content center in Microsoft SharePoint Syntex</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CPSF]

</br>

<span data-ttu-id="e678b-104">Pour créer et gérer des modèles de présentation de documents, vous devez d’abord utiliser un centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="e678b-104">To create and manage document understanding models, you first need a content center.</span></span> <span data-ttu-id="e678b-105">Le centre de contenu est l’interface de création de modèles et contient également des informations sur les bibliothèques de documents auxquelles les modèles publiés ont été appliqués.</span><span class="sxs-lookup"><span data-stu-id="e678b-105">The content center is the model creation interface and also contains information about which document libraries published models have been applied to.</span></span></br>

   ![Sélectionner une bibliothèque de documents](../media/content-understanding/content-center-page.png)</br>

<span data-ttu-id="e678b-107">Vous créez un centre de contenu par défaut lors de [l’installation](set-up-content-understanding.md).</span><span class="sxs-lookup"><span data-stu-id="e678b-107">You create a default content center during [setup](set-up-content-understanding.md).</span></span> <span data-ttu-id="e678b-108">Mais un administrateur SharePoint peut également choisir de créer d’autres centres au besoin.</span><span class="sxs-lookup"><span data-stu-id="e678b-108">But a SharePoint admin can also choose to create additional centers as needed.</span></span> <span data-ttu-id="e678b-109">Bien qu’il soit possible qu’un seul centre de contenu soit adapté aux environnements pour lesquels vous voulez regrouper toutes les activités du modèle, vous souhaiterez peut-être disposer de centres supplémentaires pour plusieurs services au sein de votre organisation, lesquels peuvent avoir des besoins et des autorisations différents pour leurs modèles.</span><span class="sxs-lookup"><span data-stu-id="e678b-109">While a single content center may be fine for environments for which you want a roll-up of all model activity, you may want to have additional centers for multiple departments within your organization, which may have different needs and permission requirements for their models.</span></span>

> [!NOTE]
> <span data-ttu-id="e678b-110">Dans un [Microsoft 365 Multigéographie](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-multi-geo), si vous avez un centre de contenu par défaut unique dans votre emplacement central, vous pouvez seulement fournir un suivi de l’activité du modèle à partir de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="e678b-110">In a [Microsoft 365 Multi-Geo environment](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-multi-geo), if you have a single default content center in your central location, you can only provide a roll-up of model activity from within that location.</span></span> <span data-ttu-id="e678b-111">Vous ne pouvez pas actuellement obtenir de déploiement de l’activité de modèle au-delà des limites de la batterie de serveurs dans l’environnement multigéographique.</span><span class="sxs-lookup"><span data-stu-id="e678b-111">You currently cannot get a roll-up of model activity across farm-boundaries in Multi-Geo environment.</span></span> 


## <a name="create-a-content-center"></a><span data-ttu-id="e678b-112">Créer un centre de contenu</span><span class="sxs-lookup"><span data-stu-id="e678b-112">Create a content center</span></span>

<span data-ttu-id="e678b-113">Un administrateur SharePoint peut créer un site de centre de contenu comme ils peuvent [créer n’importe quel autre site SharePoint](https://docs.microsoft.com/sharepoint/create-site-collection) via le panneau de configuration du site Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="e678b-113">A SharePoint admin can create a content center site like they would [create any other SharePoint site](https://docs.microsoft.com/sharepoint/create-site-collection) through the admin center site provisioning panel.</span></span>

<span data-ttu-id="e678b-114">Pour créer un nouveau centre de contenu, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e678b-114">To create a new content center:</span></span>

1. <span data-ttu-id="e678b-115">Dans le centre d’administration Microsoft 365, accédez au centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e678b-115">On the Microsoft 365 admin center, go to the SharePoint admin center.</span></span>

2. <span data-ttu-id="e678b-116">Dans le Centre d’administration SharePoint, sous **Sites** sélectionnez **Sites actifs**.</span><span class="sxs-lookup"><span data-stu-id="e678b-116">On the SharePoint admin center, under **Sites**, select **Active Sites**.</span></span>

3. <span data-ttu-id="e678b-117">Dans la page **Sites actifs**, cliquez sur **Créer**, puis sélectionnez **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="e678b-117">On the **Active Sites** page, click **Create**, and then select **Other options**.</span></span>

4. <span data-ttu-id="e678b-118">Dans le menu **Choisir un modèle** , sélectionnez **Centre de contenu**.</span><span class="sxs-lookup"><span data-stu-id="e678b-118">On the **Choose a template** menu, select **Content Center**.</span></span>

5. <span data-ttu-id="e678b-119">Pour le nouveau site, fournissez un **Nom de site**, **Administrateur principal** et une **Langue**.</span><span class="sxs-lookup"><span data-stu-id="e678b-119">For the new site, provide a **Site Name**, **Primary administrator**, and a **Language**.</span></span></br>

   > [!NOTE] 
   > <span data-ttu-id="e678b-120">Vous pouvez sélectionner un site de centre de contenu à afficher dans l’une des langues disponibles, mais notez que les modèles actuellement peuvent uniquement être créés pour les fichiers en anglais.</span><span class="sxs-lookup"><span data-stu-id="e678b-120">You can select a content center site to render in any of the available languages, but note that currently models can only be created for English files.</span></span> <span data-ttu-id="e678b-121">Notez également que comme les autres modèles de site, la langue du site par défaut ne peut pas être modifiée une fois le site créé.</span><span class="sxs-lookup"><span data-stu-id="e678b-121">Also note that like other site templates, the default site language isn't editable after the site is created.</span></span></br>

6. <span data-ttu-id="e678b-122">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="e678b-122">Select **Finished**.</span></span>
 
<span data-ttu-id="e678b-123">Une fois que vous avez créé un site de centre de contenu, celui-ci est répertorié sur la page **Sites actifs** dans le centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e678b-123">After you create a content center site, you will see it listed on the **Active sites** page in the SharePoint admin center.</span></span> 

### <a name="give-access-to-additional-users"></a><span data-ttu-id="e678b-124">Accorder l’accès à d’autres utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e678b-124">Give access to additional users</span></span>
 
<span data-ttu-id="e678b-125">Une fois le site créé, vous pouvez autoriser d’autres utilisateurs à accéder au site via le [modèle d’autorisations de site SharePoint](https://docs.microsoft.com/sharepoint/modern-experience-sharing-permissions) standard.</span><span class="sxs-lookup"><span data-stu-id="e678b-125">After you create the site, you can give additional users access to the site through the standard [SharePoint site permissions model](https://docs.microsoft.com/sharepoint/modern-experience-sharing-permissions).</span></span>

## <a name="see-also"></a><span data-ttu-id="e678b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e678b-126">See Also</span></span>
[<span data-ttu-id="e678b-127">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="e678b-127">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="e678b-128">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="e678b-128">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="e678b-129">Créer un centre de contenu</span><span class="sxs-lookup"><span data-stu-id="e678b-129">Create a content center</span></span>](create-a-content-center.md)

[<span data-ttu-id="e678b-130">Présentation de la présentation des documents</span><span class="sxs-lookup"><span data-stu-id="e678b-130">Document understanding overview</span></span>](document-understanding-overview.md)

[<span data-ttu-id="e678b-131">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="e678b-131">Create a form processing model</span></span>](create-a-form-processing-model.md)

[<span data-ttu-id="e678b-132">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="e678b-132">Apply a model</span></span>](apply-a-model.md)    
