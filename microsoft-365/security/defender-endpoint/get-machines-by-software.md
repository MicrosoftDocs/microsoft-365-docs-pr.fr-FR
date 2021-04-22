---
title: Liste des appareils par logiciel
description: Récupérez la liste des appareils sur qui ce logiciel est installé.
keywords: api, api de graphique, api pris en charge, obtenir, lister les appareils, liste des appareils, liste des appareils par logiciel, Api tvm microsoft Defender pour point de terminaison
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
ms.openlocfilehash: ff0bb9a6f17b8d4dc6432292ec98743d3eaf952c
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51929096"
---
# <a name="list-devices-by-software"></a><span data-ttu-id="ee38c-104">Liste des appareils par logiciel</span><span class="sxs-lookup"><span data-stu-id="ee38c-104">List devices by software</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ee38c-105">**S'applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="ee38c-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="ee38c-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ee38c-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="ee38c-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ee38c-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="ee38c-108">Récupérez la liste des références d'appareils sur les appareils sur qui ce logiciel est installé.</span><span class="sxs-lookup"><span data-stu-id="ee38c-108">Retrieve a list of device references that has this software installed.</span></span>

## <a name="permissions"></a><span data-ttu-id="ee38c-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="ee38c-109">Permissions</span></span>
<span data-ttu-id="ee38c-110">L'une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="ee38c-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="ee38c-111">Pour plus d'informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="ee38c-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="ee38c-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="ee38c-112">Permission type</span></span> |   <span data-ttu-id="ee38c-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="ee38c-113">Permission</span></span>  |   <span data-ttu-id="ee38c-114">Nom d'affichage de l'autorisation</span><span class="sxs-lookup"><span data-stu-id="ee38c-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="ee38c-115">Application</span><span class="sxs-lookup"><span data-stu-id="ee38c-115">Application</span></span> | <span data-ttu-id="ee38c-116">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="ee38c-116">Software.Read.All</span></span> | <span data-ttu-id="ee38c-117">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="ee38c-117">'Read Threat and Vulnerability Management Software information'</span></span>
<span data-ttu-id="ee38c-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="ee38c-118">Delegated (work or school account)</span></span> | <span data-ttu-id="ee38c-119">Software.Read</span><span class="sxs-lookup"><span data-stu-id="ee38c-119">Software.Read</span></span> | <span data-ttu-id="ee38c-120">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="ee38c-120">'Read Threat and Vulnerability Management Software information'</span></span>

## <a name="http-request"></a><span data-ttu-id="ee38c-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="ee38c-121">HTTP request</span></span>
```
GET /api/Software/{Id}/machineReferences 
```

## <a name="request-headers"></a><span data-ttu-id="ee38c-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="ee38c-122">Request headers</span></span>

| <span data-ttu-id="ee38c-123">Nom</span><span class="sxs-lookup"><span data-stu-id="ee38c-123">Name</span></span>        | <span data-ttu-id="ee38c-124">Type</span><span class="sxs-lookup"><span data-stu-id="ee38c-124">Type</span></span> | <span data-ttu-id="ee38c-125">Description</span><span class="sxs-lookup"><span data-stu-id="ee38c-125">Description</span></span>
|:--------------|:-------|:--------------|
| <span data-ttu-id="ee38c-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="ee38c-126">Authorization</span></span> | <span data-ttu-id="ee38c-127">String</span><span class="sxs-lookup"><span data-stu-id="ee38c-127">String</span></span> | <span data-ttu-id="ee38c-128">Porteur {token}. **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="ee38c-128">Bearer {token}.**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="ee38c-129">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="ee38c-129">Request body</span></span>
<span data-ttu-id="ee38c-130">Vide</span><span class="sxs-lookup"><span data-stu-id="ee38c-130">Empty</span></span>

## <a name="response"></a><span data-ttu-id="ee38c-131">Réponse</span><span class="sxs-lookup"><span data-stu-id="ee38c-131">Response</span></span>
<span data-ttu-id="ee38c-132">Si elle réussit, cette méthode renvoie 200 OK et une liste d'appareils avec le logiciel installé dans le corps.</span><span class="sxs-lookup"><span data-stu-id="ee38c-132">If successful, this method returns 200 OK and a list of devices with the software installed in the body.</span></span> 


## <a name="example"></a><span data-ttu-id="ee38c-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="ee38c-133">Example</span></span>

<span data-ttu-id="ee38c-134">**Demande**</span><span class="sxs-lookup"><span data-stu-id="ee38c-134">**Request**</span></span>

<span data-ttu-id="ee38c-135">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="ee38c-135">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/Software/microsoft-_-edge/machineReferences
```

<span data-ttu-id="ee38c-136">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="ee38c-136">**Response**</span></span>

<span data-ttu-id="ee38c-137">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="ee38c-137">Here is an example of the response.</span></span>

```json

{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#MachineReferences",
    "value": [
        {
            "id": "7c7e1896fa39efb0a32a2cf421d837af1b9bf762",
            "computerDnsName": "dave_desktop",
            "osPlatform": "Windows10",
            "rbacGroupName": "GroupTwo"
        },
        {
            "id": "7d5cc2e7c305e4a0a290392abf6707f9888fda0d",
            "computerDnsName": "jane_PC",
            "osPlatform": "Windows10",
            "rbacGroupName": "GroupTwo"
        }
        ...
    ]
}
```

## <a name="related-topics"></a><span data-ttu-id="ee38c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee38c-138">Related topics</span></span>
- [<span data-ttu-id="ee38c-139">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="ee38c-139">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="ee38c-140">Inventaire des logiciels de vulnérabilité & menace</span><span class="sxs-lookup"><span data-stu-id="ee38c-140">Threat & Vulnerability software inventory</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-software-inventory)
