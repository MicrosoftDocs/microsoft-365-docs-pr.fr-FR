---
title: API d’incidents Microsoft 365 Defender et type de ressource d’incident
description: En savoir plus sur les méthodes et les propriétés du type de ressource Incident dans Microsoft 365 Defender
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
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 37413c3c7458527e90d4657ddfb3afb058e1dfaa
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49928353"
---
# <a name="microsoft-365-defender-incidents-api-and-the-incident-resource-type"></a><span data-ttu-id="8876d-104">API d’incidents Microsoft 365 Defender et type de ressource incident</span><span class="sxs-lookup"><span data-stu-id="8876d-104">Microsoft 365 Defender incidents API and the incident resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="8876d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8876d-105">**Applies to:**</span></span>

- <span data-ttu-id="8876d-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8876d-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8876d-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8876d-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8876d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="8876d-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="8876d-109">Un [incident](incidents-overview.md) est un ensemble d’alertes associées qui permettent de décrire une attaque.</span><span class="sxs-lookup"><span data-stu-id="8876d-109">An [incident](incidents-overview.md) is a collection of related alerts that help describe an attack.</span></span> <span data-ttu-id="8876d-110">Les événements de différentes entités de votre organisation sont automatiquement agrégés par Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="8876d-110">Events from different entities in your organization are automatically aggregated by Microsoft 365 Defender.</span></span> <span data-ttu-id="8876d-111">Vous pouvez utiliser l’API d’incidents pour accéder par programmation aux incidents de votre organisation et aux alertes associées.</span><span class="sxs-lookup"><span data-stu-id="8876d-111">You can use the incidents API to programatically access your organization's incidents and related alerts.</span></span>

## <a name="quotas-and-resource-allocation"></a><span data-ttu-id="8876d-112">Quotas et allocation de ressources</span><span class="sxs-lookup"><span data-stu-id="8876d-112">Quotas and resource allocation</span></span>

<span data-ttu-id="8876d-113">Vous pouvez demander jusqu’à 50 appels par minute ou 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="8876d-113">You can request up to 50 calls per minute or 1500 calls per hour.</span></span> <span data-ttu-id="8876d-114">Chaque méthode possède également ses propres quotas.</span><span class="sxs-lookup"><span data-stu-id="8876d-114">Each method also has its own quotas.</span></span> <span data-ttu-id="8876d-115">Pour plus d’informations sur les quotas propres aux méthodes, consultez l’article respectif de la méthode que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="8876d-115">For more information on method-specific quotas, see the respective article for the method you want to use.</span></span>

<span data-ttu-id="8876d-116">Un code de réponse HTTP indique que vous avez atteint un quota, soit par nombre de demandes envoyées, soit par temps `429` d’exécution alloué.</span><span class="sxs-lookup"><span data-stu-id="8876d-116">A `429` HTTP response code indicates that you've reached a quota, either by number of requests sent, or by allotted running time.</span></span> <span data-ttu-id="8876d-117">Le corps de la réponse inclut la durée jusqu’à ce que le quota que vous avez atteint soit réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="8876d-117">The response body will include the time until the quota you reached will be reset.</span></span>

## <a name="permissions"></a><span data-ttu-id="8876d-118">Autorisations</span><span class="sxs-lookup"><span data-stu-id="8876d-118">Permissions</span></span>

<span data-ttu-id="8876d-119">L’API incidents nécessite différents types d’autorisations pour chacune de ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="8876d-119">The incidents API requires different kinds of permissions for each of its methods.</span></span> <span data-ttu-id="8876d-120">Pour plus d’informations sur les autorisations requises, consultez l’article de la méthode respective.</span><span class="sxs-lookup"><span data-stu-id="8876d-120">For more information about required permissions, see the respective method's article.</span></span>

## <a name="methods"></a><span data-ttu-id="8876d-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8876d-121">Methods</span></span>

