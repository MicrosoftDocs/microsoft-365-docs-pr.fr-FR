---
title: API Obtenir les alertes liées à l’ADRESSE IP
description: Récupérer une collection d’alertes liées à une adresse IP donnée à l’aide de Microsoft Defender pour le point de terminaison
keywords: api, api de graphique, api pris en charge, obtenir, ip, associé, alertes
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
ms.openlocfilehash: a12ae502702b7fc9f69b01cd67857003258c20f2
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770120"
---
# <a name="get-ip-related-alerts-api"></a><span data-ttu-id="6cd3a-104">API Obtenir les alertes liées à l’ADRESSE IP</span><span class="sxs-lookup"><span data-stu-id="6cd3a-104">Get IP related alerts API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6cd3a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6cd3a-105">**Applies to:**</span></span>
- [<span data-ttu-id="6cd3a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6cd3a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6cd3a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6cd3a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="6cd3a-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6cd3a-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="6cd3a-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="6cd3a-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="6cd3a-110">API description</span></span>
<span data-ttu-id="6cd3a-111">Récupère une collection d’alertes liées à une adresse IP donnée.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-111">Retrieves a collection of alerts related to a given IP address.</span></span>


## <a name="limitations"></a><span data-ttu-id="6cd3a-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="6cd3a-112">Limitations</span></span>
1. <span data-ttu-id="6cd3a-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="6cd3a-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="6cd3a-114">Permissions</span></span>
<span data-ttu-id="6cd3a-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="6cd3a-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="6cd3a-116">To learn more, including how to choose permissions, see [Use Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="6cd3a-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="6cd3a-117">Permission type</span></span> |   <span data-ttu-id="6cd3a-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="6cd3a-118">Permission</span></span>  |   <span data-ttu-id="6cd3a-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="6cd3a-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="6cd3a-120">Application</span><span class="sxs-lookup"><span data-stu-id="6cd3a-120">Application</span></span> |   <span data-ttu-id="6cd3a-121">Alert.Read.All</span><span class="sxs-lookup"><span data-stu-id="6cd3a-121">Alert.Read.All</span></span> |    <span data-ttu-id="6cd3a-122">« Lire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="6cd3a-122">'Read all alerts'</span></span>
<span data-ttu-id="6cd3a-123">Application</span><span class="sxs-lookup"><span data-stu-id="6cd3a-123">Application</span></span> |   <span data-ttu-id="6cd3a-124">Alert.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6cd3a-124">Alert.ReadWrite.All</span></span> |   <span data-ttu-id="6cd3a-125">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="6cd3a-125">'Read and write all alerts'</span></span>
<span data-ttu-id="6cd3a-126">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="6cd3a-126">Delegated (work or school account)</span></span> | <span data-ttu-id="6cd3a-127">Alert.Read</span><span class="sxs-lookup"><span data-stu-id="6cd3a-127">Alert.Read</span></span> | <span data-ttu-id="6cd3a-128">« Lire les alertes »</span><span class="sxs-lookup"><span data-stu-id="6cd3a-128">'Read alerts'</span></span>
<span data-ttu-id="6cd3a-129">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="6cd3a-129">Delegated (work or school account)</span></span> | <span data-ttu-id="6cd3a-130">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6cd3a-130">Alert.ReadWrite</span></span> | <span data-ttu-id="6cd3a-131">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="6cd3a-131">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="6cd3a-132">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="6cd3a-132">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="6cd3a-133">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="6cd3a-133">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="6cd3a-134">La réponse inclut uniquement les alertes, associées aux appareils, à qui [](machine-groups.md) l’utilisateur a accès, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils pour plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="6cd3a-134">Response will include only alerts, associated with devices, that the user have access to, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="6cd3a-135">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="6cd3a-135">HTTP request</span></span>
```
GET /api/ips/{ip}/alerts
```

## <a name="request-headers"></a><span data-ttu-id="6cd3a-136">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="6cd3a-136">Request headers</span></span>

<span data-ttu-id="6cd3a-137">Nom</span><span class="sxs-lookup"><span data-stu-id="6cd3a-137">Name</span></span> | <span data-ttu-id="6cd3a-138">Type</span><span class="sxs-lookup"><span data-stu-id="6cd3a-138">Type</span></span> | <span data-ttu-id="6cd3a-139">Description</span><span class="sxs-lookup"><span data-stu-id="6cd3a-139">Description</span></span>
:---|:---|:---
<span data-ttu-id="6cd3a-140">Autorisation</span><span class="sxs-lookup"><span data-stu-id="6cd3a-140">Authorization</span></span> | <span data-ttu-id="6cd3a-141">String</span><span class="sxs-lookup"><span data-stu-id="6cd3a-141">String</span></span> | <span data-ttu-id="6cd3a-142">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-142">Bearer {token}.</span></span> <span data-ttu-id="6cd3a-143">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-143">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="6cd3a-144">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="6cd3a-144">Request body</span></span>
<span data-ttu-id="6cd3a-145">Vide</span><span class="sxs-lookup"><span data-stu-id="6cd3a-145">Empty</span></span>

## <a name="response"></a><span data-ttu-id="6cd3a-146">Réponse</span><span class="sxs-lookup"><span data-stu-id="6cd3a-146">Response</span></span>
<span data-ttu-id="6cd3a-147">En cas de réussite et si l’adresse IP existe : 200 - OK avec la liste [des](alerts.md) entités d’alerte dans le corps.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-147">If successful and IP exists - 200 OK with list of [alert](alerts.md) entities in the body.</span></span> <span data-ttu-id="6cd3a-148">Si l’adresse IP n’existe pas : 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-148">If IP do not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="6cd3a-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="6cd3a-149">Example</span></span>

<span data-ttu-id="6cd3a-150">**Demande**</span><span class="sxs-lookup"><span data-stu-id="6cd3a-150">**Request**</span></span>

<span data-ttu-id="6cd3a-151">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-151">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/ips/10.209.67.177/alerts
```
