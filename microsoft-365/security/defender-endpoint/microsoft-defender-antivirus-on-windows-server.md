---
title: Antivirus Microsoft Defender sur Windows Server
description: Découvrez comment activer et configurer l’Antivirus Microsoft Defender sur Windows Server 2016 et Windows Server 2019.
keywords: windows defender, serveur, scep, system center endpoint protection, server 2016, current branch, server 2012
search.product: eADQiWindows 10XVcnh
ms.pagetype: security
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.reviewer: pahuijbr, shwjha
manager: dansimp
ms.technology: mde
ms.topic: article
ms.date: 04/23/2021
ms.openlocfilehash: 175b06738b8c1508dab68c1e19648aa5385a7137
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52269491"
---
# <a name="microsoft-defender-antivirus-on-windows-server"></a><span data-ttu-id="4004b-104">Antivirus Microsoft Defender sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="4004b-104">Microsoft Defender Antivirus on Windows Server</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="4004b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4004b-105">**Applies to:**</span></span>

- [<span data-ttu-id="4004b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4004b-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="4004b-107">L’Antivirus Microsoft Defender est disponible sur les éditions/versions suivantes de Windows Server :</span><span class="sxs-lookup"><span data-stu-id="4004b-107">Microsoft Defender Antivirus is available on the following editions/versions of Windows Server:</span></span>
- <span data-ttu-id="4004b-108">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="4004b-108">Windows Server 2019</span></span>
- <span data-ttu-id="4004b-109">Windows Server, version 1803 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4004b-109">Windows Server, version  1803 or later</span></span>
- <span data-ttu-id="4004b-110">Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4004b-110">Windows Server 2016.</span></span> 

<span data-ttu-id="4004b-111">Dans certains cas, l’Antivirus Microsoft Defender est appelé *Endpoint Protection*; toutefois, le moteur de protection est le même.</span><span class="sxs-lookup"><span data-stu-id="4004b-111">In some instances, Microsoft Defender Antivirus is referred to as *Endpoint Protection*; however, the protection engine is the same.</span></span> <span data-ttu-id="4004b-112">Bien que les fonctionnalités, la configuration et la gestion soient en grande partie identiques pour l’Antivirus Microsoft Defender sur [Windows 10,](microsoft-defender-antivirus-in-windows-10.md)il existe quelques différences clés sur Windows Server :</span><span class="sxs-lookup"><span data-stu-id="4004b-112">Although the functionality, configuration, and management are largely the same for [Microsoft Defender Antivirus on Windows 10](microsoft-defender-antivirus-in-windows-10.md), there are a few key differences on Windows Server:</span></span>

- <span data-ttu-id="4004b-113">Sur Windows Server, [les exclusions automatiques](configure-server-exclusions-microsoft-defender-antivirus.md) sont appliquées en fonction de votre rôle serveur défini.</span><span class="sxs-lookup"><span data-stu-id="4004b-113">On Windows Server, [automatic exclusions](configure-server-exclusions-microsoft-defender-antivirus.md) are applied based on your defined Server Role.</span></span>
 
- <span data-ttu-id="4004b-114">Sur Windows Server, si vous exécutez une solution antivirus/anti-programme malveillant non Microsoft, l’Antivirus Microsoft Defender ne passe pas en mode passif ou désactivé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4004b-114">On Windows Server, if you are running a non-Microsoft antivirus/antimalware solution, Microsoft Defender Antivirus does not go into either passive mode or disabled mode automatically.</span></span> <span data-ttu-id="4004b-115">Toutefois, vous pouvez définir l’Antivirus Microsoft Defender en mode passif ou désactivé manuellement.</span><span class="sxs-lookup"><span data-stu-id="4004b-115">However, you can set Microsoft Defender Antivirus to passive or disabled mode manually.</span></span>

## <a name="setting-up-microsoft-defender-antivirus-on-windows-server"></a><span data-ttu-id="4004b-116">Configuration de l’Antivirus Microsoft Defender sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="4004b-116">Setting up Microsoft Defender Antivirus on Windows Server</span></span>

<span data-ttu-id="4004b-117">Le processus de configuration et d’exécution de l’Antivirus Microsoft Defender sur une plateforme de serveur comprend plusieurs étapes :</span><span class="sxs-lookup"><span data-stu-id="4004b-117">The process of setting up and running Microsoft Defender Antivirus on a server platform includes several steps:</span></span>

1. <span data-ttu-id="4004b-118">[Activez l’interface.](#enable-the-user-interface-on-windows-server)</span><span class="sxs-lookup"><span data-stu-id="4004b-118">[Enable the interface](#enable-the-user-interface-on-windows-server).</span></span>
2. <span data-ttu-id="4004b-119">[Installez l’Antivirus Microsoft Defender.](#install-microsoft-defender-antivirus-on-windows-server)</span><span class="sxs-lookup"><span data-stu-id="4004b-119">[Install Microsoft Defender Antivirus](#install-microsoft-defender-antivirus-on-windows-server).</span></span>
3. <span data-ttu-id="4004b-120">[Vérifiez que l’Antivirus Microsoft Defender est en cours d’exécution.](#verify-microsoft-defender-antivirus-is-running)</span><span class="sxs-lookup"><span data-stu-id="4004b-120">[Verify Microsoft Defender Antivirus is running](#verify-microsoft-defender-antivirus-is-running).</span></span>
4. <span data-ttu-id="4004b-121">[Mettez à jour votre intelligence de sécurité anti-programme malveillant.](#update-antimalware-security-intelligence)</span><span class="sxs-lookup"><span data-stu-id="4004b-121">[Update your antimalware Security intelligence](#update-antimalware-security-intelligence).</span></span>
5. <span data-ttu-id="4004b-122">(Selon les besoins) [Envoyer des exemples.](#submit-samples)</span><span class="sxs-lookup"><span data-stu-id="4004b-122">(As needed) [Submit samples](#submit-samples).</span></span>
6. <span data-ttu-id="4004b-123">(Selon les besoins) [Configurer les exclusions automatiques.](#configure-automatic-exclusions)</span><span class="sxs-lookup"><span data-stu-id="4004b-123">(As needed) [Configure automatic exclusions](#configure-automatic-exclusions).</span></span>
7. <span data-ttu-id="4004b-124">(Uniquement si nécessaire) [Définissez l’Antivirus Microsoft Defender sur le mode passif.](#need-to-set-microsoft-defender-antivirus-to-passive-mode)</span><span class="sxs-lookup"><span data-stu-id="4004b-124">(Only if necessary) [Set Microsoft Defender Antivirus to passive mode](#need-to-set-microsoft-defender-antivirus-to-passive-mode).</span></span>

## <a name="enable-the-user-interface-on-windows-server"></a><span data-ttu-id="4004b-125">Activer l’interface utilisateur sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="4004b-125">Enable the user interface on Windows Server</span></span>

<span data-ttu-id="4004b-126">Par défaut, l’Antivirus Microsoft Defender est installé et fonctionnel sur Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4004b-126">By default, Microsoft Defender Antivirus is installed and functional on Windows Server.</span></span> <span data-ttu-id="4004b-127">Parfois, l’interface utilisateur (GUI) est installée par défaut, mais l’interface utilisateur graphique n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="4004b-127">Sometimes, the user interface (GUI) is installed by default, but the GUI is not required.</span></span> <span data-ttu-id="4004b-128">Vous pouvez utiliser PowerShell, une stratégie de groupe ou d’autres méthodes pour gérer l’Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4004b-128">You can use PowerShell, Group Policy, or other methods to manage Microsoft Defender Antivirus.</span></span> 

<span data-ttu-id="4004b-129">Si l’interface graphique graphique n’est pas installée sur  votre serveur et que vous souhaitez l’installer, l’Assistant Ajout de rôles et de fonctionnalités ou les cmdlets PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4004b-129">If the GUI is not installed on your server, and you want to install it, either the **Add Roles and Features** wizard or PowerShell cmdlets.</span></span>

### <a name="turn-on-the-gui-using-the-add-roles-and-features-wizard"></a><span data-ttu-id="4004b-130">Activer l’interface graphique à l’aide de l’Assistant Ajout de rôles et de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="4004b-130">Turn on the GUI using the Add Roles and Features Wizard</span></span>

1. <span data-ttu-id="4004b-131">Voir [Installer des rôles, des services de rôles](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#install-roles-role-services-and-features-by-using-the-add-roles-and-features-wizard)et des fonctionnalités à l’aide de l’Assistant Ajout de rôles et de fonctionnalités et utiliser l’Assistant Ajout de **rôles et de fonctionnalités.**</span><span class="sxs-lookup"><span data-stu-id="4004b-131">See [Install roles, role services, and features by using the add Roles and Features Wizard](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#install-roles-role-services-and-features-by-using-the-add-roles-and-features-wizard), and use the **Add Roles and Features Wizard**.</span></span>

2. <span data-ttu-id="4004b-132">Lorsque vous arrivez à l’étape **Fonctionnalités** de l’Assistant, sous Windows Defender **fonctionnalités,** sélectionnez l’interface graphique graphique pour **Windows Defender’option.**</span><span class="sxs-lookup"><span data-stu-id="4004b-132">When you get to the **Features** step of the wizard, under **Windows Defender Features**, select the **GUI for Windows Defender** option.</span></span>

   <span data-ttu-id="4004b-133">Dans Windows Server 2016, l’Assistant Ajout de rôles et de **fonctionnalités** se présente comme ceci :</span><span class="sxs-lookup"><span data-stu-id="4004b-133">In Windows Server 2016, the **Add Roles and Features Wizard** looks like this:</span></span>

   ![Assistant Ajout de rôles et de fonctionnalités affichant l’interface graphique graphique Windows Defender’option](images/server-add-gui.png)

   <span data-ttu-id="4004b-135">Dans Windows Server 2019, l’Assistant Ajout de rôles et de **fonctionnalités** est similaire.</span><span class="sxs-lookup"><span data-stu-id="4004b-135">In Windows Server 2019, the **Add Roles and Feature Wizard** is similar.</span></span>

### <a name="turn-on-the-gui-using-powershell"></a><span data-ttu-id="4004b-136">Activer l’interface graphique graphique à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="4004b-136">Turn on the GUI using PowerShell</span></span>

<span data-ttu-id="4004b-137">L’cmdlet PowerShell suivante active l’interface :</span><span class="sxs-lookup"><span data-stu-id="4004b-137">The following PowerShell cmdlet will enable the interface:</span></span> 

```PowerShell
Install-WindowsFeature -Name Windows-Defender-GUI
```

## <a name="install-microsoft-defender-antivirus-on-windows-server"></a><span data-ttu-id="4004b-138">Installer l’Antivirus Microsoft Defender sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="4004b-138">Install Microsoft Defender Antivirus on Windows Server</span></span>

<span data-ttu-id="4004b-139">Si vous devez installer ou réinstaller l’Antivirus Microsoft Defender sur Windows Server, vous pouvez le faire à l’aide de l’Assistant Ajout de rôles et de fonctionnalités **ou** de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4004b-139">If you need to install or reinstall Microsoft Defender Antivirus on Windows Server, you can do that using either the **Add Roles and Features Wizard** or PowerShell.</span></span>

### <a name="use-the-add-roles-and-features-wizard-to-install-microsoft-defender-antivirus"></a><span data-ttu-id="4004b-140">Utiliser l’Assistant Ajout de rôles et de fonctionnalités pour installer l’Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="4004b-140">Use the Add Roles and Features Wizard to install Microsoft Defender Antivirus</span></span>

1. <span data-ttu-id="4004b-141">[Reportez-vous à cet article](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#install-roles-role-services-and-features-by-using-the-add-roles-and-features-wizard)et utilisez l’Assistant Ajout **de rôles et de fonctionnalités.**</span><span class="sxs-lookup"><span data-stu-id="4004b-141">Refer to [this article](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#install-roles-role-services-and-features-by-using-the-add-roles-and-features-wizard), and use the **Add Roles and Features Wizard**.</span></span>

2. <span data-ttu-id="4004b-142">Lorsque vous arrivez à l’étape **Fonctionnalités** de l’Assistant, sélectionnez l’option Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4004b-142">When you get to the **Features** step of the wizard, select the Microsoft Defender Antivirus option.</span></span> <span data-ttu-id="4004b-143">Sélectionnez également **l’interface graphique graphique Windows Defender** option.</span><span class="sxs-lookup"><span data-stu-id="4004b-143">Also select the **GUI for Windows Defender** option.</span></span>

### <a name="use-powershell-to-install-microsoft-defender-antivirus"></a><span data-ttu-id="4004b-144">Utiliser PowerShell pour installer l’Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="4004b-144">Use PowerShell to install Microsoft Defender Antivirus</span></span>

<span data-ttu-id="4004b-145">Pour utiliser PowerShell afin d’installer l’Antivirus Microsoft Defender, exécutez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="4004b-145">To use PowerShell to install Microsoft Defender Antivirus, run the following cmdlet:</span></span>

```PowerShell
Install-WindowsFeature -Name Windows-Defender
```

<span data-ttu-id="4004b-146">Les messages d’événement pour le moteur anti-programme malveillant inclus avec l’Antivirus Microsoft Defender sont disponibles dans les événements [de l’Antivirus Microsoft Defender.](troubleshoot-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="4004b-146">Event messages for the antimalware engine included with Microsoft Defender Antivirus can be found in [Microsoft Defender AV Events](troubleshoot-microsoft-defender-antivirus.md).</span></span>


## <a name="verify-microsoft-defender-antivirus-is-running"></a><span data-ttu-id="4004b-147">Vérifier que l’Antivirus Microsoft Defender est en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="4004b-147">Verify Microsoft Defender Antivirus is running</span></span>

<span data-ttu-id="4004b-148">Une fois l’Antivirus Microsoft Defender installé, l’étape suivante consiste à vérifier qu’il est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4004b-148">Once Microsoft Defender Antivirus is installed, your next step is to verify that it's running.</span></span> <span data-ttu-id="4004b-149">Sur votre point de terminaison Windows Server, exécutez l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="4004b-149">On your Windows Server endpoint, run the following PowerShell cmdlet:</span></span>

```PowerShell
Get-Service -Name windefend
```

<span data-ttu-id="4004b-150">Pour vérifier que la protection pare-feu est allumée, exécutez l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="4004b-150">To verify that firewall protection is turned on, run the following PowerShell cmdlet:</span></span>

```PowerShell 
Get-Service -Name mpssvc
```

<span data-ttu-id="4004b-151">En remplacement de PowerShell, vous pouvez utiliser l’invite de commandes pour vérifier que l’Antivirus Microsoft Defender est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4004b-151">As an alternative to PowerShell, you can use Command Prompt to verify that Microsoft Defender Antivirus is running.</span></span> <span data-ttu-id="4004b-152">Pour ce faire, exécutez la commande suivante à partir d’une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="4004b-152">To do that, run the following command from a command prompt:</span></span> 

```console
sc query Windefend
```

<span data-ttu-id="4004b-153">La `sc query` commande retourne des informations sur le service Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4004b-153">The `sc query` command returns information about the Microsoft Defender Antivirus service.</span></span> <span data-ttu-id="4004b-154">Lorsque l’Antivirus Microsoft Defender est en cours d’exécution, `STATE` la valeur s’affiche. `RUNNING`</span><span class="sxs-lookup"><span data-stu-id="4004b-154">When Microsoft Defender Antivirus is running, the `STATE` value displays `RUNNING`.</span></span>

## <a name="update-antimalware-security-intelligence"></a><span data-ttu-id="4004b-155">Mettre à jour l’intelligence de sécurité contre les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="4004b-155">Update antimalware Security intelligence</span></span> 

<span data-ttu-id="4004b-156">Pour obtenir des informations de sécurité contre les programmes malveillants mises à jour, le service Windows Update doit être en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4004b-156">To get updated antimalware security intelligence, you must have the Windows Update service running.</span></span> <span data-ttu-id="4004b-157">Si vous utilisez un service de gestion des mises à jour, tel que Windows Server Update Services (WSUS), assurez-vous que les mises à jour de l’Intelligence de sécurité antivirus Microsoft Defender sont approuvées pour les ordinateurs que vous gérez.</span><span class="sxs-lookup"><span data-stu-id="4004b-157">If you use an update management service, like Windows Server Update Services (WSUS), make sure that updates for Microsoft Defender Antivirus Security intelligence are approved for the computers you manage.</span></span>

<span data-ttu-id="4004b-158">Par défaut, Windows Update ne télécharge pas et n’installe pas automatiquement les mises à jour sur Windows Server 2019 ou Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4004b-158">By default, Windows Update does not download and install updates automatically on Windows Server 2019 or Windows Server 2016.</span></span> <span data-ttu-id="4004b-159">Vous pouvez modifier cette configuration à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4004b-159">You can change this configuration by using one of the following methods:</span></span>


|<span data-ttu-id="4004b-160">Méthode</span><span class="sxs-lookup"><span data-stu-id="4004b-160">Method</span></span>  |<span data-ttu-id="4004b-161">Description</span><span class="sxs-lookup"><span data-stu-id="4004b-161">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="4004b-162">**Windows Update dans** le Panneau de contrôle</span><span class="sxs-lookup"><span data-stu-id="4004b-162">**Windows Update** in Control Panel</span></span>     |<span data-ttu-id="4004b-163">- **L’installation des mises à** jour entraîne automatiquement l’installation automatique de toutes les mises à jour, y Windows Defender mises à jour de l’intelligence de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4004b-163">- **Install updates automatically** results in all updates being automatically installed, including Windows Defender Security intelligence updates.</span></span> <br/><span data-ttu-id="4004b-164">- **Téléchargez les** mises à jour, mais laissez-moi choisir de les installer, ce qui permet à Windows Defender de télécharger et d’installer automatiquement les mises à jour security intelligence, mais les autres mises à jour ne sont pas installées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4004b-164">- **Download updates but let me choose whether to install them** allows Windows Defender to download and install Security intelligence updates automatically, but other updates are not automatically installed.</span></span>       |
|<span data-ttu-id="4004b-165">**Stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="4004b-165">**Group Policy**</span></span>     | <span data-ttu-id="4004b-166">Vous pouvez configurer et gérer Windows Update à l’aide des paramètres disponibles dans la stratégie de groupe, dans le chemin d’accès suivant : **Modèles d’administration\Composants Windows\Windows Update\Configurer** les mises à jour automatiques</span><span class="sxs-lookup"><span data-stu-id="4004b-166">You can set up and manage Windows Update by using the settings available in Group Policy, in the following path: **Administrative Templates\Windows Components\Windows Update\Configure Automatic Updates**</span></span>         |
|<span data-ttu-id="4004b-167">Clé de Registre **AUOptions**</span><span class="sxs-lookup"><span data-stu-id="4004b-167">The **AUOptions** registry key</span></span>     |<span data-ttu-id="4004b-168">Les deux valeurs suivantes permettent à Windows Update de télécharger et d’installer automatiquement les mises à jour d’informations de sécurité :</span><span class="sxs-lookup"><span data-stu-id="4004b-168">The following two values allow Windows Update to automatically download and install Security intelligence updates:</span></span> <br/><span data-ttu-id="4004b-169">- **4**  -  **Installez automatiquement les mises à jour.**</span><span class="sxs-lookup"><span data-stu-id="4004b-169">- **4** - **Install updates automatically**.</span></span> <span data-ttu-id="4004b-170">Cette valeur entraîne l’installation automatique de toutes les mises à jour, y Windows Defender mises à jour de l’intelligence de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4004b-170">This value results in all updates being automatically installed, including Windows Defender Security intelligence updates.</span></span> <br/><span data-ttu-id="4004b-171">- **3**  -  **Téléchargez les mises à jour, mais laissez-moi choisir s’il faut les installer.**</span><span class="sxs-lookup"><span data-stu-id="4004b-171">- **3** - **Download updates but let me choose whether to install them**.</span></span>  <span data-ttu-id="4004b-172">Cette valeur permet Windows Defender télécharger et installer automatiquement les mises à jour security intelligence, mais les autres mises à jour ne sont pas installées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4004b-172">This value allows Windows Defender to download and install Security intelligence updates automatically, but other updates are not automatically installed.</span></span>         |

<span data-ttu-id="4004b-173">Pour vous assurer que la protection contre les programmes malveillants est maintenue, nous vous recommandons d’activer les services suivants :</span><span class="sxs-lookup"><span data-stu-id="4004b-173">To ensure that protection from malware is maintained, we recommend that you enable the following services:</span></span>

- <span data-ttu-id="4004b-174">Service de rapport d’erreurs Windows</span><span class="sxs-lookup"><span data-stu-id="4004b-174">Windows Error Reporting service</span></span>

- <span data-ttu-id="4004b-175">Service Windows Update</span><span class="sxs-lookup"><span data-stu-id="4004b-175">Windows Update service</span></span>

<span data-ttu-id="4004b-176">Le tableau suivant répertorie les services pour l’Antivirus Microsoft Defender et les services dépendants.</span><span class="sxs-lookup"><span data-stu-id="4004b-176">The following table lists the services for Microsoft Defender Antivirus and the dependent services.</span></span>

|<span data-ttu-id="4004b-177">Nom du service</span><span class="sxs-lookup"><span data-stu-id="4004b-177">Service Name</span></span>|<span data-ttu-id="4004b-178">Emplacement du fichier</span><span class="sxs-lookup"><span data-stu-id="4004b-178">File Location</span></span>|<span data-ttu-id="4004b-179">Description</span><span class="sxs-lookup"><span data-stu-id="4004b-179">Description</span></span>|
|--------|---------|--------|
|<span data-ttu-id="4004b-180">Windows Defender Service (WinDefend)</span><span class="sxs-lookup"><span data-stu-id="4004b-180">Windows Defender Service (WinDefend)</span></span>|`C:\Program Files\Windows Defender\MsMpEng.exe`|<span data-ttu-id="4004b-181">Il s’agit du service antivirus Microsoft Defender principal qui doit être en cours d’exécution en permanence.</span><span class="sxs-lookup"><span data-stu-id="4004b-181">This is the main Microsoft Defender Antivirus service that needs to be running at all times.</span></span>|
|<span data-ttu-id="4004b-182">Service de rapport d’erreurs Windows (Wersvc)</span><span class="sxs-lookup"><span data-stu-id="4004b-182">Windows Error Reporting Service (Wersvc)</span></span>|`C:\WINDOWS\System32\svchost.exe -k WerSvcGroup`|<span data-ttu-id="4004b-183">Ce service renvoie des rapports d’erreur à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4004b-183">This service sends error reports back to Microsoft.</span></span>|
|<span data-ttu-id="4004b-184">Windows Defender Pare-feu (MpsSvc)</span><span class="sxs-lookup"><span data-stu-id="4004b-184">Windows Defender Firewall (MpsSvc)</span></span>|`C:\WINDOWS\system32\svchost.exe -k LocalServiceNoNetwork`|<span data-ttu-id="4004b-185">Nous vous recommandons de laisser le service Windows Defender pare-feu activé.</span><span class="sxs-lookup"><span data-stu-id="4004b-185">We recommend leaving the Windows Defender Firewall service enabled.</span></span>|
|<span data-ttu-id="4004b-186">Windows Update (Wuauserv)</span><span class="sxs-lookup"><span data-stu-id="4004b-186">Windows Update (Wuauserv)</span></span>|`C:\WINDOWS\system32\svchost.exe -k netsvcs`|<span data-ttu-id="4004b-187">Windows Update est nécessaire pour obtenir des mises à jour de l’intelligence de sécurité et des mises à jour du moteur anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="4004b-187">Windows Update is needed to get Security intelligence updates and antimalware engine updates</span></span>|

## <a name="submit-samples"></a><span data-ttu-id="4004b-188">Envoyer des exemples</span><span class="sxs-lookup"><span data-stu-id="4004b-188">Submit samples</span></span>

<span data-ttu-id="4004b-189">La soumission d’exemples permet à Microsoft de collecter des exemples de logiciels potentiellement malveillants.</span><span class="sxs-lookup"><span data-stu-id="4004b-189">Sample submission allows Microsoft to collect samples of potentially malicious software.</span></span> <span data-ttu-id="4004b-190">Pour assurer une protection continue et à jour, les chercheurs De Microsoft utilisent ces exemples pour analyser les activités suspectes et produire des informations de sécurité anti-programme malveillant mises à jour.</span><span class="sxs-lookup"><span data-stu-id="4004b-190">To help provide continued and up-to-date protection, Microsoft researchers use these samples to analyze suspicious activities and produce updated antimalware Security intelligence.</span></span> <span data-ttu-id="4004b-191">Nous collectons des fichiers exécutables de programme, tels que .exe et .dll fichiers.</span><span class="sxs-lookup"><span data-stu-id="4004b-191">We collect program executable files, such as .exe files and .dll files.</span></span> <span data-ttu-id="4004b-192">Nous ne collectons pas les fichiers qui contiennent des données personnelles, comme les documents Microsoft Word et les fichiers PDF.</span><span class="sxs-lookup"><span data-stu-id="4004b-192">We do not collect files that contain personal data, like Microsoft Word documents and PDF files.</span></span>

### <a name="submit-a-file"></a><span data-ttu-id="4004b-193">Envoyer un fichier</span><span class="sxs-lookup"><span data-stu-id="4004b-193">Submit a file</span></span>

1. <span data-ttu-id="4004b-194">Examinez le [guide de soumission.](/windows/security/threat-protection/intelligence/submission-guide)</span><span class="sxs-lookup"><span data-stu-id="4004b-194">Review the [submission guide](/windows/security/threat-protection/intelligence/submission-guide).</span></span>

2. <span data-ttu-id="4004b-195">Visitez le [portail de soumission d’exemples](https://www.microsoft.com/wdsi/filesubmission)et envoyez votre fichier.</span><span class="sxs-lookup"><span data-stu-id="4004b-195">Visit the [sample submission portal](https://www.microsoft.com/wdsi/filesubmission), and submit your file.</span></span>


### <a name="enable-automatic-sample-submission"></a><span data-ttu-id="4004b-196">Activer l’envoi automatique d’échantillons</span><span class="sxs-lookup"><span data-stu-id="4004b-196">Enable automatic sample submission</span></span>

<span data-ttu-id="4004b-197">Pour activer l’envoi automatique d’échantillons, démarrez une console Windows PowerShell en tant qu’administrateur et définissez les données de valeur **SubmitSamplesConsent** en fonction de l’un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4004b-197">To enable automatic sample submission, start a Windows PowerShell console as an administrator, and set the **SubmitSamplesConsent** value data according to one of the following settings:</span></span>

|<span data-ttu-id="4004b-198">Setting</span><span class="sxs-lookup"><span data-stu-id="4004b-198">Setting</span></span>  |<span data-ttu-id="4004b-199">Description</span><span class="sxs-lookup"><span data-stu-id="4004b-199">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="4004b-200">**0**  -  **Toujours invite**</span><span class="sxs-lookup"><span data-stu-id="4004b-200">**0** - **Always prompt**</span></span>     |<span data-ttu-id="4004b-201">Le service Antivirus Microsoft Defender vous invite à confirmer l’envoi de tous les fichiers requis.</span><span class="sxs-lookup"><span data-stu-id="4004b-201">The Microsoft Defender Antivirus service prompts you to confirm submission of all required files.</span></span> <span data-ttu-id="4004b-202">Il s’agit du paramètre par défaut de l’Antivirus Microsoft Defender, mais il n’est pas recommandé pour les installations sur Windows Server 2016 ou 2019 sans interface utilisateur graphique.</span><span class="sxs-lookup"><span data-stu-id="4004b-202">This is the default setting for Microsoft Defender Antivirus, but is not recommended for installations on Windows Server 2016 or 2019 without a GUI.</span></span>         |
|<span data-ttu-id="4004b-203">**1**   -  **Envoyer automatiquement des échantillons sécurisés**</span><span class="sxs-lookup"><span data-stu-id="4004b-203">**1**  - **Send safe samples automatically**</span></span>     |<span data-ttu-id="4004b-204">Le service Antivirus Microsoft Defender envoie tous les fichiers marqués comme « sûrs » et demande le reste des fichiers.</span><span class="sxs-lookup"><span data-stu-id="4004b-204">The Microsoft Defender Antivirus service sends all files marked as "safe" and prompts for the remainder of the files.</span></span>         |
|<span data-ttu-id="4004b-205">**2**  -  **Ne jamais envoyer**</span><span class="sxs-lookup"><span data-stu-id="4004b-205">**2** - **Never send**</span></span>      |<span data-ttu-id="4004b-206">Le service Antivirus Microsoft Defender n’invite pas et n’envoie aucun fichier.</span><span class="sxs-lookup"><span data-stu-id="4004b-206">The Microsoft Defender Antivirus service does not prompt and does not send any files.</span></span>         |
|<span data-ttu-id="4004b-207">**3**  -  **Envoyer tous les échantillons automatiquement**</span><span class="sxs-lookup"><span data-stu-id="4004b-207">**3** - **Send all samples automatically**</span></span>     |<span data-ttu-id="4004b-208">Le service Antivirus Microsoft Defender envoie tous les fichiers sans invite de confirmation.</span><span class="sxs-lookup"><span data-stu-id="4004b-208">The Microsoft Defender Antivirus service sends all files without a prompt for confirmation.</span></span>         |

## <a name="configure-automatic-exclusions"></a><span data-ttu-id="4004b-209">Configurer les exclusions automatiques</span><span class="sxs-lookup"><span data-stu-id="4004b-209">Configure automatic exclusions</span></span>

<span data-ttu-id="4004b-210">Pour garantir la sécurité et les performances, certaines exclusions sont automatiquement ajoutées en fonction des rôles et des fonctionnalités que vous installez lors de l’utilisation de l’Antivirus Microsoft Defender sur Windows Server 2016 ou 2019.</span><span class="sxs-lookup"><span data-stu-id="4004b-210">To help ensure security and performance, certain exclusions are automatically added based on the roles and features you install when using Microsoft Defender Antivirus on Windows Server 2016 or 2019.</span></span>

<span data-ttu-id="4004b-211">Voir [Configurer les exclusions dans l’Antivirus Microsoft Defender sur Windows Server.](configure-server-exclusions-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="4004b-211">See [Configure exclusions in Microsoft Defender Antivirus on Windows Server](configure-server-exclusions-microsoft-defender-antivirus.md).</span></span> 

## <a name="need-to-set-microsoft-defender-antivirus-to-passive-mode"></a><span data-ttu-id="4004b-212">Vous devez définir l’Antivirus Microsoft Defender sur le mode passif ?</span><span class="sxs-lookup"><span data-stu-id="4004b-212">Need to set Microsoft Defender Antivirus to passive mode?</span></span>

<span data-ttu-id="4004b-213">Si vous utilisez un produit antivirus non Microsoft comme solution antivirus principale sur Windows Server, vous devez définir l’Antivirus Microsoft Defender sur le mode passif ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="4004b-213">If you are using a non-Microsoft antivirus product as your primary antivirus solution on Windows Server, you must set Microsoft Defender Antivirus to passive mode or disabled mode.</span></span>

- <span data-ttu-id="4004b-214">Sur Windows Server, version 1803 ou plus récente, ou Windows Server 2019, vous pouvez définir l’Antivirus Microsoft Defender sur le mode passif.</span><span class="sxs-lookup"><span data-stu-id="4004b-214">On Windows Server, version 1803 or newer, or Windows Server 2019, you can set Microsoft Defender Antivirus to passive mode.</span></span>  

- <span data-ttu-id="4004b-215">Sur Windows Server 2016, l’Antivirus Microsoft Defender n’est pas pris en charge avec un produit antivirus/anti-programme malveillant non-Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4004b-215">On Windows Server 2016, Microsoft Defender Antivirus is not supported alongside a non-Microsoft antivirus/antimalware product.</span></span> <span data-ttu-id="4004b-216">Dans ce cas, vous devez définir l’Antivirus Microsoft Defender sur le mode désactivé.</span><span class="sxs-lookup"><span data-stu-id="4004b-216">In these cases, you must set Microsoft Defender Antivirus to disabled mode.</span></span>

### <a name="set-microsoft-defender-antivirus-to-passive-mode-using-powershell"></a><span data-ttu-id="4004b-217">Définir l’Antivirus Microsoft Defender en mode passif à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="4004b-217">Set Microsoft Defender Antivirus to passive mode using PowerShell</span></span>

<span data-ttu-id="4004b-218">Si vous utilisez Windows Server, version 1803 ou Windows Server 2019, vous pouvez définir l’Antivirus Microsoft Defender sur le mode passif à l’aide de l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="4004b-218">If you are using Windows Server, version 1803 or Windows Server 2019, you can set Microsoft Defender Antivirus to passive mode by using the following PowerShell cmdlet:</span></span>

`CMDLET NEEDED`

### <a name="set-microsoft-defender-antivirus-to-passive-mode-using-group-policy"></a><span data-ttu-id="4004b-219">Définir l’Antivirus Microsoft Defender en mode passif à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="4004b-219">Set Microsoft Defender Antivirus to passive mode using Group Policy</span></span>

<span data-ttu-id="4004b-220">PROCÉDURE REQUISE</span><span class="sxs-lookup"><span data-stu-id="4004b-220">PROCEDURE NEEDED</span></span>

### <a name="set-microsoft-defender-antivirus-to-passive-mode-using-a-registry-key"></a><span data-ttu-id="4004b-221">Définir l’Antivirus Microsoft Defender en mode passif à l’aide d’une clé de Registre</span><span class="sxs-lookup"><span data-stu-id="4004b-221">Set Microsoft Defender Antivirus to passive mode using a registry key</span></span>

<span data-ttu-id="4004b-222">Si vous utilisez Windows Server, version 1803 ou Windows Server 2019, vous pouvez définir l’Antivirus Microsoft Defender sur le mode passif en fixant la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="4004b-222">If you are using Windows Server, version 1803 or Windows Server 2019, you can set Microsoft Defender Antivirus to passive mode by setting the following registry key:</span></span>
- <span data-ttu-id="4004b-223">Chemin d’accès : `HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection`</span><span class="sxs-lookup"><span data-stu-id="4004b-223">Path: `HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection`</span></span>
- <span data-ttu-id="4004b-224">Nom : `ForceDefenderPassiveMode`</span><span class="sxs-lookup"><span data-stu-id="4004b-224">Name: `ForceDefenderPassiveMode`</span></span>
- <span data-ttu-id="4004b-225">Type : `REG_DWORD`</span><span class="sxs-lookup"><span data-stu-id="4004b-225">Type: `REG_DWORD`</span></span>
- <span data-ttu-id="4004b-226">Valeur : `1`</span><span class="sxs-lookup"><span data-stu-id="4004b-226">Value: `1`</span></span>

### <a name="disable-microsoft-defender-antivirus-using-the-remove-roles-and-features-wizard"></a><span data-ttu-id="4004b-227">Désactiver l’Antivirus Microsoft Defender à l’aide de l’Assistant Suppression de rôles et de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="4004b-227">Disable Microsoft Defender Antivirus using the Remove Roles and Features wizard</span></span>

1. <span data-ttu-id="4004b-228">Voir [Installer ou désinstaller des rôles, des services de rôles](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#remove-roles-role-services-and-features-by-using-the-remove-roles-and-features-wizard)ou des fonctionnalités, et utiliser l’Assistant Suppression de rôles **et de fonctionnalités.**</span><span class="sxs-lookup"><span data-stu-id="4004b-228">See [Install or Uninstall Roles, Role Services, or Features](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#remove-roles-role-services-and-features-by-using-the-remove-roles-and-features-wizard), and use the **Remove Roles and Features Wizard**.</span></span> 

2. <span data-ttu-id="4004b-229">Lorsque vous arrivez à l’étape **Fonctionnalités** de l’Assistant, Windows Defender **l’option Fonctionnalités.**</span><span class="sxs-lookup"><span data-stu-id="4004b-229">When you get to the **Features** step of the wizard, clear the **Windows Defender Features** option.</span></span> 

    <span data-ttu-id="4004b-230">Si vous supprimez **Windows Defender** vous-même sous la section **Fonctionnalités Windows Defender,** vous serez invité à supprimer l’interface utilisateur graphique de l’option d’interface **Windows Defender**.</span><span class="sxs-lookup"><span data-stu-id="4004b-230">If you clear **Windows Defender** by itself under the **Windows Defender Features** section, you will be prompted to remove the interface option **GUI for Windows Defender**.</span></span> 
    
    <span data-ttu-id="4004b-231">L’Antivirus Microsoft Defender s’exécute toujours **normalement** sans l’interface utilisateur, mais l’interface utilisateur ne peut pas être activée si vous désactivez la fonctionnalité d’Windows Defender principale.</span><span class="sxs-lookup"><span data-stu-id="4004b-231">Microsoft Defender Antivirus will still run normally without the user interface, but the user interface cannot be enabled if you disable the core **Windows Defender** feature.</span></span>

### <a name="turn-off-the-microsoft-defender-antivirus-user-interface-using-powershell"></a><span data-ttu-id="4004b-232">Désactiver l’interface utilisateur de l’Antivirus Microsoft Defender à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="4004b-232">Turn off the Microsoft Defender Antivirus user interface using PowerShell</span></span>

<span data-ttu-id="4004b-233">Pour désactiver l’interface graphique de l’Antivirus Microsoft Defender, utilisez l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="4004b-233">To turn off the Microsoft Defender Antivirus GUI, use the following PowerShell cmdlet:</span></span>

```PowerShell
Uninstall-WindowsFeature -Name Windows-Defender-GUI
```

### <a name="are-you-using-windows-server-2016"></a><span data-ttu-id="4004b-234">Utilisez-vous Windows Server 2016 ?</span><span class="sxs-lookup"><span data-stu-id="4004b-234">Are you using Windows Server 2016?</span></span>

<span data-ttu-id="4004b-235">Si vous utilisez Windows Server 2016 et un logiciel anti-programme malveillant/antivirus tiers qui n’est pas proposé ou développé par Microsoft, vous devez désactiver/désinstaller l’Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4004b-235">If you are using Windows Server 2016 and a third-party antimalware/antivirus product that is not offered or developed by Microsoft, you'll need to disable/uninstall Microsoft Defender Antivirus.</span></span> 

> [!NOTE]
> <span data-ttu-id="4004b-236">Vous ne pouvez pas désinstaller l’application Sécurité Windows, mais vous pouvez désactiver l’interface avec ces instructions.</span><span class="sxs-lookup"><span data-stu-id="4004b-236">You can't uninstall the Windows Security app, but you can disable the interface with these instructions.</span></span>

<span data-ttu-id="4004b-237">L’cmdlet PowerShell suivante désinstalle l’Antivirus Microsoft Defender sur Windows Server 2016 :</span><span class="sxs-lookup"><span data-stu-id="4004b-237">The following PowerShell cmdlet uninstalls Microsoft Defender Antivirus on Windows Server 2016:</span></span>

```PowerShell
Uninstall-WindowsFeature -Name Windows-Defender
```

<span data-ttu-id="4004b-238">Pour désactiver l’Antivirus Microsoft Defender sur Windows Server 2016, utilisez l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="4004b-238">To disable Microsoft Defender Antivirus on Windows Server 2016, use the following PowerShell cmdlet:</span></span>

```PowerShell
Set-MpPreference -DisableRealtimeMonitoring $true
```

## <a name="see-also"></a><span data-ttu-id="4004b-239">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4004b-239">See also</span></span>

- [<span data-ttu-id="4004b-240">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="4004b-240">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="4004b-241">Compatibilité de l’Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="4004b-241">Microsoft Defender Antivirus compatibility</span></span>](microsoft-defender-antivirus-compatibility.md)
