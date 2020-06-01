---
title: Configurer l'authentification multifacteur pour les utilisateurs
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: sirkkuw
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 8f0454b2-f51a-4d9c-bcde-2c48e41621c6
description: Découvrez comment configurer l’authentification multifacteur pour votre organisation.
monikerRange: o365-worldwide
ms.openlocfilehash: c84c66cc051363fbc582abfb5521f922440b6801
ms.sourcegitcommit: a005395165db8896f4109674443b5e5e9209861d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/31/2020
ms.locfileid: "44432378"
---
# <a name="set-up-multi-factor-authentication"></a><span data-ttu-id="b1718-103">Configurer Multi-factor Authentification (MFA)</span><span class="sxs-lookup"><span data-stu-id="b1718-103">Set up multi-factor authentication</span></span>
  
<span data-ttu-id="b1718-104">En fonction de votre compréhension de [Multi-Factor Authentication (MFA) et de sa prise en charge dans Microsoft 365](multi-factor-authentication-microsoft-365.md), il est temps de le configurer et de le déployer dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b1718-104">Based on your understanding of [multi-factor authentication (MFA) and its support in Microsoft 365](multi-factor-authentication-microsoft-365.md), it’s time to set it up and roll it out to your organization.</span></span>

<span data-ttu-id="b1718-105">Avant de commencer, déterminez si ces conditions spéciales s’appliquent à vous et prenez les mesures appropriées :</span><span class="sxs-lookup"><span data-stu-id="b1718-105">Before you begin, determine if these special conditions apply to you and take the appropriate action:</span></span>

- <span data-ttu-id="b1718-106">Si vous avez des clients Office 2013 sur des appareils Windows, [activez l’authentification moderne](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/enable-modern-authentication).</span><span class="sxs-lookup"><span data-stu-id="b1718-106">If you have Office 2013 clients on Windows devices, [enable Modern Authentication](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/enable-modern-authentication).</span></span>

- <span data-ttu-id="b1718-107">Si vous disposez de services d’annuaire tiers avec Active Directory Federation Services (AD FS), configurez le serveur Azure MFA.</span><span class="sxs-lookup"><span data-stu-id="b1718-107">If you have third-party directory services with Active Directory Federation Services (AD FS), set up the Azure MFA Server.</span></span> <span data-ttu-id="b1718-108">Pour plus d’informations, consultez la rubrique [scénarios avancés avec Azure Multi-Factor Authentication et des solutions VPN tierces](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfaserver-nps-vpn) .</span><span class="sxs-lookup"><span data-stu-id="b1718-108">See [advanced scenarios with Azure Multi-Factor Authentication and third-party VPN solutions](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfaserver-nps-vpn) for more information.</span></span>

## <a name="step-1-decide-on-the-method-of-requiring-your-users-to-use-mfa"></a><span data-ttu-id="b1718-109">Étape 1 : décider de la méthode d’utilisation de l’authentification multifacteur par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="b1718-109">Step 1: Decide on the method of requiring your users to use MFA</span></span>

> [!NOTE]
> <span data-ttu-id="b1718-110">Vous devez être un administrateur général pour configurer ou modifier l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="b1718-110">You must be a global admin to set up or modify MFA.</span></span> <span data-ttu-id="b1718-111">Il existe trois façons de demander à vos utilisateurs d’utiliser l’authentification multifacteur pour les connexions. Pour plus d’informations, consultez la [prise en charge MFA dans Microsoft 365](multi-factor-authentication-microsoft-365.md) .</span><span class="sxs-lookup"><span data-stu-id="b1718-111">There are three ways to require your users to use MFA for sign-ins. See [MFA support in Microsoft 365](multi-factor-authentication-microsoft-365.md) for the details.</span></span>

