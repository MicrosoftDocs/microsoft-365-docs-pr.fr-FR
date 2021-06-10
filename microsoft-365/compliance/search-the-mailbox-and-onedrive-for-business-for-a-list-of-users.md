---
title: Rechercher dans le site de & OneDrive Entreprise boîte aux lettres une liste d’utilisateurs avec la recherche de contenu
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2017
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
ms.assetid: 5f4f8206-2d6a-4cb2-bbc6-7a0698703cc0
description: Utilisez la recherche de contenu et le script de cet article pour rechercher les boîtes aux lettres et OneDrive Entreprise sites pour un groupe d’utilisateurs.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 51e668438c6016a0c5f2c914dc2b2e86cc56f49e
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50922466"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a><span data-ttu-id="1584e-103">Utiliser la recherche de contenu pour rechercher une liste d’utilisateurs dans la boîte aux lettres et OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="1584e-103">Use Content Search to search the mailbox and OneDrive for Business site for a list of users</span></span>

<span data-ttu-id="1584e-104">Le Centre de sécurité & conformité fournit plusieurs cmdlets Windows PowerShell qui vous permettent d’automatiser des tâches eDiscovery chronophages.</span><span class="sxs-lookup"><span data-stu-id="1584e-104">The Security & Compliance Center provides a number of Windows PowerShell cmdlets that let you automate time-consuming eDiscovery-related tasks.</span></span> <span data-ttu-id="1584e-105">Actuellement, la création d’une recherche de contenu dans le Centre de sécurité & conformité pour rechercher un grand nombre d’emplacements de contenu de dépositaire prend du temps et de la préparation.</span><span class="sxs-lookup"><span data-stu-id="1584e-105">Currently, creating a Content Search in the Security & Compliance Center to search a large number of custodian content locations takes time and preparation.</span></span> <span data-ttu-id="1584e-106">Avant de créer une recherche, vous devez collecter l’URL de chaque site OneDrive Entreprise puis ajouter chaque boîte aux lettres OneDrive Entreprise site à la recherche.</span><span class="sxs-lookup"><span data-stu-id="1584e-106">Before you create a search, you have to collect the URL for each OneDrive for Business site and then add each mailbox and OneDrive for Business site to the search.</span></span> <span data-ttu-id="1584e-107">Dans les prochaines version, cela sera plus facile à faire dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="1584e-107">In future releases, this will be easier to do in the Security & Compliance Center.</span></span> <span data-ttu-id="1584e-108">En attendant, vous pouvez utiliser le script de cet article pour automatiser ce processus.</span><span class="sxs-lookup"><span data-stu-id="1584e-108">Until then, you can use the script in this article to automate this process.</span></span> <span data-ttu-id="1584e-109">Ce script vous invite à donner le nom du domaine Mon site de votre organisation (par exemple, **contoso** dans l’URL), une liste d’adresses e-mail utilisateur, le nom de la nouvelle recherche de contenu et la requête de recherche à `https://contoso-my.sharepoint.com` utiliser.</span><span class="sxs-lookup"><span data-stu-id="1584e-109">This script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL `https://contoso-my.sharepoint.com`), a list of user email addresses, the name of the new Content Search, and the search query to use.</span></span> <span data-ttu-id="1584e-110">Le script obtient l’URL OneDrive Entreprise pour chaque utilisateur de la liste, puis il crée et démarre une recherche de contenu qui recherche la boîte aux lettres et le site OneDrive Entreprise pour chaque utilisateur de la liste, à l’aide de la requête de recherche que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="1584e-110">The script gets the OneDrive for Business URL for each user in the list, and then it creates and starts a Content Search that searches the mailbox and OneDrive for Business site for each user in the list, using the search query that you provide.</span></span>
  
## <a name="permissions-and-script-information"></a><span data-ttu-id="1584e-111">Autorisations et informations de script</span><span class="sxs-lookup"><span data-stu-id="1584e-111">Permissions and script information</span></span>

- <span data-ttu-id="1584e-112">Vous devez être membre du groupe de rôles Gestionnaire eDiscovery dans le Centre de sécurité & conformité et administrateur général SharePoint Online pour exécuter le script à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="1584e-112">You have to be a member of the eDiscovery Manager role group in the Security & Compliance Center and a SharePoint Online global administrator to run the script in Step 3.</span></span>

- <span data-ttu-id="1584e-113">N’oubliez pas d’enregistrer la liste des utilisateurs que vous créez à l’étape 2 et le script de l’étape 3 dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="1584e-113">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder.</span></span> <span data-ttu-id="1584e-114">Cela facilitera l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="1584e-114">That will make it easier to run the script.</span></span>

