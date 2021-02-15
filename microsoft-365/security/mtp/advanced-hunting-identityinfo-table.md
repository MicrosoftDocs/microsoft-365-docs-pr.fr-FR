---
title: Table IdentityInfo dans le schéma de recherche avancé
description: En savoir plus sur les informations de compte d’utilisateur dans la table IdentityInfo du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, AccountInfo, IdentityInfo, account
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
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
ms.technology: m365d
ms.openlocfilehash: 6604e6d48e277e840b87ddc461580bcb69dd1bc7
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49929909"
---
# <a name="identityinfo"></a><span data-ttu-id="acc57-104">IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="acc57-104">IdentityInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="acc57-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="acc57-105">**Applies to:**</span></span>
- <span data-ttu-id="acc57-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="acc57-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="acc57-107">Le tableau du schéma de recherche avancée contient des informations sur les comptes d’utilisateurs obtenus à partir de différents services, y compris `IdentityInfo` Azure Active [](advanced-hunting-overview.md) Directory.</span><span class="sxs-lookup"><span data-stu-id="acc57-107">The `IdentityInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about user accounts obtained from various services, including Azure Active Directory.</span></span> <span data-ttu-id="acc57-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="acc57-108">Use this reference to construct queries that return information from this table.</span></span>

>[!NOTE]
><span data-ttu-id="acc57-109">Cette table a été renommée à partir `AccountInfo` de .</span><span class="sxs-lookup"><span data-stu-id="acc57-109">This table was renamed from `AccountInfo`.</span></span> <span data-ttu-id="acc57-110">Pendant les changements de nom, toutes les requêtes enregistrées dans le portail sont automatiquement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="acc57-110">During renames, all queries saved in the portal are automatically updated.</span></span> <span data-ttu-id="acc57-111">Vérifiez les requêtes que vous avez enregistrées ailleurs.</span><span class="sxs-lookup"><span data-stu-id="acc57-111">Check queries you have saved elsewhere.</span></span>

<span data-ttu-id="acc57-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="acc57-112">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="acc57-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="acc57-113">Column name</span></span> | <span data-ttu-id="acc57-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="acc57-114">Data type</span></span> | <span data-ttu-id="acc57-115">Description</span><span class="sxs-lookup"><span data-stu-id="acc57-115">Description</span></span> |
|-------------|-----------|-------------|
| `AccountObjectId` | <span data-ttu-id="acc57-116">string</span><span class="sxs-lookup"><span data-stu-id="acc57-116">string</span></span> | <span data-ttu-id="acc57-117">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="acc57-117">Unique identifier for the account in Azure AD</span></span> |
| `AccountUpn` | <span data-ttu-id="acc57-118">string</span><span class="sxs-lookup"><span data-stu-id="acc57-118">string</span></span> | <span data-ttu-id="acc57-119">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-119">User principal name (UPN) of the account</span></span> |
| `OnPremSid` | <span data-ttu-id="acc57-120">string</span><span class="sxs-lookup"><span data-stu-id="acc57-120">string</span></span> | <span data-ttu-id="acc57-121">Identificateur de sécurité local (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-121">On-premises security identifier (SID) of the account</span></span> |
| `CloudSid` | <span data-ttu-id="acc57-122">string</span><span class="sxs-lookup"><span data-stu-id="acc57-122">string</span></span> | <span data-ttu-id="acc57-123">Identificateur de sécurité cloud du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-123">Cloud security identifier of the account</span></span> |
| `GivenName` | <span data-ttu-id="acc57-124">string</span><span class="sxs-lookup"><span data-stu-id="acc57-124">string</span></span> | <span data-ttu-id="acc57-125">Prénom ou nom de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-125">Given name or first name of the account user</span></span> |
| `Surname` | <span data-ttu-id="acc57-126">string</span><span class="sxs-lookup"><span data-stu-id="acc57-126">string</span></span> | <span data-ttu-id="acc57-127">Nom de famille, nom de famille ou nom de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-127">Surname, family name, or last name of the account user</span></span> |
| `AccountDisplayName` | <span data-ttu-id="acc57-128">string</span><span class="sxs-lookup"><span data-stu-id="acc57-128">string</span></span> | <span data-ttu-id="acc57-129">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="acc57-129">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="acc57-130">En règle générale, une combinaison d’un prénom ou d’un prénom donné, d’une initiation intermédiaire et d’un nom ou d’un nom de famille.</span><span class="sxs-lookup"><span data-stu-id="acc57-130">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `Department` | <span data-ttu-id="acc57-131">string</span><span class="sxs-lookup"><span data-stu-id="acc57-131">string</span></span> | <span data-ttu-id="acc57-132">Nom du service à qui appartient l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-132">Name of the department that the account user belongs to</span></span> |
| `JobTitle` | <span data-ttu-id="acc57-133">string</span><span class="sxs-lookup"><span data-stu-id="acc57-133">string</span></span> | <span data-ttu-id="acc57-134">Fonction de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-134">Job title of the account user</span></span> |
| `AccountName` | <span data-ttu-id="acc57-135">string</span><span class="sxs-lookup"><span data-stu-id="acc57-135">string</span></span> | <span data-ttu-id="acc57-136">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-136">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="acc57-137">string</span><span class="sxs-lookup"><span data-stu-id="acc57-137">string</span></span> | <span data-ttu-id="acc57-138">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-138">Domain of the account</span></span> |
| `EmailAddress` | <span data-ttu-id="acc57-139">string</span><span class="sxs-lookup"><span data-stu-id="acc57-139">string</span></span> | <span data-ttu-id="acc57-140">Adresse SMTP du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-140">SMTP address of the account</span></span> |
| `SipProxyAddress` | <span data-ttu-id="acc57-141">string</span><span class="sxs-lookup"><span data-stu-id="acc57-141">string</span></span> | <span data-ttu-id="acc57-142">Adresse SIP (Session Initiation Protocol) VOIP (Voice over IP) du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-142">Voice over IP (VOIP) session initiation protocol (SIP) address of the account</span></span> |
| `City` | <span data-ttu-id="acc57-143">string</span><span class="sxs-lookup"><span data-stu-id="acc57-143">string</span></span> | <span data-ttu-id="acc57-144">Ville où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-144">City where the account user is located</span></span> |
| `Country` | <span data-ttu-id="acc57-145">string</span><span class="sxs-lookup"><span data-stu-id="acc57-145">string</span></span> | <span data-ttu-id="acc57-146">Pays/région où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="acc57-146">Country/Region where the account user is located</span></span> |
| `IsAccountEnabled` | <span data-ttu-id="acc57-147">booléen</span><span class="sxs-lookup"><span data-stu-id="acc57-147">boolean</span></span> | <span data-ttu-id="acc57-148">Indique si le compte est activé ou non</span><span class="sxs-lookup"><span data-stu-id="acc57-148">Indicates whether the account is enabled or not</span></span> |

## <a name="related-topics"></a><span data-ttu-id="acc57-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="acc57-149">Related topics</span></span>
- [<span data-ttu-id="acc57-150">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="acc57-150">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="acc57-151">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="acc57-151">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="acc57-152">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="acc57-152">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="acc57-153">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="acc57-153">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="acc57-154">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="acc57-154">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="acc57-155">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="acc57-155">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
