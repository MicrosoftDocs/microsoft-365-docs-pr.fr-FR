---
title: Gestion des groupes de sites SharePoint Online avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/17/2019
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
description: Dans cet article, vous trouverez des procédures pour l’utilisation de PowerShell pour Microsoft 365 afin de gérer les groupes de sites SharePoint Online.
ms.openlocfilehash: fa9aff769ff84f8567c45b20c7b6c8a078b4a70c
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690076"
---
# <a name="manage-sharepoint-online-site-groups-with-powershell"></a><span data-ttu-id="1511a-103">Gestion des groupes de sites SharePoint Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="1511a-103">Manage SharePoint Online site groups with PowerShell</span></span>

<span data-ttu-id="1511a-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="1511a-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="1511a-105">Bien que vous puissiez utiliser le centre d’administration Microsoft 365, vous pouvez également utiliser PowerShell pour Microsoft 365 pour gérer vos groupes de sites SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="1511a-105">Although you can use the Microsoft 365 admin center, you can also use PowerShell for Microsoft 365 to manage your SharePoint Online site groups.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="1511a-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1511a-106">Before you begin</span></span>

<span data-ttu-id="1511a-107">Les procédures décrites dans cet article vous obligent à vous connecter à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="1511a-107">The procedures in this article require you to connect to SharePoint Online.</span></span> <span data-ttu-id="1511a-108">Pour plus d’informations, voir [Connect to SharePoint Online PowerShell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps).</span><span class="sxs-lookup"><span data-stu-id="1511a-108">For instructions, see [Connect to SharePoint Online PowerShell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps).</span></span>

## <a name="view-sharepoint-online-with-powershell-for-microsoft-365"></a><span data-ttu-id="1511a-109">Afficher SharePoint Online avec PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1511a-109">View SharePoint Online with PowerShell for Microsoft 365</span></span>

<span data-ttu-id="1511a-110">Le centre d’administration SharePoint Online propose des méthodes faciles à utiliser pour la gestion des groupes de sites.</span><span class="sxs-lookup"><span data-stu-id="1511a-110">The SharePoint Online admin center has some easy-to-use methods for managing site groups.</span></span> <span data-ttu-id="1511a-111">Par exemple, supposons que vous souhaitez consulter les groupes et les membres du groupe pour le `https://litwareinc.sharepoint.com/sites/finance` site.</span><span class="sxs-lookup"><span data-stu-id="1511a-111">For example, suppose you want to look at the groups, and the group members, for the `https://litwareinc.sharepoint.com/sites/finance` site.</span></span> <span data-ttu-id="1511a-112">Voici ce que vous devez faire pour :</span><span class="sxs-lookup"><span data-stu-id="1511a-112">Here's what you have to do to:</span></span>

1. <span data-ttu-id="1511a-113">Dans le centre d’administration SharePoint, cliquez sur **sites actifs**, puis cliquez sur l’URL du site.</span><span class="sxs-lookup"><span data-stu-id="1511a-113">From the SharePoint admin center, click **Active sites**, and then click the URL of the site.</span></span>
2. <span data-ttu-id="1511a-114">Sur la page site, cliquez sur l’icône **paramètres** (située dans l’angle supérieur droit de la page), puis cliquez sur **autorisations de site**.</span><span class="sxs-lookup"><span data-stu-id="1511a-114">On the site page, click the **Settings** icon (located in the upper right-hand corner of the page), and then click **Site permissions**.</span></span>

<span data-ttu-id="1511a-115">Répétez ensuite ce processus pour le prochain site que vous souhaitez consulter.</span><span class="sxs-lookup"><span data-stu-id="1511a-115">And then repeat the process for the next site you want to look at.</span></span>

<span data-ttu-id="1511a-116">Pour obtenir la liste des groupes avec PowerShell pour Microsoft 365, vous pouvez utiliser les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1511a-116">To get a list of the groups with PowerShell for Microsoft 365, you can use the following commands:</span></span>

```powershell
$siteURL = "https://litwareinc.sharepoint.com/sites/finance"
$x = Get-SPOSiteGroup -Site $siteURL
foreach ($y in $x)
    {
        Write-Host $y.Title -ForegroundColor "Yellow"
        Get-SPOSiteGroup -Site $siteURL -Group $y.Title | Select-Object -ExpandProperty Users
        Write-Host
    }
```

<span data-ttu-id="1511a-117">Il existe deux façons d’exécuter ce jeu de commandes dans l’invite de commandes SharePoint Online Management Shell :</span><span class="sxs-lookup"><span data-stu-id="1511a-117">There are two ways to run this command set in the SharePoint Online Management Shell command prompt:</span></span>

