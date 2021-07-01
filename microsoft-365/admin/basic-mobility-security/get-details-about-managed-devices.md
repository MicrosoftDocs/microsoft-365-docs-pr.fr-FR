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
ms.openlocfilehash: 2edee1b08f137d3e4f977b4d6800c1b0fc0e0473
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53228170"
---
# <a name="get-details-about-basic-mobility-and-security-managed-devices"></a><span data-ttu-id="5cf7a-103">Obtenir des détails sur les appareils gérés par la mobilité et la sécurité de base</span><span class="sxs-lookup"><span data-stu-id="5cf7a-103">Get details about Basic Mobility and Security managed devices</span></span>

<span data-ttu-id="5cf7a-104">Cet article vous montre comment utiliser Windows PowerShell pour obtenir des détails sur les appareils de votre organisation que vous avez mis en place pour basic Mobility and Security.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-104">This article shows you how to use Windows PowerShell to get details about the devices in your organization that you set up for Basic Mobility and Security.</span></span>

<span data-ttu-id="5cf7a-105">Voici une répartition des détails de l’appareil à votre disposition.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-105">Here's a breakdown for the device details available to you.</span></span>

|<span data-ttu-id="5cf7a-106">**Detail**</span><span class="sxs-lookup"><span data-stu-id="5cf7a-106">**Detail**</span></span>|<span data-ttu-id="5cf7a-107">**Ce qu’il faut rechercher dans PowerShell**</span><span class="sxs-lookup"><span data-stu-id="5cf7a-107">**What to look for in PowerShell**</span></span>|
|:----------------|:------------------------------------------------------------------------------|
|<span data-ttu-id="5cf7a-108">L’appareil est inscrit à Basic Mobility and Security.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-108">Device is enrolled in Basic Mobility and Security.</span></span> <span data-ttu-id="5cf7a-109">Pour plus d’informations, voir [Inscrire votre appareil mobile à l’aide de Basic Mobility and Security](enroll-your-mobile-device.md)</span><span class="sxs-lookup"><span data-stu-id="5cf7a-109">For more info, see [Enroll your mobile device using Basic Mobility and Security](enroll-your-mobile-device.md)</span></span>|<span data-ttu-id="5cf7a-110">La valeur du *paramètre isManaged est*   :</span><span class="sxs-lookup"><span data-stu-id="5cf7a-110">The value of the *isManaged* parameter is:</span></span><br/><span data-ttu-id="5cf7a-111">**True**= l’appareil est inscrit.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-111">**True**= device is enrolled.</span></span><br/><span data-ttu-id="5cf7a-112">**False**= l’appareil n’est pas inscrit.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-112">**False**= device is not enrolled.</span></span> |
|<span data-ttu-id="5cf7a-113">L’appareil est conforme aux stratégies de sécurité de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-113">Device is compliant with your device security policies.</span></span> <span data-ttu-id="5cf7a-114">Pour plus d’informations, voir [Créer des stratégies de sécurité d’appareil](create-device-security-policies.md)</span><span class="sxs-lookup"><span data-stu-id="5cf7a-114">For more info, see [Create device security policies](create-device-security-policies.md)</span></span>|<span data-ttu-id="5cf7a-115">La valeur du *paramètre isCompliant*   est :</span><span class="sxs-lookup"><span data-stu-id="5cf7a-115">The value of the *isCompliant* parameter is:</span></span><br/><span data-ttu-id="5cf7a-116">**True**   = l’appareil est conforme aux stratégies.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-116">**True** = device is compliant with policies.</span></span><br/><span data-ttu-id="5cf7a-117">**False**   = l’appareil n’est pas conforme aux stratégies.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-117">**False** = device is not compliant with policies.</span></span>|

:::image type="content" source="../../media/basic-mobility-security/bms-7-powershell-parameters.png" alt-text="Paramètres PowerShell de mobilité et de sécurité de base":::

