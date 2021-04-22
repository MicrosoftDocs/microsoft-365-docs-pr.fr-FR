---
title: Résoudre les problèmes d'installation de Microsoft Defender pour endpoint sur Linux
ms.reviewer: ''
description: Résoudre les problèmes d'installation de Microsoft Defender pour endpoint sur Linux
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, linux, installation
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 12f648ce476f6e29cbb6b038cc42f2e744d77104
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933300"
---
# <a name="troubleshoot-installation-issues-for-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="4cc1f-104">Résoudre les problèmes d'installation de Microsoft Defender pour endpoint sur Linux</span><span class="sxs-lookup"><span data-stu-id="4cc1f-104">Troubleshoot installation issues for Microsoft Defender for Endpoint on Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="4cc1f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4cc1f-105">**Applies to:**</span></span>
- [<span data-ttu-id="4cc1f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4cc1f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="4cc1f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4cc1f-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="4cc1f-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="4cc1f-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="4cc1f-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

## <a name="verify-if-installation-succeeded"></a><span data-ttu-id="4cc1f-110">Vérifier si l'installation a réussi</span><span class="sxs-lookup"><span data-stu-id="4cc1f-110">Verify if installation succeeded</span></span>

<span data-ttu-id="4cc1f-111">Une erreur d'installation peut ou non entraîner un message d'erreur significatif de la part du gestionnaire de package.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-111">An error in installation may or may not result in a meaningful error message by the package manager.</span></span> <span data-ttu-id="4cc1f-112">Pour vérifier si l'installation a réussi, obtenez et vérifiez les journaux d'installation en utilisant :</span><span class="sxs-lookup"><span data-stu-id="4cc1f-112">To verify if the installation succeeded, obtain and check the installation logs using:</span></span>

 ```bash
 sudo journalctl | grep 'microsoft-mdatp'  > installation.log
```

```bash
 grep 'postinstall end' installation.log
```

```Output
 microsoft-mdatp-installer[102243]: postinstall end [2020-03-26 07:04:43OURCE +0000] 102216
 ```

<span data-ttu-id="4cc1f-113">Une sortie de la commande précédente avec la date et l'heure correctes de l'installation indique la réussite.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-113">An output from the previous command with correct date and time of installation indicates success.</span></span>

<span data-ttu-id="4cc1f-114">Vérifiez également la [configuration du client](linux-install-manually.md#client-configuration) pour vérifier l'état du produit et détecter le fichier texte EICAR.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-114">Also check the [Client configuration](linux-install-manually.md#client-configuration) to verify the health of the product and detect the EICAR text file.</span></span>

## <a name="make-sure-you-have-the-correct-package"></a><span data-ttu-id="4cc1f-115">Assurez-vous que vous avez le package correct</span><span class="sxs-lookup"><span data-stu-id="4cc1f-115">Make sure you have the correct package</span></span>

<span data-ttu-id="4cc1f-116">N'oubliez pas que le package que vous installez correspond à la distribution et à la version de l'hôte.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-116">Please mind that the package you are installing is matching the host distribution and version.</span></span>

| <span data-ttu-id="4cc1f-117">package</span><span class="sxs-lookup"><span data-stu-id="4cc1f-117">package</span></span>                       | <span data-ttu-id="4cc1f-118">distribution</span><span class="sxs-lookup"><span data-stu-id="4cc1f-118">distribution</span></span>                             |
|-------------------------------|------------------------------------------|
| <span data-ttu-id="4cc1f-119">mdatp-rhel8. Linux.x86_64.rpm</span><span class="sxs-lookup"><span data-stu-id="4cc1f-119">mdatp-rhel8.Linux.x86_64.rpm</span></span>  | <span data-ttu-id="4cc1f-120">Oracle, RHEL et CentOS 8.x</span><span class="sxs-lookup"><span data-stu-id="4cc1f-120">Oracle, RHEL and CentOS 8.x</span></span>              |
| <span data-ttu-id="4cc1f-121">mdatp-sles12. Linux.x86_64.rpm</span><span class="sxs-lookup"><span data-stu-id="4cc1f-121">mdatp-sles12.Linux.x86_64.rpm</span></span> | <span data-ttu-id="4cc1f-122">SuSE Linux Enterprise Server 12.x</span><span class="sxs-lookup"><span data-stu-id="4cc1f-122">SuSE Linux Enterprise Server 12.x</span></span>        |
| <span data-ttu-id="4cc1f-123">mdatp-sles15. Linux.x86_64.rpm</span><span class="sxs-lookup"><span data-stu-id="4cc1f-123">mdatp-sles15.Linux.x86_64.rpm</span></span> | <span data-ttu-id="4cc1f-124">SuSE Linux Enterprise Server 15.x</span><span class="sxs-lookup"><span data-stu-id="4cc1f-124">SuSE Linux Enterprise Server 15.x</span></span>        |
| <span data-ttu-id="4cc1f-125">mdatp. Linux.x86_64.rpm</span><span class="sxs-lookup"><span data-stu-id="4cc1f-125">mdatp.Linux.x86_64.rpm</span></span>        | <span data-ttu-id="4cc1f-126">Oracle, RHEL et CentOS 7.x</span><span class="sxs-lookup"><span data-stu-id="4cc1f-126">Oracle, RHEL and CentOS 7.x</span></span>              |
| <span data-ttu-id="4cc1f-127">mdatp. Linux.x86_64.deb</span><span class="sxs-lookup"><span data-stu-id="4cc1f-127">mdatp.Linux.x86_64.deb</span></span>        | <span data-ttu-id="4cc1f-128">Debian et Ubuntu 16.04, 18.04 et 20.04</span><span class="sxs-lookup"><span data-stu-id="4cc1f-128">Debian and Ubuntu 16.04, 18.04 and 20.04</span></span> |

<span data-ttu-id="4cc1f-129">Pour [un déploiement](linux-install-manually.md)manuel, assurez-vous que la version et la version correctes ont été choisies.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-129">For [manual deployment](linux-install-manually.md), make sure the correct distro and version had been chosen.</span></span>

## <a name="installation-failed"></a><span data-ttu-id="4cc1f-130">Échec de l'installation</span><span class="sxs-lookup"><span data-stu-id="4cc1f-130">Installation failed</span></span>

<span data-ttu-id="4cc1f-131">Vérifiez si le service mdatp est en cours d'exécution :</span><span class="sxs-lookup"><span data-stu-id="4cc1f-131">Check if the mdatp service is running:</span></span>

```bash
systemctl status mdatp
```
```Output
 ● mdatp.service - Microsoft Defender for Endpoint
   Loaded: loaded (/lib/systemd/system/mdatp.service; enabled; vendor preset: enabled)
   Active: active (running) since Thu 2020-03-26 10:37:30 IST; 23h ago
 Main PID: 1966 (wdavdaemon)
    Tasks: 105 (limit: 4915)
   CGroup: /system.slice/mdatp.service
           ├─1966 /opt/microsoft/mdatp/sbin/wdavdaemon
           ├─1967 /opt/microsoft/mdatp/sbin/wdavdaemon
           └─1968 /opt/microsoft/mdatp/sbin/wdavdaemon
 ```

## <a name="steps-to-troubleshoot-if-mdatp-service-isnt-running"></a><span data-ttu-id="4cc1f-132">Étapes à suivre pour résoudre les problèmes si le service mdatp n'est pas en cours d'exécution</span><span class="sxs-lookup"><span data-stu-id="4cc1f-132">Steps to troubleshoot if mdatp service isn't running</span></span>

1. <span data-ttu-id="4cc1f-133">Vérifiez si l'utilisateur « mdatp » existe :</span><span class="sxs-lookup"><span data-stu-id="4cc1f-133">Check if "mdatp" user exists:</span></span>

    ```bash
    id "mdatp"
    ```

    <span data-ttu-id="4cc1f-134">S'il n'y a pas de sortie, exécutez</span><span class="sxs-lookup"><span data-stu-id="4cc1f-134">If there’s no output, run</span></span>

    ```bash
    sudo useradd --system --no-create-home --user-group --shell /usr/sbin/nologin mdatp
    ```

2. <span data-ttu-id="4cc1f-135">Essayez d'activer et de redémarrer le service à l'aide de :</span><span class="sxs-lookup"><span data-stu-id="4cc1f-135">Try enabling and restarting the service using:</span></span>

    ```bash
    sudo systemctl enable mdatp
    ```

    ```bash
    sudo systemctl restart mdatp
    ```

3. <span data-ttu-id="4cc1f-136">Si mdatp.service n'est pas trouvé lors de l'exécution de la commande précédente, exécutez :</span><span class="sxs-lookup"><span data-stu-id="4cc1f-136">If mdatp.service isn't found upon running the previous command, run:</span></span>

    ```bash
    sudo cp /opt/microsoft/mdatp/conf/mdatp.service <systemd_path>
    ```

    <span data-ttu-id="4cc1f-137">où ```<systemd_path>``` est pour les distributions Ubuntu et Debian et pour ```/lib/systemd/system``` ```/usr/lib/systemd/system``` Rhel, CentOS, Oracle et SLES.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-137">where ```<systemd_path>``` is ```/lib/systemd/system``` for Ubuntu and Debian distributions and ```/usr/lib/systemd/system``` for Rhel, CentOS, Oracle and SLES.</span></span>
   <span data-ttu-id="4cc1f-138">Réexécutez ensuite l'étape 2.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-138">Then rerun step 2.</span></span>

4. <span data-ttu-id="4cc1f-139">Si les étapes ci-dessus ne fonctionnent pas, vérifiez si SELinux est installé et en mode d'application.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-139">If the above steps don’t work, check if SELinux is installed and in enforcing mode.</span></span> <span data-ttu-id="4cc1f-140">Si c'est le cas, essayez de le définir sur le mode permissif (de préférence) ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-140">If so, try setting it to permissive (preferably) or disabled mode.</span></span> <span data-ttu-id="4cc1f-141">Pour ce faire, vous pouvez définir le paramètre sur « permissif » ou « désactivé » dans le fichier, puis par `SELINUX` `/etc/selinux/config` redémarrage.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-141">It can be done by setting the parameter `SELINUX` to "permissive" or "disabled" in `/etc/selinux/config` file, followed by reboot.</span></span> <span data-ttu-id="4cc1f-142">Pour plus d'informations, consultez la page de l'homme du sélinux.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-142">Check the man-page of selinux for more details.</span></span>
<span data-ttu-id="4cc1f-143">Essayez maintenant de redémarrer le service mdatp à l'aide de l'étape 2.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-143">Now try restarting the mdatp service using step 2.</span></span> <span data-ttu-id="4cc1f-144">Revert the configuration change immediately though for security reasons after trying it andboot.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-144">Revert the configuration change immediately though for security reasons after trying it and reboot.</span></span>

5. <span data-ttu-id="4cc1f-145">Si `/opt` le répertoire est un lien symbolique, créez un montage de liaison pour `/opt/microsoft` .</span><span class="sxs-lookup"><span data-stu-id="4cc1f-145">If `/opt` directory is a symbolic link, create a bind mount for `/opt/microsoft`.</span></span>

6. <span data-ttu-id="4cc1f-146">Assurez-vous que le daemon dispose de l'autorisation exécutable.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-146">Ensure that the daemon has executable permission.</span></span>

    ```bash
    ls -l /opt/microsoft/mdatp/sbin/wdavdaemon
    ```

    ```Output
    -rwxr-xr-x 2 root root 15502160 Mar  3 04:47 /opt/microsoft/mdatp/sbin/wdavdaemon
    ```

    <span data-ttu-id="4cc1f-147">Si le daemon n'a pas d'autorisations exécutables, rendez-le exécutable à l'aide de :</span><span class="sxs-lookup"><span data-stu-id="4cc1f-147">If the daemon doesn't have executable permissions, make it executable using:</span></span>

    ```bash
    sudo chmod 0755 /opt/microsoft/mdatp/sbin/wdavdaemon
    ```

    <span data-ttu-id="4cc1f-148">et réessayez d'exécution de l'étape 2.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-148">and retry running step 2.</span></span>

7. <span data-ttu-id="4cc1f-149">Assurez-vous que le système de fichiers contenant wdavdaemon n'est pas monté avec « noexec ».</span><span class="sxs-lookup"><span data-stu-id="4cc1f-149">Ensure that the file system containing wdavdaemon isn't mounted with "noexec".</span></span>

## <a name="if-mdatp-service-is-running-but-eicar-text-file-detection-doesnt-work"></a><span data-ttu-id="4cc1f-150">Si le service mdatp est en cours d'exécution, mais que la détection de fichier texte EICAR ne fonctionne pas</span><span class="sxs-lookup"><span data-stu-id="4cc1f-150">If mdatp service is running, but EICAR text file detection doesn't work</span></span>

1. <span data-ttu-id="4cc1f-151">Vérifiez le type de système de fichiers à l'aide des :</span><span class="sxs-lookup"><span data-stu-id="4cc1f-151">Check the file system type using:</span></span>

    ```bash
    findmnt -T <path_of_EICAR_file>
    ```

    <span data-ttu-id="4cc1f-152">Les systèmes de fichiers actuellement pris en charge pour l'activité d'accès sont répertoriés [ici.](microsoft-defender-endpoint-linux.md#system-requirements)</span><span class="sxs-lookup"><span data-stu-id="4cc1f-152">Currently supported file systems for on-access activity are listed [here](microsoft-defender-endpoint-linux.md#system-requirements).</span></span> <span data-ttu-id="4cc1f-153">Les fichiers en dehors de ces systèmes de fichiers ne seront pas analysés.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-153">Any files outside these file systems won't be scanned.</span></span>

## <a name="command-line-tool-mdatp-isnt-working"></a><span data-ttu-id="4cc1f-154">L'outil de ligne de commande « mdatp » ne fonctionne pas</span><span class="sxs-lookup"><span data-stu-id="4cc1f-154">Command-line tool “mdatp” isn't working</span></span>

1. <span data-ttu-id="4cc1f-155">Si l'exécution de l'outil en ligne de `mdatp` commande donne une `command not found` erreur, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4cc1f-155">If running the command-line tool `mdatp` gives an error `command not found`, run the following command:</span></span>

    ```bash
    sudo ln -sf /opt/microsoft/mdatp/sbin/wdavdaemonclient /usr/bin/mdatp
    ```

    <span data-ttu-id="4cc1f-156">et essayez à nouveau.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-156">and try again.</span></span>

    <span data-ttu-id="4cc1f-157">Si aucune des étapes ci-dessus ne vous aide, collectez les journaux de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="4cc1f-157">If none of the above steps help, collect the diagnostic logs:</span></span>

    ```bash
    sudo mdatp diagnostic create
    ```

    ```Output
    Diagnostic file created: <path to file>
    ```

    <span data-ttu-id="4cc1f-158">Le chemin d'accès à un fichier zip qui contient les journaux s'affiche en tant que sortie.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-158">Path to a zip file that contains the logs will be displayed as an output.</span></span> <span data-ttu-id="4cc1f-159">À l'aide de ces journaux, connectez-vous au support technique.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-159">Reach out to our customer support with these logs.</span></span>
