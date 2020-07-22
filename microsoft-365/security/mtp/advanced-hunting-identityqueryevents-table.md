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
ms.openlocfilehash: 436c4d7306f9f5febd614489090a0a10929ba3c9
ms.sourcegitcommit: b4119682bd3c036289e851fff56fde869c816479
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/22/2020
ms.locfileid: "45204874"
---
# <a name="identityqueryevents"></a><span data-ttu-id="0434a-104">IdentityQueryEvents</span><span class="sxs-lookup"><span data-stu-id="0434a-104">IdentityQueryEvents</span></span>

<span data-ttu-id="0434a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0434a-105">**Applies to:**</span></span>
- <span data-ttu-id="0434a-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0434a-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="0434a-107">Le `IdentityQueryEvents` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les requêtes exécutées sur des objets Active Directory, tels que les utilisateurs, les groupes, les appareils et les domaines.</span><span class="sxs-lookup"><span data-stu-id="0434a-107">The `IdentityQueryEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about queries performed against Active Directory objects, such as users, groups, devices, and domains.</span></span> <span data-ttu-id="0434a-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="0434a-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="0434a-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="0434a-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="0434a-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="0434a-110">Column name</span></span> | <span data-ttu-id="0434a-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="0434a-111">Data type</span></span> | <span data-ttu-id="0434a-112">Description</span><span class="sxs-lookup"><span data-stu-id="0434a-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="0434a-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="0434a-113">datetime</span></span> | <span data-ttu-id="0434a-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="0434a-114">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="0434a-115">string</span><span class="sxs-lookup"><span data-stu-id="0434a-115">string</span></span> | <span data-ttu-id="0434a-116">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="0434a-116">Type of activity that triggered the event</span></span> |
| `Application` | <span data-ttu-id="0434a-117">string</span><span class="sxs-lookup"><span data-stu-id="0434a-117">string</span></span> | <span data-ttu-id="0434a-118">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="0434a-118">Application that performed the recorded action</span></span> |
| `QueryType` | <span data-ttu-id="0434a-119">string</span><span class="sxs-lookup"><span data-stu-id="0434a-119">string</span></span> | <span data-ttu-id="0434a-120">Type de requête, tel que QueryGroup, QueryUser ou EnumerateUsers</span><span class="sxs-lookup"><span data-stu-id="0434a-120">Type of query, such as QueryGroup, QueryUser, or EnumerateUsers</span></span> |
| `QueryTarget` | <span data-ttu-id="0434a-121">string</span><span class="sxs-lookup"><span data-stu-id="0434a-121">string</span></span> | <span data-ttu-id="0434a-122">Nom de l’utilisateur, du groupe, de l’appareil, du domaine ou de tout autre type d’entité interrogé</span><span class="sxs-lookup"><span data-stu-id="0434a-122">Name of user, group, device, domain, or any other entity type being queried</span></span> |
| `Query` | <span data-ttu-id="0434a-123">string</span><span class="sxs-lookup"><span data-stu-id="0434a-123">string</span></span> | <span data-ttu-id="0434a-124">Chaîne utilisée pour exécuter la requête</span><span class="sxs-lookup"><span data-stu-id="0434a-124">String used to run the query</span></span> |
| `Protocol` | <span data-ttu-id="0434a-125">string</span><span class="sxs-lookup"><span data-stu-id="0434a-125">string</span></span> | <span data-ttu-id="0434a-126">Protocole utilisé pendant la communication</span><span class="sxs-lookup"><span data-stu-id="0434a-126">Protocol used during the communication</span></span> |
| `AccountName` | <span data-ttu-id="0434a-127">string</span><span class="sxs-lookup"><span data-stu-id="0434a-127">string</span></span> | <span data-ttu-id="0434a-128">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="0434a-128">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="0434a-129">string</span><span class="sxs-lookup"><span data-stu-id="0434a-129">string</span></span> | <span data-ttu-id="0434a-130">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="0434a-130">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="0434a-131">string</span><span class="sxs-lookup"><span data-stu-id="0434a-131">string</span></span> | <span data-ttu-id="0434a-132">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="0434a-132">User principal name (UPN) of the account</span></span> |
| `AccountSid` | <span data-ttu-id="0434a-133">string</span><span class="sxs-lookup"><span data-stu-id="0434a-133">string</span></span> | <span data-ttu-id="0434a-134">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="0434a-134">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="0434a-135">string</span><span class="sxs-lookup"><span data-stu-id="0434a-135">string</span></span> | <span data-ttu-id="0434a-136">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="0434a-136">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="0434a-137">string</span><span class="sxs-lookup"><span data-stu-id="0434a-137">string</span></span> | <span data-ttu-id="0434a-138">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="0434a-138">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="0434a-139">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="0434a-139">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="0434a-140">string</span><span class="sxs-lookup"><span data-stu-id="0434a-140">string</span></span> | <span data-ttu-id="0434a-141">Nom de domaine complet (FQDN) du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0434a-141">Fully qualified domain name (FQDN) of the endpoint</span></span> |
| `IPAddress` | <span data-ttu-id="0434a-142">string</span><span class="sxs-lookup"><span data-stu-id="0434a-142">string</span></span> | <span data-ttu-id="0434a-143">Adresse IP affectée au point de terminaison et utilisée pendant les communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="0434a-143">IP address assigned to the endpoint and used during related network communications</span></span> |
| `DestinationDeviceName` | <span data-ttu-id="0434a-144">string</span><span class="sxs-lookup"><span data-stu-id="0434a-144">string</span></span> | <span data-ttu-id="0434a-145">Nom de l’appareil exécutant l’application serveur qui a traité l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="0434a-145">Name of the device running the server application that processed the recorded action</span></span> |
| `DestinationIPAddress` | <span data-ttu-id="0434a-146">string</span><span class="sxs-lookup"><span data-stu-id="0434a-146">string</span></span> | <span data-ttu-id="0434a-147">Adresse IP de l’appareil exécutant l’application serveur qui a traité l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="0434a-147">IP address of the device running the server application that processed the recorded action</span></span> |
| `TargetDeviceName` | <span data-ttu-id="0434a-148">string</span><span class="sxs-lookup"><span data-stu-id="0434a-148">string</span></span> | <span data-ttu-id="0434a-149">Nom de domaine complet (FQDN) de l’appareil sur lequel l’action enregistrée a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="0434a-149">Fully qualified domain name (FQDN) of the device that the recorded action was applied to</span></span> |
| `TargetAccountUpn` | <span data-ttu-id="0434a-150">string</span><span class="sxs-lookup"><span data-stu-id="0434a-150">string</span></span> | <span data-ttu-id="0434a-151">Nom d’utilisateur principal (UPN) du compte auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="0434a-151">User principal name (UPN) of the account that the recorded action was applied to</span></span> |
| `TargetAccountDisplayName` | <span data-ttu-id="0434a-152">string</span><span class="sxs-lookup"><span data-stu-id="0434a-152">string</span></span> | <span data-ttu-id="0434a-153">Nom d’affichage du compte auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="0434a-153">Display name of the account that the recorded action was applied to</span></span> |
| `Location` | <span data-ttu-id="0434a-154">string</span><span class="sxs-lookup"><span data-stu-id="0434a-154">string</span></span> | <span data-ttu-id="0434a-155">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="0434a-155">City, country, or other geographic location associated with the event</span></span> |
| `ReportId` | <span data-ttu-id="0434a-156">long</span><span class="sxs-lookup"><span data-stu-id="0434a-156">long</span></span> | <span data-ttu-id="0434a-157">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="0434a-157">Unique identifier for the event</span></span> |
| `AdditionalFields` | <span data-ttu-id="0434a-158">string</span><span class="sxs-lookup"><span data-stu-id="0434a-158">string</span></span> | <span data-ttu-id="0434a-159">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="0434a-159">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="0434a-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0434a-160">Related topics</span></span>
- [<span data-ttu-id="0434a-161">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="0434a-161">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="0434a-162">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="0434a-162">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="0434a-163">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="0434a-163">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="0434a-164">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="0434a-164">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="0434a-165">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="0434a-165">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="0434a-166">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="0434a-166">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
