---
title: Définir le mot de passe d’un utilisateur de façon à ce qu’il n’expire jamais
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
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
description: Connectez-vous à votre compte Microsoft 365 administrateur pour définir certains mots de passe utilisateur individuels de sorte qu’ils n’expirent jamais à l’aide Windows PowerShell.
ms.openlocfilehash: 12c717d8d625b0135f185b1af131db00e9762c73
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635557"
---
# <a name="set-an-individual-users-password-to-never-expire"></a><span data-ttu-id="c354b-103">Définir le mot de passe d’un utilisateur de façon à ce qu’il n’expire jamais</span><span class="sxs-lookup"><span data-stu-id="c354b-103">Set an individual user's password to never expire</span></span>

<span data-ttu-id="c354b-104">Cet article explique comment définir un mot de passe pour qu’un utilisateur individuel n’expire pas.</span><span class="sxs-lookup"><span data-stu-id="c354b-104">This article explains how to set a password for an individual user to not expire.</span></span> <span data-ttu-id="c354b-105">Vous devez effectuer ces étapes à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c354b-105">You have to complete these steps using PowerShell.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="c354b-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c354b-106">Before you begin</span></span>

<span data-ttu-id="c354b-107">Cet article s’adresse aux personnes responsables de la stratégie d’expiration des mots de passe au sein d’une entreprise, d’une école ou d’une association.</span><span class="sxs-lookup"><span data-stu-id="c354b-107">This article is for people who set password expiration policy for a business, school, or nonprofit.</span></span> <span data-ttu-id="c354b-108">Pour effectuer ces étapes, vous devez vous connecter avec votre compte d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c354b-108">To complete these steps, you need to sign in with your Microsoft 365 admin account.</span></span> <span data-ttu-id="c354b-109">[Qu’est-ce qu’un compte d’administrateur ?](../../business-video/admin-center-overview.md)</span><span class="sxs-lookup"><span data-stu-id="c354b-109">[What's an admin account?](../../business-video/admin-center-overview.md).</span></span> 

<span data-ttu-id="c354b-110">Vous devez être administrateur général ou administrateur de [mot de](about-admin-roles.md) passe pour effectuer ces étapes.</span><span class="sxs-lookup"><span data-stu-id="c354b-110">You must be an [global admin or password administrator](about-admin-roles.md) to perform these steps.</span></span>

<span data-ttu-id="c354b-111">Un administrateur global d’un service cloud Microsoft peut utiliser la Azure Active Directory [PowerShell pour Graph](/powershell/azure/active-directory/install-adv2?view=azureadps-2.0) pour définir les mots de passe de ne pas expirer pour des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c354b-111">A global admin for a Microsoft cloud service can use the [Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2?view=azureadps-2.0) to set passwords not to expire for specific users.</span></span> <span data-ttu-id="c354b-112">Vous pouvez également utiliser des cmdlets [AzureAD](/powershell/module/Azuread) pour supprimer la configuration qui n’expire jamais ou pour voir les mots de passe utilisateur qui ne doivent jamais expirer.</span><span class="sxs-lookup"><span data-stu-id="c354b-112">You can also use [AzureAD](/powershell/module/Azuread) cmdlets to remove the never-expires configuration or to see which user passwords are set to never expire.</span></span>

<span data-ttu-id="c354b-113">Ce guide s’applique à d’autres fournisseurs, tels que Intune et Microsoft 365, qui s’appuient également sur Azure AD pour les services d’identité et d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c354b-113">This guide applies to other providers, such as Intune and Microsoft 365, which also rely on Azure AD for identity and directory services.</span></span> <span data-ttu-id="c354b-114">L’expiration du mot de passe est la seule partie de la stratégie qui peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="c354b-114">Password expiration is the only part of the policy that can be changed.</span></span>

> [!NOTE]
> <span data-ttu-id="c354b-115">Seuls les mots de passe des comptes d’utilisateur qui ne sont pas synchronisés par le biais de la synchronisation d’annuaires peuvent être configurés pour ne pas expirer.</span><span class="sxs-lookup"><span data-stu-id="c354b-115">Only passwords for user accounts that are not synchronized through directory synchronization can be configured to not expire.</span></span> <span data-ttu-id="c354b-116">Pour plus d’informations sur la synchronisation d’annuaires, [voir Connecter AD avec Azure AD](/azure/active-directory/connect/active-directory-aadconnect).</span><span class="sxs-lookup"><span data-stu-id="c354b-116">For more information about directory synchronization, see [Connect AD with Azure AD](/azure/active-directory/connect/active-directory-aadconnect).</span></span>

## <a name="how-to-check-the-expiration-policy-for-a-password"></a><span data-ttu-id="c354b-117">Comment vérifier la stratégie d’expiration pour un mot de passe</span><span class="sxs-lookup"><span data-stu-id="c354b-117">How to check the expiration policy for a password</span></span>

