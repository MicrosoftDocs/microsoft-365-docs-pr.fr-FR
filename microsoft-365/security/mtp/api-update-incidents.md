---
title: API de mise à jour des incidents
description: Découvrez comment mettre à jour les incidents à l’aide de l’API Microsoft 365 Defender
keywords: mise à jour, API, incident
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: 3f77980863b0c232166d736a6b557444df98c8ac
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48844835"
---
# <a name="update-incidents-api"></a><span data-ttu-id="e4b66-104">API de mise à jour des incidents</span><span class="sxs-lookup"><span data-stu-id="e4b66-104">Update incidents API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="e4b66-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e4b66-105">**Applies to:**</span></span>
- <span data-ttu-id="e4b66-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e4b66-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT] 
><span data-ttu-id="e4b66-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="e4b66-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e4b66-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="e4b66-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


## <a name="api-description"></a><span data-ttu-id="e4b66-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="e4b66-109">API description</span></span>
<span data-ttu-id="e4b66-110">Met à jour les propriétés d’un incident existant.</span><span class="sxs-lookup"><span data-stu-id="e4b66-110">Updates properties of existing incident.</span></span>
<br><span data-ttu-id="e4b66-111">Les propriétés pouvant être mises à jour sont les suivantes : ```status``` , ```determination``` , ```classification``` ```assignedTo``` et ```tags``` .</span><span class="sxs-lookup"><span data-stu-id="e4b66-111">Updatable properties are: ```status```, ```determination```, ```classification```, ```assignedTo``` and ```tags```.</span></span>


## <a name="limitations"></a><span data-ttu-id="e4b66-112">Limites</span><span class="sxs-lookup"><span data-stu-id="e4b66-112">Limitations</span></span>
1. <span data-ttu-id="e4b66-113">Les limites de taux pour cette API sont 50 appels par minute et 1500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="e4b66-113">Rate limitations for this API are 50 calls per minute and 1500 calls per hour.</span></span>
2. <span data-ttu-id="e4b66-114">Vous ne pouvez définir la valeur ```determination``` que si la classification est définie sur TruePositive.</span><span class="sxs-lookup"><span data-stu-id="e4b66-114">You can set the ```determination``` only if the classification is set to TruePositive.</span></span>


## <a name="permissions"></a><span data-ttu-id="e4b66-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="e4b66-115">Permissions</span></span>
<span data-ttu-id="e4b66-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="e4b66-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="e4b66-117">Pour plus d’informations, notamment sur le choix des autorisations, consultez [la rubrique accéder aux API Microsoft 365 Defender](api-access.md).</span><span class="sxs-lookup"><span data-stu-id="e4b66-117">To learn more, including how to choose permissions, see [Access the Microsoft 365 Defender APIs](api-access.md).</span></span>

<span data-ttu-id="e4b66-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="e4b66-118">Permission type</span></span> |   <span data-ttu-id="e4b66-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e4b66-119">Permission</span></span>  |   <span data-ttu-id="e4b66-120">Nom d’affichage des autorisations</span><span class="sxs-lookup"><span data-stu-id="e4b66-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="e4b66-121">Application</span><span class="sxs-lookup"><span data-stu-id="e4b66-121">Application</span></span> |   <span data-ttu-id="e4b66-122">Incident. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="e4b66-122">Incident.ReadWrite.All</span></span> |    <span data-ttu-id="e4b66-123">« Lire et écrire tous les incidents »</span><span class="sxs-lookup"><span data-stu-id="e4b66-123">'Read and write all incidents'</span></span>
<span data-ttu-id="e4b66-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="e4b66-124">Delegated (work or school account)</span></span> | <span data-ttu-id="e4b66-125">Incident. ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4b66-125">Incident.ReadWrite</span></span> | <span data-ttu-id="e4b66-126">« Incidents en lecture et en écriture »</span><span class="sxs-lookup"><span data-stu-id="e4b66-126">'Read and write incidents'</span></span>

