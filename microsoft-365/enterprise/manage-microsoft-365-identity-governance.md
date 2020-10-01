---
title: Gérer Microsoft 365 Identity Governance
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
description: Découvrez comment utiliser les fonctionnalités de gouvernance d’identités Microsoft 365.
ms.openlocfilehash: d5bcafb5b452e693bf3ff706c436a9986eeeae76
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48328515"
---
# <a name="manage-microsoft-365-identity-governance"></a><span data-ttu-id="6bfd5-103">Gérer Microsoft 365 Identity Governance</span><span class="sxs-lookup"><span data-stu-id="6bfd5-103">Manage Microsoft 365 identity governance</span></span>

<span data-ttu-id="6bfd5-104">La gouvernance des identités s’intéresse à la protection, la surveillance et l’audit de l’accès aux ressources critiques, tout en assurant la productivité des employés.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-104">Identity governance is all about protecting, monitoring, and auditing access to critical assets while ensuring employee productivity.</span></span> <span data-ttu-id="6bfd5-105">Par exemple, avec la gouvernance des identités, vous pouvez vous assurer que les utilisateurs appropriés disposent de l’accès approprié aux ressources adéquates et déterminer si cet accès change au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-105">For example, with identity governance, you can ensure that the right users have the right access to the right resources and determine if that access changes over time.</span></span>

<span data-ttu-id="6bfd5-106">Pour plus d’informations, consultez cette [vue d’ensemble de la gouvernance des identités pour Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/governance/identity-governance-overview).</span><span class="sxs-lookup"><span data-stu-id="6bfd5-106">For more information, See this [overview of identity governance for Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/governance/identity-governance-overview).</span></span>

## <a name="set-up-azure-ad-access-reviews"></a><span data-ttu-id="6bfd5-107">Configurer les révisions d’accès Azure AD</span><span class="sxs-lookup"><span data-stu-id="6bfd5-107">Set up Azure AD access reviews</span></span>

<span data-ttu-id="6bfd5-108">Les révisions Azure AD Access vous permettent de vérifier l’accès d’un utilisateur afin de s’assurer que seules les personnes appropriées disposent d’un accès continu.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-108">Azure AD access reviews allow you to review a user's access to ensure only the right people have continued access.</span></span> <span data-ttu-id="6bfd5-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6bfd5-109">For example:</span></span>

- <span data-ttu-id="6bfd5-110">Lorsqu’un nouvel employé rejoint votre organisation, vous devez vous assurer qu’il dispose d’un accès approprié pour être productif.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-110">As a new employee joins your organization, you need to ensure they have the right access to be productive.</span></span>
- <span data-ttu-id="6bfd5-111">Au fur et à mesure que cet employé passe d’une équipe, d’un emplacement ou d’un service à un autre, vous devez vous assurer que son accès aux équipes, emplacements ou services précédents est supprimé si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-111">As that employee moves to other teams, locations, or departments, you need to ensure that their access to previous teams, locations, or departments are removed as needed.</span></span>
- <span data-ttu-id="6bfd5-112">Lorsque cet employé ou un invité quitte votre organisation, vous devez vous assurer qu’il a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-112">When that employee or a guest leaves your organization, you need to ensure their access is removed.</span></span>

<span data-ttu-id="6bfd5-113">Ceci est particulièrement important si votre organisation fait l’objet d’audits de sécurité pour déterminer si les comptes d’utilisateurs ont un niveau d’accès trop important, ce qui peut entraîner des amendes en cas de violation des réglementations régionales ou industrielles.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-113">This is especially important if your organization is subject to security audits to determine if user accounts have too much access, which could result in fines if in violation of industry or regional regulations.</span></span>

