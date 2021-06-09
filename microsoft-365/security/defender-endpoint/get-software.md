---
title: Répertorier les logiciels
description: Récupère une liste d’inventaire logiciel
keywords: api, api de graphique, api pris en charge, obtenir, liste, fichier, informations, inventaire logiciel, api & gestion des vulnérabilités menace, Api Tvm Microsoft Defender pour Endpoint
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
ms.openlocfilehash: 2b7375f04094cdb56b0801adf2c1c0b7a8ab3098
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844273"
---
# <a name="list-software-inventory-api"></a><span data-ttu-id="e0730-104">API d’inventaire de logiciels de liste</span><span class="sxs-lookup"><span data-stu-id="e0730-104">List software inventory API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e0730-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="e0730-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="e0730-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e0730-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e0730-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e0730-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="e0730-108">Récupère l’inventaire logiciel de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="e0730-108">Retrieves the organization software inventory.</span></span>

## <a name="permissions"></a><span data-ttu-id="e0730-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="e0730-109">Permissions</span></span>
<span data-ttu-id="e0730-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="e0730-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="e0730-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e0730-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="e0730-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="e0730-112">Permission type</span></span> |   <span data-ttu-id="e0730-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e0730-113">Permission</span></span>  |   <span data-ttu-id="e0730-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="e0730-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="e0730-115">Application</span><span class="sxs-lookup"><span data-stu-id="e0730-115">Application</span></span> |<span data-ttu-id="e0730-116">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="e0730-116">Software.Read.All</span></span> |    <span data-ttu-id="e0730-117">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="e0730-117">'Read Threat and Vulnerability Management Software information'</span></span>
<span data-ttu-id="e0730-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="e0730-118">Delegated (work or school account)</span></span> | <span data-ttu-id="e0730-119">Software.Read</span><span class="sxs-lookup"><span data-stu-id="e0730-119">Software.Read</span></span> |    <span data-ttu-id="e0730-120">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="e0730-120">'Read Threat and Vulnerability Management Software information'</span></span>

## <a name="http-request"></a><span data-ttu-id="e0730-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="e0730-121">HTTP request</span></span>
```
GET /api/Software
```

## <a name="request-headers"></a><span data-ttu-id="e0730-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="e0730-122">Request headers</span></span>

<span data-ttu-id="e0730-123">Nom</span><span class="sxs-lookup"><span data-stu-id="e0730-123">Name</span></span> | <span data-ttu-id="e0730-124">Type</span><span class="sxs-lookup"><span data-stu-id="e0730-124">Type</span></span> | <span data-ttu-id="e0730-125">Description</span><span class="sxs-lookup"><span data-stu-id="e0730-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="e0730-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e0730-126">Authorization</span></span> | <span data-ttu-id="e0730-127">String</span><span class="sxs-lookup"><span data-stu-id="e0730-127">String</span></span> | <span data-ttu-id="e0730-128">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="e0730-128">Bearer {token}.</span></span> <span data-ttu-id="e0730-129">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="e0730-129">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="e0730-130">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="e0730-130">Request body</span></span>
<span data-ttu-id="e0730-131">Vide</span><span class="sxs-lookup"><span data-stu-id="e0730-131">Empty</span></span>

## <a name="response"></a><span data-ttu-id="e0730-132">Réponse</span><span class="sxs-lookup"><span data-stu-id="e0730-132">Response</span></span>
<span data-ttu-id="e0730-133">Si elle réussit, cette méthode renvoie 200 OK avec l’inventaire logiciel dans le corps.</span><span class="sxs-lookup"><span data-stu-id="e0730-133">If successful, this method returns 200 OK with the software inventory in the body.</span></span>


## <a name="example"></a><span data-ttu-id="e0730-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0730-134">Example</span></span>

<span data-ttu-id="e0730-135">**Demande**</span><span class="sxs-lookup"><span data-stu-id="e0730-135">**Request**</span></span>

<span data-ttu-id="e0730-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="e0730-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/Software
```

<span data-ttu-id="e0730-137">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="e0730-137">**Response**</span></span>

<span data-ttu-id="e0730-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="e0730-138">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Software",
    "value": [
            {
                "id": "microsoft-_-edge",
                "name": "edge",
                "vendor": "microsoft",
                "weaknesses": 467,
                "publicExploit": true,
                "activeAlert": false,
                "exposedMachines": 172,
                "impactScore": 2.39947438
            }
            ...
        ]
}
```

## <a name="related-topics"></a><span data-ttu-id="e0730-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0730-139">Related topics</span></span>
- [<span data-ttu-id="e0730-140">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="e0730-140">Risk-based Threat & Vulnerability Management</span></span>](/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="e0730-141">Inventaire des logiciels de vulnérabilité & menace</span><span class="sxs-lookup"><span data-stu-id="e0730-141">Threat & Vulnerability software inventory</span></span>](/microsoft-365/security/defender-endpoint/tvm-software-inventory)
