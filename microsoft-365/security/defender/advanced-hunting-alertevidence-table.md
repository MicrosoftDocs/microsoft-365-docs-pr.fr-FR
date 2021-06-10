---
title: Table AlertEvidence dans le schéma de recherche avancé
description: En savoir plus sur les informations associées aux alertes dans la table AlertEvidence du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, AlertInfo, alert, entities, evidence, file, IP address, device, machine, user, account
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
ms.openlocfilehash: 5ecab217a6181096e4689d78fa2bdddc0a767d0d
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51932582"
---
# <a name="alertevidence"></a><span data-ttu-id="b6d8c-104">AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="b6d8c-104">AlertEvidence</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="b6d8c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b6d8c-105">**Applies to:**</span></span>
- <span data-ttu-id="b6d8c-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b6d8c-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="b6d8c-107">Le tableau du schéma de recherche avancée contient des informations sur différentes `AlertEvidence` entités (fichiers, adresses IP, URL, utilisateurs ou appareils) associées aux alertes de Microsoft Defender pour point de terminaison, Microsoft Defender pour [](advanced-hunting-overview.md) Office 365, Microsoft Cloud App Security et Microsoft Defender pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="b6d8c-107">The `AlertEvidence` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about various entities—files, IP addresses, URLs, users, or devices—associated with alerts from Microsoft  Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity.</span></span> <span data-ttu-id="b6d8c-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="b6d8c-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="b6d8c-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b6d8c-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="b6d8c-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="b6d8c-110">Column name</span></span> | <span data-ttu-id="b6d8c-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6d8c-111">Data type</span></span> | <span data-ttu-id="b6d8c-112">Description</span><span class="sxs-lookup"><span data-stu-id="b6d8c-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="b6d8c-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="b6d8c-113">datetime</span></span> | <span data-ttu-id="b6d8c-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="b6d8c-114">Date and time when the event was recorded</span></span> |
| `AlertId` | <span data-ttu-id="b6d8c-115">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-115">string</span></span> | <span data-ttu-id="b6d8c-116">Identificateur unique de l’alerte</span><span class="sxs-lookup"><span data-stu-id="b6d8c-116">Unique identifier for the alert</span></span> |
| `ServiceSource` | <span data-ttu-id="b6d8c-117">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-117">string</span></span> | <span data-ttu-id="b6d8c-118">Produit ou service qui a fourni les informations d’alerte</span><span class="sxs-lookup"><span data-stu-id="b6d8c-118">Product or service that provided the alert information</span></span> |
| `EntityType` | <span data-ttu-id="b6d8c-119">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-119">string</span></span> | <span data-ttu-id="b6d8c-120">Type d’objet, tel qu’un fichier, un processus, un appareil ou un utilisateur</span><span class="sxs-lookup"><span data-stu-id="b6d8c-120">Type of object, such as a file, a process, a device, or a user</span></span> |
| `EvidenceRole` | <span data-ttu-id="b6d8c-121">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-121">string</span></span> | <span data-ttu-id="b6d8c-122">Comment l’entité est impliquée dans une alerte, indiquant si elle est concernée ou simplement liée</span><span class="sxs-lookup"><span data-stu-id="b6d8c-122">How the entity is involved in an alert, indicating whether it is impacted or is merely related</span></span> |
| `EvidenceDirection` | <span data-ttu-id="b6d8c-123">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-123">string</span></span> | <span data-ttu-id="b6d8c-124">Indique si l’entité est la source ou la destination d’une connexion réseau</span><span class="sxs-lookup"><span data-stu-id="b6d8c-124">Indicates whether the entity is the source or the destination of a network connection</span></span> |
| `FileName` | <span data-ttu-id="b6d8c-125">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-125">string</span></span> | <span data-ttu-id="b6d8c-126">Nom du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="b6d8c-126">Name of the file that the recorded action was applied to</span></span> |
| `FolderPath` | <span data-ttu-id="b6d8c-127">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-127">string</span></span> | <span data-ttu-id="b6d8c-128">Dossier contenant le fichier à lequel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="b6d8c-128">Folder containing the file that the recorded action was applied to</span></span> |
| `SHA1` | <span data-ttu-id="b6d8c-129">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-129">string</span></span> | <span data-ttu-id="b6d8c-130">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="b6d8c-130">SHA-1 of the file that the recorded action was applied to</span></span> |
| `SHA256` | <span data-ttu-id="b6d8c-131">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-131">string</span></span> | <span data-ttu-id="b6d8c-132">SHA-256 du fichier auquel l’action enregistrée a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="b6d8c-132">SHA-256 of the file that the recorded action was applied to.</span></span> <span data-ttu-id="b6d8c-133">Ce champ n’est généralement pas rempli ; utilisez la colonne SHA1 lorsqu’elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="b6d8c-133">This field is usually not populated—use the SHA1 column when available.</span></span> |
| `FileSize` | <span data-ttu-id="b6d8c-134">entier</span><span class="sxs-lookup"><span data-stu-id="b6d8c-134">int</span></span> | <span data-ttu-id="b6d8c-135">Taille du fichier en octets</span><span class="sxs-lookup"><span data-stu-id="b6d8c-135">Size of the file in bytes</span></span> |
| `ThreatFamily` | <span data-ttu-id="b6d8c-136">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-136">string</span></span> | <span data-ttu-id="b6d8c-137">Famille de programmes malveillants sous qui le fichier ou processus suspect ou malveillant a été classé</span><span class="sxs-lookup"><span data-stu-id="b6d8c-137">Malware family that the suspicious or malicious file or process has been classified under</span></span> |
| `RemoteIP` | <span data-ttu-id="b6d8c-138">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-138">string</span></span> | <span data-ttu-id="b6d8c-139">Adresse IP à laquelle la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="b6d8c-139">IP address that was being connected to</span></span> |
| `RemoteUrl` | <span data-ttu-id="b6d8c-140">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-140">string</span></span> | <span data-ttu-id="b6d8c-141">URL ou nom de domaine complet (FQDN) à laquelle/auquel la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="b6d8c-141">URL or fully qualified domain name (FQDN) that was being connected to</span></span> |
| `AccountName` | <span data-ttu-id="b6d8c-142">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-142">string</span></span> | <span data-ttu-id="b6d8c-143">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="b6d8c-143">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="b6d8c-144">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-144">string</span></span> | <span data-ttu-id="b6d8c-145">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="b6d8c-145">Domain of the account</span></span> |
| `AccountSid` | <span data-ttu-id="b6d8c-146">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-146">string</span></span> | <span data-ttu-id="b6d8c-147">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="b6d8c-147">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="b6d8c-148">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-148">string</span></span> | <span data-ttu-id="b6d8c-149">Identificateur unique du compte dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b6d8c-149">Unique identifier for the account in Azure Active Directory</span></span> |
| `AccountUpn` | <span data-ttu-id="b6d8c-150">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-150">string</span></span> | <span data-ttu-id="b6d8c-151">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="b6d8c-151">User principal name (UPN) of the account</span></span> |
| `DeviceId` | <span data-ttu-id="b6d8c-152">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-152">string</span></span> | <span data-ttu-id="b6d8c-153">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="b6d8c-153">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="b6d8c-154">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-154">string</span></span> | <span data-ttu-id="b6d8c-155">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="b6d8c-155">Fully qualified domain name (FQDN) of the machine</span></span> |
| `LocalIP` | <span data-ttu-id="b6d8c-156">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-156">string</span></span> | <span data-ttu-id="b6d8c-157">Adresse IP attribuée à l’appareil local utilisé lors de la communication</span><span class="sxs-lookup"><span data-stu-id="b6d8c-157">IP address assigned to the local device used during communication</span></span> |
| `NetworkMessageId` | <span data-ttu-id="b6d8c-158">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-158">string</span></span> | <span data-ttu-id="b6d8c-159">Identificateur unique d’e-mail, généré par Office 365</span><span class="sxs-lookup"><span data-stu-id="b6d8c-159">Unique identifier for the email, generated by Office 365</span></span> |
| `EmailSubject` | <span data-ttu-id="b6d8c-160">chaîne</span><span class="sxs-lookup"><span data-stu-id="b6d8c-160">string</span></span> | <span data-ttu-id="b6d8c-161">Objet de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="b6d8c-161">Subject of the email</span></span> |
| `ApplicationId` | <span data-ttu-id="b6d8c-162">chaîne</span><span class="sxs-lookup"><span data-stu-id="b6d8c-162">string</span></span> | <span data-ttu-id="b6d8c-163">Identificateur unique de l’application</span><span class="sxs-lookup"><span data-stu-id="b6d8c-163">Unique identifier for the application</span></span> |
| `Application` | <span data-ttu-id="b6d8c-164">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-164">string</span></span> | <span data-ttu-id="b6d8c-165">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="b6d8c-165">Application that performed the recorded action</span></span> |
| `ProcessCommandLine` | <span data-ttu-id="b6d8c-166">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-166">string</span></span> | <span data-ttu-id="b6d8c-167">Ligne de commande utilisée pour créer le nouveau processus</span><span class="sxs-lookup"><span data-stu-id="b6d8c-167">Command line used to create the new process</span></span> |
| `AdditionalFields` | <span data-ttu-id="b6d8c-168">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-168">string</span></span> | <span data-ttu-id="b6d8c-169">Informations supplémentaires sur l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="b6d8c-169">Additional information about the event in JSON array format</span></span> |
| `RegistryKey` |<span data-ttu-id="b6d8c-170">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-170">string</span></span> | <span data-ttu-id="b6d8c-171">Clé de Registre à l’application de l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="b6d8c-171">Registry key that the recorded action was applied to</span></span> |
| `RegistryValueName` |<span data-ttu-id="b6d8c-172">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-172">string</span></span> | <span data-ttu-id="b6d8c-173">Nom de la valeur de Registre à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="b6d8c-173">Name of the registry value that the recorded action was applied to</span></span> |
| `RegistryValueData` |<span data-ttu-id="b6d8c-174">string</span><span class="sxs-lookup"><span data-stu-id="b6d8c-174">string</span></span> | <span data-ttu-id="b6d8c-175">Données de la valeur de Registre à l’application de l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="b6d8c-175">Data of the registry value that the recorded action was applied to</span></span> |

## <a name="related-topics"></a><span data-ttu-id="b6d8c-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6d8c-176">Related topics</span></span>
- [<span data-ttu-id="b6d8c-177">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="b6d8c-177">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="b6d8c-178">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="b6d8c-178">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="b6d8c-179">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="b6d8c-179">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="b6d8c-180">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="b6d8c-180">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="b6d8c-181">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="b6d8c-181">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="b6d8c-182">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="b6d8c-182">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
