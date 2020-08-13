---
title: Table AlertEvidence dans le schéma de chasse avancé
description: Découvrez les informations relatives aux fichiers, aux adresses réseau, aux utilisateurs ou aux appareils associés à des alertes générées dans la table AlertEvidence du schéma de chasse avancé.
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
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 8fc713db33b0e40adcd0975d26c10daece636ab1
ms.sourcegitcommit: 51097b18d94da20aa727ebfbeb6ec84c263b25c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/12/2020
ms.locfileid: "46649510"
---
# <a name="alertevidence"></a><span data-ttu-id="d595a-104">AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="d595a-104">AlertEvidence</span></span>

<span data-ttu-id="d595a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d595a-105">**Applies to:**</span></span>
- <span data-ttu-id="d595a-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="d595a-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="d595a-107">Le `AlertEvidence` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les différentes entités (fichiers, adresses IP, URL, utilisateurs ou périphériques) associées aux alertes de Microsoft Defender atp, Office 365 ATP, Microsoft Cloud App Security et Azure ATP.</span><span class="sxs-lookup"><span data-stu-id="d595a-107">The `AlertEvidence` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about various entities — files, IP addresses, URLs, users, or devices — associated with alerts from Microsoft Defender ATP, Office 365 ATP, Microsoft Cloud App Security, and Azure ATP.</span></span> <span data-ttu-id="d595a-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="d595a-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="d595a-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d595a-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="d595a-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="d595a-110">Column name</span></span> | <span data-ttu-id="d595a-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="d595a-111">Data type</span></span> | <span data-ttu-id="d595a-112">Description</span><span class="sxs-lookup"><span data-stu-id="d595a-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="d595a-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="d595a-113">datetime</span></span> | <span data-ttu-id="d595a-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="d595a-114">Date and time when the event was recorded</span></span> |
| `AlertId` | <span data-ttu-id="d595a-115">string</span><span class="sxs-lookup"><span data-stu-id="d595a-115">string</span></span> | <span data-ttu-id="d595a-116">Identificateur unique de l’alerte</span><span class="sxs-lookup"><span data-stu-id="d595a-116">Unique identifier for the alert</span></span> |
| `EntityType` | <span data-ttu-id="d595a-117">string</span><span class="sxs-lookup"><span data-stu-id="d595a-117">string</span></span> | <span data-ttu-id="d595a-118">Type d’objet, tel qu’un fichier, un processus, un périphérique ou un utilisateur</span><span class="sxs-lookup"><span data-stu-id="d595a-118">Type of object, such as a file, a process, a device, or a user</span></span> |
| `EvidenceRole` | <span data-ttu-id="d595a-119">string</span><span class="sxs-lookup"><span data-stu-id="d595a-119">string</span></span> | <span data-ttu-id="d595a-120">La manière dont l’entité est impliquée dans une alerte, indiquant si elle est affectée ou si elle est simplement liée</span><span class="sxs-lookup"><span data-stu-id="d595a-120">How the entity is involved in an alert, indicating whether it is impacted or is merely related</span></span> |
| `SHA1` | <span data-ttu-id="d595a-121">string</span><span class="sxs-lookup"><span data-stu-id="d595a-121">string</span></span> | <span data-ttu-id="d595a-122">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="d595a-122">SHA-1 of the file that the recorded action was applied to</span></span> |
| `SHA256` | <span data-ttu-id="d595a-123">string</span><span class="sxs-lookup"><span data-stu-id="d595a-123">string</span></span> | <span data-ttu-id="d595a-124">SHA-256 du fichier auquel l’action enregistrée a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="d595a-124">SHA-256 of the file that the recorded action was applied to.</span></span> <span data-ttu-id="d595a-125">Ce champ n’est généralement pas rempli. Utilisez la colonne SHA1 lorsque celle-ci est disponible.</span><span class="sxs-lookup"><span data-stu-id="d595a-125">This field is usually not populated — use the SHA1 column when available.</span></span> |
| `RemoteIP` | <span data-ttu-id="d595a-126">string</span><span class="sxs-lookup"><span data-stu-id="d595a-126">string</span></span> | <span data-ttu-id="d595a-127">Adresse IP à laquelle la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="d595a-127">IP address that was being connected to</span></span> |
| `RemoteUrl` | <span data-ttu-id="d595a-128">string</span><span class="sxs-lookup"><span data-stu-id="d595a-128">string</span></span> | <span data-ttu-id="d595a-129">URL ou nom de domaine complet (FQDN) à laquelle/auquel la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="d595a-129">URL or fully qualified domain name (FQDN) that was being connected to</span></span> |
| `AccountName` | <span data-ttu-id="d595a-130">string</span><span class="sxs-lookup"><span data-stu-id="d595a-130">string</span></span> | <span data-ttu-id="d595a-131">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="d595a-131">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="d595a-132">string</span><span class="sxs-lookup"><span data-stu-id="d595a-132">string</span></span> | <span data-ttu-id="d595a-133">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="d595a-133">Domain of the account</span></span> |
| `AccountSid` | <span data-ttu-id="d595a-134">string</span><span class="sxs-lookup"><span data-stu-id="d595a-134">string</span></span> | <span data-ttu-id="d595a-135">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="d595a-135">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="d595a-136">string</span><span class="sxs-lookup"><span data-stu-id="d595a-136">string</span></span> | <span data-ttu-id="d595a-137">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="d595a-137">Unique identifier for the account in Azure AD</span></span> |
| `DeviceId` | <span data-ttu-id="d595a-138">string</span><span class="sxs-lookup"><span data-stu-id="d595a-138">string</span></span> | <span data-ttu-id="d595a-139">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="d595a-139">Unique identifier for the machine in the service</span></span> |
| `ThreatFamily` | <span data-ttu-id="d595a-140">string</span><span class="sxs-lookup"><span data-stu-id="d595a-140">string</span></span> | <span data-ttu-id="d595a-141">Famille de programmes malveillants dans laquelle le fichier ou le processus suspect ou malveillant a été classé sous</span><span class="sxs-lookup"><span data-stu-id="d595a-141">Malware family that the suspicious or malicious file or process has been classified under</span></span> |
| `EvidenceDirection` | <span data-ttu-id="d595a-142">string</span><span class="sxs-lookup"><span data-stu-id="d595a-142">string</span></span> | <span data-ttu-id="d595a-143">Indique si l’entité est la source ou la destination d’une connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="d595a-143">Indicates whether the entity is the source or the destination of a network connection</span></span> |
| `AdditionalFields` | <span data-ttu-id="d595a-144">string</span><span class="sxs-lookup"><span data-stu-id="d595a-144">string</span></span> | <span data-ttu-id="d595a-145">Informations supplémentaires sur l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="d595a-145">Additional information about the event in JSON array format</span></span> |

## <a name="related-topics"></a><span data-ttu-id="d595a-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d595a-146">Related topics</span></span>
- [<span data-ttu-id="d595a-147">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="d595a-147">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="d595a-148">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="d595a-148">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="d595a-149">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="d595a-149">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="d595a-150">Recherche sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="d595a-150">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="d595a-151">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="d595a-151">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="d595a-152">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="d595a-152">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