- <span data-ttu-id="1584e-115">Le script inclut une gestion minimale des erreurs.</span><span class="sxs-lookup"><span data-stu-id="1584e-115">The script includes minimal error handling.</span></span> <span data-ttu-id="1584e-116">Son objectif principal est de rechercher rapidement et facilement la boîte aux lettres et OneDrive Entreprise site de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1584e-116">Its primary purpose is to quickly and easily search the mailbox and OneDrive for Business site of each user.</span></span>

- <span data-ttu-id="1584e-p104">Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="1584e-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>

## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="1584e-122">Étape 1 : installer SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="1584e-122">Step 1: Install the SharePoint Online Management Shell</span></span>

<span data-ttu-id="1584e-123">La première étape consiste à installer SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="1584e-123">The first step is to install the SharePoint Online Management Shell.</span></span> <span data-ttu-id="1584e-124">Vous n’avez pas besoin d’utiliser l’shell dans cette procédure, mais vous devez l’installer car il contient les conditions préalables requises par le script que vous exécutez à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="1584e-124">You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3.</span></span> <span data-ttu-id="1584e-125">Ces conditions préalables permettent au script de communiquer avec SharePoint Online pour obtenir les URL des sites OneDrive Entreprise web.</span><span class="sxs-lookup"><span data-stu-id="1584e-125">These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="1584e-126">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="1584e-126">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell.</span></span>
  
## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="1584e-127">Étape 2 : Générer une liste d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="1584e-127">Step 2: Generate a list of users</span></span>

<span data-ttu-id="1584e-128">Le script de l’étape 3 crée une recherche de contenu pour rechercher les boîtes aux lettres et OneDrive comptes pour une liste d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1584e-128">The script in Step 3 will create a Content Search to search the mailboxes and OneDrive accounts for a list of users.</span></span> <span data-ttu-id="1584e-129">Vous pouvez simplement taper les adresses de messagerie dans un fichier texte ou exécuter une commande dans Windows PowerShell pour obtenir une liste d’adresses e-mail et les enregistrer dans un fichier (situé dans le dossier où vous enregistrerez le script à l’étape 3).</span><span class="sxs-lookup"><span data-stu-id="1584e-129">You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="1584e-130">Voici une commande [PowerShell Exchange Online](/powershell/exchange/connect-to-exchange-online-powershell) que vous pouvez exécuter pour obtenir la liste des adresses de messagerie de tous les utilisateurs de votre organisation et l’enregistrer dans un fichier texte nommé `Users.txt` .</span><span class="sxs-lookup"><span data-stu-id="1584e-130">Here's an [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell) command that you can runt to get a list of email addresses for all users in your organization and save it to a text file named `Users.txt`.</span></span> 
  
