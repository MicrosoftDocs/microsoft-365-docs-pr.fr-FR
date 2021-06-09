---
title: Table DeviceInfo dans le schéma de recherche avancée
description: En savoir plus sur le système d’exploitation, le nom de l’ordinateur et d’autres informations sur l’ordinateur dans la table DeviceInfo du schéma de recherche avancée
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
ms.openlocfilehash: 99a07b1517058b0e5ab241aaae9c6899e2994432
ms.sourcegitcommit: 82a4d74020cd93ba444006317cfecc178c6d41dc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52689108"
---
# <a name="deviceinfo"></a><span data-ttu-id="ace3a-104">DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="ace3a-104">DeviceInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="ace3a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ace3a-105">**Applies to:**</span></span>
- <span data-ttu-id="ace3a-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ace3a-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="ace3a-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ace3a-107">Microsoft Defender for Endpoint</span></span>



<span data-ttu-id="ace3a-108">Le tableau du schéma de recherche avancée contient des informations sur les appareils de l’organisation, notamment la version du système d’exploitation, les utilisateurs `DeviceInfo` actifs et le nom de l’ordinateur. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="ace3a-108">The `DeviceInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about devices in the organization, including OS version, active users, and computer name.</span></span> <span data-ttu-id="ace3a-109">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="ace3a-109">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="ace3a-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ace3a-110">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="ace3a-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ace3a-111">Column name</span></span> | <span data-ttu-id="ace3a-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="ace3a-112">Data type</span></span> | <span data-ttu-id="ace3a-113">Description</span><span class="sxs-lookup"><span data-stu-id="ace3a-113">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="ace3a-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="ace3a-114">datetime</span></span> | <span data-ttu-id="ace3a-115">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="ace3a-115">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="ace3a-116">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-116">string</span></span> | <span data-ttu-id="ace3a-117">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="ace3a-117">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="ace3a-118">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-118">string</span></span> | <span data-ttu-id="ace3a-119">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="ace3a-119">Fully qualified domain name (FQDN) of the machine</span></span> |
| `ClientVersion` | <span data-ttu-id="ace3a-120">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-120">string</span></span> | <span data-ttu-id="ace3a-121">Version de l’agent de point de terminaison ou du capteur en cours d’exécution sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ace3a-121">Version of the endpoint agent or sensor running on the machine</span></span> |
| `PublicIP` | <span data-ttu-id="ace3a-122">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-122">string</span></span> | <span data-ttu-id="ace3a-123">Adresse IP publique utilisée par l’ordinateur intégré pour se connecter au service Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="ace3a-123">Public IP address used by the onboarded machine to connect to the Microsoft  Defender for Endpoint service.</span></span> <span data-ttu-id="ace3a-124">Il peut s’agit de l’adresse IP de l’ordinateur lui-même, d’un périphérique NAT ou d’un proxy.</span><span class="sxs-lookup"><span data-stu-id="ace3a-124">This could be the IP address of the machine itself, a NAT device, or a proxy</span></span> |
| `OSArchitecture` | <span data-ttu-id="ace3a-125">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-125">string</span></span> | <span data-ttu-id="ace3a-126">Architecture du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="ace3a-126">Architecture of the operating system running on the machine</span></span> |
| `OSPlatform` | <span data-ttu-id="ace3a-127">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-127">string</span></span> | <span data-ttu-id="ace3a-128">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="ace3a-128">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="ace3a-129">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein de la même famille, telles que Windows 10 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="ace3a-129">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7</span></span> |
| `OSBuild` | <span data-ttu-id="ace3a-130">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-130">string</span></span> | <span data-ttu-id="ace3a-131">Version de build du système d’exploitation en cours d’exécution sur l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ace3a-131">Build version of the operating system running on the machine</span></span> |
| `IsAzureADJoined` | <span data-ttu-id="ace3a-132">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="ace3a-132">boolean</span></span> | <span data-ttu-id="ace3a-133">Indicateur booléen pour savoir si l’ordinateur est joint au Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ace3a-133">Boolean indicator of whether machine is joined to the Azure Active Directory</span></span> |
| `AadObjectId` | <span data-ttu-id="ace3a-134">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-134">string</span></span> | <span data-ttu-id="ace3a-135">Identificateur unique de l’appareil dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="ace3a-135">Unique identifier for the device in Azure AD</span></span> |
| `LoggedOnUsers` | <span data-ttu-id="ace3a-136">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-136">string</span></span> | <span data-ttu-id="ace3a-137">Liste de tous les utilisateurs connectés à l’ordinateur au moment de l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="ace3a-137">List of all users that are logged on the machine at the time of the event in JSON array format</span></span> |
| `RegistryDeviceTag` | <span data-ttu-id="ace3a-138">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-138">string</span></span> | <span data-ttu-id="ace3a-139">Balise d’ordinateur ajoutée via le Registre</span><span class="sxs-lookup"><span data-stu-id="ace3a-139">Machine tag added through the registry</span></span> |
| `OSVersion` | <span data-ttu-id="ace3a-140">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-140">string</span></span> | <span data-ttu-id="ace3a-141">Version du système d’exploitation s’exécutant sur la machine</span><span class="sxs-lookup"><span data-stu-id="ace3a-141">Version of the operating system running on the machine</span></span> |
| `MachineGroup` | <span data-ttu-id="ace3a-142">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-142">string</span></span> | <span data-ttu-id="ace3a-143">Groupe d’ordinateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ace3a-143">Machine group of the machine.</span></span> <span data-ttu-id="ace3a-144">Ce groupe est utilisé par le contrôle d’accès basé sur un rôle pour déterminer l’accès à l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ace3a-144">This group is used by role-based access control to determine access to the machine</span></span> |
| `ReportId` | <span data-ttu-id="ace3a-145">long</span><span class="sxs-lookup"><span data-stu-id="ace3a-145">long</span></span> | <span data-ttu-id="ace3a-146">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="ace3a-146">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="ace3a-147">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp</span><span class="sxs-lookup"><span data-stu-id="ace3a-147">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
| `OnboardingStatus` | <span data-ttu-id="ace3a-148">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-148">string</span></span> | <span data-ttu-id="ace3a-149">Indique si l’appareil est actuellement intégré à Microsoft Defender pour le point de terminaison ou si l’appareil n’est pas pris en charge</span><span class="sxs-lookup"><span data-stu-id="ace3a-149">Indicates whether the device is currently onboarded or not to Microsoft Defender For Endpoint or if the device is not supported</span></span> |
|`AdditionalFields` | <span data-ttu-id="ace3a-150">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-150">string</span></span> | <span data-ttu-id="ace3a-151">Informations supplémentaires sur l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="ace3a-151">Additional information about the event in JSON array format</span></span> |
|`DeviceCategory` | <span data-ttu-id="ace3a-152">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-152">string</span></span> | <span data-ttu-id="ace3a-153">Classification plus large qui groupe certains types d’appareils sous les catégories suivantes : Point de terminaison, Périphérique réseau, IoT, Inconnu</span><span class="sxs-lookup"><span data-stu-id="ace3a-153">Broader classification that groups certain device types under the following categories: Endpoint, Network device, IoT, Unknown</span></span> |
|`DeviceType` | <span data-ttu-id="ace3a-154">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-154">string</span></span> | <span data-ttu-id="ace3a-155">Type d’appareil en fonction de l’objectif et des fonctionnalités, tels que l’appareil réseau, la station de travail, le serveur, l’appareil mobile, la console de jeu ou l’imprimante</span><span class="sxs-lookup"><span data-stu-id="ace3a-155">Type of device based on purpose and functionality, such as network device, workstation, server, mobile, gaming console, or printer</span></span> |
|`DeviceSubType` | <span data-ttu-id="ace3a-156">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-156">string</span></span> | <span data-ttu-id="ace3a-157">Modificateur supplémentaire pour certains types d’appareils, par exemple, un appareil mobile peut être une tablette ou un smartphone</span><span class="sxs-lookup"><span data-stu-id="ace3a-157">Additional modifier for certain types of devices, for example, a mobile device can be a tablet or a smartphone</span></span> |
|`Model` | <span data-ttu-id="ace3a-158">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-158">string</span></span> | <span data-ttu-id="ace3a-159">Nom du modèle ou numéro du produit du fournisseur ou du fabricant</span><span class="sxs-lookup"><span data-stu-id="ace3a-159">Model name or number of the product from the vendor or manufacturer</span></span> |
|`Vendor` | <span data-ttu-id="ace3a-160">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-160">string</span></span> | <span data-ttu-id="ace3a-161">Nom du fournisseur ou du fabricant du produit</span><span class="sxs-lookup"><span data-stu-id="ace3a-161">Name of the product vendor or manufacturer</span></span> |
|`OSDistribution` | <span data-ttu-id="ace3a-162">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-162">string</span></span> | <span data-ttu-id="ace3a-163">Distribution de la plateforme du système d’exploitation, telle que Ubuntu ou RedHat pour les plateformes Linux</span><span class="sxs-lookup"><span data-stu-id="ace3a-163">Distribution of the OS platform, such as Ubuntu or RedHat for Linux platforms</span></span> |
|`OSVersionInfo` | <span data-ttu-id="ace3a-164">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-164">string</span></span> | <span data-ttu-id="ace3a-165">Informations supplémentaires sur la version du système d’exploitation, telles que le nom populaire, le nom de code ou le numéro de version</span><span class="sxs-lookup"><span data-stu-id="ace3a-165">Additional information about the OS version, such as the popular name, code name, or version number</span></span> |
|`MergedDeviceIds` | <span data-ttu-id="ace3a-166">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-166">string</span></span> | <span data-ttu-id="ace3a-167">ID d’appareil précédents qui ont été affectés au même appareil</span><span class="sxs-lookup"><span data-stu-id="ace3a-167">Previous device IDs that have been assigned to the same device</span></span> |
|`MergedToDeviceId` | <span data-ttu-id="ace3a-168">string</span><span class="sxs-lookup"><span data-stu-id="ace3a-168">string</span></span> | <span data-ttu-id="ace3a-169">ID d’appareil le plus récent affecté à un appareil</span><span class="sxs-lookup"><span data-stu-id="ace3a-169">The most recent device ID assigned to a device</span></span> |

<span data-ttu-id="ace3a-170">Le tableau fournit des informations sur l’appareil en fonction des pulsations, qui sont des rapports ou signaux périodiques `DeviceInfo` d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="ace3a-170">The `DeviceInfo` table provides device information based on heartbeats, which are periodic reports or signals from a device.</span></span> <span data-ttu-id="ace3a-171">Toutes les quinze minutes, l’appareil envoie une pulsation partielle qui contient des attributs qui changent fréquemment comme `LoggedOnUsers` .</span><span class="sxs-lookup"><span data-stu-id="ace3a-171">Every fifteen minutes, the device sends a partial heartbeat that contains frequently changing attributes like `LoggedOnUsers`.</span></span> <span data-ttu-id="ace3a-172">Une fois par jour, une pulsation complète contenant les attributs de l’appareil est envoyée.</span><span class="sxs-lookup"><span data-stu-id="ace3a-172">Once a day, a full heartbeat containing the device's attributes is sent.</span></span>

<span data-ttu-id="ace3a-173">Vous pouvez utiliser l’exemple de requête suivant pour obtenir l’état le plus récent d’un appareil :</span><span class="sxs-lookup"><span data-stu-id="ace3a-173">You can use the following sample query to get the latest state of a device:</span></span>

```kusto
// Get latest information on user/device
DeviceInfo
| where DeviceName == "example" and isnotempty(OSPlatform)
| summarize arg_max(Timestamp, *) by DeviceId 
```

## <a name="related-topics"></a><span data-ttu-id="ace3a-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ace3a-174">Related topics</span></span>
- [<span data-ttu-id="ace3a-175">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="ace3a-175">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="ace3a-176">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="ace3a-176">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="ace3a-177">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="ace3a-177">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="ace3a-178">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="ace3a-178">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="ace3a-179">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="ace3a-179">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="ace3a-180">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="ace3a-180">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
