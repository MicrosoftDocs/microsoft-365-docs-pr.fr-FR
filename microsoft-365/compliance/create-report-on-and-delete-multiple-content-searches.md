---
title: Créer, générer des rapports et supprimer plusieurs recherches de contenu
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- SPO_Content
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 1d463dda-a3b5-4675-95d4-83db19c9c4a3
description: Découvrez comment automatiser des tâches de recherche de contenu, telles que la création de recherches et l’exécution de rapports via des scripts PowerShell dans le centre de sécurité & conformité dans Office 365.
ms.openlocfilehash: 6c92d9dab093b802acc518aebb96ddf83cf54ea5
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41595571"
---
# <a name="create-report-on-and-delete-multiple-content-searches"></a><span data-ttu-id="5e9be-103">Créer, générer des rapports et supprimer plusieurs recherches de contenu</span><span class="sxs-lookup"><span data-stu-id="5e9be-103">Create, report on, and delete multiple Content Searches</span></span>

 <span data-ttu-id="5e9be-104">La création et la création rapide de rapports de recherches de découverte est souvent une étape importante dans eDiscovery et des investigations lorsque vous essayez d’en savoir plus sur les données sous-jacentes, ainsi que la richesse et la qualité de vos recherches.</span><span class="sxs-lookup"><span data-stu-id="5e9be-104">Quickly creating and reporting discovery searches is often an important step in eDiscovery and investigations when you're trying to learn about the underlying data, and the richness and quality of your searches.</span></span> <span data-ttu-id="5e9be-105">Pour vous aider, le centre de sécurité & conformité PowerShell offre un ensemble d’applets de commande permettant d’automatiser les tâches de recherche de contenu gourmandes en temps.</span><span class="sxs-lookup"><span data-stu-id="5e9be-105">To help you do this, the Security & Compliance Center PowerShell offers a set of cmdlets to automate time-consuming Content Search tasks.</span></span> <span data-ttu-id="5e9be-106">Ces scripts offrent un moyen rapide et simple de créer plusieurs recherches, puis d’exécuter des rapports sur les résultats de recherche estimés qui peuvent vous aider à déterminer la quantité de données en question.</span><span class="sxs-lookup"><span data-stu-id="5e9be-106">These scripts provide a quick and easy way to create a number of searches, and then run reports of the estimated search results that can help you determine the quantity of data in question.</span></span> <span data-ttu-id="5e9be-107">Vous pouvez également utiliser les scripts pour créer différentes versions des recherches afin de comparer les résultats générés par chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="5e9be-107">You can also use the scripts to create different versions of searches to compare the results each one produces.</span></span> <span data-ttu-id="5e9be-108">Ces scripts peuvent vous aider à identifier et à rechercher rapidement vos données.</span><span class="sxs-lookup"><span data-stu-id="5e9be-108">These scripts can help you to quickly and efficiently identify and cull your data.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="5e9be-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5e9be-109">Before you begin</span></span>

- <span data-ttu-id="5e9be-110">Pour exécuter les scripts décrits dans cette rubrique, vous devez être membre du groupe de rôles gestionnaire eDiscovery dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="5e9be-110">You have to be a member of the eDiscovery Manager role group in the Security & Compliance Center to run the scripts that are described in this topic.</span></span> 
    
