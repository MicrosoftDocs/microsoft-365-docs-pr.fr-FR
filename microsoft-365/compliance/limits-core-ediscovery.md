---
title: Limites dans le cas eDiscovery de base
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Cet article décrit les limites du cas de découverte électronique de base dans Microsoft 365.
ms.openlocfilehash: 4d91b81caee31e693ce29c6d8d629d563d973ae7
ms.sourcegitcommit: bd51f626f0c7788c2a3cf89deee25264659aebd5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "43551398"
---
# <a name="limits-in-core-ediscovery"></a><span data-ttu-id="b1283-103">Limites de la découverte électronique de base</span><span class="sxs-lookup"><span data-stu-id="b1283-103">Limits in core eDiscovery</span></span>

<span data-ttu-id="b1283-104">Le tableau suivant répertorie les limites pour les cas de découverte électronique principaux et les blocages associés à un cas de découverte électronique principale.</span><span class="sxs-lookup"><span data-stu-id="b1283-104">The following table lists the limits for core eDiscovery cases and holds associated with a core eDiscovery case.</span></span> <span data-ttu-id="b1283-105">Pour plus d’informations sur la découverte électronique principale, voir [Overview of Core eDiscovery](ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="b1283-105">For more information about core eDiscovery, see [Overview of core eDiscovery](ediscovery-cases.md).</span></span>
    
  |<span data-ttu-id="b1283-106">**Description de la limite**</span><span class="sxs-lookup"><span data-stu-id="b1283-106">**Description of limit**</span></span>|<span data-ttu-id="b1283-107">**Limite**</span><span class="sxs-lookup"><span data-stu-id="b1283-107">**Limit**</span></span>|
  |:-----|:-----|
  |<span data-ttu-id="b1283-108">Nombre maximal de cas pour une organisation</span><span class="sxs-lookup"><span data-stu-id="b1283-108">Maximum number of cases for an organization</span></span>  <br/> |<span data-ttu-id="b1283-109">Sans limite</span><span class="sxs-lookup"><span data-stu-id="b1283-109">No limit</span></span>  <br/> |
  |<span data-ttu-id="b1283-110">Nombre maximal de blocages pour une organisation</span><span class="sxs-lookup"><span data-stu-id="b1283-110">Maximum number of case holds for an organization</span></span>  <br/> |<span data-ttu-id="b1283-111">10 000</span><span class="sxs-lookup"><span data-stu-id="b1283-111">10,000</span></span>  <br/> |
  |<span data-ttu-id="b1283-112">Nombre maximal de boîtes aux lettres en une seule suspension de cas</span><span class="sxs-lookup"><span data-stu-id="b1283-112">Maximum number of mailboxes in a single case hold</span></span>  <br/> |<span data-ttu-id="b1283-113">1 000</span><span class="sxs-lookup"><span data-stu-id="b1283-113">1,000</span></span>  <br/> |
  |<span data-ttu-id="b1283-114">Nombre maximal de sites SharePoint et OneDrive entreprise en une seule suspension de cas</span><span class="sxs-lookup"><span data-stu-id="b1283-114">Maximum number of SharePoint and OneDrive for Business sites in a single case hold</span></span>  <br/> |<span data-ttu-id="b1283-115">100</span><span class="sxs-lookup"><span data-stu-id="b1283-115">100</span></span>  <br/> |
  |<span data-ttu-id="b1283-116">Nombre maximal de cas affichés sur la page d’accueil eDiscovery principale et nombre maximal d’éléments affichés dans les onglets conservation, recherches et exportation dans un cas.</span><span class="sxs-lookup"><span data-stu-id="b1283-116">Maximum number of cases displayed on the core eDiscovery home page, and the maximum number of items displayed on the Holds, Searches, and Export tabs within a case.</span></span> <span data-ttu-id="b1283-117"><sup>0,1</sup></span><span class="sxs-lookup"><span data-stu-id="b1283-117"><sup>1</sup></span></span> |<span data-ttu-id="b1283-118">1 000</span><span class="sxs-lookup"><span data-stu-id="b1283-118">1,000</span></span>|
  |||

   > [!NOTE]
   > <span data-ttu-id="b1283-119"><sup>1</sup> pour afficher une liste de plus de 1 000 cas, de suspensions, de recherches ou d’exportations, vous pouvez utiliser la cmdlet Office 365 Security & Compliance PowerShell correspondante :</span><span class="sxs-lookup"><span data-stu-id="b1283-119"><sup>1</sup> To view a list of more than 1,000 cases, holds, searches, or exports, you can use the corresponding Office 365 Security & Compliance PowerShell cmdlet:</span></span><br/> [<span data-ttu-id="b1283-120">Get-ComplianceCase</span><span class="sxs-lookup"><span data-stu-id="b1283-120">Get-ComplianceCase</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-ediscovery/get-compliancecase) <br/> [<span data-ttu-id="b1283-121">Get-CaseHoldPolicy</span><span class="sxs-lookup"><span data-stu-id="b1283-121">Get-CaseHoldPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-ediscovery/get-caseholdpolicy)<br/> [<span data-ttu-id="b1283-122">Get-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="b1283-122">Get-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/get-compliancesearch)<br/> [<span data-ttu-id="b1283-123">Get-ComplianceSearchAction</span><span class="sxs-lookup"><span data-stu-id="b1283-123">Get-ComplianceSearchAction</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/get-compliancesearchaction)
