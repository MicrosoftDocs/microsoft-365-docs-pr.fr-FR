---
title: API Obtenir les ordinateurs associés au domaine
description: Découvrez comment utiliser l’API Obtenir des ordinateurs liés au domaine pour obtenir des ordinateurs qui ont communiqué avec ou depuis un domaine dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, domaine, associé, appareils
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
ms.openlocfilehash: 3fffb87c486e8b6b89b5e868b96d02dfae496e0b
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166576"
---
# <a name="get-domain-related-machines-api"></a><span data-ttu-id="a9e64-104">API Obtenir les ordinateurs associés au domaine</span><span class="sxs-lookup"><span data-stu-id="a9e64-104">Get domain related machines API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="a9e64-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a9e64-105">**Applies to:**</span></span>
- [<span data-ttu-id="a9e64-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a9e64-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="a9e64-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a9e64-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="a9e64-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="a9e64-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="a9e64-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="a9e64-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="a9e64-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="a9e64-110">API description</span></span>
<span data-ttu-id="a9e64-111">Récupère une collection [d’ordinateurs](machine.md) qui ont communiqué avec ou à partir d’une adresse de domaine donnée.</span><span class="sxs-lookup"><span data-stu-id="a9e64-111">Retrieves a collection of [Machines](machine.md) that have communicated to or from a given domain address.</span></span>


## <a name="limitations"></a><span data-ttu-id="a9e64-112">Limites</span><span class="sxs-lookup"><span data-stu-id="a9e64-112">Limitations</span></span>
1. <span data-ttu-id="a9e64-113">Vous pouvez interroger sur les appareils la dernière mise à jour en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="a9e64-113">You can query on devices last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="a9e64-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="a9e64-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="a9e64-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="a9e64-115">Permissions</span></span>
<span data-ttu-id="a9e64-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="a9e64-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="a9e64-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="a9e64-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="a9e64-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="a9e64-118">Permission type</span></span> |   <span data-ttu-id="a9e64-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="a9e64-119">Permission</span></span>  |   <span data-ttu-id="a9e64-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="a9e64-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="a9e64-121">Application</span><span class="sxs-lookup"><span data-stu-id="a9e64-121">Application</span></span> |   <span data-ttu-id="a9e64-122">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="a9e64-122">Machine.Read.All</span></span> |  <span data-ttu-id="a9e64-123">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="a9e64-123">'Read all machine profiles'</span></span>
<span data-ttu-id="a9e64-124">Application</span><span class="sxs-lookup"><span data-stu-id="a9e64-124">Application</span></span> |   <span data-ttu-id="a9e64-125">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a9e64-125">Machine.ReadWrite.All</span></span> | <span data-ttu-id="a9e64-126">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="a9e64-126">'Read and write all machine information'</span></span>
<span data-ttu-id="a9e64-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="a9e64-127">Delegated (work or school account)</span></span> | <span data-ttu-id="a9e64-128">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="a9e64-128">Machine.Read</span></span> | <span data-ttu-id="a9e64-129">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="a9e64-129">'Read machine information'</span></span>
<span data-ttu-id="a9e64-130">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="a9e64-130">Delegated (work or school account)</span></span> | <span data-ttu-id="a9e64-131">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a9e64-131">Machine.ReadWrite</span></span> | <span data-ttu-id="a9e64-132">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="a9e64-132">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="a9e64-133">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="a9e64-133">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="a9e64-134">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="a9e64-134">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="a9e64-135">La réponse inclut uniquement les appareils accessibles à l’utilisateur, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="a9e64-135">Response will include only devices that the user can access, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="a9e64-136">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="a9e64-136">HTTP request</span></span>
```http
GET /api/domains/{domain}/machines
```

## <a name="request-headers"></a><span data-ttu-id="a9e64-137">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="a9e64-137">Request headers</span></span>

<span data-ttu-id="a9e64-138">Nom</span><span class="sxs-lookup"><span data-stu-id="a9e64-138">Name</span></span> | <span data-ttu-id="a9e64-139">Type</span><span class="sxs-lookup"><span data-stu-id="a9e64-139">Type</span></span> | <span data-ttu-id="a9e64-140">Description</span><span class="sxs-lookup"><span data-stu-id="a9e64-140">Description</span></span>
:---|:---|:---
<span data-ttu-id="a9e64-141">Autorisation</span><span class="sxs-lookup"><span data-stu-id="a9e64-141">Authorization</span></span> | <span data-ttu-id="a9e64-142">Chaîne</span><span class="sxs-lookup"><span data-stu-id="a9e64-142">String</span></span> | <span data-ttu-id="a9e64-143">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="a9e64-143">Bearer {token}.</span></span> <span data-ttu-id="a9e64-144">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="a9e64-144">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="a9e64-145">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="a9e64-145">Request body</span></span>
<span data-ttu-id="a9e64-146">Vide</span><span class="sxs-lookup"><span data-stu-id="a9e64-146">Empty</span></span>

## <a name="response"></a><span data-ttu-id="a9e64-147">Réponse</span><span class="sxs-lookup"><span data-stu-id="a9e64-147">Response</span></span>
<span data-ttu-id="a9e64-148">En cas de réussite et si le domaine existe : 200 - OK avec la liste des [entités de l’ordinateur.](machine.md)</span><span class="sxs-lookup"><span data-stu-id="a9e64-148">If successful and domain exists - 200 OK with list of [machine](machine.md) entities.</span></span> <span data-ttu-id="a9e64-149">Si le domaine n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="a9e64-149">If domain do not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="a9e64-150">Exemple</span><span class="sxs-lookup"><span data-stu-id="a9e64-150">Example</span></span>

<span data-ttu-id="a9e64-151">**Demande**</span><span class="sxs-lookup"><span data-stu-id="a9e64-151">**Request**</span></span>

<span data-ttu-id="a9e64-152">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="a9e64-152">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/domains/api.securitycenter.microsoft.com/machines
```