- <span data-ttu-id="5e9be-111">Pour collecter une liste des URL pour les sites OneDrive entreprise de votre organisation que vous pouvez ajouter au fichier CSV à l’étape 1, reportez-vous à la rubrique [créer une liste de tous les emplacements OneDrive de votre organisation](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span><span class="sxs-lookup"><span data-stu-id="5e9be-111">To collect a list of the URLs for the OneDrive for Business sites in your organization that you can add to the CSV file in Step 1, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span></span> 
    
- <span data-ttu-id="5e9be-112">Veillez à enregistrer tous les fichiers que vous créez dans cette rubrique dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="5e9be-112">Be sure to save all the files that you create in this topic to the same folder.</span></span> <span data-ttu-id="5e9be-113">Cela facilitera l’exécution des scripts.</span><span class="sxs-lookup"><span data-stu-id="5e9be-113">That will make it easier to run the scripts.</span></span>
    
- <span data-ttu-id="5e9be-114">Les scripts incluent une gestion des erreurs minimale.</span><span class="sxs-lookup"><span data-stu-id="5e9be-114">The scripts include minimal error handling.</span></span> <span data-ttu-id="5e9be-115">Leur objectif principal est de créer, de générer des rapports et de supprimer rapidement plusieurs recherches de contenu.</span><span class="sxs-lookup"><span data-stu-id="5e9be-115">Their primary purpose is to quickly create, report on, and delete multiple Content Searches.</span></span>
    
- <span data-ttu-id="5e9be-p104">Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="5e9be-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a><span data-ttu-id="5e9be-121">Étape 1 : créer un fichier CSV contenant des informations sur les recherches à exécuter</span><span class="sxs-lookup"><span data-stu-id="5e9be-121">Step 1: Create a CSV file that contains information about the searches you want to run</span></span>

<span data-ttu-id="5e9be-122">Le fichier de valeurs séparées par des virgules (CSV) que vous créez dans cette étape contient une ligne pour chaque utilisateur qui souhaite effectuer une recherche.</span><span class="sxs-lookup"><span data-stu-id="5e9be-122">The comma separated value (CSV) file that you create in this step contains a row for each user that want to search.</span></span> <span data-ttu-id="5e9be-123">Vous pouvez effectuer une recherche dans la boîte aux lettres Exchange Online de l’utilisateur (qui inclut la boîte aux lettres d’archivage, si elle est activée) et son site OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="5e9be-123">You can search the user's Exchange Online mailbox (which includes the archive mailbox, if it's enabled) and their OneDrive for Business site.</span></span> <span data-ttu-id="5e9be-124">Vous pouvez également rechercher uniquement dans la boîte aux lettres ou dans le site OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="5e9be-124">Or you can search just the mailbox or the OneDrive for Business site.</span></span> <span data-ttu-id="5e9be-125">Vous pouvez également effectuer des recherches dans n’importe quel site de votre organisation SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="5e9be-125">You can also search any site in your SharePoint Online organization.</span></span> <span data-ttu-id="5e9be-126">Le script que vous exécutez à l’étape 3 crée une recherche distincte pour chaque ligne dans le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="5e9be-126">The script that you run in Step 3 will create a separate search for each row in the CSV file.</span></span> 
  
