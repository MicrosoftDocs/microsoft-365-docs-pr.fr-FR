---
title: Fonction FileProfile () pour la protection avancée contre les menaces Microsoft
description: Découvrez comment utiliser le FileProfile () pour enrichir les informations sur les fichiers dans les résultats de la recherche avancée de la chasse
keywords: chasse aux menaces, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, FileProfile, profil de fichier, fonction, enrichissement
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
ms.openlocfilehash: d0fd359bb6f56f7c20b0a39b7fd45ec551e7e49e
ms.sourcegitcommit: 445b249a6f0420b32e49742fd7744006c7090b2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/18/2020
ms.locfileid: "46797781"
---
# <a name="fileprofile"></a><span data-ttu-id="19a0f-104">FileProfile()</span><span class="sxs-lookup"><span data-stu-id="19a0f-104">FileProfile()</span></span>

<span data-ttu-id="19a0f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="19a0f-105">**Applies to:**</span></span>
- <span data-ttu-id="19a0f-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="19a0f-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="19a0f-107">La `FileProfile()` fonction est une fonction d’enrichissement dans la [chasse avancée](advanced-hunting-overview.md) qui ajoute les données suivantes aux fichiers trouvés par la requête.</span><span class="sxs-lookup"><span data-stu-id="19a0f-107">The `FileProfile()` function is an enrichment function in [advanced hunting](advanced-hunting-overview.md) that adds the following data to files found by the query.</span></span>

