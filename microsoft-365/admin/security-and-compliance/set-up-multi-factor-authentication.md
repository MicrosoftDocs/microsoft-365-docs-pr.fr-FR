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
localization_priority: Priority
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
ms.openlocfilehash: 56ca51e77b2ba4fa370a2814a7be9df1393c29dc
ms.sourcegitcommit: 3951147f74510e2ead6c11ceab92854f0937426b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2020
ms.locfileid: "45083537"
---
# <a name="set-up-multi-factor-authentication"></a><span data-ttu-id="6becc-103">Configurer Multi-factor Authentification (MFA)</span><span class="sxs-lookup"><span data-stu-id="6becc-103">Set up multi-factor authentication</span></span>
  
<span data-ttu-id="6becc-104">En fonction de votre compréhension de [l’authentification multifacteur (MFA) et de sa prise en charge dans Microsoft 365](multi-factor-authentication-microsoft-365.md), le moment est venu de la configurer et de la déployer dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6becc-104">Based on your understanding of [multi-factor authentication (MFA) and its support in Microsoft 365](multi-factor-authentication-microsoft-365.md), it’s time to set it up and roll it out to your organization.</span></span>

<span data-ttu-id="6becc-105">Avant de commencer, déterminez si ces conditions spéciales s’appliquent à votre situation et effectuez l’action appropriée :</span><span class="sxs-lookup"><span data-stu-id="6becc-105">Before you begin, determine if these special conditions apply to you and take the appropriate action:</span></span>

- <span data-ttu-id="6becc-106">Si vous avez des clients Office 2013 sur des appareils Windows, [activer l’authentification moderne](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/enable-modern-authentication).</span><span class="sxs-lookup"><span data-stu-id="6becc-106">If you have Office 2013 clients on Windows devices, [enable Modern Authentication](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/enable-modern-authentication).</span></span>

- <span data-ttu-id="6becc-107">Si vous avez des services d’annuaire tiers avec les Services de fédération Active Directory (AD FS), configurez le serveur d’Authentification multifacteur Azure.</span><span class="sxs-lookup"><span data-stu-id="6becc-107">If you have third-party directory services with Active Directory Federation Services (AD FS), set up the Azure MFA Server.</span></span> <span data-ttu-id="6becc-108">Pour plus d’informations, voir les [scénarios avancés avec l’Authentification multifacteur Azure et les solutions VPN tierces](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfaserver-nps-vpn).</span><span class="sxs-lookup"><span data-stu-id="6becc-108">See [advanced scenarios with Azure Multi-Factor Authentication and third-party VPN solutions](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfaserver-nps-vpn) for more information.</span></span>

<span data-ttu-id="6becc-109">Tous les autres utilisateurs seront invités à effectuer une authentification supplémentaire si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6becc-109">All other users will be asked to perform additional authentication when needed.</span></span> <span data-ttu-id="6becc-110">Si vous souhaitez obtenir plus d’informations, veuillez visiter la [Méthode et les paramètres de vérification à deux facteurs](https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-manage-settings#turn-on-two-factor-verification-prompts-on-a-trusted-device).</span><span class="sxs-lookup"><span data-stu-id="6becc-110">For more information, please visit [Two-factor verification method and settings](https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-manage-settings#turn-on-two-factor-verification-prompts-on-a-trusted-device).</span></span>

## <a name="step-1-decide-on-the-method-of-requiring-your-users-to-use-mfa"></a><span data-ttu-id="6becc-111">Étape 1 : décider de la méthode consistant à exiger des utilisateurs qu’ils utilisent l’authentification multifacteur (MFA)</span><span class="sxs-lookup"><span data-stu-id="6becc-111">Step 1: Decide on the method of requiring your users to use MFA</span></span>

> [!NOTE]
> <span data-ttu-id="6becc-112">Vous devez être un administrateur général pour configurer ou modifier l’authentification multifacteur (MFA).</span><span class="sxs-lookup"><span data-stu-id="6becc-112">You must be a global admin to set up or modify MFA.</span></span> <span data-ttu-id="6becc-113">Trois méthodes s’offrent à vous pour exiger de vos utilisateurs qu’ils utilisent l’authentification multifacteur pour les connexions. Pour plus d’informations, voir [Prise en charge de l’authentification multifacteur dans Microsoft 365](multi-factor-authentication-microsoft-365.md).</span><span class="sxs-lookup"><span data-stu-id="6becc-113">There are three ways to require your users to use MFA for sign-ins. See [MFA support in Microsoft 365](multi-factor-authentication-microsoft-365.md) for the details.</span></span>

