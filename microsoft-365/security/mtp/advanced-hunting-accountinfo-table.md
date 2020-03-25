---
title: Table AccountInfo dans le schéma de chasse avancé
description: En savoir plus sur les informations de compte d’utilisateur dans la table AccountInfo du schéma de chasse avancé
keywords: chasse avancée, recherche de menace, recherche dans les menaces informatiques, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, AlertInfo, alerte, entités, preuve, fichier, adresse IP, appareil, ordinateur, utilisateur, compte
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
ms.openlocfilehash: 9e4503ab297c7a584a548faa36ca6102c1b8dda6
ms.sourcegitcommit: 3b2fdf159d7dd962493a3838e3cf0cf429ee2bf2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "42929527"
---
# <a name="accountinfo"></a><span data-ttu-id="54934-104">AccountInfo</span><span class="sxs-lookup"><span data-stu-id="54934-104">AccountInfo</span></span>

<span data-ttu-id="54934-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="54934-105">**Applies to:**</span></span>
- <span data-ttu-id="54934-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="54934-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="54934-107">Le `AccountInfo` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les comptes d’utilisateur obtenus à partir de différents services, notamment Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54934-107">The `AccountInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about user accounts obtained from various services, including Azure Active Directory.</span></span> <span data-ttu-id="54934-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="54934-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="54934-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="54934-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="54934-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="54934-110">Column name</span></span> | <span data-ttu-id="54934-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="54934-111">Data type</span></span> | <span data-ttu-id="54934-112">Description</span><span class="sxs-lookup"><span data-stu-id="54934-112">Description</span></span> |
|-------------|-----------|-------------|
| `AccountObjectId` | <span data-ttu-id="54934-113">string</span><span class="sxs-lookup"><span data-stu-id="54934-113">string</span></span> | <span data-ttu-id="54934-114">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="54934-114">Unique identifier for the account in Azure AD</span></span> |
| `AccountUpn` | <span data-ttu-id="54934-115">string</span><span class="sxs-lookup"><span data-stu-id="54934-115">string</span></span> | <span data-ttu-id="54934-116">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="54934-116">User principal name (UPN) of the account</span></span> |
| `OnPremSid` | <span data-ttu-id="54934-117">string</span><span class="sxs-lookup"><span data-stu-id="54934-117">string</span></span> | <span data-ttu-id="54934-118">Identificateur de sécurité (SID) sur site du compte</span><span class="sxs-lookup"><span data-stu-id="54934-118">On-premises security identifier (SID) of the account</span></span> |
| `CloudSid` | <span data-ttu-id="54934-119">string</span><span class="sxs-lookup"><span data-stu-id="54934-119">string</span></span> | <span data-ttu-id="54934-120">Identificateur de sécurité du Cloud du compte</span><span class="sxs-lookup"><span data-stu-id="54934-120">Cloud security identifier of the account</span></span> |
| `GivenName` | <span data-ttu-id="54934-121">string</span><span class="sxs-lookup"><span data-stu-id="54934-121">string</span></span> | <span data-ttu-id="54934-122">Prénom ou prénom de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="54934-122">Given name or first name of the account user</span></span> |
| `Surname` | <span data-ttu-id="54934-123">string</span><span class="sxs-lookup"><span data-stu-id="54934-123">string</span></span> | <span data-ttu-id="54934-124">Nom, nom de famille ou nom de famille de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="54934-124">Surname, family name, or last name of the account user</span></span> |
| `AccountDisplayName` | <span data-ttu-id="54934-125">string</span><span class="sxs-lookup"><span data-stu-id="54934-125">string</span></span> | <span data-ttu-id="54934-126">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="54934-126">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="54934-127">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="54934-127">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `Department` | <span data-ttu-id="54934-128">string</span><span class="sxs-lookup"><span data-stu-id="54934-128">string</span></span> | <span data-ttu-id="54934-129">Nom du service auquel appartient l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="54934-129">Name of the department that the account user belongs to</span></span> |
| `JobTitle` | <span data-ttu-id="54934-130">string</span><span class="sxs-lookup"><span data-stu-id="54934-130">string</span></span> | <span data-ttu-id="54934-131">Fonction de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="54934-131">Job title of the account user</span></span> |
| `AccountName` | <span data-ttu-id="54934-132">string</span><span class="sxs-lookup"><span data-stu-id="54934-132">string</span></span> | <span data-ttu-id="54934-133">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="54934-133">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="54934-134">string</span><span class="sxs-lookup"><span data-stu-id="54934-134">string</span></span> | <span data-ttu-id="54934-135">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="54934-135">Domain of the account</span></span> |
| `EmailAddress` | <span data-ttu-id="54934-136">string</span><span class="sxs-lookup"><span data-stu-id="54934-136">string</span></span> | <span data-ttu-id="54934-137">Adresse SMTP du compte</span><span class="sxs-lookup"><span data-stu-id="54934-137">SMTP address of the account</span></span> |
| `SipProxyAddress` | <span data-ttu-id="54934-138">string</span><span class="sxs-lookup"><span data-stu-id="54934-138">string</span></span> | <span data-ttu-id="54934-139">Adresse SIP (Session Initiation Protocol) voix sur IP (VOIP) du compte</span><span class="sxs-lookup"><span data-stu-id="54934-139">Voice of over IP (VOIP) session initiation protocol (SIP) address of the account</span></span> |
| `City` | <span data-ttu-id="54934-140">string</span><span class="sxs-lookup"><span data-stu-id="54934-140">string</span></span> | <span data-ttu-id="54934-141">Ville où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="54934-141">City where the account user is located</span></span> |
| `Country` | <span data-ttu-id="54934-142">string</span><span class="sxs-lookup"><span data-stu-id="54934-142">string</span></span> | <span data-ttu-id="54934-143">Pays/région où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="54934-143">Country/Region where the account user is located</span></span> |
| `IsAccountEnabled` | <span data-ttu-id="54934-144">booléen</span><span class="sxs-lookup"><span data-stu-id="54934-144">boolean</span></span> | <span data-ttu-id="54934-145">Indique si le compte est activé ou non.</span><span class="sxs-lookup"><span data-stu-id="54934-145">Indicates whether the account is enabled or not</span></span> |

## <a name="related-topics"></a><span data-ttu-id="54934-146">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="54934-146">Related topics</span></span>
- [<span data-ttu-id="54934-147">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="54934-147">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="54934-148">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="54934-148">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="54934-149">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="54934-149">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="54934-150">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="54934-150">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="54934-151">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="54934-151">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="54934-152">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="54934-152">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
