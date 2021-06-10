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
description: Dans cet article, découvrez comment utiliser PowerShell pour Microsoft 365 gérer les utilisateurs, les groupes et les sites SharePoint Online.
ms.openlocfilehash: cc977355f1182b18d2f2e90b573683ed69299c1c
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50916725"
---
# <a name="manage-sharepoint-online-users-and-groups-with-powershell"></a><span data-ttu-id="baec5-103">Gestion des utilisateurs et des groupes SharePoint Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="baec5-103">Manage SharePoint Online users and groups with PowerShell</span></span>

<span data-ttu-id="baec5-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="baec5-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="baec5-105">Si vous êtes un administrateur SharePoint Online qui travaille avec de grandes listes de comptes ou de groupes d’utilisateurs et souhaitez un moyen plus facile de les gérer, vous pouvez utiliser PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="baec5-105">If you are a SharePoint Online administrator who works with large lists of user accounts or groups and wants an easier way to manage them, you can use PowerShell for Microsoft 365.</span></span> 

<span data-ttu-id="baec5-106">Avant de commencer, les procédures de cette rubrique exigent que vous vous connectiez à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="baec5-106">Before you begin, the procedures in this topic require you to connect to SharePoint Online.</span></span> <span data-ttu-id="baec5-107">Pour obtenir des instructions, [voir Connecter à SharePoint Online PowerShell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)</span><span class="sxs-lookup"><span data-stu-id="baec5-107">For instructions, see [Connect to SharePoint Online PowerShell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)</span></span>

## <a name="get-a-list-of-sites-groups-and-users"></a><span data-ttu-id="baec5-108">Obtenir une liste de sites, de groupes et d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="baec5-108">Get a list of sites, groups, and users</span></span>

<span data-ttu-id="baec5-p102">Avant de commencer à gérer les utilisateurs et les groupes, vous devez obtenir les listes de vos sites, groupes et utilisateurs. Vous pouvez ensuite utiliser ces informations pour travailler à partir de l’exemple figurant dans cet article.</span><span class="sxs-lookup"><span data-stu-id="baec5-p102">Before we start to manage users and groups, you need to get lists of your sites, groups, and users. You can then use this information to work through the example in this article.</span></span>

<span data-ttu-id="baec5-111">Vous pouvez obtenir la liste des sites de votre client avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="baec5-111">Get a list of the sites in your tenant with this command:</span></span>

```powershell
Get-SPOSite
```

<span data-ttu-id="baec5-112">Vous pouvez obtenir la liste des groupes de votre client avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="baec5-112">Get a list of the groups in your tenant with this command:</span></span>

```powershell
Get-SPOSite | ForEach {Get-SPOSiteGroup -Site $_.Url} | Format-Table
```

<span data-ttu-id="baec5-113">Vous pouvez obtenir la liste des utilisateurs de votre client avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="baec5-113">Get a list of the users in your tenant with this command:</span></span>

```powershell
Get-SPOSite | ForEach {Get-SPOUser -Site $_.Url}
```

## <a name="add-a-user-to-the-site-collection-administrators-group"></a><span data-ttu-id="baec5-114">Ajouter un utilisateur au groupe Administrateurs de collection de sites</span><span class="sxs-lookup"><span data-stu-id="baec5-114">Add a user to the Site Collection Administrators group</span></span>

<span data-ttu-id="baec5-115">La cmdlet permet d’ajouter un utilisateur à la liste des administrateurs de collection de `Set-SPOUser` sites sur une collection de sites.</span><span class="sxs-lookup"><span data-stu-id="baec5-115">You use the `Set-SPOUser` cmdlet to add a user to the list of Site Collection Administrators on a site collection.</span></span>

```powershell
$tenant = "<tenant name, such as litwareinc for litwareinc.com>"
$site = "<site name>"
$user = "<user account name, such as opalc>"
Set-SPOUser -Site https://$tenant.sharepoint.com/sites/$site -LoginName $user@$tenant.com -IsSiteCollectionAdmin $true
 ```

