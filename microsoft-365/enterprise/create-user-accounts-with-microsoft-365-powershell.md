---
title: Créer des comptes d’utilisateur Microsoft 365 avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/17/2020
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
- seo-marvel-apr2020
ms.assetid: 6770c5fa-b886-4512-8c67-ffd53226589e
description: Dans cet article, Découvrez comment utiliser PowerShell pour créer des comptes d’utilisateurs ou plusieurs comptes d’utilisateur Microsoft 365.
ms.openlocfilehash: 53077352862b6d0df6bb569300e2d8bc2475df91
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689991"
---
# <a name="create-microsoft-365-user-accounts-with-powershell"></a><span data-ttu-id="6c2f0-103">Créer des comptes d’utilisateur Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c2f0-103">Create Microsoft 365 user accounts with PowerShell</span></span>

<span data-ttu-id="6c2f0-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="6c2f0-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="6c2f0-105">Vous pouvez utiliser PowerShell pour Microsoft 365 pour créer efficacement des comptes d’utilisateur, notamment plusieurs comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-105">You can use PowerShell for Microsoft 365 to efficiently create user accounts, especially multiple user accounts.</span></span> <span data-ttu-id="6c2f0-106">Lorsque vous créez des comptes d’utilisateur dans PowerShell, certaines propriétés de compte sont toujours obligatoires.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-106">When you create user accounts in PowerShell, certain account properties are always required.</span></span> <span data-ttu-id="6c2f0-107">D'autres propriétés ne sont pas nécessaires pour la création du compte, mais sont importantes.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-107">Other properties aren't required to create the account, but are otherwise important.</span></span> <span data-ttu-id="6c2f0-108">Ces propriétés sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="6c2f0-108">These properties are described in the following table:</span></span>
  
|<span data-ttu-id="6c2f0-109">**Nom de la propriété**</span><span class="sxs-lookup"><span data-stu-id="6c2f0-109">**Property name**</span></span>|<span data-ttu-id="6c2f0-110">**Requis ?**</span><span class="sxs-lookup"><span data-stu-id="6c2f0-110">**Required?**</span></span>|<span data-ttu-id="6c2f0-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="6c2f0-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c2f0-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="6c2f0-112">**DisplayName**</span></span> <br/> |<span data-ttu-id="6c2f0-113">Oui</span><span class="sxs-lookup"><span data-stu-id="6c2f0-113">Yes</span></span>  <br/> |<span data-ttu-id="6c2f0-114">Il s’agit du nom complet utilisé dans les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-114">This is the display name that's used in Microsoft 365 services.</span></span> <span data-ttu-id="6c2f0-115">Par exemple, Caleb Sills.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-115">For example, Caleb Sills.</span></span>  <br/> |
|<span data-ttu-id="6c2f0-116">**UserPrincipalName**</span><span class="sxs-lookup"><span data-stu-id="6c2f0-116">**UserPrincipalName**</span></span> <br/> |<span data-ttu-id="6c2f0-117">Oui</span><span class="sxs-lookup"><span data-stu-id="6c2f0-117">Yes</span></span>  <br/> |<span data-ttu-id="6c2f0-118">Il s’agit du nom de compte utilisé pour se connecter aux services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-118">This is the account name that's used to sign in to Microsoft 365 services.</span></span> <span data-ttu-id="6c2f0-119">Par exemple, CalebS@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-119">For example, CalebS@contoso.onmicrosoft.com.</span></span>  <br/> |
|<span data-ttu-id="6c2f0-120">**FirstName**</span><span class="sxs-lookup"><span data-stu-id="6c2f0-120">**FirstName**</span></span> <br/> |<span data-ttu-id="6c2f0-121">Non</span><span class="sxs-lookup"><span data-stu-id="6c2f0-121">No</span></span>  <br/> ||
|<span data-ttu-id="6c2f0-122">**NomFamille**</span><span class="sxs-lookup"><span data-stu-id="6c2f0-122">**LastName**</span></span> <br/> |<span data-ttu-id="6c2f0-123">Non</span><span class="sxs-lookup"><span data-stu-id="6c2f0-123">No</span></span>  <br/> ||
|<span data-ttu-id="6c2f0-124">**LicenseAssignment**</span><span class="sxs-lookup"><span data-stu-id="6c2f0-124">**LicenseAssignment**</span></span> <br/> |<span data-ttu-id="6c2f0-125">Non</span><span class="sxs-lookup"><span data-stu-id="6c2f0-125">No</span></span>  <br/> |<span data-ttu-id="6c2f0-126">Il s’agit du plan de gestion des licences (également appelé plan de licence ou SKU) à partir duquel une licence disponible est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-126">This is the licensing plan (also known as the license plan or SKU) from which an available license is assigned to the user account.</span></span> <span data-ttu-id="6c2f0-127">La licence définit les services Microsoft 365 disponibles pour le compte.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-127">The license defines the Microsoft 365 services that are available to account.</span></span> <span data-ttu-id="6c2f0-128">Vous n’êtes pas obligé d’attribuer une licence à un utilisateur lorsque vous créez le compte, mais le compte nécessite une licence pour accéder aux services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-128">You don't have to assign a license to a user when you create the account, but the account requires a license to access Microsoft 365 services.</span></span> <span data-ttu-id="6c2f0-129">Vous disposez de 30 jours pour attribuer une licence à un compte d'utilisateur après sa création.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-129">You have 30 days to license the user account after you create it.</span></span> |
|<span data-ttu-id="6c2f0-130">**Password**</span><span class="sxs-lookup"><span data-stu-id="6c2f0-130">**Password**</span></span> <br/> |<span data-ttu-id="6c2f0-131">Non</span><span class="sxs-lookup"><span data-stu-id="6c2f0-131">No</span></span>  <br/> | <span data-ttu-id="6c2f0-p105">Si vous n’indiquez pas de mot de passe, un mot de passe aléatoire est affecté au compte d’utilisateur et le mot de passe est visible dans les résultats de la commande. Si vous spécifiez un mot de passe, il doit être composé de 8 à 16 caractères ASCII de l'un des trois types suivants : lettres minuscules, lettres majuscules, chiffres et symboles.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-p105">If you don't specify a password, a random password is assigned to the user account, and the password is visible in the results of the command. If you specify a password, it needs to be 8 to 16 ASCII text characters from any three of the following types: lowercase letters, uppercase letters, numbers, and symbols.</span></span> <br/> |
|<span data-ttu-id="6c2f0-134">**UsageLocation**</span><span class="sxs-lookup"><span data-stu-id="6c2f0-134">**UsageLocation**</span></span> <br/> |<span data-ttu-id="6c2f0-135">Non</span><span class="sxs-lookup"><span data-stu-id="6c2f0-135">No</span></span>  <br/> |<span data-ttu-id="6c2f0-136">Il s’agit d’un code ISO 3166-1 alpha-2 valide.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-136">This is a valid ISO 3166-1 alpha-2 country code.</span></span> <span data-ttu-id="6c2f0-137">Par exemple, US pour les États-Unis et FR pour la France.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-137">For example, US for the United States, and FR for France.</span></span> <span data-ttu-id="6c2f0-138">Il est important de fournir cette valeur, car certains services Microsoft 365 ne sont pas disponibles dans certains pays, de sorte que vous ne pouvez pas attribuer une licence à un compte d’utilisateur sauf si cette valeur est configurée pour le compte.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-138">It's important to provide this value, because some Microsoft 365 services aren't available in certain countries, so you can't assign a license to a user account unless the account has this value configured.</span></span> <span data-ttu-id="6c2f0-139">Pour plus d’informations, consultez la rubrique [à propos des restrictions de licence](https://go.microsoft.com/fwlink/p/?LinkId=691730).</span><span class="sxs-lookup"><span data-stu-id="6c2f0-139">For more information, see [About license restrictions](https://go.microsoft.com/fwlink/p/?LinkId=691730).</span></span>  <br/> |
   

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="6c2f0-140">Utilisez le module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="6c2f0-140">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="6c2f0-141">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="6c2f0-141">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>

