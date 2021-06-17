---
title: API mettre à jour l’entité de l’ordinateur
description: Découvrez comment mettre à jour des balises d’ordinateur à l’aide de cette API. Vous pouvez mettre à jour les balises et les propriétés devicevalue.
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 8f08b1fdafd653561ac2aae10a73f37b21874b59
ms.sourcegitcommit: 34c06715e036255faa75c66ebf95c12a85f8ef42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "52985629"
---
# <a name="update-machine"></a><span data-ttu-id="ed36f-105">Mettre à jour l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ed36f-105">Update machine</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ed36f-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ed36f-106">**Applies to:**</span></span>
- [<span data-ttu-id="ed36f-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ed36f-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="ed36f-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ed36f-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="ed36f-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ed36f-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="ed36f-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ed36f-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="ed36f-111">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="ed36f-111">API description</span></span>
<span data-ttu-id="ed36f-112">Met à jour les propriétés de l’ordinateur [existant.](machine.md)</span><span class="sxs-lookup"><span data-stu-id="ed36f-112">Updates properties of existing [Machine](machine.md).</span></span>
<br><span data-ttu-id="ed36f-113">Les propriétés qui peuvent être mis à jour sont : ```machineTags``` et ```deviceValue``` .</span><span class="sxs-lookup"><span data-stu-id="ed36f-113">Updatable properties are: ```machineTags``` and ```deviceValue```.</span></span>


## <a name="limitations"></a><span data-ttu-id="ed36f-114">Limites</span><span class="sxs-lookup"><span data-stu-id="ed36f-114">Limitations</span></span>
1. <span data-ttu-id="ed36f-115">Vous pouvez mettre à jour les ordinateurs disponibles dans l’API.</span><span class="sxs-lookup"><span data-stu-id="ed36f-115">You can update machines that are available in the API.</span></span> 
2. <span data-ttu-id="ed36f-116">L’ordinateur de mise à jour n’appende que les balises à la collection de balises.</span><span class="sxs-lookup"><span data-stu-id="ed36f-116">Update machine only appends tags to the tag collection.</span></span> <span data-ttu-id="ed36f-117">S’il existe des balises, elles doivent être incluses dans la collection de balises dans le corps.</span><span class="sxs-lookup"><span data-stu-id="ed36f-117">If tags exist, they must be included in the tags collection in the body.</span></span>
3. <span data-ttu-id="ed36f-118">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="ed36f-118">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="ed36f-119">Autorisations</span><span class="sxs-lookup"><span data-stu-id="ed36f-119">Permissions</span></span>
<span data-ttu-id="ed36f-120">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="ed36f-120">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="ed36f-121">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="ed36f-121">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="ed36f-122">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="ed36f-122">Permission type</span></span> |   <span data-ttu-id="ed36f-123">Autorisation</span><span class="sxs-lookup"><span data-stu-id="ed36f-123">Permission</span></span>  |   <span data-ttu-id="ed36f-124">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="ed36f-124">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="ed36f-125">Application</span><span class="sxs-lookup"><span data-stu-id="ed36f-125">Application</span></span> |   <span data-ttu-id="ed36f-126">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed36f-126">Machine.ReadWrite.All</span></span> | <span data-ttu-id="ed36f-127">« Lire et écrire des informations sur l’ordinateur pour tous les ordinateurs »</span><span class="sxs-lookup"><span data-stu-id="ed36f-127">'Read and write machine information for all machines'</span></span>
<span data-ttu-id="ed36f-128">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="ed36f-128">Delegated (work or school account)</span></span> | <span data-ttu-id="ed36f-129">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ed36f-129">Machine.ReadWrite</span></span> | <span data-ttu-id="ed36f-130">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="ed36f-130">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="ed36f-131">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="ed36f-131">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="ed36f-132">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Investigation des alertes ».</span><span class="sxs-lookup"><span data-stu-id="ed36f-132">The user needs to have at least the following role permission: 'Alerts investigation'.</span></span> <span data-ttu-id="ed36f-133">Pour plus d’informations, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="ed36f-133">For more information, see [Create and manage roles](user-roles.md).</span></span>
>- <span data-ttu-id="ed36f-134">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="ed36f-134">The user needs to have access to the device associated with the alert, based on device group settings.</span></span> <span data-ttu-id="ed36f-135">Pour plus d’informations, voir [Créer et gérer des groupes d’appareils.](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="ed36f-135">For more information, see [Create and manage device groups](machine-groups.md).</span></span>

## <a name="http-request"></a><span data-ttu-id="ed36f-136">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="ed36f-136">HTTP request</span></span>
```
PATCH /api/machines/{machineId}
```

## <a name="request-headers"></a><span data-ttu-id="ed36f-137">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="ed36f-137">Request headers</span></span>

<span data-ttu-id="ed36f-138">Nom</span><span class="sxs-lookup"><span data-stu-id="ed36f-138">Name</span></span> | <span data-ttu-id="ed36f-139">Type</span><span class="sxs-lookup"><span data-stu-id="ed36f-139">Type</span></span> | <span data-ttu-id="ed36f-140">Description</span><span class="sxs-lookup"><span data-stu-id="ed36f-140">Description</span></span>
:---|:---|:---
<span data-ttu-id="ed36f-141">Autorisation</span><span class="sxs-lookup"><span data-stu-id="ed36f-141">Authorization</span></span> | <span data-ttu-id="ed36f-142">String</span><span class="sxs-lookup"><span data-stu-id="ed36f-142">String</span></span> | <span data-ttu-id="ed36f-143">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="ed36f-143">Bearer {token}.</span></span> <span data-ttu-id="ed36f-144">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="ed36f-144">**Required**.</span></span>
<span data-ttu-id="ed36f-145">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ed36f-145">Content-Type</span></span> | <span data-ttu-id="ed36f-146">String</span><span class="sxs-lookup"><span data-stu-id="ed36f-146">String</span></span> | <span data-ttu-id="ed36f-147">application/json.</span><span class="sxs-lookup"><span data-stu-id="ed36f-147">application/json.</span></span> <span data-ttu-id="ed36f-148">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="ed36f-148">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="ed36f-149">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="ed36f-149">Request body</span></span>
<span data-ttu-id="ed36f-150">Dans le corps de la demande, fournissons les valeurs des champs appropriés qui doivent être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="ed36f-150">In the request body, supply the values for the relevant fields that should be updated.</span></span>
<br><span data-ttu-id="ed36f-151">Les propriétés existantes qui ne sont pas incluses dans le corps de la demande conserveront leurs valeurs précédentes ou seront recalculées en fonction des modifications apportées à d’autres valeurs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="ed36f-151">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> 
<br><span data-ttu-id="ed36f-152">Pour de meilleures performances, vous ne devez pas inclure de valeurs existantes qui n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="ed36f-152">For best performance, you shouldn't include existing values that haven't change.</span></span>

<span data-ttu-id="ed36f-153">Propriété</span><span class="sxs-lookup"><span data-stu-id="ed36f-153">Property</span></span> | <span data-ttu-id="ed36f-154">Type</span><span class="sxs-lookup"><span data-stu-id="ed36f-154">Type</span></span> | <span data-ttu-id="ed36f-155">Description</span><span class="sxs-lookup"><span data-stu-id="ed36f-155">Description</span></span>
:---|:---|:---
<span data-ttu-id="ed36f-156">machineTags</span><span class="sxs-lookup"><span data-stu-id="ed36f-156">machineTags</span></span> | <span data-ttu-id="ed36f-157">String collection</span><span class="sxs-lookup"><span data-stu-id="ed36f-157">String collection</span></span> | <span data-ttu-id="ed36f-158">Ensemble de [balises d’ordinateur.](machine.md)</span><span class="sxs-lookup"><span data-stu-id="ed36f-158">Set of [machine](machine.md) tags.</span></span>
<span data-ttu-id="ed36f-159">deviceValue</span><span class="sxs-lookup"><span data-stu-id="ed36f-159">deviceValue</span></span> | <span data-ttu-id="ed36f-160">Nullable, enum</span><span class="sxs-lookup"><span data-stu-id="ed36f-160">Nullable Enum</span></span> | <span data-ttu-id="ed36f-161">Valeur [de l’appareil.](tvm-assign-device-value.md)</span><span class="sxs-lookup"><span data-stu-id="ed36f-161">The [value of the device](tvm-assign-device-value.md).</span></span> <span data-ttu-id="ed36f-162">Les valeurs possibles sont : « Normal » (normal), « Low » (faible) et « High » (élevé).</span><span class="sxs-lookup"><span data-stu-id="ed36f-162">Possible values are: 'Normal', 'Low' and 'High'.</span></span>

## <a name="response"></a><span data-ttu-id="ed36f-163">Réponse</span><span class="sxs-lookup"><span data-stu-id="ed36f-163">Response</span></span>
<span data-ttu-id="ed36f-164">Si elle réussit, cette méthode renvoie 200 OK et l’entité [de l’ordinateur](machine.md) dans le corps de la réponse avec les propriétés mises à jour.</span><span class="sxs-lookup"><span data-stu-id="ed36f-164">If successful, this method returns 200 OK, and the [machine](machine.md) entity in the response body with the updated properties.</span></span> <span data-ttu-id="ed36f-165">Si la collection de balises de l’ordinateur dans le corps ne contient pas de balises d’ordinateur existantes - 400 Entrée non valide et un message informant les balises manquantes.</span><span class="sxs-lookup"><span data-stu-id="ed36f-165">If machine tags collection in body doesn't contain existing machine tags - 400 Invalid Input and a message informing of the missing tag/s.</span></span>
<span data-ttu-id="ed36f-166">Si l’ordinateur avec l’ID spécifié est in trouvé - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="ed36f-166">If machine with the specified ID was not found - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="ed36f-167">Exemple</span><span class="sxs-lookup"><span data-stu-id="ed36f-167">Example</span></span>

<span data-ttu-id="ed36f-168">**Demande**</span><span class="sxs-lookup"><span data-stu-id="ed36f-168">**Request**</span></span>

<span data-ttu-id="ed36f-169">Voici un exemple de la demande.</span><span class="sxs-lookup"><span data-stu-id="ed36f-169">Here's an example of the request.</span></span>

```http
PATCH https://api.securitycenter.microsoft.com/api/machines/{machineId}
```

```json
{
    "deviceValue": "Normal",
    "machineTags": [
                     "Demo Device",
                     "Generic User Machine - Attack Source",
                     "Windows 10",
                     "Windows Insider - Fast"
    ]
}
```
