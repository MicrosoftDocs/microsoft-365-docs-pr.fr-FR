---
title: 'Étape 12 : Configurer la gestion des licences automatique'
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
description: Comprenez et configurez la gestion des licences par groupes pour des groupes Azure AD.
ms.openlocfilehash: 82e4192f2ef9ba3d1d5ed7bd99a8cf603d7d4cc9
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26866821"
---
# <a name="step-12-set-up-automatic-licensing"></a><span data-ttu-id="16fb3-103">Étape 12 : Configurer la gestion des licences automatique</span><span class="sxs-lookup"><span data-stu-id="16fb3-103">Step 12: Set up automatic licensing</span></span>

<span data-ttu-id="16fb3-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="16fb3-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="16fb3-p101">Dans cette étape, vous allez configurer des groupes de sécurité dans Azure AD pour attribuer automatiquement des licences d’un jeu d’abonnements à tous les membres du groupe. Il s’agit de la *gestion des licences par groupes*. Si un compte d’utilisateur est ajouté ou supprimé du groupe, les licences pour les abonnements du groupe sont automatiquement attribuées ou supprimées du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16fb3-p101">In Step 11, you'll configure security groups in Azure AD to automatically assign licenses from a set of subscriptions to all the members of the group. This is known as *group-based licensing*. If a user account is added to or removed from the group, the licenses for the group’s subscriptions will be automatically assigned or removed from the user account.</span></span>

<span data-ttu-id="16fb3-108">Pour Microsoft 365 Entreprise, vous allez configurer des groupes de sécurité Azure AD pour affecter ces deux licences :</span><span class="sxs-lookup"><span data-stu-id="16fb3-108">For Microsoft 365 Enterprise, you'll configure Azure AD security groups to assign both of these licenses:</span></span>

- <span data-ttu-id="16fb3-109">Office 365 Entreprise E3 ou E5</span><span class="sxs-lookup"><span data-stu-id="16fb3-109">Office 365 Enterprise E3 or E5</span></span>
- <span data-ttu-id="16fb3-110">Enterprise Mobility + Security (EMS) E3 ou E5</span><span class="sxs-lookup"><span data-stu-id="16fb3-110">Enterprise Mobility + Security (EMS) E3 or E5</span></span>

<span data-ttu-id="16fb3-p102">Utilisez les groupes identifiés à l’Étape 2 pour rechercher les groupes qui contiennent une liste de comptes où tous les utilisateurs de ce groupe doivent avoir des licences Office 365 et EMS. Vérifiez que vous avez suffisamment de licences pour tous les membres du groupe. Si vous n’avez plus de licences, aucune licence ne sera attribuée aux nouveaux utilisateurs tant que d’autres licences ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="16fb3-p102">Using the groups you identified in Step 2, look for groups that contain a list of accounts where all users in that group must have both Office 365 and EMS licenses. Make sure you have enough licenses for all the group members. If you run out of licenses, new users won’t be assigned licenses until licenses become available.</span></span>

>[!Note]
><span data-ttu-id="16fb3-114">Vous ne devez pas configurer la *gestion des licences par groupes* pour des groupes qui contiennent des comptes B2B Azure.</span><span class="sxs-lookup"><span data-stu-id="16fb3-114">You should not configure *group-based licensing* for groups that contain Azure business to business (B2B) accounts.</span></span>
>

<span data-ttu-id="16fb3-115">Consultez des informations supplémentaires dans la rubrique [Principes de base des licences basées sur les groupes dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="16fb3-115">See additional information on [Group-based licensing basics in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal).</span></span>

<span data-ttu-id="16fb3-116">Consultez les [étapes pour configurer la gestion des licences par groupes pour un groupe de sécurité Azure](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="16fb3-116">See the [steps to configure group-based licensing for an Azure security group](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal).</span></span>

<span data-ttu-id="16fb3-117">Les résultats de cette étape sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="16fb3-117">The results of this step are:</span></span>

- <span data-ttu-id="16fb3-118">Vous avez identifié les groupes de sécurité qui sont adaptés à la gestion des licences par groupes.</span><span class="sxs-lookup"><span data-stu-id="16fb3-118">You've identified which security groups are appropriate for group-based licensing.</span></span>
- <span data-ttu-id="16fb3-119">Vous avez configuré ces groupes pour la gestion des licences par groupes.</span><span class="sxs-lookup"><span data-stu-id="16fb3-119">You've configured these groups for group-based licensing.</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="16fb3-121">Guide du laboratoire de test : Automatiser les licences et l’appartenance au groupe</span><span class="sxs-lookup"><span data-stu-id="16fb3-121">Test Lab Guide: Automate licenses and group membership</span></span>](automate-licenses-group-membership-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="16fb3-122">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-group-license) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="16fb3-122">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-group-license) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="16fb3-123">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="16fb3-123">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step13.png)| [<span data-ttu-id="16fb3-124">Surveillez l’activité de connexion et du client</span><span class="sxs-lookup"><span data-stu-id="16fb3-124">Monitor tenant and sign-in activity</span></span>](identity-azure-ad-access-usage-reporting.md) |

