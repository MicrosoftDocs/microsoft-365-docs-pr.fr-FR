---
title: Table DeviceFileCertificateInfo dans le schéma de recherche avancé
description: En savoir plus sur les informations de signature de fichier dans la table DeviceFileCertificateInfo du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, digital signature, certificate, file signing, DeviceFileCertificateInfo
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
ms.openlocfilehash: e35e8e86f6814a5f90a7921f71ccab7247fcc1bc
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49931313"
---
# <a name="devicefilecertificateinfo"></a><span data-ttu-id="555c8-104">DeviceFileCertificateInfo</span><span class="sxs-lookup"><span data-stu-id="555c8-104">DeviceFileCertificateInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="555c8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="555c8-105">**Applies to:**</span></span>
- <span data-ttu-id="555c8-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="555c8-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="555c8-107">Le `DeviceFileCertificateInfo` tableau du schéma de [recherche](advanced-hunting-overview.md) avancée contient des informations sur les certificats de signature de fichiers.</span><span class="sxs-lookup"><span data-stu-id="555c8-107">The `DeviceFileCertificateInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about file signing certificates.</span></span> <span data-ttu-id="555c8-108">Ce tableau utilise les données obtenues à partir des activités de vérification de certificat effectuées régulièrement sur les fichiers sur les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="555c8-108">This table uses data obtained from certificate verification activities regularly performed on files on endpoints.</span></span>

<span data-ttu-id="555c8-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="555c8-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="555c8-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="555c8-110">Column name</span></span> | <span data-ttu-id="555c8-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="555c8-111">Data type</span></span> | <span data-ttu-id="555c8-112">Description</span><span class="sxs-lookup"><span data-stu-id="555c8-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="555c8-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="555c8-113">datetime</span></span> | <span data-ttu-id="555c8-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="555c8-114">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="555c8-115">string</span><span class="sxs-lookup"><span data-stu-id="555c8-115">string</span></span> | <span data-ttu-id="555c8-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="555c8-116">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="555c8-117">string</span><span class="sxs-lookup"><span data-stu-id="555c8-117">string</span></span> | <span data-ttu-id="555c8-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="555c8-118">Fully qualified domain name (FQDN) of the machine</span></span> |
| `SHA1` | <span data-ttu-id="555c8-119">string</span><span class="sxs-lookup"><span data-stu-id="555c8-119">string</span></span> | <span data-ttu-id="555c8-120">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="555c8-120">SHA-1 of the file that the recorded action was applied to</span></span> |
| `IsSigned` | <span data-ttu-id="555c8-121">booléen</span><span class="sxs-lookup"><span data-stu-id="555c8-121">boolean</span></span> | <span data-ttu-id="555c8-122">Indique si le fichier est signé</span><span class="sxs-lookup"><span data-stu-id="555c8-122">Indicates whether the file is signed</span></span> |
| `SignatureType` | <span data-ttu-id="555c8-123">string</span><span class="sxs-lookup"><span data-stu-id="555c8-123">string</span></span> | <span data-ttu-id="555c8-124">Indique si les informations de signature ont été lues en tant que contenu incorporé dans le fichier lui-même ou lues à partir d’un fichier catalogue externe</span><span class="sxs-lookup"><span data-stu-id="555c8-124">Indicates whether signature information was read as embedded content in the file itself or read from an external catalog file</span></span> |
| `Signer` | <span data-ttu-id="555c8-125">string</span><span class="sxs-lookup"><span data-stu-id="555c8-125">string</span></span> | <span data-ttu-id="555c8-126">Informations sur le signataire du fichier</span><span class="sxs-lookup"><span data-stu-id="555c8-126">Information about the signer of the file</span></span> |
| `SignerHash` | <span data-ttu-id="555c8-127">string</span><span class="sxs-lookup"><span data-stu-id="555c8-127">string</span></span> | <span data-ttu-id="555c8-128">Valeur de hachage unique identifiant le signataire</span><span class="sxs-lookup"><span data-stu-id="555c8-128">Unique hash value identifying the signer</span></span> |
| `Issuer` | <span data-ttu-id="555c8-129">string</span><span class="sxs-lookup"><span data-stu-id="555c8-129">string</span></span> | <span data-ttu-id="555c8-130">Informations sur l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="555c8-130">Information about the issuing certificate authority (CA)</span></span> |
| `IssuerHash` | <span data-ttu-id="555c8-131">string</span><span class="sxs-lookup"><span data-stu-id="555c8-131">string</span></span> | <span data-ttu-id="555c8-132">Valeur de hachage unique identifiant l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="555c8-132">Unique hash value identifying issuing certificate authority (CA)</span></span> |
| `CertificateSerialNumber` | <span data-ttu-id="555c8-133">string</span><span class="sxs-lookup"><span data-stu-id="555c8-133">string</span></span> | <span data-ttu-id="555c8-134">Identificateur du certificat propre à l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="555c8-134">Identifier for the certificate that is unique to the issuing certificate authority (CA)</span></span> |
| `CrlDistributionPointUrls` | <span data-ttu-id="555c8-135">string</span><span class="sxs-lookup"><span data-stu-id="555c8-135">string</span></span> |  <span data-ttu-id="555c8-136">Tableau JSON répertoriant les URL des partages réseau qui contiennent des certificats et des listes de révocation de certificats (CRL)</span><span class="sxs-lookup"><span data-stu-id="555c8-136">JSON array listing the URLs of network shares that contain certificates and certificate revocation lists (CRLs)</span></span> |
| `CertificateCreationTime` | <span data-ttu-id="555c8-137">DateHeure</span><span class="sxs-lookup"><span data-stu-id="555c8-137">datetime</span></span> | <span data-ttu-id="555c8-138">Date et heure de création du certificat</span><span class="sxs-lookup"><span data-stu-id="555c8-138">Date and time the certificate was created</span></span> |
| `CertificateExpirationTime` | <span data-ttu-id="555c8-139">DateHeure</span><span class="sxs-lookup"><span data-stu-id="555c8-139">datetime</span></span> | <span data-ttu-id="555c8-140">Date et heure d’expiration du certificat</span><span class="sxs-lookup"><span data-stu-id="555c8-140">Date and time the certificate is set to expire</span></span> |
| `CertificateCountersignatureTime` | <span data-ttu-id="555c8-141">DateHeure</span><span class="sxs-lookup"><span data-stu-id="555c8-141">datetime</span></span> | <span data-ttu-id="555c8-142">Date et heure de contre-signature du certificat</span><span class="sxs-lookup"><span data-stu-id="555c8-142">Date and time the certificate was countersigned</span></span> |
| `IsTrusted` | <span data-ttu-id="555c8-143">booléen</span><span class="sxs-lookup"><span data-stu-id="555c8-143">boolean</span></span> | <span data-ttu-id="555c8-144">Indique si le fichier est approuvé en fonction des résultats de la fonction WinVerifyTrust, qui recherche des informations de certificat racine inconnues, des signatures non valides, des certificats révoqués et d’autres attributs douteux</span><span class="sxs-lookup"><span data-stu-id="555c8-144">Indicates whether the file is trusted based on the results of the WinVerifyTrust function, which checks for unknown root certificate information, invalid signatures, revoked certificates, and other questionable attributes</span></span> |
| `IsRootSignerMicrosoft` | <span data-ttu-id="555c8-145">booléen</span><span class="sxs-lookup"><span data-stu-id="555c8-145">boolean</span></span> | <span data-ttu-id="555c8-146">Indique si le signataire du certificat racine est Microsoft</span><span class="sxs-lookup"><span data-stu-id="555c8-146">Indicates whether the signer of the root certificate is Microsoft</span></span> |
| `ReportId` | <span data-ttu-id="555c8-147">long</span><span class="sxs-lookup"><span data-stu-id="555c8-147">long</span></span> | <span data-ttu-id="555c8-148">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="555c8-148">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="555c8-149">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp.</span><span class="sxs-lookup"><span data-stu-id="555c8-149">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns.</span></span> | 

## <a name="related-topics"></a><span data-ttu-id="555c8-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="555c8-150">Related topics</span></span>
- [<span data-ttu-id="555c8-151">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="555c8-151">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="555c8-152">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="555c8-152">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="555c8-153">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="555c8-153">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="555c8-154">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="555c8-154">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="555c8-155">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="555c8-155">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="555c8-156">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="555c8-156">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
