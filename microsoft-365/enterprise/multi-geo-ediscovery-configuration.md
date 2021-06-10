---
title: Configurer Microsoft 365 Multi-Geo eDiscovery
ms.reviewer: adwood
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: o365-solutions
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
localization_priority: Normal
ms.collection: Strat_SP_gtc
description: Découvrez comment utiliser le paramètre Region pour configurer eDiscovery pour une utilisation dans des emplacements satellites Microsoft 365 multigéogé.
ms.openlocfilehash: 4d3481fe8b72bb970893ce065293a7a2cc717331
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50923719"
---
# <a name="microsoft-365-multi-geo-ediscovery-configuration"></a><span data-ttu-id="dd9c1-103">Configuration eDiscovery dans Microsoft 365 Multi-Geo</span><span class="sxs-lookup"><span data-stu-id="dd9c1-103">Microsoft 365 Multi-Geo eDiscovery configuration</span></span>

<span data-ttu-id="dd9c1-104">[Advanced eDiscovery permettent](../compliance/overview-ediscovery-20.md) à un administrateur eDiscovery multigéogé de rechercher toutes les régions géographiques sans avoir à utiliser un filtre de sécurité « Région ».</span><span class="sxs-lookup"><span data-stu-id="dd9c1-104">[Advanced eDiscovery capabilities](../compliance/overview-ediscovery-20.md) allow a multi-geo eDiscovery administrator to search all of the geos without needing to utilize a "Region" security filter.</span></span> <span data-ttu-id="dd9c1-105">Les données sont exportées vers l’instance Azure de l’emplacement central du client multigéogé.</span><span class="sxs-lookup"><span data-stu-id="dd9c1-105">Data is exported to the Azure instance of the central location of the multi-geo tenant.</span></span> 

<span data-ttu-id="dd9c1-106">Sans fonctionnalités eDiscovery avancées, un gestionnaire eDiscovery ou un administrateur d’un client multigéogé ne pourra mener eDiscovery qu’à l’emplacement central de ce client.</span><span class="sxs-lookup"><span data-stu-id="dd9c1-106">Without advanced eDiscovery capabilities, an eDiscovery manager or administrator of a multi-geo tenant will be able to conduct eDiscovery only in the central location of that tenant.</span></span> <span data-ttu-id="dd9c1-107">Pour prendre en charge la possibilité d’effectuer eDiscovery pour des emplacements satellites, un nouveau paramètre de filtre de sécurité de conformité nommé « Region » est disponible via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd9c1-107">To support the ability to conduct eDiscovery for satellite locations, a new compliance security filter parameter named "Region" is available via PowerShell.</span></span> <span data-ttu-id="dd9c1-108">Ce paramètre peut être utilisé par les locataires dont l’emplacement central se trouve en Amérique du Nord, en Europe ou en Asie-Pacifique.</span><span class="sxs-lookup"><span data-stu-id="dd9c1-108">This parameter can be used by tenants whose central location is in North America, Europe, or Asia Pacific.</span></span> <span data-ttu-id="dd9c1-109">Advanced eDiscovery est recommandé pour les locataires dont l’emplacement central n’est pas situé en Amérique du Nord, en Europe ou en Asie-Pacifique et qui doivent effectuer eDiscovery sur plusieurs emplacements géographiques satellites.</span><span class="sxs-lookup"><span data-stu-id="dd9c1-109">Advanced eDiscovery is recommended for tenants whose central location is not in North America, Europe, or Asia Pacific and who need to perform eDiscovery across satellite geo locations.</span></span> 

<span data-ttu-id="dd9c1-110">L’administrateur général Microsoft 365 doit affecter les autorisations de gestionnaire eDiscovery pour autoriser d’autres personnes à mettre en place un processus eDiscovery, et affecter un paramètre "Région" dans le filtre de sécurité de conformité correspondant pour définir la région concernée par le processus comme emplacement satellite. Sinon, aucun processus eDiscovery n’est mis en place à l’emplacement satellite.</span><span class="sxs-lookup"><span data-stu-id="dd9c1-110">The Microsoft 365 global administrator must assign eDiscovery Manager permissions to allow others to perform eDiscovery and assign a "Region" parameter in their applicable Compliance Security Filter to specify the region for conducting eDiscovery as satellite location, otherwise no eDiscovery will be carried out for the satellite location.</span></span>

