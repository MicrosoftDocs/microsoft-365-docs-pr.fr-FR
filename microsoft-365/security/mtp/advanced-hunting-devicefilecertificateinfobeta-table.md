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
ms.openlocfilehash: 4d5769088f3904bf62d2889f35f236c9410628db
ms.sourcegitcommit: 7705fdbcee4f8714ce044c9e120a431023f7a367
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2020
ms.locfileid: "41230202"
---
# <a name="devicefilecertificateinfobeta"></a><span data-ttu-id="bcbba-104">DeviceFileCertificateInfoBeta</span><span class="sxs-lookup"><span data-stu-id="bcbba-104">DeviceFileCertificateInfoBeta</span></span>

<span data-ttu-id="bcbba-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bcbba-105">**Applies to:**</span></span>
- <span data-ttu-id="bcbba-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="bcbba-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="bcbba-107">Le `DeviceFileCertificateInfoBeta` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les certificats de signature de fichier.</span><span class="sxs-lookup"><span data-stu-id="bcbba-107">The `DeviceFileCertificateInfoBeta` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about file signing certificates.</span></span> <span data-ttu-id="bcbba-108">Ce tableau utilise les données obtenues à partir des activités de vérification de certificat effectuées régulièrement sur des fichiers sur des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="bcbba-108">This table uses data obtained from certificate verification activities regularly performed on files on endpoints.</span></span>

<span data-ttu-id="bcbba-109">Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bcbba-109">For information on other tables in the advanced hunting schema, [see the advanced hunting reference](advanced-hunting-schema-tables.md).</span></span>

