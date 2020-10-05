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
ms.openlocfilehash: 4dba05ce440ec0d395fda58a12df3e9f751bb469
ms.sourcegitcommit: 8589323c1b4ab43aab30597ee66303b0a0eb71ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/05/2020
ms.locfileid: "48357897"
---
# <a name="view-microsoft-365-user-accounts-with-powershell"></a><span data-ttu-id="57fd6-103">Afficher les comptes d’utilisateur Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="57fd6-103">View Microsoft 365 user accounts with PowerShell</span></span>

<span data-ttu-id="57fd6-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="57fd6-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="57fd6-105">Bien que vous puissiez utiliser le centre d’administration Microsoft 365 pour afficher les comptes de votre client Microsoft 365, vous pouvez également utiliser PowerShell pour Microsoft 365 et effectuer quelques opérations que le centre d’administration ne peut pas faire.</span><span class="sxs-lookup"><span data-stu-id="57fd6-105">Although you can use the Microsoft 365 admin center to view the accounts for your Microsoft 365 tenant, you can also use PowerShell for Microsoft 365 and do some things that the admin center cannot.</span></span>
  
## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="57fd6-106">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="57fd6-106">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="57fd6-107">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="57fd6-107">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
### <a name="view-all-accounts"></a><span data-ttu-id="57fd6-108">Afficher tous les comptes</span><span class="sxs-lookup"><span data-stu-id="57fd6-108">View all accounts</span></span>

<span data-ttu-id="57fd6-109">Pour afficher la liste complète des comptes d’utilisateurs, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="57fd6-109">To display the full list of user accounts, run this command:</span></span>
  
```powershell
Get-AzureADUser
```

<span data-ttu-id="57fd6-110">Les informations affichées devraient être semblables à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="57fd6-110">You should see information similar to this:</span></span>
  
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

### <a name="view-a-specific-account"></a><span data-ttu-id="57fd6-111">Afficher un compte spécifique</span><span class="sxs-lookup"><span data-stu-id="57fd6-111">View a specific account</span></span>

<span data-ttu-id="57fd6-112">Pour afficher un compte d’utilisateur spécifique, renseignez le nom du compte d’utilisateur, également appelé nom d’utilisateur principal (UPN), supprimez les caractères « < » et « > », puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="57fd6-112">To display a specific user account, fill in the sign-in account name of the user account, also known as the user principal name (UPN), remove the "<" and ">" characters, and run this command:</span></span>
  
```powershell
Get-AzureADUser -ObjectID <sign-in name of the user account>
```

<span data-ttu-id="57fd6-113">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="57fd6-113">Here is an example:</span></span>
  
```powershell
Get-AzureADUser -ObjectID BelindaN@litwareinc.onmicosoft.com
```

### <a name="view-additional-property-values-for-a-specific-account"></a><span data-ttu-id="57fd6-114">Afficher des valeurs de propriétés supplémentaires pour un compte spécifique</span><span class="sxs-lookup"><span data-stu-id="57fd6-114">View additional property values for a specific account</span></span>

<span data-ttu-id="57fd6-115">Par défaut, la cmdlet **Get-AzureADUser** affiche uniquement les propriétés ObjectId, DisplayName et userPrincipalName des comptes.</span><span class="sxs-lookup"><span data-stu-id="57fd6-115">By default, the **Get-AzureADUser** cmdlet only displays the ObjectID, DisplayName, and UserPrincipalName properties of accounts.</span></span>

<span data-ttu-id="57fd6-116">Pour être plus sélectif sur la liste des propriétés à afficher, vous pouvez utiliser l’applet de commande **Select** en combinaison avec la cmdlet **Get-AzureADUser** .</span><span class="sxs-lookup"><span data-stu-id="57fd6-116">To be more selective about the list of properties to display, you can use the **Select** cmdlet in combination with the **Get-AzureADUser** cmdlet.</span></span> <span data-ttu-id="57fd6-117">Pour combiner les deux cmdlets, nous utilisons le caractère « pipe » « | », qui indique à Azure Active Directory PowerShell pour Graph de prendre les résultats d’une commande et de l’envoyer à la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="57fd6-117">To combine the two cmdlets, we use the "pipe" character "|", which tells Azure Active Directory PowerShell for Graph to take the results of one command and send it to the next command.</span></span> <span data-ttu-id="57fd6-118">Voici un exemple de commande qui affiche les DisplayName, Department et UsageLocation pour chaque compte d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="57fd6-118">Here is an example command that displays the DisplayName, Department, and UsageLocation for every user account:</span></span>
  