| <span data-ttu-id="19a0f-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="19a0f-108">Column</span></span> | <span data-ttu-id="19a0f-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="19a0f-109">Data type</span></span> | <span data-ttu-id="19a0f-110">Description</span><span class="sxs-lookup"><span data-stu-id="19a0f-110">Description</span></span> |
|------------|-------------|-------------|
| <span data-ttu-id="19a0f-111">Algorithm</span><span class="sxs-lookup"><span data-stu-id="19a0f-111">SHA1</span></span> | <span data-ttu-id="19a0f-112">string</span><span class="sxs-lookup"><span data-stu-id="19a0f-112">string</span></span> | <span data-ttu-id="19a0f-113">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="19a0f-113">SHA-1 of the file that the recorded action was applied to</span></span> |
| <span data-ttu-id="19a0f-114">SHA256</span><span class="sxs-lookup"><span data-stu-id="19a0f-114">SHA256</span></span> | <span data-ttu-id="19a0f-115">string</span><span class="sxs-lookup"><span data-stu-id="19a0f-115">string</span></span> | <span data-ttu-id="19a0f-116">SHA-256 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="19a0f-116">SHA-256 of the file that the recorded action was applied to</span></span> |
| <span data-ttu-id="19a0f-117">MD5</span><span class="sxs-lookup"><span data-stu-id="19a0f-117">MD5</span></span> | <span data-ttu-id="19a0f-118">string</span><span class="sxs-lookup"><span data-stu-id="19a0f-118">string</span></span> | <span data-ttu-id="19a0f-119">Hachage MD5 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="19a0f-119">MD5 hash of the file that the recorded action was applied to</span></span> |
| <span data-ttu-id="19a0f-120">FileSize</span><span class="sxs-lookup"><span data-stu-id="19a0f-120">FileSize</span></span> | <span data-ttu-id="19a0f-121">int</span><span class="sxs-lookup"><span data-stu-id="19a0f-121">int</span></span> | <span data-ttu-id="19a0f-122">Taille du fichier en octets</span><span class="sxs-lookup"><span data-stu-id="19a0f-122">Size of the file in bytes</span></span> |
| <span data-ttu-id="19a0f-123">GlobalPrevalence</span><span class="sxs-lookup"><span data-stu-id="19a0f-123">GlobalPrevalence</span></span> | <span data-ttu-id="19a0f-124">int</span><span class="sxs-lookup"><span data-stu-id="19a0f-124">int</span></span> | <span data-ttu-id="19a0f-125">Nombre d’instances de l’entité observées par Microsoft globalement</span><span class="sxs-lookup"><span data-stu-id="19a0f-125">Number of instances of the entity observed by Microsoft globally</span></span> |
| <span data-ttu-id="19a0f-126">GlobalFirstSeen</span><span class="sxs-lookup"><span data-stu-id="19a0f-126">GlobalFirstSeen</span></span> | <span data-ttu-id="19a0f-127">DateHeure</span><span class="sxs-lookup"><span data-stu-id="19a0f-127">datetime</span></span> | <span data-ttu-id="19a0f-128">Date et heure auxquelles l’entité a été observée pour la première fois par Microsoft de manière globale</span><span class="sxs-lookup"><span data-stu-id="19a0f-128">Date and time when the entity was first observed by Microsoft globally</span></span> |
| <span data-ttu-id="19a0f-129">GlobalLastSeen</span><span class="sxs-lookup"><span data-stu-id="19a0f-129">GlobalLastSeen</span></span> | <span data-ttu-id="19a0f-130">DateHeure</span><span class="sxs-lookup"><span data-stu-id="19a0f-130">datetime</span></span> | <span data-ttu-id="19a0f-131">Date et heure auxquelles l’entité a été observée pour la dernière fois par Microsoft globalement</span><span class="sxs-lookup"><span data-stu-id="19a0f-131">Date and time when the entity was last observed by Microsoft globally</span></span> |
| <span data-ttu-id="19a0f-132">Signataire</span><span class="sxs-lookup"><span data-stu-id="19a0f-132">Signer</span></span> | <span data-ttu-id="19a0f-133">string</span><span class="sxs-lookup"><span data-stu-id="19a0f-133">string</span></span> | <span data-ttu-id="19a0f-134">Informations sur le signataire du fichier</span><span class="sxs-lookup"><span data-stu-id="19a0f-134">Information about the signer of the file</span></span> |
| <span data-ttu-id="19a0f-135">Issuer</span><span class="sxs-lookup"><span data-stu-id="19a0f-135">Issuer</span></span> | <span data-ttu-id="19a0f-136">string</span><span class="sxs-lookup"><span data-stu-id="19a0f-136">string</span></span> | <span data-ttu-id="19a0f-137">Informations sur l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="19a0f-137">Information about the issuing certificate authority (CA)</span></span> |
| <span data-ttu-id="19a0f-138">SignerHash</span><span class="sxs-lookup"><span data-stu-id="19a0f-138">SignerHash</span></span> | <span data-ttu-id="19a0f-139">string</span><span class="sxs-lookup"><span data-stu-id="19a0f-139">string</span></span> | <span data-ttu-id="19a0f-140">Valeur de hachage unique identifiant le signataire</span><span class="sxs-lookup"><span data-stu-id="19a0f-140">Unique hash value identifying the signer</span></span> |
| <span data-ttu-id="19a0f-141">IsCertificateValid</span><span class="sxs-lookup"><span data-stu-id="19a0f-141">IsCertificateValid</span></span> | <span data-ttu-id="19a0f-142">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="19a0f-142">boolean</span></span> | <span data-ttu-id="19a0f-143">Si le certificat utilisé pour signer le fichier est valide</span><span class="sxs-lookup"><span data-stu-id="19a0f-143">Whether the certificate used to sign the file is valid</span></span> |
| <span data-ttu-id="19a0f-144">IsRootSignerMicrosoft</span><span class="sxs-lookup"><span data-stu-id="19a0f-144">IsRootSignerMicrosoft</span></span> | <span data-ttu-id="19a0f-145">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="19a0f-145">boolean</span></span> | <span data-ttu-id="19a0f-146">Indique si le signataire du certificat racine est Microsoft</span><span class="sxs-lookup"><span data-stu-id="19a0f-146">Indicates whether the signer of the root certificate is Microsoft</span></span> |
| <span data-ttu-id="19a0f-147">IsExecutable</span><span class="sxs-lookup"><span data-stu-id="19a0f-147">IsExecutable</span></span> | <span data-ttu-id="19a0f-148">valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="19a0f-148">boolean</span></span> | <span data-ttu-id="19a0f-149">Indique si le fichier est un fichier exécutable portable (PE)</span><span class="sxs-lookup"><span data-stu-id="19a0f-149">Whether the file is a Portable Executable (PE) file</span></span> |
| <span data-ttu-id="19a0f-150">ThreatName</span><span class="sxs-lookup"><span data-stu-id="19a0f-150">ThreatName</span></span> | <span data-ttu-id="19a0f-151">string</span><span class="sxs-lookup"><span data-stu-id="19a0f-151">string</span></span> | <span data-ttu-id="19a0f-152">Nom de détection pour tout programme malveillant ou autre menace détectée</span><span class="sxs-lookup"><span data-stu-id="19a0f-152">Detection name for any malware or other threats found</span></span> |
| <span data-ttu-id="19a0f-153">Publisher</span><span class="sxs-lookup"><span data-stu-id="19a0f-153">Publisher</span></span> | <span data-ttu-id="19a0f-154">string</span><span class="sxs-lookup"><span data-stu-id="19a0f-154">string</span></span> | <span data-ttu-id="19a0f-155">Nom de l’organisation qui a publié le fichier</span><span class="sxs-lookup"><span data-stu-id="19a0f-155">Name of the organization that published the file</span></span> |
| <span data-ttu-id="19a0f-156">SoftwareName</span><span class="sxs-lookup"><span data-stu-id="19a0f-156">SoftwareName</span></span> | <span data-ttu-id="19a0f-157">string</span><span class="sxs-lookup"><span data-stu-id="19a0f-157">string</span></span> | <span data-ttu-id="19a0f-158">Nom du produit logiciel</span><span class="sxs-lookup"><span data-stu-id="19a0f-158">Name of the software product</span></span> |

