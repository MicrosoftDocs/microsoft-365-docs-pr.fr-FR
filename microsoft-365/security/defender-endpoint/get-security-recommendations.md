---
title: Obtenir des recommandations de sécurité
description: Récupère une collection de recommandations de sécurité relatives à un ID d’appareil donné.
keywords: api, api de graphique, api pris en charge, obtenir, liste, fichier, informations, recommandation de sécurité par appareil, api de gestion des menaces & vulnérabilité, api tvm mdatp
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
ms.openlocfilehash: 6c65926985c7c8a194ab87c44c3fc269488c463c
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51199764"
---
# <a name="get-security-recommendations"></a><span data-ttu-id="61847-104">Obtenir des recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="61847-104">Get security recommendations</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="61847-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="61847-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

> <span data-ttu-id="61847-106">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="61847-106">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="61847-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="61847-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="61847-108">Récupère une collection de recommandations de sécurité relatives à un ID d’appareil donné.</span><span class="sxs-lookup"><span data-stu-id="61847-108">Retrieves a collection of security recommendations related to a given device ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="61847-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="61847-109">Permissions</span></span>
<span data-ttu-id="61847-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="61847-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="61847-111">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="61847-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="61847-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="61847-112">Permission type</span></span> |   <span data-ttu-id="61847-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="61847-113">Permission</span></span>  |   <span data-ttu-id="61847-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="61847-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="61847-115">Application</span><span class="sxs-lookup"><span data-stu-id="61847-115">Application</span></span> | <span data-ttu-id="61847-116">SecurityRecommendation.Read.All</span><span class="sxs-lookup"><span data-stu-id="61847-116">SecurityRecommendation.Read.All</span></span> | <span data-ttu-id="61847-117">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="61847-117">'Read Threat and Vulnerability Management security recommendation information'</span></span>
<span data-ttu-id="61847-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="61847-118">Delegated (work or school account)</span></span> | <span data-ttu-id="61847-119">SecurityRecommendation.Read</span><span class="sxs-lookup"><span data-stu-id="61847-119">SecurityRecommendation.Read</span></span> |  <span data-ttu-id="61847-120">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="61847-120">'Read Threat and Vulnerability Management security recommendation information'</span></span>

## <a name="http-request"></a><span data-ttu-id="61847-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="61847-121">HTTP request</span></span>
```
GET /api/machines/{machineId}/recommendations
```

## <a name="request-headers"></a><span data-ttu-id="61847-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="61847-122">Request headers</span></span>

<span data-ttu-id="61847-123">Nom</span><span class="sxs-lookup"><span data-stu-id="61847-123">Name</span></span> | <span data-ttu-id="61847-124">Type</span><span class="sxs-lookup"><span data-stu-id="61847-124">Type</span></span> | <span data-ttu-id="61847-125">Description</span><span class="sxs-lookup"><span data-stu-id="61847-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="61847-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="61847-126">Authorization</span></span> | <span data-ttu-id="61847-127">Chaîne</span><span class="sxs-lookup"><span data-stu-id="61847-127">String</span></span> | <span data-ttu-id="61847-128">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="61847-128">Bearer {token}.</span></span> <span data-ttu-id="61847-129">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="61847-129">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="61847-130">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="61847-130">Request body</span></span>
<span data-ttu-id="61847-131">Vide</span><span class="sxs-lookup"><span data-stu-id="61847-131">Empty</span></span>

## <a name="response"></a><span data-ttu-id="61847-132">Réponse</span><span class="sxs-lookup"><span data-stu-id="61847-132">Response</span></span>
<span data-ttu-id="61847-133">Si elle réussit, cette méthode renvoie 200 OK avec les recommandations de sécurité dans le corps.</span><span class="sxs-lookup"><span data-stu-id="61847-133">If successful, this method returns 200 OK with the security recommendations in the body.</span></span>


## <a name="example"></a><span data-ttu-id="61847-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="61847-134">Example</span></span>

<span data-ttu-id="61847-135">**Demande**</span><span class="sxs-lookup"><span data-stu-id="61847-135">**Request**</span></span>

<span data-ttu-id="61847-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="61847-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/machines/ac233fa6208e1579620bf44207c4006ed7cc4501/recommendations
```

<span data-ttu-id="61847-137">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="61847-137">**Response**</span></span>

<span data-ttu-id="61847-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="61847-138">Here is an example of the response.</span></span>


```
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Recommendations",
    "value": [
        {
            "id": "va-_-git-scm-_-git",
            "productName": "git",
            "recommendationName": "Update Git to version 2.24.1.2",
            "weaknesses": 3,
            "vendor": "git-scm",
            "recommendedVersion": "2.24.1.2",
            "recommendationCategory": "Application",
            "subCategory": "",
            "severityScore": 0,
            "publicExploit": false,
            "activeAlert": false,
            "associatedThreats": [],
            "remediationType": "Update",
            "status": "Active",
            "configScoreImpact": 0,
            "exposureImpact": 0,
            "totalMachineCount": 0,
            "exposedMachinesCount": 1,
            "nonProductivityImpactedAssets": 0,
            "relatedComponent": "Git"
        },
…
}
```

## <a name="related-topics"></a><span data-ttu-id="61847-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61847-139">Related topics</span></span>
- [<span data-ttu-id="61847-140">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="61847-140">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="61847-141">Recommandations & sécurité des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="61847-141">Threat & Vulnerability security recommendation</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-security-recommendation)
