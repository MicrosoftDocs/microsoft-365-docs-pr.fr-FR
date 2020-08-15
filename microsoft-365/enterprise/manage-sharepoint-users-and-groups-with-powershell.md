---
title: Gestion des utilisateurs et des groupes SharePoint Online avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/17/2020
audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- PowerShell
- Ent_Office_Other
- SPO_Content
- seo-marvel-apr2020
ms.assetid: d0d3877a-831f-4744-96b0-d8167f06cca2
description: Dans cet article, Découvrez comment utiliser PowerShell pour Microsoft 365 pour gérer les utilisateurs, les groupes et les sites SharePoint Online.
ms.openlocfilehash: 5252ecc950e5f26d6ad60cd871910a67bf50f187
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690073"
---
# <a name="manage-sharepoint-online-users-and-groups-with-powershell"></a><span data-ttu-id="2f366-103">Gestion des utilisateurs et des groupes SharePoint Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f366-103">Manage SharePoint Online users and groups with PowerShell</span></span>

<span data-ttu-id="2f366-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="2f366-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="2f366-105">Si vous êtes un administrateur SharePoint Online qui travaille avec de grandes listes de comptes ou de groupes d’utilisateurs et qu’il souhaite un moyen plus facile de les gérer, vous pouvez utiliser PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2f366-105">If you are a SharePoint Online administrator who works with large lists of user accounts or groups and wants an easier way to manage them, you can use PowerShell for Microsoft 365.</span></span> 

<span data-ttu-id="2f366-106">Avant de commencer, les procédures décrites dans cette rubrique nécessitent que vous vous connectiez à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="2f366-106">Before you begin, the procedures in this topic require you to connect to SharePoint Online.</span></span> <span data-ttu-id="2f366-107">Pour obtenir des instructions, consultez la rubrique [connexion à SharePoint Online PowerShell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)</span><span class="sxs-lookup"><span data-stu-id="2f366-107">For instructions, see [Connect to SharePoint Online PowerShell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)</span></span>

## <a name="get-a-list-of-sites-groups-and-users"></a><span data-ttu-id="2f366-108">Obtenir une liste de sites, de groupes et d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2f366-108">Get a list of sites, groups, and users</span></span>

<span data-ttu-id="2f366-p102">Avant de commencer à gérer les utilisateurs et les groupes, vous devez obtenir les listes de vos sites, groupes et utilisateurs. Vous pouvez ensuite utiliser ces informations pour travailler à partir de l’exemple figurant dans cet article.</span><span class="sxs-lookup"><span data-stu-id="2f366-p102">Before we start to manage users and groups, you need to get lists of your sites, groups, and users. You can then use this information to work through the example in this article.</span></span>

<span data-ttu-id="2f366-111">Vous pouvez obtenir la liste des sites de votre client avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2f366-111">Get a list of the sites in your tenant with this command:</span></span>

```powershell
Get-SPOSite
```

<span data-ttu-id="2f366-112">Vous pouvez obtenir la liste des groupes de votre client avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2f366-112">Get a list of the groups in your tenant with this command:</span></span>

```powershell
Get-SPOSite | ForEach {Get-SPOSiteGroup -Site $_.Url} | Format-Table
```

<span data-ttu-id="2f366-113">Vous pouvez obtenir la liste des utilisateurs de votre client avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2f366-113">Get a list of the users in your tenant with this command:</span></span>

```powershell
Get-SPOSite | ForEach {Get-SPOUser -Site $_.Url}
```

## <a name="add-a-user-to-the-site-collection-administrators-group"></a><span data-ttu-id="2f366-114">Ajouter un utilisateur au groupe Administrateurs de collection de sites</span><span class="sxs-lookup"><span data-stu-id="2f366-114">Add a user to the Site Collection Administrators group</span></span>

