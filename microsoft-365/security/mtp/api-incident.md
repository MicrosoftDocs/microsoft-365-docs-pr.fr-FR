---
title: Type de ressource d’incident dans l’API Microsoft 365 Defender
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
ms.openlocfilehash: 68bee647cdd5687dbaad08ce3cd01b427dabf030
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48844019"
---
# <a name="incident-resource-type"></a><span data-ttu-id="2c9cd-104">Type de ressource d’incident</span><span class="sxs-lookup"><span data-stu-id="2c9cd-104">Incident resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="2c9cd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2c9cd-105">**Applies to:**</span></span>
- <span data-ttu-id="2c9cd-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2c9cd-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT] 
><span data-ttu-id="2c9cd-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2c9cd-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="methods"></a><span data-ttu-id="2c9cd-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2c9cd-109">Methods</span></span>

<span data-ttu-id="2c9cd-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="2c9cd-110">Method</span></span> |<span data-ttu-id="2c9cd-111">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="2c9cd-111">Return Type</span></span> |<span data-ttu-id="2c9cd-112">Description</span><span class="sxs-lookup"><span data-stu-id="2c9cd-112">Description</span></span>
:---|:---|:---
[<span data-ttu-id="2c9cd-113">Répertorier les incidents</span><span class="sxs-lookup"><span data-stu-id="2c9cd-113">List incidents</span></span>](api-list-incidents.md) | <span data-ttu-id="2c9cd-114">Liste des [incidents](api-incident.md)</span><span class="sxs-lookup"><span data-stu-id="2c9cd-114">[Incident](api-incident.md) list</span></span> | <span data-ttu-id="2c9cd-115">Obtenir une liste d’incidents.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-115">Get a list of incidents.</span></span>
[<span data-ttu-id="2c9cd-116">Incident de mise à jour</span><span class="sxs-lookup"><span data-stu-id="2c9cd-116">Update incident</span></span>](api-update-incidents.md) | [<span data-ttu-id="2c9cd-117">Accessoire</span><span class="sxs-lookup"><span data-stu-id="2c9cd-117">Incident</span></span>](api-incident.md) | <span data-ttu-id="2c9cd-118">Mettre à jour un incident spécifique.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-118">Update specific incident.</span></span>


## <a name="properties"></a><span data-ttu-id="2c9cd-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c9cd-119">Properties</span></span>

