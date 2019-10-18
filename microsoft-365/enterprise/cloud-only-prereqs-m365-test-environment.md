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
ms.openlocfilehash: 08f805f77771a056cc9d847dd064b472a46cb166
ms.sourcegitcommit: d9b462e035416bfa4b3d42467902c75859c55381
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/01/2019
ms.locfileid: "36055006"
---
# <a name="identity-and-device-access-prerequisites-for-cloud-only-in-your-microsoft-365-test-environment"></a><span data-ttu-id="30fd5-103">Conditions préalables à l’accès aux identités et aux appareils uniquement pour le cloud dans votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="30fd5-103">Identity and device access for your Microsoft 365 test environment</span></span>

<span data-ttu-id="30fd5-104">Les [configurations d’accès aux identités et appareils](microsoft-365-policies-configurations.md) sont un ensemble de configurations et de stratégies d’accès conditionnel permettant de protéger l’accès à tous les services intégrés à Azure Active Directory (Azure AD), dont Office 365 et Microsoft Intune dans Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="30fd5-104">[Identity and device access configurations](microsoft-365-policies-configurations.md) are a set of features and conditional access policies to protect access to all services that are integrated with Azure Active Directory (Azure AD), including Office 365 and Enterprise Mobility + Security (EMS) in Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="30fd5-105">Cet article décrit comment configurer un environnement de test Microsoft 365 qui respecte les exigences de [configuration préalable uniquement pour le cloud](identity-access-prerequisites.md#prerequisites) pour l’accès aux identités et aux appareils.</span><span class="sxs-lookup"><span data-stu-id="30fd5-105">This article describes how to configure a Microsoft 365 test environment that meets the requirements of the [cloud only prerequisite configuration](identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span>

<span data-ttu-id="30fd5-106">La configuration de cet environnement de test comprend sept étapes :</span><span class="sxs-lookup"><span data-stu-id="30fd5-106">There are two phases to setting up this test environment:</span></span>

1.  <span data-ttu-id="30fd5-107">Créer de votre environnement de test léger</span><span class="sxs-lookup"><span data-stu-id="30fd5-107">Build out your lightweight test environment</span></span>
2.  <span data-ttu-id="30fd5-108">Configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="30fd5-108">Configure named locations</span></span>
3.  <span data-ttu-id="30fd5-109">Configurer la réécriture du mot de passe</span><span class="sxs-lookup"><span data-stu-id="30fd5-109">Configure password writeback</span></span>
4.  <span data-ttu-id="30fd5-110">Configurer la réinitialisation du mot de passe en libre-service</span><span class="sxs-lookup"><span data-stu-id="30fd5-110">Configure self-service password resets</span></span>
5.  <span data-ttu-id="30fd5-111">Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="30fd5-111">Configure multifactor authentication</span></span>
6.  <span data-ttu-id="30fd5-112">Activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="30fd5-112">Azure AD Identity Protection</span></span>
7.  <span data-ttu-id="30fd5-113">Activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="30fd5-113">Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

## <a name="phase-1-build-out-your-lightweight-microsoft-365-test-environment"></a><span data-ttu-id="30fd5-114">Étape 1 : Créer de votre environnement de test Microsoft 365 léger</span><span class="sxs-lookup"><span data-stu-id="30fd5-114">Phase 1: Build out your lightweight or simulated enterprise Office 365 dev/test environment</span></span>

<span data-ttu-id="30fd5-115">Suivez les instructions de [Configuration base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="30fd5-115">Follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
<span data-ttu-id="30fd5-116">Voici la configuration obtenue.</span><span class="sxs-lookup"><span data-stu-id="30fd5-116">Here is the resulting configuration.</span></span>

![Environnement de test Microsoft 365 Entreprise léger](media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)
 

## <a name="phase-2-configure-named-locations"></a><span data-ttu-id="30fd5-118">Étape 2 : Configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="30fd5-118">Phase 2: Configure named locations</span></span>

<span data-ttu-id="30fd5-119">Commencez par déterminer les adresses IP publiques ou les plages d’adresses que votre organisation utilise.</span><span class="sxs-lookup"><span data-stu-id="30fd5-119">First, determine the public IP addresses or address ranges used by your organization.</span></span>

<span data-ttu-id="30fd5-120">Ensuite, suivez les instructions de [Configurer des emplacements nommés dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) pour ajouter les adresses ou plages d’adresses en tant qu’emplacements nommés.</span><span class="sxs-lookup"><span data-stu-id="30fd5-120">Next, follow the instructions in [Configure named locations in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) to add the addresses or address ranges as named locations.</span></span> 

## <a name="phase-3-configure-password-writeback"></a><span data-ttu-id="30fd5-121">Étape 3 : Configurer la réécriture du mot de passe</span><span class="sxs-lookup"><span data-stu-id="30fd5-121">Phase 3: Configure password writeback</span></span>

<span data-ttu-id="30fd5-122">Suivez les instructions de l’[Étape 2 du Guide de laboratoire de Test Réécriture du mot de passe](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span><span class="sxs-lookup"><span data-stu-id="30fd5-122">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span></span>

## <a name="phase-4-configure-self-service-password-reset"></a><span data-ttu-id="30fd5-123">Étape 4 : Configurer la réinitialisation du mot de passe en libre-service</span><span class="sxs-lookup"><span data-stu-id="30fd5-123">Phase 4: Configure self-service password reset</span></span>

<span data-ttu-id="30fd5-124">Suivez les instructions de l’[Étape 3 du Guide de laboratoire de Test Réinitialisation de mot de passe](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span><span class="sxs-lookup"><span data-stu-id="30fd5-124">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span></span> 

<span data-ttu-id="30fd5-125">Lors de l’activation de réinitialisation de mot de passe pour les comptes dans un groupe Azure AD spécifique, ajoutez ces comptes au groupe **réinitialiser le mot de passe**:</span><span class="sxs-lookup"><span data-stu-id="30fd5-125">When enabling password reset for the accounts in a specific Azure AD group, add these accounts to the **Password reset** group:</span></span>

- <span data-ttu-id="30fd5-126">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="30fd5-126">User: %2</span></span>
- <span data-ttu-id="30fd5-127">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="30fd5-127">User Field 3</span></span>
- <span data-ttu-id="30fd5-128">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="30fd5-128">User: %4</span></span>
- <span data-ttu-id="30fd5-129">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="30fd5-129">User 5</span></span>

<span data-ttu-id="30fd5-130">Testez la réinitialisation de mot de passe pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="30fd5-130">Next, you test password reset for the User 2 account.</span></span>

## <a name="phase-5-configure-multi-factor-authentication"></a><span data-ttu-id="30fd5-131">Étape 5 : Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="30fd5-131">Phase 5: Configure multi-factor authentication</span></span>

<span data-ttu-id="30fd5-132">Suivez les instructions de [Étape 2 de Guide de laboratoire de Test Authentification multifacteur ](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) pour les comptes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="30fd5-132">Follow the instructions in [Phase 2 of the multi-factor authentication Test Lab Guide](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) for the following user accounts:</span></span>

- <span data-ttu-id="30fd5-133">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="30fd5-133">User: %2</span></span>
- <span data-ttu-id="30fd5-134">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="30fd5-134">User Field 3</span></span>
- <span data-ttu-id="30fd5-135">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="30fd5-135">User: %4</span></span>
- <span data-ttu-id="30fd5-136">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="30fd5-136">User 5</span></span>

<span data-ttu-id="30fd5-137">Testez l’authentification multifacteur uniquement pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="30fd5-137">Enable and test multi-factor authentication for the User 2 account.</span></span>

## <a name="phase-6-enable-azure-ad-identity-protection"></a><span data-ttu-id="30fd5-138">Étape 6 : Activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="30fd5-138">Phase 6: Enable Azure AD Identity Protection</span></span>

<span data-ttu-id="30fd5-139">Suivez les instructions de [Étape 2 du Guide de laboratoire de Test Azure AD Identity Protection](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-enable-and-use-azure-ad-identity-protection).</span><span class="sxs-lookup"><span data-stu-id="30fd5-139">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-enable-and-use-azure-ad-identity-protection).</span></span> 

## <a name="phase-7-enable-modern-authentication-for-exchange-online-and-skype-for-business-online"></a><span data-ttu-id="30fd5-140">Étape 7 : Activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="30fd5-140">Phase 7: Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

<span data-ttu-id="30fd5-141">Pour Exchange Online, suivez [ces instructions](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span><span class="sxs-lookup"><span data-stu-id="30fd5-141">For Exchange Online, follow [these instructions](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span></span> 

<span data-ttu-id="30fd5-142">Pour Skype Entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="30fd5-142">Skype for Business Online</span></span>

1. <span data-ttu-id="30fd5-143">Se connecter à [Skype Entreprise Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="30fd5-143">[Migrate to Skype for Business Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell). (Administrator)</span></span>

2. <span data-ttu-id="30fd5-144">Exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="30fd5-144">Run this command:</span></span>

  ```
  Set-CsOAuthConfiguration -ClientAdalAuthOverride Allowed
  ```

3. <span data-ttu-id="30fd5-145">Vérifiez que la commande a correctement appliqué la modification.</span><span class="sxs-lookup"><span data-stu-id="30fd5-145">Ensure that the download was successful with this command.</span></span>

  ```
  Get-CsOAuthConfiguration
  ```

<span data-ttu-id="30fd5-146">Le résultat est un environnement de test qui respecte les exigences de [configuration préalable uniquement pour le cloud](identity-access-prerequisites.md#prerequisites) pour l’accès aux identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="30fd5-146">The result is a test environment that meets the requirements of the [cloud only prerequisite configuration](identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span> 

## <a name="next-step"></a><span data-ttu-id="30fd5-147">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="30fd5-147">Next step</span></span>

<span data-ttu-id="30fd5-148">Utilisez [Stratégies d’accès courantes identité et appareil](identity-access-policies.md) pour configurer les stratégies qui se basent sur les conditions préalables et protègent identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="30fd5-148">Use [Common identity and device access policies](identity-access-policies.md) to configure the policies that build on the prerequisites and test protection for identities and devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="30fd5-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30fd5-149">See also</span></span>

[<span data-ttu-id="30fd5-150">Guides de laboratoire de Test Autres identités</span><span class="sxs-lookup"><span data-stu-id="30fd5-150">Additional identity Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md#identity)

[<span data-ttu-id="30fd5-151">Étape 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="30fd5-151">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="30fd5-152">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="30fd5-152">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="30fd5-153">Déploiement de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="30fd5-153">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="30fd5-154">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="30fd5-154">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
