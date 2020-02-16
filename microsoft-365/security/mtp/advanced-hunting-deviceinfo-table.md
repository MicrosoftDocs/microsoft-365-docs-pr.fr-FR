---
title: Table DeviceInfo dans le schéma de chasse avancé
description: En savoir plus sur le système d’exploitation, le nom de l’ordinateur et d’autres informations sur l’ordinateur dans le tableau DeviceInfo du schéma de chasse avancé
keywords: chasse avancée, recherche de menace, recherche dans les menaces de la cybercriminalité, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, MachineInfo, DeviceInfo, appareil, ordinateur, se, plateforme , les utilisateurs
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
ms.openlocfilehash: 58fd70ce62fc2e15f703063d1f8efe62df02c57d
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42087973"
---
# <a name="deviceinfo"></a><span data-ttu-id="be31b-104">DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="be31b-104">DeviceInfo</span></span>

<span data-ttu-id="be31b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="be31b-105">**Applies to:**</span></span>
- <span data-ttu-id="be31b-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="be31b-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="be31b-107">Le `DeviceInfo` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les ordinateurs de l’organisation, y compris la version du système d’exploitation, les utilisateurs actifs et le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="be31b-107">The `DeviceInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about machines in the organization, including OS version, active users, and computer name.</span></span> <span data-ttu-id="be31b-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="be31b-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="be31b-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="be31b-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="be31b-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="be31b-110">Column name</span></span> | <span data-ttu-id="be31b-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="be31b-111">Data type</span></span> | <span data-ttu-id="be31b-112">Description</span><span class="sxs-lookup"><span data-stu-id="be31b-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="be31b-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="be31b-113">datetime</span></span> | <span data-ttu-id="be31b-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="be31b-114">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="be31b-115">chaîne</span><span class="sxs-lookup"><span data-stu-id="be31b-115">string</span></span> | <span data-ttu-id="be31b-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="be31b-116">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="be31b-117">string</span><span class="sxs-lookup"><span data-stu-id="be31b-117">string</span></span> | <span data-ttu-id="be31b-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="be31b-118">Fully qualified domain name (FQDN) of the machine</span></span> |
| `ClientVersion` | <span data-ttu-id="be31b-119">string</span><span class="sxs-lookup"><span data-stu-id="be31b-119">string</span></span> | <span data-ttu-id="be31b-120">Version de l’agent de point de terminaison ou du capteur exécuté sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="be31b-120">Version of the endpoint agent or sensor running on the machine</span></span> |
| `PublicIP` | <span data-ttu-id="be31b-121">string</span><span class="sxs-lookup"><span data-stu-id="be31b-121">string</span></span> | <span data-ttu-id="be31b-122">Adresse IP publique utilisée par l’ordinateur intégré pour se connecter au service ATP de Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="be31b-122">Public IP address used by the onboarded machine to connect to the Microsoft Defender ATP service.</span></span> <span data-ttu-id="be31b-123">Il peut s’agir de l’adresse IP de l’ordinateur lui-même, d’un périphérique NAT ou d’un proxy.</span><span class="sxs-lookup"><span data-stu-id="be31b-123">This could be the IP address of the machine itself, a NAT device, or a proxy</span></span> |
| `OSArchitecture` | <span data-ttu-id="be31b-124">string</span><span class="sxs-lookup"><span data-stu-id="be31b-124">string</span></span> | <span data-ttu-id="be31b-125">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="be31b-125">Architecture of the operating system running on the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="be31b-126">string</span><span class="sxs-lookup"><span data-stu-id="be31b-126">string</span></span> | <span data-ttu-id="be31b-127">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="be31b-127">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="be31b-128">Cela indique les systèmes d’exploitation spécifiques, y compris les variantes au sein de la même famille, telles que Windows 10 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="be31b-128">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7</span></span> |
| `OSBuild` | <span data-ttu-id="be31b-129">string</span><span class="sxs-lookup"><span data-stu-id="be31b-129">string</span></span> | <span data-ttu-id="be31b-130">Version du système d’exploitation en cours d’exécution sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="be31b-130">Build version of the operating system running on the machine</span></span> |
| `IsAzureADJoined` | <span data-ttu-id="be31b-131">booléen</span><span class="sxs-lookup"><span data-stu-id="be31b-131">boolean</span></span> | <span data-ttu-id="be31b-132">Indicateur booléen indiquant si l’ordinateur est joint à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="be31b-132">Boolean indicator of whether machine is joined to the Azure Active Directory</span></span> |
| `LoggedOnUsers` | <span data-ttu-id="be31b-133">string</span><span class="sxs-lookup"><span data-stu-id="be31b-133">string</span></span> | <span data-ttu-id="be31b-134">Liste de tous les utilisateurs qui ont ouvert une session sur l’ordinateur au moment de l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="be31b-134">List of all users that are logged on the machine at the time of the event in JSON array format</span></span> |
| `RegistryDeviceTag` | <span data-ttu-id="be31b-135">string</span><span class="sxs-lookup"><span data-stu-id="be31b-135">string</span></span> | <span data-ttu-id="be31b-136">Balise d’ordinateur ajoutée via le registre</span><span class="sxs-lookup"><span data-stu-id="be31b-136">Machine tag added through the registry</span></span> |
| `ReportId` | <span data-ttu-id="be31b-137">long</span><span class="sxs-lookup"><span data-stu-id="be31b-137">long</span></span> | <span data-ttu-id="be31b-138">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="be31b-138">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="be31b-139">Pour identifier les événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et timestamp</span><span class="sxs-lookup"><span data-stu-id="be31b-139">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
| `OSVersion` | <span data-ttu-id="be31b-140">string</span><span class="sxs-lookup"><span data-stu-id="be31b-140">string</span></span> | <span data-ttu-id="be31b-141">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="be31b-141">Version of the operating system running on the machine</span></span> |
| `MachineGroup` | <span data-ttu-id="be31b-142">string</span><span class="sxs-lookup"><span data-stu-id="be31b-142">string</span></span> | <span data-ttu-id="be31b-143">Groupe d’ordinateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="be31b-143">Machine group of the machine.</span></span> <span data-ttu-id="be31b-144">Ce groupe est utilisé par le contrôle d’accès basé sur un rôle pour déterminer l’accès à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="be31b-144">This group is used by role-based access control to determine access to the machine</span></span> |

## <a name="related-topics"></a><span data-ttu-id="be31b-145">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="be31b-145">Related topics</span></span>
- [<span data-ttu-id="be31b-146">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="be31b-146">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="be31b-147">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="be31b-147">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="be31b-148">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="be31b-148">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="be31b-149">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="be31b-149">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="be31b-150">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="be31b-150">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="be31b-151">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="be31b-151">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
