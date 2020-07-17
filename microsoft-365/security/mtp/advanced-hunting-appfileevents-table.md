---
title: Table AppFileEvents dans le schéma de chasse avancé
description: En savoir plus sur les événements liés aux fichiers associés aux applications et services Cloud dans le tableau AppFileEvents du schéma de chasse avancé
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, AppFileEvents, sécurité des applications Cloud, MCAS
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
ms.openlocfilehash: da3b331d4f607aa0961e275db9444aadbec4fcf2
ms.sourcegitcommit: ab10c042e5e9c6a7b2afef930ab0d247a6aa275d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "44899338"
---
# <a name="appfileevents"></a><span data-ttu-id="83a58-104">AppFileEvents</span><span class="sxs-lookup"><span data-stu-id="83a58-104">AppFileEvents</span></span>

<span data-ttu-id="83a58-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="83a58-105">**Applies to:**</span></span>
- <span data-ttu-id="83a58-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="83a58-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="83a58-107">Le `AppFileEvents` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les activités liées aux fichiers dans les applications et les services Cloud surveillés par la sécurité des applications Cloud de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="83a58-107">The `AppFileEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about file-related activities in cloud apps and services monitored by Microsoft Cloud App Security.</span></span> <span data-ttu-id="83a58-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="83a58-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="83a58-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="83a58-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="83a58-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="83a58-110">Column name</span></span> | <span data-ttu-id="83a58-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="83a58-111">Data type</span></span> | <span data-ttu-id="83a58-112">Description</span><span class="sxs-lookup"><span data-stu-id="83a58-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="83a58-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="83a58-113">datetime</span></span> | <span data-ttu-id="83a58-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="83a58-114">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="83a58-115">chaîne</span><span class="sxs-lookup"><span data-stu-id="83a58-115">string</span></span> | <span data-ttu-id="83a58-116">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="83a58-116">Type of activity that triggered the event</span></span> |
| `Application` | <span data-ttu-id="83a58-117">string</span><span class="sxs-lookup"><span data-stu-id="83a58-117">string</span></span> | <span data-ttu-id="83a58-118">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="83a58-118">Application that performed the recorded action</span></span> |
| `FileName` | <span data-ttu-id="83a58-119">string</span><span class="sxs-lookup"><span data-stu-id="83a58-119">string</span></span> | <span data-ttu-id="83a58-120">Nom du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="83a58-120">Name of the file that the recorded action was applied to</span></span> |
| `FolderPath` | <span data-ttu-id="83a58-121">string</span><span class="sxs-lookup"><span data-stu-id="83a58-121">string</span></span> | <span data-ttu-id="83a58-122">Dossier contenant le fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="83a58-122">Folder containing the file that the recorded action was applied to</span></span> |
| `PreviousFileName` | <span data-ttu-id="83a58-123">string</span><span class="sxs-lookup"><span data-stu-id="83a58-123">string</span></span> | <span data-ttu-id="83a58-124">Nom d’origine du fichier qui a été renommé suite à l’action</span><span class="sxs-lookup"><span data-stu-id="83a58-124">Original name of the file that was renamed as a result of the action</span></span> |
| `AccountName` | <span data-ttu-id="83a58-125">string</span><span class="sxs-lookup"><span data-stu-id="83a58-125">string</span></span> | <span data-ttu-id="83a58-126">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="83a58-126">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="83a58-127">string</span><span class="sxs-lookup"><span data-stu-id="83a58-127">string</span></span> | <span data-ttu-id="83a58-128">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="83a58-128">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="83a58-129">string</span><span class="sxs-lookup"><span data-stu-id="83a58-129">string</span></span> | <span data-ttu-id="83a58-130">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="83a58-130">User principal name (UPN) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="83a58-131">string</span><span class="sxs-lookup"><span data-stu-id="83a58-131">string</span></span> | <span data-ttu-id="83a58-132">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="83a58-132">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="83a58-133">string</span><span class="sxs-lookup"><span data-stu-id="83a58-133">string</span></span> | <span data-ttu-id="83a58-134">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="83a58-134">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="83a58-135">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="83a58-135">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `IPAddress` | <span data-ttu-id="83a58-136">string</span><span class="sxs-lookup"><span data-stu-id="83a58-136">string</span></span> | <span data-ttu-id="83a58-137">Adresse IP affectée au point de terminaison et utilisée pendant les communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="83a58-137">IP address assigned to the endpoint and used during related network communications</span></span> |
| `Location` | <span data-ttu-id="83a58-138">string</span><span class="sxs-lookup"><span data-stu-id="83a58-138">string</span></span> | <span data-ttu-id="83a58-139">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="83a58-139">City, country, or other geographic location associated with the event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="83a58-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83a58-140">Related topics</span></span>
- [<span data-ttu-id="83a58-141">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="83a58-141">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="83a58-142">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="83a58-142">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="83a58-143">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="83a58-143">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="83a58-144">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="83a58-144">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="83a58-145">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="83a58-145">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="83a58-146">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="83a58-146">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
