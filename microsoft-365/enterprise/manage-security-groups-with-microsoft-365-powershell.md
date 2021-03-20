---
title: Gérer les groupes de sécurité avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: article
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
- O365ITProTrain
description: Découvrez comment utiliser PowerShell pour gérer les groupes de sécurité.
ms.openlocfilehash: 64a02a1472fdeb0d61cfb4f380cbe61dd7b557b6
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50909501"
---
# <a name="manage-security-groups-with-powershell"></a><span data-ttu-id="f7178-103">Gérer les groupes de sécurité avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7178-103">Manage security groups with PowerShell</span></span>

<span data-ttu-id="f7178-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="f7178-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="f7178-105">Vous pouvez utiliser PowerShell pour Microsoft 365 comme alternative au Centre d’administration Microsoft 365 pour gérer les groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-105">You can use PowerShell for Microsoft 365 as an alternative to the Microsoft 365 admin center to manage security groups.</span></span> 

<span data-ttu-id="f7178-106">Cet article décrit la liste, la création, la modification des paramètres et la suppression de groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-106">This article describes listing, creating, changing settings, and removing security groups.</span></span> 

<span data-ttu-id="f7178-107">Lorsqu’un bloc de commandes dans cet article nécessite que vous spécifiant des valeurs de variable, utilisez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="f7178-107">When a command block in this article requires that you specify variable values, use these steps.</span></span>

1. <span data-ttu-id="f7178-108">Copiez le bloc de commandes dans le Presse-papiers et collez-le dans le Bloc-notes ou dans l’environnement de script intégré à PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="f7178-108">Copy the command block to the clipboard and paste it into Notepad or the PowerShell Integrated Script Environment (ISE).</span></span>
2. <span data-ttu-id="f7178-109">Remplissez les valeurs des variables et supprimez les caractères « < » et « > ».</span><span class="sxs-lookup"><span data-stu-id="f7178-109">Fill in the variable values and remove the "<" and ">" characters.</span></span>
3. <span data-ttu-id="f7178-110">Exécutez les commandes dans la fenêtre PowerShell ou powerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="f7178-110">Run the commands in the PowerShell window or the PowerShell ISE.</span></span>

<span data-ttu-id="f7178-111">Voir [Gérer l’appartenance à un groupe de](maintain-group-membership-with-microsoft-365-powershell.md) sécurité pour gérer l’appartenance à un groupe avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7178-111">See [Maintain security group membership](maintain-group-membership-with-microsoft-365-powershell.md) to manage group membership with PowerShell.</span></span>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="f7178-112">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="f7178-112">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="f7178-113">Tout [d’abord, connectez-vous à votre client Microsoft 365.](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="f7178-113">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>

### <a name="list-your-groups"></a><span data-ttu-id="f7178-114">Lister vos groupes</span><span class="sxs-lookup"><span data-stu-id="f7178-114">List your groups</span></span>

<span data-ttu-id="f7178-115">Utilisez cette commande pour lister tous vos groupes.</span><span class="sxs-lookup"><span data-stu-id="f7178-115">Use this command to list all of your groups.</span></span>

```powershell
Get-AzureADGroup
```
<span data-ttu-id="f7178-116">Utilisez ces commandes pour afficher les paramètres d’un groupe spécifique par son nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f7178-116">Use these commands to display the settings of a specific group by its display name.</span></span>

```powershell
$groupName="<display name of the group>"
Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }
```

### <a name="create-a-new-group"></a><span data-ttu-id="f7178-117">Créer un groupe</span><span class="sxs-lookup"><span data-stu-id="f7178-117">Create a new group</span></span>

<span data-ttu-id="f7178-118">Utilisez cette commande pour créer un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-118">Use this command to create a new security group.</span></span>

```powershell
New-AzureADGroup -Description "<group purpose>" -DisplayName "<name>" -MailEnabled $false -SecurityEnabled $true -MailNickName "<email name>"
```

### <a name="change-the-settings-on-a-group"></a><span data-ttu-id="f7178-119">Modifier les paramètres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="f7178-119">Change the settings on a group</span></span>

<span data-ttu-id="f7178-120">Affichez les paramètres du groupe avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="f7178-120">Display the settings of the group with these commands.</span></span>

```powershell
$groupName="<display name of the group>"
Get-AzureADGroup | Where { $_.DisplayName -eq $groupName } | Select *
```

<span data-ttu-id="f7178-121">Ensuite, utilisez [l’article Set-AzureADGroup](/powershell/module/azuread/set-azureadgroup) pour déterminer comment modifier un paramètre.</span><span class="sxs-lookup"><span data-stu-id="f7178-121">Then, use the [Set-AzureADGroup](/powershell/module/azuread/set-azureadgroup) article to determine how to change a setting.</span></span>

### <a name="remove-a-security-group"></a><span data-ttu-id="f7178-122">Supprimer un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="f7178-122">Remove a security group</span></span>

<span data-ttu-id="f7178-123">Utilisez ces commandes pour supprimer un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-123">Use these commands to remove a security group.</span></span>

```powershell
$groupName="<display name of the group>"
Remove-AzureADGroup -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectId
```

