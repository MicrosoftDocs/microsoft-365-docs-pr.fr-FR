---
title: Attribuez Microsoft 365 licences aux comptes utilisateur avec PowerShell
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
description: Dans cet article, apprenez à utiliser PowerShell pour attribuer une licence Microsoft 365 aux utilisateurs non autorisés.
ms.openlocfilehash: 6d7e005aff018394810082de57c68ea289057f8e
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572620"
---
# <a name="assign-microsoft-365-licenses-to-user-accounts-with-powershell"></a><span data-ttu-id="fe31d-103">Attribuez Microsoft 365 licences aux comptes utilisateur avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe31d-103">Assign Microsoft 365 licenses to user accounts with PowerShell</span></span>

<span data-ttu-id="fe31d-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="fe31d-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="fe31d-105">Les utilisateurs ne peuvent pas utiliser de services Microsoft 365 tant que leur compte n’a pas reçu une licence d’un plan de licence.</span><span class="sxs-lookup"><span data-stu-id="fe31d-105">Users can't use any Microsoft 365 services until their account has been assigned a license from a licensing plan.</span></span> <span data-ttu-id="fe31d-106">Vous pouvez utiliser PowerShell pour attribuer rapidement des licences à des comptes non licenciés.</span><span class="sxs-lookup"><span data-stu-id="fe31d-106">You can use PowerShell to quickly assign licenses to unlicensed accounts.</span></span> 

<span data-ttu-id="fe31d-107">Les comptes d’utilisateurs doivent d’abord se voir attribuer un emplacement.</span><span class="sxs-lookup"><span data-stu-id="fe31d-107">User accounts must first be assigned a location.</span></span> <span data-ttu-id="fe31d-108">Spécifier un emplacement est une partie requise de la création d’un nouveau compte utilisateur dans [le Microsoft 365 d’administration](../admin/add-users/add-users.md).</span><span class="sxs-lookup"><span data-stu-id="fe31d-108">Specifying a location is a required part of creating a new user account in the [Microsoft 365 admin center](../admin/add-users/add-users.md).</span></span> 

<span data-ttu-id="fe31d-109">Les comptes synchronisés à partir de vos services de domaine d’annuaire actif sur place n’ont pas par défaut de localisation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fe31d-109">Accounts synchronized from your on-premises Active Directory Domain Services do not by default have a location specified.</span></span> <span data-ttu-id="fe31d-110">Vous pouvez configurer un emplacement pour ces comptes à partir de :</span><span class="sxs-lookup"><span data-stu-id="fe31d-110">You can configure a location for these accounts from:</span></span>