<span data-ttu-id="8876d-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="8876d-122">Method</span></span> | <span data-ttu-id="8876d-123">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="8876d-123">Return Type</span></span> | <span data-ttu-id="8876d-124">Description</span><span class="sxs-lookup"><span data-stu-id="8876d-124">Description</span></span>
-|-|-
[<span data-ttu-id="8876d-125">Répertorier les incidents</span><span class="sxs-lookup"><span data-stu-id="8876d-125">List incidents</span></span>](api-list-incidents.md) | <span data-ttu-id="8876d-126">[Liste des incidents](api-incident.md)</span><span class="sxs-lookup"><span data-stu-id="8876d-126">[Incident](api-incident.md) list</span></span> | <span data-ttu-id="8876d-127">Obtenir la liste des incidents.</span><span class="sxs-lookup"><span data-stu-id="8876d-127">Get a list of incidents.</span></span>
[<span data-ttu-id="8876d-128">Incident de mise à jour</span><span class="sxs-lookup"><span data-stu-id="8876d-128">Update incident</span></span>](api-update-incidents.md) | [<span data-ttu-id="8876d-129">Incident</span><span class="sxs-lookup"><span data-stu-id="8876d-129">Incident</span></span>](api-incident.md) | <span data-ttu-id="8876d-130">Mettre à jour un incident spécifique.</span><span class="sxs-lookup"><span data-stu-id="8876d-130">Update a specific incident.</span></span>

## <a name="request-body-response-and-examples"></a><span data-ttu-id="8876d-131">Corps de la demande, réponse et exemples</span><span class="sxs-lookup"><span data-stu-id="8876d-131">Request body, response, and examples</span></span>

<span data-ttu-id="8876d-132">Reportez-vous aux articles de méthode respectifs pour plus d’informations sur la construction d’une demande ou l’analyse d’une réponse, et pour obtenir des exemples pratiques.</span><span class="sxs-lookup"><span data-stu-id="8876d-132">Refer to the respective method articles for more details on how to construct a request or parse a response, and for practical examples.</span></span>

## <a name="common-properties"></a><span data-ttu-id="8876d-133">Propriétés courantes</span><span class="sxs-lookup"><span data-stu-id="8876d-133">Common properties</span></span>

