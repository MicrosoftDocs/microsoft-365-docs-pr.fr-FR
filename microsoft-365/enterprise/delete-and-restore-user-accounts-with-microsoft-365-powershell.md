---
title: Supprimer des comptes d’utilisateur Microsoft 365 avec PowerShell
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
- O365ITProTrain
- seo-marvel-apr2020
ms.assetid: 209c9868-448c-49bc-baae-11e28b923a39
description: Dans cet article, Découvrez comment utiliser des modules différents dans PowerShell pour supprimer des comptes d’utilisateur Microsoft 365.
ms.openlocfilehash: 0c13b57c13fb3d01d648438a5d6973fea8b9db67
ms.sourcegitcommit: c1ee4ed3c5826872b57339e1e1aa33b4d2209711
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2020
ms.locfileid: "48235441"
---
# <a name="delete-microsoft-365-user-accounts-with-powershell"></a><span data-ttu-id="cfae2-103">Supprimer des comptes d’utilisateur Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="cfae2-103">Delete Microsoft 365 user accounts with PowerShell</span></span>

<span data-ttu-id="cfae2-104">Vous pouvez utiliser PowerShell pour Microsoft 365 pour supprimer et restaurer un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cfae2-104">You can use PowerShell for Microsoft 365 to delete and restore a user account.</span></span>

>[!Note]
><span data-ttu-id="cfae2-105">[Découvrez comment restaurer un compte d’utilisateur](https://docs.microsoft.com/microsoft-365/admin/add-users/restore-user) à l’aide du centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cfae2-105">[Learn how to restore a user account](https://docs.microsoft.com/microsoft-365/admin/add-users/restore-user) with the Microsoft 365 admin center.</span></span> <span data-ttu-id="cfae2-106">Pour obtenir la liste des ressources supplémentaires, consultez la rubrique [gérer les utilisateurs et les groupes](https://docs.microsoft.com/microsoft-365/admin/add-users/).</span><span class="sxs-lookup"><span data-stu-id="cfae2-106">For a list of additional resources, see [Manage users and groups](https://docs.microsoft.com/microsoft-365/admin/add-users/).</span></span>
>   
   
## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="cfae2-107">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="cfae2-107">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="cfae2-108">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="cfae2-108">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>

<span data-ttu-id="cfae2-109">Après vous être connecté, utilisez la syntaxe suivante pour supprimer un compte d’utilisateur individuel :</span><span class="sxs-lookup"><span data-stu-id="cfae2-109">After you have connected, use the following syntax to remove an individual user account:</span></span>
  
```powershell
Remove-AzureADUser -ObjectID <sign-in name>
```

<span data-ttu-id="cfae2-110">Cet exemple supprime le compte d’utilisateur fabricec@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="cfae2-110">This example removes the user account fabricec@litwareinc.com.</span></span>
  
```powershell
Remove-AzureADUser -ObjectID fabricec@litwareinc.com
```

> [!NOTE]
> <span data-ttu-id="cfae2-111">Le paramètre **-ObjectID** de la cmdlet **Remove-AzureADUser** accepte le nom de connexion du compte, également appelé nom d’utilisateur principal, ou l’ID d’objet du compte.</span><span class="sxs-lookup"><span data-stu-id="cfae2-111">The **-ObjectID** parameter in the **Remove-AzureADUser** cmdlet accepts either the account's sign-in name, also known as the User Principal Name, or the account's object ID.</span></span>
  
<span data-ttu-id="cfae2-112">Pour afficher le nom du compte à partir du nom de l’utilisateur, utilisez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cfae2-112">To display the account name based on the user's name, use the following commands:</span></span>
  
```powershell
$userName="<User name>"
Write-Host (Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="cfae2-113">Cet exemple affiche le nom du compte de l’utilisateur nommé Caleb Sills.</span><span class="sxs-lookup"><span data-stu-id="cfae2-113">This example displays the account name for the user named Caleb Sills.</span></span>
  
```powershell
$userName="Caleb Sills"
Write-Host (Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

<span data-ttu-id="cfae2-114">Pour supprimer un compte à partir du nom de l’utilisateur, utilisez les commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="cfae2-114">To remove an account based on the user's display name, use the following commands:</span></span>
  
```powershell
$userName="<display name>"
Remove-AzureADUser -ObjectID (Get-AzureADUser | where {$_.DisplayName -eq $userName}).UserPrincipalName
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="cfae2-115">Utilisez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cfae2-115">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="cfae2-p102">Lorsque vous utilisez le Module Microsoft Azure Active Directory pour Windows PowerShell afin de supprimer un compte d’utilisateur, le compte n’est pas supprimé définitivement. En effet, vous pouvez le restaurer dans les 30 jours.</span><span class="sxs-lookup"><span data-stu-id="cfae2-p102">When you delete a user account with the Microsoft Azure Active Directory Module for Windows PowerShell, the account isn't permanently deleted. You can restore the deleted user account within 30 days.</span></span>

<span data-ttu-id="cfae2-118">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="cfae2-118">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

<span data-ttu-id="cfae2-119">Pour supprimer un compte d’utilisateur, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="cfae2-119">To delete a user account, use the following syntax:</span></span>
  
```powershell
Remove-MsolUser -UserPrincipalName <sign-in name>
```

>[!Note]
><span data-ttu-id="cfae2-120">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="cfae2-120">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="cfae2-121">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cfae2-121">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

<span data-ttu-id="cfae2-122">Cet exemple supprime le compte d’utilisateur BelindaN@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="cfae2-122">This example deletes the user account BelindaN@litwareinc.com.</span></span>
  
```powershell
Remove-MsolUser -UserPrincipalName belindan@litwareinc.com
```

<span data-ttu-id="cfae2-123">Pour restaurer un compte d’utilisateur supprimé pendant la période de grâce de 30 jours, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="cfae2-123">To restore a deleted user account within the 30-day grace period, use the following syntax:</span></span>
  
```powershell
Restore-MsolUser -UserPrincipalName <sign-in name>
```

<span data-ttu-id="cfae2-124">Cet exemple restaure le compte d’utilisateur supprimé BelindaN@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="cfae2-124">This example restores the deleted account BelindaN@litwareinc.com.</span></span>
  
```powershell
Restore-MsolUser -UserPrincipalName BelindaN@litwareinc.com
```

 <span data-ttu-id="cfae2-125">**Remarques :**</span><span class="sxs-lookup"><span data-stu-id="cfae2-125">**Notes:**</span></span>
  
- <span data-ttu-id="cfae2-126">Pour afficher la liste des utilisateurs supprimés dont la restauration est possible, exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="cfae2-126">To see the list of deleted users that can be restored, run the following command:</span></span>
    
  ```powershell
  Get-MsolUser -All -ReturnDeletedUsers
  ```

- <span data-ttu-id="cfae2-127">Si le nom d'utilisateur principal d'origine du compte d'utilisateur est utilisé par un autre compte, utilisez le paramètre_NewUserPrincipalName_ à la place de_UserPrincipalName_ pour spécifier un autre nom d'utilisateur principal lorsque vous restaurez le compte.</span><span class="sxs-lookup"><span data-stu-id="cfae2-127">If the user account's original user principal name is used by another account, use the _NewUserPrincipalName_ parameter instead of _UserPrincipalName_ to specify a different user principal name when you restore the user account.</span></span>


## <a name="see-also"></a><span data-ttu-id="cfae2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfae2-128">See also</span></span>

[<span data-ttu-id="cfae2-129">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="cfae2-129">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="cfae2-130">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="cfae2-130">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="cfae2-131">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cfae2-131">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
