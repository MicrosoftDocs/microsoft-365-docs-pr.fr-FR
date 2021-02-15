---
title: Expérience utilisateur dans un environnement multigéographique
ms.reviewer: adwood
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: o365-solutions
ms.collection:
- SPO_Content
- Strat_SP_gtc
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
localization_priority: Normal
description: Découvrez l’expérience utilisateur de SharePoint, de OneDrive et d’Exchange dans un environnement multigéographique pour Microsoft 365.
ms.openlocfilehash: 558e5a1f7ff2f6f5485a9f32d6e2b43b552b7f17
ms.sourcegitcommit: ae646779d84e993cf80b1207e76b856a21be5790
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/04/2021
ms.locfileid: "49749574"
---
# <a name="user-experience-in-a-multi-geo-environment"></a><span data-ttu-id="1c01e-103">Expérience utilisateur dans un environnement multigéographique</span><span class="sxs-lookup"><span data-stu-id="1c01e-103">User experience in a multi-geo environment</span></span>

<span data-ttu-id="1c01e-104">Voici ce que vos utilisateurs verront dans une configuration multigéographique de OneDrive :</span><span class="sxs-lookup"><span data-stu-id="1c01e-104">Here's what your users will see in a OneDrive Multi-Geo configuration:</span></span>

## <a name="exchange-mailbox"></a><span data-ttu-id="1c01e-105">Boîte aux lettres Exchange</span><span class="sxs-lookup"><span data-stu-id="1c01e-105">Exchange mailbox</span></span>

<span data-ttu-id="1c01e-106">La boîte aux lettres Exchange d’un utilisateur est approvisionnée dans l’emplacement par défaut des données de celui-ci, et déplacée automatiquement si cet emplacement change.</span><span class="sxs-lookup"><span data-stu-id="1c01e-106">A user's Exchange mailbox is provisioned to their preferred data location, and is automatically relocated if their PDL changes.</span></span> <span data-ttu-id="1c01e-107">Les utilisateurs peuvent se servir d’Outlook et d’Outlook sur le web normalement, sans que cela change l’expérience utilisateur dans un environnement multigéographique.</span><span class="sxs-lookup"><span data-stu-id="1c01e-107">Users can use Outlook and Outlook on the web normally with no change in user experience in a multi-geo environment.</span></span>

## <a name="hub-sites"></a><span data-ttu-id="1c01e-108">Sites hub</span><span class="sxs-lookup"><span data-stu-id="1c01e-108">Hub sites</span></span>

<span data-ttu-id="1c01e-109">Les sites hub SharePoint améliorent la détection et renforcent l’implication à l’aide de contenu destiné aux employés lors de la création d’une représentation complète et cohérente de projets, départements ou régions.</span><span class="sxs-lookup"><span data-stu-id="1c01e-109">SharePoint Hub sites enhances the discovery and engagement with content for employees, while creating a complete and consistent representation of projects, departments or regions.</span></span> <span data-ttu-id="1c01e-110">Dans un environnement multigéographique, des sites d’emplacements satellites peuvent facilement être associés à un site hub, indépendamment de l’emplacement géographique de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="1c01e-110">In a multi-geo environment, sites from satellite locations can easily be associated with a hub site regardless the hub site's geo location.</span></span> <span data-ttu-id="1c01e-111">Les utilisateurs peuvent rechercher et obtenir des résultats sur le hub via une simple expérience de recherche, indépendamment de l’emplacement géographique des sites.</span><span class="sxs-lookup"><span data-stu-id="1c01e-111">Users can search and get results across the hub through a single search experience, regardless of the geo location of the sites.</span></span>

## <a name="microsoft-365-app-launcher"></a><span data-ttu-id="1c01e-112">Lanceur d’applications Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1c01e-112">Microsoft 365 app launcher</span></span>

<span data-ttu-id="1c01e-113">Le lanceur d’applications prend en compte la configuration multigéographique et dirige chaque vignette vers l’emplacement géographique approprié de la charge de travail.</span><span class="sxs-lookup"><span data-stu-id="1c01e-113">The app launcher is multi-geo aware and will direct each tile to the appropriate geo location of the workload.</span></span> <span data-ttu-id="1c01e-114">Les vignettes SharePoint et OneDrive pointent vers l’utilisateur à l’emplacement correspondant à l’emplacement géographique approvisionné de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c01e-114">The SharePoint and OneDrive tiles will point the user to the location corresponding to the user's provisioned geo location.</span></span> <span data-ttu-id="1c01e-115">Cela signifie que, si l’utilisateur a un OneDrive dans l’emplacement central, sa vignette SharePoint pointe vers sa page d’accueil SharePoint dans l’emplacement central, mais que son site de groupe sera approvisionné à l’emplacement correspondant à son emplacement par défaut des données.</span><span class="sxs-lookup"><span data-stu-id="1c01e-115">This means that is the user has a OneDrive in the central location, their SharePoint tile will point them to SP Home in the central location but their group site will be provisioned in the location corresponding to their PDL.</span></span> 

