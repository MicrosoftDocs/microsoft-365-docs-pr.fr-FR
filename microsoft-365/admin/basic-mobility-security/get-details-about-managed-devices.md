---
title: Obtenir des détails sur les appareils gérés par la mobilité et la sécurité de base
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
- AdminSurgePortfolio
search.appverid:
- MET150
description: Utilisez Windows PowerShell pour obtenir des détails sur les périphériques de mobilité et de sécurité de base dans votre organisation.
ms.openlocfilehash: 7cb2369c9a31210f26db12b0453e7a4228e1cccc
ms.sourcegitcommit: 3b9fab82d63aea41d5f544938868c5d2cbf52d7a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "52782440"
---
# <a name="get-details-about-basic-mobility-and-security-managed-devices"></a><span data-ttu-id="a28cf-103">Obtenir des détails sur les appareils gérés par la mobilité et la sécurité de base</span><span class="sxs-lookup"><span data-stu-id="a28cf-103">Get details about Basic Mobility and Security managed devices</span></span>

<span data-ttu-id="a28cf-104">Cet article vous montre comment utiliser Windows PowerShell pour obtenir des détails sur les appareils de votre organisation que vous avez mis en place pour basic Mobility and Security.</span><span class="sxs-lookup"><span data-stu-id="a28cf-104">This article shows you how to use Windows PowerShell to get details about the devices in your organization that you set up for Basic Mobility and Security.</span></span>

<span data-ttu-id="a28cf-105">Voici une répartition des détails de l’appareil à votre disposition.</span><span class="sxs-lookup"><span data-stu-id="a28cf-105">Here's a breakdown for the device details available to you.</span></span>

|<span data-ttu-id="a28cf-106">**Detail**</span><span class="sxs-lookup"><span data-stu-id="a28cf-106">**Detail**</span></span>|<span data-ttu-id="a28cf-107">**Ce qu’il faut rechercher dans PowerShell**</span><span class="sxs-lookup"><span data-stu-id="a28cf-107">**What to look for in PowerShell**</span></span>|
|:----------------|:------------------------------------------------------------------------------|
|<span data-ttu-id="a28cf-108">L’appareil est inscrit à Basic Mobility and Security.</span><span class="sxs-lookup"><span data-stu-id="a28cf-108">Device is enrolled in Basic Mobility and Security.</span></span> <span data-ttu-id="a28cf-109">Pour plus d’informations, voir [Inscrire votre appareil mobile à l’aide de Basic Mobility and Security](enroll-your-mobile-device.md)</span><span class="sxs-lookup"><span data-stu-id="a28cf-109">For more info, see [Enroll your mobile device using Basic Mobility and Security](enroll-your-mobile-device.md)</span></span>|<span data-ttu-id="a28cf-110">La valeur du *paramètre isManaged*   est :</span><span class="sxs-lookup"><span data-stu-id="a28cf-110">The value of the *isManaged* parameter is:</span></span><br/><span data-ttu-id="a28cf-111">**True**= l’appareil est inscrit.</span><span class="sxs-lookup"><span data-stu-id="a28cf-111">**True**= device is enrolled.</span></span><br/><span data-ttu-id="a28cf-112">**False**= l’appareil n’est pas inscrit.</span><span class="sxs-lookup"><span data-stu-id="a28cf-112">**False**= device is not enrolled.</span></span> |
|<span data-ttu-id="a28cf-113">L’appareil est conforme aux stratégies de sécurité de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="a28cf-113">Device is compliant with your device security policies.</span></span> <span data-ttu-id="a28cf-114">Pour plus d’informations, voir [Créer des stratégies de sécurité d’appareil](create-device-security-policies.md)</span><span class="sxs-lookup"><span data-stu-id="a28cf-114">For more info, see [Create device security policies](create-device-security-policies.md)</span></span>|<span data-ttu-id="a28cf-115">La valeur du *paramètre isCompliant*   est :</span><span class="sxs-lookup"><span data-stu-id="a28cf-115">The value of the *isCompliant* parameter is:</span></span><br/><span data-ttu-id="a28cf-116">**True**   = l’appareil est conforme aux stratégies.</span><span class="sxs-lookup"><span data-stu-id="a28cf-116">**True** = device is compliant with policies.</span></span><br/><span data-ttu-id="a28cf-117">**False**   = l’appareil n’est pas conforme aux stratégies.</span><span class="sxs-lookup"><span data-stu-id="a28cf-117">**False** = device is not compliant with policies.</span></span>|

