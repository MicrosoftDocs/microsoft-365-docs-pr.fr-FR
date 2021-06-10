---
title: API Supprimer l’indicateur.
description: Découvrez comment utiliser l’API Supprimer l’indicateur pour supprimer une entité d’indicateur par ID dans Microsoft Defender pour le point de terminaison.
keywords: api, api publique, api pris en charge, supprimer, indicateur ti, entité, id
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
ms.openlocfilehash: eaef6b25e2db72149a1a1128899d8a79a38a4c60
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771020"
---
# <a name="delete-indicator-api"></a><span data-ttu-id="285d6-104">API Supprimer l’indicateur</span><span class="sxs-lookup"><span data-stu-id="285d6-104">Delete Indicator API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="285d6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="285d6-105">**Applies to:**</span></span>
- [<span data-ttu-id="285d6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="285d6-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="285d6-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="285d6-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="285d6-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="285d6-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="285d6-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="285d6-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)  

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="285d6-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="285d6-110">API description</span></span>
<span data-ttu-id="285d6-111">Supprime une entité [d’indicateur](ti-indicator.md) par ID.</span><span class="sxs-lookup"><span data-stu-id="285d6-111">Deletes an [Indicator](ti-indicator.md) entity by ID.</span></span>


## <a name="limitations"></a><span data-ttu-id="285d6-112">Limites</span><span class="sxs-lookup"><span data-stu-id="285d6-112">Limitations</span></span>
1. <span data-ttu-id="285d6-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="285d6-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="285d6-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="285d6-114">Permissions</span></span>
<span data-ttu-id="285d6-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="285d6-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="285d6-116">Pour en savoir plus, notamment sur le choix des autorisations, [consultez La](apis-intro.md) mise en place</span><span class="sxs-lookup"><span data-stu-id="285d6-116">To learn more, including how to choose permissions, see [Get started](apis-intro.md)</span></span>

<span data-ttu-id="285d6-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="285d6-117">Permission type</span></span> |   <span data-ttu-id="285d6-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="285d6-118">Permission</span></span>  |   <span data-ttu-id="285d6-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="285d6-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="285d6-120">Application</span><span class="sxs-lookup"><span data-stu-id="285d6-120">Application</span></span> |   <span data-ttu-id="285d6-121">Ti.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="285d6-121">Ti.ReadWrite</span></span> |  <span data-ttu-id="285d6-122">« Lire et écrire des indicateurs TI »</span><span class="sxs-lookup"><span data-stu-id="285d6-122">'Read and write TI Indicators'</span></span>
<span data-ttu-id="285d6-123">Application</span><span class="sxs-lookup"><span data-stu-id="285d6-123">Application</span></span> |   <span data-ttu-id="285d6-124">Ti.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="285d6-124">Ti.ReadWrite.All</span></span> |  <span data-ttu-id="285d6-125">« Lire et écrire des indicateurs »</span><span class="sxs-lookup"><span data-stu-id="285d6-125">'Read and write Indicators'</span></span>


## <a name="http-request"></a><span data-ttu-id="285d6-126">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="285d6-126">HTTP request</span></span>
```
Delete https://api.securitycenter.microsoft.com/api/indicators/{id}
```

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="request-headers"></a><span data-ttu-id="285d6-127">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="285d6-127">Request headers</span></span>

<span data-ttu-id="285d6-128">Nom</span><span class="sxs-lookup"><span data-stu-id="285d6-128">Name</span></span> | <span data-ttu-id="285d6-129">Type</span><span class="sxs-lookup"><span data-stu-id="285d6-129">Type</span></span> | <span data-ttu-id="285d6-130">Description</span><span class="sxs-lookup"><span data-stu-id="285d6-130">Description</span></span>
:---|:---|:---
<span data-ttu-id="285d6-131">Autorisation</span><span class="sxs-lookup"><span data-stu-id="285d6-131">Authorization</span></span> | <span data-ttu-id="285d6-132">String</span><span class="sxs-lookup"><span data-stu-id="285d6-132">String</span></span> | <span data-ttu-id="285d6-133">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="285d6-133">Bearer {token}.</span></span> <span data-ttu-id="285d6-134">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="285d6-134">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="285d6-135">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="285d6-135">Request body</span></span>
<span data-ttu-id="285d6-136">Vide</span><span class="sxs-lookup"><span data-stu-id="285d6-136">Empty</span></span>

## <a name="response"></a><span data-ttu-id="285d6-137">Réponse</span><span class="sxs-lookup"><span data-stu-id="285d6-137">Response</span></span>
<span data-ttu-id="285d6-138">Si l’indicateur existe et a été supprimé avec succès - 204 OK sans contenu.</span><span class="sxs-lookup"><span data-stu-id="285d6-138">If Indicator exist and deleted successfully - 204 OK without content.</span></span>
<span data-ttu-id="285d6-139">Si l’indicateur avec l’ID spécifié est in trouvé - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="285d6-139">If Indicator with the specified id was not found - 404 Not Found.</span></span>

## <a name="example"></a><span data-ttu-id="285d6-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="285d6-140">Example</span></span>

<span data-ttu-id="285d6-141">**Demande**</span><span class="sxs-lookup"><span data-stu-id="285d6-141">**Request**</span></span>

<span data-ttu-id="285d6-142">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="285d6-142">Here is an example of the request.</span></span>

```http
DELETE https://api.securitycenter.microsoft.com/api/indicators/995
```
