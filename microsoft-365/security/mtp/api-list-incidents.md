---
title: API de liste des incidents dans Microsoft 365 Defender
description: Découvrez comment lister les API d’incidents dans Microsoft 365 Defender
keywords: liste, incident, incidents, api
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
ms.openlocfilehash: 39a170a1845ab33f67d77b2de3d5f298f67fdc99
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49932069"
---
# <a name="list-incidents-api-in-microsoft-365-defender"></a><span data-ttu-id="8376f-104">API de liste des incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8376f-104">List incidents API in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="8376f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8376f-105">**Applies to:**</span></span>

- <span data-ttu-id="8376f-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8376f-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8376f-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8376f-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8376f-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="8376f-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


## <a name="api-description"></a><span data-ttu-id="8376f-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="8376f-109">API description</span></span>

<span data-ttu-id="8376f-110">L’API d’incidents de liste vous permet de trier les incidents pour créer une réponse de cybersécurité informée.</span><span class="sxs-lookup"><span data-stu-id="8376f-110">The list incidents API allows you to sort through incidents to create an informed cybersecurity response.</span></span> <span data-ttu-id="8376f-111">Il expose un ensemble d’incidents qui ont été signalés dans votre réseau, dans la plage de temps que vous avez spécifiée dans votre stratégie de rétention d’environnement.</span><span class="sxs-lookup"><span data-stu-id="8376f-111">It exposes a collection of incidents that were flagged in your network, within the time range you specified in your environment retention policy.</span></span> <span data-ttu-id="8376f-112">Les incidents les plus récents sont affichés en haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="8376f-112">The most recent incidents are displayed at the top of the list.</span></span> <span data-ttu-id="8376f-113">Chaque incident contient un tableau d’alertes associées et leurs entités connexes.</span><span class="sxs-lookup"><span data-stu-id="8376f-113">Each incident contains an array of related alerts, and their related entities.</span></span>

<span data-ttu-id="8376f-114">L’API prend en charge les opérateurs **OData suivants** :</span><span class="sxs-lookup"><span data-stu-id="8376f-114">The API supports the following **OData** operators:</span></span>

- <span data-ttu-id="8376f-115">`$filter`sur `lastUpdateTime` les `createdTime` propriétés `status` , et `assignedTo`</span><span class="sxs-lookup"><span data-stu-id="8376f-115">`$filter` on the `lastUpdateTime`, `createdTime`, `status`, and `assignedTo` properties</span></span>
- <span data-ttu-id="8376f-116">`$top`, avec une valeur maximale de **100**</span><span class="sxs-lookup"><span data-stu-id="8376f-116">`$top`, with a maximum value of **100**</span></span>
- `$skip`

## <a name="limitations"></a><span data-ttu-id="8376f-117">Limites</span><span class="sxs-lookup"><span data-stu-id="8376f-117">Limitations</span></span>

1. <span data-ttu-id="8376f-118">La taille maximale de page **est de 100 incidents.**</span><span class="sxs-lookup"><span data-stu-id="8376f-118">Maximum page size is **100 incidents**.</span></span>
2. <span data-ttu-id="8376f-119">Le taux maximal de demandes est **de 50 appels par minute** et de **1 500 appels par heure.**</span><span class="sxs-lookup"><span data-stu-id="8376f-119">Maximum rate of requests is **50 calls per minute** and **1500 calls per hour**.</span></span>

## <a name="permissions"></a><span data-ttu-id="8376f-120">Autorisations</span><span class="sxs-lookup"><span data-stu-id="8376f-120">Permissions</span></span>

