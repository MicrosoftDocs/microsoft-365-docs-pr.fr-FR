---
title: Créer un site de communication
f1.keywords:
- NOCSH
ms.author: samanro
author: samanro
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-identity-device-management
- M365-Campaigns
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
description: Créez un site de communication pour votre campagne.
ms.openlocfilehash: 3435ede554c16bb787b87a6ea76e0c41f62b8fe5
ms.sourcegitcommit: 46644f9778bc70ab6d62783e0a1e60ba2eccc27f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2020
ms.locfileid: "44165720"
---
# <a name="create-a-communications-site-for-your-campaign"></a><span data-ttu-id="33e87-103">Créer un site de communication pour votre campagne</span><span class="sxs-lookup"><span data-stu-id="33e87-103">Create a communications site for your campaign</span></span>

<span data-ttu-id="33e87-104">Un excellent moyen de communiquer les priorités, de partager des documents de stratégie et de mettre en surbrillance les événements à venir consiste à utiliser un site de communication dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="33e87-104">A great way to communicate priorities, share strategy documents, and highlight upcoming events is to use a communications site in SharePoint.</span></span> <span data-ttu-id="33e87-105">Les sites de communication sont destinés au partage des éléments à l’échelle de l’ensemble de votre campagne. Il s’agit de votre site de campagne interne.</span><span class="sxs-lookup"><span data-stu-id="33e87-105">Communications sites are for sharing things broadly across your whole campaign; it's your internal campaign site.</span></span>

## <a name="best-practices"></a><span data-ttu-id="33e87-106">Meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="33e87-106">Best practices</span></span>

<span data-ttu-id="33e87-107">Incluez les éléments suivants dans votre site de communication :</span><span class="sxs-lookup"><span data-stu-id="33e87-107">Include the following elements in your Communications site:</span></span>

1. <span data-ttu-id="33e87-108">Ajouter le logo et les couleurs de votre campagne sous forme d’image d’en-tête et de thème</span><span class="sxs-lookup"><span data-stu-id="33e87-108">Add your campaign logo and colors as a header image and theme</span></span>
2. <span data-ttu-id="33e87-109">Dirigez votre stratégie, votre message, vos documents importants, un annuaire et un Forum aux questions dans un **composant WebPart héros**.</span><span class="sxs-lookup"><span data-stu-id="33e87-109">Lead with your strategy, message, important documents, a directory, and FAQ in a **Hero web part**.</span></span>
3. <span data-ttu-id="33e87-110">Inclure une instruction candidate à l’équipe dans un **composant WebPart de texte**.</span><span class="sxs-lookup"><span data-stu-id="33e87-110">Include a candidate statement to the team in a **Text web part**.</span></span>
4. <span data-ttu-id="33e87-111">Ajoutez des événements de campagne marketing à un **composant WebPart événements** afin que tout le monde puisse voir ce qu’il se passe.</span><span class="sxs-lookup"><span data-stu-id="33e87-111">Add campaign events to an **Events web part** so everyone can see what's coming up.</span></span>
5. <span data-ttu-id="33e87-112">Ajoutez des photos que les utilisateurs peuvent utiliser ou partager avec un **composant WebPart Galerie d’images**.</span><span class="sxs-lookup"><span data-stu-id="33e87-112">Add photos that people can use or share to an **Image gallery web part**.</span></span>

![Diagramme d’une page de communications SharePoint avec un espace pour les éléments communs dont une campagne a besoin](../media/m365-democracy-comms-site.png)

## <a name="infographic-create-a-communications-site-infographic"></a><span data-ttu-id="33e87-114">Infographie : créer un site de communications infographie</span><span class="sxs-lookup"><span data-stu-id="33e87-114">Infographic: Create a Communications Site infographic</span></span> 
<span data-ttu-id="33e87-115">Les liens suivants pour PowerPoint et PDF peuvent être téléchargés et imprimés au format tabloïd (également appelé grand livre, 11 x 17 ou a3).</span><span class="sxs-lookup"><span data-stu-id="33e87-115">The following links for PowerPoint and PDF can be downloaded and printed in tabloid format (also known as ledger, 11 x 17, or A3).</span></span>

<span data-ttu-id="33e87-116">[![Image du site de communications infographie](../media/M365-Campaigns-CreateCommunicationSite-358-201.png)](downloads/M365CampaignsCreateCommunicationSite.pdf)</span><span class="sxs-lookup"><span data-stu-id="33e87-116">[![Image for communications site infographic](../media/M365-Campaigns-CreateCommunicationSite-358-201.png)](downloads/M365CampaignsCreateCommunicationSite.pdf)</span></span>

