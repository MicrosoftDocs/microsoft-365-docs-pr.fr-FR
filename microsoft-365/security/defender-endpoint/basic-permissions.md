---
title: Utiliser les autorisations de base pour accéder au Centre de sécurité Microsoft Defender
description: Découvrez comment utiliser les autorisations de base pour accéder au portail Microsoft Defender for Endpoint.
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
ms.technology: mde
ms.openlocfilehash: cb5762d2a9e4b62432aba6dacd1033ddc3c7daf2
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51163670"
---
# <a name="use-basic-permissions-to-access-the-portal"></a><span data-ttu-id="f9cf9-104">Utiliser les autorisations de base pour accéder au portail</span><span class="sxs-lookup"><span data-stu-id="f9cf9-104">Use basic permissions to access the portal</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f9cf9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f9cf9-105">**Applies to:**</span></span>
- <span data-ttu-id="f9cf9-106">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f9cf9-106">Azure Active Directory</span></span>
- [<span data-ttu-id="f9cf9-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f9cf9-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="f9cf9-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f9cf9-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="f9cf9-109">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="f9cf9-109">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="f9cf9-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-basicaccess-abovefoldlink)

<span data-ttu-id="f9cf9-111">Reportez-vous aux instructions ci-dessous pour utiliser la gestion des autorisations de base.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-111">Refer to the instructions below to use basic permissions management.</span></span>

<span data-ttu-id="f9cf9-112">Vous pouvez utiliser l’une des solutions suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9cf9-112">You can use either of the following solutions:</span></span>
- <span data-ttu-id="f9cf9-113">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9cf9-113">Azure PowerShell</span></span>
- <span data-ttu-id="f9cf9-114">Portail Azure</span><span class="sxs-lookup"><span data-stu-id="f9cf9-114">Azure portal</span></span>

<span data-ttu-id="f9cf9-115">Pour un contrôle granulaire des autorisations, [basculez vers le contrôle d’accès basé sur les rôles.](rbac.md)</span><span class="sxs-lookup"><span data-stu-id="f9cf9-115">For granular control over permissions, [switch to role-based access control](rbac.md).</span></span>

## <a name="assign-user-access-using-azure-powershell"></a><span data-ttu-id="f9cf9-116">Attribuer un accès utilisateur à l’aide d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9cf9-116">Assign user access using Azure PowerShell</span></span>
<span data-ttu-id="f9cf9-117">Vous pouvez affecter des utilisateurs avec l’un des niveaux d’autorisation suivants :</span><span class="sxs-lookup"><span data-stu-id="f9cf9-117">You can assign users with one of the following levels of permissions:</span></span>
- <span data-ttu-id="f9cf9-118">Accès total (lecture et écriture)</span><span class="sxs-lookup"><span data-stu-id="f9cf9-118">Full access (Read and Write)</span></span>
- <span data-ttu-id="f9cf9-119">Accès en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f9cf9-119">Read-only access</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="f9cf9-120">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f9cf9-120">Before you begin</span></span>

- <span data-ttu-id="f9cf9-121">Installez Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-121">Install Azure PowerShell.</span></span> <span data-ttu-id="f9cf9-122">Pour plus d’informations, voir [comment installer et configurer Azure PowerShell.](https://azure.microsoft.com/documentation/articles/powershell-install-configure/)</span><span class="sxs-lookup"><span data-stu-id="f9cf9-122">For more information, see, [How to install and configure Azure PowerShell](https://azure.microsoft.com/documentation/articles/powershell-install-configure/).</span></span><br>

    > [!NOTE]
    > <span data-ttu-id="f9cf9-123">Vous devez exécuter les cmdlets PowerShell dans une ligne de commande avec élévation de élévation de niveaux.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-123">You need to run the PowerShell cmdlets in an elevated command-line.</span></span>

- <span data-ttu-id="f9cf9-124">Connectez-vous à azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-124">Connect to your Azure Active Directory.</span></span> <span data-ttu-id="f9cf9-125">Pour plus d’informations, [voir Connect-MsolService.](https://docs.microsoft.com/powershell/module/msonline/connect-msolservice?view=azureadps-1.0&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="f9cf9-125">For more information, see [Connect-MsolService](https://docs.microsoft.com/powershell/module/msonline/connect-msolservice?view=azureadps-1.0&preserve-view=true).</span></span>

<span data-ttu-id="f9cf9-126">**Accès total**</span><span class="sxs-lookup"><span data-stu-id="f9cf9-126">**Full access**</span></span> <br>
<span data-ttu-id="f9cf9-127">Les utilisateurs ayant un accès total peuvent se connecter, afficher toutes les informations système et résoudre les alertes, soumettre des fichiers pour une analyse approfondie et télécharger le package d’intégration.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-127">Users with full access can log in, view all system information and resolve alerts, submit files for deep analysis, and download the onboarding package.</span></span>
<span data-ttu-id="f9cf9-128">L’attribution de droits d’accès total nécessite l’ajout des utilisateurs aux rôles intégrés AAD « Administrateur de la sécurité » ou « Administrateur général ».</span><span class="sxs-lookup"><span data-stu-id="f9cf9-128">Assigning full access rights requires adding the users to the "Security Administrator" or "Global Administrator" AAD built-in roles.</span></span>

<span data-ttu-id="f9cf9-129">**Accès en lecture seule**</span><span class="sxs-lookup"><span data-stu-id="f9cf9-129">**Read-only access**</span></span> <br>
<span data-ttu-id="f9cf9-130">Les utilisateurs ayant un accès en lecture seule peuvent se connecter, afficher toutes les alertes et les informations connexes.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-130">Users with read-only access can log in, view all alerts, and related information.</span></span>
<span data-ttu-id="f9cf9-131">Ils ne pourront pas modifier les états d’alerte, soumettre des fichiers pour analyse approfondie ou effectuer des opérations de changement d’état.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-131">They will not be able to change alert states, submit files for deep analysis or perform any state changing operations.</span></span>
<span data-ttu-id="f9cf9-132">L’attribution de droits d’accès en lecture seule nécessite l’ajout des utilisateurs au rôle intégré Azure AD « Lecteur de sécurité ».</span><span class="sxs-lookup"><span data-stu-id="f9cf9-132">Assigning read-only access rights requires adding the users to the "Security Reader" Azure AD built-in role.</span></span>

<span data-ttu-id="f9cf9-133">Pour attribuer des rôles de sécurité, utilisez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9cf9-133">Use the following steps to assign security roles:</span></span>

- <span data-ttu-id="f9cf9-134">Pour **accéder en lecture et en** écriture, attribuez aux utilisateurs le rôle d’administrateur de sécurité à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="f9cf9-134">For **read and write** access, assign users to the security administrator role by using the following command:</span></span>

  ```PowerShell
  Add-MsolRoleMember -RoleName "Security Administrator" -RoleMemberEmailAddress "secadmin@Contoso.onmicrosoft.com"
  ```
  
- <span data-ttu-id="f9cf9-135">Pour **un accès en lecture seule,** attribuez aux utilisateurs le rôle de lecteur de sécurité à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="f9cf9-135">For **read-only** access, assign users to the security reader role by using the following command:</span></span>

  ```PowerShell
  Add-MsolRoleMember -RoleName "Security Reader" -RoleMemberEmailAddress "reader@Contoso.onmicrosoft.com"
  ```

<span data-ttu-id="f9cf9-136">Pour plus d’informations, voir [Ajouter ou supprimer des membres du groupe à l’aide d’Azure Active Directory.](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-members-azure-portal)</span><span class="sxs-lookup"><span data-stu-id="f9cf9-136">For more information, see [Add or remove group members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-members-azure-portal).</span></span>

## <a name="assign-user-access-using-the-azure-portal"></a><span data-ttu-id="f9cf9-137">Attribuer un accès utilisateur à l’aide du portail Azure</span><span class="sxs-lookup"><span data-stu-id="f9cf9-137">Assign user access using the Azure portal</span></span>

<span data-ttu-id="f9cf9-138">Pour plus d’informations, voir Attribuer des rôles d’administrateur et de non-administrateur aux utilisateurs [avec Azure Active Directory.](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal)</span><span class="sxs-lookup"><span data-stu-id="f9cf9-138">For more information, see [Assign administrator and non-administrator roles to users with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal).</span></span>

## <a name="related-topic"></a><span data-ttu-id="f9cf9-139">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="f9cf9-139">Related topic</span></span>

- [<span data-ttu-id="f9cf9-140">Gérer l’accès au portail à l’aide de RBAC</span><span class="sxs-lookup"><span data-stu-id="f9cf9-140">Manage portal access using RBAC</span></span>](rbac.md)
