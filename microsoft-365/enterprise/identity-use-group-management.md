---
title: 'Étape 5 : Utiliser des groupes pour la gestion'
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
description: Vous pouvez utiliser des groupes pour automatiser la gestion de certaines tâches administratives.
ms.openlocfilehash: 215bb84cbb0cedc2f1320372ba8239cd51d07c98
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42067271"
---
# <a name="step-5-use-groups-for-management"></a><span data-ttu-id="82c2d-103">Étape 5 : Utiliser des groupes pour la gestion</span><span class="sxs-lookup"><span data-stu-id="82c2d-103">Step 5: Use groups for management</span></span>

![Phase 2 - Identité](../media/deploy-foundation-infrastructure/identity_icon-small.png)

<a name="identity-self-service-groups"></a>
## <a name="allow-users-to-create-and-manage-their-own-groups"></a><span data-ttu-id="82c2d-105">Autoriser les utilisateurs à créer et gérer leurs propres groupes</span><span class="sxs-lookup"><span data-stu-id="82c2d-105">Allow users to create and manage their own groups</span></span>

<span data-ttu-id="82c2d-106">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365*</span><span class="sxs-lookup"><span data-stu-id="82c2d-106">*This is optional and applies to both the E3 and E5 versions of Microsoft 365*</span></span>

<span data-ttu-id="82c2d-107">Dans cette section, vous allez identifier les groupes Azure Active Directory (Azure AD) qui peuvent être gérés par les propriétaires des groupes plutôt que par les administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="82c2d-107">In this section, you'll identify Azure Active Directory (Azure AD) groups that can be managed by group owners instead of IT administrators.</span></span> <span data-ttu-id="82c2d-108">Appelée *gestion de groupes en libre-service*, cette fonctionnalité permet aux propriétaires de groupes qui ne disposent d’aucun rôle administratif de créer et de gérer des groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="82c2d-108">Known as *self-service group management*, this feature allows group owners who are not assigned an administrative role to create and manage security groups.</span></span> 

<span data-ttu-id="82c2d-p102">Les utilisateurs peuvent demander à appartenir à un groupe de sécurité. Cette demande est envoyée au propriétaire du groupe, et non à l’administrateur informatique. Ainsi, le contrôle quotidien de l’appartenance au groupe peut être délégué aux propriétaires d’équipes, de projets ou d’entreprises qui comprennent l’usage du groupe pour l’entreprise et peuvent gérer ses membres.</span><span class="sxs-lookup"><span data-stu-id="82c2d-p102">Users can request membership in a security group and that request goes to the group owner, rather than an IT administrator. This allows the day-to-day control of group membership to be delegated to team, project, or business owners who understand the business use for the group and can manage its membership.</span></span>

>[!Note]
><span data-ttu-id="82c2d-111">La gestion des groupes en libre-service est réservée aux groupes Office 365 et aux groupes de sécurité Azure AD.</span><span class="sxs-lookup"><span data-stu-id="82c2d-111">Self-service group management is available only for Azure AD security and Office 365 groups.</span></span> <span data-ttu-id="82c2d-112">Elle n’est pas accessible aux groupes à extension messagerie, aux listes de distribution ou aux groupes synchronisés à partir de vos services AD DS (Active Directory Domain Services) locaux.</span><span class="sxs-lookup"><span data-stu-id="82c2d-112">It is not available for mail-enabled groups, distribution lists, or any group that has been synchronized from your on-premises Active Directory Domain Services (AD DS).</span></span>
>

<span data-ttu-id="82c2d-113">Pour plus d’informations, consultez les [instructions de configuration d’un groupe Azure AD pour la gestion en libre-service](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management).</span><span class="sxs-lookup"><span data-stu-id="82c2d-113">For more information, see the [instructions to configure an Azure AD group for self-service management](https://docs.microsoft.com/azure/active-directory/active-directory-accessmanagement-self-service-group-management).</span></span>

<span data-ttu-id="82c2d-114">Comme point de contrôle intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-self-service-groups) de cette section.</span><span class="sxs-lookup"><span data-stu-id="82c2d-114">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-self-service-groups) for this section.</span></span>

<a name="identity-dyn-groups"></a>
## <a name="set-up-dynamic-group-membership"></a><span data-ttu-id="82c2d-115">Configurer l’appartenance à un groupe dynamique</span><span class="sxs-lookup"><span data-stu-id="82c2d-115">Set up dynamic group membership</span></span>