<span data-ttu-id="baec5-116">Pour utiliser ces commandes, remplacez tout ce qui est entre guillemets, y compris les caractères < et >, par les noms corrects.</span><span class="sxs-lookup"><span data-stu-id="baec5-116">To use these commands, replace everything within the quotes, including the < and > characters, with the correct names.</span></span>

<span data-ttu-id="baec5-117">Par exemple, cet ensemble de commandes ajoute Opal List (nom d’utilisateur opalc) à la liste des administrateurs de collection de sites sur la collection de sites ContosoTest dans la location Contoso :</span><span class="sxs-lookup"><span data-stu-id="baec5-117">For example, this set of commands adds Opal Castillo (user name opalc) to the list of Site Collection Administrators on the ContosoTest site collection in the Contoso tenancy:</span></span>

```powershell
$tenant = "contoso"
$site = "contosotest"
$user = "opalc"
Set-SPOUser -Site https://$tenant.sharepoint.com/sites/$site -LoginName $user@$tenant.com -IsSiteCollectionAdmin $true
```

<span data-ttu-id="baec5-118">Vous pouvez copier et coller ces commandes dans Bloc-notes, modifier les valeurs de variables pour $tenant, $site et $user en valeurs réelles de votre environnement, puis collez-la dans votre fenêtre SharePoint Online Management Shell pour les exécuter.</span><span class="sxs-lookup"><span data-stu-id="baec5-118">You can copy and paste these commands into Notepad, change the variable values for $tenant, $site, and $user to actual values from your environment, and then paste this into your SharePoint Online Management Shell window to run them.</span></span>

## <a name="add-a-user-to-other-site-collection-groups"></a><span data-ttu-id="baec5-119">Ajouter un utilisateur à d’autres groupes de collections de sites</span><span class="sxs-lookup"><span data-stu-id="baec5-119">Add a user to other site collection groups</span></span>

<span data-ttu-id="baec5-120">Dans cette tâche, nous allons utiliser la cmdlet pour ajouter un utilisateur à un groupe `Add-SPOUser` SharePoint sur une collection de sites.</span><span class="sxs-lookup"><span data-stu-id="baec5-120">In this task, we'll use the `Add-SPOUser` cmdlet to add a user to a SharePoint group on a site collection.</span></span>

```powershell
$tenant = "<tenant name, such as litwareinc for litwareinc.com>"
$site = "<site name>"
$user = "<user account name, such as opalc>"
$group = "<group name name, such as Auditors>"
Add-SPOUser -Group $group -LoginName $user@$tenant.com -Site https://$tenant.sharepoint.com/sites/$site

```

<span data-ttu-id="baec5-121">Par exemple, nous allons ajouter Le nom de l’utilisateur (Notamment), Ainsi, au groupe Auditeurs de la collection de sites ContosoTest dans la location contoso :</span><span class="sxs-lookup"><span data-stu-id="baec5-121">For example, let's add Glen Rife (user name glenr) to the Auditors group on the ContosoTest site collection in the contoso tenancy:</span></span>

```powershell
$tenant = "contoso"
$site = "contosotest"
$user = "glenr"
$group = "Auditors"
Add-SPOUser -Group $group -LoginName $user@$tenant.com -Site https://$tenant.sharepoint.com/sites/$site
```

## <a name="create-a-site-collection-group"></a><span data-ttu-id="baec5-122">Créer un groupe de collections de sites</span><span class="sxs-lookup"><span data-stu-id="baec5-122">Create a site collection group</span></span>

<span data-ttu-id="baec5-123">Vous utilisez `New-SPOSiteGroup` l’cmdlet pour créer un groupe SharePoint et l’ajouter à une collection de sites.</span><span class="sxs-lookup"><span data-stu-id="baec5-123">You use the `New-SPOSiteGroup` cmdlet to create a new SharePoint group and add it to a site collection.</span></span>

```powershell
$tenant = "<tenant name, such as litwareinc for litwareinc.com>"
$site = "<site name>"
$group = "<group name name, such as Auditors>"
$level = "<permission level, such as View Only>"
New-SPOSiteGroup -Group $group -PermissionLevels $level -Site https://$tenant.sharepoint.com/sites/$site
```
<span data-ttu-id="baec5-124">Les propriétés de groupe, telles que les niveaux d’autorisation, peuvent être mises à jour ultérieurement à l’aide de `Set-SPOSiteGroup` l’cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baec5-124">Group properties, such as permission levels, can be updated later by using the `Set-SPOSiteGroup` cmdlet.</span></span>