<span data-ttu-id="6bfd5-114">Pour plus d’informations, consultez la rubrique [vue d’ensemble des révisions Access](https://docs.microsoft.com/azure/active-directory/governance/access-reviews-overview).</span><span class="sxs-lookup"><span data-stu-id="6bfd5-114">For more information, see the [overview of access reviews](https://docs.microsoft.com/azure/active-directory/governance/access-reviews-overview).</span></span>

<span data-ttu-id="6bfd5-115">Azure AD Privileged Identity Management (PIM) offre des contrôles supplémentaires conçus pour sécuriser les droits d’accès aux ressources dans Azure AD, Azure et d’autres services de cloud computing Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-115">Azure AD Privileged Identity Management (PIM) provides additional controls tailored to securing access rights for resources, across Azure AD, Azure, and other Microsoft cloud service.</span></span> <span data-ttu-id="6bfd5-116">Azure AD PIM fournit un ensemble complet de contrôles de gouvernance pour vous aider à sécuriser les ressources de votre entreprise telles que le répertoire, Office 365 et les rôles de ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-116">Azure AD PIM provides a comprehensive set of governance controls to help secure your company's resources such as directory, Office 365, and Azure resource roles.</span></span> <span data-ttu-id="6bfd5-117">Comme avec d’autres formes d’accès, les organisations peuvent utiliser les révisions d’accès pour configurer une recertification récurrente des accès pour tous les utilisateurs bénéficiant de rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-117">As with other forms of access, organizations can use access reviews to configure recurring access recertification for all users in administrator roles.</span></span> <span data-ttu-id="6bfd5-118">Azure AD PIM est disponible uniquement avec la version E5 de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-118">Azure AD PIM is only available with the E5 version of Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="6bfd5-119">Pour configurer différents types de révisions d’accès, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="6bfd5-119">See these articles to configure different types of access reviews:</span></span>

- [<span data-ttu-id="6bfd5-120">Groupes et applications</span><span class="sxs-lookup"><span data-stu-id="6bfd5-120">Groups and apps</span></span>](https://docs.microsoft.com/azure/active-directory/governance/create-access-review)
- [<span data-ttu-id="6bfd5-121">Rôles Azure AD</span><span class="sxs-lookup"><span data-stu-id="6bfd5-121">Azure AD roles</span></span>](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-how-to-start-security-review?toc=%2fazure%2factive-directory%2fgovernance%2ftoc.json)
- [<span data-ttu-id="6bfd5-122">Rôles de ressources Azure</span><span class="sxs-lookup"><span data-stu-id="6bfd5-122">Azure resource roles</span></span>](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-start-access-review?toc=%2fazure%2factive-directory%2fgovernance%2ftoc.json)

## <a name="set-up-azure-ad-entitlement-management"></a><span data-ttu-id="6bfd5-123">Configurer la gestion des droits Azure AD</span><span class="sxs-lookup"><span data-stu-id="6bfd5-123">Set up Azure AD entitlement management</span></span>

<span data-ttu-id="6bfd5-124">Wiht Azure AD admises, vous pouvez gérer le cycle de vie des identités et des accès à l’horizontale en automatisant les flux de travail de demande d’accès, les attributions d’accès, les révisions et l’expiration.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-124">Wiht Azure AD entitlement management, you can manage the identity and access lifecycle at scale by automating access request workflows, access assignments, reviews, and expiration.</span></span>

<span data-ttu-id="6bfd5-125">Vos employés ont besoin d’accéder à différents groupes, applications et sites pour effectuer leur travail.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-125">Your employees need access to various groups, applications, and sites to perform their job.</span></span> <span data-ttu-id="6bfd5-126">La gestion de cet accès peut être complexe, car les exigences changent, que de nouvelles applications sont ajoutées ou que les utilisateurs ont besoin de droits d’accès supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-126">Managing this access can be challenging because requirements change, new applications are added, or users need additional access rights.</span></span> <span data-ttu-id="6bfd5-127">Lorsque vous collaborez avec d’autres organisations, vous pouvez ne pas savoir qui a besoin d’accéder aux ressources de votre organisation dans l’autre organisation, et les utilisateurs externes ne sauront pas quelles applications, quels groupes ou quels sites votre organisation utilise.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-127">When you collaborate with other organizations, you may not know who in the other organization needs access to your organization's resources, and outside users won't know what applications, groups, or sites your organization is using.</span></span>

<span data-ttu-id="6bfd5-128">La gestion des droits Azure AD peut vous aider à gérer plus efficacement l’accès aux groupes, aux applications et aux sites SharePoint pour les utilisateurs internes et externes.</span><span class="sxs-lookup"><span data-stu-id="6bfd5-128">Azure AD entitlement management can help you more efficiently manage access to groups, applications, and SharePoint sites for internal and outside users.</span></span>
 
<span data-ttu-id="6bfd5-129">Pour plus d’informations, reportez-vous à la rubrique [vue d’ensemble de la gestion des droits Azure ad](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-overview).</span><span class="sxs-lookup"><span data-stu-id="6bfd5-129">For more information, see the [overview of Azure AD entitlement management](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-overview).</span></span>
