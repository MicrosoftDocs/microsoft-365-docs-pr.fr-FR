---
title: Configuration des propriétés de compte d’utilisateur Microsoft 365 avec PowerShell
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
description: 'Résumé : utilisez PowerShell pour Microsoft 365 pour configurer les propriétés d’un ou de plusieurs comptes d’utilisateur dans votre client Microsoft 365.'
ms.openlocfilehash: ae797d67b47c637dc95176b92fad8090f8a7ab37
ms.sourcegitcommit: 3165329d1fb5a7fd866ff287bea3b6354ea2be18
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2020
ms.locfileid: "48580927"
---
# <a name="configure-microsoft-365-user-account-properties-with-powershell"></a><span data-ttu-id="4a6f1-103">Configuration des propriétés de compte d’utilisateur Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="4a6f1-103">Configure Microsoft 365 user account properties with PowerShell</span></span>

<span data-ttu-id="4a6f1-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="4a6f1-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="4a6f1-105">Bien que vous puissiez utiliser le centre d’administration Microsoft 365 pour configurer les propriétés des comptes d’utilisateurs de votre client Microsoft 365, vous pouvez également utiliser PowerShell et effectuer certaines opérations que le centre d’administration Microsoft 365 ne peut pas faire.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-105">Although you can use the Microsoft 365 admin center to configure properties for the user accounts of your Microsoft 365 tenant, you can also use PowerShell and do some things that the Microsoft 365 admin center cannot.</span></span>
  
## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="4a6f1-106">Utilisez le module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="4a6f1-106">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="4a6f1-107">Pour configurer les propriétés des comptes d’utilisateur avec le module Azure Active Directory PowerShell pour Graph, vous utilisez la cmdlet [Set-AzureADUser](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser) et spécifiez les propriétés à définir ou à modifier.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-107">To configure properties for user accounts with the Azure Active Directory PowerShell for Graph module, you use the [Set-AzureADUser](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser) cmdlet and specify the properties to set or change.</span></span> 

<span data-ttu-id="4a6f1-108">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-108">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
   
### <a name="change-properties-for-a-specific-user-account"></a><span data-ttu-id="4a6f1-109">Modification des propriétés d’un compte d’utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="4a6f1-109">Change properties for a specific user account</span></span>

<span data-ttu-id="4a6f1-p101">Identifiez le compte avec le paramètre **-ObjectID** et définissez ou modifiez des propriétés spécifiques à l'aide de paramètres supplémentaires. Voici la liste des principaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-p101">You identify the account with the **-ObjectID** parameter and set or change specific properties with additional parameters. Here's a list of the most common parameters.</span></span>
  
- <span data-ttu-id="4a6f1-112">-Department "\<department name>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-112">-Department "\<department name>"</span></span>
    
- <span data-ttu-id="4a6f1-113">-DisplayName "\<full user name>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-113">-DisplayName "\<full user name>"</span></span>
    
- <span data-ttu-id="4a6f1-114">-FacsimilieTelephoneNumber "<numéro de télécopie>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-114">-FacsimilieTelephoneNumber "\<fax number>"</span></span>
    
- <span data-ttu-id="4a6f1-115">-GivenName "<prénom de l'utilisateur>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-115">-GivenName "\<user first name>"</span></span>
    
- <span data-ttu-id="4a6f1-116">-Surname "<nom de famille de l'utilisateur>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-116">-Surname "\<user last name>"</span></span>
    
- <span data-ttu-id="4a6f1-117">-Mobile "<N° de téléphone portable>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-117">-Mobile "\<mobile phone number>"</span></span>
    
- <span data-ttu-id="4a6f1-118">-JobTitle "\<job title>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-118">-JobTitle "\<job title>"</span></span>
    
- <span data-ttu-id="4a6f1-119">-PreferredLanguage "\<language>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-119">-PreferredLanguage "\<language>"</span></span>
    
- <span data-ttu-id="4a6f1-120">-StreetAddress "\<street address>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-120">-StreetAddress "\<street address>"</span></span>
    
