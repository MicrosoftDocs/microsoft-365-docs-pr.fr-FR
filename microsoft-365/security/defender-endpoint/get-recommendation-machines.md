---
title: Liste des appareils par recommandation
description: Extrait la liste des appareils associés à la recommandation de sécurité.
keywords: api, api de graphique, api pris en charge, obtenir, recommandation de sécurité pour les appareils vulnérables, Gestion des menaces et des vulnérabilités, Gestion des menaces et des vulnérabilités api
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
ms.openlocfilehash: 6c762a15051444ec950e92998317db4f7e51783c
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771812"
---
# <a name="list-devices-by-recommendation"></a><span data-ttu-id="233ae-104">Liste des appareils par recommandation</span><span class="sxs-lookup"><span data-stu-id="233ae-104">List devices by recommendation</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="233ae-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="233ae-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

> <span data-ttu-id="233ae-106">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="233ae-106">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="233ae-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="233ae-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="233ae-108">Extrait la liste des appareils associés à la recommandation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="233ae-108">Retrieves a list of devices associated with the security recommendation.</span></span>

## <a name="permissions"></a><span data-ttu-id="233ae-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="233ae-109">Permissions</span></span>
<span data-ttu-id="233ae-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="233ae-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="233ae-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="233ae-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="233ae-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="233ae-112">Permission type</span></span> |   <span data-ttu-id="233ae-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="233ae-113">Permission</span></span>  |   <span data-ttu-id="233ae-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="233ae-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="233ae-115">Application</span><span class="sxs-lookup"><span data-stu-id="233ae-115">Application</span></span> |   <span data-ttu-id="233ae-116">SecurityRecommendation.Read.All</span><span class="sxs-lookup"><span data-stu-id="233ae-116">SecurityRecommendation.Read.All</span></span> |   <span data-ttu-id="233ae-117">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="233ae-117">'Read Threat and Vulnerability Management security recommendation information'</span></span>
<span data-ttu-id="233ae-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="233ae-118">Delegated (work or school account)</span></span> | <span data-ttu-id="233ae-119">SecurityRecommendation.Read</span><span class="sxs-lookup"><span data-stu-id="233ae-119">SecurityRecommendation.Read</span></span> |  <span data-ttu-id="233ae-120">« Lire les informations de recommandation sur la sécurité de la gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="233ae-120">'Read Threat and Vulnerability Management security recommendation information'</span></span>

## <a name="http-request"></a><span data-ttu-id="233ae-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="233ae-121">HTTP request</span></span>
```
GET /api/recommendations/{id}/machineReferences
```

## <a name="request-headers"></a><span data-ttu-id="233ae-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="233ae-122">Request headers</span></span>

<span data-ttu-id="233ae-123">Nom</span><span class="sxs-lookup"><span data-stu-id="233ae-123">Name</span></span> | <span data-ttu-id="233ae-124">Type</span><span class="sxs-lookup"><span data-stu-id="233ae-124">Type</span></span> | <span data-ttu-id="233ae-125">Description</span><span class="sxs-lookup"><span data-stu-id="233ae-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="233ae-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="233ae-126">Authorization</span></span> | <span data-ttu-id="233ae-127">String</span><span class="sxs-lookup"><span data-stu-id="233ae-127">String</span></span> | <span data-ttu-id="233ae-128">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="233ae-128">Bearer {token}.</span></span> <span data-ttu-id="233ae-129">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="233ae-129">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="233ae-130">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="233ae-130">Request body</span></span>
<span data-ttu-id="233ae-131">Vide</span><span class="sxs-lookup"><span data-stu-id="233ae-131">Empty</span></span>

## <a name="response"></a><span data-ttu-id="233ae-132">Réponse</span><span class="sxs-lookup"><span data-stu-id="233ae-132">Response</span></span>
<span data-ttu-id="233ae-133">Si elle réussit, cette méthode renvoie 200 OK avec la liste des appareils associés à la recommandation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="233ae-133">If successful, this method returns 200 OK with the list of devices associated with the security recommendation.</span></span>


## <a name="example"></a><span data-ttu-id="233ae-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="233ae-134">Example</span></span>

<span data-ttu-id="233ae-135">**Demande**</span><span class="sxs-lookup"><span data-stu-id="233ae-135">**Request**</span></span>

<span data-ttu-id="233ae-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="233ae-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/recommendations/va-_-google-_-chrome/machineReferences
```

<span data-ttu-id="233ae-137">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="233ae-137">**Response**</span></span>

<span data-ttu-id="233ae-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="233ae-138">Here is an example of the response.</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#MachineReferences",
    "value": [
        {
            "id": "e058770379bc199a9c179ce52a23e16fd44fd2ee",
            "computerDnsName": "niw_pc",
            "osPlatform": "Windows10",
            "rbacGroupName": "GroupTwo"
        }
        ...
    ]
}
```

## <a name="related-topics"></a><span data-ttu-id="233ae-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="233ae-139">Related topics</span></span>
- [<span data-ttu-id="233ae-140">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="233ae-140">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="233ae-141">Recommandations & sécurité des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="233ae-141">Threat & Vulnerability security recommendation</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-security-recommendation)
