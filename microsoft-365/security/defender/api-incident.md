---
title: Microsoft 365 API d’incidents Defender et type de ressource incidents
description: En savoir plus sur les méthodes et les propriétés du type de ressource Incidents dans Microsoft 365 Defender
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
ms.openlocfilehash: 587d6107b0c09b2178311d8da6606968e7fda083
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730929"
---
# <a name="microsoft-365-defender-incidents-api-and-the-incidents-resource-type"></a><span data-ttu-id="5ab23-104">Microsoft 365 API d’incidents Defender et type de ressource incidents</span><span class="sxs-lookup"><span data-stu-id="5ab23-104">Microsoft 365 Defender incidents API and the incidents resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="5ab23-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5ab23-105">**Applies to:**</span></span>

- [<span data-ttu-id="5ab23-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5ab23-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!IMPORTANT]
> <span data-ttu-id="5ab23-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="5ab23-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5ab23-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="5ab23-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="5ab23-109">Un [incident est](incidents-overview.md) un ensemble d’alertes associées qui permettent de décrire une attaque.</span><span class="sxs-lookup"><span data-stu-id="5ab23-109">An [incident](incidents-overview.md) is a collection of related alerts that help describe an attack.</span></span> <span data-ttu-id="5ab23-110">Les événements de différentes entités de votre organisation sont automatiquement regroupés par Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="5ab23-110">Events from different entities in your organization are automatically aggregated by Microsoft 365 Defender.</span></span> <span data-ttu-id="5ab23-111">Vous pouvez utiliser l’API d’incidents pour accéder par programmation aux incidents de votre organisation et aux alertes associées.</span><span class="sxs-lookup"><span data-stu-id="5ab23-111">You can use the incidents API to programatically access your organization's incidents and related alerts.</span></span>

## <a name="quotas-and-resource-allocation"></a><span data-ttu-id="5ab23-112">Quotas et allocation de ressources</span><span class="sxs-lookup"><span data-stu-id="5ab23-112">Quotas and resource allocation</span></span>

<span data-ttu-id="5ab23-113">Vous pouvez demander jusqu’à 50 appels par minute ou 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="5ab23-113">You can request up to 50 calls per minute or 1500 calls per hour.</span></span> <span data-ttu-id="5ab23-114">Chaque méthode possède également ses propres quotas.</span><span class="sxs-lookup"><span data-stu-id="5ab23-114">Each method also has its own quotas.</span></span> <span data-ttu-id="5ab23-115">Pour plus d’informations sur les quotas propres aux méthodes, consultez l’article respectif de la méthode que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="5ab23-115">For more information on method-specific quotas, see the respective article for the method you want to use.</span></span>

<span data-ttu-id="5ab23-116">Un code de réponse HTTP indique que vous avez atteint un quota, soit par nombre de demandes envoyées, soit par temps `429` d’exécution alloué.</span><span class="sxs-lookup"><span data-stu-id="5ab23-116">A `429` HTTP response code indicates that you've reached a quota, either by number of requests sent, or by allotted running time.</span></span> <span data-ttu-id="5ab23-117">Le corps de la réponse inclut la durée jusqu’à ce que le quota que vous avez atteint soit réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="5ab23-117">The response body will include the time until the quota you reached will be reset.</span></span>

## <a name="permissions"></a><span data-ttu-id="5ab23-118">Autorisations</span><span class="sxs-lookup"><span data-stu-id="5ab23-118">Permissions</span></span>

<span data-ttu-id="5ab23-119">L’API incidents nécessite différents types d’autorisations pour chacune de ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="5ab23-119">The incidents API requires different kinds of permissions for each of its methods.</span></span> <span data-ttu-id="5ab23-120">Pour plus d’informations sur les autorisations requises, consultez l’article de la méthode respective.</span><span class="sxs-lookup"><span data-stu-id="5ab23-120">For more information about required permissions, see the respective method's article.</span></span>

## <a name="methods"></a><span data-ttu-id="5ab23-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5ab23-121">Methods</span></span>

<span data-ttu-id="5ab23-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="5ab23-122">Method</span></span> | <span data-ttu-id="5ab23-123">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="5ab23-123">Return Type</span></span> | <span data-ttu-id="5ab23-124">Description</span><span class="sxs-lookup"><span data-stu-id="5ab23-124">Description</span></span>
-|-|-
[<span data-ttu-id="5ab23-125">Répertorier les incidents</span><span class="sxs-lookup"><span data-stu-id="5ab23-125">List incidents</span></span>](api-list-incidents.md) | <span data-ttu-id="5ab23-126">[Liste des incidents](api-incident.md)</span><span class="sxs-lookup"><span data-stu-id="5ab23-126">[Incident](api-incident.md) list</span></span> | <span data-ttu-id="5ab23-127">Obtenir la liste des incidents.</span><span class="sxs-lookup"><span data-stu-id="5ab23-127">Get a list of incidents.</span></span>
[<span data-ttu-id="5ab23-128">Incident de mise à jour</span><span class="sxs-lookup"><span data-stu-id="5ab23-128">Update incident</span></span>](api-update-incidents.md) | [<span data-ttu-id="5ab23-129">Incident</span><span class="sxs-lookup"><span data-stu-id="5ab23-129">Incident</span></span>](api-incident.md) | <span data-ttu-id="5ab23-130">Mettre à jour un incident spécifique.</span><span class="sxs-lookup"><span data-stu-id="5ab23-130">Update a specific incident.</span></span>

## <a name="request-body-response-and-examples"></a><span data-ttu-id="5ab23-131">Corps de la demande, réponse et exemples</span><span class="sxs-lookup"><span data-stu-id="5ab23-131">Request body, response, and examples</span></span>

<span data-ttu-id="5ab23-132">Reportez-vous aux articles de méthode respectifs pour plus d’informations sur la construction d’une demande ou l’analyse d’une réponse, et pour obtenir des exemples pratiques.</span><span class="sxs-lookup"><span data-stu-id="5ab23-132">Refer to the respective method articles for more details on how to construct a request or parse a response, and for practical examples.</span></span>

## <a name="common-properties"></a><span data-ttu-id="5ab23-133">Propriétés courantes</span><span class="sxs-lookup"><span data-stu-id="5ab23-133">Common properties</span></span>

<span data-ttu-id="5ab23-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="5ab23-134">Property</span></span> | <span data-ttu-id="5ab23-135">Type</span><span class="sxs-lookup"><span data-stu-id="5ab23-135">Type</span></span> | <span data-ttu-id="5ab23-136">Description</span><span class="sxs-lookup"><span data-stu-id="5ab23-136">Description</span></span>
-|-|-
<span data-ttu-id="5ab23-137">incidentId</span><span class="sxs-lookup"><span data-stu-id="5ab23-137">incidentId</span></span> | <span data-ttu-id="5ab23-138">long</span><span class="sxs-lookup"><span data-stu-id="5ab23-138">long</span></span> | <span data-ttu-id="5ab23-139">ID unique de l’incident.</span><span class="sxs-lookup"><span data-stu-id="5ab23-139">Incident unique ID.</span></span>
<span data-ttu-id="5ab23-140">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="5ab23-140">redirectIncidentId</span></span> | <span data-ttu-id="5ab23-141">nullable long</span><span class="sxs-lookup"><span data-stu-id="5ab23-141">nullable long</span></span> | <span data-ttu-id="5ab23-142">L’ID d’incident dans le cas de l’incident en cours a été fusionné.</span><span class="sxs-lookup"><span data-stu-id="5ab23-142">The Incident ID the current Incident was merged to.</span></span>
<span data-ttu-id="5ab23-143">incidentName</span><span class="sxs-lookup"><span data-stu-id="5ab23-143">incidentName</span></span> | <span data-ttu-id="5ab23-144">string</span><span class="sxs-lookup"><span data-stu-id="5ab23-144">string</span></span> | <span data-ttu-id="5ab23-145">Nom de l’incident.</span><span class="sxs-lookup"><span data-stu-id="5ab23-145">The name of the Incident.</span></span>
<span data-ttu-id="5ab23-146">createdTime</span><span class="sxs-lookup"><span data-stu-id="5ab23-146">createdTime</span></span> | <span data-ttu-id="5ab23-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ab23-147">DateTimeOffset</span></span> | <span data-ttu-id="5ab23-148">Date et heure (en UTC) de création de l’incident.</span><span class="sxs-lookup"><span data-stu-id="5ab23-148">The date and time (in UTC) the Incident was created.</span></span>
<span data-ttu-id="5ab23-149">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="5ab23-149">lastUpdateTime</span></span> | <span data-ttu-id="5ab23-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ab23-150">DateTimeOffset</span></span> | <span data-ttu-id="5ab23-151">Date et heure (en UTC) de la dernière mise à jour de l’incident.</span><span class="sxs-lookup"><span data-stu-id="5ab23-151">The date and time (in UTC) the Incident was last updated.</span></span>
<span data-ttu-id="5ab23-152">assignedTo</span><span class="sxs-lookup"><span data-stu-id="5ab23-152">assignedTo</span></span> | <span data-ttu-id="5ab23-153">string</span><span class="sxs-lookup"><span data-stu-id="5ab23-153">string</span></span> | <span data-ttu-id="5ab23-154">Propriétaire de l’incident.</span><span class="sxs-lookup"><span data-stu-id="5ab23-154">Owner of the Incident.</span></span>
<span data-ttu-id="5ab23-155">Sévérité </span><span class="sxs-lookup"><span data-stu-id="5ab23-155">severity</span></span> | <span data-ttu-id="5ab23-156">Énum</span><span class="sxs-lookup"><span data-stu-id="5ab23-156">Enum</span></span> | <span data-ttu-id="5ab23-157">Gravité de l’incident.</span><span class="sxs-lookup"><span data-stu-id="5ab23-157">Severity of the Incident.</span></span> <span data-ttu-id="5ab23-158">Les valeurs possibles ```UnSpecified``` sont : , , et ```Informational``` ```Low``` ```Medium``` ```High``` .</span><span class="sxs-lookup"><span data-stu-id="5ab23-158">Possible values are: ```UnSpecified```, ```Informational```, ```Low```, ```Medium```, and ```High```.</span></span>
<span data-ttu-id="5ab23-159">status</span><span class="sxs-lookup"><span data-stu-id="5ab23-159">status</span></span> | <span data-ttu-id="5ab23-160">Énum</span><span class="sxs-lookup"><span data-stu-id="5ab23-160">Enum</span></span> | <span data-ttu-id="5ab23-161">Spécifie l’état actuel de l’incident.</span><span class="sxs-lookup"><span data-stu-id="5ab23-161">Specifies the current status of the incident.</span></span> <span data-ttu-id="5ab23-162">Les valeurs possibles ```Active``` sont : , et ```Resolved``` ```Redirected``` .</span><span class="sxs-lookup"><span data-stu-id="5ab23-162">Possible values are: ```Active```, ```Resolved```, and ```Redirected```.</span></span>
<span data-ttu-id="5ab23-163">classification</span><span class="sxs-lookup"><span data-stu-id="5ab23-163">classification</span></span> | <span data-ttu-id="5ab23-164">Énum</span><span class="sxs-lookup"><span data-stu-id="5ab23-164">Enum</span></span> | <span data-ttu-id="5ab23-165">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="5ab23-165">Specification of the incident.</span></span> <span data-ttu-id="5ab23-166">Les valeurs possibles sont les suivantes : ```Unknown```, ```FalsePositive``` et ```TruePositive```.</span><span class="sxs-lookup"><span data-stu-id="5ab23-166">Possible values are: ```Unknown```, ```FalsePositive```, ```TruePositive```.</span></span>
<span data-ttu-id="5ab23-167">détermination</span><span class="sxs-lookup"><span data-stu-id="5ab23-167">determination</span></span> | <span data-ttu-id="5ab23-168">Énum</span><span class="sxs-lookup"><span data-stu-id="5ab23-168">Enum</span></span> | <span data-ttu-id="5ab23-169">Spécifie la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="5ab23-169">Specifies the determination of the incident.</span></span> <span data-ttu-id="5ab23-170">Les valeurs possibles sont les suivantes : ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware``` et ```Other```.</span><span class="sxs-lookup"><span data-stu-id="5ab23-170">Possible values are: ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware```, ```Other```.</span></span>
<span data-ttu-id="5ab23-171">étiquettes</span><span class="sxs-lookup"><span data-stu-id="5ab23-171">tags</span></span> | <span data-ttu-id="5ab23-172">liste de chaînes</span><span class="sxs-lookup"><span data-stu-id="5ab23-172">string List</span></span> | <span data-ttu-id="5ab23-173">Liste des balises d’incident.</span><span class="sxs-lookup"><span data-stu-id="5ab23-173">List of Incident tags.</span></span>
<span data-ttu-id="5ab23-174">commentaires</span><span class="sxs-lookup"><span data-stu-id="5ab23-174">comments</span></span> | <span data-ttu-id="5ab23-175">Liste des commentaires sur les incidents</span><span class="sxs-lookup"><span data-stu-id="5ab23-175">List of incident comments</span></span> | <span data-ttu-id="5ab23-176">L’objet Incident Comment contient : chaîne de commentaire, chaîne createdBy et heure de date createTime.</span><span class="sxs-lookup"><span data-stu-id="5ab23-176">Incident Comment object contains: comment string, createdBy string, and createTime date time.</span></span>
<span data-ttu-id="5ab23-177">alerts</span><span class="sxs-lookup"><span data-stu-id="5ab23-177">alerts</span></span> | <span data-ttu-id="5ab23-178">Liste des alertes</span><span class="sxs-lookup"><span data-stu-id="5ab23-178">Alert List</span></span> | <span data-ttu-id="5ab23-179">Liste des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="5ab23-179">List of related alerts.</span></span> <span data-ttu-id="5ab23-180">Consultez des exemples dans la documentation [de l’API d’incidents](api-list-incidents.md) de liste.</span><span class="sxs-lookup"><span data-stu-id="5ab23-180">See examples at [List incidents](api-list-incidents.md) API documentation.</span></span>

## <a name="related-articles"></a><span data-ttu-id="5ab23-181">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="5ab23-181">Related articles</span></span>

- [<span data-ttu-id="5ab23-182">Microsoft 365 Vue d’ensemble des API Defender</span><span class="sxs-lookup"><span data-stu-id="5ab23-182">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="5ab23-183">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="5ab23-183">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="5ab23-184">API de liste des incidents</span><span class="sxs-lookup"><span data-stu-id="5ab23-184">List incidents API</span></span>](api-list-incidents.md)
- [<span data-ttu-id="5ab23-185">API de mise à jour de l’incident</span><span class="sxs-lookup"><span data-stu-id="5ab23-185">Update incident API</span></span>](api-update-incidents.md)