- <span data-ttu-id="fe31d-111">Le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fe31d-111">The Microsoft 365 admin center</span></span>
 - [<span data-ttu-id="fe31d-112">PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe31d-112">PowerShell</span></span>](configure-user-account-properties-with-microsoft-365-powershell.md)
 - <span data-ttu-id="fe31d-113">Le [portail Azure](/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal) **(Active Directory**  >  **Users >** compte utilisateur > **Profil**  >  **Contact Pays** ou  >  **région).**</span><span class="sxs-lookup"><span data-stu-id="fe31d-113">The [Azure portal](/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal) (**Active Directory** > **Users**  > user account > **Profile** > **Contact info** > **Country or region**).</span></span>

>[!Note]
><span data-ttu-id="fe31d-114">[Découvrez comment attribuer des licences à des comptes d’utilisateurs](../admin/manage/assign-licenses-to-users.md) avec le Microsoft 365 d’administration.</span><span class="sxs-lookup"><span data-stu-id="fe31d-114">[Learn how to assign licenses to user accounts](../admin/manage/assign-licenses-to-users.md) with the Microsoft 365 admin center.</span></span> <span data-ttu-id="fe31d-115">Pour une liste de ressources supplémentaires, consultez Gérer [les utilisateurs et les groupes](../admin/add-users/index.yml).</span><span class="sxs-lookup"><span data-stu-id="fe31d-115">For a list of additional resources, see [Manage users and groups](../admin/add-users/index.yml).</span></span>
>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="fe31d-116">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="fe31d-116">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="fe31d-117">Tout [d’abord, connectez-vous à Microsoft 365 locataire.](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="fe31d-117">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  

<span data-ttu-id="fe31d-118">Ensuite, énumérez les plans de licence pour votre locataire avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="fe31d-118">Next, list the license plans for your tenant with this command.</span></span>

```powershell
Get-AzureADSubscribedSku | Select SkuPartNumber
```

<span data-ttu-id="fe31d-119">Ensuite, obtenez le nom de connecteur du compte auquel vous souhaitez ajouter une licence, également connue sous le nom de nom principal de l’utilisateur (UPN).</span><span class="sxs-lookup"><span data-stu-id="fe31d-119">Next, get the sign-in name of the account to which you want add a license, also known as the user principal name (UPN).</span></span>

<span data-ttu-id="fe31d-120">Ensuite, assurez-vous que le compte utilisateur a un emplacement d’utilisation attribué.</span><span class="sxs-lookup"><span data-stu-id="fe31d-120">Next, ensure that the user account has a usage location assigned.</span></span>

```powershell
Get-AzureADUser -ObjectID <user sign-in name (UPN)> | Select DisplayName, UsageLocation
```

<span data-ttu-id="fe31d-121">S’il n’y a pas d’emplacement d’utilisation assigné, vous pouvez en assigner un avec ces commandes :</span><span class="sxs-lookup"><span data-stu-id="fe31d-121">If there is no usage location assigned, you can assign one with these commands:</span></span>

```powershell
$userUPN="<user sign-in name (UPN)>"
$userLoc="<ISO 3166-1 alpha-2 country code>"
Set-AzureADUser -ObjectID $userUPN -UsageLocation $userLoc
```

<span data-ttu-id="fe31d-122">Enfin, spécifiez le nom de l’utilisateur et le nom du plan de licence et exécutez ces commandes.</span><span class="sxs-lookup"><span data-stu-id="fe31d-122">Finally, specify the user sign-in name and license plan name and run these commands.</span></span>

```powershell
$userUPN="<user sign-in name (UPN)>"
$planName="<license plan name from the list of license plans>"
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$License.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value $planName -EQ).SkuID
$LicensesToAssign = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$LicensesToAssign.AddLicenses = $License
Set-AzureADUserLicense -ObjectId $userUPN -AssignedLicenses $LicensesToAssign
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="fe31d-123">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe31d-123">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="fe31d-124">Veuillez noter que nous commencerons à déprécier ce module lorsque les fonctionnalités de ce module seront disponibles dans [le nouveau module Azure Active Directory PowerShell pour Graph](/powershell/azuread/v2/azureactivedirectory) module.</span><span class="sxs-lookup"><span data-stu-id="fe31d-124">Please note that we will begin to deprecate this module when the functionality of this module is available in the newer [Azure Active Directory PowerShell for Graph](/powershell/azuread/v2/azureactivedirectory) module.</span></span> <span data-ttu-id="fe31d-125">Nous conseillons aux clients qui créent de nouveaux scripts PowerShell d’utiliser le module plus nouveau au lieu de ce module.</span><span class="sxs-lookup"><span data-stu-id="fe31d-125">We advise customers who are creating new PowerShell scripts to use the newer module instead of this module.</span></span>

<span data-ttu-id="fe31d-126">Tout [d’abord, connectez-vous à Microsoft 365 locataire.](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell)</span><span class="sxs-lookup"><span data-stu-id="fe31d-126">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

<span data-ttu-id="fe31d-127">Exécutez `Get-MsolAccountSku` la commande pour afficher les plans de licence disponibles et le nombre de licences disponibles dans chaque plan de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fe31d-127">Run the `Get-MsolAccountSku` command to view the available licensing plans and the number of available licenses in each plan in your organization.</span></span> <span data-ttu-id="fe31d-128">Le nombre de licences disponibles dans chaque plan **est ActiveUnits**  -  **WarningUnits**  -  **ConsumedUnits**.</span><span class="sxs-lookup"><span data-stu-id="fe31d-128">The number of available licenses in each plan is **ActiveUnits** - **WarningUnits** - **ConsumedUnits**.</span></span> <span data-ttu-id="fe31d-129">Pour plus d’informations sur les plans de licence, les licences et les services, [consultez les licences et services View avec PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="fe31d-129">For more information about licensing plans, licenses, and services, see [View licenses and services with PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span></span>

>[!Note]
><span data-ttu-id="fe31d-130">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="fe31d-130">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="fe31d-131">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe31d-131">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

<span data-ttu-id="fe31d-132">Pour trouver les comptes sans licence dans votre organisation, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="fe31d-132">To find the unlicensed accounts in your organization, run this command.</span></span>

```powershell
Get-MsolUser -All -UnlicensedUsersOnly
```

<span data-ttu-id="fe31d-133">Vous ne pouvez attribuer des licences qu’aux comptes d’utilisateurs dont **la propriété UtilisationLocation** est définie sur un code iso 3166-1 alpha-2 valide.</span><span class="sxs-lookup"><span data-stu-id="fe31d-133">You can only assign licenses to user accounts that have the **UsageLocation** property set to a valid ISO 3166-1 alpha-2 country code.</span></span> <span data-ttu-id="fe31d-134">Par exemple, US pour les États-Unis et FR pour la France.</span><span class="sxs-lookup"><span data-stu-id="fe31d-134">For example, US for the United States, and FR for France.</span></span> <span data-ttu-id="fe31d-135">Certains Microsoft 365 services ne sont pas disponibles dans certains pays.</span><span class="sxs-lookup"><span data-stu-id="fe31d-135">Some Microsoft 365 services aren't available in certain countries.</span></span> <span data-ttu-id="fe31d-136">Pour plus d’informations, voir [Sur les restrictions de licence](https://go.microsoft.com/fwlink/p/?LinkId=691730).</span><span class="sxs-lookup"><span data-stu-id="fe31d-136">For more information, see [About license restrictions](https://go.microsoft.com/fwlink/p/?LinkId=691730).</span></span>
    
<span data-ttu-id="fe31d-137">Pour trouver des comptes qui n’ont pas de **valeur UtilisationLocation,** exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="fe31d-137">To find accounts that don't have a **UsageLocation** value, run this command.</span></span>

```powershell
Get-MsolUser -All | where {$_.UsageLocation -eq $null}
```

<span data-ttu-id="fe31d-138">Pour définir la **valeur UtilisationLocation** sur un compte, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="fe31d-138">To set the **UsageLocation** value on an account, run this command.</span></span>

```powershell
Set-MsolUser -UserPrincipalName "<Account>" -UsageLocation <CountryCode>
```

<span data-ttu-id="fe31d-139">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="fe31d-139">For example:</span></span>

```powershell
Set-MsolUser -UserPrincipalName "belindan@litwareinc.com" -UsageLocation US
```
    
<span data-ttu-id="fe31d-140">Si vous utilisez la cmdlet **Get-MsolUser** sans utiliser le paramètre **-All**, seuls les 500 premiers comptes sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="fe31d-140">If you use the **Get-MsolUser** cmdlet without using the **-All** parameter, only the first 500 accounts are returned.</span></span>

### <a name="assigning-licenses-to-user-accounts"></a><span data-ttu-id="fe31d-141">Attribution de licences aux comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="fe31d-141">Assigning licenses to user accounts</span></span>
    
<span data-ttu-id="fe31d-142">Pour attribuer une licence à un utilisateur, utilisez la commande suivante dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe31d-142">To assign a license to a user, use the following command in PowerShell.</span></span>
  
```powershell
Set-MsolUserLicense -UserPrincipalName "<Account>" -AddLicenses "<AccountSkuId>"
```

<span data-ttu-id="fe31d-143">Cet exemple attribue une licence du plan de licence **litwareinc:ENTERPRISEPACK** (Office 365 Entreprise E3) à **l’utilisateur non titulaire d’un permis belindan \@ litwareinc.com**:</span><span class="sxs-lookup"><span data-stu-id="fe31d-143">This example assigns a license from the **litwareinc:ENTERPRISEPACK** (Office 365 Enterprise E3) licensing plan to the unlicensed user **belindan\@litwareinc.com**:</span></span>
  
```powershell
Set-MsolUserLicense -UserPrincipalName "belindan@litwareinc.com" -AddLicenses "litwareinc:ENTERPRISEPACK"
```

<span data-ttu-id="fe31d-144">Pour attribuer une licence à tous les utilisateurs non titulaires d’un permis, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="fe31d-144">To assign a license to all unlicensed users, run this command.</span></span>
  
```powershell
Get-MsolUser -All -UnlicensedUsersOnly [<FilterableAttributes>] | Set-MsolUserLicense -AddLicenses "<AccountSkuId>"
```
  
>[!Note]
><span data-ttu-id="fe31d-145">Vous ne pouvez pas attribuer plusieurs licences à un utilisateur à partir du même plan de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="fe31d-145">You can't assign multiple licenses to a user from the same licensing plan.</span></span> <span data-ttu-id="fe31d-146">Si le nombre de licences disponibles n’est pas suffisant, les licences sont attribuées aux utilisateurs selon leur ordre de renvoi par la cmdlet **Get-MsolUser** jusqu'à ce qu’il n’y ait plus de licence disponible.</span><span class="sxs-lookup"><span data-stu-id="fe31d-146">If you don't have enough available licenses, the licenses are assigned to users in the order that they're returned by the **Get-MsolUser** cmdlet until the available licenses run out.</span></span>
>

<span data-ttu-id="fe31d-147">Cet exemple attribue des licences du plan de licence **litwareinc:ENTERPRISEPACK** (Office 365 Entreprise E3) à tous les utilisateurs non titulaires d’un permis :</span><span class="sxs-lookup"><span data-stu-id="fe31d-147">This example assigns licenses from the **litwareinc:ENTERPRISEPACK** (Office 365 Enterprise E3) licensing plan to all unlicensed users:</span></span>
  
```powershell
Get-MsolUser -All -UnlicensedUsersOnly | Set-MsolUserLicense -AddLicenses "litwareinc:ENTERPRISEPACK"
```

<span data-ttu-id="fe31d-148">Cet exemple attribue ces mêmes licences à des utilisateurs non titulaires d’un permis dans le département des ventes aux États-Unis :</span><span class="sxs-lookup"><span data-stu-id="fe31d-148">This example assigns those same licenses to unlicensed users in the Sales department in the United States:</span></span>
  
```powershell
Get-MsolUser -All -Department "Sales" -UsageLocation "US" -UnlicensedUsersOnly | Set-MsolUserLicense -AddLicenses "litwareinc:ENTERPRISEPACK"
```
  
## <a name="move-a-user-to-a-different-subscription-license-plan-with-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="fe31d-149">Déplacez un utilisateur vers un abonnement différent (plan de licence) avec le module Azure Active Directory PowerShell pour Graph vidéo</span><span class="sxs-lookup"><span data-stu-id="fe31d-149">Move a user to a different subscription (license plan) with the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="fe31d-150">Tout [d’abord, connectez-vous à Microsoft 365 locataire.](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="fe31d-150">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
<span data-ttu-id="fe31d-151">Ensuite, obtenez le nom de connecteur du compte d’utilisateur pour lequel vous souhaitez changer d’abonnement, également connu sous le nom de nom principal de l’utilisateur (UPN).</span><span class="sxs-lookup"><span data-stu-id="fe31d-151">Next, get the sign-in name of the user account for which you want switch subscriptions, also known as the user principal name (UPN).</span></span>

<span data-ttu-id="fe31d-152">Ensuite, énumérez les abonnements (plans de licence) pour votre locataire avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="fe31d-152">Next, list the subscriptions (license plans) for your tenant with this command.</span></span>

```powershell
Get-AzureADSubscribedSku | Select SkuPartNumber
```

<span data-ttu-id="fe31d-153">Ensuite, énumérez les abonnements que le compte utilisateur a actuellement avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="fe31d-153">Next, list the subscriptions that the user account currently has with these commands.</span></span>

```powershell
$userUPN="<user account UPN>"
$licensePlanList = Get-AzureADSubscribedSku
$userList = Get-AzureADUser -ObjectID $userUPN | Select -ExpandProperty AssignedLicenses | Select SkuID 
$userList | ForEach { $sku=$_.SkuId ; $licensePlanList | ForEach { If ( $sku -eq $_.ObjectId.substring($_.ObjectId.length - 36, 36) ) { Write-Host $_.SkuPartNumber } } }
```

<span data-ttu-id="fe31d-154">Identifiez l’abonnement que l’utilisateur a actuellement (l’abonnement FROM) et l’abonnement auquel l’utilisateur se déplace (l’abonnement TO).</span><span class="sxs-lookup"><span data-stu-id="fe31d-154">Identify the subscription the user currently has (the FROM subscription) and the subscription to which the user is moving (the TO subscription).</span></span>

<span data-ttu-id="fe31d-155">Enfin, spécifiez les noms d’abonnement TO et FROM (numéros de pièce SKU) et exécutez ces commandes.</span><span class="sxs-lookup"><span data-stu-id="fe31d-155">Finally, specify the TO and FROM subscription names (SKU part numbers) and run these commands.</span></span>

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

<span data-ttu-id="fe31d-156">Vous pouvez vérifier la modification de l’abonnement pour le compte utilisateur avec ces commandes.</span><span class="sxs-lookup"><span data-stu-id="fe31d-156">You can verify the change in subscription for the user account with these commands.</span></span>

```powershell
$licensePlanList = Get-AzureADSubscribedSku
$userList = Get-AzureADUser -ObjectID $userUPN | Select -ExpandProperty AssignedLicenses | Select SkuID 
$userList | ForEach { $sku=$_.SkuId ; $licensePlanList | ForEach { If ( $sku -eq $_.ObjectId.substring($_.ObjectId.length - 36, 36) ) { Write-Host $_.SkuPartNumber } } }
```

## <a name="see-also"></a><span data-ttu-id="fe31d-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe31d-157">See also</span></span>

[<span data-ttu-id="fe31d-158">Gérer les comptes d’utilisateurs, les licences et les groupes avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe31d-158">Manage user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="fe31d-159">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe31d-159">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="fe31d-160">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fe31d-160">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
