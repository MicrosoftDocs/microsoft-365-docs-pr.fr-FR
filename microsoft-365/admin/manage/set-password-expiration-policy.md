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
ms.openlocfilehash: eec6231d2c6b5d51b25f42c401e367743fdb19ea
ms.sourcegitcommit: d988faa292c2661ffea43c7161aef92b2b4b99bc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/04/2020
ms.locfileid: "46560870"
---
# <a name="set-the-password-expiration-policy-for-your-organization"></a><span data-ttu-id="6095d-103">Définir la stratégie d’expiration des mots de passe pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="6095d-103">Set the password expiration policy for your organization</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="6095d-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="6095d-104">The admin center is changing.</span></span> <span data-ttu-id="6095d-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="6095d-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="6095d-106">Cet article s’adresse aux personnes responsables de la stratégie d’expiration des mots de passe au sein d’une entreprise, d’une école ou d’une association.</span><span class="sxs-lookup"><span data-stu-id="6095d-106">This article is for people who set password expiration policy for a business, school, or nonprofit.</span></span>  

<span data-ttu-id="6095d-107">Si vous êtes un utilisateur, vous ne disposez pas de l'autorisation pour paramétrer votre mot de passe afin qu'il reste valide dans le temps.</span><span class="sxs-lookup"><span data-stu-id="6095d-107">If you're a user, you don't have the permissions to set your password to never expire.</span></span> <span data-ttu-id="6095d-108">Demandez au support technique de votre bureau ou de votre école d’effectuer les opérations indiquées dans cet article pour vous.</span><span class="sxs-lookup"><span data-stu-id="6095d-108">Ask your work or school technical support to do the steps in this article for you.</span></span>

<span data-ttu-id="6095d-109">En tant qu'administrateur, vous pouvez faire en sorte qu'ils expirent après un certain nombre de jours ou qu'ils n'expirent jamais.</span><span class="sxs-lookup"><span data-stu-id="6095d-109">As an admin, you can make user passwords expire after a certain number of days, or set passwords to never expire.</span></span> 

> [!Tip]
> <span data-ttu-id="6095d-110">Par défaut, les mots de passe sont définis pour expirer après 90 jours.</span><span class="sxs-lookup"><span data-stu-id="6095d-110">By default, passwords are set to expire in 90 days.</span></span> <span data-ttu-id="6095d-111">Des recherches actuelles indiquent sans équivoque que les changements de mot de passe imposés ne sont pas forcément bénéfiques.</span><span class="sxs-lookup"><span data-stu-id="6095d-111">Current research strongly indicates that mandated password changes do more harm than good.</span></span> <span data-ttu-id="6095d-112">Ils poussent les utilisateurs à choisir des mots de passe peu fiables, à réutiliser des mots de passe ou à mettre à jour d'anciens mots de passe de façon qu'ils sont facilement devinables de la part des pirates.</span><span class="sxs-lookup"><span data-stu-id="6095d-112">They drive users to choose weaker passwords, re-use passwords, or update old passwords in ways that are easily guessed by hackers.</span></span> <span data-ttu-id="6095d-113">Si le mot de passe est paramétré de façon à ce qu'il n’expire jamais, nous vous recommandons d’activer [l'authentification multifacteur](../security-and-compliance/set-up-multi-factor-authentication.md)d’authentification.</span><span class="sxs-lookup"><span data-stu-id="6095d-113">If setting password to never expire, we recommend enabling [multi-factor authentication](../security-and-compliance/set-up-multi-factor-authentication.md).</span></span>

<span data-ttu-id="6095d-114">Si vous voulez que les mots de passe utilisateur expirent après un certain temps, suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6095d-114">Follow the steps below if you want to set user passwords to expire after a specific amount of time.</span></span>
> [!IMPORTANT]
> <span data-ttu-id="6095d-115">Seuls les [administrateurs généraux](../add-users/about-admin-roles.md) peuvent effectuer ces étapes.</span><span class="sxs-lookup"><span data-stu-id="6095d-115">Only [global admins](../add-users/about-admin-roles.md) can perform these steps.</span></span>
  
1. <span data-ttu-id="6095d-116">Dans le centre d’administration, cliquez sur la page **Paramètres** \> **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="6095d-116">In the admin center, go to the **Settings** \> **Settings**.</span></span>

