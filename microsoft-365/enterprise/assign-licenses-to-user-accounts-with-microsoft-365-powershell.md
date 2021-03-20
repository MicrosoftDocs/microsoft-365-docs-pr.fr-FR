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
description: Dans cet article, découvrez comment utiliser PowerShell pour attribuer une licence Microsoft 365 à des utilisateurs sans licence.
ms.openlocfilehash: 5fb5f9095d4f732b0bf23f26eebb22eff608b48c
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50905463"
---
# <a name="assign-microsoft-365-licenses-to-user-accounts-with-powershell"></a><span data-ttu-id="cad1d-103">Attribuer des licences Microsoft 365 à des comptes d’utilisateur avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="cad1d-103">Assign Microsoft 365 licenses to user accounts with PowerShell</span></span>

<span data-ttu-id="cad1d-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="cad1d-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="cad1d-105">Les utilisateurs ne peuvent pas utiliser les services Microsoft 365 tant que leur compte n’a pas reçu de licence d’un plan de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="cad1d-105">Users can't use any Microsoft 365 services until their account has been assigned a license from a licensing plan.</span></span> <span data-ttu-id="cad1d-106">Vous pouvez utiliser PowerShell pour attribuer rapidement des licences à des comptes sans licence.</span><span class="sxs-lookup"><span data-stu-id="cad1d-106">You can use PowerShell to quickly assign licenses to unlicensed accounts.</span></span> 

<span data-ttu-id="cad1d-107">Un emplacement doit d’abord être affecté aux comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cad1d-107">User accounts must first be assigned a location.</span></span> <span data-ttu-id="cad1d-108">La spécification d’un emplacement est une partie obligatoire de la création d’un compte d’utilisateur dans le Centre d’administration [Microsoft 365.](../admin/add-users/add-users.md)</span><span class="sxs-lookup"><span data-stu-id="cad1d-108">Specifying a location is a required part of creating a new user account in the [Microsoft 365 admin center](../admin/add-users/add-users.md).</span></span> 

<span data-ttu-id="cad1d-109">Les comptes synchronisés à partir de vos services de domaine Active Directory locaux n’ont pas d’emplacement spécifié par défaut.</span><span class="sxs-lookup"><span data-stu-id="cad1d-109">Accounts synchronized from your on-premises Active Directory Domain Services do not by default have a location specified.</span></span> <span data-ttu-id="cad1d-110">Vous pouvez configurer un emplacement pour ces comptes à partir de :</span><span class="sxs-lookup"><span data-stu-id="cad1d-110">You can configure a location for these accounts from:</span></span>

- <span data-ttu-id="cad1d-111">Le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cad1d-111">The Microsoft 365 admin center</span></span>
 - [<span data-ttu-id="cad1d-112">PowerShell</span><span class="sxs-lookup"><span data-stu-id="cad1d-112">PowerShell</span></span>](configure-user-account-properties-with-microsoft-365-powershell.md)
 - <span data-ttu-id="cad1d-113">Le [portail Azure](/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal) (**Utilisateurs Active Directory**> compte d’utilisateur > informations de contact du profil  >   Pays ou   >    >  **région**).</span><span class="sxs-lookup"><span data-stu-id="cad1d-113">The [Azure portal](/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal) (**Active Directory** > **Users**  > user account > **Profile** > **Contact info** > **Country or region**).</span></span>

