---
title: Bloquer Microsoft 365 comptes d’utilisateurs avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/16/2020
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
- seo-marvel-apr2020
ms.assetid: 04e58c2a-400b-496a-acd4-8ec5d37236dc
description: Comment utiliser PowerShell pour bloquer et débloquer l’accès Microsoft 365 comptes.
ms.openlocfilehash: c1a79d925965fafd796033182098e68e26a81473
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48754679"
---
# <a name="block-microsoft-365-user-accounts-with-powershell"></a><span data-ttu-id="66195-103">Bloquer Microsoft 365 comptes d’utilisateurs avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="66195-103">Block Microsoft 365 user accounts with PowerShell</span></span>

<span data-ttu-id="66195-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="66195-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="66195-105">Lorsque vous bloquez l’accès à un compte Microsoft 365, vous empêchez quiconque d’utiliser le compte pour se connecter et accéder aux services et données de votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="66195-105">When you block access to a Microsoft 365 account, you prevent anyone from using the account to sign in and access the services and data in your Microsoft 365 organization.</span></span> <span data-ttu-id="66195-106">Vous pouvez utiliser PowerShell pour bloquer l’accès à des comptes d’utilisateur individuels ou multiples.</span><span class="sxs-lookup"><span data-stu-id="66195-106">You can use PowerShell to block access to individual or multiple user accounts.</span></span>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="66195-107">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="66195-107">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="66195-108">Tout [d’abord, connectez-vous à Microsoft 365 client.](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="66195-108">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
 
### <a name="block-access-to-individual-user-accounts"></a><span data-ttu-id="66195-109">Bloquer l’accès à des comptes d’utilisateurs individuels</span><span class="sxs-lookup"><span data-stu-id="66195-109">Block access to individual user accounts</span></span>

<span data-ttu-id="66195-110">Utilisez la syntaxe suivante pour bloquer un compte d’utilisateur individuel :</span><span class="sxs-lookup"><span data-stu-id="66195-110">Use the following syntax to block an individual user account:</span></span>
  
```powershell
Set-AzureADUser -ObjectID <sign-in name of the user account> -AccountEnabled $false
```

> [!NOTE]
> <span data-ttu-id="66195-111">Le *paramètre -ObjectID* dans la cmdlet **Set-AzureAD** accepte soit le nom de la signature du compte, également appelé nom d’utilisateur principal, soit l’ID d’objet du compte.</span><span class="sxs-lookup"><span data-stu-id="66195-111">The *-ObjectID* parameter in the **Set-AzureAD** cmdlet accepts either the account sign-in name, also known as the User Principal Name, or the account's object ID.</span></span>
  
<span data-ttu-id="66195-112">Cet exemple bloque l’accès au compte *d’fabricec@litwareinc.com*.</span><span class="sxs-lookup"><span data-stu-id="66195-112">This example blocks access to the user account *fabricec@litwareinc.com*.</span></span>
  
```powershell
Set-AzureADUser -ObjectID fabricec@litwareinc.com -AccountEnabled $false
```

<span data-ttu-id="66195-113">Pour débloquer ce compte, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66195-113">To unblock this user account, run the following command:</span></span>
  
```powershell
Set-AzureADUser -ObjectID fabricec@litwareinc.com -AccountEnabled $true
```

<span data-ttu-id="66195-114">Pour afficher l’UPN du compte d’utilisateur en fonction du nom d’affichage de l’utilisateur, utilisez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="66195-114">To display the user account UPN based on the user's display name, use the following commands:</span></span>
  
```powershell
$userName="<display name>"
Write-Host (Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName

```

<span data-ttu-id="66195-115">Cet exemple affiche l’UPN du compte d’utilisateur pour  *l’utilisateur Caleb Sills*.</span><span class="sxs-lookup"><span data-stu-id="66195-115">This example displays the user account UPN for the user  *Caleb Sills*.</span></span>
  
```powershell
$userName="Caleb Sills"
Write-Host (Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="66195-116">Pour bloquer un compte en fonction du nom complet de l’utilisateur, utilisez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="66195-116">To block an account based on the user's display name, use the following commands:</span></span>
  
```powershell
$userName="<display name>"
Set-AzureADUser -ObjectID (Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName -AccountEnabled $false

```

<span data-ttu-id="66195-117">Pour vérifier l’état bloqué d’un compte d’utilisateur, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66195-117">To check the blocked status of a user account use the following command:</span></span>
  
```powershell
Get-AzureADUser -UserPrincipalName <UPN of user account> | Select DisplayName,AccountEnabled
```

### <a name="block-multiple-user-accounts"></a><span data-ttu-id="66195-118">Bloquer plusieurs comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="66195-118">Block multiple user accounts</span></span>

<span data-ttu-id="66195-119">Pour bloquer l’accès à plusieurs comptes d’utilisateurs, créez un fichier texte qui contient un nom de signature de compte sur chaque ligne comme ceci :</span><span class="sxs-lookup"><span data-stu-id="66195-119">To block access for multiple user accounts, create a text file that contains one account sign-in name on each line like this:</span></span>
    
  ```powershell
akol@contoso.com
tjohnston@contoso.com
kakers@contoso.com
  ```

<span data-ttu-id="66195-120">Dans les commandes suivantes, l’exemple de fichier texte est *C:\My Documents\Accounts.txt*.</span><span class="sxs-lookup"><span data-stu-id="66195-120">In the following commands, the example text file is *C:\My Documents\Accounts.txt*.</span></span> <span data-ttu-id="66195-121">Remplacez ce nom de fichier par le chemin d’accès et le nom de fichier de votre fichier texte.</span><span class="sxs-lookup"><span data-stu-id="66195-121">Replace this file name with the path and file name of your text file.</span></span>
  
<span data-ttu-id="66195-122">Pour bloquer l’accès aux comptes indiqués dans le fichier texte, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66195-122">To block access to the accounts listed in the text file, run the following command:</span></span>
    
```powershell
Get-Content "C:\My Documents\Accounts.txt" | ForEach { Set-AzureADUSer -ObjectID $_ -AccountEnabled $false }
```

<span data-ttu-id="66195-123">Pour débloquer les comptes répertoriés dans le fichier texte, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66195-123">To unblock the accounts that are listed in the text file, run the following command:</span></span>
    
```powershell
Get-Content "C:\My Documents\Accounts.txt" | ForEach { Set-AzureADUSer -ObjectID $_ -AccountEnabled $true }
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="66195-124">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="66195-124">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="66195-125">Tout [d’abord, connectez-vous à Microsoft 365 client.](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell)</span><span class="sxs-lookup"><span data-stu-id="66195-125">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>
    
### <a name="block-individual-user-accounts"></a><span data-ttu-id="66195-126">Bloquer des comptes d’utilisateurs individuels</span><span class="sxs-lookup"><span data-stu-id="66195-126">Block individual user accounts</span></span>

<span data-ttu-id="66195-127">Utilisez la syntaxe suivante pour bloquer l’accès à un compte d’utilisateur individuel :</span><span class="sxs-lookup"><span data-stu-id="66195-127">Use the following syntax to block access for an individual user account:</span></span>
  
```powershell
Set-MsolUser -UserPrincipalName <sign-in name of user account>  -BlockCredential $true
```

>[!Note]
><span data-ttu-id="66195-128">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les cmdlets dont le nom comprend *Msol.*</span><span class="sxs-lookup"><span data-stu-id="66195-128">PowerShell Core doesn't support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets that have *Msol* in their name.</span></span> <span data-ttu-id="66195-129">Vous devez exécuter ces cmdlets à partir Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="66195-129">You have to run these cmdlets from Windows PowerShell.</span></span>

<span data-ttu-id="66195-130">Cet exemple bloque l’accès au compte d’utilisateur *fabricec \@ litwareinc.com*.</span><span class="sxs-lookup"><span data-stu-id="66195-130">This example blocks access to the user account *fabricec\@litwareinc.com*.</span></span>
  
```powershell
Set-MsolUser -UserPrincipalName fabricec@litwareinc.com -BlockCredential $true
```

<span data-ttu-id="66195-131">Pour débloquer le compte, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66195-131">To unblock the user account, run the following command:</span></span>
  
```powershell
Set-MsolUser -UserPrincipalName <sign-in name of user account>  -BlockCredential $false
```

<span data-ttu-id="66195-132">Pour vérifier l’état bloqué d’un compte d’utilisateur, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66195-132">To check the blocked status of a user account run the following command:</span></span>
  
```powershell
Get-MsolUser -UserPrincipalName <sign-in name of user account> | Select DisplayName,BlockCredential
```

### <a name="block-access-for-multiple-user-accounts"></a><span data-ttu-id="66195-133">Bloquer l’accès à plusieurs comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="66195-133">Block access for multiple user accounts</span></span>

<span data-ttu-id="66195-134">Tout d’abord, créez un fichier texte qui contient un compte sur chaque ligne comme ceci :</span><span class="sxs-lookup"><span data-stu-id="66195-134">First, create a text file that contains one account on each line like this:</span></span>
    
```powershell
akol@contoso.com
tjohnston@contoso.com
kakers@contoso.com
```

<span data-ttu-id="66195-135">Dans les commandes suivantes, l’exemple de fichier texte est *C:\My Documents\Accounts.txt*.</span><span class="sxs-lookup"><span data-stu-id="66195-135">In the following commands, the example text file is *C:\My Documents\Accounts.txt*.</span></span> <span data-ttu-id="66195-136">Remplacez ce nom de fichier par le chemin d’accès et le nom de fichier de votre fichier texte.</span><span class="sxs-lookup"><span data-stu-id="66195-136">Replace this file name with the path and file name of your text file.</span></span>
    
<span data-ttu-id="66195-137">Pour bloquer l’accès aux comptes répertoriés dans le fichier texte, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66195-137">To block access for the accounts that are listed in the text file, run the following command:</span></span>
    
  ```powershell
  Get-Content "C:\My Documents\Accounts.txt" | ForEach { Set-MsolUser -UserPrincipalName $_ -BlockCredential $true }
  ```
<span data-ttu-id="66195-138">Pour débloquer les comptes indiqués dans le fichier texte, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66195-138">To unblock the accounts listed in the text file, run the following command:</span></span>
    
  ```powershell
  Get-Content "C:\My Documents\Accounts.txt" | ForEach { Set-MsolUser -UserPrincipalName $_ -BlockCredential $false }
  ```

## <a name="see-also"></a><span data-ttu-id="66195-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66195-139">See also</span></span>

[<span data-ttu-id="66195-140">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="66195-140">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="66195-141">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="66195-141">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="66195-142">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="66195-142">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