<span data-ttu-id="c354b-118">Pour plus d’informations sur Get-AzureADUser commande dans le module AzureAD, consultez l’article de référence [Get-AzureADUser](/powershell/module/Azuread/Get-AzureADUser?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="c354b-118">For more information about the Get-AzureADUser command in the AzureAD module, see the reference article [Get-AzureADUser](/powershell/module/Azuread/Get-AzureADUser?view=azureadps-2.0).</span></span>

<span data-ttu-id="c354b-119">Exécutez une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c354b-119">Run one of the following commands:</span></span>

- <span data-ttu-id="c354b-120">Pour voir si le mot de passe d’un seul utilisateur est définie pour ne jamais expirer, exécutez l’cmdlet suivante à l’aide de l’UPN (par exemple, *user@contoso.onmicrosoft.com*) ou de l’ID utilisateur de l’utilisateur que vous souhaitez vérifier :</span><span class="sxs-lookup"><span data-stu-id="c354b-120">To see if a single user's password is set to never expire, run the following cmdlet by using the UPN (for example, *user@contoso.onmicrosoft.com*) or the user ID of the user you want to check:</span></span>

    ```powershell
    Get-AzureADUser -ObjectId <user id or UPN> | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    }
    ```

    <span data-ttu-id="c354b-121">Exemple :</span><span class="sxs-lookup"><span data-stu-id="c354b-121">Example:</span></span>

    ```powershell
    Get-AzureADUser -ObjectId userUPN@contoso.com | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    }
    ```  

- <span data-ttu-id="c354b-122">Pour voir le paramètre Mot de passe n’expire jamais pour tous les **utilisateurs,** exécutez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="c354b-122">To see the **Password never expires** setting for all users, run the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
     }
    ```

- <span data-ttu-id="c354b-123">Pour obtenir un rapport de tous les utilisateurs avec PasswordNeverExpires en Html sur le bureau de l’utilisateur actuel avec le  **nomReportPasswordNeverExpires.html**</span><span class="sxs-lookup"><span data-stu-id="c354b-123">To get a report of all the users with PasswordNeverExpires in Html on the desktop of the current user with name  **ReportPasswordNeverExpires.html**</span></span>

    ```powershell
    Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
        N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
    } | ConvertTo-Html | Out-File $env:userprofile\Desktop\ReportPasswordNeverExpires.html
    ```  

- <span data-ttu-id="c354b-124">Pour obtenir un rapport de tous les utilisateurs avec PasswordNeverExpires dans CSV sur le bureau de l’utilisateur actuel avec le **nomReportPasswordNeverExpires.csv**</span><span class="sxs-lookup"><span data-stu-id="c354b-124">To get a report of all the users with PasswordNeverExpires in CSV on the desktop of the current user with name **ReportPasswordNeverExpires.csv**</span></span>

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

- <span data-ttu-id="c354b-125">Pour définir les mots de passe de tous les utilisateurs d’une organisation de sorte qu’ils n’expirent jamais, exécutez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="c354b-125">To set the passwords of all the users in an organization to never expire, run the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Set-AzureADUser -PasswordPolicies DisablePasswordExpiration
    ```

> [!WARNING]
> <span data-ttu-id="c354b-126">Les comptes d’utilisateur configurés avec le `-PasswordPolicies DisablePasswordExpiration` paramètre sont toujours basés sur l’attribut. `pwdLastSet`</span><span class="sxs-lookup"><span data-stu-id="c354b-126">User accounts configured with the `-PasswordPolicies DisablePasswordExpiration` parameter still age based on the `pwdLastSet` attribute.</span></span> <span data-ttu-id="c354b-127">En fonction de l’attribut, si vous modifiez l’expiration en , tous les mots de passe qui ont un `pwdLastSet` pwdLastSet plus de 90 jours nécessitent que l’utilisateur les modifie la prochaine fois qu’ils se `-PasswordPolicies None` connectent.</span><span class="sxs-lookup"><span data-stu-id="c354b-127">Based on the `pwdLastSet` attribute, if you change the expiration to `-PasswordPolicies None`, all passwords that have a pwdLastSet older than 90 days require the user to change them the next time they sign in.</span></span> <span data-ttu-id="c354b-128">Cette modification peut affecter un grand nombre d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c354b-128">This change can affect a large number of users.</span></span>

### <a name="set-a-password-to-expire"></a><span data-ttu-id="c354b-129">Définir un mot de passe pour expirer</span><span class="sxs-lookup"><span data-stu-id="c354b-129">Set a password to expire</span></span>

<span data-ttu-id="c354b-130">Exécutez une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c354b-130">Run one of the following commands:</span></span>

- <span data-ttu-id="c354b-131">Pour définir le mot de passe d’un utilisateur afin qu’il expire, exécutez l’cmdlet suivante à l’aide de l’UPN ou de l’ID utilisateur de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="c354b-131">To set the password of one user so that the password expires, run the following cmdlet by using the UPN or the user ID of the user:</span></span>

    ```powershell
    Set-AzureADUser -ObjectId <user ID> -PasswordPolicies None
    ```

- <span data-ttu-id="c354b-132">Pour définir les mots de passe de tous les utilisateurs de l’organisation afin qu’ils expirent, utilisez la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="c354b-132">To set the passwords of all users in the organization so that they expire, use the following cmdlet:</span></span>

    ```powershell
    Get-AzureADUser -All $true | Set-AzureADUser -PasswordPolicies None
    ```

## <a name="related-content"></a><span data-ttu-id="c354b-133">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="c354b-133">Related content</span></span>

<span data-ttu-id="c354b-134">[Laisser les utilisateurs réinitialiser leur mot de passe](../add-users/let-users-reset-passwords.md) (article)</span><span class="sxs-lookup"><span data-stu-id="c354b-134">[Let users reset their own passwords](../add-users/let-users-reset-passwords.md) (article)</span></span>\
<span data-ttu-id="c354b-135">[Réinitialiser les mots](../add-users/reset-passwords.md) de passe (article)</span><span class="sxs-lookup"><span data-stu-id="c354b-135">[Reset passwords](../add-users/reset-passwords.md) (article)</span></span>\
<span data-ttu-id="c354b-136">[Définir la stratégie d’expiration de mot de passe pour votre organisation](../manage/set-password-expiration-policy.md) (article)</span><span class="sxs-lookup"><span data-stu-id="c354b-136">[Set the password expiration policy for your organization](../manage/set-password-expiration-policy.md) (article)</span></span>