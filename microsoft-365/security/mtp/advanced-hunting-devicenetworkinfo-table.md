---
title: Table DeviceNetworkInfo dans le schéma de chasse avancé
description: En savoir plus sur les informations de configuration réseau dans la table DeviceNetworkInfo du schéma de chasse avancé
keywords: chasse aux menaces, recherche de menace, recherche sur les menaces de la cybercriminalité, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, machinenetworkinfo, DeviceNetworkInfo, appareil, ordinateur, Mac, IP, adaptateur, DNS, DHCP, passerelle, tunnel
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
ms.openlocfilehash: ce392ee074327114b0794edfeef9eb83091447d6
ms.sourcegitcommit: 74bf600424d0cb7b9d16b4f391aeda7875058be1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42234993"
---
# <a name="devicenetworkinfo"></a><span data-ttu-id="5cc0e-104">DeviceNetworkInfo</span><span class="sxs-lookup"><span data-stu-id="5cc0e-104">DeviceNetworkInfo</span></span>

<span data-ttu-id="5cc0e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5cc0e-105">**Applies to:**</span></span>
- <span data-ttu-id="5cc0e-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="5cc0e-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="5cc0e-107">Le `DeviceNetworkInfo` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur la configuration réseau des ordinateurs, y compris les cartes réseau, les adresses IP et Mac, ainsi que les réseaux ou domaines connectés.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-107">The `DeviceNetworkInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about networking configuration of machines, including network adapters, IP and MAC addresses, and connected networks or domains.</span></span> <span data-ttu-id="5cc0e-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="5cc0e-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5cc0e-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="5cc0e-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="5cc0e-110">Column name</span></span> | <span data-ttu-id="5cc0e-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="5cc0e-111">Data type</span></span> | <span data-ttu-id="5cc0e-112">Description</span><span class="sxs-lookup"><span data-stu-id="5cc0e-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="5cc0e-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="5cc0e-113">datetime</span></span> | <span data-ttu-id="5cc0e-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="5cc0e-114">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="5cc0e-115">chaîne</span><span class="sxs-lookup"><span data-stu-id="5cc0e-115">string</span></span> | <span data-ttu-id="5cc0e-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="5cc0e-116">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="5cc0e-117">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-117">string</span></span> | <span data-ttu-id="5cc0e-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="5cc0e-118">Fully qualified domain name (FQDN) of the machine</span></span> |
| `ReportId` | <span data-ttu-id="5cc0e-119">long</span><span class="sxs-lookup"><span data-stu-id="5cc0e-119">long</span></span> | <span data-ttu-id="5cc0e-120">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-120">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="5cc0e-121">Pour identifier les événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et timestamp</span><span class="sxs-lookup"><span data-stu-id="5cc0e-121">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
| `NetworkAdapterName` | <span data-ttu-id="5cc0e-122">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-122">string</span></span> | <span data-ttu-id="5cc0e-123">Nom de la carte réseau</span><span class="sxs-lookup"><span data-stu-id="5cc0e-123">Name of the network adapter</span></span> |
| `MacAddress` | <span data-ttu-id="5cc0e-124">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-124">string</span></span> | <span data-ttu-id="5cc0e-125">Adresse MAC de la carte réseau</span><span class="sxs-lookup"><span data-stu-id="5cc0e-125">MAC address of the network adapter</span></span> |
| `NetworkAdapterType` | <span data-ttu-id="5cc0e-126">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-126">string</span></span> | <span data-ttu-id="5cc0e-127">Type de carte réseau.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-127">Network adapter type.</span></span> <span data-ttu-id="5cc0e-128">Pour les valeurs possibles, reportez-vous à [cette énumération](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype?view=netframework-4.7.2)</span><span class="sxs-lookup"><span data-stu-id="5cc0e-128">For the possible values, refer to [this enumeration](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype?view=netframework-4.7.2)</span></span> |
| `NetworkAdapterStatus` | <span data-ttu-id="5cc0e-129">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-129">string</span></span> | <span data-ttu-id="5cc0e-130">État opérationnel de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-130">Operational status of the network adapter.</span></span> <span data-ttu-id="5cc0e-131">Pour les valeurs possibles, reportez-vous à [cette énumération](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.operationalstatus?view=netframework-4.7.2)</span><span class="sxs-lookup"><span data-stu-id="5cc0e-131">For the possible values, refer to [this enumeration](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.operationalstatus?view=netframework-4.7.2)</span></span> |
| `TunnelType` | <span data-ttu-id="5cc0e-132">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-132">string</span></span> | <span data-ttu-id="5cc0e-133">Protocole de tunneling, si l’interface est utilisée à cet effet, par exemple 6to4, Teredo, ISATAP, PPTP, SSTP et SSH</span><span class="sxs-lookup"><span data-stu-id="5cc0e-133">Tunneling protocol, if the interface is used for this purpose, for example 6to4, Teredo, ISATAP, PPTP, SSTP, and SSH</span></span> |
| `ConnectedNetworks` | <span data-ttu-id="5cc0e-134">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-134">string</span></span> | <span data-ttu-id="5cc0e-135">Réseaux auxquels la carte est connectée.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-135">Networks that the adapter is connected to.</span></span> <span data-ttu-id="5cc0e-136">Chaque tableau JSON contient le nom de réseau, la catégorie (public, Private ou Domain), une description et un indicateur qui indique s’il est connecté publiquement à Internet.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-136">Each JSON array contains the network name, category (public, private or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span> |
| `DnsAddresses` | <span data-ttu-id="5cc0e-137">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-137">string</span></span> | <span data-ttu-id="5cc0e-138">Adresses de serveur DNS au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="5cc0e-138">DNS server addresses in JSON array format</span></span> |
| `IPv4Dhcp` | <span data-ttu-id="5cc0e-139">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-139">string</span></span> | <span data-ttu-id="5cc0e-140">Adresse IPv4 du serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="5cc0e-140">IPv4 address of DHCP server</span></span> |
| `IPv6Dhcp` | <span data-ttu-id="5cc0e-141">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-141">string</span></span> | <span data-ttu-id="5cc0e-142">Adresse IPv6 du serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="5cc0e-142">IPv6 address of DHCP server</span></span> |
| `DefaultGateways` | <span data-ttu-id="5cc0e-143">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-143">string</span></span> | <span data-ttu-id="5cc0e-144">Adresses de passerelle par défaut au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="5cc0e-144">Default gateway addresses in JSON array format</span></span> |
| `IPAddresses` | <span data-ttu-id="5cc0e-145">string</span><span class="sxs-lookup"><span data-stu-id="5cc0e-145">string</span></span> | <span data-ttu-id="5cc0e-146">Tableau JSON contenant toutes les adresses IP affectées à la carte, ainsi que le préfixe de sous-réseau respectif et l’espace d’adressage IP, tels que public, Private ou Link-local.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-146">JSON array containing all the IP addresses assigned to the adapter, along with their respective subnet prefix and IP address space, such as public, private, or link-local</span></span> |

## <a name="related-topics"></a><span data-ttu-id="5cc0e-147">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="5cc0e-147">Related topics</span></span>
- [<span data-ttu-id="5cc0e-148">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="5cc0e-148">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="5cc0e-149">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="5cc0e-149">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="5cc0e-150">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="5cc0e-150">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="5cc0e-151">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="5cc0e-151">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="5cc0e-152">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="5cc0e-152">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="5cc0e-153">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="5cc0e-153">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
