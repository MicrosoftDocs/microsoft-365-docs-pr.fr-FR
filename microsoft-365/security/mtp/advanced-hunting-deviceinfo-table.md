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
ms.openlocfilehash: ab7e48eaf582dbf6bc26d0393d26fea433da2253
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41600441"
---
# <a name="deviceinfo"></a><span data-ttu-id="7f56c-104">DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="7f56c-104">DeviceInfo</span></span>

<span data-ttu-id="7f56c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7f56c-105">**Applies to:**</span></span>
- <span data-ttu-id="7f56c-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="7f56c-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="7f56c-107">Le `DeviceInfo` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les ordinateurs de l’organisation, y compris la version du système d’exploitation, les utilisateurs actifs et le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f56c-107">The `DeviceInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about machines in the organization, including OS version, active users, and computer name.</span></span> <span data-ttu-id="7f56c-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="7f56c-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="7f56c-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7f56c-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="7f56c-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7f56c-110">Column name</span></span> | <span data-ttu-id="7f56c-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="7f56c-111">Data type</span></span> | <span data-ttu-id="7f56c-112">Description</span><span class="sxs-lookup"><span data-stu-id="7f56c-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="7f56c-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="7f56c-113">datetime</span></span> | <span data-ttu-id="7f56c-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="7f56c-114">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="7f56c-115">chaîne</span><span class="sxs-lookup"><span data-stu-id="7f56c-115">string</span></span> | <span data-ttu-id="7f56c-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="7f56c-116">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="7f56c-117">string</span><span class="sxs-lookup"><span data-stu-id="7f56c-117">string</span></span> | <span data-ttu-id="7f56c-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="7f56c-118">Fully qualified domain name (FQDN) of the machine</span></span> |
| `ClientVersion` | <span data-ttu-id="7f56c-119">string</span><span class="sxs-lookup"><span data-stu-id="7f56c-119">string</span></span> | <span data-ttu-id="7f56c-120">Version de l’agent de point de terminaison ou du capteur exécuté sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="7f56c-120">Version of the endpoint agent or sensor running on the machine</span></span> |
| `PublicIP` | <span data-ttu-id="7f56c-121">string</span><span class="sxs-lookup"><span data-stu-id="7f56c-121">string</span></span> | <span data-ttu-id="7f56c-122">Adresse IP publique utilisée par l’ordinateur intégré pour se connecter au service ATP de Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="7f56c-122">Public IP address used by the onboarded machine to connect to the Microsoft Defender ATP service.</span></span> <span data-ttu-id="7f56c-123">Il peut s’agir de l’adresse IP de l’ordinateur lui-même, d’un périphérique NAT ou d’un proxy.</span><span class="sxs-lookup"><span data-stu-id="7f56c-123">This could be the IP address of the machine itself, a NAT device, or a proxy</span></span> |
| `OSArchitecture` | <span data-ttu-id="7f56c-124">string</span><span class="sxs-lookup"><span data-stu-id="7f56c-124">string</span></span> | <span data-ttu-id="7f56c-125">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="7f56c-125">Architecture of the operating system running on the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="7f56c-126">string</span><span class="sxs-lookup"><span data-stu-id="7f56c-126">string</span></span> | <span data-ttu-id="7f56c-127">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="7f56c-127">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="7f56c-128">Cela indique les systèmes d’exploitation spécifiques, y compris les variantes au sein de la même famille, telles que Windows 10 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f56c-128">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7</span></span> |
| `OSBuild` | <span data-ttu-id="7f56c-129">string</span><span class="sxs-lookup"><span data-stu-id="7f56c-129">string</span></span> | <span data-ttu-id="7f56c-130">Version du système d’exploitation en cours d’exécution sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="7f56c-130">Build version of the operating system running on the machine</span></span> |
| `IsAzureADJoined` | <span data-ttu-id="7f56c-131">booléen</span><span class="sxs-lookup"><span data-stu-id="7f56c-131">boolean</span></span> | <span data-ttu-id="7f56c-132">Indicateur booléen indiquant si l’ordinateur est joint à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="7f56c-132">Boolean indicator of whether machine is joined to the Azure Active Directory</span></span> |
| `LoggedOnUsers` | <span data-ttu-id="7f56c-133">string</span><span class="sxs-lookup"><span data-stu-id="7f56c-133">string</span></span> | <span data-ttu-id="7f56c-134">Liste de tous les utilisateurs qui ont ouvert une session sur l’ordinateur au moment de l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="7f56c-134">List of all users that are logged on the machine at the time of the event in JSON array format</span></span> |
| `RegistryDeviceTag` | <span data-ttu-id="7f56c-135">string</span><span class="sxs-lookup"><span data-stu-id="7f56c-135">string</span></span> | <span data-ttu-id="7f56c-136">Balise d’ordinateur ajoutée via le registre</span><span class="sxs-lookup"><span data-stu-id="7f56c-136">Machine tag added through the registry</span></span> |
| `ReportId` | <span data-ttu-id="7f56c-137">long</span><span class="sxs-lookup"><span data-stu-id="7f56c-137">long</span></span> | <span data-ttu-id="7f56c-138">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="7f56c-138">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="7f56c-139">Pour identifier les événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et timestamp</span><span class="sxs-lookup"><span data-stu-id="7f56c-139">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
| `OSVersion` | <span data-ttu-id="7f56c-140">string</span><span class="sxs-lookup"><span data-stu-id="7f56c-140">string</span></span> | <span data-ttu-id="7f56c-141">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="7f56c-141">Version of the operating system running on the machine</span></span> |
| `MachineGroup` | <span data-ttu-id="7f56c-142">string</span><span class="sxs-lookup"><span data-stu-id="7f56c-142">string</span></span> | <span data-ttu-id="7f56c-143">Groupe d’ordinateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f56c-143">Machine group of the machine.</span></span> <span data-ttu-id="7f56c-144">Ce groupe est utilisé par le contrôle d’accès basé sur un rôle pour déterminer l’accès à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f56c-144">This group is used by role-based access control to determine access to the machine</span></span> |

## <a name="related-topics"></a><span data-ttu-id="7f56c-145">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="7f56c-145">Related topics</span></span>
- [<span data-ttu-id="7f56c-146">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="7f56c-146">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="7f56c-147">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="7f56c-147">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="7f56c-148">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="7f56c-148">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="7f56c-149">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="7f56c-149">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="7f56c-150">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="7f56c-150">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="7f56c-151">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="7f56c-151">Apply query best practices</span></span>](advanced-hunting-best-practices.md)