---
title: API de liste des incidents dans la protection de Microsoft contre les menaces
description: Découvrez comment répertorier les API incidents dans Microsoft Threat Protection
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
ms.openlocfilehash: 9defc9c0f8fa04e019c0108ca0f4111de54edb5f
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48195393"
---
# <a name="list-incidents-api-in-microsoft-threat-protection"></a><span data-ttu-id="0eb37-104">API de liste des incidents dans la protection de Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0eb37-104">List incidents API in Microsoft Threat Protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="0eb37-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0eb37-105">**Applies to:**</span></span>

- <span data-ttu-id="0eb37-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0eb37-106">Microsoft Threat Protection</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0eb37-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="0eb37-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0eb37-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="0eb37-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


## <a name="api-description"></a><span data-ttu-id="0eb37-109">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="0eb37-109">API description</span></span>

<span data-ttu-id="0eb37-110">L’API incident vous permet d’effectuer un tri dans les incidents afin de hiérarchiser et de créer une réponse Cybersecurity informée.</span><span class="sxs-lookup"><span data-stu-id="0eb37-110">The Incident API allows you to sort through incidents to prioritize and create an informed cybersecurity response.</span></span> <span data-ttu-id="0eb37-111">Il expose une collection d’incidents marqués à partir des appareils, des comptes de messagerie et des utilisateurs de votre réseau, dans la plage de temps que vous avez spécifiée dans la stratégie de rétention de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0eb37-111">It exposes a collection of incidents that were flagged from devices, email accounts, and users in your network, within the time range you specified in your environment retention policy.</span></span> <span data-ttu-id="0eb37-112">Les incidents les plus récents sont affichés en haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="0eb37-112">The most recent incidents are displayed at the top of the list.</span></span> <span data-ttu-id="0eb37-113">Chaque incident contient un tableau des alertes associées et de leurs entités associées.</span><span class="sxs-lookup"><span data-stu-id="0eb37-113">Each incident contains an array of related alerts, and their related entities.</span></span>

<br><span data-ttu-id="0eb37-114">L’API prend en charge les opérateurs **OData** suivants :</span><span class="sxs-lookup"><span data-stu-id="0eb37-114">The API supports the following **OData** operators:</span></span>
<br><span data-ttu-id="0eb37-115">```$filter``` activé : ```lastUpdateTime``` , ```createdTime``` ```status``` et ```assignedTo``` Propriétés.</span><span class="sxs-lookup"><span data-stu-id="0eb37-115">```$filter``` on: ```lastUpdateTime```, ```createdTime```, ```status``` and ```assignedTo``` properties.</span></span>
<br><span data-ttu-id="0eb37-116">```$top``` avec une valeur maximale de **100**</span><span class="sxs-lookup"><span data-stu-id="0eb37-116">```$top``` with max value of **100**</span></span>
<br>```$skip```

## <a name="limitations"></a><span data-ttu-id="0eb37-117">Limites</span><span class="sxs-lookup"><span data-stu-id="0eb37-117">Limitations</span></span>

1. <span data-ttu-id="0eb37-118">La taille de page maximale est de **100 incidents**.</span><span class="sxs-lookup"><span data-stu-id="0eb37-118">Maximum page size is **100 incidents**.</span></span>
2. <span data-ttu-id="0eb37-119">Le taux maximal de demandes est de **50 appels par minute** et **1500 appels par heure**.</span><span class="sxs-lookup"><span data-stu-id="0eb37-119">Maximum rate of requests is **50 calls per minute** and **1500 calls per hour**.</span></span>

## <a name="permissions"></a><span data-ttu-id="0eb37-120">Autorisations</span><span class="sxs-lookup"><span data-stu-id="0eb37-120">Permissions</span></span>

<span data-ttu-id="0eb37-121">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="0eb37-121">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="0eb37-122">Pour plus d’informations, notamment sur le choix des autorisations, consultez la rubrique [Access Microsoft Threat Protection APIs](api-access.md)</span><span class="sxs-lookup"><span data-stu-id="0eb37-122">To learn more, including how to choose permissions, see [Access Microsoft Threat Protection APIs](api-access.md)</span></span>

<span data-ttu-id="0eb37-123">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="0eb37-123">Permission type</span></span> |   <span data-ttu-id="0eb37-124">Autorisation</span><span class="sxs-lookup"><span data-stu-id="0eb37-124">Permission</span></span>  |   <span data-ttu-id="0eb37-125">Nom d’affichage des autorisations</span><span class="sxs-lookup"><span data-stu-id="0eb37-125">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="0eb37-126">Application</span><span class="sxs-lookup"><span data-stu-id="0eb37-126">Application</span></span> |   <span data-ttu-id="0eb37-127">Incident. Read. All</span><span class="sxs-lookup"><span data-stu-id="0eb37-127">Incident.Read.All</span></span> | <span data-ttu-id="0eb37-128">« Lire tous les incidents »</span><span class="sxs-lookup"><span data-stu-id="0eb37-128">'Read all incidents'</span></span>
<span data-ttu-id="0eb37-129">Application</span><span class="sxs-lookup"><span data-stu-id="0eb37-129">Application</span></span> |   <span data-ttu-id="0eb37-130">Incident. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="0eb37-130">Incident.ReadWrite.All</span></span> | <span data-ttu-id="0eb37-131">« Lire et écrire tous les incidents »</span><span class="sxs-lookup"><span data-stu-id="0eb37-131">'Read and write all incidents'</span></span>
<span data-ttu-id="0eb37-132">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="0eb37-132">Delegated (work or school account)</span></span> | <span data-ttu-id="0eb37-133">Incident. Read</span><span class="sxs-lookup"><span data-stu-id="0eb37-133">Incident.Read</span></span> | <span data-ttu-id="0eb37-134">« Incidents de lecture »</span><span class="sxs-lookup"><span data-stu-id="0eb37-134">'Read incidents'</span></span>
<span data-ttu-id="0eb37-135">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="0eb37-135">Delegated (work or school account)</span></span> | <span data-ttu-id="0eb37-136">Incident. ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0eb37-136">Incident.ReadWrite</span></span> | <span data-ttu-id="0eb37-137">« Incidents en lecture et en écriture »</span><span class="sxs-lookup"><span data-stu-id="0eb37-137">'Read and write incidents'</span></span>

> [!Note]
> <span data-ttu-id="0eb37-138">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0eb37-138">When obtaining a token using user credentials:</span></span>
> - <span data-ttu-id="0eb37-139">L’utilisateur doit disposer de l’autorisation Afficher pour les incidents dans le portail.</span><span class="sxs-lookup"><span data-stu-id="0eb37-139">The user needs to have view permission for incidents in the portal.</span></span>
> - <span data-ttu-id="0eb37-140">La réponse inclut uniquement les incidents auxquels l’utilisateur est exposé.</span><span class="sxs-lookup"><span data-stu-id="0eb37-140">The response will only include incidents that the user is exposed to.</span></span>

