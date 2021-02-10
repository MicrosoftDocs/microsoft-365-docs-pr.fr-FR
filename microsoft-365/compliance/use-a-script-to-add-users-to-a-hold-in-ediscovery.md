---
title: Utiliser un script pour ajouter des utilisateurs à une attente dans un cas core eDiscovery
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
- SPO_Content
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
ms.custom: seo-marvel-apr2020
description: Découvrez comment exécuter un script pour ajouter des boîtes aux lettres & sites OneDrive Entreprise à une nouvelle mise en attente associée à un cas eDiscovery dans le Centre de conformité Microsoft 365.
ms.openlocfilehash: 278e8e051165eca906e9b454268068cbbe6aef05
ms.sourcegitcommit: 3dc795ea862b180484f76b3eb5d046e74041252b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "50175573"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-a-core-ediscovery-case"></a><span data-ttu-id="6cba9-103">Utiliser un script pour ajouter des utilisateurs à une attente dans un cas core eDiscovery</span><span class="sxs-lookup"><span data-stu-id="6cba9-103">Use a script to add users to a hold in a Core eDiscovery case</span></span>

<span data-ttu-id="6cba9-104">Le Centre de sécurité & conformité PowerShell fournit des cmdlets qui vous permettent d’automatiser des tâches chronophages liées à la création et à la gestion des cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="6cba9-104">Security & Compliance Center PowerShell provides cmdlets that let you automate time-consuming tasks related to creating and managing eDiscovery cases.</span></span> <span data-ttu-id="6cba9-105">Actuellement, l’utilisation du cas eDiscovery principal dans le Centre de sécurité & conformité pour placer un grand nombre d’emplacements de contenu de dépositaire en conservation prend du temps et de préparation.</span><span class="sxs-lookup"><span data-stu-id="6cba9-105">Currently, using the Core eDiscovery case in the Security & Compliance Center to place a large number of custodian content locations on hold takes time and preparation.</span></span> <span data-ttu-id="6cba9-106">Par exemple, avant de créer une attente, vous devez collecter l’URL de chaque site OneDrive Entreprise que vous souhaitez placer en attente.</span><span class="sxs-lookup"><span data-stu-id="6cba9-106">For example, before you create a hold, you have to collect the URL for each OneDrive for Business site that you want to place on hold.</span></span> <span data-ttu-id="6cba9-107">Ensuite, pour chaque utilisateur que vous souhaitez placer en attente, vous devez ajouter sa boîte aux lettres et son site OneDrive Entreprise à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6cba9-107">Then for each user you want to place on hold, you have to add their mailbox and their OneDrive for Business site to the hold.</span></span> <span data-ttu-id="6cba9-108">Vous pouvez utiliser le script de cet article pour automatiser ce processus.</span><span class="sxs-lookup"><span data-stu-id="6cba9-108">You can use the script in this article to automate this process.</span></span>
  
