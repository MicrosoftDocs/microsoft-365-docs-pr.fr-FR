---
title: Multi-Factor Authentication pour Microsoft 365
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: conceptual
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
ms.assetid: 043807b2-21db-4d5c-b430-c8a6dee0e6ba
ROBOTS: NOINDEX, NOFOLLOW
description: Découvrez l’authentification multifacteur dans Microsoft 365.
ms.openlocfilehash: cb425f3fd3d97dc0cd8815699bd22cb2540aed46
ms.sourcegitcommit: 09518b7c9146cda7fd42839ee644ad418d48491a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2020
ms.locfileid: "49001512"
---
# <a name="multi-factor-authentication-for-microsoft-365"></a><span data-ttu-id="badd3-103">Multi-Factor Authentication pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="badd3-103">Multi-factor authentication for Microsoft 365</span></span>

<span data-ttu-id="badd3-104">Les mots de passe constituent la méthode la plus courante pour authentifier une connexion à un ordinateur ou un service en ligne, mais ils sont également les plus vulnérables.</span><span class="sxs-lookup"><span data-stu-id="badd3-104">Passwords are the most common method of authenticating a sign-in to a computer or online service, but they are also the most vulnerable.</span></span> <span data-ttu-id="badd3-105">Les utilisateurs peuvent choisir des mots de passe faciles à utiliser et utiliser les mêmes mots de passe pour plusieurs connexions à différents ordinateurs et services.</span><span class="sxs-lookup"><span data-stu-id="badd3-105">People can choose easy passwords and use the same passwords for multiple sign-ins to different computers and services.</span></span>

<span data-ttu-id="badd3-106">Pour fournir un niveau de sécurité supplémentaire pour les connexions, vous devez utiliser l’authentification multifacteur (MFA), qui utilise à la fois un mot de passe, qui doit être fort, et une méthode de vérification supplémentaire basée sur :</span><span class="sxs-lookup"><span data-stu-id="badd3-106">To provide an additional level of security for sign-ins, you must use multi-factor authentication (MFA), which uses both a password, which should be strong, and an additional verification method based on:</span></span>

- <span data-ttu-id="badd3-107">Tout ce dont vous disposez avec vous n’est pas facile à dupliquer, comme un téléphone intelligent.</span><span class="sxs-lookup"><span data-stu-id="badd3-107">Something you have with you that is not easily duplicated, such as a smart phone.</span></span>
- <span data-ttu-id="badd3-108">Il s’agit d’un article que vous disposez de manière unique et biologique, comme vos empreintes digitales, face ou autre attribut biométrique.</span><span class="sxs-lookup"><span data-stu-id="badd3-108">Something you uniquely and biologically have, such as your fingerprints, face, or other biometric attribute.</span></span>

<span data-ttu-id="badd3-109">La méthode de vérification supplémentaire n’est utilisée qu’une fois que le mot de passe de l’utilisateur a été vérifié.</span><span class="sxs-lookup"><span data-stu-id="badd3-109">The additional verification method is not employed until after the user's password has been verified.</span></span> <span data-ttu-id="badd3-110">Avec l’authentification multifacteur, même si un mot de passe utilisateur fort est compromis, l’agresseur ne dispose pas de votre téléphone intelligent ou de votre empreinte digitale pour terminer la connexion.</span><span class="sxs-lookup"><span data-stu-id="badd3-110">With MFA, even if a strong user password is compromised, the attacker does not have your smart phone or your fingerprint to complete the sign-in.</span></span>

## <a name="mfa-support-in-microsoft-365"></a><span data-ttu-id="badd3-111">Prise en charge de l’authentification multifacteur dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="badd3-111">MFA support in Microsoft 365</span></span>

<span data-ttu-id="badd3-112">Par défaut, Microsoft 365 et Office 365 prennent en charge l’authentification multifacteur pour les comptes d’utilisateur à l’aide des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="badd3-112">By default, both Microsoft 365 and Office 365 support MFA for user accounts using:</span></span>