:::image type="content" source="../../media/basic-mobility-security/bms-7-powershell-parameters.png" alt-text="Paramètres PowerShell de mobilité et de sécurité de base":::

>[!NOTE]
><span data-ttu-id="a28cf-119">Les commandes et les scripts de cet article retournent également des détails sur les appareils gérés [par Microsoft Intune](https://www.microsoft.com/cloud-platform/microsoft-intune).</span><span class="sxs-lookup"><span data-stu-id="a28cf-119">The commands and scripts in this article also return details about any devices managed by [Microsoft Intune](https://www.microsoft.com/cloud-platform/microsoft-intune).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="a28cf-120">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a28cf-120">Before you begin</span></span>

<span data-ttu-id="a28cf-121">Vous devez configurer plusieurs éléments pour exécuter les commandes et les scripts décrits dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a28cf-121">There are a few things you need to set up to run the commands and scripts described in this article.</span></span>

### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="a28cf-122">Étape 1 : Télécharger et installer le module Azure Active Directory pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a28cf-122">Step 1: Download and install the Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="a28cf-123">Pour plus d’informations sur ces [étapes, voir Connecter à Microsoft 365 avec PowerShell.](/office365/enterprise/powershell/connect-to-office-365-powershell)</span><span class="sxs-lookup"><span data-stu-id="a28cf-123">For more info on these steps, see [Connect to Microsoft 365 with PowerShell](/office365/enterprise/powershell/connect-to-office-365-powershell).</span></span>

1. <span data-ttu-id="a28cf-124">Go to [Microsoft Online Services Sign-In Assistant for IT Professionals RTWl](https://download.microsoft.com/download/7/1/E/71EF1D05-A42C-4A1F-8162-96494B5E615C/msoidcli_32bit.msi)and select Download for Microsoft Online Services    **Sign-in Assistant**.</span><span class="sxs-lookup"><span data-stu-id="a28cf-124">Go to [Microsoft Online Services Sign-In Assistant for IT Professionals RTWl](https://download.microsoft.com/download/7/1/E/71EF1D05-A42C-4A1F-8162-96494B5E615C/msoidcli_32bit.msi) and select  **Download for Microsoft Online Services Sign-in Assistant**.</span></span>

2. <span data-ttu-id="a28cf-125">Téléchargez et installez le Module Microsoft Azure Active Directory pour Windows PowerShell en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="a28cf-125">Install the Microsoft Azure Active Directory Module for Windows PowerShell with these steps:</span></span>

    1. <span data-ttu-id="a28cf-126">Ouvrez une invite de commandes PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="a28cf-126">Open an administrator-level PowerShell command prompt.</span></span>  

    2. <span data-ttu-id="a28cf-127">Exécutez la commande Install-Module MSOnline.</span><span class="sxs-lookup"><span data-stu-id="a28cf-127">Run the Install-Module MSOnline command.</span></span>

    3. <span data-ttu-id="a28cf-128">Si vous êtes invité à installer le fournisseur NuGet, tapez O, puis appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="a28cf-128">If prompted to install the NuGet provider, type Y and press ENTER.</span></span>

    4. <span data-ttu-id="a28cf-129">Si vous êtes invité à installer le module à partir de PSGallery, tapez O, puis appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="a28cf-129">If prompted to install the module from PSGallery, type Y and press ENTER.</span></span>

    5. <span data-ttu-id="a28cf-130">Après l’installation, fermez la fenêtre de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a28cf-130">After installation, close the PowerShell command window.</span></span>

### <a name="step-2-connect-to-your-microsoft-365-subscription"></a><span data-ttu-id="a28cf-131">Étape 2 : Connecter à votre abonnement Microsoft 365 abonnement</span><span class="sxs-lookup"><span data-stu-id="a28cf-131">Step 2: Connect to your Microsoft 365 subscription</span></span>

1. <span data-ttu-id="a28cf-132">Dans le Windows Azure Active Directory module de Windows PowerShell, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="a28cf-132">In the Windows Azure Active Directory Module for Windows PowerShell, run the following command.</span></span>  

    <span data-ttu-id="a28cf-133">$UserCredential = Get-Credential</span><span class="sxs-lookup"><span data-stu-id="a28cf-133">$UserCredential = Get-Credential</span></span>

2. <span data-ttu-id="a28cf-134">Dans la boîte Windows PowerShell demande d’informations d’identification, tapez le nom d’utilisateur et le mot de passe de votre compte Microsoft 365 administrateur global, puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="a28cf-134">In the Windows PowerShell Credential Request dialog box, type the user name and password for your Microsoft 365 global admin account, and then select **OK**.</span></span>

3. <span data-ttu-id="a28cf-135">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="a28cf-135">Run the following command.</span></span>

    <span data-ttu-id="a28cf-136">Connect-MsolService -Credential $UserCredential</span><span class="sxs-lookup"><span data-stu-id="a28cf-136">Connect-MsolService -Credential $UserCredential</span></span>

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a><span data-ttu-id="a28cf-137">Étape 3 : Assurez-vous que vous êtes en mesure d’exécuter des scripts PowerShell</span><span class="sxs-lookup"><span data-stu-id="a28cf-137">Step 3: Make sure you’re able to run PowerShell scripts</span></span>

>[!NOTE]
><span data-ttu-id="a28cf-138">Vous pouvez ignorer cette étape si vous êtes déjà prêt à exécuter des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a28cf-138">You can skip this step if you’re already set up to run PowerShell scripts.</span></span>

<span data-ttu-id="a28cf-139">Pour exécuter le script Get-MsolUserDeviceComplianceStatus.ps1, vous devez activer l’exécution des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a28cf-139">To run the Get-MsolUserDeviceComplianceStatus.ps1 script, you need to enable the running of PowerShell scripts.</span></span>

1. <span data-ttu-id="a28cf-140">À partir de Windows bureau, sélectionnez **Démarrer,** puis tapez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a28cf-140">From your Windows Desktop, select **Start**, and then type Windows PowerShell.</span></span> <span data-ttu-id="a28cf-141">Cliquez avec le bouton Windows PowerShell, puis sélectionnez **Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="a28cf-141">Right-click Windows PowerShell, and then select **Run as administrator**.</span></span>

2. <span data-ttu-id="a28cf-142">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="a28cf-142">Run the following command.</span></span>

    <span data-ttu-id="a28cf-143">Set-ExecutionPolicy RemoteSigned</span><span class="sxs-lookup"><span data-stu-id="a28cf-143">Set-ExecutionPolicy  RemoteSigned</span></span>

3. <span data-ttu-id="a28cf-144">Lorsque vous y invitez, tapez Y, puis appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="a28cf-144">When prompted, type Y and then press Enter.</span></span>

<span data-ttu-id="a28cf-145">**Exécutez la cmdlet Get-MsolDevice pour afficher les détails de tous les appareils de votre organisation**</span><span class="sxs-lookup"><span data-stu-id="a28cf-145">**Run the Get-MsolDevice cmdlet to display details for all devices in your organization**</span></span>

1. <span data-ttu-id="a28cf-146">Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a28cf-146">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>  

2. <span data-ttu-id="a28cf-147">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="a28cf-147">Run the following command.</span></span>

    <span data-ttu-id="a28cf-148">Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_. RegisteredOwners.Count -gt 0}</span><span class="sxs-lookup"><span data-stu-id="a28cf-148">Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}</span></span>

