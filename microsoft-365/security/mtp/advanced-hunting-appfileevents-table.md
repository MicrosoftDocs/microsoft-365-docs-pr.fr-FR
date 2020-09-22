---
title: Table AppFileEvents dans le schéma de chasse avancé
description: En savoir plus sur les événements liés aux fichiers associés aux applications et services Cloud dans le tableau AppFileEvents du schéma de chasse avancé
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, AppFileEvents, sécurité des applications Cloud, MCAS
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
ms.openlocfilehash: 385011382d20919b219cf84e13cda4993826691b
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48197060"
---
# <a name="appfileevents"></a><span data-ttu-id="3d59a-104">AppFileEvents</span><span class="sxs-lookup"><span data-stu-id="3d59a-104">AppFileEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="3d59a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3d59a-105">**Applies to:**</span></span>
- <span data-ttu-id="3d59a-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="3d59a-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="3d59a-107">Le `AppFileEvents` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les activités liées aux fichiers dans les applications et les services Cloud surveillés par la sécurité des applications Cloud de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d59a-107">The `AppFileEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about file-related activities in cloud apps and services monitored by Microsoft Cloud App Security.</span></span> <span data-ttu-id="3d59a-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="3d59a-108">Use this reference to construct queries that return information from this table.</span></span>

>[!TIP]
> <span data-ttu-id="3d59a-109">Pour plus d’informations sur les types d’événements ( `ActionType` valeurs) pris en charge par un tableau, utilisez la [référence de schéma intégrée](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) disponible dans le centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3d59a-109">For detailed information about the events types (`ActionType` values) supported by a table, use the [built-in schema reference](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) available in the security center.</span></span>

