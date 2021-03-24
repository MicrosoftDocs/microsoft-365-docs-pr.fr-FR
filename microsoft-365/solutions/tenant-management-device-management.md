---
title: Étape 5. Gestion des appareils et des applications pour vos clients Microsoft 365 entreprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- m365solution-tenantmanagement
- tenant-management
- m365solution-scenario
ms.custom:
- Ent_Solutions
description: Déployez l’option correcte pour la gestion des appareils et des applications pour vos clients Microsoft 365.
ms.openlocfilehash: 0351f6be3f191e1a131da5b0b665a205a0abda8c
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51050993"
---
# <a name="step-5-device-and-app-management-for-your-microsoft-365-for-enterprise-tenants"></a><span data-ttu-id="74847-104">Étape 5.</span><span class="sxs-lookup"><span data-stu-id="74847-104">Step 5.</span></span> <span data-ttu-id="74847-105">Gestion des appareils et des applications pour vos clients Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="74847-105">Device and app management for your Microsoft 365 for enterprise tenants</span></span>

<span data-ttu-id="74847-106">Microsoft 365 entreprise inclut des fonctionnalités pour vous aider à gérer les appareils et l’utilisation des applications sur ces appareils au sein de votre organisation avec la gestion des périphériques mobiles (MDM) et la gestion des applications mobiles (MAM).</span><span class="sxs-lookup"><span data-stu-id="74847-106">Microsoft 365 for enterprise includes features to help manage devices and the use of apps on those devices within your organization with mobile device management (MDM) and mobile application management (MAM).</span></span> <span data-ttu-id="74847-107">Vous pouvez gérer les appareils iOS, Android, macOS et Windows pour protéger l’accès aux ressources de votre organisation, y compris à vos données.</span><span class="sxs-lookup"><span data-stu-id="74847-107">You can manage iOS, Android, macOS, and Windows devices to protect access to your organization's resources, including your data.</span></span> <span data-ttu-id="74847-108">Par exemple, vous pouvez empêcher l’envoi de courriers électroniques à des personnes extérieures à votre organisation ou isoler les données de l’organisation des données personnelles sur les appareils personnels de votre collaborateur.</span><span class="sxs-lookup"><span data-stu-id="74847-108">For example, you can prevent emails from being sent to people outside your organization or isolate organization data from personal data on your worker's personal devices.</span></span>

<span data-ttu-id="74847-109">Voici un exemple de validation et de gestion des utilisateurs, de leurs appareils et de leur utilisation d’applications de productivité locales et cloud telles que Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="74847-109">Here is an example of the validation and management of users, their devices, and their use of local and cloud productivity apps like Microsoft Teams.</span></span>

![Validation et gestion des utilisateurs, des appareils et des applications](../media/tenant-management-overview/tenant-management-device-app-mgmt.png)

<span data-ttu-id="74847-111">Pour vous aider à sécuriser et protéger les ressources de votre organisation, Microsoft 365 entreprise inclut des fonctionnalités pour vous aider à gérer les appareils et leur accès aux applications.</span><span class="sxs-lookup"><span data-stu-id="74847-111">To help you secure and protect your organization's resources, Microsoft 365 for enterprise includes features to help manage devices and their access to apps.</span></span> <span data-ttu-id="74847-112">Il existe deux options de gestion des appareils :</span><span class="sxs-lookup"><span data-stu-id="74847-112">There are two options for device management:</span></span>

- <span data-ttu-id="74847-113">Microsoft Intune, qui est une solution complète de gestion des appareils et des applications pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="74847-113">Microsoft Intune, which is a comprehensive device and app management solution for enterprises.</span></span>
- <span data-ttu-id="74847-114">Basic Mobility and Security, qui est un sous-ensemble de services Intune inclus avec tous les produits Microsoft 365 pour la gestion des appareils au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="74847-114">Basic Mobility and Security, which is a subset of Intune services included with all Microsoft 365 products for managing devices in your organization.</span></span> <span data-ttu-id="74847-115">Pour plus d’informations, [voir Fonctionnalités de la mobilité et de la sécurité de base.](../admin/basic-mobility-security/capabilities.md)</span><span class="sxs-lookup"><span data-stu-id="74847-115">For more information, see [Capabilities of Basic Mobility and Security](../admin/basic-mobility-security/capabilities.md).</span></span>

