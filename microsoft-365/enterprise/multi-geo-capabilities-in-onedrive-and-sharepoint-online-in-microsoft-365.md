---
title: Fonctionnalités multi-géographiques OneDrive et SharePoint Online
ms.reviewer: adwood
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: o365-solutions
f1.keywords:
- NOCSH
ms.custom: ''
ms.collection:
- Strat_SP_gtc
- SPO_Content
- m365solution-scenario
- m365solution-spintranet
localization_priority: Normal
ms.assetid: 094e86f2-9ff0-40ac-af31-28fcaba00c1d
description: Étendez votre présence Microsoft 365 à plusieurs régions géographiques grâce aux fonctionnalités multi-géographiques dans OneDrive Online.
ms.openlocfilehash: 405f876317a6cec6defdf3f1a49b0dc32ac0add2
ms.sourcegitcommit: f7fbf45af64c5c0727fd5eaab309d20ad097a483
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "53362281"
---
# <a name="multi-geo-capabilities-in-onedrive-and-sharepoint-online"></a><span data-ttu-id="6df1c-103">Fonctionnalités multi-géographiques OneDrive et SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6df1c-103">Multi-Geo Capabilities in OneDrive and SharePoint Online</span></span>

<span data-ttu-id="6df1c-104">Les fonctionnalités Multi-Géo dans OneDrive et SharePoint Online permettent de contrôler les ressources partagées telles que les sites d’équipe SharePoint et les boîtes aux lettres de groupe Microsoft 365 stockées au repos dans un emplacement géographique spécifié.</span><span class="sxs-lookup"><span data-stu-id="6df1c-104">Multi-Geo capabilities in OneDrive and SharePoint Online enables control of shared resources like SharePoint team sites and Microsoft 365 Group mailboxes stored at rest in a specified geo location.</span></span>

<span data-ttu-id="6df1c-105">Chaque utilisateur, une boîte aux lettres de groupe et un site SharePoint ont un emplacement recommandé de données (PDL) qui indique l’emplacement géographique où les données connexes sont stockées.</span><span class="sxs-lookup"><span data-stu-id="6df1c-105">Each user, Group mailbox, and SharePoint site has a Preferred Data Location (PDL) which denotes the geo location where related data is to be stored.</span></span> <span data-ttu-id="6df1c-106">Les donnée personnelle des utilisateurs (boîte aux lettres Exchange et OneDrive), ainsi que les sites de Groupes Microsoft 365 ou SharePoint qu’ils créent peuvent être stockées dans l’emplacement spécifié géographique pour répondre aux exigences de résidence de données.</span><span class="sxs-lookup"><span data-stu-id="6df1c-106">Users' personal data (Exchange mailbox and OneDrive) along with any Microsoft 365 Groups or SharePoint sites that they create can be stored in the specified geo location to meet data residency requirements.</span></span> <span data-ttu-id="6df1c-107">Vous pouvez[spécifier des différents administrateurs pour chaque emplacement géo](add-a-sharepoint-geo-admin.md).</span><span class="sxs-lookup"><span data-stu-id="6df1c-107">You can [specify different administrators for each geo location](add-a-sharepoint-geo-admin.md).</span></span>

<span data-ttu-id="6df1c-108">Les utilisateurs profitent d’une expérience transparente lors de l’utilisation des services Microsoft 365, y compris les applications Office, OneDrive et Recherche.</span><span class="sxs-lookup"><span data-stu-id="6df1c-108">Users get a seamless experience when using Microsoft 365 services, including Office applications, OneDrive, and Search.</span></span> <span data-ttu-id="6df1c-109">Voir [Expérience utilisateur dans un environnement multigéographique](multi-geo-user-experience.md) pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="6df1c-109">See [User experience in a multi-geo environment](multi-geo-user-experience.md) for details.</span></span>

## <a name="onedrive"></a><span data-ttu-id="6df1c-110">OneDrive</span><span class="sxs-lookup"><span data-stu-id="6df1c-110">OneDrive</span></span>

<span data-ttu-id="6df1c-111">Le OneDrive de chaque utilisateur peut être configuré dans ou [déplacé par un administrateur](move-onedrive-between-geo-locations.md) vers un emplacement satellite conformément aux PDL de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6df1c-111">Each user's OneDrive can be provisioned in or [moved by an administrator](move-onedrive-between-geo-locations.md) to a satellite location in accordance with the user's PDL.</span></span> <span data-ttu-id="6df1c-112">Les fichiers personnels sont alors conservés dans cet emplacement géo, même s’ils peuvent être partagés avec des utilisateurs dans d’autres emplacements géo.</span><span class="sxs-lookup"><span data-stu-id="6df1c-112">Personal files are then kept in that geo location, though they can be shared with users in other geo locations.</span></span>

## <a name="sharepoint-sites-and-groups"></a><span data-ttu-id="6df1c-113">Sites et groupes SharePoint</span><span class="sxs-lookup"><span data-stu-id="6df1c-113">SharePoint Sites and Groups</span></span>

