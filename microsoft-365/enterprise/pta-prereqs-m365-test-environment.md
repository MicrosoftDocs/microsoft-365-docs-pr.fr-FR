---
title: Conditions préalables à l’accès identité et appareil pour l’authentification directe dans votre environnement de test Microsoft 365
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 04/23/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Créer un environnement Microsoft 365 pour tester l’accès identité et appareil avec les conditions préalables pour l’authentification directe.
ms.openlocfilehash: 348885b2cc7a0d6134dce49cd0a2a39706c5e71d
ms.sourcegitcommit: 1d376287f6c1bf5174873e89ed4bf7bb15bc13f6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38627488"
---
# <a name="identity-and-device-access-prerequisites-for-pass-through-authentication-in-your-microsoft-365-test-environment"></a><span data-ttu-id="2adca-103">Conditions préalables à l’accès identité et appareil pour l’authentification directe dans votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2adca-103">Identity and device access prerequisites for pass-through authentication in your Microsoft 365 test environment</span></span>

<span data-ttu-id="2adca-104">Les [Configurations d’accès identité et appareil](microsoft-365-policies-configurations.md) sont un ensemble de configurations et stratégies d’accès conditionnel pour protéger l’accès à tous les services qui sont intégrés avec Azure Active Directory (Azure AD), y compris Office 365 et Enterprise Mobility + Security (EMS) dans Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="2adca-104">[Identity and device access configurations](microsoft-365-policies-configurations.md) are a set of configurations and conditional access policies to protect access to all services that are integrated with Azure Active Directory (Azure AD), including Office 365 and Enterprise Mobility + Security (EMS) in Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="2adca-105">Cet article décrit comment configurer un environnement de test Microsoft 365 qui respecte la configuration requise de la [configuration préalable de l’authentification directe](identity-access-prerequisites.md#prerequisites) pour l’accès identité et appareil.</span><span class="sxs-lookup"><span data-stu-id="2adca-105">This article describes how you can configure a Microsoft 365 test environment that meets the requirements of the [Pass-through authentication prerequisite configuration](identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span>

<span data-ttu-id="2adca-106">Il y a huit phases de configuration de cet environnement de test :</span><span class="sxs-lookup"><span data-stu-id="2adca-106">There are eight phases to setting up this test environment:</span></span>

1.  <span data-ttu-id="2adca-107">Construire votre entreprise simulée avec environnement de test authentification directe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2adca-107">Build out your simulated enterprise with pass-through authentication Microsoft 365 test environment</span></span>
2.  <span data-ttu-id="2adca-108">Configurer l’authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="2adca-108">Configure Azure AD seamless single sign-on</span></span>
3.  <span data-ttu-id="2adca-109">Configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="2adca-109">Configure named locations</span></span>
4.  <span data-ttu-id="2adca-110">Configurer l’écriture différée du mot de passe</span><span class="sxs-lookup"><span data-stu-id="2adca-110">Configure password writeback</span></span>
5.  <span data-ttu-id="2adca-111">Configurer la réinitialisation du mot de passe libre-service</span><span class="sxs-lookup"><span data-stu-id="2adca-111">Configure self-service password reset</span></span>
6.  <span data-ttu-id="2adca-112">Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="2adca-112">Configure multifactor authentication</span></span>
7.  <span data-ttu-id="2adca-113">Activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="2adca-113">Enable Azure AD Identity Protection</span></span>
8.  <span data-ttu-id="2adca-114">Activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="2adca-114">Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

## <a name="phase-1-build-out-your-simulated-enterprise-with-pass-through-authentication-microsoft-365-test-environment"></a><span data-ttu-id="2adca-115">Étape 1 : construire votre entreprise simulée avec environnement de test authentification directe Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2adca-115">Phase 1: Build out your simulated enterprise with pass-through authentication Microsoft 365 test environment</span></span>

<span data-ttu-id="2adca-116">Procédez comme suit pour déployer l’[authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2adca-116">Follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>

<span data-ttu-id="2adca-117">Voici la configuration obtenue.</span><span class="sxs-lookup"><span data-stu-id="2adca-117">Here is the resulting configuration.</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](media/pass-through-auth-m365-ent-test-environment/Phase2.png)
 
## <a name="phase-2-configure-azure-ad-seamless-single-sign-on"></a><span data-ttu-id="2adca-119">Étape 2 : configurer l’authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="2adca-119">Phase 2: Configure Azure AD seamless single sign-on</span></span>

<span data-ttu-id="2adca-120">Suivez les instructions de [Phase 2 du guide laboratoire test de l’authentification transparente unique Azure AD](single-sign-on-m365-ent-test-environment.md#phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso).</span><span class="sxs-lookup"><span data-stu-id="2adca-120">Follow the instructions in [Phase 2 of the Azure AD Seamless Single Sign-on Test Lab Guide](single-sign-on-m365-ent-test-environment.md#phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso).</span></span>

## <a name="phase-3-configure-named-locations"></a><span data-ttu-id="2adca-121">Étape 3 : configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="2adca-121">Phase 3: Configure named locations</span></span>

<span data-ttu-id="2adca-122">Tout d’abord, déterminer les adresses IP publiques ou les plages d’adresse utilisées par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2adca-122">First, determine the public IP addresses or address ranges used by your organization.</span></span>

<span data-ttu-id="2adca-123">Ensuite, suivez les instructions de [configurer des emplacements nommé dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) pour ajouter les adresses ou les plages d’adresses comme emplacements nommés.</span><span class="sxs-lookup"><span data-stu-id="2adca-123">Next, follow the instructions in [Configure named locations in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) to add the addresses or address ranges as named locations.</span></span> 

## <a name="phase-4-configure-password-writeback"></a><span data-ttu-id="2adca-124">Étape 4 : configurer l’écriture différée du mot de passe</span><span class="sxs-lookup"><span data-stu-id="2adca-124">Phase 4: Configure password writeback</span></span>

<span data-ttu-id="2adca-125">Suivez les instructions dans [Phase 2 du guide de laboratoire de test réinitialisation de mot de passe](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span><span class="sxs-lookup"><span data-stu-id="2adca-125">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span></span>

## <a name="phase-5-configure-self-service-password-reset"></a><span data-ttu-id="2adca-126">Étape 5 : configurer la réinitialisation du mot de passe libre-service</span><span class="sxs-lookup"><span data-stu-id="2adca-126">Phase 5: Configure self-service password reset</span></span>

<span data-ttu-id="2adca-127">Suivez les instructions du Guide de laboratoire de Test dans la [Phase 3 de la réinitialisation de mot de passe](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span><span class="sxs-lookup"><span data-stu-id="2adca-127">Follow the instructions in [Phase 3 of the password reset Test Lab Guide](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span></span> 

<span data-ttu-id="2adca-128">Lors de l’activation de réinitialisation de mot de passe pour les comptes dans un groupe Azure AD spécifique, ajoutez ces comptes au groupe **réinitialiser le mot de passe**:</span><span class="sxs-lookup"><span data-stu-id="2adca-128">When enabling password reset for the accounts in a specific Azure AD group, add these accounts to the **Password reset** group:</span></span>

- <span data-ttu-id="2adca-129">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="2adca-129">User 2</span></span>
- <span data-ttu-id="2adca-130">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="2adca-130">User 3</span></span>
- <span data-ttu-id="2adca-131">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="2adca-131">User 4</span></span>
- <span data-ttu-id="2adca-132">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="2adca-132">User 5</span></span>

<span data-ttu-id="2adca-133">Testez la réinitialisation de mot de passe pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="2adca-133">Test password reset only for the User 2 account.</span></span>

## <a name="phase-6-configure-multi-factor-authentication"></a><span data-ttu-id="2adca-134">Étape 6 : configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="2adca-134">Phase 6: Configure multi-factor authentication</span></span>

<span data-ttu-id="2adca-135">Suivez les instructions de [Phase 2 de Guide de laboratoire de Test authentification multifacteur ](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) pour les comptes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="2adca-135">Follow the instructions in [Phase 2 of the multi-factor authentication Test Lab Guide](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) for the following user accounts:</span></span>

- <span data-ttu-id="2adca-136">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="2adca-136">User 2</span></span>
- <span data-ttu-id="2adca-137">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="2adca-137">User 3</span></span>
- <span data-ttu-id="2adca-138">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="2adca-138">User 4</span></span>
- <span data-ttu-id="2adca-139">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="2adca-139">User 5</span></span>

<span data-ttu-id="2adca-140">Testez l’authentification multifacteur uniquement pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="2adca-140">Test multi-factor authentication only for the User 2 account.</span></span>

## <a name="phase-7-enable-azure-ad-identity-protection"></a><span data-ttu-id="2adca-141">Étape 7 : activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="2adca-141">Phase 7: Enable Azure AD Identity Protection</span></span>

<span data-ttu-id="2adca-142">Suivez les instructions de [Étape 2 du guide laboratoire test de l’authentification transparente unique Azure AD](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-enable-and-use-azure-ad-identity-protection).</span><span class="sxs-lookup"><span data-stu-id="2adca-142">Follow the instructions in [Phase 2 of the Azure AD Identity Protection Test Lab Guide](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-enable-and-use-azure-ad-identity-protection).</span></span> 

## <a name="phase-8-enable-modern-authentication-for-exchange-online-and-skype-for-business-online"></a><span data-ttu-id="2adca-143">Étape 8 : activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="2adca-143">Phase 8: Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

<span data-ttu-id="2adca-144">Pour Exchange Online, suivez [ces instructions](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span><span class="sxs-lookup"><span data-stu-id="2adca-144">For Exchange Online, follow [these instructions](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span></span> 

<span data-ttu-id="2adca-145">Pour Skype Entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="2adca-145">For Skype for Business Online:</span></span>

1. <span data-ttu-id="2adca-146">Se connecter à [Skype Entreprise Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="2adca-146">Connect to [Skype for Business Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

2. <span data-ttu-id="2adca-147">Exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="2adca-147">Run this command.</span></span>

  ```powershell
  Set-CsOAuthConfiguration -ClientAdalAuthOverride Allowed
  ```

3. <span data-ttu-id="2adca-148">Vérifiez que la modification a été appliquée avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="2adca-148">Verify that the change was successful with this command.</span></span>

  ```powershell
  Get-CsOAuthConfiguration
  ```

<span data-ttu-id="2adca-149">Le résultat est un environnement de test qui respecte la configuration requise de la [configuration préalable de l’authentification directe](identity-access-prerequisites.md#prerequisites) pour l’accès identité et appareil.</span><span class="sxs-lookup"><span data-stu-id="2adca-149">The result is a test environment that meets the requirements of the [Pass-through authentication prerequisite configuration](identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span> 

## <a name="next-step"></a><span data-ttu-id="2adca-150">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2adca-150">Next step</span></span>

<span data-ttu-id="2adca-151">Utilisez [Stratégies d’accès courantes identité et appareil](identity-access-policies.md) pour configurer les stratégies qui se basent sur les conditions préalables et protègent identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="2adca-151">Use [Common identity and device access policies](identity-access-policies.md) to configure the policies that build on the prerequisites and protect identities and devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="2adca-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2adca-152">See also</span></span>

[<span data-ttu-id="2adca-153">Guides de laboratoire de Test Autres identités</span><span class="sxs-lookup"><span data-stu-id="2adca-153">Additional identity Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md#identity)

[<span data-ttu-id="2adca-154">Étape 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="2adca-154">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="2adca-155">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="2adca-155">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="2adca-156">Déploiement de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="2adca-156">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="2adca-157">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="2adca-157">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)

