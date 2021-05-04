---
title: Exporter un rapport de recherche de contenu
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: how-to
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Au lieu d'exporter les résultats réels d'une recherche de contenu dans le Centre de sécurité & conformité dans Office 365, vous pouvez exporter un rapport de résultats de recherche. Le rapport contient un résumé des résultats de la recherche et un document contenant des informations détaillées sur chaque élément qui serait exporté.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: fec6e441458ad7429067a1314a7aec3824aff11a
ms.sourcegitcommit: 223a36a86753fe9cebee96f05ab4c9a144133677
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51760152"
---
# <a name="export-a-content-search-report"></a><span data-ttu-id="0a9bd-104">Exporter un rapport de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="0a9bd-104">Export a Content Search report</span></span>

<span data-ttu-id="0a9bd-105">Au lieu d'exporter l'ensemble complet des résultats de recherche à partir d'une recherche de contenu dans le Centre de sécurité & conformité (et à partir d'une recherche de contenu associée à un cas eDiscovery), vous pouvez exporter les rapports générés lors de l'exportation des résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-105">Instead of exporting the full set of search results from a Content Search in the Security & Compliance Center (and from a Content Search that's associated with an eDiscovery case), you can export the same reports that are generated when you export search results.</span></span>
  
<span data-ttu-id="0a9bd-106">Lorsque vous exportez un rapport, il est téléchargé vers un dossier qui a le même nom que la recherche de contenu, mais qui est également _ReportsOnly *.*</span><span class="sxs-lookup"><span data-stu-id="0a9bd-106">When you export a report, it's downloaded to a folder that has the same name as the Content Search, but that's appended with *_ReportsOnly*.</span></span> <span data-ttu-id="0a9bd-107">Par exemple, si la recherche de contenu est nommée  *ContosoCase0815*, le rapport est téléchargé dans un dossier nommé *ContosoCase0815_ReportsOnly*.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-107">For example, if the Content Search is named  *ContosoCase0815*, then the report is downloaded to a folder named *ContosoCase0815_ReportsOnly*.</span></span> <span data-ttu-id="0a9bd-108">Pour obtenir la liste des documents inclus dans le rapport, voir Ce qui [est inclus dans le rapport.](#whats-included-in-the-report)</span><span class="sxs-lookup"><span data-stu-id="0a9bd-108">For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="assign-roles-and-check-system-requirements"></a><span data-ttu-id="0a9bd-109">Attribuer des rôles et vérifier la exigences système</span><span class="sxs-lookup"><span data-stu-id="0a9bd-109">Assign roles and check system requirements</span></span>

- <span data-ttu-id="0a9bd-110">Pour exporter un rapport de recherche de contenu, vous devez avoir le rôle de gestion recherche de conformité dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-110">To export a Content Search report, you have to be assigned the Compliance Search management role in the Security & Compliance Center.</span></span> <span data-ttu-id="0a9bd-111">Ce rôle est attribué par défaut au Gestionnaire eDiscovery intégré et aux groupes de rôles Gestion de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-111">This role is assigned by default to the built-in eDiscovery Manager and Organization Management role groups.</span></span> <span data-ttu-id="0a9bd-112">Pour plus d'informations, voir [Attribution d'autorisations eDiscovery](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="0a9bd-112">For more information, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>

- <span data-ttu-id="0a9bd-113">Lorsque vous exportez un rapport, les données sont stockées temporairement dans une zone stockage Azure unique dans le cloud Microsoft avant d'être téléchargées sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-113">When you export a report, the data is temporarily stored in a unique Azure Storage area in the Microsoft cloud before it's downloaded to your local computer.</span></span> <span data-ttu-id="0a9bd-114">Assurez-vous que votre organisation peut se connecter au point de terminaison dans Azure, qui est **\* .blob.core.windows.net** (le caractère générique représente un identificateur unique pour votre exportation).</span><span class="sxs-lookup"><span data-stu-id="0a9bd-114">Be sure that your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export).</span></span> <span data-ttu-id="0a9bd-115">Les données de résultats de la recherche sont supprimées de la stockage Azure deux semaines après sa création.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-115">The search results data is deleted from the Azure Storage area two weeks after it's created.</span></span>

- <span data-ttu-id="0a9bd-116">L’ordinateur que vous utilisez pour exporter les résultats de recherche doit répondre aux exigences système suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a9bd-116">The computer you use to export the search results has to meet the following system requirements:</span></span>

  - <span data-ttu-id="0a9bd-117">Dernière version de Windows (32 bits ou 64 bits)</span><span class="sxs-lookup"><span data-stu-id="0a9bd-117">Latest version of Windows (32-bit or 64-bit)</span></span>

  - <span data-ttu-id="0a9bd-118">Microsoft .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="0a9bd-118">Microsoft .NET Framework 4.7</span></span>

