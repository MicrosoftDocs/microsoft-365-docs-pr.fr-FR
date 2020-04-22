---
title: Utiliser la recherche de contenu pour les regroupements ciblés
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
- SPO_Content
localization_priority: Normal
search.appverid: MOE150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Utilisez la recherche de contenu dans le centre de sécurité & conformité pour effectuer des collections ciblées. Une collection ciblée signifie que vous êtes sûr que les éléments réactifs à un cas ou des éléments privilégiés se trouvent dans une boîte aux lettres ou un dossier de site spécifique. Utilisez le script de cet article pour obtenir l’ID de dossier ou le chemin d’accès de la boîte aux lettres ou des dossiers de site spécifiques sur lesquels vous souhaitez effectuer une recherche.
ms.openlocfilehash: e6de817e7ec324e6aa80ef596340906c2f86d126
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43633379"
---
# <a name="use-content-search-for-targeted-collections"></a><span data-ttu-id="939fd-105">Utiliser la recherche de contenu pour les regroupements ciblés</span><span class="sxs-lookup"><span data-stu-id="939fd-105">Use Content Search for targeted collections</span></span>

<span data-ttu-id="939fd-106">La fonctionnalité de recherche de contenu dans &amp; le centre de sécurité et de conformité ne fournit pas une méthode directe dans l’interface utilisateur pour rechercher des dossiers spécifiques dans des boîtes aux lettres Exchange ou des sites SharePoint et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="939fd-106">The Content Search feature in the Security &amp; Compliance Center doesn't provide a direct way in the UI to search specific folders in Exchange mailboxes or SharePoint and OneDrive for Business sites.</span></span> <span data-ttu-id="939fd-107">Toutefois, il est possible de rechercher des dossiers spécifiques (appelés une *collection ciblée*) en spécifiant la propriété ID de dossier pour la propriété email ou Path (DocumentLink) pour les sites dans la syntaxe de requête de recherche réelle.</span><span class="sxs-lookup"><span data-stu-id="939fd-107">However, it's possible to search specific folders (called a *targeted collection*) by specifying the folder ID property for email or path (DocumentLink) property for sites in the actual search query syntax.</span></span> <span data-ttu-id="939fd-108">L’utilisation de la recherche de contenu pour effectuer une collection ciblée est utile lorsque vous êtes certain que les éléments réactifs à un cas ou des éléments privilégiés se trouvent dans une boîte aux lettres ou un dossier de site spécifique.</span><span class="sxs-lookup"><span data-stu-id="939fd-108">Using Content Search to perform a targeted collection is useful when you're confident that items responsive to a case or privileged items are located in a specific mailbox or site folder.</span></span> <span data-ttu-id="939fd-109">Vous pouvez utiliser le script de cet article pour obtenir l’ID de dossier pour les dossiers de boîte aux lettres ou le chemin d’accès (DocumentLink) pour les dossiers sur un site SharePoint et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="939fd-109">You can use the script in this article to obtain the folder ID for mailbox folders or the path (DocumentLink) for folders on a SharePoint and OneDrive for Business site.</span></span> <span data-ttu-id="939fd-110">Vous pouvez ensuite utiliser le chemin d’accès ou l’ID du dossier dans une requête de recherche pour renvoyer les éléments se trouvant dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="939fd-110">Then you can use the folder ID or path in a search query to return items located in the folder.</span></span>

> [!NOTE]
> <span data-ttu-id="939fd-111">Pour renvoyer du contenu se trouvant dans un dossier dans un site SharePoint ou OneDrive entreprise, le script de cette rubrique utilise la propriété gérée DocumentLink au lieu de la propriété Path.</span><span class="sxs-lookup"><span data-stu-id="939fd-111">To return content located in a folder in a SharePoint or OneDrive for Business site, the script in this topic uses the DocumentLink managed property instead of the Path property.</span></span> <span data-ttu-id="939fd-112">La propriété DocumentLink est plus robuste que la propriété Path, car elle renverra tout le contenu d’un dossier, tandis que la propriété Path ne renverra pas certains fichiers multimédias.</span><span class="sxs-lookup"><span data-stu-id="939fd-112">The DocumentLink property is more robust than the Path property because it will return all content in a folder, whereas the Path property won't return some media files.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="939fd-113">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="939fd-113">Before you begin</span></span>

