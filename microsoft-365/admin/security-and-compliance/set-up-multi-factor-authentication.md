---
title: Configurer l'authentification multifacteur pour les utilisateurs
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
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
ms.openlocfilehash: 480e09e42ea53cc78cd738a6e0650feae7a9f8c8
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635949"
---
# <a name="set-up-multi-factor-authentication"></a><span data-ttu-id="0df74-103">Configurer Multi-factor Authentification (MFA)</span><span class="sxs-lookup"><span data-stu-id="0df74-103">Set up multi-factor authentication</span></span>

<span data-ttu-id="0df74-104">En fonction de votre compréhension de [l’authentification multifacteur (MFA) et de sa prise en charge dans Microsoft 365](multi-factor-authentication-microsoft-365.md), le moment est venu de la configurer et de la déployer dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0df74-104">Based on your understanding of [multi-factor authentication (MFA) and its support in Microsoft 365](multi-factor-authentication-microsoft-365.md), it's time to set it up and roll it out to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0df74-105">Si vous avez acheté votre abonnement ou une version d’évaluation après le 21 octobre 2019 et que vous êtes, de manière, invité à fournir une authentification multifacteur lors de la connexion, [les valeurs de sécurité par défaut](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) ont été automatiquement activées pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="0df74-105">If you purchased your subscription or trial after October 21, 2019, and you're prompted for MFA when you sign in, [security defaults](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) have been automatically enabled for your subscription.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="0df74-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0df74-106">Before you begin</span></span>