<span data-ttu-id="2f366-115">Utilisez l’applet de commande `Set-SPOUser` pour ajouter un utilisateur à la liste des administrateurs de collection de sites sur une collection de sites.</span><span class="sxs-lookup"><span data-stu-id="2f366-115">You use the `Set-SPOUser` cmdlet to add a user to the list of Site Collection Administrators on a site collection.</span></span>

```powershell
$tenant = "<tenant name, such as litwareinc for litwareinc.com>"
$site = "<site name>"
$user = "<user account name, such as opalc>"
Set-SPOUser -Site https://$tenant.sharepoint.com/sites/$site -LoginName $user@$tenant.com -IsSiteCollectionAdmin $true
 ```

<span data-ttu-id="2f366-116">Pour utiliser ces commandes, remplacez tous les éléments entre guillemets, y compris les caractères < et >, par les noms corrects.</span><span class="sxs-lookup"><span data-stu-id="2f366-116">To use these commands, replace everything within the quotes, including the < and > characters, with the correct names.</span></span>

<span data-ttu-id="2f366-117">Par exemple, cet ensemble de commandes ajoute Opal Castillo (nom d’utilisateur opalc) à la liste des administrateurs de collection de sites sur la collection de sites ContosoTest dans la location contoso :</span><span class="sxs-lookup"><span data-stu-id="2f366-117">For example, this set of commands adds Opal Castillo (user name opalc) to the list of Site Collection Administrators on the ContosoTest site collection in the Contoso tenancy:</span></span>

```powershell
$tenant = "contoso"
$site = "contosotest"
$user = "opalc"
Set-SPOUser -Site https://$tenant.sharepoint.com/sites/$site -LoginName $user@$tenant.com -IsSiteCollectionAdmin $true
```

<span data-ttu-id="2f366-118">Vous pouvez copier et coller ces commandes dans le bloc-notes, modifier les valeurs des variables des $tenant, $site et $user en valeurs réelles à partir de votre environnement, puis collez-les dans votre fenêtre SharePoint Online Management Shell pour les exécuter.</span><span class="sxs-lookup"><span data-stu-id="2f366-118">You can copy and paste these commands into Notepad, change the variable values for $tenant, $site, and $user to actual values from your environment, and then paste this into your SharePoint Online Management Shell window to run them.</span></span>

## <a name="add-a-user-to-other-site-collection-groups"></a><span data-ttu-id="2f366-119">Ajouter un utilisateur à d’autres groupes de collection de sites</span><span class="sxs-lookup"><span data-stu-id="2f366-119">Add a user to other site collection groups</span></span>

<span data-ttu-id="2f366-120">Dans cette tâche, nous allons utiliser l' `Add-SPOUser` applet de commande pour ajouter un utilisateur à un groupe SharePoint sur une collection de sites.</span><span class="sxs-lookup"><span data-stu-id="2f366-120">In this task, we'll use the `Add-SPOUser` cmdlet to add a user to a SharePoint group on a site collection.</span></span>

```powershell
$tenant = "<tenant name, such as litwareinc for litwareinc.com>"
$site = "<site name>"
$user = "<user account name, such as opalc>"
$group = "<group name name, such as Auditors>"
Add-SPOUser -Group $group -LoginName $user@$tenant.com -Site https://$tenant.sharepoint.com/sites/$site

```

<span data-ttu-id="2f366-121">Par exemple, nous allons ajouter Glen Rife (nom d’utilisateur glenr) au groupe auditeurs sur la collection de sites ContosoTest dans la location contoso :</span><span class="sxs-lookup"><span data-stu-id="2f366-121">For example, let's add Glen Rife (user name glenr) to the Auditors group on the ContosoTest site collection in the contoso tenancy:</span></span>

```powershell
$tenant = "contoso"
$site = "contosotest"
$user = "glenr"
$group = "Auditors"
Add-SPOUser -Group $group -LoginName $user@$tenant.com -Site https://$tenant.sharepoint.com/sites/$site
```

