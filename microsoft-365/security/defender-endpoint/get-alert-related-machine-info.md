---
title: Obtenir des informations sur l’ordinateur associé à une alerte
description: Récupérez tous les appareils associés à une alerte spécifique à l’aide de Microsoft Defender for Endpoint.
keywords: api, api de graphique, api pris en charge, obtenir des informations d’alerte, informations d’alerte, appareil associé
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 70ce6adce3e14be7ee440b96587b8f9402c0b99f
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166630"
---
# <a name="get-alert-related-machine-information-api"></a><span data-ttu-id="42369-104">API Obtenir les informations sur l’ordinateur associé à une alerte</span><span class="sxs-lookup"><span data-stu-id="42369-104">Get alert related machine information API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="42369-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="42369-105">**Applies to:**</span></span>
- [<span data-ttu-id="42369-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="42369-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="42369-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="42369-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="42369-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="42369-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="42369-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="42369-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="42369-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="42369-110">API description</span></span>
<span data-ttu-id="42369-111">Récupère [l’appareil](machine.md) associé à une alerte spécifique.</span><span class="sxs-lookup"><span data-stu-id="42369-111">Retrieves [Device](machine.md) related to a specific alert.</span></span>


## <a name="limitations"></a><span data-ttu-id="42369-112">Limites</span><span class="sxs-lookup"><span data-stu-id="42369-112">Limitations</span></span>
1. <span data-ttu-id="42369-113">Vous pouvez interroger la dernière mise à jour des alertes en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="42369-113">You can query on alerts last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="42369-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="42369-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="42369-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="42369-115">Permissions</span></span>
<span data-ttu-id="42369-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="42369-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="42369-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="42369-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="42369-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="42369-118">Permission type</span></span> |   <span data-ttu-id="42369-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="42369-119">Permission</span></span>  |   <span data-ttu-id="42369-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="42369-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="42369-121">Application</span><span class="sxs-lookup"><span data-stu-id="42369-121">Application</span></span> |   <span data-ttu-id="42369-122">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="42369-122">Machine.Read.All</span></span> |  <span data-ttu-id="42369-123">« Lire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="42369-123">'Read all machine information'</span></span>
<span data-ttu-id="42369-124">Application</span><span class="sxs-lookup"><span data-stu-id="42369-124">Application</span></span> |   <span data-ttu-id="42369-125">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="42369-125">Machine.ReadWrite.All</span></span> | <span data-ttu-id="42369-126">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="42369-126">'Read and write all machine information'</span></span>
<span data-ttu-id="42369-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="42369-127">Delegated (work or school account)</span></span> | <span data-ttu-id="42369-128">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="42369-128">Machine.Read</span></span> | <span data-ttu-id="42369-129">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="42369-129">'Read machine information'</span></span>
<span data-ttu-id="42369-130">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="42369-130">Delegated (work or school account)</span></span> | <span data-ttu-id="42369-131">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="42369-131">Machine.ReadWrite</span></span> | <span data-ttu-id="42369-132">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="42369-132">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="42369-133">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="42369-133">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="42369-134">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="42369-134">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="42369-135">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="42369-135">The user needs to have access to the device associated with the alert, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="42369-136">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="42369-136">HTTP request</span></span>

```http
GET /api/alerts/{id}/machine
```

## <a name="request-headers"></a><span data-ttu-id="42369-137">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="42369-137">Request headers</span></span>

<span data-ttu-id="42369-138">Nom</span><span class="sxs-lookup"><span data-stu-id="42369-138">Name</span></span> | <span data-ttu-id="42369-139">Type</span><span class="sxs-lookup"><span data-stu-id="42369-139">Type</span></span> | <span data-ttu-id="42369-140">Description</span><span class="sxs-lookup"><span data-stu-id="42369-140">Description</span></span>
:---|:---|:---
<span data-ttu-id="42369-141">Autorisation</span><span class="sxs-lookup"><span data-stu-id="42369-141">Authorization</span></span> | <span data-ttu-id="42369-142">Chaîne</span><span class="sxs-lookup"><span data-stu-id="42369-142">String</span></span> | <span data-ttu-id="42369-143">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="42369-143">Bearer {token}.</span></span> <span data-ttu-id="42369-144">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="42369-144">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="42369-145">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="42369-145">Request body</span></span>
<span data-ttu-id="42369-146">Vide</span><span class="sxs-lookup"><span data-stu-id="42369-146">Empty</span></span>

## <a name="response"></a><span data-ttu-id="42369-147">Réponse</span><span class="sxs-lookup"><span data-stu-id="42369-147">Response</span></span>
<span data-ttu-id="42369-148">En cas de réussite et si l’alerte et l’appareil existent : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="42369-148">If successful and alert and device exist - 200 OK.</span></span> <span data-ttu-id="42369-149">Si l’alerte est in trouvée ou si l’appareil est in trouvé - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="42369-149">If alert not found or device not found - 404 Not Found.</span></span>

## <a name="example"></a><span data-ttu-id="42369-150">Exemple</span><span class="sxs-lookup"><span data-stu-id="42369-150">Example</span></span>

<span data-ttu-id="42369-151">**Demande**</span><span class="sxs-lookup"><span data-stu-id="42369-151">**Request**</span></span>

<span data-ttu-id="42369-152">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="42369-152">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/alerts/636688558380765161_2136280442/machine
```

<span data-ttu-id="42369-153">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="42369-153">**Response**</span></span>

<span data-ttu-id="42369-154">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="42369-154">Here is an example of the response.</span></span>


```json
{
    "id": "1e5bc9d7e413ddd7902c2932e418702b84d0cc07",
    "computerDnsName": "mymachine1.contoso.com",
    "firstSeen": "2018-08-02T14:55:03.7791856Z",
    "lastSeen": "2021-01-25T07:27:36.052313Z",
    "osPlatform": "Windows10",
    "osProcessor": "x64",
    "version": "1901",
    "lastIpAddress": "10.166.113.46",
    "lastExternalIpAddress": "167.220.203.175",
    "osBuild": 19042,
    "healthStatus": "Active",
    "deviceValue": "Normal",
    "rbacGroupName": "The-A-Team",
    "riskScore": "Low",
    "exposureLevel": "Low",
    "aadDeviceId": "fd2e4d29-7072-4195-aaa5-1af139b78028",
    "machineTags": [
        "Tag1",
        "Tag2"
    ],
    "ipAddresses": [
        {
            "ipAddress": "10.166.113.47",
            "macAddress": "8CEC4B897E73",
            "operationalStatus": "Up"
        },
        {
            "ipAddress": "2a01:110:68:4:59e4:3916:3b3e:4f96",
            "macAddress": "8CEC4B897E73",
            "operationalStatus": "Up"
        }
    ]
}
```
