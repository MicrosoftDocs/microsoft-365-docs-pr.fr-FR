---
title: Définir la stratégie d’expiration des mots de passe pour votre organisation
f1.keywords:
- CSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 0f54736f-eb22-414c-8273-498a0918678f
description: "Découvrez comment configurer une stratégie d'expiration des mots de passe pour votre organisation dans le Centre d'administration Microsoft 365. "
ms.openlocfilehash: a4d5f5240a6d4cca686b4809d05970b5e18b897f
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44399577"
---
# <a name="set-the-password-expiration-policy-for-your-organization"></a><span data-ttu-id="6ada9-103">Définir la stratégie d’expiration des mots de passe pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="6ada9-103">Set the password expiration policy for your organization</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="6ada9-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="6ada9-104">The admin center is changing.</span></span> <span data-ttu-id="6ada9-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="6ada9-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="6ada9-106">Cet article s’adresse aux personnes responsables de la stratégie d’expiration des mots de passe au sein d’une entreprise, d’une école ou d’une association.</span><span class="sxs-lookup"><span data-stu-id="6ada9-106">This article is for people who set password expiration policy for a business, school, or nonprofit.</span></span>  

<span data-ttu-id="6ada9-107">Si vous êtes un utilisateur, vous ne disposez pas de l'autorisation pour paramétrer votre mot de passe afin qu'il reste valide dans le temps.</span><span class="sxs-lookup"><span data-stu-id="6ada9-107">If you're a user, you don't have the permissions to set your password to never expire.</span></span> <span data-ttu-id="6ada9-108">Demandez au support technique de votre bureau ou de votre école d’effectuer les opérations indiquées dans cet article pour vous.</span><span class="sxs-lookup"><span data-stu-id="6ada9-108">Ask your work or school technical support to do the steps in this article for you.</span></span>

<span data-ttu-id="6ada9-109">En tant qu'administrateur, vous pouvez faire en sorte qu'ils expirent après un certain nombre de jours ou qu'ils n'expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="6ada9-109">As an admin, you can make user passwords expire after a certain number of days, or set passwords to never expire.</span></span> 

> [!Tip]
> <span data-ttu-id="6ada9-110">Par défaut, les mots de passe sont définis pour expirer après 90 jours.</span><span class="sxs-lookup"><span data-stu-id="6ada9-110">By default, passwords are set to expire in 90 days.</span></span> <span data-ttu-id="6ada9-111">Des recherches actuelles indiquent sans équivoque que les changements de mot de passe imposés ne sont pas forcément bénéfiques.</span><span class="sxs-lookup"><span data-stu-id="6ada9-111">Current research strongly indicates that mandated password changes do more harm than good.</span></span> <span data-ttu-id="6ada9-112">Ils poussent les utilisateurs à choisir des mots de passe peu fiables, à réutiliser des mots de passe ou à mettre à jour d'anciens mots de passe de façon qu'ils sont facilement devinables de la part des pirates.</span><span class="sxs-lookup"><span data-stu-id="6ada9-112">They drive users to choose weaker passwords, re-use passwords, or update old passwords in ways that are easily guessed by hackers.</span></span> <span data-ttu-id="6ada9-113">Si le mot de passe est paramétré de façon à ce qu'il n’expire jamais, nous vous recommandons d’activer [l'authentification multifacteur](../security-and-compliance/set-up-multi-factor-authentication.md)d’authentification.</span><span class="sxs-lookup"><span data-stu-id="6ada9-113">If setting password to never expire, we recommend enabling [multi-factor authentication](../security-and-compliance/set-up-multi-factor-authentication.md).</span></span>

<span data-ttu-id="6ada9-114">Si vous voulez que les mots de passe utilisateur expirent après un certain temps, suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6ada9-114">Follow the steps below if you want to set user passwords to expire after a specific amount of time.</span></span>
> [!IMPORTANT]
> <span data-ttu-id="6ada9-115">Seuls les [administrateurs généraux](../add-users/about-admin-roles.md) peuvent effectuer ces étapes.</span><span class="sxs-lookup"><span data-stu-id="6ada9-115">Only [global admins](../add-users/about-admin-roles.md) can perform these steps.</span></span>
  
