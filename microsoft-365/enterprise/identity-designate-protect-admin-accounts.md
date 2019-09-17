---
title: 'Étape 2 : sécuriser vos identités privilégiées'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/06/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez vos comptes d’administrateur pour une protection maximale.
ms.openlocfilehash: b9c645d597dfeb2bdc42e2b0b7615252dc1f5ecb
ms.sourcegitcommit: 91ff1d4339f0f043c2b43997d87d84677c79e279
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2019
ms.locfileid: "36981905"
---
# <a name="step-2-secure-your-privileged-identities"></a><span data-ttu-id="7ae96-103">Étape 2 : sécuriser vos identités privilégiées</span><span class="sxs-lookup"><span data-stu-id="7ae96-103">Step 2: Secure your privileged identities</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<a name="identity-global-admin"></a>
## <a name="protect-global-administrator-accounts"></a><span data-ttu-id="7ae96-104">Protéger des comptes d’administrateur général</span><span class="sxs-lookup"><span data-stu-id="7ae96-104">Protect global administrator accounts</span></span>

<span data-ttu-id="7ae96-105">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="7ae96-105">*This is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="7ae96-106">Dans le cadre de cette section, vous allez contribuer à empêcher des attaques numériques dirigées contre votre organisation en vérifiant que vos comptes d’administrateur sont aussi sécurisés que possible.</span><span class="sxs-lookup"><span data-stu-id="7ae96-106">In this section, you'll help prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible.</span></span> <span data-ttu-id="7ae96-107">Pour ce faire, vous devez :</span><span class="sxs-lookup"><span data-stu-id="7ae96-107">To do this, you must:</span></span>

- <span data-ttu-id="7ae96-108">créer des comptes Administrateur général dédiés avec des [mot de passe très forts](https://support.microsoft.com//help/4026406/microsoft-account-create-a-strong-password) et les utiliser uniquement en cas de nécessité ;</span><span class="sxs-lookup"><span data-stu-id="7ae96-108">Create dedicated global administrator accounts with very [strong passwords](https://support.microsoft.com//help/4026406/microsoft-account-create-a-strong-password) and use them only when necessary.</span></span>
- <span data-ttu-id="7ae96-109">effectuer des tâches d’administration quotidienne en attribuant des rôles d’administrateur spécifiques (par exemple, administrateur Exchange ou administrateur de mots de passe) aux comptes d’utilisateur de votre personnel informatique, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="7ae96-109">Perform day-to-day administration by assigning specific administrator roles—such as Exchange administrator or Password administrator—to user accounts of IT staff as needed.</span></span>

<span data-ttu-id="7ae96-110">Pour vos comptes Administrateur général dédiés, vous devez aussi effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ae96-110">For your dedicated global admin accounts, you must also:</span></span>

1. <span data-ttu-id="7ae96-p102">Testez les paramètres d’authentification multifacteur par compte d’utilisateur ou par accès conditionnel sur un compte d’utilisateur test afin de vérifier que l’authentification multifacteur fonctionne correctement et de manière prévisible. L’authentification multifacteur nécessite une forme secondaire d’authentification (par exemple, un code de vérification envoyé à un smartphone).</span><span class="sxs-lookup"><span data-stu-id="7ae96-p102">Test per-user account or conditional access-based multi-factor authentication (MFA) settings on a test user account to ensure that MFA works correctly and predictably. MFA requires a secondary form of authentication, such as a verification code sent to a smart phone.</span></span>
2. <span data-ttu-id="7ae96-113">Activez la stratégie d’accès conditionnel **Stratégie de référence: exiger l’authentification multifacteur pour les administrateurs** pour vos comptes d’administrateur général et utilisez la forme d’authentification secondaire la plus forte de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7ae96-113">Enable the **Baseline policy: Require MFA for admins** conditional access policy for your global administrator accounts and use the strongest form of secondary authentication available in your organization.</span></span> <span data-ttu-id="7ae96-114">Pour plus d’informations, consultez [Authentification multifacteur](identity-access-prerequisites.md#protecting-administrator-accounts).</span><span class="sxs-lookup"><span data-stu-id="7ae96-114">See [Multi-factor authentication](identity-access-prerequisites.md#protecting-administrator-accounts) for more information.</span></span>

<span data-ttu-id="7ae96-115">Pour des protections supplémentaires, consultez [Protéger vos comptes d’administrateur général Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts#additional-protections-for-enterprise-organizations).</span><span class="sxs-lookup"><span data-stu-id="7ae96-115">See [Protect your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts#additional-protections-for-enterprise-organizations) for more information about configuration.</span></span>

> [!Note]
> <span data-ttu-id="7ae96-p104">Les organisations doivent utiliser des identités exclusivement cloud pour créer des comptes privilégiés (par exemple, administrateurs généraux pour les scénarios d’accès en situation d’urgence comme une cyber-attaque). Pour plus d’informations, voir [Gérer les comptes d’administration d’urgence dans Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-emergency-access).</span><span class="sxs-lookup"><span data-stu-id="7ae96-p104">Organizations should use cloud-only identities to create privileged accounts, such as global administrators, for break-glass scenarios in emergencies, such as a cyberattack. For more information, see [Manage emergency-access administrative accounts in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-emergency-access).</span></span>

<span data-ttu-id="7ae96-118">Les résultats de cette section sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7ae96-118">The results of this section are:</span></span>

- <span data-ttu-id="7ae96-119">Les seuls comptes d’utilisateurs de votre abonnement dotés du rôle Administrateur général sont les comptes Administrateur général dédiés.</span><span class="sxs-lookup"><span data-stu-id="7ae96-119">The only user accounts in your subscription that have the global admin role are the new set of dedicated global administrator accounts.</span></span> <span data-ttu-id="7ae96-120">Pour le vérifier, utilisez la commande Azure Active Directory PowerShell pour Graph suivante :</span><span class="sxs-lookup"><span data-stu-id="7ae96-120">Verify this with the following Azure Active Directory PowerShell for Graph command:</span></span> 
  ```
  Get-AzureADDirectoryRole | Where { $_.DisplayName -eq "Company Administrator" } | Get-AzureADDirectoryRoleMember | Ft DisplayName
  ```
- <span data-ttu-id="7ae96-121">Tous les autres comptes d’utilisateurs qui gèrent les services de votre abonnement ont des rôles d’administrateur associés à leurs responsabilités.</span><span class="sxs-lookup"><span data-stu-id="7ae96-121">All other everyday user accounts that manage your subscription have admin roles assigned that are associated with their job responsibilities.</span></span>

> [!Note]
> <span data-ttu-id="7ae96-122">Reportez-vous à [Se connecter à Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) pour obtenir des instructions sur l’installation du module Azure AD PowerShell pour Graph et la connexion.</span><span class="sxs-lookup"><span data-stu-id="7ae96-122">See [Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) for instructions on installing the Azure Active Directory PowerShell for Graph module and signing in.</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)|  <span data-ttu-id="7ae96-124">Pour tester cette configuration dans un environnement de laboratoire de test, consultez le [Guide de laboratoire de test Protéger des comptes d’administrateur général](protect-global-administrator-accounts-microsoft-365-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7ae96-124">To practice this configuration in a test lab environment, see the [Protect global administrator accounts Test Lab Guide](protect-global-administrator-accounts-microsoft-365-test-environment.md).</span></span> |
|||

<span data-ttu-id="7ae96-125">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-global-admin) de cette section.</span><span class="sxs-lookup"><span data-stu-id="7ae96-125">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-global-admin) for this section.</span></span>


