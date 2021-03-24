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
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: e511c12240512af772b3552f63ad9ed98ff105af
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062081"
---
# <a name="fileprofile"></a><span data-ttu-id="72f30-104">FileProfile()</span><span class="sxs-lookup"><span data-stu-id="72f30-104">FileProfile()</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="72f30-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="72f30-105">**Applies to:**</span></span>
- <span data-ttu-id="72f30-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="72f30-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="72f30-107">La fonction est une fonction d’enrichissement dans le recherche avancée qui ajoute les données suivantes aux `FileProfile()` fichiers trouvés par la requête. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="72f30-107">The `FileProfile()` function is an enrichment function in [advanced hunting](advanced-hunting-overview.md) that adds the following data to files found by the query.</span></span>

| <span data-ttu-id="72f30-108">Column</span><span class="sxs-lookup"><span data-stu-id="72f30-108">Column</span></span> | <span data-ttu-id="72f30-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="72f30-109">Data type</span></span> | <span data-ttu-id="72f30-110">Description</span><span class="sxs-lookup"><span data-stu-id="72f30-110">Description</span></span> |
|------------|-------------|-------------|
| <span data-ttu-id="72f30-111">SHA1</span><span class="sxs-lookup"><span data-stu-id="72f30-111">SHA1</span></span> | <span data-ttu-id="72f30-112">string</span><span class="sxs-lookup"><span data-stu-id="72f30-112">string</span></span> | <span data-ttu-id="72f30-113">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="72f30-113">SHA-1 of the file that the recorded action was applied to</span></span> |
| <span data-ttu-id="72f30-114">SHA256</span><span class="sxs-lookup"><span data-stu-id="72f30-114">SHA256</span></span> | <span data-ttu-id="72f30-115">string</span><span class="sxs-lookup"><span data-stu-id="72f30-115">string</span></span> | <span data-ttu-id="72f30-116">SHA-256 du fichier à qui l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="72f30-116">SHA-256 of the file that the recorded action was applied to</span></span> |
| <span data-ttu-id="72f30-117">MD5</span><span class="sxs-lookup"><span data-stu-id="72f30-117">MD5</span></span> | <span data-ttu-id="72f30-118">string</span><span class="sxs-lookup"><span data-stu-id="72f30-118">string</span></span> | <span data-ttu-id="72f30-119">Hachage MD5 du fichier à l’application de l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="72f30-119">MD5 hash of the file that the recorded action was applied to</span></span> |
| <span data-ttu-id="72f30-120">FileSize</span><span class="sxs-lookup"><span data-stu-id="72f30-120">FileSize</span></span> | <span data-ttu-id="72f30-121">entier</span><span class="sxs-lookup"><span data-stu-id="72f30-121">int</span></span> | <span data-ttu-id="72f30-122">Taille du fichier en octets</span><span class="sxs-lookup"><span data-stu-id="72f30-122">Size of the file in bytes</span></span> |
| <span data-ttu-id="72f30-123">GlobalPrevalence</span><span class="sxs-lookup"><span data-stu-id="72f30-123">GlobalPrevalence</span></span> | <span data-ttu-id="72f30-124">entier</span><span class="sxs-lookup"><span data-stu-id="72f30-124">int</span></span> | <span data-ttu-id="72f30-125">Nombre d’instances de l’entité observées globalement par Microsoft</span><span class="sxs-lookup"><span data-stu-id="72f30-125">Number of instances of the entity observed by Microsoft globally</span></span> |
| <span data-ttu-id="72f30-126">GlobalFirstSeen</span><span class="sxs-lookup"><span data-stu-id="72f30-126">GlobalFirstSeen</span></span> | <span data-ttu-id="72f30-127">DateHeure</span><span class="sxs-lookup"><span data-stu-id="72f30-127">datetime</span></span> | <span data-ttu-id="72f30-128">Date et heure à laquelle l’entité a été observée pour la première fois par Microsoft globalement</span><span class="sxs-lookup"><span data-stu-id="72f30-128">Date and time when the entity was first observed by Microsoft globally</span></span> |
| <span data-ttu-id="72f30-129">GlobalLastSeen</span><span class="sxs-lookup"><span data-stu-id="72f30-129">GlobalLastSeen</span></span> | <span data-ttu-id="72f30-130">DateHeure</span><span class="sxs-lookup"><span data-stu-id="72f30-130">datetime</span></span> | <span data-ttu-id="72f30-131">Date et heure de la dernière observation de l’entité par Microsoft au niveau global</span><span class="sxs-lookup"><span data-stu-id="72f30-131">Date and time when the entity was last observed by Microsoft globally</span></span> |
| <span data-ttu-id="72f30-132">Signataire</span><span class="sxs-lookup"><span data-stu-id="72f30-132">Signer</span></span> | <span data-ttu-id="72f30-133">string</span><span class="sxs-lookup"><span data-stu-id="72f30-133">string</span></span> | <span data-ttu-id="72f30-134">Informations sur le signataire du fichier</span><span class="sxs-lookup"><span data-stu-id="72f30-134">Information about the signer of the file</span></span> |
| <span data-ttu-id="72f30-135">Issuer</span><span class="sxs-lookup"><span data-stu-id="72f30-135">Issuer</span></span> | <span data-ttu-id="72f30-136">string</span><span class="sxs-lookup"><span data-stu-id="72f30-136">string</span></span> | <span data-ttu-id="72f30-137">Informations sur l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="72f30-137">Information about the issuing certificate authority (CA)</span></span> |
| <span data-ttu-id="72f30-138">SignerHash</span><span class="sxs-lookup"><span data-stu-id="72f30-138">SignerHash</span></span> | <span data-ttu-id="72f30-139">string</span><span class="sxs-lookup"><span data-stu-id="72f30-139">string</span></span> | <span data-ttu-id="72f30-140">Valeur de hachage unique identifiant le signataire</span><span class="sxs-lookup"><span data-stu-id="72f30-140">Unique hash value identifying the signer</span></span> |
| <span data-ttu-id="72f30-141">IsCertificateValid</span><span class="sxs-lookup"><span data-stu-id="72f30-141">IsCertificateValid</span></span> | <span data-ttu-id="72f30-142">booléen</span><span class="sxs-lookup"><span data-stu-id="72f30-142">boolean</span></span> | <span data-ttu-id="72f30-143">Si le certificat utilisé pour signer le fichier est valide</span><span class="sxs-lookup"><span data-stu-id="72f30-143">Whether the certificate used to sign the file is valid</span></span> |
| <span data-ttu-id="72f30-144">IsRootSignerMicrosoft</span><span class="sxs-lookup"><span data-stu-id="72f30-144">IsRootSignerMicrosoft</span></span> | <span data-ttu-id="72f30-145">booléen</span><span class="sxs-lookup"><span data-stu-id="72f30-145">boolean</span></span> | <span data-ttu-id="72f30-146">Indique si le signataire du certificat racine est Microsoft</span><span class="sxs-lookup"><span data-stu-id="72f30-146">Indicates whether the signer of the root certificate is Microsoft</span></span> |
| <span data-ttu-id="72f30-147">IsExecutable</span><span class="sxs-lookup"><span data-stu-id="72f30-147">IsExecutable</span></span> | <span data-ttu-id="72f30-148">booléen</span><span class="sxs-lookup"><span data-stu-id="72f30-148">boolean</span></span> | <span data-ttu-id="72f30-149">Si le fichier est un fichier Exécutable portable (PE)</span><span class="sxs-lookup"><span data-stu-id="72f30-149">Whether the file is a Portable Executable (PE) file</span></span> |
| <span data-ttu-id="72f30-150">ThreatName</span><span class="sxs-lookup"><span data-stu-id="72f30-150">ThreatName</span></span> | <span data-ttu-id="72f30-151">string</span><span class="sxs-lookup"><span data-stu-id="72f30-151">string</span></span> | <span data-ttu-id="72f30-152">Nom de détection des programmes malveillants ou autres menaces détectés</span><span class="sxs-lookup"><span data-stu-id="72f30-152">Detection name for any malware or other threats found</span></span> |
| <span data-ttu-id="72f30-153">Éditeur</span><span class="sxs-lookup"><span data-stu-id="72f30-153">Publisher</span></span> | <span data-ttu-id="72f30-154">string</span><span class="sxs-lookup"><span data-stu-id="72f30-154">string</span></span> | <span data-ttu-id="72f30-155">Nom de l’organisation qui a publié le fichier</span><span class="sxs-lookup"><span data-stu-id="72f30-155">Name of the organization that published the file</span></span> |
| <span data-ttu-id="72f30-156">SoftwareName</span><span class="sxs-lookup"><span data-stu-id="72f30-156">SoftwareName</span></span> | <span data-ttu-id="72f30-157">string</span><span class="sxs-lookup"><span data-stu-id="72f30-157">string</span></span> | <span data-ttu-id="72f30-158">Nom du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="72f30-158">Name of the software product</span></span> |

