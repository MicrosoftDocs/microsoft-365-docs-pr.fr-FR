---
title: API Ajouter ou supprimer des balises d’ordinateur
description: Découvrez comment utiliser l’API Ajouter ou supprimer des balises d’ordinateur pour ajouter ou supprimer une balise pour un ordinateur dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, balises, balises d’ordinateur
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
ms.openlocfilehash: 3818fc0050790b2c3b307f95ee0760c516cbf893
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769820"
---
# <a name="add-or-remove-machine-tags-api"></a><span data-ttu-id="ae6ee-104">API Ajouter ou supprimer des balises d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ae6ee-104">Add or Remove Machine Tags API</span></span>

<span data-ttu-id="ae6ee-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ae6ee-105">**Applies to:**</span></span>

- [<span data-ttu-id="ae6ee-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ae6ee-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

> <span data-ttu-id="ae6ee-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ae6ee-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="ae6ee-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="ae6ee-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="ae6ee-109">API description</span></span>

<span data-ttu-id="ae6ee-110">Ajoute ou supprime une balise à un ordinateur [spécifique.](machine.md)</span><span class="sxs-lookup"><span data-stu-id="ae6ee-110">Adds or remove tag to a specific [Machine](machine.md).</span></span>

## <a name="limitations"></a><span data-ttu-id="ae6ee-111">Limites</span><span class="sxs-lookup"><span data-stu-id="ae6ee-111">Limitations</span></span>

1. <span data-ttu-id="ae6ee-112">Vous pouvez publier sur les ordinateurs pour la dernière fois en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-112">You can post on machines last seen according to your configured retention period.</span></span>

2. <span data-ttu-id="ae6ee-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="ae6ee-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="ae6ee-114">Permissions</span></span>

<span data-ttu-id="ae6ee-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="ae6ee-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="ae6ee-116">To learn more, including how to choose permissions, see [Use Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="ae6ee-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="ae6ee-117">Permission type</span></span> |    <span data-ttu-id="ae6ee-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="ae6ee-118">Permission</span></span>    |    <span data-ttu-id="ae6ee-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="ae6ee-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="ae6ee-120">Application</span><span class="sxs-lookup"><span data-stu-id="ae6ee-120">Application</span></span> |    <span data-ttu-id="ae6ee-121">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ae6ee-121">Machine.ReadWrite.All</span></span> |    <span data-ttu-id="ae6ee-122">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="ae6ee-122">'Read and write all machine information'</span></span>
<span data-ttu-id="ae6ee-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="ae6ee-123">Delegated (work or school account)</span></span> | <span data-ttu-id="ae6ee-124">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ae6ee-124">Machine.ReadWrite</span></span> | <span data-ttu-id="ae6ee-125">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="ae6ee-125">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="ae6ee-126">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="ae6ee-126">When obtaining a token using user credentials:</span></span>
>
>- <span data-ttu-id="ae6ee-127">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Gérer le paramètre de sécurité ».</span><span class="sxs-lookup"><span data-stu-id="ae6ee-127">The user needs to have at least the following role permission: 'Manage security setting'.</span></span> <span data-ttu-id="ae6ee-128">Pour plus d’informations ,voir [Créer et gérer des rôles](user-roles.md) pour plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="ae6ee-128">For more  (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="ae6ee-129">L’utilisateur doit avoir accès à l’ordinateur, en fonction des paramètres de groupe d’ordinateurs (voir Créer et gérer des groupes [d’ordinateurs](machine-groups.md) pour plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="ae6ee-129">User needs to have access to the machine, based on machine group settings (See [Create and manage machine groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="ae6ee-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="ae6ee-130">HTTP request</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/{id}/tags
```

## <a name="request-headers"></a><span data-ttu-id="ae6ee-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="ae6ee-131">Request headers</span></span>

<span data-ttu-id="ae6ee-132">Nom</span><span class="sxs-lookup"><span data-stu-id="ae6ee-132">Name</span></span> | <span data-ttu-id="ae6ee-133">Type</span><span class="sxs-lookup"><span data-stu-id="ae6ee-133">Type</span></span> | <span data-ttu-id="ae6ee-134">Description</span><span class="sxs-lookup"><span data-stu-id="ae6ee-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="ae6ee-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="ae6ee-135">Authorization</span></span> | <span data-ttu-id="ae6ee-136">String</span><span class="sxs-lookup"><span data-stu-id="ae6ee-136">String</span></span> | <span data-ttu-id="ae6ee-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-137">Bearer {token}.</span></span> <span data-ttu-id="ae6ee-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-138">**Required**.</span></span>
<span data-ttu-id="ae6ee-139">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ae6ee-139">Content-Type</span></span> | <span data-ttu-id="ae6ee-140">string</span><span class="sxs-lookup"><span data-stu-id="ae6ee-140">string</span></span> | <span data-ttu-id="ae6ee-141">application/json.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-141">application/json.</span></span> <span data-ttu-id="ae6ee-142">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-142">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="ae6ee-143">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="ae6ee-143">Request body</span></span>

<span data-ttu-id="ae6ee-144">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ae6ee-144">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="ae6ee-145">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ae6ee-145">Parameter</span></span> |    <span data-ttu-id="ae6ee-146">Type</span><span class="sxs-lookup"><span data-stu-id="ae6ee-146">Type</span></span>    | <span data-ttu-id="ae6ee-147">Description</span><span class="sxs-lookup"><span data-stu-id="ae6ee-147">Description</span></span>
:---|:---|:---
<span data-ttu-id="ae6ee-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae6ee-148">Value</span></span> |    <span data-ttu-id="ae6ee-149">String</span><span class="sxs-lookup"><span data-stu-id="ae6ee-149">String</span></span> |    <span data-ttu-id="ae6ee-150">Nom de la balise.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-150">The tag name.</span></span> <span data-ttu-id="ae6ee-151">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-151">**Required**.</span></span>
<span data-ttu-id="ae6ee-152">Action</span><span class="sxs-lookup"><span data-stu-id="ae6ee-152">Action</span></span>    | <span data-ttu-id="ae6ee-153">Énum</span><span class="sxs-lookup"><span data-stu-id="ae6ee-153">Enum</span></span> |    <span data-ttu-id="ae6ee-154">Ajouter ou supprimer.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-154">Add or Remove.</span></span> <span data-ttu-id="ae6ee-155">Les valeurs autorisées sont : « Ajouter » ou « Supprimer ».</span><span class="sxs-lookup"><span data-stu-id="ae6ee-155">Allowed values are: 'Add' or 'Remove'.</span></span> <span data-ttu-id="ae6ee-156">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-156">**Required**.</span></span>


## <a name="response"></a><span data-ttu-id="ae6ee-157">Réponse</span><span class="sxs-lookup"><span data-stu-id="ae6ee-157">Response</span></span>

<span data-ttu-id="ae6ee-158">Si elle réussit, cette méthode renvoie le code de réponse 200 - OK et l’ordinateur mis à jour dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-158">If successful, this method returns 200 - Ok response code and the updated Machine in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ae6ee-159">Exemple</span><span class="sxs-lookup"><span data-stu-id="ae6ee-159">Example</span></span>

<span data-ttu-id="ae6ee-160">**Demande**</span><span class="sxs-lookup"><span data-stu-id="ae6ee-160">**Request**</span></span>

<span data-ttu-id="ae6ee-161">Voici un exemple de demande qui ajoute une balise d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-161">Here is an example of a request that adds machine tag.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/tags
```

```json
{
  "Value" : "test Tag 2",
  "Action": "Add"
}
```

- <span data-ttu-id="ae6ee-162">Pour supprimer la balise de l’ordinateur, définissez l’action sur « Supprimer » au lieu de « Ajouter » dans le corps de la demande.</span><span class="sxs-lookup"><span data-stu-id="ae6ee-162">To remove machine tag, set the Action to 'Remove' instead of 'Add' in the request body.</span></span>
