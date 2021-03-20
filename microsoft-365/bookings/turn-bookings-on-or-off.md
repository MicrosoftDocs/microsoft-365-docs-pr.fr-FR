---
title: Activer ou désactiver Microsoft bookings
ms.author: kwekua
author: kwekuako
manager: scotv
audience: Admin
ms.topic: article
ms.service: bookings
localization_priority: Normal
ms.assetid: 5382dc07-aaa5-45c9-8767-502333b214ce
description: Découvrez comment accéder à Microsoft Bookings dans Microsoft 365.
ms.openlocfilehash: 7b1582a480ac4fdcd5a131febcc59450aa13e299
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50913765"
---
# <a name="turn-microsoft-bookings-on-or-off"></a><span data-ttu-id="76334-103">Activer ou désactiver Microsoft bookings</span><span class="sxs-lookup"><span data-stu-id="76334-103">Turn Microsoft Bookings on or off</span></span>

<span data-ttu-id="76334-104">Les réservations peuvent être désactivées pour l’ensemble de votre organisation ou pour des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="76334-104">Bookings can be turned on or off for your entire organization or for specific users.</span></span> <span data-ttu-id="76334-105">Lorsque vous allumez Bookings pour les utilisateurs, ils peuvent créer une page Bookings, créer un calendrier et autoriser d’autres personnes à réserver du temps avec eux.</span><span class="sxs-lookup"><span data-stu-id="76334-105">When you turn on Bookings for users, they can create a Bookings page, create a calendar, and allow other people to book time with them.</span></span>

> [!NOTE]
> <span data-ttu-id="76334-106">Les contrôles d’administration décrits dans ces sections ne sont pas disponibles pour les clients Office 365 géré par 21Vianet (Chine).</span><span class="sxs-lookup"><span data-stu-id="76334-106">The admin controls described in these sections are not available for Office 365 Operated by 21Vianet (China) customers.</span></span>

## <a name="turn-bookings-on-or-off-for-your-organization-using-the-microsoft-365-admin-center"></a><span data-ttu-id="76334-107">Activer ou désactiver bookings pour votre organisation à l’aide du Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="76334-107">Turn Bookings on or off for your organization using the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="76334-108">Connectez-vous au Centre d’administration Microsoft 365 en tant qu’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="76334-108">Sign in to the Microsoft 365 admin center as a global admin.</span></span>

2. <span data-ttu-id="76334-109">Dans le centre d’administration, sélectionnez  \*\*\*\*   \> **Paramètres de** l’organisation paramètres et **sélectionnez Réservations.**</span><span class="sxs-lookup"><span data-stu-id="76334-109">In the admin center, go to  **Settings** \> **Org Settings** and select **Bookings**.</span></span>

3. <span data-ttu-id="76334-110">Activez la case à **cocher autoriser votre organisation** à utiliser Bookings pour activer ou désactiver Bookings pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76334-110">Select the checkbox for **Allow your organization to use Bookings** to enable or disable Bookings for your organization.</span></span>

   > [!NOTE]
   > <span data-ttu-id="76334-111">La désactivation de Bookings désactive tout accès au service, y compris la création et la gestion des pages Bookings.</span><span class="sxs-lookup"><span data-stu-id="76334-111">Turning off Bookings will disable all access to the service including creation and management of Bookings pages.</span></span>

4. <span data-ttu-id="76334-112">Sélectionnez **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="76334-112">Select **Save Changes**.</span></span>

## <a name="turn-bookings-on-or-off-for-your-organization-using-powershell"></a><span data-ttu-id="76334-113">Activer ou désactiver bookings pour votre organisation à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="76334-113">Turn Bookings on or off for your organization using PowerShell</span></span>

