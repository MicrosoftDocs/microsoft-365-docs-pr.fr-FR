---
title: Se connecter à tous les services Microsoft 365 dans une seule fenêtre PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/26/2020
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- LIL_Placement
- Ent_Office_Other
- O365ITProTrain
- httpsfix
ms.assetid: 53d3eef6-4a16-4fb9-903c-816d5d98d7e8
description: 'Résumé : se connecter à tous les services Microsoft 365 dans une seule fenêtre PowerShell.'
ms.openlocfilehash: af676434017cbe7025baa5e8509e6203a5d59674
ms.sourcegitcommit: 555d756c69ac9031d1fb928f2e1f9750beede066
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2020
ms.locfileid: "47307624"
---
# <a name="connect-to-all-microsoft-365-services-in-a-single-powershell-window"></a><span data-ttu-id="95c51-103">Se connecter à tous les services Microsoft 365 dans une seule fenêtre PowerShell</span><span class="sxs-lookup"><span data-stu-id="95c51-103">Connect to all Microsoft 365 services in a single PowerShell window</span></span>

<span data-ttu-id="95c51-104">Lorsque vous utilisez PowerShell pour gérer Microsoft 365, vous pouvez avoir plusieurs sessions PowerShell différentes ouvertes en même temps dans différentes fenêtres PowerShell correspondant à la gestion des comptes utilisateur, SharePoint Online, Exchange Online, Skype Entreprise Online, Microsoft Teams et le Centre de sécurité &amp; de conformité.</span><span class="sxs-lookup"><span data-stu-id="95c51-104">When you use PowerShell to manage Microsoft 365, it is possible to have multiple PowerShell sessions open at the same time in different PowerShell windows corresponding to managing user accounts, SharePoint Online, Exchange Online, Skype for Business Online, Microsoft Teams, and the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="95c51-105">Cet affichage n’est pas optimal pour gérer Microsoft 365, car vous ne pouvez pas échanger de données entre ces fenêtres pour effectuer une gestion croisée des services.</span><span class="sxs-lookup"><span data-stu-id="95c51-105">This is not optimal for managing Microsoft 365 because you can't exchange data among those windows for cross-service management.</span></span> <span data-ttu-id="95c51-106">Cette rubrique explique comment utiliser une seule instance de PowerShell à partir de laquelle vous pouvez gérer les comptes Microsoft 365, Skype Entreprise Online, Exchange Online, SharePoint Online, Microsoft Teams et le Centre de sécurité &amp; de conformité.</span><span class="sxs-lookup"><span data-stu-id="95c51-106">This topic describes how to use a single instance of PowerShell from which you can manage Microsoft 365 accounts, Skype for Business Online, Exchange Online, SharePoint Online, Microsoft Teams, and the Security &amp; Compliance Center.</span></span>

>[!Note]
><span data-ttu-id="95c51-107">Cet article contient actuellement uniquement les commandes permettant de se connecter au cloud (+GCC) dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="95c51-107">This article currently only contains the commands to connect to the Worldwide (+GCC) cloud.</span></span> <span data-ttu-id="95c51-108">Des notes fournissent des liens vers des articles contenant des informations sur la connexion aux autres clouds Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="95c51-108">Notes provide links to articles with information about connecting to the other Microsoft 365 clouds.</span></span>
>

## <a name="before-you-begin"></a><span data-ttu-id="95c51-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="95c51-109">Before you begin</span></span>

<span data-ttu-id="95c51-110">Avant de pouvoir gérer l’ensemble de Microsoft 365 à partir d’une seule instance de PowerShell, tenez compte des conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="95c51-110">Before you can manage all of Microsoft 365 from a single instance of PowerShell, consider the following prerequisites:</span></span>
  
- <span data-ttu-id="95c51-111">Le compte professionnel ou scolaire Microsoft 365 que vous utilisez pour ces procédures doit être membre du rôle d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="95c51-111">The Microsoft 365 work or school account that you use for these procedures needs to be a member of a Microsoft 365 admin role.</span></span> <span data-ttu-id="95c51-112">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="95c51-112">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide).</span></span> <span data-ttu-id="95c51-113">Il s’agit d’une condition requise pour PowerShell pour Microsoft 365, pas nécessairement pour tous les autres services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="95c51-113">This a requirement for PowerShell for Microsoft 365, not necessarily for all other Microsoft 365 services.</span></span>
    
