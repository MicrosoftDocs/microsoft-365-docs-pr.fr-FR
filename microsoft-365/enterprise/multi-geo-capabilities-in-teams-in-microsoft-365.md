---
title: Fonctionnalités multigé géographiques dans Microsoft Teams
ms.reviewer: daro
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
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
description: Découvrez comment Teams fonctionne avec Microsoft 365 multigéogé.
ms.openlocfilehash: 9fe9b289b0ffbef12327c4232b9deb6727b6d718
ms.sourcegitcommit: f7fbf45af64c5c0727fd5eaab309d20ad097a483
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "53362652"
---
# <a name="multi-geo-capabilities-in-microsoft-teams"></a><span data-ttu-id="81b4a-103">Fonctionnalités multigé géographiques dans Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="81b4a-103">Multi-Geo capabilities in Microsoft Teams</span></span>

<span data-ttu-id="81b4a-104">Les fonctionnalités multigéogé Teams permettent Teams données de conversation d’être stockées au repos dans un emplacement géographique spécifié.</span><span class="sxs-lookup"><span data-stu-id="81b4a-104">Multi-Geo capabilities in Teams enables Teams chat data to be stored at rest in a specified geo location.</span></span> <span data-ttu-id="81b4a-105">Les données de conversation se composent de messages de conversation, y compris les messages privés, les messages de canal et les images utilisées dans les conversations.</span><span class="sxs-lookup"><span data-stu-id="81b4a-105">Chat data consists of chat messages, including private messages, channel messages, and images used in chats.</span></span>

<span data-ttu-id="81b4a-106">Teams utilise la PDL (Preferred Data Location) pour les utilisateurs et les groupes pour déterminer où stocker les données.</span><span class="sxs-lookup"><span data-stu-id="81b4a-106">Teams uses the Preferred Data Location (PDL) for users and groups to determine where to store data.</span></span> <span data-ttu-id="81b4a-107">Si la PDL n’est pas définie ou n’est pas valide, les données sont stockées dans l’emplacement central du client.</span><span class="sxs-lookup"><span data-stu-id="81b4a-107">If the PDL is not set or is invalid, data is stored in the tenant's central location.</span></span>

## <a name="user-chat"></a><span data-ttu-id="81b4a-108">Conversation utilisateur</span><span class="sxs-lookup"><span data-stu-id="81b4a-108">User chat</span></span>

<span data-ttu-id="81b4a-109">La conversation utilisateur inclut les messages de réunion un-à-un, un-à-plusieurs et les messages de réunion privée.</span><span class="sxs-lookup"><span data-stu-id="81b4a-109">User chat includes one-to-one, one-to-many, and private meeting messages.</span></span>

<span data-ttu-id="81b4a-110">Lorsqu’un nouvel utilisateur est créé, Teams lit le PDL de l’utilisateur et stocke toutes ses données de conversation dans cet emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="81b4a-110">When a new user is created, Teams reads the user's PDL and stores all their chat data in that geo location.</span></span>

<span data-ttu-id="81b4a-111">Pour les utilisateurs existants, si un administrateur ajoute ou modifie le PDL d’un utilisateur, les données de conversation de cet utilisateur sont ajoutées à une file d’attente de migration pour être déplacées vers l’emplacement géographique spécifié.</span><span class="sxs-lookup"><span data-stu-id="81b4a-111">For existing users, if an administrator adds or modifies the PDL for a user, that user's chat data is added to a migration queue to be moved to the specified geo location.</span></span>

<span data-ttu-id="81b4a-112">L’emplacement de stockage d’une conversation un-à-un ou un-à-plusieurs est basé sur la PDL de la personne qui a créé la conversation.</span><span class="sxs-lookup"><span data-stu-id="81b4a-112">The storage location for a one-to-one or one-to-many chat is based on the PDL of the person who created the chat.</span></span> <span data-ttu-id="81b4a-113">Si le PDL de cet utilisateur est modifié, la conversation est migrée vers le nouvel emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="81b4a-113">If that user's PDL is changed, the chat will be migrated to the new geo location.</span></span> <span data-ttu-id="81b4a-114">L’emplacement de stockage d’une conversation de réunion est basé sur le PDL de l’organisateur de la réunion.</span><span class="sxs-lookup"><span data-stu-id="81b4a-114">The storage location for a meeting chat is based on the PDL of the meeting organizer.</span></span>

<span data-ttu-id="81b4a-115">Pour rechercher l’emplacement actuel des données d’Teams utilisateur, connectez-vous [à Teams PowerShell](/powershell/module/teams/connect-microsoftteams) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="81b4a-115">To find the current location of a user's Teams data, [connect to Teams PowerShell](/powershell/module/teams/connect-microsoftteams) and run the following command:</span></span>

```PowerShell
Get-MultiGeoRegion -EntityType User -EntityId <UPN>
```

## <a name="channel-messages"></a><span data-ttu-id="81b4a-116">Messages de canal</span><span class="sxs-lookup"><span data-stu-id="81b4a-116">Channel messages</span></span>

<span data-ttu-id="81b4a-117">Chaque Microsoft 365 a un emplacement de données par choix (PDL) qui indique l’emplacement géographique où les données associées doivent être stockées.</span><span class="sxs-lookup"><span data-stu-id="81b4a-117">Each Microsoft 365 group has a Preferred Data Location (PDL) which denotes the geo location where related data is to be stored.</span></span> <span data-ttu-id="81b4a-118">Teams utilise la PDL pour le groupe associé à chaque équipe pour déterminer où stocker les données de messagerie de canal pour cette équipe.</span><span class="sxs-lookup"><span data-stu-id="81b4a-118">Teams uses the PDL for the group associated with each team to determine where to store channel messaging data for that team.</span></span> <span data-ttu-id="81b4a-119">Cela inclut la conversation qui se produit au sein d’une réunion de canal.</span><span class="sxs-lookup"><span data-stu-id="81b4a-119">This includes chat that occurs within a channel meeting.</span></span>

