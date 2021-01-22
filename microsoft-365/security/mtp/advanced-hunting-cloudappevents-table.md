---
title: Table CloudAppEvents dans le schéma de recherche avancé
description: En savoir plus sur les événements des applications et services cloud dans la table CloudAppEvents du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, CloudAppEvents, Cloud App Security, MCAS
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
ms.openlocfilehash: 021a8210bbe5886021e980b33ade0b9e2ded7b5b
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49928452"
---
# <a name="cloudappevents"></a><span data-ttu-id="889e0-104">CloudAppEvents</span><span class="sxs-lookup"><span data-stu-id="889e0-104">CloudAppEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="889e0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="889e0-105">**Applies to:**</span></span>
- <span data-ttu-id="889e0-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="889e0-106">Microsoft 365 Defender</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="889e0-107">Actuellement disponible en prévisualisation, le tableau du schéma de recherche avancé contient des informations sur les activités dans différentes applications et services cloud, en particulier `CloudAppEvents` Microsoft Teams et Exchange Online. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="889e0-107">Currently available in preview, the `CloudAppEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about activities in various cloud apps and services, specifically Microsoft Teams and Exchange Online.</span></span> <span data-ttu-id="889e0-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="889e0-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="889e0-109">Ce tableau s’étend pour inclure d’autres activités surveillées par Microsoft Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="889e0-109">This table will expand to include more activities monitored by Microsoft Cloud App Security.</span></span> <span data-ttu-id="889e0-110">Finalement, cette table inclut l’activité de fichier actuellement stockée dans la table [AppFileEvents.](advanced-hunting-appfileevents-table.md)</span><span class="sxs-lookup"><span data-stu-id="889e0-110">Eventually, this table will include file activity currently stored in the [AppFileEvents](advanced-hunting-appfileevents-table.md) table.</span></span> <span data-ttu-id="889e0-111">Microsoft fournit des conseils supplémentaires à mesure que d’autres données sont déplacer vers ce tableau.</span><span class="sxs-lookup"><span data-stu-id="889e0-111">Microsoft will provide additional guidance as more data moves to this table.</span></span>

