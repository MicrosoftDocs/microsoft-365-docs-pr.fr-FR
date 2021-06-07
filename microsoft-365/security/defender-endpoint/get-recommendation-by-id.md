---
title: Obtenir une recommandation par ID
description: Récupère une recommandation de sécurité par son ID.
keywords: api, api de graphique, api pris en charge, obtenir, recommandation de sécurité, recommandation de sécurité par ID, Gestion des menaces et des vulnérabilités, Gestion des menaces et des vulnérabilités api
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
ms.openlocfilehash: 4ec4758453f43cb211143918ed5fe8fe83e91c3f
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771800"
---
# <a name="get-recommendation-by-id"></a><span data-ttu-id="6a773-104">Obtenir des recommandations par ID</span><span class="sxs-lookup"><span data-stu-id="6a773-104">Get recommendation by ID</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6a773-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="6a773-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="6a773-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6a773-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="6a773-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6a773-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="6a773-108">Récupère une recommandation de sécurité par son ID.</span><span class="sxs-lookup"><span data-stu-id="6a773-108">Retrieves a security recommendation by its ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="6a773-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="6a773-109">Permissions</span></span>
<span data-ttu-id="6a773-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="6a773-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="6a773-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6a773-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="6a773-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="6a773-112">Permission type</span></span> |   <span data-ttu-id="6a773-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="6a773-113">Permission</span></span>  |   <span data-ttu-id="6a773-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="6a773-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="6a773-115">Application</span><span class="sxs-lookup"><span data-stu-id="6a773-115">Application</span></span> |   <span data-ttu-id="6a773-116">SecurityRecommendation.Read.All</span><span class="sxs-lookup"><span data-stu-id="6a773-116">SecurityRecommendation.Read.All</span></span> |   <span data-ttu-id="6a773-117">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="6a773-117">'Read Threat and Vulnerability Management security recommendation information'</span></span>
<span data-ttu-id="6a773-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="6a773-118">Delegated (work or school account)</span></span> | <span data-ttu-id="6a773-119">SecurityRecommendation.Read</span><span class="sxs-lookup"><span data-stu-id="6a773-119">SecurityRecommendation.Read</span></span> |  <span data-ttu-id="6a773-120">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="6a773-120">'Read Threat and Vulnerability Management security recommendation information'</span></span>

## <a name="http-request"></a><span data-ttu-id="6a773-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="6a773-121">HTTP request</span></span>
```
GET /api/recommendations/{id}
```

## <a name="request-headers"></a><span data-ttu-id="6a773-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="6a773-122">Request headers</span></span>

<span data-ttu-id="6a773-123">Nom</span><span class="sxs-lookup"><span data-stu-id="6a773-123">Name</span></span> | <span data-ttu-id="6a773-124">Type</span><span class="sxs-lookup"><span data-stu-id="6a773-124">Type</span></span> | <span data-ttu-id="6a773-125">Description</span><span class="sxs-lookup"><span data-stu-id="6a773-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="6a773-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="6a773-126">Authorization</span></span> | <span data-ttu-id="6a773-127">String</span><span class="sxs-lookup"><span data-stu-id="6a773-127">String</span></span> | <span data-ttu-id="6a773-128">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="6a773-128">Bearer {token}.</span></span> <span data-ttu-id="6a773-129">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="6a773-129">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="6a773-130">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="6a773-130">Request body</span></span>
<span data-ttu-id="6a773-131">Vide</span><span class="sxs-lookup"><span data-stu-id="6a773-131">Empty</span></span>

## <a name="response"></a><span data-ttu-id="6a773-132">Réponse</span><span class="sxs-lookup"><span data-stu-id="6a773-132">Response</span></span>
<span data-ttu-id="6a773-133">Si elle réussit, cette méthode renvoie 200 OK avec les recommandations de sécurité dans le corps.</span><span class="sxs-lookup"><span data-stu-id="6a773-133">If successful, this method returns 200 OK with the security recommendations in the body.</span></span>


## <a name="example"></a><span data-ttu-id="6a773-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="6a773-134">Example</span></span>

<span data-ttu-id="6a773-135">**Demande**</span><span class="sxs-lookup"><span data-stu-id="6a773-135">**Request**</span></span>

<span data-ttu-id="6a773-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="6a773-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/recommendations/va-_-google-_-chrome
```

<span data-ttu-id="6a773-137">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="6a773-137">**Response**</span></span>

<span data-ttu-id="6a773-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="6a773-138">Here is an example of the response.</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Recommendations/$entity",
    "id": "va-_-google-_-chrome",
    "productName": "chrome",
    "recommendationName": "Update Chrome",
    "weaknesses": 38,
    "vendor": "google",
    "recommendedVersion": "",
    "recommendationCategory": "Application",
    "subCategory": "",
    "severityScore": 0,
    "publicExploit": false,
    "activeAlert": false,
    "associatedThreats": [],
    "remediationType": "Update",
    "status": "Active",
    "configScoreImpact": 0,
    "exposureImpact": 3.9441860465116285,
    "totalMachineCount": 6,
    "exposedMachinesCount": 5,
    "nonProductivityImpactedAssets": 0,
    "relatedComponent": "Chrome"
}
```

## <a name="related-topics"></a><span data-ttu-id="6a773-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a773-139">Related topics</span></span>
- [<span data-ttu-id="6a773-140">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="6a773-140">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="6a773-141">Recommandations & sécurité des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="6a773-141">Threat & Vulnerability security recommendation</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-security-recommendation)
