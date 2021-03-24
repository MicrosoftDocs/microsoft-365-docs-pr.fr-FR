---
title: API de mise à jour des incidents
description: Découvrez comment mettre à jour les incidents à l’aide de l’API Microsoft 365 Defender
keywords: mise à jour, api, incident
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 549f9bf2b9dc2ea5d1c734a809ad10a168c8123e
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51056662"
---
# <a name="update-incidents-api"></a><span data-ttu-id="49779-104">API de mise à jour des incidents</span><span class="sxs-lookup"><span data-stu-id="49779-104">Update incidents API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="49779-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="49779-105">**Applies to:**</span></span>

- <span data-ttu-id="49779-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="49779-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49779-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="49779-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="49779-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="49779-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="api-description"></a><span data-ttu-id="49779-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="49779-109">API description</span></span>

<span data-ttu-id="49779-110">Met à jour les propriétés d’un incident existant.</span><span class="sxs-lookup"><span data-stu-id="49779-110">Updates properties of existing incident.</span></span> <span data-ttu-id="49779-111">Les propriétés updatables ```status``` sont : , , , et ```determination``` ```classification``` ```assignedTo``` ```tags``` .</span><span class="sxs-lookup"><span data-stu-id="49779-111">Updatable properties are: ```status```, ```determination```, ```classification```, ```assignedTo```, and ```tags```.</span></span>

### <a name="quotas-resource-allocation-and-other-constraints"></a><span data-ttu-id="49779-112">Quotas, allocation de ressources et autres contraintes</span><span class="sxs-lookup"><span data-stu-id="49779-112">Quotas, resource allocation, and other constraints</span></span>

1. <span data-ttu-id="49779-113">Vous pouvez effectuer jusqu’à 50 appels par minute ou 1 500 appels par heure avant d’atteindre le seuil de limitation.</span><span class="sxs-lookup"><span data-stu-id="49779-113">You can make up to 50 calls per minute or 1500 calls per hour before you hit the throttling threshold.</span></span>
2. <span data-ttu-id="49779-114">Vous ne pouvez définir `determination` la propriété que si elle est définie sur `classification` TruePositive.</span><span class="sxs-lookup"><span data-stu-id="49779-114">You can set the `determination` property only if `classification` is set to TruePositive.</span></span>

<span data-ttu-id="49779-115">Si votre demande est limitée, elle retourne un `429` code de réponse.</span><span class="sxs-lookup"><span data-stu-id="49779-115">If your request is throttled, it will return a `429` response code.</span></span> <span data-ttu-id="49779-116">Le corps de la réponse indique le moment où vous pouvez commencer à effectuer de nouveaux appels.</span><span class="sxs-lookup"><span data-stu-id="49779-116">The response body will indicate the time when you can begin making new calls.</span></span>

## <a name="permissions"></a><span data-ttu-id="49779-117">Autorisations</span><span class="sxs-lookup"><span data-stu-id="49779-117">Permissions</span></span>

