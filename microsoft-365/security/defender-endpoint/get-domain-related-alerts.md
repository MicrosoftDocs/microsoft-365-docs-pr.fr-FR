---
title: API Obtenir les alertes liées au domaine
description: Découvrez comment utiliser l’API Obtenir les alertes liées au domaine pour récupérer les alertes liées à une adresse de domaine donnée dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, domaine, associé, alertes
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
ms.openlocfilehash: c5de779566f1aa8e53da10b9aa5bceb92f5a0a3c
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772256"
---
# <a name="get-domain-related-alerts-api"></a><span data-ttu-id="00edf-104">API Obtenir les alertes liées au domaine</span><span class="sxs-lookup"><span data-stu-id="00edf-104">Get domain-related alerts API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="00edf-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="00edf-105">**Applies to:**</span></span>
- [<span data-ttu-id="00edf-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="00edf-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="00edf-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="00edf-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="00edf-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="00edf-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="00edf-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="00edf-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="00edf-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="00edf-110">API description</span></span>
<span data-ttu-id="00edf-111">Récupère une collection d’alertes [liées](alerts.md) à une adresse de domaine donnée.</span><span class="sxs-lookup"><span data-stu-id="00edf-111">Retrieves a collection of [Alerts](alerts.md) related to a given domain address.</span></span>


## <a name="limitations"></a><span data-ttu-id="00edf-112">Limites</span><span class="sxs-lookup"><span data-stu-id="00edf-112">Limitations</span></span>
1. <span data-ttu-id="00edf-113">Vous pouvez interroger la dernière mise à jour des alertes en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="00edf-113">You can query on alerts last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="00edf-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="00edf-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="00edf-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="00edf-115">Permissions</span></span>
<span data-ttu-id="00edf-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="00edf-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="00edf-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="00edf-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="00edf-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="00edf-118">Permission type</span></span> |   <span data-ttu-id="00edf-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="00edf-119">Permission</span></span>  |   <span data-ttu-id="00edf-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="00edf-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="00edf-121">Application</span><span class="sxs-lookup"><span data-stu-id="00edf-121">Application</span></span> |   <span data-ttu-id="00edf-122">Alert.Read.All</span><span class="sxs-lookup"><span data-stu-id="00edf-122">Alert.Read.All</span></span> |    <span data-ttu-id="00edf-123">« Lire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="00edf-123">'Read all alerts'</span></span>
<span data-ttu-id="00edf-124">Application</span><span class="sxs-lookup"><span data-stu-id="00edf-124">Application</span></span> |   <span data-ttu-id="00edf-125">Alert.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00edf-125">Alert.ReadWrite.All</span></span> |   <span data-ttu-id="00edf-126">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="00edf-126">'Read and write all alerts'</span></span>
<span data-ttu-id="00edf-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="00edf-127">Delegated (work or school account)</span></span> | <span data-ttu-id="00edf-128">Alert.Read</span><span class="sxs-lookup"><span data-stu-id="00edf-128">Alert.Read</span></span> | <span data-ttu-id="00edf-129">« Lire les alertes »</span><span class="sxs-lookup"><span data-stu-id="00edf-129">'Read alerts'</span></span>
<span data-ttu-id="00edf-130">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="00edf-130">Delegated (work or school account)</span></span> | <span data-ttu-id="00edf-131">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="00edf-131">Alert.ReadWrite</span></span> | <span data-ttu-id="00edf-132">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="00edf-132">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="00edf-133">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="00edf-133">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="00edf-134">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="00edf-134">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="00edf-135">La réponse inclut uniquement les alertes, associées aux appareils, à qui [](machine-groups.md) l’utilisateur a accès, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils pour plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="00edf-135">Response will include only alerts, associated with devices, that the user have access to, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="00edf-136">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="00edf-136">HTTP request</span></span>
```http
GET /api/domains/{domain}/alerts
```

## <a name="request-headers"></a><span data-ttu-id="00edf-137">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="00edf-137">Request headers</span></span>

| <span data-ttu-id="00edf-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="00edf-138">Header</span></span>        | <span data-ttu-id="00edf-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="00edf-139">Value</span></span>  |
|:--------------|:-------|
| <span data-ttu-id="00edf-140">Autorisation</span><span class="sxs-lookup"><span data-stu-id="00edf-140">Authorization</span></span> | <span data-ttu-id="00edf-141">String</span><span class="sxs-lookup"><span data-stu-id="00edf-141">String</span></span> |

## <a name="request-body"></a><span data-ttu-id="00edf-142">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="00edf-142">Request body</span></span>
<span data-ttu-id="00edf-143">Vide</span><span class="sxs-lookup"><span data-stu-id="00edf-143">Empty</span></span>

## <a name="response"></a><span data-ttu-id="00edf-144">Réponse</span><span class="sxs-lookup"><span data-stu-id="00edf-144">Response</span></span>
<span data-ttu-id="00edf-145">En cas de réussite et si le domaine existe : 200 - OK avec la liste des entités [d’alerte.](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="00edf-145">If successful and domain exists - 200 OK with list of [alert](alerts.md) entities.</span></span> <span data-ttu-id="00edf-146">Si le domaine n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="00edf-146">If domain does not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="00edf-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="00edf-147">Example</span></span>

<span data-ttu-id="00edf-148">**Demande**</span><span class="sxs-lookup"><span data-stu-id="00edf-148">**Request**</span></span>

<span data-ttu-id="00edf-149">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="00edf-149">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/domains/client.wns.windows.com/alerts
```