<span data-ttu-id="baec5-125">Par exemple, nous allons ajouter le groupe Auditeurs avec des autorisations Affichage seul à la collection de sites contosotest dans la location contoso :</span><span class="sxs-lookup"><span data-stu-id="baec5-125">For example, let's add the Auditors group with View Only permissions to the contosotest site collection in the contoso tenancy:</span></span>

```powershell
$tenant = "contoso"
$site = "contosotest"
$group = "Auditors"
$level = "View Only"
New-SPOSiteGroup -Group $group -PermissionLevels $level -Site https://$tenant.sharepoint.com/sites/$site
```

## <a name="remove-users-from-a-group"></a><span data-ttu-id="baec5-126">Supprimer des utilisateurs d’un groupe</span><span class="sxs-lookup"><span data-stu-id="baec5-126">Remove users from a group</span></span>

<span data-ttu-id="baec5-p103">Parfois, vous devez supprimer un utilisateur d’un site ou même de tous les sites, par exemple, si l’employé change de service ou quitte l’entreprise. Vous pouvez réaliser cette action facilement dans l’interface utilisateur pour un seul employé, mais déplacer un service complet d’un site à un autre est autrement plus compliqué.</span><span class="sxs-lookup"><span data-stu-id="baec5-p103">Sometimes you have to remove a user from a site or even all sites. Perhaps the employee moves from one division to another or leaves the company. You can do this for one employee easily in the UI, but this is not easily done when you have to move a complete division from one site to another.</span></span>

<span data-ttu-id="baec5-130">Toutefois, l’utilisation SharePoint Online Management Shell et des fichiers CSV est rapide et simple.</span><span class="sxs-lookup"><span data-stu-id="baec5-130">However by using the SharePoint Online Management Shell and CSV files, this is fast and easy.</span></span> <span data-ttu-id="baec5-131">Dans cette tâche, vous allez utiliser Windows PowerShell pour supprimer un utilisateur d’un groupe de sécurité de collection de sites.</span><span class="sxs-lookup"><span data-stu-id="baec5-131">In this task, you'll use Windows PowerShell to remove a user from a site collection security group.</span></span> <span data-ttu-id="baec5-132">Vous utiliserez ensuite un fichier CSV et supprimerez de nombreux utilisateurs de différents sites.</span><span class="sxs-lookup"><span data-stu-id="baec5-132">Then you'll use a CSV file and remove lots of users from different sites.</span></span> 

<span data-ttu-id="baec5-133">Nous allons utiliser la cmdlet « Remove-SPOUser » pour supprimer un seul utilisateur Microsoft 365 d’un groupe de collections de sites afin de voir la syntaxe de commande.</span><span class="sxs-lookup"><span data-stu-id="baec5-133">We'll be using the 'Remove-SPOUser' cmdlet to remove a single Microsoft 365 user from a site collection group just so we can see the command syntax.</span></span> <span data-ttu-id="baec5-134">Voici à quoi ressemble la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="baec5-134">Here is how the syntax looks:</span></span>

```powershell
$tenant = "<tenant name, such as litwareinc for litwareinc.com>"
$site = "<site name>"
$user = "<user account name, such as opalc>"
$group = "<group name name, such as Auditors>"
Remove-SPOUser -LoginName $user@$tenant.com -Site https://$tenant.sharepoint.com/sites/$site -Group $group
```
<span data-ttu-id="baec5-135">Par exemple, nous allons supprimer Contrôle Overby du groupe Auditeurs de la collection de sites contosotest dans la location contoso :</span><span class="sxs-lookup"><span data-stu-id="baec5-135">For example, let's remove Bobby Overby from the site collection Auditors group in the contosotest site collection in the contoso tenancy:</span></span>

```powershell
$tenant = "contoso"
$site = "contosotest"
$user = "bobbyo"
$group = "Auditors"
Remove-SPOUser -LoginName $user@$tenant.com -Site https://$tenant.sharepoint.com/sites/$site -Group $group
```

