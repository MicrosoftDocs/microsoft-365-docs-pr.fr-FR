---
title: Définir le mot de passe d’un utilisateur de façon à ce qu’il n’expire jamais
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: f493e3af-e1d8-4668-9211-230c245a0466
description: Découvrez comment définir certains mots de passe utilisateur individuels pour ne jamais expirer à l’aide de Windows PowerShell.
ms.openlocfilehash: f85eb2d3aaf5b19779ea8f293e2cbdc28c1535aa
ms.sourcegitcommit: 5c16d270c7651c2080a5043d273d979a6fcc75c6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "46804207"
---
# <a name="set-an-individual-users-password-to-never-expire"></a><span data-ttu-id="d5176-103">Définir le mot de passe d’un utilisateur de façon à ce qu’il n’expire jamais</span><span class="sxs-lookup"><span data-stu-id="d5176-103">Set an individual user's password to never expire</span></span>

## <a name="set-the-password-expiration-policy-for-your-organization"></a><span data-ttu-id="d5176-104">Définir la stratégie d’expiration des mots de passe pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="d5176-104">Set the password expiration policy for your organization</span></span>

1. <span data-ttu-id="d5176-105">Dans le centre d’administration, accédez à **Settings** la \> page <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">paramètres</a> des paramètres.</span><span class="sxs-lookup"><span data-stu-id="d5176-105">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Settings</a> page.</span></span>
2. <span data-ttu-id="d5176-106">En haut de la page Paramètres, sélectionnez **sécurité & confidentialité**.</span><span class="sxs-lookup"><span data-stu-id="d5176-106">At the top of the Settings page select **Security & Privacy**.</span></span>
3. <span data-ttu-id="d5176-107">Sélectionnez **Stratégie d’expiration du mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="d5176-107">Select **Password expiration policy**.</span></span> 
4. <span data-ttu-id="d5176-108">Si les mots de passe sont configurés pour ne jamais expirer, activez la case à cocher en regard de **définir les mots de passe d’utilisateur pour qu’ils expirent après un certain nombre de jours**.</span><span class="sxs-lookup"><span data-stu-id="d5176-108">If passwords are set to never expire, click the check box next to **Set user passwords to expire after a number of days**.</span></span> <span data-ttu-id="d5176-109">Vous aurez la possibilité de spécifier le nombre de jours avant l’expiration des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="d5176-109">You'll get the option to specify the number of days until passwords expire.</span></span>

## <a name="set-the-password-expiration-policy-for-individual-users"></a><span data-ttu-id="d5176-110">Définir la stratégie d’expiration de mot de passe pour les utilisateurs individuels</span><span class="sxs-lookup"><span data-stu-id="d5176-110">Set the password expiration policy for individual users</span></span>

<span data-ttu-id="d5176-111">Un administrateur général pour un service de Cloud Microsoft peut utiliser [Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0) pour définir des mots de passe qui n’expirent pas pour des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d5176-111">A global admin for a Microsoft cloud service can use the [Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0) to set passwords not to expire for specific users.</span></span> <span data-ttu-id="d5176-112">Vous pouvez également utiliser des applets de commande [AzureAD](https://docs.microsoft.com/powershell/module/Azuread) pour supprimer la configuration qui n’expire jamais ou pour afficher les mots de passe d’utilisateur qui sont configurés pour ne jamais expirer.</span><span class="sxs-lookup"><span data-stu-id="d5176-112">You can also use [AzureAD](https://docs.microsoft.com/powershell/module/Azuread) cmdlets to remove the never-expires configuration or to see which user passwords are set to never expire.</span></span>

<span data-ttu-id="d5176-113">Ce guide s’applique aux autres fournisseurs, comme Intune et Microsoft 365, qui reposent également sur Azure AD pour les services d’identité et d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d5176-113">This guide applies to other providers, such as Intune and Microsoft 365, which also rely on Azure AD for identity and directory services.</span></span> <span data-ttu-id="d5176-114">L’expiration du mot de passe est la seule partie de la stratégie qui peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="d5176-114">Password expiration is the only part of the policy that can be changed.</span></span>

