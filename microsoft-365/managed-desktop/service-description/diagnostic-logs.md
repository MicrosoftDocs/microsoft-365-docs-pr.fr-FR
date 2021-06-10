---
title: Journaux de diagnostic
description: Journaux qui peuvent être collectés à partir d’appareils lors de la résolution des problèmes et comment ils sont stockés
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: ef7d19fef989610c10323c2a9820a5314d5e1641
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52272890"
---
# <a name="diagnostic-logs"></a><span data-ttu-id="b2799-104">Journaux de diagnostic</span><span class="sxs-lookup"><span data-stu-id="b2799-104">Diagnostic logs</span></span>

<span data-ttu-id="b2799-105">Lorsque nous dépannageons un problème sur un appareil géré par Bureau géré Microsoft, qu’il s’agit d’un problème que vous avez signalé ou identifié par notre service, il se peut que nous deions collecter certains journaux de diagnostic à partir de l’appareil sans l’intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2799-105">When we troubleshoot an issue on a device managed by Microsoft Managed Desktop, whether one you've reported or one identified by our service, we might have to collect certain diagnostic logs from the device without intervention from the user.</span></span> <span data-ttu-id="b2799-106">Nous ne collectons pas de contenu ou d’informations générés par l’utilisateur à partir des annuaires d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b2799-106">We don't collect any user-generated content or information from user directories.</span></span> <span data-ttu-id="b2799-107">Nous collectons uniquement les données de diagnostic et de journal qui concernent l’état et l’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2799-107">We only collect diagnostic and log data that concerns device health and status.</span></span>

<span data-ttu-id="b2799-108">Nous stockons tous les journaux collectés pendant 28 jours, puis les supprimons.</span><span class="sxs-lookup"><span data-stu-id="b2799-108">We store any collected logs for 28 days, and then delete them.</span></span> <span data-ttu-id="b2799-109">Nous traiterons tous les journaux collectés à partir d’un appareil en suivant nos normes [de gestion des données.](privacy-personal-data.md)</span><span class="sxs-lookup"><span data-stu-id="b2799-109">We process any logs collected from a device following our [data handling standards](privacy-personal-data.md).</span></span>

## <a name="data-collected"></a><span data-ttu-id="b2799-110">Données collectées</span><span class="sxs-lookup"><span data-stu-id="b2799-110">Data collected</span></span>

<span data-ttu-id="b2799-111">Cette liste inclut tous les dossiers, journaux d’événements, fichiers exécutables ou emplacements de Registre à partir Bureau géré Microsoft journaux de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="b2799-111">This list includes all the folders, event logs, executables, or registry locations that Microsoft Managed Desktop might collect diagnostic logs from.</span></span> <span data-ttu-id="b2799-112">Les données réelles collectées sont un sous-ensemble de cette liste et dépendent du problème identifié.</span><span class="sxs-lookup"><span data-stu-id="b2799-112">The actual data collected will be a subset of this list and depends on the identified issue.</span></span>

### <a name="registry-keys"></a><span data-ttu-id="b2799-113">Clés du Registre</span><span class="sxs-lookup"><span data-stu-id="b2799-113">Registry keys</span></span>