- <span data-ttu-id="0a9bd-119">Vous devez utiliser l'un des navigateurs pris en charge suivants pour exécuter l'outil d'exportation eDiscovery<sup>1</sup>:</span><span class="sxs-lookup"><span data-stu-id="0a9bd-119">You have to use one of the following supported browsers to run the eDiscovery Export Tool<sup>1</sup>:</span></span>

  - <span data-ttu-id="0a9bd-120">Microsoft Edge <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="0a9bd-120">Microsoft Edge <sup>2</sup></span></span>

    <span data-ttu-id="0a9bd-121">OR</span><span class="sxs-lookup"><span data-stu-id="0a9bd-121">OR</span></span>

  - <span data-ttu-id="0a9bd-122">Microsoft Internet Explorer 10 versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0a9bd-122">Microsoft Internet Explorer 10 and later versions</span></span>

  > [!NOTE]
  > <span data-ttu-id="0a9bd-123"><sup>1</sup> Microsoft ne fabrique pas d'extensions ou d'extensions tierces pour ClickOnce applications.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-123"><sup>1</sup> Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications.</span></span> <span data-ttu-id="0a9bd-124">L'exportation des résultats de recherche à l'aide d'un navigateur non pris en charge avec des extensions ou extensions tierces n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-124">Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span><br/>
  > <span data-ttu-id="0a9bd-125"><sup>2</sup> Suite aux modifications récentes apportées à Microsoft Edge, ClickOnce prise en charge de la recherche n'est plus activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-125"><sup>2</sup> As a result of recent changes to Microsoft Edge, ClickOnce support is no longer enabled by default.</span></span> <span data-ttu-id="0a9bd-126">Pour obtenir des instructions sur l'activation ClickOnce prise en charge dans Edge, voir Utiliser l'outil d'exportation [eDiscovery dans Microsoft Edge](configure-edge-to-export-search-results.md).</span><span class="sxs-lookup"><span data-stu-id="0a9bd-126">For instructions on enabling ClickOnce support in Edge, see [Use the eDiscovery Export Tool in Microsoft Edge](configure-edge-to-export-search-results.md).</span></span>

- <span data-ttu-id="0a9bd-127">Si la taille totale estimée des résultats renvoyés par une recherche de contenu dépasse 2 To, l'exportation du rapport échoue.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-127">If the estimated total size of the results returned by a Content Search exceeds 2 TB, exporting the report fails.</span></span> <span data-ttu-id="0a9bd-128">Pour exporter correctement le rapport, essayez de restreindre l'étendue et réexécutez la recherche afin que la taille estimée des résultats soit inférieure à 2 To.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-128">To successfully export the report, try to narrow the scope and rerun the search so the estimated size of the results is less than 2 TB.</span></span>

- <span data-ttu-id="0a9bd-129">L'exportation de rapports de recherche de contenu est comptabilisée par rapport au nombre maximal d'exportations en cours d'exécution en même temps et au nombre maximal d'exportations qu'un seul utilisateur peut exécuter.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-129">Exporting Content Search reports counts against the maximum number of exports running at the same time and the maximum number of exports that a single user can run.</span></span> <span data-ttu-id="0a9bd-130">Pour plus d'informations sur les limites d'exportation, voir Exporter les résultats [de la recherche de contenu.](export-search-results.md#export-limits)</span><span class="sxs-lookup"><span data-stu-id="0a9bd-130">For more information about export limits, see [Export Content Search results](export-search-results.md#export-limits).</span></span>

## <a name="generate-and-download-a-content-search-report"></a><span data-ttu-id="0a9bd-131">Générer et télécharger un rapport de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="0a9bd-131">Generate and download a Content Search report</span></span>

<span data-ttu-id="0a9bd-132">Les étapes de générer et de télécharger un rapport de recherche de contenu sont similaires à l'exportation des résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-132">The steps to generate and download a Content Search report are similar to actually exporting search results.</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="0a9bd-133">Étape 1 : Générer le rapport pour l'exportation</span><span class="sxs-lookup"><span data-stu-id="0a9bd-133">Step 1: Generate the report for export</span></span>

<span data-ttu-id="0a9bd-134">La première étape consiste à préparer le rapport pour le téléchargement vers l'exportation de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-134">The first step is to prepare the report for downloading to your computer exporting.</span></span> <span data-ttu-id="0a9bd-135">Lorsque vous présentez le rapport, les documents de rapport sont téléchargés vers une stockage Azure dans le cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-135">When you the report, the report documents are uploaded to an Azure Storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="0a9bd-136">Accédez à [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="0a9bd-136">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="0a9bd-137">Connectez-vous à l’aide de votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-137">Sign in using your work or school account.</span></span>
    
