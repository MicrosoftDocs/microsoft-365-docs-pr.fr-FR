---
title: Attribuer des licences Microsoft 365 à des comptes d’utilisateur avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/23/2020
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- Ent_Office_Other
- LIL_Placement
- PowerShell
- O365ITProTrain
- seo-marvel-apr2020
ms.assetid: ba235f4f-e640-4360-81ea-04507a3a70be
search.appverid:
- MET150
description: Dans cet article, Découvrez comment utiliser PowerShell pour attribuer une licence Microsoft 365 à des utilisateurs sans licence.
ms.openlocfilehash: f042f8109bf9ac9b634bc66509c60a5181fb1af6
ms.sourcegitcommit: c1ee4ed3c5826872b57339e1e1aa33b4d2209711
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2020
ms.locfileid: "48235617"
---
# <a name="assign-microsoft-365-licenses-to-user-accounts-with-powershell"></a><span data-ttu-id="a92ad-103">Attribuer des licences Microsoft 365 à des comptes d’utilisateur avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="a92ad-103">Assign Microsoft 365 licenses to user accounts with PowerShell</span></span>

<span data-ttu-id="a92ad-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="a92ad-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="a92ad-105">Les utilisateurs ne peuvent pas utiliser les services Microsoft 365 tant que leur compte n’a pas reçu une licence d’un plan de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="a92ad-105">Users can't use any Microsoft 365 services until their account has been assigned a license from a licensing plan.</span></span> <span data-ttu-id="a92ad-106">Vous pouvez utiliser PowerShell pour affecter rapidement des licences à des comptes sans licence.</span><span class="sxs-lookup"><span data-stu-id="a92ad-106">You can use PowerShell to quickly assign licenses to unlicensed accounts.</span></span> 

>[!Note]
><span data-ttu-id="a92ad-107">Un emplacement doit être attribué aux comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a92ad-107">User accounts must be assigned a location.</span></span> <span data-ttu-id="a92ad-108">Vous pouvez effectuer cette opération à partir des propriétés d’un compte d’utilisateur dans le centre d’administration 365 de Microsoft ou à partir de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a92ad-108">You can do this from the properties of a user account in the Microsoft 365 admin center or from PowerShell.</span></span>
>

