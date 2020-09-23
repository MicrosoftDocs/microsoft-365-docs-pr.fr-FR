---
title: Mettre à jour l’appartenance au groupe Microsoft 365 avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/23/2020
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
ms.assetid: 6770c5fa-b886-4512-8c67-ffd53226589e
description: Découvrez comment utiliser PowerShell pour gérer l’appartenance aux groupes Microsoft 365.
ms.openlocfilehash: 464ebcebe87fcd7ce081de85e75acf76cd6d5a46
ms.sourcegitcommit: c1ee4ed3c5826872b57339e1e1aa33b4d2209711
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2020
ms.locfileid: "48235629"
---
# <a name="maintain-microsoft-365-group-membership-with-powershell"></a><span data-ttu-id="82bf1-103">Mettre à jour l’appartenance au groupe Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="82bf1-103">Maintain Microsoft 365 group membership with PowerShell</span></span>

<span data-ttu-id="82bf1-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="82bf1-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="82bf1-105">Vous pouvez utiliser PowerShell pour Microsoft 365 comme alternative au centre d’administration Microsoft 365 pour gérer l’appartenance au groupe dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="82bf1-105">You can use PowerShell for Microsoft 365 as an alternative to the Microsoft 365 admin center to maintain group membership in Microsoft 365.</span></span> 

> [!TIP]
> <span data-ttu-id="82bf1-106">Pour générer des commandes PowerShell prêtes à l’emploi en spécifiant des noms de comptes et de groupes d’utilisateurs, utilisez ce [classeur Microsoft Excel de maintenance de groupe](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/media/maintain-group-membership-with-microsoft-365-powershell/GroupMaintPowerShellGenerator.xlsx).</span><span class="sxs-lookup"><span data-stu-id="82bf1-106">To generate ready-to-run PowerShell commands by specifying user account and group names, use this [group maintenance Microsoft Excel workbook](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/media/maintain-group-membership-with-microsoft-365-powershell/GroupMaintPowerShellGenerator.xlsx).</span></span> 

