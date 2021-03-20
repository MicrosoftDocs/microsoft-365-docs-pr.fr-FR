---
title: Conserver l’appartenance à un groupe de sécurité avec PowerShell
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
ms.assetid: 6770c5fa-b886-4512-8c67-ffd53226589e
description: Découvrez comment utiliser PowerShell pour maintenir l’appartenance aux groupes Microsoft 365.
ms.openlocfilehash: 9696c9093ae6f24a2edaf544e80794bde45d18d1
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50909573"
---
# <a name="maintain-security-group-membership-with-powershell"></a><span data-ttu-id="61e4f-103">Conserver l’appartenance à un groupe de sécurité avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="61e4f-103">Maintain security group membership with PowerShell</span></span>

<span data-ttu-id="61e4f-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="61e4f-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="61e4f-105">Vous pouvez utiliser PowerShell pour Microsoft 365 comme alternative au Centre d’administration Microsoft 365 pour conserver l’appartenance au groupe de sécurité dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="61e4f-105">You can use PowerShell for Microsoft 365 as an alternative to the Microsoft 365 admin center to maintain security group membership in Microsoft 365.</span></span> 

>[!Note]
><span data-ttu-id="61e4f-106">[Découvrez comment maintenir l’appartenance au groupe Microsoft 365](../admin/create-groups/add-or-remove-members-from-groups.md) avec le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="61e4f-106">[Learn how to maintain Microsoft 365 group membership](../admin/create-groups/add-or-remove-members-from-groups.md) with the Microsoft 365 admin center.</span></span> <span data-ttu-id="61e4f-107">Pour obtenir la liste des ressources supplémentaires, voir [Gérer les utilisateurs et les groupes.](../admin/add-users/index.yml)</span><span class="sxs-lookup"><span data-stu-id="61e4f-107">For a list of additional resources, see [Manage users and groups](../admin/add-users/index.yml).</span></span>
>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="61e4f-108">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="61e4f-108">Use the Azure Active Directory PowerShell for Graph module</span></span>
<span data-ttu-id="61e4f-109">Tout [d’abord, connectez-vous à votre client Microsoft 365.](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="61e4f-109">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>

### <a name="add-or-remove-user-accounts-as-members-of-a-group"></a><span data-ttu-id="61e4f-110">Ajouter ou supprimer des comptes d’utilisateur en tant que membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="61e4f-110">Add or remove user accounts as members of a group</span></span>

<span data-ttu-id="61e4f-111">Pour ajouter un compte d’utilisateur par son **UPN,** indiquez le nom d’utilisateur principal (UPN) du compte d’utilisateur (par exemple : belindan@contoso.com) et le nom complet du groupe de sécurité, en supprimant les caractères « < » et « > », puis exécutez ces commandes dans la fenêtre PowerShell ou dans l’environnement de script intégré De PowerShell .</span><span class="sxs-lookup"><span data-stu-id="61e4f-111">**To add a user account by its UPN**, fill in the user account User Principal Name (UPN) (example: belindan@contoso.com) and the security group display name, removing the “<” and “>” characters, and run these commands in the PowerShell window or the PowerShell Integrated Script Environment (ISE).</span></span>

```powershell
$userUPN="<UPN of the user account to add>"
$groupName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="61e4f-112">Pour ajouter un compte d’utilisateur par son nom d’affichage, remplissez le nom complet du compte d’utilisateur (exemple : Belinda Newman) et le nom complet du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou powerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="61e4f-112">**To add a user account by its display name**, fill in the user account display name (example: Belinda Newman) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userName="<display name of the user account to add>"
$groupName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userName }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="61e4f-113">Pour supprimer un compte d’utilisateur par son **UPN,** remplissez l’UPN du compte d’utilisateur (exemple : belindan@contoso.com) et le nom d’affichage du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou powerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="61e4f-113">**To remove a user account by its UPN**, fill in the user account UPN (example: belindan@contoso.com) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userUPN="<UPN of the user account to remove>"
$groupName="<display name of the group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="61e4f-114">Pour supprimer un compte d’utilisateur par son nom d’affichage, remplissez le nom complet du compte d’utilisateur (exemple : Belinda Newman) et le nom complet du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou powerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="61e4f-114">**To remove a user account by its display name**, fill in the user account display name (example: Belinda Newman) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userName="<display name of the user account to remove>"
$groupName="<display name of the group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

### <a name="add-or-remove-groups-as-members-of-a-group"></a><span data-ttu-id="61e4f-115">Ajouter ou supprimer des groupes en tant que membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="61e4f-115">Add or remove groups as members of a group</span></span>

<span data-ttu-id="61e4f-116">Les groupes de sécurité peuvent contenir d’autres groupes en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="61e4f-116">Security groups can contain other groups as members.</span></span> <span data-ttu-id="61e4f-117">Toutefois, les groupes Microsoft 365 ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="61e4f-117">Microsoft 365 groups, however, cannot.</span></span> <span data-ttu-id="61e4f-118">Cette section contient des commandes PowerShell pour ajouter ou supprimer des groupes uniquement pour un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="61e4f-118">This section contains PowerShell commands to add or remove groups only for a security group.</span></span>

<span data-ttu-id="61e4f-119">Pour ajouter un groupe par son nom d’affichage, remplissez le nom complet du groupe que vous allez ajouter et le nom complet du groupe qui contiendra le groupe de membres et exécuterez ces commandes dans la fenêtre PowerShell ou l’ISE PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61e4f-119">**To add a group by its display name**, fill in the display name of the group you’re going to add and the display name of the group that will contain the member group and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group that will contain the member group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="61e4f-120">Pour supprimer un groupe par son nom d’affichage, remplissez le nom complet du groupe que vous allez supprimer et le nom complet du groupe qui contiendra le groupe de membres et exécutez ces commandes dans la fenêtre PowerShell ou l’ISE PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61e4f-120">**To remove a group by its display name**, fill in the display name of the group you’re going to remove and the display name of the group that will contain the member group and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group that will contain the member group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="61e4f-121">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61e4f-121">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="61e4f-122">Tout [d’abord, connectez-vous à votre client Microsoft 365.](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell)</span><span class="sxs-lookup"><span data-stu-id="61e4f-122">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>


### <a name="add-or-remove-user-accounts-as-members-of-a-group"></a><span data-ttu-id="61e4f-123">Ajouter ou supprimer des comptes d’utilisateur en tant que membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="61e4f-123">Add or remove user accounts as members of a group</span></span>

<span data-ttu-id="61e4f-124">Pour ajouter un compte d’utilisateur par son **nom** d’utilisateur principal, indiquez le nom d’utilisateur principal (UPN) du compte d’utilisateur (exemple : belindan@contoso.com) et le nom complet du groupe, en supprimant les caractères « < » et « > », puis exécutez ces commandes dans la fenêtre PowerShell ou l’ISE PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61e4f-124">**To add a user account by its UPN**, fill in the user account User Principal Name (UPN) (example: belindan@contoso.com) and the group display name, removing the “<” and “>” characters, and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userUPN="<UPN of the user account to add>"
$groupName="<display name of the group>"
Add-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="61e4f-125">Pour ajouter un compte d’utilisateur par son nom d’affichage, remplissez le nom complet du compte d’utilisateur (exemple : Belinda Newman) et le nom complet du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou powerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="61e4f-125">**To add a user account by its display name**, fill in the user account display name (example: Belinda Newman) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userName="<display name of the user account to add>"
$groupName="<display name of the group>"
Add-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.DisplayName -eq $userName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="61e4f-126">Pour supprimer un compte d’utilisateur par son **UPN,** remplissez l’UPN du compte d’utilisateur (exemple : belindan@contoso.com) et le nom d’affichage du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou powerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="61e4f-126">**To remove a user account by its UPN**, fill in the user account UPN (example: belindan@contoso.com) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userUPN="<UPN of the user account to remove>"
$groupName="<display name of the group>"
Remove-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

<span data-ttu-id="61e4f-127">Pour supprimer un compte d’utilisateur par son nom d’affichage, remplissez le nom complet du compte d’utilisateur (exemple : Belinda Newman) et le nom complet du groupe, puis exécutez ces commandes dans la fenêtre PowerShell ou powerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="61e4f-127">**To remove a user account by its display name**, fill in the user account display name (example: Belinda Newman) and the group display name and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$userName="<display name of the user account to remove>"
$groupName="<display name of the group>"
Remove-MsolGroupMember -GroupMemberObjectId (Get-MsolUser | Where { $_.DisplayName -eq $userName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
```

### <a name="add-or-remove-groups-as-members-of-a-group"></a><span data-ttu-id="61e4f-128">Ajouter ou supprimer des groupes en tant que membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="61e4f-128">Add or remove groups as members of a group</span></span>

<span data-ttu-id="61e4f-129">Les groupes de sécurité peuvent contenir d’autres groupes en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="61e4f-129">Security groups can contain other groups as members.</span></span> <span data-ttu-id="61e4f-130">Toutefois, les groupes Microsoft 365 ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="61e4f-130">Microsoft 365 groups, however, cannot.</span></span> <span data-ttu-id="61e4f-131">Cette section contient des commandes PowerShell pour ajouter ou supprimer des groupes uniquement pour un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="61e4f-131">This section contains PowerShell commands to add or remove groups only for a security group.</span></span>

<span data-ttu-id="61e4f-132">Pour ajouter un groupe par son nom d’affichage, remplissez le nom complet du groupe que vous allez ajouter et le nom complet du groupe qui contiendra le groupe de membres et exécuterez ces commandes dans la fenêtre PowerShell ou l’ISE PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61e4f-132">**To add a group by its display name**, fill in the display name of the group you’re going to add and the display name of the group that will contain the member group and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group that will contain the member group>"
Add-MsolGroupMember -GroupMemberObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID -GroupMemberType Group
```

<span data-ttu-id="61e4f-133">Pour supprimer un groupe par son nom d’affichage, remplissez le nom complet du groupe que vous allez supprimer et le nom complet du groupe qui contiendra le groupe de membres et exécutez ces commandes dans la fenêtre PowerShell ou l’ISE PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61e4f-133">**To remove a group by its display name**, fill in the display name of the group you’re going to remove and the display name of the group that will contain the member group and run these commands in the PowerShell window or the PowerShell ISE.</span></span>

```powershell
$groupMemberName="<display name of the group to add>"
$groupName="<display name of the group contains the member group>"
Remove-MsolGroupMember -GroupMemberObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $groupName }).ObjectID -GroupMemberType Group
```

## <a name="see-also"></a><span data-ttu-id="61e4f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61e4f-134">See also</span></span>

[<span data-ttu-id="61e4f-135">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="61e4f-135">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="61e4f-136">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="61e4f-136">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="61e4f-137">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="61e4f-137">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)