<span data-ttu-id="a28cf-149">Pour plus d’exemples,  [voir Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=2157939).</span><span class="sxs-lookup"><span data-stu-id="a28cf-149">For more examples, see  [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=2157939).</span></span>

## <a name="run-a-script-to-get-device-details"></a><span data-ttu-id="a28cf-150">Exécuter un script pour obtenir les détails de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a28cf-150">Run a script to get device details</span></span>

<span data-ttu-id="a28cf-151">Tout d’abord, enregistrez le script sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a28cf-151">First, save the script to your computer.</span></span>

1. <span data-ttu-id="a28cf-152">Copiez et collez le texte suivant dans Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="a28cf-152">Copy and paste the following text into Notepad.</span></span>  

2.  <span data-ttu-id="a28cf-153">param (</span><span class="sxs-lookup"><span data-stu-id="a28cf-153">param (</span></span>

3.  <span data-ttu-id="a28cf-154">[PSObject[]]$users = @(),</span><span class="sxs-lookup"><span data-stu-id="a28cf-154">[PSObject[]]$users = @(),</span></span>

4.  <span data-ttu-id="a28cf-155">[Switch]$export,</span><span class="sxs-lookup"><span data-stu-id="a28cf-155">[Switch]$export,</span></span>

5.  <span data-ttu-id="a28cf-156">[String]$exportFileName = « UserDeviceComplianceStatus_ » + (Get-Date -Format « yyMMdd_HHMMss ») + « .csv »,</span><span class="sxs-lookup"><span data-stu-id="a28cf-156">[String]$exportFileName = "UserDeviceComplianceStatus_" + (Get-Date -Format "yyMMdd_HHMMss") + ".csv",</span></span>

6.  <span data-ttu-id="a28cf-157">[String]$exportPath = [Environment]::GetFolderPath(« Desktop »)</span><span class="sxs-lookup"><span data-stu-id="a28cf-157">[String]$exportPath = [Environment]::GetFolderPath("Desktop")</span></span>

7.  <span data-ttu-id="a28cf-158">)</span><span class="sxs-lookup"><span data-stu-id="a28cf-158">)</span></span>

