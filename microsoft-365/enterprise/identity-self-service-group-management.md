---
title: 'Étape 6 : Utiliser des groupes pour faciliter la gestion'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 02/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Apprenez à configurer la gestion des groupes en libre-service Azure AD.
ms.openlocfilehash: 9400e99ced45370600d1d5dcee4388ddef4250fe
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283521"
---
# <a name="step-6-use-groups-for-easier-management"></a><span data-ttu-id="79467-103">Étape 6 : Utiliser des groupes pour faciliter la gestion</span><span class="sxs-lookup"><span data-stu-id="79467-103">Step 6: Use groups for easier management</span></span>

<a name="identity-self-service-groups"></a>
## <a name="allow-users-to-create-and-manage-their-own-groups"></a><span data-ttu-id="79467-104">Autoriser les utilisateurs à créer et gérer leurs propres groupes</span><span class="sxs-lookup"><span data-stu-id="79467-104">Allow users to create and manage their own groups</span></span>

<span data-ttu-id="79467-105">*Cette étape facultative s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="79467-105">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="79467-106">Dans cette section, vous allez identifier les groupes Azure Active Directory (Azure AD) qui peuvent être gérés par les propriétaires des groupes plutôt que par les administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="79467-106">In this section, you'll identify Azure Active Directory (Azure AD) groups that can be managed by group owners instead of IT administrators.</span></span> <span data-ttu-id="79467-107">Appelée *gestion de groupes en libre-service*, cette fonctionnalité permet aux propriétaires de groupes qui ne disposent d’aucun rôle administratif de créer et de gérer des groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="79467-107">In this step, you'll identify Azure Active Directory (AD) groups that can be managed by group owners instead of IT administrators. Known as *self-service group management*, this feature allows group owners who are not assigned an administrative role to create and manage security groups.</span></span> 

<span data-ttu-id="79467-p102">Les utilisateurs peuvent demander à appartenir à un groupe de sécurité. Cette demande est envoyée au propriétaire du groupe, et non à l’administrateur informatique. Ainsi, le contrôle quotidien de l’appartenance au groupe peut être délégué aux propriétaires d’équipes, de projets ou d’entreprises qui comprennent l’usage du groupe pour l’entreprise et peuvent gérer ses membres.</span><span class="sxs-lookup"><span data-stu-id="79467-p102">Users can request membership in a security group and that request goes to the group owner, rather than an IT administrator. This allows the day-to-day control of group membership to be delegated to team, project, or business owners who understand the business use for the group and can manage its membership.</span></span>

>[!Note]
><span data-ttu-id="79467-110">La gestion des groupes en libre-service est réservée aux groupes Office 365 et aux groupes de sécurité Azure AD.</span><span class="sxs-lookup"><span data-stu-id="79467-110">Optional: Self-service group management is enabled for specific Azure AD security and Office 365 groups</span></span> <span data-ttu-id="79467-111">Elle n’est pas accessible aux groupes à extension messagerie, aux listes de distribution ou aux groupes synchronisés à partir de vos services AD DS (Active Directory Domain Services) locaux.</span><span class="sxs-lookup"><span data-stu-id="79467-111">Self-service group management is available only for Azure AD security and Office 365 groups. It is not available for mail-enabled groups, distribution lists, or any group that has been synchronized from your on-premises Windows Server Active Directory (AD).</span></span>
>

<span data-ttu-id="79467-112">Pour plus d’informations, consultez les [instructions de configuration d’un groupe Azure AD pour la gestion en libre-service](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management).</span><span class="sxs-lookup"><span data-stu-id="79467-112">For more information, see the [instructions to configure an Azure AD group for self-service management](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management).</span></span>

<span data-ttu-id="79467-113">Comme point de contrôle intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-self-service-groups) de cette section.</span><span class="sxs-lookup"><span data-stu-id="79467-113">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-self-service-groups) for this step.</span></span>

<a name="identity-dyn-groups"></a>
## <a name="set-up-dynamic-group-membership"></a><span data-ttu-id="79467-114">Configurer l’appartenance à un groupe dynamique</span><span class="sxs-lookup"><span data-stu-id="79467-114">Set up dynamic group membership</span></span>

