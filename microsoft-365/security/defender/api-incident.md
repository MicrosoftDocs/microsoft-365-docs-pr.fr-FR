---
title: Microsoft 365 API d’incidents de défenseur et type de ressource d’incident
description: Renseignez-vous sur les méthodes et les propriétés du type de ressource incident dans Microsoft 365 Defender
keywords: incident, incidents, api
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
ms.openlocfilehash: 5cc149668e49e21b38b5fb95ae3f40db6c296e1d
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572584"
---
# <a name="microsoft-365-defender-incidents-api-and-the-incident-resource-type"></a><span data-ttu-id="11444-104">Microsoft 365 API des incidents de défense et le type de ressource d’incident</span><span class="sxs-lookup"><span data-stu-id="11444-104">Microsoft 365 Defender incidents API and the incident resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="11444-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="11444-105">**Applies to:**</span></span>

- <span data-ttu-id="11444-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="11444-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11444-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="11444-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="11444-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="11444-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="11444-109">Un [incident](incidents-overview.md) est une collection d’alertes connexes qui aident à décrire une attaque.</span><span class="sxs-lookup"><span data-stu-id="11444-109">An [incident](incidents-overview.md) is a collection of related alerts that help describe an attack.</span></span> <span data-ttu-id="11444-110">Les événements de différentes entités de votre organisation sont automatiquement regroupés par Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="11444-110">Events from different entities in your organization are automatically aggregated by Microsoft 365 Defender.</span></span> <span data-ttu-id="11444-111">Vous pouvez utiliser l’API incidents pour accéder de façon programmatique aux incidents et aux alertes connexes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="11444-111">You can use the incidents API to programatically access your organization's incidents and related alerts.</span></span>

## <a name="quotas-and-resource-allocation"></a><span data-ttu-id="11444-112">Quotas et allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="11444-112">Quotas and resource allocation</span></span>

<span data-ttu-id="11444-113">Vous pouvez demander jusqu’à 50 appels par minute ou 1500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="11444-113">You can request up to 50 calls per minute or 1500 calls per hour.</span></span> <span data-ttu-id="11444-114">Chaque méthode a également ses propres quotas.</span><span class="sxs-lookup"><span data-stu-id="11444-114">Each method also has its own quotas.</span></span> <span data-ttu-id="11444-115">Pour plus d’informations sur les quotas spécifiques à la méthode, consultez l’article respectif de la méthode que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="11444-115">For more information on method-specific quotas, see the respective article for the method you want to use.</span></span>

<span data-ttu-id="11444-116">Un `429` code de réponse HTTP indique que vous avez atteint un quota, soit par le nombre de demandes envoyées, soit par temps de fonctionnement alloué.</span><span class="sxs-lookup"><span data-stu-id="11444-116">A `429` HTTP response code indicates that you've reached a quota, either by number of requests sent, or by allotted running time.</span></span> <span data-ttu-id="11444-117">L’organe d’intervention inclura le temps jusqu’à ce que le quota que vous avez atteint soit réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="11444-117">The response body will include the time until the quota you reached will be reset.</span></span>

## <a name="permissions"></a><span data-ttu-id="11444-118">Autorisations</span><span class="sxs-lookup"><span data-stu-id="11444-118">Permissions</span></span>

<span data-ttu-id="11444-119">L’API incidents nécessite différents types d’autorisations pour chacune de ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="11444-119">The incidents API requires different kinds of permissions for each of its methods.</span></span> <span data-ttu-id="11444-120">Pour plus d’informations sur les autorisations requises, consultez l’article de la méthode respective.</span><span class="sxs-lookup"><span data-stu-id="11444-120">For more information about required permissions, see the respective method's article.</span></span>

## <a name="methods"></a><span data-ttu-id="11444-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="11444-121">Methods</span></span>

<span data-ttu-id="11444-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="11444-122">Method</span></span> | <span data-ttu-id="11444-123">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="11444-123">Return Type</span></span> | <span data-ttu-id="11444-124">Description</span><span class="sxs-lookup"><span data-stu-id="11444-124">Description</span></span>
-|-|-
[<span data-ttu-id="11444-125">Répertorier les incidents</span><span class="sxs-lookup"><span data-stu-id="11444-125">List incidents</span></span>](api-list-incidents.md) | <span data-ttu-id="11444-126">[Liste des](api-incident.md) incidents</span><span class="sxs-lookup"><span data-stu-id="11444-126">[Incident](api-incident.md) list</span></span> | <span data-ttu-id="11444-127">Obtenez une liste d’incidents.</span><span class="sxs-lookup"><span data-stu-id="11444-127">Get a list of incidents.</span></span>
[<span data-ttu-id="11444-128">Incident de mise à jour</span><span class="sxs-lookup"><span data-stu-id="11444-128">Update incident</span></span>](api-update-incidents.md) | [<span data-ttu-id="11444-129">Incident</span><span class="sxs-lookup"><span data-stu-id="11444-129">Incident</span></span>](api-incident.md) | <span data-ttu-id="11444-130">Mettez à jour un incident spécifique.</span><span class="sxs-lookup"><span data-stu-id="11444-130">Update a specific incident.</span></span>

