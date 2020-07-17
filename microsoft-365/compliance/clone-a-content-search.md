---
title: Cloner une recherche de contenu
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
ms.custom:
- seo-marvel-apr2020
description: Utilisez le script Windows PowerShell dans cet article pour cloner rapidement une recherche de contenu existante dans le centre de conformité dans Office 365 ou Microsoft 365.
ms.openlocfilehash: 28f1264736f158fd686174813b9cefdd087c274c
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44818083"
---
# <a name="clone-a-content-search"></a><span data-ttu-id="923a9-103">Cloner une recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="923a9-103">Clone a Content Search</span></span>

<span data-ttu-id="923a9-104">La création d’une recherche de contenu dans le centre de conformité dans Office 365 ou Microsoft 365 recherche plusieurs boîtes aux lettres ou sites SharePoint et OneDrive entreprise peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="923a9-104">Creating a Content Search in the compliance center in Office 365 or Microsoft 365 that searches many mailboxes or SharePoint and OneDrive for Business sites can take a while.</span></span> <span data-ttu-id="923a9-105">La spécification des sites à rechercher peut également être sujette à des erreurs si vous entrez une URL erronée.</span><span class="sxs-lookup"><span data-stu-id="923a9-105">Specifying the sites to search can also be prone to errors if you mistype a URL.</span></span> <span data-ttu-id="923a9-106">Pour éviter ces problèmes, vous pouvez utiliser le script Windows PowerShell dans cet article pour cloner rapidement une recherche de contenu existante.</span><span class="sxs-lookup"><span data-stu-id="923a9-106">To avoid these issues, you can use the Windows PowerShell script in this article to quickly clone an existing Content Search.</span></span> <span data-ttu-id="923a9-107">Lorsque vous clonez une recherche, une nouvelle recherche (avec un nom différent) est créée, qui contient les mêmes propriétés (telles que les emplacements de contenu et la requête de recherche) en tant que recherche d’origine.</span><span class="sxs-lookup"><span data-stu-id="923a9-107">When you clone a search, a new search (with a different name) is created that contains the same properties (such as the content locations and the search query) as the original search.</span></span> <span data-ttu-id="923a9-108">Ensuite, vous pouvez modifier la nouvelle recherche en changeant la requête par mot clé ou la plage de dates, puis l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="923a9-108">Then you can edit the new search by changing the keyword query or the date range, and run it.</span></span>
  
<span data-ttu-id="923a9-109">Pourquoi le clonage du contenu effectue des recherches ?</span><span class="sxs-lookup"><span data-stu-id="923a9-109">Why clone Content Searches?</span></span>
  
- <span data-ttu-id="923a9-110">Pour comparer les résultats de différentes requêtes de recherche par mot clé exécutées sur les mêmes emplacements de contenu.</span><span class="sxs-lookup"><span data-stu-id="923a9-110">To compare the results of different keyword search queries run on the same content locations.</span></span>
    
- <span data-ttu-id="923a9-111">Pour éviter de devoir entrer un grand nombre d’emplacements de contenu lors de la création d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="923a9-111">To save you from having to reenter a large number of content locations when you create a new search.</span></span>
    
- <span data-ttu-id="923a9-112">Pour réduire la taille des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="923a9-112">To decrease the size of the search results.</span></span> <span data-ttu-id="923a9-113">Par exemple, si vous avez une recherche qui renvoie un trop grand nombre de résultats à exporter, vous pouvez cloner la recherche, puis ajouter une condition de recherche basée sur une plage de dates pour réduire le nombre de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="923a9-113">For example, if you have a search that returns too many results to export, you can clone the search and then add a search condition based on a date range to reduce the number of search results.</span></span>
  
## <a name="script-information"></a><span data-ttu-id="923a9-114">Informations sur le script</span><span class="sxs-lookup"><span data-stu-id="923a9-114">Script information</span></span>

- <span data-ttu-id="923a9-115">Pour exécuter le script décrit dans cette rubrique, vous devez être membre du groupe de rôles gestionnaire eDiscovery dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="923a9-115">You have to be a member of the eDiscovery Manager role group in the Security & Compliance Center to run the script described in this topic.</span></span>
    
- <span data-ttu-id="923a9-116">Le script inclut une gestion des erreurs minimale.</span><span class="sxs-lookup"><span data-stu-id="923a9-116">The script includes minimal error handling.</span></span> <span data-ttu-id="923a9-117">Le principal objectif du script est de cloner rapidement une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="923a9-117">The primary purpose of the script is to quickly clone a content search.</span></span>
    
- <span data-ttu-id="923a9-118">Le script crée une recherche de contenu, mais ne le démarre pas.</span><span class="sxs-lookup"><span data-stu-id="923a9-118">The script creates a new Content Search, but doesn't start it.</span></span>
    
