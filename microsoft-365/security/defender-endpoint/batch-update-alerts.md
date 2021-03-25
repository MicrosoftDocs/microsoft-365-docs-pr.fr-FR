---
title: API des entités d’alerte de mise à jour par lot
description: Découvrez comment mettre à jour les alertes Microsoft Defender pour les points de terminaison dans un lot à l’aide de cette API. Vous pouvez mettre à jour l’état, la détermination, la classification et les propriétés assignedTo.
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
ms.technology: mde
ms.openlocfilehash: db745c1b12c64baff5bf2c0a212446ce0f773709
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166683"
---
# <a name="batch-update-alerts"></a><span data-ttu-id="8a328-105">Alertes de mise à jour par lot</span><span class="sxs-lookup"><span data-stu-id="8a328-105">Batch update alerts</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="8a328-106">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="8a328-106">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2154037)</span></span>

- <span data-ttu-id="8a328-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="8a328-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="8a328-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="8a328-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="8a328-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="8a328-109">API description</span></span>
<span data-ttu-id="8a328-110">Met à jour les propriétés d’un lot d’alertes [existantes.](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="8a328-110">Updates properties of a batch of existing [Alerts](alerts.md).</span></span>
<br><span data-ttu-id="8a328-111">L’envoi **de commentaire** est disponible avec ou sans mise à jour des propriétés.</span><span class="sxs-lookup"><span data-stu-id="8a328-111">Submission of **comment** is available with or without updating properties.</span></span>
<br><span data-ttu-id="8a328-112">Les propriétés updatables `status` sont : , et `determination` `classification` `assignedTo` .</span><span class="sxs-lookup"><span data-stu-id="8a328-112">Updatable properties are: `status`, `determination`, `classification` and `assignedTo`.</span></span>


## <a name="limitations"></a><span data-ttu-id="8a328-113">Limites</span><span class="sxs-lookup"><span data-stu-id="8a328-113">Limitations</span></span>
1. <span data-ttu-id="8a328-114">Vous pouvez mettre à jour les alertes disponibles dans l’API.</span><span class="sxs-lookup"><span data-stu-id="8a328-114">You can update alerts that are available in the API.</span></span> <span data-ttu-id="8a328-115">Pour plus [d’informations, voir Alertes](get-alerts.md) de liste.</span><span class="sxs-lookup"><span data-stu-id="8a328-115">See [List Alerts](get-alerts.md) for more information.</span></span>
2. <span data-ttu-id="8a328-116">Les limites de taux pour cette API sont de 10 appels par minute et de 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="8a328-116">Rate limitations for this API are 10 calls per minute and 500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="8a328-117">Autorisations</span><span class="sxs-lookup"><span data-stu-id="8a328-117">Permissions</span></span>
<span data-ttu-id="8a328-118">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="8a328-118">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="8a328-119">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="8a328-119">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="8a328-120">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="8a328-120">Permission type</span></span> |   <span data-ttu-id="8a328-121">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8a328-121">Permission</span></span>  |   <span data-ttu-id="8a328-122">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="8a328-122">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="8a328-123">Application</span><span class="sxs-lookup"><span data-stu-id="8a328-123">Application</span></span> |   <span data-ttu-id="8a328-124">Alerts.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8a328-124">Alerts.ReadWrite.All</span></span> |  <span data-ttu-id="8a328-125">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="8a328-125">'Read and write all alerts'</span></span>
<span data-ttu-id="8a328-126">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="8a328-126">Delegated (work or school account)</span></span> | <span data-ttu-id="8a328-127">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a328-127">Alert.ReadWrite</span></span> | <span data-ttu-id="8a328-128">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="8a328-128">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="8a328-129">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="8a328-129">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="8a328-130">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Enquête sur les alertes » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="8a328-130">The user needs to have at least the following role permission: 'Alerts investigation' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="8a328-131">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="8a328-131">The user needs to have access to the device associated with the alert, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="8a328-132">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="8a328-132">HTTP request</span></span>
```http
POST /api/alerts/batchUpdate
```

## <a name="request-headers"></a><span data-ttu-id="8a328-133">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="8a328-133">Request headers</span></span>

<span data-ttu-id="8a328-134">Nom</span><span class="sxs-lookup"><span data-stu-id="8a328-134">Name</span></span> | <span data-ttu-id="8a328-135">Type</span><span class="sxs-lookup"><span data-stu-id="8a328-135">Type</span></span> | <span data-ttu-id="8a328-136">Description</span><span class="sxs-lookup"><span data-stu-id="8a328-136">Description</span></span>
:---|:---|:---
<span data-ttu-id="8a328-137">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8a328-137">Authorization</span></span> | <span data-ttu-id="8a328-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a328-138">String</span></span> | <span data-ttu-id="8a328-139">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="8a328-139">Bearer {token}.</span></span> <span data-ttu-id="8a328-140">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="8a328-140">**Required**.</span></span>
<span data-ttu-id="8a328-141">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8a328-141">Content-Type</span></span> | <span data-ttu-id="8a328-142">String</span><span class="sxs-lookup"><span data-stu-id="8a328-142">String</span></span> | <span data-ttu-id="8a328-143">application/json.</span><span class="sxs-lookup"><span data-stu-id="8a328-143">application/json.</span></span> <span data-ttu-id="8a328-144">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="8a328-144">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="8a328-145">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="8a328-145">Request body</span></span>
<span data-ttu-id="8a328-146">Dans le corps de la demande, fournissez les ID des alertes à mettre à jour et les valeurs des champs pertinents que vous souhaitez mettre à jour pour ces alertes.</span><span class="sxs-lookup"><span data-stu-id="8a328-146">In the request body, supply the IDs of the alerts to be updated and the values of the relevant fields that you wish to update for these alerts.</span></span>
<br><span data-ttu-id="8a328-147">Les propriétés existantes qui ne sont pas incluses dans le corps de la demande conserveront leurs valeurs précédentes ou seront recalculées en fonction des modifications apportées à d’autres valeurs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="8a328-147">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> 
<br><span data-ttu-id="8a328-148">Pour de meilleures performances, n’incluez pas de valeurs existantes qui n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="8a328-148">For best performance you shouldn't include existing values that haven't changed.</span></span>

<span data-ttu-id="8a328-149">Propriété</span><span class="sxs-lookup"><span data-stu-id="8a328-149">Property</span></span> | <span data-ttu-id="8a328-150">Type</span><span class="sxs-lookup"><span data-stu-id="8a328-150">Type</span></span> | <span data-ttu-id="8a328-151">Description</span><span class="sxs-lookup"><span data-stu-id="8a328-151">Description</span></span>
:---|:---|:---
<span data-ttu-id="8a328-152">alertIds</span><span class="sxs-lookup"><span data-stu-id="8a328-152">alertIds</span></span> | <span data-ttu-id="8a328-153">Chaîne de &lt; liste&gt;</span><span class="sxs-lookup"><span data-stu-id="8a328-153">List&lt;String&gt;</span></span>| <span data-ttu-id="8a328-154">Liste des ID des alertes à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="8a328-154">A list of the IDs of the alerts to be updated.</span></span> <span data-ttu-id="8a328-155">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8a328-155">**Required**</span></span>
<span data-ttu-id="8a328-156">status</span><span class="sxs-lookup"><span data-stu-id="8a328-156">status</span></span> | <span data-ttu-id="8a328-157">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a328-157">String</span></span> | <span data-ttu-id="8a328-158">Spécifie l’état mis à jour des alertes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8a328-158">Specifies the updated status of the specified alerts.</span></span> <span data-ttu-id="8a328-159">Les valeurs des propriétés sont : « New » (nouveau), « InProgress » (InProgress) et « Resolved » (résolu).</span><span class="sxs-lookup"><span data-stu-id="8a328-159">The property values are: 'New', 'InProgress' and 'Resolved'.</span></span>
<span data-ttu-id="8a328-160">assignedTo</span><span class="sxs-lookup"><span data-stu-id="8a328-160">assignedTo</span></span> | <span data-ttu-id="8a328-161">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a328-161">String</span></span> | <span data-ttu-id="8a328-162">Propriétaire des alertes spécifiées</span><span class="sxs-lookup"><span data-stu-id="8a328-162">Owner of the specified alerts</span></span>
<span data-ttu-id="8a328-163">classification</span><span class="sxs-lookup"><span data-stu-id="8a328-163">classification</span></span> | <span data-ttu-id="8a328-164">String</span><span class="sxs-lookup"><span data-stu-id="8a328-164">String</span></span> | <span data-ttu-id="8a328-165">Spécifie la spécification des alertes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8a328-165">Specifies the specification of the specified alerts.</span></span> <span data-ttu-id="8a328-166">Les valeurs de propriété sont : « Unknown » (inconnu), « FalsePositive » (fauxpositif), « TruePositive » (vraipositif).</span><span class="sxs-lookup"><span data-stu-id="8a328-166">The property values are: 'Unknown', 'FalsePositive', 'TruePositive'.</span></span> 
<span data-ttu-id="8a328-167">détermination</span><span class="sxs-lookup"><span data-stu-id="8a328-167">determination</span></span> | <span data-ttu-id="8a328-168">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a328-168">String</span></span> | <span data-ttu-id="8a328-169">Spécifie la détermination des alertes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8a328-169">Specifies the determination of the specified alerts.</span></span> <span data-ttu-id="8a328-170">Les valeurs de propriété sont : 'NotAvailable', 'Apt', 'Malware', 'SecurityPersonnel', 'SecurityTesting', 'UnwantedSoftware', 'Other'</span><span class="sxs-lookup"><span data-stu-id="8a328-170">The property values are: 'NotAvailable', 'Apt', 'Malware', 'SecurityPersonnel', 'SecurityTesting', 'UnwantedSoftware', 'Other'</span></span>
<span data-ttu-id="8a328-171">comment</span><span class="sxs-lookup"><span data-stu-id="8a328-171">comment</span></span> | <span data-ttu-id="8a328-172">String</span><span class="sxs-lookup"><span data-stu-id="8a328-172">String</span></span> | <span data-ttu-id="8a328-173">Commentaire à ajouter aux alertes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8a328-173">Comment to be added to the specified alerts.</span></span>

## <a name="response"></a><span data-ttu-id="8a328-174">Réponse</span><span class="sxs-lookup"><span data-stu-id="8a328-174">Response</span></span>
<span data-ttu-id="8a328-175">Si elle réussit, cette méthode renvoie 200 OK, avec un corps de réponse vide.</span><span class="sxs-lookup"><span data-stu-id="8a328-175">If successful, this method returns 200 OK, with an empty response body.</span></span>


## <a name="example"></a><span data-ttu-id="8a328-176">Exemple</span><span class="sxs-lookup"><span data-stu-id="8a328-176">Example</span></span>

<span data-ttu-id="8a328-177">**Demande**</span><span class="sxs-lookup"><span data-stu-id="8a328-177">**Request**</span></span>

<span data-ttu-id="8a328-178">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="8a328-178">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/alerts/batchUpdate
```

```json
{
    "alertIds": ["da637399794050273582_760707377", "da637399989469816469_51697947354"],
    "status": "Resolved",
    "assignedTo": "secop2@contoso.com",
    "classification": "FalsePositive",
    "determination": "Malware",
    "comment": "Resolve my alert and assign to secop2"
}
```
