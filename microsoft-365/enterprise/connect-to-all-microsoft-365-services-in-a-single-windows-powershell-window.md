---
title: Se connecter à tous les services Microsoft 365 dans une seule fenêtre PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 02/02/2021
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
ms.openlocfilehash: 18ff8e1789242b4dde3b4b31aaccf2462e4c5d74
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50905127"
---
# <a name="connect-to-all-microsoft-365-services-in-a-single-powershell-window"></a><span data-ttu-id="f4bf3-103">Se connecter à tous les services Microsoft 365 dans une seule fenêtre PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4bf3-103">Connect to all Microsoft 365 services in a single PowerShell window</span></span>

<span data-ttu-id="f4bf3-104">Lorsque vous utilisez PowerShell pour gérer Microsoft 365, plusieurs sessions PowerShell peuvent être ouvertes en même temps.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-104">When you use PowerShell to manage Microsoft 365, you can have multiple PowerShell sessions open at the same time.</span></span> <span data-ttu-id="f4bf3-105">Vous avez peut-être des fenêtres PowerShell différentes pour gérer les comptes d’utilisateurs, SharePoint Online, Exchange Online, Skype Entreprise Online, Microsoft Teams et le centre de Sécurité &amp; de Conformité.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-105">You might have different PowerShell windows to manage user accounts, SharePoint Online, Exchange Online, Skype for Business Online, Microsoft Teams, and the Security &amp; Compliance center.</span></span>
  
<span data-ttu-id="f4bf3-106">Ce scénario n’est pas optimal pour gérer Microsoft 365, car vous ne pouvez pas échanger de données entre ces fenêtres pour effectuer une gestion interservices.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-106">This scenario isn't optimal for managing Microsoft 365, because you can't exchange data among those windows for cross-service management.</span></span> <span data-ttu-id="f4bf3-107">Cet article décrit comment utiliser une instance unique de PowerShell pour gérer les comptes Microsoft 365, Skype Entreprise Online, Exchange Online, SharePoint Online, Microsoft Teams et le Centre de sécurité &amp; de conformité.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-107">This article describes how to use a single instance of PowerShell to manage Microsoft 365 accounts, Skype for Business Online, Exchange Online, SharePoint Online, Microsoft Teams, and the Security &amp; Compliance Center.</span></span>

>[!Note]
><span data-ttu-id="f4bf3-108">Cet article contient actuellement uniquement les commandes permettant de se connecter au cloud (+GCC) dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-108">This article currently only contains the commands to connect to the Worldwide (+GCC) cloud.</span></span> <span data-ttu-id="f4bf3-109">Notes fournit des liens vers des articles pour la connexion aux autres clouds Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-109">Notes provide links to articles about connecting to the other Microsoft 365 clouds.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="f4bf3-110">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f4bf3-110">Before you begin</span></span>

<span data-ttu-id="f4bf3-111">Avant de pouvoir gérer l’ensemble de Microsoft 365 à partir d’une seule instance de PowerShell, tenez compte des conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4bf3-111">Before you can manage all of Microsoft 365 from a single instance of PowerShell, consider the following prerequisites:</span></span>
  
- <span data-ttu-id="f4bf3-112">Le compte professionnel ou scolaire Microsoft 365 que vous utilisez doit être membre du rôle d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-112">The Microsoft 365 work or school account that you use must be a member of a Microsoft 365 admin role.</span></span> <span data-ttu-id="f4bf3-113">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f4bf3-113">For more information, see [About admin roles](../admin/add-users/about-admin-roles.md).</span></span> <span data-ttu-id="f4bf3-114">Cette condition est requise pour PowerShell, pour Microsoft 365, mais pas nécessairement pour tous les autres services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-114">This is a requirement for PowerShell for Microsoft 365, but not necessarily for all other Microsoft 365 services.</span></span>
    
