---
title: Table DeviceInfo dans le schéma de recherche avancée
description: En savoir plus sur le système d’exploitation, le nom de l’ordinateur et d’autres informations sur l’appareil dans la table DeviceInfo du schéma de recherche avancée
keywords: recherche avancée, recherche de cybermenace, recherche, requête, télémétrie, référence de schéma, kusto, table, colonne, type de données, description, deviceinfo, appareil, système d’exploitation, plateforme, utilisateurs, DeviceInfo
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: e6a11af94a5d2b2099d14b660cf65c846532ebd1
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500832"
---
# <a name="deviceinfo"></a><span data-ttu-id="ad884-104">DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="ad884-104">DeviceInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ad884-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ad884-105">**Applies to:**</span></span>
- [<span data-ttu-id="ad884-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ad884-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)


><span data-ttu-id="ad884-107">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ad884-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="ad884-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ad884-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

<span data-ttu-id="ad884-109">Le tableau du schéma de recherche avancée contient des informations sur les appareils de l’organisation, notamment leur version du système d’exploitation, les utilisateurs `DeviceInfo` actifs et le nom de l’ordinateur. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="ad884-109">The `DeviceInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about devices in the organization, including their OS version, active users, and computer name.</span></span> <span data-ttu-id="ad884-110">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="ad884-110">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="ad884-111">Pour plus d’informations sur les autres tableaux du schéma de chasse avancé, voir [la référence du schéma de chasse avancé.](advanced-hunting-schema-reference.md)</span><span class="sxs-lookup"><span data-stu-id="ad884-111">For information on other tables in the advanced hunting schema, see [the advanced hunting schema reference](advanced-hunting-schema-reference.md).</span></span>

| <span data-ttu-id="ad884-112">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ad884-112">Column name</span></span> | <span data-ttu-id="ad884-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="ad884-113">Data type</span></span> | <span data-ttu-id="ad884-114">Description</span><span class="sxs-lookup"><span data-stu-id="ad884-114">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="ad884-115">DateHeure</span><span class="sxs-lookup"><span data-stu-id="ad884-115">datetime</span></span> | <span data-ttu-id="ad884-116">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="ad884-116">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="ad884-117">string</span><span class="sxs-lookup"><span data-stu-id="ad884-117">string</span></span> | <span data-ttu-id="ad884-118">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="ad884-118">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="ad884-119">string</span><span class="sxs-lookup"><span data-stu-id="ad884-119">string</span></span> | <span data-ttu-id="ad884-120">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="ad884-120">Fully qualified domain name (FQDN) of the device</span></span> |
| `ClientVersion` | <span data-ttu-id="ad884-121">string</span><span class="sxs-lookup"><span data-stu-id="ad884-121">string</span></span> | <span data-ttu-id="ad884-122">Version de l’agent de point de terminaison ou du capteur en cours d’exécution sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="ad884-122">Version of the endpoint agent or sensor running on the device</span></span> |
| `PublicIP` | <span data-ttu-id="ad884-123">string</span><span class="sxs-lookup"><span data-stu-id="ad884-123">string</span></span> | <span data-ttu-id="ad884-124">Adresse IP publique utilisée par l’appareil intégré pour se connecter au service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="ad884-124">Public IP address used by the onboarded device to connect to the Defender for Endpoint service.</span></span> <span data-ttu-id="ad884-125">Il peut s’agit de l’adresse IP de l’appareil lui-même, d’un périphérique NAT ou d’un proxy.</span><span class="sxs-lookup"><span data-stu-id="ad884-125">This could be the IP address of the device itself, a NAT device, or a proxy</span></span> |
| `OSArchitecture` | <span data-ttu-id="ad884-126">string</span><span class="sxs-lookup"><span data-stu-id="ad884-126">string</span></span> | <span data-ttu-id="ad884-127">Architecture du système d’exploitation en cours d’exécution sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="ad884-127">Architecture of the operating system running on the device</span></span> |
| `OSPlatform` | <span data-ttu-id="ad884-128">string</span><span class="sxs-lookup"><span data-stu-id="ad884-128">string</span></span> | <span data-ttu-id="ad884-129">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ad884-129">Platform of the operating system running on the device.</span></span> <span data-ttu-id="ad884-130">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein de la même famille, tels que Windows 10 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad884-130">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7</span></span> |
| `OSBuild` | <span data-ttu-id="ad884-131">string</span><span class="sxs-lookup"><span data-stu-id="ad884-131">string</span></span> | <span data-ttu-id="ad884-132">Version de build du système d’exploitation en cours d’exécution sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="ad884-132">Build version of the operating system running on the device</span></span> |
| `IsAzureADJoined` | <span data-ttu-id="ad884-133">booléen</span><span class="sxs-lookup"><span data-stu-id="ad884-133">boolean</span></span> | <span data-ttu-id="ad884-134">Indicateur booléen pour savoir si l’appareil est joint à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ad884-134">Boolean indicator of whether device is joined to the Azure Active Directory</span></span> |
| `LoggedOnUsers` | <span data-ttu-id="ad884-135">string</span><span class="sxs-lookup"><span data-stu-id="ad884-135">string</span></span> | <span data-ttu-id="ad884-136">Liste de tous les utilisateurs connectés à l’appareil au moment de l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="ad884-136">List of all users that are logged on the device at the time of the event in JSON array format</span></span> |
| `RegistryDeviceTag` | <span data-ttu-id="ad884-137">string</span><span class="sxs-lookup"><span data-stu-id="ad884-137">string</span></span> | <span data-ttu-id="ad884-138">Balise d’appareil ajoutée via le Registre</span><span class="sxs-lookup"><span data-stu-id="ad884-138">Device tag added through the registry</span></span> |
| `ReportId` | <span data-ttu-id="ad884-139">long</span><span class="sxs-lookup"><span data-stu-id="ad884-139">long</span></span> | <span data-ttu-id="ad884-140">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="ad884-140">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="ad884-141">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp</span><span class="sxs-lookup"><span data-stu-id="ad884-141">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
| `OSVersion` | <span data-ttu-id="ad884-142">string</span><span class="sxs-lookup"><span data-stu-id="ad884-142">string</span></span> | <span data-ttu-id="ad884-143">Version du système d’exploitation en cours d’exécution sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="ad884-143">Version of the operating system running on the device</span></span> |
| `MachineGroup` | <span data-ttu-id="ad884-144">string</span><span class="sxs-lookup"><span data-stu-id="ad884-144">string</span></span> | <span data-ttu-id="ad884-145">Groupe d’ordinateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ad884-145">Machine group of the machine.</span></span> <span data-ttu-id="ad884-146">Ce groupe est utilisé par le contrôle d’accès basé sur un rôle pour déterminer l’accès à l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ad884-146">This group is used by role-based access control to determine access to the machine</span></span> |

## <a name="related-topics"></a><span data-ttu-id="ad884-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad884-147">Related topics</span></span>
- [<span data-ttu-id="ad884-148">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="ad884-148">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="ad884-149">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="ad884-149">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="ad884-150">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="ad884-150">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