1. <span data-ttu-id="5e9be-127">Copiez et collez le texte suivant dans un fichier. txt à l’aide du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="5e9be-127">Copy and paste the following text into a .txt file using NotePad.</span></span> <span data-ttu-id="5e9be-128">Enregistrez ce fichier dans un dossier sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="5e9be-128">Save this file to a folder on your local computer.</span></span> <span data-ttu-id="5e9be-129">Vous allez également enregistrer les autres scripts dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="5e9be-129">You'll save the other scripts to this folder as well.</span></span>
    
    ```text
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    <span data-ttu-id="5e9be-130">La première ligne, ou ligne d’en-tête, du fichier répertorie les paramètres qui seront utilisés par la cmdlet **New-ComplianceSearch** (dans le script de l’étape 3) pour créer des recherches de contenu.</span><span class="sxs-lookup"><span data-stu-id="5e9be-130">The first row, or header row, of the file lists the parameters that will be used by **New-ComplianceSearch** cmdlet (in the script in Step 3) to create a new Content Searches.</span></span> <span data-ttu-id="5e9be-131">Les noms des paramètres sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5e9be-131">Each parameter name is separated by a comma.</span></span> <span data-ttu-id="5e9be-132">Vérifiez qu’il n’y a pas d’espaces dans la ligne d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="5e9be-132">Make sure there aren't any spaces in the header row.</span></span> <span data-ttu-id="5e9be-133">Chaque ligne sous la ligne d’en-tête représente les valeurs des paramètres de chaque recherche.</span><span class="sxs-lookup"><span data-stu-id="5e9be-133">Each row under the header row represents the parameter values for each search.</span></span> <span data-ttu-id="5e9be-134">Veillez à remplacer les données d’espace réservé dans le fichier CSV par vos données réelles.</span><span class="sxs-lookup"><span data-stu-id="5e9be-134">Be sure to replace the placeholder data in the CSV file with your actual data.</span></span> 
    
2. <span data-ttu-id="5e9be-135">Ouvrez le fichier. txt dans Excel, puis utilisez les informations du tableau suivant pour modifier le fichier avec les informations pour chaque recherche.</span><span class="sxs-lookup"><span data-stu-id="5e9be-135">Open the .txt file in Excel, and then use the information in the following table to edit the file with information for each search.</span></span> 
    
    |<span data-ttu-id="5e9be-136">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="5e9be-136">**Parameter**</span></span>|<span data-ttu-id="5e9be-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="5e9be-137">**Description**</span></span>|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |<span data-ttu-id="5e9be-138">Adresse SMTP de la boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5e9be-138">The SMTP address of the user's mailbox.</span></span>  <br/> |
    | `SharePointLocation` <br/> |<span data-ttu-id="5e9be-139">L’URL du site OneDrive entreprise de l’utilisateur ou l’URL de n’importe quel site de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5e9be-139">The URL for the user's OneDrive for Business site or the URL for any site in your organization.</span></span> <span data-ttu-id="5e9be-140">Pour l’URL des sites OneDrive entreprise, utilisez le format suivant : ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `.</span><span class="sxs-lookup"><span data-stu-id="5e9be-140">For the URL for OneDrive for Business sites, use this format: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `.</span></span> <span data-ttu-id="5e9be-141">Par exemple : `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.</span><span class="sxs-lookup"><span data-stu-id="5e9be-141">For example,  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.</span></span>  <br/> |
    | `ContentMatchQuery` <br/> |<span data-ttu-id="5e9be-142">Requête de recherche pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="5e9be-142">The search query for the search.</span></span> <span data-ttu-id="5e9be-143">Pour plus d’informations sur la création d’une requête de recherche, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="5e9be-143">For more information about creating a search query, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>  <br/> |
    | `StartDate` <br/> |<span data-ttu-id="5e9be-144">Pour le courrier électronique, date à laquelle un message a été reçu par un destinataire ou envoyé par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="5e9be-144">For email, the date on or after a message was received by a recipient or sent by the sender.</span></span> <span data-ttu-id="5e9be-145">Pour les documents sur les sites SharePoint ou OneDrive entreprise, date de la dernière modification d’un document.</span><span class="sxs-lookup"><span data-stu-id="5e9be-145">For documents on SharePoint or OneDrive for Business sites, the date on or after a document was last modified.</span></span>  <br/> |
    | `EndDate` <br/> |<span data-ttu-id="5e9be-146">Pour le courrier électronique, date à laquelle un message a été envoyé par l’utilisateur ou avant celui-ci.</span><span class="sxs-lookup"><span data-stu-id="5e9be-146">For email, the date on or before a message was sent by a sent by the user.</span></span> <span data-ttu-id="5e9be-147">Pour les documents sur les sites SharePoint ou OneDrive entreprise, date de la dernière modification d’un document.</span><span class="sxs-lookup"><span data-stu-id="5e9be-147">For documents on SharePoint or OneDrive for Business sites, the date on or before a document was last modified.</span></span>  <br/> |
   
