---
title: API Obtenir des informations sur les fichiers
description: Découvrez comment utiliser l’API Obtenir des informations sur le fichier pour obtenir un fichier par l’identificateur Sha1, Sha256 ou MD5 dans Microsoft Defender for Endpoint.
keywords: api, api de graphique, api pris en charge, obtenir, fichier, informations, sha1, sha256, md5
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: b7877fb2d9b616b487d23befd0f0af35ce2c0753
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770289"
---
# <a name="get-file-information-api"></a><span data-ttu-id="71871-104">API Obtenir des informations sur les fichiers</span><span class="sxs-lookup"><span data-stu-id="71871-104">Get file information API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="71871-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="71871-105">**Applies to:**</span></span>
- [<span data-ttu-id="71871-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="71871-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="71871-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="71871-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="71871-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="71871-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="71871-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="71871-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="71871-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="71871-110">API description</span></span>
<span data-ttu-id="71871-111">Récupère un fichier [par](files.md) identificateur Sha1 ou Sha256</span><span class="sxs-lookup"><span data-stu-id="71871-111">Retrieves a [File](files.md) by identifier Sha1, or Sha256</span></span>


## <a name="limitations"></a><span data-ttu-id="71871-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="71871-112">Limitations</span></span>
1. <span data-ttu-id="71871-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="71871-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="71871-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="71871-114">Permissions</span></span>
<span data-ttu-id="71871-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="71871-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="71871-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="71871-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="71871-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="71871-117">Permission type</span></span> |   <span data-ttu-id="71871-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="71871-118">Permission</span></span>  |   <span data-ttu-id="71871-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="71871-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="71871-120">Application</span><span class="sxs-lookup"><span data-stu-id="71871-120">Application</span></span> |   <span data-ttu-id="71871-121">File.Read.All</span><span class="sxs-lookup"><span data-stu-id="71871-121">File.Read.All</span></span> | <span data-ttu-id="71871-122">« Lire tous les profils de fichiers »</span><span class="sxs-lookup"><span data-stu-id="71871-122">'Read all file profiles'</span></span>
<span data-ttu-id="71871-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="71871-123">Delegated (work or school account)</span></span> | <span data-ttu-id="71871-124">File.Read.All</span><span class="sxs-lookup"><span data-stu-id="71871-124">File.Read.All</span></span> |    <span data-ttu-id="71871-125">« Lire tous les profils de fichiers »</span><span class="sxs-lookup"><span data-stu-id="71871-125">'Read all file profiles'</span></span>

>[!Note]
> <span data-ttu-id="71871-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="71871-126">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="71871-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="71871-127">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="71871-128">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="71871-128">HTTP request</span></span>
```
GET /api/files/{id}
```

## <a name="request-headers"></a><span data-ttu-id="71871-129">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="71871-129">Request headers</span></span>

<span data-ttu-id="71871-130">Nom</span><span class="sxs-lookup"><span data-stu-id="71871-130">Name</span></span> | <span data-ttu-id="71871-131">Type</span><span class="sxs-lookup"><span data-stu-id="71871-131">Type</span></span> | <span data-ttu-id="71871-132">Description</span><span class="sxs-lookup"><span data-stu-id="71871-132">Description</span></span>
:---|:---|:---
<span data-ttu-id="71871-133">Autorisation</span><span class="sxs-lookup"><span data-stu-id="71871-133">Authorization</span></span> | <span data-ttu-id="71871-134">String</span><span class="sxs-lookup"><span data-stu-id="71871-134">String</span></span> | <span data-ttu-id="71871-135">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="71871-135">Bearer {token}.</span></span> <span data-ttu-id="71871-136">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="71871-136">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="71871-137">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="71871-137">Request body</span></span>
<span data-ttu-id="71871-138">Vide</span><span class="sxs-lookup"><span data-stu-id="71871-138">Empty</span></span>

## <a name="response"></a><span data-ttu-id="71871-139">Réponse</span><span class="sxs-lookup"><span data-stu-id="71871-139">Response</span></span>
<span data-ttu-id="71871-140">En cas de réussite et si le [](files.md) fichier existe : 200 - OK avec l’entité de fichier dans le corps.</span><span class="sxs-lookup"><span data-stu-id="71871-140">If successful and file exists - 200 OK with the [file](files.md) entity in the body.</span></span> <span data-ttu-id="71871-141">Si le fichier n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="71871-141">If file does not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="71871-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="71871-142">Example</span></span>

<span data-ttu-id="71871-143">**Demande**</span><span class="sxs-lookup"><span data-stu-id="71871-143">**Request**</span></span>

<span data-ttu-id="71871-144">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="71871-144">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/files/4388963aaa83afe2042a46a3c017ad50bdcdafb3
```

<span data-ttu-id="71871-145">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="71871-145">**Response**</span></span>

<span data-ttu-id="71871-146">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="71871-146">Here is an example of the response.</span></span>


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Files/$entity",
    "sha1": "4388963aaa83afe2042a46a3c017ad50bdcdafb3",
    "sha256": "413c58c8267d2c8648d8f6384bacc2ae9c929b2b96578b6860b5087cd1bd6462",
    "globalPrevalence": 180022,
    "globalFirstObserved": "2017-09-19T03:51:27.6785431Z",
    "globalLastObserved": "2020-01-06T03:59:21.3229314Z",
    "size": 22139496,
    "fileType": "APP",
    "isPeFile": true,
    "filePublisher": "CHENGDU YIWO Tech Development Co., Ltd.",
    "fileProductName": "EaseUS MobiSaver for Android",
    "signer": "CHENGDU YIWO Tech Development Co., Ltd.",
    "issuer": "VeriSign Class 3 Code Signing 2010 CA",
    "signerHash": "6c3245d4a9bc0244d99dff27af259cbbae2e2d16",
    "isValidCertificate": false,
    "determinationType": "Pua",
    "determinationValue": "PUA:Win32/FusionCore"
}
```