- <span data-ttu-id="b2799-114">HKLM \\ SYSTEM \\ CurrentControlSet \\ Services</span><span class="sxs-lookup"><span data-stu-id="b2799-114">HKLM\\SYSTEM\\CurrentControlSet\\Services</span></span>
- <span data-ttu-id="b2799-115">HKLM \\ SOFTWARE \\ Microsoft \\ Surface</span><span class="sxs-lookup"><span data-stu-id="b2799-115">HKLM\\SOFTWARE\\Microsoft\\Surface</span></span>
- <span data-ttu-id="b2799-116">Stratégies \\ \\ logicielles \\ HKLM \\ microsoft Windows \\ WindowsUpdate</span><span class="sxs-lookup"><span data-stu-id="b2799-116">HKLM\\SOFTWARE\\Policies\\Microsoft\\Windows\\WindowsUpdate</span></span>
- <span data-ttu-id="b2799-117">HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ MUI \\ UILanguages</span><span class="sxs-lookup"><span data-stu-id="b2799-117">HKLM\\SYSTEM\\CurrentControlSet\\Control\\MUI\\UILanguages</span></span>
- <span data-ttu-id="b2799-118">Stratégies logicielles HKLM \\ \\ Microsoft \\ \\ WindowsStore</span><span class="sxs-lookup"><span data-stu-id="b2799-118">HKLM\\Software\\Policies\\Microsoft\\WindowsStore</span></span>
- <span data-ttu-id="b2799-119">HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion \\ WindowsStore \\ WindowsUpdate</span><span class="sxs-lookup"><span data-stu-id="b2799-119">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\WindowsStore\\WindowsUpdate</span></span>
- <span data-ttu-id="b2799-120">HKLM \\ SOFTWARE Microsoft Windows \\ \\ NT \\ CurrentVersion</span><span class="sxs-lookup"><span data-stu-id="b2799-120">HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion</span></span>
- <span data-ttu-id="b2799-121">HKLM \\ SOFTWARE Microsoft Windows \\ \\ NT \\ CurrentVersion</span><span class="sxs-lookup"><span data-stu-id="b2799-121">HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion</span></span>
- <span data-ttu-id="b2799-122">HKLM \\ SOFTWARE Microsoft Windows \\ \\ \\ CurrentVersion \\ AppModel</span><span class="sxs-lookup"><span data-stu-id="b2799-122">HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>
- <span data-ttu-id="b2799-123">HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ FirmwareResources</span><span class="sxs-lookup"><span data-stu-id="b2799-123">HKLM\\SYSTEM\\CurrentControlSet\\Control\\FirmwareResources</span></span>
- <span data-ttu-id="b2799-124">HKLM \\ SOFTWARE \\ Microsoft \\ WindowsSelfhost</span><span class="sxs-lookup"><span data-stu-id="b2799-124">HKLM\\SOFTWARE\\Microsoft\\WindowsSelfhost</span></span>
- <span data-ttu-id="b2799-125">HKLM \\ SOFTWARE \\ Microsoft \\ WindowsUpdate</span><span class="sxs-lookup"><span data-stu-id="b2799-125">HKLM\\SOFTWARE\\Microsoft\\WindowsUpdate</span></span>
- <span data-ttu-id="b2799-126">HKLM \\ SOFTWARE Microsoft Windows \\ \\ \\ CurrentVersion \\ Appx</span><span class="sxs-lookup"><span data-stu-id="b2799-126">HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Appx</span></span>
- <span data-ttu-id="b2799-127">HKLM \\ SOFTWARE Microsoft Windows \\ \\ NT \\ CurrentVersion \\ Superfetch</span><span class="sxs-lookup"><span data-stu-id="b2799-127">HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Superfetch</span></span>
- <span data-ttu-id="b2799-128">Configuration DU SYSTÈME HKLM \\ \\</span><span class="sxs-lookup"><span data-stu-id="b2799-128">HKLM\\SYSTEM\\Setup</span></span>
- <span data-ttu-id="b2799-129">HKLM \\ Software \\ Microsoft \\ IntuneManagementExtension</span><span class="sxs-lookup"><span data-stu-id="b2799-129">HKLM\\Software\\Microsoft\\IntuneManagementExtension</span></span>
- <span data-ttu-id="b2799-130">HKLM \\ SOFTWARE \\ Microsoft \\ SystemCertificates \\ AuthRoot</span><span class="sxs-lookup"><span data-stu-id="b2799-130">HKLM\\SOFTWARE\\Microsoft\\SystemCertificates\\AuthRoot</span></span>
- <span data-ttu-id="b2799-131">HKLM \\ SOFTWARE Microsoft Windows - Protection avancée contre les \\ \\ menaces</span><span class="sxs-lookup"><span data-stu-id="b2799-131">HKLM\\SOFTWARE\\Microsoft\\Windows Advanced Threat Protection</span></span>
- <span data-ttu-id="b2799-132">HKLM \\ SOFTWARE Microsoft Windows \\ \\ \\ CurrentVersion Authentication \\ \\ LogonUI</span><span class="sxs-lookup"><span data-stu-id="b2799-132">HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Authentication\\LogonUI</span></span>
- <span data-ttu-id="b2799-133">HKLM \\ SOFTWARE Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2799-133">HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Settings</span></span>
- <span data-ttu-id="b2799-134">\\Désinstallation de HKLM Software \\ Microsoft Windows \\ \\ CurrentVersion \\</span><span class="sxs-lookup"><span data-stu-id="b2799-134">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Uninstall</span></span>
- <span data-ttu-id="b2799-135">Stratégies \\ \\ logicielles HKLM</span><span class="sxs-lookup"><span data-stu-id="b2799-135">HKLM\\Software\\Policies</span></span>
- <span data-ttu-id="b2799-136">HKLM \\ SOFTWARE \\ Policies \\ Microsoft \\ Cryptography \\ Configuration \\ SSL</span><span class="sxs-lookup"><span data-stu-id="b2799-136">HKLM\\SOFTWARE\\Policies\\Microsoft\\Cryptography\\Configuration\\SSL</span></span>
- <span data-ttu-id="b2799-137">Stratégies logicielles HKLM \\ microsoft Windows protection avancée contre les \\ \\ \\ menaces</span><span class="sxs-lookup"><span data-stu-id="b2799-137">HKLM\\SOFTWARE\\Policies\\Microsoft\\Windows Advanced Threat Protection</span></span>
- <span data-ttu-id="b2799-138">HKLM \\ SOFTWARE \\ WOW6432Node \\ Microsoft Windows \\ \\ CurrentVersion \\ Uninstall</span><span class="sxs-lookup"><span data-stu-id="b2799-138">HKLM\\SOFTWARE\\WOW6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall</span></span>
- <span data-ttu-id="b2799-139">HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ SecurityProviders \\ SCHANNEL</span><span class="sxs-lookup"><span data-stu-id="b2799-139">HKLM\\SYSTEM\\CurrentControlSet\\Control\\SecurityProviders\\SCHANNEL</span></span>

