---
title: Utiliser la recherche de contenu pour rechercher une liste d’utilisateurs dans la boîte aux lettres et OneDrive Entreprise
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
- SPO_Content
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 5f4f8206-2d6a-4cb2-bbc6-7a0698703cc0
description: Utilisez la recherche de contenu et le script dans cet article pour effectuer des recherches dans les boîtes aux lettres et les sites OneDrive entreprise pour un groupe d’utilisateurs.
ms.openlocfilehash: fa17b9eab2613407ae6c537ffc2619e5857f9182
ms.sourcegitcommit: 93e6bf1b541e22129f8c443051375d0ef1374150
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2020
ms.locfileid: "42634672"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a><span data-ttu-id="1f0a0-103">Utiliser la recherche de contenu pour rechercher une liste d’utilisateurs dans la boîte aux lettres et OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="1f0a0-103">Use Content Search to search the mailbox and OneDrive for Business site for a list of users</span></span>

<span data-ttu-id="1f0a0-104">Le centre de sécurité & conformité fournit un certain nombre d’applets de commande Windows PowerShell qui vous permettent d’automatiser des tâches de découverte électronique gourmandes en temps.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-104">The Security & Compliance Center provides a number of Windows PowerShell cmdlets that let you automate time-consuming eDiscovery-related tasks.</span></span> <span data-ttu-id="1f0a0-105">Actuellement, la création d’une recherche de contenu dans le centre de sécurité & conformité afin de rechercher un grand nombre d’emplacements de contenu dépositaire nécessite du temps et une préparation.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-105">Currently, creating a Content Search in the Security & Compliance Center to search a large number of custodian content locations takes time and preparation.</span></span> <span data-ttu-id="1f0a0-106">Avant de créer une recherche, vous devez collecter l’URL de chaque site OneDrive entreprise, puis ajouter chaque boîte aux lettres et le site OneDrive entreprise à la recherche.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-106">Before you create a search, you have to collect the URL for each OneDrive for Business site and then add each mailbox and OneDrive for Business site to the search.</span></span> <span data-ttu-id="1f0a0-107">Dans les prochaines versions, cette opération sera plus facile à effectuer dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-107">In future releases, this will be easier to do in the Security & Compliance Center.</span></span> <span data-ttu-id="1f0a0-108">En attendant, vous pouvez utiliser le script de cet article pour automatiser ce processus.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-108">Until then, you can use the script in this article to automate this process.</span></span> <span data-ttu-id="1f0a0-109">Ce script vous invite à indiquer le nom du domaine mon site de votre organisation (par exemple, **contoso** dans l' https://contoso-my.sharepoint.com)URL, une liste des adresses de messagerie des utilisateurs, le nom de la nouvelle recherche de contenu et la requête de recherche à utiliser.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-109">This script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL https://contoso-my.sharepoint.com), a list of user email addresses, the name of the new Content Search, and the search query to use.</span></span> <span data-ttu-id="1f0a0-110">Le script obtient l’URL de OneDrive entreprise pour chaque utilisateur dans la liste, puis il crée et démarre une recherche de contenu qui recherche dans la boîte aux lettres et le site OneDrive entreprise pour chaque utilisateur de la liste, à l’aide de la requête de recherche que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-110">The script gets the OneDrive for Business URL for each user in the list, and then it creates and starts a Content Search that searches the mailbox and OneDrive for Business site for each user in the list, using the search query that you provide.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="1f0a0-111">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1f0a0-111">Before you begin</span></span>

- <span data-ttu-id="1f0a0-112">Vous devez être membre du groupe de rôles gestionnaire de découverte électronique dans le centre de sécurité & conformité et d’un administrateur global SharePoint Online pour exécuter le script à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-112">You have to be a member of the eDiscovery Manager role group in the Security & Compliance Center and a SharePoint Online global administrator to run the script in Step 3.</span></span>
    
- <span data-ttu-id="1f0a0-113">Veillez à enregistrer la liste des utilisateurs que vous créez à l’étape 2 et le script de l’étape 3 dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-113">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder.</span></span> <span data-ttu-id="1f0a0-114">Cela facilitera l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-114">That will make it easier to run the script.</span></span>
    
- <span data-ttu-id="1f0a0-115">Le script inclut une gestion des erreurs minimale.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-115">The script includes minimal error handling.</span></span> <span data-ttu-id="1f0a0-116">Son objectif principal est de rechercher rapidement et facilement la boîte aux lettres et le site OneDrive entreprise de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-116">It's primary purpose is to quickly and easily search the mailbox and OneDrive for Business site of each user.</span></span>
    
