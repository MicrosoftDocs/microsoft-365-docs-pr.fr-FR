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
description: Découvrez comment sélectionner et exporter du contenu à partir d’un jeu à réviser Advanced eDiscovery pour les présentations ou les avis externes.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 0752c5272d078e75e3bdbfb9cf7af7e49c78e65c
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51581016"
---
# <a name="export-documents-from-a-review-set-in-advanced-ediscovery"></a><span data-ttu-id="6ce29-103">Exporter des documents à partir d’un jeu à réviser dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="6ce29-103">Export documents from a review set in Advanced eDiscovery</span></span>

<span data-ttu-id="6ce29-104">L’exportation permet aux utilisateurs de personnaliser le contenu inclus dans le package de téléchargement lorsque vous exportez un document à partir d’un ensemble de révisions dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="6ce29-104">Export allows users to customize the content that is included in the download package when you export document from a review set in Advanced eDiscovery.</span></span>

<span data-ttu-id="6ce29-105">Pour exporter des documents à partir d’un jeu à réviser :</span><span class="sxs-lookup"><span data-stu-id="6ce29-105">To export documents from a review set:</span></span>

1. <span data-ttu-id="6ce29-106">Dans le Centre de conformité Microsoft 365, ouvrez le  cas Advanced eDiscovery, sélectionnez l’onglet Ensembles de révision, puis sélectionnez le jeu à réviser à exporter.</span><span class="sxs-lookup"><span data-stu-id="6ce29-106">In the Microsoft 365 compliance center, open the Advanced eDiscovery case, select the **Review sets** tab, and then select the review set that you want to export.</span></span>

2. <span data-ttu-id="6ce29-107">Dans le jeu à réviser, cliquez sur **Exporter l’action.**  >  </span><span class="sxs-lookup"><span data-stu-id="6ce29-107">In the review set, click **Action** > **Export**.</span></span>

   <span data-ttu-id="6ce29-108">L’outil Export affiche la page de présentation avec les paramètres permettant de configurer l’exportation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-108">The Export tool displays the flyout page with the settings to configure the export.</span></span> <span data-ttu-id="6ce29-109">Certaines options sont sélectionnées par défaut, mais vous pouvez les modifier.</span><span class="sxs-lookup"><span data-stu-id="6ce29-109">Some options are selected by default, but you can change these.</span></span> <span data-ttu-id="6ce29-110">Consultez la section suivante pour obtenir des descriptions des options d’exportation que vous pouvez configurer.</span><span class="sxs-lookup"><span data-stu-id="6ce29-110">See the following section for descriptions of the export options that you can configure.</span></span>

   ![Options de configuration pour l’exportation d’éléments à partir d’un jeu à réviser](../media/bcfc72c7-4a01-4697-9e16-2965b7f04fdb.png)

3. <span data-ttu-id="6ce29-112">Après avoir configuré l’exportation, cliquez sur **Exporter** pour démarrer le processus d’exportation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-112">After you configure the export, click **Export** to start the export process.</span></span> <span data-ttu-id="6ce29-113">Selon l’option que vous avez sélectionnée dans la section **Options** de sortie, vous pouvez accéder aux fichiers d’exportation en téléchargement direct ou dans le compte de stockage Azure de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-113">Depending on the option that you selected in **Output options** section, you can access the export files by direct download or in your organization's Azure Storage account.</span></span>

> [!NOTE]
> <span data-ttu-id="6ce29-114">Les travaux d’exportation sont conservés pendant toute la durée de vie du cas.</span><span class="sxs-lookup"><span data-stu-id="6ce29-114">Export jobs are retained for the life of the case.</span></span> <span data-ttu-id="6ce29-115">Toutefois, vous devez télécharger le contenu à partir d’une tâche d’exportation dans les 30 jours suivant la fin de la tâche d’exportation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-115">However, you must download the content from an export job within 30 days after the export job is complete.</span></span>

## <a name="export-options"></a><span data-ttu-id="6ce29-116">Options d’exportation</span><span class="sxs-lookup"><span data-stu-id="6ce29-116">Export options</span></span>

<span data-ttu-id="6ce29-117">Utilisez les options suivantes pour configurer l’exportation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-117">Use the following options to configure the export.</span></span>

- <span data-ttu-id="6ce29-118">**Nom d’exportation**: nom de la tâche d’exportation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-118">**Export name**: Name of the export job.</span></span>

- <span data-ttu-id="6ce29-119">**Description**: champ de texte libre pour ajouter une description.</span><span class="sxs-lookup"><span data-stu-id="6ce29-119">**Description**: Free-text field for you to add a description.</span></span>

