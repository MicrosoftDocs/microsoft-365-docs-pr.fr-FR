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
ms.openlocfilehash: 59e9affc53398f2a1b06fbab9774e4b53e146425
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49932873"
---
# <a name="appfileevents"></a><span data-ttu-id="a03cc-104">AppFileEvents</span><span class="sxs-lookup"><span data-stu-id="a03cc-104">AppFileEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="a03cc-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a03cc-105">**Applies to:**</span></span>
- <span data-ttu-id="a03cc-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a03cc-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="a03cc-107">Le tableau du schéma de recherche avancée contient des informations sur les activités liées aux fichiers dans les applications et services cloud surveillés par `AppFileEvents` Microsoft Cloud App Security. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="a03cc-107">The `AppFileEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about file-related activities in cloud apps and services monitored by Microsoft Cloud App Security.</span></span> <span data-ttu-id="a03cc-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="a03cc-108">Use this reference to construct queries that return information from this table.</span></span>

>[!TIP]
> <span data-ttu-id="a03cc-109">Pour plus d’informations sur les types d’événements (valeurs) pris en charge par une table, utilisez la référence de schéma intégrée disponible `ActionType` dans le centre de sécurité. [](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center)</span><span class="sxs-lookup"><span data-stu-id="a03cc-109">For detailed information about the events types (`ActionType` values) supported by a table, use the [built-in schema reference](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) available in the security center.</span></span>

<span data-ttu-id="a03cc-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a03cc-110">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="a03cc-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="a03cc-111">Column name</span></span> | <span data-ttu-id="a03cc-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="a03cc-112">Data type</span></span> | <span data-ttu-id="a03cc-113">Description</span><span class="sxs-lookup"><span data-stu-id="a03cc-113">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="a03cc-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="a03cc-114">datetime</span></span> | <span data-ttu-id="a03cc-115">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="a03cc-115">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="a03cc-116">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-116">string</span></span> | <span data-ttu-id="a03cc-117">Type d’activité qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="a03cc-117">Type of activity that triggered the event.</span></span> <span data-ttu-id="a03cc-118">Pour plus [d’informations, voir](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) la référence du schéma dans le portail</span><span class="sxs-lookup"><span data-stu-id="a03cc-118">See the [in-portal schema reference](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) for details</span></span> |
| `Application` | <span data-ttu-id="a03cc-119">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-119">string</span></span> | <span data-ttu-id="a03cc-120">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="a03cc-120">Application that performed the recorded action</span></span> |
| `FileName` | <span data-ttu-id="a03cc-121">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-121">string</span></span> | <span data-ttu-id="a03cc-122">Nom du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="a03cc-122">Name of the file that the recorded action was applied to</span></span> |
| `FolderPath` | <span data-ttu-id="a03cc-123">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-123">string</span></span> | <span data-ttu-id="a03cc-124">Dossier contenant le fichier à lequel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="a03cc-124">Folder containing the file that the recorded action was applied to</span></span> |
| `PreviousFileName` | <span data-ttu-id="a03cc-125">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-125">string</span></span> | <span data-ttu-id="a03cc-126">Nom d’origine du fichier qui a été renommé à la suite de l’action</span><span class="sxs-lookup"><span data-stu-id="a03cc-126">Original name of the file that was renamed as a result of the action</span></span> |
| `PreviousFolderPath` | <span data-ttu-id="a03cc-127">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-127">string</span></span> | <span data-ttu-id="a03cc-128">Dossier d’origine contenant le fichier avant l’application de l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="a03cc-128">Original folder containing the file before the recorded action was applied</span></span> |
| `Protocol` | <span data-ttu-id="a03cc-129">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-129">string</span></span> | <span data-ttu-id="a03cc-130">Protocole réseau utilisé</span><span class="sxs-lookup"><span data-stu-id="a03cc-130">Network protocol used</span></span> |
| `AccountName` | <span data-ttu-id="a03cc-131">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-131">string</span></span> | <span data-ttu-id="a03cc-132">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="a03cc-132">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="a03cc-133">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-133">string</span></span> | <span data-ttu-id="a03cc-134">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="a03cc-134">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="a03cc-135">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-135">string</span></span> | <span data-ttu-id="a03cc-136">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="a03cc-136">User principal name (UPN) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="a03cc-137">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-137">string</span></span> | <span data-ttu-id="a03cc-138">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="a03cc-138">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="a03cc-139">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-139">string</span></span> | <span data-ttu-id="a03cc-140">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="a03cc-140">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="a03cc-141">En règle générale, une combinaison d’un prénom ou d’un prénom donné, d’une initiation intermédiaire et d’un nom ou d’un nom de famille.</span><span class="sxs-lookup"><span data-stu-id="a03cc-141">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="a03cc-142">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-142">string</span></span> | <span data-ttu-id="a03cc-143">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a03cc-143">Fully qualified domain name (FQDN) of the device</span></span> |
| `DeviceType` | <span data-ttu-id="a03cc-144">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-144">string</span></span> | <span data-ttu-id="a03cc-145">Type d’appareil</span><span class="sxs-lookup"><span data-stu-id="a03cc-145">Type of device</span></span> | 
| `OSPlatform` | <span data-ttu-id="a03cc-146">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-146">string</span></span> | <span data-ttu-id="a03cc-147">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a03cc-147">Platform of the operating system running on the device.</span></span> <span data-ttu-id="a03cc-148">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a03cc-148">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `IPAddress` | <span data-ttu-id="a03cc-149">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-149">string</span></span> | <span data-ttu-id="a03cc-150">Adresse IP attribuée au point de terminaison et utilisée lors des communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="a03cc-150">IP address assigned to the endpoint and used during related network communications</span></span> |
| `DestinationDeviceName` | <span data-ttu-id="a03cc-151">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-151">string</span></span> | <span data-ttu-id="a03cc-152">Nom de l’appareil exécutant l’application serveur qui a traitée l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="a03cc-152">Name of the device running the server application that processed the recorded action</span></span> |
| `DestinationIPAddress` | <span data-ttu-id="a03cc-153">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-153">string</span></span> | <span data-ttu-id="a03cc-154">Adresse IP du périphérique exécutant l’application serveur qui a traitée l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="a03cc-154">IP address of the device running the server application that processed the recorded action</span></span> |
| `Location` | <span data-ttu-id="a03cc-155">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-155">string</span></span> | <span data-ttu-id="a03cc-156">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="a03cc-156">City, country, or other geographic location associated with the event</span></span> |
| `Isp` | <span data-ttu-id="a03cc-157">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-157">string</span></span> | <span data-ttu-id="a03cc-158">Fournisseur de services Internet (ISP) associé à l’adresse IP du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a03cc-158">Internet service provider (ISP) associated with the endpoint IP address</span></span> |
| `ReportId` | <span data-ttu-id="a03cc-159">long</span><span class="sxs-lookup"><span data-stu-id="a03cc-159">long</span></span> | <span data-ttu-id="a03cc-160">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="a03cc-160">Unique identifier for the event</span></span> |
| `AdditionalFields` | <span data-ttu-id="a03cc-161">string</span><span class="sxs-lookup"><span data-stu-id="a03cc-161">string</span></span> | <span data-ttu-id="a03cc-162">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="a03cc-162">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="a03cc-163">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="a03cc-163">Related topics</span></span>
- [<span data-ttu-id="a03cc-164">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="a03cc-164">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="a03cc-165">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="a03cc-165">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="a03cc-166">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="a03cc-166">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="a03cc-167">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="a03cc-167">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="a03cc-168">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="a03cc-168">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="a03cc-169">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="a03cc-169">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
