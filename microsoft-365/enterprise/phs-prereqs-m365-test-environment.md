---
title: Conditions préalables d’accès aux identités et appareils pour la synchronisation du hachage du mot de passe dans votre environnement de test Microsoft 365
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
ms.date: 12/12/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Créez un environnement Microsoft 365 pour tester l’accès aux identités et appareils avec les conditions préalables applicables à l’authentification de la synchronisation du hachage du mot de passe.
ms.openlocfilehash: 63f433d5297139fcc7f6eb8bd5383a6593c29388
ms.sourcegitcommit: cd17328baa58448214487e3e68c37590ab9fd08d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48399442"
---
# <a name="identity-and-device-access-prerequisites-for-password-hash-synchronization-in-your-microsoft-365-test-environment"></a><span data-ttu-id="c6ba5-103">Conditions préalables d’accès aux identités et appareils pour la synchronisation du hachage du mot de passe dans votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="c6ba5-103">Identity and device access prerequisites for password hash synchronization in your Microsoft 365 test environment</span></span>

<span data-ttu-id="c6ba5-104">*Ce guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="c6ba5-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="c6ba5-105">Les [configurations d’identité et d’accès aux appareils](../security/office-365-security/microsoft-365-policies-configurations.md) sont un ensemble de configurations et de stratégies d’accès conditionnel permettant de protéger l’accès à tous les services de Microsoft 365 pour les entreprises qui sont intégrés à Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c6ba5-105">[Identity and device access configurations](../security/office-365-security/microsoft-365-policies-configurations.md) are a set of configurations and conditional access policies to protect access to all services in Microsoft 365 for enterprise that are integrated with Azure Active Directory (Azure AD).</span></span>