2. <span data-ttu-id="6095d-117">Accédez à la page <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Sécurité & confidentialité</a>.</span><span class="sxs-lookup"><span data-stu-id="6095d-117">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Security & privacy</a> page.</span></span>
 <span data-ttu-id="6095d-118">Si vous n’êtes pas un administrateur général, l’option Sécurité et confidentialité n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="6095d-118">If you aren't a global admin, you won't see the Security and privacy option.</span></span>
  
3. <span data-ttu-id="6095d-119">Sélectionnez **Stratégie d’expiration du mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="6095d-119">Select **Password expiration policy**.</span></span>
  
4. <span data-ttu-id="6095d-120">Si vous ne souhaitez pas que les utilisateurs soient contraints de changer leur mot de passe, activez la case à cocher près de **Configurer les mots de passe utilisateur pour qu’ils expirent après un certain nombre de jours**.</span><span class="sxs-lookup"><span data-stu-id="6095d-120">If you don't want users to have to change passwords, select the checkbox next to **Set user passwords to expire after a number of days**.</span></span>
  
5. <span data-ttu-id="6095d-121">Tapez la fréquence à laquelle les mots de passe doivent expirer.</span><span class="sxs-lookup"><span data-stu-id="6095d-121">Type how often passwords should expire.</span></span> <span data-ttu-id="6095d-122">Choisissez un nombre de jours compris entre 14 et 730.</span><span class="sxs-lookup"><span data-stu-id="6095d-122">Choose a number of days from 14 to 730.</span></span>
  
6. <span data-ttu-id="6095d-123">Dans la seconde zone, indiquez à quel moment les utilisateurs doivent être avisés de l'expiration prochaine du mot de passe, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6095d-123">In the second box type when users are notified that their password will expire, and then select **Save**.</span></span> <span data-ttu-id="6095d-124">Choisissez un nombre de jours compris entre 1 et 30.</span><span class="sxs-lookup"><span data-stu-id="6095d-124">Choose a number of days from 1 to 30.</span></span>
    
7. <span data-ttu-id="6095d-125">Lorsque le mot de passe de l’utilisateur expire, ce dernier reçoit une notification qui s’affiche dans le coin inférieur droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="6095d-125">When the user's password expires, they'll get a notification that appears in the lower right corner of their screen.</span></span>
  
## <a name="important-things-you-need-to-know-about-the-password-expiration-feature"></a><span data-ttu-id="6095d-126">Points importants dont vous devez tenir compte concernant la fonctionnalité d’expiration de mot de passe</span><span class="sxs-lookup"><span data-stu-id="6095d-126">Important things you need to know about the password expiration feature</span></span>

<span data-ttu-id="6095d-127">Voici quelques points dont vous devez tenir compte concernant le fonctionnement actuel de cette fonctionnalité à compter du mois de janvier 2018 :</span><span class="sxs-lookup"><span data-stu-id="6095d-127">Here are some things to know about how this feature currently works as of January 2018:</span></span>
  
- <span data-ttu-id="6095d-p107">Les personnes qui utilisent uniquement l’application Outlook ne sont pas obligées de réinitialiser leur mot de passe Microsoft 365 tant que ce dernier n’a pas expiré dans le cache. Cela peut se produire quelques jours après la date d’expiration. Il n’existe aucune solution de contournement à ce problème pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="6095d-p107">People who only use the Outlook app won't be forced to reset their Microsoft 365 password until it expires in the cache. This can be several days after the actual expiration date. There's no workaround for this at the admin level.</span></span>
    
