---
title: API de liste des incidents dans Microsoft 365 Defender
description: Découvrez comment répertorier l’API des incidents dans Microsoft 365 Defender
keywords: liste, incident, incidents, API
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
ms.openlocfilehash: 13508d3ad9d61797517ccb55a27152883947843a
ms.sourcegitcommit: d6b1da2e12d55f69e4353289e90f5ae2f60066d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "49719427"
---
# <a name="list-incidents-api-in-microsoft-365-defender"></a><span data-ttu-id="d54cd-104">API de liste des incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d54cd-104">List incidents API in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="d54cd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d54cd-105">**Applies to:**</span></span>

- <span data-ttu-id="d54cd-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d54cd-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d54cd-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="d54cd-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d54cd-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="d54cd-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


## <a name="api-description"></a><span data-ttu-id="d54cd-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="d54cd-109">API description</span></span>

<span data-ttu-id="d54cd-110">L’API liste des incidents vous permet de trier les incidents afin de créer une réponse Cybersecurity informée.</span><span class="sxs-lookup"><span data-stu-id="d54cd-110">The list incidents API allows you to sort through incidents to create an informed cybersecurity response.</span></span> <span data-ttu-id="d54cd-111">Il expose une collection d’incidents marqués sur votre réseau, dans la plage de temps que vous avez spécifiée dans votre stratégie de rétention de l’environnement.</span><span class="sxs-lookup"><span data-stu-id="d54cd-111">It exposes a collection of incidents that were flagged in your network, within the time range you specified in your environment retention policy.</span></span> <span data-ttu-id="d54cd-112">Les incidents les plus récents sont affichés en haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="d54cd-112">The most recent incidents are displayed at the top of the list.</span></span> <span data-ttu-id="d54cd-113">Chaque incident contient un tableau des alertes associées et de leurs entités associées.</span><span class="sxs-lookup"><span data-stu-id="d54cd-113">Each incident contains an array of related alerts, and their related entities.</span></span>

<span data-ttu-id="d54cd-114">L’API prend en charge les opérateurs **OData** suivants :</span><span class="sxs-lookup"><span data-stu-id="d54cd-114">The API supports the following **OData** operators:</span></span>

- <span data-ttu-id="d54cd-115">`$filter`sur les `lastUpdateTime` Propriétés,, `createdTime` `status` et `assignedTo`</span><span class="sxs-lookup"><span data-stu-id="d54cd-115">`$filter` on the `lastUpdateTime`, `createdTime`, `status`, and `assignedTo` properties</span></span>
- <span data-ttu-id="d54cd-116">`$top`, avec une valeur maximale de **100**</span><span class="sxs-lookup"><span data-stu-id="d54cd-116">`$top`, with a maximum value of **100**</span></span>
- `$skip`

## <a name="limitations"></a><span data-ttu-id="d54cd-117">Limites</span><span class="sxs-lookup"><span data-stu-id="d54cd-117">Limitations</span></span>

1. <span data-ttu-id="d54cd-118">La taille de page maximale est de **100 incidents**.</span><span class="sxs-lookup"><span data-stu-id="d54cd-118">Maximum page size is **100 incidents**.</span></span>
2. <span data-ttu-id="d54cd-119">Le taux maximal de demandes est de **50 appels par minute** et **1500 appels par heure**.</span><span class="sxs-lookup"><span data-stu-id="d54cd-119">Maximum rate of requests is **50 calls per minute** and **1500 calls per hour**.</span></span>

## <a name="permissions"></a><span data-ttu-id="d54cd-120">Autorisations</span><span class="sxs-lookup"><span data-stu-id="d54cd-120">Permissions</span></span>