### <a name="commands"></a><span data-ttu-id="b2799-140">Commandes</span><span class="sxs-lookup"><span data-stu-id="b2799-140">Commands</span></span>

- <span data-ttu-id="b2799-141">%programfiles% \\ windows defendermpcmdrun.exe \\ -GetFiles</span><span class="sxs-lookup"><span data-stu-id="b2799-141">%programfiles%\\windows defender\\mpcmdrun.exe -GetFiles</span></span>
- <span data-ttu-id="b2799-142">%windir% \\ system32 \\certutil.exe -store</span><span class="sxs-lookup"><span data-stu-id="b2799-142">%windir%\\system32\\certutil.exe -store</span></span>
- <span data-ttu-id="b2799-143">%windir% \\ system32 \\certutil.exe -store -user my</span><span class="sxs-lookup"><span data-stu-id="b2799-143">%windir%\\system32\\certutil.exe -store -user my</span></span>
- <span data-ttu-id="b2799-144">%windir% \\ system32 \\Dsregcmd.exe /status</span><span class="sxs-lookup"><span data-stu-id="b2799-144">%windir%\\system32\\Dsregcmd.exe /status</span></span>
- <span data-ttu-id="b2799-145">%windir% \\ system32 \\ipconfig.exe /all</span><span class="sxs-lookup"><span data-stu-id="b2799-145">%windir%\\system32\\ipconfig.exe /all</span></span>
- <span data-ttu-id="b2799-146">%windir% \\ system32 \\ipconfig.exe /displaydns</span><span class="sxs-lookup"><span data-stu-id="b2799-146">%windir%\\system32\\ipconfig.exe /displaydns</span></span>
- <span data-ttu-id="b2799-147">%windir% \\ system32 \\mdmdiagnosticstool.exe</span><span class="sxs-lookup"><span data-stu-id="b2799-147">%windir%\\system32\\mdmdiagnosticstool.exe</span></span>
- <span data-ttu-id="b2799-148">%windir% \\ system32 \\msinfo32.exe /report %temp% \\ MDMDiagnostics \\ msinfo32.log</span><span class="sxs-lookup"><span data-stu-id="b2799-148">%windir%\\system32\\msinfo32.exe /report %temp%\\MDMDiagnostics\\msinfo32.log</span></span>
- <span data-ttu-id="b2799-149">%windir% \\ system32 \\netsh.exe advfirewall show allprofiles</span><span class="sxs-lookup"><span data-stu-id="b2799-149">%windir%\\system32\\netsh.exe advfirewall show allprofiles</span></span>
- <span data-ttu-id="b2799-150">%windir% \\ system32 \\netsh.exe advfirewall show global</span><span class="sxs-lookup"><span data-stu-id="b2799-150">%windir%\\system32\\netsh.exe advfirewall show global</span></span>
- <span data-ttu-id="b2799-151">%windir% \\ system32 \\netsh.exe lan show profiles</span><span class="sxs-lookup"><span data-stu-id="b2799-151">%windir%\\system32\\netsh.exe lan show profiles</span></span>
- <span data-ttu-id="b2799-152">%windir% \\ system32 \\netsh.exe winhttp show proxy</span><span class="sxs-lookup"><span data-stu-id="b2799-152">%windir%\\system32\\netsh.exe winhttp show proxy</span></span>
- <span data-ttu-id="b2799-153">%windir% \\ system32 \\netsh.exe wlan show profiles</span><span class="sxs-lookup"><span data-stu-id="b2799-153">%windir%\\system32\\netsh.exe wlan show profiles</span></span>
- <span data-ttu-id="b2799-154">%windir% \\ system32 \\netsh.exe wlan show wlanreport</span><span class="sxs-lookup"><span data-stu-id="b2799-154">%windir%\\system32\\netsh.exe wlan show wlanreport</span></span>
- <span data-ttu-id="b2799-155">%windir% \\ system32 \\ping.exe -n 50 localhost</span><span class="sxs-lookup"><span data-stu-id="b2799-155">%windir%\\system32\\ping.exe -n 50 localhost</span></span>
- <span data-ttu-id="b2799-156">%windir% \\ system32 \\powercfg.exe /batteryreport /output %temp% \\ MDMDiagnostics \\battery-report.html</span><span class="sxs-lookup"><span data-stu-id="b2799-156">%windir%\\system32\\powercfg.exe /batteryreport /output %temp%\\MDMDiagnostics\\battery-report.html</span></span>
- <span data-ttu-id="b2799-157">%windir% \\ system32 \\powercfg.exe /energy /output %temp% \\ MDMDiagnostics \\energy-report.html</span><span class="sxs-lookup"><span data-stu-id="b2799-157">%windir%\\system32\\powercfg.exe /energy /output %temp%\\MDMDiagnostics\\energy-report.html</span></span>
- <span data-ttu-id="b2799-158">bitsadmin /list /allusers /verbose</span><span class="sxs-lookup"><span data-stu-id="b2799-158">bitsadmin /list /allusers /verbose</span></span>
- <span data-ttu-id="b2799-159">fltMC.exe</span><span class="sxs-lookup"><span data-stu-id="b2799-159">fltMC.exe</span></span>
- <span data-ttu-id="b2799-160">bcdedit /enum all /v</span><span class="sxs-lookup"><span data-stu-id="b2799-160">bcdedit /enum all /v</span></span>
- <span data-ttu-id="b2799-161">manage-bde -protectors -get</span><span class="sxs-lookup"><span data-stu-id="b2799-161">manage-bde -protectors -get</span></span>
- <span data-ttu-id="b2799-162">Windows PowerShell commande :</span><span class="sxs-lookup"><span data-stu-id="b2799-162">Windows PowerShell commands:</span></span>
    - <span data-ttu-id="b2799-163">Get-appxpackage -allusers</span><span class="sxs-lookup"><span data-stu-id="b2799-163">Get-appxpackage -allusers</span></span>
    - <span data-ttu-id="b2799-164">Get-appxpackage -packagetype bundle</span><span class="sxs-lookup"><span data-stu-id="b2799-164">Get-appxpackage -packagetype bundle</span></span>
    - <span data-ttu-id="b2799-165">Get-Service wuauserv</span><span class="sxs-lookup"><span data-stu-id="b2799-165">Get-Service wuauserv</span></span>
    - <span data-ttu-id="b2799-166">Get-NetFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b2799-166">Get-NetFirewallRule</span></span>
    - <span data-ttu-id="b2799-167">Get-WmiObject -Class win32 \_ product</span><span class="sxs-lookup"><span data-stu-id="b2799-167">Get-WmiObject -Class win32\_product</span></span>
    - <span data-ttu-id="b2799-168">Get-ComputerInfo</span><span class="sxs-lookup"><span data-stu-id="b2799-168">Get-ComputerInfo</span></span>
    - <span data-ttu-id="b2799-169">Get-Service</span><span class="sxs-lookup"><span data-stu-id="b2799-169">Get-Service</span></span>
    - <span data-ttu-id="b2799-170">Get-Process</span><span class="sxs-lookup"><span data-stu-id="b2799-170">Get-Process</span></span>
    - <span data-ttu-id="b2799-171">Get-WmiObject Win32 \_ PnPSignedDriver</span><span class="sxs-lookup"><span data-stu-id="b2799-171">Get-WmiObject Win32\_PnPSignedDriver</span></span>