## <a name="create-a-site-collection-group"></a><span data-ttu-id="2f366-122">Créer un groupe de collections de sites</span><span class="sxs-lookup"><span data-stu-id="2f366-122">Create a site collection group</span></span>

<span data-ttu-id="2f366-123">Utilisez l' `New-SPOSiteGroup` applet de commande pour créer un groupe SharePoint et l’ajouter à une collection de sites.</span><span class="sxs-lookup"><span data-stu-id="2f366-123">You use the `New-SPOSiteGroup` cmdlet to create a new SharePoint group and add it to a site collection.</span></span>

```powershell
$tenant = "<tenant name, such as litwareinc for litwareinc.com>"
$site = "<site name>"
$group = "<group name name, such as Auditors>"
$level = "<permission level, such as View Only>"
New-SPOSiteGroup -Group $group -PermissionLevels $level -Site https://$tenant.sharepoint.com/sites/$site
```
<span data-ttu-id="2f366-124">Les propriétés de groupe, telles que les niveaux d’autorisation, peuvent être mises à jour ultérieurement à l’aide de l’applet de commande `Set-SPOSiteGroup` .</span><span class="sxs-lookup"><span data-stu-id="2f366-124">Group properties, such as permission levels, can be updated later by using the `Set-SPOSiteGroup` cmdlet.</span></span>

<span data-ttu-id="2f366-125">Par exemple, nous allons ajouter le groupe auditeurs avec des autorisations d’affichage seul à la collection de sites ContosoTest dans la location contoso :</span><span class="sxs-lookup"><span data-stu-id="2f366-125">For example, let's add the Auditors group with View Only permissions to the contosotest site collection in the contoso tenancy:</span></span>

```powershell
$tenant = "contoso"
$site = "contosotest"
$group = "Auditors"
$level = "View Only"
New-SPOSiteGroup -Group $group -PermissionLevels $level -Site https://$tenant.sharepoint.com/sites/$site
```

## <a name="remove-users-from-a-group"></a><span data-ttu-id="2f366-126">Supprimer des utilisateurs d’un groupe</span><span class="sxs-lookup"><span data-stu-id="2f366-126">Remove users from a group</span></span>

<span data-ttu-id="2f366-p103">Parfois, vous devez supprimer un utilisateur d’un site ou même de tous les sites, par exemple, si l’employé change de service ou quitte l’entreprise. Vous pouvez réaliser cette action facilement dans l’interface utilisateur pour un seul employé, mais déplacer un service complet d’un site à un autre est autrement plus compliqué.</span><span class="sxs-lookup"><span data-stu-id="2f366-p103">Sometimes you have to remove a user from a site or even all sites. Perhaps the employee moves from one division to another or leaves the company. You can do this for one employee easily in the UI, but this is not easily done when you have to move a complete division from one site to another.</span></span>

<span data-ttu-id="2f366-130">Cependant, à l’aide de SharePoint Online Management Shell et des fichiers CSV, cette opération est rapide et facile.</span><span class="sxs-lookup"><span data-stu-id="2f366-130">However by using the SharePoint Online Management Shell and CSV files, this is fast and easy.</span></span> <span data-ttu-id="2f366-131">Dans cette tâche, vous allez utiliser Windows PowerShell pour supprimer un utilisateur d’un groupe de sécurité de collection de sites.</span><span class="sxs-lookup"><span data-stu-id="2f366-131">In this task, you'll use Windows PowerShell to remove a user from a site collection security group.</span></span> <span data-ttu-id="2f366-132">Vous utiliserez ensuite un fichier CSV et supprimerez de nombreux utilisateurs de différents sites.</span><span class="sxs-lookup"><span data-stu-id="2f366-132">Then you'll use a CSV file and remove lots of users from different sites.</span></span> 