1. <span data-ttu-id="6ada9-116">Dans le centre d’administration, cliquez sur la page **Paramètres** \> **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="6ada9-116">In the admin center, go to the **Settings** \> **Settings**.</span></span>

2. <span data-ttu-id="6ada9-117">Accédez à la page <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Sécurité & confidentialité</a>.</span><span class="sxs-lookup"><span data-stu-id="6ada9-117">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Security & privacy</a> page.</span></span>
 <span data-ttu-id="6ada9-118">Si vous n’êtes pas un administrateur général, l’option Sécurité et confidentialité n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="6ada9-118">If you aren't a global admin, you won't see the Security and privacy option.</span></span>
  
3. <span data-ttu-id="6ada9-119">Sélectionnez **Stratégie d’expiration du mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="6ada9-119">Select **Password expiration policy**.</span></span>
  
4. <span data-ttu-id="6ada9-120">Si vous ne souhaitez pas que les utilisateurs soient contraints de changer leur mot de passe, activez la case à cocher près de **Configurer les mots de passe utilisateur pour qu’ils expirent après un certain nombre de jours**.</span><span class="sxs-lookup"><span data-stu-id="6ada9-120">If you don't want users to have to change passwords, select the checkbox next to **Set user passwords to expire after a number of days**.</span></span>
  
5. <span data-ttu-id="6ada9-121">Tapez la fréquence à laquelle les mots de passe doivent expirer.</span><span class="sxs-lookup"><span data-stu-id="6ada9-121">Type how often passwords should expire.</span></span> <span data-ttu-id="6ada9-122">Choisissez un nombre de jours compris entre 14 et 730.</span><span class="sxs-lookup"><span data-stu-id="6ada9-122">Choose a number of days from 14 to 730.</span></span>
  
6. <span data-ttu-id="6ada9-123">Dans la seconde zone, indiquez à quel moment les utilisateurs doivent être avisés de l'expiration prochaine du mot de passe, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6ada9-123">In the second box type when users are notified that their password will expire, and then select **Save**.</span></span> <span data-ttu-id="6ada9-124">Choisissez un nombre de jours compris entre 1 et 30.</span><span class="sxs-lookup"><span data-stu-id="6ada9-124">Choose a number of days from 1 to 30.</span></span>
    
7. <span data-ttu-id="6ada9-125">Lorsque le mot de passe de l’utilisateur expire, ce dernier reçoit une notification qui s’affiche dans le coin inférieur droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="6ada9-125">When the user's password expires, they'll get a notification that appears in the lower right corner of their screen.</span></span>
  
## <a name="important-things-you-need-to-know-about-the-password-expiration-feature"></a><span data-ttu-id="6ada9-126">Points importants dont vous devez tenir compte concernant la fonctionnalité d’expiration de mot de passe</span><span class="sxs-lookup"><span data-stu-id="6ada9-126">Important things you need to know about the password expiration feature</span></span>

<span data-ttu-id="6ada9-127">Voici quelques points dont vous devez tenir compte concernant le fonctionnement actuel de cette fonctionnalité à compter du mois de janvier 2018 :</span><span class="sxs-lookup"><span data-stu-id="6ada9-127">Here are some things to know about how this feature currently works as of January 2018:</span></span>
  
- <span data-ttu-id="6ada9-p107">Les personnes qui utilisent uniquement l’application Outlook ne sont pas obligées de réinitialiser leur mot de passe Microsoft 365 tant que ce dernier n’a pas expiré dans le cache. Cela peut se produire quelques jours après la date d’expiration. Il n’existe aucune solution de contournement à ce problème pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="6ada9-p107">People who only use the Outlook app won't be forced to reset their Microsoft 365 password until it expires in the cache. This can be several days after the actual expiration date. There's no workaround for this at the admin level.</span></span>
    
