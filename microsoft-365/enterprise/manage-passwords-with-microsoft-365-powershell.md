---
title: Gérer les mots de passe avec PowerShell
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
- PowerShell
- Ent_Office_Other
- O365ITProTrain
description: Découvrez comment utiliser PowerShell pour gérer les mots de passe.
ms.openlocfilehash: ac0a47edb4ccbed93c1a3b88df083d463784b4a4
ms.sourcegitcommit: fcc1b40732f28f075d95faffc1655473e262dd95
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2020
ms.locfileid: "49073197"
---
# <a name="manage-passwords-with-powershell"></a><span data-ttu-id="2e11f-103">Gérer les mots de passe avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="2e11f-103">Manage passwords with PowerShell</span></span>

<span data-ttu-id="2e11f-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="2e11f-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="2e11f-105">Vous pouvez utiliser PowerShell pour Microsoft 365 comme alternative au centre d’administration Microsoft 365 pour gérer les mots de passe dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2e11f-105">You can use PowerShell for Microsoft 365 as an alternative to the Microsoft 365 admin center to manage passwords in Microsoft 365.</span></span> 

<span data-ttu-id="2e11f-106">Lorsqu’un bloc de commande de cet article exige que vous spécifiez des valeurs variables, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="2e11f-106">When a command block in this article requires that you specify variable values, use these steps.</span></span>

1. <span data-ttu-id="2e11f-107">Copiez le bloc de commandes dans le presse-papiers et collez-le dans le bloc-notes ou dans l’environnement de script intégré PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="2e11f-107">Copy the command block to the clipboard and paste it into Notepad or the PowerShell Integrated Script Environment (ISE).</span></span>
2. <span data-ttu-id="2e11f-108">Renseignez les valeurs des variables et supprimez les caractères « < » et « > ».</span><span class="sxs-lookup"><span data-stu-id="2e11f-108">Fill in the variable values and remove the "<" and ">" characters.</span></span>
3. <span data-ttu-id="2e11f-109">Exécutez les commandes dans la fenêtre PowerShell ou PowerShell ISE.</span><span class="sxs-lookup"><span data-stu-id="2e11f-109">Run the commands in the PowerShell window or the PowerShell ISE.</span></span>

## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="2e11f-110">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="2e11f-110">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="2e11f-111">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="2e11f-111">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>

### <a name="set-a-password"></a><span data-ttu-id="2e11f-112">Définir un mot de passe</span><span class="sxs-lookup"><span data-stu-id="2e11f-112">Set a password</span></span>

<span data-ttu-id="2e11f-113">Utilisez ces commandes pour spécifier un mot de passe pour un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2e11f-113">Use these commands to specify a password for a user account.</span></span>

```powershell
$userUPN="<user account sign in name, such as belindan@contoso.com>"
$newPassword="<new password>"
$secPassword = ConvertTo-SecureString $newPassword -AsPlainText -Force
Set-AzureADUserPassword -ObjectId  $userUPN -Password $secPassword
```
### <a name="force-a-user-to-change-their-password"></a><span data-ttu-id="2e11f-114">Forcer un utilisateur à modifier son mot de passe</span><span class="sxs-lookup"><span data-stu-id="2e11f-114">Force a user to change their password</span></span>

<span data-ttu-id="2e11f-115">Utilisez ces commandes pour définir un mot de passe et obliger un utilisateur à modifier son nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2e11f-115">Use these commands to set a password and force a user to change their new password.</span></span>

```powershell
$userUPN="<user account sign in name, such as belindan@contoso.com>"
$newPassword="<new password>"
$secPassword = ConvertTo-SecureString $newPassword -AsPlainText -Force
Set-AzureADUserPassword -ObjectId  $userUPN -Password $secPassword -EnforceChangePasswordPolicy $true
```

<span data-ttu-id="2e11f-116">Utilisez ces commandes pour définir un mot de passe et obliger un utilisateur à modifier son nouveau mot de passe lors de sa prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="2e11f-116">Use these commands to set a password and force a user to change their new password the next time they sign in.</span></span>

```powershell
$userUPN="<user account sign in name, such as belindan@contoso.com>"
$newPassword="<new password>"
$secPassword = ConvertTo-SecureString $newPassword -AsPlainText -Force
Set-AzureADUserPassword -ObjectId  $userUPN -Password $secPassword -ForceChangePasswordNextLogin $true
```

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="2e11f-117">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e11f-117">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="2e11f-118">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="2e11f-118">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

### <a name="set-a-password"></a><span data-ttu-id="2e11f-119">Définir un mot de passe</span><span class="sxs-lookup"><span data-stu-id="2e11f-119">Set a password</span></span>

<span data-ttu-id="2e11f-120">Utilisez ces commandes pour spécifier un mot de passe pour un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2e11f-120">Use these commands to specify a password for a user account.</span></span>

```powershell
$userUPN="<user account sign in name>"
$newPassword="<new password>"
Set-MsolUserPassword -UserPrincipalName $userUPN -NewPassword $newPassword
```

### <a name="force-a-user-to-change-their-password"></a><span data-ttu-id="2e11f-121">Forcer un utilisateur à modifier son mot de passe</span><span class="sxs-lookup"><span data-stu-id="2e11f-121">Force a user to change their password</span></span>

<span data-ttu-id="2e11f-122">Utilisez ces commandes pour obliger un utilisateur à modifier son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2e11f-122">Use these commands to force a user to change their password.</span></span>

```powershell
$userUPN="<user account sign in name>"
Set-MsolUserPassword -UserPrincipalName $userUPN -ForceChangePassword $true
```

## <a name="see-also"></a><span data-ttu-id="2e11f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e11f-123">See also</span></span>

[<span data-ttu-id="2e11f-124">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="2e11f-124">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="2e11f-125">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="2e11f-125">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="2e11f-126">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2e11f-126">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)

