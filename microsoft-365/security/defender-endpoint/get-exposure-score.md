---
title: Obtenir un score d'exposition
description: Récupère le score d’exposition de l’organisation.
keywords: api, api de graphique, api pris en charge, obtenir, score d’exposition, score d’exposition de l’organisation
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
ms.openlocfilehash: c6b3f965c7abb1cb9208f0bfa157c1fd8aa3f891
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500711"
---
# <a name="get-exposure-score"></a><span data-ttu-id="c6ea2-104">Obtenir un score d'exposition</span><span class="sxs-lookup"><span data-stu-id="c6ea2-104">Get exposure score</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c6ea2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c6ea2-105">**Applies to:**</span></span>
- [<span data-ttu-id="c6ea2-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c6ea2-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="c6ea2-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c6ea2-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="c6ea2-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="c6ea2-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="c6ea2-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c6ea2-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="c6ea2-110">Récupère le score d’exposition de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="c6ea2-110">Retrieves the organizational exposure score.</span></span>

## <a name="permissions"></a><span data-ttu-id="c6ea2-111">Autorisations</span><span class="sxs-lookup"><span data-stu-id="c6ea2-111">Permissions</span></span>

<span data-ttu-id="c6ea2-112">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="c6ea2-112">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="c6ea2-113">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="c6ea2-113">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="c6ea2-114">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="c6ea2-114">Permission type</span></span> | <span data-ttu-id="c6ea2-115">Autorisation</span><span class="sxs-lookup"><span data-stu-id="c6ea2-115">Permission</span></span> | <span data-ttu-id="c6ea2-116">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="c6ea2-116">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="c6ea2-117">Application</span><span class="sxs-lookup"><span data-stu-id="c6ea2-117">Application</span></span> | <span data-ttu-id="c6ea2-118">Score.Read.All</span><span class="sxs-lookup"><span data-stu-id="c6ea2-118">Score.Read.All</span></span> | <span data-ttu-id="c6ea2-119">« Lire le score de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="c6ea2-119">'Read Threat and Vulnerability Management score'</span></span>
<span data-ttu-id="c6ea2-120">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="c6ea2-120">Delegated (work or school account)</span></span> | <span data-ttu-id="c6ea2-121">Score.Read</span><span class="sxs-lookup"><span data-stu-id="c6ea2-121">Score.Read</span></span> | <span data-ttu-id="c6ea2-122">« Lire le score de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="c6ea2-122">'Read Threat and Vulnerability Management score'</span></span>

## <a name="http-request"></a><span data-ttu-id="c6ea2-123">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="c6ea2-123">HTTP request</span></span>

```
GET /api/exposureScore
```

## <a name="request-headers"></a><span data-ttu-id="c6ea2-124">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="c6ea2-124">Request headers</span></span>

<span data-ttu-id="c6ea2-125">Nom</span><span class="sxs-lookup"><span data-stu-id="c6ea2-125">Name</span></span> | <span data-ttu-id="c6ea2-126">Type</span><span class="sxs-lookup"><span data-stu-id="c6ea2-126">Type</span></span> | <span data-ttu-id="c6ea2-127">Description</span><span class="sxs-lookup"><span data-stu-id="c6ea2-127">Description</span></span>
:---|:---|:---
<span data-ttu-id="c6ea2-128">Autorisation</span><span class="sxs-lookup"><span data-stu-id="c6ea2-128">Authorization</span></span> | <span data-ttu-id="c6ea2-129">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c6ea2-129">String</span></span> | <span data-ttu-id="c6ea2-130">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="c6ea2-130">Bearer {token}.</span></span> <span data-ttu-id="c6ea2-131">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="c6ea2-131">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="c6ea2-132">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="c6ea2-132">Request body</span></span>

<span data-ttu-id="c6ea2-133">Vide</span><span class="sxs-lookup"><span data-stu-id="c6ea2-133">Empty</span></span>

## <a name="response"></a><span data-ttu-id="c6ea2-134">Réponse</span><span class="sxs-lookup"><span data-stu-id="c6ea2-134">Response</span></span>

<span data-ttu-id="c6ea2-135">Si elle réussit, cette méthode renvoie 200 OK, avec les données d’exposition dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="c6ea2-135">If successful, this method returns 200 OK, with the exposure data in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c6ea2-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="c6ea2-136">Example</span></span>

### <a name="request"></a><span data-ttu-id="c6ea2-137">Demande</span><span class="sxs-lookup"><span data-stu-id="c6ea2-137">Request</span></span>

<span data-ttu-id="c6ea2-138">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="c6ea2-138">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/exposureScore
```

### <a name="response"></a><span data-ttu-id="c6ea2-139">Réponse</span><span class="sxs-lookup"><span data-stu-id="c6ea2-139">Response</span></span>

<span data-ttu-id="c6ea2-140">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="c6ea2-140">Here is an example of the response.</span></span>

>[!NOTE]
><span data-ttu-id="c6ea2-141">La liste de réponses présentée ici peut être tronquée à des raisons de concision.</span><span class="sxs-lookup"><span data-stu-id="c6ea2-141">The response list shown here may be truncated for brevity.</span></span> 

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#ExposureScore/$entity",
    "time": "2019-12-03T07:23:53.280499Z",
    "score": 33.491554051195706
}

```

## <a name="see-also"></a><span data-ttu-id="c6ea2-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6ea2-142">See also</span></span>

- [<span data-ttu-id="c6ea2-143">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="c6ea2-143">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="c6ea2-144">Niveau d’exposition & vulnérabilité des menaces</span><span class="sxs-lookup"><span data-stu-id="c6ea2-144">Threat & Vulnerability exposure score</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-exposure-score)
