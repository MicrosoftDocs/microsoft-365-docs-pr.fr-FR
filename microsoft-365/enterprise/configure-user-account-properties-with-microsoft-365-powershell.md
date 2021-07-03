---
title: Configurer les Microsoft 365 de compte d’utilisateur avec PowerShell
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
- O365ITProTrain
- Ent_Office_Other
- PowerShell
ms.assetid: 30813f8d-b08d-444b-98c1-53df7c29b4d7
description: Utilisez PowerShell pour configurer Microsoft 365 propriétés de comptes d’utilisateurs individuels ou multiples dans votre Microsoft 365 client.
ms.openlocfilehash: aeb9b586c42a0bdfb8d69b8d297998fedc1124e6
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53286008"
---
# <a name="configure-microsoft-365-user-account-properties-with-powershell"></a><span data-ttu-id="bab3e-103">Configurer les Microsoft 365 de compte d’utilisateur avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="bab3e-103">Configure Microsoft 365 user account properties with PowerShell</span></span>

<span data-ttu-id="bab3e-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="bab3e-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="bab3e-105">Vous pouvez utiliser la Centre d’administration Microsoft 365 pour configurer les propriétés des comptes d’utilisateurs de votre Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="bab3e-105">You can use the Microsoft 365 admin center to configure properties for the user accounts of your Microsoft 365 tenant.</span></span> <span data-ttu-id="bab3e-106">Dans PowerShell, vous pouvez également le faire, ainsi que d’autres choses que vous ne pouvez pas faire dans le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="bab3e-106">In PowerShell, you can also do this, plus some other things you can't do in the admin center.</span></span>
  
## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="bab3e-107">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="bab3e-107">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="bab3e-108">Pour configurer les propriétés des comptes d’utilisateurs dans le module Azure Active Directory PowerShell pour Graph, utilisez la cmdlet [**Set-AzureADUser**](/powershell/module/azuread/set-azureaduser) et spécifiez les propriétés à définir ou modifier.</span><span class="sxs-lookup"><span data-stu-id="bab3e-108">To configure properties for user accounts in the Azure Active Directory PowerShell for Graph module, use the [**Set-AzureADUser**](/powershell/module/azuread/set-azureaduser) cmdlet and specify the properties to set or change.</span></span>

