---
title: Obtenir les ko manquants par ID logiciel
description: Récupère les mises à jour de sécurité manquantes par ID logiciel
keywords: api, api de graphique, api pris en charge, obtenir, liste, fichier, informations, ID logiciel, api de gestion des menaces & vulnérabilité, api tvm mdatp
search.product: eADQiWindows 10XVcnh
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: e5d84a3eadab85713779dd70848bc11d27484dcc
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51499391"
---
# <a name="get-missing-kbs-by-software-id"></a><span data-ttu-id="fc359-104">Obtenir les ko manquants par ID logiciel</span><span class="sxs-lookup"><span data-stu-id="fc359-104">Get missing KBs by software ID</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="fc359-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="fc359-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="fc359-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="fc359-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="fc359-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="fc359-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="fc359-108">Récupère les ko manquants (mises à jour de sécurité) par ID logiciel</span><span class="sxs-lookup"><span data-stu-id="fc359-108">Retrieves missing KBs (security updates) by software ID</span></span>

## <a name="permissions"></a><span data-ttu-id="fc359-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="fc359-109">Permissions</span></span>

<span data-ttu-id="fc359-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="fc359-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="fc359-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="fc359-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="fc359-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="fc359-112">Permission type</span></span> |   <span data-ttu-id="fc359-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="fc359-113">Permission</span></span>   |   <span data-ttu-id="fc359-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="fc359-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="fc359-115">Application</span><span class="sxs-lookup"><span data-stu-id="fc359-115">Application</span></span> |<span data-ttu-id="fc359-116">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="fc359-116">Software.Read.All</span></span> |   <span data-ttu-id="fc359-117">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="fc359-117">'Read Threat and Vulnerability Management Software information'</span></span>
<span data-ttu-id="fc359-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="fc359-118">Delegated (work or school account)</span></span> | <span data-ttu-id="fc359-119">Software.Read</span><span class="sxs-lookup"><span data-stu-id="fc359-119">Software.Read</span></span> |   <span data-ttu-id="fc359-120">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="fc359-120">'Read Threat and Vulnerability Management Software information'</span></span>

## <a name="http-request"></a><span data-ttu-id="fc359-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="fc359-121">HTTP request</span></span>

```
GET /api/Software/{Id}/getmissingkbs
```

## <a name="request-header"></a><span data-ttu-id="fc359-122">En-tête de requête</span><span class="sxs-lookup"><span data-stu-id="fc359-122">Request header</span></span>

<span data-ttu-id="fc359-123">Nom</span><span class="sxs-lookup"><span data-stu-id="fc359-123">Name</span></span> | <span data-ttu-id="fc359-124">Type</span><span class="sxs-lookup"><span data-stu-id="fc359-124">Type</span></span> | <span data-ttu-id="fc359-125">Description</span><span class="sxs-lookup"><span data-stu-id="fc359-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="fc359-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="fc359-126">Authorization</span></span> | <span data-ttu-id="fc359-127">String</span><span class="sxs-lookup"><span data-stu-id="fc359-127">String</span></span> | <span data-ttu-id="fc359-128">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="fc359-128">Bearer {token}.</span></span> <span data-ttu-id="fc359-129">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="fc359-129">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="fc359-130">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="fc359-130">Request body</span></span>

<span data-ttu-id="fc359-131">Vide</span><span class="sxs-lookup"><span data-stu-id="fc359-131">Empty</span></span>

## <a name="response"></a><span data-ttu-id="fc359-132">Réponse</span><span class="sxs-lookup"><span data-stu-id="fc359-132">Response</span></span>

<span data-ttu-id="fc359-133">Si elle réussit, cette méthode renvoie 200 OK, avec les données kb du logiciel spécifié manquantes dans le corps.</span><span class="sxs-lookup"><span data-stu-id="fc359-133">If successful, this method returns 200 OK, with the specified software missing kb data in the body.</span></span>

## <a name="example"></a><span data-ttu-id="fc359-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc359-134">Example</span></span>

### <a name="request"></a><span data-ttu-id="fc359-135">Demande</span><span class="sxs-lookup"><span data-stu-id="fc359-135">Request</span></span>

<span data-ttu-id="fc359-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="fc359-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/Software/microsoft-_-edge/getmissingkbs
```

### <a name="response"></a><span data-ttu-id="fc359-137">Réponse</span><span class="sxs-lookup"><span data-stu-id="fc359-137">Response</span></span>

<span data-ttu-id="fc359-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="fc359-138">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Collection(microsoft.windowsDefenderATP.api.PublicProductFixDto)",
    "value": [
         {
            "id": "4540673",
            "name": "March 2020 Security Updates",
            "productsNames": [
                "edge"
            ],
            "url": "https://catalog.update.microsoft.com/v7/site/Search.aspx?q=KB4540673",
            "machineMissedOn": 240,
            "cveAddressed": 14
         },
         ...
        ]
}
```

## <a name="related-topics"></a><span data-ttu-id="fc359-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc359-139">Related topics</span></span>

- [<span data-ttu-id="fc359-140">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="fc359-140">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="fc359-141">Inventaire des logiciels de vulnérabilité & menace</span><span class="sxs-lookup"><span data-stu-id="fc359-141">Threat & Vulnerability software inventory</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-software-inventory)