- <span data-ttu-id="1f0a0-117">Les exemples de scripts fournis dans cette rubrique ne sont pas pris en charge dans n’importe quel programme ou service de support standard Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-117">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service.</span></span> <span data-ttu-id="1f0a0-118">Les exemples de scripts sont fournis en l'état, sans garantie d'aucune sorte.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-118">The sample scripts are provided AS IS without warranty of any kind.</span></span> <span data-ttu-id="1f0a0-119">Microsoft exclut encore toutes les garanties[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied, y compris, sans limitation, toute garantie implicite de qualité marchande ou d’adéquation à un usage particulier.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-119">Microsoft further disclaims all i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span></span> <span data-ttu-id="1f0a0-120">Vous assumez tous les risques liés à l'utilisation ou à l'exécution des exemples de scripts et de la documentation.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-120">The entire risk arising out of the use or performance of the sample scripts and documentation remains with you.</span></span> <span data-ttu-id="1f0a0-121">En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d'activité, perte d'informations commerciales ou toute autre perte pécuniaire) découlant de l'utilisation ou de l'impossibilité d'utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-121">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="1f0a0-122">Étape 1 : installer SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="1f0a0-122">Step 1: Install the SharePoint Online Management Shell</span></span>

<span data-ttu-id="1f0a0-123">La première étape consiste à installer SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-123">The first step is to install the SharePoint Online Management Shell.</span></span> <span data-ttu-id="1f0a0-124">Vous n’avez pas besoin d’utiliser l’environnement de commande Exchange Management Shell dans cette procédure, mais vous devez l’installer car il contient les conditions préalables requises par le script exécuté à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-124">You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3.</span></span> <span data-ttu-id="1f0a0-125">Ces conditions préalables permettent au script de communiquer avec SharePoint Online pour obtenir les URL des sites OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-125">These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="1f0a0-126">Accédez à [la configuration de l’environnement Windows PowerShell de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkID=286318) et effectuez les étapes 1 et 2 pour installer SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-126">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell.</span></span>
  
## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="1f0a0-127">Étape 2 : générer une liste d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="1f0a0-127">Step 2: Generate a list of users</span></span>

<span data-ttu-id="1f0a0-128">Le script de l’étape 3 crée une recherche de contenu pour rechercher dans les boîtes aux lettres et les comptes OneDrive une liste d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-128">The script in Step 3 will create a Content Search to search the mailboxes and OneDrive accounts for a list of users.</span></span> <span data-ttu-id="1f0a0-129">Vous pouvez simplement taper les adresses de messagerie dans un fichier texte ou exécuter une commande dans Windows PowerShell pour obtenir la liste des adresses de messagerie et les enregistrer dans un fichier (situé dans le même dossier dans lequel vous enregistrerez le script à l’étape 3).</span><span class="sxs-lookup"><span data-stu-id="1f0a0-129">You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="1f0a0-130">Voici une commande [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) que vous pouvez Runt pour obtenir une liste d’adresses de messagerie pour tous les utilisateurs de votre organisation et l’enregistrer dans un fichier texte `Users.txt`nommé.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-130">Here's an [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) command that you can runt to get a list of email addresses for all users in your organization and save it to a text file named `Users.txt`.</span></span> 
  
