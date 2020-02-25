---
title: Définir le mot de passe d'un utilisateur de façon à ce qu'il n'expire jamais
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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: f493e3af-e1d8-4668-9211-230c245a0466
description: Découvrez comment définir certains mots de passe utilisateur individuels pour ne jamais expirer à l’aide de Windows PowerShell.
ms.openlocfilehash: 1c44f5c4d5966d70b5fed0b1b99e69b2938c6ddd
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239344"
---
# <a name="set-an-individual-users-password-to-never-expire"></a><span data-ttu-id="3a993-103">Définir le mot de passe d'un utilisateur de façon à ce qu'il n'expire jamais</span><span class="sxs-lookup"><span data-stu-id="3a993-103">Set an individual user's password to never expire</span></span>

## <a name="set-the-password-expiration-policy-for-your-organization"></a><span data-ttu-id="3a993-104">Définir la stratégie d’expiration des mots de passe pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="3a993-104">Set the password expiration policy for your organization</span></span>

1. <span data-ttu-id="3a993-105">Dans le centre d’administration, accédez à la page **paramètres** \> de <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">sécurité & de confidentialité</a> .</span><span class="sxs-lookup"><span data-stu-id="3a993-105">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Security & privacy</a> page.</span></span>
2. <span data-ttu-id="3a993-106">En regard de **stratégie de mot de passe** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="3a993-106">Next to **Password policy** select **Edit**.</span></span> 
3. <span data-ttu-id="3a993-107">Si les mots de passe sont configurés pour ne jamais expirer, **désactivez**le bouton bascule.</span><span class="sxs-lookup"><span data-stu-id="3a993-107">If passwords are set to never expire, set the toggle to **Off**.</span></span> <span data-ttu-id="3a993-108">Vous aurez la possibilité de spécifier le nombre de jours avant l’expiration des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="3a993-108">You'll get the option to specify the number of days until passwords expire.</span></span> 


## <a name="set-the-password-expiration-policy-for-individual-users"></a><span data-ttu-id="3a993-109">Définir la stratégie d’expiration de mot de passe pour les utilisateurs individuels</span><span class="sxs-lookup"><span data-stu-id="3a993-109">Set the password expiration policy for individual users</span></span> 

<span data-ttu-id="3a993-110">Un administrateur général pour un service de Cloud Microsoft peut utiliser le module Microsoft Azure AD pour Windows PowerShell pour définir des mots de passe qui n’expirent pas pour des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3a993-110">A global admin for a Microsoft cloud service can use the Microsoft Azure AD Module for Windows PowerShell to set passwords not to expire for specific users.</span></span> <span data-ttu-id="3a993-111">Vous pouvez également utiliser les applets de commande Windows PowerShell pour supprimer la configuration sans expiration ou pour voir quels mots de passe utilisateur sont configurés pour ne jamais expirer.</span><span class="sxs-lookup"><span data-stu-id="3a993-111">You can also use Windows PowerShell cmdlets to remove the never-expires configuration or to see which user passwords are set to never expire.</span></span> 

<span data-ttu-id="3a993-112">Ce guide s’applique aux autres fournisseurs, comme Intune et Office 365, qui reposent également sur Azure AD pour les services d’identité et d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="3a993-112">This guide applies to other providers, such as Intune and Office 365, which also rely on Azure AD for identity and directory services.</span></span> <span data-ttu-id="3a993-113">L’expiration du mot de passe est la seule partie de la stratégie qui peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="3a993-113">Password expiration is the only part of the policy that can be changed.</span></span>

> [!NOTE]
> <span data-ttu-id="3a993-114">Seuls les mots de passe des comptes d’utilisateur qui ne sont pas synchronisés via la synchronisation d’annuaires peuvent être configurés pour ne pas expirer.</span><span class="sxs-lookup"><span data-stu-id="3a993-114">Only passwords for user accounts that are not synchronized through directory synchronization can be configured to not expire.</span></span> <span data-ttu-id="3a993-115">Pour plus d’informations sur la synchronisation d’annuaires, consultez la rubrique [Connect ad with Azure ad](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect).</span><span class="sxs-lookup"><span data-stu-id="3a993-115">For more information about directory synchronization, see [Connect AD with Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect).</span></span>


### <a name="how-to-check-the-expiration-policy-for-a-password"></a><span data-ttu-id="3a993-116">Procédure de vérification de la stratégie d’expiration pour un mot de passe</span><span class="sxs-lookup"><span data-stu-id="3a993-116">How to check the expiration policy for a password</span></span>

* <span data-ttu-id="3a993-117">Exécutez l’une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a993-117">Run one of the following commands:</span></span>

   * <span data-ttu-id="3a993-118">Pour savoir si le mot de passe d’un utilisateur est configuré pour ne jamais expirer, exécutez l’applet de commande suivante à l’aide du nom d’utilisateur principal (par exemple, *user@contoso.onmicrosoft.com*) ou du nom d’utilisateur de l’utilisateur que vous souhaitez vérifier :</span><span class="sxs-lookup"><span data-stu-id="3a993-118">To see if a single user’s password is set to never expire, run the following cmdlet by using the UPN (for example, *user@contoso.onmicrosoft.com*) or the user ID of the user you want to check:</span></span>
