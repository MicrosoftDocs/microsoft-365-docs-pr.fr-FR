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
description: Dans cet article, découvrez comment limiter les sites SharePoint à un emplacement géographique spécifié dans un environnement multigéogé.
ms.openlocfilehash: f2a09f177c68d30121c207287e053b2b25405fbc
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689682"
---
# <a name="restrict-sharepoint-site-content-to-a-geo-location"></a><span data-ttu-id="f2135-103">Circonscrire le contenu des sites </span><span class="sxs-lookup"><span data-stu-id="f2135-103">Restrict SharePoint site content to a geo location</span></span>

<span data-ttu-id="f2135-104">Dans certaines circonstances, vous pouvez imposer qu’un site et les fichiers qu’il contient restent dans l’emplacement géographique où le site a été créé, soit en empêchant le déplacement du site, soit en empêchant la mise en cache des fichiers qu’il contient dans un autre emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="f2135-104">Under some circumstances you may choose to enforce a site and its file content to remain in the geo location where the site was created, either by preventing the site from being moved or by preventing the caching of the site's file content in another geo location.</span></span>

<span data-ttu-id="f2135-105">Pour ce faire, vous pouvez utiliser la cmdlet [Set-SPOSite](https://docs.microsoft.com/powershell/module/sharepoint-online/set-sposite) avec le paramètre **RestrictedToGeo**.</span><span class="sxs-lookup"><span data-stu-id="f2135-105">You can do this by using the [Set-SPOSite](https://docs.microsoft.com/powershell/module/sharepoint-online/set-sposite) cmdlet with the **RestrictedToGeo** parameter.</span></span> <span data-ttu-id="f2135-106">La valeur par défaut de ce paramètre est NULL, mais vous pouvez la remplacer par l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f2135-106">This parameter has a default value of NULL, but you can change it to one of the following:</span></span>

|<span data-ttu-id="f2135-107">Restriction</span><span class="sxs-lookup"><span data-stu-id="f2135-107">Restriction</span></span>|<span data-ttu-id="f2135-108">Description</span><span class="sxs-lookup"><span data-stu-id="f2135-108">Description</span></span>|
|:----------|:----------|
|<span data-ttu-id="f2135-109">NoRestriction</span><span class="sxs-lookup"><span data-stu-id="f2135-109">NoRestriction</span></span>|<span data-ttu-id="f2135-110">Le site peut être déplacé vers un autre emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="f2135-110">The site can be moved to another geo location.</span></span>|
|<span data-ttu-id="f2135-111">BlockMoveOnly</span><span class="sxs-lookup"><span data-stu-id="f2135-111">BlockMoveOnly</span></span>|<span data-ttu-id="f2135-112">Le site ne peut pas être déplacé vers un autre emplacement géographique, mais son contenu peut être mis en cache dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="f2135-112">Site cannot be moved to another geo location, but site content can be cached in other geo locations.</span></span>|
|<span data-ttu-id="f2135-113">BlockFull</span><span class="sxs-lookup"><span data-stu-id="f2135-113">BlockFull</span></span>|<span data-ttu-id="f2135-114">Le site ne peut pas être déplacé vers un autre emplacement géographique, et les fichiers qu’il contient ne sont pas mis en cache dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="f2135-114">Site cannot be moved to another geo location, and full file content is not cached in other geo locations.</span></span> <span data-ttu-id="f2135-115">Les titres (extraits du contenu), les noms et d’autres propriétés des fichiers peuvent toujours être mis en cache dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="f2135-115">Files' title (harvested from the content), file name, and other properties of the file can still be cached in other geo-locations.</span></span><br><span data-ttu-id="f2135-116">Le contenu stocké sur le site avant la définition du paramètre RestrictedToGeo sur BlockFull peut rester en cache dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="f2135-116">Content stored in the site before it was configured to BlockFull, may continue to be cached in other geo locations.</span></span>|

<span data-ttu-id="f2135-117">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f2135-117">Use the following syntax:</span></span>

`Set-SPOSite -Identity <siteURL> -RestrictedToGeo <restriction>`

<span data-ttu-id="f2135-118">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f2135-118">For example:</span></span>

`Set-SPOSite -Identity https://contoso.sharepoint.com/sites/RegionRestrictedTeamSite -RestrictedToGeo BlockFull`
