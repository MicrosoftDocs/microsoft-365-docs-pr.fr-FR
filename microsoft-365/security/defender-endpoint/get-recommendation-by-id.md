---
title: Obtenir une recommandation par ID
description: Récupère une recommandation de sécurité par son ID.
keywords: api, api de graphique, api pris en charge, obtenir, recommandation de sécurité, recommandation de sécurité par ID, gestion des menaces et vulnérabilités, api de gestion des menaces et des vulnérabilités
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
ms.openlocfilehash: 45a151fc5855a4a2b1ba63a50b54737c90e6bdd1
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51199512"
---
# <a name="get-recommendation-by-id"></a><span data-ttu-id="9b419-104">Obtenir une recommandation par ID</span><span class="sxs-lookup"><span data-stu-id="9b419-104">Get recommendation by ID</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9b419-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="9b419-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="9b419-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="9b419-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="9b419-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9b419-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="9b419-108">Récupère une recommandation de sécurité par son ID.</span><span class="sxs-lookup"><span data-stu-id="9b419-108">Retrieves a security recommendation by its ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="9b419-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="9b419-109">Permissions</span></span>
<span data-ttu-id="9b419-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="9b419-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="9b419-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9b419-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="9b419-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="9b419-112">Permission type</span></span> |   <span data-ttu-id="9b419-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9b419-113">Permission</span></span>  |   <span data-ttu-id="9b419-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="9b419-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="9b419-115">Application</span><span class="sxs-lookup"><span data-stu-id="9b419-115">Application</span></span> |   <span data-ttu-id="9b419-116">SecurityRecommendation.Read.All</span><span class="sxs-lookup"><span data-stu-id="9b419-116">SecurityRecommendation.Read.All</span></span> |   <span data-ttu-id="9b419-117">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="9b419-117">'Read Threat and Vulnerability Management security recommendation information'</span></span>
<span data-ttu-id="9b419-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="9b419-118">Delegated (work or school account)</span></span> | <span data-ttu-id="9b419-119">SecurityRecommendation.Read</span><span class="sxs-lookup"><span data-stu-id="9b419-119">SecurityRecommendation.Read</span></span> |  <span data-ttu-id="9b419-120">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="9b419-120">'Read Threat and Vulnerability Management security recommendation information'</span></span>

## <a name="http-request"></a><span data-ttu-id="9b419-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="9b419-121">HTTP request</span></span>
```
GET /api/recommendations/{id}
```

## <a name="request-headers"></a><span data-ttu-id="9b419-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="9b419-122">Request headers</span></span>

<span data-ttu-id="9b419-123">Nom</span><span class="sxs-lookup"><span data-stu-id="9b419-123">Name</span></span> | <span data-ttu-id="9b419-124">Type</span><span class="sxs-lookup"><span data-stu-id="9b419-124">Type</span></span> | <span data-ttu-id="9b419-125">Description</span><span class="sxs-lookup"><span data-stu-id="9b419-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="9b419-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9b419-126">Authorization</span></span> | <span data-ttu-id="9b419-127">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9b419-127">String</span></span> | <span data-ttu-id="9b419-128">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="9b419-128">Bearer {token}.</span></span> <span data-ttu-id="9b419-129">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="9b419-129">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="9b419-130">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="9b419-130">Request body</span></span>
<span data-ttu-id="9b419-131">Vide</span><span class="sxs-lookup"><span data-stu-id="9b419-131">Empty</span></span>

## <a name="response"></a><span data-ttu-id="9b419-132">Réponse</span><span class="sxs-lookup"><span data-stu-id="9b419-132">Response</span></span>
<span data-ttu-id="9b419-133">Si elle réussit, cette méthode renvoie 200 OK avec les recommandations de sécurité dans le corps.</span><span class="sxs-lookup"><span data-stu-id="9b419-133">If successful, this method returns 200 OK with the security recommendations in the body.</span></span>


## <a name="example"></a><span data-ttu-id="9b419-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="9b419-134">Example</span></span>

<span data-ttu-id="9b419-135">**Demande**</span><span class="sxs-lookup"><span data-stu-id="9b419-135">**Request**</span></span>

<span data-ttu-id="9b419-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="9b419-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/recommendations/va-_-google-_-chrome
```

<span data-ttu-id="9b419-137">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="9b419-137">**Response**</span></span>

<span data-ttu-id="9b419-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="9b419-138">Here is an example of the response.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9b419-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b419-139">Related topics</span></span>
- [<span data-ttu-id="9b419-140">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="9b419-140">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="9b419-141">Recommandations & sécurité des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="9b419-141">Threat & Vulnerability security recommendation</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-security-recommendation)
