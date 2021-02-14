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
description: Découvrez comment sélectionner et exporter du contenu à partir d’un jeu à réviser pour des présentations ou des avis externes.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: b3be21d4c90c861c83acf612e9aadc373189f7ba
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285360"
---
# <a name="export-documents-from-a-review-set-in-advanced-ediscovery"></a><span data-ttu-id="9153d-103">Exporter des documents à partir d’un jeu à réviser dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9153d-103">Export documents from a review set in Advanced eDiscovery</span></span>

<span data-ttu-id="9153d-104">L’exportation permet aux utilisateurs de personnaliser le contenu inclus dans le package de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="9153d-104">Export allows users to customize the content that is included in the download package.</span></span> <span data-ttu-id="9153d-105">L’outil d’exportation fournit une page de configuration avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9153d-105">The Export tool provides a configuration page with the following settings:</span></span>

![Options d’exportation d’éléments à partir d’un jeu à réviser](../media/bcfc72c7-4a01-4697-9e16-2965b7f04fdb.png)

## <a name="export-options"></a><span data-ttu-id="9153d-107">Options d’exportation</span><span class="sxs-lookup"><span data-stu-id="9153d-107">Export options</span></span>

- <span data-ttu-id="9153d-108">Nom d’exportation : nom de la tâche d’exportation.</span><span class="sxs-lookup"><span data-stu-id="9153d-108">Export name: Name of the export job.</span></span>

- <span data-ttu-id="9153d-109">Description : champ de texte libre pour ajouter une description.</span><span class="sxs-lookup"><span data-stu-id="9153d-109">Description: Free-text field for you to add a description.</span></span>

- <span data-ttu-id="9153d-110">Exporte les documents ci-après :</span><span class="sxs-lookup"><span data-stu-id="9153d-110">Export these documents:</span></span>

  - <span data-ttu-id="9153d-111">Documents sélectionnés uniquement : exporte uniquement les documents actuellement sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="9153d-111">Selected documents only - Exports only the documents that are currently selected.</span></span>
  
  - <span data-ttu-id="9153d-112">Tous les documents du jeu à réviser : exporte tous les documents du jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="9153d-112">All documents in the review set - Exports all documents in the review set</span></span>

- <span data-ttu-id="9153d-113">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="9153d-113">Metadata</span></span>
  
  - <span data-ttu-id="9153d-114">Charger un fichier : ce fichier contient les métadonnées de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="9153d-114">Load file - This file contains metadata for each file.</span></span> <span data-ttu-id="9153d-115">voir [Champs de métadonnées de document dans Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md) pour plus d’informations sur les champs inclus.</span><span class="sxs-lookup"><span data-stu-id="9153d-115">see [Document metadata fields in Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md) for more information about what fields are included.</span></span> <span data-ttu-id="9153d-116">Ce fichier peut généralement être ingéré par des outils eDiscovery tiers.</span><span class="sxs-lookup"><span data-stu-id="9153d-116">This file can typically be ingested by third-party eDiscovery tools.</span></span>
  
  - <span data-ttu-id="9153d-117">Balises : lorsqu’elles sont sélectionnées, les informations de marquage sont incluses dans le fichier de chargement.</span><span class="sxs-lookup"><span data-stu-id="9153d-117">Tags - When selected, tagging information will be included in the load file.</span></span>

- <span data-ttu-id="9153d-118">Contenu</span><span class="sxs-lookup"><span data-stu-id="9153d-118">Content</span></span>
  
  - <span data-ttu-id="9153d-119">Fichiers natifs : cochez cette case pour inclure les fichiers natifs.</span><span class="sxs-lookup"><span data-stu-id="9153d-119">Native files - Select this checkbox to include the native files.</span></span>
  
  - <span data-ttu-id="9153d-120">Options de conversation</span><span class="sxs-lookup"><span data-stu-id="9153d-120">Conversation options</span></span>
    
    - <span data-ttu-id="9153d-121">Fichiers de conversation : exporter les messages de conversation reconstruits.</span><span class="sxs-lookup"><span data-stu-id="9153d-121">Conversation files - Export reconstructed chat messages.</span></span> <span data-ttu-id="9153d-122">Ce format présente les conversations sous une forme semblable à ce que voient les utilisateurs dans l’application native.</span><span class="sxs-lookup"><span data-stu-id="9153d-122">This format presents conversations in a form that resembles what users see in the native application.</span></span>
    
    - <span data-ttu-id="9153d-123">Messages de conversation individuels : exportez les fichiers de conversation d’origine tels qu’ils sont stockés dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9153d-123">Individual chat messages - Export the original conversation files as they are stored in Microsoft 365.</span></span>

