---
title: Gérer l’accès aux données Microsoft 365 Defender dans le centre de sécurité Microsoft 365
description: Découvrez comment gérer les autorisations d’accès aux données dans Microsoft 365 Defender
keywords: accès, autorisations, MTP, Protection Microsoft contre les menaces, M365, sécurité, MCAS, MDATP, Cloud App Security, Microsoft Defender – Protection avancée contre les menaces, étendue, contrôle, RBAC
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: 55b7b8c5755b773a4d53c95017a0a17a85495dee
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48847247"
---
# <a name="manage-access-to-microsoft-365-defender"></a><span data-ttu-id="f3e19-104">Gérer l’accès à Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f3e19-104">Manage access to Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="f3e19-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f3e19-105">**Applies to:**</span></span>
- <span data-ttu-id="f3e19-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f3e19-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="f3e19-107">Comptes affectés les rôles Azure Active Directory (AD) suivants peuvent accéder aux fonctionnalités et aux données de Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="f3e19-107">Accounts assigned the following Azure Active Directory (AD) roles can access Microsoft 365 Defender functionality and data:</span></span>
- <span data-ttu-id="f3e19-108">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="f3e19-108">Global administrator</span></span>
- <span data-ttu-id="f3e19-109">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="f3e19-109">Security administrator</span></span>
- <span data-ttu-id="f3e19-110">Opérateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="f3e19-110">Security Operator</span></span>
- <span data-ttu-id="f3e19-111">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="f3e19-111">Global Reader</span></span>
- <span data-ttu-id="f3e19-112">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="f3e19-112">Security Reader</span></span>