- <span data-ttu-id="923a9-119">Ce script prend en compte si la recherche de contenu que vous clonez est associée à un cas de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="923a9-119">This script takes into account whether the Content Search that you're cloning is associated with an eDiscovery case.</span></span> <span data-ttu-id="923a9-120">Si la recherche est associée à un cas, la nouvelle recherche est également associée à la même casse.</span><span class="sxs-lookup"><span data-stu-id="923a9-120">If the search is associated with a case, the new search will also be associated with the same case.</span></span> <span data-ttu-id="923a9-121">Si la recherche existante n’est pas associée à un cas, la nouvelle recherche est indiquée sur la page **recherche de contenu** dans le centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="923a9-121">If the existing search isn't associated with a case, the new search will be listed on the **Content search** page in the compliance center.</span></span> 
    
- <span data-ttu-id="923a9-122">L’exemple de script fourni dans cette rubrique n’est pas pris en charge dans le cadre d’un service ou d’un programme de support standard Microsoft.</span><span class="sxs-lookup"><span data-stu-id="923a9-122">The sample script provided in this topic isn't supported under any Microsoft standard support program or service.</span></span> <span data-ttu-id="923a9-123">L’exemple de script est fourni en l’État sans aucune garantie.</span><span class="sxs-lookup"><span data-stu-id="923a9-123">The sample script is provided AS IS without warranty of any kind.</span></span> <span data-ttu-id="923a9-124">Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d'adéquation à un usage particulier.</span><span class="sxs-lookup"><span data-stu-id="923a9-124">Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span></span> <span data-ttu-id="923a9-125">L’ensemble des risques liés à l’utilisation ou aux performances de l’exemple de script et de la documentation reste avec vous.</span><span class="sxs-lookup"><span data-stu-id="923a9-125">The entire risk arising out of the use or performance of the sample script and documentation remains with you.</span></span> <span data-ttu-id="923a9-126">En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d'activité, perte d'informations commerciales ou toute autre perte pécuniaire) découlant de l'utilisation ou de l'impossibilité d'utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="923a9-126">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-clone-a-search"></a><span data-ttu-id="923a9-127">Étape 1 : exécuter le script pour cloner une recherche</span><span class="sxs-lookup"><span data-stu-id="923a9-127">Step 1: Run the script to clone a search</span></span>

<span data-ttu-id="923a9-128">Le script de cette étape crée une recherche de contenu en clonant une recherche existante.</span><span class="sxs-lookup"><span data-stu-id="923a9-128">The script in this step will create a new Content Search by cloning an existing one.</span></span> <span data-ttu-id="923a9-129">Lorsque vous exécutez ce script, vous êtes invité à fournir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="923a9-129">When you run this script, you'll be prompted for the following information:</span></span>
  
- <span data-ttu-id="923a9-130">**Vos informations d’identification utilisateur** : le script utilisera vos informations d’identification pour vous connecter au centre de sécurité & conformité de votre organisation avec Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="923a9-130">**Your user credentials** - The script will use your credentials to connect to the Security & Compliance Center for your organization with Windows PowerShell.</span></span> <span data-ttu-id="923a9-131">Comme indiqué précédemment, vous devez être membre du groupe de rôles gestionnaire de découverte électronique dans le centre de sécurité & compCompliance pour exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="923a9-131">As previously stated, you have to be a member of the eDiscovery Manager role group in the Security & compCompliance Center to run the script.</span></span> 
    
- <span data-ttu-id="923a9-132">**Nom de la recherche existante** : il s’agit de la recherche de contenu que vous souhaitez Cloner.</span><span class="sxs-lookup"><span data-stu-id="923a9-132">**The name of the existing search** - This is the Content Search that you want to clone.</span></span> 
    
- <span data-ttu-id="923a9-133">**Nom de la nouvelle recherche qui sera créée** : Si vous laissez cette valeur vide, le script crée un nom pour la nouvelle recherche basée sur le nom de la recherche que vous clonez.</span><span class="sxs-lookup"><span data-stu-id="923a9-133">**The name of the new search that will be created** - If you leave this value blank, the script will create a name for the new search that is based on the name of the search that you're cloning.</span></span> 
    
<span data-ttu-id="923a9-134">Pour cloner une recherche :</span><span class="sxs-lookup"><span data-stu-id="923a9-134">To clone a search:</span></span>
  