- <span data-ttu-id="95c51-114">Vous pouvez utiliser les versions 64 bits de Windows suivantes :</span><span class="sxs-lookup"><span data-stu-id="95c51-114">You can use the following 64-bit versions of Windows:</span></span>
    
  - <span data-ttu-id="95c51-115">Windows 10</span><span class="sxs-lookup"><span data-stu-id="95c51-115">Windows 10</span></span>
    
  - <span data-ttu-id="95c51-116">Windows 8.1 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="95c51-116">Windows 8.1 or Windows 8</span></span>
    
  - <span data-ttu-id="95c51-117">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="95c51-117">Windows Server 2019</span></span>
    
  - <span data-ttu-id="95c51-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="95c51-118">Windows Server 2016</span></span>
    
  - <span data-ttu-id="95c51-119">Windows Server 2012 R2 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95c51-119">Windows Server 2012 R2 or Windows Server 2012</span></span>
    
  - <span data-ttu-id="95c51-120">Windows 7 Service Pack 1 (SP1)\*</span><span class="sxs-lookup"><span data-stu-id="95c51-120">Windows 7 Service Pack 1 (SP1)\*</span></span>
    
  - <span data-ttu-id="95c51-121">Windows Server 2008 R2 SP1\*</span><span class="sxs-lookup"><span data-stu-id="95c51-121">Windows Server 2008 R2 SP1\*</span></span>
    
    <span data-ttu-id="95c51-122">\* Vous devez installer Microsoft .NET Framework 4.5.*x* puis Windows Management Framework 3.0 ou Windows Management Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="95c51-122">\* You need to install the Microsoft .NET Framework 4.5.*x* and then either the Windows Management Framework 3.0 or the Windows Management Framework 4.0.</span></span> <span data-ttu-id="95c51-123">Pour plus d’informations, voir [l’installation du .NET Framework](https://go.microsoft.com/fwlink/p/?LinkId=257868) et [Windows Management Framework 3.0](https://go.microsoft.com/fwlink/p/?LinkId=272757) ou [Windows Management Framework 4.0](https://go.microsoft.com/fwlink/p/?LinkId=391344).</span><span class="sxs-lookup"><span data-stu-id="95c51-123">For more information, see [Installing the .NET Framework](https://go.microsoft.com/fwlink/p/?LinkId=257868) and [Windows Management Framework 3.0](https://go.microsoft.com/fwlink/p/?LinkId=272757) or [Windows Management Framework 4.0](https://go.microsoft.com/fwlink/p/?LinkId=391344).</span></span>
    
    <span data-ttu-id="95c51-124">Vous devez utiliser une version 64 bits de Windows en raison de la configuration requise pour le module Skype Entreprise Online et un des modules Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="95c51-124">You need to use a 64-bit version of Windows because of the requirements for the Skype for Business Online module and one of the Microsoft 365 modules.</span></span>
    
- <span data-ttu-id="95c51-125">Vous devez installer les modules requis pour Azure Active Directory (Azure AD), Exchange Online, SharePoint Online, Skype Entreprise Online et les équipes :</span><span class="sxs-lookup"><span data-stu-id="95c51-125">You need to install the modules that are required for Azure Active Directory (Azure AD), Exchange Online, SharePoint Online, Skype for Business Online and Teams:</span></span>
    
   - [<span data-ttu-id="95c51-126">Azure Active Directory V2</span><span class="sxs-lookup"><span data-stu-id="95c51-126">Azure Active Directory V2</span></span>](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)
   - [<span data-ttu-id="95c51-127">SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="95c51-127">SharePoint Online Management Shell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=255251)
   - [<span data-ttu-id="95c51-128">Skype Entreprise Online, module Powershell</span><span class="sxs-lookup"><span data-stu-id="95c51-128">Skype for Business Online, PowerShell Module</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=532439)
   - [<span data-ttu-id="95c51-129">Echange en ligne PowerShell V2</span><span class="sxs-lookup"><span data-stu-id="95c51-129">Exchange Online PowerShell V2</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2?view=exchange-ps#install-and-maintain-the-exchange-online-powershell-v2-module)
   - [<span data-ttu-id="95c51-130">Aperçu de Teams PowerShell</span><span class="sxs-lookup"><span data-stu-id="95c51-130">Teams PowerShell Overview</span></span>](https://docs.microsoft.com/microsoftteams/teams-powershell-overview)
    
-  <span data-ttu-id="95c51-131">PowerShell doit être configuré afin d’exécuter des scripts signés pour Skype Entreprise Online et le Centre de sécurité &amp; de conformité.</span><span class="sxs-lookup"><span data-stu-id="95c51-131">PowerShell needs to be configured to run signed scripts for Skype for Business Online and the Security &amp; Compliance Center.</span></span> <span data-ttu-id="95c51-132">Pour ce faire, exécutez la commande suivante dans une session PowerShell avec élévation de privilèges (fenêtre PowerShell que vous ouvrez en sélectionnant **Exécuter en tant qu’administrateur**).</span><span class="sxs-lookup"><span data-stu-id="95c51-132">To do this, run the following command in an elevated PowerShell session (a PowerShell window you open by selecting **Run as administrator**).</span></span>
    
   ```powershell
   Set-ExecutionPolicy RemoteSigned
   ```

## <a name="connection-steps-when-using-just-a-password"></a><span data-ttu-id="95c51-133">Étapes de connexion lors de l’utilisation d’un mot de passe</span><span class="sxs-lookup"><span data-stu-id="95c51-133">Connection steps when using just a password</span></span>

<span data-ttu-id="95c51-134">Voici les étapes à suivre pour vous connecter à tous les services dans une seule fenêtre PowerShell lorsque vous utilisez uniquement un mot de passe pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="95c51-134">Here are the steps to connect to all the services in a single PowerShell window when you are using just a password for sign-in.</span></span>
  
1. <span data-ttu-id="95c51-135">Ouvrez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95c51-135">Open Windows PowerShell.</span></span>
    
2. <span data-ttu-id="95c51-136">Exécutez la commande suivante et entrez les informations d’identification de votre compte professionnel ou scolaire Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="95c51-136">Run this command and enter your Microsoft 365 work or school account credentials.</span></span>
    
   ```powershell
   $credential = Get-Credential
   ```

3. <span data-ttu-id="95c51-137">Exécutez cette commande pour vous connecter à Azure AD à l’aide du module PowerShell Azure Active Directory pour Graph.</span><span class="sxs-lookup"><span data-stu-id="95c51-137">Run this command to connect to Azure AD using the Azure Active Directory PowerShell for Graph module.</span></span>
    
   ```powershell
   Connect-AzureAD -Credential $credential
   ```
  
   <span data-ttu-id="95c51-138">Si vous utilisez le module Microsoft Azure Active Directory pour PowerShell, vous pouvez également exécuter la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="95c51-138">Alternately, if you are using the Microsoft Azure Active Directory Module for PowerShell module, run this command.</span></span>
      
   ```powershell
   Connect-MsolService -Credential $credential
   ```

   > [!Note]
   > <span data-ttu-id="95c51-139">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour PowerShell ni les applets de commande dont le nom inclut **Msol**.</span><span class="sxs-lookup"><span data-stu-id="95c51-139">PowerShell Core does not support the Microsoft Azure Active Directory Module for PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="95c51-140">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95c51-140">To continue using these cmdlets, you must run them from PowerShell.</span></span>

4. <span data-ttu-id="95c51-141">Exécutez ces commandes pour vous connecter à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="95c51-141">Run these commands to connect to SharePoint Online.</span></span> <span data-ttu-id="95c51-142">Spécifiez le nom de l’organisation de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="95c51-142">Specify the organization name for your domain.</span></span> <span data-ttu-id="95c51-143">Par exemple, pour « litwareinc.onmicrosoft.com », la valeur nom de l’organisation est « litwareinc ».</span><span class="sxs-lookup"><span data-stu-id="95c51-143">For example, for "litwareinc.onmicrosoft.com", the  organization name value is "litwareinc".</span></span>
    
   ```powershell
   $orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
   Connect-SPOService -Url https://$orgName-admin.sharepoint.com -Credential $userCredential
   ```

5. <span data-ttu-id="95c51-144">Exécutez ces commandes pour vous connecter à Skype Entreprise online.</span><span class="sxs-lookup"><span data-stu-id="95c51-144">Run these commands to connect to Skype for Business Online.</span></span> <span data-ttu-id="95c51-145">Vous devez normalement voir apparaître un avertissement sur l’augmentation de la valeur `WSMan NetworkDelayms` la première fois que vous connectez. Ignorez-le.</span><span class="sxs-lookup"><span data-stu-id="95c51-145">A warning about increasing the `WSMan NetworkDelayms` value is expected the first time you connect and should be ignored.</span></span>
     
   ```powershell
   Import-Module SkypeOnlineConnector
   $sfboSession = New-CsOnlineSession -Credential $credential
   Import-PSSession $sfboSession
   ```

6. <span data-ttu-id="95c51-146">Exécutez cette commande pour vous connecter à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="95c51-146">Run this command to connect to Exchange Online.</span></span>
    
   ```powershell
   Connect-ExchangeOnline -Credential $credential -ShowProgress $true
   ```

   > [!Note]
   > <span data-ttu-id="95c51-147">Pour vous connecter à Exchange Online pour les nuages Microsoft 365 autres que le monde, utilisez le paramètre de **-ExchangeEnvironmentName**.</span><span class="sxs-lookup"><span data-stu-id="95c51-147">To connect to Exchange Online for Microsoft 365 clouds other than Worldwide, use the **-ExchangeEnvironmentName** parameter.</span></span> <span data-ttu-id="95c51-148">Pour plus d’informations, voir [Connect-ExchangeOnline](https://docs.microsoft.com/powershell/module/exchange/powershell-v2-module/connect-exchangeonline?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="95c51-148">See [Connect-ExchangeOnline](https://docs.microsoft.com/powershell/module/exchange/powershell-v2-module/connect-exchangeonline?view=exchange-ps) for more information.</span></span>

7. <span data-ttu-id="95c51-149">Exécutez ces commandes pour vous connecter au PowerShell Teams.</span><span class="sxs-lookup"><span data-stu-id="95c51-149">Run these commands to connect to Teams PowerShell.</span></span>
    
   ```powershell
   Import-Module MicrosoftTeams
   Connect-MicrosoftTeams -Credential $credential
   ```
  
   > [!Note]
   > <span data-ttu-id="95c51-150">Pour vous connecter aux clouds Microsoft teams autres que le monde, voir [Connect-MicrosoftTeams](https://docs.microsoft.com/powershell/module/teams/connect-microsoftteams?view=teams-ps).</span><span class="sxs-lookup"><span data-stu-id="95c51-150">To connect to Microsoft Teams clouds other than Worldwide, see [Connect-MicrosoftTeams](https://docs.microsoft.com/powershell/module/teams/connect-microsoftteams?view=teams-ps).</span></span>

8. <span data-ttu-id="95c51-151">Exécutez ces commandes pour vous connecter au centre de conformité &amp; sécurité.</span><span class="sxs-lookup"><span data-stu-id="95c51-151">Run these commands to connect to the Security &amp; Compliance Center.</span></span>
    
   ```powershell
   $SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid/ -Credential $credential -Authentication "Basic" -AllowRedirection
   Import-PSSession $SccSession -Prefix cc
   ```

   > [!Note]
   > <span data-ttu-id="95c51-152">Pour vous connecter au centre de conformité &amp; de sécurité pour les nuages Microsoft 365 autres que le monde, voir [Se connecter à la sécurité &](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)PowerShell du centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="95c51-152">To connect to the Security &amp; Compliance Center for Microsoft 365 clouds other than Worldwide, see [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>

<span data-ttu-id="95c51-153">Voici toutes les commandes d’un seul bloc lors de l’utilisation d’Azure Active Directory PowerShell for Graph module.</span><span class="sxs-lookup"><span data-stu-id="95c51-153">Here are all the commands in a single block when using the Azure Active Directory PowerShell for Graph module.</span></span> <span data-ttu-id="95c51-154">Spécifiez le nom de votre hôte de domaine, puis exécutez-les tous en même temps.</span><span class="sxs-lookup"><span data-stu-id="95c51-154">Specify the name of your domain host, and then run them all at one time.</span></span>
  
```powershell
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
$credential = Get-Credential
Connect-AzureAD -Credential $credential
Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking
Connect-SPOService -Url https://$orgName-admin.sharepoint.com -credential $credential
Import-Module SkypeOnlineConnector
$sfboSession = New-CsOnlineSession -Credential $credential
Import-PSSession $sfboSession
$SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid/ -Credential $credential -Authentication "Basic" -AllowRedirection
Import-PSSession $SccSession -Prefix cc
Connect-ExchangeOnline -Credential $credential -ShowProgress $true
Import-Module MicrosoftTeams
Connect-MicrosoftTeams -Credential $credential
```

<span data-ttu-id="95c51-155">Vous pouvez également utiliser les commandes suivantes dans un seul bloc lorsque vous utilisez le module Microsoft Azure Active Directory pour le module PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95c51-155">Alternately, here are all the commands in a single block when using the Microsoft Azure Active Directory Module for PowerShell module.</span></span> <span data-ttu-id="95c51-156">Spécifiez le nom de votre hôte de domaine, puis exécutez-les tous en même temps.</span><span class="sxs-lookup"><span data-stu-id="95c51-156">Specify the name of your domain host, and then run them all at one time.</span></span>
  
```powershell
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
$credential = Get-Credential
Connect-MsolService -Credential $credential
Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking
Connect-SPOService -Url https://$orgName-admin.sharepoint.com -credential $credential
Import-Module SkypeOnlineConnector
$sfboSession = New-CsOnlineSession -Credential $credential
Import-PSSession $sfboSession
$SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid/ -Credential $credential -Authentication "Basic" -AllowRedirection
Import-PSSession $SccSession -Prefix cc
Connect-ExchangeOnline -Credential $credential -ShowProgress $true
Import-Module MicrosoftTeams
Connect-MicrosoftTeams -Credential $credential
```

<span data-ttu-id="95c51-157">Lorsque vous êtes prêt à fermer la fenêtre PowerShell, exécutez cette commande afin de supprimer les sessions actives de Skype Entreprise Online, de SharePoint Online, du Centre de sécurité &amp; de conformité et de Teams :</span><span class="sxs-lookup"><span data-stu-id="95c51-157">When you are ready to close down the PowerShell window, run this command to remove the active sessions to Skype for Business Online, SharePoint Online, the Security &amp; Compliance Center, and Teams:</span></span>
  
```powershell
Remove-PSSession $sfboSession ; Remove-PSSession $SccSession ; Disconnect-SPOService ; Disconnect-MicrosoftTeams 
```

## <a name="connection-steps-when-using-multi-factor-authentication"></a><span data-ttu-id="95c51-158">Étapes de connexion lors de l’utilisation de l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="95c51-158">Connection steps when using multi-factor authentication</span></span>

<span data-ttu-id="95c51-159">Voici toutes les commandes d’un seul bloc pour vous connecter à Azure AD, SharePoint Online, Skype Entreprise, Exchange Online et teams à l’aide de l’authentification multifacteur dans une seule fenêtre à l’aide d’Azure Active Directory PowerShell for Graph module.</span><span class="sxs-lookup"><span data-stu-id="95c51-159">Here are all the commands in a single block to connect to Azure AD, SharePoint Online, Skype for Business, Exchange Online, and Teams using multi-factor authentication in a single window using the Azure Active Directory PowerShell for Graph module.</span></span> <span data-ttu-id="95c51-160">Spécifiez le nom d’utilisateur principal (UPN) d’un compte d’utilisateur et le nom d’hôte de votre domaine, puis exécutez-les tous en même temps.</span><span class="sxs-lookup"><span data-stu-id="95c51-160">Specify the user principal name (UPN) name of a user account and your domain host name, and then run them all at one time.</span></span>

```powershell
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
#Azure Active Directory
Connect-AzureAD
#SharePoint Online
Connect-SPOService -Url https://$orgName-admin.sharepoint.com
#Skype for Business Online
$sfboSession = New-CsOnlineSession -UserName $acctName
Import-PSSession $sfboSession
#Exchange Online
Connect-ExchangeOnline -UserPrincipalName $acctName -ShowProgress $true
#Teams
Import-Module MicrosoftTeams
Connect-MicrosoftTeams
```

<span data-ttu-id="95c51-161">Vous pouvez également utiliser les commandes suivantes lorsque vous utilisez le module Microsoft Azure Active Directory pour le module PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95c51-161">Alternately, here are all the commands when using the Microsoft Azure Active Directory Module for PowerShell module.</span></span>

```powershell
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
#Azure Active Directory
Connect-MsolService
#SharePoint Online
Connect-SPOService -Url https://$orgName-admin.sharepoint.com
#Skype for Business Online
$sfboSession = New-CsOnlineSession -UserName $acctName
Import-PSSession $sfboSession
#Exchange Online
Connect-ExchangeOnline -UserPrincipalName $acctName -ShowProgress $true
#Teams
Import-Module MicrosoftTeams
Connect-MicrosoftTeams
```

<span data-ttu-id="95c51-162">Pour le centre de sécurité &amp; conformité, voir [se connecter à la sécurité & centre de conformité PowerShell à l’aide de l’authentification multifacteur](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell?view=exchange-ps) pour vous connecter à l’aide de l’authentification multifacteur :</span><span class="sxs-lookup"><span data-stu-id="95c51-162">For the Security &amp; Compliance Center, see [Connect to Security & Compliance Center PowerShell using multi-factor authentication](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/mfa-connect-to-scc-powershell?view=exchange-ps) to connect using multi-factor authentication:</span></span>

## <a name="see-also"></a><span data-ttu-id="95c51-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95c51-163">See also</span></span>

- [<span data-ttu-id="95c51-164">Connexion à Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="95c51-164">Connect to Microsoft 365 with PowerShell</span></span>](connect-to-microsoft-365-powershell.md)
- [<span data-ttu-id="95c51-165">Gérer SharePoint Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="95c51-165">Manage SharePoint Online with PowerShell</span></span>](manage-sharepoint-online-with-microsoft-365-powershell.md)
- [<span data-ttu-id="95c51-166">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="95c51-166">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