>[!NOTE]
> <span data-ttu-id="e4b66-127">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="e4b66-127">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="e4b66-128">L’utilisateur doit avoir l’autorisation de mettre à jour l’incident dans le portail.</span><span class="sxs-lookup"><span data-stu-id="e4b66-128">The user needs to have permission to update the incident in the portal.</span></span>


## <a name="http-request"></a><span data-ttu-id="e4b66-129">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="e4b66-129">HTTP request</span></span>

```
PATCH /api/incidents/{id}
```

## <a name="request-headers"></a><span data-ttu-id="e4b66-130">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="e4b66-130">Request headers</span></span>

<span data-ttu-id="e4b66-131">Nom</span><span class="sxs-lookup"><span data-stu-id="e4b66-131">Name</span></span> | <span data-ttu-id="e4b66-132">Type</span><span class="sxs-lookup"><span data-stu-id="e4b66-132">Type</span></span> | <span data-ttu-id="e4b66-133">Description</span><span class="sxs-lookup"><span data-stu-id="e4b66-133">Description</span></span>
:---|:---|:---
<span data-ttu-id="e4b66-134">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e4b66-134">Authorization</span></span> | <span data-ttu-id="e4b66-135">String</span><span class="sxs-lookup"><span data-stu-id="e4b66-135">String</span></span> | <span data-ttu-id="e4b66-136">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="e4b66-136">Bearer {token}.</span></span> <span data-ttu-id="e4b66-137">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="e4b66-137">**Required**.</span></span>
<span data-ttu-id="e4b66-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e4b66-138">Content-Type</span></span> | <span data-ttu-id="e4b66-139">String</span><span class="sxs-lookup"><span data-stu-id="e4b66-139">String</span></span> | <span data-ttu-id="e4b66-140">application/json.</span><span class="sxs-lookup"><span data-stu-id="e4b66-140">application/json.</span></span> <span data-ttu-id="e4b66-141">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="e4b66-141">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="e4b66-142">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="e4b66-142">Request body</span></span>
<span data-ttu-id="e4b66-143">Dans le corps de la demande, fournissez les valeurs des champs pertinents qui doivent être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e4b66-143">In the request body, supply the values for the relevant fields that should be updated.</span></span>
<br><span data-ttu-id="e4b66-144">Les propriétés existantes qui ne sont pas incluses dans le corps de la demande conserveront leurs valeurs précédentes ou seront recalculées en fonction des modifications apportées à d’autres valeurs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="e4b66-144">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> 
<br><span data-ttu-id="e4b66-145">Pour des performances optimales, vous ne devez pas inclure de valeurs existantes qui n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="e4b66-145">For best performance you shouldn't include existing values that haven't change.</span></span>

