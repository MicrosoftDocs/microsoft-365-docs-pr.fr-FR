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
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 833bc1d8284829323cc2f0c391e42f4e563a6948
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730881"
---
# <a name="list-incidents-api-in-microsoft-365-defender"></a><span data-ttu-id="3c0b6-104">API de liste des incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3c0b6-104">List incidents API in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="3c0b6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3c0b6-105">**Applies to:**</span></span>

- [<span data-ttu-id="3c0b6-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3c0b6-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!IMPORTANT]
> <span data-ttu-id="3c0b6-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3c0b6-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


## <a name="api-description"></a><span data-ttu-id="3c0b6-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="3c0b6-109">API description</span></span>

<span data-ttu-id="3c0b6-110">L’API des incidents de liste vous permet de trier les incidents pour créer une réponse de cybersécurité informée.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-110">The list incidents API allows you to sort through incidents to create an informed cybersecurity response.</span></span> <span data-ttu-id="3c0b6-111">Il expose un ensemble d’incidents qui ont été signalés dans votre réseau, dans la plage de temps que vous avez spécifiée dans votre stratégie de rétention d’environnement.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-111">It exposes a collection of incidents that were flagged in your network, within the time range you specified in your environment retention policy.</span></span> <span data-ttu-id="3c0b6-112">Les incidents les plus récents sont affichés en haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-112">The most recent incidents are displayed at the top of the list.</span></span> <span data-ttu-id="3c0b6-113">Chaque incident contient un tableau d’alertes associées et leurs entités connexes.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-113">Each incident contains an array of related alerts, and their related entities.</span></span>

<span data-ttu-id="3c0b6-114">L’API prend en charge les opérateurs **OData suivants** :</span><span class="sxs-lookup"><span data-stu-id="3c0b6-114">The API supports the following **OData** operators:</span></span>

- <span data-ttu-id="3c0b6-115">`$filter` sur `lastUpdateTime` le `createdTime` , et les `status` `assignedTo` propriétés</span><span class="sxs-lookup"><span data-stu-id="3c0b6-115">`$filter` on the `lastUpdateTime`, `createdTime`, `status`, and `assignedTo` properties</span></span>
- <span data-ttu-id="3c0b6-116">`$top`, avec une valeur maximale de **100**</span><span class="sxs-lookup"><span data-stu-id="3c0b6-116">`$top`, with a maximum value of **100**</span></span>
- `$skip`

## <a name="limitations"></a><span data-ttu-id="3c0b6-117">Limites</span><span class="sxs-lookup"><span data-stu-id="3c0b6-117">Limitations</span></span>

1. <span data-ttu-id="3c0b6-118">La taille maximale de page **est de 100 incidents.**</span><span class="sxs-lookup"><span data-stu-id="3c0b6-118">Maximum page size is **100 incidents**.</span></span>
2. <span data-ttu-id="3c0b6-119">Le taux maximal de demandes est **de 50 appels par minute** et de **1 500 appels par heure.**</span><span class="sxs-lookup"><span data-stu-id="3c0b6-119">Maximum rate of requests is **50 calls per minute** and **1500 calls per hour**.</span></span>

## <a name="permissions"></a><span data-ttu-id="3c0b6-120">Autorisations</span><span class="sxs-lookup"><span data-stu-id="3c0b6-120">Permissions</span></span>

<span data-ttu-id="3c0b6-121">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-121">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="3c0b6-122">Pour en savoir plus, notamment sur le choix des autorisations, consultez les API [Access Microsoft 365 Defender](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="3c0b6-122">To learn more, including how to choose permissions, see [Access Microsoft 365 Defender APIs](api-access.md)</span></span>

<span data-ttu-id="3c0b6-123">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="3c0b6-123">Permission type</span></span> | <span data-ttu-id="3c0b6-124">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3c0b6-124">Permission</span></span> | <span data-ttu-id="3c0b6-125">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="3c0b6-125">Permission display name</span></span>
-|-|-
<span data-ttu-id="3c0b6-126">Application</span><span class="sxs-lookup"><span data-stu-id="3c0b6-126">Application</span></span> | <span data-ttu-id="3c0b6-127">Incident.Read.All</span><span class="sxs-lookup"><span data-stu-id="3c0b6-127">Incident.Read.All</span></span> | <span data-ttu-id="3c0b6-128">Lire tous les incidents</span><span class="sxs-lookup"><span data-stu-id="3c0b6-128">Read all incidents</span></span>
<span data-ttu-id="3c0b6-129">Application</span><span class="sxs-lookup"><span data-stu-id="3c0b6-129">Application</span></span> | <span data-ttu-id="3c0b6-130">Incident.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3c0b6-130">Incident.ReadWrite.All</span></span> | <span data-ttu-id="3c0b6-131">Lire et écrire tous les incidents</span><span class="sxs-lookup"><span data-stu-id="3c0b6-131">Read and write all incidents</span></span>
<span data-ttu-id="3c0b6-132">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="3c0b6-132">Delegated (work or school account)</span></span> | <span data-ttu-id="3c0b6-133">Incident.Read</span><span class="sxs-lookup"><span data-stu-id="3c0b6-133">Incident.Read</span></span> | <span data-ttu-id="3c0b6-134">Lire les incidents</span><span class="sxs-lookup"><span data-stu-id="3c0b6-134">Read incidents</span></span>
<span data-ttu-id="3c0b6-135">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="3c0b6-135">Delegated (work or school account)</span></span> | <span data-ttu-id="3c0b6-136">Incident.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3c0b6-136">Incident.ReadWrite</span></span> | <span data-ttu-id="3c0b6-137">Lire et écrire des incidents</span><span class="sxs-lookup"><span data-stu-id="3c0b6-137">Read and write incidents</span></span>

> [!Note]
> <span data-ttu-id="3c0b6-138">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3c0b6-138">When obtaining a token using user credentials:</span></span>
>
> - <span data-ttu-id="3c0b6-139">L’utilisateur doit avoir l’autorisation d’afficher les incidents dans le portail.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-139">The user needs to have view permission for incidents in the portal.</span></span>
> - <span data-ttu-id="3c0b6-140">La réponse inclut uniquement les incidents que l’utilisateur est exposé.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-140">The response will only include incidents that the user is exposed to.</span></span>

## <a name="http-request"></a><span data-ttu-id="3c0b6-141">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="3c0b6-141">HTTP request</span></span>

```HTTP
GET /api/incidents
```

## <a name="request-headers"></a><span data-ttu-id="3c0b6-142">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="3c0b6-142">Request headers</span></span>

<span data-ttu-id="3c0b6-143">Nom</span><span class="sxs-lookup"><span data-stu-id="3c0b6-143">Name</span></span> | <span data-ttu-id="3c0b6-144">Type</span><span class="sxs-lookup"><span data-stu-id="3c0b6-144">Type</span></span> | <span data-ttu-id="3c0b6-145">Description</span><span class="sxs-lookup"><span data-stu-id="3c0b6-145">Description</span></span>
-|-|-
<span data-ttu-id="3c0b6-146">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3c0b6-146">Authorization</span></span> | <span data-ttu-id="3c0b6-147">String</span><span class="sxs-lookup"><span data-stu-id="3c0b6-147">String</span></span> | <span data-ttu-id="3c0b6-148">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-148">Bearer {token}.</span></span> <span data-ttu-id="3c0b6-149">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="3c0b6-149">**Required**</span></span>


## <a name="request-body"></a><span data-ttu-id="3c0b6-150">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="3c0b6-150">Request body</span></span>

<span data-ttu-id="3c0b6-151">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-151">None.</span></span>

## <a name="response"></a><span data-ttu-id="3c0b6-152">Réponse</span><span class="sxs-lookup"><span data-stu-id="3c0b6-152">Response</span></span>

<span data-ttu-id="3c0b6-153">Si elle réussit, cette méthode renvoie `200 OK` et une liste des [incidents](api-incident.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-153">If successful, this method returns `200 OK`, and a list of [incidents](api-incident.md) in the response body.</span></span>

## <a name="schema-mapping"></a><span data-ttu-id="3c0b6-154">Mappage de schéma</span><span class="sxs-lookup"><span data-stu-id="3c0b6-154">Schema mapping</span></span>

### <a name="incident-metadata"></a><span data-ttu-id="3c0b6-155">Métadonnées d’incident</span><span class="sxs-lookup"><span data-stu-id="3c0b6-155">Incident metadata</span></span>

<span data-ttu-id="3c0b6-156">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="3c0b6-156">Field name</span></span> | <span data-ttu-id="3c0b6-157">Description</span><span class="sxs-lookup"><span data-stu-id="3c0b6-157">Description</span></span> | <span data-ttu-id="3c0b6-158">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="3c0b6-158">Example value</span></span>
-|-|-
<span data-ttu-id="3c0b6-159">incidentId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-159">incidentId</span></span> | <span data-ttu-id="3c0b6-160">Identificateur unique pour représenter l’incident</span><span class="sxs-lookup"><span data-stu-id="3c0b6-160">Unique identifier to represent the incident</span></span> | <span data-ttu-id="3c0b6-161">924565</span><span class="sxs-lookup"><span data-stu-id="3c0b6-161">924565</span></span>
<span data-ttu-id="3c0b6-162">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-162">redirectIncidentId</span></span> | <span data-ttu-id="3c0b6-163">Uniquement rempli au cas où un incident est regroupé avec un autre incident, dans le cadre de la logique de traitement des incidents.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-163">Only populated in case an incident is being grouped together with another incident, as part of the incident processing logic.</span></span> | <span data-ttu-id="3c0b6-164">924569</span><span class="sxs-lookup"><span data-stu-id="3c0b6-164">924569</span></span>
<span data-ttu-id="3c0b6-165">incidentName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-165">incidentName</span></span> | <span data-ttu-id="3c0b6-166">Valeur de chaîne disponible pour chaque incident.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-166">String value available for every incident.</span></span> | <span data-ttu-id="3c0b6-167">Activité de rançongiciel</span><span class="sxs-lookup"><span data-stu-id="3c0b6-167">Ransomware activity</span></span>
<span data-ttu-id="3c0b6-168">createdTime</span><span class="sxs-lookup"><span data-stu-id="3c0b6-168">createdTime</span></span> | <span data-ttu-id="3c0b6-169">Heure à partir de la première création de l’incident.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-169">Time when incident was first created.</span></span> | <span data-ttu-id="3c0b6-170">2020-09-06T14:46:57.0733333Z</span><span class="sxs-lookup"><span data-stu-id="3c0b6-170">2020-09-06T14:46:57.0733333Z</span></span>
<span data-ttu-id="3c0b6-171">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="3c0b6-171">lastUpdateTime</span></span> | <span data-ttu-id="3c0b6-172">Heure de la dernière mise à jour de l’incident sur le back-end.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-172">Time when the incident was last updated on the backend.</span></span><br /><br /> <span data-ttu-id="3c0b6-173">Ce champ peut être utilisé lorsque vous paramétrez le paramètre de demande pour la durée de récupération des incidents.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-173">This field can be used when you're setting the request parameter for the range of time that incidents are retrieved.</span></span> | <span data-ttu-id="3c0b6-174">2020-09-06T14:46:57.29Z</span><span class="sxs-lookup"><span data-stu-id="3c0b6-174">2020-09-06T14:46:57.29Z</span></span>
<span data-ttu-id="3c0b6-175">assignedTo</span><span class="sxs-lookup"><span data-stu-id="3c0b6-175">assignedTo</span></span> | <span data-ttu-id="3c0b6-176">Propriétaire de l’incident ou *null* si aucun propriétaire n’est affecté.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-176">Owner of the incident, or *null* if no owner is assigned.</span></span> | <span data-ttu-id="3c0b6-177">secop2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="3c0b6-177">secop2@contoso.com</span></span>
<span data-ttu-id="3c0b6-178">classification</span><span class="sxs-lookup"><span data-stu-id="3c0b6-178">classification</span></span> | <span data-ttu-id="3c0b6-179">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-179">The specification for the incident.</span></span> <span data-ttu-id="3c0b6-180">Les valeurs de propriété *sont : Unknown*, *FalsePositive*, *TruePositive*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-180">The property values are: *Unknown*, *FalsePositive*, *TruePositive*</span></span> | <span data-ttu-id="3c0b6-181">Inconnu</span><span class="sxs-lookup"><span data-stu-id="3c0b6-181">Unknown</span></span>
<span data-ttu-id="3c0b6-182">détermination</span><span class="sxs-lookup"><span data-stu-id="3c0b6-182">determination</span></span> | <span data-ttu-id="3c0b6-183">Spécifie la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-183">Specifies the determination of the incident.</span></span> <span data-ttu-id="3c0b6-184">Les valeurs de propriété sont *: NotAvailable*, *Apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *Other*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-184">The property values are: *NotAvailable*, *Apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *Other*</span></span> | <span data-ttu-id="3c0b6-185">NotAvailable</span><span class="sxs-lookup"><span data-stu-id="3c0b6-185">NotAvailable</span></span>
<span data-ttu-id="3c0b6-186">status</span><span class="sxs-lookup"><span data-stu-id="3c0b6-186">status</span></span> | <span data-ttu-id="3c0b6-187">Catégoriser les incidents *(en tant qu’incidents actifs* *ou résolus).*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-187">Categorize incidents (as *Active*, or *Resolved*).</span></span> <span data-ttu-id="3c0b6-188">Il peut vous aider à organiser et à gérer votre réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-188">It can help you organize and manage your response to incidents.</span></span> | <span data-ttu-id="3c0b6-189">Actif</span><span class="sxs-lookup"><span data-stu-id="3c0b6-189">Active</span></span>
<span data-ttu-id="3c0b6-190">Sévérité </span><span class="sxs-lookup"><span data-stu-id="3c0b6-190">severity</span></span> | <span data-ttu-id="3c0b6-191">Indique l’impact possible sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-191">Indicates the possible impact on assets.</span></span> <span data-ttu-id="3c0b6-192">Plus la gravité est élevée, plus l’impact est important.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-192">The higher the severity the bigger the impact.</span></span> <span data-ttu-id="3c0b6-193">En règle générale, les éléments de gravité plus élevée nécessitent l’attention la plus immédiate.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-193">Typically higher severity items require the most immediate attention.</span></span><br /><br /><span data-ttu-id="3c0b6-194">Une des valeurs suivantes *: Informational,* \*Low,\*\*Medium et *High*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-194">One of the following values: *Informational*, *Low*, \*Medium, and *High*.</span></span> | <span data-ttu-id="3c0b6-195">Moyenne</span><span class="sxs-lookup"><span data-stu-id="3c0b6-195">Medium</span></span>
<span data-ttu-id="3c0b6-196">étiquettes</span><span class="sxs-lookup"><span data-stu-id="3c0b6-196">tags</span></span> | <span data-ttu-id="3c0b6-197">Tableau de balises personnalisées associées à un incident, par exemple pour baliser un groupe d’incidents avec une caractéristique commune.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-197">Array of custom tags associated with an incident, for example to flag a group of incidents with a common characteristic.</span></span> | \[\]
<span data-ttu-id="3c0b6-198">commentaires</span><span class="sxs-lookup"><span data-stu-id="3c0b6-198">comments</span></span> | <span data-ttu-id="3c0b6-199">Tableau de commentaires créés par des secops lors de la gestion de l’incident, par exemple des informations supplémentaires sur la sélection de classification.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-199">Array of comments created by secops when managing the incident, for example additional information about the classification selection.</span></span> | \[\]
<span data-ttu-id="3c0b6-200">alerts</span><span class="sxs-lookup"><span data-stu-id="3c0b6-200">alerts</span></span> | <span data-ttu-id="3c0b6-201">Tableau contenant toutes les alertes liées à l’incident, ainsi que d’autres informations, telles que la gravité, les entités impliquées dans l’alerte et la source des alertes.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-201">Array containing all of the alerts related to the incident, plus other information, such as severity, entities that were involved in the alert, and the source of the alerts.</span></span> | <span data-ttu-id="3c0b6-202">\[\] (voir les détails sur les champs d’alerte ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="3c0b6-202">\[\] (see details on alert fields below)</span></span>

### <a name="alerts-metadata"></a><span data-ttu-id="3c0b6-203">Métadonnées des alertes</span><span class="sxs-lookup"><span data-stu-id="3c0b6-203">Alerts metadata</span></span>

<span data-ttu-id="3c0b6-204">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="3c0b6-204">Field name</span></span> | <span data-ttu-id="3c0b6-205">Description</span><span class="sxs-lookup"><span data-stu-id="3c0b6-205">Description</span></span> | <span data-ttu-id="3c0b6-206">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="3c0b6-206">Example value</span></span>
-|-|-
<span data-ttu-id="3c0b6-207">alertId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-207">alertId</span></span> | <span data-ttu-id="3c0b6-208">Identificateur unique pour représenter l’alerte</span><span class="sxs-lookup"><span data-stu-id="3c0b6-208">Unique identifier to represent the alert</span></span> | <span data-ttu-id="3c0b6-209">caD70CFEE2-1F54-32DB-9988-3A868A1EBFAC</span><span class="sxs-lookup"><span data-stu-id="3c0b6-209">caD70CFEE2-1F54-32DB-9988-3A868A1EBFAC</span></span>
<span data-ttu-id="3c0b6-210">incidentId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-210">incidentId</span></span> | <span data-ttu-id="3c0b6-211">Identificateur unique représentant l’incident associé à cette alerte</span><span class="sxs-lookup"><span data-stu-id="3c0b6-211">Unique identifier to represent the incident this alert is associated with</span></span> | <span data-ttu-id="3c0b6-212">924565</span><span class="sxs-lookup"><span data-stu-id="3c0b6-212">924565</span></span>
<span data-ttu-id="3c0b6-213">serviceSource</span><span class="sxs-lookup"><span data-stu-id="3c0b6-213">serviceSource</span></span> | <span data-ttu-id="3c0b6-214">Service dont provient l’alerte, tel que Microsoft Defender pour le point de terminaison, Microsoft Cloud App Security, Microsoft Defender pour l’identité ou Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-214">Service that the alert originates from, such as Microsoft Defender for Endpoint, Microsoft Cloud App Security, Microsoft Defender for Identity, or Microsoft Defender for Office 365.</span></span> | <span data-ttu-id="3c0b6-215">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="3c0b6-215">MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="3c0b6-216">creationTime</span><span class="sxs-lookup"><span data-stu-id="3c0b6-216">creationTime</span></span> | <span data-ttu-id="3c0b6-217">Heure à partir de la première création de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-217">Time when alert was first created.</span></span> | <span data-ttu-id="3c0b6-218">2020-09-06T14:46:55.7182276Z</span><span class="sxs-lookup"><span data-stu-id="3c0b6-218">2020-09-06T14:46:55.7182276Z</span></span>
<span data-ttu-id="3c0b6-219">lastUpdatedTime</span><span class="sxs-lookup"><span data-stu-id="3c0b6-219">lastUpdatedTime</span></span> | <span data-ttu-id="3c0b6-220">Heure de la dernière mise à jour de l’alerte sur le système arrière.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-220">Time when alert was last updated at the backend.</span></span> | <span data-ttu-id="3c0b6-221">2020-09-06T14:46:57.2433333Z</span><span class="sxs-lookup"><span data-stu-id="3c0b6-221">2020-09-06T14:46:57.2433333Z</span></span>
<span data-ttu-id="3c0b6-222">resolvedTime</span><span class="sxs-lookup"><span data-stu-id="3c0b6-222">resolvedTime</span></span> | <span data-ttu-id="3c0b6-223">Heure de résolution de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-223">Time when alert was resolved.</span></span> | <span data-ttu-id="3c0b6-224">2020-09-10T05:22:59Z</span><span class="sxs-lookup"><span data-stu-id="3c0b6-224">2020-09-10T05:22:59Z</span></span>
<span data-ttu-id="3c0b6-225">firstActivity</span><span class="sxs-lookup"><span data-stu-id="3c0b6-225">firstActivity</span></span> | <span data-ttu-id="3c0b6-226">Heure à partir de la première alerte signalé que l’activité a été mise à jour sur le système back-end.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-226">Time when alert first reported that activity was updated at the backend.</span></span>| <span data-ttu-id="3c0b6-227">2020-09-04T05:22:59Z</span><span class="sxs-lookup"><span data-stu-id="3c0b6-227">2020-09-04T05:22:59Z</span></span>
<span data-ttu-id="3c0b6-228">titre</span><span class="sxs-lookup"><span data-stu-id="3c0b6-228">title</span></span> | <span data-ttu-id="3c0b6-229">Brève identification de la valeur de chaîne disponible pour chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-229">Brief identifying string value available for each alert.</span></span> | <span data-ttu-id="3c0b6-230">Activité de rançongiciel</span><span class="sxs-lookup"><span data-stu-id="3c0b6-230">Ransomware activity</span></span>
<span data-ttu-id="3c0b6-231">description</span><span class="sxs-lookup"><span data-stu-id="3c0b6-231">description</span></span> | <span data-ttu-id="3c0b6-232">Valeur de chaîne décrivant chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-232">String value describing each alert.</span></span> | <span data-ttu-id="3c0b6-233">L’utilisateur Test User2 (testUser2@contoso.com) a manipulé 99 fichiers avec plusieurs extensions se terminant par l’extension *rare herunterladen*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-233">The user Test User2 (testUser2@contoso.com) manipulated 99 files with multiple extensions ending with the uncommon extension *herunterladen*.</span></span> <span data-ttu-id="3c0b6-234">Il s’agit d’un nombre inhabituel de manipulations de fichiers et qui indique une attaque potentielle par ransomware.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-234">This is an unusual number of file manipulations and is indicative of a potential ransomware attack.</span></span>
<span data-ttu-id="3c0b6-235">category</span><span class="sxs-lookup"><span data-stu-id="3c0b6-235">category</span></span> | <span data-ttu-id="3c0b6-236">Affichage visuel et numérique de la progression de l’attaque tout au long de la chaîne d’attaque.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-236">Visual and numeric view of how far the attack has progressed along the kill chain.</span></span> <span data-ttu-id="3c0b6-237">Aligné sur l’infrastructure [CK&ATT MITRE™.](https://attack.mitre.org/)</span><span class="sxs-lookup"><span data-stu-id="3c0b6-237">Aligned to the [MITRE ATT&CK™ framework](https://attack.mitre.org/).</span></span> | <span data-ttu-id="3c0b6-238">Impact</span><span class="sxs-lookup"><span data-stu-id="3c0b6-238">Impact</span></span>
<span data-ttu-id="3c0b6-239">status</span><span class="sxs-lookup"><span data-stu-id="3c0b6-239">status</span></span> | <span data-ttu-id="3c0b6-240">Catégoriser les alertes *(en tant* que Nouveau, *Actif* *ou Résolu).*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-240">Categorize alerts (as *New*, *Active*, or *Resolved*).</span></span> <span data-ttu-id="3c0b6-241">Il peut vous aider à organiser et à gérer votre réponse aux alertes.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-241">It can help you organize and manage your response to alerts.</span></span> | <span data-ttu-id="3c0b6-242">Nouveau</span><span class="sxs-lookup"><span data-stu-id="3c0b6-242">New</span></span>
<span data-ttu-id="3c0b6-243">Sévérité </span><span class="sxs-lookup"><span data-stu-id="3c0b6-243">severity</span></span> | <span data-ttu-id="3c0b6-244">Indique l’impact possible sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-244">Indicates the possible impact on assets.</span></span> <span data-ttu-id="3c0b6-245">Plus la gravité est élevée, plus l’impact est important.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-245">The higher the severity the bigger the impact.</span></span> <span data-ttu-id="3c0b6-246">En règle générale, les éléments de gravité plus élevée nécessitent l’attention la plus immédiate.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-246">Typically higher severity items require the most immediate attention.</span></span><br><span data-ttu-id="3c0b6-247">Une des valeurs suivantes *: Informational,* \*Low,\*\*Medium et *High*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-247">One of the following values: *Informational*, *Low*, \*Medium, and *High*.</span></span> | <span data-ttu-id="3c0b6-248">Moyenne</span><span class="sxs-lookup"><span data-stu-id="3c0b6-248">Medium</span></span>
<span data-ttu-id="3c0b6-249">investigationId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-249">investigationId</span></span> | <span data-ttu-id="3c0b6-250">ID d’examen automatisé déclenché par cette alerte.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-250">The automated investigation ID triggered by this alert.</span></span> | <span data-ttu-id="3c0b6-251">1234</span><span class="sxs-lookup"><span data-stu-id="3c0b6-251">1234</span></span>
<span data-ttu-id="3c0b6-252">investigationState</span><span class="sxs-lookup"><span data-stu-id="3c0b6-252">investigationState</span></span> | <span data-ttu-id="3c0b6-253">Informations sur l’état actuel de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-253">Information on the investigation's current status.</span></span> <span data-ttu-id="3c0b6-254">L’une des valeurs suivantes : *Unknown*, *Terminated*, *SuccessfullyRemediated*, *Suppressed*, *Failed*, *PartiallyRemediated*, *Running*, *PendingApproval*, *PendingResource*, *PartiallyMediaigated*, *TerminatedByUser*, *TerminatedBySystem*, *Queued*, *InnerFailure*, *PreexistingAlert*, *UnsupportedOs*, *UnsupportedAlertType*, *SuppressedAlert*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-254">One of the following values: *Unknown*, *Terminated*, *SuccessfullyRemediated*, *Benign*, *Failed*, *PartiallyRemediated*, *Running*, *PendingApproval*, *PendingResource*, *PartiallyInvestigated*, *TerminatedByUser*, *TerminatedBySystem*, *Queued*, *InnerFailure*, *PreexistingAlert*, *UnsupportedOs*, *UnsupportedAlertType*, *SuppressedAlert*.</span></span> | <span data-ttu-id="3c0b6-255">UnsupportedAlertType</span><span class="sxs-lookup"><span data-stu-id="3c0b6-255">UnsupportedAlertType</span></span>
<span data-ttu-id="3c0b6-256">classification</span><span class="sxs-lookup"><span data-stu-id="3c0b6-256">classification</span></span> | <span data-ttu-id="3c0b6-257">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-257">The specification for the incident.</span></span> <span data-ttu-id="3c0b6-258">Les valeurs de propriété *sont : Unknown*, *FalsePositive*, *TruePositive* ou *null*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-258">The property values are: *Unknown*, *FalsePositive*, *TruePositive*, or *null*</span></span> | <span data-ttu-id="3c0b6-259">Inconnu</span><span class="sxs-lookup"><span data-stu-id="3c0b6-259">Unknown</span></span>
<span data-ttu-id="3c0b6-260">détermination</span><span class="sxs-lookup"><span data-stu-id="3c0b6-260">determination</span></span> | <span data-ttu-id="3c0b6-261">Spécifie la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-261">Specifies the determination of the incident.</span></span> <span data-ttu-id="3c0b6-262">Les valeurs de propriété sont *: NotAvailable*, *Apt*, *Malware*, SecurityPersonnel , *SecurityTesting*, *UnwantedSoftware*, *Other* ou *null* </span><span class="sxs-lookup"><span data-stu-id="3c0b6-262">The property values are: *NotAvailable*, *Apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *Other* or  *null*</span></span> | <span data-ttu-id="3c0b6-263">Apt</span><span class="sxs-lookup"><span data-stu-id="3c0b6-263">Apt</span></span>
<span data-ttu-id="3c0b6-264">assignedTo</span><span class="sxs-lookup"><span data-stu-id="3c0b6-264">assignedTo</span></span> | <span data-ttu-id="3c0b6-265">Propriétaire de l’incident ou *null* si aucun propriétaire n’est affecté.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-265">Owner of the incident, or *null* if no owner is assigned.</span></span> | <span data-ttu-id="3c0b6-266">secop2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="3c0b6-266">secop2@contoso.com</span></span>
<span data-ttu-id="3c0b6-267">actorName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-267">actorName</span></span> | <span data-ttu-id="3c0b6-268">Le groupe d’activités, le caser, l’associé à cette alerte.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-268">The activity group, if any, the  associated with this alert.</span></span> | <span data-ttu-id="3c0b6-269">BORON</span><span class="sxs-lookup"><span data-stu-id="3c0b6-269">BORON</span></span>
<span data-ttu-id="3c0b6-270">threatFamilyName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-270">threatFamilyName</span></span> | <span data-ttu-id="3c0b6-271">Famille de menaces associée à cette alerte.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-271">Threat family associated with this alert.</span></span> | <span data-ttu-id="3c0b6-272">null</span><span class="sxs-lookup"><span data-stu-id="3c0b6-272">null</span></span>
<span data-ttu-id="3c0b6-273">mitreTechniques</span><span class="sxs-lookup"><span data-stu-id="3c0b6-273">mitreTechniques</span></span> | <span data-ttu-id="3c0b6-274">Les techniques d’attaque, telles qu’alignées avec l’infrastructure&[CK ™ MITRE ATT.](https://attack.mitre.org/)</span><span class="sxs-lookup"><span data-stu-id="3c0b6-274">The attack techniques, as aligned with the [MITRE ATT&CK](https://attack.mitre.org/)™ framework.</span></span> | \[\]
<span data-ttu-id="3c0b6-275">appareils</span><span class="sxs-lookup"><span data-stu-id="3c0b6-275">devices</span></span> | <span data-ttu-id="3c0b6-276">Tous les appareils sur lequel des alertes liées à l’incident ont été envoyées.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-276">All devices where alerts related to the incident were sent.</span></span> | <span data-ttu-id="3c0b6-277">\[\] (voir les détails sur les champs d’entité ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="3c0b6-277">\[\] (see details on entity fields below)</span></span>

### <a name="device-format"></a><span data-ttu-id="3c0b6-278">Format de l’appareil</span><span class="sxs-lookup"><span data-stu-id="3c0b6-278">Device format</span></span>

<span data-ttu-id="3c0b6-279">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="3c0b6-279">Field name</span></span> | <span data-ttu-id="3c0b6-280">Description</span><span class="sxs-lookup"><span data-stu-id="3c0b6-280">Description</span></span> | <span data-ttu-id="3c0b6-281">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="3c0b6-281">Example value</span></span>
-|-|-
<span data-ttu-id="3c0b6-282">DeviceId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-282">DeviceId</span></span> | <span data-ttu-id="3c0b6-283">ID d’appareil désigné dans Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-283">The device ID as designated in Microsoft Defender for Endpoint.</span></span> | <span data-ttu-id="3c0b6-284">24c222b0b60fe148eeece49ac83910cc6a7ef491</span><span class="sxs-lookup"><span data-stu-id="3c0b6-284">24c222b0b60fe148eeece49ac83910cc6a7ef491</span></span>
<span data-ttu-id="3c0b6-285">aadDeviceId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-285">aadDeviceId</span></span> |  <span data-ttu-id="3c0b6-286">ID de l’appareil tel que désigné dans [Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis).</span><span class="sxs-lookup"><span data-stu-id="3c0b6-286">The device ID as designated in [Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis).</span></span> <span data-ttu-id="3c0b6-287">Disponible uniquement pour les appareils joints au domaine.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-287">Only available for domain-joined devices.</span></span> | <span data-ttu-id="3c0b6-288">null</span><span class="sxs-lookup"><span data-stu-id="3c0b6-288">null</span></span>
<span data-ttu-id="3c0b6-289">deviceDnsName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-289">deviceDnsName</span></span> | <span data-ttu-id="3c0b6-290">Nom de domaine complet de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-290">The fully qualified domain name for the device.</span></span> | <span data-ttu-id="3c0b6-291">user5cx.middleeast.corp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3c0b6-291">user5cx.middleeast.corp.contoso.com</span></span>
<span data-ttu-id="3c0b6-292">osPlatform</span><span class="sxs-lookup"><span data-stu-id="3c0b6-292">osPlatform</span></span> | <span data-ttu-id="3c0b6-293">Plateforme du système d’exploitation que l’appareil exécute.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-293">The OS platform the device is running.</span></span>| <span data-ttu-id="3c0b6-294">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="3c0b6-294">WindowsServer2016</span></span>
<span data-ttu-id="3c0b6-295">osBuild</span><span class="sxs-lookup"><span data-stu-id="3c0b6-295">osBuild</span></span> | <span data-ttu-id="3c0b6-296">Version de build du système d’exploitation que l’appareil exécute.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-296">The build version for the OS the device is running.</span></span> | <span data-ttu-id="3c0b6-297">14393</span><span class="sxs-lookup"><span data-stu-id="3c0b6-297">14393</span></span>
<span data-ttu-id="3c0b6-298">rbacGroupName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-298">rbacGroupName</span></span> | <span data-ttu-id="3c0b6-299">Groupe [de contrôle d’accès](/azure/role-based-access-control/overview) basé sur un rôle (RBAC) associé à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-299">The [role-based access control](/azure/role-based-access-control/overview) (RBAC) group associated with the device.</span></span> | <span data-ttu-id="3c0b6-300">WDATP-Ring0</span><span class="sxs-lookup"><span data-stu-id="3c0b6-300">WDATP-Ring0</span></span>
<span data-ttu-id="3c0b6-301">firstSeen</span><span class="sxs-lookup"><span data-stu-id="3c0b6-301">firstSeen</span></span> | <span data-ttu-id="3c0b6-302">Heure de la première fois où l’appareil a été vu.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-302">Time when device was first seen.</span></span> | <span data-ttu-id="3c0b6-303">2020-02-06T14:16:01.9330135Z</span><span class="sxs-lookup"><span data-stu-id="3c0b6-303">2020-02-06T14:16:01.9330135Z</span></span>
<span data-ttu-id="3c0b6-304">healthStatus</span><span class="sxs-lookup"><span data-stu-id="3c0b6-304">healthStatus</span></span> | <span data-ttu-id="3c0b6-305">État d’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-305">The health state of the device.</span></span> | <span data-ttu-id="3c0b6-306">Actif</span><span class="sxs-lookup"><span data-stu-id="3c0b6-306">Active</span></span>
<span data-ttu-id="3c0b6-307">riskScore</span><span class="sxs-lookup"><span data-stu-id="3c0b6-307">riskScore</span></span> | <span data-ttu-id="3c0b6-308">Score de risque pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-308">The risk score for the  device.</span></span> | <span data-ttu-id="3c0b6-309">Élevé</span><span class="sxs-lookup"><span data-stu-id="3c0b6-309">High</span></span>
<span data-ttu-id="3c0b6-310">entities</span><span class="sxs-lookup"><span data-stu-id="3c0b6-310">entities</span></span> | <span data-ttu-id="3c0b6-311">Toutes les entités qui ont été identifiées comme faisant partie ou associées à une alerte donnée.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-311">All entities that have been identified to be part of, or related to, a given alert.</span></span> | <span data-ttu-id="3c0b6-312">\[\] (voir les détails sur les champs d’entité ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="3c0b6-312">\[\] (see details on entity fields below)</span></span>

### <a name="entity-format"></a><span data-ttu-id="3c0b6-313">Format d’entité</span><span class="sxs-lookup"><span data-stu-id="3c0b6-313">Entity Format</span></span>

<span data-ttu-id="3c0b6-314">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="3c0b6-314">Field name</span></span> | <span data-ttu-id="3c0b6-315">Description</span><span class="sxs-lookup"><span data-stu-id="3c0b6-315">Description</span></span> | <span data-ttu-id="3c0b6-316">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="3c0b6-316">Example value</span></span>
-|-|-
<span data-ttu-id="3c0b6-317">entityType</span><span class="sxs-lookup"><span data-stu-id="3c0b6-317">entityType</span></span> | <span data-ttu-id="3c0b6-318">Entités identifiées comme faisant partie d’une alerte donnée ou associées à celle-là.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-318">Entities that have been identified to be part of, or related to, a given alert.</span></span><br><span data-ttu-id="3c0b6-319">Les valeurs des propriétés sont *: User*, *Ip*, *Url*, *File*, *Process*, *MailBox*, *MailMessage*, *MailCluster*, *Registry*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-319">The properties values are: *User*, *Ip*, *Url*, *File*, *Process*, *MailBox*, *MailMessage*, *MailCluster*, *Registry*</span></span> | <span data-ttu-id="3c0b6-320">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="3c0b6-320">User</span></span>
<span data-ttu-id="3c0b6-321">sha1</span><span class="sxs-lookup"><span data-stu-id="3c0b6-321">sha1</span></span> | <span data-ttu-id="3c0b6-322">Disponible si entityType est *File*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-322">Available if entityType is *File*.</span></span><br><span data-ttu-id="3c0b6-323">Hachage du fichier pour les alertes associées à un fichier ou un processus.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-323">The file hash for alerts associated with a file or process.</span></span> | <span data-ttu-id="3c0b6-324">5de839186691aa96ee2ca6d74f0a38fb8d1bd6dd</span><span class="sxs-lookup"><span data-stu-id="3c0b6-324">5de839186691aa96ee2ca6d74f0a38fb8d1bd6dd</span></span>
<span data-ttu-id="3c0b6-325">sha256</span><span class="sxs-lookup"><span data-stu-id="3c0b6-325">sha256</span></span> | <span data-ttu-id="3c0b6-326">Disponible si entityType est *File*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-326">Available if entityType is *File*.</span></span><br><span data-ttu-id="3c0b6-327">Hachage du fichier pour les alertes associées à un fichier ou un processus.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-327">The file hash for alerts associated with a file or process.</span></span> | <span data-ttu-id="3c0b6-328">28cb017dfc99073aa1b47c1b30f413e3ce774c4991eb4158de50f9dbb36d8043</span><span class="sxs-lookup"><span data-stu-id="3c0b6-328">28cb017dfc99073aa1b47c1b30f413e3ce774c4991eb4158de50f9dbb36d8043</span></span>
<span data-ttu-id="3c0b6-329">fileName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-329">fileName</span></span> | <span data-ttu-id="3c0b6-330">Disponible si entityType est *File*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-330">Available if entityType is *File*.</span></span><br><span data-ttu-id="3c0b6-331">Nom de fichier des alertes associées à un fichier ou un processus</span><span class="sxs-lookup"><span data-stu-id="3c0b6-331">The file name for alerts associated with a file or process</span></span> | <span data-ttu-id="3c0b6-332">Detector.UnitTests.dll</span><span class="sxs-lookup"><span data-stu-id="3c0b6-332">Detector.UnitTests.dll</span></span>
<span data-ttu-id="3c0b6-333">filePath</span><span class="sxs-lookup"><span data-stu-id="3c0b6-333">filePath</span></span> | <span data-ttu-id="3c0b6-334">Disponible si entityType est *File*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-334">Available if entityType is *File*.</span></span><br><span data-ttu-id="3c0b6-335">Chemin d’accès au fichier pour les alertes associées à un fichier ou un processus</span><span class="sxs-lookup"><span data-stu-id="3c0b6-335">The file path for alerts associated with a file or process</span></span> | <span data-ttu-id="3c0b6-336">C : \\ \agent_work_temp\Deploy\SYSTEM\2020-09-06 12_14_54\Out</span><span class="sxs-lookup"><span data-stu-id="3c0b6-336">C:\\\agent_work_temp\Deploy\SYSTEM\2020-09-06 12_14_54\Out</span></span>
<span data-ttu-id="3c0b6-337">processId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-337">processId</span></span> | <span data-ttu-id="3c0b6-338">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-338">Available if entityType is *Process*.</span></span> | <span data-ttu-id="3c0b6-339">24348</span><span class="sxs-lookup"><span data-stu-id="3c0b6-339">24348</span></span>
<span data-ttu-id="3c0b6-340">processCommandLine</span><span class="sxs-lookup"><span data-stu-id="3c0b6-340">processCommandLine</span></span> | <span data-ttu-id="3c0b6-341">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-341">Available if entityType is *Process*.</span></span> | <span data-ttu-id="3c0b6-342">« Votre fichier est prêt à être téléchargé \_1911150169.exe »</span><span class="sxs-lookup"><span data-stu-id="3c0b6-342">"Your File Is Ready To Download\_1911150169.exe"</span></span>
<span data-ttu-id="3c0b6-343">processCreationTime</span><span class="sxs-lookup"><span data-stu-id="3c0b6-343">processCreationTime</span></span> | <span data-ttu-id="3c0b6-344">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-344">Available if entityType is *Process*.</span></span> | <span data-ttu-id="3c0b6-345">2020-07-18T03:25:38.5269993Z</span><span class="sxs-lookup"><span data-stu-id="3c0b6-345">2020-07-18T03:25:38.5269993Z</span></span>
<span data-ttu-id="3c0b6-346">parentProcessId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-346">parentProcessId</span></span> | <span data-ttu-id="3c0b6-347">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-347">Available if entityType is *Process*.</span></span> | <span data-ttu-id="3c0b6-348">16840</span><span class="sxs-lookup"><span data-stu-id="3c0b6-348">16840</span></span>
<span data-ttu-id="3c0b6-349">parentProcessCreationTime</span><span class="sxs-lookup"><span data-stu-id="3c0b6-349">parentProcessCreationTime</span></span> | <span data-ttu-id="3c0b6-350">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-350">Available if entityType is *Process*.</span></span> | <span data-ttu-id="3c0b6-351">2020-07-18T02:12:32.8616797Z</span><span class="sxs-lookup"><span data-stu-id="3c0b6-351">2020-07-18T02:12:32.8616797Z</span></span>
<span data-ttu-id="3c0b6-352">ipAddress</span><span class="sxs-lookup"><span data-stu-id="3c0b6-352">ipAddress</span></span> | <span data-ttu-id="3c0b6-353">Disponible si entityType est *Ip*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-353">Available if entityType is *Ip*.</span></span> <br><span data-ttu-id="3c0b6-354">Adresse IP des alertes associées aux événements réseau, telles que la communication vers *une destination réseau malveillante.*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-354">IP address for alerts associated with network events, such as *Communication to a malicious network destination*.</span></span> | <span data-ttu-id="3c0b6-355">62.216.203.204</span><span class="sxs-lookup"><span data-stu-id="3c0b6-355">62.216.203.204</span></span>
<span data-ttu-id="3c0b6-356">url</span><span class="sxs-lookup"><span data-stu-id="3c0b6-356">url</span></span> | <span data-ttu-id="3c0b6-357">Disponible si entityType est *l’URL*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-357">Available if entityType is *Url*.</span></span> <br><span data-ttu-id="3c0b6-358">URL des alertes associées aux événements réseau, telles que la communication avec *une destination réseau malveillante.*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-358">Url for alerts associated to network events, such as, *Communication to a malicious network destination*.</span></span> | <span data-ttu-id="3c0b6-359">down.esales360.cn</span><span class="sxs-lookup"><span data-stu-id="3c0b6-359">down.esales360.cn</span></span>
<span data-ttu-id="3c0b6-360">accountName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-360">accountName</span></span> | <span data-ttu-id="3c0b6-361">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-361">Available if entityType is *User*.</span></span> | <span data-ttu-id="3c0b6-362">testUser2</span><span class="sxs-lookup"><span data-stu-id="3c0b6-362">testUser2</span></span>
<span data-ttu-id="3c0b6-363">domainName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-363">domainName</span></span> | <span data-ttu-id="3c0b6-364">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-364">Available if entityType is *User*.</span></span> | <span data-ttu-id="3c0b6-365">europe.corp.contoso</span><span class="sxs-lookup"><span data-stu-id="3c0b6-365">europe.corp.contoso</span></span>
<span data-ttu-id="3c0b6-366">userSid</span><span class="sxs-lookup"><span data-stu-id="3c0b6-366">userSid</span></span> | <span data-ttu-id="3c0b6-367">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-367">Available if entityType is *User*.</span></span> | <span data-ttu-id="3c0b6-368">S-1-5-21-1721254763-462695806-1538882281-4156657</span><span class="sxs-lookup"><span data-stu-id="3c0b6-368">S-1-5-21-1721254763-462695806-1538882281-4156657</span></span>
<span data-ttu-id="3c0b6-369">aadUserId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-369">aadUserId</span></span> | <span data-ttu-id="3c0b6-370">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-370">Available if entityType is *User*.</span></span> | <span data-ttu-id="3c0b6-371">fc8f7484-f813-4db2-afab-bc1507913fb6</span><span class="sxs-lookup"><span data-stu-id="3c0b6-371">fc8f7484-f813-4db2-afab-bc1507913fb6</span></span>
<span data-ttu-id="3c0b6-372">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-372">userPrincipalName</span></span> | <span data-ttu-id="3c0b6-373">Disponible si entityType est *User* / *MailBox* / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-373">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span> | <span data-ttu-id="3c0b6-374">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="3c0b6-374">testUser2@contoso.com</span></span>
<span data-ttu-id="3c0b6-375">mailboxDisplayName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-375">mailboxDisplayName</span></span> | <span data-ttu-id="3c0b6-376">Disponible si entityType est *MailBox*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-376">Available if entityType is *MailBox*.</span></span> | <span data-ttu-id="3c0b6-377">test User2</span><span class="sxs-lookup"><span data-stu-id="3c0b6-377">test User2</span></span>
<span data-ttu-id="3c0b6-378">mailboxAddress</span><span class="sxs-lookup"><span data-stu-id="3c0b6-378">mailboxAddress</span></span> | <span data-ttu-id="3c0b6-379">Disponible si entityType est *User* / *MailBox* / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-379">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span> | <span data-ttu-id="3c0b6-380">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="3c0b6-380">testUser2@contoso.com</span></span>
<span data-ttu-id="3c0b6-381">clusterBy</span><span class="sxs-lookup"><span data-stu-id="3c0b6-381">clusterBy</span></span> | <span data-ttu-id="3c0b6-382">Disponible si entityType est  *MailCluster*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-382">Available if entityType is  *MailCluster*.</span></span> | <span data-ttu-id="3c0b6-383">Objet ; P2SenderDomain; ContentType</span><span class="sxs-lookup"><span data-stu-id="3c0b6-383">Subject;P2SenderDomain;ContentType</span></span>
<span data-ttu-id="3c0b6-384">expéditeur</span><span class="sxs-lookup"><span data-stu-id="3c0b6-384">sender</span></span> | <span data-ttu-id="3c0b6-385">Disponible si entityType est *User* / *MailBox* / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-385">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span> | <span data-ttu-id="3c0b6-386">user.abc@mail.contoso.co.in</span><span class="sxs-lookup"><span data-stu-id="3c0b6-386">user.abc@mail.contoso.co.in</span></span>
<span data-ttu-id="3c0b6-387">destinataire</span><span class="sxs-lookup"><span data-stu-id="3c0b6-387">recipient</span></span> | <span data-ttu-id="3c0b6-388">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-388">Available if entityType is *MailMessage*.</span></span> | <span data-ttu-id="3c0b6-389">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="3c0b6-389">testUser2@contoso.com</span></span>
<span data-ttu-id="3c0b6-390">subject</span><span class="sxs-lookup"><span data-stu-id="3c0b6-390">subject</span></span> | <span data-ttu-id="3c0b6-391">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-391">Available if entityType is *MailMessage*.</span></span> | <span data-ttu-id="3c0b6-392">\[Attention \] externe</span><span class="sxs-lookup"><span data-stu-id="3c0b6-392">\[EXTERNAL\] Attention</span></span>
<span data-ttu-id="3c0b6-393">deliveryAction</span><span class="sxs-lookup"><span data-stu-id="3c0b6-393">deliveryAction</span></span> | <span data-ttu-id="3c0b6-394">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-394">Available if entityType is *MailMessage*.</span></span> | <span data-ttu-id="3c0b6-395">Remis</span><span class="sxs-lookup"><span data-stu-id="3c0b6-395">Delivered</span></span>
<span data-ttu-id="3c0b6-396">securityGroupId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-396">securityGroupId</span></span> | <span data-ttu-id="3c0b6-397">Disponible si entityType est  *SecurityGroup*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-397">Available if entityType is  *SecurityGroup*.</span></span> | <span data-ttu-id="3c0b6-398">301c47c8-e15f-4059-ab09-e2ba9ffd372b</span><span class="sxs-lookup"><span data-stu-id="3c0b6-398">301c47c8-e15f-4059-ab09-e2ba9ffd372b</span></span>
<span data-ttu-id="3c0b6-399">securityGroupName</span><span class="sxs-lookup"><span data-stu-id="3c0b6-399">securityGroupName</span></span> | <span data-ttu-id="3c0b6-400">Disponible si entityType est  *SecurityGroup*.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-400">Available if entityType is  *SecurityGroup*.</span></span> | <span data-ttu-id="3c0b6-401">Opérateurs de configuration réseau</span><span class="sxs-lookup"><span data-stu-id="3c0b6-401">Network Configuration Operators</span></span>
<span data-ttu-id="3c0b6-402">registryHive</span><span class="sxs-lookup"><span data-stu-id="3c0b6-402">registryHive</span></span> | <span data-ttu-id="3c0b6-403">Disponible si entityType est *dans le Registre.*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-403">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="3c0b6-404">ORDINATEUR LOCAL HKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="3c0b6-404">HKEY\_LOCAL\_MACHINE</span></span> |
<span data-ttu-id="3c0b6-405">registryKey</span><span class="sxs-lookup"><span data-stu-id="3c0b6-405">registryKey</span></span> | <span data-ttu-id="3c0b6-406">Disponible si entityType est *dans le Registre.*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-406">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="3c0b6-407">SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon</span><span class="sxs-lookup"><span data-stu-id="3c0b6-407">SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon</span></span>
<span data-ttu-id="3c0b6-408">registryValueType</span><span class="sxs-lookup"><span data-stu-id="3c0b6-408">registryValueType</span></span> | <span data-ttu-id="3c0b6-409">Disponible si entityType est *dans le Registre.*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-409">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="3c0b6-410">String</span><span class="sxs-lookup"><span data-stu-id="3c0b6-410">String</span></span>
<span data-ttu-id="3c0b6-411">registryValue</span><span class="sxs-lookup"><span data-stu-id="3c0b6-411">registryValue</span></span> | <span data-ttu-id="3c0b6-412">Disponible si entityType est *dans le Registre.*</span><span class="sxs-lookup"><span data-stu-id="3c0b6-412">Available if entityType is  *Registry*.</span></span> | <span data-ttu-id="3c0b6-413">31-00-00-00</span><span class="sxs-lookup"><span data-stu-id="3c0b6-413">31-00-00-00</span></span>
<span data-ttu-id="3c0b6-414">deviceId</span><span class="sxs-lookup"><span data-stu-id="3c0b6-414">deviceId</span></span> | <span data-ttu-id="3c0b6-415">ID, le caser, de l’appareil lié à l’entité.</span><span class="sxs-lookup"><span data-stu-id="3c0b6-415">The ID, if any, of the device related to the entity.</span></span> | <span data-ttu-id="3c0b6-416">986e5df8b73dacd43c8917d17e523e76b13c75cd</span><span class="sxs-lookup"><span data-stu-id="3c0b6-416">986e5df8b73dacd43c8917d17e523e76b13c75cd</span></span>

## <a name="example"></a><span data-ttu-id="3c0b6-417">Exemple</span><span class="sxs-lookup"><span data-stu-id="3c0b6-417">Example</span></span>

<span data-ttu-id="3c0b6-418">**Demande**</span><span class="sxs-lookup"><span data-stu-id="3c0b6-418">**Request**</span></span>

```HTTP
GET https://api.security.microsoft.com/api/incidents
```

<span data-ttu-id="3c0b6-419">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="3c0b6-419">**Response**</span></span>

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
            "comments": [
                {
                    "comment": "test comment for docs",
                    "createdBy": "secop123@contoso.com",
                    "createdTime": "2021-01-26T01:00:37.8404534Z"
                }
            ],
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
            "comments": [],
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
            "comments": [],
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

## <a name="related-articles"></a><span data-ttu-id="3c0b6-420">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="3c0b6-420">Related articles</span></span>

- [<span data-ttu-id="3c0b6-421">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3c0b6-421">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="3c0b6-422">En savoir plus sur les limites d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="3c0b6-422">Learn about API limits and licensing</span></span>](api-terms.md)
- [<span data-ttu-id="3c0b6-423">Comprendre les codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3c0b6-423">Understand error codes</span></span>](api-error-codes.md)
- [<span data-ttu-id="3c0b6-424">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="3c0b6-424">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="3c0b6-425">API d’incident</span><span class="sxs-lookup"><span data-stu-id="3c0b6-425">Incident APIs</span></span>](api-incident.md)
- [<span data-ttu-id="3c0b6-426">API de mise à jour de l’incident</span><span class="sxs-lookup"><span data-stu-id="3c0b6-426">Update incident API</span></span>](api-update-incidents.md)
