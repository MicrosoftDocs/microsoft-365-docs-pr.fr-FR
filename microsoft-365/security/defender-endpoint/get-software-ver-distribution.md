---
title: Répertorier la distribution de versions du logiciel
description: Récupère la liste de la distribution des versions logicielles de votre organisation
keywords: api, api de graphique, api pris en charge, obtenir, distribution de version de logiciel, api tvm Microsoft Defender pour endpoint
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
ms.openlocfilehash: 7ac7fdf4c38846e2e8be614567ddb87a98e3a96c
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772124"
---
# <a name="list-software-version-distribution"></a><span data-ttu-id="e122d-104">Répertorier la distribution de versions du logiciel</span><span class="sxs-lookup"><span data-stu-id="e122d-104">List software version distribution</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e122d-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="e122d-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="e122d-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e122d-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e122d-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e122d-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="e122d-108">Extrait la liste de la distribution des versions des logiciels de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e122d-108">Retrieves a list of your organization's software version distribution.</span></span> 

## <a name="permissions"></a><span data-ttu-id="e122d-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="e122d-109">Permissions</span></span>
<span data-ttu-id="e122d-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="e122d-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="e122d-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e122d-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="e122d-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="e122d-112">Permission type</span></span> |   <span data-ttu-id="e122d-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e122d-113">Permission</span></span>  |   <span data-ttu-id="e122d-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="e122d-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="e122d-115">Application</span><span class="sxs-lookup"><span data-stu-id="e122d-115">Application</span></span> | <span data-ttu-id="e122d-116">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="e122d-116">Software.Read.All</span></span> | <span data-ttu-id="e122d-117">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="e122d-117">'Read Threat and Vulnerability Management Software information'</span></span>
<span data-ttu-id="e122d-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="e122d-118">Delegated (work or school account)</span></span> | <span data-ttu-id="e122d-119">Software.Read</span><span class="sxs-lookup"><span data-stu-id="e122d-119">Software.Read</span></span> | <span data-ttu-id="e122d-120">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="e122d-120">'Read Threat and Vulnerability Management Software information'</span></span>

## <a name="http-request"></a><span data-ttu-id="e122d-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="e122d-121">HTTP request</span></span>
```
GET /api/Software/{Id}/distributions
```

## <a name="request-headers"></a><span data-ttu-id="e122d-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="e122d-122">Request headers</span></span>

| <span data-ttu-id="e122d-123">Nom</span><span class="sxs-lookup"><span data-stu-id="e122d-123">Name</span></span>        | <span data-ttu-id="e122d-124">Type</span><span class="sxs-lookup"><span data-stu-id="e122d-124">Type</span></span> | <span data-ttu-id="e122d-125">Description</span><span class="sxs-lookup"><span data-stu-id="e122d-125">Description</span></span>
|:--------------|:-------|:--------------|
| <span data-ttu-id="e122d-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e122d-126">Authorization</span></span> | <span data-ttu-id="e122d-127">String</span><span class="sxs-lookup"><span data-stu-id="e122d-127">String</span></span> | <span data-ttu-id="e122d-128">Porteur {token}. **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="e122d-128">Bearer {token}.**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="e122d-129">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="e122d-129">Request body</span></span>
<span data-ttu-id="e122d-130">Vide</span><span class="sxs-lookup"><span data-stu-id="e122d-130">Empty</span></span>

## <a name="response"></a><span data-ttu-id="e122d-131">Réponse</span><span class="sxs-lookup"><span data-stu-id="e122d-131">Response</span></span>
<span data-ttu-id="e122d-132">Si elle réussit, cette méthode renvoie 200 OK avec une liste de données de distribution de logiciels dans le corps.</span><span class="sxs-lookup"><span data-stu-id="e122d-132">If successful, this method returns 200 OK with a list of software distributions data in the body.</span></span> 


## <a name="example"></a><span data-ttu-id="e122d-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="e122d-133">Example</span></span>

<span data-ttu-id="e122d-134">**Demande**</span><span class="sxs-lookup"><span data-stu-id="e122d-134">**Request**</span></span>

<span data-ttu-id="e122d-135">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="e122d-135">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/Software/microsoft-_-edge/distributions
```

<span data-ttu-id="e122d-136">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="e122d-136">**Response**</span></span>

<span data-ttu-id="e122d-137">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="e122d-137">Here is an example of the response.</span></span>

```json

{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Distributions",
    "value": [
        {
            "version": "11.0.17134.1039",
            "installations": 1,
            "vulnerabilities": 11
        },
        {
            "version": "11.0.18363.535",
            "installations": 750,
            "vulnerabilities": 0
        }
        ...
    ]
}
```

## <a name="related-topics"></a><span data-ttu-id="e122d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e122d-138">Related topics</span></span>
- [<span data-ttu-id="e122d-139">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="e122d-139">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="e122d-140">Inventaire des logiciels de vulnérabilité & menace</span><span class="sxs-lookup"><span data-stu-id="e122d-140">Threat & Vulnerability software inventory</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-software-inventory)