<span data-ttu-id="2f366-133">Nous allons utiliser la cmdlet « Remove-époux » pour supprimer un seul utilisateur de Microsoft 365 d’un groupe de collection de sites pour pouvoir voir la syntaxe de la commande.</span><span class="sxs-lookup"><span data-stu-id="2f366-133">We'll be using the 'Remove-SPOUser' cmdlet to remove a single Microsoft 365 user from a site collection group just so we can see the command syntax.</span></span> <span data-ttu-id="2f366-134">Voici à quoi ressemble la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="2f366-134">Here is how the syntax looks:</span></span>

```powershell
$tenant = "<tenant name, such as litwareinc for litwareinc.com>"
$site = "<site name>"
$user = "<user account name, such as opalc>"
$group = "<group name name, such as Auditors>"
Remove-SPOUser -LoginName $user@$tenant.com -Site https://$tenant.sharepoint.com/sites/$site -Group $group
```
<span data-ttu-id="2f366-135">Par exemple, nous allons supprimer Bobby Overby du groupe des auditeurs de collection de sites dans la collection de sites ContosoTest dans la location contoso :</span><span class="sxs-lookup"><span data-stu-id="2f366-135">For example, let's remove Bobby Overby from the site collection Auditors group in the contosotest site collection in the contoso tenancy:</span></span>

```powershell
$tenant = "contoso"
$site = "contosotest"
$user = "bobbyo"
$group = "Auditors"
Remove-SPOUser -LoginName $user@$tenant.com -Site https://$tenant.sharepoint.com/sites/$site -Group $group
```

<span data-ttu-id="2f366-136">Supposons que nous voulions supprimer Bobby de tous les groupes auxquels il appartient actuellement.</span><span class="sxs-lookup"><span data-stu-id="2f366-136">Suppose we wanted to remove Bobby from all the groups he is currently in.</span></span> <span data-ttu-id="2f366-137">Voici comment procéder :</span><span class="sxs-lookup"><span data-stu-id="2f366-137">Here is how we would do that:</span></span>

```powershell
$tenant = "contoso"
$user = "bobbyo"
Get-SPOSite | ForEach {Get-SPOSiteGroup –Site $_.Url} | ForEach {Remove-SPOUser -LoginName $user@$tenant.com -Site &_.Url}
```

> [!WARNING]
> <span data-ttu-id="2f366-138">Ce n’est qu’un exemple.</span><span class="sxs-lookup"><span data-stu-id="2f366-138">This is just an example.</span></span> <span data-ttu-id="2f366-139">Vous ne devez pas exécuter cette commande sauf si vous devez vraiment supprimer un utilisateur de chaque groupe, par exemple si l’utilisateur quitte l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="2f366-139">You should not run this command unless you really have to remove a user from every group, for example if the user leaves the company.</span></span>

## <a name="automate-management-of-large-lists-of-users-and-groups"></a><span data-ttu-id="2f366-140">Automatiser la gestion des grandes listes d’utilisateurs et de groupes</span><span class="sxs-lookup"><span data-stu-id="2f366-140">Automate management of large lists of users and groups</span></span>

<span data-ttu-id="2f366-141">Pour ajouter un grand nombre de comptes aux sites SharePoint et leur donner des autorisations, vous pouvez utiliser le centre d’administration 365 de Microsoft, des commandes PowerShell individuelles ou PowerShell un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="2f366-141">To add a large number of accounts to SharePoint sites and give them permissions, you can use the Microsoft 365 admin center, individual PowerShell commands, or PowerShell an a CSV file.</span></span> <span data-ttu-id="2f366-142">Parmi tous ces choix, le fichier CSV est le moyen le plus rapide d’automatiser cette tâche.</span><span class="sxs-lookup"><span data-stu-id="2f366-142">Of these choices, the CSV file is the fastest way to automate this task.</span></span>