9.  <span data-ttu-id="a28cf-159">[System.Collections.IDictionary]$script:schema = @{</span><span class="sxs-lookup"><span data-stu-id="a28cf-159">[System.Collections.IDictionary]$script:schema = @{</span></span>

11.  <span data-ttu-id="a28cf-160">DeviceId = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-160">DeviceId = ''</span></span>

12.  <span data-ttu-id="a28cf-161">DeviceOSType = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-161">DeviceOSType = ''</span></span>

13.  <span data-ttu-id="a28cf-162">DeviceOSVersion = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-162">DeviceOSVersion = ''</span></span>

14.  <span data-ttu-id="a28cf-163">DeviceTrustLevel = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-163">DeviceTrustLevel = ''</span></span>

15.  <span data-ttu-id="a28cf-164">DisplayName = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-164">DisplayName = ''</span></span>

16.  <span data-ttu-id="a28cf-165">IsCompliant = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-165">IsCompliant = ''</span></span>

17.  <span data-ttu-id="a28cf-166">IsManaged = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-166">IsManaged = ''</span></span>

18.  <span data-ttu-id="a28cf-167">ApproximateLastLogonTimestamp = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-167">ApproximateLastLogonTimestamp = ''</span></span>

19.  <span data-ttu-id="a28cf-168">DeviceObjectId = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-168">DeviceObjectId = ''</span></span>

20.  <span data-ttu-id="a28cf-169">RegisteredOwnerUpn = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-169">RegisteredOwnerUpn = ''</span></span>

21.  <span data-ttu-id="a28cf-170">RegisteredOwnerObjectId = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-170">RegisteredOwnerObjectId = ''</span></span>
    

22.  <span data-ttu-id="a28cf-171">RegisteredOwnerDisplayName = ''</span><span class="sxs-lookup"><span data-stu-id="a28cf-171">RegisteredOwnerDisplayName = ''</span></span>
    

23.  <span data-ttu-id="a28cf-172">}</span><span class="sxs-lookup"><span data-stu-id="a28cf-172">}</span></span>
    

25.  <span data-ttu-id="a28cf-173">fonction createResultObject</span><span class="sxs-lookup"><span data-stu-id="a28cf-173">function createResultObject</span></span>
    

26.  <span data-ttu-id="a28cf-174">{</span><span class="sxs-lookup"><span data-stu-id="a28cf-174">{</span></span>
    

28.  <span data-ttu-id="a28cf-175">[PSObject]$resultObject = New-Object -TypeName PSObject -Property $script:schema</span><span class="sxs-lookup"><span data-stu-id="a28cf-175">[PSObject]$resultObject = New-Object -TypeName PSObject -Property $script:schema</span></span>
    

30.  <span data-ttu-id="a28cf-176">renvoyer $resultObject</span><span class="sxs-lookup"><span data-stu-id="a28cf-176">return $resultObject</span></span>
    

31.  <span data-ttu-id="a28cf-177">}</span><span class="sxs-lookup"><span data-stu-id="a28cf-177">}</span></span>
    

33.  <span data-ttu-id="a28cf-178">If ($users. Count -eq 0)</span><span class="sxs-lookup"><span data-stu-id="a28cf-178">If ($users.Count -eq 0)</span></span>
    

