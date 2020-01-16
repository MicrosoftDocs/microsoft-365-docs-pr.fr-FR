---
title: Table DeviceFileCertificateInfoBeta dans le schéma de chasse avancé
description: En savoir plus sur les informations de signature de fichiers dans le tableau DeviceFileCertificateInfoBeta du schéma de chasse avancé
keywords: chasse aux menaces, recherche de menace, recherche sur les menaces de la cybercriminalité, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, signature numérique, certificat, signature de fichiers, DeviceFileCertificateInfoBeta
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: d51fc812ffb82d9af1f706e513498da7611a1a6b
ms.sourcegitcommit: 5b8e9935fe7bfcb96b8f8356119ce23152bd16a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2020
ms.locfileid: "41210466"
---
# <a name="devicefilecertificateinfobeta"></a><span data-ttu-id="4bc9c-104">DeviceFileCertificateInfoBeta</span><span class="sxs-lookup"><span data-stu-id="4bc9c-104">DeviceFileCertificateInfoBeta</span></span>

<span data-ttu-id="4bc9c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4bc9c-105">**Applies to:**</span></span>
- <span data-ttu-id="4bc9c-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="4bc9c-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="4bc9c-107">Le `DeviceFileCertificateInfoBeta` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les certificats de signature de fichier.</span><span class="sxs-lookup"><span data-stu-id="4bc9c-107">The `DeviceFileCertificateInfoBeta` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about file signing certificates.</span></span> <span data-ttu-id="4bc9c-108">Ce tableau utilise les données obtenues à partir des activités de vérification de certificat effectuées régulièrement sur des fichiers sur des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="4bc9c-108">This table uses data obtained from certificate verification activities regularly performed on files on endpoints.</span></span>

