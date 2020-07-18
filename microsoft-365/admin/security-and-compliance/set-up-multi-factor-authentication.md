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
ms.openlocfilehash: 597d8383166e0ddae0984573d77ba75cf54dafdd
ms.sourcegitcommit: 9af890ef1b1c95bfc7cc52f7f4e395b62dc5263f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "45146229"
---
# <a name="set-up-multi-factor-authentication"></a><span data-ttu-id="e7842-103">Configurer Multi-factor Authentification (MFA)</span><span class="sxs-lookup"><span data-stu-id="e7842-103">Set up multi-factor authentication</span></span>
  
<span data-ttu-id="e7842-104">En fonction de votre compréhension de [l’authentification multifacteur (MFA) et de sa prise en charge dans Microsoft 365](multi-factor-authentication-microsoft-365.md), le moment est venu de la configurer et de la déployer dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e7842-104">Based on your understanding of [multi-factor authentication (MFA) and its support in Microsoft 365](multi-factor-authentication-microsoft-365.md), it’s time to set it up and roll it out to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7842-105">Si vous avez acheté votre abonnement ou une version d’évaluation après le 21 octobre 2019 et que vous êtes, de manière, invité à fournir une authentification multifacteur lors de la connexion, [les valeurs de sécurité par défaut](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) ont été automatiquement activées pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7842-105">If you purchased your subscription or trial after October 21, 2019, and you're prompted for MFA when you sign in, [security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) have been automatically enabled for your subscription.</span></span>


## <a name="before-you-begin"></a><span data-ttu-id="e7842-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e7842-106">Before you begin</span></span>

- <span data-ttu-id="e7842-107">Vous devez être un administrateur général pour gérer l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="e7842-107">You must be a Global admin to manage MFA.</span></span> <span data-ttu-id="e7842-108">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e7842-108">For more information, see [About admin roles](../add-users/about-admin-roles.md).</span></span>
- <span data-ttu-id="e7842-109">Si l’authentification multifacteur hérité est activée, [Désactiver l'héritage multifacteur héritée par personne](#turn-off-legacy-per-person-mfa).</span><span class="sxs-lookup"><span data-stu-id="e7842-109">If you have legacy per person MFA turned on, [Turn off legacy per person MFA](#turn-off-legacy-per-person-mfa).</span></span>
- <span data-ttu-id="e7842-110">Si vous avez des clients Office 2013 sur des appareils Windows, [activer l’authentification moderne pour les clients Office 2013](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/enable-modern-authentication).</span><span class="sxs-lookup"><span data-stu-id="e7842-110">If you have Office 2013 clients on Windows devices, [turn on Modern Authentication for Office 2013 clients](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/enable-modern-authentication).</span></span>
- <span data-ttu-id="e7842-111">Avancé : si vous avez des services d’annuaire tiers avec les Services de fédération Active Directory (AD FS), configurez le serveur d’Authentification multifacteur Azure.</span><span class="sxs-lookup"><span data-stu-id="e7842-111">Advanced: If you have third-party directory services with Active Directory Federation Services (AD FS), set up the Azure MFA Server.</span></span> <span data-ttu-id="e7842-112">Pour plus d’informations, voir les [scénarios avancés avec l’Authentification multifacteur Azure et les solutions VPN tierces](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfaserver-nps-vpn).</span><span class="sxs-lookup"><span data-stu-id="e7842-112">See [advanced scenarios with Azure Multi-Factor Authentication and third-party VPN solutions](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfaserver-nps-vpn) for more information.</span></span>

## <a name="turn-security-defaults-on-or-off"></a><span data-ttu-id="e7842-113">Activer ou désactiver les paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="e7842-113">Turn Security defaults on or off</span></span>

<span data-ttu-id="e7842-114">Pour la plupart des organisations, les valeurs de sécurité par défaut offrent un niveau de sécurité de connexion supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="e7842-114">For most organizations, Security defaults offer a good level of additional sign-in security.</span></span> <span data-ttu-id="e7842-115">Pour plus d’informations, voir [Présentation des paramètres de sécurité par défaut](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)</span><span class="sxs-lookup"><span data-stu-id="e7842-115">For more information, see [What are security defaults?](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)</span></span>

<span data-ttu-id="e7842-116">Si votre abonnement est nouveau, les paramètres par défaut de sécurité peuvent déjà être activés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e7842-116">If your subscription is new, Security defaults might already be turned on for you automatically.</span></span>

<span data-ttu-id="e7842-117">Pour activer ou désactiver les paramètres de sécurité par défaut, accédez au volet **Propriétés** pour Azure Active Directory (Azure AD) dans le Portail Azure.</span><span class="sxs-lookup"><span data-stu-id="e7842-117">You enable or disable security defaults from the **Properties** pane for Azure Active Directory (Azure AD) in the Azure portal.</span></span>

1.  <span data-ttu-id="e7842-118">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) avec des informations d'identification d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="e7842-118">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with global admin credentials.</span></span>
2.  <span data-ttu-id="e7842-119">Dans le volet de navigation gauche, sélectionnez **Afficher tout** puis sous **Centres d’administration**, sélectionnez **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="e7842-119">In the left nav choose **Show All** and under **Admin centers**, choose **Azure Active Directory**.</span></span>
3. <span data-ttu-id="e7842-120">Dans le centre d’administration **Azure Active Directory** sélectionnez **Azure Active Directory** > **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="e7842-120">In the **Azure Active Directory admin center** choose **Azure Active Directory** > **Properties**.</span></span>
3.  <span data-ttu-id="e7842-121">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="e7842-121">At the bottom of the page, choose **Manage Security defaults**.</span></span>
4.  <span data-ttu-id="e7842-122">Sélectionnez **Oui** pour activer les paramètres de sécurité par défaut ou **Non** pour désactiver les paramètres de sécurité par défaut, puis choisissez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e7842-122">Choose **Yes** to enable security defaults or **No** to disable security defaults, and then choose **Save**.</span></span>

