---
title: Obtenir une recommandation par logiciel
description: Récupère une recommandation de sécurité liée à un logiciel spécifique.
keywords: api, api de graphique, api pris en charge, obtenir, recommandation de sécurité, recommandation de sécurité pour les logiciels, la gestion des menaces et des vulnérabilités, les api de gestion des menaces et des vulnérabilités
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
ms.openlocfilehash: 82479b0248ceee95321d269e3f48a4eeea3ad193
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51199500"
---
# <a name="get-recommendation-by-software"></a><span data-ttu-id="07cbe-104">Obtenir une recommandation par logiciel</span><span class="sxs-lookup"><span data-stu-id="07cbe-104">Get recommendation by software</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="07cbe-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="07cbe-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

> <span data-ttu-id="07cbe-106">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="07cbe-106">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="07cbe-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="07cbe-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="07cbe-108">Récupère une recommandation de sécurité liée à un logiciel spécifique.</span><span class="sxs-lookup"><span data-stu-id="07cbe-108">Retrieves a security recommendation related to a specific software.</span></span>

## <a name="permissions"></a><span data-ttu-id="07cbe-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="07cbe-109">Permissions</span></span>
<span data-ttu-id="07cbe-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="07cbe-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="07cbe-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="07cbe-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="07cbe-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="07cbe-112">Permission type</span></span> |   <span data-ttu-id="07cbe-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="07cbe-113">Permission</span></span>  |   <span data-ttu-id="07cbe-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="07cbe-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="07cbe-115">Application</span><span class="sxs-lookup"><span data-stu-id="07cbe-115">Application</span></span> |   <span data-ttu-id="07cbe-116">SecurityRecommendation.Read.All</span><span class="sxs-lookup"><span data-stu-id="07cbe-116">SecurityRecommendation.Read.All</span></span> |   <span data-ttu-id="07cbe-117">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="07cbe-117">'Read Threat and Vulnerability Management security recommendation information'</span></span>
<span data-ttu-id="07cbe-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="07cbe-118">Delegated (work or school account)</span></span> | <span data-ttu-id="07cbe-119">SecurityRecommendation.Read</span><span class="sxs-lookup"><span data-stu-id="07cbe-119">SecurityRecommendation.Read</span></span> |  <span data-ttu-id="07cbe-120">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="07cbe-120">'Read Threat and Vulnerability Management security recommendation information'</span></span>

## <a name="http-request"></a><span data-ttu-id="07cbe-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="07cbe-121">HTTP request</span></span>
```
GET /api/recommendations/{id}/software
```

## <a name="request-headers"></a><span data-ttu-id="07cbe-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="07cbe-122">Request headers</span></span>

<span data-ttu-id="07cbe-123">Nom</span><span class="sxs-lookup"><span data-stu-id="07cbe-123">Name</span></span> | <span data-ttu-id="07cbe-124">Type</span><span class="sxs-lookup"><span data-stu-id="07cbe-124">Type</span></span> | <span data-ttu-id="07cbe-125">Description</span><span class="sxs-lookup"><span data-stu-id="07cbe-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="07cbe-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="07cbe-126">Authorization</span></span> | <span data-ttu-id="07cbe-127">Chaîne</span><span class="sxs-lookup"><span data-stu-id="07cbe-127">String</span></span> | <span data-ttu-id="07cbe-128">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="07cbe-128">Bearer {token}.</span></span> <span data-ttu-id="07cbe-129">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="07cbe-129">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="07cbe-130">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="07cbe-130">Request body</span></span>
<span data-ttu-id="07cbe-131">Vide</span><span class="sxs-lookup"><span data-stu-id="07cbe-131">Empty</span></span>

## <a name="response"></a><span data-ttu-id="07cbe-132">Réponse</span><span class="sxs-lookup"><span data-stu-id="07cbe-132">Response</span></span>
<span data-ttu-id="07cbe-133">Si elle réussit, cette méthode renvoie 200 OK avec le logiciel associé aux recommandations de sécurité dans le corps.</span><span class="sxs-lookup"><span data-stu-id="07cbe-133">If successful, this method returns 200 OK with the software associated with the security recommendations in the body.</span></span>


## <a name="example"></a><span data-ttu-id="07cbe-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="07cbe-134">Example</span></span>

<span data-ttu-id="07cbe-135">**Demande**</span><span class="sxs-lookup"><span data-stu-id="07cbe-135">**Request**</span></span>

<span data-ttu-id="07cbe-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="07cbe-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/recommendations/va-_-google-_-chrome/software 
```

<span data-ttu-id="07cbe-137">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="07cbe-137">**Response**</span></span>

<span data-ttu-id="07cbe-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="07cbe-138">Here is an example of the response.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="07cbe-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07cbe-139">Related topics</span></span>
- [<span data-ttu-id="07cbe-140">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="07cbe-140">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="07cbe-141">Recommandations & sécurité des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="07cbe-141">Threat & Vulnerability security recommendation</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-security-recommendation)
