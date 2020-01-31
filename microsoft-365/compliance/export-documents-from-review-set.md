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
ms.openlocfilehash: 0448082ce6dcbcd9d1cee52557a78b2d7913a034
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41588354"
---
# <a name="export-documents-from-a-review-set"></a><span data-ttu-id="ab580-102">Exporter des documents d’un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="ab580-102">Export documents from a review set</span></span>

<span data-ttu-id="ab580-103">Vous pouvez exporter du contenu pour une présentation ou une révision externe à partir d’un ensemble de réexamens à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ab580-103">You can export content for presentation or external review from a review set by one of the following methods:</span></span>

- [<span data-ttu-id="ab580-104">Télécharger des documents</span><span class="sxs-lookup"><span data-stu-id="ab580-104">Download documents</span></span>](#download-documents-from-a-review-set)
 
- [<span data-ttu-id="ab580-105">Exporter des documents</span><span class="sxs-lookup"><span data-stu-id="ab580-105">Export documents</span></span>](#export-documents-from-a-review-set)

## <a name="download-documents-from-a-review-set"></a><span data-ttu-id="ab580-106">Télécharger des documents à partir d’un jeu de révision</span><span class="sxs-lookup"><span data-stu-id="ab580-106">Download documents from a review set</span></span>

<span data-ttu-id="ab580-107">Le téléchargement offre un moyen simple de télécharger du contenu à partir d’un jeu de révision au format natif.</span><span class="sxs-lookup"><span data-stu-id="ab580-107">Download offers a simple way to download content from a review set in Native format.</span></span> <span data-ttu-id="ab580-108">Il exploite les fonctionnalités de transfert de données du navigateur, de sorte qu’une invite de navigateur s’affiche une fois que le téléchargement est prêt.</span><span class="sxs-lookup"><span data-stu-id="ab580-108">It leverages the browser’s data transfer features so a browser prompt will appear once a download is ready.</span></span> <span data-ttu-id="ab580-109">Les fichiers téléchargés à l’aide de cette méthode seront Zippés dans un fichier conteneur et seront des fichiers au niveau de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ab580-109">Files downloaded using this method will be zipped into a container file and will be item level files.</span></span> <span data-ttu-id="ab580-110">Cela signifie que si vous sélectionnez une pièce jointe, vous recevrez automatiquement le courrier électronique avec la pièce jointe incluse.</span><span class="sxs-lookup"><span data-stu-id="ab580-110">This means that if you select an attachment, you will automatically receive the email with the attachment included.</span></span> <span data-ttu-id="ab580-111">De même, si vous sélectionnez une feuille de calcul Excel incorporée dans un document Word, vous recevrez le document Word avec la feuille de calcul Excel incorporée.</span><span class="sxs-lookup"><span data-stu-id="ab580-111">Similarly, if you select an excel spreadsheet that was embedded in a word document, you will receive the word document with the excel spreadsheet embedded.</span></span> <span data-ttu-id="ab580-112">Les éléments téléchargés conservent la dernière date de modification pouvant être affichée en tant que propriété de fichier.</span><span class="sxs-lookup"><span data-stu-id="ab580-112">Downloaded items will preserve the last modified date which can be viewed as a file property.</span></span>

<span data-ttu-id="ab580-113">Pour télécharger du contenu à partir d’un jeu de révision, commencez par sélectionner les fichiers que vous souhaitez télécharger, puis sélectionnez « Télécharger » sous le menu actions.</span><span class="sxs-lookup"><span data-stu-id="ab580-113">To download content from a review set, start by selecting the files you want to download then select “Download” under the Actions menu.</span></span>

![Capture d’écran d’une description d’ordinateur générée automatiquement](media/eDiscoDownload.png)

## <a name="export-documents-from-a-review-set"></a><span data-ttu-id="ab580-115">Exporter des documents d’un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="ab580-115">Export documents from a review set</span></span>

<span data-ttu-id="ab580-116">Exporter permet aux utilisateurs de personnaliser le contenu qui est inclus dans le package de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="ab580-116">Export allows users to customize the content that is included in the download package.</span></span> <span data-ttu-id="ab580-117">Il fournit une page de configuration avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ab580-117">It provides a configuration page with the following settings:</span></span>

### <a name="metadata-file"></a><span data-ttu-id="ab580-118">Fichier de métadonnées</span><span class="sxs-lookup"><span data-stu-id="ab580-118">Metadata file</span></span>

<span data-ttu-id="ab580-119">Cela peut être considéré comme votre « fichier de chargement » qui contient les métadonnées associées aux fichiers que vous avez exportés.</span><span class="sxs-lookup"><span data-stu-id="ab580-119">This can be considered your “load file” that contains metadata associated with the files you exported.</span></span> <span data-ttu-id="ab580-120">Pour obtenir la liste des champs disponibles dans le fichier de métadonnées, consultez la rubrique \[Link\].</span><span class="sxs-lookup"><span data-stu-id="ab580-120">For a list of fields available in the metadata file, see \[link\].</span></span> <span data-ttu-id="ab580-121">Ce fichier peut généralement être ingéré<sup>par 3 outils</sup> tiers en aval.</span><span class="sxs-lookup"><span data-stu-id="ab580-121">This file can typically be ingested by 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="tag-data"></a><span data-ttu-id="ab580-122">Données de balise</span><span class="sxs-lookup"><span data-stu-id="ab580-122">Tag data</span></span>

<span data-ttu-id="ab580-123">Ce contenu est ajouté en tant que champs dans le fichier de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ab580-123">This content would be added as fields in the metadata file.</span></span> <span data-ttu-id="ab580-124">Elle contient toutes les informations de balise appliquées dans les ensembles de révision.</span><span class="sxs-lookup"><span data-stu-id="ab580-124">It contains all of the tag information applied in review sets.</span></span>

### <a name="text-files"></a><span data-ttu-id="ab580-125">Fichiers texte</span><span class="sxs-lookup"><span data-stu-id="ab580-125">Text files</span></span>

<span data-ttu-id="ab580-126">Des fichiers texte peuvent être générés pour chaque fichier exporté à partir d’un ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="ab580-126">Text files can be generated for each file exported from a review set.</span></span> <span data-ttu-id="ab580-127">Ces fichiers sont souvent requis par les partenaires de services dans le cadre de l’ingestion de données<sup>dans 3 outils</sup> tiers en aval.</span><span class="sxs-lookup"><span data-stu-id="ab580-127">Often times these files are required by service partners as part of ingesting data into 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="redacted-files"></a><span data-ttu-id="ab580-128">Fichiers biffés</span><span class="sxs-lookup"><span data-stu-id="ab580-128">Redacted files</span></span>

<span data-ttu-id="ab580-129">Si des fichiers PDF biffés sont générés lors de la révision, ces fichiers sont disponibles lors de l’exportation.</span><span class="sxs-lookup"><span data-stu-id="ab580-129">If redacted PDFs are generated during review, these files are available during export.</span></span> <span data-ttu-id="ab580-130">Les utilisateurs peuvent décider s’il convient d’exporter les fichiers natifs uniquement ou de remplacer les fichiers natifs dont le Redactions avec le fichier PDF est gravé.</span><span class="sxs-lookup"><span data-stu-id="ab580-130">Users can decide whether to export native files only or to replace natives that have redactions with the burned in PDFs.</span></span>

### <a name="export-location"></a><span data-ttu-id="ab580-131">Emplacement de l’exportation</span><span class="sxs-lookup"><span data-stu-id="ab580-131">Export Location</span></span>

<span data-ttu-id="ab580-132">Le contenu exporté est remis à un objet BLOB Azure fourni par Microsoft ou le BLOB d’un client peut être utilisé si les détails sont fournis lors de l’exportation.</span><span class="sxs-lookup"><span data-stu-id="ab580-132">Exported content is delivered to either a Microsoft provided Azure blob or a customer’s blob can be used if the details are provided at export.</span></span>

### <a name="export-structure"></a><span data-ttu-id="ab580-133">Structure d’exportation</span><span class="sxs-lookup"><span data-stu-id="ab580-133">Export Structure</span></span>

<span data-ttu-id="ab580-134">Lorsque le contenu est exporté à partir d’un ensemble de révision, le contenu est organisé dans la structure suivante.</span><span class="sxs-lookup"><span data-stu-id="ab580-134">When content is exported from a review set, the content is organized in the following structure.</span></span>

  - <span data-ttu-id="ab580-135">Dossier racine – ID de téléchargement</span><span class="sxs-lookup"><span data-stu-id="ab580-135">Root folder – Download ID</span></span>
    
      - <span data-ttu-id="ab580-136">Export\_load\_file. csv = fichier de métadonnées</span><span class="sxs-lookup"><span data-stu-id="ab580-136">Export\_load\_file.csv = metadata file</span></span>
    
      - <span data-ttu-id="ab580-137">Summary. txt = un fichier résumé avec les statistiques d’exportation</span><span class="sxs-lookup"><span data-stu-id="ab580-137">Summary.txt = a summary file with export statistics</span></span>
    
      - <span data-ttu-id="ab580-138">Fichiers\_d’entrée\_ou natifs = contient tous les fichiers natifs</span><span class="sxs-lookup"><span data-stu-id="ab580-138">Input\_or native\_files = contains all native files</span></span>
    
      - <span data-ttu-id="ab580-139">Fichiers\_d’erreur = contient les fichiers d’erreur inclus dans l’exportation.</span><span class="sxs-lookup"><span data-stu-id="ab580-139">Error\_files = contains any error files included in the export</span></span>
        
          - <span data-ttu-id="ab580-140">ExtractionError : CSV qui contient les métadonnées de fichiers disponibles qui n’ont pas été correctement extraites des fichiers parents</span><span class="sxs-lookup"><span data-stu-id="ab580-140">ExtractionError – a csv that contains any available metadata of files that were not properly extracted from parent files</span></span>
        
          - <span data-ttu-id="ab580-141">ProcessingError – contenu avec des erreurs de traitement.</span><span class="sxs-lookup"><span data-stu-id="ab580-141">ProcessingError – content with processing errors.</span></span> <span data-ttu-id="ab580-142">Ce contenu est de niveau élément : si une pièce jointe a rencontré une erreur de traitement, le courrier électronique qui contient la pièce jointe est inclus dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="ab580-142">This content is item level meaning if an attachment experienced a processing error, the email that contains the attachment will be included in this folder.</span></span>
    
      - <span data-ttu-id="ab580-143">Fichiers\_texte\_extraits = contient tous les fichiers texte extraits générés lors du traitement.</span><span class="sxs-lookup"><span data-stu-id="ab580-143">Extracted\_text\_files = contains all of the extracted text files generated at processing.</span></span>