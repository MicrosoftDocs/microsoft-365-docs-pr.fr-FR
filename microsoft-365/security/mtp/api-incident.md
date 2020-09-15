---
title: Type de ressource d’incident dans l’API de protection contre les menaces Microsoft
description: En savoir plus sur les méthodes et les propriétés du type de ressource incident dans Microsoft Threat Protection
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
ms.openlocfilehash: 310e3105c973223ea79373d770eb10f7753b917e
ms.sourcegitcommit: 9a275a13af3e063e80ce1bd3cd8142a095db92d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2020
ms.locfileid: "47650288"
---
# <a name="incident-resource-type"></a><span data-ttu-id="27e16-104">Type de ressource d’incident</span><span class="sxs-lookup"><span data-stu-id="27e16-104">Incident resource type</span></span>

<span data-ttu-id="27e16-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="27e16-105">**Applies to:**</span></span>
- <span data-ttu-id="27e16-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="27e16-106">Microsoft Threat Protection</span></span>

>[!IMPORTANT] 
><span data-ttu-id="27e16-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="27e16-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="27e16-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="27e16-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="methods"></a><span data-ttu-id="27e16-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="27e16-109">Methods</span></span>

<span data-ttu-id="27e16-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="27e16-110">Method</span></span> |<span data-ttu-id="27e16-111">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="27e16-111">Return Type</span></span> |<span data-ttu-id="27e16-112">Description</span><span class="sxs-lookup"><span data-stu-id="27e16-112">Description</span></span>
:---|:---|:---
[<span data-ttu-id="27e16-113">Répertorier les incidents</span><span class="sxs-lookup"><span data-stu-id="27e16-113">List incidents</span></span>](api-list-incidents.md) | <span data-ttu-id="27e16-114">Liste des [incidents](api-incident.md)</span><span class="sxs-lookup"><span data-stu-id="27e16-114">[Incident](api-incident.md) list</span></span> | <span data-ttu-id="27e16-115">Obtenir une liste d’incidents.</span><span class="sxs-lookup"><span data-stu-id="27e16-115">Get a list of incidents.</span></span>
[<span data-ttu-id="27e16-116">Mettre à jour l’incident</span><span class="sxs-lookup"><span data-stu-id="27e16-116">Update incident</span></span>](api-update-incidents.md) | [<span data-ttu-id="27e16-117">Accessoire</span><span class="sxs-lookup"><span data-stu-id="27e16-117">Incident</span></span>](api-incident.md) | <span data-ttu-id="27e16-118">Mettre à jour un incident spécifique.</span><span class="sxs-lookup"><span data-stu-id="27e16-118">Update specific incident.</span></span>


## <a name="properties"></a><span data-ttu-id="27e16-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="27e16-119">Properties</span></span>