```powershell
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

<span data-ttu-id="1584e-131">Après avoir exécuté cette commande, n’oubliez pas d’ouvrir le fichier et de supprimer l’en-tête qui contient le nom de la  `PrimarySmtpAddress` propriété.</span><span class="sxs-lookup"><span data-stu-id="1584e-131">After you run this command, be sure to open the file and remove the header that contains the property name,  `PrimarySmtpAddress`.</span></span> <span data-ttu-id="1584e-132">Le fichier texte doit simplement contenir une liste d’adresses de messagerie, et rien d’autre.</span><span class="sxs-lookup"><span data-stu-id="1584e-132">The text file should just contain a list of email addresses, and nothing else.</span></span> <span data-ttu-id="1584e-133">Assurez-vous qu’il n’existe aucune ligne vide avant ou après la liste des adresses e-mail.</span><span class="sxs-lookup"><span data-stu-id="1584e-133">Make sure there are no blank rows before or after the list of email addresses.</span></span>
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a><span data-ttu-id="1584e-134">Étape 3 : Exécuter le script pour créer et démarrer la recherche</span><span class="sxs-lookup"><span data-stu-id="1584e-134">Step 3: Run the script to create and start the search</span></span>

<span data-ttu-id="1584e-135">Lorsque vous exécutez le script dans cette étape, il vous invite à fournir les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="1584e-135">When you run the script in this step, it will prompt you for the following information.</span></span> <span data-ttu-id="1584e-136">Veillez à ce que ces informations soient prêtes avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="1584e-136">Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="1584e-137"> Vos informations d’identification utilisateur : le script utilise vos informations d’identification pour accéder à SharePoint Online afin d’obtenir les URL OneDrive Entreprise et de se connecter au Centre de sécurité & conformité avec PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="1584e-137">**Your user credentials** - The script will use your credentials to access SharePoint Online to get the OneDrive for Business URLs and to connect to the Security & Compliance Center with remote PowerShell.</span></span> 
    
- <span data-ttu-id="1584e-138">**Nom de votre domaine Mon site** : le domaine Mon site est le domaine qui contient tous les sites OneDrive Entreprise de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1584e-138">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization.</span></span> <span data-ttu-id="1584e-139">Par exemple, si l’URL de votre domaine Mon site est , vous devez entrer lorsque le script vous invite à entrer le nom de votre **https://contoso-my.sharepoint.com**  `contoso` domaine Mon site.</span><span class="sxs-lookup"><span data-stu-id="1584e-139">For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="1584e-140">**Nom du fichier texte de** l’étape 2 : nom du fichier texte que vous avez créé à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="1584e-140">**Pathname of the text file from Step 2** - The pathname of the text file that you created in Step 2.</span></span> <span data-ttu-id="1584e-141">Si le fichier texte et le script se trouvent dans le même dossier, entrez le nom du fichier texte.</span><span class="sxs-lookup"><span data-stu-id="1584e-141">If the text file and the script are located in the same folder, then enter the name of the text file.</span></span> <span data-ttu-id="1584e-142">Dans le cas contraire, entrez le chemin d’accès complet du fichier texte.</span><span class="sxs-lookup"><span data-stu-id="1584e-142">Otherwise, enter the complete pathname for the text file.</span></span> 
    
- <span data-ttu-id="1584e-143">**Nom de la recherche de** contenu : nom de la recherche de contenu qui sera créée par le script.</span><span class="sxs-lookup"><span data-stu-id="1584e-143">**Name of the Content Search** - The name of the Content Search that will be created by the script.</span></span> 
    
- <span data-ttu-id="1584e-144">**Requête de recherche** : la requête de recherche qui sera utilisée avec la recherche de contenu est créée et exécuté.</span><span class="sxs-lookup"><span data-stu-id="1584e-144">**Search query** - The search query that will be used with the Content Search is created and run.</span></span> <span data-ttu-id="1584e-145">Pour plus d’informations sur les requêtes de recherche, voir Requêtes par mot clé et [conditions de recherche pour la recherche de contenu.](keyword-queries-and-search-conditions.md)</span><span class="sxs-lookup"><span data-stu-id="1584e-145">For more information about search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>


<span data-ttu-id="1584e-146">**Pour exécuter le script :**</span><span class="sxs-lookup"><span data-stu-id="1584e-146">**To run the script:**</span></span>
    
1. <span data-ttu-id="1584e-147">Enregistrez le texte suivant dans un fichier Windows PowerShell script à l’aide d’un suffixe de nom de fichier .ps1 ; par exemple, `SearchEXOOD4B.ps1` .</span><span class="sxs-lookup"><span data-stu-id="1584e-147">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchEXOOD4B.ps1`.</span></span> <span data-ttu-id="1584e-148">Enregistrez le fichier dans le dossier où vous avez enregistré la liste des utilisateurs à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="1584e-148">Save the file to the same folder where you saved the list of users in Step 2.</span></span>
    
  ```powershell
  # This PowerShell script will prompt you for the following information:
  #    * Your user credentials 
  #    * The name of your organization's MySite domain                                              
  #    * The pathname for the text file that contains a list of user email addresses
  #    * The name of the Content Search that will be created
  #    * The search query string
  # The script will then:
  #    * Find the OneDrive for Business site for each user in the text file
  #    * Create and start a Content Search using the above information
  # Get user credentials
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  # Get the user's MySite domain name.  We use this to create the admin URL and root URL for OneDrive for Business
  $mySiteDomain = Read-Host "What is your organization's MySite domain?  For example,  'contoso' for 'https://contoso-my.sharepoint.com'"
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
  # Get other required information
  $inputfile = read-host "Enter the file name of the text file that contains the email addresses for the users you want to search"
  $searchName = Read-Host "Enter the name for the new search"
  $searchQuery = Read-Host "Enter the search query you want to use"
  $emailAddresses = Get-Content $inputfile | where {$_ -ne ""}  | foreach{ $_.Trim() }
  # Connect to Office 365
  if (!$s -or !$a)
  {
      $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
      $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Could not create PowerShell session."
          return;
      }
  }
  # Load the SharePoint assemblies from the SharePoint Online Management Shell
  # To install, go to https://go.microsoft.com/fwlink/p/?LinkId=255251
  if (!$SharePointClient -or !$SPRuntime -or !$SPUserProfile)
  {
      $SharePointClient = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client")
      $SPRuntime = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.Runtime")
      $SPUserProfile = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.UserProfiles")
      if (!$SharePointClient)
      {
          Write-Error "SharePoint Online Management Shell isn't installed, please install from: https://go.microsoft.com/fwlink/p/?LinkId=255251 and then run this script again"
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
  # Add the path of the User Profile Service to the SPO admin URL, then create a new webservice proxy to access it
  $proxyaddr = "$AdminUrl/_vti_bin/UserProfileService.asmx?wsdl"
  $UserProfileService= New-WebServiceProxy -Uri $proxyaddr -UseDefaultCredential False
  $UserProfileService.Credentials = $credentials
  # Take care of auth cookies
  $strAuthCookie = $spCreds.GetAuthenticationCookie($AdminUrl)
  $uri = New-Object System.Uri($AdminUrl)
  $container = New-Object System.Net.CookieContainer
  $container.SetCookies($uri, $strAuthCookie)
  $UserProfileService.CookieContainer = $container
  Write-Host "Getting each user's OneDrive for Business URL"
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
      try
      {
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" } 
          $url = $prop.values[0].value
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "-$emailAddress => $furl"
      }
      catch
      {
          Write-Warning "Could not locate OneDrive for $emailAddress"
      }
  }
  Write-Host "Creating and starting the search"
  $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $emailAddresses -SharePointLocation $urls -ContentMatchQuery $searchQuery
  # Finally, start the search and then display the status
  if($search)
  {
      Start-ComplianceSearch $search.Name
      Get-ComplianceSearch $search.Name
  }
  
  ```

