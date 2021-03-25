---
title: Conditions préalables à l’accès identité et appareil pour l’authentification directe dans votre environnement de test Microsoft 365
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Créer un environnement Microsoft 365 pour tester l’accès identité et appareil avec les conditions préalables pour l’authentification directe.
ms.openlocfilehash: f257b85672a1a1b27f600d145b1f9f3296b21980
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51199848"
---
# <a name="identity-and-device-access-prerequisites-for-pass-through-authentication-in-your-microsoft-365-test-environment"></a><span data-ttu-id="2b998-103">Conditions préalables à l’accès identité et appareil pour l’authentification directe dans votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2b998-103">Identity and device access prerequisites for pass-through authentication in your Microsoft 365 test environment</span></span>

<span data-ttu-id="2b998-104">*Ce guide de laboratoire de test ne peut être utilisé que pour les environnements de test Microsoft 365 pour les entreprises.*</span><span class="sxs-lookup"><span data-stu-id="2b998-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="2b998-105">Les configurations d’accès aux [identités](../security/office-365-security/microsoft-365-policies-configurations.md) et appareils sont un ensemble de configurations et de stratégies d’accès conditionnel pour protéger l’accès à tous les services de Microsoft 365 pour les entreprises intégrés à Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="2b998-105">[Identity and device access configurations](../security/office-365-security/microsoft-365-policies-configurations.md) are a set of configurations and conditional access policies to protect access to all services in Microsoft 365 for enterprise that are integrated with Azure Active Directory (Azure AD).</span></span>

