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
ms.openlocfilehash: e18e1e6c1d9d7ecd78deaf267be72ccdc9d1ba5d
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50905886"
---
# <a name="limits-in-core-ediscovery"></a><span data-ttu-id="23ba3-103">Limites dans Core eDiscovery</span><span class="sxs-lookup"><span data-stu-id="23ba3-103">Limits in Core eDiscovery</span></span>

<span data-ttu-id="23ba3-104">Le tableau suivant répertorie les limites pour les cas eDiscovery principaux et les cas de découverte électronique principaux associés à un cas eDiscovery principal.</span><span class="sxs-lookup"><span data-stu-id="23ba3-104">The following table lists the limits for core eDiscovery cases and holds associated with a core eDiscovery case.</span></span> <span data-ttu-id="23ba3-105">Pour plus d’informations sur Core eDiscovery, voir [Vue d’ensemble de Core eDiscovery](./get-started-core-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="23ba3-105">For more information about Core eDiscovery, see [Overview of Core eDiscovery](./get-started-core-ediscovery.md).</span></span>
    
  | <span data-ttu-id="23ba3-106">Description de la limite</span><span class="sxs-lookup"><span data-stu-id="23ba3-106">Description of limit</span></span> | <span data-ttu-id="23ba3-107">Limite</span><span class="sxs-lookup"><span data-stu-id="23ba3-107">Limit</span></span> |
  |:-----|:-----|
  |<span data-ttu-id="23ba3-108">Nombre maximal de cas pour une organisation.</span><span class="sxs-lookup"><span data-stu-id="23ba3-108">Maximum number of cases for an organization.</span></span>  <br/> |<span data-ttu-id="23ba3-109">Sans limite</span><span class="sxs-lookup"><span data-stu-id="23ba3-109">No limit</span></span>  <br/> |
  |<span data-ttu-id="23ba3-110">Nombre maximal de cas d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="23ba3-110">Maximum number of case holds for an organization.</span></span>  <br/> |<span data-ttu-id="23ba3-111">10 000</span><span class="sxs-lookup"><span data-stu-id="23ba3-111">10,000</span></span>  <br/> |
  |<span data-ttu-id="23ba3-112">Nombre maximal de boîtes aux lettres dans une seule et même boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="23ba3-112">Maximum number of mailboxes in a single case hold.</span></span> <span data-ttu-id="23ba3-113">Cette limite inclut le total combiné de boîtes aux lettres utilisateur et les boîtes aux lettres associées aux groupes Microsoft 365, Microsoft Teams et Yammer groupes.</span><span class="sxs-lookup"><span data-stu-id="23ba3-113">This limit includes the combined total of user mailboxes, and the mailboxes associated with Microsoft 365 Groups, Microsoft Teams, and Yammer Groups.</span></span>  <br/> |<span data-ttu-id="23ba3-114">1 000</span><span class="sxs-lookup"><span data-stu-id="23ba3-114">1,000</span></span>  <br/> |
  |<span data-ttu-id="23ba3-115">Nombre maximal de sites dans une seule et même période d’attente.</span><span class="sxs-lookup"><span data-stu-id="23ba3-115">Maximum number of sites in a single case hold.</span></span> <span data-ttu-id="23ba3-116">Cette limite inclut le total combiné des sites OneDrive Entreprise, des sites SharePoint et des sites associés aux groupes Microsoft 365, Microsoft Teams et Yammer groupes.</span><span class="sxs-lookup"><span data-stu-id="23ba3-116">This limit includes the combined total of OneDrive for Business sites, SharePoint sites, and the sites associated with Microsoft 365 Groups, Microsoft Teams, and Yammer Groups.</span></span>  <br/> |<span data-ttu-id="23ba3-117">100</span><span class="sxs-lookup"><span data-stu-id="23ba3-117">100</span></span>  <br/> |
  |<span data-ttu-id="23ba3-118">Nombre maximal de cas affichés sur la page d’accueil eDiscovery principale, et nombre maximal d’éléments affichés dans les onglets En cours, Recherches et Exportation dans un cas.</span><span class="sxs-lookup"><span data-stu-id="23ba3-118">Maximum number of cases displayed on the core eDiscovery home page, and the maximum number of items displayed on the Holds, Searches, and Export tabs within a case.</span></span> <span data-ttu-id="23ba3-119"><sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="23ba3-119"><sup>1</sup></span></span> |<span data-ttu-id="23ba3-120">1 000</span><span class="sxs-lookup"><span data-stu-id="23ba3-120">1,000</span></span>|
  |||

   > [!NOTE]
   > <span data-ttu-id="23ba3-121"><sup>1</sup> Pour afficher une liste de plus de 1 000 cas, de mise en attente, de recherches ou d’exportations, vous pouvez utiliser les cmdlets PowerShell de sécurité & et de conformité Office 365 correspondantes :</span><span class="sxs-lookup"><span data-stu-id="23ba3-121"><sup>1</sup> To view a list of more than 1,000 cases, holds, searches, or exports, you can use the corresponding Office 365 Security & Compliance PowerShell cmdlets:</span></span>
   > 
   > - [<span data-ttu-id="23ba3-122">Get-ComplianceCase</span><span class="sxs-lookup"><span data-stu-id="23ba3-122">Get-ComplianceCase</span></span>](/powershell/module/exchange/get-compliancecase)
   > - [<span data-ttu-id="23ba3-123">Get-CaseHoldPolicy</span><span class="sxs-lookup"><span data-stu-id="23ba3-123">Get-CaseHoldPolicy</span></span>](/powershell/module/exchange/get-caseholdpolicy)
   > - [<span data-ttu-id="23ba3-124">Get-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="23ba3-124">Get-ComplianceSearch</span></span>](/powershell/module/exchange/get-compliancesearch)
   > - [<span data-ttu-id="23ba3-125">Get-ComplianceSearchAction</span><span class="sxs-lookup"><span data-stu-id="23ba3-125">Get-ComplianceSearchAction</span></span>](/powershell/module/exchange/get-compliancesearchaction)

<span data-ttu-id="23ba3-126">Pour plus d’informations sur les limites liées aux recherches de contenu et aux exportations associées à un cas core eDiscovery, voir Limites pour la recherche de contenu et core [eDiscovery](limits-for-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="23ba3-126">For more information about limits related to content searches and exports associated with a Core eDiscovery case, see [Limits for Content Search and Core eDiscovery](limits-for-content-search.md).</span></span>