<span data-ttu-id="2c9cd-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="2c9cd-120">Property</span></span> |    <span data-ttu-id="2c9cd-121">Type</span><span class="sxs-lookup"><span data-stu-id="2c9cd-121">Type</span></span>    |    <span data-ttu-id="2c9cd-122">Description</span><span class="sxs-lookup"><span data-stu-id="2c9cd-122">Description</span></span>
:---|:---|:---
<span data-ttu-id="2c9cd-123">incidentId</span><span class="sxs-lookup"><span data-stu-id="2c9cd-123">incidentId</span></span> | <span data-ttu-id="2c9cd-124">long</span><span class="sxs-lookup"><span data-stu-id="2c9cd-124">long</span></span> | <span data-ttu-id="2c9cd-125">ID unique de l’incident.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-125">Incident unique ID.</span></span>
<span data-ttu-id="2c9cd-126">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="2c9cd-126">redirectIncidentId</span></span> | <span data-ttu-id="2c9cd-127">long Nullable</span><span class="sxs-lookup"><span data-stu-id="2c9cd-127">nullable long</span></span> | <span data-ttu-id="2c9cd-128">ID d’incident vers lequel l’incident actuel a été fusionné.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-128">The Incident ID the current Incident was merged to.</span></span>
<span data-ttu-id="2c9cd-129">incidentName</span><span class="sxs-lookup"><span data-stu-id="2c9cd-129">incidentName</span></span> | <span data-ttu-id="2c9cd-130">string</span><span class="sxs-lookup"><span data-stu-id="2c9cd-130">string</span></span> | <span data-ttu-id="2c9cd-131">Nom de l’incident.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-131">The name of the Incident.</span></span>
<span data-ttu-id="2c9cd-132">createdTime</span><span class="sxs-lookup"><span data-stu-id="2c9cd-132">createdTime</span></span> | <span data-ttu-id="2c9cd-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2c9cd-133">DateTimeOffset</span></span> | <span data-ttu-id="2c9cd-134">Date et heure (en UTC) de création de l’incident.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-134">The date and time (in UTC) the Incident was created.</span></span>
<span data-ttu-id="2c9cd-135">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="2c9cd-135">lastUpdateTime</span></span> | <span data-ttu-id="2c9cd-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2c9cd-136">DateTimeOffset</span></span> | <span data-ttu-id="2c9cd-137">Date et heure de la dernière mise à jour de l’incident (en UTC).</span><span class="sxs-lookup"><span data-stu-id="2c9cd-137">The date and time (in UTC) the Incident was last updated.</span></span>
<span data-ttu-id="2c9cd-138">assignedTo</span><span class="sxs-lookup"><span data-stu-id="2c9cd-138">assignedTo</span></span> | <span data-ttu-id="2c9cd-139">string</span><span class="sxs-lookup"><span data-stu-id="2c9cd-139">string</span></span> | <span data-ttu-id="2c9cd-140">Propriétaire de l’incident.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-140">Owner of the Incident.</span></span>
<span data-ttu-id="2c9cd-141">Sévérité </span><span class="sxs-lookup"><span data-stu-id="2c9cd-141">severity</span></span> | <span data-ttu-id="2c9cd-142">Énum</span><span class="sxs-lookup"><span data-stu-id="2c9cd-142">Enum</span></span> | <span data-ttu-id="2c9cd-143">Gravité de l’incident.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-143">Severity of the Incident.</span></span> <span data-ttu-id="2c9cd-144">Les valeurs possibles sont les suivantes : ```UnSpecified``` , ```Informational``` , ```Low``` ```Medium``` et ```High``` .</span><span class="sxs-lookup"><span data-stu-id="2c9cd-144">Possible values are: ```UnSpecified```, ```Informational```, ```Low```, ```Medium``` and ```High```.</span></span>
<span data-ttu-id="2c9cd-145">statut</span><span class="sxs-lookup"><span data-stu-id="2c9cd-145">status</span></span> | <span data-ttu-id="2c9cd-146">Énum</span><span class="sxs-lookup"><span data-stu-id="2c9cd-146">Enum</span></span> | <span data-ttu-id="2c9cd-147">Indique l’état actuel de l’incident.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-147">Specifies the current status of the incident.</span></span> <span data-ttu-id="2c9cd-148">Les valeurs possibles sont les suivantes : ```Active``` ```Resolved``` et ```Redirected``` .</span><span class="sxs-lookup"><span data-stu-id="2c9cd-148">Possible values are: ```Active```, ```Resolved``` and ```Redirected```.</span></span>
<span data-ttu-id="2c9cd-149">classification</span><span class="sxs-lookup"><span data-stu-id="2c9cd-149">classification</span></span> | <span data-ttu-id="2c9cd-150">Énum</span><span class="sxs-lookup"><span data-stu-id="2c9cd-150">Enum</span></span> | <span data-ttu-id="2c9cd-151">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-151">Specification of the incident.</span></span> <span data-ttu-id="2c9cd-152">Les valeurs possibles sont ```Unknown```, ```FalsePositive``` et ```TruePositive```.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-152">Possible values are: ```Unknown```, ```FalsePositive```, ```TruePositive```.</span></span>
<span data-ttu-id="2c9cd-153">indications</span><span class="sxs-lookup"><span data-stu-id="2c9cd-153">determination</span></span> | <span data-ttu-id="2c9cd-154">Énum</span><span class="sxs-lookup"><span data-stu-id="2c9cd-154">Enum</span></span> | <span data-ttu-id="2c9cd-155">Indique la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-155">Specifies the determination of the incident.</span></span> <span data-ttu-id="2c9cd-156">Les valeurs possibles sont les suivantes : ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware``` et ```Other```.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-156">Possible values are: ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware```, ```Other```.</span></span>
<span data-ttu-id="2c9cd-157">étiquettes</span><span class="sxs-lookup"><span data-stu-id="2c9cd-157">tags</span></span> | <span data-ttu-id="2c9cd-158">Liste de chaînes</span><span class="sxs-lookup"><span data-stu-id="2c9cd-158">string List</span></span> | <span data-ttu-id="2c9cd-159">Liste des balises incident.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-159">List of Incident tags.</span></span>
<span data-ttu-id="2c9cd-160">alerts</span><span class="sxs-lookup"><span data-stu-id="2c9cd-160">alerts</span></span> | <span data-ttu-id="2c9cd-161">Liste des alertes</span><span class="sxs-lookup"><span data-stu-id="2c9cd-161">Alert List</span></span> | <span data-ttu-id="2c9cd-162">Liste des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="2c9cd-162">List of related alerts.</span></span> <span data-ttu-id="2c9cd-163">Voir des exemples dans la documentation de l’API des [incidents de liste](api-list-incidents.md) .</span><span class="sxs-lookup"><span data-stu-id="2c9cd-163">See examples at [List incidents](api-list-incidents.md) API documentation.</span></span>
