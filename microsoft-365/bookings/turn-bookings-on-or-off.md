---
title: Activer ou désactiver les réservations Microsoft
ms.author: kwekua
author: kwekuako
manager: scotv
audience: Admin
ms.topic: article
ms.service: bookings
localization_priority: Normal
ms.assetid: 5382dc07-aaa5-45c9-8767-502333b214ce
description: Découvrez comment accéder à Microsoft bookings dans Microsoft 365.
ms.openlocfilehash: 815aa3a859db15364aa18d3550001a28d085b711
ms.sourcegitcommit: 41fd71ec7175ea3b94f5d3ea1ae2c8fb8dc84227
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "47419547"
---
# <a name="turn-microsoft-bookings-on-or-off"></a><span data-ttu-id="dee13-103">Activer ou désactiver les réservations Microsoft</span><span class="sxs-lookup"><span data-stu-id="dee13-103">Turn Microsoft Bookings on or off</span></span>

<span data-ttu-id="dee13-104">Les réservations peuvent être activées ou désactivées pour l’ensemble de votre organisation ou pour des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="dee13-104">Bookings can be turned on or off for your entire organization or for specific users.</span></span> <span data-ttu-id="dee13-105">Lorsque vous activez les réservations pour les utilisateurs, ils peuvent créer une page livres, créer un calendrier et autoriser d’autres personnes à réserver des heures.</span><span class="sxs-lookup"><span data-stu-id="dee13-105">When you turn on Bookings for users, they can create a Bookings page, create a calendar, and allow other people to book time with them.</span></span>

> [!NOTE]
> <span data-ttu-id="dee13-106">Les contrôles d’administration décrits dans ces sections ne sont pas disponibles pour les clients Office 365 gérés par 21Vianet (Chine).</span><span class="sxs-lookup"><span data-stu-id="dee13-106">The admin controls described in these sections are not available for Office 365 Operated by 21Vianet (China) customers.</span></span>

## <a name="turn-bookings-on-or-off-for-your-organization-using-the-microsoft-365-admin-center"></a><span data-ttu-id="dee13-107">Activer ou désactiver les réservations pour votre organisation à l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="dee13-107">Turn Bookings on or off for your organization using the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="dee13-108">Connectez-vous au centre d’administration Microsoft 365 en tant qu’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="dee13-108">Sign in to the Microsoft 365 admin center as a global admin.</span></span>

2. <span data-ttu-id="dee13-109">Dans le centre d’administration, accédez **à paramètres paramètres**   \> **Settings** et sélectionnez **réservations**.</span><span class="sxs-lookup"><span data-stu-id="dee13-109">In the admin center, go to **Settings** \> **Settings** and select **Bookings**.</span></span>

3. <span data-ttu-id="dee13-110">Activez cette case à cocher pour **permettre à votre organisation d’utiliser des réservations** d’activation ou de désactivation des réservations pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dee13-110">Select the checkbox for **Allow your organization to use Bookings** to enable or disable Bookings for your organization.</span></span>

   > [!NOTE]
   > <span data-ttu-id="dee13-111">La désactivation des réservations désactive tout accès au service, y compris la création et la gestion des pages de livres.</span><span class="sxs-lookup"><span data-stu-id="dee13-111">Turning off Bookings will disable all access to the service including creation and management of Bookings pages.</span></span>

4. <span data-ttu-id="dee13-112">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="dee13-112">Select **Save Changes**.</span></span>

## <a name="turn-bookings-on-or-off-for-your-organization-using-powershell"></a><span data-ttu-id="dee13-113">Activer ou désactiver les réservations pour votre organisation à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="dee13-113">Turn Bookings on or off for your organization using PowerShell</span></span>

