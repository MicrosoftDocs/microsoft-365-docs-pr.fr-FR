---
title: API Obtenir les alertes associées à l’ordinateur
description: Découvrez comment utiliser l’API Obtenir les alertes associées à l’ordinateur pour récupérer toutes les alertes liées à un appareil spécifique dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, appareils, associés, alertes
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: bf445332fed7b8661c510bf60f36088b79e2d8df
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770024"
---
# <a name="get-machine-related-alerts--api"></a><span data-ttu-id="f9305-104">API Obtenir les alertes associées à l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="f9305-104">Get machine related alerts  API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f9305-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="f9305-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="f9305-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f9305-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f9305-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f9305-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="f9305-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="f9305-108">API description</span></span>
<span data-ttu-id="f9305-109">Récupère toutes les [alertes associées](alerts.md) à un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="f9305-109">Retrieves all [Alerts](alerts.md) related to a specific device.</span></span>


## <a name="limitations"></a><span data-ttu-id="f9305-110">Limitations</span><span class="sxs-lookup"><span data-stu-id="f9305-110">Limitations</span></span>
1. <span data-ttu-id="f9305-111">Vous pouvez interroger sur les appareils la dernière mise à jour en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="f9305-111">You can query on devices last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="f9305-112">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="f9305-112">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


<span data-ttu-id="f9305-113">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="f9305-113">Permission type</span></span> |   <span data-ttu-id="f9305-114">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f9305-114">Permission</span></span>  |   <span data-ttu-id="f9305-115">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="f9305-115">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="f9305-116">Application</span><span class="sxs-lookup"><span data-stu-id="f9305-116">Application</span></span> |   <span data-ttu-id="f9305-117">Alert.Read.All</span><span class="sxs-lookup"><span data-stu-id="f9305-117">Alert.Read.All</span></span> |    <span data-ttu-id="f9305-118">« Lire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="f9305-118">'Read all alerts'</span></span>
<span data-ttu-id="f9305-119">Application</span><span class="sxs-lookup"><span data-stu-id="f9305-119">Application</span></span> |   <span data-ttu-id="f9305-120">Alert.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9305-120">Alert.ReadWrite.All</span></span> |   <span data-ttu-id="f9305-121">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="f9305-121">'Read and write all alerts'</span></span>
<span data-ttu-id="f9305-122">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="f9305-122">Delegated (work or school account)</span></span> | <span data-ttu-id="f9305-123">Alert.Read</span><span class="sxs-lookup"><span data-stu-id="f9305-123">Alert.Read</span></span> | <span data-ttu-id="f9305-124">« Lire les alertes »</span><span class="sxs-lookup"><span data-stu-id="f9305-124">'Read alerts'</span></span>
<span data-ttu-id="f9305-125">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="f9305-125">Delegated (work or school account)</span></span> | <span data-ttu-id="f9305-126">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9305-126">Alert.ReadWrite</span></span> | <span data-ttu-id="f9305-127">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="f9305-127">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="f9305-128">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="f9305-128">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="f9305-129">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="f9305-129">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="f9305-130">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="f9305-130">User needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="f9305-131">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="f9305-131">HTTP request</span></span>
```http
GET /api/machines/{id}/alerts
```

## <a name="request-headers"></a><span data-ttu-id="f9305-132">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="f9305-132">Request headers</span></span>

<span data-ttu-id="f9305-133">Nom</span><span class="sxs-lookup"><span data-stu-id="f9305-133">Name</span></span> | <span data-ttu-id="f9305-134">Type</span><span class="sxs-lookup"><span data-stu-id="f9305-134">Type</span></span> | <span data-ttu-id="f9305-135">Description</span><span class="sxs-lookup"><span data-stu-id="f9305-135">Description</span></span>
:---|:---|:---
<span data-ttu-id="f9305-136">Autorisation</span><span class="sxs-lookup"><span data-stu-id="f9305-136">Authorization</span></span> | <span data-ttu-id="f9305-137">String</span><span class="sxs-lookup"><span data-stu-id="f9305-137">String</span></span> | <span data-ttu-id="f9305-138">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="f9305-138">Bearer {token}.</span></span> <span data-ttu-id="f9305-139">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="f9305-139">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="f9305-140">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="f9305-140">Request body</span></span>
<span data-ttu-id="f9305-141">Vide</span><span class="sxs-lookup"><span data-stu-id="f9305-141">Empty</span></span>

## <a name="response"></a><span data-ttu-id="f9305-142">Réponse</span><span class="sxs-lookup"><span data-stu-id="f9305-142">Response</span></span>
<span data-ttu-id="f9305-143">En cas de réussite et si l’appareil existe : 200 - OK avec la liste [des](alerts.md) entités d’alerte dans le corps.</span><span class="sxs-lookup"><span data-stu-id="f9305-143">If successful and device exists - 200 OK with list of [alert](alerts.md) entities in the body.</span></span> <span data-ttu-id="f9305-144">If device was not found - 404 Not Found.</span><span class="sxs-lookup"><span data-stu-id="f9305-144">If device was not found - 404 Not Found.</span></span>
