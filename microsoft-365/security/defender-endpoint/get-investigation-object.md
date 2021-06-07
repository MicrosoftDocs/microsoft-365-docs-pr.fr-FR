---
title: API Obtenir un objet Investigation
description: Utilisez cette API pour créer des appels liés à l’accès à l’objet Investigation
keywords: api, api de graphique, api pris en charge, objet Investigation
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
ms.openlocfilehash: 001b8dcf4b0bfd2550f41454fc840602a6e4361f
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770130"
---
# <a name="get-investigation-api"></a><span data-ttu-id="1254a-104">API Obtenir un examen</span><span class="sxs-lookup"><span data-stu-id="1254a-104">Get Investigation API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1254a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1254a-105">**Applies to:**</span></span>
- [<span data-ttu-id="1254a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1254a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1254a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1254a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="1254a-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1254a-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="1254a-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1254a-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="1254a-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="1254a-110">API description</span></span>
<span data-ttu-id="1254a-111">Récupère un [examen spécifique par](investigation.md) son ID.</span><span class="sxs-lookup"><span data-stu-id="1254a-111">Retrieves specific [Investigation](investigation.md) by its ID.</span></span>
<br> <span data-ttu-id="1254a-112">L’ID peut être l’ID d’investigation ou l’ID d’alerte déclenchant l’enquête.</span><span class="sxs-lookup"><span data-stu-id="1254a-112">ID can be the investigation ID or the investigation triggering alert ID.</span></span>


## <a name="limitations"></a><span data-ttu-id="1254a-113">Limitations</span><span class="sxs-lookup"><span data-stu-id="1254a-113">Limitations</span></span>
1. <span data-ttu-id="1254a-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="1254a-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="1254a-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="1254a-115">Permissions</span></span>
<span data-ttu-id="1254a-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="1254a-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="1254a-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="1254a-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="1254a-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="1254a-118">Permission type</span></span> |   <span data-ttu-id="1254a-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1254a-119">Permission</span></span>  |   <span data-ttu-id="1254a-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="1254a-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="1254a-121">Application</span><span class="sxs-lookup"><span data-stu-id="1254a-121">Application</span></span> |   <span data-ttu-id="1254a-122">Alert.Read.All</span><span class="sxs-lookup"><span data-stu-id="1254a-122">Alert.Read.All</span></span> |    <span data-ttu-id="1254a-123">« Lire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="1254a-123">'Read all alerts'</span></span>
<span data-ttu-id="1254a-124">Application</span><span class="sxs-lookup"><span data-stu-id="1254a-124">Application</span></span> |   <span data-ttu-id="1254a-125">Alert.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1254a-125">Alert.ReadWrite.All</span></span> |   <span data-ttu-id="1254a-126">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="1254a-126">'Read and write all alerts'</span></span>
<span data-ttu-id="1254a-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="1254a-127">Delegated (work or school account)</span></span> | <span data-ttu-id="1254a-128">Alert.Read</span><span class="sxs-lookup"><span data-stu-id="1254a-128">Alert.Read</span></span> | <span data-ttu-id="1254a-129">« Lire les alertes »</span><span class="sxs-lookup"><span data-stu-id="1254a-129">'Read alerts'</span></span>
<span data-ttu-id="1254a-130">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="1254a-130">Delegated (work or school account)</span></span> | <span data-ttu-id="1254a-131">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1254a-131">Alert.ReadWrite</span></span> | <span data-ttu-id="1254a-132">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="1254a-132">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="1254a-133">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="1254a-133">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="1254a-134">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="1254a-134">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="1254a-135">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="1254a-135">HTTP request</span></span>
```
GET https://api.securitycenter.microsoft.com/api/investigations/{id}
```

## <a name="request-headers"></a><span data-ttu-id="1254a-136">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="1254a-136">Request headers</span></span>

<span data-ttu-id="1254a-137">Nom</span><span class="sxs-lookup"><span data-stu-id="1254a-137">Name</span></span> | <span data-ttu-id="1254a-138">Type</span><span class="sxs-lookup"><span data-stu-id="1254a-138">Type</span></span> | <span data-ttu-id="1254a-139">Description</span><span class="sxs-lookup"><span data-stu-id="1254a-139">Description</span></span>
:---|:---|:---
<span data-ttu-id="1254a-140">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1254a-140">Authorization</span></span> | <span data-ttu-id="1254a-141">String</span><span class="sxs-lookup"><span data-stu-id="1254a-141">String</span></span> | <span data-ttu-id="1254a-142">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="1254a-142">Bearer {token}.</span></span> <span data-ttu-id="1254a-143">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="1254a-143">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="1254a-144">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="1254a-144">Request body</span></span>
<span data-ttu-id="1254a-145">Vide</span><span class="sxs-lookup"><span data-stu-id="1254a-145">Empty</span></span>

## <a name="response"></a><span data-ttu-id="1254a-146">Réponse</span><span class="sxs-lookup"><span data-stu-id="1254a-146">Response</span></span>
<span data-ttu-id="1254a-147">Si elle réussit, cette méthode renvoie le code de réponse 200, Ok avec une [entité Investigations.](investigation.md)</span><span class="sxs-lookup"><span data-stu-id="1254a-147">If successful, this method returns 200, Ok response code with a [Investigations](investigation.md) entity.</span></span>