<span data-ttu-id="d5176-115">Pour plus d’informations sur Azure AD PowerShell pour Graph, reportez-vous à la rubrique [Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="d5176-115">For more information about Azure AD PowerShell for Graph, see [Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0).</span></span>

> [!NOTE]
> <span data-ttu-id="d5176-116">Seuls les mots de passe des comptes d’utilisateur qui ne sont pas synchronisés via la synchronisation d’annuaires peuvent être configurés pour ne pas expirer.</span><span class="sxs-lookup"><span data-stu-id="d5176-116">Only passwords for user accounts that are not synchronized through directory synchronization can be configured to not expire.</span></span> <span data-ttu-id="d5176-117">Pour plus d’informations sur la synchronisation d’annuaires, consultez la rubrique [Connect ad with Azure ad](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect).</span><span class="sxs-lookup"><span data-stu-id="d5176-117">For more information about directory synchronization, see [Connect AD with Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect).</span></span>

### <a name="how-to-check-the-expiration-policy-for-a-password"></a><span data-ttu-id="d5176-118">Procédure de vérification de la stratégie d’expiration pour un mot de passe</span><span class="sxs-lookup"><span data-stu-id="d5176-118">How to check the expiration policy for a password</span></span>

<span data-ttu-id="d5176-119">Pour plus d’informations sur la commande Get-AzureADUser dans le module AzureAD, voir l’article de référence [Get-AzureADUser](https://docs.microsoft.com/powershell/module/Azuread/Get-AzureADUser?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="d5176-119">For more information about the Get-AzureADUser command in the AzureAD module, see the reference article [Get-AzureADUser](https://docs.microsoft.com/powershell/module/Azuread/Get-AzureADUser?view=azureadps-2.0).</span></span>

<span data-ttu-id="d5176-120">Exécutez une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5176-120">Run one of the following commands:</span></span>

- <span data-ttu-id="d5176-121">Pour savoir si le mot de passe d’un utilisateur est configuré pour ne jamais expirer, exécutez l’applet de commande suivante à l’aide du nom d’utilisateur principal (par exemple, *user@contoso.onmicrosoft.com*) ou du nom d’utilisateur de l’utilisateur que vous souhaitez vérifier :</span><span class="sxs-lookup"><span data-stu-id="d5176-121">To see if a single user's password is set to never expire, run the following cmdlet by using the UPN (for example, *user@contoso.onmicrosoft.com*) or the user ID of the user you want to check:</span></span>

    ```powershell
    Get-AzureADUser -ObjectId <user id or UPN> | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    }
    ```

    <span data-ttu-id="d5176-122">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d5176-122">Example:</span></span>

    ```powershell
    Get-AzureADUser -ObjectId userUPN@contoso.com | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    }
    ```  

- <span data-ttu-id="d5176-123">Pour afficher le paramètre le **mot de passe n’expire jamais** pour tous les utilisateurs, exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d5176-123">To see the **Password never expires** setting for all users, run the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
     }
    ```

- <span data-ttu-id="d5176-124">Pour obtenir un rapport de tous les utilisateurs avec empêcher dans le code HTML sur le Bureau de l’utilisateur actuel portant le nom  **ReportPasswordNeverExpires.html**</span><span class="sxs-lookup"><span data-stu-id="d5176-124">To get a report of all the users with PasswordNeverExpires in Html on the desktop of the current user with name  **ReportPasswordNeverExpires.html**</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    } | ConvertTo-Html | Out-File $env:userprofile\Desktop\ReportPasswordNeverExpires.html
    ```  

- <span data-ttu-id="d5176-125">Pour obtenir un rapport de tous les utilisateurs avec empêcher dans CSV sur le Bureau de l’utilisateur actuel avec le nom **ReportPasswordNeverExpires.csv**</span><span class="sxs-lookup"><span data-stu-id="d5176-125">To get a report of all the users with PasswordNeverExpires in CSV on the desktop of the current user with name **ReportPasswordNeverExpires.csv**</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    } | ConvertTo-Csv -NoTypeInformation | Out-File $env:userprofile\Desktop\ReportPasswordNeverExpires.csv
    ```

### <a name="set-a-password-to-expire"></a><span data-ttu-id="d5176-126">Définir un mot de passe pour qu’il expire</span><span class="sxs-lookup"><span data-stu-id="d5176-126">Set a password to expire</span></span>

<span data-ttu-id="d5176-127">Exécutez une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5176-127">Run one of the following commands:</span></span>

- <span data-ttu-id="d5176-128">Pour définir le mot de passe d’un utilisateur de sorte que le mot de passe expire, exécutez l’applet de commande suivante à l’aide de l’UPN ou de l’ID d’utilisateur de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="d5176-128">To set the password of one user so that the password expires, run the following cmdlet by using the UPN or the user ID of the user:</span></span>

    ```powershell
    Set-AzureADUser -ObjectId <user ID> -PasswordPolicies None
    ```

- <span data-ttu-id="d5176-129">Pour définir les mots de passe de tous les utilisateurs de l’organisation afin qu’ils arrivent à expiration, utilisez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d5176-129">To set the passwords of all users in the organization so that they expire, use the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Set-AzureADUser -PasswordPolicies None
    ```

