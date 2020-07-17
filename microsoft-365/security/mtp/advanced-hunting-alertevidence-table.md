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
ms.openlocfilehash: a0f2ae36752a4415da7c1bc39ce35bd7f744a764
ms.sourcegitcommit: ab10c042e5e9c6a7b2afef930ab0d247a6aa275d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "44899350"
---
# <a name="alertevidence"></a><span data-ttu-id="ec260-104">AlertEvidence</span><span class="sxs-lookup"><span data-stu-id="ec260-104">AlertEvidence</span></span>

<span data-ttu-id="ec260-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ec260-105">**Applies to:**</span></span>
- <span data-ttu-id="ec260-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ec260-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="ec260-107">Le `AlertEvidence` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les différentes entités (fichiers, adresses IP, URL, utilisateurs ou périphériques) associées aux alertes de Microsoft Defender atp, Office 365 ATP, Microsoft Cloud App Security et Azure ATP.</span><span class="sxs-lookup"><span data-stu-id="ec260-107">The `AlertEvidence` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about various entities — files, IP addresses, URLs, users, or devices — associated with alerts from Microsoft Defender ATP, Office 365 ATP, Microsoft Cloud App Security, and Azure ATP.</span></span> <span data-ttu-id="ec260-108">Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.</span><span class="sxs-lookup"><span data-stu-id="ec260-108">Use this reference to construct queries that return information from this table.</span></span>