34.  <span data-ttu-id="a28cf-179">{</span><span class="sxs-lookup"><span data-stu-id="a28cf-179">{</span></span>
    

35.  <span data-ttu-id="a28cf-180">$users = Get-MsolUser</span><span class="sxs-lookup"><span data-stu-id="a28cf-180">$users = Get-MsolUser</span></span>
    

36.  <span data-ttu-id="a28cf-181">}</span><span class="sxs-lookup"><span data-stu-id="a28cf-181">}</span></span>
    

38.  <span data-ttu-id="a28cf-182">[PSObject[]]$result = foreach ($u dans $users)</span><span class="sxs-lookup"><span data-stu-id="a28cf-182">[PSObject[]]$result = foreach ($u in $users)</span></span>
    

39.  <span data-ttu-id="a28cf-183">{</span><span class="sxs-lookup"><span data-stu-id="a28cf-183">{</span></span>
    

41.  <span data-ttu-id="a28cf-184">[PSObject]$devices = get-msoldevice -RegisteredOwnerUpn $u.UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a28cf-184">[PSObject]$devices = get-msoldevice -RegisteredOwnerUpn $u.UserPrincipalName</span></span>
    

42.  <span data-ttu-id="a28cf-185">foreach ($d dans $devices)</span><span class="sxs-lookup"><span data-stu-id="a28cf-185">foreach ($d in $devices)</span></span>
    

43.  <span data-ttu-id="a28cf-186">{</span><span class="sxs-lookup"><span data-stu-id="a28cf-186">{</span></span>
    

44.  <span data-ttu-id="a28cf-187">[PSObject]$deviceResult = createResultObject</span><span class="sxs-lookup"><span data-stu-id="a28cf-187">[PSObject]$deviceResult = createResultObject</span></span>
    

45.  <span data-ttu-id="a28cf-188">$deviceResult.DeviceId = $d.DeviceId</span><span class="sxs-lookup"><span data-stu-id="a28cf-188">$deviceResult.DeviceId = $d.DeviceId</span></span>
    

46.  <span data-ttu-id="a28cf-189">$deviceResult.DeviceOSType = $d.DeviceOSType</span><span class="sxs-lookup"><span data-stu-id="a28cf-189">$deviceResult.DeviceOSType = $d.DeviceOSType</span></span>
    

47.  <span data-ttu-id="a28cf-190">$deviceResult.DeviceOSVersion = $d.DeviceOSVersion</span><span class="sxs-lookup"><span data-stu-id="a28cf-190">$deviceResult.DeviceOSVersion = $d.DeviceOSVersion</span></span>
    

48.  <span data-ttu-id="a28cf-191">$deviceResult.DeviceTrustLevel = $d.DeviceTrustLevel</span><span class="sxs-lookup"><span data-stu-id="a28cf-191">$deviceResult.DeviceTrustLevel = $d.DeviceTrustLevel</span></span>
    

49.  <span data-ttu-id="a28cf-192">$deviceResult.DisplayName = $d.DisplayName</span><span class="sxs-lookup"><span data-stu-id="a28cf-192">$deviceResult.DisplayName = $d.DisplayName</span></span>
    

50.  <span data-ttu-id="a28cf-193">$deviceResult.IsCompliant = $d.GraphDeviceObject.IsCompliant</span><span class="sxs-lookup"><span data-stu-id="a28cf-193">$deviceResult.IsCompliant = $d.GraphDeviceObject.IsCompliant</span></span>
    

51.  <span data-ttu-id="a28cf-194">$deviceResult.IsManaged = $d.GraphDeviceObject.IsManaged</span><span class="sxs-lookup"><span data-stu-id="a28cf-194">$deviceResult.IsManaged = $d.GraphDeviceObject.IsManaged</span></span>
    

52.  <span data-ttu-id="a28cf-195">$deviceResult.DeviceObjectId = $d.ObjectId</span><span class="sxs-lookup"><span data-stu-id="a28cf-195">$deviceResult.DeviceObjectId = $d.ObjectId</span></span>
    

53.  <span data-ttu-id="a28cf-196">$deviceResult.RegisteredOwnerUpn = $u.UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a28cf-196">$deviceResult.RegisteredOwnerUpn = $u.UserPrincipalName</span></span>
    

54.  <span data-ttu-id="a28cf-197">$deviceResult.RegisteredOwnerObjectId = $u.ObjectId</span><span class="sxs-lookup"><span data-stu-id="a28cf-197">$deviceResult.RegisteredOwnerObjectId = $u.ObjectId</span></span>
    

55.  <span data-ttu-id="a28cf-198">$deviceResult.RegisteredOwnerDisplayName = $u.DisplayName</span><span class="sxs-lookup"><span data-stu-id="a28cf-198">$deviceResult.RegisteredOwnerDisplayName = $u.DisplayName</span></span>
    

56.  <span data-ttu-id="a28cf-199">$deviceResult.ApproximateLastLogonTimestamp = $d.ApproximateLastLogonTimestamp</span><span class="sxs-lookup"><span data-stu-id="a28cf-199">$deviceResult.ApproximateLastLogonTimestamp = $d.ApproximateLastLogonTimestamp</span></span>
    

58.  <span data-ttu-id="a28cf-200">$deviceResult</span><span class="sxs-lookup"><span data-stu-id="a28cf-200">$deviceResult</span></span>
    

59.  <span data-ttu-id="a28cf-201">}</span><span class="sxs-lookup"><span data-stu-id="a28cf-201">}</span></span>
    

61.  <span data-ttu-id="a28cf-202">}</span><span class="sxs-lookup"><span data-stu-id="a28cf-202">}</span></span>
    

