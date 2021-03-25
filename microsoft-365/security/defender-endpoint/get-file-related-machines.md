---
title: API Obtenir les ordinateurs liés aux fichiers
description: Découvrez comment utiliser l’API Obtenir des ordinateurs liés à un fichier pour obtenir une collection d’ordinateurs liés à un hachage de fichier dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, appareils, hachage
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
ms.openlocfilehash: 051bdad362e142446d248e90fad608fe5c0f016f
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166541"
---
# <a name="get-file-related-machines-api"></a><span data-ttu-id="57469-104">API Obtenir les ordinateurs liés aux fichiers</span><span class="sxs-lookup"><span data-stu-id="57469-104">Get file-related machines API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="57469-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="57469-105">**Applies to:**</span></span>
- [<span data-ttu-id="57469-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="57469-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="57469-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="57469-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="57469-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="57469-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="57469-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="57469-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="57469-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="57469-110">API description</span></span>
<span data-ttu-id="57469-111">Récupère une collection [d’ordinateurs](machine.md) associés à un hachage de fichier donné.</span><span class="sxs-lookup"><span data-stu-id="57469-111">Retrieves a collection of [Machines](machine.md) related to a given file hash.</span></span>


## <a name="limitations"></a><span data-ttu-id="57469-112">Limites</span><span class="sxs-lookup"><span data-stu-id="57469-112">Limitations</span></span>
1. <span data-ttu-id="57469-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="57469-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="57469-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="57469-114">Permissions</span></span>
<span data-ttu-id="57469-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="57469-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="57469-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="57469-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="57469-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="57469-117">Permission type</span></span> |   <span data-ttu-id="57469-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="57469-118">Permission</span></span>  |   <span data-ttu-id="57469-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="57469-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="57469-120">Application</span><span class="sxs-lookup"><span data-stu-id="57469-120">Application</span></span> |   <span data-ttu-id="57469-121">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="57469-121">Machine.Read.All</span></span> |  <span data-ttu-id="57469-122">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="57469-122">'Read all machine profiles'</span></span>
<span data-ttu-id="57469-123">Application</span><span class="sxs-lookup"><span data-stu-id="57469-123">Application</span></span> |   <span data-ttu-id="57469-124">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="57469-124">Machine.ReadWrite.All</span></span> | <span data-ttu-id="57469-125">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="57469-125">'Read and write all machine information'</span></span>
<span data-ttu-id="57469-126">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="57469-126">Delegated (work or school account)</span></span> | <span data-ttu-id="57469-127">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="57469-127">Machine.Read</span></span> | <span data-ttu-id="57469-128">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="57469-128">'Read machine information'</span></span>
<span data-ttu-id="57469-129">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="57469-129">Delegated (work or school account)</span></span> | <span data-ttu-id="57469-130">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="57469-130">Machine.ReadWrite</span></span> | <span data-ttu-id="57469-131">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="57469-131">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="57469-132">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="57469-132">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="57469-133">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="57469-133">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="57469-134">La réponse inclut uniquement les appareils, accessibles par l’utilisateur, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="57469-134">Response will include only devices, that the user have access to, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="57469-135">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="57469-135">HTTP request</span></span>
```
GET /api/files/{id}/machines
```

## <a name="request-headers"></a><span data-ttu-id="57469-136">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="57469-136">Request headers</span></span>

<span data-ttu-id="57469-137">Nom</span><span class="sxs-lookup"><span data-stu-id="57469-137">Name</span></span> | <span data-ttu-id="57469-138">Type</span><span class="sxs-lookup"><span data-stu-id="57469-138">Type</span></span> | <span data-ttu-id="57469-139">Description</span><span class="sxs-lookup"><span data-stu-id="57469-139">Description</span></span>
:---|:---|:---
<span data-ttu-id="57469-140">Autorisation</span><span class="sxs-lookup"><span data-stu-id="57469-140">Authorization</span></span> | <span data-ttu-id="57469-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="57469-141">String</span></span> | <span data-ttu-id="57469-142">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="57469-142">Bearer {token}.</span></span> <span data-ttu-id="57469-143">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="57469-143">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="57469-144">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="57469-144">Request body</span></span>
<span data-ttu-id="57469-145">Vide</span><span class="sxs-lookup"><span data-stu-id="57469-145">Empty</span></span>

## <a name="response"></a><span data-ttu-id="57469-146">Réponse</span><span class="sxs-lookup"><span data-stu-id="57469-146">Response</span></span>
<span data-ttu-id="57469-147">En cas de réussite et si le fichier existe : 200 - OK avec la liste des entités [de l’ordinateur](machine.md) dans le corps.</span><span class="sxs-lookup"><span data-stu-id="57469-147">If successful and file exists - 200 OK with list of [machine](machine.md) entities in the body.</span></span> <span data-ttu-id="57469-148">Si le fichier n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="57469-148">If file does not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="57469-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="57469-149">Example</span></span>

<span data-ttu-id="57469-150">**Demande**</span><span class="sxs-lookup"><span data-stu-id="57469-150">**Request**</span></span>

<span data-ttu-id="57469-151">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="57469-151">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/files/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/machines
```
