---
title: Attribuer des rôles à des comptes d’utilisateur Microsoft 365 avec PowerShell
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
- O365ITProTrain
- PowerShell
- Ent_Office_Other
- seo-marvel-apr2020
ms.assetid: ede7598c-b5d5-4e3e-a488-195f02f26d93
description: Dans cet article, Découvrez comment utiliser rapidement et facilement PowerShell pour Microsoft 365 pour attribuer des rôles à des comptes d’utilisateur.
ms.openlocfilehash: 9df1b018cf3e89e0afbd5265fdd1ec9f92b34aec
ms.sourcegitcommit: c1ee4ed3c5826872b57339e1e1aa33b4d2209711
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2020
ms.locfileid: "48235429"
---
# <a name="assign-roles-to-microsoft-365-user-accounts-with-powershell"></a><span data-ttu-id="84d6f-103">Attribuer des rôles à des comptes d’utilisateur Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="84d6f-103">Assign roles to Microsoft 365 user accounts with PowerShell</span></span>

<span data-ttu-id="84d6f-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="84d6f-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="84d6f-105">Vous pouvez rapidement et facilement attribuer des rôles à des comptes d’utilisateur à l’aide de PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="84d6f-105">You can quickly and easily assign roles to user accounts using PowerShell for Microsoft 365.</span></span>

>[!Note]
><span data-ttu-id="84d6f-106">[Découvrez comment attribuer des rôles à des comptes d’utilisateur](https://docs.microsoft.com/microsoft-365/admin/add-users/assign-admin-roles) avec le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="84d6f-106">[Learn how to assign roles to user accounts](https://docs.microsoft.com/microsoft-365/admin/add-users/assign-admin-roles) with the Microsoft 365 admin center.</span></span> <span data-ttu-id="84d6f-107">Pour obtenir la liste des ressources supplémentaires, consultez la rubrique [gérer les utilisateurs et les groupes](https://docs.microsoft.com/microsoft-365/admin/add-users/).</span><span class="sxs-lookup"><span data-stu-id="84d6f-107">For a list of additional resources, see [Manage users and groups](https://docs.microsoft.com/microsoft-365/admin/add-users/).</span></span>
>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="84d6f-108">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="84d6f-108">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="84d6f-109">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module) à l’aide d’un compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="84d6f-109">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module) using a global administrator account.</span></span>
  
<span data-ttu-id="84d6f-p102">Ensuite, déterminez le nom de connexion du compte d’utilisateur que vous souhaitez ajouter à un rôle (exemple : fredsm@contoso.com). On l’appelle aussi nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="84d6f-p102">Next, determine the sign-in name of the user account that you want to add to a role (example: fredsm@contoso.com). This is also known as the user principal name (UPN).</span></span>

