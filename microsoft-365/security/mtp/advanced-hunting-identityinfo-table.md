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
ms.openlocfilehash: e922fc7930d645a7024a0ffc73359277c4b637e4
ms.sourcegitcommit: b4119682bd3c036289e851fff56fde869c816479
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/22/2020
ms.locfileid: "45204922"
---
# <a name="identityinfo"></a><span data-ttu-id="1fd41-104">IdentityInfo</span><span class="sxs-lookup"><span data-stu-id="1fd41-104">IdentityInfo</span></span>

<span data-ttu-id="1fd41-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1fd41-105">**Applies to:**</span></span>
- <span data-ttu-id="1fd41-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="1fd41-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="1fd41-107">Le `IdentityInfo` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les comptes d’utilisateur obtenus à partir de différents services, notamment Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1fd41-107">The `IdentityInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about user accounts obtained from various services, including Azure Active Directory.</span></span> <span data-ttu-id="1fd41-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="1fd41-108">Use this reference to construct queries that return information from this table.</span></span>

>[!NOTE]
><span data-ttu-id="1fd41-109">Cette table a été renommée de `AccountInfo` .</span><span class="sxs-lookup"><span data-stu-id="1fd41-109">This table was renamed from `AccountInfo`.</span></span> <span data-ttu-id="1fd41-110">Lors du changement de nom, toutes les requêtes enregistrées dans le portail sont automatiquement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="1fd41-110">During renames, all queries saved in the portal are automatically updated.</span></span> <span data-ttu-id="1fd41-111">Vérifier les requêtes que vous avez enregistrées ailleurs.</span><span class="sxs-lookup"><span data-stu-id="1fd41-111">Check queries you have saved elsewhere.</span></span>

<span data-ttu-id="1fd41-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1fd41-112">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="1fd41-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="1fd41-113">Column name</span></span> | <span data-ttu-id="1fd41-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="1fd41-114">Data type</span></span> | <span data-ttu-id="1fd41-115">Description</span><span class="sxs-lookup"><span data-stu-id="1fd41-115">Description</span></span> |
|-------------|-----------|-------------|
| `AccountObjectId` | <span data-ttu-id="1fd41-116">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-116">string</span></span> | <span data-ttu-id="1fd41-117">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="1fd41-117">Unique identifier for the account in Azure AD</span></span> |
| `AccountUpn` | <span data-ttu-id="1fd41-118">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-118">string</span></span> | <span data-ttu-id="1fd41-119">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-119">User principal name (UPN) of the account</span></span> |
| `OnPremSid` | <span data-ttu-id="1fd41-120">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-120">string</span></span> | <span data-ttu-id="1fd41-121">Identificateur de sécurité (SID) sur site du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-121">On-premises security identifier (SID) of the account</span></span> |
| `CloudSid` | <span data-ttu-id="1fd41-122">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-122">string</span></span> | <span data-ttu-id="1fd41-123">Identificateur de sécurité du Cloud du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-123">Cloud security identifier of the account</span></span> |
| `GivenName` | <span data-ttu-id="1fd41-124">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-124">string</span></span> | <span data-ttu-id="1fd41-125">Prénom ou prénom de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-125">Given name or first name of the account user</span></span> |
| `Surname` | <span data-ttu-id="1fd41-126">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-126">string</span></span> | <span data-ttu-id="1fd41-127">Nom, nom de famille ou nom de famille de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-127">Surname, family name, or last name of the account user</span></span> |
| `AccountDisplayName` | <span data-ttu-id="1fd41-128">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-128">string</span></span> | <span data-ttu-id="1fd41-129">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="1fd41-129">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="1fd41-130">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="1fd41-130">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `Department` | <span data-ttu-id="1fd41-131">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-131">string</span></span> | <span data-ttu-id="1fd41-132">Nom du service auquel appartient l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-132">Name of the department that the account user belongs to</span></span> |
| `JobTitle` | <span data-ttu-id="1fd41-133">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-133">string</span></span> | <span data-ttu-id="1fd41-134">Fonction de l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-134">Job title of the account user</span></span> |
| `AccountName` | <span data-ttu-id="1fd41-135">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-135">string</span></span> | <span data-ttu-id="1fd41-136">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-136">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="1fd41-137">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-137">string</span></span> | <span data-ttu-id="1fd41-138">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-138">Domain of the account</span></span> |
| `EmailAddress` | <span data-ttu-id="1fd41-139">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-139">string</span></span> | <span data-ttu-id="1fd41-140">Adresse SMTP du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-140">SMTP address of the account</span></span> |
| `SipProxyAddress` | <span data-ttu-id="1fd41-141">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-141">string</span></span> | <span data-ttu-id="1fd41-142">Adresse SIP (Session Initiation Protocol) VOIP (Voice over IP) du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-142">Voice over IP (VOIP) session initiation protocol (SIP) address of the account</span></span> |
| `City` | <span data-ttu-id="1fd41-143">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-143">string</span></span> | <span data-ttu-id="1fd41-144">Ville où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-144">City where the account user is located</span></span> |
| `Country` | <span data-ttu-id="1fd41-145">string</span><span class="sxs-lookup"><span data-stu-id="1fd41-145">string</span></span> | <span data-ttu-id="1fd41-146">Pays/région où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="1fd41-146">Country/Region where the account user is located</span></span> |
| `IsAccountEnabled` | <span data-ttu-id="1fd41-147">booléen</span><span class="sxs-lookup"><span data-stu-id="1fd41-147">boolean</span></span> | <span data-ttu-id="1fd41-148">Indique si le compte est activé ou non.</span><span class="sxs-lookup"><span data-stu-id="1fd41-148">Indicates whether the account is enabled or not</span></span> |

## <a name="related-topics"></a><span data-ttu-id="1fd41-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fd41-149">Related topics</span></span>
- [<span data-ttu-id="1fd41-150">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="1fd41-150">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="1fd41-151">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="1fd41-151">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="1fd41-152">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="1fd41-152">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="1fd41-153">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="1fd41-153">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="1fd41-154">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="1fd41-154">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="1fd41-155">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="1fd41-155">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
