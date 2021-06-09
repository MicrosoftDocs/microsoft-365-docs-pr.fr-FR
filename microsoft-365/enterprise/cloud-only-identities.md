---
title: Microsoft 365 identité cloud uniquement
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/30/2020
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- O365p_AddUsersWithDirSync
- O365M_AddUsersWithDirSync
- O365E_HRCSetupAADConnectAboutLM617031
- O365E_AddUsersWithDirSync
ms.collection:
- Ent_O365
- M365-identity-device-management
search.appverid:
- MET150
- MOP150
- MOE150
- MBS150
ms.assetid: 01920974-9e6f-4331-a370-13aea4e82b3e
description: Décrit comment créer des utilisateurs et des groupes lorsque votre abonnement Microsoft 365 utilise l’identité cloud uniquement.
ms.openlocfilehash: 111c42e644913a8f7f6e41d4e8bf65685263f757
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48327926"
---
# <a name="microsoft-365-cloud-only-identity"></a><span data-ttu-id="f62b1-103">Microsoft 365 identité cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="f62b1-103">Microsoft 365 cloud-only identity</span></span>

<span data-ttu-id="f62b1-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="f62b1-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="f62b1-105">Avec l’identité cloud uniquement, tous vos utilisateurs, groupes et contacts sont stockés dans le client Azure Active Directory (Azure AD) de votre abonnement Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="f62b1-105">With cloud-only identity, all your users, groups, and contacts are stored in the Azure Active Directory (Azure AD) tenant of your Microsoft 365 subscription.</span></span> <span data-ttu-id="f62b1-106">Voici les composants de base de l’identité cloud uniquement.</span><span class="sxs-lookup"><span data-stu-id="f62b1-106">Here are the basic components of cloud-only identity.</span></span>
 
![Composants de base de l’identité cloud uniquement](../media/about-microsoft-365-identity/cloud-only-identity.png)

<span data-ttu-id="f62b1-108">Les utilisateurs et leurs comptes d’utilisateurs dans les organisations peuvent être classés de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="f62b1-108">Users and their user accounts in organizations can be categorized in a number of ways.</span></span> <span data-ttu-id="f62b1-109">Par exemple, certains sont des employés et ont un statut permanent.</span><span class="sxs-lookup"><span data-stu-id="f62b1-109">For example, some are employees and have a permanent status.</span></span> <span data-ttu-id="f62b1-110">Certains fournisseurs, sous-traitants ou partenaires ont un statut temporaire.</span><span class="sxs-lookup"><span data-stu-id="f62b1-110">Some are vendors, contractors, or partners that have a temporary status.</span></span> <span data-ttu-id="f62b1-111">Certains sont des utilisateurs externes qui n’ont pas de compte d’utilisateur, mais qui doivent tout de même avoir accès à des services et des ressources spécifiques pour prendre en charge l’interaction et la collaboration.</span><span class="sxs-lookup"><span data-stu-id="f62b1-111">Some are external users that have no user accounts but must still be granted access to specific services and resources to support interaction and collaboration.</span></span> <span data-ttu-id="f62b1-112">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f62b1-112">For example:</span></span>

- <span data-ttu-id="f62b1-113">Les comptes client représentent les utilisateurs au sein de votre organisation auxquels vous octroyez une licence pour les services cloud</span><span class="sxs-lookup"><span data-stu-id="f62b1-113">Tenant accounts represent users within your organization that you license for cloud services</span></span>

- <span data-ttu-id="f62b1-114">Les comptes B2B représentent les utilisateurs externes à votre organisation que vous invitez à participer à la collaboration</span><span class="sxs-lookup"><span data-stu-id="f62b1-114">Business to Business (B2B) accounts represent users outside your organization that you invite to participate in collaboration</span></span>

<span data-ttu-id="f62b1-115">Faites le point sur les types d’utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f62b1-115">Take stock of the types of users in your organization.</span></span> <span data-ttu-id="f62b1-116">Quels sont les regroupements ?</span><span class="sxs-lookup"><span data-stu-id="f62b1-116">What are the groupings?</span></span> <span data-ttu-id="f62b1-117">Par exemple, vous pouvez grouper des utilisateurs par fonction ou objectif de haut niveau pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f62b1-117">For example, you can group users by high-level function or purpose to your organization.</span></span>

<span data-ttu-id="f62b1-p104">Par ailleurs, certains services cloud peuvent être partagés avec des utilisateurs externes à votre organisation sans comptes d’utilisateur. Vous devrez identifier ces groupes d’utilisateurs également.</span><span class="sxs-lookup"><span data-stu-id="f62b1-p104">Additionally, some cloud services can be shared with users outside your organization without any user accounts. You'll need to identify these groups of users as well.</span></span>

<span data-ttu-id="f62b1-120">Vous pouvez utiliser des groupes dans Azure AD à plusieurs fins qui simplifient la gestion de votre environnement cloud.</span><span class="sxs-lookup"><span data-stu-id="f62b1-120">You can use groups in Azure AD for several purposes that simplify management of your cloud environment.</span></span> <span data-ttu-id="f62b1-121">Par exemple, avec les groupes Azure AD, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="f62b1-121">For example, with Azure AD groups, you can:</span></span>

- <span data-ttu-id="f62b1-122">Utilisez la gestion des licences basée sur les groupes pour attribuer des licences Microsoft 365 à vos comptes d’utilisateurs automatiquement dès qu’elles sont ajoutées en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="f62b1-122">Use group-based licensing to assign licenses for Microsoft 365 to your user accounts automatically as soon as they are added as members.</span></span>
- <span data-ttu-id="f62b1-123">Ajoutez dynamiquement des comptes d’utilisateur à des groupes spécifiques en fonction des attributs de compte d’utilisateur, tels que le nom du service.</span><span class="sxs-lookup"><span data-stu-id="f62b1-123">Add user accounts to specific groups dynamically based on user account attributes, such as department name.</span></span>
- <span data-ttu-id="f62b1-124">Approvisionnement automatique des utilisateurs pour les applications SaaS (Software as a Service) et pour protéger l’accès à ces applications à l’aide de l’authentification multifacteur (MFA) et d’autres stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="f62b1-124">Automatically provision users for Software as a Service (SaaS) applications and to protect access to those applications with multi-factor authentication (MFA) and other Conditional Access policies.</span></span>
- <span data-ttu-id="f62b1-125">Fournir des autorisations et des niveaux d’accès pour SharePoint sites d’équipe En ligne.</span><span class="sxs-lookup"><span data-stu-id="f62b1-125">Provision permissions and levels of access for SharePoint Online team sites.</span></span>

## <a name="next-steps-for-cloud-only-identity"></a><span data-ttu-id="f62b1-126">Étapes suivantes pour l’identité cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="f62b1-126">Next steps for cloud-only identity</span></span>

- [<span data-ttu-id="f62b1-127">Gérer les comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f62b1-127">Manage user accounts</span></span>](manage-microsoft-365-accounts.md)
- [<span data-ttu-id="f62b1-128">Attribution de licences aux comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f62b1-128">Assign licenses to user accounts</span></span>](assign-licenses-to-user-accounts.md)
- [<span data-ttu-id="f62b1-129">Gérer les groupes et l’appartenance à un groupe</span><span class="sxs-lookup"><span data-stu-id="f62b1-129">Manage groups and group membership</span></span>](manage-microsoft-365-groups.md)
- [<span data-ttu-id="f62b1-130">Gérer les mots de passe de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f62b1-130">Manage user account passwords</span></span>](manage-microsoft-365-passwords.md)
