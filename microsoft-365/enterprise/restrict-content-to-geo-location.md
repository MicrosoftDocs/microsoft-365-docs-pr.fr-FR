---
title: 'Circonscrire le contenu des sites '
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
ms.collection: Strat_SP_gtc
localization_priority: Normal
description: Dans cet article, découvrez comment limiter SharePoint sites à un emplacement géographique spécifié dans un environnement multigéogé.
ms.openlocfilehash: 74255db19b2ecf9b333d33208c63da260b2bd747
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50927263"
---
# <a name="restrict-sharepoint-site-content-to-a-geo-location"></a><span data-ttu-id="fd3db-103">Circonscrire le contenu des sites </span><span class="sxs-lookup"><span data-stu-id="fd3db-103">Restrict SharePoint site content to a geo location</span></span>

<span data-ttu-id="fd3db-104">Dans certaines circonstances, vous pouvez imposer qu’un site et les fichiers qu’il contient restent dans l’emplacement géographique où le site a été créé, soit en empêchant le déplacement du site, soit en empêchant la mise en cache des fichiers qu’il contient dans un autre emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="fd3db-104">Under some circumstances you may choose to enforce a site and its file content to remain in the geo location where the site was created, either by preventing the site from being moved or by preventing the caching of the site's file content in another geo location.</span></span>

<span data-ttu-id="fd3db-105">Pour ce faire, vous pouvez utiliser la cmdlet [Set-SPOSite](/powershell/module/sharepoint-online/set-sposite) avec le paramètre **RestrictedToGeo**.</span><span class="sxs-lookup"><span data-stu-id="fd3db-105">You can do this by using the [Set-SPOSite](/powershell/module/sharepoint-online/set-sposite) cmdlet with the **RestrictedToGeo** parameter.</span></span> <span data-ttu-id="fd3db-106">La valeur par défaut de ce paramètre est NULL, mais vous pouvez la remplacer par l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd3db-106">This parameter has a default value of NULL, but you can change it to one of the following:</span></span>

|<span data-ttu-id="fd3db-107">Restriction</span><span class="sxs-lookup"><span data-stu-id="fd3db-107">Restriction</span></span>|<span data-ttu-id="fd3db-108">Description</span><span class="sxs-lookup"><span data-stu-id="fd3db-108">Description</span></span>|
|:----------|:----------|
|<span data-ttu-id="fd3db-109">NoRestriction</span><span class="sxs-lookup"><span data-stu-id="fd3db-109">NoRestriction</span></span>|<span data-ttu-id="fd3db-110">Le site peut être déplacé vers un autre emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="fd3db-110">The site can be moved to another geo location.</span></span>|
|<span data-ttu-id="fd3db-111">BlockMoveOnly</span><span class="sxs-lookup"><span data-stu-id="fd3db-111">BlockMoveOnly</span></span>|<span data-ttu-id="fd3db-112">Le site ne peut pas être déplacé vers un autre emplacement géographique, mais son contenu peut être mis en cache dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="fd3db-112">Site cannot be moved to another geo location, but site content can be cached in other geo locations.</span></span>|
|<span data-ttu-id="fd3db-113">BlockFull</span><span class="sxs-lookup"><span data-stu-id="fd3db-113">BlockFull</span></span>|<span data-ttu-id="fd3db-114">Le site ne peut pas être déplacé vers un autre emplacement géographique, et les fichiers qu’il contient ne sont pas mis en cache dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="fd3db-114">Site cannot be moved to another geo location, and full file content is not cached in other geo locations.</span></span> <span data-ttu-id="fd3db-115">Les titres (extraits du contenu), les noms et d’autres propriétés des fichiers peuvent toujours être mis en cache dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="fd3db-115">Files' title (harvested from the content), file name, and other properties of the file can still be cached in other geo-locations.</span></span><br><span data-ttu-id="fd3db-116">Le contenu stocké sur le site avant la définition du paramètre RestrictedToGeo sur BlockFull peut rester en cache dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="fd3db-116">Content stored in the site before it was configured to BlockFull, may continue to be cached in other geo locations.</span></span>|

<span data-ttu-id="fd3db-117">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fd3db-117">Use the following syntax:</span></span>

`Set-SPOSite -Identity <siteURL> -RestrictedToGeo <restriction>`

<span data-ttu-id="fd3db-118">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="fd3db-118">For example:</span></span>

`Set-SPOSite -Identity https://contoso.sharepoint.com/sites/RegionRestrictedTeamSite -RestrictedToGeo BlockFull`