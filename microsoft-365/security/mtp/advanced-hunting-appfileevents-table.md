---
title: Table AppFileEvents dans le schéma de recherche avancé
description: En savoir plus sur les événements liés aux fichiers associés aux applications et services cloud dans la table AppFileEvents du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, AppFileEvents, Cloud App Security, MCAS
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
ms.openlocfilehash: 8406d1f9e3d56555b1699d191933c6f9735c9574
ms.sourcegitcommit: 005028af7c5a6b2e95f17a0037958131484d9e73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2021
ms.locfileid: "50145486"
---
# <a name="appfileevents"></a><span data-ttu-id="95cb8-104">AppFileEvents</span><span class="sxs-lookup"><span data-stu-id="95cb8-104">AppFileEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="95cb8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="95cb8-105">**Applies to:**</span></span>
- <span data-ttu-id="95cb8-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="95cb8-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="95cb8-107">Le tableau du schéma de recherche avancée contient des informations sur les activités liées aux fichiers dans les applications et services cloud surveillés par `AppFileEvents` Microsoft Cloud App Security. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="95cb8-107">The `AppFileEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about file-related activities in cloud apps and services monitored by Microsoft Cloud App Security.</span></span> <span data-ttu-id="95cb8-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="95cb8-108">Use this reference to construct queries that return information from this table.</span></span>

>[!TIP]
> <span data-ttu-id="95cb8-109">Pour plus d’informations sur les types d’événements (valeurs) pris en charge par une table, utilisez la référence de schéma intégrée disponible `ActionType` dans le centre de sécurité. [](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center)</span><span class="sxs-lookup"><span data-stu-id="95cb8-109">For detailed information about the events types (`ActionType` values) supported by a table, use the [built-in schema reference](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) available in the security center.</span></span>

<span data-ttu-id="95cb8-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="95cb8-110">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="95cb8-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="95cb8-111">Column name</span></span> | <span data-ttu-id="95cb8-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="95cb8-112">Data type</span></span> | <span data-ttu-id="95cb8-113">Description</span><span class="sxs-lookup"><span data-stu-id="95cb8-113">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="95cb8-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="95cb8-114">datetime</span></span> | <span data-ttu-id="95cb8-115">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="95cb8-115">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="95cb8-116">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-116">string</span></span> | <span data-ttu-id="95cb8-117">Type d’activité qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="95cb8-117">Type of activity that triggered the event.</span></span> <span data-ttu-id="95cb8-118">Pour plus [d’informations, voir](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) la référence du schéma dans le portail</span><span class="sxs-lookup"><span data-stu-id="95cb8-118">See the [in-portal schema reference](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) for details</span></span> |
| `Application` | <span data-ttu-id="95cb8-119">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-119">string</span></span> | <span data-ttu-id="95cb8-120">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="95cb8-120">Application that performed the recorded action</span></span> |
| `FileName` | <span data-ttu-id="95cb8-121">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-121">string</span></span> | <span data-ttu-id="95cb8-122">Nom du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="95cb8-122">Name of the file that the recorded action was applied to</span></span> |
| `FolderPath` | <span data-ttu-id="95cb8-123">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-123">string</span></span> | <span data-ttu-id="95cb8-124">Dossier contenant le fichier à lequel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="95cb8-124">Folder containing the file that the recorded action was applied to</span></span> |
| `PreviousFileName` | <span data-ttu-id="95cb8-125">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-125">string</span></span> | <span data-ttu-id="95cb8-126">Nom d’origine du fichier qui a été renommé à la suite de l’action</span><span class="sxs-lookup"><span data-stu-id="95cb8-126">Original name of the file that was renamed as a result of the action</span></span> |
| `PreviousFolderPath` | <span data-ttu-id="95cb8-127">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-127">string</span></span> | <span data-ttu-id="95cb8-128">Dossier d’origine contenant le fichier avant l’application de l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="95cb8-128">Original folder containing the file before the recorded action was applied</span></span> |
| `Protocol` | <span data-ttu-id="95cb8-129">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-129">string</span></span> | <span data-ttu-id="95cb8-130">Protocole réseau utilisé</span><span class="sxs-lookup"><span data-stu-id="95cb8-130">Network protocol used</span></span> |
| `AccountName` | <span data-ttu-id="95cb8-131">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-131">string</span></span> | <span data-ttu-id="95cb8-132">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="95cb8-132">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="95cb8-133">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-133">string</span></span> | <span data-ttu-id="95cb8-134">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="95cb8-134">Domain of the account</span></span> |
| `AccountSid` | <span data-ttu-id="95cb8-135">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-135">string</span></span> | <span data-ttu-id="95cb8-136">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="95cb8-136">Security Identifier (SID) of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="95cb8-137">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-137">string</span></span> | <span data-ttu-id="95cb8-138">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="95cb8-138">User principal name (UPN) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="95cb8-139">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-139">string</span></span> | <span data-ttu-id="95cb8-140">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="95cb8-140">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="95cb8-141">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-141">string</span></span> | <span data-ttu-id="95cb8-142">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="95cb8-142">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="95cb8-143">En règle générale, une combinaison d’un prénom ou d’un prénom donné, d’une initiation intermédiaire et d’un nom ou d’un nom de famille.</span><span class="sxs-lookup"><span data-stu-id="95cb8-143">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="95cb8-144">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-144">string</span></span> | <span data-ttu-id="95cb8-145">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="95cb8-145">Fully qualified domain name (FQDN) of the device</span></span> |
| `DeviceType` | <span data-ttu-id="95cb8-146">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-146">string</span></span> | <span data-ttu-id="95cb8-147">Type d’appareil</span><span class="sxs-lookup"><span data-stu-id="95cb8-147">Type of device</span></span> | 
| `OSPlatform` | <span data-ttu-id="95cb8-148">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-148">string</span></span> | <span data-ttu-id="95cb8-149">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="95cb8-149">Platform of the operating system running on the device.</span></span> <span data-ttu-id="95cb8-150">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="95cb8-150">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `IPAddress` | <span data-ttu-id="95cb8-151">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-151">string</span></span> | <span data-ttu-id="95cb8-152">Adresse IP attribuée au point de terminaison et utilisée lors des communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="95cb8-152">IP address assigned to the endpoint and used during related network communications</span></span> |
| `Port` | <span data-ttu-id="95cb8-153">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-153">string</span></span> | <span data-ttu-id="95cb8-154">Port TCP utilisé pendant la communication</span><span class="sxs-lookup"><span data-stu-id="95cb8-154">TCP port used during communication</span></span>  |
| `DestinationDeviceName` | <span data-ttu-id="95cb8-155">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-155">string</span></span> | <span data-ttu-id="95cb8-156">Nom de l’appareil exécutant l’application serveur qui a traitée l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="95cb8-156">Name of the device running the server application that processed the recorded action</span></span> |
| `DestinationIPAddress` | <span data-ttu-id="95cb8-157">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-157">string</span></span> | <span data-ttu-id="95cb8-158">Adresse IP de l’appareil exécutant l’application serveur qui a traitée l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="95cb8-158">IP address of the device running the server application that processed the recorded action</span></span> |
| `DestinationPort` | <span data-ttu-id="95cb8-159">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-159">string</span></span> | <span data-ttu-id="95cb8-160">Port de destination des communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="95cb8-160">Destination port of related network communications</span></span> |
| `Location` | <span data-ttu-id="95cb8-161">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-161">string</span></span> | <span data-ttu-id="95cb8-162">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="95cb8-162">City, country, or other geographic location associated with the event</span></span> |
| `Isp` | <span data-ttu-id="95cb8-163">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-163">string</span></span> | <span data-ttu-id="95cb8-164">Fournisseur de services Internet (ISP) associé à l’adresse IP du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="95cb8-164">Internet service provider (ISP) associated with the endpoint IP address</span></span> |
| `ReportId` | <span data-ttu-id="95cb8-165">long</span><span class="sxs-lookup"><span data-stu-id="95cb8-165">long</span></span> | <span data-ttu-id="95cb8-166">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="95cb8-166">Unique identifier for the event</span></span> |
| `AdditionalFields` | <span data-ttu-id="95cb8-167">string</span><span class="sxs-lookup"><span data-stu-id="95cb8-167">string</span></span> | <span data-ttu-id="95cb8-168">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="95cb8-168">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="95cb8-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95cb8-169">Related topics</span></span>
- [<span data-ttu-id="95cb8-170">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="95cb8-170">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="95cb8-171">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="95cb8-171">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="95cb8-172">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="95cb8-172">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="95cb8-173">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="95cb8-173">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="95cb8-174">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="95cb8-174">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="95cb8-175">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="95cb8-175">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
