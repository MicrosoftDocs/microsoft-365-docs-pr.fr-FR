---
title: Table AADSpnSignInEventsBeta dans le schéma de recherche avancé
description: En savoir plus sur les informations associées au principal Azure Active Directory service et à la table des événements de signature d’identité gérée du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, AlertInfo, alert, entities, evidence, file, IP address, device, machine, user, account, identity, AAD
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: f74972bcd5d0ddaab58d82b72a55991fda44e3b1
ms.sourcegitcommit: 9541d5e6720a06327dc785e3ad7e8fb11246fd72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2021
ms.locfileid: "52583543"
---
# <a name="aadspnsignineventsbeta"></a><span data-ttu-id="11504-104">AADSpnSignInEventsBeta</span><span class="sxs-lookup"><span data-stu-id="11504-104">AADSpnSignInEventsBeta</span></span>

<span data-ttu-id="11504-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="11504-105">**Applies to:**</span></span>

- <span data-ttu-id="11504-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="11504-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT]
> <span data-ttu-id="11504-107">Le tableau est actuellement en version bêta et est proposé à court terme pour vous permettre de chercher des événements de signature d’identité gérée et de principal de `AADSpnSignInEventsBeta` service Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="11504-107">The `AADSpnSignInEventsBeta` table is currently in beta and is being offered on a short-term basis to allow you to hunt through Azure Active Directory (AAD) service principal and managed identity sign-in events.</span></span> <span data-ttu-id="11504-108">Nous finirons par déplacer toutes les informations de schéma de signature vers la `IdentityLogonEvents` table.</span><span class="sxs-lookup"><span data-stu-id="11504-108">We will eventually move all sign-in schema information to the `IdentityLogonEvents` table.</span></span>



<span data-ttu-id="11504-109">Le tableau dans le schéma de recherche avancée contient des informations sur Azure Active Directory principal de service et les `AADSpnSignInEventsBeta` sign-ins d’identité gérée. Vous pouvez en savoir plus sur les différents types de Azure Active Directory dans les rapports d’activité de Azure Active Directory de la signature [- aperçu.](/azure/active-directory/reports-monitoring/concept-all-sign-ins)</span><span class="sxs-lookup"><span data-stu-id="11504-109">The `AADSpnSignInEventsBeta` table in the advanced hunting schema contains information about Azure Active Directory service principal and managed identity sign-ins. You can learn more about the different kinds of sign-ins in [Azure Active Directory sign-in activity reports - preview](/azure/active-directory/reports-monitoring/concept-all-sign-ins).</span></span>

<span data-ttu-id="11504-110">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="11504-110">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="11504-111">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-reference).</span><span class="sxs-lookup"><span data-stu-id="11504-111">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-reference).</span></span>





