---
title: 'Étape 2 : sécuriser vos identités privilégiées'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/01/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez vos comptes d’administrateur pour une protection maximale.
ms.openlocfilehash: 4b4a8d01cdf71e30139fa448813a3ff7c43855c7
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285156"
---
# <a name="step-2-secure-your-privileged-identities"></a><span data-ttu-id="03118-103">Étape 2 : sécuriser vos identités privilégiées</span><span class="sxs-lookup"><span data-stu-id="03118-103">Step 2: Secure your privileged identities</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<a name="identity-global-admin"></a>
## <a name="protect-global-administrator-accounts"></a><span data-ttu-id="03118-104">Protéger des comptes d’administrateur général</span><span class="sxs-lookup"><span data-stu-id="03118-104">Protect global administrator accounts</span></span>

<span data-ttu-id="03118-105">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="03118-105">*This step is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="03118-106">Dans le cadre de cette section, vous allez contribuer à empêcher des attaques numériques dirigées contre votre organisation en vérifiant que vos comptes d’administrateur sont aussi sécurisés que possible.</span><span class="sxs-lookup"><span data-stu-id="03118-106">In this step, you'll help prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible. To do this, you must:</span></span> <span data-ttu-id="03118-107">Pour ce faire, vous devez :</span><span class="sxs-lookup"><span data-stu-id="03118-107">To do this, you must:</span></span>

