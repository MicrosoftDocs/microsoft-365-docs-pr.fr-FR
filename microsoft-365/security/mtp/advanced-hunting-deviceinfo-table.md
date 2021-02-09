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
ms.openlocfilehash: 6462096a6c1b44ee11299f652a54f261d0355523
ms.sourcegitcommit: 005028af7c5a6b2e95f17a0037958131484d9e73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2021
ms.locfileid: "50145366"
---
# <a name="deviceinfo"></a><span data-ttu-id="40213-104">DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="40213-104">DeviceInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="40213-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="40213-105">**Applies to:**</span></span>
- <span data-ttu-id="40213-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="40213-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="40213-107">Le tableau du schéma de recherche avancée contient des informations sur les ordinateurs de l’organisation, notamment la version du système d’exploitation, les utilisateurs `DeviceInfo` actifs et le nom de l’ordinateur. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="40213-107">The `DeviceInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about machines in the organization, including OS version, active users, and computer name.</span></span> <span data-ttu-id="40213-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="40213-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="40213-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="40213-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="40213-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="40213-110">Column name</span></span> | <span data-ttu-id="40213-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="40213-111">Data type</span></span> | <span data-ttu-id="40213-112">Description</span><span class="sxs-lookup"><span data-stu-id="40213-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="40213-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="40213-113">datetime</span></span> | <span data-ttu-id="40213-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="40213-114">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="40213-115">string</span><span class="sxs-lookup"><span data-stu-id="40213-115">string</span></span> | <span data-ttu-id="40213-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="40213-116">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="40213-117">string</span><span class="sxs-lookup"><span data-stu-id="40213-117">string</span></span> | <span data-ttu-id="40213-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="40213-118">Fully qualified domain name (FQDN) of the machine</span></span> |
| `ClientVersion` | <span data-ttu-id="40213-119">string</span><span class="sxs-lookup"><span data-stu-id="40213-119">string</span></span> | <span data-ttu-id="40213-120">Version de l’agent de point de terminaison ou du capteur en cours d’exécution sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="40213-120">Version of the endpoint agent or sensor running on the machine</span></span> |
| `PublicIP` | <span data-ttu-id="40213-121">string</span><span class="sxs-lookup"><span data-stu-id="40213-121">string</span></span> | <span data-ttu-id="40213-122">Adresse IP publique utilisée par l’ordinateur intégré pour se connecter au service Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="40213-122">Public IP address used by the onboarded machine to connect to the Microsoft  Defender for Endpoint service.</span></span> <span data-ttu-id="40213-123">Il peut s’agit de l’adresse IP de l’ordinateur lui-même, d’un périphérique NAT ou d’un proxy.</span><span class="sxs-lookup"><span data-stu-id="40213-123">This could be the IP address of the machine itself, a NAT device, or a proxy</span></span> |
| `OSArchitecture` | <span data-ttu-id="40213-124">string</span><span class="sxs-lookup"><span data-stu-id="40213-124">string</span></span> | <span data-ttu-id="40213-125">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="40213-125">Architecture of the operating system running on the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="40213-126">string</span><span class="sxs-lookup"><span data-stu-id="40213-126">string</span></span> | <span data-ttu-id="40213-127">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="40213-127">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="40213-128">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein de la même famille, tels que Windows 10 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="40213-128">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7</span></span> |
| `OSBuild` | <span data-ttu-id="40213-129">string</span><span class="sxs-lookup"><span data-stu-id="40213-129">string</span></span> | <span data-ttu-id="40213-130">Version de build du système d’exploitation en cours d’exécution sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="40213-130">Build version of the operating system running on the machine</span></span> |
| `IsAzureADJoined` | <span data-ttu-id="40213-131">booléen</span><span class="sxs-lookup"><span data-stu-id="40213-131">boolean</span></span> | <span data-ttu-id="40213-132">Indicateur booléen pour savoir si l’ordinateur est joint à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="40213-132">Boolean indicator of whether machine is joined to the Azure Active Directory</span></span> |
| `DeviceObjectId` | <span data-ttu-id="40213-133">string</span><span class="sxs-lookup"><span data-stu-id="40213-133">string</span></span> | <span data-ttu-id="40213-134">Identificateur unique de l’appareil dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="40213-134">Unique identifier for the device in Azure AD</span></span> |
| `LoggedOnUsers` | <span data-ttu-id="40213-135">string</span><span class="sxs-lookup"><span data-stu-id="40213-135">string</span></span> | <span data-ttu-id="40213-136">Liste de tous les utilisateurs connectés à l’ordinateur au moment de l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="40213-136">List of all users that are logged on the machine at the time of the event in JSON array format</span></span> |
| `RegistryDeviceTag` | <span data-ttu-id="40213-137">string</span><span class="sxs-lookup"><span data-stu-id="40213-137">string</span></span> | <span data-ttu-id="40213-138">Balise d’ordinateur ajoutée via le Registre</span><span class="sxs-lookup"><span data-stu-id="40213-138">Machine tag added through the registry</span></span> |
| `ReportId` | <span data-ttu-id="40213-139">long</span><span class="sxs-lookup"><span data-stu-id="40213-139">long</span></span> | <span data-ttu-id="40213-140">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="40213-140">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="40213-141">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp</span><span class="sxs-lookup"><span data-stu-id="40213-141">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
|`AdditionalFields` | <span data-ttu-id="40213-142">string</span><span class="sxs-lookup"><span data-stu-id="40213-142">string</span></span> | <span data-ttu-id="40213-143">Informations supplémentaires sur l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="40213-143">Additional information about the event in JSON array format</span></span> |
| `OSVersion` | <span data-ttu-id="40213-144">string</span><span class="sxs-lookup"><span data-stu-id="40213-144">string</span></span> | <span data-ttu-id="40213-145">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="40213-145">Version of the operating system running on the machine</span></span> |
| `MachineGroup` | <span data-ttu-id="40213-146">string</span><span class="sxs-lookup"><span data-stu-id="40213-146">string</span></span> | <span data-ttu-id="40213-147">Groupe d’ordinateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="40213-147">Machine group of the machine.</span></span> <span data-ttu-id="40213-148">Ce groupe est utilisé par le contrôle d’accès basé sur un rôle pour déterminer l’accès à l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="40213-148">This group is used by role-based access control to determine access to the machine</span></span> |

## <a name="related-topics"></a><span data-ttu-id="40213-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="40213-149">Related topics</span></span>
- [<span data-ttu-id="40213-150">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="40213-150">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="40213-151">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="40213-151">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="40213-152">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="40213-152">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="40213-153">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="40213-153">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="40213-154">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="40213-154">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="40213-155">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="40213-155">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