## <a name="syntax"></a><span data-ttu-id="72f30-159">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72f30-159">Syntax</span></span>

```kusto
invoke FileProfile(x,y)
```

## <a name="arguments"></a><span data-ttu-id="72f30-160">Arguments</span><span class="sxs-lookup"><span data-stu-id="72f30-160">Arguments</span></span>

- <span data-ttu-id="72f30-161">**x**— colonne d’ID de fichier à utiliser : `SHA1` , , ou ; fonction utilise si non `SHA256` `InitiatingProcessSHA1` `InitiatingProcessSHA256` `SHA1` spécifié</span><span class="sxs-lookup"><span data-stu-id="72f30-161">**x**—file ID column to use: `SHA1`, `SHA256`, `InitiatingProcessSHA1`, or `InitiatingProcessSHA256`; function uses `SHA1` if unspecified</span></span>
- <span data-ttu-id="72f30-162">**y**— limite au nombre d’enregistrements à enrichir, de 1 à 1 000 ; utilise 100 si non spécifié</span><span class="sxs-lookup"><span data-stu-id="72f30-162">**y**—limit to the number of records to enrich, 1-1000; function uses 100 if unspecified</span></span>


>[!TIP]
> <span data-ttu-id="72f30-163">Les fonctions d’enrichissement afficheront des informations supplémentaires uniquement lorsqu’elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="72f30-163">Enrichment functions will show supplemental information only when they are available.</span></span> <span data-ttu-id="72f30-164">La disponibilité des informations varie et dépend d’un grand nombre de facteurs.</span><span class="sxs-lookup"><span data-stu-id="72f30-164">Availability of information is varied and depends on a lot of factors.</span></span> <span data-ttu-id="72f30-165">Veillez à prendre cela en compte lors de l’utilisation de FileProfile() dans vos requêtes ou lors de la création de détections personnalisées.</span><span class="sxs-lookup"><span data-stu-id="72f30-165">Make sure to consider this when using FileProfile() in your queries or in creating custom detections.</span></span> <span data-ttu-id="72f30-166">Pour de meilleurs résultats, nous vous recommandons d’utiliser la fonction FileProfile() avec SHA1.</span><span class="sxs-lookup"><span data-stu-id="72f30-166">For best results, we recommend using the FileProfile() function with SHA1.</span></span>