<span data-ttu-id="ec260-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ec260-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="ec260-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="ec260-110">Column name</span></span> | <span data-ttu-id="ec260-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="ec260-111">Data type</span></span> | <span data-ttu-id="ec260-112">Description</span><span class="sxs-lookup"><span data-stu-id="ec260-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="ec260-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="ec260-113">datetime</span></span> | <span data-ttu-id="ec260-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="ec260-114">Date and time when the event was recorded</span></span> |
| `AlertId` | <span data-ttu-id="ec260-115">chaîne</span><span class="sxs-lookup"><span data-stu-id="ec260-115">string</span></span> | <span data-ttu-id="ec260-116">Identificateur unique de l’alerte</span><span class="sxs-lookup"><span data-stu-id="ec260-116">Unique identifier for the alert</span></span> |
| `EntityType` | <span data-ttu-id="ec260-117">string</span><span class="sxs-lookup"><span data-stu-id="ec260-117">string</span></span> | <span data-ttu-id="ec260-118">Type d’objet, tel qu’un fichier, un processus, un périphérique ou un utilisateur</span><span class="sxs-lookup"><span data-stu-id="ec260-118">Type of object, such as a file, a process, a device, or a user</span></span> |
| `EvidenceRole` | <span data-ttu-id="ec260-119">string</span><span class="sxs-lookup"><span data-stu-id="ec260-119">string</span></span> | <span data-ttu-id="ec260-120">La manière dont l’entité est impliquée dans une alerte, indiquant si elle est affectée ou si elle est simplement liée</span><span class="sxs-lookup"><span data-stu-id="ec260-120">How the entity is involved in an alert, indicating whether it is impacted or is merely related</span></span> |
| `SHA1` | <span data-ttu-id="ec260-121">string</span><span class="sxs-lookup"><span data-stu-id="ec260-121">string</span></span> | <span data-ttu-id="ec260-122">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="ec260-122">SHA-1 of the file that the recorded action was applied to</span></span> |
| `SHA256` | <span data-ttu-id="ec260-123">string</span><span class="sxs-lookup"><span data-stu-id="ec260-123">string</span></span> | <span data-ttu-id="ec260-124">SHA-256 du fichier auquel l’action enregistrée a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="ec260-124">SHA-256 of the file that the recorded action was applied to.</span></span> <span data-ttu-id="ec260-125">Ce champ n’est généralement pas rempli. Utilisez la colonne SHA1 lorsque celle-ci est disponible.</span><span class="sxs-lookup"><span data-stu-id="ec260-125">This field is usually not populated — use the SHA1 column when available.</span></span> |
| `RemoteIP` | <span data-ttu-id="ec260-126">string</span><span class="sxs-lookup"><span data-stu-id="ec260-126">string</span></span> | <span data-ttu-id="ec260-127">Adresse IP à laquelle la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="ec260-127">IP address that was being connected to</span></span> |
| `RemoteUrl` | <span data-ttu-id="ec260-128">string</span><span class="sxs-lookup"><span data-stu-id="ec260-128">string</span></span> | <span data-ttu-id="ec260-129">URL ou nom de domaine complet (FQDN) à laquelle/auquel la connexion était en cours</span><span class="sxs-lookup"><span data-stu-id="ec260-129">URL or fully qualified domain name (FQDN) that was being connected to</span></span> |
| `AccountName` | <span data-ttu-id="ec260-130">string</span><span class="sxs-lookup"><span data-stu-id="ec260-130">string</span></span> | <span data-ttu-id="ec260-131">Nom d’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="ec260-131">User name of the account</span></span> |
| `AccountDomain` | <span data-ttu-id="ec260-132">string</span><span class="sxs-lookup"><span data-stu-id="ec260-132">string</span></span> | <span data-ttu-id="ec260-133">Domaine du compte</span><span class="sxs-lookup"><span data-stu-id="ec260-133">Domain of the account</span></span> |
| `AccountSid` | <span data-ttu-id="ec260-134">string</span><span class="sxs-lookup"><span data-stu-id="ec260-134">string</span></span> | <span data-ttu-id="ec260-135">Identificateur de sécurité (SID) du compte</span><span class="sxs-lookup"><span data-stu-id="ec260-135">Security Identifier (SID) of the account</span></span> |
| `AccountObjectId` | <span data-ttu-id="ec260-136">string</span><span class="sxs-lookup"><span data-stu-id="ec260-136">string</span></span> | <span data-ttu-id="ec260-137">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="ec260-137">Unique identifier for the account in Azure AD</span></span> |
| `DeviceId` | <span data-ttu-id="ec260-138">string</span><span class="sxs-lookup"><span data-stu-id="ec260-138">string</span></span> | <span data-ttu-id="ec260-139">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="ec260-139">Unique identifier for the machine in the service</span></span> |
| `ThreatFamily` | <span data-ttu-id="ec260-140">string</span><span class="sxs-lookup"><span data-stu-id="ec260-140">string</span></span> | <span data-ttu-id="ec260-141">Famille de programmes malveillants dans laquelle le fichier ou le processus suspect ou malveillant a été classé sous</span><span class="sxs-lookup"><span data-stu-id="ec260-141">Malware family that the suspicious or malicious file or process has been classified under</span></span> |
| `EvidenceDirection` | <span data-ttu-id="ec260-142">string</span><span class="sxs-lookup"><span data-stu-id="ec260-142">string</span></span> | <span data-ttu-id="ec260-143">Indique si l’entité est la source ou la destination d’une connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="ec260-143">Indicates whether the entity is the source or the destination of a network connection</span></span> |
| `AdditionalFields` | <span data-ttu-id="ec260-144">string</span><span class="sxs-lookup"><span data-stu-id="ec260-144">string</span></span> | <span data-ttu-id="ec260-145">Informations supplémentaires sur l’événement au format de tableau JSON</span><span class="sxs-lookup"><span data-stu-id="ec260-145">Additional information about the event in JSON array format</span></span> |

## <a name="related-topics"></a><span data-ttu-id="ec260-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec260-146">Related topics</span></span>
- [<span data-ttu-id="ec260-147">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="ec260-147">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="ec260-148">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="ec260-148">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="ec260-149">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="ec260-149">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="ec260-150">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="ec260-150">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="ec260-151">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="ec260-151">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="ec260-152">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="ec260-152">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
