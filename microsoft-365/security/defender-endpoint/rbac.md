---
title: Utiliser le contrôle d’accès basé sur les rôles pour accorder un accès fin au Centre de sécurité Microsoft Defender
description: Créez des rôles et des groupes au sein de vos opérations de sécurité pour accorder l’accès au portail.
keywords: rbac, role, based, access, control, groups, control, tier, aad
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: d95163bd7caf6e05295fc35b3f9c2bf95230dc83
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063841"
---
# <a name="manage-portal-access-using-role-based-access-control"></a><span data-ttu-id="c840e-104">Gérer l’accès au portail à l’aide du contrôle d’accès basé sur un rôle</span><span class="sxs-lookup"><span data-stu-id="c840e-104">Manage portal access using role-based access control</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c840e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c840e-105">**Applies to:**</span></span>
- <span data-ttu-id="c840e-106">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c840e-106">Azure Active Directory</span></span>
- <span data-ttu-id="c840e-107">Office 365</span><span class="sxs-lookup"><span data-stu-id="c840e-107">Office 365</span></span>

> <span data-ttu-id="c840e-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="c840e-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="c840e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c840e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-rbac-abovefoldlink)

<span data-ttu-id="c840e-110">À l’aide du contrôle d’accès basé sur un rôle (RBAC), vous pouvez créer des rôles et des groupes au sein de votre équipe des opérations de sécurité pour accorder un accès approprié au portail.</span><span class="sxs-lookup"><span data-stu-id="c840e-110">Using role-based access control (RBAC), you can create roles and groups within your security operations team to grant appropriate access to the  portal.</span></span> <span data-ttu-id="c840e-111">En fonction des rôles et des groupes que vous créez, vous avez un contrôle fin sur ce que les utilisateurs ayant accès au portail peuvent voir et faire.</span><span class="sxs-lookup"><span data-stu-id="c840e-111">Based on the roles and groups you create, you have fine-grained control over what users with access to the portal can see and do.</span></span> 

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4bJ2a]

<span data-ttu-id="c840e-112">Les grandes équipes d’opérations de sécurité distribuées géographiquement adoptent généralement un modèle basé sur un niveau pour attribuer et autoriser l’accès aux portails de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c840e-112">Large geo-distributed security operations teams typically adopt a tier-based model to assign and authorize access to security portals.</span></span> <span data-ttu-id="c840e-113">Les niveaux classiques incluent les trois niveaux suivants :</span><span class="sxs-lookup"><span data-stu-id="c840e-113">Typical tiers include the following three levels:</span></span>

<span data-ttu-id="c840e-114">Niveau</span><span class="sxs-lookup"><span data-stu-id="c840e-114">Tier</span></span> | <span data-ttu-id="c840e-115">Description</span><span class="sxs-lookup"><span data-stu-id="c840e-115">Description</span></span>
:---|:---
<span data-ttu-id="c840e-116">Niveau 1</span><span class="sxs-lookup"><span data-stu-id="c840e-116">Tier 1</span></span> | <span data-ttu-id="c840e-117">**Équipe locale des opérations de sécurité/équipe informatique**</span><span class="sxs-lookup"><span data-stu-id="c840e-117">**Local security operations team / IT team**</span></span> <br> <span data-ttu-id="c840e-118">Cette équipe trie et examine généralement les alertes contenues dans leur géolocalisation et atteint le niveau 2 dans les cas où une correction active est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c840e-118">This team usually triages and investigates alerts contained within their geolocation and escalates to Tier 2 in cases where an active remediation is required.</span></span>
<span data-ttu-id="c840e-119">Niveau 2</span><span class="sxs-lookup"><span data-stu-id="c840e-119">Tier 2</span></span> | <span data-ttu-id="c840e-120">**Équipe des opérations de sécurité régionale**</span><span class="sxs-lookup"><span data-stu-id="c840e-120">**Regional security operations team**</span></span> <br> <span data-ttu-id="c840e-121">Cette équipe peut voir tous les appareils de leur région et effectuer des actions de correction.</span><span class="sxs-lookup"><span data-stu-id="c840e-121">This team can see all the devices for their region and perform remediation actions.</span></span>
<span data-ttu-id="c840e-122">Niveau 3</span><span class="sxs-lookup"><span data-stu-id="c840e-122">Tier 3</span></span> | <span data-ttu-id="c840e-123">**Équipe des opérations de sécurité globale**</span><span class="sxs-lookup"><span data-stu-id="c840e-123">**Global security operations team**</span></span> <br> <span data-ttu-id="c840e-124">Cette équipe est constituée d’experts en sécurité et est autorisée à voir et à effectuer toutes les actions à partir du portail.</span><span class="sxs-lookup"><span data-stu-id="c840e-124">This team consists of security experts and are authorized to see and perform all actions from the portal.</span></span>