3. <span data-ttu-id="5e9be-148">Enregistrez le fichier Excel en tant que fichier CSV dans un dossier sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="5e9be-148">Save the Excel file as a CSV file to a folder on your local computer.</span></span> <span data-ttu-id="5e9be-149">Le script que vous créez à l’étape 3 utilise les informations contenues dans ce fichier CSV pour créer les recherches.</span><span class="sxs-lookup"><span data-stu-id="5e9be-149">The script that you create in Step 3 will use the information in this CSV file to create the searches.</span></span> 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a><span data-ttu-id="5e9be-150">Étape 2 : connectez-vous au Centre de sécurité et conformité PowerShell</span><span class="sxs-lookup"><span data-stu-id="5e9be-150">Step 2: Connect to Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="5e9be-151">L’étape suivante consiste à vous connecter au centre de sécurité & de conformité PowerShell pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5e9be-151">The next step is to connect to the Security & Compliance Center PowerShell for your organization.</span></span>
  
1. <span data-ttu-id="5e9be-152">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, `ConnectSCC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="5e9be-152">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`.</span></span> <span data-ttu-id="5e9be-153">Enregistrez le fichier dans le dossier dans lequel vous avez enregistré le fichier CSV à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="5e9be-153">Save the file to the same folder that you saved the CSV file to in Step 1.</span></span>
    
    ```powershell
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Security & Compliance Center)" 
    ```

2. <span data-ttu-id="5e9be-154">Sur votre ordinateur local, ouvrez Windows PowerShell, accédez au dossier dans lequel se trouve le script que vous avez créé à l’étape précédente, puis exécutez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="5e9be-154">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```powershell
    .\ConnectSCC.ps1
    ```

## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a><span data-ttu-id="5e9be-155">Étape 3 : exécuter le script pour créer et démarrer les recherches</span><span class="sxs-lookup"><span data-stu-id="5e9be-155">Step 3: Run the script to create and start the searches</span></span>

<span data-ttu-id="5e9be-156">Le script de cette étape crée une recherche de contenu distincte pour chaque ligne dans le fichier CSV que vous avez créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="5e9be-156">The script in this step will create a separate Content Search for each row in the CSV file that you created in Step 1.</span></span> <span data-ttu-id="5e9be-157">Lorsque vous exécutez ce script, vous êtes invité à indiquer deux valeurs :</span><span class="sxs-lookup"><span data-stu-id="5e9be-157">When you run this script, you'll be prompted for two values:</span></span>
  
- <span data-ttu-id="5e9be-158">**ID de groupe de recherche** : ce nom permet d’organiser facilement les recherches créées à partir du fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="5e9be-158">**Search Group ID** - This name provides an easy way to organize the searches that are created from the CSV file.</span></span> <span data-ttu-id="5e9be-159">Chaque recherche créée est nommée avec l’ID de groupe de recherche, puis un numéro est ajouté au nom de la recherche.</span><span class="sxs-lookup"><span data-stu-id="5e9be-159">Each search that's created is named with the Search Group ID, and then a number is appended to the search name.</span></span> <span data-ttu-id="5e9be-160">Par exemple, si vous entrez **ContosoCase** pour l’ID de groupe de recherche, les recherches sont nommées **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="5e9be-160">For example, if you enter **ContosoCase** for the Search Group ID, then the searches are named **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**, and so on.</span></span> <span data-ttu-id="5e9be-161">Notez que le nom que vous tapez est sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="5e9be-161">Note that the name you type is case sensitive.</span></span> <span data-ttu-id="5e9be-162">Lorsque vous utilisez l’ID de groupe de recherche à l’étape 4 et à l’étape 5, vous devez utiliser la même casse que celle que vous avez utilisée lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="5e9be-162">When you use the Search Group ID in Step 4 and Step 5, you have to use the same case as you did when you created it.</span></span> 
    
- <span data-ttu-id="5e9be-163">**Fichier CSV** : nom du fichier CSV que vous avez créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="5e9be-163">**CSV file** - The name of the CSV file that you created in Step 1.</span></span> <span data-ttu-id="5e9be-164">Veillez à inclure le nom de fichier complet, en incluant l’extension de fichier. csv ; par exemple, `ContosoCase.csv`.</span><span class="sxs-lookup"><span data-stu-id="5e9be-164">Be sure to include the use the full filename, include the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
<span data-ttu-id="5e9be-165">Pour exécuter le script :</span><span class="sxs-lookup"><span data-stu-id="5e9be-165">To run the script:</span></span>