1. <span data-ttu-id="923a9-135">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, `CloneSearch.ps1` .</span><span class="sxs-lookup"><span data-stu-id="923a9-135">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CloneSearch.ps1`.</span></span>
    
  ```powershell
  # This PowerShell script clones an existing content search in the Security &amp; Compliance Center.
  # Get login credentials from the user
  if(!$UserCredential)
  {
      $UserCredential = Get-Credential
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
      if (!$Session)
      {
          Write-Error "Couldn't create a remote PowerShell session."
          return
      }
      Import-PSSession $Session -AllowClobber -DisableNameChecking
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Security & Compliance Center)"
  }
  # Ask for the name of the search you want to clone
  $searchName = Read-Host 'Enter the name of the search that you want to clone'
  # Ask for the name of the new search
  $newSearchName = Read-Host 'Enter a name for the new search [leave blank to automatically generate a name]'
  $originalSearch = Get-ComplianceSearch $searchName -EA SilentlyContinue
  # Make sure we have a valid search before continuing
  if(!$originalSearch)
  {
      Write-Error "Couldn't find search: $searchName"
      return
  }
  $searchNameCounter = 1
  # Find a suitable name for the new search
  while(!$newSearchName)
  {
      $newSearchName = $originalSearch.Name + "_" + $searchNameCounter
      $tempSearch = Get-ComplianceSearch $newSearchName -EA SilentlyContinue
      if ($tempSearch)
      {
          $newSearchName = $null
          $searchNameCounter++
      }
  }
  $caseName
  # Determine if the search is part of a case; if so get the case name
  if ($originalSearch.CaseId)
  {
      $searchCase = Get-ComplianceCase $originalSearch.CaseId
      $caseName = $searchCase.Name
  }
  # Need to cast this value as a Boolean the old fashion way
  $allowNotFoundExchangeLocationsEnabled = $false
  if ($originalSearch.AllowNotFoundExchangeLocationsEnabled)
  {
      $allowNotFoundExchangeLocationsEnabled = $true
  }
  $newSearch = New-ComplianceSearch -Name $newSearchName -AllowNotFoundExchangeLocationsEnabled $allowNotFoundExchangeLocationsEnabled -Case $caseName -ContentMatchQuery $originalSearch.ContentMatchQuery -Description $originalSearch.Description -ExchangeLocation $originalSearch.ExchangeLocation -ExchangeLocationExclusion $originalSearch.ExchangeLocationExclusion -Language $originalSearch.Language -SharePointLocation $originalSearch.SharePointLocation -SharePointLocationExclusion $originalSearch.SharePointLocationExclusion -PublicFolderLocation $originalSearch.PublicFolderLocation
  if ($newSearch)
  {
      Write-Host $newSearch.Name "was successfully created" -ForegroundColor Yellow
  }
  ```

2. <span data-ttu-id="923a9-136">Ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="923a9-136">Open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="923a9-137">Exécutez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="923a9-137">Run the script; for example:</span></span>
    
    ```powershell
    .\CloneSearch.ps1
    ```

4. <span data-ttu-id="923a9-138">Lorsque vous êtes invité à entrer vos informations d’identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="923a9-138">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span>
    
5. <span data-ttu-id="923a9-139">Entrez les informations suivantes lorsque le script vous y invite.</span><span class="sxs-lookup"><span data-stu-id="923a9-139">Enter following information when prompted by the script.</span></span> <span data-ttu-id="923a9-140">Tapez chaque information, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="923a9-140">Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="923a9-141">Nom de la recherche existante.</span><span class="sxs-lookup"><span data-stu-id="923a9-141">The name of the existing search.</span></span>
    
    - <span data-ttu-id="923a9-142">Nom de la nouvelle recherche.</span><span class="sxs-lookup"><span data-stu-id="923a9-142">The name of the new search.</span></span>
    
    <span data-ttu-id="923a9-143">Le script crée la recherche de contenu, mais ne le démarre pas.</span><span class="sxs-lookup"><span data-stu-id="923a9-143">The script creates the new Content Search, but doesn't start it.</span></span> <span data-ttu-id="923a9-144">Cela vous permet de modifier et d’exécuter la recherche à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="923a9-144">This gives you a chance to edit and run the search in the next step.</span></span> <span data-ttu-id="923a9-145">Vous pouvez afficher les propriétés de la nouvelle recherche en exécutant la cmdlet **Get-ComplianceSearch** ou en accédant à la page **recherche de contenu** ou **découverte électronique** dans le centre de conformité, selon que la nouvelle recherche est associée ou non à un cas.</span><span class="sxs-lookup"><span data-stu-id="923a9-145">You can view the properties of the new search by running the **Get-ComplianceSearch** cmdlet or by going to the **Content search** or **eDiscovery** page in the compliance center, depending on whether the new search is associated with a case.</span></span> 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-compliance-center"></a><span data-ttu-id="923a9-146">Étape 2 : modifier et exécuter la recherche clonée dans le centre de conformité</span><span class="sxs-lookup"><span data-stu-id="923a9-146">Step 2: Edit and run the cloned search in the compliance center</span></span>

<span data-ttu-id="923a9-147">Une fois que vous avez exécuté le script pour cloner une recherche de contenu existante, l’étape suivante consiste à accéder au centre de conformité pour modifier et exécuter la nouvelle recherche.</span><span class="sxs-lookup"><span data-stu-id="923a9-147">After you run the script to clone an existing Content Search, the next step is to go to the compliance center to edit and run the new search.</span></span> <span data-ttu-id="923a9-148">Comme indiqué précédemment, vous pouvez modifier une recherche en modifiant la requête de recherche par mot clé et en ajoutant ou supprimant des conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="923a9-148">As previously stated, you can edit a search by changing the keyword search query and adding or removing search conditions.</span></span> <span data-ttu-id="923a9-149">Pour plus d’informations, reportez-vous aux rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="923a9-149">For more information, see:</span></span>
  
- [<span data-ttu-id="923a9-150">Recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="923a9-150">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="923a9-151">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="923a9-151">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
    
- [<span data-ttu-id="923a9-152">cas eDiscovery</span><span class="sxs-lookup"><span data-stu-id="923a9-152">eDiscovery cases</span></span>](ediscovery-cases.md)
