---
title: Exemple de script pour les paramètres EOP - plusieurs locataires
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
ms.assetid: e87e84e1-7be0-44bf-a414-d91d60ed8817
ms.custom:
- seo-marvel-apr2020
description: Dans cet article, vous allez apprendre à utiliser PowerShell pour appliquer des paramètres de configuration à vos locataires dans Microsoft Exchange Online Protection (EOP).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: b7d856a7cec3bddc32455ba3afadf0323ddce935
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50166590"
---
# <a name="sample-script-for-applying-eop-settings-to-multiple-tenants"></a><span data-ttu-id="0ad6b-103">Exemple de script pour l’application de paramètres EOP à plusieurs clients</span><span class="sxs-lookup"><span data-stu-id="0ad6b-103">Sample script for applying EOP settings to multiple tenants</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="0ad6b-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="0ad6b-104">**Applies to**</span></span>
-  [<span data-ttu-id="0ad6b-105">Exchange Online Protection autonome</span><span class="sxs-lookup"><span data-stu-id="0ad6b-105">Exchange Online Protection standalone</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)

<span data-ttu-id="0ad6b-106">L’exemple de script suivant permet aux administrateurs Microsoft Exchange Online Protection (EOP) qui gèrent plusieurs locataires (sociétés) d’utiliser Exchange Online PowerShell pour afficher et/ou appliquer des paramètres de configuration à leurs locataires.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-106">The following sample script lets Microsoft Exchange Online Protection (EOP) admins who manage multiple tenants (companies) use Exchange Online PowerShell to view and/or apply configuration settings to their tenants.</span></span>

## <a name="to-run-a-script-or-cmdlet-on-multiple-tenants"></a><span data-ttu-id="0ad6b-107">Pour exécuter un script ou une cmdlet sur plusieurs locataires</span><span class="sxs-lookup"><span data-stu-id="0ad6b-107">To run a script or cmdlet on multiple tenants</span></span>