<span data-ttu-id="84d6f-112">Ensuite, déterminez le nom du rôle.</span><span class="sxs-lookup"><span data-stu-id="84d6f-112">Next, determine the name of the role.</span></span> <span data-ttu-id="84d6f-113">Utilisez cette[liste d’autorisations des rôles d’administrateur dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="84d6f-113">Use this [list of administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span></span>

>[!Note]
><span data-ttu-id="84d6f-114">Soyez attentif aux notes dans cet article.</span><span class="sxs-lookup"><span data-stu-id="84d6f-114">Pay attention to the notes in this article.</span></span> <span data-ttu-id="84d6f-115">Certains noms de rôle sont différents pour Azure AD PowerShell.</span><span class="sxs-lookup"><span data-stu-id="84d6f-115">Some role names are different for Azure AD PowerShell.</span></span> <span data-ttu-id="84d6f-116">Par exemple, le rôle « Administrateur de SharePoint » dans le Centre d’administration Microsoft 365 est nommé « Administrateur du Service SharePoint » pour Azure AD PowerShell.</span><span class="sxs-lookup"><span data-stu-id="84d6f-116">For example, the "SharePoint Administrator" role in the Microsoft 365 admin center is named "SharePoint Service Administrator" for Azure AD PowerShell.</span></span>
>

<span data-ttu-id="84d6f-117">Ensuite, renseignez les noms de connexion et de rôle, et exécutez ces commandes.</span><span class="sxs-lookup"><span data-stu-id="84d6f-117">Next, fill in the sign-in and role names and run these commands.</span></span>
  
```powershell
$userName="<sign-in name of the account>"
$roleName="<role name>"
$role = Get-AzureADDirectoryRole | Where {$_.displayName -eq $roleName}
if ($role -eq $null) {
$roleTemplate = Get-AzureADDirectoryRoleTemplate | Where {$_.displayName -eq $roleName}
Enable-AzureADDirectoryRole -RoleTemplateId $roleTemplate.ObjectId
$role = Get-AzureADDirectoryRole | Where {$_.displayName -eq $roleName}
}
Add-AzureADDirectoryRoleMember -ObjectId $role.ObjectId -RefObjectId (Get-AzureADUser | Where {$_.UserPrincipalName -eq $userName}).ObjectID
```

<span data-ttu-id="84d6f-118">Voici un exemple d’un jeu de commandes terminé qui affecte le rôle d’administrateur de service SharePoint au compte belindan@contoso.com :</span><span class="sxs-lookup"><span data-stu-id="84d6f-118">Here is an example of a completed command set that assigns the SharePoint Service Administrator role to the belindan@contoso.com account:</span></span>
  
```powershell
$userName="belindan@contoso.com"
$roleName="SharePoint Service Administrator"
$role = Get-AzureADDirectoryRole | Where {$_.displayName -eq $roleName}
if ($role -eq $null) {
$roleTemplate = Get-AzureADDirectoryRoleTemplate | Where {$_.displayName -eq $roleName}
Enable-AzureADDirectoryRole -RoleTemplateId $roleTemplate.ObjectId
$role = Get-AzureADDirectoryRole | Where {$_.displayName -eq $roleName}
}
Add-AzureADDirectoryRoleMember -ObjectId $role.ObjectId -RefObjectId (Get-AzureADUser | Where {$_.UserPrincipalName -eq $userName}).ObjectID
```

<span data-ttu-id="84d6f-119">Pour afficher la liste des noms d’utilisateur pour un rôle spécifique, utilisez ces commandes.</span><span class="sxs-lookup"><span data-stu-id="84d6f-119">To display the list of user names for a specific role, use these commands.</span></span>

```powershell
$roleName="<role name>"
Get-AzureADDirectoryRole | Where { $_.DisplayName -eq $roleName } | Get-AzureADDirectoryRoleMember | Ft DisplayName
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="84d6f-120">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="84d6f-120">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="84d6f-121">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell) à l’aide d’un compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="84d6f-121">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell) using a global administrator account.</span></span>
  
### <a name="for-a-single-role-change"></a><span data-ttu-id="84d6f-122">Pour une seule modification de rôle</span><span class="sxs-lookup"><span data-stu-id="84d6f-122">For a single role change</span></span>

<span data-ttu-id="84d6f-123">Le moyen le plus courant de compte d’utilisateur spécifique est son nom d’affichage ou son nom de messagerie, également appelé nom de connexion ou nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="84d6f-123">The most common ways of specific user account is with its display name or its email name, also known its sign-in name or user principal name (UPN).</span></span>

#### <a name="display-names-of-user-accounts"></a><span data-ttu-id="84d6f-124">Noms d’affichage des comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="84d6f-124">Display names of user accounts</span></span>

<span data-ttu-id="84d6f-125">Si vous utilisez les noms d’affichage des comptes d’utilisateur, déterminez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="84d6f-125">If you are used to working with the display names of user accounts, determine the following:</span></span>
  
- <span data-ttu-id="84d6f-126">Le compte d’utilisateur que vous souhaitez configurer.</span><span class="sxs-lookup"><span data-stu-id="84d6f-126">The user account that you want to configure.</span></span>
    
    <span data-ttu-id="84d6f-p105">Pour spécifier le compte d'utilisateur, vous devez déterminer son nom d'affichage. Pour obtenir une liste de comptes, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="84d6f-p105">To specify the user account, you must determine its Display Name. To get a complete list accounts, use this command:</span></span>
    
  ```powershell
  Get-MsolUser -All | Sort DisplayName | Select DisplayName | More
  ```

    <span data-ttu-id="84d6f-p106">Cette commande répertorie le nom d'affichage de vos comptes d'utilisateur, triés par nom d'affichage, un écran à la fois. Vous pouvez filtrer la liste pour réduire l'ensemble à l'aide de la cmdlet **Where**. Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="84d6f-p106">This command lists the Display Name of your user accounts, sorted by the Display Name, one screen at a time. You can filter the list to a smaller set by using the **Where** cmdlet. Here is an example:</span></span>

   >[!Note]
   ><span data-ttu-id="84d6f-132">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="84d6f-132">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="84d6f-133">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="84d6f-133">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
   >
    
  ```powershell
  Get-MsolUser -All | Where DisplayName -like "John*" | Sort DisplayName | Select DisplayName | More
  ```

    <span data-ttu-id="84d6f-134">Cette commande répertorie uniquement les comptes d’utilisateur dont le nom d’affichage commence par « John ».</span><span class="sxs-lookup"><span data-stu-id="84d6f-134">This command lists only the user accounts for which the Display Name starts with "John".</span></span>
    
- <span data-ttu-id="84d6f-135">Le rôle que vous souhaitez attribuer.</span><span class="sxs-lookup"><span data-stu-id="84d6f-135">The role you want to assign.</span></span>
    
    <span data-ttu-id="84d6f-136">Pour afficher la liste des rôles disponibles que vous pouvez attribuer aux comptes d’utilisateur, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="84d6f-136">To display the list of available roles that you can assign to user accounts, use this command:</span></span>
    
  ```powershell
  Get-MsolRole | Sort Name | Select Name,Description
  ```

<span data-ttu-id="84d6f-137">Une fois que vous avez déterminé le nom d’affichage du compte et le nom du rôle, utilisez ces commandes pour attribuer le rôle au compte :</span><span class="sxs-lookup"><span data-stu-id="84d6f-137">Once you have determined the Display Name of the account and the Name of the role, use these commands to assign the role to the account:</span></span>
  
```powershell
$dispName="<The Display Name of the account>"
$roleName="<The role name you want to assign to the account>"
Add-MsolRoleMember -RoleMemberEmailAddress (Get-MsolUser -All | Where DisplayName -eq $dispName).UserPrincipalName -RoleName $roleName
```

<span data-ttu-id="84d6f-138">Copiez les commandes et collez-les dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="84d6f-138">Copy the commands and paste them into Notepad.</span></span> <span data-ttu-id="84d6f-139">Pour les variables **$dispName** et **$roleName** , remplacez le texte de description par leurs valeurs, supprimez les \< and > caractères et laissez les guillemets.</span><span class="sxs-lookup"><span data-stu-id="84d6f-139">For the **$dispName** and **$roleName** variables, replace the description text with their values, remove the \< and > characters, and leave the quotes.</span></span> <span data-ttu-id="84d6f-140">Copiez les lignes modifiées et collez-les dans la fenêtre du Module Windows Azure Active Directory pour Windows PowerShell pour les exécuter.</span><span class="sxs-lookup"><span data-stu-id="84d6f-140">Copy the modified lines and paste them into your Windows Azure Active Directory Module for Windows PowerShell window to run them.</span></span> <span data-ttu-id="84d6f-141">Vous pouvez également utiliser l'environnement d'écriture de scripts intégré de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="84d6f-141">Alternately, you can use the Windows PowerShell Integrated Script Environment (ISE).</span></span>
  
<span data-ttu-id="84d6f-142">Voici un exemple d’un jeu de commandes terminées :</span><span class="sxs-lookup"><span data-stu-id="84d6f-142">Here is an example of a completed command set:</span></span>
  
```powershell
$dispName="Scott Wallace"
$roleName="SharePoint Service Administrator"
Add-MsolRoleMember -RoleMemberEmailAddress (Get-MsolUser -All | Where DisplayName -eq $dispName).UserPrincipalName -RoleName $roleName
```

#### <a name="sign-in-names-of-user-accounts"></a><span data-ttu-id="84d6f-143">Noms de connexion des comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="84d6f-143">Sign-in names of user accounts</span></span>

<span data-ttu-id="84d6f-144">Si vous utilisez le nom de connexion ou l’UPN des comptes d’utilisateur, déterminez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="84d6f-144">If you are used to working with the sign-in names or UPNs of user accounts, determine the following:</span></span>
  
- <span data-ttu-id="84d6f-145">Nom d’utilisateur principal du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84d6f-145">The user account's UPN.</span></span>
    
    <span data-ttu-id="84d6f-146">Si vous ne connaissez pas déjà le nom d’utilisateur principal, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="84d6f-146">If you don't already know the UPN, use this command:</span></span>
    
  ```powershell
  Get-MsolUser -All | Sort UserPrincipalName | Select UserPrincipalName | More
  ```

    <span data-ttu-id="84d6f-147">Cette commande répertorie l’UPN de vos comptes d’utilisateur, triés par nom UPN, un écran à la fois.</span><span class="sxs-lookup"><span data-stu-id="84d6f-147">This command lists the UPN of your user accounts, sorted by the UPN, one screen at a time.</span></span> <span data-ttu-id="84d6f-148">Vous pouvez filtrer la liste pour réduire l'ensemble à l'aide de la cmdlet **Where**.</span><span class="sxs-lookup"><span data-stu-id="84d6f-148">You can filter the list to a smaller set by using the **Where** cmdlet.</span></span> <span data-ttu-id="84d6f-149">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="84d6f-149">Here is an example:</span></span>
    
  ```powershell
  Get-MsolUser -All | Where DisplayName -like "John*" | Sort UserPrincipalName | Select UserPrincipalName | More
  ```

    <span data-ttu-id="84d6f-150">Cette commande répertorie uniquement les comptes d’utilisateur dont le nom d’affichage commence par « John ».</span><span class="sxs-lookup"><span data-stu-id="84d6f-150">This command lists only the user accounts for which the Display Name starts with "John".</span></span>
    
- <span data-ttu-id="84d6f-151">Le rôle que vous souhaitez attribuer.</span><span class="sxs-lookup"><span data-stu-id="84d6f-151">The role you want to assign.</span></span>
    
    <span data-ttu-id="84d6f-152">Pour afficher la liste des rôles disponibles que vous pouvez attribuer aux comptes d’utilisateur, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="84d6f-152">To display the list of available roles that you can assign to user accounts, use this command:</span></span>
    
  ```powershell
  Get-MsolRole | Sort Name | Select Name,Description
  ```

<span data-ttu-id="84d6f-153">Une fois que vous avez le nom UPN du compte et le nom du rôle, utilisez ces commandes pour attribuer le rôle au compte :</span><span class="sxs-lookup"><span data-stu-id="84d6f-153">Once you have the UPN of the account and the name of the role, use these commands to assign the role to the account:</span></span>
  
```powershell
$upnName="<The UPN of the account>"
$roleName="<The role name you want to assign to the account>"
Add-MsolRoleMember -RoleMemberEmailAddress $upnName -RoleName $roleName
```

<span data-ttu-id="84d6f-154">Copiez les commandes et collez-les dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="84d6f-154">Copy the commands and paste them into Notepad.</span></span> <span data-ttu-id="84d6f-155">Pour les variables **$upnName** et **$roleName** , remplacez le texte de description par leurs valeurs, supprimez les \< and > caractères et laissez les guillemets.</span><span class="sxs-lookup"><span data-stu-id="84d6f-155">For the **$upnName** and **$roleName** variables, replace the description text with their values, remove the \< and > characters, and leave the quotes.</span></span> <span data-ttu-id="84d6f-156">Copiez les lignes modifiées et collez-les dans la fenêtre du Module Windows Azure Active Directory pour Windows PowerShell pour les exécuter.</span><span class="sxs-lookup"><span data-stu-id="84d6f-156">Copy the modified lines and paste them into your Windows Azure Active Directory Module for Windows PowerShell window to run them.</span></span> <span data-ttu-id="84d6f-157">Vous pouvez également utiliser Windows PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="84d6f-157">Alternately, you can use the Windows PowerShell ISE.</span></span>
  
<span data-ttu-id="84d6f-158">Voici un exemple d’un jeu de commandes terminées :</span><span class="sxs-lookup"><span data-stu-id="84d6f-158">Here is an example of a completed command set:</span></span>
  
```powershell
$upnName="scottw@contoso.com"
$roleName="SharePoint Service Administrator"
Add-MsolRoleMember -RoleMemberEmailAddress $upnName -RoleName $roleName
```

### <a name="multiple-role-changes"></a><span data-ttu-id="84d6f-159">Plusieurs modifications de rôle</span><span class="sxs-lookup"><span data-stu-id="84d6f-159">Multiple role changes</span></span>

<span data-ttu-id="84d6f-160">Pour les différentes modifications de rôle, déterminez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="84d6f-160">For multiple role changes, determine the following:</span></span>
  
- <span data-ttu-id="84d6f-161">Les comptes d’utilisateur que vous souhaitez configurer.</span><span class="sxs-lookup"><span data-stu-id="84d6f-161">Which user accounts that you want to configure.</span></span> <span data-ttu-id="84d6f-162">Vous pouvez utiliser les méthodes de la section précédente pour collecter le jeu de noms complets ou UPN.</span><span class="sxs-lookup"><span data-stu-id="84d6f-162">You can use the methods in the previous section to gather the set of display names or UPNs.</span></span>
    
- <span data-ttu-id="84d6f-163">Les rôles que vous souhaitez attribuer à chaque compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84d6f-163">Which roles you want to assign to each user account.</span></span>
    
    <span data-ttu-id="84d6f-164">Pour afficher la liste des rôles disponibles que vous pouvez attribuer aux comptes d’utilisateur, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="84d6f-164">To display the list of available roles that you can assign to user accounts, use this command:</span></span>
    
  ```powershell
  Get-MsolRole | Sort Name | Select Name,Description
  ```

<span data-ttu-id="84d6f-165">Ensuite, créez un fichier texte au format CSV (valeurs séparées par des virgules) contenant le nom complet ou les champs UPN et nom de rôle.</span><span class="sxs-lookup"><span data-stu-id="84d6f-165">Next, create a comma-separated value (CSV) text file that has the display name or UPN and role name fields.</span></span> <span data-ttu-id="84d6f-166">Vous pouvez le faire facilement avec Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="84d6f-166">You can do this easily with Microsoft Excel.</span></span>

<span data-ttu-id="84d6f-167">Voici un exemple de nom d’affichage :</span><span class="sxs-lookup"><span data-stu-id="84d6f-167">Here is an example for display names:</span></span>
  
```powershell
DisplayName,RoleName
"Belinda Newman","Billing Administrator"
"Scott Wallace","SharePoint Service Administrator"
```

<span data-ttu-id="84d6f-168">Ensuite, remplissez l’emplacement du fichier CSV et exécutez les commandes qui en résultent à l’invite de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="84d6f-168">Next, fill in the location of the CSV file and run the resulting commands at the PowerShell command prompt.</span></span>
  
```powershell
$fileName="<path and file name of the input CSV file that has the role changes, example: C:\admin\RoleUpdates.CSV>"
$roleChanges=Import-Csv $fileName | ForEach {Add-MsolRoleMember -RoleMemberEmailAddress (Get-MsolUser | Where DisplayName -eq $_.DisplayName).UserPrincipalName -RoleName $_.RoleName }

```

<span data-ttu-id="84d6f-169">Voici un exemple pour l’UPN :</span><span class="sxs-lookup"><span data-stu-id="84d6f-169">Here is an example for UPNs:</span></span>
  
```powershell
UserPrincipalName,RoleName
"belindan@contoso.com","Billing Administrator"
"scottw@contoso.com","SharePoint Service Administrator"
```

<span data-ttu-id="84d6f-170">Ensuite, remplissez l’emplacement du fichier CSV et exécutez les commandes qui en résultent à l’invite de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="84d6f-170">Next, fill in the location of the CSV file and run the resulting commands at the PowerShell command prompt.</span></span>
  
```powershell
$fileName="<path and file name of the input CSV file that has the role changes, example: C:\admin\RoleUpdates.CSV>"
$roleChanges=Import-Csv $fileName | ForEach { Add-MsolRoleMember -RoleMemberEmailAddress $_.UserPrincipalName -RoleName $_.RoleName }

```

## <a name="see-also"></a><span data-ttu-id="84d6f-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84d6f-171">See also</span></span>

- [<span data-ttu-id="84d6f-172">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="84d6f-172">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
- [<span data-ttu-id="84d6f-173">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="84d6f-173">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
- [<span data-ttu-id="84d6f-174">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="84d6f-174">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
