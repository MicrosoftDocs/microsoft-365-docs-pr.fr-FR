---
title: Liste du score d’exposition par groupe d’appareils
description: Récupère une liste des scores d’exposition par groupe d’appareils.
keywords: api, api de graphique, api pris en charge, obtenir, score d’exposition, groupe d’appareils, score d’exposition du groupe d’appareils
search.product: eADQiWindows 10XVcnh
ms.prod: w10
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
ms.openlocfilehash: 54b3e0cd63189e67de0aa101634508ff8833dc6a
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500242"
---
# <a name="list-exposure-score-by-device-group"></a><span data-ttu-id="c212a-104">Liste du score d’exposition par groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="c212a-104">List exposure score by device group</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c212a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c212a-105">**Applies to:**</span></span>
- [<span data-ttu-id="c212a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c212a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="c212a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c212a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="c212a-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="c212a-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="c212a-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c212a-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="c212a-110">Récupère une collection d’alertes liées à une adresse de domaine donnée.</span><span class="sxs-lookup"><span data-stu-id="c212a-110">Retrieves a collection of alerts related to a given domain address.</span></span>

## <a name="permissions"></a><span data-ttu-id="c212a-111">Autorisations</span><span class="sxs-lookup"><span data-stu-id="c212a-111">Permissions</span></span>

<span data-ttu-id="c212a-112">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="c212a-112">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="c212a-113">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="c212a-113">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="c212a-114">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="c212a-114">Permission type</span></span> |   <span data-ttu-id="c212a-115">Autorisation</span><span class="sxs-lookup"><span data-stu-id="c212a-115">Permission</span></span>  |   <span data-ttu-id="c212a-116">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="c212a-116">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="c212a-117">Application</span><span class="sxs-lookup"><span data-stu-id="c212a-117">Application</span></span> | <span data-ttu-id="c212a-118">Score.Read.All</span><span class="sxs-lookup"><span data-stu-id="c212a-118">Score.Read.All</span></span> | <span data-ttu-id="c212a-119">« Lire le score de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="c212a-119">'Read Threat and Vulnerability Management score'</span></span>
<span data-ttu-id="c212a-120">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="c212a-120">Delegated (work or school account)</span></span> | <span data-ttu-id="c212a-121">Score.Read</span><span class="sxs-lookup"><span data-stu-id="c212a-121">Score.Read</span></span> | <span data-ttu-id="c212a-122">« Lire le score de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="c212a-122">'Read Threat and Vulnerability Management score'</span></span>

## <a name="http-request"></a><span data-ttu-id="c212a-123">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="c212a-123">HTTP request</span></span>

```
GET /api/exposureScore/ByMachineGroups
```

## <a name="request-headers"></a><span data-ttu-id="c212a-124">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="c212a-124">Request headers</span></span>

| <span data-ttu-id="c212a-125">Nom</span><span class="sxs-lookup"><span data-stu-id="c212a-125">Name</span></span>        | <span data-ttu-id="c212a-126">Type</span><span class="sxs-lookup"><span data-stu-id="c212a-126">Type</span></span> | <span data-ttu-id="c212a-127">Description</span><span class="sxs-lookup"><span data-stu-id="c212a-127">Description</span></span>
|:--------------|:-------|:--------------|
| <span data-ttu-id="c212a-128">Autorisation</span><span class="sxs-lookup"><span data-stu-id="c212a-128">Authorization</span></span> | <span data-ttu-id="c212a-129">String</span><span class="sxs-lookup"><span data-stu-id="c212a-129">String</span></span> | <span data-ttu-id="c212a-130">Porteur {token}. **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="c212a-130">Bearer {token}.**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="c212a-131">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="c212a-131">Request body</span></span>

<span data-ttu-id="c212a-132">Vide</span><span class="sxs-lookup"><span data-stu-id="c212a-132">Empty</span></span>

## <a name="response"></a><span data-ttu-id="c212a-133">Réponse</span><span class="sxs-lookup"><span data-stu-id="c212a-133">Response</span></span>

<span data-ttu-id="c212a-134">Si elle réussit, cette méthode renvoie 200 OK, avec une liste de score d’exposition par données de groupe d’appareils dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="c212a-134">If successful, this method returns 200 OK, with a list of exposure score per device group data in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c212a-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="c212a-135">Example</span></span>

### <a name="request"></a><span data-ttu-id="c212a-136">Demande</span><span class="sxs-lookup"><span data-stu-id="c212a-136">Request</span></span>

<span data-ttu-id="c212a-137">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="c212a-137">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/exposureScore/ByMachineGroups
```

### <a name="response"></a><span data-ttu-id="c212a-138">Réponse</span><span class="sxs-lookup"><span data-stu-id="c212a-138">Response</span></span>

<span data-ttu-id="c212a-139">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="c212a-139">Here is an example of the response.</span></span>

```json

{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#ExposureScore",
    "value": [
        {
            "time": "2019-12-03T09:51:28.214338Z",
            "score": 41.38041766305988,
            "rbacGroupName": "GroupOne"
        },
        {
            "time": "2019-12-03T09:51:28.2143399Z",
            "score": 37.403726933165366,
            "rbacGroupName": "GroupTwo"
        }
        ...
    ]
}
```

## <a name="related-topics"></a><span data-ttu-id="c212a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c212a-140">Related topics</span></span>

- [<span data-ttu-id="c212a-141">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="c212a-141">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="c212a-142">Niveau d’exposition & vulnérabilité des menaces</span><span class="sxs-lookup"><span data-stu-id="c212a-142">Threat & Vulnerability exposure score</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-exposure-score)