- <span data-ttu-id="badd3-113">Message texte envoyé à un téléphone et qui demande à l’utilisateur de taper un code de vérification.</span><span class="sxs-lookup"><span data-stu-id="badd3-113">A text message sent to a phone that requires the user to type a verification code.</span></span>
- <span data-ttu-id="badd3-114">Un appel téléphonique.</span><span class="sxs-lookup"><span data-stu-id="badd3-114">A phone call.</span></span>
- <span data-ttu-id="badd3-115">Application Smart Phone Microsoft authentificateur.</span><span class="sxs-lookup"><span data-stu-id="badd3-115">The Microsoft Authenticator smart phone app.</span></span>

<span data-ttu-id="badd3-116">Dans les deux cas, la connexion MFA utilise la méthode « ce que vous avez avec vous qui n’est pas facilement dupliqué » pour la vérification supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="badd3-116">In both cases, the MFA sign-in is using the "something you have with you that is not easily duplicated" method for the additional verification.</span></span> <span data-ttu-id="badd3-117">Il existe plusieurs façons d’activer l’authentification multifacteur pour Microsoft 365 et Office 365 :</span><span class="sxs-lookup"><span data-stu-id="badd3-117">There are multiple ways in which you can enable MFA for Microsoft 365 and Office 365:</span></span>

- <span data-ttu-id="badd3-118">Avec les paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="badd3-118">With security defaults</span></span>
- <span data-ttu-id="badd3-119">Avec des stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="badd3-119">With Conditional Access policies</span></span>
- <span data-ttu-id="badd3-120">Pour chaque compte d’utilisateur individuel (non recommandé)</span><span class="sxs-lookup"><span data-stu-id="badd3-120">For each individual user account (not recommended)</span></span>

<span data-ttu-id="badd3-121">Ces méthodes sont basées sur votre plan Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="badd3-121">These ways are based on your Microsoft 365 plan.</span></span>

|<span data-ttu-id="badd3-122">Planification</span><span class="sxs-lookup"><span data-stu-id="badd3-122">Plan</span></span>|<span data-ttu-id="badd3-123">Recommandation</span><span class="sxs-lookup"><span data-stu-id="badd3-123">Recommendation</span></span>|<span data-ttu-id="badd3-124">Type de client</span><span class="sxs-lookup"><span data-stu-id="badd3-124">Type of customer</span></span>|
|---|---|---|
|<span data-ttu-id="badd3-125">Tous les plans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="badd3-125">All Microsoft 365 plans</span></span>|<span data-ttu-id="badd3-126">Utilisez les paramètres de sécurité par défaut, qui nécessitent l’authentification multifacteur pour tous les comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="badd3-126">Use security defaults, which require MFA for all user accounts.</span></span> <p> <span data-ttu-id="badd3-127">Vous pouvez également configurer l’authentification multifacteur par utilisateur sur des comptes d’utilisateurs individuels, mais cela n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="badd3-127">You can also configure per-user MFA on individual user accounts, but this is not recommended.</span></span>|<span data-ttu-id="badd3-128">Petite entreprise</span><span class="sxs-lookup"><span data-stu-id="badd3-128">Small business</span></span>|
|<span data-ttu-id="badd3-129">Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="badd3-129">Microsoft 365 Business Premium</span></span> <p> <span data-ttu-id="badd3-130">Microsoft 365 E3</span><span class="sxs-lookup"><span data-stu-id="badd3-130">Microsoft 365 E3</span></span> <p> <span data-ttu-id="badd3-131">Licences Azure Active Directory (Azure AD) Premium P1</span><span class="sxs-lookup"><span data-stu-id="badd3-131">Azure Active Directory (Azure AD) Premium P1 licenses</span></span>|<span data-ttu-id="badd3-132">Utilisez des stratégies d’accès conditionnel pour exiger l’authentification multifacteur pour les comptes d’utilisateur en fonction de l’appartenance à un groupe, des applications ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="badd3-132">Use Conditional Access policies to require MFA for user accounts based on group membership, apps, or other criteria.</span></span>|<span data-ttu-id="badd3-133">Petites et grandes entreprises</span><span class="sxs-lookup"><span data-stu-id="badd3-133">Small business to enterprise</span></span>|
|<span data-ttu-id="badd3-134">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="badd3-134">Microsoft 365 E5</span></span> <p> <span data-ttu-id="badd3-135">Licences Azure AD Premium P2</span><span class="sxs-lookup"><span data-stu-id="badd3-135">Azure AD Premium P2 licenses</span></span>|<span data-ttu-id="badd3-136">Utilisez Azure AD Identity Protection pour exiger la MFA en fonction des critères de risque de connexion.</span><span class="sxs-lookup"><span data-stu-id="badd3-136">Use Azure AD Identity Protection to require MFA based on sign-in risk criteria.</span></span>|<span data-ttu-id="badd3-137">Entreprise</span><span class="sxs-lookup"><span data-stu-id="badd3-137">Enterprise</span></span>|
||||

