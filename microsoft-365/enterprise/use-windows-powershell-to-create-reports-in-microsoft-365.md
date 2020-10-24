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
description: 'Résumé : utilisez PowerShell pour Microsoft 365 pour créer des rapports que vous ne pouvez pas produire dans le centre d’administration Microsoft 365.'
ms.openlocfilehash: 10000f62b1d6a747cf0373623c6038b080666e1a
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48753977"
---
# <a name="use-powershell-to-create-reports-for-microsoft-365"></a><span data-ttu-id="55446-103">Utilisation de PowerShell pour créer des rapports pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="55446-103">Use PowerShell to create reports for Microsoft 365</span></span>

<span data-ttu-id="55446-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="55446-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="55446-105">De nombreux rapports différents sont disponibles dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="55446-105">Many different reports are available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="55446-106">Toutefois, ces rapports ne fournissent que très peu d’informations et, parfois, vous avez besoin de plus.</span><span class="sxs-lookup"><span data-stu-id="55446-106">But these reports only provide so much information, and sometimes you need more.</span></span> <span data-ttu-id="55446-107">C’est lorsque vous avez besoin de PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="55446-107">That's when you need PowerShell for Microsoft 365.</span></span>
  
<span data-ttu-id="55446-108">Ces articles expliquent comment utiliser PowerShell pour Microsoft 365 pour obtenir des informations à partir de votre client Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="55446-108">These articles describe how to use PowerShell for Microsoft 365 to get information from your Microsoft 365 tenant:</span></span>
  
- <span data-ttu-id="55446-109">Prise en main de la création de rapports à l’aide de PowerShell pour Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="55446-109">Get started with reporting using PowerShell for Microsoft 365:</span></span>
    
  - [<span data-ttu-id="55446-110">Pourquoi utiliser PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="55446-110">Why you need to use PowerShell for Microsoft 365</span></span>](https://technet.microsoft.com/library/dn568034.aspx#reveal)
    
    
- <span data-ttu-id="55446-111">Rapports pour les comptes d’utilisateurs et les licences :</span><span class="sxs-lookup"><span data-stu-id="55446-111">Reports for user accounts and licenses:</span></span>
    
  - [<span data-ttu-id="55446-112">Afficher les licences et les services Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="55446-112">View Microsoft 365 licenses and services with PowerShell</span></span>](view-licenses-and-services-with-microsoft-365-powershell.md)
    
  - [<span data-ttu-id="55446-113">Afficher les utilisateurs titulaires d’une licence et d’utilisateurs sans licence Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="55446-113">View Microsoft 365 licensed and unlicensed users with PowerShell</span></span>](view-licensed-and-unlicensed-users-with-microsoft-365-powershell.md)
    
  - [<span data-ttu-id="55446-114">Afficher les détails de service et de licence de compte Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="55446-114">View Microsoft 365 account license and service details with PowerShell</span></span>](view-account-license-and-service-details-with-microsoft-365-powershell.md)
    
  - [<span data-ttu-id="55446-115">Afficher les comptes d’utilisateur Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="55446-115">View Microsoft 365 user accounts with PowerShell</span></span>](view-user-accounts-with-microsoft-365-powershell.md)
    
- <span data-ttu-id="55446-116">Rapports pour SharePoint Online :</span><span class="sxs-lookup"><span data-stu-id="55446-116">Reports for SharePoint Online:</span></span>
    
  - [<span data-ttu-id="55446-117">Prise en main de SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="55446-117">Get started with SharePoint Online Management Shell</span></span>](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
    
  - [<span data-ttu-id="55446-118">Get-SPOSiteGroup-obtient tous les groupes sur une collection de sites spécifiée</span><span class="sxs-lookup"><span data-stu-id="55446-118">Get-SPOSiteGroup - Gets all the groups on a specified site collection</span></span>](https://technet.microsoft.com/library/122f4099-c78d-4cce-bab0-4343b04596ae.aspx)
    
- <span data-ttu-id="55446-119">Rapports pour Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="55446-119">Reports for Exchange Online:</span></span>
    
  - [<span data-ttu-id="55446-120">Utiliser Exchange Online PowerShell pour afficher la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="55446-120">Use Exchange Online PowerShell to display mailbox</span></span>](https://technet.microsoft.com/library/13843002-56ca-4b75-81c5-84386522b01b.aspx)
    
    
## <a name="related-articlesl"></a><span data-ttu-id="55446-121">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="55446-121">Related articlesl</span></span>

[<span data-ttu-id="55446-122">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="55446-122">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="55446-123">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="55446-123">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="55446-124">Gérer SharePoint avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="55446-124">Manage SharePoint with PowerShell</span></span>](manage-sharepoint-online-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="55446-125">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="55446-125">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  