```powershell
Get-AzureADUser | Select DisplayName,Department,UsageLocation
```

<span data-ttu-id="57fd6-119">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="57fd6-119">This command instructs PowerShell to:</span></span>
  
- <span data-ttu-id="57fd6-120">Obtenir toutes les informations sur les comptes d’utilisateur ( **Get-AzureADUser** ) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-120">Get all of the information on the user accounts ( **Get-AzureADUser** ) and send it to the next command ( **|** ).</span></span>
    
- <span data-ttu-id="57fd6-121">Afficher uniquement le nom du compte d’utilisateur, le service et l’emplacement d’utilisation ( **Sélectionnez DisplayName, Department, UsageLocation** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-121">Display only the user account name, department, and usage location ( **Select DisplayName, Department, UsageLocation** ).</span></span>
  
<span data-ttu-id="57fd6-122">Pour afficher toutes les propriétés des comptes d’utilisateur, utilisez l’applet de commande **Select** et le caractère générique (\*) pour les afficher tous pour un compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="57fd6-122">To see all of the properties for user accounts, use the **Select** cmdlet and the wildcard character (\*) to display them all for a specific user account.</span></span> <span data-ttu-id="57fd6-123">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="57fd6-123">Here is an example:</span></span>
  
```powershell
Get-AzureADUser -ObjectID BelindaN@litwareinc.onmicosoft.com | Select *
```

<span data-ttu-id="57fd6-124">Autre exemple : vous pouvez vérifier l’état activé d’un compte d’utilisateur spécifique à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="57fd6-124">As another example, you can check the enabled status of a specific user account with the following command:</span></span>
  
```powershell
Get-AzureADUser -ObjectID <sign-in name of the user account> | Select DisplayName,UserPrincipalName,AccountEnabled
```

### <a name="view-account-synchronization-status"></a><span data-ttu-id="57fd6-125">Afficher l’état de la synchronisation des comptes</span><span class="sxs-lookup"><span data-stu-id="57fd6-125">View account synchronization status</span></span>

<span data-ttu-id="57fd6-126">Les comptes d’utilisateur ont deux sources ; Windows Server Active Directory (AD), qui sont des comptes synchronisés à partir d’AD sur site vers le Cloud et Azure AD, qui sont des comptes créés directement dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="57fd6-126">User accounts have two sources; Windows Server Active Directory (AD) which are accounts that sync from on-premises AD to the cloud and Azure AD which are accounts directly created in the cloud.</span></span>

```powershell
Get-AzureADUser | Where {$_.DirSyncEnabled -eq $true}
```
<span data-ttu-id="57fd6-127">Cette commande demande à PowerShell d’obtenir tous les utilisateurs dont l’attribut **DirSyncEnabled** est défini sur true.</span><span class="sxs-lookup"><span data-stu-id="57fd6-127">This command instructs PowerShell to get all users who have the attribute **DirSyncEnabled** set to True.</span></span> <span data-ttu-id="57fd6-128">Il peut être utilisé pour extraire les comptes en les synchronisant à partir d’AD sur site.</span><span class="sxs-lookup"><span data-stu-id="57fd6-128">It can be used to pull up accounts synchronizing from on-premise AD.</span></span>


```powershell
Get-AzureADUser | Where {$_.DirSyncEnabled -ne $true}
```
<span data-ttu-id="57fd6-129">Cette commande demande à PowerShell d’obtenir tous les utilisateurs dont l’attribut **DirSyncEnabled** est défini sur false.</span><span class="sxs-lookup"><span data-stu-id="57fd6-129">This command instructs PowerShell to get all users who have the attribute **DirSyncEnabled** set to False.</span></span> <span data-ttu-id="57fd6-130">Il peut être utilisé pour extraire des comptes en nuage uniquement.</span><span class="sxs-lookup"><span data-stu-id="57fd6-130">It can be used to pull up cloud-only accounts.</span></span>

### <a name="view-some-accounts-based-on-a-common-property"></a><span data-ttu-id="57fd6-131">Afficher certains comptes en fonction d’une propriété commune</span><span class="sxs-lookup"><span data-stu-id="57fd6-131">View some accounts based on a common property</span></span>

<span data-ttu-id="57fd6-132">Pour être plus sélectif sur la liste des comptes à afficher, vous pouvez utiliser la cmdlet **Where** en combinaison avec la cmdlet **Get-AzureADUser** .</span><span class="sxs-lookup"><span data-stu-id="57fd6-132">To be more selective about the list of accounts to display, you can use the **Where** cmdlet in combination with the **Get-AzureADUser** cmdlet.</span></span> <span data-ttu-id="57fd6-133">Pour combiner les deux cmdlets, nous utilisons le caractère « pipe » « | », qui indique à Azure Active Directory PowerShell pour Graph de prendre les résultats d’une commande et de l’envoyer à la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="57fd6-133">To combine the two cmdlets, we use the "pipe" character "|", which tells Azure Active Directory PowerShell for Graph to take the results of one command and send it to the next command.</span></span> <span data-ttu-id="57fd6-134">Voici un exemple de commande qui affiche uniquement les comptes utilisateur dont l’emplacement d’utilisation n’est pas spécifié :</span><span class="sxs-lookup"><span data-stu-id="57fd6-134">Here is an example command that displays only those user accounts that have an unspecified usage location:</span></span>
  
```powershell
Get-AzureADUser | Where {$_.UsageLocation -eq $Null}
```

<span data-ttu-id="57fd6-135">Cette commande demande à Azure Active Directory PowerShell pour Graph d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="57fd6-135">This command instructs Azure Active Directory PowerShell for Graph to:</span></span>
  
- <span data-ttu-id="57fd6-136">Obtenir toutes les informations sur les comptes d’utilisateur ( **Get-AzureADUser** ) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-136">Get all of the information on the user accounts ( **Get-AzureADUser** ) and send it to the next command ( **|** ).</span></span>
    
- <span data-ttu-id="57fd6-137">Recherchez tous les comptes d’utilisateur dont l’emplacement d’utilisation n’est pas spécifié ( **où {$ \_ . UsageLocation-EQ $Null}** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-137">Find all of the user accounts that have an unspecified usage location ( **Where {$\_.UsageLocation -eq $Null}** ).</span></span> <span data-ttu-id="57fd6-138">À l’intérieur des accolades, la commande demande à PowerShell de trouver uniquement le jeu de comptes dans lequel la propriété de compte d’utilisateur UsageLocation ( \*\* $ \_ . UsageLocation\*\* ) n’est pas spécifié ( **-EQ $null** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-138">Inside the braces, the command instructs PowerShell to only find the set of accounts in which the UsageLocation user account property ( **$\_.UsageLocation** ) is not specified ( **-eq $Null** ).</span></span>
    
<span data-ttu-id="57fd6-139">La propriété **UsageLocation** n’est que l’une des nombreuses propriétés associées à un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57fd6-139">The **UsageLocation** property is only one of many properties associated with a user account.</span></span> <span data-ttu-id="57fd6-140">Pour afficher toutes les propriétés des comptes d’utilisateur, utilisez l’applet de commande **Select** et le caractère générique (\*) pour les afficher tous pour un compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="57fd6-140">To see all of the properties for user accounts, use the **Select** cmdlet and the wildcard character (\*) to display them all for a specific user account.</span></span> <span data-ttu-id="57fd6-141">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="57fd6-141">Here is an example:</span></span>
  
```powershell
Get-AzureADUser -ObjectID BelindaN@litwareinc.onmicosoft.com | Select *
```

<span data-ttu-id="57fd6-p108">Par exemple, dans cette liste, **Ville** est le nom d’une propriété de compte d’utilisateur. Cela signifie que vous pouvez utiliser la commande suivante pour obtenir la liste des comptes d’utilisateur pour les utilisateurs qui habitent à Londres :</span><span class="sxs-lookup"><span data-stu-id="57fd6-p108">For example, from this list, **City** is the name of a user account property. This means you can use the following command to list all of the user accounts for users living in London:</span></span>
  
```powershell
Get-AzureADUser | Where {$_.City -eq "London"}
```

> [!TIP]
>  <span data-ttu-id="57fd6-144">La syntaxe de la cmdlet **Where** illustrée dans ces exemples est **where {$ \_ .**</span><span class="sxs-lookup"><span data-stu-id="57fd6-144">The syntax for the **Where** cmdlet shown in these examples is **Where {$\_.**</span></span> <span data-ttu-id="57fd6-145">[nom de la propriété du compte d’utilisateur] [opérateur de comparaison] valeur **}**. > [opérateur de comparaison] est **-EQ** pour Equals, **-** ne pour « différent de », **-lt** pour inférieur à, **-gt** pour supérieur à, et autres.</span><span class="sxs-lookup"><span data-stu-id="57fd6-145">[user account property name] [comparison operator] [value] **}**.>  [comparison operator] is **-eq** for equals, **-ne** for not equals, **-lt** for less than, **-gt** for greater than, and others.</span></span>  <span data-ttu-id="57fd6-146">[valeur] est généralement une chaîne (une séquence de lettres, de chiffres et d’autres caractères), une valeur numérique ou **$null** pour> voir [Where](https://docs.microsoft.com/powershell/module/Microsoft.PowerShell.Core/Where?view=powershell-5.1) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="57fd6-146">[value] is typically a string (a sequence of letters, numbers, and other characters), a numerical value, or **$Null** for unspecified>  See [Where](https://docs.microsoft.com/powershell/module/Microsoft.PowerShell.Core/Where?view=powershell-5.1) for more information.</span></span>
  

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="57fd6-147">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="57fd6-147">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="57fd6-148">Tout d’abord, [Connectez-vous à votre client Microsoft 365](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="57fd6-148">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

### <a name="view-all-accounts"></a><span data-ttu-id="57fd6-149">Afficher tous les comptes</span><span class="sxs-lookup"><span data-stu-id="57fd6-149">View all accounts</span></span>

<span data-ttu-id="57fd6-150">Pour afficher la liste complète des comptes d’utilisateurs, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="57fd6-150">To display the full list of user accounts, run this command:</span></span>
  
```powershell
Get-MsolUser
```

>[!Note]
><span data-ttu-id="57fd6-151">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="57fd6-151">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="57fd6-152">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="57fd6-152">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

<span data-ttu-id="57fd6-153">Les informations affichées devraient être semblables à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="57fd6-153">You should see information similar to this:</span></span>
  
```powershell
UserPrincipalName                     DisplayName           isLicensed
-----------------                     -----------           ----------
BonnieK@litwareinc.onmicrosoft.com    Bonnie Kearney        True
FabriceC@litwareinc.onmicrosoft.com   Fabrice Canel         True
BrianJ@litwareinc.onmicrosoft.com     Brian Johnson         False 
AnneWlitwareinc.onmicrosoft.com       Anne Wallace          True
ScottW@litwareinc.onmicrosoft.com     Scott Wallace         False
```

<span data-ttu-id="57fd6-154">La cmdlet **Get-MsolUser** dispose également d’un jeu de paramètres pour filtrer l’ensemble de comptes utilisateur affichés.</span><span class="sxs-lookup"><span data-stu-id="57fd6-154">The **Get-MsolUser** cmdlet also has a set of parameters to filter the set of user accounts displayed.</span></span> <span data-ttu-id="57fd6-155">Par exemple, pour la liste des utilisateurs sans licence (utilisateurs qui ont été ajoutés à Microsoft 365 mais qui n’ont pas encore été concédés sous licence pour utiliser l’un des services), exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="57fd6-155">For example, for the list of unlicensed users (users who've been added to Microsoft 365 but haven't yet been licensed to use any of the services), run this command.</span></span>
  
```powershell
Get-MsolUser -UnlicensedUsersOnly
```

<span data-ttu-id="57fd6-156">Les informations affichées devraient être semblables à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="57fd6-156">You should see information similar to this:</span></span>
  
```powershell
UserPrincipalName                     DisplayName           isLicensed
-----------------                     -----------           ----------
BrianJ@litwareinc.onmicrosoft.com     Brian Johnson         False
ScottW@litwareinc.onmicrosoft.com     Scott Wallace         False
```

<span data-ttu-id="57fd6-157">Pour plus d’informations sur les paramètres supplémentaires permettant de filtrer l’affichage de l’ensemble des comptes d’utilisateur affichés, consultez la rubrique [Get-MsolUser](https://docs.microsoft.com/previous-versions/azure/dn194133(v=azure.100)).</span><span class="sxs-lookup"><span data-stu-id="57fd6-157">For more information about additional parameters to filter the display the set of user accounts displayed, see [Get-MsolUser](https://docs.microsoft.com/previous-versions/azure/dn194133(v=azure.100)).</span></span>
  
### <a name="view-a-specific-account"></a><span data-ttu-id="57fd6-158">Afficher un compte spécifique</span><span class="sxs-lookup"><span data-stu-id="57fd6-158">View a specific account</span></span>

<span data-ttu-id="57fd6-159">Pour afficher un compte d’utilisateur spécifique, renseignez le nom de connexion du compte d’utilisateur, également appelé nom d’utilisateur principal (UPN), supprimez les caractères « < » et « > », puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="57fd6-159">To display a specific user account, fill in the sign-in name of the user account of the user account, also known as the user principal name (UPN), remove the "<" and ">" characters, and run this command:</span></span>
  
```powershell
Get-MsolUser -UserPrincipalName <sign-in name of the user account>
```

### <a name="view-some-accounts-based-on-a-common-property"></a><span data-ttu-id="57fd6-160">Afficher certains comptes en fonction d’une propriété commune</span><span class="sxs-lookup"><span data-stu-id="57fd6-160">View some accounts based on a common property</span></span>

<span data-ttu-id="57fd6-161">Pour être plus sélectif sur la liste des comptes à afficher, vous pouvez utiliser la cmdlet **Where** en combinaison avec la cmdlet **Get-MsolUser** .</span><span class="sxs-lookup"><span data-stu-id="57fd6-161">To be more selective about the list of accounts to display, you can use the **Where** cmdlet in combination with the **Get-MsolUser** cmdlet.</span></span> <span data-ttu-id="57fd6-162">Pour combiner les deux cmdlets, nous utilisons le caractère « pipe » « | », qui indique à PowerShell de prendre les résultats d’une commande et de l’envoyer à la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="57fd6-162">To combine the two cmdlets, we use the "pipe" character "|", which tells PowerShell to take the results of one command and send it to the next command.</span></span> <span data-ttu-id="57fd6-163">Voici un exemple de commande qui affiche uniquement les comptes utilisateur dont l’emplacement d’utilisation n’est pas spécifié :</span><span class="sxs-lookup"><span data-stu-id="57fd6-163">Here is an example command that displays only those user accounts that have an unspecified usage location:</span></span>
  
```powershell
Get-MsolUser | Where {$_.UsageLocation -eq $Null}
```

<span data-ttu-id="57fd6-164">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="57fd6-164">This command instructs PowerShell to:</span></span>
  
- <span data-ttu-id="57fd6-165">Obtenir toutes les informations sur les comptes utilisateur ( **Get-MsolUser** ) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-165">Get all of the information on the user accounts ( **Get-MsolUser** ) and send it to the next command ( **|** ).</span></span>
    
- <span data-ttu-id="57fd6-166">Recherchez tous les comptes d’utilisateur dont l’emplacement d’utilisation n’est pas spécifié ( **où {$ \_ . UsageLocation-EQ $Null}** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-166">Find all of the user accounts that have an unspecified usage location ( **Where {$\_.UsageLocation -eq $Null}** ).</span></span> <span data-ttu-id="57fd6-167">À l’intérieur des accolades, la commande demande à PowerShell de trouver uniquement le jeu de comptes dans lequel la propriété de compte d’utilisateur UsageLocation ( \*\* $ \_ . UsageLocation\*\* ) n’est pas spécifié ( **-EQ $null** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-167">Inside the braces, the command instructs PowerShell to only find the set of accounts in which the UsageLocation user account property ( **$\_.UsageLocation** ) is not specified ( **-eq $Null** ).</span></span>
    
<span data-ttu-id="57fd6-168">Les informations affichées devraient être semblables à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="57fd6-168">You should see information similar to this:</span></span>
  
```powershell
UserPrincipalName                     DisplayName           isLicensed
-----------------                     -----------           ----------
BrianJ@litwareinc.onmicrosoft.com     Brian Johnson         False 
ScottW@litwareinc.onmicrosoft.com     Scott Wallace         False

```

<span data-ttu-id="57fd6-169">La propriété **UsageLocation** n’est que l’une des nombreuses propriétés associées à un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57fd6-169">The **UsageLocation** property is only one of many properties associated with a user account.</span></span> <span data-ttu-id="57fd6-170">Pour afficher toutes les propriétés des comptes d’utilisateur, utilisez l’applet de commande **Select** et le caractère générique (\*) pour les afficher tous pour un compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="57fd6-170">To see all of the properties for user accounts, use the **Select** cmdlet and the wildcard character (\*) to display them all for a specific user account.</span></span> <span data-ttu-id="57fd6-171">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="57fd6-171">Here is an example:</span></span>
  
```powershell
Get-MsolUser -UserPrincipalName BelindaN@litwareinc.onmicosoft.com | Select *
```

<span data-ttu-id="57fd6-p115">Par exemple, dans cette liste, **Ville** est le nom d’une propriété de compte d’utilisateur. Cela signifie que vous pouvez utiliser la commande suivante pour obtenir la liste des comptes d’utilisateur pour les utilisateurs qui habitent à Londres :</span><span class="sxs-lookup"><span data-stu-id="57fd6-p115">For example, from this list, **City** is the name of a user account property. This means you can use the following command to list all of the user accounts for users living in London:</span></span>
  
```powershell
Get-MsolUser | Where {$_.City -eq "London"}
```

> [!TIP]
>  <span data-ttu-id="57fd6-174">La syntaxe de la cmdlet **Where** illustrée dans ces exemples est **where {$ \_ .**</span><span class="sxs-lookup"><span data-stu-id="57fd6-174">The syntax for the **Where** cmdlet shown in these examples is **Where {$\_.**</span></span> <span data-ttu-id="57fd6-175">[nom de la propriété du compte d’utilisateur] [opérateur de comparaison] valeur **}**.</span><span class="sxs-lookup"><span data-stu-id="57fd6-175">[user account property name] [comparison operator] [value] **}**.</span></span>  <span data-ttu-id="57fd6-176">[opérateur de comparaison] est **-EQ** pour Equals, **-** ne pour « différent de », **-lt** pour inférieur à, **-gt** pour supérieur à, et autres.</span><span class="sxs-lookup"><span data-stu-id="57fd6-176">[comparison operator] is **-eq** for equals, **-ne** for not equals, **-lt** for less than, **-gt** for greater than, and others.</span></span>  <span data-ttu-id="57fd6-177">[valeur] est généralement une chaîne (une séquence de lettres, de chiffres et d’autres caractères), une valeur numérique ou **$null** pour non spécifié.</span><span class="sxs-lookup"><span data-stu-id="57fd6-177">[value] is typically a string (a sequence of letters, numbers, and other characters), a numerical value, or **$Null** for unspecified.</span></span> <span data-ttu-id="57fd6-178">Pour plus d’informations, consultez la rubrique [Where](https://technet.microsoft.com/library/hh849715.aspx) .</span><span class="sxs-lookup"><span data-stu-id="57fd6-178">See [Where](https://technet.microsoft.com/library/hh849715.aspx) for more information.</span></span>
  
<span data-ttu-id="57fd6-179">Vous pouvez vérifier l’État bloqué d’un compte d’utilisateur à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="57fd6-179">You can check the blocked status of a user account with the following command:</span></span>
  
```powershell
Get-MsolUser -UserPrincipalName <UPN of user account> | Select DisplayName,BlockCredential
```

### <a name="view-additional-property-values-for-accounts"></a><span data-ttu-id="57fd6-180">Afficher les valeurs des propriétés supplémentaires des comptes</span><span class="sxs-lookup"><span data-stu-id="57fd6-180">View additional property values for accounts</span></span>

<span data-ttu-id="57fd6-181">La cmdlet **Get-MsolUser** affiche par défaut trois propriétés des comptes d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="57fd6-181">The **Get-MsolUser** cmdlet by default displays three properties of user accounts:</span></span>
  
- <span data-ttu-id="57fd6-182">UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="57fd6-182">UserPrincipalName</span></span>
    
- <span data-ttu-id="57fd6-183">DisplayName</span><span class="sxs-lookup"><span data-stu-id="57fd6-183">DisplayName</span></span>
    
- <span data-ttu-id="57fd6-184">isLicensed</span><span class="sxs-lookup"><span data-stu-id="57fd6-184">isLicensed</span></span>
    
<span data-ttu-id="57fd6-185">Si vous avez besoin de propriétés supplémentaires, telles que le service pour lequel l’utilisateur travaille pour et le pays/la région où l’utilisateur utilise les services Microsoft 365, vous pouvez exécuter **Get-MsolUser** en combinaison avec l’applet de commande **Select** pour spécifier la liste des propriétés du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57fd6-185">If you need additional properties, such as the department the user works for and the country/region where the user uses Microsoft 365 services, you can run **Get-MsolUser** in combination with the **Select** cmdlet to specify the list of user account properties.</span></span> <span data-ttu-id="57fd6-186">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="57fd6-186">Here is an example:</span></span>
  
```powershell
Get-MsolUser | Select DisplayName, Department, UsageLocation
```

<span data-ttu-id="57fd6-187">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="57fd6-187">This command instructs PowerShell to:</span></span>
  
- <span data-ttu-id="57fd6-188">Obtenir toutes les informations sur les comptes utilisateur ( **Get-MsolUser** ) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-188">Get all of the information on the user accounts ( **Get-MsolUser** ) and send it to the next command ( **|** ).</span></span>
    
- <span data-ttu-id="57fd6-189">Afficher uniquement le nom du compte d’utilisateur, le service et l’emplacement d’utilisation ( **Sélectionnez DisplayName, Department, UsageLocation** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-189">Display only the user account name, department, and usage location ( **Select DisplayName, Department, UsageLocation** ).</span></span>
    
<span data-ttu-id="57fd6-190">Les informations affichées devraient être semblables à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="57fd6-190">You should see information similar to this:</span></span>
  
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

<span data-ttu-id="57fd6-191">La cmdlet **Select** vous permet de sélectionner et de sélectionner les propriétés que vous souhaitez afficher pour une commande.</span><span class="sxs-lookup"><span data-stu-id="57fd6-191">The **Select** cmdlet lets you pick and choose the properties you want a command to display.</span></span> <span data-ttu-id="57fd6-192">Pour afficher toutes les propriétés des comptes d’utilisateur, utilisez le caractère générique (\*) pour les afficher tous pour un compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="57fd6-192">To see all of the properties for user accounts, use the wildcard character (\*) to display them all for a specific user account.</span></span> <span data-ttu-id="57fd6-193">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="57fd6-193">Here is an example:</span></span>
  
```powershell
Get-MsolUser -UserPrincipalName BelindaN@litwareinc.onmicosoft.com | Select *
```

<span data-ttu-id="57fd6-194">Pour être plus sélectif sur la liste des comptes à afficher, vous pouvez également utiliser la cmdlet **Where** .</span><span class="sxs-lookup"><span data-stu-id="57fd6-194">To be more selective about the list of accounts to display, you can also use the **Where** cmdlet.</span></span> <span data-ttu-id="57fd6-195">Voici un exemple de commande qui affiche uniquement les comptes utilisateur dont l’emplacement d’utilisation n’est pas spécifié :</span><span class="sxs-lookup"><span data-stu-id="57fd6-195">Here is an example command that displays only those user accounts that have an unspecified usage location:</span></span>
  
```powershell
Get-MsolUser | Where {$_.UsageLocation -eq $Null} | Select DisplayName, Department, UsageLocation
```

<span data-ttu-id="57fd6-196">Cette commande demande à PowerShell de :</span><span class="sxs-lookup"><span data-stu-id="57fd6-196">This command instructs PowerShell to:</span></span>
  
- <span data-ttu-id="57fd6-197">Obtenir toutes les informations sur les comptes utilisateur ( **Get-MsolUser** ) et les envoyer à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-197">Get all of the information on the user accounts ( **Get-MsolUser** ) and send it to the next command ( **|** ).</span></span>
    
- <span data-ttu-id="57fd6-198">Recherchez tous les comptes d’utilisateur dont l’emplacement d’utilisation n’est pas spécifié ( **où {$ \_ . UsageLocation-EQ $Null}** ) et envoyer les informations obtenues à la commande suivante ( **|** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-198">Find all of the user accounts that have an unspecified usage location ( **Where {$\_.UsageLocation -eq $Null}** ) and send the resulting information to the next command ( **|** ).</span></span> <span data-ttu-id="57fd6-199">À l’intérieur des accolades, la commande demande à PowerShell de trouver uniquement le jeu de comptes dans lequel la propriété de compte d’utilisateur UsageLocation ( \*\* $ \_ . UsageLocation\*\* ) n’est pas spécifié ( **-EQ $null** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-199">Inside the braces, the command is instructing PowerShell to only find the set of accounts in which the UsageLocation user account property ( **$\_.UsageLocation** ) is not specified ( **-eq $Null** ).</span></span>
    
- <span data-ttu-id="57fd6-200">Afficher uniquement le nom du compte d’utilisateur, le service et l’emplacement d’utilisation ( **Sélectionnez DisplayName, Department, UsageLocation** ).</span><span class="sxs-lookup"><span data-stu-id="57fd6-200">Display only the user account name, department, and usage location ( **Select DisplayName, Department, UsageLocation** ).</span></span>
    
<span data-ttu-id="57fd6-201">Les informations affichées devraient être semblables à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="57fd6-201">You should see information similar to this:</span></span>
  
```powershell
DisplayName              Department                      UsageLocation
-----------              ----------                      -------------
Brian Johnson 
Scott Wallace            Operations
```

<span data-ttu-id="57fd6-202">Si vous utilisez la synchronisation d’annuaires pour créer et gérer vos utilisateurs de Microsoft 365, vous pouvez afficher le compte local à partir duquel un utilisateur Microsoft 365 a été projeté.</span><span class="sxs-lookup"><span data-stu-id="57fd6-202">If you are using directory synchronization to create and manage your Microsoft 365 users, you can display which local account a Microsoft 365 user has been projected from.</span></span> <span data-ttu-id="57fd6-203">Les éléments suivants supposent qu’Azure AD Connect a été configuré pour utiliser l’ancre source par défaut d’ObjectGUID (pour plus d’informations sur la configuration d’une ancre source, reportez-vous à la rubrique [Azure ad Connect : Design concepts](https://docs.microsoft.com/azure/active-directory/hybrid/plan-connect-design-concepts)) et suppose que le module Services de domaine Active Directory pour PowerShell a été installé (voir [outils RSAT](https://www.microsoft.com/en-gb/download/details.aspx?id=45520)) :</span><span class="sxs-lookup"><span data-stu-id="57fd6-203">The following assumes that Azure AD Connect has been configured to use the default source anchor of ObjectGUID (for more on configuring a source anchor, see [Azure AD Connect: Design concepts](https://docs.microsoft.com/azure/active-directory/hybrid/plan-connect-design-concepts)) and assumes that the Active Directory Domain Services module for PowerShell has been installed (see [RSAT tools](https://www.microsoft.com/en-gb/download/details.aspx?id=45520)):</span></span>

```powershell
Get-ADUser ([guid][System.Convert]::FromBase64String((Get-MsolUser -UserPrincipalName <UPN of user account>).ImmutableID)).guid
```

## <a name="see-also"></a><span data-ttu-id="57fd6-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57fd6-204">See also</span></span>

[<span data-ttu-id="57fd6-205">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="57fd6-205">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="57fd6-206">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="57fd6-206">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="57fd6-207">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="57fd6-207">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
