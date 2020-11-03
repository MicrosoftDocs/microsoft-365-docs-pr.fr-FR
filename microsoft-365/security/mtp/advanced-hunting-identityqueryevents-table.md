---
title: Table IdentityQueryEvents dans le schéma de chasse avancé
description: En savoir plus sur les événements de requête Active Directory dans la table IdentityQueryEvents du schéma de chasse avancé
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, IdentityQueryEvents, Azure AD, Active Directory, Azure ATP, identités, requêtes LDAP
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.openlocfilehash: 2b163dc39e56c82ef177b71d197c431c744b12d7
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48847403"
---
# <a name="identityqueryevents"></a><span data-ttu-id="8bfec-104">IdentityQueryEvents</span><span class="sxs-lookup"><span data-stu-id="8bfec-104">IdentityQueryEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="8bfec-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8bfec-105">**Applies to:**</span></span>
- <span data-ttu-id="8bfec-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8bfec-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="8bfec-107">Le `IdentityQueryEvents` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les requêtes exécutées sur des objets Active Directory, tels que les utilisateurs, les groupes, les appareils et les domaines.</span><span class="sxs-lookup"><span data-stu-id="8bfec-107">The `IdentityQueryEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about queries performed against Active Directory objects, such as users, groups, devices, and domains.</span></span> <span data-ttu-id="8bfec-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="8bfec-108">Use this reference to construct queries that return information from this table.</span></span>

>[!TIP]
> <span data-ttu-id="8bfec-109">Pour plus d’informations sur les types d’événements ( `ActionType` valeurs) pris en charge par un tableau, utilisez la [référence de schéma intégrée](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) disponible dans le centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8bfec-109">For detailed information about the events types (`ActionType` values) supported by a table, use the [built-in schema reference](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) available in the security center.</span></span>