<span data-ttu-id="8376f-121">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="8376f-121">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="8376f-122">Pour en savoir plus, notamment sur le choix des autorisations, consultez les API [Microsoft 365 Defender Access](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="8376f-122">To learn more, including how to choose permissions, see [Access Microsoft 365 Defender APIs](api-access.md)</span></span>

<span data-ttu-id="8376f-123">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="8376f-123">Permission type</span></span> | <span data-ttu-id="8376f-124">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8376f-124">Permission</span></span> | <span data-ttu-id="8376f-125">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="8376f-125">Permission display name</span></span>
-|-|-
<span data-ttu-id="8376f-126">Application</span><span class="sxs-lookup"><span data-stu-id="8376f-126">Application</span></span> | <span data-ttu-id="8376f-127">Incident.Read.All</span><span class="sxs-lookup"><span data-stu-id="8376f-127">Incident.Read.All</span></span> | <span data-ttu-id="8376f-128">Lire tous les incidents</span><span class="sxs-lookup"><span data-stu-id="8376f-128">Read all incidents</span></span>
<span data-ttu-id="8376f-129">Application</span><span class="sxs-lookup"><span data-stu-id="8376f-129">Application</span></span> | <span data-ttu-id="8376f-130">Incident.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8376f-130">Incident.ReadWrite.All</span></span> | <span data-ttu-id="8376f-131">Lire et écrire tous les incidents</span><span class="sxs-lookup"><span data-stu-id="8376f-131">Read and write all incidents</span></span>
<span data-ttu-id="8376f-132">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="8376f-132">Delegated (work or school account)</span></span> | <span data-ttu-id="8376f-133">Incident.Read</span><span class="sxs-lookup"><span data-stu-id="8376f-133">Incident.Read</span></span> | <span data-ttu-id="8376f-134">Lire les incidents</span><span class="sxs-lookup"><span data-stu-id="8376f-134">Read incidents</span></span>
<span data-ttu-id="8376f-135">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="8376f-135">Delegated (work or school account)</span></span> | <span data-ttu-id="8376f-136">Incident.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8376f-136">Incident.ReadWrite</span></span> | <span data-ttu-id="8376f-137">Lire et écrire des incidents</span><span class="sxs-lookup"><span data-stu-id="8376f-137">Read and write incidents</span></span>

> [!Note]
> <span data-ttu-id="8376f-138">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="8376f-138">When obtaining a token using user credentials:</span></span>
>
> - <span data-ttu-id="8376f-139">L’utilisateur doit avoir l’autorisation d’afficher les incidents dans le portail.</span><span class="sxs-lookup"><span data-stu-id="8376f-139">The user needs to have view permission for incidents in the portal.</span></span>
> - <span data-ttu-id="8376f-140">La réponse inclut uniquement les incidents que l’utilisateur est exposé.</span><span class="sxs-lookup"><span data-stu-id="8376f-140">The response will only include incidents that the user is exposed to.</span></span>

## <a name="http-request"></a><span data-ttu-id="8376f-141">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="8376f-141">HTTP request</span></span>

```HTTP
GET /api/incidents
```

## <a name="request-headers"></a><span data-ttu-id="8376f-142">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="8376f-142">Request headers</span></span>

<span data-ttu-id="8376f-143">Nom</span><span class="sxs-lookup"><span data-stu-id="8376f-143">Name</span></span> | <span data-ttu-id="8376f-144">Type</span><span class="sxs-lookup"><span data-stu-id="8376f-144">Type</span></span> | <span data-ttu-id="8376f-145">Description</span><span class="sxs-lookup"><span data-stu-id="8376f-145">Description</span></span>
-|-|-
<span data-ttu-id="8376f-146">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8376f-146">Authorization</span></span> | <span data-ttu-id="8376f-147">String</span><span class="sxs-lookup"><span data-stu-id="8376f-147">String</span></span> | <span data-ttu-id="8376f-148">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="8376f-148">Bearer {token}.</span></span> <span data-ttu-id="8376f-149">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="8376f-149">**Required**</span></span>


## <a name="request-body"></a><span data-ttu-id="8376f-150">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="8376f-150">Request body</span></span>

<span data-ttu-id="8376f-151">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8376f-151">None.</span></span>

## <a name="response"></a><span data-ttu-id="8376f-152">Réponse</span><span class="sxs-lookup"><span data-stu-id="8376f-152">Response</span></span>

<span data-ttu-id="8376f-153">Si elle réussit, cette méthode renvoie `200 OK` et une liste des [incidents](api-incident.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="8376f-153">If successful, this method returns `200 OK`, and a list of [incidents](api-incident.md) in the response body.</span></span>

## <a name="schema-mapping"></a><span data-ttu-id="8376f-154">Mappage de schéma</span><span class="sxs-lookup"><span data-stu-id="8376f-154">Schema mapping</span></span>

### <a name="incident-metadata"></a><span data-ttu-id="8376f-155">Métadonnées d’incident</span><span class="sxs-lookup"><span data-stu-id="8376f-155">Incident metadata</span></span>

<span data-ttu-id="8376f-156">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="8376f-156">Field name</span></span> | <span data-ttu-id="8376f-157">Description</span><span class="sxs-lookup"><span data-stu-id="8376f-157">Description</span></span> | <span data-ttu-id="8376f-158">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="8376f-158">Example value</span></span>
-|-|-
<span data-ttu-id="8376f-159">incidentId</span><span class="sxs-lookup"><span data-stu-id="8376f-159">incidentId</span></span> | <span data-ttu-id="8376f-160">Identificateur unique pour représenter l’incident</span><span class="sxs-lookup"><span data-stu-id="8376f-160">Unique identifier to represent the incident</span></span> | <span data-ttu-id="8376f-161">924565</span><span class="sxs-lookup"><span data-stu-id="8376f-161">924565</span></span>
<span data-ttu-id="8376f-162">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="8376f-162">redirectIncidentId</span></span> | <span data-ttu-id="8376f-163">Uniquement rempli au cas où un incident est regroupé avec un autre incident, dans le cadre de la logique de traitement des incidents.</span><span class="sxs-lookup"><span data-stu-id="8376f-163">Only populated in case an incident is being grouped together with another incident, as part of the incident processing logic.</span></span> | <span data-ttu-id="8376f-164">924569</span><span class="sxs-lookup"><span data-stu-id="8376f-164">924569</span></span>
<span data-ttu-id="8376f-165">incidentName</span><span class="sxs-lookup"><span data-stu-id="8376f-165">incidentName</span></span> | <span data-ttu-id="8376f-166">Valeur de chaîne disponible pour chaque incident.</span><span class="sxs-lookup"><span data-stu-id="8376f-166">String value available for every incident.</span></span> | <span data-ttu-id="8376f-167">Activité de ransomware</span><span class="sxs-lookup"><span data-stu-id="8376f-167">Ransomware activity</span></span>
<span data-ttu-id="8376f-168">createdTime</span><span class="sxs-lookup"><span data-stu-id="8376f-168">createdTime</span></span> | <span data-ttu-id="8376f-169">Heure à partir de la première création de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8376f-169">Time when incident was first created.</span></span> | <span data-ttu-id="8376f-170">2020-09-06T14:46:57.0733333Z</span><span class="sxs-lookup"><span data-stu-id="8376f-170">2020-09-06T14:46:57.0733333Z</span></span>
<span data-ttu-id="8376f-171">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="8376f-171">lastUpdateTime</span></span> | <span data-ttu-id="8376f-172">Heure de la dernière mise à jour de l’incident sur le back-end.</span><span class="sxs-lookup"><span data-stu-id="8376f-172">Time when the incident was last updated on the backend.</span></span><br /><br /> <span data-ttu-id="8376f-173">Ce champ peut être utilisé lorsque vous paramétrez le paramètre de demande pour la durée de récupération des incidents.</span><span class="sxs-lookup"><span data-stu-id="8376f-173">This field can be used when you're setting the request parameter for the range of time that incidents are retrieved.</span></span> | <span data-ttu-id="8376f-174">2020-09-06T14:46:57.29Z</span><span class="sxs-lookup"><span data-stu-id="8376f-174">2020-09-06T14:46:57.29Z</span></span>
<span data-ttu-id="8376f-175">assignedTo</span><span class="sxs-lookup"><span data-stu-id="8376f-175">assignedTo</span></span> | <span data-ttu-id="8376f-176">Propriétaire de l’incident ou *null* si aucun propriétaire n’est affecté.</span><span class="sxs-lookup"><span data-stu-id="8376f-176">Owner of the incident, or *null* if no owner is assigned.</span></span> | <span data-ttu-id="8376f-177">secop2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8376f-177">secop2@contoso.com</span></span>
<span data-ttu-id="8376f-178">classification</span><span class="sxs-lookup"><span data-stu-id="8376f-178">classification</span></span> | <span data-ttu-id="8376f-179">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8376f-179">The specification for the incident.</span></span> <span data-ttu-id="8376f-180">Les valeurs de propriété *sont : Unknown*, *FalsePositive*, *TruePositive*</span><span class="sxs-lookup"><span data-stu-id="8376f-180">The property values are: *Unknown*, *FalsePositive*, *TruePositive*</span></span> | <span data-ttu-id="8376f-181">Inconnu</span><span class="sxs-lookup"><span data-stu-id="8376f-181">Unknown</span></span>
<span data-ttu-id="8376f-182">détermination</span><span class="sxs-lookup"><span data-stu-id="8376f-182">determination</span></span> | <span data-ttu-id="8376f-183">Spécifie la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8376f-183">Specifies the determination of the incident.</span></span> <span data-ttu-id="8376f-184">Les valeurs de propriété *sont : NotAvailable*, *Apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *Other*</span><span class="sxs-lookup"><span data-stu-id="8376f-184">The property values are: *NotAvailable*, *Apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *Other*</span></span> | <span data-ttu-id="8376f-185">NotAvailable</span><span class="sxs-lookup"><span data-stu-id="8376f-185">NotAvailable</span></span>
<span data-ttu-id="8376f-186">statut</span><span class="sxs-lookup"><span data-stu-id="8376f-186">status</span></span> | <span data-ttu-id="8376f-187">Catégoriser les incidents *(en tant qu’incidents actifs* *ou résolus).*</span><span class="sxs-lookup"><span data-stu-id="8376f-187">Categorize incidents (as *Active*, or *Resolved*).</span></span> <span data-ttu-id="8376f-188">Il peut vous aider à organiser et à gérer votre réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="8376f-188">It can help you organize and manage your response to incidents.</span></span> | <span data-ttu-id="8376f-189">Actif</span><span class="sxs-lookup"><span data-stu-id="8376f-189">Active</span></span>
<span data-ttu-id="8376f-190">Sévérité </span><span class="sxs-lookup"><span data-stu-id="8376f-190">severity</span></span> | <span data-ttu-id="8376f-191">Indique l’impact possible sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="8376f-191">Indicates the possible impact on assets.</span></span> <span data-ttu-id="8376f-192">Plus la gravité est élevée, plus l’impact est important.</span><span class="sxs-lookup"><span data-stu-id="8376f-192">The higher the severity the bigger the impact.</span></span> <span data-ttu-id="8376f-193">En règle générale, les éléments de gravité plus élevée nécessitent l’attention la plus immédiate.</span><span class="sxs-lookup"><span data-stu-id="8376f-193">Typically higher severity items require the most immediate attention.</span></span><br /><br /><span data-ttu-id="8376f-194">Une des valeurs suivantes *: Informational,* \*Low,\*\*Medium et *High*.</span><span class="sxs-lookup"><span data-stu-id="8376f-194">One of the following values: *Informational*, *Low*, \*Medium, and *High*.</span></span> | <span data-ttu-id="8376f-195">Moyen</span><span class="sxs-lookup"><span data-stu-id="8376f-195">Medium</span></span>
<span data-ttu-id="8376f-196">étiquettes</span><span class="sxs-lookup"><span data-stu-id="8376f-196">tags</span></span> | <span data-ttu-id="8376f-197">Tableau de balises personnalisées associées à un incident, par exemple pour baliser un groupe d’incidents avec une caractéristique commune.</span><span class="sxs-lookup"><span data-stu-id="8376f-197">Array of custom tags associated with an incident, for example to flag a group of incidents with a common characteristic.</span></span> | \[\]
<span data-ttu-id="8376f-198">alerts</span><span class="sxs-lookup"><span data-stu-id="8376f-198">alerts</span></span> | <span data-ttu-id="8376f-199">Tableau contenant toutes les alertes liées à l’incident, ainsi que d’autres informations, telles que la gravité, les entités impliquées dans l’alerte et la source des alertes.</span><span class="sxs-lookup"><span data-stu-id="8376f-199">Array containing all of the alerts related to the incident, plus other information, such as severity, entities that were involved in the alert, and the source of the alerts.</span></span> | <span data-ttu-id="8376f-200">\[\] (voir les détails sur les champs d’alerte ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="8376f-200">\[\] (see details on alert fields below)</span></span>

### <a name="alerts-metadata"></a><span data-ttu-id="8376f-201">Métadonnées des alertes</span><span class="sxs-lookup"><span data-stu-id="8376f-201">Alerts metadata</span></span>

<span data-ttu-id="8376f-202">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="8376f-202">Field name</span></span> | <span data-ttu-id="8376f-203">Description</span><span class="sxs-lookup"><span data-stu-id="8376f-203">Description</span></span> | <span data-ttu-id="8376f-204">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="8376f-204">Example value</span></span>
-|-|-
<span data-ttu-id="8376f-205">alertId</span><span class="sxs-lookup"><span data-stu-id="8376f-205">alertId</span></span> | <span data-ttu-id="8376f-206">Identificateur unique pour représenter l’alerte</span><span class="sxs-lookup"><span data-stu-id="8376f-206">Unique identifier to represent the alert</span></span> | <span data-ttu-id="8376f-207">caD70CFEE2-1F54-32DB-9988-3A868A1EBFAC</span><span class="sxs-lookup"><span data-stu-id="8376f-207">caD70CFEE2-1F54-32DB-9988-3A868A1EBFAC</span></span>
<span data-ttu-id="8376f-208">incidentId</span><span class="sxs-lookup"><span data-stu-id="8376f-208">incidentId</span></span> | <span data-ttu-id="8376f-209">Identificateur unique représentant l’incident associé à cette alerte</span><span class="sxs-lookup"><span data-stu-id="8376f-209">Unique identifier to represent the incident this alert is associated with</span></span> | <span data-ttu-id="8376f-210">924565</span><span class="sxs-lookup"><span data-stu-id="8376f-210">924565</span></span>
<span data-ttu-id="8376f-211">serviceSource</span><span class="sxs-lookup"><span data-stu-id="8376f-211">serviceSource</span></span> | <span data-ttu-id="8376f-212">Service dont provient l’alerte, tel que Microsoft Defender pour le point de terminaison, Microsoft Cloud App Security, Microsoft Defender pour l’identité ou Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="8376f-212">Service that the alert originates from, such as Microsoft Defender for Endpoint, Microsoft Cloud App Security, Microsoft Defender for Identity, or Microsoft Defender for Office 365.</span></span> | <span data-ttu-id="8376f-213">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="8376f-213">MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="8376f-214">creationTime</span><span class="sxs-lookup"><span data-stu-id="8376f-214">creationTime</span></span> | <span data-ttu-id="8376f-215">Heure à partir de la première création de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="8376f-215">Time when alert was first created.</span></span> | <span data-ttu-id="8376f-216">2020-09-06T14:46:55.7182276Z</span><span class="sxs-lookup"><span data-stu-id="8376f-216">2020-09-06T14:46:55.7182276Z</span></span>
<span data-ttu-id="8376f-217">lastUpdatedTime</span><span class="sxs-lookup"><span data-stu-id="8376f-217">lastUpdatedTime</span></span> | <span data-ttu-id="8376f-218">Heure de la dernière mise à jour de l’alerte sur le système arrière.</span><span class="sxs-lookup"><span data-stu-id="8376f-218">Time when alert was last updated at the backend.</span></span> | <span data-ttu-id="8376f-219">2020-09-06T14:46:57.2433333Z</span><span class="sxs-lookup"><span data-stu-id="8376f-219">2020-09-06T14:46:57.2433333Z</span></span>
<span data-ttu-id="8376f-220">resolvedTime</span><span class="sxs-lookup"><span data-stu-id="8376f-220">resolvedTime</span></span> | <span data-ttu-id="8376f-221">Heure de résolution de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="8376f-221">Time when alert was resolved.</span></span> | <span data-ttu-id="8376f-222">2020-09-10T05:22:59Z</span><span class="sxs-lookup"><span data-stu-id="8376f-222">2020-09-10T05:22:59Z</span></span>
<span data-ttu-id="8376f-223">firstActivity</span><span class="sxs-lookup"><span data-stu-id="8376f-223">firstActivity</span></span> | <span data-ttu-id="8376f-224">Heure à partir de la première alerte signalé que l’activité a été mise à jour sur le système back-end.</span><span class="sxs-lookup"><span data-stu-id="8376f-224">Time when alert first reported that activity was updated at the backend.</span></span>| <span data-ttu-id="8376f-225">2020-09-04T05:22:59Z</span><span class="sxs-lookup"><span data-stu-id="8376f-225">2020-09-04T05:22:59Z</span></span>
<span data-ttu-id="8376f-226">titre</span><span class="sxs-lookup"><span data-stu-id="8376f-226">title</span></span> | <span data-ttu-id="8376f-227">Brève identification de la valeur de chaîne disponible pour chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="8376f-227">Brief identifying string value available for each alert.</span></span> | <span data-ttu-id="8376f-228">Activité de ransomware</span><span class="sxs-lookup"><span data-stu-id="8376f-228">Ransomware activity</span></span>
<span data-ttu-id="8376f-229">description</span><span class="sxs-lookup"><span data-stu-id="8376f-229">description</span></span> | <span data-ttu-id="8376f-230">Valeur de chaîne décrivant chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="8376f-230">String value describing each alert.</span></span> | <span data-ttu-id="8376f-231">L’utilisateur Test User2 (testUser2@contoso.com) a manipulé 99 fichiers avec plusieurs extensions se terminant par l’extension *rare herunterladen*.</span><span class="sxs-lookup"><span data-stu-id="8376f-231">The user Test User2 (testUser2@contoso.com) manipulated 99 files with multiple extensions ending with the uncommon extension *herunterladen*.</span></span> <span data-ttu-id="8376f-232">Il s’agit d’un nombre inhabituel de manipulations de fichiers et qui indique une attaque potentielle par ransomware.</span><span class="sxs-lookup"><span data-stu-id="8376f-232">This is an unusual number of file manipulations and is indicative of a potential ransomware attack.</span></span>
<span data-ttu-id="8376f-233">category</span><span class="sxs-lookup"><span data-stu-id="8376f-233">category</span></span> | <span data-ttu-id="8376f-234">Affichage visuel et numérique de la progression de l’attaque tout au long de la chaîne d’attaque.</span><span class="sxs-lookup"><span data-stu-id="8376f-234">Visual and numeric view of how far the attack has progressed along the kill chain.</span></span> <span data-ttu-id="8376f-235">Aligné sur l’infrastructure [CK&ATT MITRE™.](https://attack.mitre.org/)</span><span class="sxs-lookup"><span data-stu-id="8376f-235">Aligned to the [MITRE ATT&CK™ framework](https://attack.mitre.org/).</span></span> | <span data-ttu-id="8376f-236">Impact</span><span class="sxs-lookup"><span data-stu-id="8376f-236">Impact</span></span>
<span data-ttu-id="8376f-237">statut</span><span class="sxs-lookup"><span data-stu-id="8376f-237">status</span></span> | <span data-ttu-id="8376f-238">Catégoriser les alertes *(en tant* que Nouveau, *Actif* *ou Résolu).*</span><span class="sxs-lookup"><span data-stu-id="8376f-238">Categorize alerts (as *New*, *Active*, or *Resolved*).</span></span> <span data-ttu-id="8376f-239">Il peut vous aider à organiser et à gérer votre réponse aux alertes.</span><span class="sxs-lookup"><span data-stu-id="8376f-239">It can help you organize and manage your response to alerts.</span></span> | <span data-ttu-id="8376f-240">Nouveau</span><span class="sxs-lookup"><span data-stu-id="8376f-240">New</span></span>
<span data-ttu-id="8376f-241">Sévérité </span><span class="sxs-lookup"><span data-stu-id="8376f-241">severity</span></span> | <span data-ttu-id="8376f-242">Indique l’impact possible sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="8376f-242">Indicates the possible impact on assets.</span></span> <span data-ttu-id="8376f-243">Plus la gravité est élevée, plus l’impact est important.</span><span class="sxs-lookup"><span data-stu-id="8376f-243">The higher the severity the bigger the impact.</span></span> <span data-ttu-id="8376f-244">En règle générale, les éléments de gravité plus élevée nécessitent l’attention la plus immédiate.</span><span class="sxs-lookup"><span data-stu-id="8376f-244">Typically higher severity items require the most immediate attention.</span></span><br><span data-ttu-id="8376f-245">Une des valeurs suivantes *: Informational,* \*Low,\*\*Medium et *High*.</span><span class="sxs-lookup"><span data-stu-id="8376f-245">One of the following values: *Informational*, *Low*, \*Medium, and *High*.</span></span> | <span data-ttu-id="8376f-246">Moyen</span><span class="sxs-lookup"><span data-stu-id="8376f-246">Medium</span></span>
<span data-ttu-id="8376f-247">investigationId</span><span class="sxs-lookup"><span data-stu-id="8376f-247">investigationId</span></span> | <span data-ttu-id="8376f-248">ID d’examen automatisé déclenché par cette alerte.</span><span class="sxs-lookup"><span data-stu-id="8376f-248">The automated investigation ID triggered by this alert.</span></span> | <span data-ttu-id="8376f-249">1234</span><span class="sxs-lookup"><span data-stu-id="8376f-249">1234</span></span>
<span data-ttu-id="8376f-250">investigationState</span><span class="sxs-lookup"><span data-stu-id="8376f-250">investigationState</span></span> | <span data-ttu-id="8376f-251">Informations sur l’état actuel de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="8376f-251">Information on the investigation's current status.</span></span> <span data-ttu-id="8376f-252">Une des valeurs suivantes : *Unknown*, *Terminated*, *SuccessfullyRemediated*, *Suppressed*, *Failed*, *PartiallyRemediated*, *Running*, *PendingApproval*, *PendingResource*, *PartiallyMediaigated*, *TerminatedByUser*, *TerminatedBySystem*, *Queued*, *InnerFailure*, *PreexistingAlert*, *UnsupportedOs*, *UnsupportedAlertType*, *SuppressedAlert*.</span><span class="sxs-lookup"><span data-stu-id="8376f-252">One of the following values: *Unknown*, *Terminated*, *SuccessfullyRemediated*, *Benign*, *Failed*, *PartiallyRemediated*, *Running*, *PendingApproval*, *PendingResource*, *PartiallyInvestigated*, *TerminatedByUser*, *TerminatedBySystem*, *Queued*, *InnerFailure*, *PreexistingAlert*, *UnsupportedOs*, *UnsupportedAlertType*, *SuppressedAlert*.</span></span> | <span data-ttu-id="8376f-253">UnsupportedAlertType</span><span class="sxs-lookup"><span data-stu-id="8376f-253">UnsupportedAlertType</span></span>
<span data-ttu-id="8376f-254">classification</span><span class="sxs-lookup"><span data-stu-id="8376f-254">classification</span></span> | <span data-ttu-id="8376f-255">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8376f-255">The specification for the incident.</span></span> <span data-ttu-id="8376f-256">Les valeurs de propriété *sont : Unknown*, *FalsePositive*, *TruePositive* ou *null*</span><span class="sxs-lookup"><span data-stu-id="8376f-256">The property values are: *Unknown*, *FalsePositive*, *TruePositive*, or *null*</span></span> | <span data-ttu-id="8376f-257">Inconnu</span><span class="sxs-lookup"><span data-stu-id="8376f-257">Unknown</span></span>
<span data-ttu-id="8376f-258">détermination</span><span class="sxs-lookup"><span data-stu-id="8376f-258">determination</span></span> | <span data-ttu-id="8376f-259">Spécifie la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8376f-259">Specifies the determination of the incident.</span></span> <span data-ttu-id="8376f-260">Les valeurs de propriété sont *: NotAvailable*, *Apt*, *Malware*, SecurityPersonnel , *SecurityTesting*, *UnwantedSoftware*, *Other* ou *null* </span><span class="sxs-lookup"><span data-stu-id="8376f-260">The property values are: *NotAvailable*, *Apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *Other* or  *null*</span></span> | <span data-ttu-id="8376f-261">Apt</span><span class="sxs-lookup"><span data-stu-id="8376f-261">Apt</span></span>
<span data-ttu-id="8376f-262">assignedTo</span><span class="sxs-lookup"><span data-stu-id="8376f-262">assignedTo</span></span> | <span data-ttu-id="8376f-263">Propriétaire de l’incident ou *null* si aucun propriétaire n’est affecté.</span><span class="sxs-lookup"><span data-stu-id="8376f-263">Owner of the incident, or *null* if no owner is assigned.</span></span> | <span data-ttu-id="8376f-264">secop2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8376f-264">secop2@contoso.com</span></span>
<span data-ttu-id="8376f-265">actorName</span><span class="sxs-lookup"><span data-stu-id="8376f-265">actorName</span></span> | <span data-ttu-id="8376f-266">Le groupe d’activités, le caser, le groupe associé à cette alerte.</span><span class="sxs-lookup"><span data-stu-id="8376f-266">The activity group, if any, the  associated with this alert.</span></span> | <span data-ttu-id="8376f-267">BORON</span><span class="sxs-lookup"><span data-stu-id="8376f-267">BORON</span></span>
<span data-ttu-id="8376f-268">threatFamilyName</span><span class="sxs-lookup"><span data-stu-id="8376f-268">threatFamilyName</span></span> | <span data-ttu-id="8376f-269">Famille de menaces associée à cette alerte.</span><span class="sxs-lookup"><span data-stu-id="8376f-269">Threat family associated with this alert.</span></span> | <span data-ttu-id="8376f-270">null</span><span class="sxs-lookup"><span data-stu-id="8376f-270">null</span></span>
<span data-ttu-id="8376f-271">mitreTechniques</span><span class="sxs-lookup"><span data-stu-id="8376f-271">mitreTechniques</span></span> | <span data-ttu-id="8376f-272">Les techniques d’attaque, telles qu’alignées avec l’infrastructure&[CK ™ MITRE ATT.](https://attack.mitre.org/)</span><span class="sxs-lookup"><span data-stu-id="8376f-272">The attack techniques, as aligned with the [MITRE ATT&CK](https://attack.mitre.org/)™ framework.</span></span> | \[\]
<span data-ttu-id="8376f-273">appareils</span><span class="sxs-lookup"><span data-stu-id="8376f-273">devices</span></span> | <span data-ttu-id="8376f-274">Tous les appareils sur lequel des alertes liées à l’incident ont été envoyées.</span><span class="sxs-lookup"><span data-stu-id="8376f-274">All devices where alerts related to the incident were sent.</span></span> | <span data-ttu-id="8376f-275">\[\] (voir les détails sur les champs d’entité ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="8376f-275">\[\] (see details on entity fields below)</span></span>

### <a name="device-format"></a><span data-ttu-id="8376f-276">Format de l’appareil</span><span class="sxs-lookup"><span data-stu-id="8376f-276">Device format</span></span>

<span data-ttu-id="8376f-277">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="8376f-277">Field name</span></span> | <span data-ttu-id="8376f-278">Description</span><span class="sxs-lookup"><span data-stu-id="8376f-278">Description</span></span> | <span data-ttu-id="8376f-279">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="8376f-279">Example value</span></span>
-|-|-
<span data-ttu-id="8376f-280">DeviceId</span><span class="sxs-lookup"><span data-stu-id="8376f-280">DeviceId</span></span> | <span data-ttu-id="8376f-281">ID d’appareil désigné dans Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="8376f-281">The device ID as designated in Microsoft Defender ATP.</span></span> | <span data-ttu-id="8376f-282">24c222b0b60fe148eeece49ac83910cc6a7ef491</span><span class="sxs-lookup"><span data-stu-id="8376f-282">24c222b0b60fe148eeece49ac83910cc6a7ef491</span></span>
<span data-ttu-id="8376f-283">aadDeviceId</span><span class="sxs-lookup"><span data-stu-id="8376f-283">aadDeviceId</span></span> |  <span data-ttu-id="8376f-284">ID d’appareil désigné dans [Azure Active Directory.](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)</span><span class="sxs-lookup"><span data-stu-id="8376f-284">The device ID as designated in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis).</span></span> <span data-ttu-id="8376f-285">Disponible uniquement pour les appareils joints au domaine.</span><span class="sxs-lookup"><span data-stu-id="8376f-285">Only available for domain-joined devices.</span></span> | <span data-ttu-id="8376f-286">null</span><span class="sxs-lookup"><span data-stu-id="8376f-286">null</span></span>
<span data-ttu-id="8376f-287">deviceDnsName</span><span class="sxs-lookup"><span data-stu-id="8376f-287">deviceDnsName</span></span> | <span data-ttu-id="8376f-288">Nom de domaine complet de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8376f-288">The fully qualified domain name for the device.</span></span> | <span data-ttu-id="8376f-289">user5cx.middleeast.corp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="8376f-289">user5cx.middleeast.corp.contoso.com</span></span>
<span data-ttu-id="8376f-290">osPlatform</span><span class="sxs-lookup"><span data-stu-id="8376f-290">osPlatform</span></span> | <span data-ttu-id="8376f-291">Plateforme du système d’exploitation en cours d’exécution de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8376f-291">The OS platform the device is running.</span></span>| <span data-ttu-id="8376f-292">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="8376f-292">WindowsServer2016</span></span>
<span data-ttu-id="8376f-293">osBuild</span><span class="sxs-lookup"><span data-stu-id="8376f-293">osBuild</span></span> | <span data-ttu-id="8376f-294">Version de build du système d’exploitation que l’appareil exécute.</span><span class="sxs-lookup"><span data-stu-id="8376f-294">The build version for the OS the device is running.</span></span> | <span data-ttu-id="8376f-295">14393</span><span class="sxs-lookup"><span data-stu-id="8376f-295">14393</span></span>
<span data-ttu-id="8376f-296">rbacGroupName</span><span class="sxs-lookup"><span data-stu-id="8376f-296">rbacGroupName</span></span> | <span data-ttu-id="8376f-297">Groupe [de contrôle d’accès](https://docs.microsoft.com/azure/role-based-access-control/overview) basé sur un rôle (RBAC) associé à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8376f-297">The [role-based access control](https://docs.microsoft.com/azure/role-based-access-control/overview) (RBAC) group associated with the device.</span></span> | <span data-ttu-id="8376f-298">WDATP-Ring0</span><span class="sxs-lookup"><span data-stu-id="8376f-298">WDATP-Ring0</span></span>
<span data-ttu-id="8376f-299">firstSeen</span><span class="sxs-lookup"><span data-stu-id="8376f-299">firstSeen</span></span> | <span data-ttu-id="8376f-300">Heure de la première fois où l’appareil a été vu.</span><span class="sxs-lookup"><span data-stu-id="8376f-300">Time when device was first seen.</span></span> | <span data-ttu-id="8376f-301">2020-02-06T14:16:01.9330135Z</span><span class="sxs-lookup"><span data-stu-id="8376f-301">2020-02-06T14:16:01.9330135Z</span></span>
<span data-ttu-id="8376f-302">healthStatus</span><span class="sxs-lookup"><span data-stu-id="8376f-302">healthStatus</span></span> | <span data-ttu-id="8376f-303">État d’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8376f-303">The health state of the device.</span></span> | <span data-ttu-id="8376f-304">Actif</span><span class="sxs-lookup"><span data-stu-id="8376f-304">Active</span></span>
<span data-ttu-id="8376f-305">riskScore</span><span class="sxs-lookup"><span data-stu-id="8376f-305">riskScore</span></span> | <span data-ttu-id="8376f-306">Score de risque pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8376f-306">The risk score for the  device.</span></span> | <span data-ttu-id="8376f-307">Élevé</span><span class="sxs-lookup"><span data-stu-id="8376f-307">High</span></span>
<span data-ttu-id="8376f-308">entities</span><span class="sxs-lookup"><span data-stu-id="8376f-308">entities</span></span> | <span data-ttu-id="8376f-309">Toutes les entités qui ont été identifiées comme faisant partie ou associées à une alerte donnée.</span><span class="sxs-lookup"><span data-stu-id="8376f-309">All entities that have been identified to be part of, or related to, a given alert.</span></span> | <span data-ttu-id="8376f-310">\[\] (voir les détails sur les champs d’entité ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="8376f-310">\[\] (see details on entity fields below)</span></span>

### <a name="entity-format"></a><span data-ttu-id="8376f-311">Format d’entité</span><span class="sxs-lookup"><span data-stu-id="8376f-311">Entity Format</span></span>

<span data-ttu-id="8376f-312">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="8376f-312">Field name</span></span> | <span data-ttu-id="8376f-313">Description</span><span class="sxs-lookup"><span data-stu-id="8376f-313">Description</span></span> | <span data-ttu-id="8376f-314">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="8376f-314">Example value</span></span>
-|-|-
<span data-ttu-id="8376f-315">entityType</span><span class="sxs-lookup"><span data-stu-id="8376f-315">entityType</span></span> | <span data-ttu-id="8376f-316">Entités identifiées comme faisant partie d’une alerte donnée ou associées à celle-là.</span><span class="sxs-lookup"><span data-stu-id="8376f-316">Entities that have been identified to be part of, or related to, a given alert.</span></span><br><span data-ttu-id="8376f-317">Les valeurs des propriétés sont *: User*, *Ip*, *Url*, *File*, *Process*, *MailBox*, *MailMessage*, *MailCluster*, *Registry*</span><span class="sxs-lookup"><span data-stu-id="8376f-317">The properties values are: *User*, *Ip*, *Url*, *File*, *Process*, *MailBox*, *MailMessage*, *MailCluster*, *Registry*</span></span> | <span data-ttu-id="8376f-318">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="8376f-318">User</span></span>
<span data-ttu-id="8376f-319">sha1</span><span class="sxs-lookup"><span data-stu-id="8376f-319">sha1</span></span> | <span data-ttu-id="8376f-320">Disponible si entityType est *File*.</span><span class="sxs-lookup"><span data-stu-id="8376f-320">Available if entityType is *File*.</span></span><br><span data-ttu-id="8376f-321">Hachage du fichier pour les alertes associées à un fichier ou un processus.</span><span class="sxs-lookup"><span data-stu-id="8376f-321">The file hash for alerts associated with a file or process.</span></span> | <span data-ttu-id="8376f-322">5de839186691aa96ee2ca6d74f0a38fb8d1bd6dd</span><span class="sxs-lookup"><span data-stu-id="8376f-322">5de839186691aa96ee2ca6d74f0a38fb8d1bd6dd</span></span>
<span data-ttu-id="8376f-323">sha256</span><span class="sxs-lookup"><span data-stu-id="8376f-323">sha256</span></span> | <span data-ttu-id="8376f-324">Disponible si entityType est *File*.</span><span class="sxs-lookup"><span data-stu-id="8376f-324">Available if entityType is *File*.</span></span><br><span data-ttu-id="8376f-325">Hachage du fichier pour les alertes associées à un fichier ou un processus.</span><span class="sxs-lookup"><span data-stu-id="8376f-325">The file hash for alerts associated with a file or process.</span></span> | <span data-ttu-id="8376f-326">28cb017dfc99073aa1b47c1b30f413e3ce774c4991eb4158de50f9dbb36d8043</span><span class="sxs-lookup"><span data-stu-id="8376f-326">28cb017dfc99073aa1b47c1b30f413e3ce774c4991eb4158de50f9dbb36d8043</span></span>
<span data-ttu-id="8376f-327">fileName</span><span class="sxs-lookup"><span data-stu-id="8376f-327">fileName</span></span> | <span data-ttu-id="8376f-328">Disponible si entityType est *File*.</span><span class="sxs-lookup"><span data-stu-id="8376f-328">Available if entityType is *File*.</span></span><br><span data-ttu-id="8376f-329">Nom de fichier des alertes associées à un fichier ou un processus</span><span class="sxs-lookup"><span data-stu-id="8376f-329">The file name for alerts associated with a file or process</span></span> | <span data-ttu-id="8376f-330">Detector.UnitTests.dll</span><span class="sxs-lookup"><span data-stu-id="8376f-330">Detector.UnitTests.dll</span></span>
<span data-ttu-id="8376f-331">filePath</span><span class="sxs-lookup"><span data-stu-id="8376f-331">filePath</span></span> | <span data-ttu-id="8376f-332">Disponible si entityType est *File*.</span><span class="sxs-lookup"><span data-stu-id="8376f-332">Available if entityType is *File*.</span></span><br><span data-ttu-id="8376f-333">Chemin d’accès au fichier pour les alertes associées à un fichier ou un processus</span><span class="sxs-lookup"><span data-stu-id="8376f-333">The file path for alerts associated with a file or process</span></span> | <span data-ttu-id="8376f-334">C : \\ \agent_work_temp\Deploy\SYSTEM\2020-09-06 12_14_54\Out</span><span class="sxs-lookup"><span data-stu-id="8376f-334">C:\\\agent_work_temp\Deploy\SYSTEM\2020-09-06 12_14_54\Out</span></span>
<span data-ttu-id="8376f-335">processId</span><span class="sxs-lookup"><span data-stu-id="8376f-335">processId</span></span> | <span data-ttu-id="8376f-336">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="8376f-336">Available if entityType is *Process*.</span></span> | <span data-ttu-id="8376f-337">24348</span><span class="sxs-lookup"><span data-stu-id="8376f-337">24348</span></span>
<span data-ttu-id="8376f-338">processCommandLine</span><span class="sxs-lookup"><span data-stu-id="8376f-338">processCommandLine</span></span> | <span data-ttu-id="8376f-339">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="8376f-339">Available if entityType is *Process*.</span></span> | <span data-ttu-id="8376f-340">« Votre fichier est prêt à être téléchargé \_1911150169.exe »</span><span class="sxs-lookup"><span data-stu-id="8376f-340">"Your File Is Ready To Download\_1911150169.exe"</span></span>
<span data-ttu-id="8376f-341">processCreationTime</span><span class="sxs-lookup"><span data-stu-id="8376f-341">processCreationTime</span></span> | <span data-ttu-id="8376f-342">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="8376f-342">Available if entityType is *Process*.</span></span> | <span data-ttu-id="8376f-343">2020-07-18T03:25:38.5269993Z</span><span class="sxs-lookup"><span data-stu-id="8376f-343">2020-07-18T03:25:38.5269993Z</span></span>
<span data-ttu-id="8376f-344">parentProcessId</span><span class="sxs-lookup"><span data-stu-id="8376f-344">parentProcessId</span></span> | <span data-ttu-id="8376f-345">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="8376f-345">Available if entityType is *Process*.</span></span> | <span data-ttu-id="8376f-346">16840</span><span class="sxs-lookup"><span data-stu-id="8376f-346">16840</span></span>
<span data-ttu-id="8376f-347">parentProcessCreationTime</span><span class="sxs-lookup"><span data-stu-id="8376f-347">parentProcessCreationTime</span></span> | <span data-ttu-id="8376f-348">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="8376f-348">Available if entityType is *Process*.</span></span> | <span data-ttu-id="8376f-349">2020-07-18T02:12:32.8616797Z</span><span class="sxs-lookup"><span data-stu-id="8376f-349">2020-07-18T02:12:32.8616797Z</span></span>
<span data-ttu-id="8376f-350">ipAddress</span><span class="sxs-lookup"><span data-stu-id="8376f-350">ipAddress</span></span> | <span data-ttu-id="8376f-351">Disponible si entityType est *Ip*.</span><span class="sxs-lookup"><span data-stu-id="8376f-351">Available if entityType is *Ip*.</span></span> <br><span data-ttu-id="8376f-352">Adresse IP des alertes associées aux événements réseau, telles que la *communication vers une destination réseau malveillante.*</span><span class="sxs-lookup"><span data-stu-id="8376f-352">IP address for alerts associated with network events, such as *Communication to a malicious network destination*.</span></span> | <span data-ttu-id="8376f-353">62.216.203.204</span><span class="sxs-lookup"><span data-stu-id="8376f-353">62.216.203.204</span></span>
<span data-ttu-id="8376f-354">url</span><span class="sxs-lookup"><span data-stu-id="8376f-354">url</span></span> | <span data-ttu-id="8376f-355">Disponible si entityType est *l’URL*.</span><span class="sxs-lookup"><span data-stu-id="8376f-355">Available if entityType is *Url*.</span></span> <br><span data-ttu-id="8376f-356">URL des alertes associées aux événements réseau, telles que la communication vers *une destination réseau malveillante.*</span><span class="sxs-lookup"><span data-stu-id="8376f-356">Url for alerts associated to network events, such as, *Communication to a malicious network destination*.</span></span> | <span data-ttu-id="8376f-357">down.esales360.cn</span><span class="sxs-lookup"><span data-stu-id="8376f-357">down.esales360.cn</span></span>
<span data-ttu-id="8376f-358">accountName</span><span class="sxs-lookup"><span data-stu-id="8376f-358">accountName</span></span> | <span data-ttu-id="8376f-359">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="8376f-359">Available if entityType is *User*.</span></span> | <span data-ttu-id="8376f-360">testUser2</span><span class="sxs-lookup"><span data-stu-id="8376f-360">testUser2</span></span>
<span data-ttu-id="8376f-361">domainName</span><span class="sxs-lookup"><span data-stu-id="8376f-361">domainName</span></span> | <span data-ttu-id="8376f-362">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="8376f-362">Available if entityType is *User*.</span></span> | <span data-ttu-id="8376f-363">europe.corp.contoso</span><span class="sxs-lookup"><span data-stu-id="8376f-363">europe.corp.contoso</span></span>
<span data-ttu-id="8376f-364">userSid</span><span class="sxs-lookup"><span data-stu-id="8376f-364">userSid</span></span> | <span data-ttu-id="8376f-365">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="8376f-365">Available if entityType is *User*.</span></span> | <span data-ttu-id="8376f-366">S-1-5-21-1721254763-462695806-1538882281-4156657</span><span class="sxs-lookup"><span data-stu-id="8376f-366">S-1-5-21-1721254763-462695806-1538882281-4156657</span></span>
<span data-ttu-id="8376f-367">aadUserId</span><span class="sxs-lookup"><span data-stu-id="8376f-367">aadUserId</span></span> | <span data-ttu-id="8376f-368">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="8376f-368">Available if entityType is *User*.</span></span> | <span data-ttu-id="8376f-369">fc8f7484-f813-4db2-afab-bc1507913fb6</span><span class="sxs-lookup"><span data-stu-id="8376f-369">fc8f7484-f813-4db2-afab-bc1507913fb6</span></span>
<span data-ttu-id="8376f-370">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8376f-370">userPrincipalName</span></span> | <span data-ttu-id="8376f-371">Disponible si entityType est *User* / *MailBox* / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="8376f-371">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span> | <span data-ttu-id="8376f-372">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8376f-372">testUser2@contoso.com</span></span>
<span data-ttu-id="8376f-373">mailboxDisplayName</span><span class="sxs-lookup"><span data-stu-id="8376f-373">mailboxDisplayName</span></span> | <span data-ttu-id="8376f-374">Disponible si entityType est *MailBox*.</span><span class="sxs-lookup"><span data-stu-id="8376f-374">Available if entityType is *MailBox*.</span></span> | <span data-ttu-id="8376f-375">test User2</span><span class="sxs-lookup"><span data-stu-id="8376f-375">test User2</span></span>
<span data-ttu-id="8376f-376">mailboxAddress</span><span class="sxs-lookup"><span data-stu-id="8376f-376">mailboxAddress</span></span> | <span data-ttu-id="8376f-377">Disponible si entityType est *User* / *MailBox* / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="8376f-377">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span> | <span data-ttu-id="8376f-378">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8376f-378">testUser2@contoso.com</span></span>
<span data-ttu-id="8376f-379">clusterBy</span><span class="sxs-lookup"><span data-stu-id="8376f-379">clusterBy</span></span> | <span data-ttu-id="8376f-380">Disponible si entityType est  *MailCluster*.</span><span class="sxs-lookup"><span data-stu-id="8376f-380">Available if entityType is  *MailCluster*.</span></span> | <span data-ttu-id="8376f-381">Objet ; P2SenderDomain; ContentType</span><span class="sxs-lookup"><span data-stu-id="8376f-381">Subject;P2SenderDomain;ContentType</span></span>
<span data-ttu-id="8376f-382">expéditeur</span><span class="sxs-lookup"><span data-stu-id="8376f-382">sender</span></span> | <span data-ttu-id="8376f-383">Disponible si entityType est *User* / *MailBox* / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="8376f-383">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span> | <span data-ttu-id="8376f-384">user.abc@mail.contoso.co.in</span><span class="sxs-lookup"><span data-stu-id="8376f-384">user.abc@mail.contoso.co.in</span></span>
<span data-ttu-id="8376f-385">destinataire</span><span class="sxs-lookup"><span data-stu-id="8376f-385">recipient</span></span> | <span data-ttu-id="8376f-386">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="8376f-386">Available if entityType is *MailMessage*.</span></span> | <span data-ttu-id="8376f-387">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8376f-387">testUser2@contoso.com</span></span>
<span data-ttu-id="8376f-388">subject</span><span class="sxs-lookup"><span data-stu-id="8376f-388">subject</span></span> | <span data-ttu-id="8376f-389">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="8376f-389">Available if entityType is *MailMessage*.</span></span> | <span data-ttu-id="8376f-390">\[Attention \] externe</span><span class="sxs-lookup"><span data-stu-id="8376f-390">\[EXTERNAL\] Attention</span></span>
<span data-ttu-id="8376f-391">deliveryAction</span><span class="sxs-lookup"><span data-stu-id="8376f-391">deliveryAction</span></span> | <span data-ttu-id="8376f-392">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="8376f-392">Available if entityType is *MailMessage*.</span></span> | <span data-ttu-id="8376f-393">Remis</span><span class="sxs-lookup"><span data-stu-id="8376f-393">Delivered</span></span>
<span data-ttu-id="8376f-394">securityGroupId</span><span class="sxs-lookup"><span data-stu-id="8376f-394">securityGroupId</span></span> | <span data-ttu-id="8376f-395">Disponible si entityType est  *SecurityGroup*.</span><span class="sxs-lookup"><span data-stu-id="8376f-395">Available if entityType is  *SecurityGroup*.</span></span> | <span data-ttu-id="8376f-396">301c47c8-e15f-4059-ab09-e2ba9ffd372b</span><span class="sxs-lookup"><span data-stu-id="8376f-396">301c47c8-e15f-4059-ab09-e2ba9ffd372b</span></span>
<span data-ttu-id="8376f-397">securityGroupName</span><span class="sxs-lookup"><span data-stu-id="8376f-397">securityGroupName</span></span> | <span data-ttu-id="8376f-398">Disponible si entityType est  *SecurityGroup*.</span><span class="sxs-lookup"><span data-stu-id="8376f-398">Available if entityType is  *SecurityGroup*.</span></span> | <span data-ttu-id="8376f-399">Opérateurs de configuration réseau</span><span class="sxs-lookup"><span data-stu-id="8376f-399">Network Configuration Operators</span></span>
<span data-ttu-id="8376f-400">registryHive</span><span class="sxs-lookup"><span data-stu-id="8376f-400">registryHive</span></span> | <span data-ttu-id="8376f-401">Disponible si entityType est *dans le Registre.*</span><span class="sxs-lookup"><span data-stu-id="8376f-401">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="8376f-402">ORDINATEUR LOCAL HKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="8376f-402">HKEY\_LOCAL\_MACHINE</span></span> |
<span data-ttu-id="8376f-403">registryKey</span><span class="sxs-lookup"><span data-stu-id="8376f-403">registryKey</span></span> | <span data-ttu-id="8376f-404">Disponible si entityType est *dans le Registre.*</span><span class="sxs-lookup"><span data-stu-id="8376f-404">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="8376f-405">SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon</span><span class="sxs-lookup"><span data-stu-id="8376f-405">SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon</span></span>
<span data-ttu-id="8376f-406">registryValueType</span><span class="sxs-lookup"><span data-stu-id="8376f-406">registryValueType</span></span> | <span data-ttu-id="8376f-407">Disponible si entityType est *dans le Registre.*</span><span class="sxs-lookup"><span data-stu-id="8376f-407">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="8376f-408">String</span><span class="sxs-lookup"><span data-stu-id="8376f-408">String</span></span>
<span data-ttu-id="8376f-409">registryValue</span><span class="sxs-lookup"><span data-stu-id="8376f-409">registryValue</span></span> | <span data-ttu-id="8376f-410">Disponible si entityType est *dans le Registre.*</span><span class="sxs-lookup"><span data-stu-id="8376f-410">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="8376f-411">31-00-00-00</span><span class="sxs-lookup"><span data-stu-id="8376f-411">31-00-00-00</span></span>
<span data-ttu-id="8376f-412">deviceId</span><span class="sxs-lookup"><span data-stu-id="8376f-412">deviceId</span></span> | <span data-ttu-id="8376f-413">ID, le caser, de l’appareil lié à l’entité.</span><span class="sxs-lookup"><span data-stu-id="8376f-413">The ID, if any, of the device related to the entity.</span></span> | <span data-ttu-id="8376f-414">986e5df8b73dacd43c8917d17e523e76b13c75cd</span><span class="sxs-lookup"><span data-stu-id="8376f-414">986e5df8b73dacd43c8917d17e523e76b13c75cd</span></span>

## <a name="example"></a><span data-ttu-id="8376f-415">Exemple</span><span class="sxs-lookup"><span data-stu-id="8376f-415">Example</span></span>

<span data-ttu-id="8376f-416">**Demande**</span><span class="sxs-lookup"><span data-stu-id="8376f-416">**Request**</span></span>

```HTTP
GET https://api.security.microsoft.com/api/incidents
```

<span data-ttu-id="8376f-417">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="8376f-417">**Response**</span></span>

```json
{
    "@odata.context": "https://api.security.microsoft.com/api/$metadata#Incidents",
    "value": [
            {
            "incidentId": 924565,
            "redirectIncidentId": null,
            "incidentName": "Ransomware activity",
            "createdTime": "2020-09-06T14:46:57.0733333Z",
            "lastUpdateTime": "2020-09-06T14:46:57.29Z",
            "assignedTo": null,
            "classification": "Unknown",
            "determination": "NotAvailable",
            "status": "Active",
            "severity": "Medium",
            "tags": [],
            "alerts": [
                {
                    "alertId": "caD70CFEE2-1F54-32DB-9988-3A868A1EBFAC",
                    "incidentId": 924565,
                    "serviceSource": "MicrosoftCloudAppSecurity",
                    "creationTime": "2020-09-06T14:46:55.7182276Z",
                    "lastUpdatedTime": "2020-09-06T14:46:57.2433333Z",
                    "resolvedTime": null,
                    "firstActivity": "2020-09-04T05:22:59Z",
                    "lastActivity": "2020-09-04T05:22:59Z",
                    "title": "Ransomware activity",
                    "description": "The user Test User2 (testUser2@contoso.com) manipulated 99 files with multiple extensions ending with the uncommon extension herunterladen. This is an unusual number of file manipulations and is indicative of a potential ransomware attack.",
                    "category": "Impact",
                    "status": "New",
                    "severity": "Medium",
                    "investigationId": null,
                    "investigationState": "UnsupportedAlertType",
                    "classification": null,
                    "determination": null,
                    "detectionSource": "MCAS",
                    "assignedTo": null,
                    "actorName": null,
                    "threatFamilyName": null,
                    "mitreTechniques": [],
                    "devices": [],
                    "entities": [
                        {
                            "entityType": "User",
                            "sha1": null,
                            "sha256": null,
                            "fileName": null,
                            "filePath": null,
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": null,
                            "url": null,
                            "accountName": "testUser2",
                            "domainName": "europe.corp.contoso",
                            "userSid": "S-1-5-21-1721254763-462695806-1538882281-4156657",
                            "aadUserId": "fc8f7484-f813-4db2-afab-bc1507913fb6",
                            "userPrincipalName": "testUser2@contoso.com",
                            "mailboxDisplayName": null,
                            "mailboxAddress": null,
                            "clusterBy": null,
                            "sender": null,
                            "recipient": null,
                            "subject": null,
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": null
                        },
                        {
                            "entityType": "Ip",
                            "sha1": null,
                            "sha256": null,
                            "fileName": null,
                            "filePath": null,
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": "62.216.203.204",
                            "url": null,
                            "accountName": null,
                            "domainName": null,
                            "userSid": null,
                            "aadUserId": null,
                            "userPrincipalName": null,
                            "mailboxDisplayName": null,
                            "mailboxAddress": null,
                            "clusterBy": null,
                            "sender": null,
                            "recipient": null,
                            "subject": null,
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": null
                        }
                    ]
                }
            ]
        },
        {
            "incidentId": 924521,
            "redirectIncidentId": null,
            "incidentName": "'Mimikatz' hacktool was detected on one endpoint",
            "createdTime": "2020-09-06T12:18:03.6266667Z",
            "lastUpdateTime": "2020-09-06T12:18:03.81Z",
            "assignedTo": null,
            "classification": "Unknown",
            "determination": "NotAvailable",
            "status": "Active",
            "severity": "Low",
            "tags": [],
            "alerts": [
                {
                    "alertId": "da637349914833441527_393341063",
                    "incidentId": 924521,
                    "serviceSource": "MicrosoftDefenderATP",
                    "creationTime": "2020-09-06T12:18:03.3285366Z",
                    "lastUpdatedTime": "2020-09-06T12:18:04.2566667Z",
                    "resolvedTime": null,
                    "firstActivity": "2020-09-06T12:15:07.7272048Z",
                    "lastActivity": "2020-09-06T12:15:07.7272048Z",
                    "title": "'Mimikatz' hacktool was detected",
                    "description": "Readily available tools, such as hacking programs, can be used by unauthorized individuals to spy on users. When used by attackers, these tools are often installed without authorization and used to compromise targeted machines.\n\nThese tools are often used to collect personal information from browser records, record key presses, access email and instant messages, record voice and video conversations, and take screenshots.\n\nThis detection might indicate that Windows Defender Antivirus has stopped the tool from being installed and used effectively. However, it is prudent to check the machine for the files and processes associated with the detected tool.",
                    "category": "Malware",
                    "status": "New",
                    "severity": "Low",
                    "investigationId": null,
                    "investigationState": "UnsupportedOs",
                    "classification": null,
                    "determination": null,
                    "detectionSource": "WindowsDefenderAv",
                    "assignedTo": null,
                    "actorName": null,
                    "threatFamilyName": "Mimikatz",
                    "mitreTechniques": [],
                    "devices": [
                        {
                            "mdatpDeviceId": "24c222b0b60fe148eeece49ac83910cc6a7ef491",
                            "aadDeviceId": null,
                            "deviceDnsName": "user5cx.middleeast.corp.contoso.com",
                            "osPlatform": "WindowsServer2016",
                            "version": "1607",
                            "osProcessor": "x64",
                            "osBuild": 14393,
                            "healthStatus": "Active",
                            "riskScore": "High",
                            "rbacGroupName": "WDATP-Ring0",
                            "rbacGroupId": 9,
                            "firstSeen": "2020-02-06T14:16:01.9330135Z"
                        }
                    ],
                    "entities": [
                        {
                            "entityType": "File",
                            "sha1": "5de839186691aa96ee2ca6d74f0a38fb8d1bd6dd",
                            "sha256": null,
                            "fileName": "Detector.UnitTests.dll",
                            "filePath": "C:\\Agent\\_work\\_temp\\Deploy_SYSTEM 2020-09-06 12_14_54\\Out",
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": null,
                            "url": null,
                            "accountName": null,
                            "domainName": null,
                            "userSid": null,
                            "aadUserId": null,
                            "userPrincipalName": null,
                            "mailboxDisplayName": null,
                            "mailboxAddress": null,
                            "clusterBy": null,
                            "sender": null,
                            "recipient": null,
                            "subject": null,
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": "24c222b0b60fe148eeece49ac83910cc6a7ef491"
                        }
                    ]
                }
            ]
        },
        {
            "incidentId": 924518,
            "redirectIncidentId": null,
            "incidentName": "Email reported by user as malware or phish",
            "createdTime": "2020-09-06T12:07:55.1366667Z",
            "lastUpdateTime": "2020-09-06T12:07:55.32Z",
            "assignedTo": null,
            "classification": "Unknown",
            "determination": "NotAvailable",
            "status": "Active",
            "severity": "Informational",
            "tags": [],
            "alerts": [
                {
                    "alertId": "faf8edc936-85f8-a603-b800-08d8525cf099",
                    "incidentId": 924518,
                    "serviceSource": "OfficeATP",
                    "creationTime": "2020-09-06T12:07:54.3716642Z",
                    "lastUpdatedTime": "2020-09-06T12:37:40.88Z",
                    "resolvedTime": null,
                    "firstActivity": "2020-09-06T12:04:00Z",
                    "lastActivity": "2020-09-06T12:04:00Z",
                    "title": "Email reported by user as malware or phish",
                    "description": "This alert is triggered when any email message is reported as malware or phish by users -V1.0.0.2",
                    "category": "InitialAccess",
                    "status": "InProgress",
                    "severity": "Informational",
                    "investigationId": null,
                    "investigationState": "Queued",
                    "classification": null,
                    "determination": null,
                    "detectionSource": "OfficeATP",
                    "assignedTo": "Automation",
                    "actorName": null,
                    "threatFamilyName": null,
                    "mitreTechniques": [],
                    "devices": [],
                    "entities": [
                        {
                            "entityType": "MailBox",
                            "sha1": null,
                            "sha256": null,
                            "fileName": null,
                            "filePath": null,
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": null,
                            "url": null,
                            "accountName": null,
                            "domainName": null,
                            "userSid": null,
                            "aadUserId": null,
                            "userPrincipalName": "testUser3@contoso.com",
                            "mailboxDisplayName": "test User3",
                            "mailboxAddress": "testUser3@contoso.com",
                            "clusterBy": null,
                            "sender": null,
                            "recipient": null,
                            "subject": null,
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": null
                        },
                        {
                            "entityType": "MailBox",
                            "sha1": null,
                            "sha256": null,
                            "fileName": null,
                            "filePath": null,
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": null,
                            "url": null,
                            "accountName": null,
                            "domainName": null,
                            "userSid": null,
                            "aadUserId": null,
                            "userPrincipalName": "testUser4@contoso.com",
                            "mailboxDisplayName": "test User4",
                            "mailboxAddress": "test.User4@contoso.com",
                            "clusterBy": null,
                            "sender": null,
                            "recipient": null,
                            "subject": null,
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": null
                        },
                        {
                            "entityType": "MailMessage",
                            "sha1": null,
                            "sha256": null,
                            "fileName": null,
                            "filePath": null,
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": null,
                            "url": null,
                            "accountName": null,
                            "domainName": null,
                            "userSid": null,
                            "aadUserId": null,
                            "userPrincipalName": "test.User4@contoso.com",
                            "mailboxDisplayName": null,
                            "mailboxAddress": null,
                            "clusterBy": null,
                            "sender": "user.abc@mail.contoso.co.in",
                            "recipient": "test.User4@contoso.com",
                            "subject": "[EXTERNAL] Attention",
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": null
                        },
                        {
                            "entityType": "MailCluster",
                            "sha1": null,
                            "sha256": null,
                            "fileName": null,
                            "filePath": null,
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": null,
                            "url": null,
                            "accountName": null,
                            "domainName": null,
                            "userSid": null,
                            "aadUserId": null,
                            "userPrincipalName": null,
                            "mailboxDisplayName": null,
                            "mailboxAddress": null,
                            "clusterBy": "Subject;P2SenderDomain;ContentType",
                            "sender": null,
                            "recipient": null,
                            "subject": null,
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": null
                        },
                        {
                            "entityType": "MailCluster",
                            "sha1": null,
                            "sha256": null,
                            "fileName": null,
                            "filePath": null,
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": null,
                            "url": null,
                            "accountName": null,
                            "domainName": null,
                            "userSid": null,
                            "aadUserId": null,
                            "userPrincipalName": null,
                            "mailboxDisplayName": null,
                            "mailboxAddress": null,
                            "clusterBy": "Subject;SenderIp;ContentType",
                            "sender": null,
                            "recipient": null,
                            "subject": null,
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": null
                        },
                        {
                            "entityType": "MailCluster",
                            "sha1": null,
                            "sha256": null,
                            "fileName": null,
                            "filePath": null,
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": null,
                            "url": null,
                            "accountName": null,
                            "domainName": null,
                            "userSid": null,
                            "aadUserId": null,
                            "userPrincipalName": null,
                            "mailboxDisplayName": null,
                            "mailboxAddress": null,
                            "clusterBy": "BodyFingerprintBin1;P2SenderDomain;ContentType",
                            "sender": null,
                            "recipient": null,
                            "subject": null,
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": null
                        },
                        {
                            "entityType": "MailCluster",
                            "sha1": null,
                            "sha256": null,
                            "fileName": null,
                            "filePath": null,
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": null,
                            "url": null,
                            "accountName": null,
                            "domainName": null,
                            "userSid": null,
                            "aadUserId": null,
                            "userPrincipalName": null,
                            "mailboxDisplayName": null,
                            "mailboxAddress": null,
                            "clusterBy": "BodyFingerprintBin1;SenderIp;ContentType",
                            "sender": null,
                            "recipient": null,
                            "subject": null,
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": null
                        },
                        {
                            "entityType": "Ip",
                            "sha1": null,
                            "sha256": null,
                            "fileName": null,
                            "filePath": null,
                            "processId": null,
                            "processCommandLine": null,
                            "processCreationTime": null,
                            "parentProcessId": null,
                            "parentProcessCreationTime": null,
                            "ipAddress": "49.50.81.121",
                            "url": null,
                            "accountName": null,
                            "domainName": null,
                            "userSid": null,
                            "aadUserId": null,
                            "userPrincipalName": null,
                            "mailboxDisplayName": null,
                            "mailboxAddress": null,
                            "clusterBy": null,
                            "sender": null,
                            "recipient": null,
                            "subject": null,
                            "deliveryAction": null,
                            "securityGroupId": null,
                            "securityGroupName": null,
                            "registryHive": null,
                            "registryKey": null,
                            "registryValueType": null,
                            "registryValue": null,
                            "deviceId": null
                        }
                    ]
                }
            ]
        },
        ...
    ]
}
```

## <a name="related-articles"></a><span data-ttu-id="8376f-418">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="8376f-418">Related articles</span></span>

- [<span data-ttu-id="8376f-419">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8376f-419">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="8376f-420">En savoir plus sur les limites d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="8376f-420">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="8376f-421">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8376f-421">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="8376f-422">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="8376f-422">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="8376f-423">API d’incident</span><span class="sxs-lookup"><span data-stu-id="8376f-423">Incident APIs</span></span>](api-incident.md)
- [<span data-ttu-id="8376f-424">API de mise à jour de l’incident</span><span class="sxs-lookup"><span data-stu-id="8376f-424">Update incident API</span></span>](api-update-incidents.md)