| <span data-ttu-id="11504-112">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="11504-112">Column name</span></span>     | <span data-ttu-id="11504-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="11504-113">Data type</span></span> | <span data-ttu-id="11504-114">Description</span><span class="sxs-lookup"><span data-stu-id="11504-114">Description</span></span>   |
| ----- | ----- | ---- |
| `Timestamp` | <span data-ttu-id="11504-115">DateHeure</span><span class="sxs-lookup"><span data-stu-id="11504-115">datetime</span></span>      | <span data-ttu-id="11504-116">Date et heure de génération de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="11504-116">Date and time when the record was generated</span></span>                                                                                                     |
| `Application`          | <span data-ttu-id="11504-117">string</span><span class="sxs-lookup"><span data-stu-id="11504-117">string</span></span>        | <span data-ttu-id="11504-118">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="11504-118">Application that performed the recorded action</span></span>                                                                                                   |
| `ApplicationId`        | <span data-ttu-id="11504-119">string</span><span class="sxs-lookup"><span data-stu-id="11504-119">string</span></span>        | <span data-ttu-id="11504-120">Identificateur unique de l’application</span><span class="sxs-lookup"><span data-stu-id="11504-120">Unique identifier for the application</span></span>                                                                                                           |
| `IsManagedIdentity`    | <span data-ttu-id="11504-121">booléen</span><span class="sxs-lookup"><span data-stu-id="11504-121">boolean</span></span>       | <span data-ttu-id="11504-122">Indique si la connectez-vous a été initiée par une identité gérée</span><span class="sxs-lookup"><span data-stu-id="11504-122">Indicates whether the sign-in was initiated by a managed identity</span></span>                                                                               |
| `ErrorCode`            | <span data-ttu-id="11504-123">entier</span><span class="sxs-lookup"><span data-stu-id="11504-123">int</span></span>        | <span data-ttu-id="11504-124">Contient le code d’erreur si une erreur de se connecte se produit.</span><span class="sxs-lookup"><span data-stu-id="11504-124">Contains the error code if a sign-in error occurs.</span></span> <span data-ttu-id="11504-125">Pour trouver une description d’un code d’erreur spécifique, visitez <https://aka.ms/AADsigninsErrorCodes> .</span><span class="sxs-lookup"><span data-stu-id="11504-125">To find a description of a specific error code, visit <https://aka.ms/AADsigninsErrorCodes>.</span></span> |
| `CorrelationId`        | <span data-ttu-id="11504-126">string</span><span class="sxs-lookup"><span data-stu-id="11504-126">string</span></span>        | <span data-ttu-id="11504-127">Identificateur unique de l’événement de signature</span><span class="sxs-lookup"><span data-stu-id="11504-127">Unique identifier of the sign-in event</span></span>                                                                                                          |
| `ServicePrincipalName` | <span data-ttu-id="11504-128">string</span><span class="sxs-lookup"><span data-stu-id="11504-128">string</span></span>        | <span data-ttu-id="11504-129">Nom du principal de service à l’origine de la signature</span><span class="sxs-lookup"><span data-stu-id="11504-129">Name of the service principal that initiated the sign-in</span></span>                                                                                        |
| `ServicePrincipalId`   | <span data-ttu-id="11504-130">string</span><span class="sxs-lookup"><span data-stu-id="11504-130">string</span></span>        | <span data-ttu-id="11504-131">Identificateur unique du principal de service à l’origine de la signature</span><span class="sxs-lookup"><span data-stu-id="11504-131">Unique identifier of the service principal that initiated the sign-in</span></span>                                                                           |
| `ResourceDisplayName`  | <span data-ttu-id="11504-132">string</span><span class="sxs-lookup"><span data-stu-id="11504-132">string</span></span>        | <span data-ttu-id="11504-133">Nom d’affichage de la ressource accessible</span><span class="sxs-lookup"><span data-stu-id="11504-133">Display name of the resource accessed</span></span>                                                                                                           |
| `ResourceId`           | <span data-ttu-id="11504-134">string</span><span class="sxs-lookup"><span data-stu-id="11504-134">string</span></span>        | <span data-ttu-id="11504-135">Identificateur unique de la ressource à accès</span><span class="sxs-lookup"><span data-stu-id="11504-135">Unique identifier of the resource accessed</span></span>                                                                                                      |
| `ResourceTenantId`     | <span data-ttu-id="11504-136">string</span><span class="sxs-lookup"><span data-stu-id="11504-136">string</span></span>        | <span data-ttu-id="11504-137">Identificateur unique du client de la ressource à accès</span><span class="sxs-lookup"><span data-stu-id="11504-137">Unique identifier of the tenant of the resource accessed</span></span>                                                                                        |
| `IPAddress`            | <span data-ttu-id="11504-138">string</span><span class="sxs-lookup"><span data-stu-id="11504-138">string</span></span>        | <span data-ttu-id="11504-139">Adresse IP attribuée au point de terminaison et utilisée lors des communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="11504-139">IP address assigned to the endpoint and used during related network communications</span></span>                                                              |
| `Country`          | <span data-ttu-id="11504-140">string</span><span class="sxs-lookup"><span data-stu-id="11504-140">string</span></span>        | <span data-ttu-id="11504-141">Code à deux lettres indiquant le pays où l’adresse IP du client est géolocalisé</span><span class="sxs-lookup"><span data-stu-id="11504-141">Two-letter code indicating the country where the client IP address is geolocated</span></span>                                                                |
| `State`                | <span data-ttu-id="11504-142">string</span><span class="sxs-lookup"><span data-stu-id="11504-142">string</span></span>        | <span data-ttu-id="11504-143">État où la se connecte s’est produite, si disponible</span><span class="sxs-lookup"><span data-stu-id="11504-143">State where the sign-in occurred, if available</span></span>                                                                                                  |
| `City`                 | <span data-ttu-id="11504-144">string</span><span class="sxs-lookup"><span data-stu-id="11504-144">string</span></span>        | <span data-ttu-id="11504-145">Ville où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="11504-145">City where the account user is located</span></span>                                                                                                          |
| `Latitude`             | <span data-ttu-id="11504-146">string</span><span class="sxs-lookup"><span data-stu-id="11504-146">string</span></span>        | <span data-ttu-id="11504-147">Coordonnées nord à sud de l’emplacement de la signature</span><span class="sxs-lookup"><span data-stu-id="11504-147">The north to south coordinates of the sign-in location</span></span>                                                                                          |
| `Longitude`            | <span data-ttu-id="11504-148">string</span><span class="sxs-lookup"><span data-stu-id="11504-148">string</span></span>        | <span data-ttu-id="11504-149">Coordonnées est à ouest de l’emplacement de la signature</span><span class="sxs-lookup"><span data-stu-id="11504-149">The east to west coordinates of the sign-in location</span></span>                                                                                            |
| `RequestId`            | <span data-ttu-id="11504-150">string</span><span class="sxs-lookup"><span data-stu-id="11504-150">string</span></span>        | <span data-ttu-id="11504-151">Identificateur unique de la demande</span><span class="sxs-lookup"><span data-stu-id="11504-151">Unique identifier of the request</span></span>                                                                                                                |
|`ReportId` | <span data-ttu-id="11504-152">string</span><span class="sxs-lookup"><span data-stu-id="11504-152">string</span></span> | <span data-ttu-id="11504-153">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="11504-153">Unique identifier for the event</span></span> | 

 

## <a name="related-articles"></a><span data-ttu-id="11504-154">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="11504-154">Related articles</span></span>

-   [<span data-ttu-id="11504-155">AADSignInEventsBeta</span><span class="sxs-lookup"><span data-stu-id="11504-155">AADSignInEventsBeta</span></span>](./advanced-hunting-aadsignineventsbeta-table.md)
-   [<span data-ttu-id="11504-156">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="11504-156">Advanced hunting overview</span></span>](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-overview)
-   [<span data-ttu-id="11504-157">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="11504-157">Learn the query language</span></span>](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-query-language)
-   [<span data-ttu-id="11504-158">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="11504-158">Understand the schema</span></span>](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference)