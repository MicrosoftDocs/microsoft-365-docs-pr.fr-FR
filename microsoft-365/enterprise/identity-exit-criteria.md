---
title: 'Phase 2 : Critères de sortie de l’infrastructure d’identités'
f1.keywords:
- NOCSH
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
ms.openlocfilehash: 3fd4d0a1df50d55cb7a21668b609341d0c01aa35
ms.sourcegitcommit: 6c8edbc54b193e964cf93aec48c51cb79231f1d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "42544063"
---
# <a name="phase-2-identity-infrastructure-exit-criteria"></a><span data-ttu-id="8a7f1-103">Phase 2 : Critères de sortie de l’infrastructure d’identités</span><span class="sxs-lookup"><span data-stu-id="8a7f1-103">Phase 2: Identity infrastructure exit criteria</span></span>

![Phase 2 - Identité](../media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="8a7f1-105">Vérifiez que votre infrastructure d’identité répond aux critères suivants requis et que vous avez décidé ceux qui sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-105">Make sure your identity infrastructure meets the following required criteria and that you've considered those that are optional.</span></span>

<span data-ttu-id="8a7f1-106">Voir également les [Conditions préalables](https://docs.microsoft.com/microsoft-365/enterprise/identity-access-prerequisites) pour consulter d’autre suggestions sur l’infrastructure d’identité.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-106">Also see [Prerequisites](https://docs.microsoft.com/microsoft-365/enterprise/identity-access-prerequisites) for additional recommendations on identity infrastructure.</span></span>

<a name="crit-identity-global-admin"></a>
## <a name="required-your-global-administrator-accounts-are-protected"></a><span data-ttu-id="8a7f1-107">Obligatoire : vos comptes d’administrateur général sont protégés</span><span class="sxs-lookup"><span data-stu-id="8a7f1-107">Required: Your global administrator accounts are protected</span></span> 

<span data-ttu-id="8a7f1-108">Vous avez [protégé vos comptes d’administrateur général Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts) pour éviter que des attaques ne compromettent l'intégrité des informations d'identification, ce qui peut entraîner des violations de votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-108">You've [protected your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts) to thwart  credential compromise by attackers that can lead to breaches of your Microsoft 365 subscription.</span></span>

<span data-ttu-id="8a7f1-109">Si vous ignorez cette exigence, vos comptes d’administrateur général peuvent être attaqués et compromis, autorisant un utilisateur à accéder à vos données à l’échelle du système à des fins de collecte, destruction ou prise en otage des données.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-109">If you skip this requirement, your global administrator accounts can be susceptible to attack and compromise, allowing an attacker to gain system-wide access to your data for harvesting, destruction, or ransom.</span></span>

<span data-ttu-id="8a7f1-110">Si nécessaire, l’[Étape 1](identity-create-protect-global-admins.md#identity-global-admin) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-110">If needed, [Step 1](identity-create-protect-global-admins.md#identity-global-admin) can help you meet this requirement.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="8a7f1-111">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="8a7f1-111">How to test</span></span>

<span data-ttu-id="8a7f1-112">Suivez ces étapes pour vérifier que vous avez protégé vos comptes d’administrateur général :</span><span class="sxs-lookup"><span data-stu-id="8a7f1-112">Use these steps to verify that you've protected your global administrator accounts:</span></span>

1. <span data-ttu-id="8a7f1-113">Exécutez la commande suivante Azure Active Directory PowerShell pour Graph à l'invite de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-113">Run the following Azure Active Directory PowerShell for Graph command at the PowerShell command prompt.</span></span> <span data-ttu-id="8a7f1-114">Vous ne devez voir que la liste des comptes d’administrateur général dédiés.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-114">You should see only the list of dedicated global administrator accounts.</span></span>
   ```powershell
   Get-AzureADDirectoryRole | where { $_.DisplayName -eq "Company Administrator" } | Get-AzureADDirectoryRoleMember | Ft DisplayName
   ```
2. <span data-ttu-id="8a7f1-115">Connectez-vous à Office 365 à l’aide de chacun des comptes de l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-115">Sign in to Office 365 using each of the accounts from step 1.</span></span> <span data-ttu-id="8a7f1-116">Chaque connexion doit exiger l’authentification multifacteur Azure et la forme la plus forte d’authentification secondaire disponible dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-116">Each sign in must require Azure Multi-Factor Authentication and the strongest form of secondary authentication available in your organization.</span></span>

> [!Note]
> <span data-ttu-id="8a7f1-117">Reportez-vous à [Se connecter à Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) pour obtenir des instructions sur l’installation du module Azure AD PowerShell pour Graph et la connexion à Office 365.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-117">See [Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) for instructions on installing the Azure Active Directory PowerShell for Graph module and signing in to Office 365.</span></span>

<a name="crit-identity-pim"></a>
## <a name="optional-you-have-set-up-privileged-identity-management-to-support-on-demand-assignment-of-the-global-administrator-role"></a><span data-ttu-id="8a7f1-118">Facultatif : vous avez configuré Privileged Identity Management pour prendre en charge l’affectation à la demande du rôle Administrateur général</span><span class="sxs-lookup"><span data-stu-id="8a7f1-118">Optional: You have set up Privileged Identity Management to support on-demand assignment of the global administrator role</span></span>

<span data-ttu-id="8a7f1-119">Vous avez déjà suivi les instructions de la rubrique [Configuration d’Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure) pour activer PIM dans votre client Azure AD et configuré vos comptes d’administrateur général comme administrateurs éligibles.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-119">You've used the instructions in [Configure Azure AD Privileged Identity Management (PIM)](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure) to enable PIM in your Azure AD tenant and configured your global administrator accounts as eligible admins.</span></span>

<span data-ttu-id="8a7f1-120">Vous avez également suivi les recommandations de la rubrique relative à la [sécurisation de l’accès privilégié pour les déploiements hybrides et cloud dans Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) pour développer une feuille de route qui sécurise l’accès privilégié contre les cyber-attaquants.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-120">You've also used the recommendations in [Securing privileged access for hybrid and cloud deployments in Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) to develop a roadmap that secures privileged access against cyber attackers.</span></span>

<span data-ttu-id="8a7f1-121">Si vous ignorez cette option, vos comptes Administrateur général sont soumis à des attaques en ligne en continu et, en cas de compromission, peuvent autoriser un utilisateur à recueillir, détruire ou conserver vos informations sensibles contre rançon.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-121">If you skip this option, your global administrator accounts are subject to ongoing online attack and, if compromised, can allow an attacker to harvest, destroy, or hold your sensitive information for ransom.</span></span>

<span data-ttu-id="8a7f1-122">Si nécessaire, l’[Étape 1](identity-create-protect-global-admins.md#identity-pim) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-122">If needed, [Step 1](identity-create-protect-global-admins.md#identity-pim) can help you with this option.</span></span>

<a name="crit-identity-pam"></a>
## <a name="optional-you-have-configure-privileged-access-management-in-office-365"></a><span data-ttu-id="8a7f1-123">Facultatif : vous avez configuré la gestion des accès privilégiés dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8a7f1-123">Optional: You have configure privileged access management in Office 365</span></span>

<span data-ttu-id="8a7f1-124">Vous avez utilisé les informations de la rubrique [Configurer la gestion des accès privilégiés dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) pour activer l’accès privilégié et créer une ou plusieurs stratégies d’accès privilégié au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-124">You've used the information in the [Configure privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) topic to enable privileged access and create one or more privileged access policies in your organization.</span></span> <span data-ttu-id="8a7f1-125">Vous avez configuré ces stratégies et l’accès juste-à-temps est activé pour l’accès aux données sensibles ou aux paramètres de configuration critiques.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-125">You've configured these policies and just-in-time access is enabled for access to sensitive data or access to critical configuration settings.</span></span>

<span data-ttu-id="8a7f1-126">Si nécessaire, l’[Étape 1](identity-create-protect-global-admins.md#identity-pam) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-126">If needed, [Step 1](identity-create-protect-global-admins.md#identity-pam) can help you meet this requirement.</span></span> 

<a name="crit-password-prot"></a>
## <a name="optional-azure-ad-password-protection-is-banning-the-use-of-weak-passwords"></a><span data-ttu-id="8a7f1-127">Facultatif : la protection de mot de passe Azure AD interdit l'utilisation de mots de passe faibles</span><span class="sxs-lookup"><span data-stu-id="8a7f1-127">Optional: Azure AD password protection is banning the use of weak passwords</span></span>

<span data-ttu-id="8a7f1-128">Vous avez activé l'interdiction des mauvais mots de passe [dans le cloud](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad) et pour vos [services de domaine Active Directory (AD DS) locaux](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad-on-premises) pour les mots de passe généraux interdits et, éventuellement, pour les termes personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-128">You have enabled the banning of bad passwords [in the cloud](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad) and for your [on-premises Active Directory Domain Services (AD DS)](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad-on-premises) for global banned passwords and, optionally, for custom terms.</span></span>

<span data-ttu-id="8a7f1-129">Si nécessaire, l’[Étape 2](identity-secure-your-passwords.md#identity-password-prot) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-129">If needed, [Step 2](identity-secure-your-passwords.md#identity-password-prot) can help you with this option.</span></span>

<a name="crit-identity-pw-reset"></a>
## <a name="optional-users-can-reset-their-own-passwords"></a><span data-ttu-id="8a7f1-130">Facultatif : les utilisateurs peuvent réinitialiser leurs mots de passe</span><span class="sxs-lookup"><span data-stu-id="8a7f1-130">Optional: Users can reset their own passwords</span></span>

<span data-ttu-id="8a7f1-131">Vous avez utilisé la rubrique relative au [déploiement rapide de la réinitialisation du mot de passe libre-service Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) pour configurer la réinitialisation du mot de passe pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-131">You've used [Azure AD self-service password reset rapid deployment](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) to configure password reset for your users.</span></span>

<span data-ttu-id="8a7f1-132">Si vous ne remplissez pas cette condition, les utilisateurs dépendront des administrateurs de compte d’utilisateur pour réinitialiser leurs mots de passe, entraînant une surcharge d’administration informatique supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-132">If you don’t meet this condition, users will be dependent on user account administrators to reset their passwords, resulting in additional IT administration overhead.</span></span>

<span data-ttu-id="8a7f1-133">Si nécessaire, l’[Étape 2](identity-secure-your-passwords.md#identity-pw-reset) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-133">If needed, [Step 2](identity-secure-your-passwords.md#identity-pw-reset) can help you with this option.</span></span>

<a name="crit-identity-sso"></a>
## <a name="optional-users-can-sign-in-using-azure-ad-seamless-single-sign-on"></a><span data-ttu-id="8a7f1-134">Facultatif : les utilisateurs peuvent se connecter à l’aide de l’authentification unique Azure AD Single Sign-on</span><span class="sxs-lookup"><span data-stu-id="8a7f1-134">Optional: Users can sign in using Azure AD Seamless Single Sign-on</span></span>

<span data-ttu-id="8a7f1-135">Vous avez activé l’[authentification unique transparente Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start) pour que votre organisation simplifie la manière dont les utilisateurs se connectent aux applications basées sur le cloud, comme Office 365.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-135">You enabled [Azure AD Connect: Seamless Single Sign-On](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start) for your organization to simplify how users sign in to cloud-based applications, such as Office 365.</span></span>

<span data-ttu-id="8a7f1-136">Si vous ignorez cette option, vos utilisateurs peuvent être invités à fournir des informations d’identification lorsqu’ils accèdent à d’autres applications qui utilisent votre client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-136">If you skip this option, your users might be prompted to provide credentials when they access additional applications that use you Azure AD tenant.</span></span>

<span data-ttu-id="8a7f1-137">Si nécessaire, l’[Étape 2](identity-secure-your-passwords.md#identity-sso) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-137">If needed, [Step 2](identity-secure-your-passwords.md#identity-sso) can help you with this option.</span></span>

<a name="crit-identity-custom-sign-in"></a>
## <a name="optional-the-office-365-sign-in-screen-is-personalized-for-your-organization"></a><span data-ttu-id="8a7f1-138">Facultatif : l’écran de connexion Office 365 est personnalisé pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="8a7f1-138">Optional: The Office 365 sign-in screen is personalized for your organization</span></span>

<span data-ttu-id="8a7f1-139">Vous avez utilisé [Ajouter la marque de votre organisation à votre page de connexion et aux pages du Panneau d’accès](https://aka.ms/aadpaddbranding) pour ajouter la marque de votre organisation à la page de connexion Office 365.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-139">You have used [Add company branding to your sign-in and Access Panel pages](https://aka.ms/aadpaddbranding) to add your organization’s branding to the Office 365 sign-in page.</span></span>

<span data-ttu-id="8a7f1-140">Si vous ignorez cette option, vos utilisateurs verront un écran de connexion Office 365 générique et peuvent ne pas être certains de se connecter au site de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-140">If you skip this option, your users will see a generic Office 365 sign-in screen and might not be confident that they’re signing into your organization’s site.</span></span>

<span data-ttu-id="8a7f1-141">Si nécessaire, l’[Étape 2](identity-secure-your-passwords.md#identity-custom-sign-in) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-141">If needed, [Step 2](identity-secure-your-passwords.md#identity-custom-sign-in) can help you with this option.</span></span>


<a name="crit-identity-mfa"></a>
## <a name="optional-azure-multi-factor-authentication-is-enabled-for-your-users"></a><span data-ttu-id="8a7f1-142">Facultatif : l’authentification multifacteur Azure est activée pour vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8a7f1-142">Optional: Azure Multi-Factor Authentication is enabled for your users</span></span>

<span data-ttu-id="8a7f1-143">Vous avez utilisé [Offre pour l’authentification multifacteur Azure](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted) et les [stratégies d’accès conditionnel](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted#enable-multi-factor-authentication-with-conditional-access) pour activer l’authentification multifacteur Azure (MFA) pour vos comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-143">You used [Plan for Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted) and [Conditional Access policies](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted#enable-multi-factor-authentication-with-conditional-access) to enable Azure Multi-Factor Authentication (MFA) for your user accounts.</span></span>

<span data-ttu-id="8a7f1-p104">Si vous ignorez cette option, vos comptes d’utilisateur sont vulnérables à la compromission des informations d’identification par des cyber-attaquants. Si le mot de passe d’un compte d’utilisateur est compromis, toutes les ressources et les fonctionnalités du compte, telles que les rôles d’administrateur, sont disponibles pour l’utilisateur malveillant. Ainsi, ce dernier peut copier, détruire ou conserver des documents internes et d’autres données contre rançon.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-p104">If you skip this option, your user accounts are vulnerable to credential compromise by cyber attackers. If a user account’s password is compromised, all the resources and capabilities of the account, such as administrator roles, are available to the attacker. This allows the attacker to copy, destroy, or hold for ransom internal documents and other data.</span></span>

<span data-ttu-id="8a7f1-147">Si nécessaire, l’[Étape 3](identity-secure-user-sign-ins.md#identity-mfa) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-147">If needed, [Step 3](identity-secure-user-sign-ins.md#identity-mfa) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="8a7f1-148">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="8a7f1-148">How to test</span></span>

1.  <span data-ttu-id="8a7f1-149">Créez un compte d’utilisateur test et attribuez-lui une licence.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-149">Create a test user account and assign them a license.</span></span> 
2.  <span data-ttu-id="8a7f1-150">Configurez l’authentification multifacteur Azure pour le compte d’utilisateur test avec la méthode de vérification supplémentaire que vous utilisez pour les comptes d’utilisateur réels, comme l’envoi d’un SMS sur votre téléphone.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-150">Configure Azure Multi-Factor Authentication for the test user account with the additional verification method that you are using for actual user accounts, such as sending a text message to your phone.</span></span> 
3.  <span data-ttu-id="8a7f1-151">Connectez-vous au portail Office 36 avec le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-151">Sign in to the Office 36 portal with the test user account.</span></span>
4.  <span data-ttu-id="8a7f1-152">Vérifiez que l’authentification multifacteur vous invite à saisir les informations de vérification supplémentaires et que l’authentification s’effectue sans problèmes.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-152">Verify that MFA prompts you for the additional verification information and results in a successful authentication.</span></span> 
5.  <span data-ttu-id="8a7f1-153">Supprimez le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-153">Delete the test user account.</span></span>

<a name="crit-identity-ident-prot"></a>
## <a name="optional-azure-ad-identity-protection-is-enabled-to-protect-against-credential-compromise-microsoft-365-e5-only"></a><span data-ttu-id="8a7f1-154">Facultatif : Azure AD Identity Protection est activé pour vous protéger contre la compromission d’informations d’identification (Microsoft 365 E5 uniquement)</span><span class="sxs-lookup"><span data-stu-id="8a7f1-154">Optional: Azure AD Identity Protection is enabled to protect against credential compromise (Microsoft 365 E5 only)</span></span>

<span data-ttu-id="8a7f1-155">Vous avez activé Azure AD Identity Protection pour :</span><span class="sxs-lookup"><span data-stu-id="8a7f1-155">You've enabled Azure AD Identity Protection to:</span></span>

- <span data-ttu-id="8a7f1-156">résoudre les vulnérabilités d’identités potentielles ;</span><span class="sxs-lookup"><span data-stu-id="8a7f1-156">Address potential identity vulnerabilities.</span></span>
- <span data-ttu-id="8a7f1-157">détecter les tentatives de compromission d’informations d’identification possibles ;</span><span class="sxs-lookup"><span data-stu-id="8a7f1-157">Detect possible credential compromise attempts.</span></span>
- <span data-ttu-id="8a7f1-158">examiner et résoudre des incidents d’identités suspects en cours.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-158">Investigate and address ongoing suspicious identity incidents.</span></span>

<span data-ttu-id="8a7f1-p105">Si vous ignorez cette option, vous ne pourrez pas détecter ou empêcher automatiquement les tentatives de compromission d’informations d’identification ni examiner des incidents de sécurité liés à l’identité. Cela rend votre organisation potentiellement vulnérable à une compromission d’informations d’identification réussie et à la menace qui en résulte pour les données sensibles de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-p105">If you skip this option, you won’t be able to detect or automatically thwart credential compromise attempts or investigate identity-related security incidents. This potentially leaves your organization vulnerable to a successful credential compromise and the resulting threat to your organization’s sensitive data.</span></span>

<span data-ttu-id="8a7f1-161">Si nécessaire, l’[Étape 3](identity-secure-user-sign-ins.md#identity-ident-prot) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-161">If needed, [Step 3](identity-secure-user-sign-ins.md#identity-ident-prot) can help you with this option.</span></span>


### <a name="how-to-test"></a><span data-ttu-id="8a7f1-162">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="8a7f1-162">How to test</span></span>

1. <span data-ttu-id="8a7f1-163">Créez un compte d’utilisateur test avec un mot de passe initial.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-163">Create a test user account with an initial password.</span></span>
2. <span data-ttu-id="8a7f1-164">Suivez les étapes décrites dans [Autoriser les utilisateurs à réinitialiser leur mot de passe dans Office 365](https://docs.microsoft.com/office365/admin/add-users/let-users-reset-passwords) pour réinitialiser le mot de passe sur le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-164">Use the steps in [Let users reset their own passwords in Office 365](https://docs.microsoft.com/office365/admin/add-users/let-users-reset-passwords) to reset the password on the test user account.</span></span>
3. <span data-ttu-id="8a7f1-165">Déconnectez-vous, puis connectez-vous au compte d’utilisateur test à l’aide du mot de passe réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-165">Sign out and then sign in to the test user account using the reset password.</span></span>
4. <span data-ttu-id="8a7f1-166">Supprimez le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-166">Delete the test user account.</span></span>

<a name="crit-identity-sync"></a>
## <a name="required-for-hybrid-identity-users-and-groups-are-synchronized-with-azure-ad"></a><span data-ttu-id="8a7f1-167">Obligatoire pour l'identité hybride : les utilisateurs et les groupes sont synchronisés avec Azure AD</span><span class="sxs-lookup"><span data-stu-id="8a7f1-167">Required for hybrid identity: Users and groups are synchronized with Azure AD</span></span>

<span data-ttu-id="8a7f1-168">Si vous disposez déjà des services de domaine Active Directory (AD DS) locaux, vous avez utilisé Azure AD Connect pour synchroniser les comptes et groupes d'utilisateurs depuis vos services AD DS locaux vers votre client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-168">If you have an existing on-premises Active Directory Domain Services (AD DS), you have used Azure AD Connect to synchronize user accounts and groups from your on-premises AD DS to your Azure AD tenant.</span></span>

<span data-ttu-id="8a7f1-169">Avec la synchronisation d’annuaires, vos utilisateurs peuvent se connecter à Office 365 et à d’autres services de cloud computing Microsoft à l’aide des mêmes informations d’identification qu’ils utilisent pour se connecter à leurs ordinateurs et accéder aux ressources locales.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-169">With directory synchronization, your users can sign in to Office 365 and other Microsoft cloud services using the same credentials that they use to sign in to their computers and access on-premises resources.</span></span>

<span data-ttu-id="8a7f1-170">Si nécessaire, l’[Étape 4](identity-add-user-accounts.md#identity-sync) peut vous aider à respecter cette exigence.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-170">If needed, [Step 4](identity-add-user-accounts.md#identity-sync) can help you meet this requirement.</span></span>

<span data-ttu-id="8a7f1-171">Si vous ignorez cette exigence, vous aurez deux ensembles de groupes et comptes d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="8a7f1-171">If you skip this requirement, you’ll have two sets of user accounts and groups:</span></span>

- <span data-ttu-id="8a7f1-172">Groupes et comptes d’utilisateur qui existent dans vos services AD DS</span><span class="sxs-lookup"><span data-stu-id="8a7f1-172">User accounts and groups that exist in your on-premises AD DS</span></span>
- <span data-ttu-id="8a7f1-173">Groupes et comptes d’utilisateur qui existent dans votre client Azure AD</span><span class="sxs-lookup"><span data-stu-id="8a7f1-173">User accounts and groups that exist in your Azure AD tenant</span></span>

<span data-ttu-id="8a7f1-p106">Dans cet état, les deux ensembles de groupes et comptes d’utilisateur doivent être gérés manuellement par les administrateurs informatiques et les utilisateurs. Cela entraînera inévitablement des groupes, leurs mots de passe et comptes non synchronisés.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-p106">In this state, the two sets of user accounts and groups must be manually maintained by both IT administrators and users. This will inevitably lead to unsynchronized accounts, their passwords, and groups.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="8a7f1-176">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="8a7f1-176">How to test</span></span>
<span data-ttu-id="8a7f1-177">Pour vérifier que l’authentification avec les informations d’identification locales fonctionne correctement, connectez-vous au portail Office avec vos informations d’identification locales.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-177">To verify that authentication with on-premises credentials works correctly, sign in to the Office portal with your on-premises credentials.</span></span>

<span data-ttu-id="8a7f1-178">Pour vérifier que la synchronisation d’annuaires fonctionne correctement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8a7f1-178">To verify that directory synchronization is working correctly, do the following:</span></span>

1.  <span data-ttu-id="8a7f1-179">Créez un groupe de test dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-179">Create a new test group in AD DS.</span></span>
2.  <span data-ttu-id="8a7f1-180">Attendez l’heure de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-180">Wait for the synchronization time.</span></span>
3.  <span data-ttu-id="8a7f1-181">Vérifiez votre client Azure AD pour vous assurer que le nouveau nom du groupe de test apparaît.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-181">Check your Azure AD tenant to verify that the new test group name appears.</span></span>

<a name="crit-identity-sync-health"></a>
## <a name="optional-directory-synchronization-is-monitored"></a><span data-ttu-id="8a7f1-182">Facultatif : la synchronisation d’annuaires est surveillée</span><span class="sxs-lookup"><span data-stu-id="8a7f1-182">Optional: Directory synchronization is monitored</span></span>

<span data-ttu-id="8a7f1-183">Vous avez utilisé [Utilisation d’Azure AD Connect Health pour la synchronisation](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) (pour la synchronisation de mot de passe) ou [Utilisation d’Azure AD Connect Health avec AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) (pour l’authentification fédérée) et avez déployé Azure AD Connect Health, ce qui implique :</span><span class="sxs-lookup"><span data-stu-id="8a7f1-183">You've used [Azure AD Connect Health with sync](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) (for password synchronization) or [Using Azure AD Connect Health with AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) (for federated authentication) and have deployed Azure AD Connect Health, which involves:</span></span>

- <span data-ttu-id="8a7f1-184">L’installation de l’agent Azure AD Connect Health sur chacun de vos serveurs d’identités local.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-184">Installing the Azure AD Connect Health agent on each of your on-premises identity servers.</span></span>
- <span data-ttu-id="8a7f1-185">L’utilisation du portail Azure AD Connect Health pour surveiller l’état de synchronisation en cours.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-185">Using the Azure AD Connect Health portal to monitor the state of the ongoing synchronization.</span></span>

<span data-ttu-id="8a7f1-186">Si vous ignorez cette option, vous pouvez évaluer plus précisément l’état de votre infrastructure d’identités basée sur le cloud.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-186">If you skip this option, you can more accurately assess the state of your cloud-based identity infrastructure.</span></span>

<span data-ttu-id="8a7f1-187">Si nécessaire, l’[Étape 4](identity-add-user-accounts.md#identity-sync-health) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-187">If needed, [Step 4](identity-add-user-accounts.md#identity-sync-health) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="8a7f1-188">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="8a7f1-188">How to test</span></span>
<span data-ttu-id="8a7f1-189">Le portail Azure AD Connect Health affiche l’état actuel et correct de vos contrôleurs de domaine locaux, ainsi que la synchronisation en cours.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-189">The Azure AD Connect Health portal shows the current and correct state of your on-premises domain controllers and the ongoing synchronization.</span></span>


<a name="crit-identity-pw-writeback"></a>
## <a name="optional-password-writeback-is-enabled-for-your-users"></a><span data-ttu-id="8a7f1-190">Facultatif : l’écriture différée du mot de passe est activée pour vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8a7f1-190">Optional: Password writeback is enabled for your users</span></span>

<span data-ttu-id="8a7f1-191">Vous avez déjà consulté les instructions de la rubrique relative à la [réinitialisation du mot de passe libre-service d’Azure AD (SSPR) avec l’écriture différée du mot de passe](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) pour activer l’écriture différée du mot de passe pour le client Azure AD de votre abonnement Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-191">You've used the instructions in [Azure AD SSPR with password writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) to enable password writeback for the Azure AD tenant of your Microsoft 365 Enterprise subscription.</span></span>

<span data-ttu-id="8a7f1-192">Si vous ignorez cette option, les utilisateurs qui ne sont pas connectés à votre réseau local doivent réinitialiser ou déverrouiller leurs mot de passe AD DS en faisant appel à un administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-192">If you skip this option, users who aren’t connected to your on-premises network must reset or unlock their AD DS passwords through an IT administrator.</span></span>

<span data-ttu-id="8a7f1-193">Si nécessaire, l’[Étape 4](identity-add-user-accounts.md#identity-pw-writeback) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-193">If needed, [Step 4](identity-add-user-accounts.md#identity-pw-writeback) can help you with this option.</span></span>

>[!Note]
><span data-ttu-id="8a7f1-194">L’écriture différée du mot de passe est requise pour exploiter pleinement les fonctionnalités d’Azure AD Identity Protection, comme l’obligation pour les utilisateurs de modifier leurs mots de passe locaux lorsque Azure AD a détecté un risque élevé de compromission de compte.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-194">Password writeback is required to fully utilize Azure AD Identity Protection features, such as requiring users to change their on-premises passwords when Azure AD has detected a high risk of account compromise.</span></span>
>

### <a name="how-to-test"></a><span data-ttu-id="8a7f1-195">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="8a7f1-195">How to test</span></span>

<span data-ttu-id="8a7f1-196">Vous testez l’écriture différée de votre mot de passe en changeant votre mot de passe Office 365.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-196">You test password writeback by changing your password in Office 365.</span></span> <span data-ttu-id="8a7f1-197">Vous devriez pouvoir utiliser votre compte et le nouveau mot de passe pour accéder aux ressources AD DS locales.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-197">You should be able to use your account and new password to access on-premises AD DS resources.</span></span>

1. <span data-ttu-id="8a7f1-198">Créez un compte d’utilisateur test dans votre version locale AD DS, autorisez la synchronisation d’annuaires, puis accordez-lui une licence Microsoft 365 Entreprise dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-198">Create a test user account in your on-premises AD DS, allow directory synchronization to occur, and then grant it a Microsoft 365 Enterprise license in the Microsoft 365 admin center.</span></span>
2. <span data-ttu-id="8a7f1-199">Sur un ordinateur distant qui est relié à votre domaine Server AD DS local, connectez-vous à l’ordinateur et au portail Office à l’aide des informations d’identification du compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-199">From a remote computer that is joined to your on-premises AD DS domain, sign in to the computer and the Office portal using the credentials of the test user account.</span></span>
3. <span data-ttu-id="8a7f1-200">Sélectionnez **Paramètres > Paramètres Office 365 > Mot de passe > Changer le mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-200">Select **Settings > Office 365 settings > Password > Change password**.</span></span>
4. <span data-ttu-id="8a7f1-201">Tapez le mot de passe actuel, tapez un nouveau mot de passe, puis confirmez-le.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-201">Type the current password, type a new password, and then confirm it.</span></span>
5. <span data-ttu-id="8a7f1-202">Déconnectez-vous du portail Office et de l’ordinateur distant, puis connectez-vous à l’ordinateur à l’aide du compte d’utilisateur de test et son nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-202">Sign out of the Office portal and the remote computer and then sign in to the computer using the test user account and its new password.</span></span> <span data-ttu-id="8a7f1-203">Cela prouve que vous avez été en mesure de modifier le mot de passe d’une version locale de compte d’utilisateur AD DS à l’aide du client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-203">This proves that you were able to change the password of an on-premises AD DS user account using the Azure AD tenant.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="8a7f1-204">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="8a7f1-204">How to test</span></span>

<span data-ttu-id="8a7f1-205">Connectez-vous au portail Office 365 avec le nom de votre compte d’utilisateur et l’authentification multifacteur Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-205">Sign in to the Office 365 portal with your user account name and Azure Multi-Factor Authentication.</span></span> <span data-ttu-id="8a7f1-206">Vous devez voir vos éléments de marque personnalisés dans la page de connexion.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-206">You should see your custom branding elements on the sign-in page.</span></span>


<a name="crit-identity-self-service-groups"></a>
## <a name="optional-self-service-group-management-is-enabled-for-specific-azure-ad-security-and-office-365-groups"></a><span data-ttu-id="8a7f1-207">Facultatif : la gestion des groupes en libre-service est activée pour des groupes Office 365 et de sécurité Azure AD spécifiques</span><span class="sxs-lookup"><span data-stu-id="8a7f1-207">Optional: Self-service group management is enabled for specific Azure AD security and Office 365 groups</span></span>

<span data-ttu-id="8a7f1-208">Vous avez déterminé les groupes qui sont appropriés pour la gestion en libre service, décrit à leurs propriétaires les responsabilités et le workflow de gestion des groupes et [configuré la gestion en libre-service dans Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management) pour ces groupes.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-208">You've determined which groups are appropriate for self-service management, instructed their owners on group management workflow and responsibilities, and [set up self-service management in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management) for those groups.</span></span>

<span data-ttu-id="8a7f1-209">Si vous ignorez cette option, toutes les tâches de gestion des groupes Azure AD doivent être effectuées par des administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-209">If you skip this option, all Azure AD group management tasks must be done by IT administrators.</span></span>

<span data-ttu-id="8a7f1-210">Si nécessaire, l’[Étape 5](identity-use-group-management.md#identity-self-service-groups) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-210">If needed, [Step 5](identity-use-group-management.md#identity-self-service-groups) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="8a7f1-211">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="8a7f1-211">How to test</span></span>
1.  <span data-ttu-id="8a7f1-212">Créez un compte d’utilisateur test dans Azure AD avec le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-212">Create a test user account in Azure AD with the Azure portal.</span></span>
2.  <span data-ttu-id="8a7f1-213">Connectez-vous comme avec le compte d’utilisateur test et créez un groupe de sécurité Azure AD test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-213">Sign-in as with the test user account and create a test Azure AD security group.</span></span>
3.  <span data-ttu-id="8a7f1-214">Déconnectez-vous, puis connectez-vous avec votre compte Administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-214">Sign out and then sign-in with your IT administrator account.</span></span>
4.  <span data-ttu-id="8a7f1-215">Configurez le groupe de sécurité test pour la gestion en libre service pour le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-215">Configure the test security group for self-service management for the test user account.</span></span>
5.  <span data-ttu-id="8a7f1-216">Déconnectez-vous, puis connectez-vous avec votre compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-216">Sign out and then sign-in with your test user account.</span></span>
6.  <span data-ttu-id="8a7f1-217">Utilisez le portail Azure pour ajouter des membres au groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-217">Use the Azure portal to add members to the test security group.</span></span>
7.  <span data-ttu-id="8a7f1-218">Supprimez le groupe de sécurité test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-218">Delete the test security group and the test user account.</span></span>

<a name="crit-identity-dyn-groups"></a>
## <a name="optional-dynamic-group-membership-settings-automatically-add-user-accounts-to-groups-based-on-user-account-attributes"></a><span data-ttu-id="8a7f1-219">Facultatif : les paramètres d’appartenance à un groupe dynamique ajoutent automatiquement des comptes d’utilisateur à des groupes en fonction des attributs de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="8a7f1-219">Optional: Dynamic group membership settings automatically add user accounts to groups based on user account attributes</span></span>

<span data-ttu-id="8a7f1-220">Vous avez déterminé l’ensemble des groupes dynamiques Azure AD et utilisé les instructions décrites dans la rubrique relative à l’[appartenance à un groupe dynamique en fonction des attributs dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal) pour créer les groupes et les règles qui déterminent l’ensemble des attributs de compte d’utilisateur et des valeurs pour l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-220">You've determined the set of Azure AD dynamic groups and used the instructions in [Attribute-based dynamic group membership in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal) to create the groups and the rules that determine the set of user account attributes and values for group membership.</span></span>

<span data-ttu-id="8a7f1-p110">Si vous ignorez cette option, l’appartenance à un groupe doit être effectuée manuellement lorsque de nouveaux comptes sont ajoutés ou que les attributs de compte d’utilisateur changent au fil du temps. Par exemple, si une personne est mutée du service des ventes au service de comptabilité, vous devez :</span><span class="sxs-lookup"><span data-stu-id="8a7f1-p110">If you skip this option, group membership must be done manually as new accounts are added or as user account attributes change over time. For example, if someone moves from the Sales department to the Accounting department, you must:</span></span>

- <span data-ttu-id="8a7f1-223">mettre à jour la valeur de l’attribut Service pour ce compte d’utilisateur ;</span><span class="sxs-lookup"><span data-stu-id="8a7f1-223">Update the value of the Department attribute for that user account.</span></span>
- <span data-ttu-id="8a7f1-224">le supprimer manuellement du groupe Ventes ;</span><span class="sxs-lookup"><span data-stu-id="8a7f1-224">Manually remove them from the Sales group.</span></span>
- <span data-ttu-id="8a7f1-225">l’ajouter manuellement au groupe Comptabilité.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-225">Manually add them to the Accounting group.</span></span>

<span data-ttu-id="8a7f1-226">Si les groupes Ventes et Comptabilité sont dynamiques, vous devez uniquement modifier la valeur Service du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-226">If the Sales and Accounting groups were dynamic, you would only have to change the user account’s Department value.</span></span>

<span data-ttu-id="8a7f1-227">Si nécessaire, l’[Étape 5](identity-use-group-management.md#identity-dyn-groups) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-227">If needed, [Step 5](identity-use-group-management.md#identity-dyn-groups) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="8a7f1-228">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="8a7f1-228">How to test</span></span>

1. <span data-ttu-id="8a7f1-229">Créez un groupe dynamique test dans Azure AD avec le portail Azure et configurez une règle pour que Service soit égal à « test1 ».</span><span class="sxs-lookup"><span data-stu-id="8a7f1-229">Create a test dynamic group in Azure AD with the Azure portal and configure a rule for the Department equals “test1”.</span></span>
2. <span data-ttu-id="8a7f1-230">Créez un compte d’utilisateur test dans Azure AD et définissez la propriété Service sur « test1 ».</span><span class="sxs-lookup"><span data-stu-id="8a7f1-230">Create a test user account in Azure AD and set the Department property to “test1”.</span></span>
3. <span data-ttu-id="8a7f1-231">Examinez les propriétés du compte d’utilisateur pour vous assurer qu’il a été défini comme membre du groupe dynamique test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-231">Examine the properties of the user account to ensure that it was made a member of the test dynamic group.</span></span>
4. <span data-ttu-id="8a7f1-232">Modifiez la valeur de la propriété Service pour le compte d’utilisateur test et définissez-la sur « test2 ».</span><span class="sxs-lookup"><span data-stu-id="8a7f1-232">Change the value of the Department property for the test user account to “test2”.</span></span>
5. <span data-ttu-id="8a7f1-233">Examinez les propriétés du compte d’utilisateur pour vous assurer qu’il n’est plus membre du groupe dynamique test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-233">Examine the properties of the user account to ensure that it is no longer a member of the test dynamic group.</span></span>
6. <span data-ttu-id="8a7f1-234">Supprimez le groupe dynamique test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-234">Delete the test dynamic group and the test user account.</span></span>

<a name="crit-identity-group-license"></a>
## <a name="optional-group-based-licensing-to-automatically-assign-and-remove-licenses-to-user-accounts-based-on-group-membership"></a><span data-ttu-id="8a7f1-235">Facultatif : gestion des licences par groupes pour attribuer des licences aux comptes d’utilisateur et les supprimer automatiquement en fonction de l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="8a7f1-235">Optional: Group-based licensing to automatically assign and remove licenses to user accounts based on group membership</span></span>

<span data-ttu-id="8a7f1-236">Vous [avez activé l'attribution de licences par groupe](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal) pour les groupes de sécurité Azure AD appropriés afin que des licences pour Microsoft 365 Entreprise soient automatiquement attribuées ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-236">You [enabled group-based licensing](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal) for the appropriate Azure AD security groups so that your Microsoft 365 Enterprise licenses are automatically assigned or unassigned.</span></span>

<span data-ttu-id="8a7f1-237">Si vous ignorez cette option, vous devez effectuer les opérations suivantes manuellement :</span><span class="sxs-lookup"><span data-stu-id="8a7f1-237">If you skip this option, you must manually:</span></span>

- <span data-ttu-id="8a7f1-238">Attribuer des licences aux nouveaux utilisateurs auxquels vous avez l'intention d'accéder.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-238">Assign licenses to new users whom you intend to have access.</span></span>
- <span data-ttu-id="8a7f1-239">Supprimer les licences des utilisateurs qui ne font plus partie de votre organisation ou qui n'y ont pas accès.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-239">Unassign licenses from users who are no longer with your organization or do not have access.</span></span>

<span data-ttu-id="8a7f1-240">Si nécessaire, l’[Étape 5](identity-use-group-management.md#identity-group-license) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-240">If needed, [Step 5](identity-use-group-management.md#identity-group-license) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="8a7f1-241">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="8a7f1-241">How to test</span></span>

1. <span data-ttu-id="8a7f1-242">Créez un groupe de sécurité test dans Azure AD à l’aide du portail Azure et configurez l’attribution de licences par groupes pour attribuer des licences Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-242">Create a test security group in Azure AD with the Azure portal and configure group-based licensing to assign Microsoft 365 Enterprise license.</span></span>
2. <span data-ttu-id="8a7f1-243">Créez un compte d’utilisateur test dans Azure AD et ajoutez-le au groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-243">Create a test user account in Azure AD and add it to the test security group.</span></span>
3. <span data-ttu-id="8a7f1-244">Examinez les propriétés du compte d’utilisateur dans le Centre d’administration Microsoft 365 pour vous assurer que les licences Microsoft 365 Entreprise lui ont été attribuées.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-244">Examine the properties of the user account in the Microsoft 365 admin center to ensure that it was assigned the Microsoft 365 Enterprise license.</span></span>
4. <span data-ttu-id="8a7f1-245">Supprimez le compte d’utilisateur test du groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-245">Remove the test user account from the test security group.</span></span>
5. <span data-ttu-id="8a7f1-246">Examinez les propriétés du compte d’utilisateur pour vous assurer que les licences Microsoft 365 Entreprise ne lui sont plus attribuées.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-246">Examine the properties of the user account to ensure that it no longer has the Microsoft 365 Enterprise license assigned.</span></span>
6. <span data-ttu-id="8a7f1-247">Supprimez le groupe de sécurité test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-247">Delete the test security group and the test user account.</span></span>


<a name="crit-identity-access-reviews"></a>
## <a name="optional-access-reviews-configured-and-being-used-to-monitor-access"></a><span data-ttu-id="8a7f1-248">Facultatif : révisions d'accès configurées et utilisées pour contrôler l'accès</span><span class="sxs-lookup"><span data-stu-id="8a7f1-248">Optional: Access reviews configured and being used to monitor access</span></span>

<span data-ttu-id="8a7f1-249">Vous avez utilisé ces articles pour configurer différents types de révisions d’accès afin de contrôler les appartenances aux groupes, l’accès aux applications d’entreprise et les attributions de rôle :</span><span class="sxs-lookup"><span data-stu-id="8a7f1-249">You have used these articles to configure different types of access reviews to monitor group memberships, access to enterprise applications, and role assignments:</span></span>

- [<span data-ttu-id="8a7f1-250">Groupes et applications</span><span class="sxs-lookup"><span data-stu-id="8a7f1-250">Groups and apps</span></span>](https://docs.microsoft.com/azure/active-directory/governance/create-access-review)
- [<span data-ttu-id="8a7f1-251">Rôles Azure AD</span><span class="sxs-lookup"><span data-stu-id="8a7f1-251">Azure AD roles</span></span>](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-how-to-start-security-review?toc=%2fazure%2factive-directory%2fgovernance%2ftoc.json)
- [<span data-ttu-id="8a7f1-252">Rôles de ressources Azure</span><span class="sxs-lookup"><span data-stu-id="8a7f1-252">Azure resource roles</span></span>](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-start-access-review?toc=%2fazure%2factive-directory%2fgovernance%2ftoc.json)

<span data-ttu-id="8a7f1-253">Si nécessaire, l’[Étape 6](identity-configure-identity-governance.md#identity-access-reviews) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-253">If needed, [Step 6](identity-configure-identity-governance.md#identity-access-reviews) can help you with this option.</span></span>


## <a name="results-and-next-steps"></a><span data-ttu-id="8a7f1-254">Résultats et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8a7f1-254">Results and next steps</span></span>

<span data-ttu-id="8a7f1-255">Votre infrastructure d’identité dans le cloud de Microsoft 365 utilise l’authentification forte, comptes administrateur protégés et l’accès et gestion utilisateur simplifiés.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-255">Your identity infrastructure in the Microsoft 365 cloud uses strong authentication, protected administrator accounts, and simplified user access and management.</span></span>

|||
|:-------|:-----|
|![Phase 3 : Windows 10 Entreprise](../media/deploy-foundation-infrastructure/win10enterprise_icon-small.png)| <span data-ttu-id="8a7f1-257">Si vous suivez les phases suivantes dans le processus de déploiement de bout en bout pour Microsoft 365 Entreprise, la suivante est la [Windows 10 Entreprise](windows10-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="8a7f1-257">If you're following the phases for the end-to-end deployment of Microsoft 365 Enterprise, your next phase is [Windows 10 Enterprise](windows10-infrastructure.md).</span></span> |