> [!NOTE]
> <span data-ttu-id="5cf7a-119">Les commandes et les scripts de cet article retournent également des détails sur les appareils gérés [par Microsoft Intune](https://www.microsoft.com/cloud-platform/microsoft-intune).</span><span class="sxs-lookup"><span data-stu-id="5cf7a-119">The commands and scripts in this article also return details about any devices managed by [Microsoft Intune](https://www.microsoft.com/cloud-platform/microsoft-intune).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="5cf7a-120">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5cf7a-120">Before you begin</span></span>

<span data-ttu-id="5cf7a-121">Vous devez configurer plusieurs éléments pour exécuter les commandes et les scripts décrits dans cet article.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-121">There are a few things you need to set up to run the commands and scripts described in this article.</span></span>

### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="5cf7a-122">Étape 1 : Télécharger et installer le module Azure Active Directory pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5cf7a-122">Step 1: Download and install the Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="5cf7a-123">Pour plus d’informations sur ces [étapes, voir Connecter à Microsoft 365 avec PowerShell.](/office365/enterprise/powershell/connect-to-office-365-powershell)</span><span class="sxs-lookup"><span data-stu-id="5cf7a-123">For more info on these steps, see [Connect to Microsoft 365 with PowerShell](/office365/enterprise/powershell/connect-to-office-365-powershell).</span></span>

1. <span data-ttu-id="5cf7a-124">Go to [Microsoft Online Services Sign-In Assistant for IT Professionals RTWl](https://download.microsoft.com/download/7/1/E/71EF1D05-A42C-4A1F-8162-96494B5E615C/msoidcli_32bit.msi)and select Download for Microsoft Online Services    **Sign-in Assistant**.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-124">Go to [Microsoft Online Services Sign-In Assistant for IT Professionals RTWl](https://download.microsoft.com/download/7/1/E/71EF1D05-A42C-4A1F-8162-96494B5E615C/msoidcli_32bit.msi) and select  **Download for Microsoft Online Services Sign-in Assistant**.</span></span>

2. <span data-ttu-id="5cf7a-125">Téléchargez et installez le Module Microsoft Azure Active Directory pour Windows PowerShell en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="5cf7a-125">Install the Microsoft Azure Active Directory Module for Windows PowerShell with these steps:</span></span>

    1. <span data-ttu-id="5cf7a-126">Ouvrez une invite de commandes PowerShell de niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-126">Open an administrator-level PowerShell command prompt.</span></span>

    2. <span data-ttu-id="5cf7a-127">Exécutez la commande `Install-Module MSOnline`.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-127">Run the `Install-Module MSOnline` command.</span></span>

    3. <span data-ttu-id="5cf7a-128">Si vous êtes invité à installer le fournisseur NuGet, tapez O, puis appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-128">If prompted to install the NuGet provider, type Y and press ENTER.</span></span>

    4. <span data-ttu-id="5cf7a-129">Si vous êtes invité à installer le module à partir de PSGallery, tapez O, puis appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-129">If prompted to install the module from PSGallery, type Y and press ENTER.</span></span>

    5. <span data-ttu-id="5cf7a-130">Après l’installation, fermez la fenêtre de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-130">After installation, close the PowerShell command window.</span></span>

### <a name="step-2-connect-to-your-microsoft-365-subscription"></a><span data-ttu-id="5cf7a-131">Étape 2 : Connecter à votre abonnement Microsoft 365 abonnement</span><span class="sxs-lookup"><span data-stu-id="5cf7a-131">Step 2: Connect to your Microsoft 365 subscription</span></span>

1. <span data-ttu-id="5cf7a-132">Dans le Windows Azure Active Directory module de Windows PowerShell, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-132">In the Windows Azure Active Directory Module for Windows PowerShell, run the following command.</span></span>

   ```powershell
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="5cf7a-133">Dans la boîte Windows PowerShell demande d’informations d’identification, tapez le nom d’utilisateur et le mot de passe de votre compte Microsoft 365 administrateur global, puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="5cf7a-133">In the Windows PowerShell Credential Request dialog box, type the user name and password for your Microsoft 365 global admin account, and then select **OK**.</span></span>

3. <span data-ttu-id="5cf7a-134">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5cf7a-134">Run the following command.</span></span>

   ```powershell
   Connect-MsolService -Credential $UserCredential
   ```

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a><span data-ttu-id="5cf7a-135">Étape 3 : Assurez-vous que vous êtes en mesure d’exécuter des scripts PowerShell</span><span class="sxs-lookup"><span data-stu-id="5cf7a-135">Step 3: Make sure you’re able to run PowerShell scripts</span></span>

> [!NOTE]
> <span data-ttu-id="5cf7a-136">Vous pouvez ignorer cette étape si vous êtes déjà prêt à exécuter des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-136">You can skip this step if you’re already set up to run PowerShell scripts.</span></span>

<span data-ttu-id="5cf7a-137">Pour exécuter le script Get-MsolUserDeviceComplianceStatus.ps1, vous devez activer l’exécution des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-137">To run the Get-MsolUserDeviceComplianceStatus.ps1 script, you need to enable the running of PowerShell scripts.</span></span>

1. <span data-ttu-id="5cf7a-138">À partir de Windows bureau, sélectionnez **Démarrer,** puis tapez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-138">From your Windows Desktop, select **Start**, and then type Windows PowerShell.</span></span> <span data-ttu-id="5cf7a-139">Cliquez avec le bouton Windows PowerShell, puis sélectionnez **Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="5cf7a-139">Right-click Windows PowerShell, and then select **Run as administrator**.</span></span>

2. <span data-ttu-id="5cf7a-140">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5cf7a-140">Run the following command.</span></span>

   ```powershell
   Set-ExecutionPolicy  RemoteSigned
   ```

3. <span data-ttu-id="5cf7a-141">Lorsque vous y invitez, tapez Y, puis appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-141">When prompted, type Y and then press Enter.</span></span>

#### <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a><span data-ttu-id="5cf7a-142">Exécutez la cmdlet Get-MsolDevice pour afficher les détails de tous les appareils de votre organisation</span><span class="sxs-lookup"><span data-stu-id="5cf7a-142">Run the Get-MsolDevice cmdlet to display details for all devices in your organization</span></span>

1. <span data-ttu-id="5cf7a-143">Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-143">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>

2. <span data-ttu-id="5cf7a-144">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5cf7a-144">Run the following command.</span></span>

   ```powershell
   Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
   ```

<span data-ttu-id="5cf7a-145">Pour plus d’exemples,  [voir Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=2157939).</span><span class="sxs-lookup"><span data-stu-id="5cf7a-145">For more examples, see  [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=2157939).</span></span>

## <a name="run-a-script-to-get-device-details"></a><span data-ttu-id="5cf7a-146">Exécuter un script pour obtenir les détails de l’appareil</span><span class="sxs-lookup"><span data-stu-id="5cf7a-146">Run a script to get device details</span></span>

<span data-ttu-id="5cf7a-147">Tout d’abord, enregistrez le script sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-147">First, save the script to your computer.</span></span>

1. <span data-ttu-id="5cf7a-148">Copiez et collez le texte suivant dans Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-148">Copy and paste the following text into Notepad.</span></span>

   ```powershell
   param (
   [PSObject[]]$users = @(),
   [Switch]$export,
   [String]$exportFileName = "UserDeviceComplianceStatus_" + (Get-Date -Format "yyMMdd_HHMMss") + ".csv",
   [String]$exportPath = [Environment]::GetFolderPath("Desktop")
   )
   [System.Collections.IDictionary]$script:schema = @{
   DeviceId = ''
   DeviceOSType = ''
   DeviceOSVersion = ''
   DeviceTrustLevel = ''
   DisplayName = ''
   IsCompliant = ''
   IsManaged = ''
   ApproximateLastLogonTimestamp = ''
   DeviceObjectId = ''
   RegisteredOwnerUpn = ''
   RegisteredOwnerObjectId = ''
   RegisteredOwnerDisplayName = ''
   }
   function createResultObject
   {
   [PSObject]$resultObject = New-Object -TypeName PSObject -Property $script:schema
   return $resultObject
   }
   If ($users.Count -eq 0)
   {
   $users = Get-MsolUser
   }
   [PSObject[]]$result = foreach ($u in $users)
   {
   [PSObject]$devices = get-msoldevice -RegisteredOwnerUpn $u.UserPrincipalName
   foreach ($d in $devices)
   {
   [PSObject]$deviceResult = createResultObject
   $deviceResult.DeviceId = $d.DeviceId
   $deviceResult.DeviceOSType = $d.DeviceOSType
   $deviceResult.DeviceOSVersion = $d.DeviceOSVersion
   $deviceResult.DeviceTrustLevel = $d.DeviceTrustLevel
   $deviceResult.DisplayName = $d.DisplayName
   $deviceResult.IsCompliant = $d.GraphDeviceObject.IsCompliant
   $deviceResult.IsManaged = $d.GraphDeviceObject.IsManaged
   $deviceResult.DeviceObjectId = $d.ObjectId
   $deviceResult.RegisteredOwnerUpn = $u.UserPrincipalName
   $deviceResult.RegisteredOwnerObjectId = $u.ObjectId
   $deviceResult.RegisteredOwnerDisplayName = $u.DisplayName
   $deviceResult.ApproximateLastLogonTimestamp = $d.ApproximateLastLogonTimestamp
   $deviceResult
   }
   }
   If ($export)
   {
   $result | Export-Csv -path ($exportPath + "\" + $exportFileName) -NoTypeInformation
   }
   Else
   {
   $result
   }
   ```

2. <span data-ttu-id="5cf7a-149">Enregistrez-le en tant que fichier Windows PowerShell script à l’aide de l’extension de .ps1 ; par exemple, Get-MsolUserDeviceComplianceStatus.ps1.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-149">Save it as a Windows PowerShell script file by using the file extension .ps1; for example, Get-MsolUserDeviceComplianceStatus.ps1.</span></span>

## <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a><span data-ttu-id="5cf7a-150">Exécutez le script pour obtenir des informations sur l’appareil d’un seul compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="5cf7a-150">Run the script to get device information for a single user account</span></span>

1. <span data-ttu-id="5cf7a-151">Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-151">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>

2. <span data-ttu-id="5cf7a-152">Go to the folder where you saved the script.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-152">Go to the folder where you saved the script.</span></span> <span data-ttu-id="5cf7a-153">Par exemple, si vous l’avez enregistré dans C:\PS-Scripts, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-153">For example, if you saved it to C:\PS-Scripts, run the following command.</span></span>

   ```powershell
   cd C:\PS-Scripts
   ```

3. <span data-ttu-id="5cf7a-154">Exécutez la commande suivante pour identifier l’utilisateur pour qui vous souhaitez obtenir les détails de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-154">Run the following command to identify the user you want to get device details for.</span></span> <span data-ttu-id="5cf7a-155">Cet exemple obtient les détails de bar@example.com.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-155">This example gets details for bar@example.com.</span></span>

   ```powershell
   $u = Get-MsolUser -UserPrincipalName bar@example.com
   ```

4. <span data-ttu-id="5cf7a-156">Exécutez la commande suivante pour lancer le script.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-156">Run the following command to initiate the script.</span></span>

   ```powershell
   .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
   ```

<span data-ttu-id="5cf7a-157">Les informations sont exportées vers votre bureau Windows en tant que fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-157">The information is exported to your Windows Desktop as a CSV file.</span></span> <span data-ttu-id="5cf7a-158">Vous pouvez utiliser des paramètres supplémentaires pour spécifier le nom de fichier et le chemin d’accès du fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-158">You can use additional parameters to specify the file name and path of the CSV.</span></span>

## <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a><span data-ttu-id="5cf7a-159">Exécutez le script pour obtenir des informations sur l’appareil d’un groupe d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="5cf7a-159">Run the script to get device information for a group of users</span></span>

1. <span data-ttu-id="5cf7a-160">Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-160">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>

2. <span data-ttu-id="5cf7a-161">Go to the folder where you saved the script.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-161">Go to the folder where you saved the script.</span></span> <span data-ttu-id="5cf7a-162">Par exemple, si vous l’avez enregistré dans C:\PS-Scripts, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-162">For example, if you saved it to C:\PS-Scripts, run the following command.</span></span>

   ```powershell
   cd C:\PS-Scripts
   ```

3. <span data-ttu-id="5cf7a-163">Exécutez la commande suivante pour identifier le groupe pour qui vous souhaitez obtenir les détails de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-163">Run the following command to identify the group you want to get device details for.</span></span> <span data-ttu-id="5cf7a-164">Cet exemple obtient des détails pour les utilisateurs du groupe FinanceStaff.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-164">This example gets details for users in the FinanceStaff group.</span></span>

   ```powershell
   $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
   ```

4. <span data-ttu-id="5cf7a-165">Exécutez la commande suivante pour lancer le script.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-165">Run the following command to initiate the script.</span></span>

   ```powershell
   .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
   ```

<span data-ttu-id="5cf7a-166">Les informations sont exportées vers votre bureau Windows en tant que fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-166">The information is exported to your Windows Desktop as a CSV file.</span></span> <span data-ttu-id="5cf7a-167">Vous pouvez utiliser des paramètres supplémentaires pour spécifier le nom de fichier et le chemin d’accès du fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-167">You can use additional parameters to specify the file name and path of the CSV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cf7a-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cf7a-168">Related topics</span></span>

[<span data-ttu-id="5cf7a-169">Microsoft Connecter été retiré</span><span class="sxs-lookup"><span data-stu-id="5cf7a-169">Microsoft Connect Has Been Retired</span></span>](/collaborate/connect-redirect)

[<span data-ttu-id="5cf7a-170">Vue d’ensemble de la fonction Mobility + Security de Base</span><span class="sxs-lookup"><span data-stu-id="5cf7a-170">Overview of Basic Mobility and Security</span></span>](overview.md)

[<span data-ttu-id="5cf7a-171">Get-MsolDevice</span><span class="sxs-lookup"><span data-stu-id="5cf7a-171">Get-MsolDevice</span></span>](https://go.microsoft.com/fwlink/?linkid=2157939)
