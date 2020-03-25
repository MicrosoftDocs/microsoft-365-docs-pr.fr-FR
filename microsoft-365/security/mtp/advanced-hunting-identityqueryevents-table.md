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
ms.openlocfilehash: b2fc94d6ac6606c97b4824bc556b7299a2bd8ec7
ms.sourcegitcommit: 3b2fdf159d7dd962493a3838e3cf0cf429ee2bf2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "42929165"
---
# <a name="identityqueryevents"></a><span data-ttu-id="f283f-104">IdentityQueryEvents</span><span class="sxs-lookup"><span data-stu-id="f283f-104">IdentityQueryEvents</span></span>

<span data-ttu-id="f283f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f283f-105">**Applies to:**</span></span>
- <span data-ttu-id="f283f-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="f283f-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="f283f-107">Le `IdentityQueryEvents` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les requêtes exécutées sur des objets Active Directory, tels que les utilisateurs, les groupes, les appareils et les domaines.</span><span class="sxs-lookup"><span data-stu-id="f283f-107">The `IdentityQueryEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about queries performed against Active Directory objects, such as users, groups, devices, and domains.</span></span> <span data-ttu-id="f283f-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="f283f-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="f283f-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f283f-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="f283f-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="f283f-110">Column name</span></span> | <span data-ttu-id="f283f-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="f283f-111">Data type</span></span> | <span data-ttu-id="f283f-112">Description</span><span class="sxs-lookup"><span data-stu-id="f283f-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="f283f-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="f283f-113">datetime</span></span> | <span data-ttu-id="f283f-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="f283f-114">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="f283f-115">string</span><span class="sxs-lookup"><span data-stu-id="f283f-115">string</span></span> | <span data-ttu-id="f283f-116">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="f283f-116">Type of activity that triggered the event</span></span> |
| `Application` | <span data-ttu-id="f283f-117">string</span><span class="sxs-lookup"><span data-stu-id="f283f-117">string</span></span> | <span data-ttu-id="f283f-118">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="f283f-118">Application that performed the recorded action</span></span> |
| `Query` | <span data-ttu-id="f283f-119">string</span><span class="sxs-lookup"><span data-stu-id="f283f-119">string</span></span> | <span data-ttu-id="f283f-120">Type de requête : QueryGroup, QueryUser ou EnumerateUsers</span><span class="sxs-lookup"><span data-stu-id="f283f-120">Type of query: QueryGroup, QueryUser, or EnumerateUsers</span></span> |
| `QueryObject` | <span data-ttu-id="f283f-121">string</span><span class="sxs-lookup"><span data-stu-id="f283f-121">string</span></span> | <span data-ttu-id="f283f-122">Nom de l’utilisateur, du groupe, de l’appareil, du domaine ou de tout autre type d’entité interrogé.</span><span class="sxs-lookup"><span data-stu-id="f283f-122">Name of the user, group, device, domain, or any other entity type being queried</span></span> |
| `Protocol` | <span data-ttu-id="f283f-123">string</span><span class="sxs-lookup"><span data-stu-id="f283f-123">string</span></span> | <span data-ttu-id="f283f-124">Protocole utilisé pendant la communication</span><span class="sxs-lookup"><span data-stu-id="f283f-124">Protocol used during the communication</span></span> |
| `AccountName` | <span data-ttu-id="f283f-125">string</span><span class="sxs-lookup"><span data-stu-id="f283f-125">string</span></span> | <span data-ttu-id="f283f-126">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="f283f-126">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="f283f-127">string</span><span class="sxs-lookup"><span data-stu-id="f283f-127">string</span></span> | <span data-ttu-id="f283f-128">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="f283f-128">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="f283f-129">string</span><span class="sxs-lookup"><span data-stu-id="f283f-129">string</span></span> | <span data-ttu-id="f283f-130">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="f283f-130">User principal name (UPN) of the account</span></span> |
| `AccountSid` | <span data-ttu-id="f283f-131">string</span><span class="sxs-lookup"><span data-stu-id="f283f-131">string</span></span> | <span data-ttu-id="f283f-132">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="f283f-132">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="f283f-133">string</span><span class="sxs-lookup"><span data-stu-id="f283f-133">string</span></span> | <span data-ttu-id="f283f-134">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="f283f-134">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="f283f-135">string</span><span class="sxs-lookup"><span data-stu-id="f283f-135">string</span></span> | <span data-ttu-id="f283f-136">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f283f-136">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="f283f-137">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="f283f-137">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="f283f-138">string</span><span class="sxs-lookup"><span data-stu-id="f283f-138">string</span></span> | <span data-ttu-id="f283f-139">Nom de domaine complet (FQDN) du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f283f-139">Fully qualified domain name (FQDN) of the endpoint</span></span> |
| `IPAddress` | <span data-ttu-id="f283f-140">string</span><span class="sxs-lookup"><span data-stu-id="f283f-140">string</span></span> | <span data-ttu-id="f283f-141">Adresse IP affectée au point de terminaison et utilisée pendant les communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="f283f-141">IP address assigned to the endpoint and used during related network communications</span></span> |
| `Location` | <span data-ttu-id="f283f-142">string</span><span class="sxs-lookup"><span data-stu-id="f283f-142">string</span></span> | <span data-ttu-id="f283f-143">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="f283f-143">City, country, or other geographic location associated with the event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="f283f-144">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="f283f-144">Related topics</span></span>
- [<span data-ttu-id="f283f-145">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="f283f-145">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="f283f-146">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="f283f-146">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="f283f-147">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="f283f-147">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="f283f-148">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="f283f-148">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="f283f-149">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="f283f-149">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="f283f-150">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="f283f-150">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
