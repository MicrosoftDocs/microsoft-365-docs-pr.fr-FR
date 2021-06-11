---
title: Répertorier les vulnérabilités par action d'amélioration
description: Récupère une liste des vulnérabilités associées à la recommandation de sécurité.
keywords: api, api de graphique, api pris en charge, obtenir, liste des vulnérabilités, recommandation de sécurité, recommandation de sécurité pour les vulnérabilités, Gestion des menaces et des vulnérabilités, Gestion des menaces et des vulnérabilités api
search.product: eADQiWindows 10XVcnh
ms.prod: w10
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: d5a59c3cd57aa369b1edb46eebddffb84a2b8c78
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52845149"
---
# <a name="list-vulnerabilities-by-recommendation"></a><span data-ttu-id="c88dc-104">Répertorier les vulnérabilités par action d'amélioration</span><span class="sxs-lookup"><span data-stu-id="c88dc-104">List vulnerabilities by recommendation</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c88dc-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="c88dc-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

> <span data-ttu-id="c88dc-106">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="c88dc-106">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="c88dc-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c88dc-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="c88dc-108">Récupère une liste des vulnérabilités associées à la recommandation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c88dc-108">Retrieves a list of vulnerabilities associated with the security recommendation.</span></span>

## <a name="permissions"></a><span data-ttu-id="c88dc-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="c88dc-109">Permissions</span></span>
<span data-ttu-id="c88dc-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="c88dc-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="c88dc-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="c88dc-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="c88dc-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="c88dc-112">Permission type</span></span> |   <span data-ttu-id="c88dc-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="c88dc-113">Permission</span></span>  |   <span data-ttu-id="c88dc-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="c88dc-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="c88dc-115">Application</span><span class="sxs-lookup"><span data-stu-id="c88dc-115">Application</span></span> |   <span data-ttu-id="c88dc-116">SecurityRecommendation.Read.All</span><span class="sxs-lookup"><span data-stu-id="c88dc-116">SecurityRecommendation.Read.All</span></span> |   <span data-ttu-id="c88dc-117">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="c88dc-117">'Read Threat and Vulnerability Management security recommendation information'</span></span>
<span data-ttu-id="c88dc-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="c88dc-118">Delegated (work or school account)</span></span> | <span data-ttu-id="c88dc-119">SecurityRecommendation.Read</span><span class="sxs-lookup"><span data-stu-id="c88dc-119">SecurityRecommendation.Read</span></span> |  <span data-ttu-id="c88dc-120">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="c88dc-120">'Read Threat and Vulnerability Management security recommendation information'</span></span>

## <a name="http-request"></a><span data-ttu-id="c88dc-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="c88dc-121">HTTP request</span></span>
```
GET /api/recommendations/{id}/vulnerabilities
```

## <a name="request-headers"></a><span data-ttu-id="c88dc-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="c88dc-122">Request headers</span></span>

<span data-ttu-id="c88dc-123">Nom</span><span class="sxs-lookup"><span data-stu-id="c88dc-123">Name</span></span> | <span data-ttu-id="c88dc-124">Type</span><span class="sxs-lookup"><span data-stu-id="c88dc-124">Type</span></span> | <span data-ttu-id="c88dc-125">Description</span><span class="sxs-lookup"><span data-stu-id="c88dc-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="c88dc-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="c88dc-126">Authorization</span></span> | <span data-ttu-id="c88dc-127">String</span><span class="sxs-lookup"><span data-stu-id="c88dc-127">String</span></span> | <span data-ttu-id="c88dc-128">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="c88dc-128">Bearer {token}.</span></span> <span data-ttu-id="c88dc-129">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="c88dc-129">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="c88dc-130">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="c88dc-130">Request body</span></span>
<span data-ttu-id="c88dc-131">Vide</span><span class="sxs-lookup"><span data-stu-id="c88dc-131">Empty</span></span>

## <a name="response"></a><span data-ttu-id="c88dc-132">Réponse</span><span class="sxs-lookup"><span data-stu-id="c88dc-132">Response</span></span>
<span data-ttu-id="c88dc-133">Si elle réussit, cette méthode renvoie 200 OK, avec la liste des vulnérabilités associées à la recommandation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c88dc-133">If successful, this method returns 200 OK, with the list of vulnerabilities associated with the security recommendation.</span></span>


## <a name="example"></a><span data-ttu-id="c88dc-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="c88dc-134">Example</span></span>

<span data-ttu-id="c88dc-135">**Demande**</span><span class="sxs-lookup"><span data-stu-id="c88dc-135">**Request**</span></span>

<span data-ttu-id="c88dc-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="c88dc-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/recommendations/va-_-google-_-chrome/vulnerabilities
```

<span data-ttu-id="c88dc-137">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="c88dc-137">**Response**</span></span>

<span data-ttu-id="c88dc-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="c88dc-138">Here is an example of the response.</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Collection(Analytics.Contracts.PublicAPI.PublicVulnerabilityDto)",
    "value": [
        {
            "id": "CVE-2019-13748",
            "name": "CVE-2019-13748",
            "description": "Insufficient policy enforcement in developer tools in Google Chrome prior to 79.0.3945.79 allowed a local attacker to obtain potentially sensitive information from process memory via a crafted HTML page.",
            "severity": "Medium",
            "cvssV3": 6.5,
            "exposedMachines": 0,
            "publishedOn": "2019-12-10T00:00:00Z",
            "updatedOn": "2019-12-16T12:15:00Z",
            "publicExploit": false,
            "exploitVerified": false,
            "exploitInKit": false,
            "exploitTypes": [],
            "exploitUris": []
        }
        ...
     ]
}
```

## <a name="related-topics"></a><span data-ttu-id="c88dc-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c88dc-139">Related topics</span></span>
- [<span data-ttu-id="c88dc-140">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="c88dc-140">Risk-based Threat & Vulnerability Management</span></span>](/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="c88dc-141">Recommandations & sécurité des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="c88dc-141">Threat & Vulnerability security recommendation</span></span>](/microsoft-365/security/defender-endpoint/tvm-security-recommendation)
