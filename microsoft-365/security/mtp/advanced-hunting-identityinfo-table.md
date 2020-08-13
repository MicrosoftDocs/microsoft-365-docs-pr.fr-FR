---
title: Table IdentityInfo dans le schéma de chasse avancé
description: En savoir plus sur les informations de compte d’utilisateur dans la table IdentityInfo du schéma de chasse avancé
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, AccountInfo, IdentityInfo, compte
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
ms.openlocfilehash: 3d59f987ae4d670e3d7c6f1638f8090ffc3ba7fe
ms.sourcegitcommit: 51097b18d94da20aa727ebfbeb6ec84c263b25c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/12/2020
ms.locfileid: "46649306"
---
# <a name="identityinfo"></a><span data-ttu-id="21ff3-104">IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="21ff3-104">IdentityInfo</span></span>

<span data-ttu-id="21ff3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="21ff3-105">**Applies to:**</span></span>
- <span data-ttu-id="21ff3-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="21ff3-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="21ff3-107">Le `IdentityInfo` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les comptes d’utilisateur obtenus à partir de différents services, notamment Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="21ff3-107">The `IdentityInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about user accounts obtained from various services, including Azure Active Directory.</span></span> <span data-ttu-id="21ff3-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="21ff3-108">Use this reference to construct queries that return information from this table.</span></span>

>[!NOTE]
><span data-ttu-id="21ff3-109">Cette table a été renommée de `AccountInfo` .</span><span class="sxs-lookup"><span data-stu-id="21ff3-109">This table was renamed from `AccountInfo`.</span></span> <span data-ttu-id="21ff3-110">Lors du changement de nom, toutes les requêtes enregistrées dans le portail sont automatiquement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="21ff3-110">During renames, all queries saved in the portal are automatically updated.</span></span> <span data-ttu-id="21ff3-111">Vérifier les requêtes que vous avez enregistrées ailleurs.</span><span class="sxs-lookup"><span data-stu-id="21ff3-111">Check queries you have saved elsewhere.</span></span>

<span data-ttu-id="21ff3-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="21ff3-112">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="21ff3-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="21ff3-113">Column name</span></span> | <span data-ttu-id="21ff3-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="21ff3-114">Data type</span></span> | <span data-ttu-id="21ff3-115">Description</span><span class="sxs-lookup"><span data-stu-id="21ff3-115">Description</span></span> |
|-------------|-----------|-------------|
| `AccountObjectId` | <span data-ttu-id="21ff3-116">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-116">string</span></span> | <span data-ttu-id="21ff3-117">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="21ff3-117">Unique identifier for the account in Azure AD</span></span> |
| `AccountUpn` | <span data-ttu-id="21ff3-118">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-118">string</span></span> | <span data-ttu-id="21ff3-119">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-119">User principal name (UPN) of the account</span></span> |
| `OnPremSid` | <span data-ttu-id="21ff3-120">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-120">string</span></span> | <span data-ttu-id="21ff3-121">Identificateur de sécurité (SID) sur site du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-121">On-premises security identifier (SID) of the account</span></span> |
| `CloudSid` | <span data-ttu-id="21ff3-122">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-122">string</span></span> | <span data-ttu-id="21ff3-123">Identificateur de sécurité du Cloud du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-123">Cloud security identifier of the account</span></span> |
| `GivenName` | <span data-ttu-id="21ff3-124">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-124">string</span></span> | <span data-ttu-id="21ff3-125">Prénom ou prénom de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-125">Given name or first name of the account user</span></span> |
| `Surname` | <span data-ttu-id="21ff3-126">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-126">string</span></span> | <span data-ttu-id="21ff3-127">Nom, nom de famille ou nom de famille de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-127">Surname, family name, or last name of the account user</span></span> |
| `AccountDisplayName` | <span data-ttu-id="21ff3-128">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-128">string</span></span> | <span data-ttu-id="21ff3-129">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="21ff3-129">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="21ff3-130">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="21ff3-130">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `Department` | <span data-ttu-id="21ff3-131">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-131">string</span></span> | <span data-ttu-id="21ff3-132">Nom du service auquel appartient l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-132">Name of the department that the account user belongs to</span></span> |
| `JobTitle` | <span data-ttu-id="21ff3-133">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-133">string</span></span> | <span data-ttu-id="21ff3-134">Fonction de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-134">Job title of the account user</span></span> |
| `AccountName` | <span data-ttu-id="21ff3-135">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-135">string</span></span> | <span data-ttu-id="21ff3-136">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-136">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="21ff3-137">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-137">string</span></span> | <span data-ttu-id="21ff3-138">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-138">Domain of the account</span></span> |
| `EmailAddress` | <span data-ttu-id="21ff3-139">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-139">string</span></span> | <span data-ttu-id="21ff3-140">Adresse SMTP du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-140">SMTP address of the account</span></span> |
| `SipProxyAddress` | <span data-ttu-id="21ff3-141">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-141">string</span></span> | <span data-ttu-id="21ff3-142">Adresse SIP (Session Initiation Protocol) VOIP (Voice over IP) du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-142">Voice over IP (VOIP) session initiation protocol (SIP) address of the account</span></span> |
| `City` | <span data-ttu-id="21ff3-143">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-143">string</span></span> | <span data-ttu-id="21ff3-144">Ville où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-144">City where the account user is located</span></span> |
| `Country` | <span data-ttu-id="21ff3-145">string</span><span class="sxs-lookup"><span data-stu-id="21ff3-145">string</span></span> | <span data-ttu-id="21ff3-146">Pays/région où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="21ff3-146">Country/Region where the account user is located</span></span> |
| `IsAccountEnabled` | <span data-ttu-id="21ff3-147">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="21ff3-147">boolean</span></span> | <span data-ttu-id="21ff3-148">Indique si le compte est activé ou non.</span><span class="sxs-lookup"><span data-stu-id="21ff3-148">Indicates whether the account is enabled or not</span></span> |

## <a name="related-topics"></a><span data-ttu-id="21ff3-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21ff3-149">Related topics</span></span>
- [<span data-ttu-id="21ff3-150">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="21ff3-150">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="21ff3-151">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="21ff3-151">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="21ff3-152">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="21ff3-152">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="21ff3-153">Recherche sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="21ff3-153">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="21ff3-154">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="21ff3-154">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="21ff3-155">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="21ff3-155">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
