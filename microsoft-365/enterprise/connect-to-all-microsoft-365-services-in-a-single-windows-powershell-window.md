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
ms.openlocfilehash: 04be916f745e2bde70554045340fc8ec03f87413
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48754315"
---
# <a name="connect-to-all-microsoft-365-services-in-a-single-powershell-window"></a><span data-ttu-id="8ec3e-103">Se connecter à tous les services Microsoft 365 dans une seule fenêtre PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec3e-103">Connect to all Microsoft 365 services in a single PowerShell window</span></span>

<span data-ttu-id="8ec3e-104">Lorsque vous utilisez PowerShell pour gérer Microsoft 365, plusieurs sessions PowerShell peuvent être ouvertes en même temps.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-104">When you use PowerShell to manage Microsoft 365, you can have multiple PowerShell sessions open at the same time.</span></span> <span data-ttu-id="8ec3e-105">Vous avez peut-être des fenêtres PowerShell différentes pour gérer les comptes d’utilisateurs, SharePoint Online, Exchange Online, Skype Entreprise Online, Microsoft Teams et le centre de Sécurité &amp; de Conformité.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-105">You might have different PowerShell windows to manage user accounts, SharePoint Online, Exchange Online, Skype for Business Online, Microsoft Teams, and the Security &amp; Compliance center.</span></span>
  
<span data-ttu-id="8ec3e-106">Ce scénario n’est pas optimal pour gérer Microsoft 365, car vous ne pouvez pas échanger de données entre ces fenêtres pour effectuer une gestion interservices.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-106">This scenario isn't optimal for managing Microsoft 365, because you can't exchange data among those windows for cross-service management.</span></span> <span data-ttu-id="8ec3e-107">Cet article décrit comment utiliser une instance unique de PowerShell pour gérer les comptes Microsoft 365, Skype Entreprise Online, Exchange Online, SharePoint Online, Microsoft Teams et le Centre de sécurité &amp; de conformité.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-107">This article describes how to use a single instance of PowerShell to manage Microsoft 365 accounts, Skype for Business Online, Exchange Online, SharePoint Online, Microsoft Teams, and the Security &amp; Compliance Center.</span></span>

>[!Note]
><span data-ttu-id="8ec3e-108">Cet article contient actuellement uniquement les commandes permettant de se connecter au cloud (+GCC) dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-108">This article currently only contains the commands to connect to the Worldwide (+GCC) cloud.</span></span> <span data-ttu-id="8ec3e-109">Notes fournit des liens vers des articles pour la connexion aux autres clouds Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-109">Notes provide links to articles about connecting to the other Microsoft 365 clouds.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="8ec3e-110">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8ec3e-110">Before you begin</span></span>

<span data-ttu-id="8ec3e-111">Avant de pouvoir gérer l’ensemble de Microsoft 365 à partir d’une seule instance de PowerShell, tenez compte des conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ec3e-111">Before you can manage all of Microsoft 365 from a single instance of PowerShell, consider the following prerequisites:</span></span>
  
- <span data-ttu-id="8ec3e-112">Le compte professionnel ou scolaire Microsoft 365 que vous utilisez doit être membre du rôle d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-112">The Microsoft 365 work or school account that you use must be a member of a Microsoft 365 admin role.</span></span> <span data-ttu-id="8ec3e-113">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="8ec3e-113">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span> <span data-ttu-id="8ec3e-114">Cette condition est requise pour PowerShell, pour Microsoft 365, mais pas nécessairement pour tous les autres services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-114">This is a requirement for PowerShell for Microsoft 365, but not necessarily for all other Microsoft 365 services.</span></span>
    