## <a name="office-applications"></a><span data-ttu-id="1c01e-116">Applications Office</span><span class="sxs-lookup"><span data-stu-id="1c01e-116">Office applications</span></span>

<span data-ttu-id="1c01e-117">Les applications Office telles que Word, Excel et PowerPoint détectent automatiquement l’emplacement géographique OneDrive Entreprise correct pour chaque utilisateur à la connexion.</span><span class="sxs-lookup"><span data-stu-id="1c01e-117">Office applications such as Word, Excel, and PowerPoint will automatically detect the correct OneDrive for Business geo-location for each user when they log in.</span></span> <span data-ttu-id="1c01e-118">Les utilisateurs ne doivent pas entrer l’URL géographique spécifique de leurs sites OneDrive ou SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1c01e-118">Users do not need to enter the geo-specific URL for their OneDrive or SharePoint sites.</span></span>

## <a name="onedrive-for-business-sync-client"></a><span data-ttu-id="1c01e-119">Client de synchronisation OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="1c01e-119">OneDrive for Business Sync Client</span></span>

<span data-ttu-id="1c01e-120">Le Client de synchronisation OneDrive Entreprise (version 17.3.6943.0625 et les versions ultérieures) détecte automatiquement l’emplacement géographique OneDrive Entreprise correct pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c01e-120">The OneDrive for Business Sync Client (version 17.3.6943.0625 and later) will automatically detect the correct OneDrive for Business geo location for the user.</span></span> <span data-ttu-id="1c01e-121">La prise en charge du client de synchronisation inclut la possibilité de synchroniser des sites basés sur des groupes, quel que soit leur emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="1c01e-121">Sync client support includes the ability to sync groups-based sites regardless of their geo location.</span></span> <span data-ttu-id="1c01e-122">Notez que le client de synchronisation Groove n’est pas pris en charge dans une configuration multigéographique.</span><span class="sxs-lookup"><span data-stu-id="1c01e-122">Note that the Groove sync client is not supported for multi-geo.</span></span> 

## <a name="onedrive-for-business-location"></a><span data-ttu-id="1c01e-123">Emplacement OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="1c01e-123">OneDrive for Business location</span></span>

<span data-ttu-id="1c01e-p106">OneDrive Entreprise sera configuré pour les utilisateurs dans leur emplacement de données préféré. Si un utilisateur accède à une URL OneDrive qui contient un emplacement géographique incorrect (par exemple, un signet provenant d’un emplacement géographique précédent), il est automatiquement redirigé vers OneDrive dans l’emplacement géographique approprié.</span><span class="sxs-lookup"><span data-stu-id="1c01e-p106">Users will have their OneDrive for Business provisioned in their preferred data location. If a user navigates to a OneDrive URL that contains an incorrect geo location (such as a bookmark from a previous geo location), they are automatically redirected to the OneDrive in the appropriate geo location.</span></span>

## <a name="onedrive-ios-and-android"></a><span data-ttu-id="1c01e-126">OneDrive iOS et Android</span><span class="sxs-lookup"><span data-stu-id="1c01e-126">OneDrive iOS and Android</span></span> 

<span data-ttu-id="1c01e-p107">Les applications mobiles OneDrive iOS et Android indiquent vos fichiers OneDrive et les fichiers partagés avec vous, indépendamment de leur emplacement géographique. Les recherches dans les applications mobiles OneDrive affichent des résultats pertinents de tous les emplacements géographiques. Téléchargez la dernière version de ces applications.</span><span class="sxs-lookup"><span data-stu-id="1c01e-p107">The OneDrive iOS and Android mobile apps will show you your OneDrive files and files shared with you regardless of their geo location. Search from the OneDrive mobile apps will show relevant results from all geo locations. Please download the latest version of these apps.</span></span>