| <span data-ttu-id="bcbba-110">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="bcbba-110">Column name</span></span> | <span data-ttu-id="bcbba-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="bcbba-111">Data type</span></span> | <span data-ttu-id="bcbba-112">Description</span><span class="sxs-lookup"><span data-stu-id="bcbba-112">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="bcbba-113">DateHeure</span><span class="sxs-lookup"><span data-stu-id="bcbba-113">datetime</span></span> | <span data-ttu-id="bcbba-114">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="bcbba-114">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="bcbba-115">chaîne</span><span class="sxs-lookup"><span data-stu-id="bcbba-115">string</span></span> | <span data-ttu-id="bcbba-116">Identificateur unique de la machine dans le service</span><span class="sxs-lookup"><span data-stu-id="bcbba-116">Unique identifier for the machine in the service</span></span> |
| `DeviceName` | <span data-ttu-id="bcbba-117">string</span><span class="sxs-lookup"><span data-stu-id="bcbba-117">string</span></span> | <span data-ttu-id="bcbba-118">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="bcbba-118">Fully qualified domain name (FQDN) of the machine</span></span> |
| `SHA1` | <span data-ttu-id="bcbba-119">string</span><span class="sxs-lookup"><span data-stu-id="bcbba-119">string</span></span> | <span data-ttu-id="bcbba-120">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="bcbba-120">SHA-1 of the file that the recorded action was applied to</span></span> |
| `IsSigned` | <span data-ttu-id="bcbba-121">booléen</span><span class="sxs-lookup"><span data-stu-id="bcbba-121">boolean</span></span> | <span data-ttu-id="bcbba-122">Indique si le fichier est signé</span><span class="sxs-lookup"><span data-stu-id="bcbba-122">Indicates whether the file is signed</span></span> |
| `SignatureType` | <span data-ttu-id="bcbba-123">string</span><span class="sxs-lookup"><span data-stu-id="bcbba-123">string</span></span> | <span data-ttu-id="bcbba-124">Indique si les informations de signature ont été lues comme étant incorporées</span><span class="sxs-lookup"><span data-stu-id="bcbba-124">Indicates whether signature information was read as embedded</span></span> | <span data-ttu-id="bcbba-125">contenu du fichier lui-même ou lu à partir d’un fichier de catalogue externe</span><span class="sxs-lookup"><span data-stu-id="bcbba-125">content in the file itself or read from an external catalog file</span></span> |
| `Signer` | <span data-ttu-id="bcbba-126">string</span><span class="sxs-lookup"><span data-stu-id="bcbba-126">string</span></span> | <span data-ttu-id="bcbba-127">Informations sur le signataire du fichier</span><span class="sxs-lookup"><span data-stu-id="bcbba-127">Information about the signer of the file</span></span> |
| `SignerHash` | <span data-ttu-id="bcbba-128">string</span><span class="sxs-lookup"><span data-stu-id="bcbba-128">string</span></span> | <span data-ttu-id="bcbba-129">Valeur de hachage unique identifiant le signataire</span><span class="sxs-lookup"><span data-stu-id="bcbba-129">Unique hash value identifying the signer</span></span> |
| `Issuer` | <span data-ttu-id="bcbba-130">string</span><span class="sxs-lookup"><span data-stu-id="bcbba-130">string</span></span> | <span data-ttu-id="bcbba-131">Informations sur l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="bcbba-131">Information about the issuing certificate authority (CA)</span></span> |
| `IssuerHash` | <span data-ttu-id="bcbba-132">string</span><span class="sxs-lookup"><span data-stu-id="bcbba-132">string</span></span> | <span data-ttu-id="bcbba-133">Valeur de hachage unique permettant l’identification de l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="bcbba-133">Unique hash value identifying issuing certificate authority (CA)</span></span> |
| `CertificateSerialNumber` | <span data-ttu-id="bcbba-134">string</span><span class="sxs-lookup"><span data-stu-id="bcbba-134">string</span></span> | <span data-ttu-id="bcbba-135">Identificateur du certificat propre à l’autorité de certification émettrice.</span><span class="sxs-lookup"><span data-stu-id="bcbba-135">Identifier for the certificate that is unique to the issuing certificate authority (CA)</span></span> |
| `CrlDistributionPointUrls` | <span data-ttu-id="bcbba-136">string</span><span class="sxs-lookup"><span data-stu-id="bcbba-136">string</span></span> |  <span data-ttu-id="bcbba-137">Tableau JSON répertoriant les URL des partages réseau qui contiennent des certificats et des listes de révocation de certificats (CRL)</span><span class="sxs-lookup"><span data-stu-id="bcbba-137">JSON array listing the URLs of network shares that contain certificates and certificate revocation lists (CRLs)</span></span> |
| `CertificateCreationTime` | <span data-ttu-id="bcbba-138">DateHeure</span><span class="sxs-lookup"><span data-stu-id="bcbba-138">datetime</span></span> | <span data-ttu-id="bcbba-139">Date et heure de création du certificat</span><span class="sxs-lookup"><span data-stu-id="bcbba-139">Date and time the certificate was created</span></span> |
| `CertificateExpirationTime` | <span data-ttu-id="bcbba-140">DateHeure</span><span class="sxs-lookup"><span data-stu-id="bcbba-140">datetime</span></span> | <span data-ttu-id="bcbba-141">Date et heure auxquelles le certificat est configuré pour expirer</span><span class="sxs-lookup"><span data-stu-id="bcbba-141">Date and time the certificate is set to expire</span></span> |
| `CertificateCountersignatureTime` | <span data-ttu-id="bcbba-142">DateHeure</span><span class="sxs-lookup"><span data-stu-id="bcbba-142">datetime</span></span> | <span data-ttu-id="bcbba-143">Date et heure auxquelles le certificat a été contresigné</span><span class="sxs-lookup"><span data-stu-id="bcbba-143">Date and time the certificate was countersigned</span></span> |
| `IsTrusted` | <span data-ttu-id="bcbba-144">booléen</span><span class="sxs-lookup"><span data-stu-id="bcbba-144">boolean</span></span> | <span data-ttu-id="bcbba-145">Indique si le fichier est approuvé en fonction des résultats de la fonction WinVerifyTrust, qui vérifie les informations de certificat racine inconnues, les signatures non valides, les certificats révoqués et d’autres attributs douteux.</span><span class="sxs-lookup"><span data-stu-id="bcbba-145">Indicates whether the file is trusted based on the results of the WinVerifyTrust function, which checks for unknown root certificate information, invalid signatures, revoked certificates, and other questionable attributes</span></span> |
| `IsRootSignerMicrosoft` | <span data-ttu-id="bcbba-146">booléen</span><span class="sxs-lookup"><span data-stu-id="bcbba-146">boolean</span></span> | <span data-ttu-id="bcbba-147">Indique si le signataire du certificat racine est Microsoft</span><span class="sxs-lookup"><span data-stu-id="bcbba-147">Indicates whether the signer of the root certificate is Microsoft</span></span> |
| `ReportId` | <span data-ttu-id="bcbba-148">long</span><span class="sxs-lookup"><span data-stu-id="bcbba-148">long</span></span> | <span data-ttu-id="bcbba-149">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="bcbba-149">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="bcbba-150">Pour identifier les événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et timestamp.</span><span class="sxs-lookup"><span data-stu-id="bcbba-150">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns.</span></span> | 

## <a name="related-topics"></a><span data-ttu-id="bcbba-151">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="bcbba-151">Related topics</span></span>
- [<span data-ttu-id="bcbba-152">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="bcbba-152">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="bcbba-153">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="bcbba-153">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="bcbba-154">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="bcbba-154">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="bcbba-155">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="bcbba-155">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="bcbba-156">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="bcbba-156">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="bcbba-157">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="bcbba-157">Apply query best practices</span></span>](advanced-hunting-best-practices.md)