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
description: Activez le partage de calendriers dans Microsoft 365 centre d’administration pour que les utilisateurs peuvent partager leurs calendriers avec toute personne à l’intérieur ou à l’extérieur de l’organisation.
ms.openlocfilehash: 6f4c215403e16ac6658619e50e6115606f106397
ms.sourcegitcommit: 9541d5e6720a06327dc785e3ad7e8fb11246fd72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2021
ms.locfileid: "52582715"
---
# <a name="share-calendars-with-external-users"></a><span data-ttu-id="f8fa9-103">Partager des calendriers avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="f8fa9-103">Share calendars with external users</span></span>

<span data-ttu-id="f8fa9-104">Il est parfois nécessaire pour vos utilisateurs de planifier des réunions avec des personnes extérieures à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-104">It's sometimes necessary for your users to schedule meetings with people outside your organization.</span></span> <span data-ttu-id="f8fa9-105">Pour simplifier le processus de recherche des heures de réunion courantes, Microsoft 365 vous permet de mettre les calendriers à la disposition de ces personnes.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-105">To simplify the process of finding common meeting times, Microsoft 365 enables you to make calendars available to these people.</span></span> <span data-ttu-id="f8fa9-106">Ce sont des personnes qui ont besoin de consulter les heures de libre et de occupé pour les utilisateurs de votre organisation, mais qui n’ont pas de comptes d’utilisateur pour Microsoft 365 organisation.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-106">These are people who need to see free and busy times for users in your organization, but don't have user accounts for your Microsoft 365 organization.</span></span>

<span data-ttu-id="f8fa9-107">Vous pouvez activer le partage de calendrier pour tous les utilisateurs de votre organisation dans le centre Microsoft 365'administration.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-107">You can enable calendar sharing for all users in your organization in the Microsoft 365 admin center.</span></span> <span data-ttu-id="f8fa9-108">Une fois le partage activé, vos utilisateurs peuvent utiliser Outlook Web App pour partager leurs calendriers avec toute personne à l’intérieur ou à l’extérieur de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-108">Once sharing is enabled, your users can use Outlook Web App to share their calendars with anyone inside or outside the organization.</span></span> <span data-ttu-id="f8fa9-109">Les membres de l’organisation peuvent afficher le calendrier partagé avec leur propre calendrier.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-109">People inside the organization can view the shared calendar along with their own calendar.</span></span> <span data-ttu-id="f8fa9-110">Les personnes extérieures à l’organisation seront envoyées à une URL qu’elles pourront utiliser pour afficher le calendrier.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-110">People outside the organization will be sent a URL that they can use to view the calendar.</span></span> <span data-ttu-id="f8fa9-111">Les utilisateurs de votre organisation décident quand partager et combien partager.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-111">Users in your organization decide when to share and how much to share.</span></span>

> [!NOTE]
> <span data-ttu-id="f8fa9-112">Si vous souhaitez partager des calendriers avec une organisation qui utilise Exchange Server 2013 (une solution sur site), l’administrateur Exchange devra configurer une relation d’authentification avec le cloud.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-112">If you want to share calendars with an organization that uses Exchange Server 2013 (an on-premises solution), the Exchange administrator will need to set up an authentication relationship with the cloud.</span></span> <span data-ttu-id="f8fa9-113">C’est ce que l’on appelle la fédération et doit satisfaire la exigences logicielle minimale.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-113">This is known as federation, and must meet minimum software requirements.</span></span> <span data-ttu-id="f8fa9-114">Pour plus [d’informations,](/exchange/sharing-exchange-2013-help) voir Partage.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-114">See [Sharing](/exchange/sharing-exchange-2013-help) for more information.</span></span>
  
## <a name="enable-calendar-sharing-using-the-microsoft-365-admin-center"></a><span data-ttu-id="f8fa9-115">Activer le partage de calendrier à l’aide Microsoft 365'administration centrale</span><span class="sxs-lookup"><span data-stu-id="f8fa9-115">Enable calendar sharing using the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="f8fa9-116">Dans le Centre d’administration, Paramètres  \> **Org Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-116">In the admin center, go to **Settings** \> **Org Settings**.</span></span>

2. <span data-ttu-id="f8fa9-117">Sous **l’onglet Services,** sélectionnez **Calendrier.**</span><span class="sxs-lookup"><span data-stu-id="f8fa9-117">On the **Services** tab, select **Calendar**.</span></span>
  
3. <span data-ttu-id="f8fa9-118">Dans **la** page Calendrier, choisissez si vous souhaitez laisser les utilisateurs partager leurs calendriers avec des personnes extérieures à votre organisation qui ont des Microsoft 365 ou Exchange.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-118">On the **Calendar** page, choose whether you want to let users share their calendars with people outside of your organization who have Microsoft 365 or Exchange.</span></span> <span data-ttu-id="f8fa9-119">Choisissez si vous souhaitez autoriser les utilisateurs anonymes (utilisateurs sans informations d’identification) à accéder aux calendriers via une invitation par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-119">Choose whether you want to allow anonymous users (users without credentials) to access calendars via an email invitation.</span></span>

4. <span data-ttu-id="f8fa9-120">Choisissez le type d’informations de calendrier à mettre à la disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-120">Choose what type of calendar information to make available to users.</span></span> <span data-ttu-id="f8fa9-121">Vous pouvez autoriser toutes les informations ou les limiter uniquement à l’heure, à l’objet et à l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-121">You can allow all information, or limit it to time only or time, subject, and location only.</span></span>

## <a name="invite-people-to-access-calendars"></a><span data-ttu-id="f8fa9-122">Inviter des personnes à accéder à des calendriers</span><span class="sxs-lookup"><span data-stu-id="f8fa9-122">Invite people to access calendars</span></span>

<span data-ttu-id="f8fa9-123">Une fois le partage activé, les propriétaires de calendrier peuvent étendre les invitations à des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-123">Once sharing is enabled, calendar owners can extend invitations to specific users.</span></span> <span data-ttu-id="f8fa9-124">Pour plus d'informations, voir [Partage de votre calendrier dans Outlook Web App](https://support.microsoft.com/office/7ecef8ae-139c-40d9-bae2-a23977ee58d5).</span><span class="sxs-lookup"><span data-stu-id="f8fa9-124">See [Sharing your calendar in Outlook Web App](https://support.microsoft.com/office/7ecef8ae-139c-40d9-bae2-a23977ee58d5) for instructions.</span></span>

## <a name="related-content"></a><span data-ttu-id="f8fa9-125">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="f8fa9-125">Related content</span></span>

<span data-ttu-id="f8fa9-126">[Activer ou désactiver le partage externe pour un site](/sharepoint/change-external-sharing-site) (article)</span><span class="sxs-lookup"><span data-stu-id="f8fa9-126">[Turn external sharing on or off for a site](/sharepoint/change-external-sharing-site) (article)</span></span>

<span data-ttu-id="f8fa9-127">[Vue d’ensemble du centre d’administration Microsoft 365](../../business-video/admin-center-overview.md) (vidéo)</span><span class="sxs-lookup"><span data-stu-id="f8fa9-127">[Overview of the Microsoft 365 admin center](../../business-video/admin-center-overview.md) (video)</span></span>

<span data-ttu-id="f8fa9-128">[Gérer les courriers électroniques et les calendriers](../email/index.yml) (page de liens)</span><span class="sxs-lookup"><span data-stu-id="f8fa9-128">[Manage email and calendars](../email/index.yml) (link page)</span></span>