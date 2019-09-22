---
title: 'Phase 2 : Critères de sortie de l’infrastructure d’identités'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/20/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Assurez-vous que votre configuration répond aux critères de Microsoft 365 Entreprise pour l’infrastructure et les services d’identités.
ms.openlocfilehash: 880bfa2b71158a2fa5c64fb09af2e8a34428a7a8
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37071683"
---
# <a name="phase-2-identity-infrastructure-exit-criteria"></a><span data-ttu-id="0d91c-103">Phase 2 : Critères de sortie de l’infrastructure d’identités</span><span class="sxs-lookup"><span data-stu-id="0d91c-103">Phase 2: Identity infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="0d91c-104">Vérifiez que votre infrastructure d’identité répond aux critères suivants requis et que vous avez décidé ceux qui sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="0d91c-104">Make sure your identity infrastructure meets the following required criteria and that you've considered those that are optional.</span></span>

<span data-ttu-id="0d91c-105">Voir également les [Conditions préalables](https://docs.microsoft.com/microsoft-365-enterprise/identity-access-policies#prerequisites) pour consulter d’autre suggestions sur l’infrastructure d’identité.</span><span class="sxs-lookup"><span data-stu-id="0d91c-105">Also see [Prerequisites](https://docs.microsoft.com/microsoft-365-enterprise/identity-access-policies#prerequisites) for additional recommendations on identity infrastructure.</span></span>

<a name="crit-identity-global-admin"></a>
## <a name="required-your-global-administrator-accounts-are-protected"></a><span data-ttu-id="0d91c-106">Obligatoire : vos comptes d’administrateur général sont protégés</span><span class="sxs-lookup"><span data-stu-id="0d91c-106">Required: Your global administrator accounts are protected</span></span> 

<span data-ttu-id="0d91c-107">Vous avez [protégé vos comptes d’administrateur général Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts) pour éviter que des attaques ne compromettent l'intégrité des informations d'identification, ce qui peut entraîner des violations de votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0d91c-107">You've [protected your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts) to thwart  credential compromise by attackers that can lead to breaches of your Microsoft 365 subscription.</span></span>

<span data-ttu-id="0d91c-108">Si vous ignorez cette exigence, vos comptes d’administrateur général peuvent être attaqués et compromis, autorisant un utilisateur à accéder à vos données à l’échelle du système à des fins de collecte, destruction ou prise en otage des données.</span><span class="sxs-lookup"><span data-stu-id="0d91c-108">If you skip this requirement, your global administrator accounts can be susceptible to attack and compromise, allowing an attacker to gain system-wide access to your data for harvesting, destruction, or ransom.</span></span>

<span data-ttu-id="0d91c-109">Si nécessaire, l’[Étape 1](identity-create-protect-global-admins.md#identity-global-admin) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="0d91c-109">If needed, [Step 1](identity-create-protect-global-admins.md#identity-global-admin) can help you meet this requirement.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="0d91c-110">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="0d91c-110">How to test</span></span>

<span data-ttu-id="0d91c-111">Suivez ces étapes pour vérifier que vous avez protégé vos comptes d’administrateur général :</span><span class="sxs-lookup"><span data-stu-id="0d91c-111">Use these steps to verify that you've protected your global administrator accounts:</span></span>

1. <span data-ttu-id="0d91c-112">Exécutez la commande suivante Azure Active Directory PowerShell pour Graph à l'invite de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d91c-112">Run the following Azure Active Directory PowerShell for Graph command at the PowerShell command prompt.</span></span> <span data-ttu-id="0d91c-113">Vous ne devez voir que la liste des comptes d’administrateur général dédiés.</span><span class="sxs-lookup"><span data-stu-id="0d91c-113">Run the following Azure AD V2 command at the PowerShell command prompt. You should see only the list of dedicated global administrator accounts.</span></span>
   ```
   Get-AzureADDirectoryRole | where { $_.DisplayName -eq "Company Administrator" } | Get-AzureADDirectoryRoleMember | Ft DisplayName
   ```
2. <span data-ttu-id="0d91c-114">Connectez-vous à Office 365 à l’aide de chacun des comptes de l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="0d91c-114">Sign in to Office 365 using each of the accounts from step 1. Each sign in must require multi-factor authentication and the strongest form of secondary authentication available in your organization.</span></span> <span data-ttu-id="0d91c-115">Chaque connexion doit exiger l’authentification multifacteur Azure et la forme la plus forte d’authentification secondaire disponible dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0d91c-115">Each sign in must require Azure Multi-Factor Authentication and the strongest form of secondary authentication available in your organization.</span></span>

> [!Note]
> <span data-ttu-id="0d91c-116">Reportez-vous à [Se connecter à Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) pour obtenir des instructions sur l’installation du module Azure AD PowerShell pour Graph et la connexion à Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d91c-116">See [Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) for instructions on installing the Azure Active Directory PowerShell for Graph module and signing in to Office 365.</span></span>

<a name="crit-identity-pim"></a>
## <a name="optional-you-have-set-up-privileged-identity-management-to-support-on-demand-assignment-of-the-global-administrator-role"></a><span data-ttu-id="0d91c-117">Facultatif : vous avez configuré Privileged Identity Management pour prendre en charge l’affectation à la demande du rôle Administrateur général</span><span class="sxs-lookup"><span data-stu-id="0d91c-117">Optional: You have set up Privileged Identity Management to support on-demand assignment of the global administrator role</span></span>

<span data-ttu-id="0d91c-118">Vous avez déjà suivi les instructions de la rubrique [Configuration d’Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure) pour activer PIM dans votre client Azure AD et configuré vos comptes d’administrateur général comme administrateurs éligibles.</span><span class="sxs-lookup"><span data-stu-id="0d91c-118">You've used the instructions in [Configure Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure) to enable PIM in your Azure AD tenant and configured your global administrator accounts as eligible admins.</span></span>

<span data-ttu-id="0d91c-119">Vous avez également suivi les recommandations de la rubrique relative à la [sécurisation de l’accès privilégié pour les déploiements hybrides et cloud dans Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) pour développer une feuille de route qui sécurise l’accès privilégié contre les cyber-attaquants.</span><span class="sxs-lookup"><span data-stu-id="0d91c-119">You've also used the recommendations in [Securing privileged access for hybrid and cloud deployments in Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) to develop a roadmap that secures privileged access against cyber attackers.</span></span>

<span data-ttu-id="0d91c-120">Si vous ignorez cette option, vos comptes Administrateur général sont soumis à des attaques en ligne en continu et, en cas de compromission, peuvent autoriser un utilisateur à recueillir, détruire ou conserver vos informations sensibles contre rançon.</span><span class="sxs-lookup"><span data-stu-id="0d91c-120">If you skip this option, your global administrator accounts are subject to ongoing online attack and, if compromised, can allow an attacker to harvest, destroy, or hold your sensitive information for ransom.</span></span>

<span data-ttu-id="0d91c-121">Si nécessaire, l’[Étape 1](identity-create-protect-global-admins.md#identity-pim) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-121">If needed, [Step 1](identity-create-protect-global-admins.md#identity-pim) can help you with this option.</span></span>

<a name="crit-identity-pam"></a>
## <a name="optional-you-have-configure-privileged-access-management-in-office-365"></a><span data-ttu-id="0d91c-122">Facultatif : vous avez configuré la gestion des accès privilégiés dans Office 365</span><span class="sxs-lookup"><span data-stu-id="0d91c-122">Optional: You have configure privileged access management in Office 365</span></span>

<span data-ttu-id="0d91c-123">Vous avez utilisé les informations de la rubrique [Configurer la gestion des accès privilégiés dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) pour activer l’accès privilégié et créer une ou plusieurs stratégies d’accès privilégié au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0d91c-123">You've used the information in the [Configure privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) topic to enable privileged access and create one or more privileged access policies in your organization.</span></span> <span data-ttu-id="0d91c-124">Vous avez configuré ces stratégies et l’accès juste-à-temps est activé pour l’accès aux données sensibles ou aux paramètres de configuration critiques.</span><span class="sxs-lookup"><span data-stu-id="0d91c-124">You've configured these policies and just-in-time access is enabled for access to sensitive data or access to critical configuration settings.</span></span>

<span data-ttu-id="0d91c-125">Si nécessaire, l’[Étape 1](identity-create-protect-global-admins.md#identity-pam) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="0d91c-125">If needed, [Step 1](identity-create-protect-global-admins.md#identity-pam) can help you meet this requirement.</span></span> 

<a name="crit-password-prot"></a>
## <a name="optional-azure-ad-password-protection-is-banning-the-use-of-weak-passwords"></a><span data-ttu-id="0d91c-126">Facultatif : la protection de mot de passe Azure AD interdit l'utilisation de mots de passe faibles</span><span class="sxs-lookup"><span data-stu-id="0d91c-126">Optional: Azure AD password protection is banning the use of weak passwords</span></span>

<span data-ttu-id="0d91c-127">Vous avez activé l'interdiction des mauvais mots de passe [dans le cloud](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad) et pour vos [services de domaine Active Directory (AD DS) locaux](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad-on-premises) pour les mots de passe généraux interdits et, éventuellement, pour les termes personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0d91c-127">You have enabled the banning of bad passwords [in the cloud](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad) and for your [on-premises Active Directory Domain Services (AD DS)](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad-on-premises) for global banned passwords and, optionally, for custom terms.</span></span>

<span data-ttu-id="0d91c-128">Si nécessaire, l’[Étape 2](identity-secure-your-passwords.md#identity-password-prot) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-128">If needed, [Step 2](identity-secure-your-passwords.md#identity-password-prot) can help you with this option.</span></span>

<a name="crit-identity-pw-reset"></a>
## <a name="optional-users-can-reset-their-own-passwords"></a><span data-ttu-id="0d91c-129">Facultatif : les utilisateurs peuvent réinitialiser leurs mots de passe</span><span class="sxs-lookup"><span data-stu-id="0d91c-129">Optional: Users can reset their own passwords</span></span>

<span data-ttu-id="0d91c-130">Vous avez utilisé la rubrique relative au [déploiement rapide de la réinitialisation du mot de passe libre-service Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) pour configurer la réinitialisation du mot de passe pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0d91c-130">You've used [Azure AD self-service password reset rapid deployment](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) to configure password reset for your users.</span></span>

<span data-ttu-id="0d91c-131">Si vous ne remplissez pas cette condition, les utilisateurs dépendront des administrateurs de compte d’utilisateur pour réinitialiser leurs mots de passe, entraînant une surcharge d’administration informatique supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="0d91c-131">If you don’t meet this condition, users will be dependent on user account administrators to reset their passwords, resulting in additional IT administration overhead.</span></span>

<span data-ttu-id="0d91c-132">Si nécessaire, l’[Étape 2](identity-secure-your-passwords.md#identity-pw-reset) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-132">If needed, [Step 2](identity-secure-your-passwords.md#identity-pw-reset) can help you with this option.</span></span>

<a name="crit-identity-sso"></a>
## <a name="optional-users-can-sign-in-using-azure-ad-seamless-single-sign-on"></a><span data-ttu-id="0d91c-133">Facultatif : les utilisateurs peuvent se connecter à l’aide de l’authentification unique Azure AD Single Sign-on</span><span class="sxs-lookup"><span data-stu-id="0d91c-133">Optional: Users can sign in using Azure AD Seamless Single Sign-on</span></span>

<span data-ttu-id="0d91c-134">Vous avez activé l’[authentification unique transparente Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start) pour que votre organisation simplifie la manière dont les utilisateurs se connectent aux applications basées sur le cloud, comme Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d91c-134">You enabled [Azure AD Connect: Seamless Single Sign-On](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start) for your organization to simplify how users sign in to cloud-based applications, such as Office 365.</span></span>

<span data-ttu-id="0d91c-135">Si vous ignorez cette option, vos utilisateurs peuvent être invités à fournir des informations d’identification lorsqu’ils accèdent à d’autres applications qui utilisent votre client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0d91c-135">If you skip this option, your users might be prompted to provide credentials when they access additional applications that use Azure AD.</span></span>

<span data-ttu-id="0d91c-136">Si nécessaire, l’[Étape 2](identity-secure-your-passwords.md#identity-sso) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-136">If needed, [Step 2](identity-secure-your-passwords.md#identity-sso) can help you with this option.</span></span>

<a name="crit-identity-custom-sign-in"></a>
## <a name="optional-the-office-365-sign-in-screen-is-personalized-for-your-organization"></a><span data-ttu-id="0d91c-137">Facultatif : l’écran de connexion Office 365 est personnalisé pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="0d91c-137">Optional: The Office 365 sign-in screen is personalized for your organization</span></span>

<span data-ttu-id="0d91c-138">Vous avez utilisé [Ajouter la marque de votre organisation à votre page de connexion et aux pages du Panneau d’accès](http://aka.ms/aadpaddbranding) pour ajouter la marque de votre organisation à la page de connexion Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d91c-138">You have used [Add company branding to your sign-in and Access Panel pages](http://aka.ms/aadpaddbranding) to add your organization’s branding to the Office 365 sign-in page.</span></span>

<span data-ttu-id="0d91c-139">Si vous ignorez cette option, vos utilisateurs verront un écran de connexion Office 365 générique et peuvent ne pas être certains de se connecter au site de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0d91c-139">If you skip this option, your users will see a generic Office 365 sign-in screen and might not be confident that they’re signing into your organization’s site.</span></span>

<span data-ttu-id="0d91c-140">Si nécessaire, l’[Étape 2](identity-secure-your-passwords.md#identity-custom-sign-in) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-140">If needed, [Step 2](identity-secure-your-passwords.md#identity-custom-sign-in) can help you with this option.</span></span>


<a name="crit-identity-mfa"></a>
## <a name="optional-azure-multi-factor-authentication-is-enabled-for-your-users"></a><span data-ttu-id="0d91c-141">Facultatif : l’authentification multifacteur Azure est activée pour vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="0d91c-141">Optional: Azure Multi-Factor Authentication is enabled for your users</span></span>

<span data-ttu-id="0d91c-142">Vous avez utilisé [Offre pour l’authentification multifacteur Azure](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted) et les [stratégies d’accès conditionnel](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted#enable-multi-factor-authentication-with-conditional-access) pour activer l’authentification multifacteur Azure (MFA) pour vos comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0d91c-142">You used [Plan for Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted) and [Conditional Access policies](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted#enable-multi-factor-authentication-with-conditional-access) to enable Azure Multi-Factor Authentication (MFA) for your user accounts.</span></span>

<span data-ttu-id="0d91c-p104">Si vous ignorez cette option, vos comptes d’utilisateur sont vulnérables à la compromission des informations d’identification par des cyber-attaquants. Si le mot de passe d’un compte d’utilisateur est compromis, toutes les ressources et les fonctionnalités du compte, telles que les rôles d’administrateur, sont disponibles pour l’utilisateur malveillant. Ainsi, ce dernier peut copier, détruire ou conserver des documents internes et d’autres données contre rançon.</span><span class="sxs-lookup"><span data-stu-id="0d91c-p104">If you skip this option, your user accounts are vulnerable to credential compromise by cyber attackers. If a user account’s password is compromised, all the resources and capabilities of the account, such as administrator roles, are available to the attacker. This allows the attacker to copy, destroy, or hold for ransom internal documents and other data.</span></span>

<span data-ttu-id="0d91c-146">Si nécessaire, l’[Étape 3](identity-secure-user-sign-ins.md#identity-mfa) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-146">If needed, [Step 3](identity-secure-user-sign-ins.md#identity-mfa) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="0d91c-147">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="0d91c-147">How to test</span></span>

1.  <span data-ttu-id="0d91c-148">Créez un compte d’utilisateur test et attribuez-lui une licence.</span><span class="sxs-lookup"><span data-stu-id="0d91c-148">Create a test user account in the Office 365 Admin portal and assign them a license.</span></span> 
2.  <span data-ttu-id="0d91c-149">Configurez l’authentification multifacteur Azure pour le compte d’utilisateur test avec la méthode de vérification supplémentaire que vous utilisez pour les comptes d’utilisateur réels, comme l’envoi d’un SMS sur votre téléphone.</span><span class="sxs-lookup"><span data-stu-id="0d91c-149">Configure multi-factor authentication for the test user account with the additional verification method that you are using for actual user accounts, such as sending a message to your phone.</span></span> 
3.  <span data-ttu-id="0d91c-150">Connectez-vous au portail Office 36 avec le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-150">Sign in to the Office 365 or Azure portal with the test user account.</span></span>
4.  <span data-ttu-id="0d91c-151">Vérifiez que l’authentification multifacteur vous invite à saisir les informations de vérification supplémentaires et que l’authentification s’effectue sans problèmes.</span><span class="sxs-lookup"><span data-stu-id="0d91c-151">Verify that MFA prompts you for the additional verification information and results in a successful authentication.</span></span> 
5.  <span data-ttu-id="0d91c-152">Supprimez le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-152">Delete the test user account.</span></span>

<a name="crit-identity-ident-prot"></a>
## <a name="optional-azure-ad-identity-protection-is-enabled-to-protect-against-credential-compromise-microsoft-365-enterprise-e5-only"></a><span data-ttu-id="0d91c-153">Facultatif : Azure AD Identity Protection est activé pour vous protéger contre la compromission d’informations d’identification (Microsoft 365 Entreprise E5 uniquement)</span><span class="sxs-lookup"><span data-stu-id="0d91c-153">Optional: Azure AD Identity Protection is enabled to protect against credential compromise</span></span>

<span data-ttu-id="0d91c-154">Vous avez activé Azure AD Identity Protection pour :</span><span class="sxs-lookup"><span data-stu-id="0d91c-154">You've enabled Azure AD Identity Protection to:</span></span>

- <span data-ttu-id="0d91c-155">résoudre les vulnérabilités d’identités potentielles ;</span><span class="sxs-lookup"><span data-stu-id="0d91c-155">Address potential identity vulnerabilities.</span></span>
- <span data-ttu-id="0d91c-156">détecter les tentatives de compromission d’informations d’identification possibles ;</span><span class="sxs-lookup"><span data-stu-id="0d91c-156">Detect possible credential compromise attempts.</span></span>
- <span data-ttu-id="0d91c-157">examiner et résoudre des incidents d’identités suspects en cours.</span><span class="sxs-lookup"><span data-stu-id="0d91c-157">Investigate and address ongoing suspicious identity incidents.</span></span>

<span data-ttu-id="0d91c-p105">Si vous ignorez cette option, vous ne pourrez pas détecter ou empêcher automatiquement les tentatives de compromission d’informations d’identification ni examiner des incidents de sécurité liés à l’identité. Cela rend votre organisation potentiellement vulnérable à une compromission d’informations d’identification réussie et à la menace qui en résulte pour les données sensibles de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0d91c-p105">If you skip this option, you won’t be able to detect or automatically thwart credential compromise attempts or investigate identity-related security incidents. This potentially leaves your organization vulnerable to a successful credential compromise and the resulting threat to your organization’s sensitive data.</span></span>

<span data-ttu-id="0d91c-160">Si nécessaire, l’[Étape 3](identity-secure-user-sign-ins.md#identity-ident-prot) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-160">If needed, [Step 3](identity-secure-user-sign-ins.md#identity-ident-prot) can help you with this option.</span></span>


### <a name="how-to-test"></a><span data-ttu-id="0d91c-161">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="0d91c-161">How to test</span></span>

1. <span data-ttu-id="0d91c-162">Créez un compte d’utilisateur test avec un mot de passe initial.</span><span class="sxs-lookup"><span data-stu-id="0d91c-162">Create a test user account with an initial password.</span></span>
2. <span data-ttu-id="0d91c-163">Suivez les étapes décrites dans [Autoriser les utilisateurs à réinitialiser leur mot de passe dans Office 365](https://docs.microsoft.com/office365/admin/add-users/let-users-reset-passwords) pour réinitialiser le mot de passe sur le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-163">Use the steps in [Let users reset their own passwords in Office 365](https://docs.microsoft.com/office365/admin/add-users/let-users-reset-passwords) to reset the password on the test user account.</span></span>
3. <span data-ttu-id="0d91c-164">Déconnectez-vous, puis connectez-vous au compte d’utilisateur test à l’aide du mot de passe réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="0d91c-164">Sign out and then sign in to the test user account using the reset password.</span></span>
4. <span data-ttu-id="0d91c-165">Supprimez le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-165">Delete the test user account.</span></span>

<a name="crit-identity-sync"></a>
## <a name="required-for-hybrid-identity-users-and-groups-are-synchronized-with-azure-ad"></a><span data-ttu-id="0d91c-166">Obligatoire pour l'identité hybride : les utilisateurs et les groupes sont synchronisés avec Azure AD</span><span class="sxs-lookup"><span data-stu-id="0d91c-166">Required: Users and groups are synchronized with Azure AD</span></span>

<span data-ttu-id="0d91c-167">Si vous disposez déjà des services de domaine Active Directory (AD DS) locaux, vous avez utilisé Azure AD Connect pour synchroniser les comptes et groupes d'utilisateurs depuis vos services AD DS locaux vers votre client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0d91c-167">If you have an existing on-premises identity provider, such as Active Directory Domain Services (AD DS), you have used Azure AD Connect to synchronize user accounts and groups from your on-premises identity provider to your Azure AD tenant.</span></span>

<span data-ttu-id="0d91c-168">Avec la synchronisation d’annuaires, vos utilisateurs peuvent se connecter à Office 365 et à d’autres services de cloud computing Microsoft à l’aide des mêmes informations d’identification qu’ils utilisent pour se connecter à leurs ordinateurs et accéder aux ressources locales.</span><span class="sxs-lookup"><span data-stu-id="0d91c-168">With directory synchronization, your users can sign in to Office 365 and other Microsoft cloud services using the same credentials that they use to sign in to their computers and access on-premises resources.</span></span>

<span data-ttu-id="0d91c-169">Si nécessaire, l’[Étape 4](identity-add-user-accounts.md#identity-sync) peut vous aider à respecter cette exigence.</span><span class="sxs-lookup"><span data-stu-id="0d91c-169">If needed, [Step 4](identity-add-user-accounts.md#identity-sync) can help you meet this requirement.</span></span>

<span data-ttu-id="0d91c-170">Si vous ignorez cette exigence, vous aurez deux ensembles de groupes et comptes d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0d91c-170">If you skip this requirement, you’ll have two sets of user accounts and groups:</span></span>

- <span data-ttu-id="0d91c-171">Groupes et comptes d’utilisateur qui existent dans vos services AD DS</span><span class="sxs-lookup"><span data-stu-id="0d91c-171">User accounts and groups that exist in your on-premises identity provider</span></span>
- <span data-ttu-id="0d91c-172">Groupes et comptes d’utilisateur qui existent dans votre client Azure AD</span><span class="sxs-lookup"><span data-stu-id="0d91c-172">User accounts and groups that exist in your Azure AD tenant</span></span>

<span data-ttu-id="0d91c-p106">Dans cet état, les deux ensembles de groupes et comptes d’utilisateur doivent être gérés manuellement par les administrateurs informatiques et les utilisateurs. Cela entraînera inévitablement des groupes, leurs mots de passe et comptes non synchronisés.</span><span class="sxs-lookup"><span data-stu-id="0d91c-p106">In this state, the two sets of user accounts and groups must be manually maintained by both IT administrators and users. This will inevitably lead to unsynchronized accounts, their passwords, and groups.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="0d91c-175">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="0d91c-175">How to test</span></span>
<span data-ttu-id="0d91c-176">Pour vérifier que l’authentification avec les informations d’identification locales fonctionne correctement, connectez-vous au portail Office avec vos informations d’identification locales.</span><span class="sxs-lookup"><span data-stu-id="0d91c-176">To verify that authentication with on-premises credentials works correctly, sign in to the Office portal with your on-premises credentials.</span></span>

<span data-ttu-id="0d91c-177">Pour vérifier que la synchronisation d’annuaires fonctionne correctement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0d91c-177">To verify that directory synchronization is working correctly, do the following:</span></span>

1.  <span data-ttu-id="0d91c-178">Créez un groupe de test dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="0d91c-178">Create a new test group in AD DS.</span></span>
2.  <span data-ttu-id="0d91c-179">Attendez l’heure de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="0d91c-179">Wait for the synchronization time.</span></span>
3.  <span data-ttu-id="0d91c-180">Vérifiez votre client Azure AD pour vous assurer que le nouveau nom du groupe de test apparaît.</span><span class="sxs-lookup"><span data-stu-id="0d91c-180">Check your Azure AD tenant to verify that the new test group name appears.</span></span>

<a name="crit-identity-sync-health"></a>
## <a name="optional-directory-synchronization-is-monitored"></a><span data-ttu-id="0d91c-181">Facultatif : la synchronisation d’annuaires est surveillée</span><span class="sxs-lookup"><span data-stu-id="0d91c-181">Optional: Directory synchronization is monitored</span></span>

<span data-ttu-id="0d91c-182">Vous avez utilisé [Utilisation d’Azure AD Connect Health pour la synchronisation](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) (pour la synchronisation de mot de passe) ou [Utilisation d’Azure AD Connect Health avec AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) (pour l’authentification fédérée) et avez déployé Azure AD Connect Health, ce qui implique :</span><span class="sxs-lookup"><span data-stu-id="0d91c-182">You've used [Azure AD Connect Health with sync](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) (for password synchronization) or [Using Azure AD Connect Health with AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) (for federated authentication) and have deployed Azure AD Connect Health, which involves:</span></span>

- <span data-ttu-id="0d91c-183">L’installation de l’agent Azure AD Connect Health sur chacun de vos serveurs d’identités local.</span><span class="sxs-lookup"><span data-stu-id="0d91c-183">Installing the Azure AD Connect Health agent on each of your on-premises identity servers.</span></span>
- <span data-ttu-id="0d91c-184">L’utilisation du portail Azure AD Connect Health pour surveiller l’état de synchronisation en cours.</span><span class="sxs-lookup"><span data-stu-id="0d91c-184">Using the Azure AD Connect Health portal to monitor the state of the ongoing synchronization.</span></span>

<span data-ttu-id="0d91c-185">Si vous ignorez cette option, vous pouvez évaluer plus précisément l’état de votre infrastructure d’identités basée sur le cloud.</span><span class="sxs-lookup"><span data-stu-id="0d91c-185">If you skip this option, you can more accurately assess the state of your cloud-based identity infrastructure.</span></span>

<span data-ttu-id="0d91c-186">Si nécessaire, l’[Étape 4](identity-add-user-accounts.md#identity-sync-health) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-186">If needed, [Step 4](identity-add-user-accounts.md#identity-sync-health) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="0d91c-187">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="0d91c-187">How to test</span></span>
<span data-ttu-id="0d91c-188">Le portail Azure AD Connect Health affiche l’état actuel et correct de vos contrôleurs de domaine locaux, ainsi que la synchronisation en cours.</span><span class="sxs-lookup"><span data-stu-id="0d91c-188">The Azure AD Connect Health portal shows the current and correct state of your on-premises identity servers and the ongoing synchronization.</span></span>


<a name="crit-identity-pw-writeback"></a>
## <a name="optional-password-writeback-is-enabled-for-your-users"></a><span data-ttu-id="0d91c-189">Facultatif : l’écriture différée du mot de passe est activée pour vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="0d91c-189">Optional: Password writeback is enabled for your users</span></span>

<span data-ttu-id="0d91c-190">Vous avez déjà consulté les instructions de la rubrique relative à la [réinitialisation du mot de passe libre-service d’Azure AD (SSPR) avec l’écriture différée du mot de passe](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) pour activer l’écriture différée du mot de passe pour le client Azure AD de votre abonnement Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="0d91c-190">You've used the instructions in [Azure AD SSPR with password writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) to enable password writeback for the Azure AD tenant of your Microsoft 365 Enterprise subscription.</span></span>

<span data-ttu-id="0d91c-191">Si vous ignorez cette option, les utilisateurs qui ne sont pas connectés à votre réseau local doivent réinitialiser ou déverrouiller leurs mot de passe AD DS en faisant appel à un administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="0d91c-191">If you skip this option, users who aren’t connected to your on-premises network must reset or unlock their AD DS passwords through an IT administrator.</span></span>

<span data-ttu-id="0d91c-192">Si nécessaire, l’[Étape 4](identity-add-user-accounts.md#identity-pw-writeback) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-192">If needed, [Step 4](identity-add-user-accounts.md#identity-pw-writeback) can help you with this option.</span></span>

>[!Note]
><span data-ttu-id="0d91c-193">L’écriture différée du mot de passe est requise pour exploiter pleinement les fonctionnalités d’Azure AD Identity Protection, comme l’obligation pour les utilisateurs de modifier leurs mots de passe locaux lorsque Azure AD a détecté un risque élevé de compromission de compte.</span><span class="sxs-lookup"><span data-stu-id="0d91c-193">Password writeback is required to fully utilize Azure AD Identity Protection features, such as requiring users to change their on-premises passwords when Azure AD has detected a high risk of account compromise.</span></span>
>

### <a name="how-to-test"></a><span data-ttu-id="0d91c-194">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="0d91c-194">How to test</span></span>

<span data-ttu-id="0d91c-195">Vous testez l’écriture différée de votre mot de passe en changeant votre mot de passe Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d91c-195">You test password writeback by changing your password in Office 365.</span></span> <span data-ttu-id="0d91c-196">Vous devriez pouvoir utiliser votre compte et le nouveau mot de passe pour accéder aux ressources AD DS locales.</span><span class="sxs-lookup"><span data-stu-id="0d91c-196">You should be able to use your account and new password to access on-premises AD DS resources.</span></span>

1. <span data-ttu-id="0d91c-197">Créez un compte d’utilisateur test dans votre version locale AD DS, autorisez la synchronisation d’annuaires, puis accordez-lui une licence Microsoft 365 Entreprise dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0d91c-197">Create a test user account in your on-premises AD DS, allow directory synchronization to occur, and then grant it an Office 365 license in the Microsoft 365 admin center.</span></span>
2. <span data-ttu-id="0d91c-198">Sur un ordinateur distant qui est relié à votre domaine Server AD DS local, connectez-vous à l’ordinateur et au portail Office à l’aide des informations d’identification du compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-198">From a remote computer that is joined to your on-premises AD DS domain, sign in to the computer and the Office portal using the credentials of the test user account.</span></span>
3. <span data-ttu-id="0d91c-199">Sélectionnez **Paramètres > Paramètres Office 365 > Mot de passe > Changer le mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="0d91c-199">Select **Settings > Office 365 settings > Password > Change password**.</span></span>
4. <span data-ttu-id="0d91c-200">Tapez le mot de passe actuel, tapez un nouveau mot de passe, puis confirmez-le.</span><span class="sxs-lookup"><span data-stu-id="0d91c-200">Type the current password, type a new password, and then confirm it.</span></span>
5. <span data-ttu-id="0d91c-201">Déconnectez-vous du portail Office et de l’ordinateur distant, puis connectez-vous à l’ordinateur à l’aide du compte d’utilisateur de test et son nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="0d91c-201">Sign out of the Office portal and the remote computer and then sign in to the computer using the test user account and its new password.</span></span> <span data-ttu-id="0d91c-202">Cela prouve que vous avez été en mesure de modifier le mot de passe d’une version locale de compte d’utilisateur AD DS à l’aide du client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0d91c-202">This proves that you were able to change the password of an on-premises AD DS user account using the Azure AD tenant.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="0d91c-203">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="0d91c-203">How to test</span></span>

<span data-ttu-id="0d91c-204">Connectez-vous au portail Office 365 avec le nom de votre compte d’utilisateur et l’authentification multifacteur Azure.</span><span class="sxs-lookup"><span data-stu-id="0d91c-204">Sign in to the Office 365 portal with your user account name and Azure Multi-Factor Authentication.</span></span> <span data-ttu-id="0d91c-205">Vous devez voir vos éléments de marque personnalisés dans la page de connexion.</span><span class="sxs-lookup"><span data-stu-id="0d91c-205">Sign in to the Office 365 portal with your user account name and multi-factor authentication. You should see your custom branding elements on the sign-in page.</span></span>


<a name="crit-identity-self-service-groups"></a>
## <a name="optional-self-service-group-management-is-enabled-for-specific-azure-ad-security-and-office-365-groups"></a><span data-ttu-id="0d91c-206">Facultatif : la gestion des groupes en libre-service est activée pour des groupes Office 365 et de sécurité Azure AD spécifiques</span><span class="sxs-lookup"><span data-stu-id="0d91c-206">Optional: Self-service group management is enabled for specific Azure AD security and Office 365 groups</span></span>

<span data-ttu-id="0d91c-207">Vous avez déterminé les groupes qui sont appropriés pour la gestion en libre service, décrit à leurs propriétaires les responsabilités et le workflow de gestion des groupes et [configuré la gestion en libre-service dans Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management) pour ces groupes.</span><span class="sxs-lookup"><span data-stu-id="0d91c-207">You've determined which groups are appropriate for self-service management, instructed their owners on group management workflow and responsibilities, and [set up self-service management in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management) for those groups.</span></span>

<span data-ttu-id="0d91c-208">Si vous ignorez cette option, toutes les tâches de gestion des groupes Azure AD doivent être effectuées par des administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="0d91c-208">If you skip this option, all Azure AD group management tasks must be done by IT administrators.</span></span>

<span data-ttu-id="0d91c-209">Si nécessaire, l’[Étape 5](identity-use-group-management.md#identity-self-service-groups) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-209">If needed, [Step 5](identity-use-group-management.md#identity-self-service-groups) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="0d91c-210">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="0d91c-210">How to test</span></span>
1.  <span data-ttu-id="0d91c-211">Créez un compte d’utilisateur test dans Azure AD avec le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="0d91c-211">Create a test user account in Azure AD with the Azure portal.</span></span>
2.  <span data-ttu-id="0d91c-212">Connectez-vous comme avec le compte d’utilisateur test et créez un groupe de sécurité Azure AD test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-212">Sign-in as with the test user account and create a test Azure AD security group.</span></span>
3.  <span data-ttu-id="0d91c-213">Déconnectez-vous, puis connectez-vous avec votre compte Administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="0d91c-213">Sign out and then sign-in with your IT administrator account.</span></span>
4.  <span data-ttu-id="0d91c-214">Configurez le groupe de sécurité test pour la gestion en libre service pour le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-214">Configure the test security group for self-service management for the test user account.</span></span>
5.  <span data-ttu-id="0d91c-215">Déconnectez-vous, puis connectez-vous avec votre compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-215">Sign out and then sign-in with your test user account.</span></span>
6.  <span data-ttu-id="0d91c-216">Utilisez le portail Azure pour ajouter des membres au groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-216">Use the Azure portal to add members to the test security group.</span></span>
7.  <span data-ttu-id="0d91c-217">Supprimez le groupe de sécurité test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-217">Delete the test security group and the test user account.</span></span>

<a name="crit-identity-dyn-groups"></a>
## <a name="optional-dynamic-group-membership-settings-automatically-add-user-accounts-to-groups-based-on-user-account-attributes"></a><span data-ttu-id="0d91c-218">Facultatif : les paramètres d’appartenance à un groupe dynamique ajoutent automatiquement des comptes d’utilisateur à des groupes en fonction des attributs de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0d91c-218">Optional: Dynamic group membership settings automatically add user accounts to groups based on user account attributes</span></span>

<span data-ttu-id="0d91c-219">Vous avez déterminé l’ensemble des groupes dynamiques Azure AD et utilisé les instructions décrites dans la rubrique relative à l’[appartenance à un groupe dynamique en fonction des attributs dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal) pour créer les groupes et les règles qui déterminent l’ensemble des attributs de compte d’utilisateur et des valeurs pour l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="0d91c-219">You've determined the set of Azure AD dynamic groups and used the instructions in [Attribute-based dynamic group membership in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal) to create the groups and the rules that determine the set of user account attributes and values for group membership.</span></span>

<span data-ttu-id="0d91c-p110">Si vous ignorez cette option, l’appartenance à un groupe doit être effectuée manuellement lorsque de nouveaux comptes sont ajoutés ou que les attributs de compte d’utilisateur changent au fil du temps. Par exemple, si une personne est mutée du service des ventes au service de comptabilité, vous devez :</span><span class="sxs-lookup"><span data-stu-id="0d91c-p110">If you skip this option, group membership must be done manually as new accounts are added or as user account attributes change over time. For example, if someone moves from the Sales department to the Accounting department, you must:</span></span>

- <span data-ttu-id="0d91c-222">mettre à jour la valeur de l’attribut Service pour ce compte d’utilisateur ;</span><span class="sxs-lookup"><span data-stu-id="0d91c-222">Update the value of the Department attribute for that user account.</span></span>
- <span data-ttu-id="0d91c-223">le supprimer manuellement du groupe Ventes ;</span><span class="sxs-lookup"><span data-stu-id="0d91c-223">Manually remove them from the Sales group.</span></span>
- <span data-ttu-id="0d91c-224">l’ajouter manuellement au groupe Comptabilité.</span><span class="sxs-lookup"><span data-stu-id="0d91c-224">Manually add them to the Accounting group.</span></span>

<span data-ttu-id="0d91c-225">Si les groupes Ventes et Comptabilité sont dynamiques, vous devez uniquement modifier la valeur Service du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0d91c-225">If the Sales and Accounting groups were dynamic, you would only have to change the user account’s Department value.</span></span>

<span data-ttu-id="0d91c-226">Si nécessaire, l’[Étape 5](identity-use-group-management.md#identity-dyn-groups) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-226">If needed, [Step 5](identity-use-group-management.md#identity-dyn-groups) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="0d91c-227">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="0d91c-227">How to test</span></span>

1. <span data-ttu-id="0d91c-228">Créez un groupe dynamique test dans Azure AD avec le portail Azure et configurez une règle pour que Service soit égal à « test1 ».</span><span class="sxs-lookup"><span data-stu-id="0d91c-228">Create a test dynamic group in Azure AD with the Azure portal and configure a rule for the Department equals “test1”.</span></span>
2. <span data-ttu-id="0d91c-229">Créez un compte d’utilisateur test dans Azure AD et définissez la propriété Service sur « test1 ».</span><span class="sxs-lookup"><span data-stu-id="0d91c-229">Create a test user account in Azure AD and set the Department property to “test1”.</span></span>
3. <span data-ttu-id="0d91c-230">Examinez les propriétés du compte d’utilisateur pour vous assurer qu’il a été défini comme membre du groupe dynamique test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-230">Examine the properties of the user account to ensure that it was made a member of the test dynamic group.</span></span>
4. <span data-ttu-id="0d91c-231">Modifiez la valeur de la propriété Service pour le compte d’utilisateur test et définissez-la sur « test2 ».</span><span class="sxs-lookup"><span data-stu-id="0d91c-231">Change the value of the Department property for the test user account to “test2”.</span></span>
5. <span data-ttu-id="0d91c-232">Examinez les propriétés du compte d’utilisateur pour vous assurer qu’il n’est plus membre du groupe dynamique test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-232">Examine the properties of the user account to ensure that it is no longer a member of the test dynamic group.</span></span>
6. <span data-ttu-id="0d91c-233">Supprimez le groupe dynamique test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-233">Delete the test dynamic group and the test user account.</span></span>

<a name="crit-identity-group-license"></a>
## <a name="optional-group-based-licensing-to-automatically-assign-and-remove-licenses-to-user-accounts-based-on-group-membership"></a><span data-ttu-id="0d91c-234">Facultatif : gestion des licences par groupes pour attribuer des licences aux comptes d’utilisateur et les supprimer automatiquement en fonction de l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="0d91c-234">Optional: Group-based licensing to automatically assign and remove licenses to user accounts based on group membership</span></span>

<span data-ttu-id="0d91c-235">Vous [avez activé l'attribution de licences par groupe](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal) pour les groupes de sécurité Azure AD appropriés afin que des licences pour Microsoft 365 Entreprise soient automatiquement attribuées ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="0d91c-235">You [enabled group-based licensing](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal) for the appropriate Azure AD security groups so that licenses for both Office 365 and EMS are automatically assigned or removed.</span></span>

<span data-ttu-id="0d91c-236">Si vous ignorez cette option, vous devez effectuer les opérations suivantes manuellement :</span><span class="sxs-lookup"><span data-stu-id="0d91c-236">If you skip this option, you must manually:</span></span>

- <span data-ttu-id="0d91c-237">Attribuer des licences aux nouveaux utilisateurs auxquels vous avez l'intention d'accéder.</span><span class="sxs-lookup"><span data-stu-id="0d91c-237">Assign licenses to new users whom you intend to have access to Office 365 and EMS.</span></span>
- <span data-ttu-id="0d91c-238">Supprimer les licences des utilisateurs qui ne font plus partie de votre organisation ou qui n'y ont pas accès.</span><span class="sxs-lookup"><span data-stu-id="0d91c-238">Remove licenses from users who are no longer with your organization or do not have access to Office 365 and EMS.</span></span>

<span data-ttu-id="0d91c-239">Si nécessaire, l’[Étape 5](identity-use-group-management.md#identity-group-license) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-239">If needed, [Step 5](identity-use-group-management.md#identity-group-license) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="0d91c-240">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="0d91c-240">How to test</span></span>

1. <span data-ttu-id="0d91c-241">Créez un groupe de sécurité test dans Azure AD à l’aide du portail Azure et configurez l’attribution de licences par groupes pour attribuer des licences Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="0d91c-241">Create a test security group in Azure AD with the Azure portal and configure group-based licensing to assign Office 365 and EMS licenses.</span></span>
2. <span data-ttu-id="0d91c-242">Créez un compte d’utilisateur test dans Azure AD et ajoutez-le au groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-242">Create a test user account in Azure AD and add it to the test security group.</span></span>
3. <span data-ttu-id="0d91c-243">Examinez les propriétés du compte d’utilisateur dans le Centre d’administration Microsoft 365 pour vous assurer que les licences Microsoft 365 Entreprise lui ont été attribuées.</span><span class="sxs-lookup"><span data-stu-id="0d91c-243">Examine the properties of the user account in the Microsoft 365 admin center to ensure that it was assigned the Office 365 and EMS licenses.</span></span>
4. <span data-ttu-id="0d91c-244">Supprimez le compte d’utilisateur test du groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-244">Remove the test user account from the test security group.</span></span>
5. <span data-ttu-id="0d91c-245">Examinez les propriétés du compte d’utilisateur pour vous assurer que les licences Microsoft 365 Entreprise ne lui sont plus attribuées.</span><span class="sxs-lookup"><span data-stu-id="0d91c-245">Examine the properties of the user account to ensure that it no longer has the Office 365 and EMS licenses assigned.</span></span>
6. <span data-ttu-id="0d91c-246">Supprimez le groupe de sécurité test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="0d91c-246">Delete the test security group and the test user account.</span></span>


<a name="crit-identity-access-reviews"></a>
## <a name="optional-access-reviews-configured-and-being-used-to-monitor-access"></a><span data-ttu-id="0d91c-247">Facultatif : révisions d'accès configurées et utilisées pour contrôler l'accès</span><span class="sxs-lookup"><span data-stu-id="0d91c-247">Optional: Access reviews configured and being used to monitor access</span></span>

<span data-ttu-id="0d91c-248">Vous avez utilisé ces articles pour configurer différents types de révisions d’accès afin de contrôler les appartenances aux groupes, l’accès aux applications d’entreprise et les attributions de rôle :</span><span class="sxs-lookup"><span data-stu-id="0d91c-248">You have used these articles to configure different types of access reviews to monitor group memberships, access to enterprise applications, and role assignments:</span></span>

- [<span data-ttu-id="0d91c-249">Groupes et applications</span><span class="sxs-lookup"><span data-stu-id="0d91c-249">Groups and apps</span></span>](https://docs.microsoft.com/azure/active-directory/governance/create-access-review)
- [<span data-ttu-id="0d91c-250">Rôles Azure AD</span><span class="sxs-lookup"><span data-stu-id="0d91c-250">Azure AD roles</span></span>](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-how-to-start-security-review?toc=%2fazure%2factive-directory%2fgovernance%2ftoc.json)
- [<span data-ttu-id="0d91c-251">Rôles de ressources Azure</span><span class="sxs-lookup"><span data-stu-id="0d91c-251">Azure resource roles</span></span>](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-start-access-review?toc=%2fazure%2factive-directory%2fgovernance%2ftoc.json)

<span data-ttu-id="0d91c-252">Si nécessaire, l’[Étape 6](identity-configure-identity-governance.md#identity-access-reviews) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="0d91c-252">If needed, [Step 6](identity-configure-identity-governance.md#identity-access-reviews) can help you with this option.</span></span>


## <a name="results-and-next-steps"></a><span data-ttu-id="0d91c-253">Résultats et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0d91c-253">Results and next steps</span></span>

<span data-ttu-id="0d91c-254">Votre infrastructure d’identité dans le cloud de Microsoft 365 utilise l’authentification forte, comptes administrateur protégés et l’accès et gestion utilisateur simplifiés.</span><span class="sxs-lookup"><span data-stu-id="0d91c-254">Your identity infrastructure in the Microsoft 365 cloud uses strong authentication, protected administrator accounts, and simplified user access and management.</span></span>

|||
|:-------|:-----|
|![](./media/deploy-foundation-infrastructure/win10enterprise_icon-small.png)| <span data-ttu-id="0d91c-255">Si vous suivez les phases suivantes dans le processus de déploiement de bout en bout pour Microsoft 365 Entreprise, la suivante est la [Windows 10 Entreprise](windows10-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="0d91c-255">If you're following the phases for the end-to-end deployment of Microsoft 365 Enterprise, your next phase is [Windows 10 Enterprise](windows10-infrastructure.md).</span></span> |

