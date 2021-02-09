---
title: Table AADSpnSignInEventsBeta dans le schéma de recherche avancé
description: En savoir plus sur les informations associées au principal de service Azure Active Directory et à la table des événements de signature d’identité gérée du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, AlertInfo, alert, entities, evidence, file, IP address, device, machine, user, account, identity, AAD
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
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 3eba2459fd9a0af1963ca8d1446b22fc0b1bdb93
ms.sourcegitcommit: 005028af7c5a6b2e95f17a0037958131484d9e73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2021
ms.locfileid: "50145402"
---
# <a name="aadspnsignineventsbeta"></a><span data-ttu-id="c53e2-104">AADSpnSignInEventsBeta</span><span class="sxs-lookup"><span data-stu-id="c53e2-104">AADSpnSignInEventsBeta</span></span>

<span data-ttu-id="c53e2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c53e2-105">**Applies to:**</span></span>

- <span data-ttu-id="c53e2-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c53e2-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT]
> <span data-ttu-id="c53e2-107">Le tableau est actuellement en version bêta et est proposé à court terme pour vous permettre de faire la recherche dans les événements de participation au principal de `AADSpnSignInEventsBeta` service Azure Active Directory (AAD) et d’identité gérée.</span><span class="sxs-lookup"><span data-stu-id="c53e2-107">The `AADSpnSignInEventsBeta` table is currently in beta and is being offered on a short-term basis to allow you to hunt through Azure Active Directory (AAD) service principal and managed identity sign-in events.</span></span> <span data-ttu-id="c53e2-108">Nous finirons par déplacer toutes les informations de schéma de signature vers la `IdentityLogonEvents` table.</span><span class="sxs-lookup"><span data-stu-id="c53e2-108">We will eventually move all sign-in schema information to the `IdentityLogonEvents` table.</span></span><br><br>
> <span data-ttu-id="c53e2-109">Les clients qui peuvent accéder à Microsoft 365 Defender par le biais de la solution Microsoft Defender for Endpoint intégrée du Centre de sécurité Azure, mais qui n’ont pas de licences pour Microsoft Defender pour Office, Microsoft Defender pour l’identité ou Microsoft Cloud App Security, ne pourront pas afficher ce schéma.</span><span class="sxs-lookup"><span data-stu-id="c53e2-109">Customers who can access Microsoft 365 Defender through the Azure Security Center’s integrated Microsoft Defender for Endpoint solution, but do not have licenses for Microsoft Defender for Office, Microsoft Defender for Identity, or Microsoft Cloud App Security, will not be able to view this schema.</span></span> 



<span data-ttu-id="c53e2-110">Le tableau du schéma de recherche avancée contient des informations sur le principal de service Azure Active Directory et les signatures d’identité `AADSpnSignInEventsBeta` gérée. Vous pouvez en savoir plus sur les différents types de sign-ins dans les rapports d’activité de la [sign-in Azure Active Directory - aperçu](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-all-sign-ins).</span><span class="sxs-lookup"><span data-stu-id="c53e2-110">The `AADSpnSignInEventsBeta` table in the advanced hunting schema contains information about Azure Active Directory service principal and managed identity sign-ins. You can learn more about the different kinds of sign-ins in [Azure Active Directory sign-in activity reports - preview](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-all-sign-ins).</span></span>

<span data-ttu-id="c53e2-111">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="c53e2-111">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="c53e2-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-reference).</span><span class="sxs-lookup"><span data-stu-id="c53e2-112">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-reference).</span></span>





