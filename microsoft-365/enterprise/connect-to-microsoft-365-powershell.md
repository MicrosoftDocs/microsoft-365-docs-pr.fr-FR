---
title: Connexion à Microsoft 365 à l’aide de PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- LIL_Placement
- O365ITProTrain
- Ent_Office_Other
ms.assetid: 5ebc0e21-b72d-46d8-96fa-00643b18eaec
description: Connectez-vous à votre client Microsoft 365 à l’aide de PowerShell pour Microsoft 365 afin d’effectuer des tâches de Centre d’administration à partir de la ligne de commande.
ms.openlocfilehash: 6b8f98441c7d727984bde8775dea496a9324d50c
ms.sourcegitcommit: 4d26a57c37ff7efbb8d235452c78498b06a59714
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "53053058"
---
# <a name="connect-to-microsoft-365-with-powershell"></a><span data-ttu-id="bbfbb-103">Connexion à Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="bbfbb-103">Connect to Microsoft 365 with PowerShell</span></span>

<span data-ttu-id="bbfbb-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="bbfbb-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="bbfbb-105">PowerShell pour Microsoft 365 vous permet de gérer vos paramètres Microsoft 365 à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-105">PowerShell for Microsoft 365 enables you to manage your Microsoft 365 settings from the command line.</span></span> <span data-ttu-id="bbfbb-106">Pour vous connecter à PowerShell, installez le logiciel requis, puis connectez-vous à votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-106">To connect to PowerShell, just install the required software and then connect to your Microsoft 365 organization.</span></span>

<span data-ttu-id="bbfbb-107">Il existe deux versions du module PowerShell que vous utilisez pour vous connecter à Microsoft 365 et administrer les comptes d’utilisateurs, les groupes et les licences:</span><span class="sxs-lookup"><span data-stu-id="bbfbb-107">There are two versions of the PowerShell module that you can use to connect to Microsoft 365 and administer user accounts, groups, and licenses:</span></span>

- <span data-ttu-id="bbfbb-108">Azure Active Directory PowerShell pour Graph dont les cmdlets incluent *AzureAD* dans leur nom</span><span class="sxs-lookup"><span data-stu-id="bbfbb-108">Azure Active Directory PowerShell for Graph, whose cmdlets include *AzureAD* in their name</span></span>
- <span data-ttu-id="bbfbb-109">Module Microsoft Azure Active Directory pour Windows PowerShell, dont les cmdlets incluent *Msol* dans leur nom</span><span class="sxs-lookup"><span data-stu-id="bbfbb-109">Microsoft Azure Active Directory Module for Windows PowerShell, whose cmdlets include *Msol* in their name</span></span>

<span data-ttu-id="bbfbb-110">À l’heure actuelle, le module Azure Active Directory PowerShell pour Graph ne remplace pas complètement la fonctionnalité du Module Microsoft Azure Active Directory pour Windows PowerShell pour l’administration des utilisateurs, des groupes et des licences.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-110">Currently, the Azure Active Directory PowerShell for Graph module doesn't completely replace the functionality of the Microsoft Azure Active Directory Module for Windows PowerShell module for user, group, and license administration.</span></span> <span data-ttu-id="bbfbb-111">Dans certains cas, vous devez utiliser les deux versions.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-111">In some cases, you need to use both versions.</span></span> <span data-ttu-id="bbfbb-112">Vous pouvez installer en toute sécurité les deux versions sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-112">You can safely install both versions on the same computer.</span></span>