<span data-ttu-id="c6ba5-106">Cet article décrit comment configurer un environnement de test Microsoft 365 qui respecte les exigences de [configuration préalable de synchronisation du hachage du mot de passe Active Directory](../security/office-365-security/identity-access-prerequisites.md#prerequisites) pour l’accès aux identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="c6ba5-106">This article describes how to configure a Microsoft 365 test environment that meets the requirements of the [Active Directory with password hash sync prerequisite configuration](../security/office-365-security/identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span>

<span data-ttu-id="c6ba5-107">La configuration de cet environnement de test comprend huit étapes :</span><span class="sxs-lookup"><span data-stu-id="c6ba5-107">There are eight phases to setting up this test environment:</span></span>

1.  <span data-ttu-id="c6ba5-108">Créer une entreprise simulée avec un environnement de test de synchronisation du hachage du mot de passe</span><span class="sxs-lookup"><span data-stu-id="c6ba5-108">Create a simulated enterprise with password hash sync test environment</span></span>
2.  <span data-ttu-id="c6ba5-109">Configurer l’authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="c6ba5-109">Configure Azure AD seamless single sign-on</span></span>
3.  <span data-ttu-id="c6ba5-110">Configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="c6ba5-110">Configure named locations</span></span>
4.  <span data-ttu-id="c6ba5-111">Configurer la réécriture du mot de passe</span><span class="sxs-lookup"><span data-stu-id="c6ba5-111">Configure password writeback</span></span>
5.  <span data-ttu-id="c6ba5-112">Configurer la réinitialisation de mot de passe en libre-service pour tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6ba5-112">Configure self-service password reset for all user accounts</span></span>
6.  <span data-ttu-id="c6ba5-113">Configurer l’authentification multifacteur pour tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6ba5-113">Configure multifactor authentication for all user accounts</span></span>
7.  <span data-ttu-id="c6ba5-114">Activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="c6ba5-114">Enable Azure AD Identity Protection</span></span>
8.  <span data-ttu-id="c6ba5-115">Activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="c6ba5-115">Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

## <a name="phase-1-build-out-your-simulated-enterprise-with-password-hash-sync-microsoft-365-test-environment"></a><span data-ttu-id="c6ba5-116">Étape 1 : Construire votre entreprise simulée avec un environnement de test Microsoft 365 pour la synchronisation du hachage du mot de passe</span><span class="sxs-lookup"><span data-stu-id="c6ba5-116">Phase 1: Build out your simulated enterprise with password hash sync Microsoft 365 test environment</span></span>

<span data-ttu-id="c6ba5-117">Suivez les instructions de [Synchronisation du hachage du mot de passe](password-hash-sync-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c6ba5-117">Follow the instructions in [Password hash synchronization](password-hash-sync-m365-ent-test-environment.md).</span></span>
<span data-ttu-id="c6ba5-118">Voici la configuration obtenue.</span><span class="sxs-lookup"><span data-stu-id="c6ba5-118">Here is the resulting configuration.</span></span>

![Entreprise simulée avec environnement de test de synchronisation du hachage du mot de passe](../media/password-hash-sync-m365-ent-test-environment/Phase3.png)
 
## <a name="phase-2-configure-azure-ad-seamless-single-sign-on"></a><span data-ttu-id="c6ba5-120">Étape 2 : Configurer l’authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="c6ba5-120">Phase 2: Configure Azure AD seamless single sign-on</span></span>

<span data-ttu-id="c6ba5-121">Suivez les instructions de [Phase 2 du guide laboratoire test de l’authentification transparente unique Azure AD](single-sign-on-m365-ent-test-environment.md#phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso).</span><span class="sxs-lookup"><span data-stu-id="c6ba5-121">Follow the instructions in [Phase 2 of the Azure AD Seamless Single Sign-on Test Lab Guide](single-sign-on-m365-ent-test-environment.md#phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso).</span></span>

## <a name="phase-3-configure-named-locations"></a><span data-ttu-id="c6ba5-122">Étape 3 : configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="c6ba5-122">Phase 3: Configure named locations</span></span>

<span data-ttu-id="c6ba5-123">Tout d’abord, déterminer les adresses IP publiques ou les plages d’adresse utilisées par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c6ba5-123">First, determine the public IP addresses or address ranges used by your organization.</span></span>

<span data-ttu-id="c6ba5-124">Ensuite, suivez les instructions de [configurer des emplacements nommé dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) pour ajouter les adresses ou les plages d’adresses comme emplacements nommés.</span><span class="sxs-lookup"><span data-stu-id="c6ba5-124">Next, follow the instructions in [Configure named locations in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) to add the addresses or address ranges as named locations.</span></span> 

## <a name="phase-4-configure-password-writeback"></a><span data-ttu-id="c6ba5-125">Étape 4 : configurer l’écriture différée du mot de passe</span><span class="sxs-lookup"><span data-stu-id="c6ba5-125">Phase 4: Configure password writeback</span></span>

<span data-ttu-id="c6ba5-126">Suivez les instructions dans [Phase 2 du guide de laboratoire de test réinitialisation de mot de passe](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span><span class="sxs-lookup"><span data-stu-id="c6ba5-126">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span></span>

## <a name="phase-5-configure-self-service-password-reset"></a><span data-ttu-id="c6ba5-127">Étape 5 : configurer la réinitialisation du mot de passe libre-service</span><span class="sxs-lookup"><span data-stu-id="c6ba5-127">Phase 5: Configure self-service password reset</span></span>

<span data-ttu-id="c6ba5-128">Suivez les instructions du Guide de laboratoire de Test dans la [Phase 3 de la réinitialisation de mot de passe](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span><span class="sxs-lookup"><span data-stu-id="c6ba5-128">Follow the instructions in [Phase 3 of the password reset Test Lab Guide](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span></span> 

<span data-ttu-id="c6ba5-129">Lors de l’activation de réinitialisation de mot de passe pour les comptes dans un groupe Azure AD spécifique, ajoutez ces comptes au groupe **réinitialiser le mot de passe**:</span><span class="sxs-lookup"><span data-stu-id="c6ba5-129">When enabling password reset for the accounts in a specific Azure AD group, add these accounts to the **Password reset** group:</span></span>

- <span data-ttu-id="c6ba5-130">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="c6ba5-130">User 2</span></span>
- <span data-ttu-id="c6ba5-131">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="c6ba5-131">User 3</span></span>
- <span data-ttu-id="c6ba5-132">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="c6ba5-132">User 4</span></span>
- <span data-ttu-id="c6ba5-133">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="c6ba5-133">User 5</span></span>

<span data-ttu-id="c6ba5-134">Testez la réinitialisation de mot de passe pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="c6ba5-134">Test password reset only for the User 2 account.</span></span>

## <a name="phase-6-configure-multi-factor-authentication"></a><span data-ttu-id="c6ba5-135">Étape 6 : configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="c6ba5-135">Phase 6: Configure multi-factor authentication</span></span>

<span data-ttu-id="c6ba5-136">Suivez les instructions de [Phase 2 de Guide de laboratoire de Test authentification multifacteur ](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) pour les comptes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="c6ba5-136">Follow the instructions in [Phase 2 of the multi-factor authentication Test Lab Guide](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) for the following user accounts:</span></span>

- <span data-ttu-id="c6ba5-137">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="c6ba5-137">User 2</span></span>
- <span data-ttu-id="c6ba5-138">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="c6ba5-138">User 3</span></span>
- <span data-ttu-id="c6ba5-139">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="c6ba5-139">User 4</span></span>
- <span data-ttu-id="c6ba5-140">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="c6ba5-140">User 5</span></span>

<span data-ttu-id="c6ba5-141">Testez l’authentification multifacteur uniquement pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="c6ba5-141">Test multi-factor authentication only for the User 2 account.</span></span>

## <a name="phase-7-enable-azure-ad-identity-protection"></a><span data-ttu-id="c6ba5-142">Étape 7 : activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="c6ba5-142">Phase 7: Enable Azure AD Identity Protection</span></span>

<span data-ttu-id="c6ba5-143">Suivez les instructions de [Étape 2 du guide laboratoire test de l’authentification transparente unique Azure AD](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-use-azure-ad-identity-protection).</span><span class="sxs-lookup"><span data-stu-id="c6ba5-143">Follow the instructions in [Phase 2 of the Azure AD Identity Protection Test Lab Guide](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-use-azure-ad-identity-protection).</span></span> 

## <a name="phase-8-enable-modern-authentication-for-exchange-online-and-skype-for-business-online"></a><span data-ttu-id="c6ba5-144">Étape 8 : activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="c6ba5-144">Phase 8: Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

<span data-ttu-id="c6ba5-145">Pour Exchange Online, suivez [ces instructions](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span><span class="sxs-lookup"><span data-stu-id="c6ba5-145">For Exchange Online, follow [these instructions](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span></span> 

<span data-ttu-id="c6ba5-146">Pour Skype Entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="c6ba5-146">For Skype for Business Online:</span></span>

1. <span data-ttu-id="c6ba5-147">Se connecter à [Skype Entreprise Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="c6ba5-147">Connect to [Skype for Business Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

2. <span data-ttu-id="c6ba5-148">Exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="c6ba5-148">Run this command.</span></span>

  ```powershell
  Set-CsOAuthConfiguration -ClientAdalAuthOverride Allowed
  ```

3. <span data-ttu-id="c6ba5-149">Vérifiez que la commande a correctement appliqué la modification.</span><span class="sxs-lookup"><span data-stu-id="c6ba5-149">Verify that the change was successful with this command.</span></span>

  ```powershell
  Get-CsOAuthConfiguration
  ```

<span data-ttu-id="c6ba5-150">Le résultat est un environnement de test conforme aux exigences de [configuration préalable de synchronisation du hachage du mot de passe Active Directory](../security/office-365-security/identity-access-prerequisites.md#prerequisites) pour l’accès aux identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="c6ba5-150">The result is a test environment that meets the requirements of the [Active Directory with password hash sync prerequisite configuration](../security/office-365-security/identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span> 

## <a name="next-step"></a><span data-ttu-id="c6ba5-151">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="c6ba5-151">Next step</span></span>

<span data-ttu-id="c6ba5-152">Utilisez [Stratégies d’accès courantes identité et appareil](identity-access-policies.md) pour configurer les stratégies qui se basent sur les conditions préalables et protègent identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="c6ba5-152">Use [Common identity and device access policies](identity-access-policies.md) to configure the policies that build on the prerequisites and protect identities and devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6ba5-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6ba5-153">See also</span></span>

[<span data-ttu-id="c6ba5-154">Guides de laboratoire de Test Autres identités</span><span class="sxs-lookup"><span data-stu-id="c6ba5-154">Additional identity Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md#identity)

[<span data-ttu-id="c6ba5-155">Feuille de route d’identité</span><span class="sxs-lookup"><span data-stu-id="c6ba5-155">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="c6ba5-156">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="c6ba5-156">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="c6ba5-157">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="c6ba5-157">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="c6ba5-158">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="c6ba5-158">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
