---
title: API d’entité d’alerte de mise à jour
description: Découvrez comment mettre à jour une alerte Microsoft Defender pour le point de terminaison à l’aide de cette API. Vous pouvez mettre à jour l’état, la détermination, la classification et les propriétés assignedTo.
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
ms.openlocfilehash: 043d423e1016d77cad4a175aa41718329f464252
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52768923"
---
# <a name="update-alert"></a><span data-ttu-id="2cb3a-105">Mettre à jour une alerte</span><span class="sxs-lookup"><span data-stu-id="2cb3a-105">Update alert</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2cb3a-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2cb3a-106">**Applies to:**</span></span>
- [<span data-ttu-id="2cb3a-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2cb3a-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="2cb3a-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2cb3a-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="2cb3a-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2cb3a-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="2cb3a-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="2cb3a-111">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="2cb3a-111">API description</span></span>
<span data-ttu-id="2cb3a-112">Met à jour les propriétés de l’alerte [existante.](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="2cb3a-112">Updates properties of existing [Alert](alerts.md).</span></span>
<br><span data-ttu-id="2cb3a-113">L’envoi **de commentaire** est disponible avec ou sans mise à jour des propriétés.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-113">Submission of **comment** is available with or without updating properties.</span></span>
<br><span data-ttu-id="2cb3a-114">Les propriétés updatables ```status``` sont : , et ```determination``` ```classification``` ```assignedTo``` .</span><span class="sxs-lookup"><span data-stu-id="2cb3a-114">Updatable properties are: ```status```, ```determination```, ```classification``` and ```assignedTo```.</span></span>


## <a name="limitations"></a><span data-ttu-id="2cb3a-115">Limites</span><span class="sxs-lookup"><span data-stu-id="2cb3a-115">Limitations</span></span>
1. <span data-ttu-id="2cb3a-116">Vous pouvez mettre à jour les alertes disponibles dans l’API.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-116">You can update alerts that available in the API.</span></span> <span data-ttu-id="2cb3a-117">Pour plus [d’informations, voir Alertes](get-alerts.md) de liste.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-117">See [List Alerts](get-alerts.md) for more information.</span></span>
2. <span data-ttu-id="2cb3a-118">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-118">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="2cb3a-119">Autorisations</span><span class="sxs-lookup"><span data-stu-id="2cb3a-119">Permissions</span></span>
<span data-ttu-id="2cb3a-120">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-120">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="2cb3a-121">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="2cb3a-121">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="2cb3a-122">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="2cb3a-122">Permission type</span></span> |   <span data-ttu-id="2cb3a-123">Autorisation</span><span class="sxs-lookup"><span data-stu-id="2cb3a-123">Permission</span></span>  |   <span data-ttu-id="2cb3a-124">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="2cb3a-124">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="2cb3a-125">Application</span><span class="sxs-lookup"><span data-stu-id="2cb3a-125">Application</span></span> |   <span data-ttu-id="2cb3a-126">Alerts.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cb3a-126">Alerts.ReadWrite.All</span></span> |  <span data-ttu-id="2cb3a-127">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="2cb3a-127">'Read and write all alerts'</span></span>
<span data-ttu-id="2cb3a-128">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="2cb3a-128">Delegated (work or school account)</span></span> | <span data-ttu-id="2cb3a-129">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2cb3a-129">Alert.ReadWrite</span></span> | <span data-ttu-id="2cb3a-130">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="2cb3a-130">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="2cb3a-131">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="2cb3a-131">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="2cb3a-132">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Enquête sur les alertes » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="2cb3a-132">The user needs to have at least the following role permission: 'Alerts investigation' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="2cb3a-133">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils (pour plus d’informations, voir Créer et gérer des groupes d’appareils) [](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="2cb3a-133">The user needs to have access to the device associated with the alert, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="2cb3a-134">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="2cb3a-134">HTTP request</span></span>
```
PATCH /api/alerts/{id}
```

## <a name="request-headers"></a><span data-ttu-id="2cb3a-135">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="2cb3a-135">Request headers</span></span>

<span data-ttu-id="2cb3a-136">Nom</span><span class="sxs-lookup"><span data-stu-id="2cb3a-136">Name</span></span> | <span data-ttu-id="2cb3a-137">Type</span><span class="sxs-lookup"><span data-stu-id="2cb3a-137">Type</span></span> | <span data-ttu-id="2cb3a-138">Description</span><span class="sxs-lookup"><span data-stu-id="2cb3a-138">Description</span></span>
:---|:---|:---
<span data-ttu-id="2cb3a-139">Autorisation</span><span class="sxs-lookup"><span data-stu-id="2cb3a-139">Authorization</span></span> | <span data-ttu-id="2cb3a-140">String</span><span class="sxs-lookup"><span data-stu-id="2cb3a-140">String</span></span> | <span data-ttu-id="2cb3a-141">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-141">Bearer {token}.</span></span> <span data-ttu-id="2cb3a-142">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-142">**Required**.</span></span>
<span data-ttu-id="2cb3a-143">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2cb3a-143">Content-Type</span></span> | <span data-ttu-id="2cb3a-144">String</span><span class="sxs-lookup"><span data-stu-id="2cb3a-144">String</span></span> | <span data-ttu-id="2cb3a-145">application/json.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-145">application/json.</span></span> <span data-ttu-id="2cb3a-146">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-146">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="2cb3a-147">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="2cb3a-147">Request body</span></span>
<span data-ttu-id="2cb3a-148">Dans le corps de la demande, fournissons les valeurs des champs appropriés qui doivent être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-148">In the request body, supply the values for the relevant fields that should be updated.</span></span>
<br><span data-ttu-id="2cb3a-149">Les propriétés existantes qui ne sont pas incluses dans le corps de la demande conserveront leurs valeurs précédentes ou seront recalculées en fonction des modifications apportées à d’autres valeurs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-149">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> 
<br><span data-ttu-id="2cb3a-150">Pour de meilleures performances, n’incluez pas de valeurs existantes qui n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-150">For best performance you shouldn't include existing values that haven't change.</span></span>

<span data-ttu-id="2cb3a-151">Propriété</span><span class="sxs-lookup"><span data-stu-id="2cb3a-151">Property</span></span> | <span data-ttu-id="2cb3a-152">Type</span><span class="sxs-lookup"><span data-stu-id="2cb3a-152">Type</span></span> | <span data-ttu-id="2cb3a-153">Description</span><span class="sxs-lookup"><span data-stu-id="2cb3a-153">Description</span></span>
:---|:---|:---
<span data-ttu-id="2cb3a-154">status</span><span class="sxs-lookup"><span data-stu-id="2cb3a-154">status</span></span> | <span data-ttu-id="2cb3a-155">String</span><span class="sxs-lookup"><span data-stu-id="2cb3a-155">String</span></span> | <span data-ttu-id="2cb3a-156">Spécifie l’état actuel de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-156">Specifies the current status of the alert.</span></span> <span data-ttu-id="2cb3a-157">Les valeurs des propriétés sont : « New » (nouveau), « InProgress » (InProgress) et « Resolved » (résolu).</span><span class="sxs-lookup"><span data-stu-id="2cb3a-157">The property values are: 'New', 'InProgress' and 'Resolved'.</span></span>
<span data-ttu-id="2cb3a-158">assignedTo</span><span class="sxs-lookup"><span data-stu-id="2cb3a-158">assignedTo</span></span> | <span data-ttu-id="2cb3a-159">String</span><span class="sxs-lookup"><span data-stu-id="2cb3a-159">String</span></span> | <span data-ttu-id="2cb3a-160">Propriétaire de l’alerte</span><span class="sxs-lookup"><span data-stu-id="2cb3a-160">Owner of the alert</span></span>
<span data-ttu-id="2cb3a-161">classification</span><span class="sxs-lookup"><span data-stu-id="2cb3a-161">classification</span></span> | <span data-ttu-id="2cb3a-162">String</span><span class="sxs-lookup"><span data-stu-id="2cb3a-162">String</span></span> | <span data-ttu-id="2cb3a-163">Spécifie la spécification de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-163">Specifies the specification of the alert.</span></span> <span data-ttu-id="2cb3a-164">Les valeurs de propriété sont : « Unknown » (inconnu), « FalsePositive » (fauxpositif), « TruePositive » (vraipositif).</span><span class="sxs-lookup"><span data-stu-id="2cb3a-164">The property values are: 'Unknown', 'FalsePositive', 'TruePositive'.</span></span> 
<span data-ttu-id="2cb3a-165">détermination</span><span class="sxs-lookup"><span data-stu-id="2cb3a-165">determination</span></span> | <span data-ttu-id="2cb3a-166">String</span><span class="sxs-lookup"><span data-stu-id="2cb3a-166">String</span></span> | <span data-ttu-id="2cb3a-167">Spécifie la détermination de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-167">Specifies the determination of the alert.</span></span> <span data-ttu-id="2cb3a-168">Les valeurs de propriété sont : 'NotAvailable', 'Apt', 'Malware', 'SecurityPersonnel', 'SecurityTesting', 'UnwantedSoftware', 'Other'</span><span class="sxs-lookup"><span data-stu-id="2cb3a-168">The property values are: 'NotAvailable', 'Apt', 'Malware', 'SecurityPersonnel', 'SecurityTesting', 'UnwantedSoftware', 'Other'</span></span>
<span data-ttu-id="2cb3a-169">comment</span><span class="sxs-lookup"><span data-stu-id="2cb3a-169">comment</span></span> | <span data-ttu-id="2cb3a-170">String</span><span class="sxs-lookup"><span data-stu-id="2cb3a-170">String</span></span> | <span data-ttu-id="2cb3a-171">Commentaire à ajouter à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-171">Comment to be added to the alert.</span></span>

## <a name="response"></a><span data-ttu-id="2cb3a-172">Réponse</span><span class="sxs-lookup"><span data-stu-id="2cb3a-172">Response</span></span>
<span data-ttu-id="2cb3a-173">Si elle réussit, cette méthode renvoie 200 OK et l’entité d’alerte dans le corps de la réponse avec les propriétés mises à jour. [](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="2cb3a-173">If successful, this method returns 200 OK, and the [alert](alerts.md) entity in the response body with the updated properties.</span></span> <span data-ttu-id="2cb3a-174">Si l’alerte avec l’ID spécifié est in trouvée - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-174">If alert with the specified id was not found - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="2cb3a-175">Exemple</span><span class="sxs-lookup"><span data-stu-id="2cb3a-175">Example</span></span>

<span data-ttu-id="2cb3a-176">**Demande**</span><span class="sxs-lookup"><span data-stu-id="2cb3a-176">**Request**</span></span>

<span data-ttu-id="2cb3a-177">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="2cb3a-177">Here is an example of the request.</span></span>

```http
PATCH https://api.securitycenter.microsoft.com/api/alerts/121688558380765161_2136280442
```

```json
{
    "status": "Resolved",
    "assignedTo": "secop2@contoso.com",
    "classification": "FalsePositive",
    "determination": "Malware",
    "comment": "Resolve my alert and assign to secop2"
}
```