<span data-ttu-id="f3e19-113">Pour examiner les comptes avec ces rôles, [afficher les autorisations dans le Centre de sécurité Microsoft 365](https://security.microsoft.com/permissions).</span><span class="sxs-lookup"><span data-stu-id="f3e19-113">To review accounts with these roles, [view Permissions in the Microsoft 365 security center](https://security.microsoft.com/permissions).</span></span>

## <a name="access-to-functionality"></a><span data-ttu-id="f3e19-114">Accéder aux fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="f3e19-114">Access to functionality</span></span>
<span data-ttu-id="f3e19-115">L’accès à des fonctionnalités spécifiques est déterminé par votre[rôle Azure AD](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="f3e19-115">Access to specific functionality is determined by your [Azure AD role](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span></span> <span data-ttu-id="f3e19-116">Contactez un administrateur général si vous avez besoin d’accéder à des fonctionnalités spécifiques qui nécessitent l'affectation d'un nouveau rôle à vous ou à votre groupe d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f3e19-116">Contact a global administrator if you need access to specific functionality that requires you or your user group be assigned a new role.</span></span>

### <a name="approve-pending-automated-tasks"></a><span data-ttu-id="f3e19-117">Approuver les tâches automatisées en attente</span><span class="sxs-lookup"><span data-stu-id="f3e19-117">Approve pending automated tasks</span></span>
<span data-ttu-id="f3e19-118">[Un examen et correction automatisés](mtp-autoir-actions.md) peuvent prendre une action sur les e-mails, les règles de transfert, les fichiers, les mécanismes de persistance et d’autres artefacts détectés lors des examens.</span><span class="sxs-lookup"><span data-stu-id="f3e19-118">[Automated investigation and remediation](mtp-autoir-actions.md) can take action on emails, forwarding rules, files, persistence mechanisms, and other artifacts found during investigations.</span></span> <span data-ttu-id="f3e19-119">Pour approuver ou refuser les actions en attente qui nécessitent une autorisation explicite, vous devez avoir certains rôles affectés dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f3e19-119">To approve or reject pending actions that require explicit approval, you must have certain roles assigned in Microsoft 365.</span></span> <span data-ttu-id="f3e19-120">Si vous souhaitez en savoir plus, veuillez consulter[Autorisation du centre de notification](mtp-action-center.md#required-permissions-for-action-center-tasks).</span><span class="sxs-lookup"><span data-stu-id="f3e19-120">To learn more, see [Action center permissions](mtp-action-center.md#required-permissions-for-action-center-tasks).</span></span>

## <a name="access-to-data"></a><span data-ttu-id="f3e19-121">Accès aux données</span><span class="sxs-lookup"><span data-stu-id="f3e19-121">Access to data</span></span>
<span data-ttu-id="f3e19-122">L’accès aux données Microsoft 365 Defender peut être contrôlé à l’aide de l’étendue affectée aux groupes d’utilisateurs dans Microsoft Defender pour le contrôle d’accès basé sur un rôle de point de terminaison (RBAC).</span><span class="sxs-lookup"><span data-stu-id="f3e19-122">Access to Microsoft 365 Defender data can be controlled using the scope assigned to user groups in Microsoft Defender for Endpoint role-based access control (RBAC).</span></span> <span data-ttu-id="f3e19-123">Si votre accès n’est pas inclus dans l’étendue d’un ensemble spécifique d’appareils dans l’application Defender pour le point de terminaison, vous aurez un accès complet aux données dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="f3e19-123">If your access has not been scoped to a specific set of devices in the Defender for Endpoint, you will have full access to data in Microsoft 365 Defender.</span></span> <span data-ttu-id="f3e19-124">Cependant, une fois votre compte étendu, vous verrez uniquement les données relatives aux appareils dans votre étendue.</span><span class="sxs-lookup"><span data-stu-id="f3e19-124">However, once your account is scoped, you will only see data about the devices in your scope.</span></span>

<span data-ttu-id="f3e19-125">Par exemple, si vous appartenez à un seul groupe d’utilisateurs avec un rôle Microsoft Defender pour le point de terminaison et que ce groupe d’utilisateurs a été autorisé à accéder uniquement aux appareils de vente, vous verrez uniquement les données sur les périphériques de vente dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="f3e19-125">For example, if you belong to only one user group with a Microsoft Defender for Endpoint role and that user group has been given access to sales devices only, you will see only data about sales devices in Microsoft 365 Defender.</span></span> [<span data-ttu-id="f3e19-126">En savoir plus sur les paramètres RBAC dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f3e19-126">Learn more about RBAC settings in Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/rbac)

### <a name="microsoft-cloud-app-security-access-controls"></a><span data-ttu-id="f3e19-127">Contrôles d'accès Microsoft Cloud App Security (MCAS)</span><span class="sxs-lookup"><span data-stu-id="f3e19-127">Microsoft Cloud App Security access controls</span></span>
<span data-ttu-id="f3e19-128">Pendant l’aperçu, Microsoft 365 Defender n’applique pas les contrôles d’accès basés sur les paramètres de sécurité de l’application Cloud.</span><span class="sxs-lookup"><span data-stu-id="f3e19-128">During the preview, Microsoft 365 Defender does not enforce access controls based on  Cloud App Security settings.</span></span> <span data-ttu-id="f3e19-129">L’accès aux données Microsoft 365 Defender n’est pas affecté par ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="f3e19-129">Access to Microsoft 365 Defender data is not affected by these settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3e19-130">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="f3e19-130">Related topics</span></span>

- [<span data-ttu-id="f3e19-131">Rôles Azure AD</span><span class="sxs-lookup"><span data-stu-id="f3e19-131">Azure AD roles</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)
- [<span data-ttu-id="f3e19-132">Microsoft Defender pour le RBAC de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f3e19-132">Microsoft Defender for Endpoint RBAC</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/rbac)
- [<span data-ttu-id="f3e19-133">Rôles des sécurité de l’application cloud</span><span class="sxs-lookup"><span data-stu-id="f3e19-133">Cloud App Security roles</span></span>](https://docs.microsoft.com/cloud-app-security/manage-admins)
