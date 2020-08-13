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
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: cf2038a15242139817eb073ec2a6408905824123
ms.sourcegitcommit: 51097b18d94da20aa727ebfbeb6ec84c263b25c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/12/2020
ms.locfileid: "46649318"
---
# <a name="identityqueryevents"></a><span data-ttu-id="629d9-104">IdentityQueryEvents</span><span class="sxs-lookup"><span data-stu-id="629d9-104">IdentityQueryEvents</span></span>

<span data-ttu-id="629d9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="629d9-105">**Applies to:**</span></span>
- <span data-ttu-id="629d9-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="629d9-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="629d9-107">Le `IdentityQueryEvents` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les requêtes exécutées sur des objets Active Directory, tels que les utilisateurs, les groupes, les appareils et les domaines.</span><span class="sxs-lookup"><span data-stu-id="629d9-107">The `IdentityQueryEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about queries performed against Active Directory objects, such as users, groups, devices, and domains.</span></span> <span data-ttu-id="629d9-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="629d9-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="629d9-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="629d9-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="629d9-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="629d9-110">Column name</span></span> | <span data-ttu-id="629d9-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="629d9-111">Data type</span></span> | <span data-ttu-id="629d9-112">Description</span><span class="sxs-lookup"><span data-stu-id="629d9-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="629d9-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="629d9-113">datetime</span></span> | <span data-ttu-id="629d9-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="629d9-114">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="629d9-115">string</span><span class="sxs-lookup"><span data-stu-id="629d9-115">string</span></span> | <span data-ttu-id="629d9-116">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="629d9-116">Type of activity that triggered the event</span></span> |
| `Application` | <span data-ttu-id="629d9-117">string</span><span class="sxs-lookup"><span data-stu-id="629d9-117">string</span></span> | <span data-ttu-id="629d9-118">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="629d9-118">Application that performed the recorded action</span></span> |
| `QueryType` | <span data-ttu-id="629d9-119">string</span><span class="sxs-lookup"><span data-stu-id="629d9-119">string</span></span> | <span data-ttu-id="629d9-120">Type de requête, tel que QueryGroup, QueryUser ou EnumerateUsers</span><span class="sxs-lookup"><span data-stu-id="629d9-120">Type of query, such as QueryGroup, QueryUser, or EnumerateUsers</span></span> |
| `QueryTarget` | <span data-ttu-id="629d9-121">string</span><span class="sxs-lookup"><span data-stu-id="629d9-121">string</span></span> | <span data-ttu-id="629d9-122">Nom de l’utilisateur, du groupe, de l’appareil, du domaine ou de tout autre type d’entité interrogé</span><span class="sxs-lookup"><span data-stu-id="629d9-122">Name of user, group, device, domain, or any other entity type being queried</span></span> |
| `Query` | <span data-ttu-id="629d9-123">string</span><span class="sxs-lookup"><span data-stu-id="629d9-123">string</span></span> | <span data-ttu-id="629d9-124">Chaîne utilisée pour exécuter la requête</span><span class="sxs-lookup"><span data-stu-id="629d9-124">String used to run the query</span></span> |
| `Protocol` | <span data-ttu-id="629d9-125">string</span><span class="sxs-lookup"><span data-stu-id="629d9-125">string</span></span> | <span data-ttu-id="629d9-126">Protocole utilisé pendant la communication</span><span class="sxs-lookup"><span data-stu-id="629d9-126">Protocol used during the communication</span></span> |
| `AccountName` | <span data-ttu-id="629d9-127">string</span><span class="sxs-lookup"><span data-stu-id="629d9-127">string</span></span> | <span data-ttu-id="629d9-128">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="629d9-128">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="629d9-129">string</span><span class="sxs-lookup"><span data-stu-id="629d9-129">string</span></span> | <span data-ttu-id="629d9-130">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="629d9-130">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="629d9-131">string</span><span class="sxs-lookup"><span data-stu-id="629d9-131">string</span></span> | <span data-ttu-id="629d9-132">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="629d9-132">User principal name (UPN) of the account</span></span> |
| `AccountSid` | <span data-ttu-id="629d9-133">string</span><span class="sxs-lookup"><span data-stu-id="629d9-133">string</span></span> | <span data-ttu-id="629d9-134">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="629d9-134">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="629d9-135">string</span><span class="sxs-lookup"><span data-stu-id="629d9-135">string</span></span> | <span data-ttu-id="629d9-136">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="629d9-136">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="629d9-137">string</span><span class="sxs-lookup"><span data-stu-id="629d9-137">string</span></span> | <span data-ttu-id="629d9-138">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="629d9-138">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="629d9-139">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="629d9-139">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="629d9-140">string</span><span class="sxs-lookup"><span data-stu-id="629d9-140">string</span></span> | <span data-ttu-id="629d9-141">Nom de domaine complet (FQDN) du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="629d9-141">Fully qualified domain name (FQDN) of the endpoint</span></span> |
| `IPAddress` | <span data-ttu-id="629d9-142">string</span><span class="sxs-lookup"><span data-stu-id="629d9-142">string</span></span> | <span data-ttu-id="629d9-143">Adresse IP affectée au point de terminaison et utilisée pendant les communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="629d9-143">IP address assigned to the endpoint and used during related network communications</span></span> |
| `DestinationDeviceName` | <span data-ttu-id="629d9-144">string</span><span class="sxs-lookup"><span data-stu-id="629d9-144">string</span></span> | <span data-ttu-id="629d9-145">Nom de l’appareil exécutant l’application serveur qui a traité l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="629d9-145">Name of the device running the server application that processed the recorded action</span></span> |
| `DestinationIPAddress` | <span data-ttu-id="629d9-146">string</span><span class="sxs-lookup"><span data-stu-id="629d9-146">string</span></span> | <span data-ttu-id="629d9-147">Adresse IP de l’appareil exécutant l’application serveur qui a traité l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="629d9-147">IP address of the device running the server application that processed the recorded action</span></span> |
| `TargetDeviceName` | <span data-ttu-id="629d9-148">string</span><span class="sxs-lookup"><span data-stu-id="629d9-148">string</span></span> | <span data-ttu-id="629d9-149">Nom de domaine complet (FQDN) de l’appareil sur lequel l’action enregistrée a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="629d9-149">Fully qualified domain name (FQDN) of the device that the recorded action was applied to</span></span> |
| `TargetAccountUpn` | <span data-ttu-id="629d9-150">string</span><span class="sxs-lookup"><span data-stu-id="629d9-150">string</span></span> | <span data-ttu-id="629d9-151">Nom d’utilisateur principal (UPN) du compte auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="629d9-151">User principal name (UPN) of the account that the recorded action was applied to</span></span> |
| `TargetAccountDisplayName` | <span data-ttu-id="629d9-152">string</span><span class="sxs-lookup"><span data-stu-id="629d9-152">string</span></span> | <span data-ttu-id="629d9-153">Nom d’affichage du compte auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="629d9-153">Display name of the account that the recorded action was applied to</span></span> |
| `Location` | <span data-ttu-id="629d9-154">string</span><span class="sxs-lookup"><span data-stu-id="629d9-154">string</span></span> | <span data-ttu-id="629d9-155">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="629d9-155">City, country, or other geographic location associated with the event</span></span> |
| `ReportId` | <span data-ttu-id="629d9-156">long</span><span class="sxs-lookup"><span data-stu-id="629d9-156">long</span></span> | <span data-ttu-id="629d9-157">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="629d9-157">Unique identifier for the event</span></span> |
| `AdditionalFields` | <span data-ttu-id="629d9-158">string</span><span class="sxs-lookup"><span data-stu-id="629d9-158">string</span></span> | <span data-ttu-id="629d9-159">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="629d9-159">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="629d9-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="629d9-160">Related topics</span></span>
- [<span data-ttu-id="629d9-161">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="629d9-161">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="629d9-162">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="629d9-162">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="629d9-163">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="629d9-163">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="629d9-164">Recherche sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="629d9-164">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="629d9-165">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="629d9-165">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="629d9-166">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="629d9-166">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
