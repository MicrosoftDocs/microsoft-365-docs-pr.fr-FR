---
title: Gérer la gouvernance des identités Microsoft 365
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
description: Découvrez comment utiliser les fonctionnalités de gouvernance des identités Microsoft 365.
ms.openlocfilehash: e4c537e7fa3ac099caf8b7dbc44327308751c8f5
ms.sourcegitcommit: 33afa334328cc4e3f2474abd611c1411adabd39f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2020
ms.locfileid: "48370345"
---
# <a name="manage-microsoft-365-identity-governance"></a><span data-ttu-id="4928f-103">Gérer la gouvernance des identités Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4928f-103">Manage Microsoft 365 identity governance</span></span>

<span data-ttu-id="4928f-104">La gouvernance des identités s’intéresse à la protection, la surveillance et l’audit de l’accès aux ressources critiques, tout en assurant la productivité des employés.</span><span class="sxs-lookup"><span data-stu-id="4928f-104">Identity governance is all about protecting, monitoring, and auditing access to critical assets while ensuring employee productivity.</span></span> <span data-ttu-id="4928f-105">Par exemple, avec la gouvernance des identités, vous pouvez vous assurer que les utilisateurs appropriés disposent de l’accès approprié aux ressources adéquates et déterminer si cet accès change au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="4928f-105">For example, with identity governance, you can ensure that the right users have the right access to the right resources and determine if that access changes over time.</span></span>