63.  <span data-ttu-id="a28cf-203">If ($export)</span><span class="sxs-lookup"><span data-stu-id="a28cf-203">If ($export)</span></span>
    

64.  <span data-ttu-id="a28cf-204">{</span><span class="sxs-lookup"><span data-stu-id="a28cf-204">{</span></span>
    

65.  <span data-ttu-id="a28cf-205">$result | Export-Csv -path ($exportPath + " \" + $exportFileName) -NoTypeInformation</span><span class="sxs-lookup"><span data-stu-id="a28cf-205">$result | Export-Csv -path ($exportPath + "\" + $exportFileName) -NoTypeInformation</span></span>
    

66.  <span data-ttu-id="a28cf-206">}</span><span class="sxs-lookup"><span data-stu-id="a28cf-206">}</span></span>
    

67.  <span data-ttu-id="a28cf-207">Else</span><span class="sxs-lookup"><span data-stu-id="a28cf-207">Else</span></span>
    

68.  <span data-ttu-id="a28cf-208">{</span><span class="sxs-lookup"><span data-stu-id="a28cf-208">{</span></span>
    

69.  <span data-ttu-id="a28cf-209">$result</span><span class="sxs-lookup"><span data-stu-id="a28cf-209">$result</span></span>
    

70.  <span data-ttu-id="a28cf-210">}</span><span class="sxs-lookup"><span data-stu-id="a28cf-210">}</span></span>
    

71.  <span data-ttu-id="a28cf-211">Enregistrez-le en tant que fichier Windows PowerShell script à l’aide de l’extension de .ps1 ; par exemple, Get-MsolUserDeviceComplianceStatus.ps1.</span><span class="sxs-lookup"><span data-stu-id="a28cf-211">Save it as a Windows PowerShell script file by using the file extension .ps1; for example, Get-MsolUserDeviceComplianceStatus.ps1.</span></span>   

## <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a><span data-ttu-id="a28cf-212">Exécutez le script pour obtenir des informations sur l’appareil d’un seul compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a28cf-212">Run the script to get device information for a single user account</span></span>

1. <span data-ttu-id="a28cf-213">Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a28cf-213">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="a28cf-214">Go to the folder where you saved the script.</span><span class="sxs-lookup"><span data-stu-id="a28cf-214">Go to the folder where you saved the script.</span></span> <span data-ttu-id="a28cf-215">Par exemple, si vous l’avez enregistré dans C:\PS-Scripts, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="a28cf-215">For example, if you saved it to C:\PS-Scripts, run the following command.</span></span>
    
    <span data-ttu-id="a28cf-216">cd C:\PS-Scripts</span><span class="sxs-lookup"><span data-stu-id="a28cf-216">cd C:\PS-Scripts</span></span>

3. <span data-ttu-id="a28cf-217">Exécutez la commande suivante pour identifier l’utilisateur pour qui vous souhaitez obtenir les détails de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a28cf-217">Run the following command to identify the user you want to get device details for.</span></span> <span data-ttu-id="a28cf-218">Cet exemple obtient les détails de bar@example.com.</span><span class="sxs-lookup"><span data-stu-id="a28cf-218">This example gets details for bar@example.com.</span></span>
    
    <span data-ttu-id="a28cf-219">$u = Get-MsolUser -UserPrincipalName bar@example.com</span><span class="sxs-lookup"><span data-stu-id="a28cf-219">$u = Get-MsolUser -UserPrincipalName bar@example.com</span></span>

4. <span data-ttu-id="a28cf-220">Exécutez la commande suivante pour lancer le script.</span><span class="sxs-lookup"><span data-stu-id="a28cf-220">Run the following command to initiate the script.</span></span>

    <span data-ttu-id="a28cf-221">.\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export</span><span class="sxs-lookup"><span data-stu-id="a28cf-221">.\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export</span></span>

<span data-ttu-id="a28cf-222">Les informations sont exportées vers votre bureau Windows en tant que fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="a28cf-222">The information is exported to your Windows Desktop as a CSV file.</span></span> <span data-ttu-id="a28cf-223">Vous pouvez utiliser des paramètres supplémentaires pour spécifier le nom de fichier et le chemin d’accès du fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="a28cf-223">You can use additional parameters to specify the file name and path of the CSV.</span></span>

## <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a><span data-ttu-id="a28cf-224">Exécutez le script pour obtenir des informations sur l’appareil d’un groupe d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a28cf-224">Run the script to get device information for a group of users</span></span>

1. <span data-ttu-id="a28cf-225">Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a28cf-225">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="a28cf-226">Go to the folder where you saved the script.</span><span class="sxs-lookup"><span data-stu-id="a28cf-226">Go to the folder where you saved the script.</span></span> <span data-ttu-id="a28cf-227">Par exemple, si vous l’avez enregistré dans C:\PS-Scripts, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="a28cf-227">For example, if you saved it to C:\PS-Scripts, run the following command.</span></span>   

    <span data-ttu-id="a28cf-228">cd C:\PS-Scripts</span><span class="sxs-lookup"><span data-stu-id="a28cf-228">cd C:\PS-Scripts</span></span>

3. <span data-ttu-id="a28cf-229">Exécutez la commande suivante pour identifier le groupe pour qui vous souhaitez obtenir les détails de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a28cf-229">Run the following command to identify the group you want to get device details for.</span></span> <span data-ttu-id="a28cf-230">Cet exemple obtient des détails pour les utilisateurs du groupe FinanceStaff.</span><span class="sxs-lookup"><span data-stu-id="a28cf-230">This example gets details for users in the FinanceStaff group.</span></span> 

    <span data-ttu-id="a28cf-231">$u = Get-MsolGroupMember -SearchString « FinanceStaff » | % { Get-MsolUser -ObjectId $_. ObjectId }</span><span class="sxs-lookup"><span data-stu-id="a28cf-231">$u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }</span></span>

