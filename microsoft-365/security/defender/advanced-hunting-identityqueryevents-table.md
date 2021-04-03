---
title: Table IdentityQueryEvents dans le schéma de recherche avancé
description: En savoir plus sur les événements de requête Active Directory dans la table IdentityQueryEvents du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, IdentityQueryEvents, Azure AD, Active Directory, Azure ATP, identities, LDAP queries
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
ms.openlocfilehash: 40383524ffe26326800369570856499d149e31c3
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500393"
---
# <a name="identityqueryevents"></a><span data-ttu-id="f53d2-104">IdentityQueryEvents</span><span class="sxs-lookup"><span data-stu-id="f53d2-104">IdentityQueryEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="f53d2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f53d2-105">**Applies to:**</span></span>
- <span data-ttu-id="f53d2-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f53d2-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="f53d2-107">Le tableau du schéma de recherche avancée contient des informations sur les requêtes effectuées sur des objets Active Directory, tels que des utilisateurs, des groupes, des appareils et `IdentityQueryEvents` des domaines. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="f53d2-107">The `IdentityQueryEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about queries performed against Active Directory objects, such as users, groups, devices, and domains.</span></span> <span data-ttu-id="f53d2-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="f53d2-108">Use this reference to construct queries that return information from this table.</span></span>

>[!TIP]
> <span data-ttu-id="f53d2-109">Pour plus d’informations sur les types d’événements (valeurs) pris en charge par une table, utilisez la référence de schéma intégrée disponible `ActionType` dans le centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f53d2-109">For detailed information about the events types (`ActionType` values) supported by a table, use the built-in schema reference available in the security center.</span></span>

