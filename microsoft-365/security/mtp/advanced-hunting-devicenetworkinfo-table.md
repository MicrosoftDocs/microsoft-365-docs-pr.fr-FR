---
title: Table DeviceNetworkInfo dans le schéma de chasse avancé
description: En savoir plus sur les informations de configuration réseau dans la table DeviceNetworkInfo du schéma de chasse avancé
keywords: recherche avancée, recherche de menace, recherche dans les menaces informatiques, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, machinenetworkinfo, DeviceNetworkInfo, appareil, ordinateur, Mac, IP, adaptateur, DNS, DHCP, passerelle, tunnel
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
ms.collection:
- M365-security-compliance
- m365-initiative-m365-defender
ms.topic: article
ms.openlocfilehash: 05812ec1c747c019bdba1c7ecffc2b33bd5f793a
ms.sourcegitcommit: 5e1b8c959a081022826fb09358730096248507ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48413877"
---
# <a name="devicenetworkinfo"></a><span data-ttu-id="34258-104">DeviceNetworkInfo</span><span class="sxs-lookup"><span data-stu-id="34258-104">DeviceNetworkInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="34258-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="34258-105">**Applies to:**</span></span>
- <span data-ttu-id="34258-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="34258-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="34258-107">Le `DeviceNetworkInfo` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur la configuration réseau des ordinateurs, y compris les cartes réseau, les adresses IP et Mac, ainsi que les réseaux ou domaines connectés.</span><span class="sxs-lookup"><span data-stu-id="34258-107">The `DeviceNetworkInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about networking configuration of machines, including network adapters, IP and MAC addresses, and connected networks or domains.</span></span> <span data-ttu-id="34258-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="34258-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="34258-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="34258-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="34258-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="34258-110">Column name</span></span> | <span data-ttu-id="34258-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="34258-111">Data type</span></span> | <span data-ttu-id="34258-112">Description</span><span class="sxs-lookup"><span data-stu-id="34258-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="34258-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="34258-113">datetime</span></span> | <span data-ttu-id="34258-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="34258-114">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="34258-115">string</span><span class="sxs-lookup"><span data-stu-id="34258-115">string</span></span> | <span data-ttu-id="34258-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="34258-116">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="34258-117">string</span><span class="sxs-lookup"><span data-stu-id="34258-117">string</span></span> | <span data-ttu-id="34258-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="34258-118">Fully qualified domain name (FQDN) of the machine</span></span> |
| `ReportId` | <span data-ttu-id="34258-119">long</span><span class="sxs-lookup"><span data-stu-id="34258-119">long</span></span> | <span data-ttu-id="34258-120">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="34258-120">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="34258-121">Pour identifier les événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et timestamp</span><span class="sxs-lookup"><span data-stu-id="34258-121">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
| `NetworkAdapterName` | <span data-ttu-id="34258-122">string</span><span class="sxs-lookup"><span data-stu-id="34258-122">string</span></span> | <span data-ttu-id="34258-123">Nom de la carte réseau</span><span class="sxs-lookup"><span data-stu-id="34258-123">Name of the network adapter</span></span> |
| `MacAddress` | <span data-ttu-id="34258-124">string</span><span class="sxs-lookup"><span data-stu-id="34258-124">string</span></span> | <span data-ttu-id="34258-125">Adresse MAC de la carte réseau</span><span class="sxs-lookup"><span data-stu-id="34258-125">MAC address of the network adapter</span></span> |
| `NetworkAdapterType` | <span data-ttu-id="34258-126">string</span><span class="sxs-lookup"><span data-stu-id="34258-126">string</span></span> | <span data-ttu-id="34258-127">Type de carte réseau.</span><span class="sxs-lookup"><span data-stu-id="34258-127">Network adapter type.</span></span> <span data-ttu-id="34258-128">Pour les valeurs possibles, reportez-vous à [cette énumération](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype?view=netframework-4.7.2)</span><span class="sxs-lookup"><span data-stu-id="34258-128">For the possible values, refer to [this enumeration](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype?view=netframework-4.7.2)</span></span> |
| `NetworkAdapterStatus` | <span data-ttu-id="34258-129">string</span><span class="sxs-lookup"><span data-stu-id="34258-129">string</span></span> | <span data-ttu-id="34258-130">État opérationnel de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="34258-130">Operational status of the network adapter.</span></span> <span data-ttu-id="34258-131">Pour les valeurs possibles, reportez-vous à [cette énumération](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.operationalstatus?view=netframework-4.7.2)</span><span class="sxs-lookup"><span data-stu-id="34258-131">For the possible values, refer to [this enumeration](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.operationalstatus?view=netframework-4.7.2)</span></span> |
| `TunnelType` | <span data-ttu-id="34258-132">string</span><span class="sxs-lookup"><span data-stu-id="34258-132">string</span></span> | <span data-ttu-id="34258-133">Protocole de tunneling, si l’interface est utilisée à cet effet, par exemple 6to4, Teredo, ISATAP, PPTP, SSTP et SSH</span><span class="sxs-lookup"><span data-stu-id="34258-133">Tunneling protocol, if the interface is used for this purpose, for example 6to4, Teredo, ISATAP, PPTP, SSTP, and SSH</span></span> |
| `ConnectedNetworks` | <span data-ttu-id="34258-134">string</span><span class="sxs-lookup"><span data-stu-id="34258-134">string</span></span> | <span data-ttu-id="34258-135">Réseaux auxquels la carte est connectée.</span><span class="sxs-lookup"><span data-stu-id="34258-135">Networks that the adapter is connected to.</span></span> <span data-ttu-id="34258-136">Chaque tableau JSON contient le nom de réseau, la catégorie (public, Private ou Domain), une description et un indicateur qui indique s’il est connecté publiquement à Internet.</span><span class="sxs-lookup"><span data-stu-id="34258-136">Each JSON array contains the network name, category (public, private or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span> |
| `DnsAddresses` | <span data-ttu-id="34258-137">string</span><span class="sxs-lookup"><span data-stu-id="34258-137">string</span></span> | <span data-ttu-id="34258-138">Adresses de serveur DNS au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="34258-138">DNS server addresses in JSON array format</span></span> |
| `IPv4Dhcp` | <span data-ttu-id="34258-139">string</span><span class="sxs-lookup"><span data-stu-id="34258-139">string</span></span> | <span data-ttu-id="34258-140">Adresse IPv4 du serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="34258-140">IPv4 address of DHCP server</span></span> |
| `IPv6Dhcp` | <span data-ttu-id="34258-141">string</span><span class="sxs-lookup"><span data-stu-id="34258-141">string</span></span> | <span data-ttu-id="34258-142">Adresse IPv6 du serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="34258-142">IPv6 address of DHCP server</span></span> |
| `DefaultGateways` | <span data-ttu-id="34258-143">string</span><span class="sxs-lookup"><span data-stu-id="34258-143">string</span></span> | <span data-ttu-id="34258-144">Adresses de passerelle par défaut au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="34258-144">Default gateway addresses in JSON array format</span></span> |
| `IPAddresses` | <span data-ttu-id="34258-145">string</span><span class="sxs-lookup"><span data-stu-id="34258-145">string</span></span> | <span data-ttu-id="34258-146">Tableau JSON contenant toutes les adresses IP affectées à la carte, ainsi que le préfixe de sous-réseau respectif et l’espace d’adressage IP, tels que public, Private ou Link-local.</span><span class="sxs-lookup"><span data-stu-id="34258-146">JSON array containing all the IP addresses assigned to the adapter, along with their respective subnet prefix and IP address space, such as public, private, or link-local</span></span> |

## <a name="related-topics"></a><span data-ttu-id="34258-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34258-147">Related topics</span></span>
- [<span data-ttu-id="34258-148">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="34258-148">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="34258-149">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="34258-149">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="34258-150">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="34258-150">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="34258-151">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="34258-151">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="34258-152">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="34258-152">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="34258-153">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="34258-153">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
