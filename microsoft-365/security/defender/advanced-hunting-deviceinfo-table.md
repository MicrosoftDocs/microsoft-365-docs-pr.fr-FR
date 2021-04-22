---
title: Table DeviceInfo dans le schéma de recherche avancée
description: En savoir plus sur le système d'exploitation, le nom de l'ordinateur et d'autres informations sur l'ordinateur dans la table DeviceInfo du schéma de recherche avancée
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, machineinfo, DeviceInfo, device, machine, OS, platform, users
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
ms.openlocfilehash: e3686099606ec1cdab756bd4991cf61289299b43
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51934884"
---
# <a name="deviceinfo"></a><span data-ttu-id="bf560-104">DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="bf560-104">DeviceInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="bf560-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bf560-105">**Applies to:**</span></span>
- <span data-ttu-id="bf560-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bf560-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="bf560-107">Le tableau du schéma de recherche avancée contient des informations sur les appareils de l'organisation, notamment la version du système d'exploitation, les utilisateurs `DeviceInfo` actifs et le nom de l'ordinateur. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="bf560-107">The `DeviceInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about devices in the organization, including OS version, active users, and computer name.</span></span> <span data-ttu-id="bf560-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="bf560-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="bf560-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bf560-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="bf560-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="bf560-110">Column name</span></span> | <span data-ttu-id="bf560-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="bf560-111">Data type</span></span> | <span data-ttu-id="bf560-112">Description</span><span class="sxs-lookup"><span data-stu-id="bf560-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="bf560-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="bf560-113">datetime</span></span> | <span data-ttu-id="bf560-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="bf560-114">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="bf560-115">string</span><span class="sxs-lookup"><span data-stu-id="bf560-115">string</span></span> | <span data-ttu-id="bf560-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="bf560-116">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="bf560-117">string</span><span class="sxs-lookup"><span data-stu-id="bf560-117">string</span></span> | <span data-ttu-id="bf560-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="bf560-118">Fully qualified domain name (FQDN) of the machine</span></span> |
| `ClientVersion` | <span data-ttu-id="bf560-119">string</span><span class="sxs-lookup"><span data-stu-id="bf560-119">string</span></span> | <span data-ttu-id="bf560-120">Version de l'agent de point de terminaison ou du capteur en cours d'exécution sur l'ordinateur</span><span class="sxs-lookup"><span data-stu-id="bf560-120">Version of the endpoint agent or sensor running on the machine</span></span> |
| `PublicIP` | <span data-ttu-id="bf560-121">string</span><span class="sxs-lookup"><span data-stu-id="bf560-121">string</span></span> | <span data-ttu-id="bf560-122">Adresse IP publique utilisée par l'ordinateur intégré pour se connecter au service Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="bf560-122">Public IP address used by the onboarded machine to connect to the Microsoft  Defender for Endpoint service.</span></span> <span data-ttu-id="bf560-123">Il peut s'agit de l'adresse IP de l'ordinateur lui-même, d'un périphérique NAT ou d'un proxy.</span><span class="sxs-lookup"><span data-stu-id="bf560-123">This could be the IP address of the machine itself, a NAT device, or a proxy</span></span> |
| `OSArchitecture` | <span data-ttu-id="bf560-124">string</span><span class="sxs-lookup"><span data-stu-id="bf560-124">string</span></span> | <span data-ttu-id="bf560-125">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="bf560-125">Architecture of the operating system running on the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="bf560-126">string</span><span class="sxs-lookup"><span data-stu-id="bf560-126">string</span></span> | <span data-ttu-id="bf560-127">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="bf560-127">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="bf560-128">Cela indique des systèmes d'exploitation spécifiques, y compris des variantes au sein de la même famille, tels que Windows 10 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf560-128">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7</span></span> |
| `OSBuild` | <span data-ttu-id="bf560-129">string</span><span class="sxs-lookup"><span data-stu-id="bf560-129">string</span></span> | <span data-ttu-id="bf560-130">Version de build du système d'exploitation en cours d'exécution sur l'ordinateur</span><span class="sxs-lookup"><span data-stu-id="bf560-130">Build version of the operating system running on the machine</span></span> |
| `IsAzureADJoined` | <span data-ttu-id="bf560-131">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="bf560-131">boolean</span></span> | <span data-ttu-id="bf560-132">Indicateur booléen pour savoir si l'ordinateur est joint à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bf560-132">Boolean indicator of whether machine is joined to the Azure Active Directory</span></span> |
| `AadObjectId` | <span data-ttu-id="bf560-133">string</span><span class="sxs-lookup"><span data-stu-id="bf560-133">string</span></span> | <span data-ttu-id="bf560-134">Identificateur unique de l'appareil dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="bf560-134">Unique identifier for the device in Azure AD</span></span> |
| `LoggedOnUsers` | <span data-ttu-id="bf560-135">string</span><span class="sxs-lookup"><span data-stu-id="bf560-135">string</span></span> | <span data-ttu-id="bf560-136">Liste de tous les utilisateurs connectés à l'ordinateur au moment de l'événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="bf560-136">List of all users that are logged on the machine at the time of the event in JSON array format</span></span> |
| `RegistryDeviceTag` | <span data-ttu-id="bf560-137">string</span><span class="sxs-lookup"><span data-stu-id="bf560-137">string</span></span> | <span data-ttu-id="bf560-138">Balise d'ordinateur ajoutée via le Registre</span><span class="sxs-lookup"><span data-stu-id="bf560-138">Machine tag added through the registry</span></span> |
| `OSVersion` | <span data-ttu-id="bf560-139">string</span><span class="sxs-lookup"><span data-stu-id="bf560-139">string</span></span> | <span data-ttu-id="bf560-140">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="bf560-140">Version of the operating system running on the machine</span></span> |
| `MachineGroup` | <span data-ttu-id="bf560-141">string</span><span class="sxs-lookup"><span data-stu-id="bf560-141">string</span></span> | <span data-ttu-id="bf560-142">Groupe d'ordinateurs de l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bf560-142">Machine group of the machine.</span></span> <span data-ttu-id="bf560-143">Ce groupe est utilisé par le contrôle d'accès basé sur un rôle pour déterminer l'accès à l'ordinateur</span><span class="sxs-lookup"><span data-stu-id="bf560-143">This group is used by role-based access control to determine access to the machine</span></span> |
| `ReportId` | <span data-ttu-id="bf560-144">long</span><span class="sxs-lookup"><span data-stu-id="bf560-144">long</span></span> | <span data-ttu-id="bf560-145">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="bf560-145">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="bf560-146">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp</span><span class="sxs-lookup"><span data-stu-id="bf560-146">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
|`AdditionalFields` | <span data-ttu-id="bf560-147">string</span><span class="sxs-lookup"><span data-stu-id="bf560-147">string</span></span> | <span data-ttu-id="bf560-148">Informations supplémentaires sur l'événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="bf560-148">Additional information about the event in JSON array format</span></span> |