1. <span data-ttu-id="5e9be-166">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, `CreateSearches.ps1`.</span><span class="sxs-lookup"><span data-stu-id="5e9be-166">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CreateSearches.ps1`.</span></span> <span data-ttu-id="5e9be-167">Enregistrez le fichier dans le dossier où vous avez enregistré les autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="5e9be-167">Save the file to the same folder where you saved the other files.</span></span>
    
  ```Powershell
  # Get the Search Group ID and the location of the CSV input file
  $searchGroup = Read-Host 'Search Group ID'
  $csvFile = Read-Host 'Source CSV file'
    
  # Do a quick check to make sure our group name will not collide with other searches
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    $searchName = $searchGroup +'_' + $searchCounter
    $search = Get-ComplianceSearch $searchName -EA SilentlyContinue
    if ($search)
    {
        Write-Error "The Search Group ID conflicts with existing searches.  Please choose a search group name and restart the script."
        return
    }
    $searchCounter++
  }
    
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    # Create the query
    $query = $_.ContentMatchQuery
    if(($_.StartDate -or $_.EndDate))
    {
          # Add the appropriate date restrictions.  NOTE: Using the Date condition property here because it works across Exchange, SharePoint, and OneDrive for Business.
          # For Exchange, the Date condition property maps to the Sent and Received dates; for SharePoint and OneDrive for Business, it maps to Created and Modified dates.
          if($query)
          {
              $query += " AND"
          }
          $query += " ("
          if($_.StartDate)
          {
              $query += "Date >= " + $_.StartDate
          }
          if($_.EndDate)
          {
              if($_.StartDate)
              {
                  $query += " AND "
              }
              $query += "Date <= " + $_.EndDate
          }
          $query += ")"
    }
      
      # -ExchangeLocation can't be set to an empty string, set to null if there's no location.
      $exchangeLocation = $null
      if ( $_.ExchangeLocation)
      {
           $exchangeLocation = $_.ExchangeLocation
      }
    
    # Create and run the search        
    $searchName = $searchGroup +'_' + $searchCounter
    Write-Host "Creating and running search: " $searchName -NoNewline
    $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $exchangeLocation -SharePointLocation $_.SharePointLocation -ContentMatchQuery $query
    
    # Start and wait for each search to complete
    Start-ComplianceSearch $search.Name
    while ((Get-ComplianceSearch $search.Name).Status -ne "Completed")
    {
        Write-Host " ." -NoNewline
        Start-Sleep -s 3
    }
    Write-Host ""
    
    $searchCounter++
  }
  ```

2. <span data-ttu-id="5e9be-168">Dans Windows PowerShell, accédez au dossier dans lequel vous avez enregistré le script à l’étape précédente, puis exécutez le script. par exemple :</span><span class="sxs-lookup"><span data-stu-id="5e9be-168">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\CreateSearches.ps1
    ```

3. <span data-ttu-id="5e9be-169">À l’invite **ID de groupe de recherche** , tapez un nom de groupe de recherche, puis appuyez sur **entrée**; par exemple, `ContosoCase`.</span><span class="sxs-lookup"><span data-stu-id="5e9be-169">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example,  `ContosoCase`.</span></span> <span data-ttu-id="5e9be-170">N’oubliez pas que ce nom est sensible à la casse, de sorte que vous devez le taper de la même manière dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e9be-170">Remember that this name is case sensitive, so you'll have to type it the same way in the subsequent steps.</span></span>
    
