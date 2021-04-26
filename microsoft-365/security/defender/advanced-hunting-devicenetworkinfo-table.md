---
title: Table DeviceNetworkInfo dans le schéma de recherche avancé
description: En savoir plus sur les informations de configuration réseau dans la table DeviceNetworkInfo du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, machinenetworkinfo, DeviceNetworkInfo, device, machine, mac, ip, adapter, dns, dhcp, gateway, tunnel
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 11a6fd00524e3dd7ad456f68da6f493d74deee69
ms.sourcegitcommit: 72795ec56a7c4db863dcaaff5e9f7c41c653fda8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "52023188"
---
# <a name="devicenetworkinfo"></a><span data-ttu-id="665dd-104">DeviceNetworkInfo</span><span class="sxs-lookup"><span data-stu-id="665dd-104">DeviceNetworkInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="665dd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="665dd-105">**Applies to:**</span></span>
- <span data-ttu-id="665dd-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="665dd-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="665dd-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="665dd-107">Microsoft Defender for Endpoint</span></span>



<span data-ttu-id="665dd-108">Le tableau du schéma de recherche avancé contient des informations sur la configuration réseau des ordinateurs, notamment les cartes réseau, les adresses IP et MAC, ainsi que les réseaux ou `DeviceNetworkInfo` domaines connectés. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="665dd-108">The `DeviceNetworkInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about networking configuration of machines, including network adapters, IP and MAC addresses, and connected networks or domains.</span></span> <span data-ttu-id="665dd-109">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="665dd-109">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="665dd-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="665dd-110">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="665dd-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="665dd-111">Column name</span></span> | <span data-ttu-id="665dd-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="665dd-112">Data type</span></span> | <span data-ttu-id="665dd-113">Description</span><span class="sxs-lookup"><span data-stu-id="665dd-113">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="665dd-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="665dd-114">datetime</span></span> | <span data-ttu-id="665dd-115">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="665dd-115">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="665dd-116">string</span><span class="sxs-lookup"><span data-stu-id="665dd-116">string</span></span> | <span data-ttu-id="665dd-117">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="665dd-117">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="665dd-118">string</span><span class="sxs-lookup"><span data-stu-id="665dd-118">string</span></span> | <span data-ttu-id="665dd-119">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="665dd-119">Fully qualified domain name (FQDN) of the machine</span></span> |
| `NetworkAdapterName` | <span data-ttu-id="665dd-120">string</span><span class="sxs-lookup"><span data-stu-id="665dd-120">string</span></span> | <span data-ttu-id="665dd-121">Nom de la carte réseau</span><span class="sxs-lookup"><span data-stu-id="665dd-121">Name of the network adapter</span></span> |
| `MacAddress` | <span data-ttu-id="665dd-122">string</span><span class="sxs-lookup"><span data-stu-id="665dd-122">string</span></span> | <span data-ttu-id="665dd-123">Adresse MAC de la carte réseau</span><span class="sxs-lookup"><span data-stu-id="665dd-123">MAC address of the network adapter</span></span> |
| `NetworkAdapterType` | <span data-ttu-id="665dd-124">string</span><span class="sxs-lookup"><span data-stu-id="665dd-124">string</span></span> | <span data-ttu-id="665dd-125">Type de carte réseau.</span><span class="sxs-lookup"><span data-stu-id="665dd-125">Network adapter type.</span></span> <span data-ttu-id="665dd-126">Pour les valeurs possibles, reportez-vous [à cette éumération](/dotnet/api/system.net.networkinformation.networkinterfacetype)</span><span class="sxs-lookup"><span data-stu-id="665dd-126">For the possible values, refer to [this enumeration](/dotnet/api/system.net.networkinformation.networkinterfacetype)</span></span> |
| `NetworkAdapterStatus` | <span data-ttu-id="665dd-127">string</span><span class="sxs-lookup"><span data-stu-id="665dd-127">string</span></span> | <span data-ttu-id="665dd-128">État opérationnel de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="665dd-128">Operational status of the network adapter.</span></span> <span data-ttu-id="665dd-129">Pour les valeurs possibles, reportez-vous [à cette éumération](/dotnet/api/system.net.networkinformation.operationalstatus)</span><span class="sxs-lookup"><span data-stu-id="665dd-129">For the possible values, refer to [this enumeration](/dotnet/api/system.net.networkinformation.operationalstatus)</span></span> |
| `TunnelType` | <span data-ttu-id="665dd-130">string</span><span class="sxs-lookup"><span data-stu-id="665dd-130">string</span></span> | <span data-ttu-id="665dd-131">Protocole tunneling, si l'interface est utilisée à cet effet, par exemple 6to4, Teredo, ISATAP, PPTP, SSTP et SSH</span><span class="sxs-lookup"><span data-stu-id="665dd-131">Tunneling protocol, if the interface is used for this purpose, for example 6to4, Teredo, ISATAP, PPTP, SSTP, and SSH</span></span> |
| `ConnectedNetworks` | <span data-ttu-id="665dd-132">string</span><span class="sxs-lookup"><span data-stu-id="665dd-132">string</span></span> | <span data-ttu-id="665dd-133">Réseaux connectés à l'adaptateur.</span><span class="sxs-lookup"><span data-stu-id="665dd-133">Networks that the adapter is connected to.</span></span> <span data-ttu-id="665dd-134">Chaque tableau JSON contient le nom du réseau, la catégorie (public, privé ou domaine), une description et un indicateur indiquant s'il est connecté publiquement à Internet</span><span class="sxs-lookup"><span data-stu-id="665dd-134">Each JSON array contains the network name, category (public, private or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span> |
| `DnsAddresses` | <span data-ttu-id="665dd-135">string</span><span class="sxs-lookup"><span data-stu-id="665dd-135">string</span></span> | <span data-ttu-id="665dd-136">Adresses de serveur DNS au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="665dd-136">DNS server addresses in JSON array format</span></span> |
| `IPv4Dhcp` | <span data-ttu-id="665dd-137">string</span><span class="sxs-lookup"><span data-stu-id="665dd-137">string</span></span> | <span data-ttu-id="665dd-138">Adresse IPv4 du serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="665dd-138">IPv4 address of DHCP server</span></span> |
| `IPv6Dhcp` | <span data-ttu-id="665dd-139">string</span><span class="sxs-lookup"><span data-stu-id="665dd-139">string</span></span> | <span data-ttu-id="665dd-140">Adresse IPv6 du serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="665dd-140">IPv6 address of DHCP server</span></span> |
| `DefaultGateways` | <span data-ttu-id="665dd-141">string</span><span class="sxs-lookup"><span data-stu-id="665dd-141">string</span></span> | <span data-ttu-id="665dd-142">Adresses de passerelle par défaut au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="665dd-142">Default gateway addresses in JSON array format</span></span> |
| `IPAddresses` | <span data-ttu-id="665dd-143">string</span><span class="sxs-lookup"><span data-stu-id="665dd-143">string</span></span> | <span data-ttu-id="665dd-144">Tableau JSON contenant toutes les adresses IP affectées à l'adaptateur, ainsi que leur préfixe de sous-réseau et espace d'adressace IP respectifs, tels que public, privé ou liaison locale</span><span class="sxs-lookup"><span data-stu-id="665dd-144">JSON array containing all the IP addresses assigned to the adapter, along with their respective subnet prefix and IP address space, such as public, private, or link-local</span></span> |
| `ReportId` | <span data-ttu-id="665dd-145">long</span><span class="sxs-lookup"><span data-stu-id="665dd-145">long</span></span> | <span data-ttu-id="665dd-146">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="665dd-146">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="665dd-147">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp</span><span class="sxs-lookup"><span data-stu-id="665dd-147">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |

## <a name="related-topics"></a><span data-ttu-id="665dd-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="665dd-148">Related topics</span></span>
- [<span data-ttu-id="665dd-149">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="665dd-149">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="665dd-150">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="665dd-150">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="665dd-151">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="665dd-151">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="665dd-152">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="665dd-152">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="665dd-153">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="665dd-153">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="665dd-154">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="665dd-154">Apply query best practices</span></span>](advanced-hunting-best-practices.md)