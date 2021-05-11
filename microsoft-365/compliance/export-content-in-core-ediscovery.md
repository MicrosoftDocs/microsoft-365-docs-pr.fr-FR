---
title: Exporter et télécharger du contenu à partir d’un cas core eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Décrit comment exporter et télécharger du contenu à partir d’un cas core eDiscovery dans Microsoft 365.
ms.openlocfilehash: 8eb54e23369ef682e8aa1ebf7e681eb34444f1cd
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52310841"
---
# <a name="export-content-from-a-core-ediscovery-case"></a><span data-ttu-id="618ae-103">Exporter du contenu à partir d’un cas core eDiscovery</span><span class="sxs-lookup"><span data-stu-id="618ae-103">Export content from a Core eDiscovery case</span></span>

<span data-ttu-id="618ae-104">Une fois qu’une recherche associée à un cas core eDiscovery a été correctement exécuté, vous pouvez exporter les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="618ae-104">After a search associated with a Core eDiscovery case is successfully run, you can export the search results.</span></span> <span data-ttu-id="618ae-105">Lorsque vous exportez des résultats de recherche, les éléments de boîte aux lettres sont téléchargés dans des fichiers PST ou sous la mesure de messages individuels.</span><span class="sxs-lookup"><span data-stu-id="618ae-105">When you export search results, mailbox items are downloaded in PST files or as individual messages.</span></span> <span data-ttu-id="618ae-106">Lorsque vous exportez du contenu à SharePoint sites OneDrive Entreprise sites, des copies de documents Office et d’autres documents sont exportées.</span><span class="sxs-lookup"><span data-stu-id="618ae-106">When you export content from SharePoint and OneDrive for Business sites, copies of native Office documents and other documents are exported.</span></span> <span data-ttu-id="618ae-107">Un Results.csv qui contient des informations sur chaque élément exporté et un fichier manifeste (au format XML) qui contient des informations sur chaque résultat de recherche est également exporté.</span><span class="sxs-lookup"><span data-stu-id="618ae-107">A Results.csv file that contains information about every item that's exported and a manifest file (in XML format) that contains information about every search result is also exported.</span></span>
  
## <a name="export-search-results"></a><span data-ttu-id="618ae-108">Exporter les résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="618ae-108">Export search results</span></span>

1. <span data-ttu-id="618ae-109">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and sign in using the credentials for user account that has been assigned the appropriate eDiscovery permissions.</span><span class="sxs-lookup"><span data-stu-id="618ae-109">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and sign in using the credentials for user account that has been assigned the appropriate eDiscovery permissions.</span></span>

2. <span data-ttu-id="618ae-110">Dans le volet de navigation gauche du centre de conformité Microsoft 365, cliquez sur Afficher **tout,** puis sur **eDiscovery > Core**.</span><span class="sxs-lookup"><span data-stu-id="618ae-110">In the left navigation pane of the Microsoft 365 compliance center, click **Show all**, and then click **eDiscovery > Core**.</span></span>

3. <span data-ttu-id="618ae-111">Dans la page **Core eDiscovery,** cliquez sur le nom du cas où vous souhaitez créer la attente.</span><span class="sxs-lookup"><span data-stu-id="618ae-111">On the **Core eDiscovery** page, click the name of the case that you want to create the hold in.</span></span>

4. <span data-ttu-id="618ae-112">Dans la page **d’accueil** du cas, cliquez sur **l’onglet Recherches.**</span><span class="sxs-lookup"><span data-stu-id="618ae-112">On the **Home** page for the case, click the **Searches** tab.</span></span>

5. <span data-ttu-id="618ae-113">Dans le menu **Actions** en bas de la page volante, cliquez sur **Exporter les résultats.**</span><span class="sxs-lookup"><span data-stu-id="618ae-113">On the **Actions** menu at the bottom of the flyout page, click **Export results**.</span></span>

   ![Option Exporter les résultats dans le menu Actions](../media/ActionMenuExportResults.png)

   <span data-ttu-id="618ae-115">Le flux de travail pour exporter les résultats d’une recherche associée à un cas core eDiscovery est identique à l’exportation des résultats de recherche pour une recherche sur la page de recherche **de** contenu.</span><span class="sxs-lookup"><span data-stu-id="618ae-115">The workflow to export the results of a search associated with a Core eDiscovery case is that same as exporting the search results for a search on the **Content search** page.</span></span> <span data-ttu-id="618ae-116">Pour obtenir des instructions détaillées, voir Exporter les résultats [de recherche de contenu.](export-search-results.md)</span><span class="sxs-lookup"><span data-stu-id="618ae-116">For step-by-step instructions, see [Export content search results](export-search-results.md).</span></span>

   > [!NOTE]
   > <span data-ttu-id="618ae-117">Lorsque vous exportez des résultats de recherche, vous avez la possibilité d’activer la dédoplication afin qu’une seule copie d’un message électronique soit exportée, même si plusieurs instances du même message ont pu être trouvées dans les boîtes aux lettres qui ont fait l’être.</span><span class="sxs-lookup"><span data-stu-id="618ae-117">When you export search results, you have the option to enable de-duplication so that only one copy of an email message is exported even though multiple instances of the same message might have been found in the mailboxes that were searched.</span></span> <span data-ttu-id="618ae-118">Pour plus d’informations sur la dédoplication et la façon dont les éléments dupliqués sont identifiés, voir Dédoplication dans les résultats de recherche [eDiscovery](de-duplication-in-ediscovery-search-results.md).</span><span class="sxs-lookup"><span data-stu-id="618ae-118">For more information about de-duplication and how duplicate items are identified, see [De-duplication in eDiscovery search results](de-duplication-in-ediscovery-search-results.md).</span></span>

   <span data-ttu-id="618ae-119">Une fois l’exportation commencée, les résultats de la recherche sont préparés pour le téléchargement, ce qui signifie qu’ils sont transférés vers un emplacement fourni par Microsoft stockage Azure dans le cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="618ae-119">After you start the export, the search results are prepared for downloading, which means they are transferred to a Microsoft-provided Azure Storage location in the Microsoft cloud.</span></span>
  
