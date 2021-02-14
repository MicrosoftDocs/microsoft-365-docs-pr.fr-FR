---
title: Attribuer des licences Microsoft 365 à des comptes d’utilisateur
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
description: Décrit comment attribuer des licences Microsoft 365 à des comptes d’utilisateur, individuellement ou en fonction de l’appartenance à un groupe.
ms.openlocfilehash: a2eed7b3597dcc2531834456a9b05f5aa1b07a23
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48326506"
---
# <a name="assign-microsoft-365-licenses-to-user-accounts"></a><span data-ttu-id="7a650-103">Attribuer des licences Microsoft 365 à des comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7a650-103">Assign Microsoft 365 licenses to user accounts</span></span>

<span data-ttu-id="7a650-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="7a650-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="7a650-105">Pour le modèle d’identité cloud uniquement, vous pouvez attribuer des licences Microsoft 365 aux comptes d’utilisateur lors de leur création, en fonction de la façon dont vous les créez.</span><span class="sxs-lookup"><span data-stu-id="7a650-105">For the cloud-only identity model, you can assign Microsoft 365 licenses to user accounts as they are created, depending on how you create them.</span></span>

<span data-ttu-id="7a650-106">Pour le modèle d’identité hybride, lorsque les comptes d’utilisateur des services de domaine Active Directory (AD DS) sont synchronisés pour la première fois, ils ne se voit pas attribuer automatiquement un emplacement ou une licence Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7a650-106">For the hybrid identity model, when Active Directory Domain Services (AD DS) user accounts are synchronized for the first time, they are not automatically assigned a location or a Microsoft 365 license.</span></span> <span data-ttu-id="7a650-107">**Vous devez configurer chaque compte d’utilisateur avec un emplacement d’utilisateur avant ou avec l’attribution d’une licence.**</span><span class="sxs-lookup"><span data-stu-id="7a650-107">**You must configure each user account with a user location prior to or along with assigning a license.**</span></span>

<span data-ttu-id="7a650-108">Dans les deux cas, vous devez attribuer une licence aux comptes d’utilisateurs afin que vos utilisateurs peuvent accéder aux services Microsoft 365, tels que le courrier électronique et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7a650-108">In either case, you must assign a license to user accounts so your users can access Microsoft 365 services, such as email and Microsoft Teams.</span></span>

<span data-ttu-id="7a650-109">Vous pouvez attribuer des licences aux comptes d’utilisateurs individuellement ou automatiquement par le biais de l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="7a650-109">You can assign licenses to user accounts either individually or automatically through group membership.</span></span>

<span data-ttu-id="7a650-110">Pour attribuer des licences Microsoft 365 à des comptes d’utilisateur individuels, vous pouvez utiliser :</span><span class="sxs-lookup"><span data-stu-id="7a650-110">To assign Microsoft 365 licenses to individual user accounts, you can use:</span></span>

- [<span data-ttu-id="7a650-111">Le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7a650-111">The Microsoft 365 admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/assign-licenses-to-users)
- [<span data-ttu-id="7a650-112">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7a650-112">PowerShell</span></span>](assign-licenses-to-user-accounts-with-microsoft-365-powershell.md)
- <span data-ttu-id="7a650-113">Centre d’administration Azure AD</span><span class="sxs-lookup"><span data-stu-id="7a650-113">The Azure AD admin center</span></span>

## <a name="group-based-licensing"></a><span data-ttu-id="7a650-114">Gestion des licences en fonction des groupes</span><span class="sxs-lookup"><span data-stu-id="7a650-114">Group-based licensing</span></span>

<span data-ttu-id="7a650-115">Vous pouvez configurer des groupes de sécurité dans Azure AD pour attribuer automatiquement des licences d’un ensemble d’abonnements à tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="7a650-115">You can configure security groups in Azure AD to automatically assign licenses from a set of subscriptions to all the members of the group.</span></span> <span data-ttu-id="7a650-116">C’est ce que l’on appelle la *gestion des licences basée sur les groupes*.</span><span class="sxs-lookup"><span data-stu-id="7a650-116">This is known as *group-based licensing*.</span></span> <span data-ttu-id="7a650-117">Si un compte d’utilisateur est ajouté au groupe ou supprimé de ce dernier, les licences des abonnements du groupe sont automatiquement attribuées au compte d’utilisateur ou supprimées du compte.</span><span class="sxs-lookup"><span data-stu-id="7a650-117">If a user account is added to or removed from the group, the licenses for the group's subscriptions will be automatically assigned or unassigned from the user account.</span></span>

<span data-ttu-id="7a650-118">Vérifiez que vous disposez de suffisamment de licences pour tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="7a650-118">Make sure you have enough licenses for all the group members.</span></span> <span data-ttu-id="7a650-119">Si vous n’avez plus de licences, aucune licence ne sera attribuée aux nouveaux utilisateurs tant que d’autres licences ne seront pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="7a650-119">If you run out of licenses, new users won't be assigned licenses until licenses become available.</span></span>

>[!Note]
><span data-ttu-id="7a650-120">Vous ne devez pas configurer la gestion des licences par groupes pour des groupes qui contiennent des comptes B2B Azure.</span><span class="sxs-lookup"><span data-stu-id="7a650-120">You should not configure group-based licensing for groups that contain Azure business to business (B2B) accounts.</span></span>
>

<span data-ttu-id="7a650-121">Pour plus d’informations, voir la gestion des licences basée [sur les groupes dans Azure AD.](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal)</span><span class="sxs-lookup"><span data-stu-id="7a650-121">For more informaion, see [group-based licensing in Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal).</span></span>

## <a name="next-steps"></a><span data-ttu-id="7a650-122">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="7a650-122">Next steps</span></span>

<span data-ttu-id="7a650-123">Avec l’ensemble approprié de comptes d’utilisateurs qui ont reçu des licences, vous êtes maintenant prêt à :</span><span class="sxs-lookup"><span data-stu-id="7a650-123">With the appropriate set of user accounts that have been assigned licenses, you are now ready to:</span></span>

- [<span data-ttu-id="7a650-124">Implémenter la sécurité</span><span class="sxs-lookup"><span data-stu-id="7a650-124">Implement security</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/security-roadmap)
- [<span data-ttu-id="7a650-125">Déployer des logiciels clients, tels que Microsoft 365 Apps</span><span class="sxs-lookup"><span data-stu-id="7a650-125">Deploy client software, such as Microsoft 365 Apps</span></span>](https://docs.microsoft.com/DeployOffice/deployment-guide-microsoft-365-apps)
- [<span data-ttu-id="7a650-126">Configurer la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="7a650-126">Set up device management</span></span>](device-management-roadmap-microsoft-365.md)
- [<span data-ttu-id="7a650-127">Configurer les services et les applications</span><span class="sxs-lookup"><span data-stu-id="7a650-127">Configure services and applications</span></span>](configure-services-and-applications.md)