- <span data-ttu-id="03118-108">créer des comptes Administrateur général dédiés avec des [mot de passe très forts](https://support.microsoft.com//help/4026406/microsoft-account-create-a-strong-password) et les utiliser uniquement en cas de nécessité ;</span><span class="sxs-lookup"><span data-stu-id="03118-108">Create dedicated global administrator accounts with very [strong passwords](https://support.microsoft.com//help/4026406/microsoft-account-create-a-strong-password) and use them only when necessary.</span></span>
- <span data-ttu-id="03118-109">effectuer des tâches d’administration quotidienne en attribuant des rôles d’administrateur spécifiques (par exemple, administrateur Exchange ou administrateur de mots de passe) aux comptes d’utilisateur de votre personnel informatique, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="03118-109">Perform day-to-day administration by assigning specific administrator roles—such as Exchange administrator or Password administrator—to user accounts of IT staff as needed.</span></span>

<span data-ttu-id="03118-110">Pour vos comptes Administrateur général dédiés, vous devez aussi effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="03118-110">For your dedicated global admin accounts, you must also:</span></span>

1. <span data-ttu-id="03118-p102">Testez les paramètres d’authentification multifacteur par compte d’utilisateur ou par accès conditionnel sur un compte d’utilisateur test afin de vérifier que l’authentification multifacteur fonctionne correctement et de manière prévisible. L’authentification multifacteur nécessite une forme secondaire d’authentification (par exemple, un code de vérification envoyé à un smartphone).</span><span class="sxs-lookup"><span data-stu-id="03118-p102">Test per-user account or conditional access-based multi-factor authentication (MFA) settings on a test user account to ensure that MFA works correctly and predictably. MFA requires a secondary form of authentication, such as a verification code sent to a smart phone.</span></span>
2. <span data-ttu-id="03118-p103">Configurez l’authentification multifacteur pour chacun des comptes Administrateur général d’Office 365 dédiés et utilisez la forme d’authentification secondaire disponible la plus forte dans votre organisation. Reportez-vous à la rubrique relative à l’[authentification multifacteur](identity-multi-factor-authentication.md#identity-mfa) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="03118-p103">Configure MFA for each of the dedicated Office 365 global administrator accounts, and use the strongest form of secondary authentication available in your organization. See [Multi-factor authentication](identity-multi-factor-authentication.md#identity-mfa) for more information.</span></span>
2. <span data-ttu-id="03118-p104">Utiliser une stratégie d’accès conditionnel pour exiger l’authentification multifacteur pour les comptes d’administrateur général. Voir [Protection des comptes d’administrateur](identity-access-prerequisites.md#protecting-administrator-accounts) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="03118-p104">Use a conditional access policy to require MFA for global administrator accounts. See [Protecting administrator accounts](identity-access-prerequisites.md#protecting-administrator-accounts) for more information.</span></span>
4. <span data-ttu-id="03118-p105">Utiliser une stratégie Office 365 Cloud App Security pour surveiller l’activité du compte Administrateur général. Reportez-vous à la rubrique [Configurez une sécurité accrue pour Office 365](infoprotect-configure-increased-security-office-365.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="03118-p105">Use an Office 365 Cloud App Security policy to monitor global administrator account activity. See [Configure increased security for Office 365](infoprotect-configure-increased-security-office-365.md) for more information.</span></span>

<span data-ttu-id="03118-119">Reportez-vous à la rubrique [Protéger vos comptes d’administrateur général Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts) pour plus d’informations sur la configuration.</span><span class="sxs-lookup"><span data-stu-id="03118-119">See [Protect your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts) for more information about configuration.</span></span>

> [!Note]
> <span data-ttu-id="03118-p106">Les organisations doivent utiliser des identités exclusivement cloud pour créer des comptes privilégiés (par exemple, administrateurs généraux pour les scénarios d’accès en situation d’urgence comme une cyber-attaque). Pour plus d’informations, voir [Gérer les comptes d’administration d’urgence dans Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-emergency-access).</span><span class="sxs-lookup"><span data-stu-id="03118-p106">Organizations should use cloud-only identities to create privileged accounts, such as global administrators, for break-glass scenarios in emergencies, such as a cyberattack. For more information, see [Manage emergency-access administrative accounts in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-emergency-access).</span></span>

<span data-ttu-id="03118-122">Les résultats de cette section sont :</span><span class="sxs-lookup"><span data-stu-id="03118-122">The results of this step are:</span></span>

- <span data-ttu-id="03118-123">Les seuls comptes d’utilisateurs de votre abonnement dotés du rôle Administrateur général sont les comptes du nouvel ensemble de comptes Administrateur général dédiés.</span><span class="sxs-lookup"><span data-stu-id="03118-123">The only user accounts in your subscription that have the global admin role are the new set of dedicated global administrator accounts. Verify this with the following Windows Azure AD V2 PowerShell command:</span></span> <span data-ttu-id="03118-124">Vérifiez cela avec la commande Azure Active Directory PowerShell pour Graph suivante :</span><span class="sxs-lookup"><span data-stu-id="03118-124">Verify this with the following Azure Active Directory PowerShell for Graph command:</span></span> 
  ```
  Get-AzureADDirectoryRole | Where { $_.DisplayName -eq "Company Administrator" } | Get-AzureADDirectoryRoleMember | Ft DisplayName
  ```
- <span data-ttu-id="03118-125">Tous les autres comptes d’utilisateurs qui gèrent votre abonnement quotidiennement ont des rôles d’administrateur associés à leurs responsabilités.</span><span class="sxs-lookup"><span data-stu-id="03118-125">All other everyday user accounts that manage your subscription have admin roles assigned that are associated with their job responsibilities.</span></span>

> [!Note]
> <span data-ttu-id="03118-126">Reportez-vous à [Se connecter à Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) pour obtenir des instructions sur l’installation du module Azure AD PowerShell pour Graph et la connexion.</span><span class="sxs-lookup"><span data-stu-id="03118-126">See [Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) for instructions on installing the Azure AD V2 PowerShell module and signing in.</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="03118-128">Guide du laboratoire de test : protéger des comptes Administrateur général</span><span class="sxs-lookup"><span data-stu-id="03118-128">Test Lab Guide: Protect global administrator accounts</span></span>](protect-global-administrator-accounts-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="03118-129">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-global-admin) pour cette section.</span><span class="sxs-lookup"><span data-stu-id="03118-129">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-global-admin) for this step.</span></span>


<a name="identity-pim"></a>
## <a name="set-up-on-demand-global-administrators"></a><span data-ttu-id="03118-130">Configurer des administrateurs généraux à la demande</span><span class="sxs-lookup"><span data-stu-id="03118-130">Set up on-demand global administrators</span></span>

<span data-ttu-id="03118-131">*Cette étape est facultative et s’applique uniquement à la version E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="03118-131">*This step is optional and applies only to the E5 version of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="03118-132">Dans le cadre de cette section, vous allez configurer Azure AD Privileged Identity Management (PIM) afin de réduire la durée pendant laquelle vos comptes d’administrateur général sont vulnérables aux attaques d’utilisateurs malveillants.</span><span class="sxs-lookup"><span data-stu-id="03118-132">In this step, you'll set up Azure AD Privileged Identity Management (PIM) to reduce the amount of time that your global administrator accounts are vulnerable to attack by malicious users. PIM provides on-demand, just-in-time assignment of the global administrator role when needed.</span></span> <span data-ttu-id="03118-133">PIM assure une affectation à la demande, juste-à-temps du rôle d’administrateur général en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="03118-133">PIM provides on-demand, just-in-time assignment of the global administrator role when needed.</span></span>  

<span data-ttu-id="03118-p109">Au lieu que vos comptes d’administrateur général soient un administrateur permanent, ils deviennent des administrateurs éligibles. Le rôle Administrateur général est inactif tant que personne n’en a besoin. Vous effectuerez ensuite un processus d’activation pour ajouter le rôle Administrateur général au compte d’administrateur général pour une durée spécifique. À l’expiration du délai, PIM supprime le rôle Administrateur général du compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="03118-p109">Instead of your global administrator accounts being a permanent admin, they become eligible admins. The global administrator role is inactive until someone needs it. You'll then complete an activation process to add the global administrator role to the global administrator account for a specific amount of time. When the time expires, PIM removes the global administrator role from the global administrator account.</span></span>

<span data-ttu-id="03118-p110">PIM est disponible avec Azure Active Directory Premium P2, qui est inclus avec Microsoft 365 Entreprise E5. Vous pouvez également acheter des licences Azure Active Directory Premium P2 individuelles pour vos comptes d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="03118-p110">PIM is available with Azure Active Directory Premium P2, which is included with Microsoft 365 Enterprise E5. Alternately, you can purchase individual Azure Active Directory Premium P2 licenses for your global administrator accounts.</span></span>

<span data-ttu-id="03118-140">Pour activer Azure PIM pour votre client Azure AD et vos comptes d’administrateur général, consultez les [étapes de configuration de PIM](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).</span><span class="sxs-lookup"><span data-stu-id="03118-140">To enable Azure PIM for your Azure AD tenant and global administrator accounts, see the [steps to configure PIM](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).</span></span>

<span data-ttu-id="03118-141">Reportez-vous à la rubrique [Sécurisation de l’accès privilégié pour les déploiements hybrides et cloud dans Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) pour développer une feuille de route détaillée qui sécurise l’accès privilégié contre les cyber-attaquants.</span><span class="sxs-lookup"><span data-stu-id="03118-141">To develop a comprehensive roadmap to secure privileged access against cyber attackers, see [Securing privileged access for hybrid and cloud deployments in Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices).</span></span>

<span data-ttu-id="03118-142">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-pim) pour cette section.</span><span class="sxs-lookup"><span data-stu-id="03118-142">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-pim) for this step.</span></span>


## <a name="next-step"></a><span data-ttu-id="03118-143">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="03118-143">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step3.png)| [<span data-ttu-id="03118-144">Configurer une identité hybride</span><span class="sxs-lookup"><span data-stu-id="03118-144">Configure hybrid identity</span></span>](identity-azure-ad-connect.md) |

