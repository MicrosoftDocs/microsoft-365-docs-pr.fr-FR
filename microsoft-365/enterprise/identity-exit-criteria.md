---
title: 'Phase 2 : Critères de sortie de l’infrastructure d’identités'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/05/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Assurez-vous que votre configuration répond aux critères de Microsoft 365 Entreprise pour l’infrastructure et les services d’identités.
ms.openlocfilehash: 0f2d1cbeef87301729b23a6290277b28466c9770
ms.sourcegitcommit: dbcc32218489ab256b7eb343290fcccb9bc04e36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/02/2019
ms.locfileid: "33553303"
---
# <a name="phase-2-identity-infrastructure-exit-criteria"></a><span data-ttu-id="d9e77-103">Phase 2 : Critères de sortie de l’infrastructure d’identités</span><span class="sxs-lookup"><span data-stu-id="d9e77-103">Phase 2: Identity infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="d9e77-104">Vérifiez que votre infrastructure d’identité répond aux critères suivants requis et que vous avez décidé ceux qui sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="d9e77-104">Make sure your identity infrastructure meets the following required criteria and that you've considered those that are optional.</span></span>

<span data-ttu-id="d9e77-105">Voir également les [Conditions préalables](https://docs.microsoft.com/microsoft-365-enterprise/identity-access-policies#prerequisites) pour consulter d’autre suggestions sur l’infrastructure d’identité.</span><span class="sxs-lookup"><span data-stu-id="d9e77-105">Also see [Prerequisites](https://docs.microsoft.com/microsoft-365-enterprise/identity-access-policies#prerequisites) for additional recommendations on identity infrastructure.</span></span>

<a name="crit-identity-user-groups"></a>
## <a name="required-all-users-groups-and-group-memberships-have-been-created"></a><span data-ttu-id="d9e77-106">Obligatoire : tous les utilisateurs, groupes et appartenances aux groupes ont été créés</span><span class="sxs-lookup"><span data-stu-id="d9e77-106">Required: All users, groups, and group memberships have been created</span></span>

<span data-ttu-id="d9e77-107">Vous avez créé des groupes et des comptes d’utilisateur afin que :</span><span class="sxs-lookup"><span data-stu-id="d9e77-107">You've created user accounts and groups so that:</span></span>

- <span data-ttu-id="d9e77-108">Les employés au sein de votre organisation et les fournisseurs, entrepreneurs et partenaires qui travaillent pour ou avec votre organisation aient un compte d’utilisateur correspondant dans Azure Active Directory (AD) ;</span><span class="sxs-lookup"><span data-stu-id="d9e77-108">Employees in your organization and the vendors, contractors, and partners that work for or with your organization have a corresponding user account in Azure Active Directory (Azure AD).</span></span>
- <span data-ttu-id="d9e77-109">les groupes Azure AD et leurs membres contiennent des comptes d’utilisateur et d’autres groupes à des fins diverses (attribution de paramètres de sécurité pour les services de cloud computing Microsoft, attribution automatique de licences et autres utilisations).</span><span class="sxs-lookup"><span data-stu-id="d9e77-109">Azure AD groups and their members contain user accounts and other groups for various purposes, such as the provisioning of security settings for Microsoft cloud services, automatic licensing, and other uses.</span></span>

<span data-ttu-id="d9e77-110">Si nécessaire, l’[Étape 1](identity-plan-users-groups.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="d9e77-110">If needed, [Step 1](identity-plan-users-groups.md) can help you meet this requirement.</span></span>

<a name="crit-identity-global-admin"></a>
## <a name="required-your-global-administrator-accounts-are-protected"></a><span data-ttu-id="d9e77-111">Obligatoire : vos comptes d’administrateur général sont protégés</span><span class="sxs-lookup"><span data-stu-id="d9e77-111">Required: Your global administrator accounts are protected</span></span> 

<span data-ttu-id="d9e77-112">Vous avez [protégé vos comptes d’administrateur général Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts) afin d’éviter de compromettre les informations d’identification pouvant entraîner des violations d’un abonnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="d9e77-112">You've [protected your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts) to avoid compromising credentials that can lead to breaches of an Office 365 subscription.</span></span>

<span data-ttu-id="d9e77-113">Si vous ignorez cette exigence, vos comptes d’administrateur général peuvent être attaqués et compromis, autorisant un utilisateur à accéder à vos données à l’échelle du système à des fins de collecte, destruction ou prise en otage des données.</span><span class="sxs-lookup"><span data-stu-id="d9e77-113">If you skip this requirement, your global administrator accounts can be susceptible to attack and compromise, allowing an attacker to gain system-wide access to your data for harvesting, destruction, or ransom.</span></span>

<span data-ttu-id="d9e77-114">Si nécessaire, l’[Étape 2](identity-designate-protect-admin-accounts.md#identity-global-admin) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="d9e77-114">If needed, [Step 2](identity-designate-protect-admin-accounts.md#identity-global-admin) can help you meet this requirement.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="d9e77-115">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="d9e77-115">How to test</span></span>

<span data-ttu-id="d9e77-116">Suivez ces étapes pour vérifier que vous avez protégé vos comptes d’administrateur général :</span><span class="sxs-lookup"><span data-stu-id="d9e77-116">Use these steps to verify that you've protected your global administrator accounts:</span></span>

1. <span data-ttu-id="d9e77-p101">Exécutez la commande Azure AD V2 suivante à l’invite de commandes PowerShell. Vous devriez voir uniquement la liste des comptes administrateur général dédiés.</span><span class="sxs-lookup"><span data-stu-id="d9e77-p101">Run the following Azure AD V2 command at the PowerShell command prompt. You should see only the list of dedicated global administrator accounts.</span></span>
   ```
   Get-AzureADDirectoryRole | where { $_.DisplayName -eq "Company Administrator" } | Get-AzureADDirectoryRoleMember | Ft DisplayName
   ```
2. <span data-ttu-id="d9e77-p102">Connectez-vous à Office 365 à l’aide de chacun des comptes de l’étape 1. Chaque connexion doit exiger l’authentification multifacteur et la forme la plus forte d’authentification secondaire disponible dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d9e77-p102">Sign in to Office 365 using each of the accounts from step 1. Each sign in must require multi-factor authentication and the strongest form of secondary authentication available in your organization.</span></span>

> [!Note]
> <span data-ttu-id="d9e77-121">Reportez-vous à [Se connecter à Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) pour obtenir des instructions sur l’installation du module Azure AD PowerShell pour Graph et la connexion à Office 365.</span><span class="sxs-lookup"><span data-stu-id="d9e77-121">See [Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) for instructions on installing the Azure Active Directory PowerShell for Graph module and signing in to Office 365.</span></span>

<a name="crit-identity-pim"></a>
## <a name="optional-you-have-set-up-privileged-identity-management-to-support-on-demand-assignment-of-the-global-administrator-role"></a><span data-ttu-id="d9e77-122">Facultatif : vous avez configuré Privileged Identity Management pour prendre en charge l’affectation à la demande du rôle Administrateur général</span><span class="sxs-lookup"><span data-stu-id="d9e77-122">Optional: You have set up Privileged Identity Management to support on-demand assignment of the global administrator role</span></span>

<span data-ttu-id="d9e77-123">Vous avez déjà suivi les instructions de la rubrique relative à la [configuration d’Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure) pour activer PIM dans votre client Azure AD et configuré vos comptes Administrateur général comme administrateurs éligibles.</span><span class="sxs-lookup"><span data-stu-id="d9e77-123">You've used the instructions in [Configure Azure AD Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure) to enable PIM in your Azure AD tenant and configured your global administrator accounts as eligible admins.</span></span>

<span data-ttu-id="d9e77-124">Vous avez également suivi les recommandations de la rubrique relative à la [sécurisation de l’accès privilégié pour les déploiements hybrides et cloud dans Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) pour développer une feuille de route qui sécurise l’accès privilégié contre les cyber-attaquants.</span><span class="sxs-lookup"><span data-stu-id="d9e77-124">You've also used the recommendations in [Securing privileged access for hybrid and cloud deployments in Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) to develop a roadmap that secures privileged access against cyber attackers.</span></span>

<span data-ttu-id="d9e77-125">Si vous ignorez cette option, vos comptes Administrateur général sont soumis à des attaques en ligne en continu et, en cas de compromission, peuvent autoriser un utilisateur à recueillir, détruire ou conserver vos informations sensibles contre rançon.</span><span class="sxs-lookup"><span data-stu-id="d9e77-125">If you skip this option, your global administrator accounts are subject to ongoing online attack and, if compromised, can allow an attacker to harvest, destroy, or hold your sensitive information for ransom.</span></span>

<span data-ttu-id="d9e77-126">Si nécessaire, l’[Étape 2](identity-designate-protect-admin-accounts.md#identity-pim) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-126">If needed, [Step 2](identity-designate-protect-admin-accounts.md#identity-pim) can help you with this option.</span></span>


<a name="crit-identity-sync"></a>
## <a name="required-users-and-groups-are-synchronized-with-azure-ad"></a><span data-ttu-id="d9e77-127">Obligatoire : les utilisateurs et les groupes sont synchronisés avec Azure AD</span><span class="sxs-lookup"><span data-stu-id="d9e77-127">Required: Users and groups are synchronized with Azure AD</span></span>

<span data-ttu-id="d9e77-128">Si vous avez un fournisseur d’identité local existant, comme Active Directory Domain Services (AD DS), vous avez utilisé Azure AD Connect pour synchroniser les comptes d’utilisateur et les groupes de votre fournisseur d’identité local avec votre client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d9e77-128">If you have an existing on-premises identity provider, such as Active Directory Domain Services (AD DS), you have used Azure AD Connect to synchronize user accounts and groups from your on-premises identity provider to your Azure AD tenant.</span></span>

<span data-ttu-id="d9e77-129">Avec la synchronisation d’annuaires, vos utilisateurs peuvent se connecter à Office 365 et à d’autres services de cloud computing Microsoft à l’aide des mêmes informations d’identification qu’ils utilisent pour se connecter à leurs ordinateurs et accéder aux ressources locales.</span><span class="sxs-lookup"><span data-stu-id="d9e77-129">With directory synchronization, your users can sign in to Office 365 and other Microsoft cloud services using the same credentials that they use to sign in to their computers and access on-premises resources.</span></span>

<span data-ttu-id="d9e77-130">Si nécessaire, l’[Étape 3](identity-azure-ad-connect.md#identity-sync) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="d9e77-130">If needed, [Step 3](identity-azure-ad-connect.md#identity-sync) can help you meet this requirement.</span></span>

<span data-ttu-id="d9e77-131">Si vous ignorez cette exigence, vous aurez deux ensembles de groupes et comptes d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="d9e77-131">If you skip this requirement, you’ll have two sets of user accounts and groups:</span></span>

- <span data-ttu-id="d9e77-132">Groupes et comptes d’utilisateur qui existent dans votre fournisseur d’identité local</span><span class="sxs-lookup"><span data-stu-id="d9e77-132">User accounts and groups that exist in your on-premises identity provider</span></span>
- <span data-ttu-id="d9e77-133">Groupes et comptes d’utilisateur qui existent dans votre client Azure AD</span><span class="sxs-lookup"><span data-stu-id="d9e77-133">User accounts and groups that exist in your Azure AD tenant</span></span>

<span data-ttu-id="d9e77-p103">Dans cet état, les deux ensembles de groupes et comptes d’utilisateur doivent être gérés manuellement par les administrateurs informatiques et les utilisateurs. Cela entraînera inévitablement des groupes, leurs mots de passe et comptes non synchronisés.</span><span class="sxs-lookup"><span data-stu-id="d9e77-p103">In this state, the two sets of user accounts and groups must be manually maintained by both IT administrators and users. This will inevitably lead to unsynchronized accounts, their passwords, and groups.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="d9e77-136">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="d9e77-136">How to test</span></span>
<span data-ttu-id="d9e77-137">Pour vérifier que l’authentification avec les informations d’identification locales fonctionne correctement, connectez-vous au portail Office avec vos informations d’identification locales.</span><span class="sxs-lookup"><span data-stu-id="d9e77-137">To verify that authentication with on-premises credentials works correctly, sign in to the Office portal with your on-premises credentials.</span></span>

<span data-ttu-id="d9e77-138">Pour vérifier que la synchronisation d’annuaires fonctionne correctement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d9e77-138">To verify that directory synchronization is working correctly, do the following:</span></span>

1.  <span data-ttu-id="d9e77-139">Créez un groupe de test dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="d9e77-139">Create a new test group in Windows Server AD.</span></span>
2.  <span data-ttu-id="d9e77-140">Attendez l’heure de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="d9e77-140">Wait for the synchronization time.</span></span>
3.  <span data-ttu-id="d9e77-141">Vérifiez votre client Azure AD pour vous assurer que le nouveau nom du groupe de test apparaît.</span><span class="sxs-lookup"><span data-stu-id="d9e77-141">Check your Azure AD tenant to verify that the new test group name appears.</span></span>

<a name="crit-identity-sync-health"></a>
## <a name="optional-directory-synchronization-is-monitored"></a><span data-ttu-id="d9e77-142">Facultatif : la synchronisation d’annuaires est surveillée</span><span class="sxs-lookup"><span data-stu-id="d9e77-142">Optional: Directory synchronization is monitored</span></span>

<span data-ttu-id="d9e77-143">Vous avez utilisé [Utilisation d’Azure AD Connect Health pour la synchronisation](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) (pour la synchronisation de mot de passe) ou [Utilisation d’Azure AD Connect Health avec AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) (pour l’authentification fédérée) et avez déployé Azure AD Connect Health, ce qui implique :</span><span class="sxs-lookup"><span data-stu-id="d9e77-143">You've used [Azure AD Connect Health with sync](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) (for password synchronization) or [Using Azure AD Connect Health with AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) (for federated authentication) and have deployed Azure AD Connect Health, which involves:</span></span>

- <span data-ttu-id="d9e77-144">L’installation de l’agent Azure AD Connect Health sur chacun de vos serveurs d’identités local.</span><span class="sxs-lookup"><span data-stu-id="d9e77-144">Installing the Azure AD Connect Health agent on each of your on-premises identity servers.</span></span>
- <span data-ttu-id="d9e77-145">L’utilisation du portail Azure AD Connect Health pour surveiller l’état de synchronisation en cours.</span><span class="sxs-lookup"><span data-stu-id="d9e77-145">Using the Azure AD Connect Health portal to monitor the state of the ongoing synchronization.</span></span>

<span data-ttu-id="d9e77-146">Si vous ignorez cette option, vous pouvez évaluer plus précisément l’état de votre infrastructure d’identités basée sur le cloud.</span><span class="sxs-lookup"><span data-stu-id="d9e77-146">If you skip this option, you can more accurately assess the state of your cloud-based identity infrastructure.</span></span>

<span data-ttu-id="d9e77-147">Si nécessaire, l’[Étape 3](identity-azure-ad-connect.md#identity-sync-health) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-147">If needed, [Step 3](identity-azure-ad-connect.md#identity-sync-health) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="d9e77-148">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="d9e77-148">How to test</span></span>
<span data-ttu-id="d9e77-149">Le portail Azure AD Connect Health affiche l’état actuel et correct de vos serveurs d’identités locaux et la synchronisation en cours.</span><span class="sxs-lookup"><span data-stu-id="d9e77-149">The Azure AD Connect Health portal shows the current and correct state of your on-premises identity servers and the ongoing synchronization.</span></span>

<a name="crit-identity-mfa"></a>
## <a name="optional-multi-factor-authentication-is-enabled-for-your-users"></a><span data-ttu-id="d9e77-150">Facultatif : l’authentification multifacteur est activée pour vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d9e77-150">Optional: Multi-factor authentication is enabled for your users</span></span>

<span data-ttu-id="d9e77-151">Vous avez utilisé [Planifier l’authentification multifacteur pour les déploiements Office 365](https://docs.microsoft.com/office365/admin/security-and-compliance/multi-factor-authentication-plan) et [Configurer l’authentification multifacteur pour les utilisateurs d’Office 365](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication) pour activer l’authentification multifacteur (MFA) pour vos comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d9e77-151">You used [Plan for multi-factor authentication for Office 365 Deployments](https://docs.microsoft.com/office365/admin/security-and-compliance/multi-factor-authentication-plan) and [Set up multi-factor authentication for Office 365 users](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication) to enable multifactor authentication (MFA) for your user accounts.</span></span>

<span data-ttu-id="d9e77-p104">Si vous ignorez cette option, vos comptes d’utilisateur sont vulnérables à la compromission des informations d’identification par des cyber-attaquants. Si le mot de passe d’un compte d’utilisateur est compromis, toutes les ressources et les fonctionnalités du compte, telles que les rôles d’administrateur, sont disponibles pour l’utilisateur malveillant. Ainsi, ce dernier peut copier, détruire ou conserver des documents internes et d’autres données contre rançon.</span><span class="sxs-lookup"><span data-stu-id="d9e77-p104">If you skip this option, your user accounts are vulnerable to credential compromise by cyber attackers. If a user account’s password is compromised, all the resources and capabilities of the account, such as administrator roles, are available to the attacker. This allows the attacker to copy, destroy, or hold for ransom internal documents and other data.</span></span>

<span data-ttu-id="d9e77-155">Si nécessaire, l’[Étape 4](identity-multi-factor-authentication.md#identity-mfa) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-155">If needed, [Step 4](identity-multi-factor-authentication.md#identity-mfa) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="d9e77-156">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="d9e77-156">How to test</span></span>

1.  <span data-ttu-id="d9e77-157">Créez un compte d’utilisateur test dans le portail Office 365 Admin et attribuez-lui une licence.</span><span class="sxs-lookup"><span data-stu-id="d9e77-157">Create a test user account in the Office 365 Admin portal and assign them a license.</span></span> 
2.  <span data-ttu-id="d9e77-158">Configurez l’authentification multifacteur pour le compte d’utilisateur test avec la méthode de vérification supplémentaire que vous utilisez pour les comptes d’utilisateur réels, comme l’envoi d’un message sur votre téléphone.</span><span class="sxs-lookup"><span data-stu-id="d9e77-158">Configure multi-factor authentication for the test user account with the additional verification method that you are using for actual user accounts, such as sending a message to your phone.</span></span> 
3.  <span data-ttu-id="d9e77-159">Connectez-vous au portail Office 365 ou Azure avec le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-159">Sign in to the Office 365 or Azure portal with the test user account.</span></span>
4.  <span data-ttu-id="d9e77-160">Vérifiez que l’authentification multifacteur vous invite à saisir les informations de vérification supplémentaires et que l’authentification s’effectue sans problèmes.</span><span class="sxs-lookup"><span data-stu-id="d9e77-160">Verify that MFA prompts you for the additional verification information and results in a successful authentication.</span></span> 
5.  <span data-ttu-id="d9e77-161">Supprimez le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-161">Delete the test user account.</span></span>

<a name="crit-identity-ident-prot"></a>
## <a name="optional-azure-ad-identity-protection-is-enabled-to-protect-against-credential-compromise"></a><span data-ttu-id="d9e77-162">Facultatif : Azure AD Identity Protection est activé pour protéger contre la compromission d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="d9e77-162">Optional: Azure AD Identity Protection is enabled to protect against credential compromise</span></span>

<span data-ttu-id="d9e77-163">Vous avez activé Azure AD Identity Protection pour :</span><span class="sxs-lookup"><span data-stu-id="d9e77-163">You've enabled Azure AD Identity Protection to:</span></span>

- <span data-ttu-id="d9e77-164">résoudre les vulnérabilités d’identités potentielles ;</span><span class="sxs-lookup"><span data-stu-id="d9e77-164">Address potential identity vulnerabilities.</span></span>
- <span data-ttu-id="d9e77-165">détecter les tentatives de compromission d’informations d’identification possibles ;</span><span class="sxs-lookup"><span data-stu-id="d9e77-165">Detect possible credential compromise attempts.</span></span>
- <span data-ttu-id="d9e77-166">examiner et résoudre des incidents d’identités suspects en cours.</span><span class="sxs-lookup"><span data-stu-id="d9e77-166">Investigate and address ongoing suspicious identity incidents.</span></span>

<span data-ttu-id="d9e77-p105">Si vous ignorez cette option, vous ne pourrez pas détecter ou empêcher automatiquement les tentatives de compromission d’informations d’identification ni examiner des incidents de sécurité liés à l’identité. Cela rend votre organisation potentiellement vulnérable à une compromission d’informations d’identification réussie et à la menace qui en résulte pour les données sensibles de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d9e77-p105">If you skip this option, you won’t be able to detect or automatically thwart credential compromise attempts or investigate identity-related security incidents. This potentially leaves your organization vulnerable to a successful credential compromise and the resulting threat to your organization’s sensitive data.</span></span>

<span data-ttu-id="d9e77-169">Si nécessaire, l’[Étape 4](identity-multi-factor-authentication.md#identity-ident-prot) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-169">If needed, [Step 4](identity-multi-factor-authentication.md#identity-ident-prot) can help you with this option.</span></span>

<a name="crit-identity-pw-reset"></a>
## <a name="optional-users-can-reset-their-own-passwords"></a><span data-ttu-id="d9e77-170">Facultatif : les utilisateurs peuvent réinitialiser leurs mots de passe</span><span class="sxs-lookup"><span data-stu-id="d9e77-170">Optional: Users can reset their own passwords</span></span>

<span data-ttu-id="d9e77-171">Vous avez utilisé la rubrique relative au [déploiement rapide de la réinitialisation du mot de passe libre-service Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) pour configurer la réinitialisation du mot de passe pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d9e77-171">You've used [Azure AD self-service password reset rapid deployment](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) to configure password reset for your users.</span></span>

<span data-ttu-id="d9e77-172">Si vous ne remplissez pas cette condition, les utilisateurs dépendront des administrateurs de compte d’utilisateur pour réinitialiser leurs mots de passe, entraînant une surcharge d’administration informatique supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d9e77-172">If you don’t meet this condition, users will be dependent on user account administrators to reset their passwords, resulting in additional IT administration overhead.</span></span>

<span data-ttu-id="d9e77-173">Si nécessaire, l’[Étape 5](identity-password-reset.md#identity-pw-reset) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-173">If needed, [Step 5](identity-password-reset.md#identity-pw-reset) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="d9e77-174">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="d9e77-174">How to test</span></span>

1. <span data-ttu-id="d9e77-175">Créez un compte d’utilisateur test avec un mot de passe initial.</span><span class="sxs-lookup"><span data-stu-id="d9e77-175">Create a test user account with an initial password.</span></span>
2. <span data-ttu-id="d9e77-176">Suivez les étapes décrites dans [Autoriser les utilisateurs à réinitialiser leur mot de passe dans Office 365](https://docs.microsoft.com/office365/admin/add-users/let-users-reset-passwords) pour réinitialiser le mot de passe sur le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-176">Use the steps in [Let users reset their own passwords in Office 365](https://docs.microsoft.com/office365/admin/add-users/let-users-reset-passwords) to reset the password on the test user account.</span></span>
3. <span data-ttu-id="d9e77-177">Déconnectez-vous, puis connectez-vous au compte d’utilisateur test à l’aide du mot de passe réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="d9e77-177">Sign out and then sign in to the test user account using the reset password.</span></span>
4. <span data-ttu-id="d9e77-178">Supprimez le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-178">Delete the test user account.</span></span>

<a name="crit-identity-pw-writeback"></a>
## <a name="optional-password-writeback-is-enabled-for-your-users"></a><span data-ttu-id="d9e77-179">Facultatif : l’écriture différée du mot de passe est activée pour vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d9e77-179">Optional: Password writeback is enabled for your users</span></span>

<span data-ttu-id="d9e77-180">Vous avez déjà consulté les instructions de la rubrique relative à la [réinitialisation du mot de passe libre-service d’Azure AD (SSPR) avec l’écriture différée du mot de passe](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) pour activer l’écriture différée du mot de passe pour le client Azure AD de votre abonnement Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d9e77-180">You've used the instructions in [Azure AD SSPR with password writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) to enable password writeback for the Azure AD tenant of your Microsoft 365 Enterprise subscription.</span></span>

<span data-ttu-id="d9e77-181">Si vous ignorez cette option, les utilisateurs qui ne sont pas connectés à votre réseau local doivent réinitialiser ou déverrouiller leurs mot de passe AD DS en faisant appel à un administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="d9e77-181">If you skip this option, users who aren’t connected to your on-premises network must reset or unlock their AD DS passwords through an IT administrator.</span></span>

<span data-ttu-id="d9e77-182">Si nécessaire, l’[Étape 5](identity-password-reset.md#identity-pw-writeback) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-182">If needed, [Step 5](identity-password-reset.md#identity-pw-writeback) can help you with this option.</span></span>

>[!Note]
><span data-ttu-id="d9e77-183">L’écriture différée du mot de passe est requise pour exploiter pleinement les fonctionnalités d’Azure AD Identity Protection, comme l’obligation pour les utilisateurs de modifier leurs mots de passe locaux lorsque Azure AD a détecté un risque élevé de compromission de compte.</span><span class="sxs-lookup"><span data-stu-id="d9e77-183">Password writeback is required to fully utilize Azure AD Identity Protection features, such as requiring users to change their on-premises passwords when Azure AD has detected a high risk of account compromise.</span></span>
>

### <a name="how-to-test"></a><span data-ttu-id="d9e77-184">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="d9e77-184">How to test</span></span>

<span data-ttu-id="d9e77-185">Vous testez l’écriture différée de votre mot de passe en changeant votre mot de passe Office 365.</span><span class="sxs-lookup"><span data-stu-id="d9e77-185">You test password writeback by changing your password in Office 365.</span></span> <span data-ttu-id="d9e77-186">Vous devriez pouvoir utiliser votre compte et le nouveau mot de passe pour accéder aux ressources AD DS locales.</span><span class="sxs-lookup"><span data-stu-id="d9e77-186">You should be able to use your account and new password to access on-premises AD DS resources.</span></span>

1. <span data-ttu-id="d9e77-187">Créez un compte d’utilisateur test dans votre version locale AD DS, autorisez la synchronisation d’annuaires, puis accordez-lui une licence Office 365 dans le portail d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d9e77-187">Create a test user account in your on-premises AD DS, allow directory synchronization to occur, and then grant it an Office 365 license in the Microsoft 365 admin center.</span></span>
2. <span data-ttu-id="d9e77-188">Sur un ordinateur distant qui est relié à votre domaine Server AD DS local, connectez-vous à l’ordinateur et au portail Office à l’aide des informations d’identification du compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-188">From a remote computer that is joined to your on-premises AD DS domain, sign in to the computer and the Office portal using the credentials of the test user account.</span></span>
3. <span data-ttu-id="d9e77-189">Sélectionnez **Paramètres > Paramètres Office 365 > Mot de passe > Changer le mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="d9e77-189">Select **Settings > Office 365 settings > Password > Change password**.</span></span>
4. <span data-ttu-id="d9e77-190">Tapez le mot de passe actuel, tapez un nouveau mot de passe, puis confirmez-le.</span><span class="sxs-lookup"><span data-stu-id="d9e77-190">Type the current password, type a new password, and then confirm it.</span></span>
5. <span data-ttu-id="d9e77-191">Déconnectez-vous du portail Office et de l’ordinateur distant, puis connectez-vous à l’ordinateur à l’aide du compte d’utilisateur de test et son nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="d9e77-191">Sign out of the Office portal and the remote computer and then sign in to the computer using the test user account and its new password.</span></span> <span data-ttu-id="d9e77-192">Cela prouve que vous avez été en mesure de modifier le mot de passe d’une version locale de compte d’utilisateur AD DS à l’aide du client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d9e77-192">This proves that you were able to change the password of an on-premises AD DS user account using the Azure AD tenant.</span></span>

<a name="crit-identity-sso"></a>
## <a name="optional-users-can-sign-in-using-azure-ad-seamless-single-sign-on"></a><span data-ttu-id="d9e77-193">Facultatif : les utilisateurs peuvent se connecter à l’aide de l’authentification unique Azure AD Single Sign-on</span><span class="sxs-lookup"><span data-stu-id="d9e77-193">Optional: Users can sign in using Azure AD Seamless Single Sign-on</span></span>

<span data-ttu-id="d9e77-194">Vous avez activé l’[authentification unique transparente Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start) pour que votre organisation simplifie la manière dont les utilisateurs se connectent aux applications basées sur le cloud, comme Office 365.</span><span class="sxs-lookup"><span data-stu-id="d9e77-194">You enabled [Azure AD Connect: Seamless Single Sign-On](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start) for your organization to simplify how users sign in to cloud-based applications, such as Office 365.</span></span>

<span data-ttu-id="d9e77-195">Si vous ignorez cette option, vos utilisateurs peuvent être invités à fournir des informations d’identification lorsqu’ils accèdent à d’autres applications qui utilisent Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d9e77-195">If you skip this option, your users might be prompted to provide credentials when they access additional applications that use Azure AD.</span></span>

<span data-ttu-id="d9e77-196">Si nécessaire, l’[Étape 5](identity-password-reset.md#identity-sso) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-196">If needed, [Step 5](identity-password-reset.md#identity-sso) can help you with this option.</span></span>

<a name="crit-identity-custom-sign-in"></a>
## <a name="optional-the-office-365-sign-in-screen-is-personalized-for-your-organization"></a><span data-ttu-id="d9e77-197">Facultatif : l’écran de connexion Office 365 est personnalisé pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="d9e77-197">Optional: The Office 365 sign-in screen is personalized for your organization</span></span>

<span data-ttu-id="d9e77-198">Vous avez utilisé [Ajouter la marque de votre organisation à votre page de connexion et aux pages du Panneau d’accès](http://aka.ms/aadpaddbranding) pour ajouter la marque de votre organisation à la page de connexion Office 365.</span><span class="sxs-lookup"><span data-stu-id="d9e77-198">You have used [Add company branding to your sign-in and Access Panel pages](http://aka.ms/aadpaddbranding) to add your organization’s branding to the Office 365 sign-in page.</span></span>

<span data-ttu-id="d9e77-199">Si vous ignorez cette option, vos utilisateurs verront un écran de connexion Office 365 générique et peuvent ne pas être certains de se connecter au site de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d9e77-199">If you skip this option, your users will see a generic Office 365 sign-in screen and might not be confident that they’re signing into your organization’s site.</span></span>

<span data-ttu-id="d9e77-200">Si nécessaire, l’[Étape 5](identity-password-reset.md#identity-custom-sign-in) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-200">If needed, [Step 5](identity-password-reset.md#identity-custom-sign-in) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="d9e77-201">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="d9e77-201">How to test</span></span>

<span data-ttu-id="d9e77-p108">Connectez-vous au portail Office 365 avec votre nom de compte d’utilisateur et l’authentification multifacteur. Vos éléments de marque personnalisés apparaissent sur la page de connexion.</span><span class="sxs-lookup"><span data-stu-id="d9e77-p108">Sign in to the Office 365 portal with your user account name and multi-factor authentication. You should see your custom branding elements on the sign-in page.</span></span>

<a name="crit-identity-self-service-groups"></a>
## <a name="optional-self-service-group-management-is-enabled-for-specific-azure-ad-security-and-office-365-groups"></a><span data-ttu-id="d9e77-204">Facultatif : la gestion des groupes en libre-service est activée pour des groupes Office 365 et de sécurité Azure AD spécifiques</span><span class="sxs-lookup"><span data-stu-id="d9e77-204">Optional: Self-service group management is enabled for specific Azure AD security and Office 365 groups</span></span>

<span data-ttu-id="d9e77-205">Vous avez déterminé les groupes qui sont appropriés pour la gestion en libre service, décrit à leurs propriétaires les responsabilités et le workflow de gestion des groupes et [configuré la gestion en libre-service dans Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management) pour ces groupes.</span><span class="sxs-lookup"><span data-stu-id="d9e77-205">You've determined which groups are appropriate for self-service management, instructed their owners on group management workflow and responsibilities, and [set up self-service management in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management) for those groups.</span></span>

<span data-ttu-id="d9e77-206">Si vous ignorez cette option, toutes les tâches de gestion des groupes Azure AD doivent être effectuées par des administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="d9e77-206">If you skip this option, all Azure AD group management tasks must be done by IT administrators.</span></span>

<span data-ttu-id="d9e77-207">Si nécessaire, l’[Étape 6](identity-self-service-group-management.md#identity-self-service-groups) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-207">If needed, [Step 6](identity-self-service-group-management.md#identity-self-service-groups) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="d9e77-208">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="d9e77-208">How to test</span></span>
1.  <span data-ttu-id="d9e77-209">Créez un compte d’utilisateur test dans Azure AD avec le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e77-209">Create a test user account in Azure AD with the Azure portal.</span></span>
2.  <span data-ttu-id="d9e77-210">Connectez-vous comme avec le compte d’utilisateur test et créez un groupe de sécurité Azure AD test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-210">Sign-in as with the test user account and create a test Azure AD security group.</span></span>
3.  <span data-ttu-id="d9e77-211">Déconnectez-vous, puis connectez-vous avec votre compte Administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="d9e77-211">Sign out and then sign-in with your IT administrator account.</span></span>
4.  <span data-ttu-id="d9e77-212">Configurez le groupe de sécurité test pour la gestion en libre service pour le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-212">Configure the test security group for self-service management for the test user account.</span></span>
5.  <span data-ttu-id="d9e77-213">Déconnectez-vous, puis connectez-vous avec votre compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-213">Sign out and then sign-in with your test user account.</span></span>
6.  <span data-ttu-id="d9e77-214">Utilisez le portail Azure pour ajouter des membres au groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-214">Use the Azure portal to add members to the test security group.</span></span>
7.  <span data-ttu-id="d9e77-215">Supprimez le groupe de sécurité test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-215">Delete the test security group and the test user account.</span></span>

<a name="crit-identity-dyn-groups"></a>
## <a name="optional-dynamic-group-membership-settings-automatically-add-user-accounts-to-groups-based-on-user-account-attributes"></a><span data-ttu-id="d9e77-216">Facultatif : les paramètres d’appartenance à un groupe dynamique ajoutent automatiquement des comptes d’utilisateur à des groupes en fonction des attributs de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d9e77-216">Optional: Dynamic group membership settings automatically add user accounts to groups based on user account attributes</span></span>

<span data-ttu-id="d9e77-217">Vous avez déterminé l’ensemble des groupes dynamiques Azure AD et utilisé les instructions décrites dans la rubrique relative à l’[appartenance à un groupe dynamique en fonction des attributs dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal) pour créer les groupes et les règles qui déterminent l’ensemble des attributs de compte d’utilisateur et des valeurs pour l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="d9e77-217">You've determined the set of Azure AD dynamic groups and used the instructions in [Attribute-based dynamic group membership in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal) to create the groups and the rules that determine the set of user account attributes and values for group membership.</span></span>

<span data-ttu-id="d9e77-p109">Si vous ignorez cette option, l’appartenance à un groupe doit être effectuée manuellement lorsque de nouveaux comptes sont ajoutés ou que les attributs de compte d’utilisateur changent au fil du temps. Par exemple, si une personne est mutée du service des ventes au service de comptabilité, vous devez :</span><span class="sxs-lookup"><span data-stu-id="d9e77-p109">If you skip this option, group membership must be done manually as new accounts are added or as user account attributes change over time. For example, if someone moves from the Sales department to the Accounting department, you must:</span></span>

- <span data-ttu-id="d9e77-220">mettre à jour la valeur de l’attribut Service pour ce compte d’utilisateur ;</span><span class="sxs-lookup"><span data-stu-id="d9e77-220">Update the value of the Department attribute for that user account.</span></span>
- <span data-ttu-id="d9e77-221">le supprimer manuellement du groupe Ventes ;</span><span class="sxs-lookup"><span data-stu-id="d9e77-221">Manually remove them from the Sales group.</span></span>
- <span data-ttu-id="d9e77-222">l’ajouter manuellement au groupe Comptabilité.</span><span class="sxs-lookup"><span data-stu-id="d9e77-222">Manually add them to the Accounting group.</span></span>

<span data-ttu-id="d9e77-223">Si les groupes Ventes et Comptabilité sont dynamiques, vous devez uniquement modifier la valeur Service du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d9e77-223">If the Sales and Accounting groups were dynamic, you would only have to change the user account’s Department value.</span></span>

<span data-ttu-id="d9e77-224">Si nécessaire, l’[Étape 6](identity-self-service-group-management.md#identity-dyn-groups) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-224">If needed, [Step 6](identity-self-service-group-management.md#identity-dyn-groups) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="d9e77-225">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="d9e77-225">How to test</span></span>

1. <span data-ttu-id="d9e77-226">Créez un groupe dynamique test dans Azure AD avec le portail Azure et configurez une règle pour que Service soit égal à « test1 ».</span><span class="sxs-lookup"><span data-stu-id="d9e77-226">Create a test dynamic group in Azure AD with the Azure portal and configure a rule for the Department equals “test1”.</span></span>
2. <span data-ttu-id="d9e77-227">Créez un compte d’utilisateur test dans Azure AD et définissez la propriété Service sur « test1 ».</span><span class="sxs-lookup"><span data-stu-id="d9e77-227">Create a test user account in Azure AD and set the Department property to “test1”.</span></span>
3. <span data-ttu-id="d9e77-228">Examinez les propriétés du compte d’utilisateur pour vous assurer qu’il a été défini comme membre du groupe dynamique test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-228">Examine the properties of the user account to ensure that it was made a member of the test dynamic group.</span></span>
4. <span data-ttu-id="d9e77-229">Modifiez la valeur de la propriété Service pour le compte d’utilisateur test et définissez-la sur « test2 ».</span><span class="sxs-lookup"><span data-stu-id="d9e77-229">Change the value of the Department property for the test user account to “test2”.</span></span>
5. <span data-ttu-id="d9e77-230">Examinez les propriétés du compte d’utilisateur pour vous assurer qu’il n’est plus membre du groupe dynamique test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-230">Examine the properties of the user account to ensure that it is no longer a member of the test dynamic group.</span></span>
6. <span data-ttu-id="d9e77-231">Supprimez le groupe dynamique test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-231">Delete the test dynamic group and the test user account.</span></span>

<a name="crit-identity-group-license"></a>
## <a name="optional-group-based-licensing-to-automatically-assign-and-remove-licenses-to-user-accounts-based-on-group-membership"></a><span data-ttu-id="d9e77-232">Facultatif : gestion des licences par groupes pour attribuer des licences aux comptes d’utilisateur et les supprimer automatiquement en fonction de l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="d9e77-232">Optional: Group-based licensing to automatically assign and remove licenses to user accounts based on group membership</span></span>

<span data-ttu-id="d9e77-233">Vous [avez activé la gestion des licences par groupes](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal) pour les groupes de sécurité Azure AD appropriés afin que des licences pour Office 365 et EMS soient automatiquement attribuées ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="d9e77-233">You [enabled group-based licensing](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal) for the appropriate Azure AD security groups so that licenses for both Office 365 and EMS are automatically assigned or removed.</span></span>

<span data-ttu-id="d9e77-234">Si vous ignorez cette option, vous devez effectuer les opérations suivantes manuellement :</span><span class="sxs-lookup"><span data-stu-id="d9e77-234">If you skip this option, you must manually:</span></span>

- <span data-ttu-id="d9e77-235">Attribuer des licences aux nouveaux utilisateurs qui accèderont à Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="d9e77-235">Assign licenses to new users whom you intend to have access to Office 365 and EMS.</span></span>
- <span data-ttu-id="d9e77-236">Supprimer les licences des utilisateurs qui ne sont plus avec votre organisation ou n’ont pas accès à Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="d9e77-236">Remove licenses from users who are no longer with your organization or do not have access to Office 365 and EMS.</span></span>

<span data-ttu-id="d9e77-237">Si nécessaire, l’[Étape 6](identity-self-service-group-management.md#identity-group-license) peut vous aider avec cette option.</span><span class="sxs-lookup"><span data-stu-id="d9e77-237">If needed, [Step 6](identity-self-service-group-management.md#identity-group-license) can help you with this option.</span></span>

### <a name="how-to-test"></a><span data-ttu-id="d9e77-238">Procédure de test</span><span class="sxs-lookup"><span data-stu-id="d9e77-238">How to test</span></span>

1. <span data-ttu-id="d9e77-239">Créez un groupe de sécurité test dans Azure AD avec le portail Azure et configurez la gestion des licences par groupes pour attribuer des licences Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="d9e77-239">Create a test security group in Azure AD with the Azure portal and configure group-based licensing to assign Office 365 and EMS licenses.</span></span>
2. <span data-ttu-id="d9e77-240">Créez un compte d’utilisateur test dans Azure AD et ajoutez-le au groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-240">Create a test user account in Azure AD and add it to the test security group.</span></span>
3. <span data-ttu-id="d9e77-241">Examinez les propriétés du compte d’utilisateur dans le portail d’administration Microsoft 365 pour vous assurer que les licences Office 365 et EMS lui ont été attribuées.</span><span class="sxs-lookup"><span data-stu-id="d9e77-241">Examine the properties of the user account in the Microsoft 365 admin center to ensure that it was assigned the Office 365 and EMS licenses.</span></span>
4. <span data-ttu-id="d9e77-242">Supprimez le compte d’utilisateur test du groupe de sécurité test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-242">Remove the test user account from the test security group.</span></span>
5. <span data-ttu-id="d9e77-243">Examinez les propriétés du compte d’utilisateur pour vous assurer que les licences Office 365 et EMS ne lui sont plus attribuées.</span><span class="sxs-lookup"><span data-stu-id="d9e77-243">Examine the properties of the user account to ensure that it no longer has the Office 365 and EMS licenses assigned.</span></span>
6. <span data-ttu-id="d9e77-244">Supprimez le groupe de sécurité test et le compte d’utilisateur test.</span><span class="sxs-lookup"><span data-stu-id="d9e77-244">Delete the test security group and the test user account.</span></span>

## <a name="results-and-next-steps"></a><span data-ttu-id="d9e77-245">Résultats et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d9e77-245">Results and next steps</span></span>

<span data-ttu-id="d9e77-246">Votre infrastructure d’identité dans le cloud de Microsoft 365 utilise l’authentification forte, comptes administrateur protégés et l’accès et gestion utilisateur simplifiés.</span><span class="sxs-lookup"><span data-stu-id="d9e77-246">Your identity infrastructure in the Microsoft 365 cloud uses strong authentication, protected administrator accounts, and simplified user access and management.</span></span>

|||
|:-------|:-----|
|![](./media/deploy-foundation-infrastructure/win10enterprise_icon-small.png)| <span data-ttu-id="d9e77-247">Si vous suivez les phases suivantes dans le processus de déploiement de bout en bout pour Microsoft 365 Entreprise, la suivante est la [Windows 10 Entreprise](windows10-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="d9e77-247">If you're following the phases for the end-to-end deployment of Microsoft 365 Enterprise, your next phase is [Windows 10 Enterprise](windows10-infrastructure.md).</span></span> |