<span data-ttu-id="2b998-106">Cet article décrit comment configurer un environnement de test Microsoft 365 qui respecte la configuration requise de la [configuration préalable de l’authentification directe](../security/office-365-security/identity-access-prerequisites.md#prerequisites) pour l’accès identité et appareil.</span><span class="sxs-lookup"><span data-stu-id="2b998-106">This article describes how you can configure a Microsoft 365 test environment that meets the requirements of the [Pass-through authentication prerequisite configuration](../security/office-365-security/identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span>

<span data-ttu-id="2b998-107">La configuration de cet environnement de test se fait en dix phases :</span><span class="sxs-lookup"><span data-stu-id="2b998-107">There are ten phases to setting up this test environment:</span></span>

1. <span data-ttu-id="2b998-108">Construire votre entreprise simulée avec environnement de test authentification directe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2b998-108">Build out your simulated enterprise with pass-through authentication Microsoft 365 test environment</span></span>
2. <span data-ttu-id="2b998-109">Configurer l’authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="2b998-109">Configure Azure AD seamless single sign-on</span></span>
3. <span data-ttu-id="2b998-110">Configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="2b998-110">Configure named locations</span></span>
4. <span data-ttu-id="2b998-111">Configurer l’écriture différée du mot de passe</span><span class="sxs-lookup"><span data-stu-id="2b998-111">Configure password writeback</span></span>
5. <span data-ttu-id="2b998-112">Configurer la réinitialisation du mot de passe libre-service</span><span class="sxs-lookup"><span data-stu-id="2b998-112">Configure self-service password reset</span></span>
6. <span data-ttu-id="2b998-113">Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="2b998-113">Configure multifactor authentication</span></span>
7. <span data-ttu-id="2b998-114">Activer l’inscription automatique des ordinateurs Windows joints à un domaine</span><span class="sxs-lookup"><span data-stu-id="2b998-114">Enable automatic device registration of domain-joined Windows computers</span></span>
8. <span data-ttu-id="2b998-115">Configurer la protection par mot de passe Azure AD</span><span class="sxs-lookup"><span data-stu-id="2b998-115">Configure Azure AD password protection</span></span> 
9. <span data-ttu-id="2b998-116">Activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="2b998-116">Enable Azure AD Identity Protection</span></span>
10. <span data-ttu-id="2b998-117">Activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="2b998-117">Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

## <a name="phase-1-build-out-your-simulated-enterprise-with-pass-through-authentication-microsoft-365-test-environment"></a><span data-ttu-id="2b998-118">Étape 1 : construire votre entreprise simulée avec environnement de test authentification directe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2b998-118">Phase 1: Build out your simulated enterprise with pass-through authentication Microsoft 365 test environment</span></span>

<span data-ttu-id="2b998-119">Procédez comme suit pour déployer l’[authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2b998-119">Follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>

<span data-ttu-id="2b998-120">Voici la configuration obtenue.</span><span class="sxs-lookup"><span data-stu-id="2b998-120">Here is the resulting configuration.</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](../media/pass-through-auth-m365-ent-test-environment/Phase2.png)
 
## <a name="phase-2-configure-azure-ad-seamless-single-sign-on"></a><span data-ttu-id="2b998-122">Étape 2 : configurer l’authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="2b998-122">Phase 2: Configure Azure AD seamless single sign-on</span></span>

<span data-ttu-id="2b998-123">Suivez les instructions de [Phase 2 du guide laboratoire test de l’authentification transparente unique Azure AD](single-sign-on-m365-ent-test-environment.md#phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso).</span><span class="sxs-lookup"><span data-stu-id="2b998-123">Follow the instructions in [Phase 2 of the Azure AD Seamless Single Sign-on Test Lab Guide](single-sign-on-m365-ent-test-environment.md#phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso).</span></span>

## <a name="phase-3-configure-named-locations"></a><span data-ttu-id="2b998-124">Étape 3 : configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="2b998-124">Phase 3: Configure named locations</span></span>

<span data-ttu-id="2b998-125">Tout d’abord, déterminer les adresses IP publiques ou les plages d’adresse utilisées par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2b998-125">First, determine the public IP addresses or address ranges used by your organization.</span></span>

<span data-ttu-id="2b998-126">Ensuite, suivez les instructions de [configurer des emplacements nommé dans Azure Active Directory](/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) pour ajouter les adresses ou les plages d’adresses comme emplacements nommés.</span><span class="sxs-lookup"><span data-stu-id="2b998-126">Next, follow the instructions in [Configure named locations in Azure Active Directory](/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) to add the addresses or address ranges as named locations.</span></span> 

## <a name="phase-4-configure-password-writeback"></a><span data-ttu-id="2b998-127">Étape 4 : configurer l’écriture différée du mot de passe</span><span class="sxs-lookup"><span data-stu-id="2b998-127">Phase 4: Configure password writeback</span></span>

<span data-ttu-id="2b998-128">Suivez les instructions dans [Phase 2 du guide de laboratoire de test réinitialisation de mot de passe](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span><span class="sxs-lookup"><span data-stu-id="2b998-128">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span></span>

## <a name="phase-5-configure-self-service-password-reset"></a><span data-ttu-id="2b998-129">Étape 5 : configurer la réinitialisation du mot de passe libre-service</span><span class="sxs-lookup"><span data-stu-id="2b998-129">Phase 5: Configure self-service password reset</span></span>

<span data-ttu-id="2b998-130">Suivez les instructions du Guide de laboratoire de Test dans la [Phase 3 de la réinitialisation de mot de passe](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span><span class="sxs-lookup"><span data-stu-id="2b998-130">Follow the instructions in [Phase 3 of the password reset Test Lab Guide](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span></span> 

<span data-ttu-id="2b998-131">Lors de l’activation de réinitialisation de mot de passe pour les comptes dans un groupe Azure AD spécifique, ajoutez ces comptes au groupe **réinitialiser le mot de passe**:</span><span class="sxs-lookup"><span data-stu-id="2b998-131">When enabling password reset for the accounts in a specific Azure AD group, add these accounts to the **Password reset** group:</span></span>

- <span data-ttu-id="2b998-132">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="2b998-132">User 2</span></span>
- <span data-ttu-id="2b998-133">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="2b998-133">User 3</span></span>
- <span data-ttu-id="2b998-134">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="2b998-134">User 4</span></span>
- <span data-ttu-id="2b998-135">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="2b998-135">User 5</span></span>

<span data-ttu-id="2b998-136">Testez la réinitialisation de mot de passe pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="2b998-136">Test password reset only for the User 2 account.</span></span>

## <a name="phase-6-configure-multi-factor-authentication"></a><span data-ttu-id="2b998-137">Étape 6 : configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="2b998-137">Phase 6: Configure multi-factor authentication</span></span>

<span data-ttu-id="2b998-138">Suivez les instructions de [Phase 2 de Guide de laboratoire de Test authentification multifacteur ](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) pour les comptes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="2b998-138">Follow the instructions in [Phase 2 of the multi-factor authentication Test Lab Guide](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) for the following user accounts:</span></span>

- <span data-ttu-id="2b998-139">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="2b998-139">User 2</span></span>
- <span data-ttu-id="2b998-140">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="2b998-140">User 3</span></span>
- <span data-ttu-id="2b998-141">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="2b998-141">User 4</span></span>
- <span data-ttu-id="2b998-142">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="2b998-142">User 5</span></span>

<span data-ttu-id="2b998-143">Testez l’authentification multifacteur uniquement pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="2b998-143">Test multi-factor authentication only for the User 2 account.</span></span>

## <a name="phase-7-enable-automatic-device-registration-of-domain-joined-windows-computers"></a><span data-ttu-id="2b998-144">Phase 7 : Activer l’inscription automatique d’appareils d’ordinateurs Windows joints à un domaine</span><span class="sxs-lookup"><span data-stu-id="2b998-144">Phase 7: Enable automatic device registration of domain-joined Windows computers</span></span> 

<span data-ttu-id="2b998-145">Suivez [ces instructions pour](/azure/active-directory/devices/hybrid-azuread-join-plan) activer l’inscription automatique des ordinateurs Windows joints à un domaine.</span><span class="sxs-lookup"><span data-stu-id="2b998-145">Follow [these instructions](/azure/active-directory/devices/hybrid-azuread-join-plan) to enable automatic device registration of domain-joined Windows computers.</span></span>

## <a name="phase-8-configure-azure-ad-password-protection"></a><span data-ttu-id="2b998-146">Phase 8 : Configurer la protection par mot de passe Azure AD</span><span class="sxs-lookup"><span data-stu-id="2b998-146">Phase 8: Configure Azure AD password protection</span></span> 

<span data-ttu-id="2b998-147">Suivez [ces instructions pour](/azure/active-directory/authentication/concept-password-ban-bad) bloquer les mots de passe faibles connus et leurs variantes.</span><span class="sxs-lookup"><span data-stu-id="2b998-147">Follow [these instructions](/azure/active-directory/authentication/concept-password-ban-bad) to block known weak passwords and their variants.</span></span>

## <a name="phase-9-enable-azure-ad-identity-protection"></a><span data-ttu-id="2b998-148">Phase 9 : Activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="2b998-148">Phase 9: Enable Azure AD Identity Protection</span></span>

<span data-ttu-id="2b998-149">Suivez les instructions de [Étape 2 du Guide de laboratoire de Test Azure AD Identity Protection](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-use-azure-ad-identity-protection).</span><span class="sxs-lookup"><span data-stu-id="2b998-149">Follow the instructions in [Phase 2 of the Azure AD Identity Protection Test Lab Guide](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-use-azure-ad-identity-protection).</span></span> 

## <a name="phase-10-enable-modern-authentication-for-exchange-online-and-skype-for-business-online"></a><span data-ttu-id="2b998-150">Phase 10 : Activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="2b998-150">Phase 10: Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

<span data-ttu-id="2b998-151">Pour Exchange Online, suivez [ces instructions](/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span><span class="sxs-lookup"><span data-stu-id="2b998-151">For Exchange Online, follow [these instructions](/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span></span> 

<span data-ttu-id="2b998-152">Pour Skype Entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="2b998-152">For Skype for Business Online:</span></span>

1. <span data-ttu-id="2b998-153">Se connecter à [Skype Entreprise Online](/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="2b998-153">Connect to [Skype for Business Online](/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

2. <span data-ttu-id="2b998-154">Exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="2b998-154">Run this command.</span></span>

  ```powershell
  Set-CsOAuthConfiguration -ClientAdalAuthOverride Allowed
  ```

3. <span data-ttu-id="2b998-155">Vérifiez que la modification a été appliquée avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="2b998-155">Verify that the change was successful with this command.</span></span>

  ```powershell
  Get-CsOAuthConfiguration
  ```

<span data-ttu-id="2b998-156">Le résultat est un environnement de test qui respecte la configuration requise de la [configuration préalable de l’authentification directe](../security/office-365-security/identity-access-prerequisites.md#prerequisites) pour l’accès identité et appareil.</span><span class="sxs-lookup"><span data-stu-id="2b998-156">The result is a test environment that meets the requirements of the [Pass-through authentication prerequisite configuration](../security/office-365-security/identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span> 

## <a name="next-step"></a><span data-ttu-id="2b998-157">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2b998-157">Next step</span></span>

<span data-ttu-id="2b998-158">Utilisez [Stratégies d’accès courantes identité et appareil](../security/office-365-security/identity-access-policies.md) pour configurer les stratégies qui se basent sur les conditions préalables et protègent identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="2b998-158">Use [Common identity and device access policies](../security/office-365-security/identity-access-policies.md) to configure the policies that build on the prerequisites and protect identities and devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b998-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b998-159">See also</span></span>

[<span data-ttu-id="2b998-160">Guides de laboratoire de Test Autres identités</span><span class="sxs-lookup"><span data-stu-id="2b998-160">Additional identity Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md#identity)

[<span data-ttu-id="2b998-161">Feuille de route des identités</span><span class="sxs-lookup"><span data-stu-id="2b998-161">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="2b998-162">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="2b998-162">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="2b998-163">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="2b998-163">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="2b998-164">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="2b998-164">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)