<span data-ttu-id="6df1c-114">La gestion de la fonctionnalité géo multiple est disponible via le Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6df1c-114">Management of the Multi-Geo feature is available through the SharePoint admin center.</span></span> <span data-ttu-id="6df1c-115">Vous trouverez des informations détaillées dans le [ billet de blog correspondant](https://techcommunity.microsoft.com/t5/Office-365-Blog/Now-available-Multi-Geo-in-SharePoint-and-Office-365-Groups/ba-p/263302).</span><span class="sxs-lookup"><span data-stu-id="6df1c-115">Detailed information can be found in the [corresponding blog post](https://techcommunity.microsoft.com/t5/Office-365-Blog/Now-available-Multi-Geo-in-SharePoint-and-Office-365-Groups/ba-p/263302).</span></span>

<span data-ttu-id="6df1c-116">Lorsqu’un utilisateur crée un site connecté à un groupe SharePoint dans un environnement multigéographique, leur PDL permet de déterminer l’emplacement géo où le site et sa boîte aux lettres de groupe associés sont créés.</span><span class="sxs-lookup"><span data-stu-id="6df1c-116">When a user creates a SharePoint group-connected site in a multi-geo environment, their PDL is used to determine the geo location where the site and its associated Group mailbox is created.</span></span> <span data-ttu-id="6df1c-117">(Si une valeur PDL de l’utilisateur n’a pas été définie ou a été définie sur l’emplacement géo qui n’a pas été configuré comme un emplacement satellite, puis le site et la boîte aux lettres sont créés dans l’emplacement central.)</span><span class="sxs-lookup"><span data-stu-id="6df1c-117">(If the user's PDL value hasn't been set, or has been set to geo location that hasn't been configured as a satellite location, then the site and mailbox are created in the central location.)</span></span>

<span data-ttu-id="6df1c-118">Microsoft 365 autres services que Exchange, OneDrive, SharePoint et Teams ne sont pas multigéo géographiques.</span><span class="sxs-lookup"><span data-stu-id="6df1c-118">Microsoft 365 services other than Exchange, OneDrive, SharePoint, and Teams are not Multi-Geo.</span></span> <span data-ttu-id="6df1c-119">Toutefois, les groupes Microsoft 365 créés par ces services seront configurés avec la PDL du créateur et leur boîte aux lettres de groupe Exchange, le site SharePoint est configuré dans la géo correspondante.</span><span class="sxs-lookup"><span data-stu-id="6df1c-119">However, Microsoft 365 Groups that are created by these services will be configured with the PDL of the creator and their Exchange Group mailbox, SharePoint site are provisioned in the corresponding geo.</span></span> 

## <a name="managing-the-multi-geo-environment"></a><span data-ttu-id="6df1c-120">Gestion de l’environnement multi-Géo</span><span class="sxs-lookup"><span data-stu-id="6df1c-120">Managing the multi-geo environment</span></span>

<span data-ttu-id="6df1c-121">Configurer et gérer votre environnement multi-géographique sont effectués via le Centre d’Administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6df1c-121">Setting up and managing your multi-geo environment is done through the SharePoint admin center.</span></span> 

![Capture d’écran de la page emplacements géo dans le Centre d’Administration SharePoint](../media/sharepoint-multi-geo-admin-center.png)

<span data-ttu-id="6df1c-123">(Certaines actions, telles que le déplacement d’un site SharePoint ou un site OneDrive nécessitent Microsoft PowerShell).</span><span class="sxs-lookup"><span data-stu-id="6df1c-123">(Some actions, such as moving a SharePoint site or a OneDrive site require Microsoft PowerShell.)</span></span>

## <a name="see-also"></a><span data-ttu-id="6df1c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6df1c-124">See also</span></span>

[<span data-ttu-id="6df1c-125">Multi-Geo dans les groupes SharePoint et Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6df1c-125">Multi-Geo in SharePoint and Microsoft 365 Groups</span></span>](https://techcommunity.microsoft.com/t5/Office-365-Blog/Now-available-Multi-Geo-in-SharePoint-and-Office-365-Groups/ba-p/263302)

[<span data-ttu-id="6df1c-126">Administration d’un environnement multi-géographique</span><span class="sxs-lookup"><span data-stu-id="6df1c-126">Administering a multi-geo environment</span></span>](administering-a-multi-geo-environment.md)

[<span data-ttu-id="6df1c-127">Quotas de stockage SharePoint dans des environnements multi-géographiques</span><span class="sxs-lookup"><span data-stu-id="6df1c-127">SharePoint storage quotas in multi-geo environments</span></span>](sharepoint-multi-geo-storage-quota.md)

[<span data-ttu-id="6df1c-128">Administration des boîtes aux lettres Exchange Online dans un environnement multi-géographique</span><span class="sxs-lookup"><span data-stu-id="6df1c-128">Administering Exchange Online mailboxes in a multi-geo environment</span></span>](administering-exchange-online-multi-geo.md)