<span data-ttu-id="4bc9c-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4bc9c-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="4bc9c-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="4bc9c-110">Column name</span></span> | <span data-ttu-id="4bc9c-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="4bc9c-111">Data type</span></span> | <span data-ttu-id="4bc9c-112">Description</span><span class="sxs-lookup"><span data-stu-id="4bc9c-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="4bc9c-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="4bc9c-113">datetime</span></span> | <span data-ttu-id="4bc9c-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="4bc9c-114">Date and time when the event was recorded</span></span>
| `DeviceId` | <span data-ttu-id="4bc9c-115">chaîne</span><span class="sxs-lookup"><span data-stu-id="4bc9c-115">string</span></span> | <span data-ttu-id="4bc9c-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="4bc9c-116">Unique identifier for the machine in the service</span></span>
| `DeviceName` | <span data-ttu-id="4bc9c-117">string</span><span class="sxs-lookup"><span data-stu-id="4bc9c-117">string</span></span> | <span data-ttu-id="4bc9c-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="4bc9c-118">Fully qualified domain name (FQDN) of the machine</span></span>
| `SHA1` | <span data-ttu-id="4bc9c-119">string</span><span class="sxs-lookup"><span data-stu-id="4bc9c-119">string</span></span> | <span data-ttu-id="4bc9c-120">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="4bc9c-120">SHA-1 of the file that the recorded action was applied to</span></span>
| `IsSigned` | <span data-ttu-id="4bc9c-121">booléen</span><span class="sxs-lookup"><span data-stu-id="4bc9c-121">boolean</span></span> | <span data-ttu-id="4bc9c-122">Indique si le fichier est signé</span><span class="sxs-lookup"><span data-stu-id="4bc9c-122">Indicates whether the file is signed</span></span>
| `SignatureType` | <span data-ttu-id="4bc9c-123">string</span><span class="sxs-lookup"><span data-stu-id="4bc9c-123">string</span></span> | <span data-ttu-id="4bc9c-124">Indique si les informations de signature ont été lues dans le fichier ou lues à partir d’un fichier de catalogue externe.</span><span class="sxs-lookup"><span data-stu-id="4bc9c-124">Indicates whether signature information was read as embedded content in the file itself or read from an external catalog file</span></span>
| `Signer` | <span data-ttu-id="4bc9c-125">string</span><span class="sxs-lookup"><span data-stu-id="4bc9c-125">string</span></span> | <span data-ttu-id="4bc9c-126">Informations sur le signataire du fichier</span><span class="sxs-lookup"><span data-stu-id="4bc9c-126">Information about the signer of the file</span></span>
| `SignerHash` | <span data-ttu-id="4bc9c-127">string</span><span class="sxs-lookup"><span data-stu-id="4bc9c-127">string</span></span> | <span data-ttu-id="4bc9c-128">Valeur de hachage unique identifiant le signataire</span><span class="sxs-lookup"><span data-stu-id="4bc9c-128">Unique hash value identifying the signer</span></span>
| `Issuer` | <span data-ttu-id="4bc9c-129">string</span><span class="sxs-lookup"><span data-stu-id="4bc9c-129">string</span></span> | <span data-ttu-id="4bc9c-130">Informations sur l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="4bc9c-130">Information about the issuing certificate authority (CA)</span></span>
| `IssuerHash` | <span data-ttu-id="4bc9c-131">string</span><span class="sxs-lookup"><span data-stu-id="4bc9c-131">string</span></span> | <span data-ttu-id="4bc9c-132">Valeur de hachage unique permettant l’identification de l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="4bc9c-132">Unique hash value identifying issuing certificate authority (CA)</span></span>
| `CrlDistributionPointUrls` | <span data-ttu-id="4bc9c-133">string</span><span class="sxs-lookup"><span data-stu-id="4bc9c-133">string</span></span> |  <span data-ttu-id="4bc9c-134">URL du partage réseau qui contient les certificats et la liste de révocation de certificats (CRL)</span><span class="sxs-lookup"><span data-stu-id="4bc9c-134">URL of the network share that contains certificates and the certificate revocation list (CRL)</span></span>
| `CertificateCreationTime` | <span data-ttu-id="4bc9c-135">DateHeure</span><span class="sxs-lookup"><span data-stu-id="4bc9c-135">datetime</span></span> | <span data-ttu-id="4bc9c-136">Date et heure de création du certificat</span><span class="sxs-lookup"><span data-stu-id="4bc9c-136">Date and time the certificate was created</span></span>
| `CertificateExpirationTime` | <span data-ttu-id="4bc9c-137">DateHeure</span><span class="sxs-lookup"><span data-stu-id="4bc9c-137">datetime</span></span> | <span data-ttu-id="4bc9c-138">Date et heure auxquelles le certificat est configuré pour expirer</span><span class="sxs-lookup"><span data-stu-id="4bc9c-138">Date and time the certificate is set to expire</span></span>
| `CertificateCountersignatureTime` | <span data-ttu-id="4bc9c-139">DateHeure</span><span class="sxs-lookup"><span data-stu-id="4bc9c-139">datetime</span></span> | <span data-ttu-id="4bc9c-140">Date et heure auxquelles le certificat a été contresigné</span><span class="sxs-lookup"><span data-stu-id="4bc9c-140">Date and time the certificate was countersigned</span></span>
| `IsTrusted` | <span data-ttu-id="4bc9c-141">booléen</span><span class="sxs-lookup"><span data-stu-id="4bc9c-141">boolean</span></span> | <span data-ttu-id="4bc9c-142">Indique si le fichier est approuvé en fonction des résultats de la fonction WinVerifyTrust, qui vérifie les informations de certificat racine inconnues, les signatures non valides, les certificats révoqués et d’autres attributs douteux.</span><span class="sxs-lookup"><span data-stu-id="4bc9c-142">Indicates whether the file is trusted based on the results of the WinVerifyTrust function, which checks for unknown root certificate information, invalid signatures, revoked certificates, and other questionable attributes</span></span>
| `IsRootSignerMicrosoft` | <span data-ttu-id="4bc9c-143">booléen</span><span class="sxs-lookup"><span data-stu-id="4bc9c-143">boolean</span></span> | <span data-ttu-id="4bc9c-144">Indique si le signataire du certificat racine est Microsoft</span><span class="sxs-lookup"><span data-stu-id="4bc9c-144">Indicates whether the signer of the root certificate is Microsoft</span></span>
| `ReportId` | <span data-ttu-id="4bc9c-145">long</span><span class="sxs-lookup"><span data-stu-id="4bc9c-145">long</span></span> | <span data-ttu-id="4bc9c-146">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="4bc9c-146">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="4bc9c-147">Pour identifier les événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et timestamp.</span><span class="sxs-lookup"><span data-stu-id="4bc9c-147">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bc9c-148">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="4bc9c-148">Related topics</span></span>
- [<span data-ttu-id="4bc9c-149">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="4bc9c-149">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="4bc9c-150">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="4bc9c-150">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="4bc9c-151">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="4bc9c-151">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="4bc9c-152">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="4bc9c-152">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="4bc9c-153">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="4bc9c-153">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="4bc9c-154">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="4bc9c-154">Apply query best practices</span></span>](advanced-hunting-best-practices.md)