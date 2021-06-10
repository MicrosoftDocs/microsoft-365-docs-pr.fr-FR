---
title: Table CloudAppEvents dans le schéma de recherche avancé
description: En savoir plus sur les événements des applications et services cloud dans la table CloudAppEvents du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, CloudAppEvents, Sécurité des applications cloud, MCAS
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
ms.openlocfilehash: 17f424d368c0df2f07cda41917f005e4163e5750
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935868"
---
# <a name="cloudappevents"></a><span data-ttu-id="53c7c-104">CloudAppEvents</span><span class="sxs-lookup"><span data-stu-id="53c7c-104">CloudAppEvents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="53c7c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="53c7c-105">**Applies to:**</span></span>
- <span data-ttu-id="53c7c-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="53c7c-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="53c7c-107">Le tableau du schéma de recherche avancée contient des informations sur les activités dans diverses applications et services cloud couverts par `CloudAppEvents` Microsoft Cloud App Security. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="53c7c-107">The `CloudAppEvents` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about activities in various cloud apps and services covered by Microsoft Cloud App Security.</span></span> <span data-ttu-id="53c7c-108">Pour obtenir la liste complète, voir [Applications et services couverts.](#apps-and-services-covered)</span><span class="sxs-lookup"><span data-stu-id="53c7c-108">For a complete list, jump to [Apps and services covered](#apps-and-services-covered).</span></span> <span data-ttu-id="53c7c-109">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="53c7c-109">Use this reference to construct queries that return information from this table.</span></span> 

>[!IMPORTANT]
><span data-ttu-id="53c7c-110">Ce tableau inclut des informations qui étaient disponibles dans le `AppFileEvents` tableau.</span><span class="sxs-lookup"><span data-stu-id="53c7c-110">This table includes information that used to be available in the `AppFileEvents` table.</span></span> <span data-ttu-id="53c7c-111">À compter du 7 mars 2021, les utilisateurs qui recherchent des activités liées aux fichiers dans les services cloud et au-delà de cette date doivent utiliser le `CloudAppEvents` tableau à la place.</span><span class="sxs-lookup"><span data-stu-id="53c7c-111">Starting March 7, 2021, users hunting through file-related activities in cloud services on and beyond this date should use the `CloudAppEvents` table instead.</span></span> <br><br><span data-ttu-id="53c7c-112">Veillez à rechercher les requêtes et les règles de détection personnalisées qui utilisent toujours le tableau et à les `AppFileEvents` modifier pour utiliser le `CloudAppEvents` tableau.</span><span class="sxs-lookup"><span data-stu-id="53c7c-112">Make sure to search for queries and custom detection rules that still use the `AppFileEvents` table and edit them to use the `CloudAppEvents` table.</span></span> <span data-ttu-id="53c7c-113">Pour plus d’informations sur la conversion des requêtes affectées, voir La recherche dans les activités d’application [cloud avec Microsoft 365 defender - recherche avancée.](https://techcommunity.microsoft.com/t5/microsoft-365-defender/hunt-across-cloud-app-activities-with-microsoft-365-defender/ba-p/1893857)</span><span class="sxs-lookup"><span data-stu-id="53c7c-113">More guidance about converting affected queries can be found in [Hunt across cloud app activities with Microsoft 365 Defender advanced hunting](https://techcommunity.microsoft.com/t5/microsoft-365-defender/hunt-across-cloud-app-activities-with-microsoft-365-defender/ba-p/1893857).</span></span>


<span data-ttu-id="53c7c-114">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="53c7c-114">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="53c7c-115">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="53c7c-115">Column name</span></span> | <span data-ttu-id="53c7c-116">Type de données</span><span class="sxs-lookup"><span data-stu-id="53c7c-116">Data type</span></span> | <span data-ttu-id="53c7c-117">Description</span><span class="sxs-lookup"><span data-stu-id="53c7c-117">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="53c7c-118">DateHeure</span><span class="sxs-lookup"><span data-stu-id="53c7c-118">datetime</span></span> | <span data-ttu-id="53c7c-119">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="53c7c-119">Date and time when the event was recorded</span></span> |
| `ActionType` | <span data-ttu-id="53c7c-120">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-120">string</span></span> | <span data-ttu-id="53c7c-121">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="53c7c-121">Type of activity that triggered the event</span></span> |
| `Application` | <span data-ttu-id="53c7c-122">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-122">string</span></span> | <span data-ttu-id="53c7c-123">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="53c7c-123">Application that performed the recorded action</span></span> |
| `ApplicationId` | <span data-ttu-id="53c7c-124">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-124">string</span></span> | <span data-ttu-id="53c7c-125">Identificateur unique de l’application</span><span class="sxs-lookup"><span data-stu-id="53c7c-125">Unique identifier for the application</span></span> |
| `AccountObjectId` | <span data-ttu-id="53c7c-126">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-126">string</span></span> | <span data-ttu-id="53c7c-127">Identificateur unique du compte dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="53c7c-127">Unique identifier for the account in Azure Active Directory</span></span> |
| `AccountDisplayName` | <span data-ttu-id="53c7c-128">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-128">string</span></span> | <span data-ttu-id="53c7c-129">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="53c7c-129">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="53c7c-130">En règle générale, une combinaison d’un prénom ou d’un prénom donné, d’une initiation intermédiaire et d’un nom ou d’un nom de famille.</span><span class="sxs-lookup"><span data-stu-id="53c7c-130">Typically a combination of a given or first name, a middle initiation, and a last name or surname.</span></span> |
| `IsAdminOperation` | <span data-ttu-id="53c7c-131">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-131">string</span></span> | <span data-ttu-id="53c7c-132">Indique si l’activité a été effectuée par un administrateur</span><span class="sxs-lookup"><span data-stu-id="53c7c-132">Indicates whether the activity was performed by an administrator</span></span> |
| `DeviceType` | <span data-ttu-id="53c7c-133">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-133">string</span></span> | <span data-ttu-id="53c7c-134">Type d’appareil en fonction de l’objectif et des fonctionnalités, tels que « Périphérique réseau », « Station de travail », « Serveur », « Mobile », « Console de jeu » ou « Imprimante »</span><span class="sxs-lookup"><span data-stu-id="53c7c-134">Type of device based on purpose and functionality, such as "Network device", "Workstation", "Server", "Mobile", "Gaming console", or "Printer"</span></span> | 
| `OSPlatform` | <span data-ttu-id="53c7c-135">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-135">string</span></span> | <span data-ttu-id="53c7c-136">Plateforme du système d’exploitation en cours d’exécution sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="53c7c-136">Platform of the operating system running on the device.</span></span> <span data-ttu-id="53c7c-137">Cette colonne indique des systèmes d’exploitation spécifiques, y compris des variantes au sein de la même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="53c7c-137">This column indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span> |
| `IPAddress` | <span data-ttu-id="53c7c-138">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-138">string</span></span> | <span data-ttu-id="53c7c-139">Adresse IP attribuée au point de terminaison et utilisée lors des communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="53c7c-139">IP address assigned to the endpoint and used during related network communications</span></span> |
| `IsAnonymousProxy` | <span data-ttu-id="53c7c-140">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-140">string</span></span> | <span data-ttu-id="53c7c-141">Indique si l’adresse IP appartient à un proxy anonyme connu</span><span class="sxs-lookup"><span data-stu-id="53c7c-141">Indicates whether the IP address belongs to a known anonymous proxy</span></span> |
| `CountryCode` | <span data-ttu-id="53c7c-142">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-142">string</span></span> | <span data-ttu-id="53c7c-143">Code à deux lettres indiquant le pays où l’adresse IP du client est géolocalisé</span><span class="sxs-lookup"><span data-stu-id="53c7c-143">Two-letter code indicating the country where the client IP address is geolocated</span></span> |
| `City` | <span data-ttu-id="53c7c-144">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-144">string</span></span> | <span data-ttu-id="53c7c-145">Ville où l’adresse IP du client est géolocalisé</span><span class="sxs-lookup"><span data-stu-id="53c7c-145">City where the client IP address is geolocated</span></span> |
| `Isp` | <span data-ttu-id="53c7c-146">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-146">string</span></span> | <span data-ttu-id="53c7c-147">Fournisseur de services Internet (ISP) associé à l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="53c7c-147">Internet service provider (ISP) associated with the IP address</span></span> |
| `UserAgent` | <span data-ttu-id="53c7c-148">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-148">string</span></span> | <span data-ttu-id="53c7c-149">Informations sur l’agent utilisateur à partir du navigateur web ou d’une autre application cliente</span><span class="sxs-lookup"><span data-stu-id="53c7c-149">User agent information from the web browser or other client application</span></span> |
| `ActivityType` | <span data-ttu-id="53c7c-150">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-150">string</span></span> | <span data-ttu-id="53c7c-151">Type d’activité qui a déclenché l’événement</span><span class="sxs-lookup"><span data-stu-id="53c7c-151">Type of activity that triggered the event</span></span> |
| `ActivityObjects` | <span data-ttu-id="53c7c-152">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-152">string</span></span> | <span data-ttu-id="53c7c-153">Liste des objets, tels que des fichiers ou des dossiers, qui ont été impliqués dans l’activité enregistrée</span><span class="sxs-lookup"><span data-stu-id="53c7c-153">List of objects, such as files or folders, that were involved in the recorded activity</span></span> |
| `ObjectName` | <span data-ttu-id="53c7c-154">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-154">string</span></span> | <span data-ttu-id="53c7c-155">Nom de l’objet à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="53c7c-155">Name of the object that the recorded action was applied to</span></span> |
| `ObjectType` | <span data-ttu-id="53c7c-156">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-156">string</span></span> | <span data-ttu-id="53c7c-157">Type d’objet, tel qu’un fichier ou un dossier, à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="53c7c-157">Type of object, such as a file or a folder, that the recorded action was applied to</span></span> |
| `ObjectId` | <span data-ttu-id="53c7c-158">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-158">string</span></span> | <span data-ttu-id="53c7c-159">Identificateur unique de l’objet à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="53c7c-159">Unique identifier of the object that the recorded action was applied to</span></span> |
| `ReportId` | <span data-ttu-id="53c7c-160">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-160">string</span></span> | <span data-ttu-id="53c7c-161">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="53c7c-161">Unique identifier for the event</span></span> |
| `RawEventData` | <span data-ttu-id="53c7c-162">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-162">string</span></span> | <span data-ttu-id="53c7c-163">Informations d’événement brutes de l’application ou du service source au format JSON</span><span class="sxs-lookup"><span data-stu-id="53c7c-163">Raw event information from the source application or service in JSON format</span></span> |
| `AdditionalFields` | <span data-ttu-id="53c7c-164">string</span><span class="sxs-lookup"><span data-stu-id="53c7c-164">string</span></span> | <span data-ttu-id="53c7c-165">Informations supplémentaires sur l’entité ou l’événement</span><span class="sxs-lookup"><span data-stu-id="53c7c-165">Additional information about the entity or event</span></span> |

## <a name="apps-and-services-covered"></a><span data-ttu-id="53c7c-166">Applications et services couverts</span><span class="sxs-lookup"><span data-stu-id="53c7c-166">Apps and services covered</span></span>

- <span data-ttu-id="53c7c-167">Dropbox</span><span class="sxs-lookup"><span data-stu-id="53c7c-167">Dropbox</span></span>
- <span data-ttu-id="53c7c-168">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="53c7c-168">Dynamics 365</span></span>
- <span data-ttu-id="53c7c-169">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="53c7c-169">Exchange Online</span></span>
- <span data-ttu-id="53c7c-170">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="53c7c-170">Microsoft Teams</span></span>
- <span data-ttu-id="53c7c-171">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="53c7c-171">OneDrive for Business</span></span>
- <span data-ttu-id="53c7c-172">Power Automate</span><span class="sxs-lookup"><span data-stu-id="53c7c-172">Power Automate</span></span>
- <span data-ttu-id="53c7c-173">Power BI</span><span class="sxs-lookup"><span data-stu-id="53c7c-173">Power BI</span></span>
- <span data-ttu-id="53c7c-174">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="53c7c-174">SharePoint Online</span></span>
- <span data-ttu-id="53c7c-175">Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="53c7c-175">Skype for Business</span></span>
- <span data-ttu-id="53c7c-176">Office 365</span><span class="sxs-lookup"><span data-stu-id="53c7c-176">Office 365</span></span>
- <span data-ttu-id="53c7c-177">Yammer</span><span class="sxs-lookup"><span data-stu-id="53c7c-177">Yammer</span></span> 

## <a name="related-topics"></a><span data-ttu-id="53c7c-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53c7c-178">Related topics</span></span>
- [<span data-ttu-id="53c7c-179">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="53c7c-179">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="53c7c-180">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="53c7c-180">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="53c7c-181">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="53c7c-181">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="53c7c-182">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="53c7c-182">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="53c7c-183">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="53c7c-183">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="53c7c-184">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="53c7c-184">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
