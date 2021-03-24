---
title: Table DeviceFileCertificateInfo dans le schéma de recherche avancé
description: En savoir plus sur les informations de signature de fichier dans la table DeviceFileCertificateInfo du schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, mdatp, microsoft defender atp, wdatp search, query, telemetry, schema reference, kusto, table, column, data type, description, digital signature, certificate, file signing, DeviceFileCertificateInfo
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.date: 01/14/2020
ms.technology: mde
ms.openlocfilehash: b3b5af8093107925c6c12c901e8138960c5eeaf6
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064382"
---
# <a name="devicefilecertificateinfo"></a><span data-ttu-id="0f31e-104">DeviceFileCertificateInfo</span><span class="sxs-lookup"><span data-stu-id="0f31e-104">DeviceFileCertificateInfo</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="0f31e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0f31e-105">**Applies to:**</span></span>
- [<span data-ttu-id="0f31e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0f31e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)


><span data-ttu-id="0f31e-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="0f31e-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="0f31e-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="0f31e-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

<span data-ttu-id="0f31e-109">Le `DeviceFileCertificateInfo` tableau du schéma de [recherche](advanced-hunting-overview.md) avancée contient des informations sur les certificats de signature de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0f31e-109">The `DeviceFileCertificateInfo` table in the [advanced hunting](advanced-hunting-overview.md) schema contains information about file signing certificates.</span></span> <span data-ttu-id="0f31e-110">Ce tableau utilise les données obtenues à partir des activités de vérification de certificat effectuées régulièrement sur les fichiers sur les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0f31e-110">This table uses data obtained from certificate verification activities regularly performed on files on endpoints.</span></span>

<span data-ttu-id="0f31e-111">Pour plus d’informations sur les autres tableaux du schéma de chasse avancé, voir la référence de schéma [de chasse avancée.](advanced-hunting-schema-reference.md)</span><span class="sxs-lookup"><span data-stu-id="0f31e-111">For information on other tables in the advanced hunting schema, see [the advanced hunting schema reference](advanced-hunting-schema-reference.md).</span></span>

| <span data-ttu-id="0f31e-112">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="0f31e-112">Column name</span></span> | <span data-ttu-id="0f31e-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="0f31e-113">Data type</span></span> | <span data-ttu-id="0f31e-114">Description</span><span class="sxs-lookup"><span data-stu-id="0f31e-114">Description</span></span> |
|-------------|-----------|-------------|
| `Timestamp` | <span data-ttu-id="0f31e-115">DateHeure</span><span class="sxs-lookup"><span data-stu-id="0f31e-115">datetime</span></span> | <span data-ttu-id="0f31e-116">Date et heure d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="0f31e-116">Date and time when the event was recorded</span></span> |
| `DeviceId` | <span data-ttu-id="0f31e-117">string</span><span class="sxs-lookup"><span data-stu-id="0f31e-117">string</span></span> | <span data-ttu-id="0f31e-118">Identificateur unique de l’appareil dans le service</span><span class="sxs-lookup"><span data-stu-id="0f31e-118">Unique identifier for the device in the service</span></span> |
| `DeviceName` | <span data-ttu-id="0f31e-119">string</span><span class="sxs-lookup"><span data-stu-id="0f31e-119">string</span></span> | <span data-ttu-id="0f31e-120">Nom de domaine complet (FQDN) de l’appareil</span><span class="sxs-lookup"><span data-stu-id="0f31e-120">Fully qualified domain name (FQDN) of the device</span></span> |
| `SHA1` | <span data-ttu-id="0f31e-121">string</span><span class="sxs-lookup"><span data-stu-id="0f31e-121">string</span></span> | <span data-ttu-id="0f31e-122">SHA-1 du fichier auquel l’action enregistrée a été appliquée</span><span class="sxs-lookup"><span data-stu-id="0f31e-122">SHA-1 of the file that the recorded action was applied to</span></span> |
| `IsSigned` | <span data-ttu-id="0f31e-123">booléen</span><span class="sxs-lookup"><span data-stu-id="0f31e-123">boolean</span></span> | <span data-ttu-id="0f31e-124">Indique si le fichier est signé</span><span class="sxs-lookup"><span data-stu-id="0f31e-124">Indicates whether the file is signed</span></span> |
| `SignatureType` | <span data-ttu-id="0f31e-125">string</span><span class="sxs-lookup"><span data-stu-id="0f31e-125">string</span></span> | <span data-ttu-id="0f31e-126">Indique si les informations de signature ont été lues en tant que contenu incorporé dans le fichier lui-même ou lues à partir d’un fichier catalogue externe</span><span class="sxs-lookup"><span data-stu-id="0f31e-126">Indicates whether signature information was read as embedded content in the file itself or read from an external catalog file</span></span> |
| `Signer` | <span data-ttu-id="0f31e-127">string</span><span class="sxs-lookup"><span data-stu-id="0f31e-127">string</span></span> | <span data-ttu-id="0f31e-128">Informations sur le signataire du fichier</span><span class="sxs-lookup"><span data-stu-id="0f31e-128">Information about the signer of the file</span></span> |
| `SignerHash` | <span data-ttu-id="0f31e-129">string</span><span class="sxs-lookup"><span data-stu-id="0f31e-129">string</span></span> | <span data-ttu-id="0f31e-130">Valeur de hachage unique identifiant le signataire</span><span class="sxs-lookup"><span data-stu-id="0f31e-130">Unique hash value identifying the signer</span></span> |
| `Issuer` | <span data-ttu-id="0f31e-131">string</span><span class="sxs-lookup"><span data-stu-id="0f31e-131">string</span></span> | <span data-ttu-id="0f31e-132">Informations sur l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="0f31e-132">Information about the issuing certificate authority (CA)</span></span> |
| `IssuerHash` | <span data-ttu-id="0f31e-133">string</span><span class="sxs-lookup"><span data-stu-id="0f31e-133">string</span></span> | <span data-ttu-id="0f31e-134">Valeur de hachage unique identifiant l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="0f31e-134">Unique hash value identifying issuing certificate authority (CA)</span></span> |
| `CertificateSerialNumber` | <span data-ttu-id="0f31e-135">string</span><span class="sxs-lookup"><span data-stu-id="0f31e-135">string</span></span> | <span data-ttu-id="0f31e-136">Identificateur du certificat propre à l’autorité de certification émettrice</span><span class="sxs-lookup"><span data-stu-id="0f31e-136">Identifier for the certificate that is unique to the issuing certificate authority (CA)</span></span> |
| `CrlDistributionPointUrls` | <span data-ttu-id="0f31e-137">string</span><span class="sxs-lookup"><span data-stu-id="0f31e-137">string</span></span> |  <span data-ttu-id="0f31e-138">Tableau JSON répertoriant les URL des partages réseau qui contiennent des certificats et des listes de révocation de certificats (CRL)</span><span class="sxs-lookup"><span data-stu-id="0f31e-138">JSON array listing the URLs of network shares that contain certificates and certificate revocation lists (CRLs)</span></span> |
| `CertificateCreationTime` | <span data-ttu-id="0f31e-139">DateHeure</span><span class="sxs-lookup"><span data-stu-id="0f31e-139">datetime</span></span> | <span data-ttu-id="0f31e-140">Date et heure de création du certificat</span><span class="sxs-lookup"><span data-stu-id="0f31e-140">Date and time the certificate was created</span></span> |
| `CertificateExpirationTime` | <span data-ttu-id="0f31e-141">DateHeure</span><span class="sxs-lookup"><span data-stu-id="0f31e-141">datetime</span></span> | <span data-ttu-id="0f31e-142">Date et heure d’expiration du certificat</span><span class="sxs-lookup"><span data-stu-id="0f31e-142">Date and time the certificate is set to expire</span></span> |
| `CertificateCountersignatureTime` | <span data-ttu-id="0f31e-143">DateHeure</span><span class="sxs-lookup"><span data-stu-id="0f31e-143">datetime</span></span> | <span data-ttu-id="0f31e-144">Date et heure de contre-signature du certificat</span><span class="sxs-lookup"><span data-stu-id="0f31e-144">Date and time the certificate was countersigned</span></span> |
| `IsTrusted` | <span data-ttu-id="0f31e-145">booléen</span><span class="sxs-lookup"><span data-stu-id="0f31e-145">boolean</span></span> | <span data-ttu-id="0f31e-146">Indique si le fichier est approuvé en fonction des résultats de la fonction WinVerifyTrust, qui recherche des informations de certificat racine inconnues, des signatures non valides, des certificats révoqués et d’autres attributs douteux</span><span class="sxs-lookup"><span data-stu-id="0f31e-146">Indicates whether the file is trusted based on the results of the WinVerifyTrust function, which checks for unknown root certificate information, invalid signatures, revoked certificates, and other questionable attributes</span></span> |
| `IsRootSignerMicrosoft` | <span data-ttu-id="0f31e-147">booléen</span><span class="sxs-lookup"><span data-stu-id="0f31e-147">boolean</span></span> | <span data-ttu-id="0f31e-148">Indique si le signataire du certificat racine est Microsoft</span><span class="sxs-lookup"><span data-stu-id="0f31e-148">Indicates whether the signer of the root certificate is Microsoft</span></span> |
| `ReportId` | <span data-ttu-id="0f31e-149">long</span><span class="sxs-lookup"><span data-stu-id="0f31e-149">long</span></span> | <span data-ttu-id="0f31e-150">Identificateur d’événement basé sur un compteur extensible.</span><span class="sxs-lookup"><span data-stu-id="0f31e-150">Event identifier based on a repeating counter.</span></span> <span data-ttu-id="0f31e-151">Pour identifier des événements uniques, cette colonne doit être utilisée conjointement avec les colonnes DeviceName et Timestamp.</span><span class="sxs-lookup"><span data-stu-id="0f31e-151">To identify unique events, this column must be used in conjunction with the DeviceName and Timestamp columns.</span></span> |


## <a name="related-topics"></a><span data-ttu-id="0f31e-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f31e-152">Related topics</span></span>
- [<span data-ttu-id="0f31e-153">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="0f31e-153">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="0f31e-154">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="0f31e-154">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="0f31e-155">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="0f31e-155">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