2. <span data-ttu-id="1584e-149">Ouvrez Windows PowerShell et allez dans le dossier où vous avez enregistré le script et la liste des utilisateurs de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="1584e-149">Open Windows PowerShell and go to the folder where you saved the script and the list of users from Step 2.</span></span>
    
3. <span data-ttu-id="1584e-150">Démarrez le script . par exemple :</span><span class="sxs-lookup"><span data-stu-id="1584e-150">Start the script; for example:</span></span>
    
    ```powershell
    .\SearchEXOOD4B.ps1
    ```

4. <span data-ttu-id="1584e-151">Lorsque vous y invitez vos informations d’identification, entrez votre adresse e-mail et votre mot de passe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1584e-151">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="1584e-152">Entrez les informations suivantes lorsque le script vous y invite.</span><span class="sxs-lookup"><span data-stu-id="1584e-152">Enter following information when prompted by the script.</span></span> <span data-ttu-id="1584e-153">Tapez chaque information, puis appuyez sur **Entrée.**</span><span class="sxs-lookup"><span data-stu-id="1584e-153">Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="1584e-154">Nom de votre domaine Mon site.</span><span class="sxs-lookup"><span data-stu-id="1584e-154">The name of your MySite domain.</span></span> 
    
    - <span data-ttu-id="1584e-155">Nom du chemin d’accès du fichier texte qui contient la liste des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1584e-155">The pathname of the text file that contains the list of users.</span></span>
    
    - <span data-ttu-id="1584e-156">Nom de la recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="1584e-156">A name for the Content Search.</span></span>
    
    - <span data-ttu-id="1584e-157">Requête de recherche (laissez ce vide pour renvoyer tous les éléments dans les emplacements de contenu).</span><span class="sxs-lookup"><span data-stu-id="1584e-157">The search query (leave this blank to return all items in the content locations).</span></span>
    
    <span data-ttu-id="1584e-158">Le script obtient les URL de chaque OneDrive Entreprise site, puis crée et démarre la recherche.</span><span class="sxs-lookup"><span data-stu-id="1584e-158">The script gets the URLs for each OneDrive for Business site and then creates and starts the search.</span></span> <span data-ttu-id="1584e-159">Vous pouvez exécuter la cmdlet **Get-ComplianceSearch** dans le Centre de sécurité & conformité PowerShell pour afficher les statistiques et les résultats de la recherche, ou vous pouvez aller à la **page** de recherche de contenu dans le Centre de sécurité & conformité pour afficher des informations sur la recherche.</span><span class="sxs-lookup"><span data-stu-id="1584e-159">You can either run the **Get-ComplianceSearch** cmdlet in Security & Compliance Center PowerShell to display the search statistics and results, or you can go to the **Content search** page in the Security & Compliance Center to view information about the search.</span></span>