- <span data-ttu-id="f4bf3-115">Vous pouvez utiliser les versions 64 bits de Windows suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4bf3-115">You can use the following 64-bit versions of Windows:</span></span>
    
  - <span data-ttu-id="f4bf3-116">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f4bf3-116">Windows 10</span></span>
    
  - <span data-ttu-id="f4bf3-117">Windows 8.1 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="f4bf3-117">Windows 8.1 or Windows 8</span></span>
    
  - <span data-ttu-id="f4bf3-118">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="f4bf3-118">Windows Server 2019</span></span>
    
  - <span data-ttu-id="f4bf3-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f4bf3-119">Windows Server 2016</span></span>
    
  - <span data-ttu-id="f4bf3-120">Windows Server 2012 R2 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4bf3-120">Windows Server 2012 R2 or Windows Server 2012</span></span>
    
  - <span data-ttu-id="f4bf3-121">Windows 7 Service Pack 1 (SP1)\*</span><span class="sxs-lookup"><span data-stu-id="f4bf3-121">Windows 7 Service Pack 1 (SP1)\*</span></span>
    
  - <span data-ttu-id="f4bf3-122">Windows Server 2008 R2 SP1\*</span><span class="sxs-lookup"><span data-stu-id="f4bf3-122">Windows Server 2008 R2 SP1\*</span></span>
    
    <span data-ttu-id="f4bf3-123">\* Vous devez installer Microsoft .NET Framework 4,5.*x* puis Windows Management Framework 3,0 ou 4,0.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-123">\* You need to install Microsoft .NET Framework 4.5.*x* and then Windows Management Framework 3.0 or 4.0.</span></span> <span data-ttu-id="f4bf3-124">Pour plus d’informations, consultez [Windows Management Framework](/powershell/scripting/windows-powershell/wmf/overview).</span><span class="sxs-lookup"><span data-stu-id="f4bf3-124">For more information, see [Windows Management Framework](/powershell/scripting/windows-powershell/wmf/overview).</span></span>
    
    <span data-ttu-id="f4bf3-125">Vous devez utiliser une version 64 bits de Windows en raison de la configuration requise pour le module Skype Entreprise Online et un des modules Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-125">You need to use a 64-bit version of Windows because of the requirements for the Skype for Business Online module and one of the Microsoft 365 modules.</span></span>
    
