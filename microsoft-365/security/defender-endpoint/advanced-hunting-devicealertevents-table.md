---
title: Table DeviceAlertEvents dans le schéma de recherche avancé
description: En savoir plus sur les événements de génération d’alertes dans la table DeviceAlertEvents du schéma de recherche avancée
keywords: advanced hunting, threat hunting, cyber threat hunting, mdatp, microsoft defender atp, wdatp search, query, telemetry, schema reference, kusto, table, column, data type, description, DeviceAlertEvents, alert, severity, category
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
ms.date: 01/22/2020
ms.technology: mde
ms.openlocfilehash: 66ecdc8fbcde04d78f2deede5f4e296a7f051ef0
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51499160"
---
# <a name="devicealertevents"></a><span data-ttu-id="50ecb-104">DeviceAlertEvents</span><span class="sxs-lookup"><span data-stu-id="50ecb-104">DeviceAlertEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="50ecb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="50ecb-105">**Applies to:**</span></span>
- [<span data-ttu-id="50ecb-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="50ecb-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)



><span data-ttu-id="50ecb-107">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="50ecb-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="50ecb-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="50ecb-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

<span data-ttu-id="50ecb-109">Le tableau du schéma de recherche avancée contient des informations sur les alertes dans `DeviceAlertEvents` le Centre de sécurité Microsoft Defender. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="50ecb-109">The `DeviceAlertEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about alerts in Microsoft Defender Security Center.</span></span> <span data-ttu-id="50ecb-110">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="50ecb-110">Use this reference to construct queries that return information from the table.</span></span>

<span data-ttu-id="50ecb-111">Pour plus d’informations sur les autres tableaux du schéma de chasse avancé, voir [la référence du schéma de chasse avancé.](advanced-hunting-schema-reference.md)</span><span class="sxs-lookup"><span data-stu-id="50ecb-111">For information on other tables in the advanced hunting schema, see [the advanced hunting schema reference](advanced-hunting-schema-reference.md).</span></span>

| <span data-ttu-id="50ecb-112">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="50ecb-112">Column name</span></span> | <span data-ttu-id="50ecb-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="50ecb-113">Data type</span></span> | <span data-ttu-id="50ecb-114">Description</span><span class="sxs-lookup"><span data-stu-id="50ecb-114">Description</span></span> |
|-------------|-----------|-------------|
| `AlertId` | <span data-ttu-id="50ecb-115">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-115">string</span></span> | <span data-ttu-id="50ecb-116">Identificateur unique de l’alerte</span><span class="sxs-lookup"><span data-stu-id="50ecb-116">Unique identifier for the alert</span></span> |
| `Timestamp` | <span data-ttu-id="50ecb-117">DateHeure</span><span class="sxs-lookup"><span data-stu-id="50ecb-117">datetime</span></span> | <span data-ttu-id="50ecb-118">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="50ecb-118">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="50ecb-119">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-119">string</span></span> | <span data-ttu-id="50ecb-120">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="50ecb-120">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="50ecb-121">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-121">string</span></span> | <span data-ttu-id="50ecb-122">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="50ecb-122">Fully qualified domain name (FQDN) of the device</span></span> |
| `Severity` | <span data-ttu-id="50ecb-123">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-123">string</span></span> | <span data-ttu-id="50ecb-124">Indique l’impact potentiel (élevé, moyen ou faible) de l’indicateur de menace ou de la violation identifié(e) par l’alerte</span><span class="sxs-lookup"><span data-stu-id="50ecb-124">Indicates the potential impact (high, medium, or low) of the threat indicator or breach activity identified by the alert</span></span> |
| `Category` | <span data-ttu-id="50ecb-125">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-125">string</span></span> | <span data-ttu-id="50ecb-126">Type d’indicateur de menace ou d’activité de violation identifié par l’alerte</span><span class="sxs-lookup"><span data-stu-id="50ecb-126">Type of threat indicator or breach activity identified by the alert</span></span> |
| `Title` | <span data-ttu-id="50ecb-127">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-127">string</span></span> | <span data-ttu-id="50ecb-128">Titre de l'alerte</span><span class="sxs-lookup"><span data-stu-id="50ecb-128">Title of the alert</span></span> |
| `FileName` | <span data-ttu-id="50ecb-129">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-129">string</span></span> | <span data-ttu-id="50ecb-130">Nom du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="50ecb-130">Name of the file that the recorded action was applied to</span></span> |
| `SHA1` | <span data-ttu-id="50ecb-131">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-131">string</span></span> | <span data-ttu-id="50ecb-132">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="50ecb-132">SHA-1 of the file that the recorded action was applied to</span></span> |
| `RemoteUrl` | <span data-ttu-id="50ecb-133">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-133">string</span></span> | <span data-ttu-id="50ecb-134">URL ou nom de domaine complet (FQDN) à laquelle/auquel la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="50ecb-134">URL or fully qualified domain name (FQDN) that was being connected to</span></span> |
| `RemoteIP` | <span data-ttu-id="50ecb-135">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-135">string</span></span> | <span data-ttu-id="50ecb-136">Adresse IP à laquelle la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="50ecb-136">IP address that was being connected to</span></span> |
| `AttackTechniques` | <span data-ttu-id="50ecb-137">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-137">string</span></span> | <span data-ttu-id="50ecb-138">MITRE ATT&techniques CK associées à l’activité ayant déclenché l’alerte</span><span class="sxs-lookup"><span data-stu-id="50ecb-138">MITRE ATT&CK techniques associated with the activity that triggered the alert</span></span> |
| `ReportId` | <span data-ttu-id="50ecb-139">long</span><span class="sxs-lookup"><span data-stu-id="50ecb-139">long</span></span> | <span data-ttu-id="50ecb-140">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="50ecb-140">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="50ecb-141">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les `DeviceName` colonnes et les `Timestamp` événements</span><span class="sxs-lookup"><span data-stu-id="50ecb-141">To identify unique events, this column must be used in conjunction with the `DeviceName` and `Timestamp` columns</span></span> |
| `Table` | <span data-ttu-id="50ecb-142">string</span><span class="sxs-lookup"><span data-stu-id="50ecb-142">string</span></span> | <span data-ttu-id="50ecb-143">Table qui contient les détails de l’événement</span><span class="sxs-lookup"><span data-stu-id="50ecb-143">Table that contains the details of the event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="50ecb-144">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="50ecb-144">Related topics</span></span>
- [<span data-ttu-id="50ecb-145">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="50ecb-145">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="50ecb-146">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="50ecb-146">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="50ecb-147">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="50ecb-147">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
