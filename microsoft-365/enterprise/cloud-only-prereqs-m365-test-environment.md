---
title: Conditions préalables à l’accès aux identités et appareils uniquement pour le cloud dans votre environnement de test Microsoft 365
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
description: Créez un environnement Microsoft 365 pour tester l’accès aux identités et appareils avec les conditions préalables pour l’authentification uniquement dans le cloud.
ms.openlocfilehash: 927aa032e4181206b3a744da7076b696ac5cf4d4
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51199548"
---
# <a name="identity-and-device-access-prerequisites-for-cloud-only-in-your-microsoft-365-test-environment"></a><span data-ttu-id="875e8-103">Conditions préalables à l’accès aux identités et aux appareils uniquement pour le cloud dans votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="875e8-103">Identity and device access prerequisites for cloud only in your Microsoft 365 test environment</span></span>

<span data-ttu-id="875e8-104">*Ce Guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="875e8-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="875e8-105">[Les configurations](../security/office-365-security/microsoft-365-policies-configurations.md) d’accès aux identités et appareils sont un ensemble de configurations recommandées et de stratégies d’accès conditionnel pour protéger l’accès à tous les services intégrés à Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="875e8-105">[Identity and device access configurations](../security/office-365-security/microsoft-365-policies-configurations.md) are a set of recommended configurations and conditional access policies to protect access to all services that are integrated with Azure Active Directory (Azure AD).</span></span>

