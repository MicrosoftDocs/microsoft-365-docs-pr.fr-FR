---
title: Obtenir les vulnérabilités découvertes
description: Récupère une collection de vulnérabilités découvertes liées à un ID d’appareil donné.
keywords: api, api de graphique, api pris en charge, obtenir, liste, fichier, informations, vulnérabilités découvertes, api de gestion des & menace, api tvm mdatp
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
author: dansimp
ms.author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 73b8fe5140ff635791e7d42358024bb7fb4ee926
ms.sourcegitcommit: 6e5c00f84b5201422aed094f2697016407df8fc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51570326"
---
# <a name="get-discovered-vulnerabilities"></a><span data-ttu-id="e5ce4-104">Obtenir les vulnérabilités découvertes</span><span class="sxs-lookup"><span data-stu-id="e5ce4-104">Get discovered vulnerabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e5ce4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e5ce4-105">**Applies to:**</span></span>
- [<span data-ttu-id="e5ce4-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e5ce4-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="e5ce4-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e5ce4-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="e5ce4-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e5ce4-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e5ce4-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e5ce4-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="e5ce4-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="e5ce4-110">API description</span></span>
<span data-ttu-id="e5ce4-111">Récupère une collection de vulnérabilités découvertes liées à un ID d’appareil donné.</span><span class="sxs-lookup"><span data-stu-id="e5ce4-111">Retrieves a collection of discovered vulnerabilities related to a given device ID.</span></span>

## <a name="limitations"></a><span data-ttu-id="e5ce4-112">Limites</span><span class="sxs-lookup"><span data-stu-id="e5ce4-112">Limitations</span></span>
1. <span data-ttu-id="e5ce4-113">Les limites de taux pour cette API sont de 50 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="e5ce4-113">Rate limitations for this API are 50 calls per minute and 1500 calls per hour.</span></span>

## <a name="permissions"></a><span data-ttu-id="e5ce4-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="e5ce4-114">Permissions</span></span>

<span data-ttu-id="e5ce4-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="e5ce4-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="e5ce4-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="e5ce4-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="e5ce4-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="e5ce4-117">Permission type</span></span> | <span data-ttu-id="e5ce4-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e5ce4-118">Permission</span></span> | <span data-ttu-id="e5ce4-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="e5ce4-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="e5ce4-120">Application</span><span class="sxs-lookup"><span data-stu-id="e5ce4-120">Application</span></span> |<span data-ttu-id="e5ce4-121">Vulnerability.Read.All</span><span class="sxs-lookup"><span data-stu-id="e5ce4-121">Vulnerability.Read.All</span></span> | <span data-ttu-id="e5ce4-122">« Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="e5ce4-122">'Read Threat and Vulnerability Management vulnerability information'</span></span>
<span data-ttu-id="e5ce4-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="e5ce4-123">Delegated (work or school account)</span></span> | <span data-ttu-id="e5ce4-124">Vulnerability.Read</span><span class="sxs-lookup"><span data-stu-id="e5ce4-124">Vulnerability.Read</span></span> | <span data-ttu-id="e5ce4-125">« Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="e5ce4-125">'Read Threat and Vulnerability Management vulnerability information'</span></span>

## <a name="http-request"></a><span data-ttu-id="e5ce4-126">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="e5ce4-126">HTTP request</span></span>

```
GET /api/machines/{machineId}/vulnerabilities
```

## <a name="request-headers"></a><span data-ttu-id="e5ce4-127">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="e5ce4-127">Request headers</span></span>

<span data-ttu-id="e5ce4-128">Nom</span><span class="sxs-lookup"><span data-stu-id="e5ce4-128">Name</span></span> | <span data-ttu-id="e5ce4-129">Type</span><span class="sxs-lookup"><span data-stu-id="e5ce4-129">Type</span></span> | <span data-ttu-id="e5ce4-130">Description</span><span class="sxs-lookup"><span data-stu-id="e5ce4-130">Description</span></span>
:---|:---|:---
<span data-ttu-id="e5ce4-131">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e5ce4-131">Authorization</span></span> | <span data-ttu-id="e5ce4-132">String</span><span class="sxs-lookup"><span data-stu-id="e5ce4-132">String</span></span> | <span data-ttu-id="e5ce4-133">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="e5ce4-133">Bearer {token}.</span></span> <span data-ttu-id="e5ce4-134">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="e5ce4-134">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="e5ce4-135">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="e5ce4-135">Request body</span></span>

<span data-ttu-id="e5ce4-136">Vide</span><span class="sxs-lookup"><span data-stu-id="e5ce4-136">Empty</span></span>

## <a name="response"></a><span data-ttu-id="e5ce4-137">Réponse</span><span class="sxs-lookup"><span data-stu-id="e5ce4-137">Response</span></span>

<span data-ttu-id="e5ce4-138">Si elle réussit, cette méthode renvoie 200 OK avec les informations de vulnérabilité découvertes dans le corps.</span><span class="sxs-lookup"><span data-stu-id="e5ce4-138">If successful, this method returns 200 OK with the discovered vulnerability information in the body.</span></span>

## <a name="example"></a><span data-ttu-id="e5ce4-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="e5ce4-139">Example</span></span>

### <a name="request"></a><span data-ttu-id="e5ce4-140">Demande</span><span class="sxs-lookup"><span data-stu-id="e5ce4-140">Request</span></span>

<span data-ttu-id="e5ce4-141">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="e5ce4-141">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/ac233fa6208e1579620bf44207c4006ed7cc4501/vulnerabilities
```

### <a name="response"></a><span data-ttu-id="e5ce4-142">Réponse</span><span class="sxs-lookup"><span data-stu-id="e5ce4-142">Response</span></span>

<span data-ttu-id="e5ce4-143">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="e5ce4-143">Here is an example of the response.</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Collection(Analytics.Contracts.PublicAPI.PublicVulnerabilityDto)",
    "value": [
        {
            "id": "CVE-2019-1348",
            "name": "CVE-2019-1348",
            "description": "Git could allow a remote attacker to bypass security restrictions, caused by a flaw in the --export-marks option of git fast-import. By persuading a victim to import specially-crafted content, an attacker could exploit this vulnerability to overwrite arbitrary paths.",
            "severity": "Medium",
            "cvssV3": 4.3,
            "exposedMachines": 1,
            "publishedOn": "2019-12-13T00:00:00Z",
            "updatedOn": "2019-12-13T00:00:00Z",
            "publicExploit": false,
            "exploitVerified": false,
            "exploitInKit": false,
            "exploitTypes": [],
            "exploitUris": []
        }
}
```

## <a name="see-also"></a><span data-ttu-id="e5ce4-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5ce4-144">See also</span></span>

- [<span data-ttu-id="e5ce4-145">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="e5ce4-145">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="e5ce4-146">Vulnérabilités dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="e5ce4-146">Vulnerabilities in your organization</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-weaknesses)
