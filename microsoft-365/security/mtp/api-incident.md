---
title: API Microsoft 365 Defender incidents et type de ressource incident
description: En savoir plus sur les méthodes et les propriétés du type de ressource incident dans Microsoft 365 Defender
keywords: incident, incidents, API
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
ms.openlocfilehash: 372c939f5eed29832725e6b048735040ca7391d6
ms.sourcegitcommit: d6b1da2e12d55f69e4353289e90f5ae2f60066d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "49719333"
---
# <a name="microsoft-365-defender-incidents-api-and-the-incident-resource-type"></a><span data-ttu-id="d3d4b-104">API Microsoft 365 Defender incidents et type de ressource incident</span><span class="sxs-lookup"><span data-stu-id="d3d4b-104">Microsoft 365 Defender incidents API and the incident resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="d3d4b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d3d4b-105">**Applies to:**</span></span>

- <span data-ttu-id="d3d4b-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d3d4b-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3d4b-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d3d4b-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="d3d4b-109">Un [incident](incidents-overview.md) est une collection d’alertes associées qui permettent de décrire une attaque.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-109">An [incident](incidents-overview.md) is a collection of related alerts that help describe an attack.</span></span> <span data-ttu-id="d3d4b-110">Les événements provenant de différentes entités de votre organisation sont automatiquement regroupés par Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-110">Events from different entities in your organization are automatically aggregated by Microsoft 365 Defender.</span></span> <span data-ttu-id="d3d4b-111">Vous pouvez utiliser l’API incidents pour accéder par programmation aux incidents et alertes connexes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-111">You can use the incidents API to programatically access your organization's incidents and related alerts.</span></span>

## <a name="quotas-and-resource-allocation"></a><span data-ttu-id="d3d4b-112">Quotas et allocation des ressources</span><span class="sxs-lookup"><span data-stu-id="d3d4b-112">Quotas and resource allocation</span></span>

<span data-ttu-id="d3d4b-113">Vous pouvez demander jusqu’à 50 appels par minute ou 1500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-113">You can request up to 50 calls per minute or 1500 calls per hour.</span></span> <span data-ttu-id="d3d4b-114">Chaque méthode possède également ses propres quotas.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-114">Each method also has its own quotas.</span></span> <span data-ttu-id="d3d4b-115">Pour plus d’informations sur les quotas spécifiques aux méthodes, reportez-vous à l’article correspondant à la méthode que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-115">For more information on method-specific quotas, see the respective article for the method you want to use.</span></span>

<span data-ttu-id="d3d4b-116">Un `429` Code de réponse http indique que vous avez atteint un quota, soit le nombre de demandes envoyées, soit le temps d’exécution alloué.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-116">A `429` HTTP response code indicates that you've reached a quota, either by number of requests sent, or by allotted running time.</span></span> <span data-ttu-id="d3d4b-117">Le corps de la réponse inclura le temps jusqu’à ce que le quota que vous avez atteint soit réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-117">The response body will include the time until the quota you reached will be reset.</span></span>

## <a name="permissions"></a><span data-ttu-id="d3d4b-118">Autorisations</span><span class="sxs-lookup"><span data-stu-id="d3d4b-118">Permissions</span></span>

<span data-ttu-id="d3d4b-119">L’API incidents requiert différents types d’autorisations pour chacune de ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-119">The incidents API requires different kinds of permissions for each of its methods.</span></span> <span data-ttu-id="d3d4b-120">Pour plus d’informations sur les autorisations requises, reportez-vous à l’article de la méthode correspondante.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-120">For more information about required permissions, see the respective method's article.</span></span>

## <a name="methods"></a><span data-ttu-id="d3d4b-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d3d4b-121">Methods</span></span>

<span data-ttu-id="d3d4b-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="d3d4b-122">Method</span></span> | <span data-ttu-id="d3d4b-123">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="d3d4b-123">Return Type</span></span> | <span data-ttu-id="d3d4b-124">Description</span><span class="sxs-lookup"><span data-stu-id="d3d4b-124">Description</span></span>
-|-|-
[<span data-ttu-id="d3d4b-125">Répertorier les incidents</span><span class="sxs-lookup"><span data-stu-id="d3d4b-125">List incidents</span></span>](api-list-incidents.md) | <span data-ttu-id="d3d4b-126">Liste des [incidents](api-incident.md)</span><span class="sxs-lookup"><span data-stu-id="d3d4b-126">[Incident](api-incident.md) list</span></span> | <span data-ttu-id="d3d4b-127">Obtenir une liste d’incidents.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-127">Get a list of incidents.</span></span>
[<span data-ttu-id="d3d4b-128">Incident de mise à jour</span><span class="sxs-lookup"><span data-stu-id="d3d4b-128">Update incident</span></span>](api-update-incidents.md) | [<span data-ttu-id="d3d4b-129">Accessoire</span><span class="sxs-lookup"><span data-stu-id="d3d4b-129">Incident</span></span>](api-incident.md) | <span data-ttu-id="d3d4b-130">Mettre à jour un incident spécifique.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-130">Update a specific incident.</span></span>