<span data-ttu-id="81b4a-120">Lorsqu’un utilisateur crée une équipe, le PDL de cet utilisateur détermine quelle PDL est affectée au groupe Microsoft 365 utilisateur.</span><span class="sxs-lookup"><span data-stu-id="81b4a-120">When a user creates a new team, that user's PDL determines what PDL is assigned to the Microsoft 365 group.</span></span> <span data-ttu-id="81b4a-121">La PDL du groupe détermine l’endroit où les données de cette équipe sont stockées.</span><span class="sxs-lookup"><span data-stu-id="81b4a-121">The group PDL determines where that team's data is stored.</span></span> <span data-ttu-id="81b4a-122">Si le PDL de cet utilisateur change ultérieurement, le PDL du groupe n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="81b4a-122">If that user's PDL later changes, the group's PDL is not changed.</span></span>

<span data-ttu-id="81b4a-123">Pour les équipes existantes, si un administrateur ajoute ou modifie le PDL pour le groupe Microsoft 365 qui assure le soutien d’une équipe, les données de messagerie de canal de cette équipe sont ajoutées à une file d’attente de migration pour être déplacées vers l’emplacement géographique spécifié.</span><span class="sxs-lookup"><span data-stu-id="81b4a-123">For existing teams, if an administrator adds or modifies the PDL for the Microsoft 365 group that backs a team, that team's channel messaging data is added to a migration queue to be moved to the specified geo location.</span></span>

<span data-ttu-id="81b4a-124">La modification du PDL du groupe de Microsoft 365 place en file d’attente Teams données à migrer vers l’emplacement choisi.</span><span class="sxs-lookup"><span data-stu-id="81b4a-124">Changing the PDL of the Microsoft 365 group queues the Teams data to migrate to the chosen location.</span></span> <span data-ttu-id="81b4a-125">Toutefois, cela ne migre pas le site SharePoint ou les fichiers associés au groupe automatiquement.</span><span class="sxs-lookup"><span data-stu-id="81b4a-125">However, this does not migrate the SharePoint site or files associated with the Group automatically.</span></span> <span data-ttu-id="81b4a-126">Vous devez déplacer le site séparément en suivant les procédures de déplacement [d’un site SharePoint vers un autre emplacement géographique.](/microsoft-365/enterprise/move-sharepoint-between-geo-locations)</span><span class="sxs-lookup"><span data-stu-id="81b4a-126">You must move the site separately by following the procedures in [Move a SharePoint site to a different geo location](/microsoft-365/enterprise/move-sharepoint-between-geo-locations).</span></span> <span data-ttu-id="81b4a-127">N’oubliez pas de suivre les deux étapes pour Teams données et SharePoint données d’un groupe à différents emplacements.</span><span class="sxs-lookup"><span data-stu-id="81b4a-127">Be sure to do both steps to avoid Teams data and SharePoint data for one group in different locations.</span></span>

<span data-ttu-id="81b4a-128">Pour rechercher l’emplacement actuel des données d’une équipe, connectez-vous [à Teams PowerShell](/powershell/module/teams/connect-microsoftteams) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="81b4a-128">To find the current location of a team's data, [connect to Teams PowerShell](/powershell/module/teams/connect-microsoftteams) and run the following command:</span></span>

```PowerShell
Get-MultiGeoRegion -EntityType Group -EntityId <GroupObjectId>
```

## <a name="user-experience"></a><span data-ttu-id="81b4a-129">Expérience de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="81b4a-129">User Experience</span></span>

<span data-ttu-id="81b4a-130">Teams Multi-Géo est transparent pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="81b4a-130">Teams Multi-Geo is seamless to the end user.</span></span> <span data-ttu-id="81b4a-131">Une fois que vous modifiez la PDL d’un utilisateur ou d’un groupe, les données respectives sont en file d’attente pour la migration et la migration se produit automatiquement sans impact sur l’utilisateur ou son client Teams même s’ils sont actifs pendant la migration.</span><span class="sxs-lookup"><span data-stu-id="81b4a-131">Once you change the PDL of a user or a group, the respective data will queue for migration and the migration will occur automatically with no impact to the user or their Teams client even if they are active while the migration occurs.</span></span>

## <a name="see-also"></a><span data-ttu-id="81b4a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81b4a-132">See also</span></span>

[<span data-ttu-id="81b4a-133">Configuration de client multigéographique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="81b4a-133">Microsoft 365 Multi-Geo tenant configuration</span></span>](/microsoft-365/enterprise/multi-geo-tenant-configuration)

[<span data-ttu-id="81b4a-134">Administration d’un environnement multi-géographique</span><span class="sxs-lookup"><span data-stu-id="81b4a-134">Administering a multi-geo environment</span></span>](administering-a-multi-geo-environment.md)

[<span data-ttu-id="81b4a-135">Administration des boîtes aux lettres Exchange Online dans un environnement multi-géographique</span><span class="sxs-lookup"><span data-stu-id="81b4a-135">Administering Exchange Online mailboxes in a multi-geo environment</span></span>](administering-exchange-online-multi-geo.md)
