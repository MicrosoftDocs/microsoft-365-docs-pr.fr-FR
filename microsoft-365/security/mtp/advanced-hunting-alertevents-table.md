---
title: Table AlertEvents dans le schéma de repérage avancé
description: En savoir plus sur les événements de génération d’alertes dans la table AlertEvents du schéma de repérage avancé
keywords: repérage avancé, repérage de menace, repérage de cybermenace, recherche, requête, télémétrie, référence de schéma, kusto, table, colonne, type de données, description, alertevents, alerte, gravité, catégorie
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: ee14dcc1c2ae0a2bc6fa3c094d757441515f00de
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40807013"
---
# <a name="alertevents"></a><span data-ttu-id="5b385-104">AlertEvents</span><span class="sxs-lookup"><span data-stu-id="5b385-104">AlertEvents</span></span>

<span data-ttu-id="5b385-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5b385-105">**Applies to:**</span></span>
- <span data-ttu-id="5b385-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="5b385-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="5b385-107">La table `AlertEvents` dans le schéma de [repérage avancé](advanced-hunting-overview.md) contient des informations sur les pièces jointes des alertes Microsoft Defender - Protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="5b385-107">The `AlertEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about Microsoft Defender ATP alerts.</span></span> <span data-ttu-id="5b385-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="5b385-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="5b385-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5b385-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="5b385-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="5b385-110">Column name</span></span> | <span data-ttu-id="5b385-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="5b385-111">Data type</span></span> | <span data-ttu-id="5b385-112">Description</span><span class="sxs-lookup"><span data-stu-id="5b385-112">Description</span></span> |
|-------------|-----------|-------------|
| `AlertId` | <span data-ttu-id="5b385-113">string</span><span class="sxs-lookup"><span data-stu-id="5b385-113">string</span></span> | <span data-ttu-id="5b385-114">Identificateur unique de l’alerte</span><span class="sxs-lookup"><span data-stu-id="5b385-114">Unique identifier for the alert</span></span> |
| `Timestamp` | <span data-ttu-id="5b385-115">DateHeure</span><span class="sxs-lookup"><span data-stu-id="5b385-115">datetime</span></span> | <span data-ttu-id="5b385-116">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="5b385-116">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="5b385-117">string</span><span class="sxs-lookup"><span data-stu-id="5b385-117">string</span></span> | <span data-ttu-id="5b385-118">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="5b385-118">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="5b385-119">string</span><span class="sxs-lookup"><span data-stu-id="5b385-119">string</span></span> | <span data-ttu-id="5b385-120">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="5b385-120">Fully qualified domain name (FQDN) of the machine</span></span> |
| `Severity` | <span data-ttu-id="5b385-121">string</span><span class="sxs-lookup"><span data-stu-id="5b385-121">string</span></span> | <span data-ttu-id="5b385-122">Indique l’impact potentiel (élevé, moyen ou faible) de l’indicateur de menace ou de la violation identifié(e) par l’alerte</span><span class="sxs-lookup"><span data-stu-id="5b385-122">Indicates the potential impact (high, medium, or low) of the threat indicator or breach activity identified by the alert</span></span> |
| `Category` | <span data-ttu-id="5b385-123">string</span><span class="sxs-lookup"><span data-stu-id="5b385-123">string</span></span> | <span data-ttu-id="5b385-124">Type d’indicateur de menace ou d’activité de violation identifié par l’alerte</span><span class="sxs-lookup"><span data-stu-id="5b385-124">Type of threat indicator or breach activity identified by the alert</span></span> |
| `Title` | <span data-ttu-id="5b385-125">string</span><span class="sxs-lookup"><span data-stu-id="5b385-125">string</span></span> | <span data-ttu-id="5b385-126">Titre de l'alerte</span><span class="sxs-lookup"><span data-stu-id="5b385-126">Title of the alert</span></span> |
| `FileName` | <span data-ttu-id="5b385-127">string</span><span class="sxs-lookup"><span data-stu-id="5b385-127">string</span></span> | <span data-ttu-id="5b385-128">Nom du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="5b385-128">Name of the file that the recorded action was applied to</span></span> |
| `SHA1` | <span data-ttu-id="5b385-129">string</span><span class="sxs-lookup"><span data-stu-id="5b385-129">string</span></span> | <span data-ttu-id="5b385-130">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="5b385-130">SHA-1 of the file that the recorded action was applied to</span></span> |
| `RemoteUrl` | <span data-ttu-id="5b385-131">string</span><span class="sxs-lookup"><span data-stu-id="5b385-131">string</span></span> | <span data-ttu-id="5b385-132">URL ou nom de domaine complet (FQDN) à laquelle/auquel la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="5b385-132">URL or fully qualified domain name (FQDN) that was being connected to</span></span> |
| `RemoteIP` | <span data-ttu-id="5b385-133">string</span><span class="sxs-lookup"><span data-stu-id="5b385-133">string</span></span> | <span data-ttu-id="5b385-134">Adresse IP à laquelle la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="5b385-134">IP address that was being connected to</span></span> |
| `ReportId` | <span data-ttu-id="5b385-135">long</span><span class="sxs-lookup"><span data-stu-id="5b385-135">long</span></span> | <span data-ttu-id="5b385-136">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="5b385-136">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="5b385-137">Pour identifier les événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et timestamp</span><span class="sxs-lookup"><span data-stu-id="5b385-137">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns</span></span> |
| `Table` | <span data-ttu-id="5b385-138">string</span><span class="sxs-lookup"><span data-stu-id="5b385-138">string</span></span> | <span data-ttu-id="5b385-139">Table qui contient les détails de l’événement</span><span class="sxs-lookup"><span data-stu-id="5b385-139">Table that contains the details of the event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="5b385-140">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="5b385-140">Related topics</span></span>
- [<span data-ttu-id="5b385-141">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="5b385-141">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="5b385-142">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="5b385-142">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="5b385-143">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="5b385-143">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="5b385-144">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="5b385-144">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="5b385-145">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="5b385-145">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="5b385-146">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="5b385-146">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
