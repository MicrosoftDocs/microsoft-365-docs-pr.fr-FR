---
title: Obtenir toutes les vulnérabilités par ordinateur et par logiciel
description: Récupère une liste de toutes les vulnérabilités affectant l'organisation par l'ordinateur et les logiciels
keywords: api, api de graphique, api pris en charge, obtenir, informations de vulnérabilité, api tvm Microsoft Defender pour endpoint
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dolmont
author: DulceMontemayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 229c1f9e77a0cb85744155e82934b48dd63052b2
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933408"
---
# <a name="list-vulnerabilities-by-machine-and-software"></a><span data-ttu-id="28b75-104">Répertorier les vulnérabilités par ordinateur et logiciel</span><span class="sxs-lookup"><span data-stu-id="28b75-104">List vulnerabilities by machine and software</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="28b75-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="28b75-105">**Applies to:**</span></span>
- [<span data-ttu-id="28b75-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="28b75-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="28b75-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="28b75-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="28b75-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="28b75-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="28b75-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="28b75-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


<span data-ttu-id="28b75-110">Récupère une liste de toutes les vulnérabilités affectant l'organisation par [ordinateur et](machine.md) [par logiciel.](software.md)</span><span class="sxs-lookup"><span data-stu-id="28b75-110">Retrieves a list of all the vulnerabilities affecting the organization per [machine](machine.md) and [software](software.md).</span></span>
- <span data-ttu-id="28b75-111">Si la vulnérabilité a une ko de réparation, elle apparaît dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="28b75-111">If the vulnerability has a fixing KB, it will appear in the response.</span></span>
- <span data-ttu-id="28b75-112">Prend [en charge les requêtes OData V4.](https://www.odata.org/documentation/)</span><span class="sxs-lookup"><span data-stu-id="28b75-112">Supports [OData V4 queries](https://www.odata.org/documentation/).</span></span>
- <span data-ttu-id="28b75-113">OData est ```$filter``` pris en charge sur toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="28b75-113">The OData ```$filter``` is supported on all properties.</span></span>

>[!Tip]
><span data-ttu-id="28b75-114">Il s'agit d'une EXCELLENTE API pour [l'intégration de Power BI.](api-power-bi.md)</span><span class="sxs-lookup"><span data-stu-id="28b75-114">This is great API for [Power BI integration](api-power-bi.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="28b75-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="28b75-115">Permissions</span></span>
<span data-ttu-id="28b75-116">L'une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="28b75-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="28b75-117">Pour plus d'informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="28b75-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="28b75-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="28b75-118">Permission type</span></span> |   <span data-ttu-id="28b75-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="28b75-119">Permission</span></span>  |   <span data-ttu-id="28b75-120">Nom d'affichage de l'autorisation</span><span class="sxs-lookup"><span data-stu-id="28b75-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="28b75-121">Application</span><span class="sxs-lookup"><span data-stu-id="28b75-121">Application</span></span> |   <span data-ttu-id="28b75-122">Vulnerability.Read.All</span><span class="sxs-lookup"><span data-stu-id="28b75-122">Vulnerability.Read.All</span></span> |    <span data-ttu-id="28b75-123">« Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="28b75-123">'Read Threat and Vulnerability Management vulnerability information'</span></span>
<span data-ttu-id="28b75-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="28b75-124">Delegated (work or school account)</span></span> | <span data-ttu-id="28b75-125">Vulnerability.Read</span><span class="sxs-lookup"><span data-stu-id="28b75-125">Vulnerability.Read</span></span> |   <span data-ttu-id="28b75-126">« Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="28b75-126">'Read Threat and Vulnerability Management vulnerability information'</span></span>

## <a name="http-request"></a><span data-ttu-id="28b75-127">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="28b75-127">HTTP request</span></span>
```
GET /api/vulnerabilities/machinesVulnerabilities
```

## <a name="request-headers"></a><span data-ttu-id="28b75-128">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="28b75-128">Request headers</span></span>

<span data-ttu-id="28b75-129">Nom</span><span class="sxs-lookup"><span data-stu-id="28b75-129">Name</span></span> | <span data-ttu-id="28b75-130">Type</span><span class="sxs-lookup"><span data-stu-id="28b75-130">Type</span></span> | <span data-ttu-id="28b75-131">Description</span><span class="sxs-lookup"><span data-stu-id="28b75-131">Description</span></span>
:---|:---|:---
<span data-ttu-id="28b75-132">Autorisation</span><span class="sxs-lookup"><span data-stu-id="28b75-132">Authorization</span></span> | <span data-ttu-id="28b75-133">String</span><span class="sxs-lookup"><span data-stu-id="28b75-133">String</span></span> | <span data-ttu-id="28b75-134">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="28b75-134">Bearer {token}.</span></span> <span data-ttu-id="28b75-135">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="28b75-135">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="28b75-136">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="28b75-136">Request body</span></span>
<span data-ttu-id="28b75-137">Vide</span><span class="sxs-lookup"><span data-stu-id="28b75-137">Empty</span></span>

## <a name="response"></a><span data-ttu-id="28b75-138">Réponse</span><span class="sxs-lookup"><span data-stu-id="28b75-138">Response</span></span>
<span data-ttu-id="28b75-139">Si elle réussit, cette méthode renvoie 200 OK avec la liste des vulnérabilités dans le corps.</span><span class="sxs-lookup"><span data-stu-id="28b75-139">If successful, this method returns 200 OK with the list of vulnerabilities in the body.</span></span>


## <a name="example"></a><span data-ttu-id="28b75-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="28b75-140">Example</span></span>

<span data-ttu-id="28b75-141">**Demande**</span><span class="sxs-lookup"><span data-stu-id="28b75-141">**Request**</span></span>

<span data-ttu-id="28b75-142">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="28b75-142">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/vulnerabilities/machinesVulnerabilities
```

<span data-ttu-id="28b75-143">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="28b75-143">**Response**</span></span>

<span data-ttu-id="28b75-144">Voici un exemple de la réponse.</span><span class="sxs-lookup"><span data-stu-id="28b75-144">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Collection(microsoft.windowsDefenderATP.api.PublicAssetVulnerabilityDto)",
    "value": [
        {
            "id": "5afa3afc92a7c63d4b70129e0a6f33f63a427e21-_-CVE-2020-6494-_-microsoft-_-edge_chromium-based-_-81.0.416.77-_-",
            "cveId": "CVE-2020-6494",
            "machineId": "5afa3afc92a7c63d4b70129e0a6f33f63a427e21",
            "fixingKbId": null,
            "productName": "edge_chromium-based",
            "productVendor": "microsoft",
            "productVersion": "81.0.416.77",
            "severity": "Low"
        },
        {
            "id": "7a704e17d1c2977c0e7b665fb18ae6e1fe7f3283-_-CVE-2016-3348-_-microsoft-_-windows_server_2012_r2-_-6.3.9600.19728-_-3185911",
            "cveId": "CVE-2016-3348",
            "machineId": "7a704e17d1c2977c0e7b665fb18ae6e1fe7f3283",
            "fixingKbId": "3185911",
            "productName": "windows_server_2012_r2",
            "productVendor": "microsoft",
            "productVersion": "6.3.9600.19728",
            "severity": "Low"
        },
        ...
    ]

}
```

## <a name="see-also"></a><span data-ttu-id="28b75-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28b75-145">See also</span></span>

- [<span data-ttu-id="28b75-146">Gestion des menaces et des vulnérabilités basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="28b75-146">Risk-based threat and vulnerability management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="28b75-147">Vulnérabilités dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="28b75-147">Vulnerabilities in your organization</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-weaknesses)