<span data-ttu-id="889e0-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="889e0-112">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="889e0-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="889e0-113">Column name</span></span> | <span data-ttu-id="889e0-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="889e0-114">Data type</span></span> | <span data-ttu-id="889e0-115">Description</span><span class="sxs-lookup"><span data-stu-id="889e0-115">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="889e0-116">DateHeure</span><span class="sxs-lookup"><span data-stu-id="889e0-116">datetime</span></span> | <span data-ttu-id="889e0-117">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="889e0-117">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="889e0-118">string</span><span class="sxs-lookup"><span data-stu-id="889e0-118">string</span></span> | <span data-ttu-id="889e0-119">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="889e0-119">Type of activity that triggered the event</span></span> |
| `Application` | <span data-ttu-id="889e0-120">string</span><span class="sxs-lookup"><span data-stu-id="889e0-120">string</span></span> | <span data-ttu-id="889e0-121">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="889e0-121">Application that performed the recorded action</span></span> |
| `ApplicationId` | <span data-ttu-id="889e0-122">string</span><span class="sxs-lookup"><span data-stu-id="889e0-122">string</span></span> | <span data-ttu-id="889e0-123">Identificateur unique de l’application</span><span class="sxs-lookup"><span data-stu-id="889e0-123">Unique identifier for the application</span></span> |
| `AccountObjectId` | <span data-ttu-id="889e0-124">string</span><span class="sxs-lookup"><span data-stu-id="889e0-124">string</span></span> | <span data-ttu-id="889e0-125">Identificateur unique du compte dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="889e0-125">Unique identifier for the account in Azure Active Directory</span></span> |
| `AccountDisplayName` | <span data-ttu-id="889e0-126">string</span><span class="sxs-lookup"><span data-stu-id="889e0-126">string</span></span> | <span data-ttu-id="889e0-127">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="889e0-127">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="889e0-128">En règle générale, une combinaison d’un prénom ou d’un prénom donné, d’une initiation intermédiaire et d’un nom ou d’un nom de famille.</span><span class="sxs-lookup"><span data-stu-id="889e0-128">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `IsAdminOperation` | <span data-ttu-id="889e0-129">string</span><span class="sxs-lookup"><span data-stu-id="889e0-129">string</span></span> | <span data-ttu-id="889e0-130">Indique si l’activité a été effectuée par un administrateur</span><span class="sxs-lookup"><span data-stu-id="889e0-130">Indicates whether the activity was performed by an administrator</span></span> |
| `DeviceType` | <span data-ttu-id="889e0-131">string</span><span class="sxs-lookup"><span data-stu-id="889e0-131">string</span></span> | <span data-ttu-id="889e0-132">Type d’appareil en fonction de l’objectif et des fonctionnalités, tels que « Périphérique réseau », « Station de travail », « Serveur », « Mobile », « Console de jeu » ou « Imprimante »</span><span class="sxs-lookup"><span data-stu-id="889e0-132">Type of device based on purpose and functionality, such as "Network device", "Workstation", "Server", "Mobile", "Gaming console", or "Printer"</span></span> | 
| `OSPlatform` | <span data-ttu-id="889e0-133">string</span><span class="sxs-lookup"><span data-stu-id="889e0-133">string</span></span> | <span data-ttu-id="889e0-134">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="889e0-134">Platform of the operating system running on the device.</span></span> <span data-ttu-id="889e0-135">Cette colonne indique des systèmes d’exploitation spécifiques, y compris des variantes au sein de la même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="889e0-135">This column indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `IPAddress` | <span data-ttu-id="889e0-136">string</span><span class="sxs-lookup"><span data-stu-id="889e0-136">string</span></span> | <span data-ttu-id="889e0-137">Adresse IP attribuée au point de terminaison et utilisée lors des communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="889e0-137">IP address assigned to the endpoint and used during related network communications</span></span> |
| `IsAnonymousProxy` | <span data-ttu-id="889e0-138">string</span><span class="sxs-lookup"><span data-stu-id="889e0-138">string</span></span> | <span data-ttu-id="889e0-139">Indique si l’adresse IP appartient à un proxy anonyme connu</span><span class="sxs-lookup"><span data-stu-id="889e0-139">Indicates whether the IP address belongs to a known anonymous proxy</span></span> |
| `CountryCode` | <span data-ttu-id="889e0-140">string</span><span class="sxs-lookup"><span data-stu-id="889e0-140">string</span></span> | <span data-ttu-id="889e0-141">Code à deux lettres indiquant le pays où l’adresse IP du client est géolocalisé</span><span class="sxs-lookup"><span data-stu-id="889e0-141">Two-letter code indicating the country where the client IP address is geolocated</span></span> |
| `City` | <span data-ttu-id="889e0-142">string</span><span class="sxs-lookup"><span data-stu-id="889e0-142">string</span></span> | <span data-ttu-id="889e0-143">Ville où l’adresse IP du client est géolocalisé</span><span class="sxs-lookup"><span data-stu-id="889e0-143">City where the client IP address is geolocated</span></span> |
| `Isp` | <span data-ttu-id="889e0-144">string</span><span class="sxs-lookup"><span data-stu-id="889e0-144">string</span></span> | <span data-ttu-id="889e0-145">Fournisseur de services Internet (ISP) associé à l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="889e0-145">Internet service provider (ISP) associated with the IP address</span></span> |
| `UserAgent` | <span data-ttu-id="889e0-146">string</span><span class="sxs-lookup"><span data-stu-id="889e0-146">string</span></span> | <span data-ttu-id="889e0-147">Informations sur l’agent utilisateur à partir du navigateur web ou d’une autre application cliente</span><span class="sxs-lookup"><span data-stu-id="889e0-147">User agent information from the web browser or other client application</span></span> |
| `ActivityType` | <span data-ttu-id="889e0-148">string</span><span class="sxs-lookup"><span data-stu-id="889e0-148">string</span></span> | <span data-ttu-id="889e0-149">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="889e0-149">Type of activity that triggered the event</span></span> |
| `ActivityObjects` | <span data-ttu-id="889e0-150">string</span><span class="sxs-lookup"><span data-stu-id="889e0-150">string</span></span> | <span data-ttu-id="889e0-151">Liste des objets, tels que des fichiers ou des dossiers, qui ont été impliqués dans l’activité enregistrée</span><span class="sxs-lookup"><span data-stu-id="889e0-151">List of objects, such as files or folders, that were involved in the recorded activity</span></span> |
| `ObjectName` | <span data-ttu-id="889e0-152">string</span><span class="sxs-lookup"><span data-stu-id="889e0-152">string</span></span> | <span data-ttu-id="889e0-153">Nom de l’objet à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="889e0-153">Name of the object that the recorded action was applied to</span></span> |
| `ObjectType` | <span data-ttu-id="889e0-154">string</span><span class="sxs-lookup"><span data-stu-id="889e0-154">string</span></span> | <span data-ttu-id="889e0-155">Type d’objet, tel qu’un fichier ou un dossier, à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="889e0-155">Type of object, such as a file or a folder, that the recorded action was applied to</span></span> |
| `ObjectId` | <span data-ttu-id="889e0-156">string</span><span class="sxs-lookup"><span data-stu-id="889e0-156">string</span></span> | <span data-ttu-id="889e0-157">Identificateur unique de l’objet à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="889e0-157">Unique identifier of the object that the recorded action was applied to</span></span> |
| `ReportId` | <span data-ttu-id="889e0-158">string</span><span class="sxs-lookup"><span data-stu-id="889e0-158">string</span></span> | <span data-ttu-id="889e0-159">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="889e0-159">Unique identifier for the event</span></span> |
| `RawEventData` | <span data-ttu-id="889e0-160">string</span><span class="sxs-lookup"><span data-stu-id="889e0-160">string</span></span> | <span data-ttu-id="889e0-161">Informations d’événement brutes de l’application ou du service source au format JSON</span><span class="sxs-lookup"><span data-stu-id="889e0-161">Raw event information from the source application or service in JSON format</span></span> |
| `AdditionalFields` | <span data-ttu-id="889e0-162">string</span><span class="sxs-lookup"><span data-stu-id="889e0-162">string</span></span> | <span data-ttu-id="889e0-163">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="889e0-163">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="889e0-164">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="889e0-164">Related topics</span></span>
- [<span data-ttu-id="889e0-165">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="889e0-165">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="889e0-166">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="889e0-166">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="889e0-167">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="889e0-167">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="889e0-168">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="889e0-168">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="889e0-169">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="889e0-169">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="889e0-170">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="889e0-170">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
