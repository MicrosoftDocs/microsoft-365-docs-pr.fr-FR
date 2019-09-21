---
title: Afficher les résultats du module de processus dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: 'Découvrez comment trouver les résultats d’un module de processus exécuté dans Office 365 Advanced eDiscovery, y compris l’état de la tâche et le résumé des processus.  '
ms.openlocfilehash: 4bbdbf68f71e3459ff2ddcd8ba3fb33e52f16825
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079883"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="d8b06-103">Afficher les résultats du module de processus dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d8b06-103">View Process module results in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="d8b06-104">Une fois le **processus** de **préparation** \> initié, vous pouvez afficher l’avancement et les résultats.</span><span class="sxs-lookup"><span data-stu-id="d8b06-104">After **Prepare** \> **Process** is initiated, you can view progress and results.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d8b06-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="d8b06-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="process-task-status"></a><span data-ttu-id="d8b06-107">État de tâche de processus</span><span class="sxs-lookup"><span data-stu-id="d8b06-107">Process task status</span></span>

<span data-ttu-id="d8b06-108">Dans **préparer** \> les **résultats**du **processus** \> , la page affiche l’état actuel (si le processus est en cours d’exécution) ou l’état de la dernière tâche d’État du processus, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="d8b06-108">In **Prepare** \> **Process** \> **Results**, the page shows the current status (if Process is currently running) or the last Process status task status as shown in the following example.</span></span>
  
