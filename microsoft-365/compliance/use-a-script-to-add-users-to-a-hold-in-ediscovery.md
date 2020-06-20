---
title: Utiliser un script pour ajouter des utilisateurs à une conservation dans un cas eDiscovery dans le centre de sécurité & conformité
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/23/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- SPO_Content
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
ms.custom: seo-marvel-apr2020
description: Découvrez comment exécuter un script pour ajouter des boîtes aux lettres & des sites OneDrive entreprise à une nouvelle conservation associée à un cas eDiscovery dans le centre de sécurité & Compliance Center.
ms.openlocfilehash: ff309bcc01bec5d67abbb0c9a0619a10ccebebac
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44819114"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-security--compliance-center"></a><span data-ttu-id="e20d9-103">Utiliser un script pour ajouter des utilisateurs à une conservation dans un cas eDiscovery dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="e20d9-103">Use a script to add users to a hold in an eDiscovery case in the Security & Compliance Center</span></span>

<span data-ttu-id="e20d9-104">Le centre de sécurité & conformité fournit un grand nombre d’applets de commande Windows PowerShell qui vous permettent d’automatiser des tâches consommatrices de temps liées à la création et à la gestion de cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="e20d9-104">The Security & Compliance Center provides lots of Windows PowerShell cmdlets that let you automate time-consuming tasks related to creating and managing eDiscovery cases.</span></span> <span data-ttu-id="e20d9-105">À l’heure actuelle, l’utilisation de l’outil de cas eDiscovery dans le centre de conformité & Compliance pour mettre en attente un grand nombre d’emplacements de contenu de dépositaire prend du temps et une préparation.</span><span class="sxs-lookup"><span data-stu-id="e20d9-105">Currently, using the eDiscovery case tool in the Security & Compliance Center to place a large number of custodian content locations on hold takes time and preparation.</span></span> <span data-ttu-id="e20d9-106">Par exemple, avant de créer une conservation, vous devez collecter l’URL de chaque site OneDrive entreprise que vous souhaitez mettre en attente.</span><span class="sxs-lookup"><span data-stu-id="e20d9-106">For example, before you create a hold, you have to collect the URL for each OneDrive for Business site that you want to place on hold.</span></span> <span data-ttu-id="e20d9-107">Ensuite, pour chaque utilisateur que vous souhaitez mettre en attente, vous devez ajouter sa boîte aux lettres et son site OneDrive entreprise à la suspension.</span><span class="sxs-lookup"><span data-stu-id="e20d9-107">Then for each user you want to place on hold, you have to add their mailbox and their OneDrive for Business site to the hold.</span></span> <span data-ttu-id="e20d9-108">Dans les prochaines versions du centre de sécurité & conformité, cela sera plus facile à réaliser.</span><span class="sxs-lookup"><span data-stu-id="e20d9-108">In future releases of the Security & Compliance Center, this will get easier to do.</span></span> <span data-ttu-id="e20d9-109">En attendant, vous pouvez utiliser le script de cet article pour automatiser ce processus.</span><span class="sxs-lookup"><span data-stu-id="e20d9-109">Until then, you can use the script in this article to automate this process.</span></span>
  
