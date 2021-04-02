---
title: Fonction FileProfile() dans le recherche avancée pour Microsoft 365 Defender
description: Découvrez comment utiliser FileProfile() pour enrichir des informations sur les fichiers dans vos résultats de requête de recherche avancée
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, FileProfile, file profile, function, enrichment
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
ms.openlocfilehash: ea4f22b70e607b42155342dde1ac16b1ad640981
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51498446"
---
# <a name="fileprofile"></a><span data-ttu-id="570d1-104">FileProfile()</span><span class="sxs-lookup"><span data-stu-id="570d1-104">FileProfile()</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="570d1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="570d1-105">**Applies to:**</span></span>
- <span data-ttu-id="570d1-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="570d1-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="570d1-107">La fonction est une fonction d’enrichissement dans le recherche avancée qui ajoute les données suivantes `FileProfile()` aux fichiers trouvés par la requête. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="570d1-107">The `FileProfile()` function is an enrichment function in [advanced hunting](advanced-hunting-overview.md) that adds the following data to files found by the query.</span></span>

| <span data-ttu-id="570d1-108">Column</span><span class="sxs-lookup"><span data-stu-id="570d1-108">Column</span></span> | <span data-ttu-id="570d1-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="570d1-109">Data type</span></span> | <span data-ttu-id="570d1-110">Description</span><span class="sxs-lookup"><span data-stu-id="570d1-110">Description</span></span> |
|------------|---------------|-------------|
| `SHA1` | <span data-ttu-id="570d1-111">string</span><span class="sxs-lookup"><span data-stu-id="570d1-111">string</span></span> | <span data-ttu-id="570d1-112">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="570d1-112">SHA-1 of the file that the recorded action was applied to</span></span> |
| `SHA256` | <span data-ttu-id="570d1-113">string</span><span class="sxs-lookup"><span data-stu-id="570d1-113">string</span></span> | <span data-ttu-id="570d1-114">SHA-256 du fichier à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="570d1-114">SHA-256 of the file that the recorded action was applied to</span></span> |
| `MD5` | <span data-ttu-id="570d1-115">string</span><span class="sxs-lookup"><span data-stu-id="570d1-115">string</span></span> | <span data-ttu-id="570d1-116">Hachage MD5 du fichier à l’application de l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="570d1-116">MD5 hash of the file that the recorded action was applied to</span></span> |
| `FileSize` | <span data-ttu-id="570d1-117">entier</span><span class="sxs-lookup"><span data-stu-id="570d1-117">int</span></span> | <span data-ttu-id="570d1-118">Taille du fichier en octets</span><span class="sxs-lookup"><span data-stu-id="570d1-118">Size of the file in bytes</span></span> |
| `GlobalPrevalence` | <span data-ttu-id="570d1-119">entier</span><span class="sxs-lookup"><span data-stu-id="570d1-119">int</span></span> | <span data-ttu-id="570d1-120">Nombre d’instances de l’entité observées globalement par Microsoft</span><span class="sxs-lookup"><span data-stu-id="570d1-120">Number of instances of the entity observed by Microsoft globally</span></span> |
| `GlobalFirstSeen` | <span data-ttu-id="570d1-121">DateHeure</span><span class="sxs-lookup"><span data-stu-id="570d1-121">datetime</span></span> | <span data-ttu-id="570d1-122">Date et heure à laquelle l’entité a été observée pour la première fois par Microsoft globalement</span><span class="sxs-lookup"><span data-stu-id="570d1-122">Date and time when the entity was first observed by Microsoft globally</span></span> |
| `GlobalLastSeen` | <span data-ttu-id="570d1-123">DateHeure</span><span class="sxs-lookup"><span data-stu-id="570d1-123">datetime</span></span> | <span data-ttu-id="570d1-124">Date et heure de la dernière observation de l’entité par Microsoft au niveau global</span><span class="sxs-lookup"><span data-stu-id="570d1-124">Date and time when the entity was last observed by Microsoft globally</span></span> |
| `Signer` | <span data-ttu-id="570d1-125">string</span><span class="sxs-lookup"><span data-stu-id="570d1-125">string</span></span> | <span data-ttu-id="570d1-126">Informations sur le signataire du fichier</span><span class="sxs-lookup"><span data-stu-id="570d1-126">Information about the signer of the file</span></span> |
| `Issuer` | <span data-ttu-id="570d1-127">string</span><span class="sxs-lookup"><span data-stu-id="570d1-127">string</span></span> | <span data-ttu-id="570d1-128">Informations sur l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="570d1-128">Information about the issuing certificate authority (CA)</span></span> |
| `SignerHash` | <span data-ttu-id="570d1-129">string</span><span class="sxs-lookup"><span data-stu-id="570d1-129">string</span></span> | <span data-ttu-id="570d1-130">Valeur de hachage unique identifiant le signataire</span><span class="sxs-lookup"><span data-stu-id="570d1-130">Unique hash value identifying the signer</span></span> |
| `IsCertificateValid` | <span data-ttu-id="570d1-131">booléen</span><span class="sxs-lookup"><span data-stu-id="570d1-131">boolean</span></span> | <span data-ttu-id="570d1-132">Si le certificat utilisé pour signer le fichier est valide</span><span class="sxs-lookup"><span data-stu-id="570d1-132">Whether the certificate used to sign the file is valid</span></span> |
| `IsRootSignerMicrosoft` | <span data-ttu-id="570d1-133">booléen</span><span class="sxs-lookup"><span data-stu-id="570d1-133">boolean</span></span> | <span data-ttu-id="570d1-134">Indique si le signataire du certificat racine est Microsoft</span><span class="sxs-lookup"><span data-stu-id="570d1-134">Indicates whether the signer of the root certificate is Microsoft</span></span> |
| `SignatureState` | <span data-ttu-id="570d1-135">string</span><span class="sxs-lookup"><span data-stu-id="570d1-135">string</span></span> | <span data-ttu-id="570d1-136">État de la signature du fichier : SignedValid - le fichier est signé avec une signature valide, SignedInvalid - le fichier est signé mais le certificat n’est pas valide, Non signé - le fichier n’est pas signé, Inconnu - les informations sur le fichier ne peuvent pas être récupérées</span><span class="sxs-lookup"><span data-stu-id="570d1-136">State of the file signature: SignedValid - the file is signed with a valid signature, SignedInvalid - the file is signed but the certificate is invalid, Unsigned - the file is not signed, Unknown - information about the file cannot be retrieved</span></span>
| `IsExecutable` | <span data-ttu-id="570d1-137">booléen</span><span class="sxs-lookup"><span data-stu-id="570d1-137">boolean</span></span> | <span data-ttu-id="570d1-138">Si le fichier est un fichier PE (Portable Executable)</span><span class="sxs-lookup"><span data-stu-id="570d1-138">Whether the file is a Portable Executable (PE) file</span></span> |
| `ThreatName` | <span data-ttu-id="570d1-139">string</span><span class="sxs-lookup"><span data-stu-id="570d1-139">string</span></span> | <span data-ttu-id="570d1-140">Nom de détection des programmes malveillants ou autres menaces détectés</span><span class="sxs-lookup"><span data-stu-id="570d1-140">Detection name for any malware or other threats found</span></span> |
| `Publisher` | <span data-ttu-id="570d1-141">string</span><span class="sxs-lookup"><span data-stu-id="570d1-141">string</span></span> | <span data-ttu-id="570d1-142">Nom de l’organisation qui a publié le fichier</span><span class="sxs-lookup"><span data-stu-id="570d1-142">Name of the organization that published the file</span></span> |
| `SoftwareName` | <span data-ttu-id="570d1-143">string</span><span class="sxs-lookup"><span data-stu-id="570d1-143">string</span></span> | <span data-ttu-id="570d1-144">Nom du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="570d1-144">Name of the software product</span></span> |

