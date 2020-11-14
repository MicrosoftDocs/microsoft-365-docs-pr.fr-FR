---
title: Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/13/2020
audience: ITPro
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- PowerShell
- Ent_Office_Other
- seo-marvel-apr2020
ms.assetid: 26b9ff81-93b0-4251-beaf-3c9f1d7c80c8
description: Découvrez comment gérer les comptes d’utilisateur, les licences et les groupes Microsoft 365 avec PowerShell.
ms.openlocfilehash: ec60fcfe3c3d2c0e26cb2cca6a56741067d154c0
ms.sourcegitcommit: fcc1b40732f28f075d95faffc1655473e262dd95
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2020
ms.locfileid: "49073124"
---
# <a name="manage-microsoft-365-user-accounts-licenses-and-groups-with-powershell"></a><span data-ttu-id="4124a-103">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="4124a-103">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>

<span data-ttu-id="4124a-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="4124a-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="4124a-105">Les administrateurs de Microsoft 365 doivent gérer les comptes d’utilisateur, les licences et les groupes.</span><span class="sxs-lookup"><span data-stu-id="4124a-105">Microsoft 365 administrators need to manage user accounts, licenses, and groups.</span></span> <span data-ttu-id="4124a-106">Bien que vous puissiez effectuer la plupart de ces tâches dans le centre d’administration 365 de Microsoft, certains sont plus faciles à utiliser dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4124a-106">Although you can do most of these tasks in the Microsoft 365 admin center, some are easier in PowerShell.</span></span>

<span data-ttu-id="4124a-107">Pour plus d'informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="4124a-107">For more information, see the following articles.</span></span>

## <a name="user-accounts"></a><span data-ttu-id="4124a-108">Comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4124a-108">User accounts</span></span>

- [<span data-ttu-id="4124a-109">Création de comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4124a-109">Create user accounts</span></span>](create-user-accounts-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-110">Affichage de comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4124a-110">View user accounts</span></span>](view-user-accounts-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-111">Configuration des propriétés de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4124a-111">Configure user account properties</span></span>](configure-user-account-properties-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-112">Attribution de rôles aux comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4124a-112">Assign roles to user accounts</span></span>](assign-roles-to-user-accounts-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-113">Suppression et restauration de comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4124a-113">Delete and restore user accounts</span></span>](delete-and-restore-user-accounts-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-114">Blocage de comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4124a-114">Block user accounts</span></span>](block-user-accounts-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-115">Mots de passe</span><span class="sxs-lookup"><span data-stu-id="4124a-115">Passwords</span></span>](manage-passwords-with-microsoft-365-powershell.md)

## <a name="licenses-and-services"></a><span data-ttu-id="4124a-116">Licences et services</span><span class="sxs-lookup"><span data-stu-id="4124a-116">Licenses and services</span></span>
- [<span data-ttu-id="4124a-117">Affichage des licences et des services</span><span class="sxs-lookup"><span data-stu-id="4124a-117">View licenses and services</span></span>](view-licenses-and-services-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-118">Affichage des utilisateurs sous licence et sans licence</span><span class="sxs-lookup"><span data-stu-id="4124a-118">View licensed and unlicensed users</span></span>](view-licensed-and-unlicensed-users-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-119">Attribution de licences aux comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4124a-119">Assign licenses to user accounts</span></span>](assign-licenses-to-user-accounts-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-120">Affichage des détails de service et de licence de compte</span><span class="sxs-lookup"><span data-stu-id="4124a-120">View account license and service details</span></span>](view-account-license-and-service-details-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-121">Désactivation de l’accès aux services</span><span class="sxs-lookup"><span data-stu-id="4124a-121">Disable access to services</span></span>](disable-access-to-services-with-microsoft-365-powershell.md)
  - [<span data-ttu-id="4124a-122">Désactivation de l’accès à Sway</span><span class="sxs-lookup"><span data-stu-id="4124a-122">Disable access to Sway</span></span>](disable-access-to-sway-with-microsoft-365-powershell.md)
  - [<span data-ttu-id="4124a-123">Désactivation de l’accès aux services lors de l’attribution des licences utilisateur</span><span class="sxs-lookup"><span data-stu-id="4124a-123">Disable access to services while assigning user licenses</span></span>](disable-access-to-services-while-assigning-user-licenses.md)
- [<span data-ttu-id="4124a-124">Suppression de licences à des comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4124a-124">Remove licenses from user accounts</span></span>](remove-licenses-from-user-accounts-with-microsoft-365-powershell.md)

## <a name="groups"></a><span data-ttu-id="4124a-125">Groupes</span><span class="sxs-lookup"><span data-stu-id="4124a-125">Groups</span></span>
- [<span data-ttu-id="4124a-126">Maintenir l’appartenance à un groupe</span><span class="sxs-lookup"><span data-stu-id="4124a-126">Maintain group membership</span></span>](maintain-group-membership-with-microsoft-365-powershell.md)
- [<span data-ttu-id="4124a-127">Gestion des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4124a-127">Manage Microsoft 365 groups</span></span>](manage-microsoft-365-groups-with-powershell.md)