3. <span data-ttu-id="0a9bd-138">Dans le volet gauche du Centre de sécurité & conformité, cliquez sur **Recherche de** contenu \> **de recherche.**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-138">In the left pane of the Security & Compliance Center, click **Search** \> **Content search**.</span></span>
    
4. <span data-ttu-id="0a9bd-139">Dans la page **de recherche de** contenu, sélectionnez une recherche.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-139">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="0a9bd-140">Dans le volet d'informations, sous **Exporter le rapport sur un ordinateur,** cliquez sur Générer un **rapport.**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-140">In the details pane, under **Export report to a computer**, click **Generate report**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="0a9bd-141">Si les résultats d’une recherche datent d’il y a plus de 7 jours, vous êtes invité à mettre à jour les résultats.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-141">If the results for a search are older than 7 days, you are prompted to update the search results.</span></span> <span data-ttu-id="0a9bd-142">Si cela se produit,  annulez l'exportation, cliquez sur Mettre à jour les résultats de recherche dans le volet d'informations de la recherche sélectionnée, puis recommencez l'exportation du rapport après la mise à jour des résultats.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-142">If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the report export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="0a9bd-143">Dans la page **Exporter un rapport,** sous Inclure ces éléments à partir de la **recherche,** choisissez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a9bd-143">On the **Export a report** page, under **Include these items from the search**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="0a9bd-144">exporter uniquement les éléments indexés ;</span><span class="sxs-lookup"><span data-stu-id="0a9bd-144">Export only indexed items</span></span>
    
    - <span data-ttu-id="0a9bd-145">exporter les éléments indexés et non indexés ;</span><span class="sxs-lookup"><span data-stu-id="0a9bd-145">Export indexed and unindexed items</span></span>
    
    - <span data-ttu-id="0a9bd-146">exporter uniquement les éléments non indexés.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-146">Export only unindexed items</span></span>
    
    <span data-ttu-id="0a9bd-147">Pour plus d'informations sur les éléments non indexés, voir [Éléments partiellement indexés dans la recherche de contenu.](partially-indexed-items-in-content-search.md)</span><span class="sxs-lookup"><span data-stu-id="0a9bd-147">For more information about unindexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="0a9bd-148">Choisissez d'inclure des statistiques de recherche pour toutes les versions SharePoint documents.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-148">Choose to include search statistics for all versions of SharePoint documents.</span></span> <span data-ttu-id="0a9bd-149">Cette option s'affiche uniquement si les sources de contenu de la recherche incluent SharePoint ou OneDrive Entreprise sites.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-149">This option appears only if the content sources of the search include SharePoint or OneDrive for Business sites.</span></span>
    
