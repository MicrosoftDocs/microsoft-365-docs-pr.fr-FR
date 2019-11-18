---
title: Télécharger l’exportation des travaux
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
description: Installez et utilisez l’Explorateur de stockage Azure pour télécharger des documents qui ont été exportés à partir d’un jeu de vérification dans Advanced eDiscovery.
ms.openlocfilehash: 412ec48865c6cb7e511e3f6068fe02d87a99f831
ms.sourcegitcommit: 1d376287f6c1bf5174873e89ed4bf7bb15bc13f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38685931"
---
# <a name="download-export-jobs"></a><span data-ttu-id="d4f1a-103">Télécharger l’exportation des travaux</span><span class="sxs-lookup"><span data-stu-id="d4f1a-103">Download export jobs</span></span>

<span data-ttu-id="d4f1a-104">Lorsque vous exportez des documents à partir d’un jeu de réexamen dans un cas avancé de découverte électronique, les documents sont téléchargés vers un emplacement de stockage Azure fourni par Microsoft ou vers un emplacement de stockage Azure géré par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-104">When you export documents from a review set in an Advanced eDiscovery case, the documents are uploaded to a Microsoft-provided Azure Storage location or to an Azure Storage location managed by your organization.</span></span> <span data-ttu-id="d4f1a-105">Le type d’emplacement de stockage Azure utilisé dépend de l’option sélectionnée lors de l’exportation des documents.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-105">The type of Azure Storage location used depends on which option was selected when the documents were exported.</span></span> 

<span data-ttu-id="d4f1a-106">Cet article fournit des instructions sur l’utilisation de l’Explorateur de stockage Microsoft Azure pour se connecter à un emplacement de stockage Azure afin de parcourir et télécharger les documents exportés.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-106">This article provides instructions for how to use the Microsoft Azure Storage Explorer to connect to an Azure Storage location to browse and download the exported documents.</span></span> <span data-ttu-id="d4f1a-107">Pour plus d’informations sur l’Explorateur de stockage Azure, voir [démarrage rapide : utiliser l’Explorateur de stockage Azure](https://docs.microsoft.com/azure/storage/blobs/storage-quickstart-blobs-storage-explorer).</span><span class="sxs-lookup"><span data-stu-id="d4f1a-107">For more information about Azure Storage Explorer, see [Quickstart: Use Azure Storage Explorer](https://docs.microsoft.com/azure/storage/blobs/storage-quickstart-blobs-storage-explorer).</span></span>

## <a name="step-1-install-the-azure-storage-explorer"></a><span data-ttu-id="d4f1a-108">Étape 1 : installer l’Explorateur de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="d4f1a-108">Step 1: Install the Azure Storage Explorer</span></span>

<span data-ttu-id="d4f1a-109">La première étape consiste à télécharger et à installer l’Explorateur de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-109">The first step is to download and install the Azure Storage Explorer.</span></span> <span data-ttu-id="d4f1a-110">Pour obtenir des instructions, consultez la rubrique [outil Explorateur de stockage Azure](https://go.microsoft.com/fwlink/p/?LinkId=544842).</span><span class="sxs-lookup"><span data-stu-id="d4f1a-110">For instructions, see [Azure Storage Explorer tool](https://go.microsoft.com/fwlink/p/?LinkId=544842).</span></span> <span data-ttu-id="d4f1a-111">Utilisez cet outil pour vous connecter aux documents exportés et les télécharger à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-111">You use this tool to connect to and download the exported documents in Step 3.</span></span>

## <a name="step-2-obtain-the-sas-url-from-the-export-job"></a><span data-ttu-id="d4f1a-112">Étape 2 : obtenir l’URL SAS à partir de la tâche d’exportation</span><span class="sxs-lookup"><span data-stu-id="d4f1a-112">Step 2: Obtain the SAS URL from the export job</span></span>