- <span data-ttu-id="f4bf3-126">Vous devez installer les modules requis pour Azure Active Directory (Azure AD), Exchange Online, SharePoint Online, Skype Entreprise Online et les équipes :</span><span class="sxs-lookup"><span data-stu-id="f4bf3-126">You need to install the modules that are required for Azure Active Directory (Azure AD), Exchange Online, SharePoint Online, Skype for Business Online and Teams:</span></span>
    
  - [<span data-ttu-id="f4bf3-127">Azure Active Directory V2</span><span class="sxs-lookup"><span data-stu-id="f4bf3-127">Azure Active Directory V2</span></span>](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)
  - [<span data-ttu-id="f4bf3-128">SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="f4bf3-128">SharePoint Online Management Shell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=255251)
  - [<span data-ttu-id="f4bf3-129">Skype Entreprise Online, module Powershell</span><span class="sxs-lookup"><span data-stu-id="f4bf3-129">Skype for Business Online, PowerShell Module</span></span>](/microsoftteams/teams-powershell-overview)
  - [<span data-ttu-id="f4bf3-130">Echange en ligne PowerShell V2</span><span class="sxs-lookup"><span data-stu-id="f4bf3-130">Exchange Online PowerShell V2</span></span>](/powershell/exchange/exchange-online-powershell-v2#install-and-maintain-the-exchange-online-powershell-v2-module)
  - [<span data-ttu-id="f4bf3-131">Aperçu de Teams PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4bf3-131">Teams PowerShell Overview</span></span>](/microsoftteams/teams-powershell-overview)
    
-  <span data-ttu-id="f4bf3-132">PowerShell doit être configuré afin d’exécuter des scripts signés pour Skype Entreprise Online et le Centre de Sécurité &amp; de Conformité.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-132">PowerShell must be configured to run signed scripts for Skype for Business Online and the Security &amp; Compliance Center.</span></span> <span data-ttu-id="f4bf3-133">Exécutez cette commande dans une session PowerShell élevée (une session PowerShell que vous **Exécutez en tant qu’administrateur**).</span><span class="sxs-lookup"><span data-stu-id="f4bf3-133">Run the following command in an elevated PowerShell session (a PowerShell session that you **Run as administrator**).</span></span>
    
   ```powershell
   Set-ExecutionPolicy RemoteSigned
   ```

## <a name="connection-steps-when-using-just-a-password"></a><span data-ttu-id="f4bf3-134">Étapes de connexion lors de l’utilisation d’un mot de passe</span><span class="sxs-lookup"><span data-stu-id="f4bf3-134">Connection steps when using just a password</span></span>

<span data-ttu-id="f4bf3-135">Voici les étapes à suivre pour vous connecter à tous les services dans une fenêtre unique PowerShell lorsque vous utilisez uniquement un mot de passe pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-135">Follow these steps to connect to all the services in a single PowerShell window when you're using just a password for sign-in.</span></span>
  
1. <span data-ttu-id="f4bf3-136">Ouvrez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-136">Open Windows PowerShell.</span></span>
    
2. <span data-ttu-id="f4bf3-137">Exécutez la commande suivante et entrez les informations d’identification de votre compte professionnel ou scolaire Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-137">Run this command and enter your Microsoft 365 work or school account credentials.</span></span>
    
   ```powershell
   $credential = Get-Credential
   ```

3. <span data-ttu-id="f4bf3-138">Exécutez cette commande pour vous connecter à Azure AD à l’aide du module Azure Active Directory PowerShell pour le module Graph.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-138">Run this command to connect to Azure AD by using the Azure Active Directory PowerShell for Graph module.</span></span>
    
   ```powershell
   Connect-AzureAD -Credential $credential
   ```
  
   <span data-ttu-id="f4bf3-139">Ou si vous utilisez le Module Microsoft Azure Active Directory pour le module Windows PowerShell, exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-139">Or if you're using the Microsoft Azure Active Directory Module for Windows PowerShell module, run this command.</span></span>
      
   ```powershell
   Connect-MsolService -Credential $credential
   ```

   > [!Note]
   > <span data-ttu-id="f4bf3-140">PowerShell Core ne prend pas en charge le Module Microsoft Azure Active Directory pour le module Windows PowerShell et les cmdlets ayant *Msol* dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-140">PowerShell Core doesn't support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with *Msol* in their name.</span></span> <span data-ttu-id="f4bf3-141">Exécutez ces cmdlets à partir de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-141">You must run these cmdlets from PowerShell.</span></span>

4. <span data-ttu-id="f4bf3-142">Exécutez ces commandes pour vous connecter à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-142">Run these commands to connect to SharePoint Online.</span></span> <span data-ttu-id="f4bf3-143">Spécifiez le nom de l’organisation de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-143">Specify the organization name for your domain.</span></span> <span data-ttu-id="f4bf3-144">Par exemple, pour « litwareinc\.onmicrosoft.com », la valeur nom de l’organisation est « litwareinc ».</span><span class="sxs-lookup"><span data-stu-id="f4bf3-144">For example, for "litwareinc\.onmicrosoft.com", the  organization name value is "litwareinc".</span></span>
    
   ```powershell
   $orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
   Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking
   Connect-SPOService -Url https://$orgName-admin.sharepoint.com -Credential $Credential
   ```

5. <span data-ttu-id="f4bf3-145">Exécutez ces commandes pour vous connecter à Skype Entreprise online.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-145">Run these commands to connect to Skype for Business Online.</span></span> <span data-ttu-id="f4bf3-146">Un avertissement relatif à la valeur `WSMan NetworkDelayms` apparaît à la première connexion. </span><span class="sxs-lookup"><span data-stu-id="f4bf3-146">A warning about increasing the `WSMan NetworkDelayms` value will appear the first time that you connect.</span></span> <span data-ttu-id="f4bf3-147">Ignorez.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-147">Ignore it.</span></span>
     
   > [!Note]
   > <span data-ttu-id="f4bf3-148">Le connecteur Skype Entreprise Online fait actuellement partie du dernier module PowerShell Teams.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-148">Skype for Business Online Connector is currently part of the latest Teams PowerShell module.</span></span> <span data-ttu-id="f4bf3-149">Si vous utilisez la version publique la plus récente de PowerShell Teams, vous n’avez pas besoin d’installer le connecteur Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-149">If you're using the latest Teams PowerShell public release, you don't need to install the Skype for Business Online Connector.</span></span>
   
   ```powershell
   Import-Module MicrosoftTeams
   $credential = Get-Credential
   Connect-MicrosoftTeams -Credential $credential
   ```

6. <span data-ttu-id="f4bf3-150">Exécutez ces commandes pour vous connecter à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-150">Run these commands to connect to Exchange Online.</span></span>
    
   ```powershell
   Import-Module ExchangeOnlineManagement
   Connect-ExchangeOnline -ShowProgress $true
   ```

   > [!Note]
   > <span data-ttu-id="f4bf3-151">Si vous souhaitez vous connecter à Exchange Online pour les clouds Microsoft 365 autres que Worldwide, veuillez consulter la rubrique [Se connecter à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="f4bf3-151">To connect to Exchange Online for Microsoft 365 clouds other than Worldwide, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

7. <span data-ttu-id="f4bf3-152">Exécutez ces commandes pour vous connecter au centre de conformité &amp; sécurité.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-152">Run these commands to connect to the Security &amp; Compliance Center.</span></span>
    
   ```powershell
   $acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
   Connect-IPPSSession -UserPrincipalName $acctName
   ```

   > [!Note]
   > <span data-ttu-id="f4bf3-153">Pour vous connecter au centre de conformité &amp; de sécurité pour les nuages Microsoft 365 autres que le monde, voir [Se connecter à la sécurité &](/powershell/exchange/connect-to-scc-powershell)PowerShell du centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-153">To connect to the Security &amp; Compliance Center for Microsoft 365 clouds other than Worldwide, see [Connect to Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell).</span></span>

8. <span data-ttu-id="f4bf3-154">Exécutez ces commandes pour vous connecter au PowerShell Teams.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-154">Run these commands to connect to Teams PowerShell.</span></span>
    
   ```powershell
   Import-Module MicrosoftTeams
   $credential = Get-Credential
   Connect-MicrosoftTeams -Credential $credential
   ```
  
   > [!Note]
   > <span data-ttu-id="f4bf3-155">Pour vous connecter aux clouds Microsoft Teams autres *que Worldwide*, consultez [Connect-MicrosoftTeams](/powershell/module/teams/connect-microsoftteams).</span><span class="sxs-lookup"><span data-stu-id="f4bf3-155">To connect to Microsoft Teams clouds other than *Worldwide*, see [Connect-MicrosoftTeams](/powershell/module/teams/connect-microsoftteams).</span></span>
  



### <a name="azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="f4bf3-156">Module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="f4bf3-156">Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="f4bf3-157">Voici les commandes de tous les services dans un bloc unique lors de l’utilisation du module Azure Active Directory PowerShell pour Graph.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-157">Here are the commands for all the services in a single block when you use the Azure Active Directory PowerShell for Graph module.</span></span> <span data-ttu-id="f4bf3-158">Spécifiez le nom de votre hôte de domaine et le nom d’utilisateur principal (UPN) pour la connexion, puis exécutez-les en même temps.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-158">Specify the name of your domain host and the UPN for the sign-in and run them all at the same time.</span></span>
  
```powershell
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$credential = Get-Credential -UserName $acctName -Message "Type the account's password."
#Azure Active Directory
Connect-AzureAD -Credential $credential
#SharePoint Online
Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking
Connect-SPOService -Url https://$orgName-admin.sharepoint.com -credential $credential
#Skype for Business Online
Import-Module MicrosoftTeams
Connect-MicrosoftTeams -Credential $credential
#Exchange Online
Import-Module ExchangeOnlineManagement
Connect-ExchangeOnline -ShowProgress $true
#Security & Compliance Center
Connect-IPPSSession -UserPrincipalName $acctName
#Teams
Import-Module MicrosoftTeams
Connect-MicrosoftTeams -Credential $credential
```

### <a name="microsoft-azure-active-directory-module-for-windows-powershell-module"></a><span data-ttu-id="f4bf3-159">Module Microsoft Azure Active Directory pour module Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4bf3-159">Microsoft Azure Active Directory Module for Windows PowerShell module</span></span>

<span data-ttu-id="f4bf3-160">Voici les commandes de tous les services dans un bloc unique lors de l’utilisation du module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-160">Here are the commands for all the services in a single block when you use the Microsoft Azure Active Directory Module for Windows PowerShell module.</span></span> <span data-ttu-id="f4bf3-161">Spécifiez le nom de votre hôte de domaine et le nom d’utilisateur principal (UPN) pour la connexion, puis exécutez-les en même temps.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-161">Specify the name of your domain host and the UPN for the sign-in and run them all at one time.</span></span>
  
```powershell
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$credential = Get-Credential -UserName $acctName -Message "Type the account's password."
#Azure Active Directory
Connect-MsolService -Credential $credential
#SharePoint Online
Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking
Connect-SPOService -Url https://$orgName-admin.sharepoint.com -credential $credential
#Skype for Business Online
Import-Module MicrosoftTeams
Connect-MicrosoftTeams -Credential $credential
#Exchange Online
Import-Module ExchangeOnlineManagement
Connect-ExchangeOnline -ShowProgress $true
#Security & Compliance Center
Connect-IPPSSession -UserPrincipalName $acctName
#Teams
Import-Module MicrosoftTeams
Connect-MicrosoftTeams -Credential $credential
```

## <a name="connection-steps-when-using-multi-factor-authentication"></a><span data-ttu-id="f4bf3-162">Étapes de connexion lors de l’utilisation de l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="f4bf3-162">Connection steps when using multi-factor authentication</span></span>

### <a name="azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="f4bf3-163">Module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="f4bf3-163">Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="f4bf3-164">Voici toutes les commandes dans un bloc unique qui vous permettent de vous connecter à plusieurs services Microsoft 365lors de l’utilisation de l’authentification multifacteur avec le module Azure Active Directory PowerShell pour Graph.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-164">Here are all the commands in a single block to connect to multiple Microsoft 365 services when you use multi-factor authentication with the Azure Active Directory PowerShell for Graph module.</span></span>

```powershell
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
#Azure Active Directory
Connect-AzureAD
#SharePoint Online
Connect-SPOService -Url https://$orgName-admin.sharepoint.com
#Skype for Business Online
Import-Module MicrosoftTeams
Connect-MicrosoftTeams
#Exchange Online
Import-Module ExchangeOnlineManagement
Connect-ExchangeOnline -UserPrincipalName $acctName -ShowProgress $true
#Security & Compliance Center
Connect-IPPSSession -UserPrincipalName $acctName
#Teams
Import-Module MicrosoftTeams
Connect-MicrosoftTeams
```
### <a name="microsoft-azure-active-directory-module-for-windows-powershell-module"></a><span data-ttu-id="f4bf3-165">Module Microsoft Azure Active Directory pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4bf3-165">Microsoft Azure Active Directory Module for Windows PowerShell module</span></span>

<span data-ttu-id="f4bf3-166">Voici toutes les commandes dans un bloc unique qui vous permettent de vous connecter à plusieurs services Microsoft 365 lors de l’utilisation de l’authentification multifacteur avec le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4bf3-166">Here are all the commands in a single block to connect to multiple Microsoft 365 services when you use multi-factor authentication with the Microsoft Azure Active Directory Module for Windows PowerShell module.</span></span>

```powershell
$acctName="<UPN of the account, such as belindan@litwareinc.onmicrosoft.com>"
$orgName="<for example, litwareinc for litwareinc.onmicrosoft.com>"
#Azure Active Directory
Connect-MsolService
#SharePoint Online
Connect-SPOService -Url https://$orgName-admin.sharepoint.com
#Skype for Business Online
Import-Module MicrosoftTeams
Connect-MicrosoftTeams
#Exchange Online
Import-Module ExchangeOnlineManagement
Connect-ExchangeOnline -UserPrincipalName $acctName -ShowProgress $true
#Security & Compliance Center
Connect-IPPSSession -UserPrincipalName $acctName
#Teams
Import-Module MicrosoftTeams
Connect-MicrosoftTeams
```

## <a name="close-the-powershell-window"></a><span data-ttu-id="f4bf3-167">Fermer la fenêtre PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4bf3-167">Close the PowerShell window</span></span>

<span data-ttu-id="f4bf3-168">Pour fermer la fenêtre PowerShell, exécutez cette commande afin de supprimer les sessions actives de Skype Entreprise Online, SharePoint Online et Teams :</span><span class="sxs-lookup"><span data-stu-id="f4bf3-168">To close down the PowerShell window, run this command to remove the active sessions to Skype for Business Online, SharePoint Online, and Teams:</span></span>
  
```powershell
Remove-PSSession $sfboSession ; Disconnect-SPOService ; Disconnect-MicrosoftTeams 
```

## <a name="see-also"></a><span data-ttu-id="f4bf3-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4bf3-169">See also</span></span>

- [<span data-ttu-id="f4bf3-170">Connexion à Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4bf3-170">Connect to Microsoft 365 with PowerShell</span></span>](connect-to-microsoft-365-powershell.md)
- [<span data-ttu-id="f4bf3-171">Gérer SharePoint Online avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4bf3-171">Manage SharePoint Online with PowerShell</span></span>](manage-sharepoint-online-with-microsoft-365-powershell.md)
- [<span data-ttu-id="f4bf3-172">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4bf3-172">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)