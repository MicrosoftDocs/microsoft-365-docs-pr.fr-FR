---
title: Définir le mot de passe d’un utilisateur de façon à ce qu’il n’expire jamais
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
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
ms.openlocfilehash: e778ad8a020a6767934d51f8bc227bfc39b13a9b
ms.sourcegitcommit: 3165329d1fb5a7fd866ff287bea3b6354ea2be18
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2020
ms.locfileid: "48580915"
---
# <a name="set-an-individual-users-password-to-never-expire"></a><span data-ttu-id="8c3fe-103">Définir le mot de passe d’un utilisateur de façon à ce qu’il n’expire jamais</span><span class="sxs-lookup"><span data-stu-id="8c3fe-103">Set an individual user's password to never expire</span></span>

<span data-ttu-id="8c3fe-104">Cet article explique comment définir un mot de passe pour qu’un utilisateur individuel n’expire pas.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-104">This article explains how to set a password for an individual user to not expire.</span></span> <span data-ttu-id="8c3fe-105">Vous devez effectuer ces étapes à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-105">You have to complete these steps using PowerShell.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="8c3fe-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8c3fe-106">Before you begin</span></span>

<span data-ttu-id="8c3fe-107">Cet article s’adresse aux personnes responsables de la stratégie d’expiration des mots de passe au sein d’une entreprise, d’une école ou d’une association.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-107">This article is for people who set password expiration policy for a business, school, or nonprofit.</span></span> <span data-ttu-id="8c3fe-108">Pour effectuer ces étapes, vous devez vous connecter avec votre compte d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-108">To complete these steps, you need to sign in with your Microsoft 365 admin account.</span></span> <span data-ttu-id="8c3fe-109">[Qu’est-ce qu’un compte d’administrateur ?](../admin-overview/admin-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8c3fe-109">[What's an admin account?](../admin-overview/admin-overview.md).</span></span> 

<span data-ttu-id="8c3fe-110">Pour effectuer ces étapes, vous devez être [administrateur général ou administrateur de mots de passe](about-admin-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="8c3fe-110">You must be an [global admin or password administrator](about-admin-roles.md) to perform these steps.</span></span>

<span data-ttu-id="8c3fe-111">Un administrateur général pour un service de Cloud Microsoft peut utiliser [Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0) pour définir des mots de passe qui n’expirent pas pour des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-111">A global admin for a Microsoft cloud service can use the [Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0) to set passwords not to expire for specific users.</span></span> <span data-ttu-id="8c3fe-112">Vous pouvez également utiliser des applets de commande [AzureAD](https://docs.microsoft.com/powershell/module/Azuread) pour supprimer la configuration qui n’expire jamais ou pour afficher les mots de passe d’utilisateur qui sont configurés pour ne jamais expirer.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-112">You can also use [AzureAD](https://docs.microsoft.com/powershell/module/Azuread) cmdlets to remove the never-expires configuration or to see which user passwords are set to never expire.</span></span>

<span data-ttu-id="8c3fe-113">Ce guide s’applique aux autres fournisseurs, comme Intune et Microsoft 365, qui reposent également sur Azure AD pour les services d’identité et d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-113">This guide applies to other providers, such as Intune and Microsoft 365, which also rely on Azure AD for identity and directory services.</span></span> <span data-ttu-id="8c3fe-114">L’expiration du mot de passe est la seule partie de la stratégie qui peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-114">Password expiration is the only part of the policy that can be changed.</span></span>

> [!NOTE]
> <span data-ttu-id="8c3fe-115">Seuls les mots de passe des comptes d’utilisateur qui ne sont pas synchronisés via la synchronisation d’annuaires peuvent être configurés pour ne pas expirer.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-115">Only passwords for user accounts that are not synchronized through directory synchronization can be configured to not expire.</span></span> <span data-ttu-id="8c3fe-116">Pour plus d’informations sur la synchronisation d’annuaires, consultez la rubrique [Connect ad with Azure ad](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect).</span><span class="sxs-lookup"><span data-stu-id="8c3fe-116">For more information about directory synchronization, see [Connect AD with Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect).</span></span>

## <a name="how-to-check-the-expiration-policy-for-a-password"></a><span data-ttu-id="8c3fe-117">Procédure de vérification de la stratégie d’expiration pour un mot de passe</span><span class="sxs-lookup"><span data-stu-id="8c3fe-117">How to check the expiration policy for a password</span></span>

<span data-ttu-id="8c3fe-118">Pour plus d’informations sur la commande Get-AzureADUser dans le module AzureAD, voir l’article de référence [Get-AzureADUser](https://docs.microsoft.com/powershell/module/Azuread/Get-AzureADUser?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="8c3fe-118">For more information about the Get-AzureADUser command in the AzureAD module, see the reference article [Get-AzureADUser](https://docs.microsoft.com/powershell/module/Azuread/Get-AzureADUser?view=azureadps-2.0).</span></span>

<span data-ttu-id="8c3fe-119">Exécutez une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c3fe-119">Run one of the following commands:</span></span>

- <span data-ttu-id="8c3fe-120">Pour savoir si le mot de passe d’un utilisateur est configuré pour ne jamais expirer, exécutez l’applet de commande suivante à l’aide du nom d’utilisateur principal (par exemple, *user@contoso.onmicrosoft.com*) ou du nom d’utilisateur de l’utilisateur que vous souhaitez vérifier :</span><span class="sxs-lookup"><span data-stu-id="8c3fe-120">To see if a single user's password is set to never expire, run the following cmdlet by using the UPN (for example, *user@contoso.onmicrosoft.com*) or the user ID of the user you want to check:</span></span>

    ```powershell
    Get-AzureADUser -ObjectId <user id or UPN> | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    }
    ```

    <span data-ttu-id="8c3fe-121">Exemple :</span><span class="sxs-lookup"><span data-stu-id="8c3fe-121">Example:</span></span>

    ```powershell
    Get-AzureADUser -ObjectId userUPN@contoso.com | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    }
    ```  

- <span data-ttu-id="8c3fe-122">Pour afficher le paramètre le **mot de passe n’expire jamais** pour tous les utilisateurs, exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8c3fe-122">To see the **Password never expires** setting for all users, run the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
     }
    ```

- <span data-ttu-id="8c3fe-123">Pour obtenir un rapport de tous les utilisateurs avec empêcher dans le code HTML sur le Bureau de l’utilisateur actuel portant le nom  **ReportPasswordNeverExpires.html**</span><span class="sxs-lookup"><span data-stu-id="8c3fe-123">To get a report of all the users with PasswordNeverExpires in Html on the desktop of the current user with name  **ReportPasswordNeverExpires.html**</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    } | ConvertTo-Html | Out-File $env:userprofile\Desktop\ReportPasswordNeverExpires.html
    ```  

- <span data-ttu-id="8c3fe-124">Pour obtenir un rapport de tous les utilisateurs avec empêcher dans CSV sur le Bureau de l’utilisateur actuel avec le nom **ReportPasswordNeverExpires.csv**</span><span class="sxs-lookup"><span data-stu-id="8c3fe-124">To get a report of all the users with PasswordNeverExpires in CSV on the desktop of the current user with name **ReportPasswordNeverExpires.csv**</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    } | ConvertTo-Csv -NoTypeInformation | Out-File $env:userprofile\Desktop\ReportPasswordNeverExpires.csv

## Set a password to never expire

Run one of the following commands:

- To set the password of one user to never expire, run the following cmdlet by using the UPN or the user ID of the user:

    ```powershell
    Set-AzureADUser -ObjectId <user ID> -PasswordPolicies DisablePasswordExpiration
    ```

- <span data-ttu-id="8c3fe-125">Pour définir les mots de passe de tous les utilisateurs d’une organisation pour qu’ils n’expirent jamais, exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8c3fe-125">To set the passwords of all the users in an organization to never expire, run the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Set-AzureADUser -PasswordPolicies DisablePasswordExpiration
    ```

### <a name="set-a-password-to-expire"></a><span data-ttu-id="8c3fe-126">Définir un mot de passe pour qu’il expire</span><span class="sxs-lookup"><span data-stu-id="8c3fe-126">Set a password to expire</span></span>

<span data-ttu-id="8c3fe-127">Exécutez une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c3fe-127">Run one of the following commands:</span></span>

- <span data-ttu-id="8c3fe-128">Pour définir le mot de passe d’un utilisateur de sorte que le mot de passe expire, exécutez l’applet de commande suivante à l’aide de l’UPN ou de l’ID d’utilisateur de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="8c3fe-128">To set the password of one user so that the password expires, run the following cmdlet by using the UPN or the user ID of the user:</span></span>

    ```powershell
    Set-AzureADUser -ObjectId <user ID> -PasswordPolicies None
    ```

- <span data-ttu-id="8c3fe-129">Pour définir les mots de passe de tous les utilisateurs de l’organisation afin qu’ils arrivent à expiration, utilisez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8c3fe-129">To set the passwords of all users in the organization so that they expire, use the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Set-AzureADUser -PasswordPolicies None
    ```

> [!WARNING]
> <span data-ttu-id="8c3fe-130">Les comptes d’utilisateur configurés avec le `-PasswordPolicies DisablePasswordExpiration` paramètre vieillissent en fonction de l' `pwdLastSet` attribut de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-130">User accounts configured with the `-PasswordPolicies DisablePasswordExpiration` parameter still age based on the `pwdLastSet` user account attribute.</span></span> <span data-ttu-id="8c3fe-131">Par exemple, si vous définissez des mots de passe d’utilisateur qui n’expirent jamais, puis 90 jours ou plus, les mots de passe expirent toujours.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-131">For example, if you set user passwords to never expire and then 90 or more days go by, the passwords still expire.</span></span> <span data-ttu-id="8c3fe-132">En fonction de l' `pwdLastSet` attribut du compte d’utilisateur, pour les comptes d’utilisateur configurés avec le `-PasswordPolicies None` paramètre, tous les mots de passe dont la `pwdLastSet` date est antérieure à 90 jours imposent à l’utilisateur de les modifier la prochaine fois qu’ils se connectent. Cette modification peut affecter un grand nombre d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8c3fe-132">Based on the `pwdLastSet` user account attribute, for user accounts configured with the `-PasswordPolicies None` parameter, all passwords that have a `pwdLastSet` older than 90 days require the user to change them the next time they sign in.This change can affect a large number of users.</span></span>

## <a name="related-content"></a><span data-ttu-id="8c3fe-133">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="8c3fe-133">Related content</span></span>

[<span data-ttu-id="8c3fe-134">Autoriser les utilisateurs à réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="8c3fe-134">Let users reset their own passwords</span></span>](../add-users/let-users-reset-passwords.md)

[<span data-ttu-id="8c3fe-135">Réinitialiser les mots de passe</span><span class="sxs-lookup"><span data-stu-id="8c3fe-135">Reset passwords</span></span>](../add-users/reset-passwords.md)