---
title: Mise à jour de l’API incident
description: Découvrez comment mettre à jour les incidents à l’aide Microsoft 365'API Defender
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
ms.openlocfilehash: e3f3919d067078ef1fd1e116dc52e8a73c0726d9
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52571780"
---
# <a name="update-incident-api"></a><span data-ttu-id="4b426-104">Mise à jour de l’API incident</span><span class="sxs-lookup"><span data-stu-id="4b426-104">Update incident API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="4b426-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4b426-105">**Applies to:**</span></span>

- <span data-ttu-id="4b426-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4b426-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b426-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="4b426-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4b426-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="4b426-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="api-description"></a><span data-ttu-id="4b426-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="4b426-109">API description</span></span>

<span data-ttu-id="4b426-110">Met à jour les propriétés de l’incident existant.</span><span class="sxs-lookup"><span data-stu-id="4b426-110">Updates properties of existing incident.</span></span> <span data-ttu-id="4b426-111">Les propriétés updatables sont : ```status``` , , , , , ```determination``` ```classification``` ```assignedTo``` ```tags``` ```comments``` et.</span><span class="sxs-lookup"><span data-stu-id="4b426-111">Updatable properties are: ```status```, ```determination```, ```classification```, ```assignedTo```, ```tags```, and ```comments```.</span></span>

### <a name="quotas-resource-allocation-and-other-constraints"></a><span data-ttu-id="4b426-112">Quotas, allocation des ressources et autres contraintes</span><span class="sxs-lookup"><span data-stu-id="4b426-112">Quotas, resource allocation, and other constraints</span></span>

1. <span data-ttu-id="4b426-113">Vous pouvez passer jusqu’à 50 appels par minute ou 1500 appels par heure avant d’atteindre le seuil de limitation.</span><span class="sxs-lookup"><span data-stu-id="4b426-113">You can make up to 50 calls per minute or 1500 calls per hour before you hit the throttling threshold.</span></span>
2. <span data-ttu-id="4b426-114">Vous ne pouvez définir la `determination` propriété que si elle est définie sur `classification` TruePositive.</span><span class="sxs-lookup"><span data-stu-id="4b426-114">You can set the `determination` property only if `classification` is set to TruePositive.</span></span>

<span data-ttu-id="4b426-115">Si votre demande est étranglée, elle retournera un `429` code de réponse.</span><span class="sxs-lookup"><span data-stu-id="4b426-115">If your request is throttled, it will return a `429` response code.</span></span> <span data-ttu-id="4b426-116">L’organe de réponse indiquera l’heure àù vous pouvez commencer à faire de nouveaux appels.</span><span class="sxs-lookup"><span data-stu-id="4b426-116">The response body will indicate the time when you can begin making new calls.</span></span>

## <a name="permissions"></a><span data-ttu-id="4b426-117">Autorisations</span><span class="sxs-lookup"><span data-stu-id="4b426-117">Permissions</span></span>

<span data-ttu-id="4b426-118">L’une des autorisations suivantes est requise pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="4b426-118">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="4b426-119">Pour en savoir plus, y compris sur la façon de choisir les autorisations, [consultez Accès Microsoft 365 API Defender](api-access.md).</span><span class="sxs-lookup"><span data-stu-id="4b426-119">To learn more, including how to choose permissions, see [Access the Microsoft 365 Defender APIs](api-access.md).</span></span>

<span data-ttu-id="4b426-120">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="4b426-120">Permission type</span></span> | <span data-ttu-id="4b426-121">Autorisation</span><span class="sxs-lookup"><span data-stu-id="4b426-121">Permission</span></span> | <span data-ttu-id="4b426-122">Nom d’affichage d’autorisation</span><span class="sxs-lookup"><span data-stu-id="4b426-122">Permission display name</span></span>
-|-|-
<span data-ttu-id="4b426-123">Application</span><span class="sxs-lookup"><span data-stu-id="4b426-123">Application</span></span> | <span data-ttu-id="4b426-124">Incident.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4b426-124">Incident.ReadWrite.All</span></span> | <span data-ttu-id="4b426-125">Lire et écrire tous les incidents</span><span class="sxs-lookup"><span data-stu-id="4b426-125">Read and write all incidents</span></span>
<span data-ttu-id="4b426-126">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="4b426-126">Delegated (work or school account)</span></span> | <span data-ttu-id="4b426-127">Incident.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4b426-127">Incident.ReadWrite</span></span> | <span data-ttu-id="4b426-128">Lire et écrire les incidents</span><span class="sxs-lookup"><span data-stu-id="4b426-128">Read and write incidents</span></span>

> [!NOTE]
> <span data-ttu-id="4b426-129">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur, l’utilisateur doit avoir la permission de mettre à jour l’incident dans le portail.</span><span class="sxs-lookup"><span data-stu-id="4b426-129">When obtaining a token using user credentials, the user needs to have permission to update the incident in the portal.</span></span>

