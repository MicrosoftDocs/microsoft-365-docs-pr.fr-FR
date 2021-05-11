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
description: Au lieu d’exporter les résultats réels d’une recherche de contenu dans le Centre de sécurité & conformité dans Office 365, vous pouvez exporter un rapport de résultats de recherche. Le rapport contient un résumé des résultats de la recherche et un document contenant des informations détaillées sur chaque élément qui serait exporté.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 094e67812b45ab1544d629ba6ddabcd86c70c633
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52311571"
---
# <a name="export-a-content-search-report"></a><span data-ttu-id="05547-104">Exporter un rapport de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="05547-104">Export a Content search report</span></span>

<span data-ttu-id="05547-105">Au lieu d’exporter l’ensemble complet des résultats de recherche à partir d’une recherche de contenu dans le Centre de conformité Microsoft 365 (ou à partir d’une recherche associée à un cas core eDiscovery), vous pouvez exporter les mêmes rapports qui sont générés lorsque vous exportez les résultats de recherche réels.</span><span class="sxs-lookup"><span data-stu-id="05547-105">Instead of exporting the full set of search results from a Content search in the Microsoft 365 compliance Center (or from a search that's associated with a Core eDiscovery case), you can export the same reports that are generated when you export the actual search results.</span></span>
  
<span data-ttu-id="05547-106">Lorsque vous exportez un rapport, les fichiers de rapport sont téléchargés dans un dossier de votre ordinateur local qui porte le même nom que la recherche de contenu, mais qui est également _ReportsOnly *.*</span><span class="sxs-lookup"><span data-stu-id="05547-106">When you export a report, the report files are downloaded to a folder on your local computer that has the same name as the Content Search, but that's appended with *_ReportsOnly*.</span></span> <span data-ttu-id="05547-107">Par exemple, si la recherche de contenu est nommée  *ContosoCase0815*, le rapport est téléchargé dans un dossier nommé *ContosoCase0815_ReportsOnly*.</span><span class="sxs-lookup"><span data-stu-id="05547-107">For example, if the Content Search is named  *ContosoCase0815*, then the report is downloaded to a folder named *ContosoCase0815_ReportsOnly*.</span></span> <span data-ttu-id="05547-108">Pour obtenir la liste des documents inclus dans le rapport, voir Ce qui [est inclus dans le rapport.](#whats-included-in-the-report)</span><span class="sxs-lookup"><span data-stu-id="05547-108">For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="before-you-export-a-search-report"></a><span data-ttu-id="05547-109">Avant d’exporter un rapport de recherche</span><span class="sxs-lookup"><span data-stu-id="05547-109">Before you export a search report</span></span>

- <span data-ttu-id="05547-110">Pour exporter un rapport de recherche, vous devez avoir le rôle de gestion de recherche de conformité dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="05547-110">To export a search report, you have to be assigned the Compliance Search management role in Security & Compliance Center.</span></span> <span data-ttu-id="05547-111">Ce rôle est attribué par défaut au Gestionnaire eDiscovery intégré et aux groupes de rôles Gestion de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="05547-111">This role is assigned by default to the built-in eDiscovery Manager and Organization Management role groups.</span></span> <span data-ttu-id="05547-112">Pour plus d'informations, voir [Attribution d'autorisations eDiscovery](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="05547-112">For more information, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>

- <span data-ttu-id="05547-113">Lorsque vous exportez un rapport, les données sont stockées temporairement dans un emplacement stockage Azure dans le cloud Microsoft avant d’être téléchargées sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="05547-113">When you export a report, the data is temporarily stored in an Azure Storage location in the Microsoft cloud before it's downloaded to your local computer.</span></span> <span data-ttu-id="05547-114">Assurez-vous que votre organisation peut se connecter au point de terminaison dans Azure, qui est **\* .blob.core.windows.net** (le caractère générique représente un identificateur unique pour votre exportation).</span><span class="sxs-lookup"><span data-stu-id="05547-114">Be sure that your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export).</span></span> <span data-ttu-id="05547-115">Les données des résultats de la recherche sont supprimées de l’emplacement stockage Azure deux semaines après leur création.</span><span class="sxs-lookup"><span data-stu-id="05547-115">The search results data is deleted from the Azure Storage location two weeks after it's created.</span></span>

- <span data-ttu-id="05547-116">L’ordinateur que vous utilisez pour exporter les résultats de recherche doit répondre aux exigences système suivantes :</span><span class="sxs-lookup"><span data-stu-id="05547-116">The computer you use to export the search results has to meet the following system requirements:</span></span>

  - <span data-ttu-id="05547-117">Dernière version de Windows (32 bits ou 64 bits)</span><span class="sxs-lookup"><span data-stu-id="05547-117">Latest version of Windows (32-bit or 64-bit)</span></span>

  - <span data-ttu-id="05547-118">Microsoft .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="05547-118">Microsoft .NET Framework 4.7</span></span>

- <span data-ttu-id="05547-119">Vous devez utiliser l’un des navigateurs pris en charge suivants pour exécuter l’outil d’exportation eDiscovery<sup>1</sup>:</span><span class="sxs-lookup"><span data-stu-id="05547-119">You have to use one of the following supported browsers to run the eDiscovery Export Tool<sup>1</sup>:</span></span>

  - <span data-ttu-id="05547-120">Microsoft Edge <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="05547-120">Microsoft Edge <sup>2</sup></span></span>

    <span data-ttu-id="05547-121">OR</span><span class="sxs-lookup"><span data-stu-id="05547-121">OR</span></span>

  - <span data-ttu-id="05547-122">Microsoft Internet Explorer 10 versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="05547-122">Microsoft Internet Explorer 10 and later versions</span></span>

  > [!NOTE]
  > <span data-ttu-id="05547-123"><sup>1</sup> Microsoft ne fabrique pas d’extensions ou d’extensions tierces pour ClickOnce applications.</span><span class="sxs-lookup"><span data-stu-id="05547-123"><sup>1</sup> Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications.</span></span> <span data-ttu-id="05547-124">L’exportation des résultats de recherche à l’aide d’un navigateur non pris en charge avec des extensions ou extensions tierces n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="05547-124">Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span><br/>
  > <span data-ttu-id="05547-125"><sup>2</sup> Suite aux modifications récentes apportées à Microsoft Edge, ClickOnce prise en charge de la recherche n’est plus activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="05547-125"><sup>2</sup> As a result of recent changes to Microsoft Edge, ClickOnce support is no longer enabled by default.</span></span> <span data-ttu-id="05547-126">Pour obtenir des instructions sur l’activation ClickOnce prise en charge dans Edge, voir Utiliser l’outil d’exportation [eDiscovery dans Microsoft Edge](configure-edge-to-export-search-results.md).</span><span class="sxs-lookup"><span data-stu-id="05547-126">For instructions on enabling ClickOnce support in Edge, see [Use the eDiscovery Export Tool in Microsoft Edge](configure-edge-to-export-search-results.md).</span></span>

- <span data-ttu-id="05547-127">Si la taille totale estimée des résultats renvoyés par la recherche dépasse 2 To, l’exportation des rapports échoue.</span><span class="sxs-lookup"><span data-stu-id="05547-127">If the estimated total size of the results returned by search exceeds 2 TB, exporting the reports fails.</span></span> <span data-ttu-id="05547-128">Pour exporter correctement les rapports, essayez de restreindre l’étendue et réexécutez la recherche afin que la taille estimée des résultats soit inférieure à 2 To.</span><span class="sxs-lookup"><span data-stu-id="05547-128">To successfully export the reports, try to narrow the scope and rerun the search so the estimated size of the results is less than 2 TB.</span></span>

- <span data-ttu-id="05547-129">Si les résultats d’une recherche ont plus de 7 jours et que vous soumettez un travail de rapport d’exportation, un message d’erreur s’affiche vous invite à réexécuter la recherche pour mettre à jour les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="05547-129">If the results of a search are older than 7 days and you submit an export report job, an error message is displayed prompting you to rerun the search to update the search results.</span></span> <span data-ttu-id="05547-130">Si cela se produit, annulez l’exportation, réexécutez la recherche, puis recommencez l’exportation.</span><span class="sxs-lookup"><span data-stu-id="05547-130">If this happens, cancel the export, rerun the search, and then start the export again.</span></span>

- <span data-ttu-id="05547-131">L’exportation de rapports de recherche est comptabilisée par rapport au nombre maximal d’exportations en cours d’exécution en même temps et au nombre maximal d’exportations qu’un seul utilisateur peut exécuter.</span><span class="sxs-lookup"><span data-stu-id="05547-131">Exporting search reports counts against the maximum number of exports running at the same time and the maximum number of exports that a single user can run.</span></span> <span data-ttu-id="05547-132">Pour plus d’informations sur les limites d’exportation, voir Exporter les résultats [de recherche de contenu.](export-search-results.md#export-limits)</span><span class="sxs-lookup"><span data-stu-id="05547-132">For more information about export limits, see [Export Content search results](export-search-results.md#export-limits).</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="05547-133">Étape 1 : Générer le rapport pour l’exportation</span><span class="sxs-lookup"><span data-stu-id="05547-133">Step 1: Generate the report for export</span></span>

<span data-ttu-id="05547-134">La première étape consiste à préparer le rapport pour le téléchargement vers l’exportation de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="05547-134">The first step is to prepare the report for downloading to your computer exporting.</span></span> <span data-ttu-id="05547-135">Lorsque vous exportez le rapport, les documents de rapport sont téléchargés vers une stockage Azure dans le cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05547-135">When you export the report, the report documents are uploaded to an Azure Storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="05547-136">Dans le centre Microsoft 365 conformité, sélectionnez la recherche de contenu à partir de celle à partir de qui vous souhaitez exporter le rapport.</span><span class="sxs-lookup"><span data-stu-id="05547-136">In the Microsoft 365 compliance center, select the Content search that you want to export the report from.</span></span>
  
2. <span data-ttu-id="05547-137">Dans le menu **Actions** en bas de la page de menu volant de recherche, cliquez sur **Exporter le rapport.**</span><span class="sxs-lookup"><span data-stu-id="05547-137">On the **Actions** menu at the bottom of the search flyout page, click **Export report**.</span></span>

   ![Option Exporter le rapport dans le menu Actions](../media/ActionMenuExportReport.png)

   <span data-ttu-id="05547-139">La page **de présentation** du rapport d’exportation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="05547-139">The **Export report** flyout page is displayed.</span></span> <span data-ttu-id="05547-140">Les options de rapport d’exportation disponibles pour exporter des informations sur la recherche varient selon que les résultats de la recherche sont situés dans des boîtes aux lettres ou des sites ou une combinaison des deux.</span><span class="sxs-lookup"><span data-stu-id="05547-140">The export report options available to export information about the search depend on whether search results are located in mailboxes or sites or a combination of both.</span></span>
  
3. <span data-ttu-id="05547-141">Sous **Options de sortie,** choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="05547-141">Under **Output options**, choose one of the following options:</span></span>
  
   ![Exporter les options de sortie](../media/ExportOutputOptions.png)

    - <span data-ttu-id="05547-143">Tous les éléments, à l’exception de ceux dont le format n’est pas reconnu, sont chiffrés ou n’ont pas été **indexés pour d’autres raisons.**</span><span class="sxs-lookup"><span data-stu-id="05547-143">**All items, excluding ones that have unrecognized format, are encrypted, or weren't indexed for other reasons**.</span></span> <span data-ttu-id="05547-144">Cette option exporte uniquement les informations sur les éléments indexés.</span><span class="sxs-lookup"><span data-stu-id="05547-144">This option only exports information about indexed items.</span></span>
  
    - <span data-ttu-id="05547-145">Tous les éléments, y compris ceux qui ont un format non reconnu, sont chiffrés ou n’ont pas été **indexés pour d’autres raisons.**</span><span class="sxs-lookup"><span data-stu-id="05547-145">**All items, including ones that have unrecognized format, are encrypted, or weren't indexed for other reasons**.</span></span> <span data-ttu-id="05547-146">Cette option exporte des informations sur les éléments indexés et non indexés.</span><span class="sxs-lookup"><span data-stu-id="05547-146">This option exports information about indexed and unindexed items.</span></span>
  
    - <span data-ttu-id="05547-147">Seuls les éléments qui ont un format non reconnu, sont chiffrés ou n’ont pas été indexés pour **d’autres raisons.**</span><span class="sxs-lookup"><span data-stu-id="05547-147">**Only items that have an unrecognized format, are encrypted, or weren't indexed for other reasons**.</span></span> <span data-ttu-id="05547-148">Cette option exporte uniquement les informations sur les éléments nonndex.</span><span class="sxs-lookup"><span data-stu-id="05547-148">This option only exports information about unindexed items.</span></span>

4. <span data-ttu-id="05547-149">Configurez **l’option Activer la déplication pour Exchange contenu.**</span><span class="sxs-lookup"><span data-stu-id="05547-149">Configure the **Enable de-duplication for Exchange content** option.</span></span>
  
   - <span data-ttu-id="05547-150">Si vous sélectionnez cette option, le nombre de messages en double (avant la déplication et après la déplication) est inclus dans le rapport récapitulatif d’exportation.</span><span class="sxs-lookup"><span data-stu-id="05547-150">If you select this option, the count of duplicate messages (before de-duplication and after de-duplication) is included in the export summary report.</span></span> <span data-ttu-id="05547-151">En outre, une seule copie d’un message sera incluse dans le fichier manifest.xml'</span><span class="sxs-lookup"><span data-stu-id="05547-151">Also, only one copy of a message will be included in the manifest.xml file.</span></span> <span data-ttu-id="05547-152">Toutefois, le rapport des résultats de l’exportation contient une ligne pour chaque copie d’un message en double afin que vous pouvez identifier les boîtes aux lettres qui contiennent une copie du message en double.</span><span class="sxs-lookup"><span data-stu-id="05547-152">But the export results report will contain a row for every copy of a duplicate message so that you can identify the mailboxes that contain a copy of the duplicate message.</span></span> <span data-ttu-id="05547-153">Pour plus d’informations sur les rapports exportés, voir Ce qui [est inclus dans le rapport.](#whats-included-in-the-report)</span><span class="sxs-lookup"><span data-stu-id="05547-153">For more information about the exported reports, see [What's included in the report](#whats-included-in-the-report).</span></span>

   - <span data-ttu-id="05547-154">Si vous ne sélectionnez pas cette option, les rapports d’exportation contiennent des informations sur tous les messages renvoyés par la recherche, y compris les doublons.</span><span class="sxs-lookup"><span data-stu-id="05547-154">If you don't select this option, the export reports will contain information about all messages returned by the search, including duplicates.</span></span>

     <span data-ttu-id="05547-155">Pour plus d’informations sur la dédoplication et la façon dont les éléments dupliqués sont identifiés, voir Dédoplication dans les résultats de recherche [eDiscovery](de-duplication-in-ediscovery-search-results.md).</span><span class="sxs-lookup"><span data-stu-id="05547-155">For more information about de-duplication and how duplicate items are identified, see [De-duplication in eDiscovery search results](de-duplication-in-ediscovery-search-results.md).</span></span>

5. <span data-ttu-id="05547-156">Cliquez **sur Générer un rapport.**</span><span class="sxs-lookup"><span data-stu-id="05547-156">Click **Generate report**.</span></span>

   <span data-ttu-id="05547-157">Les rapports de recherche sont préparés pour le téléchargement, ce qui signifie que les documents de rapport sont téléchargés vers un emplacement stockage Azure dans le cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05547-157">The search reports are prepared for downloading, which means the report documents are uploaded to an Azure Storage location in the Microsoft cloud.</span></span> <span data-ttu-id="05547-158">L'opération peut prendre plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="05547-158">This may take several minutes.</span></span>

<span data-ttu-id="05547-159">Consultez la section suivante pour obtenir des instructions sur le téléchargement des rapports de recherche exportés.</span><span class="sxs-lookup"><span data-stu-id="05547-159">See the next section for instructions to download the exported search reports.</span></span>
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="05547-160">Étape 2 : Télécharger le rapport</span><span class="sxs-lookup"><span data-stu-id="05547-160">Step 2: Download the report</span></span>

<span data-ttu-id="05547-161">L’étape suivante consiste à télécharger le rapport à partir de la stockage Azure sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="05547-161">The next step is to download the report from the Azure Storage area to your local computer.</span></span>

1. <span data-ttu-id="05547-162">Dans la page **Recherche de** contenu dans le centre Microsoft 365 conformité, sélectionnez **l’onglet** Exportation</span><span class="sxs-lookup"><span data-stu-id="05547-162">On the **Content search** page in the Microsoft 365 compliance center, select the **Exports** tab</span></span>
  
   <span data-ttu-id="05547-163">Vous de devez peut-être cliquer sur **Actualiser** pour mettre à jour la liste des tâches d’exportation afin qu’elle affiche la tâche d’exportation que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="05547-163">You may have to click **Refresh** to update the list of export jobs so that it shows the export job you created.</span></span> <span data-ttu-id="05547-164">Les travaux de rapport d’exportation ont le même nom que la recherche correspondante avec **_ReportsOnly** au nom de recherche.</span><span class="sxs-lookup"><span data-stu-id="05547-164">Export report jobs have the same name as the corresponding search with **_ReportsOnly** appended to the search name.</span></span>
  
2. <span data-ttu-id="05547-165">Sélectionnez la tâche d’exportation que vous avez créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="05547-165">Select the export job that you created in Step 1.</span></span>

3. <span data-ttu-id="05547-166">Dans la page **volant du rapport** d’exportation sous la clé **d’exportation,** cliquez **sur Copier dans le Presse-papiers.**</span><span class="sxs-lookup"><span data-stu-id="05547-166">On the **Export report** flyout page under **Export key**, click **Copy to clipboard**.</span></span> <span data-ttu-id="05547-167">Vous utilisez cette clé à l’étape 6 pour télécharger les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="05547-167">You use this key in step 6 to download the search results.</span></span>
  
   > [!IMPORTANT]
   > <span data-ttu-id="05547-168">Étant donné que tout le monde peut installer et démarrer l’outil d’exportation eDiscovery, puis utiliser cette clé pour télécharger le rapport de recherche, prenez toutes les précautions nécessaires pour protéger cette clé comme vous le feriez pour protéger les mots de passe ou d’autres informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="05547-168">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span>

4. <span data-ttu-id="05547-169">En haut de la page volante, cliquez sur **Télécharger les résultats.**</span><span class="sxs-lookup"><span data-stu-id="05547-169">At the top of the flyout page, click **Download results**.</span></span>

5. <span data-ttu-id="05547-170">Si vous êtes invité à installer l’outil **d’exportation eDiscovery,** cliquez sur **Installer.**</span><span class="sxs-lookup"><span data-stu-id="05547-170">If you're prompted to install the **eDiscovery Export Tool**, click **Install**.</span></span>

6. <span data-ttu-id="05547-171">Dans **l’outil d’exportation eDiscovery,** faites les choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="05547-171">In the **eDiscovery Export Tool**, do the following:</span></span>

   ![Outil d’exportation eDiscovery](../media/eDiscoveryExportTool.png)

   1. <span data-ttu-id="05547-173">Collez la clé d’exportation que vous avez copiée à l’étape 3 dans la zone appropriée.</span><span class="sxs-lookup"><span data-stu-id="05547-173">Paste the export key that you copied in step 3 in the appropriate box.</span></span>
  
   2. <span data-ttu-id="05547-174">Cliquez **sur Parcourir** pour spécifier l’emplacement où vous souhaitez télécharger les fichiers de rapport de recherche.</span><span class="sxs-lookup"><span data-stu-id="05547-174">Click **Browse** to specify the location where you want to download the search report files.</span></span>

7. <span data-ttu-id="05547-175">Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="05547-175">Click **Start** to download the search results to your computer.</span></span>
  
    <span data-ttu-id="05547-176">L’**outil d’exportation de découverte électronique** affiche l’état du processus d’exportation, ainsi qu’une estimation du nombre (et de la taille) d’éléments qui doivent encore être téléchargés.</span><span class="sxs-lookup"><span data-stu-id="05547-176">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded.</span></span> <span data-ttu-id="05547-177">Une fois le processus d’exportation terminé, vous pouvez accéder aux fichiers à l’emplacement où ils ont été téléchargés.</span><span class="sxs-lookup"><span data-stu-id="05547-177">When the export process is complete, you can access the files in the location where they were downloaded.</span></span>
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="05547-178">Ce qui est inclus dans le rapport</span><span class="sxs-lookup"><span data-stu-id="05547-178">What's included in the report</span></span>

<span data-ttu-id="05547-179">Lorsque vous générez et exportez un rapport sur les résultats d’une recherche de contenu, les documents suivants sont téléchargés :</span><span class="sxs-lookup"><span data-stu-id="05547-179">When you generate and export a report about the results of a Content search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="05547-180">**Résumé de l’exportation :** Un Excel qui contient un résumé de l’exportation.</span><span class="sxs-lookup"><span data-stu-id="05547-180">**Export summary:** An Excel document that contains a summary of the export.</span></span> <span data-ttu-id="05547-181">Cela inclut des informations telles que le nombre de sources de contenu qui ont fait l’objet d’une recherche, le nombre de résultats de recherche à partir de chaque emplacement de contenu, le nombre estimé d’éléments, le nombre réel d’éléments à exporter et la taille estimée et réelle des éléments à exporter.</span><span class="sxs-lookup"><span data-stu-id="05547-181">This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span>

   <span data-ttu-id="05547-182">Si vous incluez des éléments nonndes lors de l’exportation du rapport, le nombre d’éléments nonndex est inclus dans le nombre total de résultats de recherche estimés et dans le nombre total de résultats de recherche téléchargés (si vous de étiez pour exporter les résultats de recherche) répertoriés dans le rapport récapitulatif d’exportation.</span><span class="sxs-lookup"><span data-stu-id="05547-182">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the export summary report.</span></span> <span data-ttu-id="05547-183">En d’autres termes, le nombre total d’éléments à télécharger est égal au nombre total de résultats estimés et au nombre total d’éléments nonndex.</span><span class="sxs-lookup"><span data-stu-id="05547-183">In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span>
  
- <span data-ttu-id="05547-184">**Manifeste :** Fichier manifeste (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="05547-184">**Manifest:** A manifest file (in XML format) that contains information about each item included in the search results.</span></span> <span data-ttu-id="05547-185">Si vous avez activé l’option de déplication, les messages en double ne sont pas inclus dans le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="05547-185">If you enabled the de-duplication option, duplicate message are not included in the manifest file.</span></span>

- <span data-ttu-id="05547-186">**Résultats :** Un Excel qui contient une ligne contenant des informations sur chaque élément indexé qui serait exporté avec les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="05547-186">**Results:** An Excel document that contains a row with information about each indexed item that would be exported with the search results.</span></span> <span data-ttu-id="05547-187">Pour le courrier électronique, le journal des résultats contient des informations sur chaque message, y compris :</span><span class="sxs-lookup"><span data-stu-id="05547-187">For email, the result log contains information about each message, including:</span></span> 

  - <span data-ttu-id="05547-188">l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;</span><span class="sxs-lookup"><span data-stu-id="05547-188">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>

  - <span data-ttu-id="05547-189">la date à laquelle le message a été envoyé ou reçu ;</span><span class="sxs-lookup"><span data-stu-id="05547-189">The date the message was sent or received.</span></span>

  - <span data-ttu-id="05547-190">l’objet du message ;</span><span class="sxs-lookup"><span data-stu-id="05547-190">The Subject line from the message.</span></span>

  - <span data-ttu-id="05547-191">l’expéditeur et les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="05547-191">The sender and recipients of the message.</span></span>

  <span data-ttu-id="05547-192">Pour les documents provenant SharePoint sites OneDrive Entreprise sites web, le journal des résultats contient des informations sur chaque document, notamment :</span><span class="sxs-lookup"><span data-stu-id="05547-192">For documents from SharePoint and OneDrive for Business sites, the results log contains information about each document, including:</span></span>

  - <span data-ttu-id="05547-193">l’URL du document ;</span><span class="sxs-lookup"><span data-stu-id="05547-193">The URL for the document.</span></span>

  - <span data-ttu-id="05547-194">l’URL de la collection de sites qui héberge le document ;</span><span class="sxs-lookup"><span data-stu-id="05547-194">The URL for the site collection where the document is located.</span></span>

  - <span data-ttu-id="05547-195">la date à laquelle le document a été modifié pour la dernière fois ;</span><span class="sxs-lookup"><span data-stu-id="05547-195">The date that the document was last modified.</span></span>

  - <span data-ttu-id="05547-196">le nom du document (qui se trouve dans la colonne Objet du journal des résultats).</span><span class="sxs-lookup"><span data-stu-id="05547-196">The name of the document (which is located in the Subject column in the result log).</span></span>

  > [!NOTE]
  > <span data-ttu-id="05547-197">Le nombre de lignes  dans le rapport résultats doit être égal au nombre total de résultats de recherche moins le nombre total d’éléments répertoriés dans le rapport Éléments **nonndes.**</span><span class="sxs-lookup"><span data-stu-id="05547-197">The number of rows in the **Results** report should be equal to the total number of search results minus the total number of items listed in the **Unindexed Items** report.</span></span>
  
- <span data-ttu-id="05547-198">**Trace.log :** journal de suivi qui contient des informations de journalisation détaillées sur le processus d’exportation et peut vous aider à découvrir les problèmes pendant l’exportation.</span><span class="sxs-lookup"><span data-stu-id="05547-198">**Trace.log**: A trace log that contains detailed logging information about the export process and can help uncover issues during export.</span></span> <span data-ttu-id="05547-199">Si vous ouvrez un ticket avec le Support Microsoft à propos d’un problème lié à l’exportation de rapports de recherche, vous pouvez être invité à fournir ce journal de suivi.</span><span class="sxs-lookup"><span data-stu-id="05547-199">If you open a ticket with Microsoft Support about an issue related to exporting search reports, you may be asked to provide this trace log.</span></span>

- <span data-ttu-id="05547-200">**Éléments nonndexés :** Un Excel qui contient des informations sur les éléments non nonndes inclus dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="05547-200">**Unindexed items:** An Excel document that contains information about any unindexed items included in the search results.</span></span> <span data-ttu-id="05547-201">Si vous n’incluez pas d’éléments nonndex lorsque vous générez le rapport de résultats de recherche, ce rapport sera toujours téléchargé, mais il sera vide.</span><span class="sxs-lookup"><span data-stu-id="05547-201">If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
