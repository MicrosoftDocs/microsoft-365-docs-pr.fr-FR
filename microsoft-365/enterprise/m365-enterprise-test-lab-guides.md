---
title: Guides de laboratoire de test Microsoft 365 pour entreprise
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/20/2019
audience: ITPro
ms.topic: hub-page
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom:
- Ent_TLGs
- seo-marvel-apr2020
ms.assetid: 706d5449-45e5-4b0c-a012-ab60501899ad
description: Servez-vous des guides de laboratoire de test pour configurer les environnements de développement/test, de preuve de concept et de démonstration pour Microsoft 365 pour entreprise.
ms.openlocfilehash: a006f549d0ac68562faee9c935df7f15161b2f12
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50909597"
---
# <a name="microsoft-365-for-enterprise-test-lab-guides"></a><span data-ttu-id="8f2e8-103">Guides de laboratoire de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="8f2e8-103">Microsoft 365 for enterprise Test Lab Guides</span></span>

<span data-ttu-id="8f2e8-104">*Sont valables pour Microsoft 365 pour entreprise et Office 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-104">*This applies to both Microsoft 365 for enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="8f2e8-p101">Les guides de laboratoire de test vous permettent de vous familiariser rapidement avec les produits Microsoft. Ils fournissent des instructions normatives sur la configuration d’environnements de test simplifiés mais représentatifs. Vous pouvez utiliser ces environnements pour la démonstration, la personnalisation ou la création de preuves de concept complexes pour la durée d’un abonnement d’évaluation ou payant.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-p101">Test Lab Guides (TLGs) help you quickly learn about Microsoft products. They provide prescriptive instructions to configure simplified but representative test environments. You can use these environments for demonstration, customization, or creation of complex proofs of concept for the duration of a trial or paid subscription.</span></span>

<span data-ttu-id="8f2e8-108">Les modules de plateforme de plateforme (TLG) sont conçus pour être modulaires.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-108">TLGs are designed to be modular.</span></span> <span data-ttu-id="8f2e8-109">Ils s’appuient les uns sur les autres pour créer plusieurs configurations qui correspondent plus étroitement à vos besoins de configuration d’apprentissage ou de test.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-109">They build upon each other to create multiple configurations that more closely match your learning or test configuration needs.</span></span> <span data-ttu-id="8f2e8-110">L’expérience pratique « Je l’ai conçue moi-même et elle fonctionne » vous permet de comprendre les exigences de déploiement d’un nouveau produit ou d’un nouveau scénario, afin de mieux planifier son hébergement en production.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-110">The "I built it out myself and it works" hands-on experience helps you understand the deployment requirements of a new product or scenario, so that you can better plan for hosting it in production.</span></span>

<span data-ttu-id="8f2e8-111">Vous pouvez également utiliser des TLG pour créer des environnements représentatifs pour développer et tester des applications, également appelées environnements de développement/test.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-111">You can also use TLGs to create representative environments to develop and test applications, also known as dev/test environments.</span></span>
  