<span data-ttu-id="e20d9-110">Le script vous invite à indiquer le nom du domaine de site de votre organisation (par exemple, **contoso** dans l’URL https://contoso-my.sharepoint.com) , le nom d’un cas de découverte électronique existant, le nom du nouveau blocage associé au cas, la liste des adresses de messagerie des utilisateurs que vous souhaitez mettre en attente et une requête de recherche à utiliser si vous souhaitez créer une conservation basée sur une requête).</span><span class="sxs-lookup"><span data-stu-id="e20d9-110">The script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL https://contoso-my.sharepoint.com), the name of an existing eDiscovery case, the name of the new hold that associated with the case, a list of email addresses of the users you want to put on hold, and a search query to use if you want to create a query-based hold.</span></span> <span data-ttu-id="e20d9-111">Le script obtient ensuite l’URL du site OneDrive entreprise pour chaque utilisateur de la liste, crée la nouvelle conservation, puis ajoute la boîte aux lettres et le site OneDrive entreprise pour chaque utilisateur de la liste à la suspension.</span><span class="sxs-lookup"><span data-stu-id="e20d9-111">The script then gets the URL for the OneDrive for Business site for each user in the list, creates the new hold, and then adds the mailbox and OneDrive for Business site for each user in the list to the hold.</span></span> <span data-ttu-id="e20d9-112">Le script génère également des fichiers journaux qui contiennent des informations sur la nouvelle conservation.</span><span class="sxs-lookup"><span data-stu-id="e20d9-112">The script also generates log files that contain information about the new hold.</span></span> 
  
<span data-ttu-id="e20d9-113">Voici la procédure à suivre :</span><span class="sxs-lookup"><span data-stu-id="e20d9-113">Here are the steps to make this happen:</span></span>
  
[<span data-ttu-id="e20d9-114">Étape 1 : installer SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="e20d9-114">Step 1: Install the SharePoint Online Management Shell</span></span>](#step-1-install-the-sharepoint-online-management-shell)
  
[<span data-ttu-id="e20d9-115">Étape 2 : générer une liste d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e20d9-115">Step 2: Generate a list of users</span></span>](#step-2-generate-a-list-of-users)
  
[<span data-ttu-id="e20d9-116">Étape 3 : exécuter le script pour créer une conservation et ajouter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e20d9-116">Step 3: Run the script to create a hold and add users</span></span>](#step-3-run-the-script-to-create-a-hold-and-add-users)
  
## <a name="before-you-add-users-to-a-hold"></a><span data-ttu-id="e20d9-117">Avant d’ajouter des utilisateurs à une suspension</span><span class="sxs-lookup"><span data-stu-id="e20d9-117">Before you add users to a hold</span></span>

- <span data-ttu-id="e20d9-118">Vous devez être membre du groupe de rôles gestionnaire de découverte électronique dans le centre de sécurité & conformité et d’un administrateur global SharePoint Online pour exécuter le script à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="e20d9-118">You have to be a member of the eDiscovery Manager role group in the Security & Compliance Center and a SharePoint Online global administrator to run the script in Step 3.</span></span> <span data-ttu-id="e20d9-119">Pour plus d’informations, consultez [la rubrique attribution d’autorisations de découverte électronique dans le centre de conformité & Office 365 Security](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="e20d9-119">For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security & Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="e20d9-120">Un maximum de 1 000 boîtes aux lettres et 100 sites peuvent être ajoutés à une conservation qui est associée à un cas de découverte électronique dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="e20d9-120">A maximum of 1,000 mailboxes and 100 sites can be added to a hold that's associated with an eDiscovery case in the Security & Compliance Center.</span></span> <span data-ttu-id="e20d9-121">En supposant que chaque utilisateur que vous souhaitez mettre en attente dispose d’un site OneDrive entreprise, vous pouvez ajouter un maximum de 100 utilisateurs à une conservation à l’aide du script de cet article.</span><span class="sxs-lookup"><span data-stu-id="e20d9-121">Assuming that every user that you want to place on hold has a OneDrive for Business site, you can add a maximum of 100 users to a hold using the script in this article.</span></span> 
    
- <span data-ttu-id="e20d9-122">Veillez à enregistrer la liste des utilisateurs que vous créez à l’étape 2 et le script de l’étape 3 dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="e20d9-122">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder.</span></span> <span data-ttu-id="e20d9-123">Cela facilitera l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="e20d9-123">That will make it easier to run the script.</span></span>
    
- <span data-ttu-id="e20d9-124">Le script ajoute la liste des utilisateurs à une nouvelle conservation associée à un cas existant.</span><span class="sxs-lookup"><span data-stu-id="e20d9-124">The script adds the list of users to a new hold that is associated with an existing case.</span></span> <span data-ttu-id="e20d9-125">Assurez-vous que le cas où vous souhaitez associer le blocage est créé avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="e20d9-125">Be sure the case that you want to associate the hold with is created before you run the script.</span></span>
    
- <span data-ttu-id="e20d9-126">Le script inclut une gestion des erreurs minimale.</span><span class="sxs-lookup"><span data-stu-id="e20d9-126">The script includes minimal error handling.</span></span> <span data-ttu-id="e20d9-127">Son objectif principal est de placer rapidement et facilement la boîte aux lettres et le site OneDrive entreprise de chaque utilisateur en conservation.</span><span class="sxs-lookup"><span data-stu-id="e20d9-127">Its primary purpose is to quickly and easily place the mailbox and OneDrive for Business site of each user on hold.</span></span>
    
- <span data-ttu-id="e20d9-128">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service.</span><span class="sxs-lookup"><span data-stu-id="e20d9-128">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service.</span></span> <span data-ttu-id="e20d9-129">The sample scripts are provided AS IS without warranty of any kind.</span><span class="sxs-lookup"><span data-stu-id="e20d9-129">The sample scripts are provided AS IS without warranty of any kind.</span></span> <span data-ttu-id="e20d9-130">Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span><span class="sxs-lookup"><span data-stu-id="e20d9-130">Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span></span> <span data-ttu-id="e20d9-131">The entire risk arising out of the use or performance of the sample scripts and documentation remains with you.</span><span class="sxs-lookup"><span data-stu-id="e20d9-131">The entire risk arising out of the use or performance of the sample scripts and documentation remains with you.</span></span> <span data-ttu-id="e20d9-132">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span><span class="sxs-lookup"><span data-stu-id="e20d9-132">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>

## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="e20d9-133">Étape 1 : installer SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="e20d9-133">Step 1: Install the SharePoint Online Management Shell</span></span>

<span data-ttu-id="e20d9-134">La première étape consiste à installer SharePoint Online Management Shell s’il n’est pas déjà installé sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e20d9-134">The first step is to install the SharePoint Online Management Shell if it's not already installed on your local computer.</span></span> <span data-ttu-id="e20d9-135">Vous n’avez pas besoin d’utiliser l’environnement de commande Exchange Management Shell dans cette procédure, mais vous devez l’installer car il contient les conditions préalables requises par le script exécuté à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="e20d9-135">You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3.</span></span> <span data-ttu-id="e20d9-136">Ces conditions préalables permettent au script de communiquer avec SharePoint Online pour obtenir les URL des sites OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="e20d9-136">These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="e20d9-137">Accédez à [la configuration de l’environnement Windows PowerShell de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkID=286318) et effectuez les étapes 1 et 2 pour installer SharePoint Online Management Shell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e20d9-137">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell on your local computer.</span></span> 

## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="e20d9-138">Étape 2 : générer une liste d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e20d9-138">Step 2: Generate a list of users</span></span>

<span data-ttu-id="e20d9-139">Le script de l’étape 3 crée une conservation associée à un cas de découverte électronique, ainsi que les sites ajouter les boîtes aux lettres et OneDrive entreprise d’une liste d’utilisateurs à la suspension.</span><span class="sxs-lookup"><span data-stu-id="e20d9-139">The script in Step 3 will create a hold that's associated with an eDiscovery case, and the add the mailboxes and OneDrive for Business sites of a list of users to the hold.</span></span> <span data-ttu-id="e20d9-140">Vous pouvez simplement taper les adresses de messagerie dans un fichier texte ou exécuter une commande dans Windows PowerShell pour obtenir la liste des adresses de messagerie et les enregistrer dans un fichier (situé dans le même dossier dans lequel vous enregistrerez le script à l’étape 3).</span><span class="sxs-lookup"><span data-stu-id="e20d9-140">You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="e20d9-141">Voici une commande PowerShell (que vous exécutez à l’aide de PowerShell distant connecté à votre organisation Exchange Online) pour obtenir la liste des adresses de messagerie de tous les utilisateurs de votre organisation et l’enregistrer dans un fichier texte nommé HoldUsers.txt.</span><span class="sxs-lookup"><span data-stu-id="e20d9-141">Here's a PowerShell command (that you run by using remote PowerShell connected to your Exchange Online organization) to get a list of email addresses for all users in your organization and save it to a text file named HoldUsers.txt.</span></span>
  
```powershell
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

<span data-ttu-id="e20d9-142">Après avoir exécuté cette commande, ouvrez le fichier texte et supprimez l’en-tête qui contient le nom de la propriété, `PrimarySmtpAddress` .</span><span class="sxs-lookup"><span data-stu-id="e20d9-142">After you run this command, open the text file and remove the header that contains the property name,  `PrimarySmtpAddress`.</span></span> <span data-ttu-id="e20d9-143">Ensuite, supprimez toutes les adresses de messagerie sauf celles des utilisateurs que vous souhaitez ajouter à la suspension que vous allez créer à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="e20d9-143">Then remove all email addresses except the ones for the users that you want to add to the hold that you'll create in Step 3.</span></span> <span data-ttu-id="e20d9-144">Assurez-vous qu’il n’y a pas de ligne vide avant ou après la liste des adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e20d9-144">Make sure there are no blank rows before or after the list of email addresses.</span></span>
  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a><span data-ttu-id="e20d9-145">Étape 3 : exécuter le script pour créer une conservation et ajouter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e20d9-145">Step 3: Run the script to create a hold and add users</span></span>

<span data-ttu-id="e20d9-146">Lorsque vous exécutez le script dans cette étape, il vous invite à fournir les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="e20d9-146">When you run the script in this step, it will prompt you for the following information.</span></span> <span data-ttu-id="e20d9-147">Assurez-vous que vous disposez de ces informations avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="e20d9-147">Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="e20d9-148">**Vos informations d’identification utilisateur** : le script utilisera vos informations d’identification pour vous connecter au centre de sécurité & conformité à l’aide de PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="e20d9-148">**Your user credentials** - The script will use your credentials to connect to the Security & Compliance Center with remote PowerShell.</span></span> <span data-ttu-id="e20d9-149">Il utilisera également ces informations d’identification pour accéder à SharePoint Online afin d’obtenir les URL OneDrive entreprise pour la liste des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e20d9-149">It will also use these credentials to access SharePoint Online to get the OneDrive for Business URLs for the list of users.</span></span>
    
- <span data-ttu-id="e20d9-150">**Nom de votre domaine mon** site : le domaine mon site est celui qui contient tous les sites OneDrive entreprise de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e20d9-150">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization.</span></span> <span data-ttu-id="e20d9-151">Par exemple, si l’URL de votre domaine mon site mon site est **https://contoso-my.sharepoint.com** , entrez alors `contoso` lorsque le script vous invite à indiquer le nom de votre domaine mon site.</span><span class="sxs-lookup"><span data-stu-id="e20d9-151">For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="e20d9-152">**Nom de la casse** : nom d’un incident existant.</span><span class="sxs-lookup"><span data-stu-id="e20d9-152">**Name of the case** - The name of an existing case.</span></span> <span data-ttu-id="e20d9-153">Le script crée une nouvelle conservation qui est associée à ce cas.</span><span class="sxs-lookup"><span data-stu-id="e20d9-153">The script will create a new hold that is associated with this case.</span></span>
    
- <span data-ttu-id="e20d9-154">**Nom du blocage** : nom du blocage que le script crée et associe à la casse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e20d9-154">**Name of the hold** - The name of the hold the script will create and associate with the specified case.</span></span>
    
- <span data-ttu-id="e20d9-155">**Requête de recherche pour une conservation basée sur une requête** : vous pouvez créer une conservation basée sur une requête de sorte que seul le contenu correspondant aux critères de recherche spécifiés soit placé en conservation.</span><span class="sxs-lookup"><span data-stu-id="e20d9-155">**Search query for a query-based hold** - You can create a query-based hold so that only the content that meets the specified search criteria is placed on hold.</span></span> <span data-ttu-id="e20d9-156">Pour placer tout le contenu en conservation, appuyez simplement sur **entrée** lorsque vous êtes invité à entrer une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="e20d9-156">To place all content on hold, just press **Enter** when you're prompted for a search query.</span></span> 
    
- <span data-ttu-id="e20d9-157">**Indique si le blocage doit** être activé : vous pouvez faire en sorte que le script désactive le blocage une fois qu’il a été créé ou que le script peut créer la conservation sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="e20d9-157">**Whether or not to turn the hold on** - You can have the script turn the hold on after it's created or you can have the script create the hold without enabling it.</span></span> <span data-ttu-id="e20d9-158">Si le script n’est pas activé, vous pouvez l’activer ultérieurement dans le centre de sécurité & conformité ou en exécutant les commandes PowerShell suivantes :</span><span class="sxs-lookup"><span data-stu-id="e20d9-158">If you don't have the script turn on the hold, you can turn it on later in the Security & Compliance Center or by running the following PowerShell commands:</span></span> 
    
  ```powershell
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```powershell
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- <span data-ttu-id="e20d9-159">**Nom du fichier texte avec la liste d’utilisateurs** : le nom du fichier texte de l’étape 2 qui contient la liste des utilisateurs à ajouter à la suspension.</span><span class="sxs-lookup"><span data-stu-id="e20d9-159">**Name of the text file with the list of users** - The name of the text file from Step 2 that contains the list of users to add to the hold.</span></span> <span data-ttu-id="e20d9-160">Si ce fichier se trouve dans le même dossier que le script, il vous suffit de taper le nom du fichier (par exemple, HoldUsers.txt).</span><span class="sxs-lookup"><span data-stu-id="e20d9-160">If this file is located in the same folder as the script, just type the name of the file (for example, HoldUsers.txt).</span></span> <span data-ttu-id="e20d9-161">Si le fichier texte se trouve dans un autre dossier, tapez le chemin d’accès complet du fichier.</span><span class="sxs-lookup"><span data-stu-id="e20d9-161">If the text file is in another folder, type the full pathname of the file.</span></span>
    
<span data-ttu-id="e20d9-162">Une fois que vous avez collecté les informations que le script vous demande, la dernière étape consiste à exécuter le script pour créer la nouvelle conservation et y ajouter des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e20d9-162">After you've collected the information that the script will prompt you for, the final step is to run the script to create the new hold and add users to it.</span></span>
  
1. <span data-ttu-id="e20d9-163">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1 ; par exemple, `AddUsersToHold.ps1` .</span><span class="sxs-lookup"><span data-stu-id="e20d9-163">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `AddUsersToHold.ps1`.</span></span>
    
  ```powershell
  #script begin
  " " 
  write-host "***********************************************"
  write-host "   Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery cases - Add users to a hold   " -foregroundColor yellow -backgroundcolor darkgreen 
  write-host "***********************************************"
  " " 
  # Get user credentials &amp; Connect to Office 365 SCC, SPO
  $credentials = Get-Credential -Message "Specify your credentials to connect to the Security & Compliance Center and SharePoint Online"
  $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
  $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Couldn't create PowerShell session."
          return;
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
          Write-Error "The SharePoint Online Management Shell isn't installed. Please install it from: https://go.microsoft.com/fwlink/p/?LinkId=255251 and then re-run this script."
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
  # Get the user's MySite domain name. We use this to create the admin URL and root URL for OneDrive for Business
  ""
  $mySiteDomain = Read-Host "Enter the name of your organization's MySite domain. For example, 'contoso' for 'https://contoso-my.sharepoint.com'"
  ""
  # Get other required information
  do{
  $casename = Read-Host "Enter the name of the case"
  $caseexists = (get-compliancecase -identity "$casename" -erroraction SilentlyContinue).isvalid
  if($caseexists -ne 'True')
  {""
  write-host "A case named '$casename' doesn't exist. Please specify the name of an existing case, or create a new case and then re-run the script." -foregroundColor Yellow
  ""}
  }While($caseexists -ne 'True')
  ""
  do{
  $holdName = Read-Host "Enter the name of the new hold"
  $holdexists=(get-caseholdpolicy -identity "$holdname" -case "$casename" -erroraction SilentlyContinue).isvalid
  if($holdexists -eq 'True')
  {""
  write-host "A hold named '$holdname' already exists. Please specify a new hold name." -foregroundColor Yellow
  ""}
  }While($holdexists -eq 'True')
  ""
  $holdQuery = Read-Host "Enter a search query to create a query-based hold, or press Enter to hold all content"
  ""
  $holdstatus = read-host "Do you want the hold enabled after it's created? (Yes/No)"
  do{
  ""
  $inputfile = read-host "Enter the name of the text file that contains the email addresses of the users to add to the hold"
  ""
  $fileexists = test-path -path $inputfile
  if($fileexists -ne 'True'){write-host "$inputfile doesn't exist. Please enter a valid file name." -foregroundcolor Yellow}
  }while($fileexists -ne 'True')
  #Import the list of addresses from the txt file.  Trim any excess spaces and make sure all addresses 
      #in the list are unique.
    [array]$emailAddresses = Get-Content $inputfile -ErrorAction SilentlyContinue | where {$_.trim() -ne ""}  | foreach{ $_.Trim() }
    [int]$dupl = $emailAddresses.count
    [array]$emailAddresses = $emailAddresses | select-object -unique
    $dupl -= $emailAddresses.count
  #Validate email addresses so the hold creation does not run in to an error.
  if($emailaddresses.count -gt 0){
  write-host ($emailAddresses).count "addresses were found in the text file. There were $dupl duplicate entries in the file." -foregroundColor Yellow
  ""
  Write-host "Validating the email addresses. Please wait..." -foregroundColor Yellow
  ""
  $finallist =@()
  foreach($emailAddress in $emailAddresses)
  {
  if((get-recipient $emailaddress -erroraction SilentlyContinue).isvalid -eq 'True')
  {$finallist += $emailaddress}
  else {"Unable to find the user $emailaddress"
  [array]$excludedlist += $emailaddress}
  }
  ""
  #find user's OneDrive Site URL using email address
  Write-Host "Getting the URL for each user's OneDrive for Business site." -foregroundColor Yellow
  ""
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
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
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
        try{
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" }
          $url = $prop.values[0].value
        if($url -ne $null){
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "- $emailAddress => $furl"
        [array]$ODadded += $furl}
    else{    
          Write-Warning "Couldn't locate OneDrive for $emailAddress"
        [array]$ODExluded += $emailAddress
      }}
    catch { 
    Write-Warning "Could not locate OneDrive for $emailAddress"
    [array]$ODExluded += $emailAddress
    Continue }
  }
  if(($finallist.count -gt 0) -or ($urls.count -gt 0)){
  ""
  Write-Host "Creating the hold named $holdname. Please wait..." -foregroundColor Yellow
  if(($holdstatus -eq "Y") -or ($holdstatus -eq  "y") -or ($holdstatus -eq "yes") -or ($holdstatus -eq "YES")){
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $True | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery | out-null
  }
  else{
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $false | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery -disabled $true | out-null
  }
  ""
  }
  else {"No valid locations were identified. Therefore, the hold wasn't created."}
  #write log files (if needed)
  $newhold=Get-CaseHoldPolicy -Identity "$holdname" -Case "$casename" -erroraction SilentlyContinue
  $newholdrule=Get-CaseHoldRule -Identity "$holdName" -erroraction SilentlyContinue
  if(($ODAdded.count -gt 0) -or ($ODExluded.count -gt 0) -or ($finallist.count -gt 0) -or ($excludedlist.count -gt 0) -or ($newhold.isvalid -eq 'True') -or ($newholdrule.isvalid -eq 'True'))
  {
  Write-Host "Generating output files..." -foregroundColor Yellow
  if($ODAdded.count -gt 0){
  "OneDrive Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.SharePointLocation.name | add-content .\LocationsOnHold.txt}
  if($ODExluded.count -gt 0){ 
  "Users without OneDrive locations" | add-content .\LocationsNotOnHold.txt
  "================================" | add-content .\LocationsNotOnHold.txt
  $ODExluded | add-content .\LocationsNotOnHold.txt}
  if($finallist.count -gt 0){
  " " | add-content .\LocationsOnHold.txt
  "Exchange Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.ExchangeLocation.name | add-content .\LocationsOnHold.txt}
  if($excludedlist.count -gt 0){
  " "| add-content .\LocationsNotOnHold.txt
  "Mailboxes not added to the hold" | add-content .\LocationsNotOnHold.txt
  "===============================" | add-content .\LocationsNotOnHold.txt
  $excludedlist | add-content .\LocationsNotOnHold.txt}
  $FormatEnumerationLimit=-1
  if($newhold.isvalid -eq 'True'){$newhold|fl >.\GetCaseHoldPolicy.txt}
  if($newholdrule.isvalid -eq 'True'){$newholdrule|Fl >.\GetCaseHoldRule.txt}
  }
  }
  else {"The hold wasn't created because no valid entries were found in the text file."}
  ""
  Write-host "Script complete!" -foregroundColor Yellow
  ""
  #script end
  ```

2. <span data-ttu-id="e20d9-164">Sur votre ordinateur local, ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="e20d9-164">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="e20d9-165">Exécutez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="e20d9-165">Run the script; for example:</span></span>
    
      ```powershell
    .\AddUsersToHold.ps1
      ```

4. <span data-ttu-id="e20d9-166">Entrez les informations que le script vous demande.</span><span class="sxs-lookup"><span data-stu-id="e20d9-166">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="e20d9-167">Le script se connecte à la sécurité & Centre de conformité PowerShell, puis crée la nouvelle conservation dans le cas de découverte électronique et ajoute les boîtes aux lettres et OneDrive entreprise pour les utilisateurs de la liste.</span><span class="sxs-lookup"><span data-stu-id="e20d9-167">The script connects to Security & Compliance Center PowerShell, and then creates the new hold in the eDiscovery case and adds the mailboxes and OneDrive for Business for the users in the list.</span></span> <span data-ttu-id="e20d9-168">Vous pouvez accéder à la page de **découverte électronique** dans le centre de sécurité & Compliance Center pour afficher le nouveau blocage.</span><span class="sxs-lookup"><span data-stu-id="e20d9-168">You can go to the case on the **eDiscovery** page in the Security & Compliance Center to view the new hold.</span></span> 
    
<span data-ttu-id="e20d9-169">Une fois l’exécution du script terminée, les fichiers journaux suivants sont créés et enregistrés dans le dossier où se trouve le script.</span><span class="sxs-lookup"><span data-stu-id="e20d9-169">After the script is finished running, it creates the following log files, and saves them to the folder where the script is located.</span></span>
  
- <span data-ttu-id="e20d9-170">**LocationsOnHold.txt** -contient une liste de boîtes aux lettres et de sites OneDrive entreprise pour lesquels le script a été mis en attente.</span><span class="sxs-lookup"><span data-stu-id="e20d9-170">**LocationsOnHold.txt** - Contains a list of mailboxes and OneDrive for Business sites that the script successfully placed on hold.</span></span>
    
- <span data-ttu-id="e20d9-171">**LocationsNotOnHold.txt** -contient une liste de boîtes aux lettres et de sites OneDrive entreprise que le script n’a pas placé en attente.</span><span class="sxs-lookup"><span data-stu-id="e20d9-171">**LocationsNotOnHold.txt** - Contains a list of mailboxes and OneDrive for Business sites that the script did not place on hold.</span></span> <span data-ttu-id="e20d9-172">Si un utilisateur dispose d’une boîte aux lettres, mais pas d’un site OneDrive entreprise, l’utilisateur est inclus dans la liste des sites OneDrive entreprise qui n’ont pas été mis en attente.</span><span class="sxs-lookup"><span data-stu-id="e20d9-172">If a user has a mailbox, but not a OneDrive for Business site, the user would be included in the list of OneDrive for Business sites that weren't placed on hold.</span></span>
    
- <span data-ttu-id="e20d9-173">**GetCaseHoldPolicy.txt** -contient la sortie de la cmdlet **Get-CaseHoldPolicy** pour le nouveau blocage, que le script a exécuté après avoir créé la nouvelle conservation.</span><span class="sxs-lookup"><span data-stu-id="e20d9-173">**GetCaseHoldPolicy.txt** - Contains the output of the **Get-CaseHoldPolicy** cmdlet for the new hold, which the script ran after creating the new hold.</span></span> <span data-ttu-id="e20d9-174">Les informations renvoyées par cette cmdlet incluent une liste d’utilisateurs dont les boîtes aux lettres et les sites OneDrive entreprise ont été mis en attente et indique si la conservation est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="e20d9-174">The information returned by this cmdlet includes a list of users whose mailboxes and OneDrive for Business sites were placed on hold and whether the hold is enabled or disabled.</span></span> 
    
- <span data-ttu-id="e20d9-175">**GetCaseHoldRule.txt** -contient la sortie de la cmdlet **Get-CaseHoldRule** pour le nouveau blocage, que le script a exécuté après avoir créé la nouvelle conservation.</span><span class="sxs-lookup"><span data-stu-id="e20d9-175">**GetCaseHoldRule.txt** - Contains the output of the **Get-CaseHoldRule** cmdlet for the new hold, which the script ran after creating the new hold.</span></span> <span data-ttu-id="e20d9-176">Les informations renvoyées par cette cmdlet incluent la requête de recherche si vous avez utilisé le script pour créer une conservation basée sur une requête.</span><span class="sxs-lookup"><span data-stu-id="e20d9-176">The information returned by this cmdlet includes the search query if you used the script to create a query-based hold.</span></span> 
