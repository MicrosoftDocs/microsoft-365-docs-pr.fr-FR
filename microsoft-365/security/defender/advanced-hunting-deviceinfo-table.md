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
ms.openlocfilehash: f97947c2c9f02720facae4f0c3c29ff702416261
ms.sourcegitcommit: 72795ec56a7c4db863dcaaff5e9f7c41c653fda8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "52023128"
---
# <a name="deviceinfo"></a><span data-ttu-id="f8647-104">DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="f8647-104">DeviceInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="f8647-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f8647-105">**Applies to:**</span></span>
- <span data-ttu-id="f8647-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f8647-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="f8647-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f8647-107">Microsoft Defender for Endpoint</span></span>



<span data-ttu-id="f8647-108">Le tableau du schéma de recherche avancée contient des informations sur les appareils de l'organisation, notamment la version du système d'exploitation, les utilisateurs `DeviceInfo` actifs et le nom de l'ordinateur. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="f8647-108">The `DeviceInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about devices in the organization, including OS version, active users, and computer name.</span></span> <span data-ttu-id="f8647-109">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="f8647-109">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="f8647-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f8647-110">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="f8647-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="f8647-111">Column name</span></span> | <span data-ttu-id="f8647-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="f8647-112">Data type</span></span> | <span data-ttu-id="f8647-113">Description</span><span class="sxs-lookup"><span data-stu-id="f8647-113">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="f8647-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="f8647-114">datetime</span></span> | <span data-ttu-id="f8647-115">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="f8647-115">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="f8647-116">string</span><span class="sxs-lookup"><span data-stu-id="f8647-116">string</span></span> | <span data-ttu-id="f8647-117">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="f8647-117">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="f8647-118">string</span><span class="sxs-lookup"><span data-stu-id="f8647-118">string</span></span> | <span data-ttu-id="f8647-119">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="f8647-119">Fully qualified domain name (FQDN) of the machine</span></span> |
| `ClientVersion` | <span data-ttu-id="f8647-120">string</span><span class="sxs-lookup"><span data-stu-id="f8647-120">string</span></span> | <span data-ttu-id="f8647-121">Version de l'agent de point de terminaison ou du capteur en cours d'exécution sur l'ordinateur</span><span class="sxs-lookup"><span data-stu-id="f8647-121">Version of the endpoint agent or sensor running on the machine</span></span> |
| `PublicIP` | <span data-ttu-id="f8647-122">string</span><span class="sxs-lookup"><span data-stu-id="f8647-122">string</span></span> | <span data-ttu-id="f8647-123">Adresse IP publique utilisée par l'ordinateur intégré pour se connecter au service Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="f8647-123">Public IP address used by the onboarded machine to connect to the Microsoft  Defender for Endpoint service.</span></span> <span data-ttu-id="f8647-124">Il peut s'agit de l'adresse IP de l'ordinateur lui-même, d'un périphérique NAT ou d'un proxy</span><span class="sxs-lookup"><span data-stu-id="f8647-124">This could be the IP address of the machine itself, a NAT device, or a proxy</span></span> |
| `OSArchitecture` | <span data-ttu-id="f8647-125">string</span><span class="sxs-lookup"><span data-stu-id="f8647-125">string</span></span> | <span data-ttu-id="f8647-126">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="f8647-126">Architecture of the operating system running on the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="f8647-127">string</span><span class="sxs-lookup"><span data-stu-id="f8647-127">string</span></span> | <span data-ttu-id="f8647-128">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="f8647-128">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="f8647-129">Cela indique des systèmes d'exploitation spécifiques, y compris des variantes au sein de la même famille, tels que Windows 10 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8647-129">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7</span></span> |
| `OSBuild` | <span data-ttu-id="f8647-130">string</span><span class="sxs-lookup"><span data-stu-id="f8647-130">string</span></span> | <span data-ttu-id="f8647-131">Version de build du système d'exploitation en cours d'exécution sur l'ordinateur</span><span class="sxs-lookup"><span data-stu-id="f8647-131">Build version of the operating system running on the machine</span></span> |
| `IsAzureADJoined` | <span data-ttu-id="f8647-132">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="f8647-132">boolean</span></span> | <span data-ttu-id="f8647-133">Indicateur booléen pour savoir si l'ordinateur est joint à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f8647-133">Boolean indicator of whether machine is joined to the Azure Active Directory</span></span> |
| `AadObjectId` | <span data-ttu-id="f8647-134">string</span><span class="sxs-lookup"><span data-stu-id="f8647-134">string</span></span> | <span data-ttu-id="f8647-135">Identificateur unique de l'appareil dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="f8647-135">Unique identifier for the device in Azure AD</span></span> |
| `LoggedOnUsers` | <span data-ttu-id="f8647-136">string</span><span class="sxs-lookup"><span data-stu-id="f8647-136">string</span></span> | <span data-ttu-id="f8647-137">Liste de tous les utilisateurs connectés à l'ordinateur au moment de l'événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="f8647-137">List of all users that are logged on the machine at the time of the event in JSON array format</span></span> |
| `RegistryDeviceTag` | <span data-ttu-id="f8647-138">string</span><span class="sxs-lookup"><span data-stu-id="f8647-138">string</span></span> | <span data-ttu-id="f8647-139">Balise d'ordinateur ajoutée via le Registre</span><span class="sxs-lookup"><span data-stu-id="f8647-139">Machine tag added through the registry</span></span> |
| `OSVersion` | <span data-ttu-id="f8647-140">string</span><span class="sxs-lookup"><span data-stu-id="f8647-140">string</span></span> | <span data-ttu-id="f8647-141">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="f8647-141">Version of the operating system running on the machine</span></span> |
| `MachineGroup` | <span data-ttu-id="f8647-142">string</span><span class="sxs-lookup"><span data-stu-id="f8647-142">string</span></span> | <span data-ttu-id="f8647-143">Groupe d'ordinateurs de l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f8647-143">Machine group of the machine.</span></span> <span data-ttu-id="f8647-144">Ce groupe est utilisé par le contrôle d'accès basé sur un rôle pour déterminer l'accès à l'ordinateur</span><span class="sxs-lookup"><span data-stu-id="f8647-144">This group is used by role-based access control to determine access to the machine</span></span> |
| `ReportId` | <span data-ttu-id="f8647-145">long</span><span class="sxs-lookup"><span data-stu-id="f8647-145">long</span></span> | <span data-ttu-id="f8647-146">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="f8647-146">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="f8647-147">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp</span><span class="sxs-lookup"><span data-stu-id="f8647-147">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
|`AdditionalFields` | <span data-ttu-id="f8647-148">string</span><span class="sxs-lookup"><span data-stu-id="f8647-148">string</span></span> | <span data-ttu-id="f8647-149">Informations supplémentaires sur l'événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="f8647-149">Additional information about the event in JSON array format</span></span> |