- <span data-ttu-id="b1718-112">Paramètres de sécurité par défaut (recommandé pour les petites entreprises)</span><span class="sxs-lookup"><span data-stu-id="b1718-112">Security defaults (recommended for small businesses)</span></span>

  <span data-ttu-id="b1718-113">Si vous avez acheté votre abonnement ou une version d’évaluation après le 21 octobre 2019 et que vous êtes invité de manière inattendue à utiliser l’authentification multifacteur, les [paramètres de sécurité par défaut](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) ont été automatiquement activés pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1718-113">If you purchased your subscription or trial after October 21, 2019, and you're unexpectedly prompted for MFA, [security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) have been automatically enabled for your subscription.</span></span>
  
  <span data-ttu-id="b1718-114">Tous les nouveaux abonnements Microsoft 365 auront automatiquement des paramètres de sécurité par défaut activés.</span><span class="sxs-lookup"><span data-stu-id="b1718-114">Every new Microsoft 365 subscription will automatically have security defaults turned on.</span></span> <span data-ttu-id="b1718-115">Cela signifie que chaque utilisateur devra configurer MFA et installer l’application Microsoft Authenticator sur son appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="b1718-115">This means that every user will have to set up MFA and install the Microsoft Authenticator app on their mobile device.</span></span>

  <span data-ttu-id="b1718-116">Tous les utilisateurs doivent utiliser l’application Microsoft Authenticator comme méthode de vérification supplémentaire et l’authentification héritée est bloquée.</span><span class="sxs-lookup"><span data-stu-id="b1718-116">All users must use the Microsoft Authenticator app as their additional verification method and legacy authentication is blocked.</span></span> 

- <span data-ttu-id="b1718-117">Stratégies d’accès conditionnel (recommandé pour les entreprises)</span><span class="sxs-lookup"><span data-stu-id="b1718-117">Conditional Access policies (recommended for enterprises)</span></span>

  <span data-ttu-id="b1718-118">Les utilisateurs choisissent la méthode de vérification supplémentaire lors de l’inscription MFA.</span><span class="sxs-lookup"><span data-stu-id="b1718-118">Users choose the additional verification method during MFA registration.</span></span>

- <span data-ttu-id="b1718-119">Compte par utilisateur (non recommandé)</span><span class="sxs-lookup"><span data-stu-id="b1718-119">Per-user account (not recommended)</span></span>

  <span data-ttu-id="b1718-120">Les utilisateurs choisissent la méthode de vérification supplémentaire lors de l’inscription MFA.</span><span class="sxs-lookup"><span data-stu-id="b1718-120">Users choose the additional verification method during MFA registration.</span></span>

## <a name="step-2-test-mfa-on-your-pilot-users"></a><span data-ttu-id="b1718-121">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="b1718-121">Step 2.</span></span> <span data-ttu-id="b1718-122">Test MFA sur vos utilisateurs pilotes</span><span class="sxs-lookup"><span data-stu-id="b1718-122">Test MFA on your pilot users</span></span>

<span data-ttu-id="b1718-123">Si vous utilisez des stratégies d’accès conditionnel ou l’authentification multifacteur (MFA) par utilisateur (non recommandé), sélectionnez les utilisateurs pilotes de votre entreprise ou organisation pour tester l’inscription et les connexions MFA. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b1718-123">If you are using Conditional Access policies or per-user MFA (not recommended), select pilot users in your business or organization to test MFA registration and sign-ins. For example:</span></span>

- <span data-ttu-id="b1718-124">Pour les stratégies d’accès conditionnel, créez un groupe d’utilisateurs pilotes et une stratégie qui requiert l’authentification multifacteur pour les membres du groupe et pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="b1718-124">For Conditional Access policies, create a pilot users group and a policy that requires MFA for the members of the group and for all apps.</span></span> <span data-ttu-id="b1718-125">Ensuite, ajoutez les comptes de votre utilisateur pilote au groupe.</span><span class="sxs-lookup"><span data-stu-id="b1718-125">Then, add your pilot user’s accounts to the group.</span></span>

- <span data-ttu-id="b1718-126">Pour l’authentification multifacteur par utilisateur, activez une authentification multifacteur (MFA) pour les comptes d’utilisateur de vos utilisateurs pilotes un par un.</span><span class="sxs-lookup"><span data-stu-id="b1718-126">For per-user MFA, enable MFA for the user accounts of your pilot users one a time.</span></span>

<span data-ttu-id="b1718-127">Collaborez avec vos utilisateurs pilotes pour répondre à des questions et des problèmes afin de préparer un déploiement en douceur pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b1718-127">Work with your pilot users to address questions and issues to prepare for a smooth roll out to your organization.</span></span>

