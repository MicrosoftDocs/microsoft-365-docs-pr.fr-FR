---
title: Exporter des documents d’un jeu à réviser
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: b6f467f938ce14aacb9553b11d51dc63431ab409
ms.sourcegitcommit: 570ad1c7c334476ecec00dc355dfe52e8c2bb87b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2020
ms.locfileid: "41862074"
---
# <a name="export-documents-from-a-review-set"></a><span data-ttu-id="b0d2d-102">Exporter des documents d’un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="b0d2d-102">Export documents from a review set</span></span>

<span data-ttu-id="b0d2d-103">Vous pouvez exporter du contenu pour une présentation ou une révision externe à partir d’un ensemble de réexamens à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0d2d-103">You can export content for presentation or external review from a review set by one of the following methods:</span></span>

- [<span data-ttu-id="b0d2d-104">Télécharger des documents</span><span class="sxs-lookup"><span data-stu-id="b0d2d-104">Download documents</span></span>](#download-documents-from-a-review-set)
 
- [<span data-ttu-id="b0d2d-105">Exporter des documents</span><span class="sxs-lookup"><span data-stu-id="b0d2d-105">Export documents</span></span>](#export-documents-from-a-review-set)

## <a name="download-documents-from-a-review-set"></a><span data-ttu-id="b0d2d-106">Télécharger des documents à partir d’un jeu de révision</span><span class="sxs-lookup"><span data-stu-id="b0d2d-106">Download documents from a review set</span></span>

<span data-ttu-id="b0d2d-107">Le téléchargement offre un moyen simple de télécharger du contenu à partir d’un jeu de révision au format natif.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-107">Download offers a simple way to download content from a review set in Native format.</span></span> <span data-ttu-id="b0d2d-108">Il exploite les fonctionnalités de transfert de données du navigateur, de sorte qu’une invite de navigateur s’affiche une fois que le téléchargement est prêt.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-108">It leverages the browser’s data transfer features so a browser prompt will appear once a download is ready.</span></span> <span data-ttu-id="b0d2d-109">Les fichiers téléchargés à l’aide de cette méthode seront Zippés dans un fichier conteneur et seront des fichiers au niveau de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-109">Files downloaded using this method will be zipped into a container file and will be item level files.</span></span> <span data-ttu-id="b0d2d-110">Cela signifie que si vous sélectionnez une pièce jointe, vous recevrez automatiquement le courrier électronique avec la pièce jointe incluse.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-110">This means that if you select an attachment, you will automatically receive the email with the attachment included.</span></span> <span data-ttu-id="b0d2d-111">De même, si vous sélectionnez une feuille de calcul Excel incorporée dans un document Word, vous recevrez le document Word avec la feuille de calcul Excel incorporée.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-111">Similarly, if you select an excel spreadsheet that was embedded in a word document, you will receive the word document with the excel spreadsheet embedded.</span></span> <span data-ttu-id="b0d2d-112">Les éléments téléchargés conservent la dernière date de modification pouvant être affichée en tant que propriété de fichier.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-112">Downloaded items will preserve the last modified date which can be viewed as a file property.</span></span>

<span data-ttu-id="b0d2d-113">Pour télécharger du contenu à partir d’un jeu de révision, commencez par sélectionner les fichiers que vous souhaitez télécharger, puis sélectionnez « Télécharger » sous le menu actions.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-113">To download content from a review set, start by selecting the files you want to download then select “Download” under the Actions menu.</span></span>

![Capture d’écran d’une description d’ordinateur générée automatiquement](media/eDiscoDownload.png)

## <a name="export-documents-from-a-review-set"></a><span data-ttu-id="b0d2d-115">Exporter des documents d’un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="b0d2d-115">Export documents from a review set</span></span>

<span data-ttu-id="b0d2d-116">Exporter permet aux utilisateurs de personnaliser le contenu qui est inclus dans le package de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-116">Export allows users to customize the content that is included in the download package.</span></span> <span data-ttu-id="b0d2d-117">Il fournit une page de configuration avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="b0d2d-117">It provides a configuration page with the following settings:</span></span>

### <a name="metadata-file"></a><span data-ttu-id="b0d2d-118">Fichier de métadonnées</span><span class="sxs-lookup"><span data-stu-id="b0d2d-118">Metadata file</span></span>

<span data-ttu-id="b0d2d-119">Cela peut être considéré comme votre « fichier de chargement » qui contient les métadonnées associées aux fichiers que vous exportez.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-119">This can be considered your "load file" that contains metadata associated with the files you export.</span></span> <span data-ttu-id="b0d2d-120">Pour obtenir la liste des champs exportés disponibles dans le fichier de métadonnées, voir [document Metadata Fields in Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md).</span><span class="sxs-lookup"><span data-stu-id="b0d2d-120">For a list of exported fields available in the metadata file, see [Document metadata fields in Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md).</span></span> <span data-ttu-id="b0d2d-121">Ce fichier peut généralement être ingéré par des outils tiers.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-121">This file can typically be ingested by third-party tools.</span></span>

### <a name="tag-data"></a><span data-ttu-id="b0d2d-122">Données de balise</span><span class="sxs-lookup"><span data-stu-id="b0d2d-122">Tag data</span></span>

<span data-ttu-id="b0d2d-123">Ce contenu est ajouté en tant que champs dans le fichier de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-123">This content would be added as fields in the metadata file.</span></span> <span data-ttu-id="b0d2d-124">Elle contient toutes les informations de balise appliquées dans les ensembles de révision.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-124">It contains all of the tag information applied in review sets.</span></span>

### <a name="text-files"></a><span data-ttu-id="b0d2d-125">Fichiers texte</span><span class="sxs-lookup"><span data-stu-id="b0d2d-125">Text files</span></span>

<span data-ttu-id="b0d2d-126">Des fichiers texte peuvent être générés pour chaque fichier exporté à partir d’un ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-126">Text files can be generated for each file exported from a review set.</span></span> <span data-ttu-id="b0d2d-127">Souvent, ces fichiers sont requis par les partenaires de services dans le cadre de l’ingestion de données dans des outils tiers.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-127">Often times these files are required by service partners as part of ingesting data into third-party tools.</span></span>

### <a name="redacted-files"></a><span data-ttu-id="b0d2d-128">Fichiers biffés</span><span class="sxs-lookup"><span data-stu-id="b0d2d-128">Redacted files</span></span>

<span data-ttu-id="b0d2d-129">Si des fichiers au format PDF biffés sont générés lors de la révision, ces fichiers sont disponibles lors de l’exportation.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-129">If redacted PDF files are generated during review, these files are available during export.</span></span> <span data-ttu-id="b0d2d-130">Vous pouvez décider s’il faut exporter les fichiers natifs uniquement ou remplacer les fichiers natifs qui ont nécessité la biffure avec les fichiers PDF qui contiennent la Redactions réelle.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-130">You can decide whether to export native files only or to replace the native files that required redaction with the PDF files that contain the actual redactions.</span></span>

### <a name="export-location"></a><span data-ttu-id="b0d2d-131">Emplacement d’exportation</span><span class="sxs-lookup"><span data-stu-id="b0d2d-131">Export location</span></span>

<span data-ttu-id="b0d2d-132">Le contenu exporté est remis à un objet BLOB Azure fourni par Microsoft ou le BLOB d’un client peut être utilisé si les détails sont fournis lors de l’exportation.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-132">Exported content is delivered to either a Microsoft provided Azure blob or a customer’s blob can be used if the details are provided at export.</span></span>

### <a name="export-structure"></a><span data-ttu-id="b0d2d-133">Structure d’exportation</span><span class="sxs-lookup"><span data-stu-id="b0d2d-133">Export structure</span></span>

<span data-ttu-id="b0d2d-134">Lorsque le contenu est exporté à partir d’un ensemble de révision, le contenu est organisé dans la structure suivante.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-134">When content is exported from a review set, the content is organized in the following structure.</span></span>

  - <span data-ttu-id="b0d2d-135">Dossier racine – ID de téléchargement</span><span class="sxs-lookup"><span data-stu-id="b0d2d-135">Root folder – Download ID</span></span>
    
      - <span data-ttu-id="b0d2d-136">Export\_load\_file. csv = fichier de métadonnées</span><span class="sxs-lookup"><span data-stu-id="b0d2d-136">Export\_load\_file.csv = metadata file</span></span>
    
      - <span data-ttu-id="b0d2d-137">Summary. txt = un fichier résumé avec les statistiques d’exportation</span><span class="sxs-lookup"><span data-stu-id="b0d2d-137">Summary.txt = a summary file with export statistics</span></span>
    
      - <span data-ttu-id="b0d2d-138">Fichiers\_d’entrée\_ou natifs = contient tous les fichiers natifs</span><span class="sxs-lookup"><span data-stu-id="b0d2d-138">Input\_or native\_files = contains all native files</span></span>
    
      - <span data-ttu-id="b0d2d-139">Fichiers\_d’erreur = contient les fichiers d’erreur inclus dans l’exportation.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-139">Error\_files = contains any error files included in the export</span></span>
        
          - <span data-ttu-id="b0d2d-140">ExtractionError : CSV qui contient les métadonnées de fichiers disponibles qui n’ont pas été correctement extraites des fichiers parents</span><span class="sxs-lookup"><span data-stu-id="b0d2d-140">ExtractionError – a csv that contains any available metadata of files that were not properly extracted from parent files</span></span>
        
          - <span data-ttu-id="b0d2d-141">ProcessingError – contenu avec des erreurs de traitement.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-141">ProcessingError – content with processing errors.</span></span> <span data-ttu-id="b0d2d-142">Ce contenu est de niveau élément : si une pièce jointe a rencontré une erreur de traitement, le courrier électronique qui contient la pièce jointe est inclus dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-142">This content is item level meaning if an attachment experienced a processing error, the email that contains the attachment will be included in this folder.</span></span>
    
      - <span data-ttu-id="b0d2d-143">Fichiers\_texte\_extraits = contient tous les fichiers texte extraits générés lors du traitement.</span><span class="sxs-lookup"><span data-stu-id="b0d2d-143">Extracted\_text\_files = contains all of the extracted text files generated at processing.</span></span>