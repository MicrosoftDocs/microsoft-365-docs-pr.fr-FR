---
title: Obtenir des informations d’alerte par API d’ID
description: Découvrez comment utiliser l’API Obtenir des informations d’alerte par ID pour récupérer une alerte spécifique par son ID dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, alerte, informations, ID
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
ms.openlocfilehash: f9130b054ccea762e6c5cc4f2952bbfa82d24b83
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51200424"
---
# <a name="get-alert-information-by-id-api"></a><span data-ttu-id="85c51-104">Obtenir des informations d’alerte par API d’ID</span><span class="sxs-lookup"><span data-stu-id="85c51-104">Get alert information by ID API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="85c51-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="85c51-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

> <span data-ttu-id="85c51-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="85c51-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="85c51-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="85c51-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="85c51-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="85c51-108">API description</span></span>
<span data-ttu-id="85c51-109">Récupère une alerte [spécifique par](alerts.md) son ID.</span><span class="sxs-lookup"><span data-stu-id="85c51-109">Retrieves specific [Alert](alerts.md) by its ID.</span></span>


## <a name="limitations"></a><span data-ttu-id="85c51-110">Limites</span><span class="sxs-lookup"><span data-stu-id="85c51-110">Limitations</span></span>
1. <span data-ttu-id="85c51-111">Vous pouvez obtenir la dernière mise à jour des alertes en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="85c51-111">You can get alerts last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="85c51-112">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="85c51-112">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="85c51-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="85c51-113">Permissions</span></span>
<span data-ttu-id="85c51-114">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="85c51-114">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="85c51-115">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="85c51-115">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="85c51-116">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="85c51-116">Permission type</span></span> |   <span data-ttu-id="85c51-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="85c51-117">Permission</span></span>  |   <span data-ttu-id="85c51-118">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="85c51-118">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="85c51-119">Application</span><span class="sxs-lookup"><span data-stu-id="85c51-119">Application</span></span> |   <span data-ttu-id="85c51-120">Alert.Read.All</span><span class="sxs-lookup"><span data-stu-id="85c51-120">Alert.Read.All</span></span> |    <span data-ttu-id="85c51-121">« Lire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="85c51-121">'Read all alerts'</span></span>
<span data-ttu-id="85c51-122">Application</span><span class="sxs-lookup"><span data-stu-id="85c51-122">Application</span></span> |   <span data-ttu-id="85c51-123">Alert.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="85c51-123">Alert.ReadWrite.All</span></span> |   <span data-ttu-id="85c51-124">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="85c51-124">'Read and write all alerts'</span></span>
<span data-ttu-id="85c51-125">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="85c51-125">Delegated (work or school account)</span></span> | <span data-ttu-id="85c51-126">Alert.Read</span><span class="sxs-lookup"><span data-stu-id="85c51-126">Alert.Read</span></span> | <span data-ttu-id="85c51-127">« Lire les alertes »</span><span class="sxs-lookup"><span data-stu-id="85c51-127">'Read alerts'</span></span>
<span data-ttu-id="85c51-128">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="85c51-128">Delegated (work or school account)</span></span> | <span data-ttu-id="85c51-129">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="85c51-129">Alert.ReadWrite</span></span> | <span data-ttu-id="85c51-130">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="85c51-130">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="85c51-131">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="85c51-131">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="85c51-132">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="85c51-132">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="85c51-133">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="85c51-133">The user needs to have access to the device associated with the alert, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="85c51-134">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="85c51-134">HTTP request</span></span>
```
GET /api/alerts/{id}
```

## <a name="request-headers"></a><span data-ttu-id="85c51-135">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="85c51-135">Request headers</span></span>

<span data-ttu-id="85c51-136">Nom</span><span class="sxs-lookup"><span data-stu-id="85c51-136">Name</span></span> | <span data-ttu-id="85c51-137">Type</span><span class="sxs-lookup"><span data-stu-id="85c51-137">Type</span></span> | <span data-ttu-id="85c51-138">Description</span><span class="sxs-lookup"><span data-stu-id="85c51-138">Description</span></span>
:---|:---|:---
<span data-ttu-id="85c51-139">Autorisation</span><span class="sxs-lookup"><span data-stu-id="85c51-139">Authorization</span></span> | <span data-ttu-id="85c51-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="85c51-140">String</span></span> | <span data-ttu-id="85c51-141">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="85c51-141">Bearer {token}.</span></span> <span data-ttu-id="85c51-142">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="85c51-142">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="85c51-143">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="85c51-143">Request body</span></span>
<span data-ttu-id="85c51-144">Vide</span><span class="sxs-lookup"><span data-stu-id="85c51-144">Empty</span></span>

## <a name="response"></a><span data-ttu-id="85c51-145">Réponse</span><span class="sxs-lookup"><span data-stu-id="85c51-145">Response</span></span>
<span data-ttu-id="85c51-146">Si elle réussit, cette méthode renvoie 200 OK et l’entité [d’alerte](alerts.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="85c51-146">If successful, this method returns 200 OK, and the [alert](alerts.md) entity in the response body.</span></span> <span data-ttu-id="85c51-147">Si l’alerte avec l’ID spécifié est in trouvée - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="85c51-147">If alert with the specified id was not found - 404 Not Found.</span></span>