- <span data-ttu-id="6ce29-120">**Exporter ces documents**</span><span class="sxs-lookup"><span data-stu-id="6ce29-120">**Export these documents**</span></span>

  - <span data-ttu-id="6ce29-121">**Documents sélectionnés uniquement**: cette option exporte uniquement les documents actuellement sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="6ce29-121">**Selected documents only**: This option exports only the documents that are currently selected.</span></span>
  
  - <span data-ttu-id="6ce29-122">**Tous les documents du jeu à réviser :** cette option exporte tous les documents du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="6ce29-122">**All documents in the review set**: This option exports all documents in the review set.</span></span>

- <span data-ttu-id="6ce29-123">**Métadonnées**</span><span class="sxs-lookup"><span data-stu-id="6ce29-123">**Metadata**</span></span>
  
  - <span data-ttu-id="6ce29-124">**Fichier de chargement**: ce fichier contient les métadonnées de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="6ce29-124">**Load file**: This file contains metadata for each file.</span></span> <span data-ttu-id="6ce29-125">Ce fichier peut généralement être ingéré par des outils eDiscovery tiers.</span><span class="sxs-lookup"><span data-stu-id="6ce29-125">This file can typically be ingested by third-party eDiscovery tools.</span></span> <span data-ttu-id="6ce29-126">Pour plus d’informations sur les champs inclus, voir Champs de métadonnées de document dans [Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md).</span><span class="sxs-lookup"><span data-stu-id="6ce29-126">For more information about what fields are included, see [Document metadata fields in Advanced eDiscovery](document-metadata-fields-in-Advanced-eDiscovery.md).</span></span>
  
  - <span data-ttu-id="6ce29-127">**Balises**: lorsqu’elles sont sélectionnées, les informations de marquage sont incluses dans le fichier de chargement.</span><span class="sxs-lookup"><span data-stu-id="6ce29-127">**Tags**: When selected, tagging information is included in the load file.</span></span>

- <span data-ttu-id="6ce29-128">**Content**</span><span class="sxs-lookup"><span data-stu-id="6ce29-128">**Content**</span></span>
  
  - <span data-ttu-id="6ce29-129">**Fichiers natifs**: cochez cette case pour inclure les fichiers natifs des documents dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="6ce29-129">**Native files**: Select this checkbox to include the native files of the documents in the review set.</span></span> <span data-ttu-id="6ce29-130">Si vous choisissez d’exporter des fichiers natifs, vous avez les options suivantes pour exporter des conversations de conversation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-130">If you choose to export native files, you have the following options for how export chat conversations.</span></span>
  
  - <span data-ttu-id="6ce29-131">**Options de conversation**</span><span class="sxs-lookup"><span data-stu-id="6ce29-131">**Conversation options**</span></span>

    - <span data-ttu-id="6ce29-132">**Fichiers de conversation**: cette option exporte les conversations de conversation reconstruites.</span><span class="sxs-lookup"><span data-stu-id="6ce29-132">**Conversation files**: This option exports reconstructed chat conversations.</span></span> <span data-ttu-id="6ce29-133">Ce format présente les conversations sous une forme semblable à ce que voient les utilisateurs dans l’application native.</span><span class="sxs-lookup"><span data-stu-id="6ce29-133">This format presents conversations in a form that resembles what users see in the native application.</span></span>

    - <span data-ttu-id="6ce29-134">**Messages de conversation** individuels : cette option exporte les fichiers de conversation d’origine tels qu’ils sont stockés dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6ce29-134">**Individual chat messages**: This option exports the original conversation files as they are stored in Microsoft 365.</span></span>

- <span data-ttu-id="6ce29-135">**Options**</span><span class="sxs-lookup"><span data-stu-id="6ce29-135">**Options**</span></span>

  - <span data-ttu-id="6ce29-136">**Fichiers texte**: - Cette option inclut les versions texte extraites des fichiers natifs dans l’exportation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-136">**Text files**: - This option includes the extracted text versions of native files in the export.</span></span>
  
  - <span data-ttu-id="6ce29-137">**Remplacez les natifs rédigés** par des fichiers PDF convertis : si des fichiers PDF rédigés sont générés lors de la révision, ces fichiers sont disponibles à l’exportation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-137">**Replace redacted natives with converted PDFs**: If redacted PDF files are generated during review, these files are available for export.</span></span> <span data-ttu-id="6ce29-138">Vous pouvez choisir d’exporter uniquement les fichiers natifs qui ont été rédigés (en ne sélectionnant pas cette option) ou vous pouvez sélectionner cette option pour exporter les fichiers PDF qui contiennent les actions.</span><span class="sxs-lookup"><span data-stu-id="6ce29-138">You can choose to export only the native files that were redacted (by not selecting this option) or you can select this option to export the PDF files that contain the actual redactions.</span></span>

