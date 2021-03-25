---
title: Attribuer l’accès utilisateur au Centre de sécurité Microsoft Defender
description: Attribuez un accès en lecture et en écriture ou en lecture seule au portail Microsoft Defender for Endpoint.
keywords: attribuer des rôles d’utilisateur, attribuer un accès en lecture et en écriture, attribuer un accès en lecture seule, utilisateur, rôles d’utilisateur, rôles
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
ms.date: 11/28/2018
ms.technology: mde
ms.openlocfilehash: 71215c4988351644cfa4d79503c097c932caf9d6
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51164757"
---
# <a name="assign-user-access-to-microsoft-defender-security-center"></a><span data-ttu-id="baa54-104">Attribuer l’accès utilisateur au Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="baa54-104">Assign user access to Microsoft Defender Security Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="baa54-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="baa54-105">**Applies to:**</span></span>
- <span data-ttu-id="baa54-106">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="baa54-106">Azure Active Directory</span></span>
- <span data-ttu-id="baa54-107">Office 365</span><span class="sxs-lookup"><span data-stu-id="baa54-107">Office 365</span></span>
- [<span data-ttu-id="baa54-108">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="baa54-108">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="baa54-109">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="baa54-109">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="baa54-110">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="baa54-110">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="baa54-111">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="baa54-111">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="baa54-112">Defender pour le point de terminaison prend en charge deux façons de gérer les autorisations :</span><span class="sxs-lookup"><span data-stu-id="baa54-112">Defender for Endpoint supports two ways to manage permissions:</span></span>

- <span data-ttu-id="baa54-113">**Gestion des autorisations de base**: définissez les autorisations en accès total ou en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="baa54-113">**Basic permissions management**: Set permissions to either full access or read-only.</span></span>
- <span data-ttu-id="baa54-114">Contrôle d’accès basé sur un rôle **(RBAC)**: définissez des autorisations granulaires en définissant des rôles, en attribuant des groupes d’utilisateurs Azure AD aux rôles et en accordant aux groupes d’utilisateurs l’accès aux groupes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="baa54-114">**Role-based access control (RBAC)**: Set granular permissions by defining roles, assigning Azure AD user groups to the roles, and granting the user groups access to device groups.</span></span> <span data-ttu-id="baa54-115">Pour plus d’informations sur le contrôle d’accès basé sur un rôle, voir Gérer l’accès au portail à l’aide du contrôle [d’accès basé sur un rôle.](rbac.md)</span><span class="sxs-lookup"><span data-stu-id="baa54-115">For more information on RBAC, see [Manage portal access using role-based access control](rbac.md).</span></span>

> [!NOTE]
> <span data-ttu-id="baa54-116">Si vous avez déjà attribué des autorisations de base, vous pouvez basculer vers RBAC à tout moment.</span><span class="sxs-lookup"><span data-stu-id="baa54-116">If you have already assigned basic permissions, you may switch to RBAC anytime.</span></span> <span data-ttu-id="baa54-117">Prenons les considérations suivantes avant d’effectuer le basculement :</span><span class="sxs-lookup"><span data-stu-id="baa54-117">Consider the following before making the switch:</span></span>
> 
> - <span data-ttu-id="baa54-118">Les utilisateurs ayant un accès total (utilisateurs affectés au rôle d’administrateur général ou d’administrateur de sécurité dans Azure AD) se voit automatiquement attribuer le rôle d’administrateur Defender pour point de terminaison par défaut, qui dispose également d’un accès total.</span><span class="sxs-lookup"><span data-stu-id="baa54-118">Users with full access (users that are assigned the Global Administrator or Security Administrator directory role in Azure AD), are automatically assigned the default Defender for Endpoint administrator role, which also has full access.</span></span> <span data-ttu-id="baa54-119">Des groupes d’utilisateurs Azure AD supplémentaires peuvent être affectés au rôle d’administrateur Defender for Endpoint après le passage au RBAC.</span><span class="sxs-lookup"><span data-stu-id="baa54-119">Additional Azure AD user groups can be assigned to the Defender for Endpoint administrator role after switching to RBAC.</span></span>  <span data-ttu-id="baa54-120">Seuls les utilisateurs affectés au rôle d’administrateur Defender pour le point de terminaison peuvent gérer les autorisations à l’aide du contrôle d’accès en fonction du rôle.</span><span class="sxs-lookup"><span data-stu-id="baa54-120">Only users assigned to the Defender for Endpoint administrator role can manage permissions using RBAC.</span></span> 
> - <span data-ttu-id="baa54-121">Les utilisateurs qui ont un accès en lecture seule (lecteurs de sécurité) perdent l’accès au portail tant qu’un rôle ne leur est pas attribué.</span><span class="sxs-lookup"><span data-stu-id="baa54-121">Users that have read-only access (Security Readers) will lose access to the portal until they are assigned a role.</span></span> <span data-ttu-id="baa54-122">Notez que seuls les groupes d’utilisateurs Azure AD peuvent se voir attribuer un rôle sous RBAC.</span><span class="sxs-lookup"><span data-stu-id="baa54-122">Note that only Azure AD user groups can be assigned a role under RBAC.</span></span>
> - <span data-ttu-id="baa54-123">Après avoir basé vers RBAC, vous ne pourrez pas revenir à l’utilisation de la gestion des autorisations de base.</span><span class="sxs-lookup"><span data-stu-id="baa54-123">After switching to RBAC, you will not be able to switch back to using basic permissions management.</span></span>

## <a name="related-topics"></a><span data-ttu-id="baa54-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baa54-124">Related topics</span></span>

- [<span data-ttu-id="baa54-125">Utiliser les autorisations de base pour accéder au portail</span><span class="sxs-lookup"><span data-stu-id="baa54-125">Use basic permissions to access the portal</span></span>](basic-permissions.md)
- [<span data-ttu-id="baa54-126">Gérer l’accès au portail à l’aide de RBAC</span><span class="sxs-lookup"><span data-stu-id="baa54-126">Manage portal access using RBAC</span></span>](rbac.md)