### <a name="event-logs"></a><span data-ttu-id="b2799-172">Journaux d’événements</span><span class="sxs-lookup"><span data-stu-id="b2799-172">Event logs</span></span>

- <span data-ttu-id="b2799-173">Application</span><span class="sxs-lookup"><span data-stu-id="b2799-173">Application</span></span>
- <span data-ttu-id="b2799-174">Microsoft-Windows-AppLocker/EXE et DLL</span><span class="sxs-lookup"><span data-stu-id="b2799-174">Microsoft-Windows-AppLocker/EXE and DLL</span></span>
- <span data-ttu-id="b2799-175">Microsoft-Windows-AppLocker/MSI et Script</span><span class="sxs-lookup"><span data-stu-id="b2799-175">Microsoft-Windows-AppLocker/MSI and Script</span></span>
- <span data-ttu-id="b2799-176">Microsoft-Windows-AppLocker/Packaged app-Deployment</span><span class="sxs-lookup"><span data-stu-id="b2799-176">Microsoft-Windows-AppLocker/Packaged app-Deployment</span></span>
- <span data-ttu-id="b2799-177">Microsoft-Windows-AppLocker/Packaged app-Execution</span><span class="sxs-lookup"><span data-stu-id="b2799-177">Microsoft-Windows-AppLocker/Packaged app-Execution</span></span>
- <span data-ttu-id="b2799-178">Microsoft-Windows-Bitlocker/Bitlocker Management</span><span class="sxs-lookup"><span data-stu-id="b2799-178">Microsoft-Windows-Bitlocker/Bitlocker Management</span></span>
- <span data-ttu-id="b2799-179">Microsoft-Windows-SENSE/Opérationnel</span><span class="sxs-lookup"><span data-stu-id="b2799-179">Microsoft-Windows-SENSE/Operational</span></span>
- <span data-ttu-id="b2799-180">Microsoft-Windows-SenseIR/Opérationnel</span><span class="sxs-lookup"><span data-stu-id="b2799-180">Microsoft-Windows-SenseIR/Operational</span></span>
- <span data-ttu-id="b2799-181">Configuration</span><span class="sxs-lookup"><span data-stu-id="b2799-181">Setup</span></span>
- <span data-ttu-id="b2799-182">Système</span><span class="sxs-lookup"><span data-stu-id="b2799-182">System</span></span>

