---
title: Désactiver l’accès aux services Microsoft 365 avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/27/2020
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
- Ent_Office_Other
- PowerShell
- LIL_Placement
- seo-marvel-apr2020
ms.assetid: 264f4f0d-e2cd-44da-a9d9-23bef250a720
description: Dans cet article, Découvrez comment utiliser PowerShell pour désactiver l’accès aux services Microsoft 365 pour les utilisateurs.
ms.openlocfilehash: 292bda3b380b9ce3947b2427288da4f16198bb51
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689840"
---
# <a name="disable-access-to-microsoft-365-services-with-powershell"></a><span data-ttu-id="a1fe3-103">Désactiver l’accès aux services Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1fe3-103">Disable access to Microsoft 365 services with PowerShell</span></span>

<span data-ttu-id="a1fe3-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="a1fe3-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="a1fe3-105">Lorsqu’un compte Microsoft 365 est affecté à une licence d’un plan de gestion des licences, les services Microsoft 365 sont mis à la disposition de l’utilisateur à partir de cette licence.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-105">When a Microsoft 365 account is assigned a license from a licensing plan, Microsoft 365 services are made available to the user from that license.</span></span> <span data-ttu-id="a1fe3-106">Toutefois, vous pouvez contrôler les services Microsoft 365 auxquels l’utilisateur peut accéder.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-106">However, you can control the Microsoft 365 services that the user can access.</span></span> <span data-ttu-id="a1fe3-107">Par exemple, même si la licence autorise l’accès au service SharePoint Online, vous pouvez désactiver l’accès à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-107">For example, even though the license allows access to the SharePoint Online service, you can disable access to it.</span></span> <span data-ttu-id="a1fe3-108">Vous pouvez utiliser PowerShell pour désactiver l’accès à n’importe quel nombre de services pour un plan de gestion des licences spécifique pour :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-108">You can use PowerShell to disable access to any number of services for a specific licensing plan for:</span></span>

- <span data-ttu-id="a1fe3-109">un compte individuel ;</span><span class="sxs-lookup"><span data-stu-id="a1fe3-109">An individual account.</span></span>
- <span data-ttu-id="a1fe3-110">un groupe de comptes ;</span><span class="sxs-lookup"><span data-stu-id="a1fe3-110">A group of accounts.</span></span>
- <span data-ttu-id="a1fe3-111">tous les comptes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-111">All accounts in your organization.</span></span>

>[!Note]
><span data-ttu-id="a1fe3-112">Il existe des dépendances de service Microsoft 365 qui peuvent vous empêcher de désactiver un service spécifié lorsque d’autres services dépendent de lui.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-112">There are Microsoft 365 service dependencies that can prevent you from disabling a specified service when other services depend on it.</span></span>
>

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="a1fe3-113">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-113">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="a1fe3-114">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="a1fe3-114">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

<span data-ttu-id="a1fe3-115">Ensuite, utilisez cette commande pour afficher vos plans de gestion des licences disponibles, également appelés AccountSkuIds :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-115">Next, use this command to view your available licensing plans, also known as AccountSkuIds:</span></span>

```powershell
Get-MsolAccountSku | Select AccountSkuId | Sort AccountSkuId
```

>[!Note]
><span data-ttu-id="a1fe3-116">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-116">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="a1fe3-117">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-117">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