## <a name="request-body-response-and-examples"></a><span data-ttu-id="d3d4b-131">Corps de la demande, réponse et exemples</span><span class="sxs-lookup"><span data-stu-id="d3d4b-131">Request body, response, and examples</span></span>

<span data-ttu-id="d3d4b-132">Reportez-vous aux Articles de la méthode pour obtenir plus de détails sur la façon de construire une requête ou d’analyser une réponse, ainsi que pour des exemples concrets.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-132">Refer to the respective method articles for more details on how to construct a request or parse a response, and for practical examples.</span></span>

## <a name="common-properties"></a><span data-ttu-id="d3d4b-133">Propriétés courantes</span><span class="sxs-lookup"><span data-stu-id="d3d4b-133">Common properties</span></span>

<span data-ttu-id="d3d4b-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="d3d4b-134">Property</span></span> | <span data-ttu-id="d3d4b-135">Type</span><span class="sxs-lookup"><span data-stu-id="d3d4b-135">Type</span></span> | <span data-ttu-id="d3d4b-136">Description</span><span class="sxs-lookup"><span data-stu-id="d3d4b-136">Description</span></span>
-|-|-
<span data-ttu-id="d3d4b-137">incidentId</span><span class="sxs-lookup"><span data-stu-id="d3d4b-137">incidentId</span></span> | <span data-ttu-id="d3d4b-138">long</span><span class="sxs-lookup"><span data-stu-id="d3d4b-138">long</span></span> | <span data-ttu-id="d3d4b-139">ID unique de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-139">Incident unique ID.</span></span>
<span data-ttu-id="d3d4b-140">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="d3d4b-140">redirectIncidentId</span></span> | <span data-ttu-id="d3d4b-141">long Nullable</span><span class="sxs-lookup"><span data-stu-id="d3d4b-141">nullable long</span></span> | <span data-ttu-id="d3d4b-142">ID d’incident vers lequel l’incident actuel a été fusionné.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-142">The Incident ID the current Incident was merged to.</span></span>
<span data-ttu-id="d3d4b-143">incidentName</span><span class="sxs-lookup"><span data-stu-id="d3d4b-143">incidentName</span></span> | <span data-ttu-id="d3d4b-144">string</span><span class="sxs-lookup"><span data-stu-id="d3d4b-144">string</span></span> | <span data-ttu-id="d3d4b-145">Nom de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-145">The name of the Incident.</span></span>
<span data-ttu-id="d3d4b-146">createdTime</span><span class="sxs-lookup"><span data-stu-id="d3d4b-146">createdTime</span></span> | <span data-ttu-id="d3d4b-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d3d4b-147">DateTimeOffset</span></span> | <span data-ttu-id="d3d4b-148">Date et heure (en UTC) de création de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-148">The date and time (in UTC) the Incident was created.</span></span>
<span data-ttu-id="d3d4b-149">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="d3d4b-149">lastUpdateTime</span></span> | <span data-ttu-id="d3d4b-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d3d4b-150">DateTimeOffset</span></span> | <span data-ttu-id="d3d4b-151">Date et heure de la dernière mise à jour de l’incident (en UTC).</span><span class="sxs-lookup"><span data-stu-id="d3d4b-151">The date and time (in UTC) the Incident was last updated.</span></span>
<span data-ttu-id="d3d4b-152">assignedTo</span><span class="sxs-lookup"><span data-stu-id="d3d4b-152">assignedTo</span></span> | <span data-ttu-id="d3d4b-153">string</span><span class="sxs-lookup"><span data-stu-id="d3d4b-153">string</span></span> | <span data-ttu-id="d3d4b-154">Propriétaire de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-154">Owner of the Incident.</span></span>
<span data-ttu-id="d3d4b-155">Sévérité </span><span class="sxs-lookup"><span data-stu-id="d3d4b-155">severity</span></span> | <span data-ttu-id="d3d4b-156">Énum</span><span class="sxs-lookup"><span data-stu-id="d3d4b-156">Enum</span></span> | <span data-ttu-id="d3d4b-157">Gravité de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-157">Severity of the Incident.</span></span> <span data-ttu-id="d3d4b-158">Les valeurs possibles sont les suivantes : ```UnSpecified``` , ```Informational``` ,, ```Low``` ```Medium``` et ```High``` .</span><span class="sxs-lookup"><span data-stu-id="d3d4b-158">Possible values are: ```UnSpecified```, ```Informational```, ```Low```, ```Medium```, and ```High```.</span></span>
<span data-ttu-id="d3d4b-159">status</span><span class="sxs-lookup"><span data-stu-id="d3d4b-159">status</span></span> | <span data-ttu-id="d3d4b-160">Énum</span><span class="sxs-lookup"><span data-stu-id="d3d4b-160">Enum</span></span> | <span data-ttu-id="d3d4b-161">Indique l’état actuel de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-161">Specifies the current status of the incident.</span></span> <span data-ttu-id="d3d4b-162">Les valeurs possibles sont les suivantes : ```Active``` , ```Resolved``` et ```Redirected``` .</span><span class="sxs-lookup"><span data-stu-id="d3d4b-162">Possible values are: ```Active```, ```Resolved```, and ```Redirected```.</span></span>
<span data-ttu-id="d3d4b-163">classification</span><span class="sxs-lookup"><span data-stu-id="d3d4b-163">classification</span></span> | <span data-ttu-id="d3d4b-164">Énum</span><span class="sxs-lookup"><span data-stu-id="d3d4b-164">Enum</span></span> | <span data-ttu-id="d3d4b-165">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-165">Specification of the incident.</span></span> <span data-ttu-id="d3d4b-166">Les valeurs possibles sont ```Unknown```, ```FalsePositive``` et ```TruePositive```.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-166">Possible values are: ```Unknown```, ```FalsePositive```, ```TruePositive```.</span></span>
<span data-ttu-id="d3d4b-167">indications</span><span class="sxs-lookup"><span data-stu-id="d3d4b-167">determination</span></span> | <span data-ttu-id="d3d4b-168">Énum</span><span class="sxs-lookup"><span data-stu-id="d3d4b-168">Enum</span></span> | <span data-ttu-id="d3d4b-169">Indique la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-169">Specifies the determination of the incident.</span></span> <span data-ttu-id="d3d4b-170">Les valeurs possibles sont les suivantes : ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware``` et ```Other```.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-170">Possible values are: ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware```, ```Other```.</span></span>
<span data-ttu-id="d3d4b-171">étiquettes</span><span class="sxs-lookup"><span data-stu-id="d3d4b-171">tags</span></span> | <span data-ttu-id="d3d4b-172">Liste de chaînes</span><span class="sxs-lookup"><span data-stu-id="d3d4b-172">string List</span></span> | <span data-ttu-id="d3d4b-173">Liste des balises incident.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-173">List of Incident tags.</span></span>
<span data-ttu-id="d3d4b-174">alerts</span><span class="sxs-lookup"><span data-stu-id="d3d4b-174">alerts</span></span> | <span data-ttu-id="d3d4b-175">Liste des alertes</span><span class="sxs-lookup"><span data-stu-id="d3d4b-175">Alert List</span></span> | <span data-ttu-id="d3d4b-176">Liste des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="d3d4b-176">List of related alerts.</span></span> <span data-ttu-id="d3d4b-177">Voir des exemples dans la documentation de l’API des [incidents de liste](api-list-incidents.md) .</span><span class="sxs-lookup"><span data-stu-id="d3d4b-177">See examples at [List incidents](api-list-incidents.md) API documentation.</span></span>

## <a name="related-articles"></a><span data-ttu-id="d3d4b-178">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="d3d4b-178">Related articles</span></span>

- [<span data-ttu-id="d3d4b-179">Vue d’ensemble des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d3d4b-179">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="d3d4b-180">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="d3d4b-180">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="d3d4b-181">API de liste des incidents</span><span class="sxs-lookup"><span data-stu-id="d3d4b-181">List incidents API</span></span>](api-list-incidents.md)
- [<span data-ttu-id="d3d4b-182">Mettre à jour l’API incident</span><span class="sxs-lookup"><span data-stu-id="d3d4b-182">Update incident API</span></span>](api-update-incidents.md)