## <a name="syntax"></a><span data-ttu-id="570d1-145">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="570d1-145">Syntax</span></span>

```kusto
invoke FileProfile(x,y)
```

## <a name="arguments"></a><span data-ttu-id="570d1-146">Arguments</span><span class="sxs-lookup"><span data-stu-id="570d1-146">Arguments</span></span>

- <span data-ttu-id="570d1-147">**x**— colonne d’ID de fichier à utiliser : `SHA1` , , ou ; fonction utilise si non `SHA256` `InitiatingProcessSHA1` `InitiatingProcessSHA256` `SHA1` spécifié</span><span class="sxs-lookup"><span data-stu-id="570d1-147">**x**—file ID column to use: `SHA1`, `SHA256`, `InitiatingProcessSHA1`, or `InitiatingProcessSHA256`; function uses `SHA1` if unspecified</span></span>
- <span data-ttu-id="570d1-148">**y**— limite au nombre d’enregistrements à enrichir, de 1 à 1 000 ; utilise 100 si non spécifié</span><span class="sxs-lookup"><span data-stu-id="570d1-148">**y**—limit to the number of records to enrich, 1-1000; function uses 100 if unspecified</span></span>


>[!TIP]
> <span data-ttu-id="570d1-149">Les fonctions d’enrichissement afficheront des informations supplémentaires uniquement lorsqu’elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="570d1-149">Enrichment functions will show supplemental information only when they are available.</span></span> <span data-ttu-id="570d1-150">La disponibilité des informations varie et dépend d’un grand nombre de facteurs.</span><span class="sxs-lookup"><span data-stu-id="570d1-150">Availability of information is varied and depends on a lot of factors.</span></span> <span data-ttu-id="570d1-151">Veillez à prendre cela en compte lors de l’utilisation de FileProfile() dans vos requêtes ou lors de la création de détections personnalisées.</span><span class="sxs-lookup"><span data-stu-id="570d1-151">Make sure to consider this when using FileProfile() in your queries or in creating custom detections.</span></span> <span data-ttu-id="570d1-152">Pour obtenir de meilleurs résultats, nous vous recommandons d’utiliser la fonction FileProfile() avec SHA1.</span><span class="sxs-lookup"><span data-stu-id="570d1-152">For best results, we recommend using the FileProfile() function with SHA1.</span></span>