<span data-ttu-id="76334-114">Pour activer ou désactiver Bookings pour votre organisation à l’aide de la cmdlet PowerShell [Set-OrganizationConfig, connectez-vous](/powershell/module/exchange/set-organizationconfig)à [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="76334-114">To turn Bookings on or off for your organization using the PowerShell cmdlet [Set-OrganizationConfig](/powershell/module/exchange/set-organizationconfig), [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) and run the following command:</span></span>

```PowerShell
   Set-OrganizationConfig -BookingsEnabled $false
```

### <a name="turn-bookings-on-or-off-for-individual-users"></a><span data-ttu-id="76334-115">Activer ou désactiver les réservations pour des utilisateurs individuels</span><span class="sxs-lookup"><span data-stu-id="76334-115">Turn Bookings on or off for individual users</span></span>

<span data-ttu-id="76334-116">Vous pouvez désactiver les réservations pour des utilisateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="76334-116">You can disable Bookings for individual users.</span></span>

1. <span data-ttu-id="76334-117">Go to the Microsoft 365 admin center, then select **Users** \> **Active users**.</span><span class="sxs-lookup"><span data-stu-id="76334-117">Go to the Microsoft 365 admin center, then select **Users** \> **Active users**.</span></span>

1. <span data-ttu-id="76334-118">Sélectionnez l’utilisateur souhaité, puis **sélectionnez Licences et applications.**</span><span class="sxs-lookup"><span data-stu-id="76334-118">Select the desired user, then select **Licenses and Apps**.</span></span>

1. <span data-ttu-id="76334-119">Développez **Applications** et cochez la case pour Microsoft Bookings.</span><span class="sxs-lookup"><span data-stu-id="76334-119">Expand **Apps** and clear the checkbox for Microsoft Bookings.</span></span>

## <a name="require-staff-approvals-before-sharing-freebusy-information"></a><span data-ttu-id="76334-120">Exiger l’approbation du personnel avant de partager des informations de libre/occupé</span><span class="sxs-lookup"><span data-stu-id="76334-120">Require staff approvals before sharing free/busy information</span></span>

<span data-ttu-id="76334-121">Les administrateurs peuvent demander aux employés de leur organisation de s’y rendre avant que leurs informations de disponibilité soient partagées par le biais de Bookings et avant qu’ils ne soient bookables via une page de réservation.</span><span class="sxs-lookup"><span data-stu-id="76334-121">Admins can require employees in their organization to opt-in before their availability information is shared through Bookings and before they can be bookable through a booking page.</span></span> <span data-ttu-id="76334-122">Ce paramètre est disponible dans le Centre  d’administration Microsoft 365 sous \> **Paramètres Paramètres** \> **Réservations.**</span><span class="sxs-lookup"><span data-stu-id="76334-122">This setting is available in the Microsoft 365 admin center under **Settings** \> **Settings** \> **Bookings**.</span></span>

<span data-ttu-id="76334-123">Lorsque ce paramètre est activé, les employés ajoutés en tant que membres du personnel dans les calendriers de réservation trouveront un lien Approuver/Rejeter dans la notification par courrier électronique qu’ils reçoivent.</span><span class="sxs-lookup"><span data-stu-id="76334-123">When this setting is enabled, employees added as staff in booking calendars will find an Approve/Reject link in the email notification they receive.</span></span>

<span data-ttu-id="76334-124">Cette fonctionnalité est progressivement étendue aux clients Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="76334-124">This feature is gradually rolling out world wide to Microsoft 365 customers.</span></span> <span data-ttu-id="76334-125">Si cette option n’est pas disponible dans le Centre d’administration Microsoft 365, consultez-la prochainement.</span><span class="sxs-lookup"><span data-stu-id="76334-125">If you don't see this option in the Microsoft 365 admin center, check back soon.</span></span>

## <a name="block-social-sharing-options"></a><span data-ttu-id="76334-126">Bloquer les options de partage social</span><span class="sxs-lookup"><span data-stu-id="76334-126">Block social sharing options</span></span>

<span data-ttu-id="76334-127">Les administrateurs peuvent contrôler la façon dont les pages de réservation sont partagées sur les réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="76334-127">Admins can control how booking pages are shared on social networks.</span></span> <span data-ttu-id="76334-128">Ce paramètre est disponible dans le Centre  d’administration Microsoft 365 sous \> **Paramètres Paramètres** \> **Réservations.**</span><span class="sxs-lookup"><span data-stu-id="76334-128">This setting is available in the Microsoft 365 admin center under **Settings** \> **Settings** \> **Bookings**.</span></span>

<span data-ttu-id="76334-129">Cette fonctionnalité est progressivement étendue aux clients Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="76334-129">This feature is gradually rolling out world wide to Microsoft 365 customers.</span></span> <span data-ttu-id="76334-130">Si cette option n’est pas disponible dans le Centre d’administration Microsoft 365, consultez-la prochainement.</span><span class="sxs-lookup"><span data-stu-id="76334-130">If you don't see this option in the Microsoft 365 admin center, check back soon.</span></span>

## <a name="allow-only-selected-users-to-create-bookings-calendars"></a><span data-ttu-id="76334-131">Autoriser uniquement les utilisateurs sélectionnés à créer des calendriers Bookings</span><span class="sxs-lookup"><span data-stu-id="76334-131">Allow only selected users to create Bookings calendars</span></span>

<span data-ttu-id="76334-132">En utilisant des restrictions de stratégie, vous pouvez empêcher les utilisateurs titulaires d’une licence de créer des calendriers Bookings.</span><span class="sxs-lookup"><span data-stu-id="76334-132">By using policy restrictions, you can restrict licensed users from being able to create Bookings calendars.</span></span> <span data-ttu-id="76334-133">Vous devez d’abord activer Bookings pour l’ensemble de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76334-133">You must first enable Bookings for your entire organization.</span></span> <span data-ttu-id="76334-134">Tous les utilisateurs de votre organisation auront des licences Bookings, mais seuls ceux inclus dans la stratégie peuvent créer des calendriers Bookings et avoir un contrôle total sur les personnes autorisées à accéder aux calendriers qu’ils créent.</span><span class="sxs-lookup"><span data-stu-id="76334-134">All users in you organization will have Bookings licenses, but only those included in the policy can create Bookings calendars and have full control over who can access the calendars they create.</span></span>

<span data-ttu-id="76334-135">Les utilisateurs inclus dans cette stratégie peuvent créer de nouveaux calendriers Bookings et peuvent être ajoutés en tant que membres du personnel à n’importe quelle capacité (y compris le rôle d’administrateur) aux calendriers Bookings existants.</span><span class="sxs-lookup"><span data-stu-id="76334-135">Users who are included in this policy can create new Bookings calendars and can be added as staff in any capacity (including the administrator role) to existing Bookings calendars.</span></span> <span data-ttu-id="76334-136">Les utilisateurs qui ne sont pas inclus dans cette stratégie ne pourront pas créer de calendriers Bookings et recevront un message d’erreur s’ils essaient de le faire.</span><span class="sxs-lookup"><span data-stu-id="76334-136">Users who aren't included in this policy won't be able to create new Bookings calendars and will receive an error message if they try to do so.</span></span>

<span data-ttu-id="76334-137">Vous devez exécuter les commandes suivantes à l’aide d’Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="76334-137">You'll need to run the following commands using Exchange Online PowerShell.</span></span> <span data-ttu-id="76334-138">Pour plus d’informations sur l’exécution des cmdlets Exchange Online, voir [Se connecter à Exchange Online PowerShell.](/powershell/exchange/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="76334-138">For more information on running Exchange Online cmdlets, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76334-139">Les étapes ci-dessous supposent qu’aucune autre stratégie de boîte aux lettres Outlook Web App (OWA) n’a été créée dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76334-139">The steps below assume that no other Outlook Web App (OWA) mailbox policies have been created in your organization.</span></span>

1. <span data-ttu-id="76334-140">Créez une stratégie de boîte aux lettres pour les utilisateurs qui doivent être autorisés à créer des calendriers Bookings.</span><span class="sxs-lookup"><span data-stu-id="76334-140">Create a new mailbox policy for users that should be allowed to create Bookings calendars.</span></span> <span data-ttu-id="76334-141">(La création de calendrier Bookings est autorisée par défaut par les nouvelles stratégies de boîte aux lettres.)</span><span class="sxs-lookup"><span data-stu-id="76334-141">(Bookings calendar creation is allowed by default by new mailbox policies.)</span></span>

   ```PowerShell
   New-OwaMailboxPolicy -Name "BookingsCreators"
   ```

   <span data-ttu-id="76334-142">Pour plus d’informations, [voir New-OwaMailboxPolicy.](/powershell/module/exchange/new-owamailboxpolicy)</span><span class="sxs-lookup"><span data-stu-id="76334-142">For more information, see [New-OwaMailboxPolicy](/powershell/module/exchange/new-owamailboxpolicy).</span></span>

2. <span data-ttu-id="76334-143">Affectez cette stratégie aux utilisateurs concernés en exécutant cette commande pour chaque utilisateur que vous souhaitez accorder l’autorisation de créer des calendriers Bookings.</span><span class="sxs-lookup"><span data-stu-id="76334-143">Assign this policy to the relevant users by running this command for each user you want to grant permission to create Bookings calendars.</span></span>

   ```PowerShell
   Set-CASMailbox -Identity <someCreator@emailaddress> -OwaMailboxPolicy "BookingsCreators"
   ```

   <span data-ttu-id="76334-144">Pour plus d'informations, consultez la rubrique [Set-CASMailbox](/powershell/module/exchange/set-casmailbox).</span><span class="sxs-lookup"><span data-stu-id="76334-144">For more information, see [Set-CASMailbox](/powershell/module/exchange/set-casmailbox).</span></span>

3. <span data-ttu-id="76334-145">Facultatif : exécutez cette commande si vous souhaitez désactiver Bookings pour tous les autres utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="76334-145">Optional: Run this command if you want to disable Bookings for all other users in your organization.</span></span>

   ```PowerShell
   Set-OwaMailboxPolicy "OwaMailboxPolicy-Default" -BookingsMailboxCreationEnabled:$false
   ```

   <span data-ttu-id="76334-146">Pour plus d'informations, voir [Set-OwaMailboxPolicy](/powershell/module/exchange/set-owamailboxpolicy).</span><span class="sxs-lookup"><span data-stu-id="76334-146">For more information, see [Set-OwaMailboxPolicy](/powershell/module/exchange/set-owamailboxpolicy).</span></span>

<span data-ttu-id="76334-147">Pour plus d’informations OWA stratégies de boîte aux lettres, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="76334-147">For more information on OWA mailbox policies, check out the following topics:</span></span>

- [<span data-ttu-id="76334-148">Créer une stratégie de boîte aux lettres Outlook sur le web dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="76334-148">Create an Outlook on the web mailbox policy in Exchange Online</span></span>](/exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/create-outlook-web-app-mailbox-policy)

- [<span data-ttu-id="76334-149">Appliquer ou supprimer une stratégie de boîte aux lettres Outlook sur le web sur une boîte aux lettres dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="76334-149">Apply or remove an Outlook on the web mailbox policy on a mailbox in Exchange Online</span></span>](/exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/create-outlook-web-app-mailbox-policy)