>[!Note]
><span data-ttu-id="cad1d-114">[Découvrez comment attribuer des licences à des comptes d’utilisateurs](../admin/manage/assign-licenses-to-users.md) à l’aide du Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cad1d-114">[Learn how to assign licenses to user accounts](../admin/manage/assign-licenses-to-users.md) with the Microsoft 365 admin center.</span></span> <span data-ttu-id="cad1d-115">Pour obtenir la liste des ressources supplémentaires, voir [Gérer les utilisateurs et les groupes.](../admin/add-users/index.yml)</span><span class="sxs-lookup"><span data-stu-id="cad1d-115">For a list of additional resources, see [Manage users and groups](../admin/add-users/index.yml).</span></span>
>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="cad1d-116">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="cad1d-116">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="cad1d-117">Tout [d’abord, connectez-vous à votre client Microsoft 365.](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="cad1d-117">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  

<span data-ttu-id="cad1d-118">Ensuite, listez les plans de licence pour votre client avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="cad1d-118">Next, list the license plans for your tenant with this command.</span></span>

```powershell
Get-AzureADSubscribedSku | Select SkuPartNumber
```

<span data-ttu-id="cad1d-119">Ensuite, obtenez le nom de la signature du compte auquel vous souhaitez ajouter une licence, également appelée nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="cad1d-119">Next, get the sign-in name of the account to which you want add a license, also known as the user principal name (UPN).</span></span>

<span data-ttu-id="cad1d-120">Ensuite, assurez-vous qu’un emplacement d’utilisation est affecté au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cad1d-120">Next, ensure that the user account has a usage location assigned.</span></span>

```powershell
Get-AzureADUser -ObjectID <user sign-in name (UPN)> | Select DisplayName, UsageLocation
```

<span data-ttu-id="cad1d-121">Si aucun emplacement d’utilisation n’est affecté, vous pouvez en attribuer un avec les commandes ci-après :</span><span class="sxs-lookup"><span data-stu-id="cad1d-121">If there is no usage location assigned, you can assign one with these commands:</span></span>

```powershell
$userUPN="<user sign-in name (UPN)>"
$userLoc="<ISO 3166-1 alpha-2 country code>"
Set-AzureADUser -ObjectID $userUPN -UsageLocation $userLoc
```

<span data-ttu-id="cad1d-122">Enfin, spécifiez le nom de la signature de l’utilisateur et le nom du plan de licence et exécutez ces commandes.</span><span class="sxs-lookup"><span data-stu-id="cad1d-122">Finally, specify the user sign-in name and license plan name and run these commands.</span></span>

```powershell
$userUPN="<user sign-in name (UPN)>"
$planName="<license plan name from the list of license plans>"
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$License.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value $planName -EQ).SkuID
$LicensesToAssign = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$LicensesToAssign.AddLicenses = $License
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $LicensesToAssign
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="cad1d-123">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cad1d-123">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="cad1d-124">Tout [d’abord, connectez-vous à votre client Microsoft 365.](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell)</span><span class="sxs-lookup"><span data-stu-id="cad1d-124">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

<span data-ttu-id="cad1d-125">Exécutez la commande pour afficher les plans de gestion des licences disponibles et le nombre de `Get-MsolAccountSku` licences disponibles dans chaque plan de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cad1d-125">Run the `Get-MsolAccountSku` command to view the available licensing plans and the number of available licenses in each plan in your organization.</span></span> <span data-ttu-id="cad1d-126">Le nombre de licences disponibles dans chaque plan **est ActiveUnits**  -  **WarningUnits**  -  **ConsumedUnits**.</span><span class="sxs-lookup"><span data-stu-id="cad1d-126">The number of available licenses in each plan is **ActiveUnits** - **WarningUnits** - **ConsumedUnits**.</span></span> <span data-ttu-id="cad1d-127">Pour plus d’informations sur les plans de gestion des licences, les licences et les services, voir Afficher les [licences et les services avec PowerShell.](view-licenses-and-services-with-microsoft-365-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="cad1d-127">For more information about licensing plans, licenses, and services, see [View licenses and services with PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span></span>

>[!Note]
><span data-ttu-id="cad1d-128">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="cad1d-128">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="cad1d-129">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cad1d-129">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

<span data-ttu-id="cad1d-130">Pour rechercher les comptes sans permis dans votre organisation, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="cad1d-130">To find the unlicensed accounts in your organization, run this command.</span></span>

```powershell
Get-MsolUser -All -UnlicensedUsersOnly
```

<span data-ttu-id="cad1d-131">Vous pouvez uniquement attribuer des licences à des comptes d’utilisateur dont la propriété **UsageLocation** est définie sur un code pays ISO 3166-1 alpha-2 valide.</span><span class="sxs-lookup"><span data-stu-id="cad1d-131">You can only assign licenses to user accounts that have the **UsageLocation** property set to a valid ISO 3166-1 alpha-2 country code.</span></span> <span data-ttu-id="cad1d-132">Par exemple, US pour les États-Unis et FR pour la France.</span><span class="sxs-lookup"><span data-stu-id="cad1d-132">For example, US for the United States, and FR for France.</span></span> <span data-ttu-id="cad1d-133">Certains services Microsoft 365 ne sont pas disponibles dans certains pays.</span><span class="sxs-lookup"><span data-stu-id="cad1d-133">Some Microsoft 365 services aren't available in certain countries.</span></span> <span data-ttu-id="cad1d-134">Pour plus d’informations, voir [à propos des restrictions de licence.](https://go.microsoft.com/fwlink/p/?LinkId=691730)</span><span class="sxs-lookup"><span data-stu-id="cad1d-134">For more information, see [About license restrictions](https://go.microsoft.com/fwlink/p/?LinkId=691730).</span></span>
    
<span data-ttu-id="cad1d-135">Pour rechercher des comptes qui n’ont pas de valeur **UsageLocation,** exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="cad1d-135">To find accounts that don't have a **UsageLocation** value, run this command.</span></span>

```powershell
Get-MsolUser -All | where {$_.UsageLocation -eq $null}
```

<span data-ttu-id="cad1d-136">Pour définir la **valeur UsageLocation** sur un compte, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="cad1d-136">To set the **UsageLocation** value on an account, run this command.</span></span>

```powershell
Set-MsolUser -UserPrincipalName "<Account>" -UsageLocation <CountryCode>
```

<span data-ttu-id="cad1d-137">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="cad1d-137">For example:</span></span>

```powershell
Set-MsolUser -UserPrincipalName "belindan@litwareinc.com" -UsageLocation US
```
    
<span data-ttu-id="cad1d-138">Si vous utilisez la cmdlet **Get-MsolUser** sans utiliser le paramètre **-All**, seuls les 500 premiers comptes sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="cad1d-138">If you use the **Get-MsolUser** cmdlet without using the **-All** parameter, only the first 500 accounts are returned.</span></span>

### <a name="assigning-licenses-to-user-accounts"></a><span data-ttu-id="cad1d-139">Attribution de licences à des comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="cad1d-139">Assigning licenses to user accounts</span></span>
    
<span data-ttu-id="cad1d-140">Pour attribuer une licence à un utilisateur, utilisez la commande suivante dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cad1d-140">To assign a license to a user, use the following command in PowerShell.</span></span>
  
```powershell
Set-MsolUserLicense -UserPrincipalName "<Account>" -AddLicenses "<AccountSkuId>"
```

<span data-ttu-id="cad1d-141">Cet exemple affecte une licence du plan de gestion des licences **litwareinc:ENTERPRISEPACK** (Office 365 Entreprise E3) à l’utilisateur sans licence **belindan \@ litwareinc.com**:</span><span class="sxs-lookup"><span data-stu-id="cad1d-141">This example assigns a license from the **litwareinc:ENTERPRISEPACK** (Office 365 Enterprise E3) licensing plan to the unlicensed user **belindan\@litwareinc.com**:</span></span>
  
```powershell
Set-MsolUserLicense -UserPrincipalName "belindan@litwareinc.com" -AddLicenses "litwareinc:ENTERPRISEPACK"
```

<span data-ttu-id="cad1d-142">Pour attribuer une licence à tous les utilisateurs sans licence, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="cad1d-142">To assign a license to all unlicensed users, run this command.</span></span>
  
```powershell
Get-MsolUser -All -UnlicensedUsersOnly [<FilterableAttributes>] | Set-MsolUserLicense -AddLicenses "<AccountSkuId>"
```
  
>[!Note]
><span data-ttu-id="cad1d-143">Vous ne pouvez pas attribuer plusieurs licences à un utilisateur à partir du même plan de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="cad1d-143">You can't assign multiple licenses to a user from the same licensing plan.</span></span> <span data-ttu-id="cad1d-144">Si le nombre de licences disponibles n’est pas suffisant, les licences sont attribuées aux utilisateurs selon leur ordre de renvoi par la cmdlet **Get-MsolUser** jusqu'à ce qu’il n’y ait plus de licence disponible.</span><span class="sxs-lookup"><span data-stu-id="cad1d-144">If you don't have enough available licenses, the licenses are assigned to users in the order that they're returned by the **Get-MsolUser** cmdlet until the available licenses run out.</span></span>
>

<span data-ttu-id="cad1d-145">Cet exemple attribue des licences du plan de gestion des licences **litwareinc:ENTERPRISEPACK** (Office 365 Entreprise E3) à tous les utilisateurs sans licence :</span><span class="sxs-lookup"><span data-stu-id="cad1d-145">This example assigns licenses from the **litwareinc:ENTERPRISEPACK** (Office 365 Enterprise E3) licensing plan to all unlicensed users:</span></span>
  
```powershell
Get-MsolUser -All -UnlicensedUsersOnly | Set-MsolUserLicense -AddLicenses "litwareinc:ENTERPRISEPACK"
```

<span data-ttu-id="cad1d-146">Cet exemple attribue ces mêmes licences à des utilisateurs sans licence dans le service Sales aux États-Unis :</span><span class="sxs-lookup"><span data-stu-id="cad1d-146">This example assigns those same licenses to unlicensed users in the Sales department in the United States:</span></span>
  
```powershell
Get-MsolUser -All -Department "Sales" -UsageLocation "US" -UnlicensedUsersOnly | Set-MsolUserLicense -AddLicenses "litwareinc:ENTERPRISEPACK"
```
  
## <a name="move-a-user-to-a-different-subscription-license-plan-with-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="cad1d-147">Déplacer un utilisateur vers un autre abonnement (plan de licence) avec le module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="cad1d-147">Move a user to a different subscription (license plan) with the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="cad1d-148">Tout [d’abord, connectez-vous à votre client Microsoft 365.](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="cad1d-148">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
<span data-ttu-id="cad1d-149">Ensuite, obtenez le nom de la signature du compte d’utilisateur pour lequel vous souhaitez changer d’abonnement, également appelé nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="cad1d-149">Next, get the sign-in name of the user account for which you want switch subscriptions, also known as the user principal name (UPN).</span></span>

<span data-ttu-id="cad1d-150">Ensuite, listez les abonnements (plans de licence) de votre client avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="cad1d-150">Next, list the subscriptions (license plans) for your tenant with this command.</span></span>

```powershell
Get-AzureADSubscribedSku | Select SkuPartNumber
```

<span data-ttu-id="cad1d-151">Ensuite, listez les abonnements dont dispose actuellement le compte d’utilisateur avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="cad1d-151">Next, list the subscriptions that the user account currently has with these commands.</span></span>

```powershell
$userUPN="<user account UPN>"
$licensePlanList = Get-AzureADSubscribedSku
$userList = Get-AzureADUser -ObjectID $userUPN | Select -ExpandProperty AssignedLicenses | Select SkuID 
$userList | ForEach { $sku=$_.SkuId ; $licensePlanList | ForEach { If ( $sku -eq $_.ObjectId.substring($_.ObjectId.length - 36, 36) ) { Write-Host $_.SkuPartNumber } } }
```

<span data-ttu-id="cad1d-152">Identifiez l’abonnement actuel de l’utilisateur (l’abonnement FROM) et l’abonnement vers lequel l’utilisateur est en train de déplacer (l’abonnement TO).</span><span class="sxs-lookup"><span data-stu-id="cad1d-152">Identify the subscription the user currently has (the FROM subscription) and the subscription to which the user is moving (the TO subscription).</span></span>

<span data-ttu-id="cad1d-153">Enfin, spécifiez les noms des abonnements TO et FROM (numéros de partie SKU) et exécutez ces commandes.</span><span class="sxs-lookup"><span data-stu-id="cad1d-153">Finally, specify the TO and FROM subscription names (SKU part numbers) and run these commands.</span></span>

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

<span data-ttu-id="cad1d-154">Vous pouvez vérifier la modification de l’abonnement pour le compte d’utilisateur avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="cad1d-154">You can verify the change in subscription for the user account with these commands.</span></span>

```powershell
$licensePlanList = Get-AzureADSubscribedSku
$userList = Get-AzureADUser -ObjectID $userUPN | Select -ExpandProperty AssignedLicenses | Select SkuID 
$userList | ForEach { $sku=$_.SkuId ; $licensePlanList | ForEach { If ( $sku -eq $_.ObjectId.substring($_.ObjectId.length - 36, 36) ) { Write-Host $_.SkuPartNumber } } }
```

## <a name="see-also"></a><span data-ttu-id="cad1d-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cad1d-155">See also</span></span>

[<span data-ttu-id="cad1d-156">Gérer les comptes d’utilisateurs, les licences et les groupes avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="cad1d-156">Manage user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="cad1d-157">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="cad1d-157">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="cad1d-158">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cad1d-158">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)