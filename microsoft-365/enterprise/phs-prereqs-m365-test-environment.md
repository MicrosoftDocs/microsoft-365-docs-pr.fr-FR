---
title: Conditions préalables d’accès aux identités et appareils pour la synchronisation du hachage du mot de passe dans votre environnement de test Microsoft 365
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
description: Créez un environnement Microsoft 365 pour tester l’accès aux identités et appareils avec les conditions préalables applicables à l’authentification de la synchronisation du hachage du mot de passe.
ms.openlocfilehash: 274f73b1cd6a925b972ab14417c9d854c48c2f00
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34074154"
---
# <a name="identity-and-device-access-prerequisites-for-password-hash-synchronization-in-your-microsoft-365-test-environment"></a><span data-ttu-id="52587-103">Conditions préalables d’accès aux identités et appareils pour la synchronisation du hachage du mot de passe dans votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="52587-103">Identity and device access prerequisites for password hash synchronization in your Microsoft 365 test environment</span></span>

<span data-ttu-id="52587-104">Les [Configurations d’accès aux identités et appareils](microsoft-365-policies-configurations.md) sont un ensemble de configurations et stratégies d’accès conditionnel pour protéger l’accès à tous les services qui sont intégrés avec Azure Active Directory (Azure AD), dont Office 365 et Enterprise Mobility + Security dans Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="52587-104">[Identity and device access configurations](microsoft-365-policies-configurations.md) are a set of features and conditional access policies to protect access to all services that are integrated with Azure Active Directory (Azure AD), including Office 365 and Enterprise Mobility + Security (EMS) in Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="52587-105">Cet article décrit comment configurer un environnement de test Microsoft 365 qui respecte les exigences de [configuration préalable de synchronisation du hachage du mot de passe Active Directory](identity-access-prerequisites.md#prerequisites) pour l’accès aux identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="52587-105">This article describes how to configure a Microsoft 365 test environment that meets the requirements of the [Active Directory with password hash sync prerequisite configuration](identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span>

<span data-ttu-id="52587-106">La configuration de cet environnement de test comprend huit étapes :</span><span class="sxs-lookup"><span data-stu-id="52587-106">There are two phases to setting up this test environment:</span></span>

1.  <span data-ttu-id="52587-107">Créer une entreprise simulée avec un environnement de test de synchronisation du hachage du mot de passe</span><span class="sxs-lookup"><span data-stu-id="52587-107">Create a simulated enterprise with password hash sync test environment</span></span>
2.  <span data-ttu-id="52587-108">Configurer l’authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="52587-108">Configure Azure AD single sign-on</span></span>
3.  <span data-ttu-id="52587-109">Configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="52587-109">Configure named locations</span></span>
4.  <span data-ttu-id="52587-110">Configurer la réécriture du mot de passe</span><span class="sxs-lookup"><span data-stu-id="52587-110">Configure password writeback</span></span>
5.  <span data-ttu-id="52587-111">Configurer la réinitialisation de mot de passe en libre-service pour tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="52587-111">Configure self-service password reset for all user accounts</span></span>
6.  <span data-ttu-id="52587-112">Configurer l’authentification multifacteur pour tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="52587-112">Configure multifactor authentication for all user accounts</span></span>
7.  <span data-ttu-id="52587-113">Activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="52587-113">Azure AD Identity Protection</span></span>
8.  <span data-ttu-id="52587-114">Activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="52587-114">Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

## <a name="phase-1-build-out-your-simulated-enterprise-with-password-hash-sync-microsoft-365-test-environment"></a><span data-ttu-id="52587-115">Étape 1 : Construire votre entreprise simulée avec un environnement de test Microsoft 365 pour la synchronisation du hachage du mot de passe</span><span class="sxs-lookup"><span data-stu-id="52587-115">Phase 1: Build out your simulated enterprise with password hash sync Microsoft 365 test environment</span></span>

<span data-ttu-id="52587-116">Suivez les instructions de [Synchronisation du hachage du mot de passe](password-hash-sync-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="52587-116">Follow the instructions in [Password hash synchronization](password-hash-sync-m365-ent-test-environment.md).</span></span>
<span data-ttu-id="52587-117">Voici la configuration obtenue.</span><span class="sxs-lookup"><span data-stu-id="52587-117">Here is the resulting configuration.</span></span>

![Entreprise simulée avec environnement de test de synchronisation du hachage du mot de passe](media/password-hash-sync-m365-ent-test-environment/Phase3.png)
 
## <a name="phase-2-configure-azure-ad-seamless-single-sign-on"></a><span data-ttu-id="52587-119">Étape 2 : Configurer l’authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="52587-119">Phase 2: Configure Azure AD seamless single sign-on</span></span>

<span data-ttu-id="52587-120">Suivez les instructions de [Phase 2 du guide laboratoire test de l’authentification transparente unique Azure AD](single-sign-on-m365-ent-test-environment.md#phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso).</span><span class="sxs-lookup"><span data-stu-id="52587-120">Follow the instructions in [Phase 2 of the Azure AD Seamless Single Sign-on Test Lab Guide](single-sign-on-m365-ent-test-environment.md#phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso).</span></span>

## <a name="phase-3-configure-named-locations"></a><span data-ttu-id="52587-121">Étape 3 : configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="52587-121">Phase 3: Configure named locations</span></span>

<span data-ttu-id="52587-122">Tout d’abord, déterminer les adresses IP publiques ou les plages d’adresse utilisées par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="52587-122">First, determine the public IP addresses or address ranges used by your organization.</span></span>

<span data-ttu-id="52587-123">Ensuite, suivez les instructions de [configurer des emplacements nommé dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) pour ajouter les adresses ou les plages d’adresses comme emplacements nommés.</span><span class="sxs-lookup"><span data-stu-id="52587-123">Next, follow the instructions in [Configure named locations in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) to add the addresses or address ranges as named locations.</span></span> 

## <a name="phase-4-configure-password-writeback"></a><span data-ttu-id="52587-124">Étape 4 : configurer l’écriture différée du mot de passe</span><span class="sxs-lookup"><span data-stu-id="52587-124">Phase 4: Configure password writeback</span></span>

<span data-ttu-id="52587-125">Suivez les instructions dans [Phase 2 du guide de laboratoire de test réinitialisation de mot de passe](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span><span class="sxs-lookup"><span data-stu-id="52587-125">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span></span>

## <a name="phase-5-configure-self-service-password-reset"></a><span data-ttu-id="52587-126">Étape 5 : configurer la réinitialisation du mot de passe libre-service</span><span class="sxs-lookup"><span data-stu-id="52587-126">Phase 5: Configure self-service password reset</span></span>

<span data-ttu-id="52587-127">Suivez les instructions du Guide de laboratoire de Test dans la [Phase 3 de la réinitialisation de mot de passe](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span><span class="sxs-lookup"><span data-stu-id="52587-127">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span></span> 

<span data-ttu-id="52587-128">Lors de l’activation de réinitialisation de mot de passe pour les comptes dans un groupe Azure AD spécifique, ajoutez ces comptes au groupe **réinitialiser le mot de passe**:</span><span class="sxs-lookup"><span data-stu-id="52587-128">When enabling password reset for the accounts in a specific Azure AD group, add these accounts to the **Password reset** group:</span></span>

- <span data-ttu-id="52587-129">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="52587-129">User: %2</span></span>
- <span data-ttu-id="52587-130">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="52587-130">User Field 3</span></span>
- <span data-ttu-id="52587-131">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="52587-131">User: %4</span></span>
- <span data-ttu-id="52587-132">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="52587-132">User 5</span></span>

<span data-ttu-id="52587-133">Testez la réinitialisation de mot de passe pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="52587-133">Next, you test password reset for the User 2 account.</span></span>

## <a name="phase-6-configure-multi-factor-authentication"></a><span data-ttu-id="52587-134">Étape 6 : configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="52587-134">Phase 6: Configure multi-factor authentication</span></span>

<span data-ttu-id="52587-135">Suivez les instructions de [Phase 2 de Guide de laboratoire de Test authentification multifacteur ](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) pour les comptes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="52587-135">Follow the instructions in [Phase 2 of the multi-factor authentication Test Lab Guide](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) for the following user accounts:</span></span>

- <span data-ttu-id="52587-136">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="52587-136">User: %2</span></span>
- <span data-ttu-id="52587-137">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="52587-137">User Field 3</span></span>
- <span data-ttu-id="52587-138">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="52587-138">User: %4</span></span>
- <span data-ttu-id="52587-139">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="52587-139">User 5</span></span>

<span data-ttu-id="52587-140">Testez l’authentification multifacteur uniquement pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="52587-140">Enable and test multi-factor authentication for the User 2 account.</span></span>

## <a name="phase-7-enable-azure-ad-identity-protection"></a><span data-ttu-id="52587-141">Étape 7 : activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="52587-141">Phase 7: Enable Azure AD Identity Protection</span></span>

<span data-ttu-id="52587-142">Suivez les instructions de [Étape 2 du guide laboratoire test de l’authentification transparente unique Azure AD](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-enable-and-use-azure-ad-identity-protection).</span><span class="sxs-lookup"><span data-stu-id="52587-142">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-enable-and-use-azure-ad-identity-protection).</span></span> 

## <a name="phase-8-enable-modern-authentication-for-exchange-online-and-skype-for-business-online"></a><span data-ttu-id="52587-143">Étape 8 : activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="52587-143">Phase 8: Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

<span data-ttu-id="52587-144">Pour Exchange Online, suivez [ces instructions](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span><span class="sxs-lookup"><span data-stu-id="52587-144">For Exchange Online, follow [these instructions](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span></span> 

<span data-ttu-id="52587-145">Pour Skype Entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="52587-145">Skype for Business Online</span></span>

1. <span data-ttu-id="52587-146">Se connecter à [Skype Entreprise Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="52587-146">[Migrate to Skype for Business Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell). (Administrator)</span></span>

2. <span data-ttu-id="52587-147">Exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="52587-147">Run this command:</span></span>

  ```
  Set-CsOAuthConfiguration -ClientAdalAuthOverride Allowed
  ```

3. <span data-ttu-id="52587-148">Vérifiez que la commande a correctement appliqué la modification.</span><span class="sxs-lookup"><span data-stu-id="52587-148">Ensure that the download was successful with this command.</span></span>

  ```
  Get-CsOAuthConfiguration
  ```

<span data-ttu-id="52587-149">Le résultat est un environnement de test conforme aux exigences de [configuration préalable de synchronisation du hachage du mot de passe Active Directory](identity-access-prerequisites.md#prerequisites) pour l’accès aux identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="52587-149">The result is a test environment that meets the requirements of the [Active Directory with password hash sync prerequisite configuration](identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span> 

## <a name="next-step"></a><span data-ttu-id="52587-150">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="52587-150">Next step</span></span>

<span data-ttu-id="52587-151">Utilisez [Stratégies d’accès courantes identité et appareil](identity-access-policies.md) pour configurer les stratégies qui se basent sur les conditions préalables et protègent identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="52587-151">Use [Common identity and device access policies](identity-access-policies.md) to configure the policies that build on the prerequisites and test protection for identities and devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="52587-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52587-152">See also</span></span>

[<span data-ttu-id="52587-153">Guides de laboratoire de Test Autres identités</span><span class="sxs-lookup"><span data-stu-id="52587-153">Additional identity Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md#identity)

[<span data-ttu-id="52587-154">Étape 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="52587-154">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="52587-155">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="52587-155">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="52587-156">Déploiement de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="52587-156">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="52587-157">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="52587-157">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