## <a name="http-request"></a><span data-ttu-id="0eb37-141">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="0eb37-141">HTTP request</span></span>

```
GET /api/incidents
```

## <a name="request-headers"></a><span data-ttu-id="0eb37-142">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="0eb37-142">Request headers</span></span>

<span data-ttu-id="0eb37-143">Nom</span><span class="sxs-lookup"><span data-stu-id="0eb37-143">Name</span></span> | <span data-ttu-id="0eb37-144">Type</span><span class="sxs-lookup"><span data-stu-id="0eb37-144">Type</span></span> | <span data-ttu-id="0eb37-145">Description</span><span class="sxs-lookup"><span data-stu-id="0eb37-145">Description</span></span>
:---|:---|:---
<span data-ttu-id="0eb37-146">Autorisation</span><span class="sxs-lookup"><span data-stu-id="0eb37-146">Authorization</span></span> | <span data-ttu-id="0eb37-147">String</span><span class="sxs-lookup"><span data-stu-id="0eb37-147">String</span></span> | <span data-ttu-id="0eb37-148">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="0eb37-148">Bearer {token}.</span></span> <span data-ttu-id="0eb37-149">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="0eb37-149">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="0eb37-150">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="0eb37-150">Request body</span></span>
<span data-ttu-id="0eb37-151">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0eb37-151">None.</span></span>

## <a name="response"></a><span data-ttu-id="0eb37-152">Réponse</span><span class="sxs-lookup"><span data-stu-id="0eb37-152">Response</span></span>
<span data-ttu-id="0eb37-153">Si elle réussit, cette méthode renvoie 200 OK et une liste d' [incidents](api-incident.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="0eb37-153">If successful, this method returns 200 OK, and a list of [incidents](api-incident.md) in the response body.</span></span>

## <a name="schema-mapping"></a><span data-ttu-id="0eb37-154">Mappage de schéma</span><span class="sxs-lookup"><span data-stu-id="0eb37-154">Schema mapping</span></span>