- <span data-ttu-id="8ec3e-115">Vous pouvez utiliser les versions 64 bits de Windows suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ec3e-115">You can use the following 64-bit versions of Windows:</span></span>
    
  - <span data-ttu-id="8ec3e-116">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8ec3e-116">Windows 10</span></span>
    
  - <span data-ttu-id="8ec3e-117">Windows 8.1 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="8ec3e-117">Windows 8.1 or Windows 8</span></span>
    
  - <span data-ttu-id="8ec3e-118">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="8ec3e-118">Windows Server 2019</span></span>
    
  - <span data-ttu-id="8ec3e-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8ec3e-119">Windows Server 2016</span></span>
    
  - <span data-ttu-id="8ec3e-120">Windows Server 2012 R2 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ec3e-120">Windows Server 2012 R2 or Windows Server 2012</span></span>
    
  - <span data-ttu-id="8ec3e-121">Windows 7 Service Pack 1 (SP1)\*</span><span class="sxs-lookup"><span data-stu-id="8ec3e-121">Windows 7 Service Pack 1 (SP1)\*</span></span>
    
  - <span data-ttu-id="8ec3e-122">Windows Server 2008 R2 SP1\*</span><span class="sxs-lookup"><span data-stu-id="8ec3e-122">Windows Server 2008 R2 SP1\*</span></span>
    
    <span data-ttu-id="8ec3e-123">\* Vous devez installer Microsoft .NET Framework 4,5. *x* puis Windows Management Framework 3,0 ou 4,0.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-123">\* You need to install Microsoft .NET Framework 4.5. *x* and then Windows Management Framework 3.0 or 4.0.</span></span> <span data-ttu-id="8ec3e-124">Pour plus d’informations, consultez [Windows Management Framework](https://docs.microsoft.com/powershell/scripting/windows-powershell/wmf/overview?view=powershell-7).</span><span class="sxs-lookup"><span data-stu-id="8ec3e-124">For more information, see [Windows Management Framework](https://docs.microsoft.com/powershell/scripting/windows-powershell/wmf/overview?view=powershell-7).</span></span>
    
    <span data-ttu-id="8ec3e-125">Vous devez utiliser une version 64 bits de Windows en raison de la configuration requise pour le module Skype Entreprise Online et un des modules Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-125">You need to use a 64-bit version of Windows because of the requirements for the Skype for Business Online module and one of the Microsoft 365 modules.</span></span>
    
