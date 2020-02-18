---
title: 'Étape 7 : Configurer la gouvernance des identités'
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
description: Comprendre et configurer la gouvernance des identités pour votre client Azure AD.
ms.openlocfilehash: 5b7b1c91735611046133a0247ae028ed090106fd
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42067351"
---
# <a name="step-6-configure-identity-governance"></a><span data-ttu-id="5b282-103">Étape 6 : Configurer la gouvernance des identités</span><span class="sxs-lookup"><span data-stu-id="5b282-103">Step 6: Configure identity governance</span></span>

![Phase 2 - Identité](../media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="5b282-105">La gouvernance des identités s’intéresse à la protection, la surveillance et l’audit de l’accès aux ressources critiques, tout en assurant la productivité des employés.</span><span class="sxs-lookup"><span data-stu-id="5b282-105">Identity governance is all about protecting, monitoring, and auditing access to critical assets while ensuring employee productivity.</span></span> <span data-ttu-id="5b282-106">Par exemple, avec la gouvernance des identités, vous pouvez vous assurer que les utilisateurs appropriés disposent de l’accès approprié aux ressources adéquates et déterminer si cet accès change au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="5b282-106">For example, with identity governance, you can ensure that the right users have the right access to the right resources and determine if that access changes over time.</span></span>

<span data-ttu-id="5b282-107">Pour plus d' informations sur la gouvernance des identités pour Azure Active Directory (Azure AD), consultez [cet article](https://docs.microsoft.com/azure/active-directory/governance/identity-governance-overview).</span><span class="sxs-lookup"><span data-stu-id="5b282-107">See [this article](https://docs.microsoft.com/azure/active-directory/governance/identity-governance-overview) for more information about identity governance for Azure Active Directory (Azure AD).</span></span>


<span data-ttu-id="5b282-108">*Cette étape est facultative et s’applique uniquement à la version E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="5b282-108">*This is optional and applies only to the E5 version of Microsoft 365 Enterprise*</span></span>


<a name="identity-access-reviews"></a>
## <a name="set-up-azure-ad-access-reviews"></a><span data-ttu-id="5b282-109">Configurer les révisions d’accès Azure AD</span><span class="sxs-lookup"><span data-stu-id="5b282-109">Set up Azure AD access reviews</span></span>

<span data-ttu-id="5b282-110">*Cette étape est facultative et s’applique uniquement à la version E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="5b282-110">*This is optional and only applies to the E5 version of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="5b282-111">Dans cette étape, vous allez configurer les révisions d’accès Azure AD qui vous permettent de passer en revue l’accès d’un utilisateur afin de garantir l’accès permanent aux seules personnes appropriées.</span><span class="sxs-lookup"><span data-stu-id="5b282-111">In this step, you'll set up Azure AD access reviews, which allow you to review a user's access to ensure only the right people have continued access.</span></span> <span data-ttu-id="5b282-112">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="5b282-112">For example:</span></span>

- <span data-ttu-id="5b282-113">Lorsqu’un nouvel employé rejoint votre organisation, vous devez vous assurer qu’il dispose d’un accès approprié pour être productif.</span><span class="sxs-lookup"><span data-stu-id="5b282-113">As a new employee joins your organization, you need to ensure they have the right access to be productive.</span></span>
- <span data-ttu-id="5b282-114">Au fur et à mesure que cet employé passe d’une équipe, d’un emplacement ou d’un service à un autre, vous devez vous assurer que son accès aux équipes, emplacements ou services précédents est supprimé si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5b282-114">As that employee moves to other teams, locations, or departments, you need to ensure that their access to previous teams, locations, or departments are removed as needed.</span></span>
- <span data-ttu-id="5b282-115">Lorsque cet employé ou un invité quitte votre organisation, vous devez vous assurer qu’il a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="5b282-115">When that employee or a guest leaves your organization, you need to ensure their access is removed.</span></span>

<span data-ttu-id="5b282-116">Ceci est particulièrement important si votre organisation fait l’objet d’audits de sécurité pour déterminer si les comptes d’utilisateurs ont un niveau d’accès trop important, ce qui peut entraîner des amendes en cas de violation des réglementations régionales ou industrielles.</span><span class="sxs-lookup"><span data-stu-id="5b282-116">This is especially important if your organization is subject to security audits to determine if user accounts have too much access, which could result in fines if in violation of industry or regional regulations.</span></span>

<span data-ttu-id="5b282-117">Consultez [cet article](https://docs.microsoft.com/azure/active-directory/governance/access-reviews-overview) pour plus d’informations sur les révisions d’accès Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5b282-117">See [this article](https://docs.microsoft.com/azure/active-directory/governance/access-reviews-overview) for more information about Azure AD access reviews.</span></span>

<span data-ttu-id="5b282-118">Azure AD Privileged Identity Management (PIM) offre des contrôles supplémentaires conçus pour sécuriser les droits d’accès aux ressources dans Azure AD, Azure et d’autres services de cloud computing Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5b282-118">Azure AD Privileged Identity Management (PIM) provides additional controls tailored to securing access rights for resources, across Azure AD, Azure, and other Microsoft cloud service.</span></span> <span data-ttu-id="5b282-119">Azure AD PIM fournit un ensemble complet de contrôles de gouvernance pour vous aider à sécuriser les ressources de votre entreprise telles que le répertoire, Office 365 et les rôles de ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="5b282-119">Azure AD PIM provides a comprehensive set of governance controls to help secure your company's resources such as directory, Office 365, and Azure resource roles.</span></span> <span data-ttu-id="5b282-120">Comme avec d’autres formes d’accès, les organisations peuvent utiliser les révisions d’accès pour configurer une recertification récurrente des accès pour tous les utilisateurs bénéficiant de rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="5b282-120">As with other forms of access, organizations can use access reviews to configure recurring access recertification for all users in administrator roles.</span></span> <span data-ttu-id="5b282-121">Azure AD PIM est disponible uniquement avec la version E5 de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="5b282-121">Azure AD PIM is only available with the E5 version of Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="5b282-122">Pour configurer différents types de révisions d’accès, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="5b282-122">See these articles to configure different types of access reviews:</span></span>

- [<span data-ttu-id="5b282-123">Groupes et applications</span><span class="sxs-lookup"><span data-stu-id="5b282-123">Groups and apps</span></span>](https://docs.microsoft.com/azure/active-directory/governance/create-access-review)
- [<span data-ttu-id="5b282-124">Rôles Azure AD</span><span class="sxs-lookup"><span data-stu-id="5b282-124">Azure AD roles</span></span>](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-how-to-start-security-review?toc=%2fazure%2factive-directory%2fgovernance%2ftoc.json)
- [<span data-ttu-id="5b282-125">Rôles de ressources Azure</span><span class="sxs-lookup"><span data-stu-id="5b282-125">Azure resource roles</span></span>](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-start-access-review?toc=%2fazure%2factive-directory%2fgovernance%2ftoc.json)

<span data-ttu-id="5b282-126">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-access-reviews) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="5b282-126">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-access-reviews) for this section.</span></span>

## <a name="next-step"></a><span data-ttu-id="5b282-127">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="5b282-127">Next step</span></span>

[<span data-ttu-id="5b282-128"> Identifier les critères de sortie de l’infrastructure</span><span class="sxs-lookup"><span data-stu-id="5b282-128">Identity infrastructure exit criteria</span></span>](identity-exit-criteria.md)