- <span data-ttu-id="6ada9-p108">Les utilisateurs ne reçoivent pas de notification par courrier indiquant que leur mot de passe expire dans X jours. Voulez-vous utiliser cette fonctionnalité ? **[Votez ici !](https://office365.uservoice.com/forums/273493-office-365-admin/suggestions/15028344-office-365-password-email-notification)**</span><span class="sxs-lookup"><span data-stu-id="6ada9-p108">Users do not get an email notification that their password is going to expire in X number of days. Do you want this feature? **[Vote here!](https://office365.uservoice.com/forums/273493-office-365-admin/suggestions/15028344-office-365-password-email-notification)**</span></span>
    
## <a name="prevent-last-password-from-being-used-again"></a><span data-ttu-id="6ada9-134">Empêcher la réutilisation du dernier mot de passe</span><span class="sxs-lookup"><span data-stu-id="6ada9-134">Prevent last password from being used again</span></span>

<span data-ttu-id="6ada9-135">Si vous le souhaitez, vous pouvez empêcher vos utilisateurs de recycler d’anciens mots de passe à partir d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ada9-135">If you want to prevent your users from recycling old passwords, you can do so in Azure AD.</span></span> <span data-ttu-id="6ada9-136">Voir [Appliquer l'historique des mots de passe](https://docs.microsoft.com/windows/security/threat-protection/security-policy-settings/enforce-password-history).</span><span class="sxs-lookup"><span data-stu-id="6ada9-136">See [Enforce password history](https://docs.microsoft.com/windows/security/threat-protection/security-policy-settings/enforce-password-history).</span></span>

<span data-ttu-id="6ada9-137">De plus, si un employé a utilisé un appareil mobile pour accéder à Microsoft 365, vous pouvez réinitialiser le mot de passe afin de vous assurer qu’il n’est plus stocké et recyclé à partir de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="6ada9-137">In addition, if an employee used a mobile device to access Microsoft 365, you can wipe it to ensure the password is no longer stored and recycled from there.</span></span> <span data-ttu-id="6ada9-138">Pour plus d'informations, voir [Réinitialiser et bloquer l’appareil mobile d’un ancien employé](https://docs.microsoft.com/office365/admin/add-users/remove-former-employee?view=o365-worldwide#wipe-and-block-a-former-employees-mobile-device).</span><span class="sxs-lookup"><span data-stu-id="6ada9-138">To learn more, see [Wipe and block a former employee's mobile device](https://docs.microsoft.com/office365/admin/add-users/remove-former-employee?view=o365-worldwide#wipe-and-block-a-former-employees-mobile-device).</span></span>


## <a name="synchronize-user-passwords-hashes-from-an-on-premises-active-directory-to-azure-ad-microsoft-365"></a><span data-ttu-id="6ada9-139">Synchroniser les hachages de mots de passe utilisateur à partir d’une instance Active Directory locale vers une instance Azure AD (Microsoft 365)</span><span class="sxs-lookup"><span data-stu-id="6ada9-139">Synchronize user passwords hashes from an on-premises Active Directory to Azure AD (Microsoft 365)</span></span>

<span data-ttu-id="6ada9-140">Cet article est consacré à la définition de la stratégie d’expiration pour les utilisateurs exclusivement cloud (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="6ada9-140">This article is for setting the expiration policy for cloud-only users (Azure AD).</span></span> <span data-ttu-id="6ada9-141">Il ne s’applique pas aux utilisateurs d’identité hybride utilisant la synchronisation par hachage du mot de passe, l’authentification directe ou la Fédération locale telle que ADFS.</span><span class="sxs-lookup"><span data-stu-id="6ada9-141">It doesn't apply to hybrid identity users who use password hash sync, pass-through authentication or on-premises federation like ADFS.</span></span>
  
<span data-ttu-id="6ada9-142">Pour découvrir comment synchroniser les hachages de mot de passe utilisateur d'Active Directory local avec Azure Active Directory, voir [Implémenter la synchronisation du hachage de mot de passe avec la synchronisation Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization).</span><span class="sxs-lookup"><span data-stu-id="6ada9-142">To learn how to synchronize user password hashes from on premises AD to Azure AD, see [Implement password hash synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization).</span></span>
