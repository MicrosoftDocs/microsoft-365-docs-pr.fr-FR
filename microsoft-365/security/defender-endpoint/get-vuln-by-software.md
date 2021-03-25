---
title: Liste des vulnérabilités par logiciel
description: Récupérez la liste des vulnérabilités dans le logiciel installé.
keywords: api, api de graphique, api pris en charge, obtenir, liste de vulnérabilités, api tvm mdatp
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
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
ms.technology: mde
ms.openlocfilehash: 8f05c1a67c845e7f88cbcb3ee88cf7a664d5a4bf
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166743"
---
# <a name="list-vulnerabilities-by-software"></a><span data-ttu-id="9cd76-104">Liste des vulnérabilités par logiciel</span><span class="sxs-lookup"><span data-stu-id="9cd76-104">List vulnerabilities by software</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9cd76-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9cd76-105">**Applies to:**</span></span>
- [<span data-ttu-id="9cd76-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9cd76-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="9cd76-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9cd76-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="9cd76-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="9cd76-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="9cd76-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9cd76-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="9cd76-110">Récupérez la liste des vulnérabilités dans le logiciel installé.</span><span class="sxs-lookup"><span data-stu-id="9cd76-110">Retrieve a list of vulnerabilities in the installed software.</span></span> 

## <a name="permissions"></a><span data-ttu-id="9cd76-111">Autorisations</span><span class="sxs-lookup"><span data-stu-id="9cd76-111">Permissions</span></span>
<span data-ttu-id="9cd76-112">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="9cd76-112">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="9cd76-113">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9cd76-113">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="9cd76-114">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="9cd76-114">Permission type</span></span> |   <span data-ttu-id="9cd76-115">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9cd76-115">Permission</span></span>  |   <span data-ttu-id="9cd76-116">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="9cd76-116">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="9cd76-117">Application</span><span class="sxs-lookup"><span data-stu-id="9cd76-117">Application</span></span> | <span data-ttu-id="9cd76-118">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="9cd76-118">Software.Read.All</span></span> | <span data-ttu-id="9cd76-119">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="9cd76-119">'Read Threat and Vulnerability Management Software information'</span></span>
<span data-ttu-id="9cd76-120">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="9cd76-120">Delegated (work or school account)</span></span> | <span data-ttu-id="9cd76-121">Software.Read</span><span class="sxs-lookup"><span data-stu-id="9cd76-121">Software.Read</span></span> | <span data-ttu-id="9cd76-122">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="9cd76-122">'Read Threat and Vulnerability Management Software information'</span></span>

## <a name="http-request"></a><span data-ttu-id="9cd76-123">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="9cd76-123">HTTP request</span></span>
```
GET /api/Software/{Id}/vulnerabilities
```

## <a name="request-headers"></a><span data-ttu-id="9cd76-124">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="9cd76-124">Request headers</span></span>

| <span data-ttu-id="9cd76-125">Nom</span><span class="sxs-lookup"><span data-stu-id="9cd76-125">Name</span></span>        | <span data-ttu-id="9cd76-126">Type</span><span class="sxs-lookup"><span data-stu-id="9cd76-126">Type</span></span> | <span data-ttu-id="9cd76-127">Description</span><span class="sxs-lookup"><span data-stu-id="9cd76-127">Description</span></span>
|:--------------|:-------|:--------------|
| <span data-ttu-id="9cd76-128">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9cd76-128">Authorization</span></span> | <span data-ttu-id="9cd76-129">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9cd76-129">String</span></span> | <span data-ttu-id="9cd76-130">Porteur {token}. **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="9cd76-130">Bearer {token}.**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="9cd76-131">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="9cd76-131">Request body</span></span>
<span data-ttu-id="9cd76-132">Vide</span><span class="sxs-lookup"><span data-stu-id="9cd76-132">Empty</span></span>

## <a name="response"></a><span data-ttu-id="9cd76-133">Réponse</span><span class="sxs-lookup"><span data-stu-id="9cd76-133">Response</span></span>
<span data-ttu-id="9cd76-134">Si elle réussit, cette méthode renvoie 200 OK avec une liste de vulnérabilités exposées par le logiciel spécifié.</span><span class="sxs-lookup"><span data-stu-id="9cd76-134">If successful, this method returns 200 OK with a list of vulnerabilities exposed by the specified software.</span></span> 


## <a name="example"></a><span data-ttu-id="9cd76-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="9cd76-135">Example</span></span>

<span data-ttu-id="9cd76-136">**Demande**</span><span class="sxs-lookup"><span data-stu-id="9cd76-136">**Request**</span></span>

<span data-ttu-id="9cd76-137">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="9cd76-137">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/Software/microsoft-_-edge/vulnerabilities 
```

<span data-ttu-id="9cd76-138">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="9cd76-138">**Response**</span></span>

<span data-ttu-id="9cd76-139">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="9cd76-139">Here is an example of the response.</span></span>

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Collection(Analytics.Contracts.PublicAPI.PublicVulnerabilityDto)",
    "value": [
            {
                "id": "CVE-2017-0140",
                "name": "CVE-2017-0140",
                "description": "A security feature bypass vulnerability exists when Microsoft Edge improperly handles requests of different origins. The vulnerability allows Microsoft Edge to bypass Same-Origin Policy (SOP) restrictions, and to allow requests that should otherwise be ignored. An attacker who successfully exploited the vulnerability could force the browser to send data that would otherwise be restricted.In a web-based attack scenario, an attacker could host a specially crafted website that is designed to exploit the vulnerability through Microsoft Edge and then convince a user to view the website. The attacker could also take advantage of compromised websites, and websites that accept or host user-provided content or advertisements. These websites could contain specially crafted content that could exploit the vulnerability.The security update addresses the vulnerability by modifying how affected Microsoft Edge handles different-origin requests.",
                "severity": "Medium",
                "cvssV3": 4.2,
                "exposedMachines": 1,
                "publishedOn": "2017-03-14T00:00:00Z",
                "updatedOn": "2019-10-03T00:03:00Z",
                "publicExploit": false,
                "exploitVerified": false,
                "exploitInKit": false,
                "exploitTypes": [],
                "exploitUris": []
            }
            ...
        ]
}
```