<span data-ttu-id="4928f-106">Pour plus d’informations, consultez cette vue d’ensemble de la gouvernance des identités pour [Azure Active Directory (Azure AD).](https://docs.microsoft.com/azure/active-directory/governance/identity-governance-overview)</span><span class="sxs-lookup"><span data-stu-id="4928f-106">For more information, See this [overview of identity governance for Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/governance/identity-governance-overview).</span></span>

## <a name="set-up-azure-ad-access-reviews"></a><span data-ttu-id="4928f-107">Configurer les révisions d’accès Azure AD</span><span class="sxs-lookup"><span data-stu-id="4928f-107">Set up Azure AD access reviews</span></span>

<span data-ttu-id="4928f-108">Les révisions d’accès Azure AD vous permettent de passer en revue l’accès d’un utilisateur pour vous assurer que seules les bonnes personnes ont un accès continu.</span><span class="sxs-lookup"><span data-stu-id="4928f-108">Azure AD access reviews allow you to review a user's access to ensure only the right people have continued access.</span></span> <span data-ttu-id="4928f-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4928f-109">For example:</span></span>

- <span data-ttu-id="4928f-110">Lorsqu’un nouvel employé rejoint votre organisation, vous devez vous assurer qu’il dispose d’un accès approprié pour être productif.</span><span class="sxs-lookup"><span data-stu-id="4928f-110">As a new employee joins your organization, you need to ensure they have the right access to be productive.</span></span>
- <span data-ttu-id="4928f-111">Au fur et à mesure que cet employé passe d’une équipe, d’un emplacement ou d’un service à un autre, vous devez vous assurer que son accès aux équipes, emplacements ou services précédents est supprimé si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4928f-111">As that employee moves to other teams, locations, or departments, you need to ensure that their access to previous teams, locations, or departments are removed as needed.</span></span>
- <span data-ttu-id="4928f-112">Lorsque cet employé ou un invité quitte votre organisation, vous devez vous assurer qu’il a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="4928f-112">When that employee or a guest leaves your organization, you need to ensure their access is removed.</span></span>

<span data-ttu-id="4928f-113">Ceci est particulièrement important si votre organisation fait l’objet d’audits de sécurité pour déterminer si les comptes d’utilisateurs ont un niveau d’accès trop important, ce qui peut entraîner des amendes en cas de violation des réglementations régionales ou industrielles.</span><span class="sxs-lookup"><span data-stu-id="4928f-113">This is especially important if your organization is subject to security audits to determine if user accounts have too much access, which could result in fines if in violation of industry or regional regulations.</span></span>

<span data-ttu-id="4928f-114">Pour plus d’informations, voir la [vue d’ensemble des révisions d’accès.](https://docs.microsoft.com/azure/active-directory/governance/access-reviews-overview)</span><span class="sxs-lookup"><span data-stu-id="4928f-114">For more information, see the [overview of access reviews](https://docs.microsoft.com/azure/active-directory/governance/access-reviews-overview).</span></span>

<span data-ttu-id="4928f-115">Pour configurer différents types de révisions d’accès, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="4928f-115">See these articles to configure different types of access reviews:</span></span>

- [<span data-ttu-id="4928f-116">Groupes et applications</span><span class="sxs-lookup"><span data-stu-id="4928f-116">Groups and apps</span></span>](https://docs.microsoft.com/azure/active-directory/governance/create-access-review)
- [<span data-ttu-id="4928f-117">Rôles Azure AD</span><span class="sxs-lookup"><span data-stu-id="4928f-117">Azure AD roles</span></span>](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-how-to-start-security-review?toc=%2fazure%2factive-directory%2fgovernance%2ftoc.json)
- [<span data-ttu-id="4928f-118">Rôles de ressources Azure</span><span class="sxs-lookup"><span data-stu-id="4928f-118">Azure resource roles</span></span>](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-start-access-review?toc=%2fazure%2factive-directory%2fgovernance%2ftoc.json)

## <a name="set-up-azure-ad-entitlement-management"></a><span data-ttu-id="4928f-119">Configurer la gestion des droits Azure AD</span><span class="sxs-lookup"><span data-stu-id="4928f-119">Set up Azure AD entitlement management</span></span>

<span data-ttu-id="4928f-120">La gestion des droits Azure AD Wiht vous permet de gérer le cycle de vie des identités et des accès à grande échelle en automatisant les flux de travail de demande d’accès, les affectations d’accès, les avis et l’expiration.</span><span class="sxs-lookup"><span data-stu-id="4928f-120">Wiht Azure AD entitlement management, you can manage the identity and access lifecycle at scale by automating access request workflows, access assignments, reviews, and expiration.</span></span>

<span data-ttu-id="4928f-121">Vos employés ont besoin d’accéder à différents groupes, applications et sites pour effectuer leur travail.</span><span class="sxs-lookup"><span data-stu-id="4928f-121">Your employees need access to various groups, applications, and sites to perform their job.</span></span> <span data-ttu-id="4928f-122">La gestion de cet accès peut être difficile car les exigences changent, de nouvelles applications sont ajoutées ou les utilisateurs ont besoin de droits d’accès supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4928f-122">Managing this access can be challenging because requirements change, new applications are added, or users need additional access rights.</span></span> <span data-ttu-id="4928f-123">Lorsque vous collaborez avec d’autres organisations, vous ne savez peut-être pas qui dans l’autre organisation a besoin d’accéder aux ressources de votre organisation, et les utilisateurs externes ne connaissent pas les applications, les groupes ou les sites que votre organisation utilise.</span><span class="sxs-lookup"><span data-stu-id="4928f-123">When you collaborate with other organizations, you may not know who in the other organization needs access to your organization's resources, and outside users won't know what applications, groups, or sites your organization is using.</span></span>

<span data-ttu-id="4928f-124">La gestion des droits Azure AD peut vous aider à gérer plus efficacement l’accès aux groupes, applications et sites SharePoint pour les utilisateurs internes et externes.</span><span class="sxs-lookup"><span data-stu-id="4928f-124">Azure AD entitlement management can help you more efficiently manage access to groups, applications, and SharePoint sites for internal and outside users.</span></span>
 
<span data-ttu-id="4928f-125">Pour plus d’informations, voir la [vue d’ensemble de la gestion des droits Azure AD.](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-overview)</span><span class="sxs-lookup"><span data-stu-id="4928f-125">For more information, see the [overview of Azure AD entitlement management](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-overview).</span></span>
