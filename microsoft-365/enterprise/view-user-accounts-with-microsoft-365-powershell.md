---
title: Afficher les comptes d’utilisateur Microsoft 365 avec PowerShell
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
- LIL_Placement
- PowerShell
- Ent_Office_Other
- seo-marvel-apr2020
ms.assetid: bb12f49d-a85d-4f3b-ada2-5c4e33977b10
description: Découvrez comment afficher, répertorier ou afficher vos comptes d’utilisateur Microsoft 365 de différentes manières avec PowerShell.
ms.openlocfilehash: 312e9fb983c4d1f4de8bc74586c88f1e669eb90a
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48754071"
---
# <a name="view-microsoft-365-user-accounts-with-powershell"></a><span data-ttu-id="38507-103">Afficher les comptes d’utilisateur Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="38507-103">View Microsoft 365 user accounts with PowerShell</span></span>

<span data-ttu-id="38507-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="38507-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="38507-105">Vous pouvez utiliser le centre d’administration Microsoft 365 pour afficher les comptes de votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="38507-105">You can use the Microsoft 365 admin center to view the accounts for your Microsoft 365 tenant.</span></span> <span data-ttu-id="38507-106">PowerShell pour Microsoft 365 active cela, mais fournit également des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="38507-106">PowerShell for Microsoft 365 enables this but also provides additional functionality.</span></span>
  
## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="38507-107">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="38507-107">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="38507-108">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="38507-108">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
### <a name="view-all-accounts"></a><span data-ttu-id="38507-109">Afficher tous les comptes</span><span class="sxs-lookup"><span data-stu-id="38507-109">View all accounts</span></span>

<span data-ttu-id="38507-110">Pour afficher la liste complète des comptes d’utilisateurs, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="38507-110">To display the full list of user accounts, run this command:</span></span>
  
```powershell
Get-AzureADUser
```

<span data-ttu-id="38507-111">Vous devriez obtenir des informations semblables à celles-ci :</span><span class="sxs-lookup"><span data-stu-id="38507-111">You should get information similar to this:</span></span>
  
```powershell
ObjectId                             DisplayName                                           UserPrincipalName
--------                             -----------                                           -----------------
032fc1fc-b5a2-46f1-8635-3d7dcb52c48d Adele Vance                                           AdeleV@litwareinc.OnMicr...
bd1e6af1-41e7-4f77-a2ac-5b209950135c Global Administrator                                  admin@litwareinc.onmicro...
ec37a4d6-232e-4eb7-82a5-1613490642a5 Alex Wilber                                           AlexW@litwareinc.OnMicro...
be4bdddd-c790-424c-9f96-a0cf609b7815 Allan Deyoung                                         AllanD@litwareinc.OnMicr...
598ab87b-76f0-4bf9-9538-bd46b10f4438 Christie Cline                                        ChristieC@litwareinc.OnM...
40722671-e520-4a5f-97d4-0bc9e9b2dc0f Debra Berger                                          DebraB@litwareinc.OnMicr...
```

### <a name="view-a-specific-account"></a><span data-ttu-id="38507-112">Afficher un compte spécifique</span><span class="sxs-lookup"><span data-stu-id="38507-112">View a specific account</span></span>

<span data-ttu-id="38507-113">Pour afficher un compte d’utilisateur spécifique, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="38507-113">To display a specific user account, run the following command.</span></span> <span data-ttu-id="38507-114">Renseignez le nom de compte de connexion du compte d’utilisateur, également appelé nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="38507-114">Fill in the sign-in account name of the user account, which is also known as the user principal name (UPN).</span></span> <span data-ttu-id="38507-115">Supprimez les caractères « < » et « > ».</span><span class="sxs-lookup"><span data-stu-id="38507-115">Remove the "<" and ">" characters.</span></span>
  
```powershell
Get-AzureADUser -ObjectID <sign-in name of the user account>
```

<span data-ttu-id="38507-116">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="38507-116">Here's an example:</span></span>
  
```powershell
Get-AzureADUser -ObjectID BelindaN@litwareinc.onmicosoft.com
```

### <a name="view-additional-property-values-for-a-specific-account"></a><span data-ttu-id="38507-117">Afficher des valeurs de propriétés supplémentaires pour un compte spécifique</span><span class="sxs-lookup"><span data-stu-id="38507-117">View additional property values for a specific account</span></span>

