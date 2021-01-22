---
title: Table DeviceInfo dans le schéma de recherche avancée
description: En savoir plus sur le système d’exploitation, le nom de l’ordinateur et d’autres informations sur l’ordinateur dans la table DeviceInfo du schéma de recherche avancée
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, machineinfo, DeviceInfo, device, machine, OS, platform, users
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
ms.openlocfilehash: e445902ee83b734f84d02607905413a14c016b8f
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49931277"
---
# <a name="deviceinfo"></a><span data-ttu-id="920df-104">DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="920df-104">DeviceInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="920df-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="920df-105">**Applies to:**</span></span>
- <span data-ttu-id="920df-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="920df-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="920df-107">Le tableau du schéma de recherche avancée contient des informations sur les ordinateurs de l’organisation, notamment la version du système d’exploitation, les utilisateurs `DeviceInfo` actifs et le nom de l’ordinateur. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="920df-107">The `DeviceInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about machines in the organization, including OS version, active users, and computer name.</span></span> <span data-ttu-id="920df-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="920df-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="920df-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="920df-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="920df-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="920df-110">Column name</span></span> | <span data-ttu-id="920df-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="920df-111">Data type</span></span> | <span data-ttu-id="920df-112">Description</span><span class="sxs-lookup"><span data-stu-id="920df-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="920df-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="920df-113">datetime</span></span> | <span data-ttu-id="920df-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="920df-114">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="920df-115">string</span><span class="sxs-lookup"><span data-stu-id="920df-115">string</span></span> | <span data-ttu-id="920df-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="920df-116">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="920df-117">string</span><span class="sxs-lookup"><span data-stu-id="920df-117">string</span></span> | <span data-ttu-id="920df-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="920df-118">Fully qualified domain name (FQDN) of the machine</span></span> |
| `ClientVersion` | <span data-ttu-id="920df-119">string</span><span class="sxs-lookup"><span data-stu-id="920df-119">string</span></span> | <span data-ttu-id="920df-120">Version de l’agent de point de terminaison ou du capteur en cours d’exécution sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="920df-120">Version of the endpoint agent or sensor running on the machine</span></span> |
| `PublicIP` | <span data-ttu-id="920df-121">string</span><span class="sxs-lookup"><span data-stu-id="920df-121">string</span></span> | <span data-ttu-id="920df-122">Adresse IP publique utilisée par l’ordinateur intégré pour se connecter au service Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="920df-122">Public IP address used by the onboarded machine to connect to the Microsoft  Defender for Endpoint service.</span></span> <span data-ttu-id="920df-123">Il peut s’agit de l’adresse IP de l’ordinateur lui-même, d’un périphérique NAT ou d’un proxy</span><span class="sxs-lookup"><span data-stu-id="920df-123">This could be the IP address of the machine itself, a NAT device, or a proxy</span></span> |
| `OSArchitecture` | <span data-ttu-id="920df-124">string</span><span class="sxs-lookup"><span data-stu-id="920df-124">string</span></span> | <span data-ttu-id="920df-125">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="920df-125">Architecture of the operating system running on the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="920df-126">string</span><span class="sxs-lookup"><span data-stu-id="920df-126">string</span></span> | <span data-ttu-id="920df-127">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="920df-127">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="920df-128">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein de la même famille, tels que Windows 10 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="920df-128">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7</span></span> |
| `OSBuild` | <span data-ttu-id="920df-129">string</span><span class="sxs-lookup"><span data-stu-id="920df-129">string</span></span> | <span data-ttu-id="920df-130">Version de build du système d’exploitation en cours d’exécution sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="920df-130">Build version of the operating system running on the machine</span></span> |
| `IsAzureADJoined` | <span data-ttu-id="920df-131">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="920df-131">boolean</span></span> | <span data-ttu-id="920df-132">Indicateur booléen pour savoir si l’ordinateur est joint à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="920df-132">Boolean indicator of whether machine is joined to the Azure Active Directory</span></span> |
| `LoggedOnUsers` | <span data-ttu-id="920df-133">string</span><span class="sxs-lookup"><span data-stu-id="920df-133">string</span></span> | <span data-ttu-id="920df-134">Liste de tous les utilisateurs connectés à l’ordinateur au moment de l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="920df-134">List of all users that are logged on the machine at the time of the event in JSON array format</span></span> |
| `RegistryDeviceTag` | <span data-ttu-id="920df-135">string</span><span class="sxs-lookup"><span data-stu-id="920df-135">string</span></span> | <span data-ttu-id="920df-136">Balise d’ordinateur ajoutée via le Registre</span><span class="sxs-lookup"><span data-stu-id="920df-136">Machine tag added through the registry</span></span> |
| `ReportId` | <span data-ttu-id="920df-137">long</span><span class="sxs-lookup"><span data-stu-id="920df-137">long</span></span> | <span data-ttu-id="920df-138">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="920df-138">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="920df-139">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp</span><span class="sxs-lookup"><span data-stu-id="920df-139">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
| `OSVersion` | <span data-ttu-id="920df-140">string</span><span class="sxs-lookup"><span data-stu-id="920df-140">string</span></span> | <span data-ttu-id="920df-141">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="920df-141">Version of the operating system running on the machine</span></span> |
| `MachineGroup` | <span data-ttu-id="920df-142">string</span><span class="sxs-lookup"><span data-stu-id="920df-142">string</span></span> | <span data-ttu-id="920df-143">Groupe d’ordinateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="920df-143">Machine group of the machine.</span></span> <span data-ttu-id="920df-144">Ce groupe est utilisé par le contrôle d’accès basé sur un rôle pour déterminer l’accès à l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="920df-144">This group is used by role-based access control to determine access to the machine</span></span> |

## <a name="related-topics"></a><span data-ttu-id="920df-145">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="920df-145">Related topics</span></span>
- [<span data-ttu-id="920df-146">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="920df-146">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="920df-147">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="920df-147">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="920df-148">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="920df-148">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="920df-149">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="920df-149">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="920df-150">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="920df-150">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="920df-151">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="920df-151">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