<span data-ttu-id="82c2d-116">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365*</span><span class="sxs-lookup"><span data-stu-id="82c2d-116">*This is optional and applies to both the E3 and E5 versions of Microsoft 365*</span></span>

<span data-ttu-id="82c2d-117">Dans cette section, vous allez créer une série de règles permettant d’ajouter ou de supprimer automatiquement des comptes d’utilisateur en tant que membres d’un groupe Azure AD.</span><span class="sxs-lookup"><span data-stu-id="82c2d-117">In this section, you'll create a series of rules that automatically add or remove user accounts as members of an Azure AD group.</span></span> <span data-ttu-id="82c2d-118">C’est ce que l’on appelle l’*appartenance à un groupe dynamique*.</span><span class="sxs-lookup"><span data-stu-id="82c2d-118">This is known as *dynamic group membership*.</span></span> <span data-ttu-id="82c2d-119">Les règles sont basées sur les attributs du compte d’utilisateur, comme le département ou le pays.</span><span class="sxs-lookup"><span data-stu-id="82c2d-119">The rules are based on user account attributes, such as Department or Country.</span></span>

<span data-ttu-id="82c2d-120">Voici comment les règles sont appliquées :</span><span class="sxs-lookup"><span data-stu-id="82c2d-120">Here’s how the rules are applied:</span></span>

- <span data-ttu-id="82c2d-121">Si un compte d’utilisateur correspond à toutes les règles pour le groupe, il devient un membre.</span><span class="sxs-lookup"><span data-stu-id="82c2d-121">If a new user account matches all the rules for the group, it becomes a member.</span></span>
- <span data-ttu-id="82c2d-122">Si un compte d’utilisateur n’est pas membre du groupe, mais que ses attributs changent pour qu’il corresponde à toutes les règles pour le groupe, il devient un membre de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="82c2d-122">If a user account isn’t a member of the group, but its attributes change so that it matches all the rules for the group, it becomes a member of that group.</span></span>
- <span data-ttu-id="82c2d-123">Si un compte d’utilisateur ne correspond pas à toutes les règles pour le groupe, il n’est pas ajouté au groupe.</span><span class="sxs-lookup"><span data-stu-id="82c2d-123">If a user account doesn’t match all the rules for the group, it isn’t added to the group.</span></span>
- <span data-ttu-id="82c2d-124">Si un compte d’utilisateur est membre du groupe, mais que ses attributs changent pour qu’il ne corresponde plus à toutes les règles pour le groupe, il est supprimé comme membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="82c2d-124">If a user account is a member of the group, but its attributes change so that it no longer matches all the rules for the group, it is removed as a member of the group.</span></span>

<span data-ttu-id="82c2d-p105">Pour utiliser l’appartenance dynamique, vous devez commencer par déterminer les ensembles de groupes qui ont un ensemble commun d’attributs de compte d’utilisateur. Par exemple, tous les membres du service Ventes doivent être dans le groupe Ventes Azure AD, en fonction de l’attribut de compte d’utilisateur Service défini sur « Ventes ».</span><span class="sxs-lookup"><span data-stu-id="82c2d-p105">To use dynamic membership, you must first determine the sets of groups that have a common set of user account attributes. For example, all members of the Sales department should be in the Sales Azure AD group, based on the user account attribute Department set to “Sales”.</span></span>

<span data-ttu-id="82c2d-127">Reportez-vous aux [instructions pour créer et configurer les règles pour un groupe Azure AD dynamique](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="82c2d-127">See the [instructions to create and configure the rules for a dynamic Azure AD group](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span></span>

<span data-ttu-id="82c2d-128">Les résultats de cette section sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="82c2d-128">The results of this section are:</span></span>

- <span data-ttu-id="82c2d-129">Un ensemble de groupes Azure AD qui peut être configuré pour l’appartenance dynamique</span><span class="sxs-lookup"><span data-stu-id="82c2d-129">A set of Azure AD groups that can be configured for dynamic membership</span></span>
- <span data-ttu-id="82c2d-130">Un ensemble de règles sur chaque groupe dynamique</span><span class="sxs-lookup"><span data-stu-id="82c2d-130">A set of rules on each dynamic group</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="82c2d-132">Guide du laboratoire de test : Automatiser les licences et l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="82c2d-132">Test Lab Guide: Automate licenses and group membership</span></span>](automate-licenses-group-membership-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="82c2d-133">Comme point de contrôle intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-dyn-groups) de cette section.</span><span class="sxs-lookup"><span data-stu-id="82c2d-133">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-dyn-groups) for this section.</span></span>