<span data-ttu-id="38507-118">Par défaut, la cmdlet **Get-AzureADUser** affiche uniquement les propriétés *ObjectID*, *DisplayName*et *userPrincipalName* des comptes.</span><span class="sxs-lookup"><span data-stu-id="38507-118">By default, the **Get-AzureADUser** cmdlet only displays the *ObjectID*, *DisplayName*, and *UserPrincipalName* properties of accounts.</span></span>

<span data-ttu-id="38507-119">Pour être plus sélectif quant aux propriétés à afficher, utilisez l’applet de commande **Select** en combinaison avec la cmdlet **Get-AzureADUser** .</span><span class="sxs-lookup"><span data-stu-id="38507-119">To be more selective about the properties to display, use the **Select** cmdlet in combination with the **Get-AzureADUser** cmdlet.</span></span> <span data-ttu-id="38507-120">Pour combiner les deux cmdlets, utilisez le caractère « pipe » (« | »), qui indique à Azure Active Directory PowerShell pour Graph de prendre les résultats d’une commande et de l’envoyer à la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="38507-120">To combine the two cmdlets, use the "pipe" character ("|"), which tells Azure Active Directory PowerShell for Graph to take the results of one command and send it to the next command.</span></span> <span data-ttu-id="38507-121">Voici un exemple de commande qui affiche les *DisplayName*, *Department*et *UsageLocation* pour chaque compte d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="38507-121">Here's an example command that displays the *DisplayName*, *Department*, and *UsageLocation* for every user account:</span></span>
  
```powershell
Get-AzureADUser | Select DisplayName,Department,UsageLocation
```

<span data-ttu-id="38507-122">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="38507-122">This command instructs PowerShell to:</span></span>
  
1. <span data-ttu-id="38507-123">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-AzureADUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="38507-123">Get all the information on the user accounts (**Get-AzureADUser**) and send it to the next command (**|**).</span></span>
    
1.  <span data-ttu-id="38507-124">Afficher uniquement le nom du compte d’utilisateur, le service et l’emplacement d’utilisation (**Sélectionnez DisplayName, Department, UsageLocation**).</span><span class="sxs-lookup"><span data-stu-id="38507-124">Display only the user account name, department, and usage location (**Select DisplayName, Department, UsageLocation**).</span></span>
  
<span data-ttu-id="38507-125">Pour afficher toutes les propriétés d’un compte d’utilisateur spécifique, utilisez l’applet de commande **Select** et le caractère générique (\*).</span><span class="sxs-lookup"><span data-stu-id="38507-125">To see all the properties for a specific user account, use the **Select** cmdlet and the wildcard character (\*).</span></span> <span data-ttu-id="38507-126">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="38507-126">Here's an example:</span></span>
  
```powershell
Get-AzureADUser -ObjectID BelindaN@litwareinc.onmicosoft.com | Select *
```

<span data-ttu-id="38507-127">En guise d’exemple supplémentaire, exécutez la commande suivante pour vérifier l’état activé d’un compte d’utilisateur spécifique :</span><span class="sxs-lookup"><span data-stu-id="38507-127">As another example, run the following command to check the enabled status of a specific user account:</span></span>
  
```powershell
Get-AzureADUser -ObjectID <sign-in name of the user account> | Select DisplayName,UserPrincipalName,AccountEnabled
```

### <a name="view-account-synchronization-status"></a><span data-ttu-id="38507-128">Afficher l’état de la synchronisation des comptes</span><span class="sxs-lookup"><span data-stu-id="38507-128">View account synchronization status</span></span>

<span data-ttu-id="38507-129">Les comptes d’utilisateur ont deux sources :</span><span class="sxs-lookup"><span data-stu-id="38507-129">User accounts have two sources:</span></span> 

- <span data-ttu-id="38507-130">Windows Server Active Directory (AD), qui sont des comptes synchronisés à partir d’AD sur site vers le Cloud.</span><span class="sxs-lookup"><span data-stu-id="38507-130">Windows Server Active Directory (AD), which are accounts that sync from on-premises AD to the cloud.</span></span>

- <span data-ttu-id="38507-131">Les comptes AD Azure Active Directory (Azure AD), qui sont créés directement dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="38507-131">Azure Active Directory (Azure AD) AD accounts, which are created directly in the cloud.</span></span>


