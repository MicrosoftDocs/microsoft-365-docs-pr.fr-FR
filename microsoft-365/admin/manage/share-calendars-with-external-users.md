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
description: Découvrez comment laisser vos utilisateurs partager leurs calendriers avec des utilisateurs externes pour les réunions et les rendez-vous.
ms.openlocfilehash: 5fc80965ae277e66dfbf73de80618dec03d26759
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50915049"
---
# <a name="share-calendars-with-external-users"></a><span data-ttu-id="21072-103">Partager des calendriers avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="21072-103">Share calendars with external users</span></span>

<span data-ttu-id="21072-104">Il est parfois nécessaire pour vos utilisateurs de planifier des réunions avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="21072-104">It's sometimes necessary for your users to schedule meetings with people outside your organization.</span></span> <span data-ttu-id="21072-105">Pour simplifier le processus de recherche des heures de réunion courantes, Microsoft 365 vous permet de mettre les calendriers à la disposition de ces personnes.</span><span class="sxs-lookup"><span data-stu-id="21072-105">To simplify the process of finding common meeting times, Microsoft 365 enables you to make calendars available to these people.</span></span> <span data-ttu-id="21072-106">Ce sont des personnes qui ont besoin de voir les heures de libre et de occupé pour les utilisateurs de votre organisation, mais qui n’ont pas de comptes d’utilisateur pour votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="21072-106">These are people who need to see free and busy times for users in your organization, but don't have user accounts for your Microsoft 365 organization.</span></span>

<span data-ttu-id="21072-107">Vous pouvez activer le partage de calendrier pour tous les utilisateurs de votre organisation dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="21072-107">You can enable calendar sharing for all users in your organization in the Microsoft 365 admin center.</span></span> <span data-ttu-id="21072-108">Une fois le partage activé, vos utilisateurs peuvent utiliser Outlook Web App pour partager leurs calendriers avec toute personne à l’intérieur ou à l’extérieur de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="21072-108">Once sharing is enabled, your users can use Outlook Web App to share their calendars with anyone inside or outside the organization.</span></span> <span data-ttu-id="21072-109">Les membres de l’organisation peuvent afficher le calendrier partagé avec leur propre calendrier.</span><span class="sxs-lookup"><span data-stu-id="21072-109">People inside the organization can view the shared calendar along with their own calendar.</span></span> <span data-ttu-id="21072-110">Les personnes extérieures à l’organisation seront envoyées à une URL qu’elles pourront utiliser pour afficher le calendrier.</span><span class="sxs-lookup"><span data-stu-id="21072-110">People outside the organization will be sent a URL that they can use to view the calendar.</span></span> <span data-ttu-id="21072-111">Les utilisateurs de votre organisation décident quand partager et combien partager.</span><span class="sxs-lookup"><span data-stu-id="21072-111">Users in your organization decide when to share and how much to share.</span></span>

> [!NOTE]
> <span data-ttu-id="21072-112">Si vous souhaitez partager des calendriers avec une organisation qui utilise Exchange Server 2013 (une solution sur site), l’administrateur Exchange devra configurer une relation d’authentification avec le cloud.</span><span class="sxs-lookup"><span data-stu-id="21072-112">If you want to share calendars with an organization that uses Exchange Server 2013 (an on-premises solution), the Exchange administrator will need to set up an authentication relationship with the cloud.</span></span> <span data-ttu-id="21072-113">C’est ce que l’on appelle la fédération et doit satisfaire la exigences logicielle minimale.</span><span class="sxs-lookup"><span data-stu-id="21072-113">This is known as federation, and must meet minimum software requirements.</span></span> <span data-ttu-id="21072-114">Pour [plus d’informations,](/exchange/sharing-exchange-2013-help) voir Partage.</span><span class="sxs-lookup"><span data-stu-id="21072-114">See [Sharing](/exchange/sharing-exchange-2013-help) for more information.</span></span>
  
## <a name="enable-calendar-sharing-using-the-microsoft-365-admin-center"></a><span data-ttu-id="21072-115">Activer le partage de calendrier à l’aide du Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="21072-115">Enable calendar sharing using the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="21072-116">Dans le centre d’administration, allez aux **paramètres de** \> **l’organisation Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="21072-116">In the admin center, go to **Settings** \> **Org Settings**.</span></span>

2. <span data-ttu-id="21072-117">Sous **l’onglet Services,** sélectionnez **Calendrier.**</span><span class="sxs-lookup"><span data-stu-id="21072-117">On the **Services** tab, select **Calendar**.</span></span>
  
3. <span data-ttu-id="21072-118">Dans **la** page Calendrier, choisissez si vous souhaitez laisser les utilisateurs partager leurs calendriers avec des personnes extérieures à votre organisation qui ont Microsoft 365 ou Exchange.</span><span class="sxs-lookup"><span data-stu-id="21072-118">On the **Calendar** page, choose whether you want to let users share their calendars with people outside of your organization who have Microsoft 365 or Exchange.</span></span> <span data-ttu-id="21072-119">Choisissez si vous souhaitez autoriser les utilisateurs anonymes (utilisateurs sans informations d’identification) à accéder aux calendriers via une invitation par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="21072-119">Choose whether you want to allow anonymous users (users without credentials) to access calendars via an email invitation.</span></span>

4. <span data-ttu-id="21072-120">Choisissez le type d’informations de calendrier à mettre à la disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="21072-120">Choose what type of calendar information to make available to users.</span></span> <span data-ttu-id="21072-121">Vous pouvez autoriser toutes les informations ou les limiter uniquement à l’heure, à l’objet et à l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="21072-121">You can allow all information, or limit it to time only or time, subject, and location only.</span></span>

## <a name="invite-people-to-access-calendars"></a><span data-ttu-id="21072-122">Inviter des personnes à accéder à des calendriers</span><span class="sxs-lookup"><span data-stu-id="21072-122">Invite people to access calendars</span></span>

<span data-ttu-id="21072-123">Une fois le partage activé, les propriétaires de calendrier peuvent étendre les invitations à des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="21072-123">Once sharing is enabled, calendar owners can extend invitations to specific users.</span></span> <span data-ttu-id="21072-124">Pour plus d'informations, voir [Partage de votre calendrier dans Outlook Web App](https://support.microsoft.com/office/7ecef8ae-139c-40d9-bae2-a23977ee58d5).</span><span class="sxs-lookup"><span data-stu-id="21072-124">See [Sharing your calendar in Outlook Web App](https://support.microsoft.com/office/7ecef8ae-139c-40d9-bae2-a23977ee58d5) for instructions.</span></span>