```powershell
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

<span data-ttu-id="1f0a0-131">Après avoir exécuté cette commande, veillez à ouvrir le fichier et à supprimer l’en-tête qui contient le `PrimarySmtpAddress`nom de la propriété,.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-131">After you run this command, be sure to open the file and remove the header that contains the property name,  `PrimarySmtpAddress`.</span></span> <span data-ttu-id="1f0a0-132">Le fichier texte doit contenir uniquement une liste d’adresses de messagerie et rien d’autre.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-132">The text file should just contain a list of email addresses, and nothing else.</span></span> <span data-ttu-id="1f0a0-133">Assurez-vous qu’il n’y a pas de ligne vide avant ou après la liste des adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-133">Make sure there are no blank rows before or after the list of email addresses.</span></span>
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a><span data-ttu-id="1f0a0-134">Étape 3 : exécuter le script pour créer et démarrer la recherche</span><span class="sxs-lookup"><span data-stu-id="1f0a0-134">Step 3: Run the script to create and start the search</span></span>

<span data-ttu-id="1f0a0-135">Lorsque vous exécutez le script dans cette étape, il vous invite à fournir les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-135">When you run the script in this step, it will prompt you for the following information.</span></span> <span data-ttu-id="1f0a0-136">Assurez-vous que vous disposez de ces informations avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-136">Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="1f0a0-137">**Vos informations d’identification utilisateur** : le script utilisera vos informations d’identification pour accéder à SharePoint Online afin d’obtenir les URL de OneDrive entreprise et se connecter au centre de sécurité & de conformité avec PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-137">**Your user credentials** - The script will use your credentials to access SharePoint Online to get the OneDrive for Business URLs and to connect to the Security & Compliance Center with remote PowerShell.</span></span> 
    
- <span data-ttu-id="1f0a0-138">**Nom de votre domaine mon** site : le domaine mon site est celui qui contient tous les sites OneDrive entreprise de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-138">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization.</span></span> <span data-ttu-id="1f0a0-139">Par exemple, si l’URL de votre domaine mon site **https://contoso-my.sharepoint.com**mon site est, entrez `contoso` alors lorsque le script vous invite à indiquer le nom de votre domaine mon site.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-139">For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="1f0a0-140">**Chemin d’accès du fichier texte à partir de l’étape 2** : le nom de chemin du fichier texte que vous avez créé à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-140">**Pathname of the text file from Step 2** - The pathname of the text file that you created in Step 2.</span></span> <span data-ttu-id="1f0a0-141">Si le fichier texte et le script se trouvent dans le même dossier, entrez le nom du fichier texte.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-141">If the text file and the script are located in the same folder, then enter the name of the text file.</span></span> <span data-ttu-id="1f0a0-142">Dans le cas contraire, entrez le chemin d’accès complet au fichier texte.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-142">Otherwise, enter the complete pathname for the text file.</span></span> 
    
- <span data-ttu-id="1f0a0-143">**Nom de la recherche de contenu** : nom de la recherche de contenu qui sera créée par le script.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-143">**Name of the Content Search** - The name of the Content Search that will be created by the script.</span></span> 
    
- <span data-ttu-id="1f0a0-144">**Requête de recherche** : la requête de recherche qui sera utilisée avec la recherche de contenu est créée et exécutée.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-144">**Search query** - The search query that will be used with the Content Search is created and run.</span></span> <span data-ttu-id="1f0a0-145">Pour plus d’informations sur les requêtes de recherche, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="1f0a0-145">For more information about search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>


<span data-ttu-id="1f0a0-146">**Pour exécuter le script :**</span><span class="sxs-lookup"><span data-stu-id="1f0a0-146">**To run the script:**</span></span>
    
1. <span data-ttu-id="1f0a0-147">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, `SearchEXOOD4B.ps1`.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-147">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchEXOOD4B.ps1`.</span></span> <span data-ttu-id="1f0a0-148">Enregistrez le fichier dans le dossier où vous avez enregistré la liste des utilisateurs à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-148">Save the file to the same folder where you saved the list of users in Step 2.</span></span>
    
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

2. <span data-ttu-id="1f0a0-149">Ouvrez Windows PowerShell et accédez au dossier dans lequel vous avez enregistré le script et la liste des utilisateurs de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-149">Open Windows PowerShell and go to the folder where you saved the script and the list of users from Step 2.</span></span>
    
3. <span data-ttu-id="1f0a0-150">Démarrez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="1f0a0-150">Start the script; for example:</span></span>
    
    ```powershell
    .\SearchEXOOD4B.ps1
    ```

4. <span data-ttu-id="1f0a0-151">Lorsque vous êtes invité à entrer vos informations d’identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-151">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="1f0a0-152">Entrez les informations suivantes lorsque le script vous y invite.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-152">Enter following information when prompted by the script.</span></span> <span data-ttu-id="1f0a0-153">Tapez chaque information, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-153">Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="1f0a0-154">Nom de votre domaine mon site.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-154">The name of your MySite domain.</span></span> 
    
    - <span data-ttu-id="1f0a0-155">Chemin d’accès du fichier texte qui contient la liste des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-155">The pathname of the text file that contains the list of users.</span></span>
    
    - <span data-ttu-id="1f0a0-156">Nom de la recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-156">A name for the Content Search.</span></span>
    
    - <span data-ttu-id="1f0a0-157">La requête de recherche (laissez ce champ vide pour renvoyer tous les éléments dans les emplacements de contenu).</span><span class="sxs-lookup"><span data-stu-id="1f0a0-157">The search query (leave this blank to return all items in the content locations).</span></span>
    
    <span data-ttu-id="1f0a0-158">Le script obtient les URL de chaque site OneDrive entreprise, puis crée et démarre la recherche.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-158">The script gets the URLs for each OneDrive for Business site and then creates and starts the search.</span></span> <span data-ttu-id="1f0a0-159">Vous pouvez exécuter la cmdlet **Get-ComplianceSearch** dans Security & Compliance Center PowerShell pour afficher les statistiques et les résultats de la recherche, ou vous pouvez accéder à la page de **recherche de contenu** dans le centre de conformité & Compliance pour afficher les informations relatives à la recherche.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-159">You can either run the **Get-ComplianceSearch** cmdlet in Security & Compliance Center PowerShell to display the search statistics and results, or you can go to the **Content search** page in the Security & Compliance Center to view information about the search.</span></span> 