## <a name="examples"></a><span data-ttu-id="72f30-167">Exemples</span><span class="sxs-lookup"><span data-stu-id="72f30-167">Examples</span></span>

### <a name="project-only-the-sha1-column-and-enrich-it"></a><span data-ttu-id="72f30-168">Projeter uniquement la colonne SHA1 et l’enrichir</span><span class="sxs-lookup"><span data-stu-id="72f30-168">Project only the SHA1 column and enrich it</span></span>

```kusto
DeviceFileEvents
| where isnotempty(SHA1) and Timestamp > ago(1d)
| take 10
| project SHA1
| invoke FileProfile()
```

### <a name="enrich-the-first-500-records-and-list-low-prevalence-files"></a><span data-ttu-id="72f30-169">Enrichir les 500 premiers enregistrements et lister les fichiers à faible prévalence</span><span class="sxs-lookup"><span data-stu-id="72f30-169">Enrich the first 500 records and list low-prevalence files</span></span>

```kusto
DeviceFileEvents
| where ActionType == "FileCreated" and Timestamp > ago(1d)
| project CreatedOn = Timestamp, FileName, FolderPath, SHA1
| invoke FileProfile("SHA1", 500) 
| where GlobalPrevalence < 15
```

## <a name="related-topics"></a><span data-ttu-id="72f30-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72f30-170">Related topics</span></span>
- [<span data-ttu-id="72f30-171">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="72f30-171">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="72f30-172">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="72f30-172">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="72f30-173">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="72f30-173">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="72f30-174">Obtenir d’autres exemples de requête</span><span class="sxs-lookup"><span data-stu-id="72f30-174">Get more query examples</span></span>](advanced-hunting-shared-queries.md)