- <span data-ttu-id="6095d-p108">Les utilisateurs ne reçoivent pas de notification par courrier indiquant que leur mot de passe expire dans X jours. Voulez-vous utiliser cette fonctionnalité ? **[Votez ici !](https://office365.uservoice.com/forums/273493-office-365-admin/suggestions/15028344-office-365-password-email-notification)**</span><span class="sxs-lookup"><span data-stu-id="6095d-p108">Users do not get an email notification that their password is going to expire in X number of days. Do you want this feature? **[Vote here!](https://office365.uservoice.com/forums/273493-office-365-admin/suggestions/15028344-office-365-password-email-notification)**</span></span>
    
## <a name="prevent-last-password-from-being-used-again"></a><span data-ttu-id="6095d-134">Empêcher la réutilisation du dernier mot de passe</span><span class="sxs-lookup"><span data-stu-id="6095d-134">Prevent last password from being used again</span></span>

<span data-ttu-id="6095d-135">Si vous le souhaitez, vous pouvez empêcher vos utilisateurs de recycler d’anciens mots de passe en appliquant l’historique de mot de passe dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6095d-135">If you want to prevent your users from recycling old passwords, you can do so by enforcing password history in Azure AD.</span></span> <span data-ttu-id="6095d-136">Voir [Créer une stratégie de mot de passe personnalisée](https://docs.microsoft.com/azure/active-directory-domain-services/password-policy#create-a-custom-password-policy).</span><span class="sxs-lookup"><span data-stu-id="6095d-136">See [Create a custom password policy](https://docs.microsoft.com/azure/active-directory-domain-services/password-policy#create-a-custom-password-policy).</span></span>

## <a name="synchronize-user-passwords-hashes-from-an-on-premises-active-directory-to-azure-ad-microsoft-365"></a><span data-ttu-id="6095d-137">Synchroniser les hachages de mots de passe utilisateur à partir d’une instance Active Directory locale vers une instance Azure AD (Microsoft 365)</span><span class="sxs-lookup"><span data-stu-id="6095d-137">Synchronize user passwords hashes from an on-premises Active Directory to Azure AD (Microsoft 365)</span></span>

<span data-ttu-id="6095d-138">Cet article est consacré à la définition de la stratégie d’expiration pour les utilisateurs exclusivement cloud (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="6095d-138">This article is for setting the expiration policy for cloud-only users (Azure AD).</span></span> <span data-ttu-id="6095d-139">Il ne s’applique pas aux utilisateurs d’identité hybride utilisant la synchronisation par hachage du mot de passe, l’authentification directe ou la fédération locale telle que ADFS.</span><span class="sxs-lookup"><span data-stu-id="6095d-139">It doesn't apply to hybrid identity users who use password hash sync, pass-through authentication, or on-premises federation like ADFS.</span></span>
  
<span data-ttu-id="6095d-140">Pour découvrir comment synchroniser les hachages de mot de passe utilisateur d'Active Directory local avec Azure Active Directory, voir [Implémenter la synchronisation du hachage de mot de passe avec la synchronisation Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization).</span><span class="sxs-lookup"><span data-stu-id="6095d-140">To learn how to synchronize user password hashes from on premises AD to Azure AD, see [Implement password hash synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization).</span></span>


## <a name="update-password-policy"></a><span data-ttu-id="6095d-141">Mise à jour de la stratégie de mot de passe</span><span class="sxs-lookup"><span data-stu-id="6095d-141">Update password Policy</span></span>

<span data-ttu-id="6095d-142">L’applet de commande Set-MsolPasswordPolicy met à jour la stratégie de mot de passe d’un domaine ou d’un client spécifié.</span><span class="sxs-lookup"><span data-stu-id="6095d-142">The Set-MsolPasswordPolicy cmdlet updates the password policy of a specified domain or tenant.</span></span> <span data-ttu-id="6095d-143">Deux paramètres sont requis. La premier consiste à indiquer la durée pendant laquelle un mot de passe reste valide avant qu’il ne soit modifié et que le deuxième indique le nombre de jours avant la date d’expiration du mot de passe qui s’affiche lorsque les utilisateurs reçoivent la première notification leur indiquant que leur mot de passe arrive bientôt à expiration.</span><span class="sxs-lookup"><span data-stu-id="6095d-143">Two settings are required; the first is to indicate the length of time that a password remains valid before it must be changed and the second is to indicate the number of days before the password expiration date that will trigger when users will receive their first notification that their password will soon expire.</span></span>

<span data-ttu-id="6095d-144">Si vous souhaitez obtenir plus d’informations sur la mise à jour de la stratégie de mot de passe pour un domaine ou un client spécifique, consultez [Set-MsolPasswordPolicy](https://docs.microsoft.com/powershell/module/msonline/set-msolpasswordpolicy?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="6095d-144">To learn how to update password policy for a specific domain or tenant, see [Set-MsolPasswordPolicy](https://docs.microsoft.com/powershell/module/msonline/set-msolpasswordpolicy?view=azureadps-1.0).</span></span>