<span data-ttu-id="875e8-106">Cet article décrit comment configurer un environnement de test Microsoft 365 qui respecte les exigences de [configuration préalable uniquement pour le cloud](../security/office-365-security/identity-access-prerequisites.md#prerequisites) pour l’accès aux identités et aux appareils.</span><span class="sxs-lookup"><span data-stu-id="875e8-106">This article describes how to configure a Microsoft 365 test environment that meets the requirements of the [cloud only prerequisite configuration](../security/office-365-security/identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span>

<span data-ttu-id="875e8-107">La configuration de cet environnement de test comprend huit étapes :</span><span class="sxs-lookup"><span data-stu-id="875e8-107">There are eight phases to setting up this test environment:</span></span>

1. <span data-ttu-id="875e8-108">Créer de votre environnement de test léger</span><span class="sxs-lookup"><span data-stu-id="875e8-108">Build out your lightweight test environment</span></span>
2. <span data-ttu-id="875e8-109">Configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="875e8-109">Configure named locations</span></span>
3. <span data-ttu-id="875e8-110">Configurer la réinitialisation du mot de passe libre-service</span><span class="sxs-lookup"><span data-stu-id="875e8-110">Configure self-service password reset</span></span>
4. <span data-ttu-id="875e8-111">Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="875e8-111">Configure multifactor authentication</span></span>
5. <span data-ttu-id="875e8-112">Activer l’inscription automatique de l’appareil des ordinateurs Windows domaine</span><span class="sxs-lookup"><span data-stu-id="875e8-112">Enable automatic device registration of domain-joined Windows computers</span></span>
6. <span data-ttu-id="875e8-113">Configurer la protection par mot de passe Azure AD</span><span class="sxs-lookup"><span data-stu-id="875e8-113">Configure Azure AD password protection</span></span> 
7. <span data-ttu-id="875e8-114">Activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="875e8-114">Enable Azure AD Identity Protection</span></span>
8. <span data-ttu-id="875e8-115">Activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="875e8-115">Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

## <a name="phase-1-build-out-your-lightweight-microsoft-365-test-environment"></a><span data-ttu-id="875e8-116">Étape 1 : Créer de votre environnement de test Microsoft 365 léger</span><span class="sxs-lookup"><span data-stu-id="875e8-116">Phase 1: Build out your lightweight Microsoft 365 test environment</span></span>

<span data-ttu-id="875e8-117">Suivez les instructions de [Configuration base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="875e8-117">Follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
<span data-ttu-id="875e8-118">Voici la configuration obtenue.</span><span class="sxs-lookup"><span data-stu-id="875e8-118">Here is the resulting configuration.</span></span>

![Environnement de test Microsoft 365 Entreprise léger](../media/lightweight-base-configuration-microsoft-365-enterprise/Phase4.png)
 
## <a name="phase-2-configure-named-locations"></a><span data-ttu-id="875e8-120">Étape 2 : Configurer des emplacements nommés</span><span class="sxs-lookup"><span data-stu-id="875e8-120">Phase 2: Configure named locations</span></span>

<span data-ttu-id="875e8-121">Commencez par déterminer les adresses IP publiques ou les plages d’adresses que votre organisation utilise.</span><span class="sxs-lookup"><span data-stu-id="875e8-121">First, determine the public IP addresses or address ranges used by your organization.</span></span>

<span data-ttu-id="875e8-122">Ensuite, suivez les instructions de [Configurer des emplacements nommés dans Azure Active Directory](/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) pour ajouter les adresses ou plages d’adresses en tant qu’emplacements nommés.</span><span class="sxs-lookup"><span data-stu-id="875e8-122">Next, follow the instructions in [Configure named locations in Azure Active Directory](/azure/active-directory/reports-monitoring/quickstart-configure-named-locations) to add the addresses or address ranges as named locations.</span></span> 

## <a name="phase-3-configure-self-service-password-reset"></a><span data-ttu-id="875e8-123">Phase 3 : Configurer la réinitialisation du mot de passe libre-service</span><span class="sxs-lookup"><span data-stu-id="875e8-123">Phase 3: Configure self-service password reset</span></span>

<span data-ttu-id="875e8-124">Suivez les instructions de l’[Étape 3 du Guide de laboratoire de Test Réinitialisation de mot de passe](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span><span class="sxs-lookup"><span data-stu-id="875e8-124">Follow the instructions in [Phase 3 of the password reset Test Lab Guide](password-reset-m365-ent-test-environment.md#phase-3-configure-and-test-password-reset).</span></span> 

<span data-ttu-id="875e8-125">Lors de l’activation de réinitialisation de mot de passe pour les comptes dans un groupe Azure AD spécifique, ajoutez ces comptes au groupe **réinitialiser le mot de passe**:</span><span class="sxs-lookup"><span data-stu-id="875e8-125">When enabling password reset for the accounts in a specific Azure AD group, add these accounts to the **Password reset** group:</span></span>

- <span data-ttu-id="875e8-126">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="875e8-126">User 2</span></span>
- <span data-ttu-id="875e8-127">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="875e8-127">User 3</span></span>
- <span data-ttu-id="875e8-128">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="875e8-128">User 4</span></span>
- <span data-ttu-id="875e8-129">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="875e8-129">User 5</span></span>

<span data-ttu-id="875e8-130">Testez la réinitialisation de mot de passe pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="875e8-130">Test password reset only for the User 2 account.</span></span>

## <a name="phase-4-configure-multi-factor-authentication"></a><span data-ttu-id="875e8-131">Phase 4 : Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="875e8-131">Phase 4: Configure multi-factor authentication</span></span>

<span data-ttu-id="875e8-132">Suivez les instructions de [Étape 2 de Guide de laboratoire de Test Authentification multifacteur ](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) pour les comptes d’utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="875e8-132">Follow the instructions in [Phase 2 of the multi-factor authentication Test Lab Guide](multi-factor-authentication-microsoft-365-test-environment.md#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account) for the following user accounts:</span></span>

- <span data-ttu-id="875e8-133">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="875e8-133">User 2</span></span>
- <span data-ttu-id="875e8-134">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="875e8-134">User 3</span></span>
- <span data-ttu-id="875e8-135">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="875e8-135">User 4</span></span>
- <span data-ttu-id="875e8-136">Utilisateur 5</span><span class="sxs-lookup"><span data-stu-id="875e8-136">User 5</span></span>

<span data-ttu-id="875e8-137">Testez l’authentification multifacteur uniquement pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="875e8-137">Test multi-factor authentication only for the User 2 account.</span></span>

## <a name="phase-5-enable-automatic-device-registration-of-domain-joined-windows-computers"></a><span data-ttu-id="875e8-138">Phase 5 : Activer l’inscription automatique des appareils joints à un domaine Windows ordinateurs</span><span class="sxs-lookup"><span data-stu-id="875e8-138">Phase 5: Enable automatic device registration of domain-joined Windows computers</span></span> 

<span data-ttu-id="875e8-139">Suivez [ces instructions pour](/azure/active-directory/devices/hybrid-azuread-join-plan) activer l’inscription automatique des ordinateurs joints Windows domaine.</span><span class="sxs-lookup"><span data-stu-id="875e8-139">Follow [these instructions](/azure/active-directory/devices/hybrid-azuread-join-plan) to enable automatic device registration of domain-joined Windows computers.</span></span>

## <a name="phase-6-configure-azure-ad-password-protection"></a><span data-ttu-id="875e8-140">Phase 6 : Configurer la protection par mot de passe Azure AD</span><span class="sxs-lookup"><span data-stu-id="875e8-140">Phase 6: Configure Azure AD password protection</span></span> 

<span data-ttu-id="875e8-141">Suivez [ces instructions pour](/azure/active-directory/authentication/concept-password-ban-bad) bloquer les mots de passe faibles connus et leurs variantes.</span><span class="sxs-lookup"><span data-stu-id="875e8-141">Follow [these instructions](/azure/active-directory/authentication/concept-password-ban-bad) to block known weak passwords and their variants.</span></span>

## <a name="phase-7-enable-azure-ad-identity-protection"></a><span data-ttu-id="875e8-142">Étape 7 : activer Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="875e8-142">Phase 7: Enable Azure AD Identity Protection</span></span>

<span data-ttu-id="875e8-143">Suivez les instructions de [Étape 2 du guide laboratoire test de l’authentification transparente unique Azure AD](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-use-azure-ad-identity-protection).</span><span class="sxs-lookup"><span data-stu-id="875e8-143">Follow the instructions in [Phase 2 of the Azure AD Identity Protection Test Lab Guide](azure-ad-identity-protection-microsoft-365-test-environment.md#phase-2-use-azure-ad-identity-protection).</span></span> 

## <a name="phase-8-enable-modern-authentication-for-exchange-online-and-skype-for-business-online"></a><span data-ttu-id="875e8-144">Étape 8 : activer l’authentification moderne pour Exchange Online et Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="875e8-144">Phase 8: Enable modern authentication for Exchange Online and Skype for Business Online</span></span>

<span data-ttu-id="875e8-145">Pour Exchange Online, suivez [ces instructions](/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span><span class="sxs-lookup"><span data-stu-id="875e8-145">For Exchange Online, follow [these instructions](/Exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online#enable-or-disable-modern-authentication-in-exchange-online-for-client-connections-in-outlook-2013-or-later).</span></span> 

<span data-ttu-id="875e8-146">Pour Skype Entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="875e8-146">For Skype for Business Online:</span></span>

1. <span data-ttu-id="875e8-147">Se connecter à [Skype Entreprise Online](/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="875e8-147">Connect to [Skype for Business Online](/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

2. <span data-ttu-id="875e8-148">Exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="875e8-148">Run this command.</span></span>

  ```powershell
  Set-CsOAuthConfiguration -ClientAdalAuthOverride Allowed
  ```

3. <span data-ttu-id="875e8-149">Vérifiez que la commande a correctement appliqué la modification.</span><span class="sxs-lookup"><span data-stu-id="875e8-149">Verify that the change was successful with this command.</span></span>

  ```powershell
  Get-CsOAuthConfiguration
  ```

<span data-ttu-id="875e8-150">Le résultat est un environnement de test qui répond aux exigences de la configuration préalable en [nuage](../security/office-365-security/identity-access-prerequisites.md#prerequisites) uniquement pour l’accès aux identités et aux appareils.</span><span class="sxs-lookup"><span data-stu-id="875e8-150">The result is a test environment that meets the requirements of the [cloud-only prerequisite configuration](../security/office-365-security/identity-access-prerequisites.md#prerequisites) for identity and device access.</span></span> 

## <a name="next-step"></a><span data-ttu-id="875e8-151">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="875e8-151">Next step</span></span>

<span data-ttu-id="875e8-152">Utilisez [Stratégies d’accès courantes identité et appareil](../security/office-365-security/identity-access-policies.md) pour configurer les stratégies qui se basent sur les conditions préalables et protègent identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="875e8-152">Use [Common identity and device access policies](../security/office-365-security/identity-access-policies.md) to configure the policies that build on the prerequisites and protect identities and devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="875e8-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="875e8-153">See also</span></span>

[<span data-ttu-id="875e8-154">Guides de laboratoire de Test Autres identités</span><span class="sxs-lookup"><span data-stu-id="875e8-154">Additional identity Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md#identity)

[<span data-ttu-id="875e8-155">Feuille de route des identités</span><span class="sxs-lookup"><span data-stu-id="875e8-155">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="875e8-156">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="875e8-156">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="875e8-157">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="875e8-157">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="875e8-158">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="875e8-158">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)
