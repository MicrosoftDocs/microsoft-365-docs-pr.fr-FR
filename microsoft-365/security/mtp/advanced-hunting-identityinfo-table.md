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
ms.collection:
- M365-security-compliance
- m365-initiative-m365-defender
ms.topic: article
ms.openlocfilehash: 94afa9e36ca75491511338297f02e8031333e53f
ms.sourcegitcommit: 5e1b8c959a081022826fb09358730096248507ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48412741"
---
# <a name="identityinfo"></a><span data-ttu-id="685f4-104">IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="685f4-104">IdentityInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="685f4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="685f4-105">**Applies to:**</span></span>
- <span data-ttu-id="685f4-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="685f4-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="685f4-107">Le `IdentityInfo` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les comptes d’utilisateur obtenus à partir de différents services, notamment Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="685f4-107">The `IdentityInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about user accounts obtained from various services, including Azure Active Directory.</span></span> <span data-ttu-id="685f4-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="685f4-108">Use this reference to construct queries that return information from this table.</span></span>

>[!NOTE]
><span data-ttu-id="685f4-109">Cette table a été renommée de `AccountInfo` .</span><span class="sxs-lookup"><span data-stu-id="685f4-109">This table was renamed from `AccountInfo`.</span></span> <span data-ttu-id="685f4-110">Lors du changement de nom, toutes les requêtes enregistrées dans le portail sont automatiquement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="685f4-110">During renames, all queries saved in the portal are automatically updated.</span></span> <span data-ttu-id="685f4-111">Vérifier les requêtes que vous avez enregistrées ailleurs.</span><span class="sxs-lookup"><span data-stu-id="685f4-111">Check queries you have saved elsewhere.</span></span>

<span data-ttu-id="685f4-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="685f4-112">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="685f4-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="685f4-113">Column name</span></span> | <span data-ttu-id="685f4-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="685f4-114">Data type</span></span> | <span data-ttu-id="685f4-115">Description</span><span class="sxs-lookup"><span data-stu-id="685f4-115">Description</span></span> |
|-------------|-----------|-------------|
| `AccountObjectId` | <span data-ttu-id="685f4-116">string</span><span class="sxs-lookup"><span data-stu-id="685f4-116">string</span></span> | <span data-ttu-id="685f4-117">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="685f4-117">Unique identifier for the account in Azure AD</span></span> |
| `AccountUpn` | <span data-ttu-id="685f4-118">string</span><span class="sxs-lookup"><span data-stu-id="685f4-118">string</span></span> | <span data-ttu-id="685f4-119">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-119">User principal name (UPN) of the account</span></span> |
| `OnPremSid` | <span data-ttu-id="685f4-120">string</span><span class="sxs-lookup"><span data-stu-id="685f4-120">string</span></span> | <span data-ttu-id="685f4-121">Identificateur de sécurité (SID) sur site du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-121">On-premises security identifier (SID) of the account</span></span> |
| `CloudSid` | <span data-ttu-id="685f4-122">string</span><span class="sxs-lookup"><span data-stu-id="685f4-122">string</span></span> | <span data-ttu-id="685f4-123">Identificateur de sécurité du Cloud du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-123">Cloud security identifier of the account</span></span> |
| `GivenName` | <span data-ttu-id="685f4-124">string</span><span class="sxs-lookup"><span data-stu-id="685f4-124">string</span></span> | <span data-ttu-id="685f4-125">Prénom ou prénom de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-125">Given name or first name of the account user</span></span> |
| `Surname` | <span data-ttu-id="685f4-126">string</span><span class="sxs-lookup"><span data-stu-id="685f4-126">string</span></span> | <span data-ttu-id="685f4-127">Nom, nom de famille ou nom de famille de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-127">Surname, family name, or last name of the account user</span></span> |
| `AccountDisplayName` | <span data-ttu-id="685f4-128">string</span><span class="sxs-lookup"><span data-stu-id="685f4-128">string</span></span> | <span data-ttu-id="685f4-129">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="685f4-129">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="685f4-130">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="685f4-130">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `Department` | <span data-ttu-id="685f4-131">string</span><span class="sxs-lookup"><span data-stu-id="685f4-131">string</span></span> | <span data-ttu-id="685f4-132">Nom du service auquel appartient l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-132">Name of the department that the account user belongs to</span></span> |
| `JobTitle` | <span data-ttu-id="685f4-133">string</span><span class="sxs-lookup"><span data-stu-id="685f4-133">string</span></span> | <span data-ttu-id="685f4-134">Fonction de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-134">Job title of the account user</span></span> |
| `AccountName` | <span data-ttu-id="685f4-135">string</span><span class="sxs-lookup"><span data-stu-id="685f4-135">string</span></span> | <span data-ttu-id="685f4-136">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-136">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="685f4-137">string</span><span class="sxs-lookup"><span data-stu-id="685f4-137">string</span></span> | <span data-ttu-id="685f4-138">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-138">Domain of the account</span></span> |
| `EmailAddress` | <span data-ttu-id="685f4-139">string</span><span class="sxs-lookup"><span data-stu-id="685f4-139">string</span></span> | <span data-ttu-id="685f4-140">Adresse SMTP du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-140">SMTP address of the account</span></span> |
| `SipProxyAddress` | <span data-ttu-id="685f4-141">string</span><span class="sxs-lookup"><span data-stu-id="685f4-141">string</span></span> | <span data-ttu-id="685f4-142">Adresse SIP (Session Initiation Protocol) VOIP (Voice over IP) du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-142">Voice over IP (VOIP) session initiation protocol (SIP) address of the account</span></span> |
| `City` | <span data-ttu-id="685f4-143">string</span><span class="sxs-lookup"><span data-stu-id="685f4-143">string</span></span> | <span data-ttu-id="685f4-144">Ville où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-144">City where the account user is located</span></span> |
| `Country` | <span data-ttu-id="685f4-145">string</span><span class="sxs-lookup"><span data-stu-id="685f4-145">string</span></span> | <span data-ttu-id="685f4-146">Pays/région où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="685f4-146">Country/Region where the account user is located</span></span> |
| `IsAccountEnabled` | <span data-ttu-id="685f4-147">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="685f4-147">boolean</span></span> | <span data-ttu-id="685f4-148">Indique si le compte est activé ou non.</span><span class="sxs-lookup"><span data-stu-id="685f4-148">Indicates whether the account is enabled or not</span></span> |

## <a name="related-topics"></a><span data-ttu-id="685f4-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="685f4-149">Related topics</span></span>
- [<span data-ttu-id="685f4-150">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="685f4-150">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="685f4-151">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="685f4-151">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="685f4-152">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="685f4-152">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="685f4-153">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="685f4-153">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="685f4-154">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="685f4-154">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="685f4-155">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="685f4-155">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