8. <span data-ttu-id="0a9bd-150">Cliquez **sur Générer un rapport.**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-150">Click **Generate report**.</span></span>
    
    <span data-ttu-id="0a9bd-151">Le rapport des résultats de la recherche est préparé pour le téléchargement, ce qui signifie que les documents du rapport sont téléchargés vers la stockage Azure dans le cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-151">The search results report is prepared for downloading, which means the report documents will be uploaded to the Azure Storage area in the Microsoft cloud.</span></span> <span data-ttu-id="0a9bd-152">Lorsque le rapport est prêt  à être téléchargé, le lien du rapport de téléchargement s'affiche sous **Rapport** d'exportation vers un ordinateur dans le volet d'informations.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-152">When the report is ready for download, the **Download report** link is displayed under **Export report to a computer** in the details pane.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="0a9bd-153">Vous pouvez également exporter un rapport pour une recherche de contenu associée à un cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-153">You can also export a report for a Content Search that's associated with an eDiscovery case.</span></span> <span data-ttu-id="0a9bd-154">Pour ce faire, allez à **eDiscovery** \> **eDiscovery,** sélectionnez un cas, puis cliquez sur  ![ Modifier l'icône ](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) Modifier .</span><span class="sxs-lookup"><span data-stu-id="0a9bd-154">To do this, go to **eDiscovery** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span> <span data-ttu-id="0a9bd-155">Dans la page **Recherches,** sélectionnez une  recherche, puis cliquez sur Exporter les résultats de la recherche icône Exporter un ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **rapport.**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-155">On the **Searches** page, select a search, and then click **Export** ![Export search results icon](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Export a report**.</span></span> 
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="0a9bd-156">Étape 2 : Télécharger le rapport</span><span class="sxs-lookup"><span data-stu-id="0a9bd-156">Step 2: Download the report</span></span>

<span data-ttu-id="0a9bd-157">L'étape suivante consiste à télécharger le rapport à partir de la stockage Azure sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-157">The next step is to download the report from the Azure Storage area to your local computer.</span></span>
  
1. <span data-ttu-id="0a9bd-158">Dans le volet d'informations de la recherche pour qui vous avez généré le rapport, sous **Exporter** le rapport sur un ordinateur, cliquez sur **Télécharger le rapport.**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-158">In the details pane for the search that you generated the report for, under **Export report to a computer**, click **Download report**.</span></span>
    
    <span data-ttu-id="0a9bd-159">La page **Télécharger** le rapport s'affiche et contient les informations suivantes sur le rapport téléchargé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-159">The **Download report** page is displayed and contains the following information about the report that's downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="0a9bd-160">Le nombre d’éléments à télécharger.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-160">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="0a9bd-161">La taille totale estimée des éléments à télécharger.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-161">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="0a9bd-162">Si les éléments indexés ou non indexés seront exportés.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-162">Whether indexed or unindexed will be exported.</span></span> <span data-ttu-id="0a9bd-163">Les éléments non indexés sont des éléments qui ont un format reconnu, sont chiffrés ou n'ont pas été indexés pour d'autres raisons.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-163">Unindexed items are items that have a recognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="0a9bd-164">Si les versions SharePoint documents seront téléchargées.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-164">Whether versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="0a9bd-165">État du processus d'exportation de rapport.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-165">The status of the report export process.</span></span> <span data-ttu-id="0a9bd-166">Vous pouvez commencer à télécharger le rapport même si sa préparation n'est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-166">You can start downloading the report even if the preparation of the report isn't complete.</span></span>
    
2. <span data-ttu-id="0a9bd-167">Sous **Clé d’exportation**, cliquez sur **Copier dans le Presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-167">Under **Export key**, click **Copy to clipboard**.</span></span> <span data-ttu-id="0a9bd-168">Vous utilisez cette clé à l'étape 5 pour télécharger le rapport.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-168">You use this key in step 5 to download the report.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="0a9bd-169">Étant donné que tout le monde peut installer et démarrer l'outil d'exportation eDiscovery, puis utiliser cette clé pour télécharger le rapport de recherche, prenez toutes les précautions nécessaires pour protéger cette clé comme vous le feriez pour protéger les mots de passe ou d'autres informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-169">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="0a9bd-170">Cliquez **sur Télécharger le rapport.**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-170">Click **Download report**.</span></span>
    
4. <span data-ttu-id="0a9bd-171">Si vous êtes invité à installer l'outil **d'exportation eDiscovery,** cliquez sur **Installer.**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-171">If you're prompted to install the **eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="0a9bd-172">Dans l’**outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copiée à l’étape 2 dans la zone appropriée. </span><span class="sxs-lookup"><span data-stu-id="0a9bd-172">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="0a9bd-173">Cliquez **sur Parcourir** pour spécifier l'emplacement où vous souhaitez télécharger le rapport.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-173">Click **Browse** to specify the location where you want to download the report.</span></span> 
    
7. <span data-ttu-id="0a9bd-174">Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-174">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="0a9bd-175">L’**outil d’exportation de découverte électronique** affiche l’état du processus d’exportation, ainsi qu’une estimation du nombre (et de la taille) d’éléments qui doivent encore être téléchargés.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-175">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded.</span></span> <span data-ttu-id="0a9bd-176">Une fois le processus d'exportation terminé, vous pouvez accéder aux fichiers à l'emplacement où ils ont été téléchargés.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-176">When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="0a9bd-177">Vous pouvez télécharger le rapport pour une recherche de contenu associée à un cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-177">You can download the report for a Content Search that's associated with an eDiscovery case.</span></span> <span data-ttu-id="0a9bd-178">Pour ce faire, allez à **eDiscovery** \> **eDiscovery,** sélectionnez un cas, puis cliquez sur  ![ Modifier l'icône ](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) Modifier .</span><span class="sxs-lookup"><span data-stu-id="0a9bd-178">To do this, go to **eDiscovery** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span> <span data-ttu-id="0a9bd-179">Dans la page **Exportation,** sélectionnez une exportation de rapport, puis cliquez sur Télécharger le rapport **dans** le volet d'informations.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-179">On the **Exports** page, select an report export, and then click **Download report** in the details pane.</span></span> 
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="0a9bd-180">Ce qui est inclus dans le rapport</span><span class="sxs-lookup"><span data-stu-id="0a9bd-180">What's included in the report</span></span>

