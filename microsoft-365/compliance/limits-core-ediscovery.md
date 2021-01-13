---
title: Limites dans le cas de découverte électronique principale
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Cet article décrit les limites du cas eDiscovery principal dans Microsoft 365.
ms.openlocfilehash: 43d267acdb0c1fee0202c74832b376e066241d7c
ms.sourcegitcommit: 495b66b77d6dbe6d69e5b06b304089e4e476e568
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/12/2021
ms.locfileid: "49799661"
---
# <a name="limits-in-core-ediscovery"></a><span data-ttu-id="d14db-103">Limites dans core eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d14db-103">Limits in Core eDiscovery</span></span>

<span data-ttu-id="d14db-104">Le tableau suivant répertorie les limites pour les cas eDiscovery principaux et les cas de découverte électronique principaux associés à un cas eDiscovery principal.</span><span class="sxs-lookup"><span data-stu-id="d14db-104">The following table lists the limits for core eDiscovery cases and holds associated with a core eDiscovery case.</span></span> <span data-ttu-id="d14db-105">Pour plus d’informations sur Core eDiscovery, voir [Overview of Core eDiscovery](ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="d14db-105">For more information about Core eDiscovery, see [Overview of Core eDiscovery](ediscovery-cases.md).</span></span>
    
  | <span data-ttu-id="d14db-106">Description de la limite</span><span class="sxs-lookup"><span data-stu-id="d14db-106">Description of limit</span></span> | <span data-ttu-id="d14db-107">Limite</span><span class="sxs-lookup"><span data-stu-id="d14db-107">Limit</span></span> |
  |:-----|:-----|
  |<span data-ttu-id="d14db-108">Nombre maximal de cas pour une organisation</span><span class="sxs-lookup"><span data-stu-id="d14db-108">Maximum number of cases for an organization</span></span>  <br/> |<span data-ttu-id="d14db-109">Sans limite</span><span class="sxs-lookup"><span data-stu-id="d14db-109">No limit</span></span>  <br/> |
  |<span data-ttu-id="d14db-110">Nombre maximal de cas d’une organisation</span><span class="sxs-lookup"><span data-stu-id="d14db-110">Maximum number of case holds for an organization</span></span>  <br/> |<span data-ttu-id="d14db-111">10 000</span><span class="sxs-lookup"><span data-stu-id="d14db-111">10,000</span></span>  <br/> |
  |<span data-ttu-id="d14db-112">Nombre maximal de boîtes aux lettres dans une seule et même boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="d14db-112">Maximum number of mailboxes in a single case hold</span></span>  <br/> |<span data-ttu-id="d14db-113">1 000</span><span class="sxs-lookup"><span data-stu-id="d14db-113">1,000</span></span>  <br/> |
  |<span data-ttu-id="d14db-114">Nombre maximal de sites SharePoint et OneDrive Entreprise en une seule fois</span><span class="sxs-lookup"><span data-stu-id="d14db-114">Maximum number of SharePoint and OneDrive for Business sites in a single case hold</span></span>  <br/> |<span data-ttu-id="d14db-115">100</span><span class="sxs-lookup"><span data-stu-id="d14db-115">100</span></span>  <br/> |
  |<span data-ttu-id="d14db-116">Nombre maximal de cas affichés sur la page d’accueil eDiscovery principale, et nombre maximal d’éléments affichés dans les onglets En cours, Recherches et Exportation dans un cas.</span><span class="sxs-lookup"><span data-stu-id="d14db-116">Maximum number of cases displayed on the core eDiscovery home page, and the maximum number of items displayed on the Holds, Searches, and Export tabs within a case.</span></span> <span data-ttu-id="d14db-117"><sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="d14db-117"><sup>1</sup></span></span> |<span data-ttu-id="d14db-118">1 000</span><span class="sxs-lookup"><span data-stu-id="d14db-118">1,000</span></span>|
  |||

   > [!NOTE]
   > <span data-ttu-id="d14db-119"><sup>1</sup> Pour afficher une liste de plus de 1 000 cas, de mise en attente, de recherches ou d’exportations, vous pouvez utiliser les cmdlets PowerShell de sécurité & conformité Office 365 correspondantes :</span><span class="sxs-lookup"><span data-stu-id="d14db-119"><sup>1</sup> To view a list of more than 1,000 cases, holds, searches, or exports, you can use the corresponding Office 365 Security & Compliance PowerShell cmdlets:</span></span>
   > 
   > - [<span data-ttu-id="d14db-120">Get-ComplianceCase</span><span class="sxs-lookup"><span data-stu-id="d14db-120">Get-ComplianceCase</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-compliancecase)
   > - [<span data-ttu-id="d14db-121">Get-CaseHoldPolicy</span><span class="sxs-lookup"><span data-stu-id="d14db-121">Get-CaseHoldPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-caseholdpolicy)
   > - [<span data-ttu-id="d14db-122">Get-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="d14db-122">Get-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-compliancesearch)
   > - [<span data-ttu-id="d14db-123">Get-ComplianceSearchAction</span><span class="sxs-lookup"><span data-stu-id="d14db-123">Get-ComplianceSearchAction</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-compliancesearchaction)

<span data-ttu-id="d14db-124">Pour plus d’informations sur les limites liées aux recherches de contenu et aux exportations associées à un cas core eDiscovery, voir [Limits for Content Search and Core eDiscovery](limits-for-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="d14db-124">For more information about limits related to content searches and exports associated with a Core eDiscovery case, see [Limits for Content Search and Core eDiscovery](limits-for-content-search.md).</span></span>