<span data-ttu-id="d4f1a-113">L’étape suivante consiste à obtenir l’URL de signature d’accès partagé (SAS) générée lorsque vous avez créé le travail d’exportation pour [exporter des documents à partir d’un jeu de révision](export-documents-from-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="d4f1a-113">The next step is to obtain the shared access signature (SAS) URL that's generated when you created the export job to [export documents from a review set](export-documents-from-review-set.md).</span></span> <span data-ttu-id="d4f1a-114">Vous pouvez copier l’URL SAS des documents téléchargés vers un emplacement de stockage Azure fourni par Microsoft ou un emplacement de stockage Azure géré par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-114">You can copy the SAS URL for documents that are uploaded to a Microsoft-provided Azure Storage location or an Azure Storage location managed by your organization.</span></span> <span data-ttu-id="d4f1a-115">Dans les deux cas, vous utilisez l’URL SAS pour vous connecter à l’emplacement de stockage Azure à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-115">In either case, you use the SAS URL to connect to the Azure Storage location in Step 3.</span></span>

1. <span data-ttu-id="d4f1a-116">Sur la page **Advanced eDiscovery** , accédez au cas, puis cliquez sur l’onglet **exports** .</span><span class="sxs-lookup"><span data-stu-id="d4f1a-116">On the **Advanced eDiscovery** page, go to the case, and then click the **Exports** tab.</span></span>

2. <span data-ttu-id="d4f1a-117">Sous l’onglet **exportations** , cliquez sur le travail d’exportation que vous souhaitez télécharger.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-117">On the **Exports** tab, click the export job that you want to download.</span></span>

3. <span data-ttu-id="d4f1a-118">Sur la page de menu volant, sous **emplacements**, copiez l’URL de la version SAS affichée.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-118">On the flyout page, under **Locations**, copy the SAS URL that's displayed.</span></span> <span data-ttu-id="d4f1a-119">Si nécessaire, vous pouvez l’enregistrer dans un fichier pour pouvoir y accéder à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-119">If necessary, you can save it to a file so you can access it in Step 3.</span></span>
 
   ![Copier l’URL SAS affichée sous locations](./media/eDiscoExportJob.png)

## <a name="step-3-connect-to-the-azure-storage-location"></a><span data-ttu-id="d4f1a-121">Étape 3 : Connectez-vous à l’emplacement de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="d4f1a-121">Step 3: Connect to the Azure Storage location</span></span>

<span data-ttu-id="d4f1a-122">La dernière étape consiste à utiliser l’Explorateur de stockage Azure et l’URL SAS pour se connecter à l’emplacement de stockage Azure et télécharger les documents que vous avez exportés vers un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-122">The final step is to use the Azure Storage Explorer and the SAS URL to connect to the Azure Storage location and download the documents that you exported to a local computer.</span></span>

1.  <span data-ttu-id="d4f1a-123">Ouvrez l’Explorateur de stockage Azure que vous avez installé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-123">Open the Azure Storage Explorer that you installed in Step 1.</span></span>

2. <span data-ttu-id="d4f1a-124">Cliquez sur l’icône **Ajouter un compte** .</span><span class="sxs-lookup"><span data-stu-id="d4f1a-124">Click the **Add account** icon.</span></span> <span data-ttu-id="d4f1a-125">Vous pouvez également cliquer avec le bouton droit sur **comptes de stockage**.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-125">Alternatively, you can right-click **Storage Accounts**.</span></span>

   ![Cliquez sur l’icône Ajouter un compte](./media/AzureStorageConnect.png)

3.  <span data-ttu-id="d4f1a-127">Sur la page **connexion à Azure Storage** , cliquez sur **utiliser un URI de signature d’accès partagé (SAS)** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-127">On the **Connect to Azure Storage** page, click **Use a shared access signature (SAS) URI** and then click **Next**.</span></span>

    ![Cliquez sur utiliser un URI de signature d’accès partagé (SAS), puis sur suivant.](./media/AzureStorageConnect2.png)

4.  <span data-ttu-id="d4f1a-129">Dans la page **attacher avec l’URI SAS** , cliquez dans la zone URI, puis collez l’URL SAS que vous avez obtenue à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-129">On the **Attach with SAS URI** page, click in the URI box, and then paste the SAS URL that you obtained in Step 2.</span></span> 

    ![Coller l’URL SAS dans la zone URI](./media/AzureStorageConnect3.png)

    <span data-ttu-id="d4f1a-131">Notez qu’une partie de l’URL SAS apparaît dans la zone **nom d’affichage** .</span><span class="sxs-lookup"><span data-stu-id="d4f1a-131">Notice that a portion of the SAS URL is displayed in the **Display name** box.</span></span> <span data-ttu-id="d4f1a-132">Il sera utilisé comme nom d’affichage du conteneur créé sous les **comptes de stockage** une fois que vous vous êtes connecté à l’emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-132">This will be used as the display name of the container that's created under the **Storage accounts** after you connect to the storage location.</span></span> <span data-ttu-id="d4f1a-133">Ce nom se compose de l’ID du cas de découverte électronique avancée, de et d’un identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-133">This name consists of the ID of the Advanced eDiscovery case is from and a unique identifier.</span></span> <span data-ttu-id="d4f1a-134">Vous pouvez conserver le nom d’affichage par défaut ou le modifier.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-134">You can keep the default display name or change it.</span></span> <span data-ttu-id="d4f1a-135">Si vous le modifiez, le nom d’affichage doit être unique.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-135">If you change it, the display name must be unique.</span></span>

5.  <span data-ttu-id="d4f1a-136">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-136">Click **Next**.</span></span>

    <span data-ttu-id="d4f1a-137">La page **Résumé de connexion** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-137">The **Connection summary** page is displayed.</span></span>
   
    ![Cliquez sur se connecter sur la page de résumé de connexion pour vous connecter à l’emplacement de stockage Azure.](./media/AzureStorageConnect4.png)

6. <span data-ttu-id="d4f1a-139">Sur la page **Résumé de connexion** , passez en revue les informations de connexion, puis cliquez sur **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-139">On the **Connection summary** page, review the connection information, and then click **Connect**.</span></span> 

    <span data-ttu-id="d4f1a-140">Le nœud **conteneurs BLOB** (sous **comptes** > **de stockage (conteneurs associés)** \> est ouvert.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-140">The **Blob containers** node (under **Storage Accounts** > **(Attached Containers)** \> is opened.</span></span> 

    ![Exporter des travaux dans le nœud conteneurs d’objets BLOB](./media/AzureStorageConnect5.png)

    <span data-ttu-id="d4f1a-142">Il contient un conteneur nommé avec le nom d’affichage de l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-142">It contains a container named with the display name from step 4.</span></span> <span data-ttu-id="d4f1a-143">Ce conteneur contient un dossier pour chaque tâche d’exportation que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-143">This container contains a folder for each export job that you've created.</span></span> <span data-ttu-id="d4f1a-144">Ces dossiers sont nommés avec un ID correspondant à l’ID de la tâche d’exportation.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-144">These folders are named with an ID that corresponds to the ID of the export job.</span></span> <span data-ttu-id="d4f1a-145">Vous trouverez ces ID d’exportation (et le nom de l’exportation) sous **informations de support** sur la page de menu volant pour chaque tâche **de préparation des données pour l’exportation** , dans l’onglet **travaux** .</span><span class="sxs-lookup"><span data-stu-id="d4f1a-145">You can find these export IDs (and the name of the export) under **Support information** on the flyout page for each **Preparing data for export** job listed on the **Jobs** tab.</span></span>

7. <span data-ttu-id="d4f1a-146">Double-cliquez sur le dossier exporter le travail pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-146">Double-click the export job folder to open it.</span></span>

   <span data-ttu-id="d4f1a-147">Une liste des dossiers et des rapports d’exportation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-147">A list of folders and export reports is displayed.</span></span>
   
    ![Le dossier d’exportation contient des fichiers exportés et des rapports d’exportation](./media/AzureStorageConnect6.png)

   <span data-ttu-id="d4f1a-149">Le dossier exporter le travail contient les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-149">The export job folder contains the following items.</span></span> <span data-ttu-id="d4f1a-150">Les éléments réels dans le dossier d’exportation sont déterminés par les options d’exportation configurées lors de la création du travail d’exportation.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-150">The actual items in the export folder are determined by the export options configured when the export job was created.</span></span> <span data-ttu-id="d4f1a-151">Pour plus d’informations, consultez [la rubrique exporter des documents à partir d’un jeu de révision](export-documents-from-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="d4f1a-151">For more information, see [Export documents from a review set](export-documents-from-review-set.md).</span></span>

    - <span data-ttu-id="d4f1a-152">Export_load_file. csv : ce fichier CSV est un rapport d’exportation détaillé qui contient des informations sur chaque document exporté.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-152">Export_load_file.csv: This CSV file is a detail export report that contains information about each exported document.</span></span> <span data-ttu-id="d4f1a-153">Le fichier se compose d’une colonne pour chaque propriété de métadonnées d’un document.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-153">The file consists of a column for each metadata property for a document.</span></span> <span data-ttu-id="d4f1a-154">Pour obtenir la liste et la description des métadonnées incluses dans ce rapport, reportez-vous à la colonne **nom du champ exporté** du tableau dans les [champs de métadonnées de document dans Advanced eDiscovery](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="d4f1a-154">For a list and description of the metadata that's included in this report, see the **Exported field name** column in the table in [Document metadata fields in Advanced eDiscovery](document-metadata-fields.md).</span></span>
    
    - <span data-ttu-id="d4f1a-155">Summary. txt : fichier texte contenant un résumé de l’exportation, y compris les statistiques d’exportation.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-155">Summary.txt: A text file that contains a summary of the export including export statistics.</span></span>
    
    - <span data-ttu-id="d4f1a-156">Extracted_text_files : ce dossier contient une version de fichier texte de chaque document exporté.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-156">Extracted_text_files: This folder contains a text file version of each exported document.</span></span>
     
    - <span data-ttu-id="d4f1a-157">NativeFiles : ce dossier contient une version de fichier native de chaque document exporté.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-157">NativeFiles: This folder contains a native file version of each exported document.</span></span>
    
    - <span data-ttu-id="d4f1a-158">Error_files : ce dossier inclut les éléments suivants lorsque le travail d’exportation contient des fichiers d’erreur :</span><span class="sxs-lookup"><span data-stu-id="d4f1a-158">Error_files: This folder includes the following items when the export job contains any error files:</span></span> 
        
      - <span data-ttu-id="d4f1a-159">ExtractionError. csv : ce fichier CSV contient les métadonnées disponibles pour les fichiers qui n’ont pas été correctement extraits de leur élément parent.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-159">ExtractionError.csv: This CSV file contains the available metadata for files that weren't properly extracted from their parent item.</span></span>
        
      - <span data-ttu-id="d4f1a-160">ProcessingError : ce dossier contient des documents contenant des erreurs de traitement.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-160">ProcessingError: This folder contains documents with processing errors.</span></span> <span data-ttu-id="d4f1a-161">Ce contenu se trouve au niveau de l’élément, ce qui signifie qu’en cas d’erreur de traitement d’une pièce jointe, le document contenant la pièce jointe est également inclus dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-161">This content is at an item level, which means if an attachment had a processing error, the document that contains the attachment will also be included in this folder.</span></span>
 
8. <span data-ttu-id="d4f1a-162">Pour exporter tout le contenu de l’exportation, sélectionnez le dossier exporter, puis cliquez sur **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-162">To export all contents in the export, select the export folder, and then click **Download**.</span></span>

9. <span data-ttu-id="d4f1a-163">Spécifiez l’emplacement où vous souhaitez télécharger les fichiers exportés, puis cliquez sur Sélectionner un dossier.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-163">Specify the location where you want to download the exported files, and then click Select folder.</span></span>

    <span data-ttu-id="d4f1a-164">L’Explorateur de stockage Azure démarre le processus d’exportation.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-164">The Azure Storage Explorer starts the export process.</span></span> <span data-ttu-id="d4f1a-165">L’état de téléchargement des éléments exportés est affiché dans le volet **activités** .</span><span class="sxs-lookup"><span data-stu-id="d4f1a-165">The status of the downloading the exported items is displayed in the **Activities** pane.</span></span> <span data-ttu-id="d4f1a-166">Un message s’affiche lorsque le téléchargement est terminé.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-166">A message is displayed when the download is finished.</span></span>

    ![Un message s’affiche lorsque le téléchargement est terminé.](./media/AzureStorageConnect8.png)

> [!NOTE]
> <span data-ttu-id="d4f1a-168">Au lieu de télécharger l’intégralité du travail d’exportation, vous pouvez sélectionner des éléments spécifiques à télécharger.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-168">Instead of downloading the entire export job, you can select specific items to download.</span></span> <span data-ttu-id="d4f1a-169">Et au lieu de télécharger des éléments, vous pouvez double-cliquer sur un élément pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="d4f1a-169">And instead of downloading items, you can double-click an item to view it.</span></span>