## <a name="step-3-inform-your-organization-that-mfa-is-coming"></a><span data-ttu-id="b1718-128">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="b1718-128">Step 3.</span></span> <span data-ttu-id="b1718-129">Informer votre organisation de l’arrivée à l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="b1718-129">Inform your organization that MFA is coming</span></span>

<span data-ttu-id="b1718-130">Utilisez des notifications par courrier électronique, des affiches de couloir, des réunions d’équipe ou une formation formelle pour vous assurer que vos employés comprennent :</span><span class="sxs-lookup"><span data-stu-id="b1718-130">Use email notifications, hallway posters, team meetings, or formal training to ensure that your employees understand:</span></span>

- <span data-ttu-id="b1718-131">Pourquoi la MFA est-elle nécessaire pour les connexions ?</span><span class="sxs-lookup"><span data-stu-id="b1718-131">Why MFA is being required for sign-ins</span></span>
- [<span data-ttu-id="b1718-132">Comment s’inscrire pour obtenir une autre méthode de vérification</span><span class="sxs-lookup"><span data-stu-id="b1718-132">How to register for their additional verification method</span></span>](https://support.office.com/article/set-up-your-microsoft-365-sign-in-for-multi-factor-authentication-ace1d096-61e5-449b-a875-58eb3d74de14?ui=en-US&rs=en-001&ad=US)
- [<span data-ttu-id="b1718-133">Comment se connecter après l’inscription</span><span class="sxs-lookup"><span data-stu-id="b1718-133">How to sign-in after registration</span></span>](https://support.office.com/article/sign-in-to-microsoft-365-with-multi-factor-authentication-2b856342-170a-438e-9a4f-3c092394d3cb)
- [<span data-ttu-id="b1718-134">Comment modifier la méthode de vérification supplémentaire</span><span class="sxs-lookup"><span data-stu-id="b1718-134">How to change their additional verification method</span></span>](https://support.office.com/article/change-how-you-do-additional-verification-956ec8d0-7081-4518-a701-f8414cc20831)
- [<span data-ttu-id="b1718-135">Comment traiter des situations comme un nouveau téléphone intelligent ?</span><span class="sxs-lookup"><span data-stu-id="b1718-135">How to deal with situations like a new smart phone</span></span>](https://support.office.com/article/fix-common-problems-with-multi-factor-authentication-6951be76-af50-49a4-847f-21391eaa59f2)

<span data-ttu-id="b1718-136">Plus important encore, assurez-vous que vos employés comprennent ***quand les exigences MFA doivent être imposées*** afin de ne pas les surcharger.</span><span class="sxs-lookup"><span data-stu-id="b1718-136">Most importantly, make sure your employees understand ***when the MFA requirement is going to be imposed*** so that it does not surprise them.</span></span>

## <a name="step-4-roll-out-the-mfa-requirement-to-your-organization-or-users"></a><span data-ttu-id="b1718-137">Étape 4.</span><span class="sxs-lookup"><span data-stu-id="b1718-137">Step 4.</span></span> <span data-ttu-id="b1718-138">Déployer l’authentification multifacteur (MFA) pour votre organisation ou vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="b1718-138">Roll out the MFA requirement to your organization or users</span></span>

<span data-ttu-id="b1718-139">En fonction de la méthode d’authentification multifacteur que vous avez choisie, déployez l’authentification MFA auprès des employés au-delà de vos testeurs pilotes.</span><span class="sxs-lookup"><span data-stu-id="b1718-139">Based on your chosen MFA requirement method, roll out MFA authentication to the employees beyond your pilot testers.</span></span>

### <a name="security-defaults"></a><span data-ttu-id="b1718-140">Paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="b1718-140">Security defaults</span></span>

<span data-ttu-id="b1718-141">Vous activez ou désactivez les paramètres de sécurité par défaut dans le volet des **Propriétés** d’Azure Active Directory (Azure AD) dans le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="b1718-141">You enable or disable security defaults from the **Properties** pane for Azure Active Directory (Azure AD) in the Azure portal.</span></span>

1.  <span data-ttu-id="b1718-142">Connectez-vous au [Centre d’administration 365 de Microsoft](https://admin.microsoft.com) avec les informations d’identification d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="b1718-142">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with global admin credentials.</span></span>
2.  <span data-ttu-id="b1718-143">Accédez à la [page Propriétés Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="b1718-143">Go to the [Azure Active Directory - Properties page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span>
3.  <span data-ttu-id="b1718-144">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="b1718-144">At the bottom of the page, choose **Manage Security defaults**.</span></span>
4.  <span data-ttu-id="b1718-145">Choisissez **Oui** pour activer les paramètres de sécurité par défaut et **non** pour désactiver les paramètres de sécurité par défaut, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b1718-145">Choose **Yes** to enable security defaults and **No** to disable security defaults, and then choose **Save**.</span></span>

<span data-ttu-id="b1718-146">Si vous avez utilisé des [stratégies d’accès conditionnel de référence](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection), voici comment vous pouvez utiliser les paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="b1718-146">If you have been using [baseline Conditional Access policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection), here is how you move to using security defaults.</span></span>

1.  <span data-ttu-id="b1718-147">Accédez à la [page des stratégies d’accès conditionnel](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).</span><span class="sxs-lookup"><span data-stu-id="b1718-147">Go to the [Conditional Access - Policies page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).</span></span>
2.  <span data-ttu-id="b1718-148">Choisissez chaque stratégie de planification qui est **activée** et définissez **activer la stratégie** sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="b1718-148">Choose each baseline policy that is **On** and set **Enable policy** to **Off**.</span></span>
2.  <span data-ttu-id="b1718-149">Accédez à la [page Propriétés Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="b1718-149">Go to the [Azure Active Directory - Properties page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span>
4.  <span data-ttu-id="b1718-150">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="b1718-150">At the bottom of the page, choose **Manage Security defaults**.</span></span>
5.  <span data-ttu-id="b1718-151">Choisissez **Oui** pour activer les paramètres de sécurité par défaut et **non** pour désactiver les paramètres de sécurité par défaut, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b1718-151">Choose **Yes** to enable security defaults and **No** to disable security defaults, and then choose **Save**.</span></span>

### <a name="conditional-access-policies"></a><span data-ttu-id="b1718-152">Stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="b1718-152">Conditional Access policies</span></span>

<span data-ttu-id="b1718-153">Créez, configurez et activez les stratégies appropriées qui incluent le groupe d’utilisateurs qui nécessitent l’authentification MFA pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="b1718-153">Create, configure, and enable the appropriate policies that include the group of users that require MFA for sign-in.</span></span>

### <a name="per-user-mfa-not-recommended"></a><span data-ttu-id="b1718-154">Authentification multifacteur par utilisateur (non recommandé)</span><span class="sxs-lookup"><span data-stu-id="b1718-154">Per-user MFA (not recommended)</span></span>

<span data-ttu-id="b1718-155">Activez les comptes d’utilisateur pour MFA correspondant à votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="b1718-155">Enable user accounts for MFA corresponding to your rollout.</span></span>

### <a name="supporting-your-employees"></a><span data-ttu-id="b1718-156">Prise en charge de vos employés</span><span class="sxs-lookup"><span data-stu-id="b1718-156">Supporting your employees</span></span>

<span data-ttu-id="b1718-157">À mesure que vos employés s’inscrivent et commencent à se connecter avec l’authentification multifacteur, assurez-vous que vos spécialistes informatiques, votre service informatique ou le support technique peuvent répondre rapidement à des questions et résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="b1718-157">As your employees register and begin signing in with MFA, ensure that your IT specialists, IT department, or helpdesk can answer questions and address issues quickly.</span></span>

<span data-ttu-id="b1718-158">Consultez cet article pour obtenir des [informations sur la résolution des problèmes de connexion MFA](https://support.office.com/article/fix-common-problems-with-multi-factor-authentication-6951be76-af50-49a4-847f-21391eaa59f2).</span><span class="sxs-lookup"><span data-stu-id="b1718-158">See this article for [information about troubleshooting MFA sign-ins](https://support.office.com/article/fix-common-problems-with-multi-factor-authentication-6951be76-af50-49a4-847f-21391eaa59f2).</span></span> 


