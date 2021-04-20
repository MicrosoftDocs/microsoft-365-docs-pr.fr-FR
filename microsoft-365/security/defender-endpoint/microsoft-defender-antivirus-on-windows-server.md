---
title: Antivirus Microsoft Defender sur Windows Server
description: Découvrez comment activer et configurer l'Antivirus Microsoft Defender sur Windows Server 2016 et Windows Server 2019.
keywords: windows defender, serveur, scep, system center endpoint protection, server 2016, current branch, server 2012
search.product: eADQiWindows 10XVcnh
ms.pagetype: security
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.reviewer: pahuijbr, shwjha
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 50e6f9b16dbc633e75e86acdc54ac43580107ae3
ms.sourcegitcommit: 55791ddab9ae484f76b30f0470eec8a4cf7b46d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51893376"
---
# <a name="microsoft-defender-antivirus-on-windows-server"></a><span data-ttu-id="f60f1-104">Antivirus Microsoft Defender sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="f60f1-104">Microsoft Defender Antivirus on Windows Server</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f60f1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f60f1-105">**Applies to:**</span></span>

- [<span data-ttu-id="f60f1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f60f1-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="f60f1-107">L'Antivirus Microsoft Defender est disponible sur les éditions/versions suivantes de Windows Server :</span><span class="sxs-lookup"><span data-stu-id="f60f1-107">Microsoft Defender Antivirus is available on the following editions/versions of Windows Server:</span></span>
- <span data-ttu-id="f60f1-108">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="f60f1-108">Windows Server 2019</span></span>
- <span data-ttu-id="f60f1-109">Windows Server, version 1803 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="f60f1-109">Windows Server, version  1803 or later</span></span>
- <span data-ttu-id="f60f1-110">Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f60f1-110">Windows Server 2016.</span></span> 

<span data-ttu-id="f60f1-111">Dans certains cas, l'Antivirus Microsoft Defender est appelé *Endpoint Protection*; toutefois, le moteur de protection est le même.</span><span class="sxs-lookup"><span data-stu-id="f60f1-111">In some instances, Microsoft Defender Antivirus is referred to as *Endpoint Protection*; however, the protection engine is the same.</span></span> <span data-ttu-id="f60f1-112">Bien que les fonctionnalités, la configuration et la gestion soient en grande partie identiques pour l'Antivirus Microsoft Defender sur [Windows 10,](microsoft-defender-antivirus-in-windows-10.md)il existe quelques différences clés sur Windows Server :</span><span class="sxs-lookup"><span data-stu-id="f60f1-112">Although the functionality, configuration, and management are largely the same for [Microsoft Defender Antivirus on Windows 10](microsoft-defender-antivirus-in-windows-10.md), there are a few key differences on Windows Server:</span></span>

- <span data-ttu-id="f60f1-113">Dans Windows Server, les [exclusions automatiques](configure-server-exclusions-microsoft-defender-antivirus.md) sont appliquées en fonction de votre rôle serveur défini.</span><span class="sxs-lookup"><span data-stu-id="f60f1-113">In Windows Server, [automatic exclusions](configure-server-exclusions-microsoft-defender-antivirus.md) are applied based on your defined Server Role.</span></span>
- <span data-ttu-id="f60f1-114">Dans Windows Server, l'Antivirus Microsoft Defender ne se désactive pas automatiquement si vous exécutez un autre produit antivirus.</span><span class="sxs-lookup"><span data-stu-id="f60f1-114">In Windows Server, Microsoft Defender Antivirus does not automatically disable itself if you are running another antivirus product.</span></span>

## <a name="the-process-at-a-glance"></a><span data-ttu-id="f60f1-115">Le processus en un clin d’œil</span><span class="sxs-lookup"><span data-stu-id="f60f1-115">The process at a glance</span></span>

<span data-ttu-id="f60f1-116">Le processus de configuration et d'exécution de l'Antivirus Microsoft Defender sur une plateforme de serveur comprend plusieurs étapes :</span><span class="sxs-lookup"><span data-stu-id="f60f1-116">The process of setting up and running Microsoft Defender Antivirus on a server platform includes several steps:</span></span>

1. <span data-ttu-id="f60f1-117">[Activez l'interface.](#enable-the-user-interface-on-windows-server)</span><span class="sxs-lookup"><span data-stu-id="f60f1-117">[Enable the interface](#enable-the-user-interface-on-windows-server).</span></span>
2. <span data-ttu-id="f60f1-118">[Installez l'Antivirus Microsoft Defender.](#install-microsoft-defender-antivirus-on-windows-server)</span><span class="sxs-lookup"><span data-stu-id="f60f1-118">[Install Microsoft Defender Antivirus](#install-microsoft-defender-antivirus-on-windows-server).</span></span>
3. <span data-ttu-id="f60f1-119">[Vérifiez que l'Antivirus Microsoft Defender est en cours d'exécution.](#verify-microsoft-defender-antivirus-is-running)</span><span class="sxs-lookup"><span data-stu-id="f60f1-119">[Verify Microsoft Defender Antivirus is running](#verify-microsoft-defender-antivirus-is-running).</span></span>
4. <span data-ttu-id="f60f1-120">[Mettez à jour votre intelligence de sécurité anti-programme malveillant.](#update-antimalware-security-intelligence)</span><span class="sxs-lookup"><span data-stu-id="f60f1-120">[Update your antimalware Security intelligence](#update-antimalware-security-intelligence).</span></span>
5. <span data-ttu-id="f60f1-121">(Selon les besoins) [Envoyer des exemples.](#submit-samples)</span><span class="sxs-lookup"><span data-stu-id="f60f1-121">(As needed) [Submit samples](#submit-samples).</span></span>
6. <span data-ttu-id="f60f1-122">(Selon les besoins) [Configurer les exclusions automatiques.](#configure-automatic-exclusions)</span><span class="sxs-lookup"><span data-stu-id="f60f1-122">(As needed) [Configure automatic exclusions](#configure-automatic-exclusions).</span></span>
7. <span data-ttu-id="f60f1-123">(Uniquement si nécessaire) [Définissez l'Antivirus Microsoft Defender sur le mode passif.](#need-to-set-microsoft-defender-antivirus-to-passive-mode)</span><span class="sxs-lookup"><span data-stu-id="f60f1-123">(Only if necessary) [Set Microsoft Defender Antivirus to passive mode](#need-to-set-microsoft-defender-antivirus-to-passive-mode).</span></span>

## <a name="enable-the-user-interface-on-windows-server"></a><span data-ttu-id="f60f1-124">Activer l'interface utilisateur sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="f60f1-124">Enable the user interface on Windows Server</span></span>

<span data-ttu-id="f60f1-125">Par défaut, l'Antivirus Microsoft Defender est installé et fonctionnel sur Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f60f1-125">By default, Microsoft Defender Antivirus is installed and functional on Windows Server.</span></span> <span data-ttu-id="f60f1-126">L'interface utilisateur (GUI) est installée par défaut sur certaines SSO, mais elle n'est pas obligatoire, car vous pouvez utiliser PowerShell ou d'autres méthodes pour gérer l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="f60f1-126">The user interface (GUI) is installed by default on some SKUs, but is not required because you can use PowerShell or other methods to manage Microsoft Defender Antivirus.</span></span> <span data-ttu-id="f60f1-127">Si l'interface graphique graphique n'est pas installée  sur votre serveur, vous pouvez l'ajouter à l'aide de l'Assistant Ajout de rôles et de fonctionnalités, ou à l'aide des cmdlets PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f60f1-127">If the GUI is not installed on your server, you can add it by using the **Add Roles and Features** wizard, or by using PowerShell cmdlets.</span></span>

### <a name="turn-on-the-gui-using-the-add-roles-and-features-wizard"></a><span data-ttu-id="f60f1-128">Activer l'interface graphique à l'aide de l'Assistant Ajout de rôles et de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="f60f1-128">Turn on the GUI using the Add Roles and Features Wizard</span></span>

1. <span data-ttu-id="f60f1-129">Voir [Installer des rôles, des services de rôles](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#install-roles-role-services-and-features-by-using-the-add-roles-and-features-wizard)et des fonctionnalités à l'aide de l'Assistant Ajout de rôles et de fonctionnalités et utiliser l'Assistant Ajout de **rôles et de fonctionnalités.**</span><span class="sxs-lookup"><span data-stu-id="f60f1-129">See [Install roles, role services, and features by using the add Roles and Features Wizard](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#install-roles-role-services-and-features-by-using-the-add-roles-and-features-wizard), and use the **Add Roles and Features Wizard**.</span></span>

2. <span data-ttu-id="f60f1-130">Lorsque vous arrivez à l'étape **Fonctionnalités** de l'Assistant, sous Windows Defender **fonctionnalités,** sélectionnez l'interface graphique graphique pour **Windows Defender'option.**</span><span class="sxs-lookup"><span data-stu-id="f60f1-130">When you get to the **Features** step of the wizard, under **Windows Defender Features**, select the **GUI for Windows Defender** option.</span></span>

   <span data-ttu-id="f60f1-131">Dans Windows Server 2016, l'Assistant Ajout de rôles et de **fonctionnalités** se présente comme ceci :</span><span class="sxs-lookup"><span data-stu-id="f60f1-131">In Windows Server 2016, the **Add Roles and Features Wizard** looks like this:</span></span>

   ![Assistant Ajout de rôles et de fonctionnalités affichant l'interface graphique graphique Windows Defender'option](images/server-add-gui.png)

   <span data-ttu-id="f60f1-133">Dans Windows Server 2019, l'Assistant Ajout de rôles et de **fonctionnalités** est similaire.</span><span class="sxs-lookup"><span data-stu-id="f60f1-133">In Windows Server 2019, the **Add Roles and Feature Wizard** is similar.</span></span>

### <a name="turn-on-the-gui-using-powershell"></a><span data-ttu-id="f60f1-134">Activer l'interface graphique graphique à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f60f1-134">Turn on the GUI using PowerShell</span></span>

<span data-ttu-id="f60f1-135">L'cmdlet PowerShell suivante active l'interface :</span><span class="sxs-lookup"><span data-stu-id="f60f1-135">The following PowerShell cmdlet will enable the interface:</span></span> 

```PowerShell
Install-WindowsFeature -Name Windows-Defender-GUI
```

## <a name="install-microsoft-defender-antivirus-on-windows-server"></a><span data-ttu-id="f60f1-136">Installer l'Antivirus Microsoft Defender sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="f60f1-136">Install Microsoft Defender Antivirus on Windows Server</span></span>

<span data-ttu-id="f60f1-137">Vous pouvez utiliser l'Assistant Ajout de **rôles et** de fonctionnalités ou PowerShell pour installer l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="f60f1-137">You can use either the **Add Roles and Features Wizard** or PowerShell to install Microsoft Defender Antivirus.</span></span>

### <a name="use-the-add-roles-and-features-wizard"></a><span data-ttu-id="f60f1-138">Utiliser l'Assistant Ajout de rôles et de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="f60f1-138">Use the Add Roles and Features Wizard</span></span>

1. <span data-ttu-id="f60f1-139">[Reportez-vous à cet article](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#install-roles-role-services-and-features-by-using-the-add-roles-and-features-wizard)et utilisez l'Assistant Ajout **de rôles et de fonctionnalités.**</span><span class="sxs-lookup"><span data-stu-id="f60f1-139">Refer to [this article](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#install-roles-role-services-and-features-by-using-the-add-roles-and-features-wizard), and use the **Add Roles and Features Wizard**.</span></span>

2. <span data-ttu-id="f60f1-140">Lorsque vous arrivez à l'étape **Fonctionnalités** de l'Assistant, sélectionnez l'option Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="f60f1-140">When you get to the **Features** step of the wizard, select the Microsoft Defender Antivirus option.</span></span> <span data-ttu-id="f60f1-141">Sélectionnez également **l'interface graphique graphique Windows Defender** option.</span><span class="sxs-lookup"><span data-stu-id="f60f1-141">Also select the **GUI for Windows Defender** option.</span></span>

### <a name="use-powershell"></a><span data-ttu-id="f60f1-142">Utiliser PowerShell</span><span class="sxs-lookup"><span data-stu-id="f60f1-142">Use PowerShell</span></span>

<span data-ttu-id="f60f1-143">Pour utiliser PowerShell afin d'installer l'Antivirus Microsoft Defender, exécutez l'cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="f60f1-143">To use PowerShell to install Microsoft Defender Antivirus, run the following cmdlet:</span></span>

```PowerShell
Install-WindowsFeature -Name Windows-Defender
```

<span data-ttu-id="f60f1-144">Les messages d'événement pour le moteur anti-programme malveillant inclus avec l'Antivirus Microsoft Defender sont disponibles dans les événements [de l'Antivirus Microsoft Defender.](troubleshoot-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="f60f1-144">Event messages for the antimalware engine included with Microsoft Defender Antivirus can be found in [Microsoft Defender AV Events](troubleshoot-microsoft-defender-antivirus.md).</span></span>


## <a name="verify-microsoft-defender-antivirus-is-running"></a><span data-ttu-id="f60f1-145">Vérifier que l'Antivirus Microsoft Defender est en cours d'exécution</span><span class="sxs-lookup"><span data-stu-id="f60f1-145">Verify Microsoft Defender Antivirus is running</span></span>

<span data-ttu-id="f60f1-146">Pour vérifier que l'Antivirus Microsoft Defender est en cours d'exécution sur votre serveur, exécutez l'cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="f60f1-146">To verify that Microsoft Defender Antivirus is running on your server, run the following PowerShell cmdlet:</span></span>

```PowerShell
Get-Service -Name windefend
```

<span data-ttu-id="f60f1-147">Pour vérifier que la protection pare-feu est allumée, exécutez l'cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="f60f1-147">To verify that firewall protection is turned on, run the following PowerShell cmdlet:</span></span>

```PowerShell 
Get-Service -Name mpssvc
```

<span data-ttu-id="f60f1-148">En remplacement de PowerShell, vous pouvez utiliser l'invite de commandes pour vérifier que l'Antivirus Microsoft Defender est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="f60f1-148">As an alternative to PowerShell, you can use Command Prompt to verify that Microsoft Defender Antivirus is running.</span></span> <span data-ttu-id="f60f1-149">Pour ce faire, exécutez la commande suivante à partir d'une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="f60f1-149">To do that, run the following command from a command prompt:</span></span> 

```console
sc query Windefend
```

<span data-ttu-id="f60f1-150">La `sc query` commande retourne des informations sur le service Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="f60f1-150">The `sc query` command returns information about the Microsoft Defender Antivirus service.</span></span> <span data-ttu-id="f60f1-151">Lorsque l'Antivirus Microsoft Defender est en cours d'exécution, `STATE` la valeur s'affiche. `RUNNING`</span><span class="sxs-lookup"><span data-stu-id="f60f1-151">When Microsoft Defender Antivirus is running, the `STATE` value displays `RUNNING`.</span></span>

## <a name="update-antimalware-security-intelligence"></a><span data-ttu-id="f60f1-152">Mettre à jour l'intelligence de sécurité contre les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="f60f1-152">Update antimalware Security intelligence</span></span> 

<span data-ttu-id="f60f1-153">Pour obtenir des informations de sécurité contre les programmes malveillants mises à jour, le service Windows Update doit être en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="f60f1-153">To get updated antimalware security intelligence, you must have the Windows Update service running.</span></span> <span data-ttu-id="f60f1-154">Si vous utilisez un service de gestion des mises à jour, tel que Windows Server Update Services (WSUS), assurez-vous que les mises à jour de l'intelligence de sécurité antivirus Microsoft Defender sont approuvées pour les ordinateurs que vous gérez.</span><span class="sxs-lookup"><span data-stu-id="f60f1-154">If you use an update management service, like Windows Server Update Services (WSUS), make sure that updates for Microsoft Defender Antivirus Security intelligence are approved for the computers you manage.</span></span>

<span data-ttu-id="f60f1-155">Par défaut, Windows Update ne télécharge et n'installe pas automatiquement les mises à jour sur Windows Server 2019 ou Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f60f1-155">By default, Windows Update does not download and install updates automatically on Windows Server 2019 or Windows Server 2016.</span></span> <span data-ttu-id="f60f1-156">Vous pouvez modifier cette configuration à l'aide de l'une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f60f1-156">You can change this configuration by using one of the following methods:</span></span>


|<span data-ttu-id="f60f1-157">Méthode</span><span class="sxs-lookup"><span data-stu-id="f60f1-157">Method</span></span>  |<span data-ttu-id="f60f1-158">Description</span><span class="sxs-lookup"><span data-stu-id="f60f1-158">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="f60f1-159">**Windows Update dans** le Panneau de contrôle</span><span class="sxs-lookup"><span data-stu-id="f60f1-159">**Windows Update** in Control Panel</span></span>     |<span data-ttu-id="f60f1-160">- **L'installation des mises à** jour entraîne automatiquement l'installation automatique de toutes les mises à jour, y Windows Defender mises à jour de l'intelligence de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f60f1-160">- **Install updates automatically** results in all updates being automatically installed, including Windows Defender Security intelligence updates.</span></span> <br/><span data-ttu-id="f60f1-161">- **Téléchargez les** mises à jour, mais laissez-moi choisir de les installer, ce qui permet à Windows Defender de télécharger et d'installer automatiquement les mises à jour security intelligence, mais les autres mises à jour ne sont pas installées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f60f1-161">- **Download updates but let me choose whether to install them** allows Windows Defender to download and install Security intelligence updates automatically, but other updates are not automatically installed.</span></span>       |
|<span data-ttu-id="f60f1-162">**Stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="f60f1-162">**Group Policy**</span></span>     | <span data-ttu-id="f60f1-163">Vous pouvez configurer et gérer Windows Update à l'aide des paramètres disponibles dans la stratégie de groupe, dans le chemin d'accès suivant : **Modèles d'administration\Composants Windows\Windows Update\Configurer** les mises à jour automatiques</span><span class="sxs-lookup"><span data-stu-id="f60f1-163">You can set up and manage Windows Update by using the settings available in Group Policy, in the following path: **Administrative Templates\Windows Components\Windows Update\Configure Automatic Updates**</span></span>         |
|<span data-ttu-id="f60f1-164">Clé de Registre **AUOptions**</span><span class="sxs-lookup"><span data-stu-id="f60f1-164">The **AUOptions** registry key</span></span>     |<span data-ttu-id="f60f1-165">Les deux valeurs suivantes permettent à Windows Update de télécharger et d'installer automatiquement les mises à jour d'informations de sécurité :</span><span class="sxs-lookup"><span data-stu-id="f60f1-165">The following two values allow Windows Update to automatically download and install Security intelligence updates:</span></span> <br/><span data-ttu-id="f60f1-166">- **4**  -  **Installez automatiquement les mises à jour.**</span><span class="sxs-lookup"><span data-stu-id="f60f1-166">- **4** - **Install updates automatically**.</span></span> <span data-ttu-id="f60f1-167">Cette valeur entraîne l'installation automatique de toutes les mises à jour, y Windows Defender mises à jour d'informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f60f1-167">This value results in all updates being automatically installed, including Windows Defender Security intelligence updates.</span></span> <br/><span data-ttu-id="f60f1-168">- **3**  -  **Téléchargez les mises à jour, mais laissez-moi choisir s'il faut les installer.**</span><span class="sxs-lookup"><span data-stu-id="f60f1-168">- **3** - **Download updates but let me choose whether to install them**.</span></span>  <span data-ttu-id="f60f1-169">Cette valeur permet Windows Defender télécharger et installer automatiquement les mises à jour security intelligence, mais les autres mises à jour ne sont pas installées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f60f1-169">This value allows Windows Defender to download and install Security intelligence updates automatically, but other updates are not automatically installed.</span></span>         |

<span data-ttu-id="f60f1-170">Pour vous assurer que la protection contre les programmes malveillants est maintenue, nous vous recommandons d’activer les services suivants :</span><span class="sxs-lookup"><span data-stu-id="f60f1-170">To ensure that protection from malware is maintained, we recommend that you enable the following services:</span></span>

- <span data-ttu-id="f60f1-171">Service de rapport d’erreurs Windows</span><span class="sxs-lookup"><span data-stu-id="f60f1-171">Windows Error Reporting service</span></span>

- <span data-ttu-id="f60f1-172">Service Windows Update</span><span class="sxs-lookup"><span data-stu-id="f60f1-172">Windows Update service</span></span>

<span data-ttu-id="f60f1-173">Le tableau suivant répertorie les services pour l’Antivirus Microsoft Defender et les services dépendants.</span><span class="sxs-lookup"><span data-stu-id="f60f1-173">The following table lists the services for Microsoft Defender Antivirus and the dependent services.</span></span>

|<span data-ttu-id="f60f1-174">Nom du service</span><span class="sxs-lookup"><span data-stu-id="f60f1-174">Service Name</span></span>|<span data-ttu-id="f60f1-175">Emplacement du fichier</span><span class="sxs-lookup"><span data-stu-id="f60f1-175">File Location</span></span>|<span data-ttu-id="f60f1-176">Description</span><span class="sxs-lookup"><span data-stu-id="f60f1-176">Description</span></span>|
|--------|---------|--------|
|<span data-ttu-id="f60f1-177">Windows Defender Service (WinDefend)</span><span class="sxs-lookup"><span data-stu-id="f60f1-177">Windows Defender Service (WinDefend)</span></span>|`C:\Program Files\Windows Defender\MsMpEng.exe`|<span data-ttu-id="f60f1-178">Il s’agit du service antivirus Microsoft Defender principal qui doit être en cours d’exécution en permanence.</span><span class="sxs-lookup"><span data-stu-id="f60f1-178">This is the main Microsoft Defender Antivirus service that needs to be running at all times.</span></span>|
|<span data-ttu-id="f60f1-179">Service de rapport d’erreurs Windows (Wersvc)</span><span class="sxs-lookup"><span data-stu-id="f60f1-179">Windows Error Reporting Service (Wersvc)</span></span>|`C:\WINDOWS\System32\svchost.exe -k WerSvcGroup`|<span data-ttu-id="f60f1-180">Ce service renvoie des rapports d’erreur à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f60f1-180">This service sends error reports back to Microsoft.</span></span>|
|<span data-ttu-id="f60f1-181">Windows Defender Pare-feu (MpsSvc)</span><span class="sxs-lookup"><span data-stu-id="f60f1-181">Windows Defender Firewall (MpsSvc)</span></span>|`C:\WINDOWS\system32\svchost.exe -k LocalServiceNoNetwork`|<span data-ttu-id="f60f1-182">Nous vous recommandons de laisser le service Windows Defender pare-feu activé.</span><span class="sxs-lookup"><span data-stu-id="f60f1-182">We recommend leaving the Windows Defender Firewall service enabled.</span></span>|
|<span data-ttu-id="f60f1-183">Windows Update (Wuauserv)</span><span class="sxs-lookup"><span data-stu-id="f60f1-183">Windows Update (Wuauserv)</span></span>|`C:\WINDOWS\system32\svchost.exe -k netsvcs`|<span data-ttu-id="f60f1-184">Windows Update est nécessaire pour obtenir des mises à jour de l’intelligence de sécurité et des mises à jour du moteur anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="f60f1-184">Windows Update is needed to get Security intelligence updates and antimalware engine updates</span></span>|

## <a name="submit-samples"></a><span data-ttu-id="f60f1-185">Envoyer des exemples</span><span class="sxs-lookup"><span data-stu-id="f60f1-185">Submit samples</span></span>

<span data-ttu-id="f60f1-186">La soumission d’exemples permet à Microsoft de collecter des exemples de logiciels potentiellement malveillants.</span><span class="sxs-lookup"><span data-stu-id="f60f1-186">Sample submission allows Microsoft to collect samples of potentially malicious software.</span></span> <span data-ttu-id="f60f1-187">Pour assurer une protection continue et à jour, les chercheurs De Microsoft utilisent ces exemples pour analyser les activités suspectes et produire des informations de sécurité contre les programmes malveillants mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f60f1-187">To help provide continued and up-to-date protection, Microsoft researchers use these samples to analyze suspicious activities and produce updated antimalware Security intelligence.</span></span> <span data-ttu-id="f60f1-188">Nous collectons les fichiers exécutables du programme, tels que les fichiers .exe et .dll.</span><span class="sxs-lookup"><span data-stu-id="f60f1-188">We collect program executable files, such as .exe files and .dll files.</span></span> <span data-ttu-id="f60f1-189">Nous ne collectons pas les fichiers qui contiennent des données personnelles, comme les documents Microsoft Word et les fichiers PDF.</span><span class="sxs-lookup"><span data-stu-id="f60f1-189">We do not collect files that contain personal data, like Microsoft Word documents and PDF files.</span></span>

### <a name="submit-a-file"></a><span data-ttu-id="f60f1-190">Envoyer un fichier</span><span class="sxs-lookup"><span data-stu-id="f60f1-190">Submit a file</span></span>

1. <span data-ttu-id="f60f1-191">Examinez le [guide de soumission.](/windows/security/threat-protection/intelligence/submission-guide)</span><span class="sxs-lookup"><span data-stu-id="f60f1-191">Review the [submission guide](/windows/security/threat-protection/intelligence/submission-guide).</span></span>

2. <span data-ttu-id="f60f1-192">Visitez le [portail de soumission d'exemples](https://www.microsoft.com/wdsi/filesubmission)et envoyez votre fichier.</span><span class="sxs-lookup"><span data-stu-id="f60f1-192">Visit the [sample submission portal](https://www.microsoft.com/wdsi/filesubmission), and submit your file.</span></span>


### <a name="enable-automatic-sample-submission"></a><span data-ttu-id="f60f1-193">Activer l'envoi automatique d'échantillons</span><span class="sxs-lookup"><span data-stu-id="f60f1-193">Enable automatic sample submission</span></span>

<span data-ttu-id="f60f1-194">Pour activer l'envoi automatique d'échantillons, démarrez une console Windows PowerShell en tant qu'administrateur et définissez les données de valeur **SubmitSamplesConsent** en fonction de l'un des paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f60f1-194">To enable automatic sample submission, start a Windows PowerShell console as an administrator, and set the **SubmitSamplesConsent** value data according to one of the following settings:</span></span>

|<span data-ttu-id="f60f1-195">Setting</span><span class="sxs-lookup"><span data-stu-id="f60f1-195">Setting</span></span>  |<span data-ttu-id="f60f1-196">Description</span><span class="sxs-lookup"><span data-stu-id="f60f1-196">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="f60f1-197">**0**  -  **Toujours invite**</span><span class="sxs-lookup"><span data-stu-id="f60f1-197">**0** - **Always prompt**</span></span>     |<span data-ttu-id="f60f1-198">Le service Antivirus Microsoft Defender vous invite à confirmer l'envoi de tous les fichiers requis.</span><span class="sxs-lookup"><span data-stu-id="f60f1-198">The Microsoft Defender Antivirus service prompts you to confirm submission of all required files.</span></span> <span data-ttu-id="f60f1-199">Il s'agit du paramètre par défaut de l'Antivirus Microsoft Defender, mais il n'est pas recommandé pour les installations sur Windows Server 2016 ou 2019 sans interface utilisateur graphique.</span><span class="sxs-lookup"><span data-stu-id="f60f1-199">This is the default setting for Microsoft Defender Antivirus, but is not recommended for installations on Windows Server 2016 or 2019 without a GUI.</span></span>         |
|<span data-ttu-id="f60f1-200">**1**   -  **Envoyer automatiquement des échantillons sécurisés**</span><span class="sxs-lookup"><span data-stu-id="f60f1-200">**1**  - **Send safe samples automatically**</span></span>     |<span data-ttu-id="f60f1-201">Le service Antivirus Microsoft Defender envoie tous les fichiers marqués comme « sûrs » et demande le reste des fichiers.</span><span class="sxs-lookup"><span data-stu-id="f60f1-201">The Microsoft Defender Antivirus service sends all files marked as "safe" and prompts for the remainder of the files.</span></span>         |
|<span data-ttu-id="f60f1-202">**2**  -  **Ne jamais envoyer**</span><span class="sxs-lookup"><span data-stu-id="f60f1-202">**2** - **Never send**</span></span>      |<span data-ttu-id="f60f1-203">Le service Antivirus Microsoft Defender n'invite pas et n'envoie aucun fichier.</span><span class="sxs-lookup"><span data-stu-id="f60f1-203">The Microsoft Defender Antivirus service does not prompt and does not send any files.</span></span>         |
|<span data-ttu-id="f60f1-204">**3**  -  **Envoyer tous les échantillons automatiquement**</span><span class="sxs-lookup"><span data-stu-id="f60f1-204">**3** - **Send all samples automatically**</span></span>     |<span data-ttu-id="f60f1-205">Le service Antivirus Microsoft Defender envoie tous les fichiers sans invite de confirmation.</span><span class="sxs-lookup"><span data-stu-id="f60f1-205">The Microsoft Defender Antivirus service sends all files without a prompt for confirmation.</span></span>         |

## <a name="configure-automatic-exclusions"></a><span data-ttu-id="f60f1-206">Configurer les exclusions automatiques</span><span class="sxs-lookup"><span data-stu-id="f60f1-206">Configure automatic exclusions</span></span>

<span data-ttu-id="f60f1-207">Pour garantir la sécurité et les performances, certaines exclusions sont automatiquement ajoutées en fonction des rôles et des fonctionnalités que vous installez lors de l'utilisation de l'Antivirus Microsoft Defender sur Windows Server 2016 ou 2019.</span><span class="sxs-lookup"><span data-stu-id="f60f1-207">To help ensure security and performance, certain exclusions are automatically added based on the roles and features you install when using Microsoft Defender Antivirus on Windows Server 2016 or 2019.</span></span>

<span data-ttu-id="f60f1-208">Voir [Configurer les exclusions dans l'Antivirus Microsoft Defender sur Windows Server.](configure-server-exclusions-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="f60f1-208">See [Configure exclusions in Microsoft Defender Antivirus on Windows Server](configure-server-exclusions-microsoft-defender-antivirus.md).</span></span> 

## <a name="need-to-set-microsoft-defender-antivirus-to-passive-mode"></a><span data-ttu-id="f60f1-209">Vous devez définir l'Antivirus Microsoft Defender sur le mode passif ?</span><span class="sxs-lookup"><span data-stu-id="f60f1-209">Need to set Microsoft Defender Antivirus to passive mode?</span></span>

<span data-ttu-id="f60f1-210">Si vous utilisez un produit antivirus non Microsoft comme solution antivirus principale, définissez l'Antivirus Microsoft Defender sur le mode passif.</span><span class="sxs-lookup"><span data-stu-id="f60f1-210">If you are using a non-Microsoft antivirus product as your primary antivirus solution, set Microsoft Defender Antivirus to passive mode.</span></span>  

### <a name="set-microsoft-defender-antivirus-to-passive-mode-using-a-registry-key"></a><span data-ttu-id="f60f1-211">Définir l'Antivirus Microsoft Defender en mode passif à l'aide d'une clé de Registre</span><span class="sxs-lookup"><span data-stu-id="f60f1-211">Set Microsoft Defender Antivirus to passive mode using a registry key</span></span>

<span data-ttu-id="f60f1-212">Si vous utilisez Windows Server, version 1803 ou Windows Server 2019, vous pouvez définir l'Antivirus Microsoft Defender sur le mode passif en fixant la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="f60f1-212">If you are using Windows Server, version 1803 or Windows Server 2019, you can set Microsoft Defender Antivirus to passive mode by setting the following registry key:</span></span>
- <span data-ttu-id="f60f1-213">Chemin d'accès : `HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection`</span><span class="sxs-lookup"><span data-stu-id="f60f1-213">Path: `HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection`</span></span>
- <span data-ttu-id="f60f1-214">Nom : `ForceDefenderPassiveMode`</span><span class="sxs-lookup"><span data-stu-id="f60f1-214">Name: `ForceDefenderPassiveMode`</span></span>
- <span data-ttu-id="f60f1-215">Type : `REG_DWORD`</span><span class="sxs-lookup"><span data-stu-id="f60f1-215">Type: `REG_DWORD`</span></span>
- <span data-ttu-id="f60f1-216">Valeur : `1`</span><span class="sxs-lookup"><span data-stu-id="f60f1-216">Value: `1`</span></span>

### <a name="disable-microsoft-defender-antivirus-using-the-remove-roles-and-features-wizard"></a><span data-ttu-id="f60f1-217">Désactiver l'Antivirus Microsoft Defender à l'aide de l'Assistant Suppression de rôles et de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="f60f1-217">Disable Microsoft Defender Antivirus using the Remove Roles and Features wizard</span></span>

1. <span data-ttu-id="f60f1-218">Voir [Installer ou désinstaller des rôles, des services de rôles](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#remove-roles-role-services-and-features-by-using-the-remove-roles-and-features-wizard)ou des fonctionnalités, et utiliser l'Assistant Suppression de rôles **et de fonctionnalités.**</span><span class="sxs-lookup"><span data-stu-id="f60f1-218">See [Install or Uninstall Roles, Role Services, or Features](/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#remove-roles-role-services-and-features-by-using-the-remove-roles-and-features-wizard), and use the **Remove Roles and Features Wizard**.</span></span> 

2. <span data-ttu-id="f60f1-219">Lorsque vous arrivez à l'étape **Fonctionnalités** de l'Assistant, Windows Defender **l'option Fonctionnalités.**</span><span class="sxs-lookup"><span data-stu-id="f60f1-219">When you get to the **Features** step of the wizard, clear the **Windows Defender Features** option.</span></span> 

    <span data-ttu-id="f60f1-220">Si vous supprimez **Windows Defender** vous-même sous la section **Fonctionnalités Windows Defender,** vous serez invité à supprimer l'interface utilisateur graphique de l'option d'interface **Windows Defender**.</span><span class="sxs-lookup"><span data-stu-id="f60f1-220">If you clear **Windows Defender** by itself under the **Windows Defender Features** section, you will be prompted to remove the interface option **GUI for Windows Defender**.</span></span> 
    
    <span data-ttu-id="f60f1-221">L'Antivirus Microsoft Defender s'exécute toujours **normalement** sans l'interface utilisateur, mais l'interface utilisateur ne peut pas être activée si vous désactivez la fonctionnalité Windows Defender principal.</span><span class="sxs-lookup"><span data-stu-id="f60f1-221">Microsoft Defender Antivirus will still run normally without the user interface, but the user interface cannot be enabled if you disable the core **Windows Defender** feature.</span></span>

### <a name="turn-off-the-microsoft-defender-antivirus-user-interface-using-powershell"></a><span data-ttu-id="f60f1-222">Désactiver l'interface utilisateur de l'Antivirus Microsoft Defender à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f60f1-222">Turn off the Microsoft Defender Antivirus user interface using PowerShell</span></span>

<span data-ttu-id="f60f1-223">Pour désactiver l'interface graphique de l'Antivirus Microsoft Defender, utilisez l'cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="f60f1-223">To turn off the Microsoft Defender Antivirus GUI, use the following PowerShell cmdlet:</span></span>

```PowerShell
Uninstall-WindowsFeature -Name Windows-Defender-GUI
```

### <a name="are-you-using-windows-server-2016"></a><span data-ttu-id="f60f1-224">Utilisez-vous Windows Server 2016 ?</span><span class="sxs-lookup"><span data-stu-id="f60f1-224">Are you using Windows Server 2016?</span></span>

<span data-ttu-id="f60f1-225">Si vous utilisez Windows Server 2016 et un produit antivirus/anti-programme malveillant tiers qui n'est pas proposé ou développé par Microsoft, vous devez désactiver/désinstaller l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="f60f1-225">If you are using Windows Server 2016 and a third-party antimalware/antivirus product that is not offered or developed by Microsoft, you'll need to disable/uninstall Microsoft Defender Antivirus.</span></span> 

> [!NOTE]
> <span data-ttu-id="f60f1-226">Vous ne pouvez pas désinstaller l'application Sécurité Windows, mais vous pouvez désactiver l'interface avec ces instructions.</span><span class="sxs-lookup"><span data-stu-id="f60f1-226">You can't uninstall the Windows Security app, but you can disable the interface with these instructions.</span></span>

<span data-ttu-id="f60f1-227">L'cmdlet PowerShell suivante désinstalle l'Antivirus Microsoft Defender sur Windows Server 2016 :</span><span class="sxs-lookup"><span data-stu-id="f60f1-227">The following PowerShell cmdlet uninstalls Microsoft Defender Antivirus on Windows Server 2016:</span></span>

```PowerShell
Uninstall-WindowsFeature -Name Windows-Defender
```

## <a name="see-also"></a><span data-ttu-id="f60f1-228">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f60f1-228">See also</span></span>

- [<span data-ttu-id="f60f1-229">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="f60f1-229">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="f60f1-230">Compatibilité de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="f60f1-230">Microsoft Defender Antivirus compatibility</span></span>](microsoft-defender-antivirus-compatibility.md)
