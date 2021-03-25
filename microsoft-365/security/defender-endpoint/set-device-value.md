---
title: API Définir la valeur de l’appareil
description: Découvrez comment spécifier la valeur d’un appareil à l’aide d’une API Microsoft Defender pour endpoint.
keywords: api, api de graphique, api pris en charge, balises, balises d’ordinateur
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: ellevin
author: levinec
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 33692ddf62153c0a6aa8f84568d69803af113bc6
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51185562"
---
# <a name="set-device-value-api"></a><span data-ttu-id="9ea50-104">API Définir la valeur de l’appareil</span><span class="sxs-lookup"><span data-stu-id="9ea50-104">Set device value API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9ea50-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9ea50-105">**Applies to:**</span></span>
- [<span data-ttu-id="9ea50-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9ea50-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="9ea50-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9ea50-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="9ea50-108">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="9ea50-108">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="9ea50-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="9ea50-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="9ea50-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9ea50-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="9ea50-111">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="9ea50-111">API description</span></span>

<span data-ttu-id="9ea50-112">Définissez la valeur d’appareil d’un [ordinateur spécifique.](machine.md)</span><span class="sxs-lookup"><span data-stu-id="9ea50-112">Set the device value of a specific [Machine](machine.md).</span></span><br>
<span data-ttu-id="9ea50-113">Pour plus [d’informations, voir](tvm-assign-device-value.md) attribuer des valeurs d’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ea50-113">See [assign device values](tvm-assign-device-value.md) for more information.</span></span>

## <a name="limitations"></a><span data-ttu-id="9ea50-114">Limites</span><span class="sxs-lookup"><span data-stu-id="9ea50-114">Limitations</span></span>

1. <span data-ttu-id="9ea50-115">Vous pouvez publier sur les appareils pour la dernière fois en fonction de votre période de rétention configurée.</span><span class="sxs-lookup"><span data-stu-id="9ea50-115">You can post on devices last seen according to your configured retention period.</span></span>

2. <span data-ttu-id="9ea50-116">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="9ea50-116">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="9ea50-117">Autorisations</span><span class="sxs-lookup"><span data-stu-id="9ea50-117">Permissions</span></span>

<span data-ttu-id="9ea50-118">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="9ea50-118">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="9ea50-119">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="9ea50-119">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="9ea50-120">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="9ea50-120">Permission type</span></span> |    <span data-ttu-id="9ea50-121">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9ea50-121">Permission</span></span>    |    <span data-ttu-id="9ea50-122">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="9ea50-122">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="9ea50-123">Application</span><span class="sxs-lookup"><span data-stu-id="9ea50-123">Application</span></span> |    <span data-ttu-id="9ea50-124">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9ea50-124">Machine.ReadWrite.All</span></span> |    <span data-ttu-id="9ea50-125">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="9ea50-125">'Read and write all machine information'</span></span>
<span data-ttu-id="9ea50-126">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="9ea50-126">Delegated (work or school account)</span></span> | <span data-ttu-id="9ea50-127">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9ea50-127">Machine.ReadWrite</span></span> | <span data-ttu-id="9ea50-128">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="9ea50-128">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="9ea50-129">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="9ea50-129">When obtaining a token using user credentials:</span></span>
>
>- <span data-ttu-id="9ea50-130">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Gérer le paramètre de sécurité ».</span><span class="sxs-lookup"><span data-stu-id="9ea50-130">The user needs to have at least the following role permission: 'Manage security setting'.</span></span> <span data-ttu-id="9ea50-131">Pour plus d’informations ,voir [Créer et gérer des rôles](user-roles.md) pour plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="9ea50-131">For more  (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="9ea50-132">L’utilisateur doit avoir accès à l’ordinateur, en fonction des paramètres de groupe d’ordinateurs (voir Créer et gérer des groupes [d’ordinateurs](machine-groups.md) pour plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="9ea50-132">User needs to have access to the machine, based on machine group settings (See [Create and manage machine groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="9ea50-133">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="9ea50-133">HTTP request</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/{machineId}/setDeviceValue
```

## <a name="request-headers"></a><span data-ttu-id="9ea50-134">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="9ea50-134">Request headers</span></span>

<span data-ttu-id="9ea50-135">Nom</span><span class="sxs-lookup"><span data-stu-id="9ea50-135">Name</span></span> | <span data-ttu-id="9ea50-136">Type</span><span class="sxs-lookup"><span data-stu-id="9ea50-136">Type</span></span> | <span data-ttu-id="9ea50-137">Description</span><span class="sxs-lookup"><span data-stu-id="9ea50-137">Description</span></span>
:---|:---|:---
<span data-ttu-id="9ea50-138">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9ea50-138">Authorization</span></span> | <span data-ttu-id="9ea50-139">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9ea50-139">String</span></span> | <span data-ttu-id="9ea50-140">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="9ea50-140">Bearer {token}.</span></span> <span data-ttu-id="9ea50-141">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="9ea50-141">**Required**.</span></span>
<span data-ttu-id="9ea50-142">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9ea50-142">Content-Type</span></span> | <span data-ttu-id="9ea50-143">string</span><span class="sxs-lookup"><span data-stu-id="9ea50-143">string</span></span> | <span data-ttu-id="9ea50-144">application/json.</span><span class="sxs-lookup"><span data-stu-id="9ea50-144">application/json.</span></span> <span data-ttu-id="9ea50-145">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="9ea50-145">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="9ea50-146">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="9ea50-146">Request body</span></span>

<span data-ttu-id="9ea50-147">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9ea50-147">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="9ea50-148">Paramètre</span><span class="sxs-lookup"><span data-stu-id="9ea50-148">Parameter</span></span> |    <span data-ttu-id="9ea50-149">Type</span><span class="sxs-lookup"><span data-stu-id="9ea50-149">Type</span></span>    | <span data-ttu-id="9ea50-150">Description</span><span class="sxs-lookup"><span data-stu-id="9ea50-150">Description</span></span>
:---|:---|:---
<span data-ttu-id="9ea50-151">DeviceValue</span><span class="sxs-lookup"><span data-stu-id="9ea50-151">DeviceValue</span></span> |    <span data-ttu-id="9ea50-152">Énum</span><span class="sxs-lookup"><span data-stu-id="9ea50-152">Enum</span></span> |    <span data-ttu-id="9ea50-153">Valeur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ea50-153">Device value.</span></span> <span data-ttu-id="9ea50-154">Les valeurs autorisées sont : « Normal » (normal), « Low » (faible) et « High » (élevé).</span><span class="sxs-lookup"><span data-stu-id="9ea50-154">Allowed values are: 'Normal', 'Low' and 'High'.</span></span> <span data-ttu-id="9ea50-155">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="9ea50-155">**Required**.</span></span>

## <a name="response"></a><span data-ttu-id="9ea50-156">Réponse</span><span class="sxs-lookup"><span data-stu-id="9ea50-156">Response</span></span>

<span data-ttu-id="9ea50-157">Si elle réussit, cette méthode renvoie le code de réponse 200 - OK et l’ordinateur mis à jour dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="9ea50-157">If successful, this method returns 200 - Ok response code and the updated Machine in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9ea50-158">Exemple</span><span class="sxs-lookup"><span data-stu-id="9ea50-158">Example</span></span>

<span data-ttu-id="9ea50-159">**Demande**</span><span class="sxs-lookup"><span data-stu-id="9ea50-159">**Request**</span></span>

<span data-ttu-id="9ea50-160">Voici un exemple de demande qui ajoute une balise d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9ea50-160">Here is an example of a request that adds machine tag.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/setDeviceValue
```

```json
{
  "DeviceValue" : "High"
}
```
