---
title: Utiliser la recherche de contenu pour les collections ciblées
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
- SPO_Content
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
ms.custom: seo-marvel-apr2020
description: Utilisez la recherche de contenu dans le centre Microsoft 365 conformité pour effectuer une collection ciblée, qui recherche des éléments dans une boîte aux lettres ou un dossier de site spécifique.
ms.openlocfilehash: cf0364d39a78e1bbbc062d85ce750d190fbbda5a
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52311896"
---
# <a name="use-content-search-for-targeted-collections"></a><span data-ttu-id="e97f1-103">Utiliser la recherche de contenu pour les collections ciblées</span><span class="sxs-lookup"><span data-stu-id="e97f1-103">Use Content search for targeted collections</span></span>

<span data-ttu-id="e97f1-104">L’outil de recherche de contenu dans le Centre de conformité Microsoft 365 ne fournit pas un moyen direct dans l’interface utilisateur de rechercher des dossiers spécifiques dans des boîtes aux lettres Exchange ou des sites SharePoint et OneDrive Entreprise web.</span><span class="sxs-lookup"><span data-stu-id="e97f1-104">The Content search tool in the Microsoft 365 compliance center doesn't provide a direct way in the UI to search specific folders in Exchange mailboxes or SharePoint and OneDrive for Business sites.</span></span> <span data-ttu-id="e97f1-105">Toutefois, il est possible de rechercher des dossiers spécifiques (appelés une *collection* ciblée) en spécifiant la propriété d’ID de dossier pour la propriété de messagerie ou de chemin d’accès (DocumentLink) pour les sites dans la syntaxe de requête de recherche réelle.</span><span class="sxs-lookup"><span data-stu-id="e97f1-105">However, it's possible to search specific folders (called a *targeted collection*) by specifying the folder ID property for email or path (DocumentLink) property for sites in the actual search query syntax.</span></span> <span data-ttu-id="e97f1-106">L’utilisation de la recherche de contenu pour effectuer une collection ciblée est utile lorsque vous êtes certain que les éléments qui répondent à un cas ou des éléments privilégiés se trouvent dans une boîte aux lettres ou un dossier de site spécifique.</span><span class="sxs-lookup"><span data-stu-id="e97f1-106">Using Content Search to perform a targeted collection is useful when you're confident that items responsive to a case or privileged items are located in a specific mailbox or site folder.</span></span> <span data-ttu-id="e97f1-107">Vous pouvez utiliser le script de cet article pour obtenir l’ID de dossier pour les dossiers de boîte aux lettres ou le chemin d’accès (DocumentLink) pour les dossiers sur un site SharePoint et OneDrive Entreprise site.</span><span class="sxs-lookup"><span data-stu-id="e97f1-107">You can use the script in this article to obtain the folder ID for mailbox folders or the path (DocumentLink) for folders on a SharePoint and OneDrive for Business site.</span></span> <span data-ttu-id="e97f1-108">Ensuite, vous pouvez utiliser l’ID de dossier ou le chemin d’accès dans une requête de recherche pour renvoyer les éléments situés dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="e97f1-108">Then you can use the folder ID or path in a search query to return items located in the folder.</span></span>

> [!NOTE]
> <span data-ttu-id="e97f1-109">Pour renvoyer le contenu situé dans un dossier d’un site SharePoint ou OneDrive Entreprise, le script de cette rubrique utilise la propriété gérée DocumentLink au lieu de la propriété Path.</span><span class="sxs-lookup"><span data-stu-id="e97f1-109">To return content located in a folder in a SharePoint or OneDrive for Business site, the script in this topic uses the DocumentLink managed property instead of the Path property.</span></span> <span data-ttu-id="e97f1-110">La propriété DocumentLink est plus robuste que la propriété Path, car elle retourne tout le contenu d’un dossier, alors que la propriété Path ne retourne pas certains fichiers multimédias.</span><span class="sxs-lookup"><span data-stu-id="e97f1-110">The DocumentLink property is more robust than the Path property because it will return all content in a folder, whereas the Path property won't return some media files.</span></span>

## <a name="before-you-run-a-targeted-collection"></a><span data-ttu-id="e97f1-111">Avant d’exécuter une collection ciblée</span><span class="sxs-lookup"><span data-stu-id="e97f1-111">Before you run a targeted collection</span></span>