<span data-ttu-id="f53d2-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f53d2-110">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="f53d2-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="f53d2-111">Column name</span></span> | <span data-ttu-id="f53d2-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="f53d2-112">Data type</span></span> | <span data-ttu-id="f53d2-113">Description</span><span class="sxs-lookup"><span data-stu-id="f53d2-113">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="f53d2-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="f53d2-114">datetime</span></span> | <span data-ttu-id="f53d2-115">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="f53d2-115">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="f53d2-116">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-116">string</span></span> | <span data-ttu-id="f53d2-117">Type d’activité qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="f53d2-117">Type of activity that triggered the event.</span></span> <span data-ttu-id="f53d2-118">Pour plus [d’informations, voir](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) la référence du schéma dans le portail</span><span class="sxs-lookup"><span data-stu-id="f53d2-118">See the [in-portal schema reference](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) for details</span></span> |
| `Application` | <span data-ttu-id="f53d2-119">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-119">string</span></span> | <span data-ttu-id="f53d2-120">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="f53d2-120">Application that performed the recorded action</span></span> |
| `QueryType` | <span data-ttu-id="f53d2-121">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-121">string</span></span> | <span data-ttu-id="f53d2-122">Type de requête, tel que QueryGroup, QueryUser ou EnumerateUsers</span><span class="sxs-lookup"><span data-stu-id="f53d2-122">Type of query, such as QueryGroup, QueryUser, or EnumerateUsers</span></span> |
| `QueryTarget` | <span data-ttu-id="f53d2-123">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-123">string</span></span> | <span data-ttu-id="f53d2-124">Nom de l’utilisateur, du groupe, de l’appareil, du domaine ou tout autre type d’entité interrogé</span><span class="sxs-lookup"><span data-stu-id="f53d2-124">Name of user, group, device, domain, or any other entity type being queried</span></span> |
| `Query` | <span data-ttu-id="f53d2-125">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-125">string</span></span> | <span data-ttu-id="f53d2-126">Chaîne utilisée pour exécuter la requête</span><span class="sxs-lookup"><span data-stu-id="f53d2-126">String used to run the query</span></span> |
| `Protocol` | <span data-ttu-id="f53d2-127">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-127">string</span></span> | <span data-ttu-id="f53d2-128">Protocole utilisé pendant la communication</span><span class="sxs-lookup"><span data-stu-id="f53d2-128">Protocol used during the communication</span></span> |
| `AccountName` | <span data-ttu-id="f53d2-129">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-129">string</span></span> | <span data-ttu-id="f53d2-130">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="f53d2-130">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="f53d2-131">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-131">string</span></span> | <span data-ttu-id="f53d2-132">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="f53d2-132">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="f53d2-133">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-133">string</span></span> | <span data-ttu-id="f53d2-134">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="f53d2-134">User principal name (UPN) of the account</span></span> |
| `AccountSid` | <span data-ttu-id="f53d2-135">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-135">string</span></span> | <span data-ttu-id="f53d2-136">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="f53d2-136">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="f53d2-137">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-137">string</span></span> | <span data-ttu-id="f53d2-138">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="f53d2-138">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="f53d2-139">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-139">string</span></span> | <span data-ttu-id="f53d2-140">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f53d2-140">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="f53d2-141">En règle générale, une combinaison d’un prénom ou d’un prénom donné, d’une initiation intermédiaire et d’un nom ou d’un nom de famille.</span><span class="sxs-lookup"><span data-stu-id="f53d2-141">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="f53d2-142">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-142">string</span></span> | <span data-ttu-id="f53d2-143">Nom de domaine complet (FQDN) du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f53d2-143">Fully qualified domain name (FQDN) of the endpoint</span></span> |
| `IPAddress` | <span data-ttu-id="f53d2-144">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-144">string</span></span> | <span data-ttu-id="f53d2-145">Adresse IP attribuée au point de terminaison et utilisée lors des communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="f53d2-145">IP address assigned to the endpoint and used during related network communications</span></span> |
| `Port` | <span data-ttu-id="f53d2-146">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-146">string</span></span> | <span data-ttu-id="f53d2-147">Port TCP utilisé pendant la communication</span><span class="sxs-lookup"><span data-stu-id="f53d2-147">TCP port used during communication</span></span> |
| `DestinationDeviceName` | <span data-ttu-id="f53d2-148">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-148">string</span></span> | <span data-ttu-id="f53d2-149">Nom de l’appareil exécutant l’application serveur qui a traitée l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="f53d2-149">Name of the device running the server application that processed the recorded action</span></span> |
| `DestinationIPAddress` | <span data-ttu-id="f53d2-150">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-150">string</span></span> | <span data-ttu-id="f53d2-151">Adresse IP de l’appareil exécutant l’application serveur qui a traitée l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="f53d2-151">IP address of the device running the server application that processed the recorded action</span></span> |
| `DestinationPort` | <span data-ttu-id="f53d2-152">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-152">string</span></span> | <span data-ttu-id="f53d2-153">Port de destination des communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="f53d2-153">Destination port of related network communications</span></span> |
| `TargetDeviceName` | <span data-ttu-id="f53d2-154">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-154">string</span></span> | <span data-ttu-id="f53d2-155">Nom de domaine complet (FQDN) de l’appareil à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="f53d2-155">Fully qualified domain name (FQDN) of the device that the recorded action was applied to</span></span> |
| `TargetAccountUpn` | <span data-ttu-id="f53d2-156">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-156">string</span></span> | <span data-ttu-id="f53d2-157">Nom d’utilisateur principal (UPN) du compte à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="f53d2-157">User principal name (UPN) of the account that the recorded action was applied to</span></span> |
| `TargetAccountDisplayName` | <span data-ttu-id="f53d2-158">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-158">string</span></span> | <span data-ttu-id="f53d2-159">Nom complet du compte à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="f53d2-159">Display name of the account that the recorded action was applied to</span></span> |
| `Location` | <span data-ttu-id="f53d2-160">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-160">string</span></span> | <span data-ttu-id="f53d2-161">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="f53d2-161">City, country, or other geographic location associated with the event</span></span> |
| `ReportId` | <span data-ttu-id="f53d2-162">long</span><span class="sxs-lookup"><span data-stu-id="f53d2-162">long</span></span> | <span data-ttu-id="f53d2-163">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="f53d2-163">Unique identifier for the event</span></span> |
| `AdditionalFields` | <span data-ttu-id="f53d2-164">string</span><span class="sxs-lookup"><span data-stu-id="f53d2-164">string</span></span> | <span data-ttu-id="f53d2-165">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="f53d2-165">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="f53d2-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f53d2-166">Related topics</span></span>
- [<span data-ttu-id="f53d2-167">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="f53d2-167">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="f53d2-168">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="f53d2-168">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="f53d2-169">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="f53d2-169">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="f53d2-170">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="f53d2-170">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="f53d2-171">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="f53d2-171">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="f53d2-172">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="f53d2-172">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
