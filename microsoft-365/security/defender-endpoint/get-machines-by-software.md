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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: e1adf28823d6b86417c32578a89480958946c50d
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770552"
---
# <a name="list-devices-by-software"></a><span data-ttu-id="2400d-104">Liste des appareils par logiciel</span><span class="sxs-lookup"><span data-stu-id="2400d-104">List devices by software</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2400d-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="2400d-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="2400d-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2400d-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="2400d-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2400d-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="2400d-108">Récupérez la liste des références d’appareils sur les appareils sur qui ce logiciel est installé.</span><span class="sxs-lookup"><span data-stu-id="2400d-108">Retrieve a list of device references that has this software installed.</span></span>

## <a name="permissions"></a><span data-ttu-id="2400d-109">Autorisations</span><span class="sxs-lookup"><span data-stu-id="2400d-109">Permissions</span></span>
<span data-ttu-id="2400d-110">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="2400d-110">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="2400d-111">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2400d-111">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="2400d-112">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="2400d-112">Permission type</span></span> |   <span data-ttu-id="2400d-113">Autorisation</span><span class="sxs-lookup"><span data-stu-id="2400d-113">Permission</span></span>  |   <span data-ttu-id="2400d-114">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="2400d-114">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="2400d-115">Application</span><span class="sxs-lookup"><span data-stu-id="2400d-115">Application</span></span> | <span data-ttu-id="2400d-116">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="2400d-116">Software.Read.All</span></span> | <span data-ttu-id="2400d-117">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="2400d-117">'Read Threat and Vulnerability Management Software information'</span></span>
<span data-ttu-id="2400d-118">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="2400d-118">Delegated (work or school account)</span></span> | <span data-ttu-id="2400d-119">Software.Read</span><span class="sxs-lookup"><span data-stu-id="2400d-119">Software.Read</span></span> | <span data-ttu-id="2400d-120">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="2400d-120">'Read Threat and Vulnerability Management Software information'</span></span>

## <a name="http-request"></a><span data-ttu-id="2400d-121">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="2400d-121">HTTP request</span></span>
```
GET /api/Software/{Id}/machineReferences 
```

## <a name="request-headers"></a><span data-ttu-id="2400d-122">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="2400d-122">Request headers</span></span>

| <span data-ttu-id="2400d-123">Nom</span><span class="sxs-lookup"><span data-stu-id="2400d-123">Name</span></span>        | <span data-ttu-id="2400d-124">Type</span><span class="sxs-lookup"><span data-stu-id="2400d-124">Type</span></span> | <span data-ttu-id="2400d-125">Description</span><span class="sxs-lookup"><span data-stu-id="2400d-125">Description</span></span>
|:--------------|:-------|:--------------|
| <span data-ttu-id="2400d-126">Autorisation</span><span class="sxs-lookup"><span data-stu-id="2400d-126">Authorization</span></span> | <span data-ttu-id="2400d-127">String</span><span class="sxs-lookup"><span data-stu-id="2400d-127">String</span></span> | <span data-ttu-id="2400d-128">Porteur {token}. **Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="2400d-128">Bearer {token}.**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="2400d-129">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="2400d-129">Request body</span></span>
<span data-ttu-id="2400d-130">Vide</span><span class="sxs-lookup"><span data-stu-id="2400d-130">Empty</span></span>

## <a name="response"></a><span data-ttu-id="2400d-131">Réponse</span><span class="sxs-lookup"><span data-stu-id="2400d-131">Response</span></span>
<span data-ttu-id="2400d-132">Si elle réussit, cette méthode renvoie 200 OK et une liste d’appareils avec le logiciel installé dans le corps.</span><span class="sxs-lookup"><span data-stu-id="2400d-132">If successful, this method returns 200 OK and a list of devices with the software installed in the body.</span></span> 


## <a name="example"></a><span data-ttu-id="2400d-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="2400d-133">Example</span></span>

<span data-ttu-id="2400d-134">**Demande**</span><span class="sxs-lookup"><span data-stu-id="2400d-134">**Request**</span></span>

<span data-ttu-id="2400d-135">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="2400d-135">Here is an example of the request.</span></span>

```
GET https://api.securitycenter.microsoft.com/api/Software/microsoft-_-edge/machineReferences
```

<span data-ttu-id="2400d-136">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="2400d-136">**Response**</span></span>

<span data-ttu-id="2400d-137">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="2400d-137">Here is an example of the response.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2400d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2400d-138">Related topics</span></span>
- [<span data-ttu-id="2400d-139">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="2400d-139">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="2400d-140">Inventaire des logiciels de vulnérabilité & menace</span><span class="sxs-lookup"><span data-stu-id="2400d-140">Threat & Vulnerability software inventory</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-software-inventory)