4. <span data-ttu-id="5e9be-171">À l’invite **fichier csv source** , tapez le nom du fichier CSV, y compris l’extension de fichier. csv ; par exemple, `ContosoCase.csv`.</span><span class="sxs-lookup"><span data-stu-id="5e9be-171">At the **Source CSV file** prompt, type the name of the CSV file, including the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
5. <span data-ttu-id="5e9be-172">Appuyez sur **entrée** pour poursuivre l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="5e9be-172">Press **Enter** to continue running the script.</span></span> 
    
    <span data-ttu-id="5e9be-173">Le script affiche la progression de la création et de l’exécution des recherches.</span><span class="sxs-lookup"><span data-stu-id="5e9be-173">The script displays the progress of creating and running the searches.</span></span> <span data-ttu-id="5e9be-174">Une fois le script terminé, il revient à l’invite.</span><span class="sxs-lookup"><span data-stu-id="5e9be-174">When the script is complete, it returns to the prompt.</span></span> 
    
    ![Exemple de sortie après exécution du script pour créer plusieurs recherches de la conformité](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a><span data-ttu-id="5e9be-176">Étape 4 : exécuter le script pour signaler les estimations de recherche</span><span class="sxs-lookup"><span data-stu-id="5e9be-176">Step 4: Run the script to report the search estimates</span></span>

<span data-ttu-id="5e9be-177">Une fois que vous avez créé les recherches, l’étape suivante consiste à exécuter un script qui affiche un rapport simple du nombre d’accès de recherche pour chaque recherche créée à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="5e9be-177">After you create the searches, the next step is to run a script that displays a simple report of the number of search hits for each search that was created in Step 3.</span></span> <span data-ttu-id="5e9be-178">Le rapport inclut également la taille des résultats pour chaque recherche, ainsi que le nombre total d’accès et la taille totale de toutes les recherches.</span><span class="sxs-lookup"><span data-stu-id="5e9be-178">The report also includes the size of results for each search, and the total number of hits and total size of all searches.</span></span> <span data-ttu-id="5e9be-179">Lorsque vous exécutez le script de création de rapports, vous êtes invité à entrer l’ID de groupe de recherche et un nom de fichier CSV Si vous voulez enregistrer le rapport dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="5e9be-179">When you run the reporting script, you'll be prompted for the Search Group ID, and a CSV filename if you want to save the report to a CSV file.</span></span>
  
1. <span data-ttu-id="5e9be-180">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, `SearchReport.ps1`.</span><span class="sxs-lookup"><span data-stu-id="5e9be-180">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchReport.ps1`.</span></span> <span data-ttu-id="5e9be-181">Enregistrez le fichier dans le dossier où vous avez enregistré les autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="5e9be-181">Save the file to the same folder where you saved the other files.</span></span>
    
  ```Powershell
  $searchGroup = Read-Host 'Search Group ID'
  $outputFile = Read-Host 'Enter a file name or file path to save the report to a .csv file. Leave blank to only display the report'
  $searches = Get-ComplianceSearch | ?{$_.Name -clike $searchGroup + "_*"}
  $allSearchStats = @()
  foreach ($partialObj in $searches)
  {
      $search = Get-ComplianceSearch $partialObj.Name
      $sizeMB = [System.Math]::Round($search.Size / 1MB, 2)
      $searchStatus = $search.Status
      if($search.Errors)
      {
          $searchStatus = "Failed"
      }elseif($search.NumFailedSources -gt 0)
      {
          $searchStatus = "Failed Sources"
      }
      $searchStats = New-Object PSObject
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Name -Value $search.Name
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name ContentMatchQuery -Value $search.ContentMatchQuery
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Status -Value $searchStatus
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Items -Value $search.Items
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size" -Value $search.Size
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size(MB)" -Value $sizeMB
      $allSearchStats += $searchStats
  }
  # Calculate the totals
  $allItems = ($allSearchStats | Measure-Object Items -Sum).Sum
  # Convert the total size to MB and round to the nearst 100th
  $allSize = ($allSearchStats | Measure-Object 'Size' -Sum).Sum
  $allSizeMB = [System.Math]::Round($allSize  / 1MB, 2)
  # Get the total successful searches and total of all searches
  $allSuccessCount = ($allSearchStats |?{$_.Status -eq "Completed"}).Count
  $allCount = $allSearchStats.Count
  $allStatus = [string]$allSuccessCount + " of " + [string]$allCount
  # Totals Row
  $totalSearchStats = New-Object PSObject
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Name -Value "Total"
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Status -Value $allStatus
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Items -Value $allItems
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name "Size(MB)" -Value $allSizeMB
  $allSearchStats += $totalSearchStats
  # Just get the columns we're interested in showing
  $allSearchStatsPrime = $allSearchStats | Select-Object Name, Status, Items, "Size(MB)", ContentMatchQuery
  # Print the results to the screen
  $allSearchStatsPrime |ft -AutoSize -Wrap
  # Save the results to a CSV file
  if ($outputFile)
  {
      $allSearchStatsPrime | Export-Csv -Path $outputFile -NoTypeInformation
  }
  ```

2. <span data-ttu-id="5e9be-182">Dans Windows PowerShell, accédez au dossier dans lequel vous avez enregistré le script à l’étape précédente, puis exécutez le script. par exemple :</span><span class="sxs-lookup"><span data-stu-id="5e9be-182">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\SearchReport.ps1
    ```

3. <span data-ttu-id="5e9be-183">À l’invite **ID de groupe de recherche** , tapez un nom de groupe de recherche, puis appuyez sur **entrée**; par exemple `ContosoCase`.</span><span class="sxs-lookup"><span data-stu-id="5e9be-183">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example  `ContosoCase`.</span></span> <span data-ttu-id="5e9be-184">N’oubliez pas que ce nom est sensible à la casse, de sorte que vous devez le taper de la même manière que lorsque vous avez exécuté le script à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="5e9be-184">Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
4. <span data-ttu-id="5e9be-185">Dans le **chemin d’accès du fichier pour enregistrer le rapport dans un fichier CSV (laissez vide pour afficher l’État)** , tapez le chemin d’accès complet du nom de fichier (y compris l’extension. csv) si vous souhaitez enregistrer le rapport dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="5e9be-185">At the **File path to save the report to a CSV file (leave blank to just display the report)** prompt, type a file name of complete filename path (including the .csv file extension) if you want to save the report to a CSV file.</span></span> <span data-ttu-id="5e9be-186">nom du fichier CSV, y compris l’extension de fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="5e9be-186">name of the CSV file, including the .csv file extension.</span></span> <span data-ttu-id="5e9be-187">Par exemple, vous pouvez taper `ContosoCaseReport.csv` pour l’enregistrer dans le répertoire actif ou taper `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` pour l’enregistrer dans un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="5e9be-187">For example, you could type  `ContosoCaseReport.csv` to save it to the current directory or you could type  `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` to save it to a different folder.</span></span> <span data-ttu-id="5e9be-188">Vous pouvez également laisser l’invite vide pour afficher le rapport sans l’enregistrer dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="5e9be-188">You can also leave the prompt blank to display the report but not save it to a file.</span></span> 
    
5. <span data-ttu-id="5e9be-189">Appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="5e9be-189">Press **Enter**.</span></span>
    
    <span data-ttu-id="5e9be-190">Le script affiche la progression de la création et de l’exécution des recherches.</span><span class="sxs-lookup"><span data-stu-id="5e9be-190">The script displays the progress of creating and running the searches.</span></span> <span data-ttu-id="5e9be-191">Une fois le script terminé, le rapport est affiché.</span><span class="sxs-lookup"><span data-stu-id="5e9be-191">When the script is complete, the report is displayed.</span></span> 
    
    ![Exécutez le rapport de recherche pour afficher les estimations pour le groupe de recherche](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> <span data-ttu-id="5e9be-193">Si la même boîte aux lettres ou le même site est spécifié en tant qu’emplacement de contenu dans plusieurs recherches dans un groupe de recherche, le nombre total d’estimations de résultats dans le rapport (pour le nombre d’éléments et la taille totale) peut inclure les résultats pour les mêmes éléments.</span><span class="sxs-lookup"><span data-stu-id="5e9be-193">If the same mailbox or site is specified as a content location in more than one search in a search group, the total results estimate in the report (for both the number of items and the total size) might include results for the same items.</span></span> <span data-ttu-id="5e9be-194">Cela est dû au fait que le même message électronique ou document est comptabilisé plusieurs fois s’il correspond à la requête pour différentes recherches dans le groupe de recherche.</span><span class="sxs-lookup"><span data-stu-id="5e9be-194">That's because the same email message or document will be counted more than once if it matches the query for different searches in the search group.</span></span> 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a><span data-ttu-id="5e9be-195">Étape 5 : exécuter le script pour supprimer les recherches</span><span class="sxs-lookup"><span data-stu-id="5e9be-195">Step 5: Run the script to delete the searches</span></span>

<span data-ttu-id="5e9be-196">Étant donné que vous pouvez créer un grand nombre de recherches, ce dernier script facilite la suppression rapide des recherches que vous avez créées à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="5e9be-196">Because you might be creating a lot of searches, this last script just makes it easy to quickly delete the searches you created in Step 3.</span></span> <span data-ttu-id="5e9be-197">Comme les autres scripts, il vous invite également à indiquer l’ID de groupe de recherche.</span><span class="sxs-lookup"><span data-stu-id="5e9be-197">Like the other scripts, this one also prompts you for the Search Group ID.</span></span> <span data-ttu-id="5e9be-198">Toutes les recherches avec l’ID de groupe de recherche dans le nom de recherche seront supprimées lorsque vous exécuterez ce script.</span><span class="sxs-lookup"><span data-stu-id="5e9be-198">All searches with the Search Group ID in the search name will be deleted when you run this script.</span></span> 
  
1. <span data-ttu-id="5e9be-199">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, `DeleteSearches.ps1`.</span><span class="sxs-lookup"><span data-stu-id="5e9be-199">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `DeleteSearches.ps1`.</span></span> <span data-ttu-id="5e9be-200">Enregistrez le fichier dans le dossier où vous avez enregistré les autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="5e9be-200">Save the file to the same folder where you saved the other files.</span></span>
    
  ```Powershell
  # Delete all searches in a search group
  $searchGroup = Read-Host 'Search Group ID'
  Get-ComplianceSearch |
      ForEach-Object{
      # If the name matches the search group name pattern (case sensitive), delete the search
      if ($_.Name -cmatch $searchGroup + "_\d+")
      {
          Write-Host "Deleting search: " $_.Name
          Remove-ComplianceSearch $_.Name -Confirm:$false
      }
  }
  ```

2. <span data-ttu-id="5e9be-201">Dans Windows PowerShell, accédez au dossier dans lequel vous avez enregistré le script à l’étape précédente, puis exécutez le script. par exemple :</span><span class="sxs-lookup"><span data-stu-id="5e9be-201">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\DeleteSearches.ps1
    ```

3. <span data-ttu-id="5e9be-202">À l’invite **ID de groupe de recherche** , tapez un nom de groupe de recherche pour les recherches que vous souhaitez supprimer, puis appuyez sur **entrée**; par exemple, `ContosoCase`.</span><span class="sxs-lookup"><span data-stu-id="5e9be-202">At the **Search Group ID** prompt, type a search group name for the searches that you want to delete, and then press **Enter**; for example,  `ContosoCase`.</span></span> <span data-ttu-id="5e9be-203">N’oubliez pas que ce nom est sensible à la casse, de sorte que vous devez le taper de la même manière que lorsque vous avez exécuté le script à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="5e9be-203">Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
    <span data-ttu-id="5e9be-204">Le script affiche le nom de chaque recherche qui a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="5e9be-204">The script displays the name of each search that's deleted.</span></span>
    
    ![Exécutez le script pour supprimer les recherches dans le groupe de recherche](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
