---
title: 'Étape 1 : Créer et protéger vos comptes d’administrateur général'
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
description: Vos comptes d’administrateur général ont besoin d’un traitement spécial leur assurant une protection contre la compromission des informations d’identification.
ms.openlocfilehash: 27b76671581ebd2dac32304752a85f8a6f60ac98
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42067341"
---
# <a name="step-1-create-and-protect-your-global-admin-accounts"></a><span data-ttu-id="36b78-103">Étape 1 : Créer et protéger vos comptes d’administrateur général</span><span class="sxs-lookup"><span data-stu-id="36b78-103">Step 1: Create and protect your global admin accounts</span></span>

![Phase 2 - Identité](../media/deploy-foundation-infrastructure/identity_icon-small.png)

<a name="identity-global-admin"></a>
## <a name="protect-global-administrator-accounts"></a><span data-ttu-id="36b78-105">Protéger des comptes d’administrateur général</span><span class="sxs-lookup"><span data-stu-id="36b78-105">Protect global administrator accounts</span></span>

<span data-ttu-id="36b78-106">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="36b78-106">*This is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="36b78-107">Dans le cadre de cette section, vous allez contribuer à empêcher des attaques numériques dirigées contre votre organisation en vérifiant que vos comptes d’administrateur sont aussi sécurisés que possible.</span><span class="sxs-lookup"><span data-stu-id="36b78-107">In this section, you'll help prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible.</span></span> <span data-ttu-id="36b78-108">Pour ce faire, vous devez :</span><span class="sxs-lookup"><span data-stu-id="36b78-108">To do this, you must:</span></span>