<span data-ttu-id="2f366-143">Le processus de base consiste à créer un fichier CSV qui possède des en-têtes (colonnes) correspondant aux paramètres dont le script Windows PowerShell a besoin.</span><span class="sxs-lookup"><span data-stu-id="2f366-143">The basic process is to create a CSV file that has headers (columns) that correspond to the parameters that the Windows PowerShell script needs.</span></span> <span data-ttu-id="2f366-144">Vous pouvez facilement créer une liste de ce type dans Excel, puis l’exporter en tant que fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="2f366-144">You can easily create such a list in Excel and then export it as a CSV file.</span></span> <span data-ttu-id="2f366-145">Ensuite, vous utilisez un script Windows PowerShell pour parcourir les enregistrements (lignes) dans le fichier CSV, en ajoutant les utilisateurs à des groupes et les groupes à des sites.</span><span class="sxs-lookup"><span data-stu-id="2f366-145">Then, you use a Windows PowerShell script to iterate through records (rows) in the CSV file, adding the users to groups and the groups to sites.</span></span> 

<span data-ttu-id="2f366-146">Par exemple, nous allons créer un fichier CSV pour définir un groupe de collections de sites, de groupes et d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="2f366-146">For example, let's create a CSV file to define a group of site collections, groups, and permissions.</span></span> <span data-ttu-id="2f366-147">Puis, nous créerons un fichier CSV pour remplir les groupes avec des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2f366-147">Next, we will create a CSV file to populate the groups with users.</span></span> <span data-ttu-id="2f366-148">Enfin, nous créerons puis exécuterons un script Windows PowerShell simple qui crée et remplit les groupes.</span><span class="sxs-lookup"><span data-stu-id="2f366-148">Finally, we will create and run a simple Windows PowerShell script that creates and populates the groups.</span></span>

<span data-ttu-id="2f366-149">Le premier fichier CSV ajoutera des groupes à des collections de sites et aura la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="2f366-149">The first CSV file will add one or more groups to one or more site collections and will have this structure:</span></span>

<span data-ttu-id="2f366-150">Tête</span><span class="sxs-lookup"><span data-stu-id="2f366-150">Header:</span></span>

```powershell
Site,Group,PermissionLevels
```

<span data-ttu-id="2f366-151">Complémentaires</span><span class="sxs-lookup"><span data-stu-id="2f366-151">Item:</span></span>

```powershell
https://tenant.sharepoint.com/sites/site,group,level
```

<span data-ttu-id="2f366-152">Voici un exemple de fichier :</span><span class="sxs-lookup"><span data-stu-id="2f366-152">Here is an example file:</span></span>

```powershell
Site,Group,PermissionLevels
https://contoso.sharepoint.com/sites/contosotest,Contoso Project Leads,Full Control
https://contoso.sharepoint.com/sites/contosotest,Contoso Auditors,View Only
https://contoso.sharepoint.com/sites/contosotest,Contoso Designers,Design
https://contoso.sharepoint.com/sites/TeamSite01,XT1000 Team Leads,Full Control
https://contoso.sharepoint.com/sites/TeamSite01,XT1000 Advisors,Edit
https://contoso.sharepoint.com/sites/Blog01,Contoso Blog Designers,Design
https://contoso.sharepoint.com/sites/Blog01,Contoso Blog Editors,Edit
https://contoso.sharepoint.com/sites/Project01,Project Alpha Approvers,Full Control
```

<span data-ttu-id="2f366-153">Le second fichier CSV ajoutera des utilisateurs à des groupes et aura la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="2f366-153">The second CSV file will add one or more users to one or more groups and will have this structure:</span></span>

<span data-ttu-id="2f366-154">Tête</span><span class="sxs-lookup"><span data-stu-id="2f366-154">Header:</span></span>

```powershell
Group,LoginName,Site
```

<span data-ttu-id="2f366-155">Complémentaires</span><span class="sxs-lookup"><span data-stu-id="2f366-155">Item:</span></span>

```powershell
group,login,https://tenant.sharepoint.com/sites/site
```

<span data-ttu-id="2f366-156">Voici un exemple de fichier :</span><span class="sxs-lookup"><span data-stu-id="2f366-156">Here is an example file:</span></span>

