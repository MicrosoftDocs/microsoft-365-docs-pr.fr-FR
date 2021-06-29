---
title: Gérer l’accès Microsoft 365 Defender données dans le centre Microsoft 365 sécurité
description: Découvrez comment gérer les autorisations d’accès aux données dans Microsoft 365 Defender
keywords: access, permissions, Microsoft 365 Defender, M365, security, MCAS, Sécurité des applications cloud, Microsoft Defender for Endpoint, scope, scoping, RBAC
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 738315c446fd57d4cd027de92eb77b0029f84323
ms.sourcegitcommit: cfd7644570831ceb7f57c61401df6a0001ef0a6a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "53177527"
---
# <a name="manage-access-to-microsoft-365-defender-with-azure-active-directory-global-roles"></a><span data-ttu-id="39924-104">Gérer l’accès aux Microsoft 365 Defender avec Azure Active Directory rôles globaux</span><span class="sxs-lookup"><span data-stu-id="39924-104">Manage access to Microsoft 365 Defender with Azure Active Directory global roles</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="39924-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="39924-105">**Applies to:**</span></span>
- <span data-ttu-id="39924-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="39924-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="39924-107">Il existe deux façons de gérer l’accès Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="39924-107">There are two ways to manage access to Microsoft 365 Defender</span></span>
- <span data-ttu-id="39924-108">**Rôles Azure Active Directory (AD) globaux**</span><span class="sxs-lookup"><span data-stu-id="39924-108">**Global Azure Active Directory (AD) roles**</span></span>
- <span data-ttu-id="39924-109">**Accès aux rôles personnalisés**</span><span class="sxs-lookup"><span data-stu-id="39924-109">**Custom role access**</span></span>

<span data-ttu-id="39924-110">Les comptes affectés aux rôles **Azure Active Directory global (AD)** suivants peuvent accéder aux Microsoft 365 Defender et aux données suivantes :</span><span class="sxs-lookup"><span data-stu-id="39924-110">Accounts assigned the following **Global Azure Active Directory (AD) roles** can access Microsoft 365 Defender functionality and data:</span></span>
- <span data-ttu-id="39924-111">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="39924-111">Global administrator</span></span>
- <span data-ttu-id="39924-112">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="39924-112">Security administrator</span></span>
- <span data-ttu-id="39924-113">Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="39924-113">Security Operator</span></span>
- <span data-ttu-id="39924-114">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="39924-114">Global Reader</span></span>
- <span data-ttu-id="39924-115">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="39924-115">Security Reader</span></span>