>[!Note]
><span data-ttu-id="82bf1-107">[Découvrez comment gérer l’appartenance à un groupe microsoft 365](https://docs.microsoft.com/microsoft-365/admin/create-groups/add-or-remove-members-from-groups) avec le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="82bf1-107">[Learn how to maintain Microsoft 365 group membership](https://docs.microsoft.com/microsoft-365/admin/create-groups/add-or-remove-members-from-groups) with the Microsoft 365 admin center.</span></span> <span data-ttu-id="82bf1-108">Pour obtenir la liste des ressources supplémentaires, consultez la rubrique [gérer les utilisateurs et les groupes](https://docs.microsoft.com/microsoft-365/admin/add-users/).</span><span class="sxs-lookup"><span data-stu-id="82bf1-108">For a list of additional resources, see [Manage users and groups](https://docs.microsoft.com/microsoft-365/admin/add-users/).</span></span>
>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="82bf1-109">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="82bf1-109">Use the Azure Active Directory PowerShell for Graph module</span></span>
<span data-ttu-id="82bf1-110">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="82bf1-110">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>

### <a name="add-or-remove-user-accounts-as-members-of-a-group"></a><span data-ttu-id="82bf1-111">Ajouter ou supprimer des comptes d’utilisateurs en tant que membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="82bf1-111">Add or remove user accounts as members of a group</span></span>

<span data-ttu-id="82bf1-112">**Pour ajouter un compte d’utilisateur par son UPN**, renseignez le nom d’utilisateur du compte d’utilisateur (UPN) (exemple : belindan@contoso.com) et le nom d’affichage du groupe, en supprimant les caractères « < » et « > », puis exécutez ces commandes dans la fenêtre PowerShell ou dans l’environnement de script intégré PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="82bf1-112">**To add a user account by its UPN**, fill in the user account User Principal Name (UPN) (example: belindan@contoso.com) and the group display name, removing the “<” and “>” characters, and run these commands in the PowerShell window or the PowerShell Integrated Script Environment (ISE).</span></span>

```powershell
$userUPN="<UPN of the user account to add>"
$groupName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="82bf1-113">**Pour ajouter un compte d’utilisateur par son nom d’affichage**, renseignez le nom d’affichage du compte d’utilisateur (par exemple : Belinda Newman) et le nom d’affichage du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-113">**To add a user account by its display name**, fill in the user account display name (example: Belinda Newman) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userName="<display name of the user account to add>"
$groupName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userName }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="82bf1-114">**Pour supprimer un compte d’utilisateur par son UPN**, renseignez l’UPN du compte d’utilisateur (par exemple : belindan@contoso.com) et le nom d’affichage du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-114">**To remove a user account by its UPN**, fill in the user account UPN (example: belindan@contoso.com) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userUPN="<UPN of the user account to remove>"
$groupName="<display name of the group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="82bf1-115">**Pour supprimer un compte d’utilisateur par son nom d’affichage**, renseignez le nom d’affichage du compte d’utilisateur (par exemple : Belinda Newman) et le nom d’affichage du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-115">**To remove a user account by its display name**, fill in the user account display name (example: Belinda Newman) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userName="<display name of the user account to remove>"
$groupName="<display name of the group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

### <a name="add-or-remove-groups-as-members-of-a-group"></a><span data-ttu-id="82bf1-116">Ajouter ou supprimer des groupes en tant que membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="82bf1-116">Add or remove groups as members of a group</span></span>

<span data-ttu-id="82bf1-117">Les groupes de sécurité peuvent contenir d’autres groupes en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="82bf1-117">Security groups can contain other groups as members.</span></span> <span data-ttu-id="82bf1-118">Toutefois, les groupes Microsoft 365 ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="82bf1-118">Microsoft 365 groups, however, cannot.</span></span> <span data-ttu-id="82bf1-119">Cette section contient les commandes PowerShell permettant d’ajouter ou de supprimer des groupes uniquement pour un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="82bf1-119">This section contains PowerShell commands to add or remove groups only for a security group.</span></span>

<span data-ttu-id="82bf1-120">**Pour ajouter un groupe par son nom d’affichage**, renseignez le nom d’affichage du groupe que vous allez ajouter et le nom d’affichage du groupe qui contiendra le groupe de membres et exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-120">**To add a group by its display name**, fill in the display name of the group you’re going to add and the display name of the group that will contain the member group and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group that will contain the member group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="82bf1-121">**Pour supprimer un groupe par son nom d’affichage**, renseignez le nom d’affichage du groupe que vous allez supprimer et le nom d’affichage du groupe qui contiendra le groupe de membres et exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-121">**To remove a group by its display name**, fill in the display name of the group you’re going to remove and the display name of the group that will contain the member group and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group that will contain the member group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="82bf1-122">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="82bf1-122">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="82bf1-123">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="82bf1-123">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>


### <a name="add-or-remove-user-accounts-as-members-of-a-group"></a><span data-ttu-id="82bf1-124">Ajouter ou supprimer des comptes d’utilisateurs en tant que membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="82bf1-124">Add or remove user accounts as members of a group</span></span>

<span data-ttu-id="82bf1-125">**Pour ajouter un compte d’utilisateur par son UPN**, renseignez le nom d’utilisateur du compte d’utilisateur (UPN) (exemple : belindan@contoso.com) et le nom d’affichage du groupe, en supprimant les caractères « < » et « > », puis exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-125">**To add a user account by its UPN**, fill in the user account User Principal Name (UPN) (example: belindan@contoso.com) and the group display name, removing the “<” and “>” characters, and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userUPN="<UPN of the user account to add>"
$groupName="<display name of the group>"
Add-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="82bf1-126">**Pour ajouter un compte d’utilisateur par son nom d’affichage**, renseignez le nom d’affichage du compte d’utilisateur (par exemple : Belinda Newman) et le nom d’affichage du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-126">**To add a user account by its display name**, fill in the user account display name (example: Belinda Newman) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userName="<display name of the user account to add>"
$groupName="<display name of the group>"
Add-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.DisplayName -eq $userName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="82bf1-127">**Pour supprimer un compte d’utilisateur par son UPN**, renseignez l’UPN du compte d’utilisateur (par exemple : belindan@contoso.com) et le nom d’affichage du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-127">**To remove a user account by its UPN**, fill in the user account UPN (example: belindan@contoso.com) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userUPN="<UPN of the user account to remove>"
$groupName="<display name of the group>"
Remove-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="82bf1-128">**Pour supprimer un compte d’utilisateur par son nom d’affichage**, renseignez le nom d’affichage du compte d’utilisateur (par exemple : Belinda Newman) et le nom d’affichage du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-128">**To remove a user account by its display name**, fill in the user account display name (example: Belinda Newman) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userName="<display name of the user account to remove>"
$groupName="<display name of the group>"
Remove-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.DisplayName -eq $userName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

### <a name="add-or-remove-groups-as-members-of-a-group"></a><span data-ttu-id="82bf1-129">Ajouter ou supprimer des groupes en tant que membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="82bf1-129">Add or remove groups as members of a group</span></span>

<span data-ttu-id="82bf1-130">Les groupes de sécurité peuvent contenir d’autres groupes en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="82bf1-130">Security groups can contain other groups as members.</span></span> <span data-ttu-id="82bf1-131">Toutefois, les groupes Microsoft 365 ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="82bf1-131">Microsoft 365 groups, however, cannot.</span></span> <span data-ttu-id="82bf1-132">Cette section contient les commandes PowerShell permettant d’ajouter ou de supprimer des groupes uniquement pour un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="82bf1-132">This section contains PowerShell commands to add or remove groups only for a security group.</span></span>

<span data-ttu-id="82bf1-133">**Pour ajouter un groupe par son nom d’affichage**, renseignez le nom d’affichage du groupe que vous allez ajouter et le nom d’affichage du groupe qui contiendra le groupe de membres et exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-133">**To add a group by its display name**, fill in the display name of the group you’re going to add and the display name of the group that will contain the member group and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group that will contain the member group>"
Add-MsolGroupMember -GroupMemberObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID -GroupMemberType Group
```

<span data-ttu-id="82bf1-134">**Pour supprimer un groupe par son nom d’affichage**, renseignez le nom d’affichage du groupe que vous allez supprimer et le nom d’affichage du groupe qui contiendra le groupe de membres et exécutez ces commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="82bf1-134">**To remove a group by its display name**, fill in the display name of the group you’re going to remove and the display name of the group that will contain the member group and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group contains the member group>"
Remove-MsolGroupMember -GroupMemberObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID -GroupMemberType Group
```

## <a name="see-also"></a><span data-ttu-id="82bf1-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82bf1-135">See also</span></span>

[<span data-ttu-id="82bf1-136">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="82bf1-136">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="82bf1-137">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="82bf1-137">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="82bf1-138">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="82bf1-138">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)

