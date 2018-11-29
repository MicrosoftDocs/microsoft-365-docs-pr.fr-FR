---
title: 'Phase 2 : Critères de sortie de l’infrastructure d’identités'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Assurez-vous que votre configuration répond aux critères de Microsoft 365 Entreprise pour l’infrastructure et les services d’identités.
ms.openlocfilehash: 49ba7801b740b2a1cfd77955517646ee80174712
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867443"
---
# <a name="phase-2-identity-infrastructure-exit-criteria"></a><span data-ttu-id="43ade-103">Phase 2 : Critères de sortie de l’infrastructure d’identités</span><span class="sxs-lookup"><span data-stu-id="43ade-103">Phase 2: Identity infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="43ade-p101">Avant de passer à la Phase 3, assurez-vous que votre infrastructure d’identités remplit ces conditions. Reportez-vous aussi aux [Prérequis](https://docs.microsoft.com/microsoft-365-enterprise/identity-access-policies#prerequisites) pour consulter des recommandations supplémentaires sur l’infrastructure d’identités.</span><span class="sxs-lookup"><span data-stu-id="43ade-p101">Before you move on to Phase 3, make sure that your identity infrastructure meets these conditions. Also see [Prerequisites](https://docs.microsoft.com/microsoft-365-enterprise/identity-access-policies#prerequisites) for additional recommendations on identity infrastructure.</span></span>

<a name="crit-identity-user-groups"></a>
## <a name="required-all-users-groups-and-group-memberships-have-been-created"></a><span data-ttu-id="43ade-106">Obligatoire : tous les utilisateurs, groupes et appartenances aux groupes ont été créés</span><span class="sxs-lookup"><span data-stu-id="43ade-106">Required: All users, groups, and group memberships have been created</span></span>

<span data-ttu-id="43ade-107">Vous avez créé des groupes et des comptes d’utilisateur afin que :</span><span class="sxs-lookup"><span data-stu-id="43ade-107">You've created user accounts and groups so that:</span></span>

- <span data-ttu-id="43ade-108">les employés au sein de votre organisation et les fournisseurs, entrepreneurs et partenaires qui travaillent pour ou avec votre organisation aient un compte d’utilisateur correspondant dans Azure Active Directory (AD) ;</span><span class="sxs-lookup"><span data-stu-id="43ade-108">Employees in your organization and the vendors, contractors, and partners that work for or with your organization have a corresponding user account in Azure Active Directory (AD).</span></span>
- <span data-ttu-id="43ade-109">les groupes Azure AD et leurs membres contiennent des comptes d’utilisateur et d’autres groupes à des fins diverses (attribution de paramètres de sécurité pour les services de cloud computing Microsoft, attribution automatique de licences et autres utilisations).</span><span class="sxs-lookup"><span data-stu-id="43ade-109">Azure AD groups and their members contain user accounts and other groups for various purposes, such as the provisioning of security settings for Microsoft cloud services, automatic licensing, and other uses.</span></span>

<span data-ttu-id="43ade-110">Si nécessaire, l’[Étape 1](identity-plan-users-groups.md) peut vous aider à respecter cette exigence.</span><span class="sxs-lookup"><span data-stu-id="43ade-110">If needed, [Step 1](identity-plan-users-groups.md) can help you meet this requirement.</span></span>

<a name="crit-identity-sync"></a>
## <a name="required-users-and-groups-are-synchronized-with-azure-ad"></a><span data-ttu-id="43ade-111">Obligatoire : les utilisateurs et les groupes sont synchronisés avec Azure AD</span><span class="sxs-lookup"><span data-stu-id="43ade-111">Required: Users and groups are synchronized with Azure AD</span></span>

<span data-ttu-id="43ade-112">Si vous avez un fournisseur d’identité local existant, comme Windows Server Active Directory (AD), vous avez utilisé Azure AD Connect pour synchroniser les comptes d’utilisateur et les groupes de votre fournisseur d’identité local avec votre client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="43ade-112">If you have an existing on-premises identity provider, such as Windows Server Active Directory (AD), you have used Azure AD Connect to synchronize user accounts and groups from your on-premises identity provider to your Azure AD tenant.</span></span>

<span data-ttu-id="43ade-113">Avec la synchronisation d’annuaires, vos utilisateurs peuvent se connecter à Office 365 et à d’autres services de cloud computing Microsoft à l’aide des mêmes informations d’identification qu’ils utilisent pour se connecter à leurs ordinateurs et accéder aux ressources locales.</span><span class="sxs-lookup"><span data-stu-id="43ade-113">With directory synchronization, your users can sign in to Office 365 and other Microsoft cloud services using the same credentials that they use to sign in to their computers and access on-premises resources.</span></span>

