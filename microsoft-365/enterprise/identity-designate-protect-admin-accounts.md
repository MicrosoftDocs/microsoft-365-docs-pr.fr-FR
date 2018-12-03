---
title: 'Étape 2 : Protéger des comptes Administrateur général'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/01/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez vos comptes d’administrateur pour une protection maximale.
ms.openlocfilehash: ccab7c8526817ee5140a5315c56f6f8a42f085d2
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867476"
---
# <a name="step-2-protect-global-administrator-accounts"></a><span data-ttu-id="297e5-103">Étape 2 : Protéger des comptes Administrateur général</span><span class="sxs-lookup"><span data-stu-id="297e5-103">Step 2: Protect global administrator accounts</span></span>

<span data-ttu-id="297e5-104">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="297e5-104">*This step is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="297e5-p101">Lors de cette étape, vous aiderez à empêcher des attaques numériques dans votre organisation en vérifiant que vos comptes d’administrateur sont aussi sécurisés que possible. Pour ce faire, vous devez :</span><span class="sxs-lookup"><span data-stu-id="297e5-p101">In Step 5, you'll help prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible. To do this, you must:</span></span>

- <span data-ttu-id="297e5-107">créer des comptes Administrateur général dédiés avec des [mot de passe très forts](https://support.microsoft.com//help/4026406/microsoft-account-create-a-strong-password) et les utiliser uniquement en cas de nécessité ;</span><span class="sxs-lookup"><span data-stu-id="297e5-107">Create dedicated global administrator accounts with very [strong passwords](https://support.microsoft.com//help/4026406/microsoft-account-create-a-strong-password) and use them only when necessary.</span></span>
- <span data-ttu-id="297e5-108">effectuer des tâches d’administration quotidienne en attribuant des rôles d’administrateur spécifiques (par exemple, administrateur Exchange ou administrateur de mots de passe) aux comptes d’utilisateur de votre personnel informatique, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="297e5-108">Perform day-to-day administration by assigning specific administrator roles—such as Exchange administrator or Password administrator—to user accounts of IT staff as needed.</span></span>

<span data-ttu-id="297e5-109">Pour vos comptes Administrateur général dédiés, vous devez aussi effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="297e5-109">For your dedicated global admin accounts, you must also:</span></span>

1. <span data-ttu-id="297e5-p102">Testez les paramètres d’authentification multifacteur par compte d’utilisateur ou par accès conditionnel sur un compte d’utilisateur test afin de vérifier que l’authentification multifacteur fonctionne correctement et de manière prévisible. L’authentification multifacteur nécessite une forme secondaire d’authentification (par exemple, un code de vérification envoyé à un smartphone).</span><span class="sxs-lookup"><span data-stu-id="297e5-p102">Test per-user account or conditional access-based multi-factor authentication (MFA) settings on a test user account to ensure that MFA works correctly and predictably. MFA requires a secondary form of authentication, such as a verification code sent to a smart phone.</span></span>
2. <span data-ttu-id="297e5-p103">Configurez l’authentification multifacteur pour chacun des comptes Administrateur général d’Office 365 dédiés et utilisez la forme d’authentification secondaire disponible la plus forte dans votre organisation. Reportez-vous à la rubrique relative à l’[authentification multifacteur](identity-multi-factor-authentication.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="297e5-p103">Configure MFA for each of the dedicated Office 365 global administrator accounts, and use the strongest form of secondary authentication available in your organization. See [Multi-factor authentication](identity-multi-factor-authentication.md) for more information.</span></span>
2. <span data-ttu-id="297e5-p104">Utiliser une stratégie d’accès conditionnel pour exiger l’authentification multifacteur pour les comptes d’administrateur général. Voir [Protection des comptes d’administrateur](identity-access-prerequisites.md#protecting-administrator-accounts) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="297e5-p104">Use a conditional access policy to require MFA for global administrator accounts. See [Protecting administrator accounts](identity-access-prerequisites.md#protecting-administrator-accounts) for more information.</span></span>
4. <span data-ttu-id="297e5-p105">Utiliser une stratégie Office 365 Cloud App Security pour surveiller l’activité du compte Administrateur général. Reportez-vous à la rubrique [Configurez une sécurité accrue pour Office 365](infoprotect-configure-increased-security-office-365.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="297e5-p105">Use an Office 365 Cloud App Security policy to monitor global administrator account activity. See [Information protection for Microsoft 365 Enterprise](infoprotect-configure-increased-security-office-365.md) for more information.</span></span>

<span data-ttu-id="297e5-118">Reportez-vous à la rubrique [Protéger vos comptes d’administrateur général Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts) pour plus d’informations sur la configuration.</span><span class="sxs-lookup"><span data-stu-id="297e5-118">See [Protect your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts) for more information about configuration.</span></span>

> [!Note]
> <span data-ttu-id="297e5-p106">Les organisations doivent utiliser des identités exclusivement cloud pour créer des comptes privilégiés (par exemple, administrateurs généraux pour les scénarios d’accès en situation d’urgence comme une cyber-attaque). Pour plus d’informations, voir [Gérer les comptes d’administration d’urgence dans Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-emergency-access).</span><span class="sxs-lookup"><span data-stu-id="297e5-p106">Organizations should use cloud-only identities to create privileged accounts, such as global administrators, for break-glass scenarios in emergencies, such as a cyberattack. For more information, see [Manage emergency-access administrative accounts in Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-emergency-access).</span></span>

<span data-ttu-id="297e5-121">Les résultats de cette étape sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="297e5-121">The results of this step are:</span></span>

- <span data-ttu-id="297e5-p107">Les seuls comptes d’utilisateur dans votre abonnement dotés du rôle Administrateur général sont le nouvel ensemble de comptes Administrateur général dédiés. Vérifiez cela avec la commande PowerShell Windows Azure AD V2 suivante :</span><span class="sxs-lookup"><span data-stu-id="297e5-p107">The only user accounts in your subscription that have the global admin role are the new set of dedicated global administrator accounts. Verify this with the following Windows Azure AD V2 PowerShell command:</span></span> 
  ```
  Get-AzureADDirectoryRole | Where { $_.DisplayName -eq "Company Administrator" } | Get-AzureADDirectoryRoleMember | Ft DisplayName
  ```
- <span data-ttu-id="297e5-124">Tous les autres comptes d’utilisateur qui gèrent votre abonnement quotidiennement ont des rôles d’administrateur qui sont associés à leurs responsabilités.</span><span class="sxs-lookup"><span data-stu-id="297e5-124">All other everyday user accounts that manage your subscription have admin roles assigned that are associated with their job responsibilities.</span></span>

> [!Note]
> <span data-ttu-id="297e5-125">Reportez-vous à [Se connecter à Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) pour obtenir des instructions sur l’installation du module Azure AD V2 PowerShell et la connexion.</span><span class="sxs-lookup"><span data-stu-id="297e5-125">See [Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell) for instructions on installing the Azure AD V2 PowerShell module and signing in.</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="297e5-127">Guide du laboratoire de test : protéger des comptes Administrateur général</span><span class="sxs-lookup"><span data-stu-id="297e5-127">Test Lab Guide: Protect global administrator accounts</span></span>](protect-global-administrator-accounts-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="297e5-128">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-global-admin) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="297e5-128">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-global-admin) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="297e5-129">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="297e5-129">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step3.png)| [<span data-ttu-id="297e5-130">Configurez des administrateurs généraux à la demande</span><span class="sxs-lookup"><span data-stu-id="297e5-130">Set up on-demand global administrators</span></span>](identity-privileged-identity-management.md) |

