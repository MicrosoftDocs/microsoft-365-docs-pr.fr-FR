---
title: Exporter un rapport de recherche de contenu
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
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
description: Au lieu d’exporter les résultats réels d’une recherche de contenu dans le centre de sécurité & conformité dans Office 365, vous pouvez exporter un rapport des résultats de la recherche. Le rapport contient un résumé des résultats de la recherche et un document avec des informations détaillées sur chaque élément à exporter.
ms.openlocfilehash: 6730a1c406e02de26cbef964e445cfad31c948ec
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42074391"
---
# <a name="export-a-content-search-report"></a><span data-ttu-id="f9767-104">Exporter un rapport de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="f9767-104">Export a Content Search report</span></span>

<span data-ttu-id="f9767-105">Au lieu d’exporter l’ensemble complet des résultats de recherche à partir d’une recherche de contenu dans le centre de sécurité & conformité (et à partir d’une recherche de contenu associée à un cas eDiscovery), vous pouvez exporter les mêmes rapports générés lorsque vous exportez les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="f9767-105">Instead of exporting the full set of search results from a Content Search in the Security & Compliance Center (and from a Content Search that's associated with an eDiscovery case), you can export the same reports that are generated when you export search results.</span></span>
  
<span data-ttu-id="f9767-106">Lorsque vous exportez un État, il est téléchargé dans un dossier portant le même nom que la recherche de contenu, mais avec *_ReportsOnly*.</span><span class="sxs-lookup"><span data-stu-id="f9767-106">When you export a report, it's downloaded to a folder that has the same name as the Content Search, but that's appended with *_ReportsOnly*.</span></span> <span data-ttu-id="f9767-107">Par exemple, si la recherche de contenu est nommée *ContosoCase0815*, le rapport est téléchargé dans un dossier nommé *ContosoCase0815_ReportsOnly*.</span><span class="sxs-lookup"><span data-stu-id="f9767-107">For example, if the Content Search is named  *ContosoCase0815*, then the report is downloaded to a folder named *ContosoCase0815_ReportsOnly*.</span></span> <span data-ttu-id="f9767-108">Pour obtenir la liste des documents inclus dans le rapport, voir [ce qui est inclus dans le rapport](#whats-included-in-the-report).</span><span class="sxs-lookup"><span data-stu-id="f9767-108">For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="f9767-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f9767-109">Before you begin</span></span>

- <span data-ttu-id="f9767-110">Pour exporter un rapport de recherche de contenu, vous devez disposer du rôle de gestion de la recherche de conformité dans le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="f9767-110">To export a Content Search report, you have to be assigned the Compliance Search management role in the Security & Compliance Center.</span></span> <span data-ttu-id="f9767-111">Ce rôle est affecté aux groupes de rôles du gestionnaire eDiscovery intégré et de la gestion de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f9767-111">This role is assigned to the built-in eDiscovery Manager and Organization Management role groups.</span></span> <span data-ttu-id="f9767-112">Ce rôle n’est pas affecté par défaut au groupe de rôles Gestion de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f9767-112">It isn't assigned by default to the Organization Management role group.</span></span> <span data-ttu-id="f9767-113">Pour plus d'informations, voir [Attribution d'autorisations eDiscovery](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="f9767-113">For more information, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="f9767-114">Lorsque vous exportez un État, les données sont stockées temporairement dans une zone de stockage Azure unique dans le Cloud Microsoft avant d’être téléchargée sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f9767-114">When you export a report, the data is temporarily stored in a unique Azure Storage area in the Microsoft cloud before it's downloaded to your local computer.</span></span> <span data-ttu-id="f9767-115">Assurez-vous que votre organisation peut se connecter au point de terminaison dans Azure, c’est-à-dire \*\* \*. blob.Core.Windows.net\*\* (le caractère générique représente un identificateur unique pour votre exportation).</span><span class="sxs-lookup"><span data-stu-id="f9767-115">Be sure that your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export).</span></span> <span data-ttu-id="f9767-116">Les données de résultats de recherche sont supprimées de la zone de stockage Azure deux semaines après sa création.</span><span class="sxs-lookup"><span data-stu-id="f9767-116">The search results data is deleted from the Azure Storage area two weeks after it's created.</span></span> 
    
- <span data-ttu-id="f9767-117">L’ordinateur que vous utilisez pour exporter les résultats de recherche doit répondre aux exigences système suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9767-117">The computer you use to export the search results has to meet the following system requirements:</span></span>
    
  - <span data-ttu-id="f9767-118">versions 32 bits ou 64 bits de Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="f9767-118">32-bit or 64-bit versions of Windows 7 and later versions</span></span>
    
  - <span data-ttu-id="f9767-119">Microsoft .NET Framework 4,7</span><span class="sxs-lookup"><span data-stu-id="f9767-119">Microsoft .NET Framework 4.7</span></span>
    
- <span data-ttu-id="f9767-120">Pour exécuter l’outil d’exportation de découverte électronique<sup>1</sup>, vous devez utiliser l’un des navigateurs pris en charge suivants :</span><span class="sxs-lookup"><span data-stu-id="f9767-120">You have to use one of the following supported browsers to run the eDiscovery Export Tool<sup>1</sup>:</span></span>

  - <span data-ttu-id="f9767-121">Microsoft Edge <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="f9767-121">Microsoft Edge <sup>2</sup></span></span>

    <span data-ttu-id="f9767-122">OU</span><span class="sxs-lookup"><span data-stu-id="f9767-122">OR</span></span>

  - <span data-ttu-id="f9767-123">Microsoft Internet Explorer 10 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="f9767-123">Microsoft Internet Explorer 10 and later versions</span></span>

  > [!NOTE]
  > <span data-ttu-id="f9767-124"><sup>1</sup> Microsoft ne fabrique pas d’extensions ou de modules complémentaires tiers pour les applications ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="f9767-124"><sup>1</sup> Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications.</span></span> <span data-ttu-id="f9767-125">L’exportation des résultats de recherche à l’aide d’un navigateur non pris en charge avec des extensions ou des modules complémentaires tiers n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f9767-125">Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span><br/>
  > <span data-ttu-id="f9767-126"><sup>2</sup> suite à des modifications récentes apportées à Microsoft Edge, la prise en charge de ClickOnce n’est plus activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="f9767-126"><sup>2</sup> As a result of recent changes to Microsoft Edge, ClickOnce support is no longer enabled by default.</span></span> <span data-ttu-id="f9767-127">Pour obtenir des instructions sur l’activation de la prise en charge ClickOnce dans Edge, consultez [la rubrique utiliser l’outil d’exportation de découverte électronique Office 365 dans Microsoft Edge](configure-edge-to-export-search-results.md).</span><span class="sxs-lookup"><span data-stu-id="f9767-127">For instructions on enabling ClickOnce support in Edge, see [Use the Office 365 eDiscovery Export Tool in Microsoft Edge](configure-edge-to-export-search-results.md).</span></span>

- <span data-ttu-id="f9767-128">Si la taille totale estimée des résultats renvoyés par une recherche de contenu dépasse 2 to, l’exportation du rapport échoue.</span><span class="sxs-lookup"><span data-stu-id="f9767-128">If the estimated total size of the results returned by a Content Search exceeds 2 TB, exporting the report fails.</span></span> <span data-ttu-id="f9767-129">Pour réussir l’exportation du rapport, essayez de limiter l’étendue et relancez la recherche de sorte que la taille estimée des résultats soit inférieure à 2 to.</span><span class="sxs-lookup"><span data-stu-id="f9767-129">To successfully export the report, try to narrow the scope and rerun the search so the estimated size of the results is less than 2 TB.</span></span>

- <span data-ttu-id="f9767-130">L’exportation de rapports de recherche de contenu compte sur le nombre maximal d’exportations en cours d’exécution en même temps et le nombre maximal d’exportations qu’un utilisateur unique peut exécuter.</span><span class="sxs-lookup"><span data-stu-id="f9767-130">Exporting Content Search reports counts against the maximum number of exports running at the same time and the maximum number of exports that a single user can run.</span></span> <span data-ttu-id="f9767-131">Pour plus d’informations sur les limites d’exportation, voir [Export content Search Results](export-search-results.md#export-limits).</span><span class="sxs-lookup"><span data-stu-id="f9767-131">For more information about export limits, see [Export Content Search results](export-search-results.md#export-limits).</span></span>

## <a name="generate-and-download-a-content-search-report"></a><span data-ttu-id="f9767-132">Générer et télécharger un rapport de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="f9767-132">Generate and download a Content Search report</span></span>

<span data-ttu-id="f9767-133">Les étapes de génération et de téléchargement d’un rapport de recherche de contenu sont similaires à l’exportation des résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="f9767-133">The steps to generate and download a Content Search report are similar to actually exporting search results.</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="f9767-134">Étape 1 : générer le rapport pour l’exportation</span><span class="sxs-lookup"><span data-stu-id="f9767-134">Step 1: Generate the report for export</span></span>

<span data-ttu-id="f9767-135">La première étape consiste à préparer le rapport en vue de son téléchargement sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f9767-135">The first step is to prepare the report for downloading to your computer exporting.</span></span> <span data-ttu-id="f9767-136">Lorsque vous le rapport, les documents de rapport sont téléchargés vers une zone de stockage Azure dans le Cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f9767-136">When you the report, the report documents are uploaded to an Azure Storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="f9767-137">Accédez à [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="f9767-137">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="f9767-138">Ouvrez une session Office 365 en utilisant votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="f9767-138">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="f9767-139">Dans le volet gauche du centre de sécurité & conformité, cliquez sur recherche de **contenu**de **recherche** \> .</span><span class="sxs-lookup"><span data-stu-id="f9767-139">In the left pane of the Security & Compliance Center, click **Search** \> **Content search**.</span></span>
    
4. <span data-ttu-id="f9767-140">Sur la page **recherche de contenu** , sélectionnez une recherche.</span><span class="sxs-lookup"><span data-stu-id="f9767-140">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="f9767-141">Dans le volet d’informations, sous **Exporter le rapport vers un ordinateur**, cliquez sur **générer un rapport**.</span><span class="sxs-lookup"><span data-stu-id="f9767-141">In the details pane, under **Export report to a computer**, click **Generate report**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f9767-142">Si les résultats d’une recherche datent d’il y a plus de 7 jours, vous êtes invité à mettre à jour les résultats.</span><span class="sxs-lookup"><span data-stu-id="f9767-142">If the results for a search are older than 7 days, you are prompted to update the search results.</span></span> <span data-ttu-id="f9767-143">Dans ce cas, annulez l’exportation, cliquez sur **mettre à jour les résultats** de la recherche dans le volet d’informations de la recherche sélectionnée, puis redémarrez l’exportation des rapports une fois les résultats mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f9767-143">If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the report export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="f9767-144">Sur la page **exporter un rapport** , sous **inclure ces éléments de la recherche**, choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9767-144">On the **Export a report** page, under **Include these items from the search**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="f9767-145">exporter uniquement les éléments indexés ;</span><span class="sxs-lookup"><span data-stu-id="f9767-145">Export only indexed items</span></span>
    
    - <span data-ttu-id="f9767-146">exporter les éléments indexés et non indexés ;</span><span class="sxs-lookup"><span data-stu-id="f9767-146">Export indexed and unindexed items</span></span>
    
    - <span data-ttu-id="f9767-147">exporter uniquement les éléments non indexés.</span><span class="sxs-lookup"><span data-stu-id="f9767-147">Export only unindexed items</span></span>
    
    <span data-ttu-id="f9767-148">Pour plus d’informations sur les éléments non indexés, voir [éléments partiellement indexés dans la recherche de contenu](partially-indexed-items-in-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="f9767-148">For more information about unindexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="f9767-149">Choisissez d’inclure les statistiques de recherche pour toutes les versions des documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f9767-149">Choose to include search statistics for all versions of SharePoint documents.</span></span> <span data-ttu-id="f9767-150">Cette option apparaît uniquement si les sources de contenu de la recherche incluent des sites SharePoint ou OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="f9767-150">This option appears only if the content sources of the search include SharePoint or OneDrive for Business sites.</span></span>
    
8. <span data-ttu-id="f9767-151">Cliquez sur **générer un rapport**.</span><span class="sxs-lookup"><span data-stu-id="f9767-151">Click **Generate report**.</span></span>
    
    <span data-ttu-id="f9767-152">Le rapport de résultats de recherche est préparé pour le téléchargement, ce qui signifie que les documents de rapport seront téléchargés vers la zone de stockage Azure du Cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f9767-152">The search results report is prepared for downloading, which means the report documents will be uploaded to the Azure Storage area in the Microsoft cloud.</span></span> <span data-ttu-id="f9767-153">Lorsque le rapport est prêt à être téléchargé, le lien **Télécharger le rapport** est affiché sous **Exporter le rapport vers un ordinateur** dans le volet d’informations.</span><span class="sxs-lookup"><span data-stu-id="f9767-153">When the report is ready for download, the **Download report** link is displayed under **Export report to a computer** in the details pane.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="f9767-154">Vous pouvez également exporter un rapport pour une recherche de contenu associée à un cas de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="f9767-154">You can also export a report for a Content Search that's associated with an eDiscovery case.</span></span> <span data-ttu-id="f9767-155">Pour ce faire, **accédez à** \> eDiscovery **eDiscovery**, sélectionnez un cas, puis cliquez sur **modifier** ![l'](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)icône modifier.</span><span class="sxs-lookup"><span data-stu-id="f9767-155">To do this, go to **eDiscovery** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span> <span data-ttu-id="f9767-156">Sur la page **recherches** , sélectionnez une recherche, **puis cliquez sur** ![exporter les résultats](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> de la recherche d’exportation **exporter un rapport**.</span><span class="sxs-lookup"><span data-stu-id="f9767-156">On the **Searches** page, select a search, and then click **Export** ![Export search results icon](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Export a report**.</span></span> 
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="f9767-157">Étape 2 : Télécharger le rapport</span><span class="sxs-lookup"><span data-stu-id="f9767-157">Step 2: Download the report</span></span>

<span data-ttu-id="f9767-158">L’étape suivante consiste à télécharger le rapport à partir de la zone de stockage Azure sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f9767-158">The next step is to download the report from the Azure Storage area to your local computer.</span></span>
  
1. <span data-ttu-id="f9767-159">Dans le volet d’informations de la recherche pour laquelle vous avez généré le rapport, sous exporter le rapport **vers un ordinateur**, cliquez sur **Télécharger le rapport**.</span><span class="sxs-lookup"><span data-stu-id="f9767-159">In the details pane for the search that you generated the report for, under **Export report to a computer**, click **Download report**.</span></span>
    
    <span data-ttu-id="f9767-160">La page **Télécharger le rapport** s’affiche et contient les informations suivantes sur le rapport téléchargé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f9767-160">The **Download report** page is displayed and contains the following information about the report that's downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="f9767-161">Le nombre d’éléments à télécharger.</span><span class="sxs-lookup"><span data-stu-id="f9767-161">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="f9767-162">La taille totale estimée des éléments à télécharger.</span><span class="sxs-lookup"><span data-stu-id="f9767-162">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="f9767-163">Si les éléments indexés ou non indexés seront exportés.</span><span class="sxs-lookup"><span data-stu-id="f9767-163">Whether indexed or unindexed will be exported.</span></span> <span data-ttu-id="f9767-164">Les éléments non indexés sont des éléments qui ont un format reconnu, sont chiffrés ou n’ont pas été indexés pour d’autres raisons.</span><span class="sxs-lookup"><span data-stu-id="f9767-164">Unindexed items are items that have a recognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="f9767-165">Indique si les versions des documents SharePoint doivent être téléchargées.</span><span class="sxs-lookup"><span data-stu-id="f9767-165">Whether versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="f9767-166">État du processus d’exportation des rapports.</span><span class="sxs-lookup"><span data-stu-id="f9767-166">The status of the report export process.</span></span> <span data-ttu-id="f9767-167">Vous pouvez commencer à télécharger le rapport même si la préparation du rapport n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="f9767-167">You can start downloading the report even if the preparation of the report isn't complete.</span></span>
    
2. <span data-ttu-id="f9767-168">Sous **Clé d’exportation**, cliquez sur **Copier dans le Presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="f9767-168">Under **Export key**, click **Copy to clipboard**.</span></span> <span data-ttu-id="f9767-169">Utilisez cette clé à l’étape 5 pour télécharger le rapport.</span><span class="sxs-lookup"><span data-stu-id="f9767-169">You use this key in step 5 to download the report.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="f9767-170">Étant donné qu’une personne peut installer et démarrer l’outil d’exportation de découverte électronique, puis utiliser cette clé pour télécharger le rapport de recherche, veillez à protéger cette clé comme vous le feriez pour protéger les mots de passe ou d’autres informations relatives à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="f9767-170">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="f9767-171">Cliquez sur **Télécharger le rapport**.</span><span class="sxs-lookup"><span data-stu-id="f9767-171">Click **Download report**.</span></span>
    
4. <span data-ttu-id="f9767-172">Si vous êtes invité à installer l' **outil d’exportation de découverte électronique MicrosoftOffice 365**, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="f9767-172">If you're prompted to install the **MicrosoftOffice 365 eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="f9767-173">Dans l’**outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copiée à l’étape 2 dans la zone appropriée. </span><span class="sxs-lookup"><span data-stu-id="f9767-173">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="f9767-174">Cliquez sur **Parcourir** pour spécifier l’emplacement où vous souhaitez télécharger le rapport.</span><span class="sxs-lookup"><span data-stu-id="f9767-174">Click **Browse** to specify the location where you want to download the report.</span></span> 
    
7. <span data-ttu-id="f9767-175">Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f9767-175">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="f9767-176">L’**outil d’exportation de découverte électronique** affiche l’état du processus d’exportation, ainsi qu’une estimation du nombre (et de la taille) d’éléments qui doivent encore être téléchargés.</span><span class="sxs-lookup"><span data-stu-id="f9767-176">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded.</span></span> <span data-ttu-id="f9767-177">Une fois le processus d’exportation terminé, vous pouvez accéder aux fichiers à l’emplacement où ils ont été téléchargés.</span><span class="sxs-lookup"><span data-stu-id="f9767-177">When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="f9767-178">Vous pouvez télécharger le rapport pour une recherche de contenu associée à un cas de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="f9767-178">You can download the report for a Content Search that's associated with an eDiscovery case.</span></span> <span data-ttu-id="f9767-179">Pour ce faire, **accédez à** \> eDiscovery **eDiscovery**, sélectionnez un cas, puis cliquez sur **modifier** ![l'](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)icône modifier.</span><span class="sxs-lookup"><span data-stu-id="f9767-179">To do this, go to **eDiscovery** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span> <span data-ttu-id="f9767-180">Dans la page **exportations** , sélectionnez une exportation de rapport, puis cliquez sur **Télécharger le rapport** dans le volet d’informations.</span><span class="sxs-lookup"><span data-stu-id="f9767-180">On the **Exports** page, select an report export, and then click **Download report** in the details pane.</span></span> 
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="f9767-181">Éléments inclus dans le rapport</span><span class="sxs-lookup"><span data-stu-id="f9767-181">What's included in the report</span></span>

<span data-ttu-id="f9767-182">Lorsque vous générez et exportez un rapport sur les résultats d’une recherche de contenu, les documents suivants sont téléchargés :</span><span class="sxs-lookup"><span data-stu-id="f9767-182">When you generate and export a report about the results of a Content Search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="f9767-183">**Exporter le Résumé :** Document Excel qui contient un résumé de l’exportation.</span><span class="sxs-lookup"><span data-stu-id="f9767-183">**Export Summary:** An Excel document that contains a summary of the export.</span></span> <span data-ttu-id="f9767-184">Cela inclut des informations telles que le nombre de sources de contenu qui ont été recherchées, le nombre de résultats de recherche à partir de chaque emplacement de contenu, le nombre estimé d’éléments, le nombre réel d’éléments qui seront exportés et la taille estimée et réelle des éléments qui seraient exportées.</span><span class="sxs-lookup"><span data-stu-id="f9767-184">This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="f9767-185">Si vous incluez des éléments non indexés lors de l’exportation du rapport, le nombre total d’éléments non indexés est inclus dans le nombre total de résultats de recherche estimés et dans le nombre total de résultats de recherche téléchargés (si vous deviez exporter les résultats de la recherche) répertoriés dans le Exporter un rapport de synthèse.</span><span class="sxs-lookup"><span data-stu-id="f9767-185">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the Export Summary report.</span></span> <span data-ttu-id="f9767-186">En d’autres termes, le nombre total d’éléments qui seront téléchargés est égal au nombre total de résultats estimés et au nombre total d’éléments non indexés.</span><span class="sxs-lookup"><span data-stu-id="f9767-186">In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span> 
  
- <span data-ttu-id="f9767-187">**Manifeste :** Fichier manifeste (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="f9767-187">**Manifest:** A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
- <span data-ttu-id="f9767-188">**Résultats :** Document Excel contenant une ligne contenant des informations sur chaque élément indexé à exporter avec les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="f9767-188">**Results:** An Excel document that contains a row with information about each indexed item that would be exported with the search results.</span></span> <span data-ttu-id="f9767-189">Pour le courrier électronique, le journal des résultats contient des informations sur chaque message, y compris :</span><span class="sxs-lookup"><span data-stu-id="f9767-189">For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="f9767-190">l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;</span><span class="sxs-lookup"><span data-stu-id="f9767-190">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="f9767-191">la date à laquelle le message a été envoyé ou reçu ;</span><span class="sxs-lookup"><span data-stu-id="f9767-191">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="f9767-192">l’objet du message ;</span><span class="sxs-lookup"><span data-stu-id="f9767-192">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="f9767-193">l’expéditeur et les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="f9767-193">The sender and recipients of the message.</span></span>
    
    <span data-ttu-id="f9767-194">Pour les documents provenant de sites SharePoint et OneDrive entreprise, le journal des résultats contient des informations sur chaque document, notamment :</span><span class="sxs-lookup"><span data-stu-id="f9767-194">For documents from SharePoint and OneDrive for Business sites, the Results log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="f9767-195">l’URL du document ;</span><span class="sxs-lookup"><span data-stu-id="f9767-195">The URL for the document.</span></span>
    
  - <span data-ttu-id="f9767-196">l’URL de la collection de sites qui héberge le document ;</span><span class="sxs-lookup"><span data-stu-id="f9767-196">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="f9767-197">la date à laquelle le document a été modifié pour la dernière fois ;</span><span class="sxs-lookup"><span data-stu-id="f9767-197">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="f9767-198">le nom du document (qui se trouve dans la colonne Objet du journal des résultats).</span><span class="sxs-lookup"><span data-stu-id="f9767-198">The name of the document (which is located in the Subject column in the result log).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f9767-199">Le nombre de lignes dans l’état des **résultats** doit être égal au nombre total de résultats de recherche moins le nombre total d’éléments figurant dans le rapport **éléments non indexés** .</span><span class="sxs-lookup"><span data-stu-id="f9767-199">The number of rows in the **Results** report should be equal to the total number of search results minus the total number of items listed in the **Unindexed Items** report.</span></span> 
  
- <span data-ttu-id="f9767-200">**Éléments non indexés :** Document Excel qui contient des informations sur les éléments non indexés inclus dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="f9767-200">**Unindexed Items:** An Excel document that contains information about any unindexed items included in the search results.</span></span> <span data-ttu-id="f9767-201">Si vous n’incluez pas d’éléments non indexés lorsque vous générez le rapport des résultats de la recherche, ce rapport sera toujours téléchargé, mais il sera vide.</span><span class="sxs-lookup"><span data-stu-id="f9767-201">If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