<span data-ttu-id="e4b66-146">Propriété</span><span class="sxs-lookup"><span data-stu-id="e4b66-146">Property</span></span> | <span data-ttu-id="e4b66-147">Type</span><span class="sxs-lookup"><span data-stu-id="e4b66-147">Type</span></span> | <span data-ttu-id="e4b66-148">Description</span><span class="sxs-lookup"><span data-stu-id="e4b66-148">Description</span></span>
:---|:---|:---
<span data-ttu-id="e4b66-149">statut</span><span class="sxs-lookup"><span data-stu-id="e4b66-149">status</span></span> | <span data-ttu-id="e4b66-150">Énum</span><span class="sxs-lookup"><span data-stu-id="e4b66-150">Enum</span></span> | <span data-ttu-id="e4b66-151">Spécifie l’état actuel de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="e4b66-151">Specifies the current status of the alert.</span></span> <span data-ttu-id="e4b66-152">Les valeurs possibles sont les suivantes : ```Active``` ```Resolved``` et ```Redirected``` .</span><span class="sxs-lookup"><span data-stu-id="e4b66-152">Possible values are: ```Active```, ```Resolved``` and ```Redirected```.</span></span>
<span data-ttu-id="e4b66-153">assignedTo</span><span class="sxs-lookup"><span data-stu-id="e4b66-153">assignedTo</span></span> | <span data-ttu-id="e4b66-154">string</span><span class="sxs-lookup"><span data-stu-id="e4b66-154">string</span></span> | <span data-ttu-id="e4b66-155">Propriétaire de l’incident.</span><span class="sxs-lookup"><span data-stu-id="e4b66-155">Owner of the incident.</span></span>
<span data-ttu-id="e4b66-156">classification</span><span class="sxs-lookup"><span data-stu-id="e4b66-156">classification</span></span> | <span data-ttu-id="e4b66-157">Énum</span><span class="sxs-lookup"><span data-stu-id="e4b66-157">Enum</span></span> | <span data-ttu-id="e4b66-158">Spécification de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="e4b66-158">Specification of the alert.</span></span> <span data-ttu-id="e4b66-159">Les valeurs possibles sont ```Unknown```, ```FalsePositive``` et ```TruePositive```.</span><span class="sxs-lookup"><span data-stu-id="e4b66-159">Possible values are: ```Unknown```, ```FalsePositive```, ```TruePositive```.</span></span>
<span data-ttu-id="e4b66-160">indications</span><span class="sxs-lookup"><span data-stu-id="e4b66-160">determination</span></span> | <span data-ttu-id="e4b66-161">Énum</span><span class="sxs-lookup"><span data-stu-id="e4b66-161">Enum</span></span> | <span data-ttu-id="e4b66-162">Spécifie la détermination de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="e4b66-162">Specifies the determination of the alert.</span></span> <span data-ttu-id="e4b66-163">Les valeurs possibles sont les suivantes : ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware``` et ```Other```.</span><span class="sxs-lookup"><span data-stu-id="e4b66-163">Possible values are: ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware```, ```Other```.</span></span>
<span data-ttu-id="e4b66-164">étiquettes</span><span class="sxs-lookup"><span data-stu-id="e4b66-164">tags</span></span> | <span data-ttu-id="e4b66-165">Liste de chaînes</span><span class="sxs-lookup"><span data-stu-id="e4b66-165">string List</span></span> | <span data-ttu-id="e4b66-166">Liste des balises incident.</span><span class="sxs-lookup"><span data-stu-id="e4b66-166">List of Incident tags.</span></span>



## <a name="response"></a><span data-ttu-id="e4b66-167">Réponse</span><span class="sxs-lookup"><span data-stu-id="e4b66-167">Response</span></span>
<span data-ttu-id="e4b66-168">Si elle réussit, cette méthode renvoie 200 OK et l’entité incident dans le corps de la réponse avec les propriétés mises à jour.</span><span class="sxs-lookup"><span data-stu-id="e4b66-168">If successful, this method returns 200 OK, and the incident entity in the response body with the updated properties.</span></span> <span data-ttu-id="e4b66-169">Si l’incident portant l’ID spécifié est introuvable-404 introuvable.</span><span class="sxs-lookup"><span data-stu-id="e4b66-169">If incident with the specified id was not found - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="e4b66-170">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4b66-170">Example</span></span>

<span data-ttu-id="e4b66-171">**Demande**</span><span class="sxs-lookup"><span data-stu-id="e4b66-171">**Request**</span></span>

<span data-ttu-id="e4b66-172">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="e4b66-172">Here is an example of the request.</span></span>

```
 PATCH https://api.security.microsoft.com/api/incidents/{id}
```

```json
{
    "status": "Resolved",
    "assignedTo": "secop2@contoso.com",
    "classification": "TruePositive",
    "determination": "Malware",
    "tags": ["Yossi's playground", "Don't mess with the Zohan"]
}
```


## <a name="related-topic"></a><span data-ttu-id="e4b66-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4b66-173">Related topic</span></span>
- [<span data-ttu-id="e4b66-174">API d’incident</span><span class="sxs-lookup"><span data-stu-id="e4b66-174">Incident APIs</span></span>](api-incident.md)
- [<span data-ttu-id="e4b66-175">Répertorier les incidents</span><span class="sxs-lookup"><span data-stu-id="e4b66-175">List incidents</span></span>](api-list-incidents.md)