<span data-ttu-id="79467-115">*Cette étape facultative s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="79467-115">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="79467-116">Dans cette section, vous allez créer une série de règles permettant d’ajouter ou de supprimer automatiquement des comptes d’utilisateur en tant que membres d’un groupe Azure AD.</span><span class="sxs-lookup"><span data-stu-id="79467-116">In this step, you'll create a series of rules that automatically add or remove user accounts as members of an Azure AD group. This is known as dynamic group membership. The rules are based on user account attributes, such as Department or Country.</span></span> <span data-ttu-id="79467-117">C’est ce que l’on appelle l’*appartenance à un groupe dynamique*.</span><span class="sxs-lookup"><span data-stu-id="79467-117">This is known as *dynamic group membership*.</span></span> <span data-ttu-id="79467-118">Les règles sont basées sur les attributs du compte d’utilisateur, comme le département ou le pays.</span><span class="sxs-lookup"><span data-stu-id="79467-118">The rules are based on user account attributes, such as Department or Country.</span></span>

<span data-ttu-id="79467-119">Voici comment les règles sont appliquées :</span><span class="sxs-lookup"><span data-stu-id="79467-119">Here’s how the rules are applied:</span></span>

- <span data-ttu-id="79467-120">Si un compte d’utilisateur correspond à toutes les règles pour le groupe, il devient un membre.</span><span class="sxs-lookup"><span data-stu-id="79467-120">If a new user account matches all the rules for the group, it becomes a member.</span></span>
- <span data-ttu-id="79467-121">Si un compte d’utilisateur n’est pas membre du groupe, mais que ses attributs changent pour qu’il corresponde à toutes les règles pour le groupe, il devient un membre de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="79467-121">If a user account isn’t a member of the group, but its attributes change so that it matches all the rules for the group, it becomes a member of that group.</span></span>
- <span data-ttu-id="79467-122">Si un compte d’utilisateur ne correspond pas à toutes les règles pour le groupe, il n’est pas ajouté au groupe.</span><span class="sxs-lookup"><span data-stu-id="79467-122">If a user account doesn’t match all the rules for the group, it isn’t added to the group.</span></span>
- <span data-ttu-id="79467-123">Si un compte d’utilisateur est membre du groupe, mais que ses attributs changent pour qu’il ne corresponde plus à toutes les règles pour le groupe, il est supprimé comme membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="79467-123">If a user account is a member of the group, but its attributes change so that it no longer matches all the rules for the group, it is removed as a member of the group.</span></span>

<span data-ttu-id="79467-p105">Pour utiliser l’appartenance dynamique, vous devez commencer par déterminer les ensembles de groupes qui ont un ensemble commun d’attributs de compte d’utilisateur. Par exemple, tous les membres du service Ventes doivent être dans le groupe Ventes Azure AD, en fonction de l’attribut de compte d’utilisateur Service défini sur « Ventes ».</span><span class="sxs-lookup"><span data-stu-id="79467-p105">To use dynamic membership, you must first determine the sets of groups that have a common set of user account attributes. For example, all members of the Sales department should be in the Sales Azure AD group, based on the user account attribute Department set to “Sales”.</span></span>

<span data-ttu-id="79467-126">Reportez-vous aux [instructions pour créer et configurer les règles pour un groupe Azure AD dynamique](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="79467-126">See the [instructions to create and configure the rules for a dynamic Azure AD group](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span></span>

<span data-ttu-id="79467-127">Les résultats de cette section sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="79467-127">The results of this step are:</span></span>

- <span data-ttu-id="79467-128">Un ensemble de groupes Azure AD qui peut être configuré pour l’appartenance dynamique</span><span class="sxs-lookup"><span data-stu-id="79467-128">A set of Azure AD groups that can be configured for dynamic membership</span></span>
- <span data-ttu-id="79467-129">Un ensemble de règles sur chaque groupe dynamique</span><span class="sxs-lookup"><span data-stu-id="79467-129">A set of rules on each dynamic group</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="79467-131">Guide du laboratoire de test : Automatiser les licences et l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="79467-131">Test Lab Guide: Automate licenses and group membership</span></span>](automate-licenses-group-membership-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="79467-132">Comme point de contrôle intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-dyn-groups) de cette section.</span><span class="sxs-lookup"><span data-stu-id="79467-132">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-dyn-groups) for this step.</span></span>

<a name="identity-group-license"></a>
## <a name="set-up-automatic-licensing"></a><span data-ttu-id="79467-133">Configurer la gestion des licences automatique</span><span class="sxs-lookup"><span data-stu-id="79467-133">Set up automatic licensing</span></span>