- <span data-ttu-id="36b78-109">Créer plus d'un compte d'administrateur général dédié avec des [mot de passe forts](https://support.microsoft.com//help/4026406/microsoft-account-create-a-strong-password) et les utiliser uniquement en cas de nécessité.</span><span class="sxs-lookup"><span data-stu-id="36b78-109">Create more than one dedicated global administrator accounts with [strong passwords](https://support.microsoft.com//help/4026406/microsoft-account-create-a-strong-password) and use them only when necessary.</span></span>
- <span data-ttu-id="36b78-110">Effectuer des tâches d’administration quotidienne en attribuant des rôles d’administrateur spécifiques (par exemple, administrateur Exchange ou administrateur Mot de passe) aux comptes d’utilisateur de votre personnel informatique, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="36b78-110">Perform day-to-day administration by assigning specific administrator roles—such as Exchange administrator or Password administrator—to other dedicated accounts for those roles or user accounts of IT staff as needed.</span></span>

<span data-ttu-id="36b78-111">Pour vos comptes Administrateur général dédiés, vous devez aussi effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="36b78-111">For your dedicated global admin accounts, you must also:</span></span>

1. <span data-ttu-id="36b78-112">Testez les paramètres d'authentification multifacteur Azure (MFA) par compte utilisateur ou par accès conditionnel sur un compte utilisateur test pour vous assurer que l'authentification multifacteur fonctionne correctement et de manière prévisible.</span><span class="sxs-lookup"><span data-stu-id="36b78-112">Test per-user account or Conditional Access-based Azure Multi-Factor Authentication (MFA) settings on a test user account to ensure that MFA works correctly and predictably.</span></span> <span data-ttu-id="36b78-113">L’authentification multifacteur requiert une forme secondaire d’authentification, telle qu’un code de vérification envoyé à un smartphone.</span><span class="sxs-lookup"><span data-stu-id="36b78-113">MFA requires a secondary form of authentication, such as a verification code sent to a smart phone.</span></span>
2. <span data-ttu-id="36b78-114">Créez et activez une stratégie d'accès conditionnel pour vos comptes d'administrateur général qui nécessite l'authentification multifacteur et utilise la forme d'authentification secondaire la plus efficace disponible au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="36b78-114">Create and enable a Conditional Access policy for your global administrator accounts that requires MFA and uses the strongest form of secondary authentication available in your organization.</span></span> <span data-ttu-id="36b78-115">Pour plus d’informations, consultez [Authentification multifacteur Azure](identity-access-prerequisites.md#protecting-administrator-accounts).</span><span class="sxs-lookup"><span data-stu-id="36b78-115">See [Azure Multi-Factor Authentication](identity-access-prerequisites.md#protecting-administrator-accounts) for more information.</span></span>

<span data-ttu-id="36b78-116">Pour des protections supplémentaires, consultez [Protéger vos comptes d’administrateur général Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts#additional-protections-for-enterprise-organizations).</span><span class="sxs-lookup"><span data-stu-id="36b78-116">See [Protect your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts#additional-protections-for-enterprise-organizations) for additional protections.</span></span>

> [!Note]
> <span data-ttu-id="36b78-117">Les comptes d'urgence pour les scénarios catastrophes en cas d'urgence, telle une cyberattaque, devraient être des comptes de Cloud uniquement.</span><span class="sxs-lookup"><span data-stu-id="36b78-117">Emergency accounts for break-glass scenarios in emergencies such as a cyberattack should be cloud-only accounts.</span></span> <span data-ttu-id="36b78-118">Vous pouvez également disposer de comptes d’administrateur général (éligibles ou permanents) qui ne sont pas uniquement dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="36b78-118">You may also have global administrator accounts (eligible or permanent) that are not cloud-only.</span></span> <span data-ttu-id="36b78-119">Pour plus d’informations, consultez [Gestion des comptes d’administration de l’accès d’urgence dans Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-emergency-access).</span><span class="sxs-lookup"><span data-stu-id="36b78-119">For more information, see [Manage emergency-access administrative accounts in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-emergency-access).</span></span>

<span data-ttu-id="36b78-120">Les résultats de cette section sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="36b78-120">The results of this section are:</span></span>

- <span data-ttu-id="36b78-121">Les seuls comptes d’utilisateurs de votre abonnement dotés du rôle Administrateur général sont les comptes Administrateur général dédiés.</span><span class="sxs-lookup"><span data-stu-id="36b78-121">The only user accounts in your subscription that have the global admin role are the dedicated global administrator accounts.</span></span> <span data-ttu-id="36b78-122">Pour le vérifier, utilisez la commande Azure Active Directory PowerShell pour Graph suivante :</span><span class="sxs-lookup"><span data-stu-id="36b78-122">Verify this with the following Azure Active Directory PowerShell for Graph command:</span></span> 
  ```powershell
  Get-AzureADDirectoryRole | Where { $_.DisplayName -eq "Company Administrator" } | Get-AzureADDirectoryRoleMember | Ft DisplayName
  ```
- <span data-ttu-id="36b78-123">Tous les autres comptes d’utilisateurs qui gèrent les services de votre abonnement ont des rôles d’administrateur associés à leurs responsabilités.</span><span class="sxs-lookup"><span data-stu-id="36b78-123">All other user accounts that manage your subscription services have admin roles assigned that are associated with their job responsibilities.</span></span>

> [!Note]
> <span data-ttu-id="36b78-124">Reportez-vous à [Se connecter à Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) pour obtenir des instructions sur l’installation du module Azure AD PowerShell pour Graph et la connexion.</span><span class="sxs-lookup"><span data-stu-id="36b78-124">See [Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) for instructions on installing the Azure Active Directory PowerShell for Graph module and signing in.</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)|  <span data-ttu-id="36b78-126">Pour tester cette configuration dans un environnement de laboratoire de test, consultez le [Guide de laboratoire de test Protéger des comptes d’administrateur général](protect-global-administrator-accounts-microsoft-365-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="36b78-126">To practice this configuration in a test lab environment, see the [Protect global administrator accounts Test Lab Guide](protect-global-administrator-accounts-microsoft-365-test-environment.md).</span></span> |
|||

<span data-ttu-id="36b78-127">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-global-admin) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="36b78-127">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-global-admin) for this section.</span></span>


<a name="identity-pim"></a>
## <a name="set-up-on-demand-administrators"></a><span data-ttu-id="36b78-128">Configurer des administrateurs à la demande</span><span class="sxs-lookup"><span data-stu-id="36b78-128">Set up on-demand administrators</span></span>

<span data-ttu-id="36b78-129">*Cette étape est facultative et s’applique uniquement à la version E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="36b78-129">*This is optional and applies only to the E5 version of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="36b78-130">Dans cette section, vous allez configurer Azure AD Privileged Identity Management (PIM) afin de réduire la durée pendant laquelle vos comptes d’administrateur général sont vulnérables aux attaques d’utilisateurs malveillants.</span><span class="sxs-lookup"><span data-stu-id="36b78-130">In this section, you'll set up Azure AD Privileged Identity Management (PIM) to reduce the amount of time that your administrator accounts are vulnerable to attack by malicious users.</span></span> <span data-ttu-id="36b78-131">PIM assure une attribution à la demande, juste-à-temps des rôles d’administrateur général en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="36b78-131">PIM provides on-demand, just-in-time assignment of the administrator roles when needed.</span></span>  

<span data-ttu-id="36b78-132">Au lieu d'être des administrateurs permanents, vos comptes d'administrateur deviennent des administrateurs admissibles.</span><span class="sxs-lookup"><span data-stu-id="36b78-132">Instead of your administrator accounts being permanent admins, they become eligible admins.</span></span> <span data-ttu-id="36b78-133">Le rôle d'administrateur est inactif tant que vous n'en avez pas besoin.</span><span class="sxs-lookup"><span data-stu-id="36b78-133">The administrator role is inactive until someone needs it.</span></span> <span data-ttu-id="36b78-134">Vous devez ensuite effectuer un processus d’activation pour ajouter le rôle d’administrateur au compte d’administrateur pour une durée spécifique.</span><span class="sxs-lookup"><span data-stu-id="36b78-134">You'll then complete an activation process to add the administrator role to the administrator account for a specific amount of time.</span></span> <span data-ttu-id="36b78-135">Une fois l’expiration du délai écoulée, PIM supprime le rôle d’administrateur du compte d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="36b78-135">When the time expires, PIM removes the administrator role from the administrator account.</span></span>

<span data-ttu-id="36b78-136">PIM est disponible avec Azure Active Directory Premium P2, qui est inclus avec Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="36b78-136">PIM is available with Azure Active Directory Premium P2, which is included with Microsoft 365 E5.</span></span> <span data-ttu-id="36b78-137">Vous pouvez également acheter des licences Azure Active Directory Premium P2 individuelles pour vos comptes d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="36b78-137">Alternately, you can purchase individual Azure Active Directory Premium P2 licenses for your administrator accounts.</span></span>

<span data-ttu-id="36b78-138">Pour activer Azure PIM pour votre client Azure AD et vos comptes d’administrateur, consultez les [étapes de configuration de PIM](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).</span><span class="sxs-lookup"><span data-stu-id="36b78-138">To enable Azure PIM for your Azure AD tenant and administrator accounts, see the [steps to configure PIM](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).</span></span>

<span data-ttu-id="36b78-139">Reportez-vous à la rubrique [Sécurisation de l’accès privilégié pour les déploiements hybrides et cloud dans Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) pour développer une feuille de route détaillée qui sécurise l’accès privilégié contre les cyber-attaquants.</span><span class="sxs-lookup"><span data-stu-id="36b78-139">To develop a comprehensive roadmap to secure privileged access against cyber attackers, see [Securing privileged access for hybrid and cloud deployments in Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices).</span></span>

<span data-ttu-id="36b78-140">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-pim) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="36b78-140">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-pim) for this section.</span></span>