| <span data-ttu-id="0eb37-155">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="0eb37-155">Field name</span></span>                                | <span data-ttu-id="0eb37-156">Description</span><span class="sxs-lookup"><span data-stu-id="0eb37-156">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                | <span data-ttu-id="0eb37-157">Exemple de valeur</span><span class="sxs-lookup"><span data-stu-id="0eb37-157">Example value</span></span>                                                                                                                                                                                                                                     |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="0eb37-158">**Métadonnées d’incident**</span><span class="sxs-lookup"><span data-stu-id="0eb37-158">**Incident metadata**</span></span>                         |                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                   |
| <span data-ttu-id="0eb37-159">incidentId</span><span class="sxs-lookup"><span data-stu-id="0eb37-159">incidentId</span></span>                                | <span data-ttu-id="0eb37-160">Identificateur unique qui représente l’incident.</span><span class="sxs-lookup"><span data-stu-id="0eb37-160">Unique identifier to represent the incident.</span></span>                                                                                                                                                                                                                                                                                                                                                | <span data-ttu-id="0eb37-161">924565</span><span class="sxs-lookup"><span data-stu-id="0eb37-161">924565</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-162">redirectIncidentId</span><span class="sxs-lookup"><span data-stu-id="0eb37-162">redirectIncidentId</span></span>                        | <span data-ttu-id="0eb37-163">Renseigné uniquement si un incident est regroupé avec un autre incident, dans le cadre de la logique de traitement de l’incident.</span><span class="sxs-lookup"><span data-stu-id="0eb37-163">Only populated in case an incident is being grouped together with another incident, as part of the incident processing logic.</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="0eb37-164">924569</span><span class="sxs-lookup"><span data-stu-id="0eb37-164">924569</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-165">incidentName</span><span class="sxs-lookup"><span data-stu-id="0eb37-165">incidentName</span></span>                              | <span data-ttu-id="0eb37-166">Valeur de chaîne disponible pour chaque incident.</span><span class="sxs-lookup"><span data-stu-id="0eb37-166">String value available for every incident.</span></span>                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="0eb37-167">Activité ransomware</span><span class="sxs-lookup"><span data-stu-id="0eb37-167">Ransomware activity</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="0eb37-168">createdTime</span><span class="sxs-lookup"><span data-stu-id="0eb37-168">createdTime</span></span>                               | <span data-ttu-id="0eb37-169">Heure de la première création de l’incident.</span><span class="sxs-lookup"><span data-stu-id="0eb37-169">Time when incident was first created.</span></span>                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="0eb37-170">2020-09-06T14:46:57.0733333 Z</span><span class="sxs-lookup"><span data-stu-id="0eb37-170">2020-09-06T14:46:57.0733333Z</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="0eb37-171">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="0eb37-171">lastUpdateTime</span></span>                            | <span data-ttu-id="0eb37-172">Heure de la dernière mise à jour de l’incident sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="0eb37-172">Time when incident was last updated at the backend.</span></span><br> <span data-ttu-id="0eb37-173">Ce champ peut être utilisé lors de la définition du paramètre Request pour la plage de temps pendant laquelle les incidents sont récupérés.</span><span class="sxs-lookup"><span data-stu-id="0eb37-173">This field can be used when setting the request parameter for the range of time that incidents are retrieved.</span></span>                                                                                                                                                                                                                      | <span data-ttu-id="0eb37-174">2020-09-06T14:46:57.29 Z</span><span class="sxs-lookup"><span data-stu-id="0eb37-174">2020-09-06T14:46:57.29Z</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="0eb37-175">assignedTo</span><span class="sxs-lookup"><span data-stu-id="0eb37-175">assignedTo</span></span>                                | <span data-ttu-id="0eb37-176">Propriétaire de l’incident ou *valeur null* si aucun propriétaire n’est affecté.</span><span class="sxs-lookup"><span data-stu-id="0eb37-176">Owner of the incident, or *null* if no owner is assigned.</span></span>                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="0eb37-177">secop2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="0eb37-177">secop2@contoso.com</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="0eb37-178">classification</span><span class="sxs-lookup"><span data-stu-id="0eb37-178">classification</span></span>                            | <span data-ttu-id="0eb37-179">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="0eb37-179">The specification for the incident.</span></span> <span data-ttu-id="0eb37-180">Les valeurs de propriété sont les suivantes : *Unknown*, *FalsePositive*, *TruePositive*</span><span class="sxs-lookup"><span data-stu-id="0eb37-180">The property values are: *Unknown*, *FalsePositive*, *TruePositive*</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="0eb37-181">Inconnu</span><span class="sxs-lookup"><span data-stu-id="0eb37-181">Unknown</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="0eb37-182">indications</span><span class="sxs-lookup"><span data-stu-id="0eb37-182">determination</span></span>                             | <span data-ttu-id="0eb37-183">Indique la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="0eb37-183">Specifies the determination of the incident.</span></span> <span data-ttu-id="0eb37-184">Les valeurs de propriété sont les suivantes : *NotAvailable*, *apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *other*</span><span class="sxs-lookup"><span data-stu-id="0eb37-184">The property values are: *NotAvailable*, *Apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *Other*</span></span>                                                                                                                                                                                                                | <span data-ttu-id="0eb37-185">NotAvailable</span><span class="sxs-lookup"><span data-stu-id="0eb37-185">NotAvailable</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="0eb37-186">statut</span><span class="sxs-lookup"><span data-stu-id="0eb37-186">status</span></span>                                    | <span data-ttu-id="0eb37-187">Catégoriser les incidents ( *actif*ou *résolu*).</span><span class="sxs-lookup"><span data-stu-id="0eb37-187">Categorize incidents (as *Active*, or *Resolved*).</span></span> <span data-ttu-id="0eb37-188">Cela vous permet d’organiser et de gérer votre réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="0eb37-188">This helps you organize and manage your response to incidents.</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="0eb37-189">Actif</span><span class="sxs-lookup"><span data-stu-id="0eb37-189">Active</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-190">Sévérité </span><span class="sxs-lookup"><span data-stu-id="0eb37-190">severity</span></span>                                  | <span data-ttu-id="0eb37-191">Indique l’impact possible sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="0eb37-191">Indicates the possible impact on assets.</span></span> <span data-ttu-id="0eb37-192">Plus la gravité est élevée, plus l’impact est important.</span><span class="sxs-lookup"><span data-stu-id="0eb37-192">The higher the severity the bigger the impact.</span></span> <span data-ttu-id="0eb37-193">En règle générale, les éléments de gravité plus élevés nécessitent une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="0eb37-193">Typically higher severity items require the most immediate attention.</span></span><br><span data-ttu-id="0eb37-194">L’une des valeurs suivantes : *informatif*, *Low*, \* medium et *High*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-194">One of the following values: *Informational*, *Low*, \*Medium, and *High*.</span></span>                                                                                                                                | <span data-ttu-id="0eb37-195">Moyen</span><span class="sxs-lookup"><span data-stu-id="0eb37-195">Medium</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-196">étiquettes</span><span class="sxs-lookup"><span data-stu-id="0eb37-196">tags</span></span>                                      | <span data-ttu-id="0eb37-197">Tableau de balises personnalisées associées à un incident, par exemple pour marquer un groupe d’incidents avec une caractéristique commune.</span><span class="sxs-lookup"><span data-stu-id="0eb37-197">Array of custom tags associated with an incident, for example to flag a group of incidents with a common characteristic.</span></span>                                                                                                                                                                                                                                                                  | \[\]                                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-198">alerts</span><span class="sxs-lookup"><span data-stu-id="0eb37-198">alerts</span></span>                                    | <span data-ttu-id="0eb37-199">Tableau de toutes les alertes liées à l’incident et d’autres informations, telles que la gravité, les entités impliquées dans l’alerte, la source des alertes.</span><span class="sxs-lookup"><span data-stu-id="0eb37-199">Array of all the alerts related to the incident and other information, such as severity, entities that were involved in the alert, the source of the alerts.</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-200">\[\] (voir détails dans les champs d’alerte ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="0eb37-200">\[\] (see details on alert fields below)</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="0eb37-201">**Métadonnées d’alertes**</span><span class="sxs-lookup"><span data-stu-id="0eb37-201">**Alerts metadata**</span></span>                           |                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                   |
| <span data-ttu-id="0eb37-202">IDAlerte</span><span class="sxs-lookup"><span data-stu-id="0eb37-202">alertId</span></span>                                   | <span data-ttu-id="0eb37-203">Identificateur unique qui représente l’alerte.</span><span class="sxs-lookup"><span data-stu-id="0eb37-203">Unique identifier to represent the alert</span></span>                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="0eb37-204">caD70CFEE2-1F54-32DB-9988-3A868A1EBFAC</span><span class="sxs-lookup"><span data-stu-id="0eb37-204">caD70CFEE2-1F54-32DB-9988-3A868A1EBFAC</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-205">incidentId</span><span class="sxs-lookup"><span data-stu-id="0eb37-205">incidentId</span></span>                                | <span data-ttu-id="0eb37-206">Identificateur unique représentant l’incident auquel cette alerte est associée.</span><span class="sxs-lookup"><span data-stu-id="0eb37-206">Unique identifier to represent the incident this alert is associated with</span></span>                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="0eb37-207">924565</span><span class="sxs-lookup"><span data-stu-id="0eb37-207">924565</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-208">serviceSource</span><span class="sxs-lookup"><span data-stu-id="0eb37-208">serviceSource</span></span>                             | <span data-ttu-id="0eb37-209">Service d’origine de l’alerte, tel que Microsoft Defender ATP, Microsoft Cloud App Security, Azure ATP ou Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="0eb37-209">Service that the alert originates from, such as Microsoft Defender ATP, Microsoft Cloud App Security, Azure ATP, or Office 365 ATP.</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-210">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="0eb37-210">MicrosoftCloudAppSecurity</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="0eb37-211">creationTime</span><span class="sxs-lookup"><span data-stu-id="0eb37-211">creationTime</span></span>                              | <span data-ttu-id="0eb37-212">Heure à laquelle l’alerte a été créée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="0eb37-212">Time when alert was first created.</span></span>                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="0eb37-213">2020-09-06T14:46:55.7182276 Z</span><span class="sxs-lookup"><span data-stu-id="0eb37-213">2020-09-06T14:46:55.7182276Z</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="0eb37-214">lastUpdatedTime</span><span class="sxs-lookup"><span data-stu-id="0eb37-214">lastUpdatedTime</span></span>                           | <span data-ttu-id="0eb37-215">Heure de la dernière mise à jour de l’alerte sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="0eb37-215">Time when alert was last updated at the backend.</span></span>                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="0eb37-216">2020-09-06T14:46:57.2433333 Z</span><span class="sxs-lookup"><span data-stu-id="0eb37-216">2020-09-06T14:46:57.2433333Z</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="0eb37-217">resolvedTime</span><span class="sxs-lookup"><span data-stu-id="0eb37-217">resolvedTime</span></span>                              | <span data-ttu-id="0eb37-218">Heure de la résolution de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="0eb37-218">Time when alert was resolved.</span></span>                                                                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="0eb37-219">2020-09-10T05:22:59Z</span><span class="sxs-lookup"><span data-stu-id="0eb37-219">2020-09-10T05:22:59Z</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-220">firstActivity</span><span class="sxs-lookup"><span data-stu-id="0eb37-220">firstActivity</span></span>                             | <span data-ttu-id="0eb37-221">Heure à laquelle l’alerte a signalé pour la première fois que l’activité a été mise à jour sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="0eb37-221">Time when alert first reported that activity was updated at the backend.</span></span>                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="0eb37-222">2020-09-04T05:22:59Z</span><span class="sxs-lookup"><span data-stu-id="0eb37-222">2020-09-04T05:22:59Z</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-223">title</span><span class="sxs-lookup"><span data-stu-id="0eb37-223">title</span></span>                                     | <span data-ttu-id="0eb37-224">Courte valeur de chaîne d’identification disponible pour chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="0eb37-224">Brief identifying string value available for each alert.</span></span>                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-225">Activité ransomware</span><span class="sxs-lookup"><span data-stu-id="0eb37-225">Ransomware activity</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="0eb37-226">description</span><span class="sxs-lookup"><span data-stu-id="0eb37-226">description</span></span>                               | <span data-ttu-id="0eb37-227">Valeur de chaîne décrivant chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="0eb37-227">String value describing each alert.</span></span>                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="0eb37-228">Le test de l’utilisateur utilisateur2 (testUser2@contoso.com) a manipulé 99 fichiers avec plusieurs extensions se terminant par l’extension *herunterladen*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-228">The user Test User2 (testUser2@contoso.com) manipulated 99 files with multiple extensions ending with the uncommon extension *herunterladen*.</span></span> <span data-ttu-id="0eb37-229">Il s’agit d’un nombre inhabituel de manipulations de fichiers et indique une attaque par ransomware potentielle.</span><span class="sxs-lookup"><span data-stu-id="0eb37-229">This is an unusual number of file manipulations and is indicative of a potential ransomware attack.</span></span> |
| <span data-ttu-id="0eb37-230">category</span><span class="sxs-lookup"><span data-stu-id="0eb37-230">category</span></span>                                  | <span data-ttu-id="0eb37-231">Vue visuelle et numérique de la progression de l’attaque le long de la chaîne de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0eb37-231">Visual and numeric view of how far the attack has progressed along the kill chain.</span></span> <span data-ttu-id="0eb37-232">Aligné sur l' [infrastructure Mitre ATT&CK™](https://attack.mitre.org/).</span><span class="sxs-lookup"><span data-stu-id="0eb37-232">Aligned to the [MITRE ATT&CK™ framework](https://attack.mitre.org/).</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="0eb37-233">Impact</span><span class="sxs-lookup"><span data-stu-id="0eb37-233">Impact</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-234">statut</span><span class="sxs-lookup"><span data-stu-id="0eb37-234">status</span></span>                                    | <span data-ttu-id="0eb37-235">Catégoriser les alertes (en tant que *nouvelles*, *actives*ou *résolues*).</span><span class="sxs-lookup"><span data-stu-id="0eb37-235">Categorize alerts (as *New*, *Active*, or *Resolved*).</span></span> <span data-ttu-id="0eb37-236">Cela vous permet d’organiser et de gérer votre réponse aux alertes.</span><span class="sxs-lookup"><span data-stu-id="0eb37-236">This helps you organize and manage your response to alerts.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="0eb37-237">Nouveau</span><span class="sxs-lookup"><span data-stu-id="0eb37-237">New</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="0eb37-238">Sévérité </span><span class="sxs-lookup"><span data-stu-id="0eb37-238">severity</span></span>                                  | <span data-ttu-id="0eb37-239">Indique l’impact possible sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="0eb37-239">Indicates the possible impact on assets.</span></span> <span data-ttu-id="0eb37-240">Plus la gravité est élevée, plus l’impact est important.</span><span class="sxs-lookup"><span data-stu-id="0eb37-240">The higher the severity the bigger the impact.</span></span> <span data-ttu-id="0eb37-241">En règle générale, les éléments de gravité plus élevés nécessitent une attention immédiate.</span><span class="sxs-lookup"><span data-stu-id="0eb37-241">Typically higher severity items require the most immediate attention.</span></span><br><span data-ttu-id="0eb37-242">L’une des valeurs suivantes : *informatif*, *Low*, \* medium et *High*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-242">One of the following values: *Informational*, *Low*, \*Medium, and *High*.</span></span>                                                                                                                                   | <span data-ttu-id="0eb37-243">Moyen</span><span class="sxs-lookup"><span data-stu-id="0eb37-243">Medium</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-244">investigationId</span><span class="sxs-lookup"><span data-stu-id="0eb37-244">investigationId</span></span>                           | <span data-ttu-id="0eb37-245">ID d’enquête automatisé déclenché par cette alerte.</span><span class="sxs-lookup"><span data-stu-id="0eb37-245">The automated investigation id triggered by this alert.</span></span>                                                                                                                                                                                                                                                                                                                                | <span data-ttu-id="0eb37-246">1234</span><span class="sxs-lookup"><span data-stu-id="0eb37-246">1234</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-247">investigationState</span><span class="sxs-lookup"><span data-stu-id="0eb37-247">investigationState</span></span>                        | <span data-ttu-id="0eb37-248">Informations sur l’état actuel de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="0eb37-248">Information on the investigation's current status.</span></span> <span data-ttu-id="0eb37-249">L’un des éléments suivants *: inconnu*, *terminé*, *SuccessfullyRemediated*, *bénigne*, *échec*, *PartiallyRemediated*, *en cours d’exécution*, *PendingApproval*, *PendingResource*, *PartiallyInvestigated*, *TerminatedByUser*, *TerminatedBySystem*, *mis en file d’attente*, *InnerFailure*, *PreexistingAlert*, non *pris en charge*, *UnsupportedAlertType*, *SuppressedAlert.*</span><span class="sxs-lookup"><span data-stu-id="0eb37-249">One of the following: *Unknown*, *Terminated*, *SuccessfullyRemediated*, *Benign*, *Failed*, *PartiallyRemediated*, *Running*, *PendingApproval*, *PendingResource*, *PartiallyInvestigated*, *TerminatedByUser*, *TerminatedBySystem*, *Queued*, *InnerFailure*, *PreexistingAlert*, *UnsupportedOs*, *UnsupportedAlertType*, *SuppressedAlert*.</span></span> | <span data-ttu-id="0eb37-250">UnsupportedAlertType</span><span class="sxs-lookup"><span data-stu-id="0eb37-250">UnsupportedAlertType</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-251">classification</span><span class="sxs-lookup"><span data-stu-id="0eb37-251">classification</span></span>                            | <span data-ttu-id="0eb37-252">Spécification de l’incident.</span><span class="sxs-lookup"><span data-stu-id="0eb37-252">The specification for the incident.</span></span> <span data-ttu-id="0eb37-253">Les valeurs de propriété sont les suivantes : *Unknown*, *FalsePositive*, *TruePositive* ou *null*</span><span class="sxs-lookup"><span data-stu-id="0eb37-253">The property values are: *Unknown*, *FalsePositive*, *TruePositive* or *null*</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="0eb37-254">Inconnu</span><span class="sxs-lookup"><span data-stu-id="0eb37-254">Unknown</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="0eb37-255">indications</span><span class="sxs-lookup"><span data-stu-id="0eb37-255">determination</span></span>                             | <span data-ttu-id="0eb37-256">Indique la détermination de l’incident.</span><span class="sxs-lookup"><span data-stu-id="0eb37-256">Specifies the determination of the incident.</span></span> <span data-ttu-id="0eb37-257">Les valeurs de propriété sont les suivantes : *NotAvailable*, *apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *other* ou  *null*</span><span class="sxs-lookup"><span data-stu-id="0eb37-257">The property values are: *NotAvailable*, *Apt*, *Malware*, *SecurityPersonnel*, *SecurityTesting*, *UnwantedSoftware*, *Other* or  *null*</span></span>                                                                                                                                                                                                     | <span data-ttu-id="0eb37-258">Susceptibles</span><span class="sxs-lookup"><span data-stu-id="0eb37-258">Apt</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="0eb37-259">assignedTo</span><span class="sxs-lookup"><span data-stu-id="0eb37-259">assignedTo</span></span>                                | <span data-ttu-id="0eb37-260">Propriétaire de l’incident ou *valeur null* si aucun propriétaire n’est affecté.</span><span class="sxs-lookup"><span data-stu-id="0eb37-260">Owner of the incident, or *null* if no owner is assigned.</span></span>                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="0eb37-261">secop2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="0eb37-261">secop2@contoso.com</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="0eb37-262">actorName</span><span class="sxs-lookup"><span data-stu-id="0eb37-262">actorName</span></span>                                 | <span data-ttu-id="0eb37-263">Le groupe d’activités, le cas échéant, associé à cette alerte.</span><span class="sxs-lookup"><span data-stu-id="0eb37-263">The activity group, if any, the  associated with this alert.</span></span>                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="0eb37-264">DOSAGE</span><span class="sxs-lookup"><span data-stu-id="0eb37-264">BORON</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="0eb37-265">threatFamilyName</span><span class="sxs-lookup"><span data-stu-id="0eb37-265">threatFamilyName</span></span>                          | <span data-ttu-id="0eb37-266">Famille de menaces associée à cette alerte.</span><span class="sxs-lookup"><span data-stu-id="0eb37-266">Threat family associated with this alert.</span></span>                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="0eb37-267">null</span><span class="sxs-lookup"><span data-stu-id="0eb37-267">null</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-268">mitreTechniques</span><span class="sxs-lookup"><span data-stu-id="0eb37-268">mitreTechniques</span></span>                           | <span data-ttu-id="0eb37-269">Les techniques d’attaque, telles que alignées sur l’infrastructure [Mitre ATT&CK](https://attack.mitre.org/)™.</span><span class="sxs-lookup"><span data-stu-id="0eb37-269">The attack techniques, as aligned with the [MITRE ATT&CK](https://attack.mitre.org/)™ framework.</span></span>                                                                                                                                                                                                                                                                                                                              | \[\]                                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-270">appareils</span><span class="sxs-lookup"><span data-stu-id="0eb37-270">devices</span></span>                                   | <span data-ttu-id="0eb37-271">Tous les appareils pour lesquels des alertes liées à l’incident ont été envoyées.</span><span class="sxs-lookup"><span data-stu-id="0eb37-271">All devices where alerts related to the incident were sent.</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-272">\[\] (voir les détails sur les champs d’entité ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="0eb37-272">\[\] (see details on entity fields below)</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="0eb37-273">**Format du périphérique**</span><span class="sxs-lookup"><span data-stu-id="0eb37-273">**Device format**</span></span>                             |                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                   |
| <span data-ttu-id="0eb37-274">DeviceId</span><span class="sxs-lookup"><span data-stu-id="0eb37-274">DeviceId</span></span>                                  | <span data-ttu-id="0eb37-275">ID de périphérique désigné dans Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="0eb37-275">The device ID as designated in Microsoft Defender ATP.</span></span>                                                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="0eb37-276">24c222b0b60fe148eeece49ac83910cc6a7ef491</span><span class="sxs-lookup"><span data-stu-id="0eb37-276">24c222b0b60fe148eeece49ac83910cc6a7ef491</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="0eb37-277">aadDeviceId</span><span class="sxs-lookup"><span data-stu-id="0eb37-277">aadDeviceId</span></span>                               |  <span data-ttu-id="0eb37-278">ID de périphérique désigné dans [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) (AAD).</span><span class="sxs-lookup"><span data-stu-id="0eb37-278">The device Id as designated in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) (AAD).</span></span> <span data-ttu-id="0eb37-279">Disponible uniquement pour les appareils joints à un domaine.</span><span class="sxs-lookup"><span data-stu-id="0eb37-279">Only available for domain-joined devices.</span></span>                                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="0eb37-280">null</span><span class="sxs-lookup"><span data-stu-id="0eb37-280">null</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-281">deviceDnsName</span><span class="sxs-lookup"><span data-stu-id="0eb37-281">deviceDnsName</span></span>                             | <span data-ttu-id="0eb37-282">Nom de domaine complet du périphérique.</span><span class="sxs-lookup"><span data-stu-id="0eb37-282">The fully qualified domain name for the device.</span></span>                                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="0eb37-283">user5cx.middleeast.corp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="0eb37-283">user5cx.middleeast.corp.contoso.com</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="0eb37-284">osPlatform</span><span class="sxs-lookup"><span data-stu-id="0eb37-284">osPlatform</span></span>                                | <span data-ttu-id="0eb37-285">Plateforme de système d’exploitation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0eb37-285">The OS platform the device is running.</span></span>                                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-286">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="0eb37-286">WindowsServer2016</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="0eb37-287">osBuild</span><span class="sxs-lookup"><span data-stu-id="0eb37-287">osBuild</span></span>                                   | <span data-ttu-id="0eb37-288">Version de build pour le système d’exploitation sur lequel l’appareil est exécuté.</span><span class="sxs-lookup"><span data-stu-id="0eb37-288">The build version for the OS the device is running.</span></span>                                                                                                                                                                                                                                                                                                                                                                | <span data-ttu-id="0eb37-289">14393</span><span class="sxs-lookup"><span data-stu-id="0eb37-289">14393</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="0eb37-290">rbacGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb37-290">rbacGroupName</span></span>                             | <span data-ttu-id="0eb37-291">Le groupe de [contrôle d’accès basé sur un rôle](https://docs.microsoft.com/azure/role-based-access-control/overview) (RBAC) associé au périphérique.</span><span class="sxs-lookup"><span data-stu-id="0eb37-291">The [role-based access control](https://docs.microsoft.com/azure/role-based-access-control/overview) (RBAC) group associated with the device.</span></span>                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="0eb37-292">WDATP-Ring0</span><span class="sxs-lookup"><span data-stu-id="0eb37-292">WDATP-Ring0</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="0eb37-293">firstSeen</span><span class="sxs-lookup"><span data-stu-id="0eb37-293">firstSeen</span></span>                                 | <span data-ttu-id="0eb37-294">Heure du premier démarrage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0eb37-294">Time when device was first seen.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="0eb37-295">2020-02-06T14:16:01.9330135 Z</span><span class="sxs-lookup"><span data-stu-id="0eb37-295">2020-02-06T14:16:01.9330135Z</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="0eb37-296">healthStatus</span><span class="sxs-lookup"><span data-stu-id="0eb37-296">healthStatus</span></span>                              | <span data-ttu-id="0eb37-297">État d’intégrité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0eb37-297">The health state of the device.</span></span>                                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="0eb37-298">Actif</span><span class="sxs-lookup"><span data-stu-id="0eb37-298">Active</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-299">riskScore</span><span class="sxs-lookup"><span data-stu-id="0eb37-299">riskScore</span></span>                                 | <span data-ttu-id="0eb37-300">Score de risque de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0eb37-300">The risk score for the  device.</span></span>                                                                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="0eb37-301">Élevé</span><span class="sxs-lookup"><span data-stu-id="0eb37-301">High</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-302">entités</span><span class="sxs-lookup"><span data-stu-id="0eb37-302">entities</span></span>                                  | <span data-ttu-id="0eb37-303">Toutes les entités identifiées comme faisant partie d’une alerte donnée ou associées à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="0eb37-303">All entities that have been identified to be part of, or related to, a given alert.</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="0eb37-304">\[\] (voir les détails sur les champs d’entité ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="0eb37-304">\[\] (see details on entity fields below)</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="0eb37-305">**Format d’entité**</span><span class="sxs-lookup"><span data-stu-id="0eb37-305">**Entity Format**</span></span>                             |                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                   |
| <span data-ttu-id="0eb37-306">entityType</span><span class="sxs-lookup"><span data-stu-id="0eb37-306">entityType</span></span>                                | <span data-ttu-id="0eb37-307">Entités identifiées comme faisant partie d’une alerte donnée ou associées à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="0eb37-307">Entities that have been identified to be part of, or related to, a given alert.</span></span><br><span data-ttu-id="0eb37-308">Les valeurs des propriétés sont les suivantes : *User*, *IP*, *URL*, *file*, *Process*, *Mailbox*, *MailMessage*, *MailCluster*, *Registry*</span><span class="sxs-lookup"><span data-stu-id="0eb37-308">The properties values are: *User*, *Ip*, *Url*, *File*, *Process*, *MailBox*, *MailMessage*, *MailCluster*, *Registry*</span></span>                                                                                                                                                                                                     | <span data-ttu-id="0eb37-309">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="0eb37-309">User</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-310">Algorithm</span><span class="sxs-lookup"><span data-stu-id="0eb37-310">sha1</span></span>                                      | <span data-ttu-id="0eb37-311">Disponible si entityType est un *fichier*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-311">Available if entityType is *File*.</span></span><br><span data-ttu-id="0eb37-312">Hachage de fichier pour les alertes associées à un fichier ou à un processus.</span><span class="sxs-lookup"><span data-stu-id="0eb37-312">The file hash for alerts associated with a file or process.</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="0eb37-313">5de839186691aa96ee2ca6d74f0a38fb8d1bd6dd</span><span class="sxs-lookup"><span data-stu-id="0eb37-313">5de839186691aa96ee2ca6d74f0a38fb8d1bd6dd</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="0eb37-314">SHA256</span><span class="sxs-lookup"><span data-stu-id="0eb37-314">sha256</span></span>                                    | <span data-ttu-id="0eb37-315">Disponible si entityType est un *fichier*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-315">Available if entityType is *File*.</span></span><br><span data-ttu-id="0eb37-316">Hachage de fichier pour les alertes associées à un fichier ou à un processus.</span><span class="sxs-lookup"><span data-stu-id="0eb37-316">The file hash for alerts associated with a file or process.</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="0eb37-317">28cb017dfc99073aa1b47c1b30f413e3ce774c4991eb4158de50f9dbb36d8043</span><span class="sxs-lookup"><span data-stu-id="0eb37-317">28cb017dfc99073aa1b47c1b30f413e3ce774c4991eb4158de50f9dbb36d8043</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="0eb37-318">fileName</span><span class="sxs-lookup"><span data-stu-id="0eb37-318">fileName</span></span>                                  | <span data-ttu-id="0eb37-319">Disponible si entityType est un *fichier*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-319">Available if entityType is *File*.</span></span><br><span data-ttu-id="0eb37-320">Nom de fichier pour les alertes associées à un fichier ou à un processus</span><span class="sxs-lookup"><span data-stu-id="0eb37-320">The file name for alerts associated with a file or process</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="0eb37-321">Detector.UnitTests.dll</span><span class="sxs-lookup"><span data-stu-id="0eb37-321">Detector.UnitTests.dll</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-322">PCF</span><span class="sxs-lookup"><span data-stu-id="0eb37-322">filePath</span></span>                                  | <span data-ttu-id="0eb37-323">Disponible si entityType est un *fichier*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-323">Available if entityType is *File*.</span></span><br><span data-ttu-id="0eb37-324">Chemin d’accès de fichier pour les alertes associées à un fichier ou à un processus</span><span class="sxs-lookup"><span data-stu-id="0eb37-324">The file path for alerts associated with a file or process</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="0eb37-325">C : \\ \\ travail de l’agent \\ \\ \_ \\ \\ \_ temp \\ \\ Deploy \_ System 2020-09-06 12 \_ 14 \_ 54 \\ \\ out</span><span class="sxs-lookup"><span data-stu-id="0eb37-325">C:\\\\Agent\\\\\_work\\\\\_temp\\\\Deploy\_SYSTEM 2020-09-06 12\_14\_54\\\\Out</span></span>                                                                                                                                                                    |
| <span data-ttu-id="0eb37-326">processId</span><span class="sxs-lookup"><span data-stu-id="0eb37-326">processId</span></span>                                 | <span data-ttu-id="0eb37-327">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-327">Available if entityType is *Process*.</span></span>                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-328">24348</span><span class="sxs-lookup"><span data-stu-id="0eb37-328">24348</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="0eb37-329">processCommandLine</span><span class="sxs-lookup"><span data-stu-id="0eb37-329">processCommandLine</span></span>                        | <span data-ttu-id="0eb37-330">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-330">Available if entityType is *Process*.</span></span>                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-331">« \\ Votre fichier est prêt à être téléchargé \_1911150169.exe\\ »</span><span class="sxs-lookup"><span data-stu-id="0eb37-331">"\\"Your File Is Ready To Download\_1911150169.exe\\" "</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="0eb37-332">processCreationTime</span><span class="sxs-lookup"><span data-stu-id="0eb37-332">processCreationTime</span></span>                       | <span data-ttu-id="0eb37-333">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-333">Available if entityType is *Process*.</span></span>                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-334">2020-07-18T03:25:38.5269993 Z</span><span class="sxs-lookup"><span data-stu-id="0eb37-334">2020-07-18T03:25:38.5269993Z</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="0eb37-335">parentProcessId</span><span class="sxs-lookup"><span data-stu-id="0eb37-335">parentProcessId</span></span>                           | <span data-ttu-id="0eb37-336">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-336">Available if entityType is *Process*.</span></span>                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="0eb37-337">16840</span><span class="sxs-lookup"><span data-stu-id="0eb37-337">16840</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="0eb37-338">parentProcessCreationTime</span><span class="sxs-lookup"><span data-stu-id="0eb37-338">parentProcessCreationTime</span></span>                 | <span data-ttu-id="0eb37-339">Disponible si entityType est *Process*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-339">Available if entityType is *Process*.</span></span>                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-340">2020-07-18T02:12:32.8616797 Z</span><span class="sxs-lookup"><span data-stu-id="0eb37-340">2020-07-18T02:12:32.8616797Z</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="0eb37-341">ipAddress</span><span class="sxs-lookup"><span data-stu-id="0eb37-341">ipAddress</span></span>                                 | <span data-ttu-id="0eb37-342">Disponible si entityType est *IP*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-342">Available if entityType is *Ip*.</span></span> <br><span data-ttu-id="0eb37-343">Adresse IP pour les alertes associées à des événements réseau, comme *la communication avec une destination réseau malveillante*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-343">IP address for alerts associated with network events, such as *Communication to a malicious network destination*.</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="0eb37-344">62.216.203.204</span><span class="sxs-lookup"><span data-stu-id="0eb37-344">62.216.203.204</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="0eb37-345">url</span><span class="sxs-lookup"><span data-stu-id="0eb37-345">url</span></span>                                       | <span data-ttu-id="0eb37-346">Disponible si entityType est *URL*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-346">Available if entityType is *Url*.</span></span> <br><span data-ttu-id="0eb37-347">URL pour les alertes associées aux événements réseau, comme *la communication à une destination réseau malveillante*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-347">Url for alerts associated to network events, such as, *Communication to a malicious network destination*.</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="0eb37-348">down.esales360.cn</span><span class="sxs-lookup"><span data-stu-id="0eb37-348">down.esales360.cn</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="0eb37-349">accountName</span><span class="sxs-lookup"><span data-stu-id="0eb37-349">accountName</span></span>                               | <span data-ttu-id="0eb37-350">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-350">Available if entityType is *User*.</span></span>                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="0eb37-351">testUser2</span><span class="sxs-lookup"><span data-stu-id="0eb37-351">testUser2</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="0eb37-352">domainName</span><span class="sxs-lookup"><span data-stu-id="0eb37-352">domainName</span></span>                                | <span data-ttu-id="0eb37-353">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-353">Available if entityType is *User*.</span></span>                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="0eb37-354">Europe. Corp. contoso</span><span class="sxs-lookup"><span data-stu-id="0eb37-354">europe.corp.contoso</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-355">userSid</span><span class="sxs-lookup"><span data-stu-id="0eb37-355">userSid</span></span>                                   | <span data-ttu-id="0eb37-356">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-356">Available if entityType is *User*.</span></span>                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="0eb37-357">S-1-5-21-1721254763-462695806-1538882281-4156657</span><span class="sxs-lookup"><span data-stu-id="0eb37-357">S-1-5-21-1721254763-462695806-1538882281-4156657</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="0eb37-358">aadUserId</span><span class="sxs-lookup"><span data-stu-id="0eb37-358">aadUserId</span></span>                                 | <span data-ttu-id="0eb37-359">Disponible si entityType est *User*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-359">Available if entityType is *User*.</span></span>                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="0eb37-360">fc8f7484-f813-4db2-afab-bc1507913fb6</span><span class="sxs-lookup"><span data-stu-id="0eb37-360">fc8f7484-f813-4db2-afab-bc1507913fb6</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-361">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0eb37-361">userPrincipalName</span></span>                         | <span data-ttu-id="0eb37-362">Disponible si EntityType est *User*la / *boîte aux lettres*utilisateur / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-362">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span>                                                                                                                                                                                                                                                                                                                                | <span data-ttu-id="0eb37-363">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="0eb37-363">testUser2@contoso.com</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="0eb37-364">mailboxDisplayName</span><span class="sxs-lookup"><span data-stu-id="0eb37-364">mailboxDisplayName</span></span>                        | <span data-ttu-id="0eb37-365">Disponible si entityType est *Mailbox*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-365">Available if entityType is *MailBox*.</span></span>                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-366">test utilisateur2</span><span class="sxs-lookup"><span data-stu-id="0eb37-366">test User2</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="0eb37-367">mailboxAddress</span><span class="sxs-lookup"><span data-stu-id="0eb37-367">mailboxAddress</span></span>                            | <span data-ttu-id="0eb37-368">Disponible si EntityType est *User*la / *boîte aux lettres*utilisateur / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-368">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span>                                                                                                                                                                                                                                                                                                                                | <span data-ttu-id="0eb37-369">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="0eb37-369">testUser2@contoso.com</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="0eb37-370">clusterBy</span><span class="sxs-lookup"><span data-stu-id="0eb37-370">clusterBy</span></span>                                 | <span data-ttu-id="0eb37-371">Disponible si entityType est  *MailCluster*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-371">Available if entityType is  *MailCluster*.</span></span>                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="0eb37-372">Experts P2SenderDomain; ContentType</span><span class="sxs-lookup"><span data-stu-id="0eb37-372">Subject;P2SenderDomain;ContentType</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="0eb37-373">expéditeur</span><span class="sxs-lookup"><span data-stu-id="0eb37-373">sender</span></span>                                    | <span data-ttu-id="0eb37-374">Disponible si EntityType est *User*la / *boîte aux lettres*utilisateur / *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-374">Available if entityType is *User*/*MailBox*/*MailMessage*.</span></span>                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="0eb37-375">user.abc@mail.contoso.co.in</span><span class="sxs-lookup"><span data-stu-id="0eb37-375">user.abc@mail.contoso.co.in</span></span>                                                                                                                                                                 |
| <span data-ttu-id="0eb37-376">destinataire</span><span class="sxs-lookup"><span data-stu-id="0eb37-376">recipient</span></span>                                 | <span data-ttu-id="0eb37-377">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-377">Available if entityType is *MailMessage*.</span></span>                                                                                                                                                                                                                                                                                                                                                | <span data-ttu-id="0eb37-378">testUser2@contoso.com</span><span class="sxs-lookup"><span data-stu-id="0eb37-378">testUser2@contoso.com</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="0eb37-379">sujet</span><span class="sxs-lookup"><span data-stu-id="0eb37-379">subject</span></span>                                   | <span data-ttu-id="0eb37-380">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-380">Available if entityType is *MailMessage*.</span></span>                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="0eb37-381">\[\]Attention externe</span><span class="sxs-lookup"><span data-stu-id="0eb37-381">\[EXTERNAL\] Attention</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-382">deliveryAction</span><span class="sxs-lookup"><span data-stu-id="0eb37-382">deliveryAction</span></span>                            | <span data-ttu-id="0eb37-383">Disponible si entityType est *MailMessage*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-383">Available if entityType is *MailMessage*.</span></span>                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="0eb37-384">Cmds</span><span class="sxs-lookup"><span data-stu-id="0eb37-384">Delivered</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="0eb37-385">securityGroupId</span><span class="sxs-lookup"><span data-stu-id="0eb37-385">securityGroupId</span></span>                           | <span data-ttu-id="0eb37-386">Disponible si entityType est  *SecurityGroup*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-386">Available if entityType is  *SecurityGroup*.</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="0eb37-387">301c47c8-e15f-4059-AB09-e2ba9ffd372b</span><span class="sxs-lookup"><span data-stu-id="0eb37-387">301c47c8-e15f-4059-ab09-e2ba9ffd372b</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-388">securityGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb37-388">securityGroupName</span></span>                         | <span data-ttu-id="0eb37-389">Disponible si entityType est  *SecurityGroup*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-389">Available if entityType is  *SecurityGroup*.</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="0eb37-390">Opérateurs de configuration réseau</span><span class="sxs-lookup"><span data-stu-id="0eb37-390">Network Configuration Operators</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="0eb37-391">registryHive</span><span class="sxs-lookup"><span data-stu-id="0eb37-391">registryHive</span></span>                              | <span data-ttu-id="0eb37-392">Disponible si entityType est  *Registry*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-392">Available if entityType is  *Registry*.</span></span>                                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="0eb37-393">HKEY \_ local \_ machine</span><span class="sxs-lookup"><span data-stu-id="0eb37-393">HKEY\_LOCAL\_MACHINE</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="0eb37-394">registryKey</span><span class="sxs-lookup"><span data-stu-id="0eb37-394">registryKey</span></span>                               | <span data-ttu-id="0eb37-395">Disponible si entityType est  *Registry*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-395">Available if entityType is  *Registry*.</span></span>                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0eb37-396">LOGICIEL \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Winlogon</span><span class="sxs-lookup"><span data-stu-id="0eb37-396">SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Winlogon</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="0eb37-397">registryValueType</span><span class="sxs-lookup"><span data-stu-id="0eb37-397">registryValueType</span></span>                         | <span data-ttu-id="0eb37-398">Disponible si entityType est  *Registry*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-398">Available if entityType is  *Registry*.</span></span>                                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="0eb37-399">String</span><span class="sxs-lookup"><span data-stu-id="0eb37-399">String</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="0eb37-400">registryValue</span><span class="sxs-lookup"><span data-stu-id="0eb37-400">registryValue</span></span>                             | <span data-ttu-id="0eb37-401">Disponible si entityType est  *Registry*.</span><span class="sxs-lookup"><span data-stu-id="0eb37-401">Available if entityType is  *Registry*.</span></span>                                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="0eb37-402">31-00-00-00</span><span class="sxs-lookup"><span data-stu-id="0eb37-402">31-00-00-00</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="0eb37-403">deviceId</span><span class="sxs-lookup"><span data-stu-id="0eb37-403">deviceId</span></span>                                  | <span data-ttu-id="0eb37-404">ID, le cas échéant, de l’appareil associé à l’entité.</span><span class="sxs-lookup"><span data-stu-id="0eb37-404">The ID, if any, of the device related to the entity.</span></span>                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="0eb37-405">986e5df8b73dacd43c8917d17e523e76b13c75cd</span><span class="sxs-lookup"><span data-stu-id="0eb37-405">986e5df8b73dacd43c8917d17e523e76b13c75cd</span></span>                                                                                                                                                                                                          |



## <a name="example"></a><span data-ttu-id="0eb37-406">Exemple</span><span class="sxs-lookup"><span data-stu-id="0eb37-406">Example</span></span>

<span data-ttu-id="0eb37-407">**Demande**</span><span class="sxs-lookup"><span data-stu-id="0eb37-407">**Request**</span></span>

```
GET https://api.security.microsoft.com/api/incidents
```

<span data-ttu-id="0eb37-408">**Response**</span><span class="sxs-lookup"><span data-stu-id="0eb37-408">**Response**</span></span>
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

## <a name="related-topic"></a><span data-ttu-id="0eb37-409">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0eb37-409">Related topic</span></span>
- [<span data-ttu-id="0eb37-410">API d’incident</span><span class="sxs-lookup"><span data-stu-id="0eb37-410">Incident APIs</span></span>](api-incident.md)
- [<span data-ttu-id="0eb37-411">Incident de mise à jour</span><span class="sxs-lookup"><span data-stu-id="0eb37-411">Update incident</span></span>](api-update-incidents.md)
