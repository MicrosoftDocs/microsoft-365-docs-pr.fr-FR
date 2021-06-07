---
title: Obtenir les actions d’amélioration par logiciel
description: Récupère une recommandation de sécurité liée à un logiciel spécifique.
keywords: api, api de graphique, api pris en charge, obtenir, recommandation de sécurité, recommandation de sécurité pour les logiciels, Gestion des menaces et des vulnérabilités, Gestion des menaces et des vulnérabilités api
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
ms.openlocfilehash: 68bc53f2ae0b44567530cc1dd733c9dd37d380ca
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769586"
---
# <a name="get-recommendation-by-software"></a><span data-ttu-id="65cfc-104">Obtenir les actions d’amélioration par logiciel</span><span class="sxs-lookup"><span data-stu-id="65cfc-104">Get recommendation by software</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="65cfc-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="65cfc-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

> <span data-ttu-id="65cfc-106">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="65cfc-106">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="65cfc-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="65cfc-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="65cfc-108">Récupère une recommandation de sécurité liée à un logiciel spécifique.</span><span class="sxs-lookup"><span data-stu-id="65cfc-108">Retrieves a security recommendation related to a specific software.</span></span>

## <a name="permissions"></a><span data-ttu-id="65cfc-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="65cfc-109">Permissions</span></span>
<span data-ttu-id="65cfc-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="65cfc-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="65cfc-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="65cfc-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="65cfc-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="65cfc-112">Permission type</span></span> |   <span data-ttu-id="65cfc-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="65cfc-113">Permission</span></span>  |   <span data-ttu-id="65cfc-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="65cfc-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="65cfc-115">Application</span><span class="sxs-lookup"><span data-stu-id="65cfc-115">Application</span></span> |   <span data-ttu-id="65cfc-116">SecurityRecommendation.Read.All</span><span class="sxs-lookup"><span data-stu-id="65cfc-116">SecurityRecommendation.Read.All</span></span> |   <span data-ttu-id="65cfc-117">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="65cfc-117">'Read Threat and Vulnerability Management security recommendation information'</span></span>
<span data-ttu-id="65cfc-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="65cfc-118">Delegated (work or school account)</span></span> | <span data-ttu-id="65cfc-119">SecurityRecommendation.Read</span><span class="sxs-lookup"><span data-stu-id="65cfc-119">SecurityRecommendation.Read</span></span> |  <span data-ttu-id="65cfc-120">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="65cfc-120">'Read Threat and Vulnerability Management security recommendation information'</span></span>

## <a name="http-request"></a><span data-ttu-id="65cfc-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="65cfc-121">HTTP request</span></span>
```
GET /api/recommendations/{id}/software
```

## <a name="request-headers"></a><span data-ttu-id="65cfc-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="65cfc-122">Request headers</span></span>

<span data-ttu-id="65cfc-123">Nom</span><span class="sxs-lookup"><span data-stu-id="65cfc-123">Name</span></span> | <span data-ttu-id="65cfc-124">Type</span><span class="sxs-lookup"><span data-stu-id="65cfc-124">Type</span></span> | <span data-ttu-id="65cfc-125">Description</span><span class="sxs-lookup"><span data-stu-id="65cfc-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="65cfc-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="65cfc-126">Authorization</span></span> | <span data-ttu-id="65cfc-127">String</span><span class="sxs-lookup"><span data-stu-id="65cfc-127">String</span></span> | <span data-ttu-id="65cfc-128">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="65cfc-128">Bearer {token}.</span></span> <span data-ttu-id="65cfc-129">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="65cfc-129">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="65cfc-130">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="65cfc-130">Request body</span></span>
<span data-ttu-id="65cfc-131">Vide</span><span class="sxs-lookup"><span data-stu-id="65cfc-131">Empty</span></span>

## <a name="response"></a><span data-ttu-id="65cfc-132">Réponse</span><span class="sxs-lookup"><span data-stu-id="65cfc-132">Response</span></span>
<span data-ttu-id="65cfc-133">Si elle réussit, cette méthode renvoie 200 OK avec le logiciel associé aux recommandations de sécurité dans le corps.</span><span class="sxs-lookup"><span data-stu-id="65cfc-133">If successful, this method returns 200 OK with the software associated with the security recommendations in the body.</span></span>


## <a name="example"></a><span data-ttu-id="65cfc-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="65cfc-134">Example</span></span>

<span data-ttu-id="65cfc-135">**Demande**</span><span class="sxs-lookup"><span data-stu-id="65cfc-135">**Request**</span></span>

<span data-ttu-id="65cfc-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="65cfc-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/recommendations/va-_-google-_-chrome/software 
```

<span data-ttu-id="65cfc-137">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="65cfc-137">**Response**</span></span>

<span data-ttu-id="65cfc-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="65cfc-138">Here is an example of the response.</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Analytics.Contracts.PublicAPI.PublicProductDto",
    "id": "google-_-chrome",
    "name": "chrome",
    "vendor": "google",
    "weaknesses": 38,
    "publicExploit": false,
    "activeAlert": false,
    "exposedMachines": 5,
    "impactScore": 3.94418621
}
```

## <a name="related-topics"></a><span data-ttu-id="65cfc-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65cfc-139">Related topics</span></span>
- [<span data-ttu-id="65cfc-140">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="65cfc-140">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="65cfc-141">Recommandations & sécurité des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="65cfc-141">Threat & Vulnerability security recommendation</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-security-recommendation)
