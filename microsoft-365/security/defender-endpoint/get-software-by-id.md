---
title: Obtenir le logiciel par ID
description: Récupère une liste des scores d’exposition par groupe d’appareils.
keywords: api, api de graphique, api pris en charge, obtenir, logiciel, api tvm Microsoft Defender pour endpoint
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
ms.openlocfilehash: d9a7d97cea96f919f1ec7cd1e37e7a8f27042c79
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52845089"
---
# <a name="get-software-by-id"></a><span data-ttu-id="d90f1-104">Obtenir le logiciel par ID</span><span class="sxs-lookup"><span data-stu-id="d90f1-104">Get software by Id</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="d90f1-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="d90f1-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="d90f1-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d90f1-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d90f1-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d90f1-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="d90f1-108">Récupère les détails logiciels par ID.</span><span class="sxs-lookup"><span data-stu-id="d90f1-108">Retrieves software details by ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="d90f1-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="d90f1-109">Permissions</span></span>
<span data-ttu-id="d90f1-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="d90f1-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="d90f1-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d90f1-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="d90f1-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="d90f1-112">Permission type</span></span> |   <span data-ttu-id="d90f1-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="d90f1-113">Permission</span></span>  |   <span data-ttu-id="d90f1-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="d90f1-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="d90f1-115">Application</span><span class="sxs-lookup"><span data-stu-id="d90f1-115">Application</span></span> | <span data-ttu-id="d90f1-116">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="d90f1-116">Software.Read.All</span></span> | <span data-ttu-id="d90f1-117">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="d90f1-117">'Read Threat and Vulnerability Management Software information'</span></span>
<span data-ttu-id="d90f1-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="d90f1-118">Delegated (work or school account)</span></span> | <span data-ttu-id="d90f1-119">Software.Read</span><span class="sxs-lookup"><span data-stu-id="d90f1-119">Software.Read</span></span> | <span data-ttu-id="d90f1-120">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="d90f1-120">'Read Threat and Vulnerability Management Software information'</span></span>

## <a name="http-request"></a><span data-ttu-id="d90f1-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="d90f1-121">HTTP request</span></span>
```
GET /api/Software/{Id}
```

## <a name="request-headers"></a><span data-ttu-id="d90f1-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="d90f1-122">Request headers</span></span>

| <span data-ttu-id="d90f1-123">Nom</span><span class="sxs-lookup"><span data-stu-id="d90f1-123">Name</span></span>        | <span data-ttu-id="d90f1-124">Type</span><span class="sxs-lookup"><span data-stu-id="d90f1-124">Type</span></span> | <span data-ttu-id="d90f1-125">Description</span><span class="sxs-lookup"><span data-stu-id="d90f1-125">Description</span></span>
|:--------------|:-------|:--------------|
| <span data-ttu-id="d90f1-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="d90f1-126">Authorization</span></span> | <span data-ttu-id="d90f1-127">String</span><span class="sxs-lookup"><span data-stu-id="d90f1-127">String</span></span> | <span data-ttu-id="d90f1-128">Porteur {token}. **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="d90f1-128">Bearer {token}.**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="d90f1-129">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="d90f1-129">Request body</span></span>
<span data-ttu-id="d90f1-130">Vide</span><span class="sxs-lookup"><span data-stu-id="d90f1-130">Empty</span></span>

## <a name="response"></a><span data-ttu-id="d90f1-131">Réponse</span><span class="sxs-lookup"><span data-stu-id="d90f1-131">Response</span></span>
<span data-ttu-id="d90f1-132">Si elle réussit, cette méthode renvoie 200 OK avec les données logicielles spécifiées dans le corps.</span><span class="sxs-lookup"><span data-stu-id="d90f1-132">If successful, this method returns 200 OK with the specified software data in the body.</span></span> 


## <a name="example"></a><span data-ttu-id="d90f1-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="d90f1-133">Example</span></span>

<span data-ttu-id="d90f1-134">**Demande**</span><span class="sxs-lookup"><span data-stu-id="d90f1-134">**Request**</span></span>

<span data-ttu-id="d90f1-135">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="d90f1-135">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/Software/microsoft-_-edge
```

<span data-ttu-id="d90f1-136">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="d90f1-136">**Response**</span></span>

<span data-ttu-id="d90f1-137">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="d90f1-137">Here is an example of the response.</span></span>

```json

{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Software/$entity",
    "id": "microsoft-_-edge",
    "name": "edge",
    "vendor": "microsoft",
    "weaknesses": 467,
    "publicExploit": true,
    "activeAlert": false,
    "exposedMachines": 172,
    "impactScore": 2.39947438
}
```

## <a name="related-topics"></a><span data-ttu-id="d90f1-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d90f1-138">Related topics</span></span>
- [<span data-ttu-id="d90f1-139">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="d90f1-139">Risk-based Threat & Vulnerability Management</span></span>](/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="d90f1-140">Inventaire des logiciels de vulnérabilité & menace</span><span class="sxs-lookup"><span data-stu-id="d90f1-140">Threat & Vulnerability software inventory</span></span>](/microsoft-365/security/defender-endpoint/tvm-software-inventory)
