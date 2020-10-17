---
title: Se connecter à tous les services Microsoft 365 dans une seule fenêtre PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/10/2020
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
ms.openlocfilehash: 36b16b491aa97e7329e440e2c1fb01b8a221a2b6
ms.sourcegitcommit: 22755cebfbfa2c4dc3f8b4f54ccb23636a211ee5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2020
ms.locfileid: "48477052"
---
# <a name="connect-to-all-microsoft-365-services-in-a-single-powershell-window"></a><span data-ttu-id="2968f-103">Se connecter à tous les services Microsoft 365 dans une seule fenêtre PowerShell</span><span class="sxs-lookup"><span data-stu-id="2968f-103">Connect to all Microsoft 365 services in a single PowerShell window</span></span>

<span data-ttu-id="2968f-104">Lorsque vous utilisez PowerShell pour gérer Microsoft 365, vous pouvez avoir plusieurs sessions PowerShell différentes ouvertes en même temps dans différentes fenêtres PowerShell correspondant à la gestion des comptes utilisateur, SharePoint Online, Exchange Online, Skype Entreprise Online, Microsoft Teams et le Centre de sécurité &amp; de conformité.</span><span class="sxs-lookup"><span data-stu-id="2968f-104">When you use PowerShell to manage Microsoft 365, it is possible to have multiple PowerShell sessions open at the same time in different PowerShell windows corresponding to managing user accounts, SharePoint Online, Exchange Online, Skype for Business Online, Microsoft Teams, and the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="2968f-105">Cet affichage n’est pas optimal pour gérer Microsoft 365, car vous ne pouvez pas échanger de données entre ces fenêtres pour effectuer une gestion croisée des services.</span><span class="sxs-lookup"><span data-stu-id="2968f-105">This is not optimal for managing Microsoft 365 because you can't exchange data among those windows for cross-service management.</span></span> <span data-ttu-id="2968f-106">Cette rubrique explique comment utiliser une seule instance de PowerShell à partir de laquelle vous pouvez gérer les comptes Microsoft 365, Skype Entreprise Online, Exchange Online, SharePoint Online, Microsoft Teams et le Centre de sécurité &amp; de conformité.</span><span class="sxs-lookup"><span data-stu-id="2968f-106">This topic describes how to use a single instance of PowerShell from which you can manage Microsoft 365 accounts, Skype for Business Online, Exchange Online, SharePoint Online, Microsoft Teams, and the Security &amp; Compliance Center.</span></span>

>[!Note]
><span data-ttu-id="2968f-107">Cet article contient actuellement uniquement les commandes permettant de se connecter au cloud (+GCC) dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="2968f-107">This article currently only contains the commands to connect to the Worldwide (+GCC) cloud.</span></span> <span data-ttu-id="2968f-108">Des notes fournissent des liens vers des articles contenant des informations sur la connexion aux autres clouds Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2968f-108">Notes provide links to articles with information about connecting to the other Microsoft 365 clouds.</span></span>
>

## <a name="before-you-begin"></a><span data-ttu-id="2968f-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="2968f-109">Before you begin</span></span>

<span data-ttu-id="2968f-110">Avant de pouvoir gérer l’ensemble de Microsoft 365 à partir d’une seule instance de PowerShell, tenez compte des conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="2968f-110">Before you can manage all of Microsoft 365 from a single instance of PowerShell, consider the following prerequisites:</span></span>
  
- <span data-ttu-id="2968f-111">Le compte professionnel ou scolaire Microsoft 365 que vous utilisez pour ces procédures doit être membre du rôle d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2968f-111">The Microsoft 365 work or school account that you use for these procedures needs to be a member of a Microsoft 365 admin role.</span></span> <span data-ttu-id="2968f-112">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="2968f-112">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span> <span data-ttu-id="2968f-113">Il s’agit d’une condition requise pour PowerShell pour Microsoft 365, pas nécessairement pour tous les autres services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2968f-113">This a requirement for PowerShell for Microsoft 365, not necessarily for all other Microsoft 365 services.</span></span>
    