<span data-ttu-id="79467-134">*Cette étape facultative s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="79467-134">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="79467-135">Dans cette section, vous allez configurer des groupes de sécurité dans Azure AD pour attribuer automatiquement les licences d’un ensemble d’abonnements à tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="79467-135">In this section, you'll configure security groups in Azure AD to automatically assign licenses from a set of subscriptions to all the members of the group.</span></span> <span data-ttu-id="79467-136">C’est ce que l’on appelle la *gestion des licences basée sur les groupes*.</span><span class="sxs-lookup"><span data-stu-id="79467-136">This is known as *group-based licensing*.</span></span> <span data-ttu-id="79467-137">Si un compte d’utilisateur est ajouté ou supprimé du groupe, les licences des abonnements du groupe sont automatiquement attribuées ou supprimées du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="79467-137">In this step, you'll configure security groups in Azure AD to automatically assign licenses from a set of subscriptions to all the members of the group. This is known as group-based licensing. If a user account is added to or removed from the group, the licenses for the group’s subscriptions will be automatically assigned or removed from the user account.</span></span>

<span data-ttu-id="79467-138">Pour Microsoft 365 Entreprise, vous allez configurer des groupes de sécurité Azure AD pour affecter ces deux licences :</span><span class="sxs-lookup"><span data-stu-id="79467-138">For Microsoft 365 Enterprise, you'll configure Azure AD security groups to assign both of these licenses:</span></span>

- <span data-ttu-id="79467-139">Office 365 Entreprise E3 ou E5</span><span class="sxs-lookup"><span data-stu-id="79467-139">Office 365 Enterprise E3 or E5</span></span>
- <span data-ttu-id="79467-140">Enterprise Mobility + Security (EMS) E3 ou E5</span><span class="sxs-lookup"><span data-stu-id="79467-140">Enterprise Mobility + Security (EMS) E3 or E5</span></span>

<span data-ttu-id="79467-p107">Utilisez les groupes identifiés à l’Étape 2 pour rechercher les groupes qui contiennent une liste de comptes où tous les utilisateurs de ce groupe doivent avoir des licences Office 365 et EMS. Vérifiez que vous avez suffisamment de licences pour tous les membres du groupe. Si vous n’avez plus de licences, aucune licence ne sera attribuée aux nouveaux utilisateurs tant que d’autres licences ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="79467-p107">Using the groups you identified in Step 2, look for groups that contain a list of accounts where all users in that group must have both Office 365 and EMS licenses. Make sure you have enough licenses for all the group members. If you run out of licenses, new users won’t be assigned licenses until licenses become available.</span></span>

>[!Note]
><span data-ttu-id="79467-144">Vous ne devez pas configurer la *gestion des licences par groupes* pour des groupes qui contiennent des comptes B2B Azure.</span><span class="sxs-lookup"><span data-stu-id="79467-144">You should not configure *group-based licensing* for groups that contain Azure business to business (B2B) accounts.</span></span>
>

<span data-ttu-id="79467-145">Consultez des informations supplémentaires dans la rubrique [Principes de base des licences basées sur les groupes dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="79467-145">See additional information on [Group-based licensing basics in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal).</span></span>

<span data-ttu-id="79467-146">Consultez les [étapes pour configurer la gestion des licences par groupes pour un groupe de sécurité Azure](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="79467-146">See the [steps to configure group-based licensing for an Azure security group](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal).</span></span>

<span data-ttu-id="79467-147">Les résultats de cette section sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="79467-147">The results of this step are:</span></span>

- <span data-ttu-id="79467-148">Vous avez identifié les groupes de sécurité qui sont adaptés à la gestion des licences par groupes.</span><span class="sxs-lookup"><span data-stu-id="79467-148">You've identified which security groups are appropriate for group-based licensing.</span></span>
- <span data-ttu-id="79467-149">Vous avez configuré ces groupes pour la gestion des licences par groupes.</span><span class="sxs-lookup"><span data-stu-id="79467-149">You've configured these groups for group-based licensing.</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="79467-151">Guide du laboratoire de test : Automatiser les licences et l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="79467-151">Test Lab Guide: Automate licenses and group membership</span></span>](automate-licenses-group-membership-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="79467-152">Comme point de contrôle intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-group-license) de cette section.</span><span class="sxs-lookup"><span data-stu-id="79467-152">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-group-license) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="79467-153">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="79467-153">Next step</span></span>

[<span data-ttu-id="79467-154"> Identifier les critères de sortie de l’infrastructure</span><span class="sxs-lookup"><span data-stu-id="79467-154">Identity infrastructure exit criteria</span></span>](identity-exit-criteria.md)