4. <span data-ttu-id="a28cf-232">Exécutez la commande suivante pour lancer le script.</span><span class="sxs-lookup"><span data-stu-id="a28cf-232">Run the following command to initiate the script.</span></span>

    <span data-ttu-id="a28cf-233">.\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export</span><span class="sxs-lookup"><span data-stu-id="a28cf-233">.\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export</span></span>

<span data-ttu-id="a28cf-234">Les informations sont exportées vers votre bureau Windows en tant que fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="a28cf-234">The information is exported to your Windows Desktop as a CSV file.</span></span> <span data-ttu-id="a28cf-235">Vous pouvez utiliser des paramètres supplémentaires pour spécifier le nom de fichier et le chemin d’accès du fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="a28cf-235">You can use additional parameters to specify the file name and path of the CSV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a28cf-236">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a28cf-236">Related topics</span></span>

[<span data-ttu-id="a28cf-237">Microsoft Connecter été retiré</span><span class="sxs-lookup"><span data-stu-id="a28cf-237">Microsoft Connect Has Been Retired</span></span>](/collaborate/connect-redirect)

[<span data-ttu-id="a28cf-238">Vue d’ensemble de la fonction Mobility + Security de Base</span><span class="sxs-lookup"><span data-stu-id="a28cf-238">Overview of Basic Mobility and Security</span></span>](overview.md)

[<span data-ttu-id="a28cf-239">Get-MsolDevice</span><span class="sxs-lookup"><span data-stu-id="a28cf-239">Get-MsolDevice</span></span>](https://go.microsoft.com/fwlink/?linkid=2157939)