<span data-ttu-id="74847-116">Si vous avez Microsoft 365 E3 ou E5, vous devez utiliser Intune.</span><span class="sxs-lookup"><span data-stu-id="74847-116">If you have Microsoft 365 E3 or E5, you should use Intune.</span></span>

## <a name="microsoft-intune"></a><span data-ttu-id="74847-117">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="74847-117">Microsoft Intune</span></span>

<span data-ttu-id="74847-118">Vous utilisez [Microsoft Intune pour](/mem/intune/fundamentals/planning-guide) gérer l’accès à votre organisation à l’aide de LAM ou de MAM.</span><span class="sxs-lookup"><span data-stu-id="74847-118">You use [Microsoft Intune](/mem/intune/fundamentals/planning-guide) to manage access to your organization using MDM or MAM.</span></span> <span data-ttu-id="74847-119">La gestion des périphériques mobiles est le cas lorsque les utilisateurs « inscrivent » leurs appareils dans Intune.</span><span class="sxs-lookup"><span data-stu-id="74847-119">MDM is when users "enroll" their devices in Intune.</span></span> <span data-ttu-id="74847-120">Une fois qu’un appareil est inscrit, il s’agit d’un appareil géré et peut recevoir les stratégies, règles et paramètres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="74847-120">After a device is enrolled, it is a managed device and can receive your organization's  policies, rules, and settings.</span></span> <span data-ttu-id="74847-121">Par exemple, vous pouvez installer des applications spécifiques, créer une stratégie de mot de passe, installer une connexion VPN, etc.</span><span class="sxs-lookup"><span data-stu-id="74847-121">For example, you can install specific apps, create a password policy, install a VPN connection, and more.</span></span>

<span data-ttu-id="74847-122">Les utilisateurs ayant leurs propres appareils personnels peuvent ne pas vouloir inscrire leurs appareils ou être gérés par Intune et les stratégies de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="74847-122">Users with their own personal devices may not want to enroll their devices or be managed by Intune and your organization's policies.</span></span> <span data-ttu-id="74847-123">Toutefois, vous devez toujours protéger les ressources et les données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="74847-123">But you still need to protect your organization's resources and data.</span></span> <span data-ttu-id="74847-124">Dans ce scénario, vous pouvez protéger vos applications à l’aide de MAM.</span><span class="sxs-lookup"><span data-stu-id="74847-124">In this scenario, you can protect your apps using MAM.</span></span> <span data-ttu-id="74847-125">Par exemple, vous pouvez utiliser une stratégie MAM qui nécessite qu’un utilisateur entre un code confidentiel lors de l’accès à SharePoint sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="74847-125">For example, you can use an MAM policy that requires a user to enter a PIN when accessing SharePoint on the device.</span></span>

<span data-ttu-id="74847-126">Vous déterminerez également la façon dont vous allez gérer les appareils personnels et les appareils dont l’organisation est propriétaire.</span><span class="sxs-lookup"><span data-stu-id="74847-126">You'll also determine how you're going to manage personal devices and organization-owned devices.</span></span> <span data-ttu-id="74847-127">Vous souhaitez peut-être traiter les appareils différemment, en fonction de leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="74847-127">You might want to treat devices differently, depending on their uses.</span></span>

## <a name="identity-and-device-access-configurations"></a><span data-ttu-id="74847-128">Configurations des identités et de l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="74847-128">Identity and device access configurations</span></span>

<span data-ttu-id="74847-129">Microsoft fournit un ensemble de configurations pour l’accès aux identités et aux appareils [afin](../security/defender-365-security/microsoft-365-policies-configurations.md) de garantir un personnel sécurisé et productif.</span><span class="sxs-lookup"><span data-stu-id="74847-129">Microsoft provides a set of configurations for [identity and device access](../security/defender-365-security/microsoft-365-policies-configurations.md) to ensure a secure and productive workforce.</span></span> <span data-ttu-id="74847-130">Ces configurations incluent l’utilisation des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="74847-130">These configurations include the use of:</span></span>