<span data-ttu-id="3d59a-110">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3d59a-110">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="3d59a-111">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="3d59a-111">Column name</span></span> | <span data-ttu-id="3d59a-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="3d59a-112">Data type</span></span> | <span data-ttu-id="3d59a-113">Description</span><span class="sxs-lookup"><span data-stu-id="3d59a-113">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="3d59a-114">DateHeure</span><span class="sxs-lookup"><span data-stu-id="3d59a-114">datetime</span></span> | <span data-ttu-id="3d59a-115">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="3d59a-115">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="3d59a-116">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-116">string</span></span> | <span data-ttu-id="3d59a-117">Type d’activité qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="3d59a-117">Type of activity that triggered the event.</span></span> <span data-ttu-id="3d59a-118">Pour plus d’informations, consultez la [référence de schéma dans le portail](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) .</span><span class="sxs-lookup"><span data-stu-id="3d59a-118">See the [in-portal schema reference](advanced-hunting-schema-tables.md?#get-schema-information-in-the-security-center) for details</span></span> |
| `Application` | <span data-ttu-id="3d59a-119">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-119">string</span></span> | <span data-ttu-id="3d59a-120">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="3d59a-120">Application that performed the recorded action</span></span> |
| `FileName` | <span data-ttu-id="3d59a-121">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-121">string</span></span> | <span data-ttu-id="3d59a-122">Nom du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="3d59a-122">Name of the file that the recorded action was applied to</span></span> |
| `FolderPath` | <span data-ttu-id="3d59a-123">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-123">string</span></span> | <span data-ttu-id="3d59a-124">Dossier contenant le fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="3d59a-124">Folder containing the file that the recorded action was applied to</span></span> |
| `PreviousFileName` | <span data-ttu-id="3d59a-125">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-125">string</span></span> | <span data-ttu-id="3d59a-126">Nom d’origine du fichier qui a été renommé suite à l’action</span><span class="sxs-lookup"><span data-stu-id="3d59a-126">Original name of the file that was renamed as a result of the action</span></span> |
| `PreviousFolderPath` | <span data-ttu-id="3d59a-127">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-127">string</span></span> | <span data-ttu-id="3d59a-128">Dossier d’origine contenant le fichier avant l’application de l’action enregistrer</span><span class="sxs-lookup"><span data-stu-id="3d59a-128">Original folder containing the file before the recorded action was applied</span></span> |
| `Protocol` | <span data-ttu-id="3d59a-129">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-129">string</span></span> | <span data-ttu-id="3d59a-130">Protocole réseau utilisé</span><span class="sxs-lookup"><span data-stu-id="3d59a-130">Network protocol used</span></span> |
| `AccountName` | <span data-ttu-id="3d59a-131">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-131">string</span></span> | <span data-ttu-id="3d59a-132">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="3d59a-132">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="3d59a-133">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-133">string</span></span> | <span data-ttu-id="3d59a-134">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="3d59a-134">Domain of the account</span></span> |
| `AccountUpn` | <span data-ttu-id="3d59a-135">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-135">string</span></span> | <span data-ttu-id="3d59a-136">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="3d59a-136">User principal name (UPN) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="3d59a-137">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-137">string</span></span> | <span data-ttu-id="3d59a-138">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="3d59a-138">Unique identifier for the account in Azure AD</span></span> |
| `AccountDisplayName` | <span data-ttu-id="3d59a-139">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-139">string</span></span> | <span data-ttu-id="3d59a-140">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3d59a-140">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="3d59a-141">Il s’agit généralement d’une combinaison d’un nom donné, d’une initiation au milieu et d’un nom de famille ou nom.</span><span class="sxs-lookup"><span data-stu-id="3d59a-141">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `DeviceName` | <span data-ttu-id="3d59a-142">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-142">string</span></span> | <span data-ttu-id="3d59a-143">Nom de domaine complet (FQDN) du périphérique</span><span class="sxs-lookup"><span data-stu-id="3d59a-143">Fully qualified domain name (FQDN) of the device</span></span> |
| `DeviceType` | <span data-ttu-id="3d59a-144">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-144">string</span></span> | <span data-ttu-id="3d59a-145">Type de périphérique</span><span class="sxs-lookup"><span data-stu-id="3d59a-145">Type of device</span></span> | 
| `OSPlatform` | <span data-ttu-id="3d59a-146">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-146">string</span></span> | <span data-ttu-id="3d59a-147">Plateforme du système d’exploitation s’exécutant sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3d59a-147">Platform of the operating system running on the device.</span></span> <span data-ttu-id="3d59a-148">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3d59a-148">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `IPAddress` | <span data-ttu-id="3d59a-149">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-149">string</span></span> | <span data-ttu-id="3d59a-150">Adresse IP affectée au point de terminaison et utilisée pendant les communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="3d59a-150">IP address assigned to the endpoint and used during related network communications</span></span> |
| `DestinationDeviceName` | <span data-ttu-id="3d59a-151">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-151">string</span></span> | <span data-ttu-id="3d59a-152">Nom de l’appareil exécutant l’application serveur qui a traité l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="3d59a-152">Name of the device running the server application that processed the recorded action</span></span> |
| `DestinationIPAddress` | <span data-ttu-id="3d59a-153">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-153">string</span></span> | <span data-ttu-id="3d59a-154">Adresse IP de l’appareil exécutant l’application serveur qui a traité l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="3d59a-154">IP address of the device running the server application that processed the recorded action</span></span> |
| `Location` | <span data-ttu-id="3d59a-155">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-155">string</span></span> | <span data-ttu-id="3d59a-156">Ville, pays ou autre emplacement géographique associé à l’événement</span><span class="sxs-lookup"><span data-stu-id="3d59a-156">City, country, or other geographic location associated with the event</span></span> |
| `Isp` | <span data-ttu-id="3d59a-157">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-157">string</span></span> | <span data-ttu-id="3d59a-158">Fournisseur de services Internet associé à l’adresse IP du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3d59a-158">Internet service provider (ISP) associated with the endpoint IP address</span></span> |
| `ReportId` | <span data-ttu-id="3d59a-159">long</span><span class="sxs-lookup"><span data-stu-id="3d59a-159">long</span></span> | <span data-ttu-id="3d59a-160">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="3d59a-160">Unique identifier for the event</span></span> |
| `AdditionalFields` | <span data-ttu-id="3d59a-161">string</span><span class="sxs-lookup"><span data-stu-id="3d59a-161">string</span></span> | <span data-ttu-id="3d59a-162">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="3d59a-162">Additional information about the entity or event</span></span> |

## <a name="related-topics"></a><span data-ttu-id="3d59a-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d59a-163">Related topics</span></span>
- [<span data-ttu-id="3d59a-164">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="3d59a-164">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="3d59a-165">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="3d59a-165">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="3d59a-166">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="3d59a-166">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="3d59a-167">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="3d59a-167">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="3d59a-168">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="3d59a-168">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="3d59a-169">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="3d59a-169">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