<span data-ttu-id="bf560-149">Le tableau fournit des informations sur l'appareil en fonction des pulsations, qui sont des rapports ou signaux périodiques `DeviceInfo` d'un appareil.</span><span class="sxs-lookup"><span data-stu-id="bf560-149">The `DeviceInfo` table provides device information based on heartbeats, which are periodic reports or signals from a device.</span></span> <span data-ttu-id="bf560-150">Toutes les quinze minutes, l'appareil envoie une pulsation partielle qui contient des attributs qui changent fréquemment comme `LoggedOnUsers` .</span><span class="sxs-lookup"><span data-stu-id="bf560-150">Every fifteen minutes, the device sends a partial heartbeat that contains frequently changing attributes like `LoggedOnUsers`.</span></span> <span data-ttu-id="bf560-151">Une fois par jour, une pulsation complète contenant les attributs de l'appareil est envoyée.</span><span class="sxs-lookup"><span data-stu-id="bf560-151">Once a day, a full heartbeat containing the device's attributes is sent.</span></span>

<span data-ttu-id="bf560-152">Vous pouvez utiliser l’exemple de requête suivant pour obtenir l’état le plus récent d’un appareil :</span><span class="sxs-lookup"><span data-stu-id="bf560-152">You can use the following sample query to get the latest state of a device:</span></span>

```kusto
// Get latest information on user/device
DeviceInfo
| where DeviceName == "example" and isnotempty(OSPlatform)
| summarize arg_max(Timestamp, *) by DeviceId 
```

## <a name="related-topics"></a><span data-ttu-id="bf560-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf560-153">Related topics</span></span>
- [<span data-ttu-id="bf560-154">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="bf560-154">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="bf560-155">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="bf560-155">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="bf560-156">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="bf560-156">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="bf560-157">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="bf560-157">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="bf560-158">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="bf560-158">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="bf560-159">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="bf560-159">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