```
Get-AzureADUser -ObjectId <user id or UPN> | Select-Object UserprincipalName,@{
    N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
 }
```  
<span data-ttu-id="3a993-119">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3a993-119">Example:</span></span>
```
Get-AzureADUser -ObjectId userUPN@contoso.com | Select-Object UserprincipalName,@{
    N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
 }
```  

 * <span data-ttu-id="3a993-120">Pour afficher le paramètre le **mot de passe n’expire jamais** pour tous les utilisateurs, exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3a993-120">To see the **Password never expires** setting for all users, run the following cmdlet:</span></span> 
 
```
Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
    N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
 }
```  

* <span data-ttu-id="3a993-121">Pour obtenir un rapport de tous les utilisateurs avec empêcher dans le code HTML sur le Bureau de l’utilisateur actuel portant le nom **ReportPasswordNeverExpires. html**</span><span class="sxs-lookup"><span data-stu-id="3a993-121">To get a report of all the users with PasswordNeverExpires in Html on the desktop of the current user with name  **ReportPasswordNeverExpires.html**</span></span>


```
Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
    N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
} | ConvertTo-Html | Out-File $env:userprofile\Desktop\ReportPasswordNeverExpires.html
```  

* <span data-ttu-id="3a993-122">Pour obtenir un rapport de tous les utilisateurs avec empêcher dans CSV sur le Bureau de l’utilisateur actuel portant le nom **ReportPasswordNeverExpires. csv**</span><span class="sxs-lookup"><span data-stu-id="3a993-122">To get a report of all the users with PasswordNeverExpires in CSV on the desktop of the current user with name **ReportPasswordNeverExpires.csv**</span></span>


```
Get-AzureADUser -All $true | Select-Object UserprincipalName,@{
    N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}
} | ConvertTo-Csv -NoTypeInformation | Out-File $env:userprofile\Desktop\ReportPasswordNeverExpires.csv
```  


### <a name="set-a-password-to-expire"></a><span data-ttu-id="3a993-123">Définir un mot de passe pour qu’il expire</span><span class="sxs-lookup"><span data-stu-id="3a993-123">Set a password to expire</span></span>

<span data-ttu-id="3a993-124">Exécutez l’une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a993-124">Run one of the following commands:</span></span>

   * <span data-ttu-id="3a993-125">Pour définir le mot de passe d’un utilisateur de sorte que le mot de passe expire, exécutez l’applet de commande suivante à l’aide de l’UPN ou de l’ID d’utilisateur de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3a993-125">To set the password of one user so that the password expires, run the following cmdlet by using the UPN or the user ID of the user:</span></span>

```
 Set-AzureADUser -ObjectId <user ID> -PasswordPolicies None

```
   * <span data-ttu-id="3a993-126">Pour définir les mots de passe de tous les utilisateurs de l’organisation afin qu’ils arrivent à expiration, utilisez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3a993-126">To set the passwords of all users in the organization so that they expire, use the following cmdlet:</span></span>

```
 Get-AzureADUser -All $true | Set-AzureADUser -PasswordPolicies None

```
### <a name="set-a-password-to-never-expire"></a><span data-ttu-id="3a993-127">Définir un mot de passe pour qu’il n’expire jamais</span><span class="sxs-lookup"><span data-stu-id="3a993-127">Set a password to never expire</span></span>

<span data-ttu-id="3a993-128">Exécutez l’une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a993-128">Run one of the following commands:</span></span>

   * <span data-ttu-id="3a993-129">Pour définir le mot de passe d’un utilisateur de sorte qu’il n’expire jamais, exécutez l’applet de commande suivante à l’aide de l’UPN ou de l’ID d’utilisateur de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3a993-129">To set the password of one user to never expire, run the following cmdlet by using the UPN or the user ID of the user:</span></span> 

```
Set-AzureADUser -ObjectId <user ID> -PasswordPolicies DisablePasswordExpiration

```
   * <span data-ttu-id="3a993-130">Pour définir les mots de passe de tous les utilisateurs d’une organisation pour qu’ils n’expirent jamais, exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3a993-130">To set the passwords of all the users in an organization to never expire, run the following cmdlet:</span></span> 

```
Get-AzureADUser -All $true | Set-AzureADUser -PasswordPolicies DisablePasswordExpiration

```
   > [!WARNING]
   > <span data-ttu-id="3a993-131">Mots de passe définis `-PasswordPolicies DisablePasswordExpiration` sur Age en fonction de `pwdLastSet` l’attribut.</span><span class="sxs-lookup"><span data-stu-id="3a993-131">Passwords set to `-PasswordPolicies DisablePasswordExpiration` still age based on the `pwdLastSet` attribute.</span></span> <span data-ttu-id="3a993-132">Si vous configurez les mots de passe des utilisateurs de sorte qu’ils n’expirent jamais, les mots de passe expirent dans 90 jours.</span><span class="sxs-lookup"><span data-stu-id="3a993-132">If you set the user passwords to never expire and then 90+ days go by, the passwords expire.</span></span> <span data-ttu-id="3a993-133">En fonction de `pwdLastSet` l’attribut, si vous modifiez l’expiration `-PasswordPolicies None`, tous les mots de passe dont `pwdLastSet` le délai d’expiration est antérieur à 90 jours doivent être modifiés par l’utilisateur lors de sa prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="3a993-133">Based on the `pwdLastSet` attribute, if you change the expiration to `-PasswordPolicies None`, all passwords that have a `pwdLastSet` older than 90 days require the user to change them the next time they sign in.</span></span> <span data-ttu-id="3a993-134">Cette modification peut affecter un grand nombre d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3a993-134">This change can affect a large number of users.</span></span> 