- <span data-ttu-id="e97f1-112">Vous devez être membre du groupe de rôles Gestionnaire eDiscovery dans le Centre de sécurité & conformité pour exécuter le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="e97f1-112">You have to be a member of the eDiscovery Manager role group in Security & Compliance Center to run the script in Step 1.</span></span> <span data-ttu-id="e97f1-113">Pour plus d'informations, voir [Attribution d'autorisations eDiscovery](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="e97f1-113">For more information, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>

- <span data-ttu-id="e97f1-114">Vous devez également avoir le rôle Destinataires de courrier dans votre Exchange Online organisation.</span><span class="sxs-lookup"><span data-stu-id="e97f1-114">You also have to be assigned the Mail Recipients role in your Exchange Online organization.</span></span> <span data-ttu-id="e97f1-115">Cela est nécessaire pour exécuter la cmdlet **Get-MailboxFolderStatistics,** qui est incluse dans le script.</span><span class="sxs-lookup"><span data-stu-id="e97f1-115">This is required to run the **Get-MailboxFolderStatistics** cmdlet, which is included in the script.</span></span> <span data-ttu-id="e97f1-116">Par défaut, le rôle Destinataires de courrier est attribué aux groupes de rôles Gestion de l’organisation et Gestion des destinataires dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e97f1-116">By default, the Mail Recipients role is assigned to the Organization Management and Recipient Management role groups in Exchange Online.</span></span> <span data-ttu-id="e97f1-117">Pour plus d’informations sur l’attribution d’autorisations dans Exchange Online, voir [Gérer les membres du groupe de rôles.](/exchange/manage-role-group-members-exchange-2013-help)</span><span class="sxs-lookup"><span data-stu-id="e97f1-117">For more information about assigning permissions in Exchange Online, see [Manage role group members](/exchange/manage-role-group-members-exchange-2013-help).</span></span> <span data-ttu-id="e97f1-118">Vous pouvez également créer un groupe de rôles personnalisé, lui attribuer le rôle Destinataires de messagerie, puis ajouter les membres qui doivent exécuter le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="e97f1-118">You could also create a custom role group, assign the Mail Recipients role to it, and then add the members who need to run the script in Step 1.</span></span> <span data-ttu-id="e97f1-119">Pour plus d'informations, consultez la rubrique [Gérer des groupes de rôles](/Exchange/permissions-exo/role-groups).</span><span class="sxs-lookup"><span data-stu-id="e97f1-119">For more information, see [Manage role groups](/Exchange/permissions-exo/role-groups).</span></span>

- <span data-ttu-id="e97f1-120">Le script de cet article prend en charge l’authentification moderne.</span><span class="sxs-lookup"><span data-stu-id="e97f1-120">The script in this article supports modern authentication.</span></span> <span data-ttu-id="e97f1-121">Vous pouvez utiliser le script tel qu’il est si vous êtes un Microsoft 365 ou une Microsoft 365 Cloud de la communauté du secteur public organisation.</span><span class="sxs-lookup"><span data-stu-id="e97f1-121">You can use the script as-is if you are a Microsoft 365 or a Microsoft 365 GCC organization.</span></span> <span data-ttu-id="e97f1-122">Si vous êtes une organisation Office 365 Germany, une organisation Microsoft 365 Cloud de la communauté du secteur public High ou une organisation DoD Microsoft 365, vous devez modifier le script pour l’exécuter correctement.</span><span class="sxs-lookup"><span data-stu-id="e97f1-122">If you are an Office 365 Germany organization, a Microsoft 365 GCC High organization, or a Microsoft 365 DoD organization, you will have to edit the script to successfully run it.</span></span> <span data-ttu-id="e97f1-123">Plus précisément, vous devez modifier la ligne et utiliser le paramètre `Connect-ExchangeOnline` *ExchangeEnvironmentName* (et la valeur appropriée pour le type de votre organisation) pour vous connecter à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e97f1-123">Specifically, you have to edit the line `Connect-ExchangeOnline` and use the *ExchangeEnvironmentName* parameter (and the appropriate value for your organization type) to connect to Exchange Online PowerShell.</span></span>  <span data-ttu-id="e97f1-124">En outre, vous devez modifier la ligne et utiliser les `Connect-IPPSSession` paramètres *ConnectionUri* et *AzureADAuthorizationEndpointUri* (et les valeurs appropriées pour le type de votre organisation) pour vous connecter au Centre de sécurité & conformité PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e97f1-124">Also, you have to edit the line `Connect-IPPSSession` and use the *ConnectionUri* and *AzureADAuthorizationEndpointUri* parameters (and the appropriate values for your organization type) to connect to Security & Compliance Center PowerShell.</span></span> <span data-ttu-id="e97f1-125">Pour plus d’informations, voir les exemples dans Connecter pour Exchange Online [PowerShell](/powershell/exchange/connect-to-exchange-online-powershell#connect-to-exchange-online-powershell-without-using-mfa) et Connecter au Centre de sécurité & conformité [PowerShell](/powershell/exchange/connect-to-scc-powershell#connect-to-security--compliance-center-powershell-without-using-mfa).</span><span class="sxs-lookup"><span data-stu-id="e97f1-125">For more information, see the examples in [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell#connect-to-exchange-online-powershell-without-using-mfa) and [Connect to Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell#connect-to-security--compliance-center-powershell-without-using-mfa).</span></span>

- <span data-ttu-id="e97f1-126">Chaque fois que vous exécutez le script, une nouvelle session PowerShell distante est créée.</span><span class="sxs-lookup"><span data-stu-id="e97f1-126">Each time you run the script, a new remote PowerShell session is created.</span></span> <span data-ttu-id="e97f1-127">Cela signifie que vous pouvez utiliser toutes les sessions PowerShell distantes à votre disposition.</span><span class="sxs-lookup"><span data-stu-id="e97f1-127">That means you can use up all the remote PowerShell sessions available to you.</span></span> <span data-ttu-id="e97f1-128">Pour éviter que cela ne se produise, exécutez la commande suivante pour déconnecter vos sessions PowerShell distantes actives.</span><span class="sxs-lookup"><span data-stu-id="e97f1-128">To prevent this from happening, run the following command to disconnect your active remote PowerShell sessions.</span></span>

  ```powershell
  Get-PSSession | Remove-PSSession
  ```

    <span data-ttu-id="e97f1-129">Pour plus d'informations, reportez-vous à [Connexion à Exchange Online](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="e97f1-129">For more information, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="e97f1-130">Le script inclut une gestion minimale des erreurs.</span><span class="sxs-lookup"><span data-stu-id="e97f1-130">The script includes minimal error handling.</span></span> <span data-ttu-id="e97f1-131">L’objectif principal du script est d’afficher rapidement une liste d’ID de dossier de boîte aux lettres ou de chemins d’accès au site qui peuvent être utilisés dans la syntaxe de requête de recherche d’une recherche de contenu pour effectuer une collection ciblée.</span><span class="sxs-lookup"><span data-stu-id="e97f1-131">The primary purpose of the script is to quickly display a list of mailbox folder IDs or site paths that can be used in the search query syntax of a Content Search to perform a targeted collection.</span></span>

- <span data-ttu-id="e97f1-132">L’exemple de script fourni dans cette rubrique n’est pas pris en charge dans le cadre d’un programme ou d’un service de support standard Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e97f1-132">The sample script provided in this topic isn't supported under any Microsoft standard support program or service.</span></span> <span data-ttu-id="e97f1-133">L’exemple de script est fourni tel quel, sans garantie d’aucune sorte.</span><span class="sxs-lookup"><span data-stu-id="e97f1-133">The sample script is provided AS IS without warranty of any kind.</span></span> <span data-ttu-id="e97f1-134">Microsoft Corporation décline aussi toute garantie implicite, y compris et sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier.</span><span class="sxs-lookup"><span data-stu-id="e97f1-134">Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span></span> <span data-ttu-id="e97f1-135">La totalité des risques découlant de l’utilisation ou de la performance de l’exemple de script et de la documentation repose sur vous.</span><span class="sxs-lookup"><span data-stu-id="e97f1-135">The entire risk arising out of the use or performance of the sample script and documentation remains with you.</span></span> <span data-ttu-id="e97f1-136">En aucun cas Microsoft, ses auteurs ou quiconque impliqué dans la création, la production ou la livraison des scripts ne sera responsable de tous dommages quels qu’ils soient (y compris, sans limitation, les dommages pour perte de profits, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="e97f1-136">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>

## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a><span data-ttu-id="e97f1-137">Étape 1 : Exécuter le script pour obtenir la liste des dossiers d’une boîte aux lettres ou d’un site</span><span class="sxs-lookup"><span data-stu-id="e97f1-137">Step 1: Run the script to get a list of folders for a mailbox or site</span></span>

<span data-ttu-id="e97f1-138">Le script que vous exécutez lors de cette première étape retourne une liste de dossiers de boîtes aux lettres ou de dossiers SharePoint et OneDrive Entreprise, ainsi que l’ID ou le chemin d’accès correspondant pour chaque dossier.</span><span class="sxs-lookup"><span data-stu-id="e97f1-138">The script that you run in this first step will return a list of mailbox folders or SharePoint and OneDrive for Business folders, and the corresponding folder ID or path for each folder.</span></span> <span data-ttu-id="e97f1-139">Lorsque vous exécutez ce script, il vous invite à fournir les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="e97f1-139">When you run this script, it will prompt you for the following information.</span></span>

- <span data-ttu-id="e97f1-140">**Adresse de messagerie ou URL du site**: tapez l’adresse e-mail du dépositaire pour renvoyer la liste Exchange dossiers de boîte aux lettres et les ID de dossier.</span><span class="sxs-lookup"><span data-stu-id="e97f1-140">**Email address or site URL**: Type an email address of the custodian to return a list of Exchange mailbox folders and folder IDs.</span></span> <span data-ttu-id="e97f1-141">Ou tapez l’URL d’un site SharePoint ou d’un site OneDrive Entreprise pour renvoyer la liste des chemins d’accès pour le site spécifié.</span><span class="sxs-lookup"><span data-stu-id="e97f1-141">Or type the URL for a SharePoint site or a OneDrive for Business site to return a list of paths for the specified site.</span></span> <span data-ttu-id="e97f1-142">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="e97f1-142">Here are some examples:</span></span>

  - <span data-ttu-id="e97f1-143">**Exchange**: stacig@contoso.onmicrosoft <spam> <spam> .com</span><span class="sxs-lookup"><span data-stu-id="e97f1-143">**Exchange**: stacig@contoso.onmicrosoft<spam><spam>.com</span></span>

  - <span data-ttu-id="e97f1-144">**SharePoint**: https <span>://</span>contoso.sharepoint.com/sites/marketing</span><span class="sxs-lookup"><span data-stu-id="e97f1-144">**SharePoint**: https<span>://</span>contoso.sharepoint.com/sites/marketing</span></span>

  - <span data-ttu-id="e97f1-145">**OneDrive Entreprise**: https <span>://</span>contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span><span class="sxs-lookup"><span data-stu-id="e97f1-145">**OneDrive for Business**: https<span>://</span>contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span></span>

- <span data-ttu-id="e97f1-146">**Vos informations d’identification** utilisateur : le script utilisera vos informations d’identification pour vous connecter à Exchange Online PowerShell ou au Centre de sécurité & conformité PowerShell à l’aide de l’authentification moderne.</span><span class="sxs-lookup"><span data-stu-id="e97f1-146">**Your user credentials**: The script will use your credentials to connect to Exchange Online PowerShell or Security & Compliance Center PowerShell using modern authentication.</span></span> <span data-ttu-id="e97f1-147">Comme indiqué précédemment, vous devez avoir les autorisations appropriées pour exécuter correctement ce script.</span><span class="sxs-lookup"><span data-stu-id="e97f1-147">As previously explained, you have to be assigned the appropriate permissions to successfully run this script.</span></span>

<span data-ttu-id="e97f1-148">Pour afficher une liste de dossiers de boîtes aux lettres ou de noms de lien de document de site (chemin d’accès) :</span><span class="sxs-lookup"><span data-stu-id="e97f1-148">To display a list of mailbox folders or site documentlink (path) names:</span></span>

1. <span data-ttu-id="e97f1-149">Enregistrez le texte suivant dans un fichier Windows PowerShell script à l’aide d’un suffixe de nom de fichier .ps1 ; par exemple, `GetFolderSearchParameters.ps1` .</span><span class="sxs-lookup"><span data-stu-id="e97f1-149">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `GetFolderSearchParameters.ps1`.</span></span>

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
   if ($addressOrSite.IndexOf("@") -ige 0)
   {
      # List the folder Ids for the target mailbox
      $emailAddress = $addressOrSite
      # Connect to Exchange Online PowerShell
      if (!$ExoSession)
      {
          Import-Module ExchangeOnlineManagement
          Connect-ExchangeOnline
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
      # Connect to Security & Compliance Center PowerShell
      if (!$SccSession)
      {
          Import-Module ExchangeOnlineManagement
          Connect-IPPSSession
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

2. <span data-ttu-id="e97f1-150">Sur votre ordinateur local, ouvrez Windows PowerShell et allez dans le dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="e97f1-150">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>

3. <span data-ttu-id="e97f1-151">Exécutez le script . par exemple :</span><span class="sxs-lookup"><span data-stu-id="e97f1-151">Run the script; for example:</span></span>

   ```powershell
   .\GetFolderSearchParameters.ps1
   ```

4. <span data-ttu-id="e97f1-152">Entrez les informations que vous invite le script.</span><span class="sxs-lookup"><span data-stu-id="e97f1-152">Enter the information that the script prompts you for.</span></span>

    <span data-ttu-id="e97f1-153">Le script affiche la liste des dossiers de boîte aux lettres ou des dossiers de site pour l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="e97f1-153">The script displays a list of mailbox folders or site folders for the specified user.</span></span> <span data-ttu-id="e97f1-154">Laissez cette fenêtre ouverte pour pouvoir copier un ID de dossier ou un nom de lien de document et le coller dans une requête de recherche à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="e97f1-154">Leave this window open so that you can copy a folder ID or documentlink name and paste it in to a search query in Step 2.</span></span>

    > [!TIP]
    > <span data-ttu-id="e97f1-155">Au lieu d’afficher une liste de dossiers sur l’écran de l’ordinateur, vous pouvez ré-diriger la sortie du script vers un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="e97f1-155">Instead of displaying a list of folders on the computer screen, you can re-direct the output of the script to a text file.</span></span> <span data-ttu-id="e97f1-156">Ce fichier est enregistré dans le dossier où se trouve le script.</span><span class="sxs-lookup"><span data-stu-id="e97f1-156">This file will be saved to the folder where the script is located.</span></span> <span data-ttu-id="e97f1-157">Par exemple, pour rediriger la sortie du script vers un fichier texte, exécutez la commande suivante à l’étape 3 : vous pouvez ensuite copier un ID de dossier ou un lien de document à partir du fichier à utiliser dans une requête de  `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` recherche.</span><span class="sxs-lookup"><span data-stu-id="e97f1-157">For example, to redirect the script output to a text file, run the following command in Step 3:  `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` Then you can copy a folder ID or documentlink from the file to use in a search query.</span></span>

### <a name="script-output-for-mailbox-folders"></a><span data-ttu-id="e97f1-158">Sortie de script pour les dossiers de boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="e97f1-158">Script output for mailbox folders</span></span>

<span data-ttu-id="e97f1-159">Si vous obtenez des ID de dossier de boîte aux lettres, le script se connecte à Exchange Online PowerShell, exécute la cmdlet **Get-MailboxFolderStatisics,** puis affiche la liste des dossiers de la boîte aux lettres spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e97f1-159">If you're getting mailbox folder IDs, the script connects to Exchange Online PowerShell, runs the **Get-MailboxFolderStatisics** cmdlet, and then displays the list of the folders from the specified mailbox.</span></span> <span data-ttu-id="e97f1-160">Pour chaque dossier de la boîte aux lettres, le script affiche le nom du dossier dans la colonne **FolderPath** et l’ID de dossier dans la **colonne FolderQuery.**</span><span class="sxs-lookup"><span data-stu-id="e97f1-160">For every folder in the mailbox, the script displays the name of the folder in the **FolderPath** column and the folder ID in the **FolderQuery** column.</span></span> <span data-ttu-id="e97f1-161">En outre, le script ajoute le préfixe **folderId** (qui est le nom de la propriété de boîte aux lettres) à l’ID de dossier.</span><span class="sxs-lookup"><span data-stu-id="e97f1-161">Additionally, the script adds the prefix of **folderId** (which is the name of the mailbox property) to the folder ID.</span></span> <span data-ttu-id="e97f1-162">Étant donné que **la propriété folderid** est une propriété utilisable dans une recherche, vous l’utiliserez dans une requête de recherche à l’étape  `folderid:<folderid>` 2 pour rechercher ce dossier.</span><span class="sxs-lookup"><span data-stu-id="e97f1-162">Because the **folderid** property is a searchable property, you'll use  `folderid:<folderid>` in a search query in Step 2 to search that folder.</span></span> <span data-ttu-id="e97f1-163">Le script affiche un maximum de 100 dossiers de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e97f1-163">The script displays a maximum of 100 mailbox folders.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e97f1-164">Le script de cet article inclut une logique de codage qui convertit les valeurs d’ID de dossier de 64 caractères renvoyées par **Get-MailboxFolderStatistics** au même format de 48 caractères qui est indexé pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="e97f1-164">The script in this article includes encoding logic that converts the 64-character folder Id values that are returned by **Get-MailboxFolderStatistics** to the same 48-character format that is indexed for search.</span></span> <span data-ttu-id="e97f1-165">Si vous exécutez simplement la cmdlet **Get-MailboxFolderStatistics** dans PowerShell pour obtenir un ID de dossier (au lieu d’exécuter le script dans cet article), une requête de recherche qui utilise cette valeur d’ID de dossier échoue.</span><span class="sxs-lookup"><span data-stu-id="e97f1-165">If you just run the **Get-MailboxFolderStatistics** cmdlet in PowerShell to obtain a folder Id (instead of running the script in this article), a search query that uses that folder Id value will fail.</span></span> <span data-ttu-id="e97f1-166">Vous devez exécuter le script pour obtenir les ID de dossier correctement formatés qui peuvent être utilisés dans une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="e97f1-166">You have to run the script to get the correctly-formatted folder Ids that can be used in a Content Search.</span></span>

<span data-ttu-id="e97f1-167">Voici un exemple de sortie renvoyée par le script pour les dossiers de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e97f1-167">Here's an example of the output returned by the script for mailbox folders.</span></span>

![Exemple de liste des dossiers de boîte aux lettres et des ID de dossier renvoyés par le script](../media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)

<span data-ttu-id="e97f1-169">L’exemple de l’étape 2 montre la requête utilisée pour rechercher le sous-dossier Purges dans le dossier Éléments récupérables de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e97f1-169">The example in Step 2 shows the query used to search the Purges subfolder in the user's Recoverable Items folder.</span></span>

### <a name="script-output-for-site-folders"></a><span data-ttu-id="e97f1-170">Sortie de script pour les dossiers de site</span><span class="sxs-lookup"><span data-stu-id="e97f1-170">Script output for site folders</span></span>

<span data-ttu-id="e97f1-171">Si vous recherchez le chemin d’accès de la propriété **documentlink** à partir de sites SharePoint ou OneDrive Entreprise, le script se connecte à Security & Compliance PowerShell, crée une recherche de contenu qui recherche des dossiers dans le site, puis affiche la liste des dossiers situés dans le site spécifié.</span><span class="sxs-lookup"><span data-stu-id="e97f1-171">If you're getting the path of the **documentlink** property from SharePoint or OneDrive for Business sites, the script connects to Security & Compliance PowerShell, creates a new Content Search that searches the site for folders, and then displays a list of the folders located in the specified site.</span></span> <span data-ttu-id="e97f1-172">Le script affiche le nom de chaque dossier et ajoute le préfixe **de documentlink** à l’URL du dossier.</span><span class="sxs-lookup"><span data-stu-id="e97f1-172">The script displays the name of each folder and adds the prefix of **documentlink** to the folder URL.</span></span> <span data-ttu-id="e97f1-173">Étant donné que la propriété **documentlink** est une propriété utilisable dans une recherche, vous utiliserez la paire propriété:valeur dans une requête de recherche à l’étape 2 pour rechercher `documentlink:<path>` ce dossier.</span><span class="sxs-lookup"><span data-stu-id="e97f1-173">Because the **documentlink** property is a searchable property, you'll use `documentlink:<path>` property:value pair in a search query in Step 2 to search that folder.</span></span> <span data-ttu-id="e97f1-174">Le script affiche un maximum de 200 dossiers de site.</span><span class="sxs-lookup"><span data-stu-id="e97f1-174">The script displays a maximum of 200 site folders.</span></span> <span data-ttu-id="e97f1-175">S’il y a plus de 200 dossiers de site, les plus récents sont affichés.</span><span class="sxs-lookup"><span data-stu-id="e97f1-175">If there are more than 200 site folders, the newest ones are displayed.</span></span>

<span data-ttu-id="e97f1-176">Voici un exemple de sortie renvoyée par le script pour les dossiers de site.</span><span class="sxs-lookup"><span data-stu-id="e97f1-176">Here's an example of the output returned by the script for site folders.</span></span>

![Exemple de liste de noms de liens de documents pour les dossiers de site renvoyés par le script](../media/519e8347-7365-4067-af78-96c465dc3d15.png)

## <a name="step-2-use-a-folder-id-or-documentlink-to-perform-a-targeted-collection"></a><span data-ttu-id="e97f1-178">Étape 2 : Utiliser un ID de dossier ou un lien de document pour effectuer une collection ciblée</span><span class="sxs-lookup"><span data-stu-id="e97f1-178">Step 2: Use a folder ID or documentlink to perform a targeted collection</span></span>

<span data-ttu-id="e97f1-179">Après avoir exécuté le script pour collecter une liste d’ID de dossier ou de liens de documents pour un utilisateur spécifique, l’étape suivante vous permet d’aller au Centre de conformité Microsoft 365 et de créer une recherche de contenu pour rechercher un dossier spécifique.</span><span class="sxs-lookup"><span data-stu-id="e97f1-179">After you've run the script to collect a list of folder IDs or document links for a specific user, the next step to go to the Microsoft 365 compliance center and create a new Content Search to search a specific folder.</span></span> <span data-ttu-id="e97f1-180">Vous utiliserez la paire ou property:value dans la requête de recherche que vous configurez dans la zone de mot clé de recherche de contenu (ou comme valeur pour le paramètre ContentMatchQuery si vous utilisez la `folderid:<folderid>` `documentlink:<path>` cmdlet **New-ComplianceSearch).** </span><span class="sxs-lookup"><span data-stu-id="e97f1-180">You'll use the  `folderid:<folderid>` or  `documentlink:<path>` property:value pair in the search query that you configure in the Content Search keyword box (or as the value for the  *ContentMatchQuery*  parameter if you use the **New-ComplianceSearch** cmdlet).</span></span> <span data-ttu-id="e97f1-181">Vous pouvez combiner la ou la  `folderid`  `documentlink` propriété avec d’autres paramètres de recherche ou conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="e97f1-181">You can combine the  `folderid` or  `documentlink` property with other search parameters or search conditions.</span></span> <span data-ttu-id="e97f1-182">Si vous incluez uniquement la ou la propriété dans la requête, la recherche retourne tous les éléments situés  `folderid`  `documentlink` dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="e97f1-182">If you only include the  `folderid` or  `documentlink` property in the query, the search will return all items located in the specified folder.</span></span>

1. <span data-ttu-id="e97f1-183">Go to <https://compliance.microsoft.com> and sign in using the account and credentials that you used to run the script in Step 1.</span><span class="sxs-lookup"><span data-stu-id="e97f1-183">Go to <https://compliance.microsoft.com> and sign in using the account and credentials that you used to run the script in Step 1.</span></span>

2. <span data-ttu-id="e97f1-184">Dans le volet gauche du centre de conformité, cliquez sur Afficher la recherche de contenu, puis  >  sur **Nouvelle recherche.**</span><span class="sxs-lookup"><span data-stu-id="e97f1-184">In the left pane of the compliance center, click **Show all** > **Content search**, and then click **New search**.</span></span>

3. <span data-ttu-id="e97f1-185">Dans la **zone Mots clés,** collez la ou la valeur renvoyée par le script à `folderid:<folderid>`  `documentlink:<path>` l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="e97f1-185">In the **Keywords** box, paste the `folderid:<folderid>` or  `documentlink:<path>` value that was returned by the script in Step 1.</span></span>

    <span data-ttu-id="e97f1-186">Par exemple, la requête de la capture d’écran suivante recherchera n’importe quel élément du sous-dossier Purges du dossier Éléments récupérables de l’utilisateur (la valeur de la propriété du sous-dossier Purges est indiquée dans la capture d’écran de l’étape `folderid` 1) :</span><span class="sxs-lookup"><span data-stu-id="e97f1-186">For example, the query in the following screenshot will search for any item in the Purges subfolder in the user's Recoverable Items folder (the value of the `folderid` property for the Purges subfolder is shown in the screenshot in Step 1):</span></span>

    ![Coller le folderid ou le documentlink dans la zone de mot clé de la requête de recherche](../media/FolderIDSearchQuery.png)

4. <span data-ttu-id="e97f1-188">Sous **Emplacements,** **sélectionnez Des emplacements spécifiques,** puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="e97f1-188">Under **Locations**, select **Specific locations** and then click **Modify**.</span></span>

5. <span data-ttu-id="e97f1-189">Faites l’une des choses suivantes, selon que vous recherchez un dossier de boîte aux lettres ou un dossier de site :</span><span class="sxs-lookup"><span data-stu-id="e97f1-189">Do one of the following, based on whether you're searching a mailbox folder or a site folder:</span></span>

    - <span data-ttu-id="e97f1-190">En **Exchange,** cliquez sur Choisir des utilisateurs, des groupes ou des **équipes,** puis ajoutez la boîte aux lettres que vous avez spécifiée lorsque vous avez lancé le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="e97f1-190">Next to **Exchange email**, click **Choose users, groups, or teams** and then add the same mailbox that you specified when you ran the script in Step 1.</span></span>

      <span data-ttu-id="e97f1-191">Ou</span><span class="sxs-lookup"><span data-stu-id="e97f1-191">Or</span></span>

    - <span data-ttu-id="e97f1-192">En SharePoint **sites,** cliquez sur Choisir des **sites,** puis ajoutez la même URL de site que celle que vous avez spécifiée lorsque vous avez lancé le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="e97f1-192">Next to **SharePoint sites**, click **Choose sites** and then add the same site URL that you specified when you ran the script in Step 1.</span></span>

6. <span data-ttu-id="e97f1-193">Après avoir enregistrez l’emplacement de contenu à rechercher, cliquez sur Enregistrer **&** exécuter, tapez un nom pour la recherche de contenu, puis cliquez sur Enregistrer pour démarrer la recherche de collection ciblée. </span><span class="sxs-lookup"><span data-stu-id="e97f1-193">After you save the content location to search, click **Save & run**, type a name for the Content Search, and then click **Save** to start the targeted collection search.</span></span>

### <a name="examples-of-search-queries-for-targeted-collections"></a><span data-ttu-id="e97f1-194">Exemples de requêtes de recherche pour des collections ciblées</span><span class="sxs-lookup"><span data-stu-id="e97f1-194">Examples of search queries for targeted collections</span></span>

<span data-ttu-id="e97f1-195">Voici quelques exemples d’utilisation des propriétés dans une requête de recherche pour  `folderid`  `documentlink` effectuer une collection ciblée.</span><span class="sxs-lookup"><span data-stu-id="e97f1-195">Here are some examples of using the  `folderid` and  `documentlink` properties in a search query to perform a targeted collection.</span></span> <span data-ttu-id="e97f1-196">Les espaces réservé sont utilisés pour  `folderid:<folderid>` et pour économiser de  `documentlink:<path>` l’espace.</span><span class="sxs-lookup"><span data-stu-id="e97f1-196">Placeholders are used for  `folderid:<folderid>` and  `documentlink:<path>` to save space.</span></span>

- <span data-ttu-id="e97f1-197">Cet exemple recherche trois dossiers de boîtes aux lettres différents.</span><span class="sxs-lookup"><span data-stu-id="e97f1-197">This example searches three different mailbox folders.</span></span> <span data-ttu-id="e97f1-198">Vous pouvez utiliser une syntaxe de requête similaire pour rechercher les dossiers masqués dans le dossier Éléments récupérables d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e97f1-198">You could use similar query syntax to search the hidden folders in a user's Recoverable Items folder.</span></span>

  ```powershell
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- <span data-ttu-id="e97f1-199">Cet exemple recherche dans un dossier de boîte aux lettres les éléments qui contiennent une expression exacte.</span><span class="sxs-lookup"><span data-stu-id="e97f1-199">This example searches a mailbox folder for items that contain an exact phrase.</span></span>

  ```powershell
  folderid:<folderid> AND "Contoso financial results"
  ```

- <span data-ttu-id="e97f1-200">Cet exemple recherche dans un dossier de site (et tous les sous-dossiers) les documents qui contiennent les lettres « NDA » dans le titre.</span><span class="sxs-lookup"><span data-stu-id="e97f1-200">This example searches a site folder (and any subfolders) for documents that contain the letters "NDA" in the title.</span></span>

  ```powershell
  documentlink:<path> AND filename:nda
  ```

- <span data-ttu-id="e97f1-201">Cet exemple recherche dans un dossier de site (et tout sous-dossier) les documents qui ont été modifiés dans une plage de dates.</span><span class="sxs-lookup"><span data-stu-id="e97f1-201">This example searches a site folder (and any subfolder) for documents there were changed within a date range.</span></span>

  ```powershell
  documentlink:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```

## <a name="more-information"></a><span data-ttu-id="e97f1-202">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e97f1-202">More information</span></span>

<span data-ttu-id="e97f1-203">Gardez les points suivants à l’esprit lorsque vous utilisez le script de cet article pour effectuer des collections ciblées.</span><span class="sxs-lookup"><span data-stu-id="e97f1-203">Keep the following things in mind when using the script in this article to perform targeted collections.</span></span>

- <span data-ttu-id="e97f1-204">Le script ne supprime aucun dossier des résultats.</span><span class="sxs-lookup"><span data-stu-id="e97f1-204">The script doesn't remove any folders from the results.</span></span> <span data-ttu-id="e97f1-205">Par exemple, certains dossiers répertoriés dans les résultats peuvent ne pas être accessibles à la recherche (ou renvoyer zéro éléments) car ils contiennent du contenu généré par le système ou parce qu’ils contiennent uniquement des sous-dossiers et non des éléments de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e97f1-205">So some folders listed in the results might be unsearchable (or return zero items) because they contain system-generated content or because they only contain subfolders and not mailbox items.</span></span>

- <span data-ttu-id="e97f1-206">Ce script renvoie uniquement les informations de dossier pour la boîte aux lettres principale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e97f1-206">This script only returns folder information for the user's primary mailbox.</span></span> <span data-ttu-id="e97f1-207">Il ne retourne pas d’informations sur les dossiers de la boîte aux lettres d’archivage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e97f1-207">It doesn't return information about folders in the user's archive mailbox.</span></span> <span data-ttu-id="e97f1-208">Pour renvoyer des informations sur les dossiers de la boîte aux lettres d’archivage de l’utilisateur, vous pouvez modifier le script.</span><span class="sxs-lookup"><span data-stu-id="e97f1-208">To return information about folders in the user's archive mailbox, you can edit the script.</span></span> <span data-ttu-id="e97f1-209">Pour ce faire, modifiez la ligne, `$folderStatistics = Get-MailboxFolderStatistics $emailAddress` puis `$folderStatistics = Get-MailboxFolderStatistics $emailAddress -Archive` enregistrez et exécutez le script modifié.</span><span class="sxs-lookup"><span data-stu-id="e97f1-209">To do this, change the line `$folderStatistics = Get-MailboxFolderStatistics $emailAddress` to `$folderStatistics = Get-MailboxFolderStatistics $emailAddress -Archive` and then save and run the edited script.</span></span> <span data-ttu-id="e97f1-210">Cette modification retourne les ID de dossier pour les dossiers et les sous-dossiers de la boîte aux lettres d’archivage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e97f1-210">This change will return the folder IDs for folders and subfolders in the user's archive mailbox.</span></span> <span data-ttu-id="e97f1-211">Pour effectuer une recherche dans l’ensemble de la boîte aux lettres d’archivage, vous pouvez connecter toutes les paires propriété:valeur de l’ID de dossier avec un opérateur `OR` dans une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="e97f1-211">To search the entire archive mailbox, you can connect all folder ID property:value pairs with an `OR` operator in a search query.</span></span>

- <span data-ttu-id="e97f1-212">Lorsque vous recherchez des dossiers de boîte aux lettres, seul le dossier spécifié (identifié par sa propriété) est recherché ; les sous-dossiers ne sont `folderid` pas recherchés.</span><span class="sxs-lookup"><span data-stu-id="e97f1-212">When searching mailbox folders, only the specified folder (identified by its `folderid` property) will be searched; subfolders won't be searched.</span></span> <span data-ttu-id="e97f1-213">Pour rechercher des sous-dossiers, vous devez utiliser l’ID de dossier du sous-dossier que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="e97f1-213">To search subfolders, you need to use the  folder ID for the subfolder that you want to search.</span></span>

- <span data-ttu-id="e97f1-214">Lorsque vous recherchez des dossiers de site, le dossier (identifié par sa propriété) et tous les `documentlink` sous-dossiers sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="e97f1-214">When searching site folders, the folder (identified by its `documentlink` property) and all subfolders will be searched.</span></span>

- <span data-ttu-id="e97f1-215">Lors de l’exportation des résultats d’une recherche dans laquelle vous avez uniquement spécifié la propriété dans la requête de recherche, vous pouvez choisir la première option d’exportation , « Tous les éléments, à l’exception de ceux qui ont un format non reconnu, sont chiffrés ou n’ont pas été indexés pour `folderid` d’autres raisons. »</span><span class="sxs-lookup"><span data-stu-id="e97f1-215">When exporting the results of a search in which you only specified the `folderid` property in the search query, you can choose the first export option, "All items, excluding ones that have an unrecognized format, are encrypted, or weren't indexed for other reasons."</span></span> <span data-ttu-id="e97f1-216">Tous les éléments du dossier sont toujours exportés quel que soit leur état d’indexation, car l’ID de dossier est toujours indexé.</span><span class="sxs-lookup"><span data-stu-id="e97f1-216">All items in the folder will always be exported regardless of their indexing status because the folder ID is always indexed.</span></span>