### <a name="security-defaults"></a><span data-ttu-id="badd3-138">Paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="badd3-138">Security defaults</span></span>

<span data-ttu-id="badd3-139">Les paramètres de sécurité par défaut sont une nouvelle fonctionnalité pour Microsoft 365 et les abonnements Office 365 payants ou en version d’évaluation créés après le 21 octobre 2019.</span><span class="sxs-lookup"><span data-stu-id="badd3-139">Security defaults is a new feature for Microsoft 365 and Office 365 paid or trial subscriptions created after October 21, 2019.</span></span> <span data-ttu-id="badd3-140">Les paramètres de sécurité par défaut de ces abonnements sont activés :</span><span class="sxs-lookup"><span data-stu-id="badd3-140">These subscriptions have security defaults turned on, which:</span></span>

- <span data-ttu-id="badd3-141">Tous vos utilisateurs doivent utiliser l’authentification multifacteur avec l’application Microsoft Authenticator.</span><span class="sxs-lookup"><span data-stu-id="badd3-141">Requires all of your users to use MFA with the Microsoft Authenticator app.</span></span>
- <span data-ttu-id="badd3-142">Bloque l’authentification héritée.</span><span class="sxs-lookup"><span data-stu-id="badd3-142">Blocks legacy authentication.</span></span>

<span data-ttu-id="badd3-143">Les utilisateurs disposent de 14 jours pour s’inscrire à l’authentification multifacteur de l’application Microsoft Authenticator sur leur smartphone, un délai qui commence dès la première connexion suivant l’activation des paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="badd3-143">Users have 14 days to register for MFA with the Microsoft Authenticator app from their smart phones, which begins from the first time they sign in after security defaults has been enabled.</span></span> <span data-ttu-id="badd3-144">Lorsque les 14 jours sont écoulés, l’utilisateur ne peut pas se connecter tant que son inscription à l’authentification multifacteur n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="badd3-144">After 14 days have passed, the user won't be able to sign in until MFA registration is completed.</span></span>

<span data-ttu-id="badd3-145">Les paramètres de sécurité par défaut garantissent que toutes les organisations ont un niveau de sécurité de base qui est activé par défaut pour la connexion des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="badd3-145">Security defaults ensure that all organizations have a basic level of security for user sign-in that is enabled by default.</span></span> <span data-ttu-id="badd3-146">Vous pouvez désactiver les paramètres de sécurité par défaut au profit de la fonction MFA avec des stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="badd3-146">You can disable security defaults in favor of MFA with Conditional Access policies.</span></span>

<span data-ttu-id="badd3-147">Vous activez ou désactivez les paramètres de sécurité par défaut dans le volet des **Propriétés** pour Azure ad dans le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="badd3-147">You enable or disable security defaults from the **Properties** pane for Azure AD in the Azure portal.</span></span>

![Image de la page de propriétés du répertoire.](../../media/multi-factor-authentication-microsoft-365/security-defaults-mfa.png)

<span data-ttu-id="badd3-149">Vous pouvez utiliser les paramètres de sécurité par défaut avec n’importe quel plan Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="badd3-149">You can use security defaults with any Microsoft 365 plan.</span></span>