### <a name="set-a-password-to-never-expire"></a><span data-ttu-id="d5176-130">Définir un mot de passe pour qu’il n’expire jamais</span><span class="sxs-lookup"><span data-stu-id="d5176-130">Set a password to never expire</span></span>

<span data-ttu-id="d5176-131">Exécutez une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5176-131">Run one of the following commands:</span></span>

- <span data-ttu-id="d5176-132">Pour définir le mot de passe d’un utilisateur de sorte qu’il n’expire jamais, exécutez l’applet de commande suivante à l’aide de l’UPN ou de l’ID d’utilisateur de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="d5176-132">To set the password of one user to never expire, run the following cmdlet by using the UPN or the user ID of the user:</span></span>

    ```powershell
    Set-AzureADUser -ObjectId <user ID> -PasswordPolicies DisablePasswordExpiration
    ```

- <span data-ttu-id="d5176-133">Pour définir les mots de passe de tous les utilisateurs d’une organisation pour qu’ils n’expirent jamais, exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d5176-133">To set the passwords of all the users in an organization to never expire, run the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Set-AzureADUser -PasswordPolicies DisablePasswordExpiration
    ```

> [!WARNING]
> <span data-ttu-id="d5176-134">Les comptes d’utilisateur configurés avec le `-PasswordPolicies DisablePasswordExpiration` paramètre vieillissent en fonction de l' `pwdLastSet` attribut de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5176-134">User accounts configured with the `-PasswordPolicies DisablePasswordExpiration` parameter still age based on the `pwdLastSet` user account attribute.</span></span> <span data-ttu-id="d5176-135">Par exemple, si vous définissez des mots de passe d’utilisateur qui n’expirent jamais, puis 90 jours ou plus, les mots de passe expirent toujours.</span><span class="sxs-lookup"><span data-stu-id="d5176-135">For example, if you set user passwords to never expire and then 90 or more days go by, the passwords still expire.</span></span> <span data-ttu-id="d5176-136">En fonction de l' `pwdLastSet` attribut du compte d’utilisateur, pour les comptes d’utilisateur configurés avec le `-PasswordPolicies None` paramètre, tous les mots de passe dont la `pwdLastSet` date est antérieure à 90 jours imposent à l’utilisateur de les modifier la prochaine fois qu’ils se connectent. Cette modification peut affecter un grand nombre d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d5176-136">Based on the `pwdLastSet` user account attribute, for user accounts configured with the `-PasswordPolicies None` parameter, all passwords that have a `pwdLastSet` older than 90 days require the user to change them the next time they sign in.This change can affect a large number of users.</span></span>