>[!Note]
><span data-ttu-id="a92ad-109">[Découvrez comment attribuer des licences à des comptes d’utilisateur](https://docs.microsoft.com/microsoft-365/admin/manage/assign-licenses-to-users) avec le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a92ad-109">[Learn how to assign licenses to user accounts](https://docs.microsoft.com/microsoft-365/admin/manage/assign-licenses-to-users) with the Microsoft 365 admin center.</span></span> <span data-ttu-id="a92ad-110">Pour obtenir la liste des ressources supplémentaires, consultez la rubrique [gérer les utilisateurs et les groupes](https://docs.microsoft.com/microsoft-365/admin/add-users/).</span><span class="sxs-lookup"><span data-stu-id="a92ad-110">For a list of additional resources, see [Manage users and groups](https://docs.microsoft.com/microsoft-365/admin/add-users/).</span></span>
>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="a92ad-111">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="a92ad-111">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="a92ad-112">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="a92ad-112">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  

<span data-ttu-id="a92ad-113">Ensuite, répertoriez les plans de licence pour votre client à l’aide de cette commande.</span><span class="sxs-lookup"><span data-stu-id="a92ad-113">Next, list the license plans for your tenant with this command.</span></span>

```powershell
Get-AzureADSubscribedSku | Select SkuPartNumber
```

<span data-ttu-id="a92ad-114">Ensuite, obtenez le nom de connexion du compte auquel vous souhaitez ajouter une licence, également appelé nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="a92ad-114">Next, get the sign-in name of the account to which you want add a license, also known as the user principal name (UPN).</span></span>

<span data-ttu-id="a92ad-115">Ensuite, vérifiez que l’emplacement d’utilisation est affecté au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a92ad-115">Next, ensure that the user account has a usage location assigned.</span></span>

```powershell
Get-AzureADUser -ObjectID <user sign-in name (UPN)> | Select DisplayName, UsageLocation
```

<span data-ttu-id="a92ad-116">S’il n’y a pas d’emplacement d’utilisation attribué, vous pouvez en affecter un à l’aide des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a92ad-116">If there is no usage location assigned, you can assign one with these commands:</span></span>

```powershell
$userUPN="<user sign-in name (UPN)>"
$userLoc="<ISO 3166-1 alpha-2 country code>"
Set-AzureADUser -ObjectID $userUPN -UsageLocation $userLoc
```

<span data-ttu-id="a92ad-117">Enfin, spécifiez le nom de connexion de l’utilisateur et le nom du plan de licence et exécutez ces commandes.</span><span class="sxs-lookup"><span data-stu-id="a92ad-117">Finally, specify the user sign-in name and license plan name and run these commands.</span></span>

```powershell
$userUPN="<user sign-in name (UPN)>"
$planName="<license plan name from the list of license plans>"
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$License.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value $planName -EQ).SkuID
$LicensesToAssign = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$LicensesToAssign.AddLicenses = $License
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $LicensesToAssign
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="a92ad-118">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a92ad-118">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="a92ad-119">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="a92ad-119">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

<span data-ttu-id="a92ad-120">Exécutez la `Get-MsolAccountSku` commande pour afficher les plans de gestion des licences disponibles et le nombre de licences disponibles dans chaque plan de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a92ad-120">Run the `Get-MsolAccountSku` command to view the available licensing plans and the number of available licenses in each plan in your organization.</span></span> <span data-ttu-id="a92ad-121">Le nombre de licences disponibles pour chaque plan est **ActiveUnits**  -  **WarningUnits**  -  **ConsumedUnits**.</span><span class="sxs-lookup"><span data-stu-id="a92ad-121">The number of available licenses in each plan is **ActiveUnits** - **WarningUnits** - **ConsumedUnits**.</span></span> <span data-ttu-id="a92ad-122">Pour plus d’informations sur les plans de licence, les licences et les services, voir [View licenses and Services with PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="a92ad-122">For more information about licensing plans, licenses, and services, see [View licenses and services with PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span></span>

>[!Note]
><span data-ttu-id="a92ad-123">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="a92ad-123">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="a92ad-124">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a92ad-124">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

<span data-ttu-id="a92ad-125">Pour rechercher les comptes sans licence dans votre organisation, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="a92ad-125">To find the unlicensed accounts in your organization, run this command.</span></span>

```powershell
Get-MsolUser -All -UnlicensedUsersOnly
```

<span data-ttu-id="a92ad-126">Vous pouvez uniquement attribuer des licences à des comptes d’utilisateur dont la propriété **UsageLocation** est définie sur un code ISO 3166-1 alpha-2 valide.</span><span class="sxs-lookup"><span data-stu-id="a92ad-126">You can only assign licenses to user accounts that have the **UsageLocation** property set to a valid ISO 3166-1 alpha-2 country code.</span></span> <span data-ttu-id="a92ad-127">Par exemple, US pour les États-Unis et FR pour la France.</span><span class="sxs-lookup"><span data-stu-id="a92ad-127">For example, US for the United States, and FR for France.</span></span> <span data-ttu-id="a92ad-128">Certains services Microsoft 365 ne sont pas disponibles dans certains pays.</span><span class="sxs-lookup"><span data-stu-id="a92ad-128">Some Microsoft 365 services aren't available in certain countries.</span></span> <span data-ttu-id="a92ad-129">Pour plus d’informations, consultez la rubrique [à propos des restrictions de licence](https://go.microsoft.com/fwlink/p/?LinkId=691730).</span><span class="sxs-lookup"><span data-stu-id="a92ad-129">For more information, see [About license restrictions](https://go.microsoft.com/fwlink/p/?LinkId=691730).</span></span>
    
<span data-ttu-id="a92ad-130">Pour rechercher les comptes qui n’ont pas de valeur **UsageLocation** , exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="a92ad-130">To find accounts that don't have a **UsageLocation** value, run this command.</span></span>

```powershell
Get-MsolUser -All | where {$_.UsageLocation -eq $null}
```

<span data-ttu-id="a92ad-131">Pour définir la valeur **UsageLocation** sur un compte, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="a92ad-131">To set the **UsageLocation** value on an account, run this command.</span></span>

```powershell
Set-MsolUser -UserPrincipalName "<Account>" -UsageLocation <CountryCode>
```

<span data-ttu-id="a92ad-132">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a92ad-132">For example:</span></span>

```powershell
Set-MsolUser -UserPrincipalName "belindan@litwareinc.com" -UsageLocation US
```
    
<span data-ttu-id="a92ad-133">Si vous utilisez la cmdlet **Get-MsolUser** sans utiliser le paramètre **-All**, seuls les 500 premiers comptes sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="a92ad-133">If you use the **Get-MsolUser** cmdlet without using the **-All** parameter, only the first 500 accounts are returned.</span></span>

### <a name="assigning-licenses-to-user-accounts"></a><span data-ttu-id="a92ad-134">Attribution de licences à des comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a92ad-134">Assigning licenses to user accounts</span></span>
    
<span data-ttu-id="a92ad-135">Pour attribuer une licence à un utilisateur, utilisez la commande suivante dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a92ad-135">To assign a license to a user, use the following command in PowerShell.</span></span>
  
```powershell
Set-MsolUserLicense -UserPrincipalName "<Account>" -AddLicenses "<AccountSkuId>"
```

<span data-ttu-id="a92ad-136">Cet exemple attribue une licence du plan de gestion des licences **litwareinc : ENTERPRISEPACK** (Office 365 Enterprise E3) à l’utilisateur sans licence \*\* \@ litwareinc.com\*\*:</span><span class="sxs-lookup"><span data-stu-id="a92ad-136">This example assigns a license from the **litwareinc:ENTERPRISEPACK** (Office 365 Enterprise E3) licensing plan to the unlicensed user **belindan\@litwareinc.com**:</span></span>
  
```powershell
Set-MsolUserLicense -UserPrincipalName "belindan@litwareinc.com" -AddLicenses "litwareinc:ENTERPRISEPACK"
```

<span data-ttu-id="a92ad-137">Pour attribuer une licence à tous les utilisateurs sans licence, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="a92ad-137">To assign a license to all unlicensed users, run this command.</span></span>
  
```powershell
Get-MsolUser -All -UnlicensedUsersOnly [<FilterableAttributes>] | Set-MsolUserLicense -AddLicenses "<AccountSkuId>"
```
  
>[!Note]
><span data-ttu-id="a92ad-138">Vous ne pouvez pas attribuer plusieurs licences à un utilisateur à partir du même plan de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="a92ad-138">You can't assign multiple licenses to a user from the same licensing plan.</span></span> <span data-ttu-id="a92ad-139">Si le nombre de licences disponibles n’est pas suffisant, les licences sont attribuées aux utilisateurs selon leur ordre de renvoi par la cmdlet **Get-MsolUser** jusqu'à ce qu’il n’y ait plus de licence disponible.</span><span class="sxs-lookup"><span data-stu-id="a92ad-139">If you don't have enough available licenses, the licenses are assigned to users in the order that they're returned by the **Get-MsolUser** cmdlet until the available licenses run out.</span></span>
>

<span data-ttu-id="a92ad-140">Cet exemple attribue des licences à tous les utilisateurs sans licence à partir du plan de gestion des licences **litwareinc : ENTERPRISEPACK** (Office 365 Enterprise E3) :</span><span class="sxs-lookup"><span data-stu-id="a92ad-140">This example assigns licenses from the **litwareinc:ENTERPRISEPACK** (Office 365 Enterprise E3) licensing plan to all unlicensed users:</span></span>
  
```powershell
Get-MsolUser -All -UnlicensedUsersOnly | Set-MsolUserLicense -AddLicenses "litwareinc:ENTERPRISEPACK"
```

<span data-ttu-id="a92ad-141">Cet exemple attribue ces mêmes licences aux utilisateurs sans licence du département des ventes aux États-Unis :</span><span class="sxs-lookup"><span data-stu-id="a92ad-141">This example assigns those same licenses to unlicensed users in the Sales department in the United States:</span></span>
  
```powershell
Get-MsolUser -All -Department "Sales" -UsageLocation "US" -UnlicensedUsersOnly | Set-MsolUserLicense -AddLicenses "litwareinc:ENTERPRISEPACK"
```
  
## <a name="move-a-user-to-a-different-subscription-license-plan-with-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="a92ad-142">Déplacer un utilisateur vers un autre abonnement (plan de licence) avec le module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="a92ad-142">Move a user to a different subscription (license plan) with the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="a92ad-143">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="a92ad-143">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
<span data-ttu-id="a92ad-144">Ensuite, obtenez le nom de connexion du compte d’utilisateur pour lequel vous souhaitez des abonnements de commutateur, également appelé nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="a92ad-144">Next, get the sign-in name of the user account for which you want switch subscriptions, also known as the user principal name (UPN).</span></span>

<span data-ttu-id="a92ad-145">Ensuite, répertoriez les abonnements (plans de licence) de votre client à l’aide de cette commande.</span><span class="sxs-lookup"><span data-stu-id="a92ad-145">Next, list the subscriptions (license plans) for your tenant with this command.</span></span>

```powershell
Get-AzureADSubscribedSku | Select SkuPartNumber
```

<span data-ttu-id="a92ad-146">Ensuite, répertoriez les abonnements que le compte d’utilisateur possède actuellement avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="a92ad-146">Next, list the subscriptions that the user account currently has with these commands.</span></span>

```powershell
$userUPN="<user account UPN>"
$licensePlanList = Get-AzureADSubscribedSku
$userList = Get-AzureADUser -ObjectID $userUPN | Select -ExpandProperty AssignedLicenses | Select SkuID 
$userList | ForEach { $sku=$_.SkuId ; $licensePlanList | ForEach { If ( $sku -eq $_.ObjectId.substring($_.ObjectId.length - 36, 36) ) { Write-Host $_.SkuPartNumber } } }
```

<span data-ttu-id="a92ad-147">Identifiez l’abonnement dont dispose l’utilisateur (abonnement FROM) et l’abonnement que l’utilisateur déplace (l’abonnement à).</span><span class="sxs-lookup"><span data-stu-id="a92ad-147">Identify the subscription the user currently has (the FROM subscription) and the subscription to which the user is moving (the TO subscription).</span></span>

<span data-ttu-id="a92ad-148">Enfin, spécifiez les noms d’abonnement à et à (numéros de référence SKU) et exécutez ces commandes.</span><span class="sxs-lookup"><span data-stu-id="a92ad-148">Finally, specify the TO and FROM subscription names (SKU part numbers) and run these commands.</span></span>

```powershell
$subscriptionFrom="<SKU part number of the current subscription>"
$subscriptionTo="<SKU part number of the new subscription>"
# Unassign
$license = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$licenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$license.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value $subscriptionFrom -EQ).SkuID
$licenses.AddLicenses = $license
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $licenses
$licenses.AddLicenses = @()
$licenses.RemoveLicenses =  (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value $subscriptionFrom -EQ).SkuID
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $licenses
# Assign
$license.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value $subscriptionTo -EQ).SkuID
$licenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$licenses.AddLicenses = $License
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $licenses
```

<span data-ttu-id="a92ad-149">Vous pouvez vérifier la modification de l’abonnement pour le compte d’utilisateur à l’aide de ces commandes.</span><span class="sxs-lookup"><span data-stu-id="a92ad-149">You can verify the change in subscription for the user account with these commands.</span></span>

```powershell
$licensePlanList = Get-AzureADSubscribedSku
$userList = Get-AzureADUser -ObjectID $userUPN | Select -ExpandProperty AssignedLicenses | Select SkuID 
$userList | ForEach { $sku=$_.SkuId ; $licensePlanList | ForEach { If ( $sku -eq $_.ObjectId.substring($_.ObjectId.length - 36, 36) ) { Write-Host $_.SkuPartNumber } } }
```

## <a name="see-also"></a><span data-ttu-id="a92ad-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a92ad-150">See also</span></span>

[<span data-ttu-id="a92ad-151">Gérer les comptes d’utilisateurs, les licences et les groupes avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="a92ad-151">Manage user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="a92ad-152">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a92ad-152">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="a92ad-153">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a92ad-153">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