<span data-ttu-id="baec5-p106">Supposons que nous voulions supprimer Bobby de tous les groupes auxquels il appartient actuellement. Voici comment procéder :</span><span class="sxs-lookup"><span data-stu-id="baec5-p106">Suppose we wanted to remove Bobby from all the groups he is currently in. Here is how we would do that:</span></span>

```powershell
$tenant = "contoso"
$user = "bobbyo"
Get-SPOSite | ForEach {Get-SPOSiteGroup –Site $_.Url} | ForEach {Remove-SPOUser -LoginName $user@$tenant.com -Site &_.Url}
```

> [!WARNING]
> <span data-ttu-id="baec5-138">Il s’agit simplement d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="baec5-138">This is just an example.</span></span> <span data-ttu-id="baec5-139">Vous ne devez pas exécuter cette commande sauf si vous devez vraiment supprimer un utilisateur de chaque groupe, par exemple si l’utilisateur quitte l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="baec5-139">You should not run this command unless you really have to remove a user from every group, for example if the user leaves the company.</span></span>

## <a name="automate-management-of-large-lists-of-users-and-groups"></a><span data-ttu-id="baec5-140">Automatiser la gestion des grandes listes d’utilisateurs et de groupes</span><span class="sxs-lookup"><span data-stu-id="baec5-140">Automate management of large lists of users and groups</span></span>

<span data-ttu-id="baec5-141">Pour ajouter un grand nombre de comptes à des sites SharePoint et leur accorder des autorisations, vous pouvez utiliser le Centre d’administration Microsoft 365, des commandes PowerShell individuelles ou PowerShell un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="baec5-141">To add a large number of accounts to SharePoint sites and give them permissions, you can use the Microsoft 365 admin center, individual PowerShell commands, or PowerShell an a CSV file.</span></span> <span data-ttu-id="baec5-142">Parmi tous ces choix, le fichier CSV est le moyen le plus rapide d’automatiser cette tâche.</span><span class="sxs-lookup"><span data-stu-id="baec5-142">Of these choices, the CSV file is the fastest way to automate this task.</span></span>

<span data-ttu-id="baec5-143">Le processus de base consiste à créer un fichier CSV qui possède des en-têtes (colonnes) correspondant aux paramètres dont le script Windows PowerShell a besoin.</span><span class="sxs-lookup"><span data-stu-id="baec5-143">The basic process is to create a CSV file that has headers (columns) that correspond to the parameters that the Windows PowerShell script needs.</span></span> <span data-ttu-id="baec5-144">Vous pouvez facilement créer une telle liste dans Excel puis l’exporter en tant que fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="baec5-144">You can easily create such a list in Excel and then export it as a CSV file.</span></span> <span data-ttu-id="baec5-145">Ensuite, vous utilisez un script Windows PowerShell pour parcourir les enregistrements (lignes) dans le fichier CSV, en ajoutant les utilisateurs à des groupes et les groupes à des sites.</span><span class="sxs-lookup"><span data-stu-id="baec5-145">Then, you use a Windows PowerShell script to iterate through records (rows) in the CSV file, adding the users to groups and the groups to sites.</span></span> 

<span data-ttu-id="baec5-146">Par exemple, nous allons créer un fichier CSV pour définir un groupe de collections de sites, de groupes et d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="baec5-146">For example, let's create a CSV file to define a group of site collections, groups, and permissions.</span></span> <span data-ttu-id="baec5-147">Puis, nous créerons un fichier CSV pour remplir les groupes avec des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="baec5-147">Next, we will create a CSV file to populate the groups with users.</span></span> <span data-ttu-id="baec5-148">Enfin, nous créerons puis exécuterons un script Windows PowerShell simple qui crée et remplit les groupes.</span><span class="sxs-lookup"><span data-stu-id="baec5-148">Finally, we will create and run a simple Windows PowerShell script that creates and populates the groups.</span></span>

<span data-ttu-id="baec5-149">Le premier fichier CSV ajoutera des groupes à des collections de sites et aura la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="baec5-149">The first CSV file will add one or more groups to one or more site collections and will have this structure:</span></span>