<span data-ttu-id="badd3-150">Pour plus d’informations, voir[Vue d’ensemble des paramètres de sécurité par défaut](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults).</span><span class="sxs-lookup"><span data-stu-id="badd3-150">For more information, see this [overview of security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults).</span></span>

### <a name="conditional-access-policies"></a><span data-ttu-id="badd3-151">Stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="badd3-151">Conditional Access policies</span></span>

<span data-ttu-id="badd3-152">Les stratégies d’accès conditionnel sont un groupe de règles qui spécifient les conditions dans lesquelles les connexions sont évaluées et autorisées.</span><span class="sxs-lookup"><span data-stu-id="badd3-152">Conditional Access policies are a set of rules that specify the conditions under which sign-ins are evaluated and allowed.</span></span> <span data-ttu-id="badd3-153">Par exemple, vous pouvez créer une stratégie d’accès conditionnel qui indique :</span><span class="sxs-lookup"><span data-stu-id="badd3-153">For example, you can create a Conditional Access policy that states:</span></span>

- <span data-ttu-id="badd3-154">Si le nom du compte d’utilisateur concerne membre d’un groupe d’utilisateurs bénéficiant des rôles d’administrateur Exchange, utilisateur, mot de passe, sécurité, SharePoint ou global, exigez l’authentification multifacteur avant d’autoriser l’accès.</span><span class="sxs-lookup"><span data-stu-id="badd3-154">If the user account name is a member of a group for users that are assigned the Exchange, user, password, security, SharePoint, or global administrator roles, require MFA before allowing access.</span></span>

<span data-ttu-id="badd3-155">Cette stratégie vous permet de demander une authentification multifacteur basée sur l’appartenance au groupe, plutôt que d’essayer de configurer des comptes d’utilisateur individuels pour l’authentification multifacteur lorsqu’ils sont attribués ou non à des rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="badd3-155">This policy allows you to require MFA based on group membership, rather than trying to configure individual user accounts for MFA when they are assigned or unassigned from these administrator roles.</span></span>

<span data-ttu-id="badd3-156">Vous pouvez également utiliser des stratégies d’accès conditionnel pour des fonctionnalités plus avancées, telles que l’authentification MFA pour des applications spécifiques ou l’utilisation de la connexion à partir d’un appareil compatible, tel que votre ordinateur portable exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="badd3-156">You can also use Conditional Access policies for more advanced capabilities, such as requiring MFA for specific apps or that the sign-in is done from a compliant device, such as your laptop running Windows 10.</span></span>

<span data-ttu-id="badd3-157">Vous configurez les stratégies d’accès conditionnel à partir du volet de **sécurité** pour Azure ad dans le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="badd3-157">You configure Conditional Access policies from the **Security** pane for Azure AD in the Azure portal.</span></span>

![Image de l’option de menu pour un accès conditionnel](../../media/multi-factor-authentication-microsoft-365/conditional-access-mfa.png)

<span data-ttu-id="badd3-159">Vous pouvez utiliser des stratégies d’accès conditionnel avec :</span><span class="sxs-lookup"><span data-stu-id="badd3-159">You can use Conditional Access policies with:</span></span>

- <span data-ttu-id="badd3-160">Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="badd3-160">Microsoft 365 Business Premium</span></span>
- <span data-ttu-id="badd3-161">Microsoft 365 E3 et E5</span><span class="sxs-lookup"><span data-stu-id="badd3-161">Microsoft 365 E3 and E5</span></span>
- <span data-ttu-id="badd3-162">Licences Azure AD Premium P1 et Azure AD Premium P2</span><span class="sxs-lookup"><span data-stu-id="badd3-162">Azure AD Premium P1 and Azure AD Premium P2 licenses</span></span>

<span data-ttu-id="badd3-163">Pour les petites entreprises avec Microsoft 365 Business Premium, vous pouvez facilement utiliser des stratégies d’accès conditionnel en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="badd3-163">For small businesses with Microsoft 365 Business Premium, you can easily use Conditional Access policies with the following steps:</span></span>