<span data-ttu-id="c840e-125">Defender for Endpoint RBAC est conçu pour prendre en charge votre modèle de choix basé sur des rôles ou des niveaux et vous donne un contrôle granulaire sur les rôles qu’ils peuvent voir, les appareils accessibles et les actions qu’ils peuvent prendre.</span><span class="sxs-lookup"><span data-stu-id="c840e-125">Defender for Endpoint RBAC is designed to support your tier- or role-based model of choice and gives you granular control over what roles can see, devices they can access, and actions they can take.</span></span> <span data-ttu-id="c840e-126">L’infrastructure RBAC est centrée autour des contrôles suivants :</span><span class="sxs-lookup"><span data-stu-id="c840e-126">The RBAC framework is centered around the following controls:</span></span>

- <span data-ttu-id="c840e-127">**Contrôler les personnes qui peuvent prendre des mesures spécifiques**</span><span class="sxs-lookup"><span data-stu-id="c840e-127">**Control who can take specific action**</span></span>
  - <span data-ttu-id="c840e-128">Créez des rôles personnalisés et contrôlez les fonctionnalités de Defender for Endpoint accessibles avec granularité.</span><span class="sxs-lookup"><span data-stu-id="c840e-128">Create custom roles and control what Defender for Endpoint capabilities they can access with granularity.</span></span>
 
- <span data-ttu-id="c840e-129">**Contrôler qui peut voir les informations sur un ou plusieurs groupes d’appareils spécifiques**</span><span class="sxs-lookup"><span data-stu-id="c840e-129">**Control who can see information on specific device group or groups**</span></span>
  - <span data-ttu-id="c840e-130">[Créez](machine-groups.md) des groupes d’appareils en fonction de critères spécifiques tels que des noms, des balises, des domaines et d’autres, puis accordez-leur l’accès au rôle à l’aide d’un groupe d’utilisateurs Azure Active Directory (Azure AD) spécifique.</span><span class="sxs-lookup"><span data-stu-id="c840e-130">[Create device groups](machine-groups.md) by specific criteria such as names, tags, domains, and others, then grant role access to them using a specific  Azure Active Directory (Azure AD) user group.</span></span>

<span data-ttu-id="c840e-131">Pour implémenter l’accès basé sur les rôles, vous devez définir des rôles d’administrateur, attribuer des autorisations correspondantes et affecter des groupes d’utilisateurs Azure AD affectés aux rôles.</span><span class="sxs-lookup"><span data-stu-id="c840e-131">To implement role-based access, you'll need to define admin roles, assign corresponding permissions, and assign Azure AD user groups assigned to the roles.</span></span>


### <a name="before-you-begin"></a><span data-ttu-id="c840e-132">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c840e-132">Before you begin</span></span>
<span data-ttu-id="c840e-133">Avant d’utiliser le RBAC, il est important de comprendre les rôles qui peuvent accorder des autorisations et les conséquences de l’utilisation du RBAC.</span><span class="sxs-lookup"><span data-stu-id="c840e-133">Before using RBAC, it's important that you understand the roles that can grant permissions and the consequences of turning on RBAC.</span></span>