- <span data-ttu-id="0df74-107">Vous devez être un administrateur général pour gérer l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="0df74-107">You must be a Global admin to manage MFA.</span></span> <span data-ttu-id="0df74-108">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="0df74-108">For more information, see [About admin roles](../add-users/about-admin-roles.md).</span></span>
- <span data-ttu-id="0df74-109">Si l’authentification multifacteur par utilisateur héritée est activée, [Désactivez l'authentification multifacteur par utilisateur héritée](#turn-off-legacy-per-user-mfa).</span><span class="sxs-lookup"><span data-stu-id="0df74-109">If you have legacy per-user MFA turned on, [Turn off legacy per-user MFA](#turn-off-legacy-per-user-mfa).</span></span>
- <span data-ttu-id="0df74-110">Si vous avez des clients Office 2013 sur des appareils Windows, [activer l’authentification moderne pour les clients Office 2013](./enable-modern-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="0df74-110">If you have Office 2013 clients on Windows devices, [turn on Modern Authentication for Office 2013 clients](./enable-modern-authentication.md).</span></span>
- <span data-ttu-id="0df74-111">Avancé : si vous avez des services d’annuaire tiers avec les services de fédération Active Directory (AD FS), configurez le serveur Microsoft Azure Multi-Factor Authentication.</span><span class="sxs-lookup"><span data-stu-id="0df74-111">Advanced: If you have third-party directory services with Active Directory Federation Services (AD FS), set up the Azure MFA Server.</span></span> <span data-ttu-id="0df74-112">Pour plus d’informations, consultez les [scénarios avancés avec l’Authentification multifacteur Azure AD et les solutions VPN tierces](/azure/active-directory/authentication/howto-mfaserver-nps-vpn).</span><span class="sxs-lookup"><span data-stu-id="0df74-112">See [advanced scenarios with Azure AD Multi-Factor Authentication and third-party VPN solutions](/azure/active-directory/authentication/howto-mfaserver-nps-vpn) for more information.</span></span>

## <a name="turn-security-defaults-on-or-off"></a><span data-ttu-id="0df74-113">Activer ou désactiver les paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="0df74-113">Turn Security defaults on or off</span></span>

<span data-ttu-id="0df74-114">Pour la plupart des organisations, les valeurs de sécurité par défaut offrent un niveau de sécurité de connexion supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="0df74-114">For most organizations, Security defaults offer a good level of additional sign-in security.</span></span> <span data-ttu-id="0df74-115">Pour plus d’informations, voir [Présentation des paramètres de sécurité par défaut](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)</span><span class="sxs-lookup"><span data-stu-id="0df74-115">For more information, see [What are security defaults?](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)</span></span>

<span data-ttu-id="0df74-116">Si votre abonnement est nouveau, les paramètres par défaut de sécurité peuvent déjà être activés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="0df74-116">If your subscription is new, Security defaults might already be turned on for you automatically.</span></span>

<span data-ttu-id="0df74-117">Pour activer ou désactiver les paramètres de sécurité par défaut, accédez au volet **Propriétés** pour Azure Active Directory (Azure AD) dans le Portail Azure.</span><span class="sxs-lookup"><span data-stu-id="0df74-117">You enable or disable security defaults from the **Properties** pane for Azure Active Directory (Azure AD) in the Azure portal.</span></span>

1. <span data-ttu-id="0df74-118">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) avec des informations d'identification d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="0df74-118">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with global admin credentials.</span></span>
2. <span data-ttu-id="0df74-119">Dans le volet de navigation gauche, sélectionnez **Afficher tout** puis sous **Centres d’administration**, sélectionnez **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="0df74-119">In the left nav choose **Show All** and under **Admin centers**, choose **Azure Active Directory**.</span></span>
3. <span data-ttu-id="0df74-120">Dans le **centre d’administration Azure Active Directory** sélectionnez **Azure Active Directory** \> **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0df74-120">In the **Azure Active Directory admin center** choose **Azure Active Directory** \> **Properties**.</span></span>
4. <span data-ttu-id="0df74-121">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="0df74-121">At the bottom of the page, choose **Manage Security defaults**.</span></span>
5. <span data-ttu-id="0df74-122">Sélectionnez **Oui** pour activer les paramètres de sécurité par défaut ou **Non** pour désactiver les paramètres de sécurité par défaut, puis choisissez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0df74-122">Choose **Yes** to enable security defaults or **No** to disable security defaults, and then choose **Save**.</span></span>

<span data-ttu-id="0df74-123">Si vous utilisez [stratégies d’accès conditionnel de référence](/azure/active-directory/conditional-access/concept-baseline-protection), vous serez invité à les désactiver avant de passer à l’utilisation des paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="0df74-123">If you have been using [baseline Conditional Access policies](/azure/active-directory/conditional-access/concept-baseline-protection), you will be prompted to turn them off before you move to using security defaults.</span></span>

1. <span data-ttu-id="0df74-124">Accédez à la [page des stratégies d’accès conditionnel](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).</span><span class="sxs-lookup"><span data-stu-id="0df74-124">Go to the [Conditional Access - Policies page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).</span></span>
2. <span data-ttu-id="0df74-125">Sélectionnez chaque stratégie de référence sur **Activé** et définissez **Activer la stratégie** sur **Désactivé**.</span><span class="sxs-lookup"><span data-stu-id="0df74-125">Choose each baseline policy that is **On** and set **Enable policy** to **Off**.</span></span>
3. <span data-ttu-id="0df74-126">Accédez à la [page des propriétés d'Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="0df74-126">Go to the [Azure Active Directory - Properties page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span>
4. <span data-ttu-id="0df74-127">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="0df74-127">At the bottom of the page, choose **Manage Security defaults**.</span></span>
5. <span data-ttu-id="0df74-128">Sélectionnez **Oui** pour activer les paramètres de sécurité par défaut et **Non** pour désactiver les paramètres de sécurité par défaut, puis choisissez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0df74-128">Choose **Yes** to enable security defaults and **No** to disable security defaults, and then choose **Save**.</span></span>

## <a name="use-conditional-access-policies"></a><span data-ttu-id="0df74-129">Utiliser les stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="0df74-129">Use Conditional Access policies</span></span>

<span data-ttu-id="0df74-130">Si votre organisation a des besoins de sécurité de connexion plus granulaires, les stratégies d’accès conditionnel peuvent vous offrir davantage de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0df74-130">If your organization has more granular sign-in security needs, Conditional Access policies can offer you more control.</span></span> <span data-ttu-id="0df74-131">L’accès conditionnel vous permet de créer et de définir des stratégies qui réagissent aux événements de connexion et de demander des actions supplémentaires avant qu’un utilisateur ne soit autorisé à accéder à une application ou un service.</span><span class="sxs-lookup"><span data-stu-id="0df74-131">Conditional Access lets you create and define policies that react to sign in events and request additional actions before a user is granted access to an application or service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0df74-132">Désactivez les paramètres par défaut d'authentification multifacteur et de Sécurité par personne avant d'activer les stratégies d'Accès Conditionnel.</span><span class="sxs-lookup"><span data-stu-id="0df74-132">Turn off both per-user MFA and Security defaults before you enable Conditional Access policies.</span></span>

<span data-ttu-id="0df74-133">L’accès conditionnel est disponible pour les clients qui ont acheté Azure AD Premium P1 ou les licences qui incluent cette offre, telles que Microsoft 365 Business Premium et Microsoft 365 E3.</span><span class="sxs-lookup"><span data-stu-id="0df74-133">Conditional Access is available for customers who have purchased Azure AD Premium P1, or licenses that include this, such as Microsoft 365 Business Premium, and Microsoft 365 E3.</span></span> <span data-ttu-id="0df74-134">Pour en savoir plus, consultez [Créer une stratégie d’accès conditionnel](/azure/active-directory/authentication/tutorial-enable-azure-mfa).</span><span class="sxs-lookup"><span data-stu-id="0df74-134">For more information, see [create a Conditional Access policy](/azure/active-directory/authentication/tutorial-enable-azure-mfa).</span></span>

<span data-ttu-id="0df74-135">L’accès conditionnel basé sur les risques est disponible via une licence Azure AD Premium P2, ou les licences qui l’incluent, telles que Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="0df74-135">Risk-based conditional access is available through Azure AD Premium P2 license, or licenses that include this, such as Microsoft 365 E5.</span></span> <span data-ttu-id="0df74-136">Pour en savoir plus, consultez l'article [Accès conditionnel basé sur les risques](/azure/active-directory/conditional-access/howto-conditional-access-policy-risk).</span><span class="sxs-lookup"><span data-stu-id="0df74-136">For more information, see [risk-based Conditional Access](/azure/active-directory/conditional-access/howto-conditional-access-policy-risk).</span></span>

<span data-ttu-id="0df74-137">Pour plus d’informations sur Azure AD P1 et P2, voir [Tarification Azure Active Directory](https://azure.microsoft.com/pricing/details/active-directory/).</span><span class="sxs-lookup"><span data-stu-id="0df74-137">For more information about the Azure AD P1 and P2, see [Azure Active Directory pricing](https://azure.microsoft.com/pricing/details/active-directory/).</span></span>

### <a name="turn-on-modern-authentication-for-your-organization"></a><span data-ttu-id="0df74-138">Activer Authentification moderne pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="0df74-138">Turn on Modern authentication for your organization</span></span>

<span data-ttu-id="0df74-139">Pour la plupart des abonnements, l’authentification moderne est automatiquement activée, mais si vous avez acheté votre abonnement avant août 2017, il est probable que vous devrez activer l’authentification moderne pour que les fonctionnalités telles que l’authentification multifacteur fonctionnent dans les clients Windows tels qu’Outlook.</span><span class="sxs-lookup"><span data-stu-id="0df74-139">For most subscriptions modern authentication is automatically turned on, but if you purchased your subscription before August 2017, it is likely that you will need to turn on Modern Authentication in order to get features like Multi-Factor Authentication to work in Windows clients like Outlook.</span></span>


1. <span data-ttu-id="0df74-140">Dans le Centre d’administration Microsoft 365, dans le volet de navigation gauche, sélectionnez **Paramètres** \> **Paramètres d’organisation**.</span><span class="sxs-lookup"><span data-stu-id="0df74-140">In the Microsoft 365 admin center, in the left nav choose **Settings** \> **Org settings**.</span></span>
2. <span data-ttu-id="0df74-141">Sous l’onglet **Services**, sélectionnez **Authentification moderne**, puis, dans le volet **Authentification moderne**, assurez-vous que l’option **Activer l’authentification moderne** est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0df74-141">Under the **Services** tab, choose **Modern authentication**, and in the **Modern authentication** pane, make sure **Enable Modern authentication** is selected.</span></span> <span data-ttu-id="0df74-142">Sélectionnez **Save Changes (Enregistrer les modifications)**.</span><span class="sxs-lookup"><span data-stu-id="0df74-142">Choose **Save changes**.</span></span>

### <a name="turn-off-legacy-per-user-mfa"></a><span data-ttu-id="0df74-143">Désactiver l’authentification multifacteur par utilisateur héritée</span><span class="sxs-lookup"><span data-stu-id="0df74-143">Turn off legacy per-user MFA</span></span>

<span data-ttu-id="0df74-144">Si vous avez déjà activé l’authentification multifacteur (MFA) par utilisateur, vous devez désactiver cette fonctionnalité avant d’activer les paramètres de Sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="0df74-144">If you have previously turned on per-user MFA, you must turn it off before enabling Security defaults.</span></span>

1. <span data-ttu-id="0df74-145">Dans le Centre d’administration Microsoft 365, dans le volet de navigation gauche, sélectionnez **Utilisateurs** \> **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="0df74-145">In the Microsoft 365 admin center, in the left nav choose **Users** \> **Active users**.</span></span>
1. <span data-ttu-id="0df74-146">Sur la page **Utilisateurs actifs**, sélectionnez **Authentification multifacteur**.</span><span class="sxs-lookup"><span data-stu-id="0df74-146">On the **Active users** page, choose **Multi-factor authentication**.</span></span>
1. <span data-ttu-id="0df74-147">Sur la page d'authentification multifacteur, sélectionnez chaque utilisateur et définissez son état d'authentification multifacteur sur **Désactivé**.</span><span class="sxs-lookup"><span data-stu-id="0df74-147">On the multi-factor authentication page, select each user and set their Multi-Factor auth status to **Disabled**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0df74-148">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0df74-148">Next steps</span></span>

- [<span data-ttu-id="0df74-149">Comment s’inscrire à leur méthode de vérification supplémentaire</span><span class="sxs-lookup"><span data-stu-id="0df74-149">How to register for their additional verification method</span></span>](https://support.microsoft.com/office/ace1d096-61e5-449b-a875-58eb3d74de14)
- <span data-ttu-id="0df74-150">[Qu’est-ce que l’authentification multifacteur](https://support.microsoft.com/help/4577374/what-is-multifactor-authentication) ?</span><span class="sxs-lookup"><span data-stu-id="0df74-150">[What is: Multifactor Authentication](https://support.microsoft.com/help/4577374/what-is-multifactor-authentication)</span></span>
- [<span data-ttu-id="0df74-151">Comment se connecter après l’inscription</span><span class="sxs-lookup"><span data-stu-id="0df74-151">How to sign-in after registration</span></span>](https://support.microsoft.com/office/2b856342-170a-438e-9a4f-3c092394d3cb)
- [<span data-ttu-id="0df74-152">Comment modifier leur méthode de vérification supplémentaire</span><span class="sxs-lookup"><span data-stu-id="0df74-152">How to change their additional verification method</span></span>](https://support.microsoft.com/office/956ec8d0-7081-4518-a701-f8414cc20831)

## <a name="related-content"></a><span data-ttu-id="0df74-153">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="0df74-153">Related content</span></span>

<span data-ttu-id="0df74-154">[Activer l’authentification multifacteur](../../business-video/turn-on-mfa.md) (vidéo)</span><span class="sxs-lookup"><span data-stu-id="0df74-154">[Turn on multi-factor authentication](../../business-video/turn-on-mfa.md) (video)</span></span>\
<span data-ttu-id="0df74-155">[Activer l’authentification multifacteur sur votre téléphone](../../business-video/set-up-mfa.md) (vidéo)</span><span class="sxs-lookup"><span data-stu-id="0df74-155">[Turn on multi-factor authentication for your phone](../../business-video/set-up-mfa.md) (video)</span></span>