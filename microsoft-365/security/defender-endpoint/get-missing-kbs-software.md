---
title: Obtenir les ko manquants par ID logiciel
description: Récupère les mises à jour de sécurité manquantes par ID logiciel
keywords: api, api de graphique, api pris en charge, obtenir, liste, fichier, informations, ID logiciel, api de gestion des menaces & vulnérabilité, api tvm mdatp
search.product: eADQiWindows 10XVcnh
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: ellevin
author: levinec
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: c90854b043674a61c4996456c9d718b3c25afd1c
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51197784"
---
# <a name="get-missing-kbs-by-software-id"></a><span data-ttu-id="57146-104">Obtenir les ko manquants par ID logiciel</span><span class="sxs-lookup"><span data-stu-id="57146-104">Get missing KBs by software ID</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="57146-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="57146-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="57146-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="57146-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="57146-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="57146-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="57146-108">Récupère les ko manquants (mises à jour de sécurité) par ID logiciel</span><span class="sxs-lookup"><span data-stu-id="57146-108">Retrieves missing KBs (security updates) by software ID</span></span>

## <a name="permissions"></a><span data-ttu-id="57146-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="57146-109">Permissions</span></span>

<span data-ttu-id="57146-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="57146-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="57146-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="57146-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="57146-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="57146-112">Permission type</span></span> |   <span data-ttu-id="57146-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="57146-113">Permission</span></span>   |   <span data-ttu-id="57146-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="57146-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="57146-115">Application</span><span class="sxs-lookup"><span data-stu-id="57146-115">Application</span></span> |<span data-ttu-id="57146-116">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="57146-116">Software.Read.All</span></span> |   <span data-ttu-id="57146-117">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="57146-117">'Read Threat and Vulnerability Management Software information'</span></span>
<span data-ttu-id="57146-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="57146-118">Delegated (work or school account)</span></span> | <span data-ttu-id="57146-119">Software.Read</span><span class="sxs-lookup"><span data-stu-id="57146-119">Software.Read</span></span> |   <span data-ttu-id="57146-120">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="57146-120">'Read Threat and Vulnerability Management Software information'</span></span>

## <a name="http-request"></a><span data-ttu-id="57146-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="57146-121">HTTP request</span></span>

```
GET /api/Software/{Id}/getmissingkbs
```

## <a name="request-header"></a><span data-ttu-id="57146-122">En-tête de demande</span><span class="sxs-lookup"><span data-stu-id="57146-122">Request header</span></span>

<span data-ttu-id="57146-123">Nom</span><span class="sxs-lookup"><span data-stu-id="57146-123">Name</span></span> | <span data-ttu-id="57146-124">Type</span><span class="sxs-lookup"><span data-stu-id="57146-124">Type</span></span> | <span data-ttu-id="57146-125">Description</span><span class="sxs-lookup"><span data-stu-id="57146-125">Description</span></span>
:---|:---|:---
<span data-ttu-id="57146-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="57146-126">Authorization</span></span> | <span data-ttu-id="57146-127">Chaîne</span><span class="sxs-lookup"><span data-stu-id="57146-127">String</span></span> | <span data-ttu-id="57146-128">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="57146-128">Bearer {token}.</span></span> <span data-ttu-id="57146-129">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="57146-129">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="57146-130">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="57146-130">Request body</span></span>

<span data-ttu-id="57146-131">Vide</span><span class="sxs-lookup"><span data-stu-id="57146-131">Empty</span></span>

## <a name="response"></a><span data-ttu-id="57146-132">Réponse</span><span class="sxs-lookup"><span data-stu-id="57146-132">Response</span></span>

<span data-ttu-id="57146-133">Si elle réussit, cette méthode renvoie 200 OK, avec les données kb du logiciel spécifié manquantes dans le corps.</span><span class="sxs-lookup"><span data-stu-id="57146-133">If successful, this method returns 200 OK, with the specified software missing kb data in the body.</span></span>

## <a name="example"></a><span data-ttu-id="57146-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="57146-134">Example</span></span>

### <a name="request"></a><span data-ttu-id="57146-135">Demande</span><span class="sxs-lookup"><span data-stu-id="57146-135">Request</span></span>

<span data-ttu-id="57146-136">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="57146-136">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/Software/microsoft-_-edge/getmissingkbs
```

### <a name="response"></a><span data-ttu-id="57146-137">Réponse</span><span class="sxs-lookup"><span data-stu-id="57146-137">Response</span></span>

<span data-ttu-id="57146-138">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="57146-138">Here is an example of the response.</span></span>


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

## <a name="related-topics"></a><span data-ttu-id="57146-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57146-139">Related topics</span></span>

- [<span data-ttu-id="57146-140">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="57146-140">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="57146-141">Inventaire des logiciels de vulnérabilité & menace</span><span class="sxs-lookup"><span data-stu-id="57146-141">Threat & Vulnerability software inventory</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-software-inventory)