1. <span data-ttu-id="0ad6b-108">Si ce n’est pas déjà fait, [installez le module Exchange Online V2.](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2#install-and-maintain-the-exo-v2-module)</span><span class="sxs-lookup"><span data-stu-id="0ad6b-108">If you haven't already, [install the Exchange Online V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2#install-and-maintain-the-exo-v2-module).</span></span>

2. <span data-ttu-id="0ad6b-109">À l’aide d’une application de feuille de calcul (par exemple, Excel), créez un fichier .csv avec les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="0ad6b-109">Using an spreadsheet app (for example, Excel), create a .csv file with the following details:</span></span>

   - <span data-ttu-id="0ad6b-110">Colonne UserName : compte que vous utiliserez pour vous connecter (par exemple, `admin@contoso.onmicrosoft.com` ).</span><span class="sxs-lookup"><span data-stu-id="0ad6b-110">UserName column: The account that you'll use to connect (for example, `admin@contoso.onmicrosoft.com`).</span></span>
   - <span data-ttu-id="0ad6b-111">Colonne de cmdlet : cmdlet ou commande à exécuter (par exemple, `Get-AcceptedDomain` ou `Get-AcceptedDomain | FT Name` ).</span><span class="sxs-lookup"><span data-stu-id="0ad6b-111">Cmdlet column: The cmdlet or command to run (for example, `Get-AcceptedDomain` or `Get-AcceptedDomain | FT Name`).</span></span>

   <span data-ttu-id="0ad6b-112">Le fichier se présentera comme ceci :</span><span class="sxs-lookup"><span data-stu-id="0ad6b-112">The file will look like this:</span></span>

   ```text
   UserName,Cmdlet
   admin@contoso.onmicrosoft.com,Get-AcceptedDomain | FT Name
   admin@fabrikam.onmicrosoft.com,Get-AcceptedDomain | FT Name
   ```

3. <span data-ttu-id="0ad6b-113">Enregistrez le fichier .csv à un emplacement facile à trouver (par exemple, c:\scripts\inputfile.csv).</span><span class="sxs-lookup"><span data-stu-id="0ad6b-113">Save the .csv file in a location that's easy to find (for example, c:\scripts\inputfile.csv).</span></span>

4. <span data-ttu-id="0ad6b-114">Copiez le script [RunCmdletOnMultipleTenants.ps1](#runcmdletonmultipletenantsps1) dans le Bloc-notes, puis enregistrez le fichier à un emplacement facile à trouver (par exemple, c:\scripts).</span><span class="sxs-lookup"><span data-stu-id="0ad6b-114">Copy the [RunCmdletOnMultipleTenants.ps1](#runcmdletonmultipletenantsps1) script into Notepad, and then save the file to a location that's easy to find (for example, c:\scripts).</span></span>

5. <span data-ttu-id="0ad6b-115">Exécutez le script à l'aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0ad6b-115">Run the script by using the following syntax:</span></span>

   ```powershell
   & "<file path>\RunCmdletOnMultipleTenants.ps1" "<file path>\inputfile.csv"
   ```

   <span data-ttu-id="0ad6b-116">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="0ad6b-116">Here's an example:</span></span>

   ```powershell
   & "c:\scripts\RunCmdletOnMultipleTenants.ps1" "c:\scripts\inputfile.csv"
   ```

6. <span data-ttu-id="0ad6b-117">Chaque client est connecté et le script est exécuté.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-117">Each tenant will be logged on to, and the script will be run.</span></span>

## <a name="runcmdletonmultipletenantsps1"></a><span data-ttu-id="0ad6b-118">RunCmdletOnMultipleTenants.ps1</span><span class="sxs-lookup"><span data-stu-id="0ad6b-118">RunCmdletOnMultipleTenants.ps1</span></span>

> [!NOTE]
> <span data-ttu-id="0ad6b-119">Vous devrez peut-être modifier `Connect-IPPSSession` la ligne dans le script pour qu’elle corresponde à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-119">You might need to modify the `Connect-IPPSSession` line in the script to match your environment.</span></span> <span data-ttu-id="0ad6b-120">Par exemple, Office 365 Germany requiert une valeur _ConnectionUri_ différente de la valeur actuelle dans un script.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-120">For example, Office 365 Germany requires a different _ConnectionUri_ value than the current value in a script.</span></span> <span data-ttu-id="0ad6b-121">Pour plus d’informations, voir Se connecter [à Exchange Online PowerShell.](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell)</span><span class="sxs-lookup"><span data-stu-id="0ad6b-121">For details, see Connect to [Exchange Online Powershell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

```powershell
# This script runs Windows PowerShell cmdlets on multiple tenants.
#
# Usage: RunCmdletOnMultipleTenants.ps1 inputfile.csv
#
# .csv input file sample:
#
# UserName,Cmdlet
# admin@contoso.onmicrosoft.com,Get-AcceptedDomain | FT Name
# admin@fabrikam.onmicrosoft.com,Get-AcceptedDomain | FT Name

# Get the .csv file name as an argument to this script.
$FilePath = $args[0]

# Import the UserName and Cmdlet values from the .csv file.
$CompanyList = Import-CSV $FilePath

# Load the EXO V2 module
Import-Module ExchangeOnlineManagement

# Loop through each entry from the .csv file.
ForEach ($Company in $CompanyList) {

# Get the current entry's UserName.
$UserName = $Company.UserName

# Get the current entry's Cmdlet.
$Cmdlet = $Company.Cmdlet

# Connect to EOP PowerShell by using the current entry's UserName. Prompt for the password.
Connect-IPPSSession -UserPrincipalName $UserName -ConnectionUri https://ps.protection.outlook.com/powershell-liveid/

# Here's where the script to be run on the tenant goes.
# In this example, the cmdlet in the .csv file runs.
Invoke-Expression $Cmdlet

# End the current PowerShell session.
Disconnect-ExchangeOnline -Confirm:$false
}
```
