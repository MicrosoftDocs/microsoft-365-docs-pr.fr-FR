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
ms.custom:
- AdminSurgePortfolio
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 0f54736f-eb22-414c-8273-498a0918678f
description: Découvrez comment configurer une stratégie d'expiration des mots de passe pour votre organisation dans le Centre d'administration Microsoft 365.
ms.openlocfilehash: 9470a73926327777055a321eb3a592ea3ddcf41e
ms.sourcegitcommit: babbba2b5bf69fd3facde2905ec024b753dcd1b3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "50515039"
---
# <a name="set-the-password-expiration-policy-for-your-organization"></a><span data-ttu-id="8bd02-103">Définir la stratégie d’expiration des mots de passe pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="8bd02-103">Set the password expiration policy for your organization</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="8bd02-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="8bd02-104">The admin center is changing.</span></span> <span data-ttu-id="8bd02-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="8bd02-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-worldwide).</span></span>

::: moniker-end

## <a name="before-you-begin"></a><span data-ttu-id="8bd02-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8bd02-106">Before you begin</span></span>

<span data-ttu-id="8bd02-107">Cet article s’adresse aux personnes responsables de la stratégie d’expiration des mots de passe au sein d’une entreprise, d’une école ou d’une association.</span><span class="sxs-lookup"><span data-stu-id="8bd02-107">This article is for people who set password expiration policy for a business, school, or nonprofit.</span></span> <span data-ttu-id="8bd02-108">Pour effectuer ces étapes, vous devez vous connecter avec votre compte d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8bd02-108">To complete these steps, you need to sign in with your Microsoft 365 admin account.</span></span> <span data-ttu-id="8bd02-109">[Qu’est-ce qu’un compte d’administrateur ?](../admin-overview/admin-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8bd02-109">[What's an admin account?](../admin-overview/admin-overview.md).</span></span>

<span data-ttu-id="8bd02-110">Vous devez être un [administrateur global ou de mots de passe](../add-users/about-admin-roles.md) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="8bd02-110">You must be a [global admin or password admin](../add-users/about-admin-roles.md) to perform these steps.</span></span>

<span data-ttu-id="8bd02-111">Si vous êtes un utilisateur, vous ne disposez pas de l'autorisation pour paramétrer votre mot de passe afin qu'il reste valide dans le temps.</span><span class="sxs-lookup"><span data-stu-id="8bd02-111">If you're a user, you don't have the permissions to set your password to never expire.</span></span> <span data-ttu-id="8bd02-112">Demandez au support technique de votre bureau ou de votre école d’effectuer les opérations indiquées dans cet article pour vous.</span><span class="sxs-lookup"><span data-stu-id="8bd02-112">Ask your work or school technical support to do the steps in this article for you.</span></span>

<span data-ttu-id="8bd02-113">En tant qu'administrateur, vous pouvez faire en sorte qu'ils expirent après un certain nombre de jours ou qu'ils n'expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="8bd02-113">As an admin, you can make user passwords expire after a certain number of days, or set passwords to never expire.</span></span>

## <a name="set-password-expiration-policy"></a><span data-ttu-id="8bd02-114">Définir la stratégie d’expiration de mot de passe</span><span class="sxs-lookup"><span data-stu-id="8bd02-114">Set password expiration policy</span></span>

> [!Tip]
> <span data-ttu-id="8bd02-115">Par défaut, les mots de passe sont définis pour expirer après 90 jours.</span><span class="sxs-lookup"><span data-stu-id="8bd02-115">By default, passwords are set to expire in 90 days.</span></span> <span data-ttu-id="8bd02-116">Des recherches actuelles indiquent sans équivoque que les changements de mot de passe imposés ne sont pas forcément bénéfiques.</span><span class="sxs-lookup"><span data-stu-id="8bd02-116">Current research strongly indicates that mandated password changes do more harm than good.</span></span> <span data-ttu-id="8bd02-117">Ils poussent les utilisateurs à choisir des mots de passe peu fiables, à réutiliser des mots de passe ou à mettre à jour d'anciens mots de passe de façon qu'ils sont facilement devinables de la part des pirates.</span><span class="sxs-lookup"><span data-stu-id="8bd02-117">They drive users to choose weaker passwords, re-use passwords, or update old passwords in ways that are easily guessed by hackers.</span></span> <span data-ttu-id="8bd02-118">Si le mot de passe est paramétré de façon à ce qu'il n’expire jamais, nous vous recommandons d’activer [l'authentification multifacteur](../security-and-compliance/set-up-multi-factor-authentication.md)d’authentification.</span><span class="sxs-lookup"><span data-stu-id="8bd02-118">If setting password to never expire, we recommend enabling [multi-factor authentication](../security-and-compliance/set-up-multi-factor-authentication.md).</span></span>

<span data-ttu-id="8bd02-119">Si vous voulez que les mots de passe utilisateur expirent après un certain temps, suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8bd02-119">Follow the steps below if you want to set user passwords to expire after a specific amount of time.</span></span>
> [!IMPORTANT]
> <span data-ttu-id="8bd02-120">Seuls les [administrateurs généraux](../add-users/about-admin-roles.md) peuvent effectuer ces étapes.</span><span class="sxs-lookup"><span data-stu-id="8bd02-120">Only [global admins](../add-users/about-admin-roles.md) can perform these steps.</span></span>
  