<span data-ttu-id="6cba9-109">Le script vous invite à donner le nom du domaine Mon site de votre organisation (par exemple, dans l’URL, le nom d’un cas `contoso` eDiscovery existant, le nom de la nouvelle mise en attente associée au cas, une liste des adresses e-mail des utilisateurs que vous souhaitez placer en attente et une requête de recherche à utiliser si vous souhaitez créer une mise en attente basée sur une https://contoso-my.sharepoint.com) requête.</span><span class="sxs-lookup"><span data-stu-id="6cba9-109">The script prompts you for the name of your organization's My Site domain (for example, `contoso` in the URL https://contoso-my.sharepoint.com), the name of an existing eDiscovery case, the name of the new hold that associated with the case, a list of email addresses of the users you want to put on hold, and a search query to use if you want to create a query-based hold.</span></span> <span data-ttu-id="6cba9-110">Le script obtient ensuite l’URL du site OneDrive Entreprise pour chaque utilisateur de la liste, crée la nouvelle attente, puis ajoute la boîte aux lettres et le site OneDrive Entreprise pour chaque utilisateur de la liste à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6cba9-110">The script then gets the URL for the OneDrive for Business site for each user in the list, creates the new hold, and then adds the mailbox and OneDrive for Business site for each user in the list to the hold.</span></span> <span data-ttu-id="6cba9-111">Le script génère également des fichiers journaux qui contiennent des informations sur la nouvelle archive.</span><span class="sxs-lookup"><span data-stu-id="6cba9-111">The script also generates log files that contain information about the new hold.</span></span>
  
<span data-ttu-id="6cba9-112">Voici les étapes à suivre pour y arriver :</span><span class="sxs-lookup"><span data-stu-id="6cba9-112">Here are the steps to make this happen:</span></span>
  
[<span data-ttu-id="6cba9-113">Étape 1 : installer SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="6cba9-113">Step 1: Install the SharePoint Online Management Shell</span></span>](#step-1-install-the-sharepoint-online-management-shell)
  
[<span data-ttu-id="6cba9-114">Étape 2 : Générer une liste d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6cba9-114">Step 2: Generate a list of users</span></span>](#step-2-generate-a-list-of-users)
  
[<span data-ttu-id="6cba9-115">Étape 3 : Exécuter le script pour créer une attente et ajouter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6cba9-115">Step 3: Run the script to create a hold and add users</span></span>](#step-3-run-the-script-to-create-a-hold-and-add-users)
  
## <a name="before-you-add-users-to-a-hold"></a><span data-ttu-id="6cba9-116">Avant d’ajouter des utilisateurs à une attente</span><span class="sxs-lookup"><span data-stu-id="6cba9-116">Before you add users to a hold</span></span>

- <span data-ttu-id="6cba9-117">Vous devez être membre du groupe de rôles Gestionnaire eDiscovery dans le Centre de sécurité & conformité et administrateur SharePoint Online pour exécuter le script à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="6cba9-117">You have to be a member of the eDiscovery Manager role group in the Security & Compliance Center and a SharePoint Online administrator to run the script in Step 3.</span></span> <span data-ttu-id="6cba9-118">Pour plus d’informations, voir [Attribuer des autorisations eDiscovery](assign-ediscovery-permissions.md)dans le Centre de sécurité & conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="6cba9-118">For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security & Compliance Center](assign-ediscovery-permissions.md).</span></span>

- <span data-ttu-id="6cba9-119">Un maximum de 1 000 boîtes aux lettres et 100 sites peuvent être ajoutés à une mise en attente associée à un cas eDiscovery dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="6cba9-119">A maximum of 1,000 mailboxes and 100 sites can be added to a hold that's associated with an eDiscovery case in the Security & Compliance Center.</span></span> <span data-ttu-id="6cba9-120">En supposant que chaque utilisateur que vous souhaitez placer en attente possède un site OneDrive Entreprise, vous pouvez ajouter un maximum de 100 utilisateurs à une attente à l’aide du script de cet article.</span><span class="sxs-lookup"><span data-stu-id="6cba9-120">Assuming that every user that you want to place on hold has a OneDrive for Business site, you can add a maximum of 100 users to a hold using the script in this article.</span></span>

- <span data-ttu-id="6cba9-121">N’oubliez pas d’enregistrer la liste des utilisateurs que vous créez à l’étape 2 et le script de l’étape 3 dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="6cba9-121">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder.</span></span> <span data-ttu-id="6cba9-122">Cela facilitera l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="6cba9-122">That will make it easier to run the script.</span></span>

- <span data-ttu-id="6cba9-123">Le script ajoute la liste des utilisateurs à une nouvelle attente associée à un cas existant.</span><span class="sxs-lookup"><span data-stu-id="6cba9-123">The script adds the list of users to a new hold that is associated with an existing case.</span></span> <span data-ttu-id="6cba9-124">Assurez-vous que le cas avec qui vous souhaitez associer la attente est créé avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="6cba9-124">Be sure the case that you want to associate the hold with is created before you run the script.</span></span>

- <span data-ttu-id="6cba9-125">Le script de cet article prend en charge l’authentification moderne lors de la connexion au Centre de sécurité & conformité PowerShell et SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="6cba9-125">The script in this article supports modern authentication when connecting to Security & Compliance Center PowerShell and SharePoint Online Management Shell.</span></span> <span data-ttu-id="6cba9-126">Vous pouvez utiliser le script tel qu’il est si vous êtes une organisation Microsoft 365 ou Microsoft 365 GCC.</span><span class="sxs-lookup"><span data-stu-id="6cba9-126">You can use the script as-is if you are a Microsoft 365 or a Microsoft 365 GCC organization.</span></span> <span data-ttu-id="6cba9-127">Si vous êtes une organisation Office 365 Germany, une organisation Microsoft 365 GCC High ou une organisation Microsoft 365 DoD, vous devez modifier le script pour l’exécuter correctement.</span><span class="sxs-lookup"><span data-stu-id="6cba9-127">If you are an Office 365 Germany organization, a Microsoft 365 GCC High organization, or a Microsoft 365 DoD organization, you will have to edit the script to successfully run it.</span></span> <span data-ttu-id="6cba9-128">Plus précisément, vous devez modifier la ligne et utiliser les `Connect-IPPSSession` paramètres *ConnectionUri* et *AzureADAuthorizationEndpointUri* (et les valeurs appropriées pour le type de votre organisation) pour vous connecter au Centre de sécurité & conformité PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6cba9-128">Specifically, you have to edit the line `Connect-IPPSSession` and use the *ConnectionUri* and *AzureADAuthorizationEndpointUri* parameters (and the appropriate values for your organization type) to connect to Security & Compliance Center PowerShell.</span></span> <span data-ttu-id="6cba9-129">Pour plus d’informations, consultez les exemples du Centre de [sécurité & conformité PowerShell.](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell#connect-to-security--compliance-center-powershell-without-using-mfa)</span><span class="sxs-lookup"><span data-stu-id="6cba9-129">For more information, see the examples in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell#connect-to-security--compliance-center-powershell-without-using-mfa).</span></span>

- <span data-ttu-id="6cba9-130">Le script se déconnecte automatiquement du Centre de sécurité & conformité PowerShell et SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="6cba9-130">The script automatically disconnects from Security & Compliance Center PowerShell and SharePoint Online Management Shell.</span></span>

- <span data-ttu-id="6cba9-131">Le script inclut une gestion minimale des erreurs.</span><span class="sxs-lookup"><span data-stu-id="6cba9-131">The script includes minimal error handling.</span></span> <span data-ttu-id="6cba9-132">Son objectif principal est de placer rapidement et facilement la boîte aux lettres et le site OneDrive Entreprise de chaque utilisateur en attente.</span><span class="sxs-lookup"><span data-stu-id="6cba9-132">Its primary purpose is to quickly and easily place the mailbox and OneDrive for Business site of each user on hold.</span></span>

- <span data-ttu-id="6cba9-p109">Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="6cba9-p109">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>

## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="6cba9-138">Étape 1 : installer SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="6cba9-138">Step 1: Install the SharePoint Online Management Shell</span></span>

<span data-ttu-id="6cba9-139">La première étape consiste à installer SharePoint Online Management Shell s’il n’est pas déjà installé sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="6cba9-139">The first step is to install the SharePoint Online Management Shell if it's not already installed on your local computer.</span></span> <span data-ttu-id="6cba9-140">Vous n’avez pas besoin d’utiliser l’shell dans cette procédure, mais vous devez l’installer car il contient les conditions préalables requises par le script que vous exécutez à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="6cba9-140">You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3.</span></span> <span data-ttu-id="6cba9-141">Ces conditions préalables permettent au script de communiquer avec SharePoint Online pour obtenir les URL des sites OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="6cba9-141">These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="6cba9-142">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell on your local computer.</span><span class="sxs-lookup"><span data-stu-id="6cba9-142">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell on your local computer.</span></span>

## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="6cba9-143">Étape 2 : Générer une liste d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6cba9-143">Step 2: Generate a list of users</span></span>

<span data-ttu-id="6cba9-144">Le script de l’étape 3 crée une attente associée à un cas eDiscovery et ajoute les boîtes aux lettres et les sites OneDrive Entreprise d’une liste d’utilisateurs à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6cba9-144">The script in Step 3 will create a hold that's associated with an eDiscovery case, and the add the mailboxes and OneDrive for Business sites of a list of users to the hold.</span></span> <span data-ttu-id="6cba9-145">Vous pouvez simplement taper les adresses de messagerie dans un fichier texte ou exécuter une commande dans Windows PowerShell pour obtenir une liste d’adresses e-mail et les enregistrer dans un fichier (situé dans le dossier où vous enregistrerez le script à l’étape 3).</span><span class="sxs-lookup"><span data-stu-id="6cba9-145">You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="6cba9-146">Voici une commande PowerShell (que vous exécutez à l’aide de PowerShell distant connecté à votre organisation Exchange Online) pour obtenir la liste des adresses de messagerie de tous les utilisateurs de votre organisation et l’enregistrer dans un fichier texte nommé HoldUsers.txt.</span><span class="sxs-lookup"><span data-stu-id="6cba9-146">Here's a PowerShell command (that you run by using remote PowerShell connected to your Exchange Online organization) to get a list of email addresses for all users in your organization and save it to a text file named HoldUsers.txt.</span></span>
  
```powershell
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

<span data-ttu-id="6cba9-147">Après avoir exécuté cette commande, ouvrez le fichier texte et supprimez l’en-tête qui contient le nom de la  `PrimarySmtpAddress` propriété.</span><span class="sxs-lookup"><span data-stu-id="6cba9-147">After you run this command, open the text file and remove the header that contains the property name,  `PrimarySmtpAddress`.</span></span> <span data-ttu-id="6cba9-148">Ensuite, supprimez toutes les adresses de messagerie à l’exception de celle des utilisateurs que vous souhaitez ajouter à la attente que vous allez créer à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="6cba9-148">Then remove all email addresses except the ones for the users that you want to add to the hold that you'll create in Step 3.</span></span> <span data-ttu-id="6cba9-149">Assurez-vous qu’il n’existe aucune ligne vide avant ou après la liste des adresses e-mail.</span><span class="sxs-lookup"><span data-stu-id="6cba9-149">Make sure there are no blank rows before or after the list of email addresses.</span></span>
  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a><span data-ttu-id="6cba9-150">Étape 3 : Exécuter le script pour créer une attente et ajouter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6cba9-150">Step 3: Run the script to create a hold and add users</span></span>

<span data-ttu-id="6cba9-151">Lorsque vous exécutez le script dans cette étape, il vous invite à fournir les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="6cba9-151">When you run the script in this step, it will prompt you for the following information.</span></span> <span data-ttu-id="6cba9-152">Veillez à ce que ces informations soient prêtes avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="6cba9-152">Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="6cba9-153">**Vos informations d’identification d’utilisateur :** Le script utilise vos informations d’identification pour se connecter au Centre de sécurité & conformité avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6cba9-153">**Your user credentials:** The script will use your credentials to connect to Security & Compliance Center with PowerShell.</span></span> <span data-ttu-id="6cba9-154">Il utilisera également ces informations d’identification pour accéder à SharePoint Online afin d’obtenir les URL OneDrive Entreprise pour la liste des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6cba9-154">It will also use these credentials to access SharePoint Online to get the OneDrive for Business URLs for the list of users.</span></span>

- <span data-ttu-id="6cba9-155">**Nom de votre domaine SharePoint :** Le script vous invite à entrer ce nom afin qu’il puisse se connecter au Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6cba9-155">**Name of your SharePoint domain:** The script prompts you to enter this name so it can connect to the SharePoint admin center.</span></span> <span data-ttu-id="6cba9-156">Il utilise également le nom de domaine pour les URL OneDrive de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6cba9-156">It also uses the domain name for the OneDrive URLs in your organization.</span></span> <span data-ttu-id="6cba9-157">Par exemple, si l’URL de votre centre d’administration est et l’URL de OneDrive est , vous devez entrer lorsque le script vous invite à entrer `https://contoso-admin.sharepoint.com` `https://contoso-my.sharepoint.com` votre nom de `contoso` domaine.</span><span class="sxs-lookup"><span data-stu-id="6cba9-157">For example, if the URL for your admin center is `https://contoso-admin.sharepoint.com` and the URL for OneDrive is `https://contoso-my.sharepoint.com`, then you would enter `contoso` when the script prompts you for your domain name.</span></span>

- <span data-ttu-id="6cba9-158">**Nom du cas :** Nom d’un cas existant.</span><span class="sxs-lookup"><span data-stu-id="6cba9-158">**Name of the case:** The name of an existing case.</span></span> <span data-ttu-id="6cba9-159">Le script crée une nouvelle attente associée à ce cas.</span><span class="sxs-lookup"><span data-stu-id="6cba9-159">The script will create a new hold that is associated with this case.</span></span>

- <span data-ttu-id="6cba9-160">**Nom de la attente :** Nom de la attente que le script créera et associera au cas spécifié.</span><span class="sxs-lookup"><span data-stu-id="6cba9-160">**Name of the hold:** The name of the hold the script will create and associate with the specified case.</span></span>

- <span data-ttu-id="6cba9-161">**Requête de recherche pour une attente basée sur une requête :** Vous pouvez créer une mise en attente basée sur une requête afin que seul le contenu qui répond aux critères de recherche spécifiés soit mis en attente.</span><span class="sxs-lookup"><span data-stu-id="6cba9-161">**Search query for a query-based hold:** You can create a query-based hold so that only the content that meets the specified search criteria is placed on hold.</span></span> <span data-ttu-id="6cba9-162">Pour placer tout le contenu en attente, appuyez simplement sur **Entrée** lorsque vous êtes invité à effectuer une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="6cba9-162">To place all content on hold, just press **Enter** when you're prompted for a search query.</span></span>

- <span data-ttu-id="6cba9-163">**En 2013, vous tenez ou non en attente :** Le script peut être mis en attente après sa création ou le script peut créer la mise en attente sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="6cba9-163">**Turning on the hold or not:** You can have the script turn on the hold after it's created or you can have the script create the hold without enabling it.</span></span> <span data-ttu-id="6cba9-164">Si le script n’est pas en attente, vous pouvez l’activer ultérieurement dans le Centre de sécurité et conformité & ou en exécutant les commandes PowerShell suivantes :</span><span class="sxs-lookup"><span data-stu-id="6cba9-164">If you don't have the script turn on the hold, you can turn it on later in the Security & Compliance Center or by running the following PowerShell commands:</span></span>

  ```powershell
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```powershell
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- <span data-ttu-id="6cba9-165">**Nom du fichier texte avec** la liste des utilisateurs : nom du fichier texte de l’étape 2 qui contient la liste des utilisateurs à ajouter à la attente.</span><span class="sxs-lookup"><span data-stu-id="6cba9-165">**Name of the text file with the list of users** - The name of the text file from Step 2 that contains the list of users to add to the hold.</span></span> <span data-ttu-id="6cba9-166">Si ce fichier se trouve dans le même dossier que le script, tapez simplement le nom du fichier (par exemple, HoldUsers.txt).</span><span class="sxs-lookup"><span data-stu-id="6cba9-166">If this file is located in the same folder as the script, just type the name of the file (for example, HoldUsers.txt).</span></span> <span data-ttu-id="6cba9-167">Si le fichier texte se trouve dans un autre dossier, tapez le chemin d’accès complet du fichier.</span><span class="sxs-lookup"><span data-stu-id="6cba9-167">If the text file is in another folder, type the full pathname of the file.</span></span>

<span data-ttu-id="6cba9-168">Une fois que vous avez collecté les informations que le script vous invitera, l’étape finale consiste à exécuter le script pour créer la nouvelle attente et y ajouter des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6cba9-168">After you've collected the information that the script will prompt you for, the final step is to run the script to create the new hold and add users to it.</span></span>
  
1. <span data-ttu-id="6cba9-169">Enregistrez le texte suivant dans un fichier Windows PowerShell script à l’aide d’un suffixe de nom de fichier de `.ps1` .</span><span class="sxs-lookup"><span data-stu-id="6cba9-169">Save the following text to a Windows PowerShell script file by using a filename suffix of `.ps1`.</span></span> <span data-ttu-id="6cba9-170">Par exemple, `AddUsersToHold.ps1`.</span><span class="sxs-lookup"><span data-stu-id="6cba9-170">For example, `AddUsersToHold.ps1`.</span></span>

```powershell
#script begin
" "
write-host "***********************************************"
write-host "   Security & Compliance Center PowerShell  " -foregroundColor yellow -backgroundcolor darkgreen
write-host "   Core eDiscovery cases - Add users to a hold   " -foregroundColor yellow -backgroundcolor darkgreen 
write-host "***********************************************"
" "
# Connect to SCC PowerShell using modern authentication
if (!$SccSession)
{
  Import-Module ExchangeOnlineManagement
  Connect-IPPSSession
}

# Get the organization's domain name. We use this to create the SharePoint admin URL and root URL for OneDrive for Business.
""
$mySiteDomain = Read-Host "Enter the domain name for your SharePoint organization. We use this name to connect to SharePoint admin center and for the OneDrive URLs in your organization. For example, 'contoso' in 'https://contoso-admin.sharepoint.com' and 'https://contoso-my.sharepoint.com'"
""

# Connect to PnP Online using modern authentication
Import-Module PnP.PowerShell
Connect-PnPOnline -Url https://$mySiteDomain-admin.sharepoint.com -UseWebLogin

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
#Find user's OneDrive account URL using email address
Write-Host "Getting the URL for each user's OneDrive for Business site." -foregroundColor Yellow 
""
$AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
$mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
$urls = @()
foreach($emailAddress in $emailAddresses)
{
try
{
$url=Get-PnPUserProfileProperty -Account $emailAddress | Select PersonalUrl
$urls += $url.PersonalUrl
       Write-Host "- $emailAddress => $url"
       [array]$ODadded += $url.PersonalUrl
       }catch { 
 Write-Warning "Could not locate OneDrive for $emailAddress"
 [array]$ODExluded += $emailAddress
 Continue }
}
$urls | FL
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
#Disconnect from SCC PowerShell and PnPOnline

Write-host "Disconnecting from SCC PowerShell and PnP Online" -foregroundColor Yellow
Get-PSSession | Remove-PSSession
Disconnect-PnPOnline

Write-host "Script complete!" -foregroundColor Yellow
""
#script end
```

2. <span data-ttu-id="6cba9-171">Sur votre ordinateur local, ouvrez Windows PowerShell et allez dans le dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="6cba9-171">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>

3. <span data-ttu-id="6cba9-172">Exécutez le script . par exemple :</span><span class="sxs-lookup"><span data-stu-id="6cba9-172">Run the script; for example:</span></span>

   ```powershell
   .\AddUsersToHold.ps1
   ```

4. <span data-ttu-id="6cba9-173">Entrez les informations que vous invite le script.</span><span class="sxs-lookup"><span data-stu-id="6cba9-173">Enter the information that the script prompts you for.</span></span>

   <span data-ttu-id="6cba9-174">Le script se connecte au Centre de sécurité & conformité PowerShell, puis crée la nouvelle mise en attente dans le cas eDiscovery et ajoute les boîtes aux lettres et OneDrive Entreprise pour les utilisateurs dans la liste.</span><span class="sxs-lookup"><span data-stu-id="6cba9-174">The script connects to Security & Compliance Center PowerShell, and then creates the new hold in the eDiscovery case and adds the mailboxes and OneDrive for Business for the users in the list.</span></span> <span data-ttu-id="6cba9-175">Vous pouvez consulter le cas sur la page **eDiscovery** dans le Centre de sécurité & conformité pour afficher la nouvelle mise en attente.</span><span class="sxs-lookup"><span data-stu-id="6cba9-175">You can go to the case on the **eDiscovery** page in the Security & Compliance Center to view the new hold.</span></span>

<span data-ttu-id="6cba9-176">Une fois l’exécution du script terminée, il crée les fichiers journaux suivants et les enregistre dans le dossier où se trouve le script.</span><span class="sxs-lookup"><span data-stu-id="6cba9-176">After the script is finished running, it creates the following log files, and saves them to the folder where the script is located.</span></span>
  
- <span data-ttu-id="6cba9-177">**LocationsOnHold.txt :** Contient la liste des boîtes aux lettres et des sites OneDrive Entreprise que le script a correctement placés en attente.</span><span class="sxs-lookup"><span data-stu-id="6cba9-177">**LocationsOnHold.txt:** Contains a list of mailboxes and OneDrive for Business sites that the script successfully placed on hold.</span></span>

- <span data-ttu-id="6cba9-178">**LocationsNotOnHold.txt :** Contient une liste de boîtes aux lettres et de sites OneDrive Entreprise que le script n’a pas placer en attente.</span><span class="sxs-lookup"><span data-stu-id="6cba9-178">**LocationsNotOnHold.txt:** Contains a list of mailboxes and OneDrive for Business sites that the script did not place on hold.</span></span> <span data-ttu-id="6cba9-179">Si un utilisateur dispose d’une boîte aux lettres, mais pas d’un site OneDrive Entreprise, il est inclus dans la liste des sites OneDrive Entreprise qui n’ont pas été mis en attente.</span><span class="sxs-lookup"><span data-stu-id="6cba9-179">If a user has a mailbox, but not a OneDrive for Business site, the user would be included in the list of OneDrive for Business sites that weren't placed on hold.</span></span>

- <span data-ttu-id="6cba9-180">**GetCaseHoldPolicy.txt :** Contient la sortie de la cmdlet **Get-CaseHoldPolicy** pour la nouvelle mise en attente, que le script a mise en place après la création de la nouvelle mise en attente.</span><span class="sxs-lookup"><span data-stu-id="6cba9-180">**GetCaseHoldPolicy.txt:** Contains the output of the **Get-CaseHoldPolicy** cmdlet for the new hold, which the script ran after creating the new hold.</span></span> <span data-ttu-id="6cba9-181">Les informations renvoyées par cette cmdlet incluent une liste des utilisateurs dont les boîtes aux lettres et les sites OneDrive Entreprise ont été mis en attente et si la mise en attente est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="6cba9-181">The information returned by this cmdlet includes a list of users whose mailboxes and OneDrive for Business sites were placed on hold and whether the hold is enabled or disabled.</span></span> 

- <span data-ttu-id="6cba9-182">**GetCaseHoldRule.txt :** Contient la sortie de la cmdlet **Get-CaseHoldRule** pour la nouvelle mise en attente, que le script a mise en place après la création de la nouvelle mise en attente.</span><span class="sxs-lookup"><span data-stu-id="6cba9-182">**GetCaseHoldRule.txt:** Contains the output of the **Get-CaseHoldRule** cmdlet for the new hold, which the script ran after creating the new hold.</span></span> <span data-ttu-id="6cba9-183">Les informations renvoyées par cette cmdlet incluent la requête de recherche si vous avez utilisé le script pour créer une attente basée sur une requête.</span><span class="sxs-lookup"><span data-stu-id="6cba9-183">The information returned by this cmdlet includes the search query if you used the script to create a query-based hold.</span></span>
