---
title: 'Étape 15 : Configurer l’appartenance aux groupes dynamiques'
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
description: Comprenez et configurez l’appartenance à un groupe automatique en fonction des attributs de compte.
ms.openlocfilehash: 8619179bc4e3ce17d9201cafb88e1b1c48fc7f4f
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867355"
---
# <a name="step-15-set-up-dynamic-group-membership"></a><span data-ttu-id="3fd0a-103">Étape 15 : Configurer l’appartenance aux groupes dynamiques</span><span class="sxs-lookup"><span data-stu-id="3fd0a-103">Step 15: Set up dynamic group membership</span></span>

<span data-ttu-id="3fd0a-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="3fd0a-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="3fd0a-p101">Dans cette étape, vous allez créer un ensemble de règles qui ajoutent ou suppriment automatiquement des comptes d’utilisateur comme membres d’un groupe Azure AD. Il s’agit de l’*appartenance à un groupe dynamique*. Les règles sont basées sur des attributs de compte d’utilisateur tels que le Service ou le Pays.</span><span class="sxs-lookup"><span data-stu-id="3fd0a-p101">In Step 12, you'll create a series of rules that automatically add or remove user accounts as members of an Azure AD group. This is known as *dynamic group membership*. The rules are based on user account attributes, such as Department or Country.</span></span>

<span data-ttu-id="3fd0a-108">Voici comment les règles sont appliquées :</span><span class="sxs-lookup"><span data-stu-id="3fd0a-108">Here’s how the rules are applied:</span></span>

- <span data-ttu-id="3fd0a-109">Si un compte d’utilisateur correspond à toutes les règles pour le groupe, il devient un membre.</span><span class="sxs-lookup"><span data-stu-id="3fd0a-109">If a new user account matches all the rules for the group, it becomes a member.</span></span>
- <span data-ttu-id="3fd0a-110">Si un compte d’utilisateur n’est pas membre du groupe, mais que ses attributs changent pour qu’il corresponde à toutes les règles pour le groupe, il devient un membre de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="3fd0a-110">If a user account isn’t a member of the group, but its attributes change so that it matches all the rules for the group, it becomes a member of that group.</span></span>
- <span data-ttu-id="3fd0a-111">Si un compte d’utilisateur ne correspond pas à toutes les règles pour le groupe, il n’est pas ajouté au groupe.</span><span class="sxs-lookup"><span data-stu-id="3fd0a-111">If a user account doesn’t match all the rules for the group, it isn’t added to the group.</span></span>
- <span data-ttu-id="3fd0a-112">Si un compte d’utilisateur est membre du groupe, mais que ses attributs changent pour qu’il ne corresponde plus à toutes les règles pour le groupe, il est supprimé comme membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="3fd0a-112">If a user account is a member of the group, but its attributes change so that it no longer matches all the rules for the group, it is removed as a member of the group.</span></span>

<span data-ttu-id="3fd0a-p102">Pour utiliser l’appartenance dynamique, vous devez commencer par déterminer les ensembles de groupes qui ont un ensemble commun d’attributs de compte d’utilisateur. Par exemple, tous les membres du service Ventes doivent être dans le groupe Ventes Azure AD, en fonction de l’attribut de compte d’utilisateur Service défini sur « Ventes ».</span><span class="sxs-lookup"><span data-stu-id="3fd0a-p102">To use dynamic membership, you must first determine the sets of groups that have a common set of user account attributes. For example, all members of the Sales department should be in the Sales Azure AD group, based on the user account attribute Department set to “Sales”.</span></span>

<span data-ttu-id="3fd0a-115">Reportez-vous aux [instructions pour créer et configurer les règles pour un groupe Azure AD dynamique](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="3fd0a-115">See the [instructions to create and configure the rules for a dynamic Azure AD group](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span></span>

<span data-ttu-id="3fd0a-116">Les résultats de cette étape sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="3fd0a-116">The results of this step are:</span></span>

- <span data-ttu-id="3fd0a-117">Un ensemble de groupes Azure AD qui peut être configuré pour l’appartenance dynamique</span><span class="sxs-lookup"><span data-stu-id="3fd0a-117">A set of Azure AD groups that can be configured for dynamic membership</span></span>
- <span data-ttu-id="3fd0a-118">Un ensemble de règles sur chaque groupe dynamique</span><span class="sxs-lookup"><span data-stu-id="3fd0a-118">A set of rules on each dynamic group</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="3fd0a-120">Guide du laboratoire de test : Automatiser les licences et l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="3fd0a-120">Test Lab Guide: Automate licenses and group membership</span></span>](automate-licenses-group-membership-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="3fd0a-121">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-dyn-groups) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="3fd0a-121">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-dyn-groups) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="3fd0a-122">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="3fd0a-122">Next step</span></span>

[<span data-ttu-id="3fd0a-123"> Identifier les critères de sortie de l’infrastructure</span><span class="sxs-lookup"><span data-stu-id="3fd0a-123">Identity infrastructure exit criteria</span></span>](identity-exit-criteria.md)