- <span data-ttu-id="1511a-118">Copiez les commandes dans le bloc-notes (ou un autre éditeur de texte), modifiez la valeur de la variable **$SiteUrl** , sélectionnez les commandes, puis collez-les dans l’invite de commandes SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="1511a-118">Copy the commands into Notepad (or another text editor), modify the value of the **$siteURL** variable, select the commands, and then paste them into the SharePoint Online Management Shell command prompt.</span></span> <span data-ttu-id="1511a-119">Dans ce cas, PowerShell s’arrête à l' **>>** invite.</span><span class="sxs-lookup"><span data-stu-id="1511a-119">When you do, PowerShell will stop at a **>>** prompt.</span></span> <span data-ttu-id="1511a-120">Appuyez sur entrée pour exécuter la `foreach` commande.</span><span class="sxs-lookup"><span data-stu-id="1511a-120">Press Enter to execute the `foreach` command.</span></span><br/>
- <span data-ttu-id="1511a-121">Copiez les commandes dans le Bloc-notes (ou un autre éditeur de texte), modifiez la valeur de la variable **$siteURL** et enregistrez ce fichier texte avec un nom et l’extension .ps1 dans un dossier approprié.</span><span class="sxs-lookup"><span data-stu-id="1511a-121">Copy the commands into Notepad (or another text editor), modify the value of the **$siteURL** variable, and then save this text file with a name and the .ps1 extension in a suitable folder.</span></span> <span data-ttu-id="1511a-122">Ensuite, exécutez le script à partir de l’invite de commandes SharePoint Online Management Shell en spécifiant son chemin d’accès et son nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="1511a-122">Next, run the script from the SharePoint Online Management Shell command prompt by specifying its path and file name.</span></span> <span data-ttu-id="1511a-123">Voici un exemple de commande :</span><span class="sxs-lookup"><span data-stu-id="1511a-123">Here is an example command:</span></span>

```powershell
C:\Scripts\SiteGroupsAndUsers.ps1
```

<span data-ttu-id="1511a-124">Dans les deux cas, quelque chose de ce type doit apparaître :</span><span class="sxs-lookup"><span data-stu-id="1511a-124">In both cases, you should see something similar to this:</span></span>

![Groupes de sites SharePoint Online](../media/SPO-site-groups.png)

<span data-ttu-id="1511a-126">Il s’agit de tous les groupes qui ont été créés pour le site `https://litwareinc.sharepoint.com/sites/finance` , ainsi que de tous les utilisateurs affectés à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="1511a-126">These are all the groups that have been created for the site `https://litwareinc.sharepoint.com/sites/finance`, and all the users assigned to those groups.</span></span> <span data-ttu-id="1511a-127">Les noms de groupes apparaissent en jaune pour que vous puissiez distinguer les noms de groupes de leurs membres.</span><span class="sxs-lookup"><span data-stu-id="1511a-127">The group names are in yellow to help you separate group names from their members.</span></span>

<span data-ttu-id="1511a-128">Autre exemple, voici un jeu de commandes qui répertorie les groupes et toutes les appartenances aux groupes de tous vos sites SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="1511a-128">As another example, here is a command set that lists the groups, and all the group memberships, for all of your SharePoint Online sites.</span></span>

```powershell
$x = Get-SPOSite
foreach ($y in $x)
    {
        Write-Host $y.Url -ForegroundColor "Yellow"
        $z = Get-SPOSiteGroup -Site $y.Url
        foreach ($a in $z)
            {
                 $b = Get-SPOSiteGroup -Site $y.Url -Group $a.Title 
                 Write-Host $b.Title -ForegroundColor "Cyan"
                 $b | Select-Object -ExpandProperty Users
                 Write-Host
            }
    }
```
    
## <a name="see-also"></a><span data-ttu-id="1511a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1511a-129">See also</span></span>

[<span data-ttu-id="1511a-130">Connexion à SharePoint Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="1511a-130">Connect to SharePoint Online PowerShell</span></span>](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)

[<span data-ttu-id="1511a-131">Création de sites SharePoint Online et ajout d’utilisateurs avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="1511a-131">Create SharePoint Online sites and add users with PowerShell</span></span>](create-sharepoint-sites-and-add-users-with-powershell.md)

[<span data-ttu-id="1511a-132">Gestion des utilisateurs et des groupes SharePoint Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="1511a-132">Manage SharePoint Online users and groups with PowerShell</span></span>](manage-sharepoint-users-and-groups-with-powershell.md)

[<span data-ttu-id="1511a-133">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="1511a-133">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="1511a-134">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1511a-134">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)