1. <span data-ttu-id="badd3-164">Créez un groupe pour contenir les comptes d’utilisateurs qui requièrent l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="badd3-164">Create a group to contain the user accounts that require MFA.</span></span>
2. <span data-ttu-id="badd3-165">Activer la stratégie **exiger l’authentification multifacteur pour les administrateurs globaux** .</span><span class="sxs-lookup"><span data-stu-id="badd3-165">Enable the **Require MFA for global admins** policy.</span></span>
3. <span data-ttu-id="badd3-166">Créez une stratégie d’accès conditionnel basée sur un groupe avec ces paramètres :</span><span class="sxs-lookup"><span data-stu-id="badd3-166">Create a group-based Conditional Access policy with these settings:</span></span>
    - <span data-ttu-id="badd3-167">Affectations > des utilisateurs et des groupes : nom de votre groupe de l’étape 1 ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="badd3-167">Assignments > Users and groups: The name of your group from Step 1 above.</span></span>
    - <span data-ttu-id="badd3-168">Affectations > les applications ou les actions Cloud : toutes les applications Cloud.</span><span class="sxs-lookup"><span data-stu-id="badd3-168">Assignments > Cloud apps or actions: All cloud apps.</span></span>
    - <span data-ttu-id="badd3-169">Les contrôles d’accès > accorder > accorder l’accès > nécessitent une authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="badd3-169">Access controls > Grant > Grant access > Require multi-factor authentication.</span></span>
4. <span data-ttu-id="badd3-170">Activez la stratégie.</span><span class="sxs-lookup"><span data-stu-id="badd3-170">Enable the policy.</span></span>
5. <span data-ttu-id="badd3-171">Ajoutez un compte d’utilisateur au groupe créé à l’étape 1 ci-dessus et testez.</span><span class="sxs-lookup"><span data-stu-id="badd3-171">Add a user account to the group created in Step 1 above and test.</span></span>
6. <span data-ttu-id="badd3-172">Pour exiger l’authentification multifacteur pour les comptes d’utilisateur supplémentaires, ajoutez-les au groupe créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="badd3-172">To require MFA for additional user accounts, add them to the group created in Step 1.</span></span>

<span data-ttu-id="badd3-173">Cette stratégie d’accès conditionnel vous permet de déployer la configuration MFA requise pour vos utilisateurs à votre rythme.</span><span class="sxs-lookup"><span data-stu-id="badd3-173">This Conditional Access policy allows you to roll out the MFA requirement to your users at your own pace.</span></span>

<span data-ttu-id="badd3-174">Les entreprises doivent utiliser des [stratégies d’accès conditionnel courantes](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-policy-common) pour configurer les stratégies suivantes :</span><span class="sxs-lookup"><span data-stu-id="badd3-174">Enterprises should use [Common Conditional Access policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-policy-common) to configure the following policies:</span></span>

- [<span data-ttu-id="badd3-175">Exiger l’authentification multifacteur pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="badd3-175">Require MFA for administrators</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-admin-mfa)
- [<span data-ttu-id="badd3-176">Exiger l’authentification multifacteur pour tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="badd3-176">Require MFA for all users</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-all-users-mfa)
- [<span data-ttu-id="badd3-177">Bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="badd3-177">Block legacy authentication</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-block-legacy)

<span data-ttu-id="badd3-178">Si vous souhaitez en savoir plus, consultez [Présentation de l’accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/overview).</span><span class="sxs-lookup"><span data-stu-id="badd3-178">For more information, see this [overview of Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/overview).</span></span>

### <a name="azure-ad-identity-protection"></a><span data-ttu-id="badd3-179">Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="badd3-179">Azure AD Identity Protection</span></span>

