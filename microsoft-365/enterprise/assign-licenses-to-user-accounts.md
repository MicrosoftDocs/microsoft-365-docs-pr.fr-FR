---
title: Attribuer Microsoft 365 licences d’accès aux comptes d’utilisateurs
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
description: Décrit comment attribuer des licences Microsoft 365 aux comptes d’utilisateurs, individuellement ou en fonction de l’appartenance à un groupe.
ms.openlocfilehash: 2fe1e2f959fae8b0bc82a7dcd4f65f33b21c368a
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51051531"
---
# <a name="assign-microsoft-365-licenses-to-user-accounts"></a><span data-ttu-id="96a92-103">Attribuer Microsoft 365 licences d’accès aux comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="96a92-103">Assign Microsoft 365 licenses to user accounts</span></span>

<span data-ttu-id="96a92-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="96a92-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="96a92-105">Pour le modèle d’identité cloud uniquement, vous pouvez attribuer des licences Microsoft 365 aux comptes d’utilisateur lors de leur création, en fonction de la façon dont vous les créez.</span><span class="sxs-lookup"><span data-stu-id="96a92-105">For the cloud-only identity model, you can assign Microsoft 365 licenses to user accounts as they are created, depending on how you create them.</span></span>

<span data-ttu-id="96a92-106">Pour le modèle d’identité hybride, lorsque les comptes d’utilisateur des services de domaine Active Directory (AD DS) sont synchronisés pour la première fois, ils ne se voit pas attribuer automatiquement un emplacement ou une licence Microsoft 365..</span><span class="sxs-lookup"><span data-stu-id="96a92-106">For the hybrid identity model, when Active Directory Domain Services (AD DS) user accounts are synchronized for the first time, they are not automatically assigned a location or a Microsoft 365 license.</span></span> <span data-ttu-id="96a92-107">**Vous devez configurer chaque compte d’utilisateur avec un emplacement d’utilisateur avant ou avec l’attribution d’une licence.**</span><span class="sxs-lookup"><span data-stu-id="96a92-107">**You must configure each user account with a user location prior to or along with assigning a license.**</span></span>

<span data-ttu-id="96a92-108">Dans les deux cas, vous devez attribuer une licence à des comptes d’utilisateurs afin que vos utilisateurs peuvent accéder aux services Microsoft 365, tels que la messagerie et les Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="96a92-108">In either case, you must assign a license to user accounts so your users can access Microsoft 365 services, such as email and Microsoft Teams.</span></span>

<span data-ttu-id="96a92-109">Vous pouvez attribuer des licences aux comptes d’utilisateurs individuellement ou automatiquement par le biais de l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="96a92-109">You can assign licenses to user accounts either individually or automatically through group membership.</span></span>

<span data-ttu-id="96a92-110">Pour attribuer Microsoft 365 licences à des comptes d’utilisateurs individuels, vous pouvez utiliser :</span><span class="sxs-lookup"><span data-stu-id="96a92-110">To assign Microsoft 365 licenses to individual user accounts, you can use:</span></span>

- [<span data-ttu-id="96a92-111">Le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="96a92-111">The Microsoft 365 admin center</span></span>](../admin/manage/assign-licenses-to-users.md)
- [<span data-ttu-id="96a92-112">PowerShell</span><span class="sxs-lookup"><span data-stu-id="96a92-112">PowerShell</span></span>](assign-licenses-to-user-accounts-with-microsoft-365-powershell.md)
- <span data-ttu-id="96a92-113">Centre d’administration Azure AD</span><span class="sxs-lookup"><span data-stu-id="96a92-113">The Azure AD admin center</span></span>

## <a name="group-based-licensing"></a><span data-ttu-id="96a92-114">Gestion des licences en fonction des groupes</span><span class="sxs-lookup"><span data-stu-id="96a92-114">Group-based licensing</span></span>

<span data-ttu-id="96a92-115">Vous pouvez configurer des groupes de sécurité dans Azure AD pour attribuer automatiquement des licences d’un ensemble d’abonnements à tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="96a92-115">You can configure security groups in Azure AD to automatically assign licenses from a set of subscriptions to all the members of the group.</span></span> <span data-ttu-id="96a92-116">C’est ce que l’on appelle la *gestion des licences basée sur les groupes*.</span><span class="sxs-lookup"><span data-stu-id="96a92-116">This is known as *group-based licensing*.</span></span> <span data-ttu-id="96a92-117">Si un compte d’utilisateur est ajouté au groupe ou supprimé de ce dernier, les licences des abonnements du groupe sont automatiquement attribuées au compte d’utilisateur ou supprimées du compte.</span><span class="sxs-lookup"><span data-stu-id="96a92-117">If a user account is added to or removed from the group, the licenses for the group's subscriptions will be automatically assigned or unassigned from the user account.</span></span>

<span data-ttu-id="96a92-118">Vérifiez que vous disposez de suffisamment de licences pour tous les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="96a92-118">Make sure you have enough licenses for all the group members.</span></span> <span data-ttu-id="96a92-119">Si vous n’avez plus de licences, aucune licence ne sera attribuée aux nouveaux utilisateurs tant que d’autres licences ne seront pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="96a92-119">If you run out of licenses, new users won't be assigned licenses until licenses become available.</span></span>

>[!Note]
><span data-ttu-id="96a92-120">Vous ne devez pas configurer la gestion des licences par groupes pour des groupes qui contiennent des comptes B2B Azure.</span><span class="sxs-lookup"><span data-stu-id="96a92-120">You should not configure group-based licensing for groups that contain Azure business to business (B2B) accounts.</span></span>
>

<span data-ttu-id="96a92-121">Pour plus d’informations, voir la gestion des licences basée [sur les groupes dans Azure AD.](/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal)</span><span class="sxs-lookup"><span data-stu-id="96a92-121">For more informaion, see [group-based licensing in Azure AD](/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal).</span></span>

## <a name="next-steps"></a><span data-ttu-id="96a92-122">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="96a92-122">Next steps</span></span>

<span data-ttu-id="96a92-123">Avec l’ensemble approprié de comptes d’utilisateurs qui ont reçu des licences, vous êtes maintenant prêt à :</span><span class="sxs-lookup"><span data-stu-id="96a92-123">With the appropriate set of user accounts that have been assigned licenses, you are now ready to:</span></span>

- [<span data-ttu-id="96a92-124">Implémenter la sécurité</span><span class="sxs-lookup"><span data-stu-id="96a92-124">Implement security</span></span>](../security/defender-365-security/security-roadmap.md)
- [<span data-ttu-id="96a92-125">Déployer des logiciels clients, tels que Microsoft 365 Apps</span><span class="sxs-lookup"><span data-stu-id="96a92-125">Deploy client software, such as Microsoft 365 Apps</span></span>](/DeployOffice/deployment-guide-microsoft-365-apps)
- [<span data-ttu-id="96a92-126">Configurer la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="96a92-126">Set up device management</span></span>](device-management-roadmap-microsoft-365.md)
- [<span data-ttu-id="96a92-127">Configurer les services et les applications</span><span class="sxs-lookup"><span data-stu-id="96a92-127">Configure services and applications</span></span>](configure-services-and-applications.md)