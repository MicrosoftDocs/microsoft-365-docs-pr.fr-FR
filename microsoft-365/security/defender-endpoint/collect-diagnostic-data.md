---
title: Collecter des données de diagnostic de l'Antivirus Microsoft Defender
description: Utiliser un outil pour collecter des données pour résoudre les problèmes de l'Antivirus Microsoft Defender
keywords: résoudre les problèmes, erreur, corriger, mettre à jour la conformité, oms, surveiller, rapport, Microsoft Defender av, objet de stratégie de groupe, paramètre, données de diagnostic
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 06/29/2020
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 3b7c07bace86a2a4651e5c951c6e0b7d954f0982
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690475"
---
# <a name="collect-microsoft-defender-av-diagnostic-data"></a><span data-ttu-id="7d107-104">Collecter les données de diagnostic de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="7d107-104">Collect Microsoft Defender AV diagnostic data</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="7d107-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7d107-105">**Applies to:**</span></span>

- [<span data-ttu-id="7d107-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7d107-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="7d107-107">Cet article explique comment collecter des données de diagnostic qui peuvent être utilisées par le support microsoft et les équipes d'ingénierie pour vous aider à résoudre les problèmes que vous pouvez rencontrer lors de l'utilisation de l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="7d107-107">This article describes how to collect diagnostic data that can be used by Microsoft support and engineering teams to help troubleshoot issues you might encounter when using the Microsoft Defender AV.</span></span>

> [!NOTE]
> <span data-ttu-id="7d107-108">Dans le cadre du processus d'examen ou de réponse, vous pouvez collecter un package d'enquête à partir d'un appareil.</span><span class="sxs-lookup"><span data-stu-id="7d107-108">As part of the investigation or response process, you can collect an investigation package from a device.</span></span> <span data-ttu-id="7d107-109">Voici comment : Collecter un [package d'enquête à partir d'appareils.](/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts#collect-investigation-package-from-devices)</span><span class="sxs-lookup"><span data-stu-id="7d107-109">Here's how: [Collect investigation package from devices](/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts#collect-investigation-package-from-devices).</span></span>

<span data-ttu-id="7d107-110">Sur au moins deux appareils qui rencontrent le même problème, obtenez le fichier de diagnostic .cab en suivant les étapes ci-après :</span><span class="sxs-lookup"><span data-stu-id="7d107-110">On at least two devices that are experiencing the same issue, obtain the .cab diagnostic file by taking the following steps:</span></span>

1. <span data-ttu-id="7d107-111">Ouvrez une version de niveau administrateur de l'invite de commandes comme suit :</span><span class="sxs-lookup"><span data-stu-id="7d107-111">Open an administrator-level version of the command prompt as follows:</span></span>

    <span data-ttu-id="7d107-112">a.</span><span class="sxs-lookup"><span data-stu-id="7d107-112">a.</span></span> <span data-ttu-id="7d107-113">Ouvrez **le** menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="7d107-113">Open the **Start** menu.</span></span>

    <span data-ttu-id="7d107-114">b.</span><span class="sxs-lookup"><span data-stu-id="7d107-114">b.</span></span> <span data-ttu-id="7d107-115">Tapez **cmd**.</span><span class="sxs-lookup"><span data-stu-id="7d107-115">Type **cmd**.</span></span> <span data-ttu-id="7d107-116">Cliquez avec le bouton droit sur **l'invite de commandes,** puis cliquez **sur Exécuter en tant qu'administrateur.**</span><span class="sxs-lookup"><span data-stu-id="7d107-116">Right-click on **Command Prompt** and click **Run as administrator**.</span></span>

    <span data-ttu-id="7d107-117">c.</span><span class="sxs-lookup"><span data-stu-id="7d107-117">c.</span></span> <span data-ttu-id="7d107-118">Entrez les informations d'identification de l'administrateur ou approuvez l'invite.</span><span class="sxs-lookup"><span data-stu-id="7d107-118">Enter administrator credentials or approve the prompt.</span></span>

2. <span data-ttu-id="7d107-119">Accédez au répertoire Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="7d107-119">Navigate to the Microsoft Defender directory.</span></span> <span data-ttu-id="7d107-120">Par défaut, cette valeur est `C:\Program Files\Windows Defender`.</span><span class="sxs-lookup"><span data-stu-id="7d107-120">By default, this is `C:\Program Files\Windows Defender`.</span></span>

> [!NOTE]
> <span data-ttu-id="7d107-121">Si vous exécutez une version mise à jour de la plateforme [Microsoft Defender,](https://support.microsoft.com/help/4052623/update-for-microsoft-defender-antimalware-platform)exécutez-la à `MpCmdRun` partir de l'emplacement suivant : `C:\ProgramData\Microsoft\Windows Defender\Platform\<version>`</span><span class="sxs-lookup"><span data-stu-id="7d107-121">If you're running an [updated Microsoft Defender Platform version](https://support.microsoft.com/help/4052623/update-for-microsoft-defender-antimalware-platform), please run `MpCmdRun` from the following location: `C:\ProgramData\Microsoft\Windows Defender\Platform\<version>`.</span></span>

3. <span data-ttu-id="7d107-122">Tapez la commande suivante, puis appuyez sur **Entrée**</span><span class="sxs-lookup"><span data-stu-id="7d107-122">Type the following command, and then press **Enter**</span></span>  

    ```Dos
    mpcmdrun.exe -GetFiles
    ```
  
4. <span data-ttu-id="7d107-123">Un fichier .cab qui contient divers journaux de diagnostic est généré.</span><span class="sxs-lookup"><span data-stu-id="7d107-123">A .cab file will be generated that contains various diagnostic logs.</span></span> <span data-ttu-id="7d107-124">L'emplacement du fichier est spécifié dans la sortie de l'invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="7d107-124">The location of the file will be specified in the output in the command prompt.</span></span> <span data-ttu-id="7d107-125">Par défaut, l'emplacement est `C:\ProgramData\Microsoft\Microsoft Defender\Support\MpSupportFiles.cab` .</span><span class="sxs-lookup"><span data-stu-id="7d107-125">By default, the location is `C:\ProgramData\Microsoft\Microsoft Defender\Support\MpSupportFiles.cab`.</span></span>

> [!NOTE]
> <span data-ttu-id="7d107-126">Pour rediriger le fichier cab vers un chemin d'accès différent ou un partage UNC, utilisez la commande suivante : `mpcmdrun.exe -GetFiles -SupportLogLocation <path>`</span><span class="sxs-lookup"><span data-stu-id="7d107-126">To redirect the cab file to a a different path or UNC share, use the following command: `mpcmdrun.exe -GetFiles -SupportLogLocation <path>`</span></span>  <br/><span data-ttu-id="7d107-127">Pour plus d'informations, voir [Rediriger les données de diagnostic vers un partage UNC.](#redirect-diagnostic-data-to-a-unc-share)</span><span class="sxs-lookup"><span data-stu-id="7d107-127">For more information, see [Redirect diagnostic data to a UNC share](#redirect-diagnostic-data-to-a-unc-share).</span></span>

5. <span data-ttu-id="7d107-128">Copiez ces fichiers .cab vers un emplacement accessible par le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d107-128">Copy these .cab files to a location that can be accessed by Microsoft support.</span></span> <span data-ttu-id="7d107-129">Par exemple, il peut s'agit d'un dossier OneDrive protégé par mot de passe que vous pouvez partager avec nous.</span><span class="sxs-lookup"><span data-stu-id="7d107-129">An example could be a password-protected OneDrive folder that you can share with us.</span></span>

> [!NOTE]
><span data-ttu-id="7d107-130">Si vous avez un problème avec la conformité des mises à jour, envoyez un courrier électronique à l'aide du modèle de courrier électronique de support update <a href="mailto:ucsupport@microsoft.com?subject=WDAV assessment issue&body=I%20am%20encountering%20the%20following%20issue%20when%20using%20Windows%20Defender%20AV%20in%20Update%20Compliance%3a%20%0d%0aI%20have%20provided%20at%20least%202%20support%20.cab%20files%20at%20the%20following%20location%3a%20%3Caccessible%20share%2c%20including%20access%20details%20such%20as%20password%3E%0d%0aMy%20OMS%20workspace%20ID%20is%3a%20%0d%0aPlease%20contact%20me%20at%3a">Compliance</a>et remplissez le modèle avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7d107-130">If you have a problem with Update compliance, send an email using the <a href="mailto:ucsupport@microsoft.com?subject=WDAV assessment issue&body=I%20am%20encountering%20the%20following%20issue%20when%20using%20Windows%20Defender%20AV%20in%20Update%20Compliance%3a%20%0d%0aI%20have%20provided%20at%20least%202%20support%20.cab%20files%20at%20the%20following%20location%3a%20%3Caccessible%20share%2c%20including%20access%20details%20such%20as%20password%3E%0d%0aMy%20OMS%20workspace%20ID%20is%3a%20%0d%0aPlease%20contact%20me%20at%3a">Update Compliance support email template</a>, and fill out the template with the following information:</span></span>
>```
> I am encountering the following issue when using Microsoft Defender Antivirus in Update Compliance:
> I have provided at least 2 support .cab files at the following location:  
> <accessible share, including access details such as password>
>
>    My OMS workspace ID is:
>
>    Please contact me at:

## <a name="redirect-diagnostic-data-to-a-unc-share"></a><span data-ttu-id="7d107-131">Rediriger les données de diagnostic vers un partage UNC</span><span class="sxs-lookup"><span data-stu-id="7d107-131">Redirect diagnostic data to a UNC share</span></span>
<span data-ttu-id="7d107-132">Pour collecter des données de diagnostic sur un référentiel central, vous pouvez spécifier le paramètre SupportLogLocation.</span><span class="sxs-lookup"><span data-stu-id="7d107-132">To collect diagnostic data on a central repository, you can specify the SupportLogLocation parameter.</span></span>

```Dos
mpcmdrun.exe -GetFiles -SupportLogLocation <path>
```

<span data-ttu-id="7d107-133">Copie les données de diagnostic dans le chemin d'accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="7d107-133">Copies the diagnostic data to the specified path.</span></span> <span data-ttu-id="7d107-134">Si le chemin d'accès n'est pas spécifié, les données de diagnostic sont copiées à l'emplacement spécifié dans la configuration de l'emplacement du journal de support.</span><span class="sxs-lookup"><span data-stu-id="7d107-134">If the path is not specified, the diagnostic data will be copied to the location specified in the Support Log Location Configuration.</span></span>

<span data-ttu-id="7d107-135">Lorsque le paramètre SupportLogLocation est utilisé, une structure de dossiers comme suit est créée dans le chemin d'accès de destination :</span><span class="sxs-lookup"><span data-stu-id="7d107-135">When the SupportLogLocation parameter is used, a folder structure like as follows will be created in the destination path:</span></span>

```Dos
<path>\<MMDD>\MpSupport-<hostname>-<HHMM>.cab
```

| <span data-ttu-id="7d107-136">champ</span><span class="sxs-lookup"><span data-stu-id="7d107-136">field</span></span>  | <span data-ttu-id="7d107-137">Description</span><span class="sxs-lookup"><span data-stu-id="7d107-137">Description</span></span>   |
|:----|:----|
| <span data-ttu-id="7d107-138">chemin</span><span class="sxs-lookup"><span data-stu-id="7d107-138">path</span></span> | <span data-ttu-id="7d107-139">Chemin d'accès spécifié sur la ligne de commande ou récupéré à partir de la configuration</span><span class="sxs-lookup"><span data-stu-id="7d107-139">The path as specified on the command line or retrieved from configuration</span></span>
| <span data-ttu-id="7d107-140">MMDD</span><span class="sxs-lookup"><span data-stu-id="7d107-140">MMDD</span></span> | <span data-ttu-id="7d107-141">Mois et jour où les données de diagnostic ont été collectées (par exemple, 0530)</span><span class="sxs-lookup"><span data-stu-id="7d107-141">Month and day when the diagnostic data was collected (for example, 0530)</span></span>
| <span data-ttu-id="7d107-142">hostname</span><span class="sxs-lookup"><span data-stu-id="7d107-142">hostname</span></span> | <span data-ttu-id="7d107-143">Nom d'hôte de l'appareil sur lequel les données de diagnostic ont été collectées</span><span class="sxs-lookup"><span data-stu-id="7d107-143">The hostname of the device on which the diagnostic data was collected</span></span>
| <span data-ttu-id="7d107-144">HHMM</span><span class="sxs-lookup"><span data-stu-id="7d107-144">HHMM</span></span> | <span data-ttu-id="7d107-145">Heures et minutes de collecte des données de diagnostic (par exemple, 1422)</span><span class="sxs-lookup"><span data-stu-id="7d107-145">Hours and minutes when the diagnostic data was collected (for example, 1422)</span></span>

> [!NOTE]
> <span data-ttu-id="7d107-146">Lorsque vous utilisez un partage de fichiers, assurez-vous que le compte utilisé pour collecter le package de diagnostic dispose d'un accès en écriture au partage.</span><span class="sxs-lookup"><span data-stu-id="7d107-146">When using a file share please make sure that account used to collect the diagnostic package has write access to the share.</span></span>  

## <a name="specify-location-where-diagnostic-data-is-created"></a><span data-ttu-id="7d107-147">Spécifier l'emplacement où les données de diagnostic sont créées</span><span class="sxs-lookup"><span data-stu-id="7d107-147">Specify location where diagnostic data is created</span></span>

<span data-ttu-id="7d107-148">Vous pouvez également spécifier l'endroit où le fichier .cab de diagnostic sera créé à l'aide d'un objet de stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="7d107-148">You can also specify where the diagnostic .cab file will be created using a Group Policy Object (GPO).</span></span> 

1. <span data-ttu-id="7d107-149">Ouvrez l'Éditeur de stratégie de groupe locale et recherchez l'po GPO SupportLogLocation à l':: `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\SupportLogLocation`</span><span class="sxs-lookup"><span data-stu-id="7d107-149">Open the Local Group Policy Editor and find the SupportLogLocation GPO at: `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\SupportLogLocation`</span></span>
   
1. <span data-ttu-id="7d107-150">Sélectionnez **Définir le chemin d'accès du répertoire pour copier les fichiers journaux de prise en charge.**</span><span class="sxs-lookup"><span data-stu-id="7d107-150">Select **Define the directory path to copy support log files**.</span></span>

    ![Capture d'écran de l'éditeur de stratégie de groupe local](images/GPO1-SupportLogLocationDefender.png)  
        
     ![Capture d'écran du paramètre définir le chemin d'accès aux fichiers journaux](images/GPO2-SupportLogLocationGPPage.png)  
3. <span data-ttu-id="7d107-153">À l'intérieur de l'éditeur de stratégie, **sélectionnez Activé.**</span><span class="sxs-lookup"><span data-stu-id="7d107-153">Inside the policy editor, select **Enabled**.</span></span>
       
4. <span data-ttu-id="7d107-154">Spécifiez le chemin d'accès du répertoire où vous souhaitez copier les fichiers journaux de support dans le **champ Options.**</span><span class="sxs-lookup"><span data-stu-id="7d107-154">Specify the directory path where you want to copy the support log files in the **Options** field.</span></span>
     <span data-ttu-id="7d107-155">![Capture d'écran du paramètre personnalisé de chemin d'accès au répertoire activé](images/GPO3-SupportLogLocationGPPageEnabledExample.png)</span><span class="sxs-lookup"><span data-stu-id="7d107-155">![Screenshot of Enabled directory path custom setting](images/GPO3-SupportLogLocationGPPageEnabledExample.png)</span></span> 
5. <span data-ttu-id="7d107-156">Sélectionnez **OK** ou **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="7d107-156">Select **OK** or **Apply**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d107-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d107-157">See also</span></span>

- [<span data-ttu-id="7d107-158">Résoudre les problèmes de rapport de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="7d107-158">Troubleshoot Microsoft Defender Antivirus reporting</span></span>](troubleshoot-reporting.md)