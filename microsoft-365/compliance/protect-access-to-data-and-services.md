---
title: Protéger l’accès aux appareils et l’accès des utilisateurs
f1.keywords:
- NOCSH
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 4/17/2018
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Découvrez comment protéger l’accès des utilisateurs et des appareils aux données Microsoft 365 services et se défendre contre la perte de données.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 9ff7bd2ff8b4b333eb30a6cc82797a8968941e0b
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51051696"
---
# <a name="protect-user-and-device-access"></a><span data-ttu-id="14122-103">Protéger l’accès aux appareils et l’accès des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="14122-103">Protect user and device access</span></span>

<span data-ttu-id="14122-104">La protection de l’accès Microsoft 365 données et services de votre entreprise est essentielle pour la protection contre les cyberattaques et la protection contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="14122-104">Protecting access to your Microsoft 365 data and services is crucial to defending against cyberattacks and guarding against data loss.</span></span> <span data-ttu-id="14122-105">Les mêmes protections peuvent être appliquées à d’autres applications SaaS dans votre environnement et même aux applications sur site publiées avec Azure Active Directory proxy d’application.</span><span class="sxs-lookup"><span data-stu-id="14122-105">The same protections can be applied to other SaaS applications in your environment and even to on-premises applications published with Azure Active Directory Application Proxy.</span></span>
  
## <a name="step-1-review-recommendations"></a><span data-ttu-id="14122-106">Étape 1 : Examiner les recommandations</span><span class="sxs-lookup"><span data-stu-id="14122-106">Step 1: Review recommendations</span></span>

<span data-ttu-id="14122-107">Découvrez les fonctionnalités recommandées relatives à la protection des identités et des appareils qui accèdent à Office 365, aux autres services SaaS et applications locales publiées avec le proxy d’application Azure AD.</span><span class="sxs-lookup"><span data-stu-id="14122-107">Recommended capabilities for protecting identities and devices that access Office 365, other SaaS services, and on-premises applications published with Azure AD Application Proxy.</span></span>
  