1. <span data-ttu-id="8bd02-121">Dans le centre d’administration, cliquez sur la page **Paramètres** \> **Paramètres de l’organisation**.</span><span class="sxs-lookup"><span data-stu-id="8bd02-121">In the admin center, go to the **Settings** \> **Org Settings**.</span></span>

2. <span data-ttu-id="8bd02-122">Accédez à la page <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Sécurité & confidentialité</a>.</span><span class="sxs-lookup"><span data-stu-id="8bd02-122">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Security & privacy</a> page.</span></span>
 <span data-ttu-id="8bd02-123">Si vous n’êtes pas un administrateur général, l’option Sécurité et confidentialité n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="8bd02-123">If you aren't a global admin, you won't see the Security and privacy option.</span></span>
  
3. <span data-ttu-id="8bd02-124">Sélectionnez **Stratégie d’expiration du mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="8bd02-124">Select **Password expiration policy**.</span></span>
  
4. <span data-ttu-id="8bd02-125">Si vous ne voulez pas que les utilisateurs soient contraints de changer de mot de passe, décochez la case à côté de **Définir l’expiration des mots de passe d’utilisateur après un certain nombre de jours**.</span><span class="sxs-lookup"><span data-stu-id="8bd02-125">If you don't want users to have to change passwords, uncheck the box next to **Set user passwords to expire after a number of days**.</span></span>
  
5. <span data-ttu-id="8bd02-126">Tapez la fréquence à laquelle les mots de passe doivent expirer.</span><span class="sxs-lookup"><span data-stu-id="8bd02-126">Type how often passwords should expire.</span></span> <span data-ttu-id="8bd02-127">Choisissez un nombre de jours compris entre 14 et 730.</span><span class="sxs-lookup"><span data-stu-id="8bd02-127">Choose a number of days from 14 to 730.</span></span>
  
6. <span data-ttu-id="8bd02-128">Dans la seconde zone, indiquez à quel moment les utilisateurs doivent être avisés de l'expiration prochaine du mot de passe, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8bd02-128">In the second box type when users are notified that their password will expire, and then select **Save**.</span></span> <span data-ttu-id="8bd02-129">Choisissez un nombre de jours compris entre 1 et 30.</span><span class="sxs-lookup"><span data-stu-id="8bd02-129">Choose a number of days from 1 to 30.</span></span>
  
## <a name="important-things-you-need-to-know-about-the-password-expiration-feature"></a><span data-ttu-id="8bd02-130">Points importants dont vous devez tenir compte concernant la fonctionnalité d’expiration de mot de passe</span><span class="sxs-lookup"><span data-stu-id="8bd02-130">Important things you need to know about the password expiration feature</span></span>
  
- <span data-ttu-id="8bd02-p108">Les personnes qui utilisent uniquement l’application Outlook ne sont pas obligées de réinitialiser leur mot de passe Microsoft 365 tant que ce dernier n’a pas expiré dans le cache. Cela peut se produire quelques jours après la date d’expiration. Il n’existe aucune solution de contournement à ce problème pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="8bd02-p108">People who only use the Outlook app won't be forced to reset their Microsoft 365 password until it expires in the cache. This can be several days after the actual expiration date. There's no workaround for this at the admin level.</span></span>

## <a name="prevent-last-password-from-being-used-again"></a><span data-ttu-id="8bd02-134">Empêcher la réutilisation du dernier mot de passe</span><span class="sxs-lookup"><span data-stu-id="8bd02-134">Prevent last password from being used again</span></span>

