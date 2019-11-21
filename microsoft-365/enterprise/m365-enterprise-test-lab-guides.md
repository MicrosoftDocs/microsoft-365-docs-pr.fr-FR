---
title: Guides de laboratoire de test Microsoft 365 Entreprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/20/2019
audience: ITPro
ms.topic: hub-page
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom:
- Ent_TLGs
ms.assetid: 706d5449-45e5-4b0c-a012-ab60501899ad
description: Servez-vous des guides de laboratoire de test pour configurer les environnements de développement/test, de preuve de concept et de démonstration pour Microsoft 365 Entreprise.
ms.openlocfilehash: 5f2f6b9fb137cf9d1ea9dc21ca12a3792d79e249
ms.sourcegitcommit: 7ae0389cf06e2f481ee646556720ab3f3e93ea32
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2019
ms.locfileid: "38757833"
---
# <a name="microsoft-365-enterprise-test-lab-guides"></a><span data-ttu-id="31f93-103">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="31f93-103">Microsoft 365 Enterprise Test Lab Guides</span></span>

<span data-ttu-id="31f93-104">*Sont valables pour Microsoft 365 Entreprise et Office 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="31f93-104">*This applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="31f93-p101">Les guides de laboratoire de test vous permettent de vous familiariser rapidement avec les produits Microsoft. Ils fournissent des instructions normatives sur la configuration d’environnements de test simplifiés mais représentatifs. Vous pouvez utiliser ces environnements pour la démonstration, la personnalisation ou la création de preuves de concept complexes pour la durée d’un abonnement d’évaluation ou payant.</span><span class="sxs-lookup"><span data-stu-id="31f93-p101">Test Lab Guides (TLGs) help you quickly learn about Microsoft products. They provide prescriptive instructions to configure simplified but representative test environments. You can use these environments for demonstration, customization, or creation of complex proofs of concept for the duration of a trial or paid subscription.</span></span> 

<span data-ttu-id="31f93-p102">Les guides de laboratoire de test sont conçus pour être modulaires. Ils s’appuient les uns sur les autres pour créer plusieurs configurations qui correspondent mieux à vos besoins de configuration d’apprentissage ou de test. L’expérience pratique du type « je l’ai créé moi-même et ça fonctionne » vous permet de comprendre les exigences de déploiement d’un nouveau produit ou scénario afin que vous puissiez mieux planifier son hébergement lors de la production.</span><span class="sxs-lookup"><span data-stu-id="31f93-p102">TLGs are designed to be modular. They build upon each other to create multiple configurations that more closely match your learning or test configuration needs. The "I built it out myself and it works" hands-on experience helps you understand the deployment requirements of a new product or scenario so you can better plan for hosting it in production.</span></span>

<span data-ttu-id="31f93-111">Les guides de laboratoire de test vous permettent également de créer des environnements représentatifs pour le développement et le test d’applications, également connus sous le nom d’environnements de développement/test.</span><span class="sxs-lookup"><span data-stu-id="31f93-111">You can also use TLGs to create representative environments for development and testing of applications, also known as dev/test environments.</span></span>
  