<span data-ttu-id="14122-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Plus de langues](https://www.microsoft.com/download/details.aspx?id=55032)</span><span class="sxs-lookup"><span data-stu-id="14122-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [More languages](https://www.microsoft.com/download/details.aspx?id=55032)</span></span>
  
## <a name="step-2-protect-administrator-accounts-and-access"></a><span data-ttu-id="14122-109">Étape 2 : Protéger les comptes d’administrateur et l’accès</span><span class="sxs-lookup"><span data-stu-id="14122-109">Step 2: Protect administrator accounts and access</span></span>
<span data-ttu-id="14122-110">Les comptes d’administration que vous utilisez pour administrer Microsoft 365 environnement de gestion incluent des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="14122-110">The administrative accounts you use to administer your Microsoft 365 environment include elevated privileges.</span></span> <span data-ttu-id="14122-111">Ce sont des cibles précieuses pour les pirates informatiques et les cyberattaques.</span><span class="sxs-lookup"><span data-stu-id="14122-111">These are valuable targets for hackers and cyberattackers.</span></span> 

<span data-ttu-id="14122-112">Commencez par utiliser des comptes d’administrateur uniquement pour l’administration.</span><span class="sxs-lookup"><span data-stu-id="14122-112">Begin by using administrator accounts only for administration.</span></span> <span data-ttu-id="14122-113">Les administrateurs doivent avoir un compte d’utilisateur distinct pour une utilisation normale et non administrative et utiliser leur compte administratif uniquement si nécessaire pour effectuer une tâche associée à leur fonction.</span><span class="sxs-lookup"><span data-stu-id="14122-113">Admins should have a separate user account for regular, non-administrative use and only use their administrative account when necessary to complete a task associated with their job function.</span></span>

<span data-ttu-id="14122-114">Protégez vos comptes d’administrateur avec l’authentification multifacteur et l’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="14122-114">Protect your administrator accounts with multi-factor authentication and conditional access.</span></span> <span data-ttu-id="14122-115">Pour plus d’informations, [voir Protection des comptes d’administrateur.](../security/defender-365-security/identity-access-prerequisites.md#protecting-administrator-accounts)</span><span class="sxs-lookup"><span data-stu-id="14122-115">For more information, see [Protecting administrator accounts](../security/defender-365-security/identity-access-prerequisites.md#protecting-administrator-accounts).</span></span> 

<span data-ttu-id="14122-116">Ensuite, configurez la gestion des accès privilégiés dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="14122-116">Next, configure privileged access management in Office 365.</span></span> <span data-ttu-id="14122-117">La gestion des accès privilégiés permet de contrôler l’accès de manière granulaire sur les tâches d’administration privilégiée dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="14122-117">Privileged access management allows granular access control over privileged admin tasks in Office 365.</span></span> <span data-ttu-id="14122-118">Il peut aider à protéger votre organisation contre les violations qui peuvent utiliser des comptes d’administrateur privilégiés existants avec un accès permanent aux données sensibles ou à des paramètres de configuration critiques.</span><span class="sxs-lookup"><span data-stu-id="14122-118">It can help protect your organization from breaches that may use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings.</span></span>

- [<span data-ttu-id="14122-119">Vue d’ensemble de la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="14122-119">Overview of privileged access management</span></span>](privileged-access-management-overview.md)
- [<span data-ttu-id="14122-120">Configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="14122-120">Configure privileged access management</span></span>](privileged-access-management-configuration.md)

<span data-ttu-id="14122-121">Une autre recommandation consiste à utiliser des stations de travail spécialement configurées pour le travail administratif.</span><span class="sxs-lookup"><span data-stu-id="14122-121">Another top recommendation is to use workstations specifically configured for administrative work.</span></span> <span data-ttu-id="14122-122">Il s’agit d’appareils dédiés qui sont utilisés uniquement pour les tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="14122-122">These are dedicated devices that are only used for administrative tasks.</span></span> <span data-ttu-id="14122-123">Voir [Sécurisation de l’accès privilégié.](/windows-server/identity/securing-privileged-access/securing-privileged-access)</span><span class="sxs-lookup"><span data-stu-id="14122-123">See [Securing privileged access](/windows-server/identity/securing-privileged-access/securing-privileged-access).</span></span>

<span data-ttu-id="14122-124">Enfin, vous pouvez atténuer l’impact d’un manque accidentel d’accès administratif en créant au moins deux comptes d’accès d’urgence dans votre client.</span><span class="sxs-lookup"><span data-stu-id="14122-124">Finally, you can mitigate the impact of inadvertent lack of administrative access by creating two or more emergency access accounts in your tenant.</span></span> <span data-ttu-id="14122-125">Voir [Gérer les comptes d’accès d’urgence dans Azure AD.](/azure/active-directory/users-groups-roles/directory-emergency-access)</span><span class="sxs-lookup"><span data-stu-id="14122-125">See [Manage emergency access accounts in Azure AD](/azure/active-directory/users-groups-roles/directory-emergency-access).</span></span> 

## <a name="step-3-configure-recommended-identity-and-device-access-policies"></a><span data-ttu-id="14122-126">Étape 3 : Configurer les stratégies recommandées d’accès aux identités et aux appareils</span><span class="sxs-lookup"><span data-stu-id="14122-126">Step 3: Configure recommended identity and device access policies</span></span>
<span data-ttu-id="14122-127">L’authentification multifacteur (MFA) et les stratégies d’accès conditionnel sont des outils puissants pour atténuer les comptes compromis et l’accès non autorisé.</span><span class="sxs-lookup"><span data-stu-id="14122-127">Multi-factor authentication (MFA) and conditional access policies are powerful tools for mitigating against compromised accounts and unauthorized access.</span></span> <span data-ttu-id="14122-128">Nous vous recommandons d’implémenter un ensemble de stratégies qui ont été testées ensemble.</span><span class="sxs-lookup"><span data-stu-id="14122-128">We recommend implementing a set of policies that have been tested together.</span></span> <span data-ttu-id="14122-129">Pour plus d’informations, y compris sur les étapes de déploiement, voir [Configurations d’accès aux identités et aux appareils.](../security/defender-365-security/microsoft-365-policies-configurations.md)</span><span class="sxs-lookup"><span data-stu-id="14122-129">For more information, including deployment steps, see [Identity and device access configurations](../security/defender-365-security/microsoft-365-policies-configurations.md).</span></span>

 <span data-ttu-id="14122-130">Ces stratégies implémentent les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="14122-130">These policies implement the following capabilities:</span></span>
- <span data-ttu-id="14122-131">Authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="14122-131">Mult-factor authentication</span></span>
- <span data-ttu-id="14122-132">Accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="14122-132">Conditional access</span></span>
- <span data-ttu-id="14122-133">Protection des applications Intune (protection des applications et des données pour les appareils)</span><span class="sxs-lookup"><span data-stu-id="14122-133">Intune app protection (app and data protection for devices)</span></span>
- <span data-ttu-id="14122-134">Conformité des appareils Intune</span><span class="sxs-lookup"><span data-stu-id="14122-134">Intune device compliance</span></span>
- <span data-ttu-id="14122-135">Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="14122-135">Azure AD Identity Protection</span></span>

<span data-ttu-id="14122-136">L’implémentation de la conformité des appareils Intune nécessite l’inscription de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="14122-136">Implementing Intune device compliance requires device enrollment.</span></span> <span data-ttu-id="14122-137">La gestion des appareils vous permet de vous assurer qu’ils sont sains et conformes avant de leur permettre d’accéder aux ressources de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="14122-137">Managing devices allows you to ensure that they are healthy and compliant before allowing them access to resources in your environment.</span></span> <span data-ttu-id="14122-138">Voir [Inscrire des appareils pour la gestion dans Intune](/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="14122-138">See [Enroll devices for management in Intune](/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)</span></span>

## <a name="step-4-configure-sharepoint-device-access-policies"></a><span data-ttu-id="14122-139">Étape 4 : Configurer les stratégies SharePoint’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="14122-139">Step 4: Configure SharePoint device access policies</span></span>

<span data-ttu-id="14122-140">Microsoft vous recommande de protéger le contenu des sites SharePoint avec du contenu sensible et hautement réglementé avec des contrôles d’accès aux appareils.</span><span class="sxs-lookup"><span data-stu-id="14122-140">Microsoft recommends you protect content in SharePoint sites with sensitive and highly-regulated content with device access controls.</span></span> <span data-ttu-id="14122-141">Pour plus d’informations, voir [recommandations de stratégie pour la sécurisation SharePoint sites et fichiers.](../security/defender-365-security/sharepoint-file-access-policies.md)</span><span class="sxs-lookup"><span data-stu-id="14122-141">For more information, see [Policy recommendations for securing SharePoint sites and files](../security/defender-365-security/sharepoint-file-access-policies.md).</span></span>



