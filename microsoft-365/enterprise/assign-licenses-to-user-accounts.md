---
title: Attribuer des licences Microsoft 365 à des comptes d’utilisateur
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/03/2019
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
description: Indique comment attribuer des licences Microsoft 365 à des comptes d’utilisateur, individuellement ou en fonction de l’appartenance au groupe.
ms.openlocfilehash: e132a8c2d65c401899624b9d255050385f2cb721
ms.sourcegitcommit: 74ef7179887eedc696c975a82c865b2d4b3808fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "47417097"
---
# <a name="assign-microsoft-365-licenses-to-user-accounts"></a><span data-ttu-id="7fc9e-103">Attribuer des licences Microsoft 365 à des comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7fc9e-103">Assign Microsoft 365 licenses to user accounts</span></span>

<span data-ttu-id="7fc9e-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="7fc9e-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="7fc9e-105">Pour le modèle d’identité Cloud uniquement, vous pouvez attribuer des licences Microsoft 365 à des comptes d’utilisateur au fur et à mesure de leur création, en fonction de leur création.</span><span class="sxs-lookup"><span data-stu-id="7fc9e-105">For the cloud-only identity model, you can assign Microsoft 365 licenses to user accounts as they are created, depending on how you create them.</span></span>

<span data-ttu-id="7fc9e-106">Pour le modèle d’identité hybride, lorsque les comptes d’utilisateur des services de domaine Active Directory (AD DS) sont synchronisés pour la première fois, une licence Microsoft 365 n’est pas automatiquement attribuée à ces comptes.</span><span class="sxs-lookup"><span data-stu-id="7fc9e-106">For the hybrid identity model, when Active Directory Domain Services (AD DS) user accounts are synchronized for the first time, they are not automatically assigned a Microsoft 365 license.</span></span> <span data-ttu-id="7fc9e-107">Vous devez d’abord configurer chaque compte d’utilisateur avec un emplacement utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7fc9e-107">You must first configure each user account with a user location.</span></span>

<span data-ttu-id="7fc9e-108">Dans les deux cas, vous devez attribuer une licence à des comptes d’utilisateurs pour permettre à vos utilisateurs d’accéder aux services Microsoft 365, tels que le courrier électronique et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7fc9e-108">In either case, you must assign a license to user accounts so your users can access Microsoft 365 services, such as email and Microsoft Teams.</span></span>

<span data-ttu-id="7fc9e-109">Vous pouvez attribuer des licences à des comptes d’utilisateur de manière individuelle ou automatique via l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="7fc9e-109">You can assign licenses to user accounts either individually or automatically through group membership.</span></span>

<span data-ttu-id="7fc9e-110">Pour attribuer des licences Microsoft 365 à des comptes d’utilisateur individuels, vous pouvez utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7fc9e-110">To assign Microsoft 365 licenses to individual user accounts, you can use:</span></span>

- [<span data-ttu-id="7fc9e-111">Le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7fc9e-111">The Microsoft 365 admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/assign-licenses-to-users)
- [<span data-ttu-id="7fc9e-112">PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7fc9e-112">PowerShell for Microsoft 365</span></span>](assign-licenses-to-user-accounts-with-microsoft-365-powershell.md)

<span data-ttu-id="7fc9e-113">Pour l’attribution automatique de licence, consultez la rubrique [Group-based Licensing in Azure ad](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="7fc9e-113">For automatic license assignment, see [group-based licensing in Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal).</span></span>

## <a name="next-steps"></a><span data-ttu-id="7fc9e-114">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="7fc9e-114">Next steps</span></span>

<span data-ttu-id="7fc9e-115">À l’aide de l’ensemble complet des comptes d’utilisateur auxquels des licences ont été attribuées, vous êtes maintenant prêt à :</span><span class="sxs-lookup"><span data-stu-id="7fc9e-115">With the full set of user accounts that have been assigned licenses, you are now ready to:</span></span>

- [<span data-ttu-id="7fc9e-116">Implémenter la sécurité</span><span class="sxs-lookup"><span data-stu-id="7fc9e-116">Implement security</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/security-roadmap)
- [<span data-ttu-id="7fc9e-117">Déployer le logiciel client, tel que les applications Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7fc9e-117">Deploy client software, such as Microsoft 365 Apps</span></span>](https://docs.microsoft.com/DeployOffice/deployment-guide-microsoft-365-apps)
- [<span data-ttu-id="7fc9e-118">Configuration de la mobilité et de la sécurité de base dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7fc9e-118">Set up Basic Mobility and Security in Microsoft 365</span></span>](https://support.microsoft.com/office/set-up-basic-mobility-and-security-dd892318-bc44-4eb1-af00-9db5430be3cd)
- [<span data-ttu-id="7fc9e-119">Configurer les services et les applications</span><span class="sxs-lookup"><span data-stu-id="7fc9e-119">Configure services and applications</span></span>](configure-services-and-applications.md)
