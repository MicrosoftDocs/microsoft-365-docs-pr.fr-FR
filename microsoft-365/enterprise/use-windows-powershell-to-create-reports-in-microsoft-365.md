---
title: Utilisation de PowerShell pour créer des rapports pour Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/17/2020
audience: ITPro
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- Ent_Office_Other
- seo-marvel-apr2020
ms.assetid: 1ea4d4ec-af89-496f-9678-701867f5a6fc
description: "Résumé: Utilisez PowerShell pour Microsoft 365 créer des rapports que vous ne pouvez pas produire dans le centre d’administration Microsoft 365'administration."
ms.openlocfilehash: 9e3b90dcdd32f80125175ad2e15a852db51e17f8
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572740"
---
# <a name="use-powershell-to-create-reports-for-microsoft-365"></a><span data-ttu-id="ef220-103">Utilisation de PowerShell pour créer des rapports pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ef220-103">Use PowerShell to create reports for Microsoft 365</span></span>

<span data-ttu-id="ef220-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="ef220-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="ef220-105">De nombreux rapports différents sont disponibles dans le centre Microsoft 365'administration.</span><span class="sxs-lookup"><span data-stu-id="ef220-105">Many different reports are available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="ef220-106">Mais ces rapports ne fournissent que beaucoup d’informations, et parfois vous avez besoin de plus.</span><span class="sxs-lookup"><span data-stu-id="ef220-106">But these reports only provide so much information, and sometimes you need more.</span></span> <span data-ttu-id="ef220-107">C’est alors que vous avez besoin de PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ef220-107">That's when you need PowerShell for Microsoft 365.</span></span>
  
<span data-ttu-id="ef220-108">Ces articles décrivent comment utiliser PowerShell pour Microsoft 365 obtenir des informations auprès de votre Microsoft 365 locataire :</span><span class="sxs-lookup"><span data-stu-id="ef220-108">These articles describe how to use PowerShell for Microsoft 365 to get information from your Microsoft 365 tenant:</span></span>
  
- <span data-ttu-id="ef220-109">Commencer par les rapports à l’aide de PowerShell pour Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="ef220-109">Get started with reporting using PowerShell for Microsoft 365:</span></span>
    
  - [<span data-ttu-id="ef220-110">Pourquoi utiliser PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ef220-110">Why you need to use PowerShell for Microsoft 365</span></span>](./why-you-need-to-use-microsoft-365-powershell.md)
    
    
- <span data-ttu-id="ef220-111">Rapports pour les comptes d’utilisateurs et les licences :</span><span class="sxs-lookup"><span data-stu-id="ef220-111">Reports for user accounts and licenses:</span></span>
    
  - [<span data-ttu-id="ef220-112">Voir Microsoft 365 licences et services avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef220-112">View Microsoft 365 licenses and services with PowerShell</span></span>](view-licenses-and-services-with-microsoft-365-powershell.md)
    
  - [<span data-ttu-id="ef220-113">Voir Microsoft 365 utilisateurs sous licence et sans licence avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef220-113">View Microsoft 365 licensed and unlicensed users with PowerShell</span></span>](view-licensed-and-unlicensed-users-with-microsoft-365-powershell.md)
    
  - [<span data-ttu-id="ef220-114">Voir les Microsoft 365 de licence de compte et de service avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef220-114">View Microsoft 365 account license and service details with PowerShell</span></span>](view-account-license-and-service-details-with-microsoft-365-powershell.md)
    
  - [<span data-ttu-id="ef220-115">Afficher Microsoft 365 comptes d’utilisateurs avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef220-115">View Microsoft 365 user accounts with PowerShell</span></span>](view-user-accounts-with-microsoft-365-powershell.md)
    
- <span data-ttu-id="ef220-116">Rapports pour SharePoint Online :</span><span class="sxs-lookup"><span data-stu-id="ef220-116">Reports for SharePoint Online:</span></span>
    
  - [<span data-ttu-id="ef220-117">Prise en main de SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="ef220-117">Get started with SharePoint Online Management Shell</span></span>](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
    
  - [<span data-ttu-id="ef220-118">Get-SPOSiteGroup - Obtient tous les groupes sur une collection de site spécifiée</span><span class="sxs-lookup"><span data-stu-id="ef220-118">Get-SPOSiteGroup - Gets all the groups on a specified site collection</span></span>](/powershell/module/sharepoint-online/get-spositegroup)
    
- <span data-ttu-id="ef220-119">Rapports pour Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="ef220-119">Reports for Exchange Online:</span></span>
    
  - [<span data-ttu-id="ef220-120">Utilisez Exchange Online PowerShell pour afficher la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ef220-120">Use Exchange Online PowerShell to display mailbox</span></span>](/exchange/recipients-in-exchange-online/manage-user-mailboxes/use-powershell-to-display-mailbox-information)
    
    
## <a name="related-articles"></a><span data-ttu-id="ef220-121">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="ef220-121">Related articles</span></span>

[<span data-ttu-id="ef220-122">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef220-122">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="ef220-123">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ef220-123">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="ef220-124">Gérez SharePoint avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef220-124">Manage SharePoint with PowerShell</span></span>](manage-sharepoint-online-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="ef220-125">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef220-125">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
