---
title: Table DeviceNetworkInfo dans le schéma de recherche avancé
description: En savoir plus sur les informations de configuration réseau dans la table DeviceNetworkInfo du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, search, query, telemetry, schema reference, kusto, table, column, data type, description, devicenetworkinfo, device, device, device, mac, ip, adapter, dns, dhcp, gateway, tunnel, DeviceNetworkInfo
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 4ba3e81163cdbba54bf718dca929e2df3b39a1c3
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067054"
---
# <a name="devicenetworkinfo"></a><span data-ttu-id="f0539-104">DeviceNetworkInfo</span><span class="sxs-lookup"><span data-stu-id="f0539-104">DeviceNetworkInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f0539-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f0539-105">**Applies to:**</span></span>
- [<span data-ttu-id="f0539-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f0539-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

><span data-ttu-id="f0539-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="f0539-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="f0539-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f0539-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

<span data-ttu-id="f0539-109">Le tableau du schéma de recherche avancé contient des informations sur la configuration réseau des appareils, notamment les cartes réseau, les adresses IP et MAC, ainsi que les réseaux ou `DeviceNetworkInfo` domaines connectés. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="f0539-109">The `DeviceNetworkInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about networking configuration of devices, including network adapters, IP and MAC addresses, and connected networks or domains.</span></span> <span data-ttu-id="f0539-110">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="f0539-110">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="f0539-111">Pour plus d’informations sur les autres tableaux du schéma de chasse avancé, voir la référence de schéma [de chasse avancée.](advanced-hunting-schema-reference.md)</span><span class="sxs-lookup"><span data-stu-id="f0539-111">For information on other tables in the advanced hunting schema, see [the advanced hunting schema reference](advanced-hunting-schema-reference.md).</span></span>

| <span data-ttu-id="f0539-112">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="f0539-112">Column name</span></span> | <span data-ttu-id="f0539-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="f0539-113">Data type</span></span> | <span data-ttu-id="f0539-114">Description</span><span class="sxs-lookup"><span data-stu-id="f0539-114">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="f0539-115">DateHeure</span><span class="sxs-lookup"><span data-stu-id="f0539-115">datetime</span></span> | <span data-ttu-id="f0539-116">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="f0539-116">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="f0539-117">string</span><span class="sxs-lookup"><span data-stu-id="f0539-117">string</span></span> | <span data-ttu-id="f0539-118">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="f0539-118">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="f0539-119">string</span><span class="sxs-lookup"><span data-stu-id="f0539-119">string</span></span> | <span data-ttu-id="f0539-120">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="f0539-120">Fully qualified domain name (FQDN) of the device</span></span> |
| `ReportId` | <span data-ttu-id="f0539-121">long</span><span class="sxs-lookup"><span data-stu-id="f0539-121">long</span></span> | <span data-ttu-id="f0539-122">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="f0539-122">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="f0539-123">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les `DeviceName` colonnes et les `Timestamp` événements</span><span class="sxs-lookup"><span data-stu-id="f0539-123">To identify unique events, this column must be used in conjunction with the `DeviceName` and `Timestamp` columns</span></span> |
| `NetworkAdapterName` | <span data-ttu-id="f0539-124">string</span><span class="sxs-lookup"><span data-stu-id="f0539-124">string</span></span> | <span data-ttu-id="f0539-125">Nom de la carte réseau</span><span class="sxs-lookup"><span data-stu-id="f0539-125">Name of the network adapter</span></span> |
| `MacAddress` | <span data-ttu-id="f0539-126">string</span><span class="sxs-lookup"><span data-stu-id="f0539-126">string</span></span> | <span data-ttu-id="f0539-127">Adresse MAC de la carte réseau</span><span class="sxs-lookup"><span data-stu-id="f0539-127">MAC address of the network adapter</span></span> |
| `NetworkAdapterType` | <span data-ttu-id="f0539-128">string</span><span class="sxs-lookup"><span data-stu-id="f0539-128">string</span></span> | <span data-ttu-id="f0539-129">Type de carte réseau.</span><span class="sxs-lookup"><span data-stu-id="f0539-129">Network adapter type.</span></span> <span data-ttu-id="f0539-130">Pour les valeurs possibles, reportez-vous [à cette éumération](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype?view=netframework-4.7.2&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="f0539-130">For the possible values, refer to [this enumeration](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.networkinterfacetype?view=netframework-4.7.2&preserve-view=true)</span></span> |
| `NetworkAdapterStatus` | <span data-ttu-id="f0539-131">string</span><span class="sxs-lookup"><span data-stu-id="f0539-131">string</span></span> | <span data-ttu-id="f0539-132">État opérationnel de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="f0539-132">Operational status of the network adapter.</span></span> <span data-ttu-id="f0539-133">Pour les valeurs possibles, reportez-vous [à cette éumération](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.operationalstatus?view=netframework-4.7.2&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="f0539-133">For the possible values, refer to [this enumeration](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.operationalstatus?view=netframework-4.7.2&preserve-view=true)</span></span> |
| `TunnelType` | <span data-ttu-id="f0539-134">string</span><span class="sxs-lookup"><span data-stu-id="f0539-134">string</span></span> | <span data-ttu-id="f0539-135">Protocole tunneling, si l’interface est utilisée à cet effet, par exemple 6to4, Teredo, ISATAP, PPTP, SSTP et SSH</span><span class="sxs-lookup"><span data-stu-id="f0539-135">Tunneling protocol, if the interface is used for this purpose, for example 6to4, Teredo, ISATAP, PPTP, SSTP, and SSH</span></span> |
| `ConnectedNetworks` | <span data-ttu-id="f0539-136">string</span><span class="sxs-lookup"><span data-stu-id="f0539-136">string</span></span> | <span data-ttu-id="f0539-137">Réseaux connectés à l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="f0539-137">Networks that the adapter is connected to.</span></span> <span data-ttu-id="f0539-138">Chaque tableau JSON contient le nom du réseau, la catégorie (public, privé ou domaine), une description et un indicateur indiquant s’il est connecté publiquement à Internet</span><span class="sxs-lookup"><span data-stu-id="f0539-138">Each JSON array contains the network name, category (public, private or domain), a description, and a flag indicating if it's connected publicly to the internet</span></span> |
| `DnsAddresses` | <span data-ttu-id="f0539-139">string</span><span class="sxs-lookup"><span data-stu-id="f0539-139">string</span></span> | <span data-ttu-id="f0539-140">Adresses de serveur DNS au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="f0539-140">DNS server addresses in JSON array format</span></span> |
| `IPv4Dhcp` | <span data-ttu-id="f0539-141">string</span><span class="sxs-lookup"><span data-stu-id="f0539-141">string</span></span> | <span data-ttu-id="f0539-142">Adresse IPv4 du serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="f0539-142">IPv4 address of DHCP server</span></span> |
| `IPv6Dhcp` | <span data-ttu-id="f0539-143">string</span><span class="sxs-lookup"><span data-stu-id="f0539-143">string</span></span> | <span data-ttu-id="f0539-144">Adresse IPv6 du serveur DHCP</span><span class="sxs-lookup"><span data-stu-id="f0539-144">IPv6 address of DHCP server</span></span> |
| `DefaultGateways` | <span data-ttu-id="f0539-145">string</span><span class="sxs-lookup"><span data-stu-id="f0539-145">string</span></span> | <span data-ttu-id="f0539-146">Adresses de passerelle par défaut au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="f0539-146">Default gateway addresses in JSON array format</span></span> |
| `IPAddresses` | <span data-ttu-id="f0539-147">string</span><span class="sxs-lookup"><span data-stu-id="f0539-147">string</span></span> | <span data-ttu-id="f0539-148">Tableau JSON contenant toutes les adresses IP affectées à la carte, ainsi que leur préfixe de sous-réseau et espace d’adressace IP respectifs, tels que public, privé ou liaison locale</span><span class="sxs-lookup"><span data-stu-id="f0539-148">JSON array containing all the IP addresses assigned to the adapter, along with their respective subnet prefix and IP address space, such as public, private, or link-local</span></span> |

## <a name="related-topics"></a><span data-ttu-id="f0539-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0539-149">Related topics</span></span>
- [<span data-ttu-id="f0539-150">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="f0539-150">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="f0539-151">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="f0539-151">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="f0539-152">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="f0539-152">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