## <a name="http-request"></a><span data-ttu-id="4b426-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="4b426-130">HTTP request</span></span>

```HTTP
PATCH /api/incidents/{id}
```

## <a name="request-headers"></a><span data-ttu-id="4b426-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="4b426-131">Request headers</span></span>

<span data-ttu-id="4b426-132">Nom</span><span class="sxs-lookup"><span data-stu-id="4b426-132">Name</span></span> | <span data-ttu-id="4b426-133">Type</span><span class="sxs-lookup"><span data-stu-id="4b426-133">Type</span></span> | <span data-ttu-id="4b426-134">Description</span><span class="sxs-lookup"><span data-stu-id="4b426-134">Description</span></span>
-|-|-
<span data-ttu-id="4b426-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="4b426-135">Authorization</span></span> | <span data-ttu-id="4b426-136">String</span><span class="sxs-lookup"><span data-stu-id="4b426-136">String</span></span> | <span data-ttu-id="4b426-137">Porteur {jeton}.</span><span class="sxs-lookup"><span data-stu-id="4b426-137">Bearer {token}.</span></span> <span data-ttu-id="4b426-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="4b426-138">**Required**.</span></span>
<span data-ttu-id="4b426-139">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4b426-139">Content-Type</span></span> | <span data-ttu-id="4b426-140">String</span><span class="sxs-lookup"><span data-stu-id="4b426-140">String</span></span> | <span data-ttu-id="4b426-141">application/json.</span><span class="sxs-lookup"><span data-stu-id="4b426-141">application/json.</span></span> <span data-ttu-id="4b426-142">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="4b426-142">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="4b426-143">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="4b426-143">Request body</span></span>

<span data-ttu-id="4b426-144">Dans l’organisme de demande, fournissez les valeurs des champs qui doivent être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4b426-144">In the request body, supply the values for the fields that should be updated.</span></span> <span data-ttu-id="4b426-145">Les propriétés existantes qui ne sont pas incluses dans l’organisme de demande conserveront leurs valeurs, à moins qu’elles ne doivent être recalculées en raison de modifications apportées aux valeurs connexes.</span><span class="sxs-lookup"><span data-stu-id="4b426-145">Existing properties that aren't included in the request body will maintain their values, unless they have to be recalculated due to changes to related values.</span></span> <span data-ttu-id="4b426-146">Pour de meilleures performances, vous devez omettre les valeurs existantes qui n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="4b426-146">For best performance, you should omit existing values that haven't changed.</span></span>

<span data-ttu-id="4b426-147">Propriété</span><span class="sxs-lookup"><span data-stu-id="4b426-147">Property</span></span> | <span data-ttu-id="4b426-148">Type</span><span class="sxs-lookup"><span data-stu-id="4b426-148">Type</span></span> | <span data-ttu-id="4b426-149">Description</span><span class="sxs-lookup"><span data-stu-id="4b426-149">Description</span></span>
-|-|-
<span data-ttu-id="4b426-150">statut</span><span class="sxs-lookup"><span data-stu-id="4b426-150">status</span></span> | <span data-ttu-id="4b426-151">Énum</span><span class="sxs-lookup"><span data-stu-id="4b426-151">Enum</span></span> | <span data-ttu-id="4b426-152">Spécifie l’état actuel de l’incident.</span><span class="sxs-lookup"><span data-stu-id="4b426-152">Specifies the current status of the incident.</span></span> <span data-ttu-id="4b426-153">Les valeurs possibles sont: ```Active``` ```Resolved``` , , et ```Redirected``` .</span><span class="sxs-lookup"><span data-stu-id="4b426-153">Possible values are: ```Active```, ```Resolved```, and ```Redirected```.</span></span>
<span data-ttu-id="4b426-154">assignedTo</span><span class="sxs-lookup"><span data-stu-id="4b426-154">assignedTo</span></span> | <span data-ttu-id="4b426-155">string</span><span class="sxs-lookup"><span data-stu-id="4b426-155">string</span></span> | <span data-ttu-id="4b426-156">Propriétaire de l’incident.</span><span class="sxs-lookup"><span data-stu-id="4b426-156">Owner of the incident.</span></span>
<span data-ttu-id="4b426-157">classification</span><span class="sxs-lookup"><span data-stu-id="4b426-157">classification</span></span> | <span data-ttu-id="4b426-158">Énum</span><span class="sxs-lookup"><span data-stu-id="4b426-158">Enum</span></span> | <span data-ttu-id="4b426-159">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="4b426-159">Specification of the incident.</span></span> <span data-ttu-id="4b426-160">Les valeurs possibles sont les suivantes : ```Unknown```, ```FalsePositive``` et ```TruePositive```.</span><span class="sxs-lookup"><span data-stu-id="4b426-160">Possible values are: ```Unknown```, ```FalsePositive```, ```TruePositive```.</span></span>
<span data-ttu-id="4b426-161">détermination</span><span class="sxs-lookup"><span data-stu-id="4b426-161">determination</span></span> | <span data-ttu-id="4b426-162">Énum</span><span class="sxs-lookup"><span data-stu-id="4b426-162">Enum</span></span> | <span data-ttu-id="4b426-163">Précise la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="4b426-163">Specifies the determination of the incident.</span></span> <span data-ttu-id="4b426-164">Les valeurs possibles sont les suivantes : ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware``` et ```Other```.</span><span class="sxs-lookup"><span data-stu-id="4b426-164">Possible values are: ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware```, ```Other```.</span></span>
<span data-ttu-id="4b426-165">étiquettes</span><span class="sxs-lookup"><span data-stu-id="4b426-165">tags</span></span> | <span data-ttu-id="4b426-166">liste des cordes</span><span class="sxs-lookup"><span data-stu-id="4b426-166">string List</span></span> | <span data-ttu-id="4b426-167">Liste des balises incidentes.</span><span class="sxs-lookup"><span data-stu-id="4b426-167">List of Incident tags.</span></span>
<span data-ttu-id="4b426-168">comment</span><span class="sxs-lookup"><span data-stu-id="4b426-168">comment</span></span> | <span data-ttu-id="4b426-169">string</span><span class="sxs-lookup"><span data-stu-id="4b426-169">string</span></span> | <span data-ttu-id="4b426-170">Commentaire à ajouter à l’incident.</span><span class="sxs-lookup"><span data-stu-id="4b426-170">Comment to be added to the incident.</span></span>