<span data-ttu-id="dee13-114">Pour activer ou désactiver les réservations de votre organisation à l’aide de la cmdlet PowerShell [Set-OrganizationConfig](https://docs.microsoft.com/powershell/module/exchange/set-organizationconfig), [Connectez-vous à Exchange Online PowerShell]() et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="dee13-114">To turn Bookings on or off for your organization using the PowerShell cmdlet [Set-OrganizationConfig](https://docs.microsoft.com/powershell/module/exchange/set-organizationconfig), [Connect to Exchange Online PowerShell]() and run the following command:</span></span>

```PowerShell
   Set-OrganizationConfig -BookingsEnabled $false
```

### <a name="turn-bookings-on-or-off-for-individual-users"></a><span data-ttu-id="dee13-115">Activer ou désactiver les réservations pour des utilisateurs individuels</span><span class="sxs-lookup"><span data-stu-id="dee13-115">Turn Bookings on or off for individual users</span></span>

<span data-ttu-id="dee13-116">Vous pouvez désactiver les réservations pour des utilisateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="dee13-116">You can disable Bookings for individual users.</span></span>

1. <span data-ttu-id="dee13-117">Accédez au centre d’administration Microsoft 365, **puis sélectionnez utilisateurs** \> **actifs**.</span><span class="sxs-lookup"><span data-stu-id="dee13-117">Go to the Microsoft 365 admin center, then select **Users** \> **Active users**.</span></span>

1. <span data-ttu-id="dee13-118">Sélectionnez l’utilisateur de votre choix, puis sélectionnez **licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="dee13-118">Select the desired user, then select **Licenses and Apps**.</span></span>

1. <span data-ttu-id="dee13-119">Développez **applications** et désactivez la case à cocher Microsoft bookings.</span><span class="sxs-lookup"><span data-stu-id="dee13-119">Expand **Apps** and clear the checkbox for Microsoft Bookings.</span></span>

## <a name="require-staff-approvals-before-sharing-freebusy-information"></a><span data-ttu-id="dee13-120">Exiger l’approbation du personnel avant de partager les informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="dee13-120">Require staff approvals before sharing free/busy information</span></span>

<span data-ttu-id="dee13-121">Les administrateurs peuvent demander aux employés de leur organisation de s’abonner avant que leurs informations de disponibilité soient partagées via les réservations et qu’ils puissent être réservables via une page de réservation.</span><span class="sxs-lookup"><span data-stu-id="dee13-121">Admins can require employees in their organization to opt-in before their availability information is shared through Bookings and before they can be bookable through a booking page.</span></span> <span data-ttu-id="dee13-122">Ce paramètre est disponible dans le centre d’administration Microsoft 365 **sous** \> books **Settings** \> **bookings**.</span><span class="sxs-lookup"><span data-stu-id="dee13-122">This setting is available in the Microsoft 365 admin center under **Settings** \> **Settings** \> **Bookings**.</span></span>

<span data-ttu-id="dee13-123">Lorsque ce paramètre est activé, les employés ajoutés en tant que personnel dans les calendriers de réservation trouveront un lien approbation/rejet dans la notification par e-mail qu’ils reçoivent.</span><span class="sxs-lookup"><span data-stu-id="dee13-123">When this setting is enabled, employees added as staff in booking calendars will find an Approve/Reject link in the email notification they receive.</span></span>

<span data-ttu-id="dee13-124">Cette fonctionnalité est progressivement déployée dans le monde entier pour les clients Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="dee13-124">This feature is gradually rolling out world wide to Microsoft 365 customers.</span></span> <span data-ttu-id="dee13-125">Si vous ne voyez pas cette option dans le centre d’administration 365 de Microsoft, consultez-la prochainement.</span><span class="sxs-lookup"><span data-stu-id="dee13-125">If you don't see this option in the Microsoft 365 admin center, check back soon.</span></span>

## <a name="block-social-sharing-options"></a><span data-ttu-id="dee13-126">Bloquer les options de partage social</span><span class="sxs-lookup"><span data-stu-id="dee13-126">Block social sharing options</span></span>

<span data-ttu-id="dee13-127">Les administrateurs peuvent contrôler la manière dont les pages de réservation sont partagées sur des réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="dee13-127">Admins can control how booking pages are shared on social networks.</span></span> <span data-ttu-id="dee13-128">Ce paramètre est disponible dans le centre d’administration Microsoft 365 **sous** \> books **Settings** \> **bookings**.</span><span class="sxs-lookup"><span data-stu-id="dee13-128">This setting is available in the Microsoft 365 admin center under **Settings** \> **Settings** \> **Bookings**.</span></span>

<span data-ttu-id="dee13-129">Cette fonctionnalité est progressivement déployée dans le monde entier pour les clients Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="dee13-129">This feature is gradually rolling out world wide to Microsoft 365 customers.</span></span> <span data-ttu-id="dee13-130">Si vous ne voyez pas cette option dans le centre d’administration 365 de Microsoft, consultez-la prochainement.</span><span class="sxs-lookup"><span data-stu-id="dee13-130">If you don't see this option in the Microsoft 365 admin center, check back soon.</span></span>

## <a name="allow-only-selected-users-to-create-bookings-calendars"></a><span data-ttu-id="dee13-131">Autoriser uniquement les utilisateurs sélectionnés à créer des calendriers de livres</span><span class="sxs-lookup"><span data-stu-id="dee13-131">Allow only selected users to create Bookings calendars</span></span>

<span data-ttu-id="dee13-132">À l’aide de restrictions de stratégie, vous pouvez limiter les utilisateurs titulaires d’une licence à la possibilité de créer des calendriers de livres.</span><span class="sxs-lookup"><span data-stu-id="dee13-132">By using policy restrictions, you can restrict licensed users from being able to create Bookings calendars.</span></span> <span data-ttu-id="dee13-133">Vous devez d’abord activer les réservations pour l’ensemble de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dee13-133">You must first enable Bookings for your entire organization.</span></span> <span data-ttu-id="dee13-134">Tous les utilisateurs de votre organisation auront des licences de livres, mais seules celles incluses dans la stratégie peuvent créer des calendriers de livrets et disposer d’un contrôle total sur qui peut accéder aux calendriers qu’ils créent.</span><span class="sxs-lookup"><span data-stu-id="dee13-134">All users in you organization will have Bookings licenses, but only those included in the policy can create Bookings calendars and have full control over who can access the calendars they create.</span></span>

<span data-ttu-id="dee13-135">Les utilisateurs inclus dans cette stratégie peuvent créer des calendriers de réservations et être ajoutés en tant que personnel de n’importe quelle capacité (y compris le rôle d’administrateur) à des calendriers de réservations existants.</span><span class="sxs-lookup"><span data-stu-id="dee13-135">Users who are included in this policy can create new Bookings calendars and can be added as staff in any capacity (including the administrator role) to existing Bookings calendars.</span></span> <span data-ttu-id="dee13-136">Les utilisateurs qui ne sont pas inclus dans cette stratégie ne pourront pas créer de nouveaux calendriers de livres comptables et recevront un message d’erreur s’ils essaient de le faire.</span><span class="sxs-lookup"><span data-stu-id="dee13-136">Users who aren't included in this policy won't be able to create new Bookings calendars and will receive an error message if they try to do so.</span></span>

<span data-ttu-id="dee13-137">Vous devrez exécuter les commandes suivantes à l’aide d’Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dee13-137">You'll need to run the following commands using Exchange Online PowerShell.</span></span> <span data-ttu-id="dee13-138">Pour plus d’informations sur l’exécution des cmdlets Exchange Online, consultez la rubrique [connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="dee13-138">For more information on running Exchange Online cmdlets, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dee13-139">Les étapes ci-dessous supposent qu’aucune autre stratégie de boîte aux lettres Outlook Web App (OWA) n’ait été créée dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dee13-139">The steps below assume that no other Outlook Web App (OWA) mailbox policies have been created in your organization.</span></span>

1. <span data-ttu-id="dee13-140">Créez une stratégie de boîte aux lettres pour les utilisateurs qui doivent être autorisés à créer des calendriers de livres.</span><span class="sxs-lookup"><span data-stu-id="dee13-140">Create a new mailbox policy for users that should be allowed to create Bookings calendars.</span></span> <span data-ttu-id="dee13-141">(La création de calendrier livres est autorisée par défaut par de nouvelles stratégies de boîte aux lettres.)</span><span class="sxs-lookup"><span data-stu-id="dee13-141">(Bookings calendar creation is allowed by default by new mailbox policies.)</span></span>

   ```PowerShell
   New-OwaMailboxPolicy -Name "BookingsCreators"
   ```

   <span data-ttu-id="dee13-142">Pour plus d’informations, consultez la rubrique [New-OWAMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/new-owamailboxpolicy).</span><span class="sxs-lookup"><span data-stu-id="dee13-142">For more information, see [New-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/new-owamailboxpolicy).</span></span>

2. <span data-ttu-id="dee13-143">Affectez cette stratégie aux utilisateurs concernés en exécutant cette commande pour chaque utilisateur auquel vous souhaitez accorder l’autorisation de créer des calendriers de livres.</span><span class="sxs-lookup"><span data-stu-id="dee13-143">Assign this policy to the relevant users by running this command for each user you want to grant permission to create Bookings calendars.</span></span>

   ```PowerShell
   Set-CASMailbox -Identity <someCreator@emailaddress> -OwaMailboxPolicy "BookingsCreators"
   ```

   <span data-ttu-id="dee13-144">Pour plus d'informations, consultez la rubrique [Set-CASMailbox](https://docs.microsoft.com/powershell/module/exchange/set-casmailbox).</span><span class="sxs-lookup"><span data-stu-id="dee13-144">For more information, see [Set-CASMailbox](https://docs.microsoft.com/powershell/module/exchange/set-casmailbox).</span></span>

3. <span data-ttu-id="dee13-145">Facultatif : exécutez cette commande si vous souhaitez désactiver les réservations pour tous les autres utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dee13-145">Optional: Run this command if you want to disable Bookings for all other users in your organization.</span></span>

   ```PowerShell
   Set-OwaMailboxPolicy "OwaMailboxPolicy-Default" -BookingsMailboxCreationEnabled:$false
   ```

   <span data-ttu-id="dee13-146">Pour plus d'informations, voir [Set-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/set-owamailboxpolicy).</span><span class="sxs-lookup"><span data-stu-id="dee13-146">For more information, see [Set-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/set-owamailboxpolicy).</span></span>

<span data-ttu-id="dee13-147">Pour plus d’informations sur les stratégies de boîte aux lettres OWA, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="dee13-147">For more information on OWA mailbox policies, check out the following topics:</span></span>

- [<span data-ttu-id="dee13-148">Créer une stratégie de boîte aux lettres Outlook sur le Web dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="dee13-148">Create an Outlook on the web mailbox policy in Exchange Online</span></span>](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/create-outlook-web-app-mailbox-policy)

- [<span data-ttu-id="dee13-149">Appliquer ou supprimer une stratégie de boîte aux lettres Outlook sur le Web sur une boîte aux lettres dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="dee13-149">Apply or remove an Outlook on the web mailbox policy on a mailbox in Exchange Online</span></span>](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/create-outlook-web-app-mailbox-policy)