<a name="identity-pam"></a>
## <a name="privileged-access-management"></a><span data-ttu-id="36b78-141">Gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="36b78-141">Privileged access management</span></span>

<span data-ttu-id="36b78-p109">Vous activez la gestion des accès privilégiés en configurant des stratégies qui indiquent l’accès juste-à-temps pour les activités basées sur des tâches dans votre client Office 365. Elle peut vous aider à protéger votre organisation contre les violations qui pourraient survenir par le biais de comptes d’administrateur privilégiés existants qui donnent un accès permanent à des données sensibles ou à des paramètres de configuration critiques. Par exemple, vous pouvez configurer une stratégie de gestion des accès privilégiés qui requiert une approbation explicite pour pouvoir accéder aux paramètres de boîte aux lettres de votre organisation dans votre client Office 365 et les modifier.</span><span class="sxs-lookup"><span data-stu-id="36b78-p109">Privileged access management is enabled by configuring policies that specify just-in-time access for task-based activities in your Office 365 tenant. It can help protect your organization from breaches that may use existing privileged administrator accounts with standing access to sensitive data or access to critical configuration settings. For example, you could configure a privileged access management policy that requires explicit approval to access and change organization mailbox settings in your Office 365 tenant.</span></span>

<span data-ttu-id="36b78-p110">Pour cette étape, vous allez activer la gestion des accès privilégiés dans votre client Office 365 et configurer les stratégies d’accès privilégiés qui permettent de renforcer la sécurité des accès basés sur les tâches à vos paramètres de configuration et à vos données Office 365 pour votre organisation. Il existe trois étapes simples pour commencer à utiliser les accès privilégiés dans votre organisation Office 365 :</span><span class="sxs-lookup"><span data-stu-id="36b78-p110">In this step, you'll enable privileged access management in your Office 365 tenant and configure privileged access policies that provide additional security for task-based access to Office 365 data and configuration settings for your organization. There are three basic steps to get started with privileged access in your Office 365 organization:</span></span>

