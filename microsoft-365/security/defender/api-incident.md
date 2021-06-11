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
ms.openlocfilehash: 0c0c2e280f63076687a0854e25c47577b050a8f7
ms.sourcegitcommit: 03aa8ed22d9ef685a851e28c7d0cfb725732fe4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "52888432"
---
# <a name="microsoft-365-defender-incidents-api-and-the-incidents-resource-type"></a><span data-ttu-id="9f097-104">Microsoft 365 API d’incidents Defender et type de ressource incidents</span><span class="sxs-lookup"><span data-stu-id="9f097-104">Microsoft 365 Defender incidents API and the incidents resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="9f097-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9f097-105">**Applies to:**</span></span>

- [<span data-ttu-id="9f097-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9f097-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!IMPORTANT]
> <span data-ttu-id="9f097-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="9f097-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9f097-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="9f097-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="9f097-109">Un [incident](incidents-overview.md) est un ensemble d’alertes associées qui permettent de décrire une attaque.</span><span class="sxs-lookup"><span data-stu-id="9f097-109">An [incident](incidents-overview.md) is a collection of related alerts that help describe an attack.</span></span> <span data-ttu-id="9f097-110">Les événements de différentes entités de votre organisation sont regroupés automatiquement par Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="9f097-110">Events from different entities in your organization are automatically aggregated by Microsoft 365 Defender.</span></span> <span data-ttu-id="9f097-111">Vous pouvez utiliser l’API d’incidents pour accéder par programmation aux incidents de votre organisation et aux alertes associées.</span><span class="sxs-lookup"><span data-stu-id="9f097-111">You can use the incidents API to programatically access your organization's incidents and related alerts.</span></span>

## <a name="quotas-and-resource-allocation"></a><span data-ttu-id="9f097-112">Quotas et allocation de ressources</span><span class="sxs-lookup"><span data-stu-id="9f097-112">Quotas and resource allocation</span></span>

<span data-ttu-id="9f097-113">Vous pouvez demander jusqu’à 50 appels par minute ou 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="9f097-113">You can request up to 50 calls per minute or 1500 calls per hour.</span></span> <span data-ttu-id="9f097-114">Chaque méthode possède également ses propres quotas.</span><span class="sxs-lookup"><span data-stu-id="9f097-114">Each method also has its own quotas.</span></span> <span data-ttu-id="9f097-115">Pour plus d’informations sur les quotas propres aux méthodes, consultez l’article respectif de la méthode que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="9f097-115">For more information on method-specific quotas, see the respective article for the method you want to use.</span></span>

<span data-ttu-id="9f097-116">Un code de réponse HTTP indique que vous avez atteint un quota, soit par nombre de demandes envoyées, soit par temps `429` d’exécution alloué.</span><span class="sxs-lookup"><span data-stu-id="9f097-116">A `429` HTTP response code indicates that you've reached a quota, either by number of requests sent, or by allotted running time.</span></span> <span data-ttu-id="9f097-117">Le corps de la réponse inclut la durée jusqu’à ce que le quota que vous avez atteint soit réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="9f097-117">The response body will include the time until the quota you reached will be reset.</span></span>

## <a name="permissions"></a><span data-ttu-id="9f097-118">Autorisations</span><span class="sxs-lookup"><span data-stu-id="9f097-118">Permissions</span></span>

<span data-ttu-id="9f097-119">L’API incidents nécessite différents types d’autorisations pour chacune de ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="9f097-119">The incidents API requires different kinds of permissions for each of its methods.</span></span> <span data-ttu-id="9f097-120">Pour plus d’informations sur les autorisations requises, consultez l’article de la méthode respective.</span><span class="sxs-lookup"><span data-stu-id="9f097-120">For more information about required permissions, see the respective method's article.</span></span>

## <a name="methods"></a><span data-ttu-id="9f097-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9f097-121">Methods</span></span>

<span data-ttu-id="9f097-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="9f097-122">Method</span></span> | <span data-ttu-id="9f097-123">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="9f097-123">Return Type</span></span> | <span data-ttu-id="9f097-124">Description</span><span class="sxs-lookup"><span data-stu-id="9f097-124">Description</span></span>
-|-|-
[<span data-ttu-id="9f097-125">Répertorier les incidents</span><span class="sxs-lookup"><span data-stu-id="9f097-125">List incidents</span></span>](api-list-incidents.md) | <span data-ttu-id="9f097-126">[Liste des incidents](api-incident.md)</span><span class="sxs-lookup"><span data-stu-id="9f097-126">[Incident](api-incident.md) list</span></span> | <span data-ttu-id="9f097-127">Obtenir la liste des incidents.</span><span class="sxs-lookup"><span data-stu-id="9f097-127">Get a list of incidents.</span></span>
[<span data-ttu-id="9f097-128">Incident de mise à jour</span><span class="sxs-lookup"><span data-stu-id="9f097-128">Update incident</span></span>](api-update-incidents.md) | [<span data-ttu-id="9f097-129">Incident</span><span class="sxs-lookup"><span data-stu-id="9f097-129">Incident</span></span>](api-incident.md) | <span data-ttu-id="9f097-130">Mettre à jour un incident spécifique.</span><span class="sxs-lookup"><span data-stu-id="9f097-130">Update a specific incident.</span></span>
[<span data-ttu-id="9f097-131">Obtenir un incident</span><span class="sxs-lookup"><span data-stu-id="9f097-131">Get incident</span></span>](api-get-incident.md) | [<span data-ttu-id="9f097-132">Incident</span><span class="sxs-lookup"><span data-stu-id="9f097-132">Incident</span></span>](api-incident.md) | <span data-ttu-id="9f097-133">Obtenez un incident unique.</span><span class="sxs-lookup"><span data-stu-id="9f097-133">Get a single incident.</span></span>

## <a name="request-body-response-and-examples"></a><span data-ttu-id="9f097-134">Corps de la demande, réponse et exemples</span><span class="sxs-lookup"><span data-stu-id="9f097-134">Request body, response, and examples</span></span>

<span data-ttu-id="9f097-135">Reportez-vous aux articles de méthode respectifs pour plus d’informations sur la construction d’une demande ou l’analyse d’une réponse, et pour obtenir des exemples pratiques.</span><span class="sxs-lookup"><span data-stu-id="9f097-135">Refer to the respective method articles for more details on how to construct a request or parse a response, and for practical examples.</span></span>

## <a name="common-properties"></a><span data-ttu-id="9f097-136">Propriétés courantes</span><span class="sxs-lookup"><span data-stu-id="9f097-136">Common properties</span></span>

<span data-ttu-id="9f097-137">Propriété</span><span class="sxs-lookup"><span data-stu-id="9f097-137">Property</span></span> | <span data-ttu-id="9f097-138">Type</span><span class="sxs-lookup"><span data-stu-id="9f097-138">Type</span></span> | <span data-ttu-id="9f097-139">Description</span><span class="sxs-lookup"><span data-stu-id="9f097-139">Description</span></span>
-|-|-
<span data-ttu-id="9f097-140">incidentId</span><span class="sxs-lookup"><span data-stu-id="9f097-140">incidentId</span></span> | <span data-ttu-id="9f097-141">long</span><span class="sxs-lookup"><span data-stu-id="9f097-141">long</span></span> | <span data-ttu-id="9f097-142">ID unique de l’incident.</span><span class="sxs-lookup"><span data-stu-id="9f097-142">Incident unique ID.</span></span>
<span data-ttu-id="9f097-143">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="9f097-143">redirectIncidentId</span></span> | <span data-ttu-id="9f097-144">nullable long</span><span class="sxs-lookup"><span data-stu-id="9f097-144">nullable long</span></span> | <span data-ttu-id="9f097-145">L’ID d’incident dans le cas de l’incident en cours a été fusionné.</span><span class="sxs-lookup"><span data-stu-id="9f097-145">The Incident ID the current Incident was merged to.</span></span>
<span data-ttu-id="9f097-146">incidentName</span><span class="sxs-lookup"><span data-stu-id="9f097-146">incidentName</span></span> | <span data-ttu-id="9f097-147">string</span><span class="sxs-lookup"><span data-stu-id="9f097-147">string</span></span> | <span data-ttu-id="9f097-148">Nom de l’incident.</span><span class="sxs-lookup"><span data-stu-id="9f097-148">The name of the Incident.</span></span>
<span data-ttu-id="9f097-149">createdTime</span><span class="sxs-lookup"><span data-stu-id="9f097-149">createdTime</span></span> | <span data-ttu-id="9f097-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9f097-150">DateTimeOffset</span></span> | <span data-ttu-id="9f097-151">Date et heure (en UTC) de création de l’incident.</span><span class="sxs-lookup"><span data-stu-id="9f097-151">The date and time (in UTC) the Incident was created.</span></span>
<span data-ttu-id="9f097-152">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="9f097-152">lastUpdateTime</span></span> | <span data-ttu-id="9f097-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9f097-153">DateTimeOffset</span></span> | <span data-ttu-id="9f097-154">Date et heure (en UTC) de la dernière mise à jour de l’incident.</span><span class="sxs-lookup"><span data-stu-id="9f097-154">The date and time (in UTC) the Incident was last updated.</span></span>
<span data-ttu-id="9f097-155">assignedTo</span><span class="sxs-lookup"><span data-stu-id="9f097-155">assignedTo</span></span> | <span data-ttu-id="9f097-156">string</span><span class="sxs-lookup"><span data-stu-id="9f097-156">string</span></span> | <span data-ttu-id="9f097-157">Propriétaire de l’incident.</span><span class="sxs-lookup"><span data-stu-id="9f097-157">Owner of the Incident.</span></span>
<span data-ttu-id="9f097-158">Sévérité </span><span class="sxs-lookup"><span data-stu-id="9f097-158">severity</span></span> | <span data-ttu-id="9f097-159">Énum</span><span class="sxs-lookup"><span data-stu-id="9f097-159">Enum</span></span> | <span data-ttu-id="9f097-160">Gravité de l’incident.</span><span class="sxs-lookup"><span data-stu-id="9f097-160">Severity of the Incident.</span></span> <span data-ttu-id="9f097-161">Les valeurs possibles ```UnSpecified``` sont : , , et ```Informational``` ```Low``` ```Medium``` ```High``` .</span><span class="sxs-lookup"><span data-stu-id="9f097-161">Possible values are: ```UnSpecified```, ```Informational```, ```Low```, ```Medium```, and ```High```.</span></span>
<span data-ttu-id="9f097-162">status</span><span class="sxs-lookup"><span data-stu-id="9f097-162">status</span></span> | <span data-ttu-id="9f097-163">Énum</span><span class="sxs-lookup"><span data-stu-id="9f097-163">Enum</span></span> | <span data-ttu-id="9f097-164">Spécifie l’état actuel de l’incident.</span><span class="sxs-lookup"><span data-stu-id="9f097-164">Specifies the current status of the incident.</span></span> <span data-ttu-id="9f097-165">Les valeurs possibles ```Active``` sont : , et ```Resolved``` ```Redirected``` .</span><span class="sxs-lookup"><span data-stu-id="9f097-165">Possible values are: ```Active```, ```Resolved```, and ```Redirected```.</span></span>
<span data-ttu-id="9f097-166">classification</span><span class="sxs-lookup"><span data-stu-id="9f097-166">classification</span></span> | <span data-ttu-id="9f097-167">Énum</span><span class="sxs-lookup"><span data-stu-id="9f097-167">Enum</span></span> | <span data-ttu-id="9f097-168">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="9f097-168">Specification of the incident.</span></span> <span data-ttu-id="9f097-169">Les valeurs possibles sont les suivantes : ```Unknown```, ```FalsePositive``` et ```TruePositive```.</span><span class="sxs-lookup"><span data-stu-id="9f097-169">Possible values are: ```Unknown```, ```FalsePositive```, ```TruePositive```.</span></span>
<span data-ttu-id="9f097-170">détermination</span><span class="sxs-lookup"><span data-stu-id="9f097-170">determination</span></span> | <span data-ttu-id="9f097-171">Énum</span><span class="sxs-lookup"><span data-stu-id="9f097-171">Enum</span></span> | <span data-ttu-id="9f097-172">Spécifie la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="9f097-172">Specifies the determination of the incident.</span></span> <span data-ttu-id="9f097-173">Les valeurs possibles sont les suivantes : ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware``` et ```Other```.</span><span class="sxs-lookup"><span data-stu-id="9f097-173">Possible values are: ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware```, ```Other```.</span></span>
<span data-ttu-id="9f097-174">étiquettes</span><span class="sxs-lookup"><span data-stu-id="9f097-174">tags</span></span> | <span data-ttu-id="9f097-175">liste de chaînes</span><span class="sxs-lookup"><span data-stu-id="9f097-175">string List</span></span> | <span data-ttu-id="9f097-176">Liste des balises d’incident.</span><span class="sxs-lookup"><span data-stu-id="9f097-176">List of Incident tags.</span></span>
<span data-ttu-id="9f097-177">commentaires</span><span class="sxs-lookup"><span data-stu-id="9f097-177">comments</span></span> | <span data-ttu-id="9f097-178">Liste des commentaires sur les incidents</span><span class="sxs-lookup"><span data-stu-id="9f097-178">List of incident comments</span></span> | <span data-ttu-id="9f097-179">L’objet Incident Comment contient : chaîne de commentaire, chaîne createdBy et heure de date createTime.</span><span class="sxs-lookup"><span data-stu-id="9f097-179">Incident Comment object contains: comment string, createdBy string, and createTime date time.</span></span>
<span data-ttu-id="9f097-180">alerts</span><span class="sxs-lookup"><span data-stu-id="9f097-180">alerts</span></span> | <span data-ttu-id="9f097-181">Liste des alertes</span><span class="sxs-lookup"><span data-stu-id="9f097-181">Alert List</span></span> | <span data-ttu-id="9f097-182">Liste des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="9f097-182">List of related alerts.</span></span> <span data-ttu-id="9f097-183">Consultez des exemples dans la documentation [de l’API d’incidents](api-list-incidents.md) de liste.</span><span class="sxs-lookup"><span data-stu-id="9f097-183">See examples at [List incidents](api-list-incidents.md) API documentation.</span></span>

## <a name="related-articles"></a><span data-ttu-id="9f097-184">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="9f097-184">Related articles</span></span>

- [<span data-ttu-id="9f097-185">Microsoft 365 Vue d’ensemble des API Defender</span><span class="sxs-lookup"><span data-stu-id="9f097-185">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="9f097-186">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="9f097-186">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="9f097-187">API de liste des incidents</span><span class="sxs-lookup"><span data-stu-id="9f097-187">List incidents API</span></span>](api-list-incidents.md)
- [<span data-ttu-id="9f097-188">API de mise à jour de l’incident</span><span class="sxs-lookup"><span data-stu-id="9f097-188">Update incident API</span></span>](api-update-incidents.md)