<span data-ttu-id="f8647-150">Le tableau fournit des informations sur l'appareil en fonction des pulsations, qui sont des rapports ou signaux périodiques `DeviceInfo` d'un appareil.</span><span class="sxs-lookup"><span data-stu-id="f8647-150">The `DeviceInfo` table provides device information based on heartbeats, which are periodic reports or signals from a device.</span></span> <span data-ttu-id="f8647-151">Toutes les quinze minutes, l'appareil envoie une pulsation partielle qui contient des attributs qui changent fréquemment comme `LoggedOnUsers` .</span><span class="sxs-lookup"><span data-stu-id="f8647-151">Every fifteen minutes, the device sends a partial heartbeat that contains frequently changing attributes like `LoggedOnUsers`.</span></span> <span data-ttu-id="f8647-152">Une fois par jour, une pulsation complète contenant les attributs de l'appareil est envoyée.</span><span class="sxs-lookup"><span data-stu-id="f8647-152">Once a day, a full heartbeat containing the device's attributes is sent.</span></span>

<span data-ttu-id="f8647-153">Vous pouvez utiliser l’exemple de requête suivant pour obtenir l’état le plus récent d’un appareil :</span><span class="sxs-lookup"><span data-stu-id="f8647-153">You can use the following sample query to get the latest state of a device:</span></span>

```kusto
// Get latest information on user/device
DeviceInfo
| where DeviceName == "example" and isnotempty(OSPlatform)
| summarize arg_max(Timestamp, *) by DeviceId 
```

## <a name="related-topics"></a><span data-ttu-id="f8647-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8647-154">Related topics</span></span>
- [<span data-ttu-id="f8647-155">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="f8647-155">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="f8647-156">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="f8647-156">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="f8647-157">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="f8647-157">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="f8647-158">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="f8647-158">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="f8647-159">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="f8647-159">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="f8647-160">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="f8647-160">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