## <a name="examples"></a><span data-ttu-id="570d1-153">Exemples</span><span class="sxs-lookup"><span data-stu-id="570d1-153">Examples</span></span>

### <a name="project-only-the-sha1-column-and-enrich-it"></a><span data-ttu-id="570d1-154">Projeter uniquement la colonne SHA1 et l’enrichir</span><span class="sxs-lookup"><span data-stu-id="570d1-154">Project only the SHA1 column and enrich it</span></span>

```kusto
DeviceFileEvents
| where isnotempty(SHA1) and Timestamp > ago(1d)
| take 10
| project SHA1
| invoke FileProfile()
```

### <a name="enrich-the-first-500-records-and-list-low-prevalence-files"></a><span data-ttu-id="570d1-155">Enrichir les 500 premiers enregistrements et lister les fichiers de faible prévalence</span><span class="sxs-lookup"><span data-stu-id="570d1-155">Enrich the first 500 records and list low-prevalence files</span></span>

```kusto
DeviceFileEvents
| where ActionType == "FileCreated" and Timestamp > ago(1d)
| project CreatedOn = Timestamp, FileName, FolderPath, SHA1
| invoke FileProfile("SHA1", 500) 
| where GlobalPrevalence < 15
```

## <a name="related-topics"></a><span data-ttu-id="570d1-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="570d1-156">Related topics</span></span>
- [<span data-ttu-id="570d1-157">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="570d1-157">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="570d1-158">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="570d1-158">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="570d1-159">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="570d1-159">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="570d1-160">Obtenir d’autres exemples de requête</span><span class="sxs-lookup"><span data-stu-id="570d1-160">Get more query examples</span></span>](advanced-hunting-shared-queries.md)
