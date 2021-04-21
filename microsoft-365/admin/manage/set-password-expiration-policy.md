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
ms.openlocfilehash: 14ff08126533d5c530fb56761a2ef1676d5864b8
ms.sourcegitcommit: 13ce4b31303a1a21ca53700a54bcf8d91ad2f8c1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51903153"
---
# <a name="set-the-password-expiration-policy-for-your-organization"></a><span data-ttu-id="1ce6b-103">Définir la stratégie d’expiration des mots de passe pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="1ce6b-103">Set the password expiration policy for your organization</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="1ce6b-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-104">The admin center is changing.</span></span> <span data-ttu-id="1ce6b-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](../microsoft-365-admin-center-preview.md?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="1ce6b-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](../microsoft-365-admin-center-preview.md?view=o365-worldwide).</span></span>

::: moniker-end

## <a name="before-you-begin"></a><span data-ttu-id="1ce6b-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1ce6b-106">Before you begin</span></span>

<span data-ttu-id="1ce6b-107">Cet article s’adresse aux personnes responsables de la stratégie d’expiration des mots de passe au sein d’une entreprise, d’une école ou d’une association.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-107">This article is for people who set password expiration policy for a business, school, or nonprofit.</span></span> <span data-ttu-id="1ce6b-108">Pour effectuer ces étapes, vous devez vous connecter avec votre compte d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-108">To complete these steps, you need to sign in with your Microsoft 365 admin account.</span></span> <span data-ttu-id="1ce6b-109">[Qu’est-ce qu’un compte d’administrateur ?](https://docs.microsoft.com/microsoft-365/business-video/admin-center-overview)</span><span class="sxs-lookup"><span data-stu-id="1ce6b-109">[What's an admin account?](https://docs.microsoft.com/microsoft-365/business-video/admin-center-overview).</span></span>

<span data-ttu-id="1ce6b-110">En tant qu'administrateur, vous pouvez faire en sorte qu'ils expirent après un certain nombre de jours ou qu'ils n'expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-110">As an admin, you can make user passwords expire after a certain number of days, or set passwords to never expire.</span></span> <span data-ttu-id="1ce6b-111">Par défaut, les mots de passe sont définies pour qu’ils n’expirent jamais pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-111">By default, passwords are set to never expire for your organization.</span></span>

<span data-ttu-id="1ce6b-112">Des recherches actuelles indiquent sans équivoque que les changements de mot de passe imposés ne sont pas forcément bénéfiques.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-112">Current research strongly indicates that mandated password changes do more harm than good.</span></span> <span data-ttu-id="1ce6b-113">Ils poussent les utilisateurs à choisir des mots de passe peu fiables, à réutiliser des mots de passe ou à mettre à jour d'anciens mots de passe de façon qu'ils sont facilement devinables de la part des pirates.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-113">They drive users to choose weaker passwords, re-use passwords, or update old passwords in ways that are easily guessed by hackers.</span></span> <span data-ttu-id="1ce6b-114">Nous vous recommandons d’activer [Authentification multifacteur](../security-and-compliance/set-up-multi-factor-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="1ce6b-114">We recommend enabling [multi-factor authentication](../security-and-compliance/set-up-multi-factor-authentication.md).</span></span> <span data-ttu-id="1ce6b-115">Pour en savoir plus sur la stratégie de mot de passe, vérifiez les [recommandations sur la stratégie de mot de passe ](../misc/password-policy-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1ce6b-115">To learn more about password policy, check out [Password policy recommendations](../misc/password-policy-recommendations.md).</span></span>

<span data-ttu-id="1ce6b-116">Vous devez être un [Administrateur général](../add-users/about-admin-roles.md) pour procéder à ces étapes.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-116">You must be a [global admin](../add-users/about-admin-roles.md) to perform these steps.</span></span>

<span data-ttu-id="1ce6b-117">Si vous êtes un utilisateur, vous ne disposez pas de l'autorisation pour paramétrer votre mot de passe afin qu'il reste valide dans le temps.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-117">If you're a user, you don't have the permissions to set your password to never expire.</span></span> <span data-ttu-id="1ce6b-118">Demandez au support technique de votre bureau ou de votre école d’effectuer les opérations indiquées dans cet article pour vous.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-118">Ask your work or school technical support to do the steps in this article for you.</span></span>

## <a name="set-password-expiration-policy"></a><span data-ttu-id="1ce6b-119">Définir la stratégie d’expiration de mot de passe</span><span class="sxs-lookup"><span data-stu-id="1ce6b-119">Set password expiration policy</span></span>

<span data-ttu-id="1ce6b-120">Si vous voulez que les mots de passe utilisateur expirent après un certain temps, suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-120">Follow the steps below if you want to set user passwords to expire after a specific amount of time.</span></span>

1. <span data-ttu-id="1ce6b-121">Dans le centre d’administration, cliquez sur la page **Paramètres** \> **Paramètres de l’organisation**.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-121">In the admin center, go to the **Settings** \> **Org Settings**.</span></span>

2. <span data-ttu-id="1ce6b-122">Accédez à la page <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Sécurité & confidentialité</a>.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-122">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Security & privacy</a> page.</span></span>
 <span data-ttu-id="1ce6b-123">Si vous n’êtes pas un administrateur général, l’option Sécurité et confidentialité n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-123">If you aren't a global admin, you won't see the Security and privacy option.</span></span>
  
3. <span data-ttu-id="1ce6b-124">Sélectionnez **Stratégie d’expiration du mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-124">Select **Password expiration policy**.</span></span>
  
4. <span data-ttu-id="1ce6b-125">Si vous ne voulez pas que les utilisateurs soient contraints de changer de mot de passe, décochez la case à côté de **Définir l’expiration des mots de passe d’utilisateur après un certain nombre de jours**.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-125">If you don't want users to have to change passwords, uncheck the box next to **Set user passwords to expire after a number of days**.</span></span>
  
5. <span data-ttu-id="1ce6b-126">Tapez la fréquence à laquelle les mots de passe doivent expirer.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-126">Type how often passwords should expire.</span></span> <span data-ttu-id="1ce6b-127">Choisissez un nombre de jours compris entre 14 et 730.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-127">Choose a number of days from 14 to 730.</span></span>
  
6. <span data-ttu-id="1ce6b-128">Dans la seconde zone, indiquez à quel moment les utilisateurs doivent être avisés de l'expiration prochaine du mot de passe, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-128">In the second box type when users are notified that their password will expire, and then select **Save**.</span></span> <span data-ttu-id="1ce6b-129">Choisissez un nombre de jours compris entre 1 et 30.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-129">Choose a number of days from 1 to 30.</span></span>
  
## <a name="important-things-you-need-to-know-about-the-password-expiration-feature"></a><span data-ttu-id="1ce6b-130">Points importants dont vous devez tenir compte concernant la fonctionnalité d’expiration de mot de passe</span><span class="sxs-lookup"><span data-stu-id="1ce6b-130">Important things you need to know about the password expiration feature</span></span>
  
- <span data-ttu-id="1ce6b-p109">Les personnes qui utilisent uniquement l’application Outlook ne sont pas obligées de réinitialiser leur mot de passe Microsoft 365 tant que ce dernier n’a pas expiré dans le cache. Cela peut se produire quelques jours après la date d’expiration. Il n’existe aucune solution de contournement à ce problème pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-p109">People who only use the Outlook app won't be forced to reset their Microsoft 365 password until it expires in the cache. This can be several days after the actual expiration date. There's no workaround for this at the admin level.</span></span>

## <a name="prevent-last-password-from-being-used-again"></a><span data-ttu-id="1ce6b-134">Empêcher la réutilisation du dernier mot de passe</span><span class="sxs-lookup"><span data-stu-id="1ce6b-134">Prevent last password from being used again</span></span>

<span data-ttu-id="1ce6b-135">Si vous le souhaitez, vous pouvez empêcher vos utilisateurs de recycler d’anciens mots de passe en appliquant l’historique de mot de passe dans Active Directory (AD) local.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-135">If you want to prevent your users from recycling old passwords, you can do so by enforcing password history in on-premises Active Directory (AD).</span></span> <span data-ttu-id="1ce6b-136">Voir [Créer une stratégie de mot de passe personnalisée](/azure/active-directory-domain-services/password-policy#create-a-custom-password-policy).</span><span class="sxs-lookup"><span data-stu-id="1ce6b-136">See [Create a custom password policy](/azure/active-directory-domain-services/password-policy#create-a-custom-password-policy).</span></span>

<span data-ttu-id="1ce6b-137">Dans Azure AD, le dernier mot de passe ne peut pas être réutilisé lorsque l’utilisateur modifie un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-137">In Azure AD, The last password can't be used again when the user changes a password.</span></span> <span data-ttu-id="1ce6b-138">La stratégie de mot de passe est appliquée à tous les comptes d’utilisateurs qui sont créés et gérés directement dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-138">The password policy is applied to all user accounts that are created and managed directly in Azure AD.</span></span> <span data-ttu-id="1ce6b-139">Cette stratégie de mot de passe ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-139">This password policy can't be modified.</span></span> <span data-ttu-id="1ce6b-140">Consultez [Stratégies de mot de passe Azure AD](/azure/active-directory/authentication/concept-sspr-policy#password-policies-that-only-apply-to-cloud-user-accounts).</span><span class="sxs-lookup"><span data-stu-id="1ce6b-140">See [Azure AD password policies](/azure/active-directory/authentication/concept-sspr-policy#password-policies-that-only-apply-to-cloud-user-accounts).</span></span>

## <a name="synchronize-user-passwords-hashes-from-an-on-premises-active-directory-to-azure-ad-microsoft-365"></a><span data-ttu-id="1ce6b-141">Synchroniser les hachages de mots de passe utilisateur à partir d’une instance Active Directory locale vers une instance Azure AD (Microsoft 365)</span><span class="sxs-lookup"><span data-stu-id="1ce6b-141">Synchronize user passwords hashes from an on-premises Active Directory to Azure AD (Microsoft 365)</span></span>

<span data-ttu-id="1ce6b-142">Cet article est consacré à la définition de la stratégie d’expiration pour les utilisateurs exclusivement cloud (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="1ce6b-142">This article is for setting the expiration policy for cloud-only users (Azure AD).</span></span> <span data-ttu-id="1ce6b-143">Il ne s’applique pas aux utilisateurs d’identité hybride utilisant la synchronisation par hachage du mot de passe, l’authentification directe ou la fédération locale telle que ADFS.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-143">It doesn't apply to hybrid identity users who use password hash sync, pass-through authentication, or on-premises federation like ADFS.</span></span>
  
<span data-ttu-id="1ce6b-144">Pour découvrir comment synchroniser les hachages de mot de passe utilisateur d'Active Directory local avec Azure Active Directory, voir [Implémenter la synchronisation du hachage de mot de passe avec la synchronisation Azure AD Connect](/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization).</span><span class="sxs-lookup"><span data-stu-id="1ce6b-144">To learn how to synchronize user password hashes from on premises AD to Azure AD, see [Implement password hash synchronization with Azure AD Connect sync](/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization).</span></span>

## <a name="password-policies-and-account-restrictions-in-azure-active-directory"></a><span data-ttu-id="1ce6b-145">Stratégies de mot de passe et restrictions de compte dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="1ce6b-145">Password policies and account restrictions in Azure Active Directory</span></span>

<span data-ttu-id="1ce6b-146">Vous pouvez spécifier d’autres stratégies et restrictions de mot de passe dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-146">You can set more password policies and restrictions in Azure active directory.</span></span> <span data-ttu-id="1ce6b-147">Consultez [Stratégies de mot de passe et restrictions de compte dans Azure Active Directory](/azure/active-directory/authentication/concept-sspr-policy) pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-147">Check out [Password policies and account restrictions in Azure Active Directory](/azure/active-directory/authentication/concept-sspr-policy) for more info.</span></span>

## <a name="update-password-policy"></a><span data-ttu-id="1ce6b-148">Mise à jour de la stratégie de mot de passe</span><span class="sxs-lookup"><span data-stu-id="1ce6b-148">Update password Policy</span></span>

<span data-ttu-id="1ce6b-149">L’applet de commande Set-MsolPasswordPolicy met à jour la stratégie de mot de passe d’un domaine ou d’un client spécifié.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-149">The Set-MsolPasswordPolicy cmdlet updates the password policy of a specified domain or tenant.</span></span> <span data-ttu-id="1ce6b-150">Deux paramètres sont requis. La premier consiste à indiquer la durée pendant laquelle un mot de passe reste valide avant qu’il ne soit modifié et que le deuxième indique le nombre de jours avant la date d’expiration du mot de passe qui s’affiche lorsque les utilisateurs reçoivent la première notification leur indiquant que leur mot de passe arrive bientôt à expiration.</span><span class="sxs-lookup"><span data-stu-id="1ce6b-150">Two settings are required; the first is to indicate the length of time that a password remains valid before it must be changed and the second is to indicate the number of days before the password expiration date that will trigger when users will receive their first notification that their password will soon expire.</span></span>

<span data-ttu-id="1ce6b-151">Si vous souhaitez obtenir plus d’informations sur la mise à jour de la stratégie de mot de passe pour un domaine ou un client spécifique, consultez [Set-MsolPasswordPolicy](/powershell/module/msonline/set-msolpasswordpolicy?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="1ce6b-151">To learn how to update password policy for a specific domain or tenant, see [Set-MsolPasswordPolicy](/powershell/module/msonline/set-msolpasswordpolicy?view=azureadps-1.0).</span></span>

## <a name="related-content"></a><span data-ttu-id="1ce6b-152">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="1ce6b-152">Related content</span></span>

[<span data-ttu-id="1ce6b-153">Autoriser les utilisateurs à réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="1ce6b-153">Let users reset their own passwords</span></span>](../add-users/let-users-reset-passwords.md)

[<span data-ttu-id="1ce6b-154">Réinitialiser les mots de passe</span><span class="sxs-lookup"><span data-stu-id="1ce6b-154">Reset passwords</span></span>](../add-users/reset-passwords.md)