---
title: Partager des sites et des fichiers avec des utilisateurs invités
f1.keywords: NOCSH
ms.author: twerner
author: twernermsft
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- SPO_Content
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 89502322-bfbb-43d6-9207-4030f8ce26e0
ROBOTS: NOINDEX
description: 'Découvrez comment partager des sites et des fichiers avec des personnes extérieures à l’organisation. '
ms.openlocfilehash: 3857cee3073950bbb9c130368abdd7df68d0da2a
ms.sourcegitcommit: 0d709e9ab0d8d56c5fc11a921298f82e40e122c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50114464"
---
# <a name="share-sites-and-files-with-guest-users"></a><span data-ttu-id="58c6c-103">Partager des sites et des fichiers avec des utilisateurs invités</span><span class="sxs-lookup"><span data-stu-id="58c6c-103">Share sites and files with guest users</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="58c6c-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="58c6c-104">The admin center is changing.</span></span> <span data-ttu-id="58c6c-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="58c6c-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span></span>

::: moniker-end

<span data-ttu-id="58c6c-106">Pour collaborer avec des personnes extérieures à votre organisation, vous pouvez partager des sites entiers ou des fichiers spécifiques en externe.</span><span class="sxs-lookup"><span data-stu-id="58c6c-106">To collaborate with people outside your organization, you can share entire sites or specific files externally.</span></span> <span data-ttu-id="58c6c-107">Si vous voulez passer directement à la configuration du partage, sélectionnez le scénario que vous voulez activer :</span><span class="sxs-lookup"><span data-stu-id="58c6c-107">If you want to get straight to setting up sharing, choose the scenario you want to enable:</span></span>

- [<span data-ttu-id="58c6c-108">Collaborer avec des invités sur un document</span><span class="sxs-lookup"><span data-stu-id="58c6c-108">Collaborate with guests on a document</span></span>](../../solutions/collaborate-on-documents.md)
- [<span data-ttu-id="58c6c-109">Collaborer avec des invités sur un site</span><span class="sxs-lookup"><span data-stu-id="58c6c-109">Collaborate with guests in a site</span></span>](../../solutions/collaborate-in-site.md)
- [<span data-ttu-id="58c6c-110">Collaborer avec des invités au sein d’une équipe</span><span class="sxs-lookup"><span data-stu-id="58c6c-110">Collaborate with guests in a team</span></span>](../../solutions/collaborate-as-team.md)
  
## <a name="deciding-how-to-share-your-content"></a><span data-ttu-id="58c6c-111">Décider du mode de partage de votre contenu</span><span class="sxs-lookup"><span data-stu-id="58c6c-111">Deciding how to share your content</span></span>

<span data-ttu-id="58c6c-112">Quand vous déterminez si ou comment vous voulez partager du contenu de manière externe, posez-vous les questions suivantes :</span><span class="sxs-lookup"><span data-stu-id="58c6c-112">When considering if and how you want to share content externally, think about the following:</span></span>
  
- <span data-ttu-id="58c6c-113">À qui souhaitez-vous accorder l’accès au contenu sur le site et à tous les sous-sites, et que voulez-vous qu’ils puissent faire ?</span><span class="sxs-lookup"><span data-stu-id="58c6c-113">To whom do you want to grant access to content on the site and any subsites, and what do you want them to be able to do?</span></span>
    
- <span data-ttu-id="58c6c-114">À quelles personnes de votre organisation voulez-vous octroyer l'autorisation de partager du contenu avec l'extérieur ?</span><span class="sxs-lookup"><span data-stu-id="58c6c-114">To whom in your organization do you want to grant permission to share content externally?</span></span> 
    
- <span data-ttu-id="58c6c-115">Existe-t-il du contenu que vous voulez être sûr de ne jamais mettre à la disposition des personnes extérieures à votre organisation ?</span><span class="sxs-lookup"><span data-stu-id="58c6c-115">Is there content you want to ensure is never available to be viewed by people external to your organization?</span></span>
    
<span data-ttu-id="58c6c-116">Les réponses à ces questions vous aideront à planifier votre stratégie de partage de contenu.</span><span class="sxs-lookup"><span data-stu-id="58c6c-116">The answers to these questions will help you plan your strategy for content sharing.</span></span>
  
|<span data-ttu-id="58c6c-117">**Essayez ceci :**</span><span class="sxs-lookup"><span data-stu-id="58c6c-117">**Try this:**</span></span>|<span data-ttu-id="58c6c-118">**Si votre besoin est le suivant :**</span><span class="sxs-lookup"><span data-stu-id="58c6c-118">**If you need to…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58c6c-119">Ajouter un invité à un groupe</span><span class="sxs-lookup"><span data-stu-id="58c6c-119">Add a guest to a group</span></span>  <br/> |<span data-ttu-id="58c6c-120">Fournir à une personne extérieure à votre organisation un accès continu aux informations et au contenu d’un site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="58c6c-120">Provide someone outside your organization with ongoing access to information and content on a team site.</span></span> <span data-ttu-id="58c6c-121">Elle a besoin de pouvoir agir en tant qu'utilisateur à part entière du site, ainsi que de créer, modifier et afficher du contenu.</span><span class="sxs-lookup"><span data-stu-id="58c6c-121">They need the ability to perform like a full user of your site and create, edit, and view content.</span></span>  <br/> |
|<span data-ttu-id="58c6c-122">Partagez un document et exigez que les invités s’authentifier.</span><span class="sxs-lookup"><span data-stu-id="58c6c-122">Share a document and require guests to authenticate.</span></span>  <br/> |<span data-ttu-id="58c6c-123">Fournissez à des personnes spécifiques extérieures à votre organisation un accès sécurisé à un document pour révision ou collaboration, mais ces personnes n’ont pas besoin d’accéder à d’autres contenus sur le site.</span><span class="sxs-lookup"><span data-stu-id="58c6c-123">Provide specific people outside your organization with secure access to a document for review or collaboration, but these people do not require access to other content on the site.</span></span>  <br/> |
|<span data-ttu-id="58c6c-124">Partagez un document, mais ne nécessitez pas d’authentification.</span><span class="sxs-lookup"><span data-stu-id="58c6c-124">Share a document, but don't require authentication.</span></span>  <br/> |<span data-ttu-id="58c6c-125">Partager un lien vers un document qui n'est pas sensible ni confidentiel avec des personnes extérieures à votre organisation afin qu'elles puissent soit l'afficher, soit le mettre à jour en y ajoutant leurs commentaires.</span><span class="sxs-lookup"><span data-stu-id="58c6c-125">Share a link to a non-sensitive or non-confidential document with people outside your organization so that they can either view it or update it with feedback.</span></span> <span data-ttu-id="58c6c-126">Ces personnes n’ont pas besoin d’accéder au contenu du site.</span><span class="sxs-lookup"><span data-stu-id="58c6c-126">These people do not require access to content on the site.</span></span>  <br/> |
   
