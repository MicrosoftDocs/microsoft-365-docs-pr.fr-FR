---
title: Table IdentityInfo dans le schéma de recherche avancé
description: En savoir plus sur les informations de compte d'utilisateur dans la table IdentityInfo du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, AccountInfo, IdentityInfo, account
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
ms.openlocfilehash: ce1a3d5153d324d008d2d46048838351eb7bc047
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935820"
---
# <a name="identityinfo"></a><span data-ttu-id="08841-104">IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="08841-104">IdentityInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="08841-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="08841-105">**Applies to:**</span></span>
- <span data-ttu-id="08841-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="08841-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="08841-107">Le tableau du schéma de recherche avancée contient des informations sur les comptes d'utilisateurs obtenus à partir de `IdentityInfo` différents services, y compris Azure Active [](advanced-hunting-overview.md) Directory.</span><span class="sxs-lookup"><span data-stu-id="08841-107">The `IdentityInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about user accounts obtained from various services, including Azure Active Directory.</span></span> <span data-ttu-id="08841-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="08841-108">Use this reference to construct queries that return information from this table.</span></span>

>[!NOTE]
><span data-ttu-id="08841-109">Cette table a été renommée à partir `AccountInfo` de .</span><span class="sxs-lookup"><span data-stu-id="08841-109">This table was renamed from `AccountInfo`.</span></span> <span data-ttu-id="08841-110">Pendant les changements de nom, toutes les requêtes enregistrées dans le portail sont automatiquement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="08841-110">During renames, all queries saved in the portal are automatically updated.</span></span> <span data-ttu-id="08841-111">Vérifiez les requêtes que vous avez enregistrées ailleurs.</span><span class="sxs-lookup"><span data-stu-id="08841-111">Check queries you have saved elsewhere.</span></span>

<span data-ttu-id="08841-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="08841-112">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="08841-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="08841-113">Column name</span></span> | <span data-ttu-id="08841-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="08841-114">Data type</span></span> | <span data-ttu-id="08841-115">Description</span><span class="sxs-lookup"><span data-stu-id="08841-115">Description</span></span> |
|-------------|-----------|-------------|
| `AccountObjectId` | <span data-ttu-id="08841-116">string</span><span class="sxs-lookup"><span data-stu-id="08841-116">string</span></span> | <span data-ttu-id="08841-117">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="08841-117">Unique identifier for the account in Azure AD</span></span> |
| `AccountUpn` | <span data-ttu-id="08841-118">string</span><span class="sxs-lookup"><span data-stu-id="08841-118">string</span></span> | <span data-ttu-id="08841-119">Nom d'utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="08841-119">User principal name (UPN) of the account</span></span> |
| `OnPremSid` | <span data-ttu-id="08841-120">string</span><span class="sxs-lookup"><span data-stu-id="08841-120">string</span></span> | <span data-ttu-id="08841-121">Identificateur de sécurité local (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="08841-121">On-premises security identifier (SID) of the account</span></span> |
| `CloudSid` | <span data-ttu-id="08841-122">string</span><span class="sxs-lookup"><span data-stu-id="08841-122">string</span></span> | <span data-ttu-id="08841-123">Identificateur de sécurité cloud du compte</span><span class="sxs-lookup"><span data-stu-id="08841-123">Cloud security identifier of the account</span></span> |
| `GivenName` | <span data-ttu-id="08841-124">string</span><span class="sxs-lookup"><span data-stu-id="08841-124">string</span></span> | <span data-ttu-id="08841-125">Prénom ou nom de l'utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="08841-125">Given name or first name of the account user</span></span> |
| `Surname` | <span data-ttu-id="08841-126">string</span><span class="sxs-lookup"><span data-stu-id="08841-126">string</span></span> | <span data-ttu-id="08841-127">Nom de famille, nom de famille ou nom de l'utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="08841-127">Surname, family name, or last name of the account user</span></span> |
| `AccountDisplayName` | <span data-ttu-id="08841-128">string</span><span class="sxs-lookup"><span data-stu-id="08841-128">string</span></span> | <span data-ttu-id="08841-129">Nom de l'utilisateur du compte affiché dans le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="08841-129">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="08841-130">En règle générale, une combinaison d'un prénom ou d'un prénom donné, d'une initiation intermédiaire et d'un nom ou d'un nom de famille.</span><span class="sxs-lookup"><span data-stu-id="08841-130">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `Department` | <span data-ttu-id="08841-131">string</span><span class="sxs-lookup"><span data-stu-id="08841-131">string</span></span> | <span data-ttu-id="08841-132">Nom du service à qui appartient l'utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="08841-132">Name of the department that the account user belongs to</span></span> |
| `JobTitle` | <span data-ttu-id="08841-133">string</span><span class="sxs-lookup"><span data-stu-id="08841-133">string</span></span> | <span data-ttu-id="08841-134">Fonction de l'utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="08841-134">Job title of the account user</span></span> |
| `AccountName` | <span data-ttu-id="08841-135">string</span><span class="sxs-lookup"><span data-stu-id="08841-135">string</span></span> | <span data-ttu-id="08841-136">Nom d'utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="08841-136">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="08841-137">string</span><span class="sxs-lookup"><span data-stu-id="08841-137">string</span></span> | <span data-ttu-id="08841-138">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="08841-138">Domain of the account</span></span> |
| `EmailAddress` | <span data-ttu-id="08841-139">string</span><span class="sxs-lookup"><span data-stu-id="08841-139">string</span></span> | <span data-ttu-id="08841-140">Adresse SMTP du compte</span><span class="sxs-lookup"><span data-stu-id="08841-140">SMTP address of the account</span></span> |
| `SipProxyAddress` | <span data-ttu-id="08841-141">string</span><span class="sxs-lookup"><span data-stu-id="08841-141">string</span></span> | <span data-ttu-id="08841-142">Adresse SIP (Session Initiation Protocol) VOIP (Voice over IP) du compte</span><span class="sxs-lookup"><span data-stu-id="08841-142">Voice over IP (VOIP) session initiation protocol (SIP) address of the account</span></span> |
| `City` | <span data-ttu-id="08841-143">string</span><span class="sxs-lookup"><span data-stu-id="08841-143">string</span></span> | <span data-ttu-id="08841-144">Ville où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="08841-144">City where the account user is located</span></span> |
| `Country` | <span data-ttu-id="08841-145">string</span><span class="sxs-lookup"><span data-stu-id="08841-145">string</span></span> | <span data-ttu-id="08841-146">Pays/région où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="08841-146">Country/Region where the account user is located</span></span> |
| `IsAccountEnabled` | <span data-ttu-id="08841-147">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="08841-147">boolean</span></span> | <span data-ttu-id="08841-148">Indique si le compte est activé ou non</span><span class="sxs-lookup"><span data-stu-id="08841-148">Indicates whether the account is enabled or not</span></span> |

## <a name="related-topics"></a><span data-ttu-id="08841-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08841-149">Related topics</span></span>
- [<span data-ttu-id="08841-150">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="08841-150">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="08841-151">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="08841-151">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="08841-152">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="08841-152">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="08841-153">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="08841-153">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="08841-154">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="08841-154">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="08841-155">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="08841-155">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