| <span data-ttu-id="c53e2-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c53e2-113">Column name</span></span>     | <span data-ttu-id="c53e2-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="c53e2-114">Data type</span></span> | <span data-ttu-id="c53e2-115">Description</span><span class="sxs-lookup"><span data-stu-id="c53e2-115">Description</span></span>   |
| ----- | ----- | ---- |
| `Timestamp` | <span data-ttu-id="c53e2-116">DateHeure</span><span class="sxs-lookup"><span data-stu-id="c53e2-116">datetime</span></span>      | <span data-ttu-id="c53e2-117">Date et heure de génération de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="c53e2-117">Date and time when the record was generated</span></span>                                                                                                     |
| `Application`          | <span data-ttu-id="c53e2-118">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-118">string</span></span>        | <span data-ttu-id="c53e2-119">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="c53e2-119">Application that performed the recorded action</span></span>                                                                                                   |
| `ApplicationId`        | <span data-ttu-id="c53e2-120">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-120">string</span></span>        | <span data-ttu-id="c53e2-121">Identificateur unique de l’application</span><span class="sxs-lookup"><span data-stu-id="c53e2-121">Unique identifier for the application</span></span>                                                                                                           |
| `IsManagedIdentity`    | <span data-ttu-id="c53e2-122">booléen</span><span class="sxs-lookup"><span data-stu-id="c53e2-122">boolean</span></span>       | <span data-ttu-id="c53e2-123">Indique si la connectez-vous a été initiée par une identité gérée</span><span class="sxs-lookup"><span data-stu-id="c53e2-123">Indicates whether the sign-in was initiated by a managed identity</span></span>                                                                               |
| `ErrorCode`            | <span data-ttu-id="c53e2-124">int</span><span class="sxs-lookup"><span data-stu-id="c53e2-124">int</span></span>        | <span data-ttu-id="c53e2-125">Contient le code d’erreur si une erreur de se connecte se produit.</span><span class="sxs-lookup"><span data-stu-id="c53e2-125">Contains the error code if a sign-in error occurs.</span></span> <span data-ttu-id="c53e2-126">Pour trouver une description d’un code d’erreur spécifique, visitez <https://aka.ms/AADsigninsErrorCodes> .</span><span class="sxs-lookup"><span data-stu-id="c53e2-126">To find a description of a specific error code, visit <https://aka.ms/AADsigninsErrorCodes>.</span></span> |
| `CorrelationId`        | <span data-ttu-id="c53e2-127">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-127">string</span></span>        | <span data-ttu-id="c53e2-128">Identificateur unique de l’événement de signature</span><span class="sxs-lookup"><span data-stu-id="c53e2-128">Unique identifier of the sign-in event</span></span>                                                                                                          |
| `ServicePrincipalName` | <span data-ttu-id="c53e2-129">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-129">string</span></span>        | <span data-ttu-id="c53e2-130">Nom du principal de service à l’origine de la signature</span><span class="sxs-lookup"><span data-stu-id="c53e2-130">Name of the service principal that initiated the sign-in</span></span>                                                                                        |
| `ServicePrincipalId`   | <span data-ttu-id="c53e2-131">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-131">string</span></span>        | <span data-ttu-id="c53e2-132">Identificateur unique du principal de service à l’origine de la signature</span><span class="sxs-lookup"><span data-stu-id="c53e2-132">Unique identifier of the service principal that initiated the sign-in</span></span>                                                                           |
| `ResourceDisplayName`  | <span data-ttu-id="c53e2-133">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-133">string</span></span>        | <span data-ttu-id="c53e2-134">Nom d’affichage de la ressource accessible</span><span class="sxs-lookup"><span data-stu-id="c53e2-134">Display name of the resource accessed</span></span>                                                                                                           |
| `ResourceId`           | <span data-ttu-id="c53e2-135">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-135">string</span></span>        | <span data-ttu-id="c53e2-136">Identificateur unique de la ressource à accès</span><span class="sxs-lookup"><span data-stu-id="c53e2-136">Unique identifier of the resource accessed</span></span>                                                                                                      |
| `ResourceTenantId`     | <span data-ttu-id="c53e2-137">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-137">string</span></span>        | <span data-ttu-id="c53e2-138">Identificateur unique du client de la ressource à accès</span><span class="sxs-lookup"><span data-stu-id="c53e2-138">Unique identifier of the tenant of the resource accessed</span></span>                                                                                        |
| `IPAddress`            | <span data-ttu-id="c53e2-139">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-139">string</span></span>        | <span data-ttu-id="c53e2-140">Adresse IP attribuée au point de terminaison et utilisée lors des communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="c53e2-140">IP address assigned to the endpoint and used during related network communications</span></span>                                                              |
| `Country`          | <span data-ttu-id="c53e2-141">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-141">string</span></span>        | <span data-ttu-id="c53e2-142">Code à deux lettres indiquant le pays où l’adresse IP du client est géolocalisé</span><span class="sxs-lookup"><span data-stu-id="c53e2-142">Two-letter code indicating the country where the client IP address is geolocated</span></span>                                                                |
| `State`                | <span data-ttu-id="c53e2-143">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-143">string</span></span>        | <span data-ttu-id="c53e2-144">État où la se connecte s’est produite, si disponible</span><span class="sxs-lookup"><span data-stu-id="c53e2-144">State where the sign-in occurred, if available</span></span>                                                                                                  |
| `City`                 | <span data-ttu-id="c53e2-145">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-145">string</span></span>        | <span data-ttu-id="c53e2-146">Ville où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="c53e2-146">City where the account user is located</span></span>                                                                                                          |
| `Latitude`             | <span data-ttu-id="c53e2-147">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-147">string</span></span>        | <span data-ttu-id="c53e2-148">Coordonnées nord à sud de l’emplacement de la signature</span><span class="sxs-lookup"><span data-stu-id="c53e2-148">The north to south coordinates of the sign-in location</span></span>                                                                                          |
| `Longitude`            | <span data-ttu-id="c53e2-149">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-149">string</span></span>        | <span data-ttu-id="c53e2-150">Coordonnées est à ouest de l’emplacement de la signature</span><span class="sxs-lookup"><span data-stu-id="c53e2-150">The east to west coordinates of the sign-in location</span></span>                                                                                            |
| `RequestId`            | <span data-ttu-id="c53e2-151">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-151">string</span></span>        | <span data-ttu-id="c53e2-152">Identificateur unique de la demande</span><span class="sxs-lookup"><span data-stu-id="c53e2-152">Unique identifier of the request</span></span>                                                                                                                |
|`ReportId` | <span data-ttu-id="c53e2-153">string</span><span class="sxs-lookup"><span data-stu-id="c53e2-153">string</span></span> | <span data-ttu-id="c53e2-154">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="c53e2-154">Unique identifier for the event</span></span> | 

 

## <a name="related-articles"></a><span data-ttu-id="c53e2-155">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="c53e2-155">Related articles</span></span>

-   [<span data-ttu-id="c53e2-156">AADSignInEventsBeta</span><span class="sxs-lookup"><span data-stu-id="c53e2-156">AADSignInEventsBeta</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/advanced-hunting-aadsignineventsbeta-table)
-   [<span data-ttu-id="c53e2-157">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c53e2-157">Advanced hunting overview</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-overview)
-   [<span data-ttu-id="c53e2-158">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="c53e2-158">Learn the query language</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-query-language)
-   [<span data-ttu-id="c53e2-159">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="c53e2-159">Understand the schema</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference)