- <span data-ttu-id="6ce29-139">**Options de sortie**: le contenu exporté peut être téléchargé directement via un navigateur web ou peut être envoyé à un compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="6ce29-139">**Output options**: Exported content is either available for download directly through a web browser or can be sent to an Azure Storage account.</span></span> <span data-ttu-id="6ce29-140">Les deux premières options permettent le téléchargement direct.</span><span class="sxs-lookup"><span data-stu-id="6ce29-140">The first two options enable direct download.</span></span>
  
  - <span data-ttu-id="6ce29-141">Fichiers libres et **fichiers PST (la** messagerie électronique est ajoutée aux fichiers PST lorsque cela est possible) : les fichiers sont exportés dans un format qui ressemble à la structure de répertoires d’origine visible par les utilisateurs dans leurs applications natives.</span><span class="sxs-lookup"><span data-stu-id="6ce29-141">**Loose files and PSTs (email is added to PSTs when possible)**: Files are exported in a format that resembles the original directory structure seen by users in their native applications.</span></span>  <span data-ttu-id="6ce29-142">Pour plus d’informations, voir la section Sur les fichiers libres et [la structure d’exportation PST.](#loose-files-and-pst-export-structure)</span><span class="sxs-lookup"><span data-stu-id="6ce29-142">For more information, see the [Loose files and PST export structure](#loose-files-and-pst-export-structure) section.</span></span>
  
  - <span data-ttu-id="6ce29-143">**Structure du répertoire condensé :** les fichiers sont exportés et inclus dans le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="6ce29-143">**Condensed directory structure**: Files are exported and included in the download.</span></span>
  
  - <span data-ttu-id="6ce29-144">**Structure de répertoire condensée exportée** vers votre compte de stockage Azure : les fichiers sont exportés vers le compte de stockage Azure de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-144">**Condensed directory structure exported to your Azure Storage account**: Files are exported to your organization's Azure Storage account.</span></span> <span data-ttu-id="6ce29-145">Pour cette option, vous devez fournir l’URL du conteneur dans votre compte de stockage Azure vers qui exporter les fichiers.</span><span class="sxs-lookup"><span data-stu-id="6ce29-145">For this option, you have to provide the URL for the container in your Azure Storage account to export the files to.</span></span> <span data-ttu-id="6ce29-146">Vous devez également fournir le jeton de signature d’accès partagé (SAS) pour votre compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="6ce29-146">You also have to provide the shared access signature (SAS) token for your Azure Storage account.</span></span> <span data-ttu-id="6ce29-147">Pour plus d’informations, [voir Exporter des documents dans une révision définie sur un compte de stockage Azure.](download-export-jobs.md)</span><span class="sxs-lookup"><span data-stu-id="6ce29-147">For more information, see [Export documents in a review set to an Azure Storage account](download-export-jobs.md).</span></span>

<span data-ttu-id="6ce29-148">Les sections suivantes décrivent la structure des dossiers pour les fichiers libres et les options de structure de répertoire condensé.</span><span class="sxs-lookup"><span data-stu-id="6ce29-148">The following sections describe the folder structure for loose files and condensed directory structure options.</span></span>

### <a name="loose-files-and-pst-export-structure"></a><span data-ttu-id="6ce29-149">Fichiers libres et structure d’exportation PST</span><span class="sxs-lookup"><span data-stu-id="6ce29-149">Loose files and PST export structure</span></span>

<span data-ttu-id="6ce29-150">Si vous sélectionnez cette option d’exportation, le contenu exporté est organisé dans la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="6ce29-150">If you select this export option, the exported content is organized in the following structure:</span></span>

- <span data-ttu-id="6ce29-151">Dossier racine : ce dossier dans le dossier nommé ExportName.zip</span><span class="sxs-lookup"><span data-stu-id="6ce29-151">Root folder: This folder in named ExportName.zip</span></span>
  
  - <span data-ttu-id="6ce29-152">Export_load_file.csv : fichier de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="6ce29-152">Export_load_file.csv: The metadata file.</span></span>
  
  - <span data-ttu-id="6ce29-153">Summary.csv : fichier récapitulatif qui contient également des statistiques d’exportation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-153">Summary.csv: A summary file that also contains export statistics.</span></span>
  
  - <span data-ttu-id="6ce29-154">Exchange : ce dossier contient tout le contenu d’Exchange au format de fichier natif.</span><span class="sxs-lookup"><span data-stu-id="6ce29-154">Exchange: This folder contains all content from Exchange in native file format.</span></span> <span data-ttu-id="6ce29-155">Les fichiers natifs sont remplacés par des fichiers PDF rédigés si vous avez sélectionné l’option Remplacer les natifs rédigés par des fichiers **pdf convertis.**</span><span class="sxs-lookup"><span data-stu-id="6ce29-155">Natives files are replaced with redacted PDFs if you selected the **Replace redacted natives with converted PDFs** option.</span></span>
  
  - <span data-ttu-id="6ce29-156">SharePoint : ce dossier contient tout le contenu natif de SharePoint dans un format de fichier natif.</span><span class="sxs-lookup"><span data-stu-id="6ce29-156">SharePoint: This folder contains all native content from SharePoint in a native file format.</span></span> <span data-ttu-id="6ce29-157">Les fichiers natifs sont remplacés par des fichiers PDF rédigés si vous avez sélectionné l’option Remplacer les natifs rédigés par des fichiers **pdf convertis.**</span><span class="sxs-lookup"><span data-stu-id="6ce29-157">Natives files are replaced with redacted PDFs if you selected the **Replace redacted natives with converted PDFs** option.</span></span>

### <a name="condensed-directory-structure"></a><span data-ttu-id="6ce29-158">Structure du répertoire condensé</span><span class="sxs-lookup"><span data-stu-id="6ce29-158">Condensed directory structure</span></span>

- <span data-ttu-id="6ce29-159">Dossier racine : ce dossier est nommé ExportName.zip</span><span class="sxs-lookup"><span data-stu-id="6ce29-159">Root folder: This folder is named ExportName.zip</span></span>
  
  - <span data-ttu-id="6ce29-160">Export_load_file.csv : fichier de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="6ce29-160">Export_load_file.csv: The metadata file.</span></span>
  
  - <span data-ttu-id="6ce29-161">Summary.txt : fichier récapitulatif qui contient également des statistiques d’exportation.</span><span class="sxs-lookup"><span data-stu-id="6ce29-161">Summary.txt: A summary file that also contains export statistics.</span></span>
  
  - <span data-ttu-id="6ce29-162">NativeFiles : ce dossier contient tous les fichiers natifs qui ont été exportés.</span><span class="sxs-lookup"><span data-stu-id="6ce29-162">NativeFiles: This folder contains all the native files that were exported.</span></span> <span data-ttu-id="6ce29-163">Si vous exportez des fichiers PDF rédigés, ils ne sont pas placés dans des fichiers PST.</span><span class="sxs-lookup"><span data-stu-id="6ce29-163">If you export redacted PDF files, they are not put in PST files.</span></span> <span data-ttu-id="6ce29-164">Au lieu de cela, ils sont ajoutés à un dossier séparé.</span><span class="sxs-lookup"><span data-stu-id="6ce29-164">Instead, they're added to a separated folder.</span></span>
  
  - <span data-ttu-id="6ce29-165">Error_files : ce dossier contient les fichiers d’erreur suivants, s’ils sont inclus dans l’exportation :</span><span class="sxs-lookup"><span data-stu-id="6ce29-165">Error_files: This folder contains the following error files, if they are included in the export:</span></span>

    - <span data-ttu-id="6ce29-166">ExtractionError : fichier CSV qui contient toutes les métadonnées disponibles des fichiers qui n’ont pas été correctement extraits des fichiers parents.</span><span class="sxs-lookup"><span data-stu-id="6ce29-166">ExtractionError: A CSV file that contains any available metadata of files that weren't properly extracted from parent files.</span></span>

    - <span data-ttu-id="6ce29-167">ProcessingError : ce fichier contient une liste de documents contenant des erreurs de traitement.</span><span class="sxs-lookup"><span data-stu-id="6ce29-167">ProcessingError: This file contains a list of documents with processing errors.</span></span> <span data-ttu-id="6ce29-168">Ce contenu est au niveau de l’élément, ce qui signifie que si une pièce jointe a entraîné une erreur de traitement, le message électronique qui contient la pièce jointe est inclus dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="6ce29-168">This content is item-level, meaning if an attachment resulted in a processing error, the email message that contains the attachment is included in this folder.</span></span>
  
  - <span data-ttu-id="6ce29-169">Extracted_text_files : ce dossier contient tous les fichiers texte extraits qui ont été générés lors du traitement.</span><span class="sxs-lookup"><span data-stu-id="6ce29-169">Extracted_text_files: This folder contains all of the extracted text files that were generated at processing.</span></span>
