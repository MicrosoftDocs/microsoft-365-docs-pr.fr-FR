---
title: API Obtenir les ordinateurs associés au domaine
description: Découvrez comment utiliser l’API Obtenir des ordinateurs liés au domaine pour obtenir des ordinateurs qui ont communiqué avec ou à partir d’un domaine dans Microsoft Defender pour point de terminaison.
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 362e3db0ed89924c58fa9662f7acbbe0c16c37c6
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772220"
---
# <a name="get-domain-related-machines-api"></a><span data-ttu-id="1326d-104">API Obtenir les ordinateurs associés au domaine</span><span class="sxs-lookup"><span data-stu-id="1326d-104">Get domain related machines API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1326d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1326d-105">**Applies to:**</span></span>
- [<span data-ttu-id="1326d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1326d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1326d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1326d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="1326d-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1326d-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="1326d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1326d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="1326d-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="1326d-110">API description</span></span>
<span data-ttu-id="1326d-111">Extrait une collection [d’ordinateurs](machine.md) qui ont communiqué avec ou à partir d’une adresse de domaine donnée.</span><span class="sxs-lookup"><span data-stu-id="1326d-111">Retrieves a collection of [Machines](machine.md) that have communicated to or from a given domain address.</span></span>


## <a name="limitations"></a><span data-ttu-id="1326d-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="1326d-112">Limitations</span></span>
1. <span data-ttu-id="1326d-113">Vous pouvez interroger sur les appareils la dernière mise à jour en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="1326d-113">You can query on devices last updated according to your configured retention period.</span></span>
2. <span data-ttu-id="1326d-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="1326d-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="1326d-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="1326d-115">Permissions</span></span>
<span data-ttu-id="1326d-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="1326d-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="1326d-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="1326d-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="1326d-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="1326d-118">Permission type</span></span> |   <span data-ttu-id="1326d-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1326d-119">Permission</span></span>  |   <span data-ttu-id="1326d-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="1326d-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="1326d-121">Application</span><span class="sxs-lookup"><span data-stu-id="1326d-121">Application</span></span> |   <span data-ttu-id="1326d-122">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="1326d-122">Machine.Read.All</span></span> |  <span data-ttu-id="1326d-123">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="1326d-123">'Read all machine profiles'</span></span>
<span data-ttu-id="1326d-124">Application</span><span class="sxs-lookup"><span data-stu-id="1326d-124">Application</span></span> |   <span data-ttu-id="1326d-125">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1326d-125">Machine.ReadWrite.All</span></span> | <span data-ttu-id="1326d-126">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="1326d-126">'Read and write all machine information'</span></span>
<span data-ttu-id="1326d-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="1326d-127">Delegated (work or school account)</span></span> | <span data-ttu-id="1326d-128">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="1326d-128">Machine.Read</span></span> | <span data-ttu-id="1326d-129">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="1326d-129">'Read machine information'</span></span>
<span data-ttu-id="1326d-130">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="1326d-130">Delegated (work or school account)</span></span> | <span data-ttu-id="1326d-131">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1326d-131">Machine.ReadWrite</span></span> | <span data-ttu-id="1326d-132">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="1326d-132">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="1326d-133">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="1326d-133">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="1326d-134">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="1326d-134">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="1326d-135">La réponse inclut uniquement les appareils accessibles à l’utilisateur, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="1326d-135">Response will include only devices that the user can access, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="1326d-136">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="1326d-136">HTTP request</span></span>
```http
GET /api/domains/{domain}/machines
```

## <a name="request-headers"></a><span data-ttu-id="1326d-137">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="1326d-137">Request headers</span></span>

<span data-ttu-id="1326d-138">Nom</span><span class="sxs-lookup"><span data-stu-id="1326d-138">Name</span></span> | <span data-ttu-id="1326d-139">Type</span><span class="sxs-lookup"><span data-stu-id="1326d-139">Type</span></span> | <span data-ttu-id="1326d-140">Description</span><span class="sxs-lookup"><span data-stu-id="1326d-140">Description</span></span>
:---|:---|:---
<span data-ttu-id="1326d-141">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1326d-141">Authorization</span></span> | <span data-ttu-id="1326d-142">String</span><span class="sxs-lookup"><span data-stu-id="1326d-142">String</span></span> | <span data-ttu-id="1326d-143">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="1326d-143">Bearer {token}.</span></span> <span data-ttu-id="1326d-144">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="1326d-144">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="1326d-145">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="1326d-145">Request body</span></span>
<span data-ttu-id="1326d-146">Vide</span><span class="sxs-lookup"><span data-stu-id="1326d-146">Empty</span></span>

## <a name="response"></a><span data-ttu-id="1326d-147">Réponse</span><span class="sxs-lookup"><span data-stu-id="1326d-147">Response</span></span>
<span data-ttu-id="1326d-148">En cas de réussite et si le domaine existe : 200 - OK avec la liste des [entités de l’ordinateur.](machine.md)</span><span class="sxs-lookup"><span data-stu-id="1326d-148">If successful and domain exists - 200 OK with list of [machine](machine.md) entities.</span></span> <span data-ttu-id="1326d-149">Si le domaine n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="1326d-149">If domain do not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="1326d-150">Exemple</span><span class="sxs-lookup"><span data-stu-id="1326d-150">Example</span></span>

<span data-ttu-id="1326d-151">**Demande**</span><span class="sxs-lookup"><span data-stu-id="1326d-151">**Request**</span></span>

<span data-ttu-id="1326d-152">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="1326d-152">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/domains/api.securitycenter.microsoft.com/machines
```
