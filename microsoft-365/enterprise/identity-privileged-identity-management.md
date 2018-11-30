---
title: 'Étape 3 : Configurer des administrateurs généraux à la demande'
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
description: Comprenez et configurez Azure AD Privileged Identity Management.
ms.openlocfilehash: 659beff3c31d17afa03d3ecf754c581f3ca2e230
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867030"
---
# <a name="step-3-set-up-on-demand-global-administrators"></a><span data-ttu-id="a000d-103">Étape 3 : Configurer des administrateurs généraux à la demande</span><span class="sxs-lookup"><span data-stu-id="a000d-103">Step 3: Set up on-demand global administrators</span></span>

<span data-ttu-id="a000d-104">*Cette étape est facultative et s’applique uniquement à la version E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="a000d-104">*This step is optional and applies only to the E5 version of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="a000d-p101">Dans cette étape, vous configurerez Azure AD Privileged Identity Management (PIM) afin de réduire la durée pendant laquelle vos comptes d’administrateur général sont vulnérables aux attaques d’utilisateurs malveillants. PIM fournit l’affectation du rôle Administrateur général à la demande, juste-à-temps, en cas de besoin.</span><span class="sxs-lookup"><span data-stu-id="a000d-p101">In this step, you'll set up Azure AD Privileged Identity Management (PIM) to reduce the amount of time that your global administrator accounts are vulnerable to attack by malicious users. PIM provides on-demand, just-in-time assignment of the global administrator role when needed.</span></span>  

<span data-ttu-id="a000d-p102">Au lieu que vos comptes d’administrateur général soient un administrateur permanent, ils deviennent des administrateurs éligibles. Le rôle Administrateur général est inactif tant que personne n’en a besoin. Vous effectuerez ensuite un processus d’activation pour ajouter le rôle Administrateur général au compte d’administrateur général pour une durée spécifique. À l’expiration du délai, PIM supprime le rôle Administrateur général du compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="a000d-p102">Instead of your global administrator accounts being a permanent admin, they become eligible admins. The global administrator role is inactive until someone needs it. You'll then complete an activation process to add the global administrator role to the global administrator account for a specific amount of time. When the time expires, PIM removes the global administrator role from the global administrator account.</span></span>

<span data-ttu-id="a000d-p103">PIM est disponible avec Azure Active Directory Premium P2, qui est inclus avec Microsoft 365 Entreprise E5. Vous pouvez également acheter des licences Azure Active Directory Premium P2 individuelles pour vos comptes d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="a000d-p103">PIM is available with Azure Active Directory Premium P2, which is included with Microsoft 365 Enterprise E5. Alternately, you can purchase individual Azure Active Directory Premium P2 licenses for your global administrator accounts.</span></span>

<span data-ttu-id="a000d-113">Pour activer Azure PIM pour votre client Azure AD et vos comptes d’administrateur général, consultez les [étapes de configuration de PIM](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).</span><span class="sxs-lookup"><span data-stu-id="a000d-113">To enable Azure PIM for your Azure AD tenant and global administrator accounts, see the [steps to configure PIM](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).</span></span>

<span data-ttu-id="a000d-114">Reportez-vous à la rubrique [Sécurisation de l’accès privilégié pour les déploiements hybrides et cloud dans Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices) pour développer une feuille de route détaillée qui sécurise l’accès privilégié contre les cyber-attaquants.</span><span class="sxs-lookup"><span data-stu-id="a000d-114">To develop a comprehensive roadmap to secure privileged access against cyber attackers, see [Securing privileged access for hybrid and cloud deployments in Azure AD](https://docs.microsoft.com/azure/active-directory/admin-roles-best-practices).</span></span>

<span data-ttu-id="a000d-115">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-pim) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="a000d-115">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-pim) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="a000d-116">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="a000d-116">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step4.png)| [<span data-ttu-id="a000d-117">Simplifier la réinitialisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="a000d-117">Simplify password resets</span></span>](identity-password-reset.md) |