<span data-ttu-id="8876d-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="8876d-134">Property</span></span> | <span data-ttu-id="8876d-135">Type</span><span class="sxs-lookup"><span data-stu-id="8876d-135">Type</span></span> | <span data-ttu-id="8876d-136">Description</span><span class="sxs-lookup"><span data-stu-id="8876d-136">Description</span></span>
-|-|-
<span data-ttu-id="8876d-137">incidentId</span><span class="sxs-lookup"><span data-stu-id="8876d-137">incidentId</span></span> | <span data-ttu-id="8876d-138">long</span><span class="sxs-lookup"><span data-stu-id="8876d-138">long</span></span> | <span data-ttu-id="8876d-139">ID unique de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8876d-139">Incident unique ID.</span></span>
<span data-ttu-id="8876d-140">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="8876d-140">redirectIncidentId</span></span> | <span data-ttu-id="8876d-141">nullable long</span><span class="sxs-lookup"><span data-stu-id="8876d-141">nullable long</span></span> | <span data-ttu-id="8876d-142">L’ID d’incident dans le cas de l’incident en cours a été fusionné.</span><span class="sxs-lookup"><span data-stu-id="8876d-142">The Incident ID the current Incident was merged to.</span></span>
<span data-ttu-id="8876d-143">incidentName</span><span class="sxs-lookup"><span data-stu-id="8876d-143">incidentName</span></span> | <span data-ttu-id="8876d-144">string</span><span class="sxs-lookup"><span data-stu-id="8876d-144">string</span></span> | <span data-ttu-id="8876d-145">Nom de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8876d-145">The name of the Incident.</span></span>
<span data-ttu-id="8876d-146">createdTime</span><span class="sxs-lookup"><span data-stu-id="8876d-146">createdTime</span></span> | <span data-ttu-id="8876d-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8876d-147">DateTimeOffset</span></span> | <span data-ttu-id="8876d-148">Date et heure (en UTC) de création de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8876d-148">The date and time (in UTC) the Incident was created.</span></span>
<span data-ttu-id="8876d-149">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="8876d-149">lastUpdateTime</span></span> | <span data-ttu-id="8876d-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8876d-150">DateTimeOffset</span></span> | <span data-ttu-id="8876d-151">Date et heure (en UTC) de la dernière mise à jour de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8876d-151">The date and time (in UTC) the Incident was last updated.</span></span>
<span data-ttu-id="8876d-152">assignedTo</span><span class="sxs-lookup"><span data-stu-id="8876d-152">assignedTo</span></span> | <span data-ttu-id="8876d-153">string</span><span class="sxs-lookup"><span data-stu-id="8876d-153">string</span></span> | <span data-ttu-id="8876d-154">Propriétaire de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8876d-154">Owner of the Incident.</span></span>
<span data-ttu-id="8876d-155">Sévérité </span><span class="sxs-lookup"><span data-stu-id="8876d-155">severity</span></span> | <span data-ttu-id="8876d-156">Énum</span><span class="sxs-lookup"><span data-stu-id="8876d-156">Enum</span></span> | <span data-ttu-id="8876d-157">Gravité de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8876d-157">Severity of the Incident.</span></span> <span data-ttu-id="8876d-158">Les valeurs possibles ```UnSpecified``` sont : , , et ```Informational``` ```Low``` ```Medium``` ```High``` .</span><span class="sxs-lookup"><span data-stu-id="8876d-158">Possible values are: ```UnSpecified```, ```Informational```, ```Low```, ```Medium```, and ```High```.</span></span>
<span data-ttu-id="8876d-159">statut</span><span class="sxs-lookup"><span data-stu-id="8876d-159">status</span></span> | <span data-ttu-id="8876d-160">Énum</span><span class="sxs-lookup"><span data-stu-id="8876d-160">Enum</span></span> | <span data-ttu-id="8876d-161">Spécifie l’état actuel de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8876d-161">Specifies the current status of the incident.</span></span> <span data-ttu-id="8876d-162">Les valeurs possibles ```Active``` sont : , et ```Resolved``` ```Redirected``` .</span><span class="sxs-lookup"><span data-stu-id="8876d-162">Possible values are: ```Active```, ```Resolved```, and ```Redirected```.</span></span>
<span data-ttu-id="8876d-163">classification</span><span class="sxs-lookup"><span data-stu-id="8876d-163">classification</span></span> | <span data-ttu-id="8876d-164">Énum</span><span class="sxs-lookup"><span data-stu-id="8876d-164">Enum</span></span> | <span data-ttu-id="8876d-165">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8876d-165">Specification of the incident.</span></span> <span data-ttu-id="8876d-166">Les valeurs possibles sont ```Unknown```, ```FalsePositive``` et ```TruePositive```.</span><span class="sxs-lookup"><span data-stu-id="8876d-166">Possible values are: ```Unknown```, ```FalsePositive```, ```TruePositive```.</span></span>
<span data-ttu-id="8876d-167">détermination</span><span class="sxs-lookup"><span data-stu-id="8876d-167">determination</span></span> | <span data-ttu-id="8876d-168">Énum</span><span class="sxs-lookup"><span data-stu-id="8876d-168">Enum</span></span> | <span data-ttu-id="8876d-169">Spécifie la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8876d-169">Specifies the determination of the incident.</span></span> <span data-ttu-id="8876d-170">Les valeurs possibles sont les suivantes : ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware``` et ```Other```.</span><span class="sxs-lookup"><span data-stu-id="8876d-170">Possible values are: ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware```, ```Other```.</span></span>
<span data-ttu-id="8876d-171">étiquettes</span><span class="sxs-lookup"><span data-stu-id="8876d-171">tags</span></span> | <span data-ttu-id="8876d-172">string List</span><span class="sxs-lookup"><span data-stu-id="8876d-172">string List</span></span> | <span data-ttu-id="8876d-173">Liste des balises d’incident.</span><span class="sxs-lookup"><span data-stu-id="8876d-173">List of Incident tags.</span></span>
<span data-ttu-id="8876d-174">alerts</span><span class="sxs-lookup"><span data-stu-id="8876d-174">alerts</span></span> | <span data-ttu-id="8876d-175">Liste des alertes</span><span class="sxs-lookup"><span data-stu-id="8876d-175">Alert List</span></span> | <span data-ttu-id="8876d-176">Liste des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="8876d-176">List of related alerts.</span></span> <span data-ttu-id="8876d-177">Consultez des exemples dans la documentation [de l’API d’incidents](api-list-incidents.md) de liste.</span><span class="sxs-lookup"><span data-stu-id="8876d-177">See examples at [List incidents](api-list-incidents.md) API documentation.</span></span>

## <a name="related-articles"></a><span data-ttu-id="8876d-178">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="8876d-178">Related articles</span></span>

- [<span data-ttu-id="8876d-179">Présentation des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8876d-179">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="8876d-180">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="8876d-180">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="8876d-181">API de liste des incidents</span><span class="sxs-lookup"><span data-stu-id="8876d-181">List incidents API</span></span>](api-list-incidents.md)
- [<span data-ttu-id="8876d-182">API de mise à jour de l’incident</span><span class="sxs-lookup"><span data-stu-id="8876d-182">Update incident API</span></span>](api-update-incidents.md)