- <span data-ttu-id="939fd-114">Vous devez être membre du groupe de rôles gestionnaire eDiscovery dans le centre de sécurité &amp; conformité pour exécuter le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="939fd-114">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script in Step 1.</span></span> <span data-ttu-id="939fd-115">Pour plus d'informations, voir [Attribution d'autorisations eDiscovery](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="939fd-115">For more information, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>
    
    <span data-ttu-id="939fd-116">De plus, vous devez disposer du rôle destinataires de messagerie dans votre organisation Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="939fd-116">Additionally, you have to be assigned the Mail Recipients role in your Exchange Online organization.</span></span> <span data-ttu-id="939fd-117">Cette opération est nécessaire pour exécuter la cmdlet **Get-MailboxFolderStatistics** , qui est incluse dans le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="939fd-117">This is required to run the **Get-MailboxFolderStatistics** cmdlet, which is included in the script in Step 1.</span></span> <span data-ttu-id="939fd-118">Par défaut, le rôle destinataires de messagerie est affecté aux groupes de rôles gestion de l’organisation et gestion des destinataires dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="939fd-118">By default, the Mail Recipients role is assigned to the Organization Management and Recipient Management role groups in Exchange Online.</span></span> <span data-ttu-id="939fd-119">Pour plus d’informations sur l’attribution d’autorisations dans Exchange Online, consultez la rubrique [Manage Role Group members](https://go.microsoft.com/fwlink/p/?linkid=692102).</span><span class="sxs-lookup"><span data-stu-id="939fd-119">For more information about assigning permissions in Exchange Online, see [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102).</span></span> <span data-ttu-id="939fd-120">Vous pouvez également créer un groupe de rôles personnalisé, lui attribuer le rôle destinataires de messagerie, puis ajouter les membres qui doivent exécuter le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="939fd-120">You could also create a custom role group, assign the Mail Recipients role to it, and then add the members who need to run the script in Step 1.</span></span> <span data-ttu-id="939fd-121">Pour plus d'informations, consultez la rubrique [Gérer des groupes de rôles](https://go.microsoft.com/fwlink/p/?linkid=730688).</span><span class="sxs-lookup"><span data-stu-id="939fd-121">For more information, see [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).</span></span>
    
- <span data-ttu-id="939fd-122">Chaque fois que vous exécutez le script à l’étape 1, une nouvelle session PowerShell distante est créée.</span><span class="sxs-lookup"><span data-stu-id="939fd-122">Each time you run the script in Step 1, a new remote PowerShell session is created.</span></span> <span data-ttu-id="939fd-123">Vous pouvez donc utiliser toutes les sessions PowerShell distantes disponibles.</span><span class="sxs-lookup"><span data-stu-id="939fd-123">So you could use up all the remote PowerShell sessions available to you.</span></span> <span data-ttu-id="939fd-124">Pour éviter ce problème, vous pouvez exécuter la commande suivante pour déconnecter vos sessions PowerShell à distance actives.</span><span class="sxs-lookup"><span data-stu-id="939fd-124">To prevent this from happening, you can run the following command to disconnect your active remote PowerShell sessions.</span></span>
    
  ```powershell
  Get-PSSession | Remove-PSSession
  ```

    <span data-ttu-id="939fd-125">Pour plus d'informations, reportez-vous à [Connexion à Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="939fd-125">For more information, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="939fd-126">Le script inclut une gestion des erreurs minimale.</span><span class="sxs-lookup"><span data-stu-id="939fd-126">The script includes minimal error handling.</span></span> <span data-ttu-id="939fd-127">Le principal objectif du script est d’afficher rapidement une liste des ID de dossier ou des chemins d’accès de site qui peuvent être utilisés dans la syntaxe de requête de recherche d’une recherche de contenu pour effectuer une collection ciblée.</span><span class="sxs-lookup"><span data-stu-id="939fd-127">The primary purpose of the script is to quickly display a list of mailbox folder IDs or site paths that can be used in the search query syntax of a Content Search to perform a targeted collection.</span></span>
    
- <span data-ttu-id="939fd-128">L’exemple de script fourni dans cette rubrique n’est pas pris en charge dans le cadre d’un service ou d’un programme de support standard Microsoft.</span><span class="sxs-lookup"><span data-stu-id="939fd-128">The sample script provided in this topic isn't supported under any Microsoft standard support program or service.</span></span> <span data-ttu-id="939fd-129">L’exemple de script est fourni en l’État sans aucune garantie.</span><span class="sxs-lookup"><span data-stu-id="939fd-129">The sample script is provided AS IS without warranty of any kind.</span></span> <span data-ttu-id="939fd-130">Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d'adéquation à un usage particulier.</span><span class="sxs-lookup"><span data-stu-id="939fd-130">Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span></span> <span data-ttu-id="939fd-131">L’ensemble des risques liés à l’utilisation ou aux performances de l’exemple de script et de la documentation reste avec vous.</span><span class="sxs-lookup"><span data-stu-id="939fd-131">The entire risk arising out of the use or performance of the sample script and documentation remains with you.</span></span> <span data-ttu-id="939fd-132">En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d'activité, perte d'informations commerciales ou toute autre perte pécuniaire) découlant de l'utilisation ou de l'impossibilité d'utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="939fd-132">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a><span data-ttu-id="939fd-133">Étape 1 : exécuter le script pour obtenir la liste des dossiers d’une boîte aux lettres ou d’un site</span><span class="sxs-lookup"><span data-stu-id="939fd-133">Step 1: Run the script to get a list of folders for a mailbox or site</span></span>

<span data-ttu-id="939fd-134">Le script que vous exécutez dans cette première étape renverra une liste de dossiers de boîte aux lettres ou de dossiers SharePoint et OneDrive entreprise, ainsi que le chemin d’accès ou l’ID de dossier correspondant pour chaque dossier.</span><span class="sxs-lookup"><span data-stu-id="939fd-134">The script that you run in this first step will return a list of mailbox folders or SharePoint and OneDrive for Business folders, and the corresponding folder ID or path for each folder.</span></span> <span data-ttu-id="939fd-135">Lorsque vous exécutez ce script, il vous invite à fournir les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="939fd-135">When you run this script, it will prompt you for the following information.</span></span>
  
- <span data-ttu-id="939fd-136">**Adresse de messagerie ou URL de site** Tapez une adresse de messagerie du dépositaire pour renvoyer la liste des dossiers de boîte aux lettres Exchange et les ID de dossier.</span><span class="sxs-lookup"><span data-stu-id="939fd-136">**Email address or site URL** Type an email address of the custodian to return a list of Exchange mailbox folders and folder IDs.</span></span> <span data-ttu-id="939fd-137">Ou tapez l’URL d’un site SharePoint ou d’un site OneDrive entreprise pour renvoyer une liste de chemins d’accès pour le site spécifié.</span><span class="sxs-lookup"><span data-stu-id="939fd-137">Or type the URL for a SharePoint site or a OneDrive for Business site to return a list of paths for the specified site.</span></span> <span data-ttu-id="939fd-138">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="939fd-138">Here are some examples:</span></span> 
    
  - <span data-ttu-id="939fd-139">**Exchange** -stacig@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="939fd-139">**Exchange** - stacig@contoso.onmicrosoft.com</span></span> 
    
  - <span data-ttu-id="939fd-140">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span><span class="sxs-lookup"><span data-stu-id="939fd-140">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span></span> 
    
  - <span data-ttu-id="939fd-141">**OneDrive entreprise** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span><span class="sxs-lookup"><span data-stu-id="939fd-141">**OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span></span> 
    
- <span data-ttu-id="939fd-142">**Vos informations d’identification utilisateur** : le script utilisera vos informations d’identification pour vous connecter à Exchange Online et le centre de sécurité & conformité à l’aide de PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="939fd-142">**Your user credentials** - The script will use your credentials to connect to Exchange Online and the Security & Compliance Center with remote PowerShell.</span></span> <span data-ttu-id="939fd-143">Comme expliqué précédemment, vous devez disposer des autorisations appropriées pour exécuter ce script.</span><span class="sxs-lookup"><span data-stu-id="939fd-143">As previously explained, you have to assigned the appropriate permissions to successfully run this script.</span></span>
    
<span data-ttu-id="939fd-144">Pour afficher la liste des dossiers de boîte aux lettres ou documentlink de site (chemin d’accès), procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="939fd-144">To display a list of mailbox folders or site documentlink (path) names:</span></span>
  
1. <span data-ttu-id="939fd-145">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, `GetFolderSearchParameters.ps1`.</span><span class="sxs-lookup"><span data-stu-id="939fd-145">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `GetFolderSearchParameters.ps1`.</span></span>
    
  ```powershell
  #########################################################################################################
  # This PowerShell script will prompt you for:                                #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security & Compliance Center.            #
  # The script will then:                                            #
  #    * If an email address is supplied: list the folders for the target mailbox.            #
  #    * If a SharePoint or OneDrive for Business site is supplied: list the documentlinks (folder paths) #
  #    * for the site.                                                                                    #
  #    * In both cases, the script supplies the correct search properties (folderid: or documentlink:)    #
  #      appended to the folder ID or documentlink to use in a Content Search.                #
  # Notes:                                                #
  #    * For SharePoint and OneDrive for Business, the paths are searched recursively; this means the     #
  #      the current folder and all sub-folders are searched.                        #
  #    * For Exchange, only the specified folder will be searched; this means sub-folders in the folder    #
  #      will not be searched.  To search sub-folders, you need to use the specify the folder ID for    #
  #      each sub-folder that you want to search.                                #
  #    * For Exchange, only folders in the user's primary mailbox will be returned by the script.        #
  #########################################################################################################
  # Collect the target email address or SharePoint Url
  $addressOrSite = Read-Host "Enter an email address or a URL for a SharePoint or OneDrive for Business site"
  # Authenticate with Exchange Online and the Security & Compliance Center (Exchange Online Protection - EOP)
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  if ($addressOrSite.IndexOf("@") -ige 0)
  {
      # List the folder Ids for the target mailbox
      $emailAddress = $addressOrSite
      # Authenticate with Exchange Online
      if (!$ExoSession)
      {
          $ExoSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid/ -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $ExoSession -AllowClobber -DisableNameChecking
      }
      $folderQueries = @()
      $folderStatistics = Get-MailboxFolderStatistics $emailAddress
      foreach ($folderStatistic in $folderStatistics)
      {
          $folderId = $folderStatistic.FolderId;
          $folderPath = $folderStatistic.FolderPath;
          $encoding= [System.Text.Encoding]::GetEncoding("us-ascii")
          $nibbler= $encoding.GetBytes("0123456789ABCDEF");
          $folderIdBytes = [Convert]::FromBase64String($folderId);
          $indexIdBytes = New-Object byte[] 48;
          $indexIdIdx=0;
          $folderIdBytes | select -skip 23 -First 24 | %{$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -shr 4];$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -band 0xF]}
          $folderQuery = "folderid:$($encoding.GetString($indexIdBytes))";
          $folderStat = New-Object PSObject
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderPath -Value $folderPath
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderQuery -Value $folderQuery
          $folderQueries += $folderStat
      }
      Write-Host "-----Exchange Folders-----"
      $folderQueries |ft
  }
  elseif ($addressOrSite.IndexOf("http") -ige 0)
  {
      $searchName = "SPFoldersSearch"
      $searchActionName = "SPFoldersSearch_Preview"
      # List the folders for the SharePoint or OneDrive for Business Site
      $siteUrl = $addressOrSite
      # Authenticate with the Security & Compliance Center
      if (!$SccSession)
      {
          $SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $SccSession -AllowClobber -DisableNameChecking
      }
      # Clean-up, if the script was aborted, the search we created might not have been deleted.  Try to do so now.
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
      # Create a Content Search against the SharePoint Site or OneDrive for Business site and only search for folders; wait for the search to complete
      $complianceSearch = New-ComplianceSearch -Name $searchName -ContentMatchQuery "contenttype:folder" -SharePointLocation $siteUrl
      Start-ComplianceSearch $searchName
      do{
          Write-host "Waiting for search to complete..."
          Start-Sleep -s 5
          $complianceSearch = Get-ComplianceSearch $searchName
      }while ($complianceSearch.Status -ne 'Completed')
      if ($complianceSearch.Items -gt 0)
      {
          # Create a Compliance Search Action and wait for it to complete. The folders will be listed in the .Results parameter
          $complianceSearchAction = New-ComplianceSearchAction -SearchName $searchName -Preview
          do
          {
              Write-host "Waiting for search action to complete..."
              Start-Sleep -s 5
              $complianceSearchAction = Get-ComplianceSearchAction $searchActionName
          }while ($complianceSearchAction.Status -ne 'Completed')
          # Get the results and print out the folders
          $results = $complianceSearchAction.Results
          $matches = Select-String "Data Link:.+[,}]" -Input $results -AllMatches
          foreach ($match in $matches.Matches)
          {
              $rawUrl = $match.Value
              $rawUrl = $rawUrl -replace "Data Link: " -replace "," -replace "}"
              Write-Host "DocumentLink:""$rawUrl"""
          }
      }
      else
      {
          Write-Host "No folders were found for $siteUrl"
      }
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
  }
  else
  {
      Write-Error "Couldn't recognize $addressOrSite as an email address or a site URL"
  }
  ```

2. <span data-ttu-id="939fd-146">Sur votre ordinateur local, ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="939fd-146">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="939fd-147">Exécutez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="939fd-147">Run the script; for example:</span></span>
    
      ```powershell
      .\GetFolderSearchParameters.ps1
      ```

4. <span data-ttu-id="939fd-148">Entrez les informations que le script vous demande.</span><span class="sxs-lookup"><span data-stu-id="939fd-148">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="939fd-149">Le script affiche la liste des dossiers de boîte aux lettres ou des dossiers de site pour l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="939fd-149">The script displays a list of mailbox folders or site folders for the specified user.</span></span> <span data-ttu-id="939fd-150">Laissez cette fenêtre ouverte afin de pouvoir copier un ID de dossier ou un nom documentlink et collez-le dans une requête de recherche à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="939fd-150">Let this window open so that you can copy a folder ID or documentlink name and paste it in to a search query in Step 2.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="939fd-151">Au lieu d’afficher une liste de dossiers sur l’écran de l’ordinateur, vous pouvez rediriger la sortie du script vers un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="939fd-151">Instead of displaying a list of folders on the computer screen, you can re-direct the output of the script to a text file.</span></span> <span data-ttu-id="939fd-152">Ce fichier sera enregistré dans le dossier où se trouve le script.</span><span class="sxs-lookup"><span data-stu-id="939fd-152">This file will be saved to the folder where the script is located.</span></span> <span data-ttu-id="939fd-153">Par exemple, pour rediriger la sortie du script vers un fichier texte, exécutez la commande suivante à l’étape `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` 3 : vous pouvez ensuite copier un ID de dossier ou documentlink à partir du fichier à utiliser dans une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="939fd-153">For example, to redirect the script output to a text file, run the following command in Step 3:  `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` Then you can copy a folder ID or documentlink from the file to use in a search query.</span></span>
  
### <a name="script-output-for-mailbox-folders"></a><span data-ttu-id="939fd-154">Sortie du script pour les dossiers de boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="939fd-154">Script output for mailbox folders</span></span>

<span data-ttu-id="939fd-155">Si vous obtenez des ID de dossier de boîte aux lettres, le script se connecte à Exchange Online à l’aide de PowerShell à distance, exécute la cmdlet **Get-MailboxFolderStatisics** , puis affiche la liste des dossiers de la boîte aux lettres spécifiée.</span><span class="sxs-lookup"><span data-stu-id="939fd-155">If you're getting mailbox folder IDs, the script connects to Exchange Online by using remote PowerShell, runs the **Get-MailboxFolderStatisics** cmdlet, and then displays the list of the folders from the specified mailbox.</span></span> <span data-ttu-id="939fd-156">Pour chaque dossier de la boîte aux lettres, le script affiche le nom du dossier dans la colonne **folderPath** et l’ID de dossier dans la colonne **FolderQuery** .</span><span class="sxs-lookup"><span data-stu-id="939fd-156">For every folder in the mailbox, the script displays the name of the folder in the **FolderPath** column and the folder ID in the **FolderQuery** column.</span></span> <span data-ttu-id="939fd-157">En outre, le script ajoute le préfixe **FolderId** (qui est le nom de la propriété Mailbox) à l’ID du dossier.</span><span class="sxs-lookup"><span data-stu-id="939fd-157">Additionally, the script adds the prefix of **folderId** (which is the name of the mailbox property) to the folder ID.</span></span> <span data-ttu-id="939fd-158">Étant donné que la propriété **FolderId** est une propriété pouvant faire l’objet `folderid:<folderid>` d’une recherche, vous utiliserez dans une requête de recherche à l’étape 2 pour rechercher ce dossier.</span><span class="sxs-lookup"><span data-stu-id="939fd-158">Because the **folderid** property is a searchable property, you'll use  `folderid:<folderid>` in a search query in Step 2 to search that folder.</span></span> <span data-ttu-id="939fd-159">Le script affiche un maximum de 100 dossiers de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="939fd-159">The script displays a maximum of 100 mailbox folders.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="939fd-160">Le script de cet article inclut une logique de codage qui convertit les valeurs d’ID de dossier de 64 caractères renvoyées par **Get-MailboxFolderStatistics** au même format de 48 caractères que celui indexé pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="939fd-160">The script in this article includes encoding logic that converts the 64-character folder Id values that are returned by **Get-MailboxFolderStatistics** to the same 48-character format that is indexed for search.</span></span> <span data-ttu-id="939fd-161">Si vous exécutez simplement la cmdlet **Get-MailboxFolderStatistics** dans PowerShell pour obtenir un ID de dossier (au lieu d’exécuter le script de cet article), une requête de recherche qui utilise cette valeur d’ID de dossier échouera.</span><span class="sxs-lookup"><span data-stu-id="939fd-161">If you just run the **Get-MailboxFolderStatistics** cmdlet in PowerShell to obtain a folder Id (instead of running the script in this article), a search query that uses that folder Id value will fail.</span></span> <span data-ttu-id="939fd-162">Vous devez exécuter le script pour obtenir les ID de dossier correctement mis en forme qui peuvent être utilisés dans une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="939fd-162">You have to run the script to get the correctly-formatted folder Ids that can be used in a Content Search.</span></span>
  
<span data-ttu-id="939fd-163">Voici un exemple de la sortie renvoyée par le script pour les dossiers de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="939fd-163">Here's an example of the output returned by the script for mailbox folders.</span></span>
  
![Exemple de liste des dossiers de boîte aux lettres et des ID de dossier renvoyés par le script](../media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
<span data-ttu-id="939fd-165">L’exemple de l’étape 2 montre la requête utilisée pour rechercher le sous-dossier purges dans le dossier éléments récupérables de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="939fd-165">The example in Step 2 shows the query used to search the Purges subfolder in the user's Recoverable Items folder.</span></span>
  
### <a name="script-output-for-site-folders"></a><span data-ttu-id="939fd-166">Sortie du script pour les dossiers de site</span><span class="sxs-lookup"><span data-stu-id="939fd-166">Script output for site folders</span></span>

<span data-ttu-id="939fd-167">Si vous obtenez le chemin d’accès de la propriété **documentlink** à partir de sites SharePoint ou OneDrive entreprise, le script se connecte au centre de sécurité & conformité à l’aide de PowerShell à distance, crée une recherche de contenu qui recherche les dossiers sur le site, puis affiche une liste des dossiers situés dans le site spécifié.</span><span class="sxs-lookup"><span data-stu-id="939fd-167">If you're getting the path of the **documentlink** property from SharePoint or OneDrive for Business sites, the script connects to the Security & Compliance Center using remote PowerShell, creates a new Content Search that searches the site for folders, and then displays a list of the folders located in the specified site.</span></span> <span data-ttu-id="939fd-168">Le script affiche le nom de chaque dossier et ajoute le préfixe **documentlink** à l’URL du dossier.</span><span class="sxs-lookup"><span data-stu-id="939fd-168">The script displays the name of each folder and adds the prefix of **documentlink** to the folder URL.</span></span> <span data-ttu-id="939fd-169">Étant donné que la propriété **documentlink** est une propriété pouvant faire l’objet `documentlink:<path>` d’une recherche, vous devez utiliser la paire propriété : valeur dans une requête de recherche à l’étape 2 pour rechercher ce dossier.</span><span class="sxs-lookup"><span data-stu-id="939fd-169">Because the **documentlink** property is a searchable property, you'll use `documentlink:<path>` property:value pair in a search query in Step 2 to search that folder.</span></span> <span data-ttu-id="939fd-170">Le script affiche un maximum de 200 dossiers de site.</span><span class="sxs-lookup"><span data-stu-id="939fd-170">The script displays a maximum of 200 site folders.</span></span> <span data-ttu-id="939fd-171">S’il y a plus de 200 dossiers de site, les plus récents sont affichés.</span><span class="sxs-lookup"><span data-stu-id="939fd-171">If there are more than 200 site folders, the newest ones are displayed.</span></span>
  
<span data-ttu-id="939fd-172">Voici un exemple de la sortie renvoyée par le script pour les dossiers de site.</span><span class="sxs-lookup"><span data-stu-id="939fd-172">Here's an example of the output returned by the script for site folders.</span></span>
  
![Exemple de liste de noms documentlink pour les dossiers de site renvoyés par le script](../media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-documentlink-to-perform-a-targeted-collection"></a><span data-ttu-id="939fd-174">Étape 2 : utiliser un ID de dossier ou documentlink pour effectuer une collection ciblée</span><span class="sxs-lookup"><span data-stu-id="939fd-174">Step 2: Use a folder ID or documentlink to perform a targeted collection</span></span>

<span data-ttu-id="939fd-175">Une fois que vous avez exécuté le script pour collecter une liste d’ID de dossiers ou de documentlinks pour un utilisateur spécifique, l’étape suivante consiste à accéder au centre de sécurité & conformité et à créer une recherche de contenu pour rechercher un dossier spécifique.</span><span class="sxs-lookup"><span data-stu-id="939fd-175">After you've run the script to collect a list of folder IDs or documentlinks for a specific user, the next step to go to the Security & Compliance Center and create a new Content Search to search a specific folder.</span></span> <span data-ttu-id="939fd-176">Vous utiliserez la `folderid:<folderid>` paire `documentlink:<path>` ou propriété : valeur dans la requête de recherche que vous configurez dans la zone mot-clé de recherche de contenu (ou en tant que valeur du paramètre *ContentMatchQuery* si vous utilisez la cmdlet **New-ComplianceSearch** ).</span><span class="sxs-lookup"><span data-stu-id="939fd-176">You'll use the  `folderid:<folderid>` or  `documentlink:<path>` property:value pair in the search query that you configure in the Content Search keyword box (or as the value for the  *ContentMatchQuery*  parameter if you use the **New-ComplianceSearch** cmdlet).</span></span> <span data-ttu-id="939fd-177">Vous pouvez combiner la `folderid` propriété `documentlink` ou avec d’autres paramètres de recherche ou conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="939fd-177">You can combine the  `folderid` or  `documentlink` property with other search parameters or search conditions.</span></span> <span data-ttu-id="939fd-178">Si vous incluez uniquement `folderid` la `documentlink` propriété ou dans la requête, la recherche renverra tous les éléments situés dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="939fd-178">If you only include the  `folderid` or  `documentlink` property in the query, the search will return all items located in the specified folder.</span></span> 
  
1. <span data-ttu-id="939fd-179">Accédez à [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="939fd-179">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="939fd-180">Connectez-vous à l’aide du compte et des informations d’identification que vous avez utilisés pour exécuter le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="939fd-180">Sign in using the account and credentials that you used to run the script in Step 1.</span></span>
    
3. <span data-ttu-id="939fd-181">Dans le volet gauche du centre de sécurité & conformité, cliquez sur recherche de **contenu**de **recherche** \> , puis cliquez sur](../media/O365-MDM-CreatePolicy-AddIcon.gif) **nouvelle** ![icône Ajouter.</span><span class="sxs-lookup"><span data-stu-id="939fd-181">In the left pane of the Security & Compliance Center, click **Search** \> **Content search**, and then click **New** ![Add icon](../media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="939fd-182">Sur la page **Nouvelle recherche**, entrez un nom pour la recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="939fd-182">On the **New search** page, type a name for the Content Search.</span></span> <span data-ttu-id="939fd-183">Ce nom doit être unique dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="939fd-183">This name has to be unique in your organization.</span></span> 
    
5. <span data-ttu-id="939fd-184">Sous **où souhaitez-vous Rechercher**, effectuez l’une des opérations suivantes, selon que vous recherchez un dossier de boîte aux lettres ou un dossier de site :</span><span class="sxs-lookup"><span data-stu-id="939fd-184">Under **Where do you want us to look**, do one of the following, based on whether you're searching a mailbox folder or a site folder:</span></span>
    
    - <span data-ttu-id="939fd-185">Cliquez sur **choisir des boîtes aux lettres spécifiques à rechercher** , puis ajoutez la même boîte aux lettres que celle que vous avez spécifiée lors de l’exécution du script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="939fd-185">Click **Choose specific mailboxes to search** and then add the same mailbox that you specified when you ran the script in Step 1.</span></span> 
    
      <span data-ttu-id="939fd-186">Ou</span><span class="sxs-lookup"><span data-stu-id="939fd-186">Or</span></span>
    
    - <span data-ttu-id="939fd-187">Cliquez sur **choisir des sites spécifiques à** Rechercher, puis ajoutez l’URL de site que vous avez spécifiée lors de l’exécution du script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="939fd-187">Click **Choose specific sites to search** to search and then add the same site URL that you specified when you ran the script in Step 1.</span></span> 
    
6. <span data-ttu-id="939fd-188">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="939fd-188">Click **Next**.</span></span>
    
7. <span data-ttu-id="939fd-189">Dans la zone mot clé de la page **que souhaitez-vous Rechercher** , collez la `folderid:<folderid>` valeur ou `documentlink:<path>` qui a été renvoyée par le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="939fd-189">In the keyword box on the **What do you want us to look for** page, paste the  `folderid:<folderid>` or  `documentlink:<path>` value that was returned by the script in Step 1.</span></span> 
    
    <span data-ttu-id="939fd-190">Par exemple, la requête de la capture d’écran suivante recherche tout élément dans le sous-dossier purges du dossier éléments récupérables de l’utilisateur (la valeur `folderid` de la propriété pour le sous-dossier purges est illustrée dans la capture d’écran de l’étape 1) :</span><span class="sxs-lookup"><span data-stu-id="939fd-190">For example, the query in the following screenshot will search for any item in the Purges subfolder in the user's Recoverable Items folder (the value of the `folderid` property for the Purges subfolder is shown in the screenshot in Step 1):</span></span>
    
    ![Coller le FolderId ou documentlink dans la zone mot clé de la requête de recherche](../media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. <span data-ttu-id="939fd-192">Cliquez sur **Rechercher** pour lancer la recherche cible de la collection.</span><span class="sxs-lookup"><span data-stu-id="939fd-192">Click **Search** to start the targeted collection search.</span></span> 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a><span data-ttu-id="939fd-193">Exemples de requêtes de recherche pour des collections ciblées</span><span class="sxs-lookup"><span data-stu-id="939fd-193">Examples of search queries for targeted collections</span></span>

<span data-ttu-id="939fd-194">Voici quelques exemples d’utilisation des propriétés `folderid` et `documentlink` dans une requête de recherche pour effectuer une collection ciblée.</span><span class="sxs-lookup"><span data-stu-id="939fd-194">Here are some examples of using the  `folderid` and  `documentlink` properties in a search query to perform a targeted collection.</span></span> <span data-ttu-id="939fd-195">Notez que les espaces réservés sont utilisés `folderid:<folderid>` pour `documentlink:<path>` économiser de l’espace.</span><span class="sxs-lookup"><span data-stu-id="939fd-195">Note that placeholders are used for  `folderid:<folderid>` and  `documentlink:<path>` to save space.</span></span> 
  
- <span data-ttu-id="939fd-196">Cet exemple montre comment rechercher trois dossiers de boîte aux lettres différents.</span><span class="sxs-lookup"><span data-stu-id="939fd-196">This example searches three different mailbox folders.</span></span> <span data-ttu-id="939fd-197">Vous pouvez utiliser une syntaxe de requête similaire pour effectuer une recherche dans les dossiers cachés dans le dossier éléments récupérables d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="939fd-197">You could use similar query syntax to search the hidden folders in a user's Recoverable Items folder.</span></span>
    
  ```powershell
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- <span data-ttu-id="939fd-198">Cet exemple montre comment rechercher dans un dossier de boîte aux lettres des éléments qui contiennent une expression exacte.</span><span class="sxs-lookup"><span data-stu-id="939fd-198">This example searches a mailbox folder for items that contain an exact phrase.</span></span>
    
  ```powershell
  folderid:<folderid> AND "Contoso financial results"
  ```

- <span data-ttu-id="939fd-199">Cet exemple montre comment rechercher dans un dossier de site (et tous les sous-dossiers) les documents qui contiennent les lettres « NDA » dans le titre.</span><span class="sxs-lookup"><span data-stu-id="939fd-199">This example searches a site folder (and any subfolders) for documents that contain the letters "NDA" in the title.</span></span>
    
  ```powershell
  documentlink:<path> AND filename:nda
  ```

- <span data-ttu-id="939fd-200">Cet exemple recherche dans un dossier de site (et dans un sous-dossier) les documents qui ont été modifiés au cours d’une plage de dates.</span><span class="sxs-lookup"><span data-stu-id="939fd-200">This example searches a site folder (and any subfolder) for documents there were changed within a date range.</span></span>
    
  ```powershell
  documentlink:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```

## <a name="more-information"></a><span data-ttu-id="939fd-201">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="939fd-201">More information</span></span>

<span data-ttu-id="939fd-202">Lors de l’utilisation du script de cet article, vous devez tenir compte des points suivants pour effectuer des collections ciblées.</span><span class="sxs-lookup"><span data-stu-id="939fd-202">Keep the following things in mind when using the script in this article to perform targeted collections.</span></span>
  
- <span data-ttu-id="939fd-203">Le script ne supprime aucun dossier des résultats.</span><span class="sxs-lookup"><span data-stu-id="939fd-203">The script doesn't remove any folders from the results.</span></span> <span data-ttu-id="939fd-204">Par conséquent, il se peut que certains dossiers figurant dans les résultats ne puissent pas faire l’objet d’une recherche (ou ne renvoient aucun élément), car ils contiennent du contenu généré par le système.</span><span class="sxs-lookup"><span data-stu-id="939fd-204">So some folders listed in the results might be unsearchable (or return zero items) because they contain system-generated content.</span></span>
    
- <span data-ttu-id="939fd-205">Ce script renvoie uniquement les informations de dossier de la boîte aux lettres principale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="939fd-205">This script only returns folder information for the user's primary mailbox.</span></span> <span data-ttu-id="939fd-206">Il ne retourne pas d’informations sur les dossiers dans la boîte aux lettres d’archivage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="939fd-206">It doesn't return information about folders in the user's archive mailbox.</span></span>
    
- <span data-ttu-id="939fd-207">Lors de la recherche de dossiers de boîte aux lettres, seul le `folderid` dossier spécifié (identifié par sa propriété) fera l’objet d’une recherche ; les sous-dossiers ne feront pas l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="939fd-207">When searching mailbox folders, only the specified folder (identified by its  `folderid` property) will be searched; subfolders won't be searched.</span></span> <span data-ttu-id="939fd-208">Pour rechercher des sous-dossiers, vous devez utiliser l’ID de dossier pour le sous-dossier dans lequel vous souhaitez effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="939fd-208">To search sub-folders, you need to use the  folder ID for the sub-folder that you want to search.</span></span> 
    
- <span data-ttu-id="939fd-209">Lors de la recherche de dossiers de site, le dossier `documentlink` (identifié par sa propriété) et tous les sous-dossiers feront l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="939fd-209">When searching site folders, the folder (identified by its  `documentlink` property) and all sub-folders will be searched.</span></span> 
    
- <span data-ttu-id="939fd-210">Lorsque vous exportez les résultats d’une recherche dans laquelle vous `folderid` avez spécifié la propriété uniquement dans la requête de recherche, vous pouvez choisir la première option d’exportation, « tous les éléments, sauf ceux dont le format n’est pas reconnu, sont chiffrés ou n’ont pas été indexés pour d’autres raisons ».</span><span class="sxs-lookup"><span data-stu-id="939fd-210">When exporting the results of a search in which you only specified the `folderid` property in the search query, you can choose the first export option, "All items, excluding ones that have an unrecognized format, are encrypted, or weren't indexed for other reasons."</span></span> <span data-ttu-id="939fd-211">Tous les éléments du dossier sont toujours exportés, quel que soit leur état d’indexation, car l’ID de dossier est toujours indexé.</span><span class="sxs-lookup"><span data-stu-id="939fd-211">All items in the folder will always be exported regardless of their indexing status because the folder ID is always indexed.</span></span>