- <span data-ttu-id="8ec3e-126">Vous devez installer les modules requis pour Azure Active Directory (Azure AD), Exchange Online, SharePoint Online, Skype Entreprise Online et les équipes :</span><span class="sxs-lookup"><span data-stu-id="8ec3e-126">You need to install the modules that are required for Azure Active Directory (Azure AD), Exchange Online, SharePoint Online, Skype for Business Online and Teams:</span></span>
    
  - [<span data-ttu-id="8ec3e-127">Azure Active Directory V2</span><span class="sxs-lookup"><span data-stu-id="8ec3e-127">Azure Active Directory V2</span></span>](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)
  - [<span data-ttu-id="8ec3e-128">SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="8ec3e-128">SharePoint Online Management Shell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=255251)
  - [<span data-ttu-id="8ec3e-129">Skype Entreprise Online, module Powershell</span><span class="sxs-lookup"><span data-stu-id="8ec3e-129">Skype for Business Online, PowerShell Module</span></span>](https://docs.microsoft.com/microsoftteams/teams-powershell-overview)
  - [<span data-ttu-id="8ec3e-130">Echange en ligne PowerShell V2</span><span class="sxs-lookup"><span data-stu-id="8ec3e-130">Exchange Online PowerShell V2</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2#install-and-maintain-the-exchange-online-powershell-v2-module)
  - [<span data-ttu-id="8ec3e-131">Aperçu de Teams PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec3e-131">Teams PowerShell Overview</span></span>](https://docs.microsoft.com/microsoftteams/teams-powershell-overview)
    
-  <span data-ttu-id="8ec3e-132">PowerShell doit être configuré afin d’exécuter des scripts signés pour Skype Entreprise Online et le Centre de Sécurité &amp; de Conformité.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-132">PowerShell must be configured to run signed scripts for Skype for Business Online and the Security &amp; Compliance Center.</span></span> <span data-ttu-id="8ec3e-133">Exécutez cette commande dans une session PowerShell élevée (une session PowerShell que vous **Exécutez en tant qu’administrateur** ).</span><span class="sxs-lookup"><span data-stu-id="8ec3e-133">Run the following command in an elevated PowerShell session (a PowerShell session that you **Run as administrator** ).</span></span>
    
   ```powershell
   Set-ExecutionPolicy RemoteSigned
   ```

## <a name="exchange-online-and-security-amp-compliance-center-with-the-exchange-online-powershell-v2-module"></a><span data-ttu-id="8ec3e-134">Centre de conformité et sécurité &amp;Exchange Online avec le module Exchange Online PowerShell v2</span><span class="sxs-lookup"><span data-stu-id="8ec3e-134">Exchange Online and Security &amp; Compliance Center with the Exchange Online PowerShell V2 module</span></span>

<span data-ttu-id="8ec3e-135">Les procédures contenues dans cet article utilisent le module Exchange Online PowerShell v2 pour se connecter à Exchange Online et au Centre de Sécurité &amp; de Conformité.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-135">The procedures in this article use the Exchange Online PowerShell V2 module to connect to both Exchange Online and the Security &amp; Compliance Center.</span></span> <span data-ttu-id="8ec3e-136">Mais pour l’instant, vous ne pouvez pas vous connecter aux deux *dans la même fenêtre PowerShell* .</span><span class="sxs-lookup"><span data-stu-id="8ec3e-136">But currently you can't connect to both *in the same PowerShell window* .</span></span> <span data-ttu-id="8ec3e-137">Vous devez donc choisir de vous connecter à l’un ou l’autre lorsque vous configurez une fenêtre PowerShell pour plusieurs services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-137">So you have to choose to connect to one or the other when you configure a PowerShell window for multiple Microsoft 365 services.</span></span>

## <a name="connection-steps-when-using-just-a-password"></a><span data-ttu-id="8ec3e-138">Étapes de connexion lors de l’utilisation d’un mot de passe</span><span class="sxs-lookup"><span data-stu-id="8ec3e-138">Connection steps when using just a password</span></span>

<span data-ttu-id="8ec3e-139">Voici les étapes à suivre pour vous connecter à tous les services dans une fenêtre unique PowerShell lorsque vous utilisez uniquement un mot de passe pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-139">Follow these steps to connect to all the services in a single PowerShell window when you're using just a password for sign-in.</span></span>
  
1. <span data-ttu-id="8ec3e-140">Ouvrez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-140">Open Windows PowerShell.</span></span>
    
2. <span data-ttu-id="8ec3e-141">Exécutez la commande suivante et entrez les informations d’identification de votre compte professionnel ou scolaire Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-141">Run this command and enter your Microsoft 365 work or school account credentials.</span></span>
    
   ```powershell
   $credential = Get-Credential
   ```

3. <span data-ttu-id="8ec3e-142">Exécutez cette commande pour vous connecter à Azure AD à l’aide du module Azure Active Directory PowerShell pour le module Graph.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-142">Run this command to connect to Azure AD by using the Azure Active Directory PowerShell for Graph module.</span></span>
    
   ```powershell
   Connect-AzureAD -Credential $credential
   ```
  
   <span data-ttu-id="8ec3e-143">Ou si vous utilisez le Module Microsoft Azure Active Directory pour le module Windows PowerShell, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-143">Or if you're using the Microsoft Azure Active Directory Module for Windows PowerShell module, run this command.</span></span>
      
   ```powershell
   Connect-MsolService -Credential $credential
   ```

   > [!Note]
   > <span data-ttu-id="8ec3e-144">PowerShell Core ne prend pas en charge le Module Microsoft Azure Active Directory pour le module Windows PowerShell et les cmdlets ayant *Msol* dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-144">PowerShell Core doesn't support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with *Msol* in their name.</span></span> <span data-ttu-id="8ec3e-145">Exécutez ces cmdlets à partir de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-145">You must run these cmdlets from PowerShell.</span></span>

4. <span data-ttu-id="8ec3e-146">Exécutez ces commandes pour vous connecter à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-146">Run these commands to connect to SharePoint Online.</span></span> <span data-ttu-id="8ec3e-147">Spécifiez le nom de l’organisation de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-147">Specify the organization name for your domain.</span></span> <span data-ttu-id="8ec3e-148">Par exemple, pour « litwareinc\.onmicrosoft.com », la valeur nom de l’organisation est « litwareinc ».</span><span class="sxs-lookup"><span data-stu-id="8ec3e-148">For example, for "litwareinc\.onmicrosoft.com", the  organization name value is "litwareinc".</span></span>
    
   ```powershell
   $orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
   Connect-SPOService -Url https://$orgName-admin.sharepoint.com -Credential $userCredential
   ```

5. <span data-ttu-id="8ec3e-149">Exécutez ces commandes pour vous connecter à Skype Entreprise online.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-149">Run these commands to connect to Skype for Business Online.</span></span> <span data-ttu-id="8ec3e-150">Un avertissement relatif à la valeur `WSMan NetworkDelayms` apparaît à la première connexion. </span><span class="sxs-lookup"><span data-stu-id="8ec3e-150">A warning about increasing the `WSMan NetworkDelayms` value will appear the first time that you connect.</span></span> <span data-ttu-id="8ec3e-151">Ignorez.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-151">Ignore it.</span></span>
     
   > [!Note]
   > <span data-ttu-id="8ec3e-152">Le connecteur Skype Entreprise Online fait actuellement partie du dernier module PowerShell Teams.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-152">Skype for Business Online Connector is currently part of the latest Teams PowerShell module.</span></span> <span data-ttu-id="8ec3e-153">Si vous utilisez la version publique la plus récente de PowerShell Teams, vous n’avez pas besoin d’installer le connecteur Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-153">If you're using the latest Teams PowerShell public release, you don't need to install the Skype for Business Online Connector.</span></span>
   
   ```powershell
   Import-Module MicrosoftTeams
   $sfboSession = New-CsOnlineSession -Credential $credential
   Import-PSSession $sfboSession
   ```

6. <span data-ttu-id="8ec3e-154">Exécutez cette commande pour vous connecter à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-154">Run this command to connect to Exchange Online.</span></span>
    
   ```powershell
   Import-Module ExchangeOnlineManagement
   Connect-ExchangeOnline -Credential $credential -ShowProgress $true
   ```

   > [!Note]
   > <span data-ttu-id="8ec3e-155">Pour vous connecter à Exchange Online pour les nuages Microsoft 365 autres que le monde, consulter [Se connecter à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="8ec3e-155">To connect to Exchange Online for Microsoft 365 clouds other than Worldwide, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

   <span data-ttu-id="8ec3e-156">Vous pouvez également exécuter ces commandes pour vous connecter au Centre de Sécurité &amp; de Conformité.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-156">Alternatively, run these commands to connect to the Security &amp; Compliance Center.</span></span>
    
   ```powershell
   $acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
   Import-Module ExchangeOnlineManagement
   Connect-IPPSSession -UserPrincipalName $acctName
   ```

   > [!Note]
   > <span data-ttu-id="8ec3e-157">Pour vous connecter au centre de conformité &amp; de sécurité pour les nuages Microsoft 365 autres que le monde, voir [Se connecter à la sécurité &](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell)PowerShell du centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-157">To connect to the Security &amp; Compliance Center for Microsoft 365 clouds other than Worldwide, see [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

   <span data-ttu-id="8ec3e-158">Exécutez ces commandes pour vous connecter au PowerShell Teams.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-158">Run these commands to connect to Teams PowerShell.</span></span>
    
   ```powershell
   Import-Module MicrosoftTeams
   Connect-MicrosoftTeams -Credential $credential
   ```
  
   > [!Note]
   > <span data-ttu-id="8ec3e-159">Pour vous connecter aux clouds Microsoft Teams autres *que Worldwide* , consultez [Connect-MicrosoftTeams](https://docs.microsoft.com/powershell/module/teams/connect-microsoftteams).</span><span class="sxs-lookup"><span data-stu-id="8ec3e-159">To connect to Microsoft Teams clouds other than *Worldwide* , see [Connect-MicrosoftTeams](https://docs.microsoft.com/powershell/module/teams/connect-microsoftteams).</span></span>


### <a name="azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="8ec3e-160">Module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="8ec3e-160">Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="8ec3e-161">Voici les commandes de tous les services *à l’exception  du Centre de Sécurité &amp; de Conformité* dans un bloc unique lors de l’utilisation de Azure Active Directory PowerShell pour le module Graph.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-161">Here are the commands for all the services *except Security &amp; Compliance Center* in a single block when you use the Azure Active Directory PowerShell for Graph module.</span></span> <span data-ttu-id="8ec3e-162">Spécifiez le nom de votre hôte de domaine, puis exécutez-les en même temps.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-162">Specify the name of your domain host and run them all at the same time.</span></span>
  
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

<span data-ttu-id="8ec3e-163">Voici les commandes de tous les services *à l’exception de Exchange Online* dans un bloc unique lors de l’utilisation de Azure Active Directory PowerShell pour le module Graph.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-163">Here are the commands for all the services *except Exchange Online* in a single block when you use the Azure Active Directory PowerShell for Graph module.</span></span> <span data-ttu-id="8ec3e-164">Spécifiez le nom de votre hôte de domaine et le nom d’utilisateur principal (UPN) pour la connexion, puis exécutez-les en même temps.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-164">Specify the name of your domain host and the UPN for the sign-in and run them all at the same time.</span></span>
  
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

### <a name="microsoft-azure-active-directory-module-for-windows-powershell-module"></a><span data-ttu-id="8ec3e-165">Module Microsoft Azure Active Directory pour module Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec3e-165">Microsoft Azure Active Directory Module for Windows PowerShell module</span></span>

<span data-ttu-id="8ec3e-166">Voici les commandes de tous les services *à l’exception  du Centre de Sécurité &amp; de Conformité* dans un bloc unique lors de l’utilisation du Module Microsoft Azure Active Directory pour le module Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-166">Here are the commands for all the services *except Security &amp; Compliance Center* in a single block when you use the Microsoft Azure Active Directory Module for Windows PowerShell module.</span></span> <span data-ttu-id="8ec3e-167">Spécifiez le nom de votre hôte de domaine, puis exécutez-les en même temps.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-167">Specify the name of your domain host and run them all at one time.</span></span>
  
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

<span data-ttu-id="8ec3e-168">Voici les commandes de tous les services *à l’exception de Exchange Online* dans un bloc unique lors de l’utilisation du Module Microsoft Azure Active Directory pour le module Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-168">Here are the commands for all the services *except Exchange Online* in a single block when you use the Microsoft Azure Active Directory Module for Windows PowerShell module.</span></span> <span data-ttu-id="8ec3e-169">Spécifiez le nom de votre hôte de domaine et le nom d’utilisateur principal (UPN) pour la connexion, puis exécutez-les en même temps.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-169">Specify the name of your domain host and the UPN for the sign-in and run them all at one time.</span></span>
  
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
## <a name="connection-steps-when-using-multi-factor-authentication"></a><span data-ttu-id="8ec3e-170">Étapes de connexion lors de l’utilisation de l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="8ec3e-170">Connection steps when using multi-factor authentication</span></span>

### <a name="azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="8ec3e-171">Module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="8ec3e-171">Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="8ec3e-172">Voici toutes les commandes dans un bloc unique pour vous connecter à plusieurs services Microsoft 365 *à l’exception du Centre de Sécurité &amp;de conformité* lors de l’utilisation de l’authentification multifacteur à l’aide de Azure Active Directory PowerShell pour le module Graph.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-172">Here are all the commands in a single block to connect to multiple Microsoft 365 services *except Security &amp; Compliance Center* when you use multi-factor authentication with the Azure Active Directory PowerShell for Graph module.</span></span>

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
<span data-ttu-id="8ec3e-173">Voici toutes les commandes dans un bloc unique pour vous connecter à plusieurs services Microsoft 365 *à l’exception de Exchange Online* avec l’authentification multifacteur lors de l’utilisation de Azure Active Directory PowerShell pour le module Graph.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-173">Here are all the commands in a single block to connect to multiple Microsoft 365 services *except Exchange Online* with multi-factor authentication when you use the Azure Active Directory PowerShell for Graph module.</span></span>

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
### <a name="microsoft-azure-active-directory-module-for-windows-powershell-module"></a><span data-ttu-id="8ec3e-174">Module Microsoft Azure Active Directory pour module Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec3e-174">Microsoft Azure Active Directory Module for Windows PowerShell module</span></span>

<span data-ttu-id="8ec3e-175">Voici toutes les commandes dans un bloc unique pour vous connecter à plusieurs services Microsoft 365 *à l’exception du Centre de Sécurité &amp;de conformité* avec l’authentification multifacteur à l’aide du Module Microsoft Azure Active Directory pour le module Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-175">Here are all the commands in a single block to connect to multiple Microsoft 365 services *except Security &amp; Compliance Center* when you use multi-factor authentication with the Microsoft Azure Active Directory Module for Windows PowerShell module.</span></span>

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
<span data-ttu-id="8ec3e-176">Voici toutes les commandes dans un bloc unique pour vous connecter à plusieurs services Microsoft 365 *à l’exception de Exchange Online* lors de l’utilisation de l’authentification multifacteur avec le Module Microsoft Azure Active Directory pour le module Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-176">Here are all the commands in a single block to connect to multiple Microsoft 365 services *except Exchange Online* when you use multi-factor authentication with the Microsoft Azure Active Directory Module for Windows PowerShell module.</span></span>

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

## <a name="close-the-powershell-window"></a><span data-ttu-id="8ec3e-177">Fermer la fenêtre PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec3e-177">Close the PowerShell window</span></span>

<span data-ttu-id="8ec3e-178">Pour fermer la fenêtre PowerShell, exécutez cette commande afin de supprimer les sessions actives de Skype Entreprise Online, SharePoint Online et Teams :</span><span class="sxs-lookup"><span data-stu-id="8ec3e-178">To close down the PowerShell window, run this command to remove the active sessions to Skype for Business Online, SharePoint Online, and Teams:</span></span>
  
```powershell
Remove-PSSession $sfboSession ; Disconnect-SPOService ; Disconnect-MicrosoftTeams 
```

## <a name="see-also"></a><span data-ttu-id="8ec3e-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ec3e-179">See also</span></span>

- [<span data-ttu-id="8ec3e-180">Connexion à Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec3e-180">Connect to Microsoft 365 with PowerShell</span></span>](connect-to-microsoft-365-powershell.md)
- [<span data-ttu-id="8ec3e-181">Gérer SharePoint Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec3e-181">Manage SharePoint Online with PowerShell</span></span>](manage-sharepoint-online-with-microsoft-365-powershell.md)
- [<span data-ttu-id="8ec3e-182">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ec3e-182">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