![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

<span data-ttu-id="31f93-113">Cliquez [ici](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="31f93-113">Click [here](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

<span data-ttu-id="31f93-114">[![Ensemble de guides de laboratoire de test Microsoft 365 Entreprise](./media/m365-enterprise-test-lab-guides/microsoft-365-enterprise-tlg-stack.png)](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf)</span><span class="sxs-lookup"><span data-stu-id="31f93-114">[![The Microsoft 365 Enterprise Test Lab Guide stack](./media/m365-enterprise-test-lab-guides/microsoft-365-enterprise-tlg-stack.png)](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf)</span></span>

## <a name="base-configuration"></a><span data-ttu-id="31f93-115">Configuration de base</span><span class="sxs-lookup"><span data-stu-id="31f93-115">Base configuration</span></span>

<span data-ttu-id="31f93-p103">Tout d’abord, créez un environnement de test pour [Microsoft 365 Entreprise](https://docs.microsoft.com/microsoft-365-enterprise/) qui inclut Office 365 E5, Enterprise Mobility + Security (EMS) E5 et Windows 10 Entreprise. Vous pouvez créer deux types de configuration de base différents :</span><span class="sxs-lookup"><span data-stu-id="31f93-p103">First, you create a test environment for [Microsoft 365 Enterprise](https://docs.microsoft.com/microsoft-365-enterprise/) that includes Office 365 E5, Enterprise Mobility + Security (EMS) E5, and Windows 10 Enterprise. You can create two different types of base configurations:</span></span>

- <span data-ttu-id="31f93-118">Utilisez la [configuration de base minimale](lightweight-base-configuration-microsoft-365-enterprise.md) pour configurer et faire une démonstration des fonctionnalités de Microsoft 365 Entreprise dans un environnement cloud uniquement, sans aucun composant local.</span><span class="sxs-lookup"><span data-stu-id="31f93-118">Use the [lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md) when you want to configure and demonstrate Microsoft 365 Enterprise features and capabilities in a cloud-only environment, which does not include any on-premises components.</span></span>

- <span data-ttu-id="31f93-119">Utilisez la [configuration de base d’une entreprise simulée](simulated-ent-base-configuration-microsoft-365-enterprise.md) pour configurer et démontrer des fonctionnalités de Microsoft 365 Entreprise dans un environnement cloud hybride, qui utilise des composants locaux à l’instar d’un domaine Windows Server Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="31f93-119">Use the [simulated enterprise base configuration](simulated-ent-base-configuration-microsoft-365-enterprise.md) when you want to configure and demonstrate Microsoft 365 Enterprise features and capabilities in a hybrid cloud environment, which uses on-premises components such as an Active Directory Domain Services (AD DS) domain.</span></span>

<span data-ttu-id="31f93-120">Vous pouvez également créer des environnements de test pour Office 365 E5 sans ajouter la licence Microsoft 365 E5 à votre version d’évaluation ou à votre environnement de test de production.</span><span class="sxs-lookup"><span data-stu-id="31f93-120">You can also create test environments for Office 365 E5 by not adding the Microsoft 365 E5 license to your trial or production test environment.</span></span>
    
## <a name="identity"></a><span data-ttu-id="31f93-121">Identité</span><span class="sxs-lookup"><span data-stu-id="31f93-121">Identity</span></span>

<span data-ttu-id="31f93-122">Pour obtenir une description des fonctionnalités liées à l’identité, reportez-vous aux ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="31f93-122">To demonstrate identity-related features and capabilities, see:</span></span>

- [<span data-ttu-id="31f93-123">Synchronisation de hachage de mot de passe</span><span class="sxs-lookup"><span data-stu-id="31f93-123">Password hash synchronization</span></span>](password-hash-sync-m365-ent-test-environment.md)
  
   <span data-ttu-id="31f93-124">Activez et testez la synchronisation de répertoires basée sur le hachage de mots de passe à partir d’un contrôleur de domaine AD DS.</span><span class="sxs-lookup"><span data-stu-id="31f93-124">Enable and test password hash-based directory synchronization from an AD DS domain controller.</span></span>

- [<span data-ttu-id="31f93-125">Authentification directe</span><span class="sxs-lookup"><span data-stu-id="31f93-125">Pass-through authentication</span></span>](pass-through-auth-m365-ent-test-environment.md)
  
   <span data-ttu-id="31f93-126">Activez et testez l’authentification directe à un contrôleur de domaine Windows Server AD DS.</span><span class="sxs-lookup"><span data-stu-id="31f93-126">Enable and test pass-through authentication to an AD DS domain controller.</span></span>

- <span data-ttu-id="31f93-127">[Authentification fédérée](federated-identity-for-your-office-365-dev-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="31f93-127">[](federated-identity-for-your-office-365-dev-test-environment.md)Federated authentication</span></span>
  
   <span data-ttu-id="31f93-128">Activez et testez l’authentification fédérée à un contrôleur de domaine Windows Server AD DS.</span><span class="sxs-lookup"><span data-stu-id="31f93-128">Enable and test pass-through authentication to an AD DS domain controller.</span></span>

- [<span data-ttu-id="31f93-129">Authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="31f93-129">Azure AD Seamless Single Sign-on</span></span>](single-sign-on-m365-ent-test-environment.md)
  
   <span data-ttu-id="31f93-130">Activer et tester l’authentification unique transparente Azure AD (SSO) avec un contrôleur de domaine Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="31f93-130">Enable and test Azure AD Seamless Single Sign-on (SSO) with an AD DS domain controller.</span></span>

- [<span data-ttu-id="31f93-131">Authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="31f93-131">Multi-factor authentication</span></span>](multi-factor-authentication-microsoft-365-test-environment.md)
  
   <span data-ttu-id="31f93-132">Activez et testez l’authentification multifacteur sur smartphone pour un compte utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="31f93-132">Enable and test smart phone-based multi-factor authentication for a specific user account.</span></span>

- [<span data-ttu-id="31f93-133">Protéger des comptes Administrateur général</span><span class="sxs-lookup"><span data-stu-id="31f93-133">Protect global administrator accounts</span></span>](protect-global-administrator-accounts-microsoft-365-test-environment.md)
 
   <span data-ttu-id="31f93-134">Verrouillez vos comptes d’administrateur général avec des stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="31f93-134">Lock down your global administrator accounts with conditional access policies.</span></span>

- [<span data-ttu-id="31f93-135">Écriture différée de mot de passe</span><span class="sxs-lookup"><span data-stu-id="31f93-135">Password writeback</span></span>](password-writeback-m365-ent-test-environment.md)

   <span data-ttu-id="31f93-136">Utilisez l’écriture différée de mot de passe pour modifier le mot de passe de votre compte d’utilisateur Windows Server AD DS à partir d’Azure AD.</span><span class="sxs-lookup"><span data-stu-id="31f93-136">Use password writeback to change the password on your AD DS user account from Azure AD.</span></span>

- [<span data-ttu-id="31f93-137">Réinitialisation des mots de passe</span><span class="sxs-lookup"><span data-stu-id="31f93-137">Password reset</span></span>](password-reset-m365-ent-test-environment.md)

   <span data-ttu-id="31f93-138">Utilisez la réinitialisation du mot de passe en libre-service (SSPR) pour réinitialiser votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="31f93-138">Use self-service password reset (SSPR) to reset your password.</span></span>

- [<span data-ttu-id="31f93-139">Attribution automatique de licences et appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="31f93-139">Automatic licensing and group membership</span></span>](automate-licenses-group-membership-microsoft-365-test-environment.md)

   <span data-ttu-id="31f93-140">Facilitez l’administration des nouveaux comptes grâce à l’attribution automatique de licences et l’appartenance au groupe dynamique.</span><span class="sxs-lookup"><span data-stu-id="31f93-140">Make administering new accounts easier than ever with automatic licensing and dynamic group membership.</span></span>

- [<span data-ttu-id="31f93-141">Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="31f93-141">Azure AD Identity Protection</span></span>](azure-ad-identity-protection-microsoft-365-test-environment.md)

   <span data-ttu-id="31f93-142">Recherchez des vulnérabilités dans vos comptes utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="31f93-142">Scan your current user accounts for vulnerabilities.</span></span>

- [<span data-ttu-id="31f93-143">Accès aux identités et appareils</span><span class="sxs-lookup"><span data-stu-id="31f93-143">Identity and device access</span></span>](identity-device-access-m365-test-environment.md)

   <span data-ttu-id="31f93-144">Créez un environnement pour tester les configurations recommandées pour l’accès aux identités aux appareils et les stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="31f93-144">Create an environment to test recommended identity and device access configurations and conditional access policies.</span></span>


## <a name="mobile-device-management"></a><span data-ttu-id="31f93-145">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="31f93-145">Mobile device management</span></span>

<span data-ttu-id="31f93-146">Pour obtenir une description des fonctionnalités liées à la gestion des appareils mobiles, reportez-vous aux ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="31f93-146">To demonstrate mobile device management-related features and capabilities, see:</span></span>

- [<span data-ttu-id="31f93-147">Stratégies de conformité d’appareil</span><span class="sxs-lookup"><span data-stu-id="31f93-147">Device compliance policies</span></span>](mam-policies-for-your-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="31f93-148">Créez un groupe d’utilisateurs et une stratégie de conformité d’appareil pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="31f93-148">Create a user group and a device compliance policy for Windows 10 devices.</span></span>
    
- [<span data-ttu-id="31f93-149">Inscription d’appareils iOS et Android</span><span class="sxs-lookup"><span data-stu-id="31f93-149">Enroll iOS and Android devices</span></span>](enroll-ios-and-android-devices-in-your-microsoft-enterprise-365-dev-test-environ.md)
   
   <span data-ttu-id="31f93-150">Inscrivez des appareils iOS ou Android et gérez-les à distance.</span><span class="sxs-lookup"><span data-stu-id="31f93-150">Enroll iOS or Android devices and manage them remotely.</span></span>


## <a name="information-protection"></a><span data-ttu-id="31f93-151">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="31f93-151">Information protection</span></span>

<span data-ttu-id="31f93-152">Pour faire la démonstration de fonctionnalités liées à la protection des informations, reportez-vous à :</span><span class="sxs-lookup"><span data-stu-id="31f93-152">To demonstrate information protection-related features and capabilities, see:</span></span>

- [<span data-ttu-id="31f93-153">Sécurité Office 365 accrue</span><span class="sxs-lookup"><span data-stu-id="31f93-153">Increased Office 365 security</span></span>](increased-o365-security-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="31f93-154">Configurez les paramètres pour une sécurité Office 365 accrue et examinez les outils de sécurité intégrée.</span><span class="sxs-lookup"><span data-stu-id="31f93-154">Configure settings for increased Office 365 security and investigate built-in security tools.</span></span>
  
- [<span data-ttu-id="31f93-155">Classification des données</span><span class="sxs-lookup"><span data-stu-id="31f93-155">Data classification</span></span>](data-classification-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="31f93-156">Configurez et appliquez des étiquettes Office 365 à un document dans un site d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="31f93-156">Configure and apply Office 365 labels to a document in a SharePoint Online team site.</span></span>
    
- [<span data-ttu-id="31f93-157">Gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="31f93-157">Privileged access management</span></span>](privileged-access-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="31f93-158">Configurez la gestion des accès privilégiés pour un accès juste-à-temps aux tâches élevées et privilégiées dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="31f93-158">Configure privileged access management for just-in-time access to elevated and privileged tasks in your Office 365 organization.</span></span>


