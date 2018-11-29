---
title: Guides de laboratoire de test Microsoft 365 Entreprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/19/2018
ms.audience: ITPro
ms.topic: hub-page
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_TLGs
ms.assetid: 706d5449-45e5-4b0c-a012-ab60501899ad
description: Servez-vous des guides de laboratoire de test pour configurer les environnements de développement/test, de preuve de concept et de démonstration pour Microsoft 365 Entreprise.
ms.openlocfilehash: df723647748532936e40bbdb4e34ff698b9fa650
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867339"
---
# <a name="microsoft-365-enterprise-test-lab-guides"></a><span data-ttu-id="8e827-103">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="8e827-103">Microsoft 365 Enterprise Test Lab Guides</span></span>

<span data-ttu-id="8e827-p101">Les guides de laboratoire de test vous permettent de vous familiariser rapidement avec les produits Microsoft. Ils fournissent des instructions normatives sur la configuration d’environnements de test simplifiés mais représentatifs. Vous pouvez utiliser ces environnements pour la démonstration, la personnalisation ou la création de preuves de concept complexes pour la durée d’un abonnement d’évaluation ou payant.</span><span class="sxs-lookup"><span data-stu-id="8e827-p101">Test Lab Guides (TLGs) help you quickly learn about Microsoft products. They provide prescriptive instructions to configure simplified but representative test environments. You can use these environments for demonstration, customization, or creation of complex proofs of concept for the duration of a trial or paid subscription.</span></span> 

<span data-ttu-id="8e827-p102">Les guides de laboratoire de test sont conçus pour être modulaires. Ils s’appuient les uns sur les autres pour créer plusieurs configurations qui correspondent mieux à vos besoins de configuration d’apprentissage ou de test. L’expérience pratique du type « je l’ai créé moi-même et ça fonctionne » vous permet de comprendre les exigences de déploiement d’un nouveau produit ou scénario afin que vous puissiez mieux planifier son hébergement lors de la production.</span><span class="sxs-lookup"><span data-stu-id="8e827-p102">TLGs are designed to be modular. They build upon each other to create multiple configurations that more closely match your learning or test configuration needs. The "I built it out myself and it works" hands-on experience helps you understand the deployment requirements of a new product or scenario so you can better plan for hosting it in production.</span></span>

<span data-ttu-id="8e827-110">Les guides de laboratoire de test vous permettent également de créer des environnements représentatifs pour le développement et le test d’applications, également connus sous le nom d’environnements de développement/test.</span><span class="sxs-lookup"><span data-stu-id="8e827-110">You can also use TLGs to create representative environments for development and testing of applications, also known as dev/test environments.</span></span>
  
