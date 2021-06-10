---
title: Gestion des groupes Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-mar2020
ms.collection:
- Ent_O365
- M365-subscription-management
search.appverid:
- MET150
- MOE150
- MED150
- BCS160
ms.assetid: 98ca5b3f-f720-4d8e-91be-fe656548a25a
description: Découvrez comment gérer les groupes Microsoft 365'équipe.
ms.openlocfilehash: 529bdb874661329497b103a1207b90625ad33a4b
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50911006"
---
# <a name="manage-microsoft-365-groups"></a><span data-ttu-id="5bd95-103">Gestion des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5bd95-103">Manage Microsoft 365 groups</span></span>

<span data-ttu-id="5bd95-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="5bd95-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="5bd95-105">Vous pouvez gérer Microsoft 365 groupes de plusieurs manières différentes, en fonction de votre configuration.</span><span class="sxs-lookup"><span data-stu-id="5bd95-105">You can manage Microsoft 365 groups in several different ways, depending on your configuration.</span></span> <span data-ttu-id="5bd95-106">Vous pouvez gérer les comptes d’utilisateurs dans le Centre [d’administration Microsoft 365,](../admin/add-users/index.yml)PowerShell, dans les services de domaine Active Directory (AD DS) ou dans le Centre d’administration [Azure Active Directory (Azure AD).](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)</span><span class="sxs-lookup"><span data-stu-id="5bd95-106">You can manage user accounts in the [Microsoft 365 admin center](../admin/add-users/index.yml), PowerShell, in Active Directory Domain Services (AD DS), or in the [Azure Active Directory (Azure AD) admin center](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span> 

## <a name="plan-for-where-and-how-you-will-manage-your-groups"></a><span data-ttu-id="5bd95-107">Planifier l’endroit et la façon dont vous allez gérer vos groupes</span><span class="sxs-lookup"><span data-stu-id="5bd95-107">Plan for where and how you will manage your groups</span></span>

<span data-ttu-id="5bd95-108">L’endroit où et comment vous pouvez gérer vos comptes d’utilisateur dépend du modèle d’identité que vous souhaitez utiliser pour votre Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5bd95-108">Where and how you can manage your user accounts depends on the identity model you want to use for your Microsoft 365.</span></span> <span data-ttu-id="5bd95-109">Les deux modèles globaux sont uniquement cloud et hybrides.</span><span class="sxs-lookup"><span data-stu-id="5bd95-109">The two overall models are cloud-only and hybrid.</span></span>
  
### <a name="cloud-only"></a><span data-ttu-id="5bd95-110">Cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="5bd95-110">Cloud-only</span></span>

<span data-ttu-id="5bd95-111">Vous créez et gérez des groupes avec :</span><span class="sxs-lookup"><span data-stu-id="5bd95-111">You create and manage groups with:</span></span>

- [<span data-ttu-id="5bd95-112">Le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5bd95-112">The Microsoft 365 admin center</span></span>](../admin/add-users/index.yml)
- [<span data-ttu-id="5bd95-113">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5bd95-113">PowerShell</span></span>](maintain-group-membership-with-microsoft-365-powershell.md)
- [<span data-ttu-id="5bd95-114">Centre d’administration d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="5bd95-114">Azure AD admin center</span></span>](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
    
### <a name="hybrid"></a><span data-ttu-id="5bd95-115">Hybride</span><span class="sxs-lookup"><span data-stu-id="5bd95-115">Hybrid</span></span>

<span data-ttu-id="5bd95-116">Les groupes AD DS sont synchronisés avec les Microsoft 365 d’AD DS. Vous devez donc utiliser les outils AD DS locaux pour gérer ces groupes.</span><span class="sxs-lookup"><span data-stu-id="5bd95-116">AD DS groups are synchronized with Microsoft 365 from AD DS, so you must use on-premises AD DS tools to manage these groups.</span></span>

<span data-ttu-id="5bd95-117">Vous pouvez également créer et gérer des groupes Azure AD séparés des groupes AD DS, mais qui peuvent contenir des utilisateurs et des groupes d’AD DS.</span><span class="sxs-lookup"><span data-stu-id="5bd95-117">You can also create and manage Azure AD groups that are separate from AD DS groups but can contain users and groups from AD DS.</span></span> <span data-ttu-id="5bd95-118">Dans ce cas, vous pouvez utiliser :</span><span class="sxs-lookup"><span data-stu-id="5bd95-118">In this case, you can use:</span></span>

- [<span data-ttu-id="5bd95-119">Le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5bd95-119">The Microsoft 365 admin center</span></span>](../admin/add-users/index.yml)
- [<span data-ttu-id="5bd95-120">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5bd95-120">PowerShell</span></span>](maintain-group-membership-with-microsoft-365-powershell.md)
- [<span data-ttu-id="5bd95-121">Centre d’administration d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="5bd95-121">Azure AD admin center</span></span>](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

## <a name="allow-users-to-create-and-manage-their-own-groups"></a><span data-ttu-id="5bd95-122">Autoriser les utilisateurs à créer et gérer leurs propres groupes</span><span class="sxs-lookup"><span data-stu-id="5bd95-122">Allow users to create and manage their own groups</span></span>

<span data-ttu-id="5bd95-123">Azure AD autorise les groupes qui peuvent être gérés par les propriétaires de groupes plutôt que par les administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="5bd95-123">Azure AD allows groups that can be managed by group owners instead of IT administrators.</span></span> <span data-ttu-id="5bd95-124">Appelée *gestion de groupes en libre-service*, cette fonctionnalité permet aux propriétaires de groupes qui ne disposent d’aucun rôle administratif de créer et de gérer des groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5bd95-124">Known as *self-service group management*, this feature allows group owners who are not assigned an administrative role to create and manage security groups.</span></span> 

<span data-ttu-id="5bd95-p105">Les utilisateurs peuvent demander à appartenir à un groupe de sécurité. Cette demande est envoyée au propriétaire du groupe, et non à l’administrateur informatique. Ainsi, le contrôle quotidien de l’appartenance au groupe peut être délégué aux propriétaires d’équipes, de projets ou d’entreprises qui comprennent l’usage du groupe pour l’entreprise et peuvent gérer ses membres.</span><span class="sxs-lookup"><span data-stu-id="5bd95-p105">Users can request membership in a security group and that request goes to the group owner, rather than an IT administrator. This allows the day-to-day control of group membership to be delegated to team, project, or business owners who understand the business use for the group and can manage its membership.</span></span>

>[!Note]
><span data-ttu-id="5bd95-127">La gestion des groupes en libre-service est réservée aux groupes Microsoft 365 et aux groupes de sécurité Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5bd95-127">Self-service group management is available only for Azure AD security and Microsoft 365 groups.</span></span> <span data-ttu-id="5bd95-128">Il n’est pas disponible pour les groupes à messagerie, les listes de distribution ou les groupes qui ont été synchronisés à partir d’AD DS.</span><span class="sxs-lookup"><span data-stu-id="5bd95-128">It is not available for mail-enabled groups, distribution lists, or any group that has been synchronized from AD DS.</span></span>
>

<span data-ttu-id="5bd95-129">Pour plus d’informations, consultez les [instructions de configuration d’un groupe Azure AD pour la gestion en libre-service](/azure/active-directory/active-directory-accessmanagement-self-service-group-management).</span><span class="sxs-lookup"><span data-stu-id="5bd95-129">For more information, see the [instructions to configure an Azure AD group for self-service management](/azure/active-directory/active-directory-accessmanagement-self-service-group-management).</span></span>

## <a name="set-up-dynamic-group-membership"></a><span data-ttu-id="5bd95-130">Configurer l’appartenance à un groupe dynamique</span><span class="sxs-lookup"><span data-stu-id="5bd95-130">Set up dynamic group membership</span></span>

<span data-ttu-id="5bd95-131">Azure AD prend en charge la configuration d’une série de règles qui ajoutent ou suppriment automatiquement des comptes d’utilisateur en tant que membres d’un groupe Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5bd95-131">Azure AD supports configuring a series of rules that automatically add or remove user accounts as members of an Azure AD group.</span></span> <span data-ttu-id="5bd95-132">C’est ce que l’on appelle l’*appartenance à un groupe dynamique*.</span><span class="sxs-lookup"><span data-stu-id="5bd95-132">This is known as *dynamic group membership*.</span></span> <span data-ttu-id="5bd95-133">Les règles sont basées sur les attributs du compte d’utilisateur, comme le département ou le pays.</span><span class="sxs-lookup"><span data-stu-id="5bd95-133">The rules are based on user account attributes, such as Department or Country.</span></span>

<span data-ttu-id="5bd95-134">Voici comment les règles sont appliquées :</span><span class="sxs-lookup"><span data-stu-id="5bd95-134">Here's how the rules are applied:</span></span>

- <span data-ttu-id="5bd95-135">Si un compte d’utilisateur correspond à toutes les règles pour le groupe, il devient un membre.</span><span class="sxs-lookup"><span data-stu-id="5bd95-135">If a new user account matches all the rules for the group, it becomes a member.</span></span>
- <span data-ttu-id="5bd95-136">Si un compte d’utilisateur n’est pas membre du groupe, mais que ses attributs changent pour qu’il corresponde à toutes les règles pour le groupe, il devient un membre de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="5bd95-136">If a user account isn't a member of the group, but its attributes change so that it matches all the rules for the group, it becomes a member of that group.</span></span>
- <span data-ttu-id="5bd95-137">Si un compte d’utilisateur ne correspond pas à toutes les règles pour le groupe, il n’est pas ajouté au groupe.</span><span class="sxs-lookup"><span data-stu-id="5bd95-137">If a user account doesn't match all the rules for the group, it isn't added to the group.</span></span>
- <span data-ttu-id="5bd95-138">Si un compte d’utilisateur est membre du groupe, mais que ses attributs changent pour qu’il ne corresponde plus à toutes les règles pour le groupe, il est supprimé comme membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="5bd95-138">If a user account is a member of the group, but its attributes change so that it no longer matches all the rules for the group, it is removed as a member of the group.</span></span>

<span data-ttu-id="5bd95-p108">Pour utiliser l’appartenance dynamique, vous devez commencer par déterminer les ensembles de groupes qui ont un ensemble commun d’attributs de compte d’utilisateur. Par exemple, tous les membres du service Ventes doivent être dans le groupe Ventes Azure AD, en fonction de l’attribut de compte d’utilisateur Service défini sur « Ventes ».</span><span class="sxs-lookup"><span data-stu-id="5bd95-p108">To use dynamic membership, you must first determine the sets of groups that have a common set of user account attributes. For example, all members of the Sales department should be in the Sales Azure AD group, based on the user account attribute Department set to "Sales".</span></span>

<span data-ttu-id="5bd95-141">Reportez-vous aux [instructions pour créer et configurer les règles pour un groupe Azure AD dynamique](/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="5bd95-141">See the [instructions to create and configure the rules for a dynamic Azure AD group](/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span></span>

## <a name="set-up-automatic-licensing"></a><span data-ttu-id="5bd95-142">Configurer la gestion des licences automatique</span><span class="sxs-lookup"><span data-stu-id="5bd95-142">Set up automatic licensing</span></span>

<span data-ttu-id="5bd95-143">Vous pouvez configurer des groupes de sécurité dans Azure AD pour attribuer automatiquement des licences d’un ensemble d’abonnements à tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="5bd95-143">You can configure security groups in Azure AD to automatically assign licenses from a set of subscriptions to all the members of the group.</span></span> <span data-ttu-id="5bd95-144">C’est ce que l’on appelle la *gestion des licences basée sur les groupes*.</span><span class="sxs-lookup"><span data-stu-id="5bd95-144">This is known as *group-based licensing*.</span></span> <span data-ttu-id="5bd95-145">Si un compte d’utilisateur est ajouté au groupe ou supprimé de ce dernier, les licences des abonnements du groupe sont automatiquement attribuées au compte d’utilisateur ou supprimées du compte.</span><span class="sxs-lookup"><span data-stu-id="5bd95-145">If a user account is added to or removed from the group, the licenses for the group's subscriptions will be automatically assigned or unassigned from the user account.</span></span>

<span data-ttu-id="5bd95-146">Pour Microsoft 365 Entreprise, vous allez configurer des groupes de sécurité Azure AD afin d’attribuer la licence Microsoft 365 Entreprise qui convient.</span><span class="sxs-lookup"><span data-stu-id="5bd95-146">For Microsoft 365 Enterprise, you'll configure Azure AD security groups to assign the appropriate Microsoft 365 Enterprise license.</span></span>

<span data-ttu-id="5bd95-147">Vérifiez que vous disposez de suffisamment de licences pour tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="5bd95-147">Make sure you have enough licenses for all the group members.</span></span> <span data-ttu-id="5bd95-148">Si vous n’avez plus de licences, aucune licence ne sera attribuée aux nouveaux utilisateurs tant que d’autres licences ne seront pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="5bd95-148">If you run out of licenses, new users won't be assigned licenses until licenses become available.</span></span>

>[!Note]
><span data-ttu-id="5bd95-149">Vous ne devez pas configurer la gestion des licences par groupes pour des groupes qui contiennent des comptes B2B Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd95-149">You should not configure group-based licensing for groups that contain Azure business to business (B2B) accounts.</span></span>
>

<span data-ttu-id="5bd95-150">Pour plus d’informations, voir les informations de base sur les [licences basées sur les groupes dans Azure AD.](/azure/active-directory/active-directory-licensing-whatis-azure-portal)</span><span class="sxs-lookup"><span data-stu-id="5bd95-150">For more information, see [Group-based licensing basics in Azure AD](/azure/active-directory/active-directory-licensing-whatis-azure-portal).</span></span>

<span data-ttu-id="5bd95-151">Consultez les instructions pour configurer la gestion des licences basée sur [les groupes pour un groupe de sécurité Azure.](/azure/active-directory/active-directory-licensing-group-assignment-azure-portal)</span><span class="sxs-lookup"><span data-stu-id="5bd95-151">See the [instructions to configure group-based licensing for an Azure security group](/azure/active-directory/active-directory-licensing-group-assignment-azure-portal).</span></span>