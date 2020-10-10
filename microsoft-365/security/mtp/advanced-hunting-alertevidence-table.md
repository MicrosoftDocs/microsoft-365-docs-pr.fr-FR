---
title: Table AlertEvidence dans le schéma de chasse avancé
description: En savoir plus sur les informations associées aux alertes dans la table AlertEvidence du schéma de chasse avancé
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, AlertInfo, alerte, entités, preuve, fichier, adresse IP, appareil, ordinateur, utilisateur, compte
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
ms.collection:
- M365-security-compliance
- m365-initiative-m365-defender
ms.topic: article
ms.openlocfilehash: ec6fe3d080efb396ce0ecacadd3d5d9a8fa9f8d1
ms.sourcegitcommit: 5e1b8c959a081022826fb09358730096248507ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48413197"
---
# <a name="alertevidence"></a><span data-ttu-id="e0ae2-104">AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="e0ae2-104">AlertEvidence</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="e0ae2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e0ae2-105">**Applies to:**</span></span>
- <span data-ttu-id="e0ae2-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e0ae2-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="e0ae2-107">Le `AlertEvidence` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les différentes entités (fichiers, adresses IP, URL, utilisateurs ou périphériques) associées aux alertes de Microsoft Defender atp, Office 365 ATP, Microsoft Cloud App Security et Azure ATP.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-107">The `AlertEvidence` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about various entities—files, IP addresses, URLs, users, or devices—associated with alerts from Microsoft Defender ATP, Office 365 ATP, Microsoft Cloud App Security, and Azure ATP.</span></span> <span data-ttu-id="e0ae2-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="e0ae2-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e0ae2-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="e0ae2-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="e0ae2-110">Column name</span></span> | <span data-ttu-id="e0ae2-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="e0ae2-111">Data type</span></span> | <span data-ttu-id="e0ae2-112">Description</span><span class="sxs-lookup"><span data-stu-id="e0ae2-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="e0ae2-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="e0ae2-113">datetime</span></span> | <span data-ttu-id="e0ae2-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="e0ae2-114">Date and time when the event was recorded</span></span> |
| `AlertId` | <span data-ttu-id="e0ae2-115">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-115">string</span></span> | <span data-ttu-id="e0ae2-116">Identificateur unique de l’alerte</span><span class="sxs-lookup"><span data-stu-id="e0ae2-116">Unique identifier for the alert</span></span> |
| `ServiceSource` | <span data-ttu-id="e0ae2-117">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-117">string</span></span> | <span data-ttu-id="e0ae2-118">Produit ou service qui a fourni les informations d’alerte</span><span class="sxs-lookup"><span data-stu-id="e0ae2-118">Product or service that provided the alert information</span></span> |
| `EntityType` | <span data-ttu-id="e0ae2-119">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-119">string</span></span> | <span data-ttu-id="e0ae2-120">Type d’objet, tel qu’un fichier, un processus, un périphérique ou un utilisateur</span><span class="sxs-lookup"><span data-stu-id="e0ae2-120">Type of object, such as a file, a process, a device, or a user</span></span> |
| `EvidenceRole` | <span data-ttu-id="e0ae2-121">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-121">string</span></span> | <span data-ttu-id="e0ae2-122">La manière dont l’entité est impliquée dans une alerte, indiquant si elle est affectée ou si elle est simplement liée</span><span class="sxs-lookup"><span data-stu-id="e0ae2-122">How the entity is involved in an alert, indicating whether it is impacted or is merely related</span></span> |
| `EvidenceDirection` | <span data-ttu-id="e0ae2-123">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-123">string</span></span> | <span data-ttu-id="e0ae2-124">Indique si l’entité est la source ou la destination d’une connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-124">Indicates whether the entity is the source or the destination of a network connection</span></span> |
| `FileName` | <span data-ttu-id="e0ae2-125">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-125">string</span></span> | <span data-ttu-id="e0ae2-126">Nom du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="e0ae2-126">Name of the file that the recorded action was applied to</span></span> |
| `FolderPath` | <span data-ttu-id="e0ae2-127">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-127">string</span></span> | <span data-ttu-id="e0ae2-128">Dossier contenant le fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="e0ae2-128">Folder containing the file that the recorded action was applied to</span></span> |
| `SHA1` | <span data-ttu-id="e0ae2-129">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-129">string</span></span> | <span data-ttu-id="e0ae2-130">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="e0ae2-130">SHA-1 of the file that the recorded action was applied to</span></span> |
| `SHA256` | <span data-ttu-id="e0ae2-131">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-131">string</span></span> | <span data-ttu-id="e0ae2-132">SHA-256 du fichier auquel l’action enregistrée a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-132">SHA-256 of the file that the recorded action was applied to.</span></span> <span data-ttu-id="e0ae2-133">Ce champ n’est généralement pas rempli : utilisez la colonne SHA1 quand elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-133">This field is usually not populated—use the SHA1 column when available.</span></span> |
| `FileSize` | <span data-ttu-id="e0ae2-134">int</span><span class="sxs-lookup"><span data-stu-id="e0ae2-134">int</span></span> | <span data-ttu-id="e0ae2-135">Taille du fichier en octets</span><span class="sxs-lookup"><span data-stu-id="e0ae2-135">Size of the file in bytes</span></span> |
| `ThreatFamily` | <span data-ttu-id="e0ae2-136">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-136">string</span></span> | <span data-ttu-id="e0ae2-137">Famille de programmes malveillants dans laquelle le fichier ou le processus suspect ou malveillant a été classé sous</span><span class="sxs-lookup"><span data-stu-id="e0ae2-137">Malware family that the suspicious or malicious file or process has been classified under</span></span> |
| `RemoteIP` | <span data-ttu-id="e0ae2-138">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-138">string</span></span> | <span data-ttu-id="e0ae2-139">Adresse IP à laquelle la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="e0ae2-139">IP address that was being connected to</span></span> |
| `RemoteUrl` | <span data-ttu-id="e0ae2-140">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-140">string</span></span> | <span data-ttu-id="e0ae2-141">URL ou nom de domaine complet (FQDN) à laquelle/auquel la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="e0ae2-141">URL or fully qualified domain name (FQDN) that was being connected to</span></span> |
| `AccountName` | <span data-ttu-id="e0ae2-142">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-142">string</span></span> | <span data-ttu-id="e0ae2-143">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="e0ae2-143">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="e0ae2-144">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-144">string</span></span> | <span data-ttu-id="e0ae2-145">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="e0ae2-145">Domain of the account</span></span> |
| `AccountSid` | <span data-ttu-id="e0ae2-146">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-146">string</span></span> | <span data-ttu-id="e0ae2-147">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="e0ae2-147">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="e0ae2-148">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-148">string</span></span> | <span data-ttu-id="e0ae2-149">Identificateur unique du compte dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e0ae2-149">Unique identifier for the account in Azure Active Directory</span></span> |
| `DeviceId` | <span data-ttu-id="e0ae2-150">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-150">string</span></span> | <span data-ttu-id="e0ae2-151">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="e0ae2-151">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="e0ae2-152">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-152">string</span></span> | <span data-ttu-id="e0ae2-153">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="e0ae2-153">Fully qualified domain name (FQDN) of the machine</span></span> |
| `LocalIP` | <span data-ttu-id="e0ae2-154">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-154">string</span></span> | <span data-ttu-id="e0ae2-155">Adresse IP affectée au périphérique local utilisé pendant la communication</span><span class="sxs-lookup"><span data-stu-id="e0ae2-155">IP address assigned to the local device used during communication</span></span> |
| `NetworkMessageId` | <span data-ttu-id="e0ae2-156">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-156">string</span></span> | <span data-ttu-id="e0ae2-157">Identificateur unique d’e-mail, généré par Office 365</span><span class="sxs-lookup"><span data-stu-id="e0ae2-157">Unique identifier for the email, generated by Office 365</span></span> |
| `EmailSubject` | <span data-ttu-id="e0ae2-158">chaîne</span><span class="sxs-lookup"><span data-stu-id="e0ae2-158">string</span></span> | <span data-ttu-id="e0ae2-159">Objet de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="e0ae2-159">Subject of the email</span></span> |
| `ApplicationId` | <span data-ttu-id="e0ae2-160">chaîne</span><span class="sxs-lookup"><span data-stu-id="e0ae2-160">string</span></span> | <span data-ttu-id="e0ae2-161">Identificateur unique de l’application</span><span class="sxs-lookup"><span data-stu-id="e0ae2-161">Unique identifier for the application</span></span> |
| `Application` | <span data-ttu-id="e0ae2-162">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-162">string</span></span> | <span data-ttu-id="e0ae2-163">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="e0ae2-163">Application that performed the recorded action</span></span> |
| `ProcessCommandLine` | <span data-ttu-id="e0ae2-164">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-164">string</span></span> | <span data-ttu-id="e0ae2-165">Ligne de commande utilisée pour créer le nouveau processus</span><span class="sxs-lookup"><span data-stu-id="e0ae2-165">Command line used to create the new process</span></span> |
| `AdditionalFields` | <span data-ttu-id="e0ae2-166">string</span><span class="sxs-lookup"><span data-stu-id="e0ae2-166">string</span></span> | <span data-ttu-id="e0ae2-167">Informations supplémentaires sur l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="e0ae2-167">Additional information about the event in JSON array format</span></span> |

## <a name="related-topics"></a><span data-ttu-id="e0ae2-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0ae2-168">Related topics</span></span>
- [<span data-ttu-id="e0ae2-169">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="e0ae2-169">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="e0ae2-170">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="e0ae2-170">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="e0ae2-171">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="e0ae2-171">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="e0ae2-172">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="e0ae2-172">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="e0ae2-173">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="e0ae2-173">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="e0ae2-174">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="e0ae2-174">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
