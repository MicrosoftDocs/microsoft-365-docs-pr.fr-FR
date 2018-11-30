---
title: 'Étape 14 : permettre aux utilisateurs de créer et de gérer leurs propres groupes'
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
description: Comprendre et configurer la gestion des groupes en libre-service Azure AD.
ms.openlocfilehash: d46e82fd72b8eef896a223229a2cc3d25ae56c76
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867168"
---
# <a name="step-14-allow-users-to-create-and-manage-their-own-groups"></a><span data-ttu-id="524b8-103">Étape 14 : permettre aux utilisateurs de créer et de gérer leurs propres groupes</span><span class="sxs-lookup"><span data-stu-id="524b8-103">Step 14: Allow users to create and manage their own groups</span></span>

<span data-ttu-id="524b8-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="524b8-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="524b8-p101">Dans cette étape, vous allez identifier des groupes Azure Active Directory (AD) qui peuvent être gérés par des propriétaires de groupe et non par les administrateurs informatiques. Appelée *gestion des groupes en libre-service*, cette fonctionnalité permet aux propriétaires de groupe non désignés comme administrateurs de créer et de gérer des groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="524b8-p101">In Step 14, you'll identify Azure Active Directory (AD) groups that can be managed by group owners instead of IT administrators. Known as *self-service group management*, this feature allows group owners who are not assigned an administrative role to create and manage security groups.</span></span> 

<span data-ttu-id="524b8-p102">Les utilisateurs peuvent demander à appartenir à un groupe de sécurité. Cette demande est envoyée au propriétaire du groupe, et non à l’administrateur informatique. Ainsi, le contrôle quotidien de l’appartenance au groupe peut être délégué aux propriétaires d’équipes, de projets ou d’entreprises qui comprennent l’usage du groupe pour l’entreprise et peuvent gérer ses membres.</span><span class="sxs-lookup"><span data-stu-id="524b8-p102">Users can request membership in a security group and that request goes to the group owner, rather than an IT administrator. This allows the day-to-day control of group membership to be delegated to team, project, or business owners who understand the business use for the group and can manage its membership.</span></span>

>[!Note]
><span data-ttu-id="524b8-p103">La gestion des groupes en libre-service est disponible uniquement pour la sécurité Azure AD et les groupes Office 365. Cette fonction n’est pas disponible pour les groupes à extension messagerie, les listes de distribution ou les groupes ayant été synchronisés à partir de votre instance Windows Server Active Directory (AD) locale.</span><span class="sxs-lookup"><span data-stu-id="524b8-p103">Self-service group management is available only for Azure AD security and Office 365 groups. It is not available for mail-enabled groups, distribution lists, or any group that has been synchronized from your on-premises Windows Server Active Directory (AD).</span></span>
>

<span data-ttu-id="524b8-111">Pour obtenir plus d’informations, consultez les [instructions pour configurer un groupe Azure AD pour la gestion en libre-service](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management).</span><span class="sxs-lookup"><span data-stu-id="524b8-111">For more information, see the [instructions to configure an Azure AD group for self-service management](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management).</span></span>

<span data-ttu-id="524b8-112">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-self-service-groups) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="524b8-112">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-self-service-groups) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="524b8-113">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="524b8-113">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step15.png)| [<span data-ttu-id="524b8-114">Configurer l’appartenance à un groupe dynamique</span><span class="sxs-lookup"><span data-stu-id="524b8-114">Set up dynamic group membership</span></span>](identity-automatic-group-membership.md) |