![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="8e827-112">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="8e827-112">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="base-configuration"></a><span data-ttu-id="8e827-113">Configuration de base</span><span class="sxs-lookup"><span data-stu-id="8e827-113">Base configuration</span></span>

<span data-ttu-id="8e827-p103">Tout d’abord, créez un environnement de test pour [Microsoft 365 Entreprise](https://docs.microsoft.com/microsoft-365-enterprise/) qui inclut Office 365 E5, Enterprise Mobility + Security (EMS) E5 et Windows 10 Entreprise. Vous pouvez créer deux types de configuration de base différents :</span><span class="sxs-lookup"><span data-stu-id="8e827-p103">First, you create a test environment for [Microsoft 365 Enterprise](https://docs.microsoft.com/microsoft-365-enterprise/) that includes Office 365 E5, Enterprise Mobility + Security (EMS) E5, and Windows 10 Enterprise. You can create two different types of base configurations:</span></span>

- <span data-ttu-id="8e827-116">Utilisez la [configuration de base minimale](lightweight-base-configuration-microsoft-365-enterprise.md) pour configurer et faire une démonstration des fonctionnalités de Microsoft 365 Entreprise dans un environnement cloud uniquement, sans aucun composant local.</span><span class="sxs-lookup"><span data-stu-id="8e827-116">Use the [lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md) when you want to configure and demonstrate Microsoft 365 Enterprise features and capabilities in a cloud-only environment, which does not include any on-premises components.</span></span>

- <span data-ttu-id="8e827-117">Utilisez la [configuration de base d’une entreprise simulée](simulated-ent-base-configuration-microsoft-365-enterprise.md) pour configurer et démontrer des fonctionnalités de Microsoft 365 Entreprise dans un environnement cloud hybride, qui utilise des composants locaux à l’instar d’un domaine Windows Server Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="8e827-117">Use the [simulated enterprise base configuration](simulated-ent-base-configuration-microsoft-365-enterprise.md) when you want to configure and demonstrate Microsoft 365 Enterprise features and capabilities in a hybrid cloud environment, which uses on-premises components such as a Windows Server Active Directory (AD) domain.</span></span>
    
## <a name="identity"></a><span data-ttu-id="8e827-118">Identité</span><span class="sxs-lookup"><span data-stu-id="8e827-118">Identity</span></span>

<span data-ttu-id="8e827-119">Pour obtenir une description des fonctionnalités liées à l’identité, reportez-vous aux ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e827-119">To demonstrate identity-related features and capabilities, see:</span></span>

- [<span data-ttu-id="8e827-120">Synchronisation de hachage de mot de passe</span><span class="sxs-lookup"><span data-stu-id="8e827-120">Password hash synchronization</span></span>](password-hash-sync-m365-ent-test-environment.md)
  
   <span data-ttu-id="8e827-121">Permet d’activer et de tester la synchronisation d’annuaires basée sur le hachage de mot de passe à partir d’un contrôleur de domaine Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="8e827-121">Enable and test password hash-based directory synchronization from a Windows Server AD domain controller.</span></span>

- [<span data-ttu-id="8e827-122">Authentification directe</span><span class="sxs-lookup"><span data-stu-id="8e827-122">Pass-through authentication</span></span>](pass-through-auth-m365-ent-test-environment.md)
  
   <span data-ttu-id="8e827-123">Permet d’activer et de tester l’authentification directe à un contrôleur de domaine Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="8e827-123">Enable and test pass-through authentication to a Windows Server AD domain controller.</span></span>

- [<span data-ttu-id="8e827-124">Authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="8e827-124">Azure AD Seamless Single Sign-on</span></span>](single-sign-on-m365-ent-test-environment.md)
  
   <span data-ttu-id="8e827-125">Permet d’activer et de tester l’authentification unique transparente Azure AD avec un contrôleur de domaine Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="8e827-125">Enable and test Azure AD Seamless Single Sign-on (SSO) with a Windows Server AD domain controller.</span></span>

- [<span data-ttu-id="8e827-126">Authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="8e827-126">Multi-factor authentication</span></span>](multi-factor-authentication-microsoft-365-test-environment.md)
  
   <span data-ttu-id="8e827-127">Activez et testez l’authentification multifacteur sur smartphone pour un compte utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="8e827-127">Enable and test smart phone-based multi-factor authentication for a specific user account.</span></span>

- [<span data-ttu-id="8e827-128">Protéger des comptes Administrateur général</span><span class="sxs-lookup"><span data-stu-id="8e827-128">Protect global administrator accounts</span></span>](protect-global-administrator-accounts-microsoft-365-test-environment.md)
 
   <span data-ttu-id="8e827-129">Verrouiller vos comptes d’administrateur général avec la sécurité des applications cloud Office 365 et les stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="8e827-129">Lock down your global administrator accounts with Office 365 Cloud App Security and conditional access policies.</span></span>

- [<span data-ttu-id="8e827-130">Réinitialisation des mots de passe</span><span class="sxs-lookup"><span data-stu-id="8e827-130">Password reset</span></span>](password-reset-m365-ent-test-environment.md)

   <span data-ttu-id="8e827-131">Utilisez la réinitialisation du mot de passe en libre-service (SSPR) pour réinitialiser votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="8e827-131">Use self-service password reset (SSPR) to reset your password.</span></span>

- [<span data-ttu-id="8e827-132">Attribution automatique de licences et appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="8e827-132">Automatic licensing and group membership</span></span>](automate-licenses-group-membership-microsoft-365-test-environment.md)

   <span data-ttu-id="8e827-133">Facilitez l’administration des nouveaux comptes grâce à l’attribution automatique de licences et l’appartenance au groupe dynamique.</span><span class="sxs-lookup"><span data-stu-id="8e827-133">Make administering new accounts easier than ever with automatic licensing and dynamic group membership.</span></span>

- [<span data-ttu-id="8e827-134">Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="8e827-134">Azure AD Identity Protection</span></span>](azure-ad-identity-protection-microsoft-365-test-environment.md)

   <span data-ttu-id="8e827-135">Recherchez des vulnérabilités dans vos comptes utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="8e827-135">Scan your current user accounts for vulnerabilities.</span></span>

## <a name="mobile-device-management"></a><span data-ttu-id="8e827-136">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="8e827-136">Mobile device management</span></span>

<span data-ttu-id="8e827-137">Pour obtenir une description des fonctionnalités liées à la gestion des appareils mobiles, reportez-vous aux ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e827-137">To demonstrate mobile device management-related features and capabilities, see:</span></span>

- [<span data-ttu-id="8e827-138">Stratégies de gestion des applications mobiles</span><span class="sxs-lookup"><span data-stu-id="8e827-138">MAM policies</span></span>](mam-policies-for-your-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="8e827-139">Créez des groupes d’utilisateurs et des stratégies de gestion des applications mobiles pour les appareils iOS et Android.</span><span class="sxs-lookup"><span data-stu-id="8e827-139">Create user groups and mobile application management (MAM) policies for iOS and Android devices.</span></span>
    
- [<span data-ttu-id="8e827-140">Inscription d’appareils iOS et Android</span><span class="sxs-lookup"><span data-stu-id="8e827-140">Enroll iOS and Android devices</span></span>](enroll-ios-and-android-devices-in-your-microsoft-enterprise-365-dev-test-environ.md)
   
   <span data-ttu-id="8e827-141">Inscrivez des appareils iOS ou Android et gérez-les à distance.</span><span class="sxs-lookup"><span data-stu-id="8e827-141">Enroll iOS or Android devices and manage them remotely.</span></span>


## <a name="information-protection"></a><span data-ttu-id="8e827-142">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="8e827-142">Information protection</span></span>

<span data-ttu-id="8e827-143">Pour faire la démonstration de fonctionnalités liées à la protection des informations, reportez-vous à :</span><span class="sxs-lookup"><span data-stu-id="8e827-143">To demonstrate information protection-related features and capabilities, see:</span></span>

- [<span data-ttu-id="8e827-144">Sécurité Office 365 accrue</span><span class="sxs-lookup"><span data-stu-id="8e827-144">Increased Office 365 security</span></span>](increased-o365-security-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="8e827-145">Configurez les paramètres pour une sécurité Office 365 accrue et examinez les outils de sécurité intégrée.</span><span class="sxs-lookup"><span data-stu-id="8e827-145">Configure settings for increased Office 365 security and investigate built-in security tools.</span></span>
  
- [<span data-ttu-id="8e827-146">Classification des données</span><span class="sxs-lookup"><span data-stu-id="8e827-146">Data classification</span></span>](data-classification-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="8e827-147">Configurez et appliquez des étiquettes Office 365 à un document dans un site d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8e827-147">Configure and apply Office 365 labels to a document in a SharePoint Online team site.</span></span>
    
- [<span data-ttu-id="8e827-148">Gestion des accès privilégiés pour votre environnement de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="8e827-148">Privileged access management for your Microsoft 365 Enterprise test environment</span></span>](privileged-access-microsoft-365-enterprise-dev-test-environment.md)
    
   <span data-ttu-id="8e827-149">Configurez la gestion des accès privilégiés pour un accès juste-à-temps aux tâches élevées et privilégiées dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="8e827-149">Configure privileged acccess management for just-in-time access to elevated and privileged tasks in your Office 365 organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e827-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e827-150">See also</span></span>

[<span data-ttu-id="8e827-151">Découvrez Microsoft Cloud grâce aux Guides de laboratoire de test d’adoption cloud</span><span class="sxs-lookup"><span data-stu-id="8e827-151">Experience the Microsoft Cloud with Cloud Adoption Test Lab Guides</span></span>](https://mva.microsoft.com/training-courses/experience-the-microsoft-cloud-with-cloud-adoption-test-lab-guides-17960?l=LXNRdhSLE_1000115881)
    
[<span data-ttu-id="8e827-152">Pile de guides de laboratoire de test Microsoft Cloud unique</span><span class="sxs-lookup"><span data-stu-id="8e827-152">One Microsoft Cloud Test Lab Guide stack</span></span>](http://aka.ms/catlgstack)