<span data-ttu-id="43ade-114">Si nécessaire, l’[Étape 7](identity-azure-ad-connect.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="43ade-114">If needed, [Step 7](identity-azure-ad-connect.md) can help you meet this requirement.</span></span>

<span data-ttu-id="43ade-115">Si vous ignorez cette exigence, vous aurez deux ensembles de groupes et comptes d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="43ade-115">If you skip this requirement, you’ll have two sets of user accounts and groups:</span></span>

- <span data-ttu-id="43ade-116">Groupes et comptes d’utilisateur qui existent dans votre fournisseur d’identité local</span><span class="sxs-lookup"><span data-stu-id="43ade-116">User accounts and groups that exist in your on-premises identity provider</span></span>
- <span data-ttu-id="43ade-117">Groupes et comptes d’utilisateur qui existent dans votre client Azure AD</span><span class="sxs-lookup"><span data-stu-id="43ade-117">User accounts and groups that exist in your Azure AD tenant</span></span>

<span data-ttu-id="43ade-p102">Dans cet état, les deux ensembles de groupes et comptes d’utilisateur doivent être gérés manuellement par les administrateurs informatiques et les utilisateurs. Cela entraînera inévitablement des groupes, leurs mots de passe et comptes non synchronisés.</span><span class="sxs-lookup"><span data-stu-id="43ade-p102">In this state, the two sets of user accounts and groups must be manually maintained by both IT administrators and users. This will inevitably lead to unsynchronized accounts, their passwords, and groups.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="43ade-120">Comment effectuer les tests</span><span class="sxs-lookup"><span data-stu-id="43ade-120">How to test</span></span>
<span data-ttu-id="43ade-121">Pour vérifier que l’authentification avec les informations d’identification locales fonctionne correctement, connectez-vous au portail d’Office 365 avec vos informations d’identification locales.</span><span class="sxs-lookup"><span data-stu-id="43ade-121">To verify that authentication with on-premises credentials works correctly, sign in to the Office 365 portal with your on-premises credentials.</span></span>

<span data-ttu-id="43ade-122">Pour vérifier que la synchronisation d’annuaires fonctionne correctement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="43ade-122">To verify that directory synchronization is working correctly, do the following:</span></span>

1.  <span data-ttu-id="43ade-123">Créez un groupe de test dans Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="43ade-123">Create a new test group in Windows Server AD.</span></span>
2.  <span data-ttu-id="43ade-124">Attendez l’heure de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="43ade-124">Wait for the synchronization time.</span></span>
3.  <span data-ttu-id="43ade-125">Vérifiez votre client Azure AD pour vous assurer que le nouveau nom du groupe de test apparaît.</span><span class="sxs-lookup"><span data-stu-id="43ade-125">Check your Azure AD tenant to verify that the new test group name appears.</span></span>

<a name="crit-identity-global-admin"></a>
## <a name="required-your-global-administrator-accounts-are-protected"></a><span data-ttu-id="43ade-126">Obligatoire : vos comptes d’administrateur général sont protégés</span><span class="sxs-lookup"><span data-stu-id="43ade-126">Required: Your global administrator accounts are protected</span></span> 

<span data-ttu-id="43ade-127">Vous avez [protégé vos comptes d’administrateur général Office 365](https://support.office.com/article/Protect-your-Office-365-global-administrator-accounts-6b4ded77-ac8d-42ed-8606-c014fd947560) afin d’éviter de compromettre les informations d’identification pouvant entraîner des violations d’un abonnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="43ade-127">You've [protected your Office 365 global administrator accounts](https://support.office.com/article/Protect-your-Office-365-global-administrator-accounts-6b4ded77-ac8d-42ed-8606-c014fd947560) to avoid compromising credentials that can lead to breaches of an Office 365 subscription.</span></span>

<span data-ttu-id="43ade-128">Si vous ignorez cette exigence, vos comptes d’administrateur général peuvent être attaqués et compromis, autorisant un utilisateur à accéder à vos données à l’échelle du système à des fins de collecte, destruction ou prise en otage des données.</span><span class="sxs-lookup"><span data-stu-id="43ade-128">If you skip this requirement, your global administrator accounts can be susceptible to attack and compromise, allowing an attacker to gain system-wide access to your data for harvesting, destruction, or ransom.</span></span>

<span data-ttu-id="43ade-129">Si nécessaire, l’[Étape 2](identity-designate-protect-admin-accounts.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="43ade-129">If needed, [Step 2](identity-designate-protect-admin-accounts.md) can help you meet this requirement.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="43ade-130">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="43ade-130">How to test</span></span>

<span data-ttu-id="43ade-131">Suivez ces étapes pour vérifier que vous avez protégé vos comptes d’administrateur général :</span><span class="sxs-lookup"><span data-stu-id="43ade-131">Use these steps to verify that you've protected your global administrator accounts:</span></span>

1. <span data-ttu-id="43ade-p103">Exécutez la commande Azure AD V2 suivante à l’invite de commandes PowerShell. Vous devriez voir uniquement la liste des comptes administrateur général dédiés.</span><span class="sxs-lookup"><span data-stu-id="43ade-p103">Run the following Azure AD V2 command at the PowerShell command prompt. You should see only the list of dedicated global administrator accounts.</span></span>
   ```
   Get-AzureADDirectoryRole | where { $_.DisplayName -eq "Company Administrator" } | Get-AzureADDirectoryRoleMember | Ft DisplayName
   ```
2. <span data-ttu-id="43ade-p104">Connectez-vous à Office 365 à l’aide de chacun des comptes de l’étape 1. Chaque connexion doit exiger l’authentification multifacteur et la forme la plus forte d’authentification secondaire disponible dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="43ade-p104">Sign in to Office 365 using each of the accounts from step 1. Each sign in must require multi-factor authentication and the strongest form of secondary authentication available in your organization.</span></span>

> [!Note]
> <span data-ttu-id="43ade-136">Reportez-vous à [Se connecter à Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) pour obtenir des instructions sur l’installation du module Azure AD V2 PowerShell et la connexion à Office 365.</span><span class="sxs-lookup"><span data-stu-id="43ade-136">See [Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) for instructions on installing the Azure AD V2 PowerShell module and signing in to Office 365.</span></span>

<a name="crit-identity-custom-sign-in"></a>
## <a name="optional-the-office-365-sign-in-screen-is-personalized-for-your-organization"></a><span data-ttu-id="43ade-137">Facultatif : l’écran de connexion Office 365 est personnalisé pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="43ade-137">Optional: The Office 365 sign-in screen is personalized for your organization</span></span>

<span data-ttu-id="43ade-138">Vous avez utilisé [Ajouter la marque de votre organisation à votre page de connexion et aux pages du Panneau d’accès](http://aka.ms/aadpaddbranding) pour ajouter la marque de votre organisation à la page de connexion Office 365.</span><span class="sxs-lookup"><span data-stu-id="43ade-138">You have used [Add company branding to your sign-in and Access Panel pages](http://aka.ms/aadpaddbranding) to add your organization’s branding to the Office 365 sign-in page.</span></span>

<span data-ttu-id="43ade-139">Si vous ignorez cette option, vos utilisateurs verront un écran de connexion Office 365 générique et peuvent ne pas être certains de se connecter au site de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="43ade-139">If you skip this option, your users will see a generic Office 365 sign-in screen and might not be confident that they’re signing into your organization’s site.</span></span>

<span data-ttu-id="43ade-140">Si nécessaire, l’[Étape 11](identity-customize-office-365-sign-in.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-140">If needed, [Step 11](identity-customize-office-365-sign-in.md) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="43ade-141">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="43ade-141">How to test</span></span>

<span data-ttu-id="43ade-p105">Connectez-vous au portail Office 365 avec votre nom de compte d’utilisateur et l’authentification multifacteur. Vos éléments de marque personnalisés apparaissent sur la page de connexion.</span><span class="sxs-lookup"><span data-stu-id="43ade-p105">Sign in to the Office 365 portal with your user account name and multi-factor authentication. You should see your custom branding elements on the sign-in page.</span></span>

<a name="crit-identity-mfa"></a>
## <a name="optional-multi-factor-authentication-is-enabled-for-your-users"></a><span data-ttu-id="43ade-144">Facultatif : l’authentification multifacteur est activée pour vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="43ade-144">Optional: Multi-factor authentication is enabled for your users</span></span>

<span data-ttu-id="43ade-145">Vous avez utilisé [Planifier l’authentification multifacteur pour les déploiements Office 365](https://support.office.com/article/Plan-for-multifactor-authentication-for-Office-365-Deployments-043807b2-21db-4d5c-b430-c8a6dee0e6ba) et [Configurer l’authentification multifacteur pour les utilisateurs d’Office 365](https://support.office.com/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6) pour activer l’authentification multifacteur (MFA) pour vos comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="43ade-145">You used [Plan for multi-factor authentication for Office 365 Deployments](https://support.office.com/article/Plan-for-multifactor-authentication-for-Office-365-Deployments-043807b2-21db-4d5c-b430-c8a6dee0e6ba) and [Set up multi-factor authentication for Office 365 users](https://support.office.com/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6) to enable multifactor authentication (MFA) for your user accounts.</span></span>

<span data-ttu-id="43ade-p106">Si vous ignorez cette option, vos comptes d’utilisateur sont vulnérables à la compromission des informations d’identification par des cyber-attaquants. Si le mot de passe d’un compte d’utilisateur est compromis, toutes les ressources et les fonctionnalités du compte, telles que les rôles d’administrateur, sont disponibles pour l’utilisateur malveillant. Ainsi, ce dernier peut copier, détruire ou conserver des documents internes et d’autres données contre rançon.</span><span class="sxs-lookup"><span data-stu-id="43ade-p106">If you skip this option, your user accounts are vulnerable to credential compromise by cyber attackers. If a user account’s password is compromised, all the resources and capabilities of the account, such as administrator roles, are available to the attacker. This allows the attacker to copy, destroy, or hold for ransom internal documents and other data.</span></span>

<span data-ttu-id="43ade-149">Si nécessaire, l’[Étape 5](identity-multi-factor-authentication.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-149">If needed, [Step 5](identity-multi-factor-authentication.md) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="43ade-150">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="43ade-150">How to test</span></span>

1.  <span data-ttu-id="43ade-151">Créez un compte d’utilisateur test dans le portail Office 365 Admin et attribuez-lui une licence.</span><span class="sxs-lookup"><span data-stu-id="43ade-151">Create a test user account in the Office 365 Admin portal and assign them a license.</span></span> 
2.  <span data-ttu-id="43ade-152">Configurez l’authentification multifacteur pour le compte d’utilisateur test avec la méthode de vérification supplémentaire que vous utilisez pour les comptes d’utilisateur réels, comme l’envoi d’un message sur votre téléphone.</span><span class="sxs-lookup"><span data-stu-id="43ade-152">Configure multi-factor authentication for the test user account with the additional verification method that you are using for actual user accounts, such as sending a message to your phone.</span></span> 
3.  <span data-ttu-id="43ade-153">Connectez-vous au portail Office 365 ou Azure avec le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="43ade-153">Sign in to the Office 365 or Azure portal with the test user account.</span></span>
4.  <span data-ttu-id="43ade-154">Vérifiez que l’authentification multifacteur vous invite à saisir les informations de vérification supplémentaires et que l’authentification s’effectue sans problèmes.</span><span class="sxs-lookup"><span data-stu-id="43ade-154">Verify that MFA prompts you for the additional verification information and results in a successful authentication.</span></span> 
5.  <span data-ttu-id="43ade-155">Supprimez le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="43ade-155">Delete the test user account.</span></span>

<a name="crit-identity-sync-health"></a>
## <a name="optional-directory-synchronization-is-monitored"></a><span data-ttu-id="43ade-156">Facultatif : la synchronisation d’annuaires est surveillée</span><span class="sxs-lookup"><span data-stu-id="43ade-156">Optional: Directory synchronization is monitored</span></span>

<span data-ttu-id="43ade-157">Vous avez utilisé [Utilisation d’Azure AD Connect Health pour la synchronisation](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) (pour la synchronisation de mot de passe) ou [Utilisation d’Azure AD Connect Health avec AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) (pour l’authentification fédérée) et avez déployé Azure AD Connect Health, ce qui implique :</span><span class="sxs-lookup"><span data-stu-id="43ade-157">You've used [Azure AD Connect Health with sync](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) (for password synchronization) or [Using Azure AD Connect Health with AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) (for federated authentication) and have deployed Azure AD Connect Health, which involves:</span></span>

- <span data-ttu-id="43ade-158">L’installation de l’agent Azure AD Connect Health sur chacun de vos serveurs d’identités local.</span><span class="sxs-lookup"><span data-stu-id="43ade-158">Installing the Azure AD Connect Health agent on each of your on-premises identity servers.</span></span>
- <span data-ttu-id="43ade-159">L’utilisation du portail Azure AD Connect Health pour surveiller l’état de synchronisation en cours.</span><span class="sxs-lookup"><span data-stu-id="43ade-159">Using the Azure AD Connect Health portal to monitor the state of the ongoing synchronization.</span></span>

<span data-ttu-id="43ade-160">Si vous ignorez cette option, vous pouvez évaluer plus précisément l’état de votre infrastructure d’identités basée sur le cloud.</span><span class="sxs-lookup"><span data-stu-id="43ade-160">If you skip this option, you can more accurately assess the state of your cloud-based identity infrastructure.</span></span>

<span data-ttu-id="43ade-161">Si nécessaire, l’[Étape 8](identity-azure-ad-connect-health.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-161">If needed, [Step 8](identity-azure-ad-connect-health.md) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="43ade-162">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="43ade-162">How to test</span></span>
<span data-ttu-id="43ade-163">Le portail Azure AD Connect Health affiche l’état actuel et correct de vos serveurs d’identités locaux et la synchronisation en cours.</span><span class="sxs-lookup"><span data-stu-id="43ade-163">The Azure AD Connect Health portal shows the current and correct state of your on-premises identity servers and the ongoing synchronization.</span></span>

<a name="crit-identity-pw-reset"></a>
## <a name="optional-users-can-reset-their-own-passwords"></a><span data-ttu-id="43ade-164">Facultatif : les utilisateurs peuvent réinitialiser leurs mots de passe</span><span class="sxs-lookup"><span data-stu-id="43ade-164">Optional: Users can reset their own passwords</span></span>

<span data-ttu-id="43ade-165">Vous avez utilisé la rubrique relative au [déploiement rapide de la réinitialisation du mot de passe libre-service Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) pour configurer la réinitialisation du mot de passe pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="43ade-165">You've used [Azure AD self-service password reset rapid deployment](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) to configure password reset for your users.</span></span>

<span data-ttu-id="43ade-166">Si vous ne remplissez pas cette condition, les utilisateurs dépendront des administrateurs de compte d’utilisateur pour réinitialiser leurs mots de passe, entraînant une surcharge d’administration informatique supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="43ade-166">If you don’t meet this condition, users will be dependent on user account administrators to reset their passwords, resulting in additional IT administration overhead.</span></span>

<span data-ttu-id="43ade-167">Si nécessaire, l’[Étape 4](identity-password-reset.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-167">If needed, [Step 4](identity-password-reset.md) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="43ade-168">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="43ade-168">How to test</span></span>

1. <span data-ttu-id="43ade-169">Créez un compte d’utilisateur test avec un mot de passe initial.</span><span class="sxs-lookup"><span data-stu-id="43ade-169">Create a test user account with an initial password.</span></span>
2. <span data-ttu-id="43ade-170">Suivez les étapes décrites dans [Autoriser les utilisateurs à réinitialiser leur mot de passe dans Office 365](https://support.office.com/article/Let-users-reset-their-own-passwords-in-Office-365-5bc3f460-13cc-48c0-abd6-b80bae72d04a) pour réinitialiser le mot de passe sur le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="43ade-170">Use the steps in [Let users reset their own passwords in Office 365](https://support.office.com/article/Let-users-reset-their-own-passwords-in-Office-365-5bc3f460-13cc-48c0-abd6-b80bae72d04a) to reset the password on the test user account.</span></span>
3. <span data-ttu-id="43ade-171">Déconnectez-vous, puis connectez-vous au compte d’utilisateur test à l’aide du mot de passe réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="43ade-171">Sign out and then sign in to the test user account using the reset password.</span></span>
4. <span data-ttu-id="43ade-172">Supprimez le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="43ade-172">Delete the test user account.</span></span>

<a name="crit-identity-pw-writeback"></a>
## <a name="optional-password-writeback-is-enabled-for-your-users"></a><span data-ttu-id="43ade-173">Facultatif : l’écriture différée du mot de passe est activée pour vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="43ade-173">Optional: Password writeback is enabled for your users</span></span>

<span data-ttu-id="43ade-174">Vous avez déjà consulté les instructions de la rubrique relative à la [réinitialisation du mot de passe libre-service d’Azure AD (SSPR) avec l’écriture différée du mot de passe](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) pour activer l’écriture différée du mot de passe pour le client Azure AD de votre abonnement Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="43ade-174">You've used the instructions in [Azure AD SSPR with password writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) to enable password writeback for the Azure AD tenant of your Microsoft 365 Enterprise subscription.</span></span>

<span data-ttu-id="43ade-175">Si vous ignorez cette option, les utilisateurs qui ne sont pas connectés à votre réseau local doivent réinitialiser ou déverrouiller leurs mot de passe Windows Server AD en faisant appel à un administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="43ade-175">If you skip this option, users who aren’t connected to your on-premises network must reset or unlock their Windows Server AD passwords through an IT administrator.</span></span>

<span data-ttu-id="43ade-176">Si nécessaire, l’[Étape 9](identity-password-writeback.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-176">If needed, [Step 9](identity-password-writeback.md) can help you with this option.</span></span>

>[!Note]
><span data-ttu-id="43ade-177">L’écriture différée du mot de passe est requise pour exploiter pleinement les fonctionnalités d’Azure AD Identity Protection, comme l’obligation pour les utilisateurs de modifier leurs mots de passe locaux lorsque Azure AD a détecté un risque élevé de compromission de compte.</span><span class="sxs-lookup"><span data-stu-id="43ade-177">Password writeback is required to fully utilize Azure AD Identity Protection features, such as requiring users to change their on-premises passwords when Azure AD has detected a high risk of account compromise.</span></span>
>

### <a name="how-to-test"></a><span data-ttu-id="43ade-178">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="43ade-178">How to test</span></span>

<span data-ttu-id="43ade-p107">Vous testez l’écriture différée du mot de passe en modifiant votre mot de passe dans Office 365. Vous devez pouvoir utiliser votre compte et le nouveau mot de passe pour accéder aux ressources Windows Server AD locales.</span><span class="sxs-lookup"><span data-stu-id="43ade-p107">You test password writeback by changing your password in Office 365. You should be able to use your account and new password to access on-premises Windows Server AD resources.</span></span>

1. <span data-ttu-id="43ade-181">Créez un compte d’utilisateur test dans votre version locale de Windows Server AD, autorisez la synchronisation d’annuaires, puis accordez-lui une licence Office 365 dans le portail d’administration Office 365.</span><span class="sxs-lookup"><span data-stu-id="43ade-181">Create a test user account in your on-premises Windows Server AD, allow directory synchronization to occur, and then grant it an Office 365 license in the Office 365 admin portal.</span></span>
2. <span data-ttu-id="43ade-182">Sur un ordinateur distant qui est relié à votre domaine Windows Server AD local, connectez-vous à l’ordinateur et au portail Office 365 à l’aide des informations d’identification du compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="43ade-182">From a remote computer that is joined to your on-premises Windows Server AD domain, sign in to the computer and the Office 365 portal using the credentials of the test user account.</span></span>
3. <span data-ttu-id="43ade-183">Sélectionnez **Paramètres > Paramètres Office 365 > Mot de passe > Changer le mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="43ade-183">Select **Settings > Office 365 settings > Password > Change password**.</span></span>
4. <span data-ttu-id="43ade-184">Tapez le mot de passe actuel, tapez un nouveau mot de passe, puis confirmez-le.</span><span class="sxs-lookup"><span data-stu-id="43ade-184">Type the current password, type a new password, and then confirm it.</span></span>
5. <span data-ttu-id="43ade-p108">Déconnectez-vous du portail Office 365 et de l’ordinateur distant, puis connectez-vous à l’ordinateur à l’aide du compte d’utilisateur test et de son nouveau mot de passe. Cela prouve que vous avez pu modifier le mot de passe d’un compte d’utilisateur Windows Server AD local à l’aide du client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="43ade-p108">Sign out of the Office 365 portal and the remote computer and then sign in to the computer using the test user account and its new password. This proves that you were able to change the password of an on-premises Windows Server AD user account using the Azure AD tenant.</span></span>

<a name="crit-identity-sso"></a>
## <a name="optional-users-can-sign-in-using-single-sign-on"></a><span data-ttu-id="43ade-187">Facultatif : les utilisateurs peuvent se connecter à l’aide de l’authentification unique</span><span class="sxs-lookup"><span data-stu-id="43ade-187">Optional: Users can sign in using single sign-on</span></span>

<span data-ttu-id="43ade-188">Vous avez activé l’[authentification unique transparente Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start) pour que votre organisation simplifie la manière dont les utilisateurs se connectent aux applications basées sur le cloud, comme Office 365.</span><span class="sxs-lookup"><span data-stu-id="43ade-188">You enabled [Azure AD Connect: Seamless Single Sign-On](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start) for your organization to simplify how users sign in to cloud-based applications, such as Office 365.</span></span>

<span data-ttu-id="43ade-189">Si vous ignorez cette option, vos utilisateurs peuvent être invités à fournir des informations d’identification lorsqu’ils accèdent à d’autres applications qui utilisent Azure AD.</span><span class="sxs-lookup"><span data-stu-id="43ade-189">If you skip this option, your users might be prompted to provide credentials when they access additional applications that use Azure AD.</span></span>

<span data-ttu-id="43ade-190">Si nécessaire, l’[Étape 10](identity-single-sign-on.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-190">If needed, [Step 10](identity-single-sign-on.md) can help you with this option.</span></span>


<a name="crit-identity-group-license"></a>
## <a name="optional-group-based-licensing-to-automatically-assign-and-remove-licenses-to-user-accounts-based-on-group-membership"></a><span data-ttu-id="43ade-191">Facultatif : gestion des licences par groupes pour attribuer des licences aux comptes d’utilisateur et les supprimer automatiquement en fonction de l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="43ade-191">Optional: Group-based licensing to automatically assign and remove licenses to user accounts based on group membership</span></span>

<span data-ttu-id="43ade-192">Vous [avez activé la gestion des licences par groupes](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal) pour les groupes de sécurité Azure AD appropriés afin que des licences pour Office 365 et EMS soient automatiquement attribuées ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="43ade-192">You [enabled group-based licensing](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal) for the appropriate Azure AD security groups so that licenses for both Office 365 and EMS are automatically assigned or removed.</span></span>

<span data-ttu-id="43ade-193">Si vous ignorez cette option, vous devez effectuer les opérations suivantes manuellement :</span><span class="sxs-lookup"><span data-stu-id="43ade-193">If you skip this option, you must manually:</span></span>

- <span data-ttu-id="43ade-194">Attribuer des licences aux nouveaux utilisateurs qui accèderont à Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="43ade-194">Assign licenses to new users whom you intend to have access to Office 365 and EMS.</span></span>
- <span data-ttu-id="43ade-195">Supprimer les licences des utilisateurs qui ne sont plus avec votre organisation ou n’ont pas accès à Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="43ade-195">Remove licenses from users who are no longer with your organization or do not have access to Office 365 and EMS.</span></span>

<span data-ttu-id="43ade-196">Si nécessaire, l’[Étape 12](identity-group-based-licensing.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-196">If needed, [Step 12](identity-group-based-licensing.md) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="43ade-197">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="43ade-197">How to test</span></span>

1. <span data-ttu-id="43ade-198">Créez un groupe de sécurité test dans Azure AD avec le portail Azure et configurez la gestion des licences par groupes pour attribuer des licences Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="43ade-198">Create a test security group in Azure AD with the Azure portal and configure group-based licensing to assign Office 365 and EMS licenses.</span></span>
2. <span data-ttu-id="43ade-199">Créez un compte d’utilisateur test dans Azure AD et ajoutez-le au groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="43ade-199">Create a test user account in Azure AD and add it to the test security group.</span></span>
3. <span data-ttu-id="43ade-200">Examinez les propriétés du compte d’utilisateur dans le portail d’administration Office 365 pour vous assurer que les licences Office 365 et EMS lui ont été attribuées.</span><span class="sxs-lookup"><span data-stu-id="43ade-200">Examine the properties of the user account in the Office 365 admin portal to ensure that it was assigned the Office 365 and EMS licenses.</span></span>
4. <span data-ttu-id="43ade-201">Supprimez le compte d’utilisateur test du groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="43ade-201">Remove the test user account from the test security group.</span></span>
5. <span data-ttu-id="43ade-202">Examinez les propriétés du compte d’utilisateur pour vous assurer que les licences Office 365 et EMS ne lui sont plus attribuées.</span><span class="sxs-lookup"><span data-stu-id="43ade-202">Examine the properties of the user account to ensure that it no longer has the Office 365 and EMS licenses assigned.</span></span>
6. <span data-ttu-id="43ade-203">Supprimez le groupe de sécurité test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="43ade-203">Delete the test security group and the test user account.</span></span>

<a name="crit-identity-dyn-groups"></a>
## <a name="optional-dynamic-group-membership-settings-automatically-add-user-accounts-to-groups-based-on-user-account-attributes"></a><span data-ttu-id="43ade-204">Facultatif : les paramètres d’appartenance à un groupe dynamique ajoutent automatiquement des comptes d’utilisateur à des groupes en fonction des attributs de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="43ade-204">Optional: Dynamic group membership settings automatically add user accounts to groups based on user account attributes</span></span>

<span data-ttu-id="43ade-205">Vous avez déterminé l’ensemble des groupes dynamiques Azure AD et utilisé les instructions décrites dans la rubrique relative à l’[appartenance à un groupe dynamique en fonction des attributs dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal) pour créer les groupes et les règles qui déterminent l’ensemble des attributs de compte d’utilisateur et des valeurs pour l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="43ade-205">You've determined the set of Azure AD dynamic groups and used the instructions in [Attribute-based dynamic group membership in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal) to create the groups and the rules that determine the set of user account attributes and values for group membership.</span></span>

<span data-ttu-id="43ade-p109">Si vous ignorez cette option, l’appartenance à un groupe doit être effectuée manuellement lorsque de nouveaux comptes sont ajoutés ou que les attributs de compte d’utilisateur changent au fil du temps. Par exemple, si une personne est mutée du service des ventes au service de comptabilité, vous devez :</span><span class="sxs-lookup"><span data-stu-id="43ade-p109">If you skip this option, group membership must be done manually as new accounts are added or as user account attributes change over time. For example, if someone moves from the Sales department to the Accounting department, you must:</span></span>

- <span data-ttu-id="43ade-208">mettre à jour la valeur de l’attribut Service pour ce compte d’utilisateur ;</span><span class="sxs-lookup"><span data-stu-id="43ade-208">Update the value of the Department attribute for that user account.</span></span>
- <span data-ttu-id="43ade-209">le supprimer manuellement du groupe Ventes ;</span><span class="sxs-lookup"><span data-stu-id="43ade-209">Manually remove them from the Sales group.</span></span>
- <span data-ttu-id="43ade-210">l’ajouter manuellement au groupe Comptabilité.</span><span class="sxs-lookup"><span data-stu-id="43ade-210">Manually add them to the Accounting group.</span></span>

<span data-ttu-id="43ade-211">Si les groupes Ventes et Comptabilité sont dynamiques, vous devez uniquement modifier la valeur Service du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="43ade-211">If the Sales and Accounting groups were dynamic, you would only have to change the user account’s Department value.</span></span>

<span data-ttu-id="43ade-212">Si nécessaire, l’[Étape 15](identity-automatic-group-membership.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-212">If needed, [Step 15](identity-automatic-group-membership.md) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="43ade-213">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="43ade-213">How to test</span></span>

1. <span data-ttu-id="43ade-214">Créez un groupe dynamique test dans Azure AD avec le portail Azure et configurez une règle pour que Service soit égal à « test1 ».</span><span class="sxs-lookup"><span data-stu-id="43ade-214">Create a test dynamic group in Azure AD with the Azure portal and configure a rule for the Department equals “test1”.</span></span>
2. <span data-ttu-id="43ade-215">Créez un compte d’utilisateur test dans Azure AD et définissez la propriété Service sur « test1 ».</span><span class="sxs-lookup"><span data-stu-id="43ade-215">Create a test user account in Azure AD and set the Department property to “test1”.</span></span>
3. <span data-ttu-id="43ade-216">Examinez les propriétés du compte d’utilisateur pour vous assurer qu’il a été défini comme membre du groupe dynamique test.</span><span class="sxs-lookup"><span data-stu-id="43ade-216">Examine the properties of the user account to ensure that it was made a member of the test dynamic group.</span></span>
4. <span data-ttu-id="43ade-217">Modifiez la valeur de la propriété Service pour le compte d’utilisateur test et définissez-la sur « test2 ».</span><span class="sxs-lookup"><span data-stu-id="43ade-217">Change the value of the Department property for the test user account to “test2”.</span></span>
5. <span data-ttu-id="43ade-218">Examinez les propriétés du compte d’utilisateur pour vous assurer qu’il n’est plus membre du groupe dynamique test.</span><span class="sxs-lookup"><span data-stu-id="43ade-218">Examine the properties of the user account to ensure that it is no longer a member of the test dynamic group.</span></span>
6. <span data-ttu-id="43ade-219">Supprimez le groupe dynamique test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="43ade-219">Delete the test dynamic group and the test user account.</span></span>

<a name="crit-identity-self-service-groups"></a>
## <a name="optional-self-service-group-management-is-enabled-for-specific-azure-ad-security-and-office-365-groups"></a><span data-ttu-id="43ade-220">Facultatif : la gestion des groupes en libre-service est activée pour des groupes Office 365 et de sécurité Azure AD spécifiques</span><span class="sxs-lookup"><span data-stu-id="43ade-220">Optional: Self-service group management is enabled for specific Azure AD security and Office 365 groups</span></span>

<span data-ttu-id="43ade-221">Vous avez déterminé les groupes qui sont appropriés pour la gestion en libre service, décrit à leurs propriétaires les responsabilités et le workflow de gestion des groupes et [configuré la gestion en libre-service dans Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management) pour ces groupes.</span><span class="sxs-lookup"><span data-stu-id="43ade-221">You've determined which groups are appropriate for self-service management, instructed their owners on group management workflow and responsibilities, and [set up self-service management in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management) for those groups.</span></span>

<span data-ttu-id="43ade-222">Si vous ignorez cette option, toutes les tâches de gestion des groupes Azure AD doivent être effectuées par des administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="43ade-222">If you skip this option, all Azure AD group management tasks must be done by IT administrators.</span></span>

<span data-ttu-id="43ade-223">Si nécessaire, l’[Étape 14](identity-self-service-group-management.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-223">If needed, [Step 14](identity-self-service-group-management.md) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="43ade-224">Comment effectuer les tests</span><span class="sxs-lookup"><span data-stu-id="43ade-224">How to test</span></span>
1.  <span data-ttu-id="43ade-225">Créez un compte d’utilisateur test dans Azure AD avec le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="43ade-225">Create a test user account in Azure AD with the Azure portal.</span></span>
2.  <span data-ttu-id="43ade-226">Connectez-vous comme avec le compte d’utilisateur test et créez un groupe de sécurité Azure AD test.</span><span class="sxs-lookup"><span data-stu-id="43ade-226">Sign-in as with the test user account and create a test Azure AD security group.</span></span>
3.  <span data-ttu-id="43ade-227">Déconnectez-vous, puis connectez-vous avec votre compte Administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="43ade-227">Sign out and then sign-in with your IT administrator account.</span></span>
4.  <span data-ttu-id="43ade-228">Configurez le groupe de sécurité test pour la gestion en libre service pour le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="43ade-228">Configure the test security group for self-service management for the test user account.</span></span>
5.  <span data-ttu-id="43ade-229">Déconnectez-vous, puis connectez-vous avec votre compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="43ade-229">Sign out and then sign-in with your test user account.</span></span>
6.  <span data-ttu-id="43ade-230">Utilisez le portail Azure pour ajouter des membres au groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="43ade-230">Use the Azure portal to add members to the test security group.</span></span>
7.  <span data-ttu-id="43ade-231">Supprimez le groupe de sécurité test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="43ade-231">Delete the test security group and the test user account.</span></span>

<a name="crit-identity-ident-prot"></a>
## <a name="optional-azure-ad-identity-protection-is-enabled-to-protect-against-credential-compromise"></a><span data-ttu-id="43ade-232">Facultatif : Azure AD Identity Protection est activé pour protéger contre la compromission d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="43ade-232">Optional: Azure AD Identity Protection is enabled to protect against credential compromise</span></span>

<span data-ttu-id="43ade-233">Vous avez activé Azure AD Identity Protection pour :</span><span class="sxs-lookup"><span data-stu-id="43ade-233">You've enabled Azure AD Identity Protection to:</span></span>

- <span data-ttu-id="43ade-234">résoudre les vulnérabilités d’identités potentielles ;</span><span class="sxs-lookup"><span data-stu-id="43ade-234">Address potential identity vulnerabilities.</span></span>
- <span data-ttu-id="43ade-235">détecter les tentatives de compromission d’informations d’identification possibles ;</span><span class="sxs-lookup"><span data-stu-id="43ade-235">Detect possible credential compromise attempts.</span></span>
- <span data-ttu-id="43ade-236">examiner et résoudre des incidents d’identités suspects en cours.</span><span class="sxs-lookup"><span data-stu-id="43ade-236">Investigate and address ongoing suspicious identity incidents.</span></span>

<span data-ttu-id="43ade-p110">Si vous ignorez cette option, vous ne pourrez pas détecter ou empêcher automatiquement les tentatives de compromission d’informations d’identification ni examiner des incidents de sécurité liés à l’identité. Cela rend votre organisation potentiellement vulnérable à une compromission d’informations d’identification réussie et à la menace qui en résulte pour les données sensibles de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="43ade-p110">If you skip this option, you won’t be able to detect or automatically thwart credential compromise attempts or investigate identity-related security incidents. This potentially leaves your organization vulnerable to a successful credential compromise and the resulting threat to your organization’s sensitive data.</span></span>

<span data-ttu-id="43ade-239">Si nécessaire, l’[Étape 6](identity-azure-ad-identity-protection.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-239">If needed, [Step 6](identity-azure-ad-identity-protection.md) can help you with this option.</span></span>

<a name="crit-identity-pim"></a>
## <a name="optional-you-have-set-up-privileged-identity-management-to-support-on-demand-assignment-of-the-global-administrator-role"></a><span data-ttu-id="43ade-240">Facultatif : vous avez configuré Privileged Identity Management pour prendre en charge l’affectation à la demande du rôle Administrateur général</span><span class="sxs-lookup"><span data-stu-id="43ade-240">Optional: You have set up Privileged Identity Management to support on-demand assignment of the global administrator role</span></span>

<span data-ttu-id="43ade-241">Vous avez déjà suivi les instructions de la rubrique relative à la [configuration d’Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure) pour activer PIM dans votre client Azure AD et configuré vos comptes Administrateur général comme administrateurs éligibles.</span><span class="sxs-lookup"><span data-stu-id="43ade-241">You've used the instructions in [Configure Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure) to enable PIM in your Azure AD tenant and configured your global administrator accounts as eligible admins.</span></span>

<span data-ttu-id="43ade-242">Vous avez également suivi les recommandations de la rubrique relative à la [sécurisation de l’accès privilégié pour les déploiements hybrides et cloud dans Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) pour développer une feuille de route qui sécurise l’accès privilégié contre les cyber-attaquants.</span><span class="sxs-lookup"><span data-stu-id="43ade-242">You've also used the recommendations in [Securing privileged access for hybrid and cloud deployments in Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) to develop a roadmap that secures privileged access against cyber attackers.</span></span>

<span data-ttu-id="43ade-243">Si vous ignorez cette option, vos comptes Administrateur général sont soumis à des attaques en ligne en continu et, en cas de compromission, peuvent autoriser un utilisateur à recueillir, détruire ou conserver vos informations sensibles contre rançon.</span><span class="sxs-lookup"><span data-stu-id="43ade-243">If you skip this option, your global administrator accounts are subject to ongoing online attack and, if compromised, can allow an attacker to harvest, destroy, or hold your sensitive information for ransom.</span></span>

<span data-ttu-id="43ade-244">Si nécessaire, l’[Étape 3](identity-azure-ad-identity-protection.md) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="43ade-244">If needed, [Step 3](identity-azure-ad-identity-protection.md) can help you with this option.</span></span>


## <a name="next-phase"></a><span data-ttu-id="43ade-245">Phase suivante</span><span class="sxs-lookup"><span data-stu-id="43ade-245">Next phase</span></span>

|||
|:-------|:-----|
|![](./media/deploy-foundation-infrastructure/win10enterprise_icon-small.png)| <span data-ttu-id="43ade-246">Votre phase suivante dans le processus de déploiement de bout en bout pour Microsoft 365 Entreprise est [Windows 10 Entreprise](windows10-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="43ade-246">Your next phase in the end-to-end deployment process for Microsoft 365 Enterprise is [Windows 10 Enterprise](windows10-infrastructure.md).</span></span> |