<span data-ttu-id="39924-116">Pour examiner les comptes avec ces rôles, [afficher les autorisations dans le Centre de sécurité Microsoft 365](https://security.microsoft.com/permissions).</span><span class="sxs-lookup"><span data-stu-id="39924-116">To review accounts with these roles, [view Permissions in the Microsoft 365 security center](https://security.microsoft.com/permissions).</span></span>

<span data-ttu-id="39924-117">**L’accès** aux rôles personnalisés est une nouvelle fonctionnalité de Microsoft 365 Defender et vous permet de gérer l’accès à des données, des tâches et des fonctionnalités spécifiques dans Microsoft Defender 365.</span><span class="sxs-lookup"><span data-stu-id="39924-117">**Custom role** access is a new capability in Microsoft 365 Defender and allows you to manage access to specific data, tasks, and capabilities in Microsoft Defender 365.</span></span> <span data-ttu-id="39924-118">Les rôles personnalisés offrent plus de contrôle que les rôles Azure AD globaux, fournissant aux utilisateurs uniquement l’accès dont ils ont besoin avec les rôles les moins permissifs nécessaires.</span><span class="sxs-lookup"><span data-stu-id="39924-118">Custom roles offer more control than global Azure AD roles, providing users only the access they need with the least-permissive roles necessary.</span></span>  <span data-ttu-id="39924-119">Les rôles personnalisés peuvent être créés en plus des rôles Azure AD globaux.</span><span class="sxs-lookup"><span data-stu-id="39924-119">Custom roles can be created in addition to global Azure AD roles.</span></span> <span data-ttu-id="39924-120">[En savoir plus sur les rôles personnalisés.](custom-roles.md)</span><span class="sxs-lookup"><span data-stu-id="39924-120">[Learn more about custom roles](custom-roles.md).</span></span>

> [!NOTE]
> <span data-ttu-id="39924-121">Cet article s’applique uniquement à la gestion des rôles Azure Active Directory globaux.</span><span class="sxs-lookup"><span data-stu-id="39924-121">This article applies only to managing global Azure Active Directory roles.</span></span> <span data-ttu-id="39924-122">Pour plus d’informations sur l’utilisation du contrôle d’accès basé sur un rôle personnalisé, voir [Rôles](custom-roles.md) personnalisés pour le contrôle d’accès basé sur un rôle</span><span class="sxs-lookup"><span data-stu-id="39924-122">For more information about using custom role-based access control, see [Custom roles for role-based access control](custom-roles.md)</span></span>

## <a name="access-to-functionality"></a><span data-ttu-id="39924-123">Accéder aux fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="39924-123">Access to functionality</span></span>
<span data-ttu-id="39924-124">L’accès à des fonctionnalités spécifiques est déterminé par votre[rôle Azure AD](/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="39924-124">Access to specific functionality is determined by your [Azure AD role](/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span></span> <span data-ttu-id="39924-125">Contactez un administrateur général si vous avez besoin d’accéder à des fonctionnalités spécifiques qui nécessitent l'affectation d'un nouveau rôle à vous ou à votre groupe d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="39924-125">Contact a global administrator if you need access to specific functionality that requires you or your user group be assigned a new role.</span></span>

### <a name="approve-pending-automated-tasks"></a><span data-ttu-id="39924-126">Approuver les tâches automatisées en attente</span><span class="sxs-lookup"><span data-stu-id="39924-126">Approve pending automated tasks</span></span>
<span data-ttu-id="39924-127">[Un examen et correction automatisés](m365d-autoir-actions.md) peuvent prendre une action sur les e-mails, les règles de transfert, les fichiers, les mécanismes de persistance et d’autres artefacts détectés lors des examens.</span><span class="sxs-lookup"><span data-stu-id="39924-127">[Automated investigation and remediation](m365d-autoir-actions.md) can take action on emails, forwarding rules, files, persistence mechanisms, and other artifacts found during investigations.</span></span> <span data-ttu-id="39924-128">Pour approuver ou refuser les actions en attente qui nécessitent une autorisation explicite, vous devez avoir certains rôles affectés dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="39924-128">To approve or reject pending actions that require explicit approval, you must have certain roles assigned in Microsoft 365.</span></span> <span data-ttu-id="39924-129">Si vous souhaitez en savoir plus, veuillez consulter[Autorisation du centre de notification](m365d-action-center.md#required-permissions-for-action-center-tasks).</span><span class="sxs-lookup"><span data-stu-id="39924-129">To learn more, see [Action center permissions](m365d-action-center.md#required-permissions-for-action-center-tasks).</span></span>

## <a name="access-to-data"></a><span data-ttu-id="39924-130">Accès aux données</span><span class="sxs-lookup"><span data-stu-id="39924-130">Access to data</span></span>
<span data-ttu-id="39924-131">L’accès Microsoft 365 Defender données peut être contrôlé à l’aide de l’étendue attribuée aux groupes d’utilisateurs dans Microsoft Defender for Endpoint role-based access control (RBAC).</span><span class="sxs-lookup"><span data-stu-id="39924-131">Access to Microsoft 365 Defender data can be controlled using the scope assigned to user groups in Microsoft Defender for Endpoint role-based access control (RBAC).</span></span> <span data-ttu-id="39924-132">Si votre accès n’a pas été limité à un ensemble spécifique d’appareils dans Defender for Endpoint, vous aurez un accès total aux données dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="39924-132">If your access has not been scoped to a specific set of devices in the Defender for Endpoint, you will have full access to data in Microsoft 365 Defender.</span></span> <span data-ttu-id="39924-133">Cependant, une fois votre compte étendu, vous verrez uniquement les données relatives aux appareils dans votre étendue.</span><span class="sxs-lookup"><span data-stu-id="39924-133">However, once your account is scoped, you will only see data about the devices in your scope.</span></span>

<span data-ttu-id="39924-134">Par exemple, si vous n’appartenez qu’à un seul groupe d’utilisateurs avec un rôle Microsoft Defender pour point de terminaison et que ce groupe d’utilisateurs n’a accès qu’aux appareils commerciaux, vous ne verrez que les données relatives aux appareils de vente dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="39924-134">For example, if you belong to only one user group with a Microsoft Defender for Endpoint role and that user group has been given access to sales devices only, you will see only data about sales devices in Microsoft 365 Defender.</span></span> [<span data-ttu-id="39924-135">En savoir plus sur les paramètres RBAC dans Microsoft Defender pour endpoint</span><span class="sxs-lookup"><span data-stu-id="39924-135">Learn more about RBAC settings in Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/microsoft-defender-atp/rbac)

### <a name="microsoft-cloud-app-security-access-controls"></a><span data-ttu-id="39924-136">Contrôles d'accès Microsoft Cloud App Security (MCAS)</span><span class="sxs-lookup"><span data-stu-id="39924-136">Microsoft Cloud App Security access controls</span></span>
<span data-ttu-id="39924-137">Pendant la prévisualisation, Microsoft 365 Defender n’applique pas les contrôles d’accès basés sur Sécurité des applications cloud paramètres.</span><span class="sxs-lookup"><span data-stu-id="39924-137">During the preview, Microsoft 365 Defender does not enforce access controls based on  Cloud App Security settings.</span></span> <span data-ttu-id="39924-138">L’accès Microsoft 365 Defender données n’est pas affecté par ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="39924-138">Access to Microsoft 365 Defender data is not affected by these settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39924-139">Sujets connexes</span><span class="sxs-lookup"><span data-stu-id="39924-139">Related topics</span></span>
- [<span data-ttu-id="39924-140">Rôles personnalisés dans le contrôle d’accès basé sur les rôles pour Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="39924-140">Custom roles in role-based access control for Microsoft 365 Defender</span></span>](custom-roles.md)
- [<span data-ttu-id="39924-141">Rôles Azure AD</span><span class="sxs-lookup"><span data-stu-id="39924-141">Azure AD roles</span></span>](/azure/active-directory/users-groups-roles/directory-assign-admin-roles)
- [<span data-ttu-id="39924-142">Microsoft Defender pour point de terminaison RBAC</span><span class="sxs-lookup"><span data-stu-id="39924-142">Microsoft Defender for Endpoint RBAC</span></span>](/windows/security/threat-protection/microsoft-defender-atp/rbac)
- [<span data-ttu-id="39924-143">Rôles des sécurité de l’application cloud</span><span class="sxs-lookup"><span data-stu-id="39924-143">Cloud App Security roles</span></span>](/cloud-app-security/manage-admins)
