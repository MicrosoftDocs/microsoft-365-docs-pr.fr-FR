---
title: Table IdentityDirectoryEvents dans le schéma de recherche avancé
description: En savoir plus sur le contrôleur de domaine et les événements Active Directory dans la table IdentityDirectoryEvents du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, IdentityDirectoryEvents, domain controller, Active Directory, Azure ATP, identities
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
ms.openlocfilehash: 73018bb65c011d10234ec9c02fc61bfb93fa125a
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51501130"
---
# <a name="identitydirectoryevents"></a><span data-ttu-id="17c91-104">IdentityDirectoryEvents</span><span class="sxs-lookup"><span data-stu-id="17c91-104">IdentityDirectoryEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="17c91-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="17c91-105">**Applies to:**</span></span>
- <span data-ttu-id="17c91-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="17c91-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="17c91-107">Le tableau du schéma de recherche avancée contient des événements impliquant un contrôleur de domaine local exécutant `IdentityDirectoryEvents` Active Directory [](advanced-hunting-overview.md) (AD).</span><span class="sxs-lookup"><span data-stu-id="17c91-107">The `IdentityDirectoryEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains events involving an on-premises domain controller running Active Directory (AD).</span></span> <span data-ttu-id="17c91-108">Ce tableau capture différents événements liés à l’identité, tels que les modifications de mot de passe, l’expiration du mot de passe et les modifications de nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="17c91-108">This table captures various identity-related events, like password changes, password expiration, and user principal name (UPN) changes.</span></span> <span data-ttu-id="17c91-109">Il capture également les événements système sur le contrôleur de domaine, tels que la planification des tâches et l’activité PowerShell.</span><span class="sxs-lookup"><span data-stu-id="17c91-109">It also captures system events on the domain controller, like scheduling of tasks and PowerShell activity.</span></span> <span data-ttu-id="17c91-110">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="17c91-110">Use this reference to construct queries that return information from this table.</span></span>

>[!TIP]
> <span data-ttu-id="17c91-111">Pour plus d’informations sur les types d’événements (valeurs) pris en charge par une table, utilisez la référence de schéma intégrée disponible `ActionType` dans le centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="17c91-111">For detailed information about the events types (`ActionType` values) supported by a table, use the built-in schema reference available in the security center.</span></span>

<span data-ttu-id="17c91-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="17c91-112">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="17c91-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="17c91-113">Column name</span></span> | <span data-ttu-id="17c91-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="17c91-114">Data type</span></span> | <span data-ttu-id="17c91-115">Description</span><span class="sxs-lookup"><span data-stu-id="17c91-115">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="17c91-116">DateHeure</span><span class="sxs-lookup"><span data-stu-id="17c91-116">datetime</span></span> | <span data-ttu-id="17c91-117">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="17c91-117">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="17c91-118">string</span><span class="sxs-lookup"><span data-stu-id="17c91-118">string</span></span> | <span data-ttu-id="17c91-119">Type d’activité qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="17c91-119">Type of activity that triggered the event.</span></span> <span data-ttu-id="17c91-120">Pour plus [d’informations, voir](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) la référence du schéma dans le portail</span><span class="sxs-lookup"><span data-stu-id="17c91-120">See the [in-portal schema reference](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) for details</span></span> |
| `Application` | <span data-ttu-id="17c91-121">string</span><span class="sxs-lookup"><span data-stu-id="17c91-121">string</span></span> | <span data-ttu-id="17c91-122">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="17c91-122">Application that performed the recorded action</span></span> |
| `TargetAccountUpn` | <span data-ttu-id="17c91-123">string</span><span class="sxs-lookup"><span data-stu-id="17c91-123">string</span></span> | <span data-ttu-id="17c91-124">Nom d’utilisateur principal (UPN) du compte à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="17c91-124">User principal name (UPN) of the account that the recorded action was applied to</span></span> |
| `TargetAccountDisplayName` | <span data-ttu-id="17c91-125">string</span><span class="sxs-lookup"><span data-stu-id="17c91-125">string</span></span> | <span data-ttu-id="17c91-126">Nom complet du compte à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="17c91-126">Display name of the account that the recorded action was applied to</span></span> |
| `TargetDeviceName` | <span data-ttu-id="17c91-127">string</span><span class="sxs-lookup"><span data-stu-id="17c91-127">string</span></span> | <span data-ttu-id="17c91-128">Nom de domaine complet (FQDN) de l’appareil à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="17c91-128">Fully qualified domain name (FQDN) of the device that the recorded action was applied to</span></span> |
| `DestinationDeviceName` | <span data-ttu-id="17c91-129">string</span><span class="sxs-lookup"><span data-stu-id="17c91-129">string</span></span> | <span data-ttu-id="17c91-130">Nom de l’appareil exécutant l’application serveur qui a traitée l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="17c91-130">Name of the device running the server application that processed the recorded action</span></span> |
| `DestinationIPAddress` | <span data-ttu-id="17c91-131">string</span><span class="sxs-lookup"><span data-stu-id="17c91-131">string</span></span> | <span data-ttu-id="17c91-132">Adresse IP de l’appareil exécutant l’application serveur qui a traitée l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="17c91-132">IP address of the device running the server application that processed the recorded action</span></span> |
| `DestinationPort` | <span data-ttu-id="17c91-133">string</span><span class="sxs-lookup"><span data-stu-id="17c91-133">string</span></span> | <span data-ttu-id="17c91-134">Port de destination de l’activité</span><span class="sxs-lookup"><span data-stu-id="17c91-134">Destination port of the activity</span></span> |
| `Protocol` | <span data-ttu-id="17c91-135">string</span><span class="sxs-lookup"><span data-stu-id="17c91-135">string</span></span> | <span data-ttu-id="17c91-136">Protocole utilisé pendant la communication</span><span class="sxs-lookup"><span data-stu-id="17c91-136">Protocol used during the communication</span></span> |
| `AccountName` | <span data-ttu-id="17c91-137">string</span><span class="sxs-lookup"><span data-stu-id="17c91-137">string</span></span> | <span data-ttu-id="17c91-138">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="17c91-138">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="17c91-139">string</span><span class="sxs-lookup"><span data-stu-id="17c91-139">string</span></span> | <span data-ttu-id="17c91-140">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="17c91-140">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="17c91-141">string</span><span class="sxs-lookup"><span data-stu-id="17c91-141">string</span></span> | <span data-ttu-id="17c91-142">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="17c91-142">User principal name (UPN) of the account</span></span> |
| `AccountSid` | <span data-ttu-id="17c91-143">string</span><span class="sxs-lookup"><span data-stu-id="17c91-143">string</span></span> | <span data-ttu-id="17c91-144">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="17c91-144">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="17c91-145">string</span><span class="sxs-lookup"><span data-stu-id="17c91-145">string</span></span> | <span data-ttu-id="17c91-146">Identificateur unique du compte dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="17c91-146">Unique identifier for the account in Azure Active Directory</span></span> |
| `AccountDisplayName` | <span data-ttu-id="17c91-147">string</span><span class="sxs-lookup"><span data-stu-id="17c91-147">string</span></span> | <span data-ttu-id="17c91-148">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="17c91-148">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="17c91-149">En règle générale, une combinaison d’un prénom ou d’un prénom donné, d’une initiation intermédiaire et d’un nom ou d’un nom de famille.</span><span class="sxs-lookup"><span data-stu-id="17c91-149">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="17c91-150">string</span><span class="sxs-lookup"><span data-stu-id="17c91-150">string</span></span> | <span data-ttu-id="17c91-151">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="17c91-151">Fully qualified domain name (FQDN) of the device</span></span> |
| `IPAddress` | <span data-ttu-id="17c91-152">string</span><span class="sxs-lookup"><span data-stu-id="17c91-152">string</span></span> | <span data-ttu-id="17c91-153">Adresse IP attribuée à l’appareil lors de la communication</span><span class="sxs-lookup"><span data-stu-id="17c91-153">IP address assigned to the device during communication</span></span> |
| `Port` | <span data-ttu-id="17c91-154">string</span><span class="sxs-lookup"><span data-stu-id="17c91-154">string</span></span> | <span data-ttu-id="17c91-155">Port TCP utilisé pendant la communication</span><span class="sxs-lookup"><span data-stu-id="17c91-155">TCP port used during communication</span></span> |
| `Location` | <span data-ttu-id="17c91-156">string</span><span class="sxs-lookup"><span data-stu-id="17c91-156">string</span></span> | <span data-ttu-id="17c91-157">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="17c91-157">City, country, or other geographic location associated with the event</span></span> |
| `ISP` | <span data-ttu-id="17c91-158">string</span><span class="sxs-lookup"><span data-stu-id="17c91-158">string</span></span> | <span data-ttu-id="17c91-159">Fournisseur de services Internet associé à l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="17c91-159">Internet service provider associated with the IP address</span></span> |
| `ReportId` | <span data-ttu-id="17c91-160">long</span><span class="sxs-lookup"><span data-stu-id="17c91-160">long</span></span> | <span data-ttu-id="17c91-161">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="17c91-161">Unique identifier for the event</span></span> |
| `AdditionalFields` | <span data-ttu-id="17c91-162">string</span><span class="sxs-lookup"><span data-stu-id="17c91-162">string</span></span> | <span data-ttu-id="17c91-163">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="17c91-163">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="17c91-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17c91-164">Related topics</span></span>
- [<span data-ttu-id="17c91-165">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="17c91-165">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="17c91-166">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="17c91-166">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="17c91-167">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="17c91-167">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="17c91-168">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="17c91-168">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="17c91-169">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="17c91-169">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="17c91-170">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="17c91-170">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