<span data-ttu-id="badd3-180">Avec Azure AD Identity Protection, vous pouvez créer une stratégie d’accès conditionnel supplémentaire pour [exiger l’authentification multifacteur lorsque le risque de connexion est moyen ou élevé](https://docs.microsoft.com/microsoft-365/enterprise/identity-access-policies#require-mfa-based-on-sign-in-risk).</span><span class="sxs-lookup"><span data-stu-id="badd3-180">With Azure AD Identity Protection, you can create an additional Conditional Access policy to [require MFA when sign-in risk is medium or high](https://docs.microsoft.com/microsoft-365/enterprise/identity-access-policies#require-mfa-based-on-sign-in-risk).</span></span>

<span data-ttu-id="badd3-181">Vous pouvez utiliser Azure AD identity protection et les stratégies d’accès conditionnel basées sur les risques avec :</span><span class="sxs-lookup"><span data-stu-id="badd3-181">You can use Azure AD Identity Protection and risk-based Conditional Access policies with:</span></span>

- <span data-ttu-id="badd3-182">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="badd3-182">Microsoft 365 E5</span></span>
- <span data-ttu-id="badd3-183">Licences Azure AD Premium P2</span><span class="sxs-lookup"><span data-stu-id="badd3-183">Azure AD Premium P2 licenses</span></span>

<span data-ttu-id="badd3-184">Si vous souhaitez en savoir plus, consultez la page [Présentation de Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/identity-protection/overview-identity-protection).</span><span class="sxs-lookup"><span data-stu-id="badd3-184">For more information, see this [overview of Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/identity-protection/overview-identity-protection).</span></span>

### <a name="legacy-per-user-mfa-not-recommended"></a><span data-ttu-id="badd3-185">Héritage par utilisateur (non recommandé)</span><span class="sxs-lookup"><span data-stu-id="badd3-185">Legacy per-user MFA (not recommended)</span></span>

<span data-ttu-id="badd3-186">Vous devez utiliser des paramètres de sécurité par défaut ou des stratégies d’accès conditionnel pour exiger l’authentification multifacteur pour les connexions de vos comptes d’utilisateur. Toutefois, si l’une de ces méthodes n’est pas utilisable, Microsoft recommande vivement la fonction MFA pour les comptes d’utilisateur qui ont des rôles d’administrateur, en particulier le rôle d’administrateur général, pour n’importe quel abonnement de taille.</span><span class="sxs-lookup"><span data-stu-id="badd3-186">You should be using either security defaults or Conditional Access policies to require MFA for your user account sign-ins. However, if either of these cannot be used, Microsoft strongly recommends MFA for user accounts that have administrator roles, especially the global administrator role, for any size subscription.</span></span>

<span data-ttu-id="badd3-187">Vous activez l’authentification multifacteur pour des comptes d’utilisateur individuels à partir du volet **utilisateur actif** du centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="badd3-187">You enable MFA for individual user accounts from the **Active user** pane of the Microsoft 365 admin center.</span></span>

![Image de l’option d’authentification multifacteur sur la page utilisateurs actifs](../../media/multi-factor-authentication-microsoft-365/per-user-mfa.png)

<span data-ttu-id="badd3-189">Après avoir été activé, la prochaine fois que l’utilisateur se connecte, il est invité à s’inscrire pour l’authentification multifacteur (MFA) et à choisir et tester la méthode de vérification supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="badd3-189">After being enabled, the next time the user signs in, they will be prompted to register for MFA and to choose and test the additional verification method.</span></span>

### <a name="using-these-methods-together"></a><span data-ttu-id="badd3-190">Utilisation combinée des méthodes</span><span class="sxs-lookup"><span data-stu-id="badd3-190">Using these methods together</span></span>

<span data-ttu-id="badd3-191">Ce tableau présente les résultats de l’activation de l’authentification multifacteur avec les paramètres de sécurité par défaut, les stratégies d’accès conditionnel et les paramètres de compte par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="badd3-191">This table shows the results of enabling MFA with security defaults, Conditional Access policies, and per-user account settings.</span></span>

||<span data-ttu-id="badd3-192">Activé</span><span class="sxs-lookup"><span data-stu-id="badd3-192">Enabled</span></span>|<span data-ttu-id="badd3-193">Désactivé</span><span class="sxs-lookup"><span data-stu-id="badd3-193">Disabled</span></span>|<span data-ttu-id="badd3-194">Méthode d'authentification secondaire</span><span class="sxs-lookup"><span data-stu-id="badd3-194">Secondary authentication method</span></span>|
|---|---|---|---|
|<span data-ttu-id="badd3-195">**Paramètres de sécurité par défaut**</span><span class="sxs-lookup"><span data-stu-id="badd3-195">**Security defaults**</span></span>|<span data-ttu-id="badd3-196">Impossible d’utiliser des stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="badd3-196">Can't use Conditional Access policies</span></span>|<span data-ttu-id="badd3-197">Peut utiliser les stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="badd3-197">Can use Conditional Access policies</span></span>|<span data-ttu-id="badd3-198">Application Microsoft Authenticator</span><span class="sxs-lookup"><span data-stu-id="badd3-198">Microsoft Authenticator app</span></span>|
|<span data-ttu-id="badd3-199">**Stratégies d’accès conditionnel**</span><span class="sxs-lookup"><span data-stu-id="badd3-199">**Conditional Access policies**</span></span>|<span data-ttu-id="badd3-200">Si elles sont activées, vous ne pouvez pas activer les paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="badd3-200">If any are enabled, you can't enable security defaults</span></span>|<span data-ttu-id="badd3-201">Si tous ces éléments sont désactivés, vous pouvez activer les paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="badd3-201">If all are disabled, you can enable security defaults</span></span>|<span data-ttu-id="badd3-202">Utilisateur spécifié lors de l’inscription à l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="badd3-202">User-specified during MFA registration</span></span>|
|<span data-ttu-id="badd3-203">**Héritage par utilisateur (non recommandé)**</span><span class="sxs-lookup"><span data-stu-id="badd3-203">**Legacy per-user MFA (not recommended)**</span></span>|<span data-ttu-id="badd3-204">Remplace les paramètres de sécurité par défaut et les stratégies d’accès conditionnel exigeant une authentification multifacteur à chaque connexion</span><span class="sxs-lookup"><span data-stu-id="badd3-204">Overrides security defaults and Conditional Access policies requiring MFA at each sign in</span></span>|<span data-ttu-id="badd3-205">Remplacé par les paramètres de sécurité et les stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="badd3-205">Overridden by security defaults and Conditional Access policies</span></span>|<span data-ttu-id="badd3-206">Utilisateur spécifié lors de l’inscription à l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="badd3-206">User-specified during MFA registration</span></span>|
||||

<span data-ttu-id="badd3-207">Si les paramètres de sécurité par défaut sont activés, tous les nouveaux utilisateurs sont invités à indiquer l’enregistrement MFA et l’utilisation de l’application Microsoft Authenticator lors de la prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="badd3-207">If security defaults are enabled, all new users are prompted for MFA registration and the use of the Microsoft Authenticator app at their next sign-in.</span></span>

## <a name="ways-to-manage-mfa-settings"></a><span data-ttu-id="badd3-208">Méthodes de gestion des paramètres MFA</span><span class="sxs-lookup"><span data-stu-id="badd3-208">Ways to manage MFA settings</span></span>

<span data-ttu-id="badd3-209">Il existe deux façons de gérer les paramètres MFA.</span><span class="sxs-lookup"><span data-stu-id="badd3-209">There are two ways to manage MFA settings.</span></span>

<span data-ttu-id="badd3-210">Dans le portail Azure, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="badd3-210">In the Azure portal, you can:</span></span>

- <span data-ttu-id="badd3-211">Activer et désactiver les paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="badd3-211">Enable and disable security defaults</span></span>
- <span data-ttu-id="badd3-212">Configurer des stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="badd3-212">Configure Conditional Access policies</span></span>

<span data-ttu-id="badd3-213">Dans le centre d’administration 365 de Microsoft, vous pouvez configurer les paramètres par utilisateur et par authentification multifacteur de service.</span><span class="sxs-lookup"><span data-stu-id="badd3-213">In the Microsoft 365 admin center, you can configure per-user and service MFA settings.</span></span>

## <a name="your-next-step"></a><span data-ttu-id="badd3-214">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="badd3-214">Your next step</span></span>

[<span data-ttu-id="badd3-215">Configurer MFA pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="badd3-215">Set up MFA for Microsoft 365</span></span>](set-up-multi-factor-authentication.md)