<span data-ttu-id="38507-132">La commande suivante indique à PowerShell d’obtenir tous les utilisateurs dont l’attribut *DirSyncEnabled* est défini sur *true*.</span><span class="sxs-lookup"><span data-stu-id="38507-132">The following command instructs PowerShell to get all users who have the attribute *DirSyncEnabled* set to *True*.</span></span> <span data-ttu-id="38507-133">Vous pouvez l’utiliser pour rechercher les comptes qui sont synchronisés à partir d’AD sur site.</span><span class="sxs-lookup"><span data-stu-id="38507-133">You can use it to find accounts that are synchronizing from on-premise AD.</span></span>

```powershell
Get-AzureADUser | Where {$_.DirSyncEnabled -eq $true}
```

<span data-ttu-id="38507-134">La commande suivante indique à PowerShell d’obtenir tous les utilisateurs dont l’attribut *DirSyncEnabled* est défini sur *false*.</span><span class="sxs-lookup"><span data-stu-id="38507-134">The following command instructs PowerShell to get all users who have the attribute *DirSyncEnabled* set to *False*.</span></span> <span data-ttu-id="38507-135">Vous pouvez l’utiliser pour rechercher des comptes en nuage uniquement.</span><span class="sxs-lookup"><span data-stu-id="38507-135">You can use it to find cloud-only accounts.</span></span>

```powershell
Get-AzureADUser | Where {$_.DirSyncEnabled -ne $false}
```

### <a name="view-accounts-based-on-a-common-property"></a><span data-ttu-id="38507-136">Afficher les comptes en fonction d’une propriété commune</span><span class="sxs-lookup"><span data-stu-id="38507-136">View accounts based on a common property</span></span>

<span data-ttu-id="38507-137">Pour être plus sélectif sur la liste des comptes à afficher, vous pouvez utiliser la cmdlet **Where** en combinaison avec la cmdlet **Get-AzureADUser** .</span><span class="sxs-lookup"><span data-stu-id="38507-137">To be more selective about the list of accounts to display, you can use the **Where** cmdlet in combination with the **Get-AzureADUser** cmdlet.</span></span> <span data-ttu-id="38507-138">Pour combiner les deux cmdlets, utilisez le caractère « pipe » (« | »), qui indique à Azure Active Directory PowerShell pour Graph de prendre les résultats d’une commande et de l’envoyer à la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="38507-138">To combine the two cmdlets, use the "pipe" character ("|"), which tells Azure Active Directory PowerShell for Graph to take the results of one command and send it to the next command.</span></span> <span data-ttu-id="38507-139">Voici un exemple de commande qui affiche uniquement les comptes d’utilisateur dont l’emplacement d’utilisation n’est pas spécifié :</span><span class="sxs-lookup"><span data-stu-id="38507-139">Here's an example command that displays only those user accounts that have an unspecified usage location:</span></span>
  
```powershell
Get-AzureADUser | Where {$_.UsageLocation -eq $Null}
```

<span data-ttu-id="38507-140">Cette commande demande à Azure Active Directory PowerShell pour Graph d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="38507-140">This command instructs Azure Active Directory PowerShell for Graph to:</span></span>
  
1. <span data-ttu-id="38507-141">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-AzureADUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="38507-141">Get all the information on the user accounts (**Get-AzureADUser**) and send it to the next command (**|**).</span></span>
    
1. <span data-ttu-id="38507-142">Recherchez tous les comptes d’utilisateur dont l’emplacement d’utilisation n’est pas spécifié (**où {$ \_ . UsageLocation-EQ $Null}**).</span><span class="sxs-lookup"><span data-stu-id="38507-142">Find all the user accounts that have an unspecified usage location (**Where {$\_.UsageLocation -eq $Null}**).</span></span> <span data-ttu-id="38507-143">À l’intérieur des accolades, la commande demande à PowerShell de trouver uniquement l’ensemble des comptes pour lesquels la propriété de compte d’utilisateur UsageLocation (\*\* $ \_ . UsageLocation**) n’est pas spécifié (**-EQ $null\*\*).</span><span class="sxs-lookup"><span data-stu-id="38507-143">Inside the braces, the command instructs PowerShell to only find the set of accounts for which the UsageLocation user account property (**$\_.UsageLocation**) is not specified (**-eq $Null**).</span></span>
    