6. <span data-ttu-id="618ae-120">Cliquez sur **l’onglet Exports** dans le cas pour afficher la liste des travaux d’exportation.</span><span class="sxs-lookup"><span data-stu-id="618ae-120">Click the **Exports** tab in the case to display the list of export jobs.</span></span>
  
   ![Exporter des travaux sous l’onglet Exportation dans le cas core eDiscovery](../media/CoreeDiscoveryExport.png)

   <span data-ttu-id="618ae-122">Vous de devez peut-être cliquer sur **Actualiser** pour mettre à jour la liste des tâches d’exportation afin qu’elle affiche la tâche d’exportation que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="618ae-122">You may have to click **Refresh** to update the list of export jobs so that it shows the export job you created.</span></span> <span data-ttu-id="618ae-123">Les travaux d’exportation ont le même nom que la recherche correspondante avec **_Export** au nom de recherche.</span><span class="sxs-lookup"><span data-stu-id="618ae-123">Export jobs have the same name as the corresponding search with **_Export** appended to the search name.</span></span>

7. <span data-ttu-id="618ae-124">Cliquez sur la tâche d’exportation que vous avez créée pour afficher les informations d’état sur la page volante.</span><span class="sxs-lookup"><span data-stu-id="618ae-124">Click the export job you created to display status information on the flyout page.</span></span> <span data-ttu-id="618ae-125">Ces informations incluent le pourcentage d’éléments qui ont été transférés vers stockage Azure’emplacement.</span><span class="sxs-lookup"><span data-stu-id="618ae-125">This information includes the percentage of items that have been transferred to the Azure Storage location.</span></span>

8. <span data-ttu-id="618ae-126">Une fois tous les éléments transférés, cliquez sur **Télécharger** les résultats pour télécharger les résultats de la recherche sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="618ae-126">After all items have been transferred, click **Download results** to download the search results to your local computer.</span></span> <span data-ttu-id="618ae-127">Pour plus d’informations sur le téléchargement des résultats de recherche, voir l’étape 2 de [l’exportation des](export-search-results.md#step-2-download-the-search-results) résultats de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="618ae-127">For more information downloading search results, see Step 2 in [Export content search results](export-search-results.md#step-2-download-the-search-results)</span></span>

### <a name="more-information-about-exporting-searches-from-a-case"></a><span data-ttu-id="618ae-128">Plus d’informations sur l’exportation de recherches à partir d’un cas</span><span class="sxs-lookup"><span data-stu-id="618ae-128">More information about exporting searches from a case</span></span>

- <span data-ttu-id="618ae-129">Pour plus d’informations sur les fichiers d’exportation inclus lorsque vous exportez des résultats de recherche, voir [Exporter un rapport de recherche de contenu.](export-a-content-search-report.md#whats-included-in-the-report)</span><span class="sxs-lookup"><span data-stu-id="618ae-129">For more information about the export files that are included when you export search results, see [Export a Content search report](export-a-content-search-report.md#whats-included-in-the-report).</span></span>

- <span data-ttu-id="618ae-130">Si vous redémarrez l’exportation, les modifications apportées aux requêtes des recherches qui font la tâche d’exportation n’affecteront pas les résultats de recherche récupérés.</span><span class="sxs-lookup"><span data-stu-id="618ae-130">If you restart the export, any changes to the queries of the searches that make up the export job won't affect the search results that are retrieved.</span></span> <span data-ttu-id="618ae-131">Lorsque vous redémarrez une exportation, le même travail de requête de recherche combiné qui a été exécuté lors de la création de la tâche d’exportation est ré-exécuté.</span><span class="sxs-lookup"><span data-stu-id="618ae-131">When you restart an export, the same combined search query job that was run when the export job was created will be run again.</span></span>

- <span data-ttu-id="618ae-132">En outre, si vous redémarrez une exportation, les résultats de la recherche qui sont copiés vers l’emplacement stockage Azure de recherche ont la valeur par rapport aux résultats précédents.</span><span class="sxs-lookup"><span data-stu-id="618ae-132">Also, if you restart an export, the search results that are copied to the Azure Storage location overwrites the previous results.</span></span> <span data-ttu-id="618ae-133">Les résultats précédents qui ont été copiés ne pourront pas être téléchargés.</span><span class="sxs-lookup"><span data-stu-id="618ae-133">The previous results that were copied won't be available to be downloaded.</span></span>