- <span data-ttu-id="4a6f1-121">-City "\<city name>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-121">-City "\<city name>"</span></span>
    
- <span data-ttu-id="4a6f1-122">-State "<nom de l'État>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-122">-State "\<state name>"</span></span>
    
- <span data-ttu-id="4a6f1-123">-PostalCode "\<postal code></span><span class="sxs-lookup"><span data-stu-id="4a6f1-123">-PostalCode "\<postal code>"</span></span>
    
- <span data-ttu-id="4a6f1-124">-Country "\<country name>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-124">-Country "\<country name>"</span></span>
    
- <span data-ttu-id="4a6f1-125">-TelephoneNumber "<numéro de téléphone du bureau>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-125">-TelephoneNumber "\<office phone number>"</span></span>
    
- <span data-ttu-id="4a6f1-126">-UsageLocation " \<2-character country or region code> "</span><span class="sxs-lookup"><span data-stu-id="4a6f1-126">-UsageLocation "\<2-character country or region code>"</span></span>
    
    <span data-ttu-id="4a6f1-127">Voici le code de la région ou du pays à deux lettres ISO 3166-1 alpha-2 (A2).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-127">This is the ISO 3166-1 alpha-2 (A2) two-letter country or region code.</span></span>
    
<span data-ttu-id="4a6f1-128">Pour consulter des paramètres supplémentaires, reportez-vous à [Set-AzureADUser](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-128">See [Set-AzureADUser](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser) for additional parameters.</span></span>

>[!Note]
><span data-ttu-id="4a6f1-129">Avant de pouvoir attribuer des licences à un compte d’utilisateur, vous devez affecter un emplacement d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-129">Before you can assign licenses to a user account, you must assign a usage location.</span></span>
>

<span data-ttu-id="4a6f1-130">Pour afficher le nom d’utilisateur principal pour vos comptes d’utilisateur, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-130">To display the User Principal Name for your user accounts, run the following command.</span></span>
  
```powershell
Get-AzureADUser | Sort UserPrincipalName | Select UserPrincipalName | More
```

<span data-ttu-id="4a6f1-131">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-131">This command instructs PowerShell to:</span></span>
  
- <span data-ttu-id="4a6f1-132">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-AzureADUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-132">Get all of the information on the user accounts (**Get-AzureADUser**) and send it to the next command (**|**).</span></span>
    
- <span data-ttu-id="4a6f1-133">Trier par ordre alphabétique la liste des noms d’utilisateur principaux (**sort userPrincipalName**) et l’envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-133">Sort the list of User Principal Names alphabetically (**Sort UserPrincipalName**) and send it to the next command (**|**).</span></span>
    
- <span data-ttu-id="4a6f1-134">Afficher uniquement la propriété nom d’utilisateur principal pour chaque compte (**Sélectionnez userPrincipalName**).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-134">Display just the User Principal Name property for each account (**Select UserPrincipalName**).</span></span>

- <span data-ttu-id="4a6f1-135">Afficher un écran à la fois (**Plus**).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-135">Display them one screen at a time (**More**).</span></span>
    
<span data-ttu-id="4a6f1-136">Cette commande répertorie tous vos comptes.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-136">This command will list all of your accounts.</span></span> <span data-ttu-id="4a6f1-137">Si vous souhaitez afficher le nom d’utilisateur principal d’un compte en fonction de son nom d’affichage (prénom et nom), renseignez la variable **$username** ci-dessous (en supprimant les \< and > caractères), puis exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-137">If you want to display the User Principal Name for an account based on its display name (first and last name), fill in the **$userName** variable below (removing the \< and > characters), and then run the following commands:</span></span>
  
```powershell
$userName="<Display name>"
Write-Host (Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="4a6f1-138">Cet exemple affiche le nom d’utilisateur principal pour le compte l’utilisateur avec Caleb Sills comme nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-138">This example displays the User Principal Name for the user account with the display name of Caleb Sills.</span></span>
  
```powershell
$userName="Caleb Sills"
Write-Host (Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="4a6f1-p103">En utilisant une variable **$upn**, vous pouvez apporter des modifications à des comptes individuels en fonction de leur nom d'affichage. Voici un exemple de définition de l'emplacement d'utilisation de Belinda Newman en France, mais en spécifiant son nom d'affichage plutôt que son nom d'utilisateur principal :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-p103">By using a **$upn** variable, you can make changes to individual accounts based on their display name. Here is an example of setting Belinda Newman's usage location to France, but specifying her display name rather than her User Principal Name:</span></span>
  
```powershell
$userName="Belinda Newman"
$upn=(Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
Set-AzureADUser -ObjectID $upn -UsageLocation "FR"
```

### <a name="change-properties-for-all-user-accounts"></a><span data-ttu-id="4a6f1-141">Modification des propriétés de tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4a6f1-141">Change properties for all user accounts</span></span>

<span data-ttu-id="4a6f1-p104">Afin de modifier les propriétés pour tous les utilisateurs, vous pouvez utiliser la combinaison des cmdlets **Get-AzureADUser** et **Set-AzureADUser**. L'exemple suivant modifie l'emplacement d'utilisation pour tous les utilisateurs et définit la France comme nouvel emplacement :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-p104">To change properties for all users, you can use the combination of the **Get-AzureADUser** and **Set-AzureADUser** cmdlets. The following example changes the usage location for all users to France:</span></span>
  
```powershell
Get-AzureADUser | Set-AzureADUser -UsageLocation "FR"
```

<span data-ttu-id="4a6f1-144">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-144">This command instructs PowerShell to:</span></span>
  
- <span data-ttu-id="4a6f1-145">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-AzureADUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-145">Get all of the information on the user accounts (**Get-AzureADUser**) and send it to the next command (**|**).</span></span>
    
- <span data-ttu-id="4a6f1-146">Définissez la France comme emplacement de l’utilisateur (**Set-AzureADUser-UsageLocation "fr"**).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-146">Set the user location to France (**Set-AzureADUser -UsageLocation "FR"**).</span></span>
    
### <a name="change-properties-for-a-specific-set-of-user-accounts"></a><span data-ttu-id="4a6f1-147">Modification des propriétés d’un ensemble spécifique de comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4a6f1-147">Change properties for a specific set of user accounts</span></span>

<span data-ttu-id="4a6f1-p105">Pour modifier les propriétés d’un ensemble spécifique de comptes d’utilisateur, vous pouvez utiliser la combinaison des cmdlets **Get-AzureADUser**, **Where** et **Set-AzureADUser**. L’exemple suivant modifie l’emplacement d’utilisation pour tous les utilisateurs du service Accounting et définit la France comme nouvel emplacement :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-p105">To change properties for a specific set of user account, you can use the combination of the **Get-AzureADUser**, **Where**, and **Set-AzureADUser** cmdlets. The following example changes the usage location for all the users in the Accounting department to France:</span></span>
  
```powershell
Get-AzureADUser | Where {$_.Department -eq "Accounting"} | Set-AzureADUser -UsageLocation "FR"
```

<span data-ttu-id="4a6f1-150">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-150">This command instructs PowerShell to:</span></span>
  
- <span data-ttu-id="4a6f1-151">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-AzureADUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-151">Get all of the information on the user accounts (**Get-AzureADUser**) and send it to the next command (**|**).</span></span>
    
- <span data-ttu-id="4a6f1-152">Recherchez tous les comptes d’utilisateur dont la propriété Department est définie sur « Accounting » (**where {$ _. Department-EQ "Accounting"}**) et envoyer les informations obtenues à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-152">Find all of the user accounts that have their Department property set to "Accounting" (**Where {$_.Department -eq "Accounting"}**) and send the resulting information to the next command (**|**).</span></span>
    
- <span data-ttu-id="4a6f1-153">Définissez la France comme emplacement de l’utilisateur (**Set-AzureADUser-UsageLocation "fr"**).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-153">Set the user location to France (**Set-AzureADUser -UsageLocation "FR"**).</span></span>
    
## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="4a6f1-154">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-154">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="4a6f1-155">Pour configurer les propriétés des comptes d’utilisateur avec le module Microsoft Azure Active Directory pour Windows PowerShell, utilisez la cmdlet **Set-MsolUser** et spécifiez les propriétés à définir ou à modifier.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-155">To configure properties for user accounts with the Microsoft Azure Active Directory Module for Windows PowerShell, you use the **Set-MsolUser** cmdlet and specify the properties to set or change.</span></span> 

<span data-ttu-id="4a6f1-156">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-156">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>
  
>[!Note]
><span data-ttu-id="4a6f1-157">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-157">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="4a6f1-158">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-158">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

### <a name="change-properties-for-a-specific-user-account"></a><span data-ttu-id="4a6f1-159">Modification des propriétés d’un compte d’utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="4a6f1-159">Change properties for a specific user account</span></span>

<span data-ttu-id="4a6f1-160">Pour configurer les propriétés d’un compte d’utilisateur spécifique, vous utilisez la cmdlet [Set-MsolUser](https://docs.microsoft.com/previous-versions/azure/dn194136(v=azure.100)) et spécifiez les propriétés de définition ou de modification.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-160">To configure properties for a specific user account, you use the [Set-MsolUser](https://docs.microsoft.com/previous-versions/azure/dn194136(v=azure.100)) cmdlet and specify the properties to set or change.</span></span> 

<span data-ttu-id="4a6f1-p107">Identifiez le compte avec le paramètre **-UserPrincipalName** et définissez ou modifiez des propriétés spécifiques à l'aide de paramètres supplémentaires. Voici la liste des principaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-p107">You identify the account with the **-UserPrincipalName** parameter and set or change specific properties with additional parameters. Here is a list of the most common parameters.</span></span>
  
- <span data-ttu-id="4a6f1-163">-City "\<city name>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-163">-City "\<city name>"</span></span>
    
- <span data-ttu-id="4a6f1-164">-Country "\<country name>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-164">-Country "\<country name>"</span></span>
    
- <span data-ttu-id="4a6f1-165">-Department "\<department name>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-165">-Department "\<department name>"</span></span>
    
- <span data-ttu-id="4a6f1-166">-DisplayName "\<full user name>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-166">-DisplayName "\<full user name>"</span></span>
    
- <span data-ttu-id="4a6f1-167">-Fax "<numéro de fax>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-167">-Fax "\<fax number>"</span></span>
    
- <span data-ttu-id="4a6f1-168">-FirstName "<prénom de l'utilisateur>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-168">-FirstName "\<user first name>"</span></span>
    
- <span data-ttu-id="4a6f1-169">-LastName "<nom de famille de l'utilisateur>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-169">-LastName "\<user last name>"</span></span>
    
- <span data-ttu-id="4a6f1-170">-MobilePhone "<numéro de téléphone portable>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-170">-MobilePhone "\<mobile phone number>"</span></span>
    
- <span data-ttu-id="4a6f1-171">-Office "\<office location>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-171">-Office "\<office location>"</span></span>
    
- <span data-ttu-id="4a6f1-172">-PhoneNumber "<numéro de téléphone du bureau>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-172">-PhoneNumber "\<office phone number>"</span></span>
    
- <span data-ttu-id="4a6f1-173">-PostalCode "\<postal code></span><span class="sxs-lookup"><span data-stu-id="4a6f1-173">-PostalCode "\<postal code>"</span></span>
    
- <span data-ttu-id="4a6f1-174">-PreferredLanguage "\<language>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-174">-PreferredLanguage "\<language>"</span></span>
    
- <span data-ttu-id="4a6f1-175">-State "<nom de l'État>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-175">-State "\<state name>"</span></span>
    
- <span data-ttu-id="4a6f1-176">-StreetAddress "\<street address>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-176">-StreetAddress "\<street address>"</span></span>
    
- <span data-ttu-id="4a6f1-177">-Title "<intitulé du poste>"</span><span class="sxs-lookup"><span data-stu-id="4a6f1-177">-Title "\<title name>"</span></span>
    
- <span data-ttu-id="4a6f1-178">-UsageLocation " \<2-character country or region code> "</span><span class="sxs-lookup"><span data-stu-id="4a6f1-178">-UsageLocation "\<2-character country or region code>"</span></span>
    
    <span data-ttu-id="4a6f1-179">Voici le code de la région ou du pays à deux lettres ISO 3166-1 alpha-2 (A2).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-179">This is the ISO 3166-1 alpha-2 (A2) two-letter country or region code.</span></span>
    
<span data-ttu-id="4a6f1-180">Pour obtenir plus de paramètres, voir [Set-MsolUser](https://docs.microsoft.com/previous-versions/azure/dn194136(v=azure.100)).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-180">See [Set-MsolUser](https://docs.microsoft.com/previous-versions/azure/dn194136(v=azure.100)) for additional parameters.</span></span>

<span data-ttu-id="4a6f1-181">Pour afficher les noms d’utilisateur principaux de tous vos utilisateurs, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-181">To see the User Principal Names of all your users, run the following command.</span></span>
  
```powershell
Get-MSolUser | Sort UserPrincipalName | Select UserPrincipalName | More
```

<span data-ttu-id="4a6f1-182">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-182">This command instructs PowerShell to:</span></span>
  
- <span data-ttu-id="4a6f1-183">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-MsolUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-183">Get all of the information on the user accounts (**Get-MsolUser**) and send it to the next command (**|**).</span></span>
    
- <span data-ttu-id="4a6f1-184">Trier par ordre alphabétique la liste des noms d’utilisateur principaux (**sort userPrincipalName**) et l’envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-184">Sort the list of User Principal Names alphabetically (**Sort UserPrincipalName**) and send it to the next command (**|**).</span></span>
    
- <span data-ttu-id="4a6f1-185">Afficher uniquement la propriété nom d’utilisateur principal pour chaque compte (**Sélectionnez userPrincipalName**).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-185">Display just the User Principal Name property for each account (**Select UserPrincipalName**).</span></span>
    
- <span data-ttu-id="4a6f1-186">Afficher un écran à la fois (**Plus**).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-186">Display them one screen at a time (**More**).</span></span>
    
<span data-ttu-id="4a6f1-187">Cette commande répertorie tous vos comptes.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-187">This command will list all of your accounts.</span></span> <span data-ttu-id="4a6f1-188">Si vous souhaitez afficher le nom d’utilisateur principal d’un compte en fonction de son nom d’affichage (prénom et nom), renseignez la variable **$username** ci-dessous (en supprimant les \< and > caractères), puis exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-188">If you want to display the User Principal Name for an account based on its display name (first and last name), fill in the **$userName** variable below (removing the \< and > characters), and then run the following commands:</span></span>
  
```powershell
$userName="<Display name>"
Write-Host (Get-MsolUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="4a6f1-189">Cet exemple affiche le nom d’utilisateur principal de l’utilisateur nommé Caleb Sills.</span><span class="sxs-lookup"><span data-stu-id="4a6f1-189">This example displays the User Principal Name for the user named Caleb Sills.</span></span>
  
```powershell
$userName="Caleb Sills"
Write-Host (Get-MsolUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="4a6f1-p109">En utilisant une variable **$upn**, vous pouvez apporter des modifications à des comptes individuels en fonction de leur nom d'affichage. Voici un exemple de définition de l'emplacement d'utilisation de Belinda Newman en France, mais en spécifiant son nom d'affichage plutôt que son nom d'utilisateur principal :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-p109">By using a **$upn** variable, you can make changes to individual accounts based on their display name. Here is an example of setting Belinda Newman's usage location to France, but specifying her display name rather than her User Principal Name:</span></span>
  
```powershell
$userName="<display name>"
$upn=(Get-MsolUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
Set-MsolUser -UserPrincipalName $upn -UsageLocation "FR"
```

### <a name="change-properties-for-all-user-accounts"></a><span data-ttu-id="4a6f1-192">Modification des propriétés de tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4a6f1-192">Change properties for all user accounts</span></span>

<span data-ttu-id="4a6f1-p110">Pour modifier les propriétés pour tous les utilisateurs, vous pouvez utiliser la combinaison des cmdlets **Get-MsolUser** et **Set-MsolUser**. L'exemple suivant modifie l'emplacement d'utilisation pour tous les utilisateurs et définit la France comme nouvel emplacement :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-p110">To change properties for all users, you can use the combination of the **Get-MsolUser** and **Set-MsolUser** cmdlets. The following example changes the usage location for all users to France:</span></span>
  
```powershell
Get-MsolUser | Set-MsolUser -UsageLocation "FR"
```

<span data-ttu-id="4a6f1-195">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-195">This command instructs PowerShell to:</span></span>
  
- <span data-ttu-id="4a6f1-196">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-MsolUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-196">Get all of the information on the user accounts (**Get-MsolUser**) and send it to the next command (**|**).</span></span>
    
- <span data-ttu-id="4a6f1-197">Définissez la France comme emplacement de l’utilisateur (**Set-MsolUser-UsageLocation "fr"**).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-197">Set the user location to France (**Set-MsolUser -UsageLocation "FR"**).</span></span>
    
### <a name="change-properties-for-a-specific-set-of-user-accounts"></a><span data-ttu-id="4a6f1-198">Modification des propriétés d’un ensemble spécifique de comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4a6f1-198">Change properties for a specific set of user accounts</span></span>

<span data-ttu-id="4a6f1-199">Pour modifier les propriétés d’un ensemble spécifique de compte d’utilisateur, vous pouvez utiliser la combinaison des cmdlets **Get-MsolUser**, **Where**et **Set-MsolUser** .</span><span class="sxs-lookup"><span data-stu-id="4a6f1-199">To change properties for a specific set of user account, you can use the combination of the **Get-MsolUser**, **Where**, and **Set-MsolUser** cmdlets.</span></span> <span data-ttu-id="4a6f1-200">L'exemple suivant modifie l'emplacement d'utilisation pour tous les utilisateurs du service Accounting et définit la France comme nouvel emplacement :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-200">The following example changes the usage location for all the users in the Accounting department to France:</span></span>
  
```powershell
Get-MsolUser | Where {$_.Department -eq "Accounting"} | Set-MsolUser -UsageLocation "FR"
```

<span data-ttu-id="4a6f1-201">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="4a6f1-201">This command instructs PowerShell to:</span></span>
  
- <span data-ttu-id="4a6f1-202">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-MsolUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-202">Get all of the information on the user accounts (**Get-MsolUser**) and send it to the next command (**|**).</span></span>
    
- <span data-ttu-id="4a6f1-203">Recherchez tous les comptes d’utilisateur dont la propriété Department est définie sur « Accounting » (**where {$ _. Department-EQ "Accounting"}**) et envoyer les informations obtenues à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-203">Find all of the user accounts that have their Department property set to "Accounting" (**Where {$_.Department -eq "Accounting"}**) and send the resulting information to the next command (**|**).</span></span>
    
- <span data-ttu-id="4a6f1-204">Définissez la France comme emplacement de l’utilisateur (**Set-MsolUser-UsageLocation "fr"**).</span><span class="sxs-lookup"><span data-stu-id="4a6f1-204">Set the user location to France (**Set-MsolUser -UsageLocation "FR"**).</span></span>


## <a name="see-also"></a><span data-ttu-id="4a6f1-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a6f1-205">See also</span></span>

[<span data-ttu-id="4a6f1-206">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="4a6f1-206">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="4a6f1-207">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="4a6f1-207">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="4a6f1-208">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4a6f1-208">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
