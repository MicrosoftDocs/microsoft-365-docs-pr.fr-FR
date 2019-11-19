---
title: Conditions préalables à l’accès aux identités et appareils uniquement pour le cloud dans votre environnement de test Microsoft 365
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
description: Créez un environnement Microsoft 365 pour tester l’accès aux identités et appareils avec les conditions préalables pour l’authentification uniquement dans le cloud.
ms.openlocfilehash: 6e0796d24f2644907d214c4528eab2051fa3d83c
ms.sourcegitcommit: 9ee873c6a2f738a0c99921e036894b646742e706
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2019
ms.locfileid: "38673230"
---
# <a name="identity-and-device-access-prerequisites-for-cloud-only-in-your-microsoft-365-test-environment"></a><span data-ttu-id="56a47-103">Conditions préalables à l’accès aux identités et aux appareils uniquement pour le cloud dans votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="56a47-103">Identity and device access prerequisites for cloud only in your Microsoft 365 test environment</span></span>

<span data-ttu-id="56a47-104">*Ce Guide de Laboratoire Test peut uniquement être utilisé pour les environnements de test Microsoft 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="56a47-104">*This Test Lab Guide can only be used for Microsoft 365 Enterprise test environments.*</span></span>

<span data-ttu-id="56a47-105">Les [configurations d’accès aux identités et appareils](microsoft-365-policies-configurations.md) sont un ensemble de configurations et de stratégies d’accès conditionnel permettant de protéger l’accès à tous les services intégrés à Azure Active Directory (Azure AD), dont Office 365 et Microsoft Intune dans Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="56a47-105">[Identity and device access configurations](microsoft-365-policies-configurations.md) are a set of configurations and conditional access policies to protect access to all services that are integrated with Azure Active Directory (Azure AD), including Office 365 and Microsoft Intune in Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="56a47-106">Cet article décrit comment configurer un environnement de test Microsoft 365 qui respecte les exigences de [configuration préalable uniquement pour le cloud](identity-access-prerequisites.md#prerequisites) pour l’accès aux identités et aux appareils.</span><span class="sxs-lookup"><span data-stu-id="56a47-106">This article describes how to configure a Microsoft 365 test environment that meets the requirements of the [cloud only prerequisite configuration](identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span>

<span data-ttu-id="56a47-107">La configuration de cet environnement de test comprend sept étapes :</span><span class="sxs-lookup"><span data-stu-id="56a47-107">There are seven phases to setting up this test environment:</span></span>

1.  <span data-ttu-id="56a47-108">Créer de votre environnement de test léger</span><span class="sxs-lookup"><span data-stu-id="56a47-108">Build out your lightweight test environment</span></span>
2.  <span data-ttu-id="56a47-109">Configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="56a47-109">Configure named locations</span></span>
3.  <span data-ttu-id="56a47-110">Configurer la réécriture du mot de passe</span><span class="sxs-lookup"><span data-stu-id="56a47-110">Configure password writeback</span></span>
4.  <span data-ttu-id="56a47-111">Configurer la réinitialisation du mot de passe en libre-service</span><span class="sxs-lookup"><span data-stu-id="56a47-111">Configure self-service password resets</span></span>
5.  <span data-ttu-id="56a47-112">Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="56a47-112">Configure multifactor authentication</span></span>
6.  <span data-ttu-id="56a47-113">Activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="56a47-113">Enable Azure AD Identity Protection</span></span>
7.  <span data-ttu-id="56a47-114">Activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="56a47-114">Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

## <a name="phase-1-build-out-your-lightweight-microsoft-365-test-environment"></a><span data-ttu-id="56a47-115">Étape 1 : Créer de votre environnement de test Microsoft 365 léger</span><span class="sxs-lookup"><span data-stu-id="56a47-115">Phase 1: Build out your lightweight Microsoft 365 test environment</span></span>

<span data-ttu-id="56a47-116">Suivez les instructions de [Configuration base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="56a47-116">Follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
<span data-ttu-id="56a47-117">Voici la configuration obtenue.</span><span class="sxs-lookup"><span data-stu-id="56a47-117">Here is the resulting configuration.</span></span>

![Environnement de test Microsoft 365 Entreprise léger](media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)
 

## <a name="phase-2-configure-named-locations"></a><span data-ttu-id="56a47-119">Étape 2 : Configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="56a47-119">Phase 2: Configure named locations</span></span>

<span data-ttu-id="56a47-120">Commencez par déterminer les adresses IP publiques ou les plages d’adresses que votre organisation utilise.</span><span class="sxs-lookup"><span data-stu-id="56a47-120">First, determine the public IP addresses or address ranges used by your organization.</span></span>

<span data-ttu-id="56a47-121">Ensuite, suivez les instructions de [Configurer des emplacements nommés dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) pour ajouter les adresses ou plages d’adresses en tant qu’emplacements nommés.</span><span class="sxs-lookup"><span data-stu-id="56a47-121">Next, follow the instructions in [Configure named locations in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) to add the addresses or address ranges as named locations.</span></span> 

## <a name="phase-3-configure-password-writeback"></a><span data-ttu-id="56a47-122">Étape 3 : Configurer la réécriture du mot de passe</span><span class="sxs-lookup"><span data-stu-id="56a47-122">Phase 3: Configure password writeback</span></span>

<span data-ttu-id="56a47-123">Suivez les instructions de l’[Étape 2 du Guide de laboratoire de Test Réécriture du mot de passe](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span><span class="sxs-lookup"><span data-stu-id="56a47-123">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span></span>

## <a name="phase-4-configure-self-service-password-reset"></a><span data-ttu-id="56a47-124">Étape 4 : Configurer la réinitialisation du mot de passe en libre-service</span><span class="sxs-lookup"><span data-stu-id="56a47-124">Phase 4: Configure self-service password reset</span></span>

<span data-ttu-id="56a47-125">Suivez les instructions de l’[Étape 3 du Guide de laboratoire de Test Réinitialisation de mot de passe](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span><span class="sxs-lookup"><span data-stu-id="56a47-125">Follow the instructions in [Phase 3 of the password reset Test Lab Guide](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span></span> 

<span data-ttu-id="56a47-126">Lors de l’activation de réinitialisation de mot de passe pour les comptes dans un groupe Azure AD spécifique, ajoutez ces comptes au groupe **réinitialiser le mot de passe**:</span><span class="sxs-lookup"><span data-stu-id="56a47-126">When enabling password reset for the accounts in a specific Azure AD group, add these accounts to the **Password reset** group:</span></span>

- <span data-ttu-id="56a47-127">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="56a47-127">User 2</span></span>
- <span data-ttu-id="56a47-128">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="56a47-128">User 3</span></span>
- <span data-ttu-id="56a47-129">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="56a47-129">User 4</span></span>
- <span data-ttu-id="56a47-130">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="56a47-130">User 5</span></span>

<span data-ttu-id="56a47-131">Testez la réinitialisation de mot de passe pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="56a47-131">Test password reset only for the User 2 account.</span></span>

## <a name="phase-5-configure-multi-factor-authentication"></a><span data-ttu-id="56a47-132">Étape 5 : Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="56a47-132">Phase 5: Configure multi-factor authentication</span></span>

<span data-ttu-id="56a47-133">Suivez les instructions de [Étape 2 de Guide de laboratoire de Test Authentification multifacteur ](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) pour les comptes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="56a47-133">Follow the instructions in [Phase 2 of the multi-factor authentication Test Lab Guide](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) for the following user accounts:</span></span>

- <span data-ttu-id="56a47-134">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="56a47-134">User 2</span></span>
- <span data-ttu-id="56a47-135">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="56a47-135">User 3</span></span>
- <span data-ttu-id="56a47-136">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="56a47-136">User 4</span></span>
- <span data-ttu-id="56a47-137">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="56a47-137">User 5</span></span>

<span data-ttu-id="56a47-138">Testez l’authentification multifacteur uniquement pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="56a47-138">Test multi-factor authentication only for the User 2 account.</span></span>

## <a name="phase-6-enable-azure-ad-identity-protection"></a><span data-ttu-id="56a47-139">Étape 6 : Activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="56a47-139">Phase 6: Enable Azure AD Identity Protection</span></span>

<span data-ttu-id="56a47-140">Suivez les instructions de [Étape 2 du Guide de laboratoire de Test Azure AD Identity Protection](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-enable-and-use-azure-ad-identity-protection).</span><span class="sxs-lookup"><span data-stu-id="56a47-140">Follow the instructions in [Phase 2 of the Azure AD Identity Protection Test Lab Guide](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-enable-and-use-azure-ad-identity-protection).</span></span> 

## <a name="phase-7-enable-modern-authentication-for-exchange-online-and-skype-for-business-online"></a><span data-ttu-id="56a47-141">Étape 7 : Activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="56a47-141">Phase 7: Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

<span data-ttu-id="56a47-142">Pour Exchange Online, suivez [ces instructions](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span><span class="sxs-lookup"><span data-stu-id="56a47-142">For Exchange Online, follow [these instructions](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span></span> 

<span data-ttu-id="56a47-143">Pour Skype Entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="56a47-143">For Skype for Business Online:</span></span>

1. <span data-ttu-id="56a47-144">Se connecter à [Skype Entreprise Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="56a47-144">Connect to [Skype for Business Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

2. <span data-ttu-id="56a47-145">Exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="56a47-145">Run this command.</span></span>

  ```powershell
  Set-CsOAuthConfiguration -ClientAdalAuthOverride Allowed
  ```

3. <span data-ttu-id="56a47-146">Vérifiez que la commande a correctement appliqué la modification.</span><span class="sxs-lookup"><span data-stu-id="56a47-146">Verify that the change was successful with this command.</span></span>

  ```powershell
  Get-CsOAuthConfiguration
  ```

<span data-ttu-id="56a47-147">Le résultat est un environnement de test qui respecte les exigences de [configuration préalable uniquement pour le cloud](identity-access-prerequisites.md#prerequisites) pour l’accès aux identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="56a47-147">The result is a test environment that meets the requirements of the [cloud only prerequisite configuration](identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span> 

## <a name="next-step"></a><span data-ttu-id="56a47-148">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="56a47-148">Next step</span></span>

<span data-ttu-id="56a47-149">Utilisez [Stratégies d’accès courantes identité et appareil](identity-access-policies.md) pour configurer les stratégies qui se basent sur les conditions préalables et protègent identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="56a47-149">Use [Common identity and device access policies](identity-access-policies.md) to configure the policies that build on the prerequisites and protect identities and devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="56a47-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56a47-150">See also</span></span>

[<span data-ttu-id="56a47-151">Guides de laboratoire de Test Autres identités</span><span class="sxs-lookup"><span data-stu-id="56a47-151">Additional identity Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md#identity)

[<span data-ttu-id="56a47-152">Étape 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="56a47-152">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="56a47-153">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="56a47-153">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="56a47-154">Déploiement de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="56a47-154">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="56a47-155">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="56a47-155">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