>[!Note]
><span data-ttu-id="bbfbb-113">Vous pouvez également vous connecter à [Azure Cloud Shell](#connect-with-the-azure-cloud-shell) à partir du Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-113">You can also connect with the [Azure Cloud Shell](#connect-with-the-azure-cloud-shell) from the Microsoft 365 admin center.</span></span>
>


## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="bbfbb-114">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="bbfbb-114">What do you need to know before you begin?</span></span>


<span data-ttu-id="bbfbb-115">**Système d’exploitation**</span><span class="sxs-lookup"><span data-stu-id="bbfbb-115">**Operating system**</span></span>

<span data-ttu-id="bbfbb-p103">Vous devez utiliser une version 64 bits de Windows. La prise en charge de la version 32 bits du Module Microsoft Azure Active Directory pour Windows PowerShell a expiré en 2014.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-p103">You must use a 64-bit version of Windows. Support for the 32-bit version of the Microsoft Azure Active Directory Module for Windows PowerShell ended in 2014.</span></span>

<span data-ttu-id="bbfbb-118">Vous pouvez utiliser les versions de Windows suivantes :</span><span class="sxs-lookup"><span data-stu-id="bbfbb-118">You can use the following versions of Windows:</span></span>
    
  - <span data-ttu-id="bbfbb-119">Windows 10, Windows 8.1, Windows 8 ou Windows 7 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="bbfbb-119">Windows 10, Windows 8.1, Windows 8, or Windows 7 Service Pack 1 (SP1)</span></span> 
    
  - <span data-ttu-id="bbfbb-120">Windows Server 2019, Windows Server 2016, Windows Server 2012 R2, Windows Server 2012 ou Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="bbfbb-120">Windows Server 2019, Windows Server 2016, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2 SP1</span></span>

>[!Note]
><span data-ttu-id="bbfbb-121">Pour Windows 8.1, Windows 8, Windows 7 Service Pack 1 (SP1), Windows Server 2012 R2, Windows Server 2012 et Windows Server 2008 R2 SP1, téléchargez et installez [Windows Management Framework 5.1](https://www.microsoft.com/download/details.aspx?id=54616).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-121">For Windows 8.1, Windows 8, Windows 7 Service Pack 1 (SP1), Windows Server 2012 R2, Windows Server 2012, and Windows Server 2008 R2 SP1, download and install the [Windows Management Framework 5.1](https://www.microsoft.com/download/details.aspx?id=54616).</span></span>

<span data-ttu-id="bbfbb-122">**PowerShell**</span><span class="sxs-lookup"><span data-stu-id="bbfbb-122">**PowerShell**</span></span>

- <span data-ttu-id="bbfbb-123">Pour le module Graph de Azure Active Directory PowerShell, vous devez utiliser PowerShell version 5.1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-123">For the Azure Active Directory PowerShell for Graph module, you must use PowerShell version 5.1 or later.</span></span>

- <span data-ttu-id="bbfbb-p104">Vous devez utiliser PowerShell version 5.1 ou ultérieure jusqu’à PowerShell version 6 pour le Module Microsoft Azure Active Directory pour Windows PowerShell. Vous ne pouvez pas utiliser PowerShell version 7.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-p104">For the Microsoft Azure Active Directory Module for Windows PowerShell module, you must use PowerShell version 5.1 or later, up to PowerShell version 6. You can't use PowerShell version 7.</span></span>
       
>[!Note]
><span data-ttu-id="bbfbb-126">Ces procédures sont destinées aux utilisateurs qui sont membres d’un groupe de rôles d'administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-126">These procedures are intended for users who are members of a Microsoft 365 admin role.</span></span> <span data-ttu-id="bbfbb-127">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-127">For more information, see [About admin roles](../admin/add-users/about-admin-roles.md).</span></span>


## <a name="connect-with-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="bbfbb-128">Se connecter avec le module PowerShell Azure Active Directory pour Graph</span><span class="sxs-lookup"><span data-stu-id="bbfbb-128">Connect with the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="bbfbb-129">Le nom des cmdlets du module Azure Active Directory PowerShell pour Graph contient la chaîne de caractères *AzureAD*.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-129">Commands in the Azure Active Directory PowerShell for Graph module have *AzureAD* in their cmdlet name.</span></span> <span data-ttu-id="bbfbb-130">Vous pouvez installer le module [Azure Active Directory PowerShell pour Graph](/powershell/azure/active-directory/install-adv2) ou [Azure PowerShell](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-130">You can install the [Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2) module or [Azure PowerShell](/powershell/azure/install-az-ps).</span></span>

<span data-ttu-id="bbfbb-131">Si vous devez utiliser les nouvelles cmdlets dans le module Microsoft Azure Active Directory PowerShell pour Graph, veuillez suivre cette procédure pour installer le module et vous connecter à votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-131">For procedures that require the new cmdlets in the Azure Active Directory PowerShell for Graph module, follow these steps to install the module and connect to your Microsoft 365 subscription.</span></span>

> [!Note]
> <span data-ttu-id="bbfbb-132">Pour les informations sur la prise en charge de différentes versions de Windows, consultez le [Module Microsoft Azure Active Directory PowerShell pour Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-132">For information about support for different versions of Windows, see [Azure Active Directory PowerShell for Graph module](/powershell/azure/active-directory/install-adv2) .</span></span>

### <a name="step-1-install-the-required-software"></a><span data-ttu-id="bbfbb-133">Étape 1 : installez le logiciel requis</span><span class="sxs-lookup"><span data-stu-id="bbfbb-133">Step 1: Install the required software</span></span>

<span data-ttu-id="bbfbb-134">Ces étapes ne sont requises qu’une fois sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-134">These steps are required only one time on your computer.</span></span> <span data-ttu-id="bbfbb-135">Mais vous devrez peut-être mettre à jour le logiciel régulièrement.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-135">But you'll likely need to update the software periodically.</span></span>
  
1. <span data-ttu-id="bbfbb-136">Ouvrez une fenêtre élevée de l’invite de commandes Windows PowerShell en exécutant Windows PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-136">Open an elevated Windows PowerShell Command Prompt window (run Windows PowerShell as an administrator).</span></span>
    
2. <span data-ttu-id="bbfbb-137">Ensuite, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="bbfbb-137">Run this command:</span></span>
    
    ```powershell
    Install-Module -Name AzureAD
    ```

  <span data-ttu-id="bbfbb-138">Par défaut, la galerie PowerShell (PSGallery) n'est pas configurée comme un référentiel de confiance pour **PowerShellGet** .</span><span class="sxs-lookup"><span data-stu-id="bbfbb-138">By default, the PowerShell Gallery (PSGallery) isn't configured as a trusted repository for **PowerShellGet**.</span></span> <span data-ttu-id="bbfbb-139">La première fois que vous utilisez la PSGallery, vous verrez le message suivant :</span><span class="sxs-lookup"><span data-stu-id="bbfbb-139">The first time you use the PSGallery, you'll see the following message:</span></span>

```console
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="bbfbb-140">Répondez **Oui** ou **Oui à Tout** pour continuer l'installation.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-140">Answer **Yes** or **Yes to All** to continue with the installation.</span></span>


### <a name="step-2-connect-to-azure-ad-for-your-microsoft-365-subscription"></a><span data-ttu-id="bbfbb-141">Étape 2 : connectez-vous à Azure AD avec votre abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bbfbb-141">Step 2: Connect to Azure AD for your Microsoft 365 subscription</span></span>

<span data-ttu-id="bbfbb-p109">Pour vous connecter à Azure AD avec une authentification multifacteur ou les identifiants d’un compte de votre abonnement Microsoft 365, exécutez l’une des commandes suivantes à partir d’une invite de commandes Windows PowerShell. (elle ne nécessite pas d’élévation de privilèges).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-p109">To connect to Azure Active Directory (Azure AD) for your Microsoft 365 subscription with an account name and password or with multi-factor authentication, run one of these commands from a Windows PowerShell command prompt. (It doesn't have to be elevated.)</span></span>

| <span data-ttu-id="bbfbb-144">Office 365 dans le cloud</span><span class="sxs-lookup"><span data-stu-id="bbfbb-144">Office 365 cloud</span></span> | <span data-ttu-id="bbfbb-145">Commande</span><span class="sxs-lookup"><span data-stu-id="bbfbb-145">Command</span></span> |
|:-------|:-----|
| <span data-ttu-id="bbfbb-146">Office 365 dans le monde (+GCC)</span><span class="sxs-lookup"><span data-stu-id="bbfbb-146">Office 365 Worldwide (+GCC)</span></span> | `Connect-AzureAD` |
| <span data-ttu-id="bbfbb-147">Office 365 géré par 21 ViaNet</span><span class="sxs-lookup"><span data-stu-id="bbfbb-147">Office 365 operated by 21 Vianet</span></span> | `Connect-AzureAD -AzureEnvironmentName AzureChinaCloud` |
| <span data-ttu-id="bbfbb-148">Office 365 Allemagne</span><span class="sxs-lookup"><span data-stu-id="bbfbb-148">Office 365 Germany</span></span> | `Connect-AzureAD -AzureEnvironmentName AzureGermanyCloud` |
| <span data-ttu-id="bbfbb-149">Office 365 U.S. Government DoD et Office 365 U.S. Government GCC High</span><span class="sxs-lookup"><span data-stu-id="bbfbb-149">Office 365 U.S. Government DoD and Office 365 U.S. Government GCC High</span></span> | `Connect-AzureAD -AzureEnvironmentName AzureUSGovernment` |
|||

<span data-ttu-id="bbfbb-150">Dans la boîte de dialogue **Connectez-vous à votre compte**, tapez le nom d’utilisateur et le mot de passe de votre compte professionnel ou scolaire Microsoft 365, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-150">In the **Sign into your account** dialog box, type your Microsoft 365 work or school account user name and password, and then select **OK**.</span></span>

<span data-ttu-id="bbfbb-151">Si vous utilisez une authentification multifacteur, suivez les instructions pour fournir des informations d’authentification supplémentaires telles que le code de vérification.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-151">If you're using multi-factor authentication, follow the instructions to provide additional authentication information, such as a verification code.</span></span>

<span data-ttu-id="bbfbb-152">Une fois connecté, vous pouvez utiliser les cmdlets du [module Azure Active Directory PowerShell pour Graph](/powershell/module/azuread).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-152">After you connect, you can use the cmdlets for the [Azure Active Directory PowerShell for Graph module](/powershell/module/azuread).</span></span>

## <a name="connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="bbfbb-153">Se connecter au Module Microsoft Azure Active Directory pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bbfbb-153">Connect with the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

>[!Note]
><span data-ttu-id="bbfbb-154">Les cmdlets du Module Microsoft Azure Active Directory pour Windows PowerShell ont *MSol* dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-154">Cmdlets in the Microsoft Azure Active Directory Module for Windows PowerShell have *Msol* in their name.</span></span>

<span data-ttu-id="bbfbb-155">PowerShell version 7 et ultérieures ne prennent pas en charge le Module Microsoft Azure Active Directory pour Windows PowerShell et les cmdlets incluant *Msol* dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-155">PowerShell version 7 and later don't support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with *Msol* in their name.</span></span> <span data-ttu-id="bbfbb-156">Pour PowerShell version 7 ou ultérieure, vous devez utiliser le module Azure Active Directory PowerShell pour Graph ou Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-156">For PowerShell version 7 and later, you must use the Azure Active Directory PowerShell for Graph module or Azure PowerShell.</span></span>

<span data-ttu-id="bbfbb-157">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour le module Windows PowerShell et les cmdlets incluant *Msol* dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-157">PowerShell Core doesn't support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with *Msol* in their name.</span></span> <span data-ttu-id="bbfbb-158">Exécutez ces cmdlets à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-158">Run these cmdlets from Windows PowerShell.</span></span>
    
### <a name="step-1-install-the-required-software"></a><span data-ttu-id="bbfbb-159">Étape 1 : installez le logiciel requis</span><span class="sxs-lookup"><span data-stu-id="bbfbb-159">Step 1: Install the required software</span></span>

<span data-ttu-id="bbfbb-160">Ces étapes ne sont requises qu’une fois sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-160">These steps are required only one time on your computer.</span></span> <span data-ttu-id="bbfbb-161">Mais vous devrez peut-être mettre à jour le logiciel régulièrement.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-161">But you'll likely need to update the software periodically.</span></span>
  
1.  <span data-ttu-id="bbfbb-162">Si vous n’exécutez pas Windows 10, installez la version 64 bits de l’Assistant de connexion Microsoft Online Services: [Assistant de connexion Microsoft Online Services pour les professionnels des Technologies de l'Information RTW](https://download.microsoft.com/download/7/1/E/71EF1D05-A42C-4A1F-8162-96494B5E615C/msoidcli_32bit.msi).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-162">If you're not running Windows 10, install the 64-bit version of the Microsoft Online Services Sign-in Assistant: [Microsoft Online Services Sign-in Assistant for IT Professionals RTW](https://download.microsoft.com/download/7/1/E/71EF1D05-A42C-4A1F-8162-96494B5E615C/msoidcli_32bit.msi).</span></span>
    
2. <span data-ttu-id="bbfbb-163">Installez le Module Microsoft Azure Active Directory pour Windows PowerShell en suivant ces étapes:</span><span class="sxs-lookup"><span data-stu-id="bbfbb-163">Follow these steps to install the Microsoft Azure Active Directory Module for Windows PowerShell:</span></span>
    
   1. <span data-ttu-id="bbfbb-164">Ouvrez une invite de commandes Windows PowerShell avec élévation de privilèges (exécutez Windows PowerShell en tant qu’administrateur).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-164">Open an elevated Windows PowerShell command prompt (run Windows PowerShell as an administrator).</span></span>
   1.  <span data-ttu-id="bbfbb-165">Exécutez la commande **Install-Module MSOnline**.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-165">Run the **Install-Module MSOnline** command.</span></span>
   1. <span data-ttu-id="bbfbb-166">Si vous êtes invité à installer le fournisseur NuGet, tapez **Y**, puis appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-166">If you're prompted to install the NuGet provider, type **Y** and press Enter.</span></span>
   1. <span data-ttu-id="bbfbb-167">Si vous êtes invité à installer le module à partir de PSGallery, tapez **Y**, puis appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-167">If you're prompted to install the module from PSGallery, type **Y** and press Enter.</span></span>
    
### <a name="step-2-connect-to-azure-ad-for-your-microsoft-365-subscription"></a><span data-ttu-id="bbfbb-168">Étape 2 : connectez-vous à Azure AD avec votre abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bbfbb-168">Step 2: Connect to Azure AD for your Microsoft 365 subscription</span></span>

<span data-ttu-id="bbfbb-p113">Pour vous connecter à Azure AD avec une authentification multifacteur ou les identifiants d’un compte de votre abonnement Microsoft 365, exécutez l’une des commandes suivantes à partir d’une invite de commandes Windows PowerShell. (Elle ne nécessite pas d’élévation de privilèges).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-p113">To connect to Azure AD for your Microsoft 365 subscription with an account name and password or with multi-factor authentication, run one of these commands from a Windows PowerShell command prompt. (It doesn't have to be elevated.)</span></span>

| <span data-ttu-id="bbfbb-171">Office 365 dans le cloud</span><span class="sxs-lookup"><span data-stu-id="bbfbb-171">Office 365 cloud</span></span> | <span data-ttu-id="bbfbb-172">Commande</span><span class="sxs-lookup"><span data-stu-id="bbfbb-172">Command</span></span> |
|:-------|:-----|
| <span data-ttu-id="bbfbb-173">Office 365 dans le monde (+GCC)</span><span class="sxs-lookup"><span data-stu-id="bbfbb-173">Office 365 Worldwide (+GCC)</span></span> | `Connect-MsolService` |
| <span data-ttu-id="bbfbb-174">Office 365 géré par 21 ViaNet</span><span class="sxs-lookup"><span data-stu-id="bbfbb-174">Office 365 operated by 21 Vianet</span></span> | `Connect-MsolService -AzureEnvironment AzureChinaCloud` |
| <span data-ttu-id="bbfbb-175">Office 365 Allemagne</span><span class="sxs-lookup"><span data-stu-id="bbfbb-175">Office 365 Germany</span></span> | `Connect-MsolService -AzureEnvironment AzureGermanyCloud` |
| <span data-ttu-id="bbfbb-176">Office 365 U.S. Government DoD et Office 365 U.S. Government GCC High</span><span class="sxs-lookup"><span data-stu-id="bbfbb-176">Office 365 U.S. Government DoD and Office 365 U.S. Government GCC High</span></span> | `Connect-MsolService -AzureEnvironment USGovernment` |
|||

<span data-ttu-id="bbfbb-177">Dans la boîte de dialogue **Connectez-vous à votre compte**, tapez le nom d’utilisateur et le mot de passe de votre compte professionnel ou scolaire Microsoft 365, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-177">In the **Sign into your account** dialog box, type your Microsoft 365 work or school account user name and password, and then select **OK**.</span></span>

<span data-ttu-id="bbfbb-178">Si vous utilisez une authentification multifacteur, suivez les instructions pour fournir des informations d’authentification supplémentaires telles que le code de vérification.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-178">If you're using multi-factor authentication, follow the instructions to provide additional authentication information, such as a verification code.</span></span>

### <a name="how-do-you-know-it-worked"></a><span data-ttu-id="bbfbb-179">Vérification du bon fonctionnement</span><span class="sxs-lookup"><span data-stu-id="bbfbb-179">How do you know it worked?</span></span>

<span data-ttu-id="bbfbb-180">Si vous ne recevez pas de message d’erreur, alors vous vous êtes connecté.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-180">If you don't get an error message, you connected successfully.</span></span> <span data-ttu-id="bbfbb-181">Pour effectuer un test rapide, exécutez une cmdlet Microsoft 365 telle que, **Get-MsolUser**, et consultez les résultats.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-181">For quick test,  run a Microsoft 365 cmdlet, such as  **Get-MsolUser**, and see the results.</span></span>
  
<span data-ttu-id="bbfbb-182">Si vous recevez un message d’erreur, vérifiez les problèmes suivants:</span><span class="sxs-lookup"><span data-stu-id="bbfbb-182">If you get an error message, check the following issues:</span></span>
  
- <span data-ttu-id="bbfbb-183">**L’inexactitude du mot de passe est un problème courant**.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-183">**A common problem is an incorrect password**.</span></span> <span data-ttu-id="bbfbb-184">Exécutez [L’étape 2](#step-2-connect-to-azure-ad-for-your-microsoft-365-subscription)à nouveau et entrez attentivement le nom et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-184">Run [Step 2](#step-2-connect-to-azure-ad-for-your-microsoft-365-subscription) again, and pay close attention to the user name and password that you enter.</span></span>
    
- <span data-ttu-id="bbfbb-185">**Le Module Microsoft Azure Active Directory pour Windows PowerShell requiert que la fonctionnalité Microsoft .NET Framework 3.5.* x* soit activée sur votre ordinateur**. Il est probable qu’une version plus récente soit installée sur votre ordinateur (par exemple, 4 ou 4.5.* x*),</span><span class="sxs-lookup"><span data-stu-id="bbfbb-185">**The Microsoft Azure Active Directory Module for Windows PowerShell requires that Microsoft .NET Framework 3.5.* x* is enabled on your computer**. It's likely that your computer has a newer version installed (for example, 4 or 4.5.* x*).</span></span> <span data-ttu-id="bbfbb-186">Mais la rétrocompatibilité avec les versions antérieures du .NET Framework peut être activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-186">But backward compatibility with older versions of the .NET Framework can be enabled or disabled.</span></span> <span data-ttu-id="bbfbb-187">Pour plus d’informations, voir les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="bbfbb-187">For more information, see the following articles:</span></span>
    
  - <span data-ttu-id="bbfbb-188">Pour Windows Server 2012 ou Windows Server 2012 R2, consultez [Activer .NET Framework 3.5 en utilisant l’Assistant Ajout de Roles et de Fonctionnalités](/previous-versions/windows/it-pro/windows-8.1-and-8/dn482071(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-188">For Windows Server 2012 or Windows Server 2012 R2, see [Enable .NET Framework 3.5 by using the Add Roles and Features Wizard](/previous-versions/windows/it-pro/windows-8.1-and-8/dn482071(v=win.10)).</span></span>
    
  - <span data-ttu-id="bbfbb-189">For Windows 7 or Windows Server 2008 R2, consultez [Vous ne pouvez pas ouvrir le Module Azure Active Directory pour Windows PowerShell](/troubleshoot/azure/active-directory/cant-open-aad-module-powershell).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-189">For Windows 7 or Windows Server 2008 R2, see [You can't open the Azure Active Directory Module for Windows PowerShell](/troubleshoot/azure/active-directory/cant-open-aad-module-powershell).</span></span>

  - <span data-ttu-id="bbfbb-190">Pour Windows 10, Windows 8.1 et Windows 8, consultez [Installer .NET Framework 3.5 sur Windows 10, Windows 8.1 et Windows 8](/dotnet/framework/install/dotnet-35-windows-10).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-190">For Windows 10, Windows 8.1, and Windows 8, see [Install the .NET Framework 3.5 on Windows 10, Windows 8.1, and Windows 8](/dotnet/framework/install/dotnet-35-windows-10).</span></span>

  
- <span data-ttu-id="bbfbb-191">**Votre version du Module Microsoft Azure Active Directory pour Windows PowerShell est peut-être obsolète.**</span><span class="sxs-lookup"><span data-stu-id="bbfbb-191">**Your version of the Microsoft Azure Active Directory Module for Windows PowerShell might be out of date.**</span></span> <span data-ttu-id="bbfbb-192">Pour vérifier cela, exécutez la commande suivante dans PowerShell pour Microsoft 365 ou le Module Microsoft Azure Active Directory pour Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="bbfbb-192">To check, run the following command in PowerShell for Microsoft 365 or the Microsoft Azure Active Directory Module for Windows PowerShell:</span></span>
    
  ```powershell
  (Get-Item C:\Windows\System32\WindowsPowerShell\v1.0\Modules\MSOnline\Microsoft.Online.Administration.Automation.PSModule.dll).VersionInfo.FileVersion
  ```

    <span data-ttu-id="bbfbb-193">Si le numéro de version renvoyé est inférieur à la valeur *1.0.8070.2*, désinstallez le Module Microsoft Azure Active Directory pour Windows PowerShell, puis installez-le à partir de [l’Etape 1](#step-1-install-the-required-software) ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-193">If the version number returned is lower than *1.0.8070.2*, uninstall the Microsoft Azure Active Directory Module for Windows PowerShell and install from [Step 1](#step-1-install-the-required-software), above.</span></span>

- <span data-ttu-id="bbfbb-194">**Si un message d’erreur de connexion s’affiche**, consultez [Erreur « Connect-MsolService: Une exception de type a été levée »](/office365/troubleshoot/active-directory/connect-msoservice-throw-exception).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-194">**If you get a connection error message**, see ["Connect-MsolService: Exception of type was thrown" error](/office365/troubleshoot/active-directory/connect-msoservice-throw-exception).</span></span>
    
- <span data-ttu-id="bbfbb-195">**Si vous recevez un message d’erreur «Get-Item : Chemin introuvable»**, exécutez cette commande:</span><span class="sxs-lookup"><span data-stu-id="bbfbb-195">**If you get a "Get-Item: Cannot find path" error message**, run this command:</span></span>


   ```powershell
     (dir "C:\Program Files\WindowsPowerShell\Modules\MSOnline").Name
   ```

## <a name="connect-with-the-azure-cloud-shell"></a><span data-ttu-id="bbfbb-196">Se connecter à Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="bbfbb-196">Connect with the Azure Cloud Shell</span></span>

<span data-ttu-id="bbfbb-197">Pour vous connecter à Azure Cloud Shell et l’utiliser à partir du Centre d’administration Microsoft 365, sélectionnez l’icône de fenêtre PowerShell dans le coin supérieur droit de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-197">To connect with and use the Azure Cloud Shell from the Microsoft 365 admin center, select the PowerShell window icon from the upper-right corner of the task bar.</span></span> <span data-ttu-id="bbfbb-198">Dans le volet **Bienvenue dans Azure Cloud Shell** , sélectionnez **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-198">In the **Welcome to Azure Cloud Shell** pane, select **PowerShell**.</span></span>

<span data-ttu-id="bbfbb-199">Vous aurez besoin d’un abonnement Azure actif pour votre organisation lié à votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-199">You will need an active Azure subscription for your organization that is tied to your Microsoft 365 subscription.</span></span> <span data-ttu-id="bbfbb-200">Si vous n’en avez pas encore, vous pouvez en créer un.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-200">If you don't already have one, you can create one.</span></span> <span data-ttu-id="bbfbb-201">Une fois que vous disposez d’un abonnement Azure, une fenêtre PowerShell s’ouvre à partir de laquelle vous pouvez exécuter des commandes et des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bbfbb-201">Once you have an Azure subscription, a PowerShell window opens from which you can run PowerShell commands and scripts.</span></span>

<span data-ttu-id="bbfbb-202">Pour plus d’informations, consultez [Azure Cloud Shell](/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="bbfbb-202">For more information, see [Azure Cloud Shell](/azure/cloud-shell/overview).</span></span>

## <a name="see-also"></a><span data-ttu-id="bbfbb-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbfbb-203">See also</span></span>

- [<span data-ttu-id="bbfbb-204">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="bbfbb-204">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
- [<span data-ttu-id="bbfbb-205">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bbfbb-205">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
- [<span data-ttu-id="bbfbb-206">Connexion à tous les services Microsoft 365 dans une seule fenêtre Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bbfbb-206">Connect to all Microsoft 365 services in a single Windows PowerShell window</span></span>](connect-to-all-microsoft-365-services-in-a-single-windows-powershell-window.md)
