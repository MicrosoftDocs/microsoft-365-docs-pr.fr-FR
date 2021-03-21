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
description: 'Résumé : Utilisez PowerShell pour Microsoft 365 pour créer des rapports que vous ne pouvez pas produire dans le Centre d’administration Microsoft 365.'
ms.openlocfilehash: 12cba74d114ea03804741335bd34ece403926033
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50924695"
---
# <a name="use-powershell-to-create-reports-for-microsoft-365"></a><span data-ttu-id="0cfda-103">Utilisation de PowerShell pour créer des rapports pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0cfda-103">Use PowerShell to create reports for Microsoft 365</span></span>

<span data-ttu-id="0cfda-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="0cfda-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="0cfda-105">De nombreux rapports différents sont disponibles dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0cfda-105">Many different reports are available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="0cfda-106">Toutefois, ces rapports fournissent uniquement une telle quantité d’informations, et vous en avez parfois besoin de plus.</span><span class="sxs-lookup"><span data-stu-id="0cfda-106">But these reports only provide so much information, and sometimes you need more.</span></span> <span data-ttu-id="0cfda-107">C’est à ce moment que vous avez besoin de PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0cfda-107">That's when you need PowerShell for Microsoft 365.</span></span>
  
<span data-ttu-id="0cfda-108">Ces articles décrivent comment utiliser PowerShell pour Microsoft 365 afin d’obtenir des informations auprès de votre client Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="0cfda-108">These articles describe how to use PowerShell for Microsoft 365 to get information from your Microsoft 365 tenant:</span></span>
  
- <span data-ttu-id="0cfda-109">Commencer à faire des rapports à l’aide de PowerShell pour Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="0cfda-109">Get started with reporting using PowerShell for Microsoft 365:</span></span>
    
  - [<span data-ttu-id="0cfda-110">Pourquoi utiliser PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0cfda-110">Why you need to use PowerShell for Microsoft 365</span></span>](./why-you-need-to-use-microsoft-365-powershell.md#reveal)
    
    
- <span data-ttu-id="0cfda-111">Rapports pour les comptes d’utilisateurs et les licences :</span><span class="sxs-lookup"><span data-stu-id="0cfda-111">Reports for user accounts and licenses:</span></span>
    
  - [<span data-ttu-id="0cfda-112">Afficher les licences et services Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cfda-112">View Microsoft 365 licenses and services with PowerShell</span></span>](view-licenses-and-services-with-microsoft-365-powershell.md)
    
  - [<span data-ttu-id="0cfda-113">Afficher les utilisateurs sous licence et sans licence Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cfda-113">View Microsoft 365 licensed and unlicensed users with PowerShell</span></span>](view-licensed-and-unlicensed-users-with-microsoft-365-powershell.md)
    
  - [<span data-ttu-id="0cfda-114">Afficher les détails de service et de licence de compte Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cfda-114">View Microsoft 365 account license and service details with PowerShell</span></span>](view-account-license-and-service-details-with-microsoft-365-powershell.md)
    
  - [<span data-ttu-id="0cfda-115">Afficher les comptes d’utilisateur Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cfda-115">View Microsoft 365 user accounts with PowerShell</span></span>](view-user-accounts-with-microsoft-365-powershell.md)
    
- <span data-ttu-id="0cfda-116">Rapports pour SharePoint Online :</span><span class="sxs-lookup"><span data-stu-id="0cfda-116">Reports for SharePoint Online:</span></span>
    
  - [<span data-ttu-id="0cfda-117">Prise en main de SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="0cfda-117">Get started with SharePoint Online Management Shell</span></span>](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
    
  - [<span data-ttu-id="0cfda-118">Get-SPOSiteGroup : obtient tous les groupes sur une collection de sites spécifiée</span><span class="sxs-lookup"><span data-stu-id="0cfda-118">Get-SPOSiteGroup - Gets all the groups on a specified site collection</span></span>](/powershell/module/sharepoint-online/get-spositegroup)
    
- <span data-ttu-id="0cfda-119">Rapports pour Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="0cfda-119">Reports for Exchange Online:</span></span>
    
  - [<span data-ttu-id="0cfda-120">Utiliser Exchange Online PowerShell pour afficher la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="0cfda-120">Use Exchange Online PowerShell to display mailbox</span></span>](/exchange/recipients-in-exchange-online/manage-user-mailboxes/use-powershell-to-display-mailbox-information)
    
    
## <a name="related-articlesl"></a><span data-ttu-id="0cfda-121">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="0cfda-121">Related articlesl</span></span>

[<span data-ttu-id="0cfda-122">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cfda-122">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="0cfda-123">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0cfda-123">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="0cfda-124">Gérer SharePoint avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cfda-124">Manage SharePoint with PowerShell</span></span>](manage-sharepoint-online-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="0cfda-125">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cfda-125">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
