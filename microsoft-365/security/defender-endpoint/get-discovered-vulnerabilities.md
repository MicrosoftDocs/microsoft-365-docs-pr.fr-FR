---
title: Obtenir les vulnérabilités découvertes
description: Récupère une collection de vulnérabilités découvertes liées à un ID d’appareil donné.
keywords: api, api de graphique, api pris en charge, obtenir, liste, fichier, informations, vulnérabilités découvertes, api & gestion des vulnérabilités menace, Api tvm Microsoft Defender pour endpoint
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 73d9803736df546f2381b7a84c9089d2460c4c44
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843081"
---
# <a name="get-discovered-vulnerabilities"></a><span data-ttu-id="2921b-104">Obtenir les vulnérabilités découvertes</span><span class="sxs-lookup"><span data-stu-id="2921b-104">Get discovered vulnerabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2921b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2921b-105">**Applies to:**</span></span>
- [<span data-ttu-id="2921b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2921b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="2921b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2921b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="2921b-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2921b-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="2921b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2921b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="2921b-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="2921b-110">API description</span></span>
<span data-ttu-id="2921b-111">Récupère une collection de vulnérabilités découvertes liées à un ID d’appareil donné.</span><span class="sxs-lookup"><span data-stu-id="2921b-111">Retrieves a collection of discovered vulnerabilities related to a given device ID.</span></span>

## <a name="limitations"></a><span data-ttu-id="2921b-112">Limites</span><span class="sxs-lookup"><span data-stu-id="2921b-112">Limitations</span></span>
1. <span data-ttu-id="2921b-113">Les limites de taux pour cette API sont de 50 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="2921b-113">Rate limitations for this API are 50 calls per minute and 1500 calls per hour.</span></span>

## <a name="permissions"></a><span data-ttu-id="2921b-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="2921b-114">Permissions</span></span>

<span data-ttu-id="2921b-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="2921b-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="2921b-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="2921b-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="2921b-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="2921b-117">Permission type</span></span> | <span data-ttu-id="2921b-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="2921b-118">Permission</span></span> | <span data-ttu-id="2921b-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="2921b-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="2921b-120">Application</span><span class="sxs-lookup"><span data-stu-id="2921b-120">Application</span></span> |<span data-ttu-id="2921b-121">Vulnerability.Read.All</span><span class="sxs-lookup"><span data-stu-id="2921b-121">Vulnerability.Read.All</span></span> | <span data-ttu-id="2921b-122">« Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="2921b-122">'Read Threat and Vulnerability Management vulnerability information'</span></span>
<span data-ttu-id="2921b-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="2921b-123">Delegated (work or school account)</span></span> | <span data-ttu-id="2921b-124">Vulnerability.Read</span><span class="sxs-lookup"><span data-stu-id="2921b-124">Vulnerability.Read</span></span> | <span data-ttu-id="2921b-125">« Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="2921b-125">'Read Threat and Vulnerability Management vulnerability information'</span></span>

## <a name="http-request"></a><span data-ttu-id="2921b-126">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="2921b-126">HTTP request</span></span>

```
GET /api/machines/{machineId}/vulnerabilities
```

## <a name="request-headers"></a><span data-ttu-id="2921b-127">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="2921b-127">Request headers</span></span>

<span data-ttu-id="2921b-128">Nom</span><span class="sxs-lookup"><span data-stu-id="2921b-128">Name</span></span> | <span data-ttu-id="2921b-129">Type</span><span class="sxs-lookup"><span data-stu-id="2921b-129">Type</span></span> | <span data-ttu-id="2921b-130">Description</span><span class="sxs-lookup"><span data-stu-id="2921b-130">Description</span></span>
:---|:---|:---
<span data-ttu-id="2921b-131">Autorisation</span><span class="sxs-lookup"><span data-stu-id="2921b-131">Authorization</span></span> | <span data-ttu-id="2921b-132">String</span><span class="sxs-lookup"><span data-stu-id="2921b-132">String</span></span> | <span data-ttu-id="2921b-133">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="2921b-133">Bearer {token}.</span></span> <span data-ttu-id="2921b-134">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="2921b-134">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="2921b-135">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="2921b-135">Request body</span></span>

<span data-ttu-id="2921b-136">Vide</span><span class="sxs-lookup"><span data-stu-id="2921b-136">Empty</span></span>

## <a name="response"></a><span data-ttu-id="2921b-137">Réponse</span><span class="sxs-lookup"><span data-stu-id="2921b-137">Response</span></span>

<span data-ttu-id="2921b-138">Si elle réussit, cette méthode renvoie 200 OK avec les informations de vulnérabilité découvertes dans le corps.</span><span class="sxs-lookup"><span data-stu-id="2921b-138">If successful, this method returns 200 OK with the discovered vulnerability information in the body.</span></span>

## <a name="example"></a><span data-ttu-id="2921b-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="2921b-139">Example</span></span>

### <a name="request"></a><span data-ttu-id="2921b-140">Demande</span><span class="sxs-lookup"><span data-stu-id="2921b-140">Request</span></span>

<span data-ttu-id="2921b-141">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="2921b-141">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/ac233fa6208e1579620bf44207c4006ed7cc4501/vulnerabilities
```

### <a name="response"></a><span data-ttu-id="2921b-142">Réponse</span><span class="sxs-lookup"><span data-stu-id="2921b-142">Response</span></span>

<span data-ttu-id="2921b-143">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="2921b-143">Here is an example of the response.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="2921b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2921b-144">See also</span></span>

- [<span data-ttu-id="2921b-145">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="2921b-145">Risk-based Threat & Vulnerability Management</span></span>](/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="2921b-146">Vulnérabilités de votre organisation</span><span class="sxs-lookup"><span data-stu-id="2921b-146">Vulnerabilities in your organization</span></span>](/microsoft-365/security/defender-endpoint/tvm-weaknesses)