<span data-ttu-id="baec5-150">En-tête :</span><span class="sxs-lookup"><span data-stu-id="baec5-150">Header:</span></span>

```powershell
Site,Group,PermissionLevels
```

<span data-ttu-id="baec5-151">Élément :</span><span class="sxs-lookup"><span data-stu-id="baec5-151">Item:</span></span>

```powershell
https://tenant.sharepoint.com/sites/site,group,level
```

<span data-ttu-id="baec5-152">Voici un exemple de fichier :</span><span class="sxs-lookup"><span data-stu-id="baec5-152">Here is an example file:</span></span>

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

<span data-ttu-id="baec5-153">Le second fichier CSV ajoutera des utilisateurs à des groupes et aura la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="baec5-153">The second CSV file will add one or more users to one or more groups and will have this structure:</span></span>

<span data-ttu-id="baec5-154">En-tête :</span><span class="sxs-lookup"><span data-stu-id="baec5-154">Header:</span></span>

```powershell
Group,LoginName,Site
```

<span data-ttu-id="baec5-155">Élément :</span><span class="sxs-lookup"><span data-stu-id="baec5-155">Item:</span></span>

```powershell
group,login,https://tenant.sharepoint.com/sites/site
```

<span data-ttu-id="baec5-156">Voici un exemple de fichier :</span><span class="sxs-lookup"><span data-stu-id="baec5-156">Here is an example file:</span></span>

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

<span data-ttu-id="baec5-157">Pour la prochaine étape, vous devez avoir enregistré les deux fichiers CSV sur votre lecteur.</span><span class="sxs-lookup"><span data-stu-id="baec5-157">For the next step, you must have the two CSV files saved to your drive.</span></span> <span data-ttu-id="baec5-158">Voici des exemples de commandes qui utilisent à la fois les fichiers CSV et pour ajouter des autorisations et l’appartenance à un groupe :</span><span class="sxs-lookup"><span data-stu-id="baec5-158">Here are example commands that use both CSV files and to add permissions and group membership:</span></span>

```powershell
Import-Csv C:\O365Admin\GroupsAndPermissions.csv | ForEach {New-SPOSiteGroup -Group $_.Group -PermissionLevels $_.PermissionLevels -Site $_.Site}
Import-Csv C:\O365Admin\Users.csv | ForEach {Add-SPOUser -Group $_.Group –LoginName $_.LoginName -Site $_.Site}
```

<span data-ttu-id="baec5-159">Le script importe le contenu du fichier CSV et utilise les valeurs des colonnes pour remplir les paramètres des commandes **New-SPOSiteGroup** et **Add-SPOUser.**</span><span class="sxs-lookup"><span data-stu-id="baec5-159">The script imports the CSV file contents and uses the values in the columns to populate the parameters of the **New-SPOSiteGroup** and **Add-SPOUser** commands.</span></span> <span data-ttu-id="baec5-160">Dans notre exemple, nous l’enregistrez dans le dossierO365Admin sur le lecteur C, mais vous pouvez l’enregistrer à tout moment.</span><span class="sxs-lookup"><span data-stu-id="baec5-160">In our example, we are saving this to theO365Admin folder on drive C, but you can save it wherever you want.</span></span>

<span data-ttu-id="baec5-161">Maintenant, nous allons supprimer un groupe de personnes pour plusieurs groupes dans différents sites à l’aide du même fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="baec5-161">Now, let's remove a bunch of people for several groups in different sites using the same CSV file.</span></span> <span data-ttu-id="baec5-162">Voici un exemple de commande :</span><span class="sxs-lookup"><span data-stu-id="baec5-162">Here is an example command:</span></span>

```powershell
Import-Csv C:\O365Admin\Users.csv | ForEach {Remove-SPOUser -LoginName $_.LoginName -Site $_.Site -Group $_.Group}
```

## <a name="generate-user-reports"></a><span data-ttu-id="baec5-163">Générer des rapports sur les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="baec5-163">Generate user reports</span></span>

<span data-ttu-id="baec5-p114">Vous pouvez obtenir un rapport simple pour quelques sites et afficher les utilisateurs de ces sites, leur niveau d’autorisation, ainsi que d’autres propriétés. Voici à quoi ressemble la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="baec5-p114">You might want to get a simple report for a few sites and display the users for those sites, their permission level, and other properties. This is how the syntax looks:</span></span>