- <span data-ttu-id="74847-131">Stratégies d’accès conditionnel Azure AD</span><span class="sxs-lookup"><span data-stu-id="74847-131">Azure AD Conditional Access policies</span></span>
- <span data-ttu-id="74847-132">Stratégies de protection des applications et de conformité des appareils Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="74847-132">Microsoft Intune device compliance and app protection policies</span></span>
- <span data-ttu-id="74847-133">Stratégies de risque utilisateur Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="74847-133">Azure AD Identity Protection user risk policies</span></span>
- <span data-ttu-id="74847-134">Stratégies supplémentaires des applications cloud</span><span class="sxs-lookup"><span data-stu-id="74847-134">Additional policies of cloud apps</span></span>

<span data-ttu-id="74847-135">Voici un exemple de l’application de ces paramètres et stratégies pour valider et restreindre les utilisateurs, leurs appareils et leur utilisation d’applications de productivité locales et cloud telles que Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="74847-135">Here is an example of the application of these settings and policies to validate and restrict users, their devices, and their use of local and cloud productivity apps like Microsoft Teams.</span></span>

![Configurations des identités et de l’accès aux appareils pour les exigences et les restrictions imposées aux utilisateurs, à leurs appareils et à leur utilisation des applications](../media/tenant-management-overview/tenant-management-device-app-mgmt-golden-config.png)

<span data-ttu-id="74847-137">Pour l’accès aux appareils et la gestion des applications, utilisez les configurations des articles suivants :</span><span class="sxs-lookup"><span data-stu-id="74847-137">For device access and app management, use the configurations in these articles:</span></span>

- [<span data-ttu-id="74847-138">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="74847-138">Prerequisites</span></span>](../security/defender-365-security/identity-access-prerequisites.md)
- [<span data-ttu-id="74847-139">Stratégies communes pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="74847-139">Common identity and device access policies</span></span>](../security/defender-365-security/identity-access-policies.md)

## <a name="results-of-step-5"></a><span data-ttu-id="74847-140">Résultats de l’étape 5</span><span class="sxs-lookup"><span data-stu-id="74847-140">Results of Step 5</span></span>

<span data-ttu-id="74847-141">Pour la gestion des appareils et des applications pour votre client Microsoft 365, vous avez déterminé les paramètres et stratégies Intune pour valider et restreindre les utilisateurs, leurs appareils et leur utilisation des applications de productivité locales et cloud.</span><span class="sxs-lookup"><span data-stu-id="74847-141">For device and app management for your Microsoft 365 tenant, you have determined the Intune settings and policies to validate and restrict users, their devices, and their use of local and cloud productivity apps.</span></span>

<span data-ttu-id="74847-142">Voici un exemple de client avec la gestion des applications et des appareils Intune avec les nouveaux éléments mis en surbrill plan.</span><span class="sxs-lookup"><span data-stu-id="74847-142">Here is an example of a tenant with Intune device and app management with the new elements highlighted.</span></span>

![Exemple de client avec gestion des appareils et des applications Intune](../media/tenant-management-overview/tenant-management-tenant-build-step5.png)

<span data-ttu-id="74847-144">Dans cette illustration, le client a :</span><span class="sxs-lookup"><span data-stu-id="74847-144">In this illustration, the tenant has:</span></span>

- <span data-ttu-id="74847-145">Appareils de l’organisation inscrits dans Intune.</span><span class="sxs-lookup"><span data-stu-id="74847-145">Organization-owned devices enrolled in Intune.</span></span>
- <span data-ttu-id="74847-146">Stratégies d’appareil et d’application Intune pour les appareils inscrits et personnels.</span><span class="sxs-lookup"><span data-stu-id="74847-146">Intune device and app policies for enrolled and personal devices.</span></span>

## <a name="ongoing-maintenance-for-device-and-app-management"></a><span data-ttu-id="74847-147">Maintenance continue pour la gestion des appareils et des applications</span><span class="sxs-lookup"><span data-stu-id="74847-147">Ongoing maintenance for device and app management</span></span>

<span data-ttu-id="74847-148">Régulièrement, vous devrez peut-être :</span><span class="sxs-lookup"><span data-stu-id="74847-148">On an ongoing basis, you might need to:</span></span> 

- <span data-ttu-id="74847-149">Gérer l’inscription des appareils.</span><span class="sxs-lookup"><span data-stu-id="74847-149">Manage device enrollment.</span></span>
- <span data-ttu-id="74847-150">Révisez vos paramètres et stratégies pour les applications, les appareils et les exigences de sécurité supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="74847-150">Revise your settings and policies for additional apps, devices, and security requirements.</span></span>