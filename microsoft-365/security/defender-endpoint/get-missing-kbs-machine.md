---
title: Obtenir les ko manquants par ID d’appareil
description: Récupère les mises à jour de sécurité manquantes par ID d’appareil
keywords: api, api de graphique, api pris en charge, obtenir, liste, fichier, informations, ID d’appareil, api de gestion des menaces & vulnérabilité, api tvm mdatp
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
ms.openlocfilehash: 908ddf531a5a20b9811084ba534a152ad6158170
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51198848"
---
# <a name="get-missing-kbs-by-device-id"></a><span data-ttu-id="7f3c4-104">Obtenir les ko manquants par ID d’appareil</span><span class="sxs-lookup"><span data-stu-id="7f3c4-104">Get missing KBs by device ID</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="7f3c4-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="7f3c4-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="7f3c4-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="7f3c4-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="7f3c4-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7f3c4-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="7f3c4-108">Récupère les ko manquants (mises à jour de sécurité) par ID d’appareil</span><span class="sxs-lookup"><span data-stu-id="7f3c4-108">Retrieves missing KBs (security updates) by device ID</span></span>

## <a name="http-request"></a><span data-ttu-id="7f3c4-109">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="7f3c4-109">HTTP request</span></span>

```
GET /api/machines/{machineId}/getmissingkbs
```

## <a name="request-header"></a><span data-ttu-id="7f3c4-110">En-tête de requête</span><span class="sxs-lookup"><span data-stu-id="7f3c4-110">Request header</span></span>

<span data-ttu-id="7f3c4-111">Nom</span><span class="sxs-lookup"><span data-stu-id="7f3c4-111">Name</span></span> | <span data-ttu-id="7f3c4-112">Type</span><span class="sxs-lookup"><span data-stu-id="7f3c4-112">Type</span></span> | <span data-ttu-id="7f3c4-113">Description</span><span class="sxs-lookup"><span data-stu-id="7f3c4-113">Description</span></span>
:---|:---|:---
<span data-ttu-id="7f3c4-114">Autorisation</span><span class="sxs-lookup"><span data-stu-id="7f3c4-114">Authorization</span></span> | <span data-ttu-id="7f3c4-115">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7f3c4-115">String</span></span> | <span data-ttu-id="7f3c4-116">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="7f3c4-116">Bearer {token}.</span></span> <span data-ttu-id="7f3c4-117">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="7f3c4-117">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="7f3c4-118">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="7f3c4-118">Request body</span></span>

<span data-ttu-id="7f3c4-119">Vide</span><span class="sxs-lookup"><span data-stu-id="7f3c4-119">Empty</span></span>

## <a name="response"></a><span data-ttu-id="7f3c4-120">Réponse</span><span class="sxs-lookup"><span data-stu-id="7f3c4-120">Response</span></span>

<span data-ttu-id="7f3c4-121">Si elle réussit, cette méthode renvoie 200 OK, avec les données kb du périphérique spécifié manquantes dans le corps.</span><span class="sxs-lookup"><span data-stu-id="7f3c4-121">If successful, this method returns 200 OK, with the specified device missing kb data in the body.</span></span>

## <a name="example"></a><span data-ttu-id="7f3c4-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="7f3c4-122">Example</span></span>

### <a name="request"></a><span data-ttu-id="7f3c4-123">Demande</span><span class="sxs-lookup"><span data-stu-id="7f3c4-123">Request</span></span>

<span data-ttu-id="7f3c4-124">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="7f3c4-124">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/machines/2339ad14a01bd0299afb93dfa2550136057bff96/getmissingkbs 
```

### <a name="response"></a><span data-ttu-id="7f3c4-125">Réponse</span><span class="sxs-lookup"><span data-stu-id="7f3c4-125">Response</span></span>

<span data-ttu-id="7f3c4-126">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="7f3c4-126">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Collection(microsoft.windowsDefenderATP.api.PublicProductFixDto)",
    "value": [
        {
            "id": "4540673",
            "name": "March 2020 Security Updates",
            "productsNames": [
                "windows_10",
                "edge",
                "internet_explorer"
            ],
            "url": "https://catalog.update.microsoft.com/v7/site/Search.aspx?q=KB4540673",
            "machineMissedOn": 1,
            "cveAddressed": 97
        },
         ...
        ]
}
```

## <a name="related-topics"></a><span data-ttu-id="7f3c4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f3c4-127">Related topics</span></span>

- [<span data-ttu-id="7f3c4-128">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="7f3c4-128">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="7f3c4-129">Inventaire des logiciels de vulnérabilité & menace</span><span class="sxs-lookup"><span data-stu-id="7f3c4-129">Threat & Vulnerability software inventory</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-software-inventory)
