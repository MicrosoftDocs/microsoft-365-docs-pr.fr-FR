---
title: Table CloudAppEvents dans le schéma de chasse avancé
description: En savoir plus sur les événements des applications et services Cloud dans le tableau CloudAppEvents du schéma de chasse avancé
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, CloudAppEvents, sécurité des applications Cloud, MCAS
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
- m365initiative-m365-defender
ms.topic: article
ms.openlocfilehash: 3cb4498e5db6a7752e99b8c677bc8936d2c975ef
ms.sourcegitcommit: e7bf23df4852b78912229d1d38ec475223597f34
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "49087765"
---
# <a name="cloudappevents"></a><span data-ttu-id="c3925-104">CloudAppEvents</span><span class="sxs-lookup"><span data-stu-id="c3925-104">CloudAppEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="c3925-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c3925-105">**Applies to:**</span></span>
- <span data-ttu-id="c3925-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c3925-106">Microsoft 365 Defender</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="c3925-107">Actuellement disponible en aperçu, le `CloudAppEvents` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les activités dans les différents services et applications Cloud, en particulier Microsoft teams et Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c3925-107">Currently available in preview, the `CloudAppEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about activities in various cloud apps and services, specifically Microsoft Teams and Exchange Online.</span></span> <span data-ttu-id="c3925-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="c3925-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="c3925-109">Cette table s’étendra pour inclure plus d’activités surveillées par la sécurité des applications Cloud de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c3925-109">This table will expand to include more activities monitored by Microsoft Cloud App Security.</span></span> <span data-ttu-id="c3925-110">Cette table inclut finalement l’activité de fichier actuellement stockée dans la table [AppFileEvents](advanced-hunting-appfileevents-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c3925-110">Eventually, this table will include file activity currently stored in the [AppFileEvents](advanced-hunting-appfileevents-table.md) table.</span></span> <span data-ttu-id="c3925-111">Microsoft fournira des conseils supplémentaires au fur et à mesure que des données seront déplacées vers ce tableau.</span><span class="sxs-lookup"><span data-stu-id="c3925-111">Microsoft will provide additional guidance as more data moves to this table.</span></span>

<span data-ttu-id="c3925-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c3925-112">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="c3925-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="c3925-113">Column name</span></span> | <span data-ttu-id="c3925-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="c3925-114">Data type</span></span> | <span data-ttu-id="c3925-115">Description</span><span class="sxs-lookup"><span data-stu-id="c3925-115">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="c3925-116">DateHeure</span><span class="sxs-lookup"><span data-stu-id="c3925-116">datetime</span></span> | <span data-ttu-id="c3925-117">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="c3925-117">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="c3925-118">string</span><span class="sxs-lookup"><span data-stu-id="c3925-118">string</span></span> | <span data-ttu-id="c3925-119">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="c3925-119">Type of activity that triggered the event</span></span> |
| `Application` | <span data-ttu-id="c3925-120">string</span><span class="sxs-lookup"><span data-stu-id="c3925-120">string</span></span> | <span data-ttu-id="c3925-121">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="c3925-121">Application that performed the recorded action</span></span> |
| `ApplicationId` | <span data-ttu-id="c3925-122">string</span><span class="sxs-lookup"><span data-stu-id="c3925-122">string</span></span> | <span data-ttu-id="c3925-123">Identificateur unique de l’application</span><span class="sxs-lookup"><span data-stu-id="c3925-123">Unique identifier for the application</span></span> |
| `AccountObjectId` | <span data-ttu-id="c3925-124">string</span><span class="sxs-lookup"><span data-stu-id="c3925-124">string</span></span> | <span data-ttu-id="c3925-125">Identificateur unique du compte dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c3925-125">Unique identifier for the account in Azure Active Directory</span></span> |
| `AccountDisplayName` | <span data-ttu-id="c3925-126">string</span><span class="sxs-lookup"><span data-stu-id="c3925-126">string</span></span> | <span data-ttu-id="c3925-127">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="c3925-127">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="c3925-128">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="c3925-128">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `IsAdminOperation` | <span data-ttu-id="c3925-129">string</span><span class="sxs-lookup"><span data-stu-id="c3925-129">string</span></span> | <span data-ttu-id="c3925-130">Indique si l’activité a été effectuée par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="c3925-130">Indicates whether the activity was performed by an administrator</span></span> |
| `DeviceType` | <span data-ttu-id="c3925-131">string</span><span class="sxs-lookup"><span data-stu-id="c3925-131">string</span></span> | <span data-ttu-id="c3925-132">Type d’appareil basé sur l’objectif et les fonctionnalités, tels que « périphérique réseau », « station de travail », « serveur », « mobile », « console de jeu » ou « imprimante »</span><span class="sxs-lookup"><span data-stu-id="c3925-132">Type of device based on purpose and functionality, such as "Network device", "Workstation", "Server", "Mobile", "Gaming console", or "Printer"</span></span> | 
| `OSPlatform` | <span data-ttu-id="c3925-133">string</span><span class="sxs-lookup"><span data-stu-id="c3925-133">string</span></span> | <span data-ttu-id="c3925-134">Plateforme du système d’exploitation s’exécutant sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3925-134">Platform of the operating system running on the device.</span></span> <span data-ttu-id="c3925-135">Cette colonne indique les systèmes d’exploitation spécifiques, y compris les variantes au sein de la même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3925-135">This column indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `IPAddress` | <span data-ttu-id="c3925-136">string</span><span class="sxs-lookup"><span data-stu-id="c3925-136">string</span></span> | <span data-ttu-id="c3925-137">Adresse IP affectée au point de terminaison et utilisée pendant les communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="c3925-137">IP address assigned to the endpoint and used during related network communications</span></span> |
| `IsAnonymousProxy` | <span data-ttu-id="c3925-138">string</span><span class="sxs-lookup"><span data-stu-id="c3925-138">string</span></span> | <span data-ttu-id="c3925-139">Indique si l’adresse IP appartient à un proxy anonyme connu.</span><span class="sxs-lookup"><span data-stu-id="c3925-139">Indicates whether the IP address belongs to a known anonymous proxy</span></span> |
| `CountryCode` | <span data-ttu-id="c3925-140">string</span><span class="sxs-lookup"><span data-stu-id="c3925-140">string</span></span> | <span data-ttu-id="c3925-141">Code à deux lettres indiquant le pays où se trouve l’adresse IP du client</span><span class="sxs-lookup"><span data-stu-id="c3925-141">Two-letter code indicating the country where the client IP address is geolocated</span></span> |
| `City` | <span data-ttu-id="c3925-142">string</span><span class="sxs-lookup"><span data-stu-id="c3925-142">string</span></span> | <span data-ttu-id="c3925-143">Ville où se trouve l’adresse IP du client</span><span class="sxs-lookup"><span data-stu-id="c3925-143">City where the client IP address is geolocated</span></span> |
| `Isp` | <span data-ttu-id="c3925-144">string</span><span class="sxs-lookup"><span data-stu-id="c3925-144">string</span></span> | <span data-ttu-id="c3925-145">Fournisseur de services Internet (ISP) associé à l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="c3925-145">Internet service provider (ISP) associated with the IP address</span></span> |
| `UserAgent` | <span data-ttu-id="c3925-146">string</span><span class="sxs-lookup"><span data-stu-id="c3925-146">string</span></span> | <span data-ttu-id="c3925-147">Informations de l’agent utilisateur à partir du navigateur Web ou d’une autre application cliente</span><span class="sxs-lookup"><span data-stu-id="c3925-147">User agent information from the web browser or other client application</span></span> |
| `ActivityType` | <span data-ttu-id="c3925-148">string</span><span class="sxs-lookup"><span data-stu-id="c3925-148">string</span></span> | <span data-ttu-id="c3925-149">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="c3925-149">Type of activity that triggered the event</span></span> |
| `ActivityObjects` | <span data-ttu-id="c3925-150">string</span><span class="sxs-lookup"><span data-stu-id="c3925-150">string</span></span> | <span data-ttu-id="c3925-151">Liste d’objets, tels que des fichiers ou des dossiers, qui ont été impliqués dans l’activité enregistrée</span><span class="sxs-lookup"><span data-stu-id="c3925-151">List of objects, such as files or folders, that were involved in the recorded activity</span></span> |
| `ObjectName` | <span data-ttu-id="c3925-152">string</span><span class="sxs-lookup"><span data-stu-id="c3925-152">string</span></span> | <span data-ttu-id="c3925-153">Nom de l’objet auquel l’action enregistrée a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="c3925-153">Name of the object that the recorded action was applied to</span></span> |
| `ObjectType` | <span data-ttu-id="c3925-154">string</span><span class="sxs-lookup"><span data-stu-id="c3925-154">string</span></span> | <span data-ttu-id="c3925-155">Type d’objet, tel qu’un fichier ou un dossier, auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="c3925-155">Type of object, such as a file or a folder, that the recorded action was applied to</span></span> |
| `ObjectId` | <span data-ttu-id="c3925-156">string</span><span class="sxs-lookup"><span data-stu-id="c3925-156">string</span></span> | <span data-ttu-id="c3925-157">Identificateur unique de l’objet auquel l’action enregistrée a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="c3925-157">Unique identifier of the object that the recorded action was applied to</span></span> |
| `ReportId` | <span data-ttu-id="c3925-158">string</span><span class="sxs-lookup"><span data-stu-id="c3925-158">string</span></span> | <span data-ttu-id="c3925-159">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="c3925-159">Unique identifier for the event</span></span> |
| `RawEventData` | <span data-ttu-id="c3925-160">string</span><span class="sxs-lookup"><span data-stu-id="c3925-160">string</span></span> | <span data-ttu-id="c3925-161">Informations d’événements brutes à partir de l’application ou du service source au format JSON</span><span class="sxs-lookup"><span data-stu-id="c3925-161">Raw event information from the source application or service in JSON format</span></span> |
| `AdditionalFields` | <span data-ttu-id="c3925-162">string</span><span class="sxs-lookup"><span data-stu-id="c3925-162">string</span></span> | <span data-ttu-id="c3925-163">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="c3925-163">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="c3925-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3925-164">Related topics</span></span>
- [<span data-ttu-id="c3925-165">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c3925-165">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="c3925-166">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="c3925-166">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="c3925-167">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="c3925-167">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="c3925-168">Rechercher sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="c3925-168">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="c3925-169">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="c3925-169">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="c3925-170">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="c3925-170">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