![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

<span data-ttu-id="8f2e8-113">Pour obtenir une carte visuelle de tous les articles de la pile de guides de laboratoire de test Microsoft 365 pour entreprise, développez le graphique suivant ou allez à [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="8f2e8-113">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, expand the following graphic or go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

<span data-ttu-id="8f2e8-114">[![Ensemble de guides de laboratoire de test Microsoft 365 pour entreprise](../media/m365-enterprise-test-lab-guides/microsoft-365-enterprise-tlg-stack.png)](../downloads/Microsoft365EnterpriseTLGStack.pdf)</span><span class="sxs-lookup"><span data-stu-id="8f2e8-114">[![The Microsoft 365 for enterprise Test Lab Guide stack](../media/m365-enterprise-test-lab-guides/microsoft-365-enterprise-tlg-stack.png)](../downloads/Microsoft365EnterpriseTLGStack.pdf)</span></span>

## <a name="base-configuration"></a><span data-ttu-id="8f2e8-115">Configuration de base</span><span class="sxs-lookup"><span data-stu-id="8f2e8-115">Base configuration</span></span>

<span data-ttu-id="8f2e8-116">Tout d’abord, créez un environnement de test [pour Microsoft 365 entreprise.](/microsoft-365-enterprise/)</span><span class="sxs-lookup"><span data-stu-id="8f2e8-116">First, create a test environment for [Microsoft 365 for enterprise](/microsoft-365-enterprise/).</span></span> <span data-ttu-id="8f2e8-117">Vous pouvez créer deux types différents de configurations de base :</span><span class="sxs-lookup"><span data-stu-id="8f2e8-117">You can create two different types of base configurations:</span></span>

- <span data-ttu-id="8f2e8-118">[Configuration](lightweight-base-configuration-microsoft-365-enterprise.md) de base légère : utilisez cette fonctionnalité lorsque vous souhaitez configurer et faire une démonstration des Microsoft 365 pour les fonctionnalités d’entreprise et les fonctionnalités dans un environnement cloud uniquement, qui n’inclut aucun composant local.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-118">[Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md) - Use this when you want to configure and demonstrate Microsoft 365 for enterprise features and capabilities in a cloud-only environment, which does not include any on-premises components.</span></span>

- <span data-ttu-id="8f2e8-119">Configuration de [base](simulated-ent-base-configuration-microsoft-365-enterprise.md) d’entreprise simulée : utilisez cette fonctionnalité lorsque vous souhaitez configurer et faire une démonstration des Microsoft 365 pour les fonctionnalités d’entreprise dans un environnement cloud hybride, qui utilise des composants locaux tels qu’un domaine AD DS (Active Directory Domain Services).</span><span class="sxs-lookup"><span data-stu-id="8f2e8-119">[Simulated enterprise base configuration](simulated-ent-base-configuration-microsoft-365-enterprise.md) - Use this when you want to configure and demonstrate Microsoft 365 for enterprise features and capabilities in a hybrid cloud environment, which uses on-premises components such as an Active Directory Domain Services (AD DS) domain.</span></span>

<span data-ttu-id="8f2e8-120">Vous pouvez également créer des environnements de test pour Office 365 E5 sans ajouter la licence Microsoft 365 E5 à votre version d’évaluation ou à votre environnement de test de production.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-120">You can also create test environments for Office 365 E5 by not adding the Microsoft 365 E5 license to your trial or production test environment.</span></span>
    
## <a name="identity"></a><span data-ttu-id="8f2e8-121">Identité</span><span class="sxs-lookup"><span data-stu-id="8f2e8-121">Identity</span></span>

<span data-ttu-id="8f2e8-122">Pour obtenir une description des fonctionnalités liées à l’identité, reportez-vous aux ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f2e8-122">To demonstrate identity-related features and capabilities, see:</span></span>

- [<span data-ttu-id="8f2e8-123">Synchronisation de hachage de mot de passe</span><span class="sxs-lookup"><span data-stu-id="8f2e8-123">Password hash synchronization</span></span>](password-hash-sync-m365-ent-test-environment.md)
  
   <span data-ttu-id="8f2e8-124">Activez et testez la synchronisation de répertoires basée sur le hachage de mots de passe à partir d’un contrôleur de domaine AD DS.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-124">Enable and test password hash-based directory synchronization from an AD DS domain controller.</span></span>

- [<span data-ttu-id="8f2e8-125">Authentification directe</span><span class="sxs-lookup"><span data-stu-id="8f2e8-125">Pass-through authentication</span></span>](pass-through-auth-m365-ent-test-environment.md)
  
   <span data-ttu-id="8f2e8-126">Activez et testez l’authentification directe à un contrôleur de domaine Windows Server AD DS.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-126">Enable and test pass-through authentication to an AD DS domain controller.</span></span>

- [<span data-ttu-id="8f2e8-127">Authentification fédérée</span><span class="sxs-lookup"><span data-stu-id="8f2e8-127">Federated authentication</span></span>](federated-identity-for-your-microsoft-365-dev-test-environment.md)
  
   <span data-ttu-id="8f2e8-128">Activez et testez l’authentification fédérée à un contrôleur de domaine Windows Server AD DS.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-128">Enable and test federated authentication to an AD DS domain controller.</span></span>

- [<span data-ttu-id="8f2e8-129">Authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="8f2e8-129">Azure AD Seamless Single Sign-on</span></span>](single-sign-on-m365-ent-test-environment.md)
  
   <span data-ttu-id="8f2e8-130">Activez et testez l' sign-on unique transparente Azure AD (SSO transparente) avec un contrôleur de domaine AD DS.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-130">Enable and test Azure AD Seamless Single Sign-on (Seamless SSO) with an AD DS domain controller.</span></span>

- [<span data-ttu-id="8f2e8-131">Authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="8f2e8-131">Multi-factor authentication</span></span>](multi-factor-authentication-microsoft-365-test-environment.md)
  
   <span data-ttu-id="8f2e8-132">Activez et testez l’authentification multifacteur sur smartphone pour un compte utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-132">Enable and test smart phone-based multi-factor authentication for a specific user account.</span></span>

- [<span data-ttu-id="8f2e8-133">Protéger des comptes Administrateur général</span><span class="sxs-lookup"><span data-stu-id="8f2e8-133">Protect global administrator accounts</span></span>](protect-global-administrator-accounts-microsoft-365-test-environment.md)

   <span data-ttu-id="8f2e8-134">Verrouillez vos comptes d’administrateur général avec des stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-134">Lock down your global administrator accounts with conditional access policies.</span></span>

- [<span data-ttu-id="8f2e8-135">Écriture différée de mot de passe</span><span class="sxs-lookup"><span data-stu-id="8f2e8-135">Password writeback</span></span>](password-writeback-m365-ent-test-environment.md)

   <span data-ttu-id="8f2e8-136">Utilisez l’écriture différée de mot de passe pour modifier le mot de passe de votre compte d’utilisateur Windows Server AD DS à partir d’Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-136">Use password writeback to change the password on your AD DS user account from Azure AD.</span></span>

- [<span data-ttu-id="8f2e8-137">Réinitialisation des mots de passe</span><span class="sxs-lookup"><span data-stu-id="8f2e8-137">Password reset</span></span>](password-reset-m365-ent-test-environment.md)

   <span data-ttu-id="8f2e8-138">Utilisez la réinitialisation du mot de passe libre-service pour réinitialiser votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-138">Use self-service password reset to reset your password.</span></span>

- [<span data-ttu-id="8f2e8-139">Attribution automatique de licences et appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="8f2e8-139">Automatic licensing and group membership</span></span>](automate-licenses-group-membership-microsoft-365-test-environment.md)

   <span data-ttu-id="8f2e8-140">Facilitez l’administration des nouveaux comptes grâce à l’attribution automatique de licences et l’appartenance au groupe dynamique.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-140">Make administering new accounts easier than ever with automatic licensing and dynamic group membership.</span></span>

- [<span data-ttu-id="8f2e8-141">Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="8f2e8-141">Azure AD Identity Protection</span></span>](azure-ad-identity-protection-microsoft-365-test-environment.md)

   <span data-ttu-id="8f2e8-142">Recherchez des vulnérabilités dans vos comptes utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-142">Scan your current user accounts for vulnerabilities.</span></span>

- [<span data-ttu-id="8f2e8-143">Accès aux identités et appareils</span><span class="sxs-lookup"><span data-stu-id="8f2e8-143">Identity and device access</span></span>](identity-device-access-m365-test-environment.md)

   <span data-ttu-id="8f2e8-144">Créez un environnement pour tester les configurations recommandées pour l’accès aux identités aux appareils et les stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-144">Create an environment to test recommended identity and device access configurations and conditional access policies.</span></span>

## <a name="mobile-device-management"></a><span data-ttu-id="8f2e8-145">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="8f2e8-145">Mobile device management</span></span>

<span data-ttu-id="8f2e8-146">Pour obtenir une description des fonctionnalités liées à la gestion des appareils mobiles, reportez-vous aux ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f2e8-146">To demonstrate mobile device management-related features and capabilities, see:</span></span>

- [<span data-ttu-id="8f2e8-147">Stratégies de conformité d’appareil</span><span class="sxs-lookup"><span data-stu-id="8f2e8-147">Device compliance policies</span></span>](mam-policies-for-your-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="8f2e8-148">Créez un groupe d’utilisateurs et une stratégie de conformité d’appareil pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-148">Create a user group and a device compliance policy for Windows 10 devices.</span></span>
    
- [<span data-ttu-id="8f2e8-149">Inscription d’appareils iOS et Android</span><span class="sxs-lookup"><span data-stu-id="8f2e8-149">Enroll iOS and Android devices</span></span>](enroll-ios-and-android-devices-in-your-microsoft-enterprise-365-dev-test-environ.md)
   
   <span data-ttu-id="8f2e8-150">Inscrivez des appareils iOS ou Android et gérez-les à distance.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-150">Enroll iOS or Android devices and manage them remotely.</span></span>

## <a name="information-protection"></a><span data-ttu-id="8f2e8-151">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="8f2e8-151">Information protection</span></span>

<span data-ttu-id="8f2e8-152">Pour faire la démonstration de fonctionnalités liées à la protection des informations, reportez-vous à :</span><span class="sxs-lookup"><span data-stu-id="8f2e8-152">To demonstrate information protection-related features and capabilities, see:</span></span>

- [<span data-ttu-id="8f2e8-153">Sécurité Microsoft 365 renforcée</span><span class="sxs-lookup"><span data-stu-id="8f2e8-153">Increased Microsoft 365 security</span></span>](increased-o365-security-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="8f2e8-154">Configurez les paramètres pour une sécurité Microsoft 365 renforcée et examinez les outils de sécurité intégrée.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-154">Configure settings for increased Microsoft 365 security and investigate built-in security tools.</span></span>
  
- [<span data-ttu-id="8f2e8-155">Classification des données</span><span class="sxs-lookup"><span data-stu-id="8f2e8-155">Data classification</span></span>](data-classification-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="8f2e8-156">Configurez et appliquez des étiquettes à un document dans un site d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-156">Configure and apply labels to a document in a SharePoint Online team site.</span></span>
    
- [<span data-ttu-id="8f2e8-157">Gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="8f2e8-157">Privileged access management</span></span>](privileged-access-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="8f2e8-158">Configurez la gestion des accès privilégiés pour un accès juste-à-temps aux tâches élevées et privilégiées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8f2e8-158">Configure privileged access management for just-in-time access to elevated and privileged tasks in your organization.</span></span>