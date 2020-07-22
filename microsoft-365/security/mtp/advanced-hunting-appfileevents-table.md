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
ms.openlocfilehash: 663dc2a3de676fa2daeab3d9621254e956d42fc4
ms.sourcegitcommit: b4119682bd3c036289e851fff56fde869c816479
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/22/2020
ms.locfileid: "45204754"
---
# <a name="appfileevents"></a><span data-ttu-id="dc3a0-104">AppFileEvents</span><span class="sxs-lookup"><span data-stu-id="dc3a0-104">AppFileEvents</span></span>

<span data-ttu-id="dc3a0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="dc3a0-105">**Applies to:**</span></span>
- <span data-ttu-id="dc3a0-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="dc3a0-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="dc3a0-107">Le `AppFileEvents` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les activités liées aux fichiers dans les applications et les services Cloud surveillés par la sécurité des applications Cloud de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-107">The `AppFileEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about file-related activities in cloud apps and services monitored by Microsoft Cloud App Security.</span></span> <span data-ttu-id="dc3a0-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="dc3a0-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="dc3a0-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="dc3a0-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dc3a0-110">Column name</span></span> | <span data-ttu-id="dc3a0-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="dc3a0-111">Data type</span></span> | <span data-ttu-id="dc3a0-112">Description</span><span class="sxs-lookup"><span data-stu-id="dc3a0-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="dc3a0-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="dc3a0-113">datetime</span></span> | <span data-ttu-id="dc3a0-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="dc3a0-114">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="dc3a0-115">chaîne</span><span class="sxs-lookup"><span data-stu-id="dc3a0-115">string</span></span> | <span data-ttu-id="dc3a0-116">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="dc3a0-116">Type of activity that triggered the event</span></span> |
| `Application` | <span data-ttu-id="dc3a0-117">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-117">string</span></span> | <span data-ttu-id="dc3a0-118">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="dc3a0-118">Application that performed the recorded action</span></span> |
| `FileName` | <span data-ttu-id="dc3a0-119">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-119">string</span></span> | <span data-ttu-id="dc3a0-120">Nom du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="dc3a0-120">Name of the file that the recorded action was applied to</span></span> |
| `FolderPath` | <span data-ttu-id="dc3a0-121">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-121">string</span></span> | <span data-ttu-id="dc3a0-122">Dossier contenant le fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="dc3a0-122">Folder containing the file that the recorded action was applied to</span></span> |
| `PreviousFileName` | <span data-ttu-id="dc3a0-123">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-123">string</span></span> | <span data-ttu-id="dc3a0-124">Nom d’origine du fichier qui a été renommé suite à l’action</span><span class="sxs-lookup"><span data-stu-id="dc3a0-124">Original name of the file that was renamed as a result of the action</span></span> |
| `PreviousFolderPath` | <span data-ttu-id="dc3a0-125">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-125">string</span></span> | <span data-ttu-id="dc3a0-126">Dossier d’origine contenant le fichier avant l’application de l’action enregistrer</span><span class="sxs-lookup"><span data-stu-id="dc3a0-126">Original folder containing the file before the recorded action was applied</span></span> |
| `Protocol` | <span data-ttu-id="dc3a0-127">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-127">string</span></span> | <span data-ttu-id="dc3a0-128">Protocole réseau utilisé</span><span class="sxs-lookup"><span data-stu-id="dc3a0-128">Network protocol used</span></span> |
| `AccountName` | <span data-ttu-id="dc3a0-129">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-129">string</span></span> | <span data-ttu-id="dc3a0-130">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="dc3a0-130">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="dc3a0-131">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-131">string</span></span> | <span data-ttu-id="dc3a0-132">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="dc3a0-132">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="dc3a0-133">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-133">string</span></span> | <span data-ttu-id="dc3a0-134">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="dc3a0-134">User principal name (UPN) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="dc3a0-135">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-135">string</span></span> | <span data-ttu-id="dc3a0-136">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="dc3a0-136">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="dc3a0-137">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-137">string</span></span> | <span data-ttu-id="dc3a0-138">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-138">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="dc3a0-139">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-139">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="dc3a0-140">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-140">string</span></span> | <span data-ttu-id="dc3a0-141">Nom de domaine complet (FQDN) du périphérique</span><span class="sxs-lookup"><span data-stu-id="dc3a0-141">Fully qualified domain name (FQDN) of the device</span></span> |
| `DeviceType` | <span data-ttu-id="dc3a0-142">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-142">string</span></span> | <span data-ttu-id="dc3a0-143">Type de périphérique</span><span class="sxs-lookup"><span data-stu-id="dc3a0-143">Type of device</span></span> | 
| `OSPlatform` | <span data-ttu-id="dc3a0-144">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-144">string</span></span> | <span data-ttu-id="dc3a0-145">Plateforme du système d’exploitation s’exécutant sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-145">Platform of the operating system running on the device.</span></span> <span data-ttu-id="dc3a0-146">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-146">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `IPAddress` | <span data-ttu-id="dc3a0-147">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-147">string</span></span> | <span data-ttu-id="dc3a0-148">Adresse IP affectée au point de terminaison et utilisée pendant les communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="dc3a0-148">IP address assigned to the endpoint and used during related network communications</span></span> |
| `DestinationDeviceName` | <span data-ttu-id="dc3a0-149">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-149">string</span></span> | <span data-ttu-id="dc3a0-150">Nom de l’appareil exécutant l’application serveur qui a traité l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-150">Name of the device running the server application that processed the recorded action</span></span> |
| `DestinationIPAddress` | <span data-ttu-id="dc3a0-151">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-151">string</span></span> | <span data-ttu-id="dc3a0-152">Adresse IP de l’appareil exécutant l’application serveur qui a traité l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="dc3a0-152">IP address of the device running the server application that processed the recorded action</span></span> |
| `Location` | <span data-ttu-id="dc3a0-153">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-153">string</span></span> | <span data-ttu-id="dc3a0-154">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="dc3a0-154">City, country, or other geographic location associated with the event</span></span> |
| `Isp` | <span data-ttu-id="dc3a0-155">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-155">string</span></span> | <span data-ttu-id="dc3a0-156">Fournisseur de services Internet associé à l’adresse IP du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="dc3a0-156">Internet service provider (ISP) associated with the endpoint IP address</span></span> |
| `ReportId` | <span data-ttu-id="dc3a0-157">long</span><span class="sxs-lookup"><span data-stu-id="dc3a0-157">long</span></span> | <span data-ttu-id="dc3a0-158">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="dc3a0-158">Unique identifier for the event</span></span> |
| `AdditionalFields` | <span data-ttu-id="dc3a0-159">string</span><span class="sxs-lookup"><span data-stu-id="dc3a0-159">string</span></span> | <span data-ttu-id="dc3a0-160">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="dc3a0-160">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="dc3a0-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc3a0-161">Related topics</span></span>
- [<span data-ttu-id="dc3a0-162">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="dc3a0-162">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="dc3a0-163">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="dc3a0-163">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="dc3a0-164">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="dc3a0-164">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="dc3a0-165">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="dc3a0-165">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="dc3a0-166">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="dc3a0-166">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="dc3a0-167">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="dc3a0-167">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