### <a name="files"></a><span data-ttu-id="b2799-183">Fichiers</span><span class="sxs-lookup"><span data-stu-id="b2799-183">Files</span></span>

- <span data-ttu-id="b2799-184">%ProgramData% \\ Microsoft \\ DiagnosticLogCSP \\ Collectors \\ \* .etl</span><span class="sxs-lookup"><span data-stu-id="b2799-184">%ProgramData%\\Microsoft\\DiagnosticLogCSP\\Collectors\\\*.etl</span></span>
- <span data-ttu-id="b2799-185">%ProgramData% \\ Microsoft \\ IntuneManagementExtension \\ Logs \\ \* .\*</span><span class="sxs-lookup"><span data-stu-id="b2799-185">%ProgramData%\\Microsoft\\IntuneManagementExtension\\Logs\\\*.\*</span></span>
- <span data-ttu-id="b2799-186">%ProgramData% \\ Prise en charge Windows Defender Microsoft \\ \\MpSupportFiles.cab \\</span><span class="sxs-lookup"><span data-stu-id="b2799-186">%ProgramData%\\Microsoft\\Windows Defender\\Support\\MpSupportFiles.cab</span></span>
- <span data-ttu-id="b2799-187">%ProgramData% \\ Microsoft \\ Windows \\ WlanReport \\wlan-report-latest.html</span><span class="sxs-lookup"><span data-stu-id="b2799-187">%ProgramData%\\Microsoft\\Windows\\WlanReport\\wlan-report-latest.html</span></span>
- <span data-ttu-id="b2799-188">%ProgramData% \\ Microsoft \\ Windows \\ WlanReport -SourceFileName wlan-report-latest.html</span><span class="sxs-lookup"><span data-stu-id="b2799-188">%ProgramData%\\Microsoft\\Windows\\WlanReport -SourceFileName wlan-report-latest.html</span></span>
- <span data-ttu-id="b2799-189">%windir% \\ ccm \\ logs \* .log</span><span class="sxs-lookup"><span data-stu-id="b2799-189">%windir%\\ccm\\logs\*.log</span></span>
- <span data-ttu-id="b2799-190">%windir% \\ ccmsetup \\ logs \* .log</span><span class="sxs-lookup"><span data-stu-id="b2799-190">%windir%\\ccmsetup\\logs\*.log</span></span>
- <span data-ttu-id="b2799-191">%windir% \\ enregistre \\ CBS \\ cbs.log</span><span class="sxs-lookup"><span data-stu-id="b2799-191">%windir%\\logs\\CBS\\cbs.log</span></span>
- <span data-ttu-id="b2799-192">%windir% \\ logs \\ measuredboot \* .\*</span><span class="sxs-lookup"><span data-stu-id="b2799-192">%windir%\\logs\\measuredboot\*.\*</span></span>
- <span data-ttu-id="b2799-193">%windir% \\ Logs \\ WindowsUpdate \* .etl</span><span class="sxs-lookup"><span data-stu-id="b2799-193">%windir%\\Logs\\WindowsUpdate\*.etl</span></span>
- <span data-ttu-id="b2799-194">%windir% \\ inf \\ \* .log</span><span class="sxs-lookup"><span data-stu-id="b2799-194">%windir%\\inf\\\*.log</span></span>
- <span data-ttu-id="b2799-195">%windir% \\ servicing \\ sessions \\ActionList.xml</span><span class="sxs-lookup"><span data-stu-id="b2799-195">%windir%\\servicing\\sessions\\ActionList.xml</span></span>
- <span data-ttu-id="b2799-196">%windir% \\ servicing \\ sessions \\Sessions.xml</span><span class="sxs-lookup"><span data-stu-id="b2799-196">%windir%\\servicing\\sessions\\Sessions.xml</span></span>
- <span data-ttu-id="b2799-197">%windir% \\ SoftwareDistribution \\ DataStore \\ Logs \\ edb.log</span><span class="sxs-lookup"><span data-stu-id="b2799-197">%windir%\\SoftwareDistribution\\DataStore\\Logs\\edb.log</span></span>
- <span data-ttu-id="b2799-198">%windir% \\ SoftwareDistribution \\ DataStore \\ DataStore.edb</span><span class="sxs-lookup"><span data-stu-id="b2799-198">%windir%\\SoftwareDistribution\\DataStore\\DataStore.edb</span></span>
- <span data-ttu-id="b2799-199">%windir% \\ logs \\ dism \\ dism.log</span><span class="sxs-lookup"><span data-stu-id="b2799-199">%windir%\\logs\\dism\\dism.log</span></span>
- <span data-ttu-id="b2799-200">%SystemRoot% \\ System32 \\ Winevt \\ Logs</span><span class="sxs-lookup"><span data-stu-id="b2799-200">%SystemRoot%\\System32\\Winevt\\Logs</span></span>\\
- <span data-ttu-id="b2799-201">%appdata% \\ Microsoft \\ Teams \\ media-stack \\ \* .blog</span><span class="sxs-lookup"><span data-stu-id="b2799-201">%appdata%\\Microsoft\\Teams\\media-stack\\\*.blog</span></span>
- <span data-ttu-id="b2799-202">%appdata% \\ Microsoft \\ Teams \\ skylib \\ \* .blog</span><span class="sxs-lookup"><span data-stu-id="b2799-202">%appdata%\\Microsoft\\Teams\\skylib\\\*.blog</span></span>
- <span data-ttu-id="b2799-203">%appdata% \\ Microsoft \\ Teams \\ media-stack \\ \* .etl</span><span class="sxs-lookup"><span data-stu-id="b2799-203">%appdata%\\Microsoft\\Teams\\media-stack\\\*.etl</span></span>
- <span data-ttu-id="b2799-204">%appdata% \\ Microsoft \\ Teams \\logs.txt</span><span class="sxs-lookup"><span data-stu-id="b2799-204">%appdata%\\Microsoft\\Teams\\logs.txt</span></span>
- <span data-ttu-id="b2799-205">%windir% \\ Windows \\ System32 \\ winevt \\ \* .\*</span><span class="sxs-lookup"><span data-stu-id="b2799-205">%windir%\\Windows\\System32\\winevt\\\*.\*</span></span>