<span data-ttu-id="38507-144">La propriété **UsageLocation** n’est que l’une des nombreuses propriétés associées à un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38507-144">The **UsageLocation** property is only one of many properties associated with a user account.</span></span> <span data-ttu-id="38507-145">Pour afficher toutes les propriétés d’un compte d’utilisateur spécifique, utilisez l’applet de commande **Select** et le caractère générique (\*).</span><span class="sxs-lookup"><span data-stu-id="38507-145">To display all the properties for a specific user account, use the **Select** cmdlet and the wildcard character (\*).</span></span> <span data-ttu-id="38507-146">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="38507-146">Here's an example:</span></span>
  
```powershell
Get-AzureADUser -ObjectID BelindaN@litwareinc.onmicosoft.com | Select *
```

<span data-ttu-id="38507-147">Par exemple, **Ville** est le nom d’une propriété de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38507-147">For example, **City** is the name of a user account property.</span></span> <span data-ttu-id="38507-148">Vous pouvez utiliser la commande suivante pour répertorier tous les comptes d’utilisateurs vivant à Londres :</span><span class="sxs-lookup"><span data-stu-id="38507-148">You can use the following command to list all accounts of users who live in London:</span></span>
  
```powershell
Get-AzureADUser | Where {$_.City -eq "London"}
```

> [!TIP]
>  <span data-ttu-id="38507-149">La syntaxe de la cmdlet **Where** de ces exemples est **where {$ \_ .**</span><span class="sxs-lookup"><span data-stu-id="38507-149">The syntax for the **Where** cmdlet in these examples is **Where {$\_.**</span></span> <span data-ttu-id="38507-150">[nom de la propriété du compte d’utilisateur] [opérateur de comparaison] valeur **}**. > [opérateur de comparaison] est **-EQ** pour Equals, **-** ne pour « différent de », **-lt** pour inférieur à, **-gt** pour supérieur à, et autres.</span><span class="sxs-lookup"><span data-stu-id="38507-150">[user account property name] [comparison operator] [value] **}**.> [comparison operator] is **-eq** for equals, **-ne** for not equals, **-lt** for less than, **-gt** for greater than, and others.</span></span>  <span data-ttu-id="38507-151">[valeur] est généralement une chaîne (une séquence de lettres, de chiffres et d’autres caractères), une valeur numérique ou **$null** pour non spécifié.</span><span class="sxs-lookup"><span data-stu-id="38507-151">[value] is typically a string (a sequence of letters, numbers, and other characters), a numerical value, or **$Null** for unspecified.</span></span> <span data-ttu-id="38507-152">Pour plus d’informations, voir [Where](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/where-object?view=powershell-7).</span><span class="sxs-lookup"><span data-stu-id="38507-152">For more information, see [Where](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/where-object?view=powershell-7).</span></span>
  

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="38507-153">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38507-153">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="38507-154">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="38507-154">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

### <a name="view-all-accounts"></a><span data-ttu-id="38507-155">Afficher tous les comptes</span><span class="sxs-lookup"><span data-stu-id="38507-155">View all accounts</span></span>

<span data-ttu-id="38507-156">Pour afficher la liste complète des comptes d’utilisateurs, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="38507-156">To display the full list of user accounts, run this command:</span></span>
  
```powershell
Get-MsolUser
```

>[!Note]
><span data-ttu-id="38507-157">PowerShell Core ne prend pas en charge les applets de commande et le module Microsoft Azure Active Directory pour Windows PowerShell avec *MSOL* dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="38507-157">PowerShell Core doesn't support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with *Msol* in their name.</span></span> <span data-ttu-id="38507-158">Exécutez ces applets de commande à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38507-158">Run these cmdlets from Windows PowerShell.</span></span>
>

<span data-ttu-id="38507-159">Vous devriez obtenir des informations semblables à celles-ci :</span><span class="sxs-lookup"><span data-stu-id="38507-159">You should get information similar to this:</span></span>
  
```powershell
UserPrincipalName                     DisplayName           isLicensed
-----------------                     -----------           ----------
BonnieK@litwareinc.onmicrosoft.com    Bonnie Kearney        True
FabriceC@litwareinc.onmicrosoft.com   Fabrice Canel         True
BrianJ@litwareinc.onmicrosoft.com     Brian Johnson         False 
AnneWlitwareinc.onmicrosoft.com       Anne Wallace          True
ScottW@litwareinc.onmicrosoft.com     Scott Wallace         False
```