<span data-ttu-id="1c01e-130">Consultez [OneDrive sur iOS](https://support.office.com/article/08d5c5b2-ccc6-40eb-a244-fe3597a3c247) et [Utiliser OneDrive sur Android](https://support.office.com/article/eee1d31c-792d-41d4-8132-f9621b39eb36) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1c01e-130">See Use [OneDrive on iOS](https://support.office.com/article/08d5c5b2-ccc6-40eb-a244-fe3597a3c247) and [Use OneDrive for Android](https://support.office.com/article/eee1d31c-792d-41d4-8132-f9621b39eb36) for more information.</span></span>

## <a name="onedrive-mobile-client"></a><span data-ttu-id="1c01e-131">Client mobile OneDrive</span><span class="sxs-lookup"><span data-stu-id="1c01e-131">OneDrive Mobile Client</span></span> 

<span data-ttu-id="1c01e-132">Le client mobile OneDrive prend en compte la configuration multigéographique et affiche du contenu et des résultats pertinents de tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="1c01e-132">The OneDrive Mobile Client is multi-geo aware and will display pertinent content and results from all geo locations.</span></span>

## <a name="search"></a><span data-ttu-id="1c01e-133">Search</span><span class="sxs-lookup"><span data-stu-id="1c01e-133">Search</span></span>

<span data-ttu-id="1c01e-p108">Chaque emplacement géographique a ses propres index de recherche et son centre de recherche. Lorsqu’un utilisateur effectue une recherche, la requête est envoyée à tous les emplacements géographiques et les résultats renvoyés sont fusionnés puis classés afin que l’utilisateur dispose de résultats unifiés. Les utilisateurs obtiennent des résultats de tous les emplacements géographiques, indépendamment de leur emplacement géographique. Reportez-vous à la rubrique relative à la [configuration de la recherche pour OneDrive Entreprise Multi-Géo](configure-search-for-multi-geo.md) pour des informations spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1c01e-p108">Each geo location has its own search index and Search Center. When a user searches, the query is sent to all the geo locations, and the returned results are merged and then ranked so the user gets unified results. Users get results from all geo locations regardless of their own geo location. See [Configure Search for OneDrive for Business Multi-Geo](configure-search-for-multi-geo.md) for specifics.</span></span>

<span data-ttu-id="1c01e-138">Les clients de recherche suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="1c01e-138">The following search clients are supported:</span></span>

-   <span data-ttu-id="1c01e-139">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="1c01e-139">OneDrive for Business</span></span>

-   <span data-ttu-id="1c01e-140">Delve</span><span class="sxs-lookup"><span data-stu-id="1c01e-140">Delve</span></span>

-   <span data-ttu-id="1c01e-141">Page d’accueil SharePoint</span><span class="sxs-lookup"><span data-stu-id="1c01e-141">SharePoint Home</span></span>

-   <span data-ttu-id="1c01e-142">Centre de recherche</span><span class="sxs-lookup"><span data-stu-id="1c01e-142">The Search Center</span></span>

-   <span data-ttu-id="1c01e-143">Applications de recherche personnalisée qui utilisent l’API de recherche SharePoint</span><span class="sxs-lookup"><span data-stu-id="1c01e-143">Custom search applications that use the SharePoint Search API</span></span>

## <a name="sharepoint-home"></a><span data-ttu-id="1c01e-144">Page d’accueil SharePoint</span><span class="sxs-lookup"><span data-stu-id="1c01e-144">SharePoint Home</span></span> 

<span data-ttu-id="1c01e-145">Dans SharePoint multigéographique, votre page d’accueil SharePoint est hébergée dans l’emplacement où l’utilisateur se trouve, tel que déterminé par son emplacement OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="1c01e-145">In SharePoint Multi-Geo your SharePoint home is hosted in the location where the user resides as determined by their OneDrive for business location.</span></span> <span data-ttu-id="1c01e-146">Par exemple, si le OneDrive de l’utilisateur est hébergé dans un emplacement satellite européen, la page d’accueil SharePoint sera restituée à partir de l’Europe.</span><span class="sxs-lookup"><span data-stu-id="1c01e-146">For example: if the user has their OneDrive hosted in an European satellite location, their SharePoint Home will be rendered from Europe.</span></span> <span data-ttu-id="1c01e-147">La page d’accueil SharePoint inclut tout contenu pertinent pour l’utilisateur indépendamment de son emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="1c01e-147">SharePoint home includes all content relevant to the user regardless of its geo location.</span></span> 

<span data-ttu-id="1c01e-148">**Sites suivis, Actualités de sites, Sites récents, Sites fréquents et Sites suggérés**</span><span class="sxs-lookup"><span data-stu-id="1c01e-148">**Followed Sites, News from Sites, Recent Sites, Frequent Sites, and Suggested sites**</span></span>

<span data-ttu-id="1c01e-149">Toutes ces composants s’affichent pour l’utilisateur indépendamment de l’emplacement géographique où le contenu est hébergé, aussi longtemps que l’utilisateur est autorisé à accéder au contenu en question.</span><span class="sxs-lookup"><span data-stu-id="1c01e-149">All of these components will show up for the user regardless of the geo location where the content is hosted, so long as the user has permissions to said content.</span></span> 

<span data-ttu-id="1c01e-150">**Liens proposés**</span><span class="sxs-lookup"><span data-stu-id="1c01e-150">**Features Links**</span></span>

<span data-ttu-id="1c01e-151">Les administrateurs peuvent configurer dans la page d’accueil SharePoint des liens proposés pertinents pour chaque emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="1c01e-151">Admins may configure Featured links in SharePoint home as appropriate to each geo location.</span></span> <span data-ttu-id="1c01e-152">Ainsi, dans la page d’accueil SharePoint, l’administrateur peut suggérer, pour chaque région, des liens appropriés pour les utilisateurs dans cette région.</span><span class="sxs-lookup"><span data-stu-id="1c01e-152">This allows the admin to feature in the SP Home for each region the links that are appropriate for users in the region.</span></span> 

## <a name="sharepoint-mobile-client"></a><span data-ttu-id="1c01e-153">Client mobile SharePoint</span><span class="sxs-lookup"><span data-stu-id="1c01e-153">SharePoint Mobile Client</span></span> 

<span data-ttu-id="1c01e-154">Le client mobile SharePoint prend en compte la configuration multigéographique et affiche du contenu et des résultats pertinents de tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="1c01e-154">The SharePoint Mobile Client is multi-geo aware and will display pertinent content and results from all geo locations.</span></span>

## <a name="sharing"></a><span data-ttu-id="1c01e-155">Partage</span><span class="sxs-lookup"><span data-stu-id="1c01e-155">Sharing</span></span>

<span data-ttu-id="1c01e-156">L’interface du Sélecteur de personnes affiche tous les utilisateurs indépendamment de leur emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="1c01e-156">The People Picker experience shows all users regardless of their geo location.</span></span> <span data-ttu-id="1c01e-157">Cela permet à un utilisateur de partager avec un autre utilisateur dans le même emplacement géographique, ou dans tout autre emplacement géographique de votre locataire.</span><span class="sxs-lookup"><span data-stu-id="1c01e-157">This allows a user to share with another user in their same geo or in any other of your tenant's geo locations.</span></span> <span data-ttu-id="1c01e-158">Le contenu des différents emplacements géographiques s’affiche dans la vue **Partagé avec moi** sur le OneDrive Entreprise de l’utilisateur, et est accessible via une interface d’authentification unique indépendamment de l’emplacement géographique où il est hébergé.</span><span class="sxs-lookup"><span data-stu-id="1c01e-158">Content from different geo locations will show up in the **Shared with Me** view in the user's OneDrive for Business and can be accessed with Single Sign-On experience regardless of which geo location it is hosted in.</span></span>

## <a name="teams-experience"></a><span data-ttu-id="1c01e-159">Expérience Teams</span><span class="sxs-lookup"><span data-stu-id="1c01e-159">Teams Experience</span></span>

<span data-ttu-id="1c01e-160">Teams prend en compte la configuration multigéographique.</span><span class="sxs-lookup"><span data-stu-id="1c01e-160">Teams is multi-geo aware.</span></span> <span data-ttu-id="1c01e-161">Les fichiers OneDrive et les fichiers récemment consultés s’affichent indépendamment de l’emplacement géographique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c01e-161">OneDrive files and recently viewed files are shown regardless of the user's geo location.</span></span> <span data-ttu-id="1c01e-162">Les mentions @ fonctionnent avec des utilisateurs de tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="1c01e-162">@ mentions work with users from all geo-locations.</span></span>

## <a name="user-profiles"></a><span data-ttu-id="1c01e-163">Profils utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c01e-163">User profiles</span></span>

<span data-ttu-id="1c01e-p113">Les informations de profil utilisateur sont gérées dans l’emplacement géographique de l’utilisateur. Lorsque vous sélectionnez un utilisateur, vous êtes redirigé vers l’emplacement géographique approprié pour l’utilisateur, qui indique ses informations de profil complètes.</span><span class="sxs-lookup"><span data-stu-id="1c01e-p113">User profile information is mastered in the user's geo location. When selecting a user, you will be directed to the appropriate geo location for the user, where you will see their full profile details.</span></span>

<span data-ttu-id="1c01e-166">Si Delve est désactivé, vous voyez l’expérience profil classique dans SharePoint, qui n’est pas adaptée à Multi-Géo.</span><span class="sxs-lookup"><span data-stu-id="1c01e-166">If Delve is turned off, you will see the classic profile experience in SharePoint, which is not multi-geo aware.</span></span>