```powershell
Group,LoginName,Site
Contoso Project Leads,bobbyo@contoso.com,https://contoso.sharepoint.com/sites/contosotest
Contoso Auditors,allieb@contoso.com,https://contoso.sharepoint.com/sites/contosotest
Contoso Designers,bonniek@contoso.com,https://contoso.sharepoint.com/sites/contosotest
XT1000 Team Leads,dorenap@contoso.com,https://contoso.sharepoint.com/sites/TeamSite01
XT1000 Advisors,garthf@contoso.com,https://contoso.sharepoint.com/sites/TeamSite01
Contoso Blog Designers,janets@contoso.com,https://contoso.sharepoint.com/sites/Blog01
Contoso Blog Editors,opalc@contoso.com,https://contoso.sharepoint.com/sites/Blog01
Project Alpha Approvers,robinc@contoso.com,https://contoso.sharepoint.com/sites/Project01
```

<span data-ttu-id="2f366-157">Pour la prochaine étape, vous devez avoir enregistré les deux fichiers CSV sur votre lecteur.</span><span class="sxs-lookup"><span data-stu-id="2f366-157">For the next step, you must have the two CSV files saved to your drive.</span></span> <span data-ttu-id="2f366-158">Voici des exemples de commandes qui utilisent des fichiers CSV et pour ajouter des autorisations et l’appartenance à un groupe :</span><span class="sxs-lookup"><span data-stu-id="2f366-158">Here are example commands that use both CSV files and to add permissions and group membership:</span></span>

```powershell
Import-Csv C:\O365Admin\GroupsAndPermissions.csv | ForEach {New-SPOSiteGroup -Group $_.Group -PermissionLevels $_.PermissionLevels -Site $_.Site}
Import-Csv C:\O365Admin\Users.csv | ForEach {Add-SPOUser -Group $_.Group –LoginName $_.LoginName -Site $_.Site}
```

<span data-ttu-id="2f366-159">Le script importe le contenu du fichier CSV et utilise les valeurs des colonnes pour renseigner les paramètres des commandes **New-SPOSiteGroup** et **Add-époux** .</span><span class="sxs-lookup"><span data-stu-id="2f366-159">The script imports the CSV file contents and uses the values in the columns to populate the parameters of the **New-SPOSiteGroup** and **Add-SPOUser** commands.</span></span> <span data-ttu-id="2f366-160">Dans notre exemple, nous enregistrons ce fichier dans le dossier theO365Admin sur le lecteur C, mais vous pouvez l’enregistrer où vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="2f366-160">In our example, we are saving this to theO365Admin folder on drive C, but you can save it wherever you want.</span></span>

<span data-ttu-id="2f366-161">À présent, nous allons supprimer un groupe de personnes pour plusieurs groupes dans différents sites utilisant le même fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="2f366-161">Now, let's remove a bunch of people for several groups in different sites using the same CSV file.</span></span> <span data-ttu-id="2f366-162">Voici un exemple de commande :</span><span class="sxs-lookup"><span data-stu-id="2f366-162">Here is an example command:</span></span>

```powershell
Import-Csv C:\O365Admin\Users.csv | ForEach {Remove-SPOUser -LoginName $_.LoginName -Site $_.Site -Group $_.Group}
```

## <a name="generate-user-reports"></a><span data-ttu-id="2f366-163">Générer des rapports sur les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2f366-163">Generate user reports</span></span>

<span data-ttu-id="2f366-p114">Vous pouvez obtenir un rapport simple pour quelques sites et afficher les utilisateurs de ces sites, leur niveau d’autorisation, ainsi que d’autres propriétés. Voici à quoi ressemble la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="2f366-p114">You might want to get a simple report for a few sites and display the users for those sites, their permission level, and other properties. This is how the syntax looks:</span></span>

```powershell
$tenant = "<tenant name, such as litwareinc for litwareinc.com>"
$site = "<site name>"
Get-SPOUser -Site https://$tenant.sharepoint.com/sites/$site | select * | Format-table -Wrap -AutoSize | Out-File c\UsersReport.txt -Force -Width 360 -Append
```

