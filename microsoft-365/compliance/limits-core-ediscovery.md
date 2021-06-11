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
description: Cet article décrit les limites du cas eDiscovery principal Microsoft 365.
ms.openlocfilehash: e7b1013abd9fd94748baf3b83dd04efbc3831a1d
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52311423"
---
# <a name="limits-in-core-ediscovery"></a><span data-ttu-id="a62fa-103">Limites dans core eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a62fa-103">Limits in Core eDiscovery</span></span>

<span data-ttu-id="a62fa-104">Le tableau suivant répertorie les limites pour les cas eDiscovery principaux et les cas de découverte électronique principaux associés à un cas eDiscovery principal.</span><span class="sxs-lookup"><span data-stu-id="a62fa-104">The following table lists the limits for core eDiscovery cases and holds associated with a core eDiscovery case.</span></span> <span data-ttu-id="a62fa-105">Pour plus d’informations sur Core eDiscovery, voir [Overview of Core eDiscovery](./get-started-core-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="a62fa-105">For more information about Core eDiscovery, see [Overview of Core eDiscovery](./get-started-core-ediscovery.md).</span></span>
    
  | <span data-ttu-id="a62fa-106">Description de la limite</span><span class="sxs-lookup"><span data-stu-id="a62fa-106">Description of limit</span></span> | <span data-ttu-id="a62fa-107">Limite</span><span class="sxs-lookup"><span data-stu-id="a62fa-107">Limit</span></span> |
  |:-----|:-----|
  |<span data-ttu-id="a62fa-108">Nombre maximal de cas pour une organisation.</span><span class="sxs-lookup"><span data-stu-id="a62fa-108">Maximum number of cases for an organization.</span></span>  <br/> |<span data-ttu-id="a62fa-109">Sans limite</span><span class="sxs-lookup"><span data-stu-id="a62fa-109">No limit</span></span>  <br/> |
  |<span data-ttu-id="a62fa-110">Nombre maximal de cas d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="a62fa-110">Maximum number of case holds for an organization.</span></span>  <br/> |<span data-ttu-id="a62fa-111">10 000</span><span class="sxs-lookup"><span data-stu-id="a62fa-111">10,000</span></span>  <br/> |
  |<span data-ttu-id="a62fa-112">Nombre maximal de boîtes aux lettres dans une seule et même boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a62fa-112">Maximum number of mailboxes in a single case hold.</span></span> <span data-ttu-id="a62fa-113">Cette limite inclut le total combiné de boîtes aux lettres utilisateur et les boîtes aux lettres associées aux groupes Microsoft 365, Microsoft Teams et Yammer groupes.</span><span class="sxs-lookup"><span data-stu-id="a62fa-113">This limit includes the combined total of user mailboxes, and the mailboxes associated with Microsoft 365 Groups, Microsoft Teams, and Yammer Groups.</span></span>  <br/> |<span data-ttu-id="a62fa-114">1 000</span><span class="sxs-lookup"><span data-stu-id="a62fa-114">1,000</span></span>  <br/> |
  |<span data-ttu-id="a62fa-115">Nombre maximal de sites dans une seule et même période d’attente.</span><span class="sxs-lookup"><span data-stu-id="a62fa-115">Maximum number of sites in a single case hold.</span></span> <span data-ttu-id="a62fa-116">Cette limite inclut le total combiné des sites OneDrive Entreprise, des sites SharePoint et des sites associés aux groupes Microsoft 365, Microsoft Teams et Yammer groupes.</span><span class="sxs-lookup"><span data-stu-id="a62fa-116">This limit includes the combined total of OneDrive for Business sites, SharePoint sites, and the sites associated with Microsoft 365 Groups, Microsoft Teams, and Yammer Groups.</span></span>  <br/> |<span data-ttu-id="a62fa-117">100</span><span class="sxs-lookup"><span data-stu-id="a62fa-117">100</span></span>  <br/> |
  |<span data-ttu-id="a62fa-118">Nombre maximal de cas affichés sur la page d’accueil eDiscovery principale, et nombre maximal d’éléments affichés dans les onglets En cours, Recherches et Exportation dans un cas.</span><span class="sxs-lookup"><span data-stu-id="a62fa-118">Maximum number of cases displayed on the core eDiscovery home page, and the maximum number of items displayed on the Holds, Searches, and Export tabs within a case.</span></span> <span data-ttu-id="a62fa-119"><sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="a62fa-119"><sup>1</sup></span></span> |<span data-ttu-id="a62fa-120">1 000</span><span class="sxs-lookup"><span data-stu-id="a62fa-120">1,000</span></span>|
  |||

   > [!NOTE]
   > <span data-ttu-id="a62fa-121"><sup>1</sup> Pour afficher une liste de plus de 1 000 cas, de mise en attente, de recherches ou d’exportations, vous pouvez utiliser les cmdlets PowerShell de sécurité Office 365 & conformité correspondantes :</span><span class="sxs-lookup"><span data-stu-id="a62fa-121"><sup>1</sup> To view a list of more than 1,000 cases, holds, searches, or exports, you can use the corresponding Office 365 Security & Compliance PowerShell cmdlets:</span></span>
   > 
   > - [<span data-ttu-id="a62fa-122">Get-ComplianceCase</span><span class="sxs-lookup"><span data-stu-id="a62fa-122">Get-ComplianceCase</span></span>](/powershell/module/exchange/get-compliancecase)
   > - [<span data-ttu-id="a62fa-123">Get-CaseHoldPolicy</span><span class="sxs-lookup"><span data-stu-id="a62fa-123">Get-CaseHoldPolicy</span></span>](/powershell/module/exchange/get-caseholdpolicy)
   > - [<span data-ttu-id="a62fa-124">Get-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="a62fa-124">Get-ComplianceSearch</span></span>](/powershell/module/exchange/get-compliancesearch)
   > - [<span data-ttu-id="a62fa-125">Get-ComplianceSearchAction</span><span class="sxs-lookup"><span data-stu-id="a62fa-125">Get-ComplianceSearchAction</span></span>](/powershell/module/exchange/get-compliancesearchaction)

<span data-ttu-id="a62fa-126">Pour plus d’informations sur les limites liées aux recherches et aux exportations associées à un cas core eDiscovery, voir Limites pour la recherche de contenu et core [eDiscovery](limits-for-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="a62fa-126">For more information about limits related to searches and exports associated with a Core eDiscovery case, see [Limits for Content search and Core eDiscovery](limits-for-content-search.md).</span></span>