![État de tâche du module de processus](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
<span data-ttu-id="d8b06-110">Les tâches affichées peuvent varier en fonction des options de processus sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="d8b06-110">The displayed tasks may vary depending on the Process options selected.</span></span> 
  
- <span data-ttu-id="d8b06-111">**Inventory**: Advanced eDiscovery effectue une itération dans tous les fichiers sélectionnés pour le processus et effectue une collecte de données de base.</span><span class="sxs-lookup"><span data-stu-id="d8b06-111">**Inventory**: Advanced eDiscovery iterates through all files selected for Process and performs basic data collection.</span></span>
    
- <span data-ttu-id="d8b06-112">**Calculer les signatures**: calcule les signatures numériques MD5.</span><span class="sxs-lookup"><span data-stu-id="d8b06-112">**Calculate signatures**: Calculates the MD5 digital signatures.</span></span>
    
- <span data-ttu-id="d8b06-113">**Extraction de composés**: extrait les fichiers internes ou contenus de manière récursive des fichiers composés (par exemple, PST, zip, MSG).</span><span class="sxs-lookup"><span data-stu-id="d8b06-113">**Compounds extraction**: Extracts inner or contained files recursively from compound files (for example, PST, ZIP, MSG).</span></span> <span data-ttu-id="d8b06-114">Les fichiers extraits sont stockés dans le dossier case du cas.</span><span class="sxs-lookup"><span data-stu-id="d8b06-114">Extracted files are stored in the case folder of the case.</span></span>
    
- <span data-ttu-id="d8b06-115">**Synchronisation de la base de données**: processus de base de données interne.</span><span class="sxs-lookup"><span data-stu-id="d8b06-115">**Synchronizing database**: Internal database process.</span></span>
    
- <span data-ttu-id="d8b06-116">**Copie**de fichiers : copie les fichiers du processus.</span><span class="sxs-lookup"><span data-stu-id="d8b06-116">**File copy**: Copies Process files.</span></span> <span data-ttu-id="d8b06-117">Cette tâche est toujours affichée, même lorsque l’option copie avancée des fichiers est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d8b06-117">This task is always displayed, even when the advanced Copy files option is selected.</span></span>
    
- <span data-ttu-id="d8b06-118">**Extraction de texte**: lorsqu’il existe des fichiers natifs, Advanced eDiscovery extrait le texte de ces fichiers à l’aide de DTSearch.</span><span class="sxs-lookup"><span data-stu-id="d8b06-118">**Text extraction**: When there are native files, Advanced eDiscovery extracts text from these files using DTSearch.</span></span> <span data-ttu-id="d8b06-119">Le texte extrait de ces fichiers est stocké sous forme de fichiers texte dans le dossier case.</span><span class="sxs-lookup"><span data-stu-id="d8b06-119">The extracted text of these files is stored as text files in the case folder.</span></span>
    
- <span data-ttu-id="d8b06-120">**Mise à jour des métadonnées**: traite les métadonnées chargées.</span><span class="sxs-lookup"><span data-stu-id="d8b06-120">**Updating metadata**: Processes the loaded metadata.</span></span> 
    
- <span data-ttu-id="d8b06-121">**Finalisation**: traitement interne qui finalise les données des fichiers de casse chargés (par exemple, identifier les fichiers d’erreur et de réussite).</span><span class="sxs-lookup"><span data-stu-id="d8b06-121">**Finalizing**: Internal processing that finalizes data of loaded case files (for example, identify error and success files).</span></span> 
    
<span data-ttu-id="d8b06-122">État de la tâche : affiché une fois la tâche terminée.</span><span class="sxs-lookup"><span data-stu-id="d8b06-122">Task status: Displayed after task completion.</span></span> <span data-ttu-id="d8b06-123">Pendant l’exécution des tâches, la durée de l’exécution s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d8b06-123">While tasks are running, run duration is displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d8b06-124">Les tâches achevées peuvent également inclure des totaux pour les fichiers ayant terminé le traitement ou des fichiers contenant des erreurs.</span><span class="sxs-lookup"><span data-stu-id="d8b06-124">Completed tasks may also include totals for files that completed processing or files with errors.</span></span> 
  
> [!TIP]
> <span data-ttu-id="d8b06-125">« Annuler » fournit une option de restauration pour arrêter l’exécution du processus, puis restaurer le remplissage de données précédent ou les données traitées enregistrées.</span><span class="sxs-lookup"><span data-stu-id="d8b06-125">"Cancel" provides a rollback option to stop Process execution and then roll back to the previous data population or saved processed data.</span></span> <span data-ttu-id="d8b06-126">La restauration efface toutes les données traitées.</span><span class="sxs-lookup"><span data-stu-id="d8b06-126">Rollback clears all processed data.</span></span> <span data-ttu-id="d8b06-127">Si vous ne souhaitez pas que les données traitées soient perdues (par exemple, si vous envisagez de recharger ces fichiers), sélectionnez l’option « Annuler » dans cette fenêtre pour choisir de ne pas restaurer.</span><span class="sxs-lookup"><span data-stu-id="d8b06-127">If you do not want the processed data to be lost (for example, you plan to reload these files), select the "Cancel" option in this window to choose not to roll back.</span></span> 
  
## <a name="process-summary"></a><span data-ttu-id="d8b06-128">Résumé du processus</span><span class="sxs-lookup"><span data-stu-id="d8b06-128">Process summary</span></span>

<span data-ttu-id="d8b06-129">Dans la \> synthèse \> du \> processus de préparation des résultats du processus, une répartition des résultats des fichiers chargés est affichée en fonction du traitement réussi des fichiers et des résultats de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="d8b06-129">In Prepare \> Process \> Results \> Process summary, a breakdown of loaded file results is displayed according to successful file processing and error results.</span></span>
  
<span data-ttu-id="d8b06-130">Les volets présentent un affichage graphique des statistiques sur les fichiers importés, comme suit :</span><span class="sxs-lookup"><span data-stu-id="d8b06-130">The panes present a graphical display of imported file statistics, as follows:</span></span>
  
- <span data-ttu-id="d8b06-131">Le **Résumé des processus accumule**d : tous les fichiers dans le cas.</span><span class="sxs-lookup"><span data-stu-id="d8b06-131">**Process summary accumulate**d: All files in the case.</span></span>
    
- <span data-ttu-id="d8b06-132">**Dernier processus-Résumé**: fichiers chargés à partir de la dernière session ou action.</span><span class="sxs-lookup"><span data-stu-id="d8b06-132">**Process summary last**: Files loaded from the last session or action.</span></span> 
    
- <span data-ttu-id="d8b06-133">**Famille : informations**sur la famille dans le cas (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="d8b06-133">**Families last**: Family information in the case (if any).</span></span>
    
- <span data-ttu-id="d8b06-134">Si des fichiers de **départ** ont été ajoutés, le nombre de fichiers de départ est indiqué par problème qui a été défini pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="d8b06-134">If **Seed** files were added, the number of seed files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="d8b06-135">Si le marquage des fichiers de **départ** a échoué, cela est également indiqué.</span><span class="sxs-lookup"><span data-stu-id="d8b06-135">If the marking of **Seed** files failed, that is also noted.</span></span> 
    
- <span data-ttu-id="d8b06-136">Si des fichiers **pré-balisés** ont été ajoutés, le nombre de fichiers pré-balisés est indiqué par problème qui a été défini pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="d8b06-136">If **Pre-tagged** files were added, the number of pre-tagged files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="d8b06-137">Si le marquage des fichiers **pré-balisés** a échoué, cela est également indiqué.</span><span class="sxs-lookup"><span data-stu-id="d8b06-137">If the marking of **Pre-tagged** files failed, that is also noted.</span></span> 
    
![Résumé de module de processus](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a><span data-ttu-id="d8b06-139">Processus récapitulatif de processus accumulés et derniers graphiques</span><span class="sxs-lookup"><span data-stu-id="d8b06-139">Process summary accumulated and last charts</span></span>

<span data-ttu-id="d8b06-140">La barre de gauche inclut les fichiers sources et extraits : tous les fichiers trouvés.</span><span class="sxs-lookup"><span data-stu-id="d8b06-140">The left bar includes Source + extracted files: which is all files found.</span></span> 
  
<span data-ttu-id="d8b06-141">La barre de droite, traitée, inclut les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8b06-141">The right bar, Processed, includes:</span></span>
  
- <span data-ttu-id="d8b06-142">Fichiers avec des erreurs de chargement</span><span class="sxs-lookup"><span data-stu-id="d8b06-142">Files with load errors</span></span>
    
- <span data-ttu-id="d8b06-143">Fichiers correctement chargés, qui peuvent inclure les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8b06-143">Successfully loaded files, which may include:</span></span> 
    
  - <span data-ttu-id="d8b06-144">**Existant**: les fichiers qui ont été chargés précédemment et sont à nouveau chargés (y compris les doublons).</span><span class="sxs-lookup"><span data-stu-id="d8b06-144">**Existing**: Files that were loaded before and are now loaded again (including duplicates).</span></span>
    
  - <span data-ttu-id="d8b06-145">**Text**: fichiers uniques avec texte.</span><span class="sxs-lookup"><span data-stu-id="d8b06-145">**Text**: Unique files with text.</span></span>
    
  - <span data-ttu-id="d8b06-146">**Non-texte**: fichiers texte vides, fichiers texte natif vides, fichiers non-texte natifs.</span><span class="sxs-lookup"><span data-stu-id="d8b06-146">**Non-text**: Empty text files, empty native text files, native non-text files.</span></span> 
    
  - <span data-ttu-id="d8b06-147">**Duplicate**s : fichiers en double avec texte.</span><span class="sxs-lookup"><span data-stu-id="d8b06-147">**Duplicate**s: Duplicate files with text.</span></span>
    
## <a name="last-process-errors"></a><span data-ttu-id="d8b06-148">Erreurs du dernier processus</span><span class="sxs-lookup"><span data-stu-id="d8b06-148">Last process errors</span></span>

<span data-ttu-id="d8b06-149">Dans \> prepare \> process \> Results Last process Errors, les détails des erreurs de la dernière session ou action effectuée sont affichés.</span><span class="sxs-lookup"><span data-stu-id="d8b06-149">In Prepare \> Process \> Results \> Last process errors, details of the errors in the last session or action performed are displayed.</span></span>
  
![Erreurs de module de processus](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a><span data-ttu-id="d8b06-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b06-151">See also</span></span>

[<span data-ttu-id="d8b06-152">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d8b06-152">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="d8b06-153">Exécution du module de processus et chargement des données</span><span class="sxs-lookup"><span data-stu-id="d8b06-153">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