- <span data-ttu-id="6becc-114">Paramètres de sécurité par défaut (recommandés pour les petites entreprises)</span><span class="sxs-lookup"><span data-stu-id="6becc-114">Security defaults (recommended for small businesses)</span></span>

  <span data-ttu-id="6becc-115">Si vous avez acheté votre abonnement ou une version d’évaluation après le 21 octobre 2019 et que vous êtes, de manière inattendue, invité à fournir une authentification multifacteur, [les valeurs de sécurité par défaut](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) ont été automatiquement activées pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="6becc-115">If you purchased your subscription or trial after October 21, 2019, and you're unexpectedly prompted for MFA, [security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) have been automatically enabled for your subscription.</span></span>
  
  <span data-ttu-id="6becc-116">Les paramètres de sécurité par défaut sont automatiquement activés avec tout nouvel abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6becc-116">Every new Microsoft 365 subscription will automatically have security defaults turned on.</span></span> <span data-ttu-id="6becc-117">Chaque utilisateur doit ainsi configurer l’authentification multifacteur (MFA) et installer l’application Microsoft Authenticator sur son appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="6becc-117">This means that every user will have to set up MFA and install the Microsoft Authenticator app on their mobile device.</span></span>

  <span data-ttu-id="6becc-118">Tous les utilisateurs doivent utiliser l’application Microsoft Authenticator en tant que méthode de vérification supplémentaire et l’authentification héritée est bloquée.</span><span class="sxs-lookup"><span data-stu-id="6becc-118">All users must use the Microsoft Authenticator app as their additional verification method and legacy authentication is blocked.</span></span> 

- <span data-ttu-id="6becc-119">Stratégies d’accès conditionnel (recommandé pour les entreprises)</span><span class="sxs-lookup"><span data-stu-id="6becc-119">Conditional Access policies (recommended for enterprises)</span></span>

  <span data-ttu-id="6becc-120">Les utilisateurs choisissent la méthode de vérification supplémentaire pendant l’inscription à l’authentification multifacteur (MFA).</span><span class="sxs-lookup"><span data-stu-id="6becc-120">Users choose the additional verification method during MFA registration.</span></span>

- <span data-ttu-id="6becc-121">Compte par utilisateur (non recommandé)</span><span class="sxs-lookup"><span data-stu-id="6becc-121">Per-user account (not recommended)</span></span>

  <span data-ttu-id="6becc-122">Les utilisateurs choisissent la méthode de vérification supplémentaire pendant l’inscription à l’authentification multifacteur (MFA).</span><span class="sxs-lookup"><span data-stu-id="6becc-122">Users choose the additional verification method during MFA registration.</span></span>

## <a name="step-2-test-mfa-on-your-pilot-users"></a><span data-ttu-id="6becc-123">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="6becc-123">Step 2.</span></span> <span data-ttu-id="6becc-124">Tester l’authentification multifacteur (MFA) sur vos utilisateurs pilotes</span><span class="sxs-lookup"><span data-stu-id="6becc-124">Test MFA on your pilot users</span></span>

<span data-ttu-id="6becc-125">Si vous utilisez des stratégies d’accès conditionnel ou l’authentification multifacteur (MFA) par utilisateur (non recommandé), sélectionnez les utilisateurs pilotes au sein de votre entreprise ou organisation pour tester l’inscription à l’authentification multifacteur et les connexions. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6becc-125">If you are using Conditional Access policies or per-user MFA (not recommended), select pilot users in your business or organization to test MFA registration and sign-ins. For example:</span></span>

- <span data-ttu-id="6becc-126">Pour les stratégies d’accès conditionnel, créez un groupe d’utilisateurs pilotes et une stratégie nécessitant une authentification multifacteur (MFA) pour les membres du groupe et toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="6becc-126">For Conditional Access policies, create a pilot users group and a policy that requires MFA for the members of the group and for all apps.</span></span> <span data-ttu-id="6becc-127">Ajoutez ensuite les comptes de vos utilisateurs pilotes au groupe.</span><span class="sxs-lookup"><span data-stu-id="6becc-127">Then, add your pilot user’s accounts to the group.</span></span>

- <span data-ttu-id="6becc-128">Pour l’authentification multifacteur (MFA) par utilisateur, activez-la pour les comptes d’utilisateurs de vos utilisateurs pilotes l’un après l’autre.</span><span class="sxs-lookup"><span data-stu-id="6becc-128">For per-user MFA, enable MFA for the user accounts of your pilot users one a time.</span></span>

