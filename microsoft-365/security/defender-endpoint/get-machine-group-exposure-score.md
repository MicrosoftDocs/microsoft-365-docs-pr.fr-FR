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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: a7f343db64174fe3c48eaf8b584b03b53921edcb
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843613"
---
# <a name="list-exposure-score-by-device-group"></a><span data-ttu-id="093df-104">Liste du score d’exposition par groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="093df-104">List exposure score by device group</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="093df-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="093df-105">**Applies to:**</span></span>
- [<span data-ttu-id="093df-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="093df-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="093df-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="093df-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="093df-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="093df-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="093df-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="093df-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="093df-110">Récupère une collection d’alertes liées à une adresse de domaine donnée.</span><span class="sxs-lookup"><span data-stu-id="093df-110">Retrieves a collection of alerts related to a given domain address.</span></span>

## <a name="permissions"></a><span data-ttu-id="093df-111">Autorisations</span><span class="sxs-lookup"><span data-stu-id="093df-111">Permissions</span></span>

<span data-ttu-id="093df-112">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="093df-112">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="093df-113">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="093df-113">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="093df-114">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="093df-114">Permission type</span></span> |   <span data-ttu-id="093df-115">Autorisation</span><span class="sxs-lookup"><span data-stu-id="093df-115">Permission</span></span>  |   <span data-ttu-id="093df-116">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="093df-116">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="093df-117">Application</span><span class="sxs-lookup"><span data-stu-id="093df-117">Application</span></span> | <span data-ttu-id="093df-118">Score.Read.All</span><span class="sxs-lookup"><span data-stu-id="093df-118">Score.Read.All</span></span> | <span data-ttu-id="093df-119">« Lire le score de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="093df-119">'Read Threat and Vulnerability Management score'</span></span>
<span data-ttu-id="093df-120">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="093df-120">Delegated (work or school account)</span></span> | <span data-ttu-id="093df-121">Score.Read</span><span class="sxs-lookup"><span data-stu-id="093df-121">Score.Read</span></span> | <span data-ttu-id="093df-122">« Lire le score de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="093df-122">'Read Threat and Vulnerability Management score'</span></span>

## <a name="http-request"></a><span data-ttu-id="093df-123">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="093df-123">HTTP request</span></span>

```
GET /api/exposureScore/ByMachineGroups
```

## <a name="request-headers"></a><span data-ttu-id="093df-124">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="093df-124">Request headers</span></span>

| <span data-ttu-id="093df-125">Nom</span><span class="sxs-lookup"><span data-stu-id="093df-125">Name</span></span>        | <span data-ttu-id="093df-126">Type</span><span class="sxs-lookup"><span data-stu-id="093df-126">Type</span></span> | <span data-ttu-id="093df-127">Description</span><span class="sxs-lookup"><span data-stu-id="093df-127">Description</span></span>
|:--------------|:-------|:--------------|
| <span data-ttu-id="093df-128">Autorisation</span><span class="sxs-lookup"><span data-stu-id="093df-128">Authorization</span></span> | <span data-ttu-id="093df-129">String</span><span class="sxs-lookup"><span data-stu-id="093df-129">String</span></span> | <span data-ttu-id="093df-130">Porteur {token}. **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="093df-130">Bearer {token}.**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="093df-131">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="093df-131">Request body</span></span>

<span data-ttu-id="093df-132">Vide</span><span class="sxs-lookup"><span data-stu-id="093df-132">Empty</span></span>

## <a name="response"></a><span data-ttu-id="093df-133">Réponse</span><span class="sxs-lookup"><span data-stu-id="093df-133">Response</span></span>

<span data-ttu-id="093df-134">Si elle réussit, cette méthode renvoie 200 OK, avec une liste de score d’exposition par groupe d’appareils dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="093df-134">If successful, this method returns 200 OK, with a list of exposure score per device group data in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="093df-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="093df-135">Example</span></span>

### <a name="request"></a><span data-ttu-id="093df-136">Demande</span><span class="sxs-lookup"><span data-stu-id="093df-136">Request</span></span>

<span data-ttu-id="093df-137">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="093df-137">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/exposureScore/ByMachineGroups
```

### <a name="response"></a><span data-ttu-id="093df-138">Réponse</span><span class="sxs-lookup"><span data-stu-id="093df-138">Response</span></span>

<span data-ttu-id="093df-139">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="093df-139">Here is an example of the response.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="093df-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="093df-140">Related topics</span></span>

- [<span data-ttu-id="093df-141">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="093df-141">Risk-based Threat & Vulnerability Management</span></span>](/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="093df-142">Score d& exposition des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="093df-142">Threat & Vulnerability exposure score</span></span>](/microsoft-365/security/defender-endpoint/tvm-exposure-score)