### <a name="manage-the-owners-of-a-security-group"></a><span data-ttu-id="f7178-124">Gérer les propriétaires d’un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="f7178-124">Manage the owners of a security group</span></span>

<span data-ttu-id="f7178-125">Utilisez ces commandes pour afficher les propriétaires actuels d’un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-125">Use these commands to display the current owners of a security group.</span></span>

```powershell
$groupName="<display name of the group>"
Get-AzureADGroupOwner -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectId
```
<span data-ttu-id="f7178-126">Utilisez ces commandes pour ajouter un compte d’utilisateur par son nom **d’utilisateur principal (UPN)** aux propriétaires actuels d’un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-126">Use these commands to add a user account by its **user principal name (UPN)** to the current owners of a security group.</span></span>

```powershell
$userUPN="<UPN of the user account to add>"
$groupName="<display name of the group>"
Add-AzureADGroupOwner -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectId -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectId
```
<span data-ttu-id="f7178-127">Utilisez ces commandes pour ajouter un compte d’utilisateur par **son** nom complet aux propriétaires actuels d’un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-127">Use these commands to add a user account by its **display name** to the current owners of a security group.</span></span>

```powershell
$userName="<Display name of the user account to add>"
$groupName="<display name of the group>"
Add-AzureADGroupOwner -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectId -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userName }).ObjectId
```
<span data-ttu-id="f7178-128">Utilisez ces commandes pour supprimer un compte d’utilisateur par son **UPN** aux propriétaires actuels d’un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-128">Use these commands to remove a user account by its **UPN** to the current owners of a security group.</span></span>

```powershell
$userUPN="<UPN of the user account to remove>"
$groupName="<display name of the group>"
Remove-AzureADGroupOwner -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectId -OwnerId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectId
```

<span data-ttu-id="f7178-129">Utilisez ces commandes pour supprimer un compte d’utilisateur par **son** nom d’affichage pour les propriétaires actuels d’un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-129">Use these commands to remove a user account by its **display name** to the current owners of a security group.</span></span>

```powershell
$userName="<Display name of the user account to remove>"
$groupName="<display name of the group>"
Remove-AzureADGroupOwner -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectId -OwnerId (Get-AzureADUser | Where { $_.DisplayName -eq $userName }).ObjectId
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="f7178-130">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7178-130">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="f7178-131">Tout [d’abord, connectez-vous à votre client Microsoft 365.](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell)</span><span class="sxs-lookup"><span data-stu-id="f7178-131">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

### <a name="list-your-groups"></a><span data-ttu-id="f7178-132">Lister vos groupes</span><span class="sxs-lookup"><span data-stu-id="f7178-132">List your groups</span></span>

<span data-ttu-id="f7178-133">Utilisez cette commande pour lister tous vos groupes.</span><span class="sxs-lookup"><span data-stu-id="f7178-133">Use this command to list all of your groups.</span></span>

```powershell
Get-MsolGroup
```
<span data-ttu-id="f7178-134">Utilisez ces commandes pour afficher les paramètres d’un groupe spécifique par son nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f7178-134">Use these commands to display the settings of a specific group by its display name.</span></span>

```powershell
$groupName="<display name of the group>"
Get-MsolGroup | Where { $_.DisplayName -eq $groupName }
```

### <a name="create-a-new-group"></a><span data-ttu-id="f7178-135">Créer un groupe</span><span class="sxs-lookup"><span data-stu-id="f7178-135">Create a new group</span></span>

<span data-ttu-id="f7178-136">Utilisez cette commande pour créer un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-136">Use this command to create a new security group.</span></span>

```powershell
New-MsolGroup -Description "<group purpose>" -DisplayName "<name>"
```

### <a name="change-the-settings-on-a-group"></a><span data-ttu-id="f7178-137">Modifier les paramètres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="f7178-137">Change the settings on a group</span></span>

<span data-ttu-id="f7178-138">Affichez les paramètres du groupe avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="f7178-138">Display the settings of the group with these commands.</span></span>

```powershell
$groupName="<display name of the group>"
Get-MsolGroup | Where { $_.DisplayName -eq $groupName } | Select *
```

<span data-ttu-id="f7178-139">Ensuite, utilisez [l’article Set-MsolGroup](/powershell/module/msonline/set-msolgroup) pour déterminer comment modifier un paramètre.</span><span class="sxs-lookup"><span data-stu-id="f7178-139">Then, use the [Set-MsolGroup](/powershell/module/msonline/set-msolgroup) article to determine how to change a setting.</span></span>

### <a name="remove-a-security-group"></a><span data-ttu-id="f7178-140">Supprimer un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="f7178-140">Remove a security group</span></span>

<span data-ttu-id="f7178-141">Utilisez ces commandes pour supprimer un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f7178-141">Use these commands to remove a security group.</span></span>

```powershell
$groupName="<display name of the group>"
Remove-MsolGroup -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectId
```

## <a name="see-also"></a><span data-ttu-id="f7178-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7178-142">See also</span></span>

[<span data-ttu-id="f7178-143">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7178-143">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="f7178-144">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7178-144">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="f7178-145">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f7178-145">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)