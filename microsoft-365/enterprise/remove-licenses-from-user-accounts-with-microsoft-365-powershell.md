---
title: Suppression des licences Microsoft 365 des comptes d’utilisateur avec PowerShell
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
- LIL_Placement
- O365ITProTrain
ms.assetid: e7e4dc5e-e299-482c-9414-c265e145134f
description: Explique comment utiliser PowerShell pour supprimer des licences Microsoft 365 qui ont été précédemment attribuées à des utilisateurs.
ms.openlocfilehash: 7651f300dbf7a57ce163096d500401365e624663
ms.sourcegitcommit: c1ee4ed3c5826872b57339e1e1aa33b4d2209711
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2020
ms.locfileid: "48235453"
---
# <a name="remove-microsoft-365-licenses-from-user-accounts-with-powershell"></a><span data-ttu-id="87226-103">Suppression des licences Microsoft 365 des comptes d’utilisateur avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="87226-103">Remove Microsoft 365 licenses from user accounts with PowerShell</span></span>

<span data-ttu-id="87226-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="87226-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

>[!Note]
><span data-ttu-id="87226-105">[Découvrez comment supprimer des licences de comptes d’utilisateur](https://docs.microsoft.com/microsoft-365/admin/manage/remove-licenses-from-users) avec le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="87226-105">[Learn how to remove licenses from user accounts](https://docs.microsoft.com/microsoft-365/admin/manage/remove-licenses-from-users) with the Microsoft 365 admin center.</span></span> <span data-ttu-id="87226-106">Pour obtenir la liste des ressources supplémentaires, consultez la rubrique [gérer les utilisateurs et les groupes](https://docs.microsoft.com/microsoft-365/admin/add-users/).</span><span class="sxs-lookup"><span data-stu-id="87226-106">For a list of additional resources, see [Manage users and groups](https://docs.microsoft.com/microsoft-365/admin/add-users/).</span></span>
>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="87226-107">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="87226-107">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="87226-108">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="87226-108">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>

<span data-ttu-id="87226-109">Ensuite, répertoriez les plans de licence pour votre client à l’aide de cette commande.</span><span class="sxs-lookup"><span data-stu-id="87226-109">Next, list the license plans for your tenant with this command.</span></span>

```powershell
Get-AzureADSubscribedSku | Select SkuPartNumber
```

<span data-ttu-id="87226-110">Ensuite, obtenez le nom de connexion du compte pour lequel vous souhaitez supprimer une licence, également appelée nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="87226-110">Next, get the sign-in name of the account for which you want remove a license, also known as the user principal name (UPN).</span></span>

<span data-ttu-id="87226-111">Enfin, spécifiez les noms de connexion et de plan de licence de l’utilisateur, supprimez les caractères « < » et « > », puis exécutez ces commandes.</span><span class="sxs-lookup"><span data-stu-id="87226-111">Finally, specify the user sign-in and license plan names, remove the "<" and ">" characters, and run these commands.</span></span>

```powershell
$userUPN="<user sign-in name (UPN)>"
$planName="<license plan name from the list of license plans>"
$license = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$License.RemoveLicenses = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value $planName -EQ).SkuID
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $license
```

<span data-ttu-id="87226-112">Pour supprimer toutes les licences pour un compte d’utilisateur spécifique, spécifiez le nom de connexion de l’utilisateur, supprimez les caractères « < » et « > », puis exécutez ces commandes.</span><span class="sxs-lookup"><span data-stu-id="87226-112">To remove all of the licenses for a specific user account, specify the user sign-in name, remove the "<" and ">" characters, and run these commands.</span></span>

```powershell
$userUPN="<user sign-in name (UPN)>"
$licensePlanList = Get-AzureADSubscribedSku
$userList = Get-AzureADUser -ObjectID $userUPN | Select -ExpandProperty AssignedLicenses | Select SkuID
if($userList.Count -ne 0) {
if($userList -is [array]) {
for ($i=0; $i -lt $userList.Count; $i++) {
$license = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$licenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$license.SkuId = $userList[$i].SkuId
$licenses.AddLicenses = $license
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $licenses
$Licenses.AddLicenses = @()
$Licenses.RemoveLicenses =  (Get-AzureADSubscribedSku | Where-Object -Property SkuID -Value $userList[$i].SkuId -EQ).SkuID
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $licenses
}
} else {
$license = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$licenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$license.SkuId = $userList.SkuId
$licenses.AddLicenses = $license
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $licenses
$Licenses.AddLicenses = @()
$Licenses.RemoveLicenses =  (Get-AzureADSubscribedSku | Where-Object -Property SkuID -Value $userList.SkuId -EQ).SkuID
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $licenses
}}
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="87226-113">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="87226-113">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="87226-114">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="87226-114">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>
   
<span data-ttu-id="87226-115">Pour afficher les informations sur le plan de gestion des licences (**AccountSkuID**) dans votre organisation, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="87226-115">To view the licensing plan (**AccountSkuID**) information in your organization, see the following topics:</span></span>
    
  - [<span data-ttu-id="87226-116">Afficher les licences et les services avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="87226-116">View licenses and services with PowerShell</span></span>](view-licenses-and-services-with-microsoft-365-powershell.md)
    
  - [<span data-ttu-id="87226-117">Afficher les détails de service et de licence de compte avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="87226-117">View account license and service details with PowerShell</span></span>](view-account-license-and-service-details-with-microsoft-365-powershell.md)
    
<span data-ttu-id="87226-118">Si vous utilisez la cmdlet **Get-MsolUser** sans utiliser le paramètre _-All_, seuls les 500 premiers comptes sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="87226-118">If you use the **Get-MsolUser** cmdlet without using the _-All_ parameter, only the first 500 accounts are returned.</span></span>
    
### <a name="removing-licenses-from-user-accounts"></a><span data-ttu-id="87226-119">Suppression de licences de comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="87226-119">Removing licenses from user accounts</span></span>

<span data-ttu-id="87226-120">Pour supprimer des licences à partir d’un compte d’utilisateur existant, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="87226-120">To remove licenses from an existing user account, use the following syntax:</span></span>
  
```powershell
Set-MsolUserLicense -UserPrincipalName <Account> -RemoveLicenses "<AccountSkuId1>", "<AccountSkuId2>"...
```

>[!Note]
><span data-ttu-id="87226-121">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="87226-121">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="87226-122">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="87226-122">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

<span data-ttu-id="87226-123">Cet exemple supprime la licence **litwareinc : ENTERPRISEPACK** (Office 365 Enterprise E3) du compte d’utilisateur BelindaN@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="87226-123">This example removes the **litwareinc:ENTERPRISEPACK** (Office 365 Enterprise E3) license from the user account BelindaN@litwareinc.com.</span></span>
  
```powershell
Set-MsolUserLicense -UserPrincipalName belindan@litwareinc.com -RemoveLicenses "litwareinc:ENTERPRISEPACK"
```

>[!Note]
><span data-ttu-id="87226-124">Vous ne pouvez pas utiliser l' `Set-MsolUserLicense` applet de commande pour annuler l’affectation des utilisateurs des licences *annulées* .</span><span class="sxs-lookup"><span data-stu-id="87226-124">You cannot use the `Set-MsolUserLicense` cmdlet to unassign users from *canceled* licenses.</span></span> <span data-ttu-id="87226-125">Vous devez effectuer cette opération individuellement pour chaque compte d’utilisateur dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="87226-125">You must do this individually for each user account in the Microsoft 365 admin center.</span></span>
>

<span data-ttu-id="87226-126">Pour supprimer toutes les licences d’un groupe d’utilisateurs sous licence existants, utilisez l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="87226-126">To remove all licenses from a group of existing licensed users, use either of the following methods:</span></span>
  
- <span data-ttu-id="87226-127">**Filtrer les comptes en fonction d’un attribut de compte existant** Pour ce faire, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="87226-127">**Filter the accounts based on an existing account attribute** To do this, use the following syntax:</span></span>
    
```powershell
$userArray = Get-MsolUser -All <FilterableAttributes> | where {$_.isLicensed -eq $true}
for ($i=0; $i -lt $userArray.Count; $i++)
{
Set-MsolUserLicense -UserPrincipalName $userArray[$i].UserPrincipalName -RemoveLicenses $userArray[$i].licenses.accountskuid
}
```

<span data-ttu-id="87226-128">Cet exemple supprime toutes les licences de tous les comptes d’utilisateur du département des ventes aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="87226-128">This example removes all licenses from all user accounts in the Sales department in the United States.</span></span>
    
```powershell
$userArray = Get-MsolUser -All -Department "Sales" -UsageLocation "US" | where {$_.isLicensed -eq $true}
for ($i=0; $i -lt $userArray.Count; $i++)
{
Set-MsolUserLicense -UserPrincipalName $userArray[$i].UserPrincipalName -RemoveLicenses $userArray[$i].licenses.accountskuid
}
```

- <span data-ttu-id="87226-129">**Utiliser une liste de comptes spécifiques pour une licence spécifique** Pour ce faire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="87226-129">**Use a list of specific accounts for a specific license** To do this, perform the following steps:</span></span>
    
1. <span data-ttu-id="87226-130">Créez et enregistrez un fichier texte contenant un seul compte sur chaque ligne comme suit :</span><span class="sxs-lookup"><span data-stu-id="87226-130">Create and save a text file that contains one account on each line like this:</span></span>
    
  ```powershell
akol@contoso.com
tjohnston@contoso.com
kakers@contoso.com
  ```

2. <span data-ttu-id="87226-131">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="87226-131">Use the following syntax:</span></span>
    
  ```powershell
  $x=Get-Content "<FileNameAndPath>"
  for ($i=0; $i -lt $x.Count; $i++)
  {
  Set-MsolUserLicense -UserPrincipalName $x[$i] -RemoveLicenses "<AccountSkuId1>","<AccountSkuId2>"...
  }
  ```
<span data-ttu-id="87226-132">Cet exemple supprime la licence **litwareinc : ENTERPRISEPACK** (Office 365 Enterprise E3) des comptes d’utilisateur définis dans le fichier texte C:\My Documents\Accounts.txt.</span><span class="sxs-lookup"><span data-stu-id="87226-132">This example removes the **litwareinc:ENTERPRISEPACK** (Office 365 Enterprise E3) license from the user accounts defined in the text file C:\My Documents\Accounts.txt.</span></span>
    
  ```powershell
  $x=Get-Content "C:\My Documents\Accounts.txt"
  for ($i=0; $i -lt $x.Count; $i++)
  {
  Set-MsolUserLicense -UserPrincipalName $x[$i] -RemoveLicenses "litwareinc:ENTERPRISEPACK"
  }
  ```

<span data-ttu-id="87226-133">Pour supprimer toutes les licences de tous les comptes d’utilisateur existants, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="87226-133">To remove all licenses from all existing user accounts, use the following syntax:</span></span>
  
```powershell
$userArray = Get-MsolUser -All | where {$_.isLicensed -eq $true}
for ($i=0; $i -lt $userArray.Count; $i++)
{
Set-MsolUserLicense -UserPrincipalName $userArray[$i].UserPrincipalName -RemoveLicenses $userArray[$i].licenses.accountskuid
}
```

<span data-ttu-id="87226-134">Une autre façon de libérer une licence consiste à supprimer le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="87226-134">Another way to free up a license is by deleting the user account.</span></span> <span data-ttu-id="87226-135">Pour plus d’informations, consultez la rubrique [Delete and Restore User Accounts with PowerShell](delete-and-restore-user-accounts-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="87226-135">For more information, see [Delete and restore user accounts with PowerShell](delete-and-restore-user-accounts-with-microsoft-365-powershell.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="87226-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87226-136">See also</span></span>

[<span data-ttu-id="87226-137">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="87226-137">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="87226-138">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="87226-138">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="87226-139">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="87226-139">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)

