---
title: Partager des calendriers avec des utilisateurs externes
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: fb00dd4e-2d5f-4e8d-8ff4-94b2cf002bdd
description: 'Découvrez comment permettre à vos utilisateurs de partager leurs calendriers avec des utilisateurs externes pour des réunions et des rendez-vous. '
ms.openlocfilehash: 905280d3c23ffcb9fcf281c39b232a3d05ba1ec5
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44399565"
---
# <a name="share-calendars-with-external-users"></a><span data-ttu-id="7621b-103">Partager des calendriers avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="7621b-103">Share calendars with external users</span></span>

<span data-ttu-id="7621b-104">[] Il est souvent nécessaire de programmer des réunions avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7621b-104">It's often necessary to schedule meetings with people outside your organization.</span></span> <span data-ttu-id="7621b-105">Pour simplifier le processus de recherche des heures d’accord mutuellement acceptables, Microsoft 365 vous permet de mettre des calendriers à disposition des « utilisateurs externes », qui doivent voir les disponibilités, mais pas de comptes d’utilisateur pour votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7621b-105">To simplify the process of finding mutually agreeable meeting times, Microsoft 365 enables you to make calendars available to "external users," those who need to see free/busy time but don't have user accounts for your Microsoft 365 environment.</span></span>
  
<span data-ttu-id="7621b-106">Le partage de calendrier est un paramètre global, ce qui signifie que vous pouvez l’activer pour tous les utilisateurs du client.</span><span class="sxs-lookup"><span data-stu-id="7621b-106">Calendar sharing is a global setting, meaning that you, the admin, can enable it for all users in the tenant.</span></span> <span data-ttu-id="7621b-107">Une fois le partage activé, les utilisateurs peuvent utiliser Outlook Web App pour partager leurs calendriers avec quiconque se trouve à l’intérieur ou à l’extérieur de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="7621b-107">Once sharing is enabled, users can use Outlook Web App to share their calendars with anyone inside or outside the organization.</span></span> <span data-ttu-id="7621b-108">Les utilisateurs au sein de l’organisation peuvent afficher le calendrier partagé côte à côte avec leur propre calendrier.</span><span class="sxs-lookup"><span data-stu-id="7621b-108">People inside the organization can view the shared calendar side-by-side with their own.</span></span> <span data-ttu-id="7621b-109">Les personnes en dehors de l’organisation recevront une URL qu’elles peuvent utiliser pour afficher le calendrier.</span><span class="sxs-lookup"><span data-stu-id="7621b-109">People outside the organization will be sent a URL that they can use to view the calendar.</span></span> <span data-ttu-id="7621b-110">Les utilisateurs décident quand ils doivent partager, combien de partager et quand les calendriers doivent rester privés.</span><span class="sxs-lookup"><span data-stu-id="7621b-110">Users decide when to share, how much to share, and when to keep their calendars private.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7621b-p103">Si vous voulez partager des calendriers avec une organisation qui utilise Exchange Server 2013 (solution locale), l'administrateur Exchange devra configurer une relation d'authentification avec le cloud. Il s'agit de la « fédération ». Celle-ci doit satisfaire une configuration logicielle minimale. Pour plus d'informations, voir [Partage](https://technet.microsoft.com/library/dd638083%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7621b-p103">If you want to share calendars with an organization that uses Exchange Server 2013 (an on-premises solution), the Exchange administrator will need to set up an authentication relationship with the cloud. This is known as "federation" and must meet minimum software requirements. See [Sharing](https://technet.microsoft.com/library/dd638083%28v=exchg.150%29.aspx) for more information.</span></span> 
  
## <a name="enable-calendar-sharing-using-the-microsoft-365-admin-center"></a><span data-ttu-id="7621b-114">Activer le partage de calendrier à l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7621b-114">Enable calendar sharing using the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="7621b-115">Dans le centre d’administration, accédez à **paramètres** \> **org paramètres**.</span><span class="sxs-lookup"><span data-stu-id="7621b-115">In the admin center, go to **Settings** \> **Org Settings**.</span></span> 
    
2. <span data-ttu-id="7621b-116">Dans l’onglet **services** , sélectionnez **calendrier**.</span><span class="sxs-lookup"><span data-stu-id="7621b-116">On the **Services** tab, select **Calendar**.</span></span>
  
3. <span data-ttu-id="7621b-117">Sur la page **calendrier** qui s’ouvre, indiquez si vous souhaitez autoriser vos utilisateurs à partager leurs calendriers avec des personnes extérieures à votre organisation qui disposent de Microsoft 365 ou Exchange.</span><span class="sxs-lookup"><span data-stu-id="7621b-117">On the **Calendar** page that opens, choose whether you want to let your users share their calendars with people outside of your organization who have Microsoft 365 or Exchange.</span></span>
    
4. <span data-ttu-id="7621b-118">Indiquez si vous souhaitez autoriser les utilisateurs anonymes (utilisateurs sans informations d’identification de connexion) à accéder aux calendriers par le biais d’une invitation par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="7621b-118">Choose whether you want to allow anonymous users (users without logon credentials) to access calendars via an email invitation.</span></span>

5. <span data-ttu-id="7621b-119">Choisissez le type d’informations de calendrier à mettre à la disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7621b-119">Choose what type of calendar information to make available to users.</span></span> <span data-ttu-id="7621b-120">Vous pouvez autoriser toutes les informations ou les limiter à des heures ou à des heures seulement ou à des heures, des objets et des emplacements uniquement.</span><span class="sxs-lookup"><span data-stu-id="7621b-120">You can allow all information, or limit it to time only or time, subject, and location only.</span></span>

    
## <a name="invite-people-to-access-calendars"></a><span data-ttu-id="7621b-121">Inviter des personnes à accéder à des calendriers</span><span class="sxs-lookup"><span data-stu-id="7621b-121">Invite people to access calendars</span></span>

<span data-ttu-id="7621b-p105">Une fois le partage activé pour le client, les propriétaires de calendrier peuvent envoyer des invitations à des utilisateurs spécifiques. Pour plus d'informations, voir [Partage de votre calendrier dans Outlook Web App](https://support.office.com/article/7ecef8ae-139c-40d9-bae2-a23977ee58d5.aspx).</span><span class="sxs-lookup"><span data-stu-id="7621b-p105">Once sharing is enabled for the tenant, calendar owners can extend invitations to specific users. See [Sharing your calendar in Outlook Web App](https://support.office.com/article/7ecef8ae-139c-40d9-bae2-a23977ee58d5.aspx) for instructions.</span></span> 
  