> [!IMPORTANT]
> <span data-ttu-id="58c6c-127">Lorsque vous désactivez le partage externe, les personnes extérieures à l’organisation qui ont actuellement accès n’y ont plus accès.</span><span class="sxs-lookup"><span data-stu-id="58c6c-127">When you disable external sharing, people outside the organization who currently have access will no longer have access.</span></span> <span data-ttu-id="58c6c-128">Si vous ré turniez ultérieurement le partage externe, l’accès sera restauré pour ces personnes.</span><span class="sxs-lookup"><span data-stu-id="58c6c-128">If you later turn external sharing back on, access will be restored for these people.</span></span> <span data-ttu-id="58c6c-129">Pour empêcher un utilisateur d’accéder à un contenu partagé, supprimez-le du groupe [Microsoft 365,](/office365/admin/create-groups/add-or-remove-members-from-groups)supprimez ses autorisations du site ou arrêtez de partager le fichier ou le dossier avec [lui.](https://support.microsoft.com/office/0a36470f-d7fe-40a0-bd74-0ac6c1e13323)</span><span class="sxs-lookup"><span data-stu-id="58c6c-129">To prevent a user from accessing a shared content, [remove them from the Microsoft 365 group](/office365/admin/create-groups/add-or-remove-members-from-groups), remove their permissions from the site, or [stop sharing the file or folder with them](https://support.microsoft.com/office/0a36470f-d7fe-40a0-bd74-0ac6c1e13323).</span></span> 
  
## <a name="enable-external-sharing-at-the-organization-level"></a><span data-ttu-id="58c6c-130">Activer le partage externe au niveau de l’organisation</span><span class="sxs-lookup"><span data-stu-id="58c6c-130">Enable external sharing at the organization level</span></span>

<span data-ttu-id="58c6c-131">Le partage externe est désactivé par défaut au niveau de l’organisation, mais pas pour tous les nouveaux sites.</span><span class="sxs-lookup"><span data-stu-id="58c6c-131">External sharing is turned on by default at the organization level, but not for all new sites.</span></span> <span data-ttu-id="58c6c-132">Pour plus d’informations, voir [vue d’ensemble du partage externe.](/sharepoint/external-sharing-overview)</span><span class="sxs-lookup"><span data-stu-id="58c6c-132">For info, see [External sharing overview](/sharepoint/external-sharing-overview).</span></span> 

> [!NOTE]
>  <span data-ttu-id="58c6c-133">Pour autoriser le partage externe pour n’importe quel site, vous devez l’autoriser au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="58c6c-133">To allow external sharing for any site, you need to allow it at the organization level.</span></span> 
  
1. <span data-ttu-id="58c6c-134">Dans le Centre [d’administration,](https://go.microsoft.com/fwlink/p/?linkid=2024339)tapez « externe » dans la zone de recherche de la page d’accueil, puis choisissez **Partage externe de sites.**</span><span class="sxs-lookup"><span data-stu-id="58c6c-134">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339), type "external" in the search box on the Home page, and choose **Sites external sharing**.</span></span>
  
2. <span data-ttu-id="58c6c-135">Sur la page qui s’ouvre, choisissez si les utilisateurs peuvent partager avec des invités existants uniquement, des invités nouveaux et existants, ou toute autre personne.</span><span class="sxs-lookup"><span data-stu-id="58c6c-135">On the page that opens, choose whether users can share with existing guests only, new and existing guests, or anyone.</span></span> 
    
3. <span data-ttu-id="58c6c-136">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="58c6c-136">Select **Save**.</span></span>
    
<span data-ttu-id="58c6c-137">Après avoir activé le partage externe au niveau de l’organisation, vous pouvez affiner vos paramètres de partage pour désactiver le partage externe pour des sites particuliers.</span><span class="sxs-lookup"><span data-stu-id="58c6c-137">After you enable external sharing at the organization level, you can fine tune your sharing settings to disable external sharing for particular sites.</span></span> <span data-ttu-id="58c6c-138">Pour plus d’informations, voir Activer ou désactiver le partage [externe pour un site.](/sharepoint/change-external-sharing-site)</span><span class="sxs-lookup"><span data-stu-id="58c6c-138">For info, see [Turn external sharing on or off for a site](/sharepoint/change-external-sharing-site).</span></span>
  

  

    