<span data-ttu-id="8bfec-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8bfec-110">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="8bfec-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="8bfec-111">Column name</span></span> | <span data-ttu-id="8bfec-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="8bfec-112">Data type</span></span> | <span data-ttu-id="8bfec-113">Description</span><span class="sxs-lookup"><span data-stu-id="8bfec-113">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="8bfec-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="8bfec-114">datetime</span></span> | <span data-ttu-id="8bfec-115">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="8bfec-115">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="8bfec-116">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-116">string</span></span> | <span data-ttu-id="8bfec-117">Type d’activité qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="8bfec-117">Type of activity that triggered the event.</span></span> <span data-ttu-id="8bfec-118">Pour plus d’informations, consultez la [référence de schéma dans le portail](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) .</span><span class="sxs-lookup"><span data-stu-id="8bfec-118">See the [in-portal schema reference](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) for details</span></span> |
| `Application` | <span data-ttu-id="8bfec-119">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-119">string</span></span> | <span data-ttu-id="8bfec-120">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="8bfec-120">Application that performed the recorded action</span></span> |
| `QueryType` | <span data-ttu-id="8bfec-121">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-121">string</span></span> | <span data-ttu-id="8bfec-122">Type de requête, tel que QueryGroup, QueryUser ou EnumerateUsers</span><span class="sxs-lookup"><span data-stu-id="8bfec-122">Type of query, such as QueryGroup, QueryUser, or EnumerateUsers</span></span> |
| `QueryTarget` | <span data-ttu-id="8bfec-123">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-123">string</span></span> | <span data-ttu-id="8bfec-124">Nom de l’utilisateur, du groupe, de l’appareil, du domaine ou de tout autre type d’entité interrogé</span><span class="sxs-lookup"><span data-stu-id="8bfec-124">Name of user, group, device, domain, or any other entity type being queried</span></span> |
| `Query` | <span data-ttu-id="8bfec-125">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-125">string</span></span> | <span data-ttu-id="8bfec-126">Chaîne utilisée pour exécuter la requête</span><span class="sxs-lookup"><span data-stu-id="8bfec-126">String used to run the query</span></span> |
| `Protocol` | <span data-ttu-id="8bfec-127">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-127">string</span></span> | <span data-ttu-id="8bfec-128">Protocole utilisé pendant la communication</span><span class="sxs-lookup"><span data-stu-id="8bfec-128">Protocol used during the communication</span></span> |
| `AccountName` | <span data-ttu-id="8bfec-129">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-129">string</span></span> | <span data-ttu-id="8bfec-130">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="8bfec-130">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="8bfec-131">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-131">string</span></span> | <span data-ttu-id="8bfec-132">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="8bfec-132">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="8bfec-133">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-133">string</span></span> | <span data-ttu-id="8bfec-134">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="8bfec-134">User principal name (UPN) of the account</span></span> |
| `AccountSid` | <span data-ttu-id="8bfec-135">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-135">string</span></span> | <span data-ttu-id="8bfec-136">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="8bfec-136">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="8bfec-137">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-137">string</span></span> | <span data-ttu-id="8bfec-138">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="8bfec-138">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="8bfec-139">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-139">string</span></span> | <span data-ttu-id="8bfec-140">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="8bfec-140">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="8bfec-141">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="8bfec-141">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="8bfec-142">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-142">string</span></span> | <span data-ttu-id="8bfec-143">Nom de domaine complet (FQDN) du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8bfec-143">Fully qualified domain name (FQDN) of the endpoint</span></span> |
| `IPAddress` | <span data-ttu-id="8bfec-144">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-144">string</span></span> | <span data-ttu-id="8bfec-145">Adresse IP affectée au point de terminaison et utilisée pendant les communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="8bfec-145">IP address assigned to the endpoint and used during related network communications</span></span> |
| `DestinationDeviceName` | <span data-ttu-id="8bfec-146">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-146">string</span></span> | <span data-ttu-id="8bfec-147">Nom de l’appareil exécutant l’application serveur qui a traité l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="8bfec-147">Name of the device running the server application that processed the recorded action</span></span> |
| `DestinationIPAddress` | <span data-ttu-id="8bfec-148">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-148">string</span></span> | <span data-ttu-id="8bfec-149">Adresse IP de l’appareil exécutant l’application serveur qui a traité l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="8bfec-149">IP address of the device running the server application that processed the recorded action</span></span> |
| `TargetDeviceName` | <span data-ttu-id="8bfec-150">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-150">string</span></span> | <span data-ttu-id="8bfec-151">Nom de domaine complet (FQDN) de l’appareil sur lequel l’action enregistrée a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="8bfec-151">Fully qualified domain name (FQDN) of the device that the recorded action was applied to</span></span> |
| `TargetAccountUpn` | <span data-ttu-id="8bfec-152">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-152">string</span></span> | <span data-ttu-id="8bfec-153">Nom d’utilisateur principal (UPN) du compte auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="8bfec-153">User principal name (UPN) of the account that the recorded action was applied to</span></span> |
| `TargetAccountDisplayName` | <span data-ttu-id="8bfec-154">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-154">string</span></span> | <span data-ttu-id="8bfec-155">Nom d’affichage du compte auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="8bfec-155">Display name of the account that the recorded action was applied to</span></span> |
| `Location` | <span data-ttu-id="8bfec-156">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-156">string</span></span> | <span data-ttu-id="8bfec-157">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="8bfec-157">City, country, or other geographic location associated with the event</span></span> |
| `ReportId` | <span data-ttu-id="8bfec-158">long</span><span class="sxs-lookup"><span data-stu-id="8bfec-158">long</span></span> | <span data-ttu-id="8bfec-159">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="8bfec-159">Unique identifier for the event</span></span> |
| `AdditionalFields` | <span data-ttu-id="8bfec-160">string</span><span class="sxs-lookup"><span data-stu-id="8bfec-160">string</span></span> | <span data-ttu-id="8bfec-161">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="8bfec-161">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="8bfec-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bfec-162">Related topics</span></span>
- [<span data-ttu-id="8bfec-163">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="8bfec-163">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="8bfec-164">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="8bfec-164">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="8bfec-165">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="8bfec-165">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="8bfec-166">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="8bfec-166">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="8bfec-167">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="8bfec-167">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="8bfec-168">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="8bfec-168">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