> [!WARNING]
> <span data-ttu-id="c840e-134">Avant d’activer la fonctionnalité, il est important que vous disposez d’un rôle d’administrateur général ou d’administrateur de la sécurité dans Azure AD et que vos groupes Azure AD sont prêts à réduire le risque d’être verrouillé du portail.</span><span class="sxs-lookup"><span data-stu-id="c840e-134">Before enabling the feature, it's important that you have a Global Administrator role or Security Administrator role in Azure AD and that you have your Azure AD groups ready to reduce the risk of being locked out of the portal.</span></span> 

<span data-ttu-id="c840e-135">Lorsque vous vous connectez pour la première fois au Centre de sécurité Microsoft Defender, l’accès complet ou l’accès en lecture seule vous est accordé.</span><span class="sxs-lookup"><span data-stu-id="c840e-135">When you first log in to Microsoft Defender Security Center, you're granted either full access or read only access.</span></span> <span data-ttu-id="c840e-136">Les droits d’accès total sont accordés aux utilisateurs ayant des rôles Administrateur de sécurité ou Administrateur général dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c840e-136">Full access rights are granted to users with Security Administrator or Global Administrator roles in Azure AD.</span></span> <span data-ttu-id="c840e-137">L’accès en lecture seule est accordé aux utilisateurs ayant un rôle de lecteur de sécurité dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c840e-137">Read only access is granted to users with a Security Reader role in Azure AD.</span></span> 

<span data-ttu-id="c840e-138">Une personne ayant un rôle d’administrateur général Defender pour point de terminaison dispose d’un accès illimité à tous les appareils, quelle que soit l’association de leur groupe d’appareils et les affectations des groupes d’utilisateurs Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c840e-138">Someone with a Defender for Endpoint Global administrator role has unrestricted access to all devices, regardless of their device group association and the Azure AD user groups assignments</span></span>

> [!WARNING]
> <span data-ttu-id="c840e-139">Initialement, seules les personnes ayant des droits d’administrateur général Azure AD ou d’administrateur de la sécurité pourront créer et attribuer des rôles dans le Centre de sécurité Microsoft Defender. Par conséquent, il est important que les groupes soient prêts dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c840e-139">Initially, only those with Azure AD Global Administrator or Security Administrator rights will be able to create and assign roles in Microsoft Defender Security Center, therefore, having the right groups ready in Azure AD is important.</span></span>
>
> <span data-ttu-id="c840e-140">**L’turning on role-based access control will cause users with read-only permissions (for example, users assigned to Azure AD Security reader role) to lose access until they are assigned to a role.**</span><span class="sxs-lookup"><span data-stu-id="c840e-140">**Turning on role-based access control will cause users with read-only permissions (for example, users assigned to Azure AD Security reader role) to lose access until they are assigned to a role.**</span></span> 
>
><span data-ttu-id="c840e-141">Le rôle d’administrateur général Defender for Endpoint intégré par défaut est automatiquement attribué aux utilisateurs ayant des autorisations d’administrateur avec des autorisations complètes.</span><span class="sxs-lookup"><span data-stu-id="c840e-141">Users with admin permissions are automatically assigned the default built-in Defender for Endpoint global administrator role with full permissions.</span></span> <span data-ttu-id="c840e-142">Après avoir choisi d’utiliser le contrôle d’accès en fonction du rôle, vous pouvez affecter d’autres utilisateurs qui ne sont pas des administrateurs globaux ou de sécurité Azure AD au rôle d’administrateur général Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="c840e-142">After opting in to use RBAC, you can assign additional users that are not Azure AD Global or Security Administrators to the Defender for Endpoint global administrator role.</span></span> 
>
> <span data-ttu-id="c840e-143">Après avoir choisi d’utiliser le RBAC, vous ne pouvez pas revenir aux rôles initiaux comme lorsque vous vous êtes connecté au portail pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="c840e-143">After opting in to use RBAC, you cannot revert to the initial roles as when you first logged into the portal.</span></span> 



## <a name="related-topic"></a><span data-ttu-id="c840e-144">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="c840e-144">Related topic</span></span>
- [<span data-ttu-id="c840e-145">Créer et gérer des groupes d’appareils dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c840e-145">Create and manage device groups in Microsoft Defender for Endpoint</span></span>](machine-groups.md)
