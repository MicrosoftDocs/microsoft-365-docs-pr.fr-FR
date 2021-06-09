---
title: Obtenir toutes les vulnérabilités
description: Récupère une liste de toutes les vulnérabilités affectant l’organisation
keywords: api, api de graphique, api pris en charge, obtenir, informations de vulnérabilité, api tvm Microsoft Defender pour endpoint
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 4be87e296739020c80babb864c57bc803f10d3e0
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843685"
---
# <a name="list-vulnerabilities"></a><span data-ttu-id="7554a-104">Répertorier des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="7554a-104">List vulnerabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="7554a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7554a-105">**Applies to:**</span></span>
- [<span data-ttu-id="7554a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7554a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="7554a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7554a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="7554a-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="7554a-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="7554a-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7554a-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="7554a-110">Récupère une liste de toutes les vulnérabilités affectant l’organisation.</span><span class="sxs-lookup"><span data-stu-id="7554a-110">Retrieves a list of all the vulnerabilities affecting the organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="7554a-111">Autorisations</span><span class="sxs-lookup"><span data-stu-id="7554a-111">Permissions</span></span>
<span data-ttu-id="7554a-112">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="7554a-112">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="7554a-113">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7554a-113">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="7554a-114">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="7554a-114">Permission type</span></span> |   <span data-ttu-id="7554a-115">Autorisation</span><span class="sxs-lookup"><span data-stu-id="7554a-115">Permission</span></span>  |   <span data-ttu-id="7554a-116">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="7554a-116">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="7554a-117">Application</span><span class="sxs-lookup"><span data-stu-id="7554a-117">Application</span></span> |   <span data-ttu-id="7554a-118">Vulnerability.Read.All</span><span class="sxs-lookup"><span data-stu-id="7554a-118">Vulnerability.Read.All</span></span> |    <span data-ttu-id="7554a-119">« Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="7554a-119">'Read Threat and Vulnerability Management vulnerability information'</span></span>
<span data-ttu-id="7554a-120">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="7554a-120">Delegated (work or school account)</span></span> | <span data-ttu-id="7554a-121">Vulnerability.Read</span><span class="sxs-lookup"><span data-stu-id="7554a-121">Vulnerability.Read</span></span> |   <span data-ttu-id="7554a-122">« Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="7554a-122">'Read Threat and Vulnerability Management vulnerability information'</span></span>

## <a name="http-request"></a><span data-ttu-id="7554a-123">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="7554a-123">HTTP request</span></span>
```
GET /api/vulnerabilities
```

## <a name="request-headers"></a><span data-ttu-id="7554a-124">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="7554a-124">Request headers</span></span>

<span data-ttu-id="7554a-125">Nom</span><span class="sxs-lookup"><span data-stu-id="7554a-125">Name</span></span> | <span data-ttu-id="7554a-126">Type</span><span class="sxs-lookup"><span data-stu-id="7554a-126">Type</span></span> | <span data-ttu-id="7554a-127">Description</span><span class="sxs-lookup"><span data-stu-id="7554a-127">Description</span></span>
:---|:---|:---
<span data-ttu-id="7554a-128">Autorisation</span><span class="sxs-lookup"><span data-stu-id="7554a-128">Authorization</span></span> | <span data-ttu-id="7554a-129">String</span><span class="sxs-lookup"><span data-stu-id="7554a-129">String</span></span> | <span data-ttu-id="7554a-130">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="7554a-130">Bearer {token}.</span></span> <span data-ttu-id="7554a-131">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="7554a-131">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="7554a-132">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="7554a-132">Request body</span></span>
<span data-ttu-id="7554a-133">Vide</span><span class="sxs-lookup"><span data-stu-id="7554a-133">Empty</span></span>

## <a name="response"></a><span data-ttu-id="7554a-134">Réponse</span><span class="sxs-lookup"><span data-stu-id="7554a-134">Response</span></span>
<span data-ttu-id="7554a-135">Si elle réussit, cette méthode renvoie 200 OK avec la liste des vulnérabilités dans le corps.</span><span class="sxs-lookup"><span data-stu-id="7554a-135">If successful, this method returns 200 OK with the list of vulnerabilities in the body.</span></span>


## <a name="example"></a><span data-ttu-id="7554a-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="7554a-136">Example</span></span>

<span data-ttu-id="7554a-137">**Demande**</span><span class="sxs-lookup"><span data-stu-id="7554a-137">**Request**</span></span>

<span data-ttu-id="7554a-138">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="7554a-138">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/Vulnerabilities
```

<span data-ttu-id="7554a-139">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="7554a-139">**Response**</span></span>

<span data-ttu-id="7554a-140">Voici un exemple de la réponse.</span><span class="sxs-lookup"><span data-stu-id="7554a-140">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Vulnerabilities",
    "value": [
        {
            "id": "CVE-2019-0608",
            "name": "CVE-2019-0608",
            "description": "A spoofing vulnerability exists when Microsoft Browsers does not properly parse HTTP content. An attacker who successfully exploited this vulnerability could impersonate a user request by crafting HTTP queries. The specially crafted website could either spoof content or serve as a pivot to chain an attack with other vulnerabilities in web services.To exploit the vulnerability, the user must click a specially crafted URL. In an email attack scenario, an attacker could send an email message containing the specially crafted URL to the user in an attempt to convince the user to click it.In a web-based attack scenario, an attacker could host a specially crafted website designed to appear as a legitimate website to the user. However, the attacker would have no way to force the user to visit the specially crafted website. The attacker would have to convince the user to visit the specially crafted website, typically by way of enticement in an email or instant message, and then convince the user to interact with content on the website.The update addresses the vulnerability by correcting how Microsoft Browsers parses HTTP responses.",
            "severity": "Medium",
            "cvssV3": 4.3,
            "exposedMachines": 4,
            "publishedOn": "2019-10-08T00:00:00Z",
            "updatedOn": "2019-12-16T16:20:00Z",
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

## <a name="see-also"></a><span data-ttu-id="7554a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7554a-141">See also</span></span>
- [<span data-ttu-id="7554a-142">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="7554a-142">Risk-based Threat & Vulnerability Management</span></span>](/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="7554a-143">Vulnérabilités de votre organisation</span><span class="sxs-lookup"><span data-stu-id="7554a-143">Vulnerabilities in your organization</span></span>](/microsoft-365/security/defender-endpoint/tvm-weaknesses)