- <span data-ttu-id="36b78-147">Création d’un groupe d’approbateurs</span><span class="sxs-lookup"><span data-stu-id="36b78-147">Creating an approver's group</span></span>
- <span data-ttu-id="36b78-148">Activation des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="36b78-148">Enabling privileged access</span></span>
- <span data-ttu-id="36b78-149">Création de stratégies d’approbation</span><span class="sxs-lookup"><span data-stu-id="36b78-149">Creating approval policies</span></span>

<span data-ttu-id="36b78-p111">Une fois configurée, la gestion des accès privilégiés permettra à votre organisation de fonctionner sans aucun privilège permanent et de fournir une sécurité renforcée contre les lacunes d’un accès administratif permanent comme celui-ci. L’accès privilégié requiert des approbations pour exécuter toute tâche pour laquelle une stratégie d’approbation associée a été définie. Les utilisateurs ayant besoin d’exécuter des tâches incluses dans la stratégie d’approbation doivent demander l’approbation de l’accès et l’obtenir afin de disposer des autorisations nécessaires pour exécuter les tâches définies dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="36b78-p111">One configured, privileged access management will enable your organization to operate with zero standing privileges and provide a layer of defense against vulnerabilities arising because of such standing administrative access. Privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute tasks defined in the policy.</span></span>

<span data-ttu-id="36b78-153">Pour activer la gestion des accès privilégiés d’Office 365, consultez la rubrique relative à la [configuration de la gestion des accès privilégiés dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration).</span><span class="sxs-lookup"><span data-stu-id="36b78-153">To enable Office 365 privileged access management, see the [Configure privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) topic.</span></span>

<span data-ttu-id="36b78-154">Pour plus d’informations, reportez-vous à la rubrique relative à la [gestion des accès privilégiés dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-overview).</span><span class="sxs-lookup"><span data-stu-id="36b78-154">For more information, see the [Privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-overview) topic.</span></span>


|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)|  <span data-ttu-id="36b78-156">Pour tester cette configuration dans un environnement de laboratoire de test, consultez le [Guide de laboratoire de test Gestion des accès privilégiés](privileged-access-microsoft-365-enterprise-dev-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="36b78-156">To practice this configuration in a test lab environment, see the [Privileged access management Test Lab Guide](privileged-access-microsoft-365-enterprise-dev-test-environment.md).</span></span> |
|||

<span data-ttu-id="36b78-157">Comme point de contrôle intermédiaire, consultez les [critères de sortie](identity-exit-criteria.md#crit-identity-pam) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="36b78-157">As an interim checkpoint, see the [exit criteria](identity-exit-criteria.md#crit-identity-pam) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="36b78-158">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="36b78-158">Next step</span></span>

|||
|:-------|:-----|
|![Étape 2](../media/stepnumbers/Step2.png)| [<span data-ttu-id="36b78-160">Sécuriser vos mots de passe</span><span class="sxs-lookup"><span data-stu-id="36b78-160">Secure your passwords</span></span>](identity-secure-your-passwords.md) |

