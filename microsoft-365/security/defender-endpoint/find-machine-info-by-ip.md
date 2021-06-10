---
title: Rechercher des informations sur l’appareil par API IP interne
description: Utilisez cette API pour créer des appels liés à la recherche d’une entrée d’appareil autour d’un timestamp spécifique par ip interne.
keywords: ip, api, api de graphique, api pris en charge, rechercher un appareil, informations sur l’appareil
search.product: eADQiWindows 10XVcnh
ms.prod: w10
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
ms.openlocfilehash: fa1973d1c53048b04c9135a72e55ec4759412b18
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166708"
---
# <a name="find-device-information-by-internal-ip-api"></a><span data-ttu-id="b7d16-104">Rechercher des informations sur l’appareil par API IP interne</span><span class="sxs-lookup"><span data-stu-id="b7d16-104">Find device information by internal IP API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="b7d16-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="b7d16-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2154037)</span></span>

- <span data-ttu-id="b7d16-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b7d16-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="b7d16-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b7d16-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="b7d16-108">Recherchez un appareil par adresse IP interne.</span><span class="sxs-lookup"><span data-stu-id="b7d16-108">Find a device by internal IP.</span></span>

>[!NOTE]
><span data-ttu-id="b7d16-109">L’timestamp doit se trouver dans les 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="b7d16-109">The timestamp must be within the last 30 days.</span></span>

## <a name="permissions"></a><span data-ttu-id="b7d16-110">Autorisations</span><span class="sxs-lookup"><span data-stu-id="b7d16-110">Permissions</span></span>
<span data-ttu-id="b7d16-111">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="b7d16-111">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="b7d16-112">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="b7d16-112">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="b7d16-113">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="b7d16-113">Permission type</span></span> | <span data-ttu-id="b7d16-114">Autorisation</span><span class="sxs-lookup"><span data-stu-id="b7d16-114">Permission</span></span> | <span data-ttu-id="b7d16-115">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="b7d16-115">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="b7d16-116">Application</span><span class="sxs-lookup"><span data-stu-id="b7d16-116">Application</span></span> | <span data-ttu-id="b7d16-117">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="b7d16-117">Machine.Read.All</span></span> | <span data-ttu-id="b7d16-118">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="b7d16-118">'Read all machine profiles'</span></span>
<span data-ttu-id="b7d16-119">Application</span><span class="sxs-lookup"><span data-stu-id="b7d16-119">Application</span></span> | <span data-ttu-id="b7d16-120">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b7d16-120">Machine.ReadWrite.All</span></span> | <span data-ttu-id="b7d16-121">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="b7d16-121">'Read and write all machine information'</span></span>

## <a name="http-request"></a><span data-ttu-id="b7d16-122">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="b7d16-122">HTTP request</span></span>
```
GET /api/machines/find(timestamp={time},key={IP})
```

## <a name="request-headers"></a><span data-ttu-id="b7d16-123">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="b7d16-123">Request headers</span></span>

<span data-ttu-id="b7d16-124">Nom</span><span class="sxs-lookup"><span data-stu-id="b7d16-124">Name</span></span> | <span data-ttu-id="b7d16-125">Type</span><span class="sxs-lookup"><span data-stu-id="b7d16-125">Type</span></span> | <span data-ttu-id="b7d16-126">Description</span><span class="sxs-lookup"><span data-stu-id="b7d16-126">Description</span></span>
:---|:---|:---
<span data-ttu-id="b7d16-127">Autorisation</span><span class="sxs-lookup"><span data-stu-id="b7d16-127">Authorization</span></span> | <span data-ttu-id="b7d16-128">String</span><span class="sxs-lookup"><span data-stu-id="b7d16-128">String</span></span> | <span data-ttu-id="b7d16-129">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="b7d16-129">Bearer {token}.</span></span> <span data-ttu-id="b7d16-130">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="b7d16-130">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="b7d16-131">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="b7d16-131">Request body</span></span>
<span data-ttu-id="b7d16-132">Vide</span><span class="sxs-lookup"><span data-stu-id="b7d16-132">Empty</span></span>

## <a name="response"></a><span data-ttu-id="b7d16-133">Réponse</span><span class="sxs-lookup"><span data-stu-id="b7d16-133">Response</span></span>
<span data-ttu-id="b7d16-134">En cas de réussite et si l’ordinateur existe : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="b7d16-134">If successful and machine exists - 200 OK.</span></span>
<span data-ttu-id="b7d16-135">Si aucun ordinateur n’est trouvé - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="b7d16-135">If no machine found - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="b7d16-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="b7d16-136">Example</span></span>

<span data-ttu-id="b7d16-137">**Demande**</span><span class="sxs-lookup"><span data-stu-id="b7d16-137">**Request**</span></span>

<span data-ttu-id="b7d16-138">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="b7d16-138">Here is an example of the request.</span></span>

```
GET https://graph.microsoft.com/testwdatppreview/machines/find(timestamp=2018-06-19T10:00:00Z,key='10.166.93.61')
Content-type: application/json
```

<span data-ttu-id="b7d16-139">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="b7d16-139">**Response**</span></span>

<span data-ttu-id="b7d16-140">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="b7d16-140">Here is an example of the response.</span></span>

<span data-ttu-id="b7d16-141">La réponse retourne la liste de tous les appareils qui ont signalé cette adresse IP dans les 16 minutes qui s’viennent avant et après l’heure.</span><span class="sxs-lookup"><span data-stu-id="b7d16-141">The response will return a list of all devices that reported this IP address within sixteen minutes prior and after the timestamp.</span></span> 

```
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context": "https://graph.microsoft.com/testwdatppreview/$metadata#Machines",
    "value": [
        {
            "id": "04c99d46599f078f1c3da3783cf5b95f01ac61bb",
            "computerDnsName": "",
            "firstSeen": "2017-07-06T01:25:04.9480498Z",
            "osPlatform": "Windows10",
…
}
```
