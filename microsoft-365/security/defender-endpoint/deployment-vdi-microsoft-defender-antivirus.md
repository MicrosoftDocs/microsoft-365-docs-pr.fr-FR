---
title: Antivirus Microsoft Defender Guide de déploiement de l’infrastructure de bureau virtuel
description: Découvrez comment déployer des Antivirus Microsoft Defender dans un environnement de bureau virtuel pour un meilleur équilibre entre la protection et les performances.
keywords: vdi, hyper-v, vm, machine virtuelle, windows defender, antivirus, av, bureau virtuel, rds, bureau à distance
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 12/28/2020
ms.reviewer: jesquive
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 4ecd14e055646804d81e22da7c192988cf1e6f6f
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52275251"
---
# <a name="deployment-guide-for-microsoft-defender-antivirus-in-a-virtual-desktop-infrastructure-vdi-environment"></a><span data-ttu-id="4d21f-104">Guide de déploiement de l’antivirus Microsoft Defender dans un environnement VDI (Virtual Desktop Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="4d21f-104">Deployment guide for Microsoft Defender Antivirus in a virtual desktop infrastructure (VDI) environment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="4d21f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4d21f-105">**Applies to:**</span></span>

- [<span data-ttu-id="4d21f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4d21f-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="4d21f-107">Outre les configurations matérielles ou locales standard, vous pouvez également utiliser Antivirus Microsoft Defender dans un environnement bureau à distance (RDS) ou vDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="4d21f-107">In addition to standard on-premises or hardware configurations, you can also use Microsoft Defender Antivirus in a remote desktop (RDS) or virtual desktop infrastructure (VDI) environment.</span></span>

<span data-ttu-id="4d21f-108">Voir [Windows virtual desktop documentation](/azure/virtual-desktop) for more details on Bureau à distance Microsoft Services and VDI support.</span><span class="sxs-lookup"><span data-stu-id="4d21f-108">See [Windows Virtual Desktop Documentation](/azure/virtual-desktop) for more details on Microsoft Remote Desktop Services and VDI support.</span></span>

<span data-ttu-id="4d21f-109">Pour les machines virtuelles basées sur Azure, voir [Installer Endpoint Protection dans Azure Defender.](/azure/security-center/security-center-install-endpoint-protection)</span><span class="sxs-lookup"><span data-stu-id="4d21f-109">For Azure-based virtual machines, see [Install Endpoint Protection in Azure Defender](/azure/security-center/security-center-install-endpoint-protection).</span></span>

<span data-ttu-id="4d21f-110">Avec la possibilité de déployer facilement des mises à jour sur des ordinateurs VM en cours d’exécution dans des VDIs, nous avons raccourci ce guide pour vous concentrer sur la façon dont vous pouvez obtenir des mises à jour sur vos ordinateurs rapidement et facilement.</span><span class="sxs-lookup"><span data-stu-id="4d21f-110">With the ability to easily deploy updates to VMs running in VDIs, we've shortened this guide to focus on how you can get updates on your machines quickly and easily.</span></span> <span data-ttu-id="4d21f-111">Vous n’avez plus besoin de créer et de sceller régulièrement des images d’or, car les mises à jour sont étendues dans leurs bits de composant sur le serveur hôte, puis téléchargées directement sur la VM lorsqu’elle est allumée.</span><span class="sxs-lookup"><span data-stu-id="4d21f-111">You no longer need to create and seal golden images on a periodic basis, as updates are expanded into their component bits on the host server and then downloaded directly to the VM when it's turned on.</span></span>

<span data-ttu-id="4d21f-112">Ce guide décrit comment configurer vos VM pour une protection et des performances optimales, notamment comment :</span><span class="sxs-lookup"><span data-stu-id="4d21f-112">This guide describes how to configure your VMs for optimal protection and performance, including how to:</span></span>

- [<span data-ttu-id="4d21f-113">Configurer un partage de fichiers VDI dédié pour les mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="4d21f-113">Set up a dedicated VDI file share for security intelligence updates</span></span>](#set-up-a-dedicated-vdi-file-share)
- [<span data-ttu-id="4d21f-114">Randomiser les analyses programmées</span><span class="sxs-lookup"><span data-stu-id="4d21f-114">Randomize scheduled scans</span></span>](#randomize-scheduled-scans)
- [<span data-ttu-id="4d21f-115">Utiliser des analyses rapides</span><span class="sxs-lookup"><span data-stu-id="4d21f-115">Use quick scans</span></span>](#use-quick-scans)
- [<span data-ttu-id="4d21f-116">Empêcher les notifications</span><span class="sxs-lookup"><span data-stu-id="4d21f-116">Prevent notifications</span></span>](#prevent-notifications)
- [<span data-ttu-id="4d21f-117">Désactiver l’analyse après chaque mise à jour</span><span class="sxs-lookup"><span data-stu-id="4d21f-117">Disable scans from occurring after every update</span></span>](#disable-scans-after-an-update)
- [<span data-ttu-id="4d21f-118">Analyser les ordinateurs ou ordinateurs hors connexion depuis un certain temps</span><span class="sxs-lookup"><span data-stu-id="4d21f-118">Scan out-of-date machines or machines that have been offline for a while</span></span>](#scan-vms-that-have-been-offline)
- [<span data-ttu-id="4d21f-119">Appliquer des exclusions</span><span class="sxs-lookup"><span data-stu-id="4d21f-119">Apply exclusions</span></span>](#exclusions)

<span data-ttu-id="4d21f-120">Vous pouvez également télécharger le Antivirus Microsoft Defender de livre blanc sur [l’infrastructure](https://demo.wd.microsoft.com/Content/wdav-testing-vdi-ssu.pdf)de bureau virtuel, qui examine la nouvelle fonctionnalité de mise à jour de l’intelligence de sécurité partagée, ainsi que des tests de performances et des conseils sur la façon de tester les performances de l’antivirus sur votre propre environnement VDI.</span><span class="sxs-lookup"><span data-stu-id="4d21f-120">You can also download the whitepaper [Microsoft Defender Antivirus on Virtual Desktop Infrastructure](https://demo.wd.microsoft.com/Content/wdav-testing-vdi-ssu.pdf), which looks at the new shared security intelligence update feature, alongside performance testing and guidance on how you can test antivirus performance on your own VDI.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d21f-121">Bien que l’environnement VDI puisse être hébergé sur Windows Server 2012 ou Windows Server 2016, les machines virtuelles doivent au minimum être en Windows 10, 1607, en raison de l’augmentation des technologies et des fonctionnalités de protection qui ne sont pas disponibles dans les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="4d21f-121">Although the VDI can be hosted on Windows Server 2012 or Windows Server 2016, the virtual machines (VMs) should be running Windows 10, 1607 at a minimum, due to increased protection technologies and features that are unavailable in earlier versions of Windows.</span></span><br/><span data-ttu-id="4d21f-122">Il existe des améliorations en matière de performances et de fonctionnalités dans le fonctionnement de Microsoft Defender AV sur des machines virtuelles dans Windows 10 Insider Preview, build 18323 (et version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="4d21f-122">There are performance and feature improvements to the way in which Microsoft Defender AV operates on virtual machines in Windows 10 Insider Preview, build 18323 (and later).</span></span> <span data-ttu-id="4d21f-123">Nous identifierons dans ce guide si vous devez utiliser une build Insider Preview ; Si elle n’est pas spécifiée, la version minimale requise pour une protection et des performances Windows 10 1607.</span><span class="sxs-lookup"><span data-stu-id="4d21f-123">We'll identify in this guide if you need to be using an Insider Preview build; if it isn't specified, then the minimum required version for the best protection and performance is Windows 10 1607.</span></span>

## <a name="set-up-a-dedicated-vdi-file-share"></a><span data-ttu-id="4d21f-124">Configurer un partage de fichiers VDI dédié</span><span class="sxs-lookup"><span data-stu-id="4d21f-124">Set up a dedicated VDI file share</span></span>

<span data-ttu-id="4d21f-125">Dans Windows 10, version 1903, nous avons introduit la fonctionnalité d’intelligence de sécurité partagée, qui décharge le déballage des mises à jour d’informations de sécurité téléchargées sur un ordinateur hôte, ce qui permet d’enregistrer les ressources précédentes de l’UC, du disque et de la mémoire sur des ordinateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="4d21f-125">In Windows 10, version 1903, we introduced the shared security intelligence feature, which offloads the unpackaging of downloaded security intelligence updates onto a host machine—thus saving previous CPU, disk, and memory resources on individual machines.</span></span> <span data-ttu-id="4d21f-126">Cette fonctionnalité a été backportée et fonctionne désormais dans Windows 10 version 1703 et versions supérieures.</span><span class="sxs-lookup"><span data-stu-id="4d21f-126">This feature has been backported and now works in Windows 10 version 1703 and above.</span></span> <span data-ttu-id="4d21f-127">Vous pouvez définir cette fonctionnalité avec une stratégie de groupe ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d21f-127">You can set this feature with a Group Policy, or PowerShell.</span></span>

### <a name="use-group-policy-to-enable-the-shared-security-intelligence-feature"></a><span data-ttu-id="4d21f-128">Utilisez la stratégie de groupe pour activer la fonctionnalité d’intelligence de sécurité partagée :</span><span class="sxs-lookup"><span data-stu-id="4d21f-128">Use Group Policy to enable the shared security intelligence feature:</span></span>

1. <span data-ttu-id="4d21f-129">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la Console de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-129">On your Group Policy management computer, open the Group Policy Management Console, right-click the Group Policy Object you want to configure, and then click **Edit**.</span></span>

2. <span data-ttu-id="4d21f-130">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-130">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="4d21f-131">Cliquez **sur Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-131">Click **Administrative templates**.</span></span>

4. <span data-ttu-id="4d21f-132">Développez l’arborescence **Windows composants Antivirus Microsoft Defender**  >    >  **security intelligence updates**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-132">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Security Intelligence Updates**.</span></span>

5. <span data-ttu-id="4d21f-133">Double-cliquez sur **Définir l’emplacement d’intelligence** de sécurité pour les clients VDI, puis définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-133">Double-click **Define security intelligence location for VDI clients**, and then set the option to **Enabled**.</span></span> <span data-ttu-id="4d21f-134">Un champ s’affiche automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4d21f-134">A field automatically appears.</span></span>

6. <span data-ttu-id="4d21f-135">Entrez `\\<sharedlocation\>\wdav-update` (pour obtenir de l’aide sur cette valeur, voir [Télécharger et décompresser).](#download-and-unpackage-the-latest-updates)</span><span class="sxs-lookup"><span data-stu-id="4d21f-135">Enter `\\<sharedlocation\>\wdav-update` (for help with this value, see [Download and unpackage](#download-and-unpackage-the-latest-updates)).</span></span>

7. <span data-ttu-id="4d21f-136">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-136">Click **OK**.</span></span>

8. <span data-ttu-id="4d21f-137">Déployez l’GPO sur les VM que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="4d21f-137">Deploy the GPO to the VMs you want to test.</span></span>

### <a name="use-powershell-to-enable-the-shared-security-intelligence-feature"></a><span data-ttu-id="4d21f-138">Utiliser PowerShell pour activer la fonctionnalité d’intelligence de sécurité partagée</span><span class="sxs-lookup"><span data-stu-id="4d21f-138">Use PowerShell to enable the shared security intelligence feature</span></span>

<span data-ttu-id="4d21f-139">Utilisez l’cmdlet suivante pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4d21f-139">Use the following cmdlet to enable the feature.</span></span> <span data-ttu-id="4d21f-140">Vous devez ensuite la pousser comme vous le feriez normalement pour les stratégies de configuration basées sur PowerShell sur les ordinateurs VM :</span><span class="sxs-lookup"><span data-stu-id="4d21f-140">You’ll need to then push this as you normally would push PowerShell-based configuration policies onto the VMs:</span></span>

```PowerShell
Set-MpPreference -SharedSignaturesPath \\<shared location>\wdav-update
```

<span data-ttu-id="4d21f-141">Consultez la section [Télécharger et décompresser](#download-and-unpackage-the-latest-updates) pour savoir ce \<shared location\> qui sera.</span><span class="sxs-lookup"><span data-stu-id="4d21f-141">See the [Download and unpackage](#download-and-unpackage-the-latest-updates) section for what the \<shared location\> will be.</span></span>

## <a name="download-and-unpackage-the-latest-updates"></a><span data-ttu-id="4d21f-142">Télécharger et décompresser les dernières mises à jour</span><span class="sxs-lookup"><span data-stu-id="4d21f-142">Download and unpackage the latest updates</span></span>

<span data-ttu-id="4d21f-143">Vous pouvez maintenant commencer à télécharger et installer de nouvelles mises à jour.</span><span class="sxs-lookup"><span data-stu-id="4d21f-143">Now you can get started on downloading and installing new updates.</span></span> <span data-ttu-id="4d21f-144">Nous avons créé un exemple de script PowerShell ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4d21f-144">We’ve created a sample PowerShell script for you below.</span></span> <span data-ttu-id="4d21f-145">Ce script est le moyen le plus simple de télécharger de nouvelles mises à jour et de les préparer pour vos VM.</span><span class="sxs-lookup"><span data-stu-id="4d21f-145">This script is the easiest way to download new updates and get them ready for your VMs.</span></span> <span data-ttu-id="4d21f-146">Vous devez ensuite définir le script pour qu’il s’exécute à un moment donné sur l’ordinateur de gestion à l’aide d’une tâche programmée (ou, si vous êtes familiarisé avec l’utilisation de scripts PowerShell dans Azure, Intune ou SCCM, vous pouvez également utiliser ces scripts).</span><span class="sxs-lookup"><span data-stu-id="4d21f-146">You should then set the script to run at a certain time on the management machine by using a scheduled task (or, if you’re familiar with using PowerShell scripts in Azure, Intune, or SCCM, you could also use those scripts).</span></span>

```PowerShell
$vdmpathbase = "$env:systemdrive\wdav-update\{00000000-0000-0000-0000-"
$vdmpathtime = Get-Date -format "yMMddHHmmss"
$vdmpath = $vdmpathbase + $vdmpathtime + '}'
$vdmpackage = $vdmpath + '\mpam-fe.exe'

New-Item -ItemType Directory -Force -Path $vdmpath | Out-Null

Invoke-WebRequest -Uri 'https://go.microsoft.com/fwlink/?LinkID=121721&arch=x64' -OutFile $vdmpackage

cmd /c "cd $vdmpath & c: & mpam-fe.exe /x"
```

<span data-ttu-id="4d21f-147">Vous pouvez définir une tâche programmée de sorte qu’elle s’exécute une fois par jour de sorte que chaque fois que le package est téléchargé et décompressé, les VM reçoivent la nouvelle mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4d21f-147">You can set a scheduled task to run once a day so that whenever the package is downloaded and unpacked then the VMs will receive the new update.</span></span> <span data-ttu-id="4d21f-148">Nous vous suggérons de commencer une fois par jour, mais vous devez essayer d’augmenter ou de réduire la fréquence pour en comprendre l’impact.</span><span class="sxs-lookup"><span data-stu-id="4d21f-148">We suggest starting with once a day—but you should experiment with increasing or decreasing the frequency to understand the impact.</span></span> 

<span data-ttu-id="4d21f-149">Les packages d’informations de sécurité sont généralement publiés toutes les trois à quatre heures.</span><span class="sxs-lookup"><span data-stu-id="4d21f-149">Security intelligence packages are typically published once every three to four hours.</span></span> <span data-ttu-id="4d21f-150">Il n’est pas conseillé de définir une fréquence de moins de quatre heures, car cela augmente la surcharge réseau sur votre ordinateur de gestion sans aucun avantage.</span><span class="sxs-lookup"><span data-stu-id="4d21f-150">Setting a frequency shorter than four hours isn’t advised because it will increase the network overhead on your management machine for no benefit.</span></span>

### <a name="set-a-scheduled-task-to-run-the-powershell-script"></a><span data-ttu-id="4d21f-151">Définir une tâche programmée pour exécuter le script PowerShell</span><span class="sxs-lookup"><span data-stu-id="4d21f-151">Set a scheduled task to run the PowerShell script</span></span>

1. <span data-ttu-id="4d21f-152">Sur l’ordinateur de gestion, ouvrez le menu Démarrer et tapez **Planification des tâches.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-152">On the management machine, open the Start menu and type **Task Scheduler**.</span></span> <span data-ttu-id="4d21f-153">Ouvrez-le et **sélectionnez Créer une tâche...**</span><span class="sxs-lookup"><span data-stu-id="4d21f-153">Open it and select **Create task…**</span></span> <span data-ttu-id="4d21f-154">sur le panneau latéral.</span><span class="sxs-lookup"><span data-stu-id="4d21f-154">on the side panel.</span></span>

2. <span data-ttu-id="4d21f-155">Entrez le nom en **tant que décompresseur security intelligence**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-155">Enter the name as **Security intelligence unpacker**.</span></span> <span data-ttu-id="4d21f-156">Go to the **Trigger** tab. Sélectionnez **Nouveau...**</span><span class="sxs-lookup"><span data-stu-id="4d21f-156">Go to the **Trigger** tab. Select **New…**</span></span><span data-ttu-id="4d21f-157"> > **Tous** les jours, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-157"> > **Daily**, and select **OK**.</span></span>

3. <span data-ttu-id="4d21f-158">Go to the **Actions** tab. Sélectionnez **Nouveau...**</span><span class="sxs-lookup"><span data-stu-id="4d21f-158">Go to the **Actions** tab. Select **New…**</span></span> <span data-ttu-id="4d21f-159">Entrez **PowerShell dans** le **champ Programme/Script.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-159">Enter **PowerShell** in the **Program/Script** field.</span></span> <span data-ttu-id="4d21f-160">Entrez `-ExecutionPolicy Bypass c:\wdav-update\vdmdlunpack.ps1` le champ Ajouter des **arguments.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-160">Enter `-ExecutionPolicy Bypass c:\wdav-update\vdmdlunpack.ps1` in the **Add arguments** field.</span></span> <span data-ttu-id="4d21f-161">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-161">Select **OK**.</span></span>

4. <span data-ttu-id="4d21f-162">Vous pouvez choisir de configurer des paramètres supplémentaires si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="4d21f-162">You can choose to configure additional settings if you wish.</span></span>

5. <span data-ttu-id="4d21f-163">Sélectionnez **OK** pour enregistrer la tâche programmée.</span><span class="sxs-lookup"><span data-stu-id="4d21f-163">Select **OK** to save the scheduled task.</span></span>
 
<span data-ttu-id="4d21f-164">Vous pouvez lancer la mise à jour manuellement en cliquant avec le bouton droit sur la tâche et en cliquant sur **Exécuter.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-164">You can initiate the update manually by right-clicking on the task and clicking **Run**.</span></span>

### <a name="download-and-unpackage-manually"></a><span data-ttu-id="4d21f-165">Télécharger et décompresser manuellement</span><span class="sxs-lookup"><span data-stu-id="4d21f-165">Download and unpackage manually</span></span>

<span data-ttu-id="4d21f-166">Si vous préférez tout faire manuellement, voici comment répliquer le comportement du script :</span><span class="sxs-lookup"><span data-stu-id="4d21f-166">If you would prefer to do everything manually, here's what to do to replicate the script’s behavior:</span></span>

1. <span data-ttu-id="4d21f-167">Créez un dossier à la racine du système appelé pour stocker les mises à jour d’intelligence, par `wdav_update` exemple, créez le `c:\wdav_update` dossier.</span><span class="sxs-lookup"><span data-stu-id="4d21f-167">Create a new folder on the system root called `wdav_update` to store intelligence updates, for example, create the folder `c:\wdav_update`.</span></span>

2. <span data-ttu-id="4d21f-168">Créez un *sous-wdav_update* sous un nom GUID, par exemple `{00000000-0000-0000-0000-000000000000}`</span><span class="sxs-lookup"><span data-stu-id="4d21f-168">Create a subfolder under *wdav_update* with a GUID name, such as `{00000000-0000-0000-0000-000000000000}`</span></span>

<span data-ttu-id="4d21f-169">Voici un exemple : `c:\wdav_update\{00000000-0000-0000-0000-000000000000}`</span><span class="sxs-lookup"><span data-stu-id="4d21f-169">Here's an example: `c:\wdav_update\{00000000-0000-0000-0000-000000000000}`</span></span>

   > [!NOTE]
   > <span data-ttu-id="4d21f-170">Dans le script, nous l’avons définie de sorte que les 12 derniers chiffres du GUID soient l’année, le mois, le jour et l’heure de téléchargement du fichier afin qu’un nouveau dossier soit créé à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="4d21f-170">In the script we set it so the last 12 digits of the GUID are the year, month, day, and time when the file was downloaded so that a new folder is created each time.</span></span> <span data-ttu-id="4d21f-171">Vous pouvez modifier cela afin que le fichier soit téléchargé dans le même dossier à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="4d21f-171">You can change this so that the file is downloaded to the same folder each time.</span></span>

3. <span data-ttu-id="4d21f-172">Téléchargez un package d’informations de sécurité [https://www.microsoft.com/wdsi/definitions](https://www.microsoft.com/wdsi/definitions)  à partir du dossier GUID.</span><span class="sxs-lookup"><span data-stu-id="4d21f-172">Download a security intelligence package from [https://www.microsoft.com/wdsi/definitions](https://www.microsoft.com/wdsi/definitions)  into the GUID folder.</span></span> <span data-ttu-id="4d21f-173">Le fichier doit être nommé `mpam-fe.exe` .</span><span class="sxs-lookup"><span data-stu-id="4d21f-173">The file should be named `mpam-fe.exe`.</span></span>

4. <span data-ttu-id="4d21f-174">Ouvrez une fenêtre d’invite de cmd et accédez au dossier GUID que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="4d21f-174">Open a cmd prompt window and navigate to the GUID folder you created.</span></span> <span data-ttu-id="4d21f-175">Utilisez la **commande d’extraction /X** pour extraire les fichiers, par `mpam-fe.exe /X` exemple.</span><span class="sxs-lookup"><span data-stu-id="4d21f-175">Use the **/X** extraction command to extract the files, for example `mpam-fe.exe /X`.</span></span>

   > [!NOTE]
   > <span data-ttu-id="4d21f-176">Les VMs sélectionnent le package mis à jour chaque fois qu’un nouveau dossier GUID est créé avec un package de mise à jour extrait ou chaque fois qu’un dossier existant est mis à jour avec un nouveau package extrait.</span><span class="sxs-lookup"><span data-stu-id="4d21f-176">The VMs will pick up the updated package whenever a new GUID folder is created with an extracted update package or whenever an existing folder is updated with a new extracted package.</span></span>

## <a name="randomize-scheduled-scans"></a><span data-ttu-id="4d21f-177">Randomiser les analyses programmées</span><span class="sxs-lookup"><span data-stu-id="4d21f-177">Randomize scheduled scans</span></span>

<span data-ttu-id="4d21f-178">Les analyses programmées s’exécutent en plus de la protection et de [l’analyse en temps réel.](configure-real-time-protection-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="4d21f-178">Scheduled scans run in addition to [real-time protection and scanning](configure-real-time-protection-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="4d21f-179">L’heure de début de l’analyse elle-même est toujours basée sur la stratégie d’analyse programmée (**ScheduleDay**, **ScheduleTime** et **ScheduleQuickScanTime**).</span><span class="sxs-lookup"><span data-stu-id="4d21f-179">The start time of the scan itself is still based on the scheduled scan policy (**ScheduleDay**, **ScheduleTime**, and **ScheduleQuickScanTime**).</span></span> <span data-ttu-id="4d21f-180">La randomisation entraîne Antivirus Microsoft Defender démarrer une analyse sur chaque ordinateur dans une fenêtre de 4 heures à partir de l’heure définie pour l’analyse programmée.</span><span class="sxs-lookup"><span data-stu-id="4d21f-180">Randomization will cause Microsoft Defender Antivirus to start a scan on each machine within a 4-hour window from the time set for the scheduled scan.</span></span>

<span data-ttu-id="4d21f-181">Voir [Analyses de planification pour](scheduled-catch-up-scans-microsoft-defender-antivirus.md) les autres options de configuration disponibles pour les analyses programmées.</span><span class="sxs-lookup"><span data-stu-id="4d21f-181">See [Schedule scans](scheduled-catch-up-scans-microsoft-defender-antivirus.md) for other configuration options available for scheduled scans.</span></span>

## <a name="use-quick-scans"></a><span data-ttu-id="4d21f-182">Utiliser des analyses rapides</span><span class="sxs-lookup"><span data-stu-id="4d21f-182">Use quick scans</span></span>

<span data-ttu-id="4d21f-183">Vous pouvez spécifier le type d’analyse à effectuer lors d’une analyse programmée.</span><span class="sxs-lookup"><span data-stu-id="4d21f-183">You can specify the type of scan that should be performed during a scheduled scan.</span></span> <span data-ttu-id="4d21f-184">Les analyses rapides sont l’approche préférée, car elles sont conçues pour rechercher tous les endroits où les programmes malveillants doivent résider pour être actifs.</span><span class="sxs-lookup"><span data-stu-id="4d21f-184">Quick scans are the preferred approach as they are designed to look in all places where malware needs to reside to be active.</span></span> <span data-ttu-id="4d21f-185">La procédure suivante décrit comment configurer des analyses rapides à l’aide de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4d21f-185">The following procedure describes how to set up quick scans using Group Policy.</span></span>

1. <span data-ttu-id="4d21f-186">Dans votre Éditeur de stratégie de groupe, allez aux **modèles**  >  **d’administration Windows composants**  >    >  **Antivirus Microsoft Defender’analyse.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-186">In your Group Policy Editor, go to **Administrative templates** > **Windows components** > **Microsoft Defender Antivirus** > **Scan**.</span></span>

2. <span data-ttu-id="4d21f-187">Sélectionnez **Spécifier le type d’analyse à utiliser pour** une analyse programmée, puis modifiez le paramètre de stratégie.</span><span class="sxs-lookup"><span data-stu-id="4d21f-187">Select **Specify the scan type to use for a scheduled scan** and then edit the policy setting.</span></span>

3. <span data-ttu-id="4d21f-188">Définissez la stratégie **sur Activé,** puis sous **Options,** sélectionnez **Analyse rapide.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-188">Set the policy to **Enabled**, and then under **Options**, select  **Quick scan**.</span></span>

4. <span data-ttu-id="4d21f-189">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-189">Select **OK**.</span></span> 

5. <span data-ttu-id="4d21f-190">Déployez votre objet de stratégie de groupe comme vous le faites habituellement.</span><span class="sxs-lookup"><span data-stu-id="4d21f-190">Deploy your Group Policy object as you usually do.</span></span>

## <a name="prevent-notifications"></a><span data-ttu-id="4d21f-191">Empêcher les notifications</span><span class="sxs-lookup"><span data-stu-id="4d21f-191">Prevent notifications</span></span>

<span data-ttu-id="4d21f-192">Parfois, Antivirus Microsoft Defender notifications peuvent être envoyées à plusieurs sessions ou être persistantes.</span><span class="sxs-lookup"><span data-stu-id="4d21f-192">Sometimes, Microsoft Defender Antivirus notifications may be sent to or persist across multiple sessions.</span></span> <span data-ttu-id="4d21f-193">Pour minimiser ce problème, vous pouvez verrouiller l’interface Antivirus Microsoft Defender utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4d21f-193">In order to minimize this problem, you can lock down the Microsoft Defender Antivirus user interface.</span></span> <span data-ttu-id="4d21f-194">La procédure suivante décrit comment supprimer les notifications avec la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4d21f-194">The following procedure describes how to suppress notifications with Group Policy.</span></span>

1. <span data-ttu-id="4d21f-195">Dans votre Éditeur de stratégie de groupe, Windows **composants**  >  **Antivirus Microsoft Defender**  >  **interface client.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-195">In your Group Policy Editor, go to **Windows components** > **Microsoft Defender Antivirus** > **Client Interface**.</span></span>

2. <span data-ttu-id="4d21f-196">Sélectionnez **Supprimer toutes les notifications,** puis modifiez les paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="4d21f-196">Select **Suppress all notifications** and then edit the policy settings.</span></span> 

3. <span data-ttu-id="4d21f-197">Définissez la stratégie **sur Activé,** puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-197">Set the policy to **Enabled**, and then select **OK**.</span></span>

4. <span data-ttu-id="4d21f-198">Déployez votre objet de stratégie de groupe comme vous le faites habituellement.</span><span class="sxs-lookup"><span data-stu-id="4d21f-198">Deploy your Group Policy object as you usually do.</span></span>

<span data-ttu-id="4d21f-199">La suppression des notifications empêche les notifications d’Antivirus Microsoft Defender de s’afficher dans le centre de notifications sur Windows 10 lorsque des analyses sont réalisées ou que des actions de correction sont prises.</span><span class="sxs-lookup"><span data-stu-id="4d21f-199">Suppressing notifications prevents notifications from Microsoft Defender Antivirus from showing up in the Action Center on Windows 10 when scans are done or remediation actions are taken.</span></span> <span data-ttu-id="4d21f-200">Toutefois, votre équipe des opérations de sécurité verra les résultats de l’analyse dans le Centre de sécurité Microsoft Defender ( [https://securitycenter.windows.com](https://securitycenter.windows.com) ).</span><span class="sxs-lookup"><span data-stu-id="4d21f-200">However, your security operations team will see the results of the scan in the Microsoft Defender Security Center ([https://securitycenter.windows.com](https://securitycenter.windows.com)).</span></span>

> [!TIP]
> <span data-ttu-id="4d21f-201">Pour ouvrir le Centre de Windows 10, prenez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d21f-201">To open the Action Center on Windows 10, take one of the following steps:</span></span>
> - <span data-ttu-id="4d21f-202">À l’extrémité droite de la barre des tâches, sélectionnez l’icône centre de travail.</span><span class="sxs-lookup"><span data-stu-id="4d21f-202">On the right end of the taskbar, select the Action Center icon.</span></span>
> - <span data-ttu-id="4d21f-203">Appuyez sur Windows touche de logo + A.</span><span class="sxs-lookup"><span data-stu-id="4d21f-203">Press the Windows logo key button + A.</span></span>
> - <span data-ttu-id="4d21f-204">Sur un appareil tactile, effectuez un balayage à partir du bord droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="4d21f-204">On a touchscreen device, swipe in from the right edge of the screen.</span></span>

## <a name="disable-scans-after-an-update"></a><span data-ttu-id="4d21f-205">Désactiver les analyses après une mise à jour</span><span class="sxs-lookup"><span data-stu-id="4d21f-205">Disable scans after an update</span></span>

<span data-ttu-id="4d21f-206">La désactivation d’une analyse après une mise à jour empêche l’analyse de se produire après la réception d’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4d21f-206">Disabling a scan after an update will prevent a scan from occurring after receiving an update.</span></span> <span data-ttu-id="4d21f-207">Vous pouvez appliquer ce paramètre lors de la création de l’image de base si vous avez également exécuté une analyse rapide.</span><span class="sxs-lookup"><span data-stu-id="4d21f-207">You can apply this setting when creating the base image if you have also run a quick scan.</span></span> <span data-ttu-id="4d21f-208">De cette façon, vous pouvez empêcher la nouvelle mise à jour de la VM d’effectuer à nouveau une analyse (comme vous l’avez déjà analysé lors de la création de l’image de base).</span><span class="sxs-lookup"><span data-stu-id="4d21f-208">This way, you can prevent the newly updated VM from performing a scan again (as you've already scanned it when you created the base image).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d21f-209">L’exécution d’analyses après une mise à jour permet de s’assurer que vos VM sont protégées avec les dernières mises à jour d’intelligence de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4d21f-209">Running scans after an update will help ensure your VMs are protected with the latest Security intelligence updates.</span></span> <span data-ttu-id="4d21f-210">La désactivation de cette option réduit le niveau de protection de vos VM et ne doit être utilisée que lors de la création ou du déploiement de l’image de base.</span><span class="sxs-lookup"><span data-stu-id="4d21f-210">Disabling this option will reduce the protection level of your VMs and should only be used when first creating or deploying the base image.</span></span>

1. <span data-ttu-id="4d21f-211">Dans votre Éditeur de stratégie de groupe, Windows **composants** Antivirus Microsoft Defender mises à jour  >    >  **security intelligence**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-211">In your Group Policy Editor, go to **Windows components** > **Microsoft Defender Antivirus** > **Security Intelligence Updates**.</span></span>

2. <span data-ttu-id="4d21f-212">Sélectionnez **Activer l’analyse après la mise** à jour des informations de sécurité, puis modifiez le paramètre de stratégie.</span><span class="sxs-lookup"><span data-stu-id="4d21f-212">Select **Turn on scan after security intelligence update** and then edit the policy setting.</span></span>

3. <span data-ttu-id="4d21f-213">Définissez la stratégie sur **Désactivé.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-213">Set the policy to **Disabled**.</span></span>

4. <span data-ttu-id="4d21f-214">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-214">Select **OK**.</span></span>

5. <span data-ttu-id="4d21f-215">Déployez votre objet de stratégie de groupe comme vous le faites habituellement.</span><span class="sxs-lookup"><span data-stu-id="4d21f-215">Deploy your Group Policy object as you usually do.</span></span>

<span data-ttu-id="4d21f-216">Cette stratégie empêche l’exécution d’une analyse immédiatement après une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4d21f-216">This policy prevents a scan from running immediately after an update.</span></span>

## <a name="scan-vms-that-have-been-offline"></a><span data-ttu-id="4d21f-217">Analyser les ordinateurs VM qui ont été hors connexion</span><span class="sxs-lookup"><span data-stu-id="4d21f-217">Scan VMs that have been offline</span></span>

1. <span data-ttu-id="4d21f-218">Dans votre Éditeur de stratégie de groupe, Windows **composants**  >  **Antivirus Microsoft Defender**  >  **Scan**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-218">In your Group Policy Editor, go to to **Windows components** > **Microsoft Defender Antivirus** > **Scan**.</span></span>

2. <span data-ttu-id="4d21f-219">Sélectionnez **Activer l’analyse rapide de rattrapage,** puis modifiez le paramètre de stratégie.</span><span class="sxs-lookup"><span data-stu-id="4d21f-219">Select **Turn on catch-up quick scan** and then edit the policy setting.</span></span>

3. <span data-ttu-id="4d21f-220">Définissez la stratégie **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-220">Set the policy to **Enabled**.</span></span>

4. <span data-ttu-id="4d21f-221">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-221">Select **OK**.</span></span>

5. <span data-ttu-id="4d21f-222">Déployez votre objet de stratégie de groupe comme vous le faites généralement.</span><span class="sxs-lookup"><span data-stu-id="4d21f-222">Deploy your Group Policy Object as you usually do.</span></span>

<span data-ttu-id="4d21f-223">Cette stratégie force une analyse si la VM a manqué au moins deux analyses programmées consécutives.</span><span class="sxs-lookup"><span data-stu-id="4d21f-223">This policy forces a scan if the VM has missed two or more consecutive scheduled scans.</span></span>

## <a name="enable-headless-ui-mode"></a><span data-ttu-id="4d21f-224">Activer le mode d’interface utilisateur sans en-tête</span><span class="sxs-lookup"><span data-stu-id="4d21f-224">Enable headless UI mode</span></span>

1. <span data-ttu-id="4d21f-225">Dans votre Éditeur de stratégie de groupe, Windows **composants**  >  **Antivirus Microsoft Defender**  >  **interface client.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-225">In your Group Policy Editor, go to **Windows components** > **Microsoft Defender Antivirus** > **Client Interface**.</span></span>

2. <span data-ttu-id="4d21f-226">Sélectionnez **Activer le mode d’interface utilisateur sans tête** et modifiez la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4d21f-226">Select **Enable headless UI mode** and edit the policy.</span></span>

3. <span data-ttu-id="4d21f-227">Définissez la stratégie **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="4d21f-227">Set the policy to **Enabled**.</span></span>

4. <span data-ttu-id="4d21f-228">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d21f-228">Click **OK**.</span></span>

5. <span data-ttu-id="4d21f-229">Déployez votre objet de stratégie de groupe comme vous le faites généralement.</span><span class="sxs-lookup"><span data-stu-id="4d21f-229">Deploy your Group Policy Object as you usually do.</span></span>
 
<span data-ttu-id="4d21f-230">Cette stratégie masque l’intégralité Antivirus Microsoft Defender’interface utilisateur des utilisateurs finaux de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4d21f-230">This policy hides the entire Microsoft Defender Antivirus user interface from end users in your organization.</span></span>

## <a name="exclusions"></a><span data-ttu-id="4d21f-231">Exclusions</span><span class="sxs-lookup"><span data-stu-id="4d21f-231">Exclusions</span></span>

<span data-ttu-id="4d21f-232">Les exclusions peuvent être ajoutées, supprimées ou personnalisées en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="4d21f-232">Exclusions can be added, removed, or customized to suit your needs.</span></span>

<span data-ttu-id="4d21f-233">Pour plus d’informations, [voir Configurer Antivirus Microsoft Defender exclusions sur Windows Server.](configure-exclusions-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="4d21f-233">For more information, see [Configure Microsoft Defender Antivirus exclusions on Windows Server](configure-exclusions-microsoft-defender-antivirus.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d21f-234">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4d21f-234">Additional resources</span></span>

- [<span data-ttu-id="4d21f-235">Blog tech Community : Configuration de Antivirus Microsoft Defender pour les ordinateurs VDI non persistants</span><span class="sxs-lookup"><span data-stu-id="4d21f-235">Tech Community Blog: Configuring Microsoft Defender Antivirus for non-persistent VDI machines</span></span>](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/configuring-microsoft-defender-antivirus-for-non-persistent-vdi/ba-p/1489633)
- [<span data-ttu-id="4d21f-236">Forums TechNet sur les services Bureau à distance et VDI</span><span class="sxs-lookup"><span data-stu-id="4d21f-236">TechNet forums on Remote Desktop Services and VDI</span></span>](https://social.technet.microsoft.com/Forums/windowsserver/en-US/home?forum=winserverTS)
- [<span data-ttu-id="4d21f-237">Script PowerShell SignatureDownloadCustomTask</span><span class="sxs-lookup"><span data-stu-id="4d21f-237">SignatureDownloadCustomTask PowerShell script</span></span>](https://www.powershellgallery.com/packages/SignatureDownloadCustomTask/1.4)