<span data-ttu-id="6c2f0-142">Une fois connecté, utilisez la syntaxe suivante pour créer un compte individuel :</span><span class="sxs-lookup"><span data-stu-id="6c2f0-142">After you have connected, use the following syntax to create an individual account:</span></span>
  
```powershell
$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password="<user account password>"
New-AzureADUser -DisplayName "<display name>" -GivenName "<first name>" -SurName "<last name>" -UserPrincipalName <sign-in name> -UsageLocation <ISO 3166-1 alpha-2 country code> -MailNickName <mailbox name> -PasswordProfile $PasswordProfile -AccountEnabled $true
```

<span data-ttu-id="6c2f0-143">L’exemple suivant crée un compte pour l’utilisateur américain appelé Caleb Sills :</span><span class="sxs-lookup"><span data-stu-id="6c2f0-143">This example creates an account for the United States user named Caleb Sills:</span></span>
  
```powershell
$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password="3Rv0y1q39/chsy"
New-AzureADUser -DisplayName "Caleb Sills" -GivenName "Caleb" -SurName "Sills" -UserPrincipalName calebs@contoso.onmicrosoft.com -UsageLocation US -MailNickName calebs -PasswordProfile $PasswordProfile -AccountEnabled $true
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="6c2f0-144">Utilisez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-144">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="6c2f0-145">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="6c2f0-145">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

### <a name="create-an-individual-user-account"></a><span data-ttu-id="6c2f0-146">Créez un compte d’utilisateur individuel</span><span class="sxs-lookup"><span data-stu-id="6c2f0-146">Create an individual user account</span></span>

<span data-ttu-id="6c2f0-147">Pour créer un compte individuel, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6c2f0-147">To create an individual account, use the following syntax:</span></span>
  
```powershell
New-MsolUser -DisplayName <display name> -FirstName <first name> -LastName <last name> -UserPrincipalName <sign-in name> -UsageLocation <ISO 3166-1 alpha-2 country code> -LicenseAssignment <licensing plan name> [-Password <Password>]
```

>[!Note]
><span data-ttu-id="6c2f0-148">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-148">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="6c2f0-149">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-149">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

<span data-ttu-id="6c2f0-150">Pour répertorier les noms des plans de gestion des licences disponibles, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6c2f0-150">To list the available licensing plan names, use this command:</span></span>

````powershell
Get-MsolAccountSku
````

<span data-ttu-id="6c2f0-151">Cet exemple crée un compte pour l’utilisateur nommé Caleb Sills et situé aux États-Unis, et affecte une licence à partir du plan de gestion des licences `contoso:ENTERPRISEPACK` (Office 365 Entreprise E3).</span><span class="sxs-lookup"><span data-stu-id="6c2f0-151">This example creates an account for the United States user named Caleb Sills, and assigns a license from the `contoso:ENTERPRISEPACK` (Office 365 Enterprise E3) licensing plan.</span></span>
  
```powershell
New-MsolUser -DisplayName "Caleb Sills" -FirstName Caleb -LastName Sills -UserPrincipalName calebs@contoso.onmicrosoft.com -UsageLocation US -LicenseAssignment contoso:ENTERPRISEPACK
```

### <a name="create-multiple-user-accounts"></a><span data-ttu-id="6c2f0-152">Créez plusieurs comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6c2f0-152">Create multiple user accounts</span></span>

1. <span data-ttu-id="6c2f0-p108">Créez un fichier CSV (valeurs séparées par des virgules) qui contient les informations de compte d’utilisateur requises. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6c2f0-p108">Create a comma-separated value (CSV) file that contains the required user account information. For example:</span></span>
    
  ```powershell
  UserPrincipalName,FirstName,LastName,DisplayName,UsageLocation,AccountSkuId
  ClaudeL@contoso.onmicrosoft.com,Claude,Loiselle,Claude Loiselle,US,contoso:ENTERPRISEPACK
  LynneB@contoso.onmicrosoft.com,Lynne,Baxter,Lynne Baxter,US,contoso:ENTERPRISEPACK
  ShawnM@contoso.onmicrosoft.com,Shawn,Melendez,Shawn Melendez,US,contoso:ENTERPRISEPACK
  ```

 > [!NOTE]
><span data-ttu-id="6c2f0-155">Les noms de colonne et leur ordre dans la première ligne du fichier CSV sont arbitraires, mais assurez-vous que les données dans le reste du fichier correspondent à l’ordre des noms de colonne et utilisez les noms de colonne pour les valeurs de paramètre dans la commande PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-155">The column names and their order in the first row of the CSV file are arbitrary, but make sure the data in the rest of the file matches the order of the column names, and use the column names for the parameter values in the PowerShell for Microsoft 365 command.</span></span>
    
2. <span data-ttu-id="6c2f0-156">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6c2f0-156">Use the following syntax:</span></span>
    
  ```powershell
  Import-Csv -Path <Input CSV File Path and Name> | foreach {New-MsolUser -DisplayName $_.DisplayName -FirstName $_.FirstName -LastName $_.LastName -UserPrincipalName $_.UserPrincipalName -UsageLocation $_.UsageLocation -LicenseAssignment $_.AccountSkuId [-Password $_.Password]} | Export-Csv -Path <Output CSV File Path and Name>
  ```

<span data-ttu-id="6c2f0-157">Cet exemple crée des comptes d’utilisateurs à partir du fichier nommé C:\My Documents\NewAccounts.csv et enregistre les résultats dans le fichier nommé C:\My Documents\NewAccountResults.csv.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-157">This example creates the user accounts from the file named C:\My Documents\NewAccounts.csv, and logs the results in the file named C:\My Documents\NewAccountResults.csv</span></span>
    
  ```powershell
  Import-Csv -Path "C:\My Documents\NewAccounts.csv" | foreach {New-MsolUser -DisplayName $_.DisplayName -FirstName $_.FirstName -LastName $_.LastName -UserPrincipalName $_.UserPrincipalName -UsageLocation $_.UsageLocation -LicenseAssignment $_.AccountSkuId} | Export-Csv -Path "C:\My Documents\NewAccountResults.csv"
  ```

3. <span data-ttu-id="6c2f0-158">Passez en revue le fichier de sortie pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-158">Review the output file to see the results.</span></span> <span data-ttu-id="6c2f0-159">Les mots de passe ne sont pas spécifiés, de sorte que les mots de passe aléatoires générés par Microsoft 365 sont visibles dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="6c2f0-159">We didn't specify passwords, so the random passwords that Microsoft 365 generated are visible in the output file.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c2f0-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c2f0-160">See also</span></span>

[<span data-ttu-id="6c2f0-161">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c2f0-161">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="6c2f0-162">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c2f0-162">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="6c2f0-163">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6c2f0-163">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