<span data-ttu-id="8bd02-135">Si vous le souhaitez, vous pouvez empêcher vos utilisateurs de recycler d’anciens mots de passe en appliquant l’historique de mot de passe dans Active Directory (AD) local.</span><span class="sxs-lookup"><span data-stu-id="8bd02-135">If you want to prevent your users from recycling old passwords, you can do so by enforcing password history in on-premises Active Directory (AD).</span></span> <span data-ttu-id="8bd02-136">Voir [Créer une stratégie de mot de passe personnalisée](https://docs.microsoft.com/azure/active-directory-domain-services/password-policy#create-a-custom-password-policy).</span><span class="sxs-lookup"><span data-stu-id="8bd02-136">See [Create a custom password policy](https://docs.microsoft.com/azure/active-directory-domain-services/password-policy#create-a-custom-password-policy).</span></span>

<span data-ttu-id="8bd02-137">Dans Azure AD, le dernier mot de passe ne peut pas être réutilisé lorsque l’utilisateur modifie un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="8bd02-137">In Azure AD, The last password can't be used again when the user changes a password.</span></span> <span data-ttu-id="8bd02-138">La stratégie de mot de passe est appliquée à tous les comptes d’utilisateurs qui sont créés et gérés directement dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8bd02-138">The password policy is applied to all user accounts that are created and managed directly in Azure AD.</span></span> <span data-ttu-id="8bd02-139">Cette stratégie de mot de passe ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="8bd02-139">This password policy can't be modified.</span></span> <span data-ttu-id="8bd02-140">Consultez [Stratégies de mot de passe Azure AD](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy#password-policies-that-only-apply-to-cloud-user-accounts).</span><span class="sxs-lookup"><span data-stu-id="8bd02-140">See [Azure AD password policies](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy#password-policies-that-only-apply-to-cloud-user-accounts).</span></span>

## <a name="synchronize-user-passwords-hashes-from-an-on-premises-active-directory-to-azure-ad-microsoft-365"></a><span data-ttu-id="8bd02-141">Synchroniser les hachages de mots de passe utilisateur à partir d’une instance Active Directory locale vers une instance Azure AD (Microsoft 365)</span><span class="sxs-lookup"><span data-stu-id="8bd02-141">Synchronize user passwords hashes from an on-premises Active Directory to Azure AD (Microsoft 365)</span></span>

<span data-ttu-id="8bd02-142">Cet article est consacré à la définition de la stratégie d’expiration pour les utilisateurs exclusivement cloud (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="8bd02-142">This article is for setting the expiration policy for cloud-only users (Azure AD).</span></span> <span data-ttu-id="8bd02-143">Il ne s’applique pas aux utilisateurs d’identité hybride utilisant la synchronisation par hachage du mot de passe, l’authentification directe ou la fédération locale telle que ADFS.</span><span class="sxs-lookup"><span data-stu-id="8bd02-143">It doesn't apply to hybrid identity users who use password hash sync, pass-through authentication, or on-premises federation like ADFS.</span></span>
  
<span data-ttu-id="8bd02-144">Pour découvrir comment synchroniser les hachages de mot de passe utilisateur d'Active Directory local avec Azure Active Directory, voir [Implémenter la synchronisation du hachage de mot de passe avec la synchronisation Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization).</span><span class="sxs-lookup"><span data-stu-id="8bd02-144">To learn how to synchronize user password hashes from on premises AD to Azure AD, see [Implement password hash synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization).</span></span>

## <a name="password-policies-and-account-restrictions-in-azure-active-directory"></a><span data-ttu-id="8bd02-145">Stratégies de mot de passe et restrictions de compte dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8bd02-145">Password policies and account restrictions in Azure Active Directory</span></span>

<span data-ttu-id="8bd02-146">Vous pouvez spécifier d’autres stratégies et restrictions de mot de passe dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8bd02-146">You can set more password policies and restrictions in Azure active directory.</span></span> <span data-ttu-id="8bd02-147">Consultez [Stratégies de mot de passe et restrictions de compte dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy) pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="8bd02-147">Check out [Password policies and account restrictions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy) for more info.</span></span>

## <a name="update-password-policy"></a><span data-ttu-id="8bd02-148">Mise à jour de la stratégie de mot de passe</span><span class="sxs-lookup"><span data-stu-id="8bd02-148">Update password Policy</span></span>

<span data-ttu-id="8bd02-149">L’applet de commande Set-MsolPasswordPolicy met à jour la stratégie de mot de passe d’un domaine ou d’un client spécifié.</span><span class="sxs-lookup"><span data-stu-id="8bd02-149">The Set-MsolPasswordPolicy cmdlet updates the password policy of a specified domain or tenant.</span></span> <span data-ttu-id="8bd02-150">Deux paramètres sont requis. La premier consiste à indiquer la durée pendant laquelle un mot de passe reste valide avant qu’il ne soit modifié et que le deuxième indique le nombre de jours avant la date d’expiration du mot de passe qui s’affiche lorsque les utilisateurs reçoivent la première notification leur indiquant que leur mot de passe arrive bientôt à expiration.</span><span class="sxs-lookup"><span data-stu-id="8bd02-150">Two settings are required; the first is to indicate the length of time that a password remains valid before it must be changed and the second is to indicate the number of days before the password expiration date that will trigger when users will receive their first notification that their password will soon expire.</span></span>

<span data-ttu-id="8bd02-151">Si vous souhaitez obtenir plus d’informations sur la mise à jour de la stratégie de mot de passe pour un domaine ou un client spécifique, consultez [Set-MsolPasswordPolicy](https://docs.microsoft.com/powershell/module/msonline/set-msolpasswordpolicy?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="8bd02-151">To learn how to update password policy for a specific domain or tenant, see [Set-MsolPasswordPolicy](https://docs.microsoft.com/powershell/module/msonline/set-msolpasswordpolicy?view=azureadps-1.0).</span></span>

## <a name="related-content"></a><span data-ttu-id="8bd02-152">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="8bd02-152">Related content</span></span>

[<span data-ttu-id="8bd02-153">Autoriser les utilisateurs à réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="8bd02-153">Let users reset their own passwords</span></span>](../add-users/let-users-reset-passwords.md)

[<span data-ttu-id="8bd02-154">Réinitialiser les mots de passe</span><span class="sxs-lookup"><span data-stu-id="8bd02-154">Reset passwords</span></span>](../add-users/reset-passwords.md)