```powershell
$tenant = "<tenant name, such as litwareinc for litwareinc.com>"
$site = "<site name>"
Get-SPOUser -Site https://$tenant.sharepoint.com/sites/$site | select * | Format-table -Wrap -AutoSize | Out-File c\UsersReport.txt -Force -Width 360 -Append
```

<span data-ttu-id="baec5-p115">Cela permet de collecter les données de ces trois sites et de les écrire dans un fichier texte sur votre lecteur local. Notez que le paramètre –Append ajoutera le nouveau contenu à un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="baec5-p115">This will grab the data for these three sites and write them to a text file on your local drive. Note that the parameter –Append will add new content to an existing file.</span></span>

<span data-ttu-id="baec5-168">Par exemple, nous allons exécuter un rapport sur les sites ContosoTest, TeamSite01 et Project01 pour la location contoso1 :</span><span class="sxs-lookup"><span data-stu-id="baec5-168">For example, let's run a report on the ContosoTest, TeamSite01, and Project01 sites for the Contoso1 tenant:</span></span>

```powershell
$tenant = "contoso"
$site = "contosotest"
Get-SPOUser -Site https://$tenant.sharepoint.com/sites/$site | Format-Table -Wrap -AutoSize | Out-File c:\UsersReport.txt -Force -Width 360 -Append
$site = "TeamSite01"
Get-SPOUser -Site https://$tenant.sharepoint.com/sites/$site |Format-Table -Wrap -AutoSize | Out-File c:\UsersReport.txt -Force -Width 360 -Append
$site = "Project01"
Get-SPOUser -Site https://$tenant.sharepoint.com/sites/$site | Format-Table -Wrap -AutoSize | Out-File c:\UsersReport.txt -Force -Width 360 -Append
```

<span data-ttu-id="baec5-169">Notez que nous n’avons dû modifier que **$site** variable.</span><span class="sxs-lookup"><span data-stu-id="baec5-169">Note that we had to change only the **$site** variable.</span></span> <span data-ttu-id="baec5-170">La **$tenant** variable conserve sa valeur pendant les trois séries de la commande.</span><span class="sxs-lookup"><span data-stu-id="baec5-170">The **$tenant** variable keeps its value through all three runs of the command.</span></span>

<span data-ttu-id="baec5-p117">Mais que faire si vous souhaitez effectuer cette action pour chaque site ? Vous pouvez le faire sans avoir à entrer tous ces sites web à l’aide de cette commande :</span><span class="sxs-lookup"><span data-stu-id="baec5-p117">However, what if you wanted to do this for every site? You can do this without having to type all those websites by using this command:</span></span>

```powershell
Get-SPOSite | ForEach {Get-SPOUser –Site $_.Url} | Format-Table -Wrap -AutoSize | Out-File c:\UsersReport.txt -Force -Width 360 -Append
```

<span data-ttu-id="baec5-173">Ce rapport est assez simple, et vous pouvez ajouter du code pour créer des rapports plus spécifiques ou des rapports qui contiennent des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="baec5-173">This report is fairly simple, and you can add more code to create more specific reports or reports that include more detailed information.</span></span> <span data-ttu-id="baec5-174">Toutefois, cela devrait vous donner une idée de l’utilisation de SharePoint Online Management Shell pour gérer les utilisateurs dans l’environnement SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="baec5-174">But this should give you an idea of how to use the SharePoint Online Management Shell to manage users in the SharePoint Online environment.</span></span>
   
## <a name="see-also"></a><span data-ttu-id="baec5-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baec5-175">See also</span></span>

[<span data-ttu-id="baec5-176">Connexion à SharePoint Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="baec5-176">Connect to SharePoint Online PowerShell</span></span>](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[<span data-ttu-id="baec5-177">Gérer SharePoint Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="baec5-177">Manage SharePoint Online with PowerShell</span></span>](create-sharepoint-sites-and-add-users-with-powershell.md)

[<span data-ttu-id="baec5-178">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="baec5-178">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="baec5-179">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="baec5-179">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)