<a name="identity-pim"></a>
## <a name="set-up-on-demand-global-administrators"></a><span data-ttu-id="7ae96-126">Configurer des administrateurs généraux à la demande</span><span class="sxs-lookup"><span data-stu-id="7ae96-126">Set up on-demand global administrators</span></span>

<span data-ttu-id="7ae96-127">*Cette étape est facultative et s’applique uniquement à la version E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="7ae96-127">*This is optional and applies only to the E5 version of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="7ae96-128">Dans le cadre de cette section, vous allez configurer Azure AD Privileged Identity Management (PIM) afin de réduire la durée pendant laquelle vos comptes d’administrateur général sont vulnérables aux attaques d’utilisateurs malveillants.</span><span class="sxs-lookup"><span data-stu-id="7ae96-128">In this section, you'll set up Azure AD Privileged Identity Management (PIM) to reduce the amount of time that your global administrator accounts are vulnerable to attack by malicious users.</span></span> <span data-ttu-id="7ae96-129">PIM assure une affectation à la demande, juste-à-temps du rôle d’administrateur général en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="7ae96-129">PIM provides on-demand, just-in-time assignment of the global administrator role when needed.</span></span>  

<span data-ttu-id="7ae96-p107">Au lieu que vos comptes d’administrateur général soient un administrateur permanent, ils deviennent des administrateurs éligibles. Le rôle Administrateur général est inactif tant que personne n’en a besoin. Vous effectuerez ensuite un processus d’activation pour ajouter le rôle Administrateur général au compte d’administrateur général pour une durée spécifique. À l’expiration du délai, PIM supprime le rôle Administrateur général du compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="7ae96-p107">Instead of your global administrator accounts being a permanent admin, they become eligible admins. The global administrator role is inactive until someone needs it. You'll then complete an activation process to add the global administrator role to the global administrator account for a specific amount of time. When the time expires, PIM removes the global administrator role from the global administrator account.</span></span>

<span data-ttu-id="7ae96-p108">PIM est disponible avec Azure Active Directory Premium P2, qui est inclus avec Microsoft 365 Entreprise E5. Vous pouvez également acheter des licences Azure Active Directory Premium P2 individuelles pour vos comptes d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="7ae96-p108">PIM is available with Azure Active Directory Premium P2, which is included with Microsoft 365 Enterprise E5. Alternately, you can purchase individual Azure Active Directory Premium P2 licenses for your global administrator accounts.</span></span>

<span data-ttu-id="7ae96-136">Pour activer Azure PIM pour votre client Azure AD et vos comptes d’administrateur général, consultez les [étapes de configuration de PIM](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).</span><span class="sxs-lookup"><span data-stu-id="7ae96-136">To enable Azure PIM for your Azure AD tenant and global administrator accounts, see the [steps to configure PIM](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).</span></span>

<span data-ttu-id="7ae96-137">Reportez-vous à la rubrique [Sécurisation de l’accès privilégié pour les déploiements hybrides et cloud dans Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) pour développer une feuille de route détaillée qui sécurise l’accès privilégié contre les cyber-attaquants.</span><span class="sxs-lookup"><span data-stu-id="7ae96-137">To develop a comprehensive roadmap to secure privileged access against cyber attackers, see [Securing privileged access for hybrid and cloud deployments in Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices).</span></span>

<span data-ttu-id="7ae96-138">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-pim) pour cette section.</span><span class="sxs-lookup"><span data-stu-id="7ae96-138">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-pim) for this section.</span></span>


## <a name="next-step"></a><span data-ttu-id="7ae96-139">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="7ae96-139">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step3.png)| [<span data-ttu-id="7ae96-140">Configurer une identité hybride</span><span class="sxs-lookup"><span data-stu-id="7ae96-140">Configure hybrid identity</span></span>](identity-azure-ad-connect.md) |

