---
title: Table AlertEvidence dans le schéma de recherche avancé
description: En savoir plus sur les informations associées aux alertes dans la table AlertEvidence du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, AlertInfo, alert, entities, evidence, file, IP address, device, machine, user, account
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
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
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: c01b0aae1eff3d9b4add632aff0f13cb56941a30
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49932303"
---
# <a name="alertevidence"></a><span data-ttu-id="8ad9c-104">AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="8ad9c-104">AlertEvidence</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="8ad9c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8ad9c-105">**Applies to:**</span></span>
- <span data-ttu-id="8ad9c-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8ad9c-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="8ad9c-107">Le tableau du schéma de recherche avancée contient des informations sur différentes `AlertEvidence` entités (fichiers, adresses IP, URL, utilisateurs ou appareils) associées aux alertes de Microsoft Defender pour endpoint, Microsoft Defender pour Office 365, Microsoft Cloud App Security et Microsoft Defender pour l’identité. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8ad9c-107">The `AlertEvidence` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about various entities—files, IP addresses, URLs, users, or devices—associated with alerts from Microsoft  Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity.</span></span> <span data-ttu-id="8ad9c-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="8ad9c-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8ad9c-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="8ad9c-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="8ad9c-110">Column name</span></span> | <span data-ttu-id="8ad9c-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="8ad9c-111">Data type</span></span> | <span data-ttu-id="8ad9c-112">Description</span><span class="sxs-lookup"><span data-stu-id="8ad9c-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="8ad9c-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="8ad9c-113">datetime</span></span> | <span data-ttu-id="8ad9c-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="8ad9c-114">Date and time when the event was recorded</span></span> |
| `AlertId` | <span data-ttu-id="8ad9c-115">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-115">string</span></span> | <span data-ttu-id="8ad9c-116">Identificateur unique de l’alerte</span><span class="sxs-lookup"><span data-stu-id="8ad9c-116">Unique identifier for the alert</span></span> |
| `ServiceSource` | <span data-ttu-id="8ad9c-117">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-117">string</span></span> | <span data-ttu-id="8ad9c-118">Produit ou service qui a fourni les informations d’alerte</span><span class="sxs-lookup"><span data-stu-id="8ad9c-118">Product or service that provided the alert information</span></span> |
| `EntityType` | <span data-ttu-id="8ad9c-119">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-119">string</span></span> | <span data-ttu-id="8ad9c-120">Type d’objet, tel qu’un fichier, un processus, un appareil ou un utilisateur</span><span class="sxs-lookup"><span data-stu-id="8ad9c-120">Type of object, such as a file, a process, a device, or a user</span></span> |
| `EvidenceRole` | <span data-ttu-id="8ad9c-121">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-121">string</span></span> | <span data-ttu-id="8ad9c-122">Comment l’entité est impliquée dans une alerte, indiquant si elle est concernée ou simplement liée</span><span class="sxs-lookup"><span data-stu-id="8ad9c-122">How the entity is involved in an alert, indicating whether it is impacted or is merely related</span></span> |
| `EvidenceDirection` | <span data-ttu-id="8ad9c-123">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-123">string</span></span> | <span data-ttu-id="8ad9c-124">Indique si l’entité est la source ou la destination d’une connexion réseau</span><span class="sxs-lookup"><span data-stu-id="8ad9c-124">Indicates whether the entity is the source or the destination of a network connection</span></span> |
| `FileName` | <span data-ttu-id="8ad9c-125">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-125">string</span></span> | <span data-ttu-id="8ad9c-126">Nom du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="8ad9c-126">Name of the file that the recorded action was applied to</span></span> |
| `FolderPath` | <span data-ttu-id="8ad9c-127">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-127">string</span></span> | <span data-ttu-id="8ad9c-128">Dossier contenant le fichier à lequel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="8ad9c-128">Folder containing the file that the recorded action was applied to</span></span> |
| `SHA1` | <span data-ttu-id="8ad9c-129">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-129">string</span></span> | <span data-ttu-id="8ad9c-130">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="8ad9c-130">SHA-1 of the file that the recorded action was applied to</span></span> |
| `SHA256` | <span data-ttu-id="8ad9c-131">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-131">string</span></span> | <span data-ttu-id="8ad9c-132">SHA-256 du fichier auquel l’action enregistrée a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-132">SHA-256 of the file that the recorded action was applied to.</span></span> <span data-ttu-id="8ad9c-133">Ce champ n’est généralement pas rempli ; utilisez la colonne SHA1 lorsqu’elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="8ad9c-133">This field is usually not populated—use the SHA1 column when available.</span></span> |
| `FileSize` | <span data-ttu-id="8ad9c-134">int</span><span class="sxs-lookup"><span data-stu-id="8ad9c-134">int</span></span> | <span data-ttu-id="8ad9c-135">Taille du fichier en octets</span><span class="sxs-lookup"><span data-stu-id="8ad9c-135">Size of the file in bytes</span></span> |
| `ThreatFamily` | <span data-ttu-id="8ad9c-136">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-136">string</span></span> | <span data-ttu-id="8ad9c-137">Famille de programmes malveillants sous qui le fichier ou processus suspect ou malveillant a été classé</span><span class="sxs-lookup"><span data-stu-id="8ad9c-137">Malware family that the suspicious or malicious file or process has been classified under</span></span> |
| `RemoteIP` | <span data-ttu-id="8ad9c-138">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-138">string</span></span> | <span data-ttu-id="8ad9c-139">Adresse IP à laquelle la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="8ad9c-139">IP address that was being connected to</span></span> |
| `RemoteUrl` | <span data-ttu-id="8ad9c-140">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-140">string</span></span> | <span data-ttu-id="8ad9c-141">URL ou nom de domaine complet (FQDN) à laquelle/auquel la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="8ad9c-141">URL or fully qualified domain name (FQDN) that was being connected to</span></span> |
| `AccountName` | <span data-ttu-id="8ad9c-142">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-142">string</span></span> | <span data-ttu-id="8ad9c-143">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="8ad9c-143">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="8ad9c-144">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-144">string</span></span> | <span data-ttu-id="8ad9c-145">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="8ad9c-145">Domain of the account</span></span> |
| `AccountSid` | <span data-ttu-id="8ad9c-146">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-146">string</span></span> | <span data-ttu-id="8ad9c-147">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="8ad9c-147">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="8ad9c-148">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-148">string</span></span> | <span data-ttu-id="8ad9c-149">Identificateur unique du compte dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8ad9c-149">Unique identifier for the account in Azure Active Directory</span></span> |
| `DeviceId` | <span data-ttu-id="8ad9c-150">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-150">string</span></span> | <span data-ttu-id="8ad9c-151">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="8ad9c-151">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="8ad9c-152">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-152">string</span></span> | <span data-ttu-id="8ad9c-153">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="8ad9c-153">Fully qualified domain name (FQDN) of the machine</span></span> |
| `LocalIP` | <span data-ttu-id="8ad9c-154">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-154">string</span></span> | <span data-ttu-id="8ad9c-155">Adresse IP attribuée à l’appareil local utilisé lors de la communication</span><span class="sxs-lookup"><span data-stu-id="8ad9c-155">IP address assigned to the local device used during communication</span></span> |
| `NetworkMessageId` | <span data-ttu-id="8ad9c-156">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-156">string</span></span> | <span data-ttu-id="8ad9c-157">Identificateur unique d’e-mail, généré par Office 365</span><span class="sxs-lookup"><span data-stu-id="8ad9c-157">Unique identifier for the email, generated by Office 365</span></span> |
| `EmailSubject` | <span data-ttu-id="8ad9c-158">chaîne</span><span class="sxs-lookup"><span data-stu-id="8ad9c-158">string</span></span> | <span data-ttu-id="8ad9c-159">Objet de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="8ad9c-159">Subject of the email</span></span> |
| `ApplicationId` | <span data-ttu-id="8ad9c-160">chaîne</span><span class="sxs-lookup"><span data-stu-id="8ad9c-160">string</span></span> | <span data-ttu-id="8ad9c-161">Identificateur unique de l’application</span><span class="sxs-lookup"><span data-stu-id="8ad9c-161">Unique identifier for the application</span></span> |
| `Application` | <span data-ttu-id="8ad9c-162">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-162">string</span></span> | <span data-ttu-id="8ad9c-163">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="8ad9c-163">Application that performed the recorded action</span></span> |
| `ProcessCommandLine` | <span data-ttu-id="8ad9c-164">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-164">string</span></span> | <span data-ttu-id="8ad9c-165">Ligne de commande utilisée pour créer le nouveau processus</span><span class="sxs-lookup"><span data-stu-id="8ad9c-165">Command line used to create the new process</span></span> |
| `AdditionalFields` | <span data-ttu-id="8ad9c-166">string</span><span class="sxs-lookup"><span data-stu-id="8ad9c-166">string</span></span> | <span data-ttu-id="8ad9c-167">Informations supplémentaires sur l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="8ad9c-167">Additional information about the event in JSON array format</span></span> |

## <a name="related-topics"></a><span data-ttu-id="8ad9c-168">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="8ad9c-168">Related topics</span></span>
- [<span data-ttu-id="8ad9c-169">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="8ad9c-169">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="8ad9c-170">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="8ad9c-170">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="8ad9c-171">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="8ad9c-171">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="8ad9c-172">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="8ad9c-172">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="8ad9c-173">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="8ad9c-173">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="8ad9c-174">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="8ad9c-174">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