<span data-ttu-id="38507-160">La cmdlet **Get-MsolUser** dispose également d’un jeu de paramètres pour filtrer l’ensemble de comptes utilisateur affichés.</span><span class="sxs-lookup"><span data-stu-id="38507-160">The **Get-MsolUser** cmdlet also has a set of parameters to filter the set of user accounts displayed.</span></span> <span data-ttu-id="38507-161">Par exemple, pour la liste des utilisateurs sans licence (utilisateurs qui ont été ajoutés à Microsoft 365 mais qui n’ont pas encore été concédés sous licence pour utiliser l’un des services), exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="38507-161">For example, for the list of unlicensed users (users who have been added to Microsoft 365 but haven't yet been licensed to use any of the services), run this command:</span></span>
  
```powershell
Get-MsolUser -UnlicensedUsersOnly
```

<span data-ttu-id="38507-162">Vous devriez obtenir des informations semblables à celles-ci :</span><span class="sxs-lookup"><span data-stu-id="38507-162">You should get information similar to this:</span></span>
  
```powershell
UserPrincipalName                     DisplayName           isLicensed
-----------------                     -----------           ----------
BrianJ@litwareinc.onmicrosoft.com     Brian Johnson         False
ScottW@litwareinc.onmicrosoft.com     Scott Wallace         False
```

<span data-ttu-id="38507-163">Pour plus d’informations sur les paramètres supplémentaires permettant de filtrer l’ensemble des comptes d’utilisateur affichés, consultez la rubrique [Get-MsolUser](https://docs.microsoft.com/previous-versions/azure/dn194133(v=azure.100)).</span><span class="sxs-lookup"><span data-stu-id="38507-163">For information about additional parameters to filter the set of user accounts that are displayed, see [Get-MsolUser](https://docs.microsoft.com/previous-versions/azure/dn194133(v=azure.100)).</span></span>
  
### <a name="view-a-specific-account"></a><span data-ttu-id="38507-164">Afficher un compte spécifique</span><span class="sxs-lookup"><span data-stu-id="38507-164">View a specific account</span></span>

<span data-ttu-id="38507-165">Pour afficher un compte d’utilisateur spécifique, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="38507-165">To display a specific user account, run the following command.</span></span> <span data-ttu-id="38507-166">Renseignez le nom de connexion du compte d’utilisateur, également appelé nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="38507-166">Fill in the sign-in name of the user account, which is also known as the user principal name (UPN).</span></span> <span data-ttu-id="38507-167">Supprimez les caractères « < » et « > ».</span><span class="sxs-lookup"><span data-stu-id="38507-167">Remove the "<" and ">" characters.</span></span>
  
```powershell
Get-MsolUser -UserPrincipalName <sign-in name of the user account>
```

### <a name="view-accounts-based-on-a-common-property"></a><span data-ttu-id="38507-168">Afficher les comptes en fonction d’une propriété commune</span><span class="sxs-lookup"><span data-stu-id="38507-168">View accounts based on a common property</span></span>

<span data-ttu-id="38507-169">Pour être plus sélectif sur la liste des comptes à afficher, vous pouvez utiliser la cmdlet **Where** en combinaison avec la cmdlet **Get-MsolUser** .</span><span class="sxs-lookup"><span data-stu-id="38507-169">To be more selective about the list of accounts to display, you can use the **Where** cmdlet in combination with the **Get-MsolUser** cmdlet.</span></span> <span data-ttu-id="38507-170">Pour combiner les deux cmdlets, utilisez le caractère « pipe » (« | »), qui indique à PowerShell de prendre les résultats d’une commande et de l’envoyer à la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="38507-170">To combine the two cmdlets, use the "pipe" character ("|"), which tells PowerShell to take the results of one command and send it to the next command.</span></span> <span data-ttu-id="38507-171">Voici un exemple qui affiche uniquement les comptes d’utilisateur dont l’emplacement d’utilisation n’est pas spécifié :</span><span class="sxs-lookup"><span data-stu-id="38507-171">Here's an example that displays only those user accounts that have an unspecified usage location:</span></span>
  
```powershell
Get-MsolUser | Where {$_.UsageLocation -eq $Null}
```

<span data-ttu-id="38507-172">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="38507-172">This command instructs PowerShell to:</span></span>
  
1. <span data-ttu-id="38507-173">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-MsolUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="38507-173">Get all the information on the user accounts (**Get-MsolUser**) and send it to the next command (**|**).</span></span>
    
1. <span data-ttu-id="38507-174">Recherchez tous les comptes d’utilisateur dont l’emplacement d’utilisation n’est pas spécifié (**où {$ \_ . UsageLocation-EQ $Null}**).</span><span class="sxs-lookup"><span data-stu-id="38507-174">Find all user accounts that have an unspecified usage location (**Where {$\_.UsageLocation -eq $Null}**).</span></span> <span data-ttu-id="38507-175">À l’intérieur des accolades, la commande demande à PowerShell de rechercher uniquement l’ensemble des comptes pour lesquels la propriété de compte d’utilisateur UsageLocation (\*\* $ \_ . UsageLocation**) n’est pas spécifié (**-EQ $null\*\*).</span><span class="sxs-lookup"><span data-stu-id="38507-175">Inside the braces, the command instructs PowerShell to find only the set of accounts for which the UsageLocation user account property (**$\_.UsageLocation**) is not specified (**-eq $Null**).</span></span>
    
<span data-ttu-id="38507-176">Vous devriez obtenir des informations semblables à celles-ci :</span><span class="sxs-lookup"><span data-stu-id="38507-176">You should get information similar to this:</span></span>
  
```powershell
UserPrincipalName                     DisplayName           isLicensed
-----------------                     -----------           ----------
BrianJ@litwareinc.onmicrosoft.com     Brian Johnson         False 
ScottW@litwareinc.onmicrosoft.com     Scott Wallace         False

```

<span data-ttu-id="38507-177">La propriété *UsageLocation* n’est que l’une des nombreuses propriétés associées à un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38507-177">The *UsageLocation* property is only one of many properties associated with a user account.</span></span> <span data-ttu-id="38507-178">Pour afficher toutes les propriétés des comptes d’utilisateur, utilisez l’applet de commande **Select** et le caractère générique (\*) pour les afficher tous pour un compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="38507-178">To see all of the properties for user accounts, use the **Select** cmdlet and the wildcard character (\*) to display them all for a specific user account.</span></span> <span data-ttu-id="38507-179">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="38507-179">Here's an example:</span></span>
  
```powershell
Get-MsolUser -UserPrincipalName BelindaN@litwareinc.onmicosoft.com | Select *
```

<span data-ttu-id="38507-180">Par exemple, *Ville* est le nom d’une propriété de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38507-180">For example, *City* is the name of a user account property.</span></span> <span data-ttu-id="38507-181">Vous pouvez utiliser la commande suivante pour répertorier tous les comptes d’utilisateur pour les utilisateurs qui vivent à Londres :</span><span class="sxs-lookup"><span data-stu-id="38507-181">You can use the following command to list all of the user accounts for users who live in London:</span></span>
  
```powershell
Get-MsolUser | Where {$_.City -eq "London"}
```

> [!TIP]
>  <span data-ttu-id="38507-182">La syntaxe de la cmdlet **Where** de ces exemples est **where {$ \_ .**</span><span class="sxs-lookup"><span data-stu-id="38507-182">The syntax for the **Where** cmdlet in these examples is **Where {$\_.**</span></span> <span data-ttu-id="38507-183">[nom de la propriété du compte d’utilisateur] [opérateur de comparaison] valeur **}**.</span><span class="sxs-lookup"><span data-stu-id="38507-183">[user account property name] [comparison operator] [value] **}**.</span></span>  <span data-ttu-id="38507-184">[opérateur de comparaison] est **-EQ** pour Equals, **-** ne pour « différent de », **-lt** pour inférieur à, **-gt** pour supérieur à, et autres.</span><span class="sxs-lookup"><span data-stu-id="38507-184">[comparison operator] is **-eq** for equals, **-ne** for not equals, **-lt** for less than, **-gt** for greater than, and others.</span></span>  <span data-ttu-id="38507-185">[valeur] est généralement une chaîne (une séquence de lettres, de chiffres et d’autres caractères), une valeur numérique ou **$null** pour non spécifié.</span><span class="sxs-lookup"><span data-stu-id="38507-185">[value] is typically a string (a sequence of letters, numbers, and other characters), a numerical value, or **$Null** for unspecified.</span></span> <span data-ttu-id="38507-186">Pour plus d’informations, voir [Where](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/where-object?view=powershell-7).</span><span class="sxs-lookup"><span data-stu-id="38507-186">For more information, see [Where](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/where-object?view=powershell-7).</span></span>
  
<span data-ttu-id="38507-187">Pour vérifier l’État bloqué d’un compte d’utilisateur, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="38507-187">To check the blocked status of a user account, use the following command:</span></span>
  
```powershell
Get-MsolUser -UserPrincipalName <UPN of user account> | Select DisplayName,BlockCredential
```

### <a name="view-additional-property-values-for-accounts"></a><span data-ttu-id="38507-188">Afficher les valeurs des propriétés supplémentaires des comptes</span><span class="sxs-lookup"><span data-stu-id="38507-188">View additional property values for accounts</span></span>

<span data-ttu-id="38507-189">Par défaut, la cmdlet **Get-MsolUser** affiche ces trois propriétés des comptes d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="38507-189">By default, the **Get-MsolUser** cmdlet displays these three properties of user accounts:</span></span>
  
- <span data-ttu-id="38507-190">UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="38507-190">UserPrincipalName</span></span>
    
- <span data-ttu-id="38507-191">DisplayName</span><span class="sxs-lookup"><span data-stu-id="38507-191">DisplayName</span></span>
    
- <span data-ttu-id="38507-192">isLicensed</span><span class="sxs-lookup"><span data-stu-id="38507-192">isLicensed</span></span>
    
<span data-ttu-id="38507-193">Si vous avez besoin de propriétés supplémentaires, telles que le service dans lequel travaille l’utilisateur et le pays/la région où ils utilisent les services Microsoft 365, vous pouvez exécuter **Get-MsolUser** en combinaison avec l’applet de commande **Select** pour spécifier la liste des propriétés du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38507-193">If you need additional properties, such as the department where the user works and the country/region where they use Microsoft 365 services, you can run **Get-MsolUser** in combination with the **Select** cmdlet to specify the list of user account properties.</span></span> <span data-ttu-id="38507-194">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="38507-194">Here's an example:</span></span>
  
```powershell
Get-MsolUser | Select DisplayName, Department, UsageLocation
```

<span data-ttu-id="38507-195">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="38507-195">This command instructs PowerShell to:</span></span>
  
1. <span data-ttu-id="38507-196">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-MsolUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="38507-196">Get all the information about the user accounts (**Get-MsolUser**) and send it to the next command (**|**).</span></span>
    
1. <span data-ttu-id="38507-197">Afficher uniquement le nom du compte d’utilisateur, le service et l’emplacement d’utilisation (**Sélectionnez DisplayName, Department, UsageLocation**).</span><span class="sxs-lookup"><span data-stu-id="38507-197">Display only the user account name, department, and usage location (**Select DisplayName, Department, UsageLocation**).</span></span>
    
<span data-ttu-id="38507-198">Vous devriez obtenir des informations semblables à celles-ci :</span><span class="sxs-lookup"><span data-stu-id="38507-198">You should get information similar to this:</span></span>
  
```powershell
DisplayName             Department                       UsageLocation
-----------             ----------                       -------------
Bonnie Kearney          Sales & Marketing                    US
Fabrice Canel           Legal                                US
Brian Johnson
Anne Wallace            Executive Management                 US
Alex Darrow             Sales & Marketing                    US
Scott Wallace           Operations
```

<span data-ttu-id="38507-199">L’applet de commande **Select** vous permet de choisir les propriétés à afficher.</span><span class="sxs-lookup"><span data-stu-id="38507-199">The **Select** cmdlet lets you choose what properties to display.</span></span> <span data-ttu-id="38507-200">Pour afficher toutes les propriétés d’un compte d’utilisateur spécifique, utilisez le caractère générique (\*).</span><span class="sxs-lookup"><span data-stu-id="38507-200">To display all the properties for a specific user account, use the wildcard character (\*).</span></span> <span data-ttu-id="38507-201">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="38507-201">Here's an example:</span></span>
  
```powershell
Get-MsolUser -UserPrincipalName BelindaN@litwareinc.onmicosoft.com | Select *
```

<span data-ttu-id="38507-202">Pour être plus sélectif sur la liste des comptes à afficher, vous pouvez également utiliser la cmdlet **Where** .</span><span class="sxs-lookup"><span data-stu-id="38507-202">To be more selective about the list of accounts to display, you can also use the **Where** cmdlet.</span></span> <span data-ttu-id="38507-203">Voici un exemple de commande qui affiche uniquement les comptes d’utilisateur dont l’emplacement d’utilisation n’est pas spécifié :</span><span class="sxs-lookup"><span data-stu-id="38507-203">Here's an example command that displays only those user accounts that have an unspecified usage location:</span></span>
  
```powershell
Get-MsolUser | Where {$_.UsageLocation -eq $Null} | Select DisplayName, Department, UsageLocation
```

<span data-ttu-id="38507-204">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="38507-204">This command instructs PowerShell to:</span></span>
  
1. <span data-ttu-id="38507-205">Obtenir toutes les informations sur les comptes d’utilisateur (**Get-MsolUser**) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="38507-205">Get all the information about the user accounts (**Get-MsolUser**) and send it to the next command (**|**).</span></span>
    
1. <span data-ttu-id="38507-206">Recherchez tous les comptes d’utilisateur dont l’emplacement d’utilisation n’est pas spécifié (**où {$ \_ . UsageLocation-EQ $Null}**) et envoyer les informations obtenues à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="38507-206">Find all user accounts that have an unspecified usage location (**Where {$\_.UsageLocation -eq $Null}**), and send the resulting information to the next command (**|**).</span></span> <span data-ttu-id="38507-207">À l’intérieur des accolades, la commande demande à PowerShell de trouver uniquement l’ensemble des comptes pour lesquels la propriété de compte d’utilisateur UsageLocation (\*\* $ \_ . UsageLocation**) n’est pas spécifié (**-EQ $null\*\*).</span><span class="sxs-lookup"><span data-stu-id="38507-207">Inside the braces, the command instructs PowerShell to only find the set of accounts for which the UsageLocation user account property (**$\_.UsageLocation**) is not specified (**-eq $Null**).</span></span>
    
1. <span data-ttu-id="38507-208">Afficher uniquement le nom du compte d’utilisateur, le service et l’emplacement d’utilisation (**Sélectionnez DisplayName, Department, UsageLocation**).</span><span class="sxs-lookup"><span data-stu-id="38507-208">Display only the user account name, department, and usage location (**Select DisplayName, Department, UsageLocation**).</span></span>
    
<span data-ttu-id="38507-209">Vous devriez obtenir des informations semblables à celles-ci :</span><span class="sxs-lookup"><span data-stu-id="38507-209">You should get information similar to this:</span></span>
  
```powershell
DisplayName              Department                      UsageLocation
-----------              ----------                      -------------
Brian Johnson 
Scott Wallace            Operations
```

<span data-ttu-id="38507-210">Si vous utilisez la synchronisation d’annuaires pour créer et gérer vos utilisateurs de Microsoft 365, vous pouvez afficher le compte local à partir duquel un utilisateur de Microsoft 365 a été projeté.</span><span class="sxs-lookup"><span data-stu-id="38507-210">If you're using directory synchronization to create and manage your Microsoft 365 users, you can display the local account from which a Microsoft 365 user has been projected.</span></span> <span data-ttu-id="38507-211">L’exemple suivant suppose que :</span><span class="sxs-lookup"><span data-stu-id="38507-211">The following example assumes that:</span></span>

- <span data-ttu-id="38507-212">Azure AD Connect est configuré pour utiliser l’ancre source par défaut d’ObjectGUID.</span><span class="sxs-lookup"><span data-stu-id="38507-212">Azure AD Connect is configured to use the default source anchor of ObjectGUID.</span></span> <span data-ttu-id="38507-213">(Pour plus d’informations sur la configuration d’une ancre source, reportez-vous à la rubrique [Azure ad Connect : Design concepts](https://docs.microsoft.com/azure/active-directory/hybrid/plan-connect-design-concepts)).</span><span class="sxs-lookup"><span data-stu-id="38507-213">(For more information about configuring a source anchor, see [Azure AD Connect: Design concepts](https://docs.microsoft.com/azure/active-directory/hybrid/plan-connect-design-concepts)).</span></span>
- <span data-ttu-id="38507-214">Le module des services de domaine Active Directory pour PowerShell a été installé (voir [outils RSAT](https://www.microsoft.com/en-gb/download/details.aspx?id=45520)).</span><span class="sxs-lookup"><span data-stu-id="38507-214">The Active Directory Domain Services module for PowerShell has been installed (see [RSAT tools](https://www.microsoft.com/en-gb/download/details.aspx?id=45520)).</span></span>

```powershell
Get-ADUser ([guid][System.Convert]::FromBase64String((Get-MsolUser -UserPrincipalName <UPN of user account>).ImmutableID)).guid
```

## <a name="see-also"></a><span data-ttu-id="38507-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38507-215">See also</span></span>

[<span data-ttu-id="38507-216">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="38507-216">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="38507-217">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="38507-217">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="38507-218">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="38507-218">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