<span data-ttu-id="2f366-166">Cela permet de collecter les données de ces trois sites et de les écrire dans un fichier texte sur votre lecteur local.</span><span class="sxs-lookup"><span data-stu-id="2f366-166">This will grab the data for these three sites and write them to a text file on your local drive.</span></span> <span data-ttu-id="2f366-167">Notez que le paramètre –Append ajoutera le nouveau contenu à un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="2f366-167">Note that the parameter –Append will add new content to an existing file.</span></span>

<span data-ttu-id="2f366-168">Par exemple, nous allons exécuter un rapport sur les sites ContosoTest, TeamSite01 et Project01 pour la location contoso1 :</span><span class="sxs-lookup"><span data-stu-id="2f366-168">For example, let's run a report on the ContosoTest, TeamSite01, and Project01 sites for the Contoso1 tenant:</span></span>

```powershell
$tenant = "contoso"
$site = "contosotest"
Get-SPOUser -Site https://$tenant.sharepoint.com/sites/$site | Format-Table -Wrap -AutoSize | Out-File c:\UsersReport.txt -Force -Width 360 -Append
$site = "TeamSite01"
Get-SPOUser -Site https://$tenant.sharepoint.com/sites/$site |Format-Table -Wrap -AutoSize | Out-File c:\UsersReport.txt -Force -Width 360 -Append
$site = "Project01"
Get-SPOUser -Site https://$tenant.sharepoint.com/sites/$site | Format-Table -Wrap -AutoSize | Out-File c:\UsersReport.txt -Force -Width 360 -Append
```

<span data-ttu-id="2f366-169">Notez que nous devions modifier uniquement la variable **$site** .</span><span class="sxs-lookup"><span data-stu-id="2f366-169">Note that we had to change only the **$site** variable.</span></span> <span data-ttu-id="2f366-170">La variable **$tenant** conserve sa valeur par le biais des trois exécutions de la commande.</span><span class="sxs-lookup"><span data-stu-id="2f366-170">The **$tenant** variable keeps its value through all three runs of the command.</span></span>

<span data-ttu-id="2f366-p117">Mais que faire si vous souhaitez effectuer cette action pour chaque site ? Vous pouvez le faire sans avoir à entrer tous ces sites web à l’aide de cette commande :</span><span class="sxs-lookup"><span data-stu-id="2f366-p117">However, what if you wanted to do this for every site? You can do this without having to type all those websites by using this command:</span></span>

```powershell
Get-SPOSite | ForEach {Get-SPOUser –Site $_.Url} | Format-Table -Wrap -AutoSize | Out-File c:\UsersReport.txt -Force -Width 360 -Append
```

<span data-ttu-id="2f366-173">Ce rapport est assez simple, et vous pouvez ajouter du code pour créer des rapports plus spécifiques ou des rapports qui contiennent des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="2f366-173">This report is fairly simple, and you can add more code to create more specific reports or reports that include more detailed information.</span></span> <span data-ttu-id="2f366-174">Mais cela doit vous donner une idée de l’utilisation de SharePoint Online Management Shell pour gérer les utilisateurs dans l’environnement SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="2f366-174">But this should give you an idea of how to use the SharePoint Online Management Shell to manage users in the SharePoint Online environment.</span></span>
   
## <a name="see-also"></a><span data-ttu-id="2f366-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f366-175">See also</span></span>

[<span data-ttu-id="2f366-176">Connexion à SharePoint Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f366-176">Connect to SharePoint Online PowerShell</span></span>](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[<span data-ttu-id="2f366-177">Gérer SharePoint Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f366-177">Manage SharePoint Online with PowerShell</span></span>](create-sharepoint-sites-and-add-users-with-powershell.md)

[<span data-ttu-id="2f366-178">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f366-178">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="2f366-179">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2f366-179">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