<span data-ttu-id="d54cd-121">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="d54cd-121">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="d54cd-122">Pour plus d’informations, notamment sur le choix des autorisations, consultez la rubrique [Access Microsoft 365 Defender API](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="d54cd-122">To learn more, including how to choose permissions, see [Access Microsoft 365 Defender APIs](api-access.md)</span></span>

<span data-ttu-id="d54cd-123">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="d54cd-123">Permission type</span></span> | <span data-ttu-id="d54cd-124">Autorisation</span><span class="sxs-lookup"><span data-stu-id="d54cd-124">Permission</span></span> | <span data-ttu-id="d54cd-125">Nom d’affichage des autorisations</span><span class="sxs-lookup"><span data-stu-id="d54cd-125">Permission display name</span></span>
-|-|-
<span data-ttu-id="d54cd-126">Application</span><span class="sxs-lookup"><span data-stu-id="d54cd-126">Application</span></span> | <span data-ttu-id="d54cd-127">Incident. Read. All</span><span class="sxs-lookup"><span data-stu-id="d54cd-127">Incident.Read.All</span></span> | <span data-ttu-id="d54cd-128">Lire tous les incidents</span><span class="sxs-lookup"><span data-stu-id="d54cd-128">Read all incidents</span></span>
<span data-ttu-id="d54cd-129">Application</span><span class="sxs-lookup"><span data-stu-id="d54cd-129">Application</span></span> | <span data-ttu-id="d54cd-130">Incident. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="d54cd-130">Incident.ReadWrite.All</span></span> | <span data-ttu-id="d54cd-131">Lire et écrire tous les incidents</span><span class="sxs-lookup"><span data-stu-id="d54cd-131">Read and write all incidents</span></span>
<span data-ttu-id="d54cd-132">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="d54cd-132">Delegated (work or school account)</span></span> | <span data-ttu-id="d54cd-133">Incident. Read</span><span class="sxs-lookup"><span data-stu-id="d54cd-133">Incident.Read</span></span> | <span data-ttu-id="d54cd-134">Incidents de lecture</span><span class="sxs-lookup"><span data-stu-id="d54cd-134">Read incidents</span></span>
<span data-ttu-id="d54cd-135">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="d54cd-135">Delegated (work or school account)</span></span> | <span data-ttu-id="d54cd-136">Incident. ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d54cd-136">Incident.ReadWrite</span></span> | <span data-ttu-id="d54cd-137">Incidents de lecture et d’écriture</span><span class="sxs-lookup"><span data-stu-id="d54cd-137">Read and write incidents</span></span>

> [!Note]
> <span data-ttu-id="d54cd-138">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="d54cd-138">When obtaining a token using user credentials:</span></span>
>
> - <span data-ttu-id="d54cd-139">L’utilisateur doit disposer de l’autorisation Afficher pour les incidents dans le portail.</span><span class="sxs-lookup"><span data-stu-id="d54cd-139">The user needs to have view permission for incidents in the portal.</span></span>
> - <span data-ttu-id="d54cd-140">La réponse inclut uniquement les incidents auxquels l’utilisateur est exposé.</span><span class="sxs-lookup"><span data-stu-id="d54cd-140">The response will only include incidents that the user is exposed to.</span></span>

## <a name="http-request"></a><span data-ttu-id="d54cd-141">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="d54cd-141">HTTP request</span></span>

```HTTP
GET /api/incidents
```

## <a name="request-headers"></a><span data-ttu-id="d54cd-142">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="d54cd-142">Request headers</span></span>

<span data-ttu-id="d54cd-143">Nom</span><span class="sxs-lookup"><span data-stu-id="d54cd-143">Name</span></span> | <span data-ttu-id="d54cd-144">Type</span><span class="sxs-lookup"><span data-stu-id="d54cd-144">Type</span></span> | <span data-ttu-id="d54cd-145">Description</span><span class="sxs-lookup"><span data-stu-id="d54cd-145">Description</span></span>
-|-|-
<span data-ttu-id="d54cd-146">Autorisation</span><span class="sxs-lookup"><span data-stu-id="d54cd-146">Authorization</span></span> | <span data-ttu-id="d54cd-147">String</span><span class="sxs-lookup"><span data-stu-id="d54cd-147">String</span></span> | <span data-ttu-id="d54cd-148">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="d54cd-148">Bearer {token}.</span></span> <span data-ttu-id="d54cd-149">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d54cd-149">**Required**</span></span>


## <a name="request-body"></a><span data-ttu-id="d54cd-150">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="d54cd-150">Request body</span></span>

<span data-ttu-id="d54cd-151">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d54cd-151">None.</span></span>

## <a name="response"></a><span data-ttu-id="d54cd-152">Réponse</span><span class="sxs-lookup"><span data-stu-id="d54cd-152">Response</span></span>

<span data-ttu-id="d54cd-153">Si elle réussit, cette méthode renvoie `200 OK` et une liste d' [incidents](api-incident.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="d54cd-153">If successful, this method returns `200 OK`, and a list of [incidents](api-incident.md) in the response body.</span></span>

## <a name="schema-mapping"></a><span data-ttu-id="d54cd-154">Mappage de schéma</span><span class="sxs-lookup"><span data-stu-id="d54cd-154">Schema mapping</span></span>

### <a name="incident-metadata"></a><span data-ttu-id="d54cd-155">Métadonnées d’incident</span><span class="sxs-lookup"><span data-stu-id="d54cd-155">Incident metadata</span></span>

<span data-ttu-id="d54cd-156">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="d54cd-156">Field name</span></span> | <span data-ttu-id="d54cd-157">Description</span><span class="sxs-lookup"><span data-stu-id="d54cd-157">Description</span></span> | <span data-ttu-id="d54cd-158">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="d54cd-158">Example value</span></span>
-|-|-
<span data-ttu-id="d54cd-159">incidentId</span><span class="sxs-lookup"><span data-stu-id="d54cd-159">incidentId</span></span> | <span data-ttu-id="d54cd-160">Identificateur unique qui représente l’incident.</span><span class="sxs-lookup"><span data-stu-id="d54cd-160">Unique identifier to represent the incident</span></span> | <span data-ttu-id="d54cd-161">924565</span><span class="sxs-lookup"><span data-stu-id="d54cd-161">924565</span></span>
<span data-ttu-id="d54cd-162">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="d54cd-162">redirectIncidentId</span></span> | <span data-ttu-id="d54cd-163">Renseigné uniquement si un incident est regroupé avec un autre incident, dans le cadre de la logique de traitement de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d54cd-163">Only populated in case an incident is being grouped together with another incident, as part of the incident processing logic.</span></span> | <span data-ttu-id="d54cd-164">924569</span><span class="sxs-lookup"><span data-stu-id="d54cd-164">924569</span></span>
<span data-ttu-id="d54cd-165">incidentName</span><span class="sxs-lookup"><span data-stu-id="d54cd-165">incidentName</span></span> | <span data-ttu-id="d54cd-166">Valeur de chaîne disponible pour chaque incident.</span><span class="sxs-lookup"><span data-stu-id="d54cd-166">String value available for every incident.</span></span> | <span data-ttu-id="d54cd-167">Activité ransomware</span><span class="sxs-lookup"><span data-stu-id="d54cd-167">Ransomware activity</span></span>
<span data-ttu-id="d54cd-168">createdTime</span><span class="sxs-lookup"><span data-stu-id="d54cd-168">createdTime</span></span> | <span data-ttu-id="d54cd-169">Heure de la première création de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d54cd-169">Time when incident was first created.</span></span> | <span data-ttu-id="d54cd-170">2020-09-06T14:46:57.0733333 Z</span><span class="sxs-lookup"><span data-stu-id="d54cd-170">2020-09-06T14:46:57.0733333Z</span></span>
<span data-ttu-id="d54cd-171">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="d54cd-171">lastUpdateTime</span></span> | <span data-ttu-id="d54cd-172">Heure de la dernière mise à jour de l’incident sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="d54cd-172">Time when the incident was last updated on the backend.</span></span><br /><br /> <span data-ttu-id="d54cd-173">Ce champ peut être utilisé lorsque vous définissez le paramètre de demande pour la plage de temps pendant laquelle les incidents sont récupérés.</span><span class="sxs-lookup"><span data-stu-id="d54cd-173">This field can be used when you're setting the request parameter for the range of time that incidents are retrieved.</span></span> | <span data-ttu-id="d54cd-174">2020-09-06T14:46:57.29 Z</span><span class="sxs-lookup"><span data-stu-id="d54cd-174">2020-09-06T14:46:57.29Z</span></span>
<span data-ttu-id="d54cd-175">assignedTo</span><span class="sxs-lookup"><span data-stu-id="d54cd-175">assignedTo</span></span> | <span data-ttu-id="d54cd-176">Propriétaire de l’incident ou *valeur null* si aucun propriétaire n’est affecté.</span><span class="sxs-lookup"><span data-stu-id="d54cd-176">Owner of the incident, or *null* if no owner is assigned.</span></span> | <span data-ttu-id="d54cd-177">secop2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d54cd-177">secop2@contoso.com</span></span>
<span data-ttu-id="d54cd-178">classification</span><span class="sxs-lookup"><span data-stu-id="d54cd-178">classification</span></span> | <span data-ttu-id="d54cd-179">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d54cd-179">The specification for the incident.</span></span> <span data-ttu-id="d54cd-180">Les valeurs de propriété sont les suivantes : *Unknown*, *FalsePositive*, *TruePositive*</span><span class="sxs-lookup"><span data-stu-id="d54cd-180">The property values are: *Unknown*, *FalsePositive*, *TruePositive*</span></span> | <span data-ttu-id="d54cd-181">Inconnu</span><span class="sxs-lookup"><span data-stu-id="d54cd-181">Unknown</span></span>
<span data-ttu-id="d54cd-182">indications</span><span class="sxs-lookup"><span data-stu-id="d54cd-182">determination</span></span> | <span data-ttu-id="d54cd-183">Indique la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d54cd-183">Specifies the determination of the incident.</span></span> <span data-ttu-id="d54cd-184">Les valeurs de propriété sont les suivantes : *NotAvailable*, *apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *other*</span><span class="sxs-lookup"><span data-stu-id="d54cd-184">The property values are: *NotAvailable*, *Apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *Other*</span></span> | <span data-ttu-id="d54cd-185">NotAvailable</span><span class="sxs-lookup"><span data-stu-id="d54cd-185">NotAvailable</span></span>
<span data-ttu-id="d54cd-186">status</span><span class="sxs-lookup"><span data-stu-id="d54cd-186">status</span></span> | <span data-ttu-id="d54cd-187">Catégoriser les incidents ( *actif* ou *résolu*).</span><span class="sxs-lookup"><span data-stu-id="d54cd-187">Categorize incidents (as *Active*, or *Resolved*).</span></span> <span data-ttu-id="d54cd-188">Elle vous permet d’organiser et de gérer votre réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="d54cd-188">It can help you organize and manage your response to incidents.</span></span> | <span data-ttu-id="d54cd-189">Actif</span><span class="sxs-lookup"><span data-stu-id="d54cd-189">Active</span></span>
<span data-ttu-id="d54cd-190">Sévérité </span><span class="sxs-lookup"><span data-stu-id="d54cd-190">severity</span></span> | <span data-ttu-id="d54cd-191">Indique l’impact possible sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="d54cd-191">Indicates the possible impact on assets.</span></span> <span data-ttu-id="d54cd-192">Plus la gravité est élevée, plus l’impact est important.</span><span class="sxs-lookup"><span data-stu-id="d54cd-192">The higher the severity the bigger the impact.</span></span> <span data-ttu-id="d54cd-193">En règle générale, les éléments de gravité plus élevés nécessitent une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="d54cd-193">Typically higher severity items require the most immediate attention.</span></span><br /><br /><span data-ttu-id="d54cd-194">L’une des valeurs suivantes : *informatif*, *Low*, \* medium et *High*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-194">One of the following values: *Informational*, *Low*, \*Medium, and *High*.</span></span> | <span data-ttu-id="d54cd-195">Moyen</span><span class="sxs-lookup"><span data-stu-id="d54cd-195">Medium</span></span>
<span data-ttu-id="d54cd-196">étiquettes</span><span class="sxs-lookup"><span data-stu-id="d54cd-196">tags</span></span> | <span data-ttu-id="d54cd-197">Tableau de balises personnalisées associées à un incident, par exemple pour marquer un groupe d’incidents avec une caractéristique commune.</span><span class="sxs-lookup"><span data-stu-id="d54cd-197">Array of custom tags associated with an incident, for example to flag a group of incidents with a common characteristic.</span></span> | \[\]
<span data-ttu-id="d54cd-198">alerts</span><span class="sxs-lookup"><span data-stu-id="d54cd-198">alerts</span></span> | <span data-ttu-id="d54cd-199">Tableau contenant toutes les alertes liées à l’incident, ainsi que d’autres informations, telles que la gravité, les entités impliquées dans l’alerte et la source des alertes.</span><span class="sxs-lookup"><span data-stu-id="d54cd-199">Array containing all of the alerts related to the incident, plus other information, such as severity, entities that were involved in the alert, and the source of the alerts.</span></span> | <span data-ttu-id="d54cd-200">\[\] (voir détails dans les champs d’alerte ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="d54cd-200">\[\] (see details on alert fields below)</span></span>

### <a name="alerts-metadata"></a><span data-ttu-id="d54cd-201">Métadonnées d’alertes</span><span class="sxs-lookup"><span data-stu-id="d54cd-201">Alerts metadata</span></span>

<span data-ttu-id="d54cd-202">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="d54cd-202">Field name</span></span> | <span data-ttu-id="d54cd-203">Description</span><span class="sxs-lookup"><span data-stu-id="d54cd-203">Description</span></span> | <span data-ttu-id="d54cd-204">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="d54cd-204">Example value</span></span>
-|-|-
<span data-ttu-id="d54cd-205">IDAlerte</span><span class="sxs-lookup"><span data-stu-id="d54cd-205">alertId</span></span> | <span data-ttu-id="d54cd-206">Identificateur unique qui représente l’alerte.</span><span class="sxs-lookup"><span data-stu-id="d54cd-206">Unique identifier to represent the alert</span></span> | <span data-ttu-id="d54cd-207">caD70CFEE2-1F54-32DB-9988-3A868A1EBFAC</span><span class="sxs-lookup"><span data-stu-id="d54cd-207">caD70CFEE2-1F54-32DB-9988-3A868A1EBFAC</span></span>
<span data-ttu-id="d54cd-208">incidentId</span><span class="sxs-lookup"><span data-stu-id="d54cd-208">incidentId</span></span> | <span data-ttu-id="d54cd-209">Identificateur unique représentant l’incident auquel cette alerte est associée.</span><span class="sxs-lookup"><span data-stu-id="d54cd-209">Unique identifier to represent the incident this alert is associated with</span></span> | <span data-ttu-id="d54cd-210">924565</span><span class="sxs-lookup"><span data-stu-id="d54cd-210">924565</span></span>
<span data-ttu-id="d54cd-211">serviceSource</span><span class="sxs-lookup"><span data-stu-id="d54cd-211">serviceSource</span></span> | <span data-ttu-id="d54cd-212">Service d’origine de l’alerte, comme Microsoft Defender pour le point de terminaison, sécurité de l’application Cloud Microsoft, Microsoft Defender pour l’identité ou Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="d54cd-212">Service that the alert originates from, such as Microsoft Defender for Endpoint, Microsoft Cloud App Security, Microsoft Defender for Identity, or Microsoft Defender for Office 365.</span></span> | <span data-ttu-id="d54cd-213">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="d54cd-213">MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="d54cd-214">creationTime</span><span class="sxs-lookup"><span data-stu-id="d54cd-214">creationTime</span></span> | <span data-ttu-id="d54cd-215">Heure à laquelle l’alerte a été créée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="d54cd-215">Time when alert was first created.</span></span> | <span data-ttu-id="d54cd-216">2020-09-06T14:46:55.7182276 Z</span><span class="sxs-lookup"><span data-stu-id="d54cd-216">2020-09-06T14:46:55.7182276Z</span></span>
<span data-ttu-id="d54cd-217">lastUpdatedTime</span><span class="sxs-lookup"><span data-stu-id="d54cd-217">lastUpdatedTime</span></span> | <span data-ttu-id="d54cd-218">Heure de la dernière mise à jour de l’alerte sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="d54cd-218">Time when alert was last updated at the backend.</span></span> | <span data-ttu-id="d54cd-219">2020-09-06T14:46:57.2433333 Z</span><span class="sxs-lookup"><span data-stu-id="d54cd-219">2020-09-06T14:46:57.2433333Z</span></span>
<span data-ttu-id="d54cd-220">resolvedTime</span><span class="sxs-lookup"><span data-stu-id="d54cd-220">resolvedTime</span></span> | <span data-ttu-id="d54cd-221">Heure de la résolution de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="d54cd-221">Time when alert was resolved.</span></span> | <span data-ttu-id="d54cd-222">2020-09-10T05:22:59Z</span><span class="sxs-lookup"><span data-stu-id="d54cd-222">2020-09-10T05:22:59Z</span></span>
<span data-ttu-id="d54cd-223">firstActivity</span><span class="sxs-lookup"><span data-stu-id="d54cd-223">firstActivity</span></span> | <span data-ttu-id="d54cd-224">Heure à laquelle l’alerte a signalé pour la première fois que l’activité a été mise à jour sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="d54cd-224">Time when alert first reported that activity was updated at the backend.</span></span>| <span data-ttu-id="d54cd-225">2020-09-04T05:22:59Z</span><span class="sxs-lookup"><span data-stu-id="d54cd-225">2020-09-04T05:22:59Z</span></span>
<span data-ttu-id="d54cd-226">title</span><span class="sxs-lookup"><span data-stu-id="d54cd-226">title</span></span> | <span data-ttu-id="d54cd-227">Courte valeur de chaîne d’identification disponible pour chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="d54cd-227">Brief identifying string value available for each alert.</span></span> | <span data-ttu-id="d54cd-228">Activité ransomware</span><span class="sxs-lookup"><span data-stu-id="d54cd-228">Ransomware activity</span></span>
<span data-ttu-id="d54cd-229">description</span><span class="sxs-lookup"><span data-stu-id="d54cd-229">description</span></span> | <span data-ttu-id="d54cd-230">Valeur de chaîne décrivant chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="d54cd-230">String value describing each alert.</span></span> | <span data-ttu-id="d54cd-231">Le test de l’utilisateur utilisateur2 (testUser2@contoso.com) a manipulé 99 fichiers avec plusieurs extensions se terminant par l’extension *herunterladen*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-231">The user Test User2 (testUser2@contoso.com) manipulated 99 files with multiple extensions ending with the uncommon extension *herunterladen*.</span></span> <span data-ttu-id="d54cd-232">Il s’agit d’un nombre inhabituel de manipulations de fichiers et indique une attaque par ransomware potentielle.</span><span class="sxs-lookup"><span data-stu-id="d54cd-232">This is an unusual number of file manipulations and is indicative of a potential ransomware attack.</span></span>
<span data-ttu-id="d54cd-233">category</span><span class="sxs-lookup"><span data-stu-id="d54cd-233">category</span></span> | <span data-ttu-id="d54cd-234">Vue visuelle et numérique de la progression de l’attaque le long de la chaîne de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d54cd-234">Visual and numeric view of how far the attack has progressed along the kill chain.</span></span> <span data-ttu-id="d54cd-235">Aligné sur l' [infrastructure Mitre ATT&CK™](https://attack.mitre.org/).</span><span class="sxs-lookup"><span data-stu-id="d54cd-235">Aligned to the [MITRE ATT&CK™ framework](https://attack.mitre.org/).</span></span> | <span data-ttu-id="d54cd-236">Impact</span><span class="sxs-lookup"><span data-stu-id="d54cd-236">Impact</span></span>
<span data-ttu-id="d54cd-237">status</span><span class="sxs-lookup"><span data-stu-id="d54cd-237">status</span></span> | <span data-ttu-id="d54cd-238">Catégoriser les alertes (en tant que *nouvelles*, *actives* ou *résolues*).</span><span class="sxs-lookup"><span data-stu-id="d54cd-238">Categorize alerts (as *New*, *Active*, or *Resolved*).</span></span> <span data-ttu-id="d54cd-239">Elle vous permet d’organiser et de gérer votre réponse aux alertes.</span><span class="sxs-lookup"><span data-stu-id="d54cd-239">It can help you organize and manage your response to alerts.</span></span> | <span data-ttu-id="d54cd-240">Nouveau</span><span class="sxs-lookup"><span data-stu-id="d54cd-240">New</span></span>
<span data-ttu-id="d54cd-241">Sévérité </span><span class="sxs-lookup"><span data-stu-id="d54cd-241">severity</span></span> | <span data-ttu-id="d54cd-242">Indique l’impact possible sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="d54cd-242">Indicates the possible impact on assets.</span></span> <span data-ttu-id="d54cd-243">Plus la gravité est élevée, plus l’impact est important.</span><span class="sxs-lookup"><span data-stu-id="d54cd-243">The higher the severity the bigger the impact.</span></span> <span data-ttu-id="d54cd-244">En règle générale, les éléments de gravité plus élevés nécessitent une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="d54cd-244">Typically higher severity items require the most immediate attention.</span></span><br><span data-ttu-id="d54cd-245">L’une des valeurs suivantes : *informatif*, *Low*, \* medium et *High*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-245">One of the following values: *Informational*, *Low*, \*Medium, and *High*.</span></span> | <span data-ttu-id="d54cd-246">Moyen</span><span class="sxs-lookup"><span data-stu-id="d54cd-246">Medium</span></span>
<span data-ttu-id="d54cd-247">investigationId</span><span class="sxs-lookup"><span data-stu-id="d54cd-247">investigationId</span></span> | <span data-ttu-id="d54cd-248">ID d’enquête automatisé déclenché par cette alerte.</span><span class="sxs-lookup"><span data-stu-id="d54cd-248">The automated investigation ID triggered by this alert.</span></span> | <span data-ttu-id="d54cd-249">1234</span><span class="sxs-lookup"><span data-stu-id="d54cd-249">1234</span></span>
<span data-ttu-id="d54cd-250">investigationState</span><span class="sxs-lookup"><span data-stu-id="d54cd-250">investigationState</span></span> | <span data-ttu-id="d54cd-251">Informations sur l’état actuel de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="d54cd-251">Information on the investigation's current status.</span></span> <span data-ttu-id="d54cd-252">L’une des valeurs suivantes : *inconnu*, *terminé*, *SuccessfullyRemediated*, *bénigne*, *échec*, *PartiallyRemediated*, *en cours d’exécution*, *PendingApproval*, *PendingResource*, *PartiallyInvestigated*, *TerminatedByUser*, *TerminatedBySystem*, *mis en file d’attente*, *InnerFailure*, *PreexistingAlert*, non *pris en charge*, *UnsupportedAlertType*, *SuppressedAlert.*</span><span class="sxs-lookup"><span data-stu-id="d54cd-252">One of the following values: *Unknown*, *Terminated*, *SuccessfullyRemediated*, *Benign*, *Failed*, *PartiallyRemediated*, *Running*, *PendingApproval*, *PendingResource*, *PartiallyInvestigated*, *TerminatedByUser*, *TerminatedBySystem*, *Queued*, *InnerFailure*, *PreexistingAlert*, *UnsupportedOs*, *UnsupportedAlertType*, *SuppressedAlert*.</span></span> | <span data-ttu-id="d54cd-253">UnsupportedAlertType</span><span class="sxs-lookup"><span data-stu-id="d54cd-253">UnsupportedAlertType</span></span>
<span data-ttu-id="d54cd-254">classification</span><span class="sxs-lookup"><span data-stu-id="d54cd-254">classification</span></span> | <span data-ttu-id="d54cd-255">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d54cd-255">The specification for the incident.</span></span> <span data-ttu-id="d54cd-256">Les valeurs de propriété sont les suivantes : *Unknown*, *FalsePositive*, *TruePositive* ou *null*</span><span class="sxs-lookup"><span data-stu-id="d54cd-256">The property values are: *Unknown*, *FalsePositive*, *TruePositive*, or *null*</span></span> | <span data-ttu-id="d54cd-257">Inconnu</span><span class="sxs-lookup"><span data-stu-id="d54cd-257">Unknown</span></span>
<span data-ttu-id="d54cd-258">indications</span><span class="sxs-lookup"><span data-stu-id="d54cd-258">determination</span></span> | <span data-ttu-id="d54cd-259">Indique la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="d54cd-259">Specifies the determination of the incident.</span></span> <span data-ttu-id="d54cd-260">Les valeurs de propriété sont les suivantes : *NotAvailable*, *apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *other* ou  *null*</span><span class="sxs-lookup"><span data-stu-id="d54cd-260">The property values are: *NotAvailable*, *Apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *Other* or  *null*</span></span> | <span data-ttu-id="d54cd-261">Susceptibles</span><span class="sxs-lookup"><span data-stu-id="d54cd-261">Apt</span></span>
<span data-ttu-id="d54cd-262">assignedTo</span><span class="sxs-lookup"><span data-stu-id="d54cd-262">assignedTo</span></span> | <span data-ttu-id="d54cd-263">Propriétaire de l’incident ou *valeur null* si aucun propriétaire n’est affecté.</span><span class="sxs-lookup"><span data-stu-id="d54cd-263">Owner of the incident, or *null* if no owner is assigned.</span></span> | <span data-ttu-id="d54cd-264">secop2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d54cd-264">secop2@contoso.com</span></span>
<span data-ttu-id="d54cd-265">actorName</span><span class="sxs-lookup"><span data-stu-id="d54cd-265">actorName</span></span> | <span data-ttu-id="d54cd-266">Le groupe d’activités, le cas échéant, associé à cette alerte.</span><span class="sxs-lookup"><span data-stu-id="d54cd-266">The activity group, if any, the  associated with this alert.</span></span> | <span data-ttu-id="d54cd-267">DOSAGE</span><span class="sxs-lookup"><span data-stu-id="d54cd-267">BORON</span></span>
<span data-ttu-id="d54cd-268">threatFamilyName</span><span class="sxs-lookup"><span data-stu-id="d54cd-268">threatFamilyName</span></span> | <span data-ttu-id="d54cd-269">Famille de menaces associée à cette alerte.</span><span class="sxs-lookup"><span data-stu-id="d54cd-269">Threat family associated with this alert.</span></span> | <span data-ttu-id="d54cd-270">null</span><span class="sxs-lookup"><span data-stu-id="d54cd-270">null</span></span>
<span data-ttu-id="d54cd-271">mitreTechniques</span><span class="sxs-lookup"><span data-stu-id="d54cd-271">mitreTechniques</span></span> | <span data-ttu-id="d54cd-272">Les techniques d’attaque, telles que alignées sur l’infrastructure [Mitre ATT&CK](https://attack.mitre.org/)™.</span><span class="sxs-lookup"><span data-stu-id="d54cd-272">The attack techniques, as aligned with the [MITRE ATT&CK](https://attack.mitre.org/)™ framework.</span></span> | \[\]
<span data-ttu-id="d54cd-273">appareils</span><span class="sxs-lookup"><span data-stu-id="d54cd-273">devices</span></span> | <span data-ttu-id="d54cd-274">Tous les appareils pour lesquels des alertes liées à l’incident ont été envoyées.</span><span class="sxs-lookup"><span data-stu-id="d54cd-274">All devices where alerts related to the incident were sent.</span></span> | <span data-ttu-id="d54cd-275">\[\] (voir les détails sur les champs d’entité ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="d54cd-275">\[\] (see details on entity fields below)</span></span>

### <a name="device-format"></a><span data-ttu-id="d54cd-276">Format du périphérique</span><span class="sxs-lookup"><span data-stu-id="d54cd-276">Device format</span></span>

<span data-ttu-id="d54cd-277">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="d54cd-277">Field name</span></span> | <span data-ttu-id="d54cd-278">Description</span><span class="sxs-lookup"><span data-stu-id="d54cd-278">Description</span></span> | <span data-ttu-id="d54cd-279">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="d54cd-279">Example value</span></span>
-|-|-
<span data-ttu-id="d54cd-280">DeviceId</span><span class="sxs-lookup"><span data-stu-id="d54cd-280">DeviceId</span></span> | <span data-ttu-id="d54cd-281">ID de périphérique désigné dans Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="d54cd-281">The device ID as designated in Microsoft Defender ATP.</span></span> | <span data-ttu-id="d54cd-282">24c222b0b60fe148eeece49ac83910cc6a7ef491</span><span class="sxs-lookup"><span data-stu-id="d54cd-282">24c222b0b60fe148eeece49ac83910cc6a7ef491</span></span>
<span data-ttu-id="d54cd-283">aadDeviceId</span><span class="sxs-lookup"><span data-stu-id="d54cd-283">aadDeviceId</span></span> |  <span data-ttu-id="d54cd-284">L’ID de périphérique tel qu’il est désigné dans [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis).</span><span class="sxs-lookup"><span data-stu-id="d54cd-284">The device ID as designated in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis).</span></span> <span data-ttu-id="d54cd-285">Disponible uniquement pour les appareils joints à un domaine.</span><span class="sxs-lookup"><span data-stu-id="d54cd-285">Only available for domain-joined devices.</span></span> | <span data-ttu-id="d54cd-286">null</span><span class="sxs-lookup"><span data-stu-id="d54cd-286">null</span></span>
<span data-ttu-id="d54cd-287">deviceDnsName</span><span class="sxs-lookup"><span data-stu-id="d54cd-287">deviceDnsName</span></span> | <span data-ttu-id="d54cd-288">Nom de domaine complet du périphérique.</span><span class="sxs-lookup"><span data-stu-id="d54cd-288">The fully qualified domain name for the device.</span></span> | <span data-ttu-id="d54cd-289">user5cx.middleeast.corp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d54cd-289">user5cx.middleeast.corp.contoso.com</span></span>
<span data-ttu-id="d54cd-290">osPlatform</span><span class="sxs-lookup"><span data-stu-id="d54cd-290">osPlatform</span></span> | <span data-ttu-id="d54cd-291">Plateforme de système d’exploitation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d54cd-291">The OS platform the device is running.</span></span>| <span data-ttu-id="d54cd-292">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="d54cd-292">WindowsServer2016</span></span>
<span data-ttu-id="d54cd-293">osBuild</span><span class="sxs-lookup"><span data-stu-id="d54cd-293">osBuild</span></span> | <span data-ttu-id="d54cd-294">Version de build pour le système d’exploitation sur lequel l’appareil est exécuté.</span><span class="sxs-lookup"><span data-stu-id="d54cd-294">The build version for the OS the device is running.</span></span> | <span data-ttu-id="d54cd-295">14393</span><span class="sxs-lookup"><span data-stu-id="d54cd-295">14393</span></span>
<span data-ttu-id="d54cd-296">rbacGroupName</span><span class="sxs-lookup"><span data-stu-id="d54cd-296">rbacGroupName</span></span> | <span data-ttu-id="d54cd-297">Le groupe de [contrôle d’accès basé sur un rôle](https://docs.microsoft.com/azure/role-based-access-control/overview) (RBAC) associé au périphérique.</span><span class="sxs-lookup"><span data-stu-id="d54cd-297">The [role-based access control](https://docs.microsoft.com/azure/role-based-access-control/overview) (RBAC) group associated with the device.</span></span> | <span data-ttu-id="d54cd-298">WDATP-Ring0</span><span class="sxs-lookup"><span data-stu-id="d54cd-298">WDATP-Ring0</span></span>
<span data-ttu-id="d54cd-299">firstSeen</span><span class="sxs-lookup"><span data-stu-id="d54cd-299">firstSeen</span></span> | <span data-ttu-id="d54cd-300">Heure du premier démarrage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d54cd-300">Time when device was first seen.</span></span> | <span data-ttu-id="d54cd-301">2020-02-06T14:16:01.9330135 Z</span><span class="sxs-lookup"><span data-stu-id="d54cd-301">2020-02-06T14:16:01.9330135Z</span></span>
<span data-ttu-id="d54cd-302">healthStatus</span><span class="sxs-lookup"><span data-stu-id="d54cd-302">healthStatus</span></span> | <span data-ttu-id="d54cd-303">État d’intégrité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d54cd-303">The health state of the device.</span></span> | <span data-ttu-id="d54cd-304">Actif</span><span class="sxs-lookup"><span data-stu-id="d54cd-304">Active</span></span>
<span data-ttu-id="d54cd-305">riskScore</span><span class="sxs-lookup"><span data-stu-id="d54cd-305">riskScore</span></span> | <span data-ttu-id="d54cd-306">Score de risque de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d54cd-306">The risk score for the  device.</span></span> | <span data-ttu-id="d54cd-307">Élevé</span><span class="sxs-lookup"><span data-stu-id="d54cd-307">High</span></span>
<span data-ttu-id="d54cd-308">entités</span><span class="sxs-lookup"><span data-stu-id="d54cd-308">entities</span></span> | <span data-ttu-id="d54cd-309">Toutes les entités identifiées comme faisant partie d’une alerte donnée ou associées à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="d54cd-309">All entities that have been identified to be part of, or related to, a given alert.</span></span> | <span data-ttu-id="d54cd-310">\[\] (voir les détails sur les champs d’entité ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="d54cd-310">\[\] (see details on entity fields below)</span></span>

### <a name="entity-format"></a><span data-ttu-id="d54cd-311">Format d’entité</span><span class="sxs-lookup"><span data-stu-id="d54cd-311">Entity Format</span></span>

<span data-ttu-id="d54cd-312">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="d54cd-312">Field name</span></span> | <span data-ttu-id="d54cd-313">Description</span><span class="sxs-lookup"><span data-stu-id="d54cd-313">Description</span></span> | <span data-ttu-id="d54cd-314">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="d54cd-314">Example value</span></span>
-|-|-
<span data-ttu-id="d54cd-315">entityType</span><span class="sxs-lookup"><span data-stu-id="d54cd-315">entityType</span></span> | <span data-ttu-id="d54cd-316">Entités identifiées comme faisant partie d’une alerte donnée ou associées à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="d54cd-316">Entities that have been identified to be part of, or related to, a given alert.</span></span><br><span data-ttu-id="d54cd-317">Les valeurs des propriétés sont les suivantes : *User*, *IP*, *URL*, *file*, *Process*, *Mailbox*, *MailMessage*, *MailCluster*, *Registry*</span><span class="sxs-lookup"><span data-stu-id="d54cd-317">The properties values are: *User*, *Ip*, *Url*, *File*, *Process*, *MailBox*, *MailMessage*, *MailCluster*, *Registry*</span></span> | <span data-ttu-id="d54cd-318">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="d54cd-318">User</span></span>
<span data-ttu-id="d54cd-319">Algorithm</span><span class="sxs-lookup"><span data-stu-id="d54cd-319">sha1</span></span> | <span data-ttu-id="d54cd-320">Disponible si entityType est un *fichier*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-320">Available if entityType is *File*.</span></span><br><span data-ttu-id="d54cd-321">Hachage de fichier pour les alertes associées à un fichier ou à un processus.</span><span class="sxs-lookup"><span data-stu-id="d54cd-321">The file hash for alerts associated with a file or process.</span></span> | <span data-ttu-id="d54cd-322">5de839186691aa96ee2ca6d74f0a38fb8d1bd6dd</span><span class="sxs-lookup"><span data-stu-id="d54cd-322">5de839186691aa96ee2ca6d74f0a38fb8d1bd6dd</span></span>
<span data-ttu-id="d54cd-323">SHA256</span><span class="sxs-lookup"><span data-stu-id="d54cd-323">sha256</span></span> | <span data-ttu-id="d54cd-324">Disponible si entityType est un *fichier*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-324">Available if entityType is *File*.</span></span><br><span data-ttu-id="d54cd-325">Hachage de fichier pour les alertes associées à un fichier ou à un processus.</span><span class="sxs-lookup"><span data-stu-id="d54cd-325">The file hash for alerts associated with a file or process.</span></span> | <span data-ttu-id="d54cd-326">28cb017dfc99073aa1b47c1b30f413e3ce774c4991eb4158de50f9dbb36d8043</span><span class="sxs-lookup"><span data-stu-id="d54cd-326">28cb017dfc99073aa1b47c1b30f413e3ce774c4991eb4158de50f9dbb36d8043</span></span>
<span data-ttu-id="d54cd-327">fileName</span><span class="sxs-lookup"><span data-stu-id="d54cd-327">fileName</span></span> | <span data-ttu-id="d54cd-328">Disponible si entityType est un *fichier*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-328">Available if entityType is *File*.</span></span><br><span data-ttu-id="d54cd-329">Nom de fichier pour les alertes associées à un fichier ou à un processus</span><span class="sxs-lookup"><span data-stu-id="d54cd-329">The file name for alerts associated with a file or process</span></span> | <span data-ttu-id="d54cd-330">Detector.UnitTests.dll</span><span class="sxs-lookup"><span data-stu-id="d54cd-330">Detector.UnitTests.dll</span></span>
<span data-ttu-id="d54cd-331">PCF</span><span class="sxs-lookup"><span data-stu-id="d54cd-331">filePath</span></span> | <span data-ttu-id="d54cd-332">Disponible si entityType est un *fichier*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-332">Available if entityType is *File*.</span></span><br><span data-ttu-id="d54cd-333">Chemin d’accès de fichier pour les alertes associées à un fichier ou à un processus</span><span class="sxs-lookup"><span data-stu-id="d54cd-333">The file path for alerts associated with a file or process</span></span> | <span data-ttu-id="d54cd-334">C : \\ \ agent_work_temp \deploy\system\2020-09-06 12_14_54</span><span class="sxs-lookup"><span data-stu-id="d54cd-334">C:\\\agent_work_temp\Deploy\SYSTEM\2020-09-06 12_14_54\Out</span></span>
<span data-ttu-id="d54cd-335">processId</span><span class="sxs-lookup"><span data-stu-id="d54cd-335">processId</span></span> | <span data-ttu-id="d54cd-336">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-336">Available if entityType is *Process*.</span></span> | <span data-ttu-id="d54cd-337">24348</span><span class="sxs-lookup"><span data-stu-id="d54cd-337">24348</span></span>
<span data-ttu-id="d54cd-338">processCommandLine</span><span class="sxs-lookup"><span data-stu-id="d54cd-338">processCommandLine</span></span> | <span data-ttu-id="d54cd-339">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-339">Available if entityType is *Process*.</span></span> | <span data-ttu-id="d54cd-340">« Votre fichier est prêt à télécharger \_1911150169.exe »</span><span class="sxs-lookup"><span data-stu-id="d54cd-340">"Your File Is Ready To Download\_1911150169.exe"</span></span>
<span data-ttu-id="d54cd-341">processCreationTime</span><span class="sxs-lookup"><span data-stu-id="d54cd-341">processCreationTime</span></span> | <span data-ttu-id="d54cd-342">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-342">Available if entityType is *Process*.</span></span> | <span data-ttu-id="d54cd-343">2020-07-18T03:25:38.5269993 Z</span><span class="sxs-lookup"><span data-stu-id="d54cd-343">2020-07-18T03:25:38.5269993Z</span></span>
<span data-ttu-id="d54cd-344">parentProcessId</span><span class="sxs-lookup"><span data-stu-id="d54cd-344">parentProcessId</span></span> | <span data-ttu-id="d54cd-345">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-345">Available if entityType is *Process*.</span></span> | <span data-ttu-id="d54cd-346">16840</span><span class="sxs-lookup"><span data-stu-id="d54cd-346">16840</span></span>
<span data-ttu-id="d54cd-347">parentProcessCreationTime</span><span class="sxs-lookup"><span data-stu-id="d54cd-347">parentProcessCreationTime</span></span> | <span data-ttu-id="d54cd-348">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-348">Available if entityType is *Process*.</span></span> | <span data-ttu-id="d54cd-349">2020-07-18T02:12:32.8616797 Z</span><span class="sxs-lookup"><span data-stu-id="d54cd-349">2020-07-18T02:12:32.8616797Z</span></span>
<span data-ttu-id="d54cd-350">ipAddress</span><span class="sxs-lookup"><span data-stu-id="d54cd-350">ipAddress</span></span> | <span data-ttu-id="d54cd-351">Disponible si entityType est *IP*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-351">Available if entityType is *Ip*.</span></span> <br><span data-ttu-id="d54cd-352">Adresse IP pour les alertes associées à des événements réseau, comme *la communication avec une destination réseau malveillante*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-352">IP address for alerts associated with network events, such as *Communication to a malicious network destination*.</span></span> | <span data-ttu-id="d54cd-353">62.216.203.204</span><span class="sxs-lookup"><span data-stu-id="d54cd-353">62.216.203.204</span></span>
<span data-ttu-id="d54cd-354">url</span><span class="sxs-lookup"><span data-stu-id="d54cd-354">url</span></span> | <span data-ttu-id="d54cd-355">Disponible si entityType est *URL*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-355">Available if entityType is *Url*.</span></span> <br><span data-ttu-id="d54cd-356">URL pour les alertes associées aux événements réseau, comme *la communication à une destination réseau malveillante*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-356">Url for alerts associated to network events, such as, *Communication to a malicious network destination*.</span></span> | <span data-ttu-id="d54cd-357">down.esales360.cn</span><span class="sxs-lookup"><span data-stu-id="d54cd-357">down.esales360.cn</span></span>
<span data-ttu-id="d54cd-358">accountName</span><span class="sxs-lookup"><span data-stu-id="d54cd-358">accountName</span></span> | <span data-ttu-id="d54cd-359">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-359">Available if entityType is *User*.</span></span> | <span data-ttu-id="d54cd-360">testUser2</span><span class="sxs-lookup"><span data-stu-id="d54cd-360">testUser2</span></span>
<span data-ttu-id="d54cd-361">domainName</span><span class="sxs-lookup"><span data-stu-id="d54cd-361">domainName</span></span> | <span data-ttu-id="d54cd-362">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-362">Available if entityType is *User*.</span></span> | <span data-ttu-id="d54cd-363">Europe. Corp. contoso</span><span class="sxs-lookup"><span data-stu-id="d54cd-363">europe.corp.contoso</span></span>
<span data-ttu-id="d54cd-364">userSid</span><span class="sxs-lookup"><span data-stu-id="d54cd-364">userSid</span></span> | <span data-ttu-id="d54cd-365">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-365">Available if entityType is *User*.</span></span> | <span data-ttu-id="d54cd-366">S-1-5-21-1721254763-462695806-1538882281-4156657</span><span class="sxs-lookup"><span data-stu-id="d54cd-366">S-1-5-21-1721254763-462695806-1538882281-4156657</span></span>
<span data-ttu-id="d54cd-367">aadUserId</span><span class="sxs-lookup"><span data-stu-id="d54cd-367">aadUserId</span></span> | <span data-ttu-id="d54cd-368">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-368">Available if entityType is *User*.</span></span> | <span data-ttu-id="d54cd-369">fc8f7484-f813-4db2-afab-bc1507913fb6</span><span class="sxs-lookup"><span data-stu-id="d54cd-369">fc8f7484-f813-4db2-afab-bc1507913fb6</span></span>
<span data-ttu-id="d54cd-370">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d54cd-370">userPrincipalName</span></span> | <span data-ttu-id="d54cd-371">Disponible si EntityType est la / *boîte aux lettres* utilisateur / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-371">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span> | <span data-ttu-id="d54cd-372">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d54cd-372">testUser2@contoso.com</span></span>
<span data-ttu-id="d54cd-373">mailboxDisplayName</span><span class="sxs-lookup"><span data-stu-id="d54cd-373">mailboxDisplayName</span></span> | <span data-ttu-id="d54cd-374">Disponible si entityType est *Mailbox*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-374">Available if entityType is *MailBox*.</span></span> | <span data-ttu-id="d54cd-375">test utilisateur2</span><span class="sxs-lookup"><span data-stu-id="d54cd-375">test User2</span></span>
<span data-ttu-id="d54cd-376">mailboxAddress</span><span class="sxs-lookup"><span data-stu-id="d54cd-376">mailboxAddress</span></span> | <span data-ttu-id="d54cd-377">Disponible si EntityType est la / *boîte aux lettres* utilisateur / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-377">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span> | <span data-ttu-id="d54cd-378">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d54cd-378">testUser2@contoso.com</span></span>
<span data-ttu-id="d54cd-379">clusterBy</span><span class="sxs-lookup"><span data-stu-id="d54cd-379">clusterBy</span></span> | <span data-ttu-id="d54cd-380">Disponible si entityType est  *MailCluster*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-380">Available if entityType is  *MailCluster*.</span></span> | <span data-ttu-id="d54cd-381">Experts P2SenderDomain; ContentType</span><span class="sxs-lookup"><span data-stu-id="d54cd-381">Subject;P2SenderDomain;ContentType</span></span>
<span data-ttu-id="d54cd-382">sender</span><span class="sxs-lookup"><span data-stu-id="d54cd-382">sender</span></span> | <span data-ttu-id="d54cd-383">Disponible si EntityType est la / *boîte aux lettres* utilisateur / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-383">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span> | <span data-ttu-id="d54cd-384">user.abc@mail.contoso.co.in</span><span class="sxs-lookup"><span data-stu-id="d54cd-384">user.abc@mail.contoso.co.in</span></span>
<span data-ttu-id="d54cd-385">destinataire</span><span class="sxs-lookup"><span data-stu-id="d54cd-385">recipient</span></span> | <span data-ttu-id="d54cd-386">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-386">Available if entityType is *MailMessage*.</span></span> | <span data-ttu-id="d54cd-387">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d54cd-387">testUser2@contoso.com</span></span>
<span data-ttu-id="d54cd-388">sujet</span><span class="sxs-lookup"><span data-stu-id="d54cd-388">subject</span></span> | <span data-ttu-id="d54cd-389">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-389">Available if entityType is *MailMessage*.</span></span> | <span data-ttu-id="d54cd-390">\[\]Attention externe</span><span class="sxs-lookup"><span data-stu-id="d54cd-390">\[EXTERNAL\] Attention</span></span>
<span data-ttu-id="d54cd-391">deliveryAction</span><span class="sxs-lookup"><span data-stu-id="d54cd-391">deliveryAction</span></span> | <span data-ttu-id="d54cd-392">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-392">Available if entityType is *MailMessage*.</span></span> | <span data-ttu-id="d54cd-393">Cmds</span><span class="sxs-lookup"><span data-stu-id="d54cd-393">Delivered</span></span>
<span data-ttu-id="d54cd-394">securityGroupId</span><span class="sxs-lookup"><span data-stu-id="d54cd-394">securityGroupId</span></span> | <span data-ttu-id="d54cd-395">Disponible si entityType est  *SecurityGroup*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-395">Available if entityType is  *SecurityGroup*.</span></span> | <span data-ttu-id="d54cd-396">301c47c8-e15f-4059-AB09-e2ba9ffd372b</span><span class="sxs-lookup"><span data-stu-id="d54cd-396">301c47c8-e15f-4059-ab09-e2ba9ffd372b</span></span>
<span data-ttu-id="d54cd-397">securityGroupName</span><span class="sxs-lookup"><span data-stu-id="d54cd-397">securityGroupName</span></span> | <span data-ttu-id="d54cd-398">Disponible si entityType est  *SecurityGroup*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-398">Available if entityType is  *SecurityGroup*.</span></span> | <span data-ttu-id="d54cd-399">Opérateurs de configuration réseau</span><span class="sxs-lookup"><span data-stu-id="d54cd-399">Network Configuration Operators</span></span>
<span data-ttu-id="d54cd-400">registryHive</span><span class="sxs-lookup"><span data-stu-id="d54cd-400">registryHive</span></span> | <span data-ttu-id="d54cd-401">Disponible si entityType est  *Registry*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-401">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="d54cd-402">HKEY \_ local \_ machine</span><span class="sxs-lookup"><span data-stu-id="d54cd-402">HKEY\_LOCAL\_MACHINE</span></span> |
<span data-ttu-id="d54cd-403">registryKey</span><span class="sxs-lookup"><span data-stu-id="d54cd-403">registryKey</span></span> | <span data-ttu-id="d54cd-404">Disponible si entityType est  *Registry*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-404">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="d54cd-405">SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon</span><span class="sxs-lookup"><span data-stu-id="d54cd-405">SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon</span></span>
<span data-ttu-id="d54cd-406">registryValueType</span><span class="sxs-lookup"><span data-stu-id="d54cd-406">registryValueType</span></span> | <span data-ttu-id="d54cd-407">Disponible si entityType est  *Registry*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-407">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="d54cd-408">String</span><span class="sxs-lookup"><span data-stu-id="d54cd-408">String</span></span>
<span data-ttu-id="d54cd-409">registryValue</span><span class="sxs-lookup"><span data-stu-id="d54cd-409">registryValue</span></span> | <span data-ttu-id="d54cd-410">Disponible si entityType est  *Registry*.</span><span class="sxs-lookup"><span data-stu-id="d54cd-410">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="d54cd-411">31-00-00-00</span><span class="sxs-lookup"><span data-stu-id="d54cd-411">31-00-00-00</span></span>
<span data-ttu-id="d54cd-412">deviceId</span><span class="sxs-lookup"><span data-stu-id="d54cd-412">deviceId</span></span> | <span data-ttu-id="d54cd-413">ID, le cas échéant, de l’appareil associé à l’entité.</span><span class="sxs-lookup"><span data-stu-id="d54cd-413">The ID, if any, of the device related to the entity.</span></span> | <span data-ttu-id="d54cd-414">986e5df8b73dacd43c8917d17e523e76b13c75cd</span><span class="sxs-lookup"><span data-stu-id="d54cd-414">986e5df8b73dacd43c8917d17e523e76b13c75cd</span></span>

## <a name="example"></a><span data-ttu-id="d54cd-415">Exemple</span><span class="sxs-lookup"><span data-stu-id="d54cd-415">Example</span></span>

<span data-ttu-id="d54cd-416">**Demande**</span><span class="sxs-lookup"><span data-stu-id="d54cd-416">**Request**</span></span>

```HTTP
GET https://api.security.microsoft.com/api/incidents
```

<span data-ttu-id="d54cd-417">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="d54cd-417">**Response**</span></span>

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

## <a name="related-articles"></a><span data-ttu-id="d54cd-418">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="d54cd-418">Related articles</span></span>

- [<span data-ttu-id="d54cd-419">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d54cd-419">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="d54cd-420">En savoir plus sur les limites d’API et la gestion des licences</span><span class="sxs-lookup"><span data-stu-id="d54cd-420">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="d54cd-421">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d54cd-421">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="d54cd-422">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="d54cd-422">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="d54cd-423">API d’incident</span><span class="sxs-lookup"><span data-stu-id="d54cd-423">Incident APIs</span></span>](api-incident.md)
- [<span data-ttu-id="d54cd-424">Mettre à jour l’API incident</span><span class="sxs-lookup"><span data-stu-id="d54cd-424">Update incident API</span></span>](api-update-incidents.md)