<span data-ttu-id="0a9bd-181">Lorsque vous générez et exportez un rapport sur les résultats d'une recherche de contenu, les documents suivants sont téléchargés :</span><span class="sxs-lookup"><span data-stu-id="0a9bd-181">When you generate and export a report about the results of a Content Search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="0a9bd-182">**Résumé de l'exportation :** Un Excel qui contient un résumé de l'exportation.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-182">**Export Summary:** An Excel document that contains a summary of the export.</span></span> <span data-ttu-id="0a9bd-183">Cela inclut des informations telles que le nombre de sources de contenu qui ont fait l'objet d'une recherche, le nombre de résultats de recherche à partir de chaque emplacement de contenu, le nombre estimé d'éléments, le nombre réel d'éléments à exporter et la taille estimée et réelle des éléments à exporter.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-183">This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="0a9bd-184">Si vous incluez des éléments nonndes lors de l'exportation du rapport, le nombre d'éléments nonndex est inclus dans le nombre total de résultats de recherche estimés et dans le nombre total de résultats de recherche téléchargés (si vous de étiez pour exporter les résultats de recherche) répertoriés dans le rapport de synthèse d'exportation.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-184">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the Export Summary report.</span></span> <span data-ttu-id="0a9bd-185">En d'autres termes, le nombre total d'éléments à télécharger est égal au nombre total de résultats estimés et au nombre total d'éléments nonndex.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-185">In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span> 
  
- <span data-ttu-id="0a9bd-186">**Manifeste :** Fichier manifeste (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-186">**Manifest:** A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
- <span data-ttu-id="0a9bd-187">**Résultats :** Un Excel qui contient une ligne contenant des informations sur chaque élément indexé qui serait exporté avec les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-187">**Results:** An Excel document that contains a row with information about each indexed item that would be exported with the search results.</span></span> <span data-ttu-id="0a9bd-188">Pour le courrier électronique, le journal des résultats contient des informations sur chaque message, y compris :</span><span class="sxs-lookup"><span data-stu-id="0a9bd-188">For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="0a9bd-189">l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;</span><span class="sxs-lookup"><span data-stu-id="0a9bd-189">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="0a9bd-190">la date à laquelle le message a été envoyé ou reçu ;</span><span class="sxs-lookup"><span data-stu-id="0a9bd-190">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="0a9bd-191">l’objet du message ;</span><span class="sxs-lookup"><span data-stu-id="0a9bd-191">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="0a9bd-192">l’expéditeur et les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-192">The sender and recipients of the message.</span></span>
    
    <span data-ttu-id="0a9bd-193">Pour les documents provenant SharePoint sites OneDrive Entreprise sites web, le journal des résultats contient des informations sur chaque document, notamment :</span><span class="sxs-lookup"><span data-stu-id="0a9bd-193">For documents from SharePoint and OneDrive for Business sites, the Results log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="0a9bd-194">l’URL du document ;</span><span class="sxs-lookup"><span data-stu-id="0a9bd-194">The URL for the document.</span></span>
    
  - <span data-ttu-id="0a9bd-195">l’URL de la collection de sites qui héberge le document ;</span><span class="sxs-lookup"><span data-stu-id="0a9bd-195">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="0a9bd-196">la date à laquelle le document a été modifié pour la dernière fois ;</span><span class="sxs-lookup"><span data-stu-id="0a9bd-196">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="0a9bd-197">le nom du document (qui se trouve dans la colonne Objet du journal des résultats).</span><span class="sxs-lookup"><span data-stu-id="0a9bd-197">The name of the document (which is located in the Subject column in the result log).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="0a9bd-198">Le nombre de lignes  dans le rapport résultats doit être égal au nombre total de résultats de recherche moins le nombre total d'éléments répertoriés dans le rapport Éléments **nonndes.**</span><span class="sxs-lookup"><span data-stu-id="0a9bd-198">The number of rows in the **Results** report should be equal to the total number of search results minus the total number of items listed in the **Unindexed Items** report.</span></span> 
  
- <span data-ttu-id="0a9bd-199">**Éléments nonndexés :** Un Excel qui contient des informations sur les éléments nonndex inclus dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-199">**Unindexed Items:** An Excel document that contains information about any unindexed items included in the search results.</span></span> <span data-ttu-id="0a9bd-200">Si vous n'incluez pas d'éléments nonndex lorsque vous générez le rapport de résultats de recherche, ce rapport sera toujours téléchargé, mais il sera vide.</span><span class="sxs-lookup"><span data-stu-id="0a9bd-200">If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