<span data-ttu-id="27e16-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="27e16-120">Property</span></span> |    <span data-ttu-id="27e16-121">Type</span><span class="sxs-lookup"><span data-stu-id="27e16-121">Type</span></span>    |    <span data-ttu-id="27e16-122">Description</span><span class="sxs-lookup"><span data-stu-id="27e16-122">Description</span></span>
:---|:---|:---
<span data-ttu-id="27e16-123">incidentId</span><span class="sxs-lookup"><span data-stu-id="27e16-123">incidentId</span></span> | <span data-ttu-id="27e16-124">long</span><span class="sxs-lookup"><span data-stu-id="27e16-124">long</span></span> | <span data-ttu-id="27e16-125">ID unique de l’incident.</span><span class="sxs-lookup"><span data-stu-id="27e16-125">Incident unique ID.</span></span>
<span data-ttu-id="27e16-126">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="27e16-126">redirectIncidentId</span></span> | <span data-ttu-id="27e16-127">long Nullable</span><span class="sxs-lookup"><span data-stu-id="27e16-127">nullable long</span></span> | <span data-ttu-id="27e16-128">ID d’incident vers lequel l’incident actuel a été fusionné.</span><span class="sxs-lookup"><span data-stu-id="27e16-128">The Incident ID the current Incident was merged to.</span></span>
<span data-ttu-id="27e16-129">incidentName</span><span class="sxs-lookup"><span data-stu-id="27e16-129">incidentName</span></span> | <span data-ttu-id="27e16-130">string</span><span class="sxs-lookup"><span data-stu-id="27e16-130">string</span></span> | <span data-ttu-id="27e16-131">Nom de l’incident.</span><span class="sxs-lookup"><span data-stu-id="27e16-131">The name of the Incident.</span></span>
<span data-ttu-id="27e16-132">createdTime</span><span class="sxs-lookup"><span data-stu-id="27e16-132">createdTime</span></span> | <span data-ttu-id="27e16-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="27e16-133">DateTimeOffset</span></span> | <span data-ttu-id="27e16-134">Date et heure (en UTC) de création de l’incident.</span><span class="sxs-lookup"><span data-stu-id="27e16-134">The date and time (in UTC) the Incident was created.</span></span>
<span data-ttu-id="27e16-135">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="27e16-135">lastUpdateTime</span></span> | <span data-ttu-id="27e16-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="27e16-136">DateTimeOffset</span></span> | <span data-ttu-id="27e16-137">Date et heure de la dernière mise à jour de l’incident (en UTC).</span><span class="sxs-lookup"><span data-stu-id="27e16-137">The date and time (in UTC) the Incident was last updated.</span></span>
<span data-ttu-id="27e16-138">assignedTo</span><span class="sxs-lookup"><span data-stu-id="27e16-138">assignedTo</span></span> | <span data-ttu-id="27e16-139">string</span><span class="sxs-lookup"><span data-stu-id="27e16-139">string</span></span> | <span data-ttu-id="27e16-140">Propriétaire de l’incident.</span><span class="sxs-lookup"><span data-stu-id="27e16-140">Owner of the Incident.</span></span>
<span data-ttu-id="27e16-141">Sévérité </span><span class="sxs-lookup"><span data-stu-id="27e16-141">severity</span></span> | <span data-ttu-id="27e16-142">Énum</span><span class="sxs-lookup"><span data-stu-id="27e16-142">Enum</span></span> | <span data-ttu-id="27e16-143">Gravité de l’incident.</span><span class="sxs-lookup"><span data-stu-id="27e16-143">Severity of the Incident.</span></span> <span data-ttu-id="27e16-144">Les valeurs possibles sont les suivantes : ```UnSpecified``` , ```Informational``` , ```Low``` ```Medium``` et ```High``` .</span><span class="sxs-lookup"><span data-stu-id="27e16-144">Possible values are: ```UnSpecified```, ```Informational```, ```Low```, ```Medium``` and ```High```.</span></span>
<span data-ttu-id="27e16-145">statut</span><span class="sxs-lookup"><span data-stu-id="27e16-145">status</span></span> | <span data-ttu-id="27e16-146">Énum</span><span class="sxs-lookup"><span data-stu-id="27e16-146">Enum</span></span> | <span data-ttu-id="27e16-147">Indique l’état actuel de l’incident.</span><span class="sxs-lookup"><span data-stu-id="27e16-147">Specifies the current status of the incident.</span></span> <span data-ttu-id="27e16-148">Les valeurs possibles sont les suivantes : ```Active``` ```Resolved``` et ```Redirected``` .</span><span class="sxs-lookup"><span data-stu-id="27e16-148">Possible values are: ```Active```, ```Resolved``` and ```Redirected```.</span></span>
<span data-ttu-id="27e16-149">classification</span><span class="sxs-lookup"><span data-stu-id="27e16-149">classification</span></span> | <span data-ttu-id="27e16-150">Énum</span><span class="sxs-lookup"><span data-stu-id="27e16-150">Enum</span></span> | <span data-ttu-id="27e16-151">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="27e16-151">Specification of the incident.</span></span> <span data-ttu-id="27e16-152">Les valeurs possibles sont les suivantes : ```Unknown```, ```FalsePositive``` et ```TruePositive```.</span><span class="sxs-lookup"><span data-stu-id="27e16-152">Possible values are: ```Unknown```, ```FalsePositive```, ```TruePositive```.</span></span>
<span data-ttu-id="27e16-153">indications</span><span class="sxs-lookup"><span data-stu-id="27e16-153">determination</span></span> | <span data-ttu-id="27e16-154">Énum</span><span class="sxs-lookup"><span data-stu-id="27e16-154">Enum</span></span> | <span data-ttu-id="27e16-155">Indique la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="27e16-155">Specifies the determination of the incident.</span></span> <span data-ttu-id="27e16-156">Les valeurs possibles sont les suivantes : ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware``` et ```Other```.</span><span class="sxs-lookup"><span data-stu-id="27e16-156">Possible values are: ```NotAvailable```, ```Apt```, ```Malware```, ```SecurityPersonnel```, ```SecurityTesting```, ```UnwantedSoftware```, ```Other```.</span></span>
<span data-ttu-id="27e16-157">étiquettes</span><span class="sxs-lookup"><span data-stu-id="27e16-157">tags</span></span> | <span data-ttu-id="27e16-158">Liste de chaînes</span><span class="sxs-lookup"><span data-stu-id="27e16-158">string List</span></span> | <span data-ttu-id="27e16-159">Liste des balises incident.</span><span class="sxs-lookup"><span data-stu-id="27e16-159">List of Incident tags.</span></span>
<span data-ttu-id="27e16-160">alerts</span><span class="sxs-lookup"><span data-stu-id="27e16-160">alerts</span></span> | <span data-ttu-id="27e16-161">Liste des alertes</span><span class="sxs-lookup"><span data-stu-id="27e16-161">Alert List</span></span> | <span data-ttu-id="27e16-162">Liste des alertes associées.</span><span class="sxs-lookup"><span data-stu-id="27e16-162">List of related alerts.</span></span> <span data-ttu-id="27e16-163">Voir des exemples dans la documentation de l’API des [incidents de liste](api-list-incidents.md) .</span><span class="sxs-lookup"><span data-stu-id="27e16-163">See examples at [List incidents](api-list-incidents.md) API documentation.</span></span>