## <a name="syntax"></a><span data-ttu-id="19a0f-159">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19a0f-159">Syntax</span></span>

```kusto
invoke FileProfile(x,y)
```

## <a name="arguments"></a><span data-ttu-id="19a0f-160">Arguments</span><span class="sxs-lookup"><span data-stu-id="19a0f-160">Arguments</span></span>

- <span data-ttu-id="19a0f-161">**x** — colonne ID de fichier à utiliser : `SHA1` , `SHA256` , `InitiatingProcessSHA1` ou ; la `InitiatingProcessSHA256` fonction utilise `SHA1` si elle n’est pas spécifiée</span><span class="sxs-lookup"><span data-stu-id="19a0f-161">**x** — file ID column to use: `SHA1`, `SHA256`, `InitiatingProcessSHA1` or `InitiatingProcessSHA256`; function uses `SHA1` if unspecified</span></span>
- <span data-ttu-id="19a0f-162">**y** : limiter le nombre d’enregistrements à enrichir, 1-1000 ; la fonction utilise 100 si elle n’est pas spécifiée</span><span class="sxs-lookup"><span data-stu-id="19a0f-162">**y** — limit to the number of records to enrich, 1-1000; function uses 100 if unspecified</span></span>

## <a name="examples"></a><span data-ttu-id="19a0f-163">Exemples</span><span class="sxs-lookup"><span data-stu-id="19a0f-163">Examples</span></span>

### <a name="project-only-the-sha1-column-and-enrich-it"></a><span data-ttu-id="19a0f-164">Projet uniquement la colonne SHA1 et enrichir celle-ci</span><span class="sxs-lookup"><span data-stu-id="19a0f-164">Project only the SHA1 column and enrich it</span></span>

```kusto
DeviceFileEvents
| where isnotempty(SHA1) and Timestamp > ago(1d)
| take 10
| project SHA1
| invoke FileProfile()
```

### <a name="enrich-the-first-500-records-and-list-low-prevalence-files"></a><span data-ttu-id="19a0f-165">Enrichir les premiers 500 enregistrements et répertorier les fichiers à faible prévalence</span><span class="sxs-lookup"><span data-stu-id="19a0f-165">Enrich the first 500 records and list low-prevalence files</span></span>

```kusto
DeviceFileEvents
| where ActionType == "FileCreated" and Timestamp > ago(1d)
| project CreatedOn = Timestamp, FileName, FolderPath, SHA1
| invoke FileProfile("SHA1", 500) 
| where GlobalPrevalence < 15
```

## <a name="related-topics"></a><span data-ttu-id="19a0f-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19a0f-166">Related topics</span></span>
- [<span data-ttu-id="19a0f-167">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="19a0f-167">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="19a0f-168">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="19a0f-168">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="19a0f-169">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="19a0f-169">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="19a0f-170">Obtenir d’autres exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="19a0f-170">Get more query examples</span></span>](advanced-hunting-shared-queries.md)