<span data-ttu-id="49779-118">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="49779-118">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="49779-119">Pour plus d’informations, notamment sur le choix des autorisations, voir Access sur les [API Microsoft 365 Defender.](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="49779-119">To learn more, including how to choose permissions, see [Access the Microsoft 365 Defender APIs](api-access.md).</span></span>

<span data-ttu-id="49779-120">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="49779-120">Permission type</span></span> | <span data-ttu-id="49779-121">Autorisation</span><span class="sxs-lookup"><span data-stu-id="49779-121">Permission</span></span> | <span data-ttu-id="49779-122">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="49779-122">Permission display name</span></span>
-|-|-
<span data-ttu-id="49779-123">Application</span><span class="sxs-lookup"><span data-stu-id="49779-123">Application</span></span> | <span data-ttu-id="49779-124">Incident.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="49779-124">Incident.ReadWrite.All</span></span> | <span data-ttu-id="49779-125">Lire et écrire tous les incidents</span><span class="sxs-lookup"><span data-stu-id="49779-125">Read and write all incidents</span></span>
<span data-ttu-id="49779-126">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="49779-126">Delegated (work or school account)</span></span> | <span data-ttu-id="49779-127">Incident.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="49779-127">Incident.ReadWrite</span></span> | <span data-ttu-id="49779-128">Lire et écrire des incidents</span><span class="sxs-lookup"><span data-stu-id="49779-128">Read and write incidents</span></span>

> [!NOTE]
> <span data-ttu-id="49779-129">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur, l’utilisateur doit être autorisé à mettre à jour l’incident dans le portail.</span><span class="sxs-lookup"><span data-stu-id="49779-129">When obtaining a token using user credentials, the user needs to have permission to update the incident in the portal.</span></span>

## <a name="http-request"></a><span data-ttu-id="49779-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="49779-130">HTTP request</span></span>

```HTTP
PATCH /api/incidents/{id}
```

## <a name="request-headers"></a><span data-ttu-id="49779-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="49779-131">Request headers</span></span>

<span data-ttu-id="49779-132">Nom</span><span class="sxs-lookup"><span data-stu-id="49779-132">Name</span></span> | <span data-ttu-id="49779-133">Type</span><span class="sxs-lookup"><span data-stu-id="49779-133">Type</span></span> | <span data-ttu-id="49779-134">Description</span><span class="sxs-lookup"><span data-stu-id="49779-134">Description</span></span>
-|-|-
<span data-ttu-id="49779-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="49779-135">Authorization</span></span> | <span data-ttu-id="49779-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="49779-136">String</span></span> | <span data-ttu-id="49779-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="49779-137">Bearer {token}.</span></span> <span data-ttu-id="49779-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="49779-138">**Required**.</span></span>
<span data-ttu-id="49779-139">Content-Type</span><span class="sxs-lookup"><span data-stu-id="49779-139">Content-Type</span></span> | <span data-ttu-id="49779-140">String</span><span class="sxs-lookup"><span data-stu-id="49779-140">String</span></span> | <span data-ttu-id="49779-141">application/json.</span><span class="sxs-lookup"><span data-stu-id="49779-141">application/json.</span></span> <span data-ttu-id="49779-142">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="49779-142">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="49779-143">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="49779-143">Request body</span></span>

<span data-ttu-id="49779-144">Dans le corps de la demande, fournissons les valeurs des champs qui doivent être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="49779-144">In the request body, supply the values for the fields that should be updated.</span></span> <span data-ttu-id="49779-145">Les propriétés existantes qui ne sont pas incluses dans le corps de la demande conserveront leurs valeurs, sauf si elles doivent être recalculées en raison de modifications apportées aux valeurs associées.</span><span class="sxs-lookup"><span data-stu-id="49779-145">Existing properties that aren't included in the request body will maintain their values, unless they have to be recalculated due to changes to related values.</span></span> <span data-ttu-id="49779-146">Pour de meilleures performances, vous devez omettre les valeurs existantes qui n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="49779-146">For best performance, you should omit existing values that haven't changed.</span></span>

<span data-ttu-id="49779-147">Propriété</span><span class="sxs-lookup"><span data-stu-id="49779-147">Property</span></span> | <span data-ttu-id="49779-148">Type</span><span class="sxs-lookup"><span data-stu-id="49779-148">Type</span></span> | <span data-ttu-id="49779-149">Description</span><span class="sxs-lookup"><span data-stu-id="49779-149">Description</span></span>
-|-|-
<span data-ttu-id="49779-150">statut</span><span class="sxs-lookup"><span data-stu-id="49779-150">status</span></span> | <span data-ttu-id="49779-151">Énum</span><span class="sxs-lookup"><span data-stu-id="49779-151">Enum</span></span> | <span data-ttu-id="49779-152">Spécifie l’état actuel de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="49779-152">Specifies the current status of the alert.</span></span> <span data-ttu-id="49779-153">Les valeurs possibles ```Active``` sont : , et ```Resolved``` ```Redirected``` .</span><span class="sxs-lookup"><span data-stu-id="49779-153">Possible values are: ```Active```, ```Resolved```, and ```Redirected```.</span></span>
<span data-ttu-id="49779-154">assignedTo</span><span class="sxs-lookup"><span data-stu-id="49779-154">assignedTo</span></span> | <span data-ttu-id="49779-155">string</span><span class="sxs-lookup"><span data-stu-id="49779-155">string</span></span> | <span data-ttu-id="49779-156">Propriétaire de l’incident.</span><span class="sxs-lookup"><span data-stu-id="49779-156">Owner of the incident.</span></span>
<span data-ttu-id="49779-157">classification</span><span class="sxs-lookup"><span data-stu-id="49779-157">classification</span></span> | <span data-ttu-id="49779-158">Énum</span><span class="sxs-lookup"><span data-stu-id="49779-158">Enum</span></span> | <span data-ttu-id="49779-159">Spécification de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="49779-159">Specification of the alert.</span></span> <span data-ttu-id="49779-160">Les valeurs possibles sont les suivantes : ```Unknown```, ```FalsePositive``` et ```TruePositive```.</span><span class="sxs-lookup"><span data-stu-id="49779-160">Possible values are: ```Unknown```, ```FalsePositive```, ```TruePositive```.</span></span>
<span data-ttu-id="49779-161">détermination</span><span class="sxs-lookup"><span data-stu-id="49779-161">determination</span></span> | <span data-ttu-id="49779-162">Énum</span><span class="sxs-lookup"><span data-stu-id="49779-162">Enum</span></span> | <span data-ttu-id="49779-163">Spécifie la détermination de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="49779-163">Specifies the determination of the alert.</span></span> <span data-ttu-id="49779-164">Les valeurs possibles sont les suivantes : ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware``` et ```Other```.</span><span class="sxs-lookup"><span data-stu-id="49779-164">Possible values are: ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware```, ```Other```.</span></span>
<span data-ttu-id="49779-165">étiquettes</span><span class="sxs-lookup"><span data-stu-id="49779-165">tags</span></span> | <span data-ttu-id="49779-166">string List</span><span class="sxs-lookup"><span data-stu-id="49779-166">string List</span></span> | <span data-ttu-id="49779-167">Liste des balises d’incident.</span><span class="sxs-lookup"><span data-stu-id="49779-167">List of Incident tags.</span></span>

## <a name="response"></a><span data-ttu-id="49779-168">Réponse</span><span class="sxs-lookup"><span data-stu-id="49779-168">Response</span></span>

<span data-ttu-id="49779-169">Si elle réussit, cette méthode renvoie `200 OK` .</span><span class="sxs-lookup"><span data-stu-id="49779-169">If successful, this method returns `200 OK`.</span></span> <span data-ttu-id="49779-170">Le corps de la réponse contient l’entité d’incident avec les propriétés mises à jour.</span><span class="sxs-lookup"><span data-stu-id="49779-170">The response body will contain the incident entity with updated properties.</span></span> <span data-ttu-id="49779-171">Si un incident avec l’ID spécifié n’a pas été trouvé, la méthode renvoie `404 Not Found` .</span><span class="sxs-lookup"><span data-stu-id="49779-171">If an incident with the specified ID wasn't found, the method returns `404 Not Found`.</span></span>

## <a name="example"></a><span data-ttu-id="49779-172">Exemple</span><span class="sxs-lookup"><span data-stu-id="49779-172">Example</span></span>

<span data-ttu-id="49779-173">**Demande**</span><span class="sxs-lookup"><span data-stu-id="49779-173">**Request**</span></span>

<span data-ttu-id="49779-174">Voici un exemple de la demande.</span><span class="sxs-lookup"><span data-stu-id="49779-174">Here's an example of the request.</span></span>

```HTTP
 PATCH https://api.security.microsoft.com/api/incidents/{id}
```

<span data-ttu-id="49779-175">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="49779-175">**Response**</span></span>

```json
{
    "status": "Resolved",
    "assignedTo": "secop2@contoso.com",
    "classification": "TruePositive",
    "determination": "Malware",
    "tags": ["Yossi's playground", "Don't mess with the Zohan"]
}
```

## <a name="related-articles"></a><span data-ttu-id="49779-176">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="49779-176">Related articles</span></span>

- [<span data-ttu-id="49779-177">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="49779-177">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="49779-178">En savoir plus sur les limites d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="49779-178">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="49779-179">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="49779-179">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="49779-180">API d’incident</span><span class="sxs-lookup"><span data-stu-id="49779-180">Incident APIs</span></span>](api-incident.md)
- [<span data-ttu-id="49779-181">Répertorier les incidents</span><span class="sxs-lookup"><span data-stu-id="49779-181">List incidents</span></span>](api-list-incidents.md)
- [<span data-ttu-id="49779-182">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="49779-182">Incidents overview</span></span>](incidents-overview.md)