<span data-ttu-id="bab3e-109">Tout [d’abord, connectez-vous à Microsoft 365 client.](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="bab3e-109">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>

### <a name="change-properties-for-a-specific-user-account"></a><span data-ttu-id="bab3e-110">Modification des propriétés d’un compte d’utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="bab3e-110">Change properties for a specific user account</span></span>

<span data-ttu-id="bab3e-111">Vous identifiez le compte avec le *paramètre -ObjectID* et définissez ou modifiez des propriétés spécifiques à l’aide de paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bab3e-111">You identify the account with the *-ObjectID* parameter and set or change specific properties by using additional parameters.</span></span> <span data-ttu-id="bab3e-112">Voici la liste des paramètres les plus courants :</span><span class="sxs-lookup"><span data-stu-id="bab3e-112">Here's a list of the most common parameters:</span></span>
  
- <span data-ttu-id="bab3e-113">-Department "\<department name>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-113">-Department "\<department name>"</span></span>

- <span data-ttu-id="bab3e-114">-DisplayName "\<full user name>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-114">-DisplayName "\<full user name>"</span></span>

- <span data-ttu-id="bab3e-115">-FacsimilieTelephoneNumber "<numéro de télécopie>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-115">-FacsimilieTelephoneNumber "\<fax number>"</span></span>

- <span data-ttu-id="bab3e-116">-GivenName "<prénom de l'utilisateur>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-116">-GivenName "\<user first name>"</span></span>

- <span data-ttu-id="bab3e-117">-Surname "<nom de famille de l'utilisateur>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-117">-Surname "\<user last name>"</span></span>

- <span data-ttu-id="bab3e-118">-Mobile "<N° de téléphone portable>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-118">-Mobile "\<mobile phone number>"</span></span>

- <span data-ttu-id="bab3e-119">-JobTitle "\<job title>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-119">-JobTitle "\<job title>"</span></span>

- <span data-ttu-id="bab3e-120">-PreferredLanguage "\<language>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-120">-PreferredLanguage "\<language>"</span></span>

- <span data-ttu-id="bab3e-121">-StreetAddress "\<street address>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-121">-StreetAddress "\<street address>"</span></span>

- <span data-ttu-id="bab3e-122">-City "\<city name>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-122">-City "\<city name>"</span></span>

- <span data-ttu-id="bab3e-123">-State "<nom de l'État>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-123">-State "\<state name>"</span></span>

- <span data-ttu-id="bab3e-124">-PostalCode "\<postal code></span><span class="sxs-lookup"><span data-stu-id="bab3e-124">-PostalCode "\<postal code>"</span></span>

- <span data-ttu-id="bab3e-125">-Country "\<country name>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-125">-Country "\<country name>"</span></span>

- <span data-ttu-id="bab3e-126">-TelephoneNumber "<numéro de téléphone du bureau>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-126">-TelephoneNumber "\<office phone number>"</span></span>

- <span data-ttu-id="bab3e-127">-UsageLocation \<2-character country or region code> »</span><span class="sxs-lookup"><span data-stu-id="bab3e-127">-UsageLocation "\<2-character country or region code>"</span></span>

    <span data-ttu-id="bab3e-128">Voici le code de la région ou du pays à deux lettres ISO 3166-1 alpha-2 (A2).</span><span class="sxs-lookup"><span data-stu-id="bab3e-128">This is the ISO 3166-1 alpha-2 (A2) two-letter country or region code.</span></span>

<span data-ttu-id="bab3e-129">Pour obtenir des paramètres supplémentaires, [voir Set-AzureADUser.](/powershell/module/azuread/set-azureaduser)</span><span class="sxs-lookup"><span data-stu-id="bab3e-129">For additional parameters, see [Set-AzureADUser](/powershell/module/azuread/set-azureaduser).</span></span>

> [!NOTE]
> <span data-ttu-id="bab3e-130">Avant de pouvoir attribuer des licences à un compte d’utilisateur, vous devez affecter un emplacement d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="bab3e-130">Before you can assign licenses to a user account, you must assign a usage location.</span></span>

<span data-ttu-id="bab3e-131">Pour afficher le nom d’utilisateur principal pour vos comptes d’utilisateur, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="bab3e-131">To display the User Principal Name for your user accounts, run the following command.</span></span>
  
```powershell
Get-AzureADUser | Sort UserPrincipalName | Select UserPrincipalName | More
```

<span data-ttu-id="bab3e-132">Cette commande indique à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="bab3e-132">This command instructs PowerShell to:</span></span>
  
1. <span data-ttu-id="bab3e-133">Obtenez toutes les informations sur les comptes d’utilisateur (**Get-AzureADUser**) et envoyez-les à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="bab3e-133">Get all the information on the user accounts (**Get-AzureADUser**) and send it to the next command (**|**).</span></span>

1. <span data-ttu-id="bab3e-134">Trier la liste des noms d’utilisateur principaux par ordre alphabétique (**Trier UserPrincipalName**) et l’envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="bab3e-134">Sort the list of User Principal Names alphabetically (**Sort UserPrincipalName**) and send it to the next command (**|**).</span></span>

1. <span data-ttu-id="bab3e-135">Afficher uniquement la propriété Nom d’utilisateur principal pour chaque compte (**Sélectionnez UserPrincipalName**).</span><span class="sxs-lookup"><span data-stu-id="bab3e-135">Display just the User Principal Name property for each account (**Select UserPrincipalName**).</span></span>

1. <span data-ttu-id="bab3e-136">Afficher un écran à la fois (**Plus**).</span><span class="sxs-lookup"><span data-stu-id="bab3e-136">Display them one screen at a time (**More**).</span></span>

<span data-ttu-id="bab3e-137">Pour afficher le nom d’utilisateur principal d’un compte en fonction de son nom complet (prénom et nom), exécutez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bab3e-137">To display the User Principal Name for an account based on its display name (first and last name), run the following commands.</span></span> <span data-ttu-id="bab3e-138">Remplissez la *$userName* variable et supprimez les \< and > caractères :</span><span class="sxs-lookup"><span data-stu-id="bab3e-138">Fill in the *$userName* variable, and remove the \< and > characters:</span></span>
  
```powershell
$userName="<Display name>"
Write-Host (Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="bab3e-139">Cet exemple affiche le nom d’utilisateur principal du compte d’utilisateur dont le nom complet *est Caleb Sills*.</span><span class="sxs-lookup"><span data-stu-id="bab3e-139">This example displays the User Principal Name for the user account that has the display name *Caleb Sills*.</span></span>
  
```powershell
$userName="Caleb Sills"
Write-Host (Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="bab3e-140">En utilisant une variable *$upn*, vous pouvez apporter des modifications à des comptes individuels en fonction de leur nom d'affichage.</span><span class="sxs-lookup"><span data-stu-id="bab3e-140">By using a *$upn* variable, you can make changes to individual accounts based on their display name.</span></span> <span data-ttu-id="bab3e-141">Voici un exemple qui définit l’emplacement d’utilisation de *Belinda Newman* en France.</span><span class="sxs-lookup"><span data-stu-id="bab3e-141">Here's an example that sets *Belinda Newman*'s usage location to France.</span></span> <span data-ttu-id="bab3e-142">Mais il spécifie son nom d’affichage plutôt que son nom d’utilisateur principal :</span><span class="sxs-lookup"><span data-stu-id="bab3e-142">But it specifies her display name rather than her User Principal Name:</span></span>
  
```powershell
$userName="Belinda Newman"
$upn=(Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
Set-AzureADUser -ObjectID $upn -UsageLocation "FR"
```

### <a name="change-properties-for-all-user-accounts"></a><span data-ttu-id="bab3e-143">Modification des propriétés de tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="bab3e-143">Change properties for all user accounts</span></span>

<span data-ttu-id="bab3e-144">Pour modifier les propriétés de tous les utilisateurs, vous pouvez utiliser une combinaison des cmdlets **Get-AzureADUser** et **Set-AzureADUser.**</span><span class="sxs-lookup"><span data-stu-id="bab3e-144">To change properties for all users, you can use a combination of the **Get-AzureADUser** and **Set-AzureADUser** cmdlets.</span></span> <span data-ttu-id="bab3e-145">L’exemple suivant modifie l’emplacement d’utilisation de tous les utilisateurs en *France*:</span><span class="sxs-lookup"><span data-stu-id="bab3e-145">The following example changes the usage location for all users to *France*:</span></span>
  
```powershell
Get-AzureADUser | Set-AzureADUser -UsageLocation "FR"
```

<span data-ttu-id="bab3e-146">Cette commande indique à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="bab3e-146">This command instructs PowerShell to:</span></span>
  
1. <span data-ttu-id="bab3e-147">Obtenez toutes les informations sur les comptes d’utilisateur (**Get-AzureADUser**) et envoyez-les à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="bab3e-147">Get all of the information on the user accounts (**Get-AzureADUser**) and send it to the next command (**|**).</span></span>

1. <span data-ttu-id="bab3e-148">Définissez l’emplacement utilisateur sur France (**Set-AzureADUser -UsageLocation « FR »**).</span><span class="sxs-lookup"><span data-stu-id="bab3e-148">Set the user location to France (**Set-AzureADUser -UsageLocation "FR"**).</span></span>

### <a name="change-properties-for-a-specific-set-of-user-accounts"></a><span data-ttu-id="bab3e-149">Modification des propriétés d’un ensemble spécifique de comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="bab3e-149">Change properties for a specific set of user accounts</span></span>

<span data-ttu-id="bab3e-150">Pour modifier les propriétés d’un ensemble spécifique de comptes d’utilisateurs, vous pouvez utiliser une combinaison des cmdlets **Get-AzureADUser**, **Where** et **Set-AzureADUser.**</span><span class="sxs-lookup"><span data-stu-id="bab3e-150">To change properties for a specific set of user accounts, you can use a combination of the **Get-AzureADUser**, **Where**, and **Set-AzureADUser** cmdlets.</span></span> <span data-ttu-id="bab3e-151">L’exemple suivant modifie l’emplacement d’utilisation de tous les utilisateurs du service Comptabilité en *France*:</span><span class="sxs-lookup"><span data-stu-id="bab3e-151">The following example changes the usage location for all the users in the Accounting department to *France*:</span></span>
  
```powershell
Get-AzureADUser | Where {$_.Department -eq "Accounting"} | Set-AzureADUser -UsageLocation "FR"
```

<span data-ttu-id="bab3e-152">Cette commande indique à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="bab3e-152">This command instructs PowerShell to:</span></span>
  
1. <span data-ttu-id="bab3e-153">Obtenez toutes les informations sur les comptes d’utilisateur (**Get-AzureADUser**), et envoyez-les à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="bab3e-153">Get all the information on the user accounts (**Get-AzureADUser**), and send it to the next command (**|**).</span></span>

1.  <span data-ttu-id="bab3e-154">Recherchez tous les comptes d’utilisateur dont la propriété *Department* est définie sur « Accounting » (**Où {$_. Department -eq « Accounting"}**), et envoyer les informations résultantes à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="bab3e-154">Find all the user accounts that have their *Department* property set to "Accounting" (**Where {$_.Department -eq "Accounting"}**), and send the resulting information to the next command (**|**).</span></span>

1. <span data-ttu-id="bab3e-155">Définissez l’emplacement utilisateur sur France (**Set-AzureADUser -UsageLocation « FR »**).</span><span class="sxs-lookup"><span data-stu-id="bab3e-155">Set the user location to France (**Set-AzureADUser -UsageLocation "FR"**).</span></span>

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="bab3e-156">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bab3e-156">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="bab3e-157">Pour configurer les propriétés des comptes d’utilisateurs avec le module Microsoft Azure Active Directory pour Windows PowerShell, utilisez la cmdlet **Set-MsolUser** et spécifiez les propriétés à définir ou modifier.</span><span class="sxs-lookup"><span data-stu-id="bab3e-157">To configure properties for user accounts with the Microsoft Azure Active Directory Module for Windows PowerShell, use the **Set-MsolUser** cmdlet and specify the properties to set or change.</span></span>

<span data-ttu-id="bab3e-158">Tout [d’abord, connectez-vous à Microsoft 365 client.](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell)</span><span class="sxs-lookup"><span data-stu-id="bab3e-158">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>
  
> [!NOTE]
> <span data-ttu-id="bab3e-159">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour le module Windows PowerShell et les cmdlets incluant *Msol* dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="bab3e-159">PowerShell Core doesn't support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with *Msol* in their name.</span></span> <span data-ttu-id="bab3e-160">Exécutez ces cmdlets à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bab3e-160">Run these cmdlets from Windows PowerShell.</span></span>

### <a name="change-properties-for-a-specific-user-account"></a><span data-ttu-id="bab3e-161">Modification des propriétés d’un compte d’utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="bab3e-161">Change properties for a specific user account</span></span>

<span data-ttu-id="bab3e-162">Pour configurer les propriétés d’un compte d’utilisateur spécifique, utilisez l’cmdlet [**Set-MsolUser**](/previous-versions/azure/dn194136(v=azure.100)) et spécifiez les propriétés à définir ou à modifier.</span><span class="sxs-lookup"><span data-stu-id="bab3e-162">To configure properties for a specific user account, use the [**Set-MsolUser**](/previous-versions/azure/dn194136(v=azure.100)) cmdlet and specify the properties to set or change.</span></span> 

<span data-ttu-id="bab3e-163">Vous identifiez le compte avec le paramètre *-UserPrincipalName* et définissez ou modifiez des propriétés spécifiques à l’aide de paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bab3e-163">You identify the account with the *-UserPrincipalName* parameter and set or change specific properties by using additional parameters.</span></span> <span data-ttu-id="bab3e-164">Voici la liste des paramètres les plus courants.</span><span class="sxs-lookup"><span data-stu-id="bab3e-164">Here's a list of the most common parameters.</span></span>
  
- <span data-ttu-id="bab3e-165">-City "\<city name>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-165">-City "\<city name>"</span></span>

- <span data-ttu-id="bab3e-166">-Country "\<country name>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-166">-Country "\<country name>"</span></span>

- <span data-ttu-id="bab3e-167">-Department "\<department name>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-167">-Department "\<department name>"</span></span>

- <span data-ttu-id="bab3e-168">-DisplayName "\<full user name>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-168">-DisplayName "\<full user name>"</span></span>

- <span data-ttu-id="bab3e-169">-Fax "<numéro de fax>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-169">-Fax "\<fax number>"</span></span>

- <span data-ttu-id="bab3e-170">-FirstName "<prénom de l'utilisateur>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-170">-FirstName "\<user first name>"</span></span>

- <span data-ttu-id="bab3e-171">-LastName "<nom de famille de l'utilisateur>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-171">-LastName "\<user last name>"</span></span>

- <span data-ttu-id="bab3e-172">-MobilePhone "<numéro de téléphone portable>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-172">-MobilePhone "\<mobile phone number>"</span></span>

- <span data-ttu-id="bab3e-173">-Office "\<office location>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-173">-Office "\<office location>"</span></span>

- <span data-ttu-id="bab3e-174">-PhoneNumber "<numéro de téléphone du bureau>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-174">-PhoneNumber "\<office phone number>"</span></span>

- <span data-ttu-id="bab3e-175">-PostalCode "\<postal code></span><span class="sxs-lookup"><span data-stu-id="bab3e-175">-PostalCode "\<postal code>"</span></span>

- <span data-ttu-id="bab3e-176">-PreferredLanguage "\<language>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-176">-PreferredLanguage "\<language>"</span></span>

- <span data-ttu-id="bab3e-177">-State "<nom de l'État>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-177">-State "\<state name>"</span></span>

- <span data-ttu-id="bab3e-178">-StreetAddress "\<street address>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-178">-StreetAddress "\<street address>"</span></span>

- <span data-ttu-id="bab3e-179">-Title "<intitulé du poste>"</span><span class="sxs-lookup"><span data-stu-id="bab3e-179">-Title "\<title name>"</span></span>

- <span data-ttu-id="bab3e-180">-UsageLocation \<2-character country or region code> »</span><span class="sxs-lookup"><span data-stu-id="bab3e-180">-UsageLocation "\<2-character country or region code>"</span></span>

    <span data-ttu-id="bab3e-181">Voici le code de la région ou du pays à deux lettres ISO 3166-1 alpha-2 (A2).</span><span class="sxs-lookup"><span data-stu-id="bab3e-181">This is the ISO 3166-1 alpha-2 (A2) two-letter country or region code.</span></span>

<span data-ttu-id="bab3e-182">Pour d’autres paramètres, [voir Set-MsolUser](/previous-versions/azure/dn194136(v=azure.100)).</span><span class="sxs-lookup"><span data-stu-id="bab3e-182">For additional parameters, see [Set-MsolUser](/previous-versions/azure/dn194136(v=azure.100)).</span></span>

<span data-ttu-id="bab3e-183">Pour voir les noms d’utilisateur principaux de tous vos utilisateurs, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="bab3e-183">To see the User Principal Names of all your users, run the following command:</span></span>
  
```powershell
Get-MSolUser | Sort UserPrincipalName | Select UserPrincipalName | More
```

<span data-ttu-id="bab3e-184">Cette commande indique à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="bab3e-184">This command instructs PowerShell to:</span></span>
  
1. <span data-ttu-id="bab3e-185">Obtenez toutes les informations pour les comptes d’utilisateur (**Get-MsolUser**) et envoyez-les à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="bab3e-185">Get all of information for the user accounts (**Get-MsolUser**) and send it to the next command (**|**).</span></span>

1. <span data-ttu-id="bab3e-186">Trier la liste des noms d’utilisateur principaux par ordre alphabétique (**Trier UserPrincipalName**) et l’envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="bab3e-186">Sort the list of User Principal Names alphabetically (**Sort UserPrincipalName**) and send it to the next command (**|**).</span></span>

1. <span data-ttu-id="bab3e-187">Afficher uniquement la propriété Nom d’utilisateur principal pour chaque compte (**Sélectionnez UserPrincipalName**).</span><span class="sxs-lookup"><span data-stu-id="bab3e-187">Display just the User Principal Name property for each account (**Select UserPrincipalName**).</span></span>

1. <span data-ttu-id="bab3e-188">Afficher un écran à la fois (**Plus**).</span><span class="sxs-lookup"><span data-stu-id="bab3e-188">Display them one screen at a time (**More**).</span></span>

<span data-ttu-id="bab3e-189">Pour afficher le nom d’utilisateur principal d’un compte en fonction de son nom complet (prénom et nom), exécutez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bab3e-189">To display the User Principal Name for an account based on its display name (first and last name), run the following commands.</span></span> <span data-ttu-id="bab3e-190">Remplissez la *$userName* variable et supprimez les \< and > caractères.</span><span class="sxs-lookup"><span data-stu-id="bab3e-190">Fill in the *$userName* variable, and remove the \< and > characters.</span></span>
  
```powershell
$userName="<Display name>"
Write-Host (Get-MsolUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="bab3e-191">Cet exemple montre comment afficher le nom d’utilisateur principal de l’utilisateur nommé Caleb Sills :</span><span class="sxs-lookup"><span data-stu-id="bab3e-191">This example displays the User Principal Name for the user named Caleb Sills:</span></span>
  
```powershell
$userName="Caleb Sills"
Write-Host (Get-MsolUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="bab3e-192">En utilisant une variable *$upn*, vous pouvez apporter des modifications à des comptes individuels en fonction de leur nom d'affichage.</span><span class="sxs-lookup"><span data-stu-id="bab3e-192">By using a *$upn* variable, you can make changes to individual accounts based on their display name.</span></span> <span data-ttu-id="bab3e-193">Voici un exemple qui définit l’emplacement d’utilisation de *Belinda Newman* en *France,* mais spécifie son nom d’affichage plutôt que son nom d’utilisateur principal :</span><span class="sxs-lookup"><span data-stu-id="bab3e-193">Here's an example that sets *Belinda Newman*'s usage location to *France*, but specifies her display name rather than her User Principal Name:</span></span>
  
```powershell
$userName="<display name>"
$upn=(Get-MsolUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
Set-MsolUser -UserPrincipalName $upn -UsageLocation "FR"
```

### <a name="change-properties-for-all-user-accounts"></a><span data-ttu-id="bab3e-194">Modification des propriétés de tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="bab3e-194">Change properties for all user accounts</span></span>

<span data-ttu-id="bab3e-195">Pour modifier les propriétés de tous les utilisateurs, utilisez une combinaison des cmdlets **Get-MsolUser** et **Set-MsolUser.**</span><span class="sxs-lookup"><span data-stu-id="bab3e-195">To change properties for all users,  use a combination of the **Get-MsolUser** and **Set-MsolUser** cmdlets.</span></span> <span data-ttu-id="bab3e-196">L’exemple suivant modifie l’emplacement d’utilisation de tous les utilisateurs en *France*:</span><span class="sxs-lookup"><span data-stu-id="bab3e-196">The following example changes the usage location for all users to *France*:</span></span>
  
```powershell
Get-MsolUser | Set-MsolUser -UsageLocation "FR"
```

<span data-ttu-id="bab3e-197">Cette commande indique à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="bab3e-197">This command instructs PowerShell to:</span></span>
  
1. <span data-ttu-id="bab3e-198">Obtenez toutes les informations des comptes d’utilisateur (**Get-MsolUser**) et envoyez-les à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="bab3e-198">Get all the information for the user accounts (**Get-MsolUser**) and send it to the next command (**|**).</span></span>

1. <span data-ttu-id="bab3e-199">Définissez l’emplacement utilisateur sur France (**Set-MsolUser -UsageLocation « FR »**).</span><span class="sxs-lookup"><span data-stu-id="bab3e-199">Set the user location to France (**Set-MsolUser -UsageLocation "FR"**).</span></span>

### <a name="change-properties-for-a-specific-set-of-user-accounts"></a><span data-ttu-id="bab3e-200">Modification des propriétés d’un ensemble spécifique de comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="bab3e-200">Change properties for a specific set of user accounts</span></span>

<span data-ttu-id="bab3e-201">Pour modifier les propriétés d’un ensemble spécifique de comptes d’utilisateurs, vous pouvez utiliser une combinaison des cmdlets **Get-MsolUser**, **Where** et **Set-MsolUser.**</span><span class="sxs-lookup"><span data-stu-id="bab3e-201">To change properties for a specific set of user accounts, you can use a combination of the **Get-MsolUser**, **Where**, and **Set-MsolUser** cmdlets.</span></span> <span data-ttu-id="bab3e-202">L’exemple suivant modifie l’emplacement d’utilisation de tous les utilisateurs du service Comptabilité en *France*:</span><span class="sxs-lookup"><span data-stu-id="bab3e-202">The following example changes the usage location for all the users in the Accounting department to *France*:</span></span>
  
```powershell
Get-MsolUser | Where {$_.Department -eq "Accounting"} | Set-MsolUser -UsageLocation "FR"
```

<span data-ttu-id="bab3e-203">Cette commande indique à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="bab3e-203">This command instructs PowerShell to:</span></span>
  
1. <span data-ttu-id="bab3e-204">Obtenez toutes les informations des comptes d’utilisateur (**Get-MsolUser**) et envoyez-les à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="bab3e-204">Get all the information for the user accounts (**Get-MsolUser**) and send it to the next command (**|**).</span></span>

1. <span data-ttu-id="bab3e-205">Recherchez tous les comptes d’utilisateur dont la propriété *Department* est définie sur « Accounting » (**Where {$_. Department -eq « Accounting"}**) et envoyer les informations résultantes à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="bab3e-205">Find all user accounts that have their *Department* property set to "Accounting" (**Where {$_.Department -eq "Accounting"}**) and send the resulting information to the next command (**|**).</span></span>

1. <span data-ttu-id="bab3e-206">Définissez l’emplacement utilisateur sur France (**Set-MsolUser -UsageLocation « FR »**).</span><span class="sxs-lookup"><span data-stu-id="bab3e-206">Set the user location to France (**Set-MsolUser -UsageLocation "FR"**).</span></span>

## <a name="see-also"></a><span data-ttu-id="bab3e-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bab3e-207">See also</span></span>

[<span data-ttu-id="bab3e-208">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="bab3e-208">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="bab3e-209">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="bab3e-209">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="bab3e-210">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bab3e-210">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