<span data-ttu-id="33e87-117">[PDF](downloads/M365CampaignsCreateCommunicationSite.pdf) | [PowerPoint](https://github.com/MicrosoftDocs/microsoft-365-docs-pr/raw/live/m365-democracy/microsoft-365/campaigns/downloads/M365CampaignsCreateCommunicationSite.pptx)</span><span class="sxs-lookup"><span data-stu-id="33e87-117">[PDF](downloads/M365CampaignsCreateCommunicationSite.pdf) | [PowerPoint](https://github.com/MicrosoftDocs/microsoft-365-docs-pr/raw/live/m365-democracy/microsoft-365/campaigns/downloads/M365CampaignsCreateCommunicationSite.pptx)</span></span>


## <a name="set-it-up"></a><span data-ttu-id="33e87-118">Configuration</span><span class="sxs-lookup"><span data-stu-id="33e87-118">Set it up</span></span>

1. <span data-ttu-id="33e87-119">Connectez-vous https://Office.comà.</span><span class="sxs-lookup"><span data-stu-id="33e87-119">Sign in to https://Office.com.</span></span>
2. <span data-ttu-id="33e87-120">Dans le coin supérieur gauche de la page, sélectionnez l’icône du lanceur d’applications, puis sélectionnez la vignette **SharePoint** .</span><span class="sxs-lookup"><span data-stu-id="33e87-120">In the top-left corner of the page, select the app launcher icon and then select the **SharePoint** tile.</span></span> <span data-ttu-id="33e87-121">Si vous ne voyez pas la vignette **SharePoint** , cliquez sur la vignette **sites** ou sur **tout** si SharePoint n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="33e87-121">If you don't see the **SharePoint** tile, click the **Sites** tile or **All** if SharePoint isn't visible.</span></span>
3. <span data-ttu-id="33e87-122">En haut de la page d’accueil SharePoint, cliquez sur **+ créer un site** , puis sur l’option **site de communication** .</span><span class="sxs-lookup"><span data-stu-id="33e87-122">At the top of the SharePoint home page, click **+ Create site** and choose the **Communication site** option.</span></span>

<span data-ttu-id="33e87-123">Découvrez toutes les [informations sur les sites](https://support.office.com/article/What-is-a-SharePoint-communication-site-94A33429-E580-45C3-A090-5512A8070732) de communication et la [création d’un site de communication dans SharePoint Online](https://support.microsoft.com/en-us/office/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb).</span><span class="sxs-lookup"><span data-stu-id="33e87-123">Learn all [about Communications sites](https://support.office.com/article/What-is-a-SharePoint-communication-site-94A33429-E580-45C3-A090-5512A8070732) and how to [create a communication site in SharePoint Online](https://support.microsoft.com/en-us/office/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb).</span></span>


## <a name="admin-settings"></a><span data-ttu-id="33e87-124">Paramètres d’administration</span><span class="sxs-lookup"><span data-stu-id="33e87-124">Admin settings</span></span>

<span data-ttu-id="33e87-125">Si vous ne voyez pas le lien **+ créer** un lien vers le site, la création de sites libre-service n’est peut-être pas disponible dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="33e87-125">If you don't see the **+ Create** site link, self-service site creation might not be available in Microsoft 365.</span></span> <span data-ttu-id="33e87-126">Pour créer un site d’équipe, contactez la personne qui administre Microsoft 365 dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="33e87-126">To create a team site, contact the person administering Microsoft 365 in your organization.</span></span> <span data-ttu-id="33e87-127">Si vous êtes un administrateur 365 de Microsoft, consultez la rubrique [Manage site Creation in SharePoint Online](https://docs.microsoft.com/sharepoint/manage-site-creation) pour activer la création de sites libre-service pour votre organisation ou [gérer les sites dans le nouveau centre d’administration SharePoint](https://docs.microsoft.com/sharepoint/manage-sites-in-new-admin-center) pour créer un site à partir du centre d’administration SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="33e87-127">If you're a Microsoft 365 admin, see [Manage site creation in SharePoint Online](https://docs.microsoft.com/sharepoint/manage-site-creation) to enable self-service site creation for your organization or [Manage sites in the new SharePoint admin center](https://docs.microsoft.com/sharepoint/manage-sites-in-new-admin-center) to create a site from the SharePoint Online admin center.</span></span>
  