<span data-ttu-id="dd9c1-p103">Quand un gestionnaire ou un administrateur eDiscovery est défini pour un emplacement satellite particulier, ce gestionnaire ou cet administrateur eDiscovery peut uniquement effectuer des actions de recherche eDiscovery dans les sites SharePoint et OneDrive situés dans cet emplacement satellite. Si un gestionnaire ou un administrateur eDiscovery tente de rechercher des sites SharePoint ou OneDrive en dehors de l’emplacement satellite spécifié, aucun résultat n’est renvoyé. Par ailleurs, lorsque le gestionnaire ou l’administrateur eDiscovery d’un emplacement satellite déclenche une exportation, les données sont exportées vers l’instance Azure de cette région. Ainsi, les entreprises respectent les règles de conformité en interdisant l’exportation de contenu au-delà de frontières contrôlées.</span><span class="sxs-lookup"><span data-stu-id="dd9c1-p103">When the eDiscovery Manager or Administrator role is set for a particular satellite location, the eDiscovery Manager or Administrator will only be able to perform eDiscovery search actions against the SharePoint sites and OneDrive sites located in that satellite location. If an eDiscovery Manager or Administrator attempts to search SharePoint or OneDrive sites outside the specified satellite location, no results will be returned. Also, when the eDiscovery Manager or Administrator for a satellite location triggers an export, data is exported to the Azure instance of that region. This helps organizations stay in compliance by not allowing content to be exported across controlled borders.</span></span>

> [!NOTE]
> <span data-ttu-id="dd9c1-115">Si un gestionnaire eDiscovery doit effectuer des recherches dans plusieurs emplacements satellites SharePoint, un autre compte d’utilisateur doit être créé pour ce gestionnaire, lequel doit indiquer un autre emplacement satellite où sont situés les sites OneDrive ou SharePoint.</span><span class="sxs-lookup"><span data-stu-id="dd9c1-115">If it's necessary for an eDiscovery Manager to search across multiple SharePoint satellite locations, another user account will need to be created for the eDiscovery Manager which specifies the alternate satellite location where the OneDrive or SharePoint sites are located.</span></span>

[!INCLUDE [Microsoft 365 Multi-Geo locations](../includes/microsoft-365-multi-geo-locations.md)]

<span data-ttu-id="dd9c1-116">Pour définir le filtre de sécurité de conformité pour une région :</span><span class="sxs-lookup"><span data-stu-id="dd9c1-116">To set the Compliance Security Filter for a Region:</span></span>

1. [<span data-ttu-id="dd9c1-117">Connectez-vous au centre de conformité Microsoft 365 Security & PowerShell</span><span class="sxs-lookup"><span data-stu-id="dd9c1-117">Connect to Microsoft 365 Security & Compliance Center PowerShell</span></span>](/powershell/exchange/connect-to-scc-powershell)

2. <span data-ttu-id="dd9c1-118">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="dd9c1-118">Use the following syntax:</span></span>

   ```powershell
   New-ComplianceSecurityFilter -Action All -FilterName <TheNameYouWantToAssign> -Region <RegionValue> -Users <UserPrincipalName>
   ```

   <span data-ttu-id="dd9c1-119">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="dd9c1-119">For example:</span></span>

   ```powershell
   New-ComplianceSecurityFilter -Action All -FilterName "NAM eDiscovery Managers" -Region NAM -Users adwood@contoso.onmicrosoft.com
   ```

<span data-ttu-id="dd9c1-120">Consultez l’article [New-ComplianceSecurityFilter](/powershell/module/exchange/new-compliancesecurityfilter) pour en savoir plus sur la syntaxe et les paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="dd9c1-120">See the [New-ComplianceSecurityFilter](/powershell/module/exchange/new-compliancesecurityfilter) article for additional parameters and syntax.</span></span>