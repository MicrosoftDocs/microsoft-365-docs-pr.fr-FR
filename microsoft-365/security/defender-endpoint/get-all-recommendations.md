---
title: Liste de toutes les recommandations
description: Récupère la liste de toutes les recommandations de sécurité affectant l’organisation.
keywords: api, api de graphique, api pris en charge, obtenir, recommandations de sécurité, api tvm mdatp, gestion des menaces et vulnérabilités, api de gestion des menaces et des vulnérabilités
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
ms.openlocfilehash: 5fb68572ee1b154be1db5eb5a092013a1c1a257e
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166594"
---
# <a name="list-all-recommendations"></a><span data-ttu-id="d64cb-104">Liste de toutes les recommandations</span><span class="sxs-lookup"><span data-stu-id="d64cb-104">List all recommendations</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="d64cb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d64cb-105">**Applies to:**</span></span>
- [<span data-ttu-id="d64cb-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d64cb-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="d64cb-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d64cb-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="d64cb-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d64cb-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d64cb-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d64cb-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="d64cb-110">Récupère la liste de toutes les recommandations de sécurité affectant l’organisation.</span><span class="sxs-lookup"><span data-stu-id="d64cb-110">Retrieves a list of all security recommendations affecting the organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="d64cb-111">Autorisations</span><span class="sxs-lookup"><span data-stu-id="d64cb-111">Permissions</span></span>
<span data-ttu-id="d64cb-112">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="d64cb-112">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="d64cb-113">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d64cb-113">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="d64cb-114">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="d64cb-114">Permission type</span></span> |   <span data-ttu-id="d64cb-115">Autorisation</span><span class="sxs-lookup"><span data-stu-id="d64cb-115">Permission</span></span>  |   <span data-ttu-id="d64cb-116">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="d64cb-116">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="d64cb-117">Application</span><span class="sxs-lookup"><span data-stu-id="d64cb-117">Application</span></span> |   <span data-ttu-id="d64cb-118">SecurityRecommendation.Read.All</span><span class="sxs-lookup"><span data-stu-id="d64cb-118">SecurityRecommendation.Read.All</span></span> |   <span data-ttu-id="d64cb-119">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="d64cb-119">'Read Threat and Vulnerability Management security recommendation information'</span></span>
<span data-ttu-id="d64cb-120">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="d64cb-120">Delegated (work or school account)</span></span> | <span data-ttu-id="d64cb-121">SecurityRecommendation.Read</span><span class="sxs-lookup"><span data-stu-id="d64cb-121">SecurityRecommendation.Read</span></span> |  <span data-ttu-id="d64cb-122">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="d64cb-122">'Read Threat and Vulnerability Management security recommendation information'</span></span>

## <a name="http-request"></a><span data-ttu-id="d64cb-123">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="d64cb-123">HTTP request</span></span>
```
GET /api/recommendations
```

## <a name="request-headers"></a><span data-ttu-id="d64cb-124">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="d64cb-124">Request headers</span></span>

<span data-ttu-id="d64cb-125">Nom</span><span class="sxs-lookup"><span data-stu-id="d64cb-125">Name</span></span> | <span data-ttu-id="d64cb-126">Type</span><span class="sxs-lookup"><span data-stu-id="d64cb-126">Type</span></span> | <span data-ttu-id="d64cb-127">Description</span><span class="sxs-lookup"><span data-stu-id="d64cb-127">Description</span></span>
:---|:---|:---
<span data-ttu-id="d64cb-128">Autorisation</span><span class="sxs-lookup"><span data-stu-id="d64cb-128">Authorization</span></span> | <span data-ttu-id="d64cb-129">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d64cb-129">String</span></span> | <span data-ttu-id="d64cb-130">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="d64cb-130">Bearer {token}.</span></span> <span data-ttu-id="d64cb-131">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="d64cb-131">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="d64cb-132">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="d64cb-132">Request body</span></span>
<span data-ttu-id="d64cb-133">Vide</span><span class="sxs-lookup"><span data-stu-id="d64cb-133">Empty</span></span>

## <a name="response"></a><span data-ttu-id="d64cb-134">Réponse</span><span class="sxs-lookup"><span data-stu-id="d64cb-134">Response</span></span>
<span data-ttu-id="d64cb-135">Si elle réussit, cette méthode renvoie 200 OK avec la liste des recommandations de sécurité dans le corps.</span><span class="sxs-lookup"><span data-stu-id="d64cb-135">If successful, this method returns 200 OK with the list of security recommendations in the body.</span></span>


## <a name="example"></a><span data-ttu-id="d64cb-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="d64cb-136">Example</span></span>

<span data-ttu-id="d64cb-137">**Demande**</span><span class="sxs-lookup"><span data-stu-id="d64cb-137">**Request**</span></span>

<span data-ttu-id="d64cb-138">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="d64cb-138">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/recommendations
```

<span data-ttu-id="d64cb-139">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="d64cb-139">**Response**</span></span>

<span data-ttu-id="d64cb-140">Voici un exemple de la réponse.</span><span class="sxs-lookup"><span data-stu-id="d64cb-140">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Recommendations",
    "value": [
        {
            "id": "va-_-microsoft-_-windows_10",
            "productName": "windows_10",
            "recommendationName": "Update Windows 10",
            "weaknesses": 397,
            "vendor": "microsoft",
            "recommendedVersion": "",
            "recommendationCategory": "Application",
            "subCategory": "",
            "severityScore": 0,
            "publicExploit": true,
            "activeAlert": false,
            "associatedThreats": [
                "3098b8ef-23b1-46b3-aed4-499e1928f9ed",
                "40c189d5-0330-4654-a816-e48c2b7f9c4b",
                "4b0c9702-9b6c-4ca2-9d02-1556869f56f8",
                "e8fc2121-3cf3-4dd2-9ea0-87d7e1d2b29d",
                "94b6e94b-0c1d-4817-ac06-c3b8639be3ab"
            ],
            "remediationType": "Update",
            "status": "Active",
            "configScoreImpact": 0,
            "exposureImpact": 7.674418604651163,
            "totalMachineCount": 37,
            "exposedMachinesCount": 7,
            "nonProductivityImpactedAssets": 0,
            "relatedComponent": "Windows 10"
        }
        ...
     ]
}
```
## <a name="see-also"></a><span data-ttu-id="d64cb-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d64cb-141">See also</span></span>
- [<span data-ttu-id="d64cb-142">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="d64cb-142">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="d64cb-143">Recommandations & sécurité des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="d64cb-143">Threat & Vulnerability security recommendation</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-security-recommendation)