<a name="identity-group-license"></a>
## <a name="set-up-automatic-licensing"></a><span data-ttu-id="82c2d-134">Configurer la gestion des licences automatique</span><span class="sxs-lookup"><span data-stu-id="82c2d-134">Set up automatic licensing</span></span>

<span data-ttu-id="82c2d-135">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365*</span><span class="sxs-lookup"><span data-stu-id="82c2d-135">*This is optional and applies to both the E3 and E5 versions of Microsoft 365*</span></span>

<span data-ttu-id="82c2d-136">Dans cette section, vous allez configurer des groupes de sécurité dans Azure AD pour attribuer automatiquement les licences d’un ensemble d’abonnements à tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="82c2d-136">In this section, you'll configure security groups in Azure AD to automatically assign licenses from a set of subscriptions to all the members of the group.</span></span> <span data-ttu-id="82c2d-137">C’est ce que l’on appelle la *gestion des licences basée sur les groupes*.</span><span class="sxs-lookup"><span data-stu-id="82c2d-137">This is known as *group-based licensing*.</span></span> <span data-ttu-id="82c2d-138">Si un compte d’utilisateur est ajouté ou supprimé du groupe, les licences des abonnements du groupe sont automatiquement attribuées ou supprimées du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82c2d-138">If a user account is added to or removed from the group, the licenses for the group’s subscriptions will be automatically assigned or unassigned from the user account.</span></span>

<span data-ttu-id="82c2d-139">Pour Microsoft 365 Entreprise, vous allez configurer des groupes de sécurité Azure AD afin d’attribuer la licence Microsoft 365 Entreprise qui convient.</span><span class="sxs-lookup"><span data-stu-id="82c2d-139">For Microsoft 365 Enterprise, you'll configure Azure AD security groups to assign the appropriate Microsoft 365 Enterprise license.</span></span>

<span data-ttu-id="82c2d-140">Vérifiez que vous disposez de suffisamment de licences pour tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="82c2d-140">Make sure you have enough licenses for all the group members.</span></span> <span data-ttu-id="82c2d-141">Si vous n’avez plus de licences, aucune licence ne sera attribuée aux nouveaux utilisateurs tant que d’autres licences ne seront pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="82c2d-141">If you run out of licenses, new users won’t be assigned licenses until licenses become available.</span></span>

>[!Note]
><span data-ttu-id="82c2d-142">Vous ne devez pas configurer la *gestion des licences par groupes* pour des groupes qui contiennent des comptes B2B Azure.</span><span class="sxs-lookup"><span data-stu-id="82c2d-142">You should not configure *group-based licensing* for groups that contain Azure business to business (B2B) accounts.</span></span>
>

<span data-ttu-id="82c2d-143">Consultez des informations supplémentaires dans la rubrique [Principes de base des licences basées sur les groupes dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="82c2d-143">See additional information on [Group-based licensing basics in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal).</span></span>

<span data-ttu-id="82c2d-144">Consultez les [étapes pour configurer la gestion des licences par groupes pour un groupe de sécurité Azure](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="82c2d-144">See the [steps to configure group-based licensing for an Azure security group](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal).</span></span>

<span data-ttu-id="82c2d-145">Les résultats de cette section sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="82c2d-145">The results of this section are:</span></span>

- <span data-ttu-id="82c2d-146">Vous avez identifié les groupes de sécurité qui sont adaptés à la gestion des licences par groupes.</span><span class="sxs-lookup"><span data-stu-id="82c2d-146">You've identified which security groups are appropriate for group-based licensing.</span></span>
- <span data-ttu-id="82c2d-147">Vous avez configuré ces groupes pour la gestion des licences par groupes.</span><span class="sxs-lookup"><span data-stu-id="82c2d-147">You've configured these groups for group-based licensing.</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="82c2d-149">Guide du laboratoire de test : Automatiser les licences et l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="82c2d-149">Test Lab Guide: Automate licenses and group membership</span></span>](automate-licenses-group-membership-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="82c2d-150">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-group-license) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="82c2d-150">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-group-license) for this section.</span></span>

|||
|:-------|:-----|
|![Étape 6](../media/stepnumbers/Step6.png)| [<span data-ttu-id="82c2d-152">Configurer la gouvernance des identités</span><span class="sxs-lookup"><span data-stu-id="82c2d-152">Configure identity governance</span></span>](identity-configure-identity-governance.md) |