<span data-ttu-id="a1fe3-118">Pour plus d’informations, consultez la rubrique [afficher les licences et les services avec PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="a1fe3-118">For more information, see [View licenses and services with PowerShell](view-licenses-and-services-with-microsoft-365-powershell.md).</span></span>
    
<span data-ttu-id="a1fe3-119">Pour afficher les résultats avant et après des procédures de cette rubrique, voir [View Account License and service Details with PowerShell](view-account-license-and-service-details-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="a1fe3-119">To see the before and after results of the procedures in this topic, see [View account license and service details with PowerShell](view-account-license-and-service-details-with-microsoft-365-powershell.md).</span></span>
    
<span data-ttu-id="a1fe3-120">Un script PowerShell est disponible pour automatiser les procédures décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-120">A PowerShell script is available that automates the procedures described in this topic.</span></span> <span data-ttu-id="a1fe3-121">Plus précisément, le script vous permet d’afficher et de désactiver les services de votre organisation Microsoft 365, y compris Sway.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-121">Specifically, the script lets you view and disable services in your Microsoft 365 organization, including Sway.</span></span> <span data-ttu-id="a1fe3-122">Pour plus d’informations, consultez la rubrique [désactiver l’accès à Sway avec PowerShell](disable-access-to-sway-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="a1fe3-122">For more information, see [Disable access to Sway with PowerShell](disable-access-to-sway-with-microsoft-365-powershell.md).</span></span>
    
    
### <a name="disable-specific-microsoft-365-services-for-specific-users-for-a-specific-licensing-plan"></a><span data-ttu-id="a1fe3-123">Désactiver des services Microsoft 365 spécifiques pour des utilisateurs spécifiques pour un plan de gestion des licences spécifique</span><span class="sxs-lookup"><span data-stu-id="a1fe3-123">Disable specific Microsoft 365 services for specific users for a specific licensing plan</span></span>
  
<span data-ttu-id="a1fe3-124">Pour désactiver un ensemble spécifique de services Microsoft 365 pour les utilisateurs pour un plan de gestion de licences spécifique, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-124">To disable a specific set of Microsoft 365 services for users for a specific licensing plan, perform the following steps:</span></span>
  
#### <a name="step-1-identify-the-undesirable-services-in-the-licensing-plan-by-using-the-following-syntax"></a><span data-ttu-id="a1fe3-125">Étape 1 : identifier les services indésirables dans le plan de gestion des licences à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-125">Step 1: Identify the undesirable services in the licensing plan by using the following syntax:</span></span>
    
```powershell
$LO = New-MsolLicenseOptions -AccountSkuId <AccountSkuId> -DisabledPlans "<UndesirableService1>", "<UndesirableService2>"...
```

<span data-ttu-id="a1fe3-126">L’exemple suivant crée un objet **LicenseOptions** qui désactive les services Office et SharePoint Online dans le plan de gestion des licences nommé `litwareinc:ENTERPRISEPACK` (Office 365 entreprise E3).</span><span class="sxs-lookup"><span data-stu-id="a1fe3-126">The following example creates a **LicenseOptions** object that disables the Office and SharePoint Online services in the licensing plan named `litwareinc:ENTERPRISEPACK` (Office 365 Enterprise E3).</span></span>
    
```powershell
$LO = New-MsolLicenseOptions -AccountSkuId "litwareinc:ENTERPRISEPACK" -DisabledPlans "SHAREPOINTWAC", "SHAREPOINTENTERPRISE"
```

#### <a name="step-2-use-the-licenseoptions-object-from-step-1-on-one-or-more-users"></a><span data-ttu-id="a1fe3-127">Étape 2 : utilisez l’objet **LicenseOptions** de l’étape 1 sur un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-127">Step 2: Use the **LicenseOptions** object from Step 1 on one or more users.</span></span>
    
<span data-ttu-id="a1fe3-128">Pour créer un compte dont les services sont désactivés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-128">To create a new account that has the services disabled, use the following syntax:</span></span>
    
```powershell
New-MsolUser -UserPrincipalName <Account> -DisplayName <DisplayName> -FirstName <FirstName> -LastName <LastName> -LicenseAssignment <AccountSkuId> -LicenseOptions $LO -UsageLocation <CountryCode>
```

<span data-ttu-id="a1fe3-129">L’exemple suivant crée un nouveau compte pour allie Bellew qui affecte la licence et désactive les services décrits à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-129">The following example creates a new account for Allie Bellew that assigns the license and disables the services described in Step 1.</span></span>
    
```powershell
New-MsolUser -UserPrincipalName allieb@litwareinc.com -DisplayName "Allie Bellew" -FirstName Allie -LastName Bellew -LicenseAssignment litwareinc:ENTERPRISEPACK -LicenseOptions $LO -UsageLocation US
```

<span data-ttu-id="a1fe3-130">Pour plus d’informations sur la création de comptes d’utilisateur dans PowerShell pour Microsoft 365, voir [Create User Accounts with PowerShell](create-user-accounts-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="a1fe3-130">For more information about creating user accounts in PowerShell for Microsoft 365, see [Create user accounts with PowerShell](create-user-accounts-with-microsoft-365-powershell.md).</span></span>
    
<span data-ttu-id="a1fe3-131">Pour désactiver les services d’un utilisateur sous licence existant, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-131">To disable the services for an existing licensed user, use the following syntax:</span></span>
    
```powershell
Set-MsolUserLicense -UserPrincipalName <Account> -LicenseOptions $LO
```

<span data-ttu-id="a1fe3-132">Cet exemple désactive les services de l’utilisateur BelindaN@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-132">This example disables the services for the user BelindaN@litwareinc.com.</span></span>
    
```powershell
Set-MsolUserLicense -UserPrincipalName belindan@litwareinc.com -LicenseOptions $LO
```

<span data-ttu-id="a1fe3-133">Pour désactiver les services décrits à l’étape 1 pour tous les utilisateurs sous licence existants, spécifiez le nom de votre plan Microsoft 365 à partir de l’affichage de la cmdlet **Get-MsolAccountSku** (comme **litwareinc : ENTERPRISEPACK**), puis exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-133">To disable the services described in Step 1 for all existing licensed users, specify the name of your Microsoft 365 plan from the display of the **Get-MsolAccountSku** cmdlet (such as **litwareinc:ENTERPRISEPACK**), and then run the following commands:</span></span>
    
```powershell
$acctSKU="<AccountSkuId>"
$AllLicensed = Get-MsolUser -All | Where {$_.isLicensed -eq $true -and $_.licenses.AccountSku.SkuPartNumber -contains ($acctSKU).Substring($acctSKU.IndexOf(":")+1, $acctSKU.Length-$acctSKU.IndexOf(":")-1)}
$AllLicensed | ForEach {Set-MsolUserLicense -UserPrincipalName $_.UserPrincipalName -LicenseOptions $LO}
```

 <span data-ttu-id="a1fe3-134">Si vous utilisez l’applet de commande **Get-MsolUser** sans utiliser le paramètre _All_ , seuls les premiers comptes d’utilisateur 500 sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-134">If you use the **Get-MsolUser** cmdlet without using the _All_ parameter, only the first 500 user accounts are returned.</span></span>

<span data-ttu-id="a1fe3-135">Pour désactiver les services pour un groupe d’utilisateurs existants, appliquez l’une des méthodes suivantes pour identifier les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-135">To disable the services for a group of existing users, use either of the following methods to identify the users:</span></span>
    
<span data-ttu-id="a1fe3-136">**Méthode 1. Filtrer les comptes en fonction d’un attribut de compte existant**</span><span class="sxs-lookup"><span data-stu-id="a1fe3-136">**Method 1. Filter the accounts based on an existing account attribute**</span></span> 

<span data-ttu-id="a1fe3-137">Pour ce faire, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-137">To do this, use the following syntax:</span></span>
    
```powershell
$x = Get-MsolUser -All <FilterableAttributes>
$x | ForEach {Set-MsolUserLicense -UserPrincipalName $_.UserPrincipalName -LicenseOptions $LO}
```

<span data-ttu-id="a1fe3-138">L’exemple suivant désactive les services pour les utilisateurs du service des ventes aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-138">The following example disables the services for users in the Sales department in the United States.</span></span>
    
```powershell
$USSales = Get-MsolUser -All -Department "Sales" -UsageLocation "US"
$USSales | ForEach {Set-MsolUserLicense -UserPrincipalName $_.UserPrincipalName -LicenseOptions $LO}
```

<span data-ttu-id="a1fe3-139">**Méthode 2 : utiliser une liste de comptes spécifiques**</span><span class="sxs-lookup"><span data-stu-id="a1fe3-139">**Method 2: Use a list of specific accounts**</span></span> 

<span data-ttu-id="a1fe3-140">Pour ce faire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-140">To do this, perform the following steps:</span></span>
    
1. <span data-ttu-id="a1fe3-141">Créez un fichier texte contenant un seul compte sur chaque ligne comme suit :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-141">Create a text file that contains one account on each line like this:</span></span>
    
   ```powershell
   akol@contoso.com
   tjohnston@contoso.com
   kakers@contoso.com
   ```

   <span data-ttu-id="a1fe3-142">Dans cet exemple, le fichier texte est C : \\ My Documents \\Accounts.txt.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-142">In this example, the text file is C:\\My Documents\\Accounts.txt.</span></span>
    
2. <span data-ttu-id="a1fe3-143">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-143">Run the following command:</span></span>
    
   ```powershell
   Get-Content "C:\My Documents\Accounts.txt" | foreach {Set-MsolUserLicense -UserPrincipalName $_ -LicenseOptions $LO}
   ```

<span data-ttu-id="a1fe3-144">Si vous souhaitez désactiver l’accès aux services pour plusieurs plans de gestion des licences, répétez les instructions ci-dessus pour chaque plan de gestion des licences, en vous assurant que :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-144">If you want to disable access to services for multiple licensing plans, repeat the above instructions for each licensing plan, ensuring that:</span></span>

- <span data-ttu-id="a1fe3-145">Le plan de gestion des licences a été attribué aux comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-145">The user accounts have been assigned the licensing plan.</span></span>
- <span data-ttu-id="a1fe3-146">Les services à désactiver sont disponibles dans le plan de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="a1fe3-146">The services to disable are available in the licensing plan.</span></span>

<span data-ttu-id="a1fe3-147">Pour désactiver les services Microsoft 365 pour les utilisateurs pendant que vous les affectez à un plan de gestion des licences, reportez-vous à la rubrique [désactiver l’accès aux services lors de l’attribution de licences utilisateur](disable-access-to-services-while-assigning-user-licenses.md).</span><span class="sxs-lookup"><span data-stu-id="a1fe3-147">To disable Microsoft 365 services for users while you are assigning them to a licensing plan, see [Disable access to services while assigning user licenses](disable-access-to-services-while-assigning-user-licenses.md).</span></span>

### <a name="assign-all-services-in-a-licensing-plan-to-a-user-account"></a><span data-ttu-id="a1fe3-148">Affecter tous les services d’un plan de gestion des licences à un compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a1fe3-148">Assign all services in a licensing plan to a user account</span></span>

<span data-ttu-id="a1fe3-149">Pour les comptes d’utilisateur pour lesquels des services ont été désactivés, vous pouvez activer tous les services pour un plan de gestion des licences spécifique à l’aide des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1fe3-149">For user accounts that have had services disabled, you can enable all services for a specific licensing plan with these commands:</span></span>

```powershell
$userUPN="<user account UPN>"
$acctSKU="<AccountSkuId>"
$LO = New-MsolLicenseOptions -AccountSkuId $acctSKU
Set-MsolUserLicense -UserPrincipalName $userUPN -LicenseOptions $LO
```

## <a name="related-topic"></a><span data-ttu-id="a1fe3-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1fe3-150">Related topic</span></span>

[<span data-ttu-id="a1fe3-151">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1fe3-151">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="a1fe3-152">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1fe3-152">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="a1fe3-153">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a1fe3-153">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