- <span data-ttu-id="9153d-124">Options</span><span class="sxs-lookup"><span data-stu-id="9153d-124">Options</span></span>

  - <span data-ttu-id="9153d-125">Fichiers texte : inclure les versions texte extraites des fichiers natifs.</span><span class="sxs-lookup"><span data-stu-id="9153d-125">Text files - Include extracted text versions of native files.</span></span>
  
  - <span data-ttu-id="9153d-126">Remplacez les natifs rédigés par des fichiers PDF convertis : si des fichiers PDF rédigés sont générés au cours de la révision, ces fichiers peuvent être exportés.</span><span class="sxs-lookup"><span data-stu-id="9153d-126">Replace redacted natives with converted PDFs - If redacted PDF files are generated during review, these files are available for export.</span></span> <span data-ttu-id="9153d-127">Vous pouvez choisir d’exporter uniquement les fichiers natifs qui ont été rédigés (en ne sélectionnant pas cette option) ou vous pouvez sélectionner cette option pour exporter les fichiers PDF qui contiennent les actions.</span><span class="sxs-lookup"><span data-stu-id="9153d-127">You can choose to export only the native files that were redacted (by not selecting this option) or you can select this option to export the PDF files that contain the actual redactions.</span></span>

- <span data-ttu-id="9153d-128">Options de sortie (le contenu exporté peut être téléchargé directement via un navigateur web ou peut être envoyé à un compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="9153d-128">Output options (Exported content is either available for download directly through a web browser or can be sent to an Azure Storage account.</span></span> <span data-ttu-id="9153d-129">Les deux premières options activent le téléchargement direct.)</span><span class="sxs-lookup"><span data-stu-id="9153d-129">The first two options enable direct download.)</span></span>
  
  - <span data-ttu-id="9153d-130">Fichiers libres et fichiers PST (le courrier électronique est ajouté aux fichiers PST lorsque cela est possible) : les fichiers sont exportés dans un format qui ressemble à la structure de répertoires d’origine visible par les utilisateurs dans leurs applications natives.</span><span class="sxs-lookup"><span data-stu-id="9153d-130">Loose files and PSTs (email is added to PSTs when possible) - Files are exported in a format that resembles the original directory structure seen by users in their native applications.</span></span>  <span data-ttu-id="9153d-131">Pour plus d’informations, voir la section Sur les fichiers libres et [la structure d’exportation PST.](#loose-files-and-pst-export-structure)</span><span class="sxs-lookup"><span data-stu-id="9153d-131">For more information, see the [Loose files and PST export structure](#loose-files-and-pst-export-structure) section.</span></span>
  
  - <span data-ttu-id="9153d-132">Structure du répertoire condensé : les fichiers sont exportés et inclus dans le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="9153d-132">Condensed directory structure - Files are exported and included in the download.</span></span>
  
  - <span data-ttu-id="9153d-133">Structure de répertoire condensée exportée vers votre compte de stockage Azure : les fichiers sont exportés vers l’accès au stockage Azure de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9153d-133">Condensed directory structure exported to your Azure Storage account - Files are exported to your organization's Azure Storage accouunt.</span></span>

## <a name="loose-files-and-pst-export-structure"></a><span data-ttu-id="9153d-134">Fichiers libres et structure d’exportation PST</span><span class="sxs-lookup"><span data-stu-id="9153d-134">Loose files and PST export structure</span></span>

<span data-ttu-id="9153d-135">Si vous sélectionnez cette option d’exportation, le contenu exporté est organisé dans la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="9153d-135">If you select this export option, the exported content is organized in the following structure:</span></span>

- <span data-ttu-id="9153d-136">Dossier racine : ce dossier dans le dossier nommé ExportName.zip</span><span class="sxs-lookup"><span data-stu-id="9153d-136">Root folder – This folder in named ExportName.zip</span></span>
  
  - <span data-ttu-id="9153d-137">Export_load_file.csv - Fichier de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="9153d-137">Export_load_file.csv - Metadata file.</span></span>
  
  - <span data-ttu-id="9153d-138">Summary.csv : fichier récapitulatif qui contient également des statistiques d’exportation.</span><span class="sxs-lookup"><span data-stu-id="9153d-138">Summary.csv - A summary file that also contains export statistics.</span></span>
  
  - <span data-ttu-id="9153d-139">Exchange : ce dossier contient tout le contenu d’Exchange au format de fichier natif.</span><span class="sxs-lookup"><span data-stu-id="9153d-139">Exchange - This folder contains all content from Exchange in native file format.</span></span> <span data-ttu-id="9153d-140">Les fichiers natifs sont remplacés par des fichiers PDF rédigés si vous avez sélectionné l’option Remplacer les natifs rédigés par des fichiers **pdf convertis.**</span><span class="sxs-lookup"><span data-stu-id="9153d-140">Natives files are replaced with redacted PDFs if you selected the **Replace redacted natives with converted PDFs** option.</span></span>
  
  - <span data-ttu-id="9153d-141">SharePoint = Ce dossier contient tout le contenu natif de SharePoint dans un format de fichier natif.</span><span class="sxs-lookup"><span data-stu-id="9153d-141">SharePoint = This folder contains all native content from SharePoint in a native file format.</span></span> <span data-ttu-id="9153d-142">Les fichiers natifs sont remplacés par des fichiers PDF rédigés si vous avez sélectionné l’option Remplacer les natifs rédigés par des fichiers **PDF convertis.**</span><span class="sxs-lookup"><span data-stu-id="9153d-142">Natives files are replaced with redacted PDFs if you selected the **Replace redacted natives with converted PDFs** option.</span></span>

## <a name="condensed-directory-structure"></a><span data-ttu-id="9153d-143">Structure du répertoire condensé</span><span class="sxs-lookup"><span data-stu-id="9153d-143">Condensed directory structure</span></span>

- <span data-ttu-id="9153d-144">Dossier racine : ce dossier est nommé ExportName.zip</span><span class="sxs-lookup"><span data-stu-id="9153d-144">Root folder - This folder is named ExportName.zip</span></span>
  
  - <span data-ttu-id="9153d-145">Export_load_file.csv - Fichier de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="9153d-145">Export_load_file.csv - Metadata file.</span></span>
  
  - <span data-ttu-id="9153d-146">Summary.txt : fichier récapitulatif qui contient également des statistiques d’exportation.</span><span class="sxs-lookup"><span data-stu-id="9153d-146">Summary.txt - A summary file that also contains export statistics.</span></span>
  
  - <span data-ttu-id="9153d-147">Input_or_native_files - Ce dossier contient tous les fichiers natifs qui ont été exportés.</span><span class="sxs-lookup"><span data-stu-id="9153d-147">Input_or_native_files - This folder contains all the native files that were exported.</span></span> <span data-ttu-id="9153d-148">Si vous exportez des fichiers PDF rédigés, ils ne sont pas placés dans des fichiers PST.</span><span class="sxs-lookup"><span data-stu-id="9153d-148">If you export redacted PDF files, they are not put in PST files.</span></span> <span data-ttu-id="9153d-149">Au lieu de cela, ils sont ajoutés à un dossier séparé.</span><span class="sxs-lookup"><span data-stu-id="9153d-149">Instead, they're added to a separated folder.</span></span>
  
  - <span data-ttu-id="9153d-150">Error_files - Ce dossier contient les fichiers d’erreur suivants, s’ils sont inclus dans l’exportation :</span><span class="sxs-lookup"><span data-stu-id="9153d-150">Error_files - This folder contains the following error files, if they are included in the export:</span></span>
    
    - <span data-ttu-id="9153d-151">ExtractionError.</span><span class="sxs-lookup"><span data-stu-id="9153d-151">ExtractionError.</span></span> <span data-ttu-id="9153d-152">Un fichier CSV qui contient toutes les métadonnées disponibles des fichiers qui n’ont pas été correctement extraits des fichiers parents.</span><span class="sxs-lookup"><span data-stu-id="9153d-152">A CSV file that contains any available metadata of files that weren't properly extracted from parent files.</span></span>
    
    - <span data-ttu-id="9153d-153">ProcessingError : ce fichier contient une liste de documents avec des erreurs de traitement.</span><span class="sxs-lookup"><span data-stu-id="9153d-153">ProcessingError – This file contains a list of documents with processing errors.</span></span> <span data-ttu-id="9153d-154">Ce contenu est au niveau de l’élément, ce qui signifie que si une pièce jointe a entraîné une erreur de traitement, le message électronique qui contient la pièce jointe est inclus dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="9153d-154">This content is item-level, meaning if an attachment resulted in a processing error, the email message that contains the attachment is included in this folder.</span></span>
  
  - <span data-ttu-id="9153d-155">Extracted_text_files - Ce dossier contient tous les fichiers texte extraits qui ont été générés lors du traitement.</span><span class="sxs-lookup"><span data-stu-id="9153d-155">Extracted_text_files - This folder contains all of the extracted text files that were generated at processing.</span></span>

> [!NOTE]
> <span data-ttu-id="9153d-156">Les travaux d’exportation sont conservés pendant la durée de vie du cas et peuvent être téléchargés tant que le cas n’est pas supprimé.</span><span class="sxs-lookup"><span data-stu-id="9153d-156">Export jobs are retained for the life of the case and can be downloaded as long as the case isn't deleted.</span></span>