<span data-ttu-id="e7842-123">Si vous utilisez [stratégies d’accès conditionnel de référence](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection), vous serez invité à les désactiver avant de passer à l’utilisation des paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7842-123">If you have been using [baseline Conditional Access policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection), you will be prompted to turn them off before you move to using security defaults.</span></span>

1.  <span data-ttu-id="e7842-124">Accédez à la [page des stratégies d’accès conditionnel](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).</span><span class="sxs-lookup"><span data-stu-id="e7842-124">Go to the [Conditional Access - Policies page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).</span></span>
2.  <span data-ttu-id="e7842-125">Sélectionnez chaque stratégie de référence sur **Activé** et définissez **Activer la stratégie** sur **Désactivé**.</span><span class="sxs-lookup"><span data-stu-id="e7842-125">Choose each baseline policy that is **On** and set **Enable policy** to **Off**.</span></span>
2.  <span data-ttu-id="e7842-126">Accédez à la [page des propriétés d'Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="e7842-126">Go to the [Azure Active Directory - Properties page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span>
4.  <span data-ttu-id="e7842-127">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="e7842-127">At the bottom of the page, choose **Manage Security defaults**.</span></span>
5.  <span data-ttu-id="e7842-128">Sélectionnez **Oui** pour activer les paramètres de sécurité par défaut et **Non** pour désactiver les paramètres de sécurité par défaut, puis choisissez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e7842-128">Choose **Yes** to enable security defaults and **No** to disable security defaults, and then choose **Save**.</span></span>

## <a name="use-conditional-access-policies"></a><span data-ttu-id="e7842-129">Utiliser les stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="e7842-129">Use Conditional Access policies</span></span>

<span data-ttu-id="e7842-130">Si votre organisation a des besoins de sécurité de connexion plus granulaires, les stratégies d’accès conditionnel peuvent vous offrir davantage de contrôle.</span><span class="sxs-lookup"><span data-stu-id="e7842-130">If your organization has more granular sign-in security needs, Conditional Access policies can offer you more control.</span></span> <span data-ttu-id="e7842-131">L’accès conditionnel vous permet de créer et de définir des stratégies qui réagissent aux événements de connexion et de demander des actions supplémentaires avant qu’un utilisateur ne soit autorisé à accéder à une application ou un service.</span><span class="sxs-lookup"><span data-stu-id="e7842-131">Conditional Access lets you create and define policies that react to sign in events and request additional actions before a user is granted access to an application or service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7842-132">Désactivez les paramètres par défaut d'authentification multifacteur' et de sécurité par personne avant d'activer les stratégies d'accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="e7842-132">Turn off both per person MFA and Security defaults before you enable Conditional Access policies.</span></span> 

<span data-ttu-id="e7842-133">L’accès conditionnel est disponible pour les clients qui ont acheté Azure AD Premium P1 ou les licences qui incluent cette offre, telles que Microsoft 365 Business Premium et Microsoft 365 E3.</span><span class="sxs-lookup"><span data-stu-id="e7842-133">Conditional Access is available for customers who have purchased Azure AD Premium P1, or licenses that include this, such as Microsoft 365 Business Premium, and Microsoft 365 E3.</span></span> <span data-ttu-id="e7842-134">Pour en savoir plus, consultez [Créer une stratégie d’accès conditionnel](https://docs.microsoft.com/azure/active-directory/authentication/tutorial-enable-azure-mfa).</span><span class="sxs-lookup"><span data-stu-id="e7842-134">For more information, see [create a Conditional Access policy](https://docs.microsoft.com/azure/active-directory/authentication/tutorial-enable-azure-mfa).</span></span>

<span data-ttu-id="e7842-135">L’accès conditionnel basé sur les risques est disponible via une licence Azure AD Premium P2, ou les licences qui l’incluent, telles que Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="e7842-135">Risk-based conditional access is available through Azure AD Premium P2 license, or licences that include this, such as Microsoft 365 E5.</span></span> <span data-ttu-id="e7842-136">Pour en savoir plus, consultez l'article [Accès conditionnel basé sur les risques](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-risk).</span><span class="sxs-lookup"><span data-stu-id="e7842-136">For more information, see [risk-based Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-risk).</span></span>

### <a name="turn-on-modern-authentication-for-your-organization"></a><span data-ttu-id="e7842-137">Activer Authentification moderne pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="e7842-137">Turn on Modern authentication for your organization</span></span>

<span data-ttu-id="e7842-138">Pour la plupart des abonnements, l'authentification moderne est automatiquement activée, mais si vous avez acheté votre abonnement il y a longtemps, il se peut qu'elle ne le soit pas.</span><span class="sxs-lookup"><span data-stu-id="e7842-138">For most subscriptions modern authentication is automatically turned on, but if you purchased your subscription a long time ago, it might not be.</span></span> <span data-ttu-id="e7842-139">Celle-ci doit être activée avant que l’authentification multifacteur fonctionne convenablement avec les applications Office.</span><span class="sxs-lookup"><span data-stu-id="e7842-139">This has to be turned on before MFA works appropriately with Office apps.</span></span>

1. <span data-ttu-id="e7842-140">Dans le Centre d’administration Microsoft 365, dans le volet de navigation gauche, sélectionnez **Paramètres** > **Paramètres d’organisation**.</span><span class="sxs-lookup"><span data-stu-id="e7842-140">In the Microsoft 365 admin center, in the left nav choose **Settings** > **Org settings**.</span></span>
1. <span data-ttu-id="e7842-141">Sous l’onglet **Services**, sélectionnez **Authentification moderne**, puis, dans le volet **Authentification moderne**, assurez-vous que l’option **Activer l’authentification moderne** est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e7842-141">Under **Services** tab, choose **Modern authentication**, and in the **Modern authentication** pane, make sure **Enable Modern authentication** is selected.</span></span> <span data-ttu-id="e7842-142">Sélectionnez **Save Changes (Enregistrer les modifications)**.</span><span class="sxs-lookup"><span data-stu-id="e7842-142">Choose **Save changes**.</span></span>

### <a name="turn-off-legacy-per-person-mfa"></a><span data-ttu-id="e7842-143">Désactiver l’authentification multifacteur héritée par personne</span><span class="sxs-lookup"><span data-stu-id="e7842-143">Turn off legacy per person MFA</span></span>

<span data-ttu-id="e7842-144">Si vous avez déjà activé l’authentification multifacteur (MFA) par personne, vous devez désactiver cette fonctionnalité avant d’activer les paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7842-144">If you have previously turned on per person MFA, you must turn it off before enabling Security defaults.</span></span>

1. <span data-ttu-id="e7842-145">Dans le Centre d’administration Microsoft 365, dans le volet de navigation gauche, sélectionnez **Paramètres** > **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="e7842-145">In the Microsoft 365 admin center, in the left nav choose **Users** > **Active users**.</span></span> 
1. <span data-ttu-id="e7842-146">Sur la page **Utilisateurs actifs**, sélectionnez **Authentification multifacteur**.</span><span class="sxs-lookup"><span data-stu-id="e7842-146">On the **Active users** page, choose **Multi-factor authentication**.</span></span>
1. <span data-ttu-id="e7842-147">Sur la page d'authentification multifacteur, sélectionnez chaque utilisateur et définissez son état d'authentification multifacteur sur **Désactivé**.</span><span class="sxs-lookup"><span data-stu-id="e7842-147">On the multi-factor authentication page, select each user and set their Multi-Factor auth status to **Disabled**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e7842-148">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e7842-148">Next steps</span></span>

- [<span data-ttu-id="e7842-149">Comment s’inscrire à leur méthode de vérification supplémentaire</span><span class="sxs-lookup"><span data-stu-id="e7842-149">How to register for their additional verification method</span></span>](https://support.microsoft.com/office/ace1d096-61e5-449b-a875-58eb3d74de14)
- [<span data-ttu-id="e7842-150">Comment se connecter après l’inscription</span><span class="sxs-lookup"><span data-stu-id="e7842-150">How to sign-in after registration</span></span>](https://support.microsoft.com/office/2b856342-170a-438e-9a4f-3c092394d3cb)
- [<span data-ttu-id="e7842-151">Comment modifier leur méthode de vérification supplémentaire</span><span class="sxs-lookup"><span data-stu-id="e7842-151">How to change their additional verification method</span></span>](https://support.microsoft.com/office/956ec8d0-7081-4518-a701-f8414cc20831)
- [<span data-ttu-id="e7842-152">Comment gérer les situations telles qu’un nouveau smartphone</span><span class="sxs-lookup"><span data-stu-id="e7842-152">How to deal with situations like a new smart phone</span></span>](https://support.microsoft.com/office/6951be76-af50-49a4-847f-21391eaa59f2)
- [<span data-ttu-id="e7842-153">Résoudre les problèmes liés aux connexions par authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="e7842-153">Troubleshoot MFA sign-ins</span></span>](https://support.microsoft.com/office/6951be76-af50-49a4-847f-21391eaa59f2)