## <a name="request-body-response-and-examples"></a><span data-ttu-id="11444-131">Corps de demande, réponse, et exemples</span><span class="sxs-lookup"><span data-stu-id="11444-131">Request body, response, and examples</span></span>

<span data-ttu-id="11444-132">Consultez les articles de méthode respectifs pour plus de détails sur la façon de construire une demande ou d’affiner une réponse, et pour des exemples pratiques.</span><span class="sxs-lookup"><span data-stu-id="11444-132">Refer to the respective method articles for more details on how to construct a request or parse a response, and for practical examples.</span></span>

## <a name="common-properties"></a><span data-ttu-id="11444-133">Propriétés courantes</span><span class="sxs-lookup"><span data-stu-id="11444-133">Common properties</span></span>

<span data-ttu-id="11444-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="11444-134">Property</span></span> | <span data-ttu-id="11444-135">Type</span><span class="sxs-lookup"><span data-stu-id="11444-135">Type</span></span> | <span data-ttu-id="11444-136">Description</span><span class="sxs-lookup"><span data-stu-id="11444-136">Description</span></span>
-|-|-
<span data-ttu-id="11444-137">incidentId</span><span class="sxs-lookup"><span data-stu-id="11444-137">incidentId</span></span> | <span data-ttu-id="11444-138">long</span><span class="sxs-lookup"><span data-stu-id="11444-138">long</span></span> | <span data-ttu-id="11444-139">Pièce d’identité unique incident.</span><span class="sxs-lookup"><span data-stu-id="11444-139">Incident unique ID.</span></span>
<span data-ttu-id="11444-140">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="11444-140">redirectIncidentId</span></span> | <span data-ttu-id="11444-141">nullable long</span><span class="sxs-lookup"><span data-stu-id="11444-141">nullable long</span></span> | <span data-ttu-id="11444-142">L’ID incident de l’incident actuel a été fusionné.</span><span class="sxs-lookup"><span data-stu-id="11444-142">The Incident ID the current Incident was merged to.</span></span>
<span data-ttu-id="11444-143">incidentName</span><span class="sxs-lookup"><span data-stu-id="11444-143">incidentName</span></span> | <span data-ttu-id="11444-144">string</span><span class="sxs-lookup"><span data-stu-id="11444-144">string</span></span> | <span data-ttu-id="11444-145">Le nom de l’incident.</span><span class="sxs-lookup"><span data-stu-id="11444-145">The name of the Incident.</span></span>
<span data-ttu-id="11444-146">createdTime (en)</span><span class="sxs-lookup"><span data-stu-id="11444-146">createdTime</span></span> | <span data-ttu-id="11444-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="11444-147">DateTimeOffset</span></span> | <span data-ttu-id="11444-148">La date et l’heure (dans UTC) l’incident a été créé.</span><span class="sxs-lookup"><span data-stu-id="11444-148">The date and time (in UTC) the Incident was created.</span></span>
<span data-ttu-id="11444-149">lastUpdateTime (en)</span><span class="sxs-lookup"><span data-stu-id="11444-149">lastUpdateTime</span></span> | <span data-ttu-id="11444-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="11444-150">DateTimeOffset</span></span> | <span data-ttu-id="11444-151">La date et l’heure (dans UTC) l’incident a été mis à jour pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="11444-151">The date and time (in UTC) the Incident was last updated.</span></span>
<span data-ttu-id="11444-152">assignedTo</span><span class="sxs-lookup"><span data-stu-id="11444-152">assignedTo</span></span> | <span data-ttu-id="11444-153">string</span><span class="sxs-lookup"><span data-stu-id="11444-153">string</span></span> | <span data-ttu-id="11444-154">Propriétaire de l’incident.</span><span class="sxs-lookup"><span data-stu-id="11444-154">Owner of the Incident.</span></span>
<span data-ttu-id="11444-155">Sévérité </span><span class="sxs-lookup"><span data-stu-id="11444-155">severity</span></span> | <span data-ttu-id="11444-156">Énum</span><span class="sxs-lookup"><span data-stu-id="11444-156">Enum</span></span> | <span data-ttu-id="11444-157">Gravité de l’incident.</span><span class="sxs-lookup"><span data-stu-id="11444-157">Severity of the Incident.</span></span> <span data-ttu-id="11444-158">Les valeurs possibles sont : ```UnSpecified``` , , , , et ```Informational``` ```Low``` ```Medium``` ```High``` .</span><span class="sxs-lookup"><span data-stu-id="11444-158">Possible values are: ```UnSpecified```, ```Informational```, ```Low```, ```Medium```, and ```High```.</span></span>
<span data-ttu-id="11444-159">statut</span><span class="sxs-lookup"><span data-stu-id="11444-159">status</span></span> | <span data-ttu-id="11444-160">Énum</span><span class="sxs-lookup"><span data-stu-id="11444-160">Enum</span></span> | <span data-ttu-id="11444-161">Spécifie l’état actuel de l’incident.</span><span class="sxs-lookup"><span data-stu-id="11444-161">Specifies the current status of the incident.</span></span> <span data-ttu-id="11444-162">Les valeurs possibles sont: ```Active``` ```Resolved``` , , et ```Redirected``` .</span><span class="sxs-lookup"><span data-stu-id="11444-162">Possible values are: ```Active```, ```Resolved```, and ```Redirected```.</span></span>
<span data-ttu-id="11444-163">classification</span><span class="sxs-lookup"><span data-stu-id="11444-163">classification</span></span> | <span data-ttu-id="11444-164">Énum</span><span class="sxs-lookup"><span data-stu-id="11444-164">Enum</span></span> | <span data-ttu-id="11444-165">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="11444-165">Specification of the incident.</span></span> <span data-ttu-id="11444-166">Les valeurs possibles sont les suivantes : ```Unknown```, ```FalsePositive``` et ```TruePositive```.</span><span class="sxs-lookup"><span data-stu-id="11444-166">Possible values are: ```Unknown```, ```FalsePositive```, ```TruePositive```.</span></span>
<span data-ttu-id="11444-167">détermination</span><span class="sxs-lookup"><span data-stu-id="11444-167">determination</span></span> | <span data-ttu-id="11444-168">Énum</span><span class="sxs-lookup"><span data-stu-id="11444-168">Enum</span></span> | <span data-ttu-id="11444-169">Précise la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="11444-169">Specifies the determination of the incident.</span></span> <span data-ttu-id="11444-170">Les valeurs possibles sont les suivantes : ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware``` et ```Other```.</span><span class="sxs-lookup"><span data-stu-id="11444-170">Possible values are: ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware```, ```Other```.</span></span>
<span data-ttu-id="11444-171">étiquettes</span><span class="sxs-lookup"><span data-stu-id="11444-171">tags</span></span> | <span data-ttu-id="11444-172">liste des cordes</span><span class="sxs-lookup"><span data-stu-id="11444-172">string List</span></span> | <span data-ttu-id="11444-173">Liste des balises incidentes.</span><span class="sxs-lookup"><span data-stu-id="11444-173">List of Incident tags.</span></span>
<span data-ttu-id="11444-174">commentaires</span><span class="sxs-lookup"><span data-stu-id="11444-174">comments</span></span> | <span data-ttu-id="11444-175">Liste des commentaires sur les incidents</span><span class="sxs-lookup"><span data-stu-id="11444-175">List of incident comments</span></span> | <span data-ttu-id="11444-176">Incident Commentaire objet contient: chaîne de commentaires, crééPar chaîne, et créertime date time.</span><span class="sxs-lookup"><span data-stu-id="11444-176">Incident Comment object contains: comment string, createdBy string, and createTime date time.</span></span>
<span data-ttu-id="11444-177">alerts</span><span class="sxs-lookup"><span data-stu-id="11444-177">alerts</span></span> | <span data-ttu-id="11444-178">Liste d’alerte</span><span class="sxs-lookup"><span data-stu-id="11444-178">Alert List</span></span> | <span data-ttu-id="11444-179">Liste des alertes connexes.</span><span class="sxs-lookup"><span data-stu-id="11444-179">List of related alerts.</span></span> <span data-ttu-id="11444-180">Voir les exemples de documentation [api sur les incidents](api-list-incidents.md) de liste.</span><span class="sxs-lookup"><span data-stu-id="11444-180">See examples at [List incidents](api-list-incidents.md) API documentation.</span></span>

## <a name="related-articles"></a><span data-ttu-id="11444-181">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="11444-181">Related articles</span></span>

- [<span data-ttu-id="11444-182">Microsoft 365 Vue d’ensemble des API Defender</span><span class="sxs-lookup"><span data-stu-id="11444-182">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="11444-183">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="11444-183">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="11444-184">Liste des incidents API</span><span class="sxs-lookup"><span data-stu-id="11444-184">List incidents API</span></span>](api-list-incidents.md)
- [<span data-ttu-id="11444-185">Mise à jour de l’API incident</span><span class="sxs-lookup"><span data-stu-id="11444-185">Update incident API</span></span>](api-update-incidents.md)
