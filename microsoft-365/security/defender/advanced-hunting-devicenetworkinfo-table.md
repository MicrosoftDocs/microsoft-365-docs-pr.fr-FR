---
title: Table DeviceNetworkInfo dans le schéma de recherche avancé
description: En savoir plus sur les informations de configuration réseau dans le tableau DeviceNetworkInfo du schéma de recherche avancée
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, machinenetworkinfo, DeviceNetworkInfo, device, machine, mac, ip, adapter, dns, dhcp, gateway, tunnel
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
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 9a3806d3e2bff66e04f4adb50217fc1c6f267364
ms.sourcegitcommit: ef98b8a18d275e5b5961e63d2b0743d046321737
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "51382602"
---
# <a name="devicenetworkinfo"></a><span data-ttu-id="8de2b-104">DeviceNetworkInfo</span><span class="sxs-lookup"><span data-stu-id="8de2b-104">DeviceNetworkInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="8de2b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8de2b-105">**Applies to:**</span></span>
- <span data-ttu-id="8de2b-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8de2b-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="8de2b-107">Le tableau du schéma de recherche avancé contient des informations sur la configuration réseau des ordinateurs, notamment les cartes réseau, les adresses IP et MAC, ainsi que les réseaux ou `DeviceNetworkInfo` domaines connectés. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8de2b-107">The `DeviceNetworkInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about networking configuration of machines, including network adapters, IP and MAC addresses, and connected networks or domains.</span></span> <span data-ttu-id="8de2b-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="8de2b-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="8de2b-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8de2b-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="8de2b-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="8de2b-110">Column name</span></span> | <span data-ttu-id="8de2b-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="8de2b-111">Data type</span></span> | <span data-ttu-id="8de2b-112">Description</span><span class="sxs-lookup"><span data-stu-id="8de2b-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="8de2b-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="8de2b-113">datetime</span></span> | <span data-ttu-id="8de2b-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="8de2b-114">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="8de2b-115">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-115">string</span></span> | <span data-ttu-id="8de2b-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="8de2b-116">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="8de2b-117">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-117">string</span></span> | <span data-ttu-id="8de2b-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="8de2b-118">Fully qualified domain name (FQDN) of the machine</span></span> |
| `NetworkAdapterName` | <span data-ttu-id="8de2b-119">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-119">string</span></span> | <span data-ttu-id="8de2b-120">Nom de la carte réseau</span><span class="sxs-lookup"><span data-stu-id="8de2b-120">Name of the network adapter</span></span> |
| `MacAddress` | <span data-ttu-id="8de2b-121">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-121">string</span></span> | <span data-ttu-id="8de2b-122">Adresse MAC de la carte réseau</span><span class="sxs-lookup"><span data-stu-id="8de2b-122">MAC address of the network adapter</span></span> |
| `NetworkAdapterType` | <span data-ttu-id="8de2b-123">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-123">string</span></span> | <span data-ttu-id="8de2b-124">Type de carte réseau.</span><span class="sxs-lookup"><span data-stu-id="8de2b-124">Network adapter type.</span></span> <span data-ttu-id="8de2b-125">Pour les valeurs possibles, reportez-vous [à cette éumération](/dotnet/api/system.net.networkinformation.networkinterfacetype?view=netframework-4.7.2)</span><span class="sxs-lookup"><span data-stu-id="8de2b-125">For the possible values, refer to [this enumeration](/dotnet/api/system.net.networkinformation.networkinterfacetype?view=netframework-4.7.2)</span></span> |
| `NetworkAdapterStatus` | <span data-ttu-id="8de2b-126">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-126">string</span></span> | <span data-ttu-id="8de2b-127">État opérationnel de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="8de2b-127">Operational status of the network adapter.</span></span> <span data-ttu-id="8de2b-128">Pour les valeurs possibles, reportez-vous [à cette éumération](/dotnet/api/system.net.networkinformation.operationalstatus?view=netframework-4.7.2)</span><span class="sxs-lookup"><span data-stu-id="8de2b-128">For the possible values, refer to [this enumeration](/dotnet/api/system.net.networkinformation.operationalstatus?view=netframework-4.7.2)</span></span> |
| `TunnelType` | <span data-ttu-id="8de2b-129">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-129">string</span></span> | <span data-ttu-id="8de2b-130">Protocole tunneling, si l’interface est utilisée à cet effet, par exemple 6to4, Teredo, ISATAP, PPTP, SSTP et SSH</span><span class="sxs-lookup"><span data-stu-id="8de2b-130">Tunneling protocol, if the interface is used for this purpose, for example 6to4, Teredo, ISATAP, PPTP, SSTP, and SSH</span></span> |
| `ConnectedNetworks` | <span data-ttu-id="8de2b-131">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-131">string</span></span> | <span data-ttu-id="8de2b-132">Réseaux connectés à l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="8de2b-132">Networks that the adapter is connected to.</span></span> <span data-ttu-id="8de2b-133">Chaque tableau JSON contient le nom du réseau, la catégorie (public, privé ou domaine), une description et un indicateur indiquant s’il est connecté publiquement à Internet</span><span class="sxs-lookup"><span data-stu-id="8de2b-133">Each JSON array contains the network name, category (public, private or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span> |
| `DnsAddresses` | <span data-ttu-id="8de2b-134">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-134">string</span></span> | <span data-ttu-id="8de2b-135">Adresses de serveur DNS au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="8de2b-135">DNS server addresses in JSON array format</span></span> |
| `IPv4Dhcp` | <span data-ttu-id="8de2b-136">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-136">string</span></span> | <span data-ttu-id="8de2b-137">Adresse IPv4 du serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="8de2b-137">IPv4 address of DHCP server</span></span> |
| `IPv6Dhcp` | <span data-ttu-id="8de2b-138">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-138">string</span></span> | <span data-ttu-id="8de2b-139">Adresse IPv6 du serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="8de2b-139">IPv6 address of DHCP server</span></span> |
| `DefaultGateways` | <span data-ttu-id="8de2b-140">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-140">string</span></span> | <span data-ttu-id="8de2b-141">Adresses de passerelle par défaut au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="8de2b-141">Default gateway addresses in JSON array format</span></span> |
| `IPAddresses` | <span data-ttu-id="8de2b-142">string</span><span class="sxs-lookup"><span data-stu-id="8de2b-142">string</span></span> | <span data-ttu-id="8de2b-143">Tableau JSON contenant toutes les adresses IP affectées à l’adaptateur, ainsi que leur préfixe de sous-réseau et espace d’adressace IP respectifs, tels que public, privé ou liaison locale</span><span class="sxs-lookup"><span data-stu-id="8de2b-143">JSON array containing all the IP addresses assigned to the adapter, along with their respective subnet prefix and IP address space, such as public, private, or link-local</span></span> |
| `ReportId` | <span data-ttu-id="8de2b-144">long</span><span class="sxs-lookup"><span data-stu-id="8de2b-144">long</span></span> | <span data-ttu-id="8de2b-145">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="8de2b-145">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="8de2b-146">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp</span><span class="sxs-lookup"><span data-stu-id="8de2b-146">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |

## <a name="related-topics"></a><span data-ttu-id="8de2b-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8de2b-147">Related topics</span></span>
- [<span data-ttu-id="8de2b-148">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="8de2b-148">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="8de2b-149">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="8de2b-149">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="8de2b-150">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="8de2b-150">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="8de2b-151">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="8de2b-151">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="8de2b-152">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="8de2b-152">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="8de2b-153">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="8de2b-153">Apply query best practices</span></span>](advanced-hunting-best-practices.md)