## <a name="response"></a><span data-ttu-id="4b426-171">Réponse</span><span class="sxs-lookup"><span data-stu-id="4b426-171">Response</span></span>

<span data-ttu-id="4b426-172">En cas de succès, cette méthode revient `200 OK` .</span><span class="sxs-lookup"><span data-stu-id="4b426-172">If successful, this method returns `200 OK`.</span></span> <span data-ttu-id="4b426-173">L’organe d’intervention contiendra l’entité incidente avec des propriétés mises à jour.</span><span class="sxs-lookup"><span data-stu-id="4b426-173">The response body will contain the incident entity with updated properties.</span></span> <span data-ttu-id="4b426-174">Si un incident avec l’iD spécifié n’a pas été trouvé, la méthode revient `404 Not Found` .</span><span class="sxs-lookup"><span data-stu-id="4b426-174">If an incident with the specified ID wasn't found, the method returns `404 Not Found`.</span></span>

## <a name="example"></a><span data-ttu-id="4b426-175">Exemple</span><span class="sxs-lookup"><span data-stu-id="4b426-175">Example</span></span>

<span data-ttu-id="4b426-176">**Demande**</span><span class="sxs-lookup"><span data-stu-id="4b426-176">**Request**</span></span>

<span data-ttu-id="4b426-177">Voici un exemple de la demande.</span><span class="sxs-lookup"><span data-stu-id="4b426-177">Here's an example of the request.</span></span>

```HTTP
 PATCH https://api.security.microsoft.com/api/incidents/{id}
```

<span data-ttu-id="4b426-178">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="4b426-178">**Response**</span></span>

```json
{
    "status": "Resolved",
    "assignedTo": "secop2@contoso.com",
    "classification": "TruePositive",
    "determination": "Malware",
    "tags": ["Yossi's playground", "Don't mess with the Zohan"],
    "comments": [
          {
              "comment": "pen testing",
              "createdBy": "secop2@contoso.com",
              "createdTime": "2021-05-02T09:34:21.5519738Z"
          },
          {
              "comment": "valid incident",
              "createdBy": "secop2@contoso.comt",
              "createdTime": "2021-05-02T09:36:27.6652581Z"
          }
      ]
}
```

## <a name="related-articles"></a><span data-ttu-id="4b426-179">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="4b426-179">Related articles</span></span>

- [<span data-ttu-id="4b426-180">Accédez aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4b426-180">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="4b426-181">En savoir plus sur les limites de l’API et les licences</span><span class="sxs-lookup"><span data-stu-id="4b426-181">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="4b426-182">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4b426-182">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="4b426-183">API d’incident</span><span class="sxs-lookup"><span data-stu-id="4b426-183">Incident APIs</span></span>](api-incident.md)
- [<span data-ttu-id="4b426-184">Répertorier les incidents</span><span class="sxs-lookup"><span data-stu-id="4b426-184">List incidents</span></span>](api-list-incidents.md)
- [<span data-ttu-id="4b426-185">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="4b426-185">Incidents overview</span></span>](incidents-overview.md)