<span data-ttu-id="6becc-129">Collaborez avec vos utilisateurs pilotes pour répondre aux questions et problèmes afin de préparer un déploiement parfait pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6becc-129">Work with your pilot users to address questions and issues to prepare for a smooth roll out to your organization.</span></span>

## <a name="step-3-inform-your-organization-that-mfa-is-coming"></a><span data-ttu-id="6becc-130">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="6becc-130">Step 3.</span></span> <span data-ttu-id="6becc-131">Informez votre organisation que l’authentification multifacteur arrive bientôt</span><span class="sxs-lookup"><span data-stu-id="6becc-131">Inform your organization that MFA is coming</span></span>

<span data-ttu-id="6becc-132">Utilisez des notifications par courrier électronique, des affiches dans les couloirs, des réunions d’équipe ou une formation officielle afin de vérifier que vos employés comprennent :</span><span class="sxs-lookup"><span data-stu-id="6becc-132">Use email notifications, hallway posters, team meetings, or formal training to ensure that your employees understand:</span></span>

- <span data-ttu-id="6becc-133">Pourquoi l’authentification multifacteur est exigée pour les connexions</span><span class="sxs-lookup"><span data-stu-id="6becc-133">Why MFA is being required for sign-ins</span></span>
- [<span data-ttu-id="6becc-134">Comment s’inscrire à leur méthode de vérification supplémentaire</span><span class="sxs-lookup"><span data-stu-id="6becc-134">How to register for their additional verification method</span></span>](https://support.microsoft.com/office/ace1d096-61e5-449b-a875-58eb3d74de14)
- [<span data-ttu-id="6becc-135">Comment se connecter après l’inscription</span><span class="sxs-lookup"><span data-stu-id="6becc-135">How to sign-in after registration</span></span>](https://support.microsoft.com/office/2b856342-170a-438e-9a4f-3c092394d3cb)
- [<span data-ttu-id="6becc-136">Comment modifier leur méthode de vérification supplémentaire</span><span class="sxs-lookup"><span data-stu-id="6becc-136">How to change their additional verification method</span></span>](https://support.microsoft.com/office/956ec8d0-7081-4518-a701-f8414cc20831)
- [<span data-ttu-id="6becc-137">Comment gérer les situations telles qu’un nouveau smartphone</span><span class="sxs-lookup"><span data-stu-id="6becc-137">How to deal with situations like a new smart phone</span></span>](https://support.microsoft.com/office/6951be76-af50-49a4-847f-21391eaa59f2)

<span data-ttu-id="6becc-138">Assurez-vous surtout que vos employés sachent ***à quel moment l’authentification multifacteur va être imposée*** afin qu’ils ne soient pas surpris.</span><span class="sxs-lookup"><span data-stu-id="6becc-138">Most importantly, make sure your employees understand ***when the MFA requirement is going to be imposed*** so that it does not surprise them.</span></span>

## <a name="step-4-roll-out-the-mfa-requirement-to-your-organization-or-users"></a><span data-ttu-id="6becc-139">Étape 4.</span><span class="sxs-lookup"><span data-stu-id="6becc-139">Step 4.</span></span> <span data-ttu-id="6becc-140">Déployer les conditions pour l’authentification multifacteur (MFA) pour votre organisation ou vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6becc-140">Roll out the MFA requirement to your organization or users</span></span>

<span data-ttu-id="6becc-141">Selon la méthode d’exigence choisie de l’authentification multifacteur, déployez l’authentification multifacteur (MFA) auprès des employés au-delà de vos testeurs pilotes.</span><span class="sxs-lookup"><span data-stu-id="6becc-141">Based on your chosen MFA requirement method, roll out MFA authentication to the employees beyond your pilot testers.</span></span>

### <a name="security-defaults"></a><span data-ttu-id="6becc-142">Paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="6becc-142">Security defaults</span></span>

<span data-ttu-id="6becc-143">Pour activer ou désactiver les paramètres de sécurité par défaut, accédez au volet **Propriétés** pour Azure Active Directory (Azure AD) dans le Portail Azure.</span><span class="sxs-lookup"><span data-stu-id="6becc-143">You enable or disable security defaults from the **Properties** pane for Azure Active Directory (Azure AD) in the Azure portal.</span></span>

1.  <span data-ttu-id="6becc-144">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) avec des informations d'identification d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="6becc-144">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with global admin credentials.</span></span>
2.  <span data-ttu-id="6becc-145">Accédez à la [page des propriétés d'Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="6becc-145">Go to the [Azure Active Directory - Properties page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span>
3.  <span data-ttu-id="6becc-146">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="6becc-146">At the bottom of the page, choose **Manage Security defaults**.</span></span>
4.  <span data-ttu-id="6becc-147">Sélectionnez **Oui** pour activer les paramètres de sécurité par défaut et **Non** pour désactiver les paramètres de sécurité par défaut, puis choisissez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6becc-147">Choose **Yes** to enable security defaults and **No** to disable security defaults, and then choose **Save**.</span></span>

<span data-ttu-id="6becc-148">Si vous utilisez des [stratégies d’accès conditionnel de référence](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection), voici comment vous pouvez utiliser les paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="6becc-148">If you have been using [baseline Conditional Access policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection), here is how you move to using security defaults.</span></span>

1.  <span data-ttu-id="6becc-149">Accédez à la [page des stratégies d’accès conditionnel](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).</span><span class="sxs-lookup"><span data-stu-id="6becc-149">Go to the [Conditional Access - Policies page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).</span></span>
2.  <span data-ttu-id="6becc-150">Sélectionnez chaque stratégie de référence sur **Activé** et définissez **Activer la stratégie** sur **Désactivé**.</span><span class="sxs-lookup"><span data-stu-id="6becc-150">Choose each baseline policy that is **On** and set **Enable policy** to **Off**.</span></span>
2.  <span data-ttu-id="6becc-151">Accédez à la [page des propriétés d'Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="6becc-151">Go to the [Azure Active Directory - Properties page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span>
4.  <span data-ttu-id="6becc-152">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="6becc-152">At the bottom of the page, choose **Manage Security defaults**.</span></span>
5.  <span data-ttu-id="6becc-153">Sélectionnez **Oui** pour activer les paramètres de sécurité par défaut et **Non** pour désactiver les paramètres de sécurité par défaut, puis choisissez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6becc-153">Choose **Yes** to enable security defaults and **No** to disable security defaults, and then choose **Save**.</span></span>

### <a name="conditional-access-policies"></a><span data-ttu-id="6becc-154">Stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="6becc-154">Conditional Access policies</span></span>

<span data-ttu-id="6becc-155">Créez, configurez et activez les stratégies appropriées qui incluent le groupe d’utilisateurs qui ont besoin de l’authentification multifacteur pour se connecter.</span><span class="sxs-lookup"><span data-stu-id="6becc-155">Create, configure, and enable the appropriate policies that include the group of users that require MFA for sign-in.</span></span>

### <a name="per-user-mfa-not-recommended"></a><span data-ttu-id="6becc-156">Authentification multifacteur (MFA) par utilisateur (non recommandé)</span><span class="sxs-lookup"><span data-stu-id="6becc-156">Per-user MFA (not recommended)</span></span>

<span data-ttu-id="6becc-157">Activez les comptes d’utilisateur pour l’authentification multifacteur (MFA) correspondant à votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="6becc-157">Enable user accounts for MFA corresponding to your rollout.</span></span>

### <a name="supporting-your-employees"></a><span data-ttu-id="6becc-158">Support de vos employés</span><span class="sxs-lookup"><span data-stu-id="6becc-158">Supporting your employees</span></span>

<span data-ttu-id="6becc-159">Au fur et à mesure que vos employés s’inscrivent et commencent à se connecter avec l’authentification multifacteur, assurez-vous que vos spécialistes informatiques, votre service informatique ou votre support technique peuvent répondre aux questions et résoudre rapidement des problèmes.</span><span class="sxs-lookup"><span data-stu-id="6becc-159">As your employees register and begin signing in with MFA, ensure that your IT specialists, IT department, or helpdesk can answer questions and address issues quickly.</span></span>

<span data-ttu-id="6becc-160">Consultez cet article pour des [informations sur la résolution des problèmes liés aux connexions via l’authentification multifacteur (MFA)](https://support.microsoft.com/office/6951be76-af50-49a4-847f-21391eaa59f2).</span><span class="sxs-lookup"><span data-stu-id="6becc-160">See this article for [information about troubleshooting MFA sign-ins](https://support.microsoft.com/office/6951be76-af50-49a4-847f-21391eaa59f2).</span></span> 