- <span data-ttu-id="2968f-114">Vous pouvez utiliser les versions 64 bits de Windows suivantes :</span><span class="sxs-lookup"><span data-stu-id="2968f-114">You can use the following 64-bit versions of Windows:</span></span>
    
  - <span data-ttu-id="2968f-115">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2968f-115">Windows 10</span></span>
    
  - <span data-ttu-id="2968f-116">Windows 8.1 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="2968f-116">Windows 8.1 or Windows 8</span></span>
    
  - <span data-ttu-id="2968f-117">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="2968f-117">Windows Server 2019</span></span>
    
  - <span data-ttu-id="2968f-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2968f-118">Windows Server 2016</span></span>
    
  - <span data-ttu-id="2968f-119">Windows Server 2012 R2 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2968f-119">Windows Server 2012 R2 or Windows Server 2012</span></span>
    
  - <span data-ttu-id="2968f-120">Windows 7 Service Pack 1 (SP1)\*</span><span class="sxs-lookup"><span data-stu-id="2968f-120">Windows 7 Service Pack 1 (SP1)\*</span></span>
    
  - <span data-ttu-id="2968f-121">Windows Server 2008 R2 SP1\*</span><span class="sxs-lookup"><span data-stu-id="2968f-121">Windows Server 2008 R2 SP1\*</span></span>
    
    <span data-ttu-id="2968f-122">\* Vous devez installer Microsoft .NET Framework 4.5.*x* puis Windows Management Framework 3.0 ou Windows Management Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="2968f-122">\* You need to install the Microsoft .NET Framework 4.5.*x* and then either the Windows Management Framework 3.0 or the Windows Management Framework 4.0.</span></span> <span data-ttu-id="2968f-123">Pour plus d’informations, voir [l’installation du .NET Framework](https://go.microsoft.com/fwlink/p/?LinkId=257868) et [Windows Management Framework 3.0](https://go.microsoft.com/fwlink/p/?LinkId=272757) ou [Windows Management Framework 4.0](https://go.microsoft.com/fwlink/p/?LinkId=391344).</span><span class="sxs-lookup"><span data-stu-id="2968f-123">For more information, see [Installing the .NET Framework](https://go.microsoft.com/fwlink/p/?LinkId=257868) and [Windows Management Framework 3.0](https://go.microsoft.com/fwlink/p/?LinkId=272757) or [Windows Management Framework 4.0](https://go.microsoft.com/fwlink/p/?LinkId=391344).</span></span>
    
    <span data-ttu-id="2968f-124">Vous devez utiliser une version 64 bits de Windows en raison de la configuration requise pour le module Skype Entreprise Online et un des modules Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2968f-124">You need to use a 64-bit version of Windows because of the requirements for the Skype for Business Online module and one of the Microsoft 365 modules.</span></span>
    
- <span data-ttu-id="2968f-125">Vous devez installer les modules requis pour Azure Active Directory (Azure AD), Exchange Online, SharePoint Online, Skype Entreprise Online et les équipes :</span><span class="sxs-lookup"><span data-stu-id="2968f-125">You need to install the modules that are required for Azure Active Directory (Azure AD), Exchange Online, SharePoint Online, Skype for Business Online and Teams:</span></span>
    
  - [<span data-ttu-id="2968f-126">Azure Active Directory V2</span><span class="sxs-lookup"><span data-stu-id="2968f-126">Azure Active Directory V2</span></span>](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)
  - [<span data-ttu-id="2968f-127">SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="2968f-127">SharePoint Online Management Shell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=255251)
  - [<span data-ttu-id="2968f-128">Skype Entreprise Online, module Powershell</span><span class="sxs-lookup"><span data-stu-id="2968f-128">Skype for Business Online, PowerShell Module</span></span>](https://docs.microsoft.com/microsoftteams/teams-powershell-overview)
  - [<span data-ttu-id="2968f-129">Echange en ligne PowerShell V2</span><span class="sxs-lookup"><span data-stu-id="2968f-129">Exchange Online PowerShell V2</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2#install-and-maintain-the-exchange-online-powershell-v2-module)
  - [<span data-ttu-id="2968f-130">Aperçu de Teams PowerShell</span><span class="sxs-lookup"><span data-stu-id="2968f-130">Teams PowerShell Overview</span></span>](https://docs.microsoft.com/microsoftteams/teams-powershell-overview)
    
-  <span data-ttu-id="2968f-131">PowerShell doit être configuré afin d’exécuter des scripts signés pour Skype Entreprise Online et le Centre de sécurité &amp; de conformité.</span><span class="sxs-lookup"><span data-stu-id="2968f-131">PowerShell needs to be configured to run signed scripts for Skype for Business Online and the Security &amp; Compliance Center.</span></span> <span data-ttu-id="2968f-132">Pour ce faire, exécutez la commande suivante dans une session PowerShell avec élévation de privilèges (fenêtre PowerShell que vous ouvrez en sélectionnant **Exécuter en tant qu’administrateur**).</span><span class="sxs-lookup"><span data-stu-id="2968f-132">To do this, run the following command in an elevated PowerShell session (a PowerShell window you open by selecting **Run as administrator**).</span></span>
    
   ```powershell
   Set-ExecutionPolicy RemoteSigned
   ```

## <a name="exchange-online-and-security-amp-compliance-center-with-the-exchange-online-powershell-v2-module"></a><span data-ttu-id="2968f-133">Centre de conformité et sécurité &amp;Exchange Online avec le module Exchange Online PowerShell v2</span><span class="sxs-lookup"><span data-stu-id="2968f-133">Exchange Online and Security &amp; Compliance Center with the Exchange Online PowerShell V2 module</span></span>

<span data-ttu-id="2968f-134">Cet article utilise le module Exchange Online PowerShell v2 pour se connecter à Exchange Online et au Centre de conformité &amp; sécurité.</span><span class="sxs-lookup"><span data-stu-id="2968f-134">This article uses the Exchange Online PowerShell V2 module to connect to both Exchange Online and Security &amp; Compliance Center.</span></span> <span data-ttu-id="2968f-135">Toutefois, pour le moment, vous ne pouvez pas vous connecter à Exchange Online et au Centre de sécurité &amp; de conformité **dans la même fenêtre PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="2968f-135">However, at this time you cannot connect to both Exchange Online and the Security &amp; Compliance Center **in the same PowerShell window**.</span></span>

<span data-ttu-id="2968f-136">Par conséquent, vous devez choisir une connexion avec Exchange Online *ou* le Centre de sécurité &amp; de conformité lors de la configuration d’une fenêtre PowerShell pour plusieurs services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2968f-136">Therefore, you must choose a connection with either Exchange Online *or* the Security &amp; Compliance Center when configuring a PowerShell window for multiple Microsoft 365 services.</span></span>

## <a name="connection-steps-when-using-just-a-password"></a><span data-ttu-id="2968f-137">Étapes de connexion lors de l’utilisation d’un mot de passe</span><span class="sxs-lookup"><span data-stu-id="2968f-137">Connection steps when using just a password</span></span>

<span data-ttu-id="2968f-138">Voici les étapes à suivre pour vous connecter à tous les services dans une seule fenêtre PowerShell lorsque vous utilisez uniquement un mot de passe pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="2968f-138">Here are the steps to connect to all the services in a single PowerShell window when you are using just a password for sign-in.</span></span>
  
1. <span data-ttu-id="2968f-139">Ouvrez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2968f-139">Open Windows PowerShell.</span></span>
    
2. <span data-ttu-id="2968f-140">Exécutez la commande suivante et entrez les informations d’identification de votre compte professionnel ou scolaire Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2968f-140">Run this command and enter your Microsoft 365 work or school account credentials.</span></span>
    
   ```powershell
   $credential = Get-Credential
   ```

3. <span data-ttu-id="2968f-141">Exécutez cette commande pour vous connecter à Azure AD à l’aide du module PowerShell Azure Active Directory pour Graph.</span><span class="sxs-lookup"><span data-stu-id="2968f-141">Run this command to connect to Azure AD using the Azure Active Directory PowerShell for Graph module.</span></span>
    
   ```powershell
   Connect-AzureAD -Credential $credential
   ```
  
   <span data-ttu-id="2968f-142">Si vous utilisez le module Microsoft Azure Active Directory pour Windows PowerShell, vous pouvez également exécuter la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="2968f-142">Alternately, if you are using the Microsoft Azure Active Directory Module for Windows PowerShell module, run this command.</span></span>
      
   ```powershell
   Connect-MsolService -Credential $credential
   ```

   > [!Note]
   > <span data-ttu-id="2968f-143">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="2968f-143">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="2968f-144">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2968f-144">To continue using these cmdlets, you must run them from PowerShell.</span></span>

4. <span data-ttu-id="2968f-145">Exécutez ces commandes pour vous connecter à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="2968f-145">Run these commands to connect to SharePoint Online.</span></span> <span data-ttu-id="2968f-146">Spécifiez le nom de l’organisation de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="2968f-146">Specify the organization name for your domain.</span></span> <span data-ttu-id="2968f-147">Par exemple, pour « litwareinc.onmicrosoft.com », la valeur nom de l’organisation est « litwareinc ».</span><span class="sxs-lookup"><span data-stu-id="2968f-147">For example, for "litwareinc.onmicrosoft.com", the  organization name value is "litwareinc".</span></span>
    
   ```powershell
   $orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
   Connect-SPOService -Url https://$orgName-admin.sharepoint.com -Credential $userCredential
   ```

5. <span data-ttu-id="2968f-148">Exécutez ces commandes pour vous connecter à Skype Entreprise online.</span><span class="sxs-lookup"><span data-stu-id="2968f-148">Run these commands to connect to Skype for Business Online.</span></span> <span data-ttu-id="2968f-149">Vous devez normalement voir apparaître un avertissement sur l’augmentation de la valeur `WSMan NetworkDelayms` la première fois que vous connectez. Ignorez-le.</span><span class="sxs-lookup"><span data-stu-id="2968f-149">A warning about increasing the `WSMan NetworkDelayms` value is expected the first time you connect and should be ignored.</span></span>
     
   > [!Note]
   > <span data-ttu-id="2968f-150">Le connecteur Skype Entreprise Online fait actuellement partie du dernier module PowerShell Teams.</span><span class="sxs-lookup"><span data-stu-id="2968f-150">Skype for Business Online Connector is currently part of the latest Teams PowerShell module.</span></span> <span data-ttu-id="2968f-151">Si vous utilisez la version publique la plus récente de PowerShell Teams, vous n’avez pas besoin d’installer le connecteur Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="2968f-151">If you're using the latest Teams PowerShell public release, you don't need to install the Skype for Business Online Connector..</span></span>
   
   ```powershell
   Import-Module MicrosoftTeams
   $sfboSession = New-CsOnlineSession -Credential $credential
   Import-PSSession $sfboSession
   ```

6. <span data-ttu-id="2968f-152">Exécutez cette commande pour vous connecter à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2968f-152">Run this command to connect to Exchange Online.</span></span>
    
   ```powershell
   Import-Module ExchangeOnlineManagement
   Connect-ExchangeOnline -Credential $credential -ShowProgress $true
   ```

   > [!Note]
   > <span data-ttu-id="2968f-153">Pour vous connecter à Exchange Online pour les nuages Microsoft 365 autres que le monde, consulter [Se connecter à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="2968f-153">To connect to Exchange Online for Microsoft 365 clouds other than Worldwide, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

7. <span data-ttu-id="2968f-154">Vous pouvez également exécuter ces commandes pour vous connecter au Centre de sécurité &amp; de conformité.</span><span class="sxs-lookup"><span data-stu-id="2968f-154">Alternately, run these commands to connect to the Security &amp; Compliance Center.</span></span>
    
   ```powershell
   $acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
   Import-Module ExchangeOnlineManagement
   Connect-IPPSSession -UserPrincipalName $acctName
   ```

   > [!Note]
   > <span data-ttu-id="2968f-155">Pour vous connecter au centre de conformité &amp; de sécurité pour les nuages Microsoft 365 autres que le monde, voir [Se connecter à la sécurité &](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell)PowerShell du centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="2968f-155">To connect to the Security &amp; Compliance Center for Microsoft 365 clouds other than Worldwide, see [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

8. <span data-ttu-id="2968f-156">Exécutez ces commandes pour vous connecter au PowerShell Teams.</span><span class="sxs-lookup"><span data-stu-id="2968f-156">Run these commands to connect to Teams PowerShell.</span></span>
    
   ```powershell
   Import-Module MicrosoftTeams
   Connect-MicrosoftTeams -Credential $credential
   ```
  
   > [!Note]
   > <span data-ttu-id="2968f-157">Pour vous connecter aux clouds Microsoft teams autres que le monde, voir [Connect-MicrosoftTeams](https://docs.microsoft.com/powershell/module/teams/connect-microsoftteams).</span><span class="sxs-lookup"><span data-stu-id="2968f-157">To connect to Microsoft Teams clouds other than Worldwide, see [Connect-MicrosoftTeams](https://docs.microsoft.com/powershell/module/teams/connect-microsoftteams).</span></span>


### <a name="azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="2968f-158">Module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="2968f-158">Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="2968f-159">Voici les commandes de tous les services \* à l’exception  du Centre de conformité &amp; de sécurité \* dans un même bloc lors de l’utilisation d’Azure Active Directory PowerShell for Graph module.</span><span class="sxs-lookup"><span data-stu-id="2968f-159">Here are the commands for all of the services *except Security &amp; Compliance Center* in a single block when using the Azure Active Directory PowerShell for Graph module.</span></span> <span data-ttu-id="2968f-160">Spécifiez le nom de votre hôte de domaine, puis exécutez-les tous en même temps.</span><span class="sxs-lookup"><span data-stu-id="2968f-160">Specify the name of your domain host, and then run them all at one time.</span></span>
  
```powershell
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
$credential = Get-Credential
Connect-AzureAD -Credential $credential
Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking
Connect-SPOService -Url https://$orgName-admin.sharepoint.com -credential $credential
Import-Module MicrosoftTeams
$sfboSession = New-CsOnlineSession -Credential $credential
Import-PSSession $sfboSession
Import-Module ExchangeOnlineManagement
Connect-ExchangeOnline -Credential $credential -ShowProgress $true
Import-Module MicrosoftTeams
Connect-MicrosoftTeams -Credential $credential
```

<span data-ttu-id="2968f-161">Voici les commandes de tous les services \* à l’exception de Exchange Online\* dans un même bloc lors de l’utilisation d’Azure Active Directory PowerShell pour module Graph.</span><span class="sxs-lookup"><span data-stu-id="2968f-161">Here are the commands for all of the services *except Exchange Online* in a single block when using the Azure Active Directory PowerShell for Graph module.</span></span> <span data-ttu-id="2968f-162">Spécifiez le nom de votre hôte de domaine et le nom d’utilisateur principal (UPN) pour la connexion, puis exécutez-les tous en même temps.</span><span class="sxs-lookup"><span data-stu-id="2968f-162">Specify the name of your domain host and the UPN for the sign-in, and then run them all at one time.</span></span>
  
```powershell
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$credential = Get-Credential -UserName $acctName
Connect-AzureAD -Credential $credential
Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking
Connect-SPOService -Url https://$orgName-admin.sharepoint.com -credential $credential
Import-Module MicrosoftTeams
$sfboSession = New-CsOnlineSession -Credential $credential
Import-PSSession $sfboSession
Import-Module ExchangeOnlineManagement
Connect-IPPSSession -UserPrincipalName $acctName
Import-Module MicrosoftTeams
Connect-MicrosoftTeams -Credential $credential
```

### <a name="microsoft-azure-active-directory-module-for-windows-powershell-module"></a><span data-ttu-id="2968f-163">Module Microsoft Azure Active Directory pour module Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2968f-163">Microsoft Azure Active Directory Module for Windows PowerShell module</span></span>

<span data-ttu-id="2968f-164">Voici les commandes de tous les services \* à l’exception  du Centre de conformité &amp; de sécurité \* dans un même bloc lors de l’utilisation Module Microsoft Azure Active Directory pour module Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2968f-164">Here are the commands for all of the services *except Security &amp; Compliance Center* in a single block when using the Microsoft Azure Active Directory Module for Windows PowerShell module.</span></span> <span data-ttu-id="2968f-165">Spécifiez le nom de votre hôte de domaine, puis exécutez-les tous en même temps.</span><span class="sxs-lookup"><span data-stu-id="2968f-165">Specify the name of your domain host, and then run them all at one time.</span></span>
  
```powershell
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
$credential = Get-Credential
Connect-MsolService -Credential $credential
Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking
Connect-SPOService -Url https://$orgName-admin.sharepoint.com -credential $credential
Import-Module MicrosoftTeams
$sfboSession = New-CsOnlineSession -Credential $credential
Import-PSSession $sfboSession
Import-Module ExchangeOnlineManagement
Connect-ExchangeOnline -Credential $credential -ShowProgress $true
Import-Module MicrosoftTeams
Connect-MicrosoftTeams -Credential $credential
```

<span data-ttu-id="2968f-166">Voici les commandes de tous les services \* à l’exception de Exchange Online\* dans un même bloc lors de l’utilisation Module Microsoft Azure Active Directory pour module Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2968f-166">Here are the commands for all of the services *except Exchange Online* in a single block when using the Microsoft Azure Active Directory Module for Windows PowerShell module.</span></span> <span data-ttu-id="2968f-167">Spécifiez le nom de votre hôte de domaine et le nom d’utilisateur principal (UPN) pour la connexion, puis exécutez-les tous en même temps.</span><span class="sxs-lookup"><span data-stu-id="2968f-167">Specify the name of your domain host and the UPN for the sign-in, and then run them all at one time.</span></span>
  
```powershell
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$credential = Get-Credential -UserName $acctName
Connect-AzureAD -Credential $credential
Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking
Connect-SPOService -Url https://$orgName-admin.sharepoint.com -credential $credential
Import-Module MicrosoftTeams
$sfboSession = New-CsOnlineSession -Credential $credential
Import-PSSession $sfboSession
Import-Module ExchangeOnlineManagement
Connect-IPPSSession -UserPrincipalName $acctName
Import-Module MicrosoftTeams
Connect-MicrosoftTeams -Credential $credential
```
## <a name="connection-steps-when-using-multi-factor-authentication"></a><span data-ttu-id="2968f-168">Étapes de connexion lors de l’utilisation de l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="2968f-168">Connection steps when using multi-factor authentication</span></span>

### <a name="azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="2968f-169">Module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="2968f-169">Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="2968f-170">Voici toutes les commandes d’un seul bloc pour vous connecter à plusieurs services Microsoft 365 *à l’exception du Centre de conformité &amp;de sécurité* avec l’authentification multifacteur à l’aide d’Azure Active Directory PowerShell pour module Graph.</span><span class="sxs-lookup"><span data-stu-id="2968f-170">Here are all the commands in a single block to connect to multiple Microsoft 365 services *except Security &amp; Compliance Center* with multi-factor authentication using the Azure Active Directory PowerShell for Graph module.</span></span>

```powershell
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
#Azure Active Directory
Connect-AzureAD
#SharePoint Online
Connect-SPOService -Url https://$orgName-admin.sharepoint.com
#Skype for Business Online
Import-Module MicrosoftTeams
$sfboSession = New-CsOnlineSession -UserName $acctName
Import-PSSession $sfboSession
#Exchange Online
Import-Module ExchangeOnlineManagement
Connect-ExchangeOnline -UserPrincipalName $acctName -ShowProgress $true
#Teams
Import-Module MicrosoftTeams
Connect-MicrosoftTeams
```
<span data-ttu-id="2968f-171">Voici toutes les commandes d’un seul bloc pour vous connecter à plusieurs services Microsoft 365 *à l’exception de Exchange Online* avec l’authentification multifacteur à l’aide d’Azure Active Directory PowerShell pour module Graph.</span><span class="sxs-lookup"><span data-stu-id="2968f-171">Here are all the commands in a single block to connect to multiple Microsoft 365 services *except Exchange Online* with multi-factor authentication using the Azure Active Directory PowerShell for Graph module.</span></span>

```powershell
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
#Azure Active Directory
Connect-AzureAD
#SharePoint Online
Connect-SPOService -Url https://$orgName-admin.sharepoint.com
#Skype for Business Online
Import-Module MicrosoftTeams
$sfboSession = New-CsOnlineSession -UserName $acctName
Import-PSSession $sfboSession
#Security & Compliance Center
Import-Module ExchangeOnlineManagement
Connect-IPPSSession -UserPrincipalName $acctName
#Teams
Import-Module MicrosoftTeams
Connect-MicrosoftTeams
```
### <a name="microsoft-azure-active-directory-module-for-windows-powershell-module"></a><span data-ttu-id="2968f-172">Module Microsoft Azure Active Directory pour module Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2968f-172">Microsoft Azure Active Directory Module for Windows PowerShell module</span></span>

<span data-ttu-id="2968f-173">Voici toutes les commandes d’un seul bloc pour vous connecter à plusieurs services Microsoft 365 *à l’exception du Centre de conformité &amp;de sécurité* avec l’authentification multifacteur à l’aide du Module Microsoft Azure Active Directory pour module Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2968f-173">Here are all the commands in a single block to connect to multiple Microsoft 365 services *except Security &amp; Compliance Center* with multi-factor authentication using the Microsoft Azure Active Directory Module for Windows PowerShell module.</span></span>

```powershell
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
#Azure Active Directory
Connect-MsolService
#SharePoint Online
Connect-SPOService -Url https://$orgName-admin.sharepoint.com
#Skype for Business Online
Import-Module MicrosoftTeams
$sfboSession = New-CsOnlineSession -UserName $acctName
Import-PSSession $sfboSession
#Exchange Online
Import-Module ExchangeOnlineManagement
Connect-ExchangeOnline -UserPrincipalName $acctName -ShowProgress $true
#Teams
Import-Module MicrosoftTeams
Connect-MicrosoftTeams
```
<span data-ttu-id="2968f-174">Voici toutes les commandes d’un seul bloc pour vous connecter à plusieurs services Microsoft 365 *à l’exception de Exchange Online* à l’aide de l’authentification multifacteur avec le Module Microsoft Azure Active Directory pour module Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2968f-174">Here are all the commands in a single block to connect to multiple Microsoft 365 services *except Exchange Online* using multi-factor authentication with the Microsoft Azure Active Directory Module for Windows PowerShell module.</span></span>

```powershell
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
#Azure Active Directory
Connect-MsolService
#SharePoint Online
Connect-SPOService -Url https://$orgName-admin.sharepoint.com
#Skype for Business Online
Import-Module MicrosoftTeams
$sfboSession = New-CsOnlineSession -UserName $acctName
Import-PSSession $sfboSession
#Security & Compliance Center
Import-Module ExchangeOnlineManagement
Connect-IPPSSession -UserPrincipalName $acctName
#Teams
Import-Module MicrosoftTeams
Connect-MicrosoftTeams
```

## <a name="close-the-powershell-window"></a><span data-ttu-id="2968f-175">Fermer la fenêtre PowerShell</span><span class="sxs-lookup"><span data-stu-id="2968f-175">Close the PowerShell window</span></span>

<span data-ttu-id="2968f-176">Lorsque vous êtes prêt à fermer la fenêtre PowerShell, exécutez cette commande afin de supprimer les sessions actives de Skype Entreprise Online, de SharePoint Online et de Teams :</span><span class="sxs-lookup"><span data-stu-id="2968f-176">When you are ready to close down the PowerShell window, run this command to remove the active sessions to Skype for Business Online, SharePoint Online, and Teams:</span></span>
  
```powershell
Remove-PSSession $sfboSession ; Disconnect-SPOService ; Disconnect-MicrosoftTeams 
```


## <a name="see-also"></a><span data-ttu-id="2968f-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2968f-177">See also</span></span>

- [<span data-ttu-id="2968f-178">Connexion à Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="2968f-178">Connect to Microsoft 365 with PowerShell</span></span>](connect-to-microsoft-365-powershell.md)
- [<span data-ttu-id="2968f-179">Gérer SharePoint Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="2968f-179">Manage SharePoint Online with PowerShell</span></span>](manage-sharepoint-online-with-microsoft-365-powershell.md)
- [<span data-ttu-id="2968f-180">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="2968f-180">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
